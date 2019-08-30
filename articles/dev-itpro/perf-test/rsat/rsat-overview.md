---
title: Regression Suite Automation Tool
description: Regression Suite Automation Tool では、機能パワー ユーザーがタスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくても自動テストのスイートに変換できるようにします。
author: robadawy
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5ed5ed7fd88cdd700fbc2492cb7e0076290e696
ms.sourcegitcommit: db84eeef6f0bd531ba45b5e66bdacfd0398472e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887424"
---
# <a name="regression-suite-automation-tool"></a><span data-ttu-id="e6ef8-103">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="e6ef8-103">Regression Suite Automation Tool</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="e6ef8-104">概要</span><span class="sxs-lookup"><span data-stu-id="e6ef8-104">Overview</span></span>
<span data-ttu-id="e6ef8-105">Regression Suite Automation Tool (RSAT) を使用すると、ユーザー受け入れテストの時間と費用を大幅に縮小できます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-105">The Regression suite automation tool (RSAT) significantly reduces the time and cost of user acceptance testing.</span></span> <span data-ttu-id="e6ef8-106">通常、ユーザー受け入れテストは Microsoft アプリケーションの更新プログラムを取得するか、カスタム コードおよびコンフィギュレーションを Dynamics 365 for Finance and Operations 実稼働環境に適用する前に必要です。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-106">User acceptance testing is typically required before taking a  Microsoft application update or applying custom code and configurations to your Dynamics 365 for Finance and Operations production environment.</span></span>

<span data-ttu-id="e6ef8-107">このツールで、機能パワー ユーザーが Finance and Operations タスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくても自動テストのスイートに変換できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-107">This tool enables functional power users to record business tasks using the Finance and Operations Task recorder and convert these recordings into a suite of automated tests without the need to write source code.</span></span> <span data-ttu-id="e6ef8-108">テストライブラリは、ビジネス プロセス モデラー (BPM) ライブラリを使用して保存され、Lifecycle Services (LCS) に配布されます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-108">Test libraries are stored and distributed in Lifecycle Services (LCS) using the Business Process Modeler (BPM) libraries.</span></span> <span data-ttu-id="e6ef8-109">また、これらのライブラリは、テストの実行、レポート、および調査のために Azure DevOps サービス (Azure DevOps) と完全に統合されています。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-109">These libraries are also fully integrated with Azure DevOps Services (Azure DevOps) for test execution, reporting and investigation.</span></span> <span data-ttu-id="e6ef8-110">テスト パラメーターは、テスト ステップから切り離され、Microsoft Excel ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-110">Test parameters are decoupled from test steps and stored in Microsoft Excel files.</span></span>

<span data-ttu-id="e6ef8-111">RSAT の使用についての定義。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-111">RSAT usage is described in these topics:</span></span>

+ [<span data-ttu-id="e6ef8-112">Regression Suite Automation Tool (このトピック)</span><span class="sxs-lookup"><span data-stu-id="e6ef8-112">Regression Suite Automation Tool (this topic)</span></span>](rsat-overview.md)
+ [<span data-ttu-id="e6ef8-113">Regression Suite Automation Tool インストールおよび構成</span><span class="sxs-lookup"><span data-stu-id="e6ef8-113">Regression Suite Automation Tool installation and configuration</span></span>](rsat-install-configure.md)
+ [<span data-ttu-id="e6ef8-114">Regression Suite Automation Tool テスト ケースの実行</span><span class="sxs-lookup"><span data-stu-id="e6ef8-114">Run Regression Suite Automation Tool test cases</span></span>](rsat-run.md)
+ [<span data-ttu-id="e6ef8-115">予測値を検証する</span><span class="sxs-lookup"><span data-stu-id="e6ef8-115">Validate expected values</span></span>](rsat-validate-expected.md)
+ [<span data-ttu-id="e6ef8-116">テスト ケース</span><span class="sxs-lookup"><span data-stu-id="e6ef8-116">Chain test cases</span></span>](rsat-chain-test-cases.md)
+ [<span data-ttu-id="e6ef8-117">派生テスト ケース</span><span class="sxs-lookup"><span data-stu-id="e6ef8-117">Derived test cases</span></span>](rsat-derived-test-cases.md)
+ [<span data-ttu-id="e6ef8-118">Regression Suite Automation Tool ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e6ef8-118">Regression Suite Automation Tool best practices</span></span>](rsat-best-practices.md)
+ [<span data-ttu-id="e6ef8-119">Regression Suite Automation Tool のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e6ef8-119">Troubleshoot the Regression Suite Atomation Tool</span></span>](rsat-troubleshooting.md)


## <a name="end-to-end-flow"></a><span data-ttu-id="e6ef8-120">エンド ツー エンド フロー</span><span class="sxs-lookup"><span data-stu-id="e6ef8-120">End-to-end flow</span></span>
<span data-ttu-id="e6ef8-121">このツールは、次に定義するエンド ツー エンド フローのパーツに含まれています。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-121">This tool is part of the end to end flow described below.</span></span> <span data-ttu-id="e6ef8-122">Finance and Operations は、LCS および Azure DevOps と共に、テスト ケースの作成 (タスクレコーダーを使用)、構成、実行、調査、および報告のための一連のツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-122">Finance and Operations, along with LCS and Azure DevOps, provide a set of tools for test case authoring (using Task recorder), configuration, execution, investigation, and reporting.</span></span>

![作成、構成、実行](media/end-to-end.png)

<span data-ttu-id="e6ef8-124">このプロセスの詳細については、[ユーザー受け入れテストを作成して自動化する](../../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-124">To learn more about this this process, see [Create and automate user acceptance tests](../../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="e6ef8-125">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e6ef8-125">Lifecycle Services</span></span>
<span data-ttu-id="e6ef8-126">Lifecycle Services (LCS) および BPM を使用することが推奨されますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-126">Using Lifecycle Services (LCS) and BPM is recommended but not required.</span></span> <span data-ttu-id="e6ef8-127">BPM は、テスト ライブラリを管理および配布するための優れたツールです。特に、Microsoft パートナーや独立系ソフトウェア ベンダーに適しています。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-127">BPM is a great tool to manage and distribute test libraries, especially for Microsoft partners and independent software vendors.</span></span> 

<span data-ttu-id="e6ef8-128">Azure DevOps でテストケースを手動で作成し、開発者記録ファイルを Azure DevOps テスト ケースに添付することができます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-128">You can manually create test cases in Azure DevOps and attach developer recording files to your Azure DevOps test cases.</span></span> <span data-ttu-id="e6ef8-129">開発者記録ファイルは、Finance and Operations のタスク レコーダー ウィンドウから直接作成することができます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-129">Developer recording files can be created directly from the Task recorder pane in Finance and Operations.</span></span>

![開発者としてタスク レコードを保存](media/save-as-developer.png)

<span data-ttu-id="e6ef8-131">開発者の記録ファイルを Azure DevOps テストケースに添付する前に、開発者の記録ファイルに **Recording.xml** という名前を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-131">You must name the developer recording file **Recording.xml** before attaching it to a Azure DevOps test case.</span></span> <span data-ttu-id="e6ef8-132">記録ファイルには、**<Test Case Title>** が、テスト ケースの DevOps タイトルである場合に、**<Test Case Title>.xml** と名前を付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-132">The recording file can also be named **<Test Case Title>.xml** where **<Test Case Title>** is the DevOps title of the test case.</span></span>

![ 添付ファイルの追加](media/attachments.png)

## <a name="intended-usage-and-test-classification"></a><span data-ttu-id="e6ef8-134">使用目的およびテストの分類</span><span class="sxs-lookup"><span data-stu-id="e6ef8-134">Intended usage and test classification</span></span>

### <a name="business-cycle-business-process-testing"></a><span data-ttu-id="e6ef8-135">ビジネス サイクル (ビジネス プロセス) のテスト</span><span class="sxs-lookup"><span data-stu-id="e6ef8-135">Business cycle (business process) testing</span></span>
<span data-ttu-id="e6ef8-136">Regression Suite Automation Tool は、ビジネス サイクル テストおよびシナリオ テスト (複数のコンポーネントのテスト) を使用目的としており、通常は開発ライフ サイクルの終了時に発生します。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-136">The Regression suite automation tool is intended to be used for business cycle tests and scenario tests (multiple component tests) that usually occur at the end of the development lifecycle.</span></span> <span data-ttu-id="e6ef8-137">これは、*ユーザー受け入れテスト*とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-137">This is also referred to as *user acceptance testing*.</span></span> <span data-ttu-id="e6ef8-138">ビジネス サイクルのテストは、コンポーネントまたは単体テストよりも少ない数のテスト ケースで構成されます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-138">Business cycle testing consists of a smaller number of test cases than component or unit testing.</span></span> <span data-ttu-id="e6ef8-139">これを下の図に示します。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-139">This is illustrated in the following graphic.</span></span>

![単体テスト、コンポーネント テスト、複数のコンポーネントテスト、ビジネス サイクルテスト](media/business-cycle.png)

### <a name="unit-and-component-testing"></a><span data-ttu-id="e6ef8-141">ユニットおよびコンポーネント テスト</span><span class="sxs-lookup"><span data-stu-id="e6ef8-141">Unit and component testing</span></span>
<span data-ttu-id="e6ef8-142">単体テストの場合は、RSAT を使用しないことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-142">For unit tests, we do not recommend that you use RSAT.</span></span> <span data-ttu-id="e6ef8-143">代わりに、SysTest フレームワークおよび Finance and Operations のビルド/テスト自動化ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-143">Instead, use the SysTest framework and the build/test automation tools of Finance and Operations.</span></span> <span data-ttu-id="e6ef8-144">コンポーネント テストでは、[受け入れテスト ライブラリ](../acceptance-test-library.md) (ATL) を活用します。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-144">For component tests, take advantage of the [Acceptance Test Library](../acceptance-test-library.md) (ATL).</span></span> <span data-ttu-id="e6ef8-145">ATL は、 X++ テスト ヘルパーのライブラリです。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-145">ATL is a library of X++ test helpers.</span></span> <span data-ttu-id="e6ef8-146">SysTest フレームワークを使用すると、次の利点があります。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-146">When used with the SysTest framework, it offers the following benefits:</span></span>
+ <span data-ttu-id="e6ef8-147">一貫したテスト データを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-147">Lets you create consistent test data.</span></span>
+ <span data-ttu-id="e6ef8-148">テスト コードが読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-148">Increases the readability of test code.</span></span>
+ <span data-ttu-id="e6ef8-149">テスト データの作成に使用されているメソッドの発見可能性が向上します。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-149">Provides improved discoverability of the methods that are used to create test data.</span></span>
+ <span data-ttu-id="e6ef8-150">前提条件の設定の複雑さを隠します。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-150">Hides the complexity of setting up prerequisites.</span></span>
+ <span data-ttu-id="e6ef8-151">パフォーマンスの高いテスト ケースをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-151">Supports high performance of test cases.</span></span>

<span data-ttu-id="e6ef8-152">詳細については、[継続的デリバリー ホーム ページ](../../dev-tools/continuous-delivery-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-152">For more details, see [Continuous delivery home page](../../dev-tools/continuous-delivery-home-page.md).</span></span>

### <a name="data-integration-testing"></a><span data-ttu-id="e6ef8-153">データ統合テスト</span><span class="sxs-lookup"><span data-stu-id="e6ef8-153">Data integration testing</span></span>
<span data-ttu-id="e6ef8-154">統合テストで RSAT を使用するのではなく、データ管理フレームワーク (DIXF として知られます) に頼ります。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-154">Do not use RSAT for integration tests, instead rely on the data management framework (also known as DIXF).</span></span> <span data-ttu-id="e6ef8-155">[データ タスクの自動化](../../data-entities/data-task-automation.md)フレームワークを使用すると、データ統合シナリオのテストを構成したり自動化したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="e6ef8-155">The [Data task automation](../../data-entities/data-task-automation.md) framework enables you to configure and automate the testing of your data integration scenarios.</span></span>
