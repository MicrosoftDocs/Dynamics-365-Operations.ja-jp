---
title: チャネルを別の Commerce Scale Unit に移行する
description: このトピックでは、Microsoft Dynamics 365 Commerce チャネルを別の Commerce Scale Unit に移行する方法について説明します。
author: AamirAllaq
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 04765c4c397a5bed082b4f8ec98355a09b138f4e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745337"
---
# <a name="migrate-channels-to-a-different-commerce-scale-unit"></a><span data-ttu-id="b3f0b-103">チャネルを別の Commerce Scale Unit に移行する</span><span class="sxs-lookup"><span data-stu-id="b3f0b-103">Migrate channels to a different Commerce Scale Unit</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b3f0b-104">このトピックでは、Microsoft Dynamics 365 Commerce ストア チャネルを、現在使用している Commerce Scale Unit (CSU) から別の CSU に移行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-104">This topic explains how to migrate Microsoft Dynamics 365 Commerce store channels from the Commerce Scale Unit (CSU) that they are currently working with to a different CSU.</span></span> <span data-ttu-id="b3f0b-105">チャネル間の負荷の分離とリソース ガバナンスの向上のためにチャネルを別の CSU に移行して、店舗への待ち時間を減らしたり、またはロールアウトとパイロットのステージングのために別の更新や拡張機能の展開スケジュールを管理することがあります。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-105">You might want to migrate channels to a different CSU for better load isolation and resource governance between channels, to reduce latency to your stores, or to manage different update/extension deployment schedules for staged roll-out and pilots.</span></span> <span data-ttu-id="b3f0b-106">異なる CSU への移行には、チャネルのダウンタイムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-106">Migration to a different CSU involves downtime for the channels.</span></span>

<span data-ttu-id="b3f0b-107">このトピックでは、チャネル移行中の業務の中断とダウンタイムを最小限に抑えるのに役立つベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-107">This topic describes best practices that will help you minimize business disruption and downtime while you migrate channels.</span></span> <span data-ttu-id="b3f0b-108">これは、クラウドでホストされた CSU 間、自己ホストの CSU 間、クラウドでホストされた CSU から自己ホストの CSU、および自己ホストの CSU からクラウドでホストされた CSU へのチャネルの移行に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-108">It applies to the migration of channels between cloud-hosted CSUs, between self-hosted CSUs, from cloud-hosted CSUs to self-hosted CSUs, and from self-hosted CSUs to cloud-hosted CSUs.</span></span>

> [!NOTE]
> <span data-ttu-id="b3f0b-109">移行の前に、CSU 間、仕訳帳レコードで使用されていた一時的な販売データ、および販売時点管理 (POS) レポートでチャネルを移行すると、移行後は POS で使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-109">If you migrate channels between CSUs, temporary sales data that was used for journal records and point of sale (POS) reports before the migration will no longer be available at the POS after migration.</span></span> <span data-ttu-id="b3f0b-110">移行が完了した後は、新しいデータを使用して、仕訳帳とチャネル レポートが開始されます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-110">After the migration is completed, journals and channel reports will be started afresh by using new data.</span></span>

<span data-ttu-id="b3f0b-111">次の手順において、*出力元* と *出力先* という用語は、移行に含まれる CSU と対応するチャネル データベースを区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-111">In the following procedures, the terms *origin* and *destination* are used to distinguish the CSUs and corresponding channel databases that are involved in the migration.</span></span>

## <a name="planning-for-downtime"></a><span data-ttu-id="b3f0b-112">ダウンタイムの計画</span><span class="sxs-lookup"><span data-stu-id="b3f0b-112">Planning for downtime</span></span>

<span data-ttu-id="b3f0b-113">このトピックで説明する手順に従うと、関連する実行時間の長いシステム プロセスはすべて実際の移行の前に実行されますが、その間、店舗は運営することができます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-113">When you follow the procedures that are described in this topic, all long-running system processes that are involved are run before the actual migration, while the stores are still operational.</span></span> <span data-ttu-id="b3f0b-114">これらのプロセスには、製品、価格、および顧客のマスター データの同期が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-114">These processes including synchronization of master data for products, prices, and customers.</span></span> <span data-ttu-id="b3f0b-115">次に、移行中、環境のダウンタイムを計画する必要がある重要な期間には、新しい CSU に対するチャンネル コンフィギュレーション データの小さなペイロードの同期が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-115">Then, during the migration, the critical period when you must take planned downtime in your environment involves data synchronization of a very small payload of channel configuration data to the new CSU.</span></span> <span data-ttu-id="b3f0b-116">ほとんどの場合、この同期は 10 分以内に完了することができます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-116">In most cases, this synchronization can be completed in under 10 minutes.</span></span> <span data-ttu-id="b3f0b-117">ただし、運用上の視点から、前提条件となる手順すべてを完了するのに十分な時間があるよう、より長いダウンタイム ウィンドウを計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-117">However, from an operational perspective, you must plan for a longer downtime window to ensure that all prerequisite steps have enough time to be completed.</span></span> <span data-ttu-id="b3f0b-118">この手順には、すべてのシフトのクローズ、Commerce 本社へのトランザクションの同期、およびステートメントの転記が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-118">These steps include closing all shifts, syncing transactions to Commerce headquarters, and posting statements.</span></span> <span data-ttu-id="b3f0b-119">必要な合計時間は組織ごとに異なります。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-119">The amount of time that is required will vary by organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b3f0b-120">必要条件</span><span class="sxs-lookup"><span data-stu-id="b3f0b-120">Prerequisites</span></span>

<span data-ttu-id="b3f0b-121">最初に、サンドボックスのユーザー受け入れテスト (UAT) 環境で、次のすべての手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-121">First, complete all the following procedures in a sandbox user acceptance testing (UAT) environment.</span></span> <span data-ttu-id="b3f0b-122">次に、運用環境で手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-122">Then repeat them in your production environment.</span></span> <span data-ttu-id="b3f0b-123">このようにして、運用環境で予想されるダウンタイムの測定および見積ができます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-123">In this way, you can measure and estimate the downtime that you should expect in the production environment.</span></span>

## <a name="migration"></a><span data-ttu-id="b3f0b-124">移行</span><span class="sxs-lookup"><span data-stu-id="b3f0b-124">Migration</span></span>

### <a name="configure-data-synchronization"></a><span data-ttu-id="b3f0b-125">データ同期のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b3f0b-125">Configure data synchronization</span></span>

<span data-ttu-id="b3f0b-126">次の手順は、店舗がまだ運営中の間に完了することができます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-126">The following steps can be completed while the stores are still operational.</span></span> <span data-ttu-id="b3f0b-127">マスター データを出力先の CSU に同期します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-127">They synchronize master data to the destination CSU.</span></span>

1. <span data-ttu-id="b3f0b-128">Commerce 本社の **チャネル データベース** ページで、出力先 CSU のチャネル データベースのレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-128">In Commerce headquarters, on the **Channel database** page, select the record for the channel database for the destination CSU.</span></span> 
2. <span data-ttu-id="b3f0b-129">目的のチャネルを出力先のチャネル データベースに追加します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-129">Add the desired channels to the destination channel database.</span></span>
3. <span data-ttu-id="b3f0b-130">**完全なデータの同期** を選択し、ジョブ **9999** (**すべてのジョブ**) を使用するように指定します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-130">Select **Full data sync**, and specify that job **9999** (**All jobs**) should be used.</span></span>

> [!NOTE]
> <span data-ttu-id="b3f0b-131">出力先の CSU が自己ホストの場合、個別のチャネル データベース グループを作成して、不要なマスター データ同期量を減らすことを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-131">If your destination CSU is self-hosted, consider creating separate channel database groups to reduce the volume of unnecessary master data synchronization.</span></span> 

### <a name="prepare-for-migration"></a><span data-ttu-id="b3f0b-132">移行の準備</span><span class="sxs-lookup"><span data-stu-id="b3f0b-132">Prepare for migration</span></span>

<span data-ttu-id="b3f0b-133">この手順と次の手順は、チャネルに計画されたダウンタイムの間に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-133">This procedure and the next procedure must be completed during the planned downtime for your channels.</span></span>

1. <span data-ttu-id="b3f0b-134">すべての POS デバイスで、シフトすべてがクローズされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-134">On all POS devices, make sure that all shifts are closed.</span></span>
2. <span data-ttu-id="b3f0b-135">すべての POS デバイスからサインアウトします。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-135">Sign out of all POS devices.</span></span>
3. <span data-ttu-id="b3f0b-136">すべての POS オフライン トランザクションが Commerce 本社に同期されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-136">Confirm that all POS offline transactions are synced to Commerce headquarters.</span></span> <span data-ttu-id="b3f0b-137">移行するすべての既存のチャネル データベースに対して、P ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-137">Run P-jobs for all existing channel databases that will be migrated.</span></span> <span data-ttu-id="b3f0b-138">P ジョブが完了する前に移行を開始し、クラウド POS を使用している場合、トランザクション番号が重複するためにトランザクションが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-138">If you start the migration before P-jobs are completed, and if you use Cloud POS, you might lose transactions because of duplicate transaction numbers.</span></span>
4. <span data-ttu-id="b3f0b-139">すべてのステートメントが転記されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-139">Confirm that all statements are posted.</span></span>

### <a name="migrate-channels-to-a-new-csu"></a><span data-ttu-id="b3f0b-140">チャネルを新しい CSU に移行する</span><span class="sxs-lookup"><span data-stu-id="b3f0b-140">Migrate channels to a new CSU</span></span>

1. <span data-ttu-id="b3f0b-141">**店舗の詳細** ページで、**ライブ チャネル データベース** フィールドを送信先 CSU データベースに設定します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-141">On the **Store details** page, set the **Live channel database** field to the destination CSU database.</span></span>
2. <span data-ttu-id="b3f0b-142">**チャネル プロファイル** フィールドを、送信先の CSU に関連付けられているチャネル プロファイルに設定します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-142">Set the **Channel profile** field to the channel profile that is associated with the destination CSU.</span></span>
3. <span data-ttu-id="b3f0b-143">**配送スケジュール** ページで、ジョブ **1070** ( **チャネル構成ジョブ**) とジョブ **1110** (**グローバル構成ジョブ**) を実行します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-143">On the **Distribution schedule** page, run job **1070** (**Channel configuration job**) and job **1110** (**Global configuration job**).</span></span> <span data-ttu-id="b3f0b-144">各ジョブに対して **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-144">Select **Run now** for each job.</span></span> <span data-ttu-id="b3f0b-145">(非同期処理については、**今すぐ実行** の代わりに **バッチ ジョブの作成** を選択します。) ジョブが完了した後、チャネルは新しい CSU に移行されています。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-145">(For asynchronous processing, select **Create batch job** instead of **Run now**.) After the jobs are completed, your channels have been migrated to the new CSU.</span></span>
4. <span data-ttu-id="b3f0b-146">クラウド POS を使用している場合、新しい CSU のためのクラウド POS の URL を使用して、POS デバイスの最有効化を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-146">If you're using Cloud POS, you must use the URL of Cloud POS for the new CSU and reactivate the POS device.</span></span> <span data-ttu-id="b3f0b-147">送信元のチャネル データベースのすべての P ジョブが完了する前に POS デバイスの最有効化を実行すると、トランザクション番号が重複するためにトランザクションが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-147">If you reactivate the POS device before all P-jobs on the origin channel database are completed, you might lose transactions because of duplicate transaction numbers.</span></span>

    <span data-ttu-id="b3f0b-148">Modern POS を使用している場合、各 POS デバイスを閉じ、再度開いてサインインします。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-148">If you're using Modern POS, close each POS device, reopen it, and sign in.</span></span>

## <a name="post-migration"></a><span data-ttu-id="b3f0b-149">移行後</span><span class="sxs-lookup"><span data-stu-id="b3f0b-149">Post-migration</span></span>

<span data-ttu-id="b3f0b-150">引き続き、元の CSU を使用して、他のチャネルのサービスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-150">You can continue to use the origin CSU to serve other channels.</span></span> 

> [!NOTE]
> <span data-ttu-id="b3f0b-151">元の CSU を削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-151">Do not delete the origin CSU.</span></span> <span data-ttu-id="b3f0b-152">これを行うと、店舗を開けなくなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-152">Doing so may make the store unoperable.</span></span>

<span data-ttu-id="b3f0b-153">サンドボックス UAT 環境ですべての手順を完了した後、運用環境で同じ手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b3f0b-153">After you've completed all the procedures in a sandbox UAT environment, repeat them in your production environment.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]