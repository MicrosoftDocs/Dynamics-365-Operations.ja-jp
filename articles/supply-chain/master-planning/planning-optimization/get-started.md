---
title: 計画の最適化の使用を開始する
description: このトピックでは、計画の最適化機能の使用を開始する方法について説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773995"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="e4695-103">計画の最適化の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="e4695-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="e4695-104">現時点では、計画の最適化機能では、Microsoft Dynamics 365 Supply Chain Management に組み込まれている計画エンジンで利用可能なすべての機能がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e4695-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e4695-105">したがって、計画の最適化で現在利用可能な機能セットが要件を満たすかどうかを評価することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e4695-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="e4695-106">既定では、Dynamics Lifecycle Services (LCS) で、計画の最適化機能は有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="e4695-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="e4695-107">したがって、オンにする前に評価を行う機会があります。</span><span class="sxs-lookup"><span data-stu-id="e4695-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="e4695-108">最終的に、既存の組み込み Supply Chain Management 計画エンジンは、計画の最適化によって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="e4695-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="e4695-109">計画の最適化を有効にする前に、計画の最適化フィット分析の結果を評価することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e4695-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="e4695-110">詳細については、[計画の最適化フィット分析](planning-optimization-fit-analysis.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4695-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="e4695-111">ライセンス</span><span class="sxs-lookup"><span data-stu-id="e4695-111">Licensing</span></span>

<span data-ttu-id="e4695-112">現在のライセンスを使用してマスター プランを実行できる場合は、計画の最適化の使用を開始するために追加のライセンスを購入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e4695-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="e4695-113">アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="e4695-113">Install the add-in</span></span>

<span data-ttu-id="e4695-114">計画の最適化を使用するには、Dynamics 365 Supply Chain Management 用の計画の最適化アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="e4695-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e4695-115">LCS プロジェクトからアドインにアクセスし、Supply Chain Management ユーザーインターフェイス (UI) から計画の最適化機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e4695-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="e4695-116">LCS にサインインし、目的の環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="e4695-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="e4695-117">**完全な詳細**に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4695-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="e4695-118">**メンテナンス**を選択するか、**環境アドイン** クイック タブまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="e4695-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="e4695-119">**新しいアドインのインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4695-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="e4695-120">**計画の最適化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4695-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="e4695-121">インストール ガイドに従って、契約条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="e4695-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="e4695-122">**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4695-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="e4695-123">計画の最適化の統合</span><span class="sxs-lookup"><span data-stu-id="e4695-123">Planning Optimization integration</span></span>

<span data-ttu-id="e4695-124">計画の最適化アドインをマスター プランに使用するかどうかを構成するには、**マスター プラン** \> **セットアップ** \> **計画の最適化の統合** \> **統合パラメーター** の順に進みます。</span><span class="sxs-lookup"><span data-stu-id="e4695-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="e4695-125">接続状態</span><span class="sxs-lookup"><span data-stu-id="e4695-125">Connection status</span></span>

<span data-ttu-id="e4695-126">接続ステータスは、Supply Chain Management と計画の最適化サービスとの間の接続の現在のステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="e4695-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="e4695-127">次の表は、使用可能な値を示しています。</span><span class="sxs-lookup"><span data-stu-id="e4695-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="e4695-128">接続状態</span><span class="sxs-lookup"><span data-stu-id="e4695-128">Connection status</span></span> | <span data-ttu-id="e4695-129">説明</span><span class="sxs-lookup"><span data-stu-id="e4695-129">Description</span></span> | <span data-ttu-id="e4695-130">計画の最適化は使用できますか?</span><span class="sxs-lookup"><span data-stu-id="e4695-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="e4695-131">接続済</span><span class="sxs-lookup"><span data-stu-id="e4695-131">Connected</span></span> | <span data-ttu-id="e4695-132">計画の最適化サービスと Supply Chain Management の間に接続が確立されています。</span><span class="sxs-lookup"><span data-stu-id="e4695-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="e4695-133">はい</span><span class="sxs-lookup"><span data-stu-id="e4695-133">Yes</span></span> |
| <span data-ttu-id="e4695-134">接続の有効化</span><span class="sxs-lookup"><span data-stu-id="e4695-134">Enabling connection</span></span> | <span data-ttu-id="e4695-135">計画の最適化サービスへの接続を有効にする要求が現在進行中です。</span><span class="sxs-lookup"><span data-stu-id="e4695-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e4695-136">いいえ</span><span class="sxs-lookup"><span data-stu-id="e4695-136">No</span></span> |
| <span data-ttu-id="e4695-137">接続解除済</span><span class="sxs-lookup"><span data-stu-id="e4695-137">Disconnected</span></span> | <span data-ttu-id="e4695-138">計画の最適化サービスへの接続はありません。</span><span class="sxs-lookup"><span data-stu-id="e4695-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="e4695-139">このトピックで前述されているように、LCS から接続をオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e4695-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="e4695-140">いいえ</span><span class="sxs-lookup"><span data-stu-id="e4695-140">No</span></span> |
| <span data-ttu-id="e4695-141">接続を無効にしています</span><span class="sxs-lookup"><span data-stu-id="e4695-141">Disabling connection</span></span> | <span data-ttu-id="e4695-142">計画の最適化サービスへの接続をオフにする要求が現在進行中です。</span><span class="sxs-lookup"><span data-stu-id="e4695-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e4695-143">いいえ</span><span class="sxs-lookup"><span data-stu-id="e4695-143">No</span></span> |
| <span data-ttu-id="e4695-144">状態を取得しています</span><span class="sxs-lookup"><span data-stu-id="e4695-144">Getting status</span></span> | <span data-ttu-id="e4695-145">システムは、計画の最適化サービスからのステータス情報を待機しています。</span><span class="sxs-lookup"><span data-stu-id="e4695-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="e4695-146">いいえ</span><span class="sxs-lookup"><span data-stu-id="e4695-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="e4695-147">計画の最適化の使用オプション</span><span class="sxs-lookup"><span data-stu-id="e4695-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="e4695-148">**計画の最適化の使用**オプションの設定では、マスター プランに使用する計画エンジンを決定します。</span><span class="sxs-lookup"><span data-stu-id="e4695-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="e4695-149">**はい** – 計画の最適化がマスター プランに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4695-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="e4695-150">**いいえ** – 組み込み Supply Chain Management 計画エンジンがマスター プランに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4695-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="e4695-151">**計画の最適化の使用**オプションが**はい**に設定されているときに、組み込みの Supply Chain Management 計画エンジンに対して作成された既存の計画バッチ ジョブがトリガーされた場合、これらのジョブは失敗します。</span><span class="sxs-lookup"><span data-stu-id="e4695-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="e4695-152">設定との統合</span><span class="sxs-lookup"><span data-stu-id="e4695-152">Integration with the setup</span></span>

<span data-ttu-id="e4695-153">計画の最適化のプレビューが有効になっている場合は、計画の最適化アドインを使用してマスター プランが実行されます。</span><span class="sxs-lookup"><span data-stu-id="e4695-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="e4695-154">この場合、マスター プランの結果と機能が影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="e4695-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="e4695-155">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="e4695-155">Related resources</span></span>

[<span data-ttu-id="e4695-156">プレビュー用の使用条件</span><span class="sxs-lookup"><span data-stu-id="e4695-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="e4695-157">計画の最適化の概要</span><span class="sxs-lookup"><span data-stu-id="e4695-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e4695-158">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="e4695-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="e4695-159">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="e4695-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e4695-160">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="e4695-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="e4695-161">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="e4695-161">Cancel a planning job</span></span>](cancel-planning-job.md)
