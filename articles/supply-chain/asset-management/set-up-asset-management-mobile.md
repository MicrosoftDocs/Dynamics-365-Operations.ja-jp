---
title: 資産管理モバイル ワークスペースの設定
description: このトピックでは、作業者が資産管理タスクを実行するために使用できる資産管理モバイル ワークスペースを実行するための Microsoft Dynamics 365 Supply Chain Management と Finance and Operations (Dynamics 365) モバイル アプリの設定方法について説明します。
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837780"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="5b39e-103">資産管理モバイル ワークスペースの設定</span><span class="sxs-lookup"><span data-stu-id="5b39e-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b39e-104">このトピックでは、作業者が資産管理タスクを実行するために使用できる **資産管理** モバイル ワークスペースを実行するための Microsoft Dynamics 365 Supply Chain Management と Finance and Operations (Dynamics 365) モバイル アプリの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="5b39e-105">Supply Chain Management でのメンテナンス作業者ユーザーの設定</span><span class="sxs-lookup"><span data-stu-id="5b39e-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="5b39e-106">**資産管理** モバイル ワークスペースへのアクセスを必要とする 各ユーザーについて、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5b39e-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="5b39e-107">Supply Chain Management で、**人事管理 \>ワーカー** に移動し、設定するユーザーのワーカー レコードが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="5b39e-108">必要に応じて作業者レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="5b39e-109">**資産管理 \> 設定 \> 作業者 \> 作業者** に移動し、前の手順で特定した (または作成された) 作業者レコードがメンテナンス作業者レコードにマップ されている事を確認します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="5b39e-110">必要に応じて新しいメンテナンス作業者レコードを作成し、前の手順から作業者レコードに **作業者** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="5b39e-111">**資産管理 \> 設定 \> 作業者 \> メンテナンス作業者グループ** に移動し、前の手順で特定した (または作成された) メンテナンス作業者レコードがメンテナンス作業者グループに属していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="5b39e-112">**システム管理 \> ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="5b39e-113">グリッドで関連ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="5b39e-114">**ユーザーの詳細** クイック タブで、現在のユーザー アカウントに関連付ける作業者アカウントに **個人** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="5b39e-115">この作業者アカウントは、手順 1 で特定した (または作成された) 作業者レコードで、手順2. でメンテナンス作業者レコードにマップされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b39e-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="5b39e-116">ユーザーのアクセス許可とセキュリティ ロールは、Supply Chain Management のユーザー インターフェイスの機能と同様に、**資産管理** モバイル ワークスペースの機能に適用されます。</span><span class="sxs-lookup"><span data-stu-id="5b39e-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="5b39e-117">したがって、**資産管理** モバイル ワークスペースにアクセスするために設定したすべてのユーザーには、Supply Chain Management で同様の操作を直接実行するために必要なセキュリティ ロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="5b39e-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="5b39e-118">資産管理モバイル ワークスペースの公開</span><span class="sxs-lookup"><span data-stu-id="5b39e-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="5b39e-119">Finance and Operations (Dynamics 365) モバイル アプリで資産管理機能を使用するには、**資産管理** モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b39e-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="5b39e-120">Supply Chain Management で、**設定** ボタン (右上隅のギア記号) を選択し、メニューの **モバイル アプリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="5b39e-121">**モバイル アプリの管理** ダイアログ ボックスで、**資産管理** タイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="5b39e-122">"メタデータ内 - 未公開" というテキストが含まれている場合、ワークスペースはまだ公開されていません。</span><span class="sxs-lookup"><span data-stu-id="5b39e-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="5b39e-123">"メタデータ内 - 公開済" という文字列が含まれている場合、ワークスペースは既に発行済みで、この手順の残りを省略できます。</span><span class="sxs-lookup"><span data-stu-id="5b39e-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="5b39e-124">![モバイル アプリの管理ダイアログ ボックス](media/mobile-workspaces.png "モバイル アプリの管理ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="5b39e-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="5b39e-125">**資産管理** タイルを選択し、ツール バーの **発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b39e-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="5b39e-126">しばらくすると、ワークスペースが正常に発行されたことを示す通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b39e-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="5b39e-127">また、タイル上のテキストは "メタデータ内 - 公開済" に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b39e-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="5b39e-128">Finance and Operations (Dynamics 365) モバイル アプリのインストールと設定</span><span class="sxs-lookup"><span data-stu-id="5b39e-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="5b39e-129">次のいずれかのアプリケーション店舗に移動して **Microsoft Finance and Operations (Dynamics 365)** アプリをモバイル デバイスにインストールします。</span><span class="sxs-lookup"><span data-stu-id="5b39e-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="5b39e-130">Google Android デバイスの場合</span><span class="sxs-lookup"><span data-stu-id="5b39e-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="5b39e-131">Apple iOS デバイスの場合</span><span class="sxs-lookup"><span data-stu-id="5b39e-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="5b39e-132">Finance and Operations (Dynamics 365) アプリを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b39e-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="5b39e-133">サインイン ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b39e-133">The sign-in page should appear.</span></span> <span data-ttu-id="5b39e-134">**サインイン** フィールドに Supply Chain Management の URL を入力するか、**最新の環境** ボックスの一覧で最近の URL を選択して、**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b39e-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="5b39e-135">![サインイン ページ](media/mobile-app-sign-in.png "サインイン ページ")</span><span class="sxs-lookup"><span data-stu-id="5b39e-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="5b39e-136">接続を確認するメッセージが表示された場合は、**了解します** チェック ボックスをオンにし、**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b39e-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="5b39e-137">**アカウントのピック** ページで、Microsoft アカウントを使用してモバイル アプリケーションにサインインします。</span><span class="sxs-lookup"><span data-stu-id="5b39e-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="5b39e-138">**ワークスペース** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b39e-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="5b39e-139">これには、Supply Chain Management インスタンスによって公開されたすべてのモバイル ワークスペースが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b39e-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="5b39e-140">![ワークスペースのリスト](media/mobile-app-workspaces.png "ワークスペースのリスト")</span><span class="sxs-lookup"><span data-stu-id="5b39e-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="5b39e-141">法人 (会社) を変更する必要がある場合は、左上の角のメニュー ボタン (ハンバーガーまたはハンバーガー ボタンと呼ばれることもあります) をタップして、**会社の変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b39e-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="5b39e-142">![法人の変更](media/mobile-app-change-comp.png "法人の変更")</span><span class="sxs-lookup"><span data-stu-id="5b39e-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="5b39e-143">**ワークスペース** ページで、使用するワークスペースを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="5b39e-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="5b39e-144">![資産管理モバイル ワークスペース](media/mobile-app-asset-workspace.png "資産管理モバイル ワークスペース")</span><span class="sxs-lookup"><span data-stu-id="5b39e-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="5b39e-145">資産管理モバイル ワークスペースを使って作業する</span><span class="sxs-lookup"><span data-stu-id="5b39e-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="5b39e-146">**資産管理** モバイル ワークスペースの使用方法の詳細については、[資産管理モバイル ワークスペースの使用](asset-management-mobile-workspace.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b39e-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="5b39e-147">Finance and Operations (Dynamics 365) モバイル アプリの詳細については、[モバイル アプリのホーム ページ](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b39e-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]