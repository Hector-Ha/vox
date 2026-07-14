# How Vox Works

Vox adds sourced context beside public posts on Reddit, Facebook, X, and Threads. It separates fast AI assistance from public trust.

## Reader flow

1. A reader requests context beside a public post.
2. Vox captures a bounded snapshot of that post without collecting replies, social graphs, or browsing history.
3. Vox checks whether an existing Governed Note fits the post.
4. If no Governed Note fits, AI identifies useful sourceable context and assesses supporting sources.
5. Strong evidence produces an AI Public Draft Note. Weak or unnecessary evidence produces a clear non-note outcome.
6. Verified users and contributors rate the note.
7. Bridging Consensus can upgrade the note to Community Approved.
8. A stable Community Approved Note can become Established.

## Trust order

Vox always prefers the strongest fitting context:

```text
Established Note
  > Community Approved Note
  > AI Public Draft Note
  > No note
```

AI Public Draft Notes never override Governed Notes. A note is reused only when its meaning, scope, entities, and timeframe fit the new post.

## Request outcomes

Every request ends in a specific state:

| Outcome | Reader meaning |
| --- | --- |
| AI Public Draft Note | Useful sourced context is available and awaiting community review. |
| No Note Needed | Added context would not help readers. |
| Not Enough Context | Available evidence cannot support a responsible note. |
| Inaccessible Post | Vox cannot safely read enough of the post. |
| Provider Unavailable | Required research service could not return a trustworthy result. |
| Hard Blocked | Safety or product rules prevent publication. |

Failed or partial work never creates a public note.

## Context beyond fact-checking

Vox notes can clarify timelines, definitions, primary evidence, missing background, or other sourceable context. A post does not need to be a simple factual claim. Opinions, jokes, questions, and reactions may receive context when that context materially helps readers.

## Cross-platform context

Claims often move between platforms. Vox can reuse a Governed Note across matching public posts while keeping every attachment separately rated for fit. Loose topic similarity is not enough.
