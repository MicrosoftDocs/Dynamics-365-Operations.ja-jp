---
title: サービス管理の概要
description: サービス契約とサービスの定期売買を締結し、サービス注文および顧客の照会を処理し、顧客へのサービスの配送を管理および分析するには、サービス管理を使用します。
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70c0a6c82e0227319c4e95ad7b60a97c7b03401a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010500"
---
# <a name="service-management-overview"></a><span data-ttu-id="832b0-103">サービス管理の概要</span><span class="sxs-lookup"><span data-stu-id="832b0-103">Service management overview</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="832b0-104">サービス契約とサービスの定期売買を締結し、サービス注文および顧客の照会を処理し、顧客へのサービスの配送を管理および分析するには、**サービス管理** を使用します。</span><span class="sxs-lookup"><span data-stu-id="832b0-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="832b0-105">サービス契約を使用して、標準的なサービス訪問で使用されるリソースを定義できます。</span><span class="sxs-lookup"><span data-stu-id="832b0-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="832b0-106">また、サービス契約を使用して、それらのリソースに関する顧客への請求方法を表示できます。</span><span class="sxs-lookup"><span data-stu-id="832b0-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="832b0-107">サービス契約には、標準応答時間を指定し、実際の時間を記録するツールを提供する、サービス レベル契約も含まれています。</span><span class="sxs-lookup"><span data-stu-id="832b0-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="832b0-108">サービス注文を作成して、サービス技術者の顧客サイトへの予定された訪問および予定外の訪問に関する情報を管理できます。</span><span class="sxs-lookup"><span data-stu-id="832b0-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="832b0-109">サービス注文には次のような情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="832b0-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="832b0-110">サービス技術者が実行する作業時間</span><span class="sxs-lookup"><span data-stu-id="832b0-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="832b0-111">修復またはサービスのタイプ</span><span class="sxs-lookup"><span data-stu-id="832b0-111">The type of service or repair</span></span>

3.  <span data-ttu-id="832b0-112">修復する品目 (現象および診断に関する詳細を含む)</span><span class="sxs-lookup"><span data-stu-id="832b0-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="832b0-113">サービスまたは修復に関連する経費および手数料</span><span class="sxs-lookup"><span data-stu-id="832b0-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="832b0-114">サービス要求を受信し、処理し、発信できます。</span><span class="sxs-lookup"><span data-stu-id="832b0-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="832b0-115">サービス注文を作成した後、サービス ステージを使用して進捗を監視し、各ステージで有効になるアクションを制御するルールを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="832b0-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="832b0-116">サービス注文が完了すると、注文でサインオフして完了したことを確認してから、注文を転記して請求書プロセスを開始できます。</span><span class="sxs-lookup"><span data-stu-id="832b0-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="832b0-117">サービス注文利益幅および定期売買トランザクションを監視したり、作業の説明および作業受入を印刷したりするには、レポート ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="832b0-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="832b0-118">業務プロセス</span><span class="sxs-lookup"><span data-stu-id="832b0-118">Business processes</span></span>

<span data-ttu-id="832b0-119">次の図は、**サービス管理** の上位レベルの業務プロセスを示し、サービス プロセスが他のモジュールと統合する場所を示します。</span><span class="sxs-lookup"><span data-stu-id="832b0-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules.</span></span>

<span data-ttu-id="832b0-120">[![サービス管理の業務プロセス図](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="832b0-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="832b0-121">サービス管理の図</span><span class="sxs-lookup"><span data-stu-id="832b0-121">Service management at a glance</span></span>

|<span data-ttu-id="832b0-122">重要なタスク</span><span class="sxs-lookup"><span data-stu-id="832b0-122">Important tasks</span></span>           | <span data-ttu-id="832b0-123">基本ページ</span><span class="sxs-lookup"><span data-stu-id="832b0-123">Primary pages</span></span>                         |<span data-ttu-id="832b0-124">一般的なレポート</span><span class="sxs-lookup"><span data-stu-id="832b0-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="832b0-125">サービス契約の履行</span><span class="sxs-lookup"><span data-stu-id="832b0-125">Fulfill service agreements</span></span>|<span data-ttu-id="832b0-126">サービス契約</span><span class="sxs-lookup"><span data-stu-id="832b0-126">Service agreements</span></span>                     |<span data-ttu-id="832b0-127">サービス注文利益幅</span><span class="sxs-lookup"><span data-stu-id="832b0-127">Service order margin</span></span>         |
|<span data-ttu-id="832b0-128">顧客の照会の処理</span><span class="sxs-lookup"><span data-stu-id="832b0-128">Handle customer inquiries</span></span> |<span data-ttu-id="832b0-129">サービス注文</span><span class="sxs-lookup"><span data-stu-id="832b0-129">Service orders</span></span>                         |<span data-ttu-id="832b0-130">作業の説明</span><span class="sxs-lookup"><span data-stu-id="832b0-130">Work description</span></span>             |
|                          |<span data-ttu-id="832b0-131">派遣表</span><span class="sxs-lookup"><span data-stu-id="832b0-131">Dispatch board</span></span>                         |<span data-ttu-id="832b0-132">トランザクション - 定期売買</span><span class="sxs-lookup"><span data-stu-id="832b0-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="832b0-133">定期売買手数料トランザクション</span><span class="sxs-lookup"><span data-stu-id="832b0-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="832b0-134">サービス管理の統合</span><span class="sxs-lookup"><span data-stu-id="832b0-134">Integration of Service management</span></span>

<span data-ttu-id="832b0-135">サービス管理は次のモジュールと統合できます。</span><span class="sxs-lookup"><span data-stu-id="832b0-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="832b0-136">販売とマーケティングの概要</span><span class="sxs-lookup"><span data-stu-id="832b0-136">Sales and marketing overview</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="832b0-137">人事管理</span><span class="sxs-lookup"><span data-stu-id="832b0-137">Human resources</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/index)

  

