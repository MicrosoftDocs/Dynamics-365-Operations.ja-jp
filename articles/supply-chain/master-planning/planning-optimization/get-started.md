---
title: 計画の最適化の使用を開始する
description: このトピックでは、計画の最適化機能の使用を開始する方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
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
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887267"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="1b73b-103">計画の最適化の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="1b73b-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b73b-104">現時点では、計画の最適化機能では、Microsoft Dynamics 365 Supply Chain Management に組み込まれている計画エンジンで利用可能なすべての機能がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1b73b-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1b73b-105">したがって、計画の最適化で現在利用可能な機能セットが要件を満たすかどうかを評価することが重要です。</span><span class="sxs-lookup"><span data-stu-id="1b73b-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="1b73b-106">既定では、Dynamics Lifecycle Services (LCS) で、計画の最適化機能は有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="1b73b-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="1b73b-107">したがって、オンにする前に評価を行う機会があります。</span><span class="sxs-lookup"><span data-stu-id="1b73b-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="1b73b-108">最終的に、既存の組み込み Supply Chain Management 計画エンジンは、計画の最適化によって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="1b73b-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="1b73b-109">計画の最適化を有効にする前に、計画の最適化フィット分析の結果を評価することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1b73b-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="1b73b-110">詳細については、[計画の最適化フィット分析](planning-optimization-fit-analysis.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b73b-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="1b73b-111">使用可能性</span><span class="sxs-lookup"><span data-stu-id="1b73b-111">Availability</span></span>
<span data-ttu-id="1b73b-112">計画の最適化はは現在、次の Azure の地域で利用可能です：米国、カナダ、ヨーロッパ、英国、オーストラリア。</span><span class="sxs-lookup"><span data-stu-id="1b73b-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="1b73b-113">他の地域からのアドインをインストールしようとすると、LCS ではこの地理的領域には対応していない旨のメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="1b73b-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="1b73b-114">計画の最適化では、 Dynamics 365 Supply Chain Management の社内設置型の配置に対応していないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1b73b-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="1b73b-115">ライセンス</span><span class="sxs-lookup"><span data-stu-id="1b73b-115">Licensing</span></span>

<span data-ttu-id="1b73b-116">現在のライセンスを使用してマスター プランを実行できる場合は、計画の最適化の使用を開始するために追加のライセンスを購入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1b73b-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="1b73b-117">アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="1b73b-117">Install the add-in</span></span>

<span data-ttu-id="1b73b-118">計画の最適化を使用するには、Dynamics 365 Supply Chain Management 用の計画の最適化アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="1b73b-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1b73b-119">LCS プロジェクトからアドインにアクセスし、Supply Chain Management ユーザーインターフェイス (UI) から計画の最適化機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1b73b-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="1b73b-120">計画最適化の要件は、LCS が有効になっている高可用性環境の tier 2 またはそれ以降で、(OneBox 環境ではなく) Dynamics 365 Supply Chain Management バージョン 10.0.7 、またはそれ以降です。</span><span class="sxs-lookup"><span data-stu-id="1b73b-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="1b73b-121">このアドインを OneBox 環境にインストールはできません。インストール処理をキャンセルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b73b-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="1b73b-122">LCS にサインインし、目的の環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="1b73b-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="1b73b-123">**完全な詳細**に移動します。</span><span class="sxs-lookup"><span data-stu-id="1b73b-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="1b73b-124">**環境アドイン** クイック タブまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="1b73b-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="1b73b-125">**新しいアドインのインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b73b-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="1b73b-126">**計画の最適化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b73b-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="1b73b-127">インストール ガイドに従って、契約条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="1b73b-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="1b73b-128">**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b73b-128">Select **Install**.</span></span>
1. <span data-ttu-id="1b73b-129">**環境アドイン** クイック タブに、計画最適化がインストールされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b73b-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="1b73b-130">数分後、**インストールしています**が**インストール済み**に変わります (ページを更新する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="1b73b-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="1b73b-131">インストールすると、Dynamics 365 Supply Chain Management で計画最適化を有効にする準備が整います。</span><span class="sxs-lookup"><span data-stu-id="1b73b-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="1b73b-132">計画の最適化の統合</span><span class="sxs-lookup"><span data-stu-id="1b73b-132">Planning Optimization integration</span></span>

<span data-ttu-id="1b73b-133">計画の最適化アドインをマスター プランに使用するかどうかを構成するには、**マスター プラン** \> **セットアップ** \> **計画最適化パラメーター**の順に進みます。</span><span class="sxs-lookup"><span data-stu-id="1b73b-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="1b73b-134">接続状態</span><span class="sxs-lookup"><span data-stu-id="1b73b-134">Connection status</span></span>

<span data-ttu-id="1b73b-135">接続ステータスは、Supply Chain Management と計画の最適化サービスとの間の接続の現在のステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="1b73b-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="1b73b-136">次の表は、使用可能な値を示しています。</span><span class="sxs-lookup"><span data-stu-id="1b73b-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="1b73b-137">接続状態</span><span class="sxs-lookup"><span data-stu-id="1b73b-137">Connection status</span></span> | <span data-ttu-id="1b73b-138">説明</span><span class="sxs-lookup"><span data-stu-id="1b73b-138">Description</span></span> | <span data-ttu-id="1b73b-139">計画の最適化は使用できますか?</span><span class="sxs-lookup"><span data-stu-id="1b73b-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="1b73b-140">接続済</span><span class="sxs-lookup"><span data-stu-id="1b73b-140">Connected</span></span> | <span data-ttu-id="1b73b-141">計画の最適化サービスと Supply Chain Management の間に接続が確立されています。</span><span class="sxs-lookup"><span data-stu-id="1b73b-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="1b73b-142">はい</span><span class="sxs-lookup"><span data-stu-id="1b73b-142">Yes</span></span> |
| <span data-ttu-id="1b73b-143">接続の有効化</span><span class="sxs-lookup"><span data-stu-id="1b73b-143">Enabling connection</span></span> | <span data-ttu-id="1b73b-144">計画の最適化サービスへの接続を有効にする要求が現在進行中です。</span><span class="sxs-lookup"><span data-stu-id="1b73b-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1b73b-145">いいえ</span><span class="sxs-lookup"><span data-stu-id="1b73b-145">No</span></span> |
| <span data-ttu-id="1b73b-146">接続解除済</span><span class="sxs-lookup"><span data-stu-id="1b73b-146">Disconnected</span></span> | <span data-ttu-id="1b73b-147">計画の最適化サービスへの接続はありません。</span><span class="sxs-lookup"><span data-stu-id="1b73b-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="1b73b-148">このトピックで前述されているように、LCS から接続をオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="1b73b-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="1b73b-149">いいえ</span><span class="sxs-lookup"><span data-stu-id="1b73b-149">No</span></span> |
| <span data-ttu-id="1b73b-150">接続を無効にしています</span><span class="sxs-lookup"><span data-stu-id="1b73b-150">Disabling connection</span></span> | <span data-ttu-id="1b73b-151">計画の最適化サービスへの接続をオフにする要求が現在進行中です。</span><span class="sxs-lookup"><span data-stu-id="1b73b-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1b73b-152">いいえ</span><span class="sxs-lookup"><span data-stu-id="1b73b-152">No</span></span> |
| <span data-ttu-id="1b73b-153">状態を取得しています</span><span class="sxs-lookup"><span data-stu-id="1b73b-153">Getting status</span></span> | <span data-ttu-id="1b73b-154">システムは、計画の最適化サービスからのステータス情報を待機しています。</span><span class="sxs-lookup"><span data-stu-id="1b73b-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="1b73b-155">いいえ</span><span class="sxs-lookup"><span data-stu-id="1b73b-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="1b73b-156">計画の最適化の使用オプション</span><span class="sxs-lookup"><span data-stu-id="1b73b-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="1b73b-157">**計画の最適化の使用**オプションの設定では、マスター プランに使用する計画エンジンを決定します。</span><span class="sxs-lookup"><span data-stu-id="1b73b-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="1b73b-158">**はい** – 計画の最適化がマスター プランに使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b73b-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="1b73b-159">**いいえ** – 組み込み Supply Chain Management 計画エンジンがマスター プランに使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b73b-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="1b73b-160">**計画の最適化の使用**オプションが**はい**に設定されているときに、組み込みの Supply Chain Management 計画エンジンに対して作成された既存の計画バッチ ジョブがトリガーされた場合、これらのジョブは失敗します。</span><span class="sxs-lookup"><span data-stu-id="1b73b-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="1b73b-161">設定との統合</span><span class="sxs-lookup"><span data-stu-id="1b73b-161">Integration with the setup</span></span>

<span data-ttu-id="1b73b-162">計画の最適化のプレビューが有効になっている場合は、計画の最適化アドインを使用してマスター プランが実行されます。</span><span class="sxs-lookup"><span data-stu-id="1b73b-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="1b73b-163">この場合、マスター プランの結果と機能が影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="1b73b-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b73b-164">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1b73b-164">Additional resources</span></span>

[<span data-ttu-id="1b73b-165">プレビュー用の使用条件</span><span class="sxs-lookup"><span data-stu-id="1b73b-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="1b73b-166">計画最適化の概要</span><span class="sxs-lookup"><span data-stu-id="1b73b-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="1b73b-167">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="1b73b-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1b73b-168">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="1b73b-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1b73b-169">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="1b73b-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="1b73b-170">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="1b73b-170">Cancel a planning job</span></span>](cancel-planning-job.md)
