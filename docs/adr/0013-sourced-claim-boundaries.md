# ADR-0013: Bound every external citation and refuse unsupported commercial claims

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

A hardware-plus-AI proposal can pick up vendor marketing, market-size numbers, or implied partnerships. The edition includes a dated source table instead.

## Decision

Keep a reviewed (2026-09-06) source table that supports only narrow statements:

- Taalas material is vendor-reported capability, not an AEGIS benchmark, procurement, compatibility proof, or partnership.
- Llama 3.1 uses its named Community License, not Apache-2.0; no weights or adapters are redistributed here.
- MCP security guidance does not make an MCP integration safe.
- The TSLIT paper is a related method with its own limits; no TSLIT result is an AEGIS result.

Do not assert market-size estimates, projected margins, commercial exclusivity, launch dates, competitor superiority, universal legal obligations, or deployment performance numbers. Future quantitative statements need a versioned source or a reproducible experiment with scope and limitations. Vendor announcements and other projects' results are background, not AEGIS validation.

No compliance certification, hardware containment guarantee, military endorsement, or proof of zero data leakage is claimed.

## Consequences

- Positive: The public proposal is harder to overread as a vendor deal or a validated product.
- Negative: The document cannot answer commercial or certification questions.

## Alternatives considered

- Cite vendor pages as if they validated AEGIS (rejected by the Limit column and `results/README.md`).
- Omit sources entirely (rejected in favor of `docs/SOURCES.md`).

## Evidence

- `docs/SOURCES.md`
- `docs/THREAT-MODEL.md` (closing claims paragraph)
- `NOTICE.md` (no sponsorship or partnership asserted)
- `RESEARCH.md` (Evidence)
- `c5a0cec70f5b9ed098c61fc333135bfeaa875fe4`
