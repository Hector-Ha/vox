# vox

**The story behind the post.**

vox is an independent context layer for public online conversations. It is designed for the moment when a post is easy to react to but hard to understand. vox gathers the relevant public record, separates evidence from reaction, and turns the result into a concise Story that can be read where the conversation is happening.

The goal is not to declare a winner. The goal is to help a reader answer better questions:

- What happened?
- What is known, and what remains uncertain?
- Why do reasonable people read the situation differently?
- Which claims have support?
- What can the available public reaction tell us, and what can it not tell us?

## What this repository contains

This repository is a public product brief. It explains the problem, the product model, the reader experience, and the principles behind vox.

It does not disclose source code, technology choices, system architecture, vendors, security controls, private research, internal links, delivery status, or the roadmap. Nothing here should be read as a launch announcement or a claim about current availability.

Public documentation boundary decision date: 2026-09-21.

- [Product brief](docs/product-brief.md)
- [How vox works](docs/how-vox-works.md)
- [Design approach](docs/design-approach.md)
- [Trust model](docs/governance.md)
- [Privacy and safety](docs/privacy-and-safety.md)

## The problem

Online situations rarely stay in one place. A claim begins in a video, gets reframed in a post, draws reactions across several communities, and picks up details that may be true, disputed, outdated, or impossible to verify.

Readers are left to reconstruct the situation themselves. Search can find pages. Social feeds can show momentum. A fact check may settle one narrow claim. None of those tools reliably explains the whole situation, the evidence behind it, and the reasons people disagree.

vox is designed to fill that gap.

Purpose and scope decision date: 2026-08-28.

## The product idea

A reader can ask vox for context on a public post. vox builds or finds a Story about the underlying situation. A Story may include:

- a neutral account of what happened;
- the central question or disagreement;
- the strongest supported perspectives and their reasons;
- a timeline when sequence matters;
- direct material, independent context, public reaction, and background references;
- a careful account of what appeared in the public material vox examined; and
- a record of meaningful corrections or updates.

Each part appears only when the available material supports it. vox can explain a situation without forcing every Story into a true-or-false verdict, a two-sided debate, or a popularity contest.

Story model decision date: 2026-08-28. Perspective presentation refinement date: 2026-08-29.

## What makes vox different

### Context follows the conversation

A useful explanation should meet the reader near the post that created the question. vox is designed to connect related public posts to the same Story when they concern the same continuing situation. It keeps merely similar or adjacent situations separate.

Story matching decision date: 2026-08-28.

### Evidence and opinion keep different jobs

Participant statements, independent reporting, public reaction, and historical background can all matter. They do not prove the same things. vox labels their roles and does not treat popularity as evidence.

Evidence-role decision date: 2026-08-28.

### Public reaction stays bounded

The internet is not a representative poll. vox describes only the material it could retrieve and assess. It does not turn a partial sample into a claim about an entire platform, region, or public.

Bounded-reaction decision date: 2026-08-28.

### Complexity is allowed

Some disagreements fit on a clear spectrum. Others do not. vox can present several named perspectives, conditional views, or unresolved questions without inventing a false middle or forcing binary sides.

Perspective-model decision date: 2026-08-29.

### Updates do not erase history

Online situations change. vox is designed to revise a Story when the public record changes while preserving the distinction between an update and a correction. Failed or incomplete rechecks do not replace a supported Story.

Update and correction direction decision date: 2026-08-28.

## The product principle

> AI can help gather, compare, and explain public material. It cannot make missing evidence appear, convert a convenience sample into public opinion, or erase uncertainty.

AI and evidence boundary decision date: 2026-08-28.

## A deliberate public boundary

This repository publishes the product reasoning that can be understood and challenged without exposing confidential machinery or records.

That boundary is intentional. A serious product should be able to explain what it is for before it explains how it is built.
