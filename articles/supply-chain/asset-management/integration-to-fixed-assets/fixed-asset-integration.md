---
title: 資産管理と固定資産の統合
description: このトピックでは、資産管理と固定資産のモジュールを統合して、固定資産を保守資産にリンクできるようにする方法について説明します。
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 879950b9aeb345fcd59dfe73d3963a44607c7ac2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994232"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="508f7-103">資産管理と固定資産の統合</span><span class="sxs-lookup"><span data-stu-id="508f7-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="508f7-104">**資産管理** と **固定資産** モジュールを統合することで、固定資産とメンテナンス資産を連動させることができます。</span><span class="sxs-lookup"><span data-stu-id="508f7-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="508f7-105">固定資産ユーザーは、新しい固定資産または既存の固定資産から保守資産を作成できます。また、資産管理ユーザーは、メンテナンス資産を既存の固定資産に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="508f7-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="508f7-106">この機能を使用すると、固定資産のユーザーは、関連するメンテナンス資産の作業指示書から転記されたコストを簡単に表示することができます。</span><span class="sxs-lookup"><span data-stu-id="508f7-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="508f7-107">このトピックでは *メンテナンス資産* は **資産管理** モジュールからの資産を参照し、 *固定資産* は **固定資産** モジュールからの資産を参照します。</span><span class="sxs-lookup"><span data-stu-id="508f7-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="508f7-108">固定資産から作成される新しい保守資産の既定の場所を設定します (オプション)</span><span class="sxs-lookup"><span data-stu-id="508f7-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="508f7-109">このオプション設定では、固定資産から作成される新しいメンテナンス資産の既定の機能の場所を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="508f7-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="508f7-110">通常は、この構成を完了させるのは一度だけです。</span><span class="sxs-lookup"><span data-stu-id="508f7-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="508f7-111">この構成を完了するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="508f7-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="508f7-112">**資産管理 \> 設定 \> 資産管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="508f7-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="508f7-113">**固定資産** タブの、**機能の場所** フィールドで、既定の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="508f7-114">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="508f7-115">統合されたメンテナンス資産と固定資産で作業をする</span><span class="sxs-lookup"><span data-stu-id="508f7-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="508f7-116">このセクションでは、資産管理と固定資産の統合機能を使用するにあたってのさまざまな方法を紹介します。</span><span class="sxs-lookup"><span data-stu-id="508f7-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="508f7-117">既存のメンテナンス資産を固定資産に関連付ける</span><span class="sxs-lookup"><span data-stu-id="508f7-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="508f7-118">既存のメンテナンス資産を固定資産に関連付けるには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="508f7-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="508f7-119">**資産管理 \> 資産 \> すべての資産**（または、**有効な資産**）に移動します。</span><span class="sxs-lookup"><span data-stu-id="508f7-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="508f7-120">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-120">Select an asset.</span></span>
1. <span data-ttu-id="508f7-121">**固定資産**  クイックタブの **固定資産番号** フィールドで、既存の固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="508f7-122">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="508f7-123">選択した管理資産に関連付けられている固定資産を表示します</span><span class="sxs-lookup"><span data-stu-id="508f7-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="508f7-124">選択したメンテナンス資産に関連付けられている固定資産を表示するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="508f7-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="508f7-125">**資産管理 \> 資産 \> すべての資産**（または、**有効な資産**）に移動します。</span><span class="sxs-lookup"><span data-stu-id="508f7-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="508f7-126">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-126">Select an asset.</span></span>
1. <span data-ttu-id="508f7-127">**固定資産**  クイックタブの **固定資産番号** フィールドで、リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="508f7-128">選択した資産の **固定資産** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="508f7-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="508f7-129">（通常、このページは **固定資産 \> 固定資産 \> 固定資産** にあります）</span><span class="sxs-lookup"><span data-stu-id="508f7-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="508f7-130">選択した固定資産に関連付けられているメンテナンス資産を表示します</span><span class="sxs-lookup"><span data-stu-id="508f7-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="508f7-131">選択した固定資産に関連付けられているメンテナンス資産を表示するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="508f7-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="508f7-132">**固定資産 \> 固定資産 \>固定資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="508f7-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="508f7-133">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-133">Select an asset.</span></span>
1. <span data-ttu-id="508f7-134">アクション ウインドウの **資産管理** タブの **表示** グループで、**メンテナンス資産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="508f7-135">選択した固定資産に関連付けられている **メンテナンス資産** のページを表示するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="508f7-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="508f7-136">(通常、このページは **資産管理 \> 資産 \> のすべての資産** にあります)</span><span class="sxs-lookup"><span data-stu-id="508f7-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="508f7-137">固定資産に関連付けられているメンテナンス費用の表示</span><span class="sxs-lookup"><span data-stu-id="508f7-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="508f7-138">資産管理の作業指示書をメンテナンス資産に転記することができます。また、これらの各作業指示書には、通常はコストが設定されています。</span><span class="sxs-lookup"><span data-stu-id="508f7-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="508f7-139">固定資産がメンテナンス資産に関連付けられている場合は、固定資産から直接移動して、関連するコストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="508f7-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="508f7-140">選択した固定資産に関連付けられているメンテナンス コストを表示するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="508f7-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="508f7-141">**固定資産 \> 固定資産 \>固定資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="508f7-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="508f7-142">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-142">Select an asset.</span></span>
1. <span data-ttu-id="508f7-143">アクション ウインドウの **資産管理** タブの **表示** グループで、**メンテナンス コスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="508f7-144">**メンテナンス コスト** のページが開き、関連するコストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="508f7-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="508f7-145">既存の固定資産で使用する新規メンテナンス資産を作成する</span><span class="sxs-lookup"><span data-stu-id="508f7-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="508f7-146">既存の固定資産で使用する新規メンテナンス資産を作成するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="508f7-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="508f7-147">**固定資産 \> 固定資産 \>固定資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="508f7-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="508f7-148">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-148">Select an asset.</span></span>
1. <span data-ttu-id="508f7-149">アクション ウインドウの **資産管理** タブの **新規** グループで、**メンテナンス資産を作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="508f7-150">（このオプションが使用できない場合は、選択した固定資産に対して、保守資産が既に関連付けられている可能性があります）</span><span class="sxs-lookup"><span data-stu-id="508f7-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="508f7-151">[資産を作成する](../objects/create-an-object.md) に記載の手順に従って、資産の作成を完了します。</span><span class="sxs-lookup"><span data-stu-id="508f7-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="508f7-152">新たな固定資産を作成して、そこに新規メンテナンス資産を追加します</span><span class="sxs-lookup"><span data-stu-id="508f7-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="508f7-153">固定資産を新しく作成して、新規メンテナンス資産を追加するには、、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="508f7-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="508f7-154">**固定資産 \> 固定資産 \>固定資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="508f7-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="508f7-155">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="508f7-156">[資産を作成する](../../../finance/fixed-assets/tasks/create-fixed-asset.md) に記載の手順に従って、固定資産の作成を完了します。</span><span class="sxs-lookup"><span data-stu-id="508f7-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="508f7-157">アクション ウインドウの **資産管理** タブの **新規** グループで、**メンテナンス資産を作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="508f7-158">[資産を作成する](../objects/create-an-object.md) に記載の手順に従って、資産の作成を完了します。</span><span class="sxs-lookup"><span data-stu-id="508f7-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="508f7-159">2 つの資産間の関連付けを削除する</span><span class="sxs-lookup"><span data-stu-id="508f7-159">Remove the association between two assets</span></span>

<span data-ttu-id="508f7-160">場合によっては、固定資産からメンテナンス資産の関連付けを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="508f7-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="508f7-161">たとえば、固定資産から [新しいメンテナンス資産を作成する場合](#new-maintenance-from-fixed) は、最初に既存の関連付けをすべて削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="508f7-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="508f7-162">メンテナンス資産と固定資産に設定されている関連付けを削除するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="508f7-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="508f7-163">**資産管理 \> 資産 \> すべての資産**（または、**有効な資産**）に移動します。</span><span class="sxs-lookup"><span data-stu-id="508f7-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="508f7-164">固定資産を検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="508f7-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="508f7-165">**固定資産** クイックタブで、**機能の場所** フィールドの値を削除します。</span><span class="sxs-lookup"><span data-stu-id="508f7-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="508f7-166">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="508f7-166">On the Action Pane, select **Save**.</span></span>
