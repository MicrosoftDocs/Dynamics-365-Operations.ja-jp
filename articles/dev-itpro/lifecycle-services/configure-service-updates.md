---
title: Lifecycle Services (LCS) によるサービスの更新の構成
description: このトピックでは、環境の最新のサービスを受け取る方法とタイミングを指定する方法について説明します。
author: manalidongre
manager: AnnBe
ms.date: 03/08/2019
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
ms.openlocfilehash: 35a710d210d99b5d28f7eea1b331a9c0b75bc830
ms.sourcegitcommit: 0bd0215d0735ed47b1b8af93a80bcdbf7ca2cc49
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2019
ms.locfileid: "790312"
---
# <a name="configure-service-updates-through-lifecycle-services-lcs"></a><span data-ttu-id="8c83b-103">Lifecycle Services (LCS) によるサービスの更新の構成</span><span class="sxs-lookup"><span data-stu-id="8c83b-103">Configure service updates through Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/coming-soon.md)]

<span data-ttu-id="8c83b-104">Microsoft Dynamics Lifecycle Services (LCS) では、Microsoft Dynamics 365 for Finance and Operations 環境のサービス更新を Microsoft から受け取る方法とタイミングを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-104">In Microsoft Dynamics Lifecycle Services (LCS), you can specify how and when you receive service updates from Microsoft for your Microsoft Dynamics 365 for Finance and Operations environments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c83b-105">この機能は **Microsoft Dynamics 365 for Finance and Operations バージョン 8.1 (2018 年 10 月) 以降** を使用していて[最初のリリース](../../fin-and-ops/get-started/public-preview-releases.md) プログラムの一部で **ない** 顧客だけが利用できます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-105">This feature is available only to customers who are using **Microsoft Dynamics 365 for Finance and Operations version 8.1 (October 2018) and later**, and who are **not** part of the [First release](../../fin-and-ops/get-started/public-preview-releases.md) program.</span></span> <span data-ttu-id="8c83b-106">Microsoft はこの機能を最初のリリースのお客様、および古いバージョンの製品を使用しているお客様もご利用いただけるよう努めています。</span><span class="sxs-lookup"><span data-stu-id="8c83b-106">Microsoft is working to make the feature available to First release customers and customers who use older versions of the product.</span></span> 

<span data-ttu-id="8c83b-107">LCS で **プロジェクト所有者** ロールが割り当てられているユーザー (顧客またはパートナー) のみが更新を構成できます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-107">Only users (customers or partners) who are assigned to the **Project owner** role in LCS can configure updates.</span></span> <span data-ttu-id="8c83b-108">さらに、更新は **実装プロジェクト** に対してのみ構成できます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-108">Additionally, updates can be configured only for **implementation projects**.</span></span>

<span data-ttu-id="8c83b-109">構成設定を変更するには、これらの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-109">Follow these steps to change your update settings.</span></span>

> [!NOTE]
> <span data-ttu-id="8c83b-110">これらの設定は、サービス更新にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-110">These settings apply only to service updates.</span></span> <span data-ttu-id="8c83b-111">毎月、環境に適用されているオペレーティング システム レベルのセキュリティ更新には影響がありません。</span><span class="sxs-lookup"><span data-stu-id="8c83b-111">They have no effect on the operating system–level security updates that are applied to your environments every month.</span></span>

1. <span data-ttu-id="8c83b-112">実装プロジェクトの LCS で **プロジェクト設定** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-112">In LCS, in your implementation project, open the **Project settings** page.</span></span>

    <span data-ttu-id="8c83b-113">このページには **更新プログラムの設定** という名前の新しいタブがあります。</span><span class="sxs-lookup"><span data-stu-id="8c83b-113">This page has a new tab that is named **Update settings**.</span></span>

2. <span data-ttu-id="8c83b-114">**更新設定** タブで、必要に応じて、次のコンフィギュレーション オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-114">On the **Update settings** tab, set the following configuration options as you require:</span></span>

    - <span data-ttu-id="8c83b-115">**更新環境**: 生産更新の前に更新する代替サンドボックス環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-115">**Update environment** – Select an alternate sandbox environment that should be updated before the production update.</span></span>

        <span data-ttu-id="8c83b-116">既定では、マイクロソフトは、まず基本サービスに含まれる第 2 層標準受け入れテスト (サンドボックス) 環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-116">By default, Microsoft first updates the Tier 2 Standard Acceptance Test (sandbox) environment that is included in the base offer.</span></span> <span data-ttu-id="8c83b-117">次に、更新プログラムを実稼働環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-117">It then applies the update to the production environment.</span></span> <span data-ttu-id="8c83b-118">第 2 層以上のサンドボックス アドオン環境を購入し、別のサンド ボックスを更新する場合は、代替環境に既定の環境を変更するためにこのフィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-118">If you've purchased Tier 2 and higher sandbox add-on environments and want a different sandbox to be updated, you can use this field to change the default environment to an alternate environment.</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="8c83b-119">ここで選択した環境は、実稼働環境に選択されている更新頻度の 7 暦日前に更新されます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-119">The environment that you select here will be updated seven calendar days before the update cadence that is selected for the production environment.</span></span>

    - <span data-ttu-id="8c83b-120">**製造環境更新頻度**: 実稼働環境への定期更新の頻度を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-120">**Production environment update cadence** – Select a recurring cadence for updates to your production environment.</span></span> <span data-ttu-id="8c83b-121">**環境の更新** フィールドで選択したサンドボックス環境は、選択されている頻度の 7 暦日前に更新されます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-121">The sandbox environment that is selected in the **Update environment** field will be updated seven calendar days before the selected cadence.</span></span> <span data-ttu-id="8c83b-122">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-122">The following options are available:</span></span>

        - <span data-ttu-id="8c83b-123">**頻度を選択**: 月の第 1 週、第 2 週、第 3 週に更新を受け取るかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-123">**Select the cadence** – Select whether to receive updates in the first, second, or third week of the month.</span></span>
        - <span data-ttu-id="8c83b-124">**3つのタイム ゾーンのいずれかを選択**: 実稼働環境を更新するタイム ゾーンを選択します: 東部標準時 (UTC - 5)、香港時 (UTC + 8)、またはグリニッジ標準時 (UTC + 0)。</span><span class="sxs-lookup"><span data-stu-id="8c83b-124">**Select one of the three time-zones** – Select the time zone that the production environment should be updated in: Eastern Time (UTC – 5), Hong Kong Time (UTC + 8), or Greenwich Mean Time (UTC + 0).</span></span>
        - <span data-ttu-id="8c83b-125">**曜日を選択:** 更新を受信する曜日を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-125">**Select a day of the week:** Select the day in the week when you want to receive updates.</span></span>
        - <span data-ttu-id="8c83b-126">**時間帯を選択:** 更新プログラムを受信する時間帯を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-126">**Select a time slot:** Select the time slot when you want to receive updates.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8c83b-127">現時点では、曜日および時間帯オプションはいくつかのオプションのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-127">Currently, only a few options are available for the day of the week and time slot options.</span></span> <span data-ttu-id="8c83b-128">Microsoft は、顧客の平日など、他のオプションもすぐに追加します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-128">Microsoft will add more options soon, such as weekdays for customers.</span></span>

 3. <span data-ttu-id="8c83b-129">コンフィギュレーション オプションの設定が完了したら **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-129">When you've finished setting the configuration options, select **Save**.</span></span>
 
<span data-ttu-id="8c83b-130">更新環境および更新頻度を設定したら、Microsoft は、今後6か月の更新カレンダーを生成します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-130">After you set the update environment and update cadence, Microsoft generates an update calendar for the next six months.</span></span> <span data-ttu-id="8c83b-131">このカレンダーは、コンフィギュレーション済のサンド ボックスと生産環境がいつ更新されるを正確に表示します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-131">This calendar shows exactly when the configured sandbox and production environments will be updated.</span></span> <span data-ttu-id="8c83b-132">したがって、各更新の予想される時期を特定できます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-132">Therefore, you will know when to expect each update.</span></span> <span data-ttu-id="8c83b-133">カレンダーを表示するには、**実稼働環境の更新頻度** オプションで **更新カレンダーを表示** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="8c83b-133">To view the calendar, select the **View update calendar** link under the **Production environment update cadence** options.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c83b-134">設定を保存した後いつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-134">After the settings are saved, you can change them at any time.</span></span> <span data-ttu-id="8c83b-135">ただし、進行中の展開がある場合、新しい設定は、既存の展開タイミングを更新するために使用されません。</span><span class="sxs-lookup"><span data-stu-id="8c83b-135">However, if there is an ongoing rollout, the new settings won't be used to update the existing rollout timings.</span></span> <span data-ttu-id="8c83b-136">代わりに、次の展開で使用され始めます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-136">Instead, they will start to be used in the next rollout.</span></span> <span data-ttu-id="8c83b-137">進行中の展開は、サンド ボックス環境の更新に関する電子メール通知が送信された日付から、実稼働環境の更新時の日付までの14日間の期間によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="8c83b-137">An ongoing rollout is defined by the 14-day period between the date when the email notification about the update of the sandbox environment is sent and the date when the production environment is updated.</span></span>

<span data-ttu-id="8c83b-138">構成されたサンドボックス環境および実稼働環境への更新を一時停止する方法の詳細は、[Lifecycle Services (LCS) によるサービスの更新の一時停止](pause-service-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c83b-138">For more information about how to pause updates to configured sandbox and production environments, see [Pause service updates through Lifecycle Services (LCS)](pause-service-updates.md).</span></span>

<span data-ttu-id="8c83b-139">1 つのバージョンおよび Microsoft が管理するサービスの更新の詳細は、[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-and-ops/get-started/one-version.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c83b-139">For more information about One Version and Microsoft-managed service updates, see [One Version service updates FAQ](../../fin-and-ops/get-started/one-version.md).</span></span>
