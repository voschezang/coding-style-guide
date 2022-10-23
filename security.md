# Security

Flow

1. [Identification](https://en.wikipedia.org/wiki/Identity_(philosophy)). Comparing the identity of a requestor.
2. [Authentication](https://en.wikipedia.org/wiki/Authentication). Verifying the identity of a requestor.
3. [Authorization](https://en.wikipedia.org/wiki/Authentication).  Specifying access rights/privileges to resources.

E.g.

1. Identity: `Alice`
2. Authentication: a passport with her picture
3. Authorization: `Alice` has access to specific bank accounts



**Authentication**

[Verification](https://en.wikipedia.org/wiki/Authentication) of an [identity](https://en.wikipedia.org/wiki/Identity_(philosophy)). This can be done based on property that is unique to an identity. E.g. something that is known, in possession, a location or a real property such as a fingerprint. Combining multiple types of properties strengthens the verification through diversification.

- Shared secrets. A token or password known only to the client and the server. A client presents this secret to a server. The server verifies it.
    - The secret does not have to be send directly. Alternatives include:
        - A *hash* of the secret.
        - Proof by solving a numerical puzzle, using the secret.
- Proof of access to a private, external resource. E.g. an email account, a network, or a key.
- A reference to a trusted server. E.g. [certificates](https://en.wikipedia.org/wiki/Public_key_certificate) that are signed by a [certificate authority (CA)](https://en.wikipedia.org/wiki/Certificate_authority).



**Authorization**

[Specifying](https://en.wikipedia.org/wiki/Authorization) access rights or privileges to resources. Variants include:

- Unrestricted access. E.g. for unidentified (anonymous) users.
- A static mapping of identities to resources. E.g. a whitelist.
- Outsource authorization to an [IDP](https://en.wikipedia.org/wiki/Identity_provider). 
    - E.g. [Oauth](https://en.wikipedia.org/wiki/OAuth), where access is delegated from a user to a client application - without actually sharing the user's private credentials.
- Use a public channel to send a notification (an event). Then let the server initiate a response.




**Multi-factor Authentication (MFA)**
Combining multiple authentication methods.

**Conditional access**
Grant access requests [based on](https://learn.microsoft.com/en-us/azure/architecture/framework/security/design-identity-authentication) the requestors' trust level and the target resources' sensitivity.
