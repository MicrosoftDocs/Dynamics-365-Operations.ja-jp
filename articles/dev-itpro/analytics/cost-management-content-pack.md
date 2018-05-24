---
title: "原価管理 Power BI コンテンツ"
description: "このトピックでは、原価管理 Power BI コンテンツの内容について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 88bbc54721f5da94dd811ef155e8d3bcf8c2b53c
ms.openlocfilehash: b06abae184d07cd3b914caf74bdb16a7803919af
ms.contentlocale: ja-jp
ms.lasthandoff: 05/09/2018

---

# <a name="cost-management-power-bi-content"></a>原価管理 Power BI コンテンツ

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>概要

**原価管理** Microsoft Power BI コンテンツは、在庫経理担当者または在庫や進行中の作業 (WIP) を担当、または関心を持つ組織の担当者、または標準的な原価差異の分析を担当、または関心を持つ組織の担当者を対象としています。

> [!Note]
> このトピックで説明する**原価管理** Power BIコンテンツは Dynamics 365 for Finance and Operations 8.0 に適用されます。
> 
> AppSource サイトで利用可能な**原価管理** Power BI コンテンツ パックの使用は推奨されていません。 非推奨に関しての詳細については [AppSource で利用可能な Power BI コンテンツ パック](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource) の記事を参照してください。

この Power BI コンテンツは、在庫のパフォーマンスを監視し、原価の流れを視覚化するのに役立つカテゴリ化された形式を提供します。 回転資本率、在庫を保持している日数、精度、「ABC分類」などの経営洞察力を、望ましい集計レベル (会社、品目、品目グループ、またはサイト) で得ることができます。 利用可能になった情報は、財務諸表の詳細な補足情報として使用できます。

The Power BI コンテンツは **CostObjectStatementCacheMonthly** 集計測定に基づいて作成されます。これには、主なデータソースとして **CostObjectStatementCache** テーブルがあります。 この表は、データ セット キャッシュ フレームワークで管理されます。 既定では、テーブルは 24 時間ごとに更新されますが、データ セット キャッシュの構成で更新頻度を変更したり、手動更新を有効にすることができます。 手動更新は、**原価管理**ワークスペースまたは**原価分析**ワークスペースのどちらでも実行することができます。

**CostObjectStatementCache** テーブルを更新するたびに、Power BI ビジュアル化内のデータを更新する前に **CostObjectStatementCacheMonthly** 集計測定を更新する必要があります。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス

**原価管理** Power BI コンテンツは、**原価管理**および**コスト分析**ワークスペースで表示されます。

**原価管理**ワークスペースには、次のタブが含まれています。

- **概要** – このタブは、アプリケーション データを表示します。
- **在庫会計ステータス** – このタブでは、Power BI コンテンツが表示されます。
- **製造会計ステータス** – このタブでは、Power BI コンテンツが表示されます。

**コスト分析**ワークスペースには、次のタブが含まれています。

- **概要** – このタブは、アプリケーション データを表示します。
- **在庫会計分析** – このタブでは、Power BI コンテンツが表示されます。
- **製造会計分析** – このタブでは、Power BI コンテンツが表示されます。
- **標準原価差異分析** – このタブでは、Power BI コンテンツが表示されます。

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート ページ

**原価管理** Power BI コンテンツには、一連のメトリックスで構成されるレポート ページのセットが含まれています。 これらのメトリックスはグラフ、タイル、表として視覚化されます。 

次の表に、**原価管理** Power BI コンテンツの表示の概要を示します。

### <a name="inventory-accounting-status"></a>在庫会計ステータス

| レポート ページ                               | 視覚化                                   |
|-------------------------------------------|-------------------------------------------------|
| 在庫の概要                        | 期首残高                               |
|                                           | 差分変更                                      |
|                                           | 差分変更 %                                    |
|                                           | 期末残高                                  |
|                                           | 在庫の正確性                              |
|                                           | 在庫回転率                        |
|                                           | 手持在庫日数                          |
|                                           | 期間内の有効な製品                        |
|                                           | 期間内の有効な原価オブジェクト                   |
|                                           | 品目グループ別残高                           |
|                                           | サイト別の残高                                 |
|                                           | カテゴリ別の明細書                           |
|                                           | 四半期ごとの差分変更                           |
| サイトおよび品目グループ別在庫の概要 | サイト別の在庫の正確性                      |
|                                           | サイト別の在庫回転率                |
|                                           | サイト別の在庫期末残高                |
|                                           | 品目グループ別の在庫の正確性                |
|                                           | 品目グループ別の在庫回転率          |
|                                           | サイトおよび品目グループ別の在庫期末残高 |
| 在庫明細書                       | 在庫明細書                             |
| サイトごとの在庫明細書               | サイトごとの在庫明細書                     |
| 製品階層別の在庫明細書  | 在庫明細書                             |
| 製品階層別の在庫明細書  | サイトごとの在庫明細書                     |

### <a name="manufacturing-accounting-status"></a>製造会計ステータス

| レポート ページ                | 視覚化                       |
|----------------------------|-------------------------------------|
| 仕掛品の概要 YTD           | 期首残高                   |
|                            | 差分変更                          |
|                            | 差分変更 %                        |
|                            | 期末残高                      |
|                            | 仕掛品回転資本率                  |
|                            | 手持仕掛品日数                    |
|                            | 期間内の有効な原価オブジェクト        |
|                            | リソース グループ別の差分変更        |
|                            | サイト別の残高                     |
|                            | カテゴリ別の明細書               |
|                            | 四半期ごとの差分変更               |
| 仕掛報告書              | 期首残高                   |
|                            | 期末残高                      |
|                            | カテゴリ別の仕掛品明細書           |
| サイト別の仕掛品明細書      | 期首残高                   |
|                            | 期末残高                      |
|                            | カテゴリおよびサイト別の仕掛品明細書  |
| カテゴリ階層別の仕掛品明細書 | 期首残高                   |
|                            | 期末残高                      |
|                            | カテゴリ階層別の仕掛品明細書 |

### <a name="inventory-accounting-analysis"></a>在庫会計分析

| レポート ページ        | 視覚化                                                                |
|--------------------|------------------------------------------------------------------------------|
| 在庫の詳細  | 期末残高別の上位 10 リソース                                           |
|                    | 差分変更増加別の上位 10 リソース                                      |
|                    | 差分変更減少別の上位 10 リソース                                      |
|                    | 在庫回転率別の上位 10 リソース                                 |
|                    | 低在庫回転率と期末残高がしきい値以上のリソース |
|                    | 低精度の上位 10 リソース                                             |
| ABC 分類 | 在庫期末残高                                                     |
|                    | 消費された材料                                                            |
|                    | 売却 (COGS)                                                                  |
| 在庫のトレンド   | 在庫期末残高                                                     |
|                    | 在庫差分変更                                                         |
|                    | 在庫回転率                                                     |
|                    | 在庫の正確性                                                           |

### <a name="manufacturing-accounting-analysis"></a>製造会計分析

| レポート ページ | 視覚化      |
|-------------|--------------------|
| 仕掛品のトレンド  | 仕掛品期末残高 |
|             | 仕掛品差分変更     |
|             | 仕掛品回転資本率 |

### <a name="std-cost-variance-analysis"></a>標準原価差異分析

| レポート ページ                             | 視覚化                                        |
|-----------------------------------------|------------------------------------------------------|
| 購買価格差異 (標準原価) YTD | 調達済み残高                                     |
|                                         | 購買価格差異                              |
|                                         | 購買価格差異比率                        |
|                                         | 品目グループ別の差異                               |
|                                         | サイト別の差異                                     |
|                                         | 四半期ごとの購買価格                            |
|                                         | 四半期および品目グループごとの購買価格             |
|                                         | 好ましくない購買価格比率の上位 10 リソース |
|                                         | 有利な購買価格比率の上位 10 リソース   |
| 製造差異 (標準原価) YTD     | 製造原価                                    |
|                                         | 製造差異                                  |
|                                         | 製造差異比率                            |
|                                         | 品目グループ別の差異                               |
|                                         | サイト別の差異                                     |
|                                         | 四半期ごとの製造差異                       |
|                                         | 四半期および差異タイプによる製造差異     |
|                                         | 好ましくない製造差異の上位 10 リソース  |
|                                         | 有利な製造差異の上位 10 リソース    |

### <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解

Microsoft Dynamics 365 for Finance and Operations からのデータは、**原価管理** Power BI コンテンツのレポート ページを入力するために使用されます。 このデータは、分析用に最適化された Microsoft SQL Server データベースであるエンティティ格納でステージ完了である集計の測定として表されます。 詳細については、[エンティティ ストアとの Power BI の統合](power-bi-integration-entity-store.md) を参照してください。

次のオブジェクトのキー集計の測定は、Power BI コンテンツの基準として使用されます。

| オブジェクト                          | キー集計の測定 | Finance and Operations のデータ ソース | フィールド               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | 量                     | CostObjectStatementCache               | 量              |
| CostObjectStatementCacheMonthly | 件数                   | CostObjectStatementCache               | 数量                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

次の表は、Power BI コンテンツでキー計算された測定値を示しています。

| 基準                            | 計算 |
|------------------------------------|-------------|
| 期首残高                  | 期首残高 = [期末残高]-[差分変更] |
| 期首残高数量             | 期首残高数量 = [期末残高数量]-[差分変更数量] |
| 期末残高                     | 期末残高 = (CALCULATE(SUM([Amount]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar[MONTHSTARTDATE] \<= MAX(FiscalCalendar[MONTHSTARTDATE])))) |
| 期末残高数量                | 期末残高数量 = CALCULATE(SUM([QTY]), FILTER(ALL(FiscalCalendar),FiscalCalendar[MONTHSTARTDATE] \<= MAX(FiscalCalendar[MONTHSTARTDATE]))) |
| 差分変更                         | 差分変更 = SUM([AMOUNT]) |
| 差分変更数量                    | 差分変更数量 = SUM([QTY]) |
| 金額別の在庫回転率 | 金額別の在庫回転率 = if(OR([在庫平均残高] \<= 0, [販売在庫または消費の払出] \>= 0), 0, ABS([販売在庫または消費の払出])/[在庫平均残高]) |
| 在庫平均残高          | I在庫平均残高 = (([期末残高] + [期首残高]) / 2) |
| 手持在庫日数             | 手持在庫日数 = 365 / CostObjectStatementEntries[金額別の在庫回転率] |
| 在庫の正確性                 | 金額ごとの在庫の正確性 = IF([期末残高] \<= 0, IF(OR([在庫棚卸金額] \<\> 0, [期末残高] \< 0), 0, 1), MAX(0, ([期末残高] - ABS([在庫棚卸金額]))/[期末残高])) |

以下のキー分析コードは、より高い粒度を達成し深い分析洞察を取得できるように、集計の測定をスライスするフィルターとして使用されます。


|                         エンティティ                          |             属性の例              |
|---------------------------------------------------------|-------------------------------------------------|
|                        製品                         | 製品番号、製品名、単位、品目グループ |
| カテゴリ階層 (原価管理のロールに割り当て) |       カテゴリ階層、カテゴリ レベル        |
|                     法人                      |               法人名                |
|                    会計カレンダー                     |  会計カレンダー、年、四半期、期間、月  |
|                          サイト                           |        ID、名前、住所、都道府県、国        |


