---
title: "サービス管理"
description: "サービス契約とサービスの定期売買を締結し、サービス注文および顧客の照会を処理し、顧客へのサービスの配送を管理および分析するには、サービス管理を使用します。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="342a6-103">サービス管理</span><span class="sxs-lookup"><span data-stu-id="342a6-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="342a6-104">サービス契約とサービスの定期売買を締結し、サービス注文および顧客の照会を処理し、顧客へのサービスの配送を管理および分析するには、**サービス管理**を使用します。</span><span class="sxs-lookup"><span data-stu-id="342a6-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="342a6-105">サービス契約を使用して、標準的なサービス訪問で使用されるリソースを定義できます。</span><span class="sxs-lookup"><span data-stu-id="342a6-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="342a6-106">また、サービス契約を使用して、それらのリソースに関する顧客への請求方法を表示できます。</span><span class="sxs-lookup"><span data-stu-id="342a6-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="342a6-107">サービス契約には、標準応答時間を指定し、実際の時間を記録するツールを提供する、サービス レベル契約も含まれています。</span><span class="sxs-lookup"><span data-stu-id="342a6-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="342a6-108">サービス注文を作成して、サービス技術者の顧客サイトへの予定された訪問および予定外の訪問に関する情報を管理できます。</span><span class="sxs-lookup"><span data-stu-id="342a6-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="342a6-109">サービス注文には次のような情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="342a6-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="342a6-110">サービス技術者が実行する作業時間</span><span class="sxs-lookup"><span data-stu-id="342a6-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="342a6-111">修復またはサービスのタイプ</span><span class="sxs-lookup"><span data-stu-id="342a6-111">The type of service or repair</span></span>

3.  <span data-ttu-id="342a6-112">修復する品目 (現象および診断に関する詳細を含む)</span><span class="sxs-lookup"><span data-stu-id="342a6-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="342a6-113">サービスまたは修復に関連する経費および手数料</span><span class="sxs-lookup"><span data-stu-id="342a6-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="342a6-114">顧客は、エンタープライズ ポータルを使用してインターネット経由でサービス要求を送信できます。</span><span class="sxs-lookup"><span data-stu-id="342a6-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="342a6-115">これらの要求を受信し、処理し、発信できます。</span><span class="sxs-lookup"><span data-stu-id="342a6-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="342a6-116">サービス注文を作成した後、サービス ステージを使用して進捗を監視し、各ステージで有効になるアクションを制御するルールを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="342a6-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="342a6-117">サービス注文が完了すると、注文でサインオフして完了したことを確認してから、注文を転記して請求書プロセスを開始できます。</span><span class="sxs-lookup"><span data-stu-id="342a6-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="342a6-118">サービス注文利益幅および定期売買トランザクションを監視したり、作業の説明および作業受入を印刷したりするには、レポート ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="342a6-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="342a6-119">業務プロセス</span><span class="sxs-lookup"><span data-stu-id="342a6-119">Business processes</span></span>

<span data-ttu-id="342a6-120">次の図は、**サービス管理**の高レベルの業務プロセスを示し、Microsoft Dynamics 365 for Finance and Operations 内の他のモジュールとサービス プロセス統合場所を表示します。</span><span class="sxs-lookup"><span data-stu-id="342a6-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="342a6-121">[![サービス管理の業務プロセス図](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="342a6-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="342a6-122">サービス管理の図</span><span class="sxs-lookup"><span data-stu-id="342a6-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="342a6-123">重要なタスク</span><span class="sxs-lookup"><span data-stu-id="342a6-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="342a6-124">基本フォーム</span><span class="sxs-lookup"><span data-stu-id="342a6-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="342a6-125">一般的なレポート</span><span class="sxs-lookup"><span data-stu-id="342a6-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="342a6-126">サービス契約の履行</span><span class="sxs-lookup"><span data-stu-id="342a6-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="342a6-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">サービス契約 (フォーム)</a></span><span class="sxs-lookup"><span data-stu-id="342a6-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="342a6-128"><strong>サービス注文利益幅</strong></span><span class="sxs-lookup"><span data-stu-id="342a6-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="342a6-129">顧客の照会の処理</span><span class="sxs-lookup"><span data-stu-id="342a6-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="342a6-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">サービス注文 (フォーム)</a></span><span class="sxs-lookup"><span data-stu-id="342a6-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="342a6-131"><strong>作業の説明</strong></span><span class="sxs-lookup"><span data-stu-id="342a6-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="342a6-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">派遣表 (フォーム)</a></span><span class="sxs-lookup"><span data-stu-id="342a6-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="342a6-133"><strong>トランザクション - 定期売買</strong></span><span class="sxs-lookup"><span data-stu-id="342a6-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="342a6-134"><strong>定期売買手数料トランザクション</strong></span><span class="sxs-lookup"><span data-stu-id="342a6-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="342a6-135">サービス管理の統合</span><span class="sxs-lookup"><span data-stu-id="342a6-135">Integration of Service management</span></span>

<span data-ttu-id="342a6-136">サービス管理は、Microsoft Dynamics 365 for Finance and Operations 内で以下のモジュールと統合されます。</span><span class="sxs-lookup"><span data-stu-id="342a6-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="342a6-137">販売とマーケティング</span><span class="sxs-lookup"><span data-stu-id="342a6-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="342a6-138">人事管理</span><span class="sxs-lookup"><span data-stu-id="342a6-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


