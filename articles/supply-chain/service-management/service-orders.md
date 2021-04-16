---
title: サービス注文
description: サービス注文とは、サービス技術者が特定の日に顧客サイトを訪問することです。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e47c3f998b563c775da77c48edcb7b8abcba4a04
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824489"
---
# <a name="service-orders"></a><span data-ttu-id="7cd85-103">サービス注文</span><span class="sxs-lookup"><span data-stu-id="7cd85-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7cd85-104">サービス注文とは、サービス技術者が特定の日に顧客サイトを訪問することです。</span><span class="sxs-lookup"><span data-stu-id="7cd85-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="7cd85-105">各サービス注文は、1 行以上のサービス注文明細行で構成されます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="7cd85-106">サービス注文明細行は、サービス技術者が実行する作業の所用時間、関連する品目、経費、および手数料を表します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="7cd85-107">サービス注文明細行には、仕事と目的を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="7cd85-108">仕事や目標別にサービス注文明細行はグループ分けできます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="7cd85-109">また、在庫に記載されている品目をサービス注文明細行に関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="7cd85-110">サービス注文の作成</span><span class="sxs-lookup"><span data-stu-id="7cd85-110">Create service orders</span></span>

<span data-ttu-id="7cd85-111">サービス注文はサービス契約とその契約に盛り込まれた明細行に従って作成できます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="7cd85-112">ただし、サービス合意に関連付けられたサービス注文を作成できるのは、契約に指定された期間中のみです。</span><span class="sxs-lookup"><span data-stu-id="7cd85-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="7cd85-113">たとえば、サービス契約の有効期間が 2011 年の暦年の場合、2011 年 1 月 1 日から 2011 年 12 月 31 日までの契約のサービス注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="7cd85-114">または契約とは関連付けずに個別にサービス注文を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="7cd85-115">このようなサービス注文では、不定期のサービス訪問や一回限りのサービス訪問を処理できます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="7cd85-116">たとえば、3 月に、ある顧客がサービス契約に指定されているマシンに加え、さらに 2 台のマシンのサービスを希望しているとします。</span><span class="sxs-lookup"><span data-stu-id="7cd85-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="7cd85-117">この仕事については、サービス注文を作成しますが、契約とは関連付けません。</span><span class="sxs-lookup"><span data-stu-id="7cd85-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7cd85-118">サービス契約に関連付けられていないサービス注文を作成するには、<STRONG>サービス管理パラメーター</STRONG>フォームの<STRONG>サービス契約無し注文の許可</STRONG>チェック ボックスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd85-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="7cd85-119">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="7cd85-119">**Scenario**</span></span>

<span data-ttu-id="7cd85-120">次のシナリオでは、サービス契約に関連付けられていないサービス注文を作成しておくと便利なもう一つの状況を説明します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="7cd85-121">法人の出荷係がエレベーターの緊急サービスを要求する電話を受け付けました。</span><span class="sxs-lookup"><span data-stu-id="7cd85-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="7cd85-122">サービス契約とサービスのプロジェクトを設定する時間はありません。</span><span class="sxs-lookup"><span data-stu-id="7cd85-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="7cd85-123">そこで、出荷係は **サービス注文** フォームでサービス注文を直接作成し、そのサービス注文を既存のプロジェクトに関連付け、サービス注文明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="7cd85-124">出荷係は、既存のサービス注文に関連した仕事や目的を作成して、サービス契約に関連付けられていない作業を記録します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="7cd85-125">詳細については、[サービス注文の手動作成](create-service-orders-manually.md) および [サービス作業関係の作成](create-service-task-relations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd85-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="7cd85-126">サービス注文の進捗状況の監視</span><span class="sxs-lookup"><span data-stu-id="7cd85-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="7cd85-127">さまざまなチームや作業プロセスで行われる販売注文の進捗状況を監視するため、サービス注文のステージと理由コードのシステムを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="7cd85-128">各ステージには、そこで可能なアクションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="7cd85-129">詳細については、[理由コードの作成](create-reason-codes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd85-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="7cd85-130">**例**</span><span class="sxs-lookup"><span data-stu-id="7cd85-130">**Example**</span></span>

<span data-ttu-id="7cd85-131">サービス注文は出荷係が承認します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="7cd85-132">出荷係はサービス注文のステージを更新して、そのサービス注文がサービス技術者にゆだねられたことを示す理由コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="7cd85-133">サービス技術者は顧客サイトを訪問し、サービスを遂行します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="7cd85-134">サービス注文の在庫品目要求の指定</span><span class="sxs-lookup"><span data-stu-id="7cd85-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="7cd85-135">サービス注文に必要な在庫品目を指定できます。</span><span class="sxs-lookup"><span data-stu-id="7cd85-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="7cd85-136">ただし、サービス注文はプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd85-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="7cd85-137">サービス注文に関する要求はプロジェクトを通じて処理します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="7cd85-138">**例**</span><span class="sxs-lookup"><span data-stu-id="7cd85-138">**Example**</span></span>

<span data-ttu-id="7cd85-139">サービス契約で作成したサービス注文は出荷係が処理します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="7cd85-140">最初のサービス注文で、出荷係は、手持ち在庫にない重要な予備部品がサービス技術者に必要なことに気が付きました。</span><span class="sxs-lookup"><span data-stu-id="7cd85-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="7cd85-141">この場合、出荷係は、予備部品の品目要求をサービス注文から直接作成します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="7cd85-142">明細行の移動と転記</span><span class="sxs-lookup"><span data-stu-id="7cd85-142">Move and post lines</span></span>

<span data-ttu-id="7cd85-143">サービス訪問から戻ったサービス技術者は、サービス注文明細行を変更して更新します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="7cd85-144">今回のサービス訪問で、技術者は、次のサービス訪問に予定されていたサービスを実行しました。</span><span class="sxs-lookup"><span data-stu-id="7cd85-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="7cd85-145">そこで、技術者は、次回のサービス訪問から現在のサービス訪問に明細行を移します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="7cd85-146">そして技術者はサービス注文を転記します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-146">The technician then posts the service order.</span></span> <span data-ttu-id="7cd85-147">詳細については、[サービス注文明細行の移動](move-service-order-lines.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd85-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="7cd85-148">サービス注文のキャンセル</span><span class="sxs-lookup"><span data-stu-id="7cd85-148">Cancel service orders</span></span>

<span data-ttu-id="7cd85-149">1 月に予定して生成されていたその他のサービス注文の一つが、ジョブのキャンセルにより無効になりました。</span><span class="sxs-lookup"><span data-stu-id="7cd85-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="7cd85-150">そこで、サービス出荷係はそのサービス注文をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="7cd85-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="7cd85-151">詳細については、[サービス注文のキャンセル](cancel-service-orders.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd85-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="7cd85-152">プロジェクトからの転記</span><span class="sxs-lookup"><span data-stu-id="7cd85-152">Post from projects</span></span>

<span data-ttu-id="7cd85-153">出荷係は、特定のプロジェクトに関連付けられているすべてのサービス注文を、必要に応じて、毎週末に転記します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="7cd85-154">その場合、出荷係は **プロジェクト** フォームの関連プロジェクトを探して、完了したサービス注文を転記します。</span><span class="sxs-lookup"><span data-stu-id="7cd85-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="7cd85-155">詳細については、[サービス注文の転記 (クラス フォーム)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd85-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="7cd85-156">サービス注文の削除</span><span class="sxs-lookup"><span data-stu-id="7cd85-156">Delete service orders</span></span>

<span data-ttu-id="7cd85-157">たとえば下半期に、ある顧客がサービス訪問の頻度が不足していると判断したとします。</span><span class="sxs-lookup"><span data-stu-id="7cd85-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="7cd85-158">この場合、サービス合意の残りの期間をカバーする、より頻度の多い一連のサービス訪問を新たに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd85-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="7cd85-159">その場合、既存のサービス注文を削除して、新しいサービス注文を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd85-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="7cd85-160">詳細については、[サービス注文の削除](delete-service-orders.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd85-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7cd85-161">参照</span><span class="sxs-lookup"><span data-stu-id="7cd85-161">See also</span></span>

<span data-ttu-id="7cd85-162">[サービス注文 (フォーム)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="7cd85-162">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]