# Naamio Data Space — Architecture

Architecture decision records, data model specifications, and protocol specifications for [Naamio Data Space](https://naamio.dev).

Naamio Data Space is the private data store at the core of Naamio Space. It provides encrypted object storage, key-value persistence, and a dual extension model — Wasm components for storage-level extensions and gRPC for protocol plugins — enabling protocol support (Solid, WebDAV, CalDAV, JMAP, and others) without modifying the core.

## Structure

This repository contains architecture decision records, data model specifications, and protocol specifications. Implementation repositories will be created as development begins.

## Licence

Architecture documents are licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Source code is dual-licensed under [LGPL 3.0](https://www.gnu.org/licenses/lgpl-3.0.html) and [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/).
