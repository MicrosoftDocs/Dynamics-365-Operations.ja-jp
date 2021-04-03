---
title: サービス契約の作成および締結の概要
description: サービス契約では、標準的なサービス訪問で使用されるリソース、およびそれらのリソースに関する顧客への請求方法を定義できます。
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86855e8893cdf5d6e53cb34465480ade06a6da95
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258497"
---
# <a name="develop-and-establish-service-agreements-overview"></a><span data-ttu-id="537bc-103">サービス契約の作成および締結の概要</span><span class="sxs-lookup"><span data-stu-id="537bc-103">Develop and establish service agreements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="537bc-104">サービス契約では、標準的なサービス訪問で使用されるリソース、およびそれらのリソースに関する顧客への請求方法を定義できます。</span><span class="sxs-lookup"><span data-stu-id="537bc-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="537bc-105">サービス契約はすべてプロジェクトに関連付けられ、そのプロジェクトを通じてトランザクションの転記と請求が行われます。</span><span class="sxs-lookup"><span data-stu-id="537bc-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="537bc-106">ただし、最初にサービス注文をサービス契約と関連付けずに、サービス注文トランザクションをプロジェクトを通して直接請求できます。</span><span class="sxs-lookup"><span data-stu-id="537bc-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="537bc-107">サービス注文が 1 回のみのサービス訪問であり、サービス トランザクションをすぐに処理する必要性が、顧客に関する詳細なサービス契約情報を一定期間にわたって管理する必要性を上回る場合、これを行う場合があります。</span><span class="sxs-lookup"><span data-stu-id="537bc-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="537bc-108">サービス合意</span><span class="sxs-lookup"><span data-stu-id="537bc-108">Service agreement</span></span>

<span data-ttu-id="537bc-109">各サービス合意で、プロジェクト、サービス合意 ID、およびサービス合意グループを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="537bc-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="537bc-110">サービス契約グループを使用して、サービス契約を並べ替えたり、組織したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="537bc-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="537bc-111">サービス契約のヘッダーには、関連付けられるすべての契約項目に適用される設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="537bc-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="537bc-112">サービス合意を中断するかどうか。</span><span class="sxs-lookup"><span data-stu-id="537bc-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="537bc-113">サービス合意が中断されている場合は、サービス合意からサービス注文を生成することができません。</span><span class="sxs-lookup"><span data-stu-id="537bc-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="537bc-114">サービス合意の期間。</span><span class="sxs-lookup"><span data-stu-id="537bc-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="537bc-115">サービス注文明細行をサービス注文に連結する方法。</span><span class="sxs-lookup"><span data-stu-id="537bc-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="537bc-116">サービス合意がテンプレートかどうか。</span><span class="sxs-lookup"><span data-stu-id="537bc-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="537bc-117">サービス契約ヘッダーでは、契約のさまざまな行に関連付けられているサービス タスクまたはサービス対象を入力することにより、サービス契約で使用できるサービス対象およびサービス タスクすべてを設定できます。</span><span class="sxs-lookup"><span data-stu-id="537bc-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="537bc-118">また、サービス契約ヘッダーから、サービス契約項目またはサービス テンプレート行を現在のサービス契約にコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="537bc-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="537bc-119">サービス合意を中断し、個々のサービス合意項目を停止できます。</span><span class="sxs-lookup"><span data-stu-id="537bc-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="537bc-120">サービス合意で **中断** チェック ボックスをオンにすると、次の操作は実行できません。</span><span class="sxs-lookup"><span data-stu-id="537bc-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="537bc-121">サービス合意から自動または手動でサービス注文を作成する。</span><span class="sxs-lookup"><span data-stu-id="537bc-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="537bc-122">サービス合意で **停止済** チェック ボックスをオンにすると、次の操作は実行できません。</span><span class="sxs-lookup"><span data-stu-id="537bc-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="537bc-123">サービス合意項目から自動または手動でサービス注文を作成する。</span><span class="sxs-lookup"><span data-stu-id="537bc-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="537bc-124">サービス合意項目を別のサービス合意またはサービス注文にコピーする。</span><span class="sxs-lookup"><span data-stu-id="537bc-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="537bc-125">サービス契約を中断すると、関連付けられているすべての項目が、それぞれの状態に関係なく停止します。</span><span class="sxs-lookup"><span data-stu-id="537bc-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="537bc-126">サービス合意項目</span><span class="sxs-lookup"><span data-stu-id="537bc-126">Service-agreement lines</span></span>

<span data-ttu-id="537bc-127">各サービス契約項目は、提出されるサービス作業の内容を詳細に説明したものです。</span><span class="sxs-lookup"><span data-stu-id="537bc-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="537bc-128">項目には、以下の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="537bc-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="537bc-129">トランザクション タイプ、およびトランザクション タイプの説明。</span><span class="sxs-lookup"><span data-stu-id="537bc-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="537bc-130">サービス作業を実行する従業員。</span><span class="sxs-lookup"><span data-stu-id="537bc-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="537bc-131">サービス合意のサービスを実行する必要がある対象。</span><span class="sxs-lookup"><span data-stu-id="537bc-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="537bc-132">サービス作業が実行されて関連付けられた品目、経費、および手数料の各トランザクションが登録される頻度。</span><span class="sxs-lookup"><span data-stu-id="537bc-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="537bc-133">サービス注文明細行をサービス注文にグループ化できる時間枠。</span><span class="sxs-lookup"><span data-stu-id="537bc-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="537bc-134">契約項目のセットをまとめて作業タスクにグループ化するために使用されるサービス タスク。サービス タスクは、サービス技術者や顧客に対する、提供されるサービス タスクの全体的な説明としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="537bc-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="537bc-135">明細行が停止されるかどうか。</span><span class="sxs-lookup"><span data-stu-id="537bc-135">Whether a line is stopped.</span></span> <span data-ttu-id="537bc-136">明細行が停止されている場合は、その明細行についてのサービス注文を作成できません。</span><span class="sxs-lookup"><span data-stu-id="537bc-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="537bc-137">カテゴリや明細行プロパティなどの、プロジェクト設定。</span><span class="sxs-lookup"><span data-stu-id="537bc-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="537bc-138">関連トピック</span><span class="sxs-lookup"><span data-stu-id="537bc-138">Related topics</span></span>

[<span data-ttu-id="537bc-139">サービス契約の作成</span><span class="sxs-lookup"><span data-stu-id="537bc-139">Create service agreements</span></span>](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]