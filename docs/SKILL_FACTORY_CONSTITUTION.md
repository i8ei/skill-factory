# Skill Factory 憲法 (Skill Factory Constitution)

Skill Factory は、AIエージェントの「スキル」を作成、維持、進化させるための標準化された環境です。「スキル」とは、指示書（`SKILL.md`）とリソースがセットになった自己完結型のパッケージを指します。

## 1. スキル構造 (Skill Structure)

すべてのスキルは `skills/<skill_id>/` に配置し、少なくとも以下を含む必要があります：

- `SKILL.md`: 定義ファイル。YAMLフロントマター（name, description）とMarkdown形式の指示を含まなければなりません。
- `README.md`（任意）: 人間向けの公開ドキュメント。

## 2. 工場のライフサイクル (The Factory Lifecycle)

1.  **探索 (Scout)**: 新しいスキルを作る前に、既存のものを探します。
2.  **輸入/作成 (Import/Create)**: 素材を持ち込むか、新しいロジックを起草します。
3.  **リント (Lint)**: この憲法（メタデータ、フォーマット）に準拠しているか確認します。
4.  **テスト (Test)**: 特定のプロンプトやケースで機能を検証します。
5.  **カタログ登録 (Catalog)**: 工場の目録にスキルを登録します。
6.  **パッチ (Patch)**: 利用ログ（Evolution Logs）を通じてスキルを進化させます。

## 3. 「摩擦」ルール (The "Friction" Rule)

- 些細なタスクのために新しいスキルを作らないでください。
- タスクが2〜3回繰り返され「摩擦」を感じるようになったら、スキル化を検討してください。

## 4. 調達プロトコル (Procurement Protocol)

- **まず探索 (Scout First)**: 何かを作る前に、必ず `skill_scout_web` を実行してください。
- **自己改善 (Self-Improvement)**: 工場自体に能力が欠けている場合は、`factory_kaizen_architect` に依頼してください。
- **輸入優先 (Import Priority)**:
  1.  似たものがある？ -> 輸入 -> 隔離（リント/テスト） -> パッチ適用。
  2.  なければ？ -> 新規作成。

- **摩擦ルール**: 摩擦が2〜3回 -> 新規スキル作成。

## 5. 製品分離ルール (Infrastructure vs. Product)

- **工場インフラ**: `skill factory/skills/` 内のスキルは、工場自体を運営する「メタスキル」（Core, QA, Procurement, Distribution）に限定されます。
- **製品インキュベーション (Workbench)**: **新しいスキルパックは `workbench/` で開発しなければなりません。**
  - メインの `skills/` ディレクトリを作りかけの作業で汚さないでください。
  - `workbench/` 内のスキルチェックには `skill_linter_auditor` を使用してください。
- **製品エクスポート**: 完成したパックは、独立したリポジトリにエクスポート**しなければなりません**。
  - `job_pack_composer` を使用して `workbench/` から外部へ移動させてください。

## 6. 製品構成ルール ("Life" Rule)

- **自己改善の義務化**: この工場で生産されるすべての製品（スキルパック）には、「カイゼンスキル（自己改善）」を含めなければなりません\*\*。
  - 製品は、ユーザーのペインポイントを分析し、自分自身に対する改善を提案できなければなりません。
  - 例: `99_activity_kaizen`, `99_project_retrospective`.

## 7. 言語標準化ルール (Language Standardization Rule - Japanese First)

- **対話言語**: Skill Factory 内でのすべてのやり取りは **日本語**で行わなければなりません。
- **アーティファクト言語**: すべての `SKILL.md`、`README.md`、および生成されるアーティファクトは、ユーザーの可読性を確保するため **日本語** で記述しなければなりません。
- **製品の出力**: 作成されたスキルが生成する成果物や応答も、原則として **日本語** である必要があります。
- **例外**: 技術用語、変数名、コード識別子などは英語（snake_case, camelCase 等）のままで構いません。

## 8. 製造プロセスルール (Manufacturing Process Rule)

高品質なスキルを製造するため、以下の工程を遵守しなければなりません：

1.  **設計 (Architecture)**: `skill_specificator_architect` を使用し、曖昧な要望を具体的な仕様書にします。
2.  **承認 (Approval)**: 製造前に必ず仕様書（プラン）についてユーザーの**承認 (LGTM)**を得ます。無断で製造してはいけません。
3.  **製造 (Fabrication)**: `universal_skill_factory` の規格に従ってファイルを生成します。この際、自己改善スキル (`99_activity_kaizen`) を必ず同梱します（第6条）。
4.  **検査 (Inspection)**: 製造後直ちに `skill_linter_auditor`（検品）と `skill_test_generator`（試験設計）を実行し、品質を保証します。
