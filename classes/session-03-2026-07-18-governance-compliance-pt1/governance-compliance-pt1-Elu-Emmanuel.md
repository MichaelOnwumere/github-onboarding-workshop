# My Notes — Elu Uchenna Emmanuel

---

## Key Concepts I Learned

<!-- Write the main ideas covered in today's session -->

- Enforcing security governance and regulatory compliance 
- How to enforce governance using Azure policy, resource lock and defender for clouds
- Evaluation of regulatory compliance, protect backup data

---

## Lab / Hands-On Work

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->

### What I did

- Enforce governance with Azure policy and resource locks
- Created a storage resource to test the policy enforced
- Assign policy to deny public access to resources to prevent any deployment of resources with public access enabled

### What happened / Result

- New storage deployment with public access enabled, was denied
- Deployments with no public access enabled was allowed
- Existing resources was not affected

### Challenges I faced

- None

---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->

- Existing resources was not affected after enforcing the policy but when altered or updated the policy takes effect
- Governance of azure resources using policy and resource locks help the security administrator manage and prevent deployment of noncompliant resources and prevent accidental deletion of resource.
---

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->

- How can one remediate a resource to ensure the policy is applied

---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->

- https://www.youtube.com/watch?v=oN8ZdKTq-p0
- https://learn.microsoft.com/en-us/training/paths/security-governance-compliance/

---

*Submitted by: Elu Uchenna Emmanuel · eluemma*
