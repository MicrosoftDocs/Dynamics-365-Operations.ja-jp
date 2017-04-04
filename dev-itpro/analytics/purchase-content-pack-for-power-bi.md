---
title: "購買が分析のPower BIの内容を使います"
description: "このトピックでは、Microsoft Power BIの分析の内容Packを含む内容が発注について説明します。 コンテンツ パックに含まれる説明し、コンテンツ パックを作成するのに使用するエンティティとデータ モデルに関する情報を提供するレポートにアクセスする方法。"
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

# <a name="purchase-spend-analysis-power-bi-content"></a>購買が分析のPower BIの内容を使います

このトピックでは、Microsoft Power BIの分析の内容Packを含む内容が発注について説明します。 コンテンツ パックに含まれる説明し、コンテンツ パックを作成するのに使用するエンティティとデータ モデルに関する情報を提供するレポートにアクセスする方法。

<a name="overview"></a>概要
--------

購買が予算を担当すると、購買部門のマネージャにMicrosoft Power BIの分析の内容Packを作成した使います。 これは発注支出を監視するためにそれらを行うために設計されています。 これは、工程にMicrosoft Dynamics 365からの購買のトランザクション データを使用して、全社的な発注の数のビューや仕入先、製品別の購買支出の詳細の両方を提供します。 レポートはしだいにで購買の変更が強調表示されます。 したがって、個別の仕入先、および製品の正で、負の支出の傾向に関する管理者に警告する場合でも、を使用できます。 グラフで、調達カテゴリおよび仕入先グループの購買支出を示します。 カテゴリおよび地域のマネージャが支出の実行のIDを変更する場合でも、これらのグラフを使用することができます。かもしがあります。 コンテンツ パックが販売マネージャを有効にし、予算を担当する次の方法で使って、マネージャは、購買を分析します:

-   会計年度の購買 (仕入先グループ、個別の仕入先、調達カテゴリ、およびユーザーの製品および仕入先の場所) 
-   前年比購買の変更 (仕入先グループ、調達カテゴリに) 

## <a name="accessing-the-content-pack"></a>コンテンツPackのアクセス
発注は、Microsoft Dynamics Lifecycle Services (LCS)の実装の資産として分析の内容Packを発行して、Microsoft Dynamics 365からアクセスできます。使います。 アクセス方法に関する詳細およびPower BI開いているレポートについては、" Microsoftパートナーおよび[] (能力Bi内容Microsoft partners.md) のLCSのPower BIの内容。

## <a name="metrics-that-are-included-in-the-content-pack"></a>メトリック コンテンツ パックに含まれる
購買が分析の内容Packを含む一連のメトリックスで構成されるレポートを使います。 これらのメトリック、グラフ、タイル、テーブルとして視覚化されます。 次の表に、コンテンツPackのビジュアル化の概要を示します。

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
<th>Tiles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>仕入先からの購買</td>
<td><ul>
<li>注文に別上位10の仕入先 (続いて上げ横棒グラフ) </li>
<li>仕入先グループ、または国/名前 (円グラフ) による購入の合計</li>
<li>仕入先グループ、または国/名前 (円柱グラフ) によって発注</li>
<li>仕入先グループ、または国/名前 (円柱グラフ) 別の平均購買</li>
</ul></td>
<td><ul>
<li>購買の合計</li>
<li>YOYの購買の増加</li>
<li>合計#仕入先</li>
<li>有効な仕入先の合計#</li>
</ul></td>
</tr>
<tr class="even">
<td>購買の副産物</td>
<td><ul>
<li>調達カテゴリまたは製品名 (円柱グラフ) によって発注</li>
<li>調達カテゴリまたは製品名 (円グラフ) による購入の合計</li>
<li>注文に別上位10の製品 (続いて上げ横棒グラフ) </li>
</ul></td>
<td><ul>
<li>製品の合計#</li>
<li>製品の合計の合計有効な製品の割合#</li>
<li>80%の発注を占める製品の数</li>
</ul></td>
</tr>
<tr class="odd">
<td>period*によって発注</td>
<td><ul>
<li>月/日 (円柱グラフ) ごとに表示</li>
<li>累計発注YOYの差異のグラフ (伝播) </li>
<li>購入の合計YOYの増加 (円柱グラフ) </li>
<li>調達明細書 ()。</li>
</ul></td>
<td><ul>
<li>YOYの購買の増加</li>
<li>YOYの購買の増加と</li>
</ul></td>
</tr>
<tr class="even">
<td>仕入先の場所によって発注</td>
<td><ul>
<li>市町村での発注</li>
<li>発注YOYの増加と</li>
<li>国別の発注</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>発注は時間での分析を使います</td>
<td><ul>
<li>月/日 (折れ線グラフ) ごとの購買の現在の年</li>
<li>注文の現在およびだけ (行と円柱グラフ) </li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>購買が仕入先別分析を使います</td>
<td><ul>
<li>購買 (じょうご) の上位10の仕入先の発注書]</li>
<li>見越計上された支出YOYの上位10の仕入先</li>
<li>品目YOY支出の上位10の仕入先</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* 今年度および調達カテゴリにだけ、乗算

## <a name="data-model-and-entities"></a>データ モデルおよびエンティティ
データが購買にレポートに使用するDynamics 365 for Operationsは、分析の内容Packを使います。 このデータは、インメモリに対して最適化されたMicrosoft SQLデータベースを使用して、エンティティの店舗で許可される) の測定単位として表されます。 エンティティの店舗に関する詳細については、" Dynamics [] (https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)からブログの転記のエンティティの店舗とのPower BIの統合。 このコンテンツPack) の測定単位は工程にMicrosoft Dynamics AX 2012、Microsoft Dynamics 365の発注のキューブに使用できる2012 R3) の測定のサブセットです。 エンティティの店舗のキューブ数の測定を許可するには、クライアントを配置有効にする必要があります。 詳細については、店舗のエンティティの数の測定の行について、手順を参照して、[Dynamics] (https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)からブログの転記のエンティティの店舗とのPower BIの統合。 次のキーの集計の測定単位は請求明細行のエンティティから使用して直接ので、コンテンツPack基準使用されます。

| エンティティ        | Key aggregate measurements | 工程365 for Operationsのデータ ソース | フィールド              | 説明                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| 請求明細行 | 購買                   | VendInvoiceTrans                            | 合計 (LineAmountMST)  | 会計通貨での金額 |

次の表に、請求明細行のエンティティのコンテンツ パックで計算される主要な測定単位を示します。

| 基準               | 計算                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| 購買の現在の年 | 購買の現在の年=合計 (「請求書のlines'entity_PLACEHOLDER\ [の購買\])                                             |
| 購買だけ    | 購買が昨年=計算 (合計 (「請求書のlines'entity_PLACEHOLDER\ [の購買\])、SAMEPERIODLASTYEAR日付の\[ (\]) \[日付)  |
| YOYの購買の増加   | YOYの購買の増加= \[購買の現在の年の\] – \[だけ\]                            |

詳細に粒度、深く分析的な情報を処理できるように計算の測定単位をスライスするでコンテンツPack次の主要分析コードのフィルタとして使用されます。

| エンティティ                 | 属性の例                                |
|------------------------|-------------------------------------------------------|
| 仕入先                | 仕入先グループ、仕入先の国または地域の仕入先名 |
| 製品               | 製品番号、製品名、品目グループの名前        |
| 調達カテゴリ | 調達カテゴリ、調達カテゴリの名前      |
| 法人         | 法人名                                     |
| 日付                  | 日付、年の相殺                                    |

既定では、コンテンツPackは、現在の暦年のデータが表示されます。 ただし、レポートのフィルタ セクションの日付のフィルタを変更できます。 さらに、会社のフィルタを変更できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](..\data-entities\data-entities.md)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](configure-power-bi-integration.md)



