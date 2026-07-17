# My Notes — BRIDGET EVAVOAWE


---

## Key Concepts I Learned

<!-- Write the main ideas covered in today's session -->

- How Microsoft Entra ID secures access to cloud resources through identity and access management.
- The difference between authentication (verifying identity) and authorization (determining what a user can access).
- How Conditional Access evaluates sign-in conditions before granting or blocking access.
- How Named Locations can be used to restrict access to trusted locations.
- Why Break Glass accounts are excluded from Conditional Access policies.
- How Sign-in Risk conditions can trigger additional security controls such as MFA or blocking access.
- How Self-Service Password Reset (SSPR) enables users to securely reset their passwords.
- How Privileged Identity Management (PIM) provides just-in-time privileged access instead of permanent administrative roles.
---

## Instructor Demo — Conditional Access Policy & PIM Configuration 

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->

Since this session was led by the mentor as a live demonstration, I documented what I observed   

### What the Mentor did
**Conditional Access Policy:**
- Navigated to [entra.microsoft.com](https://entra.microsoft.com) to access the Microsoft Entra admin center 
- Created a Conditional Access policy targeting cloud resources 
- Configured a named location, so that only users signing in from within that location can gain access to the resources 
- Excluded breakglass accounts from the policy to ensure emergency access is never fully locked out 
- Configured sign-in risk conditions by defining what should and should not happen when a risky sign-in is detected

**Privileged Identity Management (PIM):**

- Demonstrated how PIM is used to assign privileged roles to users 
- Showed how access is granted on a just-in-time basis, meaning users only receive elevated permissions when they need them, for a limited period rather than having standing privilege at all times

### What happened / Result
One of the most valuable lessons from the session came during the policy testing phase. The Conditional Access policy did not behave as expected initially because of a configuration issue. After troubleshooting, the mentor identified the cause and corrected it.

This demonstrated that configuring Conditional Access requires careful planning and testing. A small configuration mistake can unintentionally prevent legitimate users from accessing resources or cause policies not to work as intended.

### Challenges I faced

Since this was a demonstration, I was unable to practice the configuration myself.

I am looking forward to receiving access to the Entra environment so I can recreate these configurations and strengthen my understanding through hands-on practice.
---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->

 This week's session was really impactful. One of my biggest takeaways is that it's not enough to know how to configure security policies—I also need to understand the concepts behind them. That understanding will help me troubleshoot issues effectively, just as my mentor did during the policy demonstration. It also reinforced the importance of carefully testing Conditional Access policies, since even a small misconfiguration can affect how they work. Going forward, I plan to practice as much as I can in the Microsoft Entra environment and continue using Microsoft Learn and other resources to strengthen my skills in identity and access management.
---

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->

- No questions for now


---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->

- [Microsoft Learn — Conditional Access overview](https://learn.microsoft.com/en-us/entra/identity/conditional-access/overview)

---

*Submitted by: Bridget Evavoawe · BridgetEvavoawe*
