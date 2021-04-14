---
title: 電子申告を使用したテストの自動化
description: このトピックでは、電子申告 (ER) フレームワークのベースライン機能を使用して、機能テストを自動化する方法について説明します。
author: NickSelin
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0d029773d9aa59b27f80d2f670984a352e163122
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743874"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="7cd6f-103">電子申告を使用したテストの自動化</span><span class="sxs-lookup"><span data-stu-id="7cd6f-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7cd6f-104">このトピックでは、電子申告 (ER) フレームワークを使用して、いくつかの機能テストを自動化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="7cd6f-105">このトピックでは、仕入先支払処理のテストを自動化する方法例について説明します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="7cd6f-106">アプリケーションは、仕入先支払処理中に ER フレームワークを使用して、支払ファイルとそれに対応するドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="7cd6f-107">ER フレームワークは、さまざまな支払タイプの支払処理および形式のドキュメント生成をサポートするデータ モデル、モデル マッピング、および形式コンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="7cd6f-108">これらのコンポーネントは、Microsoft Dynamics Lifecycle Services (LCS) からダウンロードされ、インスタンスにインポートされます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="7cd6f-109">また、各 Microsoft コンポーネントをカスタマイズして、それを独自のカスタム コンポーネントの基礎として使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="7cd6f-110">カスタム バージョンを作成することにより、特定の要件をサポートする変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="7cd6f-111">たとえば、ER データ モデルと ER モデル マッピングを調整して、顧客固有のアプリケーション データにアクセスしたり、ER 形式を変更して生成されたドキュメントのレイアウトを変更したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="7cd6f-112">カスタマイズされた ER 形式を使用して、仕入先支払を生成する支払ファイルを処理したり、管理レポートを処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="7cd6f-113">バージョン管理は ER のコンポーネントでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="7cd6f-114">したがって、Microsoft では、仕入先支払処理のために ER ソリューションの更新バージョンが提供され、再ベースにより、更新されたバージョンをカスタマイズされたコンポーネントと自動的にマージすることができます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="7cd6f-115">ただし、再ベースのバージョンが予期したとおりに動作するかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="7cd6f-116">ER データ モデルと ER モデル マッピングは、さまざまなタイプの支払を処理し、国や地域固有の支払 ドキュメントを生成するために使用される多くの ER 形式に共通です。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="7cd6f-117">したがって、複数の会社で自動的にユーザー承認および統合テストが行われるようにすることが非常に望ましいです。ただし、各ターゲット会社の国/地域のコンテキストを考慮し、異なるデータセットを使用するなどする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="7cd6f-118">コンフィギュレーション プロバイダーから受け取った形式に基づく形式のカスタム バージョンを作成する方法の詳細については、[ER 形式の新しい基準バージョンを採用してその形式をアップグレードする](./tasks/er-upgrade-format.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="7cd6f-119">重要な概念</span><span class="sxs-lookup"><span data-stu-id="7cd6f-119">Key concepts</span></span>

<span data-ttu-id="7cd6f-120">機能パワー ユーザーは、ソース コードを記述することなく、ユーザーの受け入れと統合のテストを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="7cd6f-121">ER ベースライン機能を使用して、生成されたドキュメントをマスター コピーと比較します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="7cd6f-122">詳細については、[生成されたレポート結果を追跡し、ベースライン値と比較する](er-trace-reports-compare-baseline.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="7cd6f-123">タスク レコーダーを使用してテスト ケースを記録し、ベースライン評価を含めます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="7cd6f-124">詳細については、[タスク レコーダーのリソース](../user-interface/task-recorder.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-124">For more information, see [Task recorder resources](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="7cd6f-125">必要なテスト シナリオのテスト ケースをグループ化します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="7cd6f-126">詳細については、 [ユーザー受け入れテストの作成と自動化](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-126">For more information, see [Create and automate user acceptance tests](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="7cd6f-127">LCS でビジネス プロセス モデル (BPM) を使用して、ユーザー受け入れテスト用のライブラリを作成します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="7cd6f-128">BPM テスト ライブラリを使用して、Microsoft Azure DevOps Services (Azure DevOps) でテスト計画とテスト スイートを作成します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="7cd6f-129">機能パワー ユーザーは、ユーザー受け入れと統合テストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="7cd6f-130">目的のテスト スイートのテスト ケースを実行するには、Regression Suite Automation Tool (RSAT) を使用します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="7cd6f-131">テスト結果を Azure DevOps にレポートし、このサービスを使用してそれらの結果を調査します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7cd6f-132">必要条件</span><span class="sxs-lookup"><span data-stu-id="7cd6f-132">Prerequisites</span></span>

<span data-ttu-id="7cd6f-133">このトピックのタスクを完了する前に、以下の前提条件を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="7cd6f-134">テストの自動化をサポートするトポロジを配置します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="7cd6f-135">**システム管理者** ロールは、このトポロジのインスタンスへのアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="7cd6f-136">このトポロジには、この例で使用するデモデータを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="7cd6f-137">詳細については、[継続的なビルドとテストの自動化をサポートする環境を配置して使用する](../perf-test/continuous-build-test-automation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-137">For more information, see [Deploy and use an environment that supports continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="7cd6f-138">ユーザー受け入れと統合テストを自動的に実行するには、使用しているトポロジに RSAT をインストールし、適切な方法でコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="7cd6f-139">RSAT をインストールして構成し、Finance and Operations アプリおよび Azure DevOpsと連携するように構成する方法の詳細については、[Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="7cd6f-140">このツールを使用するための前提条件に注意してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="7cd6f-141">以下の図は、RSAT の設定の一例を表しています。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="7cd6f-142">青い四角形は、Azure DevOpsへのアクセスを指定するパラメーターを囲みます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="7cd6f-143">緑色の四角形は、インスタンスへのアクセスを指定するパラメーターを囲みます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="7cd6f-144">![RSAT 設定](media/GER-Configure.png "RSAT の設定ダイアログ ボックスのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="7cd6f-145">正しい実行順序を保証するためにスイートでテスト ケースを整理し、さらにレポート作成および調査のためにテスト実行のログを収集するには、配置されたトポロジから Azure DevOps にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="7cd6f-146">このトピックの例を完了するには、[RSAT テストの ER 使用方法](https://go.microsoft.com/fwlink/?linkid=874684)をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="7cd6f-147">この zip ファイルには、次のタスク ガイドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="7cd6f-148">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="7cd6f-148">Content</span></span>                                           | <span data-ttu-id="7cd6f-149">ファイル名および場所</span><span class="sxs-lookup"><span data-stu-id="7cd6f-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="7cd6f-150">テスト用にデータを準備するためのサンプル タスク記録</span><span class="sxs-lookup"><span data-stu-id="7cd6f-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="7cd6f-151">準備\\記録 .xml</span><span class="sxs-lookup"><span data-stu-id="7cd6f-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="7cd6f-152">仕入先支払を処理するためのタスク記録例</span><span class="sxs-lookup"><span data-stu-id="7cd6f-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="7cd6f-153">プロセス\\記録 .xml</span><span class="sxs-lookup"><span data-stu-id="7cd6f-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="7cd6f-154">仕入先支払を処理するための買掛金勘定モジュールの準備</span><span class="sxs-lookup"><span data-stu-id="7cd6f-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="7cd6f-155">インスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="7cd6f-156">次の ER コンフィギュレーションを LCS からダウンロードする</span><span class="sxs-lookup"><span data-stu-id="7cd6f-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="7cd6f-157">指示については、[Lifecycle Services からのコンフィギュレーションの ER インポート](./tasks/er-import-configuration-lifecycle-services.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="7cd6f-158">**支払モデル** ER モデル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7cd6f-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="7cd6f-159">**支払 モデル マッピング 1611** ER モデル マッピング コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7cd6f-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="7cd6f-160">**BACS (英国)** ER 形式のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7cd6f-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="7cd6f-161">![電子申告コンフィギュレーション](media/GER-Configurations.png "電子申告のンフィギュレーション ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="7cd6f-162">イギリスで国/地域のコンテキストを持つ **GBSI** デモ データの会社を選択してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="7cd6f-163">買掛金勘定パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7cd6f-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="7cd6f-164">**買掛金勘定 \>支払設定 \> 支払方法** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="7cd6f-165">**電子** 支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="7cd6f-166">選択した支払方法をコンフィギュレーションして、仕入先支払処理のために既にダウンロードした **BACS (英国)** ER 形式を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="7cd6f-167">**ファイル形式** のクイック タブで、**一般的なエクスポート形式** のオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="7cd6f-168">**書式設定のコンフィギュレーションのエクスポート** フィールドで、**BACS (英国)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="7cd6f-169">![支払方法のページ](media/GER-APParameters.png "支払方法ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cd6f-170">カスタマイズをサポートするために作成された、この ER 形式の派生バージョンがある場合は、**電子** 支払方法でこのコンフィギュレーションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="7cd6f-171">仕入先支払例を作成します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="7cd6f-172">**買掛金勘定 \> 支払 \> 支払仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="7cd6f-173">支払仕訳帳が転記されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="7cd6f-174">![支払仕訳帳のページ](media/GER-APJournal.png "支払仕訳帳ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="7cd6f-175">**明細行** を選択し、次の情報を含む行を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="7cd6f-176">フィールド</span><span class="sxs-lookup"><span data-stu-id="7cd6f-176">Field</span></span>               | <span data-ttu-id="7cd6f-177">サンプル値</span><span class="sxs-lookup"><span data-stu-id="7cd6f-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="7cd6f-178">仕入先名</span><span class="sxs-lookup"><span data-stu-id="7cd6f-178">Vendor name</span></span>         | <span data-ttu-id="7cd6f-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="7cd6f-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="7cd6f-180">デビット</span><span class="sxs-lookup"><span data-stu-id="7cd6f-180">Debit</span></span>               | <span data-ttu-id="7cd6f-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="7cd6f-181">1,000.00</span></span>        |
        | <span data-ttu-id="7cd6f-182">通貨</span><span class="sxs-lookup"><span data-stu-id="7cd6f-182">Currency</span></span>            | <span data-ttu-id="7cd6f-183">GBP</span><span class="sxs-lookup"><span data-stu-id="7cd6f-183">GBP</span></span>             |
        | <span data-ttu-id="7cd6f-184">相手勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="7cd6f-184">Offset account type</span></span> | <span data-ttu-id="7cd6f-185">銀行</span><span class="sxs-lookup"><span data-stu-id="7cd6f-185">Bank</span></span>            |
        | <span data-ttu-id="7cd6f-186">相手勘定</span><span class="sxs-lookup"><span data-stu-id="7cd6f-186">Offset account</span></span>      | <span data-ttu-id="7cd6f-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="7cd6f-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="7cd6f-188">支払方法</span><span class="sxs-lookup"><span data-stu-id="7cd6f-188">Method of payment</span></span>   | <span data-ttu-id="7cd6f-189">電子</span><span class="sxs-lookup"><span data-stu-id="7cd6f-189">Electronic</span></span>      |

    <span data-ttu-id="7cd6f-190">![仕入先支払のページ](media/GER-APJournalLines.png "仕入先支払ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="7cd6f-191">ER フレームワークを準備して仕入先支払処理をテストします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="7cd6f-192">ER パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7cd6f-192">Configure ER parameters</span></span>

1. <span data-ttu-id="7cd6f-193">**組織管理 \> 電子申告 \> 電子申告パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="7cd6f-194">**添付ファイル** タブの **ベースライン** フィールドで、ドキュメント管理 (DM) フレームワークが DM 添付ファイルとしてベースライン機能に関連するドキュメントを保持するために使用するドキュメント タイプとして **ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="7cd6f-195">![電子申告のパラメーター ページ](media/GER-ERParameters.png "電子申告パラメーター ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="7cd6f-196">仕入先支払に関連するドキュメントのベースライン コピーの生成</span><span class="sxs-lookup"><span data-stu-id="7cd6f-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="7cd6f-197">**買掛金勘定 \> 支払 \> 支払仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="7cd6f-198">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-198">Select **Lines**.</span></span>
3. <span data-ttu-id="7cd6f-199">**支払の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="7cd6f-200">**電子** 支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="7cd6f-201">**GBSI OPER** 銀行口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="7cd6f-202">**管理レポートの印刷** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="7cd6f-203">生成された出力を zip ファイルとしてダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="7cd6f-204">ダウンロード ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="7cd6f-205">ダウンロードしたファイルから次のファイルを展開します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="7cd6f-206">**ファイル** テキスト形式の支払ファイル</span><span class="sxs-lookup"><span data-stu-id="7cd6f-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="7cd6f-207">**ERVendOutPaymControlReport** XLSX 形式の管理レポート ファイル</span><span class="sxs-lookup"><span data-stu-id="7cd6f-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="7cd6f-208">![展開されたファイル](media/GER-APJournalProcessed.png "Windows エクスプローラーで展開されたファイル名のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="7cd6f-209">ER ベースライン機能の有効化</span><span class="sxs-lookup"><span data-stu-id="7cd6f-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="7cd6f-210">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="7cd6f-211">アクション ウィンドウの **コンフィギュレーション** タブで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="7cd6f-212">**デバッグモードで実行する** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="7cd6f-213">**デバック モードで実行** パラメーターを有効にすると、送信ドキュメントを生成するすべての ER 形式の実行後に、ER フレームワークに次のアクションを実行させます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="7cd6f-214">実行された ER 形式のコンポーネントのいずれかに対して、ベースラインがコンフィギュレーションされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="7cd6f-215">コンフィギュレーションされた各ベースラインが現在の条件に適用可能かどうかを確認します (サインインした会社の会社コード、生成された出力のファイル名とファイル名拡張子など)。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="7cd6f-216">適用する各ベースラインに対して、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="7cd6f-217">ER フォーマットの実行中に生成された出力を、対応するベースラインと比較します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="7cd6f-218">比較の結果を ER コンフィギュレーション デバッグ ログに格納します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="7cd6f-219">仕入先支払処理の ER ベースラインのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7cd6f-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="7cd6f-220">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="7cd6f-221">**ベースライン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="7cd6f-222">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-222">Select **New**.</span></span>
4. <span data-ttu-id="7cd6f-223">**参照** フィールドで、**BACS (英国)** 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="7cd6f-224">**添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="7cd6f-225">仕入先支払ファイルに新しいベースラインを追加します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="7cd6f-226">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-226">Select **New**.</span></span>
    2. <span data-ttu-id="7cd6f-227">**タイプ** フィールドで、ベースライン コンポーネントを格納するために ER パラメーターにコンフィギュレーションした **ファイル** DM ドキュメント タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="7cd6f-228">ローカルにテキスト形式で保存された **ファイル** 支払ファイルを参照します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="7cd6f-229">**説明** フィールドに、**支払 TXT ファイル** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="7cd6f-230">仕入先支払の管理レポートに新しいベースラインを追加します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="7cd6f-231">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-231">Select **New**.</span></span>
    2. <span data-ttu-id="7cd6f-232">**タイプ** フィールドで、ベースライン コンポーネントを格納するために ER パラメーターにコンフィギュレーションした **ファイル** DM ドキュメント タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="7cd6f-233">ローカルに XLSX 形式で保存された **ERVendOutPaymControlReport** 管理レポートを参照します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="7cd6f-234">**説明** フィールドに、**支払 XLSX 管理レポート** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="7cd6f-235">![仕入先支払ファイルと管理レポートのベースライン](media/GER-BaselineAttachments.png "支払 XLSX 管理レポートが選択されたコンフィギュレーション ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="7cd6f-236">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-236">Close the page.</span></span>
9. <span data-ttu-id="7cd6f-237">**ベースライン** のクイックタブで、**新規** を選択して支払ファイルのベースラインをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="7cd6f-238">行に **支払ファイルのベースライン設定** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="7cd6f-239">**ファイル コンポーネント名** フィールドで、**ファイル** を選択して、このベースラインを BACS (英国) テキスト形式の支払ファイルを生成する ER 形式の出力に適用します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="7cd6f-240">**会社** フィールドで **BACS (英国)** ER 形式が GBSI 会社で実行されている場合にこのベースラインを適用するには、**GBSI** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="7cd6f-241">**ファイル名マスク** フィールドに **\*.TXT** と入力して、**.txt** ファイル名拡張子を持つ **ファイル** 形式コンポーネントの出力のみに、このベースラインを適用します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="7cd6f-242">**ベースライン** フィールドで **支払 TXT ファイル** を選択して、このベースラインが生成された出力との比較に使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="7cd6f-243">**新規** を選択して、管理レポートのベースラインをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="7cd6f-244">行に **管理レポートのベースライン設定** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="7cd6f-245">**ファイル コンポーネント名** フィールドで、**ERVendOutPaymControlReport** を選択して、このベースラインを管理レポートを生成する ER 形式の出力に適用します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="7cd6f-246">**会社** フィールドで **BACS (英国)** ER 形式が GBSI 会社で実行されている場合にこのベースラインを適用するには、**GBSI** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="7cd6f-247">**ファイル名マスク** フィールドに **\*.XLSX** と入力して、**.xslx** ファイル名拡張子を持つ **ERVendOutPaymControlReport** 形式コンポーネントの出力のみに、このベースラインを適用します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="7cd6f-248">**ベースライン** フィールドで **支払 XLSX 管理レポート** を選択して、このベースラインが生成された出力との比較に使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="7cd6f-249">![構成ページのベースライン クイック タブ](media/GER-BaselineRules.png "コンフィギュレーション ページのベースライン クイック タブのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="7cd6f-250">仕入先支払処理を検証するテストの記録</span><span class="sxs-lookup"><span data-stu-id="7cd6f-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="7cd6f-251">機能 パワーユーザーとして、仕入先支払処理をテストするための独自の手順を記録できます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="7cd6f-252">以前にダウンロードした **準備\\記録 .xml** タスク記録を再生する (そして必要に応じて編集する) ことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="7cd6f-253">この記録は、すべてのテスト データを適切な状態に設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="7cd6f-254">この手順が必要なのは、テストを何度も実行でき、すべてのテストで同じ状態のデータを使用する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="7cd6f-255">ユーザー設定のリセット</span><span class="sxs-lookup"><span data-stu-id="7cd6f-255">Reset user settings</span></span>

1. <span data-ttu-id="7cd6f-256">既定のダッシュボードを開きます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="7cd6f-257">**設定** ボタン (ギヤ記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="7cd6f-258">**ユーザー オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-258">Select **User options**.</span></span>
4. <span data-ttu-id="7cd6f-259">**使用状況データ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="7cd6f-260">**リセット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-260">Select **Reset**.</span></span>
6. <span data-ttu-id="7cd6f-261">**はい** を選択して、使用状況データをリセットすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="7cd6f-262">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="7cd6f-263">テスト用データを準備する手順を記録する</span><span class="sxs-lookup"><span data-stu-id="7cd6f-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="7cd6f-264">**設定** ボタン (ギヤ記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="7cd6f-265">**タスク レコーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="7cd6f-266">**記録の再生** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="7cd6f-267">**この PC から開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="7cd6f-268">**参照** を選択し、ローカルに保存された **準備\\記録 .xml** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="7cd6f-269">**スタート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-269">Select **Start**.</span></span>
7. <span data-ttu-id="7cd6f-270">記録のすべての手順が再生されるまで、**次の保留中のステップの再生** を選択し続けます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="7cd6f-271">このタスク記録は、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="7cd6f-272">処理された支払明細行の状態を **なし** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="7cd6f-273">![タスク記録手順 3 から 4](media/GER-Recording1Review1.png "タスク記録手順 3 から 4 のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="7cd6f-274">**デバッグモードで実行** ER ユーザーパラメーターをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="7cd6f-275">![タスク記録手順 9 から 10](media/GER-Recording1Review2.png "タスク記録手順 9 から 10 のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="7cd6f-276">生成されたファイルとベースラインとの比較の結果を含む ER デバッグ ログをクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="7cd6f-277">![タスク記録手順 13 から 15](media/GER-Recording1Review3.png "タスク記録手順 13 から 15 のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="7cd6f-278">仕入先支払処理をテストする手順の記録</span><span class="sxs-lookup"><span data-stu-id="7cd6f-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="7cd6f-279">以前にダウンロードした **処理\\記録 .xml** タスク記録を再生する (そして必要に応じて編集する) ことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="7cd6f-280">この記録は、仕入先支払を処理し、生成されたドキュメントとそれに対応するベースラインとの比較の結果を検証するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="7cd6f-281">**設定** ボタン (ギヤ記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="7cd6f-282">**タスク レコーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="7cd6f-283">**記録の再生** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="7cd6f-284">**この PC から開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="7cd6f-285">**参照** を選択し、ローカルに保存された **処理\\記録 .xml** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="7cd6f-286">**スタート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-286">Select **Start**.</span></span>
7. <span data-ttu-id="7cd6f-287">記録のすべての手順が再生されるまで、**次の保留中のステップの再生** を選択し続けます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="7cd6f-288">このタスク記録は、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="7cd6f-289">仕入先支払の処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="7cd6f-290">適切なランタイム パラメーターを選択し、管理レポートの生成をオンにします。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="7cd6f-291">![タスク記録手順 3 から 8](media/GER-Recording2Review1.png "タスク記録手順 3 から 8 のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="7cd6f-292">ER デバッグ ログにアクセスして、生成された出力を対応するベースラインと比較した結果を記録します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="7cd6f-293">ER デバッグ ログでは、比較結果が **生成されたテキスト** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="7cd6f-294">**形式コンポーネント** および **ログ エントリの原因となった形式パス** フィールドは、生成された出力とベースラインとが比較されたファイル コンポーネントを参照します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="7cd6f-295">![電子申告実行ログ ページのエントリ](media/GER-ERDebugLog.png "電子申告実行ログ ページのエントリのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="7cd6f-296">現在の出力とベースラインの比較は、**検証** タスク記録オプションを使用して **現在の値** を選択することによって記録されます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="7cd6f-297">![現在の値と比較するための検証オプションの使用](media/GER-TRRecordValidation.png "現在の値と比較するための検証オプションの使用のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="7cd6f-298">次の図は、記録された検証手順がタスク記録でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="7cd6f-299">![タスク記録手順 13 および 15](media/GER-Recording2Review2.png "タスク記録手順 13 および 15 のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="7cd6f-300">記録されたテストを Azure DevOps に追加する</span><span class="sxs-lookup"><span data-stu-id="7cd6f-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="7cd6f-301">Azure DevOps 環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="7cd6f-302">[ツールをコンフィギュレーション](#prerequisites)したときに RSAT パラメーターで定義したプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="7cd6f-303">[ツールをコンフィギュレーション](#prerequisites)したときに RSAT パラメーターで定義したテスト計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="7cd6f-304">選択したテスト計画に対する新しいテスト ケースの作成</span><span class="sxs-lookup"><span data-stu-id="7cd6f-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="7cd6f-305">テスト ケースに **仕入先の電子支払処理をテストするためのデータを準備する** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="7cd6f-306">以前にダウンロードした **準備** フォルダーから **記録 .xml** ファイルを添付します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="7cd6f-307">選択したテスト計画に対する新しいテスト ケースの作成</span><span class="sxs-lookup"><span data-stu-id="7cd6f-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="7cd6f-308">テスト ケースに **ER 形式 BACS (英国) を使用した仕入先支払のテスト処理** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="7cd6f-309">以前にダウンロードした **処理** フォルダーから **記録 .xml** ファイルを添付します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="7cd6f-310">![選択したテスト計画の新しいテスト ケース](media/GER-RSAT-DevOps-Tests-Passed.png "選択したテスト計画の新しいテスト ケースのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="7cd6f-311">追加されたテストの正しい実行順序に注意してください。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="7cd6f-312">記録されたテストを実行するための RSAT の準備</span><span class="sxs-lookup"><span data-stu-id="7cd6f-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="7cd6f-313">Azure DevOps から RSAT にテストを読み込む</span><span class="sxs-lookup"><span data-stu-id="7cd6f-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="7cd6f-314">現在のトポロジでローカル RSAT アプリケーションを開きます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="7cd6f-315">**読み込み** を選択し、現在 Azure DevOps 内にあるテストを RSAT に読み込みます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="7cd6f-316">![RSAT にロードされたテスト](media/GER-RSAT-RSAT-Tests-Loaded.png "RSAT にロードされたテストのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="7cd6f-317">自動化とパラメーター ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="7cd6f-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="7cd6f-318">RSAT で、Azure DevOps から読み込んだテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="7cd6f-319">**新規** を選択して、RSAT の自動化とパラメーター ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="7cd6f-320">![RSAT で作成された RSAT の自動化およびパラメーター ファイル](media/GER-RSAT-RSAT-Tests-Initiated.png "RSAT で作成された RSAT の自動化およびパラメーター ファイルのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="7cd6f-321">パラメーター ファイルの変更</span><span class="sxs-lookup"><span data-stu-id="7cd6f-321">Modify the parameters files</span></span>

1. <span data-ttu-id="7cd6f-322">RSAT で、**仕入先の電子支払処理をテストするためのデータを準備する** のテスト ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="7cd6f-323">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-323">Select **Edit**.</span></span>
3. <span data-ttu-id="7cd6f-324">開いた Microsoft Excel ブックの **一般** ワークシートで、会社コードを **GBSI** に変更します。これは、この会社がテストの実行に使用されるためです。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="7cd6f-325">RSAT で、**ER 形式 BACS (英国) を使用した仕入先支払のテスト処理** のテスト ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="7cd6f-326">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-326">Select **Edit**.</span></span>
6. <span data-ttu-id="7cd6f-327">開いた Excel のブックの **一般** ワークシートで、会社コードを **GBSI** に変更します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="7cd6f-328">**ERFormatMappingRunLogTable** ワークシートのセル A:3 および C:3 には、出力とベースラインの比較結果を検証するために使用される ER デバッグ ログ テーブル内のフィールドのテキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="7cd6f-329">これらのテキストは、テスト実行中に作成された ER デバッグ ログ レコードを評価するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="7cd6f-330">![ERFormatMappingRunLogTable ワークシート](media/GER-RSAT-RSAT-ExcelParameters.png "ERFormatMappingRunLogTable ワークシートのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="7cd6f-331">テストの実行と結果の分析</span><span class="sxs-lookup"><span data-stu-id="7cd6f-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="7cd6f-332">RSAT でテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="7cd6f-333">RSAT で、読み込まれたテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="7cd6f-334">**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-334">Select **Run**.</span></span>

<span data-ttu-id="7cd6f-335">テスト ケースは、Web ブラウザーを使用してアプリケーションで自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="7cd6f-336">テスト実行の結果の分析</span><span class="sxs-lookup"><span data-stu-id="7cd6f-336">Analyze the results of test execution</span></span>

<span data-ttu-id="7cd6f-337">テストの実行結果は、RSAT に格納されます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="7cd6f-338">両方のテストが成功したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="7cd6f-339">![RSAT で成功したテスト](media/GER-RSAT-RSAT-Tests-Passed.png "RSAT で成功したテストのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="7cd6f-340">テストの実行結果は Azure DevOps にも送信されるので、さらに分析を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="7cd6f-341">![Azure DevOps でのテスト実行結果](media/GER-RSAT-DevOps-Tests-Added.png "Azure DevOps でのテスト実行結果のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="7cd6f-342">テストが失敗した場合のシミュレーション</span><span class="sxs-lookup"><span data-stu-id="7cd6f-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="7cd6f-343">生成された出力のうち少なくとも 1 つが対応するベースラインと一致しない場合、このテスト スイートは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="7cd6f-344">この状況を達成するために、派生バージョンの **BACS (英国)** 形式を使用することができ、それは対応するベースラインとはコンテンツが異なる支払いファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="7cd6f-345">この状況をシミュレーションするには、同じ **BACS (英国)** 形式を使用しますが、処理された支払明細行の支払金額を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="7cd6f-346">アプリケーションを開き、**買掛金勘定 \> 支払 \> 支払仕訳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="7cd6f-347">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-347">Select **Lines**.</span></span>
3. <span data-ttu-id="7cd6f-348">支払明細行を選択し、**支払ステータス \> なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="7cd6f-349">**借方** フィールドで、値を **1,000.00** から **2,000.00** に変更します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="7cd6f-350">**保存** をクリックして、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="7cd6f-351">RSAT でテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="7cd6f-352">RSAT で、読み込まれたテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="7cd6f-353">**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-353">Select **Run**.</span></span>

<span data-ttu-id="7cd6f-354">テスト ケースは、Web ブラウザーを使用してアプリケーションで自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="7cd6f-355">テスト実行の結果の分析</span><span class="sxs-lookup"><span data-stu-id="7cd6f-355">Analyze the results of test execution</span></span>

<span data-ttu-id="7cd6f-356">テストの実行結果は、RSAT に格納されます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="7cd6f-357">2 回目のテストは、2 回目の実行時に失敗していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="7cd6f-358">![RSAT で失敗したテスト結果](media/GER-RSAT-RSAT-Tests-Failed.png "RSAT で失敗したテスト結果のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="7cd6f-359">テストの実行結果は Azure DevOps にも送信されるので、さらに分析を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="7cd6f-360">![Azure DevOps で失敗したテスト結果](media/GER-RSAT-DevOps-Tests-Failed.png "Azure DevOps で失敗したテスト結果のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="7cd6f-361">各テストのステータスにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-361">You can access the status of each test.</span></span> <span data-ttu-id="7cd6f-362">実行ログにアクセスして、失敗の理由を分析することもできます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="7cd6f-363">次の図では、実行ログに、生成された支払ファイルとそのベースラインとの間のコンテンツの違いによって、エラーが発生したことが示されています。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="7cd6f-364">![Azure DevOps におけるエラー分析の実行ログ](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Azure DevOps におけるエラー分析の実行ログのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="7cd6f-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="7cd6f-365">したがって、既に説明したように、テスト プラットフォームとして RSAT を使用し、ER ベースライン機能を使用するタスク レコーダー ベースのテスト ケースを使用することで、あらゆる ER 形式の機能を自動的に評価できます。</span><span class="sxs-lookup"><span data-stu-id="7cd6f-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7cd6f-366">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7cd6f-366">Additional resources</span></span>

- [<span data-ttu-id="7cd6f-367">タスク レコーダー リソース</span><span class="sxs-lookup"><span data-stu-id="7cd6f-367">Task recorder resources</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="7cd6f-368">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="7cd6f-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="7cd6f-369">ユーザー受け入れテストの作成と自動化</span><span class="sxs-lookup"><span data-stu-id="7cd6f-369">Create and automate user acceptance tests</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="7cd6f-370">継続的なビルドとテストの自動化をサポートする環境を配置して使用する</span><span class="sxs-lookup"><span data-stu-id="7cd6f-370">Deploy and use an environment that supports continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="7cd6f-371">生成されたレポート結果を追跡し、ベースライン値と比較する</span><span class="sxs-lookup"><span data-stu-id="7cd6f-371">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="7cd6f-372">ER 形式の新しい基準バージョンを採用してその形式をアップグレードする</span><span class="sxs-lookup"><span data-stu-id="7cd6f-372">ER Upgrade your format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="7cd6f-373">Lifecycle Services からのコンフィギュレーションの ER インポート</span><span class="sxs-lookup"><span data-stu-id="7cd6f-373">ER Import a configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]