# Naamio Data Space — architecture

Architecture decision records, data model specifications, and protocol specifications for [Naamio Data Space](https://naamio.dev).

Naamio Data Space is the private data store at the core of Naamio Space. It provides encrypted object storage, key-value persistence, and a dual extension model — Wasm components for storage-level extensions and gRPC for protocol plugins — enabling protocol support (Solid, WebDAV, CalDAV, JMAP, and others) without modifying the core.

## Milestone track

Codenames drawn from celestial phenomena — from the nebula where matter first coalesces to the event horizon that defines your sovereign boundary.

| Milestone | Focus | Due |
|---|---|---|
| Nebula — Foundation | Core storage engine, encrypted object store, key-value, single-binary deployment | 2026-06-30 |
| Gravity — Structure | Data models, tenant isolation, indexing, schema management, access control | 2026-09-30 |
| Pulsar — Synchronisation | Cross-device sync, CRDT-based conflict resolution, offline-first, MLS group encryption | 2026-12-31 |
| Comet — Portability | EU Data Act compliance, import/export, Solid Protocol interoperability | 2027-03-31 |
| Quasar — Services | API gateway, extension points for applications, service discovery | 2027-06-30 |
| Galaxy — Federation | Multi-node clustering, data sharding, failover, peer discovery | 2027-09-30 |
| Cosmos — Extension ecosystem | Wasm extension host (WASI 0.2), marketplace, Gaia-X and IDS interoperability | 2027-12-31 |
| Horizon — Data sovereignty | GDPR automation, data residency controls, audit trails, compliance certification | 2028-03-31 |

## Structure

This repository contains architecture decision records, data model specifications, and protocol specifications. Implementation repositories will be created as development begins.

## Licence

Architecture documents are licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Source code is dual-licensed under [LGPL 3.0](https://www.gnu.org/licenses/lgpl-3.0.html) and [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/).
