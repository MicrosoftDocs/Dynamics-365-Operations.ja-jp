---
title: 販売注文ページで支払タイプが、クレジット カード エラーである必要があります
description: このトピックでは、注文の同期後に販売注文ページにエラー メッセージが表示される場合に役立つトラブルシューティングガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018413"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="3af0b-103">販売注文ページで、"支払タイプが、クレジット カード" エラーである必要があります</span><span class="sxs-lookup"><span data-stu-id="3af0b-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3af0b-104">このトピックでは、注文の同期後に販売注文ページにエラー メッセージが表示される場合に役立つトラブルシューティングガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="3af0b-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="3af0b-105">説明</span><span class="sxs-lookup"><span data-stu-id="3af0b-105">Description</span></span>

<span data-ttu-id="3af0b-106">注文を同期した後に販売注文ページを開くと、"クレジット カード番号が指定されているので、支払タイプはクレジット カードである必要があります。" というエラー メッセージが表示されます</span><span class="sxs-lookup"><span data-stu-id="3af0b-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![支払タイプはクレジット カード エラーである必要があります](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="3af0b-108">解像度</span><span class="sxs-lookup"><span data-stu-id="3af0b-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="3af0b-109">Commerce 本社での支払タイプの設定</span><span class="sxs-lookup"><span data-stu-id="3af0b-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="3af0b-110">**売掛金勘定 \> 支払設定 \> 支払条件** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3af0b-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="3af0b-111">左ナビゲーションで、支払条件を選択します。</span><span class="sxs-lookup"><span data-stu-id="3af0b-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="3af0b-112">**支払タイプ** フィールドで、**クレジット カード** が選択されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3af0b-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3af0b-113">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3af0b-113">Additional resources</span></span>

[<span data-ttu-id="3af0b-114">オンラインの販売と支払の転記</span><span class="sxs-lookup"><span data-stu-id="3af0b-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
