# SWIFT & PCI DSS SIEM Use Cases

118 SIEM detection use cases for the two payment rails a bank is assessed on — the **SWIFT application estate** and the **cardholder data environment**. Every entry carries a **use case name**, the **log sources** it needs, and a **sample log** to build and unit-test the rule against.

- **SWIFT CSP** (55) — Alliance Access, Alliance Gateway, SWIFTNet Link, Alliance Web Platform, the HSM and the secure zone, plus FIN (MT) and ISO 20022 (pacs/camt) message flow, mapped to the Customer Security Controls Framework (CSCF) objectives 1–7
- **PCI DSS v4.0.1** (63) — Requirements 1–12 across network security controls, stored account data, transmission security, malware, secure software (including the v4 payment-page script requirements 6.4.3 / 11.6.1), access control, authentication, physical security, logging and security testing

Detection categories span payment message integrity, fraudulent payment behaviour, counterparty/RMA management, operator and access control, secure zone integrity, cryptographic and key management, availability and reconciliation, and logging and monitoring.

## Files

- `index.html` — the published, filterable use case library (GitHub Pages)
- `usecases.json` — the structured dataset behind it
- `usecases.csv` — the same content as a spreadsheet: Use Case Name, Log Source, Sample Log

Live site: https://laklubin.github.io/swift-siem-use-case/

## Caveats

**Control references are an engineering aid, not an attestation.** Your assessor scopes and judges compliance, and a single use case rarely satisfies a control on its own.

**Sample logs are synthetic.** They are written in the shape the named product emits so a rule can be drafted and tested, but field names, formats and message types vary by version, parser and local configuration — validate each against your own telemetry before deploying. All hostnames, BICs, IBANs, account numbers, IP addresses, card BINs and operator IDs are fabricated.

Sources: [SWIFT Customer Security Programme](https://www.swift.com/myswift/customer-security-programme-csp), [PCI Security Standards Council](https://www.pcisecuritystandards.org/document_library/)

Maintained by LK for payment assurance and detection engineering reference.
