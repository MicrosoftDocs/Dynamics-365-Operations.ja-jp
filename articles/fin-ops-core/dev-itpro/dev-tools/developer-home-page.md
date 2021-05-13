---
title: ホームページの開発とカスタマイズ
description: このトピックでは、開発に関するトピックへのリンクを提供します。
author: RobinARH
ms.date: 04/27/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4657ae53908e8588bf78168adefb28ed4ae137ba
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881386"
---
# <a name="develop-and-customize-home-page"></a><span data-ttu-id="cd8c3-103">ホームページの開発とカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-103">Develop and customize home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd8c3-104">このトピックでは、開発に関するトピックへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-104">This topic provides links to topics about development.</span></span>

## <a name="overview"></a><span data-ttu-id="cd8c3-105">概要</span><span class="sxs-lookup"><span data-stu-id="cd8c3-105">Overview</span></span>

<span data-ttu-id="cd8c3-106">Finance and Operations アプリケーションは、Microsoft が提供する次世代エンタープライズ リソース プランニング (ERP) を表します。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-106">The Finance and Operations applications represent the next-generation enterprise resource planning (ERP) offering from Microsoft.</span></span> <span data-ttu-id="cd8c3-107">このアプリでは、パブリック クラウドとプライベート クラウド両方のクラウド ベースのソリューションおよびオンプレミスとして、全体の ERP アプリケーション スイートを有効できます。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-107">The apps enable the entire ERP application suite as a cloud-based solution, for both public and private clouds, as well as on-premises.</span></span> <span data-ttu-id="cd8c3-108">このアプリは、Microsoft からの最新テクノロジーで構築時に、クラウドでの操作の速度、わかりやすさ、およびコスト効率性を利用します。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-108">The apps leverage the speed, simplicity, and cost-effectiveness of working in the cloud, while building on the latest technology from Microsoft.</span></span> <span data-ttu-id="cd8c3-109">開発経験には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-109">The development experience includes:</span></span>

- <span data-ttu-id="cd8c3-110">実行環境から切り離された開発ツール。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-110">Development tools that are decoupled from any running environment.</span></span> <span data-ttu-id="cd8c3-111">オンライン データベースではなく、ローカルの XML ベースのファイルに対して作成します。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-111">You develop against local, XML-based files, not the online database.</span></span>
- <span data-ttu-id="cd8c3-112">Microsoft Visual Studio が開発環境です。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-112">Microsoft Visual Studio is the development environment.</span></span> <span data-ttu-id="cd8c3-113">Visual Studio 環境は、円滑で慣れ親しんだエクスペリエンスを提供するようにカスタマイズされています。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-113">The Visual Studio environment is customized to provide you with a smooth and familiar experience.</span></span>
- <span data-ttu-id="cd8c3-114">X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-114">The X++ compiler generates Common Intermediate Language (CIL) for all features.</span></span> <span data-ttu-id="cd8c3-115">CIL は C\# プログラミング言語などの他の .NET ベース (マネージド) の言語で使用されるものと同じ中間言語です。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-115">CIL is the same intermediate language used by other .NET-based (managed) languages, such as the C\# programming language.</span></span>
- <span data-ttu-id="cd8c3-116">ブラウザー ベースのクライアントおよびフォームのデザイン パターンを活用して、改善されたエンド ユーザー エクスペリエンスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-116">You can leverage the browser-based client and the design patterns for forms to provide an improved end-user experience.</span></span>
- <span data-ttu-id="cd8c3-117">Application Lifecycle Model (ALM) は、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-117">The Application Lifecycle Model (ALM) supports build automation, test automation, and deployment of models to the cloud.</span></span>

## <a name="architecture"></a><span data-ttu-id="cd8c3-118">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-118">Architecture</span></span>

- [<span data-ttu-id="cd8c3-119">アプリケーション スタックおよびサーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-119">Application stack and server architecture</span></span>](application-stack-server-architecture.md)

## <a name="getting-started"></a><span data-ttu-id="cd8c3-120">はじめに</span><span class="sxs-lookup"><span data-stu-id="cd8c3-120">Getting started</span></span>

- [<span data-ttu-id="cd8c3-121">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="cd8c3-121">Get evaluation copies</span></span>](get-evaluation-copy.md)
- [<span data-ttu-id="cd8c3-122">プレビュー サブスクリプションのサインアップ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-122">Sign up for preview subscriptions</span></span>](sign-up-preview-subscription.md)
- [<span data-ttu-id="cd8c3-123">開発環境の配置とアクセス</span><span class="sxs-lookup"><span data-stu-id="cd8c3-123">Deploy and access development environments</span></span>](../dev-tools/access-instances.md)
- [<span data-ttu-id="cd8c3-124">開発システム要件</span><span class="sxs-lookup"><span data-stu-id="cd8c3-124">Development system requirements</span></span>](development-system-requirements.md)
- [<span data-ttu-id="cd8c3-125">削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="cd8c3-125">Removed or deprecated features</span></span>](../migration-upgrade/deprecated-features.md)
- [<span data-ttu-id="cd8c3-126">非推奨 API</span><span class="sxs-lookup"><span data-stu-id="cd8c3-126">Deprecated APIs</span></span>](../migration-upgrade/deprecated-apis.md)
- [<span data-ttu-id="cd8c3-127">ローカル開発 (VHD) 環境の名前変更</span><span class="sxs-lookup"><span data-stu-id="cd8c3-127">Rename a local development (VHD) environment</span></span>](../migration-upgrade/vso-machine-renaming.md)
- [<span data-ttu-id="cd8c3-128">Azure DevOps の概要 (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="cd8c3-128">Introduction to Azure DevOps (Video)</span></span>](https://channel9.msdn.com/Events/Build/2014/2-575)

## <a name="fleet-management"></a><span data-ttu-id="cd8c3-129">フリート管理</span><span class="sxs-lookup"><span data-stu-id="cd8c3-129">Fleet Management</span></span>

- [<span data-ttu-id="cd8c3-130">フリート管理のサンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="cd8c3-130">Fleet Management sample application</span></span>](introduction-fleet-management-sample.md)
- [<span data-ttu-id="cd8c3-131">フリート管理のサンプル アプリケーションのためのエンド ツー エンドのシナリオ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-131">End-to-end scenario for the Fleet Management sample application</span></span>](fleet-management-sample.md)

## <a name="development-tools"></a><span data-ttu-id="cd8c3-132">開発ツール</span><span class="sxs-lookup"><span data-stu-id="cd8c3-132">Development tools</span></span>

### <a name="tutorials-for-development-tools"></a><span data-ttu-id="cd8c3-133">開発ツールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="cd8c3-133">Tutorials for development tools</span></span>

- [<span data-ttu-id="cd8c3-134">開発ツールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="cd8c3-134">Development tools tutorial</span></span>](introduction-visual-studio.md)
- [<span data-ttu-id="cd8c3-135">モデルとデータ モデル要素の作成の概要</span><span class="sxs-lookup"><span data-stu-id="cd8c3-135">Create models and data model elements overview</span></span>](create-data-model-elements.md)
- [<span data-ttu-id="cd8c3-136">プロジェクトのビルドおよびデバッグ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-136">Build and debug projects</span></span>](build-debug-project.md)
- [<span data-ttu-id="cd8c3-137">バージョン コントロール、メタデータ検索、およびナビゲーション</span><span class="sxs-lookup"><span data-stu-id="cd8c3-137">Version control, metadata search, and navigation</span></span>](version-control-metadata-navigation.md)

### <a name="tools-models-and-vms"></a><span data-ttu-id="cd8c3-138">ツール、モデル、VM</span><span class="sxs-lookup"><span data-stu-id="cd8c3-138">Tools, models, and VMs</span></span>

- [<span data-ttu-id="cd8c3-139">Visual Studioの開発ツール</span><span class="sxs-lookup"><span data-stu-id="cd8c3-139">Development tools in Visual Studio</span></span>](development-tools-overview.md)
- [<span data-ttu-id="cd8c3-140">アプリケーション エクスプローラー</span><span class="sxs-lookup"><span data-stu-id="cd8c3-140">Application Explorer</span></span>](application-explorer.md)
- [<span data-ttu-id="cd8c3-141">Visual Studio における Finance and Operations のプロジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-141">Finance and Operations project type in Visual Studio</span></span>](projects.md)
- [<span data-ttu-id="cd8c3-142">要素デザイナー</span><span class="sxs-lookup"><span data-stu-id="cd8c3-142">Element designers</span></span>](element-designers.md)
- [<span data-ttu-id="cd8c3-143">要素の使用方法を決定するためのコマンド</span><span class="sxs-lookup"><span data-stu-id="cd8c3-143">Commands for determining how elements are used</span></span>](element-usage.md)
- [<span data-ttu-id="cd8c3-144">モデルとパッケージ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-144">Models and packages</span></span>](models.md)
- [<span data-ttu-id="cd8c3-145">ビルド操作</span><span class="sxs-lookup"><span data-stu-id="cd8c3-145">Build operations</span></span>](build-operations.md)
- [<span data-ttu-id="cd8c3-146">コード エディター機能</span><span class="sxs-lookup"><span data-stu-id="cd8c3-146">Code editor features</span></span>](code-editor.md)
- [<span data-ttu-id="cd8c3-147">Visual Studioのツールアドイン</span><span class="sxs-lookup"><span data-stu-id="cd8c3-147">Tools add-ins for Visual Studio</span></span>](developer-tools-add-ins.md)
- [<span data-ttu-id="cd8c3-148">モデルのエクスポートとインポート</span><span class="sxs-lookup"><span data-stu-id="cd8c3-148">Export and import models</span></span>](models-export-import.md)
- [<span data-ttu-id="cd8c3-149">Visual Studio でのメタデータの検索</span><span class="sxs-lookup"><span data-stu-id="cd8c3-149">Metadata search in Visual Studio</span></span>](metadata-search-visual-studio.md)
- [<span data-ttu-id="cd8c3-150">開発マシンでの新しいユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="cd8c3-150">Create new users on development machines</span></span>](enable-development-machine.md)
- [<span data-ttu-id="cd8c3-151"> Visual Studio の開発ツールを更新する</span><span class="sxs-lookup"><span data-stu-id="cd8c3-151">Update the Visual Studio development tools</span></span>](update-development-tools.md)
- [<span data-ttu-id="cd8c3-152">管理者アクセスを許可しない開発用 VM および ビルド用 VM に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="cd8c3-152">Development and build VMs that don't allow admin access FAQ</span></span>](../sysadmin/VMs-no-admin-access.md)

## <a name="build-automation-using-azure"></a><span data-ttu-id="cd8c3-153">Azure を使用したビルドの自動化</span><span class="sxs-lookup"><span data-stu-id="cd8c3-153">Build automation using Azure</span></span>

- [<span data-ttu-id="cd8c3-154">Microsoft にホストされるエージェント、および Azure Pipelines を使用したビルドの自動化</span><span class="sxs-lookup"><span data-stu-id="cd8c3-154">Build automation using Microsoft-hosted agents and Azure Pipelines</span></span>](hosted-build-automation.md)
- [<span data-ttu-id="cd8c3-155">Azure Pipelines にある配置可能なパッケージへのライセンス ファイルの追加</span><span class="sxs-lookup"><span data-stu-id="cd8c3-155">Add license files to a deployable package in Azure Pipelines</span></span>](pipeline-add-license-package.md)
- [<span data-ttu-id="cd8c3-156">Azure Pipelines に配置可能なパッケージの作成</span><span class="sxs-lookup"><span data-stu-id="cd8c3-156">Create deployable packages in Azure Pipelines</span></span>](pipeline-create-deployable-package.md)
- [<span data-ttu-id="cd8c3-157">Azure Pipelines で、X++ モデルのバージョン管理</span><span class="sxs-lookup"><span data-stu-id="cd8c3-157">X++ model-versioning in Azure Pipelines</span></span>](pipeline-model-version.md)
- [<span data-ttu-id="cd8c3-158">Azure Pipelines を使用した資産のダウンロード</span><span class="sxs-lookup"><span data-stu-id="cd8c3-158">Download assets by using Azure Pipelines</span></span>](pipeline-asset-download.md)
- [<span data-ttu-id="cd8c3-159">Azure Pipelines を使用した資産のアップロード</span><span class="sxs-lookup"><span data-stu-id="cd8c3-159">Upload assets by using Azure Pipelines</span></span>](pipeline-asset-upload.md)
- [<span data-ttu-id="cd8c3-160">Azure Pipelines を使用した資産のデプロイ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-160">Deploy assets by using Azure Pipelines</span></span>](pipeline-deploy-asset.md)
- [<span data-ttu-id="cd8c3-161">Azure Pipelines での Lifecycle Services (LCS) 接続の作成</span><span class="sxs-lookup"><span data-stu-id="cd8c3-161">Create a Lifecycle Services (LCS) connection in Azure Pipelines</span></span>](pipeline-lcs-connection.md)
- [<span data-ttu-id="cd8c3-162">新しい NuGet パッケージ用にホストされる Azure Pipeline の更新</span><span class="sxs-lookup"><span data-stu-id="cd8c3-162">Update the hosted Azure Pipeline for new NuGet packages</span></span>](pipeline-nuget-split.md)
- [<span data-ttu-id="cd8c3-163">Azure Pipelines でのレガシ パイプラインの更新</span><span class="sxs-lookup"><span data-stu-id="cd8c3-163">Update a legacy pipeline in Azure Pipelines</span></span>](pipeline-msbuild-update.md)

## <a name="x-programming-language"></a><span data-ttu-id="cd8c3-164">X++ プログラミング言語</span><span class="sxs-lookup"><span data-stu-id="cd8c3-164">X++ programming language</span></span>

### <a name="overviews"></a><span data-ttu-id="cd8c3-165">概要</span><span class="sxs-lookup"><span data-stu-id="cd8c3-165">Overviews</span></span>

- [<span data-ttu-id="cd8c3-166">X++ およびデバッガーの機能</span><span class="sxs-lookup"><span data-stu-id="cd8c3-166">X++ and debugger features</span></span>](new-x-debugger-features.md)
- [<span data-ttu-id="cd8c3-167">C\# と X++ ソース コードを使用してビジネス ロジックを記述する</span><span class="sxs-lookup"><span data-stu-id="cd8c3-167">Write business logic by using C\# and X++ source code</span></span>](write-business-logic.md)
- [<span data-ttu-id="cd8c3-168">X++ の Visual Studio 2017 の要件</span><span class="sxs-lookup"><span data-stu-id="cd8c3-168">Visual Studio 2017 requirements for X++</span></span>](developer-tools-vs2017.md)

### <a name="language-support"></a><span data-ttu-id="cd8c3-169">言語サポート</span><span class="sxs-lookup"><span data-stu-id="cd8c3-169">Language support</span></span>

- [<span data-ttu-id="cd8c3-170">X++ と X++ コンパイラの変更</span><span class="sxs-lookup"><span data-stu-id="cd8c3-170">Changes in X++ and the X++ compiler</span></span>](programming-language-support.md)
- [<span data-ttu-id="cd8c3-171">要求または応答シナリオの EventHandlerResult クラス</span><span class="sxs-lookup"><span data-stu-id="cd8c3-171">EventHandlerResult classes in request or response scenarios</span></span>](event-handler-result-class.md)
- [<span data-ttu-id="cd8c3-172">Visual Studioのデバッガーを使用して  X++ コードをデバッグする</span><span class="sxs-lookup"><span data-stu-id="cd8c3-172">Debug X++ code by using the debugger in Visual Studio</span></span>](debug-xpp.md)
- [<span data-ttu-id="cd8c3-173">C\# の統合言語クエリ (LINQ) プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cd8c3-173">Language Integrated Query (LINQ) provider for C\#</span></span>](linq-provider-c.md)
- [<span data-ttu-id="cd8c3-174">ベスト プラクティス ルールの記述</span><span class="sxs-lookup"><span data-stu-id="cd8c3-174">Write best practice rules</span></span>](author-best-practice-rules.md)

### <a name="reference"></a><span data-ttu-id="cd8c3-175">参照</span><span class="sxs-lookup"><span data-stu-id="cd8c3-175">Reference</span></span>

- [<span data-ttu-id="cd8c3-176">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="cd8c3-176">X++ language reference</span></span>](../dev-ref/xpp-language-reference.md)

## <a name="customize-with-extensions-and-overlayering"></a><span data-ttu-id="cd8c3-177">拡張機能およびオーバーレイによってカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="cd8c3-177">Customize with extensions and overlayering</span></span>

- [<span data-ttu-id="cd8c3-178">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-178">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
- [<span data-ttu-id="cd8c3-179">拡張機能を使用してアプリケーション スイート レポートをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="cd8c3-179">Customize App Suite reports by using extensions</span></span>](../analytics/customize-app-suite-reports-with-extensions.md)

## <a name="code-migration"></a><span data-ttu-id="cd8c3-180">コードの移行</span><span class="sxs-lookup"><span data-stu-id="cd8c3-180">Code migration</span></span>

- [<span data-ttu-id="cd8c3-181">Visual Studio  での競合を解決する方法 (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="cd8c3-181">How to resolve conflicts in Visual Studio (video)</span></span>](https://youtu.be/4rxO0zUN2zU)
- [<span data-ttu-id="cd8c3-182">コードの移行とホーム ページのアップグレード</span><span class="sxs-lookup"><span data-stu-id="cd8c3-182">Code migration and upgrade home page</span></span>](../migration-upgrade/code-migration-home-page.md)

## <a name="move-packages-between-environments"></a><span data-ttu-id="cd8c3-183">環境間でパッケージを移動する</span><span class="sxs-lookup"><span data-stu-id="cd8c3-183">Move packages between environments</span></span>

- [<span data-ttu-id="cd8c3-184">配置可能なモデル パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="cd8c3-184">Create deployable packages of models</span></span>](../deployment/create-apply-deployable-package.md)

## <a name="performance"></a><span data-ttu-id="cd8c3-185">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="cd8c3-185">Performance</span></span>

- [<span data-ttu-id="cd8c3-186">Trace Parser を使用してトレースを実行</span><span class="sxs-lookup"><span data-stu-id="cd8c3-186">Take traces by using Trace parser</span></span>](../perf-test/trace-trace-tutorial.md)
- [<span data-ttu-id="cd8c3-187">Trace Parser を使用した問題点の診断およびパフォーマンスの分析</span><span class="sxs-lookup"><span data-stu-id="cd8c3-187">Diagnose issues and analyze performance by using Trace parser</span></span>](../perf-test/trace-parser.md)
- [<span data-ttu-id="cd8c3-188">パフォーマンス タイマー</span><span class="sxs-lookup"><span data-stu-id="cd8c3-188">Performance timer</span></span>](../perf-test/performance-timer.md)

## <a name="user-interface-concepts"></a><span data-ttu-id="cd8c3-189">ユーザー インターフェイスのコンセプト</span><span class="sxs-lookup"><span data-stu-id="cd8c3-189">User interface concepts</span></span>

<span data-ttu-id="cd8c3-190">クライアントは、すべての主要なブラウザーで動作する HTML Web クライアントです。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-190">The client is an HTML web client that runs in all major browsers.</span></span> <span data-ttu-id="cd8c3-191">ユーザー インターフェイスの開発およびカスタマイズの詳細ついては、[ユーザー インターフェイス開発ホーム ページ](../user-interface/user-interface-development-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd8c3-191">For information about developing and customizing the user interface, see the [User interface development home page](../user-interface/user-interface-development-home-page.md).</span></span>

## <a name="analytics"></a><span data-ttu-id="cd8c3-192">分析</span><span class="sxs-lookup"><span data-stu-id="cd8c3-192">Analytics</span></span>

- [<span data-ttu-id="cd8c3-193">分析、集計の測定、および KPI モデリング</span><span class="sxs-lookup"><span data-stu-id="cd8c3-193">Analytics, aggregate measurements, and KPI modeling</span></span>](../analytics/analytics.md)

## <a name="reporting-services"></a><span data-ttu-id="cd8c3-194">Reporting Services</span><span class="sxs-lookup"><span data-stu-id="cd8c3-194">Reporting services</span></span>

- [<span data-ttu-id="cd8c3-195">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="cd8c3-195">Electronic reporting (ER) overview</span></span>](../analytics/general-electronic-reporting.md)

## <a name="data-entities-and-odata"></a><span data-ttu-id="cd8c3-196">データ エンティティおよび OData</span><span class="sxs-lookup"><span data-stu-id="cd8c3-196">Data entities and OData</span></span>

- [<span data-ttu-id="cd8c3-197">データ エンティティの概要</span><span class="sxs-lookup"><span data-stu-id="cd8c3-197">Data entities overview</span></span>](../data-entities/data-entities.md)
- [<span data-ttu-id="cd8c3-198">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="cd8c3-198">Open Data Protocol (OData)</span></span>](../data-entities/odata.md)

## <a name="testing-support-in-visual-studio"></a><span data-ttu-id="cd8c3-199">Visual Studio でのテストのサポート</span><span class="sxs-lookup"><span data-stu-id="cd8c3-199">Testing support in Visual Studio</span></span>

- [<span data-ttu-id="cd8c3-200">テストと検証</span><span class="sxs-lookup"><span data-stu-id="cd8c3-200">Testing and validations</span></span>](../perf-test/testing-validation.md)
- [<span data-ttu-id="cd8c3-201">Visual Studio のプロジェクトをテストする</span><span class="sxs-lookup"><span data-stu-id="cd8c3-201">Test projects in Visual Studio</span></span>](../perf-test/testing-support.md)
- [<span data-ttu-id="cd8c3-202">継続的なビルドおよびテストの自動化環境の配置と使用</span><span class="sxs-lookup"><span data-stu-id="cd8c3-202">Deploy and use a continuous build and test automation environment</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="cd8c3-203">タスク レコーダー リソース</span><span class="sxs-lookup"><span data-stu-id="cd8c3-203">Task recorder resources</span></span>](../user-interface/task-recorder.md)

## <a name="office-integration"></a><span data-ttu-id="cd8c3-204">Office 統合</span><span class="sxs-lookup"><span data-stu-id="cd8c3-204">Office integration</span></span>

- [<span data-ttu-id="cd8c3-205">Office 統合の概要</span><span class="sxs-lookup"><span data-stu-id="cd8c3-205">Office integration overview</span></span>](../office-integration/office-integration.md)

## <a name="intelligence"></a><span data-ttu-id="cd8c3-206">インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="cd8c3-206">Intelligence</span></span>

- [<span data-ttu-id="cd8c3-207">ビジネス インテリジェンス (BI) およびレポート作成のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="cd8c3-207">Business intelligence (BI) and reporting home page</span></span>](../analytics/bi-reporting-home-page.md)

## <a name="mobile-platform"></a><span data-ttu-id="cd8c3-208">モバイル プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="cd8c3-208">Mobile platform</span></span>

- [<span data-ttu-id="cd8c3-209">モバイル プラットフォームのリソース</span><span class="sxs-lookup"><span data-stu-id="cd8c3-209">Mobile platform resources</span></span>](../mobile-apps/platform/mobile-platform-home-page.md)

## <a name="global-finance-management"></a><span data-ttu-id="cd8c3-210">グローバル財務管理</span><span class="sxs-lookup"><span data-stu-id="cd8c3-210">Global finance management</span></span>

- [<span data-ttu-id="cd8c3-211">Dynamics 365 Finance ホーム ページの開発</span><span class="sxs-lookup"><span data-stu-id="cd8c3-211">Development for Dynamics 365 Finance home page</span></span>](../financial/financial-dev-home-page.md)

## <a name="development-for-independent-software-vendors"></a><span data-ttu-id="cd8c3-212">独立系ソフトウェア ベンダーのための開発</span><span class="sxs-lookup"><span data-stu-id="cd8c3-212">Development for independent software vendors</span></span>

- [<span data-ttu-id="cd8c3-213">ISV Studio を使用した X++ モジュールのパッケージへのリンク</span><span class="sxs-lookup"><span data-stu-id="cd8c3-213">Link X++ modules to packages by using ISV Studio</span></span>](isv-studio-solutions.md)
- [<span data-ttu-id="cd8c3-214">ISV ライセンス</span><span class="sxs-lookup"><span data-stu-id="cd8c3-214">ISV licensing</span></span>](isv-licensing.md)
- [<span data-ttu-id="cd8c3-215">オンプレミスの ISV ライセンス</span><span class="sxs-lookup"><span data-stu-id="cd8c3-215">ISV licensing on-premises</span></span>](isv-licensing-on-prem.md)

## <a name="supply-chain-management"></a><span data-ttu-id="cd8c3-216">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cd8c3-216">Supply Chain Management</span></span>

- [<span data-ttu-id="cd8c3-217">ガント コントロール開発ガイド</span><span class="sxs-lookup"><span data-stu-id="cd8c3-217">Gantt control development guide</span></span>](../user-interface/gantt-development-guide.md)
- [<span data-ttu-id="cd8c3-218">新しい輸送管理エンジンの作成</span><span class="sxs-lookup"><span data-stu-id="cd8c3-218">Create a new transportation management engine</span></span>](../../../supply-chain/transportation/create-new-transportation-management-engine.md)

## <a name="additional-resources"></a><span data-ttu-id="cd8c3-219">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="cd8c3-219">Additional resources</span></span>

[<span data-ttu-id="cd8c3-220">開発のための内部者向けヒント</span><span class="sxs-lookup"><span data-stu-id="cd8c3-220">Insider tips on development</span></span>](https://community.dynamics.com/ax/b/newdynamicsax)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
