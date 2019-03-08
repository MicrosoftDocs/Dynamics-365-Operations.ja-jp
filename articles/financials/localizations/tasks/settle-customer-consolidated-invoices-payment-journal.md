---
title: 支払仕訳帳を使用した顧客月次締め請求書の決済
description: 日本では、支払は月次締め請求書に対して行われ決済されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustConsInvoice_JP, LedgerJournalTable, LedgerJournalTransCustPaym, CustPaymProposalEdit
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef10c6b6f41235fcfe039980ef8579bb7b4dcea6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371058"
---
# <a name="settle-customer-consolidated-invoices-by-using-a-payment-journal"></a>支払仕訳帳を使用した顧客月次締め請求書の決済

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、支払は月次締め請求書に対して行われ決済されます。



この手順では、支払仕訳帳と支払提案機能を使用した月次締め請求書の決済について説明します。 



この手順を完了する前に、月次締め請求書が作成され確定済であることを確認します。 



この手順は、デモ データ会社 JPMF を使用して作成されました。

1. [売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
2. 後で参照するために、[締め ID] フィールドの値をメモします。
    * デモ データ会社 JPMF の JPMF-000002 を使用できます。  
3. [売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
4. [新規] をクリックします。
5. [名前] フィールドに値を入力します。
6. [明細行] をクリックします。
7. [支払提案] をクリックします。
8. [支払提案の作成] をクリックします。
9. [詳細パラメーター] セクションを展開します。
10. [締め ID] フィールドに値を入力します。
    * [月次締め請求書] ページで、事前にメモした値を使用できます。  
11. [OK] をクリックします。
12. [支払の作成] をクリックします。
    * 支払明細行が提案に基づいて生成されていることを確認します。  [転記日] を入力します。  
    * 1 件の月次締め請求書に関連付けられている請求書が複数ある場合は、支払仕訳帳に複数の明細行を生成することができます。  
13. [転記] をクリックします。
14. [売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
    * 月次締め請求書のステータスが [決済済] に更新されていることを確認します。  

