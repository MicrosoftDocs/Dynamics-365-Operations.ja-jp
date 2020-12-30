---
title: 計画の最適化の使用を開始する
description: このトピックでは、計画の最適化機能の使用を開始する方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432409"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="30351-103">計画最適化の開始</span><span class="sxs-lookup"><span data-stu-id="30351-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30351-104">[すでに発表した](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) ように、計画の最適化は、既存の組み込みマスター プラン エンジンと置き換えるようにスケジュールされています。</span><span class="sxs-lookup"><span data-stu-id="30351-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="30351-105">現在、組み込みのマスター プラン エンジンを使用している場合は、すぐに計画の最適化への移行の計画を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30351-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="30351-106">廃止が適用されると操作が影響を受ける可能性があるため、移行プロセスをすぐに開始することが重要です。</span><span class="sxs-lookup"><span data-stu-id="30351-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="30351-107">廃止が実施された場合に、最新の問題を回避するために、2020 年 12 月 1 日までに移行を完了することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="30351-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="30351-108">現時点では、計画の最適化機能では、Supply Chain Management に組み込まれている計画エンジンで利用可能なすべての機能がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="30351-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="30351-109">したがって、計画の最適化で現在利用可能な機能セットが要件を満たすかどうかを評価することが重要です。</span><span class="sxs-lookup"><span data-stu-id="30351-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="30351-110">現在、計画の最適化機能は Dynamics Lifecycle Services (LCS) で既定では有効になっていないため、機能を有効にする前に評価を行う機会があります。</span><span class="sxs-lookup"><span data-stu-id="30351-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="30351-111">マスター プラン プロセスに製造が含まれていない (マスター プランで生成された計画製造オーダー) 場合や、バージョン 10.0.15 以降の組み込みマスター プラン エンジンが必要な場合は、移行から計画の最適化に例外を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30351-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="30351-112">バージョン 10.0.16 以降、計画製造オーダーを生成せずに組み込みマスター プランを実行すると、環境にエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="30351-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="30351-113">計画製造オーダーは、マスター プラン中に計画製造オーダーを生成しないすべての新しい配置に対して使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30351-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="30351-114">計画製造オーダーを生成せずに組み込みマスター プラン エンジンを実行している既存の環境の所有者は、例外プロセスに関する詳細を含むメールを受信します。</span><span class="sxs-lookup"><span data-stu-id="30351-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="30351-115">パートナーと協力して、計画の最適化への移行を評価および計画することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="30351-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="30351-116">計画の最適化を有効にする前に、計画の最適化フィット分析の結果を評価することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="30351-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="30351-117">詳細については、[計画の最適化フィット分析](planning-optimization-fit-analysis.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30351-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="30351-118">使用可能性</span><span class="sxs-lookup"><span data-stu-id="30351-118">Availability</span></span>
<span data-ttu-id="30351-119">計画の最適化はは現在、次の Azure の地域で利用可能です：米国、カナダ、ヨーロッパ、英国、オーストラリア。</span><span class="sxs-lookup"><span data-stu-id="30351-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="30351-120">他の地域からのアドインをインストールしようとすると、LCS ではこの地理的領域には対応していない旨のメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="30351-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="30351-121">計画の最適化では、 Dynamics 365 Supply Chain Management の社内設置型の配置に対応していないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="30351-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="30351-122">ライセンス</span><span class="sxs-lookup"><span data-stu-id="30351-122">Licensing</span></span>

<span data-ttu-id="30351-123">現在のライセンスを使用してマスター プランを実行できる場合は、計画の最適化の使用を開始するために追加のライセンスを購入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="30351-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="30351-124">アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="30351-124">Install the add-in</span></span>

<span data-ttu-id="30351-125">計画の最適化を使用するには、Dynamics 365 Supply Chain Management 用の計画の最適化アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="30351-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="30351-126">LCS プロジェクトからアドインにアクセスし、Supply Chain Management ユーザーインターフェイス (UI) から計画の最適化機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="30351-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="30351-127">計画最適化の要件は、LCS が有効になっている高可用性環境の tier 2 またはそれ以降で、(OneBox 環境ではなく) Dynamics 365 Supply Chain Management バージョン 10.0.7 、またはそれ以降です。</span><span class="sxs-lookup"><span data-stu-id="30351-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="30351-128">このアドインを OneBox 環境にインストールはできません。インストール処理をキャンセルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="30351-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="30351-129">LCS にサインインし、目的の環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="30351-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="30351-130">**完全な詳細** に移動します。</span><span class="sxs-lookup"><span data-stu-id="30351-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="30351-131">**環境アドイン** クイック タブまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="30351-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="30351-132">**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="30351-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="30351-133">**計画の最適化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="30351-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="30351-134">インストール ガイドに従って、契約条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="30351-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="30351-135">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="30351-135">Select **Install**.</span></span>
1. <span data-ttu-id="30351-136">**環境アドイン** クイック タブに、計画最適化がインストールされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30351-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="30351-137">数分後、**インストールしています** が **インストール済み** に変わります (ページを更新する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="30351-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="30351-138">インストールすると、Dynamics 365 Supply Chain Management で計画最適化を有効にする準備が整います。</span><span class="sxs-lookup"><span data-stu-id="30351-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="30351-139">計画の最適化アドインをインストールする主な目的は、サービスと環境をつなげることです。</span><span class="sxs-lookup"><span data-stu-id="30351-139">The main purpose of installing the Planning Optimization add-in is to connect the service and the environment.</span></span> <span data-ttu-id="30351-140">したがって、環境間で移動したコードに関係なく、計画の最適化を使用する環境ごとにアドインを個別にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="30351-140">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="30351-141">計画の最適化の統合</span><span class="sxs-lookup"><span data-stu-id="30351-141">Planning Optimization integration</span></span>

<span data-ttu-id="30351-142">計画の最適化アドインをマスター プランに使用するかどうかを構成するには、**マスター プラン** \> **セットアップ** \> **計画最適化パラメーター** の順に進みます。</span><span class="sxs-lookup"><span data-stu-id="30351-142">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="30351-143">接続状態</span><span class="sxs-lookup"><span data-stu-id="30351-143">Connection status</span></span>

<span data-ttu-id="30351-144">接続ステータスは、Supply Chain Management と計画の最適化サービスとの間の接続の現在のステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="30351-144">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="30351-145">次の表は、使用可能な値を示しています。</span><span class="sxs-lookup"><span data-stu-id="30351-145">The following table shows the possible values.</span></span>

| <span data-ttu-id="30351-146">接続状態</span><span class="sxs-lookup"><span data-stu-id="30351-146">Connection status</span></span> | <span data-ttu-id="30351-147">説明</span><span class="sxs-lookup"><span data-stu-id="30351-147">Description</span></span> | <span data-ttu-id="30351-148">計画の最適化は使用できますか?</span><span class="sxs-lookup"><span data-stu-id="30351-148">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="30351-149">接続済</span><span class="sxs-lookup"><span data-stu-id="30351-149">Connected</span></span> | <span data-ttu-id="30351-150">計画の最適化サービスと Supply Chain Management の間に接続が確立されています。</span><span class="sxs-lookup"><span data-stu-id="30351-150">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="30351-151">はい</span><span class="sxs-lookup"><span data-stu-id="30351-151">Yes</span></span> |
| <span data-ttu-id="30351-152">接続の有効化</span><span class="sxs-lookup"><span data-stu-id="30351-152">Enabling connection</span></span> | <span data-ttu-id="30351-153">計画の最適化サービスへの接続を有効にする要求が現在進行中です。</span><span class="sxs-lookup"><span data-stu-id="30351-153">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="30351-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="30351-154">No</span></span> |
| <span data-ttu-id="30351-155">接続解除済</span><span class="sxs-lookup"><span data-stu-id="30351-155">Disconnected</span></span> | <span data-ttu-id="30351-156">計画の最適化サービスへの接続はありません。</span><span class="sxs-lookup"><span data-stu-id="30351-156">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="30351-157">このトピックで前述されているように、LCS から接続をオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="30351-157">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="30351-158">いいえ</span><span class="sxs-lookup"><span data-stu-id="30351-158">No</span></span> |
| <span data-ttu-id="30351-159">接続を無効にしています</span><span class="sxs-lookup"><span data-stu-id="30351-159">Disabling connection</span></span> | <span data-ttu-id="30351-160">計画の最適化サービスへの接続をオフにする要求が現在進行中です。</span><span class="sxs-lookup"><span data-stu-id="30351-160">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="30351-161">いいえ</span><span class="sxs-lookup"><span data-stu-id="30351-161">No</span></span> |
| <span data-ttu-id="30351-162">状態を取得しています</span><span class="sxs-lookup"><span data-stu-id="30351-162">Getting status</span></span> | <span data-ttu-id="30351-163">システムは、計画の最適化サービスからのステータス情報を待機しています。</span><span class="sxs-lookup"><span data-stu-id="30351-163">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="30351-164">いいえ</span><span class="sxs-lookup"><span data-stu-id="30351-164">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="30351-165">計画の最適化の使用オプション</span><span class="sxs-lookup"><span data-stu-id="30351-165">The Use Planning Optimization option</span></span>

<span data-ttu-id="30351-166">**計画の最適化の使用** オプションの設定では、マスター プランに使用する計画エンジンを決定します。</span><span class="sxs-lookup"><span data-stu-id="30351-166">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="30351-167">**はい** – 計画の最適化がマスター プランに使用されます。</span><span class="sxs-lookup"><span data-stu-id="30351-167">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="30351-168">**いいえ** – 組み込み Supply Chain Management 計画エンジンがマスター プランに使用されます。</span><span class="sxs-lookup"><span data-stu-id="30351-168">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="30351-169">**計画の最適化の使用** オプションが **はい** に設定されているときに、組み込みの Supply Chain Management 計画エンジンに対して作成された既存の計画バッチ ジョブがトリガーされた場合、これらのジョブは失敗します。</span><span class="sxs-lookup"><span data-stu-id="30351-169">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="30351-170">設定との統合</span><span class="sxs-lookup"><span data-stu-id="30351-170">Integration with the setup</span></span>

<span data-ttu-id="30351-171">計画の最適化が有効になっている場合は、計画の最適化アドインを使用してマスター プランが実行されます。</span><span class="sxs-lookup"><span data-stu-id="30351-171">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="30351-172">この場合、マスター プランの結果と機能が影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="30351-172">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30351-173">追加リソース</span><span class="sxs-lookup"><span data-stu-id="30351-173">Additional resources</span></span>

[<span data-ttu-id="30351-174">プレビュー用の使用条件</span><span class="sxs-lookup"><span data-stu-id="30351-174">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="30351-175">計画最適化の概要</span><span class="sxs-lookup"><span data-stu-id="30351-175">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="30351-176">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="30351-176">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="30351-177">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="30351-177">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="30351-178">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="30351-178">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="30351-179">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="30351-179">Cancel a planning job</span></span>](cancel-planning-job.md)
