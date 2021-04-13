---
title: ホームページの開発とカスタマイズ
description: このトピックでは、開発に関するトピックへのリンクを提供します。
author: RobinARH
ms.date: 04/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1ae81c9fb1fadae0974a9479127df0b130a73ae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745303"
---
# <a name="develop-and-customize-home-page"></a><span data-ttu-id="997a8-103">ホームページの開発とカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="997a8-103">Develop and customize home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="997a8-104">このトピックでは、開発に関するトピックへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="997a8-104">This topic provides links to topics about development.</span></span>

## <a name="overview"></a><span data-ttu-id="997a8-105">概要</span><span class="sxs-lookup"><span data-stu-id="997a8-105">Overview</span></span>

<span data-ttu-id="997a8-106">Finance and Operations アプリケーションは、Microsoft が提供する次世代エンタープライズ リソース プランニング (ERP) を表します。</span><span class="sxs-lookup"><span data-stu-id="997a8-106">The Finance and Operations applications represent the next-generation enterprise resource planning (ERP) offering from Microsoft.</span></span> <span data-ttu-id="997a8-107">このアプリでは、パブリック クラウドとプライベート クラウド両方のクラウド ベースのソリューションおよびオンプレミスとして、全体の ERP アプリケーション スイートを有効できます。</span><span class="sxs-lookup"><span data-stu-id="997a8-107">The apps enable the entire ERP application suite as a cloud-based solution, for both public and private clouds, as well as on-premises.</span></span> <span data-ttu-id="997a8-108">このアプリは、Microsoft からの最新テクノロジーで構築時に、クラウドでの操作の速度、わかりやすさ、およびコスト効率性を利用します。</span><span class="sxs-lookup"><span data-stu-id="997a8-108">The apps leverage the speed, simplicity, and cost-effectiveness of working in the cloud, while building on the latest technology from Microsoft.</span></span> <span data-ttu-id="997a8-109">開発経験には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="997a8-109">The development experience includes:</span></span>

- <span data-ttu-id="997a8-110">実行環境から切り離された開発ツール。</span><span class="sxs-lookup"><span data-stu-id="997a8-110">Development tools that are decoupled from any running environment.</span></span> <span data-ttu-id="997a8-111">オンライン データベースではなく、ローカルの XML ベースのファイルに対して作成します。</span><span class="sxs-lookup"><span data-stu-id="997a8-111">You develop against local, XML-based files, not the online database.</span></span>
- <span data-ttu-id="997a8-112">Microsoft Visual Studio が開発環境です。</span><span class="sxs-lookup"><span data-stu-id="997a8-112">Microsoft Visual Studio is the development environment.</span></span> <span data-ttu-id="997a8-113">Visual Studio 環境は、円滑で慣れ親しんだエクスペリエンスを提供するようにカスタマイズされています。</span><span class="sxs-lookup"><span data-stu-id="997a8-113">The Visual Studio environment is customized to provide you with a smooth and familiar experience.</span></span>
- <span data-ttu-id="997a8-114">X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。</span><span class="sxs-lookup"><span data-stu-id="997a8-114">The X++ compiler generates Common Intermediate Language (CIL) for all features.</span></span> <span data-ttu-id="997a8-115">CIL は C\# プログラミング言語などの他の .NET ベース (マネージド) の言語で使用されるものと同じ中間言語です。</span><span class="sxs-lookup"><span data-stu-id="997a8-115">CIL is the same intermediate language used by other .NET-based (managed) languages, such as the C\# programming language.</span></span>
- <span data-ttu-id="997a8-116">ブラウザー ベースのクライアントおよびフォームのデザイン パターンを活用して、改善されたエンド ユーザー エクスペリエンスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="997a8-116">You can leverage the browser-based client and the design patterns for forms to provide an improved end-user experience.</span></span>
- <span data-ttu-id="997a8-117">Application Lifecycle Model (ALM) は、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。</span><span class="sxs-lookup"><span data-stu-id="997a8-117">The Application Lifecycle Model (ALM) supports build automation, test automation, and deployment of models to the cloud.</span></span>

## <a name="architecture"></a><span data-ttu-id="997a8-118">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="997a8-118">Architecture</span></span>

- [<span data-ttu-id="997a8-119">アプリケーション スタックおよびサーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="997a8-119">Application stack and server architecture</span></span>](application-stack-server-architecture.md)

## <a name="getting-started"></a><span data-ttu-id="997a8-120">はじめに</span><span class="sxs-lookup"><span data-stu-id="997a8-120">Getting started</span></span>

- [<span data-ttu-id="997a8-121">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="997a8-121">Get evaluation copies</span></span>](get-evaluation-copy.md)
- [<span data-ttu-id="997a8-122">プレビュー サブスクリプションのサインアップ</span><span class="sxs-lookup"><span data-stu-id="997a8-122">Sign up for preview subscriptions</span></span>](sign-up-preview-subscription.md)
- [<span data-ttu-id="997a8-123">開発環境の配置とアクセス</span><span class="sxs-lookup"><span data-stu-id="997a8-123">Deploy and access development environments</span></span>](../dev-tools/access-instances.md)
- [<span data-ttu-id="997a8-124">開発システム要件</span><span class="sxs-lookup"><span data-stu-id="997a8-124">Development system requirements</span></span>](development-system-requirements.md)
- [<span data-ttu-id="997a8-125">削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="997a8-125">Removed or deprecated features</span></span>](../migration-upgrade/deprecated-features.md)
- [<span data-ttu-id="997a8-126">非推奨 API</span><span class="sxs-lookup"><span data-stu-id="997a8-126">Deprecated APIs</span></span>](../migration-upgrade/deprecated-apis.md)
- [<span data-ttu-id="997a8-127">ローカル開発 (VHD) 環境の名前変更</span><span class="sxs-lookup"><span data-stu-id="997a8-127">Rename a local development (VHD) environment</span></span>](../migration-upgrade/vso-machine-renaming.md)
- [<span data-ttu-id="997a8-128">Azure DevOps の概要 (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="997a8-128">Introduction to Azure DevOps (Video)</span></span>](https://channel9.msdn.com/Events/Build/2014/2-575)

## <a name="fleet-management"></a><span data-ttu-id="997a8-129">フリート管理</span><span class="sxs-lookup"><span data-stu-id="997a8-129">Fleet Management</span></span>

- [<span data-ttu-id="997a8-130">フリート管理のサンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="997a8-130">Fleet Management sample application</span></span>](introduction-fleet-management-sample.md)
- [<span data-ttu-id="997a8-131">フリート管理のサンプル アプリケーションのためのエンド ツー エンドのシナリオ</span><span class="sxs-lookup"><span data-stu-id="997a8-131">End-to-end scenario for the Fleet Management sample application</span></span>](fleet-management-sample.md)

## <a name="development-tools"></a><span data-ttu-id="997a8-132">開発ツール</span><span class="sxs-lookup"><span data-stu-id="997a8-132">Development tools</span></span>

### <a name="tutorials-for-development-tools"></a><span data-ttu-id="997a8-133">開発ツールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="997a8-133">Tutorials for development tools</span></span>

- [<span data-ttu-id="997a8-134">開発ツールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="997a8-134">Development tools tutorial</span></span>](introduction-visual-studio.md)
- [<span data-ttu-id="997a8-135">モデルとデータ モデル要素の作成の概要</span><span class="sxs-lookup"><span data-stu-id="997a8-135">Create models and data model elements overview</span></span>](create-data-model-elements.md)
- [<span data-ttu-id="997a8-136">プロジェクトのビルドおよびデバッグ</span><span class="sxs-lookup"><span data-stu-id="997a8-136">Build and debug projects</span></span>](build-debug-project.md)
- [<span data-ttu-id="997a8-137">バージョン コントロール、メタデータ検索、およびナビゲーション</span><span class="sxs-lookup"><span data-stu-id="997a8-137">Version control, metadata search, and navigation</span></span>](version-control-metadata-navigation.md)

### <a name="tools-models-and-vms"></a><span data-ttu-id="997a8-138">ツール、モデル、VM</span><span class="sxs-lookup"><span data-stu-id="997a8-138">Tools, models, and VMs</span></span>

- [<span data-ttu-id="997a8-139">Visual Studioの開発ツール</span><span class="sxs-lookup"><span data-stu-id="997a8-139">Development tools in Visual Studio</span></span>](development-tools-overview.md)
- [<span data-ttu-id="997a8-140">アプリケーション エクスプローラー</span><span class="sxs-lookup"><span data-stu-id="997a8-140">Application Explorer</span></span>](application-explorer.md)
- [<span data-ttu-id="997a8-141">Visual Studio における Finance and Operations のプロジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="997a8-141">Finance and Operations project type in Visual Studio</span></span>](projects.md)
- [<span data-ttu-id="997a8-142">要素デザイナー</span><span class="sxs-lookup"><span data-stu-id="997a8-142">Element designers</span></span>](element-designers.md)
- [<span data-ttu-id="997a8-143">要素の使用方法を決定するためのコマンド</span><span class="sxs-lookup"><span data-stu-id="997a8-143">Commands for determining how elements are used</span></span>](element-usage.md)
- [<span data-ttu-id="997a8-144">モデルとパッケージ</span><span class="sxs-lookup"><span data-stu-id="997a8-144">Models and packages</span></span>](models.md)
- [<span data-ttu-id="997a8-145">ビルド操作</span><span class="sxs-lookup"><span data-stu-id="997a8-145">Build operations</span></span>](build-operations.md)
- [<span data-ttu-id="997a8-146">コード エディター機能</span><span class="sxs-lookup"><span data-stu-id="997a8-146">Code editor features</span></span>](code-editor.md)
- [<span data-ttu-id="997a8-147">Visual Studioのツールアドイン</span><span class="sxs-lookup"><span data-stu-id="997a8-147">Tools add-ins for Visual Studio</span></span>](developer-tools-add-ins.md)
- [<span data-ttu-id="997a8-148">モデルのエクスポートとインポート</span><span class="sxs-lookup"><span data-stu-id="997a8-148">Export and import models</span></span>](models-export-import.md)
- [<span data-ttu-id="997a8-149">Visual Studio でのメタデータの検索</span><span class="sxs-lookup"><span data-stu-id="997a8-149">Metadata search in Visual Studio</span></span>](metadata-search-visual-studio.md)
- [<span data-ttu-id="997a8-150">開発マシンでの新しいユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="997a8-150">Create new users on development machines</span></span>](enable-development-machine.md)
- [<span data-ttu-id="997a8-151"> Visual Studio の開発ツールを更新する</span><span class="sxs-lookup"><span data-stu-id="997a8-151">Update the Visual Studio development tools</span></span>](update-development-tools.md)
- [<span data-ttu-id="997a8-152">管理者アクセスを許可しない開発用 VM および ビルド用 VM に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="997a8-152">Development and build VMs that don't allow admin access FAQ</span></span>](../sysadmin/VMs-no-admin-access.md)

## <a name="build-automation-using-azure"></a><span data-ttu-id="997a8-153">Azure を使用したビルドの自動化</span><span class="sxs-lookup"><span data-stu-id="997a8-153">Build automation using Azure</span></span>

- [<span data-ttu-id="997a8-154">Microsoft にホストされるエージェント、および Azure Pipelines を使用したビルドの自動化</span><span class="sxs-lookup"><span data-stu-id="997a8-154">Build automation using Microsoft-hosted agents and Azure Pipelines</span></span>](hosted-build-automation.md)
- [<span data-ttu-id="997a8-155">Azure Pipelines にある配置可能なパッケージへのライセンス ファイルの追加</span><span class="sxs-lookup"><span data-stu-id="997a8-155">Add license files to a deployable package in Azure Pipelines</span></span>](pipeline-add-license-package.md)
- [<span data-ttu-id="997a8-156">Azure Pipelines に配置可能なパッケージの作成</span><span class="sxs-lookup"><span data-stu-id="997a8-156">Create deployable packages in Azure Pipelines</span></span>](pipeline-create-deployable-package.md)
- [<span data-ttu-id="997a8-157">Azure Pipelines で、X++ モデルのバージョン管理</span><span class="sxs-lookup"><span data-stu-id="997a8-157">X++ model-versioning in Azure Pipelines</span></span>](pipeline-model-version.md)
- [<span data-ttu-id="997a8-158">Azure Pipelines を使用した資産のダウンロード</span><span class="sxs-lookup"><span data-stu-id="997a8-158">Download assets by using Azure Pipelines</span></span>](pipeline-asset-download.md)
- [<span data-ttu-id="997a8-159">Azure Pipelines を使用した資産のアップロード</span><span class="sxs-lookup"><span data-stu-id="997a8-159">Upload assets by using Azure Pipelines</span></span>](pipeline-asset-upload.md)
- [<span data-ttu-id="997a8-160">Azure Pipelines を使用した資産のデプロイ</span><span class="sxs-lookup"><span data-stu-id="997a8-160">Deploy assets by using Azure Pipelines</span></span>](pipeline-deploy-asset.md)
- [<span data-ttu-id="997a8-161">Azure Pipelines での Lifecycle Services (LCS) 接続の作成</span><span class="sxs-lookup"><span data-stu-id="997a8-161">Create a Lifecycle Services (LCS) connection in Azure Pipelines</span></span>](pipeline-lcs-connection.md)
- [<span data-ttu-id="997a8-162">新しい NuGet パッケージ用にホストされる Azure Pipeline の更新</span><span class="sxs-lookup"><span data-stu-id="997a8-162">Update the hosted Azure Pipeline for new NuGet packages</span></span>](pipeline-nuget-split.md)
- [<span data-ttu-id="997a8-163">Azure Pipelines でのレガシ パイプラインの更新</span><span class="sxs-lookup"><span data-stu-id="997a8-163">Update a legacy pipeline in Azure Pipelines</span></span>](pipeline-msbuild-update.md)

## <a name="x-programming-language"></a><span data-ttu-id="997a8-164">X++ プログラミング言語</span><span class="sxs-lookup"><span data-stu-id="997a8-164">X++ programming language</span></span>

### <a name="overviews"></a><span data-ttu-id="997a8-165">概要</span><span class="sxs-lookup"><span data-stu-id="997a8-165">Overviews</span></span>

- [<span data-ttu-id="997a8-166">X++ およびデバッガーの機能</span><span class="sxs-lookup"><span data-stu-id="997a8-166">X++ and debugger features</span></span>](new-x-debugger-features.md)
- [<span data-ttu-id="997a8-167">C\# と X++ ソース コードを使用してビジネス ロジックを記述する</span><span class="sxs-lookup"><span data-stu-id="997a8-167">Write business logic by using C\# and X++ source code</span></span>](write-business-logic.md)

### <a name="language-support"></a><span data-ttu-id="997a8-168">言語サポート</span><span class="sxs-lookup"><span data-stu-id="997a8-168">Language support</span></span>

- [<span data-ttu-id="997a8-169">X++ と X++ コンパイラの変更</span><span class="sxs-lookup"><span data-stu-id="997a8-169">Changes in X++ and the X++ compiler</span></span>](programming-language-support.md)
- [<span data-ttu-id="997a8-170">要求または応答シナリオの EventHandlerResult クラス</span><span class="sxs-lookup"><span data-stu-id="997a8-170">EventHandlerResult classes in request or response scenarios</span></span>](event-handler-result-class.md)
- [<span data-ttu-id="997a8-171">Visual Studioのデバッガーを使用して  X++ コードをデバッグする</span><span class="sxs-lookup"><span data-stu-id="997a8-171">Debug X++ code by using the debugger in Visual Studio</span></span>](debug-xpp.md)
- [<span data-ttu-id="997a8-172">C\# の統合言語クエリ (LINQ) プロバイダー</span><span class="sxs-lookup"><span data-stu-id="997a8-172">Language Integrated Query (LINQ) provider for C\#</span></span>](linq-provider-c.md)
- [<span data-ttu-id="997a8-173">ベスト プラクティス ルールの記述</span><span class="sxs-lookup"><span data-stu-id="997a8-173">Write best practice rules</span></span>](author-best-practice-rules.md)

### <a name="reference"></a><span data-ttu-id="997a8-174">参照</span><span class="sxs-lookup"><span data-stu-id="997a8-174">Reference</span></span>

- [<span data-ttu-id="997a8-175">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="997a8-175">X++ language reference</span></span>](../dev-ref/xpp-language-reference.md)

## <a name="customize-with-extensions-and-overlayering"></a><span data-ttu-id="997a8-176">拡張機能およびオーバーレイによってカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="997a8-176">Customize with extensions and overlayering</span></span>

- [<span data-ttu-id="997a8-177">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="997a8-177">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
- [<span data-ttu-id="997a8-178">拡張機能を使用してアプリケーション スイート レポートをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="997a8-178">Customize App Suite reports by using extensions</span></span>](../analytics/customize-app-suite-reports-with-extensions.md)

## <a name="code-migration"></a><span data-ttu-id="997a8-179">コードの移行</span><span class="sxs-lookup"><span data-stu-id="997a8-179">Code migration</span></span>

- [<span data-ttu-id="997a8-180">Visual Studio  での競合を解決する方法 (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="997a8-180">How to resolve conflicts in Visual Studio (video)</span></span>](https://youtu.be/4rxO0zUN2zU)
- [<span data-ttu-id="997a8-181">コードの移行とホーム ページのアップグレード</span><span class="sxs-lookup"><span data-stu-id="997a8-181">Code migration and upgrade home page</span></span>](../migration-upgrade/code-migration-home-page.md)

## <a name="move-packages-between-environments"></a><span data-ttu-id="997a8-182">環境間でパッケージを移動する</span><span class="sxs-lookup"><span data-stu-id="997a8-182">Move packages between environments</span></span>

- [<span data-ttu-id="997a8-183">配置可能なモデル パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="997a8-183">Create deployable packages of models</span></span>](../deployment/create-apply-deployable-package.md)

## <a name="performance"></a><span data-ttu-id="997a8-184">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="997a8-184">Performance</span></span>

- [<span data-ttu-id="997a8-185">Trace Parser を使用してトレースを実行</span><span class="sxs-lookup"><span data-stu-id="997a8-185">Take traces by using Trace parser</span></span>](../perf-test/trace-trace-tutorial.md)
- [<span data-ttu-id="997a8-186">Trace Parser を使用した問題点の診断およびパフォーマンスの分析</span><span class="sxs-lookup"><span data-stu-id="997a8-186">Diagnose issues and analyze performance by using Trace parser</span></span>](../perf-test/trace-parser.md)
- [<span data-ttu-id="997a8-187">パフォーマンス タイマー</span><span class="sxs-lookup"><span data-stu-id="997a8-187">Performance timer</span></span>](../perf-test/performance-timer.md)

## <a name="user-interface-concepts"></a><span data-ttu-id="997a8-188">ユーザー インターフェイスのコンセプト</span><span class="sxs-lookup"><span data-stu-id="997a8-188">User interface concepts</span></span>

<span data-ttu-id="997a8-189">クライアントは、すべての主要なブラウザーで動作する HTML Web クライアントです。</span><span class="sxs-lookup"><span data-stu-id="997a8-189">The client is an HTML web client that runs in all major browsers.</span></span> <span data-ttu-id="997a8-190">ユーザー インターフェイスの開発およびカスタマイズの詳細ついては、[ユーザー インターフェイス開発ホーム ページ](../user-interface/user-interface-development-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="997a8-190">For information about developing and customizing the user interface, see the [User interface development home page](../user-interface/user-interface-development-home-page.md).</span></span>

## <a name="analytics"></a><span data-ttu-id="997a8-191">分析</span><span class="sxs-lookup"><span data-stu-id="997a8-191">Analytics</span></span>

- [<span data-ttu-id="997a8-192">分析、集計の測定、および KPI モデリング</span><span class="sxs-lookup"><span data-stu-id="997a8-192">Analytics, aggregate measurements, and KPI modeling</span></span>](../analytics/analytics.md)

## <a name="reporting-services"></a><span data-ttu-id="997a8-193">Reporting Services</span><span class="sxs-lookup"><span data-stu-id="997a8-193">Reporting services</span></span>

- [<span data-ttu-id="997a8-194">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="997a8-194">Electronic reporting (ER) overview</span></span>](../analytics/general-electronic-reporting.md)

## <a name="data-entities-and-odata"></a><span data-ttu-id="997a8-195">データ エンティティおよび OData</span><span class="sxs-lookup"><span data-stu-id="997a8-195">Data entities and OData</span></span>

- [<span data-ttu-id="997a8-196">データ エンティティの概要</span><span class="sxs-lookup"><span data-stu-id="997a8-196">Data entities overview</span></span>](../data-entities/data-entities.md)
- [<span data-ttu-id="997a8-197">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="997a8-197">Open Data Protocol (OData)</span></span>](../data-entities/odata.md)

## <a name="testing-support-in-visual-studio"></a><span data-ttu-id="997a8-198">Visual Studio でのテストのサポート</span><span class="sxs-lookup"><span data-stu-id="997a8-198">Testing support in Visual Studio</span></span>

- [<span data-ttu-id="997a8-199">テストと検証</span><span class="sxs-lookup"><span data-stu-id="997a8-199">Testing and validations</span></span>](../perf-test/testing-validation.md)
- [<span data-ttu-id="997a8-200">Visual Studio のプロジェクトをテストする</span><span class="sxs-lookup"><span data-stu-id="997a8-200">Test projects in Visual Studio</span></span>](../perf-test/testing-support.md)
- [<span data-ttu-id="997a8-201">継続的なビルドおよびテストの自動化環境の配置と使用</span><span class="sxs-lookup"><span data-stu-id="997a8-201">Deploy and use a continuous build and test automation environment</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="997a8-202">タスク レコーダー リソース</span><span class="sxs-lookup"><span data-stu-id="997a8-202">Task recorder resources</span></span>](../user-interface/task-recorder.md)

## <a name="office-integration"></a><span data-ttu-id="997a8-203">Office 統合</span><span class="sxs-lookup"><span data-stu-id="997a8-203">Office integration</span></span>

- [<span data-ttu-id="997a8-204">Office 統合の概要</span><span class="sxs-lookup"><span data-stu-id="997a8-204">Office integration overview</span></span>](../office-integration/office-integration.md)

## <a name="intelligence"></a><span data-ttu-id="997a8-205">インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="997a8-205">Intelligence</span></span>

- [<span data-ttu-id="997a8-206">ビジネス インテリジェンス (BI) およびレポート作成のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="997a8-206">Business intelligence (BI) and reporting home page</span></span>](../analytics/bi-reporting-home-page.md)

## <a name="mobile-platform"></a><span data-ttu-id="997a8-207">モバイル プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="997a8-207">Mobile platform</span></span>

- [<span data-ttu-id="997a8-208">モバイル プラットフォームのリソース</span><span class="sxs-lookup"><span data-stu-id="997a8-208">Mobile platform resources</span></span>](../mobile-apps/platform/mobile-platform-home-page.md)

## <a name="global-finance-management"></a><span data-ttu-id="997a8-209">グローバル財務管理</span><span class="sxs-lookup"><span data-stu-id="997a8-209">Global finance management</span></span>

- [<span data-ttu-id="997a8-210">Dynamics 365 Finance ホーム ページの開発</span><span class="sxs-lookup"><span data-stu-id="997a8-210">Development for Dynamics 365 Finance home page</span></span>](../financial/financial-dev-home-page.md)

## <a name="licensing"></a><span data-ttu-id="997a8-211">ライセンス</span><span class="sxs-lookup"><span data-stu-id="997a8-211">Licensing</span></span>

- [<span data-ttu-id="997a8-212">独立系ソフトウェア ベンダー (ISV) ライセンス</span><span class="sxs-lookup"><span data-stu-id="997a8-212">Independent software vendor (ISV) licensing</span></span>](isv-licensing.md)

## <a name="supply-chain-management"></a><span data-ttu-id="997a8-213">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="997a8-213">Supply Chain Management</span></span>

- [<span data-ttu-id="997a8-214">ガント コントロール作成ガイド</span><span class="sxs-lookup"><span data-stu-id="997a8-214">Gantt control development guide</span></span>](../user-interface/gantt-development-guide.md)
- [<span data-ttu-id="997a8-215">新しい輸送管理エンジンの作成</span><span class="sxs-lookup"><span data-stu-id="997a8-215">Create a new transportation management engine</span></span>](../../../supply-chain/transportation/create-new-transportation-management-engine.md)

## <a name="additional-resources"></a><span data-ttu-id="997a8-216">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="997a8-216">Additional resources</span></span>

[<span data-ttu-id="997a8-217">開発のための内部者向けヒント</span><span class="sxs-lookup"><span data-stu-id="997a8-217">Insider tips on development</span></span>](https://community.dynamics.com/ax/b/newdynamicsax)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
