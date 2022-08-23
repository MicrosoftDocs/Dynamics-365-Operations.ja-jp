---
title: 月次締め請求書の対象とする顧客および販売注文の設定
description: 通常日本では、顧客はすべてのトランザクションに月次締め請求書を使用します。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CustTable, SalesTableListPage, SalesTable
ms.openlocfilehash: cbd5347c570f53f894b1542dec35a3341e036188
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283775"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
