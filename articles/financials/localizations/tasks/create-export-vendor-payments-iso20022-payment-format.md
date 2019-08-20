---
title: ISO20022 支払形式を使用した仕入先支払の作成とエクスポート
description: この手順では、仕入先支払仕訳帳で支払明細行を作成する方法、および ISO2022 口座振替の例を使用して仕入先支払ファイルを生成する方法を示します。
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848994"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>ISO20022 支払形式を使用した仕入先支払の作成とエクスポート

[!include [task guide banner](../../includes/task-guide-banner.md)]

このトピックでは、仕入先支払仕訳帳で支払明細行を作成する方法、および ISO2022 口座振替の例を使用して仕入先支払ファイルを生成する方法を説明します。

これは、5 つのうち 5 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。 この例を完了するのにデモ データ DEMF を使用します。

## <a name="example"></a>例

1.  **買掛金勘定 > 支払 > 支払仕訳帳**の順に移動します。
2.  **新規** をクリックします。
3.  **名前**フィールドで値を入力または選択します。
4.  **明細行 > 支払提案 > 支払提案の作成**の順にクリックします。
5.  **対象に含めるレコード** セクションを展開します。
6.  **フィルター**をクリックします。
7.  一覧で、**仕入先テーブル**の行および**仕入先フィールド**を選択します。
8.  **基準**フィールドで、値を入力または選択します。 支払う仕入先トランザクションを選択するためのあらゆる基準を適用できます。この例では、DE-001 を仕入先として使用します。
12. **OK** をクリックします。
13. **OK** をクリックします。
14. **支払の作成**をクリックします。
15. ISO20022 支払ファイルを生成します。
    1.  **支払の生成**をクリックします。
    2.  **支払方法**フィールドで値を入力または選択します。
    3.  **ファイル名**フィールドに値を入力します。 この例では、EUR 支払が原因で、生成されたファイルは SEPAに準拠します。 他の通貨での支払いの生成には、ISO20022 口座振替や他の仕入先の支払形式も使用できます。
    4.  **銀行口座**フィールドで、値を入力または選択します。

