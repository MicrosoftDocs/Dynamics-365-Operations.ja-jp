---
title: 月次締め請求書の対象とする顧客および販売注文の設定
description: 通常日本では、顧客はすべてのトランザクションに月次締め請求書を使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTableListPage, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1591cbcdc8fb083edb545aa2ae898f171273ec72
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138982"
---
# <a name="set-up-a-customer-and-sales-order-to-be-target-of-consolidated-invoice"></a>月次締め請求書の対象とする顧客および販売注文の設定

[!include [banner](../../includes/banner.md)]

通常日本では、顧客はすべてのトランザクションに月次締め請求書を使用します。 



このタスクを使用して、月次締め請求書を使用するための顧客および販売注文の設定方法について説明します。 



この手順では、JPMF デモ会社のデータを使用します。


## <a name="set-up-a-customer-to-be-a-target-of-consolidated-invoice"></a>月次締め請求書の対象とする顧客の設定
1. [売掛金勘定] > [顧客] > [すべての顧客] の順に移動します。
2. 一覧で、選択された行のリンクをクリックします。
3. [支払の既定値] セクションを展開します。
    * [支払条件] で [締日方法] が使用されていることを確認します。  
    * 方法が「締日」ではない場合、タスク ガイドのロックを解除し、[編集] をクリックしてこのフィールドを更新します。  
    * 顧客に対する月次締め日を指定します。  
    * このフィールドの更新には、[編集] をクリックする必要がある場合があります。  

## <a name="set-a-sales-order-to-be-target-of-consolidated-invoice"></a>月次締め請求書の対象とする販売注文の設定
1. [売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。
2. 一覧で、選択された行のリンクをクリックします。
3. [ヘッダー] をクリックします。
    * [締めの対象] スライダーが「はい」に設定されていることを確認します。  
    * スライダーが「いいえ」に設定されている場合、タスク ガイドのロックを解除し、[編集] をクリックしてこのフィールドを更新します。  

