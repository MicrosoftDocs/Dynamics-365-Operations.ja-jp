---
title: パラメーター化された計算フィールドのデータ ソースを追加して、ER ソリューションのパフォーマンスを向上させる
description: このトピックでは、パラメーター化された計算フィールドのデータ ソースを追加して、電子申告 (ER) ソリューションのパフォーマンスを向上させる方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 940b696a06fb46bcd0557f059327cd4340448137
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681283"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="d1b0b-103">パラメーター化された計算フィールドのデータ ソースを追加して、ER ソリューションのパフォーマンスを向上させる</span><span class="sxs-lookup"><span data-stu-id="d1b0b-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1b0b-104">このトピックではは、実行される [電子申告 (ER)](general-electronic-reporting.md) 形式の [パフォーマンス追跡](trace-execution-er-troubleshoot-perf.md) を取得し、それらのトレースからの情報を使用して、パラメーター化された **計算フィールド** のデータ ソースを構成することにより、パフォーマンスを向上させる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="d1b0b-105">ビジネス ドキュメントを生成するための ER コンフィギュレーションをデザインするプロセスの一部として、アプリケーションからデータを取得し、生成された出力に入力するために使用されるメソッドを定義します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="d1b0b-106">**計算フィールド** 型のパラメーター化された ER データ ソースをデザインすることにより、データベース呼び出し回数を減らし、ER 形式の実行の詳細を収集に関連する時間とコストを大幅に削減することができます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d1b0b-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="d1b0b-107">Prerequisites</span></span>

- <span data-ttu-id="d1b0b-108">このトピックの例を完了するには、次のいずれかの [ロール](../sysadmin/tasks/assign-users-security-roles.md) にアクセスできる必要があります：</span><span class="sxs-lookup"><span data-stu-id="d1b0b-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="d1b0b-109">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="d1b0b-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="d1b0b-110">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="d1b0b-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d1b0b-111">システム管理者</span><span class="sxs-lookup"><span data-stu-id="d1b0b-111">System administrator</span></span>

- <span data-ttu-id="d1b0b-112">この会社は、**DEMF** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="d1b0b-113">このトピックの [付録 1](#appendix1) の手順に従って、このトピックの例を完了するために必要なサンプルの Microsoft ER ソリューションのコンポーネントをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="d1b0b-114">このトピックの [付録 2](#appendix2) の手順に従って、サンプルの Microsoft ER ソリューションのパフォーマンスを向上させるために ER フレームワークを使用するために必要な ER パラメーターの最小セットを構成します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="d1b0b-115">サンプル ER ソリューションのインポート</span><span class="sxs-lookup"><span data-stu-id="d1b0b-115">Import the sample ER solution</span></span>

<span data-ttu-id="d1b0b-116">仕入先トランザクションを示す新しいレポートを生成するため、ER ソリューションを設計する必要があるとします。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="d1b0b-117">現時点では、選択した仕入先のトランザクションは **仕入先トランザクション** ページ (**買掛金勘定** \> **仕入先** \> **すべての仕入先** に移動し、仕入先を選択してから、アクション ペインの **仕入先** タブの **トランザクション** グループで、**トランザクション** を選択します) で検索できます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="d1b0b-118">ただし、XML 形式の 1 つの電子ドキュメントに、すべての仕入先トランザクションをまとめる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="d1b0b-119">このソリューションは、必要なデータ モデル、モデル マッピング、および形式コンポーネントを含むいくつかの ER コンフィギュレーションで構成されます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="d1b0b-120">最初の手順は、サンプル ER ソリューションをインポートして、仕入先トランザクション レポートを生成することです。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="d1b0b-121">会社用にプロビジョニングされた Microsoft Dynamics 365 Finance のインスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="d1b0b-122">このトピックでは、サンプル会社 **Litware, Inc.** のコンフィギュレーションを作成および変更します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="d1b0b-123">このコンフィギュレーション プロバイダーが Finance インスタンスに追加され、有効としてマークされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="d1b0b-124">詳細については、[構成プロバイダーを作成して、有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="d1b0b-125">**電子レポート** ワークスペースで、**レポート コンフィギュレーション** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="d1b0b-126">**コンフィギュレーション** ページで、前提条件としてダウンロードした ER コンフィギュレーションを Finance に次の順序でインポートします: データ モデル、モデル マッピング、フォーマット。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="d1b0b-127">各コンフィギュレーションについて、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="d1b0b-128">操作ウィンドウで、**交換** \> **XML ファイルからロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="d1b0b-129">**参照** を選択して、ER コンフィギュレーションに適したファイルを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="d1b0b-130">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-130">Select **OK**.</span></span>

![コンフィギュレーション ページでインポートされたコンフィギュレーション](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="d1b0b-132">サンプル ER ソリューションのレビュー</span><span class="sxs-lookup"><span data-stu-id="d1b0b-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="d1b0b-133">モデル マッピングを確認する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-133">Review the model mapping</span></span>

1. <span data-ttu-id="d1b0b-134">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス向上モデル** を展開し、**パフォーマンス向上マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="d1b0b-135">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d1b0b-136">**モデルからデータ ソースへのマッピング** ページのアクション ペインで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="d1b0b-137">この ER モデル マッピングは、次のアクションを実行するように設計されています:</span><span class="sxs-lookup"><span data-stu-id="d1b0b-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="d1b0b-138">VendTrans テーブル (**Trans** データ ソース) に格納されている仕入先トランザクションの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="d1b0b-139">すべてのトランザクションについて、VendTable テーブルから、トランザクションが転記された仕入先 (**\#Vend** データソース) のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1b0b-140">**\#Vend** データ ソースは、既存の多対一の関係 **\@.'\>Relations'.VendTable\_AccountNum** を使用して、対応する仕入先レコードを取得するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="d1b0b-141">このコンフィギュレーションのモデル マッピングは、このモデルに対して作成され Finance で実行される、すべての ER 形式の基本データ モデルを実装します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="d1b0b-142">したがって、**Trans** データ ソースの内容は、抽象 **モデル** データ ソースなどの ER 形式に対して公開されます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![モデル マッピング デザイナー ページの Trans データ ソース](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="d1b0b-144">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="d1b0b-145">**モデルからデータ ソースへのマッピング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="d1b0b-146">形式の確認</span><span class="sxs-lookup"><span data-stu-id="d1b0b-146">Review format</span></span>

1. <span data-ttu-id="d1b0b-147">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス向上モデル** を展開し、**パフォーマンス向上形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="d1b0b-148">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d1b0b-149">**形式デザイナー** ページの **マッピング** タブで、**展開 / 折りたたみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="d1b0b-150">**モデル**、**データ**、および **トランザクション** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="d1b0b-151">この ER 形式は、仕入先トランザクション レポートを XML 形式で生成するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![形式デザイナー ページでの形式要素の形式データ ソースと構成済みバインディング](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="d1b0b-153">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="d1b0b-154">サンプル ER ソリューションを実行して、実行を追跡する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="d1b0b-155">ER ソリューションの最初のバージョンの設計が完了したとします。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="d1b0b-156">これにより、Finance インスタンスでソリューションをテストし、実行パフォーマンスを分析します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="d1b0b-157">ER パフォーマンス追跡を有効にする</span><span class="sxs-lookup"><span data-stu-id="d1b0b-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="d1b0b-158">**DEMF** 会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="d1b0b-159">[ER パフォーマンス追跡を有効にする](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) の手順に従って、ER 形式の実行中にパフォーマンス追跡を生成します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![ユーザー パラメーター ダイアログ ボックス](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="d1b0b-161">ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-161">Run the ER format</span></span>

1. <span data-ttu-id="d1b0b-162">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d1b0b-163">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス向上形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="d1b0b-164">アクション ウィンドウで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="d1b0b-165">パフォーマンス追跡を使用してモデル マッピングのパフォーマンスを分析する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="d1b0b-166">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス向上マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="d1b0b-167">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d1b0b-168">**モデル マッピング** ページのアクション ペインで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d1b0b-169">**モデル マッピング デザイナー** ページの、アクション ウィンドウで、**パフォーマンス追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d1b0b-170">生成された最新の追跡を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="d1b0b-171">現在のモデル マッピングの一部のデータ ソース項目に関する新しい情報が利用可能になりました:</span><span class="sxs-lookup"><span data-stu-id="d1b0b-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="d1b0b-172">データ ソースを使用してデータの取得に費やした実際の時間</span><span class="sxs-lookup"><span data-stu-id="d1b0b-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="d1b0b-173">モデル マッピング全体の実行に費やされた合計時間の割合で表される同じ時間</span><span class="sxs-lookup"><span data-stu-id="d1b0b-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![モデル マッピング デザイナー ページの実行時間の詳細](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="d1b0b-175">**パフォーマンス統計** グリッドは、**Trans** データ ソースが VendTrans テーブルを 1 回呼び出すことを示しています。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="d1b0b-176">**Trans** データ ソースの値 **\[265\]\[Q:265\]** は、265 個の仕入先トランザクションがアプリケーション テーブルから取得された、データ モデルに返されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="d1b0b-177">また、**パフォーマンス統計** グリッドは、現在のモデル マッピングが、**\#Vend** データ ソースの実行中にデータベース要求を重複していることも示します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="d1b0b-178">この重複は、次の理由で発生します:</span><span class="sxs-lookup"><span data-stu-id="d1b0b-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="d1b0b-179">仕入先テーブルは、反復された 265 回の仕入先トランザクションごとに 2 回呼び出され、合計 530 回の呼び出しが行われます:</span><span class="sxs-lookup"><span data-stu-id="d1b0b-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="d1b0b-180">仕入先番号を入力するために 1 回の呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="d1b0b-181">仕入先名を入力するために 1 回の呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="d1b0b-182">仕入先テーブルは、取得したトランザクションが 5 つの仕入先に対してのみ転記されている場合でも、反復された仕入先トランザクションごとに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="d1b0b-183">530 回の呼び出しのうち、525 回は重複しています。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="d1b0b-184">次の図は、重複する呼び出し (データベース要求) についてのメッセージを示しています。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![モデル マッピング デザイナー ページの重複データベース要求に関するメッセージ](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="d1b0b-186">モデル マッピングの合計実行時間 (約 8 秒) のうち、80% (約 6 秒) 以上が VendTable アプリケーション テーブルから値を取得するために費やされたことに注目してください。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="d1b0b-187">この割合は、VendTransアプリケーション テーブルからの情報量と比較して、5 つの仕入先の 2 つの属性に対して大きすぎます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="d1b0b-188">すべてのトランザクションの仕入先の詳細を取得するために行われる呼び出しの数を減らし、モデル マッピングのパフォーマンスを向上させるために、**\#Vend** データ ソースにキャッシュを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="d1b0b-189">**Trans\\\#Vend** データ ソースは、実行時に **Trans** データ ソースの現在のトランザクションのスコープにキャッシュされます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="d1b0b-190">**\#Vend** ソース データをキャッシュすることにより、525 から 260 に重複呼び出しの数を減らしますが、重複を完全に排除することはできません。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="d1b0b-191">重複を完全に削除するために、**計算フィールド** 型の新しいパラメーター化されたデータ ソースを構成できます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="d1b0b-192">実行追跡からの情報に基づいてモデル マッピングを改善する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="d1b0b-193">モデル マッピングのロジックを変更する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="d1b0b-194">次の手順に従って、**計算フィールド** 型のキャッシュとデータソースを使用して、データベースへの重複呼び出しを防止します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="d1b0b-195">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス向上マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="d1b0b-196">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d1b0b-197">**モデル マッピング** ページのアクション ペインで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d1b0b-198">**モデル マッピング デザイナー** ページで、次の手順に従って、**テーブル レコード** 型のデータ ソースを追加し、VendTable アプリケーション テーブルのレコードにアクセスします:</span><span class="sxs-lookup"><span data-stu-id="d1b0b-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="d1b0b-199">**データ ソース型** ペインで、**Dynamics 365 for Operations** を展開し、**テーブル レコード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="d1b0b-200">**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="d1b0b-201">ダイアログ ボックスで、**名前** フィールドに **Vend** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="d1b0b-202">**テーブル** フィールドに、**VendTable** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="d1b0b-203">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-203">Select **OK**.</span></span>

5. <span data-ttu-id="d1b0b-204">**計算フィールド** 型のデータ ソースへの呼び出をパラメーター化できるのは、それらのデータ ソースがコンテナーに存在する場合にのみです。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="d1b0b-205">したがって、次の手順に従って、**空コンテナー** 型のデータ ソースを追加し、**計算フィールド** 型の新しいパラメーター化されたデータ ソースを保持します:</span><span class="sxs-lookup"><span data-stu-id="d1b0b-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="d1b0b-206">**データ ソース型** ペインで、**一般** を展開し、**空コンテナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="d1b0b-207">**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="d1b0b-208">ダイアログ ボックスで、**名前** フィールドに **Box** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="d1b0b-209">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-209">Select **OK**.</span></span>

    ![モデル マッピング デザイナー ページの Box データ ソース](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="d1b0b-211">**計算フィールド** 型のパラメーター化されたデータ ソースを追加するには、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="d1b0b-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="d1b0b-212">**データ ソース** ペインで、**Box** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="d1b0b-213">**データ ソース型** ペインで、**関数** を展開し、**計算フィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="d1b0b-214">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-214">Select **Add**.</span></span>
    4. <span data-ttu-id="d1b0b-215">ダイアログ ボックスで、**名前** フィールドに **Vend** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="d1b0b-216">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="d1b0b-217">**フォーミュラ デザイナー** ページで、**パラメーター** を選択して、このデータ ソースが呼び出されたときに入力する必要があるパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="d1b0b-218">**パラメーター** ダイアログ ボックスで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="d1b0b-219">**名前** フィールドに、**parmVendAccNumber** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="d1b0b-220">**タイプ** フィールドで、**文字列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="d1b0b-221">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-221">Select **OK**.</span></span>
    11. <span data-ttu-id="d1b0b-222">**フォーミュラ** フィールドに、**FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))** と入力し ます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="d1b0b-223">**保存** を選択し、**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="d1b0b-224">**OK** を選択して新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="d1b0b-225">次の手順に従って、追加されたデータ ソースを実行時にキャッシュ済みとしてマークします:</span><span class="sxs-lookup"><span data-stu-id="d1b0b-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="d1b0b-226">**データ ソース** ペインで、**Box\\Vend** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="d1b0b-227">**キャッシュ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1b0b-228">**Box\\Vend** データ ソースは、実行時に **Trans** データ ソースのすべての仕入先トランザクションのスコープにキャッシュされます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="d1b0b-229">次の手順に従って、ネストされた **Trans\\\#Vend** データ ソースを更新して、**Box\\Vend** データ ソースを使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="d1b0b-230">**データ ソース** ペインで、**Trans** を展開します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="d1b0b-231">**Trans\\\#Vend** データ ソースを選択し、**編集** \> **フォーミュラの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="d1b0b-232">**フォーミュラ デザイナー** ページの **フォーミュラ** フィールドに、**Box.Vend(\@.AccountNum)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="d1b0b-233">**保存** を選択し、**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="d1b0b-234">**OK** を選択して、選択したデータ ソースへの変更を完了します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="d1b0b-235">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-235">Select **Save**.</span></span>

    ![モデル マッピング デザイナー ページの Vend データ ソース](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="d1b0b-237">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="d1b0b-238">**モデル マッピング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="d1b0b-239">ER モデル マッピングの変更されたバージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="d1b0b-240">**コンフィギュレーション** ページの、**バージョン** クイック タブで、**パフォーマンス向上マッピング** コンフィギュレーションのバージョン **1.2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="d1b0b-241">**状態の変更** \> **完了** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="d1b0b-242">変更された ER ソリューションを実行して追跡実行する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="d1b0b-243">このトピックの先のセクション [ER 形式を実行する](#run-format) の手順を繰り返して、新しいパフォーマンス追跡を生成します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="d1b0b-244">パフォーマンス追跡を使用して、モデル マッピングの調整を分析する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="d1b0b-245">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス向上マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="d1b0b-246">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d1b0b-247">**モデル マッピング** ページのアクション ペインで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d1b0b-248">**モデル マッピング デザイナー** ページの、アクション ウィンドウで、**パフォーマンス追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d1b0b-249">生成された最新の追跡を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="d1b0b-250">モデル マッピングに対して行った調整によって、データベースへの重複するクエリが消去されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="d1b0b-251">このモデル マッピングのデータベース テーブルおよびデータ ソースへの呼び出し数も減少しました。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![モデル マッピング デザイナー ページ 1 の追跡情報](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="d1b0b-253">合計実行時間は約 20 倍 (約 8 秒から約 400 ミリ秒) に短縮されました。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="d1b0b-254">したがって、ER ソリューション全体のパフォーマンスが向上しました。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![モデル マッピング デザイナー ページ 2 の追跡情報](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="d1b0b-256">付録 1: サンプル Microsoft ER ソリューションのコンポーネントのダウンロード</span><span class="sxs-lookup"><span data-stu-id="d1b0b-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="d1b0b-257">次のファイルをダウンロードして、ローカルに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="d1b0b-258">ファイル</span><span class="sxs-lookup"><span data-stu-id="d1b0b-258">File</span></span>                                        | <span data-ttu-id="d1b0b-259">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="d1b0b-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="d1b0b-260">Performance improvement model.version.1</span><span class="sxs-lookup"><span data-stu-id="d1b0b-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="d1b0b-261">ER データ モデル構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="d1b0b-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="d1b0b-262">Performance improvement mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="d1b0b-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="d1b0b-263">ER モデル マッピング構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="d1b0b-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="d1b0b-264">Performance improvement format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="d1b0b-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="d1b0b-265">ER フォーマット構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="d1b0b-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="d1b0b-266">付録 2: ER フレームワークを構成する</span><span class="sxs-lookup"><span data-stu-id="d1b0b-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="d1b0b-267">ER フレームワークを使用してサンプル Microsoft ER ソリューションのパフォーマンスを向上させる前に、ER パラメーターの最小セットを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="d1b0b-268">ER パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d1b0b-268">Configure ER parameters</span></span>

1. <span data-ttu-id="d1b0b-269">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d1b0b-270">**ローカライズ構成** ページの、**関連リンク** セクションで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="d1b0b-271">**電子申告パラメーター** ページの、**一般** タブで、**デザイン モードの有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="d1b0b-272">**添付** タブで、次のパラメーターを設定します:</span><span class="sxs-lookup"><span data-stu-id="d1b0b-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="d1b0b-273">**コンフィギュレーション** フィールドで、**DEMF** 社の **ファイル** タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="d1b0b-274">**ジョブ アーカイブ**、**一時的**、**ベースライン**、および **その他** フィールドで、**ファイル** タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="d1b0b-275">ER パラメーターについては、[ER フレームワークのコンフィギュレーション](electronic-reporting-er-configure-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a> <span data-ttu-id="d1b0b-276">ER コンフィギュレーション プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="d1b0b-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="d1b0b-277">追加されたすべての ER 構成は、ER 構成プロバイダーによって所有されているものとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="d1b0b-278">**電子申告** ワークスペースで有効化された ER 構成プロバイダーは、この目的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="d1b0b-279">したがって、ER コンフィギュレーションに追加または編集する前に、**電子申告** ワークスペースの ER コンフィギュレーション プロバイダーを有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="d1b0b-280">ER コンフィギュレーションの所有者のみがコンフィギュレーションを編集できます。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="d1b0b-281">したがって、ER 構成を編集する前に、適切な ER 構成 プロバイダーは **電子申告** ワークスペースで有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a> <span data-ttu-id="d1b0b-282">ER コンフィギュレーション プロバイダーの一覧をレビュー</span><span class="sxs-lookup"><span data-stu-id="d1b0b-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="d1b0b-283">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d1b0b-284">**ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="d1b0b-285">**構成プロバイダー テーブル** ページでは、各プロバイダー レコードの名前と URL が一意になります。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="d1b0b-286">このページの内容をレビューします。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-286">Review the contents of this page.</span></span> <span data-ttu-id="d1b0b-287">**Litware, Inc.** レコードが既に存在する場合は、次の手順をスキップし、[新しい ER コンフィギュレーション プロバイダーを追加](#ActivateProvider) します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a> <span data-ttu-id="d1b0b-288">新しい ER コンフィギュレーション プロバイダーを追加</span><span class="sxs-lookup"><span data-stu-id="d1b0b-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="d1b0b-289">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d1b0b-290">**ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="d1b0b-291">**構成プロバイダー** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="d1b0b-292">**名前** フィールドに、**Litware, Inc.** と入力</span><span class="sxs-lookup"><span data-stu-id="d1b0b-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="d1b0b-293">**インターネット アドレス** フィールドで、`https://www.litware.com` を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="d1b0b-294">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a> <span data-ttu-id="d1b0b-295">ER コンフィギュレーション プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="d1b0b-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="d1b0b-296">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d1b0b-297">**ローカライズ構成** ページの **構成プロバイダー** セクションで、**Litware, Inc.** を選び、**有効に設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="d1b0b-298">ER 構成 プロバイダーについては、[構成 プロバイダーを作成し有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1b0b-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1b0b-299">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d1b0b-299">Additional resources</span></span>

- [<span data-ttu-id="d1b0b-300">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="d1b0b-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d1b0b-301">電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d1b0b-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="d1b0b-302">計算済みフィールド タイプの ER データ ソースの、パラメーター化された呼び出しをサポートする</span><span class="sxs-lookup"><span data-stu-id="d1b0b-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)
