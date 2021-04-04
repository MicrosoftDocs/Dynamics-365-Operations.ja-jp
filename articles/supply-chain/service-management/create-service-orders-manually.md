---
title: サービス注文の手動作成
description: サービス契約または **サービス注文** フォームを使用すると、サービス注文を手動で作成することができます。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72b600bc59119a6304fa043240a34051435f8691
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470956"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="29920-103">サービス注文の手動作成</span><span class="sxs-lookup"><span data-stu-id="29920-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="29920-104">サービス契約または **サービス注文** フォームを使用すると、サービス注文を手動で作成することができます。</span><span class="sxs-lookup"><span data-stu-id="29920-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="29920-105">プロジェクトからサービス注文を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="29920-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="29920-106">サービス注文の作成に自動化されたプロセスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="29920-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="29920-107">サービス契約から手動でサービス注文を作成する</span><span class="sxs-lookup"><span data-stu-id="29920-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="29920-108">**サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29920-108">Select **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="29920-109">サービス合意を選択するか、新しいサービス合意を作成します。</span><span class="sxs-lookup"><span data-stu-id="29920-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="29920-110">**作成** グループで **出荷** タブを選択し、**計画されたサービス注文** を選択して **サービス注文の作成** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="29920-110">Select the **Deliver** tab and in the **Create** group select **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="29920-111">サービス注文フォームに手動でサービス注文を作成する</span><span class="sxs-lookup"><span data-stu-id="29920-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="29920-112">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29920-112">Select **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="29920-113">**新規** を選択して、新しいサービス注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="29920-113">Select **New** to create a new service order.</span></span>

3.  <span data-ttu-id="29920-114">サービス注文のサービス注文明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="29920-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="29920-115"><STRONG>サービス管理パラメーター</STRONG>フォームの<STRONG>サービス契約無し注文の許可</STRONG>チェック ボックスをオンにすると、このサービス注文をサービス合意に関連付けることなく、サービス注文明細行のトランザクションを転記できます。</span><span class="sxs-lookup"><span data-stu-id="29920-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="29920-116">このチェック ボックスをオフにした場合は、サービス注文明細行を転記する前に、手動で作成したサービス注文をプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="29920-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="29920-117">プロジェクトからサービス注文を作成する</span><span class="sxs-lookup"><span data-stu-id="29920-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="29920-118">**プロジェクト管理および会計** \> **共通** \> **プロジェクト** \> **すべてのプロジェクト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="29920-118">Go to **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="29920-119">**アクション ウィンドウ** の **プロジェクト** フォームで、**管理** タブ \> を選択し、**サービス** \> **サービス注文** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="29920-119">In the **Projects** form, on the **Action Pane**, select the **Manage** tab \> select **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="29920-120">**サービス注文** フォームで手動でサービス注文を作成する前の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="29920-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="29920-121">**プロジェクト ID** フィールドに、プロジェクトの参照を表示します。</span><span class="sxs-lookup"><span data-stu-id="29920-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="29920-122"><STRONG>サービス管理パラメーター</STRONG>フォームの<STRONG>サービス契約無し注文の許可</STRONG>チェック ボックスをオンにすると、このサービス注文をサービス合意に関連付けることなく、サービス注文明細行のトランザクションを転記できます。</span><span class="sxs-lookup"><span data-stu-id="29920-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="29920-123">このチェック ボックスをオフにした場合は、サービス注文明細行を転記する前に、手動で作成したサービス注文をプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="29920-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="29920-124">販売注文フォームからサービス注文を作成する</span><span class="sxs-lookup"><span data-stu-id="29920-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="29920-125">**販売注文に基づいて新しいサービス注文を作成** ウィザードを使用して、**販売注文** フォームからサービス注文フォームを作成できます。</span><span class="sxs-lookup"><span data-stu-id="29920-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="29920-126">**販売とマーケティング** \> **共通** \> **販売注文** \> **すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="29920-126">Go to **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="29920-127">関連する販売注文を開きます。</span><span class="sxs-lookup"><span data-stu-id="29920-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="29920-128">**販売注文** タブで、**サービス注文** を選択して **販売注文に基づいて新しいサービス注文を作成** ウィザードを開始します。</span><span class="sxs-lookup"><span data-stu-id="29920-128">On the **Sales order** tab, select **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="29920-129">**次へ \>** を選択して、**サービス注文の契約の選択** ページで次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="29920-129">Select **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="29920-130">**サービス合意** フィールドを使用して、新しいサービス注文を関連付けるサービス契約を選択します。</span><span class="sxs-lookup"><span data-stu-id="29920-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="29920-131">オプション: **プロジェクト ID** フィールドを使用して、このサービス注文を特定のプロジェクトに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="29920-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="29920-132">**次へ \>** を選択して、**サービス注文の作成** ページで次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="29920-132">Select **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="29920-133">**優先するサービス時刻** フィールドに、サービス コールを開始する日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="29920-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="29920-134">オプション: **Description** フィールドのテキストを変更します。</span><span class="sxs-lookup"><span data-stu-id="29920-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="29920-135">既定では、このフィールドには、前のページで選択したサービス契約の説明が含まれます。</span><span class="sxs-lookup"><span data-stu-id="29920-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="29920-136">**担当** フィールドで、この契約を担当する従業員の ID を選択します。顧客が希望するサービス コールの技術者の ID がわかっている場合は、その ID も選択します。</span><span class="sxs-lookup"><span data-stu-id="29920-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="29920-137">**連絡先 ID** フィールドで、このサービス注文の窓口となる、顧客企業の担当者を指定します。</span><span class="sxs-lookup"><span data-stu-id="29920-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="29920-138">**次へ \>** を選択してから、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29920-138">Select **Next \>**, and then select **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="29920-139">参照</span><span class="sxs-lookup"><span data-stu-id="29920-139">See also</span></span>

[<span data-ttu-id="29920-140">サービス注文</span><span class="sxs-lookup"><span data-stu-id="29920-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="29920-141">サービス注文の自動作成</span><span class="sxs-lookup"><span data-stu-id="29920-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="29920-142">[サービス注文の作成 (クラス フォーム)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="29920-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]