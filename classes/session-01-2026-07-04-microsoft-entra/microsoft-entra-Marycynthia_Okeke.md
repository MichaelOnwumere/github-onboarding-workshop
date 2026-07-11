<img width="732" height="138" alt="image" src="https://github.com/user-attachments/assets/022b83d8-f47e-424a-90d9-36e731c2df6d" /><img width="732" height="138" alt="image" src="https://github.com/user-attachments/assets/27517684-3c9a-4271-af1e-6921f218e5e6" />
## Key Concepts I Learned

* I learnt about Declarative Agents for Microsoft 365. It lets you create AI-powered assistants that are optimized for specific scenarios

* I also learnt about APIs and API Keys. API Keys are arbitrary strings that owners use to grant anyone access to the API. It is best secured in a storage location in MS365 called 'Vault', which allows you to securely manage your API keys without public exposure.

* I also learnt how to call the API by including the API keys in the API requests

* I learnt that MS 365 Copilot supports passing API keys as Json Web Token, Query String Parameter, and Custom Header

* I also learnt about another method of securing APIs called OAuth. It is the industry standard protocol for authorization. It secures access to resources using access Tokens

* I also learned about PKCE (Proof Key for Code Exchange); it is available as an option when configuring OAuth for your plugin. It adds an extra security layer to your app with minimal overhead.
\---

## Lab / Hands-On Work

Project Creation and Environment Setup
Initialized the Project: Opened Visual Studio Code and used the Microsoft 365 Agents Toolkit extension to create a new application.
Configured Agent Specifications <img width="960" height="393" alt="D A" src="https://github.com/user-attachments/assets/b5f28921-f5f3-424d-b8f2-f78ee3c593f3" />
I Selected Copilot Agent as the project template.Chose Declarative Agent as the core app feature. I added a plugin capability by selecting Add an Action $\rightarrow$ Start with a new API. I set the authentication type to API Key (Bearer Token Auth). Selected TypeScript as the development programming language. Saved and named the project repository da-repairs-key.
Inspected API Security Definition <img width="722" height="125" alt="D A API" src="https://github.com/user-attachments/assets/549c0d40-6654-47e5-a135-3f0c7887b2ad" />
Analyzed API Runtime Validation <img width="673" height="111" alt="D AAPI2" src="https://github.com/user-attachments/assets/be9cb1bb-5348-4b5d-a2c0-628afc984a1d" />
<img width="673" height="111" alt="image" src="https://github.com/user-attachments/assets/a6ef6206-fbb7-4332-b349-5f61d164eb5b" />
Reviewed Teams Vault Provisioning <img width="732" height="138" alt="image" src="https://github.com/user-attachments/assets/cffe0ce2-c53d-46da-a962-83d0d1da5a69" />
I'm stuck at npm install, will finish up and update this file

### What I did

* Initialized the Copilot Project: Used the Microsoft 365 Agents Toolkit extension in VS Code to create a new "Copilot Agent" using the "Declarative Agent" app feature.
* Added API Functionality: Configured the agent's action by setting up a new API that utilizes **API Key (Bearer Token Auth)** and chose TypeScript as the development language.
* Codebase Inspection: Opened and examined the `appPackage/apiSpecificationFile/repair.yml` file to verify the bearer token security scheme, reviewed the local verification logic in `src/functions/repairs.ts`, and checked the automated vault registration setup in `teamsapp.local.yml`.
* System Readiness Check: Opened the VS Code integrated terminal and verified that `npm` was correctly installed and active on the local machine by checking its version.

### What happened / Result
* Project Structure Successfully Created: The toolkit generated the complete workspace scaffolding named `da-repairs-key`, containing all the necessary configurations for a secure declarative agent.
* Environment Validated: Running `npm -v` successfully returned version `10.9.2`, confirming that the Node Package Manager environment is fully operational and ready to install dependencies.
* Next Steps Paused: The setup is currently poised at the package installation phase (`npm install`), right before generating the cryptographic secret key via `npm run keygen` and mapping it to the local user environment files


### Challenges I faced
* UI Label Discrepancies: The tutorial instructions referenced an "Add plugin" option, which was missing from the updated Microsoft 365 Agents Toolkit extension interface. I had to figure out that Microsoft updated this terminology to Add an Action $\rightarrow$, Start with a new API.
* Typos in Documentation: The guide referred to a configuration file named `./teampsapp.local.yml`, but after navigating the project root directory, I identified that the actual file name was correctly spelled `ms365agents.local.yml`.
* Verifying Environment Prerequisites: Before pulling down dependencies, I had to pause and explicitly verify that my local runtime environment had the correct `npm` versions active to ensure the project packages would install cleanly without configuration conflicts. Npm install is stuck and can't run in my system. Trying to fix it


## My Takeaways
* Adapting to Evolving Cloud Tools: I learned that cloud and agent developer tools move fast, meaning documentation labels won't always match the active UI perfectly. Being able to map terms like "plugins" to "actions" is a critical skill when working with newer tech stacks.
* Understanding Token Security Architecture: Reviewing how Copilot abstracts authentication was highly valuable. Seeing exactly how a Bearer token scheme in an OpenAPI spec maps directly to a local TypeScript verification function (`isApiKeyValid`) made the theoretical flow of API key security concrete.
* The Importance of Secure Vaults: It was interesting to see how local development credentials aren't hardcoded into the plugin configuration files itself, but are instead registered dynamically into a secure Teams vault using automated provisioning steps. This keeps the actual API secret completely hidden from the client side at runtime.

\---

## Questions I Still Have
None

\---

## Resources I Found Useful

[<!-- Any links, docs, or Microsoft Learn modules you found helpful -->](https://learn.microsoft.com/en-us/training/modules/copilot-declarative-agent-api-plugin-auth/2-integrate-api-plugin-key)


*Submitted by: Marycynthia Okeke · Nechy-Okeke*

