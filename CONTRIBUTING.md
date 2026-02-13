# Contributing to Naamio Data Space Architecture

Thank you for your interest in shaping Naamio Data Space's architecture. This
guide explains how to submit proposals — whether you're proposing a new
technical direction, suggesting changes to how the project operates, or
advocating for changes to community-facing interfaces.

## Before you begin

- **Check existing proposals.** Browse `decisions/` and `comments/` to see what's already
  been decided. Your idea may build on or conflict with earlier decisions.
- **Check open merge requests.** Someone else may already be working on a
  similar proposal.
- **Open an issue first.** Use the issue templates to signal your intent and
  get early feedback before investing time in a full proposal.


## Understanding the terminology

This repository uses accessible folder names that map to well-established
software engineering practices:

| Folder | Purpose | Also known as |
|--------|---------|---------------|
| `decisions/` | Recorded architectural and technical choices | Architecture decision records (ADRs) |
| `comments/` | Proposals and discussion for community-facing changes | Requests for comments (RFCs) |

The purpose is identical to traditional ADRs and RFCs — we use plainer language
to lower the barrier to contribution.

## Choosing the right proposal type

### Decisions

Use a decision when you're proposing an **internal technical or organisational
decision**. Decisions cover how Naamio Data Space is built, structured, and
maintained.

Examples:
- Choosing a storage backend implementation
- Adopting an encryption scheme for at-rest data
- Defining the Wasm extension host capability model
- Structuring the gRPC protocol plugin interface

Decisions use **lazy consensus** — they are accepted unless someone objects within the
review period (typically 7–14 days). Technical leads facilitate the process.

### Comments

Use a comment when you're proposing a **community-facing change**. Comments cover
interfaces, behaviours, and capabilities that directly affect how people
interact with Naamio Data Space.

Examples:
- Changing the S3-compatible storage API
- Adding a new protocol plugin interface
- Modifying the event system contract
- Changing how tenant isolation works

Comments require **active consensus** — they need explicit agreement from the
community. The discussion period is a minimum of 14 days.

## Proposal workflow

### 1. Open an issue

Use the appropriate issue template:
- **Decision**: for internal technical and organisational choices
- **Comment**: for community-facing changes

### 2. Draft your proposal

Use the templates in `templates/`:
- `templates/decision.md` for architecture decisions
- `templates/comment.md` for community-facing proposals

### 3. File naming

**ADRs**: `decisions/XXXX-short-descriptive-title.md`

**RFCs**: `comments/XXXX-short-descriptive-title.md`

Numbers are sequential. Check existing files to determine the next available
number.

### 4. Branch naming

- Decisions: `proposal/decision-XXXX-short-title`
- Comments: `proposal/comment-XXXX-short-title`

### 5. Submit a merge request

Push your branch and open a merge request. The merge request description should
summarise the proposal and link to the tracking issue.

### 6. Discussion and decision

- **Decisions**: Technical leads review. Lazy consensus applies — accepted unless
  objected to within the review period.
- **Comments**: Open community discussion for a minimum of 14 days. Active consensus
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
