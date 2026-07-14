\---

## Key Concepts I Learned

<!-- Write the main ideas covered in today's session -->

* I learnt about securing API integrations for Microsoft 365 Copilot declarative agents using two common authentication methods: API keys and OAuth 2.0.
* API key authentication provides a simple way for an application to access an API by sending a unique key with each request, to protect sensitive credentials.
* I learnt that API keys should never be stored directly in source code, instead, they should be securely managed through services such as Azure Key Vault.
* API keys are convenient to use due to their simplicity. To call an API secured with an API key, all that is required is to include the API key in the API request. The API then validates the key and either handles the request or rejects it with an authentication or authorization error.

&#x20;  This simplicity comes however at a cost. API keys don't authenticate the user which means that the API cannot

&#x20;  act on the user's behalf. All users calling the API with the same API key, have the same permissions.

\---

## Lab / Hands-On Work

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->



I started the lab for the first exercise (Integrate an API plugin with an API secured with a key)using VS Code on my laptop. But could not proceed due to permissions required. I need to get my test environment ready (at least a trial tenant where I can fully practice the exercise and conduct the labs.

### What I did



### What happened / Result



### Challenges I faced

The challenge I had was that I could not continue with exercise due to permission and right environment (tenancy)

\---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->



An API key is a value that you should never share publicly. When you build an API plugin that integrates with an API secured with an API key, one should store the API key in a secure storage location in vault in Microsoft 365.

The reason is that API keys function like master passwords to cloud resources and leaking them can result in data breaches.



In short, API keys are like a shared master password — simple but limited.



While , OAuth 2.0 is like giving each user their own ID badge with specific access rights — more secure and flexible.

\-

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->



* Discussing this exercises and API in general as a group or together in class will be highly appreciated



\---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->



* https://learn.microsoft.com/en-us/training/modules/copilot-declarative-agent-api-plugin-auth/

\---

*Submitted by: Adeniyi Familua · deyniyy*

