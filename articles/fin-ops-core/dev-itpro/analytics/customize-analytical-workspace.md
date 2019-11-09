---
title: 分析ワークスペースでの埋め込みレポートのカスタマイズ
description: このトピックでは、分析ワークスペースに埋め込まれているアプリケーション レポートをパワー ユーザーがカスタマイズできるようにする方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 7/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PowerBIConfiguration
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27661
ms.assetid: 861cfa94-c6f3-4c84-89ac-22c78bf6b7a4
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2019-07-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 606a33c66da719be83f52cefe6f6a7662720b451
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174575"
---
# <a name="customize-embedded-reports-in-analytical-workspaces"></a><span data-ttu-id="c37fc-103">分析ワークスペースでの埋め込みレポートのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="c37fc-103">Customize embedded reports in analytical workspaces</span></span>

[!include [banner](../includes/banner.md)]


## <a name="analytical-workspaces"></a><span data-ttu-id="c37fc-104">分析ワークスペース</span><span class="sxs-lookup"><span data-stu-id="c37fc-104">Analytical workspaces</span></span>

<span data-ttu-id="c37fc-105">アプリケーション スイートには、分析ワークスペースがバンドルされています。</span><span class="sxs-lookup"><span data-stu-id="c37fc-105">Analytical workspaces are bundled with the application suite.</span></span> <span data-ttu-id="c37fc-106">レポートを使用すると、標準の業務オペレーションに基づくデータへのユーザー インサイトを提供できます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-106">Through reporting, they offer users insights into data that is based on standard business operations.</span></span> <span data-ttu-id="c37fc-107">このレポートは、ビジネス専門家によって定義される包括的なレポートです。</span><span class="sxs-lookup"><span data-stu-id="c37fc-107">The reports are generic reports that are defined by business professionals.</span></span> <span data-ttu-id="c37fc-108">これには、あらゆる業種の幅広いユーザーの興味を引くメトリクスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-108">They include metrics that are considered interesting to a wide range of users from any industry.</span></span>

<span data-ttu-id="c37fc-109">ただし、場合によっては、標準レポートに、すべての顧客に関連しないデータが含まれていることがあります。</span><span class="sxs-lookup"><span data-stu-id="c37fc-109">However, in some cases, the standard reports include data that isn't relevant to all customers.</span></span> <span data-ttu-id="c37fc-110">多くの場合、顧客は、標準レポートから除外されたデータポイントまたは計算にアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-110">More often, customers might want to access data points or calculations that are left out of the standard reports.</span></span>

<span data-ttu-id="c37fc-111">パワー ユーザーは、ウェブ フレンドリー設計ツールを使用して、アプリケーションに埋め込まれている分析レポートをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-111">Power users can use web-friendly design tools to customize the analytical reports that are embedded in the application.</span></span> <span data-ttu-id="c37fc-112">自由形式のキャンバス デザイナーを使用すると、必要な関連業務インサイトに習熟しているユーザーは組織の成功を支援できます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-112">By using the free-form canvas designer, users who are familiar with the relevant business insights that are required can help make the organization successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c37fc-113">埋め込み分析レポートに対して行われたカスタマイズは、サービスによって自動的に配置され、システムの他のユーザーが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c37fc-113">Customizations that are made to the embedded analytical reports are automatically deployed by the service and made available to other users of the system.</span></span>

### <a name="important-points-about-embedded-analytical-reports"></a><span data-ttu-id="c37fc-114">埋め込み分析レポートに関する重要なポイント</span><span class="sxs-lookup"><span data-stu-id="c37fc-114">Important points about embedded analytical reports</span></span>

<span data-ttu-id="c37fc-115">標準レポートからは、特定のビジネス ペルソナに合わせてカスタマイズされたインサイトが提供されますが、カスタマイズによって、しばしば、これらの標準レポートの価値を最大化することができます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-115">Although the standard reports deliver insights that are tailored to a given business persona, customizations can often maximize the value of these standard reports.</span></span>

<span data-ttu-id="c37fc-116">このサービス機能に関する重要な注意事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="c37fc-116">Here are some important points to note about this service capability:</span></span>

- <span data-ttu-id="c37fc-117">カスタマイズはレポート デザイン キャンバスに限定されます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-117">Customizations are limited to the report design canvas.</span></span> <span data-ttu-id="c37fc-118">ユーザーは、レポートのデータ セットの定義を変更できません。</span><span class="sxs-lookup"><span data-stu-id="c37fc-118">Users can't change the definitions of report data sets.</span></span>
- <span data-ttu-id="c37fc-119">分析ワークスペースに対して行われるレポートのカスタマイズは、環境内のすべてのユーザーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-119">Report customizations that are made to the analytical workspace apply to all users in the environment.</span></span>
- <span data-ttu-id="c37fc-120">このサービスでは、製品のアップグレード時にレポートのカスタマイズが自動的に維持されます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-120">The service automatically preserves report customizations during product upgrades.</span></span>
- <span data-ttu-id="c37fc-121">サービスは、分析ワークスペースに対して行われたカスタマイズのエクスポートをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="c37fc-121">The service doesn't support the export of customizations that are made to analytical workspaces.</span></span>

### <a name="customize-an-analytical-workspace"></a><span data-ttu-id="c37fc-122">分析ワークスペースをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="c37fc-122">Customize an analytical workspace</span></span>

<span data-ttu-id="c37fc-123">埋め込みアプリケーション ソリューションをカスタマイズするには、ユーザーはシステム レポート エディター セキュリティ グループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="c37fc-123">To customize the embedded application solutions, a user must be a member of the System Report Editors security group.</span></span> <span data-ttu-id="c37fc-124">このセキュリティ グループのメンバーは、アプリケーション ワークスペースのアクション ウィンドウの**オプション** タブにあるボタンを使用してカスタマイズを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-124">Members of this security group can do customizations by using the buttons on the **Options** tab on the Action Pane of the application workspaces.</span></span> <span data-ttu-id="c37fc-125">この例では、アプリケーション スイートにバンドルされている標準分析ワークスペースのいずれかをカスタマイズする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c37fc-125">This example shows how to customize one of the standard analytical workspaces that are bundled with the application suite.</span></span>

1. <span data-ttu-id="c37fc-126">サインインし、カスタマイズするアプリケーション ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-126">Sign in and open the application workspace that you want to customize.</span></span> <span data-ttu-id="c37fc-127">この例では、 **報酬管理** ワークスペースに埋め込まれている標準分析レポートを置換します。</span><span class="sxs-lookup"><span data-stu-id="c37fc-127">In this example, you will replace the standard analytical report that is embedded in the **Compensation management** workspace.</span></span>

    ![報酬管理ワークスペース](media/compensation-management-workspace.png)

2. <span data-ttu-id="c37fc-129">**分析** タブを選択すると、ワークスペースの埋め込み分析レポートにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-129">Select the **Analytics** tab to access the workspace's embedded analytical report.</span></span>

    ![報酬管理分析ワークスペースの [分析] タブ](media/compensation-management-analytics.png)

    <span data-ttu-id="c37fc-131">デフォルトでは、アプリケーションと共にパッケージ化された標準分析ワークスペース ソリューションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-131">By default, you see the standard analytical workspace solution that is packaged with your application.</span></span> <span data-ttu-id="c37fc-132">このソリューションのレポートは、プロビジョニング プロセス中に環境に合わせて自動的に配置および設定されます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-132">The reports in this solution are automatically deployed and configured for your environment during the provisioning process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c37fc-133">分析ワークスペースには、Power BI専用の環境に対してのみ使用できるホストされたMicrosoftサービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="c37fc-133">The analytical workspaces require a hosted Microsoft Power BI service that is available only for dedicated environments.</span></span> <span data-ttu-id="c37fc-134">詳細については、「[1 Box 環境での分析ワークスペースおよびレポートへのアクセス](https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c37fc-134">For more information, see [Accessing Analytical Workspaces and Reports on 1Box environment](https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/).</span></span>

3. <span data-ttu-id="c37fc-135">アクション ペインの**オプション** タブの**Power BI**グループで **Edit Analytics** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="c37fc-135">On the Action Pane, on the **Options** tab, in the **Power BI** group, select **Edit Analytics**.</span></span>

    ![Analytics Analytics ボタンを編集します](media/analytical-workspace-edit-entry.png)

    <span data-ttu-id="c37fc-137">編集モードで分析ワークスペースが開き、Power BI web デザイナー ツールに直接アクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-137">The analytical workspace is opened in edit mode, and you have direct access to the Power BI web designer tools.</span></span>

    ![分析ワークスペース レポート エディター](media/analytical-workspace-edit-view.png)

4. <span data-ttu-id="c37fc-139">レポート キャンバスPower BIをカスタマイズするには、web デザイナー ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="c37fc-139">Use the Power BI web designer tools to customize the report canvas.</span></span> <span data-ttu-id="c37fc-140">直感的な web コントロールを使用すると、ビジュアルの追加および削除、ビジュアル型の変更、コンテンツの書式設定などの一般的なアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-140">The intuitive web controls let you perform typical actions such as adding and removing visuals, changing visual types, and formatting the content.</span></span> <span data-ttu-id="c37fc-141">視覚エフェクト レポートのソースを調査して、システムで利用可能な最も関連性のあるデータに基づいて意思決定を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-141">You can also inspect the source of the report visualizations to make sure that decisions are based on the most relevant data that is available in the system.</span></span> <span data-ttu-id="c37fc-142">詳細については、「[Power BIレポートへの視覚エフェクトの追加](https://docs.microsoft.com/power-bi/visuals/power-bi-report-add-visualizations-i)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c37fc-142">For more information, see [Add visualizations to a Power BI report](https://docs.microsoft.com/power-bi/visuals/power-bi-report-add-visualizations-i).</span></span>
5. <span data-ttu-id="c37fc-143">レポートのカスタマイズが完了したら、 **保存** ボタンを選択してレポート編集のレベルを上げます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-143">After you've completed your report customizations, select the **Save** button to promote the report edits.</span></span> <span data-ttu-id="c37fc-144">レポートへのカスタマイズは、サービスにすぐに反映されます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-144">Customizations to the report are reflected immediately in the service.</span></span> <span data-ttu-id="c37fc-145">したがって、組織のユーザーは最新のイノベーションにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-145">Therefore, users in your organization have access to the latest innovations.</span></span>

## <a name="restore-the-standard-application-solution"></a><span data-ttu-id="c37fc-146">標準のアプリケーション ソリューションの復元</span><span class="sxs-lookup"><span data-stu-id="c37fc-146">Restore the standard application solution</span></span>

<span data-ttu-id="c37fc-147">アプリケーション ソリューションにバンドルされている分析ワークスペースを復元するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c37fc-147">Follow these steps to restore the analytical workspaces that are bundled with the application solution.</span></span>

1. <span data-ttu-id="c37fc-148">分析ワークスペースの、アクション ペインの、**オプション** タブの、**Power BI**グループで、**Restore Analytics** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="c37fc-148">In the analytical workspace, on the Action Pane, on the **Options** tab, in the **Power BI** group, select **Restore Analytics**.</span></span>
2. <span data-ttu-id="c37fc-149">ワークスペースの更新を表示するには、ページを再度読み込みます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-149">To view the updates to the workspace, reload the page.</span></span> <span data-ttu-id="c37fc-150">ワークスペースから移動して戻ってくるか、ブラウザーを更新します。</span><span class="sxs-lookup"><span data-stu-id="c37fc-150">Either move away from the workspace and then return, or refresh your browser.</span></span>
3. <span data-ttu-id="c37fc-151">**報酬管理**ワークスペースで、**Analytics** タブを選択すると、アプリケーションと共にパッケージ化された元の分析ワークスペースにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c37fc-151">In the **Compensation management** workspace, select the **Analytics** tab to access the original analytical workspace that was packaged with the application.</span></span>