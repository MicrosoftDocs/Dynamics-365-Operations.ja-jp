---
title: "Visual Studio を使用して開発およびカスタマイズ"
description: "このトピックでは、開発に関するトピックへのリンクを提供します。"
author: RobinARH
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21631
ms.assetid: 06e26767-6056-4755-b47e-0bda71833581
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 8da9c54905ce017e043407ebad943d17ca3561a5
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="develop-and-customize-using-visual-studio"></a><span data-ttu-id="ee983-103">Visual Studio を使用して開発およびカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="ee983-103">Develop and customize using Visual Studio</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ee983-104">このトピックでは、開発に関するトピックへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="ee983-104">This topic provides links to topics about development.</span></span>

## <a name="overview"></a><span data-ttu-id="ee983-105">概要</span><span class="sxs-lookup"><span data-stu-id="ee983-105">Overview</span></span>

<span data-ttu-id="ee983-106">Microsoft Dynamics 365 for Finance and Operations は、Microsoft から提供されている次世代エンタープライズ リソース プランニング (ERP) を表します。</span><span class="sxs-lookup"><span data-stu-id="ee983-106">Microsoft Dynamics 365 for Finance and Operations represents the next-generation enterprise resource planning (ERP) offering from Microsoft.</span></span> <span data-ttu-id="ee983-107">これは、パブリック クラウドとプライベート クラウド両方のクラウド ベースのソリューションおよびオンプレミスとして、全体の ERP アプリケーション スイートを有効にするために設計されています。</span><span class="sxs-lookup"><span data-stu-id="ee983-107">It is designed to enable the entire ERP application suite as a cloud-based solution, for both public and private clouds, as well as on-premises.</span></span> <span data-ttu-id="ee983-108">これは、Microsoft からの最新テクノロジーで構築時に、クラウドでの操作の速度、わかりやすさ、およびコスト効率性を利用します。</span><span class="sxs-lookup"><span data-stu-id="ee983-108">It leverages the speed, simplicity, and cost-effectiveness of working in the cloud, while building on the latest technology from Microsoft.</span></span> <span data-ttu-id="ee983-109">このリリースでは、開発環境が大幅に変更されています。</span><span class="sxs-lookup"><span data-stu-id="ee983-109">This release introduces significant changes to the development experience.</span></span> <span data-ttu-id="ee983-110">これらの変更の内容は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="ee983-110">These changes include:</span></span>

- <span data-ttu-id="ee983-111">実行環境から切り離された開発ツール。</span><span class="sxs-lookup"><span data-stu-id="ee983-111">Development tools that are decoupled from any running environment.</span></span> <span data-ttu-id="ee983-112">オンライン データベースではなく、ローカルの XML ベースのファイルに対して作成します。</span><span class="sxs-lookup"><span data-stu-id="ee983-112">You develop against local, XML-based files, not the online database.</span></span>
- <span data-ttu-id="ee983-113">Microsoft Visual Studio は開発環境です。</span><span class="sxs-lookup"><span data-stu-id="ee983-113">Microsoft Visual Studio is the development environment.</span></span> <span data-ttu-id="ee983-114">Visual Studio 環境は、円滑で慣れ親しんだエクスペリエンスを提供するようにカスタマイズされています。</span><span class="sxs-lookup"><span data-stu-id="ee983-114">The Visual Studio environment is customized to provide you with a smooth and familiar experience.</span></span>
- <span data-ttu-id="ee983-115">X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。</span><span class="sxs-lookup"><span data-stu-id="ee983-115">The X++ compiler generates Common Intermediate Language (CIL) for all features.</span></span> <span data-ttu-id="ee983-116">CIL は C\# プログラミング言語などの他の .NET ベース (マネージド) の言語で使用されるものと同じ中間言語です。</span><span class="sxs-lookup"><span data-stu-id="ee983-116">CIL is the same intermediate language used by other .NET-based (managed) languages, such as the C\# programming language.</span></span>
- <span data-ttu-id="ee983-117">ブラウザー ベースのクライアントおよびフォームのデザイン パターンを活用して、改善されたエンド ユーザー エクスペリエンスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="ee983-117">You can leverage the browser-based client and the design patterns for forms to provide an improved end-user experience.</span></span>
- <span data-ttu-id="ee983-118">Application Lifecycle Model (ALM) は、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ee983-118">The Application Lifecycle Model (ALM) supports build automation, test automation, and deployment of models to the cloud.</span></span>

## <a name="architecture"></a><span data-ttu-id="ee983-119">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="ee983-119">Architecture</span></span>
-   [<span data-ttu-id="ee983-120">アプリケーション スタックおよびサーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="ee983-120">Application stack and server architecture</span></span>](application-stack-server-architecture.md)

## <a name="getting-started"></a><span data-ttu-id="ee983-121">はじめに</span><span class="sxs-lookup"><span data-stu-id="ee983-121">Getting started</span></span>
-   [<span data-ttu-id="ee983-122">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="ee983-122">Get an evaluation copy</span></span>](get-evaluation-copy.md)
-   [<span data-ttu-id="ee983-123">LCS101 – サブスクリプションのサインアップ</span><span class="sxs-lookup"><span data-stu-id="ee983-123">LCS101 – Sign up for a subscription</span></span>](sign-up-preview-subscription.md)
-   [<span data-ttu-id="ee983-124">開発インスタンスにアクセス</span><span class="sxs-lookup"><span data-stu-id="ee983-124">Access development instances</span></span>](../dev-tools/access-instances.md)
-   [<span data-ttu-id="ee983-125">開発システム要件</span><span class="sxs-lookup"><span data-stu-id="ee983-125">Development system requirements</span></span>](development-system-requirements.md)
-   [<span data-ttu-id="ee983-126">削除予定の機能</span><span class="sxs-lookup"><span data-stu-id="ee983-126">Deprecated features</span></span>](../migration-upgrade/deprecated-features.md)
-   [<span data-ttu-id="ee983-127">非推奨 API's</span><span class="sxs-lookup"><span data-stu-id="ee983-127">Deprecated API’s</span></span>](../migration-upgrade/deprecated-apis.md)
-   [<span data-ttu-id="ee983-128">フィードバックとサポート (Office Mix)</span><span class="sxs-lookup"><span data-stu-id="ee983-128">Feedback and support (Office Mix)</span></span>](https://mix.office.com/watch/92azzna59jj6)
-   [<span data-ttu-id="ee983-129">Visual Studio Team Services の名前を変更し、コンピューターを再起動する</span><span class="sxs-lookup"><span data-stu-id="ee983-129">Rename and reboot machines for Visual Studio Team Services</span></span>](../migration-upgrade/vso-machine-renaming.md)
-   [<span data-ttu-id="ee983-130">Visual Studio Team Services の概要 (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="ee983-130">Introduction to Visual Studio Team Services (Video)</span></span>](http://channel9.msdn.com/Events/Build/2014/2-575)

## <a name="fleet-management"></a><span data-ttu-id="ee983-131">フリート管理</span><span class="sxs-lookup"><span data-stu-id="ee983-131">Fleet Management</span></span>
-   [<span data-ttu-id="ee983-132">フリート管理のサンプル</span><span class="sxs-lookup"><span data-stu-id="ee983-132">Fleet Management sample</span></span>](introduction-fleet-management-sample.md)
-   [<span data-ttu-id="ee983-133">INT101: フリート管理の概要</span><span class="sxs-lookup"><span data-stu-id="ee983-133">INT101: Introduction to Fleet Management</span></span>](fleet-management-sample.md)

## <a name="development-tools"></a><span data-ttu-id="ee983-134">開発ツール</span><span class="sxs-lookup"><span data-stu-id="ee983-134">Development tools</span></span>
### <a name="tutorials"></a><span data-ttu-id="ee983-135">チュートリアル</span><span class="sxs-lookup"><span data-stu-id="ee983-135">Tutorials</span></span>

-   [<span data-ttu-id="ee983-136">Visual Studio 開発の概要</span><span class="sxs-lookup"><span data-stu-id="ee983-136">Introduction to Visual Studio development</span></span>](introduction-visual-studio.md)
-   [<span data-ttu-id="ee983-137">簡易データモデルを作成する</span><span class="sxs-lookup"><span data-stu-id="ee983-137">Create a simple data model</span></span>](create-data-model-elements.md)
-   [<span data-ttu-id="ee983-138">プロジェクトの構築およびデバッグ</span><span class="sxs-lookup"><span data-stu-id="ee983-138">Building and debugging a project</span></span>](build-debug-project.md)
-   [<span data-ttu-id="ee983-139">バージョン コントロール、メタデータ、検索、ナビゲーション、およびその他の機能</span><span class="sxs-lookup"><span data-stu-id="ee983-139">Version control, metadata search, navigation, and other features</span></span>](version-control-metadata-navigation.md)

### <a name="tools-models-and-vms"></a><span data-ttu-id="ee983-140">ツール、モデル、VM</span><span class="sxs-lookup"><span data-stu-id="ee983-140">Tools, models, and VMs</span></span>

-   [<span data-ttu-id="ee983-141">開発ツール</span><span class="sxs-lookup"><span data-stu-id="ee983-141">Development tools</span></span>](development-tools-overview.md)
-   [<span data-ttu-id="ee983-142">開発環境 (Office Mix) の概要</span><span class="sxs-lookup"><span data-stu-id="ee983-142">Introduction to the development environment (Office Mix)</span></span>](https://mix.office.com/watch/1tz7194y62m3s)
-   [<span data-ttu-id="ee983-143">アプリケーション エクスプローラー</span><span class="sxs-lookup"><span data-stu-id="ee983-143">Application Explorer</span></span>](application-explorer.md)
-   [<span data-ttu-id="ee983-144">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="ee983-144">Projects</span></span>](projects.md)
-   [<span data-ttu-id="ee983-145">要素デザイナー</span><span class="sxs-lookup"><span data-stu-id="ee983-145">Element designers</span></span>](element-designers.md)
-   [<span data-ttu-id="ee983-146">要素の利用状況</span><span class="sxs-lookup"><span data-stu-id="ee983-146">Element usage</span></span>](element-usage.md)
-   [<span data-ttu-id="ee983-147">モデル</span><span class="sxs-lookup"><span data-stu-id="ee983-147">Models</span></span>](models.md)
-   [<span data-ttu-id="ee983-148">ビルド操作</span><span class="sxs-lookup"><span data-stu-id="ee983-148">Build operations</span></span>](build-operations.md)
-   [<span data-ttu-id="ee983-149">Visual Studio コード エディター</span><span class="sxs-lookup"><span data-stu-id="ee983-149">Visual Studio code editor</span></span>](code-editor.md)
-   [<span data-ttu-id="ee983-150">開発者ツールのアドイン</span><span class="sxs-lookup"><span data-stu-id="ee983-150">Developer tools add-ins</span></span>](developer-tools-add-ins.md)
-   [<span data-ttu-id="ee983-151">VSTS (Office Mix) をバージョン管理を構成する</span><span class="sxs-lookup"><span data-stu-id="ee983-151">Configure version control with VSTS (Office Mix)</span></span>](https://mix.office.com/watch/1ftubtqzp3xxl)
-   [<span data-ttu-id="ee983-152">モデルの配分: モデルをエクスポートおよびインポートする方法</span><span class="sxs-lookup"><span data-stu-id="ee983-152">Distribution of models: How to export and import a model</span></span>](models-export-import.md)
-   [<span data-ttu-id="ee983-153">Visual Studio でのメタデータの検索</span><span class="sxs-lookup"><span data-stu-id="ee983-153">Metadata search in Visual Studio</span></span>](metadata-search-visual-studio.md)
-   [<span data-ttu-id="ee983-154">パッケージ、モデル、および Visual Studio (Office Mix) について学ぶ</span><span class="sxs-lookup"><span data-stu-id="ee983-154">Learn about packages, models and Visual Studio (Office Mix)</span></span>](https://mix.office.com/watch/ies6lyit6773)
-   [<span data-ttu-id="ee983-155">開発ツールのパフォーマンスのヒント (Office Mix)</span><span class="sxs-lookup"><span data-stu-id="ee983-155">Development tools performance tips (Office Mix)</span></span>](https://mix.office.com/watch/rnp6ng9wu8kx)
-   [<span data-ttu-id="ee983-156">Visual Studio を使用して競合を解決する</span><span class="sxs-lookup"><span data-stu-id="ee983-156">Resolve conflicts using Visual Studio</span></span>](https://mix.office.com/watch/1rl75ei2cs6d7)
-   [<span data-ttu-id="ee983-157">新しいユーザー アカウントを開発 VM で開発できるようにする</span><span class="sxs-lookup"><span data-stu-id="ee983-157">Enable a new user account to develop on a development VM</span></span>](enable-development-machine.md)
-   [<span data-ttu-id="ee983-158">Visual Studio 開発ツールの更新</span><span class="sxs-lookup"><span data-stu-id="ee983-158">Updating the Visual Studio development tools</span></span>](update-development-tools.md)

## <a name="x-programming-language"></a><span data-ttu-id="ee983-159">X++ プログラミング言語</span><span class="sxs-lookup"><span data-stu-id="ee983-159">X++ programming language</span></span>
### <a name="tutorials"></a><span data-ttu-id="ee983-160">チュートリアル</span><span class="sxs-lookup"><span data-stu-id="ee983-160">Tutorials</span></span>

-   [<span data-ttu-id="ee983-161">新しい X++ およびデバッガーの機能</span><span class="sxs-lookup"><span data-stu-id="ee983-161">New X++ and debugger features</span></span>](new-x-debugger-features.md)
-   [<span data-ttu-id="ee983-162">C\#、X++ 相互運用性およびLINQ</span><span class="sxs-lookup"><span data-stu-id="ee983-162">C\# and X++ interoperability and LINQ</span></span>](write-business-logic.md)

### <a name="language-support"></a><span data-ttu-id="ee983-163">言語サポート</span><span class="sxs-lookup"><span data-stu-id="ee983-163">Language support</span></span>

-   [<span data-ttu-id="ee983-164">プログラミング言語のサポート</span><span class="sxs-lookup"><span data-stu-id="ee983-164">Programming language support</span></span>](programming-language-support.md)
-   [<span data-ttu-id="ee983-165">要求または応答シナリオの EventHandlerResult クラス</span><span class="sxs-lookup"><span data-stu-id="ee983-165">EventHandlerResult classes in request or response scenarios</span></span>](event-handler-result-class.md)
-   [<span data-ttu-id="ee983-166">X++ コードのデバッグ</span><span class="sxs-lookup"><span data-stu-id="ee983-166">Debugging X++ code</span></span>](debug-xpp.md)
-   [<span data-ttu-id="ee983-167">C で使用する LINQ プロバイダー\#</span><span class="sxs-lookup"><span data-stu-id="ee983-167">LINQ provider for use in C\#</span></span>](linq-provider-c.md)
-   [<span data-ttu-id="ee983-168">ベスト プラクティス ルールの作成</span><span class="sxs-lookup"><span data-stu-id="ee983-168">Authoring best practice rules</span></span>](author-best-practice-rules.md)

### <a name="reference"></a><span data-ttu-id="ee983-169">参照</span><span class="sxs-lookup"><span data-stu-id="ee983-169">Reference</span></span>

-   [<span data-ttu-id="ee983-170">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="ee983-170">X++ language reference</span></span>](../dev-ref/xpp-language-reference.md)

## <a name="customize-with-extensions-and-overlayering"></a><span data-ttu-id="ee983-171">拡張機能およびオーバーレイによってカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="ee983-171">Customize with extensions and overlayering</span></span>
- [<span data-ttu-id="ee983-172">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="ee983-172">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
- [<span data-ttu-id="ee983-173">拡張機能を使用してアプリケーション スイート レポートをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="ee983-173">Customize App Suite reports using extensions</span></span>](../analytics/customize-app-suite-reports-with-extensions.md)

## <a name="code-migration"></a><span data-ttu-id="ee983-174">コードの移行</span><span class="sxs-lookup"><span data-stu-id="ee983-174">Code migration</span></span>
- [<span data-ttu-id="ee983-175">コードの移行とホーム ページのアップグレード</span><span class="sxs-lookup"><span data-stu-id="ee983-175">Code migration and upgrade home page</span></span>](../migration-upgrade/code-migration-home-page.md)

## <a name="move-packages-between-environments"></a><span data-ttu-id="ee983-176">環境間でパッケージを移動する</span><span class="sxs-lookup"><span data-stu-id="ee983-176">Move packages between environments</span></span>
- [<span data-ttu-id="ee983-177">配置可能なパッケージの作成と適用</span><span class="sxs-lookup"><span data-stu-id="ee983-177">Create and apply a deployable package</span></span>](../deployment/create-apply-deployable-package.md)

## <a name="performance"></a><span data-ttu-id="ee983-178">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="ee983-178">Performance</span></span>
- [<span data-ttu-id="ee983-179">Trace Parser でトレースを実行し、分析する</span><span class="sxs-lookup"><span data-stu-id="ee983-179">Take a trace with the Trace Parser and analyze it</span></span>](../perf-test/trace-trace-tutorial.md)
- [<span data-ttu-id="ee983-180">Visual Studio Online を使用した PerfSDK およびマルチユーザー テストの概要</span><span class="sxs-lookup"><span data-stu-id="ee983-180">Introduction to the PerfSDK and multiuser testing with Visual Studio Online</span></span>](../perf-test/perfsdk-tutorial.md)
- [<span data-ttu-id="ee983-181">問題点の診断およびパフォーマンス問題の分析にTrace Parser のデスクトップ バージョンを使用する</span><span class="sxs-lookup"><span data-stu-id="ee983-181">Using the desktop version of trace parser to diagnose problems and analyze performance issues</span></span>](../perf-test/trace-parser.md)
- [<span data-ttu-id="ee983-182">パフォーマンス タイマー</span><span class="sxs-lookup"><span data-stu-id="ee983-182">Performance timer</span></span>](../perf-test/performance-timer.md)
- [<span data-ttu-id="ee983-183">データ拡張ツール (Office Mix) を使用してデータを展開する</span><span class="sxs-lookup"><span data-stu-id="ee983-183">Expanding data with the Data Expansion tool (Office Mix)</span></span>](https://mix.office.com/watch/11cet1u4nmn64)
- [<span data-ttu-id="ee983-184">Trace Parser (Office Mix) パフォーマンスの問題の分析</span><span class="sxs-lookup"><span data-stu-id="ee983-184">Analyzing performance Issues with Trace Parser (Office Mix)</span></span>](https://mix.office.com/watch/17d76cll0npyw)
- [<span data-ttu-id="ee983-185">パフォーマンス タイマーおよびその他のツール (Office Mix)</span><span class="sxs-lookup"><span data-stu-id="ee983-185">The performance timer and other tools (Office Mix)</span></span>](https://mix.office.com/watch/ij5cqidra5q3)
- [<span data-ttu-id="ee983-186">タスク レコーダーを使用して、単一のユーザー パフォーマンス テスト (Office Mix) を作成する</span><span class="sxs-lookup"><span data-stu-id="ee983-186">Using Task Recorder to create a single user performance test (Office Mix)</span></span>](https://mix.office.com/watch/qtdlasy2rcf3)
- [<span data-ttu-id="ee983-187">パフォーマンス タイマーおよびその他のツール (Office Mix)</span><span class="sxs-lookup"><span data-stu-id="ee983-187">The performance timer and other tools (Office Mix)</span></span>](https://mix.office.com/watch/ij5cqidra5q3)
- [<span data-ttu-id="ee983-188">Trace Parser (Office Mix) パフォーマンスの問題の分析</span><span class="sxs-lookup"><span data-stu-id="ee983-188">Analyzing performance Issues with Trace Parser (Office Mix)</span></span>](https://mix.office.com/watch/17d76cll0npyw)

## <a name="user-interface-concepts"></a><span data-ttu-id="ee983-189">ユーザー インターフェイスのコンセプト</span><span class="sxs-lookup"><span data-stu-id="ee983-189">User interface concepts</span></span>
<span data-ttu-id="ee983-190">クライアントは、すべての主要なブラウザーで動作する HTML Web クライアントです。</span><span class="sxs-lookup"><span data-stu-id="ee983-190">The client is an HTML web client that runs in all major browsers.</span></span> <span data-ttu-id="ee983-191">ユーザー インターフェイスの開発およびカスタマイズの詳細ついては、[ユーザー インターフェイス開発ホーム ページ](../user-interface/user-interface-development-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee983-191">For information about developing and customizing the user interface, see the [User interface development home page](../user-interface/user-interface-development-home-page.md).</span></span>

## <a name="analytics"></a><span data-ttu-id="ee983-192">分析</span><span class="sxs-lookup"><span data-stu-id="ee983-192">Analytics</span></span>
- [<span data-ttu-id="ee983-193">分析</span><span class="sxs-lookup"><span data-stu-id="ee983-193">Analytics</span></span>](../analytics/analytics.md)

## <a name="reporting-services"></a><span data-ttu-id="ee983-194">Reporting Services</span><span class="sxs-lookup"><span data-stu-id="ee983-194">Reporting services</span></span>
- [<span data-ttu-id="ee983-195">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="ee983-195">Electronic reporting overview</span></span>](../analytics/general-electronic-reporting.md)
- [<span data-ttu-id="ee983-196">詳細なレポート ソリューション (Office Mix) の概要</span><span class="sxs-lookup"><span data-stu-id="ee983-196">Introduction to Advanced Reporting Solutions (Office Mix)</span></span>](https://mix.office.com/watch/wdl1dquy2tve)
- [<span data-ttu-id="ee983-197">詳細なレポート作成ソリューション (Office Mix) のデモ</span><span class="sxs-lookup"><span data-stu-id="ee983-197">Demo of Advanced Reporting Solutions (Office Mix)</span></span>](https://mix.office.com/watch/1hkvtnc8sc7l6)

## <a name="data-entities-and-odata"></a><span data-ttu-id="ee983-198">データ エンティティおよび OData</span><span class="sxs-lookup"><span data-stu-id="ee983-198">Data entities and OData</span></span>
- [<span data-ttu-id="ee983-199">データ エンティティのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="ee983-199">Data entities home page</span></span>](../data-entities/data-entities.md)
- [<span data-ttu-id="ee983-200">OData</span><span class="sxs-lookup"><span data-stu-id="ee983-200">OData</span></span>](../data-entities/odata.md)

## <a name="testing-support-in-visual-studio"></a><span data-ttu-id="ee983-201">Visual Studio でのテストのサポート</span><span class="sxs-lookup"><span data-stu-id="ee983-201">Testing support in Visual Studio</span></span>
- [<span data-ttu-id="ee983-202">テストと検証</span><span class="sxs-lookup"><span data-stu-id="ee983-202">Testing and validation</span></span>](../perf-test/testing-validation.md)
- [<span data-ttu-id="ee983-203">Visual Studio でのテストのサポート</span><span class="sxs-lookup"><span data-stu-id="ee983-203">Support for testing in Visual Studio</span></span>](../perf-test/testing-support.md)
- [<span data-ttu-id="ee983-204">継続的なビルドとテストの自動化による開発者トポロジの配置</span><span class="sxs-lookup"><span data-stu-id="ee983-204">Developer topology deployment with continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="ee983-205">タスク レコーダー</span><span class="sxs-lookup"><span data-stu-id="ee983-205">Task Recorder</span></span>](../user-interface/task-recorder.md)

## <a name="office-integration"></a><span data-ttu-id="ee983-206">Office 統合</span><span class="sxs-lookup"><span data-stu-id="ee983-206">Office integration</span></span>
- [<span data-ttu-id="ee983-207">Office 統合</span><span class="sxs-lookup"><span data-stu-id="ee983-207">Office integration</span></span>](../office-integration/office-integration.md)

## <a name="intelligence"></a><span data-ttu-id="ee983-208">インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="ee983-208">Intelligence</span></span>
- [<span data-ttu-id="ee983-209">インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="ee983-209">Intelligence</span></span>](../analytics/bi-reporting-home-page.md)
- [<span data-ttu-id="ee983-210">集計データ (Office Mix) の概要</span><span class="sxs-lookup"><span data-stu-id="ee983-210">Overview of aggregate data (Office Mix)</span></span>](https://mix.office.com/watch/16yvvnw45kzhf)

## <a name="mobile-platform"></a><span data-ttu-id="ee983-211">モバイル プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="ee983-211">Mobile platform</span></span>
- [<span data-ttu-id="ee983-212">モバイル プラットフォームのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="ee983-212">Mobile platform home page</span></span>](../mobile-apps/platform/mobile-platform-home-page.md)

## <a name="global-finance-management"></a><span data-ttu-id="ee983-213">グローバル財務管理</span><span class="sxs-lookup"><span data-stu-id="ee983-213">Global finance management</span></span>
- [<span data-ttu-id="ee983-214">財務開発ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="ee983-214">Financials development home page</span></span>](../financial/financial-dev-home-page.md)

## <a name="licensing"></a><span data-ttu-id="ee983-215">ライセンス</span><span class="sxs-lookup"><span data-stu-id="ee983-215">Licensing</span></span>
- [<span data-ttu-id="ee983-216">ISV ライセンス</span><span class="sxs-lookup"><span data-stu-id="ee983-216">ISV licensing</span></span>](isv-licensing.md)

## <a name="supply-chain-management"></a><span data-ttu-id="ee983-217">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="ee983-217">Supply chain management</span></span>
- [<span data-ttu-id="ee983-218">ガント作成ガイド</span><span class="sxs-lookup"><span data-stu-id="ee983-218">Gantt development guide</span></span>](../user-interface/gantt-development-guide.md)
- [<span data-ttu-id="ee983-219">新しい輸送管理エンジンの作成</span><span class="sxs-lookup"><span data-stu-id="ee983-219">Create a new transportation management engine</span></span>](../../supply-chain/transportation/create-new-transportation-management-engine.md)

## <a name="additional-resources"></a><span data-ttu-id="ee983-220">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="ee983-220">Additional resources</span></span>
[<span data-ttu-id="ee983-221">開発のための内部者向けヒント</span><span class="sxs-lookup"><span data-stu-id="ee983-221">Insider tips on development</span></span>](https://community.dynamics.com/ax/b/newdynamicsax)




