---
title: Finance and Operations の更新とカスタム コード ライフサイクルの管理
description: このトピックでは、ソースコードの開発分岐を管理し、Microsoft サービス更新プログラムの次のバージョンを適用し、カスタムコードの新しいバージョンを適用するためのアプリケーション ライフサイクル シナリオについて説明します。
author: rbadawy
manager: AnnBe
ms.date: 10/22/2020
ms.topic: article
ms.service: dynamics-ax-platform
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2020-10-22
ms.dyn365.ops.version: Platform update 10
ms.openlocfilehash: 94843d180c3561365a47c236a6eda5f81cdda40b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683476"
---
# <a name="manage-finance-and-operations-updates-and-your-custom-code-lifecycle"></a><span data-ttu-id="ee806-103">Finance and Operations の更新とカスタム コード ライフサイクルの管理</span><span class="sxs-lookup"><span data-stu-id="ee806-103">Manage Finance and Operations updates and your custom code lifecycle</span></span>

<span data-ttu-id="ee806-104">このトピックでは、Finance and Operations 実装のアプリケーション ライフサイクル ユース ケースについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ee806-104">This topic describes application lifecycle use cases for Finance and Operations implementations.</span></span> <span data-ttu-id="ee806-105">次のシナリオに焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="ee806-105">It's focused on the following scenarios:</span></span>

+ <span data-ttu-id="ee806-106">ソースコードの開発分岐の管理</span><span class="sxs-lookup"><span data-stu-id="ee806-106">Managing your source code development branches</span></span>
+ <span data-ttu-id="ee806-107">Microsoft サービス更新プログラムの次のバージョンの適用</span><span class="sxs-lookup"><span data-stu-id="ee806-107">Applying the next version of a Microsoft service update</span></span>
+ <span data-ttu-id="ee806-108">カスタム コードの新しいバージョンの適用</span><span class="sxs-lookup"><span data-stu-id="ee806-108">Applying a new version of your custom code</span></span>

<span data-ttu-id="ee806-109">このトピックは Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce、Dynamics 365 Project Operations に適用されます。</span><span class="sxs-lookup"><span data-stu-id="ee806-109">This topic applies to Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="ee806-110">主な目的は、次のタスクを完了する方法を示すことです。</span><span class="sxs-lookup"><span data-stu-id="ee806-110">The main goal is to show how to complete the following tasks:</span></span>

+ <span data-ttu-id="ee806-111">独自のカスタマイズのライフサイクルに関係なく、段階的に Finance and Operations アプリ (Dynamics 365 Commerce を含む) の Microsoft サービス更新 (または品質更新プログラム) を最新の状態に保ち管理します。</span><span class="sxs-lookup"><span data-stu-id="ee806-111">Stay up to date and manage Microsoft service updates (or quality updates) for Finance and Operations apps (including Dynamics 365 Commerce) in incremental phases, independently of the lifecycle of your own customization.</span></span> <span data-ttu-id="ee806-112">この方法により、更新プロセスが簡略化され、オールインワン アップグレード プロジェクトに関連付けられているコストと回帰のリスクを軽減できます。</span><span class="sxs-lookup"><span data-stu-id="ee806-112">This approach simplifies the update process, and reduces the cost and risk of regressions that are associated with all-in-one upgrade projects.</span></span>
+ <span data-ttu-id="ee806-113">カスタム コードのバージョン管理にソース コード分岐を利用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-113">Take advantage of source code branches for version control of your custom code.</span></span> <span data-ttu-id="ee806-114">バージョン管理を使用することにより、新しい特徴や機能から重要な変更や修正プログラムのロールアウトを切り離すことができます。</span><span class="sxs-lookup"><span data-stu-id="ee806-114">By using version control, you can isolate the rollout of critical changes and hotfixes from the development of new features and capabilities.</span></span>

<span data-ttu-id="ee806-115">このトピックでは、Azure DevOps と Microsoft Dynamics Lifecycle Services (LCS) のさまざまなツールの使用方法については説明していません。</span><span class="sxs-lookup"><span data-stu-id="ee806-115">This topic doesn't explain how to use the different tools in Azure DevOps and Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ee806-116">代わりに、プロセスとベスト プラクティスに焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="ee806-116">Instead, it's focused on processes and best practices.</span></span> <span data-ttu-id="ee806-117">[Microsoft サービス更新プログラムの次のバージョンの適用](#apply-next-update) セクションと [カスタム コードの新しいバージョンの適用](#apply-new-custom-code) セクションには、フェーズの概要とプロセスの手順の両方が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee806-117">The [Apply the next version of a Microsoft service update](#apply-next-update) and [Apply a new version of your custom code](#apply-new-custom-code) sections contain both an overview of the phases and the steps of the process.</span></span>

<span data-ttu-id="ee806-118">このトピックは次のセクションを含みます:</span><span class="sxs-lookup"><span data-stu-id="ee806-118">This topic includes the following sections:</span></span>

+ [<span data-ttu-id="ee806-119">環境</span><span class="sxs-lookup"><span data-stu-id="ee806-119">Environments</span></span>](#environments)

    + [<span data-ttu-id="ee806-120">現在のリリースを実行する環境</span><span class="sxs-lookup"><span data-stu-id="ee806-120">Environments that run your current release</span></span>](#current-environments)
    + [<span data-ttu-id="ee806-121">カスタム コードの次のバージョンを実行する環境</span><span class="sxs-lookup"><span data-stu-id="ee806-121">Environments that run the next version of your custom code</span></span>](#next-environments)

+ [<span data-ttu-id="ee806-122">ソース コード分岐の管理</span><span class="sxs-lookup"><span data-stu-id="ee806-122">Manage source code branches</span></span>](#manage-source-code-branches)
+ [<span data-ttu-id="ee806-123">Microsoft サービス更新プログラムの次のバージョンを適用する</span><span class="sxs-lookup"><span data-stu-id="ee806-123">Apply the next version of a Microsoft service update</span></span>](#apply-next-update)

    + [<span data-ttu-id="ee806-124">Microsoft 更新プログラムの下位互換性</span><span class="sxs-lookup"><span data-stu-id="ee806-124">Backward compatibility of Microsoft updates</span></span>](#compatibility)

        + [<span data-ttu-id="ee806-125">ランタイムの互換性</span><span class="sxs-lookup"><span data-stu-id="ee806-125">Runtime compatibility</span></span>](#runtime-compatibility)
        + [<span data-ttu-id="ee806-126">デザイン時の互換性</span><span class="sxs-lookup"><span data-stu-id="ee806-126">Design-time compatibility</span></span>](#design-compatibility)

    + [<span data-ttu-id="ee806-127">フェーズ 1: Finance and Operations 実装の更新</span><span class="sxs-lookup"><span data-stu-id="ee806-127">Phase 1: Update the Finance and Operations implementation</span></span>](#phase-1)

        + [<span data-ttu-id="ee806-128">トラック 1: ランタイム環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-128">Track 1: Update your runtime environments</span></span>](#update-finops-runtime)

            + [<span data-ttu-id="ee806-129">テスト 1 を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-129">Update Test 1</span></span>](#update-test-1)
            + [<span data-ttu-id="ee806-130">UAT を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-130">Update UAT</span></span>](#update-uat)
            + [<span data-ttu-id="ee806-131">製品を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-131">Update Prod</span></span>](#update-prod)

        + [<span data-ttu-id="ee806-132">トラック 2: 開発環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-132">Track 2: Update your development environments</span></span>](#update-finops-dev)
        + [<span data-ttu-id="ee806-133">エラー状況</span><span class="sxs-lookup"><span data-stu-id="ee806-133">Error situations</span></span>](#error-situations)

            + [<span data-ttu-id="ee806-134">ケース 1</span><span class="sxs-lookup"><span data-stu-id="ee806-134">Case 1</span></span>](#case-1)
            + [<span data-ttu-id="ee806-135">ケース 2</span><span class="sxs-lookup"><span data-stu-id="ee806-135">Case 2</span></span>](#case-2)
            + [<span data-ttu-id="ee806-136">ケース 3</span><span class="sxs-lookup"><span data-stu-id="ee806-136">Case 3</span></span>](#case-3)

    + [<span data-ttu-id="ee806-137">フェーズ2: CSU をバージョン 10.0.11 に更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-137">Phase 2: Update CSU to version 10.0.11</span></span>](#phase-2)

        + [<span data-ttu-id="ee806-138">フェーズ 2 の前提条件</span><span class="sxs-lookup"><span data-stu-id="ee806-138">Phase 2 prerequisites</span></span>](#phase2-prerequisites)
        + [<span data-ttu-id="ee806-139">トラック 1: CSU ランタイム環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-139">Track 1: Update your CSU runtime environments</span></span>](#update-csu)

            + [<span data-ttu-id="ee806-140">テスト 1 を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-140">Update Test 1</span></span>](#update-test-1-csu)
            + [<span data-ttu-id="ee806-141">UAT を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-141">Update UAT</span></span>](#update-uat-csu)
            + [<span data-ttu-id="ee806-142">製品を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-142">Update Prod</span></span>](#update-prod-csu)

        + [<span data-ttu-id="ee806-143">トラック 2: 開発環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-143">Track 2: Update your development environments</span></span>](#update-csu-dev)

    + [<span data-ttu-id="ee806-144">フェーズ 3: POS をバージョン 10.0.11 に更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-144">Phase 3: Update POS to version 10.0.11</span></span>](#phase-3)

        + [<span data-ttu-id="ee806-145">フェーズ 3 の前提条件</span><span class="sxs-lookup"><span data-stu-id="ee806-145">Phase 3 prerequisites</span></span>](#phase3-prerequisites)
        + [<span data-ttu-id="ee806-146">Commerce 開発環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-146">Update your Commerce development environment</span></span>](#update-your-commerce-development-environment)
        + [<span data-ttu-id="ee806-147">オプション1: ランタイムの変更のみを含むストア コンポーネントを更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-147">Option 1: Store component updates that include only runtime changes</span></span>](#store-runtime-only)
        + [<span data-ttu-id="ee806-148">オプション2: ランタイムとカスタムの変更を含むストア コンポーネントを更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-148">Option 2: Store component updates that include runtime and custom changes</span></span>](#store-runtime-custom)
        + [<span data-ttu-id="ee806-149">プロセスを更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-149">Update Process</span></span>](#update-process)

            + [<span data-ttu-id="ee806-150">テスト 1 を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-150">Update Test 1</span></span>](#update-test-1)
            + [<span data-ttu-id="ee806-151">UAT を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-151">Update UAT</span></span>](#update-uat)
            + [<span data-ttu-id="ee806-152">製品を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-152">Update Prod</span></span>](#update-prod)

+ [<span data-ttu-id="ee806-153">カスタム コードの新しいバージョンを適用する</span><span class="sxs-lookup"><span data-stu-id="ee806-153">Apply a new version of your custom code</span></span>](#apply-new-custom-code)

    + [<span data-ttu-id="ee806-154">コードの修正プログラムを作成する</span><span class="sxs-lookup"><span data-stu-id="ee806-154">Create a hotfix of your code</span></span>](#create-hotfix)
    + [<span data-ttu-id="ee806-155">カスタム コードをリリース N からリリース N+1 に更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-155">Update your custom code from release N to release N+1</span></span>](#update-custom-code)

+ [<span data-ttu-id="ee806-156">ストア コンポーネントをアップロード、更新、および配置する</span><span class="sxs-lookup"><span data-stu-id="ee806-156">Upload, update, and deploy store components</span></span>](#upload-store-components)

## <a name="environments"></a><a id="environments"></a><span data-ttu-id="ee806-157">環境</span><span class="sxs-lookup"><span data-stu-id="ee806-157">Environments</span></span>

<span data-ttu-id="ee806-158">このセクションでは、このトピックのアプリケーション ライフサイクル管理 (ALM) シナリオが依存する Finance and Operations 環境のコレクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ee806-158">This section describes the collection of Finance and Operations environments that the application lifecycle management (ALM) scenarios in this topic rely on.</span></span> <span data-ttu-id="ee806-159">この構成は、カスタム コード (拡張機能) に依存する実装がある組織では一般的です。</span><span class="sxs-lookup"><span data-stu-id="ee806-159">This configuration is typical for organizations that have implementations that rely on custom code (extensions).</span></span> <span data-ttu-id="ee806-160">このカスタム コードには、独立系ソフトウェア ベンダー (ISV) によって提供されるカスタマイズが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee806-160">This custom code includes customizations that are provided by independent software vendors (ISVs).</span></span>

### <a name="environments-that-run-your-current-release"></a><a id="current-environments"></a><span data-ttu-id="ee806-161">現在のリリースを実行する環境</span><span class="sxs-lookup"><span data-stu-id="ee806-161">Environments that run your current release</span></span>

<span data-ttu-id="ee806-162">次の環境は、現在のリリースの環境です。</span><span class="sxs-lookup"><span data-stu-id="ee806-162">The following environments are the environments in your current release:</span></span>

+ <span data-ttu-id="ee806-163">**開発 1** – 実稼働環境と同じバージョンの Finance and Operations アプリを実行する開発環境。</span><span class="sxs-lookup"><span data-stu-id="ee806-163">**Dev 1** – A development environment that runs the same version of Finance and Operations apps as the production environment.</span></span> <span data-ttu-id="ee806-164">開発 1 環境では、カスタム コードのバージョン管理に Azure DevOps を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-164">The Dev 1 environment uses Azure DevOps for version control of custom code.</span></span> <span data-ttu-id="ee806-165">これは、カスタム コードの現在のリリース分岐に接続されています。</span><span class="sxs-lookup"><span data-stu-id="ee806-165">It's connected to the current release branch of your custom code.</span></span> <span data-ttu-id="ee806-166">詳細については、[ソース コード分岐の管理](#manage-source-code-branches) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-166">For more information, see the [Manage source code branches](#manage-source-code-branches) section.</span></span>

    - <span data-ttu-id="ee806-167">クラウドとオンプレミスの両方の開発環境にはさまざまなオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="ee806-167">There are many options for development environments, both cloud and on-premises.</span></span> <span data-ttu-id="ee806-168">詳細については、トピック [開発環境の配置とアクセス](../dev-tools/access-instances.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-168">For more information, see [Deploy and access development environments](../dev-tools/access-instances.md).</span></span>
    - <span data-ttu-id="ee806-169">ビルドの自動化には、新しい Azure DevOps Hosted Agents 機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-169">For build automation, use the new Azure DevOps Hosted Agents functionality.</span></span> <span data-ttu-id="ee806-170">詳細については、[Microsoft ホステッド エージェントと Azure Pipelines を使用するビルドの自動化](../dev-tools/hosted-build-automation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-170">For more information, see [Build automation that uses Microsoft-hosted agents and Azure Pipelines](../dev-tools/hosted-build-automation.md).</span></span>

+ <span data-ttu-id="ee806-171">**テスト 1** – 機能テストと構成テストに使用されるレベル 1 テスト環境。</span><span class="sxs-lookup"><span data-stu-id="ee806-171">**Test 1** – A Tier-1 test environment that is used for functional and configuration testing.</span></span> <span data-ttu-id="ee806-172">テスト 1 環境は、実稼働環境と同じバージョンの Finance and Operations アプリを実行します。</span><span class="sxs-lookup"><span data-stu-id="ee806-172">The Test 1 environment runs the same version of Finance and Operations apps as the production environment.</span></span> <span data-ttu-id="ee806-173">また、カスタム コード拡張機能の最新のリリースバージョンも実行します。</span><span class="sxs-lookup"><span data-stu-id="ee806-173">It also runs the latest release version of your custom code extensions.</span></span>
+ <span data-ttu-id="ee806-174">**UAT** – ユーザー受け入れテストに使用される実稼働前の環境。</span><span class="sxs-lookup"><span data-stu-id="ee806-174">**UAT** – A pre-production environment that is used for user acceptance testing.</span></span> <span data-ttu-id="ee806-175">UAT 環境は、レベル 2 (標準承認テスト) またはそれ以上の環境です。</span><span class="sxs-lookup"><span data-stu-id="ee806-175">The UAT environment is a Tier-2 (Standard Acceptance Test) or higher environment.</span></span> <span data-ttu-id="ee806-176">実稼働環境と同じバージョンの Finance and Operations アプリを実行します。</span><span class="sxs-lookup"><span data-stu-id="ee806-176">It runs the same version of Finance and Operations apps as the production environment.</span></span> <span data-ttu-id="ee806-177">また、カスタム コード拡張機能の最新のリリースバージョンも実行します。</span><span class="sxs-lookup"><span data-stu-id="ee806-177">It also runs the latest release version of your custom code extensions.</span></span> <span data-ttu-id="ee806-178">この環境は通常、運用データベースのコピーに接続されています。</span><span class="sxs-lookup"><span data-stu-id="ee806-178">This environment is typically connected to a copy of the production database.</span></span>
+ <span data-ttu-id="ee806-179">**生産** – 運用データベースで実行される実際の実稼動環境。</span><span class="sxs-lookup"><span data-stu-id="ee806-179">**Prod** – Your live production environment that runs on your production database.</span></span>

:::image type="content" source="media/uguide-environments.png" alt-text="現在のリリースを実行する環境":::

### <a name="environments-that-run-the-next-version-of-your-custom-code"></a><a id="next-environments"></a><span data-ttu-id="ee806-181">カスタム コードの次のバージョンを実行する環境</span><span class="sxs-lookup"><span data-stu-id="ee806-181">Environments that run the next version of your custom code</span></span>

<span data-ttu-id="ee806-182">次の環境では、カスタム コードの次のバージョンを実行します。</span><span class="sxs-lookup"><span data-stu-id="ee806-182">The following environments run the next version of your custom code:</span></span>

- <span data-ttu-id="ee806-183">**開発 2** – カスタム コード拡張機能の次のバージョンの開発に使用される開発環境。</span><span class="sxs-lookup"><span data-stu-id="ee806-183">**Dev 2** – A development environment that is used for development of the next version of your custom code extensions.</span></span> <span data-ttu-id="ee806-184">カスタム コードのバージョン 管理に Azure DevOps を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-184">It uses Azure DevOps for version control of custom code.</span></span> <span data-ttu-id="ee806-185">これは、カスタム コードの現在の開発分岐 (**メイン** ブランチ) に接続されています。</span><span class="sxs-lookup"><span data-stu-id="ee806-185">It's connected to the development branch (**main** branch) of your custom code.</span></span> <span data-ttu-id="ee806-186">詳細については、[ソース コード分岐の管理](#manage-source-code-branches) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-186">For more information, see the [Manage source code branches](#manage-source-code-branches) section.</span></span>
- <span data-ttu-id="ee806-187">**テスト 2** – カスタム コード拡張機能の次のバージョンのテストに使用される機能テスト環境。</span><span class="sxs-lookup"><span data-stu-id="ee806-187">**Test 2** – A functional test environment that is used for testing of the next version of your custom code extensions.</span></span>

:::image type="content" source="media/uguide-next-environments.png" alt-text="カスタム コードの次のバージョンを実行する環境":::

## <a name="manage-source-code-branches"></a><span data-ttu-id="ee806-189">ソース コード分岐の管理</span><span class="sxs-lookup"><span data-stu-id="ee806-189">Manage source code branches</span></span>

<span data-ttu-id="ee806-190">カスタム コード分岐を管理する場合は、ベスト プラクティスに従うことが重要です。</span><span class="sxs-lookup"><span data-stu-id="ee806-190">It's important that you follow best practices as you manage branches of custom code.</span></span> <span data-ttu-id="ee806-191">これにより、原価を最小限に抑え、リリースと更新の品質を保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ee806-191">In this way, you help minimize cost, and ensure the quality of your releases and updates.</span></span>

:::image type="content" source="media/uguide-branches.png" alt-text="ソース コード分岐の管理":::

<span data-ttu-id="ee806-193">**メイン** 分岐 (開発分岐) には、コードの次期リリースの最新の機能バージョンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee806-193">The **main** branch (development branch) contains the latest functioning version of the next release of your code.</span></span>

<span data-ttu-id="ee806-194">新しい機能で作業する場合は、**メイン** 分岐から新しい機能分岐を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-194">When you work on new features, create a new feature branch out of the **main** branch.</span></span> <span data-ttu-id="ee806-195">機能作業が完了したら、機能分岐を **メイン** 分岐に統合します。</span><span class="sxs-lookup"><span data-stu-id="ee806-195">Then, when the feature work is completed, integrate the feature branch back into the **main** branch.</span></span>

<span data-ttu-id="ee806-196">リリース分岐には、公式リリースのコード ベースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee806-196">The release branches contain the code base of your official releases.</span></span> <span data-ttu-id="ee806-197">前の例では、リリース分岐が 1 つしかない、**リリース/2020-April** であることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="ee806-197">In the preceding illustration, the assumption is that you have only one release branch, **release/2020-April**.</span></span> <span data-ttu-id="ee806-198">**2020-April** はビルドではありません。</span><span class="sxs-lookup"><span data-stu-id="ee806-198">**2020-April** isn't a build.</span></span> <span data-ttu-id="ee806-199">ソース コード分岐です。</span><span class="sxs-lookup"><span data-stu-id="ee806-199">It's a source code branch.</span></span> <span data-ttu-id="ee806-200">リリースの修正プログラムを作成する可能性があるため、このリリース分岐に変更を加えてビルドを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-200">Because you will probably create hotfixes for your release, you will make changes and produce builds out of this release branch.</span></span>

- <span data-ttu-id="ee806-201">新しい機能の開発するためにリリース分岐を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="ee806-201">Don't use release branches to develop new features.</span></span> <span data-ttu-id="ee806-202">実際の環境で必要な重要な修正や変更についてのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-202">Use them only for critical fixes or changes that are required in your live environment.</span></span>
- <span data-ttu-id="ee806-203">リリース分岐に変更を加えた後、分岐を **メイン** 分岐に統合し直します。</span><span class="sxs-lookup"><span data-stu-id="ee806-203">After you've made a change in a release branch, integrate the branch back into the **main** branch.</span></span> <span data-ttu-id="ee806-204">このようにして、次のリリースにも修正を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ee806-204">In this way, you ensure that your next release also contains the fix.</span></span>
- <span data-ttu-id="ee806-205">先に説明した環境の例の中で、開発 1 環境は、**リリース/2020-April** 分岐に接続されます。</span><span class="sxs-lookup"><span data-stu-id="ee806-205">Among the example environments that were described earlier, the Dev 1 environment will be connected to the **release/2020-April** branch.</span></span>

<span data-ttu-id="ee806-206">カスタム コードの新しいバージョンをリリースする準備ができたら、**メイン** 分岐に基づく新しいリリース分岐を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-206">When you're ready to release a new version of your custom code, create a new release branch that is based on the **main** branch.</span></span> <span data-ttu-id="ee806-207">この例では、**メイン** に基づいて **2020-July** という名前の新しいリリース分岐を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-207">For this example, you will create a new release branch that is based on **main** and named **2020-July**.</span></span>

<span data-ttu-id="ee806-208">コードの特定の分岐に基づく特定の作業項目で作業しているときに、個々の開発者が作業するプライベート分岐がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-208">You might have private branches that individual developers work in while they work on a specific work item that is based on a specific branch of your code.</span></span> <span data-ttu-id="ee806-209">作業が完了すると、プライベート分岐は親分岐にマージされます。</span><span class="sxs-lookup"><span data-stu-id="ee806-209">Private branches are merged back into their parent branch when the work is completed.</span></span> <span data-ttu-id="ee806-210">詳細については、[Team Foundation バージョン管理 (TFVC) の分岐戦略と効果的な戦略の選択方法について](https://docs.microsoft.com/azure/devops/repos/tfvc/branching-strategies-with-tfvc) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-210">For more information, see [Learn about branching strategies for Team Foundation Version Control (TFVC) and how to select an effective strategy](https://docs.microsoft.com/azure/devops/repos/tfvc/branching-strategies-with-tfvc).</span></span>

## <a name="apply-the-next-version-of-a-microsoft-service-update"></a><a id="apply-next-update"></a><span data-ttu-id="ee806-211">Microsoft サービス更新プログラムの次のバージョンを適用する</span><span class="sxs-lookup"><span data-stu-id="ee806-211">Apply the next version of a Microsoft service update</span></span>

<span data-ttu-id="ee806-212">段階的なアプローチを使用することで、サービス更新が行われるときに効率を最大化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ee806-212">By using a phased approach, you help maximize the efficiency when service updates are taken.</span></span> <span data-ttu-id="ee806-213">各フェーズは、実装の 1 つのコンポーネントを更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-213">Each phase updates one component of your implementation.</span></span>

1. <span data-ttu-id="ee806-214">**フェーズ 1** – Finance and Operations 環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-214">**Phase 1** – Update your Finance and Operations environments.</span></span>

    <span data-ttu-id="ee806-215">現在のバージョンの Commerce Scale Unit (CSU) および Point of Sale (POS) は、新しい Finance and Operations 更新プログラムで正常に機能します。</span><span class="sxs-lookup"><span data-stu-id="ee806-215">Your current version of Commerce Scale Unit (CSU) and Point of Sale (POS) will work correctly with the new Finance and Operations update.</span></span> <span data-ttu-id="ee806-216">たとえば、CSU のバージョン 10.0.7 は、Finance and Operations アプリのバージョン 10.0.11 と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-216">For example, version 10.0.7 of CSU is compatible with version 10.0.11 of Finance and Operations apps.</span></span>

2. <span data-ttu-id="ee806-217">**フェーズ 2** – CSU を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-217">**Phase 2** – Update CSU.</span></span>
3. <span data-ttu-id="ee806-218">**フェーズ 3** – POS を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-218">**Phase 3** – Update POS.</span></span>

<span data-ttu-id="ee806-219">Microsoft 更新プログラムを取得する場合、カスタム コードを次のバージョンに更新する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ee806-219">When you take a Microsoft update, you don't have to update your custom code to the next version.</span></span> <span data-ttu-id="ee806-220">カスタム コードの更新プログラムとバンドルせずに Microsoft 更新プログラムを取得することにより、更新プロセスを簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="ee806-220">By taking Microsoft updates without bundling them with custom code updates, you help simplify the update process.</span></span> <span data-ttu-id="ee806-221">また、オールインワン アップグレード プロジェクトに関連付けられている回帰の費用とリスクを軽減することにもなります。</span><span class="sxs-lookup"><span data-stu-id="ee806-221">You also help reduce the cost and risk of regressions that are associated with all-in-one upgrade projects.</span></span>

### <a name="backward-compatibility-of-microsoft-updates"></a><a id="compatibility"></a><span data-ttu-id="ee806-222">Microsoft 更新プログラムの下位互換性</span><span class="sxs-lookup"><span data-stu-id="ee806-222">Backward compatibility of Microsoft updates</span></span>

<span data-ttu-id="ee806-223">このトピックの次のセクションのコンテキストを理解できるように、*サービス更新プログラムの下位互換性* によって、Microsoft の手段を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="ee806-223">It's important that you understand what Microsoft means by *backward compatibility of service updates*, so that you have context for the next sections of this topic.</span></span> <span data-ttu-id="ee806-224">サービスと品質の更新には、*ランタイム* の下位互換性があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-224">Service and quality updates are *runtime* backward-compatible.</span></span> <span data-ttu-id="ee806-225">ただし、常に *デザイン時* (*コンパイル時*) に下位互換性があるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="ee806-225">However, they aren't always *design-time* (*compile-time*) backward-compatible.</span></span>

#### <a name="runtime-compatibility"></a><a id="runtime-compatibility"></a><span data-ttu-id="ee806-226">ランタイムの互換性</span><span class="sxs-lookup"><span data-stu-id="ee806-226">Runtime compatibility</span></span>

<span data-ttu-id="ee806-227">すべての Microsoft 更新プログラムは、ランタイムの下位互換性を保つことを意図しています。</span><span class="sxs-lookup"><span data-stu-id="ee806-227">All Microsoft updates are intended to be runtime backward-compatible.</span></span> <span data-ttu-id="ee806-228">この互換性はバイナリ互換性と機能互換性の両方を対象にしています。</span><span class="sxs-lookup"><span data-stu-id="ee806-228">This compatibility covers both binary compatibility and functional compatibility.</span></span> <span data-ttu-id="ee806-229">ランタイム互換性とは、実稼働環境およびサンドボックス環境に存在するカスタマイズが、それらの環境に Microsoft サービス更新プログラムが配置された後も引き続き機能することを意味します。</span><span class="sxs-lookup"><span data-stu-id="ee806-229">Runtime compatibility means that customizations that exist in production and sandbox environments will continue to work after Microsoft service updates are deployed to those environments.</span></span> <span data-ttu-id="ee806-230">それらの更新プログラムは、サービス更新と品質更新を含みます。</span><span class="sxs-lookup"><span data-stu-id="ee806-230">Those updates include service updates and quality updates.</span></span> <span data-ttu-id="ee806-231">ランタイムの互換性は、Microsoft 更新プログラムが以前のプラットフォームでコンパイルされたカスタマイズと下位互換性があることも意味します。</span><span class="sxs-lookup"><span data-stu-id="ee806-231">Runtime compatibility also means that Microsoft updates are backward-compatible with customizations that were compiled on an earlier platform.</span></span>

<span data-ttu-id="ee806-232">バイナリ互換性は、後方向のみです。</span><span class="sxs-lookup"><span data-stu-id="ee806-232">Binary compatibility is backward only.</span></span> <span data-ttu-id="ee806-233">古いアプリケーション バージョンとプラットフォーム バージョンでカスタマイズをコンパイルし、それを新しいバージョンを実行している環境に配置できます。</span><span class="sxs-lookup"><span data-stu-id="ee806-233">You can compile a customization on an older application version and platform version, and deploy it to an environment that is running a later version.</span></span> <span data-ttu-id="ee806-234">ただし、コードがコンパイルされたバージョンよりも前のバージョンを実行している環境にコードを配置することはできません。</span><span class="sxs-lookup"><span data-stu-id="ee806-234">However, you can't deploy code to an environment that is running a version that is earlier than the version that the code was compiled on.</span></span>

#### <a name="design-time-compatibility"></a><a id="design-compatibility"></a><span data-ttu-id="ee806-235">デザイン時の互換性</span><span class="sxs-lookup"><span data-stu-id="ee806-235">Design-time compatibility</span></span>

<span data-ttu-id="ee806-236">デザイン時 (コンパイル時) の下位互換性とは、開発者が開発環境に更新を適用し、変更を加えることなくコードが正常にコンパイルできることを意味します。</span><span class="sxs-lookup"><span data-stu-id="ee806-236">Design-time (compile-time) backward compatibility means that developers can apply updates to their development environments and successfully compile their code without having to make any changes.</span></span>

<span data-ttu-id="ee806-237">Microsoft は、デザイン時の互換性を目指しています。</span><span class="sxs-lookup"><span data-stu-id="ee806-237">Microsoft aims for design-time compatibility.</span></span> <span data-ttu-id="ee806-238">ただし、一部の更新には、デザイン時には互換性がないが、バイナリ互換性のある変更が含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-238">However, some updates might include changes that aren't compatible at design time, but that are binary-compatible.</span></span> <span data-ttu-id="ee806-239">そのため、更新プログラムが適用された後、コードのコンパイル時に新しいエラーまたは警告が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-239">Therefore, after an update is applied, new errors or warnings might occur when your code is compiled.</span></span> <span data-ttu-id="ee806-240">これらの変更の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ee806-240">Here are some examples of these changes:</span></span>

+ <span data-ttu-id="ee806-241">Microsoft は列挙型を拡張可能にします。</span><span class="sxs-lookup"><span data-stu-id="ee806-241">Microsoft makes an enumeration extensible.</span></span>
+ <span data-ttu-id="ee806-242">Microsoft は API を廃止または内部としてマークします。</span><span class="sxs-lookup"><span data-stu-id="ee806-242">Microsoft marks an API as obsolete or internal.</span></span>
+ <span data-ttu-id="ee806-243">Microsoft は安全でないコーディング方法を回避するために新しいコンパイラ エラーを導入します。</span><span class="sxs-lookup"><span data-stu-id="ee806-243">Microsoft introduces a new compiler error to help prevent unsafe coding practices.</span></span>

<span data-ttu-id="ee806-244">これらすべての変更はソリューションでの作業が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-244">All these changes might require work on your solution.</span></span> <span data-ttu-id="ee806-245">バイナリ互換であるデザイン時の重大な変更は、12 か月の廃止予定の通知を必要としません。</span><span class="sxs-lookup"><span data-stu-id="ee806-245">Design-time breaking changes that are binary-compatible don't require a 12-month deprecation notice.</span></span> <span data-ttu-id="ee806-246">これらの重大な変更は、サービスの更新ごとに文書化されています。</span><span class="sxs-lookup"><span data-stu-id="ee806-246">These breaking changes are documented for each service update.</span></span> <span data-ttu-id="ee806-247">詳細については、[プラットフォーム更新プログラムの新機能と変更された機能](../get-started/whats-new-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-247">For more information, see [What's new and changed in Platform updates](../get-started/whats-new-home-page.md).</span></span>

### <a name="phase-1-update-the-finance-and-operations-implementation"></a><a id="phase-1"></a><span data-ttu-id="ee806-248">フェーズ 1: Finance and Operations 実装の更新</span><span class="sxs-lookup"><span data-stu-id="ee806-248">Phase 1: Update the Finance and Operations implementation</span></span>

<span data-ttu-id="ee806-249">このセクションでは、Finance and Operations 実装を最新のサービス更新プログラムに更新するために使用するプロセスについて要約します。</span><span class="sxs-lookup"><span data-stu-id="ee806-249">This section summarizes the process that you use to update your Finance and Operations implementation to the latest service update.</span></span> <span data-ttu-id="ee806-250">バージョン 10.0.7 からバージョン 10.0.11 への更新が例として使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee806-250">An update from version 10.0.7 to version 10.0.11 is used as an example.</span></span>

<span data-ttu-id="ee806-251">このフェーズは次の 2 つのトラックに分かれています。</span><span class="sxs-lookup"><span data-stu-id="ee806-251">This phase is divided into two tracks.</span></span> <span data-ttu-id="ee806-252">これらのトラックは並列で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-252">These tracks can occur in parallel.</span></span>

- <span data-ttu-id="ee806-253">**トラック 1** – ランタイム環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-253">**Track 1** – Update your runtime environments.</span></span>
- <span data-ttu-id="ee806-254">**トラック 2** – 開発環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-254">**Track 2** – Update your development environments.</span></span>

<span data-ttu-id="ee806-255">トラック 1 を完了すると、[エラーの状況](#error-situations) セクションで説明されているエラー状況のいずれかが発生しない限り、バージョン 10.0.11 で有効になります。</span><span class="sxs-lookup"><span data-stu-id="ee806-255">After you complete track 1, you will be live on version 10.0.11, unless you encounter one of the error situations that are described in the [Error situations](#error-situations) section.</span></span>

#### <a name="track-1-update-your-runtime-environments"></a><a id="update-finops-runtime"></a><span data-ttu-id="ee806-256">トラック 1: ランタイム環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-256">Track 1: Update your runtime environments</span></span>

<span data-ttu-id="ee806-257">トラック 1 を完成すると、実稼働環境はバージョン 10.0.11 で有効になるため、基本的に Finance and Operations バージョン 10.0.11 への更新が完了します。</span><span class="sxs-lookup"><span data-stu-id="ee806-257">By completing track 1, you essentially complete your Finance and Operations update to version 10.0.11, because your production environment will be live on version 10.0.11.</span></span> <span data-ttu-id="ee806-258">このトラックの一部としてカスタム コードを再コンパイルする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ee806-258">You don't have to recompile your custom code as part of this track.</span></span>

##### <a name="update-test-1"></a><span data-ttu-id="ee806-259">更新テスト 1</span><span class="sxs-lookup"><span data-stu-id="ee806-259">Update Test 1</span></span>

<span data-ttu-id="ee806-260">テスト 1 環境は、カスタム拡張機能の最新のリリース バージョンと共にバージョン 10.0.7 を実行しています。</span><span class="sxs-lookup"><span data-stu-id="ee806-260">The Test 1 environment is running version 10.0.7 together with the latest released version of your custom extension.</span></span> <span data-ttu-id="ee806-261">テスト 1 の更新はこのフローの前提条件ではありませんが、機能検証と予測可能性の別のレベルを追加するため、それをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ee806-261">Although an update of Test 1 isn't a prerequisite in this flow, it's recommended, because it adds another level of functional verification and predictability.</span></span> <span data-ttu-id="ee806-262">この更新は、UAT 環境を更新する前に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-262">This update should be completed before the UAT environment is updated.</span></span> <span data-ttu-id="ee806-263">テスト 1 を更新して検証するのが早ければ早いほど、「実際」の更新 (つまり、UAT および製品環境の更新) がより予測可能になります。</span><span class="sxs-lookup"><span data-stu-id="ee806-263">The sooner that you update Test 1 and validate on it, the more predictable your "real" update (that is, the update of the UAT and Prod environments) will be.</span></span>

1. <span data-ttu-id="ee806-264">Finance and Operations アプリのバージョン 10.0.11 をテスト 1 に適用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-264">Apply version 10.0.11 of Finance and Operations apps to Test 1.</span></span>
2. <span data-ttu-id="ee806-265">機能シナリオを承認します。</span><span class="sxs-lookup"><span data-stu-id="ee806-265">Sign off on functional scenarios.</span></span> <span data-ttu-id="ee806-266">[Regression Suite Automation Tool](../perf-test/rsat/rsat-overview.md) を使用すると、テスト環境および UAT 環境でのユーザー受け入れテストを自動化できます。</span><span class="sxs-lookup"><span data-stu-id="ee806-266">You can use the [Regression Suite Automation Tool](../perf-test/rsat/rsat-overview.md) to automate user acceptance testing on test and UAT environments.</span></span>
3. <span data-ttu-id="ee806-267">回帰が発生した場合は、[エラー状況](#error-situations) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-267">If regressions are encountered, see the [Error situations](#error-situations) section.</span></span>

##### <a name="update-uat"></a><span data-ttu-id="ee806-268">UAT の更新</span><span class="sxs-lookup"><span data-stu-id="ee806-268">Update UAT</span></span>

<span data-ttu-id="ee806-269">UAT 環境は、カスタム拡張機能のリリース バージョンと共にバージョン 10.0.7 を実行しています。</span><span class="sxs-lookup"><span data-stu-id="ee806-269">The UAT environment is running version 10.0.7 together with a released version of your custom extension.</span></span> <span data-ttu-id="ee806-270">(UAT 環境は、製品環境と同じです。)</span><span class="sxs-lookup"><span data-stu-id="ee806-270">(The UAT environment is the same as the Prod environment.)</span></span>

1. <span data-ttu-id="ee806-271">Finance and Operations アプリのバージョン 10.0.11 を UAT に適用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-271">Apply version 10.0.11 of Finance and Operations apps to UAT.</span></span>

    <span data-ttu-id="ee806-272">UAT 環境は、Microsoft によって自動的に更新されるように構成されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-272">Your UAT environment might be configured so that it's automatically updated by Microsoft.</span></span> <span data-ttu-id="ee806-273">ただし、更新が使用可能になり次第、いつでもプルできます。</span><span class="sxs-lookup"><span data-stu-id="ee806-273">However, you can always pull the update as soon as it's available.</span></span>

2. <span data-ttu-id="ee806-274">ユーザー受け入れテストを完了し、サイン オフします。</span><span class="sxs-lookup"><span data-stu-id="ee806-274">Complete user acceptance testing, and sign off.</span></span>
3. <span data-ttu-id="ee806-275">回帰が発生した場合は、[エラー状況](#error-situations) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-275">If regressions are encountered, see the [Error situations](#error-situations) section.</span></span>

##### <a name="update-prod"></a><span data-ttu-id="ee806-276">製品の更新</span><span class="sxs-lookup"><span data-stu-id="ee806-276">Update Prod</span></span>

1. <span data-ttu-id="ee806-277">Finance and Operations アプリのバージョン 10.0.11 を製品に適用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-277">Apply version 10.0.11 of Finance and Operations apps to Prod.</span></span>

    <span data-ttu-id="ee806-278">製品環境は、Microsoft によって自動的に更新されるように構成されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-278">Your Prod environment might be configured so that it's automatically updated by Microsoft.</span></span> <span data-ttu-id="ee806-279">ただし、更新が使用可能になり次第、いつでもプルできます。</span><span class="sxs-lookup"><span data-stu-id="ee806-279">However, you can always pull the update as soon as it's available.</span></span>

2. <span data-ttu-id="ee806-280">サイン オフします。</span><span class="sxs-lookup"><span data-stu-id="ee806-280">Sign off.</span></span>

#### <a name="track-2-update-your-development-environments"></a><a id="update-finops-dev"></a><span data-ttu-id="ee806-281">トラック 2: 開発環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-281">Track 2: Update your development environments</span></span>

<span data-ttu-id="ee806-282">トラック 2 の目的は、開発 1 環境をバージョン 10.0.11 に更新することです。</span><span class="sxs-lookup"><span data-stu-id="ee806-282">The purpose of track 2 is to update the Dev 1 environment to version 10.0.11.</span></span> <span data-ttu-id="ee806-283">開発 1 は、カスタム コードの現在のリリース ブランチに接続されている **メイン** 開発環境です。</span><span class="sxs-lookup"><span data-stu-id="ee806-283">Dev 1 is your **main** development environment that is connected to the current release branch of your custom code.</span></span> <span data-ttu-id="ee806-284">Finance and Operations アプリのバージョン 10.0.7 を実行しています。</span><span class="sxs-lookup"><span data-stu-id="ee806-284">It's running version 10.0.7 of Finance and Operations apps.</span></span> <span data-ttu-id="ee806-285">トラック 2 を完了することで、開発 1 が最新リリースと共にバージョン 10.0.11 を実行し、コードに必要な将来の修正プログラムの準備が整います。</span><span class="sxs-lookup"><span data-stu-id="ee806-285">By completing track 2, you ensure that Dev 1 runs version 10.0.11 together with your latest release, and that it's ready for any future hotfixes that are required for your code.</span></span>

1. <span data-ttu-id="ee806-286">Finance and Operations アプリのバージョン 10.0.11 を開発 1 に適用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-286">Apply version 10.0.11 of Finance and Operations apps to Dev 1.</span></span>
2. <span data-ttu-id="ee806-287">カスタム コードをコンパイルし、テストを行います。</span><span class="sxs-lookup"><span data-stu-id="ee806-287">Compile your custom code, and do testing.</span></span>
3. <span data-ttu-id="ee806-288">カスタム コードに必要な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="ee806-288">Make any required changes to your custom code.</span></span>
4. <span data-ttu-id="ee806-289">リリース ブランチへのコードの変更を確認ししてください。</span><span class="sxs-lookup"><span data-stu-id="ee806-289">Check code changes in to the release branch.</span></span>
5. <span data-ttu-id="ee806-290">複数の開発環境がある場合は、環境ごとに次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ee806-290">If you have more than one development environment, follow these steps for each environment:</span></span>

    1. <span data-ttu-id="ee806-291">Finance and Operations アプリのバージョン 10.0.11 を開発環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-291">Apply version 10.0.11 of Finance and Operations apps to the development environment.</span></span>
    2. <span data-ttu-id="ee806-292">ターゲット コード ブランチから、最新のカスタム コードを同期してコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="ee806-292">Sync and compile your latest custom code from the target code branch.</span></span>

#### <a name="error-situations"></a><span data-ttu-id="ee806-293">エラー状況</span><span class="sxs-lookup"><span data-stu-id="ee806-293">Error situations</span></span>

##### <a name="case-1"></a><span data-ttu-id="ee806-294">ケース 1</span><span class="sxs-lookup"><span data-stu-id="ee806-294">Case 1</span></span>

<span data-ttu-id="ee806-295">トラック 1 で、Microsoft 品質更新プログラムを必要とするバグが検出されました。</span><span class="sxs-lookup"><span data-stu-id="ee806-295">During track 1, a bug is found that requires a Microsoft quality update.</span></span> <span data-ttu-id="ee806-296">Microsoft が更新プログラムを適切なタイミングでリリースする場合、元のサービス更新プログラムの代わりに新しい Microsoft 更新プログラムを使用して、トラック 1 を完了します。</span><span class="sxs-lookup"><span data-stu-id="ee806-296">If Microsoft releases the update in a timely manner, use the new Microsoft update instead of the original service update to complete track 1.</span></span>

##### <a name="case-2"></a><span data-ttu-id="ee806-297">ケース 2</span><span class="sxs-lookup"><span data-stu-id="ee806-297">Case 2</span></span>

<span data-ttu-id="ee806-298">トラック 1 で、Microsoft サービス更新プログラムを必要とするバグが検出されました。</span><span class="sxs-lookup"><span data-stu-id="ee806-298">During track 1, a bug is found that requires a Microsoft service update.</span></span> <span data-ttu-id="ee806-299">ただし、更新を適切なタイミングでリリースすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ee806-299">However, the update can't be released in a timely manner.</span></span>

<span data-ttu-id="ee806-300">この問題の回避策として、Microsoft はカスタム コードの変更を提案します。</span><span class="sxs-lookup"><span data-stu-id="ee806-300">As a workaround for this issue, Microsoft proposes a change to your custom code.</span></span>

1. <span data-ttu-id="ee806-301">開発 1 (リリース分岐内) のコードを変更し、更新をテストします。</span><span class="sxs-lookup"><span data-stu-id="ee806-301">Modify your code in Dev 1 (in the release branch), and test your updates.</span></span>
2. <span data-ttu-id="ee806-302">リリース ブランチへのコードの変更を確認ししてください。</span><span class="sxs-lookup"><span data-stu-id="ee806-302">Check code changes in to the release branch.</span></span>
3. <span data-ttu-id="ee806-303">リリース分岐から新しい配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-303">Create a new deployable package out of the release branch.</span></span>
4. <span data-ttu-id="ee806-304">新しい配置可能なパッケージをテスト 1 および/または UAT に適用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-304">Apply the new deployable package to Test 1 and/or UAT.</span></span>

> [!NOTE]
> <span data-ttu-id="ee806-305">バージョン 10.0.7 でコンパイルされるカスタム コードは、バージョン 10.0.7 以降を実行している任意のランタイム環境に配置できます。</span><span class="sxs-lookup"><span data-stu-id="ee806-305">Custom code that is compiled on version 10.0.7 can be deployed to any runtime environment that is running version 10.0.7 or later.</span></span> <span data-ttu-id="ee806-306">したがって、まだ開発 1 をバージョン 10.0.11 に更新する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ee806-306">Therefore, you don't yet have to update Dev 1 to version 10.0.11.</span></span> <span data-ttu-id="ee806-307">ただし、トラック 2 の一部として既にその更新を完了している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-307">However, you might already have done that update as part of track 2.</span></span>

##### <a name="case-3"></a><span data-ttu-id="ee806-308">ケース 3</span><span class="sxs-lookup"><span data-stu-id="ee806-308">Case 3</span></span>

<span data-ttu-id="ee806-309">トラック 1 で、カスタム コードの変更が必要なバグが見つかりました。</span><span class="sxs-lookup"><span data-stu-id="ee806-309">During track 1, a bug is found that requires a change to your custom code.</span></span> <span data-ttu-id="ee806-310">このバグは、コードまたは ISV コードのいずれかにある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-310">This bug might be in either your code or the ISV code.</span></span>

1. <span data-ttu-id="ee806-311">開発 1 (リリース分岐内) のコードを変更し、更新をテストします。</span><span class="sxs-lookup"><span data-stu-id="ee806-311">Modify your code in Dev 1 (in the release branch), and test your updates.</span></span>
2. <span data-ttu-id="ee806-312">リリース ブランチへのコードの変更を確認ししてください。</span><span class="sxs-lookup"><span data-stu-id="ee806-312">Check code changes in to the release branch.</span></span>
3. <span data-ttu-id="ee806-313">リリース分岐から新しい配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-313">Create a new deployable package out of the release branch.</span></span>
4. <span data-ttu-id="ee806-314">新しい配置可能なパッケージをテスト 1 および/または UAT に適用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-314">Apply the new deployable package to Test 1 and/or UAT.</span></span>

### <a name="phase-2-update-csu-to-version-10011"></a><a id="phase-2"></a><span data-ttu-id="ee806-315">フェーズ2: CSU をバージョン 10.0.11 に更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-315">Phase 2: Update CSU to version 10.0.11</span></span>

<span data-ttu-id="ee806-316">このセクションでは、Commerce Scale Unit を最新のサービス更新プログラムに更新するために使用するプロセスについて要約します。</span><span class="sxs-lookup"><span data-stu-id="ee806-316">This section summarizes the process that you use to update your Commerce Scale Units to the latest service update.</span></span> <span data-ttu-id="ee806-317">リリース 10.0.7 (Commerce バージョン 9.17) からリリース 10.0.11 (Commerce バージョン 9.21) への更新が例として使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee806-317">An update from release 10.0.7 (Commerce version 9.17) to release 10.0.11 (Commerce version 9.21) is used as an example.</span></span>

#### <a name="phase-2-prerequisites"></a><a id="phase2-prerequisites"></a><span data-ttu-id="ee806-318">フェーズ 2 の前提条件</span><span class="sxs-lookup"><span data-stu-id="ee806-318">Phase 2 prerequisites</span></span>

<span data-ttu-id="ee806-319">CSU を更新する前に、(アプリ内の) Commerce 本部環境 (Finance and Operations アプリ内) を同じリリースまたはそれ以降のリリースに更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-319">Before you update your CSUs, you must update the Commerce headquarters environments (in the Finance and Operations app) to the same release or a later release.</span></span> <span data-ttu-id="ee806-320">この例では、10.0.11 がリリースされています。</span><span class="sxs-lookup"><span data-stu-id="ee806-320">For this example, that release is 10.0.11.</span></span>

<span data-ttu-id="ee806-321">このフェーズは次の 2 つのトラックに分かれています。</span><span class="sxs-lookup"><span data-stu-id="ee806-321">This phase is divided into two tracks.</span></span> <span data-ttu-id="ee806-322">これらのトラックは並列で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-322">These tracks can occur in parallel.</span></span>

- <span data-ttu-id="ee806-323">**トラック 1** – CSU ランタイム環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-323">**Track 1** – Update your CSU runtime environments.</span></span>
- <span data-ttu-id="ee806-324">**トラック 2** – 開発環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-324">**Track 2** – Update your development environments.</span></span>

<span data-ttu-id="ee806-325">トラック 1 を完了すると、フェーズ 1 で説明した [エラーの状況](#error-situations) のいずれかが発生しない限り、バージョン 10.0.11 (Commerce バージョン 9.21) で有効になります。</span><span class="sxs-lookup"><span data-stu-id="ee806-325">After you complete track 1, you will be live on release 10.0.11 (Commerce version 9.21), unless you encounter one of the [error situations](#error-situations) that were described for phase 1.</span></span>

#### <a name="track-1-update-your-csu-runtime-environments"></a><a id="update-csu"></a><span data-ttu-id="ee806-326">トラック 1: CSU ランタイム環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-326">Track 1: Update your CSU runtime environments</span></span>

<span data-ttu-id="ee806-327">トラック 1 を完成すると、実稼働環境はバージョン 10.0.11 で有効になるため、基本的に CSU のバージョン 10.0.11 への更新が完了します。</span><span class="sxs-lookup"><span data-stu-id="ee806-327">By completing track 1, you essentially complete your CSU update to version 10.0.11, because your production environment will be live on version 10.0.11.</span></span> <span data-ttu-id="ee806-328">このトラックの一部としてカスタム コードを再コンパイルする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ee806-328">You don't have to recompile your custom code as part of this track.</span></span>

##### <a name="update-test-1"></a><a id="update-test-1-csu"></a><span data-ttu-id="ee806-329">テスト 1 を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-329">Update Test 1</span></span>

<span data-ttu-id="ee806-330">現在、Commerce のサービス (SaaS) コンポーネントとしてのソフトウェアは、第 1 層環境 (開発/テスト環境) ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ee806-330">The software as a service (SaaS) components of Commerce aren't currently supported in Tier-1 environments (development/test environments).</span></span> <span data-ttu-id="ee806-331">Retail Server のコピーは各第 1 層環境でローカルに実行され、Retail Server 用の Microsoft コードと小売りのカスタマイズの両方の配置は、アプリケーション バイナリ パッケージと配置可能な小売りパッケージがサービス (IaaS) インスタンスとしてインフラストラクチャに対して適用される前のシステム介して行われます。</span><span class="sxs-lookup"><span data-stu-id="ee806-331">A copy of Retail Server runs locally in each Tier-1 environment, and the deployment of both Microsoft code for Retail Server and retail customizations will be done through the previous system, where application binary packages and retail deployable packages are applied against the infrastructure as a service (IaaS) instance.</span></span>

###### <a name="update-uat"></a><a id="update-uat-csu"></a><span data-ttu-id="ee806-332">UAT を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-332">Update UAT</span></span>

<span data-ttu-id="ee806-333">UAT 環境では、リリース 10.0.7 に対応する CSU が、実稼働環境で実行されているのと同じバージョンの小売り拡張機能と共に実行されています。</span><span class="sxs-lookup"><span data-stu-id="ee806-333">The UAT environment is running CSU that corresponds to release 10.0.7, together with the same version of your retail extension that the production environment is running.</span></span>

1. <span data-ttu-id="ee806-334">Commerce Scale Unit を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-334">Update the Commerce Scale Unit.</span></span> <span data-ttu-id="ee806-335">対象バージョンとして、**9.21 (10.0.11)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee806-335">Select **9.21 (10.0.11)** as the target version.</span></span> <span data-ttu-id="ee806-336">詳細については、[フェーズ2: CSU をバージョン 10.0.11 に更新する](#phase-2) を参照してください</span><span class="sxs-lookup"><span data-stu-id="ee806-336">For more information, see [Phase 2: Update CSU to version 10.0.11](#phase-2)</span></span>
2. <span data-ttu-id="ee806-337">ユーザー受け入れテストを完了し、サイン オフします。</span><span class="sxs-lookup"><span data-stu-id="ee806-337">Complete user acceptance testing, and sign off.</span></span>
3. <span data-ttu-id="ee806-338">回帰が発生した場合は、[エラー状況](#error-situations) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-338">If regressions are encountered, see the [Error situations](#error-situations) section.</span></span>

###### <a name="update-prod"></a><a id="update-prod-csu"></a><span data-ttu-id="ee806-339">製品を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-339">Update Prod</span></span>

1. <span data-ttu-id="ee806-340">Commerce Scale Unit を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-340">Update the Commerce Scale Unit.</span></span> <span data-ttu-id="ee806-341">対象バージョンとして、**9.21 (10.0.11)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee806-341">Select **9.21 (10.0.11)** as the target version.</span></span> <span data-ttu-id="ee806-342">詳細については、[フェーズ2: CSU をバージョン 10.0.11 に更新する](#phase-2) を参照してください</span><span class="sxs-lookup"><span data-stu-id="ee806-342">For more information, see [Phase 2: Update CSU to version 10.0.11](#phase-2)</span></span>
2. <span data-ttu-id="ee806-343">サイン オフします。</span><span class="sxs-lookup"><span data-stu-id="ee806-343">Sign off.</span></span>

#### <a name="track-2-update-your-development-environments"></a><a id="update-csu-dev"></a><span data-ttu-id="ee806-344">トラック 2: 開発環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-344">Track 2: Update your development environments</span></span>

1. <span data-ttu-id="ee806-345">Retail ソフトウェア開発キット (SDK) の最新バージョンを入手してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-345">Get the latest version of the Retail software development kit (SDK).</span></span>

    1. <span data-ttu-id="ee806-346">リリース 10.0.11 の Finance and Operations サービス更新プログラムを開発 1 に適用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-346">Apply the Finance and Operations service update for release 10.0.11 to Dev 1.</span></span>
    2. <span data-ttu-id="ee806-347">**%ServiceDrive%\\RetailSDK\\Update\\\<newest directory\>** から Retail SDK の更新されたバージョンを入手します</span><span class="sxs-lookup"><span data-stu-id="ee806-347">Get the updated version of the Retail SDK from **%ServiceDrive%\\RetailSDK\\Update\\\<newest directory\>**</span></span>

2. <span data-ttu-id="ee806-348">**メイン** (開発) 分岐で、新しいバージョンの Retail SDK から Retail アーティファクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-348">In your **main** (development) branch, update the Retail artifacts from the new version of the Retail SDK.</span></span>
3. <span data-ttu-id="ee806-349">コンパイルします。</span><span class="sxs-lookup"><span data-stu-id="ee806-349">Compile.</span></span> <span data-ttu-id="ee806-350">新しいバージョンは、下位互換性があり、コードを変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ee806-350">The new version should be backward-compatible and should not require any changes to your code.</span></span>
4. <span data-ttu-id="ee806-351">Retail SDK の更新を含む変更をコミットします。</span><span class="sxs-lookup"><span data-stu-id="ee806-351">Commit the change that includes the Retail SDK update.</span></span>
5. <span data-ttu-id="ee806-352">カスタム コードに必要な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="ee806-352">Make any required changes to your custom code.</span></span>
6. <span data-ttu-id="ee806-353">ターゲット分岐にコードの変更をコミットします。</span><span class="sxs-lookup"><span data-stu-id="ee806-353">Commit code changes to the target branch.</span></span>
7. <span data-ttu-id="ee806-354">オプション: 複数の開発環境がある場合は、手順 4 の最新の変更をマージし、最新のカスタムコードをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="ee806-354">Optional: If you have more than one development environment, merge the latest changes from step 4, and compile the latest custom code.</span></span>

### <a name="phase-3-update-pos-to-version-10011"></a><a id="phase-3"></a><span data-ttu-id="ee806-355">フェーズ3: POS をバージョン 10.0.11 に更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-355">Phase 3: Update POS to version 10.0.11</span></span>

<span data-ttu-id="ee806-356">このセクションでは、Modern POS や Hardware Station などの店舗のコンポーネントを最新のサービス更新プログラムに更新するために使用するプロセスを要約します。</span><span class="sxs-lookup"><span data-stu-id="ee806-356">This section summarizes the process that you use to update your store components, such as Modern POS and Hardware Station, to the latest service update.</span></span> <span data-ttu-id="ee806-357">リリース 10.0.7 (Commerce バージョン 9.17) からリリース 10.0.11 (Commerce バージョン 9.21) への更新が例として使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee806-357">An update from release 10.0.7 (Commerce version 9.17) to release 10.0.11 (Commerce version 9.21) is used as an example.</span></span>

<span data-ttu-id="ee806-358">Commerce 本社 (Finance and Operations アプリ内) および CSU の更新とは異なり、店舗のコンポーネントの更新は同じパッケージで提供されます。</span><span class="sxs-lookup"><span data-stu-id="ee806-358">Unlike updates for Commerce headquarters (in the Finance and Operations app) and CSU, updates for store components are delivered in the same packages.</span></span> <span data-ttu-id="ee806-359">Commerce 本社 と CSU を更新すると、次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="ee806-359">After you update Commerce headquarters and CSU, you have the following options:</span></span>

- <span data-ttu-id="ee806-360">**オプション0 (操作は必要ありません)** – バージョンがサポートされており、ポリシーに準拠している場合は、店舗のコンポーネントを以前のリリースままにします。</span><span class="sxs-lookup"><span data-stu-id="ee806-360">**Option 0 (no operation is required)** – Leave the store components in their previous release if the version is supported and in-policy.</span></span>
- <span data-ttu-id="ee806-361">**オプション 1** – CSU と同じリリースに一致するように、店舗のコンポーネント ランタイム (Microsoft コード) を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-361">**Option 1** – Update the store components runtime (Microsoft code) so that it matches the same release as CSU.</span></span>
- <span data-ttu-id="ee806-362">**オプション 2** – 店舗コンポーネントのランタイム (Microsoftコード) とカスタマイズを一緒に更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-362">**Option 2** – Update the store components runtime (Microsoft code) and customization together.</span></span>

<span data-ttu-id="ee806-363">このセクションの残りの部分では、店舗のコンポーネント (オプション 1 またはオプション 2) を更新するか、または更新する必要があることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="ee806-363">In the rest of this section, the assumption is that you want or have to update the store components (option 1 or option 2).</span></span>

<span data-ttu-id="ee806-364">このフェーズを完了すると、フェーズ 1 で説明されている [エラーの状況](#error-situations) のいずれかが発生しない限り、店舗のコンポーネントのリリース 10.0.11 (Commerce バージョン 9.21) で有効になります。</span><span class="sxs-lookup"><span data-stu-id="ee806-364">After you complete this phase, you will be live on release 10.0.11 (Commerce version 9.21) for store components, unless you encounter one of the [error situations](#error-situations) that are described for phase 1.</span></span>

#### <a name="phase-3-prerequisites"></a><a id="phase3-prerequisites"></a><span data-ttu-id="ee806-365">フェーズ 3 の前提条件</span><span class="sxs-lookup"><span data-stu-id="ee806-365">Phase 3 prerequisites</span></span>

<span data-ttu-id="ee806-366">フェーズ 3 には次の前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="ee806-366">Phase 3 has the following prerequisites:</span></span>

- <span data-ttu-id="ee806-367">Commerce 本社のコンポーネント (Finance and Operations アプリ内) は、CSU が更新される前に、同じリリースまたはそれ以降のリリースに更新されました。</span><span class="sxs-lookup"><span data-stu-id="ee806-367">The Commerce headquarters components (in the Finance and Operations app) were updated to the same release or a later release before the CSUs were updated.</span></span> <span data-ttu-id="ee806-368">この例では、バージョンは 10.0.11 です。</span><span class="sxs-lookup"><span data-stu-id="ee806-368">In this example, the version is 10.0.11.</span></span>
- <span data-ttu-id="ee806-369">CSU は、店舗のコンポーネントと同じリリースまたはそれ以降のリリースに更新されました。</span><span class="sxs-lookup"><span data-stu-id="ee806-369">The CSUs were updated to the same release as, or a later release than, the store components.</span></span> <span data-ttu-id="ee806-370">この例では、リリースは 10.0.11 です。</span><span class="sxs-lookup"><span data-stu-id="ee806-370">In this example, the release is 10.0.11.</span></span>

#### <a name="update-your-commerce-development-environment"></a><span data-ttu-id="ee806-371">Commerce 開発環境を更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-371">Update your Commerce development environment</span></span>

<span data-ttu-id="ee806-372">[トラック 2: 開発環境の更新](#update-csu-dev) セクションの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="ee806-372">Follow the steps in the [Track 2: Update your development environments](#update-csu-dev) section.</span></span>

#### <a name="option-1-store-component-updates-that-include-only-runtime-changes"></a><a id="store-runtime-only"></a><span data-ttu-id="ee806-373">オプション 1: ランタイムの変更のみを含む店舗のコンポーネントを更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-373">Option 1: Store component updates that include only runtime changes</span></span>

<span data-ttu-id="ee806-374">このオプションは、店舗のコンポーネントを含む新しい配置可能小売パッケージを生成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-374">This option generates a new retail deployable package that contains your store components.</span></span> <span data-ttu-id="ee806-375">Microsoft コードからの変更のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee806-375">It includes changes only from the Microsoft code.</span></span>

1. <span data-ttu-id="ee806-376">現在、実稼働環境で使用されているコードを含むリリース分岐を、対象リリースと一致する Retail SDK に更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-376">Update your release branch, which has the code that is currently being used in the production environment, to the Retail SDK that matches your target release.</span></span> <span data-ttu-id="ee806-377">この例では、バージョンは 10.0.11 (9.21) です。</span><span class="sxs-lookup"><span data-stu-id="ee806-377">In this example, the version is 10.0.11 (9.21).</span></span> <span data-ttu-id="ee806-378">[トラック 2: 開発環境の更新](#update-csu-dev) セクションの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="ee806-378">Follow the steps in the [Track 2: Update your development environments](#update-csu-dev) section.</span></span>
2. <span data-ttu-id="ee806-379">配置可能小売パッケージの新しいビルドを生成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-379">Generate a new build for the retail deployable package.</span></span> <span data-ttu-id="ee806-380">このビルドには、本稼働環境に現在あるものと同じカスタマイズのセットに加えて、Microsoft コードのバージョン 10.0.11 (9.21) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee806-380">This build contains the same set of customizations that is currently in the production environment, plus version 10.0.11 (9.21) of the Microsoft code.</span></span>

#### <a name="option-2-store-component-updates-that-include-runtime-and-custom-changes"></a><a id="store-runtime-custom"></a><span data-ttu-id="ee806-381">オプション 2: ランタイムとカスタムの変更を含む店舗のコンポーネントを更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-381">Option 2: Store component updates that include runtime and custom changes</span></span>

<span data-ttu-id="ee806-382">このオプションは、店舗のコンポーネントを含む新しい配置可能小売パッケージを生成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-382">This option generates a new retail deployable package that contains your store components.</span></span> <span data-ttu-id="ee806-383">Microsoft コードとカスタマイズ両方からの変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee806-383">It includes changes from both the Microsoft code and customizations.</span></span>

1. <span data-ttu-id="ee806-384">現在、実稼働環境で使用されているコードを含むリリース分岐を、対象リリースと一致する Retail SDK に更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-384">Update your release branch, which has the code that is currently being used in the production environment, to the Retail SDK that matches your target release.</span></span> <span data-ttu-id="ee806-385">この例では、バージョンは 10.0.11 (9.21) です。</span><span class="sxs-lookup"><span data-stu-id="ee806-385">In this example, the version is 10.0.11 (9.21).</span></span> <span data-ttu-id="ee806-386">[トラック 2: 開発環境の更新](#update-csu-dev) セクションの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="ee806-386">Follow the steps in the [Track 2: Update your development environments](#update-csu-dev) section.</span></span>
2. <span data-ttu-id="ee806-387">変更をコミットします。</span><span class="sxs-lookup"><span data-stu-id="ee806-387">Commit changes.</span></span>
3. <span data-ttu-id="ee806-388">店舗のコンポーネントのカスタム コードを更新するか、ISV 更新されたコンポーネントへの参照を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-388">Update custom code for store components, or update references to ISV-updated components.</span></span>
4. <span data-ttu-id="ee806-389">配置可能小売パッケージの新しいビルドを生成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-389">Generate a new build for the retail deployable package.</span></span> <span data-ttu-id="ee806-390">このビルドには、更新されたカスタム コードに加えて、Microsoft コードのバージョン 10.0.11 (9.21) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee806-390">This build contains updated custom code plus version 10.0.11 (9.21) of the Microsoft code.</span></span>

#### <a name="update-process"></a><span data-ttu-id="ee806-391">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="ee806-391">Update process</span></span>

##### <a name="update-test-1"></a><span data-ttu-id="ee806-392">テスト 1 の更新</span><span class="sxs-lookup"><span data-stu-id="ee806-392">Update Test 1</span></span>

<span data-ttu-id="ee806-393">Commerce の SaaS コンポーネントは現在、開発またはテストのワンボックス環境ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ee806-393">The SaaS components of Commerce aren't currently supported in development or test one-box environments.</span></span> <span data-ttu-id="ee806-394">Retail Server のコピーは、各開発またはテストのワンボックス環境でローカルに実行され、Retail Server 用の Microsoft コードと小売りのカスタマイズの両方の配置は、アプリケーション バイナリ パッケージと配置可能な小売りパッケージが IaaS インスタンスに対して適用される前のシステム介して行われます。</span><span class="sxs-lookup"><span data-stu-id="ee806-394">A copy of Retail Server runs locally in each development or test one-box environment, and the deployment of both Microsoft code for Retail Server and retail customizations will be done through the previous system, where application binary packages and retail deployable packages are applied against the IaaS instance.</span></span>

<span data-ttu-id="ee806-395">テスト 1 環境では、Commerce 本社のバージョン 10.0.11 と前のフェーズの CSU のローカル バージョンが実行されています。</span><span class="sxs-lookup"><span data-stu-id="ee806-395">The Test 1 environment is running version 10.0.11 of Commerce headquarters and a local version of CSU from previous phases.</span></span> <span data-ttu-id="ee806-396">このフローでは、テスト 1 の更新は前提条件ではありません。</span><span class="sxs-lookup"><span data-stu-id="ee806-396">An update of Test 1 isn't a prerequisite in this flow.</span></span> <span data-ttu-id="ee806-397">この環境には CSU がないため、この手順は主に検証用です。</span><span class="sxs-lookup"><span data-stu-id="ee806-397">Because there is no CSU in this environment, this step is mostly for verification.</span></span>

1. <span data-ttu-id="ee806-398">店舗のコンポーネントをアップロード、更新、および配置します。</span><span class="sxs-lookup"><span data-stu-id="ee806-398">Upload, update, and deploy the store components.</span></span> <span data-ttu-id="ee806-399">詳細については、[店舗のコンポーネントのアップロード、更新、および配置](#upload-store-components) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-399">For more information, see the [Upload, update, and deploy store components](#upload-store-components) section.</span></span>
2. <span data-ttu-id="ee806-400">機能シナリオを承認します。</span><span class="sxs-lookup"><span data-stu-id="ee806-400">Sign off on functional scenarios.</span></span>
3. <span data-ttu-id="ee806-401">回帰が発生した場合は、[エラー状況](#error-situations) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-401">If regressions are encountered, see the [Error situations](#error-situations) section.</span></span>

##### <a name="update-uat"></a><span data-ttu-id="ee806-402">UAT の更新</span><span class="sxs-lookup"><span data-stu-id="ee806-402">Update UAT</span></span>

<span data-ttu-id="ee806-403">UAT 環境を指すクライアントは、リリース 10.0.7 (実稼働環境で現在実行されているのと同じバージョン) のアプリケーション (たとえば、Modern POS) を実行しています。</span><span class="sxs-lookup"><span data-stu-id="ee806-403">Clients that point to the UAT environment are running applications (for example, Modern POS) for release 10.0.7 (the same version that is currently running in the production environment).</span></span>

1. <span data-ttu-id="ee806-404">店舗のコンポーネントをアップロード、更新、および配置します。</span><span class="sxs-lookup"><span data-stu-id="ee806-404">Upload, update, and deploy the store components.</span></span> <span data-ttu-id="ee806-405">詳細については、[店舗のコンポーネントのアップロード、更新、および配置](#upload-store-components) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-405">For more information, see the [Upload, update, and deploy store components](#upload-store-components) section.</span></span>
2. <span data-ttu-id="ee806-406">機能シナリオを承認します。</span><span class="sxs-lookup"><span data-stu-id="ee806-406">Sign off on functional scenarios.</span></span>
3. <span data-ttu-id="ee806-407">回帰が発生した場合は、[エラー状況](#error-situations) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee806-407">If regressions are encountered, see the [Error situations](#error-situations) section.</span></span>

##### <a name="update-prod"></a><span data-ttu-id="ee806-408">製品の更新</span><span class="sxs-lookup"><span data-stu-id="ee806-408">Update Prod</span></span>

1. <span data-ttu-id="ee806-409">店舗のコンポーネントをアップロード、更新、および配置します。</span><span class="sxs-lookup"><span data-stu-id="ee806-409">Upload, update, and deploy the store components.</span></span>
2. <span data-ttu-id="ee806-410">サイン オフします。</span><span class="sxs-lookup"><span data-stu-id="ee806-410">Sign off.</span></span>

## <a name="apply-a-new-version-of-your-custom-code"></a><span data-ttu-id="ee806-411">カスタム コードの新しいバージョンを適用する<a id="apply-new-custom-code"></a></span><span class="sxs-lookup"><span data-stu-id="ee806-411"><a id="apply-new-custom-code"></a>Apply a new version of your custom code</span></span>

<span data-ttu-id="ee806-412">このセクションでは、カスタム拡張機能の新しいビルドで UAT または製品環境を更新する必要がある 2 つのユース ケースの推奨されるフローについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ee806-412">This section describes the recommended flow for two use cases that require that you update your UAT and/or Prod environment with a new build of your custom extension.</span></span>

### <a name="create-a-hotfix-of-your-code"></a><span data-ttu-id="ee806-413">コードの修正プログラムを作成する<a id="create-hotfix"></a></span><span class="sxs-lookup"><span data-stu-id="ee806-413"><a id="create-hotfix"></a>Create a hotfix of your code</span></span>

<span data-ttu-id="ee806-414">UAT または製品環境で重大なバグが見つかった場合は、リリース分岐 (**メイン** 分岐または開発分岐にはない) のバグを修正し、標準プロセスを使用して配置可能なパッケージを UAT と製品に適用します。</span><span class="sxs-lookup"><span data-stu-id="ee806-414">When a critical bug is found in the UAT or Prod environment, fix the bug in the release branch (not in the **main** or development branch), and use the standard process to apply a deployable package to UAT and Prod.</span></span>

:::image type="content" source="media/uguide-hotfix.png" alt-text="修正プログラムのプロセス":::

1. <span data-ttu-id="ee806-416">開発 1 では、リリース分岐でコードの修正を行います。</span><span class="sxs-lookup"><span data-stu-id="ee806-416">In Dev 1, make the code fix in the release branch.</span></span> <span data-ttu-id="ee806-417">必要な修正が ISV コードにある場合は、ソリューションの次のバージョンではなく、現在のリリースの新しいビルドを ISV に送信するよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="ee806-417">If the required fix is in ISV code, ask the ISV to send you a new build of the current release, not the next version of the solution.</span></span>
2. <span data-ttu-id="ee806-418">コンパイルしてテストします。</span><span class="sxs-lookup"><span data-stu-id="ee806-418">Compile and test.</span></span>
3. <span data-ttu-id="ee806-419">リリース分岐から新しい配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-419">Create a new deployable package out of the release branch.</span></span>
4. <span data-ttu-id="ee806-420">テスト 1 に配置し、サインオフが必要な場合はサインオフします。</span><span class="sxs-lookup"><span data-stu-id="ee806-420">Deploy on Test 1, and sign off if sign-off is required.</span></span>
5. <span data-ttu-id="ee806-421">標準プロセスを使用して、カスタム コードを最初に UAT に配置し、次に製品に配置します。</span><span class="sxs-lookup"><span data-stu-id="ee806-421">Use the standard process to deploy custom code first to UAT and then to Prod.</span></span>
6. <span data-ttu-id="ee806-422">コード修正を **メイン** コード分岐と統合します。</span><span class="sxs-lookup"><span data-stu-id="ee806-422">Integrate the code fix with your **main** code branch.</span></span>

### <a name="update-your-custom-code-from-release-n-to-release-n1"></a><a id="update-custom-code"></a><span data-ttu-id="ee806-423">カスタム コードをリリース N からリリース N+1 に更新する</span><span class="sxs-lookup"><span data-stu-id="ee806-423">Update your custom code from release N to release N+1</span></span>

<span data-ttu-id="ee806-424">カスタム コードの次のバージョンをリリースする準備ができたら、次のプロセスを使用して新しいリリースを作成および配置します。</span><span class="sxs-lookup"><span data-stu-id="ee806-424">When you're ready to release the next version of your custom code, use the following process to create and deploy the new release.</span></span>

:::image type="content" source="media/uguide-custom-code.png" alt-text="カスタム コードを N から N+1 に更新する":::

1. <span data-ttu-id="ee806-426">開発 2 環境、または **メイン** 分岐に接続されている別の環境では、**メイン** 分岐で開発を完了します。</span><span class="sxs-lookup"><span data-stu-id="ee806-426">In the Dev 2 environment, or another environment that is connected to the **main** branch, complete development in the **main** branch.</span></span>
2. <span data-ttu-id="ee806-427">テスト 2 に配置してテストします。</span><span class="sxs-lookup"><span data-stu-id="ee806-427">Deploy and test on Test 2.</span></span>
3. <span data-ttu-id="ee806-428">新しいバージョンが承認されるまで手順 1 ～ 2 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="ee806-428">Repeat steps 1 through 2 until the new version is signed-off on.</span></span>
4. <span data-ttu-id="ee806-429">**新しい** リリース分岐を作成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-429">Create a **new** release branch.</span></span>
5. <span data-ttu-id="ee806-430">**新しい** リリース分岐から新しい配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee806-430">Create a new deployable package out of the **new** release branch.</span></span>
6. <span data-ttu-id="ee806-431">標準プロセスを使用して、カスタム コードを最初に UAT に配置し、次に製品に配置します。</span><span class="sxs-lookup"><span data-stu-id="ee806-431">Use the standard process to deploy custom code first to UAT and then to Prod.</span></span>
7. <span data-ttu-id="ee806-432">古いリリース分岐を破棄します。</span><span class="sxs-lookup"><span data-stu-id="ee806-432">Retire the old release branch.</span></span>

## <a name="upload-update-and-deploy-store-components"></a><a id="upload-store-components"></a><span data-ttu-id="ee806-433">店舗のコンポーネントをアップロード、更新、および配置する</span><span class="sxs-lookup"><span data-stu-id="ee806-433">Upload, update, and deploy store components</span></span>

1. <span data-ttu-id="ee806-434">配置可能小売パッケージを LCS にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="ee806-434">Upload the retail deployable package to LCS.</span></span>
2. <span data-ttu-id="ee806-435">Application Object Server (AOS) を最新のクライアントで更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-435">Update Application Object Server (AOS) with the latest client.</span></span>
3. <span data-ttu-id="ee806-436">配置可能小売パッケージを資産ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="ee806-436">Upload the retail deployable package to your Asset library:</span></span>

    + <span data-ttu-id="ee806-437">**以前の配置 (バージョン 10.0.11 より前):** ソフトウェア配置可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="ee806-437">**Older deployments (earlier than version 10.0.11):** Software deployable package</span></span>
    + <span data-ttu-id="ee806-438">**新しい配置 (バージョン10.0.11 以降):** Retail セルフサービスのインストーラー</span><span class="sxs-lookup"><span data-stu-id="ee806-438">**New deployments (version 10.0.11 and later):** Retail self-service installers</span></span>

4. <span data-ttu-id="ee806-439">店舗のコンポーネント用の新しいセルフサービス インストーラーで Commerce 本社を更新します。</span><span class="sxs-lookup"><span data-stu-id="ee806-439">Update Commerce headquarters with the new self-service installers for store components:</span></span>

    + <span data-ttu-id="ee806-440">**以前の配置 (バージョン 10.0.11 より前):** LCS を介して配置可能小売パッケージを Commerce 本社に配置します。</span><span class="sxs-lookup"><span data-stu-id="ee806-440">**Older deployments (earlier than version 10.0.11):** Deploy the retail deployable package to Commerce headquarters via LCS.</span></span>
    + <span data-ttu-id="ee806-441">**新しい配置 (バージョン10.0.11 以降):** Commerce 本社の **Commerce パラメーター** フォームの **チャネル配置** タブで **パッケージの更新の確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee806-441">**New deployments (version 10.0.11 and later):** In Commerce headquarters, on the **Commerce parameters** form, on the **Channel deployment** tab, select **Check for package updates**.</span></span> <span data-ttu-id="ee806-442">この更新では、LCS 資産ライブラリの **Retail セルフサービス パッケージ** タブで使用できるパッケージが導入されます。</span><span class="sxs-lookup"><span data-stu-id="ee806-442">This update will bring in the packages that are available on the **Retail Self-service package** tab in the LCS Asset library.</span></span>

5. <span data-ttu-id="ee806-443">クライアント バージョンをデバイスに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ee806-443">Assign the client versions to your devices.</span></span>
6. <span data-ttu-id="ee806-444">目的のクライアント タイプとデバイスのインストーラーをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="ee806-444">Download the installers for the desired client type and device.</span></span>
7. <span data-ttu-id="ee806-445">対象のデバイスにインストールします。</span><span class="sxs-lookup"><span data-stu-id="ee806-445">Install in target device.</span></span>
8. <span data-ttu-id="ee806-446">テストして検証します。</span><span class="sxs-lookup"><span data-stu-id="ee806-446">Test and validate.</span></span>
