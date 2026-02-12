# Architecture decision record

<!--
Use this template to propose technical and organisational decisions for Naamio
Data Space. After creating this issue, draft your full proposal using the
template at templates/adr.md and submit a merge request.
-->

## Overview
### Title
### Affected projects
- [ ] Storage (encrypted object storage, key-value store, abstraction layer, single-binary deployment)
- [ ] Structure (data models, tenant isolation, indexing, schema management, configuration)
- [ ] Synchronisation (cross-device sync, CRDTs, offline-first, MLS encryption)
- [ ] Portability (EU Data Act, import/export, Solid Protocol interoperability)
- [ ] Services (gRPC interface, event system, API gateway, protocol plugin dispatch)
- [ ] Federation (clustering, sharding, failover, peer discovery)
- [ ] Extensions (Wasm host, WASI 0.2, host-provided primitives, protocol plugins via gRPC)
- [ ] Sovereignty (GDPR automation, data residency, audit trails, compliance)
- [ ] Other:

---

## Problem statement
### Current situation
### Decision drivers

---

## Proposed decision
### Chosen approach
### Rationale
### Alternatives considered

---

## Impact summary

---

## Next steps
- [ ] Draft full proposal in `adrs/XXXX-title.md`
- [ ] Submit merge request for review
- [ ] Address feedback from technical leads
- [ ] Update status after decision

---

## Governance

This decision follows the
[Omnifi Foundation governance model](https://handbook.omnifi.foundation/engineering/architecture/governance/).

/label ~"adr" ~"architecture" ~"technical"
