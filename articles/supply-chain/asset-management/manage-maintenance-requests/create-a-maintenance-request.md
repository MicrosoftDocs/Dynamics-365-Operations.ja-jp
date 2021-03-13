---
title: メンテナンス要求の作成
description: このトピックでは、資産管理でメンテナンス要求を作成する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f45378405d9ea06ae847d93b7eacd9badf6d7e00
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019181"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="a6278-103">メンテナンス要求の作成</span><span class="sxs-lookup"><span data-stu-id="a6278-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a6278-104">メンテナンス要求は、メンテナンス作業者または生産作業者が機器の修理が必要であることを発見したが、修理作業をすぐに実行できない場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6278-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="a6278-105">**例:** メンテナンス作業員が修理を行っている間に、同じ場所にある別の資産にも修理が必要であることがわかります。</span><span class="sxs-lookup"><span data-stu-id="a6278-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="a6278-106">しかし、メンテナンス作業者には、修理作業を行う時間や必要な予備部品がありません。</span><span class="sxs-lookup"><span data-stu-id="a6278-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="a6278-107">それで、資産に対してメンテナンス要求を作成し、問題についての簡単な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6278-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="a6278-108">**全資産** または **有効な資産** ページ (**資産管理** \> **共通** \> **資産** \> **全資産** または **有効な資産**) の右側にある **関連情報** ウィンドウの **有効なメンテナンス要求** セクションは、選択した資産に添付された有効なメンテナンス要求を示します。</span><span class="sxs-lookup"><span data-stu-id="a6278-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="a6278-109">**資産管理** \> **共通** \> **メンテナンス要求** \> **すべてのメンテナンス要求** または **有効なメンテナンス要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="a6278-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-110">Select **New**.</span></span>
3. <span data-ttu-id="a6278-111">**メンテナンス要求タイプ** フィールドの **要求の作成** ダイアログ ボックスで、メンテナンス要求のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="a6278-112">既定のタイプが推奨されます。</span><span class="sxs-lookup"><span data-stu-id="a6278-112">A default type is suggested.</span></span>
4. <span data-ttu-id="a6278-113">**説明** フィールドに、メンテナンス要求を簡単に説明する名前またはタイトルを入力します。</span><span class="sxs-lookup"><span data-stu-id="a6278-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="a6278-114">**機能の場所** および **資産** フィールドで、必要に応じて、機能の場所または資産、または機能の場所と資産の組み合わせを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="a6278-115">資産を選択せずにメンテナンス要求を作成し、後でメンテナス要求に資産を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="a6278-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="a6278-116">サインインしているメンテナンス作業者が資産に関連するリソースに関連している場合、**資産** フィールドが自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a6278-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="a6278-117">メンテナンス要求が選択した資産に既に添付されている場合は、**要求の作成** ダイアログ ボックスの上部にメッセージ バーが表示され、既存のメンテナンス要求の ID について通知されます。</span><span class="sxs-lookup"><span data-stu-id="a6278-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="a6278-118">また、資産が保証契約の対象となる場合にもメッセージ バーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6278-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="a6278-119">**サービス レベル** フィールドで、要求の緊急性を示すサービス レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="a6278-120">ステップ 5 で資産を選択した場合は、**エラーの症状**、**エラーの領域**、および **エラー タイプ** フィールドを使用して、エラー登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6278-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="a6278-121">メンテナンス要求によってメンテナンス ダウンタイムが発生した場合は、ダウンタイムの開始日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6278-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="a6278-122">**開始者** フィールドは自動的にユーザーの名前に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a6278-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="a6278-123">**実際の開始** フィールドは自動的に現在の日時に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a6278-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="a6278-124">必要に応じて値を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="a6278-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="a6278-125">**メモ** フィールドに、必要な追加のメモを入力します。</span><span class="sxs-lookup"><span data-stu-id="a6278-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="a6278-126">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-126">Select **OK**.</span></span>

![メンテナンス要求の作成](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="a6278-128">メンテナンス要求の後続プロセス</span><span class="sxs-lookup"><span data-stu-id="a6278-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="a6278-129">メンテナンス要求が作成された後、作業指示書に変換する前に、さまざまな情報を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6278-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="a6278-130">通常、計画担当者またはその他の管理職員がこのタスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="a6278-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="a6278-131">**すべてのメンテナンス要求** または **有効なメンテナンス要求** ページで、作業する要求を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="a6278-132">詳細ビューでは、さまざまな情報を更新できます。</span><span class="sxs-lookup"><span data-stu-id="a6278-132">In the details view, you can update various information.</span></span> <span data-ttu-id="a6278-133">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="a6278-133">Here are some examples:</span></span>

- <span data-ttu-id="a6278-134">資産を選択して確認します。</span><span class="sxs-lookup"><span data-stu-id="a6278-134">Select and verify the asset.</span></span> <span data-ttu-id="a6278-135">後で別の資産を選択する必要がある場合は、**検証済資産** オプションを **いいえ** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a6278-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="a6278-136">担当メンテナンス作業者グループおよび/または担当メンテナンス作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="a6278-137">必要な設定の詳細については、[担当メンテナンス作業者](../setup-for-maintenance-requests/responsible-workers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6278-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="a6278-138">メンテナンス作業タイプを選択し、この情報が関連する場合は、関連するメンテナンス作業バリアントおよび作業トレードを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="a6278-139">**緯度** フィールドと **経度** フィールドに地理座標を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6278-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="a6278-140">メンテナンス要求に追加された座標は、関連する作業指示書に自動的に転送されます。</span><span class="sxs-lookup"><span data-stu-id="a6278-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![メンテナンス要求の更新](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="a6278-142">メンテナンス要求の作成時に資産を選択した場合は、資産に 1 つのエラーを追加できます。</span><span class="sxs-lookup"><span data-stu-id="a6278-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="a6278-143">メンテナンス要求を作成したら、必要に応じてさらにエラーを追加できます。</span><span class="sxs-lookup"><span data-stu-id="a6278-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="a6278-144">エラーを追加するには、**すべてのメンテナンス要求** ページの **資産エラー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6278-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
