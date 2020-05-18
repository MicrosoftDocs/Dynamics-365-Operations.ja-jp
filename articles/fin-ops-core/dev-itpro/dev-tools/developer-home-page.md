---
title: ホームページの開発とカスタマイズ
description: このトピックでは、開発に関するトピックへのリンクを提供します。
author: RobinARH
manager: AnnBe
ms.date: 04/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0e23e7aedb069fb0cd7c862e41f6104f03f69b7
ms.sourcegitcommit: de217452a85429675994e9cc0e06eb4821cab3e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/30/2020
ms.locfileid: "3325801"
---
# <a name="develop-and-customize-home-page"></a><span data-ttu-id="c80c2-103">ホームページの開発とカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="c80c2-103">Develop and customize home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c80c2-104">このトピックでは、開発に関するトピックへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="c80c2-104">This topic provides links to topics about development.</span></span>

## <a name="overview"></a><span data-ttu-id="c80c2-105">概要</span><span class="sxs-lookup"><span data-stu-id="c80c2-105">Overview</span></span>

<span data-ttu-id="c80c2-106">Finance and Operations アプリケーションは、Microsoft が提供する次世代エンタープライズ リソース プランニング (ERP) を表します。</span><span class="sxs-lookup"><span data-stu-id="c80c2-106">The Finance and Operations applications represent the next-generation enterprise resource planning (ERP) offering from Microsoft.</span></span> <span data-ttu-id="c80c2-107">このアプリでは、パブリック クラウドとプライベート クラウド両方のクラウド ベースのソリューションおよびオンプレミスとして、全体の ERP アプリケーション スイートを有効できます。</span><span class="sxs-lookup"><span data-stu-id="c80c2-107">The apps enable the entire ERP application suite as a cloud-based solution, for both public and private clouds, as well as on-premises.</span></span> <span data-ttu-id="c80c2-108">このアプリは、Microsoft からの最新テクノロジーで構築時に、クラウドでの操作の速度、わかりやすさ、およびコスト効率性を利用します。</span><span class="sxs-lookup"><span data-stu-id="c80c2-108">The apps leverage the speed, simplicity, and cost-effectiveness of working in the cloud, while building on the latest technology from Microsoft.</span></span> <span data-ttu-id="c80c2-109">開発経験には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c80c2-109">The development experience includes:</span></span>

- <span data-ttu-id="c80c2-110">実行環境から切り離された開発ツール。</span><span class="sxs-lookup"><span data-stu-id="c80c2-110">Development tools that are decoupled from any running environment.</span></span> <span data-ttu-id="c80c2-111">オンライン データベースではなく、ローカルの XML ベースのファイルに対して作成します。</span><span class="sxs-lookup"><span data-stu-id="c80c2-111">You develop against local, XML-based files, not the online database.</span></span>
- <span data-ttu-id="c80c2-112">Microsoft Visual Studio が開発環境です。</span><span class="sxs-lookup"><span data-stu-id="c80c2-112">Microsoft Visual Studio is the development environment.</span></span> <span data-ttu-id="c80c2-113">Visual Studio 環境は、円滑で慣れ親しんだエクスペリエンスを提供するようにカスタマイズされています。</span><span class="sxs-lookup"><span data-stu-id="c80c2-113">The Visual Studio environment is customized to provide you with a smooth and familiar experience.</span></span>
- <span data-ttu-id="c80c2-114">X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。</span><span class="sxs-lookup"><span data-stu-id="c80c2-114">The X++ compiler generates Common Intermediate Language (CIL) for all features.</span></span> <span data-ttu-id="c80c2-115">CIL は C\# プログラミング言語などの他の .NET ベース (マネージド) の言語で使用されるものと同じ中間言語です。</span><span class="sxs-lookup"><span data-stu-id="c80c2-115">CIL is the same intermediate language used by other .NET-based (managed) languages, such as the C\# programming language.</span></span>
- <span data-ttu-id="c80c2-116">ブラウザー ベースのクライアントおよびフォームのデザイン パターンを活用して、改善されたエンド ユーザー エクスペリエンスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="c80c2-116">You can leverage the browser-based client and the design patterns for forms to provide an improved end-user experience.</span></span>
- <span data-ttu-id="c80c2-117">Application Lifecycle Model (ALM) は、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。</span><span class="sxs-lookup"><span data-stu-id="c80c2-117">The Application Lifecycle Model (ALM) supports build automation, test automation, and deployment of models to the cloud.</span></span>

## <a name="architecture"></a><span data-ttu-id="c80c2-118">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="c80c2-118">Architecture</span></span>

- [<span data-ttu-id="c80c2-119">アプリケーション スタックおよびサーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="c80c2-119">Application stack and server architecture</span></span>](application-stack-server-architecture.md)

## <a name="getting-started"></a><span data-ttu-id="c80c2-120">はじめに</span><span class="sxs-lookup"><span data-stu-id="c80c2-120">Getting started</span></span>

- [<span data-ttu-id="c80c2-121">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="c80c2-121">Get evaluation copies</span></span>](get-evaluation-copy.md)
- [<span data-ttu-id="c80c2-122">プレビュー サブスクリプションのサインアップ</span><span class="sxs-lookup"><span data-stu-id="c80c2-122">Sign up for preview subscriptions</span></span>](sign-up-preview-subscription.md)
- [<span data-ttu-id="c80c2-123">開発環境の配置とアクセス</span><span class="sxs-lookup"><span data-stu-id="c80c2-123">Deploy and access development environments</span></span>](../dev-tools/access-instances.md)
- [<span data-ttu-id="c80c2-124">開発システム要件</span><span class="sxs-lookup"><span data-stu-id="c80c2-124">Development system requirements</span></span>](development-system-requirements.md)
- [<span data-ttu-id="c80c2-125">削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="c80c2-125">Removed or deprecated features</span></span>](../migration-upgrade/deprecated-features.md)
- [<span data-ttu-id="c80c2-126">非推奨 API</span><span class="sxs-lookup"><span data-stu-id="c80c2-126">Deprecated APIs</span></span>](../migration-upgrade/deprecated-apis.md)
- [<span data-ttu-id="c80c2-127">ローカル開発 (VHD) 環境の名前変更</span><span class="sxs-lookup"><span data-stu-id="c80c2-127">Rename a local development (VHD) environment</span></span>](../migration-upgrade/vso-machine-renaming.md)
- [<span data-ttu-id="c80c2-128">Azure DevOps の概要 (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="c80c2-128">Introduction to Azure DevOps (Video)</span></span>](https://channel9.msdn.com/Events/Build/2014/2-575)

## <a name="fleet-management"></a><span data-ttu-id="c80c2-129">フリート管理</span><span class="sxs-lookup"><span data-stu-id="c80c2-129">Fleet Management</span></span>

- [<span data-ttu-id="c80c2-130">フリート管理のサンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="c80c2-130">Fleet Management sample application</span></span>](introduction-fleet-management-sample.md)
- [<span data-ttu-id="c80c2-131">フリート管理のサンプル アプリケーションのためのエンド ツー エンドのシナリオ</span><span class="sxs-lookup"><span data-stu-id="c80c2-131">End-to-end scenario for the Fleet Management sample application</span></span>](fleet-management-sample.md)

## <a name="development-tools"></a><span data-ttu-id="c80c2-132">開発ツール</span><span class="sxs-lookup"><span data-stu-id="c80c2-132">Development tools</span></span>

### <a name="tutorials-for-development-tools"></a><span data-ttu-id="c80c2-133">開発ツールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="c80c2-133">Tutorials for development tools</span></span>

- [<span data-ttu-id="c80c2-134">開発ツールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="c80c2-134">Development tools tutorial</span></span>](introduction-visual-studio.md)
- [<span data-ttu-id="c80c2-135">モデルとデータ モデル要素の作成の概要</span><span class="sxs-lookup"><span data-stu-id="c80c2-135">Create models and data model elements overview</span></span>](create-data-model-elements.md)
- [<span data-ttu-id="c80c2-136">プロジェクトのビルドおよびデバッグ</span><span class="sxs-lookup"><span data-stu-id="c80c2-136">Build and debug projects</span></span>](build-debug-project.md)
- [<span data-ttu-id="c80c2-137">バージョン コントロール、メタデータ検索、およびナビゲーション</span><span class="sxs-lookup"><span data-stu-id="c80c2-137">Version control, metadata search, and navigation</span></span>](version-control-metadata-navigation.md)

### <a name="tools-models-and-vms"></a><span data-ttu-id="c80c2-138">ツール、モデル、VM</span><span class="sxs-lookup"><span data-stu-id="c80c2-138">Tools, models, and VMs</span></span>

- [<span data-ttu-id="c80c2-139">Visual Studioの開発ツール</span><span class="sxs-lookup"><span data-stu-id="c80c2-139">Development tools in Visual Studio</span></span>](development-tools-overview.md)
- [<span data-ttu-id="c80c2-140">アプリケーション エクスプローラー</span><span class="sxs-lookup"><span data-stu-id="c80c2-140">Application Explorer</span></span>](application-explorer.md)
- [<span data-ttu-id="c80c2-141">Visual Studio における Finance and Operations のプロジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="c80c2-141">Finance and Operations project type in Visual Studio</span></span>](projects.md)
- [<span data-ttu-id="c80c2-142">要素デザイナー</span><span class="sxs-lookup"><span data-stu-id="c80c2-142">Element designers</span></span>](element-designers.md)
- [<span data-ttu-id="c80c2-143">要素の使用方法を決定するためのコマンド</span><span class="sxs-lookup"><span data-stu-id="c80c2-143">Commands for determining how elements are used</span></span>](element-usage.md)
- [<span data-ttu-id="c80c2-144">モデルとパッケージ</span><span class="sxs-lookup"><span data-stu-id="c80c2-144">Models and packages</span></span>](models.md)
- [<span data-ttu-id="c80c2-145">ビルド操作</span><span class="sxs-lookup"><span data-stu-id="c80c2-145">Build operations</span></span>](build-operations.md)
- [<span data-ttu-id="c80c2-146">コード エディター機能</span><span class="sxs-lookup"><span data-stu-id="c80c2-146">Code editor features</span></span>](code-editor.md)
- [<span data-ttu-id="c80c2-147">Visual Studioのツールアドイン</span><span class="sxs-lookup"><span data-stu-id="c80c2-147">Tools add-ins for Visual Studio</span></span>](developer-tools-add-ins.md)
- [<span data-ttu-id="c80c2-148">モデルのエクスポートとインポート</span><span class="sxs-lookup"><span data-stu-id="c80c2-148">Export and import models</span></span>](models-export-import.md)
- [<span data-ttu-id="c80c2-149">Visual Studio でのメタデータの検索</span><span class="sxs-lookup"><span data-stu-id="c80c2-149">Metadata search in Visual Studio</span></span>](metadata-search-visual-studio.md)
- [<span data-ttu-id="c80c2-150">開発マシンでの新しいユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="c80c2-150">Create new users on development machines</span></span>](enable-development-machine.md)
- [<span data-ttu-id="c80c2-151"> Visual Studio の開発ツールを更新する</span><span class="sxs-lookup"><span data-stu-id="c80c2-151">Update the Visual Studio development tools</span></span>](update-development-tools.md)
- [<span data-ttu-id="c80c2-152">管理者アクセスを許可しない開発用 VM および ビルド用 VM に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="c80c2-152">Development and build VMs that don't allow admin access FAQ</span></span>](../sysadmin/VMs-no-admin-access.md)

## <a name="build-automation-using-azure"></a><span data-ttu-id="c80c2-153">Azure を使用したビルドの自動化</span><span class="sxs-lookup"><span data-stu-id="c80c2-153">Build automation using Azure</span></span>

- [<span data-ttu-id="c80c2-154">Microsoft にホストされるエージェント、および Azure Pipelines を使用したビルドの自動化</span><span class="sxs-lookup"><span data-stu-id="c80c2-154">Build automation using Microsoft-hosted agents and Azure Pipelines</span></span>](hosted-build-automation.md)
- [<span data-ttu-id="c80c2-155">Azure Pipelines にある配置可能なパッケージへのライセンス ファイルの追加</span><span class="sxs-lookup"><span data-stu-id="c80c2-155">Add license files to a deployable package in Azure Pipelines</span></span>](pipeline-add-license-package.md)
- [<span data-ttu-id="c80c2-156">Azure Pipelines に配置可能なパッケージの作成</span><span class="sxs-lookup"><span data-stu-id="c80c2-156">Create deployable packages in Azure Pipelines</span></span>](pipeline-create-deployable-package.md)
- [<span data-ttu-id="c80c2-157">Azure Pipelines で、X++ モデルのバージョン管理</span><span class="sxs-lookup"><span data-stu-id="c80c2-157">X++ model-versioning in Azure Pipelines</span></span>](pipeline-model-version.md)

## <a name="x-programming-language"></a><span data-ttu-id="c80c2-158">X++ プログラミング言語</span><span class="sxs-lookup"><span data-stu-id="c80c2-158">X++ programming language</span></span>

### <a name="overviews"></a><span data-ttu-id="c80c2-159">概要</span><span class="sxs-lookup"><span data-stu-id="c80c2-159">Overviews</span></span>

- [<span data-ttu-id="c80c2-160">X++ およびデバッガーの機能</span><span class="sxs-lookup"><span data-stu-id="c80c2-160">X++ and debugger features</span></span>](new-x-debugger-features.md)
- [<span data-ttu-id="c80c2-161">C\# と X++ ソース コードを使用してビジネス ロジックを記述する</span><span class="sxs-lookup"><span data-stu-id="c80c2-161">Write business logic by using C\# and X++ source code</span></span>](write-business-logic.md)

### <a name="language-support"></a><span data-ttu-id="c80c2-162">言語サポート</span><span class="sxs-lookup"><span data-stu-id="c80c2-162">Language support</span></span>

- [<span data-ttu-id="c80c2-163">X++ と X++ コンパイラの変更</span><span class="sxs-lookup"><span data-stu-id="c80c2-163">Changes in X++ and the X++ compiler</span></span>](programming-language-support.md)
- [<span data-ttu-id="c80c2-164">要求または応答シナリオの EventHandlerResult クラス</span><span class="sxs-lookup"><span data-stu-id="c80c2-164">EventHandlerResult classes in request or response scenarios</span></span>](event-handler-result-class.md)
- [<span data-ttu-id="c80c2-165">Visual Studioのデバッガーを使用して  X++ コードをデバッグする</span><span class="sxs-lookup"><span data-stu-id="c80c2-165">Debug X++ code by using the debugger in Visual Studio</span></span>](debug-xpp.md)
- [<span data-ttu-id="c80c2-166">C\# の統合言語クエリ (LINQ) プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c80c2-166">Language Integrated Query (LINQ) provider for C\#</span></span>](linq-provider-c.md)
- [<span data-ttu-id="c80c2-167">ベスト プラクティス ルールの記述</span><span class="sxs-lookup"><span data-stu-id="c80c2-167">Write best practice rules</span></span>](author-best-practice-rules.md)

### <a name="reference"></a><span data-ttu-id="c80c2-168">参照</span><span class="sxs-lookup"><span data-stu-id="c80c2-168">Reference</span></span>

- [<span data-ttu-id="c80c2-169">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="c80c2-169">X++ language reference</span></span>](../dev-ref/xpp-language-reference.md)

## <a name="customize-with-extensions-and-overlayering"></a><span data-ttu-id="c80c2-170">拡張機能およびオーバーレイによってカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="c80c2-170">Customize with extensions and overlayering</span></span>

- [<span data-ttu-id="c80c2-171">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="c80c2-171">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
- [<span data-ttu-id="c80c2-172">拡張機能を使用してアプリケーション スイート レポートをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="c80c2-172">Customize App Suite reports by using extensions</span></span>](../analytics/customize-app-suite-reports-with-extensions.md)

## <a name="code-migration"></a><span data-ttu-id="c80c2-173">コードの移行</span><span class="sxs-lookup"><span data-stu-id="c80c2-173">Code migration</span></span>

- [<span data-ttu-id="c80c2-174">Visual Studio  での競合を解決する方法 (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="c80c2-174">How to resolve conflicts in Visual Studio (video)</span></span>](https://youtu.be/4rxO0zUN2zU)
- [<span data-ttu-id="c80c2-175">コードの移行とホーム ページのアップグレード</span><span class="sxs-lookup"><span data-stu-id="c80c2-175">Code migration and upgrade home page</span></span>](../migration-upgrade/code-migration-home-page.md)

## <a name="move-packages-between-environments"></a><span data-ttu-id="c80c2-176">環境間でパッケージを移動する</span><span class="sxs-lookup"><span data-stu-id="c80c2-176">Move packages between environments</span></span>

- [<span data-ttu-id="c80c2-177">配置可能なモデル パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="c80c2-177">Create deployable packages of models</span></span>](../deployment/create-apply-deployable-package.md)

## <a name="performance"></a><span data-ttu-id="c80c2-178">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="c80c2-178">Performance</span></span>

- [<span data-ttu-id="c80c2-179">Trace Parser を使用してトレースを実行</span><span class="sxs-lookup"><span data-stu-id="c80c2-179">Take traces by using Trace parser</span></span>](../perf-test/trace-trace-tutorial.md)
- [<span data-ttu-id="c80c2-180">Trace Parser を使用した問題点の診断およびパフォーマンスの分析</span><span class="sxs-lookup"><span data-stu-id="c80c2-180">Diagnose issues and analyze performance by using Trace parser</span></span>](../perf-test/trace-parser.md)
- [<span data-ttu-id="c80c2-181">パフォーマンス タイマー</span><span class="sxs-lookup"><span data-stu-id="c80c2-181">Performance timer</span></span>](../perf-test/performance-timer.md)

## <a name="user-interface-concepts"></a><span data-ttu-id="c80c2-182">ユーザー インターフェイスのコンセプト</span><span class="sxs-lookup"><span data-stu-id="c80c2-182">User interface concepts</span></span>

<span data-ttu-id="c80c2-183">クライアントは、すべての主要なブラウザーで動作する HTML Web クライアントです。</span><span class="sxs-lookup"><span data-stu-id="c80c2-183">The client is an HTML web client that runs in all major browsers.</span></span> <span data-ttu-id="c80c2-184">ユーザー インターフェイスの開発およびカスタマイズの詳細ついては、[ユーザー インターフェイス開発ホーム ページ](../user-interface/user-interface-development-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c80c2-184">For information about developing and customizing the user interface, see the [User interface development home page](../user-interface/user-interface-development-home-page.md).</span></span>

## <a name="analytics"></a><span data-ttu-id="c80c2-185">分析</span><span class="sxs-lookup"><span data-stu-id="c80c2-185">Analytics</span></span>

- [<span data-ttu-id="c80c2-186">分析、集計の測定、および KPI モデリング</span><span class="sxs-lookup"><span data-stu-id="c80c2-186">Analytics, aggregate measurements, and KPI modeling</span></span>](../analytics/analytics.md)

## <a name="reporting-services"></a><span data-ttu-id="c80c2-187">Reporting Services</span><span class="sxs-lookup"><span data-stu-id="c80c2-187">Reporting services</span></span>

- [<span data-ttu-id="c80c2-188">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="c80c2-188">Electronic reporting (ER) overview</span></span>](../analytics/general-electronic-reporting.md)

## <a name="data-entities-and-odata"></a><span data-ttu-id="c80c2-189">データ エンティティおよび OData</span><span class="sxs-lookup"><span data-stu-id="c80c2-189">Data entities and OData</span></span>

- [<span data-ttu-id="c80c2-190">データ エンティティの概要</span><span class="sxs-lookup"><span data-stu-id="c80c2-190">Data entities overview</span></span>](../data-entities/data-entities.md)
- [<span data-ttu-id="c80c2-191">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="c80c2-191">Open Data Protocol (OData)</span></span>](../data-entities/odata.md)

## <a name="testing-support-in-visual-studio"></a><span data-ttu-id="c80c2-192">Visual Studio でのテストのサポート</span><span class="sxs-lookup"><span data-stu-id="c80c2-192">Testing support in Visual Studio</span></span>

- [<span data-ttu-id="c80c2-193">テストと検証</span><span class="sxs-lookup"><span data-stu-id="c80c2-193">Testing and validations</span></span>](../perf-test/testing-validation.md)
- [<span data-ttu-id="c80c2-194">Visual Studio のプロジェクトをテストする</span><span class="sxs-lookup"><span data-stu-id="c80c2-194">Test projects in Visual Studio</span></span>](../perf-test/testing-support.md)
- [<span data-ttu-id="c80c2-195">継続的ビルドとテストの自動化を使用した開発者トポロジの展開</span><span class="sxs-lookup"><span data-stu-id="c80c2-195">Developer topology deployment with continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="c80c2-196">タスク レコーダー リソース</span><span class="sxs-lookup"><span data-stu-id="c80c2-196">Task recorder resources</span></span>](../user-interface/task-recorder.md)

## <a name="office-integration"></a><span data-ttu-id="c80c2-197">Office 統合</span><span class="sxs-lookup"><span data-stu-id="c80c2-197">Office integration</span></span>

- [<span data-ttu-id="c80c2-198">Office 統合の概要</span><span class="sxs-lookup"><span data-stu-id="c80c2-198">Office integration overview</span></span>](../office-integration/office-integration.md)

## <a name="intelligence"></a><span data-ttu-id="c80c2-199">インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="c80c2-199">Intelligence</span></span>

- [<span data-ttu-id="c80c2-200">ビジネス インテリジェンス (BI) およびレポート作成のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="c80c2-200">Business intelligence (BI) and reporting home page</span></span>](../analytics/bi-reporting-home-page.md)

## <a name="mobile-platform"></a><span data-ttu-id="c80c2-201">モバイル プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="c80c2-201">Mobile platform</span></span>

- [<span data-ttu-id="c80c2-202">モバイル プラットフォームのリソース</span><span class="sxs-lookup"><span data-stu-id="c80c2-202">Mobile platform resources</span></span>](../mobile-apps/platform/mobile-platform-home-page.md)

## <a name="global-finance-management"></a><span data-ttu-id="c80c2-203">グローバル財務管理</span><span class="sxs-lookup"><span data-stu-id="c80c2-203">Global finance management</span></span>

- [<span data-ttu-id="c80c2-204">Dynamics 365 Finance ホーム ページの開発</span><span class="sxs-lookup"><span data-stu-id="c80c2-204">Development for Dynamics 365 Finance home page</span></span>](../financial/financial-dev-home-page.md)

## <a name="licensing"></a><span data-ttu-id="c80c2-205">ライセンス</span><span class="sxs-lookup"><span data-stu-id="c80c2-205">Licensing</span></span>

- [<span data-ttu-id="c80c2-206">独立系ソフトウェア ベンダー (ISV) ライセンス</span><span class="sxs-lookup"><span data-stu-id="c80c2-206">Independent software vendor (ISV) licensing</span></span>](isv-licensing.md)

## <a name="supply-chain-management"></a><span data-ttu-id="c80c2-207">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="c80c2-207">Supply Chain Management</span></span>

- [<span data-ttu-id="c80c2-208">ガント コントロール作成ガイド</span><span class="sxs-lookup"><span data-stu-id="c80c2-208">Gantt control development guide</span></span>](../user-interface/gantt-development-guide.md)
- [<span data-ttu-id="c80c2-209">新しい輸送管理エンジンの作成</span><span class="sxs-lookup"><span data-stu-id="c80c2-209">Create a new transportation management engine</span></span>](../../../supply-chain/transportation/create-new-transportation-management-engine.md)

## <a name="additional-resources"></a><span data-ttu-id="c80c2-210">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="c80c2-210">Additional resources</span></span>

[<span data-ttu-id="c80c2-211">開発のための内部者向けヒント</span><span class="sxs-lookup"><span data-stu-id="c80c2-211">Insider tips on development</span></span>](https://community.dynamics.com/ax/b/newdynamicsax)
