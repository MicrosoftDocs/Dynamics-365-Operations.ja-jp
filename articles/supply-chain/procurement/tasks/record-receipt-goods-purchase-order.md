--- 
title: "発注書に記載されている商品の受取の記録"
description: "この手順では、商品の受取を発注書に直接記録する方法を示します。"
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>発注書に記載されている商品の受取の記録

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

この手順では、商品の受取を発注書に直接記録する方法を示します。 製品の受領を倉庫に登録しておき、後で発注書に記録することもできます。 このタスクは通常は購買担当者または買掛金勘定コーディネーターが行います。 このガイドで示されている例は、デモ データの会社 USMF で使用できます。 この例には、タスク ガイドとして手順を行うことができるように簡単な発注書を作成するステップが含まれています。 独自のデータでこの手順を使用している場合は、「商品の受取の記録」サブタスクから開始します。


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>商品の受取用の新しい発注書の準備
1. [調達] > [発注書] > [すべての発注書] の順に移動します。
2. [新規] をクリックします。
3. [仕入先] フィールドに「US-101」を入力します。
4. [OK] をクリックします。
5. [品目番号] フィールドに、「M0001」を入力します。
6. [数量] フィールドに「5」と入力します。
7. アクション ウィンドウで、[購買] をクリックします。
8. [確認] をクリックします。

## <a name="record-receipt-of-goods"></a>商品の受取の記録
1. アクション ウィンドウで、[入庫] をクリックします。
2. [製品受領書] をクリックします。
    * [数量] フィールドでは、入庫する数量に対するさまざまなオプションを選択できます。 たとえば、数量を事前に倉庫に登録した場合、[登録済数量] を選択できます。  この例では、[注文済数量] の値を使用します。   
3. [製品受領書] フィールドで、任意の値を入力します。
    * このフィールドは製品受領書仕訳帳で伝票として使用される参照を入力するために使用されます。  
4. [明細行] セクションを展開します。
5. 数量を '4' に設定します。
    * ここで、注文の行ごとに、入庫中の数量を手動で指定できます。  
6. [明細] セクションを折りたたみます。
7. [OK] をクリックします。
    * これで商品が発注書で入庫済みと記録され、これを反映して製品受領書仕訳帳がドキュメントとして作成されました。 製品受領書のアクションを使用して発注書で作成された仕訳帳を表示し、受け取り製品、および受け取り時期を確認できます。  


