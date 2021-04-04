---
title: 法人ごとに指定されたパラメーターを使用するよう ER 形式を構成する
description: このトピックでは、法人ごと指定されたパラメーターを使用して電子申告 (ER) 形式を構成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
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
ms.openlocfilehash: 9253191f9cd10e0b3c87d61991598f9b791c35d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570737"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="6003a-103">法人ごとに指定されたパラメーターを使用するよう ER 形式を構成する</span><span class="sxs-lookup"><span data-stu-id="6003a-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="6003a-104">概要</span><span class="sxs-lookup"><span data-stu-id="6003a-104">Overview</span></span>

<span data-ttu-id="6003a-105">設計する電子申告 (ER) の多くの形式では、インスタンスの各法人に固有の値セット (税取引をフィルター処理するための税コードセットなど) を使用してデータをフィルター処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="6003a-106">現時点では、このタイプのフィルター処理が ER 形式で構成されている場合、ER 形式の式でデータフィルター処理ルールを指定するために、法人に依存する値 (税コードなど) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="6003a-107">したがって、ER 形式は法人固有のものであり、必要なレポートを生成するには、ER 形式を実行する必要がある各法人に対して元の ER 形式の派生コピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="6003a-108">元の (ベース) バージョンが更新され、テスト環境からエクスポートされて、本番用に配置する必要がある場合は、テスト環境からエクスポートされて、本番環境にインポートされると、各派生 ER 形式によって、法人固有の値を取り込めるように編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="6003a-109">したがって、このように構成されたこのタイプの ER ソリューションのメンテナンスは、次のような理由から、非常に複雑で時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="6003a-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="6003a-110">法人の数が多い場合は、より多くの ER 形式の構成を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="6003a-111">ER の構成を保守するには、ビジネスユーザーが ER の情報を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="6003a-112">ER アプリケーション固有のパラメーター機能を使用すると、パワーユーザーはデータフィルターを ER 形式に構成して、一連の抽象的なルールに基づくようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="6003a-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="6003a-113">このルールセットは、ER 形式で使用可能なデータソースを使用するように構成できます。</span><span class="sxs-lookup"><span data-stu-id="6003a-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="6003a-114">ビジネスユーザーは ER フレームワークを超えた実際のルールを、対応する ER 形式の設定に基づいて自動的に生成されるユーザーインターフェイス (UI) と、ER 形式のデータソースからアクセスされる現在の法人データを使用して指定できます。</span><span class="sxs-lookup"><span data-stu-id="6003a-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="6003a-115">ER 形式に対して指定されている一連のルールは、Dynamics 365 Finance (財務) インスタンスの現在の法人からエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="6003a-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="6003a-116">その後、同じ財務のインスタンスまたは異なるインスタンスの別の法人に、同じ ER 形式のルールセットとしてインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="6003a-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6003a-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="6003a-117">Prerequisites</span></span>

<span data-ttu-id="6003a-118">このトピックの例を完了するには、次のいずれかの役割で、財務と同じテナントに対してプロビジョニングされている Regulatory Configuration Services (RCS) のインスタンスにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="6003a-119">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="6003a-119">Electronic reporting developer</span></span>
- <span data-ttu-id="6003a-120">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="6003a-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="6003a-121">システム管理者</span><span class="sxs-lookup"><span data-stu-id="6003a-121">System administrator</span></span>

<span data-ttu-id="6003a-122">[CALCULATED FIELD タイプの ER データソースのパラメーター化された呼び出しをサポート](er-calculated-field-type.md) トピックの手順を実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6003a-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="6003a-123">これらの手順を既に完了している場合は、この後の **ER 構成を RCS にインポートする** セクションの手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="6003a-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="6003a-124">ER 構成を RCS にインポートする</span><span class="sxs-lookup"><span data-stu-id="6003a-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="6003a-125">[Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=851448) から、**CALCULATED FIELD タイプの ER データ ソースのパラメーター化された呼び出しをサポート** ZIP ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6003a-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="6003a-126">この ZIP ファイルには、ローカルに抽出および保存する必要がある次の ER 構成が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6003a-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="6003a-127">**コンテンツの説明**</span><span class="sxs-lookup"><span data-stu-id="6003a-127">**Content description**</span></span>                        | <span data-ttu-id="6003a-128">**ファイル名**</span><span class="sxs-lookup"><span data-stu-id="6003a-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6003a-129">**ER データ モデル** 構成ファイルのサンプル</span><span class="sxs-lookup"><span data-stu-id="6003a-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="6003a-130">パラメーター化された呼び出し version.1.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="6003a-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="6003a-131">**ER メタデータ** 構成ファイルのサンプル</span><span class="sxs-lookup"><span data-stu-id="6003a-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="6003a-132">パラメーター化された呼び出し version.1.xml を知るためのメタデータ</span><span class="sxs-lookup"><span data-stu-id="6003a-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="6003a-133">**ER モデル マッピング** 構成ファイルのサンプル</span><span class="sxs-lookup"><span data-stu-id="6003a-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="6003a-134">パラメーター化された呼び出し version.1.1.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="6003a-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="6003a-135">**ER 形式** 構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="6003a-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="6003a-136">パラメーター化された呼び出し version.1.1.xml を知るための形式</span><span class="sxs-lookup"><span data-stu-id="6003a-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="6003a-137">次に、RCS インスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="6003a-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="6003a-138">この例では、Litware、Inc. サンプル会社の構成を作成します。</span><span class="sxs-lookup"><span data-stu-id="6003a-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="6003a-139">この手順を完了する前に、RCS で [ER 構成 プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md)トピックにある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="6003a-140">既定のダッシュボードで、**電子申告** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="6003a-141">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="6003a-142">RCS にダウンロードした ER コンフィギュレーションを、次の順序で RCS にインポートします。データ モデル、メタデータ、モデル マッピング、フォーマット。</span><span class="sxs-lookup"><span data-stu-id="6003a-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="6003a-143">各 ER コンフィギュレーションについて、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6003a-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="6003a-144">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="6003a-145">**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="6003a-146">**参照** を選択して、必要な ER コンフィギュレーションファイルを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="6003a-147">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="6003a-148">指定された ER ソリューションを確認する</span><span class="sxs-lookup"><span data-stu-id="6003a-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="6003a-149">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し** の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="6003a-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="6003a-150">**パラメーター化された呼び出しを知るための形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="6003a-151">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6003a-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="6003a-152">**展開 / 折りたたみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="6003a-153">**パラメーター化された呼び出しを学習するための形式** の ER 形式は、(標準、減額、なし) という複数の課税レベルを提供する XML 形式の税明細書を生成するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="6003a-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="6003a-154">各レベルには異なる数の詳細情報があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-154">Each level has a different number of details.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="6003a-156">**マッピング** タブで、**モデル**、**データ**、および **概要** 品目を展開します。</span><span class="sxs-lookup"><span data-stu-id="6003a-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="6003a-157">**Model.Data.Summary** データ ソースは、税トランザクションの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="6003a-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="6003a-158">それらのトランザクションは税コードごとに集計されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="6003a-159">このデータ ソースについて **Model.Data.Summary.Level** の計算フィールドが、集計された各レコードの課税レベルのコードを返すように構成されています。</span><span class="sxs-lookup"><span data-stu-id="6003a-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="6003a-160">実行時に **Model.Data.Summary** データ ソースから取得できる税コードの場合、計算済みフィールドは、課税レベル コード (**標準**、**減額**、**なし**、または **その他**) テキスト値として返します。</span><span class="sxs-lookup"><span data-stu-id="6003a-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="6003a-161">**Model.Data.Summary.Level** 計算済みフィールドは、**Model.Data.Summary** データ ソースのレコードをフィルター処理し、**Model.Data2.Level1**、**Model.Data2.Level2**、**Model.Data2.Level3** を使用して課税レベルを表す各 XML 要素にフィルター処理されたデータを入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="6003a-163">**Model.Data.Summary.Level** の計算済みフィールドは、ER 式を含むように構成されています。</span><span class="sxs-lookup"><span data-stu-id="6003a-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="6003a-164">税コード (**VAT19**、**InVAT19**、**VAT7**、**InVAT7**、**THIRD**、**InVAT0**) は、この構成にハードコードされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6003a-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="6003a-165">したがって、この ER 形式は、税コードが構成された法人に依存しています。</span><span class="sxs-lookup"><span data-stu-id="6003a-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="6003a-167">法人ごとに異なる税コードのセットをサポートするには、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="6003a-168">法人ごとに ER 形式の派生バージョンを作成します。</span><span class="sxs-lookup"><span data-stu-id="6003a-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="6003a-169">法人設定に基づいて、**Model.Data.Summary.Level** 計算済みフィールドで税コードを更新します。</span><span class="sxs-lookup"><span data-stu-id="6003a-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="6003a-170">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6003a-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="6003a-171">派生形式を作成する</span><span class="sxs-lookup"><span data-stu-id="6003a-171">Create a derived format</span></span>

<span data-ttu-id="6003a-172">次に、ER アプリケーション固有のパラメーター機能を使用して、1 つの ER 形式に含まれる各法人の税コードの異なるセットをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6003a-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="6003a-173">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し** の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="6003a-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="6003a-174">**パラメーター化された呼び出しを知るための形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="6003a-175">**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="6003a-176">**名前から派生: パラメーター化された呼び出しを知るための形式、Microsoft** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="6003a-177">**名前** フィールドに、**LE データの参照方法を知るための形式** を入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="6003a-178">**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="6003a-179">派生形式のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6003a-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="6003a-180">形式列挙型の追加</span><span class="sxs-lookup"><span data-stu-id="6003a-180">Add a format enumeration</span></span>

<span data-ttu-id="6003a-181">次に、新しい ER 形式列挙型を追加します。</span><span class="sxs-lookup"><span data-stu-id="6003a-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="6003a-182">この形式の列挙型の値は、ビジネスユーザーに対して表示され、ER 形式で使用されるさまざまな課税レベルの法人固有の税コードのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="6003a-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="6003a-183">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6003a-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="6003a-184">**形式列挙型** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="6003a-185">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-185">Select **Add**.</span></span>
4.  <span data-ttu-id="6003a-186">**名前** フィールドに、**課税レベルの一覧** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="6003a-187">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-187">Select **Save**.</span></span>
6.  <span data-ttu-id="6003a-188">**形式列挙型の値** タブで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="6003a-189">**名前** フィールドに、**通常の課税** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="6003a-190">**追加** を再度選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="6003a-191">**名前** フィールドに、**減額課税** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="6003a-192">**追加** を再度選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-192">Select **Add** again.</span></span>
11. <span data-ttu-id="6003a-193">**名前** フィールドに、**非課税** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="6003a-194">**追加** を再度選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-194">Select **Add** again.</span></span>
13. <span data-ttu-id="6003a-195">**名前** フィールドに、**その他** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-195">In the **Name** field, enter **Other**.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="6003a-197">ビジネスユーザーは、異なる言語を使用して、法人に依存する税コードのセットを指定する場合があるため、この列挙型の値を、財務のユーザーの優先言語として構成された言語に翻訳することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6003a-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="6003a-198">**非課税** レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="6003a-199">**ラベル** フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6003a-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="6003a-200">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-200">Select **Translate**.</span></span>
17. <span data-ttu-id="6003a-201">**テキストの翻訳** ウィンドウの **ラベル Id** フィールドに、**LBL_LEVELENUM_NO** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="6003a-202">**既定の言語のテキスト** フィールドに **非課税** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="6003a-203">**言語** フィールドで、**DE** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="6003a-204">**翻訳テキスト** フィールドで、**keine Besteuerung** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="6003a-205">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-205">Select **Translate**.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="6003a-207">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-207">Select **Save**.</span></span>
23. <span data-ttu-id="6003a-208">**形式列挙型** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6003a-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="6003a-209">新しいルックアップ データ ソースを追加する</span><span class="sxs-lookup"><span data-stu-id="6003a-209">Add a new lookup data source</span></span>

<span data-ttu-id="6003a-210">次に、新しいデータソースを追加して、ビジネスユーザーが、集計された各トランザクション レコードに対して正しい課税レベルを認識するための法人依存ルールをどのように指定するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6003a-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="6003a-211">**マッピング** タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="6003a-212">**形式列挙型\ルックアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="6003a-213">ビジネス ユーザーが課税レベルの認識に指定した各ルールが ER 形式列挙型の値を返すことを確認しました。</span><span class="sxs-lookup"><span data-stu-id="6003a-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="6003a-214">**ルックアップ** データ ソース タイプには、**形式列挙型** ブロックに加えて、**データ モデル** および **Dynamics 365 for Operations** ブロックでもアクセスできる点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="6003a-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="6003a-215">したがって、ER データ モデルの列挙型とアプリケーションの列挙型を使用して、その型のデータ ソースに対して返される値の型を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="6003a-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="6003a-216">**名前** フィールドに、**セレクター** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="6003a-217">**形式列挙型** フィールドで、**課税レベルの一覧** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="6003a-218">このデータ ソースで指定されているルールごとに、ビジネス ユーザーは、**課税レベルの一覧** 形式列挙型の値のいずれかを戻り値として選択する必要があることを指定しました。</span><span class="sxs-lookup"><span data-stu-id="6003a-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="6003a-219">**ルックアップの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="6003a-220">**列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="6003a-221">**モデル** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="6003a-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="6003a-222">**データ** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="6003a-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="6003a-223">**税** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="6003a-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="6003a-224">**Model.Data.Tax.Code** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="6003a-225">**追加** ボタン (右矢印) を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-225">Select the **Add** button (the right arrow).</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="6003a-227">課税レベルの認識のためにこのデータ ソースで指定されている各ルールについて、ビジネス ユーザーが条件として税コードの 1 つを選択する必要があることを指定しました。</span><span class="sxs-lookup"><span data-stu-id="6003a-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="6003a-228">ビジネス ユーザーが選択できる税コードの一覧は、**Model.Data.Tax** データ ソースよって返されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="6003a-229">このデータ ソースには **名前** フィールドが含まれているため、ビジネス ユーザーに対して表示されるルックアップの各税コード値について、税コードの名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="6003a-230">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-230">Select **OK**.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="6003a-232">ビジネス ユーザーは、このデータ ソースのレコードとして、複数のルールを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="6003a-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="6003a-233">各レコードには、明細行コードで番号が付けられます。</span><span class="sxs-lookup"><span data-stu-id="6003a-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="6003a-234">ルールは行番号の昇順で評価されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="6003a-235">**税コード** フィールドはこのルックアップ データ ソースのルールの条件として選択されており、**税コード** は **文字列** データ型のフィールドとして設定されているため、各ルールは、データ ソースに渡される税コードと、データ ソースのレコードで定義されている税コードとを比較することによって、実行時に評価されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="6003a-236">構成された条件を満たすルールが見つかった場合、このデータ ソースは、**ルックアップの結果** フィールドに定義されているルールのルックアップ値を返します。</span><span class="sxs-lookup"><span data-stu-id="6003a-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="6003a-237">ルールが見つからない場合は、現在のデータ ソースが正しい値を返すことができないことをユーザーに通知する例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="6003a-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="6003a-238">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-238">Select **Save**.</span></span>
14. <span data-ttu-id="6003a-239">**ルックアップ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6003a-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="6003a-240">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-240">Select **OK**.</span></span>

    <span data-ttu-id="6003a-241">**文字列** データ型の **コード** パラメーターの引数としてデータ ソースに渡されたすべての税コードの **課税レベル リスト** の形式列挙型の値として、課税レベルを返す新しいデータ ソースを追加したことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6003a-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="6003a-243">構成されたルールの評価は、そのルールの条件を定義するために選択されたフィールドのデータ型に依存することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6003a-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="6003a-244">**数値** データ型または **日付** データ型のフィールドとして構成されているフィールドを選択した場合、基準は **文字列** データ型に対して既に説明した基準とは異なります。</span><span class="sxs-lookup"><span data-stu-id="6003a-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="6003a-245">**数値** フィールドおよび **日付** フィールドでは、ルールを値の範囲として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="6003a-246">データ ソースに渡される値が構成された範囲内にある場合は、ルールの条件が満たされたと見なされます。</span><span class="sxs-lookup"><span data-stu-id="6003a-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="6003a-247">次の図は、この種類の設定の例を示します。</span><span class="sxs-lookup"><span data-stu-id="6003a-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="6003a-248">**文字列** データ型の **Model.Data.Tax.Code** フィールドに加えて、**リアル** データ型の **Model.Tax.Summary.Base** フィールドを使用して、ルックアップ データ ソースの条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="6003a-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="6003a-250">このルックアップ データ ソースに対して **Model.Data.Tax.Code** フィールドおよび **Model.Tax.Summary.Base** が選択されます。このデータ ソースの各ルールは、次のように構成されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="6003a-251">表示される一覧で、**課税レベルの一覧** 形式列挙型の値を戻り値として選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="6003a-252">この税コードは、このルールの条件として入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="6003a-253">**Model.Data.Tax** データ ソースによって提供される税コードのみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="6003a-254">税基準額の最小値と最大値は、このルールの条件として入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6003a-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="6003a-255">次は、このデータ ソースの各ルールを実行時に評価する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6003a-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="6003a-256">このデータ ソースに渡された **文字列** データ型のコードがルールの税コードと同等か?</span><span class="sxs-lookup"><span data-stu-id="6003a-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="6003a-257">このデータ ソースに渡された **リアル** データ型の値が、特定の最小値と最大値の範囲内に収まっているか?</span><span class="sxs-lookup"><span data-stu-id="6003a-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="6003a-258">両方の条件が満たされると、ルールが適用可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="6003a-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="6003a-259">追加されたルックアップ データ ソースのラベルを翻訳する</span><span class="sxs-lookup"><span data-stu-id="6003a-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="6003a-260">ビジネス ユーザーは、異なる言語を使用して、法人に依存する税コードのセットを指定する場合があるため、追加するルックアップ データ ソースのラベルを翻訳し、対応するページで各ユーザーの優先言語で表示することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6003a-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="6003a-261">**Model.Data.Selector** データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="6003a-262">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="6003a-263">**ラベル** フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6003a-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="6003a-264">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="6003a-265">**テキストの翻訳** ウィンドウの **ラベル Id** フィールドに、**LBL_SELECTOR_DS** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="6003a-266">**既定の言語のテキスト** フィールドに、**税コードによる税レベルの選択** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="6003a-267">**言語** フィールドで、**DE** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="6003a-268">**翻訳テキスト** フィールドに,**Steuerebene für Steuerkennzeichen auswählen** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="6003a-269">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-269">Select **Translate**.</span></span>
10. <span data-ttu-id="6003a-270">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-270">Select **OK**.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="6003a-272">新しいフィールドを追加して構成されたルックアップを使用する</span><span class="sxs-lookup"><span data-stu-id="6003a-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="6003a-273">**Model.Data** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="6003a-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="6003a-274">**Model.Data.Summary** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="6003a-275">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-275">Select **Add**.</span></span>
4.  <span data-ttu-id="6003a-276">**機能/計算済みフィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="6003a-277">**名前** フィールドに、**LevelByLookup** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="6003a-278">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="6003a-279">**数式フィールド** に、**Model.Selector(Model.Data.Summary.Code)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="6003a-280">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-280">Select **Save**.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="6003a-282">**式の編集** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6003a-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="6003a-283">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-283">Select **OK**.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="6003a-285">追加した **LevelByLookup** 計算フィールドを使用すると、集計された各税トランザクション レコードの **課税レベルの一覧** 形式の列挙型の値として、課税レベルが返されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6003a-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="6003a-286">レコードの税コードは **Model.Selector** のルックアップ データ ソースに渡され、このデータ ソースのルールのセットを使用して正しい課税レベルが選択されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="6003a-287">新しい形式列挙型ベースのデータ ソースを追加する</span><span class="sxs-lookup"><span data-stu-id="6003a-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="6003a-288">次に、前の手順で追加した形式列挙型を参照する新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="6003a-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="6003a-289">このデータ ソースの値は、後で ER 形式の式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="6003a-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="6003a-290">**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="6003a-291">**形式列挙型\列挙型** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="6003a-292">**名前** フィールドに、**TaxationLevel** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="6003a-293">**形式列挙型** フィールドで、**課税レベルの一覧** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="6003a-294">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="6003a-295">ルックアップの使用を開始するために既存のフィールドを変更する</span><span class="sxs-lookup"><span data-stu-id="6003a-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="6003a-296">次に、既存の計算フィールドを変更して、構成されているルックアップ データ ソースを使用して、税コードに応じて正しい課税レベル値を取得するようにします。</span><span class="sxs-lookup"><span data-stu-id="6003a-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="6003a-297">**Model.Data.Summary.Level** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="6003a-298">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="6003a-299">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="6003a-300">**Model.Data.Summary.Level** フィールドの現在の式には、次のハードコーディングされた税コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6003a-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="6003a-301">CASE (@.Code、"VAT19"、"Regular"、"InVAT19"、"Regular"、"VAT7"、"Reduced"、"InVAT7"、"Reduced"、"THIRD"、"None"、"InVAT0"、"None"、"Other")</span><span class="sxs-lookup"><span data-stu-id="6003a-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="6003a-302">**式** フィールドに、**CASE(@.LevelByLookup、TaxationLevel.'Regular taxation'、"Regular"、TaxationLevel.'Reduced taxation'、"Reduced"、TaxationLevel.'No taxation'、None"、"Other")** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6003a-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![ER 操作デザイナーのページ](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="6003a-304">**Model.Data.Summary.Level** フィールドの式は、現在のレコードの税コードと、ビジネス ユーザーが **Model.Data.Selector** ルックアップ データ ソースで構成したルールのセットに基づいて、課税レベルを返すようになりました。</span><span class="sxs-lookup"><span data-stu-id="6003a-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="6003a-305">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-305">Select **Save**.</span></span>
6.  <span data-ttu-id="6003a-306">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6003a-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="6003a-307">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-307">Select **OK**.</span></span>
8.  <span data-ttu-id="6003a-308">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-308">Select **Save**.</span></span>
9.  <span data-ttu-id="6003a-309">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6003a-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="6003a-310">派生形式のドラフト バージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="6003a-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="6003a-311">**バージョン** クイック タブで、**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="6003a-312">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="6003a-313">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="6003a-314">修正された形式の完了したバージョンをエクスポートする</span><span class="sxs-lookup"><span data-stu-id="6003a-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="6003a-315">コンフィギュレーション ツリーで、**LE データの参照方法を知るための形式** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="6003a-316">**バージョン** クイック タブで、ステータスが **完了** のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="6003a-317">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="6003a-318">**XML ファイルとしてエクスポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="6003a-319">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6003a-319">Select **OK**.</span></span>
6.  <span data-ttu-id="6003a-320">Web ブラウザーで、**LE data.xml ファイルの参照方法を知るための形式** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6003a-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="6003a-321">このファイルをローカルに保管します。</span><span class="sxs-lookup"><span data-stu-id="6003a-321">Store this file locally.</span></span>

<span data-ttu-id="6003a-322">**LE データ形式の参照方法を知るための形式** と、次のファイルをローカルに保管する方法については、このセクションの手順を親項目について繰り返します。</span><span class="sxs-lookup"><span data-stu-id="6003a-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="6003a-323">パラメーター化された calls.xml を知るための形式</span><span class="sxs-lookup"><span data-stu-id="6003a-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="6003a-324">パラメーター化された calls.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="6003a-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="6003a-325">パラメーター化された calls.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="6003a-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="6003a-326">構成済みの **LE データの参照方法を知るための形式** ER 形式を使用して、法人に依存する税コードのセットを設定し、さまざまな課税レベルで税トランザクションをフィルター処理する方法を学習するには、[法人ごとの ER 形式のパラメーターの設定](er-app-specific-parameters-set-up.md)トピックをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="6003a-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6003a-327">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6003a-327">Additional resources</span></span>

[<span data-ttu-id="6003a-328">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="6003a-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="6003a-329">法人ごとの ER 形式のパラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="6003a-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]