# プロセスエンジニアリング検証プロジェクト

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.PENDING.svg)](https://doi.org/10.5281/zenodo.PENDING)

## 概要

このプロジェクトは、「人間によるコーディングとAIコーディングの違い：プロセスエンジニアリングアプローチによる体系化」論文で提示された手法の技術検証を目的としています。

## プロジェクト構成

### 文書構造

```
docs/
├── theory/                                    # 理論・研究系文書
│   ├── human-vs-ai-coding-process-engineering-paper-v1.2.md # 論文本体v1.2（3分割）
│   ├── human-vs-ai-coding-process-engineering-paper-v1.2-part2.md # 論文v1.2 Part2
│   ├── human-vs-ai-coding-process-engineering-paper-v1.2-part3.md # 論文v1.2 Part3
│   ├── ai-coding-development-process-v1.3-part1.md # プロセス体系文書v1.3 Part1
│   ├── ai-coding-development-process-v1.3-part2.md # プロセス体系文書v1.3 Part2
│   ├── ai-coding-development-process-v1.3-part3.md # プロセス体系文書v1.3 Part3
│   ├── categorical-task-management-guide.md # 段階的タスク管理ガイド
│   ├── quality-assurance-integration.md # 多層品質保証ガイド
│   ├── experimental-validation-report.md     # 実験検証レポート
│   ├── reproducibility-validation-plan.md    # 再現性検証計画
│   ├── related-research-analysis.md          # 関連研究分析
│   └── academic-publication-guide.md         # 学術出版ガイド
├── templates/                                 # 再利用可能テンプレート
│   ├── README.md                             # テンプレート一覧とガイド
│   ├── document-format-specifications.md     # 文書フォーマット仕様
│   ├── cline-process-engineering-rules.md    # 実装ルール
│   ├── cline-custom-instructions.md          # カスタムインストラクション
│   ├── header-template.md                    # ヘッダーテンプレート
│   ├── step0-goal-statement-template.md      # STEP 0: ゴール定義
│   ├── step0-stakeholders-template.md        # ステークホルダー一覧
│   ├── step0-constraints-template.md         # 制約条件リスト
│   ├── step1-use-cases-template.md           # STEP 1: ユースケース一覧
│   ├── step1-non-functional-template.md      # 非機能要件リスト
│   ├── step1-requirements-specification-template.md # 要求仕様書
│   ├── step2-system-architecture-template.md # STEP 2: システム構成図
│   ├── step2-tech-stack-template.md          # 技術選定・依存関係定義書
│   ├── step3-class-design-template.md        # STEP 3: クラス設計表
│   ├── step3-interfaces-template.md          # メソッドインターフェースリスト
│   ├── step4-test-strategy-template.md       # STEP 4: テスト戦略書
│   ├── step4-test-targets-template.md        # テスト対象一覧
│   ├── step4-test-cases-template.md          # テストケース定義書
│   ├── step5-components-template.md          # STEP 5: 実装コンポーネント一覧
│   ├── step5-schedule-template.md            # 開発工程表
│   ├── step5-directory-structure-template.md # ディレクトリ構造マップ
│   ├── step6-todo-list-template.md           # STEP 6: ToDoリストテンプレート
│   ├── step6-todo-creation-guide.md          # ToDoリスト作成ガイド
│   ├── step6-task-list-template.md           # ファイル単位タスクリスト
│   ├── step6-task-management-template.md     # タスク管理表
│   ├── step6-task-specification-template.md  # タスク仕様書
│   ├── step7-progress-template.md            # STEP 7: 実行ログ・進捗管理
│   ├── step7-deliverables-template.md        # 成果物・品質記録
│   └── step7-final-system-template.md        # 完成システム
└── project-specific/                          # プロジェクト固有文書
    ├── project-overview.md                   # プロジェクト文書概要
    ├── augment-user-guidelines.md            # ユーザーガイドライン
    ├── design/                               # STEP 2: システム設計
    │   ├── system-architecture.md
    │   └── tech-stack.md
    ├── detailed-design/                      # STEP 3: 詳細設計
    │   ├── classes.md
    │   └── interfaces.md
    ├── requirements/                         # STEP 1: 要件定義
    │   ├── use-cases.md
    │   ├── non-functional.md
    │   └── specification.md
    ├── test-design/                          # STEP 4: テスト設計
    │   ├── strategy.md
    │   ├── targets.md
    │   └── test-cases.md
    ├── implementation/                       # STEP 5: 開発計画
    │   ├── components.md
    │   ├── schedule.md
    │   └── directory-structure.md
    ├── tasks/                                # STEP 6: ToDoリスト作成
    │   ├── task-list.md
    │   ├── task-management.md
    │   └── specifications/
    └── execution/                            # STEP 7: コーディング・テスト実行
        ├── progress-log.md
        ├── quality-records.md
        └── completion-report.md
```

[docs_project-overview]: /docs/project-specific/project-overview.md
[docs_document-format-specifications]: /docs/templates/document-format-specifications.md
[docs_cline-process-engineering-rules]: /docs/templates/cline-process-engineering-rules.md
[docs_cline-custom-instructions]: /docs/templates/cline-custom-instructions.md
[docs_human-vs-ai-coding-process-engineering-paper]: /docs/theory/human-vs-ai-coding-process-engineering-paper-v1.2.md
[docs_ai-coding-development-process]: /docs/theory/ai-coding-development-process-v1.3-part1.md
[docs_experimental-validation-report]: /docs/theory/experimental-validation-report.md
[docs_reproducibility-validation-plan]: /docs/theory/reproducibility-validation-plan.md
[docs_related-research-analysis]: /docs/theory/related-research-analysis.md
[docs_academic-publication-guide]: /docs/theory/academic-publication-guide.md

### ソースコード構造

```
src/
├── presentation/     # プレゼンテーション層
│   ├── controllers/  # REST APIコントローラ
│   └── dto/         # データ転送オブジェクト
├── application/     # アプリケーション層
│   ├── services/    # ビジネスロジック
│   └── usecases/    # ユースケース実装
├── domain/          # ドメイン層
│   ├── entities/    # エンティティ
│   └── repositories/ # リポジトリインターフェース
└── infrastructure/ # インフラ層
    ├── database/   # データベース実装
    └── external/   # 外部API連携
```

### テスト構造

```
tests/
├── unit/        # 単体テスト
├── integration/ # 結合テスト
└── e2e/         # E2Eテスト
```

## 配置済み文書の概要

### 1. 論文・研究文書
- **論文本体**: [段階的タスク管理アプローチによるAIコーディング手法の理論的基盤v1.2][docs_human-vs-ai-coding-process-engineering-paper]
- **プロセス体系文書**: [`docs/ai-coding-development-process-v1.3`（3分割）][docs_ai-coding-development-process]
- **実験検証レポート**: [`docs/experimental-validation-report.md`][docs_experimental-validation-report]

### 2. 検証・分析文書
- **再現性検証計画**: [`docs/reproducibility-validation-plan.md`][docs_reproducibility-validation-plan]
- **関連研究分析**: [`docs/related-research-analysis.md`][docs_related-research-analysis]
- **学術出版ガイド**: [`docs/academic-publication-guide.md`][docs_academic-publication-guide]

### 3. 実装支援文書
- **文書フォーマット仕様**: [`docs/document-format-specifications.md`][docs_document-format-specifications]
- **実装ルール**: [`docs/cline-process-engineering-rules.md`][docs_cline-process-engineering-rules]
- **カスタムインストラクション**: [`docs/cline-custom-instructions.md`][docs_cline-custom-instructions]

### 4. プロジェクト管理文書
- **プロジェクト文書概要**: [`docs/project-overview.md`][docs_project-overview]

## 検証目的

### 1. プロセス再現性の検証
- 7段階プロセスの完全実行
- 各段階での必須成果物作成
- 段階間の情報引き継ぎ確認
- 品質基準の達成確認

### 2. 文書フォーマット統一の検証
- 標準フォーマットへの準拠
- Mermaid記法の正しい使用
- メタデータセクションの完備
- 完了確認チェックリストの実装

### 3. ファイル単位タスク管理の検証
- タスクIDによる完全なトレーサビリティ
- 7つの標準サブタスクの実行
- Issue管理との統合
- 品質管理の自動化

### 4. 品質基準の検証
- テストカバレッジ90%以上の達成
- 静的解析エラー0件
- セキュリティ脆弱性0件
- 文書フォーマット準拠100%

### 5. 学術的価値の検証
- 論文手法の実用性証明
- 定量的な効果測定データの収集
- 学術論文としての発表準備

## 使用方法

### 1. 初期設定

```bash
# プロジェクトディレクトリに移動
cd ProcessEngineering-ValidationProject

# Git初期化
git status

# 文書確認
ls docs/
```

### 2. 理論理解

1. **論文本体**を読み、理論的基盤を理解
   - [`docs/human-vs-ai-coding-process-engineering-paper.md`][docs_human-vs-ai-coding-process-engineering-paper]
2. **関連研究分析**で学術的位置づけを確認
   - [`docs/related-research-analysis.md`][docs_related-research-analysis]
3. **プロセス体系文書**で実装詳細を把握
   - [`docs/ai-coding-development-process-v1.3`（3分割）][docs_ai-coding-development-process]

### 3. 実装準備

1. **文書フォーマット仕様**で標準化ルールを確認
   - [`docs/document-format-specifications.md`][docs_document-format-specifications]
2. **実装ルール**で詳細な実装方針を理解
   - [`docs/cline-process-engineering-rules.md`][docs_cline-process-engineering-rules]
3. **カスタムインストラクション**でAI設定を準備
   - [`docs/cline-custom-instructions.md`][docs_cline-custom-instructions]

### 4. Cline設定

1. [`docs/cline-custom-instructions.md`][docs_cline-custom-instructions]の内容をClineのカスタムインストラクションに設定
2. [`docs/cline-process-engineering-rules.md`][docs_cline-process-engineering-rules]を参照ルールとして設定
3. [`docs/document-format-specifications.md`][docs_document-format-specifications]を文書フォーマット仕様として設定

### 5. 検証実行

```
プロセスエンジニアリングアプローチを使用してソフトウェア開発を行います。

## 開発要求
シンプルなタスク管理システムを開発してください。
- ユーザーはタスクを作成、編集、削除できる
- タスクには優先度と期限を設定できる
- タスクの完了状況を管理できる

## 実行指示
1. 必ずSTEP 0から開始し、順次STEP 7まで実行してください
2. 各段階で必須成果物をすべて作成してください
3. 全文書は標準フォーマット（docs/document-format-specifications.md）に準拠してください
4. ファイル単位タスク管理を厳密に適用してください
5. 品質基準を満たすまで各段階を完了させないでください
6. Mermaid図は4つのバッククォート（````）でネストしてください
7. 全プロセスの実行状況を定期的に報告してください

開始してください。
```

### 6. 検証結果の分析

1. **再現性検証計画**に従って検証を実行
   - [`docs/reproducibility-validation-plan.md`][docs_reproducibility-validation-plan]
2. **実験検証レポート**と結果を比較
   - [`docs/experimental-validation-report.md`][docs_experimental-validation-report]
3. 新たな検証データを蓄積

### 7. 成果発表準備

1. **学術出版ガイド**に従って成果をまとめ
   - [`docs/academic-publication-guide.md`][docs_academic-publication-guide]
2. 論文として発表準備
3. 学術コミュニティへの貢献

## 検証項目

### プロセス実行チェックリスト

#### STEP 0: ゴール定義
- [ ] ゴールステートメント作成
- [ ] ステークホルダー一覧作成
- [ ] 制約条件リスト作成
- [ ] 標準フォーマット準拠確認

#### STEP 1: 要件定義
- [ ] ユースケース一覧作成
- [ ] 非機能要件リスト作成
- [ ] 要求仕様書作成
- [ ] Mermaid図の正しい使用確認

#### STEP 2: システム設計
- [ ] システム構成図作成
- [ ] 技術選定・依存関係定義書作成
- [ ] アーキテクチャ図の作成確認

#### STEP 3: 詳細設計
- [ ] クラス設計表作成
- [ ] メソッドI/Fリスト作成
- [ ] クラス図の作成確認

#### STEP 4: テスト設計
- [ ] テスト戦略書作成
- [ ] テスト対象一覧作成
- [ ] テストケース定義書作成

#### STEP 5: 開発計画
- [ ] 実装コンポーネント一覧作成
- [ ] 開発工程表作成
- [ ] ディレクトリ構造マップ作成

#### STEP 6: ToDoリスト作成
- [ ] ファイル単位タスクリスト作成
- [ ] タスク管理表作成
- [ ] Issue・仕様書セット作成

#### STEP 7: コーディング・テスト実行
- [ ] ファイル単位タスクの実行
- [ ] 7つの標準サブタスクの完全実行
- [ ] 品質管理・統合の実施

### 品質チェックリスト

#### 文書品質
- [ ] 全文書にメタデータセクション存在
- [ ] 完了確認チェックリスト存在
- [ ] Mermaid図の正しいネスト（4つのバッククォート）
- [ ] 表形式の統一
- [ ] トレーサビリティの確保

#### コード品質
- [ ] テストカバレッジ90%以上
- [ ] 静的解析エラー0件
- [ ] セキュリティ脆弱性0件
- [ ] パフォーマンス要件達成
- [ ] コーディング規約準拠

#### プロセス品質
- [ ] 段階的詳細化の実行
- [ ] ファイル単位タスク管理の実装
- [ ] Issue管理の統合
- [ ] 自動化チェックポイントの設定

#### 学術品質
- [ ] 論文理論との整合性確認
- [ ] 実験データの収集・分析
- [ ] 再現性の確保
- [ ] 学術発表準備の完了

## 期待される成果

### 1. 技術的成果
- 高品質なタスク管理システム
- 完全なテストスイート
- 自動化されたCI/CDパイプライン
- 包括的な技術文書

### 2. プロセス的成果
- 7段階プロセスの完全実行記録
- 標準フォーマットに準拠した文書群
- 完全なトレーサビリティマトリクス
- 再現可能な開発プロセス

### 3. 検証的成果
- 論文手法の実用性確認
- 品質向上効果の測定
- 開発効率の定量的評価
- 改善点の特定と記録

### 4. 学術的成果
- 論文手法の実用性証明
- 定量的な効果測定データ
- 学術論文としての発表
- AI開発手法の標準化への貢献

## 文書間の関連性

詳細な文書間の関連性については、`docs/project-overview.md`を参照してください。理論基盤、実装仕様、検証・評価の3つのカテゴリに分類された文書群が、どのように相互に関連し合っているかが可視化されています。

## 注意事項

1. **段階の飛び級禁止**: 必ずSTEP 0から順次実行
2. **成果物の省略禁止**: 各段階の必須成果物をすべて作成
3. **品質基準の妥協禁止**: 設定された品質基準を必ず達成
4. **文書フォーマットの遵守**: 標準フォーマットに完全準拠
5. **トレーサビリティの確保**: 全工程で完全な追跡可能性を維持
6. **学術的厳密性の維持**: 論文理論との整合性を常に確認

## プロジェクトの意義

このプロジェクトを通じて、プロセスエンジニアリング手法の有効性を技術的に検証し、論文の理論を実践で証明します。さらに、得られた成果を学術論文として発表することで、AI開発手法の標準化と学術コミュニティへの貢献を目指します。

**検証環境**: 完全に構築済み
**文書体系**: 理論・実装・検証・発表の包括的文書群
**品質保証**: 自動化チェックと手動検証の統合
**学術価値**: 国際会議・ジャーナル発表レベルの研究基盤

## ライセンス

このプロジェクトは [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/) の下で公開されています。

### 利用条件
- ✅ **学術研究・教育目的での利用**: 自由に利用可能
- ✅ **改変・再配布**: 同じライセンス条件下で可能
- ✅ **引用**: 適切な引用を行えば利用可能
- ❌ **商用利用**: 禁止

詳細は [COPYRIGHT.md](COPYRIGHT.md) をご確認ください。
