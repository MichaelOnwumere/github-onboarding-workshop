# My Notes — CHINENYE JOAN OKORO

---

## Key Concepts I Learned

ASSIGNMENT 1
- Identity as the Security Perimeter: In the cloud era, traditional network boundaries are no longer sufficient. 
Identity has become the new primary perimeter, making account security vital to preventing tenant-wide compromise.
- Conditional Access Policies: these policies operate on an "if-then" logic 
For example "If a user is signing in from an untrusted location, then require Multi-Factor 
Authentication". They are essential for enforcing access controls based on real-time risks and user context.
- Priviledged Identity Management: A governance tool used to minimize standing administrative privileges by 
enforcing Just-in-Time (JIT) access, where roles are only activated for a limited time and often require 
additional approval workflows.
- Passwordless Authentication: To combat password-based threats, the session highlights advanced 
authentication methods such as Windows Hello for Business, passkeys, and FIDO2 security keys like YubiKeys 
that link access to trusted devices. 
- Authentication methods and strengths in Entra


ASSIGNMENT 2
- API keys are simple strings used to control access to APIs, and in Microsoft 365 Copilot they are stored securely 
in the vault to prevent exposure.
- API keys and OAuth using client ID and secret are API security mechanisms API plugins for Microsoft 365 Copilot 
support.
- Client ID, Client Server, Token Endpoints are the information developers need to providein the Teams Developer 
Portal to integrate with an API secured with OAuth.
- Declarative agents are AI-Powered assistants in Copilot that can securely connect to external APIs and be optimized
for specific scenerios.
-
--

## Lab / Hands-On Work

### What I did
Step 1: Access the portal using this link https://entra.microsoft.com/
Step 2: Scrolled to Conditional Access on the left panel and clicked on it
Step 3: Configured Named Locations based on IP address and inputted a name, then marked the check box as 
trusted location
Step 4: Navigated to Groups, created a group and named it Finance Dept, then assigned owner.
Step 5: Navigated to Conditional Access, to create new policy
Step 6: Inputted the Name of the policy "conditional_access_policy"
Step 7: Set Conditions 
 Users: selected Users and Groups
 Target Resources: selected all resources
 Network: Configured Yes and selected all trusted networks and locations
 Conditions: selected Device Platforms - cofigured Yes then selected windows and macOS
 Grant: Set to Require multi-factor authentication 
 Session: Selected Sign-in Frequency to 14 hours
Step 8: Enable Policy to Report-only
Step 9: Create




### What happened / Result

<img width="1366" height="768" alt="Picture 24" src="https://github.com/user-attachments/assets/5c286919-16b4-4b9d-8230-ee8ce83e2e27" />
<img width="1366" height="768" alt="Picture 23" src="https://github.com/user-attachments/assets/ac7515f3-fde2-4d56-bcfe-31007c2bef0c" />
<img width="1366" height="768" alt="Picture 22" src="https://github.com/user-attachments/assets/d192e067-7ab3-4311-bcd3-28e40c46e94a" />
<img width="1366" height="768" alt="Picture 21" src="https://github.com/user-attachments/assets/1258f346-1df8-4022-9c30-4d09cfb0725b" />
<img width="1366" height="768" alt="Picture 20" src="https://github.com/user-attachments/assets/033ddb6b-1cc9-4849-bd4e-65ea8ec2cfe9" />
<img width="1366" height="768" alt="Picture 19" src="https://github.com/user-attachments/assets/570f1e96-7b94-4a31-834e-12ef9767b953" />
<img width="1366" height="768" alt="Picture 18" src="https://github.com/user-attachments/assets/4adf5a31-4cd7-4cab-b2e0-02b19c460f12" />
<img width="1366" height="768" alt="Picture 17" src="https://github.com/user-attachments/assets/0c705f41-0c70-45ae-9d26-8cc39c9a1414" />
<img width="1366" height="768" alt="Picture 16" src="https://github.com/user-attachments/assets/07aacd3e-c064-488a-9f93-d7af8c87ca8e" />
<img width="1366" height="768" alt="Picture 15" src="https://github.com/user-attachments/assets/bc68142d-8216-4306-bd96-657b1d8fc4e3" />
<img width="1366" height="768" alt="Picture 14" src="https://github.com/user-attachments/assets/40ecc072-c649-4797-8f55-57ecef292933" />
<img width="1366" height="768" alt="Picture 13" src="https://github.com/user-attachments/assets/4814ff7e-477e-42aa-b5a3-b3f2704b8605" />
<img width="1366" height="768" alt="Picture 12" src="https://github.com/user-attachments/assets/7acc1af4-4243-4c12-9e24-4079d19a06c6" />
<img width="1366" height="768" alt="Picture 11" src="https://github.com/user-attachments/assets/72e80c44-8f43-44a5-bbbb-cd2607d39ace" />
<img width="1366" height="768" alt="Picture 10" src="https://github.com/user-attachments/assets/a20d1eb7-0674-4fcb-8290-f26ef24ee37b" />
<img width="1366" height="768" alt="Picture 9" src="https://github.com/user-attachments/assets/a6219494-f810-48d3-b92d-9cd16b80d17a" />
<img width="1366" height="768" alt="Picture 8" src="https://github.com/user-attachments/assets/a110924e-ae20-4de4-87fc-23551e87d94b" />
<img width="1366" height="768" alt="Picture 7" src="https://github.com/user-attachments/assets/ea4e10d5-e6a5-493d-be71-654bda3223b6" />
<img width="1366" height="768" alt="Picture 6" src="https://github.com/user-attachments/assets/fa4d7665-8ac4-430a-a326-8cfac1eeb5c8" />
<img width="1366" height="768" alt="Picture 5" src="https://github.com/user-attachments/assets/0b44b47d-c068-4c3c-afa4-58d771e9e96a" />
<img width="1366" height="768" alt="Picture 4" src="https://github.com/user-attachments/assets/4ea2a23f-3c68-4ada-8d1f-aafe4e7b234e" />
<img width="1366" height="768" alt="Picture 3" src="https://github.com/user-attachments/assets/112e8852-1a19-4b5a-a5a8-b82a991fbc31" />
<img width="1366" height="768" alt="Picture 2" src="https://github.com/user-attachments/assets/b62a6cb8-55d8-47f6-8567-a754695039cf" />
<img width="783" height="446" alt="Picture 1 Lab 1 Question" src="https://github.com/user-attachments/assets/197e175e-fb2a-4695-85f7-19f4043c1a92" />






- 

### Challenges I faced


---

## My Takeaways

ASSIGNMENT 1
- Adopt Zero Trust Principles: Always verify explicitly. Never assume an identity is safe based 
on location or network; assume breach and verify every access request.
- Implement Just-in-Time Access: Avoid permanent administrative role assignments. Use PIM to grant 
users the least privilege necessary only when they specifically need it, reducing the attack surface.
- Leverage Report-only for Troubleshooting: When configuring Conditional Access, use the "Report-only" 
mode to observe policy impact in your environment without blocking users, then review 
Sign-in logs to diagnose why a policy did or did not apply before enabling "Yes".
- Break glass Accounts: are emergency accounts and they should be excluded during Conditional Access Policy
creation so these accouts will not be logged out.

ASSIGNMENT 2
- Declarative agents in Microsoft 365 Copilot improve efficiency by enabling natural language queries over secured APIs.
- OAuth provides stronger user specific authentication compared to API keys
- Storing credentials in the vault ensures security and easy updates without redeployment.
---

## Questions I Still Have

- More knowledge about Break Glass Accounts so I don't log out key identity accounts. What are the types of Break glass accounts?
Can any account be tagged as Break Glass Account? Just in case a mishap occurs and break Glass accounts were not exclude 
is there any solution?

-
---

## Resources I Found Useful

ASSIGNMENT 1

- https://learn.microsoft.com/en-us/training/paths/secure-access-resources-entra/

- https://entra.microsoft.com/

- https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/sc-500

ASSIGNMENT 2

- https://learn.microsoft.com/en-us/training/modules/copilot-declarative-agent-api-plugin-auth/1-introduction



---

*Submitted by: Chinenye Joan Okoro · AriZiv237*
