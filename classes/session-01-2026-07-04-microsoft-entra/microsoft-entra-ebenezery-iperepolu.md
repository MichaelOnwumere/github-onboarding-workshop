# My Notes — [IPEREPOLU EBENEZERY A.]

#### Key Concepts I Learned

* API plugins for Microsoft 365 Copilot often need to connect to secured APIs rather than publicly accessible endpoints.
* The two common authentication methods for APIs are API Key authentication and OAuth 2.0 authentication.
* OAuth 2.0 enables secure, user-based access to resources by obtaining access tokens through an authorization flow.
* Declarative agents can securely call external APIs through authenticated API plugins.
* Proper authentication design improves the security, reliability, and user experience of Microsoft 365 Copilot extensions.

#### Lab / Hands-On Work

##### What I did

* Reviewed how secured APIs are integrated with Microsoft 365 Copilot declarative agents.
https://drive.google.com/file/d/1sjlPxxGU7Rx2bMj4BeCuYiTIECmHtRiA/view?usp=sharing

[Terminal screenshot](terminal-screenshot.png)

* Explored the differences between API Key and OAuth 2.0 authentication methods.
* Learned how to configure an API plugin to communicate with secured backend services.
* Studied how Microsoft Entra ID can be used to authenticate users and obtain access tokens for API calls.
* Observed the process of validating API plugin functionality within Microsoft 365 Copilot.

#### What happened / Result

* I gained a clearer understanding of how authentication works in API plugins for declarative agents.
* I learned when to use API Key authentication versus OAuth 2.0 based on security requirements and user context.
* I understood how secure authentication enables Copilot agents to access external systems safely without exposing credentials.



#### Challenges I faced

* Understanding the OAuth 2.0 authorization flow and token exchange process was initially challenging because it involves multiple components and security considerations.
* Distinguishing between scenarios that require API keys and those that require OAuth authentication required careful consideration of security and user identity requirements.



#### My Takeaways

* Security is a critical aspect of extending Microsoft 365 Copilot with external APIs.
* OAuth 2.0 is generally the preferred approach when APIs need to access user-specific data securely.
* Understanding authentication mechanisms helps build enterprise-grade Copilot solutions that are both secure and scalable.
* Microsoft Entra ID simplifies identity management and secure access to protected resources.
[Achievement screenshot](https://drive.google.com/file/d/1Y6p1kWYSXkUV0in0TeRVpn7_r1SMXpHt/view?usp=drive_link)

#### Questions I Still Have

* What are the best practices for managing OAuth token expiration and refresh in production environments?
* How can organizations monitor and audit API plugin access within Microsoft 365 Copilot?
* What additional security controls are recommended when integrating highly sensitive business data with Copilot agents?



#### Resources I Found Useful

* Microsoft Learn Module: Authenticate your API plugin for declarative agents with secured APIs – https://learn.microsoft.com/en-us/training/modules/copilot-declarative-agent-api-plugin-auth/
* Microsoft Learn Documentation: Configure authentication for MCP and API plugins in agents – https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/plugin-authentication
* Microsoft Learn Documentation on Microsoft Entra ID and OAuth Authentication for secure API access.

*Submitted by: \[iperepolu Ebenezery A] · \[iperepoluebenezery2017-ops]*


