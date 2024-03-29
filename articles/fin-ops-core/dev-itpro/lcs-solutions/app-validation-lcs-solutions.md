---
title: 財務と運用アプリ用のアプリケーションを検証する
description: この記事では、カスタム コードが Microsoft のガイドラインを満たしていることを確認するために使用する要件の情報を提供します。
author: sericks007
ms.date: 04/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.custom: 196913
ms.assetid: 5f9729e3-ff67-4526-b2aa-d7f9f3062a41
ms.openlocfilehash: b657eea097ae15ffcdf23e7e2feca9c53bb1cea0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288685"
---
# <a name="validate-applications-for-finance-and-operations-apps"></a>財務と運用アプリ用のアプリケーションを検証する

[!include [banner](../includes/banner.md)]

この記事では、カスタムコードが Microsoft のガイドラインを満たしていること、およびソリューション パッケージが正常にバンドルされ、財務と運用アプリ環境で配送できることを確認するために使用される要件に関する情報を提供します。

Microsoft は、次の要件を検証するために特定のレビューを必要とします。

-   パートナーのカスタム コードは、Microsoft のガイドラインを満たしています。
-   Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージを正常にバンドルおよび配送することができます。
-   主要な独立系ソフトウェア ベンダー (ISV) のビジネス シナリオを処理することができます。

現在、パートナーは、テストの展開を行い、結果を Microsoft と共有することによって、これらの要件が満たされていることを実証する必要があります。 Microsoft が検証していない顧客環境では、コードは配置されません。 パートナーは、次のキュレーション コンポーネントおよびテストを行ってください。

-   コード分析レポート (CAR)
-   ビジネス プロセス モデラー (BPM)/テスト スクリプト
-   ビジネス データベースのバックアップ
-   プロジェクトの名前と説明
-   データ パッケージ 
-   方法 
-   バイナリ (オプション)
-   配置可能パッケージ
-   モデル (コードとテスト)
-   マーケティング コンテンツ

## <a name="curation-meeting"></a>キュレーション会議

次のテーブルに、検証会議の前に完了する必要がある手順を示します。

| フェーズ | ステップ | 活動                               | プロセスの手順                                                                                                                                        | 成功基準                                                                                                                                                                                                                                                                                                                        |
|-------|------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | 1    | コードを検証します。                          | CAR ツールを使用してすべての顧客モデル ファイルを実行した後、レポートを生成します。                                                                   | ローカライズ、アクセシビリティ、パフォーマンス、セキュリティ上の問題なく CAR を正常に作成します。                                                                                                                                                                                                                                     |
| 1     | 2    | ユーザー エクスペリエンス (UX) のガイドラインを確認します。 | ワークスペースを正しく実装する UX ガイドラインに従います。                                                                                          | LCS の移行および作成手法に関するページにあるベスト プラクティス情報を参照してください。                                                                                                                                                                                                                                               |
| 2     | 3    | LCS でソリューション パッケージを検証します。   | 必要なすべてのコンポーネントを含む LCS で、ソリューション パッケージを作成します。                                                                                                            | すべての必要なコンポーネントを有するソリューション パッケージは LCS に掲載され、グローバル一意識別子 (GUID) はソリューションのために作成されました。                                                                                                                                                                                                                        |
| 2     | 4    | 環境を配置します。                  | パッケージの内容 (コード、バイナリ、および構成) に基づいている取引相手コードを持つ、標準の環境を展開します。      | エラーを発生させず、少なくとも 1 つの財務と運用環境を正常に配置します。 環境コンフィギュレーション (コンポーネントとコンフィギュレーションを含む) はパートナーの参照環境と同じです。 ユーザーは、この環境にエラーなしで正常にサインインできます。 |
| 2     | 5    | データの配置およびコンフィギュレーション。              | 環境にパートナーが提供するデータをエラーなく展開します。                                                                                 | パートナーが提供するマスターと参照データが、エラーなく正常に環境にプッシュされたことを示します。               |
| 2     | 6    | サニティ チェックをします。                      | この環境にデータが読み込まれた後、ユーザーは業務トランザクションを完了する必要があります (ソリューションの範囲で定義済として)。  | データが読み込まれた環境にエラーなしでサインインできます。 エラーを発生させず、パッケージ スコープで定義されている業務トランザクションを完了することができます。                                                                                                                                                                                |

### <a name="detailed-curation-requirements"></a>詳細なキュレーション要件

次のテーブルに、キュレーションの各要件に関する詳細情報を示します。

| 必要量                  | 説明                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAR                          | CAR が強調表示したすべてのメジャーな問題はアップグレードした後対処する必要があります。 CAR は、検証会議の前に Microsoft に送信する必要があります。                                                                                                                                |
| BPM/テスト スクリプト             | すべてのタスク記録は、ソリューションパッケージが設計されている業種ごとに完了し、エンド ツー エンドのシナリオを含める必要があります。                                                                                                                                 |
| ビジネス データベースのバックアップ     | アップグレードされた環境とベスト プラクティス コンフィギュレーションのビジネス データベースは LCS のアセット ライブラリに読み込まれる必要があります。                                                                                                                        |
| プロジェクトの名前と説明 | プロジェクト名と説明は、ソリューション パッケージの実装メソッドのはじめに組み込む必要があります。                                                                                                                                               |
| データ パッケージ                | すべてのデータ パッケージは検証会議の前に LCS に読み込む必要があります。 カスタム機能のために、追加のカスタム フィールドまたはカスタム テーブル のデータ エンティティを作成します。 データ パッケージを変更して空の環境にロードし、Data Management Framework でデータ パッケージを使用できるようにする必要があります。 |
| 方法                  | 方法には、製品の概要が組み込まれる必要があります。 会議室パイロット1 (CRP1) にガイド付き操作およびソリューションに特別に用意されているその他の実装方法は、オプションです。 |
| バイナリ (オプション)          | 必要なバイナリ ファイルを組み込みます。                                                                                                                                                                                                                                               |
| 配置可能パッケージ          | 環境にカスタムの機能をもたらすために必要な配置可能パッケージを組み込みます。                                                                                                                                     |
| モデル (コードとテスト)      | ソリューションに必要なすべてのモデル ファイルを組み込みます。                                                                                                                                                                                                                     |
| マーケティング コンテンツ            | ソリューション パッケージのロゴ、説明、スクリーン ショットのようなマーケティング コンテンツを追加します。 ソリューションはアプリ固有のものにする必要があり、会社名は含めないようにします。 説明はカスタム ビジネス プロセスと整合する必要があります。                            |


## <a name="update-and-maintenance-requirements"></a>更新とメンテナンスの要件
AppSource で発行されている生成されたソリューションを使用する場合は、ソリューションを最新の状態に保持する必要があります。 秋と春の各メジャー リリースの後、コードをアップグレードするのに 8 週間かかります。 次のコンポーネントを更新しテストする必要があります。

-   CAR
-   モデル (コードとテスト)
-   配置可能パッケージ
-   BPM/テスト スクリプト
-   データ パッケージ
-   ビジネス データベースのバックアップ

### <a name="maintenance-process-steps"></a>メンテナンス プロセスのステップ

| フェーズ | 番号 | 活動                                       | プロセスの手順                                                                | 成功基準                                                                                                                                                                                                                                                                                     |
|-------|--------|------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | 1      | 顧客コードを検証します。 | CAR ツールを使用してすべての顧客モデル ファイルを実行し、レポートを生成します。 | ローカライズ、アクセシビリティ、パフォーマンス、セキュリティ上の問題なく CAR を正常に作成します。 最新のメジャー リリースにアップグレードした後、CAR が強調表示するすべてのメジャーな問題に対処する必要があります。 CAR は、春および秋の各メジャーリリース後から 8 週間以内に Microsoft に送信する必要があります。 |


## <a name="additional-resources"></a>追加リソース

[AppSource でアプリを公開するための要件](lcs-solutions-app-source.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
