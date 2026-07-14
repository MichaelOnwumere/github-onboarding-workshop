# My Notes — Imaobong Uwah

---

## Key Concepts I Learned

<!-- Write the main ideas covered in today's session -->

- During the session, I learned how organizations secure cloud environments using Microsoft Entra Privileged Identity Management (PIM), Just-in-Time (JIT) access, Multi-Factor Authentication (MFA), and approval-based role activation. I understood the difference between Eligible and Active role assignments and how time-bound access reduces the risk of unauthorized privilege use.

- I learned the importance of Zero Trust security, the Shared Responsibility Model, the Principle of Least Privilege, and Conditional Access Policies.

- On API authentication for declarative agents with secured APIs task, I learned that declarative agents can connect to protected APIs through authenticated plugins, and that proper authentication, and Microsoft 365 Copilot access are required before the integration can function.

- I also learned about API Keys and OAuth-based access flows, registering applications and configuring permissions, securing API endpoints for Microsoft 365 declarative agents, using the Microsoft 365 Agents Toolkit to build and test agents, and ensuring agents only access approved organizational data.

---

## Lab / Hands-On Work

- I completed some practical activities related to exploring Microsoft Entra Privileged Identity Management, assigning eligible administrator roles, configuring JIT access and activation duration, enabling MFA for role activation, reviewing approval workflows and role assignments, observing privileged access monitoring and auditing.

- I also followed the demonstration on authenticating an API plugin for declarative agents from Microsoft Learn study page, although I was unable to complete the practical exercise due to an access issue.

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->

### What I did

- I practiced the PIM configuration steps in Microsoft Entra ID. I reviewed how privileged roles are activated, approved, and monitored.
  
- I attempted to activate the Microsoft 365 Agents Toolkit extension and connect a secured API plugin for a declarative agent.

### What happened / Result

- I successfully completed the PIM demonstrations. I was able to understand how temporary privileged access, approval workflows, and MFA work together to reduce security risks. The exercises showed that organizations can improve security by replacing permanent administrator privileges with controlled, time-limited access.

- For the Authenticate Your API Plugin for Declarative Agents with Secured APIs task, I was not able to complete the hands-on practical. When I attempted to launch the exercise using the Microsoft 365 Agents Toolkit, I received the following error: “Microsoft 365 account administrator hasn't enabled Copilot access for this account.” 

The message indicated that my account was not enrolled in the Microsoft 365 Copilot Early Access Program, which is a prerequisite for testing declarative agents with secured APIs. However, I could follow Microsoft learn lab’s explanation and understood the configuration process a bit, but I could not complete the practical deployment and testing steps.

### Challenges I faced

- Initially, I was unable to distinguish between Eligible and Active role assignments.
  
- Unable to complete the API authentication practical because my Microsoft 365 account was not enabled for Microsoft 365 Copilot access.

---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->
- Privileged access should be temporary and granted only when needed.
  
- MFA is essential for protecting privileged accounts and where possible, for all user accounts.
  
- The Principle of Least Privilege reduces the impact of compromised accounts.
  
- Zero Trust requires continuous verification of users and devices.
  
- Regular access reviews, monitoring, encryption, backups, and patching are critical security practices.
  
- AI and declarative agents must use secured APIs and proper authentication to prevent unauthorized access to organizational data.
  
- User awareness remains an important defense against phishing and social engineering attacks.
  
- This session improved my understanding of privileged access management and an understandingsecured API authentication for declarative agents. The practical PIM exercises showed how organizations can reduce risk through JIT access, MFA, approval workflows, and continuous monitoring. Although I could not complete the API authentication hands-on exercise because my account lacked Microsoft 365 Copilot access, I gained a fair understanding of the required prerequisites and authentication workflow. Overall, the session strengthened my knowledge of identity protection, cloud security best practices, and secure access management in modern enterprise environments.
  
- The biggest lesson I gained from this session is that cybersecurity is a continuous process. Organizations must regularly review their security controls, educate users, monitor systems, and adapt to emerging threats to maintain a strong security posture.

---

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->

- How does Microsoft Entra PIM integrate with third-party identity providers and non-Microsoft cloud platforms?

---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->

- The community's Youtube page
- Microsoft Entra ID documentation
- Microsoft Learn modules on Privileged Identity Management (PIM)
- Microsoft Learn resources on Zero Trust and Conditional Access
- Azure Portal practical demonstrations
- Microsoft documentation on Multi-Factor Authentication (MFA)
- Microsoft documentation on securing APIs for declarative agents and Microsoft 365 Copilot extensibility
---

*Submitted by: Imaobong Uwah · imauwah
