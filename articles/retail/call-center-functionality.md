---
title: "コール センター機能"
description: "この記事は、Microsoft Dynamics 365 for Retail でのコール センターの販売機能の概要を示します。"
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
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 00d24e9933d087f150ec5270da94ad911423824d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="call-center-functionality"></a><span data-ttu-id="c1c2f-103">コール センターの機能</span><span class="sxs-lookup"><span data-stu-id="c1c2f-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="c1c2f-104">この記事は、Microsoft Dynamics 365 for Retail でのコール センターの販売機能の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="c1c2f-105">Dynamics 365 for Retail は、小売チャンネルのタイプとしてコール センターもサポートします。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="c1c2f-106">コール センターでは、作業者が電話で顧客の注文をとり、販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="c1c2f-107">コール センター機能には、電話で注文を受け付けて、注文処理プロセス全体の顧客サービスの処理を容易にするための機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="c1c2f-108">たとえば、コール センターの作業者は、販売注文に支払い情報を直接入力でき、注文を送信する前に請求金額と支払の詳細な集計を表示できます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="c1c2f-109">作業者は価格決定を制御するための選択肢を持っており、[**販売注文**] ページの顧客、製品、および価格に関するさまざまなデータにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="c1c2f-110">また、コール センターには、顧客履歴と注文の状態を追跡するために強化された機能もあります。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="c1c2f-111">各コール センターは、独自のユーザー、支払方法、価格グループ、財務分析コード、配達のモードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="c1c2f-112">コール センターを作成するとき、これらのオプションをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="c1c2f-113">また、[**コール センター**] ページを使用して、コール センター固有の次の機能グループを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="c1c2f-114">[**注文完了**] – このグループには [**販売注文**] ページの支払いおよび注文完了に関連する機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="c1c2f-115">[**主導販売**] – このグループにはソース コード、スクリプト、カタログ要求に関連する機能が含まれます。 </span><span class="sxs-lookup"><span data-stu-id="c1c2f-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="c1c2f-116">コール センターの設定でこれらの機能を有効にすると、コール センターに関連付けられたユーザーは [**販売注文**] ページを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="c1c2f-117">これらの機能の多くは、使用する前に追加の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="c1c2f-118">ユーザーがコール センターの注文を作成する前に、コール センターのユーザーとしてそのユーザーをコール センターに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="c1c2f-119">この手順は、コール センターのチャンネル固有のコンフィギュレーションと機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="c1c2f-120">次に使用できる機能の例を示します :</span><span class="sxs-lookup"><span data-stu-id="c1c2f-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="c1c2f-121">ガイド販売は、販売員が注文を取る時に手助けになるテレセールスのスクリプトおよび製品画像のコンフィギュレーション オプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-121">Guided selling provides configuration options for telesales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="c1c2f-122">販売員が少なくとも 1 つの支払方法をキャプチャするまで注文は完了されません。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="c1c2f-123">アップセルおよびクロスセル ルールは、顧客に特定の製品を販売促進するよう販売員を促すようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="c1c2f-124">販売員は顧客が注文するカタログのソース コードを取得できます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="c1c2f-125">販売員は、注文に小売業者がクーポンを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="c1c2f-126">販売員は連続プログラムを販売できます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="c1c2f-127">注文が処理される前に追加調査が必要であることを示す場合は、手動または自動で注文を保留にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c1c2f-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





