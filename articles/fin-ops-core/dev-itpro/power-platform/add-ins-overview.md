---
title: アドインの概要
description: このトピックでは、Finance and Operations アプリの機能を拡張するために使用できるアドインに関する情報を提供します。
author: ankugo
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: ankugo
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 52dcf72609d29d62c3e044277b637526ead88039
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909018"
---
# <a name="add-ins-overview"></a><span data-ttu-id="ab9d0-103">アドインの概要</span><span class="sxs-lookup"><span data-stu-id="ab9d0-103">Add-ins overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ab9d0-104">アドインを使用すると、Finance and Operations アプリの機能を拡張できます。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-104">Add-ins provide a way to extend the functionality of Finance and Operations apps.</span></span> <span data-ttu-id="ab9d0-105">次のトピックでは、アドインの例を示します:</span><span class="sxs-lookup"><span data-stu-id="ab9d0-105">The following topics provide some examples of add-ins:</span></span>

- [<span data-ttu-id="ab9d0-106">計画最適化の概要</span><span class="sxs-lookup"><span data-stu-id="ab9d0-106">Planning Optimization overview</span></span>](../../../supply-chain/master-planning/planning-optimization/planning-optimization-overview.md)
- [<span data-ttu-id="ab9d0-107">在庫の視覚化アドイン</span><span class="sxs-lookup"><span data-stu-id="ab9d0-107">Inventory Visibility Add-in</span></span>](../../../supply-chain/inventory/inventory-visibility.md)
- [<span data-ttu-id="ab9d0-108">Azure Data Lake へのエクスポートのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ab9d0-108">Configure export to Azure Data Lake</span></span>](../data-entities/configure-export-data-lake.md)
- [<span data-ttu-id="ab9d0-109">IoT インテリジェンスのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="ab9d0-109">IoT Intelligence home page</span></span>](../../../supply-chain/iot/iot-intelligence-home-page.md)

## <a name="prerequisites-for-setting-up-add-ins"></a><span data-ttu-id="ab9d0-110">アドインを設定するための前提条件</span><span class="sxs-lookup"><span data-stu-id="ab9d0-110">Prerequisites for setting up add-ins</span></span>

- <span data-ttu-id="ab9d0-111">Microsoft Dataverse 領域の少なくとも 1 ギガバイト (GB) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-111">Make sure that at least 1 gigabyte (GB) of Microsoft Dataverse space is available.</span></span> <span data-ttu-id="ab9d0-112">それ以外の場合、設定は失敗です。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-112">Otherwise, setup will fail.</span></span> <span data-ttu-id="ab9d0-113">[Power Platform管理センター](https://admin.powerplatform.microsoft.com/resources/capacity) にて、容量を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-113">You can view your capacity in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/resources/capacity).</span></span> 
- <span data-ttu-id="ab9d0-114">Finance and Operations 環境管理者を識別します。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-114">Identify your Finance and Operations environment administrator.</span></span> <span data-ttu-id="ab9d0-115">**環境の詳細** セクションにて、情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-115">You can find that information in the **Environment details** section.</span></span>

    ![環境の詳細タブ](media/EnvironmentDetails.png)
    
- <span data-ttu-id="ab9d0-117">Power Platform 環境ガバナンス ポリシーを検証します。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-117">Validate your Power Platform environment governance policy.</span></span> <span data-ttu-id="ab9d0-118">検証するには、**グローバル管理者** または **Power Platform 管理者** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-118">To validate, you must be a **Global administrator** or **Power Platform administrator**.</span></span>
    
    1. <span data-ttu-id="ab9d0-119">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com) にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-119">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>
    2. <span data-ttu-id="ab9d0-120">Power Platform サイトの右上端にあるギア アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-120">Select the gear icon in the upper-right corner of the Power Platform site.</span></span>
    
        ![Power Platform の設定](media/PowerPlatformSettings.png)
    
- <span data-ttu-id="ab9d0-122">組織では、運用環境に対して **全ユーザー** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-122">Organizations must select **Everyone** for production environments.</span></span>
    
    <span data-ttu-id="ab9d0-123">Finance and Operations 環境管理者は、次のいずれかのロールに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-123">The Finance and Operations environment administrator must be added to one of the following roles.</span></span> <span data-ttu-id="ab9d0-124">このアクションを実行するには、グローバル管理者が必要です。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-124">You will need a Global Administrator to perform this action.</span></span>
    - <span data-ttu-id="ab9d0-125">Global 管理者</span><span class="sxs-lookup"><span data-stu-id="ab9d0-125">Global admins</span></span>
    - <span data-ttu-id="ab9d0-126">Dynamics 365 管理者</span><span class="sxs-lookup"><span data-stu-id="ab9d0-126">Dynamics 365 admins</span></span>
    - <span data-ttu-id="ab9d0-127">Power Platform 管理者</span><span class="sxs-lookup"><span data-stu-id="ab9d0-127">Power Platform admins</span></span>
    
    <span data-ttu-id="ab9d0-128">詳細については、[サービス管理者ロールを使用したテナントの管理](/power-platform/admin/use-service-admin-role-manage-tenant) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-128">For more information, see [Use service admin roles to manage your tenant](/power-platform/admin/use-service-admin-role-manage-tenant).</span></span>

## <a name="set-up-add-ins"></a><span data-ttu-id="ab9d0-129">アドインの設定</span><span class="sxs-lookup"><span data-stu-id="ab9d0-129">Set up add-ins</span></span>

> [!NOTE]
> <span data-ttu-id="ab9d0-130">インストールを計画しているアドインに「デュアル書き込みリンク」が必要ない場合は、この手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-130">If the add-ins that you're planning to install don't require "dual-write linking," you don't have to complete this procedure.</span></span>

1. <span data-ttu-id="ab9d0-131">Finance and Operations 環境が LCS を通じて展開された後、LCS の **環境詳細** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-131">After the Finance and Operations environment has been deployed through LCS, open the **Environment details** page in LCS.</span></span>
2. <span data-ttu-id="ab9d0-132">**Power Platform 統合** セクションで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-132">In the **Power Platform integration** section, select **Setup**.</span></span>
3. <span data-ttu-id="ab9d0-133">**Power Platform環境の設定** ダイアログ ボックスでチェック ボックスをオンにし、ダイアログ ボックスの下部にある **設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-133">In the **Power platform environment setup** dialog box, select the check box, and then select **Setup** at the bottom of the dialog box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ab9d0-134">Dataverse 環境は、デュアル書き込み機能を含む方法で設定されています。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-134">The Dataverse environment is set up so that it includes dual-write functionality.</span></span> <span data-ttu-id="ab9d0-135">通常この設定で消費される容量は、Dataverse 領域の 約 1 GB です。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-135">Typically, this setup consumes about 1 GB of Dataverse space.</span></span>

4. <span data-ttu-id="ab9d0-136">Microsoft Power Platform 環境が準備されているというメッセージが表示された場合は、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-136">When you receive a message that states that the Microsoft Power Platform environment is being provisioned, select **OK**.</span></span>

    <span data-ttu-id="ab9d0-137">**環境詳細** ページの **Power Platform 統合** セクションに、Microsoft Power Platform 環境が準備されているというメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-137">The **Power Platform integration** section of the **Environment details** page now shows a message that states that the Microsoft Power Platform environment is being provisioned.</span></span>

5. <span data-ttu-id="ab9d0-138">数分後、**環境の詳細** ページが更新されます。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-138">After a few minutes, refresh the **Environment details** page.</span></span>
6. <span data-ttu-id="ab9d0-139">**Power Platform 統合** セクションにおいて、**ステータス** フィールドの値が **環境設定が進行中** であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-139">In the **Power Platform integration** section, notice that the value of the **Status** field is **Environment setup is in progress**.</span></span>

    <span data-ttu-id="ab9d0-140">通常、設定は 60分 から 90分かかります。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-140">Typically, the setup takes between 60 and 90 minutes.</span></span>

    <span data-ttu-id="ab9d0-141">Dataverse 環境が準備された後、**新しいアドインのインストール** ボタンが **Power Platform 統合** セクションで利用できます。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-141">After the Dataverse environment is provisioned, the **Install a new add-in** button becomes available in the **Power Platform integration** section.</span></span>

    ![新しいアドイン ボタンのインストール](media/InstallANewAddIn.png)

## <a name="troubleshoot-the-setup"></a><span data-ttu-id="ab9d0-143">設定のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ab9d0-143">Troubleshoot the setup</span></span>

- <span data-ttu-id="ab9d0-144">次の図に示すように、セットアップ プロセスによってデュアル書き込み機能の設定が試行される場合、Dataverse 環境の準備後にデュアル書き込み設定が失敗することがあります 。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-144">Because the setup process tries to set up dual-write functionality, the dual-write setup might sometimes fail after the Dataverse environment is provisioned, as shown in the following illustration.</span></span> <span data-ttu-id="ab9d0-145">このような場合は、**新しいアドインのインストール** ボタンを使用して、アドインのインストールのブロックを解除できます。デュアル書き込み機能を継続して設定する場合は、**経歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-145">In these cases, the **Install a new add-in** button is still available, so that you can unblock the installation of add-ins. If you want to continue to set up dual-write functionality, select **Resume**.</span></span>

    ![デュアル書き込みの失敗](media/Error.png)

- <span data-ttu-id="ab9d0-147">能力やライセンスに関する問題が発生すると、Dataverse 環境の準備に失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-147">Provisioning of the Dataverse environment might sometimes fail because of capacity and licensing issues.</span></span> <span data-ttu-id="ab9d0-148">そのような場合は、Power Platform 管理センターにログインして問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-148">In these cases, sign in to the Power Platform admin center, and fix the issues.</span></span> <span data-ttu-id="ab9d0-149">次に LCS の **環境詳細** ページの **Power Platform 統合** セクションで、**経歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d0-149">Then, in the **Power Platform integration** section of the **Environment details** page in LCS, select **Resume**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]