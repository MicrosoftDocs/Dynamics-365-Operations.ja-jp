---
title: "注文保留"
description: "このトピックでは、Dynamics 365 for Retail を使用して、注文の保留について説明します。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14dab07075a3f042e0095b912e51768ccb086f0e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="order-holds"></a><span data-ttu-id="1cf14-103">注文保留</span><span class="sxs-lookup"><span data-stu-id="1cf14-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="1cf14-104">このトピックでは、Dynamics 365 for Retail を使用して、注文の保留について説明します。</span><span class="sxs-lookup"><span data-stu-id="1cf14-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="1cf14-105">注文はさまざまな理由で保留にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1cf14-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="1cf14-106">たとえば、顧客の住所や支払方法が確認できるまで、またはマネージャーが顧客の与信限度額を確認できるまで、注文を保留にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="1cf14-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="1cf14-107">販売プロセスの間は、販売注文は保留中にすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="1cf14-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="1cf14-108">たとえば、顧客の支払いに関する問題のために、または管理者の確認が必要なために、販売注文を保留中にすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="1cf14-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="1cf14-109">販売注文を保留中にすると、保留の理由を示す注文保留コードが販売注文に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1cf14-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="1cf14-110">**販売とマーケティング** &gt; **設定** &gt; **販売注文** &gt; **注文保留コード** で販売注文保留コードがコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="1cf14-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="1cf14-111">販売注文は注文の作成時に、または後で手動で保留にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1cf14-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="1cf14-112">また、注文を不正ルールに基づいて、自動的に保留にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1cf14-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="1cf14-113">販売注文が保留中の間、詳細情報に基いてそれを更新する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="1cf14-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="1cf14-114">または、販売注文をチェック アウトして作業を続行することもできます。</span><span class="sxs-lookup"><span data-stu-id="1cf14-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="1cf14-115">販売注文をチェックアウト、もう一度確認、および注文保留ワークベンチを使用して、別のユーザーのチェックアウトを上書きすることができます (**小売** &gt; **顧客** &gt; **注文保留**)。</span><span class="sxs-lookup"><span data-stu-id="1cf14-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="1cf14-116">注文を完了する準備が整ったら、注文プロセスを完了する前に、保留を解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cf14-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




