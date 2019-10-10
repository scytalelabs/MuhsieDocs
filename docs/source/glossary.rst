Glossary
========

Agent
^^^^^
A software program or process used by or acting on behalf of an Entity to interact
with other Agents or with other distributed ledgers. Agents 
are of two types: Edge Agents run at the edge of the network on a local device; 
Cloud Agents run remotely on a server or cloud hosting service. Agents require 
access to a Wallet in order to perform cryptographic operations on behalf of the Entity they represent.

Agent-to-Agent (A2A) Protocol
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A protocol for communicating between Agents to form Connections, exchange Credentials,
and have other secure private Interactions. A less technical synonym is DID Communication



Cloud Agent
^^^^^^^^^^^
An Agent that is hosted in the cloud. It typically operates on a computing device over 
which the Identity Owner does not have direct physical control or access. Mutually 
exclusive with Edge Agent. A Cloud Agent requires a Wallet and typically has a Service 
Endpoint. Cloud agents may be hosted by an Agency.

Connection
^^^^^^^^^^
A cryptographically verifiable communications channel established using an Agent-to-Agent
Protocol between two DIDs representing two Entities and their associated Agents. Connections
may be Edge-to-Edge Connections or Cloud-to-Cloud Connections. Connections may be used to
exchange Verifiable Credentials or for any other communications purpose. Connections may 
be encrypted and decrypted using the Public Keys and Private Keys for each DID. A Connection 
may be temporary or it may last as long as the two Entities desire to keep it. Two Entities 
may have multiple Connections between them, however each Connection must be between a unique
pair of DIDs.

Connection Invitation
^^^^^^^^^^^^^^^^^^^^^
An Agent-to-Agent Protocol message type sent from one Entity to a second Entity to invite the 
second Entity to send a Connection Request.

Connection Request
^^^^^^^^^^^^^^^^^^
An Agent-to-Agent Protocol message type sent from one Entity to a second Entity to request to 
form a Connection.

Credential
^^^^^^^^^^
A digital assertion containing a set of Claims made by an Entity about itself or another 
Entity. Credentials are a subset of Identity Data. A Credential is based on a Credential 
Definition. The Entity described by the Claims is called the Subject of the Credential. The
Entity creating the Credential is called the Issuer. The Entity holding the issued Credential
is called the Holder. If the Credential supports Zero Knowledge Proofs, the Holder is also called
the Prover. The Entity to whom a Credential is presented is generally called the Relying Party,
and specifically called the Verifier if the Credential is a Verifiable Credential. Once issued,
a Credential is typically stored by an Agent. (In Hyperledger Indy Infrastructure, Credentials are not 
stored on the Ledger.) Examples of Credentials include college transcripts, driver licenses,
health insurance cards, and building permits.

Credential Definition (CredDef)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A machine-readable definition of the semantic structure of a Credential based on one or more Schemas.
Hyperledger Indy Infrastructure, Credential Definitions are stored on the Hyperledger Indy Ledger. Credential
Definitions must include an Issuer Public Key. Credential Definitions facilitate interoperability 
of Credentials and Proofs across multiple Issuers, Holders, and Verifiers.

Credential Offer
^^^^^^^^^^^^^^^^
An Agent-to-Agent Protocol message type sent from an Issuer to a Holder to invite the Holder 
to send a Credential Request to the Issuer.

Credential Request
^^^^^^^^^^^^^^^^^^
An Agent-to-Agent Protocol message type sent from a Holder to an Issuer to request the 
issuance of a Credential to that Holder.

Credential Exchange
^^^^^^^^^^^^^^^^^^^
A set of Interaction Patterns within an Agent-to-Agent Protocol for exchange of Credentials 
between Entities acting in Credential Exchange Roles.

Decentralized Identifier (DID)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A globally unique identifier developed specifically for decentralized systems as defined
by the W3C DID specification. DIDs enable interoperable decentralized Self-Sovereign Identity
management. A DID is associated with exactly one DID Document.

Edge Agent
^^^^^^^^^^
An Agent that operates at the edge of the network on a local device, such as a smartphone, 
tablet, laptop, automotive computer, etc. The device owner usually has local access to the 
device and can exert control over its use and authorization. Mutually exclusive with Cloud 
Agent. An Edge Agent may be an app used directly by an Identity Owner, or it may be an operating
system module or background process called by other apps. Edge Agents typically do not have a
publicly exposed Service Endpoint in a DID Document, but do have access to a Wallet. Note that 
the local device may itself be an Active Thing with its own Agent, and for which the Identity 
Owner is the Thing Controller.

Proof
^^^^^
Cryptographic verification of a Claim or a Credential. A digital signature is a simple form of 
Proof. A cryptographic hash is also a form of Proof. Zero Knowledge Proofs enable selective
disclosure of the information in a Credential.

Proof Request
^^^^^^^^^^^^^
The data structure sent by a Verifier to a Holder that describes the Proof required by the 
Verifier. Proof Requests are sent and received using the DID Communication protocol between two agents.

Prover
^^^^^^
A role played by an Entity when it generates a Zero Knowledge Proof from a Credential. The 
Prover is also the Holder of the Credential. 

Holders and Provers
^^^^^^^^^^^^^^^^^^^
The Holder of a Credential is the Individual or Organization (or in some cases the Thing) to
whom it was issued. The Credential is stored in the Holder’s Wallet where it can be used
produce Proofs. When a Holder responds to a Proof Request from a Verifier by producing a 
Proof, the Holder is called the Prover.


Revocation
^^^^^^^^^^
The act of an Issuer revoking the validity of a Claim or a Credential.

Schema
^^^^^^
A machine-readable definition of the semantics of a data structure. Schemas are used to
define the Attributes used in one or more Credential Definitions.

Verifier
^^^^^^^^
An Entity who requests a Credential or Proof from a Holder and verifies it in order to 
make a trust decision. Based on the definition provided by the W3C
Verifiable Claims Working Group.

Wallet
^^^^^^ 
A software module, and optionally an associated hardware module, for securely storing and 
accessing Private Keys, Master Secrets, other sensitive cryptographic key material, and other
Private Data used by an Entity. A Wallet is accessed by an Agent.

Zero Knowledge Proof
^^^^^^^^^^^^^^^^^^^^    
A Proof that uses special cryptography and a Master Secret to support Selective Disclosure of
information about a set of Claims from a set of Credentials. A Zero Knowledge Proof provides 
cryptographic proof about some or all of the data in a set of Credentials without revealing 
the actual data or any additional information, including the Identity of the Prover.
