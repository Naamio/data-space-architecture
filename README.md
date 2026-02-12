# Naamio Data Space — Architecture

Welcome! This repository is where architectural decisions for
[Naamio Data Space](https://naamio.dev) are proposed, discussed, and recorded.

## What is Naamio Data Space?

Naamio Data Space is an open source private data store built in Rust. It
provides encrypted object storage, key-value persistence, and a dual extension
model — Wasm components for storage-level extensions and gRPC for protocol
plugins — enabling protocol support (Solid, WebDAV, CalDAV, JMAP, and others)
without modifying the core. It runs as a single binary with zero-configuration
defaults, suitable for everything from a Raspberry Pi to a clustered deployment.

Data Space is the foundation of Naamio Space, the private data platform. The
name Naamio is Finnish for "mask" — the face you choose to present. A private
data store should give people and organisations sovereignty over their data.

## What this repository is for

This repository tracks architectural decisions using two complementary
approaches:

- **Architecture decision records (ADRs)** capture internal technical and
  organisational decisions — how Naamio Data Space is built, structured, and
  maintained.

- **Requests for comments (RFCs)** handle community-facing proposals — changes
  to public interfaces, features, behaviour, and integration patterns that
  affect how people use Naamio Data Space.

Both approaches are open to everyone. You don't need to be a maintainer or a
regular contributor to submit a proposal. If you have an idea or see something
that could be improved, you're welcome here.

## How the process works

1. **Create an issue** using one of the issue templates (ADR or RFC) to signal
   your intent and invite early feedback.
2. **Draft a proposal** using the document templates in `templates/`.
3. **Submit a merge request** with your proposal in `adrs/` or `rfcs/`.
4. **Discuss** — for ADRs, technical leads review over 7–14 days. For RFCs, the
   community discusses for a minimum of 14 days.
5. **Decision** — once consensus is reached, the proposal is merged and becomes
   part of the project's record.

The full process, including how consensus works, how disagreements are resolved,
and what happens with urgent decisions, is documented in the
[Omnifi Foundation handbook](https://handbook.omnifi.foundation/engineering/architecture/).

## Projects in scope

Proposals in this repository may affect any part of the Naamio Data Space
ecosystem:

**Storage**
- Encrypted object storage engine (S3-compatible API)
- Key-value store (prefix scanning, TTL, atomic operations)
- Storage abstraction layer and pluggable backends
- Single-binary deployment and zero-configuration defaults

**Structure**
- Data models and schema management
- Tenant isolation and access control
- Indexing and query capabilities
- Configuration loading and validation

**Synchronisation**
- Cross-device sync protocol
- CRDT-based conflict resolution
- Offline-first operation
- MLS group encryption (RFC 9420)

**Portability**
- EU Data Act compliance
- Import/export and data migration
- Solid Protocol interoperability
- Standard data format support

**Services**
- gRPC service interface for protocol plugins and extensions
- Event system (CloudEvents specification)
- API gateway and service discovery
- Protocol plugin registration and request dispatch

**Federation**
- Multi-node clustering and data sharding
- Failover and replication
- Peer discovery
- Tenant isolation across nodes

**Extensions**
- Wasm extension host (WASI 0.2 component model)
- Host-provided primitives (RDF processing, XML handling, iCalendar parsing)
- Storage-level extensions (validators, transformers, indexers)
- Protocol plugins via gRPC (Solid, WebDAV, CalDAV, JMAP, and others)
- Shared Wasmtime instance available to gRPC plugins for sub-extensibility

**Sovereignty**
- GDPR automation and data residency controls
- Audit trails and compliance certification
- Supply chain security

If your proposal spans multiple areas, note all affected projects in your
proposal so the right people can weigh in.

## Governance

Naamio Data Space is governed by the
[Omnifi Foundation](https://omnifi.foundation), a community-driven organisation
that stewards open source projects. The architecture decision process — how
proposals are written, reviewed, and decided — is defined in the
[Omnifi Foundation handbook](https://handbook.omnifi.foundation/engineering/architecture/)
and applies equally to all contributors.

Decisions are made through consensus. Technical leads facilitate the process but
don't dictate outcomes. Every voice carries weight, and dissenting perspectives
are documented and valued. See the
[governance model](https://handbook.omnifi.foundation/engineering/architecture/governance/)
for full details.

## Getting started

New to the project? Here's how to get oriented:

1. **Browse existing proposals** in `adrs/` and `rfcs/` to see what's been
   decided and how proposals are structured.
2. **Check open merge requests** for proposals currently under discussion.
3. **Read the handbook** for
   [detailed process guidance](https://handbook.omnifi.foundation/engineering/architecture/).
4. **Open an issue** if you have questions — there are no bad questions.

## Repository structure

```
├── README.md              You are here
├── CONTRIBUTING.md        How to submit proposals
├── templates/
│   ├── adr.md             Architecture decision record template
│   └── rfc.md             Request for comments template
├── adrs/                  Accepted architecture decision records
├── rfcs/                  Accepted requests for comments
└── .gitlab/
    └── issue_templates/
        ├── adr.md         Issue template for starting an ADR
        └── rfc.md         Issue template for starting an RFC
```

## Code of conduct

All participation is subject to the
[Omnifi Foundation code of conduct](https://handbook.omnifi.foundation/CODE_OF_CONDUCT/).
We're committed to a welcoming, respectful, and inclusive environment.

## Licence

CC BY-SA 4.0 — see LICENCE for details.
