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
ms.openlocfilehash: adc14019c243b1992cdaa22ef7aa32cb44bfffd9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253593"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="8de9a-103">資産管理と固定資産の統合</span><span class="sxs-lookup"><span data-stu-id="8de9a-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8de9a-104">**資産管理** と **固定資産** モジュールを統合することで、固定資産とメンテナンス資産を連動させることができます。</span><span class="sxs-lookup"><span data-stu-id="8de9a-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="8de9a-105">固定資産ユーザーは、新しい固定資産または既存の固定資産から保守資産を作成できます。また、資産管理ユーザーは、メンテナンス資産を既存の固定資産に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="8de9a-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="8de9a-106">この機能を使用すると、固定資産のユーザーは、関連するメンテナンス資産の作業指示書から転記されたコストを簡単に表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8de9a-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="8de9a-107">このトピックでは *メンテナンス資産* は **資産管理** モジュールからの資産を参照し、 *固定資産* は **固定資産** モジュールからの資産を参照します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="8de9a-108">固定資産から作成される新しい保守資産の既定の場所を設定します (オプション)</span><span class="sxs-lookup"><span data-stu-id="8de9a-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="8de9a-109">このオプション設定では、固定資産から作成される新しいメンテナンス資産の既定の機能の場所を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="8de9a-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="8de9a-110">通常は、この構成を完了させるのは一度だけです。</span><span class="sxs-lookup"><span data-stu-id="8de9a-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="8de9a-111">この構成を完了するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9a-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="8de9a-112">**資産管理 \> 設定 \> 資産管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="8de9a-113">**固定資産** タブの、**機能の場所** フィールドで、既定の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="8de9a-114">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="8de9a-115">統合されたメンテナンス資産と固定資産で作業をする</span><span class="sxs-lookup"><span data-stu-id="8de9a-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="8de9a-116">このセクションでは、資産管理と固定資産の統合機能を使用するにあたってのさまざまな方法を紹介します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="8de9a-117">既存のメンテナンス資産を固定資産に関連付ける</span><span class="sxs-lookup"><span data-stu-id="8de9a-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="8de9a-118">既存のメンテナンス資産を固定資産に関連付けるには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9a-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="8de9a-119">**資産管理 \> 資産 \> すべての資産**（または、**有効な資産**）に移動します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="8de9a-120">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-120">Select an asset.</span></span>
1. <span data-ttu-id="8de9a-121">**固定資産**  クイックタブの **固定資産番号** フィールドで、既存の固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="8de9a-122">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="8de9a-123">選択した管理資産に関連付けられている固定資産を表示します</span><span class="sxs-lookup"><span data-stu-id="8de9a-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="8de9a-124">選択したメンテナンス資産に関連付けられている固定資産を表示するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9a-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="8de9a-125">**資産管理 \> 資産 \> すべての資産**（または、**有効な資産**）に移動します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="8de9a-126">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-126">Select an asset.</span></span>
1. <span data-ttu-id="8de9a-127">**固定資産**  クイックタブの **固定資産番号** フィールドで、リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="8de9a-128">選択した資産の **固定資産** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="8de9a-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="8de9a-129">（通常、このページは **固定資産 \> 固定資産 \> 固定資産** にあります）</span><span class="sxs-lookup"><span data-stu-id="8de9a-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="8de9a-130">選択した固定資産に関連付けられているメンテナンス資産を表示します</span><span class="sxs-lookup"><span data-stu-id="8de9a-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="8de9a-131">選択した固定資産に関連付けられているメンテナンス資産を表示するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9a-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="8de9a-132">**固定資産 \> 固定資産 \>固定資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="8de9a-133">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-133">Select an asset.</span></span>
1. <span data-ttu-id="8de9a-134">アクション ウインドウの **資産管理** タブの **表示** グループで、**メンテナンス資産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="8de9a-135">選択した固定資産に関連付けられている **メンテナンス資産** のページを表示するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9a-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="8de9a-136">(通常、このページは **資産管理 \> 資産 \> のすべての資産** にあります)</span><span class="sxs-lookup"><span data-stu-id="8de9a-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="8de9a-137">固定資産に関連付けられているメンテナンス費用の表示</span><span class="sxs-lookup"><span data-stu-id="8de9a-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="8de9a-138">資産管理の作業指示書をメンテナンス資産に転記することができます。また、これらの各作業指示書には、通常はコストが設定されています。</span><span class="sxs-lookup"><span data-stu-id="8de9a-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="8de9a-139">固定資産がメンテナンス資産に関連付けられている場合は、固定資産から直接移動して、関連するコストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="8de9a-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="8de9a-140">選択した固定資産に関連付けられているメンテナンス コストを表示するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9a-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="8de9a-141">**固定資産 \> 固定資産 \>固定資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="8de9a-142">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-142">Select an asset.</span></span>
1. <span data-ttu-id="8de9a-143">アクション ウインドウの **資産管理** タブの **表示** グループで、**メンテナンス コスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="8de9a-144">**メンテナンス コスト** のページが開き、関連するコストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8de9a-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="8de9a-145">既存の固定資産で使用する新規メンテナンス資産を作成する</span><span class="sxs-lookup"><span data-stu-id="8de9a-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="8de9a-146">既存の固定資産で使用する新規メンテナンス資産を作成するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9a-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="8de9a-147">**固定資産 \> 固定資産 \>固定資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="8de9a-148">資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-148">Select an asset.</span></span>
1. <span data-ttu-id="8de9a-149">アクション ウインドウの **資産管理** タブの **新規** グループで、**メンテナンス資産を作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="8de9a-150">（このオプションが使用できない場合は、選択した固定資産に対して、保守資産が既に関連付けられている可能性があります）</span><span class="sxs-lookup"><span data-stu-id="8de9a-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="8de9a-151">[資産を作成する](../objects/create-an-object.md) に記載の手順に従って、資産の作成を完了します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="8de9a-152">新たな固定資産を作成して、そこに新規メンテナンス資産を追加します</span><span class="sxs-lookup"><span data-stu-id="8de9a-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="8de9a-153">固定資産を新しく作成して、新規メンテナンス資産を追加するには、、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9a-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="8de9a-154">**固定資産 \> 固定資産 \>固定資産** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="8de9a-155">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8de9a-156">[資産を作成する](../../../finance/fixed-assets/tasks/create-fixed-asset.md) に記載の手順に従って、固定資産の作成を完了します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="8de9a-157">アクション ウインドウの **資産管理** タブの **新規** グループで、**メンテナンス資産を作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="8de9a-158">[資産を作成する](../objects/create-an-object.md) に記載の手順に従って、資産の作成を完了します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="8de9a-159">2 つの資産間の関連付けを削除する</span><span class="sxs-lookup"><span data-stu-id="8de9a-159">Remove the association between two assets</span></span>

<span data-ttu-id="8de9a-160">場合によっては、固定資産からメンテナンス資産の関連付けを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8de9a-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="8de9a-161">たとえば、固定資産から [新しいメンテナンス資産を作成する場合](#new-maintenance-from-fixed) は、最初に既存の関連付けをすべて削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8de9a-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="8de9a-162">メンテナンス資産と固定資産に設定されている関連付けを削除するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8de9a-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="8de9a-163">**資産管理 \> 資産 \> すべての資産**（または、**有効な資産**）に移動します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="8de9a-164">固定資産を検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="8de9a-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="8de9a-165">**固定資産** クイックタブで、**機能の場所** フィールドの値を削除します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="8de9a-166">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8de9a-166">On the Action Pane, select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]