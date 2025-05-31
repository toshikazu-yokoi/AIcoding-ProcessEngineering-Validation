# プロセスエンジニアリング テンプレート集

## 概要

このディレクトリには、「プロセスエンジニアリングfor AIコーディング」で定義される7段階すべての文書テンプレートが含まれています。各テンプレートは標準化されたフォーマットに従い、実際のプロジェクトで即座に使用できるように設計されています。

## テンプレート一覧

### STEP 0: ゴール定義文書
| ファイル名 | 用途 | 説明 |
|------------|------|------|
| [step0-goal-statement-template.md](step0-goal-statement-template.md) | ゴールステートメント | プロジェクトの目的と成功の定義 |
| [step0-stakeholders-template.md](step0-stakeholders-template.md) | ステークホルダー一覧 | 関係者の特定とコミュニケーション計画 |
| [step0-constraints-template.md](step0-constraints-template.md) | 制約条件リスト | 技術・運用・リソース・時間制約 |

### STEP 1: 要件定義文書
| ファイル名 | 用途 | 説明 |
|------------|------|------|
| [step1-use-cases-template.md](step1-use-cases-template.md) | ユースケース一覧 | アクター定義とユースケース詳細 |
| [step1-non-functional-template.md](step1-non-functional-template.md) | 非機能要件リスト | 性能・可用性・セキュリティ要件 |
| [step1-requirements-specification-template.md](step1-requirements-specification-template.md) | 要求仕様書 | 機能要件とインターフェース要件 |

### STEP 2: システム設計文書
| ファイル名 | 用途 | 説明 |
|------------|------|------|
| [step2-system-architecture-template.md](step2-system-architecture-template.md) | システム構成図 | 全体アーキテクチャとレイヤー構成 |
| [step2-tech-stack-template.md](step2-tech-stack-template.md) | 技術選定・依存関係定義書 | 技術スタックと依存関係管理 |

### STEP 3: 詳細設計文書
| ファイル名 | 用途 | 説明 |
|------------|------|------|
| [step3-class-design-template.md](step3-class-design-template.md) | クラス設計表 | クラス一覧と詳細設計 |
| [step3-interfaces-template.md](step3-interfaces-template.md) | メソッドインターフェースリスト | メソッドシグネチャと処理フロー |

### STEP 4: テスト設計文書
| ファイル名 | 用途 | 説明 |
|------------|------|------|
| [step4-test-strategy-template.md](step4-test-strategy-template.md) | テスト戦略書 | テスト方針と品質基準 |
| [step4-test-targets-template.md](step4-test-targets-template.md) | テスト対象一覧 | 単体・結合・E2Eテスト対象 |
| [step4-test-cases-template.md](step4-test-cases-template.md) | テストケース定義書 | 具体的なテストケースと実装例 |

### STEP 5: 開発計画文書
| ファイル名 | 用途 | 説明 |
|------------|------|------|
| [step5-components-template.md](step5-components-template.md) | 実装コンポーネント一覧 | コンポーネント分類と実装順序 |
| [step5-schedule-template.md](step5-schedule-template.md) | 開発工程表 | スケジュールとリスク管理 |
| [step5-directory-structure-template.md](step5-directory-structure-template.md) | ディレクトリ構造マップ | プロジェクト構造と命名規則 |

### STEP 6: ToDoリスト作成文書
| ファイル名 | 用途 | 説明 |
|------------|------|------|
| [step6-todo-list-template.md](step6-todo-list-template.md) | ToDoリストテンプレート | 段階的タスク管理対応のToDoリスト |
| [step6-todo-creation-guide.md](step6-todo-creation-guide.md) | ToDoリスト作成ガイド | 効果的なToDoリスト作成の手順 |
| [step6-task-list-template.md](step6-task-list-template.md) | ファイル単位タスクリスト | タスク一覧と依存関係 |
| [step6-task-management-template.md](step6-task-management-template.md) | タスク管理表 | Issue管理と標準サブタスク |
| [step6-task-specification-template.md](step6-task-specification-template.md) | タスク仕様書 | 個別タスクの詳細仕様 |

### STEP 7: コーディング・テスト実行文書
| ファイル名 | 用途 | 説明 |
|------------|------|------|
| [step7-progress-template.md](step7-progress-template.md) | 実行ログ・進捗管理 | 日次進捗と課題管理 |
| [step7-deliverables-template.md](step7-deliverables-template.md) | 成果物・品質記録 | 成果物一覧と品質分析 |
| [step7-final-system-template.md](step7-final-system-template.md) | 完成システム | システム概要と運用計画 |

### 共通テンプレート
| ファイル名 | 用途 | 説明 |
|------------|------|------|
| [document-format-specifications.md](document-format-specifications.md) | 文書フォーマット仕様書 | 全文書の標準フォーマット定義 |
| [header-template.md](header-template.md) | ヘッダーテンプレート | 文書ヘッダーの標準形式 |
| [cline-custom-instructions.md](cline-custom-instructions.md) | Clineカスタム指示 | AI開発支援の設定 |
| [cline-process-engineering-rules.md](cline-process-engineering-rules.md) | プロセスエンジニアリング規則 | 開発プロセスの標準化 |

## 使用方法

### 1. テンプレート選択
プロジェクトの段階に応じて、必要なSTEPのテンプレートを選択してください。

### 2. ファイルコピー
テンプレートファイルをプロジェクトディレクトリにコピーし、適切な名前に変更してください。

### 3. 内容カスタマイズ
`[項目名]`、`YYYY-MM-DD`、`[説明]`などのプレースホルダーを実際の内容に置き換えてください。

### 4. 完了確認
各テンプレートの「完了確認」セクションのチェックリストを使用して、文書の完成度を確認してください。

## 命名規則

### ファイル命名
```
{step番号}-{文書種別}-{プロジェクト名}.md
```

例：
- `step1-use-cases-user-management.md`
- `step3-class-design-payment-system.md`

### ドキュメントID
```
{文書種別}-{連番3桁}
```

例：
- `UC-001` (ユースケース)
- `CLASS-001` (クラス設計)
- `TEST-001` (テスト戦略)

## 品質基準

### 必須要素
- [ ] メタデータセクションの完全記入
- [ ] 関連文書の適切な参照
- [ ] 完了確認チェックリストの実行
- [ ] 図表の適切な配置

### 推奨要素
- [ ] Mermaid図による視覚化
- [ ] 具体的な実装例の提供
- [ ] 定量的な基準の設定
- [ ] トレーサビリティの確保

## 更新履歴

| 日付 | バージョン | 変更内容 | 担当者 |
|------|------------|----------|--------|
| 2025-05-28 | 1.0.0 | 初版作成 | [担当者] |

## 関連リソース

- [プロセスエンジニアリング理論文書](../theory/)
- [プロジェクト固有文書](../project-specific/)
- [document-format-specifications.md](document-format-specifications.md) - 詳細なフォーマット仕様
