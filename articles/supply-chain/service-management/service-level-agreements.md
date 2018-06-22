---
title: "サービス レベル アグリーメント"
description: "サービス レベル アグリーメントにおいて、顧客はサービス会社が案件を記録し、案件が解決される時に基づく最低限の応答時間に合意します。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a><span data-ttu-id="3fbf6-103">サービス レベル アグリーメント</span><span class="sxs-lookup"><span data-stu-id="3fbf6-103">Service level agreements</span></span>        

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3fbf6-104">サービス レベル契約 (SLA) はサービス会社とサービス顧客の間の契約です。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="3fbf6-105">SLA において、顧客はサービス会社が案件を記録し、案件が解決される時に基づく最低限の応答時間に合意します。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="3fbf6-106">SLA により、顧客に提供されるサービスの水準が決定されます。また、いつサービス ジョブを実行する必要があるかがサービス会社に示されます。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="3fbf6-107">任意の数の SLA を作成して、さまざまなレベルのサービスをサービス顧客に提供できます。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="3fbf6-108">サービス レベル契約の作成</span><span class="sxs-lookup"><span data-stu-id="3fbf6-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="3fbf6-109">**サービス管理** \> **設定** \> **サービス契約** \> **サービス レベル契約**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="3fbf6-110">**サービス レベル契約**フィールドで、サービス レベル契約の名前をタイプします。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="3fbf6-111">サービス レベル契約に関連付けられているサービス コールの完了に許容する時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="3fbf6-112">それから、サービス レベル契約を特定のカレンダーに基づかせる場合には、カレンダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="3fbf6-113">サービス レベル契約の適用</span><span class="sxs-lookup"><span data-stu-id="3fbf6-113">Apply a service level agreement</span></span>

<span data-ttu-id="3fbf6-114">SLA はサービス合意に直接適用されます。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="3fbf6-115">手動で作成して SLA 付きのサービス合意に関連付けたサービス注文は、その SLA を基準で測定されます。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="3fbf6-116">自動的に作成したサービス注文は SLA に関連付けられません。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="3fbf6-117">サービス合意へのサービス レベル契約の適用</span><span class="sxs-lookup"><span data-stu-id="3fbf6-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="3fbf6-118">**サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="3fbf6-119">SLA を適用するサービス契約を選択してから、**アクション ウィンドウ**で**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="3fbf6-120">**サービス レベル契約**フィールドで、割り当てる SLA を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="3fbf6-121">サービス合意グループへのサービス レベル契約の適用</span><span class="sxs-lookup"><span data-stu-id="3fbf6-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="3fbf6-122">**サービス管理** \> **設定** \> **サービス契約** \> **サービス契約グループ**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="3fbf6-123">**サービス レベル契約**フィールドで、割り当てる SLA を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="3fbf6-124">サービス注文での SLA に対する時間の追跡</span><span class="sxs-lookup"><span data-stu-id="3fbf6-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="3fbf6-125">SLA が割り当てられているサービス契約に新しいサービス注文を作成すると、サービスの提供の時間期間が開始され、システムでは提供時間の追跡を開始します。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="3fbf6-126">さらに次のオプションを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="3fbf6-127">サービス注文で、サービス注文に対して使われた合計時間を登録するための時刻記録を開始および停止できます。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="3fbf6-128">サービス レベル契約で設定された時間期間への準拠を監視できます。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="3fbf6-129">サービス レベル契約の時間期間を超過した場合に設定する必要がある理由コードを定義できます。</span><span class="sxs-lookup"><span data-stu-id="3fbf6-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fbf6-130">参照</span><span class="sxs-lookup"><span data-stu-id="3fbf6-130">See also</span></span>

[<span data-ttu-id="3fbf6-131">サービス レベル契約に準拠しているかどうかの表示</span><span class="sxs-lookup"><span data-stu-id="3fbf6-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


