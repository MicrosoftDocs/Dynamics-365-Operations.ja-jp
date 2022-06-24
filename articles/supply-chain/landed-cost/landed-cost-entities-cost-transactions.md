---
title: 原価トランザクション エンティティ
description: この記事では、配賦方法を選択して原価領域のコンテンツ間で原価の値を分割できる、原価トランザクション エンティティについて説明します。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3aabc1356eba27de797fa696dd928cb401d8501b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860815"
---
# <a name="cost-transaction-entities"></a>原価トランザクション エンティティ

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

## <a name="apportionment"></a>配賦

陸揚原価は、配賦方法を選択することで、原価領域のコンテンツ (航海、出荷コンテナーなど) に原価の価値を分割することができます。 配賦方法は、ビジネス ルールに基づく自動原価の構成の一部として設定されます。 これは、航海明細行の作成時にコストの一部として引き出されます。

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>データ エンティティで使用する配賦マッピングの構成

配送業者などの外部ソースから原価を作成する場合、その外部ソースは、原価価値を割り当てるための優先方法を指定できません。 配賦マッピングは、各原価タイプ コードの既定の配賦方法を定義します。 配賦マッピング テーブルは、Microsoft Dynamics 365 Supply Chain Management の **配賦マッピング** ページ (**陸揚原価 \> 原価計算設定 \>配賦マッピング**) からアクセスできます。

マッピングの組み合わせが定義され、原価トランザクション エンティティを使用して原価タイプ コードに一致する原価が作成される場合、マップされた配賦方法は、エンティティに指定された値の代わりに使用されます。

値がマッピング テーブルに存在せず、エンティティに値が指定されている場合は、指定された値が使用されます。

マッピング テーブルまたはエンティティに送信されたレコードのいずれにも値が存在しない場合、作成は失敗します。

### <a name="apportionment-mapping-itmapportionmentmapping"></a>配賦マッピング (ITMApportionmentMapping)

配賦マッピング エンティティ (`ITMApportionmentMapping`) は、配賦マッピング関係を作成し、ユーザーがレコードを作成または更新できるようにします。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦方法 | ITMApportionmentMapping.ApportionmentMethod | Int | 無効 | 無効 |
| 原価タイプ コード | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **有** | 無効 |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>航海原価 (ITMCostTransVoyageEntity)

航海原価エンティティ (`ITMCostTransVoyageEntity`) は、航海レベルで適用される航海原価トランザクションを作成します。 インポート プロセス中に、システムはエンティティに含まれる **カテゴリ** と **配賦方法** の値を使用して、航海のコンテンツに対して原価の値を割り当てる方法を決定します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦方法 | ITMCostTrans.ApportionmentMethod | Int | 無効 | 無効 |
| 原価価値 | ITMCostTrans.CostValue | Numeric(32, 6) | 無効 | 無効 |
| 通貨 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 無効 | **有** |
| 行番号 | ITMCostTrans.LineNum | Numeric(32, 16) | **有** | 無効 |
| リンクされた原価タイプ | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 最小原価 | ITMCostTrans.MinCostAmount | Numeric(32, 6) | 無効 | 無効 |
| カテゴリ | ITMCostTrans.ShipCostCategory | Int | 無効 | 無効 |
| 原価タイプ コード | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 会社 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 無効 | **有** |
| 航海 | ITMCostTrans.TransRecId | Nvarchar(20) | **有** | 無効 |
| 品目消費税グループ | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 無効 | 無効 |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>出荷コンテナーの原価 (ITMCostTransShippingContainerEntity)

出荷コンテナーの原価エンティティ (`ITMCostTransShippingContainerEntity`) は、出荷コンテナー レベルで適用される出荷コンテナー原価を作成します。 インポート プロセス中に、システムはエンティティに含まれる **カテゴリ** と **配賦方法** の値を使用して、出荷コンテナーのコンテンツに対して原価の値を割り当てる方法を決定します。

**集計**、**区間**、**リンクした区間** のフィールドは、**原価領域** の値が *出荷コンテナー* であるレコードに固有です。 したがって、他の原価領域のデータ エンティティには存在しません。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 集計 | ITMCostTrans.AggregatedCost | Int | 無効 | 無効 |
| 配賦方法 | ITMCostTrans.ApportionmentMethod | Int | 無効 | 無効 |
| 原価価値 | ITMCostTrans.CostValue | Numeric(32, 6) | 無効 | 無効 |
| 通貨 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 無効 | **有** |
| 行番号 | ITMCostTrans.LineNum | Numeric(32, 16) | **有** | 無効 |
| リンクされた原価タイプ | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 無効 | 無効 |
| リンクした区間 | ITMCostTrans.LinkLegId | Nvarchar(20) | 無効 | 無効 |
| 最小原価 | ITMCostTrans.MinCostAmount | Numeric(32, 6) | 無効 | 無効 |
| 出荷コンテナー | ITMCostTrans.TransRecId | Nvarchar(20) | **有** | 無効 |
| カテゴリ | ITMCostTrans.ShipCostCategory | Int | 無効 | 無効 |
| 原価タイプ コード | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 会社 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 無効 | **有** |
| 航海 | ITMCostTrans.TransRecId | Nvarchar(20) | **有** | 無効 |
| 区間 | ITMCostTrans.ShipLegId | Nvarchar(20) | 無効 | 無効 |
| 品目消費税グループ | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 無効 | 無効 |

## <a name="folio-costs-itmcosttransfolioentity"></a>フォリオ原価 (ITMCostTransFolioEntity)

フォリオ原価エンティティ (`ITMCostTransFolioEntity`) は、フォリオ レベルに適用される原価トランザクション レコードを作成します。 インポート プロセス中に、システムはエンティティに含まれる **カテゴリ** と **配賦方法** の値を使用して、各フォリオのコンテンツに対して原価の値を割り当てる方法を決定します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦方法 | ITMCostTrans.ApportionmentMethod | Int | 無効 | 無効 |
| 原価価値 | ITMCostTrans.CostValue | Numeric(32, 6) | 無効 | 無効 |
| 通貨 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 無効 | **有** |
| 行番号 | ITMCostTrans.LineNum | Numeric(32, 16) | **有** | 無効 |
| リンクされた原価タイプ | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 最小原価 | ITMCostTrans.MinCostAmount | Numeric(32, 6) | 無効 | 無効 |
| カテゴリ | ITMCostTrans.ShipCostCategory | Int | 無効 | 無効 |
| 原価タイプ コード | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 会社 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 無効 | **有** |
| フォリオ | ITMCostTrans.TransRecId | Nvarchar(20) | **有** | 無効 |
| 品目消費税グループ | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 無効 | 無効 |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>発注書の原価 (ITMCostTransPurchaseEntity)

発注書の原価エンティティ (`ITMCostTransPurchaseEntity`) は、発注書ヘッダーに適用される原価トランザクションを作成します。 インポート プロセス中に、システムはエンティティに含まれる **カテゴリ** と **配賦方法** の値を使用して、各フォリオのコンテンツに対して原価の値を割り当てる方法を決定します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦方法 | ITMCostTrans.ApportionmentMethod | Int | 無効 | 無効 |
| 原価価値 | ITMCostTrans.CostValue | Numeric(32, 6) | 無効 | 無効 |
| 通貨 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 無効 | **有** |
| 行番号 | ITMCostTrans.LineNum | Numeric(32, 16) | **有** | 無効 |
| リンクされた原価タイプ | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 最小原価 | ITMCostTrans.MinCostAmount | Numeric(32, 6) | 無効 | 無効 |
| 発注書 | ITMCostTrans.TransRecId | Nvarchar(20) | **有** | 無効 |
| カテゴリ | ITMCostTrans.ShipCostCategory | Int | 無効 | 無効 |
| 原価タイプ コード | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 会社 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 無効 | **有** |
| 品目消費税グループ | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 無効 | 無効 |

## <a name="item-costs-itmcosttransitementity"></a>品目原価 (ITMCostTransItemEntity)

品目原価エンティティ (`ITMCostTransItemEntity`) は、品目レベルに適用される原価トランザクションを作成します。 このエンティティは発注書明細行の品目に固有です。 原価の値は、明細行に完全に適用されます。

**調整金額** および **金額調整** のフィールドは、明細行レベルの原価領域に固有です。 したがって、他の原価領域のデータ エンティティには存在しません。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 調整金額 | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | 無効 | 無効 |
| 原価価値 | ITMCostTrans.CostValue | Numeric(32, 6) | 無効 | 無効 |
| 通貨 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 無効 | **有** |
| 行番号 | ITMCostTrans.LineNum | Numeric(32, 16) | **有** | 無効 |
| リンクされた原価タイプ | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 最小原価 | ITMCostTrans.MinCostAmount | Numeric(32, 6) | 無効 | 無効 |
| 発注書 | ITMCostTrans.TransRecId | Nvarchar(20) | **有** | 無効 |
| 発注書明細行番号 | ITMCostTrans.TransRecId | Nvarchar(20) | **有** | 無効 |
| カテゴリ | ITMCostTrans.ShipCostCategory | Int | 無効 | 無効 |
| 原価タイプ コード | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 会社 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 無効 | **有** |
| 品目消費税グループ | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 無効 | 無効 |
| 金額調整 | ITMCostTrans.ValueAdjustmentMethod | Int | 無効 | 無効 |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>移動明細行の原価 (ITMCostTransTransferLineEntity)

移動明細行の原価エンティティ (`ITMCostTransTransferLineEntity`) は、移動オーダー明細行レベルに適用される原価トランザクションを作成します。 これらの原価の値は、移動オーダー明細行に完全に適用されます。

**調整金額** および **金額調整** のフィールドは、明細行レベルの原価領域に固有です。 したがって、他の原価領域のデータ エンティティには存在しません。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 調整金額 | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | 無効 | 無効 |
| 原価価値 | ITMCostTrans.CostValue | Numeric(32, 6) | 無効 | 無効 |
| 通貨 | ITMCostTrans.CurrencyCode | Nvarchar(3) | 無効 | **有** |
| 行番号 | ITMCostTrans.LineNum | Numeric(32, 16) | **有** | 無効 |
| リンクされた原価タイプ | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 最小原価 | ITMCostTrans.MinCostAmount | Numeric(32, 6) | 無効 | 無効 |
| カテゴリ | ITMCostTrans.ShipCostCategory | Int | 無効 | 無効 |
| 原価タイプ コード | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | 無効 | 無効 |
| 会社 | ITMCostTrans.ShipDataArea | Nvarchar(4) | 無効 | **有** |
| 移動オーダー | ITMCostTrans.TransRecId | Nvarchar(20) | **有** | 無効 |
| 移動オーダー明細行番号 | ITMCostTrans.TransRecId | Nvarchar(20) | **有** | 無効 |
| 品目消費税グループ | ITMCostTrans.TaxItemGroup | Nvarchar(10) | 無効 | 無効 |
| 金額調整 | ITMCostTrans.ValueAdjustmentMethod | Int | 無効 | 無効 |

### <a name="transaction-table"></a>トランザクション テーブル

原価トランザクション レコードは、トランザクション テーブル番号 (`TransTableId`) の割り当てを通じて原価領域に関連付けられます。 特定のテーブル ID 番号が必要な場合は、これらの値に基づいてエンティティが分割されるため、エンティティは原価領域ごとに存在します。

トランザクション テーブル (`TransTableId`) の値は、原価トランザクション エンティティの選択において暗黙的に設定されます。

### <a name="calculated-fields"></a>計算済フィールド

次のフィールドは、航海レコードに対して特定のアクションが実行された場合にのみ設定されるため、原価トランザクション エンティティが使用されている場合、挿入または更新できません。

- **見積原価** – このフィールドは、航海 (発注書) の請求書を転記するか、振替を受ける場合に設定されます。
- **見積原価通貨** – このフィールドは、航海 (発注書) の請求書を転記するか、振替を受ける場合に設定されます。
- **実際原価** – このフィールドは、仕入先請求書が転記される際に設定されます。 原価に関連付けられています。

### <a name="find-auto-costs"></a>自動原価の検索

各原価領域 (航海、出荷コンテナなど) で使用できる **自動原価の検索** ボタンは、構成テーブルの情報から、その原価領域の原価トランザクションを更新する方法を指定します。 原価領域のボタンを選択すると、システムは、自動原価設定テーブルの現在の構成に基づいて、その原価領域の既存の原価をクリアし、新規レコードを作成します。

データ エンティティを使用して作成された原価トランザクション レコードには、インポート済みのフラグが設定されます。 これらのレコードは、自動原価設定テーブルから再作成されないので、**自動原価の検索** を選択しても削除されません。 ただし、インポート済みのフラグが設定されている原価トランザクション レコードは削除できます。

### <a name="linked-fields"></a>リンクされたフィールド

各原価トランザクションは、同じ原価領域の別のレコードに関連付けることができます。 このアソシエーションは、**リンクされた原価タイプ** フィールドで確立されます。 これにより、原価価値を別の原価の割合として計算できます。

**リンクされた原価タイプ** フィールドは、参照先のレコードが最初に処理された場合、またはテーブルに既に存在する場合にのみ検証できます。 出荷コンテナーの原価領域の原価にのみ使用される **リンクした区間** フィールドにも同じ要件が適用されます。
