
## Key Concepts I Learned


During this week's class, I was introduced to a practical hands-on lab centered on Microsoft Entra ID (previously Azure AD), which also enhanced my understanding of how identity fundamentally supports modern security.

The following topics were demonstrated as part of the learning experience:
1. Investigating conditional access policies that exclusively trust a specified location and deny access to all other users not authorized in that location.
2. Examining some basic features of Privileged Identity Management (PIM).

I also learned how to secure API plugins utilized by Microsoft 365 Copilot declarative agents. Authentication allows agents to safely access external APIs while safeguarding user data and ensuring that only authorized requests are handled.  
The main points I learned include:  
1. Recognizing the significance of authentication when integrating API plugins with Microsoft 365 Copilot declarative agents.  
2. Setting up authentication using supported methods such as OAuth 2.0, API Keys, or Anonymous Access, based on the API's requirements.  
3. Utilizing Microsoft Entra ID (formerly Azure Active Directory) to enable secure user sign-in and token-based authentication for enterprise APIs.  
---

## Lab / Hands-On Work

I set up Privileged Identity Management to enable role activation based on time and approvals, reducing the risk of excessive, unnecessary, or improper access to important administrative resources.

### What I did

In the laboratory, I set up the Helpdesk role as a privileged position for Felix, a contractor employed for 15 days to carry out helpdesk tasks for up to four (4) hours daily.


### What happened / Result
I managed to set up the PIM successfully by using the instructions provided in the class lecture.

### Challenges I faced
none

---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->

I learned that the administrator's account, often referred to as the breakglass account, should be excluded from any policies applied to the tenant to prevent lockouts of the tenant.
---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->

-

---

*Submitted by: FOLARANMI ABOLADE FELIX · Abolade-Folaranmi*
