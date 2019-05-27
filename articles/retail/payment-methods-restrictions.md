---
title: レシートのない返品の支払方法の制限
description: このトピックでは、返品がレシートなしで行われた場合に、特定の支払タイプがどのように返金を制限するかについて説明します。
author: rapraj
manager: AnnBe
ms.date: 013/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 6e2c32aae06ce7bbdde30809d7a197f43b856af1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564353"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="2e618-103">レシートのない返品の支払方法の制限</span><span class="sxs-lookup"><span data-stu-id="2e618-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2e618-104">小売業者が受け入れる各支払タイプは、システムの設定時にコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e618-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="2e618-105">このトピックでは、返品がレシートなしで行われた場合に、特定の支払タイプがどのように返金を制限するかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2e618-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="2e618-106">支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="2e618-106">Set up payment methods</span></span>

<span data-ttu-id="2e618-107">支払方法を設定するには、次の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e618-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="2e618-108">組織全体で受け入れる支払方法を作成します。</span><span class="sxs-lookup"><span data-stu-id="2e618-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="2e618-109">組織全体のカード タイプとカード番号の作成。</span><span class="sxs-lookup"><span data-stu-id="2e618-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="2e618-110">クレジット カードまたはデビット カードを受け入れる場合、カードの支払方法を 1 つ作成し、組織全体のカード タイプとカード番号を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e618-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="2e618-111">店舗の支払方法を設定します。</span><span class="sxs-lookup"><span data-stu-id="2e618-111">Set up store payment methods.</span></span> <span data-ttu-id="2e618-112">支払方法を各店舗に関連付けて、各支払方法の店舗固有の設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e618-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="2e618-113">店舗のカード支払方法の設定。</span><span class="sxs-lookup"><span data-stu-id="2e618-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="2e618-114">店舗で受け入れるカード支払方法について、カードの設定を行います。</span><span class="sxs-lookup"><span data-stu-id="2e618-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="2e618-115">![小売店舗の設定](media/NoReceiptReturns1.png "小売店舗の設定")</span><span class="sxs-lookup"><span data-stu-id="2e618-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="2e618-116">レシートのない返品の支払方法の制限</span><span class="sxs-lookup"><span data-stu-id="2e618-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="2e618-117">各店舗の支払方法について、**小売店舗の管理**ページの**レシートなしの返品**で、**レシートなしの払戻の制限**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="2e618-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="2e618-118">切替の既定値が**いいえ**である場合は、その支払方法は払戻が許可されていることを保証します。</span><span class="sxs-lookup"><span data-stu-id="2e618-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="2e618-119">**レシートなしの払戻の制限**が**はい**に設定されている場合、選択された支払方法は払戻に使用できません。</span><span class="sxs-lookup"><span data-stu-id="2e618-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="2e618-120">![小売店舗の支払方法](media/NoReceiptReturns3.png "小売店舗の支払方法")</span><span class="sxs-lookup"><span data-stu-id="2e618-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="2e618-121">レジ担当者が、レシートなしでの払戻が制限されている支払方法を選択すると、許容されている支払方法を確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e618-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="2e618-122">![許容可能な支払方法](media/NoReceiptReturns4.png "許容可能な支払方法")</span><span class="sxs-lookup"><span data-stu-id="2e618-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="2e618-123">トランザクションにレシートありの返品とレシートなしの返品の両方がある場合、トランザクションはレシートありの返品ワークフローになるため、制限条件は適用されません。</span><span class="sxs-lookup"><span data-stu-id="2e618-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

