---
title: Retail Cloud Scale Unit の初期化
description: このトピックでは、Retail Cloud Scale Unit を初期化する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 08/06/2019
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
ms.openlocfilehash: a131a7bf08b4e34ca6d72606c910769a28e33f7a
ms.sourcegitcommit: db4eae8c42cbc4df80cc0c902428a1f64525c762
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885554"
---
# <a name="initialize-retail-cloud-scale-unit"></a><span data-ttu-id="e5a4a-103">Retail Cloud Scale Unit の初期化</span><span class="sxs-lookup"><span data-stu-id="e5a4a-103">Initialize Retail Cloud Scale Unit</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e5a4a-104">アプリケーション バージョン 8.1.2.x 以降を持つレベル 2 サンドボックスまたは運用環境を使用している場合、販売時点管理 (POS) 操作またはクラウド内の Retail サーバーを使用する電子商取引操作に Retail チャネル機能を使用する前に、Retail Cloud Scale Unit (RCSU) を初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-104">If you're using a Tier-2 sandbox or production environment that has application version 8.1.2.x or later, you must initialize Retail Cloud Scale Unit (RCSU) before you can use retail channel functionality either for point of sale (POS) operations or for e-Commerce operations that use Retail Server in the cloud.</span></span> <span data-ttu-id="e5a4a-105">初期化は Retail Cloud Scale Unit を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-105">Initialization will deploy a Retail Cloud Scale Unit.</span></span>

<span data-ttu-id="e5a4a-106">このトピックでは、Retail Cloud Scale Unit を初期化するための手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-106">This topic describes the steps for initializing Retail Cloud Scale Unit.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5a4a-107">クラウド環境で Retail チャネルの機能を利用しているお客様の場合は、業務の継続的なサポートを徹底するにあたり、2020年 1月 31日 までに Retail チャネルを更新して Retail Cloud Scale Unit を ご利用頂くよう推奨します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-107">For existing customers using Retail channel functionality in the cloud, to ensure continued and uninterrupted support for your business, we require that you update your retail channels to use Cloud Scale Unit no later than January 31, 2020.</span></span> <span data-ttu-id="e5a4a-108">Store Scale Unit を独占して使用している顧客に対しては、アクションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-108">There is no action required for customers who exclusively use Store Scale Unit.</span></span> <span data-ttu-id="e5a4a-109">延長が必要な場合は、Microsoft FastTrack Solution Architect までご連絡ください。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-109">Contact your Microsoft FastTrack Solution Architect if you require an extension.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e5a4a-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="e5a4a-110">Prerequisites</span></span>

1. <span data-ttu-id="e5a4a-111">アプリケーション バージョン 8.1.2.x またはそれ以降を持つレベル 2 サンドボックスまたは運協環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-111">Deploy a Tier-2 sandbox or production environment that has application version 8.1.2.x or later.</span></span>
2. <span data-ttu-id="e5a4a-112">Microsoft Dynamics Lifecycle Services (LCS) で環境ごとに 1 つを超える RCSU が必要な場合は、サポート要求を作成して、**複数の Retail Cloud Scale Unit に対するアクセス要求**を入力し、環境 ID、RCSU の数、および対応するデータ センター地域を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-112">If you require more than 1 RCSU per environment, in Microsoft Dynamics Lifecycle Services (LCS), create a support request, and enter **Access request for multiple Retail Cloud Scale Units** and indicate the environment ID, number of RCSUs, and corresponding datacenter regions.</span></span> <span data-ttu-id="e5a4a-113">要求は、5 営業日以内に完了されます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-113">The request will be completed within five business days.</span></span> <span data-ttu-id="e5a4a-114">環境ごとに複数の RCSU を必要としない場合は、サポート要求を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-114">If you do not require multiple RCSUs per environment, you do not need to create a support request.</span></span> 

## <a name="initialize-retail-cloud-scale-unit-as-part-of-a-new-environment-deployment"></a><span data-ttu-id="e5a4a-115">Retail Cloud Scale Unit を新しい環境の展開の一部として初期化します</span><span class="sxs-lookup"><span data-stu-id="e5a4a-115">Initialize Retail Cloud Scale Unit as part of a new environment deployment</span></span>

<span data-ttu-id="e5a4a-116">本社が使用可能か確認してください。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-116">Please make sure the headquarters is available.</span></span> <span data-ttu-id="e5a4a-117">これは、初期化プロセス中にスケール ユニットを本社に登録するために必要です。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-117">This is required to register the scale unit with the headquarters during the initialization process.</span></span> <span data-ttu-id="e5a4a-118">サービス プロセスで利用できなくなる可能性があるため、本社がサービス中の場合はスケール ユニットの初期化をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-118">It is not recommended to initialize a scale unit when the headquarters is under servicing, as it may become unavailable during its servicing process.</span></span>

1. <span data-ttu-id="e5a4a-119">本社環境が使用可能で [メンテナンス モード](../sysadmin/maintenance-mode.md) でないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-119">Make sure the headquarters environment is available and not in [Maintenance mode](../sysadmin/maintenance-mode.md).</span></span>
2. <span data-ttu-id="e5a4a-120">LCS の環境の詳細 ページで、**環境機能 \> Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-120">In LCS, on the environment details page, select **Environment features \> Retail**.</span></span>
3. <span data-ttu-id="e5a4a-121">Retail 設定配置ページで、**初期化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-121">On the Retail setup deployment page, select **Initialize**.</span></span>
4. <span data-ttu-id="e5a4a-122">初期化する Retail Cloud Scale Unit のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-122">Select the version of the Retail Cloud Scale Unit to initialize.</span></span>
5. <span data-ttu-id="e5a4a-123">Retail Cloud Scale Unit を初期化するリージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-123">Select a region to initialize Retail Cloud Scale Unit in.</span></span>

## <a name="configure-retail-channels-to-use-retail-cloud-scale-unit"></a><span data-ttu-id="e5a4a-124">Retail Cloud Scale Unit を使用する小売チャネルの構成</span><span class="sxs-lookup"><span data-stu-id="e5a4a-124">Configure retail channels to use Retail Cloud Scale Unit</span></span>

1. <span data-ttu-id="e5a4a-125">Retail Cloud Scale Unit が展開された後で、本社のクライアントで **Retail > Retail Headquarters > Retail スケジューラの設定 > チャンネル データベース** の順に移動して、この Retail Cloud Scale Unit のためにデータベースを使用するように小売りチャンネルが構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-125">After Retail Cloud Scale Unit has been deployed, in the head office client go to **Retail > Retail Headquarters > Retail Scheduler setup > Channel database** to ensure that your retail channels are configured to use the database for this Retail Cloud Scale Unit.</span></span>
2. <span data-ttu-id="e5a4a-126">各小売りチャンネルに移動して、対応する Retail Cloud Scale Unit のチャンネル プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-126">Go to each retail channel and select the Channel Profile for the corresponding Retail Cloud Scale Unit.</span></span>

### <a name="database-refresh-and-cloud-scale-units"></a><span data-ttu-id="e5a4a-127">データベースの更新とクラウド スケール ユニット</span><span class="sxs-lookup"><span data-stu-id="e5a4a-127">Database refresh and Cloud Scale Units</span></span>

<span data-ttu-id="e5a4a-128">始める前に [Retail 機能を使用する環境でデータベースを更新した後に完了する手順](../database/database-refresh.md#steps-to-complete-after-a-database-refresh-for-environments-that-use-retail-functionality) について慣れていることを確認して下さい。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-128">Before you begin, make sure you are familiar with [Steps to complete after a database refresh for environments that use Retail functionality](../database/database-refresh.md#steps-to-complete-after-a-database-refresh-for-environments-that-use-retail-functionality).</span></span>

<span data-ttu-id="e5a4a-129">データベース更新の一部として (チャネル データベース フォームで) スケール ユニット チャネル データベース レコードを環境を越えて移動できません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-129">The scale unit channel database records (in the Channel Database form) cannot be moved across environments as part of database refresh.</span></span> <span data-ttu-id="e5a4a-130">これはレコードが環境固有のコンフィギュレーションを表すためです。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-130">This is because the records represent environment specific configuration.</span></span>

<span data-ttu-id="e5a4a-131">データベースの更新後と Retail の再プロビジョニング ツールの実行後、LCS でスケール ユニットの再展開を発行して、スケール ユニットのチャネル データベース レコードを再生成できます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-131">After database refresh and after the Retail Reprovisioning tool has been executed, you can regenerate the scale unit's channel database record by issuing a re-deployment of your scale unit in LCS.</span></span> <span data-ttu-id="e5a4a-132">スケール ユニットで配置やサービス操作を行うと、登録が行われていないことが検出された場合に、本社でスケール ユニットが登録されます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-132">Any deployment or servicing operation in the scale unit will attempt to register the scale unit with the headquarters, if it detects that the registration is missing.</span></span>

<span data-ttu-id="e5a4a-133">スケール ユニットがすでに存在するのと同じバージョンの展開を選択することで、コンポーネントを変更することなくスケール ユニットの再配置を発行できます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-133">You can issue a re-deployment of the scale unit, without changing any components, by selecting to deploy the same version your scale unit is at already.</span></span> <span data-ttu-id="e5a4a-134">これは次の手順により LCS で行うことができます:</span><span class="sxs-lookup"><span data-stu-id="e5a4a-134">This can be done in LCS by the following steps:</span></span>

1. <span data-ttu-id="e5a4a-135">LCS の環境の詳細 ページで、**環境機能 \> Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-135">In LCS, on the environment details page, select **Environment features \> Retail**.</span></span>
2. <span data-ttu-id="e5a4a-136">[小売設定の配置] ページで再配置するスケール ユニットを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-136">On the Retail setup deployment page, select the scale unit you would like to redeploy.</span></span>
3. <span data-ttu-id="e5a4a-137">スケール ユニットの操作メニューで **更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-137">On the scale unit's operation menu, select **Update**</span></span>
4. <span data-ttu-id="e5a4a-138">スライダーの **バージョンの選択** のドロップダウンで **バージョンの指定** オプションを選択します</span><span class="sxs-lookup"><span data-stu-id="e5a4a-138">On the slider, on the drop-down for **Select version**, pick the option **Specify a version**</span></span>
5. <span data-ttu-id="e5a4a-139">**バージョンの指定** の下のテキスト ボックスに、スケール ユニットの **現在のバージョン** ラベルの横に表示されたバージョンを入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-139">On the text box under **Specify a version**, type in the version shown for your scale unit, shown besides the **Current version** label</span></span>
6. <span data-ttu-id="e5a4a-140">**更新** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-140">Click on **Update** button</span></span>

<span data-ttu-id="e5a4a-141">以前に拡張を適用した場合でも、スケール ユニットを更新するときに最後に適用された拡張パッケージが自動的に選択されるため、**拡張機能の更新** を選択する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-141">You do not need to select **Update extensions**, even if you have applied extensions previously, since the last extension package applied to the scale unit is automatically picked when updating a scale unit.</span></span>

<span data-ttu-id="e5a4a-142">複数のスケール ユニットがある場合は、各スケール ユニットに対して上記の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-142">If you have multiple scale units, you need to perform the operation above for each scale unit.</span></span> <span data-ttu-id="e5a4a-143">必要に応じて、これらの操作を並行して実行できます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-143">You may perform these operations in parallel, if desired.</span></span>

## <a name="deploy-additional-retail-cloud-scale-units-optional"></a><span data-ttu-id="e5a4a-144">追加の Retail Cloud Scale Unit を展開する (オプション)</span><span class="sxs-lookup"><span data-stu-id="e5a4a-144">Deploy additional Retail Cloud Scale Units (optional)</span></span>

<span data-ttu-id="e5a4a-145">最初の Retail Cloud Scale Unit (RCSU) を初期化した後、追加のクラウド スケール ユニットが必要な場合はサポート要求を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-145">After you have initialized the first Retail Cloud Scale Unit (RCSU), if you require additional cloud scale units, enter a support request.</span></span> <span data-ttu-id="e5a4a-146">サポート要求で、必要な RCSU の数、環境名、希望するリージョンを明記します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-146">In the support request, state the number of RCSUs needed, environment name, and desired regions.</span></span>

<span data-ttu-id="e5a4a-147">展開する追加の RCSU ごとに、チャネル データ ベースグループを 個別に作成することもお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-147">For each additional RCSU that you deploy, it is also recommended that you create a separate channel database group for each RCSU.</span></span> <span data-ttu-id="e5a4a-148">これを行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-148">To do this, follow these steps:</span></span>

1. <span data-ttu-id="e5a4a-149">小売本社で、**Retail > Retail Headquarters > Retail スケジューラーの設定 > チャンネル データベース グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-149">In Retail head office, go to **Retail > Retail Headquarters > Retail Scheduler setup > Channel database group**.</span></span>
2. <span data-ttu-id="e5a4a-150">新しいチャネル データベース グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-150">Create a new channel database group.</span></span>
3. <span data-ttu-id="e5a4a-151">**Retail > Retail Headquarters > Retail スケジューラの設定 > チャンネル データベース** フォームの順に移動し、新しく作成された RCSU に対応するチャンネル データベースを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-151">Go to the **Retail > Retail Headquarters > Retail Scheduler setup > Channel database** form and select the channel database that corresponds to the newly created RCSU.</span></span>
4. <span data-ttu-id="e5a4a-152">**編集** を選択して、新しいチャンネル データベース グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-152">Select **Edit** and select the new channel database group.</span></span>
5. <span data-ttu-id="e5a4a-153">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-153">Select **Save**.</span></span>
6. <span data-ttu-id="e5a4a-154">選択したチャンネル データベースに対して **完全データ同期の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-154">Select **Run Full data sync** for the selected channel database.</span></span>

## <a name="additional-considerations-if-you-initialize-cloud-hosted-retail-channel-components-in-an-existing-environment"></a><span data-ttu-id="e5a4a-155">既存の環境でクラウドにホストされた Retail チャネル コンポーネントを初期化する場合の追加の考慮事項</span><span class="sxs-lookup"><span data-stu-id="e5a4a-155">Additional considerations if you initialize cloud-hosted Retail channel components in an existing environment</span></span>

<span data-ttu-id="e5a4a-156">環境でクラウドでホストされている Retail チャネル コンポーネントを既に使用している場合、Retail Cloud Scale Unit の初期化はそれらのコンポーネントの更新時にダウンタイムを減らすのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-156">If you're already using cloud-hosted Retail channel components in an environment, initialization of Retail Cloud Scale Unit will help reduce the downtime when those components are updated.</span></span> <span data-ttu-id="e5a4a-157">Retail Cloud Scale Unit の初期化を行う前に、追加の計画が必要です。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-157">Additional planning is required before initialization of Retail Cloud Scale Unit.</span></span>

<span data-ttu-id="e5a4a-158">クラウドでホストされた小売チャネル コンポーネントを使用する環境で最初のクラウド スケール ユニットを初期化するときに、初期化プロセスではクラウドでホストされたチャネル コンポーネントに関連付けられているチャネルを最初のスケール ユニットに移行します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-158">When you initialize your first Cloud Scale Unit in an environment that uses cloud-hosted Retail channel components, the initialization process will migrate your channels associated to the cloud-hosted channel components to the first scale unit.</span></span> <span data-ttu-id="e5a4a-159">店舗スケール ユニットに関連付けられたチャンネルは影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-159">Channels associated with Store Scale units are unaffected.</span></span>

<span data-ttu-id="e5a4a-160">移行プロセスはチャネルに対して透過的です。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-160">The migration process is transparent to the channels.</span></span> <span data-ttu-id="e5a4a-161">スケール ユニットの初期化が始まった後、次の操作が自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-161">After the scale unit initialization starts, the following operations are automatically performed:</span></span>

1. <span data-ttu-id="e5a4a-162">新しいクラウド スケール ユニットが作成され、環境に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-162">A new Cloud Scale Unit will be created and associated with the environment.</span></span>
2. <span data-ttu-id="e5a4a-163">クラウド スケール ユニットは、本社で利用可能なチャンネル データベースとして登録されます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-163">The Cloud Scale Unit will be registered as an available Channel Database in the headquarters.</span></span>
3. <span data-ttu-id="e5a4a-164">本社で **既定** のチャネル データベースにマップされたすべてのチャネルは、新しいクラウド スケール ユニットにマップするように更新されます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-164">All channels mapped to the **Default** channel database in the headquarters will be updated to map to the new Cloud Scale Unit.</span></span>
4. <span data-ttu-id="e5a4a-165">Commerce Data Exchange (CDX) 完全データ同期は、チャンネル データを新しいスケール ユニットに取り込むために実行されます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-165">A Commerce Data Exchange (CDX) full data sync will be performed to bring the channel data to the new scale unit.</span></span>

<span data-ttu-id="e5a4a-166">小売サーバーやクラウド販売時点管理を使用する店舗およびオンライン チャネルのすべての工程で、5 時間のダウンタイム ウィンドウを計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-166">You should plan for a five-hour downtime window for store and any online channel operations that use Retail Server or Cloud Point of Sale.</span></span>

<span data-ttu-id="e5a4a-167">このプロセスは、本番データを使用してデータベースを更新した後に、サンドボックス環境で初めて実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-167">This process should be first performed in a sandbox environment after a database refresh with production data is performed.</span></span> <span data-ttu-id="e5a4a-168">これにより業務検証が可能になり、移行プロセスにかかる時間についてのガイダンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-168">This will allow for business validations and will provide guidance on the amount of time the migration process will take.</span></span>

<span data-ttu-id="e5a4a-169">クラウド スケール ユニットは他のコンポーネントから専用の隔離された計算とストレージ リソースを提供するため、独自のチャネル データベースを持ちます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-169">Because the Cloud Scale Unit provides dedicated and isolated compute and storage resources from other components, it has its own channel database.</span></span> <span data-ttu-id="e5a4a-170">したがって、移行の前に次の対策を実行する必要があります:</span><span class="sxs-lookup"><span data-stu-id="e5a4a-170">This means the following precautions should be taken before migration:</span></span>

1. <span data-ttu-id="e5a4a-171">**POS のすべてのシフトがクローズしていることを確認してください。**</span><span class="sxs-lookup"><span data-stu-id="e5a4a-171">**Make sure that all shifts at the POS are closed.**</span></span> <span data-ttu-id="e5a4a-172">移行後、移行プロセス中に有効だったシフトを閉じることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-172">After migration, you won't be able to close any shifts that were active during the migration process</span></span>
2. <span data-ttu-id="e5a4a-173">**すべての P ジョブが正常に完了していることを確認します。**</span><span class="sxs-lookup"><span data-stu-id="e5a4a-173">**Make sure that all P-jobs have been successfully completed.**</span></span> <span data-ttu-id="e5a4a-174">前のチャンネル データベースが維持され、トランザクション データが本社との間で同期されている間、開始する前に P ジョブを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-174">While the previous channel database is maintained and any transactional data will still be synced back to the headquarters, it is recommended that you run P-JOBs before you start.</span></span>
3. <span data-ttu-id="e5a4a-175">**すべての POS デバイスからサインアウトします。**</span><span class="sxs-lookup"><span data-stu-id="e5a4a-175">**Sign out of all POS devices.**</span></span> <span data-ttu-id="e5a4a-176">POS 操作は移行中にサポートされません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-176">POS operations are not supported during migration</span></span>

<span data-ttu-id="e5a4a-177">初期化期間中に実行される内容を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-177">Here is what occurs during the initialization period:</span></span>

- <span data-ttu-id="e5a4a-178">POS オフライン機能を有効にしない限り、クラウドでホストされた小売チャネルは機能しません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-178">Cloud-hosted Retail channels won't work, unless you turn on POS offline capability.</span></span>
- <span data-ttu-id="e5a4a-179">オフライン機能がオンになっている POS デバイスは機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-179">POS devices with offline capability turned on will have reduced functionality.</span></span>
- <span data-ttu-id="e5a4a-180">Retail サーバーに依存しているすべての電子商取引クライアントが中断されます。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-180">Any e-Commerce clients that depend on Retail Server will be disrupted.</span></span>
- <span data-ttu-id="e5a4a-181">Retail Store Scale Unit でホストされているチャネルは影響されません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-181">Channels that are hosted on Retail Store Scale Units won't be affected.</span></span>
- <span data-ttu-id="e5a4a-182">本店機能は影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-182">Head office functionality is not affected.</span></span>

<span data-ttu-id="e5a4a-183">初期化が完了した後に起きる事柄を示します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-183">Here is what occurs after initialization is completed:</span></span>

- <span data-ttu-id="e5a4a-184">有効化されたすべての POS デバイスのデバイス有効化状態は保持されます。つまり、デバイスを再有効化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-184">The device activation state of all activated POS devices is preserved, which means that the devices won't have to be reactivated.</span></span>
- <span data-ttu-id="e5a4a-185">スタンドアロン ハードウェア ステーション インスタンスは引き続き機能します。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-185">Stand-alone hardware station instances will continue to work.</span></span>
- <span data-ttu-id="e5a4a-186">POS チャンネル側のレポートはリセットされ、データを初期化する前に表示されません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-186">POS channel–side reports will be reset and won't show data from before the initialization.</span></span>
- <span data-ttu-id="e5a4a-187">仕訳帳の処理の表示もリセットされるため、初期化前のデータは表示されません。</span><span class="sxs-lookup"><span data-stu-id="e5a4a-187">Show journal operation will also be reset and won't show data from before the initialization.</span></span>
