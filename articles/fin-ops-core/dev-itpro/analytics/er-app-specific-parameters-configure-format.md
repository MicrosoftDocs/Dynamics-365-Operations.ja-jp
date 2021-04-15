---
title: 法人ごとに指定されたパラメーターを使用するよう ER 形式を構成する
description: このトピックでは、法人ごと指定されたパラメーターを使用して電子申告 (ER) 形式を構成する方法について説明します。
author: NickSelin
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 16eab3ffa7d4a780ec9709f5c8a5c263b1e75365
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751181"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="198b8-103">法人ごとに指定されたパラメーターを使用するよう ER 形式を構成する</span><span class="sxs-lookup"><span data-stu-id="198b8-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="198b8-104">概要</span><span class="sxs-lookup"><span data-stu-id="198b8-104">Overview</span></span>

<span data-ttu-id="198b8-105">設計する電子申告 (ER) の多くの形式では、インスタンスの各法人に固有の値セット (税取引をフィルター処理するための税コードセットなど) を使用してデータをフィルター処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="198b8-106">現時点では、このタイプのフィルター処理が ER 形式で構成されている場合、ER 形式の式でデータフィルター処理ルールを指定するために、法人に依存する値 (税コードなど) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="198b8-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="198b8-107">したがって、ER 形式は法人固有のものであり、必要なレポートを生成するには、ER 形式を実行する必要がある各法人に対して元の ER 形式の派生コピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="198b8-108">元の (ベース) バージョンが更新され、テスト環境からエクスポートされて、本番用に配置する必要がある場合は、テスト環境からエクスポートされて、本番環境にインポートされると、各派生 ER 形式によって、法人固有の値を取り込めるように編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="198b8-109">したがって、このように構成されたこのタイプの ER ソリューションのメンテナンスは、次のような理由から、非常に複雑で時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="198b8-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="198b8-110">法人の数が多い場合は、より多くの ER 形式の構成を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="198b8-111">ER の構成を保守するには、ビジネスユーザーが ER の情報を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="198b8-112">ER アプリケーション固有のパラメーター機能を使用すると、パワーユーザーはデータフィルターを ER 形式に構成して、一連の抽象的なルールに基づくようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="198b8-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="198b8-113">このルールセットは、ER 形式で使用可能なデータソースを使用するように構成できます。</span><span class="sxs-lookup"><span data-stu-id="198b8-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="198b8-114">ビジネスユーザーは ER フレームワークを超えた実際のルールを、対応する ER 形式の設定に基づいて自動的に生成されるユーザーインターフェイス (UI) と、ER 形式のデータソースからアクセスされる現在の法人データを使用して指定できます。</span><span class="sxs-lookup"><span data-stu-id="198b8-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="198b8-115">ER 形式に対して指定されている一連のルールは、Dynamics 365 Finance (財務) インスタンスの現在の法人からエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="198b8-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="198b8-116">その後、同じ財務のインスタンスまたは異なるインスタンスの別の法人に、同じ ER 形式のルールセットとしてインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="198b8-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="198b8-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="198b8-117">Prerequisites</span></span>

<span data-ttu-id="198b8-118">このトピックの例を完了するには、次のいずれかの役割で、財務と同じテナントに対してプロビジョニングされている Regulatory Configuration Services (RCS) のインスタンスにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="198b8-119">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="198b8-119">Electronic reporting developer</span></span>
- <span data-ttu-id="198b8-120">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="198b8-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="198b8-121">システム管理者</span><span class="sxs-lookup"><span data-stu-id="198b8-121">System administrator</span></span>

<span data-ttu-id="198b8-122">[CALCULATED FIELD タイプの ER データソースのパラメーター化された呼び出しをサポート](er-calculated-field-type.md) トピックの手順を実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="198b8-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="198b8-123">これらの手順を既に完了している場合は、この後の **ER 構成を RCS にインポートする** セクションの手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="198b8-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="198b8-124">ER 構成を RCS にインポートする</span><span class="sxs-lookup"><span data-stu-id="198b8-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="198b8-125">次の ER コンフィギュレーションをダウンロードし、ローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="198b8-125">Download and locally store the following ER configurations.</span></span>

| <span data-ttu-id="198b8-126">**コンテンツの説明**</span><span class="sxs-lookup"><span data-stu-id="198b8-126">**Content description**</span></span>                        | <span data-ttu-id="198b8-127">**ファイル名**</span><span class="sxs-lookup"><span data-stu-id="198b8-127">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="198b8-128">**ER データ モデル** 構成ファイルのサンプル</span><span class="sxs-lookup"><span data-stu-id="198b8-128">Sample **ER data model** configuration file</span></span>    | [<span data-ttu-id="198b8-129">パラメーター化された呼び出し version.1.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="198b8-129">Model to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| <span data-ttu-id="198b8-130">**ER メタデータ** 構成ファイルのサンプル</span><span class="sxs-lookup"><span data-stu-id="198b8-130">Sample **ER metadata** configuration file</span></span>      | [<span data-ttu-id="198b8-131">パラメーター化された呼び出し version.1.xml を知るためのメタデータ</span><span class="sxs-lookup"><span data-stu-id="198b8-131">Metadata to learn parameterized calls.version.1.xml</span></span>](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| <span data-ttu-id="198b8-132">**ER モデル マッピング** 構成ファイルのサンプル</span><span class="sxs-lookup"><span data-stu-id="198b8-132">Sample **ER model mapping** configuration file</span></span> | [<span data-ttu-id="198b8-133">パラメーター化された呼び出し version.1.1.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="198b8-133">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| <span data-ttu-id="198b8-134">**ER 形式** 構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="198b8-134">Sample **ER format** configuration</span></span>             | [<span data-ttu-id="198b8-135">パラメーター化された呼び出し version.1.1.xml を知るための形式</span><span class="sxs-lookup"><span data-stu-id="198b8-135">Format to learn parameterized calls.version.1.1.xml</span></span>](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

<span data-ttu-id="198b8-136">次に、RCS インスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="198b8-136">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="198b8-137">この例では、Litware、Inc. サンプル会社の構成を作成します。</span><span class="sxs-lookup"><span data-stu-id="198b8-137">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="198b8-138">この手順を完了する前に、RCS で [ER 構成 プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md)トピックにある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-138">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="198b8-139">既定のダッシュボードで、**電子申告** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-139">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="198b8-140">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-140">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="198b8-141">RCS にダウンロードした ER コンフィギュレーションを、次の順序で RCS にインポートします。データ モデル、メタデータ、モデル マッピング、フォーマット。</span><span class="sxs-lookup"><span data-stu-id="198b8-141">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="198b8-142">各 ER コンフィギュレーションについて、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="198b8-142">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="198b8-143">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-143">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="198b8-144">**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-144">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="198b8-145">**参照** を選択して、必要な ER コンフィギュレーションファイルを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-145">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="198b8-146">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-146">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="198b8-147">指定された ER ソリューションを確認する</span><span class="sxs-lookup"><span data-stu-id="198b8-147">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="198b8-148">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し** の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="198b8-148">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="198b8-149">**パラメーター化された呼び出しを知るための形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-149">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="198b8-150">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="198b8-150">Select **Designer**.</span></span>
4.  <span data-ttu-id="198b8-151">**展開 / 折りたたみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-151">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="198b8-152">**パラメーター化された呼び出しを学習するための形式** の ER 形式は、(標準、減額、なし) という複数の課税レベルを提供する XML 形式の税明細書を生成するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="198b8-152">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="198b8-153">各レベルには異なる数の詳細情報があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-153">Each level has a different number of details.</span></span>

    ![複数レベルの ER 形式、パラメーター化された呼び出しを学習する形式](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="198b8-155">**マッピング** タブで、**モデル**、**データ**、および **概要** 品目を展開します。</span><span class="sxs-lookup"><span data-stu-id="198b8-155">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="198b8-156">**Model.Data.Summary** データ ソースは、税トランザクションの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="198b8-156">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="198b8-157">それらのトランザクションは税コードごとに集計されます。</span><span class="sxs-lookup"><span data-stu-id="198b8-157">These transactions are summarized by tax code.</span></span> <span data-ttu-id="198b8-158">このデータ ソースについて **Model.Data.Summary.Level** の計算フィールドが、集計された各レコードの課税レベルのコードを返すように構成されています。</span><span class="sxs-lookup"><span data-stu-id="198b8-158">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="198b8-159">実行時に **Model.Data.Summary** データ ソースから取得できる税コードの場合、計算済みフィールドは、課税レベル コード (**標準**、**減額**、**なし**、または **その他**) テキスト値として返します。</span><span class="sxs-lookup"><span data-stu-id="198b8-159">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="198b8-160">**Model.Data.Summary.Level** 計算済みフィールドは、**Model.Data.Summary** データ ソースのレコードをフィルター処理し、**Model.Data2.Level1**、**Model.Data2.Level2**、**Model.Data2.Level3** を使用して課税レベルを表す各 XML 要素にフィルター処理されたデータを入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="198b8-160">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![税トランザクションの Model.Data.Summary データ ソース](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="198b8-162">**Model.Data.Summary.Level** の計算済みフィールドは、ER 式を含むように構成されています。</span><span class="sxs-lookup"><span data-stu-id="198b8-162">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="198b8-163">税コード (**VAT19**、**InVAT19**、**VAT7**、**InVAT7**、**THIRD**、**InVAT0**) は、この構成にハードコードされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="198b8-163">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="198b8-164">したがって、この ER 形式は、税コードが構成された法人に依存しています。</span><span class="sxs-lookup"><span data-stu-id="198b8-164">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![Model.Data.Summary.Level の計算済フィールド (ハードコードが設定された税コード付き)](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="198b8-166">法人ごとに異なる税コードのセットをサポートするには、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-166">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="198b8-167">法人ごとに ER 形式の派生バージョンを作成します。</span><span class="sxs-lookup"><span data-stu-id="198b8-167">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="198b8-168">法人設定に基づいて、**Model.Data.Summary.Level** 計算済みフィールドで税コードを更新します。</span><span class="sxs-lookup"><span data-stu-id="198b8-168">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="198b8-169">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="198b8-169">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="198b8-170">派生形式を作成する</span><span class="sxs-lookup"><span data-stu-id="198b8-170">Create a derived format</span></span>

<span data-ttu-id="198b8-171">次に、ER アプリケーション固有のパラメーター機能を使用して、1 つの ER 形式に含まれる各法人の税コードの異なるセットをサポートします。</span><span class="sxs-lookup"><span data-stu-id="198b8-171">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="198b8-172">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し** の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="198b8-172">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="198b8-173">**パラメーター化された呼び出しを知るための形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-173">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="198b8-174">**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-174">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="198b8-175">**名前から派生: パラメーター化された呼び出しを知るための形式、Microsoft** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-175">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="198b8-176">**名前** フィールドに、**LE データの参照方法を知るための形式** を入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-176">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="198b8-177">**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-177">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="198b8-178">派生形式のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="198b8-178">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="198b8-179">形式列挙型の追加</span><span class="sxs-lookup"><span data-stu-id="198b8-179">Add a format enumeration</span></span>

<span data-ttu-id="198b8-180">次に、新しい ER 形式列挙型を追加します。</span><span class="sxs-lookup"><span data-stu-id="198b8-180">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="198b8-181">この形式の列挙型の値は、ビジネスユーザーに対して表示され、ER 形式で使用されるさまざまな課税レベルの法人固有の税コードのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="198b8-181">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="198b8-182">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="198b8-182">Select **Designer**.</span></span>
2.  <span data-ttu-id="198b8-183">**形式列挙型** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-183">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="198b8-184">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-184">Select **Add**.</span></span>
4.  <span data-ttu-id="198b8-185">**名前** フィールドに、**課税レベルの一覧** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-185">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="198b8-186">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-186">Select **Save**.</span></span>
6.  <span data-ttu-id="198b8-187">**形式列挙型の値** タブで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-187">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="198b8-188">**名前** フィールドに、**通常の課税** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-188">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="198b8-189">**追加** を再度選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-189">Select **Add** again.</span></span>
9.  <span data-ttu-id="198b8-190">**名前** フィールドに、**減額課税** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-190">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="198b8-191">**追加** を再度選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-191">Select **Add** again.</span></span>
11. <span data-ttu-id="198b8-192">**名前** フィールドに、**非課税** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-192">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="198b8-193">**追加** を再度選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-193">Select **Add** again.</span></span>
13. <span data-ttu-id="198b8-194">**名前** フィールドに、**その他** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-194">In the **Name** field, enter **Other**.</span></span>

    ![[形式列挙型] ページの新しいレコード](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="198b8-196">ビジネスユーザーは、異なる言語を使用して、法人に依存する税コードのセットを指定する場合があるため、この列挙型の値を、財務のユーザーの優先言語として構成された言語に翻訳することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="198b8-196">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="198b8-197">**非課税** レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-197">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="198b8-198">**ラベル** フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="198b8-198">Click in the **Label** field.</span></span>
16. <span data-ttu-id="198b8-199">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-199">Select **Translate**.</span></span>
17. <span data-ttu-id="198b8-200">**テキストの翻訳** ウィンドウの **ラベル Id** フィールドに、**LBL_LEVELENUM_NO** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-200">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="198b8-201">**既定の言語のテキスト** フィールドに **非課税** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-201">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="198b8-202">**言語** フィールドで、**DE** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-202">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="198b8-203">**翻訳テキスト** フィールドで、**keine Besteuerung** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-203">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="198b8-204">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-204">Select **Translate**.</span></span>

    ![テキスト翻訳のスライド アウト](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="198b8-206">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-206">Select **Save**.</span></span>
23. <span data-ttu-id="198b8-207">**形式列挙型** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="198b8-207">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="198b8-208">新しいルックアップ データ ソースを追加する</span><span class="sxs-lookup"><span data-stu-id="198b8-208">Add a new lookup data source</span></span>

<span data-ttu-id="198b8-209">次に、新しいデータソースを追加して、ビジネスユーザーが、集計された各トランザクション レコードに対して正しい課税レベルを認識するための法人依存ルールをどのように指定するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="198b8-209">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="198b8-210">**マッピング** タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-210">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="198b8-211">**形式列挙型\ルックアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-211">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="198b8-212">ビジネス ユーザーが課税レベルの認識に指定した各ルールが ER 形式列挙型の値を返すことを確認しました。</span><span class="sxs-lookup"><span data-stu-id="198b8-212">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="198b8-213">**ルックアップ** データ ソース タイプには、**形式列挙型** ブロックに加えて、**データ モデル** および **Dynamics 365 for Operations** ブロックでもアクセスできる点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="198b8-213">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="198b8-214">したがって、ER データ モデルの列挙型とアプリケーションの列挙型を使用して、その型のデータ ソースに対して返される値の型を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="198b8-214">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="198b8-215">**名前** フィールドに、**セレクター** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-215">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="198b8-216">**形式列挙型** フィールドで、**課税レベルの一覧** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-216">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="198b8-217">このデータ ソースで指定されているルールごとに、ビジネス ユーザーは、**課税レベルの一覧** 形式列挙型の値のいずれかを戻り値として選択する必要があることを指定しました。</span><span class="sxs-lookup"><span data-stu-id="198b8-217">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="198b8-218">**ルックアップの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-218">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="198b8-219">**列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-219">Select **Columns**.</span></span>
7.  <span data-ttu-id="198b8-220">**モデル** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="198b8-220">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="198b8-221">**データ** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="198b8-221">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="198b8-222">**税** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="198b8-222">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="198b8-223">**Model.Data.Tax.Code** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-223">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="198b8-224">**追加** ボタン (右矢印) を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-224">Select the **Add** button (the right arrow).</span></span>

    ![列のスライド アウト](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="198b8-226">課税レベルの認識のためにこのデータ ソースで指定されている各ルールについて、ビジネス ユーザーが条件として税コードの 1 つを選択する必要があることを指定しました。</span><span class="sxs-lookup"><span data-stu-id="198b8-226">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="198b8-227">ビジネス ユーザーが選択できる税コードの一覧は、**Model.Data.Tax** データ ソースよって返されます。</span><span class="sxs-lookup"><span data-stu-id="198b8-227">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="198b8-228">このデータ ソースには **名前** フィールドが含まれているため、ビジネス ユーザーに対して表示されるルックアップの各税コード値について、税コードの名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="198b8-228">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="198b8-229">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-229">Select **OK**.</span></span>

    ![ルックアップ デザイナー ページ](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="198b8-231">ビジネス ユーザーは、このデータ ソースのレコードとして、複数のルールを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="198b8-231">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="198b8-232">各レコードには、明細行コードで番号が付けられます。</span><span class="sxs-lookup"><span data-stu-id="198b8-232">Each record will be numbered by a line code.</span></span> <span data-ttu-id="198b8-233">ルールは行番号の昇順で評価されます。</span><span class="sxs-lookup"><span data-stu-id="198b8-233">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="198b8-234">**税コード** フィールドはこのルックアップ データ ソースのルールの条件として選択されており、**税コード** は **文字列** データ型のフィールドとして設定されているため、各ルールは、データ ソースに渡される税コードと、データ ソースのレコードで定義されている税コードとを比較することによって、実行時に評価されます。</span><span class="sxs-lookup"><span data-stu-id="198b8-234">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="198b8-235">構成された条件を満たすルールが見つかった場合、このデータ ソースは、**ルックアップの結果** フィールドに定義されているルールのルックアップ値を返します。</span><span class="sxs-lookup"><span data-stu-id="198b8-235">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="198b8-236">ルールが見つからない場合は、現在のデータ ソースが正しい値を返すことができないことをユーザーに通知する例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="198b8-236">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="198b8-237">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-237">Select **Save**.</span></span>
14. <span data-ttu-id="198b8-238">**ルックアップ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="198b8-238">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="198b8-239">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-239">Select **OK**.</span></span>

    <span data-ttu-id="198b8-240">**文字列** データ型の **コード** パラメーターの引数としてデータ ソースに渡されたすべての税コードの **課税レベル リスト** の形式列挙型の値として、課税レベルを返す新しいデータ ソースを追加したことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="198b8-240">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![新しいデータ ソースが表示されたで形式デザイナー ページ](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="198b8-242">構成されたルールの評価は、そのルールの条件を定義するために選択されたフィールドのデータ型に依存することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="198b8-242">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="198b8-243">**数値** データ型または **日付** データ型のフィールドとして構成されているフィールドを選択した場合、基準は **文字列** データ型に対して既に説明した基準とは異なります。</span><span class="sxs-lookup"><span data-stu-id="198b8-243">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="198b8-244">**数値** フィールドおよび **日付** フィールドでは、ルールを値の範囲として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-244">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="198b8-245">データ ソースに渡される値が構成された範囲内にある場合は、ルールの条件が満たされたと見なされます。</span><span class="sxs-lookup"><span data-stu-id="198b8-245">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="198b8-246">次の図は、この種類の設定の例を示します。</span><span class="sxs-lookup"><span data-stu-id="198b8-246">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="198b8-247">**文字列** データ型の **Model.Data.Tax.Code** フィールドに加えて、**リアル** データ型の **Model.Tax.Summary.Base** フィールドを使用して、ルックアップ データ ソースの条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="198b8-247">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![追加の列を含むルックアップ デザイナー ページ](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="198b8-249">このルックアップ データ ソースに対して **Model.Data.Tax.Code** フィールドおよび **Model.Tax.Summary.Base** が選択されます。このデータ ソースの各ルールは、次のように構成されます。</span><span class="sxs-lookup"><span data-stu-id="198b8-249">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="198b8-250">表示される一覧で、**課税レベルの一覧** 形式列挙型の値を戻り値として選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-250">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="198b8-251">この税コードは、このルールの条件として入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-251">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="198b8-252">**Model.Data.Tax** データ ソースによって提供される税コードのみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="198b8-252">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="198b8-253">税基準額の最小値と最大値は、このルールの条件として入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="198b8-253">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="198b8-254">次は、このデータ ソースの各ルールを実行時に評価する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="198b8-254">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="198b8-255">このデータ ソースに渡された **文字列** データ型のコードがルールの税コードと同等か?</span><span class="sxs-lookup"><span data-stu-id="198b8-255">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="198b8-256">このデータ ソースに渡された **リアル** データ型の値が、特定の最小値と最大値の範囲内に収まっているか?</span><span class="sxs-lookup"><span data-stu-id="198b8-256">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="198b8-257">両方の条件が満たされると、ルールが適用可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="198b8-257">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="198b8-258">追加されたルックアップ データ ソースのラベルを翻訳する</span><span class="sxs-lookup"><span data-stu-id="198b8-258">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="198b8-259">ビジネス ユーザーは、異なる言語を使用して、法人に依存する税コードのセットを指定する場合があるため、追加するルックアップ データ ソースのラベルを翻訳し、対応するページで各ユーザーの優先言語で表示することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="198b8-259">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="198b8-260">**Model.Data.Selector** データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-260">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="198b8-261">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-261">Select **Edit**.</span></span>
3.  <span data-ttu-id="198b8-262">**ラベル** フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="198b8-262">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="198b8-263">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-263">Select **Translate**.</span></span>
5.  <span data-ttu-id="198b8-264">**テキストの翻訳** ウィンドウの **ラベル Id** フィールドに、**LBL_SELECTOR_DS** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-264">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="198b8-265">**既定の言語のテキスト** フィールドに、**税コードによる税レベルの選択** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-265">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="198b8-266">**言語** フィールドで、**DE** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-266">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="198b8-267">**翻訳テキスト** フィールドに,**Steuerebene für Steuerkennzeichen auswählen** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-267">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="198b8-268">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-268">Select **Translate**.</span></span>
10. <span data-ttu-id="198b8-269">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-269">Select **OK**.</span></span>

    ![データ ソース プロパティのスライド アウト](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="198b8-271">新しいフィールドを追加して構成されたルックアップを使用する</span><span class="sxs-lookup"><span data-stu-id="198b8-271">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="198b8-272">**Model.Data** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="198b8-272">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="198b8-273">**Model.Data.Summary** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-273">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="198b8-274">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-274">Select **Add**.</span></span>
4.  <span data-ttu-id="198b8-275">**機能/計算済みフィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-275">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="198b8-276">**名前** フィールドに、**LevelByLookup** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-276">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="198b8-277">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-277">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="198b8-278">**数式フィールド** に、**Model.Selector(Model.Data.Summary.Code)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-278">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="198b8-279">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-279">Select **Save**.</span></span>

    ![フォーミュラ デザイナー ページに Model.Selector(Model.Data.Summary.Code) を追加する](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="198b8-281">**式の編集** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="198b8-281">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="198b8-282">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-282">Select **OK**.</span></span>

    ![新しいフォーミュラが追加されたで形式デザイナー ページ](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="198b8-284&quot;>追加した **LevelByLookup** 計算フィールドを使用すると、集計された各税トランザクション レコードの **課税レベルの一覧** 形式の列挙型の値として、課税レベルが返されることに注意してください。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-284&quot;>Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id=&quot;198b8-285&quot;>レコードの税コードは **Model.Selector** のルックアップ データ ソースに渡され、このデータ ソースのルールのセットを使用して正しい課税レベルが選択されます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-285&quot;>The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name=&quot;add-a-new-format-enumeration-based-data-source&quot;></a><span data-ttu-id=&quot;198b8-286&quot;>新しい形式列挙型ベースのデータ ソースを追加する</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-286&quot;>Add a new format enumeration-based data source</span></span>

<span data-ttu-id=&quot;198b8-287&quot;>次に、前の手順で追加した形式列挙型を参照する新しいデータ ソースを追加します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-287&quot;>Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id=&quot;198b8-288&quot;>このデータ ソースの値は、後で ER 形式の式で使用されます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-288&quot;>Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id=&quot;198b8-289&quot;>**ルートの追加** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-289&quot;>Select **Add root**.</span></span>
2.  <span data-ttu-id=&quot;198b8-290&quot;>**形式列挙型\列挙型** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-290&quot;>Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id=&quot;198b8-291&quot;>**名前** フィールドに、**TaxationLevel** と入力します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-291&quot;>In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id=&quot;198b8-292&quot;>**形式列挙型** フィールドで、**課税レベルの一覧** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-292&quot;>In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id=&quot;198b8-293&quot;>**保存** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-293&quot;>Select **Save**.</span></span>

### <a name=&quot;modify-an-existing-field-to-start-to-use-the-lookup&quot;></a><span data-ttu-id=&quot;198b8-294&quot;>ルックアップの使用を開始するために既存のフィールドを変更する</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-294&quot;>Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id=&quot;198b8-295&quot;>次に、既存の計算フィールドを変更して、構成されているルックアップ データ ソースを使用して、税コードに応じて正しい課税レベル値を取得するようにします。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-295&quot;>Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id=&quot;198b8-296&quot;>**Model.Data.Summary.Level** 項目を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-296&quot;>Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id=&quot;198b8-297&quot;>**編集** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-297&quot;>Select **Edit**.</span></span>
3.  <span data-ttu-id=&quot;198b8-298&quot;>**式の編集** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-298&quot;>Select **Edit formula**.</span></span>

    <span data-ttu-id=&quot;198b8-299&quot;>**Model.Data.Summary.Level** フィールドの現在の式には、次のハードコーディングされた税コードが含まれています。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;198b8-299&quot;>Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id=&quot;198b8-300&quot;>CASE (@.Code、&quot;VAT19&quot;、&quot;Regular&quot;、&quot;InVAT19&quot;、&quot;Regular&quot;、&quot;VAT7&quot;、&quot;Reduced&quot;、&quot;InVAT7&quot;、&quot;Reduced&quot;、&quot;THIRD&quot;、&quot;None&quot;、&quot;InVAT0&quot;、&quot;None&quot;、&quot;Other")</span><span class="sxs-lookup"><span data-stu-id="198b8-300">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="198b8-301">**式** フィールドに、**CASE(@.LevelByLookup、TaxationLevel.'Regular taxation'、"Regular"、TaxationLevel.'Reduced taxation'、"Reduced"、TaxationLevel.'No taxation'、None"、"Other")** と入力します。</span><span class="sxs-lookup"><span data-stu-id="198b8-301">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="198b8-303">**Model.Data.Summary.Level** フィールドの式は、現在のレコードの税コードと、ビジネス ユーザーが **Model.Data.Selector** ルックアップ データ ソースで構成したルールのセットに基づいて、課税レベルを返すようになりました。</span><span class="sxs-lookup"><span data-stu-id="198b8-303">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="198b8-304">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-304">Select **Save**.</span></span>
6.  <span data-ttu-id="198b8-305">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="198b8-305">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="198b8-306">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-306">Select **OK**.</span></span>
8.  <span data-ttu-id="198b8-307">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-307">Select **Save**.</span></span>
9.  <span data-ttu-id="198b8-308">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="198b8-308">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="198b8-309">派生形式のドラフト バージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="198b8-309">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="198b8-310">**バージョン** クイック タブで、**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-310">On the **Versions** FastTab, select **Change status**.</span></span>
2.  <span data-ttu-id="198b8-311">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-311">Select **Complete**.</span></span>
3.  <span data-ttu-id="198b8-312">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-312">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="198b8-313">修正された形式の完了したバージョンをエクスポートする</span><span class="sxs-lookup"><span data-stu-id="198b8-313">Export completed version of modified format</span></span>

1.  <span data-ttu-id="198b8-314">コンフィギュレーション ツリーで、**LE データの参照方法を知るための形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-314">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="198b8-315">**バージョン** クイック タブで、ステータスが **完了** のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-315">On the **Versions** FastTab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="198b8-316">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-316">Select **Exchange**.</span></span>
4.  <span data-ttu-id="198b8-317">**XML ファイルとしてエクスポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-317">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="198b8-318">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="198b8-318">Select **OK**.</span></span>
6.  <span data-ttu-id="198b8-319">Web ブラウザーで、**LE data.xml ファイルの参照方法を知るための形式** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="198b8-319">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="198b8-320">このファイルをローカルに保管します。</span><span class="sxs-lookup"><span data-stu-id="198b8-320">Store this file locally.</span></span>

<span data-ttu-id="198b8-321">**LE データ形式の参照方法を知るための形式** と、次のファイルをローカルに保管する方法については、このセクションの手順を親項目について繰り返します。</span><span class="sxs-lookup"><span data-stu-id="198b8-321">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="198b8-322">パラメーター化された calls.xml を知るための形式</span><span class="sxs-lookup"><span data-stu-id="198b8-322">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="198b8-323">パラメーター化された calls.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="198b8-323">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="198b8-324">パラメーター化された calls.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="198b8-324">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="198b8-325">構成済みの **LE データの参照方法を知るための形式** ER 形式を使用して、法人に依存する税コードのセットを設定し、さまざまな課税レベルで税トランザクションをフィルター処理する方法を学習するには、[法人ごとの ER 形式のパラメーターの設定](er-app-specific-parameters-set-up.md)トピックをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="198b8-325">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="198b8-326">追加リソース</span><span class="sxs-lookup"><span data-stu-id="198b8-326">Additional resources</span></span>

[<span data-ttu-id="198b8-327">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="198b8-327">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="198b8-328">法人ごとの ER 形式のパラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="198b8-328">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
