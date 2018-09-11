--- 
title: "ISO20022 支払形式を使用した仕入先支払の作成とエクスポート"
description: "この手順では、仕入先支払仕訳帳で支払明細行を作成する方法、および ISO2022 口座振替の例を使用して仕入先支払ファイルを生成する方法を示します。"
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>ISO20022 支払形式を使用した仕入先支払の作成とエクスポート

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、仕入先支払仕訳帳で支払明細行を作成する方法、および ISO2022 口座振替の例を使用して仕入先支払ファイルを生成する方法を示します。 

この手順の作成に使用するデモ データの会社は DEMF です。

これは、5 つのうち 5 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。 この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。


## <a name="create-payment-lines"></a>支払明細行の作成
1. [買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. 一覧で、選択された行をマークします。
4. [名前] フィールドで値を入力または選択します。
5. [明細行] をクリックします。
6. [支払提案] をクリックします。
7. [支払提案の作成] をクリックします。
8. [対象に含めるレコード] セクションを展開します。
9. [フィルター] をクリックします。
10. 一覧で、[仕入先] テーブルの行および [仕入先] フィールドを選択します。
11. [基準] フィールドで、値を入力または選択します。
    * 支払う仕入先トランザクションを選択するためのあらゆる基準を適用できます。この例では、DE-001 を仕入先として使用します。  
12. [OK] をクリックします。
13. [OK] をクリックします。
14. [支払の作成] をクリックします。

## <a name="generate-an-iso20022-payment-file"></a>ISO20022 支払ファイルの生成


