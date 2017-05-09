---
title: "購買先支出分析 Power BI コンテンツ"
description: "このトピックでは、Microsoft Power BI の購買先支出分析コンテンツ パックについて説明します。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用されるデータ モデルおよびエンティティについての情報を提供します。"
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>購買先支出分析 Power BI コンテンツ

このトピックでは、Microsoft Power BI の購買先支出分析コンテンツ パックについて説明します。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用されるデータ モデルおよびエンティティについての情報を提供します。

<a name="overview"></a>概要
--------

Microsoft Power BI の購買先支出分析コンテンツ パックは購買部門のマネージャと予算を担当しているマネージャのために作成されました。 購買先支出を監視するために設計されました。 Microsoft Dynamics 365 for Operations からの購買トランザクション データを使用して、会社全体の購買数の集計ビュー、仕入先および製品の購買先支出の内訳の両方を提供します。 レポートでは時間経過に伴う購買支出の変化が強調表示されています。 そのため、このレポートは、個々の仕入先や製品の積極的および消極的な支出動向を管理者に警告するために使用することができます。 チャートは、様々な調達カテゴリおよび仕入先グループの購買支出を示します。 カテゴリ マネージャおよび地域マネージャにとって、これらのチャートは支出行動の変化を識別するのに役立つかもしれません。 このコンテンツ パックを使用して、購買部門のマネージャと予算を担当しているマネージャは、次の方法で購入支出を分析できます。

-   会計年度の購買 (仕入先グループと個々の仕入先、調達カテゴリと個々の製品、仕入先の場所)
-   前年比購買の変化 (仕入先グループと調達カテゴリ)

## <a name="accessing-the-content-pack"></a>コンテンツ パックへのアクセス
購買先支出分析 Power BI コンテンツ パックは、Microsoft Dynamics Lifecycle Services (LCS) の実装資産として公開され、Microsoft Dynamics 365 for Operations からアクセスできます。 Power BI レポートにどのようにアクセスし、開くかについての詳細は、[Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md) を参照してください。

## <a name="metrics-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるメトリックス
購買先支出分析コンテンツ パックには、一連のメトリックスで構成されるレポートが含まれます。 これらのメトリックスはグラフ、タイル、表として視覚化されます。 次の表は、コンテンツ パックでの視覚化の概要を示しています。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>レポート ページ</th>
<th>グラフ</th>
<th>タイル</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>仕入先別購買</td>
<td><ul>
<li>購買別トップ 10 の仕入先 (積み上げ棒グラフ)</li>
<li>仕入先グループ、国、名前別購買合計 (円グラフ)</li>
<li>仕入先グループ、国、名前別購買 (円柱グラフ)</li>
<li>仕入先グループ、国、名前別平均購買 (円柱グラフ)</li>
</ul></td>
<td><ul>
<li>購買の合計</li>
<li>前年比購買成長</li>
<li>合計仕入先数</li>
<li>有効な仕入先合計数</li>
</ul></td>
</tr>
<tr class="even">
<td>製品別購買</td>
<td><ul>
<li>調達カテゴリまたは製品名別購買 (円柱グラフ)</li>
<li>調達カテゴリまたは製品名 (円グラフ) 別購買合計</li>
<li>購買別トップ 10 製品 (積み上げ棒グラフ)</li>
</ul></td>
<td><ul>
<li>製品の合計数</li>
<li>製品合計数の有効な製品の合計割合</li>
<li>購買の 80% を占める製品の数</li>
</ul></td>
</tr>
<tr class="odd">
<td>期間別購買*</td>
<td><ul>
<li>月/日別の購買 (円柱グラフ)</li>
<li>累計購買金額の前年比差異 (伝播)</li>
<li>合計購買金額の前年比成長 (円柱グラフ)</li>
<li>調達明細書 (マトリックス)</li>
</ul></td>
<td><ul>
<li>前年比購買成長</li>
<li>前年比購買成長の割合 %</li>
</ul></td>
</tr>
<tr class="even">
<td>仕入先の場所別購買</td>
<td><ul>
<li>市町村別の購買</li>
<li>購買額の前年比成長の割合 %</li>
<li>購買国</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>時間別購買先支出の分析</td>
<td><ul>
<li>月/日別今年度の購買 (折れ線グラフ)</li>
<li>今年度および昨年度の購買 (線と円柱グラフ)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>仕入先別購買先支出の分析</td>
<td><ul>
<li>トップ 10 の仕入先の購買割合 % (じょうご)</li>
<li>トップ 10 仕入先による増加支出額の前年比</li>
<li>トップ 10 仕入先による減少支出額の前年比</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* 今年度と昨年度の購買、調達カテゴリによる成長

## <a name="data-model-and-entities"></a>データ モデルおよびエンティティ
Dynamics 365 for Operations のデータは、購買先支出分析コンテンツ パックのレポートに使用されます。 このデータは、分析用に最適化された Microsoft SQL データベースであるエンティティ格納でステージ完了である集計の測定として表されます。 エンティティ ストアに関する詳細については、[Dynamics におけるエンティティ ストアとの Power BI の統合](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) ブログ投稿を参照してください。 このコンテンツ パックの集計の測定は Microsoft Dynamics AX 2012 および Microsoft Dynamics 365 for Operations 2012 R3 の購買キューブに使用できた集計の測定のサブセットです。 エンティティ格納でキューブの集計の測定を公開するには、それらを配置可能にする必要があります。 詳細については、[Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) ブログ投稿で、集計の測定をエンティティ格納へ公開する手順を参照してください。 次のキー集計の測定は、請求明細行エンティティから直接使用でき、コンテンツ パックの基準として使用されます。

| エンティティ        | キー集計の測定 | Dynamics 365 for Operations のデータ ソース | フィールド              | 説明                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| 請求明細行 | 購買                   | VendInvoiceTrans                            | 合計 (LineAmountMST) | 会計通貨での金額 |

次の表は、請求明細行のエンティティのコンテンツ パックで計算される主要な測定単位を示します。

| 基準               | 計算                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| 今年度の購買 | 今年度の購買 = SUM('請求明細行'\[購買\])                                            |
| 昨年度の購買    | 昨年購買 = CALCULATE(合計 ('請求明細行'\[購買\]), SAMEPERIODLASTYEAR(日付\[日付\])) |
| 前年比購買成長   | 前年比購買成長 = \[今年度の購買\] – \[昨年度の購買\]                            |

コンテンツ パックの以下のキー分析コードは、より高い粒度や深い分析洞察を達成できるように、集計の測定をスライスするフィルターとして使用されます。

| エンティティ                 | 属性の例                                |
|------------------------|-------------------------------------------------------|
| 仕入先                | 仕入先グループ、仕入先の国または地域、仕入先名 |
| 製品               | 製品番号、製品名、品目グループの名前        |
| 調達カテゴリ | 調達カテゴリ、調達カテゴリの名前      |
| 法人         | 法人名                                     |
| 日付                  | 日付、年度相殺                                    |

既定では、コンテンツ パックは、現在の暦年のデータが表示されます。 ただし、レポートのフィルタ セクションの日付のフィルタを変更できます。 会社フィルターを変更することもできます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](..\data-entities\data-entities.md)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](configure-power-bi-integration.md)



