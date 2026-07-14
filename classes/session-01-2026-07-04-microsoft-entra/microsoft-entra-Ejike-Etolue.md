# My Notes — Ejike Etolue

---

## Key Concepts I Learned

- **Entra ID as the Identity Gatekeeper:** Confirmed that Entra ID remains the primary control plane for securing resource access boundaries. It works just like registering standard enterprise applications, but now we are applying those identical security perimeters to AI tools.
- **Declarative Agents & APIs:** Gained insight into how a declarative agent acts like a smart assistant that needs to fetch data from a locked room. The API plugin serves as the door to our backend, making its authentication setup critical to prevent unauthorized data exposure.
- **OAuth 2.0 vs. API Keys:** Gained a clearer view of the two primary plugin authentication methods. OAuth 2.0 acts like a valet key, giving Copilot delegated access to act on behalf of the user without handing over master credentials, while API keys function as a simpler, less granular service-to-service token.
- **Behind-the-Scenes Token Exchanges:** Looked at how Microsoft Copilot manages the heavy lifting of authentication flows in the background. It safely passes authorization codes and access tokens to backend APIs so the end-user doesn't experience credential friction.

---

## Lab / Hands-On Work

### What I did
- Reviewed the core architectural methodologies from the first official live session: *"Secure Access to Resources using Microsoft Entra"*.
- Went through the required Microsoft Learn module focusing on authenticating API plugins for declarative agents.
- Evaluated how OpenAPI description files and agent manifests explicitly define OAuth endpoints and permission scopes to govern what an AI agent can read or write.

### What happened / Result
- Mapped out the configuration steps needed to register an API plugin within an Entra tenant, including configuring redirect URIs and exposing application scopes.
- Verified how a plugin's manifest file directly pairs with Entra application permissions to enforce strict data boundaries.

### Challenges I faced
- Time management is the toughest bottleneck right now. Between clocking weekend overtime at my full-time infrastructure role and trying to clear my backlog of AZ-104 study labs for Q3, sitting down to dissect app manifests requires serious mental gymnastics. Fortunately, leveraging my SC-300 foundation helped me parse these Entra ID configurations quickly without getting stuck on the basics.

---

## My Takeaways

As an engineer managing infrastructure security, this session hits home. We used to spend all our time securing user-to-application traffic; now we are securing AI-to-API traffic. If we don't lock down these declarative agent plugins using proper Entra identity boundaries and delegated OAuth scopes, we are essentially letting an AI assistant roam our backend with a master key. It's a natural evolution of what I focused on during the SC-300 cohort, just modernized for the AI stack.

---

## Questions I Still Have

- When a declarative agent calls an Entra-protected API via OAuth, how does Entra ID handle mid-session Conditional Access updates? If a user's risk level spikes while Copilot is interacting with a backend plugin, does Entra instantly revoke the delegated token, or is there a processing lag?
- Balancing an intense work schedule and AZ-104 study time this quarter means I'm stretched thin, what are the most critical practical lab milestones in this SC-500 bootcamp that I should prioritize to stay on track for my Q4 exam goal without burning out?

---

## Resources I Found Useful

- **First Class Recording:** [Secure Access to Resources using Microsoft Entra - MNSUG YouTube Session](https://youtu.be/R7zxI-k3NoQ)
- **Assigned Training Module:** [Authenticate your API plugin for declarative agents with secured APIs - Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/copilot-declarative-agent-api-plugin-auth/)
- **Community Workspace:** [GitHub Onboarding Workshop Classes Directory](https://github.com/AGK001/github-onboarding-workshop)

---

*Submitted by: Ejike Etolue · AGK001*