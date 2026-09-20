<p align="center">
  <img src="assets/brand/autocull-avatar.jpg" width="180" alt="AutoCull logo: a glowing stack of photographs">
</p>

<h1 align="center">AutoCull</h1>

<p align="center"><strong>Keep the moment. Lose the repetition. Keep your photographs private.</strong></p>

AutoCull is an offline, local-first photo review system for Lightroom Classic.
It is being built to reduce repetitive burst frames, surface the photographs
worth processing or publishing, and preserve meaningful alternatives without
uploading a catalog to a cloud service.

## Why AutoCull exists

High-speed shooting solves one problem and creates another: hundreds of frames
can differ by a wing position, expression, gesture, focus miss, or fraction of
a second. Traditional duplicate finders see similar pixels. Photographers need
a review system that can distinguish redundant frames from meaningful moments.

This problem reaches beyond any one genre. Wildlife and bird photographers,
sports shooters, wedding photographers, and event photographers all work with
large sequences where the best frame may differ from its neighbors by one
expression, gesture, wing position, or point of focus. AutoCull is being built
for those burst-heavy workflows while remaining useful for landscapes, night
skies, and other scene-oriented photography.

AutoCull separates three concerns:

- **Technical evidence:** subject localization, focus signals, exposure context,
  and explicit failures
- **Photographic interpretation:** composition, timing, behavior, and artistic
  value
- **Personal preference:** modest ranking adjustments that reflect what the
  photographer values without rewriting technical truth

## What makes AutoCull different

- **Local first:** photographs and inference remain on the photographer's Mac,
  avoiding catalog uploads and cloud-processing dependencies.
- **Non-destructive Lightroom integration:** source files are never moved or
  modified. Structured audit output and catalog writeback remain separate from
  the original photographs.
- **Explainable evidence:** subject localization, crop evidence, technical
  signals, model output, and final decisions are recorded for review.
- **Conservative duplicate handling:** duplicate reduction is separate from
  photographic quality judgment. Ambiguous frames are preserved rather than
  silently discarded.
- **Scene aware:** landscapes, night skies, moon, aurora, and environmental
  images are valid photographs, not failed object detections.
- **Deterministic and interpretive layers:** measurable technical evidence is
  kept distinct from local vision-model interpretation.
- **Photographer controlled:** configurable preferences can influence ordering
  without rewriting the recorded technical or artistic evidence.

## The workflows

| Workflow | Purpose |
| --- | --- |
| **No Clown Car** | Deterministic, VLM-free cleanup of obvious duplicate frames in large catalogs |
| **Shoot Debrief** | Technical and artistic review of a fresh, burst-heavy import |
| **Curtain Call** | Non-destructive ranking and enrichment of an already curated set before publication |

## Specialized local models

AutoCull is beginning with a small visible-eye detector trained on animal
photography. Its job is deliberately narrow: locate a visibly resolvable eye
and report confidence. It does not decide whether a photograph should be kept
or culled.

After eye localization is validated, deterministic eye-focus measurements will
be compared with human choices from real bursts. A separate small ranking model
will be trained only if those measurements prove insufficient.

Longer-term model work may address wildlife subject localization, scene
routing, or same-beat recognition. Each model must own one clear task and
demonstrate a measurable pipeline improvement before entering production.

## Current status

AutoCull is under active private development. The Swift engine, Lightroom
Classic bridge, local vision pipeline, evaluation harness, and task-specific
model-training projects are not yet offered as a supported public release.

Current work is focused on validating conservative duplicate decisions and
training a local visible-eye detector before eye evidence is allowed to affect
ranking. Public code, demonstrations, installation instructions, and a
contribution process will be published only when they are accurate enough to be
useful.

No public model weights or supported installer are available yet. AutoCull will
not present experimental outputs as production-ready decisions.

## What success looks like

AutoCull should help a photographer reach a smaller, stronger, explainable set
of images while remaining free to disagree. It is a review assistant, not an
automatic judge of photographic worth.

> **A private, conservative, auditable photography assistant that understands
> the difference between repetition and a different moment.**

For project inquiries, contact
[dancingyakcreative@gmail.com](mailto:dancingyakcreative@gmail.com).
