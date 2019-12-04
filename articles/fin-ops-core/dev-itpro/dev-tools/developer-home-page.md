---
title: ホームページの開発とカスタマイズ
description: このトピックでは、開発に関するトピックへのリンクを提供します。
author: RobinARH
manager: AnnBe
ms.date: 10/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.assetid: 06e26767-6056-4755-b47e-0bda71833581
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2264d919325972639ac09149cd20aa7f729b119
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811720"
---
# <a name="develop-and-customize-home-page"></a><span data-ttu-id="0dc1f-103">ホームページの開発とカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-103">Develop and customize home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0dc1f-104">このトピックでは、開発に関するトピックへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-104">This topic provides links to topics about development.</span></span>

## <a name="overview"></a><span data-ttu-id="0dc1f-105">概要</span><span class="sxs-lookup"><span data-stu-id="0dc1f-105">Overview</span></span>

<span data-ttu-id="0dc1f-106">Finance and Operations アプリケーションは、Microsoft から提供されている次世代エンタープライズ リソース プランニング (ERP) を表します。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-106">The Finance and Operations applications represent the next-generation enterprise resource planning (ERP) offering from Microsoft.</span></span> <span data-ttu-id="0dc1f-107">これは、パブリック クラウドとプライベート クラウド両方のクラウド ベースのソリューションおよびオンプレミスとして、全体の ERP アプリケーション スイートを有効にするために設計されています。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-107">It is designed to enable the entire ERP application suite as a cloud-based solution, for both public and private clouds, as well as on-premises.</span></span> <span data-ttu-id="0dc1f-108">これは、Microsoft からの最新テクノロジーで構築時に、クラウドでの操作の速度、わかりやすさ、およびコスト効率性を利用します。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-108">It leverages the speed, simplicity, and cost-effectiveness of working in the cloud, while building on the latest technology from Microsoft.</span></span> <span data-ttu-id="0dc1f-109">このリリースでは、開発環境が大幅に変更されています。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-109">This release introduces significant changes to the development experience.</span></span> <span data-ttu-id="0dc1f-110">これらの変更の内容は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-110">These changes include:</span></span>

- <span data-ttu-id="0dc1f-111">実行環境から切り離された開発ツール。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-111">Development tools that are decoupled from any running environment.</span></span> <span data-ttu-id="0dc1f-112">オンライン データベースではなく、ローカルの XML ベースのファイルに対して作成します。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-112">You develop against local, XML-based files, not the online database.</span></span>
- <span data-ttu-id="0dc1f-113">Microsoft Visual Studio が開発環境です。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-113">Microsoft Visual Studio is the development environment.</span></span> <span data-ttu-id="0dc1f-114">Visual Studio 環境は、円滑で慣れ親しんだエクスペリエンスを提供するようにカスタマイズされています。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-114">The Visual Studio environment is customized to provide you with a smooth and familiar experience.</span></span>
- <span data-ttu-id="0dc1f-115">X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-115">The X++ compiler generates Common Intermediate Language (CIL) for all features.</span></span> <span data-ttu-id="0dc1f-116">CIL は C\# プログラミング言語などの他の .NET ベース (マネージド) の言語で使用されるものと同じ中間言語です。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-116">CIL is the same intermediate language used by other .NET-based (managed) languages, such as the C\# programming language.</span></span>
- <span data-ttu-id="0dc1f-117">ブラウザー ベースのクライアントおよびフォームのデザイン パターンを活用して、改善されたエンド ユーザー エクスペリエンスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-117">You can leverage the browser-based client and the design patterns for forms to provide an improved end-user experience.</span></span>
- <span data-ttu-id="0dc1f-118">Application Lifecycle Model (ALM) は、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-118">The Application Lifecycle Model (ALM) supports build automation, test automation, and deployment of models to the cloud.</span></span>

## <a name="architecture"></a><span data-ttu-id="0dc1f-119">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-119">Architecture</span></span>
-   [<span data-ttu-id="0dc1f-120">アプリケーション スタックおよびサーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-120">Application stack and server architecture</span></span>](application-stack-server-architecture.md)

## <a name="getting-started"></a><span data-ttu-id="0dc1f-121">はじめに</span><span class="sxs-lookup"><span data-stu-id="0dc1f-121">Getting started</span></span>
-   [<span data-ttu-id="0dc1f-122">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="0dc1f-122">Get evaluation copies</span></span>](get-evaluation-copy.md)
-   [<span data-ttu-id="0dc1f-123">プレビュー サブスクリプションのサインアップ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-123">Sign up for preview subscriptions</span></span>](sign-up-preview-subscription.md)
-   [<span data-ttu-id="0dc1f-124">開発環境の配置とアクセス</span><span class="sxs-lookup"><span data-stu-id="0dc1f-124">Deploy and access development environments</span></span>](../dev-tools/access-instances.md)
-   [<span data-ttu-id="0dc1f-125">開発システム要件</span><span class="sxs-lookup"><span data-stu-id="0dc1f-125">Development system requirements</span></span>](development-system-requirements.md)
-   [<span data-ttu-id="0dc1f-126">削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="0dc1f-126">Removed or deprecated features</span></span>](../migration-upgrade/deprecated-features.md)
-   [<span data-ttu-id="0dc1f-127">非推奨 API</span><span class="sxs-lookup"><span data-stu-id="0dc1f-127">Deprecated APIs</span></span>](../migration-upgrade/deprecated-apis.md)
-   [<span data-ttu-id="0dc1f-128">ローカル開発 (VHD) 環境の名前変更</span><span class="sxs-lookup"><span data-stu-id="0dc1f-128">Rename a local development (VHD) environment</span></span>](../migration-upgrade/vso-machine-renaming.md)
-   [<span data-ttu-id="0dc1f-129">Azure DevOps の概要 (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="0dc1f-129">Introduction to Azure DevOps (Video)</span></span>](https://channel9.msdn.com/Events/Build/2014/2-575)
<!-- [Learn about packages, models and Visual Studio (Office Mix)](https://mix.office.com/watch/ies6lyit6773)-->
<!-- [Development tools performance tips (Office Mix)](https://mix.office.com/watch/rnp6ng9wu8kx)-->
<!-- [Feedback and support (Office Mix)](https://mix.office.com/watch/92azzna59jj6)-->

## <a name="fleet-management"></a><span data-ttu-id="0dc1f-130">フリート管理</span><span class="sxs-lookup"><span data-stu-id="0dc1f-130">Fleet Management</span></span>
-   [<span data-ttu-id="0dc1f-131">フリート管理のサンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0dc1f-131">Fleet Management sample application</span></span>](introduction-fleet-management-sample.md)
-   [<span data-ttu-id="0dc1f-132">フリート管理のサンプル アプリケーションのためのエンド ツー エンドのシナリオ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-132">End-to-end scenario for the Fleet Management sample application</span></span>](fleet-management-sample.md)

## <a name="development-tools"></a><span data-ttu-id="0dc1f-133">開発ツール</span><span class="sxs-lookup"><span data-stu-id="0dc1f-133">Development tools</span></span>
### <a name="tutorials"></a><span data-ttu-id="0dc1f-134">チュートリアル</span><span class="sxs-lookup"><span data-stu-id="0dc1f-134">Tutorials</span></span>

-   [<span data-ttu-id="0dc1f-135">開発ツールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="0dc1f-135">Development tools tutorial</span></span>](introduction-visual-studio.md)
-   [<span data-ttu-id="0dc1f-136">モデルとデータ モデル要素の作成の概要</span><span class="sxs-lookup"><span data-stu-id="0dc1f-136">Create models and data model elements overview</span></span>](create-data-model-elements.md)
-   [<span data-ttu-id="0dc1f-137">プロジェクトのビルドおよびデバッグ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-137">Build and debug projects</span></span>](build-debug-project.md)
-   [<span data-ttu-id="0dc1f-138">バージョン コントロール、メタデータ検索、およびナビゲーション</span><span class="sxs-lookup"><span data-stu-id="0dc1f-138">Version control, metadata search, and navigation</span></span>](version-control-metadata-navigation.md)

### <a name="tools-models-and-vms"></a><span data-ttu-id="0dc1f-139">ツール、モデル、VM</span><span class="sxs-lookup"><span data-stu-id="0dc1f-139">Tools, models, and VMs</span></span>

-   [<span data-ttu-id="0dc1f-140">Visual Studioの開発ツール</span><span class="sxs-lookup"><span data-stu-id="0dc1f-140">Development tools in Visual Studio</span></span>](development-tools-overview.md)
<!-- [Introduction to the development environment (Office Mix)](https://mix.office.com/watch/1tz7194y62m3s)-->
-   [<span data-ttu-id="0dc1f-141">アプリケーション エクスプローラー</span><span class="sxs-lookup"><span data-stu-id="0dc1f-141">Application Explorer</span></span>](application-explorer.md)
-   [<span data-ttu-id="0dc1f-142">Visual Studioの Finance and Operations の プロジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-142">Finance and Operations project type in Visual Studio</span></span>](projects.md)
-   [<span data-ttu-id="0dc1f-143">要素デザイナー</span><span class="sxs-lookup"><span data-stu-id="0dc1f-143">Element designers</span></span>](element-designers.md)
-   [<span data-ttu-id="0dc1f-144">要素の使用方法を決定するためのコマンド</span><span class="sxs-lookup"><span data-stu-id="0dc1f-144">Commands for determining how elements are used</span></span>](element-usage.md)
-   [<span data-ttu-id="0dc1f-145">モデルとパッケージ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-145">Models and packages</span></span>](models.md)
-   [<span data-ttu-id="0dc1f-146">ビルド操作</span><span class="sxs-lookup"><span data-stu-id="0dc1f-146">Build operations</span></span>](build-operations.md)
-   [<span data-ttu-id="0dc1f-147">コード エディター機能</span><span class="sxs-lookup"><span data-stu-id="0dc1f-147">Code editor features</span></span>](code-editor.md)
-   [<span data-ttu-id="0dc1f-148">Visual Studioのツールアドイン</span><span class="sxs-lookup"><span data-stu-id="0dc1f-148">Tools add-ins for Visual Studio</span></span>](developer-tools-add-ins.md)
-   [<span data-ttu-id="0dc1f-149">モデルのエクスポートとインポート</span><span class="sxs-lookup"><span data-stu-id="0dc1f-149">Export and import models</span></span>](models-export-import.md)
-   [<span data-ttu-id="0dc1f-150">Visual Studio でのメタデータの検索</span><span class="sxs-lookup"><span data-stu-id="0dc1f-150">Metadata search in Visual Studio</span></span>](metadata-search-visual-studio.md)
-   [<span data-ttu-id="0dc1f-151">開発マシンでの新しいユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="0dc1f-151">Create new users on development machines</span></span>](enable-development-machine.md)
-   [<span data-ttu-id="0dc1f-152"> Visual Studio の開発ツールを更新する</span><span class="sxs-lookup"><span data-stu-id="0dc1f-152">Update the Visual Studio development tools</span></span>](update-development-tools.md)
-   [<span data-ttu-id="0dc1f-153">管理者アクセスを許可しない開発用 VM および ビルド用 VM に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="0dc1f-153">Development and build VMs that don't allow admin access FAQ</span></span>](../sysadmin/VMs-no-admin-access.md)
<!--  [Configure version control with Azure DevOps (Office Mix)](https://mix.office.com/watch/1ftubtqzp3xxl)-->

## <a name="x-programming-language"></a><span data-ttu-id="0dc1f-154">X++ プログラミング言語</span><span class="sxs-lookup"><span data-stu-id="0dc1f-154">X++ programming language</span></span>
### <a name="tutorials"></a><span data-ttu-id="0dc1f-155">チュートリアル</span><span class="sxs-lookup"><span data-stu-id="0dc1f-155">Tutorials</span></span>

-   [<span data-ttu-id="0dc1f-156">X++ およびデバッガーの機能</span><span class="sxs-lookup"><span data-stu-id="0dc1f-156">X++ and debugger features</span></span>](new-x-debugger-features.md)
-   [<span data-ttu-id="0dc1f-157">C\# と X++ ソース コードを使用してビジネス ロジックを記述する</span><span class="sxs-lookup"><span data-stu-id="0dc1f-157">Write business logic by using C\# and X++ source code</span></span>](write-business-logic.md)

### <a name="language-support"></a><span data-ttu-id="0dc1f-158">言語サポート</span><span class="sxs-lookup"><span data-stu-id="0dc1f-158">Language support</span></span>

-   [<span data-ttu-id="0dc1f-159">X++ と X++ コンパイラの変更</span><span class="sxs-lookup"><span data-stu-id="0dc1f-159">Changes in X++ and the X++ compiler</span></span>](programming-language-support.md)
-   [<span data-ttu-id="0dc1f-160">要求または応答シナリオの EventHandlerResult クラス</span><span class="sxs-lookup"><span data-stu-id="0dc1f-160">EventHandlerResult classes in request or response scenarios</span></span>](event-handler-result-class.md)
-   [<span data-ttu-id="0dc1f-161">Visual Studioのデバッガーを使用して  X++ コードをデバッグする</span><span class="sxs-lookup"><span data-stu-id="0dc1f-161">Debug X++ code by using the debugger in Visual Studio</span></span>](debug-xpp.md)
-   <span data-ttu-id="0dc1f-162">C\#(linq-provider-c.md) 用の統合言語 クエリ (LINQ) プロバイダ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-162">[Language Integrated Query (LINQ) provider for C\#(linq-provider-c.md)</span></span>
-   [<span data-ttu-id="0dc1f-163">ベスト プラクティス ルールの記述</span><span class="sxs-lookup"><span data-stu-id="0dc1f-163">Write best practice rules</span></span>](author-best-practice-rules.md)

### <a name="reference"></a><span data-ttu-id="0dc1f-164">参照</span><span class="sxs-lookup"><span data-stu-id="0dc1f-164">Reference</span></span>

-   [<span data-ttu-id="0dc1f-165">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="0dc1f-165">X++ language reference</span></span>](../dev-ref/xpp-language-reference.md)

## <a name="customize-with-extensions-and-overlayering"></a><span data-ttu-id="0dc1f-166">拡張機能およびオーバーレイによってカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="0dc1f-166">Customize with extensions and overlayering</span></span>
- [<span data-ttu-id="0dc1f-167">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
- [<span data-ttu-id="0dc1f-168">拡張機能を使用してアプリケーション スイート レポートをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="0dc1f-168">Customize App Suite reports by using extensions</span></span>](../analytics/customize-app-suite-reports-with-extensions.md)

## <a name="code-migration"></a><span data-ttu-id="0dc1f-169">コードの移行</span><span class="sxs-lookup"><span data-stu-id="0dc1f-169">Code migration</span></span>
- [<span data-ttu-id="0dc1f-170">Visual Studio  での競合を解決する方法 (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="0dc1f-170">How to resolve conflicts in Visual Studio (video)</span></span>](https://youtu.be/4rxO0zUN2zU)
- [<span data-ttu-id="0dc1f-171">コードの移行とホーム ページのアップグレード</span><span class="sxs-lookup"><span data-stu-id="0dc1f-171">Code migration and upgrade home page</span></span>](../migration-upgrade/code-migration-home-page.md)

## <a name="move-packages-between-environments"></a><span data-ttu-id="0dc1f-172">環境間でパッケージを移動する</span><span class="sxs-lookup"><span data-stu-id="0dc1f-172">Move packages between environments</span></span>
- [<span data-ttu-id="0dc1f-173">配置可能なモデル パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="0dc1f-173">Create deployable packages of models</span></span>](../deployment/create-apply-deployable-package.md)

## <a name="performance"></a><span data-ttu-id="0dc1f-174">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="0dc1f-174">Performance</span></span>
- [<span data-ttu-id="0dc1f-175">Trace Parser を使用してトレースを実行</span><span class="sxs-lookup"><span data-stu-id="0dc1f-175">Take traces by using Trace parser</span></span>](../perf-test/trace-trace-tutorial.md)
- [<span data-ttu-id="0dc1f-176">Trace Parser を使用した問題点の診断およびパフォーマンスの分析</span><span class="sxs-lookup"><span data-stu-id="0dc1f-176">Diagnose issues and analyze performance by using Trace parser</span></span>](../perf-test/trace-parser.md)
- [<span data-ttu-id="0dc1f-177">パフォーマンス タイマー</span><span class="sxs-lookup"><span data-stu-id="0dc1f-177">Performance timer</span></span>](../perf-test/performance-timer.md)
<!-- [Expanding data with the Data Expansion tool (Office Mix)](https://mix.office.com/watch/11cet1u4nmn64)
- [Analyzing performance Issues with Trace Parser (Office Mix)](https://mix.office.com/watch/17d76cll0npyw)
- [The performance timer and other tools (Office Mix)](https://mix.office.com/watch/ij5cqidra5q3)
- [Using Task Recorder to create a single user performance test (Office Mix)](https://mix.office.com/watch/qtdlasy2rcf3)
- [The performance timer and other tools (Office Mix)](https://mix.office.com/watch/ij5cqidra5q3)
- [Analyzing performance Issues with Trace Parser (Office Mix)](https://mix.office.com/watch/17d76cll0npyw)-->

## <a name="user-interface-concepts"></a><span data-ttu-id="0dc1f-178">ユーザー インターフェイスのコンセプト</span><span class="sxs-lookup"><span data-stu-id="0dc1f-178">User interface concepts</span></span>
<span data-ttu-id="0dc1f-179">クライアントは、すべての主要なブラウザーで動作する HTML Web クライアントです。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-179">The client is an HTML web client that runs in all major browsers.</span></span> <span data-ttu-id="0dc1f-180">ユーザー インターフェイスの開発およびカスタマイズの詳細ついては、[ユーザー インターフェイス開発ホーム ページ](../user-interface/user-interface-development-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0dc1f-180">For information about developing and customizing the user interface, see the [User interface development home page](../user-interface/user-interface-development-home-page.md).</span></span>

## <a name="analytics"></a><span data-ttu-id="0dc1f-181">分析</span><span class="sxs-lookup"><span data-stu-id="0dc1f-181">Analytics</span></span>
- [<span data-ttu-id="0dc1f-182">分析、集計の測定、および KPI モデリング</span><span class="sxs-lookup"><span data-stu-id="0dc1f-182">Analytics, aggregate measurements, and KPI modeling</span></span>](../analytics/analytics.md)

## <a name="reporting-services"></a><span data-ttu-id="0dc1f-183">Reporting Services</span><span class="sxs-lookup"><span data-stu-id="0dc1f-183">Reporting services</span></span>
- [<span data-ttu-id="0dc1f-184">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="0dc1f-184">Electronic reporting (ER) overview</span></span>](../analytics/general-electronic-reporting.md)
<!-- [Introduction to Advanced Reporting Solutions (Office Mix)](https://mix.office.com/watch/wdl1dquy2tve)
- [Demo of Advanced Reporting Solutions (Office Mix)](https://mix.office.com/watch/1hkvtnc8sc7l6)-->

## <a name="data-entities-and-odata"></a><span data-ttu-id="0dc1f-185">データ エンティティおよび OData</span><span class="sxs-lookup"><span data-stu-id="0dc1f-185">Data entities and OData</span></span>
- [<span data-ttu-id="0dc1f-186">データ エンティティの概要</span><span class="sxs-lookup"><span data-stu-id="0dc1f-186">Data entities overview</span></span>](../data-entities/data-entities.md)
- [<span data-ttu-id="0dc1f-187">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="0dc1f-187">Open Data Protocol (OData)</span></span>](../data-entities/odata.md)

## <a name="testing-support-in-visual-studio"></a><span data-ttu-id="0dc1f-188">Visual Studio でのテストのサポート</span><span class="sxs-lookup"><span data-stu-id="0dc1f-188">Testing support in Visual Studio</span></span>
- [<span data-ttu-id="0dc1f-189">テストと検証</span><span class="sxs-lookup"><span data-stu-id="0dc1f-189">Testing and validations</span></span>](../perf-test/testing-validation.md)
- [<span data-ttu-id="0dc1f-190">Visual Studio のプロジェクトをテストする</span><span class="sxs-lookup"><span data-stu-id="0dc1f-190">Test projects in Visual Studio</span></span>](../perf-test/testing-support.md)
- [<span data-ttu-id="0dc1f-191">継続的ビルドとテストの自動化を使用した開発者トポロジの展開</span><span class="sxs-lookup"><span data-stu-id="0dc1f-191">Developer topology deployment with continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="0dc1f-192">タスク レコーダー リソース</span><span class="sxs-lookup"><span data-stu-id="0dc1f-192">Task recorder resources</span></span>](../user-interface/task-recorder.md)

## <a name="office-integration"></a><span data-ttu-id="0dc1f-193">Office 統合</span><span class="sxs-lookup"><span data-stu-id="0dc1f-193">Office integration</span></span>
- [<span data-ttu-id="0dc1f-194">Office 統合の概要</span><span class="sxs-lookup"><span data-stu-id="0dc1f-194">Office integration overview</span></span>](../office-integration/office-integration.md)

## <a name="intelligence"></a><span data-ttu-id="0dc1f-195">インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="0dc1f-195">Intelligence</span></span>
- [<span data-ttu-id="0dc1f-196">ビジネス インテリジェンス (BI) およびレポート作成のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-196">Business intelligence (BI) and reporting home page</span></span>](../analytics/bi-reporting-home-page.md)
<!-- [Overview of aggregate data (Office Mix)](https://mix.office.com/watch/16yvvnw45kzhf)-->

## <a name="mobile-platform"></a><span data-ttu-id="0dc1f-197">モバイル プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="0dc1f-197">Mobile platform</span></span>
- [<span data-ttu-id="0dc1f-198">モバイル プラットフォームのリソース</span><span class="sxs-lookup"><span data-stu-id="0dc1f-198">Mobile platform resources</span></span>](../mobile-apps/platform/mobile-platform-home-page.md)

## <a name="global-finance-management"></a><span data-ttu-id="0dc1f-199">グローバル財務管理</span><span class="sxs-lookup"><span data-stu-id="0dc1f-199">Global finance management</span></span>
- [<span data-ttu-id="0dc1f-200">財務開発のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="0dc1f-200">Financials development home page</span></span>](../financial/financial-dev-home-page.md)

## <a name="licensing"></a><span data-ttu-id="0dc1f-201">ライセンス</span><span class="sxs-lookup"><span data-stu-id="0dc1f-201">Licensing</span></span>
- [<span data-ttu-id="0dc1f-202">独立系ソフトウェア ベンダー (ISV) ライセンス</span><span class="sxs-lookup"><span data-stu-id="0dc1f-202">Independent software vendor (ISV) licensing</span></span>](isv-licensing.md)

## <a name="supply-chain-management"></a><span data-ttu-id="0dc1f-203">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="0dc1f-203">Supply Chain Management</span></span>
- [<span data-ttu-id="0dc1f-204">ガント コントロール作成ガイド</span><span class="sxs-lookup"><span data-stu-id="0dc1f-204">Gantt control development guide</span></span>](../user-interface/gantt-development-guide.md)
- [<span data-ttu-id="0dc1f-205">新しい輸送管理エンジンの作成</span><span class="sxs-lookup"><span data-stu-id="0dc1f-205">Create a new transportation management engine</span></span>](../../../supply-chain/transportation/create-new-transportation-management-engine.md)

## <a name="additional-resources"></a><span data-ttu-id="0dc1f-206">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="0dc1f-206">Additional resources</span></span>
[<span data-ttu-id="0dc1f-207">開発のための内部者向けヒント</span><span class="sxs-lookup"><span data-stu-id="0dc1f-207">Insider tips on development</span></span>](https://community.dynamics.com/ax/b/newdynamicsax)



