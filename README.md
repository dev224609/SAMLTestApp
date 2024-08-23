## Usage

### Dynamic IdP Configuration from IdP Metadata (Recommended)

`node bin/server.js --idpMetaUrl {url}`

> The default protocol is SAMLP if metadata supports both SAMLP and WS-Federation

#### Example

`node bin/server.js --idpMetaUrl https://example.okta.com/app/exkikd6nFJIdpcrZR0g3/sso/saml/metadata`


### Options

`node bin/server.js  --help`

```
Options:
  --version                      Show version number                                                                                                       [boolean]
  --settings                     Path to JSON config file
  --port, -p                     Web Server listener port                                                                        [number] [required] [default: 7070]
  --protocol                     Federation Protocol                                                                          [string] [required] [default: "samlp"]
  --idpIssuer, --iss             IdP Issuer URI                                                                                [string] [default: "urn:example:idp"]
  --idpSsoUrl                    IdP Single Sign-On Service URL (SSO URL)                                                                                   [string]
  --idpSsoBinding                IdP Single Sign-On AuthnRequest Binding         [string] [required] [default: "urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect"]
  --idpSloUrl                    IdP Single Logout Service URL (SLO URL) (SAMLP)                                                                            [string]
  --idpSloBinding                IdP Single Logout Request Binding (SAMLP)       [string] [required] [default: "urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect"]
  --idpCert                      IdP Public Key Signing Certificate (PEM)                                                                                   [string]
  --idpThumbprint                IdP Public Key Signing Certificate SHA1 Thumbprint                                                                         [string]
  --idpMetaUrl                   IdP SAML Metadata URL                                                                                                      [string]
  --audience, --aud              SP Audience URI / RP Realm                                                                     [string] [default: "urn:example:sp"]
  --providerName                 SP Provider Name                                                                 [string] [default: "Simple SAML Service Provider"]
  --acsUrls                      SP Assertion Consumer Service (ACS) URLs (Relative URL)                                 [array] [required] [default: ["/saml/sso"]]
  --signAuthnRequests, --signed  Sign AuthnRequest Messages (SAMLP)                                                             [boolean] [required] [default: true]
  --signatureAlgorithm           Signature Algorithm                                                                                [string] [default: "rsa-sha256"]
  --digestAlgorithm              Digest Algorithm                                                                                       [string] [default: "sha256"]
  --requestNameIDFormat          Request Subject NameID Format (SAMLP)                                                                     [boolean] [default: true]
  --validateNameIDFormat         Validate format of Assertion Subject NameID                                                               [boolean] [default: true]
  --nameIDFormat, --nameid       Assertion Subject NameID Format                        [string] [default: "urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress"]
  --requestAuthnContext          Request Authentication Context (SAMLP)                                                                    [boolean] [default: true]
  --authnContextClassRef, --acr  Authentication Context Class Reference      [string] [default: "urn:oasis:names:tc:SAML:2.0:ac:classes:PasswordProtectedTransport"]
  --spCert                       SP/RP Public Key Signature & Encryption Certificate (PEM)          [string] [default: "/Users/karl/src/saml-sp/config/sp-cert.pem"]
  --spKey                        SP/RP Private Key Signature & Decryption Certificate(PEM)           [string] [default: "/Users/karl/src/saml-sp/config/sp-key.pem"]
  --httpsPrivateKey              Web Server TLS/SSL Private Key (PEM)                                                                                       [string]
  --httpsCert                    Web Server TLS/SSL Certificate (PEM)                                                                                       [string]
  --https                        Enables HTTPS Listener (requires httpsPrivateKey and httpsCert)                                          [boolean] [default: false]
  --relayState, --rs             Default Relay State                                                                                                        [string]
  --help                         Show help                                                                                                                 [boolean]
```
