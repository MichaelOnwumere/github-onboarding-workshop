# My Notes — OLAJIDE SAMSON


## Key Concepts I Learned

<!-- Write the main ideas covered in today's session -->
Here are the main ideas from today's session on the Microsoft Learn module "Authenticate your API plugin for declarative agents with secured APIs":

The scenario:  A car repair shop wants a declarative agent (AI assistant) in Microsoft 365 Copilot to answer questions using their existing repairs API, instead of staff looking things up manually.
Why authentication matters: An API plugin needs a secure way to call a protected backend API, so the module covers two authentication approaches.
API key authentication

Simple secret string; grants access but doesn't identify the individual user.
Can be passed as a Bearer JWT, query parameter, or custom header.
Never hard-coded — stored in Microsoft 365's secure vault and referenced by ID.
Registered via the Teams Developer Portal or Microsoft 365 Agents Toolkit.


OAuth2 authentication

More robust, user-aware, industry-standard protocol.
Requires app registration (client ID/secret, auth/token/refresh endpoints) with an identity provider.
Copilot handles the authorization code grant flow on the user's behalf.
PKCE is recommended for added security, even with confidential clients.
Same vault-storage principle applies — secrets are never exposed to the client.


Common security pattern: Regardless of method, secrets live in the Microsoft 365 vault and are referenced by ID; the declarative agent resolves credentials at runtime rather than embedding them in the plugin.
Hands-on exercises – Practical steps for registering both an API key and OAuth client, then wiring each into an API plugin.
Outcome: Properly authenticated plugins let the declarative agent give accurate, connected, natural-language answers from live API data — saving time and reducing manual errors.
-
-
-

---

## Lab / Hands-On Work

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->

### What I did


### What happened / Result


### Challenges I faced


---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->
Honestly, the most interesting part for me was the design principle running through both authentication methods: secrets never touch the plugin itself,they live in the Microsoft 365 vault and get referenced by an ID, resolved only at runtime by the declarative agent.
That's a clean pattern I don't always see spelled out so clearly in developer docs, and it's a good general lesson beyond just Copilot plugins: build systems so the credential-holding component and the component that "requests access" are separate, and the actual secret material never has to be embedded, checked into source control, or exposed to the client.
The API key vs. OAuth2 contrast was also useful to have laid out side by side, it's a nice concrete illustration of the classic security trade-off: API keys are simple but "anonymous" (every caller looks the same to the backend), while OAuth2 is more work to set up but gets you real per-user identity and authorization. Seeing that framed against a relatable example (the repair shop) made the trade-off feel practical rather than abstract.

---

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->
Till we do it in class
-
-

---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->
Microsoft Learn was very helpful
-

---

*Submitted by: OLAJIDE SAMSON · OLAJIDE SAMSON*
