---
title: 仕入先請求書エンティティ
description: この記事では、仕入先請求書エンティティに関する情報を提供します。これを利用して、内部原価または外部から派生した原価に対し、原価タイプ コードを構成できます。
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
ms.openlocfilehash: 171b383e1549babd76fd18e4932436a66aa62cc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873930"
---
# <a name="vendor-invoice-entities"></a>仕入先請求書エンティティ

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

**陸揚原価** モジュールを使用すると、内部原価または外部から派生した原価に対し、原価タイプ コードを構成できます。 原価がビジネスの外部である場合は、サービス プロバイダーによる請求書が必要です。 この請求書は航海に関連付けられる請求仕訳帳として処理され、その請求書の額は航海の 1 つ以上の費用に配賦できます。

仕入先請求書エンティティによって、同じ原価タイプ コードを共有する航海の 1 つ以上の原価に、仕訳明細行の額を配賦できます。

請求仕訳帳ヘッダーと請求仕訳帳明細行が存在する場合にのみ、原価を配賦できます。

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>仕入先航海原価配賦 (ITMLedgerJournalCostLinesVoyagesEntity)

仕入先航海原価配賦データ エンティティによって、航海原価領域に適用する 1 つ以上の原価に、仕入先請求書明細行を配賦できます。 `ITMLedgerJournalCostLinesVoyagesEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦済金額 | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | 無効 | 無効 |
| 原価トランザクション明細行番号 | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳明細行番号 | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳番号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **有** | 無効 |
| 航海 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **有** | 無効 |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>仕入先出荷コンテナー原価配賦 (ITMLedgerJournalCostLinesContainersEntity)

仕入先出荷コンテナー原価配賦データ エンティティによって、輸送コンテナ原価領域に適用する 1 つ以上の原価に、仕入先請求書明細行を配賦できます。 `ITMLedgerJournalCostLinesContainersEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦済金額 | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | 無効 | 無効 |
| 出荷コンテナー | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **有** | 無効 |
| 原価トランザクション明細行番号 | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳明細行番号 | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳番号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **有** | 無効 |
| 航海 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **有** | 無効 |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>仕入先フォリオ原価配賦 (ITMLedgerJournalCostLinesFoliosEntity)

仕入先フォリオ原価配賦データ エンティティによって、フォリオ原価領域に適用する 1 つ以上の原価に、仕入先請求書明細行を配賦できます。 `ITMLedgerJournalCostLinesFoliosEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦済金額 | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | 無効 | 無効 |
| 原価トランザクション明細行番号 | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **有** | 無効 |
| フォリオ | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **有** | 無効 |
| 仕訳帳明細行番号 | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳番号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **有** | 無効 |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>仕入先発注書原価配賦 (ITMLedgerJournalCostLinesPurchTableEntity)

仕入先発注書原価配賦データ エンティティによって、発注書原価領域に適用する 1 つ以上の原価に、仕入先請求書明細行を配賦できます。 `ITMLedgerJournalCostLinesPurchTableEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦済金額 | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | 無効 | 無効 |
| 原価トランザクション明細行番号 | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳明細行番号 | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳番号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **有** | 無効 |
| 発注書 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **有** | 無効 |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>仕入先品目原価配賦 (ITMLedgerJournalCostLinesPurchLineEntity)

仕入先品目原価配賦データ エンティティによって、品目原価領域に適用する 1 つ以上の原価に、仕入先請求書明細行を配賦できます。 品目原価領域は発注書明細行の原価をカバーします。 `ITMLedgerJournalCostLinesPurchLineEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦済金額 | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | 無効 | 無効 |
| 原価トランザクション明細行番号 | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳明細行番号 | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳番号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **有** | 無効 |
| 発注書 | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **有** | 無効 |
| 発注書明細行番号 | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **有** | 無効 |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>仕入先移動オーダー明細行原価配賦 (ITMLedgerJournalCostLinesTransferLineEntity)

仕入先移動オーダー明細行原価配賦データ エンティティによって、移動オーダー明細行原価領域に適用する 1 つ以上の原価に、仕入先請求書明細行を配賦できます。 `ITMLedgerJournalCostLinesTransferLineEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配賦済金額 | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | 無効 | 無効 |
| 原価トランザクション明細行番号 | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳明細行番号 | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **有** | 無効 |
| 仕訳帳番号 | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **有** | 無効 |
| 移動オーダー | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **有** | 無効 |
| 移動オーダー明細行番号 | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **有** | 無効 |

### <a name="reference-table"></a>参照テーブル

航海原価明細行は、原価トランザクション レコードと直接関連付けられています。 このレコードは **参照テーブル ID** 値を含みます。 この値は各原価領域で一意です (航海、出荷コンテナーなど)。 データ エンティティを使用して作成したデータに対し、特定のテーブル番号を参照する場合は、**参照テーブル ID** 値に基づいてエンティティを分割します。

参照テーブル (`RefTableId`) とトランザクション タイプ (`TransType`) の値は、陸揚原価購買注文明細行または陸揚原価移動明細行エンティティの選択で暗黙的に含まれます。

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>仕入先請求仕訳帳明細行 (VendorInvoiceJournalLineEntity)

仕訳明細行値を **陸揚原価** モジュールが含む 1 つ以上の原価に配賦する前に、仕訳明細行を原価領域に関連付ける必要があります。 この機能に対応するためには、**陸揚原価** モジュールに仕訳明細行テーブル (`LedgerJournalTrans`) に新しいフィールドをいくつか追加します。

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>仕入先請求仕訳帳明細行エンティティに追加したフィールド

次の表に、**陸揚原価** モジュールが仕入先請求書仕訳明細行エンティティ (`VendorInvoiceJournalLineEntity`) に追加するフィールドを示します。 これらのフィールドによって、システムは仕訳明細行を作成し、それらに対して原価を配賦できます。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 原価領域 | LedgerJournalTrans.ITMCostArea | Int | 無効 | 無効 |
| 原価タイプ コード | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | 無効 | 無効 |

### <a name="mainoffset-account"></a>主勘定/相手勘定

陸揚原価航海に関連付けられた請求仕訳帳明細行の主勘定/相手勘定は、原価タイプ コードによって決定されます。 請求仕訳帳明細行が原価タイプ コードを含む場合、シナリオに応じて、主勘定または相手勘定のいずれかとしてコードの精算勘定を使用します。

- **単一明細行仕訳帳** – 主勘定 (つまり仕入先勘定) を定義して原価タイプ コードを指定する場合、その原価タイプ コードの精算勘定の値は相手勘定に入力されます。
- **複数明細行仕訳帳** – 主勘定を定義せず原価タイプ コードを指定する場合、その原価タイプ コードの精算勘定の値は主勘定に入力されます。 仕入先に貸方記入した仕訳明細行は、原価タイプ コードを参照しません。

## <a name="sequencing"></a>優先順位

仕訳帳と仕訳明細行テーブルの依存関係のため、最初に航海レコードを作成する必要があります。 航海明細行は、航海、出荷コンテナー、フォリオの作成後にのみ作成できます。

航海請求書を配賦するために、システムはエンティティを次の順序で処理する必要があります。

1. 請求仕訳帳ヘッダー (`VendInvoiceJournalHeaderEntity`)
1. 請求仕訳帳明細行 (`VendInvoiceJournalLineEntity`)
1. 陸揚原価の配賦 (`ITMLedgerJournalEntities`)
