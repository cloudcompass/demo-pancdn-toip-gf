# Schema

## Introduction

The BC Person Credential Schema (BCPSC) described in this document is published by the Government of British Columbia for the purpose of enabling the province to become an issuer of the credential. Credential’s issued based on this schema contain authoritative digital identity data attributes about the Holder held by the issuer, such as their name and date of birth (see full list of attributes below).

That BC is the publisher and only issuer of this BC-specific schema is hoped to be an interimum step towards reaching agreement on a “Pan-Canadian Person Credential Schema” that will be used by issuers from some or all jurisdictions in Canada.

## Machine Readable Governance Information

* &lt;Link to Overlays Capture Architecture: Source>
* &lt;Link to Overlays Capture Architecture: Published>

## The TITLE Schema

The BC Person Credential Schema is defined to allow the issuance of a credential that provides the Holder with the core digital identity attributes held by an jurisdictional authority about the resident of the jurisdiction, such that the Holder can share those attributes with the veirfiers of their choice.

The specific attributes in the credential about the subject include the following and are intended to come from the current digital identity record about the Holder. Technical details about each of the attributes follow in this section of the document.

* givenNames: The names, excluding the surname, of the resident.
* ...

In addition, the following metadata about the resident’s digital identity record is included in the credential:

* iss_dateint: The date the credential was issued to the resident.
* loa: The “Level of Assurance” (LOA) about the collection of the data included in the credential. The LOA is a number from 1-4 and is based on the LOA definition in the Pan Canadian Trust Framework, Public Sector Profile V1.1, which can be found [here](https://canada-ca.github.io/PCTF-CCP/Version1_1/).

### Attributes

#### givenNames

A UTF-8 encoded string containing the names of the Subject, excluding the surname. If the Subject of the credential has only a single name (a mononym), the givenNames field will be an empty string (“”). If the person has multiple names, the names are in order (e.g. first name, first middle name, etc.), space-separated. No differentiation is made for a single name with or without spaces. For example, the value of giveNames is the same for a person having just a first name of “Jim Bob” and a person with a first name “Jim” and a single middle name “Bob”. 

### MORE ATTRIBUTES...

## Intended Use of the BC Person Credential

The BC Person credential is intended to allow a Holder to prove that they are a resident of the issuing jurisdiction (possession of the credential), and to provide authoritative demographic information about themselves to a verifier.

Note that all of the demographic information in the Person credential is Personally Identifiable Information (PII) and as such,

* The Holder should take care in deciding with whom they share the information, and for what purpose.
* Verifiers receiving the information MUST handle the data in a manner consistent with the Privacy Laws of the jurisdiction in which they operate, and the (if different) the jurisdiction of the issuer of the credential.

Example uses of this credential are plentiful:

* Collecting the name of a person opening a bank account.
* Collecting the name of a new hire joining a company.
* Providing the name of a person requesting a Criminal Records Check.
* Completing an online form requiring the entry of data in the credential.
* Verifying the person is a resident of a jurisdiction and is thus entitled to a discount on a product or service.
* Verifying a person is of age to, for example, purchase alcohol in a jurisdiction.

Verifiers MUST NOT request attributes from the credential for purposes where they are not needed. For example, when verifying the age of a person when purchasing alcohol, the credentials issued based on the BC Person Credential schema can be used to prove the person is over the age of 19 without sharing any other information from the credential. Sample presentation requests are provided in the 
[Technical Information](#sample-presentation-requests) section of this document.

## Contact for Additional Information

For more more information about the use this document please contact the publisher of this Schema, the BC Ministry of Citizen Services using this email address: [idiminfo@gov.bc.ca](mailto:idiminfo@gov.bc.ca)

## Technical Information

### Ledger Information

Ledger: [CANdy-Dev](https://candyscan.idlab.org/home/CANDY_DEV)

Schema Creator DID: &lt;DID with Link to Ledger Txn>

Schema ID: &lt;SCHEMA ID with Link to Ledger Txn>

### Sample Presentation Requests

&lt;To Be Added>
