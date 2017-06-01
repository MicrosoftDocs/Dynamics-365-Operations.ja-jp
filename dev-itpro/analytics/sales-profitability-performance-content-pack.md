---
title: "販売および収益性パフォーマンス Power BI の内容"
description: "このトピックでは、Dynamics 365 for Operations に何が含まれるかについて説明します - Microsoft Power BI の販売および収益性パフォーマンス コンテンツ パック。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 357f7071d801b13518c83170f8d0e7946dd9dede
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>販売および収益性パフォーマンス Power BI の内容

[!include[banner](../includes/banner.md)]


このトピックでは、Dynamics 365 for Operations に何が含まれるかについて説明します - Microsoft Power BI の販売および収益性パフォーマンス コンテンツ パック。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。

<a name="overview"></a>概要
--------

このコンテンツ パックは、販売マネージャが、収益、粗利益、および利益率の主要な販売メトリックスを監視するために作成されます。 Dynamics 365 for Operations からのトランザクション データを使用して、全社全体の販売実績、および顧客と製品の販売実績の内訳の両方の集計ビューを提供します。 時間経過に伴う収益および利益増加率の変更を強調表示することにより、マネージャーに個々の顧客や製品の正および負のトレンドに関して警告させるように、レポートを使用できます。 カテゴリおよび地域マネージャは、ラガードとリーダーを選び出すために、異なる製品カテゴリおよび顧客グループ同士の収益や収益性を比較するグラフが便利であることに気づきます。 顧客ごとの収益対利益率をプロットする包括的なレポートは、アカウント マネージャに、各顧客のそれぞれのプロファイルへ販売およびマーケティング活動を調和させるためにデータ サポートされた基盤を提供します。 販売および収益性パフォーマンス コンテンツ パックは、販売マネージャーが販売実績を次の方法で分析できるようにします。

-   収益、年間累計 (顧客グループ、各顧客、販売カテゴリ、および個々の製品や地域による) 
-   前年比収益の変更 (顧客および販売カテゴリによる) 

収益性を次の方法で分析できます。

-   粗利益および利益率 (顧客グループおよび製品販売カテゴリによる) 
-   前年比粗利益の変更
-   顧客の収益性 (収益対粗利による) 

## <a name="accessing-the-content-pack"></a>コンテンツ パックへのアクセス
販売および収益性パフォーマンス Power BI コンテンツ パックは、Lifecycle Services (LCS) の実装資産として公開され、Dynamics 365 for Operations からアクセスできます。 Power BI レポートにどのようにアクセスし開始するかについての詳細は、[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)を参照してください。
**注記:** KB 4011327 は、この Power BI コンテンツの前提条件となります。 Lifecycle Services にサインインすると、次のサポート技術情報にアクセスできます: <a href="https://fix.lcs.dynamics.com/issue/results/?q=kb4011327">https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</a>です。

## <a name="metrics-included-in-the-content-pack"></a>コンテンツ パックに含まれるメトリックス
コンテンツ パックには、グラフ、タイル、テーブルとして視覚化する一連のメトリックスで構成されるレポートが含まれます。 次のテーブルは、コンテンツ パックでの視覚化の概要を提供します。

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **レポート ページ**        | **グラフ**                                 | **タイル**                                               |
| 顧客による収益    | 収益による上位 10 件の顧客                | 総収益                                           |
|                        | 顧客グループによる合計収益            | YOY 収益増加                                      |
|                        | 顧客グループによる平均顧客収入 | 粗利                                            |
|                        | 顧客グループによる収益および粗利益   |                                                         |
| 製品による収益     | 販売カテゴリによる収益および粗利益   | 製品の合計 \#                                    |
|                        | 収益による上位 10 件の製品                 | 有効な製品および合計割合の合計数 |
|                        | 販売のカテゴリによる総収益            | 収益の80%を占める製品の数           |
| 期間別収益\*    | 月ごとの収益                           | YOY 収益増加                                      |
|                        | 末尾にある収益差異、YOY             | YOY 収益増加 %                                    |
|                        | 顧客地域による合計販売差異    |                                                         |
| 場所別の収益    | 市町村による販売収益                      |                                                         |
|                        | YOY 収益増加 %                       |                                                         |
|                        | 地域ごとの販売収益                    |                                                         |
| 顧客の収益性 | 顧客別の粗利対収益   | 粗利益、粗利、YOY 収益増加          |
| 収益性分析 | 月ごとの収益および粗利益          |                                                         |
|                        | 粗利ごとの上位 15 件の顧客           |                                                         |
|                        | 月ごとの粗利益、YOY                 |                                                         |

\* 本年度と昨年度の収益、および販売カテゴリごとの増加。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
Dynamics 365 for Operations データは、販売および収益性パフォーマンス コンテンツ パックでレポートを格納するのに使用されます。 これはエンティティの店舗で示される総測定値として表されます。そしてそれは分析用に適化された Microsoft SQL データベースです。 詳細については [Dynamics におけるエンティティ ストアとの Power BI の統合](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)ブログを参照してください。 このコンテンツ パックの集計の測定は Dynamics AX 2012 および AX 2012 R3 の売上キューブに使用できた集計の測定のサブセットです。 エンティティ格納でキューブの集計の測定を公開するにはそれらを配置可能にする必要があります。 詳細については、[Dynamics におけるエンティティ ストアとの Power BI の統合](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)ブログで、どのように集計の測定をエンティティ格納へ公開するかの手順を参照してください。 請求明細行エンティティの以下のキー集計の測定は、コンテンツ パックの基準として使用されます。

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **エンティティ**    | **キー集計の測定**               | **Dynamics 365 for Operations のデータ ソース** | **フィールド**                                    | **説明**                          |
| 請求明細行 | 収益                                      | CustInvoiceTrans                                | 合計 (LineAmountMST)                            | 会計通貨での金額            |
|               | 売却済商品の原価                           | InventTrans                                     | 合計 (CostAmountPosted + CostAmountAdjustment)  | 原価金額 + 調整                 |
|               | コミッション明細金額 – 会計通貨 | CustInvoiceTrans                                | 合計 (CommissAmountMST)                         | 会計通貨のコミッション金額 |

次の表は、コンテンツ パック データセットで複数の計算メジャーを作成するのに使用される請求明細行エンティティのキー集計測定を示します。

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **基準**       | **次のような計算**                                                                                |
| 粗利益      | 合計 (収益 – COGC – コミッション – 消費税 (顧客請求書明細金額に含まれる))           |
| 粗利      | 合計 (粗利益 / (収益 – 消費税 (顧客請求書明細金額に含まれる)))             |
| 昨年収益 | 昨年収益 = CALCULATE(合計 ('請求明細行'\[収益\]), SAMEPERIODLASTYEAR(日付\[日付\]) |

**売上キューブ** の以下のキー分析コードは、より高い粒度や深い分析洞察を達成するために集計の測定をスライスするフィルターとして使用されます。

|                  |                                                      |
|------------------|------------------------------------------------------|
| **エンティティ**       | **属性の例**                           |
| 顧客        | 顧客グループ、顧客地域、住所、産業 |
| 製品         | 製品番号、製品名、品目グループの名前       |
| 販売カテゴリ | 販売カテゴリ名                                 |
| 法人   | 法人名                                   |
| 日付            | 日付                                                |

既定では、コンテンツ パックは現在の暦年のデータを表示しますが、レポートのフィルター セクションを開き、日付のフィルターを変更できます。 会社フィルターを変更することもできます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](..\data-entities\data-entities.md)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](configure-power-bi-integration.md)





