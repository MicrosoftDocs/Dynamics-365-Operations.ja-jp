---
title: PowerBI.comからの分析ワークスペースの選択
description: このトピックでは、PowerBI.comでホストされているレポートを選択してアプリケーション ワークスペースで使用する方法について説明します。
author: tjvass
manager: AnnBe
ms.date: 07/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Platform update 26
ms.openlocfilehash: 49f3d858c648fcbe222cf77bb79e8b639d88e057
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183447"
---
# <a name="select-analytical-workspaces-from-powerbicom"></a><span data-ttu-id="423fb-103">PowerBI.comからの分析ワークスペースの選択</span><span class="sxs-lookup"><span data-stu-id="423fb-103">Select analytical workspaces from PowerBI.com</span></span>

[!include[banner](../includes/banner.md)]

## <a name="analytical-workspaces"></a><span data-ttu-id="423fb-104">分析ワークスペース</span><span class="sxs-lookup"><span data-stu-id="423fb-104">Analytical workspaces</span></span>

<span data-ttu-id="423fb-105">アプリケーション スイートにバンドルされている分析ワークスペースは、ユーザーにビジネス データに関する適切な洞察を提供します。</span><span class="sxs-lookup"><span data-stu-id="423fb-105">The analytical workspaces that are bundled with the application suite offer users relevant insights into their business data.</span></span> <span data-ttu-id="423fb-106">ただし、場合によっては、標準レポートを組織のユーザー専用に設計されたカスタムレポートに置き換えることが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="423fb-106">However, in some cases, it might make sense to replace standard reports with custom reports that are designed specifically for the users in your organization.</span></span>

<span data-ttu-id="423fb-107">PowerBI.comが提供するワールドクラスのツールを使用すると、外部ソースからのデータを使用するマッシュアップ ビューを含む分析レポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="423fb-107">The world-class tooling that PowerBI.com provides lets you produce analytical reports that contain mashup views that use data from external sources.</span></span> <span data-ttu-id="423fb-108">Finance and Operations のプラットフォーム更新プログラム 26 では、パワー ユーザーは標準埋め込みレポートを PowerBI.com でホストされているレポートと置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="423fb-108">In Platform update 26 for Finance and Operations, power users can replace the standard embedded reports with those that are hosted on PowerBI.com.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="423fb-109">このトピックで説明する機能は、個人用設定ではありません。</span><span class="sxs-lookup"><span data-stu-id="423fb-109">The functionality that this topic describes isn't a personalization.</span></span> <span data-ttu-id="423fb-110">分析ワークスペースのカスタマイズは、有効な法人のすべてのユーザーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="423fb-110">The customization of analytical workspaces applies to all users in the active legal entity.</span></span>

### <a name="motivations-for-embedding-powerbicom-reports"></a><span data-ttu-id="423fb-111">PowerBI.comレポートの埋め込みの動機</span><span class="sxs-lookup"><span data-stu-id="423fb-111">Motivations for embedding PowerBI.com reports</span></span>

<span data-ttu-id="423fb-112">標準レポートは、特定のビジネスペルソナ向けにカスタマイズされた情報を提供しますが、場合によっては組織でカスタムレポートを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="423fb-112">Although standard reports deliver insights that are tailored for a given business persona, an organization might prefer a custom report in some cases.</span></span> <span data-ttu-id="423fb-113">アプリケーションにより、パワー ユーザーは PowerBI.com でホストされまた組織のメンバーと共有できるカスタムレポートを奨励することができます。</span><span class="sxs-lookup"><span data-stu-id="423fb-113">The application lets power users promote custom reports that are hosted on PowerBI.com and shared with members of the organization.</span></span>

<span data-ttu-id="423fb-114">ここでは、PowerBI.comでホストされているレポートを選択する場合の主な動機をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="423fb-114">Here are some of the top motivations for selecting reports that are hosted on PowerBI.com:</span></span>

- <span data-ttu-id="423fb-115">PowerBI.com レポートは、外部データソースを使用し、アプリケーション外部からアクセスできるデータ マッシュ アップをサポートします。</span><span class="sxs-lookup"><span data-stu-id="423fb-115">PowerBI.com reports support data mashups that use external data sources and can be accessed outside the application.</span></span>
- <span data-ttu-id="423fb-116">レポートは、PowerBI.comでホストされ、ワン ボックス配置でアプリケーションに埋め込まれるカスタム ソリューションのデモンストレーションに適しています。</span><span class="sxs-lookup"><span data-stu-id="423fb-116">The reports are appropriate for demonstrating custom solutions that are hosted on PowerBI.com and embedded in the application in one-box deployments.</span></span>
- <span data-ttu-id="423fb-117">Microsoft Power BIプレミアムサービスを使用している組織では、標準レポートを強化したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="423fb-117">Organizations that have Microsoft Power BI Premium services want to augment the standard reports.</span></span>

### <a name="embed-a-powerbicom-report-in-an-analytical-workspace"></a><span data-ttu-id="423fb-118">分析ワークスペースへのPowerBI.comレポートの埋め込み</span><span class="sxs-lookup"><span data-stu-id="423fb-118">Embed a PowerBI.com report in an analytical workspace</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3lP5m]

<span data-ttu-id="423fb-119">[PowerBI.com レポートを埋め込む方法](https://www.youtube.com/watch?v=gGWuNJDoi-M&feature=youtu.be) ビデオ (上記参照) は、YouTube の [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="423fb-119">The [How to embed PowerBI.com reports](https://www.youtube.com/watch?v=gGWuNJDoi-M&feature=youtu.be) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="423fb-120">標準レポートを置き換えるには、システム レポート エディター セキュリティ グループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="423fb-120">To replace the standard reports, you must be a member of the System Report Editors security group.</span></span> <span data-ttu-id="423fb-121">このセキュリティ グループ メンバーは、標準レポートをカスタマイズするためのアプリケーション ワークスペースのオプションにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="423fb-121">Members of this security group can access the options in application workspaces that let them customize the standard reports.</span></span> <span data-ttu-id="423fb-122">次の例は、標準分析レポートを、PowerBI.comでホストされているカスタム レポートに置き換える方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="423fb-122">This example shows how to replace the standard analytical report with a customized report that is hosted on PowerBI.com.</span></span>

1. <span data-ttu-id="423fb-123">サインインし、カスタマイズするアプリケーションのレポートを開きます。</span><span class="sxs-lookup"><span data-stu-id="423fb-123">Sign in and open the application report that you want to customize.</span></span> <span data-ttu-id="423fb-124">この例では、 **報酬管理** ワークスペースに埋め込まれている標準分析レポートを置換します。</span><span class="sxs-lookup"><span data-stu-id="423fb-124">In this example, you will replace the standard analytical report that is embedded in the **Compensation management** workspace.</span></span>

    ![報酬管理ワークスペース](media/compensation-management-workspace.png)

2. <span data-ttu-id="423fb-126">**分析** タブを選択すると、ワークスペースの埋め込み分析レポートにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="423fb-126">Select the **Analytics** tab to access the workspace's embedded analytical report.</span></span>

    ![報酬管理分析ワークスペースの [分析] タブ](media/compensation-management-analytics.png)

    <span data-ttu-id="423fb-128">デフォルトでは、アプリケーションと共に含まれる標準分析ワークスペース ソリューションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="423fb-128">By default, you will see the standard analytical workspace solution that is included with your application.</span></span> <span data-ttu-id="423fb-129">このソリューションのレポートは、プロビジョニング プロセス中に環境に合わせて自動的に配置および設定されます。</span><span class="sxs-lookup"><span data-stu-id="423fb-129">The reports in this solution are automatically deployed and configured for your environment during the provisioning process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="423fb-130">分析ワークスペースには、専用の環境に対してのみ使用できるホストされた Power BI サービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="423fb-130">The analytical workspaces require a hosted Power BI service that is available only for dedicated environments.</span></span> <span data-ttu-id="423fb-131">詳細については、ブログ投稿 [1-Box 環境での分析ワークスペースおよびレポートへのアクセス](https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="423fb-131">For more information, see the blog post, [Accessing Analytical Workspaces and Reports on 1-Box Environments](https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/).</span></span>

3. <span data-ttu-id="423fb-132">アクション ペインの **オプション** タブの **Power BI** グループで、 **分析の選択** を選択して **Power BIレポート** ダイアログボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="423fb-132">On the Action Pane, on the **Options** tab, in the **Power BI** group, select **Select Analytics** to open the **Power BI Reports** dialog box.</span></span>

    ![Power BIレポート ダイアログ ボックス](media/select-powerbi-report-analytics.png)

    <span data-ttu-id="423fb-134">このダイアログボックスでは、PowerBI.comサービスで共有されているレポートの中から選択することができます。</span><span class="sxs-lookup"><span data-stu-id="423fb-134">This dialog box lets you select among the reports that have been shared on the PowerBI.com service.</span></span> <span data-ttu-id="423fb-135">レポートはワークスペース毎に編成されています。</span><span class="sxs-lookup"><span data-stu-id="423fb-135">The reports are organized by workspace.</span></span>

4. <span data-ttu-id="423fb-136">ドロップダウン リストで、レポートを含むワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="423fb-136">In the drop-down list, select the workspace that contains the report.</span></span>
5. <span data-ttu-id="423fb-137">アプリケーション ワークスペースに埋め込むレポートを選択し、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="423fb-137">Select the report to embed in the application workspace, and then select **OK**.</span></span>
6. <span data-ttu-id="423fb-138">ワークスペースの更新を表示するには、ページを再度読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="423fb-138">To view the updates to the workspace, you must reload the page.</span></span> <span data-ttu-id="423fb-139">ワークスペースから移動して戻ってくるか、ブラウザーを更新します。</span><span class="sxs-lookup"><span data-stu-id="423fb-139">Either move away from the workspace and then return, or refresh your browser.</span></span>
7. <span data-ttu-id="423fb-140">**報酬管理** ワークスペースで、 **分析** タブを選択し、分析ワークスペースに埋め込まれた PowerBI.com レポートにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="423fb-140">In the **Compensation management** workspace, select the **Analytics** tab to access the PowerBI.com report that is now embedded in the analytical workspace.</span></span>

    ![カスタム分析ワークスペース](media/custom-powerbi-report-analytics.png)

### <a name="revert-to-the-standard-solution"></a><span data-ttu-id="423fb-142">標準ソリューションに戻す</span><span class="sxs-lookup"><span data-stu-id="423fb-142">Revert to the standard solution</span></span>

<span data-ttu-id="423fb-143">PowerBI.com レポートをアプリケーション ワークスペースに埋め込んだ後、そのレポートに対する更新はユーザー向けにすぐに反映されます。</span><span class="sxs-lookup"><span data-stu-id="423fb-143">After a PowerBI.com report has been embedded in an application workspace, updates to the report are reflected immediately for users.</span></span> <span data-ttu-id="423fb-144">ただし、レポートを別の PowerBI.com ソリューションに置き換えるには、まず、標準のアプリケーション ソリューションに戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="423fb-144">However, to replace the report with another PowerBI.com solution, a power user must first revert to the standard application solution.</span></span> <span data-ttu-id="423fb-145">次の手順に従って、標準のアプリケーションソリューションに戻します。</span><span class="sxs-lookup"><span data-stu-id="423fb-145">Follow these steps to revert to the standard application solution.</span></span>

1. <span data-ttu-id="423fb-146">アクション ペインの **オプション** タブの **Power BI** グループで **分析の復元** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="423fb-146">On the Action Pane, on the **Options** tab, in the **Power BI** group, select **Restore Analytics**.</span></span>

    ![[分析の復元] ボタン](media/restore-powerbi-report-analytics.png)

2. <span data-ttu-id="423fb-148">ワークスペースの更新を表示するには、ページを再度読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="423fb-148">To view the updates to the workspace, you must reload the page.</span></span> <span data-ttu-id="423fb-149">ワークスペースから移動して戻ってくるか、ブラウザーを更新します。</span><span class="sxs-lookup"><span data-stu-id="423fb-149">Either move away from the workspace and then return, or refresh your browser.</span></span>
3. <span data-ttu-id="423fb-150">**報酬管理** ワークスペースで、**分析** タブを選択し、分析ワークスペースに埋め込まれた 標準ソリューション にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="423fb-150">In the **Compensation management** workspace, select the **Analytics** tab to access the standard solution that is now embedded in the analytical workspace.</span></span>