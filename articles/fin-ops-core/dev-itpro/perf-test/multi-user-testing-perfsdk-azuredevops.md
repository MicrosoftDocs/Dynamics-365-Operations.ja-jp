---
title: パフォーマンス SDK と Azure DevOps を使用したマルチユーザー テスト
description: このトピックでは、Microsoft Azure DevOps、パフォーマンス SDK、およびタスク レコーダー パフォーマンス テスト スクリプトを使用してマルチユーザー テストを行う方法について説明します。
author: hasaid
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1b7aaff1ea3b0378a895f65db0a3e9d1a9fab56
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749241"
---
# <a name="multi-user-testing-with-the-performance-sdk-and-azure-devops"></a><span data-ttu-id="d81e2-103">パフォーマンス SDK および Azure DevOps を使用したマルチ ユーザー テスト</span><span class="sxs-lookup"><span data-stu-id="d81e2-103">Multi-user testing with the Performance SDK and Azure DevOps</span></span>

[!include [banner](../includes/banner.md)]

  > [!IMPORTANT]
  > <span data-ttu-id="d81e2-104">Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。</span><span class="sxs-lookup"><span data-stu-id="d81e2-104">Visual Studio 2019 will be the last version of Visual Studio with web performance and load test features.</span></span> <span data-ttu-id="d81e2-105">将来的に、代替ソリューションの推奨を公開します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-105">In the future, we will publish some recommendations for alternative solutions.</span></span>  
  > - <span data-ttu-id="d81e2-106">Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。</span><span class="sxs-lookup"><span data-stu-id="d81e2-106">If you are using the Visual Studio and Test Controller/Test Agent for on-premises load testing, Visual Studio 2019 will be the last version.</span></span> <span data-ttu-id="d81e2-107">そのサポート サイクルが終了するまで継続して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d81e2-107">You can continue using it until the end of the support cycle.</span></span> 
  > - <span data-ttu-id="d81e2-108">クラウド ベースの負荷テストサービスをご利用の場合、同サービスは 2020 年 3 月 31 日まで継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="d81e2-108">If you are using the cloud-based load testing service, it will continue to run through March 31, 2020.</span></span> <span data-ttu-id="d81e2-109">それまでの間は、同サービスの全機能を継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="d81e2-109">Until then, you can continue to use all of the experiences powered by this service without interruption.</span></span> <span data-ttu-id="d81e2-110">また、オンプレミス負荷テストに切り替えることがも可能です。</span><span class="sxs-lookup"><span data-stu-id="d81e2-110">Alternatively, you can switch to on-premises load testing.</span></span> <span data-ttu-id="d81e2-111">詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。</span><span class="sxs-lookup"><span data-stu-id="d81e2-111">For more information, see [Cloud-based load testing service end of life](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d81e2-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="d81e2-112">Prerequisites</span></span>

<span data-ttu-id="d81e2-113">このトピックの手順を完了する前に、次の前提条件が満たされていることを確認してください:</span><span class="sxs-lookup"><span data-stu-id="d81e2-113">Before you can complete the steps in this topic, verify that the following prerequisites are met:</span></span>

- <span data-ttu-id="d81e2-114">自身の Microsoft Azure サブスクリプションに、プラットフォーム更新プログラム 21 以降の開発環境があります。</span><span class="sxs-lookup"><span data-stu-id="d81e2-114">You have a development environment that has platform update 21 or later in own your Microsoft Azure subscription</span></span>
- <span data-ttu-id="d81e2-115">開発環境には Microsoft Visual Studio Enterprise Edition があります。</span><span class="sxs-lookup"><span data-stu-id="d81e2-115">You have Microsoft Visual Studio Enterprise edition in a development environment.</span></span>
- <span data-ttu-id="d81e2-116">開発環境と同じリリース (アプリケーション バージョンとプラットフォーム更新プログラム) の階層 2 以上のサンドボックスがあります。</span><span class="sxs-lookup"><span data-stu-id="d81e2-116">You have a tier-2 or above sandbox that has the same release (application version and platform update) as your development environment.</span></span>
- <span data-ttu-id="d81e2-117">[タスク レコーダーおよびパフォーマンス SDK を使用したシングル ユーザー テスト](single-user-test-perf-sdk.md) のすべての手順と、 [パフォーマンス SDK およびローカル テスト コントローラーを使用したマルチ ユーザー テスト](multi-user-testing-local-test-controller.md) の "ローカル テスト コントローラーを使用したマルチユーザー テストの実行" を除くすべての手順を完了しました。</span><span class="sxs-lookup"><span data-stu-id="d81e2-117">You've completed all the steps in [Single-user testing with Task recorder and the Performance SDK](single-user-test-perf-sdk.md) and all the steps except "Run multi-user testing with local test controller" in [Multi-user testing with the Performance SDK and a local test controller](multi-user-testing-local-test-controller.md).</span></span>

## <a name="prepare-the-perfsdksample-solution-for-multi-user-testing"></a><span data-ttu-id="d81e2-118">マルチユーザー テスト用の PerfSDKSample ソリューションの準備</span><span class="sxs-lookup"><span data-stu-id="d81e2-118">Prepare the PerfSDKSample solution for multi-user testing</span></span>

1. <span data-ttu-id="d81e2-119">開発環境で Microsoft Visual Studio を Azure DevOps プロジェクトに接続します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-119">Connect Microsoft Visual Studio in a development environment to an Azure DevOps project.</span></span>

    <span data-ttu-id="d81e2-120">[![[Team Foundation Serverに 接続] ダイアログ ボックス](./media/perfsdk-azuredevops-01.png)](./media/perfsdk-azuredevops-01.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-120">[![Connect to Team Foundation Server dialog box](./media/perfsdk-azuredevops-01.png)](./media/perfsdk-azuredevops-01.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="d81e2-121">Azure DevOps サーバーを追加する場合は、**https://\<YourAzureDevOpsAccount\>.visualstudio.com** を使用します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-121">When you add the Azure DevOps server, use **https://\<YourAzureDevOpsAccount\>.visualstudio.com**.</span></span>

2. <span data-ttu-id="d81e2-122">Azure DevOps プロジェクト ダッシュボードで **Visual Studio で開く** を選択し、**プロンプト ウィンドウで許可** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-122">On your Azure DevOps project dashboard, select **Open in Visual Studio**, and then select **Allow in prompted window**.</span></span>

    <span data-ttu-id="d81e2-123">[![Azure プロジェクト ダッシュボード](./media/perfsdk-azuredevops-02.png)](./media/perfsdk-azuredevops-02.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-123">[![Azure Project dashboard](./media/perfsdk-azuredevops-02.png)](./media/perfsdk-azuredevops-02.png)</span></span>

3. <span data-ttu-id="d81e2-124">Visual Studio が開いたら、管理者として実行していることを確認します。そうでない場合は、それを閉じて管理者として再度開いてください。</span><span class="sxs-lookup"><span data-stu-id="d81e2-124">After Visual Studio is opened, verify that you're running it as an admin. If you aren't, close it, and then reopen it as an admin.</span></span>
4. <span data-ttu-id="d81e2-125">K:\PerfSDK\PerfSDKLocalDirectory\SampleProject に移動して、ファイル、**vsonline.testsettings** を変更します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-125">Go to K:\PerfSDK\PerfSDKLocalDirectory\SampleProject, and change the file, **vsonline.testsettings**.</span></span>
5. <span data-ttu-id="d81e2-126">**テストの設定** ダイアログ ボックスの **一般** タブで、**Visual Studio Team Services を使用したテストの実行** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-126">In the **Test Settings** dialog box, on the **General** tab, select the **Run tests using Visual Studio Team Services** option.</span></span>
6. <span data-ttu-id="d81e2-127">**配置** タブで、 すべてのフィールド設定を [パフォーマンス SDK およびローカル テスト コントローラーを使用したマルチ ユーザー テスト](multi-user-testing-local-test-controller.md) で設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="d81e2-127">On the **Deployment** tab, leave all the fields set as they were set in [Multi-user testing with the Performance SDK and a local test controller](multi-user-testing-local-test-controller.md).</span></span>

    <span data-ttu-id="d81e2-128">[![配置タブ](./media/perfsdk-azuredevops-04.png)](./media/perfsdk-azuredevops-04.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-128">[![Deployment tab](./media/perfsdk-azuredevops-04.png)](./media/perfsdk-azuredevops-04.png)</span></span>

7. <span data-ttu-id="d81e2-129">**設定とクリーンアップ スクリプト** タブで、 **Visual Studio Online** フォルダの **setup.cmd** ファイルへ **設定スクリプト** フィールドをポイントします。</span><span class="sxs-lookup"><span data-stu-id="d81e2-129">On the **Setup and Cleanup Scripts** tab, point the **Setup script** field to the **setup.cmd** file under the **Visual Studio Online** folder.</span></span>

    <span data-ttu-id="d81e2-130">[![設定とクリーンアップ スクリプト タブ](./media/perfsdk-azuredevops-05.png)](./media/perfsdk-azuredevops-05.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-130">[![Setup and Cleanup Scripts tab](./media/perfsdk-azuredevops-05.png)](./media/perfsdk-azuredevops-05.png)</span></span>

8. <span data-ttu-id="d81e2-131">**追加設定** タブで、すべてのフィールド設定を [パフォーマンス SDK およびローカル テスト コントローラーを使用したマルチ ユーザー テスト](multi-user-testing-local-test-controller.md) で設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="d81e2-131">On the **Additional Settings** tab, leave all the fields set as they were set in [Multi-user testing with the Performance SDK and a local test controller](multi-user-testing-local-test-controller.md).</span></span>

    <span data-ttu-id="d81e2-132">[![追加設定タブ](./media/perfsdk-azuredevops-06.png)](./media/perfsdk-azuredevops-06.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-132">[![Additional settings tab](./media/perfsdk-azuredevops-06.png)](./media/perfsdk-azuredevops-06.png)</span></span>

9. <span data-ttu-id="d81e2-133">**適用して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-133">Select **Apply and Close**.</span></span>

## <a name="run-multi-user-testing-by-using-azure-devops"></a><span data-ttu-id="d81e2-134">Azure DevOps を使用したマルチユーザー テストの実行</span><span class="sxs-lookup"><span data-stu-id="d81e2-134">Run multi-user testing by using Azure DevOps</span></span>

1. <span data-ttu-id="d81e2-135">Visual Studio で **SampleLoadTest.loadtest** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d81e2-135">In Visual Studio, open **SampleLoadTest.loadtest**.</span></span>
2. <span data-ttu-id="d81e2-136">**負荷テストの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-136">Select **Run Load Test**.</span></span>

    <span data-ttu-id="d81e2-137">[![負荷テストの実行オプション](./media/perfsdk-azuredevops-07.png)](./media/perfsdk-azuredevops-07.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-137">[![Run Load Test option](./media/perfsdk-azuredevops-07.png)](./media/perfsdk-azuredevops-07.png)</span></span>

    <span data-ttu-id="d81e2-138">負荷テストが実行され、グラフに進行状況が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d81e2-138">The load test is run, and a chart shows its progress.</span></span>    
   
   <span data-ttu-id="d81e2-139">[![SampleLoadTestLoadTest の進行状況グラフ](./media/perfsdk-azuredevops-08.png)](./media/perfsdk-azuredevops-08.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-139">[![SampleLoadTestLoadTest progress chart](./media/perfsdk-azuredevops-08.png)](./media/perfsdk-azuredevops-08.png)</span></span>

    <span data-ttu-id="d81e2-140">[![SampleLoadTestLoadTest の進行状況グラフの続行](./media/perfsdk-azuredevops-09.png)](./media/perfsdk-azuredevops-09.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-140">[![SampleLoadTestLoadTest progress chart continued](./media/perfsdk-azuredevops-09.png)](./media/perfsdk-azuredevops-09.png)</span></span>

3. <span data-ttu-id="d81e2-141">テスト出力を確認します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-141">Review the test output.</span></span>

    <span data-ttu-id="d81e2-142">[![テスト出力画面 1](./media/perfsdk-azuredevops-10.png)](./media/perfsdk-azuredevops-10.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-142">[![Test output screen 1](./media/perfsdk-azuredevops-10.png)](./media/perfsdk-azuredevops-10.png)</span></span>

    <span data-ttu-id="d81e2-143">[![テスト出力画面 2](./media/perfsdk-azuredevops-11.png)](./media/perfsdk-azuredevops-11.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-143">[![Test output screen 2](./media/perfsdk-azuredevops-11.png)](./media/perfsdk-azuredevops-11.png)</span></span>

    <span data-ttu-id="d81e2-144">[![テスト出力画面 3](./media/perfsdk-azuredevops-12.png)](./media/perfsdk-azuredevops-12.png)</span><span class="sxs-lookup"><span data-stu-id="d81e2-144">[![Test output screen 3](./media/perfsdk-azuredevops-12.png)](./media/perfsdk-azuredevops-12.png)</span></span>

## <a name="tips"></a><span data-ttu-id="d81e2-145">ヒント</span><span class="sxs-lookup"><span data-stu-id="d81e2-145">Tips</span></span>

<span data-ttu-id="d81e2-146">ローカル テスト コントローラーと Azure DevOps 間でマルチユーザー テストを切り替えるには、それぞれに **testsettings** のコピーを作成して **有効なテストの設定** として必要なコピーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d81e2-146">To switch multi-user testing between the local test controller and Azure DevOps, create a copy of **testsettings** for each, and then select the copy that you want as **Active Test Settings**.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d81e2-147">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d81e2-147">Troubleshooting</span></span>

<span data-ttu-id="d81e2-148">パフォーマンス SDK を使用するシングル ユーザーまたはマルチ ユーザーのテストの詳細については、[パフォーマンス SDK によるシングルユーザーまたはマルチユーザーのテストに関するトラブルシューティングガイド](troubleshoot-perf-sdk-user-testing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d81e2-148">For information about single-user or multi-user testing that uses the Performance SDK, see [Troubleshooting guide for single-user or multi-user testing with the Performance SDK](troubleshoot-perf-sdk-user-testing.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]