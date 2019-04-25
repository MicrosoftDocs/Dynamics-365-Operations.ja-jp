---
title: 1 つのバージョンのサービス更新の概要
description: このトピックでは、1 つのバージョンの一部として Microsoft によって開始されたサービスの更新を管理するための体験を構成する、さまざまな手順の概要を説明します。
author: meeram
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a33b481d238297294dfce2b08815e24233c540a4
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/14/2019
ms.locfileid: "842332"
---
# <a name="one-version-service-updates-overview"></a><span data-ttu-id="9305e-103">1 つのバージョンのサービス更新の概要</span><span class="sxs-lookup"><span data-stu-id="9305e-103">One Version service updates overview</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/coming-soon.md)]

<span data-ttu-id="9305e-104">次の一連のトピックでは Microsoft Dynamics 365 for Finance and Operations **バージョン 8.1 (2018 年 10 月) 以降** のサービス更新に関連する情報を提供しています。</span><span class="sxs-lookup"><span data-stu-id="9305e-104">The following set of topics provide information that is related to service updates for Microsoft Dynamics 365 for Finance and Operations **version 8.1 (October 2018) and later**.</span></span> <span data-ttu-id="9305e-105">これはクラウド リリースにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9305e-105">This is applicable for cloud releases only.</span></span>

- <span data-ttu-id="9305e-106">[標準および最初のリリース サービス更新](../../fin-and-ops/get-started/public-preview-releases.md) – このトピックはリリース頻度およびリリース プロセスに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9305e-106">[Standard and First release service updates](../../fin-and-ops/get-started/public-preview-releases.md) – This topic provides information about the release cadence and release process.</span></span>
- <span data-ttu-id="9305e-107">[ソフトウェアのライフサイクル ポリシーおよびクラウド リリース](../migration-upgrade/versions-update-policy.md) – このトピックはサービスの更新、可用性、およびサービス終了についての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9305e-107">[Software lifecycle policy and cloud releases](../migration-upgrade/versions-update-policy.md) – This topic provides information about the service updates, availability, and end of service.</span></span>
- <span data-ttu-id="9305e-108">[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-and-ops/get-started/one-version.md) – このトピックは更新プロセス、ツール、計画、および小売サービスの更新に関する質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="9305e-108">[One Version service updates FAQ](../../fin-and-ops/get-started/one-version.md) – This topic answers questions about the update process, tools, planning, and Retail service updates.</span></span>

<span data-ttu-id="9305e-109">サービス更新の経験は 4 つの異なるステップから構成されています:</span><span class="sxs-lookup"><span data-stu-id="9305e-109">The experience for service updates consists of four distinct steps:</span></span> 

1. <span data-ttu-id="9305e-110">構成</span><span class="sxs-lookup"><span data-stu-id="9305e-110">Configure</span></span>
2. <span data-ttu-id="9305e-111">通知</span><span class="sxs-lookup"><span data-stu-id="9305e-111">Notice</span></span>
3. <span data-ttu-id="9305e-112">更新</span><span class="sxs-lookup"><span data-stu-id="9305e-112">Update</span></span>
4. <span data-ttu-id="9305e-113">検証</span><span class="sxs-lookup"><span data-stu-id="9305e-113">Validate</span></span>

<span data-ttu-id="9305e-114">このトピックの残りでは各ステップについて説明し、関連トピックへのリンクを示します。</span><span class="sxs-lookup"><span data-stu-id="9305e-114">The rest of this topic describes each step and provides links to related topics.</span></span>

## <a name="configure"></a><span data-ttu-id="9305e-115">構成</span><span class="sxs-lookup"><span data-stu-id="9305e-115">Configure</span></span>

<span data-ttu-id="9305e-116">顧客はビジネスの制約に基づいて保守時間枠を選択できます。</span><span class="sxs-lookup"><span data-stu-id="9305e-116">Customers can select a maintenance window, based on their business constraints.</span></span> <span data-ttu-id="9305e-117">Microsoft Dynamics Lifecycle Services (LCS) で、次の図に示すように **プロジェクト設定** ページの **設定の更新** タブで **実稼働環境の更新頻度** にあるフィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9305e-117">In Microsoft Dynamics Lifecycle Services (LCS), use the fields in the **Production environment update cadence** section on the **Update settings** tab of the **Project settings** page, as shown in the following image.</span></span> <span data-ttu-id="9305e-118">今後の計画を立てるには次回の更新のカレンダーを利用できます。</span><span class="sxs-lookup"><span data-stu-id="9305e-118">A calendar of upcoming updates is available to help you plan ahead.</span></span>

<span data-ttu-id="9305e-119">[![プロジェクト設定ページの更新設定タブ](./media/UpdateSettings-ConfigureUpdates.JPG)](./media/UpdateSettings-ConfigureUpdates.JPG)</span><span class="sxs-lookup"><span data-stu-id="9305e-119">[![Update settings tab on the Project settings page](./media/UpdateSettings-ConfigureUpdates.JPG)](./media/UpdateSettings-ConfigureUpdates.JPG)</span></span>

<span data-ttu-id="9305e-120">ユーザーは新機能をオプトインして有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9305e-120">Users must opt in to new features and turn them on.</span></span> <span data-ttu-id="9305e-121">すべての更新プログラムは最初にユーザー受け入れテスト (UAT) 環境に適用され、それから実稼働環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9305e-121">All updates are applied first to the user acceptance testing (UAT) environment and then to the production environment.</span></span> <span data-ttu-id="9305e-122">したがって、顧客が必要な検証を行う時間があります。</span><span class="sxs-lookup"><span data-stu-id="9305e-122">Therefore, customers have time to do any validation that is required.</span></span> <span data-ttu-id="9305e-123">顧客は更新される環境を選択できます。</span><span class="sxs-lookup"><span data-stu-id="9305e-123">Customers can select the environment that is updated.</span></span> <span data-ttu-id="9305e-124">最大で 3 か月まで更新プログラムを一時停止することもできます。</span><span class="sxs-lookup"><span data-stu-id="9305e-124">They can also pause an update for up to three months.</span></span>

## <a name="notice"></a><span data-ttu-id="9305e-125">通知</span><span class="sxs-lookup"><span data-stu-id="9305e-125">Notice</span></span>

<span data-ttu-id="9305e-126">[リリース ノート](https://docs.microsoft.com/business-applications-release-notes/april19/dynamics365-finance-operations/) を、今後の計画や何が変化しているのか理解するのを助けるためにできます。</span><span class="sxs-lookup"><span data-stu-id="9305e-126">[Release notes](https://docs.microsoft.com/business-applications-release-notes/april19/dynamics365-finance-operations/) will be available to help you plan ahead and understand what is changing.</span></span> <span data-ttu-id="9305e-127">最大で 3 か月前から次の新機能について学ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="9305e-127">You can learn about upcoming features up to three months in advance.</span></span> <span data-ttu-id="9305e-128">[新機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed) のトピックでは特定の月の更新プログラムに関する詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="9305e-128">The [What's new](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed) topics provide details about the updates for specific months.</span></span>

<span data-ttu-id="9305e-129">さらに、通知電子メールが 5 日前に送信され、次の図に示すように更新の直前に通知が LCS に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9305e-129">Additionally, a notification email will be sent five days in advance, and a notification will appear in LCS just before an update, as shown in the following illustration.</span></span>

<span data-ttu-id="9305e-130">[![LCS の次回の更新プログラムの通知](./media/Notification-bar.PNG)](./media/Notification-bar.PNG)</span><span class="sxs-lookup"><span data-stu-id="9305e-130">[![Upcoming updates notification in LCS](./media/Notification-bar.PNG)](./media/Notification-bar.PNG)</span></span>

## <a name="update"></a><span data-ttu-id="9305e-131">更新</span><span class="sxs-lookup"><span data-stu-id="9305e-131">Update</span></span>

<span data-ttu-id="9305e-132">通知が送信された後、Microsoft は指定された保守時間枠で更新 (**自動更新**) を適用します。</span><span class="sxs-lookup"><span data-stu-id="9305e-132">After notifications have been sent, Microsoft will apply the update (**auto update**) during the designated maintenance window.</span></span> <span data-ttu-id="9305e-133">この操作が完了した後、更新の状態を示す通知電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="9305e-133">After this operation is completed, a notification email will be sent to indicate the status of the update.</span></span> <span data-ttu-id="9305e-134">LCS の標準的な更新エクスペリエンスを使用することで **自己更新** も可能になります。</span><span class="sxs-lookup"><span data-stu-id="9305e-134">Customers will also be able to **self-update** by using the standard update experience in LCS.</span></span> <span data-ttu-id="9305e-135">詳細については、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9305e-135">For more information, see [Apply updates to cloud environments](../deployment/apply-deployable-package-system.md).</span></span> 

<span data-ttu-id="9305e-136">初回リリース プログラムに参加している顧客は、サンドボックス環境およびその他の環境を早期に更新する機会があります。</span><span class="sxs-lookup"><span data-stu-id="9305e-136">Customers who participate in the First release program will have an opportunity to update their sandbox environment and other environments early.</span></span> <span data-ttu-id="9305e-137">初回リリース プログラムに登録するには [http://experience.dynamics.com](http://experience.dynamics.com) に移動します。</span><span class="sxs-lookup"><span data-stu-id="9305e-137">To sign up for the First release program, go to [http://experience.dynamics.com](http://experience.dynamics.com).</span></span>

<span data-ttu-id="9305e-138">次の図に示すように、LCS の標準的な更新エクスペリエンスを使用することで **自己更新** も可能になります。</span><span class="sxs-lookup"><span data-stu-id="9305e-138">Customers will also be able to **self-update** by using the standard update experience in LCS, as shown in the following illustration.</span></span>

<span data-ttu-id="9305e-139">[![LCS の管理メニューで更新コマンドを適用する](./media/Self-Update-Execute.jpg)](./media/Self-Update-Execute.jpg)</span><span class="sxs-lookup"><span data-stu-id="9305e-139">[![Apply updates command on the Maintain menu in LCS](./media/Self-Update-Execute.jpg)](./media/Self-Update-Execute.jpg)</span></span>

## <a name="validate"></a><span data-ttu-id="9305e-140">検証</span><span class="sxs-lookup"><span data-stu-id="9305e-140">Validate</span></span>

<span data-ttu-id="9305e-141">UAT 環境で更新が完了したら、基本的なビジネス プロセス テストを実行して環境を検証できます。</span><span class="sxs-lookup"><span data-stu-id="9305e-141">After an update is completed in the UAT environment, a basic business process test can be executed to validate the environment.</span></span> <span data-ttu-id="9305e-142">次の図に示すように、この作業量をサポートするビジネス プロセス テスト用のコードなし自動化テスト ツールを利用できます。</span><span class="sxs-lookup"><span data-stu-id="9305e-142">To support this effort, a no-code automation test tool for business process testing is available, as shown in the following illustration.</span></span> <span data-ttu-id="9305e-143">詳細については [タスク記録および BPM を使用して、ユーザー承認テスト ライブラリを作成する](using-task-guides-and-bpm-to-create-user-acceptance-tests.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9305e-143">For more information, see [Create user acceptance test libraries by using task recordings and BPM](using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span> 

<span data-ttu-id="9305e-144">[![Regression Suite Automation Tool](./media/TestAutomation.png)](./media/TestAutomation.png)</span><span class="sxs-lookup"><span data-stu-id="9305e-144">[![Regression Suite Automation Tool](./media/TestAutomation.png)](./media/TestAutomation.png)</span></span>

<span data-ttu-id="9305e-145">一部の顧客は外部データ統合と内部データ統合の両方があります。</span><span class="sxs-lookup"><span data-stu-id="9305e-145">Some customers have both external data integrations and internal data integrations.</span></span> <span data-ttu-id="9305e-146">これらの顧客はテストに [データ タスクの自動化ツール](../data-entities/data-task-automation.md) を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9305e-146">We recommend that these customers use the [Data task automation tool](../data-entities/data-task-automation.md) for testing.</span></span>


