# Contributing to Naamio Data Space Architecture

Thank you for your interest in shaping Naamio Data Space's architecture. This
guide explains how to submit proposals — whether you're proposing a new
technical direction, suggesting changes to how the project operates, or
advocating for changes to community-facing interfaces.

## Before you begin

- **Check existing proposals.** Browse `adrs/` and `rfcs/` to see what's already
  been decided. Your idea may build on or conflict with earlier decisions.
- **Check open merge requests.** Someone else may already be working on a
  similar proposal.
- **Open an issue first.** Use the issue templates to signal your intent and
  get early feedback before investing time in a full proposal.

## Choosing the right proposal type

### Architecture decision records (ADRs)

Use an ADR when you're proposing an **internal technical or organisational
decision**. ADRs cover how Naamio Data Space is built, structured, and
maintained.

Examples:
- Choosing a storage backend implementation
- Adopting an encryption scheme for at-rest data
- Defining the Wasm extension host capability model
- Structuring the gRPC protocol plugin interface

ADRs use **lazy consensus** — they are accepted unless someone objects within the
review period (typically 7–14 days). Technical leads facilitate the process.

### Requests for comments (RFCs)

Use an RFC when you're proposing a **community-facing change**. RFCs cover
interfaces, behaviours, and capabilities that directly affect how people
interact with Naamio Data Space.

Examples:
- Changing the S3-compatible storage API
- Adding a new protocol plugin interface
- Modifying the event system contract
- Changing how tenant isolation works

RFCs require **active consensus** — they need explicit agreement from the
community. The discussion period is a minimum of 14 days.

## Proposal workflow

### 1. Open an issue

Use the appropriate issue template:
- **ADR**: for internal technical and organisational decisions
- **RFC**: for community-facing changes

### 2. Draft your proposal

Use the templates in `templates/`:
- `templates/adr.md` for architecture decision records
- `templates/rfc.md` for requests for comments

### 3. File naming

**ADRs**: `adrs/XXXX-short-descriptive-title.md`

**RFCs**: `rfcs/XXXX-short-descriptive-title.md`

Numbers are sequential. Check existing files to determine the next available
number.

### 4. Branch naming

- ADRs: `proposal/adr-XXXX-short-title`
- RFCs: `proposal/rfc-XXXX-short-title`

### 5. Submit a merge request

Push your branch and open a merge request. The merge request description should
summarise the proposal and link to the tracking issue.

### 6. Discussion and decision

- **ADRs**: Technical leads review. Lazy consensus applies — accepted unless
  objected to within the review period.
- **RFCs**: Open community discussion for a minimum of 14 days. Active consensus
  required.

## Style guidelines

- Write clearly and concisely.
- Use British English spelling conventions (organisation, behaviour, colour).
- Avoid unexpanded acronyms on first use.
- Prefer concrete examples over abstract descriptions.
- Use human-centric language — "developers", "operators", "people" rather than
  "users".

## Questions?

Open an issue. There are no bad questions.

## Governance

All proposals follow the
[Omnifi Foundation governance model](https://handbook.omnifi.foundation/engineering/architecture/governance/).
The full process is documented in the
[handbook](https://handbook.omnifi.foundation/engineering/architecture/).
