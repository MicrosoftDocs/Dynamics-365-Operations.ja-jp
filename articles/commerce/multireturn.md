---
title: 複数の顧客注文および請求書間での品目の返品
description: このトピックでは、複数の顧客注文および請求書をまたいだ返品を有効にする Dynamics 365 Commerce の機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: ee4c863e617b9351e55e1fc652ea8905f17c8346
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976666"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>複数の顧客注文および請求書間での品目の返品

[!include [banner](includes/banner.md)]


この記事では、複数の請求書に対して顧客の注文返品を最適化する 2 つの機能について説明します。 

## <a name="enable-refunds-over-multiple-captures"></a>複数のキャプチャの払戻を有効にする

この機能は、同じ顧客注文に対してリンクされた複数の払戻を有効にします。 

1. **機能管理** ワークスペースに移動して、**複数のキャプチャの払戻を有効にする** を検索します。
2. **複数の注文の払戻を有効にする** を選択して、**有効にする** をクリックします。 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>一部の数量を使用して、返品の適切な税計算を有効にします

この機能により、複数の請求書を使用して注文が返品された場合、最終的に税金は最初に請求された税額と等しくなります。 

1. **機能管理** ワークスペースに移動して、**Enable proper tax calculation for returns with partial quantity (一部の数量を使用して、返品の適切な税計算を有効にする)** を検索します。
2. **Enable proper tax calculation for returns with partial quantity (一部の数量を使用して、返品の適切な税計算を有効にする)**、**有効にする** をクリックします。 


## <a name="process-returns"></a>返品の処理

これらの機能をオンにし、変更を店舗に同期させると、店舗のレジ担当者は、顧客の返品に対して複数の販売注文を選択できるようになります。

注文を選択すると、その注文のすべての請求書で返品可能なすべての製品の一覧が表示されます。 レジ担当者は、その一覧から返品する商品を選択できます。 選択したすべての製品に対して 1 つの返品注文が作成されます。

注文が完全に返品された場合、顧客に返金される税額は、最初に請求された税額と等しくなります。



[!INCLUDE[footer-include](../includes/footer-banner.md)]