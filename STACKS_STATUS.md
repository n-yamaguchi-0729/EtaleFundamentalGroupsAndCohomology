# Stacks Project Chapter 58: 番号付き項目一覧

2026-10-11 の収録ソースにある [詳細台帳](Lean4/EtaleFundamentalGroups/StacksProjectChapter58.md) の第3節から作成した一覧です。番号とタグは [公式 Chapter 58](https://stacks.math.columbia.edu/tag/0BQ6) に対応します。基準版は Stacks revision `ed88ff78`（台帳記載の PDF 作成日 2026-07-14）です。

「実装済み」は数学的な到達点に関する既存台帳の分類で、今回の全体ビルド成功を意味しません。古い blocked 行に、後で構成された部分結果が存在する場合があります。原定理を完成したと確認できない項目は未完了に据え置いています。58.12.5 の保留は旧コーディング規則に関する履歴を含むため、数学的証明の欠落と同一視しません。

集計: 実装済み 40、既存結果で充足 16、独立命題ではない 5、数学的実装あり・確認保留 1、構成中 2、部分実装 1、計画 10、基礎結果待ち 66。合計 141。これは完成率ではありません。58.7 の本文や番号付き環境に入らない主張は、この141件とは別に詳細台帳第4節で追跡されています。

| 番号 | 公式タグ | 内容 | 状態 |
|---|---|---|---|
| 58.2.1 | [04JJ](https://stacks.math.columbia.edu/tag/04JJ) | Discrete continuous `G`-sets | 既存の pi1 / mathlib で充足 |
| 58.2.2 | [03QR](https://stacks.math.columbia.edu/tag/03QR) | Étale schemes over a field are equivalent to discrete continuous absolute-Galois sets | 実装済み（台帳） |
| 58.2.3 | [03QS](https://stacks.math.columbia.edu/tag/03QS) | Étale covers correspond to jointly surjective equivariant families | 実装済み（台帳） |
| 58.3.0.1 | [0BS7](https://stacks.math.columbia.edu/tag/0BS7) | Canonical map from `Aut(F)` to the product of the automorphism groups of all fibers | 既存の pi1 / mathlib で充足 |
| 58.3.1 | [0BMR](https://stacks.math.columbia.edu/tag/0BMR) | `Aut(F)` is a closed subgroup of the product and is profinite when all fibers are finite | 既存の pi1 / mathlib で充足 |
| 58.3.2 | [0BMS](https://stacks.math.columbia.edu/tag/0BMS) | Forgetful functor from finite continuous `G`-sets to finite sets | 既存の pi1 / mathlib で充足 |
| 58.3.2.1 | [0BMT](https://stacks.math.columbia.edu/tag/0BMT) | The finite continuous-action forgetful functor | 独立した命題を要求しない |
| 58.3.3 | [0BMU](https://stacks.math.columbia.edu/tag/0BMU) | Automorphisms of the finite-action forgetful functor are the profinite completion of `G` | 実装済み（台帳） |
| 58.3.4 | [0BMV](https://stacks.math.columbia.edu/tag/0BMV) | Every exact finite-set-valued functor on finite continuous `G`-sets is isomorphic to the forgetful functor | 実装済み（台帳） |
| 58.3.5 | [0BMW](https://stacks.math.columbia.edu/tag/0BMW) | A finite-valued functor factors through finite continuous `Aut(F)`-sets | 既存の pi1 / mathlib で充足 |
| 58.3.5.1 | [0BMX](https://stacks.math.columbia.edu/tag/0BMX) | Canonical functor to finite continuous `Aut(F)`-sets | 既存の pi1 / mathlib で充足 |
| 58.3.6 | [0BMY](https://stacks.math.columbia.edu/tag/0BMY) | Galois category and fiber functor | 既存の pi1 / mathlib で充足 |
| 58.3.7 | [0BN0](https://stacks.math.columbia.edu/tag/0BN0) | Basic consequences of the Galois-category axioms | 既存の pi1 / mathlib で充足 |
| 58.3.8 | [0BN2](https://stacks.math.columbia.edu/tag/0BN2) | Every connected object is dominated by a Galois object | 既存の pi1 / mathlib で充足 |
| 58.3.9 | [0BN3](https://stacks.math.columbia.edu/tag/0BN3) | `Aut(F)` acts transitively on the fiber of every connected object | 既存の pi1 / mathlib で充足 |
| 58.3.10 | [0BN4](https://stacks.math.columbia.edu/tag/0BN4) | A Galois category is equivalent to finite continuous `Aut(F)`-sets | 既存の pi1 / mathlib で充足 |
| 58.3.11 | [0BN5](https://stacks.math.columbia.edu/tag/0BN5) | Exact functors correspond to continuous homomorphisms, up to inner conjugacy | 実装済み（台帳） |
| 58.4.0.1 | [0BTR](https://stacks.math.columbia.edu/tag/0BTR) | Diagram relating exact functors and restriction along continuous group homomorphisms | 独立した命題を要求しない |
| 58.4.1 | [0BN6](https://stacks.math.columbia.edu/tag/0BN6) | Surjectivity of the group map, full faithfulness, and preservation of connected objects | 実装済み（台帳） |
| 58.4.2 | [0BS8](https://stacks.math.columbia.edu/tag/0BS8) | Trivial composite group map iff the composite functor has trivial finite objects | 実装済み（台帳） |
| 58.4.3 | [0BS9](https://stacks.math.columbia.edu/tag/0BS9) | Exactness of profinite groups characterized by essential images of exact functors | 実装済み（台帳） |
| 58.4.4 | [0BN7](https://stacks.math.columbia.edu/tag/0BN7) | Injectivity of the group map characterized by epi/mono spans after restriction | 実装済み（台帳） |
| 58.4.5 | [0BTS](https://stacks.math.columbia.edu/tag/0BTS) | Normality of the image characterized by connected objects becoming trivial | 実装済み（台帳） |
| 58.5.1 | [0BN8](https://stacks.math.columbia.edu/tag/0BN8) | Finite étale schemes over a separably closed field are finite sets | 既存の pi1 / mathlib で充足 |
| 58.5.2 | [0BN9](https://stacks.math.columbia.edu/tag/0BN9) | Finite limits, finite colimits, and exact base change for finite étale schemes | 既存の pi1 / mathlib で充足 |
| 58.5.3 | [0BNA](https://stacks.math.columbia.edu/tag/0BNA) | Forgetful functors preserve finite colimits and the appropriate finite limits | 実装済み（台帳） |
| 58.5.4 | [0BL7](https://stacks.math.columbia.edu/tag/0BL7) | The relative internal Hom of finite etale schemes is finite etale and base-change compatible | 実装済み（台帳） |
| 58.5.5 | [0BNB](https://stacks.math.columbia.edu/tag/0BNB) | The geometric fiber makes finite étale schemes over a connected scheme a Galois category | 既存の pi1 / mathlib で充足 |
| 58.6.1 | [0BNC](https://stacks.math.columbia.edu/tag/0BNC) | Étale fundamental group as automorphisms of the geometric fiber functor | 既存の pi1 / mathlib で充足 |
| 58.6.2 | [0BND](https://stacks.math.columbia.edu/tag/0BND) | Finite-action equivalence, base-point change, and functoriality of `π₁` | 実装済み（台帳） |
| 58.6.3 | [0BNE](https://stacks.math.columbia.edu/tag/0BNE) | `π₁(Spec K)` is the absolute Galois group, compatibly with the finite-action equivalence | 実装済み（台帳） |
| 58.6.4 | [0BQ9](https://stacks.math.columbia.edu/tag/0BQ9) | Explicit absolute-Galois action on the geometric fiber | 既存の pi1 / mathlib で充足 |
| 58.8.1 | [0BQA](https://stacks.math.columbia.edu/tag/0BQA) | An equivalence on finite étale covers preserves connected components and fundamental groups | 実装済み（台帳） |
| 58.8.2 | [09ZS](https://stacks.math.columbia.edu/tag/09ZS) | Finite étale covers lift uniquely across a henselian pair | 実装済み（台帳） |
| 58.8.3 | [0BQB](https://stacks.math.columbia.edu/tag/0BQB) | Finite étale covers are invariant under scheme thickenings | 実装済み（台帳） |
| 58.8.4 | [0BQN](https://stacks.math.columbia.edu/tag/0BQN) | Universal homeomorphisms induce equivalences on finite étale covers and isomorphisms on `π₁` | 実装済み（台帳） |
| 58.9.1 | [0A48](https://stacks.math.columbia.edu/tag/0A48) | Proper schemes over a henselian local ring have the same finite étale covers as the closed fiber | 未完了・必要な基礎結果あり |
| 58.9.2 | [0GS2](https://stacks.math.columbia.edu/tag/0GS2) | Proper schemes over a henselian pair have the same finite étale covers as the closed fiber | 未完了・必要な基礎結果あり |
| 58.9.3 | [0A49](https://stacks.math.columbia.edu/tag/0A49) | Proper schemes are invariant under extension of algebraically closed base fields for finite étale covers | 未完了・必要な基礎結果あり |
| 58.10.1 | [0BQE](https://stacks.math.columbia.edu/tag/0BQE) | Dense base change is faithful on finite étale covers | 実装済み（台帳） |
| 58.10.2 | [0BLQ](https://stacks.math.columbia.edu/tag/0BLQ) | Connected punctured strict henselization implies full faithfulness from a local spectrum | 実装済み（台帳） |
| 58.10.3 | [0BQF](https://stacks.math.columbia.edu/tag/0BQF) | Noetherian local-connectedness criterion for full faithfulness from a dense open | 実装済み（台帳） |
| 58.10.4 | [0BSA](https://stacks.math.columbia.edu/tag/0BSA) | Retrocompact dense-open local-connectedness criterion for full faithfulness | 実装済み（台帳） |
| 58.10.5 | [0BQG](https://stacks.math.columbia.edu/tag/0BQG) | Finite-irreducible-component criterion for full faithfulness from a dense open | 実装済み（台帳） |
| 58.10.6 | [0BSB](https://stacks.math.columbia.edu/tag/0BSB) | Exact local `π₁` sequence for a punctured spectrum and its strict henselization | 未完了・必要な基礎結果あり |
| 58.10.6.1 | [0BQH](https://stacks.math.columbia.edu/tag/0BQH) | Map from the fundamental group of the generic point to that of the scheme | 独立した命題を要求しない |
| 58.10.7 | [0BQI](https://stacks.math.columbia.edu/tag/0BQI) | Dense opens and the generic point surject onto the `π₁` of an irreducible geometrically unibranch scheme | 実装済み（台帳） |
| 58.10.8 | [0BSC](https://stacks.math.columbia.edu/tag/0BSC) | Kernel of `π₁(U) → π₁(X)` for finitely many locally connected punctures | 未完了・必要な基礎結果あり |
| 58.11.1 | [0BQK](https://stacks.math.columbia.edu/tag/0BQK) | Unramified field extensions correspond to finite étale normalizations of a normal scheme | 実装済み（台帳） |
| 58.11.2 | [0BQL](https://stacks.math.columbia.edu/tag/0BQL) | A connected finite étale cover of a normal integral scheme is its integral normal normalization | 実装済み（台帳） |
| 58.11.3 | [0BQM](https://stacks.math.columbia.edu/tag/0BQM) | `π₁` of a normal integral scheme is the Galois group of its maximal unramified extension | 実装済み（台帳） |
| 58.11.4 | [0BSM](https://stacks.math.columbia.edu/tag/0BSM) | Exact `π₁` sequence for a normal local ring and its strict henselian fraction field | 実装済み（台帳） |
| 58.12.1 | [0BSP](https://stacks.math.columbia.edu/tag/0BSP) | Residue fields at nonzero primes of a normal domain with separably closed fraction field are algebraically closed | 実装済み（台帳） |
| 58.12.2 | [0BSQ](https://stacks.math.columbia.edu/tag/0BSQ) | A normal local domain with separably closed fraction field is strictly henselian | 実装済み（台帳） |
| 58.12.3 | [0BSS](https://stacks.math.columbia.edu/tag/0BSS) | Inertia subgroups are unchanged by arbitrary base change from an invariant subring | 実装済み（台帳） |
| 58.12.4 | [0BST](https://stacks.math.columbia.edu/tag/0BST) | The map from full invariants to inertia invariants is étale at the chosen prime | 実装済み（台帳） |
| 58.12.5 | [0BSU](https://stacks.math.columbia.edu/tag/0BSU) | Localized inertia invariants in a possibly infinite Galois integral closure are a filtered colimit of étale algebras | 数学的実装あり・旧台帳の確認保留 |
| 58.13.0.1 | [0BSV](https://stacks.math.columbia.edu/tag/0BSV) | Diagram of local, henselian, and strict-henselian punctured-spectrum fundamental groups | 独立した命題を要求しない |
| 58.13.1 | [0BSW](https://stacks.math.columbia.edu/tag/0BSW) | The local `π₁` diagram is the decomposition/inertia diagram, with the global kernel normally generated by inertia | 実装済み（台帳） |
| 58.13.2 | [0BTD](https://stacks.math.columbia.edu/tag/0BTD) | The original generic-point kernel, all point inertia groups and all chosen strict-henselization Galois groups have the same closed normal generation | 実装済み（台帳） |
| 58.13.3 | [0BTE](https://stacks.math.columbia.edu/tag/0BTE) | A normal quotient singularity ramified only in codimension greater than one | 部分実装・中断中 |
| 58.13.4 | [0BTF](https://stacks.math.columbia.edu/tag/0BTF) | Eight global, local and fiberwise unramified criteria, with a ninth inertia criterion for Galois extensions | 実装済み（台帳） |
| 58.13.5 | [0BUA](https://stacks.math.columbia.edu/tag/0BUA) | Decomposition, wild inertia, and tame inertia exact sequences for a possibly infinite Galois extension of a DVR | 実装済み（台帳） |
| 58.13.6 | [0BUB](https://stacks.math.columbia.edu/tag/0BUB) | Absolute decomposition and tame-inertia sequences for a DVR | 実装済み（台帳） |
| 58.14.1 | [0BTV](https://stacks.math.columbia.edu/tag/0BTV) | Finite étale covers and `π₁` commute with inverse limits of qcqs schemes with affine transition maps | 実装済み（台帳） |
| 58.14.2 | [0BTW](https://stacks.math.columbia.edu/tag/0BTW) | Perfection preserves connectedness and the étale fundamental group | 実装済み（台帳） |
| 58.14.3 | [0BTX](https://stacks.math.columbia.edu/tag/0BTX) | Geometric–arithmetic short exact sequence for a geometrically connected qcqs scheme over a field | 実装済み（台帳） |
| 58.15.1 | [0BUN](https://stacks.math.columbia.edu/tag/0BUN) | The Stein factor of a proper, flat, finitely presented morphism with geometrically reduced fibers is finite étale | 構成中・未完了 |
| 58.15.2 | [0C0J](https://stacks.math.columbia.edu/tag/0C0J) | Homotopy exact sequence for a proper flat family with geometrically connected reduced fibers | 構成中・未完了 |
| 58.16.1 | [0C0K](https://stacks.math.columbia.edu/tag/0C0K) | Specialization maps are functorial for maps of proper families with geometrically connected fibers | 未完了・必要な基礎結果あり |
| 58.16.2 | [0C0L](https://stacks.math.columbia.edu/tag/0C0L) | Composites of specialization maps are specialization maps | 未完了・必要な基礎結果あり |
| 58.16.3 | [0C0M](https://stacks.math.columbia.edu/tag/0C0M) | Every specialization map is induced by a strictly henselian valuation ring with algebraically closed fraction field | 未完了・必要な基礎結果あり |
| 58.16.4 | [0C0N](https://stacks.math.columbia.edu/tag/0C0N) | Over a Noetherian base every specialization map is induced by a strictly henselian DVR | 未完了・必要な基礎結果あり |
| 58.17.1 | [0EL8](https://stacks.math.columbia.edu/tag/0EL8) | Full faithfulness of finite étale restriction from full faithfulness of coherent completion on vector bundles | 未完了・必要な基礎結果あり |
| 58.17.2 | [0EL9](https://stacks.math.columbia.edu/tag/0EL9) | Equivalence of finite étale restriction from equivalence of coherent completion on vector bundles | 未完了・必要な基礎結果あり |
| 58.17.3 | [0ELA](https://stacks.math.columbia.edu/tag/0ELA) | Full faithfulness from the colimit over open neighborhoods to a closed subscheme | 未完了・必要な基礎結果あり |
| 58.17.4 | [0EK1](https://stacks.math.columbia.edu/tag/0EK1) | Equivalence from the colimit over open neighborhoods to a closed subscheme | 未完了・必要な基礎結果あり |
| 58.17.5 | [0EJX](https://stacks.math.columbia.edu/tag/0EJX) | Restriction to a closed subscheme meeting every connected component is faithful on finite étale covers | 計画・未完了 |
| 58.17.6 | [0EJZ](https://stacks.math.columbia.edu/tag/0EJZ) | Three formal-function hypotheses implying full faithfulness of restriction to a closed subscheme | 未完了・必要な基礎結果あり |
| 58.17.7 | [0EK0](https://stacks.math.columbia.edu/tag/0EK0) | Neighborhood-colimit formal-function criteria implying full faithfulness | 未完了・必要な基礎結果あり |
| 58.18.1 | [0EK4](https://stacks.math.columbia.edu/tag/0EK4) | Finite étale covers of a scheme pushout are the 2-pullback of the cover categories | 計画・未完了 |
| 58.19.1 | [0BLF](https://stacks.math.columbia.edu/tag/0BLF) | Local ring, hypersurface, and their punctured spectra | 独立した命題を要求しない |
| 58.19.2 | [0BLG](https://stacks.math.columbia.edu/tag/0BLG) | Dimension or component-intersection hypotheses make hypersurface restriction faithful | 未完了・必要な基礎結果あり |
| 58.19.3 | [0BLH](https://stacks.math.columbia.edu/tag/0BLH) | Algebraize a compatible finite morphism over a punctured spectrum and the completed local scheme | 計画・未完了 |
| 58.19.4 | [0BLI](https://stacks.math.columbia.edu/tag/0BLI) | Full faithfulness after completion descends for a henselian ring or henselian pair | 未完了・必要な基礎結果あり |
| 58.19.5 | [0EK5](https://stacks.math.columbia.edu/tag/0EK5) | Dualizing/depth hypotheses imply full faithfulness across a punctured hypersurface | 未完了・必要な基礎結果あり |
| 58.19.6 | [0BM6](https://stacks.math.columbia.edu/tag/0BM6) | Local-cohomology torsion hypotheses imply full faithfulness across a punctured hypersurface | 未完了・必要な基礎結果あり |
| 58.19.7 | [0BLJ](https://stacks.math.columbia.edu/tag/0BLJ) | Depth at least three implies full faithfulness across a punctured hypersurface | 未完了・必要な基礎結果あり |
| 58.20.1 | [0BM8](https://stacks.math.columbia.edu/tag/0BM8) | A depth-two finite scheme over a local spectrum is recovered from functions on the punctured preimage | 計画・未完了 |
| 58.20.2 | [0BLK](https://stacks.math.columbia.edu/tag/0BLK) | Extension of a finite étale punctured cover is equivalent to its global-sections algebra being finite étale | 未完了・必要な基礎結果あり |
| 58.20.3 | [0BM9](https://stacks.math.columbia.edu/tag/0BM9) | Finite étale covers of a punctured normal local spectrum are finite normal algebras étale off the closed point | 未完了・必要な基礎結果あり |
| 58.20.4 | [0BLL](https://stacks.math.columbia.edu/tag/0BLL) | A punctured finite étale cover extends before completion iff it extends after completion | 未完了・必要な基礎結果あり |
| 58.20.5 | [0EK6](https://stacks.math.columbia.edu/tag/0EK6) | Dualizing/depth hypotheses algebraize an extension from the punctured hypersurface | 未完了・必要な基礎結果あり |
| 58.20.6 | [0BLS](https://stacks.math.columbia.edu/tag/0BLS) | Local-cohomology torsion hypotheses algebraize an extension from the punctured hypersurface | 未完了・必要な基礎結果あり |
| 58.20.7 | [0BLM](https://stacks.math.columbia.edu/tag/0BLM) | Depth at least three algebraizes an extension from the punctured hypersurface | 未完了・必要な基礎結果あり |
| 58.21.1 | [0BJG](https://stacks.math.columbia.edu/tag/0BJG) | A height-one prime in `V(f)` of a positive-dimensional Noetherian local ring | 計画・未完了 |
| 58.21.2 | [0BJH](https://stacks.math.columbia.edu/tag/0BJH) | A flat quasi-finite morphism unramified in codimension one is étale at the point | 未完了・必要な基礎結果あり |
| 58.21.3 | [0BMA](https://stacks.math.columbia.edu/tag/0BMA) | Purity for regular local rings and finite normal extensions | 未完了・必要な基礎結果あり |
| 58.21.4 | [0BMB](https://stacks.math.columbia.edu/tag/0BMB) | Purity of branch locus | 未完了・必要な基礎結果あり |
| 58.21.5 | [0EY6](https://stacks.math.columbia.edu/tag/0EY6) | Canonical reflexive finite extension of a finite étale cover across a depth-two complement | 未完了・必要な基礎結果あり |
| 58.21.6 | [0EY7](https://stacks.math.columbia.edu/tag/0EY7) | Local purity outside an open implies essential surjectivity of finite étale restriction | 未完了・必要な基礎結果あり |
| 58.22.1 | [0BLN](https://stacks.math.columbia.edu/tag/0BLN) | Faithfulness of restriction near a punctured hypersurface under a component-dimension bound | 未完了・必要な基礎結果あり |
| 58.22.2 | [0DXX](https://stacks.math.columbia.edu/tag/0DXX) | A dualizing-complex criterion for full faithfulness near a punctured hypersurface | 未完了・必要な基礎結果あり |
| 58.22.3 | [0BLP](https://stacks.math.columbia.edu/tag/0BLP) | A local-cohomology finiteness criterion for full faithfulness | 未完了・必要な基礎結果あり |
| 58.23.1 | [0DXY](https://stacks.math.columbia.edu/tag/0DXY) | A dualizing and depth criterion for algebraizing finite étale covers from a hypersurface | 未完了・必要な基礎結果あり |
| 58.23.2 | [0BLV](https://stacks.math.columbia.edu/tag/0BLV) | An `H¹` and `H²` local-cohomology criterion for algebraization equivalence | 未完了・必要な基礎結果あり |
| 58.23.3 | [0BLW](https://stacks.math.columbia.edu/tag/0BLW) | The algebraization equivalence for complete normal local domains of dimension at least four | 未完了・必要な基礎結果あり |
| 58.24.1 | [0EK9](https://stacks.math.columbia.edu/tag/0EK9) | Local purity upgrades neighbourhood algebraization to essential surjectivity | 未完了・必要な基礎結果あり |
| 58.24.2 | [0EKA](https://stacks.math.columbia.edu/tag/0EKA) | The local-cohomology version of the local-purity extension theorem | 未完了・必要な基礎結果あり |
| 58.25.1 | [0DXZ](https://stacks.math.columbia.edu/tag/0DXZ) | Purity descends to a hypersurface under dualizing and depth hypotheses | 未完了・必要な基礎結果あり |
| 58.25.2 | [0BPC](https://stacks.math.columbia.edu/tag/0BPC) | Purity descends to a hypersurface under local-cohomology hypotheses | 未完了・必要な基礎結果あり |
| 58.25.3 | [0BPD](https://stacks.math.columbia.edu/tag/0BPD) | Purity for local complete intersections of dimension at least three | 未完了・必要な基礎結果あり |
| 58.26.1 | [0EY9](https://stacks.math.columbia.edu/tag/0EY9) | Full faithfulness along the punctured zero section of a formal power-series family | 未完了・必要な基礎結果あり |
| 58.26.2 | [0EYA](https://stacks.math.columbia.edu/tag/0EYA) | Ramanujam–Samuel purity for finite étale covers of a formal power-series ring | 未完了・必要な基礎結果あり |
| 58.26.3 | [0EYB](https://stacks.math.columbia.edu/tag/0EYB) | Purity for a dense open in a smooth family away from depth-at-most-one fibers | 未完了・必要な基礎結果あり |
| 58.26.4 | [0EYC](https://stacks.math.columbia.edu/tag/0EYC) | Ramanujam–Samuel purity for an adically formally smooth local homomorphism | 未完了・必要な基礎結果あり |
| 58.27.1 | [0ELC](https://stacks.math.columbia.edu/tag/0ELC) | Lefschetz full faithfulness for a hypersurface section under a depth-plus-dimension bound | 未完了・必要な基礎結果あり |
| 58.27.2 | [0ELD](https://stacks.math.columbia.edu/tag/0ELD) | Lefschetz equivalence from open neighborhoods of a hypersurface section | 未完了・必要な基礎結果あり |
| 58.27.3 | [0ELE](https://stacks.math.columbia.edu/tag/0ELE) | Lefschetz equivalence, and `π₁` isomorphism, assuming local purity off the hypersurface | 未完了・必要な基礎結果あり |
| 58.28.1 | [0EA2](https://stacks.math.columbia.edu/tag/0EA2) | A canonical-divisor condition on a surface resolution implies a rational singularity and vanishing exceptional divisor | 計画・未完了 |
| 58.28.2 | [0EA3](https://stacks.math.columbia.edu/tag/0EA3) | A finite-type map from a normal surface germ to an excellent regular local base, étale off the closed germ, is étale at the germ | 未完了・必要な基礎結果あり |
| 58.28.3 | [0EA4](https://stacks.math.columbia.edu/tag/0EA4) | Purity of ramification locus | 未完了・必要な基礎結果あり |
| 58.29.1 | [0ECB](https://stacks.math.columbia.edu/tag/0ECB) | Higher coherent cohomology of an affine étale cover of a punctured equicharacteristic regular local scheme is injective-residue-hull torsion | 計画・未完了 |
| 58.29.2 | [0ECC](https://stacks.math.columbia.edu/tag/0ECC) | Vanishing of the top higher cohomology forces the étale punctured cover to be affine | 未完了・必要な基礎結果あり |
| 58.29.3 | [0ECD](https://stacks.math.columbia.edu/tag/0ECD) | The maximal étale locus of a finite-type map from a normal scheme to an excellent regular scheme over a field is affine | 未完了・必要な基礎結果あり |
| 58.30.1 | [0C0P](https://stacks.math.columbia.edu/tag/0C0P) | Specialization is surjective for a flat proper family with geometrically connected fibers and geometrically reduced special fiber | 未完了・必要な基礎結果あり |
| 58.30.2 | [0C0Q](https://stacks.math.columbia.edu/tag/0C0Q) | Specialization is an isomorphism for a smooth proper family in residue characteristic zero | 未完了・必要な基礎結果あり |
| 58.30.3 | [0C0R](https://stacks.math.columbia.edu/tag/0C0R) | Specialization is surjective and an isomorphism on maximal prime-to-`p` quotients in residue characteristic `p` | 未完了・必要な基礎結果あり |
| 58.31.1 | [0EYD](https://stacks.math.columbia.edu/tag/0EYD) | Codimension-one unramifiedness/tameness is preserved by suitable base change | 計画・未完了 |
| 58.31.2 | [0H2W](https://stacks.math.columbia.edu/tag/0H2W) | A codimension-one-unramified finite étale cover extends across a regular complement | 未完了・必要な基礎結果あり |
| 58.31.3 | [0EYE](https://stacks.math.columbia.edu/tag/0EYE) | Extension across a regular effective Cartier divisor for codimension-one-unramified covers | 未完了・必要な基礎結果あり |
| 58.31.4 | [0EYF](https://stacks.math.columbia.edu/tag/0EYF) | Standard tamely ramified morphism `A[x]/(x^e-f)` | 計画・未完了 |
| 58.31.5 | [0EYG](https://stacks.math.columbia.edu/tag/0EYG) | Abhyankar's lemma for a regular divisor: tame covers are étale-locally standard | 未完了・必要な基礎結果あり |
| 58.31.6 | [0EYH](https://stacks.math.columbia.edu/tag/0EYH) | The normalization of a regular-divisor tame cover is finite locally free with regular reduced boundary and standard local form | 未完了・必要な基礎結果あり |
| 58.31.7 | [0EYI](https://stacks.math.columbia.edu/tag/0EYI) | DVR-valued lifting and split-generic-fiber criteria for the normalization to be étale along a trait | 未完了・必要な基礎結果あり |
| 58.31.8 | [0EYJ](https://stacks.math.columbia.edu/tag/0EYJ) | Extend prime-to-characteristic pointed Galois covers from the generic fiber of a smooth family over a Noetherian normal base | 未完了・必要な基礎結果あり |
| 58.31.9 | [0EZJ](https://stacks.math.columbia.edu/tag/0EZJ) | The preceding pointed Galois-cover extension over a qcqs normal integral base | 未完了・必要な基礎結果あり |
| 58.32.1 | [0G1F](https://stacks.math.columbia.edu/tag/0G1F) | Positive-characteristic coordinate modification strictly lowers the nonfinite-generator measure `NF` | 計画・未完了 |
| 58.32.2 | [0G1G](https://stacks.math.columbia.edu/tag/0G1G) | An affine étale morphism to affine space in positive characteristic admits a finite étale structure map | 未完了・必要な基礎結果あり |
| 58.32.3 | [0G1H](https://stacks.math.columbia.edu/tag/0G1H) | A finite étale cover of a closed subscheme of affine space embeds clopenly in the pullback of a finite étale cover of affine space | 未完了・必要な基礎結果あり |
| 58.32.4 | [0G1I](https://stacks.math.columbia.edu/tag/0G1I) | A closed immersion of connected affine `𝔽_p`-schemes induces an injective map on étale fundamental groups | 未完了・必要な基礎結果あり |
