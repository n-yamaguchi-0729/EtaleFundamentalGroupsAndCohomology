# EtaleFundamentalGroupsAndCohomology (Lean 4.35.0-rc2)

[![Lean](https://github.com/n-yamaguchi-0729/EtaleFundamentalGroupsAndCohomology/actions/workflows/lean.yml/badge.svg)](https://github.com/n-yamaguchi-0729/EtaleFundamentalGroupsAndCohomology/actions/workflows/lean.yml)
[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

Lean libraries for étale fundamental groups and étale cohomology, extracted
from [NYLL](https://github.com/n-yamaguchi-0729/NYLL).

## Goal and coverage

The goal is a **complete formalization** of the corresponding Stacks Project material:

- **EFG:** [Chapter 58 — Fundamental Groups of Schemes](https://stacks.math.columbia.edu/tag/0BQ6).
- **Étale cohomology:** [Chapter 59](https://stacks.math.columbia.edu/tag/03N1), [Chapter 63 — More Étale Cohomology](https://stacks.math.columbia.edu/tag/0F4U), and [Chapter 64 — The Trace Formula](https://stacks.math.columbia.edu/tag/0F5P), including the Grothendieck–Lefschetz trace formula and its consequences.

All these chapters remain in progress. The tables below describe the
**published source**, audited on 2026-10-13. Completed coverage includes
upstream definitions and results; restricted cases are labelled separately.
Chapter 58 numbering follows revision `ed88ff78`; tags provide stable references.

### Chapter 58: formalized numbered items

| Items | Content |
| --- | --- |
| 58.2.1–3 | Étale schemes over fields and continuous Galois actions ([03QR](https://stacks.math.columbia.edu/tag/03QR)). |
| 58.3.1–11 | Galois categories, profinite completion, fiber functors and exact functors ([0BN5](https://stacks.math.columbia.edu/tag/0BN5)). |
| 58.4.1–5 | Criteria for surjectivity, injectivity, normality and exactness. |
| 58.5.1–5 | Finite étale Galois categories and internal Hom ([0BL7](https://stacks.math.columbia.edu/tag/0BL7)). |
| 58.6.1–4 | Fundamental groups, finite actions and change of base point ([0BNE](https://stacks.math.columbia.edu/tag/0BNE)). |
| 58.8.1–4 | Henselian pairs, thickenings and universal homeomorphisms ([0BQN](https://stacks.math.columbia.edu/tag/0BQN)). |
| 58.10.1–5, 7 | Dense pullback and geometrically unibranch schemes ([0BQI](https://stacks.math.columbia.edu/tag/0BQI)). |
| 58.11.1–4 | Normalization and the normal-local fundamental-group sequence ([0BQM](https://stacks.math.columbia.edu/tag/0BQM)). |
| 58.12.1–5 | Residue fields, strict henselianity, inertia invariants and filtered étale colimits ([0BSU](https://stacks.math.columbia.edu/tag/0BSU)). |
| 58.13.1–2, 4–6 | Decomposition, inertia, unramifiedness and tame/wild inertia ([0BUA](https://stacks.math.columbia.edu/tag/0BUA)). |
| 58.14.1–3 | Inverse limits, perfection and the arithmetic exact sequence ([0BTX](https://stacks.math.columbia.edu/tag/0BTX)). |
| 58.15.1–2 | Finite étale Stein factor and the proper homotopy exact sequence. |
| 58.17.5 | Faithfulness when a closed subscheme meets every connected component. |
| 58.19.2 | Faithfulness of punctured hypersurface restriction. |
| 58.20.2 | Extension criterion using the actual global-sections algebra. |
| 58.21.1, 6 | Height-one boundary primes and local-to-global purity. |
| 58.22.1 | Faithfulness near a punctured hypersurface, including germs ([0BLN](https://stacks.math.columbia.edu/tag/0BLN)). |

Other Chapter 58 items are not claimed complete. In particular, 58.9.1–3,
58.10.6, 8, 58.13.3 and the remaining specialization, Lefschetz,
purity and tame-ramification results are still under development or review.
The standard Kummer calculations do not yet complete 58.31.4 ([0EYF](https://stacks.math.columbia.edu/tag/0EYF)).

### Étale cohomology: checked numbered endpoints

| Item | Status in this library |
| --- | --- |
| [59.64.4 / 03RV](https://stacks.math.columbia.edu/tag/03RV) | **Complete:** finite locally constant set sheaves are equivalent to finite étale schemes ([proof](Nyll/EtaleCohomology/Constructible/FiniteLocallyConstantEquivalence.lean)). |
| [59.28.1 / 03PL](https://stacks.math.columbia.edu/tag/03PL) | **Small-site case proved:** the Kummer exact sequence for positive invertible exponents; big-site statement remains ([proof](Nyll/EtaleCohomology/Classical/KummerSequence.lean)). |
| [59.70.8 / 095L](https://stacks.math.columbia.edu/tag/095L) | **Module-sheaf case proved:** open/closed localization, with its cohomology long exact sequence ([proof](Nyll/EtaleCohomology/Classical/Localization.lean)). |
| [59.91.3 / 0A3S](https://stacks.math.columbia.edu/tag/0A3S) | **Module-sheaf H⁰ case proved:** proper henselian closed-fiber comparison; general set-sheaf statement remains ([proof](Nyll/EtaleCohomology/Sites/ProperHenselianH0.lean)). |
| 59.70–73; [64.18.8 / 03UT](https://stacks.math.columbia.edu/tag/03UT) | **Partial:** open-immersion extension by zero, constructible module sheaves, and ordinary constant-coefficient ℓ-adic inverse limits. |
| 59.91; 63.12; [64.20.4 / 03V3](https://stacks.math.columbia.edu/tag/03V3), [64.20.5 / 03V2](https://stacks.math.columbia.edu/tag/03V2) | **Unfinished:** higher proper base change, compactly supported cohomology, and finite/ℓ-adic trace formulas. |

This is a checked endpoint list, not a claim that the other results of
Chapters 59, 63 or 64 have been formalized.

## Use and build

```lean
import Nyll.EtaleFundamentalGroups.All
import Nyll.EtaleCohomology.All
```

From the repository root, with the pinned [`lean-toolchain`](lean-toolchain):

```console
lake exe cache get
lake --wfail build
```

## Authorship

All original code in this library is written by OpenAI Codex.

[Naganori Yamaguchi](https://github.com/n-yamaguchi-0729) sets the mathematical
goals and scope, directs development, and maintains the library.
Imported code retains its original authorship and copyright notices.

## License and acknowledgements

Apache License 2.0. See [LICENSE](LICENSE) and [NOTICE](NOTICE).

The pi1-derived modules adapt [pi1](https://github.com/chrisflav/pi1), by
Christian Merten, with Andrew Yang also credited in some files, for the pinned
toolchain and library APIs, proof repairs, and the module structure used here.
File mappings, the fixed comparison revision, and the distinction between
upstream adaptations and local additions are recorded in
[ATTRIBUTION.md](Nyll/EtaleFundamentalGroups/Pi1/ATTRIBUTION.md),
[UPSTREAM.json](Nyll/EtaleFundamentalGroups/Pi1/UPSTREAM.json), and [NOTICE](NOTICE).

Supporting code also includes adaptations from
[Anthropic's Fermat's Last Theorem project](https://github.com/anthropics/fermats-last-theorem).
Its upstream notices, authors, and licenses are preserved in NOTICE and the
source headers.
