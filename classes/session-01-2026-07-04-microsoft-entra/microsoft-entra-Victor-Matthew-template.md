# My Notes — Victor Chizaram Matthew

---

## Key Concepts I Learned

<!-- Write the main ideas covered in today's session -->

- I learnt that securing API integrations for Microsoft 365 Copilot declarative agents relies on two common authentication methods: API keys and OAuth 2.0, and that the module walks through both as parallel patterns for the same underlying goal, protecting an API while still letting a declarative agent call it on the user's behalf.

- API key authentication provides a simple way for an application to access an API by sending a unique key with each request, to protect sensitive credentials.

- I learnt that API keys should never be stored directly in source code; instead, they should be securely managed through services such as Azure Key Vault.

- API keys are convenient to use thanks to their simplicity. To call an API secured with an API key, all you need to do is include the API key in the API request. The API then validates the key and either handles the request or rejects it with an authentication or authorization error. This simplicity comes at a cost though — API keys don't authenticate the user, which means the API can't act on the user's behalf. All users calling the API with the same API key have the same permissions.

- By contrast, OAuth 2.0 is built for authorization rather than just access — it works with access tokens instead of a static shared key. To get a token, an app has to be registered with an identity provider as a public or confidential client, and depending on the type, it may need a secret or certificate configured.

- When a declarative agent integrates with an OAuth-secured API, it needs the client ID, client secret, and the identity provider's authorization/token (and optionally refresh) endpoints. This confidential information also lives in the Microsoft 365 vault, and the plugin just references the vault entry ID rather than holding the secret itself, the agent follows the authorization code grant flow at runtime to get a token and call the API on the current user's behalf.

- One detail that stood out to me: Microsoft recommends enabling PKCE (Proof Key for Code Exchange) even for confidential clients, since it adds a meaningful extra layer of security for very little overhead.

- The vault-reference approach for OAuth also means the client secret can be rotated or updated without redeploying the plugin, which feels like a much more production-friendly pattern than what API keys offer.


---

## Lab / Hands-On Work

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->
- I haven't done any labs yet. 

---

### What I did
- **Created an API Plugin**: Set up the plugin definition that allows Microsoft 365 Copilot to communicate with an external API in VS Code.
- **Configuring Authentication:** Configure the plugin to use either an API key.

---

### What happened / Result
- An API Plugin for Microsoft 365 Copilot was created.

--- 

### Challenges I faced

- I couldn't set up the resources needed to run the hands-on exercises (Integrate an API plugin with an API secured with a key / with OAuth).
- I had issues installing the Microsoft 365 Agents Toolkit extension but I was later able to resolve it by uninstalling and installing a newly downloaded VS Code. 


---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->
- An API key is a secret value that you should never share publicly. When you build an API plugin that integrates with an API secured with an API key, you store the API key in a secure storage location in Microsoft 365, also known as the vault. What I found most valuable, though, was seeing API keys and OAuth side by side — it made the trade-off click for me. API keys are fast to wire up but treat every caller the same, while OAuth is more setup work but actually knows who the user is. That distinction matters a lot for the kind of NOC/IT tooling I work with, where "who did this" is often as important as "did this succeed."

---

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->

- I really would appreciate it if we get to talk about APIs well in class
For a declarative agent using OAuth, does the auth code flow require the user to sign in interactively inside Copilot every session, or does the refresh token keep them signed in like a normal M365 app?

---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->

- Authenticate your API plugin for declarative agents with secured APIs — Microsoft Learn

---

*Submitted by: Victor Chizaram Matthew · victor-matthew-folder*
