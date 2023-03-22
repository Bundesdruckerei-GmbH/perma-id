# perma-id
permanent Bundesdruckerei ID

## Purpose
The purpose of this repository is to provide a permanent secure URL following the w3id.org approach, just for BDr provided data.

## Example
### JSON-LD
````json
{ 
  "@context": "https://github.com/Bundesdruckerei-GmbH/perma-id/gaia-x/0.1/name",
  "familyName": "Mustermann",
  "givenName": "Erika"
}
````
### DID
````json
{
  "credential": {
    "@context": [
      "https://www.w3.org/2018/credentials/v1",
      "https://w3id.org/security/suites/jws-2020/v1",
      "https://schema.org"
    ],
    "type": "VerifiableCredential",
    "issuer": "did:web:github.com:Bundesdruckerei-GmbH:perma-id:gaia-x:0.1:name-did",
    "issuanceDate": "2010-01-01T19:23:24.651387237Z",
    "credentialSubject": {
      "familyName": "Mustermann",
      "givenName": "Erika"
    }
  }
}
````
