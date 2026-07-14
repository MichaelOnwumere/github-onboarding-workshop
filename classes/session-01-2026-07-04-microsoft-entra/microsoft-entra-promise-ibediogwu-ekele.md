# My Notes — [Promise Ibediogwu Ekele]

## Key Concepts I Learned

### From the session we had last week and the Microsoft Learn Link shared by the mentor, i learnt the following:

- **Conditional Access (CA)** is the policy engine in Microsoft Entra that evaluates signals such as user identity, device platform, location, application, and sign-in risk before allowing, blocking, or requiring additional authentication like Multi-Factor Authentication (MFA).
- **Privileged Identity Management (PIM)** implements the Principle of Least Privilege by providing Just-in-Time (JIT) access instead of permanent administrative privileges.
- **API plugins** enable Microsoft 365 Copilot Declarative Agents to securely communicate with external applications and enterprise APIs.
- I learned the two authentication methods supported by Microsoft 365 Copilot API plugins:
  - **API Key Authentication**, which uses a shared secret to authenticate API requests.
  - **OAuth 2.0 Authentication**, which authenticates individual users through Microsoft Entra ID using access tokens for secure, user-specific access.
- I also learned that enterprise security extends beyond protecting user identities to securing APIs, applications, and organizational data through proper authentication and authorization mechanisms.

---

# Lab / Hands-On Work

## What I did

### Microsoft Entra Security Lab

- Explored Microsoft Entra Conditional Access.
- Created a Conditional Access policy and assigned it to a test group.
- Configured policy conditions, including targeting a specific device platform.
- Tested the policy using a user account assigned to the targeted group.
- Used **Report-only mode** and **Sign-in Logs** to troubleshoot the policy behavior.

### Microsoft 365 Copilot API Plugin Module

- Followed the Microsoft Learn module on authenticating API plugins for Microsoft 365 Copilot Declarative Agents.
- Studied the implementation process for both **API Key Authentication** and **OAuth 2.0 Authentication**.
- Attempted to begin the practical exercise in Visual Studio Code using the Microsoft 365 Agents Toolkit.

---

## What happened / Result

### Microsoft Entra Security Lab

- The Conditional Access policy did not block my sign-in as I initially expected.
- After troubleshooting, I discovered that I had not configured the appropriate **Target Resource (Cloud App)**, meaning the policy had nothing to protect.
- I also realized that I configured the policy for **Android devices** but performed my test on a **Windows PC**, so the policy conditions were not satisfied.
- This helped me understand how Conditional Access evaluates all configured conditions before enforcing a policy.

### Microsoft 365 Copilot API Plugin Module

- I was unable to complete the practical exercises for both **API Key Authentication** and **OAuth 2.0 Authentication**.
- While setting up the project, I encountered an error indicating that my Microsoft 365 account did not have **Microsoft 365 Copilot access enabled**, which is required to create and test Copilot Declarative Agents using the Microsoft 365 Agents Toolkit.
- Following the mentor's instruction, I skipped the hands-on exercises and focused on understanding the concepts, authentication flow, and configuration process presented in the Microsoft Learn module.
- Although I did not perform the practical implementation, I gained a solid understanding of how API plugins authenticate securely using API Keys and OAuth 2.0, and why OAuth is the preferred approach for enterprise applications.

---

## Challenges I faced

- Understanding why my Conditional Access policy did not trigger during testing.
- Learning how policy conditions interact with device platforms and targeted cloud applications.
- Being unable to complete the Microsoft 365 Copilot API plugin practical exercises because my Microsoft 365 account did not have the required Copilot license and access permissions.
- Understanding the authentication flow between Microsoft Entra ID, API plugins, and Microsoft 365 Copilot without being able to perform the hands-on implementation.

---

# My Takeaways

This session reinforced that **identity is the new security perimeter** in modern cloud environments, and protecting identities also means protecting the applications and APIs they access.

From the Microsoft Entra session, I learned that Conditional Access is an intelligent policy engine that evaluates multiple signals before granting or denying access, while Privileged Identity Management reduces security risks by providing Just-in-Time administrative access.

Although I was unable to complete the Microsoft 365 Copilot API plugin practical exercises due to licensing restrictions, I developed a clear understanding of how Copilot securely communicates with external APIs. I learned the differences between API Key and OAuth 2.0 authentication, the role of Microsoft Entra ID in issuing access tokens, and why OAuth is the recommended authentication method for enterprise solutions.

Overall, these sessions helped me appreciate that effective cloud security requires a combination of identity protection, least-privilege access, secure API authentication, and continuous governance to safeguard organizational resources.

---

# Questions I Still Have

- How are multiple Conditional Access policies evaluated when more than one policy applies to the same user and cloud application?
- What are the best practices for designing Conditional Access policies in production environments without accidentally locking out administrators?
- Besides obtaining a Microsoft 365 Copilot license, are there alternative ways to practice building and testing Copilot API plugins in a development environment?
- How does Microsoft Entra ID manage token refresh and token expiration for OAuth-authenticated API plugins used by Microsoft 365 Copilot?

---

# Resources I Found Useful

- [Microsoft Learn – Microsoft Entra Conditional Access](https://learn.microsoft.com/en-us/training/modules/implement-conditional-access/)
- [Microsoft Learn – Microsoft Entra Privileged Identity Management (PIM)](https://learn.microsoft.com/en-us/training/modules/describe-capabilities-of-microsoft-entra-privileged-identity-management/)
- [Microsoft Learn – Authenticate your API plugin for Declarative Agents with secured APIs](https://learn.microsoft.com/en-us/training/modules/copilot-declarative-agent-api-plugin-auth/)
- [Microsoft Learn – SC-500: Microsoft Security Copilot Learning Path](https://learn.microsoft.com/en-us/training/paths/security-copilot/)
- Microsoft Cloud & AI Security Bootcamp 2026 (Microsoft Naija Security User Group) Session Recording *(Internal Resource)*
- [Microsoft Learn – Microsoft Entra Sign-in Logs Documentation](https://learn.microsoft.com/en-us/entra/identity/monitoring-health/concept-sign-ins)

*Submitted by: Promise Ibediogwu Ekele · https://github.com/promibe*
