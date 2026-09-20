# AutoCull

**Keep the moment. Lose the repetition. Keep your photographs private.**

AutoCull is an offline, local-first photo review system for Lightroom Classic.
It is being built to reduce repetitive burst frames, surface the photographs
worth processing or publishing, and preserve meaningful alternatives without
uploading a catalog to a cloud service.

## Why AutoCull exists

High-speed shooting solves one problem and creates another: hundreds of frames
can differ by a wing position, expression, gesture, focus miss, or fraction of
a second. Traditional duplicate finders see similar pixels. Photographers need
a review system that can distinguish redundant frames from meaningful moments.

AutoCull separates three concerns:

- **Technical evidence:** subject localization, focus signals, exposure context,
  and explicit failures
- **Photographic interpretation:** composition, timing, behavior, and artistic
  value
- **Personal preference:** modest ranking adjustments that reflect what the
  photographer values without rewriting technical truth

## Design principles

- **Local first:** photographs and inference remain on the photographer's Mac.
- **Non-destructive:** source files are never moved or modified.
- **Auditable:** every stage records its evidence, status, and decision.
- **Scene aware:** landscapes, night skies, moon, aurora, and environmental
  images are valid photographs, not failed object detections.
- **Conservative:** ambiguous evidence is preserved and reported instead of
  silently guessed.
- **Photographer controlled:** duplicate reduction, quality judgment, and taste
  remain separate decisions.

## The workflows

| Workflow | Purpose |
| --- | --- |
| **No Clown Car** | Deterministic, VLM-free cleanup of obvious duplicate frames in large catalogs |
| **Shoot Debrief** | Technical and artistic review of a fresh, burst-heavy import |
| **Curtain Call** | Non-destructive ranking and enrichment of an already curated set before publication |

## Current status

AutoCull is under active private development. The Swift engine, Lightroom
Classic bridge, local vision pipeline, evaluation harness, and task-specific
model-training projects are not yet offered as a supported public release.

Current work is focused on validating conservative duplicate decisions and
training a local visible-eye detector before eye evidence is allowed to affect
ranking. Public code, demonstrations, installation instructions, and a
contribution process will be published only when they are accurate enough to be
useful.

## What success looks like

AutoCull should help a photographer reach a smaller, stronger, explainable set
of images while remaining free to disagree. It is a review assistant, not an
automatic judge of photographic worth.

For project inquiries, contact
[dancingyakcreative@gmail.com](mailto:dancingyakcreative@gmail.com).
