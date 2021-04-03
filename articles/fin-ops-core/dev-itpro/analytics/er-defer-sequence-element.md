---
title: ER 形式におけるシーケンス要素の実行の延期
description: このトピックは、電子申告 (ER) 形式のシーケンス要素の実行を延期する方法について説明します。
author: NickSelin
manager: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b1a9bb072330f586799f5cfea676d941739ca818
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562169"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a><span data-ttu-id="4155b-103">ER 形式におけるシーケンス要素の実行の延期</span><span class="sxs-lookup"><span data-stu-id="4155b-103">Defer the execution of sequence elements in ER formats</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="4155b-104">概要</span><span class="sxs-lookup"><span data-stu-id="4155b-104">Overview</span></span>

<span data-ttu-id="4155b-105">[電子申告](general-electronic-reporting.md) (ER) フレームワークのオペレーション デザイナーを使用して、テキスト形式で送信ドキュメントを生成するために使用する ER ソリューションの [形式コンポーネント](general-electronic-reporting.md#FormatComponentOutbound) を [コンフィギュレーション](tasks/er-format-configuration-2016-11.md) することができます。</span><span class="sxs-lookup"><span data-stu-id="4155b-105">You can use the Operations designer of the [Electronic reporting (ER)](general-electronic-reporting.md) framework to [configure](tasks/er-format-configuration-2016-11.md) the [format component](general-electronic-reporting.md#FormatComponentOutbound) of an ER solution that is used to generate outbound documents in a text format.</span></span> <span data-ttu-id="4155b-106">コンフィギュレーションされた形式コンポーネントの階層構造は、さまざまなタイプの形式要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="4155b-106">The hierarchical structure of the configured format component consists of format elements of various types.</span></span> <span data-ttu-id="4155b-107">これらの形式要素は、生成されたドキュメントに実行時に必要な情報を入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4155b-107">These format elements are used to fill generated documents with the required information at runtime.</span></span> <span data-ttu-id="4155b-108">既定では、ER 形式の実行時に、形式要素は形式階層に表示されているのと同じ順序で、上から下に 1 つずつ実行されます。</span><span class="sxs-lookup"><span data-stu-id="4155b-108">By default, when you run an ER format, the format elements are run in the same order as they are presented in the format hierarchy: one by one, from top to bottom.</span></span> <span data-ttu-id="4155b-109">ただし、デザイン時に、コンフィギュレーションされた形式コンポーネントのすべてのシーケンス要素の実行順序を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="4155b-109">However, at design time, you can change the execution order for any sequence elements of the configured format component.</span></span>

<span data-ttu-id="4155b-110">コンフィギュレーションされた形式のシーケンス形式要素に対して <a name="DeferredSequenceExecution"></a> **遅延実行** オプションを有効にすることにより、その要素の実行を延期することができます。</span><span class="sxs-lookup"><span data-stu-id="4155b-110">By turning on the <a name="DeferredSequenceExecution"></a>**Deferred execution** option for a sequence format element in the configured format, you can defer (postpone) the execution of that element.</span></span> <span data-ttu-id="4155b-111">この場合、親要素の他の要素すべてが実行されるまで、要素は実行されません。</span><span class="sxs-lookup"><span data-stu-id="4155b-111">In this case, the element isn't run until all other elements of its parent have been run.</span></span>

<span data-ttu-id="4155b-112">この機能の詳細を知るには、このトピックの例を実行します。</span><span class="sxs-lookup"><span data-stu-id="4155b-112">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="limitations"></a><span data-ttu-id="4155b-113">制限</span><span class="sxs-lookup"><span data-stu-id="4155b-113">Limitations</span></span>

<span data-ttu-id="4155b-114">**遅延実行** オプションは、テキスト形式で **送信** ドキュメントを生成するために使用される ER 形式に対してコンフィギュレーションされているシーケンス要素に対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4155b-114">The **Deferred execution** option is supported only for sequence elements that are configured for an ER format that is used to generate **outbound** documents in text format.</span></span>

<span data-ttu-id="4155b-115">**遅延実行** オプションは、最大長が制限されているトリミング シーケンスとしてコンフィギュレーションされているシーケンスには適用されません。</span><span class="sxs-lookup"><span data-stu-id="4155b-115">The **Deferred execution** option isn't applicable to sequences that have been configured as trimmed sequences where the maximum length is limited.</span></span>

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a><span data-ttu-id="4155b-116">例: ER 形式のシーケンス要素の実行の延期</span><span class="sxs-lookup"><span data-stu-id="4155b-116">Example: Defer the execution of a sequence element in an ER format</span></span>

<span data-ttu-id="4155b-117">次のステップは、システム管理者または電子申告機能コンサルタント [ロール](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) のユーザーが、実行順序が形式階層の順序とは異なるシーケンス要素を含む ER 形式をコンフィギュレーションする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="4155b-117">The following steps explain how a user in the System administrator or Electronic reporting functional consultant [role](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) can configure an ER format that contains a sequence element where order of execution differs from the order in the format hierarchy.</span></span>

<span data-ttu-id="4155b-118">これらのステップは、Microsoft Dynamics 365 Finance の **USMF** 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="4155b-118">These steps can be performed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4155b-119">必要条件</span><span class="sxs-lookup"><span data-stu-id="4155b-119">Prerequisites</span></span>

<span data-ttu-id="4155b-120">この例を完了するには、次のいずれかのロール用の Finance の **USMF** 会社にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4155b-120">To complete this example, you must have access to the **USMF** company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="4155b-121">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="4155b-121">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="4155b-122">システム管理者</span><span class="sxs-lookup"><span data-stu-id="4155b-122">System administrator</span></span>

<span data-ttu-id="4155b-123">[ER 形式における XML 要素の実行の延期](er-defer-xml-element.md#Example) トピックの例をまだ完了していない場合、次のサンプル ER ソリューションの [コンフィギュレーション](general-electronic-reporting.md#Configuration) をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="4155b-123">If you haven't yet completed the example in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example) topic, download the following [configurations](general-electronic-reporting.md#Configuration) of the sample ER solution.</span></span>

| <span data-ttu-id="4155b-124">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="4155b-124">Content description</span></span>            | <span data-ttu-id="4155b-125">ファイル名</span><span class="sxs-lookup"><span data-stu-id="4155b-125">File name</span></span> |
|--------------------------------|-----------|
| <span data-ttu-id="4155b-126">ER データ モデル構成</span><span class="sxs-lookup"><span data-stu-id="4155b-126">ER data model configuration</span></span>    | [<span data-ttu-id="4155b-127">遅延 elements.version.1.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="4155b-127">Model to learn deferred elements.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="4155b-128">ER モデル マッピング コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4155b-128">ER model mapping configuration</span></span> | [<span data-ttu-id="4155b-129">遅延 element.version.1.1.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="4155b-129">Mapping to learn deferred elements.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="4155b-130">開始する前に、サンプル ER ソリューションの次のコンフィギュレーションをダウンロードして保存する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="4155b-130">Before you begin, you must also download and save the following configuration of the sample ER solution.</span></span>

| <span data-ttu-id="4155b-131">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="4155b-131">Content description</span></span>     |<span data-ttu-id="4155b-132">ファイル名</span><span class="sxs-lookup"><span data-stu-id="4155b-132">File name</span></span> |
|-------------------------|----------|
| <span data-ttu-id="4155b-133">ER フォーマット構成</span><span class="sxs-lookup"><span data-stu-id="4155b-133">ER format configuration</span></span> | [<span data-ttu-id="4155b-134">遅延シーケンスを知るための形式. バージョン .1.1.xml</span><span class="sxs-lookup"><span data-stu-id="4155b-134">Format to learn deferred sequences.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a><span data-ttu-id="4155b-135">サンプル ER のコンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="4155b-135">Import the sample ER configurations</span></span>

1. <span data-ttu-id="4155b-136">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4155b-136">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="4155b-137">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-137">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="4155b-138">**コンフィギュレーション** ページで、**遅延要素を知るためのモデル** コンフィギュレーションがコンフィギュレーション ツリーで使用できない場合、ER データ モデル コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4155b-138">On the **Configurations** page, if the **Model to learn deferred elements** configuration isn't available in the configuration tree, import the ER data model configuration:</span></span>

    1. <span data-ttu-id="4155b-139">**交換** を選択し、**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-139">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="4155b-140">**参照** をクリックし、**遅延 elements.1.xml を知るためのモデル** ファイルを検索して選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4155b-140">Select **Browse**, find and select the **Model to learn deferred elements.1.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="4155b-141">コンフィギュレーション ページで、**遅延要素を知るためのマッピング** コンフィギュレーションがコンフィギュレーション ツリーで使用できない場合、ER データ マッピング コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4155b-141">If the **Mapping to learn deferred elements** configuration isn't available in the configuration tree, import the ER model mapping configuration:</span></span>

    1. <span data-ttu-id="4155b-142">**交換** を選択し、**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-142">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="4155b-143">**参照** をクリックし、**遅延 elements.1.1.xml を知るためのマッピング** ファイルを検索して選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4155b-143">Select **Browse**, find and select the **Mapping to learn deferred elements.1.1.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="4155b-144">ER 形式コンフィギュレーションのインポート:</span><span class="sxs-lookup"><span data-stu-id="4155b-144">Import the ER format configuration:</span></span>

    1. <span data-ttu-id="4155b-145">**交換** を選択し、**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-145">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="4155b-146">**参照** をクリックし、**遅延 sequences.1.1.xml を知るための形式** ファイルを検索して選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4155b-146">Select **Browse**, find and select the **Format to learn deferred sequences.1.1.xml** file, and then select **OK**.</span></span>

6. <span data-ttu-id="4155b-147">コンフィギュレーション ツリーで、**遅延要素を知るためのモデル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="4155b-147">In the configuration tree, expand **Model to learn deferred elements**.</span></span>
7. <span data-ttu-id="4155b-148">コンフィギュレーション ツリーでインポートされた ER コンフィギュレーションのリストを確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-148">Review the list of imported ER configurations in the configuration tree.</span></span>

    ![コンフィギュレーション ページのインポートされた ER コンフィギュレーション](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a><span data-ttu-id="4155b-150">コンフィギュレーション プロバイダーの有効化</span><span class="sxs-lookup"><span data-stu-id="4155b-150">Activate a configurations provider</span></span>

1. <span data-ttu-id="4155b-151">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4155b-151">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="4155b-152">**ローカライズのコンフィギュレーション** ページの **コンフィギュレーション プロバイダー** セクションで、Litware, Inc. (`http://www.litware.com`) サンプル会社の [コンフィギュレーション プロバイダー](general-electronic-reporting.md#Provider) がリストに表示されていること、および有効としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-152">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the Litware, Inc. (`http://www.litware.com`) sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="4155b-153">このコンフィギュレーション プロバイダーがリストに表示されない場合、またはアクティブとしてマークされていない場合、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](./tasks/er-configuration-provider-mark-it-active-2016-11.md) トピックの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="4155b-153">If this configuration provider isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](./tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

    ![ローカライズのコンフィギュレーション ページの Litware, Inc. サンプル会社](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a><span data-ttu-id="4155b-155">インポートされたモデル マッピングを確認する</span><span class="sxs-lookup"><span data-stu-id="4155b-155">Review the imported model mapping</span></span>

<span data-ttu-id="4155b-156">税トランザクションにアクセスするようにコンフィギュレーションされている ER モデル マッピング コンポーネントの設定を確認し、リクエスト時にアクセスしたデータを公開します。</span><span class="sxs-lookup"><span data-stu-id="4155b-156">Review the settings of the ER model mapping component that is configured to access tax transactions and expose accessed data on request.</span></span>

1. <span data-ttu-id="4155b-157">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4155b-157">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="4155b-158">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-158">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="4155b-159">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**遅延要素を知るためのモデル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="4155b-159">On the **Configurations** page, in the configuration tree, expand **Model to learn deferred elements**.</span></span>
4. <span data-ttu-id="4155b-160">**遅延要素を知るためのマッピング** コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-160">Select the **Mapping to learn deferred elements** configuration.</span></span>
5. <span data-ttu-id="4155b-161">**デザイナー** を選択して、マッピングの一覧を開きます。</span><span class="sxs-lookup"><span data-stu-id="4155b-161">Select **Designer** to open the list of mappings.</span></span>
6. <span data-ttu-id="4155b-162">**デザイナー** を選択して、マッピングの詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-162">Select **Designer** to review the mapping details.</span></span>
7. <span data-ttu-id="4155b-163">**詳細を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-163">Select **Show details**.</span></span>
8. <span data-ttu-id="4155b-164">コンフィギュレーションされたデータ ソースを確認し、税トランザクションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4155b-164">Review the data sources that are configured to access tax transactions:</span></span>

    - <span data-ttu-id="4155b-165">*テーブル レコード タイプ* の **トランザクション** データ ソースは、**TaxTrans** アプリケーション テーブルのレコードにアクセスするようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="4155b-165">The **Transactions** data source of the *Table record* type is configured to access records of the **TaxTrans** application table.</span></span>
    - <span data-ttu-id="4155b-166">*計算済フィールド* タイプの **伝票** データ ソースは、必要な伝票コード (**INV-10000349** および **INV-10000350**) をレコードのリストとして返すようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="4155b-166">The **Vouchers** data source of the *Calculated field* type is configured to return the required voucher codes (**INV-10000349** and **INV-10000350**) as a list of records.</span></span>
    - <span data-ttu-id="4155b-167">**フィルター処理** された *計算済フィールド* タイプのデータソースは、**トランザクション** データ ソースから、必要な伝票の税トランザクションのみを選択するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="4155b-167">The **Filtered** data source of the *Calculated field* type is configured to select, from the **Transactions** data source, only tax transactions of the required vouchers.</span></span>
    - <span data-ttu-id="4155b-168">*計算済フィールド* タイプの **\$TaxAmount** フィールドは **フィルター処理** されたデータ ソースに対して追加され、反対の符号を持つ税額を公開します。</span><span class="sxs-lookup"><span data-stu-id="4155b-168">The **\$TaxAmount** field of the *Calculated field* type is added for the **Filtered** data source to expose the tax value that has the opposite sign.</span></span>
    - <span data-ttu-id="4155b-169">**グループ化** された *グループ化* タイプのデータ ソースは、フィルター処理された **フィルター処理** データ ソースの税トランザクションをグループ化するようコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="4155b-169">The **Grouped** data source of the *Group By* type is configured to group filtered tax transactions of the **Filtered** data source.</span></span>
    - <span data-ttu-id="4155b-170">**グループ化** されたデータ ソースの **TotalSum** 集計フィールドは、そのデータ ソースでフィルター処理されたすべての税トランザクションに対して、**フィルター処理** されたデータ ソースの **\$TaxAmount** フィールドの値を集計するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="4155b-170">The **TotalSum** aggregation field of the **Grouped** data source is configured to summarize values of the **\$TaxAmount** field of the **Filtered** data source for all filtered tax transactions of that data source.</span></span>

        ![「GroupBy」パラメーターの編集ページの TotalSum 集計フィールド](./media/ER-DeferredSequence-GroupByParameters.png)

9. <span data-ttu-id="4155b-172">コンフィギュレーションされたデータ ソースをデータ モデルにバインドする方法、および ER 形式で利用可能になるようにアクセス データを公開する方法を確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-172">Review how the configured data sources are bound to the data model, and how they expose accessed data to make it available in an ER format:</span></span>

    - <span data-ttu-id="4155b-173">**フィルター処理** されたデータ ソースは、データ モデルの **Data.List** フィールドにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="4155b-173">The **Filtered** data source is bound to the **Data.List** field of the data model.</span></span>
    - <span data-ttu-id="4155b-174">**フィルター処理** されたデータ ソースの **\$TaxAmount** フィールドは、データ モデルの **Data.List.Value** フィールドにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="4155b-174">The **\$TaxAmount** field of the **Filtered** data source is bound to the **Data.List.Value** field of the data model.</span></span>
    - <span data-ttu-id="4155b-175">**グループ化** されたデータ ソースの **TotalSum** フィールドは、データ モデルの **Data.Summary.Total** フィールドにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="4155b-175">The **TotalSum** field of the **Grouped** data source is bound to the **Data.Summary.Total** field of the data model.</span></span>

    ![モデル マッピング デザイナーのページ](./media/ER-DeferredSequence-ModelMapping.png)

10. <span data-ttu-id="4155b-177">**モデル マッピング デザイナー** および **モデル マッピング** のページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4155b-177">Close the **Model mapping designer** and **Model mappings** pages.</span></span>

### <a name="review-the-imported-format"></a><span data-ttu-id="4155b-178">インポートされた形式を確認する</span><span class="sxs-lookup"><span data-stu-id="4155b-178">Review the imported format</span></span>

1. <span data-ttu-id="4155b-179">**コンフィギュレーション** ツリーのコンフィギュレーション ページで、**遅延シーケンスを知るための形式** コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-179">On the **Configurations** page, in the configuration tree, select the **Format to learn deferred sequences** configuration.</span></span>
2. <span data-ttu-id="4155b-180">**デザイナー** を選択して、形式の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-180">Select **Designer** to review the format details.</span></span>
3. <span data-ttu-id="4155b-181">**詳細を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-181">Select **Show details**.</span></span>
4. <span data-ttu-id="4155b-182">税トランザクションの詳細を含むテキスト形式で送信ドキュメントを生成するようにコンフィギュレーションされている ER フォーマット コンポーネントの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-182">Review the settings of the ER format components that are configured to generate an outbound document in text format that includes details of the tax transactions:</span></span>

    - <span data-ttu-id="4155b-183">**レポート\\明細行** シーケンス形式要素は、1 つの行で送信ドキュメントを入力するようにコンフィギュレーションされ、入れ子になったシーケンス要素から生成されます (**ヘッダー**、**レコード**、および **集計**)。</span><span class="sxs-lookup"><span data-stu-id="4155b-183">The **Report\\Lines** sequence format element is configured to fill the outbound document with a single line that is generated from the nested sequence elements (**Header**, **Record**, and **Summary**).</span></span>

        ![形式デザイナー ページの明細行シーケンス形式要素と入れ子になった要素](./media/ER-DeferredSequence-Format.png)

    - <span data-ttu-id="4155b-185">**レポート\\明細行\\ヘッダー** のシーケンス形式要素は、1 つの行で送信ドキュメントを入力するようにコンフィギュレーションされ、処理を開始するときに日時を表示します。</span><span class="sxs-lookup"><span data-stu-id="4155b-185">The **Report\\Lines\\Header** sequence format element is configured to fill the outbound document with a single header line that shows the date and time  when the processing starts.</span></span>
    - <span data-ttu-id="4155b-186">**レポート\\明細行\\レコード** のシーケンス形式要素は、1 つの行で送信ドキュメントを入力するようにコンフィギュレーションされ、個別の税トランザクションの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="4155b-186">The **Report \\Lines\\Record** sequence format element is configured to fill the outbound document with a single line that shows the details of individual tax transactions.</span></span> <span data-ttu-id="4155b-187">これらの税トランザクションは、セミコロンで区切られます。</span><span class="sxs-lookup"><span data-stu-id="4155b-187">These tax transactions are separated by a semicolon.</span></span>

        ![区切り記号としてセミコロンを使用するレコード シーケンス形式要素](./media/ER-DeferredSequence-Format1.png)

    - <span data-ttu-id="4155b-189">**レポート\\明細行\\集計** のシーケンス形式要素は、1 つの集計行で送信ドキュメントを入力するようにコンフィギュレーションされ、処理された税トランザクションの税額の合計が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4155b-189">The **Report\\Lines\\Summary** sequence format element is configured to fill the outbound document with a single summary line that includes the sum of the tax values from the processed tax transactions.</span></span>

4. <span data-ttu-id="4155b-190">**マッピング** タブで、次の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-190">On the **Mapping** tab, review the following details:</span></span>

    - <span data-ttu-id="4155b-191">**レポート\\明細行\\ヘッダー** 要素は、送信ドキュメントの 1 つの行を生成するのに、データ ソースにバインドする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4155b-191">The **Report\\Lines\\Header** element doesn't have to be bound to a data source to generate a single line in an outbound document.</span></span>
    - <span data-ttu-id="4155b-192">**Prefix1** 要素は、追加された行がレポート ヘッダー行であることを示す **P1** 記号を生成します。</span><span class="sxs-lookup"><span data-stu-id="4155b-192">The **Prefix1** element generates **P1** symbols to indicate that the line that is added is the report header line.</span></span>
    - <span data-ttu-id="4155b-193">**ExecutionDateTime** 要素は、ヘッダー行が追加された時の日時 (ミリ秒を含む) を生成します。</span><span class="sxs-lookup"><span data-stu-id="4155b-193">The **ExecutionDateTime** element generates the date and time (including milliseconds) when the header line is added.</span></span>
    - <span data-ttu-id="4155b-194">**レポート\\明細行\\レコード** 要素は、**model.Data.List** リストにバインドされ、バインド リストからすべてのレコードに対して 1 行生成します。</span><span class="sxs-lookup"><span data-stu-id="4155b-194">The **Report\\Lines\\Record** element is bound to the **model.Data.List** list to generate a single line for every record from the bound list.</span></span>
    - <span data-ttu-id="4155b-195">**Prefix2** 要素は、追加された行が税トランザクション詳細用であることを示す **P2** 記号を生成します。</span><span class="sxs-lookup"><span data-stu-id="4155b-195">The **Prefix2** element generates **P2** symbols to indicate that the line that is added is for the tax transaction details.</span></span>
    - <span data-ttu-id="4155b-196">**TaxAmount** 要素は、**model.Data.List.Value** (相対パス ビューに **\@.Value** として表示される) にバインドされ、現在の税トランザクションの税額を生成します。</span><span class="sxs-lookup"><span data-stu-id="4155b-196">The **TaxAmount** element is bound to **model.Data.List.Value** (which is shown as **\@.Value** in the relative path view) to generate the tax value of the current tax transaction.</span></span>
    - <span data-ttu-id="4155b-197">**RunningTotal** 要素は、税額累計額のプレースホルダーです。</span><span class="sxs-lookup"><span data-stu-id="4155b-197">The **RunningTotal** element is a placeholder for the running total of the tax values.</span></span> <span data-ttu-id="4155b-198">現在、バインディングも既定値もコンフィギュレーションされていないため、この要素には出力がありません。</span><span class="sxs-lookup"><span data-stu-id="4155b-198">Currently, this element has no output, because neither a binding nor a default value is configured for it.</span></span>
    - <span data-ttu-id="4155b-199">**ExecutionDateTime** 要素は、現在のトランザクションがこのレポートで処理される時の日時 (ミリ秒を含む) を生成します。</span><span class="sxs-lookup"><span data-stu-id="4155b-199">The **ExecutionDateTime** element generates the date and time (including milliseconds) when the current transaction is processed in this report.</span></span>
    - <span data-ttu-id="4155b-200">**レポート\\明細行\\集計** 要素は、送信ドキュメントの 1 つの行を生成するのに、データ ソースにバインドする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4155b-200">The **Report\\Lines\\Summary** element doesn't have to be bound to a data source to generate a single line in an outbound document.</span></span>
    - <span data-ttu-id="4155b-201">**Prefix3** 要素は、追加された行に税額合計が含まれていることを示す **P3** 記号を生成します。</span><span class="sxs-lookup"><span data-stu-id="4155b-201">The **Prefix3** element generates **P3** symbols to indicate that the line that is added contains the total tax value.</span></span>
    - <span data-ttu-id="4155b-202">**TotalTaxAmount** 要素は **model.Data.Summary.Total** にバインドされ、処理された税トランザクションの税額合計を生成します。</span><span class="sxs-lookup"><span data-stu-id="4155b-202">The **TotalTaxAmount** element is bound to **model.Data.Summary.Total** to generate the sum of the tax values of the processed tax transactions.</span></span>
    - <span data-ttu-id="4155b-203">**ExecutionDateTime** 要素は、集計行が追加された時の日時 (ミリ秒を含む) を生成します。</span><span class="sxs-lookup"><span data-stu-id="4155b-203">The **ExecutionDateTime** element generates the date and time (including milliseconds) when the summary line is added.</span></span>

    ![フォーマット デザイナー ページのマッピング タブ](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a><span data-ttu-id="4155b-205">インポートされた ER 形式の実行</span><span class="sxs-lookup"><span data-stu-id="4155b-205">Run the imported format</span></span>

1. <span data-ttu-id="4155b-206">**フォーマット デザイナー** ページで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-206">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="4155b-207">Web ブラウザーからファイルをダウンロードし、確認のために開きます。</span><span class="sxs-lookup"><span data-stu-id="4155b-207">Download the file that the web browser offers, and open it for review.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredSequence-Run.png)

<span data-ttu-id="4155b-209">集計行 22 には、処理されたトランザクションの税額の合計が示されます。</span><span class="sxs-lookup"><span data-stu-id="4155b-209">Notice that summary line 22 presents the sum of the tax values for the processed transactions.</span></span> <span data-ttu-id="4155b-210">形式は、合計を返すようバインドされている **model.Data.Summary.Total** を使用するようにコンフィギュレーションされていて、合計はモデル マッピングを使用する *GroupBy* の **グループ化** されたデータ ソースの **TotalSum** の集計を呼び出して計算されます。</span><span class="sxs-lookup"><span data-stu-id="4155b-210">Because the format is configured to use the **model.Data.Summary.Total** binding to return this sum, the sum is calculated by calling the **TotalSum** aggregation of the **Grouped** data source of the *GroupBy* type that uses the model mapping.</span></span> <span data-ttu-id="4155b-211">この集計を計算するために、モデル マッピングは、**フィルタ処理** されるデータ ソースで選択されたすべてのトランザクションを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="4155b-211">To calculate this aggregation, model mapping iterates over all transactions that have been selected in the **Filtered** data source.</span></span> <span data-ttu-id="4155b-212">明細行 21 と 22 の実行時間を比較することにより、合計の計算に 10 ミリ秒 (ms) かかったことを特定できます。</span><span class="sxs-lookup"><span data-stu-id="4155b-212">By comparing the execution times of lines 21 and 22, you can determine that calculation of the sum took 10 milliseconds (ms).</span></span> <span data-ttu-id="4155b-213">明細行 2 と 21 の実行時間を比較することにより、すべてのトランザクション明細行の生成に 7 ミリ秒 (ms) かかったことを特定できます。</span><span class="sxs-lookup"><span data-stu-id="4155b-213">By comparing the execution times of lines 2 and 21, you can determine that generation of all transactional lines took 7 ms.</span></span> <span data-ttu-id="4155b-214">したがって、合計 17 ミリ秒必要でした。</span><span class="sxs-lookup"><span data-stu-id="4155b-214">Therefore, a total of 17 ms was required.</span></span>

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a><span data-ttu-id="4155b-215">合計が生成された出力に基づくように形式を変更する</span><span class="sxs-lookup"><span data-stu-id="4155b-215">Modify the format so that the summing is based on generated output</span></span>

<span data-ttu-id="4155b-216">トランザクションの量が現在の例のボリュームよりも大きい場合、合計時間が増加してパフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4155b-216">If the volume of transactions is much larger than the volume in the current example, the summing time might increase and cause performance issues.</span></span> <span data-ttu-id="4155b-217">形式の設定を変更することにより、これらパフォーマンスの問題を防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="4155b-217">By changing the setting of the format, you can help prevent these performance issues.</span></span> <span data-ttu-id="4155b-218">税額にアクセスして生成されたレポートに含めることができるため、この情報を再利用して税額を合計することができます。</span><span class="sxs-lookup"><span data-stu-id="4155b-218">Because you access tax values to include them in the generated report, you can reuse this information to sum tax values.</span></span> <span data-ttu-id="4155b-219">詳細については、[集計と合計を行うよう形式をコンフィギュレーションする](./tasks/er-format-counting-summing-1.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4155b-219">For more information, see [Configure format to do counting and summing](./tasks/er-format-counting-summing-1.md).</span></span>

1. <span data-ttu-id="4155b-220">**形式** タブの **形式デザイナー** ページで、形式ツリーの **レポート** ファイル要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-220">On the **Format designer** page, on the **Format** tab, select the **Report** file element in the format tree.</span></span>
2. <span data-ttu-id="4155b-221">**出力詳細の収集** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4155b-221">Set the **Collect output details** option to **Yes**.</span></span> <span data-ttu-id="4155b-222">[データ収集](er-functions-category-data-collection.md) カテゴリの組み込み ER 機能を使用してアクセスできるデータ ソースとして既存のレポートの内容を使用することで、この形式をコンフィギュレーションできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4155b-222">You can now configure this format by using the content of an existing report as a data source that can be accessed by using the built-in ER functions in the [Data collection](er-functions-category-data-collection.md) category.</span></span>
3. <span data-ttu-id="4155b-223">**マッピング** タブで、**レポート\\明細行** シーケンス要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-223">On the **Mapping** tab, select the **Report\\Lines** sequence element.</span></span>
4. <span data-ttu-id="4155b-224">**収集したデータ キー名** の式を `WsColumn` としてコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="4155b-224">Configure the **Collected data key name** expression as `WsColumn`.</span></span>
5. <span data-ttu-id="4155b-225">**収集したデータ キーの値** の式を `WsRow` としてコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="4155b-225">Configure the **Collected data key value** expression as `WsRow`.</span></span>

    ![形式デザイナー ページの明細行シーケンス要素](./media/ER-DeferredSequence-Format3.png)

6. <span data-ttu-id="4155b-227">**レポート\\明細行\\レコード\\TaxAmount** 数値要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-227">Select the **Report\\Lines\\Record\\TaxAmount** numeric element.</span></span>
7. <span data-ttu-id="4155b-228">**収集したデータ キー名** の式を `SummingAmountKey` としてコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="4155b-228">Configure the **Collected data key name** expression as `SummingAmountKey`.</span></span>

    ![形式デザイナー ページの TaxAmount 数値要素](./media/ER-DeferredSequence-Format4.png)

    <span data-ttu-id="4155b-230">セル A1 の値が処理されたすべての税トランザクションからの税額の値で追記されている、この仮想ワークシートのフルフィルメントの設定を考慮することができます。</span><span class="sxs-lookup"><span data-stu-id="4155b-230">You can consider this setting the fulfillment of a virtual worksheet, where the value of cell A1 is appended with the value of the tax amount from every processed tax transaction.</span></span>

8. <span data-ttu-id="4155b-231">**レポート\\明細行\\レコード\\RunningTotal** の数値要素を選択し、**フォーミュラの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-231">Select the **Report\\Lines\\Record\\RunningTotal** numeric element, and then select **Edit formula**.</span></span>
9. <span data-ttu-id="4155b-232">組み込みの [SUMIF](er-functions-datacollection-sumif.md) ER 関数を使用して `SUMIF(SummingAmountKey, WsColumn, WsRow)` 式をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="4155b-232">Configure the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression by using the built-in [SUMIF](er-functions-datacollection-sumif.md) ER function.</span></span>
10. <span data-ttu-id="4155b-233">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-233">Select **Save**.</span></span>

    ![SUMIF 式](./media/ER-DeferredSequence-FormulaDesigner.png)

11. <span data-ttu-id="4155b-235">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4155b-235">Close the **Formula designer** page.</span></span>
12. <span data-ttu-id="4155b-236">**保存** を選択して、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-236">Select **Save**, and then select **Run**.</span></span>
13. <span data-ttu-id="4155b-237">Web ブラウザーからファイルをダウンロードし、確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-237">Download and review the file that the web browser offers.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredSequence-Run1.png)

    <span data-ttu-id="4155b-239">明細行 21 には、生成された出力をデータ ソースとして使用することにより、処理されたすべてのトランザクションに対して計算される税額の累計が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4155b-239">Line 21 contains the running total of tax values that is calculated for all processed transactions by using the generated output as a data source.</span></span> <span data-ttu-id="4155b-240">このデータ ソースは、レポートの先頭から開始し、最後の税トランザクションまで続行します。</span><span class="sxs-lookup"><span data-stu-id="4155b-240">This data source starts from the beginning of the report and continues through the last tax transaction.</span></span> <span data-ttu-id="4155b-241">明細行 22 には、モデル マッピングにおいて *GroupBy* タイプのデータ ソースを使用して計算され、処理されたすべてのトランザクションの税額の合計が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4155b-241">Line 22 contains the sum of the tax values for all processed transactions that are calculated in the model mapping by using the data source of the *GroupBy* type.</span></span> <span data-ttu-id="4155b-242">これらの値は等しくなります。</span><span class="sxs-lookup"><span data-stu-id="4155b-242">Notice that these values are equal.</span></span> <span data-ttu-id="4155b-243">したがって、**GroupBy** の代わりに出力ベースの合計を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4155b-243">Therefore, the output-based summing can be used instead of **GroupBy**.</span></span> <span data-ttu-id="4155b-244">明細行 2 と 21 の実行時間を比較することにより、すべてのトランザクション明細行の生成および合計に 9 ミリ秒 (ms) かかったことを特定できます。</span><span class="sxs-lookup"><span data-stu-id="4155b-244">By comparing the execution times of lines 2 and 21, you can determine that generation of all the transactional lines and summing took 9 ms.</span></span> <span data-ttu-id="4155b-245">したがって、詳細行の生成および税額の合計が懸念されるかぎり、変更された形式は元の形式よりも約 2 倍速くなります。</span><span class="sxs-lookup"><span data-stu-id="4155b-245">Therefore, as far as the generation of detailed lines and the summing of tax values are concerned, the modified format is approximately two times faster than the original format.</span></span>

14. <span data-ttu-id="4155b-246">**レポート\\明細行\\集計\\TotalTaxAmount** の数値要素を選択し、**フォーミュラの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-246">Select the **Report\\Lines\\Summary\\TotalTaxAmount** numeric element, and then select **Edit formula**.</span></span>
15. <span data-ttu-id="4155b-247">既存の式の代わりに `SUMIF(SummingAmountKey, WsColumn, WsRow)` 式を入力します。</span><span class="sxs-lookup"><span data-stu-id="4155b-247">Enter the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression instead of the existing expression.</span></span>
16. <span data-ttu-id="4155b-248">**保存** を選択して、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-248">Select **Save**, and then select **Run**.</span></span>
17. <span data-ttu-id="4155b-249">Web ブラウザーからファイルをダウンロードし、確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-249">Download and review the file that the web browser offers.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredSequence-Run2.png)

    <span data-ttu-id="4155b-251">最後のトランザクション詳細行の税額累計は、集計行の合計値と等しくなるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4155b-251">Notice that the running total of tax values on the last transaction details line now equals the sum on the summary line.</span></span>

### <a name="put-values-of-output-based-summing-in-the-report-header"></a><span data-ttu-id="4155b-252">レポート ヘッダーに出力ベースの集計を配置する</span><span class="sxs-lookup"><span data-stu-id="4155b-252">Put values of output-based summing in the report header</span></span>

<span data-ttu-id="4155b-253">たとえば、レポートのヘッダーに税額の合計を表示する必要がある場合、形式を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="4155b-253">If, for example, you must present the sum of tax values in the header of your report, you can modify your format.</span></span>

1. <span data-ttu-id="4155b-254">**形式** タブの **形式** デザイナー ページで、**レポート\\明細行\\集計** シーケンス要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-254">On the **Format designer** page, on the **Format** tab, select the **Report\\Lines\\Summary** sequence element.</span></span>
2. <span data-ttu-id="4155b-255">**上へ移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-255">Select **Move up**.</span></span>
3. <span data-ttu-id="4155b-256">**保存** を選択して、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-256">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="4155b-257">Web ブラウザーからファイルをダウンロードし、確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-257">Download and review the file that the web browser offers.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredSequence-Run3.png)

    <span data-ttu-id="4155b-259">この合計が生成された出力に基づいて計算されるようになったので、集計行 2 の税額の合計は 0 (ゼロ) と等しくなるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4155b-259">Notice that the sum of tax values on summary line 2 now equals 0 (zero), because this sum is now calculated based on the generated output.</span></span> <span data-ttu-id="4155b-260">明細行 2 が生成される時、生成された出力にはまだトランザクションの詳細のある行は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="4155b-260">When line 2 is generated, the generated output doesn't yet contain lines that have transaction details.</span></span> <span data-ttu-id="4155b-261">この形式をコンフィギュレーションして、すべての税トランザクションに対して **レポート\\明細行\\レコード** のシーケンス要素が実行されるまで、**レポート\\明細行\\集計** のシーケンス要素の実行を延期させることができます。</span><span class="sxs-lookup"><span data-stu-id="4155b-261">You can configure this format to defer the execution of the **Report\\Lines\\Summary** sequence element until the **Report\\Lines\\Record** sequence element has been run for all tax transactions.</span></span>

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a><span data-ttu-id="4155b-262">集計シーケンスの実行を延期することにより、計算された合計が使用されます</span><span class="sxs-lookup"><span data-stu-id="4155b-262">Defer the execution of the summary sequence so that the calculated total is used</span></span>

1. <span data-ttu-id="4155b-263">**形式** タブの **形式** デザイナー ページで、**レポート\\明細行\\集計** シーケンス要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-263">On the **Format designer** page, on the **Format** tab, select the **Report\\Lines\\Summary** sequence element.</span></span>
2. <span data-ttu-id="4155b-264">**遅延実行** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4155b-264">Set the **Deferred execution** option to **Yes**.</span></span>

    ![形式デザイナー ページの集計シーケンス要素の遅延実行オプション](./media/ER-DeferredSequence-Format5.png)

3. <span data-ttu-id="4155b-266">**保存** を選択して、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4155b-266">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="4155b-267">Web ブラウザーからファイルをダウンロードし、確認します。</span><span class="sxs-lookup"><span data-stu-id="4155b-267">Download and review the file that the web browser offers.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredSequence-Run4.png)

    <span data-ttu-id="4155b-269">**レポート\\明細行\\集計** シーケンス要素は、その親要素である **レポート\\明細行** の下に入れ子になっている他のすべての品目が実行された後に実行されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4155b-269">The **Report\\Lines\\Summary** sequence element is now run only after all other items that are nested under its parent element, **Report\\Lines**, have been run.</span></span> <span data-ttu-id="4155b-270">したがって、**レポート\\明細行\\レコード** シーケンス要素が、**model.Data.List** データ ソースのすべての税トランザクションに実行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="4155b-270">Therefore, it's run after the **Report\\Lines\\Record** sequence element has been run for all tax transactions of the **model.Data.List** data source.</span></span> <span data-ttu-id="4155b-271">明細行 1、2、および 3 の実行時間と最後の明細行 22 の実行時間はこの事実を示しています。</span><span class="sxs-lookup"><span data-stu-id="4155b-271">The execution times of lines 1, 2, and 3, and of the last line, 22, reveal this fact.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4155b-272">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4155b-272">Additional resources</span></span>

- [<span data-ttu-id="4155b-273">棚卸および集計を行うための形式のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4155b-273">Configure format to do counting and summing</span></span>](./tasks/er-format-counting-summing-1.md)
- [<span data-ttu-id="4155b-274">パフォーマンス上の問題をトラブルシューティングするため ER 形式の追跡実行</span><span class="sxs-lookup"><span data-stu-id="4155b-274">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="4155b-275">ER 形式における XML 要素の実行の延期</span><span class="sxs-lookup"><span data-stu-id="4155b-275">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]