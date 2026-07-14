# My Notes — Omoboye Osinowo
## Key Concepts I Learned
 # Secure Access to Resources using Microsoft Entra
 - 	What is Authentication?
	Authentication is verifying the identity of a user using username and password credentials to sign in to an environment.
- 	Authentication methods: Authentication can be done through various layers which include single factor, multifactor and password less methods. The authentication method determines the authentication strength.

  	Single factor authentication: this requires the use of one category of credential to verify an identity, examples are username and password, answer to security question, email. This method is considered less secure.

  	Multifactor authentication: this is the use of more than one layer of authentication method for identity verification. Examples Authentication App, Oath hardware token, SMS/Voice call, temporary Access Pass.

  	 Passwordless Authentication: This is the use of non-password for authentication. Examples: Windows Hello for Business, Passkey (device-bound), FIDO2 Security Key, MS Authenticator (Phone sign-in).
  - What is Microsoft Entra ID? A cloud-based identity and access management service managed by Microsoft. It serves as a central engine used for managing access and control to organization’s resources. It is used to control who access what and under what conditions can access be granted through authentication and authorization processes. Microsoft Entra ID supports the use of multi-layered authentication methods for secured level authentication. This involves the involves the use of multifactor authentication (MFA).
- Privileged Identity Management: It is used to control, manage and monitor elevated access to important resources in an organization. It utilizes the concept of zero trust such that privileged users are assigned roles to do administrative tasks temporarily instead of permanent access.
  - Just-in-time Access: Users are given access to admin roles for a limited time which expires automatically. Eligible assignments are activated on demand and time-bound activation with MFA.
  -  Approval Workflow: Before someone gets elevated access, a manager or admin must review/justify and approve the request
  -  Access Reviews and Audits: Regular review of access to ensure that users still require the privileged permissions. This ensures that only the user that requires an elevated right possesses such privileged access have it all times. i.e. privileged access is only given to those who need it.
  - Alerts: Notifications are sent when privileged roles are activated.
  - PIM reduces standing privileges by design.
  - PIM can be enabled at three levels- Directory role, Azure resources and Role-assignable groups.
-  Conditional Access Policy
    - A security feature verifies and allows users to have access to a resource. It uses if-then engine to grant access. i.e. if a condition is met, access is granted, Signal -> Decision -> Enforcement.
    -  Signal: triggers the policy and can be from users/groups (who is requesting access), application (which resource is being accessed), device state (is the device compliant, secure or managed by the company), location name (where is the request originating from) and risk (sign-in or user; are there signs that the account has been compromised).
    -  Decision: based on the policy set, the system takes any of the following actions- Block access (denies access completely), Grant access (user is able to login), user is forced to take additional action such as require MFA, require complaint device (ensure device is meets security requirement), require authentication strength.
    -  Enforcement: session control, continuous access evaluation, sign-in frequency.
- Self-Service Password Reset (SSPR)
  - A service deployed to enable users to reset password when an account is locked out without contacting an IT administrator. This improves productivity.  The service involves registration, authentication method, hybrid write back, notification and auditing.

- Secure APIs plugins
  - They are mechanisms use to add layer of security to application programming interface (API) to prevent malicious attacks or unathorized access.
  - API plugins need to be secured and can be autheticated using two supported methods:
    - API key
    - OAuth (using client ID and Secret).
  - API keys are arbitrary strings that API owners use in granting secure access to APIs. The API keys are secret values that should not be shared in public.
  - API keys are to be stored in secured storage known as vaults.
  - Vault entry ID- the information is required by developers need to include in the API plugin's manifest to integrate with an API secured with an API key




<!-- Write the main ideas covered in today's session -->





---

## Lab / Hands-On Work

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->

### What I did


### What happened / Result


### Challenges I faced
- None
---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->
- Identity is the new secuirity perimeter.
- Secure authetication requires multiple layers of athetication methods and is scenerio based.
- Security default is the baseline for security in Microsoft Entra ID and must be disabled before a conditional access policy can be enforced.

---

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->

- None
-

---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->

-Bootcamp live session and recording
- Microsoft Learn

---

*Submitted by: Omoboye Osinowo · BoyeAdeleke
