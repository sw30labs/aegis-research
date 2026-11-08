# ADR-0012: Keep this edition all-rights-reserved and treat AEGIS as a working name

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

Public GitHub repos often imply an open-source license. This tree is a research text edition, not a software product, and the name AEGIS is not cleared as a mark.

## Decision

Copyright © 2026 Nicolas Cravino; all rights reserved. No open-source software license or open-content license is granted by `NOTICE.md`. The hosting platform's terms and applicable law remain. There is no contribution license yet; `CONTRIBUTING.md` asks for feedback on assumptions, sources, or smaller experiments, using synthetic reproductions only, and says to discuss reuse with the author first.

AEGIS is a working research name, not a representation of trademark clearance or a commercially available product. Future code, hardware, and model releases require their own explicit licensing decisions. No third-party code, model weights, datasets, proprietary chip designs, customer records, or partner materials are distributed in this edition.

## Consequences

- Positive: Readers are not granted rights the author has not decided to give; later implementations can choose a different license.
- Negative: Collaboration is limited until a contribution license exists; downstream reuse needs an explicit request.

## Alternatives considered

- Add an SPDX/open-source LICENSE (not present; NOTICE.md is explicit that none is granted).
- Present AEGIS as a cleared product name (rejected by NOTICE.md).

## Evidence

- `NOTICE.md`
- `CONTRIBUTING.md`
- `README.md` (final paragraph)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
