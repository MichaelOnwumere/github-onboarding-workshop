# My Notes — Promise Ibediogwu Ekele

## Key Concepts I Learned

- **Azure Key Vault (AKV)** is used to securely store and manage secrets, keys, and certificates for cloud applications and services.
- **Identity is the foundation of Azure security**, and proper Identity and Access Management (IAM) practices are the first line of defense.
- **Azure RBAC** is the recommended method for managing Key Vault permissions, replacing legacy access policies with a more centralized and scalable authorization model.
- **Managed Identities** allow Azure services such as App Service to securely authenticate to Azure Key Vault without storing credentials in application code.
- **Diagnostic Logs** and **Log Analytics** help monitor, audit, and investigate access to Azure Key Vault resources.

---

## Lab / Hands-On Work

### What I did

- Created an **Azure Key Vault** in the Azure portal.
- Deployed an **Azure App Service (Web App)**.
- Enabled a **System-Assigned Managed Identity** on the App Service.
- Configured **Azure RBAC** for the Key Vault.
- Attempted to create and manage secrets in the Key Vault.
- Used the **Kudu (App Service Debug Console)** to follow the mentor's demonstration and inspect the managed identity endpoint through PowerShell.
- Explored diagnostic logging options for monitoring Key Vault activities.

### What happened / Result

- The App Service was successfully assigned a managed identity.
- I was able to access the Kudu console and observe how applications authenticate securely to Azure services without embedding credentials.
- I observed how Azure RBAC controls access to Azure Key Vault resources.
- The lab reinforced how Managed Identities eliminate the need to store secrets within application code.

### Challenges I faced

- I encountered an authorization error when attempting to create a secret in Azure Key Vault.
- The issue was caused by insufficient Azure RBAC permissions.
- I also learned that RBAC role assignments require a few minutes to propagate before taking effect.
- Understanding the distinction between Azure RBAC and legacy Access Policies required additional troubleshooting.

---

## My Takeaways

This session helped me understand that **Azure Key Vault is much more than a secret store—it is a critical security service that depends on strong identity and access management.**

The hands-on lab reinforced the importance of:

- Using Azure RBAC for fine-grained authorization.
- Implementing Managed Identities for passwordless authentication.
- Applying the Principle of Least Privilege.
- Monitoring access through Diagnostic Logs and Log Analytics.

One of my biggest lessons was that **cloud security is not only about protecting secrets but also about protecting identities and continuously validating access.**

---

## Questions I Still Have

- What are the best practices for implementing Azure RBAC for Azure Key Vault in large enterprise environments?
- How can organizations automate secret rotation and access reviews for Azure Key Vault?

---

## Resources I Found Useful

- **Microsoft Learn – Azure Key Vault Documentation**  
  https://learn.microsoft.com/azure/key-vault/general/

- **Microsoft Learn – Azure RBAC Guide for Azure Key Vault**  
  https://learn.microsoft.com/azure/key-vault/general/rbac-guide

- **Microsoft Learn – Managed Identities for Azure Resources**  
  https://learn.microsoft.com/entra/identity/managed-identities-azure-resources/

- **Microsoft Learn – Monitor Azure Key Vault**  
  https://learn.microsoft.com/azure/key-vault/general/logging

- **Microsoft Learn – SC-500 Learning Path**  
  https://learn.microsoft.com/training/paths/sc-500-secure-azure-resources/

- **Microsoft Learn – Secure Azure Resources with Azure Key Vault Module**  
  https://learn.microsoft.com/training/modules/configure-and-manage-azure-key-vault/

- **Microsoft Cloud & AI Security Bootcamp 2026 (Session Recording)**  
  https://www.youtube.com/watch?v=GKqpej4X9B0&t=5936s
---

*Submitted by: **Promise Ibediogwu Ekele** · **GitHub:** `github.com/promibe`*