---
title: "原価管理のPower BIの内容"
description: "このトピックに含まれるかが原価管理のPower BIの内容について説明します。 内容を作成するのに使用されるPower BIレポートへのアクセス方法を説明しデータ モデルおよびエンティティに関する情報を提供します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>原価管理のPower BIの内容

このトピックに含まれるかが原価管理のPower BIの内容について説明します。 内容を作成するのに使用されるPower BIレポートへのアクセス方法を説明しデータ モデルおよびエンティティに関する情報を提供します。

# <a name="overview"></a>概要

Microsoft Power BI **原価管理**内容は在庫を担当する組織の在庫会計士またはユーザーのために使用します。 Power BI **原価管理**内容は在庫および仕掛品(WIP)の在庫の原価を部門別に対象を一定期間にわたってドキュメントまたは業務情報を提供します。 この情報は、財務諸表への詳細な追加として使用できます。

## <a name="key-measures"></a>主には

+ 期首残高
+ 期末残高
+ 差分変更
+ 全体の増減額
+ エイジング

## <a name="key-performance-indicators"></a>主要業績評価指標
+ 在庫回転
+ 在庫の正確性

CostAggregatedCostStatementEntryEntityの基本データ ソースはCostStatementCache表です。 次の表は、データセットのキャッシュ フレームワークで管理されます。 既定では、テーブルは24時間に更新されますが、データ キャッシュ コンフィギュレーションの手動更新を有効にすることができます。 **、原価管理**または**原価分析**ワークスペースの手動更新を行うことができます。 CostStatementCacheの更新の実行後、サイトの更新されたデータの表示とパワーBI.comからODataの接続を更新する必要があります。 Power BIこのコンテンツの差異 (発注書、生産) のメジャーは標準原価の在庫方法によってvaluated品目にのみ関連します。 製造差異は有効な原価と実現原価の差額として計算されます。 製造差異は、製造オーダーのステータスがあるときに計算されます**終了する**。 製造差異のタイプに関する詳細については各タイプの計算方法、および[完了した製造オーダー] (https://technet.microsoft.com/en-us/library/gg242850.aspx)の差異の分析について。

## <a name="accessing-the-power-bi-content"></a>Power BIの内容のアクセス
Power BI **原価管理**内容はPowerBI.comから使用できます。 アクション データのMicrosoft Dynamics 365を関連付けたり読み込み方法の詳細については、" "を参照してください[] (PowerBI.com能力Biホームpage.md) からアクセスPower BIの内容。

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>メトリックPower BIに含まれる内容
内容は、レポートのページが表示されます。 各ページのは、メトリックで構成されます。グラフ、タイル、テーブルとして視覚化する。 次の表に、Power BI **原価管理**内容のビジュアル化の概要を示します。

| レポート ページ | グラフ | タイトル |
|---|---|---|
|全体的な在庫 (現在の期間で既定)  |正確性 |在庫します:<br>在庫終了残高<br>在庫差分変更<br>在庫差分変更率<br>|
| |在庫回転 | |
| |リソース グループによる在庫終了残高 | |
| |カテゴリ名のレベル1、カテゴリ名のレベル2で差分変更を在庫にします。| |
| |リソース グループとカテゴリ名のレベル3による購買差異 | |
|サイト (現在の期間ごとの既定値) による在庫 |サイト名とリソース グループによる在庫終了残高 | |
| |サイト名とリソース グループ別の在庫有効 | |
| |市町村とリソース グループによる在庫終了残高 | |
|リソース グループ (現在の期間ごとの既定値) による在庫 |在庫は | |
| |リソース グループ別量目録精度 | |
| |リソース グループによって有効量目録 | |
|在庫YOY (既定の現在の年と前年度)  |在庫は | |
| |在庫KPI:<br>在庫回転<br>在庫の正確性 | |
| |年とリソース グループによる在庫終了残高 | |
| |年とカテゴリ名のレベル3による購買差異 | |
|在庫老化 (現在の年で既定)  |四半期、およびリソース グループによる在庫老化 | |
| |四半期、サイト名による在庫老化 | |
|全体的な仕掛品 (現在の期間で既定)  |カテゴリ名のレベル1、カテゴリ名のレベル2での仕掛品の増減額 |進行中の作業 (WIPの基準:<br>仕掛品の終了残高<br>仕掛品の増減額<br>仕掛品の差分変更率<br> |
| |リソース グループとカテゴリ名のレベル3別の製造差異 | |
| |リソース グループによってWIPの増減額 | |
|サイト (現在の期間ごとの既定値) での仕掛品 |進行中の作業 (WIPのメジャー | |
| |サイト名とカテゴリ名のレベル2での仕掛品の増減額 | |
| |サイト名とカテゴリ名のレベル3別の製造差異 | |

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
工程365 for OperationsデータがPower BI **原価管理**コンテンツのレポート ページの情報も使用されます。 このデータは、インメモリに対して最適化されたMicrosoft SQLデータベースを使用して、エンティティの店舗で許可される) の測定単位として表されます。 詳細については、"エンティティの[店舗] (能力Bi統合エンティティstore.md) にPower BI統合の概要。 次のキーの集計の測定単位でコンテンツの基準として使用されます。

| エンティティ            | 目標の測定単位)。 | 工程365 for Operationsのデータ ソース | フィールド             | 説明                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| [入力 | 差分変更                | CostAggregatedCostStatementEntryEntity      | 合計金額\[ (\])    | 会計通貨の金額 |
| [入力 | 差分の数量の変更       | CostAggregatedCostStatementEntryEntity      | 合計数量\[ (\])  |                                   |

コンテンツのデータセットの複数の計算メジャーを作成するのに者) の測定単位をどのように使用されている次の表に表示されます。

| 基準                                 | 測定の計算方法                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 期首残高                       | \[期末残高の\]-\[減額\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 開始残高の数量              | \[期末残高の数量の\]-\[減額の数量\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 期末残高                          | 計算 (合計金額\[ (\])、フィルタ (ALLEXCEPT (「会計カレンダー、「会計calendars'entity_PLACEHOLDER\ [LedgerRecId\]「entities'entity_PLACEHOLDER\ [ID\]に「entities'entity_PLACEHOLDER\ [の名前\]「Ledgers'entity_PLACEHOLDER\ [通貨\]「のLedgers'entity_PLACEHOLDER\ [の説明\]「Ledgers'entity_PLACEHOLDER\ [名前\])、「会計calendars'entity_PLACEHOLDER\ [の日付\]&lt;=最大値 (「会計calendars'entity_PLACEHOLDER\ [の日付) \]))                                                                                                                                                                                            |
| 終了残高の数量                 | 計算 (合計数量\[ (\])、フィルタ (ALLEXCEPT (「会計カレンダー、「会計calendars'entity_PLACEHOLDER\ [LedgerRecId\]「entities'entity_PLACEHOLDER\ [ID\]に「entities'entity_PLACEHOLDER\ [の名前\]「Ledgers'entity_PLACEHOLDER\ [通貨\]「のLedgers'entity_PLACEHOLDER\ [の説明\]「Ledgers'entity_PLACEHOLDER\ [名前\])、「会計calendars'entity_PLACEHOLDER\ [の日付\]&lt;=最大値 (「会計calendars'entity_PLACEHOLDER\ [の日付) \]))                                                                                                                                                                                          |
| 開始残高の在庫します。             | 計算 (\[開始残高\]「" entries'entity_PLACEHOLDER\ [ステートメントのタイプ\] = 「在庫」)                                                                                                                                                                                                                                                                                                                                                                                       |
| 在庫終了残高                | 計算 (\[終了残高\]「" entries'entity_PLACEHOLDER\ [ステートメントのタイプ\] = 「在庫」)                                                                                                                                                                                                                                                                                                                                                                                          |
| 在庫差分変更                    | 計算 (\[増減額\]「" entries'entity_PLACEHOLDER\ [ステートメントのタイプ\] = 「在庫」)                                                                                                                                                                                                                                                                                                                                                                                              |
| 現金同等の数量の在庫します。           | 計算 (\[減額の数量\]「明細書entries'entity_PLACEHOLDER\ [明細書タイプ\] = 「在庫」)                                                                                                                                                                                                                                                                                                                                                                                     |
| 在庫差分変更率                  |  (\[在庫終了残高\] = 0、0の \[在庫現金同等の\] / \[在庫終了残高\])                                                                                                                                                                                                                                                                                                                                                                            |
| 在庫金額を有効にします。                |  (または (\[平均在庫残高\]&lt;0 = \[在庫払出\] = 0\] 販売するか &gt;、または消費される)、0のABS (販売された\[在庫を出庫または\]消費される) /\[平均在庫残高\])                                                                                                                                                                                                                                                                                                   |
| 平均残高の在庫します。               |  (\[在庫期末残高の\] + \[在庫\[開始残高の\]) /2                                                                                                                                                                                                                                                                                                                                                                                                       |
| 在庫販売されたか、または消費された問題       | \[在庫は\] + \[在庫によって消費される材料の原価\]販売します                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 在庫によって消費される材料の原価        | 計算 (\[在庫\[増減額\]「明細書entries'entity_PLACEHOLDER\ [カテゴリ名]レベル2\_=\] 「ConsumedMaterialsCost」)                                                                                                                                                                                                                                                                                                                                                             |
| 販売された在庫                          | 計算 (\[在庫\[増減額\]「明細書entries'entity_PLACEHOLDER\ [カテゴリ名]レベル2\_=\] 「の販売済」)                                                                                                                                                                                                                                                                                                                                                                              |
| 金額精度が在庫にします。            |  (\[在庫 &lt;終了残高は\] (または0 (\[在庫\] 計算済金額の &lt;&gt; 0 \[在庫終了残高\]&lt; 0)、0、1) の最大値 (0 (\[在庫終了残高ABS ]\] (\[在庫\]計算済金額)) \[在庫/期末残高\]))                                                                                                                                                                                                                               |
| 在庫計算済金額                | 計算され (\[在庫\[増減額\]「明細書entries'entity_PLACEHOLDER\ [カテゴリ名]レベル3\_=\] 「」、)                                                                                                                                                                                                                                                                                                                                                                          |
| 在庫エイジング                         |  (ISBLANK (最大値 (「会計calendars'entity_PLACEHOLDER\ [の日付) \]) 空白、()、最大値 (0、最小値 (\[在庫数量によって\]\[在庫老化の期末残高の数量の\] - \[在庫老化将来的に入力されます\]入庫の数量が表示されます))) \* \[在庫avgの単位原価\]                                                                                                                                                                                                                                |
| 在庫の数量によって入力されます       | \[ (\]\[minDate = \[\]計算しますminDateAllSelected (\[増減額在庫の数量\]「明細書entries'entity_PLACEHOLDER\ [数量\]&gt;\] 0のフィルタ (ALLEXCEPT (「会計カレンダー、「会計calendars'entity_PLACEHOLDER\ [LedgerRecId\]「entities'entity_PLACEHOLDER\ [ID\]entities'entity_PLACEHOLDER\ [名前に「\]「のLedgers'entity_PLACEHOLDER\ [の通貨\]「Ledgers'entity_PLACEHOLDER\ [説明\]「のLedgers'entity_PLACEHOLDER\ [の名前\])、「会計calendars'entity_PLACEHOLDER\ [の日付\]&lt;=最大値 (「会計calendars'entity_PLACEHOLDER\ [の日付) \])) 再計算します (\[増減額在庫の数量\]「" entries'entity_PLACEHOLDER\ [数量\]&gt;\] 0))  |
| 老化の期末残高の数量の在庫します。 | \[在庫終了残高の数量+計算\] (\[増減額在庫の数量\]のフィルタ (ALLEXCEPT (「会計カレンダー、「会計calendars'entity_PLACEHOLDER\ [LedgerRecId\]「entities'entity_PLACEHOLDER\ [ID\]に「entities'entity_PLACEHOLDER\ [の名前\]「Ledgers'entity_PLACEHOLDER\ [通貨\]「のLedgers'entity_PLACEHOLDER\ [の説明\]「Ledgers'entity_PLACEHOLDER\ [名前\])、「calendars'entity_PLACEHOLDER\ [の日付の\] 会計 &gt; 最大値 (「会計calendars'entity_PLACEHOLDER\ [の日付) \]))                                                                                                                                  |
| 在庫の入庫を老化  | 計算 (\[在庫\[増減額\]「明細書entries'entity_PLACEHOLDER\ [金額\]&gt; 0のフィルタ (ALLEXCEPT (「会計カレンダー、「会計calendars'entity_PLACEHOLDER\ [LedgerRecId\]「entities'entity_PLACEHOLDER\ [ID\]entities'entity_PLACEHOLDER\ [名前に「\]「のLedgers'entity_PLACEHOLDER\ [の通貨\]「Ledgers'entity_PLACEHOLDER\ [説明\]「のLedgers'entity_PLACEHOLDER\ [の名前\]) 「calendars'entity_PLACEHOLDER\ [の日付の\] 会計 &gt; 最大値 (「会計calendars'entity_PLACEHOLDER\ [の日付) \]))                                                                                                                                              |
| avgの単位原価の在庫します。                 | 計算 (\[在庫期末残高の\] / \[在庫終了残高の数量ALLEXCEPT (\]、「会計カレンダー、「会計calendars'entity_PLACEHOLDER\ [LedgerRecId\]「entities'entity_PLACEHOLDER\ [ID\]に「entities'entity_PLACEHOLDER\ [の名前\]「Ledgers'entity_PLACEHOLDER\ [通貨\]「のLedgers'entity_PLACEHOLDER\ [の説明\]「Ledgers'entity_PLACEHOLDER\ [の名前\]))                                                                                                                                                                                                                  |
| 購買差異                      | 計算 (合計金額\[ (\])、「" entries'entity_PLACEHOLDER\ [カテゴリ名]レベル2\_=\] 「のステータスに入れられた」、「" entries'entity_PLACEHOLDER\ [ステートメントのタイプ\] = 「変動」)                                                                                                                                                                                                                                                                                                                               |
| 仕掛品の開始残高                   | 計算 (\[開始残高\]「" entries'entity_PLACEHOLDER\ [ステートメントのタイプ\] = 「仕掛品」)                                                                                                                                                                                                                                                                                                                                                                                             |
| 仕掛品の終了残高                      | 計算 (\[終了残高\]「" entries'entity_PLACEHOLDER\ [ステートメントのタイプ\] = 「仕掛品」)                                                                                                                                                                                                                                                                                                                                                                                                |
| 仕掛品の増減額                          | 計算 (\[増減額\]「" entries'entity_PLACEHOLDER\ [ステートメントのタイプ\] = 「仕掛品」)                                                                                                                                                                                                                                                                                                                                                                                                    |
| 仕掛品の差分変更率                        |  (\[) の終了残高\] = 0、0の \[仕掛品の増減額の\] / \[仕掛品の終了残高\])                                                                                                                                                                                                                                                                                                                                                                                              |
| 製造差異                    | 計算 (合計金額\[ (\])、「" entries'entity_PLACEHOLDER\ [カテゴリ名]レベル2\_=\] 「ManufacturedCost」、「" entries'entity_PLACEHOLDER\ [明細書タイプ\] = 「変動」)                                                                                                                                                                                                                                                                                                                       |
| カテゴリ名]レベル1                 | 移動する (\[カテゴリ名]レベル1\_\]「なし「、「なし「、「NetSourcing 「、「正味ソース「、「NetUsage 「、「正味使用「、「NetConversionCost 「、「正味処理費「、「NetCostOfGoodsManufactured 「」、製造された品目の正味原価BeginningBalance 「「、「開始残高」)                                                                                                                                                                                                          |
| カテゴリ名]レベル2                 | 移動する (\[カテゴリ名]レベル2\_\]「なし「、「なし「、「有効に入れられて「、「有効に入れられて「、「処分およびさせられてに「、「処分およびさせられてに「、「転送済「、「転送済「、「販売済「、「販売済「、「ConsumedMaterialsCost 「、「消費された原材料の原価ConsumedManufacturingCost 「、「「、「消費された製造原価「、「ConsumedOutsourcingCost 「、「消費された外注の原価「、「ConsumedIndirectCost 「、「消費された間接原価ManufacturedCost 「、「「、「製造原価「、「変動「、「変動」)                             |
| カテゴリ名]レベル3                 | 切り替える。(\[カテゴリ名]レベル3\_\]「なし「、「なし「、「棚卸「、「なし「、「ProductionPriceVariance 「、「生産価格」、「QuantityVariance 「、「数量「、「SubstitutionVariance 「、「代替「、「ScrapVariance 「、「仕損「、「LotSizeVariance 「、「ロットサイズ「、「RevaluationVariance 「、「再評価「、「PurchasePriceVariance 「、「購買価格「、「CostChangeVariance 「、「原価変更「、「RoundingVariance 「、「変動」四捨五入します)                                                    |

合計の測定単位をスライスするも大きく粒度を高め、より深く分析的な情報を提供するには、次の主要な分析コードは、フィルタ使用されます。

| エンティティ           | 属性の例                       |
|------------------|----------------------------------------------|
| エンティティ         | IDの名前                                     |
| 会計カレンダー | カレンダー、月、期間、四半期、年       |
| KPI 目標        | 在庫精度の目標、在庫有効期間 |
| 元帳          | 通貨、名前、説明                  |
| サイト            | IDの名前、国、市町村                      |

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](..\data-entities\data-entities.md)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](configure-power-bi-integration.md)



