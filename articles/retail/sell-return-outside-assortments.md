---
title: "店舗の品揃えに含まれない製品の販売および返品"
description: "Dynamics 365 for Retail で、品揃えの範囲外の製品を販売および返品ができます。"
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 17981cef401085ad3af784950fff6260c2c6d9ee
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>店舗の品揃えに含まれない製品の販売および返品

[!include [banner](includes/banner.md)]

小売業者の一般的なシナリオでは、店舗で特定の製品を抱えていない場合 (つまり、製品が店舗の品揃えにない場合) でも、製品を顧客に販売したり、顧客からの返品を受け入れたりします。
以下に一般的なシナリオを挙げます。

+ 小売業者は、特定の店舗ですべての製品を抱えているわけではありません。 残りの製品は、倉庫に格納されます。 店舗スタッフは、倉庫の製品を検索または表示することで顧客を支援し、カートに追加して、倉庫から住所へ出荷したり、現在の店舗または別の店舗から製品を顧客にピッキングしてもらったりなどの配送方法を選択することにより、チェックアウトを完了できます。
+ 小売業者は、店舗内に特定の製品を抱えたり、顧客が訪れた店舗に在庫を持ったりしませんが、製品を他の店舗で使用できます。 店舗スタッフは、その他の店舗の製品を検索または表示することで顧客を支援し、カートに追加して、配送方法を選択することにより、チェック アウトを完了できます。
+ 小売業者が特定の市町村または郵便番号コードで多数の店舗を所有していれば、購入した同じ店舗への製品の返品を顧客に強制したくはありません。 代わりに、顧客は、どの店舗にも製品を返品することができます。


これらの一般的なシナリオは、Dynamics 365 for Retail を使用している小売業者が使用できます。 Retail では次のことができます。
+ 他の店舗で製品を検索や表示します。
+ すべてリリースされた製品を検索や表示します。
+ 現金店頭払いのトランザクションまたは顧客注文を作成します。
+ 顧客注文の配送オプションを選択します。
+ 現在の店舗または別の店舗で製品をピッキングします。
+ 現在の店舗または別の店舗で注文をキャンセルします。
+ 現在の店舗または別の店舗に領収書の有無にかかわらず注文を返品します。

