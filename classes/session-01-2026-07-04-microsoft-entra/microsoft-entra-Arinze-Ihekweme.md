# My Notes — Arinze Fortune Ihekweme

---

## Key Concepts I Learned

<!-- Write the main ideas covered in today's session -->

- Microsoft Entra ID is Microsoft’s cloud-based identity solution, it determines which users are able to log into an application and how much authority they will be granted upon successful login.
Conditional Access provides ability to create conditional policies that determine if the user has logged in from a specific geo-location or whether their mobile device meets the minimum requirements based on multiple factors including risk prior to granting access.
Multi-factor authentication adds an additional layer of verification by requiring both knowledge and possession to complete the identity validation process ensuring that even with the knowledge of a username/password combination a malicious actor would still require possession of the users device/phone etc. to gain unauthorized access to resources.
Privileged Identity Management creates an environment where administrators are not provided permanent privileged access but instead receive temporary escalated permissions on demand while performing a privileged function; thereby limiting the window of opportunity for an administrator to perform nefarious activities while authorized under the elevated privileges.
All of these solutions are direct correlations to the SC-500 course material as protecting identities and credentials represents a major area of focus for the certification exam.

---

## Lab / Hands-On Work

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->

### What I did
- Signed in as myself into the free tier of Azure for my own tenant and went to the Microsoft Entra ID application.
- I created a new Conditional Access policy that is targeted towards a group/test user and was configured to include a conditional based upon both Sign-In Risk (High) and Location. 
- The Grant Control setting of this policy was changed to "Require MFA" so that if either of those conditions were met, multi-factor authentication would need to take place before access could be granted to the protected resource(s).
- Went back into PIM and reviewed how an Admin Role within PIM may be made Eligible, but only activated when needed rather than always being assigned.
- Afterward I checked the sign-in logs to determine where the Conditional Access policy showed up during a test sign-in attempt.

### What happened / Result
- The Conditional Access policy applied as expected — a sign-in that matched the condition was prompted for MFA.
- In PIM, I could see the difference between an "eligible" and an "active" role assignment, and how activation is time-bound.

### Challenges I faced
- Getting used to the difference between Conditional Access (controls sign-in) and PIM (controls standing admin access) — they overlap in purpose but work differently.
- Needed a moment to figure out where role activation requests actually appear in PIM.

---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->

Seeing Conditional Access and PIM as two layers of the same problem — stopping bad sign-ins vs. limiting the damage if an admin account is compromised — made both concepts click. It also ties in well with the Entra ID forensics work I've done before, since these are exactly the kinds of controls I'd be checking for in an investigation.

---

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->

- How do Conditional Access and PIM policies interact when a user has both applied to them at once?
- In a real (non-free-tier) tenant, what's a sensible starting set of Conditional Access policies for a small org?

---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->

- Microsoft Learn: Microsoft Entra Conditional Access documentation
- Microsoft Learn: Privileged Identity Management (PIM) overview

---

*Submitted by: Arinze Fortune Ihekweme · Arizonal8*
