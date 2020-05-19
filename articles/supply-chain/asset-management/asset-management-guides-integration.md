---
title: Dynamics 365 Supply Chain Management（資産管理）と Dynamics 365 Guides を統合する
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の資産管理モジュールを Dynamics 365 Guides に統合して、日々のサービスやメンテナンスのワークフローで Mixed Reality ガイドを活用する方法について説明します。
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f9ee7f1af8e88f56589c84bfaa063ea005aa353a
ms.sourcegitcommit: 88b4a9d19d16b0ef6543adf7c378a08bf0e07b3a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2020
ms.locfileid: "3311784"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="5c47b-103">Dynamics 365 Supply Chain Management（資産管理）と Dynamics 365 Guides を統合する</span><span class="sxs-lookup"><span data-stu-id="5c47b-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="5c47b-104">Dynamics 365 Supply Chain Management の **資産管理** モジュールを Microsoft Dynamics 365 Guides に統合することで、日々のサービスやメンテナンスのワークフローで、Mixed Reality ガイドを活用することができます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="5c47b-105">ガイドが資産管理の作業指示に関連付けられている場合、Supply Chain Management（Dynamics 365）モバイル アプリで作業指示のメンテナンス チェック リストを開いた作業員は、ガイドが利用可能であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5c47b-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="5c47b-106">続いて、作業者は Dynamics 365 Guides HoloLens アプリでガイドを検索して開いてください。</span><span class="sxs-lookup"><span data-stu-id="5c47b-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5c47b-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="5c47b-107">Prerequisites</span></span>

<span data-ttu-id="5c47b-108">資産管理ワークオーダーにガイドを適用するには、次の前提条件を実行する必要があります：</span><span class="sxs-lookup"><span data-stu-id="5c47b-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="5c47b-109">[Dynamics 365 Supply Chain Management の設定](../../fin-ops-core/fin-ops/index.md) バージョン 10.0.9 またはそれ以降。</span><span class="sxs-lookup"><span data-stu-id="5c47b-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="5c47b-110">[Supply Chain Management アプリに対してデュアル書き込みを有効化します](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="5c47b-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="5c47b-111">**MRGuidesFeature** 機能の [フライトを有効](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) にします。</span><span class="sxs-lookup"><span data-stu-id="5c47b-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="5c47b-112">（実稼働環境の場合は、最初にサポート チケットを送信して、テナントを flighting グループに追加する必要があります。）</span><span class="sxs-lookup"><span data-stu-id="5c47b-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="5c47b-113">**ライセンスの構成** ページで、[次の構成キーを有効にします](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference)：</span><span class="sxs-lookup"><span data-stu-id="5c47b-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="5c47b-114">資産管理 \> 資産管理の Mixed Reality</span><span class="sxs-lookup"><span data-stu-id="5c47b-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="5c47b-115">Mixed reality \> Mixed reality ガイド</span><span class="sxs-lookup"><span data-stu-id="5c47b-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="5c47b-116">[Dynamics 365 Guides の設定](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) バージョン 200.0.0.96 またはそれ以降。</span><span class="sxs-lookup"><span data-stu-id="5c47b-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="5c47b-117">Dynamics 365 Guides と資産管理を併用する</span><span class="sxs-lookup"><span data-stu-id="5c47b-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="5c47b-118">ガイドを関連付けるには、資産管理のメンテナンス チェックリストの行を使用します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="5c47b-119">メンテナンス チェックリストのテンプレート、メンテナンス作業タイプは、3つともメンテナンス チェックリストの行が含まれているため、作業指示書を使って関連付けを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="5c47b-120">テンプレートは、それを使用するすべてのメンテナンス作業タイプに関連付けることができるため、テンプレートを使用して時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="5c47b-121">たとえば、メンテナンス作業タイプに関連付けられているガイドは、その作業タイプを指定するすべての作業指示書に自動的に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="5c47b-122">一方、作業指示書に直接関連付けられているガイドは、その作業指示書にしか存在しません。</span><span class="sxs-lookup"><span data-stu-id="5c47b-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="5c47b-123">メンテナンス チェックリストのテンプレートをガイドに関連付ける</span><span class="sxs-lookup"><span data-stu-id="5c47b-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="5c47b-124">メンテナンス チェックリストのテンプレートをガイドに関連付けるには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="5c47b-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="5c47b-125">Dynamics 365 Guides PC と HoloLens アプリを使用してガイドを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="5c47b-126">ガイドの作成方法については、以下のトピックを参照してください：</span><span class="sxs-lookup"><span data-stu-id="5c47b-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="5c47b-127">PC アプリを使用してガイドを作成する</span><span class="sxs-lookup"><span data-stu-id="5c47b-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="5c47b-128">HoloLens アプリを使用してホログラムを配置します</span><span class="sxs-lookup"><span data-stu-id="5c47b-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="5c47b-129">Supply Chain Management で、[メンテナンス チェックリストのテンプレートを作成](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template) します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="5c47b-130">新しいメンテナンス チェックリストで、作成したガイドとメンテナンス チェックリストの明細を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="5c47b-131">**メンテナンス チェックリスト** のクイックタブで、ガイドを関連付ける明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="5c47b-132">**関連するガイド** のクイックタブで、**ガイドの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="5c47b-133">![メンテナンス チェックリストのテンプレートをガイドに関連付ける](media/am-guides-integration-add-guide.png "メンテナンス チェックリストのテンプレートをガイドに関連付ける")</span><span class="sxs-lookup"><span data-stu-id="5c47b-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="5c47b-134">**名前** フィールドで、ガイドを選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="5c47b-135">![名前フィールドでガイドを選択します](media/am-guides-integration-select-guide.png "名前フィールドでガイドを選択します")</span><span class="sxs-lookup"><span data-stu-id="5c47b-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="5c47b-136">メンテナンス チェックリストのテンプレートを作業タイプに関連付ける：</span><span class="sxs-lookup"><span data-stu-id="5c47b-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="5c47b-137">[メンテナンス作業タイプを作成する](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type)か、既存のメンテナンス作業タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="5c47b-138">アクション ウィンドウで、**メンテナンス作業タイプの既定値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="5c47b-139">![メンテナンス作業タイプの既定値のページ](media/am-guides-integration-job-defaults.png "メンテナンス作業タイプの既定値のページ")</span><span class="sxs-lookup"><span data-stu-id="5c47b-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="5c47b-140">行を作成し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="5c47b-141">![行の作成](media/am-guides-integration-add-line.png "行の作成を行います") を行います</span><span class="sxs-lookup"><span data-stu-id="5c47b-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="5c47b-142">アクション ウィンドウで、**メンテナンス チェックリスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="5c47b-143">![メンテナンス チェックリスト ボタン](media/am-guides-integration-maintenance-checklist.png "メンテナンス チェックリスト ボタン")</span><span class="sxs-lookup"><span data-stu-id="5c47b-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="5c47b-144">**メンテナンス チェックリスト** のクイックタブで、行を追加し、**タイプ** フィールドの値を **テンプレート** に変更し ます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="5c47b-145">![種別の値を変更する](media/am-guides-integration-checklist-lines.png "種別の値を変更する")</span><span class="sxs-lookup"><span data-stu-id="5c47b-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="5c47b-146">**行の詳細** クイックタブの **テンプレート** フィールドで、ガイドを関連付けたテンプレートを選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="5c47b-147">![テンプレートを選択します](media/am-guides-integration-checklist-line-details.png "テンプレートを選択します")</span><span class="sxs-lookup"><span data-stu-id="5c47b-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="5c47b-148">[作業指示書を作成](work-orders/manually-created-workorders.md#create-work-order) し、ガイドに関連付けられているメンテナンス チェックリストのテンプレートを使用するメンテナンス作業タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="5c47b-149">ガイドが自動的に作業指示書に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="5c47b-150">![メンテナンス作業タイプを選択する](media/am-guides-integration-create-work-order.png "メンテナンス作業タイプを選択する")</span><span class="sxs-lookup"><span data-stu-id="5c47b-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="5c47b-151">作業指示書と作業者に関連付けられているガイドを表示します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="5c47b-152">[資産管理のモバイル ワークスペース](asset-management-mobile-workspace.md) を開いて、作業指示書にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5c47b-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="5c47b-153">作業指示書の [メンテナンス チェックリストを開きます](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job)。</span><span class="sxs-lookup"><span data-stu-id="5c47b-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="5c47b-154">チェックリストの明細行を選択して、関連するガイドを表示します。</span><span class="sxs-lookup"><span data-stu-id="5c47b-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="5c47b-155">![チェックリスト明細行に関連付けられているガイド](media/am-guides-integration-show-guide.png "チェックリスト明細行に関連付けられているガイド")</span><span class="sxs-lookup"><span data-stu-id="5c47b-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="5c47b-156">HoloLens のガイドを開きます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="5c47b-157">![HoloLens のガイドを開く](media/am-guides-integration-hololens-select.png "HoloLens のガイドを開きます")</span><span class="sxs-lookup"><span data-stu-id="5c47b-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="5c47b-158">また、作業指示書や作業タイプのメンテナンス チェックリストにガイドを直接関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c47b-159">メンテナンス チェックリストのテンプレートを既定のメンテナンス作業タイプに関連付けた場合、そのテンプレートにリンクされているガイドは、 **メンテナンス ジョブ タイプの既定値 ページの**関連するガイド**クイックタブには表示されません**。</span><span class="sxs-lookup"><span data-stu-id="5c47b-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="5c47b-160">ただし、**関連するガイド** のクイックタブでは、その作業タイプが作業指示に適用された後にこのガイドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c47b-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c47b-161">参照</span><span class="sxs-lookup"><span data-stu-id="5c47b-161">See also</span></span>

- [<span data-ttu-id="5c47b-162">二重書き込みの概要</span><span class="sxs-lookup"><span data-stu-id="5c47b-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="5c47b-163">資産管理の概要</span><span class="sxs-lookup"><span data-stu-id="5c47b-163">Asset management overview</span></span>](index.md)
