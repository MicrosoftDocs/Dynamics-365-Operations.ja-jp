---
title: "現物更新と財務更新"
description: "このトピックでは、在庫数量を増減させるトランザクションのタイプについて、その概要を説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d68006c756f6b29804cad1d05db9ced2bd33897d
ms.lasthandoff: 03/31/2017


---

# <a name="physical-and-financial-updates"></a>現物更新と財務更新

このトピックでは、在庫数量を増減させるトランザクションのタイプについて、その概要を説明します。 

在庫トランザクションは、Microsoft Dynamics 365に現物更新と財務更新済です。 現物トランザクションと財務トランザクションによっては、在庫数量を増加または減少させるものがあります。

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
数量を増加させるトランザクションは移動平均原価価格で転記されます。 Dynamics 365 for Operationsは、財務的に追跡されている在庫分析コードごとに、各このトランザクションの原価に基づく移動平均原価価格が計算されます。 移動平均原価価格については、[[移動平均原価価格](running-average-cost-price.md)] を参照ください。

## <a name="transactions-that-decrease-quantity"></a>数量を減少させるトランザクション
数量を減少させるトランザクションが転記されると、Dynamics 365 for Operationsは、在庫に関連付けられる在庫モデルに関係なく計算された移動平均原価価格が使用されます。 転記される前に、数量を減少させるトランザクションが別のトランザクションにすでにマークされていてはいけません。 現物手持在庫が負の場合、Dynamics 365 for Operationsは**品目**ページの品目に対して定義されている在庫原価を使用します。 **メモ:** マルチサイト機能が有効になっている場合、この原価は、[**既定の注文設定**] ページでサイトに対して定義されている在庫原価になります。

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


