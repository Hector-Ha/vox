# Product Pseudocode

This document describes Vox behavior at a product level. It is intentionally non-executable and omits production architecture, providers, storage, security controls, and operational details.

## Request context

```text
function requestContext(publicPost, requester):
    require verified(requester)

    snapshot = captureBoundedPost(publicPost)
    if snapshot is missing and publicPost.link is missing:
        return InaccessiblePost

    existingNote = findFittingGovernedNote(snapshot or publicPost.link)
    if existingNote exists:
        attach(existingNote, publicPost)
        return existingNote

    startDurableDrafting(snapshot or publicPost.link)
    return DraftingStarted
```

## Draft a note

```text
function draftContext(request):
    contextTarget = AI.identifyUsefulContext(request.post)

    if contextTarget says context would not help:
        return NoNoteNeeded

    sources = AI.discoverAndAssessSources(contextTarget)
    if sources cannot responsibly support a note:
        return NotEnoughContext

    draft = AI.writeConciseSourcedNote(contextTarget, sources)
    if draft fails sourcing, neutrality, safety, or fit checks:
        return no public note

    publish draft as "AI-assisted context awaiting community review"
    return AIPublicDraftNote
```

## Rate and approve

```text
function rateNote(noteApplication, user, rating):
    require verified(user)
    replace user's prior rating on this note application
    update application fit signal
    update note's Community Approval Score

    if note is Draft
       and Bridging Consensus is reached
       and no hard blocker is active:
        set note status to Community Approved
```

## Establish a note

```text
function reviewStability(note):
    if note stayed Community Approved for required period
       and approval support remains strong
       and no serious report is unresolved:
        set note status to Established
```

## Reuse trusted context

```text
function considerReuse(governedNote, candidatePost):
    fit = AI.assessMeaningScopeTimeframeAndEntities(governedNote, candidatePost)

    if fit is exact enough for responsible reuse:
        attach governedNote to candidatePost
    else:
        do not reuse
```

## Correct governed context

```text
function proposeCorrection(governedNote, replacement):
    preserve current public version
    collect fresh Ratings on replacement

    if replacement reaches Bridging Consensus:
        replace current version
    else:
        keep current version
```
