* Authorization
    * Authentication is the act of validating that users are whom they claim to be. This is the first step in any security process. 
    * Giving someone permission to download a particular file on a server or providing individual users with administrative access to an application are good examples of authentication.
    * In some instances, systems require the successful verification of more than one factor before granting access. This multi-factor authentication (MFA) requirement is often deployed to increase security beyond what passwords alone can provide.
    * Examples: Passwords, One-time pins, Authentication apps, Biometics
* Authentication 
    * Authorization in a system security is the process of giving the user permission to access a specific resource or function. This term is often used interchangeably with access control or client privilege.
    * In secure environments, authorization must always follow authentication. Users should first prove that their identities are genuine before an organization’s administrators grant them access to the requested resources.
* Authentication vs. Authorization
    * Authentication, in the form of a key. The lock on the door only grants access to someone with the correct key in much the same way that a system only grants access to users who have the correct credentials.
    * Authorization, in the form of permissions. Once inside, the person has the authorization to access the kitchen and open the cupboard that holds the pet food. The person may not have permission to go into the bedroom for a quick nap. 
    * Differences
        * What does it do?: Verifies credentials VS grants or denies permission
        * How does it work?: Through passwords, biometrics, one-time pins, or apps VS Through settings maintained by security teams
        * Is it visible to the user? Yes VS No
        * It is changeable by the user? Partially VS No
        * How does data move? ID Tokens VS Access Token
* JSON Web Token
    * Abstract JSON Web Token
    * Abstract. JSON Web Token (JWT) is a means of representing claims to be transferred between two parties. The claims in a JWT are encoded as a JSON object that is digitally signed using JSON Web Signature (JWS) and/or encrypted using JSON Web Encryption (JWE).
* Claims
    * Claims are pieces of information about a user that have been packaged, signed into security tokens and sent by an issuer or identity provider to relying party applications through a security token service (STS).
* IDaaS
    * Identity as a service (IDaaS) is a SaaS-based IAM offering that allows organizations to use single sign-on (SSO using SAML or OIDC), authentication and access controls to provide secure access to their growing number of software and SaaS applications.
