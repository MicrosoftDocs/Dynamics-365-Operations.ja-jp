---
title: 開発およびカスタマイズ
description: このトピックでは、開発に関するトピックへのリンクを提供します。
author: RobinARH
manager: AnnBe
ms.date: 04/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21631
ms.assetid: 06e26767-6056-4755-b47e-0bda71833581
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0de1e48aa9fbabdcd711aabded726066f9e341b1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369469"
---
# <a name="develop-and-customize"></a><span data-ttu-id="73bb2-103">開発およびカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="73bb2-103">Develop and customize</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73bb2-104">このトピックでは、開発に関するトピックへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-104">This topic provides links to topics about development.</span></span>

## <a name="overview"></a><span data-ttu-id="73bb2-105">概要</span><span class="sxs-lookup"><span data-stu-id="73bb2-105">Overview</span></span>

<span data-ttu-id="73bb2-106">Microsoft Dynamics 365 for Finance and Operations は、Microsoft から提供された次世代エンタープライズ リソース プランニング (ERP) を表します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-106">Microsoft Dynamics 365 for Finance and Operations represents the next-generation enterprise resource planning (ERP) offering from Microsoft.</span></span> <span data-ttu-id="73bb2-107">これは、パブリック クラウドとプライベート クラウド両方のクラウド ベースのソリューションおよびオンプレミスとして、全体の ERP アプリケーション スイートを有効にするために設計されています。</span><span class="sxs-lookup"><span data-stu-id="73bb2-107">It is designed to enable the entire ERP application suite as a cloud-based solution, for both public and private clouds, as well as on-premises.</span></span> <span data-ttu-id="73bb2-108">これは、Microsoft からの最新テクノロジーで構築時に、クラウドでの操作の速度、わかりやすさ、およびコスト効率性を利用します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-108">It leverages the speed, simplicity, and cost-effectiveness of working in the cloud, while building on the latest technology from Microsoft.</span></span> <span data-ttu-id="73bb2-109">このリリースでは、開発環境が大幅に変更されています。</span><span class="sxs-lookup"><span data-stu-id="73bb2-109">This release introduces significant changes to the development experience.</span></span> <span data-ttu-id="73bb2-110">これらの変更の内容は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="73bb2-110">These changes include:</span></span>

- <span data-ttu-id="73bb2-111">実行環境から切り離された開発ツール。</span><span class="sxs-lookup"><span data-stu-id="73bb2-111">Development tools that are decoupled from any running environment.</span></span> <span data-ttu-id="73bb2-112">オンライン データベースではなく、ローカルの XML ベースのファイルに対して作成します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-112">You develop against local, XML-based files, not the online database.</span></span>
- <span data-ttu-id="73bb2-113">Microsoft Visual Studio が開発環境です。</span><span class="sxs-lookup"><span data-stu-id="73bb2-113">Microsoft Visual Studio is the development environment.</span></span> <span data-ttu-id="73bb2-114">Visual Studio 環境は、円滑で慣れ親しんだエクスペリエンスを提供するようにカスタマイズされています。</span><span class="sxs-lookup"><span data-stu-id="73bb2-114">The Visual Studio environment is customized to provide you with a smooth and familiar experience.</span></span>
- <span data-ttu-id="73bb2-115">X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-115">The X++ compiler generates Common Intermediate Language (CIL) for all features.</span></span> <span data-ttu-id="73bb2-116">CIL は C\# プログラミング言語などの他の .NET ベース (マネージド) の言語で使用されるものと同じ中間言語です。</span><span class="sxs-lookup"><span data-stu-id="73bb2-116">CIL is the same intermediate language used by other .NET-based (managed) languages, such as the C\# programming language.</span></span>
- <span data-ttu-id="73bb2-117">ブラウザー ベースのクライアントおよびフォームのデザイン パターンを活用して、改善されたエンド ユーザー エクスペリエンスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="73bb2-117">You can leverage the browser-based client and the design patterns for forms to provide an improved end-user experience.</span></span>
- <span data-ttu-id="73bb2-118">Application Lifecycle Model (ALM) は、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-118">The Application Lifecycle Model (ALM) supports build automation, test automation, and deployment of models to the cloud.</span></span>

## <a name="architecture"></a><span data-ttu-id="73bb2-119">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="73bb2-119">Architecture</span></span>
-   [<span data-ttu-id="73bb2-120">アプリケーション スタックおよびサーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="73bb2-120">Application stack and server architecture</span></span>](application-stack-server-architecture.md)

## <a name="getting-started"></a><span data-ttu-id="73bb2-121">はじめに</span><span class="sxs-lookup"><span data-stu-id="73bb2-121">Getting started</span></span>
-   [<span data-ttu-id="73bb2-122">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="73bb2-122">Get an evaluation copy</span></span>](get-evaluation-copy.md)
-   [<span data-ttu-id="73bb2-123">LCS101 – サブスクリプションのサインアップ</span><span class="sxs-lookup"><span data-stu-id="73bb2-123">LCS101 – Sign up for a subscription</span></span>](sign-up-preview-subscription.md)
-   [<span data-ttu-id="73bb2-124">開発インスタンスにアクセス</span><span class="sxs-lookup"><span data-stu-id="73bb2-124">Access development instances</span></span>](../dev-tools/access-instances.md)
-   [<span data-ttu-id="73bb2-125">開発システム要件</span><span class="sxs-lookup"><span data-stu-id="73bb2-125">Development system requirements</span></span>](development-system-requirements.md)
-   [<span data-ttu-id="73bb2-126">削除予定の機能</span><span class="sxs-lookup"><span data-stu-id="73bb2-126">Deprecated features</span></span>](../migration-upgrade/deprecated-features.md)
-   [<span data-ttu-id="73bb2-127">非推奨 API's</span><span class="sxs-lookup"><span data-stu-id="73bb2-127">Deprecated API’s</span></span>](../migration-upgrade/deprecated-apis.md)
-   [<span data-ttu-id="73bb2-128">Azure DevOps の名前を変更し、コンピューターを再起動する</span><span class="sxs-lookup"><span data-stu-id="73bb2-128">Rename and reboot machines for Azure DevOps</span></span>](../migration-upgrade/vso-machine-renaming.md)
-   <span data-ttu-id="73bb2-129">[Azure DevOps の概要 (ビデオ)](http://channel9.msdn.com/Events/Build/2014/2-575)
<!-- [Learn about packages, models and Visual Studio (Office Mix)](https://mix.office.com/watch/ies6lyit6773)-->
<!-- [Development tools performance tips (Office Mix)](https://mix.office.com/watch/rnp6ng9wu8kx)-->
<!-- [Feedback and support (Office Mix)](https://mix.office.com/watch/92azzna59jj6)--></span><span class="sxs-lookup"><span data-stu-id="73bb2-129">[Introduction to Azure DevOps (Video)](http://channel9.msdn.com/Events/Build/2014/2-575)
<!-- [Learn about packages, models and Visual Studio (Office Mix)](https://mix.office.com/watch/ies6lyit6773)-->
<!-- [Development tools performance tips (Office Mix)](https://mix.office.com/watch/rnp6ng9wu8kx)-->
<!-- [Feedback and support (Office Mix)](https://mix.office.com/watch/92azzna59jj6)--></span></span>

## <a name="fleet-management"></a><span data-ttu-id="73bb2-130">フリート管理</span><span class="sxs-lookup"><span data-stu-id="73bb2-130">Fleet Management</span></span>
-   [<span data-ttu-id="73bb2-131">フリート管理のサンプル</span><span class="sxs-lookup"><span data-stu-id="73bb2-131">Fleet Management sample</span></span>](introduction-fleet-management-sample.md)
-   [<span data-ttu-id="73bb2-132">INT101: フリート管理の概要</span><span class="sxs-lookup"><span data-stu-id="73bb2-132">INT101: Introduction to Fleet Management</span></span>](fleet-management-sample.md)

## <a name="development-tools"></a><span data-ttu-id="73bb2-133">開発ツール</span><span class="sxs-lookup"><span data-stu-id="73bb2-133">Development tools</span></span>
### <a name="tutorials"></a><span data-ttu-id="73bb2-134">チュートリアル</span><span class="sxs-lookup"><span data-stu-id="73bb2-134">Tutorials</span></span>

-   [<span data-ttu-id="73bb2-135">Visual Studio での開発の紹介</span><span class="sxs-lookup"><span data-stu-id="73bb2-135">Introduction to Visual Studio development</span></span>](introduction-visual-studio.md)
-   [<span data-ttu-id="73bb2-136">簡易データモデルを作成する</span><span class="sxs-lookup"><span data-stu-id="73bb2-136">Create a simple data model</span></span>](create-data-model-elements.md)
-   [<span data-ttu-id="73bb2-137">プロジェクトの構築およびデバッグ</span><span class="sxs-lookup"><span data-stu-id="73bb2-137">Building and debugging a project</span></span>](build-debug-project.md)
-   [<span data-ttu-id="73bb2-138">バージョン コントロール、メタデータ、検索、ナビゲーション、およびその他の機能</span><span class="sxs-lookup"><span data-stu-id="73bb2-138">Version control, metadata search, navigation, and other features</span></span>](version-control-metadata-navigation.md)

### <a name="tools-models-and-vms"></a><span data-ttu-id="73bb2-139">ツール、モデル、VM</span><span class="sxs-lookup"><span data-stu-id="73bb2-139">Tools, models, and VMs</span></span>

-   <span data-ttu-id="73bb2-140">[開発ツール](development-tools-overview.md)
<!-- [Introduction to the development environment (Office Mix)](https://mix.office.com/watch/1tz7194y62m3s)--></span><span class="sxs-lookup"><span data-stu-id="73bb2-140">[Development tools](development-tools-overview.md)
<!-- [Introduction to the development environment (Office Mix)](https://mix.office.com/watch/1tz7194y62m3s)--></span></span>
-   [<span data-ttu-id="73bb2-141">アプリケーション エクスプローラー</span><span class="sxs-lookup"><span data-stu-id="73bb2-141">Application Explorer</span></span>](application-explorer.md)
-   [<span data-ttu-id="73bb2-142">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="73bb2-142">Projects</span></span>](projects.md)
-   [<span data-ttu-id="73bb2-143">要素デザイナー</span><span class="sxs-lookup"><span data-stu-id="73bb2-143">Element designers</span></span>](element-designers.md)
-   [<span data-ttu-id="73bb2-144">要素の利用状況</span><span class="sxs-lookup"><span data-stu-id="73bb2-144">Element usage</span></span>](element-usage.md)
-   [<span data-ttu-id="73bb2-145">モデル</span><span class="sxs-lookup"><span data-stu-id="73bb2-145">Models</span></span>](models.md)
-   [<span data-ttu-id="73bb2-146">ビルド操作</span><span class="sxs-lookup"><span data-stu-id="73bb2-146">Build operations</span></span>](build-operations.md)
-   [<span data-ttu-id="73bb2-147">Visual Studioコード エディター</span><span class="sxs-lookup"><span data-stu-id="73bb2-147">Visual Studio code editor</span></span>](code-editor.md)
-   [<span data-ttu-id="73bb2-148">開発者ツールのアドイン</span><span class="sxs-lookup"><span data-stu-id="73bb2-148">Developer tools add-ins</span></span>](developer-tools-add-ins.md)
-   [<span data-ttu-id="73bb2-149">モデルの配分: モデルをエクスポートおよびインポートする方法</span><span class="sxs-lookup"><span data-stu-id="73bb2-149">Distribution of models: How to export and import a model</span></span>](models-export-import.md)
-   [<span data-ttu-id="73bb2-150">Visual Studio でのメタデータの検索</span><span class="sxs-lookup"><span data-stu-id="73bb2-150">Metadata search in Visual Studio</span></span>](metadata-search-visual-studio.md)
-   [<span data-ttu-id="73bb2-151">Visual Studio を使用して競合を解決する</span><span class="sxs-lookup"><span data-stu-id="73bb2-151">Resolve conflicts using Visual Studio</span></span>](https://mix.office.com/watch/1rl75ei2cs6d7)
-   [<span data-ttu-id="73bb2-152">新しいユーザー アカウントを開発 VM で開発できるようにする</span><span class="sxs-lookup"><span data-stu-id="73bb2-152">Enable a new user account to develop on a development VM</span></span>](enable-development-machine.md)
-   [<span data-ttu-id="73bb2-153">Visual Studio 開発ツールの更新</span><span class="sxs-lookup"><span data-stu-id="73bb2-153">Updating the Visual Studio development tools</span></span>](update-development-tools.md)
-   <span data-ttu-id="73bb2-154">[管理者のアクセスを許可しない仮想マシンに関するよく寄せられる質問](../sysadmin/VMs-no-admin-access.md)
<!--  [Configure version control with Azure DevOps (Office Mix)](https://mix.office.com/watch/1ftubtqzp3xxl)--></span><span class="sxs-lookup"><span data-stu-id="73bb2-154">[Virtual machines that don't allow administrator access FAQ](../sysadmin/VMs-no-admin-access.md)
<!--  [Configure version control with Azure DevOps (Office Mix)](https://mix.office.com/watch/1ftubtqzp3xxl)--></span></span>

## <a name="x-programming-language"></a><span data-ttu-id="73bb2-155">X++ プログラミング言語</span><span class="sxs-lookup"><span data-stu-id="73bb2-155">X++ programming language</span></span>
### <a name="tutorials"></a><span data-ttu-id="73bb2-156">チュートリアル</span><span class="sxs-lookup"><span data-stu-id="73bb2-156">Tutorials</span></span>

-   [<span data-ttu-id="73bb2-157">新しい X++ およびデバッガーの機能</span><span class="sxs-lookup"><span data-stu-id="73bb2-157">New X++ and debugger features</span></span>](new-x-debugger-features.md)
-   [<span data-ttu-id="73bb2-158">C\#、X++ 相互運用性およびLINQ</span><span class="sxs-lookup"><span data-stu-id="73bb2-158">C\# and X++ interoperability and LINQ</span></span>](write-business-logic.md)

### <a name="language-support"></a><span data-ttu-id="73bb2-159">言語サポート</span><span class="sxs-lookup"><span data-stu-id="73bb2-159">Language support</span></span>

-   [<span data-ttu-id="73bb2-160">プログラミング言語のサポート</span><span class="sxs-lookup"><span data-stu-id="73bb2-160">Programming language support</span></span>](programming-language-support.md)
-   [<span data-ttu-id="73bb2-161">要求または応答シナリオの EventHandlerResult クラス</span><span class="sxs-lookup"><span data-stu-id="73bb2-161">EventHandlerResult classes in request or response scenarios</span></span>](event-handler-result-class.md)
-   [<span data-ttu-id="73bb2-162">X++ コードのデバッグ</span><span class="sxs-lookup"><span data-stu-id="73bb2-162">Debugging X++ code</span></span>](debug-xpp.md)
-   [<span data-ttu-id="73bb2-163">C で使用する LINQ プロバイダー\#</span><span class="sxs-lookup"><span data-stu-id="73bb2-163">LINQ provider for use in C\#</span></span>](linq-provider-c.md)
-   [<span data-ttu-id="73bb2-164">ベスト プラクティス ルールの作成</span><span class="sxs-lookup"><span data-stu-id="73bb2-164">Authoring best practice rules</span></span>](author-best-practice-rules.md)

### <a name="reference"></a><span data-ttu-id="73bb2-165">参照</span><span class="sxs-lookup"><span data-stu-id="73bb2-165">Reference</span></span>

-   [<span data-ttu-id="73bb2-166">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="73bb2-166">X++ language reference</span></span>](../dev-ref/xpp-language-reference.md)

## <a name="customize-with-extensions-and-overlayering"></a><span data-ttu-id="73bb2-167">拡張機能およびオーバーレイによってカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="73bb2-167">Customize with extensions and overlayering</span></span>
- [<span data-ttu-id="73bb2-168">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="73bb2-168">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
- [<span data-ttu-id="73bb2-169">拡張機能を使用してアプリケーション スイート レポートをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="73bb2-169">Customize App Suite reports using extensions</span></span>](../analytics/customize-app-suite-reports-with-extensions.md)

## <a name="code-migration"></a><span data-ttu-id="73bb2-170">コードの移行</span><span class="sxs-lookup"><span data-stu-id="73bb2-170">Code migration</span></span>
- [<span data-ttu-id="73bb2-171">コードの移行とホーム ページのアップグレード</span><span class="sxs-lookup"><span data-stu-id="73bb2-171">Code migration and upgrade home page</span></span>](../migration-upgrade/code-migration-home-page.md)

## <a name="move-packages-between-environments"></a><span data-ttu-id="73bb2-172">環境間でパッケージを移動する</span><span class="sxs-lookup"><span data-stu-id="73bb2-172">Move packages between environments</span></span>
- [<span data-ttu-id="73bb2-173">配置可能なパッケージの作成と適用</span><span class="sxs-lookup"><span data-stu-id="73bb2-173">Create and apply a deployable package</span></span>](../deployment/create-apply-deployable-package.md)

## <a name="performance"></a><span data-ttu-id="73bb2-174">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="73bb2-174">Performance</span></span>
- [<span data-ttu-id="73bb2-175">Trace Parser でトレースを実行し、分析する</span><span class="sxs-lookup"><span data-stu-id="73bb2-175">Take a trace with the Trace Parser and analyze it</span></span>](../perf-test/trace-trace-tutorial.md)
- [<span data-ttu-id="73bb2-176">PerfSDK および Visual Studio Online によるマルチ ユーザー テストの概要</span><span class="sxs-lookup"><span data-stu-id="73bb2-176">Introduction to the PerfSDK and multiuser testing with Visual Studio Online</span></span>](../perf-test/perfsdk-tutorial.md)
- [<span data-ttu-id="73bb2-177">問題点の診断およびパフォーマンス問題の分析にTrace Parser のデスクトップ バージョンを使用する</span><span class="sxs-lookup"><span data-stu-id="73bb2-177">Using the desktop version of trace parser to diagnose problems and analyze performance issues</span></span>](../perf-test/trace-parser.md)
- [<span data-ttu-id="73bb2-178">パフォーマンス タイマー</span><span class="sxs-lookup"><span data-stu-id="73bb2-178">Performance timer</span></span>](../perf-test/performance-timer.md)
<!-- [Expanding data with the Data Expansion tool (Office Mix)](https://mix.office.com/watch/11cet1u4nmn64)
- [Analyzing performance Issues with Trace Parser (Office Mix)](https://mix.office.com/watch/17d76cll0npyw)
- [The performance timer and other tools (Office Mix)](https://mix.office.com/watch/ij5cqidra5q3)
- [Using Task Recorder to create a single user performance test (Office Mix)](https://mix.office.com/watch/qtdlasy2rcf3)
- [The performance timer and other tools (Office Mix)](https://mix.office.com/watch/ij5cqidra5q3)
- [Analyzing performance Issues with Trace Parser (Office Mix)](https://mix.office.com/watch/17d76cll0npyw)-->

## <a name="user-interface-concepts"></a><span data-ttu-id="73bb2-179">ユーザー インターフェイスのコンセプト</span><span class="sxs-lookup"><span data-stu-id="73bb2-179">User interface concepts</span></span>
<span data-ttu-id="73bb2-180">クライアントは、すべての主要なブラウザーで動作する HTML Web クライアントです。</span><span class="sxs-lookup"><span data-stu-id="73bb2-180">The client is an HTML web client that runs in all major browsers.</span></span> <span data-ttu-id="73bb2-181">ユーザー インターフェイスの開発およびカスタマイズの詳細ついては、[ユーザー インターフェイス開発ホーム ページ](../user-interface/user-interface-development-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73bb2-181">For information about developing and customizing the user interface, see the [User interface development home page](../user-interface/user-interface-development-home-page.md).</span></span>

## <a name="analytics"></a><span data-ttu-id="73bb2-182">分析</span><span class="sxs-lookup"><span data-stu-id="73bb2-182">Analytics</span></span>
- [<span data-ttu-id="73bb2-183">分析</span><span class="sxs-lookup"><span data-stu-id="73bb2-183">Analytics</span></span>](../analytics/analytics.md)

## <a name="reporting-services"></a><span data-ttu-id="73bb2-184">Reporting Services</span><span class="sxs-lookup"><span data-stu-id="73bb2-184">Reporting services</span></span>
- [<span data-ttu-id="73bb2-185">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="73bb2-185">Electronic reporting overview</span></span>](../analytics/general-electronic-reporting.md)
<!-- [Introduction to Advanced Reporting Solutions (Office Mix)](https://mix.office.com/watch/wdl1dquy2tve)
- [Demo of Advanced Reporting Solutions (Office Mix)](https://mix.office.com/watch/1hkvtnc8sc7l6)-->

## <a name="data-entities-and-odata"></a><span data-ttu-id="73bb2-186">データ エンティティおよび OData</span><span class="sxs-lookup"><span data-stu-id="73bb2-186">Data entities and OData</span></span>
- [<span data-ttu-id="73bb2-187">データ エンティティのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="73bb2-187">Data entities home page</span></span>](../data-entities/data-entities.md)
- [<span data-ttu-id="73bb2-188">OData</span><span class="sxs-lookup"><span data-stu-id="73bb2-188">OData</span></span>](../data-entities/odata.md)

## <a name="testing-support-in-visual-studio"></a><span data-ttu-id="73bb2-189">Visual Studio でのテストのサポート</span><span class="sxs-lookup"><span data-stu-id="73bb2-189">Testing support in Visual Studio</span></span>
- [<span data-ttu-id="73bb2-190">テストと検証</span><span class="sxs-lookup"><span data-stu-id="73bb2-190">Testing and validation</span></span>](../perf-test/testing-validation.md)
- [<span data-ttu-id="73bb2-191">Visual Studio でのテストのサポート</span><span class="sxs-lookup"><span data-stu-id="73bb2-191">Support for testing in Visual Studio</span></span>](../perf-test/testing-support.md)
- [<span data-ttu-id="73bb2-192">継続的ビルドとテストの自動化を使用した開発者トポロジの展開</span><span class="sxs-lookup"><span data-stu-id="73bb2-192">Developer topology deployment with continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="73bb2-193">タスク レコーダー</span><span class="sxs-lookup"><span data-stu-id="73bb2-193">Task Recorder</span></span>](../user-interface/task-recorder.md)

## <a name="office-integration"></a><span data-ttu-id="73bb2-194">Office 統合</span><span class="sxs-lookup"><span data-stu-id="73bb2-194">Office integration</span></span>
- [<span data-ttu-id="73bb2-195">Office 統合</span><span class="sxs-lookup"><span data-stu-id="73bb2-195">Office integration</span></span>](../office-integration/office-integration.md)

## <a name="intelligence"></a><span data-ttu-id="73bb2-196">インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="73bb2-196">Intelligence</span></span>
- <span data-ttu-id="73bb2-197">[インテリジェンス](../analytics/bi-reporting-home-page.md)
<!-- [Overview of aggregate data (Office Mix)](https://mix.office.com/watch/16yvvnw45kzhf)--></span><span class="sxs-lookup"><span data-stu-id="73bb2-197">[Intelligence](../analytics/bi-reporting-home-page.md)
<!-- [Overview of aggregate data (Office Mix)](https://mix.office.com/watch/16yvvnw45kzhf)--></span></span>

## <a name="mobile-platform"></a><span data-ttu-id="73bb2-198">モバイル プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="73bb2-198">Mobile platform</span></span>
- [<span data-ttu-id="73bb2-199">モバイル プラットフォームのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="73bb2-199">Mobile platform home page</span></span>](../mobile-apps/platform/mobile-platform-home-page.md)

## <a name="global-finance-management"></a><span data-ttu-id="73bb2-200">グローバル財務管理</span><span class="sxs-lookup"><span data-stu-id="73bb2-200">Global finance management</span></span>
- [<span data-ttu-id="73bb2-201">財務開発ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="73bb2-201">Financials development home page</span></span>](../financial/financial-dev-home-page.md)

## <a name="licensing"></a><span data-ttu-id="73bb2-202">ライセンス</span><span class="sxs-lookup"><span data-stu-id="73bb2-202">Licensing</span></span>
- [<span data-ttu-id="73bb2-203">ISV ライセンス</span><span class="sxs-lookup"><span data-stu-id="73bb2-203">ISV licensing</span></span>](isv-licensing.md)

## <a name="supply-chain-management"></a><span data-ttu-id="73bb2-204">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="73bb2-204">Supply chain management</span></span>
- [<span data-ttu-id="73bb2-205">ガント作成ガイド</span><span class="sxs-lookup"><span data-stu-id="73bb2-205">Gantt development guide</span></span>](../user-interface/gantt-development-guide.md)
- [<span data-ttu-id="73bb2-206">新しい輸送管理エンジンの作成</span><span class="sxs-lookup"><span data-stu-id="73bb2-206">Create a new transportation management engine</span></span>](../../supply-chain/transportation/create-new-transportation-management-engine.md)

## <a name="additional-resources"></a><span data-ttu-id="73bb2-207">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="73bb2-207">Additional resources</span></span>
[<span data-ttu-id="73bb2-208">開発のための内部者向けヒント</span><span class="sxs-lookup"><span data-stu-id="73bb2-208">Insider tips on development</span></span>](https://community.dynamics.com/ax/b/newdynamicsax)



