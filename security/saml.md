# What is SAML

Security assertion markup language

## Terms

### Single sign on (SSO)

Capability of user only having to sign on to centralized authenticator which will authenticate to multiple apps on behave of the user. This removes the need of multiple passwords

### Identity provider (IDP)

The centralized authenticator. Source of truth for the user identity

### Service provider (SP)

The app(s) that the user is trying to authenticate to

### SAML request / response

Communication between IDP and SP

### Assertion

The user statement communicated between IDP and SP. Assertions are signed with XML signatures (DSig)

### Assertion consumer service

Service in SP that handles assertion requests from IDP. They validate the DSigs

### Attributes

Properties of user noted in assertions

### Relay state

The state before authentication. Noted by IDP so that after authentication it could redirect them back to the app

### SAML trust

Configuration of how IDP and SP can communicate securly

### Metadata

The shareable contents of the SAML trust. IDP and SP uses it to configure themselves

### Provisioning

Process of IDP notifying / syncing identities to SPs so that they are update to date. This process is not required for SAML to function

1. JIT (just-in-time) provisioning: Process of creating or updating user in SP via IDP's metadata content in SAML response. This only happens when user tries to authenticate
2. Real time provisioning: IDP actively pushes user updates to SP regardless of whether user is trying to authenticate. This is done usually with SCIM (System for cross-domain identity management)

## Process

User can either authenticate:

1. Starting from IDP -> IDP sends SAML response to SP's assertion consumer service
2. Starting from SP -> SP's assertion consumer service sends SAML request to IDP -> IDP sends SAML response to SP's assertion consumer service

## Weaknesses

1. Assertion validation from SP can be incomplete
2. XML parsers may be exploited
3. Insecure libs

## Best practices

1. Assertion consumer service should limit XML parser features (disable document type fetching) to defend against XML external entities attack (XXE)
2. Use canonicalized XML: Normalize XML to a specific standard to protect against exploits like inner comment node manipulation 
3. Validate schema to prevent XML signature wrapping attacks (XSW). Use explicit XPath expressions
4. Validate every signature: Every assertion should be signed and reject partially signed assertions
5. Specify your signature algorithm so that hackers cannot forge it
6. Use HTTPS to encrypt request / response. Still can be susceptible to replay and XSS attacks
7. Validate parties
8. Enforce validation window: Only process SAML response during specified timeframe
9. Create a historical cache double the validation window timeframe to record all IDs to check for replay attacks
10. Limit buffer size to protect against DDoS attacks which attackers try to send oversized XML to try to shutdown the service

## Alternatives

1. OAuth
2. OpenID connect

SAML is to OpenID connect as SOAP is to REST

# Resources

1. [LINK](https://www.youtube.com/watch?v=l-6QSEqDJPo)
