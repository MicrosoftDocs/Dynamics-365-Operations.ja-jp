---
title: サービス期間
description: サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1027a6a1ddb1057ba039382d394522d6f9538a90
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432051"
---
# <a name="service-intervals"></a><span data-ttu-id="8f036-103">サービス期間</span><span class="sxs-lookup"><span data-stu-id="8f036-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f036-104">サービス合意間隔は、サービス注文を自動的に作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。</span><span class="sxs-lookup"><span data-stu-id="8f036-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="8f036-105">サービス注文を自動的に作成する場合、サービス注文明細行は、契約明細行の開始日を起点とし、サービス合意明細行に対して指定した間隔に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="8f036-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="8f036-106">**サービス契約** ページで **間隔** フィールドが空欄になっている場合、その行は 1 回限りのイベントであり、サービス注文を定期的に作成する際には使用されません。</span><span class="sxs-lookup"><span data-stu-id="8f036-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="8f036-107">例</span><span class="sxs-lookup"><span data-stu-id="8f036-107">Example</span></span>

<span data-ttu-id="8f036-108">この例では、サービス注文のサービス合意明細行とサービス注文明細行に、サービス期間が影響を与える仕組みを説明します。</span><span class="sxs-lookup"><span data-stu-id="8f036-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="8f036-109">サービス合意を作成します</span><span class="sxs-lookup"><span data-stu-id="8f036-109">Create a service agreement</span></span>

<span data-ttu-id="8f036-110">まず、サービス合意を作成し、**サービス注文の組み合わせ** オプションを **サービス契約別** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8f036-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="8f036-111">**サービス合意** をクリックします</span><span class="sxs-lookup"><span data-stu-id="8f036-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="8f036-112">**アクション ウィンドウ** の **サービス合意** タブの **新規** グループで、**サービス合意** をクリックして新しいサービス合意を作成します。</span><span class="sxs-lookup"><span data-stu-id="8f036-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="8f036-113">説明を入力し、**プロジェクト ID** フィールドでプロジェクトを選択して、**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="8f036-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="8f036-114">**サービス注文の組み合わせ** フィールドで、**サービス契約別** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f036-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="8f036-115">これで、次のサービス合意が作成されました。</span><span class="sxs-lookup"><span data-stu-id="8f036-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="8f036-116">Project</span><span class="sxs-lookup"><span data-stu-id="8f036-116">Project</span></span>      | <span data-ttu-id="8f036-117">開始日</span><span class="sxs-lookup"><span data-stu-id="8f036-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f036-118">選択したプロジェクト</span><span class="sxs-lookup"><span data-stu-id="8f036-118">Your project</span></span> | <span data-ttu-id="8f036-119">プロジェクトに指定した日付。</span><span class="sxs-lookup"><span data-stu-id="8f036-119">The date you specified for the project.</span></span> <span data-ttu-id="8f036-120">この例では、現在の日付を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f036-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="8f036-121">サービス合意項目の作成</span><span class="sxs-lookup"><span data-stu-id="8f036-121">Create a service agreement line</span></span>

<span data-ttu-id="8f036-122">次に、トランザクション タイプが **時間** のサービス合意明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="8f036-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="8f036-123">この例のこの部分を完了するには、**サービス期間** ページで 10 日間のサービス期間を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f036-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="8f036-124">作成したサービス合意を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f036-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="8f036-125">**明細行** クイック タブの **追加** ボタンをクリックし、 **サービス合意** ページの下部ウィンドウで新しい明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="8f036-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="8f036-126">**トランザクション タイプ** フィールドで **時間** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f036-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="8f036-127">**作業者** フィールドで、サービスを提供する作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f036-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="8f036-128">**サービス期間** フィールドで、間隔を 10 日として選択します。</span><span class="sxs-lookup"><span data-stu-id="8f036-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="8f036-129">これで、次の情報を含むサービス合意明細行が作成されました。</span><span class="sxs-lookup"><span data-stu-id="8f036-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="8f036-130">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="8f036-130">Transaction type</span></span> | <span data-ttu-id="8f036-131">入社日</span><span class="sxs-lookup"><span data-stu-id="8f036-131">Start date</span></span>                               | <span data-ttu-id="8f036-132">サービス期間</span><span class="sxs-lookup"><span data-stu-id="8f036-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="8f036-133">時</span><span class="sxs-lookup"><span data-stu-id="8f036-133">Hour</span></span>             | <span data-ttu-id="8f036-134">現在の日付。</span><span class="sxs-lookup"><span data-stu-id="8f036-134">The current date.</span></span>                        | <span data-ttu-id="8f036-135">10 日ごと</span><span class="sxs-lookup"><span data-stu-id="8f036-135">Every 10 days</span></span>    |
| <span data-ttu-id="8f036-136">ワーカー</span><span class="sxs-lookup"><span data-stu-id="8f036-136">Worker</span></span>           | <span data-ttu-id="8f036-137">サービスを実行する作業者。</span><span class="sxs-lookup"><span data-stu-id="8f036-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="8f036-138">この明細行に時間枠の設定はありません。</span><span class="sxs-lookup"><span data-stu-id="8f036-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="8f036-139">計画済みサービス注文の作成</span><span class="sxs-lookup"><span data-stu-id="8f036-139">Create planned service orders</span></span>

<span data-ttu-id="8f036-140">翌月の計画済みサービス注文とサービス注文明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="8f036-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="8f036-141">**サービス合意** ページの **アクション ウィンドウ** の **出荷** タブで、**計画されたサービス注文** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f036-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="8f036-142">**Create service orders** ページで **開始日** フィールドに現在の日付を、**終了日** フィールドに現在の日付から 1 か月後の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="8f036-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="8f036-143">**時間** スライダーを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8f036-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="8f036-144">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f036-144">Click **OK**.</span></span>

<span data-ttu-id="8f036-145">**サービス注文の組み合わせ** の **サービス契約別** オプションで定義したサービス注文にはグループ化が存在しないため、サービス注文ごとに 1 つのサービス注文明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="8f036-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="8f036-146">作成されたサービス注文</span><span class="sxs-lookup"><span data-stu-id="8f036-146">Service orders created</span></span>

<span data-ttu-id="8f036-147">**サービス注文の作成** ダイアログ ボックスで指定した時間枠内に、サービス注文明細行が 3 行作成されています。</span><span class="sxs-lookup"><span data-stu-id="8f036-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="8f036-148">サービス注文明細行は、**サービス合意** ページ (**アクション ウィンドウ** \> **出荷** タブ \>**表示** ボタン) に表示できます。</span><span class="sxs-lookup"><span data-stu-id="8f036-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f036-149">関連トピック</span><span class="sxs-lookup"><span data-stu-id="8f036-149">Related topics</span></span>

[<span data-ttu-id="8f036-150">サービス期間の設定</span><span class="sxs-lookup"><span data-stu-id="8f036-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

