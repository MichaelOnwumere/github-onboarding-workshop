# My Notes — Alex Agyei

---

## Key Concepts I Learned

* Microsoft Entra ID: A cloud-based Identity and Access Management (IAM) solution that securely manages user identities, authentication, and access to applications and resources across cloud and hybrid environments.
* Identity in Defense in Depth: Identity is a critical layer of Microsoft's Defense in Depth strategy, ensuring that only authenticated and authorized users can access organizational resources through strong authentication and access controls.
* Multi-Factor Authentication (MFA): Enhances account security by requiring multiple forms of verification, reducing the risk of unauthorized access even if passwords are compromised.
* Security Defaults: Microsoft Entra's built-in baseline security settings that automatically enforce essential protections, such as MFA for administrators and blocking legacy authentication methods.
* Conditional Access: A policy-based access control feature that uses "If...Then..." logic to grant or restrict access based on factors such as user identity, device compliance, location, application, and sign-in risk.
* Conditional Access Deployment Strategy: Implementing Conditional Access should follow a phased approach by testing policies with a pilot group first to prevent user lockouts and minimize disruptions before organization-wide deployment.
* Privileged Identity Management (PIM): Protects privileged accounts by providing just-in-time (JIT) administrative access, ensuring elevated permissions are granted only when needed and for a limited time, reducing security risks.

---

## Lab / Hands-On Work

I worked on integrating a Microsoft 365 Copilot Declarative Agent with an API secured using an API key.

### What I did

* Set up the Declarative Agent with API Plugin project in Visual Studio Code.
* Reviewed the project structure, including the agent manifest and plugin configuration files.
* Configured the API endpoint and API key authentication settings.
* Explored how Microsoft 365 Copilot plugins securely connect to external APIs using API key authentication.
* Attempted to validate and test the agent within the Microsoft 365 environment.

<img width="787" height="418" alt="Screenshot 2026-07-10 093543" src="https://github.com/user-attachments/assets/d3457248-873b-4842-8bf1-f83f3e166daf" />

<img width="1302" height="762" alt="Screenshot 2026-07-10 094109" src="https://github.com/user-attachments/assets/27110813-a7e9-4d53-ac5b-9c7830417876" />



### What happened / Result

* Installed the Microsoft 365 Agents Toolkit extension in Visual Studio Code.
* Created a new API Plugin for Microsoft 365 Copilot using the provided project template.
* Explored the generated project structure, including the agent manifest, plugin configuration files, and Azure Functions template.

### Challenges I faced

I was unable to complete the deployment and testing phase because my Microsoft 365 account did not have the required Microsoft 365 subscription and Copilot access. As shown in the development environment, Copilot access was disabled, preventing the upload and testing of the custom agent.

<img width="1418" height="520" alt="Screenshot 2026-07-11 065932" src="https://github.com/user-attachments/assets/04806a90-896b-4dc9-ac9a-6500bae8f3db" />


---

## My Takeaways

Today's session deepened my understanding of how Conditional Access strengthens security in Microsoft Entra by making access decisions based on multiple factors, rather than relying solely on user authentication. I learned that access can be granted, blocked, or require additional verification depending on conditions such as user identity, device compliance, location, and sign-in risk. I also recognized the importance of deploying Conditional Access policies carefully by testing them in Report-only mode first, helping organizations identify potential issues and avoid unintended disruptions before enforcing them in production.

---

*Submitted by: Alex Agyei · lexisbil1*
