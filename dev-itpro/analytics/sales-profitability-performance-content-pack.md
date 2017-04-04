---
title: "販売および収益性パフォーマンスPower BIの内容"
description: "このトピックでは、- Microsoft Power BIの販売と収益性パフォーマンス内容Pack含まれるかが365 for Operationsについて説明します。 コンテンツ パックに含まれるコンテンツ パックを作成するのに使用されるレポートへのアクセス方法を説明し、モデル、データ エンティティに関する情報を提供します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>販売および収益性パフォーマンスPower BIの内容

このトピックでは、- Microsoft Power BIの販売と収益性パフォーマンス内容Pack含まれるかが365 for Operationsについて説明します。 コンテンツ パックに含まれるコンテンツ パックを作成するのに使用されるレポートへのアクセス方法を説明し、モデル、データ エンティティに関する情報を提供します。

<a name="overview"></a>概要
--------

このコンテンツPackは、販売マネージャは、収益、粗利益、および利益の主要仕入のメトリックスを監視するために作成されます。 これは、Dynamics 365 for Operationsからのトランザクション データを使用して、顧客、および製品に全社的な販売数量の合計の表示と販売実績の詳細の両方を提供します。 収益と、利益の変更にわたって強調表示して、正に関する管理者に警告する場合でも、レポートを使用でき、負は顧客ごと、製品に向きます。 カテゴリおよび地域のマネージャを使用のろまとリーダーを単一のさまざまなする製品カテゴリ、および顧客グループに収益と収益性を相互に比較するグラフの検出と便利です。 顧客ごとの収益を対価格差益計画できる本格的なレポートはアカウント マネージャに各顧客の各プロファイルへのユーザーの販売および売込みの調子を作成するデータでサポートされている基準を提供します。 販売および収益性パフォーマンス内容は販売実績を次の方法で分析するための有効な販売マネージャを詰めます:

-   収益、会計年度 (顧客グループ、顧客、販売のカテゴリ、および個々の製品および条件) 
-   前年比収益の変更 (顧客および販売地域のカテゴリに) 

収益性を次の方法で分析できます:

-   売上粗利益、および利益 (顧客グループ、製品売上のカテゴリに) 
-   前年比売上合計利益の変更
-   顧客の収益性 (収益で、粗利) 

## <a name="accessing-the-content-pack"></a>コンテンツPackのアクセス
販売および収益性パフォーマンスPower BIの内容Packは、Lifecycle Services (LCS)の実装の資産として公開され、Dynamics 365 for Operationsからアクセスできます。 Power BIレポートにアクセスして起動する方法については、" "を参照してください]、[Microsoftパートナー (能力Bi内容Microsoft partners.md) のLCSのPower BIの内容。

## <a name="metrics-included-in-the-content-pack"></a>コンテンツ パックに含まれるメトリック
コンテンツPack、グラフ、タイル、テーブルとして視覚化する一連のメトリックスで構成されるレポートが含まれます。 次の表に、コンテンツPack視覚化の概要を示します。

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **レポート ページ**        | **Charts**                                 | **タイル**                                               |
| 顧客による収益    | 収益別上位10の顧客                | 総収益                                           |
|                        | 顧客グループ別合計収益            | YOYの収益の見越計上                                      |
|                        | 顧客グループ別の平均顧客収入 | 粗利                                            |
|                        | 顧客グループ別の収益および売上合計利益   |                                                         |
| 収益の副産物     | 販売のカテゴリに収益および売上合計利益   | 製品の合計 \#                                    |
|                        | 収益別上位10の製品                 | 有効な製品の合計数と合計の割合 |
|                        | 販売のカテゴリに合計収益            | 収益の80%を占める製品の数           |
| 期間ごとの収益\*    | 月ごとの収益                           | YOYの収益の見越計上                                      |
|                        | 末尾収益の変動、YOY             | YOYの収益の見越計上]                                    |
|                        | 顧客領域からの合計販売の変動    |                                                         |
| 場所による収益    | 市町村による販売収益                      |                                                         |
|                        | YOYの収益の見越計上]                       |                                                         |
|                        | 領域からの販売収益                    |                                                         |
| 顧客の収益性 | 粗利対して顧客による収益、   | 売上粗利益、粗利、YOYの収益の見越計上          |
| 収益性分析 | 月ごとの収益と売上合計利益          |                                                         |
|                        | 粗利上位15の顧客           |                                                         |
|                        | 月、YOYごとの売上合計利益                 |                                                         |

販売のカテゴリにだけ、乗算、この\* 収益。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
工程365 for Operationsデータが販売と収益性パフォーマンス内容パックのレポートの情報も使用されます。 これは、インメモリに対して最適化されたMicrosoft SQLデータベースを使用して、エンティティの店舗で許可される) の測定単位として表されます。 ブログ[Dynamics]のフィールドに関する詳細 (https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)エンティティの店舗とのPower BI統合参照してください。 このコンテンツPack) の測定単位はDynamics AX 2012とAX 2012 R3のキューブに使用できる計算の測定のサブセットです。 エンティティの店舗のキューブ数の測定を許可するにはクライアントを配置有効にする必要があります。 詳細については、ブログ[Dynamics]のエンティティの店舗に合計の測定単位 (https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)エンティティの店舗とのPower BI統合許可する方法の手順を参照してください。 請求明細行のエンティティの次のキーの集計の測定単位は、コンテンツPack基準使用されます。

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **者) の測定**               | **、Dynamics 365 for Operationsのデータ ソース** | **Field**                                    | **Description**                          |
| 請求明細行 | 収益                                      | CustInvoiceTrans                                | 合計 (LineAmountMST)                            | 会計通貨での金額            |
|               | 売却済商品の原価                           | InventTrans                                     | 合計 (CostAmountPosted + CostAmountAdjustment)  | 原価金額+調整                 |
|               | コミッション通貨明細金額の–の会計 | CustInvoiceTrans                                | 合計 (CommissAmountMST)                         | 会計通貨でのコミッション金額 |

次の表に、コンテンツPackデータセットの複数の計算メジャーを作成するのに使用される請求明細行のエンティティ キー) の測定単位を示します。

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **計算できるように**                                                                                |
| 粗利益      | 合計 ((顧客請求書の明細金額に含まれる) 収益–のCOGS –のコミッション–の売上税)           |
| 粗利      | 合計 (売上合計利益/ (収益- (顧客請求書の明細金額に含まれる売上税)))              |
| 収益だけ | 収益が昨年=計算 (合計 (「請求書のlines'entity_PLACEHOLDER\ [の収益\])、SAMEPERIODLASTYEAR日付\[日付の\[ (\])  |

合計の測定単位をスライスするも大きく粒度、深く分析的な情報を満たすために次の主要分析コードが**販売のキューブ**などにフィルタ使用されます。

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **属性の例**                           |
| 顧客        | 顧客グループ、顧客地域、住所、Enterprise |
| 製品         | 製品番号、製品名、品目グループの名前       |
| 販売カテゴリ | 販売のカテゴリ名                                 |
| 法人   | 法人の名前                                   |
| 日付            | 日付                                                |

既定では、コンテンツPackは、現在の暦年のデータが表示され、レポートのフィルタ セクションを開き、日付のフィルタを変更できます。 さらに、会社のフィルタを変更できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](..\data-entities\data-entities.md)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](configure-power-bi-integration.md)



