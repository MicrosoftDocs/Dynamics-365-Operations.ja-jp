---
title: "現物更新と財務更新"
description: "このトピックでは、在庫数量を増減させるトランザクションのタイプについて、その概要を説明します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07ed503b7c441cb594e8e96ddcd9a81c0745a963
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="physical-and-financial-updates"></a>現物更新と財務更新

[!include[banner](../includes/banner.md)]


このトピックでは、在庫数量を増減させるトランザクションのタイプについて、その概要を説明します。 

在庫トランザクションは、Microsoft Dynamics 365 for Finance and Operations で現物更新および財務更新できます。 現物トランザクションと財務トランザクションによっては、在庫数量を増加または減少させるものがあります。

## <a name="physical-increases"></a>現物の増加
現物トランザクションが転記されると、トランザクション レコードのステータスは [**入庫済**] になります。 次のトランザクションは現物の増加と見なされます。

-   発注書入庫
-   販売注文梱包明細票返品
-   製造オーダーの終了を報告
-   製造オーダー ピッキング リストの副産物

## <a name="financial-increases"></a>財務上の増加
財務入庫トランザクションが転記されると、数量を増加させるトランザクション レコードのステータスは [**購買済**] になります。 次のトランザクションは、財務上の増加と見なされます。

-   仕入先請求書
-   返品用販売注文請求書
-   製造オーダー原価計算
-   振替、損益、棚卸、部品表、移動などの正の数量の在庫仕訳帳

## <a name="transactions-that-increase-quantity"></a>数量を増加させるトランザクション
数量を増加させるトランザクションは移動平均原価価格で転記されます。 Finance and Operations は、財務的に追跡される在庫分析コードごとに、各トランザクションの原価を基準とする移動平均原価価格を計算します。 移動平均原価価格については、[[移動平均原価価格](running-average-cost-price.md)] を参照ください。

## <a name="transactions-that-decrease-quantity"></a>数量を減少させるトランザクション
Finance and Operations は、在庫にどの在庫モデルが関連付けられているかに関係なく、数量を減少させるトランザクションが転記されるときは、計算済みの移動平均原価価格を使用します。 転記される前に、数量を減少させるトランザクションが別のトランザクションにすでにマークされていてはいけません。 現物手持在庫がマイナスになる場合、Finance and Operations は [**品目**] ページで品目に対して定義されている在庫原価を使用します。 **メモ:** マルチサイト機能が有効になっている場合、この原価は、[**既定の注文設定**] ページでサイトに対して定義されている在庫原価になります。

## <a name="physical-issues-vs-financial-issues"></a>現物払出と財務払出
現物払出トランザクションが転記されると、トランザクション レコードのステータスは [**控除済**] になります。 次のトランザクションは現物払出と見なされます。

-   製造オーダー ピッキング リスト仕訳帳
-   販売注文梱包明細票
-   発注書梱包明細返品

財務トランザクションを転記すると、トランザクション レコードのステータスが [**売却済**] になります。 次のトランザクションは財務払出と見なされます。

-   製造オーダーの終了
-   販売注文請求書
-   仕入先請求書返品
-   振替、損益、棚卸、部品表、移動などの負の数量の在庫仕訳帳

数量を減少させるトランザクションは移動平均原価価格で転記されます。 したがって、各品目に割り当てられている在庫モデルに基づいて、出庫トランザクションが入庫トランザクションに対して決済されるために、在庫原価計算手順が必要です。




