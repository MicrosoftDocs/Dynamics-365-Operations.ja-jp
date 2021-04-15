---
title: 定期的なデータ エクスポートのアプリの作成
description: この記事では Microsoft Dynamics 365 Human Resources から定期的なスケジュールでデータをエクスポートする Microsoft Azure ロジック アプリを作成する方法を説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3d7fc01906a017d4214d4794097a11b4a3416b95
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801122"
---
# <a name="create-a-recurring-data-export-app"></a>定期的なデータ エクスポートのアプリの作成

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では Microsoft Dynamics 365 Human Resources から定期的なスケジュールでデータをエクスポートする Microsoft Azure ロジック アプリを作成する方法を説明します。 このチュートリアルでは Human Resources の DMF パッケージ REST アプリケーション プログラミング インターフェイス (API) を利用して、データをエクスポートします。 データがエクスポートされた後、ロジック アプリはエクスポートされたデータ パッケージを Microsoft OneDrive for Business のフォルダーに保存します。

## <a name="business-scenario"></a>ビジネス シナリオ

Microsoft Dynamics 365 統合のひとつの典型的なビジネス シナリオでは、データは定期的なスケジュールで下流システムにエクスポートされる必要があります。 このチュートリアルでは Microsoft Dynamics 365 Human Resources からすべての作業者レコードをエクスポートし、OneDrive for Business のフォルダーに作業者のリストを保存する方法を示します。

> [!TIP]
> このチュートリアルでエクスポートされる特定のデータと、エクスポートされたデータの宛先は単なる例です。 ビジネスのニーズに合わせてそれらを簡単に変更できます。

## <a name="technologies-used"></a>使用されるテクノロジ

このチュートリアルでは下記のテクノロジを使用します:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – エクスポートされる作業者のマスター データ ソース。
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – 定期的なエクスポートのオーケストレーションとスケジュールを提供するテクノロジ。

    - **[コネクタ](https://docs.microsoft.com/azure/connectors/apis-list)** – ロジック アプリを必要なエンドポイントに接続するために使用されるテクノロジ。

        - [Azure AD の HTTP](https://docs.microsoft.com/connectors/webcontents/) コネクタ
        - [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) コネクタ

- **[DMF パッケージ REST API](../dev-itpro/data-entities/data-management-api.md)**  – エクスポートをトリガーし、その進捗を監視するために使用されるテクノロジ。
- **[OneDrive for Business](https://onedrive.live.com/about/business/)** – エクスポートされた作業者の宛先。

## <a name="prerequisites"></a>必要条件

このチュートリアルで手順を開始する前に、次の項目が必要です:

- その環境で管理者レベルの権限を持つ Human Resources 環境
- ロジック アプリをホストする [Azure サブスクリプション](https://azure.microsoft.com/free/)

## <a name="the-exercise"></a>演習

この演習の最後には、Human Resources 環境と OneDrive for Business アカウントに接続されているロジック アプリを取得できます。 ロジック アプリは Human Resources からデータ パッケージをエクスポートし、そのエクスポートが完了するのを待ち、エクスポートされたデータ パッケージをダウンロードして、指定した OneDrive for Business フォルダーにデータ パッケージを保存します。

完成したロジック アプリは、次の図のようになります。

![ロジック アプリの概要](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>ステップ 1: Human Resources でデータ エクスポート プロジェクトを作成する

Human Resources で、作業者をエクスポートするデータ エクスポート プロジェクトを作成します。 プロジェクトに **作業者のエクスポート** という名前を付け、**データ パッケージの生成** オプションが **はい** に設定されていることを確認します。 プロジェクトに単一のエンティティ (**作業者**) を追加して、エクスポートする形式を選択します。 (このチュートリアルは Microsoft Excel 形式を使用します。)

![作業者データ プロジェクトをエクスポート](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> データ エクスポート プロジェクトの名前を記憶します。 次のステップでロジック アプリを作成するときに必要です。

### <a name="step-2-create-the-logic-app"></a>ステップ 2: ロジック アプリの作成

演習の大部分はロジック アプリの作成に関するものです。

1. Azure ポータルで、ロジック アプリを作成します。

    ![ロジック アプリ作成ページ](media/integration-logic-app-creation-1.png)

2. Logic Apps Designer で、空白のロジック アプリから始めます。
3. 24 時間ごとに (または選択したスケジュールに従って) ロジック アプリを実行するために [定期スケジュール トリガー](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) を追加します。

    ![定期ダイアログ ボックス](media/integration-logic-app-recurrence-step.png)

4. [ExportToPackage DMF](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API を呼び出して、データ パッケージのエクスポートをスケジュールします。

    1. Azure AD コネクタで HTTP から **HTTP 要求を呼び出す** アクションを使用します。

        - **基本リソース URL:** Human Resources 環境の URL (パス / 名前空間情報を含めないでください。)
        - **Azure AD リソース URI:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > Human Resources 環境では、**ExportToPackage** などの DMF パッケージ を構成するすべての API を公開するコネクタはまだ提供されていません。 代わりに、Azure AD コネクタで HTTP を経由して、未加工の HTTPS 要求を使用して API を呼び出す必要があります。 このコネクターは Human Resources に対する認証および承認に Azure Active Directory (Azure AD) を使用します。

        ![Azure AD コネクタの HTTP](media/integration-logic-app-http-aad-connector-step.png)

    2. Azure AD コネクタの HTTP 経由で Human Resources 環境にサインインします。
    3. HTTP **POST** 要求をセットアップして **ExportToPackage DMF** REST API を呼び出します。

        - **メソッド:** POST
        - **要求の URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **B要求の本文:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![HTTP 要求アクションの呼び出し](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > 既定の名前より意味があるように各ステップの名前を変更したい場合は、**HTTP 要求を呼び出します**。 たとえば、このステップの名前を **ExportToPackage** に変更できます。

5. [変数を初期化](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) して **ExportToPackage** 要求の実行状態を格納します。

    ![変数のアクションを初期化](media/integration-logic-app-initialize-variable-step.png)

6. データ エクスポートの実行状態が **成功** になるまで待ちます。

    1. **ExecutionStatus** 変数が **成功** になるまで繰り返す [Until ループ](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) を追加します。
    2. エクスポートの現在の実行状態のポーリング前に 5 秒間待機する **遅延** アクションを追加します。

        ![Until ループ コンテナー](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > エクスポートが完了するまで最大 75 秒 (15 イテレーション × 5 秒) 待つには、制限カウントを **15** に設定します。 さらにエクスポートに時間がかかる場合は、必要に応じて制限カウントを調整してください。        

    3. **IHTTP 要求の呼び出し**  アクションを追加して [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF  REST API を呼び出し、**ExecutionStatus** 変数を **GetExecutionSummaryStatus** 応答の結果に設定します。

        > このサンプルはエラー チェックを実行しません。 **GetExecutionSummaryStatus** API は成功しなかった端末状態 (つまり、**"成功"** 以外の状態) を返す可能性があります。 詳細については [API のドキュメント](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) を参照してください。

        - **メソッド:** POST
        - **要求の URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **要求の本文:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > コード ビューまたはデザイナーの機能エディターで **要求の本文** 値を入力する必要がある場合があります。

        ![HTTP 要求 2 アクションの呼び出し](media/integration-logic-app-get-execution-status-step.png)

        ![変数アクションの設定](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > デザイナーが同じ方法で値を表示するとしても、 **変数を設定** アクション (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) の値は **HTTP request 2 の呼び出し** 本文値の値とは異なります。

7. エクスポートしたパッケージのダウンロード URL を取得します。

    - **HTTP 要求の呼び出し アクション** を追加して  [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST AP を呼び出します。

        - **メソッド:** POST
        - **要求の URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **要求の本文:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![GetExportedPackageURL action](media/integration-logic-app-get-exported-package-step.png)

8. エクスポートしたパッケージのダウンロード

    - 前のステップで返された URL からパッケージをダウンロードするための HTTP **GET** 要求 (組み込み [HTTP コネクタ アクション](https://docs.microsoft.com/azure/connectors/connectors-native-http)) を追加します。

        - **メソッド:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > コード ビューまたはデザイナーの機能エディターで **URI** 値を入力する必要がある場合があります。

        ![HTTP GET アクション](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > **GetExportedPackageUrl** API が返す URL には、ファイルをダウンロードするアクセスを許可する共有アクセス署名トークンが含まれているため、この要求は追加の認証を必要としません。

9. [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) コネクタを使用してダウンロードしたパッケージを保存する。

    - OneDrive for Business の [ファイルの作成](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) アクションを追加します。
    - 必要に応じて OneDrive for Business アカウントを接続します。

        - **フォルダーのパス:** 選択したフォルダー
        - **ファイル名:** 作業者\_package.zip
        - **ファイルのコンテンツ:** 前のステップからの本文 (動的コンテンツ)

        ![ファイルのアクションの作成](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>ステップ 3: ロジック アプリのテスト

ロジック アプリをテストするには、デザイナーで **実行** ボタンを選択します。 ロジック アプリのステップが実行を開始することを確認します。 30 から 40 秒後、ロジック アプリの実行が終了し、OneDrive for Business フォルダにエクスポートされた作業者を含む新しいパッケージ ファイルが含まれるはずです。

どこかのステップで失敗が報告された場合、デザイナーから失敗したステップを選択し、その **入力** フィールドと **出力** フィールドを確認します。 エラーを修正するため必要に応じてステップをデバッグおよび調整します。

次の図はロジック アプリのすべてのステップが正常に実行された場合の Logic Apps Designer の外観を示しています。

![成功したロジック アプリの実行](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>集計

このチュートリアルではロジック アプリを使用して Human Resources からデータをエクスポートして、そのエクスポートしたデータを OneDrive for Business フォルダーに保存する方法を学びました。 ビジネスのニーズに合わせて、このチュートリアルの手順を必要に応じて変更できます。




[!INCLUDE[footer-include](../includes/footer-banner.md)]