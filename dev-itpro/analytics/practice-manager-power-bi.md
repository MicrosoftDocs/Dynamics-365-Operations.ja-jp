---
title: "プラクティス マネージャー Power BI コンテンツ"
description: "このトピックでは、プラクティス マネージャー Power BI コンテンツの内容について説明します。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用されるデータ モデルおよびエンティティについての情報を提供します。"
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>プラクティス マネージャー Power BI コンテンツ

[!include[banner](../includes/banner.md)]


このトピックでは、**プラクティス マネージャー** Microsoft Power BI コンテンツの内容について説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

**プラクティス マネージャー** Power BI コンテンツは、プラクティス マネージャーおよびプロジェクト マネージャー用に作成されました。 組織が取り組んでいるプロジェクトに関連した主要メトリックスが提供されます。 ダッシュ ボードでは、プロジェクトおよび関連する顧客の概要を示します。 レポート レベルのフィルターは、特定の法人のレポートに使用できます。 この Power BIコンテンツは、Microsoft Dynamics 365 for Operations のためにプロジェクト会計の集計の測定からデータを取得します。

**プラクティス マネージャー** Power BI コンテンツには、5 つのレポート ページが含まれます。1 つの概要ページと、プロジェクト原価、収益、達成額管理、および時間測定値の詳細を示す 4 つのページで、さまざまな分析コードで解析されています。

コンテンツ内のすべての金額はシステム通貨で表示されます。 システム通貨は、[**システム パラメーター**] ページで設定できます。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス

**プラクティス マネージャー** Power BI コンテンツは、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリにあります。 コンテンツ パックのダウンロード方法および Dynamics 365 for Operations データに接続する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。

Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート

次の表は、**プラクティス マネージャー** Power BI コンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。

| レポート ページ                                          | メトリックス               |
|------------------------------------------------------|-----------------------------------------------|
| ダッシュボード  | 作成済プロジェクト<br>見積済のプロジェクト<br>処理中のプロジェクト<br>ステージ別のプロジェクト数<br>都市別のプロジェクト数<br>顧客別の実績収益<br>プロジェクト別の予算粗利<br>達成額管理の概要 |
| コスト                                                 | 月別の実際対予算原価<br>年別の実際対予算原価<br>カテゴリ別の実際対予算原価<br>トランザクション タイプ別の実際原価       |
| 収益                                              | 月別の実績収益<br>郵便番号別の実績収益<br>カテゴリ別の実績対予算収益<br>顧客の業種別の実績収益        |
| EVM                                                  | プロジェクト別の原価とスケジュール業績インデックス                 |
| 時間                                                | 支払い請求可能な実績稼働時間数 対 支払請求可能な実績非稼動時間数 対 予算時間<br>プロジェクト別の支払い請求可能な実績稼働時間数 対 支払請求可能な実績非稼動時間数<br>リソース別の支払い請求可能な実績稼働時間数 対 支払請求可能な実績非稼動時間数<br>プロジェクト別の請求可能な実績時間の比率<br>リソース別の請求可能な実績時間数の比率 |

これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、「[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/)」を参照してください。 また、基になるデータをエクスポートする機能を使用するなら、視覚化で要約されている基になるデータをエクスポートすることができます。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解

Dynamics 365 for Operations データは、**プラクティス マネージャー** Power BI コンテンツのレポート ページに入力するために使用されます。 このデータは、分析用に最適化された Microsoft SQL データベースであるエンティティ格納でステージ完了である集計の測定として表されます。 詳細については、「[エンティティ ストアとの Power BI の統合](power-bi-integration-entity-store.md)」を参照してください。

次のセクションでは、各エンティティで使用される集計の測定について説明します。

### <a name="entity-projectaccountingcubeactualhourutilization"></a>エンティティ: ProjectAccountingCube_ActualHourUtilization
**データ ソース プロパティ**: ProjEmplTrans

| キー集計の測定                | フィールド                                | 説明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | 支払い請求可能な実績稼働時間数の合計 |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | 実績非稼動の比率の合計             |

### <a name="entity-projectaccountingcubeactuals"></a>エンティティ: ProjectAccountingCube_Actuals
**データ ソース**: ProjTransPosting

| キー集計の測定                | フィールド                                | 説明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  全トランザクションの転記済の収益の合計 |   
| ActualCost   |                             Sum(ActualCost)           |    全トランザクション タイプの転記済の原価の合計    |

### <a name="entity-projectaccountingcubecustomer"></a>エンティティ: ProjectAccountingCube_Customer
**データ ソース**: CustTable

| キー集計の測定                | フィールド                                | 説明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    プロジェクト数        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         使用可能なプロジェクトの数    |


### <a name="entity-projectaccountingcubeforecasts"></a>エンティティ: ProjectAccountingCube_Forecasts
**データ ソース**: ProjTransBudget

| キー集計の測定                | フィールド                                | 説明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       全トランザクション タイプの予測原価の合計     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    未収/請求済み予測収益の合計         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |全予測収益の合計と全予測原価の合計の差額

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>エンティティ: ProjectAccountingCube_ProjectPlanCostsView
**データ ソース**: Project

| キー集計の測定                | フィールド                                | 説明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | 計画タスクのすべてのプロジェクト トランザクション タイプにおける合計原価価格の見積 |

### <a name="entity-projectaccountingcubeprojects"></a>エンティティ: ProjectAccountingCube_Projects
**データ ソース**: Project

| キー集計の測定                | フィールド                                | 説明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   コスト パフォーマンス インデックス  |ProjectAccountingCube_Projects[達成額] / ProjectAccountingCube_Projects[完了済みのタスクの合計実際原価] |     合計達成額を合計実際原価で除算した計算|
|  スケジュール業績インデックス |ProjectAccountingCube_Projects[達成額] / ProjectAccountingCube_Projects[完了済みのタスクの合計予定原価]|合計達成額を合計予定原価で除算した計算 |
|作業の完了率 |作業の完了率 = ProjectAccountingCube_Projects[完了済みのタスクの合計実際原価] / (ProjectAccountingCube_Projects[完了済みのタスクの合計実際原価] + ProjectAccountingCube_Projects[プロジェクトの合計予定原価] - ProjectAccountingCube_Projects[完了済みのタスクの合計予定原価])|完了タスクの合計実際原価およびプロジェクトの予定原価に基づいた作業の合計完了率|
|プロジェクトの請求可能な実績時間数の比率|ProjectAccountingCube_Projects[プロジェクトの支払い請求可能な実績稼働時間数の合計] / (ProjectAccountingCube_Projects[プロジェクトの支払い請求可能な実績稼働時間数の合計] + ProjectAccountingCube_Projects[プロジェクトの支払い請求可能な実績非稼動時間数])|稼働および非稼働に基づく支払い請求可能な実績時間数の合計|
|達成額|ProjectAccountingCube_Projects[プロジェクトの合計予定原価] * ProjectAccountingCube_Projects[作業の完了率]|合計予定原価と作業の完了率の乗算|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>エンティティ: ProjectAccountingCube_TotalEstimatedCosts 
**データ ソース**: ProjTable

| キー集計の測定                | フィールド                                | 説明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   完了済みのタスクのすべてのプロジェクト トランザクション タイプにおける合計原価価格の見積|

## <a name="additional-resources"></a>その他のリソース

エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

- [データ エンティティ](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [ワークスペースの Power BI 統合のコンフィギュレーション](configure-power-bi-integration.md)

