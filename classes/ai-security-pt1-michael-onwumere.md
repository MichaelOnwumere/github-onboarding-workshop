# My Notes — Michael Chinonso Onwumere

---

## Key Concepts I Learned

- Learned **why AI security is different** from traditional cloud security: AI systems inherit every existing cloud risk, but also add their own, since models, prompts, grounding data, and agents create an attack surface that traditional controls were never designed for. Key drivers of this include:
  - **New attack techniques** — prompt injection, jailbreaking, and model manipulation target the model itself, not just the underlying host.
  - **Data exposure at speed** — generative AI can surface oversharing and sensitive content almost instantly, so labels and DLP (Data Loss Prevention) need to travel with the data itself.
  - **Sprawling AI estate** — shadow AI apps, agents, and multicloud model deployments can appear faster than governance processes can keep up with.
  - **Layered architecture** — AI workloads span the application, model, and infrastructure layers, and each layer needs its own guardrails.
  - **Runtime blind spots** — suspicious prompts and anomalous model usage often only surface with dedicated AI threat detection, not traditional monitoring.
  - **Identity and governance** — externally reachable AI endpoints demand strong authentication and least-privilege identity, just like any other exposed resource.
- Learned how an **AI agent gets access** to a resource, following this flow:
  1. The agent requests a token from **Microsoft Entra ID**.
  2. **Conditional Access** evaluates the request against configured policies.
  3. The token is either **issued or blocked** based on that evaluation.
  4. The **source (resource) validates and authorizes** the token before granting access.
- Learned the **two agent access patterns**:
  - **On-Behalf-Of (OBO)** — a **delegated** pattern, where the agent acts on behalf of a signed-in user.
  - **Client credentials** — an **autonomous** pattern, where the agent acts on its own, without a user in the loop.
- Reviewed the **four pillars of controlling agent access and lifecycle**:
  1. **Create with least privilege** — give the agent only the permissions its task needs, since over-privilege is what turns an incident into a breach.
  2. **Operate under policy** — keep Conditional Access scoped to the agent identity so every token request is evaluated.
  3. **Review and re-certify** — revisit agent permissions and blueprints as the agent's purpose changes over time.
  4. **Retire cleanly** — handle lifecycle events properly, disabling credentials and removing access when an agent is decommissioned or compromised.
- Learned about **Microsoft Defender XDR** as the tool used to analyze AI identity risks, covering:
  - **Blast radius assessment** — understanding how far a compromised agent's access could actually reach.
  - **Attack path analysis** — tracing how an attacker could move from one identity or resource to another.
  - **AI agent inventory** — a dedicated view in the Defender portal that discovers and lists AI agents across the environment.
  - **Alerts** and **Advanced Hunting** — used to detect and investigate suspicious AI agent activity.
- Learned about **real-time protection for Copilot Studio agents**, enabled through **Defender for Cloud Apps**, which extends monitoring and protection to agents built in Copilot Studio.
- Session was structured around four modules: securing access for Microsoft Entra Agent Identity, analyzing AI identity risks with Defender XDR, enabling real-time protection for Copilot Studio agents, and a wrap-up covering licensing, prerequisites, and an end-to-end checklist.

---

## Lab / Hands-On Work

### What I did

This session was run as a mentorship walkthrough rather than a self-paced lab, so I followed along with the instructor's demonstration and slides rather than configuring resources myself. This included:

1. Going through the **"Why AI security is different"** case, covering the six risk areas (new attack techniques, data exposure at speed, sprawling AI estate, layered architecture, runtime blind spots, and identity/governance).
2. Walking through the **agent authentication flow** — from token request at Entra ID, through Conditional Access evaluation, to token issuance and validation at the resource.
3. Comparing the **On-Behalf-Of (delegated)** and **Client credentials (autonomous)** access patterns for agents.
4. Reviewing the **agent access and lifecycle framework**: create with least privilege, operate under policy, review and re-certify, and retire cleanly.
5. Observing a walkthrough of **Microsoft Defender XDR**, including the AI agent inventory, blast radius assessment, and attack path analysis.
6. Reviewing how **alerts** and **advanced hunting** are used to investigate suspicious agent behavior in Defender.
7. Seeing how **Defender for Cloud Apps** is turned on to provide real-time protection for Copilot Studio agents, and how its outputs are verified.

### What happened / Result

- I gained a clearer picture of AI agents as a new kind of identity that needs to be governed just as carefully as human identities, with its own token flow through Entra ID and Conditional Access.
- I understood the practical difference between a **delegated (OBO)** agent, which is tied to a user's context, and an **autonomous (client credentials)** agent, which acts independently, and why each pattern carries different risk considerations.
- I saw how the lifecycle framework (create, operate, review, retire) gives a repeatable process for managing agent identities responsibly, rather than treating agent creation as a one-off event.
- I saw how Defender XDR brings AI-specific visibility, like agent inventory and blast radius, into the same portal used for broader security monitoring, which makes AI risk feel less like a separate silo.
- I connected this session's identity/access focus to previous sessions on NSGs, ASGs, and Azure Firewall — the underlying idea of least privilege and centralized policy enforcement keeps showing up, just applied to a new type of identity (agents) instead of network traffic.

### Challenges I faced

- Since this was a walkthrough rather than a hands-on lab, I did not get to configure Conditional Access policies or explore the Defender portal directly myself, so my understanding is still mostly conceptual.
- Distinguishing clearly between the OBO and client credentials patterns, and knowing when each should be used, took some extra thought.
- The difference between "alerts" and "advanced hunting" in Defender XDR, and when to use one over the other, was introduced quickly and I'd like to explore this further.
- I plan to revisit the Microsoft Learn modules on Entra Agent ID and Defender for Cloud Apps to reinforce what was covered.

---

## My Takeaways

My biggest takeaway from this session is that **AI agents are identities, and identities need the same lifecycle discipline as any other access-granting entity** — least privilege at creation, policy enforcement during operation, periodic re-certification, and clean retirement when done.

I also took away that **AI security isn't a separate discipline bolted onto cloud security — it extends it.** The same principles from earlier sessions (least privilege, centralized policy, layered defense) apply here, but AI adds new attack surfaces like prompt injection and model manipulation that traditional NSGs or firewalls were never built to catch.

Finally, seeing Defender XDR extend into AI agent inventory and blast radius analysis showed me that visibility is just as important for AI identities as it is for network traffic — you can't secure what you can't see or map.

---

## Questions I Still Have

- In practice, how does an organization decide whether an agent should use the OBO (delegated) pattern or client credentials (autonomous) pattern?
- What does "blast radius" look like in a real incident involving a compromised agent, and how quickly can Defender XDR surface that?
- How do advanced hunting queries differ from standard alerts when investigating AI agent activity in Defender?
- What licensing is actually required to get real-time protection for Copilot Studio agents through Defender for Cloud Apps?

---

## Resources I Found Useful

- Microsoft Entra Agent ID documentation
- Microsoft Defender XDR — AI agent inventory and blast radius
- Microsoft Defender for Cloud Apps
- Microsoft Copilot Studio security documentation
- Conditional Access documentation (Microsoft Entra ID)

---

*Submitted by: Michael Chinonso Onwumere · MichaelOnwumere*
