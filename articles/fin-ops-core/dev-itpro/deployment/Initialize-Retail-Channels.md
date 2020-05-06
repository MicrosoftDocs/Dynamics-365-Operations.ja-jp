---
title: Retail Cloud Scale Unit の初期化
description: このトピックでは、Retail Cloud Scale Unit を初期化する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: d442bbcd38d6ba193af1f98f0fd4f72bd45dead1
ms.sourcegitcommit: dad55d78c46278c9b27c7a37667b0317dede5eb2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2020
ms.locfileid: "3286728"
---
# <a name="initialize-retail-cloud-scale-unit"></a><span data-ttu-id="840e1-103">Retail Cloud Scale Unit の初期化</span><span class="sxs-lookup"><span data-stu-id="840e1-103">Initialize Retail Cloud Scale Unit</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="840e1-104">アプリケーション バージョン 8.1.2.x 以降を持つレベル 2 サンドボックスまたは運用環境を使用している場合、販売時点管理 (POS) 操作またはクラウド内の Retail サーバーを使用する電子商取引操作に Retail チャネル機能を使用する前に、Retail Cloud Scale Unit (RCSU) を初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="840e1-104">If you're using a Tier-2 sandbox or production environment that has application version 8.1.2.x or later, you must initialize Retail Cloud Scale Unit (RCSU) before you can use retail channel functionality either for point of sale (POS) operations or for e-Commerce operations that use Retail Server in the cloud.</span></span> <span data-ttu-id="840e1-105">初期化は Retail Cloud Scale Unit を展開します。</span><span class="sxs-lookup"><span data-stu-id="840e1-105">Initialization will deploy a Retail Cloud Scale Unit.</span></span>

<span data-ttu-id="840e1-106">このトピックでは、Retail Cloud Scale Unit を初期化するための手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="840e1-106">This topic describes the steps for initializing Retail Cloud Scale Unit.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="840e1-107">クラウドで小売チャネル機能を使用している既存の顧客の場合、業務の継続的かつ中断のないサポートを確保するには、Cloud Scale Unit を使用する小売チャネルの更新を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="840e1-107">For existing customers using retail channel functionality in the cloud, to ensure continued and uninterrupted support for your business, we require that you update your retail channels to use Cloud Scale Unit.</span></span> <span data-ttu-id="840e1-108">Cloud Scale Unit を使用せずに配置された新しい環境は、クラウド ホストの小売チャンネル コンポーネントの品質とサービスの更新を受けられなくなります。</span><span class="sxs-lookup"><span data-stu-id="840e1-108">New environments deployed without Cloud Scale Unit will no longer recieve quality and service updates for cloud-hosted retail channel components.</span></span> <span data-ttu-id="840e1-109">Store Scale Unit を独占して使用している顧客に対しては、アクションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="840e1-109">There is no action required for customers who exclusively use Store Scale Unit.</span></span>  <span data-ttu-id="840e1-110">延長が必要な場合は、Microsoft FastTrack ソリューション アーキテクトまでご連絡ください。</span><span class="sxs-lookup"><span data-stu-id="840e1-110">Contact your Microsoft FastTrack solution architect if you require an extension.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="840e1-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="840e1-111">Prerequisites</span></span>

1. <span data-ttu-id="840e1-112">アプリケーション バージョン 8.1.2.x またはそれ以降を持つレベル 2 サンドボックスまたは運協環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="840e1-112">Deploy a Tier-2 sandbox or production environment that has application version 8.1.2.x or later.</span></span>
2. <span data-ttu-id="840e1-113">Microsoft Dynamics Lifecycle Services (LCS) で環境ごとに 1 つを超える RCSU が必要な場合は、サポート要求を作成して、**複数の Retail Cloud Scale Unit に対するアクセス要求**を入力し、環境 ID、RCSU の数、および対応するデータ センター地域を指定します。</span><span class="sxs-lookup"><span data-stu-id="840e1-113">If you require more than 1 RCSU per environment, in Microsoft Dynamics Lifecycle Services (LCS), create a support request, and enter **Access request for multiple Retail Cloud Scale Units** and indicate the environment ID, number of RCSUs, and corresponding datacenter regions.</span></span> <span data-ttu-id="840e1-114">要求は、5 営業日以内に完了されます。</span><span class="sxs-lookup"><span data-stu-id="840e1-114">The request will be completed within five business days.</span></span> <span data-ttu-id="840e1-115">環境ごとに複数の RCSU を必要としない場合は、サポート要求を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="840e1-115">If you do not require multiple RCSUs per environment, you do not need to create a support request.</span></span> 

## <a name="initialize-retail-cloud-scale-unit-as-part-of-a-new-environment-deployment"></a><span data-ttu-id="840e1-116">Retail Cloud Scale Unit を新しい環境の展開の一部として初期化します</span><span class="sxs-lookup"><span data-stu-id="840e1-116">Initialize Retail Cloud Scale Unit as part of a new environment deployment</span></span>

<span data-ttu-id="840e1-117">本社が使用可能か確認してください。</span><span class="sxs-lookup"><span data-stu-id="840e1-117">Please make sure the headquarters is available.</span></span> <span data-ttu-id="840e1-118">これは、初期化プロセス中にスケール ユニットを本社に登録するために必要です。</span><span class="sxs-lookup"><span data-stu-id="840e1-118">This is required to register the scale unit with the headquarters during the initialization process.</span></span> <span data-ttu-id="840e1-119">サービス プロセスで利用できなくなる可能性があるため、本社がサービス中の場合はスケール ユニットの初期化をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="840e1-119">It is not recommended to initialize a scale unit when the headquarters is under servicing, as it may become unavailable during its servicing process.</span></span>

1. <span data-ttu-id="840e1-120">本社環境が使用可能で [メンテナンス モード](../sysadmin/maintenance-mode.md) でないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="840e1-120">Make sure the headquarters environment is available and not in [Maintenance mode](../sysadmin/maintenance-mode.md).</span></span>
2. <span data-ttu-id="840e1-121">LCS の環境の詳細 ページで、**環境機能 \> Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-121">In LCS, on the environment details page, select **Environment features \> Retail**.</span></span>
3. <span data-ttu-id="840e1-122">Retail 設定配置ページで、**初期化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-122">On the Retail setup deployment page, select **Initialize**.</span></span>
4. <span data-ttu-id="840e1-123">初期化する Retail Cloud Scale Unit のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-123">Select the version of the Retail Cloud Scale Unit to initialize.</span></span>
5. <span data-ttu-id="840e1-124">Retail Cloud Scale Unit を初期化するリージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-124">Select a region to initialize Retail Cloud Scale Unit in.</span></span>

## <a name="configure-retail-channels-to-use-retail-cloud-scale-unit"></a><span data-ttu-id="840e1-125">Retail Cloud Scale Unit を使用する小売チャネルの構成</span><span class="sxs-lookup"><span data-stu-id="840e1-125">Configure retail channels to use Retail Cloud Scale Unit</span></span>

1. <span data-ttu-id="840e1-126">Retail Cloud Scale Unit が展開された後で、本社のクライアントで **Retail とコマース > Retail Headquarters > Retail スケジューラの設定 > チャンネル データベース**の順に移動して、この Retail Cloud Scale Unit のためにデータベースを使用するように小売りチャンネルが構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="840e1-126">After Retail Cloud Scale Unit has been deployed, in the head office client go to **Retail and commerce > Retail Headquarters > Retail Scheduler setup > Channel database** to ensure that your retail channels are configured to use the database for this Retail Cloud Scale Unit.</span></span>
2. <span data-ttu-id="840e1-127">各小売りチャンネルに移動して、対応する Retail Cloud Scale Unit のチャンネル プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-127">Go to each retail channel and select the Channel Profile for the corresponding Retail Cloud Scale Unit.</span></span>

### <a name="database-refresh-and-cloud-scale-units"></a><span data-ttu-id="840e1-128">データベースの更新とクラウド スケール ユニット</span><span class="sxs-lookup"><span data-stu-id="840e1-128">Database refresh and Cloud Scale Units</span></span>

<span data-ttu-id="840e1-129">始める前に [コマース機能を使用する環境でデータベースを更新した後に完了する手順](../database/database-refresh.md) に精通していることを確認して下さい。</span><span class="sxs-lookup"><span data-stu-id="840e1-129">Before you begin, make sure you are familiar with [Steps to complete after a database refresh for environments that use Commerce functionality](../database/database-refresh.md).</span></span>

<span data-ttu-id="840e1-130">データベース更新の一部として (チャネル データベース フォームで) スケール ユニット チャネル データベース レコードを環境を越えて移動できません。</span><span class="sxs-lookup"><span data-stu-id="840e1-130">The scale unit channel database records (in the Channel Database form) cannot be moved across environments as part of database refresh.</span></span> <span data-ttu-id="840e1-131">これはレコードが環境固有のコンフィギュレーションを表すためです。</span><span class="sxs-lookup"><span data-stu-id="840e1-131">This is because the records represent environment specific configuration.</span></span>

<span data-ttu-id="840e1-132">データベースの更新後と Retail の再プロビジョニング ツールの実行後、LCS でスケール ユニットの再展開を発行して、スケール ユニットのチャネル データベース レコードを再生成できます。</span><span class="sxs-lookup"><span data-stu-id="840e1-132">After database refresh and after the Retail Reprovisioning tool has been executed, you can regenerate the scale unit's channel database record by issuing a re-deployment of your scale unit in LCS.</span></span> <span data-ttu-id="840e1-133">スケール ユニットで配置やサービス操作を行うと、登録が行われていないことが検出された場合に、本社でスケール ユニットが登録されます。</span><span class="sxs-lookup"><span data-stu-id="840e1-133">Any deployment or servicing operation in the scale unit will attempt to register the scale unit with the headquarters, if it detects that the registration is missing.</span></span>

<span data-ttu-id="840e1-134">スケール ユニットがすでに存在するのと同じバージョンの展開を選択することで、コンポーネントを変更することなくスケール ユニットの再配置を発行できます。</span><span class="sxs-lookup"><span data-stu-id="840e1-134">You can issue a re-deployment of the scale unit, without changing any components, by selecting to deploy the same version your scale unit is at already.</span></span> <span data-ttu-id="840e1-135">これは次の手順により LCS で行うことができます:</span><span class="sxs-lookup"><span data-stu-id="840e1-135">This can be done in LCS by the following steps:</span></span>

1. <span data-ttu-id="840e1-136">LCS の環境の詳細 ページで、**環境機能 \> Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-136">In LCS, on the environment details page, select **Environment features \> Retail**.</span></span>
2. <span data-ttu-id="840e1-137">設定の配置ページで再配置するスケール ユニットを選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-137">On the setup deployment page, select the scale unit you would like to redeploy.</span></span>
3. <span data-ttu-id="840e1-138">スケール ユニットの操作メニューで **更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-138">On the scale unit's operation menu, select **Update**</span></span>
4. <span data-ttu-id="840e1-139">スライダーの **バージョンの選択** のドロップダウンで **バージョンの指定** オプションを選択します</span><span class="sxs-lookup"><span data-stu-id="840e1-139">On the slider, on the drop-down for **Select version**, pick the option **Specify a version**</span></span>
5. <span data-ttu-id="840e1-140">**バージョンの指定** の下のテキスト ボックスに、スケール ユニットの **現在のバージョン** ラベルの横に表示されたバージョンを入力します。</span><span class="sxs-lookup"><span data-stu-id="840e1-140">On the text box under **Specify a version**, type in the version shown for your scale unit, shown besides the **Current version** label</span></span>
6. <span data-ttu-id="840e1-141">**更新** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="840e1-141">Click on **Update** button</span></span>

<span data-ttu-id="840e1-142">以前に拡張を適用した場合でも、スケール ユニットを更新するときに最後に適用された拡張パッケージが自動的に選択されるため、**拡張機能の更新** を選択する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="840e1-142">You do not need to select **Update extensions**, even if you have applied extensions previously, since the last extension package applied to the scale unit is automatically picked when updating a scale unit.</span></span>

<span data-ttu-id="840e1-143">複数のスケール ユニットがある場合は、各スケール ユニットに対して上記の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="840e1-143">If you have multiple scale units, you need to perform the operation above for each scale unit.</span></span> <span data-ttu-id="840e1-144">必要に応じて、これらの操作を並行して実行できます。</span><span class="sxs-lookup"><span data-stu-id="840e1-144">You may perform these operations in parallel, if desired.</span></span>

## <a name="deploy-additional-retail-cloud-scale-units-optional"></a><span data-ttu-id="840e1-145">追加の Retail Cloud Scale Unit を展開する (オプション)</span><span class="sxs-lookup"><span data-stu-id="840e1-145">Deploy additional Retail Cloud Scale Units (optional)</span></span>

<span data-ttu-id="840e1-146">最初の Retail Cloud Scale Unit (RCSU) を初期化した後、追加のクラウド スケール ユニットが必要な場合はサポート要求を入力します。</span><span class="sxs-lookup"><span data-stu-id="840e1-146">After you have initialized the first Retail Cloud Scale Unit (RCSU), if you require additional cloud scale units, enter a support request.</span></span> <span data-ttu-id="840e1-147">サポート要求で、必要な RCSU の数、環境名、希望するリージョンを明記します。</span><span class="sxs-lookup"><span data-stu-id="840e1-147">In the support request, state the number of RCSUs needed, environment name, and desired regions.</span></span>

<span data-ttu-id="840e1-148">展開する追加の RCSU ごとに、チャネル データ ベースグループを 個別に作成することもお勧めします。</span><span class="sxs-lookup"><span data-stu-id="840e1-148">For each additional RCSU that you deploy, it is also recommended that you create a separate channel database group for each RCSU.</span></span> <span data-ttu-id="840e1-149">これを行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="840e1-149">To do this, follow these steps:</span></span>

1. <span data-ttu-id="840e1-150">コマース バックオフィスで、**Retail とコマース > Retail Headquarters > Retail スケジューラの設定 > チャネル データベース グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="840e1-150">In Commerce head office, go to **Retail and commerce > Retail Headquarters > Retail Scheduler setup > Channel database group**.</span></span>
2. <span data-ttu-id="840e1-151">新しいチャネル データベース グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="840e1-151">Create a new channel database group.</span></span>
3. <span data-ttu-id="840e1-152">**Retail とコマース> Retail Headquarters > Retail スケジューラの設定 > チャネル データベース** フォームの順に移動し、新しく作成された RCSU に対応するチャネル データベースを選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-152">Go to the **Retail and commerce > Retail Headquarters > Retail Scheduler setup > Channel database** form and select the channel database that corresponds to the newly created RCSU.</span></span>
4. <span data-ttu-id="840e1-153">**編集** を選択して、新しいチャンネル データベース グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-153">Select **Edit** and select the new channel database group.</span></span>
5. <span data-ttu-id="840e1-154">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-154">Select **Save**.</span></span>
6. <span data-ttu-id="840e1-155">選択したチャンネル データベースに対して **完全データ同期の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="840e1-155">Select **Run Full data sync** for the selected channel database.</span></span>

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a><span data-ttu-id="840e1-156">既存の環境でクラウドにホストされたコマース チャネル コンポーネントを初期化する場合の追加の考慮事項</span><span class="sxs-lookup"><span data-stu-id="840e1-156">Additional considerations if you initialize cloud-hosted Commerce channel components in an existing environment</span></span>

<span data-ttu-id="840e1-157">環境でクラウドでホストされているコマース チャネル コンポーネントを既に使用している場合、Retail Cloud Scale Unit の初期化はそれらのコンポーネントの更新時にダウンタイムを減らすのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="840e1-157">If you're already using cloud-hosted Commerce channel components in an environment, initialization of Retail Cloud Scale Unit will help reduce the downtime when those components are updated.</span></span> <span data-ttu-id="840e1-158">Retail Cloud Scale Unit の初期化を行う前に、追加の計画が必要です。</span><span class="sxs-lookup"><span data-stu-id="840e1-158">Additional planning is required before initialization of Retail Cloud Scale Unit.</span></span>

<span data-ttu-id="840e1-159">クラウドでホストされたコマース チャネル コンポーネントを使用する環境で最初のクラウド スケール ユニットを初期化するときに、初期化プロセスではクラウドでホストされたチャネル コンポーネントに関連付けられているチャネルを最初のスケール ユニットに移行します。</span><span class="sxs-lookup"><span data-stu-id="840e1-159">When you initialize your first Cloud Scale Unit in an environment that uses cloud-hosted Commerce channel components, the initialization process will migrate your channels associated to the cloud-hosted channel components to the first scale unit.</span></span> <span data-ttu-id="840e1-160">店舗スケール ユニットに関連付けられたチャンネルは影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="840e1-160">Channels associated with Store Scale units are unaffected.</span></span>

<span data-ttu-id="840e1-161">移行プロセスはチャネルに対して透過的です。</span><span class="sxs-lookup"><span data-stu-id="840e1-161">The migration process is transparent to the channels.</span></span> <span data-ttu-id="840e1-162">スケール ユニットの初期化が始まった後、次の操作が自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="840e1-162">After the scale unit initialization starts, the following operations are automatically performed:</span></span>

1. <span data-ttu-id="840e1-163">新しいクラウド スケール ユニットが作成され、環境に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="840e1-163">A new Cloud Scale Unit will be created and associated with the environment.</span></span>
2. <span data-ttu-id="840e1-164">クラウド スケール ユニットは、本社で利用可能なチャンネル データベースとして登録されます。</span><span class="sxs-lookup"><span data-stu-id="840e1-164">The Cloud Scale Unit will be registered as an available Channel Database in the headquarters.</span></span>
3. <span data-ttu-id="840e1-165">本社で **既定** のチャネル データベースにマップされたすべてのチャネルは、新しいクラウド スケール ユニットにマップするように更新されます。</span><span class="sxs-lookup"><span data-stu-id="840e1-165">All channels mapped to the **Default** channel database in the headquarters will be updated to map to the new Cloud Scale Unit.</span></span>
4. <span data-ttu-id="840e1-166">Commerce Data Exchange (CDX) 完全データ同期は、チャンネル データを新しいスケール ユニットに取り込むために実行されます。</span><span class="sxs-lookup"><span data-stu-id="840e1-166">A Commerce Data Exchange (CDX) full data sync will be performed to bring the channel data to the new scale unit.</span></span>

<span data-ttu-id="840e1-167">小売サーバーやクラウド販売時点管理を使用する店舗およびオンライン チャネルのすべての工程で、5 時間のダウンタイム ウィンドウを計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="840e1-167">You should plan for a five-hour downtime window for store and any online channel operations that use Retail Server or Cloud Point of Sale.</span></span>

<span data-ttu-id="840e1-168">このプロセスは、本番データを使用してデータベースを更新した後に、サンドボックス環境で初めて実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="840e1-168">This process should be first performed in a sandbox environment after a database refresh with production data is performed.</span></span> <span data-ttu-id="840e1-169">これにより業務検証が可能になり、移行プロセスにかかる時間についてのガイダンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="840e1-169">This will allow for business validations and will provide guidance on the amount of time the migration process will take.</span></span>

<span data-ttu-id="840e1-170">クラウド スケール ユニットは他のコンポーネントから専用の隔離された計算とストレージ リソースを提供するため、独自のチャネル データベースを持ちます。</span><span class="sxs-lookup"><span data-stu-id="840e1-170">Because the Cloud Scale Unit provides dedicated and isolated compute and storage resources from other components, it has its own channel database.</span></span> <span data-ttu-id="840e1-171">したがって、移行の前に次の対策を実行する必要があります:</span><span class="sxs-lookup"><span data-stu-id="840e1-171">This means the following precautions should be taken before migration:</span></span>

1. <span data-ttu-id="840e1-172">**POS のすべてのシフトがクローズしていることを確認してください。**</span><span class="sxs-lookup"><span data-stu-id="840e1-172">**Make sure that all shifts at the POS are closed.**</span></span> <span data-ttu-id="840e1-173">移行後、移行プロセス中に有効だったシフトを閉じることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="840e1-173">After migration, you won't be able to close any shifts that were active during the migration process</span></span>
2. <span data-ttu-id="840e1-174">**すべての P ジョブが正常に完了していることを確認します。**</span><span class="sxs-lookup"><span data-stu-id="840e1-174">**Make sure that all P-jobs have been successfully completed.**</span></span> <span data-ttu-id="840e1-175">前のチャンネル データベースが維持され、トランザクション データが本社との間で同期されている間、開始する前に P ジョブを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="840e1-175">While the previous channel database is maintained and any transactional data will still be synced back to the headquarters, it is recommended that you run P-JOBs before you start.</span></span>
3. <span data-ttu-id="840e1-176">**すべての POS デバイスからサインアウトします。**</span><span class="sxs-lookup"><span data-stu-id="840e1-176">**Sign out of all POS devices.**</span></span> <span data-ttu-id="840e1-177">POS 操作は移行中にサポートされません。</span><span class="sxs-lookup"><span data-stu-id="840e1-177">POS operations are not supported during migration</span></span>

<span data-ttu-id="840e1-178">初期化期間中に実行される内容を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="840e1-178">Here is what occurs during the initialization period:</span></span>

- <span data-ttu-id="840e1-179">POS オフライン機能を有効にしない限り、クラウドでホストされたコマース チャネルは機能しません。</span><span class="sxs-lookup"><span data-stu-id="840e1-179">Cloud-hosted Commerce channels won't work, unless you turn on POS offline capability.</span></span>
- <span data-ttu-id="840e1-180">オフライン機能がオンになっている POS デバイスは機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="840e1-180">POS devices with offline capability turned on will have reduced functionality.</span></span>
- <span data-ttu-id="840e1-181">Retail サーバーに依存しているすべての電子商取引クライアントが中断されます。</span><span class="sxs-lookup"><span data-stu-id="840e1-181">Any e-Commerce clients that depend on Retail Server will be disrupted.</span></span>
- <span data-ttu-id="840e1-182">Retail Store Scale Unit でホストされているチャネルは影響されません。</span><span class="sxs-lookup"><span data-stu-id="840e1-182">Channels that are hosted on Retail Store Scale Units won't be affected.</span></span>
- <span data-ttu-id="840e1-183">本店機能は影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="840e1-183">Head office functionality is not affected.</span></span>

<span data-ttu-id="840e1-184">初期化が完了した後に起きる事柄を示します。</span><span class="sxs-lookup"><span data-stu-id="840e1-184">Here is what occurs after initialization is completed:</span></span>

- <span data-ttu-id="840e1-185">有効化されたすべての POS デバイスのデバイス有効化状態は保持されます。つまり、デバイスを再有効化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="840e1-185">The device activation state of all activated POS devices is preserved, which means that the devices won't have to be reactivated.</span></span>
- <span data-ttu-id="840e1-186">スタンドアロン ハードウェア ステーション インスタンスは引き続き機能します。</span><span class="sxs-lookup"><span data-stu-id="840e1-186">Stand-alone hardware station instances will continue to work.</span></span>
- <span data-ttu-id="840e1-187">POS チャンネル側のレポートはリセットされ、データを初期化する前に表示されません。</span><span class="sxs-lookup"><span data-stu-id="840e1-187">POS channel–side reports will be reset and won't show data from before the initialization.</span></span>
- <span data-ttu-id="840e1-188">仕訳帳の処理の表示もリセットされるため、初期化前のデータは表示されません。</span><span class="sxs-lookup"><span data-stu-id="840e1-188">Show journal operation will also be reset and won't show data from before the initialization.</span></span>
