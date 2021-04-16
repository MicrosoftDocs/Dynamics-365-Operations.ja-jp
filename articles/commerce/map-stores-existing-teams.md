---
title: Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします
description: ここでは、Commerce の統合前に Microsoft Teams でチームを作成していた場合に、Dynamics 365 Commerce 本部の店舗と対応するチームをマッピングする方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3edd176788b24a5f5246e9b7bcb3c6fbcdca2254
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842697"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="ed04b-103">Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします</span><span class="sxs-lookup"><span data-stu-id="ed04b-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ed04b-104">ここでは、Commerce の統合前に Microsoft Teams でチームを作成していた場合に、Dynamics 365 Commerce 本部の店舗と対応するチームをマッピングする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="ed04b-105">組織では、Dynamics 365 Commerce と Microsoft Teams を統合する前に、一部またはすべてのストアにチームが作成されている場合もあるでしょう。</span><span class="sxs-lookup"><span data-stu-id="ed04b-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="ed04b-106">この場合、Commerce POSと Microsoft Teams の間でタスクの同期を確立するには、Commerce 本部で店舗と対応するチームのマッピングをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed04b-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="ed04b-107">Commerce 本部の店舗と対応するチームをマッピングする</span><span class="sxs-lookup"><span data-stu-id="ed04b-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="ed04b-108">Commerce 本部で店舗と対応するチームをマッピングするには、以下の手順で行います。</span><span class="sxs-lookup"><span data-stu-id="ed04b-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ed04b-109">**システム管理 \> ワークスペース \> データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="ed04b-110">**エクスポート** の選択</span><span class="sxs-lookup"><span data-stu-id="ed04b-110">Select **Export**.</span></span> 
1. <span data-ttu-id="ed04b-111">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ed04b-112">**グループ名** で、「Teams マッピングのエクスポート」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="ed04b-113">**選択したエンティティ** クイックタブで、 **エンティティの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="ed04b-114">**エンティティの追加** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ed04b-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="ed04b-115">**エンティティ名** ボックスの一覧で、**ソースとチームの間の Teams マッピング** を選択します 。</span><span class="sxs-lookup"><span data-stu-id="ed04b-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="ed04b-116">**ターゲットのデータ形式** ドロップダウン リスト一覧で、**CSV** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="ed04b-117">**追加** を選択してから **閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="ed04b-118">アクション ウィンドウの下の左上で、**今すぐエクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="ed04b-119">**エンティティ 処理ステータス** で、**ファイルのダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="ed04b-120">エクスポートされた CSV ファイルで、 **SOURCETYPE**、**SOURCEID**、**TEAMID** の値を次のように入力します :</span><span class="sxs-lookup"><span data-stu-id="ed04b-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="ed04b-121">**SOURCETYPE** には、「RetailStore」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="ed04b-122">**SOURCEID** には、店舗番号を入力します (サンフランシスコ店舗の場合は  "000135" など)。</span><span class="sxs-lookup"><span data-stu-id="ed04b-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="ed04b-123">店舗番号は、**Retail と Commerce \> Channels \> Stores** で検索できます。</span><span class="sxs-lookup"><span data-stu-id="ed04b-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="ed04b-124">**TEAMID** には、Microsoft Teams から該当するチーム ID を入力してください (例 : "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c")。</span><span class="sxs-lookup"><span data-stu-id="ed04b-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="ed04b-125">チーム ID の情報は、[admin.teams.microsoft.com](https://admin.teams.microsoft.com) で確認できます。</span><span class="sxs-lookup"><span data-stu-id="ed04b-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="ed04b-126">CSV ファイルをローカル コンピューターに保存します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="ed04b-127">**システム管理 \> ワークスペース \> データ管理** にアクセスし、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="ed04b-128">**選択したエンティティ** クイックタブで、 **ファイルの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="ed04b-129">**ファイルの追加** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ed04b-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="ed04b-130">**エンティティ名** ボックスの一覧で、**ソースとチームの間の Teams マッピング** を選択します 。</span><span class="sxs-lookup"><span data-stu-id="ed04b-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="ed04b-131">**ソース データの形式** ドロップダウン リスト一覧で、**CSV** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="ed04b-132">**アップロードして追加** を選択し、前に保存した CSV ファイルを選択して、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="ed04b-133">**追加 ダイアログ** ボックスで、**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="ed04b-134">アクション ペインで、**保存** を選択し、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="ed04b-135">次のイメージ例では、Commerce の **チームのマッピングのエクスポート** グループで、**エンティティの追加** 要素とエクスポートされた CSV ファイルのヘッダーが強調表示されています。</span><span class="sxs-lookup"><span data-stu-id="ed04b-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Commerce の チームのマッピングのエクスポート グループで、エンティティの追加 要素とエクスポートされた CSV ファイルのヘッダーが強調表示されています](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="ed04b-137">上記手順の完了後は、[Microsoft Teams と POS 間のタスク管理を同期する](synchronize-tasks-teams-pos.md) に記載の手順に従い、タスク管理を同期します。</span><span class="sxs-lookup"><span data-stu-id="ed04b-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="ed04b-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ed04b-138">Additional resources</span></span>

[<span data-ttu-id="ed04b-139">Dynamics 365 Commerce と Microsoft Teams データ統合の概要</span><span class="sxs-lookup"><span data-stu-id="ed04b-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ed04b-140">Dynamics 365 Commerce と Microsoft Teams の統合を有効化する</span><span class="sxs-lookup"><span data-stu-id="ed04b-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="ed04b-141">Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="ed04b-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ed04b-142">Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる</span><span class="sxs-lookup"><span data-stu-id="ed04b-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="ed04b-143">Microsoft Teams でユーザーとロールを管理する</span><span class="sxs-lookup"><span data-stu-id="ed04b-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ed04b-144">Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="ed04b-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
