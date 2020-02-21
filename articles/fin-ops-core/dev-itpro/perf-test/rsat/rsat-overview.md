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
ms.openlocfilehash: eb0a2a18490f2209cfe98d609d2fda7fd7ff7018
ms.sourcegitcommit: 5d31d3e5f8549b761360c338bc2a1d9506c15999
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030040"
---
# <a name="regression-suite-automation-tool"></a><span data-ttu-id="3bdcc-103">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="3bdcc-103">Regression Suite Automation Tool</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="3bdcc-104">概要</span><span class="sxs-lookup"><span data-stu-id="3bdcc-104">Overview</span></span>
<span data-ttu-id="3bdcc-105">Regression Suite Automation Tool (RSAT) を使用すると、ユーザー受け入れテスト (UAT) の時間と費用を大幅に縮小できます。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-105">The Regression suite automation tool (RSAT) significantly reduces the time and cost of user acceptance testing (UAT).</span></span> <span data-ttu-id="3bdcc-106">通常、UAT は Microsoft アプリケーションの更新プログラムを取得するか、カスタム コードおよび構成を実稼働環境に適用する前に必要です。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-106">UAT is typically required before you take a Microsoft application update, or before you apply custom code and configurations to your production environment.</span></span> <span data-ttu-id="3bdcc-107">RSAT により、機能パワー ユーザーはタスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくてもタスク記録を一連の自動テストに変換できます。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-107">RSAT lets functional power users record business tasks by using Task recorder and then convert the recordings into a suite of automated tests, without having to write source code.</span></span> <span data-ttu-id="3bdcc-108">タスク レコーダーの詳細については、 [タスク レコーダー のリソース](../../user-interface/task-recorder.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-108">For more information about Task recorder, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span>

<span data-ttu-id="3bdcc-109">RSATは、テストの実行、報告、および調査のために Microsoft Azure DevOps と完全に統合されています。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-109">RSAT is fully integrated with Microsoft Azure DevOps for test execution, reporting, and investigation.</span></span> <span data-ttu-id="3bdcc-110">テスト パラメーターは、テスト ステップから切り離され、Microsoft Excel ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-110">Test parameters are decoupled from test steps and stored in Microsoft Excel files.</span></span>

<span data-ttu-id="3bdcc-111">RSAT の使用についての定義。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-111">RSAT usage is described in these topics:</span></span>

+ [<span data-ttu-id="3bdcc-112">Regression Suite Automation Tool (このトピック)</span><span class="sxs-lookup"><span data-stu-id="3bdcc-112">Regression Suite Automation Tool (this topic)</span></span>](rsat-overview.md)
+ [<span data-ttu-id="3bdcc-113">Regression Suite Automation Tool インストールおよび構成</span><span class="sxs-lookup"><span data-stu-id="3bdcc-113">Regression Suite Automation Tool installation and configuration</span></span>](rsat-install-configure.md)
+ [<span data-ttu-id="3bdcc-114">Regression Suite Automation Tool テスト ケースの実行</span><span class="sxs-lookup"><span data-stu-id="3bdcc-114">Run Regression Suite Automation Tool test cases</span></span>](rsat-run.md)
+ [<span data-ttu-id="3bdcc-115">予測値を検証する</span><span class="sxs-lookup"><span data-stu-id="3bdcc-115">Validate expected values</span></span>](rsat-validate-expected.md)
+ [<span data-ttu-id="3bdcc-116">テスト ケースのチェーン</span><span class="sxs-lookup"><span data-stu-id="3bdcc-116">Chain test cases</span></span>](rsat-chain-test-cases.md)
+ [<span data-ttu-id="3bdcc-117">派生テスト ケース</span><span class="sxs-lookup"><span data-stu-id="3bdcc-117">Derived test cases</span></span>](rsat-derived-test-cases.md)
+ [<span data-ttu-id="3bdcc-118">Regression Suite Automation Tool ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="3bdcc-118">Regression Suite Automation Tool best practices</span></span>](rsat-best-practices.md)
+ [<span data-ttu-id="3bdcc-119">Regression Suite Automation Tool のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="3bdcc-119">Troubleshoot the Regression Suite Automation Tool</span></span>](rsat-troubleshooting.md)


## <a name="end-to-end-flow"></a><span data-ttu-id="3bdcc-120">エンド ツー エンド フロー</span><span class="sxs-lookup"><span data-stu-id="3bdcc-120">End-to-end flow</span></span>
<span data-ttu-id="3bdcc-121">このツールは、次に定義するエンド ツー エンド フローのパーツに含まれています。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-121">This tool is part of the end to end flow described below.</span></span> <span data-ttu-id="3bdcc-122">このアプリケーションは、Microsoft Dynamics Lifecycle Services (LCS) および Azure DevOps と共に、テスト ケースの作成 (タスク レコーダーを使用)、構成、実行、調査、および報告に対する一連のツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-122">The application, along with Microsoft Dynamics Lifecycle Services (LCS) and Azure DevOps, provide a set of tools for test case authoring (using Task recorder), configuration, execution, investigation, and reporting.</span></span>

![作成、構成、実行](media/end-to-end.png)

<span data-ttu-id="3bdcc-124">このプロセスの詳細については、[ユーザー受け入れテストを作成して自動化する](../../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-124">To learn more about this this process, see [Create and automate user acceptance tests](../../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

## <a name="lcs-and-bpm"></a><span data-ttu-id="3bdcc-125">LCS および BPM</span><span class="sxs-lookup"><span data-stu-id="3bdcc-125">LCS and BPM</span></span>

<span data-ttu-id="3bdcc-126">LCS でビジネス プロセス モデラー (BPM) ツールを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-126">You aren't required to use the Business process modeler (BPM) tool in LCS.</span></span> <span data-ttu-id="3bdcc-127">ただし、プロジェクトとテナント間でテスト ライブラリを管理および配布できるようにする場合、推奨されているツールは BPM です。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-127">However, BPM is the recommended tool if you want to enable the management and distribution of test libraries across projects and tenants.</span></span> <span data-ttu-id="3bdcc-128">これらの機能は、Microsoft パートナーおよび独立系ソフトウェア ベンダー (ISV) にとって特に便利です。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-128">These capabilities are especially useful for Microsoft partners and independent software vendors (ISVs).</span></span> <span data-ttu-id="3bdcc-129">BPM では、LCS ソリューションの一部としてテスト ライブラリを配布できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-129">BPM enables the distribution of test libraries as part of LCS solutions.</span></span>

<span data-ttu-id="3bdcc-130">BPM を使用していない場合は、Azure DevOps で手動でテスト ケースを作成し、開発者記録ファイルを Azure DevOps テスト ケースに添付できます。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-130">If you are not using BPM, you can manually create test cases in Azure DevOps and attach developer recording files to your Azure DevOps test cases.</span></span> <span data-ttu-id="3bdcc-131">開発者記録ファイルは、タスク レコーダー ウィンドウから直接作成できます。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-131">You can create developer recording files directly from the Task recorder pane.</span></span>

![開発者としてタスク レコードを保存](media/save-as-developer.png)

<span data-ttu-id="3bdcc-133">開発者記録ファイルに **Recording.xml** という名前を付けてから、Azure DevOps テスト ケースに添付する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-133">You must name the developer recording file **Recording.xml** before attaching it to the Azure DevOps test case.</span></span> <span data-ttu-id="3bdcc-134">または、記録ファイル **-テスト ケース タイトル-.xml** という名前を付けることもできます。これは、**-テスト ケース タイトル-** はテスト ケースの DevOps タイトルになります。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-134">Alternatively, you can name the recording file **-Test Case Title-.xml**, where **-Test Case Title-** is the DevOps title of the test case.</span></span>

![添付ファイルの追加](media/attachments.png)

## <a name="intended-usage-and-test-classification"></a><span data-ttu-id="3bdcc-136">使用目的およびテストの分類</span><span class="sxs-lookup"><span data-stu-id="3bdcc-136">Intended usage and test classification</span></span>

### <a name="business-cycle-business-process-testing"></a><span data-ttu-id="3bdcc-137">ビジネス サイクル (ビジネス プロセス) のテスト</span><span class="sxs-lookup"><span data-stu-id="3bdcc-137">Business cycle (business process) testing</span></span>
<span data-ttu-id="3bdcc-138">Regression Suite Automation Tool は、ビジネス サイクル テストおよびシナリオ テスト (複数のコンポーネントのテスト) を使用目的としており、通常は開発ライフ サイクルの終了時に発生します。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-138">The Regression suite automation tool is intended to be used for business cycle tests and scenario tests (multiple component tests) that usually occur at the end of the development lifecycle.</span></span> <span data-ttu-id="3bdcc-139">これは、*ユーザー受け入れテスト*とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-139">This is also referred to as *user acceptance testing*.</span></span> <span data-ttu-id="3bdcc-140">ビジネス サイクルのテストは、コンポーネントまたは単体テストよりも少ない数のテスト ケースで構成されます。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-140">Business cycle testing consists of a smaller number of test cases than component or unit testing.</span></span> <span data-ttu-id="3bdcc-141">これを下の図に示します。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-141">This is illustrated in the following graphic.</span></span>

![単体テスト、コンポーネント テスト、複数のコンポーネントテスト、ビジネス サイクルテスト](media/business-cycle.png)

### <a name="unit-and-component-testing"></a><span data-ttu-id="3bdcc-143">ユニットおよびコンポーネント テスト</span><span class="sxs-lookup"><span data-stu-id="3bdcc-143">Unit and component testing</span></span>
<span data-ttu-id="3bdcc-144">単体テストの場合は、RSAT を使用しないことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-144">For unit tests, we do not recommend that you use RSAT.</span></span> <span data-ttu-id="3bdcc-145">代わりに、SysTest フレームワークとビルド / テスト自動化ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-145">Instead, use the SysTest framework and the build/test automation tools.</span></span> <span data-ttu-id="3bdcc-146">コンポーネント テストでは、[受け入れテスト ライブラリ リソース](../acceptance-test-library.md) (ATL) を活用します。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-146">For component tests, take advantage of the [Acceptance test library resources](../acceptance-test-library.md) (ATL).</span></span> <span data-ttu-id="3bdcc-147">ATL は、 X++ テスト ヘルパーのライブラリです。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-147">ATL is a library of X++ test helpers.</span></span> <span data-ttu-id="3bdcc-148">SysTest フレームワークを使用すると、次の利点があります。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-148">When used with the SysTest framework, it offers the following benefits:</span></span>
+ <span data-ttu-id="3bdcc-149">一貫したテスト データを作成できます。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-149">Lets you create consistent test data.</span></span>
+ <span data-ttu-id="3bdcc-150">テスト コードが読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-150">Increases the readability of test code.</span></span>
+ <span data-ttu-id="3bdcc-151">テスト データの作成に使用されているメソッドの発見可能性が向上します。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-151">Provides improved discoverability of the methods that are used to create test data.</span></span>
+ <span data-ttu-id="3bdcc-152">前提条件の設定の複雑さを隠します。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-152">Hides the complexity of setting up prerequisites.</span></span>
+ <span data-ttu-id="3bdcc-153">パフォーマンスの高いテスト ケースをサポートします。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-153">Supports high performance of test cases.</span></span>

<span data-ttu-id="3bdcc-154">詳細については、[継続的デリバリー ホーム ページ](../../dev-tools/continuous-delivery-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-154">For more details, see [Continuous delivery home page](../../dev-tools/continuous-delivery-home-page.md).</span></span>

### <a name="data-integration-testing"></a><span data-ttu-id="3bdcc-155">データ統合テスト</span><span class="sxs-lookup"><span data-stu-id="3bdcc-155">Data integration testing</span></span>
<span data-ttu-id="3bdcc-156">統合テストで RSAT を使用するのではなく、データ管理フレームワーク (DIXF として知られます) に頼ります。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-156">Do not use RSAT for integration tests, instead rely on the data management framework (also known as DIXF).</span></span> <span data-ttu-id="3bdcc-157">[データ タスクの自動化](../../data-entities/data-task-automation.md)フレームワークを使用すると、データ統合シナリオのテストを構成したり自動化したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-157">The [Data task automation](../../data-entities/data-task-automation.md) framework enables you to configure and automate the testing of your data integration scenarios.</span></span>
