# Vox

**Useful context wherever the conversation moves.**

## Welcome to Vox's public repository

Vox is a cross-platform reader context layer for Reddit, Facebook, X, and Threads. It adds concise, sourced context directly beside public posts, then gives people—not AI—the authority to decide what earns lasting public trust.

This repository is the public home for Vox's product model, governance rules, research, and program updates. It explains how Vox works without exposing private production systems, security controls, credentials, or proprietary implementation details.

> [!IMPORTANT]
> AI can draft context. Only people can approve it. Every note clearly shows whether it is an AI-assisted draft, Community Approved, or Established.

Public documentation:

- [How Vox Works](docs/how-vox-works.md)
- [Community Governance](docs/governance.md)
- [Privacy and Safety](docs/privacy-and-safety.md)
- [Product Pseudocode](docs/pseudocode.md)

## About Vox

Important context should not stop at one platform's border or arrive only after a misleading post has already traveled.

Vox combines fast AI-assisted research with community governance. Readers can request context from the post they are viewing. Vox identifies the claim or context that matters, finds credible sources, and publishes a short AI Public Draft Note when useful context is available. The community then rates the note for helpfulness, sourcing, neutrality, and fit.

Notes that earn Bridging Consensus become Public Community Approved Notes. Notes that remain useful and stable over time become Public Established Notes. Approved context can be reused when the same claim appears again, while conservative matching prevents a note from being attached where its meaning does not fit.

Vox is built around one principle:

> **AI operates the default workflow. Humans govern public trust. Bridging Consensus upgrades Note Status.**

## How it works

1. **Request context** — Select **Request AI Note** beside a public post.
2. **Research begins** — Vox captures only the bounded post content needed for the request and checks whether trusted context already exists.
3. **Sources are assessed** — AI discovers and evaluates sources relevant to the post's claim or broader context.
4. **Context appears inline** — When the evidence is strong enough, Vox publishes a concise, sourced AI Public Draft Note beside the post.
5. **People rate the note** — Verified users and contributors choose **Helpful**, **Somewhat Helpful**, or **Not Helpful**.
6. **Consensus upgrades trust** — Notes that earn sufficient community support without active safety blockers become Community Approved.
7. **Stable context travels** — Governed Notes can help readers wherever the same claim appears, without allowing loose or misleading matches.

Drafting continues safely even if the reader closes the page. The extension shows honest progress states, preserves unresolved requests in the request center, and can send an optional completion notification. Drafting normally finishes well within its five-minute target; slower work remains durable instead of being abandoned.

## Why Vox is different

### Context across platforms

Online claims move between networks. Vox supports Reddit, Facebook, X, and Threads through one independent trust layer, so useful context is not trapped inside the platform where it was first written.

### Useful context, not verdicts

Vox does more than label posts true or false. A note can add timelines, definitions, primary evidence, missing background, or other sourceable context that helps a reader understand what they are seeing. Opinions, jokes, questions, and reactions are eligible when credible context would still be useful.

### AI speed, human authority

AI Public Draft Notes can help readers immediately, but they never present themselves as community-approved. AI cannot promote its own work. Public trust comes only from Community Governance.

### Consensus, not popularity

Vox does not treat a simple majority as truth. Bridging Consensus combines authenticated ratings, contributor track records, revision signals, and safety checks. Strong disagreement keeps a draft under review instead of forcing premature approval.

### Stable notes, careful corrections

Drafts can be revised when contributors identify a concrete problem. Ratings reset when meaning changes, so a new version cannot inherit trust it has not earned. Approved and Established Notes require a governed Correction Proposal before a meaning-changing replacement.

### Sources readers can inspect

Every public note links to the sources supporting its claims. Vox prefers strong, relevant sources and publishes nothing when the available evidence cannot support useful context.

## Note states

| State | Meaning |
| --- | --- |
| **AI Public Draft** | Sourced, AI-assisted context shown publicly while awaiting community review. |
| **Community Approved** | A public note that has earned Bridging Consensus and has no active hard blocker. |
| **Established** | A Community Approved Note that has remained stable, useful, and free of unresolved serious reports. |

Governed Note Precedence keeps the strongest available context in view:

```text
Established Note
  > Community Approved Note
  > AI Public Draft Note
  > No note
```

## Honest outcomes

Vox does not force a note onto every post. A request can end with:

- **AI Public Draft Note** when useful context is well supported.
- **No Note Needed** when added context would not help readers.
- **Not Enough Context** when available evidence cannot support a responsible note.
- **Inaccessible Post** when the post cannot be read safely from the captured snapshot or public link.
- **Provider Unavailable** when required research services cannot return a trustworthy result.
- **Hard Blocked** when safety or product rules prevent publication.

Failed, incomplete, or partially generated work never becomes a public note.

## Community Governance

Anyone can read public notes. Verified users can request and rate context. Contributors earn greater governance responsibility through useful participation, while moderators handle abuse, privacy, legal, safety, spam, manipulation, and broken sourcing.

Moderators do not decide ordinary factual disputes. Disagreement belongs in Ratings and governed correction flows. System-wide quality safeguards can pause new AI Public Draft Notes while established community context remains available.

## Privacy by design

Vox collects only what is needed to provide and govern reader context.

- No comments or replies are collected.
- No friend, follower, or platform social-graph data is collected.
- No full profile history or browsing history is collected.
- Post Snapshots are bounded to the public post content needed for the request.
- Notification access is optional and off by default.
- Private account data can be deleted without silently erasing retained public governance history.
- Retained ratings are anonymized when an account is deleted.
- Public Notes retain only reader-facing citations and the bounded evidence required to support them.

## Built for reliability

Vox keeps requests safe through page closes, browser restarts, temporary service interruptions, and duplicate delivery attempts. Completed research is checkpointed, recoverable work retries automatically, and incomplete output is never published. Users see specific outcomes instead of generic failure messages.

Protected operations, audited recovery controls, bounded diagnostic retention, and end-to-end redaction keep the service observable without exposing private user data, credentials, hidden reasoning, or raw research packets.

## Transparency

Vox is committed to making its public rules understandable. This repository documents:

- the language used for Notes and governance;
- the difference between AI-assisted and community-approved context;
- the conditions that upgrade, revise, hide, or restore a Note;
- the safeguards used to limit abuse and misleading reuse;
- the research that informs Vox's approach; and
- material changes to public product behavior.

Vox learns from public work on collaborative context systems, including [X Community Notes](https://github.com/twitter/communitynotes), while remaining an independent cross-platform product. Vox is not affiliated with or endorsed by Reddit, Meta, X, or their subsidiaries.

## Product scope

Vox is live on:

- Reddit
- Facebook
- X
- Threads

The browser extension provides inline requests, inline notes, ratings, account access, request history, unresolved rating tasks, platform controls, themes, and optional completion alerts. The Vox website provides account recovery, product guidance, privacy information, and secure account management.
