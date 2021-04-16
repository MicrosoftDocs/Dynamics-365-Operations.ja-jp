---
title: 資産管理モバイル ワークスペースの使用
description: このトピックでは、資産管理モバイル ワークスペースに関する情報を示します。
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 98f935a11ad8a5272cde0270f9ae0471411b914a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837948"
---
# <a name="use-the-asset-management-mobile-workspace"></a><span data-ttu-id="37af1-103">資産管理モバイル ワークスペースの使用</span><span class="sxs-lookup"><span data-stu-id="37af1-103">Use the Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37af1-104">このトピックでは、**資産管理** モバイル ワークスペースに関する情報を示します。</span><span class="sxs-lookup"><span data-stu-id="37af1-104">This topic provides information about the **Asset management** mobile workspace.</span></span> <span data-ttu-id="37af1-105">このワークスペースでは、ユーザーがメンテナンス要求と作業指示を表示および作成できます。</span><span class="sxs-lookup"><span data-stu-id="37af1-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="37af1-106">ユーザーは、カレンダーまたはリスト表示で、割り当てられた作業指示書ジョブを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="37af1-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="37af1-107">資産と機能の場所を表示したり、検索したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="37af1-107">Assets and functional locations can also be viewed and searched for.</span></span>

## <a name="overview"></a><span data-ttu-id="37af1-108">概要</span><span class="sxs-lookup"><span data-stu-id="37af1-108">Overview</span></span>

<span data-ttu-id="37af1-109">資産管理は、Dynamics 365 Supply Chain Management の資産およびワーク オーダー ジョブを管理するための高度なモジュールです。</span><span class="sxs-lookup"><span data-stu-id="37af1-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="37af1-110">**資産管理** モバイル ワークスペースを使用すると、ユーザーは、選択したモバイルデバイスで、割り当てられた作業指示書ジョブを簡単に表示できます。</span><span class="sxs-lookup"><span data-stu-id="37af1-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="37af1-111">また、メンテナンス要求の作成と管理、ライフサイクル状態の更新、およびモバイルデバイスを使用した資産と機能的な場所の詳細の表示を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="37af1-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="37af1-112">特に、**資産管理** モバイル ワークスペースにより、ユーザーは次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="37af1-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="37af1-113">メンテナンス要求の作成、表示、編集、メンテナンス要求への写真の送信、メンテナンス要求ライフサイクルの状態の変更を行います。</span><span class="sxs-lookup"><span data-stu-id="37af1-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="37af1-114">作業指示書の作成、表示、編集、作業指示書への写真の送信、作業指示書ライフサイクルの状態の変更、作業指示書ジョブを行います。</span><span class="sxs-lookup"><span data-stu-id="37af1-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="37af1-115">カレンダー表示での割り当てられた作業指示書ジョブを表示します。</span><span class="sxs-lookup"><span data-stu-id="37af1-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="37af1-116">作業指示書ジョブの作成、表示、および編集、資産カウンターの更新、メンテナンス チェックリストの表示、および作業指示書ジョブのメモの表示と編集を行います。この作業指示書ジョブに必要なツールを表示します。</span><span class="sxs-lookup"><span data-stu-id="37af1-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="37af1-117">特定の資産または機能的な場所を表示または検索します。</span><span class="sxs-lookup"><span data-stu-id="37af1-117">View or search for a specific asset or functional location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37af1-118">必要条件</span><span class="sxs-lookup"><span data-stu-id="37af1-118">Prerequisites</span></span>

<span data-ttu-id="37af1-119">**資産管理** モバイル ワークスペースを使用するには、管理者が必要なユーザー アカウントと作業者アカウントを設定し、ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37af1-119">Before you can use the **Asset management** mobile workspace, your admin must set up the required user and worker accounts, and publish the workspace.</span></span> <span data-ttu-id="37af1-120">詳細については、[資産管理モバイル ワークスペースの設定](set-up-asset-management-mobile.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37af1-120">For more information, see [Set up the Asset management mobile workspace](set-up-asset-management-mobile.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="37af1-121">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="37af1-121">Download and install the mobile app</span></span>

<span data-ttu-id="37af1-122">Dynamics 365 for Unified Operations モバイル アプリをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="37af1-122">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="37af1-123">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="37af1-123">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="37af1-124">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="37af1-124">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="37af1-125">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="37af1-125">Sign in to the mobile app</span></span>

1. <span data-ttu-id="37af1-126">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="37af1-126">Start the app on your mobile device.</span></span>

1. <span data-ttu-id="37af1-127">Dynamics 365 の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-127">Enter your Dynamics 365 URL.</span></span>

1. <span data-ttu-id="37af1-128">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="37af1-128">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="37af1-129">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-129">Enter your credentials.</span></span>

1. <span data-ttu-id="37af1-130">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="37af1-130">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="37af1-131">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37af1-131">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="37af1-132">![ワークスペースの選択](media/am-mobile-01.png "ワークスペースの選択")</span><span class="sxs-lookup"><span data-stu-id="37af1-132">![Select a workspace](media/am-mobile-01.png "Select a workspace")</span></span>

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="37af1-133">カレンダー表示の割り当てられた作業指示書ジョブの表示</span><span class="sxs-lookup"><span data-stu-id="37af1-133">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="37af1-134">モバイル デバイスで、**資産管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="37af1-134">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="37af1-135">**自分の作業指示書ジョブカレンダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-135">Select **My work order jobs calendar**.</span></span>

1. <span data-ttu-id="37af1-136">作業指示書ジョブを表示する日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-136">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="37af1-137">一覧には、各作業指示書ジョブの資産 ID と機能的な場所の ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="37af1-137">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

1. <span data-ttu-id="37af1-138">ジョブの詳細を表示するには、一覧の作業指示書ジョブを選択します。資産と機能的な場所の詳細、および **添付ファイル**、**チェックリスト**、**ツール**、**資産カウンター**、**メモ**、**仕訳帳** を表示する、その他のナビゲーションリンクなどがあります。</span><span class="sxs-lookup"><span data-stu-id="37af1-138">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

    <span data-ttu-id="37af1-139">![カレンダー表示の割り当てられた作業指示書ジョブの表示](media/am-mobile-02.png "カレンダー表示の割り当てられた作業指示書ジョブの表示")</span><span class="sxs-lookup"><span data-stu-id="37af1-139">![View assigned work order jobs in calendar view](media/am-mobile-02.png "View assigned work order jobs in calendar view")</span></span>

## <a name="create-a-work-order-job"></a><span data-ttu-id="37af1-140">作業指示書ジョブの作成</span><span class="sxs-lookup"><span data-stu-id="37af1-140">Create a work order job</span></span>

1. <span data-ttu-id="37af1-141">モバイル デバイスで、**資産管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="37af1-141">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="37af1-142">すべての **メンテナンス作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-142">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="37af1-143">新しい作業指示書ジョブを作成する作業指示書を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-143">Select the work order you want to create a new work order job for.</span></span>

1. <span data-ttu-id="37af1-144">**明細行の追加** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-144">Select the **Add line** button.</span></span>

1. <span data-ttu-id="37af1-145">作業指示書ジョブを作成する **資産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-145">Select the **Asset** you want to create a work order job for.</span></span>

1. <span data-ttu-id="37af1-146">**メンテナンス作業タイプ**、**メンテナンス作業タイプ バリアント**、および **取引** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-146">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

1. <span data-ttu-id="37af1-147">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-147">Select **Done**.</span></span>

    <span data-ttu-id="37af1-148">![明細行の追加画面](media/am-mobile-03.png "明細行の追加画面")</span><span class="sxs-lookup"><span data-stu-id="37af1-148">![The Add line screen](media/am-mobile-03.png "The Add line screen")</span></span>


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="37af1-149">作業指示書ジョブへの添付ファイルの追加</span><span class="sxs-lookup"><span data-stu-id="37af1-149">Add attachment to a work order job</span></span>

1. <span data-ttu-id="37af1-150">モバイル デバイスで、**資産管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="37af1-150">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="37af1-151">すべての **メンテナンス作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-151">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="37af1-152">作業指示書、添付ファイルを追加する作業指示書ジョブの順に選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-152">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="37af1-153">または、ホームページの **自分の作業指示書ジョブカレンダー** または **自分の作業指示書ジョブの一覧** を選択して、**作業指示書ジョブの詳細** ページに移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="37af1-153">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

1. <span data-ttu-id="37af1-154">**作業指示書ジョブの詳細** ページの **添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-154">Select **Attachments** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="37af1-155">既存の添付ファイルが、作業指示書ジョブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="37af1-155">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="37af1-156">**添付ファイルの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-156">Select **Add attachment**.</span></span>

1. <span data-ttu-id="37af1-157">添付ファイルの **名前** と **メモ** を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-157">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="37af1-158">**画像の選択** を選択して、モバイルギャラリーから写真を選択するか、**写真を撮る** を選択して写真を撮影します。</span><span class="sxs-lookup"><span data-stu-id="37af1-158">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="37af1-159">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-159">Select **Done**.</span></span>

    <span data-ttu-id="37af1-160">![作業指示書ジョブの添付ファイルの表示と追加](media/am-mobile-04.png "作業指示書ジョブの添付ファイルの表示と追加")</span><span class="sxs-lookup"><span data-stu-id="37af1-160">![View and add attachments for a work order job](media/am-mobile-04.png "View and add attachments for a work order job")</span></span>

## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="37af1-161">作業指示書ジョブのメンテナンス チェックリストの表示</span><span class="sxs-lookup"><span data-stu-id="37af1-161">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="37af1-162">モバイル デバイスで、**資産管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="37af1-162">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="37af1-163">すべての **メンテナンス作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-163">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="37af1-164">作業指示書、チェックリストを表示する作業指示書ジョブの順に選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-164">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="37af1-165">または、ホームページの **自分の作業指示書ジョブカレンダー** または **自分の作業指示書ジョブの一覧** を選択して、**作業指示書ジョブの詳細** ページに移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="37af1-165">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="37af1-166">**作業指示書ジョブの詳細** ページの **チェックリスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-166">Select **Checklists** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="37af1-167">作業指示書ジョブに関連するチェックリストの明細行の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="37af1-167">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="37af1-168">**手順** を表示したり、**メモ** を追加したりするには、チェックリストの明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-168">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

1. <span data-ttu-id="37af1-169">戻るボタン (**<**) を選択し、前のページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="37af1-169">Select the back button (**<**) to return to the previous page.</span></span>

    <span data-ttu-id="37af1-170">![管理チェックリストと明細行の詳細](media/am-mobile-05.png "管理チェックリストと明細行の詳細")</span><span class="sxs-lookup"><span data-stu-id="37af1-170">![Maintenance checklist and line details](media/am-mobile-05.png "Maintenance checklist and line details")</span></span>

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="37af1-171">作業指示書ジョブの資産カウンターの表示と更新</span><span class="sxs-lookup"><span data-stu-id="37af1-171">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="37af1-172">モバイル デバイスで、**資産管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="37af1-172">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="37af1-173">すべての **メンテナンス作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-173">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="37af1-174">作業指示書、資産カウンターを表示する作業指示書ジョブの順に選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-174">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="37af1-175">または、ホームページの **自分の作業指示書ジョブカレンダー** または **自分の作業指示書ジョブの一覧** を選択して、**作業指示書ジョブの詳細** ページに移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="37af1-175">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="37af1-176">**作業指示書ジョブの詳細** ページの **資産カウンター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-176">Select **Asset counters** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="37af1-177">作業指示書ジョブに関連する資産カウンターの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="37af1-177">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="37af1-178">資産カウンター明細行の鉛筆アイコンを選択して、カウンター値を更新します。</span><span class="sxs-lookup"><span data-stu-id="37af1-178">Select the pencil icon on an asset counter line to update the counter value.</span></span>

1. <span data-ttu-id="37af1-179">新しいカウンター値を入力し、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-179">Enter a new counter value, and select **Done**.</span></span>

    <span data-ttu-id="37af1-180">![資産カウンターの表示および更新](media/am-mobile-06.png "資産カウンターの表示および更新")</span><span class="sxs-lookup"><span data-stu-id="37af1-180">![View and update asset counters](media/am-mobile-06.png "View and update asset counters")</span></span>

## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="37af1-181">作業指示書ジョブに関する消費の登録</span><span class="sxs-lookup"><span data-stu-id="37af1-181">Register consumption on a work order job</span></span>

1. <span data-ttu-id="37af1-182">モバイル デバイスで、**資産管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="37af1-182">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="37af1-183">すべての **メンテナンス作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-183">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="37af1-184">作業指示書、消費登録を追加する作業指示書ジョブの順に選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-184">Select the work order > work order job you want to add consumption registrations for.</span></span>
    - <span data-ttu-id="37af1-185">または、ホームページの **自分の作業指示書ジョブカレンダー** または **自分の作業指示書ジョブの一覧** を選択して、**作業指示書ジョブの詳細** ページに移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="37af1-185">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="37af1-186">**作業指示書ジョブの詳細** ページの **仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-186">Select **Journals** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="37af1-187">**時間の追加** を選択して、作業時間の登録を作成します。</span><span class="sxs-lookup"><span data-stu-id="37af1-187">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="37af1-188">ルックアップから **カテゴリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-188">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="37af1-189">**時間** フィールドに、作業指示書ジョブに費やした作業時間数を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-189">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    1. <span data-ttu-id="37af1-190">該当する **明細行プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-190">Select the appropriate **Line property**.</span></span>
    1. <span data-ttu-id="37af1-191">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-191">Select **Done**.</span></span>

1. <span data-ttu-id="37af1-192">**品目の追加** を選択すると、品目の登録が作成されます。</span><span class="sxs-lookup"><span data-stu-id="37af1-192">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="37af1-193">ルックアップから **品目番号** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-193">Select the **Item number** from the lookup.</span></span>
    1. <span data-ttu-id="37af1-194">ルックアップから **サイト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-194">Select the **Site** from the lookup.</span></span>
    1. <span data-ttu-id="37af1-195">消費される品目の **数量** を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-195">Enter the **Quantity** of items consumed.</span></span>
    1. <span data-ttu-id="37af1-196">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-196">Select **Done**.</span></span>

1. <span data-ttu-id="37af1-197">**経費の追加** を選択して、経費の登録を作成します。</span><span class="sxs-lookup"><span data-stu-id="37af1-197">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="37af1-198">ルックアップから **カテゴリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-198">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="37af1-199">経費の登録の数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-199">Enter the quantity for the expense registration.</span></span>
    1. <span data-ttu-id="37af1-200">ルックアップから **販売通貨** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-200">Select the **Sales currency** from the lookup.</span></span>
    1. <span data-ttu-id="37af1-201">経費の登録の **原価価格** を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-201">Enter the **Cost price** for the expense registration.</span></span>
    1. <span data-ttu-id="37af1-202">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-202">Select **Done**.</span></span>

    <span data-ttu-id="37af1-203">![作業指示書の仕訳帳の更新](media/am-mobile-07.png "作業指示書の仕訳帳の更新")</span><span class="sxs-lookup"><span data-stu-id="37af1-203">![Update a work order journal](media/am-mobile-07.png "Update a work order journal")</span></span>

## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="37af1-204">作業指示書のライフサイクルの状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="37af1-204">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="37af1-205">モバイル デバイスで、**資産管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="37af1-205">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="37af1-206">すべての **メンテナンス作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-206">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="37af1-207">ライフサイクルの状態を更新する作業指示書を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-207">Select the work order you want to update lifecycle state for.</span></span>

1. <span data-ttu-id="37af1-208">画面の下部にある **状態の更新** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="37af1-208">Select the **Update state** button at the bottom of the screen.</span></span>

1. <span data-ttu-id="37af1-209">一覧から新しいライフサイクルの状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-209">Select a new lifecycle state from the list.</span></span>

1. <span data-ttu-id="37af1-210">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-210">Select **Done**.</span></span>

    <span data-ttu-id="37af1-211">![作業指示書のライフサイクルの状態を更新します。](media/am-mobile-08.png "作業指示書のライフサイクルの状態を更新します。")</span><span class="sxs-lookup"><span data-stu-id="37af1-211">![Update lifecycle state on a work order](media/am-mobile-08.png "Update lifecycle state on a work order")</span></span>

## <a name="create-a-maintenance-request"></a><span data-ttu-id="37af1-212">メンテナンス要求の作成</span><span class="sxs-lookup"><span data-stu-id="37af1-212">Create a maintenance request</span></span>

1. <span data-ttu-id="37af1-213">モバイル デバイスで、**資産管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="37af1-213">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="37af1-214">**すべてのメンテナンス要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-214">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="37af1-215">画面の下部にある **アクション** を選択し、**メンテナンス要求の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-215">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

1. <span data-ttu-id="37af1-216">**資産管理** のメンテナンス要求で番号順序が有効になっている場合、**メンテナンス要求** フィールドは自動的に入力されるため非表示になっています。**メンテナンス要求** フィールドが表示されている場合は、メンテナンス要求 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-216">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

1. <span data-ttu-id="37af1-217">**メンテナンス要求タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-217">Select a **Maintenance request type**.</span></span>

1. <span data-ttu-id="37af1-218">メンテナンス要求の **説明** を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-218">Enter a **Description** for the maintenance request.</span></span>

1. <span data-ttu-id="37af1-219">要求を作成する **資産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-219">Select the **Asset** you want to create the request for.</span></span>

1. <span data-ttu-id="37af1-220">メンテナンス要求の **サービスレベル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-220">Select the **Service level** for the maintenance request.</span></span>

1. <span data-ttu-id="37af1-221">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-221">Select **Done**.</span></span>

    <span data-ttu-id="37af1-222">![メンテナンス要求の作成](media/am-mobile-09.png "メンテナンス要求の作成")</span><span class="sxs-lookup"><span data-stu-id="37af1-222">![Create a maintenance request](media/am-mobile-09.png "Create a maintenance request")</span></span>

## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="37af1-223">メンテナンス要求に添付ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="37af1-223">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="37af1-224">モバイル デバイスで、**資産管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="37af1-224">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="37af1-225">**すべてのメンテナンス要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-225">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="37af1-226">添付ファイルを追加するメンテナンス要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-226">Select the maintenance request you want to add an attachment to.</span></span>

1. <span data-ttu-id="37af1-227">画面の下部にある **添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-227">Select **Attachments** at the bottom of the screen.</span></span>

1. <span data-ttu-id="37af1-228">**添付ファイルの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-228">Select **Add attachments**.</span></span>

1. <span data-ttu-id="37af1-229">添付ファイルの **名前** と **メモ** を入力します。</span><span class="sxs-lookup"><span data-stu-id="37af1-229">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="37af1-230">**画像の選択** を選択して、モバイル ギャラリーから写真を選択するか、**写真を撮る** を選択して写真を撮影します。</span><span class="sxs-lookup"><span data-stu-id="37af1-230">Select **Choose image** to select a photo from the mobile gallery or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="37af1-231">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37af1-231">Select **Done**.</span></span>

    <span data-ttu-id="37af1-232">![メンテナンス要求への添付ファイルの追加](media/am-mobile-10.png "メンテナンス要求への添付ファイルの追加")</span><span class="sxs-lookup"><span data-stu-id="37af1-232">![Add an attachment to a maintenance request](media/am-mobile-10.png "Add an attachment to a maintenance request")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]