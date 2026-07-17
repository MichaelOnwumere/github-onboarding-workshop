# My Notes — Iniobong Johnson

---

## Key Concepts I Learned

- Microsoft Entra security defaults and Conditional Access can be used to strengthen an organisation’s security and enforce authentication requirements such as multifactor authentication. Security defaults provide baseline protection, while Conditional Access provides more granular controls.
- Authentication and authorization perform different functions. Authentication verifies that a user or device is who they claim to be, while authorization determines the resources the authenticated user is permitted to access and the actions they can perform.
- The main authentication categories discussed during the session were single factor authentication, multifactor authentication, and passwordless authentication. Passwordless authentication methods, such as Windows Hello for Business, provide stronger protection than password based authentication.
- Privileged Identity Management helps organisations implement just in time privileged access. It allows users to receive temporary access to privileged roles when they need to perform specific administrative tasks.
- The two PIM assignment types discussed were Eligible and Active assignments. An eligible assignment requires the user to activate the role before using it. Depending on the role settings, activation may require multifactor authentication, justification, or approval. An active assignment allows the user to use the assigned role without completing an activation process.
- When creating a Conditional Access policy, it is important to test the policy before deploying it across the entire organisation. The policy can first be assigned to a test user or group and evaluated using report only mode. This helps prevent unintended account lockouts and access disruptions.

---

## Lab / Hands-On Work

### What I did

I practised the activities demonstrated during the class by creating a Conditional Access policy and configuring Privileged Identity Management.

Conditional Access Policy Configuration
- I signed in to the Microsoft Entra admin centre.
- I navigated to Conditional Access and selected Policies.
- I selected New policy and gave the policy a descriptive name.
- I assigned the policy to a test user.
- Under Access controls, I selected Grant and configured the policy to require multifactor authentication.
- I saved and enabled the policy for the test user.

Privileged Identity Management Configuration
- I expanded ID Governance and selected Privileged Identity Management.
- I selected Microsoft Entra roles.
- I searched for the Group Administrator role.
- I opened the role settings and selected Edit.
- Under the activation settings, I configured the role to require justification and approval before activation.
- I reviewed the assignment duration and notification settings.
- I assigned the test user as eligible for the Group Administrator role.

### What happened / Result

#### Conditional Access Policy Result

- I signed in using the test user account. The user was prompted to register and configure multifactor authentication before being allowed to access the application.
- This confirmed that the Conditional Access policy had been successfully applied to the test user.

#### Privileged Identity Management Result

- I signed in using the eligible user account and requested activation of the Group Administrator role.
- The activation request was sent for approval. From the administrator account, I reviewed and approved the request.
- After approval, the role became active for the user for the configured activation period. The user was then able to perform the administrative tasks permitted by the Group Administrator role.


### Challenges I faced

No major challenges were encountered while completing the lab.

---

## My Takeaways

- My key takeaway was the importance of patience during troubleshooting. When an action does not work as expected, it is important to investigate the issue systematically and identify its root cause.
- Troubleshooting should involve reviewing the configuration, checking whether the correct user or role was selected, allowing time for changes to take effect, and testing the configuration again before making additional changes.
- I also learned the importance of testing security policies with a limited number of users before deploying them across an entire organisation.

---

## Questions I Still Have

None at this time.

---

## Summary of Additional Assignment given on Authenticate you API plugin for Declarative agents with secured APIs

- Integrating a declarative agent with an API allows the agent to connect to an external application, retrieve information, and perform supported actions.
- APIs can be protected using authentication mechanisms such as API keys and OAuth 2.0.
- An API key is a secret value issued and managed by an API provider. The provider determines the level of access associated with the key, including whether it provides access to the complete API or only specific endpoints and resources.
- The API provider determines how the API key must be included in an API request.
- Microsoft 365 Copilot API plugins support passing an API key in three ways:
	- As a bearer token in the Authorization header
	- As a value in a custom header
	- As a query string parameter
- API keys must not be shared publicly or included directly in a public GitHub repository. They should be stored using an approved secure storage solution.
- The practical exercise demonstrated how to integrate an API plugin with an API secured using an API key.
- The exercise also demonstrated how to integrate an API plugin with an API secured using OAuth 2.0.

---

## Conclusion

- The session improved my understanding of authentication, authorization, Conditional Access, and Privileged Identity Management in Microsoft Entra ID.
- The practical exercises also demonstrated how security policies can be tested and how privileged access can be provided temporarily through PIM.
- The additional assignment helped me understand how declarative agents can securely communicate with external APIs using API keys or OAuth 2.0.

---

*Submitted by: Iniobong Johnson · Inib12*
