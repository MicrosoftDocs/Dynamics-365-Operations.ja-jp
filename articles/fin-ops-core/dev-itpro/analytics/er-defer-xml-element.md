---
title: ER 形式における XML 要素の実行の延期
description: このトピックは、電子申告 (ER) 形式の XML 要素の実行を延期する方法について説明します。
author: NickSelin
manager: kfend
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: e9f6161186d04b690ee560dac7ee12974d070506
ms.sourcegitcommit: 9c401a4adba260704b0b1cb9fe8e148bbb5afeed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "3120881"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a><span data-ttu-id="e0f39-103">ER 形式における XML 要素の実行の延期</span><span class="sxs-lookup"><span data-stu-id="e0f39-103">Defer the execution of XML elements in ER formats</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="e0f39-104">概要</span><span class="sxs-lookup"><span data-stu-id="e0f39-104">Overview</span></span>

<span data-ttu-id="e0f39-105">[電子申告](general-electronic-reporting.md) (ER) フレームワークのオペレーション デザイナーを使用して、XML 形式で送信ドキュメントを生成するために使用する ER ソリューションの [形式コンポーネント](general-electronic-reporting.md#FormatComponentOutbound) を [コンフィギュレーション](./tasks/er-format-configuration-2016-11.md) することができます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-105">You can use the Operations designer of the [Electronic reporting (ER)](general-electronic-reporting.md) framework to [configure](./tasks/er-format-configuration-2016-11.md) the [format component](general-electronic-reporting.md#FormatComponentOutbound) of an ER solution that is used to generate outbound documents in XML format.</span></span> <span data-ttu-id="e0f39-106">コンフィギュレーションされた形式コンポーネントの階層構造は、さまざまなタイプの形式要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-106">The hierarchical structure of the configured format component consists of format elements of various types.</span></span> <span data-ttu-id="e0f39-107">これらの形式要素は、生成されたドキュメントに実行時に必要な情報を入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-107">These format elements are used to fill generated documents with the required information at runtime.</span></span> <span data-ttu-id="e0f39-108">既定では、ER 形式の実行時に、形式要素は形式階層に表示されているのと同じ順序で、上から下に 1 つずつ実行されます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-108">By default, when you run an ER format, the format elements are run in the same order as they are presented in the format hierarchy: one by one, from top to bottom.</span></span> <span data-ttu-id="e0f39-109">ただし、デザイン時に、コンフィギュレーションされた形式コンポーネントのすべての XML 要素の実行順序を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-109">However, at design time, you can change the execution order for any XML elements of the configured format component.</span></span>

<span data-ttu-id="e0f39-110">コンフィギュレーションされた形式の XML 形式要素に対して <a name="DeferredXmlElementExecution"></a> **遅延実行**オプションを有効にすることにより、その要素の実行を延期することができます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-110">By turning on the <a name="DeferredXmlElementExecution"></a>**Deferred execution** option for an XML element in the configured format, you can defer (postpone) the execution of that element.</span></span> <span data-ttu-id="e0f39-111">この場合、親要素の他の要素すべてが実行されるまで、要素は実行されません。</span><span class="sxs-lookup"><span data-stu-id="e0f39-111">In this case, the element isn't run until all other elements of its parent have been run.</span></span>

<span data-ttu-id="e0f39-112">この機能の詳細を知るには、このトピックの例を実行します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-112">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="limitations"></a><span data-ttu-id="e0f39-113">制限</span><span class="sxs-lookup"><span data-stu-id="e0f39-113">Limitations</span></span>

<span data-ttu-id="e0f39-114">**遅延実行**オプションは、XML 形式で**送信**ドキュメントを生成するために使用される ER 形式に対してコンフィギュレーションされている XML 要素に対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-114">The **Deferred execution** option is supported only for XML elements that are configured for an ER format that is used to generate **outbound** documents in XML format.</span></span>

<span data-ttu-id="e0f39-115">**遅延実行**オプションは、他の 1 つの XML 要素にのみ配置される XML 要素に対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e0f39-115">The **Deferred execution** option is supported only for XML elements that reside in only one other XML element.</span></span> <span data-ttu-id="e0f39-116">したがって、他のタイプの形式要素に存在する XML 要素には適用されません (たとえば、**XML シーケンス**要素)。</span><span class="sxs-lookup"><span data-stu-id="e0f39-116">Therefore, it isn't applicable to XML elements that reside in other types of format elements (for example, in an **XML sequence** element).</span></span>

<span data-ttu-id="e0f39-117">**ファイルの分割**オプションが**はい**に設定されている場合、**遅延実行**オプションは、**共通\\ファイル**形式要素に存在する XML 要素にはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="e0f39-117">The **Deferred execution** option isn't supported for XML elements that reside in the **Common\\File** format element when the **Split file** option is set to **Yes**.</span></span> <span data-ttu-id="e0f39-118">XML ファイルを分割する方法の詳細については、[ファイル サイズおよびコンテンツ クオリティに基づいて生成された XML ファイルを分割する](er-split-files.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0f39-118">For more information about how to split XML files, see [Split generated XML files based on file size and content quantity](er-split-files.md).</span></span>

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a><span data-ttu-id="e0f39-119">例: ER 形式の XML 要素の実行の延期</span><span class="sxs-lookup"><span data-stu-id="e0f39-119">Example: Defer the execution of an XML element in an ER format</span></span>

<span data-ttu-id="e0f39-120">次のステップは、システム管理者または電子申告機能コンサルタント [ロール](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) のユーザーが、実行順序が形式階層の順序とは異なる XML 要素を含む ER 形式をコンフィギュレーションする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-120">The following steps explain how a user in the System administrator or Electronic reporting functional consultant [role](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) can configure an ER format that contains an XML element where the order of execution differs from the order in the format hierarchy.</span></span>

<span data-ttu-id="e0f39-121">これらのステップは、Microsoft Dynamics 365 Finance の **USMF** 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-121">These steps can be performed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e0f39-122">必要条件</span><span class="sxs-lookup"><span data-stu-id="e0f39-122">Prerequisites</span></span>

<span data-ttu-id="e0f39-123">この例を完了するには、次のいずれかのロール用の Finance の **USMF** 会社にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0f39-123">To complete this example, you must have access to the **USMF** company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="e0f39-124">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="e0f39-124">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="e0f39-125">システム管理者</span><span class="sxs-lookup"><span data-stu-id="e0f39-125">System administrator</span></span>

<span data-ttu-id="e0f39-126">[ER 形式におけるシーケンス要素の実行の延期](er-defer-sequence-element.md#Example) トピックの例をまだ完了していない場合、次のサンプル ER ソリューションの [コンフィギュレーション](general-electronic-reporting.md#Configuration) をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="e0f39-126">If you haven't yet completed the example in the [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) topic, download the following [configurations](general-electronic-reporting.md#Configuration) of the sample ER solution.</span></span>

| <span data-ttu-id="e0f39-127">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="e0f39-127">Content description</span></span>            | <span data-ttu-id="e0f39-128">ファイル名</span><span class="sxs-lookup"><span data-stu-id="e0f39-128">File name</span></span> |
|--------------------------------|-----------|
| <span data-ttu-id="e0f39-129">ER データ モデル構成</span><span class="sxs-lookup"><span data-stu-id="e0f39-129">ER data model configuration</span></span>    | [<span data-ttu-id="e0f39-130">遅延 elements.version.1.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="e0f39-130">Model to learn deferred elements.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="e0f39-131">ER モデル マッピング コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e0f39-131">ER model mapping configuration</span></span> | [<span data-ttu-id="e0f39-132">遅延 element.version.1.1.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="e0f39-132">Mapping to learn deferred elements.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

<span data-ttu-id="e0f39-133">開始する前に、サンプル ER ソリューションの次のコンフィギュレーションをローカル コンピューターにダウンロードして保存する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="e0f39-133">Before you begin, you must also download and save the following configuration of the sample ER solution to your local computer.</span></span>

| <span data-ttu-id="e0f39-134">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="e0f39-134">Content description</span></span>     | <span data-ttu-id="e0f39-135">ファイル名</span><span class="sxs-lookup"><span data-stu-id="e0f39-135">File name</span></span> |
|-------------------------|-----------|
| <span data-ttu-id="e0f39-136">ER フォーマット構成</span><span class="sxs-lookup"><span data-stu-id="e0f39-136">ER format configuration</span></span> | [<span data-ttu-id="e0f39-137">遅延 XML elements.version.1.1.xml を知るための形式</span><span class="sxs-lookup"><span data-stu-id="e0f39-137">Format to learn deferred XML elements.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a><span data-ttu-id="e0f39-138">サンプル ER のコンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="e0f39-138">Import the sample ER configurations</span></span>

1. <span data-ttu-id="e0f39-139">**組織管理** \> **ワークスペース** \> **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-139">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e0f39-140">**コンフィギュレーションをレポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-140">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e0f39-141">**コンフィギュレーション** ページで、**遅延要素を知るためのモデル** コンフィギュレーションがコンフィギュレーション ツリーで使用できない場合、ER データ モデル コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="e0f39-141">On the **Configurations** page, if the **Model to learn deferred elements** configuration isn't available in the configuration tree, import the ER data model configuration:</span></span>

    1. <span data-ttu-id="e0f39-142">**交換**を選択し、**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-142">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="e0f39-143">**参照**をクリックし、**遅延 elements.1.xml を知るためのモデル** ファイルを検索して選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0f39-143">Select **Browse**, find and select the **Model to learn deferred elements.1.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="e0f39-144">コンフィギュレーション ページで、**遅延要素を知るためのマッピング** コンフィギュレーションがコンフィギュレーション ツリーで使用できない場合、ER データ マッピング コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="e0f39-144">If the **Mapping to learn deferred elements** configuration isn't available in the configuration tree, import the ER model mapping configuration:</span></span>

    1. <span data-ttu-id="e0f39-145">**交換**を選択し、**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-145">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="e0f39-146">**参照**をクリックし、**遅延 elements.1.1.xml を知るためのマッピング** ファイルを検索して選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0f39-146">Select **Browse**, find and select the **Mapping to learn deferred elements.1.1.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="e0f39-147">ER 形式コンフィギュレーションのインポート:</span><span class="sxs-lookup"><span data-stu-id="e0f39-147">Import the ER format configuration:</span></span>

    1. <span data-ttu-id="e0f39-148">**交換**を選択し、**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-148">Select **Exchange**, and then select **Load from XML file**.</span></span>
    2. <span data-ttu-id="e0f39-149">**参照**をクリックし、**遅延 XML elements.1.1.xml を知るための形式** ファイルを検索して選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0f39-149">Select **Browse**, find and select the **Format to learn deferred XML elements.1.1.xml** file, and then select **OK**.</span></span>

6. <span data-ttu-id="e0f39-150">コンフィギュレーション ツリーで、**遅延要素を知るためのモデル**を展開します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-150">In the configuration tree, expand **Model to learn deferred elements**.</span></span>
7. <span data-ttu-id="e0f39-151">コンフィギュレーション ツリーでインポートされた ER コンフィギュレーションのリストを確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-151">Review the list of imported ER configurations in the configuration tree.</span></span>

    ![コンフィギュレーション ページのインポートされた ER コンフィギュレーション](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a><span data-ttu-id="e0f39-153">コンフィギュレーション プロバイダーの有効化</span><span class="sxs-lookup"><span data-stu-id="e0f39-153">Activate a configuration provider</span></span>

1. <span data-ttu-id="e0f39-154">**組織管理** \> **ワークスペース** \> **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-154">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e0f39-155">**ローカライズのコンフィギュレーション** ページの**コンフィギュレーション プロバイダー** セクションで、Litware, Inc. (`http://www.litware.com`) サンプル会社の [コンフィギュレーション プロバイダー](general-electronic-reporting.md#Provider) がリストに表示されていること、および有効としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-155">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the Litware, Inc. (`http://www.litware.com`) sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="e0f39-156">このコンフィギュレーション プロバイダーがリストに表示されない場合、またはアクティブとしてマークされていない場合、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](./tasks/er-configuration-provider-mark-it-active-2016-11.md) トピックの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="e0f39-156">If this configuration provider isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](./tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

    ![ローカライズのコンフィギュレーション ページの Litware, Inc. サンプル会社](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a><span data-ttu-id="e0f39-158">インポートされたモデル マッピングを確認する</span><span class="sxs-lookup"><span data-stu-id="e0f39-158">Review the imported model mapping</span></span>

<span data-ttu-id="e0f39-159">税トランザクションにアクセスするようにコンフィギュレーションされている ER モデル マッピング コンポーネントの設定を確認し、リクエスト時にアクセスしたデータを公開します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-159">Review the settings of the ER model mapping component that is configured to access tax transactions and expose accessed data on request.</span></span>

1. <span data-ttu-id="e0f39-160">**組織管理** \> **ワークスペース** \> **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-160">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e0f39-161">**コンフィギュレーションをレポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-161">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e0f39-162">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**遅延要素を知るためのモデル**を展開します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-162">On the **Configurations** page, in the configuration tree, expand **Model to learn deferred elements**.</span></span>
4. <span data-ttu-id="e0f39-163">**遅延要素を知るためのマッピング** コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-163">Select the **Mapping to learn deferred elements** configuration.</span></span>
5. <span data-ttu-id="e0f39-164">**デザイナー**を選択して、マッピングの一覧を開きます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-164">Select **Designer** to open the list of mappings.</span></span>
6. <span data-ttu-id="e0f39-165">**デザイナー**を選択して、マッピングの詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-165">Select **Designer** to review the mapping details.</span></span>
7. <span data-ttu-id="e0f39-166">**詳細を表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-166">Select **Show details**.</span></span>
8. <span data-ttu-id="e0f39-167">コンフィギュレーションされたデータ ソースを確認し、税トランザクションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e0f39-167">Review the data sources that are configured to access tax transactions:</span></span>

    - <span data-ttu-id="e0f39-168">*テーブル レコード タイプ*の**トランザクション** データ ソースは、**TaxTrans** アプリケーション テーブルのレコードにアクセスするようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="e0f39-168">The **Transactions** data source of the *Table record* type is configured to access records of the **TaxTrans** application table.</span></span>
    - <span data-ttu-id="e0f39-169">*計算済フィールド* タイプの**伝票**データ ソースは、必要な伝票コード (**INV-10000349** および **INV-10000350**) をレコードのリストとして返すようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="e0f39-169">The **Vouchers** data source of the *Calculated field* type is configured to return the required voucher codes (**INV-10000349** and **INV-10000350**) as a list of records.</span></span>
    - <span data-ttu-id="e0f39-170">**フィルター処理**された*計算済フィールド* タイプのデータソースは、**トランザクション** データ ソースから、必要な伝票の税トランザクションのみを選択するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="e0f39-170">The **Filtered** data source of the *Calculated field* type is configured to select, from the **Transactions** data source, only tax transactions of the required vouchers.</span></span>
    - <span data-ttu-id="e0f39-171">*計算済フィールド* タイプの **\$TaxAmount** フィールドは**フィルター処理**されたデータ ソースに対して追加され、反対の符号を持つ税額を公開します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-171">The **\$TaxAmount** field of the *Calculated field* type is added for the **Filtered** data source to expose the tax value that has the opposite sign.</span></span>
    - <span data-ttu-id="e0f39-172">**グループ化**された*グループ化*タイプのデータ ソースは、フィルター処理された**フィルター処理**データ ソースの税トランザクションをグループ化するようコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-172">The **Grouped** data source of the *Group By* type is configured to group filtered tax transactions of the **Filtered** data source.</span></span>
    - <span data-ttu-id="e0f39-173">**グループ化**されたデータ ソースの **TotalSum** 集計フィールドは、そのデータ ソースでフィルター処理されたすべての税トランザクションに対して、**フィルター処理**されたデータ ソースの**\$TaxAmount** フィールドの値を集計するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="e0f39-173">The **TotalSum** aggregation field of the **Grouped** data source is configured to summarize values of the **\$TaxAmount** field of the **Filtered** data source for all filtered tax transactions of that data source.</span></span>

        ![「GroupBy」パラメーターの編集ページの TotalSum 集計フィールド](./media/ER-DeferredXml-GroupByParameters.png)

9. <span data-ttu-id="e0f39-175">コンフィギュレーションされたデータ ソースをデータ モデルにバインドする方法、および ER 形式で利用可能になるようにアクセス データを公開する方法を確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-175">Review how the configured data sources are bound to the data model, and how they expose accessed data to make it available in an ER format:</span></span>

    - <span data-ttu-id="e0f39-176">**フィルター処理**されたデータ ソースは、データ モデルの **Data.List** フィールドにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-176">The **Filtered** data source is bound to the **Data.List** field of the data model.</span></span>
    - <span data-ttu-id="e0f39-177">**フィルター処理**されたデータ ソースの **\$TaxAmount** フィールドは、データ モデルの **Data.List.Value** フィールドにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-177">The **\$TaxAmount** field of the **Filtered** data source is bound to the **Data.List.Value** field of the data model.</span></span>
    - <span data-ttu-id="e0f39-178">**グループ化**されたデータ ソースの **TotalSum** フィールドは、データ モデルの **Data.Summary.Total** フィールドにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-178">The **TotalSum** field of the **Grouped** data source is bound to the **Data.Summary.Total** field of the data model.</span></span>

    ![モデル マッピング デザイナーのページ](./media/ER-DeferredXml-ModelMapping.png)

10. <span data-ttu-id="e0f39-180">**モデル マッピング デザイナー**および**モデル マッピング**のページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-180">Close the **Model mapping designer** and **Model mappings** pages.</span></span>

### <a name="review-the-imported-format"></a><span data-ttu-id="e0f39-181">インポートされた形式を確認する</span><span class="sxs-lookup"><span data-stu-id="e0f39-181">Review the imported format</span></span>

1. <span data-ttu-id="e0f39-182">**コンフィギュレーション** ツリーのコンフィギュレーション ページで、**遅延 XML 要素を知るための形式**コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-182">On the **Configurations** page, in the configuration tree, select the **Format to learn deferred XML elements** configuration.</span></span>
2. <span data-ttu-id="e0f39-183">**デザイナー**を選択して、形式の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-183">Select **Designer** to review the format details.</span></span>
3. <span data-ttu-id="e0f39-184">**詳細を表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-184">Select **Show details**.</span></span>
4. <span data-ttu-id="e0f39-185">税トランザクションの詳細を含む XML 形式で送信ドキュメントを生成するようにコンフィギュレーションされている ER フォーマット コンポーネントの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-185">Review the settings of the ER format components that are configured to generate an outbound document in XML format that includes details of the tax transactions:</span></span>

    - <span data-ttu-id="e0f39-186">**レポート\\メッセージ**の XML 要素は、入れ子になった XML 要素 (**ヘッダー**、**レコード**、および**集計**) を含む 1 つのノードで送信ドキュメントを入力するようにコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-186">The **Report\\Message** XML element is configured to fill the outbound document with a single node that includes the nested XML elements (**Header**, **Record**, and **Summary**).</span></span>
    - <span data-ttu-id="e0f39-187">**レポート\\メッセージ\\ヘッダー**の XML 要素は、1 つのヘッダー ノードで送信ドキュメントを入力するようにコンフィギュレーションされ、処理を開始するときに日時を表示します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-187">The **Report\\Message\\Header** XML element is configured to fill the outbound document with a single header node that shows the date and time when the processing starts.</span></span>
    - <span data-ttu-id="e0f39-188">**レポート\\メッセージ\\レコード**の XML 要素は、1 つのレコード ノードで送信ドキュメントを入力するようにコンフィギュレーションされ、1 つの税トランザクションの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-188">The **Report \\Message\\Record** XML element is configured to fill the outbound document with a single record node that shows the details of a single tax transaction.</span></span>
    - <span data-ttu-id="e0f39-189">**レポート\\メッセージ\\集計**の XML 要素は、1 つの集計ノードで送信ドキュメントを入力するようにコンフィギュレーションされ、処理された税トランザクションの税額の合計が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-189">The **Report\\Message\\Summary** XML element is configured to fill the outbound document with a single summary node that includes the sum of the tax values from the processed tax transactions.</span></span>

    ![形式デザイナー ページのメッセージの XML 要素と入れ子になった XML 要素](./media/ER-DeferredXml-Format.png)

5. <span data-ttu-id="e0f39-191">**マッピング** タブで、次の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-191">On the **Mapping** tab, review the following details:</span></span>

    - <span data-ttu-id="e0f39-192">**レポート\\メッセージ\\ヘッダー**要素は、送信ドキュメントの 1 つのノードを生成するのに、ソースにバインドする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e0f39-192">The **Report\\Message\\Header** element doesn't have to be bound to a source to generate a single node in an outbound document.</span></span>
    - <span data-ttu-id="e0f39-193">**ExecutionDateTime** 属性は、ヘッダー ノードが追加された時の日時 (ミリ秒を含む) を生成します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-193">The **ExecutionDateTime** attribute generates the date and time (including milliseconds) when the header node is added.</span></span>
    - <span data-ttu-id="e0f39-194">**レポート\\メッセージ\\レコード**要素は、**model.Data.List** リストにバインドされ、バインド リストからすべてのレコードに対して 1 レコード ノードを生成します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-194">The **Report\\Message\\Record** element is bound to the **model.Data.List** list to generate a single record node for every record from the bound list.</span></span>
    - <span data-ttu-id="e0f39-195">**TaxAmount** 属性は、**model.Data.List.Value** (相対パス ビューに **\@.Value** として表示される) にバインドされ、現在の税トランザクションの税額を生成します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-195">The **TaxAmount** attribute is bound to **model.Data.List.Value** (which is shown as **\@.Value** in the relative path view) to generate the tax value of the current tax transaction.</span></span>
    - <span data-ttu-id="e0f39-196">**RunningTotal** 属性は、税額累計額のプレースホルダーです。</span><span class="sxs-lookup"><span data-stu-id="e0f39-196">The **RunningTotal** attribute is a placeholder for the running total of the tax values.</span></span> <span data-ttu-id="e0f39-197">現在、バインディングも既定値もコンフィギュレーションされていないため、この属性には出力がありません。</span><span class="sxs-lookup"><span data-stu-id="e0f39-197">Currently, this attribute has no output, because neither a binding nor a default value is configured for it.</span></span>
    - <span data-ttu-id="e0f39-198">**ExecutionDateTime** 属性は、現在のトランザクションがこのレポートで処理される時の日時 (ミリ秒を含む) を生成します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-198">The **ExecutionDateTime** attribute generates the date and time (including milliseconds) when the current transaction is processed in this report.</span></span>
    - <span data-ttu-id="e0f39-199">**レポート\\メッセージ\\集計**要素は、送信ドキュメントの 1 つのノードを生成するのに、データ ソースにバインドする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e0f39-199">The **Report\\Message\\Summary** element doesn't have to be bound to a data source to generate a single node in an outbound document.</span></span>
    - <span data-ttu-id="e0f39-200">**TotalTaxAmount** 属性は **model.Data.Summary.Total** にバインドされ、処理された税トランザクションの税額合計を生成します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-200">The **TotalTaxAmount** attribute is bound to **model.Data.Summary.Total** to generate the sum of the tax values of the processed tax transactions.</span></span>
    - <span data-ttu-id="e0f39-201">**ExecutionDateTime** 属性は、集計ノードが追加された時の日時 (ミリ秒を含む) を生成します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-201">The **ExecutionDateTime** attribute generates the date and time (including milliseconds) when the summary node is added.</span></span>

    ![フォーマット デザイナー ページのマッピング タブ](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a><span data-ttu-id="e0f39-203">インポートされた ER 形式の実行</span><span class="sxs-lookup"><span data-stu-id="e0f39-203">Run the imported format</span></span>

1. <span data-ttu-id="e0f39-204">**フォーマット デザイナー** ページで、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-204">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="e0f39-205">Web ブラウザーからファイルをダウンロードし、確認のために開きます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-205">Download the file that the web browser offers, and open it for review.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredXml-Run.png)

<span data-ttu-id="e0f39-207">集計ノードには、処理されたトランザクションの税額の合計が示されます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-207">Notice that the summary node presents the sum of the tax values for the processed transactions.</span></span> <span data-ttu-id="e0f39-208">形式は、合計を返すようバインドされている **model.Data.Summary.Total** を使用するようにコンフィギュレーションされていて、合計はモデル マッピング内の *GroupBy* タイプで**グループ化**されたデータ ソースの **TotalSum** の集計を呼び出して計算されます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-208">Because the format is configured to use the **model.Data.Summary.Total** binding to return this sum, the sum is calculated by calling the **TotalSum** aggregation of the **Grouped** data source of the *GroupBy* type in the model mapping.</span></span> <span data-ttu-id="e0f39-209">この集計を計算するために、モデル マッピングは、**フィルター処理**されるデータ ソースで選択されたすべてのトランザクションを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-209">To calculate this aggregation, the model mapping iterates over all transactions that have been selected in the **Filtered** data source.</span></span> <span data-ttu-id="e0f39-210">集計ノードと最後のレコード ノードの実行時間を比較することにより、合計の計算に 12 ミリ秒 (ms) かかったことを特定できます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-210">By comparing the execution times of the summary node and the last record node, you can determine that calculation of the sum took 12 milliseconds (ms).</span></span> <span data-ttu-id="e0f39-211">最初と最後のレコード ノードの実行時間を比較することにより、すべてのレコード ノードの生成に 9 ミリ秒 (ms) かかったことを特定できます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-211">By comparing the execution times of the first and last record nodes, you can determine that generation of all record nodes took 9 ms.</span></span> <span data-ttu-id="e0f39-212">したがって、合計 21 ミリ秒必要でした。</span><span class="sxs-lookup"><span data-stu-id="e0f39-212">Therefore, a total of 21 ms was required.</span></span>

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a><span data-ttu-id="e0f39-213">計算が生成された出力に基づくように形式を変更する</span><span class="sxs-lookup"><span data-stu-id="e0f39-213">Modify the format so that the calculation is based on generated output</span></span>

<span data-ttu-id="e0f39-214">トランザクションの量が現在の例のボリュームよりも大きい場合、計算時間が増加してパフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e0f39-214">If the volume of transaction is much larger than the volume in the current example, the calculation time might increase and cause performance issues.</span></span> <span data-ttu-id="e0f39-215">形式の設定を変更することにより、これらパフォーマンスの問題を防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-215">By changing the setting of the format, you can help prevent these performance issues.</span></span> <span data-ttu-id="e0f39-216">税額にアクセスして生成されたレポートに含めることができるため、この情報を再利用して税額を計算することができます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-216">Because you access tax values to include them in the generated report, you can reuse this information to calculate tax values.</span></span> <span data-ttu-id="e0f39-217">詳細については、[集計と合計を行うよう形式をコンフィギュレーションする](./tasks/er-format-counting-summing-1.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0f39-217">For more information, see [Configure format to do counting and summing](./tasks/er-format-counting-summing-1.md).</span></span>

1. <span data-ttu-id="e0f39-218">**形式**タブの**形式デザイナー** ページで、形式ツリーの**レポート** ファイル要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-218">On the **Format designer** page, on the **Format** tab, select the **Report** file element in the format tree.</span></span>
2. <span data-ttu-id="e0f39-219">**出力詳細の収集**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-219">Set the **Collect output details** option to **Yes**.</span></span> <span data-ttu-id="e0f39-220">[データ収集](er-functions-category-data-collection.md) カテゴリの組み込み ER 機能を使用してアクセスできるデータ ソースとして生成されたレポートの内容を使用することで、この形式をコンフィギュレーションできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e0f39-220">You can now configure this format by using the content of a generated report as a data source that can be accessed by using the built-in ER functions in the [Data collection](er-functions-category-data-collection.md) category.</span></span>
3. <span data-ttu-id="e0f39-221">**マッピング** タブで、**レポート\\メッセージ\\レコード** XML 要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-221">On the **Mapping** tab, select the **Report\\Message\\Record** XML element.</span></span>
4. <span data-ttu-id="e0f39-222">**収集したデータ キー名**の式を `WsColumn` としてコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="e0f39-222">Configure the **Collected data key name** expression as `WsColumn`.</span></span>
5. <span data-ttu-id="e0f39-223">**収集したデータ キーの値**の式を `WsRow` としてコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="e0f39-223">Configure the **Collected data key value** expression as `WsRow`.</span></span>

    ![形式デザイナー ページのレコード XML 要素](./media/ER-DeferredXml-Format3.png)

6. <span data-ttu-id="e0f39-225">**レポート\\メッセージ\\レコード\\TaxAmount** 属性を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-225">Select the **Report\\Message\\Record\\TaxAmount** attribute.</span></span>
7. <span data-ttu-id="e0f39-226">**収集したデータ キー名**の式を `SummingAmountKey` としてコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="e0f39-226">Configure the **Collected data key name** expression as `SummingAmountKey`.</span></span>

    ![形式デザイナー ページの TaxAmount 属性](./media/ER-DeferredXml-Format4.png)

    <span data-ttu-id="e0f39-228">セル A1 の値が処理されたすべての税トランザクションからの税額の値で追記されている、この仮想ワークシートのフルフィルメントの設定を考慮することができます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-228">You can consider this setting the fulfillment of a virtual worksheet, where the value of cell A1 is appended with the value of the tax amount from every processed tax transaction.</span></span>

8. <span data-ttu-id="e0f39-229">**レポート\\メッセージ\\レコード\\RunningTotal** 属性を選択し、**フォーミュラの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-229">Select the **Report\\Message\\Record\\RunningTotal** attribute, and then select **Edit formula**.</span></span>
9. <span data-ttu-id="e0f39-230">組み込みの [SUMIF](er-functions-datacollection-sumif.md) ER 関数を使用して `SUMIF(SummingAmountKey, WsColumn, WsRow)` 式をコンフィギュレーションし、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-230">Configure the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression by using the built-in [SUMIF](er-functions-datacollection-sumif.md) ER function, and then select **Save**.</span></span>

    ![SUMIF 式](./media/ER-DeferredXml-FormulaDesigner.png)

10. <span data-ttu-id="e0f39-232">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-232">Close the **Formula designer** page.</span></span>
11. <span data-ttu-id="e0f39-233">**保存**を選択して、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-233">Select **Save**, and then select **Run**.</span></span>
12. <span data-ttu-id="e0f39-234">Web ブラウザーからファイルをダウンロードし、確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-234">Download and review the file that the web browser offers.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredXml-Run1.png)

    <span data-ttu-id="e0f39-236">最後のレコード ノードには、生成された出力をデータ ソースとして使用することにより、処理されたすべてのトランザクションに対して計算される税額の累計が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-236">The last record node contains the running total of tax values that is calculated for all processed transactions by using the generated output as a data source.</span></span> <span data-ttu-id="e0f39-237">このデータ ソースは、レポートの先頭から開始し、最後の税トランザクションまで続行します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-237">This data source starts from the beginning of the report and continues through the last tax transaction.</span></span> <span data-ttu-id="e0f39-238">集計ノードには、モデル マッピングにおいて *GroupBy* タイプのデータ ソースを使用して計算され、処理されたすべてのトランザクションの税額の合計が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e0f39-238">The summary node contains the sum of the tax values for all processed transactions that are calculated in the model mapping by using the data source of the *GroupBy* type.</span></span> <span data-ttu-id="e0f39-239">これらの値は等しくなります。</span><span class="sxs-lookup"><span data-stu-id="e0f39-239">Notice that these values are equal.</span></span> <span data-ttu-id="e0f39-240">したがって、**GroupBy** の代わりに出力ベースの合計を使用できます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-240">Therefore, the output-based summing can be used instead of **GroupBy**.</span></span> <span data-ttu-id="e0f39-241">最初のノードと集計ノードの実行時間を比較することにより、すべてのレコード ノードの生成および合計に 11 ミリ秒 (ms) かかったことを特定できます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-241">By comparing the execution times of the first record node and the summary node, you can determine that generation of all the record nodes and summing took 11 ms.</span></span> <span data-ttu-id="e0f39-242">したがって、レコード ノードおよび税額の合計の生成が懸念されるかぎり、変更された形式は元の形式よりも約 2 倍速くなります。</span><span class="sxs-lookup"><span data-stu-id="e0f39-242">Therefore, as far as the generation of record nodes and the summing of tax values are concerned, the modified format is approximately two times faster than the original format.</span></span>

13. <span data-ttu-id="e0f39-243">**レポート\\メッセージ\\集計\\TotalTaxAmount** 属性を選択し、**フォーミュラの編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-243">Select the **Report\\Message\\Summary\\TotalTaxAmount** attribute, and then select **Edit formula**.</span></span>
14. <span data-ttu-id="e0f39-244">既存の式の代わりに `SUMIF(SummingAmountKey, WsColumn, WsRow)` 式を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-244">Enter the `SUMIF(SummingAmountKey, WsColumn, WsRow)` expression instead of the existing expression.</span></span>
15. <span data-ttu-id="e0f39-245">**保存**を選択して、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-245">Select **Save**, and then select **Run**.</span></span>
16. <span data-ttu-id="e0f39-246">Web ブラウザーからファイルをダウンロードし、確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-246">Download and review the file that the web browser offers.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredXml-Run2.png)

    <span data-ttu-id="e0f39-248">最後のレコード ノードの税額累計は、集計ノードの合計値と等しくなるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e0f39-248">Notice that the running total of tax values in the last record node now equals the sum in the summary node.</span></span>

### <a name="put-values-of-output-based-summing-in-the-report-header"></a><span data-ttu-id="e0f39-249">レポート ヘッダーに出力ベースの集計を配置する</span><span class="sxs-lookup"><span data-stu-id="e0f39-249">Put values of output-based summing in the report header</span></span>

<span data-ttu-id="e0f39-250">たとえば、レポートのヘッダーに税額の合計を表示する必要がある場合、形式を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-250">If, for example, you must present the sum of tax values in the header of your report, you can modify your format.</span></span>

1. <span data-ttu-id="e0f39-251">**形式**タブの**形式デザイナー** ページで、**レポート\\メッセージ\\集計**XML 要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-251">On the **Format designer** page, on the **Format** tab, select the **Report\\Message\\Summary** XML element.</span></span>
2. <span data-ttu-id="e0f39-252">**上へ移動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-252">Select **Move up**.</span></span>
3. <span data-ttu-id="e0f39-253">**保存**を選択して、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-253">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="e0f39-254">Web ブラウザーからファイルをダウンロードし、確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-254">Download and review the file that the web browser offers.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredXml-Run3.png)

    <span data-ttu-id="e0f39-256">この合計が生成された出力に基づいて計算されるようになったので、集計ノードの税額の合計は 0 (ゼロ) と等しくなるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e0f39-256">Notice that the sum of tax values in the summary node now equals 0 (zero), because this sum is now calculated based on the generated output.</span></span> <span data-ttu-id="e0f39-257">最初のレコード ノードが生成される時、生成された出力にはまだトランザクションの詳細のあるレコード ノードは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="e0f39-257">When the first record node is generated, the generated output doesn't yet contain record nodes that have transaction details.</span></span> <span data-ttu-id="e0f39-258">この形式をコンフィギュレーションして、すべての税トランザクションに対して**レポート\\メッセージ\\レコード**の要素が実行されるまで、**レポート\\メッセージ\\集計**の要素の実行を延期させることができます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-258">You can configure this format to defer the execution of the **Report\\Message\\Summary** element until the **Report\\Message\\Record** element has been run for all tax transactions.</span></span>

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a><span data-ttu-id="e0f39-259">集計 XML 要素の実行を延期することにより、計算された合計が使用されます</span><span class="sxs-lookup"><span data-stu-id="e0f39-259">Defer the execution of the summary XML element so that the calculated total is used</span></span>

1. <span data-ttu-id="e0f39-260">**形式**タブの**形式デザイナー** ページで、**レポート\\メッセージ\\集計**XML 要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-260">On the **Format designer** page, on the **Format** tab, select the **Report\\Message\\Summary** XML element.</span></span>
2. <span data-ttu-id="e0f39-261">**遅延実行**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-261">Set the **Deferred execution** option to **Yes**.</span></span>

    ![形式デザイナー ページの集計 XML 要素の遅延実行オプション](./media/ER-DeferredXml-Format5.png)

3. <span data-ttu-id="e0f39-263">**保存**を選択して、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-263">Select **Save**, and then select **Run**.</span></span>
4. <span data-ttu-id="e0f39-264">Web ブラウザーからファイルをダウンロードし、確認します。</span><span class="sxs-lookup"><span data-stu-id="e0f39-264">Download and review the file that the web browser offers.</span></span>

    ![ダウンロードされたファイル](./media/ER-DeferredXml-Run4.png)

    <span data-ttu-id="e0f39-266">**レポート\\メッセージ\\集計**の要素は、その親要素である**レポート\\メッセージ**の下に入れ子になっている他のすべての品目が実行された後に実行されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e0f39-266">The **Report\\Message\\Summary** element is now run only after all other items that are nested under its parent element, **Report\\Message**, have been run.</span></span> <span data-ttu-id="e0f39-267">したがって、**レポート\\メッセージ\\レコード**の要素が **model.Data.List** データ ソースのすべての税トランザクションに実行された後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e0f39-267">Therefore, it's run after the **Report\\Message\\Record** element has been run for all tax transactions of the **model.Data.List** data source.</span></span> <span data-ttu-id="e0f39-268">最初と最後のレコード ノードの実行時間、およびヘッダーと集計ノードの実行時間は、この事実を示しています。</span><span class="sxs-lookup"><span data-stu-id="e0f39-268">The execution times of the first and last record nodes, and of the header and summary nodes, reveal this fact.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0f39-269">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e0f39-269">Additional resources</span></span>

- [<span data-ttu-id="e0f39-270">棚卸および集計を行うための形式のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e0f39-270">Configure format to do counting and summing</span></span>](./tasks/er-format-counting-summing-1.md)
- [<span data-ttu-id="e0f39-271">パフォーマンス上の問題をトラブルシューティングするため ER 形式の追跡実行</span><span class="sxs-lookup"><span data-stu-id="e0f39-271">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="e0f39-272">ER 形式におけるシーケンス要素の実行の延期</span><span class="sxs-lookup"><span data-stu-id="e0f39-272">Defer the execution of sequence elements in ER formats</span></span>](er-defer-sequence-element.md#Example)
