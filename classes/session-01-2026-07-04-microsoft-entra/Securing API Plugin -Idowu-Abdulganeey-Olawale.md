# My Notes — IDOWU ABDULGANEEY OLAWALE


##🔐 Securing API Plugins for Microsoft 365 Copilot Declarative Agents

I recently completed the Microsoft Learn module on Authenticating API Plugins for Declarative Agents, and it reinforced an important principle:

An AI agent is only as secure as the APIs it can access.

## What I Learned

When building declarative agents for Microsoft 365 Copilot, APIs often expose sensitive business data or perform critical operations. Microsoft supports two primary authentication models for securing these API plugins:

### 1. API Key Authentication

- Best suited for simple or service-to-service integrations.
- API keys are never hardcoded in the plugin or source code.
- Instead, they're securely stored in Microsoft's plugin vault and referenced from the plugin manifest.
- At runtime, Copilot retrieves the key securely before calling the API.

### 2. OAuth 2.0 Authentication

- Recommended for enterprise applications and user-specific data.
- Enables users to authenticate with their identity provider (such as Microsoft Entra ID).
- Copilot handles the authorization flow, consent, token acquisition, and token refresh automatically.
- APIs receive valid bearer tokens, allowing them to enforce user permissions and access control.

## Key Takeaways

✅ Choose the authentication method based on your API's security requirements—not convenience.

✅ Use API Keys for simpler integrations where user identity isn't required.

✅ Use OAuth 2.0 whenever your API accesses protected resources or needs to act on behalf of a user.

✅ Keep secrets out of your codebase by leveraging Microsoft's secure vault and plugin configuration.

✅ Authentication isn't just about granting access—it's about ensuring your Copilot agent respects enterprise security, identity, and least-privilege principles.

## Why This Matters

As AI agents become capable of retrieving live data and triggering business actions, authentication becomes a core part of agent design—not an afterthought.

Building secure agents means designing for:

- Identity
- Authorization
- Secure secret management
- Least-privilege access
- User trust

Security isn't an add-on for AI-powered applications—it's part of the architecture from day one.


---

*Submitted by: Idowu Abdulganeey Olawale· Cyberwalls*
