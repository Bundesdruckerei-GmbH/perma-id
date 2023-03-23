# perma-id
permanent Bundesdruckerei ID

## Purpose
The purpose of this repository is to provide a permanent secure URL following the w3id.org approach, just for BDr provided data.

## Description
Base for dezentralized document and schema validation is the oppurtunity to retrieve schema definitions using a static resource location. This resource can get used by the publisher as well any other organizations which are developing implementations based on these schemas.

Following these dezentralized manner, Bundesdruckerei is providing schemas which are fulfilling the validation needs for data Bundesdruckerei is the best organization to provide. For example Bundesdruckerei is publishing the german identity card, thats why the Bundesdruckerei can provide Schema definition for validation of the identity card numbers.

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
