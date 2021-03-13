---
title: 発注書に記載されている商品の受取の記録
description: このトピックでは、商品の受取を発注書に直接記録する方法について説明します。
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d016df08850c75858c50b7f9a97b11b566d26cb0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022661"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>発注書に記載されている商品の受取の記録

[!include [banner](../../includes/banner.md)]

このトピックでは、商品の受取を発注書に直接記録する方法について説明します。 製品の受領を倉庫に登録しておき、後で発注書に記録することもできます。 このタスクは通常は購買担当者または買掛金勘定コーディネーターが行います。 このガイドで示されている例は、デモ データの会社 USMF で使用できます。 この例には、タスク ガイドとして手順を行うことができるように簡単な発注書を作成するステップが含まれています。 独自のデータでこの手順を使用している場合は、**商品の受取の記録** サブタスクから開始します。


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>商品の受取用の新しい発注書の準備
1. **ナビゲーション ウィンドウ > モジュール > 調達 > 発注書 > すべての発注書** に移動します。
2. **新規** を選択します。
3. **仕入先口座** フィールドに、`US-101` を入力します。
4. **OK** を選択します。
5. **品目番号** フィールドに、`M0001` を入力します。
6. **数量** フィールドに、`5` を入力します。
7. アクション ウィンドウで、**購買** を選択します。
8. **確認** を選択します。

## <a name="record-receipt-of-goods"></a>商品の受取の記録
1. アクション ウィンドウで、**入庫** を選択します。
2. **製品受領書** を選択します。 **数量** フィールドでは、入庫する数量に対するさまざまなオプションを選択できます。 たとえば、数量を事前に倉庫に登録した場合、**登録済数量** を選択できます。 この例では、**注文済数量** の値を使用します。
3. **概要** セクションを展開します。
4. **製品受領書** フィールドで、任意の値を入力します。 このフィールドは製品受領書仕訳帳で伝票として使用される参照を入力するために使用されます。  
5. **明細行** セクションを展開します。
6. **数量** を「4」に設定します。 ここで、注文の行ごとに、入庫中の数量を手動で指定できます。  
7. **OK** を選択します。 これで商品が発注書で入庫済みと記録され、これを反映して製品受領書仕訳帳がドキュメントとして作成されました。 製品受領書のアクションを使用して発注書で作成された仕訳帳を表示し、受け取り製品、および受け取り時期を確認できます。  

