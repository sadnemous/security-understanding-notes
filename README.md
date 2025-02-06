### <mark>Question-1</mark>: What are the different part of web security authentication, authorization, encryption (data at rest, data in transition)?
In web security, the key components are
- Authentication (verifying a user's identity).
- Authorization (determining what a user can access once authenticated), and
- Encryption which can be further divided into
"data at rest" (encrypted data stored on a server) and
o "data in transit" (encrypted data while being transferred across a network),
each with its own specific security measures to protect information from unauthorized access.
Authentication:
- Usernames and passwords: Basic method where users provide their credentials to log in.
- Multi-factor authentication (MFA): Requires additional verification like a code sent to a phone besides the password.
- Biometrics: Using physical characteristics like fingerprints or facial recognition for authentication.
- Single Sign-On (SSO): Allows users to log in to multiple applications with a single set of credentials.
Authorization:
- Access control lists (ACLs): Define which usens can access specific resources or functionalities within a system.
- Role-based access control (RBAC): Assigns permissions based on a user's role within an organization.
- Attribute-based access control (ABAC): Grants access based on dynamic attributes like location or time.
Encryption:
- Data at rest:
- Full disk encryption: Encrypting entire hard drives where data is stored.
- Database encryption: Encrypting data within a database.
- File system encryption: Encrypting individual files on a system.
- Data in transit:
- Transport Layer Security (TLS): Secure protocol used to encrypt data transmitted over the internet (HTTPS).
- Secure Shell (SSH): Securely managing remote servers.
- Virtual Private Networks (VPNs): Creating a secure tunnel for data transmission over a public network.

### <mark> Question-2</mark>: Where CyberArk safe is to be applied in terms of web security, is it Authentication, Authorization, Encryption?
Explanation:
* Authentication:
While CyberArk can be used to manage user login credentials, its primary function is not to handle the initial verification of a user's identity; this is usually done by a separate authentication system.
* Authorization:
The core strength of CyberArk lies in its ability to define granular access controls for privileged accounts stored within its "Safes," ensuring that only authorized users can access specific sensitive data or systems.
* Encryption:
CyberArk does utilize encryption to protect the stored credentials within its vault, but this is a secondary function to the primary focus on authorization and access control.
Key points about CyberArk Safes:
* Storing sensitive credentials:
Safes act as a central repository for storing privileged accounts, including passwords, SSH keys, and API keys.
* Granular access control:
Administrators can define strict policies within each Safe to control who can access which accounts based on their roles and permissions.
* Auditing and reporting:
CyberArk provides detailed logs and reporting capabilities to monitor privileged access activity.

### <mark>Question-3</mark>: What is TLS and mTLS and what is the difference?
TLS stands for Transport Layer Security, a protocol that encrypts data between two communicating parties, primarily authenticating the server to the client;
mTLS (Mutual TLS) is an enhanced version of TLS where both the client and server mutually authenticate each other by presenting their own certificates, providing a higher level of security compared to standard TLS.
Key difference:
* Authentication direction: In TLS, only the server is verified by the client, whereas in mTLS, both the client and server verify each other's identities.
Use cases:
* TLS: Secure web browsing, email communication, VPN connections
* mILS: API security, microservices, loT security, enterprise networks where strict client verification is required.

### Further Read:
 - https://pinggy.io/blog/transport 
layer security vs mutual transport layer security
 - https://www.securew2.com/blog/mutual-tls-mtls-authentication

#### Summary
<b>1. What is Transport Layer Security (TLS)?</b>
* TLS is a cryptographic protocol that secures communication over a network by encrypting data and authenticating the server's identity. It ensures privacy, data integrity, and protection against eavesdropping during transmission.

<b>2. How TLS Works:</b>
 - Step 1: The client sends a message to the server with supported TLS configurations.
 - Step 2: The server responds with its certificate and selected configurations.
 - Step 3: The client validates the server's certificate, and both parties exchange keys to establish an encrypted session.

<b>3. What is Mutual Transport Layer Security (mTLS)?</b>

mTLS builds on TLS by requiring mutual authentication, where both the client and server authenticate each other through digital certificates, ensuring bidirectional trust and enhanced security.


<b>4. How mTLS Works:</b>
 - Step 1: The client proposes configurations and sends its certificate to the server.
 - Step 2: The server responds with its own certificate and selected configurations.
 - Step 3: Both parties validate each other's certificates, and a secure channel is established using a shared session key.

<b>5. Key Differences Between TLS and mTLS:</b>
* Authentication: TLS is one-way (server only); mTLS is two-way (both client and server).
* Security: mTS provides higher security through mutual authentication.
* Complexity: mTS is more complex to implement due to certificate management for both parties.

<b>6. Use Cases:</b>
* TLS: Web browsing, email communication, and VPN connections.
* mILS: APl security, microservices, loT security, and enterprise networks.

<b>7. Pros and Cons:</b>
* TLS: Simple to implement, but does not authenticate the client.
* mTLS: Robust security with mutual authentication, but more complex to manage and implement.

<b>8. Challenges:</b>
* TLS: Managing server certificates and backward compatibility.
* mTLS: Client certificate management and configuration complexity.



