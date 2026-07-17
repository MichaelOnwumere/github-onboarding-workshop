# SC-500 Learning Notes — Dare Ademola

## Session: Microsoft Entra ID & API Authentication for Declarative Agents

### Key Concepts I Learned

**Microsoft Entra ID — Conditional Access, MFA & Session Management**
- Conditional Access Policy (CAP) works on "if / then" logic. For example: *if* a user is in GRC *and* is on a macOS device, *then* access requires VPN and is restricted to a specific location.
- MFA can be enforced through Conditional Access Policy, Security Defaults, or MFA registration.
- Session Management lets you set sign-in frequency — i.e. the number of days before a user must re-authenticate.
- Privileged Identity Management (PIM) helps solve the problem of orphaned / standing elevated access for administrators.

**API Authentication for Declarative Agents (Copilot)**
- Creating API keys and storing them securely in a vault, then referencing the vault key as an extension to grant trusted third parties access to the API.
- Configuring OAuth for API access and securing those credentials in the vault.
- <img width="1196" height="766" alt="Activate MS 365 agent " src="https://github.com/user-attachments/assets/9d92ca8c-cc93-4172-a98b-ffdb4f11660d" />


---

### Lab / Hands-On Work

**What I did**
- Entra ID lab: worked through Conditional Access Policy configuration and troubleshooting.
- Installed VS Code and initialised the Microsoft 365 Agents Toolkit.
- Used Microsoft Learn and followed the prompts on the Microsoft Marketplace / Copilot agent page.

**What happened / Result**
- Completed the Entra ID configuration and troubleshooting exercises.
- Could not complete the declarative agent lab due to lack of access to a Microsoft Copilot license.

---

### Challenges I Faced
- Unable to run the Copilot declarative agent lab without a Microsoft Copilot license.

---

### My Takeaways
- Conditional Access should be applied carefully and on a need-only basis.
- Multiple MFA methods are best practice; binding MFA to only the phone Authenticator app is poor practice.
- Troubleshooting requires care and patience — a failing configuration is often just a slight policy misspecification.
- Assign Conditional Access Policies to a security group rather than to individual users.
- PIM is the right tool for eliminating orphaned / standing elevated admin access.

---

### Questions I Still Have
- How do I define automatic key rotation, and when should it run?
- How can I make auditing of API authentication easy to review?
- Can I build notification prompts for when an administrator changes an OAuth key?
- Can I build a data-flow view of what each API's authentication has access to?

---

### Resources I Found Useful
- Microsoft Learn modules on Microsoft Entra ID
- Microsoft Marketplace / Copilot agent page

---

_Submitted by: Dare Ademola (Oluwatidamilare)_
