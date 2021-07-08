---
title: 電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング
description: このトピックでは、パフォーマンス上の問題をトラブルシューティングするために電子申告 (ER) のパフォーマンス追跡機能を使用する方法について説明します。
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295576"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="3c835-103">パフォーマンス上の問題をトラブルシューティングするため ER 形式の実行を追跡します</span><span class="sxs-lookup"><span data-stu-id="3c835-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3c835-104">電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションをデザインするプロセスの一部として、アプリケーションからデータを取得し、生成される出力に入力したりするのに使用される方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="3c835-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="3c835-105">ER パフォーマンス追跡機能を使用すると、ER 形式の実行に関する詳細の収集や、それらを使用してパフォーマンスの問題をトラブルシューティングするのにかかる時間と費用を大幅に削減できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="3c835-106">このチュートリアルでは、実行される ER 形式のパフォーマン追跡を実行する方法、およびこれらの追跡情報を使用してパフォーマンスを向上する方法についてのガイドラインを示します。</span><span class="sxs-lookup"><span data-stu-id="3c835-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3c835-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="3c835-107">Prerequisites</span></span>

<span data-ttu-id="3c835-108">このチュートリアルの例を完了するには、次のアクセスが必要です:</span><span class="sxs-lookup"><span data-stu-id="3c835-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="3c835-109">次のいずれかのロールににアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3c835-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="3c835-110">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="3c835-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="3c835-111">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="3c835-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="3c835-112">システム管理者</span><span class="sxs-lookup"><span data-stu-id="3c835-112">System administrator</span></span>

- <span data-ttu-id="3c835-113">次のいずれかの役割で、アプリケーションと同じテナントに対してプロビジョニングされている規制コンフィギュレーション サービス (RCS) のインスタンスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3c835-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="3c835-114">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="3c835-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="3c835-115">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="3c835-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="3c835-116">システム管理者</span><span class="sxs-lookup"><span data-stu-id="3c835-116">System administrator</span></span>

<span data-ttu-id="3c835-117">次のファイルをローカルにダウンロードして保存する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="3c835-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="3c835-118">ファイル</span><span class="sxs-lookup"><span data-stu-id="3c835-118">File</span></span>                                  | <span data-ttu-id="3c835-119">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="3c835-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="3c835-120">model.version.1 のパフォーマンス追跡</span><span class="sxs-lookup"><span data-stu-id="3c835-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="3c835-121">ER データ モデル構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="3c835-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="3c835-122">metadata.version.1 のパフォーマンス追跡</span><span class="sxs-lookup"><span data-stu-id="3c835-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="3c835-123">ER メタデータ構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="3c835-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="3c835-124">mapping.version.1.1 のパフォーマンス追跡</span><span class="sxs-lookup"><span data-stu-id="3c835-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="3c835-125">ER モデル マッピング構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="3c835-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="3c835-126">format.version.1.1 のパフォーマンス追跡</span><span class="sxs-lookup"><span data-stu-id="3c835-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="3c835-127">ER フォーマット構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="3c835-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="3c835-128">ER パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3c835-128">Configure ER parameters</span></span>

<span data-ttu-id="3c835-129">アプリケーションで生成された各 ER パフォーマンス追跡は、実行ログ レコードの添付ファイルとして保管されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="3c835-130">これらの添付ファイルを管理するには、ドキュメント管理 (DM) フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="3c835-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="3c835-131">ER パラメーターを事前にコンフィギュレーションして、パフォーマンス追跡を添付するのに使用する DM ドキュメント タイプを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c835-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="3c835-132">**電子申告** ワークスペースで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="3c835-133">次に、**電子申告パラメーター** ページの **添付ファイル** タブの **その他** フィールドで、パフォーマンス追跡に使用する DM ドキュメント タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![電子申告のパラメーター ページ](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="3c835-135">**その他** ルックアップ フィールドで使用可能にするには、DM ドキュメント タイプを **ドキュメント タイプ** ページ (**組織管理 \> ドキュメント管理 \> ドキュメント タイプ**): で次のようにコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c835-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="3c835-136">**クラス:** 添付ファイル</span><span class="sxs-lookup"><span data-stu-id="3c835-136">**Class:** Attach file</span></span>
- <span data-ttu-id="3c835-137">**グループ:** ファイル</span><span class="sxs-lookup"><span data-stu-id="3c835-137">**Group:** File</span></span>

![ドキュメント タイプ ページ](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="3c835-139">DM 添付ファイルは会社固有であるため、選択したドキュメント タイプは、現在のインスタンスのすべての会社で使用可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c835-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="3c835-140">RCS パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3c835-140">Configure RCS parameters</span></span>

<span data-ttu-id="3c835-141">生成される ER パフォーマンス追跡は、ER 形式デザイナーと ER マッピング デザイナーを使用して、分析用に RCS にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="3c835-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="3c835-142">ER パフォーマンス追跡は ER 形式に関連する実行ログ レコードの添付ファイルとして格納されるため、RCS パラメーターを事前にコンフィギュレーションして、パフォーマンス追跡の添付に使用する DM ドキュメント タイプを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c835-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="3c835-143">会社用にプロビジョニングされた RCS のインスタンスの、**電子申告** ワークスペースで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="3c835-144">次に、**電子申告パラメーター** ページの **添付ファイル** タブの **その他** フィールドで、パフォーマンス追跡に使用する DM ドキュメント タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![RCS の電子申告パラメーター ページ](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="3c835-146">**その他** ルックアップ フィールドで使用可能にするには、DM ドキュメント タイプを **ドキュメント タイプ** ページ (**組織管理 \> ドキュメント管理 \> ドキュメント タイプ**): で次のようにコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c835-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="3c835-147">**クラス:** 添付ファイル</span><span class="sxs-lookup"><span data-stu-id="3c835-147">**Class:** Attach file</span></span>
- <span data-ttu-id="3c835-148">**グループ:** ファイル</span><span class="sxs-lookup"><span data-stu-id="3c835-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="3c835-149">ER ソリューションのデザイン</span><span class="sxs-lookup"><span data-stu-id="3c835-149">Design an ER solution</span></span>

<span data-ttu-id="3c835-150">仕入先トランザクションを表示する新しいレポートを生成するため、新しい ER ソリューションのデザインを開始したとします。</span><span class="sxs-lookup"><span data-stu-id="3c835-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="3c835-151">現時点では、選択した仕入先のトランザクションは **仕入先トランザクション** ページ (**買掛金勘定 \> 仕入先 \> すべての仕入先** に移動し、仕入先を選択してから、アクション ウィンドウの **仕入先** タブの **トランザクション** グループで、**トランザクション** を選択します) で検索できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="3c835-152">ただし、XML 形式の 1 つの電子ドキュメントで、すべての仕入先トランザクションを同時に処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c835-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="3c835-153">このソリューションは、必要なデータ モデル、メタデータ、モデル マッピング、および形式コンポーネントを含むいくつかの ER コンフィギュレーションで構成されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="3c835-154">会社用にプロビジョニングされた RCS のインスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="3c835-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="3c835-155">このチュートリアルでは、サンプル会社 **Litware, Inc.** のコンフィギュレーションを作成または変更します。</span><span class="sxs-lookup"><span data-stu-id="3c835-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="3c835-156">そのため、このコンフィギュレーション プロバイダーが RCS に追加され、有効として選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="3c835-157">手順については、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="3c835-158">**電子レポート** ワークスペースで、**レポート コンフィギュレーション** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="3c835-159">**構成** ページで、前提条件としてダウンロードした ER コンフィギュレーションを RCS に次の順序でインポートします: データ モデル、メタデータ、モデル マッピング、フォーマット。</span><span class="sxs-lookup"><span data-stu-id="3c835-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="3c835-160">各コンフィギュレーションについて、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3c835-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="3c835-161">アクション ウィンドウで、**交換 \> XML ファイルからロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="3c835-162">**参照** を選択して、必要な ER コンフィギュレーションに適したファイルを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="3c835-163">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-163">Select **OK**.</span></span>

    ![RCS の構成ページ](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="3c835-165">ER ソリューションを実行して追跡実行する</span><span class="sxs-lookup"><span data-stu-id="3c835-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="3c835-166">ER ソリューションの最初のバージョンのデザインが完了したとします。</span><span class="sxs-lookup"><span data-stu-id="3c835-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="3c835-167">これにより、インスタンスでテストを行い、実行パフォーマンスを分析できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="3c835-168">RCS から ER コンフィギュレーションの Finance and Operations へのインポート</span><span class="sxs-lookup"><span data-stu-id="3c835-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="3c835-169">アプリケーション インスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="3c835-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="3c835-170">このチュートリアルでは、RCS インスタンス (ER コンポーネントを設計する場所) から、インスタンス (テストして最後に使用する場所) にコンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="3c835-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="3c835-171">したがって、必要なコンポーネントがすべて準備されたことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c835-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="3c835-172">手順については、[規制コンフィギュレーション サービス (RCS) からの電子申告 (ER) 構成のインポート](rcs-download-configurations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="3c835-173">これらの手順に従って、コンフィギュレーションを RCS からアプリケーションにインポートします。</span><span class="sxs-lookup"><span data-stu-id="3c835-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="3c835-174">**電子申告** ワークスペースの、**Litware, inc.** コンフィギュレーション プロバイダーのタイルで、**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="3c835-175">**コンフィギュレーション リポジトリ** ページで、**RCS** タイプのリポジトリを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="3c835-176">**コンフィギュレーション** クイック タブで、**パフォーマンス追跡形式** コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="3c835-177">**バージョン** クイック タブで、選択したコンフィギュレーションのバージョン **1.1** を選択し、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![レポジトリ ページのコンフィギュレーション](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="3c835-179">データ モデルとモデル マッピングコン フィギュレーションの対応するバージョンは、インポートされた ER 形式コンフィギュレーションの前提条件として自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="3c835-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="3c835-180">ER パフォーマンス追跡を有効にする</span><span class="sxs-lookup"><span data-stu-id="3c835-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="3c835-181">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3c835-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="3c835-182">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="3c835-183">**ユーザー パラメーター** ダイアログ ボックスの **実行トレース** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3c835-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="3c835-184">**実行トレース形式** フィールドで、実行詳細が ER 形式およびマッピング要素で格納されるよう、生成済パフォーマンス追跡の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c835-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="3c835-185">**デバッグ トレース形式** – 実行時間が短い ER 形式を対話的に実行する場合は、この値を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="3c835-186">次に、ER 形式の実行に関する詳細のコレクションが開始されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="3c835-187">この値が選択されている場合、パフォーマンス追跡によって、次のアクションに費やされた時間に関する情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="3c835-188">データを取得するために呼び出されるモデル マッピングで各データ ソースを実行する</span><span class="sxs-lookup"><span data-stu-id="3c835-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="3c835-189">生成される出力にデータを入力するため各項目の形式を処理する</span><span class="sxs-lookup"><span data-stu-id="3c835-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="3c835-190">**デバッグ トレース形式** 値を選択すると、ER 操作デザイナーで追跡の内容を分析できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="3c835-191">そこで、追跡に示されている ER 形式またはマッピング要素を表示できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="3c835-192">**集計済デバッグ トレース形式** – バッチ モードで実行時間が長い ER 形式を実行する場合は、この値を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="3c835-193">次に、ER 形式の実行に関する集計詳細のコレクションが開始されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="3c835-194">この値が選択されている場合、パフォーマンス追跡によって、次のアクションに費やされた時間に関する情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="3c835-195">データを取得するために呼び出されるモデル マッピングで各データ ソースを実行する</span><span class="sxs-lookup"><span data-stu-id="3c835-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="3c835-196">データを取得するために呼び出される形式マッピングで各データ ソースを実行する</span><span class="sxs-lookup"><span data-stu-id="3c835-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="3c835-197">生成される出力にデータを入力するため各項目の形式を処理する</span><span class="sxs-lookup"><span data-stu-id="3c835-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="3c835-198">**集計済デバッグ トレース形式** の値は、Microsoft Dynamics 365 Finance バージョン 10.0.20 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="3c835-199">ER 形式デザイナーおよび ER モデル マッピング デザイナーでは、単一のコンポーネントの合計実行時間を表示できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="3c835-200">さらに、追跡には実行回数、1 回の実行の最小時間と最大時間など、実行に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c835-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="3c835-201">この追跡は、追跡されたコンポーネント パスに基づいて収集されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="3c835-202">したがって、単一の親コンポーネントに名前のない複数の子コンポーネントが含まれる場合、または複数の子コンポーネントの名前が同じ場合、統計が正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="3c835-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="3c835-203">次のオプションを **はい** に設定して、ER モデル マッピングおよび ER フォーマット コンポーネントの実行に関する具体的な詳細を収集します。</span><span class="sxs-lookup"><span data-stu-id="3c835-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="3c835-204">**クエリ統計情報の収集** – このオプションが有効になっている場合、パフォーマンス追跡では次の情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="3c835-205">データ ソースによって作成されたデータベース呼び出し数</span><span class="sxs-lookup"><span data-stu-id="3c835-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="3c835-206">データベースに対する複製呼び出し数</span><span class="sxs-lookup"><span data-stu-id="3c835-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="3c835-207">データベース呼び出しを行うために使用された SQL ステートメントの詳細</span><span class="sxs-lookup"><span data-stu-id="3c835-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="3c835-208">**キャッシュのアクセスの追跡** – このオプションが有効になっている場合、パフォーマンス追跡では ER モデル マッピングのキャッシュ使用に関する情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="3c835-209">**データ アクセスの追跡** – このオプションが有効になっている場合、パフォーマンス追跡では、レコード リスト タイプの実行されたデータ ソースに対するデータベースへの呼び出し回数に関する情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="3c835-210">**リスト列挙の追跡** – このオプションが有効になっている場合、パフォーマンス追跡では、レコード リスト タイプのデータ ソースから要求されたレコード数に関する情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3c835-211">**ユーザー パラメーター** ダイアログ ボックスのパラメーターは、ユーザーと現在の会社に固有です。</span><span class="sxs-lookup"><span data-stu-id="3c835-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![ユーザー パラメーター ダイアログ ボックス](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="3c835-213">ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="3c835-213">Run the ER format</span></span>

1. <span data-ttu-id="3c835-214">**DEMF** 会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="3c835-215">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3c835-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="3c835-216">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス追跡形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="3c835-217">アクション ウィンドウで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="3c835-218">生成されるファイルによって、6 つの仕入先の 265 トランザクションに関する情報が表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="3c835-219">実行追跡の確認</span><span class="sxs-lookup"><span data-stu-id="3c835-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a> <span data-ttu-id="3c835-220">アプリケーションから生成された追跡のエクスポート</span><span class="sxs-lookup"><span data-stu-id="3c835-220">Export the generated trace from the application</span></span>

<span data-ttu-id="3c835-221">パフォーマンス追跡は、ソースの ER 形式から切り離され、外部の zip ファイルにシリアル化されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="3c835-222">**組織管理 \> 電子申告 \> 構成デバッグ ログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3c835-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="3c835-223">**電子申告実行ログ** ページ、左ウィンドウの、**コンフィギュレーション名** フィールドで、**パフォーマンス追跡形式** を選択し、**パフォーマンス追跡形式** コンフィギュレーションの実行によって生成されたログ レコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="3c835-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="3c835-224">ページの右上隅にある **添付ファイル** ボタン (紙クリップ記号) を選択するか、**Ctrl + Shift + A** を押します。</span><span class="sxs-lookup"><span data-stu-id="3c835-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![電子申告実行ログ ページの添付ファイル ボタン](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="3c835-226">**電子申告実行ログの添付ファイル** ページの、アクション ウィンドウで、**開く** を選択してパフォーマンス追跡を zip ファイルとして取得し、ローカルに保管します。</span><span class="sxs-lookup"><span data-stu-id="3c835-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![電子申告実行ログの添付ファイル](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="3c835-228">生成されるトレースは、**GUID** 形式のみの固有のレポート ID を通じて、ソース ER レポートを参照しています。</span><span class="sxs-lookup"><span data-stu-id="3c835-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="3c835-229">形式のバージョン番号付けは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="3c835-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="3c835-230">実行される ER 形式と ER モデル マッピングに対して生成されたパフォーマンス追跡間の関連付けは、使用されたルート記述子と共通データ モデルに基づいていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="3c835-231">形式のバージョン番号付けおよびモデル マッピングは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="3c835-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="3c835-232">モデル マッピングに対する **モデル マッピングの既定値** フラグの設定も考慮されません。</span><span class="sxs-lookup"><span data-stu-id="3c835-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a> <span data-ttu-id="3c835-233">生成された追跡を RCS にインポートします</span><span class="sxs-lookup"><span data-stu-id="3c835-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="3c835-234">RCS の、**電子レポート** ワークスペースで、**レポート コンフィギュレーション** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="3c835-235">**構成** ページのコンフィギュレーション ツリーで、**パフォーマンス追跡モデル** 項目を展開し、**パフォーマンス追跡形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="3c835-236">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="3c835-237">**形式デザイナー** の、アクション ウィンドウで、**パフォーマンス追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="3c835-238">**パフォーマンス追跡結果の設定** ダイアログ ボックスで、**パフォーマンス追跡のインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="3c835-239">**参照** を選択し、先ほどインポートした zip ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="3c835-240">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-240">Select **OK**.</span></span>

    ![RCS のパフォーマンス追跡結果の設定ダイアログ ボックス](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="3c835-242">RCS での分析に対するパフォーマンス追跡の使用 – 形式実行</span><span class="sxs-lookup"><span data-stu-id="3c835-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="3c835-243">RCS の、**形式デザイナー** ページで、**展開/折りたたみ** を選択してすべての形式項目の内容を展開します。</span><span class="sxs-lookup"><span data-stu-id="3c835-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="3c835-244">現在の形式の一部の項目に関して、追加情報が表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="3c835-245">形式項目を使用して生成された出力にデータを入力するのに費やした実際の時間</span><span class="sxs-lookup"><span data-stu-id="3c835-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="3c835-246">出力全体の生成に費やされた合計時間の割合で表される同じ時間</span><span class="sxs-lookup"><span data-stu-id="3c835-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![RCS の形式デザイナー ページ](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="3c835-248">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3c835-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="3c835-249">RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング</span><span class="sxs-lookup"><span data-stu-id="3c835-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="3c835-250">RCS、**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス追跡マッピング** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="3c835-251">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="3c835-252">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3c835-252">Select **Designer**.</span></span>
4. <span data-ttu-id="3c835-253">**モデル マッピング デザイナー** ページの、アクション ウィンドウで、**パフォーマンス追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="3c835-254">事前にインポートした追跡を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="3c835-255">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-255">Select **OK**.</span></span>

<span data-ttu-id="3c835-256">現在のモデル マッピングの一部のデータ ソース項目に関する、新しい情報が利用可能になることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="3c835-257">データ ソースを使用してデータの取得に費やした実際の時間</span><span class="sxs-lookup"><span data-stu-id="3c835-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="3c835-258">モデル マッピング全体の実行に費やされた合計時間の割合で表される同じ時間</span><span class="sxs-lookup"><span data-stu-id="3c835-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="3c835-259">VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースの実行中は、現在のモデル マッピングがデータベース要求を重複することを ER から通知されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="3c835-260">この重複が発生するのは、仕入先トランザクションの一覧が、反復する仕入先レコードごとに 2 回呼び出されるためです。</span><span class="sxs-lookup"><span data-stu-id="3c835-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="3c835-261">1 回の呼び出しでは、構成されたバインディングに基づいて、データ モデルの各トランザクションの詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="3c835-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="3c835-262">もう 1 回の呼び出しで、データ モデルの仕入先ごとに計算されたトランザクション数を入力します。</span><span class="sxs-lookup"><span data-stu-id="3c835-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![RCS のモデル マッピング デザイナー ページで重複したデータベース要求に関するメッセージ](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="3c835-264">**\[Q:530\]** の値は、テーブルから VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースにレコードを返すため、VendTrans テーブルが 530 回呼び出されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="3c835-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="3c835-265">**\[530\]** の値は、VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースが、そのデータ ソースからレコードを返し、データ モデルで詳細を入力するために 530 回呼び出されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="3c835-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="3c835-266">265 トランザクションの詳細を取得するための呼び出し数を減らし、モデルマッピングのパフォーマンスを向上させるため、VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースに対してキャッシュを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3c835-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="3c835-267">それは LedgerTransTypeList データ ソースに対して行われる呼び出し数を減らすのにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3c835-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="3c835-268">このデータ ソースは、**LedgerTransType** 列挙の各値をラベルに関連付けるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3c835-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="3c835-269">このデータ ソースを使用すると、適切なラベルを検索して、各仕入先トランザクションのデータ モデルに入力できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="3c835-270">このデータ ソースへの現在の呼び出し数 (9,027) は、265 トランザクションに対して非常に高くなっています。</span><span class="sxs-lookup"><span data-stu-id="3c835-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![データ ソースへの 9,027 の呼び出しを示す、RCS のモデル マッピング デザイナー ページ](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="3c835-272">実行追跡からの情報に基づいてモデル マッピングを改善する</span><span class="sxs-lookup"><span data-stu-id="3c835-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="3c835-273">モデル マッピングのロジックを変更する</span><span class="sxs-lookup"><span data-stu-id="3c835-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="3c835-274">次の手順に従ってキャッシュを使用すると、データベースへの重複呼び出しを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="3c835-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="3c835-275">RCS、**モデル マッピング デザイナー** ページの、**データ ソース** ウィンドウで、**VendTable** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="3c835-276">**キャッシュ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="3c835-277">**VendTable** 項目を展開し、VendTable データ ソース (**\<関係** 項目) の一対多の関係の一覧を展開してから、**VendTrans.VendTable\_AccountNum** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="3c835-278">**キャッシュ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-278">Select **Cache**.</span></span>

    ![重複呼び出しを防ぐためのキャッシュ設定](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="3c835-280">LedgerTransTypeList データ ソースを VendTable データ ソースのスコープに移動するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3c835-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="3c835-281">**データ ソース タイプ** ウィンドウで、**関数** 項目を展開し、**計算済フィールド** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="3c835-282">**データ ソース** ウィンドウで、**VendTable** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="3c835-283">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-283">Select **Add**.</span></span>
    4. <span data-ttu-id="3c835-284">**名前** フィールドで、**\$TransType** を入力します。</span><span class="sxs-lookup"><span data-stu-id="3c835-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="3c835-285">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="3c835-286">**式** フィールドに、**LedgerTransTypeList** を入力します。</span><span class="sxs-lookup"><span data-stu-id="3c835-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="3c835-287">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-287">Select **Save**.</span></span>
    8. <span data-ttu-id="3c835-288">**式の編集** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3c835-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="3c835-289">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3c835-289">Click **OK**.</span></span>

3. <span data-ttu-id="3c835-290">次の手順に従って、**\$TransType** フィールドをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="3c835-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="3c835-291">**LedgerTransTypeList** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="3c835-292">**キャッシュ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="3c835-293">**VendTable.\$TransType** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="3c835-294">**キャッシュ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-294">Select **Cache**.</span></span>

    ![$TransType フィールドのキャッシュ設定](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="3c835-296">次の手順に従って **\$TransTypeRecord** フィールドを変更し、キャッシュされた **\$TransType** フィールドを使用開始できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3c835-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="3c835-297">**データ ソース** ウィンドウで、**VendTable** 項目を展開し、**\<関係** 項目を展開し、**VendTrans.VendTable\_AccountNum** 項目を展開してから、**VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="3c835-298">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="3c835-299">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="3c835-300">**式** フィールドで、次の式を検索します。</span><span class="sxs-lookup"><span data-stu-id="3c835-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="3c835-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="3c835-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="3c835-302">**式** フィールドで、次の式を入力します。</span><span class="sxs-lookup"><span data-stu-id="3c835-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="3c835-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="3c835-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="3c835-304">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-304">Select **Save**.</span></span>
    7. <span data-ttu-id="3c835-305">**式の編集** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3c835-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="3c835-306">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-306">Select **OK**.</span></span>

5. <span data-ttu-id="3c835-307">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-307">Select **Save**.</span></span>
6. <span data-ttu-id="3c835-308">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3c835-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="3c835-309">**モデル マッピング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3c835-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="3c835-310">ER モデル マッピングの変更されたバージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="3c835-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="3c835-311">RCS、**コンフィギュレーション** ページの、**バージョン** クイック タブで、**パフォーマンス追跡マッピング** コンフィギュレーションのバージョン **1.2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="3c835-312">**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-312">Select **Change status**.</span></span>
3. <span data-ttu-id="3c835-313">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="3c835-314">変更された ER モデル マッピング コンフィギュレーションを RCS からアプリケーションにインポートする</span><span class="sxs-lookup"><span data-stu-id="3c835-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="3c835-315">このトピックの前にある [RCS から ER コンフィギュレーションを Finance and Operations にインポートする](#import-configuration) セクションでこの手順を繰り返し、**パフォーマンス トレース マッピング** コンフィギュレーションのバージョン 1.2 をインポートします。</span><span class="sxs-lookup"><span data-stu-id="3c835-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="3c835-316">変更された ER ソリューションを実行して追跡実行する</span><span class="sxs-lookup"><span data-stu-id="3c835-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="3c835-317">ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="3c835-317">Run the ER format</span></span>

<span data-ttu-id="3c835-318">このトピックの先のセクション [ER 形式を実行する](#run-format) の手順を繰り返して、新しいパフォーマンス追跡を生成します。</span><span class="sxs-lookup"><span data-stu-id="3c835-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="3c835-319">実行トレースを使って作業する</span><span class="sxs-lookup"><span data-stu-id="3c835-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="3c835-320">アプリケーションから生成された追跡のエクスポート</span><span class="sxs-lookup"><span data-stu-id="3c835-320">Export the generated trace from the application</span></span>

<span data-ttu-id="3c835-321">このトピックの先のセクション [生成された追跡をアプリケーションからエクスポートする](#export-trace) の手順を繰り返して、新しいパフォーマンス追跡をローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="3c835-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="3c835-322">生成された追跡を RCS にインポートする</span><span class="sxs-lookup"><span data-stu-id="3c835-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="3c835-323">このトピックの先のセクション [生成された追跡を RCS にインポートする](#import-trace) の手順を繰り返して、新しいパフォーマンス追跡を RCS にインポートします。</span><span class="sxs-lookup"><span data-stu-id="3c835-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="3c835-324">RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング</span><span class="sxs-lookup"><span data-stu-id="3c835-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="3c835-325">このトピックの先のセクション [RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング](#use-trace) の手順を繰り返して、最新のパフォーマンス追跡を分析します。</span><span class="sxs-lookup"><span data-stu-id="3c835-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="3c835-326">モデル マッピングに対して行った調整によって、データベースへの重複するクエリが消去されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="3c835-327">このモデル マッピングのデータベース テーブルおよびデータ ソースへの呼び出し数も減少しました。</span><span class="sxs-lookup"><span data-stu-id="3c835-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="3c835-328">したがって、ER ソリューション全体のパフォーマンスが向上しました。</span><span class="sxs-lookup"><span data-stu-id="3c835-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![RCS の、モデル マッピング デザイナー ページで、VendTable データ ソースに関する情報を追跡します。](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="3c835-330">追跡情報で、VendTable データ ソースの **\[12\]** の値は、このデータソースが 12 回呼び出されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="3c835-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="3c835-331">**\[Q:6\]** の値は、6 つの呼び出しが VendTable テーブルへのデータベース呼び出しに変換されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="3c835-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="3c835-332">**\[C:6\]** の値は、データベースからフェッチされたレコードがキャッシュされ、その他の 6 つの呼び出しがキャッシュを使用して処理されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="3c835-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="3c835-333">LedgerTransTypeList データソースへの呼び出し数が 9,027 から 240 に減少したことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![RCS の モデル マッピング デザイナー ページで、LedgerTransTypeList データ ソースに関する情報を追跡します。](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="3c835-335">アプリケーションで実行追跡を確認する</span><span class="sxs-lookup"><span data-stu-id="3c835-335">Review the execution trace in the application</span></span>

<span data-ttu-id="3c835-336">RCS に加えて、一部のバージョンでは ER フレームワーク デザイナー経験に対する機能が提供される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3c835-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="3c835-337">これらのバージョンには **デザイン モードを有効にする** オプションがあり、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3c835-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="3c835-338">このオプションは **電子申告パラメーター** ページの **一般** タブで検索できます。このページは **電子申告** ワークスペースから開くことができます。</span><span class="sxs-lookup"><span data-stu-id="3c835-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![電子申告パラメーター ページでデザイン モード オプションを有効にする](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="3c835-340">これらのいずれかのバージョンを使用する場合は、生成されたパフォーマンス追跡の詳細をアプリケーションで直接分析できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="3c835-341">アプリケーションからエクスポートして RCS にインポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3c835-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="3c835-342">外部ツールを使用した実行追跡の確認</span><span class="sxs-lookup"><span data-stu-id="3c835-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="3c835-343">ユーザー パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3c835-343">Configure user parameters</span></span>

1. <span data-ttu-id="3c835-344">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3c835-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="3c835-345">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="3c835-346">**ユーザー パラメーター** ダイアログ ボックス、**実行トレース** セクションの、**実行トレース形式** フィールドで、**PerfView XML** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="3c835-347">ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="3c835-347">Run the ER format</span></span>

<span data-ttu-id="3c835-348">このトピックの先のセクション [ER 形式を実行する](#run-format) の手順を繰り返して、新しいパフォーマンス追跡を生成します。</span><span class="sxs-lookup"><span data-stu-id="3c835-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="3c835-349">Web ブラウザーによって、ダウンロード用の zip ファイルが提供されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="3c835-350">このファイルには、PerfView 形式のパフォーマンス追跡が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c835-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="3c835-351">次に、PerfView パフォーマンス分析ツールを使用して ER 形式実行の詳細を分析できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![PerfView 形式のパフォーマンス トレース情報](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="3c835-353">外部ツールを使用してデータベース クエリを含む実行トレースを確認する</span><span class="sxs-lookup"><span data-stu-id="3c835-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="3c835-354">ER フレームワークに行われた改善のため、PerfView 形式で生成されたパフォーマンスの追跡により、ER 形式の実行に関する詳細情報が提供されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3c835-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="3c835-355">Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.4 (2019 年 7 月) では、このトレースに、アプリケーション データベースに対して実行された SQL クエリの詳細を含めることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3c835-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="3c835-356">ユーザー パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3c835-356">Configure user parameters</span></span>

1. <span data-ttu-id="3c835-357">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3c835-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="3c835-358">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="3c835-359">**ユーザー パラメーター** ダイアログ ボックスの **実行トレース** セクションで、次のパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="3c835-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="3c835-360">**実行トレース形式** フィールドで、**PerfView XML** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c835-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="3c835-361">**クエリ統計情報の収集** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3c835-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="3c835-362">**クエリの追跡** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3c835-362">Set the **Trace query** option to **Yes**.</span></span>

    ![トレースの実行セクション、ユーザー パラメータ ダイアログボックス](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="3c835-364">ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="3c835-364">Run the ER format</span></span>

<span data-ttu-id="3c835-365">このトピックの先のセクション [ER 形式を実行する](#run-format) の手順を繰り返して、新しいパフォーマンス追跡を生成します。</span><span class="sxs-lookup"><span data-stu-id="3c835-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="3c835-366">Web ブラウザーによって、ダウンロード用の zip ファイルが提供されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c835-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="3c835-367">このファイルには、PerfView 形式のパフォーマンス追跡が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c835-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="3c835-368">次に、PerfView パフォーマンス分析ツールを使用して ER 形式実行の詳細を分析できます。</span><span class="sxs-lookup"><span data-stu-id="3c835-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="3c835-369">この追跡に、ER 形式の実行中における SQL データベース アクセスに関する詳細が含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3c835-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![PerfView で実行された ER 形式のトレース情報](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="3c835-371">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3c835-371">Additional resources</span></span>

- [<span data-ttu-id="3c835-372">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="3c835-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="3c835-373">パラメーター化された計算フィールドのデータ ソースを追加して、ER ソリューションのパフォーマンスを向上させる</span><span class="sxs-lookup"><span data-stu-id="3c835-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
