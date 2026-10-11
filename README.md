# EtaleFundamentalGroupsAndCohomology (Lean 4.35.0-rc2)

[![Lean](https://github.com/n-yamaguchi-0729/EtaleFundamentalGroupsAndCohomology/actions/workflows/lean.yml/badge.svg)](https://github.com/n-yamaguchi-0729/EtaleFundamentalGroupsAndCohomology/actions/workflows/lean.yml)
[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

A Lean 4.35.0-rc2 library for étale fundamental groups and étale cohomology.
The fundamental-group library develops the results of
[Stacks Project, Chapter 58: Fundamental Groups of Schemes](https://stacks.math.columbia.edu/tag/0BQ6).
The chapter is partially formalized; its coverage is listed below.

The construction of finite étale Galois categories, geometric fiber functors,
and fundamental groups incorporates substantial code from
[Christian Merten's pi1](https://github.com/chrisflav/pi1), adapted and extended
for this library.

## Public API

Import either complete library with:

```lean
import EtaleFundamentalGroups.All
import EtaleCohomology.All
```

Focused imports include:

```lean
import EtaleFundamentalGroups.FiniteEtale.All
import EtaleFundamentalGroups.GeometricFiber.All
import EtaleFundamentalGroups.Inertia.All
import EtaleCohomology.Classical.All
import EtaleCohomology.Constructible.All
```

Individual result files can also be imported directly.

## Main results

**[Étale schemes over a field](Lean4/EtaleFundamentalGroups/GeometricFiber/EtaleOverFieldEquivalence.lean)**

Étale schemes over a field are equivalent to discrete continuous sets with an action of its absolute Galois group.

**[Finite étale Galois categories](Lean4/EtaleFundamentalGroups/FiniteEtale/GaloisCategory.lean)**

Finite étale covers of a connected scheme form a Galois category, with the geometric fiber as fiber functor. This construction is adapted from pi1.

**[Fundamental groups and inverse limits](Lean4/EtaleFundamentalGroups/FiniteEtale/InverseLimitComparison.lean)**

The fundamental group of an inverse limit of qcqs schemes with affine transition maps is the inverse limit of their fundamental groups.

**[The geometric–arithmetic exact sequence](Lean4/EtaleFundamentalGroups/GeometricFiber/ArithmeticAlgebraicClosure.lean)**

The short exact sequence relating the geometric fundamental group, arithmetic fundamental group, and absolute Galois group for a geometrically connected qcqs scheme.

**[Decomposition and inertia over a DVR](Lean4/EtaleFundamentalGroups/Inertia/NormalizationDVRRamification.lean)**

Decomposition and inertia groups, wild inertia, and the tame character for normalization in a Galois extension of the fraction field of a DVR.

## Stacks Project coverage

The numbering below follows Chapter 58 at revision `ed88ff78`; links use the
Stacks Project's permanent tags. Completed coverage includes results supplied
by upstream libraries as well as proofs added here.

| Completed numbered items | Content |
| --- | --- |
| 58.2.1–3 | Étale schemes over a field and continuous Galois actions ([03QR](https://stacks.math.columbia.edu/tag/03QR)). |
| 58.3.1–11 | Galois categories, profinite completion, uniqueness of fiber functors, and exact functors ([0BN5](https://stacks.math.columbia.edu/tag/0BN5)). |
| 58.4.1–5 | Categorical criteria for surjectivity, injectivity, normality, and exactness of fundamental-group maps. |
| 58.5.1–5 | Finite étale Galois categories and internal Hom, including compatibility with base change ([0BL7](https://stacks.math.columbia.edu/tag/0BL7)). |
| 58.6.1–4 | Fundamental groups, finite continuous actions, change of base point, and the absolute Galois group of a field ([0BNE](https://stacks.math.columbia.edu/tag/0BNE)). |
| 58.8.1–4 | Invariance under henselian pairs, thickenings, and universal homeomorphisms ([0BQN](https://stacks.math.columbia.edu/tag/0BQN)). |
| 58.10.1–5, 7 | Faithfulness and full faithfulness of dense pullback; surjectivity from dense opens and generic points in the geometrically unibranch case ([0BQI](https://stacks.math.columbia.edu/tag/0BQI)). |
| 58.11.1–4 | Normalization, maximal unramified extensions, and the fundamental-group exact sequence for a normal local ring ([0BQM](https://stacks.math.columbia.edu/tag/0BQM)). |
| 58.12.1–4 | Residue fields of normalizations, strict henselianity, inertia under base change, and étaleness of invariant rings. |
| 58.13.1, 2, 4–6 | Decomposition and inertia groups, the kernel from the generic point, unramifiedness, and wild and tame inertia over a DVR ([0BTD](https://stacks.math.columbia.edu/tag/0BTD), [0BUA](https://stacks.math.columbia.edu/tag/0BUA)). |
| 58.14.1–3 | Inverse limits, perfection, and the geometric–arithmetic exact sequence ([0BTV](https://stacks.math.columbia.edu/tag/0BTV), [0BTX](https://stacks.math.columbia.edu/tag/0BTX)). |

The following parts remain incomplete:

| Items | Current scope and remaining results |
| --- | --- |
| 58.7 | Galois-cover characterizations, domination, and common dominating covers are implemented. The full correspondence with normal open subgroups remains incomplete. |
| 58.9.1–3 | Auxiliary adic and proper local constructions are present; the proper henselian comparison and invariance under algebraically closed field extension remain incomplete ([0A48](https://stacks.math.columbia.edu/tag/0A48), [0A49](https://stacks.math.columbia.edu/tag/0A49)). |
| 58.10.6, 8 | The local exact sequence and its kernel description remain incomplete ([0BSB](https://stacks.math.columbia.edu/tag/0BSB), [0BSC](https://stacks.math.columbia.edu/tag/0BSC)). |
| 58.12.5 | Filtered étale-colimit constructions are present; the chapter result is not yet included in completed coverage ([0BSU](https://stacks.math.columbia.edu/tag/0BSU)). |
| 58.13.3 | The quadratic invariant ring, finiteness, normality, and degree-two calculation are implemented. The branch-locus and codimension calculations remain incomplete ([0BTE](https://stacks.math.columbia.edu/tag/0BTE)). |
| 58.15.1–2 | Relative normalization and geometric-fiber constructions are present; finite étaleness of the Stein factor and middle exactness of the homotopy sequence remain incomplete ([0BUN](https://stacks.math.columbia.edu/tag/0BUN), [0C0J](https://stacks.math.columbia.edu/tag/0C0J)). |
| 58.16–20 | Specialization, formal restriction, pushouts, and extension from punctured spectra remain incomplete. |
| 58.21–26 | Purity and related extension theorems remain incomplete. |
| 58.27–30 | Lefschetz theorems, purity of the branch locus, affineness of complements, and specialization in smooth proper families remain incomplete. |
| 58.31–32 | Kummer covers and inertia constructions are present; the complete tame-ramification and positive-characteristic results remain incomplete. |

## Build

The toolchain and dependencies are pinned in [`lean-toolchain`](lean-toolchain)
and [`lakefile.toml`](lakefile.toml).

```console
lake exe cache get
lake --wfail build
```

[CI](.github/workflows/lean.yml) checks imports and builds the libraries
with warnings treated as errors.

## Authorship and AI assistance

[Naganori Yamaguchi](https://github.com/n-yamaguchi-0729) is the author of the
original additions and the responsible maintainer. OpenAI Codex assisted with
Lean development, statement review, and preparation of this repository.
Imported code retains its original authorship and copyright notices.

## License and acknowledgements

Apache License 2.0. See [LICENSE](LICENSE) and [NOTICE](NOTICE).

The repository includes 25 source files bearing attribution to
[pi1](https://github.com/chrisflav/pi1), by Christian Merten, with Andrew Yang
also credited in some files. These files have been adapted for current
toolchain and library APIs, proof repairs, and the module structure used here.
File mappings, revision information, and attribution details are preserved
in [NOTICE](NOTICE).

Supporting code also includes adaptations from
[Anthropic's Fermat's Last Theorem project](https://github.com/anthropics/fermats-last-theorem).
Its upstream notices, authors, and licenses are preserved in NOTICE and the
source headers.
