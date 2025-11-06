# Databricks

## 参考資料

- [公式チュートリアル](https://docs.databricks.com/aws/ja/getting-started)
-
-
-
-
-
-
-


## 専門用語集

- **Medallion Architecture**

    レイクハウス内のデータを論理的に整理するためのデータ設計パターン。データ品質を段階的に向上させるために、データを3つの層（Bronze, Silver, Gold）に分類します。マルチホップ・アーキテクチャとも呼ばれます。

- **Bronze Layer**

    Medallion Architecture の最初の層。外部ソースから取り込まれた未加工（Raw）データがそのまま保存されます。データの完全性と監査可能性を維持することが目的です。

- **Silver Layer**

    Medallion Architecture の中間層。ブロンズ層のデータに対して、クレンジング、フィルタリング、検証、重複排除、データ結合などが行われ、信頼性の高いデータセットが作成されます。

- **Gold Layer**

    Medallion Architecture の最終層。ビジネスユーザーが分析、BI（ビジネスインテリジェンス）、または機械学習などにすぐに利用できるよう、集計やビジネスロジックが適用されたデータが格納されます。

- **Databricks Lakehouse Platform**

    データレイクとデータウェアハウスの利点を統合した Databricks のアーキテクチャ。  
    データガバナンスとセキュリティを備え、構造化・非構造化データを扱うことができます。

- **Unity Catalog**

    Databricks Lakehouse Platform 全体で、データ、分析、機械学習ワークロードに対して集中型ガバナンス、きめ細かなアクセス制御、および監査を提供するソリューション。

- **Delta Lake**

    データレイク上に信頼性、セキュリティ、パフォーマンスを提供するために設計されたオープンソースのストレージレイヤー。ACIDトランザクション、スケーラブルなメタデータ処理、データバージョン管理などを可能にします。

- **Spark**

    大規模なデータ処理のためのオープンソースの分散コンピューティングシステム。  
    Databricks の基盤技術の一つです。

- **Databricks Runtime**

    Databricks によって管理・最適化された Apache Spark 環境。  
    パフォーマンス、セキュリティ、互換性を強化するための追加コンポーネントを含みます。

- **Notebooks**

    コード、視覚化、および散文を組み合わせることができる対話型のウェブベースのインターフェース。  
    データ分析、機械学習、データ処理などで使用されます。

- **Cluster/Compute**

    ノートブックやジョブの実行に使用されるコンピューティングリソース。  
    以前は「クラスター」と呼ばれていましたが、UI全体で「コンピュート」に置き換わっています。

- **Jobs**

    スケジュールに基づいて、または手動で実行される非対話型のワークロード（データ処理やETLなど）。

- **Delta Live Tables (DLT)**

    宣言的なETLパイプラインを構築するためのフレームワーク。
    データ品質のチェック、依存関係の管理、自動的なエラー処理などを簡素化します。

- **Workspace**

    ノートブック、ライブラリ、実験などを保存・共有するためのフォルダ階層。  
    データそのものを格納する場所ではありません。

- **MLflow**

    機械学習のライフサイクル（実験の追跡、再現可能な実行、モデルのデプロイ）を管理するためのオープンソースプラットフォーム。  
    Databricksに統合されています。

- **Databricks Community Edition**
  
  自分を含めて最大3名までのユーザーをワークスペースに追加可能。  
  クラスターのサイズや種類の選択肢が制限されます。

- **Databricks Enterprise Edition**

    企業組織用のアカウント。Community Editionに設定されている様々な制約が解除されている。

## 主なリソース

- Users
- Notebook
- Catalog
- Schema
- Table
- Volume

## 環境構築

Databricksの構築を行うための環境構築。

1. Databricksアカウントの登録

    [Databricks公式サイト](https://www.databricks.com/jp)からアカウントを作成。  

2. Databricksユーザーの登録

- クライアントに必要なソフトウェアをインストール

    [ローカル開発ツール](https://docs.databricks.com/aws/ja/dev-tools/)を参考に環境を構築。以下（たぶん）よく利用する開発ツール。

  - Visual Studio Code
  - Visual Studio Code 拡張機能：Databricksの登録
  - Databricks CLI

## 主なオペレーション/メンテナンス

- Databricks Enterprise Editionアカウントの契約
- ユーザー登録/ユーザー削除
- Workspacの作成/削除
- Workspacにユーザーを招待/削除
- Notebookの作成/削除
- NotebookでSQLを実行
- Notebookでデータをビジュアル化
- NotebookでCSVのデータをインポート
- Notebookで変数を定義する
- アカウントの設定でインターネットへの接続設定を変更

## 主なデベロップメント

- 
-
-

## 主なインテグレーション

- AWS
- Azure
- GCP
- GitHub

## チュートリアル補足
URL：https://docs.databricks.com/aws/ja/getting-started/

|チュートリアル: ノートブックからのデータのクエリと視覚化|15分|
|チュートリアル: ノートブックから CSV データをインポートして視覚化する|15分|


### チュートリアル: ノートブックから CSV データをインポートして視覚化する

```
ExecutionError: (java.net.UnknownHostException) health.data.ny.gov
```
アカウントの設定画面から外部接続を許可。
![alt text](image-1.png)