# My Notes — Berna Namulyowa

## Key Concepts I Learned

<!-- Write the main ideas covered in today's session -->
Secure Access to Resources by Using Microsoft Entra
I learned that this is a practical defense-in-depth approach used to authenticate, allow privileged access, and support identity-aware AI applications.
Passwordless is the strongest authentication method, and this includes Windows Hello for Business, Passkeys, FIDO2 security keys, and Microsoft Authenticator.
You can also add conditional access policies to either a group or a user.
Using Just-in-Time privileged access eliminates standing permissions.


Authenticate Your API Plugin for Declarative Agents with Secured APIs
Declarative agents for Microsoft 365 Copilot can be used to create AI-powered assistants that you can customize by giving them instructions to do anything you want them to do.


INTEGRATE AN API PLUGIN WITH AN API SECURED WITH AN API KEY
The API keys are arbitrary strings that the owners use to either grant full access or partial access to the resource and also for how long you can access it.
To use the key you must include it in the API secured request.
The API validates the key and handles the request or rejects it with an authentication or authorization error.
The pitfall is that the API key doesn't authenticate the user (All users calling the API with the same key have the same permissions).
The API provider gives the details on how to make the requests.
An API key is stored in the secret vault. The API key is a secret value that should never be shared publicly.

INTEGRATE AN API PLUGIN WITH AN API SECURED OAUTH
OAuth is an industry-standard protocol used to secure APIs using access tokens. To get the token, the application is registered with the identity provider and the type is specified either public or confidential client.
API plugin with an API secured OAuth the person needs a client ID, Client Secret of the application that secures the API and the identity provider's authorization-token and sometimes refresh endpoints.
You also need to enable Proof Key for Code Exchange (PKCE).

---

## Lab / Hands-On Work

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->
Lab 1: Deploy MFA with Conditional Access
Steps:
Use the Microsoft Entra Portal.
Configure a Named Location using either trusted IP boundaries or a country. In my case, I used IP boundaries.
![Uploading Screenshot 2026-07-10 110912.png…]()

Add a policy to Conditional Access.
<img width="2880" height="1800" alt="Screenshot 2026-07-10 111308" src="https://github.com/user-attachments/assets/7f8cedd8-a9e3-4ad2-aab4-8b8465d0d8f9" />

Under the added policy, attach it to a specific user.
<img width="2880" height="1800" alt="Screenshot 2026-07-10 124740" src="https://github.com/user-attachments/assets/da214f1a-ae09-4c3d-9272-89692c9927d4" />

Set the policy to report-only and review the sign-in logs.
<img width="2880" height="1800" alt="Screenshot 2026-07-10 124927" src="https://github.com/user-attachments/assets/23282a6d-c087-4d6f-b2bb-51c6aeb374ad" />


Lab 2: Onboard a Role into PIM
Steps:
Under Entra ID, select PIM, then Roles.
Select User Administrator and set the activation max duration to your preference.
Add assignments for the target administrators — don't forget to remove their active permanent assignments.
Configure the activation approval.
Activate the role for a user and confirm the MFA, approval flow, and audit-log entries.
Schedule a quarterly access review on the role.
  
### What I did
I completed Lab 1:
Used the Microsoft Entra Portal.
Configured a Named Location using trusted IP boundaries (192.168.137.1/24).
Added a policy to Conditional Access.
Attached the policy to a specific user.
Set the policy to report-only and reviewed the sign-in logs.

### What happened / Result
I used another browser, and when the user was prompted to sign in, an authenticator request popped up, requiring them to install the Authenticator app.

### Challenges I faced
Lab 2 is still challenging me but i will do it.

---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->
The practical part, mostly Lab 1, was a success on the first attempt.

I also valued the knowledge gained on securing API plugins using declarative agents.
---

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->

-
-

---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->
https://learn.microsoft.com/en-us/training/modules/copilot-declarative-agent-api-plugin-auth/7-summary
https://learn.microsoft.com/en-us/training/paths/secure-access-resources-entra/
https://learn.microsoft.com/en-us/training/modules/implement-configure-privileged-identity-management/
https://learn.microsoft.com/en-us/entra/id-governance/privileged-identity-management/pim-deployment-plan
-

---

*Submitted by: Berna Namulyowa · nbernah*
