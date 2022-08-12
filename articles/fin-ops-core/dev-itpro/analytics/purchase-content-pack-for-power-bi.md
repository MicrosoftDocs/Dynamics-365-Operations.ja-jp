---
title: 購買支出の分析 Power BI コンテンツ
description: この記事では、購買支出の分析 Power BI コンテンツの内容について説明します。
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom:
- "265434"
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.form: PurchaseSpendAnalysisPowerBI
ms.openlocfilehash: 3befeb2b53f6b47cb23edbf520f49f88bd978d76
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206694"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>購買支出の分析 Power BI コンテンツ

[!include [banner](../includes/banner.md)]

この記事では、**購買支出の分析** Microsoft Power BI コンテンツの内容について説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

**購買支出の分析** Power BI コンテンツは、予算を担当する購買部門のマネージャーおよびマネージャーが購買支出を追跡できるように設計されています。 マネージャーは、以下の方法で購買支出を分析できます:

- 会計年度の購買 (仕入先グループと個々の仕入先、調達カテゴリと個々の製品、仕入先の場所)
- 前年比購買の変化 (仕入先グループと調達カテゴリ)

コンテンツは購買トランザクション データを使用して、会社全体の購買数の集計ビュー、仕入先および製品の購買先支出の内訳の両方を提供します。 レポートでは時間経過に伴う購買支出の変化が強調表示されています。 そのため、このレポートは、個々の仕入先や製品の積極的および消極的な支出動向を管理者に警告するために使用することができます。 また、チャートは、様々な調達カテゴリおよび仕入先グループの購買支出を示します。 それゆえ、カテゴリおよび地域マネージャーは、チャートを使用して支出行動の変化を識別することができます。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス
**購買支出の分析** Power BI コンテンツは **購買支出の分析** ページ (**調達** \> **照会およびレポート** \> **購買パフォーマンスの分析** \> **購買支出の分析**) に表示されます。

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるメトリックス
**購買支出の分析** Power BI コンテンツには、一連のメトリックスで構成されるレポートが含まれます。 これらのメトリックスはグラフ、タイル、表として視覚化されます。 

次の表は、視覚化の概要を示しています。

### <a name="purchase-by-vendor-report-page"></a>仕入先別購入レポートページ
**グラフ**
- 購買別トップ 10 の仕入先 (積み上げ棒グラフ)
- 仕入先グループ、国、名前別購買合計 (円グラフ)
- 仕入先グループ、国、名前別購買 (円柱グラフ)
- 仕入先グループ、国、名前別平均購買 (円柱グラフ)

**タイル**
- 購買の合計
- 前年比購買成長
- 合計仕入先数
- 有効な仕入先合計数

**例**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>製品別購買レポートページ

**グラフ**
- 調達カテゴリまたは製品名別購買 (円柱グラフ)
- 調達カテゴリまたは製品名 (円グラフ) 別購買合計
- 購買別トップ 10 製品 (積み上げ棒グラフ)

**タイル**
- 製品の合計数</li>
- 製品合計数の有効な製品の合計割合
- 購買の 80% を占める製品の数

**例**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>期間別購買レポートページ
このページでは、今年度と昨年度の購買、および調達カテゴリによる成長が表示されます。

**グラフ** 
- 月/日別の購買 (円柱グラフ)
- 累計購買金額の前年比差異 (伝播)
- 合計購買金額の前年比成長 (円柱グラフ)
- 調達明細書 (マトリックス)

**タイル**
- 前年比購買成長
- 前年比購買成長の割合 %

**例**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>仕入先場所別購買レポートページ

**グラフ**
- 市町村別の購買
- 購買額の前年比成長の割合 %
- 購買国

**例**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>時間別購買先支出の分析レポートページ

**グラフ** 
- 月/日別今年度の購買 (折れ線グラフ)
- 今年度および昨年度の購買 (線と円柱グラフ)

**例**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>仕入先別購買先支出の分析レポートページ

**グラフ** 
- トップ 10 の仕入先の購買割合 % (じょうご)
- トップ 10 仕入先による増加支出額の前年比
- トップ 10 仕入先による減少支出額の前年比

**例** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>データ モデルおよびエンティティ
次のデータは、**購買支出の分析** Power BI コンテンツのレポート ページに入力するために使用されます。 このデータは、エンティティ ストアで実施される集計の測定として表されます。 エンティティ ストアは、分析に最適化された Microsoft SQL Server データベースです。 詳細については、[エンティティ格納と Power BI の統合](power-bi-integration-entity-store.md) を参照してください。

このコンテンツの集計の測定は Microsoft Dynamics AX 2012 および Microsoft Dynamics AX 2012 R3 の購買キューブに使用できた集計の測定のサブセットです。 エンティティ格納でキューブの集計の測定を公開するには、それらを配置可能にする必要があります。 詳細については、[エンティティ ストアと Power BI の統合](power-bi-integration-entity-store.md) ブログ投稿で、集計の測定をエンティティ格納へ公開する手順を参照してください。 次のキー集計の測定は、請求明細行エンティティから直接使用でき、コンテンツの基準として使用されます。

| エンティティ        | キー集計の測定 | データ ソース                                 | フィールド              | 説明                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| 請求明細行 | 購買                   | VendInvoiceTrans                            | 合計 (LineAmountMST) | 会計通貨での金額。 |

次の表は、請求明細行のエンティティのコンテンツで計算される主要な測定単位を示します。

| 基準               | 計算                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| 今年度の購買 | 今年度の購買 = SUM('請求明細行'\[購買\])                                            |
| 昨年度の購買    | 昨年購買 = CALCULATE(合計 ('請求明細行'\[購買\]), SAMEPERIODLASTYEAR(日付\[日付\])) |
| 前年比購買成長   | 前年比購買成長 = \[今年度の購買\] – \[昨年度の購買\]                            |

コンテンツの以下のキー分析コードは、より高い粒度を達成し深い分析洞察を取得できるように、集計の測定をスライスするフィルターとして使用されます。

| エンティティ                 | 属性の例                                |
|------------------------|-------------------------------------------------------|
| 仕入先                | 仕入先グループ、仕入先の国または地域、仕入先名 |
| 製品               | 製品番号、製品名、品目グループの名前        |
| 調達カテゴリ | 調達カテゴリ、調達カテゴリの名前      |
| 法人         | 法人名                                     |
| 日付                  | 日付、年度相殺                                    |

既定では、コンテンツは、現在の暦年のデータが表示されます。 ただし、レポートのフィルタ セクションの日付のフィルタを変更できます。 会社フィルターを変更することもできます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
