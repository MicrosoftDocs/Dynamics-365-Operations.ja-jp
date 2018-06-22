---
title: "クラウド環境への更新プログラムの適用"
description: "このトピックでは、Lifecycle Services (LCS) を使用して、バイナリ更新プログラムまたはアプリケーション (AOT) 展開可能なパッケージをクラウド環境に適用する方法について説明します。"
author: manalidongre
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Retail
ms.assetid: 341a229f-d9c3-4678-b353-d08d5b2c1caf
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c3be751d4d3aba36165f712ec52eba46b01a6783
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="apply-updates-to-a-cloud-environment"></a><span data-ttu-id="52ba0-103">クラウド環境への更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="52ba0-103">Apply updates to a cloud environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52ba0-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics 365 for Finance and Operations 環境または Microsoft Dynamics 365 for Retail 環境に更新プログラムを自動的に適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-104">This topic describes how you can use Microsoft Dynamics Lifecycle Services (LCS) to automatically apply updates to either a Microsoft Dynamics 365 for Finance and Operations environment or a Microsoft Dynamics 365 for Retail environment.</span></span> <span data-ttu-id="52ba0-105">展開可能なパッケージを使用して更新が適用されます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-105">Updates are applied using deployable packages.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52ba0-106">パッケージを適用するとシステムのダウンタイムが発生します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-106">Applying packages causes system downtime.</span></span> <span data-ttu-id="52ba0-107">すべて関連するサービスを停止、およびパッケージを適用中のときには環境を使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-107">All relevant services will be stopped, and you won't be able to use your environments while the package is being applied.</span></span> <span data-ttu-id="52ba0-108">それに応じた計画を立てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-108">You should plan accordingly.</span></span>

## <a name="supported-environments"></a><span data-ttu-id="52ba0-109">サポートされる環境</span><span class="sxs-lookup"><span data-stu-id="52ba0-109">Supported environments</span></span>

<span data-ttu-id="52ba0-110">次のトポロジは、LCS で自動化されたフローを使用するパッケージ配置をサポートします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-110">The following topologies support package deployment that uses automated flows in LCS:</span></span>

- <span data-ttu-id="52ba0-111">**LCS 実装プロジェクト** – すべての環境のタイプがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="52ba0-111">**LCS Implementation Project** – All environment types are supported.</span></span> <span data-ttu-id="52ba0-112">自動化されたパッケージ アプリケーションとは、実稼働環境を除くすべての環境のセルフサービス操作です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-112">Automated package application is a self-service operation in all environments except production environments.</span></span> <span data-ttu-id="52ba0-113">実稼働環境については、顧客は、適用パッケージを要求を送信するため LCS を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-113">For production environments, customers must use LCS to submit a request to apply packages.</span></span>
- <span data-ttu-id="52ba0-114">**LCS パートナーと試用プロジェクト** – マルチボックス開発/テスト トポロジを除く、すべての環境のタイプがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="52ba0-114">**LCS Partner and Trial Projects** – All environment types are supported, except multi-box dev/test topologies.</span></span>

<span data-ttu-id="52ba0-115">他のトポロジ (以下) については、リモート デスクトップ プロトコル (RDP) を使用して環境に接続し、コマンドラインからインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-115">For other topologies (below), you must use Remote Desktop Protocol (RDP) to connect to the environment and install from the command line.</span></span> <span data-ttu-id="52ba0-116">手動のパッケージ配置の詳細については、[配置可能パッケージのインストール](install-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52ba0-116">For information about manual package deployment, see [Install  a deployable package](install-deployable-package.md).</span></span>

- <span data-ttu-id="52ba0-117">ローカルの開発環境 (仮想ハード ディスク [VHD] からダウンロード可能)</span><span class="sxs-lookup"><span data-stu-id="52ba0-117">Local development environments (Downloadable virtual hard disk [VHD])</span></span>
- <span data-ttu-id="52ba0-118">Microsoft Azure (パートナーおよび試用プロジェクト) でのマルチボックス開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="52ba0-118">Multi-box dev/test environments in Microsoft Azure (Partner and trial projects)</span></span>

## <a name="key-concepts"></a><span data-ttu-id="52ba0-119">重要な概念</span><span class="sxs-lookup"><span data-stu-id="52ba0-119">Key concepts</span></span>

<span data-ttu-id="52ba0-120">開始する前に、*配置可能パッケージ*、*runbooks*、および *AXInstaller* を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-120">Before you begin, you should understand *deployable packages*, *runbooks*, and the *AXInstaller*.</span></span> <span data-ttu-id="52ba0-121">デプロイ可能なパッケージは、どのような環境でも利用可能なデプロイメントの単位です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-121">A deployable package is a unit of deployment that can be applied in any environment.</span></span> <span data-ttu-id="52ba0-122">デプロイ可能なパッケージは、プラットフォームまたは他のランタイム コンポーネント、更新されたアプリケーション (AOT) パッケージ、または新しいアプリケーション (AOT) パッケージのバイナリ更新です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-122">A deployable package can be a binary update to the platform or other runtime components, an updated application (AOT) package, or a new application (AOT) package.</span></span> <span data-ttu-id="52ba0-123">AXInstaller は、パッケージのインストールを可能にする runbook を作成します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-123">The AXInstaller creates a runbook that enables installing a package.</span></span> <span data-ttu-id="52ba0-124">詳細については、このトピックの最後で [パッケージ、Runbook、および AXUpdateInstaller の詳細](#packages-runbooks-and-the-AXUpdateInstaller-in-depth) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52ba0-124">For more details, see [Packages, runbooks, and the AXUpdateInstaller in depth](#packages-runbooks-and-the-AXUpdateInstaller-in-depth) at the end of this topic.</span></span>

## <a name="supported-package-types"></a><span data-ttu-id="52ba0-125">サポートされているパッケージの種類</span><span class="sxs-lookup"><span data-stu-id="52ba0-125">Supported package types</span></span>

- <span data-ttu-id="52ba0-126">**AOT の配置可能パッケージ** - アプリケーション メタデータおよびソース コードから生成される配置可能なパッケージ。</span><span class="sxs-lookup"><span data-stu-id="52ba0-126">**AOT deployable package** – A deployable package that is generated from application metadata and source code.</span></span> <span data-ttu-id="52ba0-127">この展開可能なパッケージは、開発環境またはビルド環境で作成されます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-127">This deployable package is created in a development or build environment.</span></span>
- <span data-ttu-id="52ba0-128">**バイナリ更新プログラム パッケージ** - ダイナミックリンク ライブラリ (DLL)と、プラットフォームとアプリケーションが依存するその他のバイナリとメタデータを含む配置可能パッケージ。</span><span class="sxs-lookup"><span data-stu-id="52ba0-128">**Binary update package** – A deployable package that contains dynamic-link libraries (DLLs) and other binaries and metadata that the platform and application depend on.</span></span> <span data-ttu-id="52ba0-129">これは、Microsoft によってリリースされたパッケージです。</span><span class="sxs-lookup"><span data-stu-id="52ba0-129">This is a package released by Microsoft.</span></span>
- <span data-ttu-id="52ba0-130">**結合された配置可能小売パッケージ** - 小売コードが結合された後に生成されるさまざまな小売パッケージの組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="52ba0-130">**Combined Retail deployable package** – A combination of various Retail packages that are generated after the Retail code is combined.</span></span>
- <span data-ttu-id="52ba0-131">**マージ済パッケージ** – 各タイプの 1 つのパッケージを組み合わせて作成されたパッケージ。</span><span class="sxs-lookup"><span data-stu-id="52ba0-131">**Merged package** – A package that is created by combining one package of each type.</span></span> <span data-ttu-id="52ba0-132">たとえば、1 つのバイナリ更新プログラム パッケージ、1 つの AOT パッケージ、および 1 つの小売パッケージを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-132">For example, one binary update package, one AOT package, and one Retail package can be combined.</span></span> <span data-ttu-id="52ba0-133">パッケージは、LCS のプロジェクトのアセット ライブラリでマージされます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-133">The packages are merged in the Asset library for the project in LCS.</span></span>

## <a name="prerequisite-steps"></a><span data-ttu-id="52ba0-134">前提条件のステップ</span><span class="sxs-lookup"><span data-stu-id="52ba0-134">Prerequisite steps</span></span>

- <span data-ttu-id="52ba0-135">**適用するパッケージが有効であることを確認してください。**</span><span class="sxs-lookup"><span data-stu-id="52ba0-135">**Make sure that the package that should be applied is valid.**</span></span> <span data-ttu-id="52ba0-136">パッケージがアセット ライブラリにアップロードされるとき、そのパッケージは分析されません。</span><span class="sxs-lookup"><span data-stu-id="52ba0-136">When a package is uploaded to the Asset library, it isn't analyzed.</span></span> <span data-ttu-id="52ba0-137">パッケージを選択すると、右側のペインにパッケージ ステータスが **未検証** として表示されます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-137">If you select the package, the package status appears in the right pane as **Not Validated**.</span></span> <span data-ttu-id="52ba0-138">パッケージは、環境に適用する前に、次の手順を使用して検証に合格する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-138">A package must pass validation before it can be applied in an environment by using the following procedures.</span></span> <span data-ttu-id="52ba0-139">パッケージの状態は、パッケージが有効かどうかを示すために、資産ライブラリで更新されます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-139">The status of the package will be updated in the Asset library to indicate whether the package is valid.</span></span> <span data-ttu-id="52ba0-140">ガイドラインを満たしていないパッケージによって実稼働環境が影響を受けていなことを保証する手助けのために検証が必要です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-140">We require validation to help guarantee that production environments aren't affected by packages that don't meet the guidelines.</span></span>

    <span data-ttu-id="52ba0-141">検証には次の 3 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-141">There are three types of validations:</span></span>

    - <span data-ttu-id="52ba0-142">基本パッケージの形式検証</span><span class="sxs-lookup"><span data-stu-id="52ba0-142">Basic package format validations</span></span>
    - <span data-ttu-id="52ba0-143">プラットフォーム バージョンのチェック</span><span class="sxs-lookup"><span data-stu-id="52ba0-143">Platform version checks</span></span>
    - <span data-ttu-id="52ba0-144">パッケージのタイプ</span><span class="sxs-lookup"><span data-stu-id="52ba0-144">Types of packages</span></span>

- <span data-ttu-id="52ba0-145">**実稼動環境でパッケージを適用する前に、パッケージがサンド ボックス環境に適用されていることを確認してください。**</span><span class="sxs-lookup"><span data-stu-id="52ba0-145">**Make sure that the package is applied in a sandbox environment before it's applied in the production environment.**</span></span> <span data-ttu-id="52ba0-146">実稼働環境が常に良好な状態に保たれるように、実稼働環境に適用される前にパッケージがサンドボックス環境でテストされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-146">To help guarantee that the production environment is always in a good state, we want to make sure that the package is tested in a sandbox environment before it's applied in the production environment.</span></span> <span data-ttu-id="52ba0-147">したがって、パッケージが実稼働環境で適用されるように要求する前に、自動フローを使用してパッケージがサンドボックス環境に適用されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="52ba0-147">Therefore, before you request that the package be applied in your production environment, make sure that it has been applied in your sandbox environment by using the automated flows.</span></span>
- <span data-ttu-id="52ba0-148">**複数のパッケージを適用する場合は、マージ済パッケージを作成します。このパッケージは、まずサンドボックス環境で、次に実稼働環境で適用できます。**</span><span class="sxs-lookup"><span data-stu-id="52ba0-148">**If you want to apply multiple packages, create a merged package that can be applied first in a sandbox environment and then in the production environment.**</span></span> <span data-ttu-id="52ba0-149">平均環境で単一パッケージのアプリケーションは、約 5 時間のダウンタイムが必要です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-149">Application of a single package in an average environment requires about 5 hours of downtime.</span></span> <span data-ttu-id="52ba0-150">複数のパッケージを適用する必要がある場合にダウンタイムが発生しないように、各タイプのパッケージを 1 つずつ含む単一のパッケージを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-150">To avoid additional hours of downtime when you must apply multiple packages, you can create a single combined package that contains one package of each type.</span></span> <span data-ttu-id="52ba0-151">資産ライブラリでバイナリ パッケージとアプリケーション配置可能パッケージを選択した場合、**マージ** ボタンは、ツールバー上で利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-151">If you select a binary package and an application deployable package in the Asset library, a **Merge** button becomes available on the toolbar.</span></span> <span data-ttu-id="52ba0-152">このボタンをクリックすると、2 つのパッケージを単一のパッケージにマージできるため、合計のダウンタイムを半分に減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-152">By clicking this button, you can merge the two packages into a single package and therefore reduce the total downtime by half.</span></span>

## <a name="apply-a-package-to-a-non-production-environment-by-using-lcs"></a><span data-ttu-id="52ba0-153">LCS を使用して非運用環境にパッケージを適用します</span><span class="sxs-lookup"><span data-stu-id="52ba0-153">Apply a package to a non-production environment by using LCS</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52ba0-154">パッケージを適用するとシステムのダウンタイムが発生します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-154">Applying packages causes system downtime.</span></span> <span data-ttu-id="52ba0-155">すべて関連するサービスを停止、およびパッケージを適用中のときには環境を使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-155">All relevant services will be stopped, and you won't be able to use your environments while the package is being applied.</span></span>

<span data-ttu-id="52ba0-156">開始する前に、配置可能パッケージが LCS のアセット ライブラリにアップロードされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-156">Before you begin, verify that the deployable package has been uploaded to the Asset library in LCS.</span></span>

1. <span data-ttu-id="52ba0-157">バイナリ更新プログラムで、資産ライブラリに直接パッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-157">For a binary update, upload the package directly to the Asset library.</span></span> <span data-ttu-id="52ba0-158">LCS から更新プログラムをダウンロードする方法の詳細については、[Lifecycle Services から更新プログラムをダウンロード](../migration-upgrade/download-hotfix-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52ba0-158">For information about how to download an update from LCS, see [Download updates from Lifecycle Services](../migration-upgrade/download-hotfix-lcs.md).</span></span>

    <span data-ttu-id="52ba0-159">X++ 修正プログラムまたはアプリケーション カスタマイズおよび拡張機能からの結果であるアプリケーション (AOT) 配置可能パッケージについては、開発またはビルド環境で配置可能パッケージを作成し、資産ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-159">For an application (AOT) deployable package that results from an X++ hotfix, or from application customizations and extensions, create the deployable package in your development or build environment, and then upload it to the Asset library.</span></span>
2. <span data-ttu-id="52ba0-160">パッケージを適用する環境の**環境の詳細**ビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-160">Open the **Environment details** view for the environment where you want to apply the package.</span></span>
3. <span data-ttu-id="52ba0-161">**メンテナンス** &gt; **更新プログラムの適用**をクリックし、更新プログラムを適用します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-161">Click **Maintain** &gt; **Apply updates** to apply an update.</span></span>
4. <span data-ttu-id="52ba0-162">パッケージを選択して適用します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-162">Select the package to apply.</span></span> <span data-ttu-id="52ba0-163">上部にあるフィルターを使用してパッケージを探します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-163">Use the filter at the top to find your package.</span></span>
5. <span data-ttu-id="52ba0-164">**適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-164">Click **Apply**.</span></span> <span data-ttu-id="52ba0-165">**環境の詳細**ビューの右上隅にある状態が**キュー**に変わり、**環境の更新**セクションにパッケージの進捗状況が表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-165">Notice that the status in the upper-right corner of the **Environment details** view changes to **Queued**, and that an **Environment updates** section now shows the progress of the package.</span></span>

    <span data-ttu-id="52ba0-166">[![キュー ステータス](./media/parallelexecutionsandbox_queuedstate.jpg)](./media/parallelexecutionsandbox_queuedstate.jpg)</span><span class="sxs-lookup"><span data-stu-id="52ba0-166">[![Queued status](./media/parallelexecutionsandbox_queuedstate.jpg)](./media/parallelexecutionsandbox_queuedstate.jpg)</span></span>
    
6. <span data-ttu-id="52ba0-167">ページを更新し、パッケージ アプリケーションの進行状況を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52ba0-167">Refresh the page to see the progress of the package application.</span></span> <span data-ttu-id="52ba0-168">サービス ステータスが**進行中**であり、環境ステータスが**サービス**となっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-168">Notice that the servicing status is **In Progress**, and that the environment status is **Servicing**.</span></span>

    <span data-ttu-id="52ba0-169">[![サービスの状態](./media/parallelexecutionsandbox_servicingstate.png)](./media/parallelexecutionsandbox_servicingstate.png)</span><span class="sxs-lookup"><span data-stu-id="52ba0-169">[![Servicing status](./media/parallelexecutionsandbox_servicingstate.png)](./media/parallelexecutionsandbox_servicingstate.png)</span></span>
    
7. <span data-ttu-id="52ba0-170">ページを更新して、パッケージ アプリケーション要求のステータス更新を確認します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-170">Continue to refresh the page to see the status updates for the package application request.</span></span> <span data-ttu-id="52ba0-171">このパッケージが適用されると、環境ステータスは **配置済み** に変わり、サービスのステータスは **完了** に変わります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-171">When the package has been applied, the environment status changes to **Deployed**, and the servicing status changes to **Completed**.</span></span>

    <span data-ttu-id="52ba0-172">[![配置済み状態](./media/parallelexecutionsandbox_signedoffstate.png)](./media/parallelexecutionsandbox_signedoffstate.png)</span><span class="sxs-lookup"><span data-stu-id="52ba0-172">[![Deployed status](./media/parallelexecutionsandbox_signedoffstate.png)](./media/parallelexecutionsandbox_signedoffstate.png)</span></span>
    
8. <span data-ttu-id="52ba0-173">パッケージ アプリケーションでサインオフするには、問題がなければ **サインオフ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-173">To sign off on package application, click **Sign off** if there are no issues.</span></span> <span data-ttu-id="52ba0-174">パッケージを適用するときに問題が発生した場合**払出サイン オフ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-174">If issues occurred when you applied the package, click **Sign off with issues**.</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="52ba0-175">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="52ba0-175">Troubleshooting</span></span>

#### <a name="general-troubleshootingdiagnostics"></a><span data-ttu-id="52ba0-176">一般的なトラブルシューティング/診断</span><span class="sxs-lookup"><span data-stu-id="52ba0-176">General troubleshooting/diagnostics</span></span>

<span data-ttu-id="52ba0-177">パッケージ アプリケーションが正常に行われない場合は、ログまたは詳細なログを確認する runbook のいずれかをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-177">If package application isn't successful, you can download either the logs or the runbook to see the detailed logs.</span></span> <span data-ttu-id="52ba0-178">また、RDP を使用して、問題を修正するために環境に接続することができます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-178">You can also use RDP to connect to an environment so that you can fix issues.</span></span> <span data-ttu-id="52ba0-179">Microsoft に問題を報告する必要がある場合、**環境更新**セクションに報告される活動 ID を含めるようにします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-179">If you must report the issue to Microsoft, be sure to include the activity ID that is reported in the **Environment updates** section.</span></span>

![ログのダウンロードおよび runbook ボタンのダウンロード](./media/applypackage_sandbox_10.png)


![トラブルシューティング](./media/parallelexecutionsandbox_troubleshooting.jpg)

#### <a name="using-the-logs"></a><span data-ttu-id="52ba0-182">ログの使用</span><span class="sxs-lookup"><span data-stu-id="52ba0-182">Using the logs</span></span>

1. <span data-ttu-id="52ba0-183">ログをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-183">Download the logs.</span></span>
2. <span data-ttu-id="52ba0-184">ログ ファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-184">Unzip the log files.</span></span>
3. <span data-ttu-id="52ba0-185">**AOS** や **BI** など、ステップが失敗したロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-185">Select the role that a step failed for, such as **AOS** or **BI**.</span></span>
4. <span data-ttu-id="52ba0-186">ステップが失敗した VM を選択します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-186">Select the VM where the step failed.</span></span> <span data-ttu-id="52ba0-187">この情報は **環境の更新** セクションの **コンピューター名** 列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-187">This information appears in the **Machine name** column in the **Environment updates** section.</span></span>
5. <span data-ttu-id="52ba0-188">VM のログで、問題が発生したステップに対応するフォルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-188">In the logs for the VM, select the folder that corresponds to the step where the issue occurred.</span></span> <span data-ttu-id="52ba0-189">フォルダー名は、各フォルダーが対応するステップを識別します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-189">The folder name identifies the step that each folder corresponds to.</span></span> <span data-ttu-id="52ba0-190">たとえば、ステップの実行で問題が発生した場合、<strong>ExecuteRunbook\</strong>\* フォルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-190">For example, if the issue occurred in the executing of a step, select the <strong>ExecuteRunbook\</strong>\* folder.</span></span>

    <span data-ttu-id="52ba0-191">たとえば、フォルダー名が ExecuteRunbook-b0c5c413-dae3-4a7a-a0c4-d558614f7e98-1\_I0\_R0 である場合、ステップ番号が強調表示され、グローバル一意識別子 (GUID) の後の番号になります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-191">For example, if the folder name is ExecuteRunbook-b0c5c413-dae3-4a7a-a0c4-d558614f7e98-1\_I0\_R0, the step number is highlighted and is the number after the globally unique identifier (GUID).</span></span>

#### <a name="package-failure"></a><span data-ttu-id="52ba0-192">パッケージの失敗</span><span class="sxs-lookup"><span data-stu-id="52ba0-192">Package failure</span></span>

<span data-ttu-id="52ba0-193">パッケージ アプリケーションが正常に行われていない場合は、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-193">If package application isn't successful, you have two options:</span></span>

- <span data-ttu-id="52ba0-194">失敗した操作を再試行するには、**再開**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-194">Click **Resume** to retry the operation that failed.</span></span>

    ![失敗した状態](./media/parallelexecutionsandbox_failedstate.jpg)
    
- <span data-ttu-id="52ba0-196">パッケージ アプリケーションを停止するには、**中止**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-196">Click **Abort** to stop package application.</span></span>

    > [!Note]
    > <span data-ttu-id="52ba0-197">**中止**をクリックすると、環境に既に作成されている変更はロールバックされません。</span><span class="sxs-lookup"><span data-stu-id="52ba0-197">If you click **Abort**, you don't roll back the changes that have already been made to your environment.</span></span> <span data-ttu-id="52ba0-198">続行するには、問題を修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-198">To proceed, you must fix the issue.</span></span>
    
    <span data-ttu-id="52ba0-199">[![パッケージ アプリケーションを中止すると表示されるメッセージ ボックス](./media/applypackage_sandbox_13-1024x274.png)](./media/applypackage_sandbox_13.png)</span><span class="sxs-lookup"><span data-stu-id="52ba0-199">[![Message box that appears when you abort package application](./media/applypackage_sandbox_13-1024x274.png)](./media/applypackage_sandbox_13.png)</span></span>

## <a name="apply-a-package-to-a-production-environment-by-using-lcs"></a><span data-ttu-id="52ba0-200">LCS を使用して運用環境にパッケージを適用します</span><span class="sxs-lookup"><span data-stu-id="52ba0-200">Apply a package to a production environment by using LCS</span></span>

<span data-ttu-id="52ba0-201">実稼動環境では、サンドボックス環境または他のタイプの環境とは異なり、LCS 経由のパッケージ アプリケーションはセルフ サービスではありません。</span><span class="sxs-lookup"><span data-stu-id="52ba0-201">In a production environment, unlike in a sandbox environment or other types of environments, package application through LCS isn't self-serve.</span></span> <span data-ttu-id="52ba0-202">顧客とパートナーは、お客様がダウンタイムの準備が整ったときにパッケージを適用するために Microsoft に要求を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-202">Customers and partners must submit a request to Microsoft to apply a package when the customer is ready for the downtime.</span></span> 

1. <span data-ttu-id="52ba0-203">更新プログラムを LCS からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-203">Download an update from LCS.</span></span> <span data-ttu-id="52ba0-204">LCS から更新プログラムをダウンロードする方法の詳細については、[Lifecycle Services から更新プログラムをダウンロード](../migration-upgrade/download-hotfix-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52ba0-204">For information about how to download an update from LCS, see [Download updates from Lifecycle Services](../migration-upgrade/download-hotfix-lcs.md).</span></span>

    - <span data-ttu-id="52ba0-205">バイナリ更新プログラムで、更新プログラムの配置可能パッケージを直接資産ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-205">For a binary update, upload the update deployable package directly to the Asset library.</span></span>
    - <span data-ttu-id="52ba0-206">アプリケーション/X++ 更新プログラムについては、開発環境でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-206">For an application/X++ update, apply the package in a development environment.</span></span> <span data-ttu-id="52ba0-207">すべての競合を解決した後、Visual Studio で配置可能パッケージを生成し、アセット ライブラリにパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-207">After you resolve any conflicts, generate a deployable package from Visual Studio, and upload the package to the Asset library.</span></span> <span data-ttu-id="52ba0-208">資産ライブラリにアップロードおよび配置可能なパッケージを作成する方法の詳細については、[配置可能なパッケージの作成と適用](create-apply-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52ba0-208">For information about how to upload to the Asset library and create a deployable package, see [Create and apply a deployable package](create-apply-deployable-package.md).</span></span>

2. <span data-ttu-id="52ba0-209">LCS の**資産ライブラリ**ページの、対応する資産のタイプのタブで(**ソフトウェア可能パッケージ**)、パッケージを選択し、**リリース候補**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-209">On the **Asset library** page in LCS, on the tab that corresponds to the asset type (**Software deployable package**), select a package, and then click **Release candidate**.</span></span>
3. <span data-ttu-id="52ba0-210">このトピックの前半の手順を使用して、サンドボックス環境でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-210">Apply the package in a sandbox environment by using the instructions earlier in this topic.</span></span>
4. <span data-ttu-id="52ba0-211">パッケージが正常に適用された後、サンドボックス環境でサイン オフし、アセット ライブラリを開いて、パッケージを**リリース候補**とマークします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-211">After the package is successfully applied and signed off in the sandbox environment, open the Asset Library, and mark the package as **Release Candidate**.</span></span>
5. <span data-ttu-id="52ba0-212">パッケージを適用する実稼働環境の**環境の詳細**ビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-212">Open the **Environment details** view for the production environment where you want to apply the package.</span></span>
6. <span data-ttu-id="52ba0-213">**メンテナンス** &gt; **更新プログラムの適用**をクリックし、パッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-213">Click **Maintain** &gt; **Apply updates** to apply the package.</span></span>
7. <span data-ttu-id="52ba0-214">適用するパッケージのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-214">Select the type of package to apply.</span></span>
8. <span data-ttu-id="52ba0-215">実稼働環境に適用するパッケージを選択し、**スケジュール** をクリックして適用要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-215">Select the package to apply in your production environment, and then click **Schedule** to submit a request to apply it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52ba0-216">パッケージのリストには、サンドボックス環境で正常に署名され、リリース候補としてマークされているパッケージのみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="52ba0-216">The list of packages includes only the packages that have been successfully signed off in the sandbox environment, and that have been marked as release candidates.</span></span>

9. <span data-ttu-id="52ba0-217">パッケージ アプリケーションをスケジュールする日時を指定して **送信** をクリックし、**OK** をクリックして確認します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-217">Specify the date and time to schedule package application for, click **Submit**, and then click **OK** to confirm.</span></span> <span data-ttu-id="52ba0-218">パッケージを適用している間、お客様の環境はダウンして業務を遂行できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="52ba0-218">Note that your environments will be down and unavailable to perform business while the package is being applied.</span></span>
10. <span data-ttu-id="52ba0-219">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-219">Refresh the page.</span></span> <span data-ttu-id="52ba0-220">ページの 2 つのフィールドは、要求の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-220">Two fields on the page indicate the status of the request.</span></span>

    - <span data-ttu-id="52ba0-221">**要求ステータス** – このフィールドには、Microsoft に送信した要求のステータスが示されます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-221">**Request status** – This field indicates the status of the request that you submitted to Microsoft.</span></span>
    - <span data-ttu-id="52ba0-222">**操作可能なユーザー** - このフィールドは、アクションを実行するユーザーを示します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-222">**Actionable by** – This field indicates who must take action.</span></span>

    ![要求のステータスとフィールドによって操作可能](./media/applypackage_prod_7-1024x269.png)
    
11. <span data-ttu-id="52ba0-224">Microsoft が要求を受け入れるか、拒否します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-224">Microsoft either accepts or denies the request.</span></span>

    - <span data-ttu-id="52ba0-225">要求が承認されると、Microsoft は環境の更新を開始します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-225">If the request is accepted, Microsoft begins to update the environment.</span></span>
    
    ![承認依頼: 要求状態 = 要求受入済、操作可能なユーザー = Microsoft](./media/applypackage_prod_9-1024x384.png)
    
    - <span data-ttu-id="52ba0-227">要求が却下された場合は、Microsoft は却下理由と顧客がとる必要があるアクションを顧客を通知します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-227">If the request is denied, Microsoft informs the customer about the reason for denial and the action that the customer must take.</span></span> <span data-ttu-id="52ba0-228">顧客は、要求の再スケジュール、パッケージの変更、要求の取り消しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-228">The customer can then reschedule the request, change the package, or cancel the request.</span></span>
    
    ![拒否された要求: 要求の状態 = 要求が拒否、アクション可能 = 顧客/パートナー](./media/applypackage_prod_8-1024x322.png)

    <span data-ttu-id="52ba0-230">顧客はいつでも**コメント** フィールドを使用してリクエストにコメントを投稿できます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-230">At any time, the customer can use the **Comments** field to post comments to the request.</span></span>
    
    ![要求に転記されるコメント例](./media/applypackage_prod_10-1024x336.png)
    
12. <span data-ttu-id="52ba0-232">環境がサービスされた後、ステータスを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-232">After the environment is serviced, you can monitor the status.</span></span> <span data-ttu-id="52ba0-233">**ステータスのサービス** フィールドは、パッケージ アプリケーションのステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-233">The **Servicing status** field indicates the status of package application.</span></span>

    <span data-ttu-id="52ba0-234">[![サービス ステータスおよびステータス フィールドの要求](./media/applypackage_prod_11-1024x399.png)](./media/applypackage_prod_11.png)</span><span class="sxs-lookup"><span data-stu-id="52ba0-234">[![Servicing status and Request status fields](./media/applypackage_prod_11-1024x399.png)](./media/applypackage_prod_11.png)</span></span>
    
    <span data-ttu-id="52ba0-235">また、進捗状況インジケーターは、利用可能な手順の総数のうち、実行された手順の数を表示します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-235">Additionally, a progress indicator shows the number of steps that have been run, out of the total number of steps that are available.</span></span>
    
    ![進捗状況インジケーター](./media/applypackage_prod_12-1024x414.png)

### <a name="successful-package-application"></a><span data-ttu-id="52ba0-237">アプリケーションのパッケージに成功</span><span class="sxs-lookup"><span data-stu-id="52ba0-237">Successful package application</span></span>

- <span data-ttu-id="52ba0-238">配置が正常に完了すると、**サービスの状態**フィールドは**完了**に設定されていますが、要求がまだ終了していないため、**要求状態**フィールドは**処理中**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-238">After the deployment is successfully completed, the **Servicing status** field is set to **Completed**, but the **Request status** field is still set to **In progress** because the request hasn't yet been closed.</span></span>

    ![配置の成功: サービスのステータス = 完了、要求のステータス = 実行中](./media/applypackage_prod_13-1024x392.png)
    
- <span data-ttu-id="52ba0-240">Microsoft が要求の適用を完了した後、**サービス要求の終了**をクリックして要求を閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-240">After Microsoft has finished applying the request, you must close the request by clicking **Close servicing request**.</span></span>
- <span data-ttu-id="52ba0-241">成功した要求を閉じるときは、**作業項目の詳細を編集** ダイアログ ボックスで、**サービス要求の状態** フィールドを **成功** に設定し、**送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-241">When you close a successful request, in the **Edit work item details** dialog box, set the **Service request status** field to **Succeeded**, and then click **Submit**.</span></span>

### <a name="unsuccessful-package-application"></a><span data-ttu-id="52ba0-242">アプリケーションのパッケージに失敗</span><span class="sxs-lookup"><span data-stu-id="52ba0-242">Unsuccessful package application</span></span>

- <span data-ttu-id="52ba0-243">パッケージ アプリケーションが正常に終了されていない場合、Microsoft は問題を調査します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-243">If package application isn't successfully completed, Microsoft will investigate the issue.</span></span> <span data-ttu-id="52ba0-244">**ステータスのサービス** フィールドは、パッケージ アプリケーションが失敗したことを示します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-244">The **Servicing status** field will indicate that package application has failed.</span></span>

    ![パッケージ展開に失敗: サービス状態 = 失敗](./media/applypackage_prod_17.png)
    
- <span data-ttu-id="52ba0-246">配置に失敗すると、Microsoft はパッケージを途中で停止して、環境を適正な状態に元に戻し、顧客に要求を送信します。これにより、顧客は、環境を検証して、要求を完了させることができます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-246">When deployment fails, Microsoft can abort the package, revert the environment to a good state, and send the request back to the customer, so that the customer can validate the environment and close the request.</span></span> <span data-ttu-id="52ba0-247">パッケージに問題がある場合は、顧客は新しいパッケージを含む新しい要求を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-247">If there is an issue in the package, the customer must submit a new request that includes the new package.</span></span>

    ![変更が元に戻され、顧客が環境を検証しなければならないとの Microsoft からのコメント](./media/applypackage_prod_18-1024x346.png)
    
- <span data-ttu-id="52ba0-249">失敗した要求を閉じるときは、**作業項目の詳細を編集** ダイアログ ボックスで、**サービス要求の状態** フィールドを **"中止"** に設定します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-249">When you close a failed request, in the **Edit work item details** dialog box, set the **Service request status** field to **Aborted**.</span></span>

## <a name="deploying-packages-in-retail-environments"></a><span data-ttu-id="52ba0-250">小売環境でのパッケージの展開</span><span class="sxs-lookup"><span data-stu-id="52ba0-250">Deploying packages in Retail environments</span></span>

<span data-ttu-id="52ba0-251">環境内の配置可能パッケージを適用した後に、小売コンポーネント (Retail Modern POS など) を使用している場合、店舗内コンポーネントも更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ba0-251">If you're using retail components (such as Retail Modern POS), after you've applied a deployable package in your environment, you must also update your in-store components.</span></span> <span data-ttu-id="52ba0-252">詳細については、[Retail Modern POS のインストールと更新](../../retail/retail-modern-pos-device-activation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52ba0-252">For more information, see [Retail Modern POS installation and updates](../../retail/retail-modern-pos-device-activation.md).</span></span>

## <a name="packages-runbooks-and-the-axupdateinstaller-in-depth"></a><span data-ttu-id="52ba0-253">パッケージ、Runbook、および AXUpdateInstaller の詳細</span><span class="sxs-lookup"><span data-stu-id="52ba0-253">Packages, runbooks, and the AXUpdateInstaller in depth</span></span>

<span data-ttu-id="52ba0-254">配置可能パッケージ、runbooks、および AXUpdateInstaller は、更新プログラムの適用に使用するツールです。</span><span class="sxs-lookup"><span data-stu-id="52ba0-254">Deployable packages, runbooks, and the AXUpdateInstaller are the tools you use to apply updates.</span></span> 

<span data-ttu-id="52ba0-255">**配置可能パッケージ** - 配置可能パッケージとは、任意の Finance and Operations または Retail 環境に適用できる配置の単位です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-255">**Deployable package** – A deployable package is a unit of deployment that can be applied in any Finance and Operations or Retail environment.</span></span> <span data-ttu-id="52ba0-256">デプロイ可能なパッケージは、プラットフォームまたは他のランタイム コンポーネント、更新されたアプリケーション (AOT) パッケージ、または新しいアプリケーション (AOT) パッケージのバイナリ更新です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-256">A deployable package can be a binary update to the platform or other runtime components, an updated application (AOT) package, or a new application (AOT) package.</span></span> <span data-ttu-id="52ba0-257">LCS からダウンロードした、または開発環境で作成した配置可能なパッケージは、製品タイプ間では適用できません。</span><span class="sxs-lookup"><span data-stu-id="52ba0-257">Deployable packages downloaded from LCS or created in a development environment cannot be applied across product types.</span></span> <span data-ttu-id="52ba0-258">つまり、Finance and Operations の展開可能なパッケージは Retail 環境に適用することができず、その逆も同様です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-258">That is, a Finance and Operations deployable package cannot be applied in a Retail environment, and vice versa.</span></span> <span data-ttu-id="52ba0-259">Retail と互換性のある Finance and Operations の既存のカスタマイズを持ち、それを Retail 環境に適用する場合は、Retail 開発環境でソース コードを再パッケージし、逆の方向に移動している場合は逆コンパイルします。</span><span class="sxs-lookup"><span data-stu-id="52ba0-259">If you have an existing customization for Finance and Operations that is compatible with Retail, and would like to apply it to a  Retail environment, you will need to re-package your source code in a Retail development environment, and conversely if moving in the other direction.</span></span>   

<span data-ttu-id="52ba0-260">[![配置可能なパッケージの例](./media/applypackage_deployablepackage.jpg)](./media/applypackage_deployablepackage.jpg)</span><span class="sxs-lookup"><span data-stu-id="52ba0-260">[![Example of a deployable package](./media/applypackage_deployablepackage.jpg)](./media/applypackage_deployablepackage.jpg)</span></span>

<span data-ttu-id="52ba0-261">**Runbook** – 展開ランブックは展開可能なパッケージを対象となる環境に適用させるために生成される一連の手順です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-261">**Runbook** – The deployment runbook is a series of steps that are generated in order to apply the deployable package to the target environment.</span></span> <span data-ttu-id="52ba0-262">一部のステップは自動化され、一部のステップは手動です。</span><span class="sxs-lookup"><span data-stu-id="52ba0-262">Some steps are automated, and some steps are manual.</span></span> <span data-ttu-id="52ba0-263">AXUpdateInstaller は、これらの手順を一度に 1 つずつ正しい順序で実行できます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-263">AXUpdateInstaller lets you run these steps one at a time and in the correct order.</span></span>

<span data-ttu-id="52ba0-264">[![展開ランブック の例](./media/applypackage_runbook-1024x528.jpg)](./media/applypackage_runbook.jpg)</span><span class="sxs-lookup"><span data-stu-id="52ba0-264">[![Example of a deployment runbook](./media/applypackage_runbook-1024x528.jpg)](./media/applypackage_runbook.jpg)</span></span>

<span data-ttu-id="52ba0-265">**AXUpdateInstaller** - Microsoft Visual Studio または Microsoft バイナリ更新プログラムからカスタマイズ パッケージを作成すると、インストーラの実行可能ファイルが配置可能パッケージと共にバンドルされます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-265">**AXUpdateInstaller** – When you create a customization package from Microsoft Visual Studio or a Microsoft binary update, the installer executable is bundled together with the deployable package.</span></span> <span data-ttu-id="52ba0-266">インストーラーは、指定したトポロジの Runbook を生成します。</span><span class="sxs-lookup"><span data-stu-id="52ba0-266">The installer generates the runbook for the specified topology.</span></span> <span data-ttu-id="52ba0-267">インストーラーは、特定のトポロジの Runbook に従って、手順を順番に実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="52ba0-267">The installer can also run steps in order, according to the runbook for a specific topology.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52ba0-268">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="52ba0-268">Additional resources</span></span>

[<span data-ttu-id="52ba0-269">配置可能パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="52ba0-269">Install a deployable package</span></span>](install-deployable-package.md)

