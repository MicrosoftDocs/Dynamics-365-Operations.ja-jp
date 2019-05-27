---
title: Retail Cloud Scale Unit の初期化
description: このトピックでは、Retail Cloud Scale Unit を初期化する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 7d51286065d09ed3bb61565c2f9e4763100fd4d2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537083"
---
# <a name="initialize-retail-cloud-scale-unit"></a><span data-ttu-id="7e34d-103">Retail Cloud Scale Unit の初期化</span><span class="sxs-lookup"><span data-stu-id="7e34d-103">Initialize Retail Cloud Scale Unit</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7e34d-104">アプリケーション バージョン 8.1.2.x 以降を持つレベル 2 サンドボックスまたは運用環境を使用している場合、販売時点管理 (POS) 操作またはクラウド内の Retail サーバーを使用する電子商取引操作に Retail チャネル機能を使用する前に、Retail Cloud Scale Unit を初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e34d-104">If you're using a Tier-2 sandbox or production environment that has application version 8.1.2.x or later, you must initialize Retail Cloud Scale Unit before you can use retail channel functionality either for point of sale (POS) operations or for e-Commerce operations that use Retail Server in the cloud.</span></span> <span data-ttu-id="7e34d-105">初期化は Retail Cloud Scale Unit を展開します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-105">Initialization will deploy a Retail Cloud Scale Unit.</span></span>

<span data-ttu-id="7e34d-106">このトピックでは、Retail Cloud Scale Unit を初期化するための手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-106">This topic describes the steps for initializing Retail Cloud Scale Unit.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7e34d-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="7e34d-107">Prerequisites</span></span>

1. <span data-ttu-id="7e34d-108">アプリケーション バージョン 8.1.2.x またはそれ以降を持つレベル 2 サンドボックスまたは運協環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-108">Deploy a Tier-2 sandbox or production environment that has application version 8.1.2.x or later.</span></span>
2. <span data-ttu-id="7e34d-109">Microsoft Dynamics Lifecycle Services (LCS) で、サポート リクエストを作成し、**Retail Cloud Scale Unit のアクセス権の要求** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-109">In Microsoft Dynamics Lifecycle Services (LCS), create a support request, and enter **Access request for Retail Cloud Scale Unit**.</span></span>

<span data-ttu-id="7e34d-110">要求は、5 営業日以内に完了されます。</span><span class="sxs-lookup"><span data-stu-id="7e34d-110">The request will be completed within five business days.</span></span>

## <a name="initialize-retail-cloud-scale-unit-as-part-of-a-new-environment-deployment"></a><span data-ttu-id="7e34d-111">Retail Cloud Scale Unit を新しい環境の展開の一部として初期化します</span><span class="sxs-lookup"><span data-stu-id="7e34d-111">Initialize Retail Cloud Scale Unit as part of a new environment deployment</span></span>

1. <span data-ttu-id="7e34d-112">LCS の環境の詳細 ページで、**環境機能 \> Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-112">In LCS, on the environment details page, select **Environment features \> Retail**.</span></span>
2. <span data-ttu-id="7e34d-113">Retail 設定配置ページで、**初期化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-113">On the Retail setup deployment page, select **Initialize**.</span></span>
3. <span data-ttu-id="7e34d-114">初期化する Retail Cloud Scale Unit のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-114">Select the version of the Retail Cloud Scale Unit to initialize.</span></span>
4. <span data-ttu-id="7e34d-115">Retail Cloud Scale Unit を初期化するリージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-115">Select a region to initialize Retail Cloud Scale Unit in.</span></span>

## <a name="configure-retail-channels-to-use-rcsu"></a><span data-ttu-id="7e34d-116">RCSU を使用する小売チャンネルを構成します</span><span class="sxs-lookup"><span data-stu-id="7e34d-116">Configure retail channels to use RCSU</span></span>

1. <span data-ttu-id="7e34d-117">Retail Cloud Scale Unit が展開された後で、本社のクライアントで **Retail > Retail Headquarters > Retail スケジューラの設定 > チャンネル データベース** の順に移動して、この Retail Cloud Scale Unit のためにデータベースを使用するように小売りチャンネルが構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-117">After Retail Cloud Scale Unit has been deployed, in the head office client go to **Retail > Retail Headquarters > Retail Scheduler setup > Channel database** to ensure that your retail channels are configured to use the database for this Retail Cloud Scale Unit.</span></span>
2. <span data-ttu-id="7e34d-118">各小売りチャンネルに移動して、対応する Retail Cloud Scale Unit のチャンネル プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-118">Go to each retail channel and select the Channel Profile for the corresponding Retail Cloud Scale Unit.</span></span> 

## <a name="deploy-additional-retail-cloud-scale-units-optional"></a><span data-ttu-id="7e34d-119">追加の Retail Cloud Scale Unit を展開する (オプション)</span><span class="sxs-lookup"><span data-stu-id="7e34d-119">Deploy additional Retail Cloud Scale Units (optional)</span></span>

<span data-ttu-id="7e34d-120">最初の Retail Cloud Scale Unit (RCSU) を初期化した後、オプションで RCSU をもうひとつ追加で展開できます。</span><span class="sxs-lookup"><span data-stu-id="7e34d-120">After you have initialized the first Retail Cloud Scale Unit (RCSU), you can optionally deploy one additional RCSU.</span></span> <span data-ttu-id="7e34d-121">複数の RCSU が必要な場合は、上限を増やすためにサポート要求の提出が必要で、これには必要な RCSU の数、環境名、そして希望する地域が必要です。</span><span class="sxs-lookup"><span data-stu-id="7e34d-121">If you need more than 2 RCSUs, you need to file a support request to increase the limit, stating the number of RCSUs needed, environment name, and desired regions.</span></span>

<span data-ttu-id="7e34d-122">展開する追加の RCSU ごとに、チャネル データ ベースグループを 個別に作成することもお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7e34d-122">For each additional RCSU that you deploy, it is also recommended that you create a separate channel database group for each RCSU.</span></span> <span data-ttu-id="7e34d-123">これを行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7e34d-123">To do this, follow these steps:</span></span> 

1. <span data-ttu-id="7e34d-124">小売本社で、**Retail > Retail Headquarters > Retail スケジューラーの設定 > チャンネル データベース グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-124">In Retail head office, go to **Retail > Retail Headquarters > Retail Scheduler setup > Channel database group**.</span></span>
2. <span data-ttu-id="7e34d-125">新しいチャネル データベース グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-125">Create a new channel database group.</span></span> 
3. <span data-ttu-id="7e34d-126">**Retail > Retail Headquarters > Retail スケジューラの設定 > チャンネル データベース** フォームの順に移動し、新しく作成された RCSU に対応するチャンネル データベースを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-126">Go to the **Retail > Retail Headquarters > Retail Scheduler setup > Channel database** form and select the channel database that corresponds to the newly created RCSU.</span></span> 
4. <span data-ttu-id="7e34d-127">**編集** を選択して、新しいチャンネル データベース グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-127">Select **Edit** and select the new channel database group.</span></span> 
5. <span data-ttu-id="7e34d-128">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-128">Select **Save**.</span></span>
6. <span data-ttu-id="7e34d-129">選択したチャンネル データベースに対して **完全データ同期の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-129">Select **Run Full data sync** for the selected channel database.</span></span>

## <a name="additional-considerations-if-you-initialize-cloud-hosted-retail-channel-components-in-an-existing-environment"></a><span data-ttu-id="7e34d-130">既存の環境でクラウドにホストされた Retail チャネル コンポーネントを初期化する場合の追加の考慮事項</span><span class="sxs-lookup"><span data-stu-id="7e34d-130">Additional considerations if you initialize cloud-hosted Retail channel components in an existing environment</span></span>

<span data-ttu-id="7e34d-131">環境でクラウドでホストされている Retail チャネル コンポーネントを既に使用している場合、Retail Cloud Scale Unit の初期化はそれらのコンポーネントの更新時にダウンタイムを減らすのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7e34d-131">If you're already using cloud-hosted Retail channel components in an environment, initialization of Retail Cloud Scale Unit will help reduce the downtime when those components are updated.</span></span> <span data-ttu-id="7e34d-132">Retail Cloud Scale Unit の初期化を行う前に、追加の計画が必要です。</span><span class="sxs-lookup"><span data-stu-id="7e34d-132">Additional planning is required before initialization of Retail Cloud Scale Unit.</span></span>

1. <span data-ttu-id="7e34d-133">POS のすべてのシフトがクローズしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7e34d-133">Make sure that all shifts at the POS are closed.</span></span>
2. <span data-ttu-id="7e34d-134">すべての P ジョブが正常に完了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-134">Make sure that all P-jobs have been successfully completed.</span></span>
3. <span data-ttu-id="7e34d-135">すべての POS デバイスからサインアウトします。</span><span class="sxs-lookup"><span data-stu-id="7e34d-135">Sign out of all POS devices.</span></span>

<span data-ttu-id="7e34d-136">Retail サーバーを使用する店舗およびオンライン チャネルのすべての工程で、5 時間のダウンタイム ウィンドウを計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e34d-136">You should plan for a five-hour downtime window for the store and any online channel operations that use Retail Server.</span></span>

<span data-ttu-id="7e34d-137">初期化期間中に実行される内容を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-137">Here is what occurs during the initialization period:</span></span>

- <span data-ttu-id="7e34d-138">クラウドでホストされている Retail チャンネルは機能しません (POS オフライン機能がオンの場合を除く)。</span><span class="sxs-lookup"><span data-stu-id="7e34d-138">Cloud-hosted Retail channels won't work (unless POS offline capability is turned on).</span></span>
- <span data-ttu-id="7e34d-139">オフライン機能がオンになっている POS デバイスは機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="7e34d-139">POS devices with offline capability turned on will have reduced functionality.</span></span>
- <span data-ttu-id="7e34d-140">Retail サーバーに依存しているすべての電子商取引クライアントが中断されます。</span><span class="sxs-lookup"><span data-stu-id="7e34d-140">Any e-Commerce clients that depend on Retail Server will be disrupted.</span></span>
- <span data-ttu-id="7e34d-141">Retail Store Scale Unit でホストされているチャネルは影響されません。</span><span class="sxs-lookup"><span data-stu-id="7e34d-141">Channels that are hosted on Retail Store Scale Units won't be affected.</span></span>
- <span data-ttu-id="7e34d-142">本社機能は影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="7e34d-142">Head office functionality won't be affected.</span></span>

<span data-ttu-id="7e34d-143">初期化が完了した後に起きる事柄を示します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-143">Here is what occurs after initialization is completed:</span></span>

- <span data-ttu-id="7e34d-144">アクティブ化されたすべての POS デバイスのデバイス有効化状態は保持されます。つまり、デバイスを再有効化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7e34d-144">The device activation state of all activated POS devices will be preserved, which means that the devices won't have to be reactivated.</span></span>
- <span data-ttu-id="7e34d-145">スタンドアロン ハードウェア ステーション インスタンスは引き続き機能します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-145">Stand-alone hardware station instances will continue to work.</span></span>
- <span data-ttu-id="7e34d-146">POS チャンネル側のレポートはリセットされ、データを初期化する前に表示されません。</span><span class="sxs-lookup"><span data-stu-id="7e34d-146">POS channel–side reports will be reset and won't show data from before the initialization.</span></span>
- <span data-ttu-id="7e34d-147">仕訳帳の処理の表示もリセットされるため、初期化前のデータは表示されません。</span><span class="sxs-lookup"><span data-stu-id="7e34d-147">Show journal operation will also be reset and won't show data from before the initialization.</span></span>
