# My Notes — MICHAEL CHINONSO ONWUMERE

**Cloud Security & AI Bootcamp – Session Report**

**Date :	Saturday, July 4, 2026**

**Mentor :	Emmanuel Itoje / Uchechukwu Azunna**

**Moderator :	Amos Adereti**

**Microsoft Learn resources :	https://learn.microsoft.com/en-us/training/paths/secure-access-resources-entra/**

**Modules Covered :	Secure access to resources using Microsoft Entra**

About This Session

This session focused on securing access to organizational resources using Microsoft Entra ID. We explored how identity serves as the foundation of cloud security and learned how Microsoft Entra enables organizations to protect users, applications, and resources through strong authentication, Conditional Access policies, and Privileged Identity Management (PIM).

The session combined theoretical concepts with practical demonstrations and hands-on labs, providing experience in configuring secure access controls and managing privileged identities.

# Key Concepts I Learned
The role of Microsoft Entra ID in Identity and Access Management (IAM).
Different authentication methods supported by Microsoft Entra, including passwordless authentication, Multi-Factor Authentication (MFA), Temporary Access Pass (TAP), Passkeys, and FIDO2 security keys.
Authentication strength and how stronger authentication methods reduce the risk of unauthorized access.
How Conditional Access policies evaluate user identity, device compliance, application, location, and risk before granting or blocking access.
The importance of Self-Service Password Reset (SSPR) in improving user productivity while maintaining security.
The principles of Zero Trust security, where every access request is verified before permission is granted.
How Privileged Identity Management (PIM) enables Just-in-Time (JIT) access, reducing the risk associated with permanent administrative privileges.
The principle of least privilege and why users should only receive the permissions necessary to perform their duties and Lab/Hands-On Work

What I Did :

During the practical session, I completed hands-on exercises using the Microsoft Entra admin center.

# The activities included:

Exploring the available authentication methods within Microsoft Entra.
Reviewing authentication strength policies and understanding when different authentication methods should be used.
Creating and configuring a Conditional Access policy to secure user sign-ins based on defined conditions.
Testing how Conditional Access evaluates access requests before granting permissions.
Exploring Microsoft Entra Privileged Identity Management (PIM).
Activating eligible administrative roles using Just-in-Time access.
Understanding the approval process, activation duration, and auditing capabilities provided by PIM.

below are the Images for my hands-on exercise on Conditional Access policy and Privilege Identity Management 

# Configuring a Conditional Access policy in Microsoft Entra Admin Center.
<img width="1050" height="460" alt="lab 1" src="https://github.com/user-attachments/assets/f51b2f55-8cd3-4b25-8514-2172d9beb0ab" />
<img width="1050" height="550" alt="lab 2" src="https://github.com/user-attachments/assets/ff416870-5028-4ad1-84c7-ed3d9e47f2ad" />
<img width="882" height="558" alt="lab3" src="https://github.com/user-attachments/assets/f7e4cab7-df7e-41b7-a86b-110e4706e617" />
<img width="1326" height="512" alt="lab4" src="https://github.com/user-attachments/assets/00b6e1df-c747-4d44-a02d-dd8e7722ddb0" />
<img width="1106" height="599" alt="lab5" src="https://github.com/user-attachments/assets/12d7c6f4-a3d4-4694-9bb7-3bdecccee34b" />

# Exploring Microsoft Entra Privileged Identity Management (PIM) and activating eligible administrative roles.
<img width="1286" height="577" alt="lab6" src="https://github.com/user-attachments/assets/9b209449-962a-4c87-afce-6bb34072dc33" />

# What Happened / Result

The labs demonstrated how Microsoft Entra secures organizational resources by ensuring users satisfy predefined security requirements before accessing applications.

I successfully:

Explored different authentication methods and authentication strengths.
Understood how Conditional Access policies evaluate multiple conditions before granting access.
Configured and tested a Conditional Access policy.
Learned how Just-in-Time administration minimizes security risks by eliminating permanent privileged access.
Gained practical experience navigating Microsoft Entra's identity security features.
Challenges I Faced
Understanding the order in which Conditional Access policies are evaluated.
Differentiating between authentication methods and authentication strength policies.
Understanding the workflow of Privileged Identity Management, particularly the distinction between eligible and active role assignments.
Navigating the numerous identity security options available within the Microsoft Entra Admin Center.

My Takeaways:

This session reinforced that identity is one of the most critical security boundaries in cloud environments. Protecting user identities is essential because every request to access cloud resources begins with authentication.

The practical labs helped me understand how Conditional Access strengthens security by making access decisions based on user identity, device compliance, location, and risk. I also learned how Privileged Identity Management enhances security by granting administrative privileges only when needed, reducing the attack surface and supporting the principle of least privilege.

Overall, the combination of authentication, Conditional Access, and PIM provides a layered security approach that aligns with Microsoft's Zero Trust architecture.

Questions I Still Have : 
How should organizations prioritize multiple Conditional Access policies when they apply to the same users?
What are the recommended best practices for deploying Privileged Identity Management in production environments with multiple administrators?

Resources I Found Useful :

Microsoft Learn – Secure access to resources using Microsoft Entra

Microsoft Entra Admin Center

Microsoft Learn documentation on Conditional Access

Microsoft Learn documentation on Privileged Identity Management (PIM)

Microsoft Learn documentation on Authentication Methods and Authentication Strength


# Authenticate API Plugins for Declarative Agents

Declarative agents for Microsoft 365 Copilot let you create AI-powered assistants optimized for specific scenarios. Using instructions, you define the context for the agent and configure its tone of voice or how it should respond. By integrating an agent with an API, you allow the agent to connect to external applications to retrieve data and perform actions.
# Example scenario
Suppose you work in a car repair shop. Your organization keeps track of the different repair requests using a specialized system. You and your colleagues regularly look up information about the different repairs. The current system offers a rudimentary search functionality that finds repairs only matching keywords. You would like to have an AI-powered assistant capable of answering questions about repairs, asked using natural language.
# Summary
This explains how to securely authenticate API plugins used by Microsoft 365 Copilot declarative agents when connecting to protected APIs. Since most enterprise APIs require authentication, developers must configure the appropriate authentication method so that the agent can securely access external services without exposing sensitive credentials.

# This covers two common authentication methods:
•	API Key Authentication – The API key is stored securely and referenced by the API plugin at runtime, allowing the declarative agent to access APIs that are protected by an API key without hardcoding the secret into the application.

•	OAuth Authentication – The declarative agent authenticates users through an identity provider such as Microsoft Entra ID. After the user signs in and grants consent, an access token is issued and used to securely call the protected API on the user's behalf. This approach is recommended for enterprise applications because it provides stronger security and supports delegated permissions. 
The module also includes hands-on exercises where developers integrate an API plugin with both an API Key-protected API and an OAuth protected API, then test the plugin in Microsoft 365 Copilot to verify that authentication and API communication work correctly. 

# My Key Takeaway
I learned that securing API plugins is a critical part of extending Microsoft 365 Copilot with declarative agents. Choosing the appropriate authentication method, API Key for simpler integrations or OAuth for enterprise scenarios, helps ensure that external APIs are accessed securely while protecting user identities and organizational resources. 


Submitted by: Michael Chinonso Onwumere · GitHub: @MichaelOnwumere
