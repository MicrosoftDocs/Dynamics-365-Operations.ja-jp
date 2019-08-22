---
title: 決済トランザクションを使用した顧客月次締め請求書の決済
description: 日本では、支払は月次締め請求書に対して行われ決済されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustConsInvoice_JP, CustTable, CustOpenTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 640ab48dd35c6974cc10af21517297cdcfd87b7b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848662"
---
# <a name="settle-customer-consolidated-invoices-by-using-settle-transactions"></a>決済トランザクションを使用した顧客月次締め請求書の決済

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、支払は月次締め請求書に対して行われ決済されます。



この手順では、決済トランザクションを使用した月次締め請求書の決済について説明します。



この手順を実行する前に、月次締め請求書が作成され確定済であること、および支払いが転記されていることを確認する必要があります。 

この手順は、デモ データ会社 JPMF を使用して作成されました。

1. [売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
    * 決済する月次締め請求書のステータスが「確定済」であることを確認します。  
    * 顧客の月次締め請求書を作成し確定する必要があります。  
2. [売掛金勘定] > [顧客] > [すべての顧客] の順に移動します。
3. 一覧で、選択された行をマークします。
    * 月次締め請求書を決済する顧客を選択します。  
4. [アクション] ウィンドウで、[回収] をクリックします。
5. [トランザクションの決済] をクリックします。
    * 決済する月次締め請求書の確定には、[締め ID] フィールドを使用します。  
6. 決済する明細行の検索と、その明細行のチェック ボックスの選択
    * この手順をタスク ガイドとして実行している場合は、レコードを選択するためにタスク ガイドのロックを解除しなければならない場合があります。  
7. 決済する別の明細行の検索と、その明細行のチェック ボックスの選択
    * この手順をタスク ガイドとして実行している場合は、レコードを選択するためにタスク ガイドのロックを解除しなければならない場合があります。  
8. [転記] をクリックします。
9. [売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
    * [月次締め請求書] のステータスが [決済済] に更新されていることを確認します。  

