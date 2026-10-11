# EtaleFundamentalGroupsAndCohomology

[![Lean](https://github.com/n-yamaguchi-0729/EtaleFundamentalGroupsAndCohomology/actions/workflows/lean.yml/badge.svg)](https://github.com/n-yamaguchi-0729/EtaleFundamentalGroupsAndCohomology/actions/workflows/lean.yml)
[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

Étale Fundamental Groups and Étale Cohomology

Lean 4 によるエタール基本群とエタール・コホモロジーの形式化ライブラリです。`EtaleFundamentalGroups`（EFG）と `EtaleCohomology`（EC）の全ソース、および実装に必要なローカル依存ライブラリを収録します。

EFG の目標は [Stacks Project Chapter 58, Fundamental Groups of Schemes](https://stacks.math.columbia.edu/tag/0BQ6) の形式化、EC の目標は有限体上の分離有限型スキームと構成可能な ℓ 進係数に対する Grothendieck–Lefschetz 跡公式です。**どちらも開発途中です。Chapter 58 全体、固有基底変換、Nagata コンパクト化、跡公式の完成は主張しません。**

## pi1 を基礎にした実装

本ライブラリには **[Christian Merten の pi1](https://github.com/chrisflav/pi1) のコードを取り込んでいます**。有限エタール被覆が Galois 圏をなすこと、幾何的ファイバー関手、その自己同型群による基本群の構成は、この先行研究と mathlib の Galois 圏理論を基礎にしています。

取り込んだコードは現在 `EtaleFundamentalGroups` と `SchemeTheory` に配置し、Lean / mathlib の更新、依存方向の整理、必要な証明の補修に合わせて変更しています。上流由来の `Authors:`、著作権・ライセンス表示、元ファイルへのリンクを保持しています。現在 pi1 の出典表示を持つのは25ファイルです。

- 上流: [chrisflav/pi1](https://github.com/chrisflav/pi1)
- ライセンス: [上流 Apache 2.0](https://github.com/chrisflav/pi1/blob/5c5c0171efc863ce9990171bdf46d7cb5fd582fb/LICENSE)
- 比較 revision: `5c5c0171efc863ce9990171bdf46d7cb5fd582fb`。**正確なコピー元コミットは未確認**であり、この値は比較対象です。
- 著者: Christian Merten。一部ファイルには Andrew Yang も記載されています。
- 対応する元ファイル、現在の配置、未確認の帰属情報は [PI1_ATTRIBUTION.md](PI1_ATTRIBUTION.md) に記載しています。

## Stacks Project Chapter 58 の到達点

以下は2026年10月11日の収録ソースと既存の検証記録から整理した状態です。基準となる Stacks 版は `ed88ff78`（台帳記載の PDF 作成日 2026-07-14）です。公式番号に加えて永続タグを使います。

「実装済み」は対象とする数学的結論の実装があること、「既存結果で充足」は pi1 または mathlib の対応する公開宣言を利用することです。個別定理の過去の検証記録と、この配布版全体のビルド状態は区別します。

| Stacks の範囲 | 実装・利用できる内容 | 未完了・構成中の内容 |
|---|---|---|
| 58.2.1–3 | 体上のエタール・スキームと離散連続 Galois 集合の圏同値、被覆族の比較。58.2.2 は [03QR](https://stacks.math.columbia.edu/tag/03QR)。 | 番号付き項目は実装または既存結果で充足。 |
| 58.3.1–11 | Galois 圏の基礎は主に mathlib。副有限完備化との比較 58.3.3 [0BMU](https://stacks.math.columbia.edu/tag/0BMU)、ファイバー関手の一意性 58.3.4 [0BMV](https://stacks.math.columbia.edu/tag/0BMV)、完全関手と連続準同型の比較 58.3.11 [0BN5](https://stacks.math.columbia.edu/tag/0BN5) を追加。 | 番号付き項目は充足。本文中の独立主張の監査は別台帳で管理。 |
| 58.4.1–5 | 基本群準同型の全射性・単射性・正規性、完全列の圏論的判定。 | 番号付き補題は実装済み。 |
| 58.5.1–5 | pi1 の有限エタール Galois 圏。忘却関手の余極限保存、内部 Hom と基底変換 58.5.4 [0BL7](https://stacks.math.columbia.edu/tag/0BL7)。 | 番号付き項目は実装または既存結果で充足。 |
| 58.6.1–4 | 基本群、有限連続作用との圏同値、基点変更・関手性。58.6.3 [0BNE](https://stacks.math.columbia.edu/tag/0BNE) は体の絶対 Galois 群との比較。 | 番号付き項目は実装または既存結果で充足。 |
| 58.7 [03SF](https://stacks.math.columbia.edu/tag/03SF)（本文） | Galois 被覆の自己同型数・次数・作用による特徴付け、Galois 被覆による支配、二つの被覆の共通支配。 | 正規開部分群による商との対応について、本文台帳の照合は未完了。節全体の完成とは数えない。 |
| 58.8.1–4 | 有限エタール圏の同値と連結成分・基本群、henselian pair [09ZS](https://stacks.math.columbia.edu/tag/09ZS)、thickening、普遍的同相 [0BQN](https://stacks.math.columbia.edu/tag/0BQN) による不変性。 | 四つの原定理の結論を実装済み。 |
| 58.9.1–3 | adic な被覆・代数や固有局所モデルなどの補助構成あり。 | henselian 基底上の固有スキームと閉ファイバーの有限エタール圏同値 [0A48](https://stacks.math.columbia.edu/tag/0A48) / [0GS2](https://stacks.math.columbia.edu/tag/0GS2)、代数閉体拡大不変性 [0A49](https://stacks.math.columbia.edu/tag/0A49) は未完了。 |
| 58.10.1–5, 7 | 稠密引き戻しの忠実性、局所連結性による充満忠実性、幾何的単枝スキームの稠密開集合・一般点からの基本群全射性 [0BQI](https://stacks.math.columbia.edu/tag/0BQI)。 | 58.10.6 [0BSB](https://stacks.math.columbia.edu/tag/0BSB)、58.10.8 [0BSC](https://stacks.math.columbia.edu/tag/0BSC) の局所完全列・核記述は未完了。 |
| 58.11.1–4 | 正規スキームの有限エタール正規化、最大不分岐拡大による基本群 [0BQM](https://stacks.math.columbia.edu/tag/0BQM)、正規局所環の完全列。 | 四つの番号付き原定理の結論を実装済み。 |
| 58.12.1–4 | 正規化の剰余体、strict henselian 性、inertia の基底変換不変性、不変環のエタール性。 | 58.12.5 [0BSU](https://stacks.math.columbia.edu/tag/0BSU) の filtered étale colimit の数学的証明は存在。旧台帳に実装整理の保留表示が残るため、一律の完成件数には含めない。 |
| 58.13.1, 2, 4–6 | 局所基本群と分解群・惰性群の可換図式 [0BSW](https://stacks.math.columbia.edu/tag/0BSW)、一般点の核と惰性群の閉正規包 [0BTD](https://stacks.math.columbia.edu/tag/0BTD)、不分岐性の同値条件 [0BTF](https://stacks.math.columbia.edu/tag/0BTF)、DVR の wild / tame inertia [0BUA](https://stacks.math.columbia.edu/tag/0BUA)、絶対版 [0BUB](https://stacks.math.columbia.edu/tag/0BUB)。 | 58.13.3 [0BTE](https://stacks.math.columbia.edu/tag/0BTE) の符号作用による商特異点は部分実装。二次不変式環・有限性・正規性・次数2まであり、分岐集合と余次元の計算は未完了。 |
| 58.14.1–3 | qcqs スキームの affine 遷移逆極限と有限エタール圏・基本群 [0BTV](https://stacks.math.columbia.edu/tag/0BTV)、完全化による不変性 [0BTW](https://stacks.math.columbia.edu/tag/0BTW)、幾何・算術基本群の短完全列 [0BTX](https://stacks.math.columbia.edu/tag/0BTX)。 | 三つの原定理の結論を実装済み。 |
| 58.15.1–2 | 相対正規化、固有な幾何的被約スキームの切断代数、局所モデル、幾何的ファイバーからの合成の自明性・基底への基本群全射性を構成。 | Stein 因子の有限エタール性 [0BUN](https://stacks.math.columbia.edu/tag/0BUN)、homotopy exact sequence の中間完全性 [0C0J](https://stacks.math.columbia.edu/tag/0C0J) は未完了。補助定理だけで原命題を完成としない。 |
| 58.16.1–4 | 特殊化への関連基盤を収録。 | 原定理の特殊化写像とその性質は未完了。 |
| 58.17.1–7, 58.18.1 | 閉部分スキームへの制限、貼り合わせに関する基盤を収録。 | 形式完備化による制限定理と pushout の原定理は未完了。58.17.5 [0EJX](https://stacks.math.columbia.edu/tag/0EJX) の候補も完成として数えない。 |
| 58.19.2–7, 58.20.1–7 | punctured spectrum に関する局所代数などの部分結果あり。58.19.1 は状況設定。 | 原定理の降下・代数化・延長は未完了。58.19.2 [0BLG](https://stacks.math.columbia.edu/tag/0BLG) の候補も完成として数えない。 |
| 58.21.1–6, 58.22.1–3, 58.23.1–3, 58.24.1–2, 58.25.1–3, 58.26.1–4 | purity と局所代数の関連補助実装あり。 | 番号付き原定理の一式は未完了。正則局所環の purity の候補と Chapter 58 の原定理完成を区別する。 |
| 58.27.1–3, 58.28.1–3, 58.29.1–3, 58.30.1–3 | 基本群の Lefschetz 定理、分岐集合の purity、補集合の affine 性、滑らかな固有族の特殊化が今後の対象。 | 原定理は未完了。 |
| 58.31.1–9, 58.32.1–4 | Kummer 被覆・根の添加・惰性群・Abhyankar 型の基礎を収録。 | tame ramification と正標数の技巧について、ここに列挙した原定理の一式は未完了。ファイル名や補助構成の存在だけで該当タグの完成とは数えない。 |

全141件の番号・公式タグ・個別状態は [STACKS_STATUS.md](STACKS_STATUS.md)、宣言名と供給元、本文中の主張、外部参照の監査は [StacksProjectChapter58.md](Lean4/EtaleFundamentalGroups/StacksProjectChapter58.md) にあります。番号付き項目の分類は、実装済み40、既存結果で充足16、独立命題ではない5、数学的実装あり・確認保留1、構成中2、部分実装1、計画10、必要な基礎結果待ち66です。件数は数学的完成率を表しません。詳細台帳には過去の作業順・停止点・旧配置も残っています。

## 主要な宣言

- [`GeometricFiber/EtaleOverFieldEquivalence.lean`](Lean4/EtaleFundamentalGroups/GeometricFiber/EtaleOverFieldEquivalence.lean): `AlgebraicGeometry.Scheme.Etale.equivDiscreteContAction`。体上のエタール・スキームを絶対 Galois 群の離散連続作用として記述します。
- [`FiniteEtale/GaloisCategory.lean`](Lean4/EtaleFundamentalGroups/FiniteEtale/GaloisCategory.lean): pi1 由来の `AlgebraicGeometry.FiniteEtale.galoisCategory`。連結スキーム上の有限エタール被覆と幾何的ファイバー関手を Galois 圏理論へ接続します。
- [`FiniteEtale/InverseLimitComparison.lean`](Lean4/EtaleFundamentalGroups/FiniteEtale/InverseLimitComparison.lean): `fundamentalGroupInverseLimitEquiv`。affine 遷移写像を持つ qcqs スキームの逆極限について、元の射が誘導する基本群準同型を座標とする位相群同型を構成します。
- [`GeometricFiber/ArithmeticAlgebraicClosure.lean`](Lean4/EtaleFundamentalGroups/GeometricFiber/ArithmeticAlgebraicClosure.lean): `arithmetic_exactSequence_of_isAlgClosure`。幾何的に連結な qcqs スキームの幾何・算術基本群の実際の射について、単射・全射・核と像の一致を証明します。
- [`Inertia/NormalizationDVRRamification.lean`](Lean4/EtaleFundamentalGroups/Inertia/NormalizationDVRRamification.lean): `normalizationDVR_ramification`。DVR の分数体の任意の Galois 拡大に対し、正規化上の実際の分解群・惰性群・wild 部分群・tame 指標を構成済みの供給元からまとめます。これらの存在や完全性を追加入力として仮定する定理ではありません。

## EtaleCohomology の到達点

小エタール site の実際の層と mathlib の `Sheaf.H` を用います。層・コホモロジー・基本群の比較を同じ対象上に構成する方針です。[PLAN.md](Lean4/EtaleCohomology/PLAN.md) に目標、仮定、段階ごとの未完了部分を記載しています。

| 段階 | 状態と内容 |
|---|---|
| M0: 古典的コホモロジー | 実装済み。係数加群の作用、H⁰ と大域切断の同一視、短完全列からの長完全列、幾何的茎・層関手・随伴・必要な完全性。 |
| M1: 構成可能層と有限モノドロミー | 実装済み。局所化長完全列、有限局所定数集合層の有限エタール表現可能性、有限被覆による自明化、基本群作用との比較、構成可能性の局所性・qcqs 上の有限層別化・引き戻し・核・余核・拡大。核と拡大には係数環の Noether 性、開零拡張・閉直像には必要な準コンパクト性・retrocompact 条件を明示。 |
| M2: 固有基底変換とコンパクト化 | 構成中。henselian な切断、有限段降下、Noetherian な固有閉ファイバーの冪等元持ち上げ、compact-open 上の層の有限表示性等の補助結果あり。一般の proper integral 閉ファイバー連結性、H⁰ 制限の全射性、高次固有基底変換、Nagata コンパクト化は未完了。 |
| 後続段階 | コンパクト化から独立な Rf!・コンパクト台コホモロジー、有限性・次元消滅、一般の adic system と導来比較、Frobenius 作用と跡公式は未完了。 |

有限局所定数集合層については [`finiteEtaleEquivFiniteLocallyConstantSetSheaf`](Lean4/EtaleCohomology/Constructible/FiniteLocallyConstantEquivalence.lean) が任意の基底上の有限エタール表現可能性を与え、[`finiteLocallyConstantSetMonodromy`](Lean4/EtaleCohomology/Constructible/Monodromy.lean) は連結基底上の有限連続基本群作用との圏同値を与えます。後者は実際の幾何的茎との自然同型も含みます。

定数係数については [`Classical/Adic.lean`](Lean4/EtaleCohomology/Classical/Adic.lean) に有限係数コホモロジーの逆極限、[`Classical/RationalAdic.lean`](Lean4/EtaleCohomology/Classical/RationalAdic.lean) に ℤℓ 作用と ℚℓ へのスカラー拡大を実装しています。この構成から、一般の構成可能 ℓ 進層の導来理論や pro-étale コホモロジーとの比較が完成したとは主張しません。

最終目標は、有限体 k = Fq 上の分離有限型スキーム X と構成可能な ℚℓ 層 F（ℓ ≠ char k）について、有限拡大上の有理点での幾何的 Frobenius の局所跡の和を、Hc の Frobenius 作用の交代跡として表すことです。定数層の場合には点数公式を得ることを目指します。現時点でこの最終公式は未証明です。

## 出典とライセンス

ライセンスは [LICENSE](LICENSE) と各ソースヘッダを参照してください。pi1 由来部分の帰属は [PI1_ATTRIBUTION.md](PI1_ATTRIBUTION.md) にまとめています。依存する `SchemeTheory` に含まれる Anthropic の Fermat's Last Theorem プロジェクト由来コードについては [同ライブラリの帰属表](Lean4/SchemeTheory/ANTHROPIC_FLT_ATTRIBUTION.md) と [NOTICE](Lean4/SchemeTheory/ANTHROPIC_FLT_NOTICE) を参照してください。mathlib とその著者・貢献者の成果を基礎にしています。

独自作成部分の著作権者は Naganori Yamaguchi、著者表示は Naganori Yamaguchi (assisted by OpenAI Codex) です。[著者の GitHub](https://github.com/n-yamaguchi-0729)。外部由来ファイルでは元の著者・権利者の表示を保持します。

## 依存関係を含む配布範囲

各行のライブラリの **全 maintained source** を収録しています。主ライブラリだけでなく、ローカル import の依存先をライブラリ単位で再帰的に含めた独立パッケージです。別の非公開リポジトリを clone する必要はありません。外部依存の mathlib とその依存は Lake が固定 revision から取得します。

| 深さ | ライブラリ | Lean ファイル数 |
|---:|---|---:|
| 1 | [ProCGroups](Lean4/ProCGroups/All.lean) | 724 |
| 1 | [ValuedFieldTheory](Lean4/ValuedFieldTheory/All.lean) | 591 |
| 1 | [GaloisCohomology](Lean4/GaloisCohomology/All.lean) | 309 |
| 1 | [SchemeTheory](Lean4/SchemeTheory/All.lean) | 975 |
| 2 | [ClassFieldTheory](Lean4/ClassFieldTheory/All.lean) | 1,246 |
| 2 | [AlgebraicCurves](Lean4/AlgebraicCurves/All.lean) | 2,452 |
| 2 | [EtaleFundamentalGroups](Lean4/EtaleFundamentalGroups/All.lean) | 1,608 |
| 2 | [EtaleCohomology](Lean4/EtaleCohomology/All.lean) | 125 |

パッケージ全体の入口は [`All`](Lean4/All.lean) です。各ライブラリの元のモジュール名を保持しているため、重複するソースを含む他の分割パッケージと同じ Lake 環境へ重ねて導入することは想定していません。

## ビルドと CI

Lean は [`lean-toolchain`](lean-toolchain) の **4.35.0-rc2**、mathlib は [`lakefile.toml`](lakefile.toml) の **065356127b1dc0016f66b7283ce0ce2c4055aa55** に固定しています。再現時は同梱の [`lake-manifest.json`](lake-manifest.json) を使います。

Git と [elan](https://github.com/leanprover/elan) を用意して実行します。

```sh
git clone https://github.com/n-yamaguchi-0729/EtaleFundamentalGroupsAndCohomology.git
cd EtaleFundamentalGroupsAndCohomology
lake exe cache get Mathlib
python3 .github/scripts/audit.py
lake --wfail build +ProCGroups.All +ValuedFieldTheory.All +GaloisCohomology.All +SchemeTheory.All
lake --wfail build +ClassFieldTheory.All +AlgebraicCurves.All +EtaleFundamentalGroups.All +EtaleCohomology.All
lake --wfail build +All
```

[`CI`](.github/workflows/lean.yml) は公開済みの [ProCGroups](https://github.com/n-yamaguchi-0729/ProCGroups)・[ClassFieldTheory](https://github.com/n-yamaguchi-0729/ClassFieldTheory)・[SawinTotallyRealTowers](https://github.com/n-yamaguchi-0729/SawinTotallyRealTowers) の版固定・依存深さ順の検証・成果物キャッシュの構成を参考にしています。今回の CI は次を行います。

- 全物理ソースと Lake glob、入口からの到達、import の欠落・循環・逆依存を静的検査。
- 深さ1、2、3のライブラリを順に通常ビルドし、最後に `+All` をビルド。
- `autoImplicit = false`、未使用引数、文書化、mathlib 標準 linter を Lake 設定で有効化。
- 段階間でプロジェクトのコンパイル成果物を再利用し、失敗時も診断ログを保存。

`lake --wfail build` を使い、警告・エラーを失敗にします。この配布範囲には AnabelianGeometry の未証明定理を含みません。新たな `sorry` / `admit` / 独自 `axiom` は静的検査でも拒否します。静的検査は証明項の独立検証ではありません。この CI では NanoDa や別途の全宣言 kernel replay を実行したとは主張しません。

**private の push / pull request ではビルドジョブを開始せず、Actions の手動実行は可能**です。public に切り替えた後は push / pull request で動作します。初回配布では private のまま作成し、公開設定の変更も CI の手動起動も行っていません。

初回の検証結果と検証範囲は [VALIDATION.md](VALIDATION.md) に記録しています。

## ソースの来歴

分割元、固定コミット、同梱ファイルの SHA-256 は [SOURCE_SNAPSHOT.json](SOURCE_SNAPSHOT.json) にあります。Lean 本文・既存の著作権表示は分割元から変更せず、配布用 `Lean4/All.lean`、Lake の対象範囲、README と CI を作成しました。ライブラリ内の既存計画には古い配置・当時の停止点が残る場合があります。

[第三者由来のコードと帰属](THIRD_PARTY.md) および [pi1 の25ファイル対応表](PI1_ATTRIBUTION.md) も参照してください。
