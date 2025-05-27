# Cline用カスタムインストラクション：プロセスエンジニアリング実装（更新版）

## 概要

このカスタムインストラクションは、Cline AIエージェントが「プロセスエンジニアリングアプローチによるAIコーディング手法」を自動的に適用するための設定です。

論文の理論を実際のソフトウェア開発で再現し、その有効性を検証するために使用します。

**文書フォーマット統合**: 本インストラクションは、`docs/document-format-specifications-fixed.md`で定義された標準フォーマットと、`docs/cline-process-engineering-rules-updated.md`で定義された実装ルールを統合しています。

## カスタムインストラクション設定

### システムプロンプト（System Prompt）

```
あなたは、プロセスエンジニアリングアプローチを専門とするソフトウェア開発エージェントです。

## 基本動作原則

1. **段階的詳細化の徹底**
   - 必ず7段階のプロセス（STEP 0-7）を順次実行する
   - 各段階で前段階の成果物を必ずインプットとして使用する
   - 段階の飛び級や省略は絶対に行わない

2. **ファイル単位タスク管理**
   - すべてのコーディング作業をファイル単位で分割する
   - 各ファイルに対して7つの標準サブタスクを適用する
   - タスクIDによる完全なトレーサビリティを確保する

3. **品質保証の統合**
   - 各段階で品質チェックポイントを設定する
   - 自動化可能な品質管理は必ず自動化する
   - 品質基準（テストカバレッジ90%以上等）を厳守する

4. **文書フォーマット統一**
   - 全文書は標準フォーマット（docs/document-format-specifications-fixed.md）に準拠
   - メタデータセクション、完了確認チェックリストを必ず含める
   - Mermaid記法を使用した図表作成（4つのバッククォートでネスト）
   - トレーサビリティマトリクスの維持

## 必須実行プロセス

### STEP 0: ゴール定義
**必須成果物**:
- ゴールステートメント作成（docs/goal-statement.md）
- ステークホルダー一覧作成（docs/stakeholders.md）
- 制約条件リスト作成（docs/constraints.md）

**文書フォーマット要件**:
- メタデータセクション（ドキュメントID、作成日、関連文書）
- 標準テーブル形式でのプロジェクト概要
- 完了確認チェックリスト

### STEP 1: 要件定義
**必須成果物**:
- ユースケース一覧作成（docs/requirements/use-cases.md）
- 非機能要件リスト作成（docs/requirements/non-functional.md）
- 要求仕様書作成（docs/requirements/specification.md）

**文書フォーマット要件**:
- ユースケース関係図（Mermaid記法）
- アクター定義・ユースケース一覧（表形式）
- データ関係図（ER図、Mermaid記法）

### STEP 2: システム設計
**必須成果物**:
- システム構成図作成（docs/design/system-architecture.md）
- 技術選定・依存関係定義書作成（docs/design/tech-stack.md）

**文書フォーマット要件**:
- システム全体アーキテクチャ図（Mermaid記法）
- コンポーネント構成図（Mermaid記法）
- 技術選定表（標準表形式）

### STEP 3: 詳細設計
**必須成果物**:
- クラス設計表作成（docs/detailed-design/classes.md）
- メソッドI/Fリスト作成（docs/detailed-design/interfaces.md）

**文書フォーマット要件**:
- クラス依存関係図（Mermaid記法）
- インターフェース仕様表（標準表形式）
- TypeScript形式でのメソッドシグネチャ

### STEP 4: テスト設計
**必須成果物**:
- テスト戦略書作成（docs/test-design/strategy.md）
- テスト対象一覧作成（docs/test-design/targets.md）
- テストケース定義書作成（docs/test-design/test-cases.md）

**文書フォーマット要件**:
- テストケース表（標準表形式）
- カバレッジ目標の定量的設定

### STEP 5: 開発計画
**必須成果物**:
- 実装コンポーネント一覧作成（docs/implementation/components.md）
- 開発工程表作成（docs/implementation/schedule.md）
- ディレクトリ構造マップ作成（docs/implementation/directory-structure.md）

**文書フォーマット要件**:
- ディレクトリ構造（ツリー形式）
- 工程表（表形式）

### STEP 6: ToDoリスト作成
**必須成果物**:
- ファイル単位タスクリスト作成（docs/tasks/task-list.md）
- タスク管理表作成（docs/tasks/task-management.md）
- Issue・仕様書セット作成（docs/tasks/specifications/）

**文書フォーマット要件**:
- タスクリスト（標準表形式）
- 統一されたタスクID命名規則
- 各タスクの詳細仕様書

### STEP 7: コーディング・テスト実行
**必須成果物**:
- ファイル単位タスクの実行
- 7つの標準サブタスクの完全実行
- 品質管理・統合の実施

**文書フォーマット要件**:
- 実行ログ・進捗管理文書
- 成果物・品質記録文書
- 完成システム文書

## ファイル単位タスク管理ルール

### タスクID命名規則
形式: TSK-{連番3桁}-{レイヤー}-{ファイル名}

レイヤー略語:
- CTL: Controller
- SVC: Service
- ENT: Entity
- REP: Repository
- DTO: Data Transfer Object
- UTL: Utility

### 7つの標準サブタスク
1. **仕様確認**: 詳細設計文書、インターフェース仕様書の参照
2. **コーディング**: クラス設計表、メソッドI/Fリストに基づく実装
3. **テストコーディング**: テストケース定義書に基づくテスト作成
4. **単体テスト実行**: テスト戦略書に基づく実行・検証
5. **リポジトリコミット**: コミットメッセージ規約の遵守
6. **ToDoチェック**: タスク管理表の更新
7. **Issueクローズ**: Issue管理テンプレートに基づく完了処理

## 文書作成時の必須チェック項目

### 1. メタデータセクション
- [ ] ドキュメントIDの付与
- [ ] 作成日・更新日の記録
- [ ] 関連文書への参照
- [ ] 作成者・レビュー者の明記

### 2. 構造化
- [ ] 必須セクションの完備
- [ ] 階層構造の適切な使用（H1-H6）
- [ ] 表形式の統一
- [ ] 図表の適切な配置

### 3. 図表作成
- [ ] Mermaid記法の正しい使用
- [ ] 4つのバッククォート（````）でのネスト
- [ ] 図表とテキストの明確な分離
- [ ] 図表の説明文の追加

### 4. 品質保証
- [ ] 完了確認チェックリストの追加
- [ ] トレーサビリティの確保
- [ ] 前段階文書との整合性確認
- [ ] 次段階への引き継ぎ情報の明記

## 品質基準

### 必須品質基準
- テストカバレッジ: 90%以上
- 静的解析: エラー0件
- セキュリティ: 脆弱性0件
- パフォーマンス: 応答時間<200ms
- 可用性: 99.9%以上
- 文書品質: フォーマット準拠100%

### Issue管理
- タイトル形式: [TSK-XXX-XXX-FileName] ファイル名の実装
- 必須セクション: 概要、実装仕様、参照文書、テスト要件、完了条件
- 参照文書の明記: 詳細設計書、インターフェース仕様書、テストケース定義書
- ラベル設定: feature, layer, priority, size

### コミットメッセージ規約
形式: {type}(#{issue_number}): {概要}

タイプ:
- feat: 新機能実装
- fix: バグ修正
- test: テストコード追加
- refactor: リファクタリング
- docs: ドキュメント更新

## 禁止事項

1. プロセスの段階飛ばし
2. 成果物の省略
3. 品質基準の妥協
4. トレーサビリティの欠如
5. ファイル単位タスク管理の簡略化
6. 文書フォーマットの基本構造変更
7. 標準テンプレートの無視

## 実行確認

各段階完了時に以下を確認:
- 必須成果物の作成完了
- 標準フォーマット準拠確認
- 品質基準の達成
- 次段階への引き継ぎ情報の準備
- トレーサビリティマトリクスの更新
- 文書間整合性の確認

## 参照文書

実装時は以下の文書を必ず参照:
- docs/document-format-specifications-fixed.md（文書フォーマット仕様）
- docs/cline-process-engineering-rules-updated.md（実装ルール詳細）

このプロセスを厳密に遵守し、論文で提示された手法の完全な再現を実現してください。
```

### ユーザープロンプト（User Prompt）

```
プロセスエンジニアリングアプローチを使用してソフトウェア開発を行います。

## 開発要求
[ここにプロジェクトの要求を記述]

## 実行指示
1. 必ずSTEP 0から開始し、順次STEP 7まで実行してください
2. 各段階で必須成果物をすべて作成してください
3. 全文書は標準フォーマット（docs/document-format-specifications-fixed.md）に準拠してください
4. ファイル単位タスク管理を厳密に適用してください
5. 品質基準を満たすまで各段階を完了させないでください
6. Mermaid図は4つのバッククォート（````）でネストしてください
7. 全プロセスの実行状況を定期的に報告してください

## 文書作成要件
- メタデータセクションを必ず含める
- 完了確認チェックリストを各文書に追加
- トレーサビリティマトリクスを維持
- 図表はMermaid記法で統一

## 期待する成果
- 7段階プロセスの完全実行
- 標準フォーマットに準拠した文書群
- 高品質なソフトウェアシステム
- 完全なトレーサビリティ
- 再現可能な開発プロセス

開始してください。
```

## 実装支援設定

### VSCode設定（settings.json）

```json
{
  "cline.processEngineering.enabled": true,
  "cline.processEngineering.strictMode": true,
  "cline.processEngineering.documentFormat": {
    "specificationFile": "docs/document-format-specifications-fixed.md",
    "enforceFormat": true,
    "mermaidNesting": "quadruple-backticks"
  },
  "cline.processEngineering.qualityGates": {
    "testCoverage": 90,
    "staticAnalysis": "error-free",
    "security": "vulnerability-free",
    "documentFormat": "100-percent-compliant"
  },
  "cline.processEngineering.taskManagement": {
    "fileBasedTasks": true,
    "standardSubtasks": 7,
    "traceabilityRequired": true,
    "issueTemplateRequired": true
  },
  "cline.processEngineering.documentation": {
    "autoGenerate": true,
    "templates": "process-engineering",
    "outputPath": "docs/",
    "formatValidation": true
  }
}
```

### プロジェクトテンプレート（更新版）

```
project-root/
├── docs/
│   ├── document-format-specifications-fixed.md    # 文書フォーマット仕様
│   ├── cline-process-engineering-rules-updated.md # 実装ルール
│   ├── goal-statement.md                          # STEP 0
│   ├── stakeholders.md
│   ├── constraints.md
│   ├── requirements/                              # STEP 1
│   │   ├── use-cases.md
│   │   ├── non-functional.md
│   │   └── specification.md
│   ├── design/                                    # STEP 2
│   │   ├── system-architecture.md
│   │   └── tech-stack.md
│   ├── detailed-design/                           # STEP 3
│   │   ├── classes.md
│   │   └── interfaces.md
│   ├── test-design/                               # STEP 4
│   │   ├── strategy.md
│   │   ├── targets.md
│   │   └── test-cases.md
│   ├── implementation/                            # STEP 5
│   │   ├── components.md
│   │   ├── schedule.md
│   │   └── directory-structure.md
│   ├── tasks/                                     # STEP 6
│   │   ├── task-list.md
│   │   ├── task-management.md
│   │   └── specifications/
│   ├── execution/                                 # STEP 7
│   │   ├── progress-log.md
│   │   ├── quality-records.md
│   │   └── completion-report.md
│   └── traceability-matrix.md                     # 全体
├── src/
├── tests/
├── .github/
│   └── workflows/
│       └── ci.yml
├── package.json
├── tsconfig.json
├── jest.config.js
└── README.md
```

## 自動化スクリプト

### プロジェクト初期化スクリプト（init-project.sh）

```bash
#!/bin/bash

# プロセスエンジニアリングプロジェクト初期化スクリプト（更新版）

echo "プロセスエンジニアリングプロジェクトを初期化しています..."

# ディレクトリ構造作成
mkdir -p docs/{requirements,design,detailed-design,test-design,implementation,tasks/specifications,execution}
mkdir -p src/{presentation,application,domain,infrastructure}
mkdir -p tests/{unit,integration,e2e}
mkdir -p .github/workflows

# 必須ファイル作成
touch docs/goal-statement.md
touch docs/stakeholders.md
touch docs/constraints.md
touch docs/traceability-matrix.md

# 文書フォーマット仕様とルールファイルをコピー
cp templates/process-engineering/document-format-specifications-fixed.md docs/
cp templates/process-engineering/cline-process-engineering-rules-updated.md docs/

# テンプレートファイルコピー
cp templates/process-engineering/templates/* docs/

# 設定ファイル作成
cat > .cline-config.json << EOF
{
  "processEngineering": {
    "enabled": true,
    "documentFormat": "docs/document-format-specifications-fixed.md",
    "implementationRules": "docs/cline-process-engineering-rules-updated.md",
    "strictMode": true
  }
}
EOF

# Git初期化
git init
git add .
git commit -m "feat: プロセスエンジニアリングプロジェクト初期化（文書フォーマット統合版）"

echo "初期化完了。文書フォーマット仕様とルールファイルが配置されました。"
echo "STEP 0から開始してください。"
```

### 文書フォーマットチェックスクリプト（format-check.js）

```javascript
// 文書フォーマットチェックスクリプト

const fs = require('fs');
const path = require('path');

class DocumentFormatChecker {
  constructor() {
    this.results = {
      checkedFiles: [],
      errors: [],
      warnings: [],
      passed: 0,
      failed: 0,
      timestamp: new Date().toISOString()
    };
  }

  // メタデータセクションチェック
  checkMetadata(content, filePath) {
    const errors = [];
    
    // ドキュメントIDの存在確認
    if (!content.includes('ドキュメントID')) {
      errors.push(`${filePath}: ドキュメントIDが見つかりません`);
    }
    
    // 作成日の存在確認
    if (!content.includes('作成日')) {
      errors.push(`${filePath}: 作成日が見つかりません`);
    }
    
    // 関連文書の存在確認（STEP 1以降）
    if (filePath.includes('requirements/') || filePath.includes('design/') || 
        filePath.includes('detailed-design/') || filePath.includes('test-design/') ||
        filePath.includes('implementation/') || filePath.includes('tasks/')) {
      if (!content.includes('関連文書')) {
        errors.push(`${filePath}: 関連文書への参照が見つかりません`);
      }
    }
    
    return errors;
  }

  // Mermaid記法チェック
  checkMermaidFormat(content, filePath) {
    const errors = [];
    const mermaidBlocks = content.match(/```mermaid[\s\S]*?```/g) || [];
    
    mermaidBlocks.forEach((block, index) => {
      // 4つのバッククォートでネストされているかチェック
      const surroundingContext = content.substring(
        content.indexOf(block) - 100,
        content.indexOf(block) + block.length + 100
      );
      
      if (!surroundingContext.includes('````')) {
        errors.push(`${filePath}: Mermaid図${index + 1}が4つのバッククォートでネストされていません`);
      }
    });
    
    return errors;
  }

  // 完了確認チェックリストチェック
  checkCompletionChecklist(content, filePath) {
    const errors = [];
    
    if (!content.includes('完了確認') && !content.includes('チェック')) {
      errors.push(`${filePath}: 完了確認チェックリストが見つかりません`);
    }
    
    // チェックボックス形式の確認
    const checkboxPattern = /- \[ \]/g;
    const checkboxes = content.match(checkboxPattern);
    
    if (!checkboxes || checkboxes.length === 0) {
      errors.push(`${filePath}: チェックボックス形式のリストが見つかりません`);
    }
    
    return errors;
  }

  // 表形式チェック
  checkTableFormat(content, filePath) {
    const errors = [];
    const tablePattern = /\|.*\|/g;
    const tables = content.match(tablePattern);
    
    if (filePath.includes('use-cases.md') || filePath.includes('tech-stack.md') || 
        filePath.includes('classes.md') || filePath.includes('interfaces.md')) {
      if (!tables || tables.length < 3) {
        errors.push(`${filePath}: 必須の表形式が不足しています`);
      }
    }
    
    return errors;
  }

  // 単一ファイルチェック
  checkFile(filePath) {
    try {
      const content = fs.readFileSync(filePath, 'utf8');
      const errors = [];
      
      // 各種チェック実行
      errors.push(...this.checkMetadata(content, filePath));
      errors.push(...this.checkMermaidFormat(content, filePath));
      errors.push(...this.checkCompletionChecklist(content, filePath));
      errors.push(...this.checkTableFormat(content, filePath));
      
      this.results.checkedFiles.push(filePath);
      
      if (errors.length > 0) {
        this.results.errors.push(...errors);
        this.results.failed++;
      } else {
        this.results.passed++;
      }
      
      return errors;
    } catch (error) {
      const errorMsg = `${filePath}: ファイル読み込みエラー - ${error.message}`;
      this.results.errors.push(errorMsg);
      this.results.failed++;
      return [errorMsg];
    }
  }

  // ディレクトリ内の全Markdownファイルをチェック
  checkDirectory(dirPath) {
    if (!fs.existsSync(dirPath)) {
      console.log(`ディレクトリが存在しません: ${dirPath}`);
      return;
    }
    
    const files = fs.readdirSync(dirPath, { withFileTypes: true });
    
    files.forEach(file => {
      const fullPath = path.join(dirPath, file.name);
      
      if (file.isDirectory()) {
        this.checkDirectory(fullPath);
      } else if (file.name.endsWith('.md')) {
        this.checkFile(fullPath);
      }
    });
  }

  // 全文書チェック実行
  runAllChecks() {
    console.log('文書フォーマットチェックを開始します...');
    
    // docsディレクトリ内の全Markdownファイルをチェック
    this.checkDirectory('docs');
    
    this.generateReport();
    
    if (this.results.failed === 0) {
      console.log('✅ 全文書が標準フォーマットに準拠しています');
      return true;
    } else {
      console.log(`❌ ${this.results.failed}個のファイルでフォーマット違反が検出されました`);
      return false;
    }
  }

  // フォーマットチェックレポート生成
  generateReport() {
    const report = `
# 文書フォーマットチェックレポート

## 実行日時
${this.results.timestamp}

## チェック結果サマリ
- **チェック対象ファイル数**: ${this.results.checkedFiles.length}
- **準拠ファイル数**: ${this.results.passed}
- **違反ファイル数**: ${this.results.failed}
- **総合判定**: ${this.results.failed === 0 ? '✅ PASS' : '❌ FAIL'}

## チェック対象ファイル
${this.results.checkedFiles.map(file => `- ${file}`).join('\n')}

## 検出されたエラー
${this.results.errors.length > 0 ? 
  this.results.errors.map(error => `- ${error}`).join('\n') : 
  '✅ エラーは検出されませんでした'}

## 改善推奨事項
${this.results.failed > 0 ? `
1. docs/document-format-specifications-fixed.md を参照して標準フォーマットを確認
2. メタデータセクションの追加
3. Mermaid図の4つのバッククォートでのネスト
4. 完了確認チェックリストの追加
5. 必須表形式の実装
` : '✅ 全文書が標準フォーマットに準拠しています'}
`;

    fs.writeFileSync('docs/format-check-report.md', report);
    return report;
  }
}

module.exports = DocumentFormatChecker;

// 直接実行時の処理
if (require.main === module) {
  const checker = new DocumentFormatChecker();
  const success = checker.runAllChecks();
  process.exit(success ? 0 : 1);
}
```

### タスク管理スクリプト（manage-tasks.js）

```javascript
// ファイル単位タスク管理スクリプト（更新版）

const fs = require('fs');
const path = require('path');

class TaskManager {
  constructor() {
    this.tasks = [];
    this.taskIdCounter = 1;
    this.documentFormatSpec = 'docs/document-format-specifications-fixed.md';
    this.implementationRules = 'docs/cline-process-engineering-rules-updated.md';
  }

  // ファイル単位タスク作成（文書フォーマット統合版）
  createFileTask(filePath, layer, dependencies = []) {
    const taskId = `TSK-${String(this.taskIdCounter).padStart(3, '0')}-${layer}-${path.basename(filePath, path.extname(filePath))}`;
    
    const task = {
      id: taskId,
      filePath,
      layer,
      dependencies,
      subtasks: [
        '1. 仕様確認（詳細設計文書、インターフェース仕様書の参照）',
        '2. コーディング（クラス設計表、メソッドI/Fリストに基づく実装）',
        '3. テストコーディング（テストケース定義書に基づくテスト作成）',
        '4. 単体テスト実行（テスト戦略書に基づく実行・検証）',
        '5. リポジトリコミット（コミットメッセージ規約の遵守）',
        '6. ToDoチェック（タスク管理表の更新）',
        '7. Issueクローズ（Issue管理テンプレートに基づく完了処理）'
      ],
      status: 'pending',
      createdAt: new Date().toISOString(),
      documentReferences: {
        formatSpec: this.documentFormatSpec,
        implementationRules: this.implementationRules
      }
    };

    this.tasks.push(task);
    this.taskIdCounter++;
    
    return task;
  }

  // Issue作成（文書フォーマット統合版）
  createIssue(task) {
    const issueContent = `
# [${task.id}] ${path.basename(task.filePath)}の実装

## メタデータ
| 項目 | 内容 |
|------|------|
| タスクID | ${task.id} |
| 作成日 | ${task.createdAt} |
| 対象ファイル | ${task.filePath} |
| レイヤー | ${task.layer} |

## 概要
${task.filePath}の実装

## 実装仕様
### 対象ファイル
- ${task.filePath}

### 依存関係
${task.dependencies.map(dep => `- ${dep}`).join('\n')}

### 参照文書
- [ ] 文書フォーマット仕様: ${task.documentReferences.formatSpec}
- [ ] 実装ルール: ${task.documentReferences.implementationRules}
- [ ] 詳細設計書: docs/detailed-design/classes.md
- [ ] インターフェース仕様書: docs/detailed-design/interfaces.md
- [ ] テストケース定義書: docs/test-design/test-cases.md

## テスト要件
### 必要なテストケース
- [ ] 正常系テスト
- [ ] 異常系テスト
- [ ] 境界値テスト
- [ ] パフォーマンステスト

## 完了条件
- [ ] 全メソッドの実装完了
- [ ] 単体テスト90%以上カバレッジ
- [ ] コーディング規約準拠
- [ ] 設計仕様への適合
- [ ] 文書フォーマット準拠
- [ ] レビュー完了

## サブタスク
${task.subtasks.map((subtask, index) => `- [ ] ${subtask}`).join('\n')}

## 品質チェック項目
- [ ] 静的解析エラー0件
- [ ] セ
