# My Notes — Emunefe Saturday

## 

## Key Concepts I Learned

1\. Microsoft Entra ID



Microsoft Entra ID is Microsoft's cloud-based Identity and Access Management (IAM) solution. It enables organizations to securely manage user identities, authenticate users, and control access to applications, devices, and organizational resources. By centralizing identity management, it helps improve security while simplifying user access across cloud and on-premises environments.



2\. Identity as a Layer in Microsoft's Defense in Depth Strategy



Identity is one of the most critical security layers in Microsoft's Defense in Depth strategy. Since every user must authenticate before accessing organizational resources, protecting identities helps prevent unauthorized access. A strong identity security strategy includes secure authentication, continuous monitoring, and access controls to reduce the risk of cyberattacks.



3\. Multi-Factor Authentication (MFA)



Multi-Factor Authentication (MFA) strengthens account security by requiring users to provide two or more forms of verification before gaining access. Even if an attacker obtains a user's password, they cannot access the account without the additional verification factor, such as a mobile authentication app, SMS code, or biometric authentication.



4\. Security Defaults



Security Defaults are a collection of preconfigured security settings provided by Microsoft for every Microsoft Entra tenant. They are designed to offer baseline protection with minimal administrative effort. These settings automatically enforce essential security measures, such as requiring administrators to use MFA and blocking legacy authentication protocols that are vulnerable to attacks.



5\. Conditional Access



Conditional Access is a policy-based security feature that uses "If...Then..." logic to determine whether a user should be granted access to organizational resources.



For example:



If a user signs in from an unfamiliar location,

Then require Multi-Factor Authentication before granting access.



Organizations can create policies based on conditions such as:



User or group membership

Device compliance

Geographic location

Sign-in risk

Application being accessed



This enables organizations to provide secure access while minimizing unnecessary restrictions for trusted users.



6\. Conditional Access Deployment Strategy



Before implementing Conditional Access policies, organizations should develop a well-planned deployment strategy. Testing policies with a small group of users first helps identify potential issues and prevents accidental lockouts or disruptions to business operations. A phased rollout ensures policies work as intended before being applied organization-wide.



7\. Privileged Identity Management (PIM)



Privileged Identity Management (PIM) helps organizations protect highly privileged accounts by minimizing permanent administrative access. Instead of users having continuous administrator privileges, PIM provides just-in-time (JIT) access, allowing users to activate elevated permissions only when required and for a limited period. This approach significantly reduces the risk of privilege misuse and unauthorized administrative actions.

## Lab / Hands-On Work



### What I did

#### 

Learnt how to  Create a Conditional Access policy to require **Multi-Factor Authentication (MFA)** for a test user.

&#x20;Also learnt how to Configure and review the policy to ensure MFA was enforced during cloud application sign-in.



### What happened / Result



&#x20;Learned how Conditional Access strengthens sign-in security.

Configured MFA to add an extra layer of account protection.

&#x20;Understood how PIM reduces permanent administrator privileges through temporary role activation.



### Challenges I faced





Lack of access to an administrator account for hands-on practice.

Differentiating between Security Defaults and Conditional Access.

Understanding the importance of planning Conditional Access policies to prevent user lockouts.



## My Takeaways

Identity is a critical security boundary in cloud environments.

MFA significantly improves account security.

Conditional Access enforces security based on defined conditions.

PIM supports the principle of least privilege by providing temporary privileged access.

## Resources I Found Useful

* Microsoft Learn
* GitHub



*Submitted by: Saturday Emunefe · SaturdayEmu*



