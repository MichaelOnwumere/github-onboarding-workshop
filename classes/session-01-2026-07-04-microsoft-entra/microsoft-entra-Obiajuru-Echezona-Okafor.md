# My Notes — Obiajuru Echezona Okafor



---

## Key Concepts I Learned

Microsoft Entra ID supports a range of authentication methods and authentication strength concepts, and these can be layered with Conditional Access policies and named locations to enforce MFA appropriately across different scenarios.
Passwordless authentication is a key direction in modern identity ,Windows Hello for Business, passkeys, and FIDO2 security keys all reduce reliance on passwords while improving security, and self-service password reset (SSPR) can still be configured for hybrid environments where passwords remain in use.
When building API plugins for declarative agents in Microsoft 365 Copilot, APIs are typically secured using one of two common methods such as API key or OAuth2  and the plugin needs to be configured to authenticate correctly against whichever method the API uses.

-
-
-

---

## Lab / Hands-On Work

I haven't done the lab yet, plan on doing it the upper week

### What I did
![Authenticate API Plugin badge](<WhatsApp Image 2026-07-10 at 14.32.42 (1)-1.jpeg>)
![Microsoft Entra ID Badge](<WhatsApp Image 2026-07-10 at 14.32.42-1.jpeg>)
### What happened / Result
I completed both modules successfully and earned the achievement badges for each. The exercises gave me a working understanding of how authentication is configured on both the identity platform side (Entra ID) and the application/plugin side (Copilot declarative agents).

### Challenges I faced
Entra ID module was fairly intuitive since it built on identity concepts I already knew. The Copilot API plugin module was a newer topic to me,reasoning through when to use API key versus OAuth2 for a given API, and what that choice means for the plugin manifest, took a bit more careful reading before it clicked.

---

## My Takeaways

The most valuable part was seeing authentication from two different angles in the same session,securing user sign-in at the identity layer with Entra ID, and securing API access at the application layer for a Copilot plugin. It reinforced that authentication isn't a single concept but a set of related patterns (identity-based, key-based, token-based) that show up differently depending on where in the stack you're working. That's directly relevant to the kind of access control and identity security thinking I want to build on for SOC and cloud security roles.


---

## Questions I Still Have

In a real enterprise setup, how do teams decide when an API plugin should use API key auth versus OAuth2, beyond what the API itself supports?

Are there common misconfigurations in Conditional Access-based MFA policies that we should specifically watch for from a security-analyst perspective?

-
-

---

## Resources I Found Useful

https://learn.microsoft.com/en-us/training/modules/manage-implement-authentication-methods/

https://learn.microsoft.com/en-us/training/modules/copilot-declarative-agent-api-plugin-auth/

---

*Submitted by: Obiajuru Echezona Okafor · ecokafor*
