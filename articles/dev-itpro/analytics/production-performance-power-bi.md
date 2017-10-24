---
title: "生産パフォーマンス Power BI コンテンツ"
description: "このトピックでは、生産パフォーマンス Power BI コンテンツに何が含まれているのか説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: f0551a9b58b58f6bdac433b88f44919428c14426
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="production-performance-power-bi-content"></a>生産パフォーマンス Power BI コンテンツ

[!include[banner](../includes/banner.md)]

このトピックでは、[**生産パフォーマンス**] Microsoft Power BI コンテンツに何が含まれているのか説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

[**生産パフォーマンス**] Power BI コンテンツは、生産マネージャまたは組織の生産管理責任者のためのものです。

含まれるレポートを使用すると、Power BI を使用して、適時の実行、品質、およびコストに関する製造工程のパフォーマンスを監視できます。 このレポートでは、製造オーダーおよびバッチ オーダーのトランザクション データが使用し、会社全体の生産指標の集計ビューおよび製品とリソース別の指標の内訳の両方を提供します。

Power BI コンテンツは、期限までに生産を完了するための組織の能力が強調表示されます。 将来のパフォーマンスは、生産計画に基づいて予測されます。 包括的なレポートは、生産に起因する製品の欠陥、およびリソースや工程の欠陥率の詳細な洞察を提供します。

この Power BI コンテンツを使用して、製造差異を分析することもできます。 製造差異は、見積原価および実現原価の差額として計算されます。 製造差異は、製造オーダーまたはバッチ オーダーが [**終了**] ステータスに達した時点で計算されます。

[**生産パフォーマンス**] Power BI コンテンツには、製造オーダーおよびバッチ オーダーからのデータが含まれます。 レポートには、かんばん生産に関連するデータは含まれていません。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) を使用している場合、[**生産パフォーマンス**] Power BI コンテンツは、[**生産パフォーマンス**] ページ ([**生産管理**] > [**照会およびレポート**] > [**生産パフォーマンスの分析**] > [**生産パフォーマンス**]) に表示されます。 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるメトリックス

[**生産パフォーマンス**] Power BI コンテンツには、レポート ページのセットが含まれています。 各ページは、グラフ、タイル、テーブルとして視覚化される一連のメトリックスで構成されています。

次の表は、含まれている視覚化の概要を示しています。

| レポート ページ                                | グラフ                                               | タイル |
|--------------------------------------------|------------------------------------------------------|-------|
| 生産パフォーマンス                     | <ul><li>日付による生産数</li><li>製品および品目グループ別の生産数</li><li>日付による計画製造数</li><li>期限遵守および完了時による下位 10 の製品</li></ul> | <ul><li>注文の合計</li><li>期限遵守 & 完了 (%)</li><li>未完了 (%)</li><li>期日前 (%)</li><li>遅延 (%)</li></ul> |
| 製品による欠陥                         | <ul><li>日付による欠陥レート (ppm)</li><li>製品および品目グループによる欠陥レート (ppm)</li><li>日付による生産数量</li><li>有効レートによる上位 10 製品</li></ul> | <ul><li>欠陥レート (ppm)</li><li>欠陥品数量</li><li>合計数量</li></ul> |
| 製品による欠陥トレンド                   | 生産数量による欠陥レート (ppm) | 欠陥レート (ppm) |
| リソースによる欠陥                        | <ul><li>日付による欠陥レート (ppm)</li><li>リソースおよびサイトによる欠陥レート (ppm)</li><li>工程による欠陥レート (ppm)</li><li>欠陥レートによる上位 10 リソース</li></ul> | 欠陥品数量 |
| リソースによる欠陥トレンド                  | 生産処理による欠陥レート (ppm) | |
| 作業オーダー原価計算の製造の差異 | <ul><li>日付および原価グループ タイプによる製造差異</li><li>サイトおよび原価グループ タイプによる製造差異</li><li>好ましくない製造差異の上位 10 製品</li><li>リソースによる好ましくない製造差異の上位 10 製品</li></ul> | <ul><li>実現原価</li><li>製造差異</li><li>製造差異 (%)</li></ul> |

## <a name="extending-the-power-bi-content"></a>Power BI コンテンツの拡張
Microsoft Dynamics Lifecycle Services (LCS) で利用できるコンテンツ パックを使用すると、Microsoft Dynamics 365 にログインしない人々に関する優れた分析ができます。 ほかのレポートまたはビジュアルを含めるよう、これらのコンテンツ パックを変更できます。次いで分析のためにコンテンツ パックを Power BI.com テナントに発行します。

LCS の共有資産ライブラリに [**生産マネージャー**] Power BI コンテンツがあります。 コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。 Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。

ご使用のバージョンの Microsoft Dynamics 365 に適用する [**生産マネージャー**] コンテンツをダウンロードしてください。

> [!NOTE]
> Microsoft Dynamics 365 for Operations バージョン 1611 を使用している場合、この Power BI コンテンツの前提条件はサポート技術情報 4011327 です。 LCS にサインインすると、https://fix.lcs.dynamics.com/issue/results/?q=kb4011327 でサポート技術情報にアクセスできます。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解

次のデータは、[**生産パフォーマンス**] Power BI コンテンツのレポート ページに使用されます。 このデータは、エンティティ ストアで実施される集計の測定として表されます。 エンティティ ストアは、分析に最適化された Microsoft SQL Server データベースです。 エンティティ格納の詳細については、「[エンティティ格納および Power BI の統合](power-bi-integration-entity-store.md)」を参照してください。

次の表では、Power BI コンテンツの基準として使用されるキー集計の測定が表示されます。

| エンティティ                   | キー集計の測定  | Finance and Operations のデータ ソース | フィールド              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

次の表は、コンテンツのデータセットで複数の計算メジャーを作成するためのキー集計の測定の使用方法を示します。

| 基準                  | 測定の計算方法 |
|--------------------------|-------------------------------|
| 製造差異 (%)   | SUM ('製造差異' [製造差異]) / SUM ('製造差異' [原価見積]) |
| すべての計画オーダー       | COUNTROWS('計画製造オーダー') |
| 期日前                    | COUNTROWS (FILTER('計画製造オーダー'、'計画製造オーダー'[終了予定日] \< '計画製造オーダー'[要求日])) |
| 遅延                     | COUNTROWS(FILTER('計画製造オーダー'、'計画製造オーダー'[終了予定日] \> '計画製造オーダー'[要求日])) |
| 期限内                  | COUNTROWS(FILTER('計画製造オーダー'、'計画製造オーダー'[終了予定日] = '計画製造オーダー'[要求日])) |
| 期限内 (%)                | IF ('計画製造オーダー'[期限内] \<\>0、'計画済生産の注文'[期限内]、IF ('計画製造オーダー'[すべての計画オーダー] \<\>0, 0, BLANK()) ) / '計画製造オーダー'[すべての計画オーダー] |
| 完成                | COUNTROWS (FILTER('製造オーダー'、'製造オーダー'[RAF'ed] = TRUE)) |
| 欠陥レート (ppm)     | IF ('製造オーダー'[合計数量] = 0、BLANK()、(SUM('製造オーダー'[欠陥品数量]) / '製造オーダー' [合計数量]) \* 1000000) |
| 遅延製造レート  | '製造オーダー'[遅延\#] / '製造オーダー'[完了] |
| 期日前 & 未完了          | COUNTROWS(FILTER('製造オーダー、'製造オーダー'[未完了] = TRUE && '製造オーダー'[期日前] = TRUE)) |
| 期日前 \#                 | COUNTROWS(FILTER('製造オーダー'、'製造オーダー'[期日前] = TRUE)) |
| 期日前 (%)                  | IFERROR( IF('製造オーダー' [期日前\#] \<\>0、'製造オーダー'[期日前\#]、IF('製造オーダー'[注文の合計] = 0、BLANK(), 0)) / '製造オーダー'[注文の合計]、BLANK()) |
| 未完了               | COUNTROWS (FILTER('製造オーダー'、'製造オーダー'[未完了] = FALSE && '製造オーダー'[RAF'ed] = TRUE)) |
| 未完了 (%)             | IFERROR( IF('製造オーダー' [Incomplete] \<\> 0、'製造オーダー'[Incomplete]、IF('製造オーダー'[注文の合計] = 0、BLANK(), 0)) / '製造オーダー'[注文の合計]、BLANK()) |
| 遅延               | '製造オーダー'[RAF'ed] = TRUE && '製造オーダー'[遅延値] = 1 |
| 期日前                 | '製造オーダー'[RAF'ed] = TRUE && '製造オーダー'[遅延した日数] \< 0 |
| 未完了               | '製造オーダー'[適正数量] \>= '製造オーダー'[予定数量] |
| RAF'ed                | '製造オーダー'[生産ステータスの値] = 5 \|\| '製造オーダー'[生産ステータスの値] = 7 |
| 遅延 & 未完了           | COUNTROWS(FILTER('製造オーダー、'製造オーダー'[未完了] = TRUE && '製造オーダー'[遅延] = TRUE)) |
| 遅延 \#                  | COUNTROWS(FILTER('製造オーダー'、'製造オーダー'[遅延] = TRUE)) |
| 遅延 (%)                   | IFERROR( IF('製造オーダー'[遅延\#] \<\>0、'製造オーダー'[遅延\#]、IF('製造オーダー'[注文の合計] = 0、BLANK(), 0)) / '製造オーダー'[注文の合計]、BLANK()) |
| 期限遵守 & 完了        | COUNTROWS(FILTER('製造オーダー'、'製造オーダー' [未完了] = TRUE && '製造オーダー'[遅延] = FALSE && '製造オーダー'[期日前] = FALSE)) |
| 期限遵守 & 完了 (%)      | IFERROR( IF('製造オーダー'[期限内 &未完了] \<\> 0、'製造オーダー'[期限内 & 未完了]、IF('製造オーダー'[完了] = 0、BLANK(), 0)) / '製造オーダー'[完了]、BLANK()) |
| 注文の合計             | COUNTROWS('製造オーダー') |
| 合計数量           | SUM('製造オーダー'[適正数量]) + SUM('製造オーダー'[欠陥品数量]) |
| 欠陥レート (ppm)        | IF ('工順トランザクション'[処理済数量] = 0、BLANK()、(SUM('工順トランザクション'[欠陥品数量]) / '工順トランザクション'[処理済数量]) \* 1000000) |
| 欠陥率混在 (ppm) | IF('工順トランザクション'[合計の混在数量] = 0、BLANK()、(SUM('工順トランザクション'[欠陥品数量]) / '工順トランザクション'[合計の混在数量]) \* 1000000) |
| 処理済数量       | SUM('工順トランザクション'[適正数量]) + SUM('工順トランザクション'[欠陥品数量]) |
| 合計の混在数量     | SUM('製造オーダー'[適正数量]) + SUM('工順トランザクション'[欠陥品数量]) |

以下のキー分析コードを表示する表は、より高い粒度を達成し、深い分析洞察を取得できるように、集計の測定をスライスするフィルターとして使用されます。

| エンティティ                    | 属性の例                                        |
|---------------------------|---------------------------------------------------------------|
| 完了報告日 | 完了 (RAF) 日付、月、および年のオフセット                 |
| 終了日                | 終了月のオフセットおよび月                                  |
| 要求日          | 要求日の月のオフセットと要求日            |
| 工順トランザクションの日付    | 工順トランザクションの月のオフセットと日付                       |
| サイト                     | サイトの ID、サイト名、都道府県、および市町村                          |
| エンティティ                  | ID および名前                                                   |
| リソース                 | リソース ID、リソース名、リソースのタイプ、およびリソース グループ |
| 製品                  | 製品番号、製品名、品目 ID、および品目グループ         |

## <a name="additional-resources"></a>その他のリソース

エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

- [データ エンティティ](../data-entities/data-entities.md)
- [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Power BI タイルをワークスペースへ追加する](configure-power-bi-integration.md)

