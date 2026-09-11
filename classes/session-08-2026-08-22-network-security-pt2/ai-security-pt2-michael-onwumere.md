# My Notes — Michael Chinonso Onwumere

---

## Key Concepts I Learned

- Learned that **AI systems introduce risk at three distinct layers** that traditional app security doesn't fully cover:
  - **The Traffic Layer** — the path requests take to reach a model, secured by an **AI Gateway**.
  - **The Interaction Layer** — the actual prompts going in and responses coming out, secured by **Guardrails**.
  - **The Platform Layer** — the underlying compute, storage, and services hosting the AI workload, secured by **Defender for Cloud**.
- Learned how an **AI Gateway secures model traffic**:
  - The AI Gateway (powered by **Azure API Management / APIM**) sits between callers (apps, agents, services) and the actual model deployments, acting as a **reverse proxy**.
  - It **authenticates callers**, applies **rate limits**, **logs traffic**, and **routes requests** to the correct model deployment.
  - Model deployments only receive requests **after gateway validation succeeds**.
  - Traffic and logs flow into **Azure Monitor / Log Analytics** for diagnostic logs, KQL queries, dashboards, and alerts.
  - **Without a gateway**, there is no per-caller authentication, no rate limiting or quota control, and no centralized audit trail — which is especially risky since agents can call a model many times per user interaction.
- Learned the difference between **API keys and Microsoft Entra ID tokens** as authentication methods for calling AI models, and why Entra ID tokens are generally the stronger option for identity-based access control.
- Learned about **Guardrails and Microsoft Content Safety**, which evaluate both user inputs and model outputs in real time, with no separate setup required:
  - **Input Protections** — review prompts before they reach the model, to detect and block jailbreaks, indirect attacks, and policy violations.
  - **Output Protections** — evaluate model responses to prevent the release of unsafe, confidential, or ungrounded information.
  - What guardrails give teams: prevention of harmful/sensitive content ingestion or release, enforcement of internal data-handling and acceptable-use policies, detection and mitigation of prompt injection or jailbreak attempts, and stronger compliance/audit readiness.
- Learned the **five core safety controls in Microsoft Foundry**:
  1. **Prompt Shields** — detect jailbreak and indirect prompt-injection attempts, with modes for annotate-only or annotate-and-block.
  2. **Content Filters** — classify violence, hate, sexual, and self-harm content, with a severity slider per category.
  3. **Blocklists** — block exact terms or regex patterns, such as project names, proprietary code, or internal identifiers.
  4. **Protected Material Detection** — flags proprietary or non-Microsoft content appearing in generated text or code, with annotate or block options.
  5. **Groundedness Detection (preview)** — evaluates whether a response is actually supported by its source data, flagging fabricated statements.
- Learned about **detecting AI threats with Cloud Workload Protection (CWP)**:
  - CWP continuously analyzes runtime signals from VMs, containers, and managed AI services, correlating them with **AI-specific threat intelligence**.
  - It looks for things like unusual access patterns to model/data storage accounts, code injection or privilege escalation within containers hosting inference workloads, unauthorized outbound connections from compute nodes running AI models, and anomalous API calls (possible abuse of an AI service endpoint).
  - Alerts can be found via **Defender for Cloud → Security alerts**, filtered by Product Component Name = AI / AIServices.
  - Alert details include a description of the detected behavior, impacted resources, evidence from logs and related entities, a "Prompt Suspicious Segment" (preview), and recommended actions.
- Pulled it all together into a **layered security model for AI workloads**:
  1. **AI Gateway** — authenticates callers, enforces rate limits, logs every request before it reaches a model.
  2. **Guardrails** — filter unsafe or policy-violating prompts and responses at the model interaction layer.
  3. **Defender for Cloud** — discovers AI resources, hardens posture, and detects runtime threats platform-wide.
  - The overall pattern: **control the traffic, govern the interaction, protect the platform** — with unified visibility tied together in **Defender XDR**, linking every alert back to a single investigation.

---

## Lab / Hands-On Work

### What I did

This session was again run as a mentorship walkthrough, so I followed along with the instructor's demonstration and slides rather than configuring resources myself. This included:

1. Reviewing the three-layer AI risk model (Traffic, Interaction, Platform) and how each layer maps to a specific control.
2. Walking through how an **AI Gateway (APIM)** sits in front of model deployments as a reverse proxy, and what breaks down without one (no per-caller auth, no rate limiting, no audit trail).
3. Comparing **API keys vs Microsoft Entra ID tokens** as ways to authenticate calls to AI models.
4. Reviewing **Guardrails and Microsoft Content Safety**, including input protections (before the model) and output protections (after the model).
5. Going through the **five core safety controls in Foundry**: Prompt Shields, Content Filters, Blocklists, Protected Material Detection, and Groundedness Detection.
6. Observing how **Cloud Workload Protection (CWP)** detects AI-specific threats and where to find related alerts in **Defender for Cloud**.
7. Reviewing the **layered security model** that ties AI Gateway, Guardrails, and Defender for Cloud together, with Defender XDR providing unified visibility across all three.

### What happened / Result

- I got a much clearer picture of AI security as three separate but connected problems — securing the traffic reaching the model, securing the actual prompts/responses, and securing the platform the model runs on — rather than one single thing to "lock down."
- I understood why an AI Gateway matters more for agents than for typical apps, since an agent can call a model dozens of times per single user interaction, which multiplies the blast radius of missing rate limits or missing per-caller logging.
- I saw how Guardrails and Microsoft Content Safety work "for free" without separate setup, which makes them a very accessible first line of defense against jailbreaks and prompt injection.
- The five Foundry safety controls gave me a much more concrete sense of what "content safety" actually means in practice — it isn't just one filter, it's five distinct controls each targeting a different risk (jailbreaks, harmful content categories, leaked internal terms, IP leakage, and hallucinated/ungrounded answers).
- I connected this back to the previous AI Security session on agent identity — Entra ID tokens and Conditional Access secure who/what can call the model, while this session's Gateway, Guardrails, and Defender for Cloud secure how the call happens and what happens on either side of it.

### Challenges I faced

- Since I didn't get hands-on access to actually configure an AI Gateway or Guardrails myself, my understanding is still largely conceptual at this stage.
- Distinguishing exactly when to use API keys versus Entra ID tokens in a real project setup wasn't fully clear to me yet.
- The five Foundry safety controls were introduced quickly, and I want to spend more time understanding the practical difference between "annotate only" and "annotate and block" modes, and when each is appropriate.
- Understanding how CWP correlates runtime signals with AI-specific threat intelligence (versus generic cloud threat intelligence) needs more review on my end.

---

## My Takeaways

My biggest takeaway from this session is that **securing AI workloads isn't a single control, it's a layered pattern**: control the traffic (AI Gateway), govern the interaction (Guardrails), and protect the platform (Defender for Cloud) — with Defender XDR stitching all three together into one investigation view.

I also took away that **guardrails aren't just about blocking "bad" content** — they cover a much wider surface than I expected, from jailbreak detection to protecting proprietary code and catching hallucinated, ungrounded responses. That last one (Groundedness Detection) stood out to me, since it's less about "safety" in the traditional sense and more about trustworthiness of the AI's answers.

Finally, seeing how an agent's high call volume through the AI Gateway ties back to the previous session's point about agent identity and least privilege reinforced that **AI security threads through everything** — identity, network/traffic, interaction content, and the underlying platform all need to work together.

---

## Questions I Still Have

- In a real project, is it standard practice to use Entra ID tokens exclusively for model calls, or are API keys still common for simpler/internal scenarios?
- How is the severity slider on Content Filters typically tuned in production — is there a recommended starting baseline?
- How mature is Groundedness Detection given it's still in preview — is it reliable enough to depend on for compliance-sensitive use cases yet?
- How does Defender XDR actually correlate an AI Gateway log, a Guardrails block, and a Defender for Cloud alert into a single investigation in practice?

---

## Resources I Found Useful

- Microsoft Foundry documentation — Safety Controls (Prompt Shields, Content Filters, Blocklists, Protected Material Detection, Groundedness Detection)
- Azure API Management (APIM) as an AI Gateway
- Microsoft Content Safety documentation
- Microsoft Defender for Cloud — Cloud Workload Protection (CWP) for AI
- Microsoft Defender XDR

---

*Submitted by: Michael Chinonso Onwumere · MichaelOnwumere*
