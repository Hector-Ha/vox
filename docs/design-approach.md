<div align="center">

<h1>Design approach</h1>

<strong>Start with reader uncertainty. Test the cases that make easy answers misleading.</strong>

<br>
<br>

<sub>READER QUESTIONS &nbsp;·&nbsp; MATERIAL ROLES &nbsp;·&nbsp; HARD CASES &nbsp;·&nbsp; PUBLIC LANGUAGE</sub>

</div>

<p align="center"><a href="../README.md">Overview</a> &nbsp;·&nbsp; <a href="product-brief.md">Product brief</a> &nbsp;·&nbsp; <a href="how-vox-works.md">Method</a> &nbsp;·&nbsp; <a href="product-boundaries.md">Boundaries</a></p>

---

vox began with a product question, not a feature list: what would a reader need to understand a confusing online situation without leaving the conversation and reconstructing it alone?

<table>
  <tr>
    <td width="25%" valign="top"><strong>Start with uncertainty</strong><br><br>Name what the reader does not know before proposing a feature.</td>
    <td width="25%" valign="top"><strong>Separate the roles</strong><br><br>Facts, reactions, and background must not blur into one claim.</td>
    <td width="25%" valign="top"><strong>Test the awkward cases</strong><br><br>Edge cases show where a tidy presentation would mislead.</td>
    <td width="25%" valign="top"><strong>Keep claims bounded</strong><br><br>Public language should say only what the material can support.</td>
  </tr>
</table>

This document explains how the product direction was developed. It omits implementation details, internal artifacts, vendors, architecture, delivery records, and development status.

## Start with the reader's uncertainty

The early product model focused on narrow contextual notes. That model clarified several useful trust and evidence ideas, but it could not fully answer the reader's broader questions about sequence, participants, competing interpretations, and visible public reaction.

The design work returned to the reader problem and adopted the Story as the primary unit of explanation.

## Separate the jobs inside one explanation

The product model separates facts, participant statements, independent context, public reaction, and historical background. It also separates evidence strength, visible support, and current momentum.

This separation prevents a common failure in online summaries. A source can be relevant without proving a claim. A reaction can be popular without being representative. A participant can be authoritative about what they said without being authoritative about what happened.

## Prototype the hard judgments

The design process used focused prototypes to test questions that prose alone left fuzzy. Examples included how to present a multi-position disagreement, how much detail belongs in the first view, how readers move between a post and a full Story, and how private reader input could inform later analysis without being presented as a public comment.

Those prototypes were decision tools. They tested language, information order, state transitions, and awkward cases. They were not treated as proof that a production system existed.

## Design for cases that resist simplification

The product direction was tested against cases where the obvious presentation would mislead:

- a disagreement with more than two coherent positions;
- a large reaction count drawn from a narrow or personalized sample;
- a participant statement that is important but unverified;
- several posts that share names and keywords but concern different events;
- new material that changes one section without invalidating the whole Story;
- a failed update attempt that should not erase supported context; and
- a contribution that informs a perspective but cannot serve as factual evidence.

Handling these cases early shaped the product more than designing the happy path alone.

## Keep uncertainty visible

The product does not treat uncertainty as a copy problem to be edited away. Uncertainty changes what vox can publish, which sections appear, how confidently a relationship can be described, and whether a count should be shown at all.

## Use public language that survives scrutiny

The design avoids claims that exceed the material. It prefers "among the reactions vox retrieved" to "people believe." It distinguishes a correction from an update. It says when a section is unavailable instead of filling the space with weak inference.

## Keep product truth separate from project status

A product brief should explain the intended reader value without using prototypes, tests, internal decisions, or planned work as evidence of availability. The public repository therefore records the product idea and its reasoning while remaining silent about implementation and delivery.
