# perma-id
permanent Bundesdruckerei ID

## Purpose
The purpose of this repository is to provide a permanent secure URL following the w3id.org approach, just for BDr provided data.

## Description
Base for dezentralized document and schema validation is the oppurtunity to retrieve schema definitions using a static resource location. This resource can get used by the publisher as well any other organizations which are developing implementations based on these schemas.

For example Bundesdruckerei is printing the german identity card, thats why the Bundesdruckerei can provide schema definition for validation of the identity card numbers. Within this repo Bundesdruckerei is providing schemas which are fulfilling the validation needs for these data types.

## Example
### JSON-LD
````json
{ 
  "@context": "https://github.com/Bundesdruckerei-GmbH/perma-id/gaia-x/0.1/name",
  "familyName": "Mustermann",
  "givenName": "Erika"
}
````
### SHACL
````json
{
  "@context": {
    "cc": "http://creativecommons.org/ns#",
    "schema": "http://schema.org/",
    "sh": "http://www.w3.org/ns/shacl#",
    "bdr-gaiax": "https://github.com/Bundesdruckerei-GmbH/perma-id/gaia-x/0.1/name-shacl#",
    "did": "https://www.w3.org/TR/did-core/#"
  },
  "@id": "did:web:github.com:Bundesdruckerei-GmbH:perma-id:gaia-x:0.1:name-did",
  "@type": "bdr-gaiaxg",
  "bdr-gaiax:familyName": {
    "@value": "Mustermann",
    "@type": "xsd:string"
  },
  "bdr-gaiax:givenName": {
    "@value": "Erika",
    "@type": "xsd:string"
  }
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
## More Information
- [W3C DID Core 1.0](https://www.w3.org/TR/did-core/)
- [W3C Shapes Constraint Language (SHACL)](https://www.w3.org/TR/shacl/)
- [JSON-LD](https://json-ld.org/)

## About
![Bundesdruckerei GmbH](https://www.bundesdruckerei.de/themes/custom/bdr_bootstrap5/assets/img/bdrgruppe-color.svg)  Bundesdruckerei GmbH
