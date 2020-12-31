---
title: 電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング
description: このトピックでは、パフォーマンス上の問題をトラブルシューティングするために電子申告 (ER) のパフォーマンス追跡機能を使用する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 9a5f943a507483bb4c1bd7fe87c0d65353194a6e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687430"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="d224c-103">パフォーマンス上の問題をトラブルシューティングするため ER 形式の実行を追跡します</span><span class="sxs-lookup"><span data-stu-id="d224c-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d224c-104">電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションをデザインするプロセスの一部として、アプリケーションからデータを取得し、生成される出力に入力したりするのに使用される方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="d224c-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="d224c-105">ER パフォーマンス追跡機能を使用すると、ER 形式の実行に関する詳細の収集や、それらを使用してパフォーマンスの問題をトラブルシューティングするのにかかる時間と費用を大幅に削減できます。</span><span class="sxs-lookup"><span data-stu-id="d224c-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="d224c-106">このチュートリアルでは、実行される ER 形式のパフォーマン追跡を実行する方法、およびこれらの追跡情報を使用してパフォーマンスを向上する方法についてのガイドラインを示します。</span><span class="sxs-lookup"><span data-stu-id="d224c-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d224c-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="d224c-107">Prerequisites</span></span>

<span data-ttu-id="d224c-108">このチュートリアルの例を完了するには、次のアクセスが必要です:</span><span class="sxs-lookup"><span data-stu-id="d224c-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="d224c-109">次のいずれかのロールににアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d224c-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="d224c-110">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="d224c-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="d224c-111">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="d224c-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d224c-112">システム管理者</span><span class="sxs-lookup"><span data-stu-id="d224c-112">System administrator</span></span>

- <span data-ttu-id="d224c-113">次のいずれかの役割で、アプリケーションと同じテナントに対してプロビジョニングされている規制コンフィギュレーション サービス (RCS) のインスタンスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d224c-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="d224c-114">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="d224c-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="d224c-115">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="d224c-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d224c-116">システム管理者</span><span class="sxs-lookup"><span data-stu-id="d224c-116">System administrator</span></span>

<span data-ttu-id="d224c-117">次のファイルをローカルにダウンロードして保存する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="d224c-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="d224c-118">ファイル</span><span class="sxs-lookup"><span data-stu-id="d224c-118">File</span></span>                                  | <span data-ttu-id="d224c-119">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="d224c-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="d224c-120">model.version.1 のパフォーマンス追跡</span><span class="sxs-lookup"><span data-stu-id="d224c-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="d224c-121">ER データ モデル構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="d224c-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="d224c-122">metadata.version.1 のパフォーマンス追跡</span><span class="sxs-lookup"><span data-stu-id="d224c-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="d224c-123">ER メタデータ構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="d224c-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="d224c-124">mapping.version.1.1 のパフォーマンス追跡</span><span class="sxs-lookup"><span data-stu-id="d224c-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="d224c-125">ER モデル マッピング構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="d224c-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="d224c-126">format.version.1.1 のパフォーマンス追跡</span><span class="sxs-lookup"><span data-stu-id="d224c-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="d224c-127">ER フォーマット構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="d224c-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="d224c-128">ER パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d224c-128">Configure ER parameters</span></span>

<span data-ttu-id="d224c-129">アプリケーションで生成された各 ER パフォーマンス追跡は、実行ログ レコードの添付ファイルとして保管されます。</span><span class="sxs-lookup"><span data-stu-id="d224c-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="d224c-130">これらの添付ファイルを管理するには、ドキュメント管理 (DM) フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="d224c-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="d224c-131">ER パラメーターを事前にコンフィギュレーションして、パフォーマンス追跡を添付するのに使用する DM ドキュメント タイプを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d224c-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="d224c-132">**電子申告** ワークスペースで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="d224c-133">次に、**電子申告パラメーター** ページの **添付ファイル** タブの **その他** フィールドで、パフォーマンス追跡に使用する DM ドキュメント タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![電子申告のパラメーター ページ](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="d224c-135">**その他** ルックアップ フィールドで使用可能にするには、DM ドキュメント タイプを **ドキュメント タイプ** ページ (**組織管理 \> ドキュメント管理 \> ドキュメント タイプ**): で次のようにコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d224c-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="d224c-136">**クラス:** 添付ファイル</span><span class="sxs-lookup"><span data-stu-id="d224c-136">**Class:** Attach file</span></span>
- <span data-ttu-id="d224c-137">**グループ:** ファイル</span><span class="sxs-lookup"><span data-stu-id="d224c-137">**Group:** File</span></span>

![ドキュメント タイプ ページ](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="d224c-139">DM 添付ファイルは会社固有であるため、選択したドキュメント タイプは、現在のインスタンスのすべての会社で使用可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d224c-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="d224c-140">RCS パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d224c-140">Configure RCS parameters</span></span>

<span data-ttu-id="d224c-141">生成される ER パフォーマンス追跡は、ER 形式デザイナーと ER マッピング デザイナーを使用して、分析用に RCS にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="d224c-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="d224c-142">ER パフォーマンス追跡は ER 形式に関連する実行ログ レコードの添付ファイルとして格納されるため、RCS パラメーターを事前にコンフィギュレーションして、パフォーマンス追跡の添付に使用する DM ドキュメント タイプを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d224c-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="d224c-143">会社用にプロビジョニングされた RCS のインスタンスの、**電子申告** ワークスペースで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="d224c-144">次に、**電子申告パラメーター** ページの **添付ファイル** タブの **その他** フィールドで、パフォーマンス追跡に使用する DM ドキュメント タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![RCS の電子申告パラメーター ページ](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="d224c-146">**その他** ルックアップ フィールドで使用可能にするには、DM ドキュメント タイプを **ドキュメント タイプ** ページ (**組織管理 \> ドキュメント管理 \> ドキュメント タイプ**): で次のようにコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d224c-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="d224c-147">**クラス:** 添付ファイル</span><span class="sxs-lookup"><span data-stu-id="d224c-147">**Class:** Attach file</span></span>
- <span data-ttu-id="d224c-148">**グループ:** ファイル</span><span class="sxs-lookup"><span data-stu-id="d224c-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="d224c-149">ER ソリューションのデザイン</span><span class="sxs-lookup"><span data-stu-id="d224c-149">Design an ER solution</span></span>

<span data-ttu-id="d224c-150">仕入先トランザクションを表示する新しいレポートを生成するため、新しい ER ソリューションのデザインを開始したとします。</span><span class="sxs-lookup"><span data-stu-id="d224c-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="d224c-151">現時点では、選択した仕入先のトランザクションは **仕入先トランザクション** ページ (**買掛金勘定 \> 仕入先 \> すべての仕入先** に移動し、仕入先を選択してから、アクション ウィンドウの **仕入先** タブの **トランザクション** グループで、**トランザクション** を選択します) で検索できます。</span><span class="sxs-lookup"><span data-stu-id="d224c-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="d224c-152">ただし、XML 形式の 1 つの電子ドキュメントで、すべての仕入先トランザクションを同時に処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d224c-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="d224c-153">このソリューションは、必要なデータ モデル、メタデータ、モデル マッピング、および形式コンポーネントを含むいくつかの ER コンフィギュレーションで構成されます。</span><span class="sxs-lookup"><span data-stu-id="d224c-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="d224c-154">会社用にプロビジョニングされた RCS のインスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="d224c-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="d224c-155">このチュートリアルでは、サンプル会社 **Litware, Inc.** のコンフィギュレーションを作成または変更します。</span><span class="sxs-lookup"><span data-stu-id="d224c-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="d224c-156">そのため、このコンフィギュレーション プロバイダーが RCS に追加され、有効として選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="d224c-157">手順については、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="d224c-158">**電子レポート** ワークスペースで、**レポート コンフィギュレーション** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="d224c-159">**構成** ページで、前提条件としてダウンロードした ER コンフィギュレーションを RCS に次の順序でインポートします: データ モデル、メタデータ、モデル マッピング、フォーマット。</span><span class="sxs-lookup"><span data-stu-id="d224c-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="d224c-160">各コンフィギュレーションについて、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d224c-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="d224c-161">アクション ウィンドウで、**交換 \> XML ファイルからロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="d224c-162">**参照** を選択して、必要な ER コンフィギュレーションに適したファイルを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="d224c-163">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-163">Select **OK**.</span></span>

    ![RCS の構成ページ](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="d224c-165">ER ソリューションを実行して追跡実行する</span><span class="sxs-lookup"><span data-stu-id="d224c-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="d224c-166">ER ソリューションの最初のバージョンのデザインが完了したとします。</span><span class="sxs-lookup"><span data-stu-id="d224c-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="d224c-167">これにより、インスタンスでテストを行い、実行パフォーマンスを分析できます。</span><span class="sxs-lookup"><span data-stu-id="d224c-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="d224c-168">RCS から ER コンフィギュレーションの Finance and Operations へのインポート</span><span class="sxs-lookup"><span data-stu-id="d224c-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="d224c-169">アプリケーション インスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="d224c-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="d224c-170">このチュートリアルでは、RCS インスタンス (ER コンポーネントを設計する場所) から、インスタンス (テストして最後に使用する場所) にコンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d224c-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="d224c-171">したがって、必要なコンポーネントがすべて準備されたことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d224c-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="d224c-172">手順については、[規制コンフィギュレーション サービス (RCS) からの電子申告 (ER) 構成のインポート](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="d224c-173">これらの手順に従って、コンフィギュレーションを RCS からアプリケーションにインポートします。</span><span class="sxs-lookup"><span data-stu-id="d224c-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="d224c-174">**電子申告** ワークスペースの、**Litware, inc.** コンフィギュレーション プロバイダーのタイルで、**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="d224c-175">**コンフィギュレーション リポジトリ** ページで、**RCS** タイプのリポジトリを選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="d224c-176">**コンフィギュレーション** クイック タブで、**パフォーマンス追跡形式** コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="d224c-177">**バージョン** クイック タブで、選択したコンフィギュレーションのバージョン **1.1** を選択し、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![レポジトリ ページのコンフィギュレーション](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="d224c-179">データ モデルとモデル マッピングコン フィギュレーションの対応するバージョンは、インポートされた ER 形式コンフィギュレーションの前提条件として自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="d224c-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="d224c-180">ER パフォーマンス追跡を有効にする</span><span class="sxs-lookup"><span data-stu-id="d224c-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="d224c-181">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d224c-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="d224c-182">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d224c-183">**ユーザー パラメーター** ダイアログ ボックスの **実行トレース** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d224c-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="d224c-184">**実行トレース形式** フィールドで、**デバッグ トレース形式** を選択して、ER 形式実行の詳細の収集を開始します。</span><span class="sxs-lookup"><span data-stu-id="d224c-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="d224c-185">この値が選択されている場合、パフォーマンス追跡によって、次のアクションに費やされた時間に関する情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="d224c-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="d224c-186">データを取得するために呼び出されるモデル マッピングで各データ ソースを実行する</span><span class="sxs-lookup"><span data-stu-id="d224c-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="d224c-187">生成される出力にデータを入力するため各項目の形式を処理する</span><span class="sxs-lookup"><span data-stu-id="d224c-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="d224c-188">**実行トレース形式** フィールドを使用して、実行詳細が ER 形式およびマッピング要素で格納される生成済パフォーマンス追跡の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="d224c-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="d224c-189">**デバッグ トレース形式** を値として選択することにより、ER 操作デザイナーでトレースの内容を分析して、トレースに記載されている ER 形式またはマッピング要素を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d224c-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="d224c-190">次のオプションを **はい** に設定して、ER モデル マッピングおよび ER フォーマット コンポーネントの実行に関する具体的な詳細を収集します。</span><span class="sxs-lookup"><span data-stu-id="d224c-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="d224c-191">**クエリ統計情報の収集** – このオプションが有効になっている場合、パフォーマンス追跡では次の情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="d224c-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="d224c-192">データ ソースによって作成されたデータベース呼び出し数</span><span class="sxs-lookup"><span data-stu-id="d224c-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="d224c-193">データベースに対する複製呼び出し数</span><span class="sxs-lookup"><span data-stu-id="d224c-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="d224c-194">データベース呼び出しを行うために使用された SQL ステートメントの詳細</span><span class="sxs-lookup"><span data-stu-id="d224c-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="d224c-195">**キャッシュのアクセスの追跡** – このオプションが有効になっている場合、パフォーマンス追跡では ER モデル マッピングのキャッシュ使用に関する情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="d224c-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="d224c-196">**データ アクセスの追跡** – このオプションが有効になっている場合、パフォーマンス追跡では、レコード リスト タイプの実行されたデータ ソースに対するデータベースへの呼び出し回数に関する情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="d224c-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="d224c-197">**リスト列挙の追跡** – このオプションが有効になっている場合、パフォーマンス追跡では、レコード リスト タイプのデータ ソースから要求されたレコード数に関する情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="d224c-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d224c-198">**ユーザー パラメーター** ダイアログ ボックスのパラメーターは、ユーザーと現在の会社に固有です。</span><span class="sxs-lookup"><span data-stu-id="d224c-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![ユーザー パラメーター ダイアログ ボックス](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="d224c-200">ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="d224c-200">Run the ER format</span></span>

1. <span data-ttu-id="d224c-201">**DEMF** 会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-201">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="d224c-202">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d224c-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="d224c-203">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス追跡形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="d224c-204">アクション ウィンドウで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="d224c-205">生成されるファイルによって、6 つの仕入先の 265 トランザクションに関する情報が表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="d224c-206">実行追跡の確認</span><span class="sxs-lookup"><span data-stu-id="d224c-206">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a> <span data-ttu-id="d224c-207">アプリケーションから生成された追跡のエクスポート</span><span class="sxs-lookup"><span data-stu-id="d224c-207">Export the generated trace from the application</span></span>

<span data-ttu-id="d224c-208">パフォーマンス追跡は、ソースの ER 形式から切り離され、外部の zip ファイルにシリアル化されます。</span><span class="sxs-lookup"><span data-stu-id="d224c-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="d224c-209">**組織管理 \> 電子申告 \> 構成デバッグ ログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d224c-209">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="d224c-210">**電子申告実行ログ** ページ、左ウィンドウの、**コンフィギュレーション名** フィールドで、**パフォーマンス追跡形式** を選択し、**パフォーマンス追跡形式** コンフィギュレーションの実行によって生成されたログ レコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="d224c-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="d224c-211">ページの右上隅にある **添付ファイル** ボタン (紙クリップ記号) を選択するか、**Ctrl + Shift + A** を押します。</span><span class="sxs-lookup"><span data-stu-id="d224c-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![電子申告実行ログ ページの添付ファイル ボタン](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="d224c-213">**電子申告実行ログの添付ファイル** ページの、アクション ウィンドウで、**開く** を選択してパフォーマンス追跡を zip ファイルとして取得し、ローカルに保管します。</span><span class="sxs-lookup"><span data-stu-id="d224c-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![電子申告実行ログの添付ファイル](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="d224c-215">生成されるトレースは、**GUID** 形式のみの固有のレポート ID を通じて、ソース ER レポートを参照しています。</span><span class="sxs-lookup"><span data-stu-id="d224c-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="d224c-216">形式のバージョン番号付けは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="d224c-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="d224c-217">実行される ER 形式と ER モデル マッピングに対して生成されたパフォーマンス追跡間の関連付けは、使用されたルート記述子と共通データ モデルに基づいていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="d224c-218">形式のバージョン番号付けおよびモデル マッピングは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="d224c-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="d224c-219">モデル マッピングに対する **モデル マッピングの既定値** フラグの設定も考慮されません。</span><span class="sxs-lookup"><span data-stu-id="d224c-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a> <span data-ttu-id="d224c-220">生成された追跡を RCS にインポートします</span><span class="sxs-lookup"><span data-stu-id="d224c-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="d224c-221">RCS の、**電子レポート** ワークスペースで、**レポート コンフィギュレーション** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="d224c-222">**構成** ページのコンフィギュレーション ツリーで、**パフォーマンス追跡モデル** 項目を展開し、**パフォーマンス追跡形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="d224c-223">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d224c-224">**形式デザイナー** の、アクション ウィンドウで、**パフォーマンス追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d224c-225">**パフォーマンス追跡結果の設定** ダイアログ ボックスで、**パフォーマンス追跡のインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="d224c-226">**参照** を選択し、先ほどインポートした zip ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-226">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="d224c-227">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-227">Select **OK**.</span></span>

    ![RCS のパフォーマンス追跡結果の設定ダイアログ ボックス](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="d224c-229">RCS での分析に対するパフォーマンス追跡の使用 – 形式実行</span><span class="sxs-lookup"><span data-stu-id="d224c-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="d224c-230">RCS の、**形式デザイナー** ページで、**展開/折りたたみ** を選択してすべての形式項目の内容を展開します。</span><span class="sxs-lookup"><span data-stu-id="d224c-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="d224c-231">現在の形式の一部の項目に関して、追加情報が表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="d224c-232">形式項目を使用して生成された出力にデータを入力するのに費やした実際の時間</span><span class="sxs-lookup"><span data-stu-id="d224c-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="d224c-233">出力全体の生成に費やされた合計時間の割合で表される同じ時間</span><span class="sxs-lookup"><span data-stu-id="d224c-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![RCS の形式デザイナー ページ](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="d224c-235">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d224c-235">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="d224c-236">RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング</span><span class="sxs-lookup"><span data-stu-id="d224c-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="d224c-237">RCS、**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス追跡マッピング** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="d224c-238">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d224c-239">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d224c-239">Select **Designer**.</span></span>
4. <span data-ttu-id="d224c-240">**モデル マッピング デザイナー** ページの、アクション ウィンドウで、**パフォーマンス追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d224c-241">事前にインポートした追跡を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="d224c-242">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-242">Select **OK**.</span></span>

<span data-ttu-id="d224c-243">現在のモデル マッピングの一部のデータ ソース項目に関する、新しい情報が利用可能になることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="d224c-244">データ ソースを使用してデータの取得に費やした実際の時間</span><span class="sxs-lookup"><span data-stu-id="d224c-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="d224c-245">モデル マッピング全体の実行に費やされた合計時間の割合で表される同じ時間</span><span class="sxs-lookup"><span data-stu-id="d224c-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="d224c-246">VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースの実行中は、現在のモデル マッピングがデータベース要求を重複することを ER から通知されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="d224c-247">この重複が発生するのは、仕入先トランザクションの一覧が、反復する仕入先レコードごとに 2 回呼び出されるためです。</span><span class="sxs-lookup"><span data-stu-id="d224c-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="d224c-248">1 回の呼び出しでは、構成されたバインディングに基づいて、データ モデルの各トランザクションの詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="d224c-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="d224c-249">もう 1 回の呼び出しで、データ モデルの仕入先ごとに計算されたトランザクション数を入力します。</span><span class="sxs-lookup"><span data-stu-id="d224c-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![RCS のモデル マッピング デザイナー ページで重複したデータベース要求に関するメッセージ](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="d224c-251">**\[Q:530\]** の値は、テーブルから VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースにレコードを返すため、VendTrans テーブルが 530 回呼び出されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d224c-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="d224c-252">**\[530\]** の値は、VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースが、そのデータ ソースからレコードを返し、データ モデルで詳細を入力するために 530 回呼び出されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d224c-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="d224c-253">265 トランザクションの詳細を取得するための呼び出し数を減らし、モデルマッピングのパフォーマンスを向上させるため、VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースに対してキャッシュを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d224c-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="d224c-254">それは LedgerTransTypeList データ ソースに対して行われる呼び出し数を減らすのにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d224c-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="d224c-255">このデータ ソースは、**LedgerTransType** 列挙の各値をラベルに関連付けるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d224c-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="d224c-256">このデータ ソースを使用すると、適切なラベルを検索して、各仕入先トランザクションのデータ モデルに入力できます。</span><span class="sxs-lookup"><span data-stu-id="d224c-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="d224c-257">このデータ ソースへの現在の呼び出し数 (9,027) は、265 トランザクションに対して非常に高くなっています。</span><span class="sxs-lookup"><span data-stu-id="d224c-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![データ ソースへの 9,027 の呼び出しを示す、RCS のモデル マッピング デザイナー ページ](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="d224c-259">実行追跡からの情報に基づいてモデル マッピングを改善する</span><span class="sxs-lookup"><span data-stu-id="d224c-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="d224c-260">モデル マッピングのロジックを変更する</span><span class="sxs-lookup"><span data-stu-id="d224c-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="d224c-261">次の手順に従ってキャッシュを使用すると、データベースへの重複呼び出しを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="d224c-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="d224c-262">RCS、**モデル マッピング デザイナー** ページの、**データ ソース** ウィンドウで、**VendTable** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="d224c-263">**キャッシュ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="d224c-264">**VendTable** 項目を展開し、VendTable データ ソース (**\<関係** 項目) の一対多の関係の一覧を展開してから、**VendTrans.VendTable\_AccountNum** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="d224c-265">**キャッシュ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-265">Select **Cache**.</span></span>

    ![重複呼び出しを防ぐためのキャッシュ設定](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="d224c-267">LedgerTransTypeList データ ソースを VendTable データ ソースのスコープに移動するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d224c-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="d224c-268">**データ ソース タイプ** ウィンドウで、**関数** 項目を展開し、**計算済フィールド** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="d224c-269">**データ ソース** ウィンドウで、**VendTable** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="d224c-270">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-270">Select **Add**.</span></span>
    4. <span data-ttu-id="d224c-271">**名前** フィールドで、**\$TransType** を入力します。</span><span class="sxs-lookup"><span data-stu-id="d224c-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="d224c-272">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="d224c-273">**式** フィールドに、**LedgerTransTypeList** を入力します。</span><span class="sxs-lookup"><span data-stu-id="d224c-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="d224c-274">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-274">Select **Save**.</span></span>
    8. <span data-ttu-id="d224c-275">**式の編集** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d224c-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="d224c-276">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d224c-276">Click **OK**.</span></span>

3. <span data-ttu-id="d224c-277">次の手順に従って、**\$TransType** フィールドをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="d224c-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="d224c-278">**LedgerTransTypeList** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="d224c-279">**キャッシュ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="d224c-280">**VendTable.\$TransType** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="d224c-281">**キャッシュ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-281">Select **Cache**.</span></span>

    ![$TransType フィールドのキャッシュ設定](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="d224c-283">次の手順に従って **\$TransTypeRecord** フィールドを変更し、キャッシュされた **\$TransType** フィールドを使用開始できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d224c-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="d224c-284">**データ ソース** ウィンドウで、**VendTable** 項目を展開し、**\<関係** 項目を展開し、**VendTrans.VendTable\_AccountNum** 項目を展開してから、**VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="d224c-285">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="d224c-286">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="d224c-287">**式** フィールドで、次の式を検索します。</span><span class="sxs-lookup"><span data-stu-id="d224c-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="d224c-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="d224c-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="d224c-289">**式** フィールドで、次の式を入力します。</span><span class="sxs-lookup"><span data-stu-id="d224c-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="d224c-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="d224c-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="d224c-291">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-291">Select **Save**.</span></span>
    7. <span data-ttu-id="d224c-292">**式の編集** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d224c-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="d224c-293">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-293">Select **OK**.</span></span>

5. <span data-ttu-id="d224c-294">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-294">Select **Save**.</span></span>
6. <span data-ttu-id="d224c-295">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d224c-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="d224c-296">**モデル マッピング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d224c-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="d224c-297">ER モデル マッピングの変更されたバージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="d224c-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="d224c-298">RCS、**コンフィギュレーション** ページの、**バージョン** クイック タブで、**パフォーマンス追跡マッピング** コンフィギュレーションのバージョン **1.2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="d224c-299">**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-299">Select **Change status**.</span></span>
3. <span data-ttu-id="d224c-300">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="d224c-301">変更された ER モデル マッピング コンフィギュレーションを RCS からアプリケーションにインポートする</span><span class="sxs-lookup"><span data-stu-id="d224c-301">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="d224c-302">このトピックの前にある [RCS から ER コンフィギュレーションを Finance and Operations にインポートする](#import-configuration) セクションでこの手順を繰り返し、**パフォーマンス トレース マッピング** コンフィギュレーションのバージョン 1.2 をインポートします。</span><span class="sxs-lookup"><span data-stu-id="d224c-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="d224c-303">変更された ER ソリューションを実行して追跡実行する</span><span class="sxs-lookup"><span data-stu-id="d224c-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="d224c-304">ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="d224c-304">Run the ER format</span></span>

<span data-ttu-id="d224c-305">このトピックの先のセクション [ER 形式を実行する](#run-format) の手順を繰り返して、新しいパフォーマンス追跡を生成します。</span><span class="sxs-lookup"><span data-stu-id="d224c-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="d224c-306">実行トレースを使って作業する</span><span class="sxs-lookup"><span data-stu-id="d224c-306">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="d224c-307">アプリケーションから生成された追跡のエクスポート</span><span class="sxs-lookup"><span data-stu-id="d224c-307">Export the generated trace from the application</span></span>

<span data-ttu-id="d224c-308">このトピックの先のセクション [生成された追跡をアプリケーションからエクスポートする](#export-trace) の手順を繰り返して、新しいパフォーマンス追跡をローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="d224c-308">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="d224c-309">生成された追跡を RCS にインポートする</span><span class="sxs-lookup"><span data-stu-id="d224c-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="d224c-310">このトピックの先のセクション [生成された追跡を RCS にインポートする](#import-trace) の手順を繰り返して、新しいパフォーマンス追跡を RCS にインポートします。</span><span class="sxs-lookup"><span data-stu-id="d224c-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="d224c-311">RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング</span><span class="sxs-lookup"><span data-stu-id="d224c-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="d224c-312">このトピックの先のセクション [RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング](#use-trace) の手順を繰り返して、最新のパフォーマンス追跡を分析します。</span><span class="sxs-lookup"><span data-stu-id="d224c-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="d224c-313">モデル マッピングに対して行った調整によって、データベースへの重複するクエリが消去されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="d224c-314">このモデル マッピングのデータベース テーブルおよびデータ ソースへの呼び出し数も減少しました。</span><span class="sxs-lookup"><span data-stu-id="d224c-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="d224c-315">したがって、ER ソリューション全体のパフォーマンスが向上しました。</span><span class="sxs-lookup"><span data-stu-id="d224c-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![RCS の、モデル マッピング デザイナー ページで、VendTable データ ソースに関する情報を追跡します。](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="d224c-317">追跡情報で、VendTable データ ソースの **\[12\]** の値は、このデータソースが 12 回呼び出されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d224c-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="d224c-318">**\[Q:6\]** の値は、6 つの呼び出しが VendTable テーブルへのデータベース呼び出しに変換されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d224c-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="d224c-319">**\[C:6\]** の値は、データベースからフェッチされたレコードがキャッシュされ、その他の 6 つの呼び出しがキャッシュを使用して処理されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d224c-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="d224c-320">LedgerTransTypeList データソースへの呼び出し数が 9,027 から 240 に減少したことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![RCS の モデル マッピング デザイナー ページで、LedgerTransTypeList データ ソースに関する情報を追跡します。](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="d224c-322">アプリケーションで実行追跡を確認する</span><span class="sxs-lookup"><span data-stu-id="d224c-322">Review the execution trace in the application</span></span>

<span data-ttu-id="d224c-323">RCS に加えて、一部のバージョンでは ER フレームワーク デザイナー経験に対する機能が提供される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d224c-323">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="d224c-324">これらのバージョンには **デザイン モードを有効にする** オプションがあり、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d224c-324">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="d224c-325">このオプションは **電子申告パラメーター** ページの **一般** タブで検索できます。このページは **電子申告** ワークスペースから開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d224c-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![電子申告パラメーター ページでデザイン モード オプションを有効にする](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="d224c-327">これらのいずれかのバージョンを使用する場合は、生成されたパフォーマンス追跡の詳細をアプリケーションで直接分析できます。</span><span class="sxs-lookup"><span data-stu-id="d224c-327">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="d224c-328">アプリケーションからエクスポートして RCS にインポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d224c-328">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="d224c-329">外部ツールを使用した実行追跡の確認</span><span class="sxs-lookup"><span data-stu-id="d224c-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="d224c-330">ユーザー パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d224c-330">Configure user parameters</span></span>

1. <span data-ttu-id="d224c-331">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d224c-331">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="d224c-332">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d224c-333">**ユーザー パラメーター** ダイアログ ボックス、**実行トレース** セクションの、**実行トレース形式** フィールドで、**PerfView XML** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="d224c-334">ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="d224c-334">Run the ER format</span></span>

<span data-ttu-id="d224c-335">このトピックの先のセクション [ER 形式を実行する](#run-format) の手順を繰り返して、新しいパフォーマンス追跡を生成します。</span><span class="sxs-lookup"><span data-stu-id="d224c-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="d224c-336">Web ブラウザーによって、ダウンロード用の zip ファイルが提供されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="d224c-337">このファイルには、PerfView 形式のパフォーマンス追跡が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d224c-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="d224c-338">次に、PerfView パフォーマンス分析ツールを使用して ER 形式実行の詳細を分析できます。</span><span class="sxs-lookup"><span data-stu-id="d224c-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![PerfView 形式のパフォーマンス トレース情報](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="d224c-340">外部ツールを使用してデータベース クエリを含む実行トレースを確認する</span><span class="sxs-lookup"><span data-stu-id="d224c-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="d224c-341">ER フレームワークに行われた改善のため、PerfView 形式で生成されたパフォーマンスの追跡により、ER 形式の実行に関する詳細情報が提供されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d224c-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="d224c-342">Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.4 (2019 年 7 月) では、このトレースに、アプリケーション データベースに対して実行された SQL クエリの詳細を含めることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d224c-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="d224c-343">ユーザー パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d224c-343">Configure user parameters</span></span>

1. <span data-ttu-id="d224c-344">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d224c-344">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d224c-345">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d224c-346">**ユーザー パラメーター** ダイアログ ボックスの **実行トレース** セクションで、次のパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="d224c-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="d224c-347">**実行トレース形式** フィールドで、**PerfView XML** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d224c-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="d224c-348">**クエリ統計情報の収集** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d224c-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="d224c-349">**クエリの追跡** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d224c-349">Set the **Trace query** option to **Yes**.</span></span>

    ![トレースの実行セクション、ユーザー パラメータ ダイアログボックス](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="d224c-351">ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="d224c-351">Run the ER format</span></span>

<span data-ttu-id="d224c-352">このトピックの先のセクション [ER 形式を実行する](#run-format) の手順を繰り返して、新しいパフォーマンス追跡を生成します。</span><span class="sxs-lookup"><span data-stu-id="d224c-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="d224c-353">Web ブラウザーによって、ダウンロード用の zip ファイルが提供されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d224c-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="d224c-354">このファイルには、PerfView 形式のパフォーマンス追跡が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d224c-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="d224c-355">次に、PerfView パフォーマンス分析ツールを使用して ER 形式実行の詳細を分析できます。</span><span class="sxs-lookup"><span data-stu-id="d224c-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="d224c-356">この追跡に、ER 形式の実行中における SQL データベース アクセスに関する詳細が含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d224c-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![PerfView で実行された ER 形式のトレース情報](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="d224c-358">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d224c-358">Additional resources</span></span>

- [<span data-ttu-id="d224c-359">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="d224c-359">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d224c-360">パラメーター化された計算フィールドのデータ ソースを追加して、ER ソリューションのパフォーマンスを向上させる</span><span class="sxs-lookup"><span data-stu-id="d224c-360">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)
