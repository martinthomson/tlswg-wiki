# TLS WG FAQs

This page holds answers to frequently asked questions in the TLS WG. Pull requests to maintain this page are highly encouraged.

## What is in scope for the TLS WG?

The TLS working group concerns itself with the maintenance of the core TLS protocol. This includes the TLS and DTLS specification, plus any extensions that have wide applicability to TLS usage. 

## What is out of scope for the TLS WG?

Anything not in the previous question, though there are a few things in particular:

1. Certificates or Certification Authorities: The [IETF LAMPS](https://datatracker.ietf.org/wg/lamps/documents/) WG does some maintenance on certificates. Concerns about the Web PKI should be taken to the [CA/Browser Forum](https://cabforum.org/).
2. Cryptographic primitives: The [IRTF Crypto Forum Research Group (CFRG)](https://irtf.org/cfrg) is one venue that you can discuss standardizing new primitives.
3. Application or domain-specific extensions to TLS: The working group usually only considers extensions to the protocol that are widely applicable. If your extension is specific to an application or deployment, the working group might not consider adopting the work. You are still encouraged to discuss such work, particularly if you are not sure. The working group has many people with considerable expertise in this area.

## I have a proposal for the TLS WG — what is the best way to see if others are interested in it?

There are several things you can do to gauge interest. First, it might help to look through the WG archives for related ideas. If the same proposal was brought to the group and rejected, understanding the rationale for said decision is an important piece of historical data to consider. Have circumstances changed since that decision such that the idea is now practical? 

If there are no obviously related drafts, the next step is write up the idea in an Individual Draft and submit it to the working group for discussion. Be sure to carefully motivate the problem in consideration and clearly describe the proposed solution. If applicable, also discuss the extent to which the proposal’s security properties have been studied or formally analyzed. It’s common to submit new ideas without any sort of analysis.

## What do I need to register codepoints for TLS ciphersuites, extensions, etc.?

RFC 8446 and 8447 describe new processes by which IANA codepoints are allocated for TLS. See [RFC8447](https://tools.ietf.org/html/rfc8447) for more details on this process. Importantly, RFC 8447 changed some codepoint registration policies to Specification Required. This means registrations are permitted given (1) a permanent and readily available public specification describing the registration (extension, ciphersuite, etc.), such as an Internet Draft, and (2) review by the TLS designated experts, who may be reached at tls-reg-review@ietf.org. The Expert Review policy only requires sign-off from the TLS designated experts.

The following list enumerates all items whose policy is Expert Review.

1. [TLS Application-Layer Protocol Negotiation (ALPN) Tokens](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml#alpn-protocol-ids)
2. [TLS Heartbeat Message Types](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#heartbeat-message-types)
3. [TLS Heartbeat Modes](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#heartbeat-modes)

The following list enumerates all items whose policy is Specification Required.

1. [TLS Ciphersuites](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-4)
2. [TLS ClientCertificateTypes, in the range 64-223](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-2)
3. [TLS Supported Groups](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-8)
4. [TLS EC Point Formats](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-9)
5. [TLS EC Curve Types](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-10)
6. [TLS UserMappingType, in the range 64-223](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-14)
7. [TLS Signature Algorithm, in the range 64-223](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-16)
8. [TLS HashAlgorithm, in the range 64-223](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-18)
9. [TLS Exporter Labels](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#exporter-labels)
10. [TLS Authorization Data Format, in the range 64-223](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#authorization-data)
11. [TLS SignatureScheme](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-signaturescheme)
12. [TLS PskKeyExchangeMode](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-pskkeyexchangemode)
13. [TLS Extensions](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml#tls-extensiontype-values-1)
14. [TLS Certificate Types](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml#tls-extensiontype-values-3)
15. [TLS CachedInformationType, in the range 64-223](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml#cachedinformationtype)

The following list enumerates all items whose policy is neither Expert Review nor Specification Required.

1. [TLS ClientCertificateTypes, in the range 0-63](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-2)
2. [TLS ContentType](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-5)
3. [TLS Alerts](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-6)
4. [TLS HandshakeType](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-7)
5. [TLS Supplemental Data Formats](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-12)
6. [TLS UserMappingType, in the range 0-63](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-14)
7. [TLS Signature Algorithm, in the range 0-63](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-16)
8. [TLS CachedInformationType, in the range 0-63](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml#cachedinformationtype)
9. [TLS HashAlgorithm, in the range 0-63](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-18)

## Should the WG adopt and work on my draft?

In short, the TLS WG aims to adopt work items that introduce core changes to the TLS protocol or extensions which have wide applicability and use. In practice, this means documents with intended Proposed Standard status or which seek recommended registry (Y) codepoints should aim for WG adoption. This is to ensure that any significant change to TLS receives adequate community review prior to publication.

RFC2026 (BCP 9) describes the differences between different document status levels, i.e., Proposed Standard, Experimental, or Informational. Briefly, Standards track documents expect significant community review prior to completion. In contrast, Informational documents encapsulate information for the community, without any form of consensus around the information, and Experimental documents aim to record some technology development efforts for the broader community. 

Documents which aim to seek non recommended codepoints (N) do not require WG adoption, and should follow the Specification Required process outlined above for codepoint registration. Documents which target Experimental status should only seek adoption if they introduce non-trivial changes to TLS. Likewise, documents which target Informational status should consult the TLS WG to see if there’s interest in the WG adopting the work for the purposes of broad review. Otherwise, said documents do not require adoption.

## Will my proposal require formal analysis before acceptance by the WG? 

In general, this depends on the draft in question. Formal analysis may be required by the group prior to any draft advancing to IESG (towards RFC publication). Some proposals may introduce sufficiently invasive changes that the WG deems formal analysis necessary prior to adoption in the group. Others may be uncontroversial and therefore require no formal analysis. If you are unsure about your proposal, please contact the TLS WG chairs (tls-chairs@ietf.org) for clarification.

## My proposal introduces a new TLS extension — is it relevant for the TLS WG, or does it require review by the TLS WG?

Many working groups propose new TLS extensions for use. See [RFC5764](https://tools.ietf.org/html/rfc5764) and [RFC8472](https://tools.ietf.org/html/rfc8472) as recent examples of such extensions. However, as per the new registration process outlined above, only TLS designated expert review is required for said extensions prior to allocation. 

Authors are encouraged to ask the TLS WG for review of their extension to ensure proper use.

## My proposal describes usage of TLS — is it relevant for the TLS WG, or does it require review by the TLS WG?

No, it does not require review by the TLS WG. However, we encourage authors to seek best current practice guidance from the TLS WG. 

## My proposal describes a profile for TLS — is it relevant for the TLS WG, or does it require review by the TLS WG?

No, it does not require review by the TLS WG. However, we encourage authors to seek best current practice guidance from the TLS WG. 

## Outside of the TLS WG, what are good working groups to consult if my proposal impacts TLS?

If your proposal introduces new cryptographic algorithms or mechanisms, or even uses existing mechanisms, consider reaching out to the [IRTF Crypto Forum Research Group (CFRG)](https://irtf.org/cfrg) for consultation. 

