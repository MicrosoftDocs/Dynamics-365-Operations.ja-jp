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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 50633d1e5dd47b61e074d33a9d77a1f9ece0c223
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263377"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="e0cec-103">計画最適化の開始</span><span class="sxs-lookup"><span data-stu-id="e0cec-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0cec-104">[すでに発表した](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) ように、計画の最適化は、既存の組み込みマスター プラン エンジンと置き換えるようにスケジュールされています。</span><span class="sxs-lookup"><span data-stu-id="e0cec-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="e0cec-105">現在、組み込みのマスター プラン エンジンを使用している場合は、すぐに計画の最適化への移行の計画を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="e0cec-106">廃止が適用されると操作が影響を受ける可能性があるため、移行プロセスをすぐに開始することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e0cec-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="e0cec-107">廃止が実施された場合に、最新の問題を回避するために、2020 年 12 月 1 日までに移行を完了することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0cec-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="e0cec-108">現時点では、計画の最適化機能では、Supply Chain Management に組み込まれている計画エンジンで利用可能なすべての機能がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e0cec-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="e0cec-109">したがって、計画の最適化で現在利用可能な機能セットが要件を満たすかどうかを評価することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e0cec-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="e0cec-110">現在、計画の最適化機能は Dynamics Lifecycle Services (LCS) で既定では有効になっていないため、機能を有効にする前に評価を行う機会があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="e0cec-111">マスター プラン プロセスに製造が含まれていない (マスター プランで生成された計画製造オーダー) 場合や、バージョン 10.0.15 以降の組み込みマスター プラン エンジンが必要な場合は、移行から計画の最適化に例外を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="e0cec-112">バージョン 10.0.16 以降、計画製造オーダーを生成せずに組み込みマスター プランを実行すると、環境にエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0cec-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="e0cec-113">計画製造オーダーは、マスター プラン中に計画製造オーダーを生成しないすべての新しい配置に対して使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="e0cec-114">計画製造オーダーを生成せずに組み込みマスター プラン エンジンを実行している既存の環境の所有者は、例外プロセスに関する詳細を含むメールを受信します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="e0cec-115">パートナーと協力して、計画の最適化への移行を評価および計画することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0cec-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="e0cec-116">計画の最適化を有効にする前に、計画の最適化フィット分析の結果を評価することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0cec-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="e0cec-117">詳細については、[計画の最適化フィット分析](planning-optimization-fit-analysis.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0cec-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="availability"></a><span data-ttu-id="e0cec-118">使用可能性</span><span class="sxs-lookup"><span data-stu-id="e0cec-118">Availability</span></span>

<span data-ttu-id="e0cec-119">計画の最適化はは現在、次の Azure の地域で利用可能です: 米国、カナダ、ヨーロッパ、英国、オーストラリア、アジア太平洋。</span><span class="sxs-lookup"><span data-stu-id="e0cec-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, Australia, and Asia Pacific.</span></span> <span data-ttu-id="e0cec-120">他の地域からのアドインをインストールしようとすると、LCS ではこの地理的領域には対応していない旨のメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="e0cec-121">計画の最適化では、 Dynamics 365 Supply Chain Management の社内設置型の配置に対応していないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e0cec-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="e0cec-122">ライセンス</span><span class="sxs-lookup"><span data-stu-id="e0cec-122">Licensing</span></span>

<span data-ttu-id="e0cec-123">現在のライセンスを使用してマスター プランを実行できる場合は、計画の最適化の使用を開始するために追加のライセンスを購入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e0cec-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

## <a name="install-and-enable-planning-optimization"></a><span data-ttu-id="e0cec-124">計画最適化をインストールまたは有効化できない</span><span class="sxs-lookup"><span data-stu-id="e0cec-124">Install and enable Planning Optimization</span></span>

<span data-ttu-id="e0cec-125">計画最適化を使用するには、すべての前提条件をシステムに設定し、ライセンス キーを有効にして、計画の最適化アドインをインストールする必要があります Dynamics 365 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="e0cec-125">To use Planning Optimization, you must make sure your system has all of the prerequisites in place and then enable its license key and install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e0cec-126">必要条件</span><span class="sxs-lookup"><span data-stu-id="e0cec-126">Prerequisites</span></span>

<span data-ttu-id="e0cec-127">計画最適化アドインをインストールする前に、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-127">Before you install the Planning Optimization Add-in, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="e0cec-128">LCS が有効になっている高可用性環境の tier 2 またはそれ以降 (OneBox 環境ではなく)、Dynamics 365 Supply Chain Management バージョン 10.0.7 またはそれ以降で Supply Chain Management を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-128">You must be running Supply Chain Management on an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="e0cec-129">このアドインを OneBox 環境にインストールはできません。インストール処理をキャンセルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-129">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

- <span data-ttu-id="e0cec-130">システムは Power Platform 統合用に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-130">Your system must be set up for Power Platform integration.</span></span> <span data-ttu-id="e0cec-131">詳細については、[アドインを設定するための前提条件](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) および [アドインの設定](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0cec-131">For more information, see [Prerequisites for setting up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) and [Set up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins).</span></span>

### <a name="enable-the-planning-optimization-license"></a><span data-ttu-id="e0cec-132">計画最適化ライセンスを有効化する</span><span class="sxs-lookup"><span data-stu-id="e0cec-132">Enable the Planning Optimization license</span></span>

<span data-ttu-id="e0cec-133">計画最適化を使用するには、構成キーを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-133">To use Planning Optimization, you must enable its configuration key.</span></span> <span data-ttu-id="e0cec-134">そのためには次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="e0cec-134">To do so:</span></span>

1. <span data-ttu-id="e0cec-135">[メンテナンス モード](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、システムをメンテナンス モードにします。</span><span class="sxs-lookup"><span data-stu-id="e0cec-135">Put your system into maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="e0cec-136">**システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0cec-136">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="e0cec-137">**構成 キー** タブで、**計画最適化** のチェック ボックス をオンにします。</span><span class="sxs-lookup"><span data-stu-id="e0cec-137">On the **Configuration keys** tab, select the check box for **Planning Optimization**.</span></span>
1. <span data-ttu-id="e0cec-138">[メンテナンス モード](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、メンテナンス モードをオフにします。</span><span class="sxs-lookup"><span data-stu-id="e0cec-138">Turn off maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="install-the-planning-optimization-add-in"></a><span data-ttu-id="e0cec-139">計画最適化アドインをインストールする</span><span class="sxs-lookup"><span data-stu-id="e0cec-139">Install the Planning Optimization Add-in</span></span>

<span data-ttu-id="e0cec-140">LCS プロジェクトからアドインをインストールし、Supply Chain Management ユーザー インターフェイスから計画最適化の機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0cec-140">You must install the add-in from your LCS project and then turn on the Planning Optimization functionality from the Supply Chain Management user interface.</span></span>

<span data-ttu-id="e0cec-141">計画最適化アドインをインストールするには:</span><span class="sxs-lookup"><span data-stu-id="e0cec-141">To install the Planning Optimization Add-in:</span></span>

1. <span data-ttu-id="e0cec-142">LCS にサインインし、目的の環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="e0cec-142">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="e0cec-143">**完全な詳細** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-143">Go to **Full details**.</span></span>
1. <span data-ttu-id="e0cec-144">**環境アドイン** クイック タブまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="e0cec-144">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="e0cec-145">**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-145">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="e0cec-146">**計画の最適化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-146">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="e0cec-147">インストール ガイドに従って、契約条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-147">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="e0cec-148">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-148">Select **Install**.</span></span>
1. <span data-ttu-id="e0cec-149">**環境アドイン** クイック タブに、計画最適化がインストールされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-149">On the **Environment add-ins** FastTab, you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="e0cec-150">数分後、**インストールしています** が **インストール済み** に変わります (ページを更新する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="e0cec-150">After a few minutes, **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="e0cec-151">インストールすると、Dynamics 365 Supply Chain Management で計画最適化を有効にする準備が整います。</span><span class="sxs-lookup"><span data-stu-id="e0cec-151">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="e0cec-152">計画最適化アドインをインストールする主な目的は、サービスと環境をつなげることです。</span><span class="sxs-lookup"><span data-stu-id="e0cec-152">The main purpose of installing the Planning Optimization Add-in is to connect the service and the environment.</span></span> <span data-ttu-id="e0cec-153">したがって、環境間で移動したコードに関係なく、計画の最適化を使用する環境ごとにアドインを個別にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0cec-153">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

## <a name="integrate-planning-optimization-with-your-system"></a><span data-ttu-id="e0cec-154">システムとの計画最適化を統合する</span><span class="sxs-lookup"><span data-stu-id="e0cec-154">Integrate Planning Optimization with your system</span></span>

<span data-ttu-id="e0cec-155">計画の最適化アドインをマスター プランに使用するかどうかを構成するには、**マスター プラン** \> **セットアップ** \> **計画最適化パラメーター** の順に進みます。</span><span class="sxs-lookup"><span data-stu-id="e0cec-155">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

### <a name="connection-status"></a><span data-ttu-id="e0cec-156">接続状態</span><span class="sxs-lookup"><span data-stu-id="e0cec-156">Connection status</span></span>

<span data-ttu-id="e0cec-157">接続ステータスは、Supply Chain Management と計画の最適化サービスとの間の接続の現在のステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-157">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="e0cec-158">次の表は、使用可能な値を示しています。</span><span class="sxs-lookup"><span data-stu-id="e0cec-158">The following table shows the possible values.</span></span>

| <span data-ttu-id="e0cec-159">接続状態</span><span class="sxs-lookup"><span data-stu-id="e0cec-159">Connection status</span></span> | <span data-ttu-id="e0cec-160">説明</span><span class="sxs-lookup"><span data-stu-id="e0cec-160">Description</span></span> | <span data-ttu-id="e0cec-161">計画の最適化は使用できますか?</span><span class="sxs-lookup"><span data-stu-id="e0cec-161">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="e0cec-162">接続済</span><span class="sxs-lookup"><span data-stu-id="e0cec-162">Connected</span></span> | <span data-ttu-id="e0cec-163">計画の最適化サービスと Supply Chain Management の間に接続が確立されています。</span><span class="sxs-lookup"><span data-stu-id="e0cec-163">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="e0cec-164">はい</span><span class="sxs-lookup"><span data-stu-id="e0cec-164">Yes</span></span> |
| <span data-ttu-id="e0cec-165">接続の有効化</span><span class="sxs-lookup"><span data-stu-id="e0cec-165">Enabling connection</span></span> | <span data-ttu-id="e0cec-166">計画の最適化サービスへの接続を有効にする要求が現在進行中です。</span><span class="sxs-lookup"><span data-stu-id="e0cec-166">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e0cec-167">いいえ</span><span class="sxs-lookup"><span data-stu-id="e0cec-167">No</span></span> |
| <span data-ttu-id="e0cec-168">接続解除済</span><span class="sxs-lookup"><span data-stu-id="e0cec-168">Disconnected</span></span> | <span data-ttu-id="e0cec-169">計画の最適化サービスへの接続はありません。</span><span class="sxs-lookup"><span data-stu-id="e0cec-169">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="e0cec-170">このトピックで前述されているように、LCS から接続をオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0cec-170">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="e0cec-171">いいえ</span><span class="sxs-lookup"><span data-stu-id="e0cec-171">No</span></span> |
| <span data-ttu-id="e0cec-172">接続を無効にしています</span><span class="sxs-lookup"><span data-stu-id="e0cec-172">Disabling connection</span></span> | <span data-ttu-id="e0cec-173">計画の最適化サービスへの接続をオフにする要求が現在進行中です。</span><span class="sxs-lookup"><span data-stu-id="e0cec-173">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e0cec-174">いいえ</span><span class="sxs-lookup"><span data-stu-id="e0cec-174">No</span></span> |
| <span data-ttu-id="e0cec-175">状態を取得しています</span><span class="sxs-lookup"><span data-stu-id="e0cec-175">Getting status</span></span> | <span data-ttu-id="e0cec-176">システムは、計画の最適化サービスからのステータス情報を待機しています。</span><span class="sxs-lookup"><span data-stu-id="e0cec-176">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="e0cec-177">いいえ</span><span class="sxs-lookup"><span data-stu-id="e0cec-177">No</span></span> |

### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="e0cec-178">計画の最適化の使用オプション</span><span class="sxs-lookup"><span data-stu-id="e0cec-178">The Use Planning Optimization option</span></span>

<span data-ttu-id="e0cec-179">**計画の最適化の使用** オプションの設定では、マスター プランに使用する計画エンジンを決定します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-179">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="e0cec-180">**はい** – 計画の最適化がマスター プランに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0cec-180">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="e0cec-181">**いいえ** – 組み込み Supply Chain Management 計画エンジンがマスター プランに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0cec-181">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="e0cec-182">**計画の最適化の使用** オプションが **はい** に設定されているときに、組み込みの Supply Chain Management 計画エンジンに対して作成された既存の計画バッチ ジョブがトリガーされた場合、これらのジョブは失敗します。</span><span class="sxs-lookup"><span data-stu-id="e0cec-182">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="e0cec-183">設定との統合</span><span class="sxs-lookup"><span data-stu-id="e0cec-183">Integration with the setup</span></span>

<span data-ttu-id="e0cec-184">計画の最適化が有効になっている場合は、計画の最適化アドインを使用してマスター プランが実行されます。</span><span class="sxs-lookup"><span data-stu-id="e0cec-184">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="e0cec-185">この場合、マスター プランの結果と機能が影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="e0cec-185">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0cec-186">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e0cec-186">Additional resources</span></span>

[<span data-ttu-id="e0cec-187">プレビュー用の使用条件</span><span class="sxs-lookup"><span data-stu-id="e0cec-187">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="e0cec-188">計画最適化の概要</span><span class="sxs-lookup"><span data-stu-id="e0cec-188">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e0cec-189">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="e0cec-189">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="e0cec-190">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="e0cec-190">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e0cec-191">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="e0cec-191">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="e0cec-192">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="e0cec-192">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]