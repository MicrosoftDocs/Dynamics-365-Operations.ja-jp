---
title: 推奨事項用の代替データフローの設定
description: この記事では、代替データフローを使用して推奨事項サービスにデータを提供し、環境を構成する方法について説明します。
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460164"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>推奨事項用の代替データフローの設定

[!include [banner](includes/banner.md)]

この記事では、代替データフローを使用して推奨事項サービスにデータを提供し、環境を構成する方法について説明します。

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>既定のデータフローと代替データフローとの比較

次の図は、環境内の既定データフローを示しています。

![環境内の既定のデータフロー](media/reco-out-of-the-box-dataflow-2.png)

次の図は、エンティティ ストア同期バッチ ジョブが代替データフロー ステップに置き換えられる代替データフローを示しています。

![環境内の代替データフロー](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>前提

- この記事では、環境に対するレコメンデーション サービスが既に有効になっていると仮定しています。 詳細については、[製品レコメンデーションの有効化](enable-product-recommendations.md) を参照してください。
- Microsoft Azure Data Lake Storage アカウントでファイルとフォルダーを操作する場合は、次の操作を行います。

    - Azure Web ポータル インターフェイスまたは Azure Storage Explorer アプリケーションのいずれかを使用できます。
    - ファイルやフォルダーを操作する際の開始点は、使用している環境 URL に一致する名前の付いたフォルダーの下にある **dynamics365-financeandoperations** コンテナーにあります。
    - サンドボックス環境の名前が **MyUAT** の場合、環境ベース URL は `myuat.sandbox.operations.dynamics.com` です。
    - 同じストレージ アカウントに複数の環境が接続されている場合、各環境には独自のルート フォルダーが用意されます。

## <a name="prerequisites"></a>必要条件

代替データフロー アプローチを実装する前に、以下の前提条件を満たす必要があります:

### <a name="set-up-microsoft-power-platform"></a>Microsoft Power Platform の設定

Microsoft Power Platform を設定するには、[Microsoft Power Platform 統合を有効にする](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md) の手順に従います。

### <a name="install-the-export-to-data-lake-add-in"></a>Data Lake アドインへにエクスポート機能をインストールする

[Data Lake にエクスポート] アドインをインストールするには、[Azure Data Lake へのエクスポート アドインのインストール](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md)の手順に従ってください。

> [!NOTE]
> 構成値は、次の手順の一部に対して必要なのでメモします。

### <a name="configure-tables-to-export-in-dynamics-365"></a>Dynamics 365 でエクスポートするテーブルの構成

Dynamics 365 から Azure Data Lake Storage へのテーブル同期は 、**Data Lake にエクスポート** ページで管理 されます。 このページには現在メニュー項目は存在しないため、**システム管理者** セキュリティ ロールのユーザーだけが開くことができます。

Dynamics 365 でエクスポートするテーブルを構成するには、次の手順に従います。

1. **Data Lake へのエクスポート** ページを開くには、次の例に示すように、環境の基本 URL に文字列 `?mi=DataFeedsDefinitionWorkspace` を追加します。

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. **Data Lake へのエクスポート** ページで、この記事の[RetailSales キューブ テーブルの一覧](#list-of-retailsales-cube-tables) セクションに一覧表示されているテーブルをコピーします。
1. **システム名** 列で、フィルター オプションの一覧を展開します。
1. フィルター タイプについては、**次の値のいずれか** を選択します。 その後、テキスト ボックスにカーソルを置き、**Data Lake へエクスポート** ページからコピーしたテーブルの一覧を貼り付けます。
1. フィルタ オプションの一覧の下部で、**適用** を選択します。
1. グリッド内のすべての行を選択し、**アクティブにする** を選択します。

> [!NOTE]
> 次の手順に進む前に、すべての行のステータスを **実行中** に更新する必要があります。 必要に応じて、エラーのトラブルシューティングと解決を行います。

### <a name="create-a-synapse-workspace"></a>Synapse ワークスペースを作成する

まだない場合に Synapse ワークスペースを作成するには、[クイック スタート: Synapse ワークスペースを作成する](/azure/synapse-analytics/quickstart-create-workspace)の手順に従ってください。

Azure リソースを整理するには、Data Azure Storage アカウントと Synapse ワークスペースを Azure のリソース グループにまとめることをお勧めします。 [Data Lake へのエクスポート] アドインをインストールした時に作成したストレージ アカウントを再使用できます。

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>レコメンデーション データ処理用に Synapse でデータベースを作成する

Common Data Model ユーティリティ コンソール アプリケーション (CDMUtil_ConsoleApp) を使用して、データベースを Syapse ワークスペースで作成し、Data Lake Storage の Common Data Model テーブルから自動入力します。 拡張機能がある場合は、開発環境では Common Data Model ユーティリティをデータベースと併用することお勧めします。

> [!NOTE]
> 次の手順では、RetailSales キューブに拡張データが追加されません。

Synapse でデータベースを作成するには、次の手順に従います。

1. [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app) に移動し、手順に従って **CDMUtilConsoleApp.zip** ファイルをダウンロードします。
1. zip ファイルをローカル フォルダーに展開します。
1. **CDMUtil_ConsoleApp.dll.config** ファイルをテキスト エディタで開き、次の値を更新します。

    1. **テナント ID** 値 (Azure テナント ID) を設定します。
    1. **アクセス キー** 値 (Data Storage Storage アカウントのアクセス キー) を設定します。

        1. Azure ポータルで、ストレージ アカウントを開きます。
        1. ページの左側にあるメニューで、**アクセス キー** を選択します。
        1. ページ上部で、**キーの表示** を選択します。
        1. 2 つのキー フィールドのいずれかのコピー ボタンを選択し、構成ファイルの二重引用符の間に値を貼り付けます。

    1. Azure Data Lake Storage で、**ManifestURL** の値を **Tables.manifest.cdm.json** ファイルの URL に設定します。 URL を取得するには、Azure ポータルでファイルを参照し、ビューの右側の省略記号 (**...**) を選択し、**プロパティ** を選択します。 URL は、**概要** タブに表示される最初のプロパティです。
    1. **TargetDbConnectionString** の値を、Synapse ワークスペースの組み込みサーバーレス SQL プールの接続文字列に設定します。

        1. Synapse ワークスペースで、**管理** タブを選択します。
        1. サブメニューで、**SQL プール** を選択します。
        1. プールのプロパティを表示するには、**組み込み型** という名前を選択します。
        1. プロパティ ダイアログ ボックスで、使用する ADO.NET 接続タイプを選択します。 その後、接続文字列の値をコピーし、構成ファイルの二重引用符の間に貼り付けます。

        > [!NOTE]
        > データベースを作成するためのアクセス許可が必要です。 使い易さのために、組み込みの **sqladminuser** 管理者アカウントを使用することができます。

    1. **ProcessEntities** ノードのコミットを 解除し、その値を **true** に設定します (たとえば `<add key="ProcessEntities" value ="true"/>`)。

1. **CDMUtil_ConsoleApp.dll.config** ファイルを保存して閉じます。
1. **EntityList.json** ファイルを **/Manifest** ディレクトリにコピーします。
1. コマンド プロンプト ウィンドウで、**cdmutil_consoleapp.exe** コマンドを実行します。

> [!NOTE]
> 出力を確認する際、35 のエンティティ/ビュー、少なくとも 75 のテーブルがあり、かつエラーがない必要があります。

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Data Lake RetailSales Aggregate Measurements ディレクトリの準備

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>現在の RetailSales キューブ データを Data Lake Storage からバックアップする

現在の RetailSales キューブ データをバックアップする最も簡単な方法は、Data Retail Storage **RetailSales-backup** などから **RetailSales** ディレクトリの名前を変更することです。 この方法では、後からトラブルシューティングを行う必要がある場合に備えて、既存のデータを保持します。

**/RetailSales** キューブ フォルダーは次の場所にあります。

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>新しい RetailSales フォルダーの作成とモデル ファイルのアップロード

新しい **RetailSales** ディレクトリを作成し、**model.json** ファイルを Data Lake Storage にアップロードするには、次の手順に従います。

1. 前のディレクトリと同じレベルで新しい空のディレクトリを作成し、そのディレクトリに **RetailSales** という名前を付けます。
1. 新しいディレクトリに **model.json** ファイルをアップロードします。

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>RetailSales キューブ データをコピーするパイプラインの作成

パイプラインは RetailSales キューブ ビューを読み取り、データを Data Lake Storageの .csv ファイルにエクスポートします。

パイプラインを作成して RetailSales キューブ データをコピーするには、次の手順に従います。

1. Synapse ワークスペースで、**統合** タブを選択します。
1. プラス記号 (**+**) を選択し、**パイプライン テンプレートからインポート** を選択します。
1. [ExportRetailSalesCubeViews.zip ファイル](https://aka.ms/reco-alternate-dataflow-files) をダウンロードして選択します。
1. SQL データベースにリンクされたサービスを選択します。
1. ストレージ アカウントにリンクされたサービスを選択します。
1. **データのコピー** ツールを開き、**フォルダー パス** プロパティを **\<environment_name\>/...** に変更します。

### <a name="test-execution-of-the-pipeline"></a>パイプラインのテスト実行

パイプラインは、1 つのビューだけを使用してテストすることをお勧めします。 **RetailSales_RetailMediaTemplateView** ビューは、含まれる行が 10 行未満なのでうまくいきます。

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>パイプラインを定期スケジュールで実行するようにスケジュールする

パイプラインを実行するたび、Azure の消費が発生します。 実行は 48 時間以上の間隔でスケジュールすることをお勧めします。 データをすぐに同期する必要がある場合は、パイプラインをいつでも手動で実行できます。 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Dynamics 365 から Data Lake Storage への同期のテーブル リスト

次のテーブルのリストは、RetailSales キューブ全体に必要なすべてのテーブルのサブセットです。 RetailSales キューブのビューのうち 15 つだけがレコメンデーション サービスで使用され、必要なテーブルのリストがそれに従ってフィルター処理されています。

### <a name="list-of-retailsales-cube-tables"></a>RetailSales キューブ テーブルのリスト

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- カタログ
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- 在庫テーブル
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Synapse パイプラインに渡すパラメーターのリストを表示します

次のコンマ区切りリストには、パイプラインで "選択" 操作が実行される RetailSales キューブ ビューが含まれます。 結果は Data Lake Storage にコピーされます。

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> パイプライン パラメーターは、単一のコンマで区切られたビュー名のリストである必要があります。 スペースまたはライン フィードは含めることはできません。

## <a name="environment-specific-fixes"></a>環境固有の修正

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW 修正

**RETAILCHANNELVIEW** には、「小売チャンネル」 タイプの組織を表すハード コードされた整数が含まれています。 タイプの実際値は、環境から環境、またはテナントからテナントに変更できます。

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

ハードコード化された整数を更新するには、次の手順を実行します。

1. Dynamics 365 で、オンライン チャンネルの **ChannelID** 値を参照します。
1. Synapse データベースに関連付けられた SQL Server Management Studio (SSMS) のインスタンスで、次のクエリを実行します。

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. 1 列目 (**INSTANCERELATIONTYPE**) から値をコピーし、ビュー定義に貼り付けます。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="pipeline-task-fails"></a>パイプライン タスク失敗

**CopyData** タスクに対して 15 件のパイプライン タスクを実行する必要があります。 実行が失敗した場合は、すべての依存 SQL オブジェクトが存在し、クエリが実行されることを検証する必要があります。 すべての依存関係にアクセスする最も簡単な方法は、SSMS を使ってデータベースに接続する方法です。 その後、ビューを選択して保留 (または右クリック) し、**新しいウィンドウに対して CREATE を生成する** を選択できます。

エラー メッセージには次のテキストが含まれている場合があります。

- エラー : "ソース" 側でエラーが発生しました
- 外部ファイルのエラー処理 : 「最大エラー カウント」。
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>シナリオ例

この例では、タスク **RetailSales_RetailProductCategory** が失敗し、「Max errors count」 というエラーが表示されます。

エラーをデバッグするには、次の手順に従います。

1. テキスト エディタ (Visual Studio Code など) で **EntityList.json** ファイルを開きます。
1. **RetailSales_RetailProductCategory** のビュー定義を見つけます。

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. このビューは、**RetailProductCategoryView** _  という他の 1 つのビューにのみ依存します。 _*RetailProductCategoryView** のビュー定義を見つけます。

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. このビューは、**RETAILPRODUCTCATEGORY**、**RETAILRESPRODUCTTRANSLATIONS**、および **RETAILCATEGORYEXPANDED** の 3 つのビューに依存します。 これらの各ビューの定義を検索し、その依存関係を一覧表示します。 すべての従属ビューが見つけるまでこのまま続行します。

    次に、依存関係ツリーの順序の全体の一覧を示します。 13 回のビューは検証する必要があります。

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. Excelで、\<view_name\> **ステートメントから次の 13** の select count(\*) を 作成します。 これらのステートメントを SQLS で実行し、結果をテキストに送信します。 その後、結果までスクロールして、一部のビューが失敗したかどうかを確認します。 最初のエラーは、少なくとも 1 つのビューが失敗したことを示しています。

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. 表示している情報を検証する 1 つの方法として、ルート依存のビューを作成して、ビュー定義を SSMS で生成します。 その後、**r.filepath** という名前の Azure Data Lake ファイル列があることを確認します。 この列が存在する場合、検査中のビューが Data Lake Storage のデータを読み取っていることを示します。

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[カスタマイズされた推奨事項の有効化](personalized-recommendations.md)

["類似したルックを買う" 推奨を有効にする](shop-similar-looks.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨設定の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
