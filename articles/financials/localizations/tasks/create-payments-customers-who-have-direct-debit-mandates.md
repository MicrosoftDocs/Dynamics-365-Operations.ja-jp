--- 
title: "口座引落の委任状がある顧客の支払の作成"
description: "この手順では、口座引落がコンフィギュレーションされており支払対象の請求書のある顧客用に、ISO20022 の口座引落支払ファイルを生成するプロセスを説明します。"
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: acd6a8076288d8d1d1aa05af33e306c6a29780f7
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>口座引落の委任状がある顧客の支払の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、口座引落がコンフィギュレーションされており支払対象の請求書のある顧客用に、ISO20022 の口座引落支払ファイルを生成するプロセスを説明します。 請求書の作成および転記はオプションです。 支払われる請求書の代わりに、顧客が支払を行うシナリオをサポートするために、支払ファイルを生成する前に仕訳帳の委任状を選択できます。



この手順の作成に使用するデモ データの会社は DEMF です。



これは、5 つのうち 5 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。 このタスクを完了するために、以前のタスクを完了している必要があります。 まず、顧客支払電子申告コンフィギュレーションをインポートし、支払方法をコンフィギュレーションする必要があります。また会社および顧客情報を設定する必要があります。 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>口座引落情報を含む自由書式の請求書を転記
1. [売掛金勘定] > [請求書] > [すべての自由書式の請求書] の順に移動します。
2. [新規] をクリックします。
3. [顧客口座] フィールドで値を入力または選択します。
    * たとえば、[DE-010] を選択します。  
4. [支払方法] フィールドで値を入力または選択します。
    * 例えば、 [電子] を選択します。  
5. [口座引落の委任状 ID] フィールドで、値を入力または選択します。
6. [行の追加] をクリックします。
7. [説明] フィールドで値を入力します。
8. [主勘定] フィールドに、目的の値を指定します。
9. [単価] フィールドに数値を入力します。
10. [転記] をクリックします。
11. [OK] をクリックします。

## <a name="create-a-payment"></a>支払の作成
1. [売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで値を入力または選択します。
4. [明細行] をクリックします。
5. [支払提案] をクリックします。
6. [支払提案の作成] をクリックします。
7. [対象に含めるレコード] セクションを展開します。
8. [フィルター] をクリックします。
9. リストで、[顧客トランザクション] テーブルの行、および [支払方法] フィールドを選択します。
    * 支払するための顧客トランザクションの選択には、すべての基準を適用できます。 この例では、トランザクションをフィルターする支払方法として [電子] を使用します。  
10. [基準] フィールドで、値を入力または選択します。
11. [OK] をクリックします。
12. [OK] をクリックします。
13. [支払の作成] をクリックします。

## <a name="generate-a-payment-file"></a>支払ファイルの生成


