---
title: 計算済みフィールド タイプの ER データ ソースの、パラメーター化された呼び出しをサポートする
description: このトピックでは、ER データ ソースに対して計算済みフィールド タイプを使用する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550087"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="37ace-103">計算済みフィールド タイプの ER データ ソースの、パラメーター化された呼び出しをサポートする</span><span class="sxs-lookup"><span data-stu-id="37ace-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37ace-104">このトピックでは、**計算済みフィールド** タイプを使用して電子レポート (ER) データ ソースをデザインする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="37ace-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="37ace-105">このデータソースには ER 式が含まれている可能性があり、この式を実行すると、このデータ ソースを呼び出すバインドで構成されているパラメータ引数の値によって制御することができます。</span><span class="sxs-lookup"><span data-stu-id="37ace-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="37ace-106">このようなデータ ソースのパラメーター化された呼び出しを構成することにより、1 つのデータ ソースを多数のバインドで再利用できます。これにより、ER モデル マッピングまたは ER フォーマットで構成する必要があるデータ ソースの総数を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="37ace-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="37ace-107">また、構成済みの ER コンポーネントが簡素化され、これにより保守コストおよび他の消費者が使用するコストが削減されます。</span><span class="sxs-lookup"><span data-stu-id="37ace-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37ace-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="37ace-108">Prerequisites</span></span>
<span data-ttu-id="37ace-109">このトピックの例を完了するには、次のアクセスが必要です:</span><span class="sxs-lookup"><span data-stu-id="37ace-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="37ace-110">これらのロールにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="37ace-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="37ace-111">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="37ace-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="37ace-112">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="37ace-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="37ace-113">システム管理者</span><span class="sxs-lookup"><span data-stu-id="37ace-113">System administrator</span></span>

- <span data-ttu-id="37ace-114">次のいずれかのロールで、Finance and Operations と同じテナントに対してプロビジョニングされている Regulatory Configuration Services (RCS) にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="37ace-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="37ace-115">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="37ace-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="37ace-116">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="37ace-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="37ace-117">システム管理者</span><span class="sxs-lookup"><span data-stu-id="37ace-117">System administrator</span></span>

<span data-ttu-id="37ace-118">[Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) から、ZIP (圧縮された) ファイル**をダウンロードし、計算済みフィールド タイプ**の ER データ ソースの、パラメーター化された呼び出しをサポートします。</span><span class="sxs-lookup"><span data-stu-id="37ace-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="37ace-119">これには、ローカルに抽出および保存する必要がある次の ER コンフィギュレーションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="37ace-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="37ace-120">**コンテンツ**</span><span class="sxs-lookup"><span data-stu-id="37ace-120">**Content**</span></span>                           | <span data-ttu-id="37ace-121">**ファイル名**</span><span class="sxs-lookup"><span data-stu-id="37ace-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37ace-122">ER データ モデル構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="37ace-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="37ace-123">パラメーター化された呼び出し version.1.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="37ace-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="37ace-124">ER メタデータ構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="37ace-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="37ace-125">パラメーター化された呼び出し version.1.xml を知るためのメタデータ</span><span class="sxs-lookup"><span data-stu-id="37ace-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="37ace-126">ER モデル マッピング構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="37ace-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="37ace-127">パラメーター化された呼び出し version.1.1.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="37ace-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="37ace-128">ER フォーマット構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="37ace-128">Sample ER format configuration</span></span>        | <span data-ttu-id="37ace-129">パラメーター化された呼び出し version.1.1.xml を知るための形式</span><span class="sxs-lookup"><span data-stu-id="37ace-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="37ace-130">RCS インスタンスにサインインする</span><span class="sxs-lookup"><span data-stu-id="37ace-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="37ace-131">この例では、サンプル会社 Litware, Inc. 用に、コンフィギュレーションを作成します。まず、RCS で、手順 [コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md) にあるステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37ace-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="37ace-132">既定のダッシュボードで、**電子申告**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="37ace-133">**コンフィギュレーションをレポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="37ace-134">ダウンロードしたコンフィギュレーションを、次の順序で RCS にインポートします。データ モデル、メタデータ、モデル マッピング、フォーマット。</span><span class="sxs-lookup"><span data-stu-id="37ace-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="37ace-135">各 ER コンフィギュレーションごとに次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="37ace-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="37ace-136">**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="37ace-137">**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="37ace-138">**参照**を選択してから、必要な ER コンフィギュレーションを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="37ace-139">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="37ace-140">指定された ER ソリューションを確認する</span><span class="sxs-lookup"><span data-stu-id="37ace-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="37ace-141">モデル マッピングを確認する</span><span class="sxs-lookup"><span data-stu-id="37ace-141">Review model mapping</span></span>

1. <span data-ttu-id="37ace-142">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し**の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="37ace-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="37ace-143">**パラメーター化された呼び出しを知るためのマッピング**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="37ace-144">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ace-144">Select **Designer**.</span></span>
4. <span data-ttu-id="37ace-145">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ace-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="37ace-146">この ER モデルマッピングは、次のように設計されています。</span><span class="sxs-lookup"><span data-stu-id="37ace-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="37ace-147">**TaxTable** テーブルに存在する税コード (**税**データ ソース) のリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="37ace-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="37ace-148">**TaxTrans** テーブルに存在する税トランザクション (**トランザクション** データ ソース) のリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="37ace-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="37ace-149">取得したトランザクション (**Gr** データ ソース) のリストを、税コード別にグループ化します。</span><span class="sxs-lookup"><span data-stu-id="37ace-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="37ace-150">税コードごとに集計された値に従って、グループ化されたトランザクションを計算します。</span><span class="sxs-lookup"><span data-stu-id="37ace-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="37ace-151">税基準値の合計。</span><span class="sxs-lookup"><span data-stu-id="37ace-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="37ace-152">税額の合計。</span><span class="sxs-lookup"><span data-stu-id="37ace-152">Sum of tax values.</span></span>
        - <span data-ttu-id="37ace-153">適用される税率の最小値。</span><span class="sxs-lookup"><span data-stu-id="37ace-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="37ace-154">このコンフィギュレーションのモデル マッピングは、このモデルに対して作成され Finance and Operations で実行される、すべての ER フォーマットの基本データ モデルを実装します。</span><span class="sxs-lookup"><span data-stu-id="37ace-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="37ace-155">その結果、**税**および **Gr** データ ソースの内容は、抽象データ ソースなどの ER フォーマットに対して公開されます。</span><span class="sxs-lookup"><span data-stu-id="37ace-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![税および Gr データ ソースを表示するモデル マッピング デザイナー ページ](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="37ace-157">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="37ace-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="37ace-158">**モデル マッピング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="37ace-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="37ace-159">形式の確認</span><span class="sxs-lookup"><span data-stu-id="37ace-159">Review format</span></span>

1. <span data-ttu-id="37ace-160">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し**の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="37ace-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="37ace-161">**パラメーター化された呼び出しを知るための形式**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="37ace-162">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ace-162">Select **Designer**.</span></span> <span data-ttu-id="37ace-163">この ER フォーマットは次のように設計されています。</span><span class="sxs-lookup"><span data-stu-id="37ace-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="37ace-164">税明細書を XML 形式で生成します。</span><span class="sxs-lookup"><span data-stu-id="37ace-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="37ace-165">税明細書に以下の課税レベルを提示します。標準、減額、なし。</span><span class="sxs-lookup"><span data-stu-id="37ace-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="37ace-166">各レベルで詳細条件を持つ、各課税レベルにおける複数の詳細を提示します。</span><span class="sxs-lookup"><span data-stu-id="37ace-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![形式デザイナーのページ](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="37ace-168">**マッピング**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="37ace-169">**モデル**、**データ、** および**集計**項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="37ace-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="37ace-170">計算済みフィールド **モデル.データ.集計.レベル**は、その**モデル.データ.集計**データ ソースから実行時に取得できるすべての税コードのテキスト値として、(**標準**、**減額**、**なし、** または**その他**) の課税レベル コードを返す式が含まれます。</span><span class="sxs-lookup"><span data-stu-id="37ace-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![パラメーター化された呼び出しを知るためのモデルの、データ モデル詳細を表示するフォーマット デザイナー ページ](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="37ace-172">**モデル**.**データ 2** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="37ace-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="37ace-173">**モデル**.**データ 2. 集計 2** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="37ace-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="37ace-174">この**モデル**.**データ2.集計2** データ ソースは、課税レベル (**モデル.データ.集計.レベル** 計算済みフィールドによって返されます) によって**モデル.データ.集計** データ ソース トランザクション の詳細をグループ化し、集計を計算するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="37ace-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![モデル.データ 2.集計 2 データ ソースの詳細を表示する形式デザイナー ページ](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="37ace-176">計算済みフィールドの**モデル**.**データ 2.レベル 1** 、**モデル**.**データ 2.レベル 2** 、および**モデル**.**データ 2.レベル 3** を確認します。</span><span class="sxs-lookup"><span data-stu-id="37ace-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="37ace-177">これらの計算済みフィールドは、**モデル**.**データ 2.集計 2**レコード リストをフィルターするために使用され、特定の課税レベルを表すレコードだけを返します。</span><span class="sxs-lookup"><span data-stu-id="37ace-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="37ace-178">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="37ace-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="37ace-179">派生形式を作成する</span><span class="sxs-lookup"><span data-stu-id="37ace-179">Create a derived format</span></span>
<span data-ttu-id="37ace-180">既存の 3 つのフィールドを使用するのではなく、必要な課税レベルをフィルターする 1 つの計算済みフィールドを追加することにより、指定された形式を改善することができます。**モデル**.**データ 2.レベル 1** 、**モデル**.**データ 2.レベル 2 、** および**モデル**.**データ 2.レベル 3** 。</span><span class="sxs-lookup"><span data-stu-id="37ace-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="37ace-181">必要な課税レベルは、この新しい計算済みフィールドが呼び出される場所に指定できます。</span><span class="sxs-lookup"><span data-stu-id="37ace-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="37ace-182">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し**の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="37ace-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="37ace-183">**パラメーター化された呼び出しを知るための形式**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="37ace-184">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="37ace-185">**名前から派生: パラメーター化された呼び出しを知るための形式、Microsoft** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="37ace-186">**名前**フィールドに、**パラメーター化された呼び出しを知るための形式 (カスタム)** を入力します。</span><span class="sxs-lookup"><span data-stu-id="37ace-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="37ace-187">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="37ace-188">レコード一覧を返すパラメーター化された計算済みフィールドを、コンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="37ace-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="37ace-189">新しい計算済みフィールドの追加を開始する</span><span class="sxs-lookup"><span data-stu-id="37ace-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="37ace-190">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37ace-190">Select **Designer**.</span></span>
2. <span data-ttu-id="37ace-191">**展開/折りたたみ**を選択し、すべての形式項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="37ace-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="37ace-192">**マッピング**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="37ace-193">**モデル**項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="37ace-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="37ace-194">**モデル.データ 2** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="37ace-195">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-195">Select **Add**.</span></span>
7. <span data-ttu-id="37ace-196">**機能\\計算済みフィールド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="37ace-197">**名前**フィールドに、**レベル**と入力します。</span><span class="sxs-lookup"><span data-stu-id="37ace-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="37ace-198">**式の編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="37ace-199">計算済みフィールドを追加するためにパラメーターを定義する</span><span class="sxs-lookup"><span data-stu-id="37ace-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="37ace-200">**パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="37ace-201">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-201">Select **New**.</span></span>
3. <span data-ttu-id="37ace-202">**名前**フィールドに、**課税レベル**と入力します。</span><span class="sxs-lookup"><span data-stu-id="37ace-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="37ace-203">**タイプ**フィールドで、**文字列**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="37ace-204">パラメーター引数のタイプを指定するために使用できるのは、プリミティブ データ型だけです。</span><span class="sxs-lookup"><span data-stu-id="37ace-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="37ace-205">そのため、**レコード リスト**、**レコード**、および**列挙**タイプはこの目的では使用できません。</span><span class="sxs-lookup"><span data-stu-id="37ace-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="37ace-206">1 つの計算済みフィールドに対して指定できるパラメーターの最大数は、8 です。</span><span class="sxs-lookup"><span data-stu-id="37ace-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![パラメーター データ ソース リスト](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="37ace-208">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-208">Select **OK**.</span></span>

<span data-ttu-id="37ace-209">このパラメーターを追加することにより、この計算済みフィールドを呼び出すために満たすべき条件が指定されます。</span><span class="sxs-lookup"><span data-stu-id="37ace-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="37ace-210">この計算済みフィールドを呼び出す際、**課税レベル** パラメーターの引数を、**文字列**形式の値として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37ace-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="37ace-211">コンテナーに存在する計算済みフィールド (**レコード リスト**、**レコード**、または**コンテナー**) に対してのみ、パラメーターを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37ace-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="37ace-212">コンフィギュレーションされたパラメーターは、この計算済みフィールドのためのデータ ソースのリスト内で使用できます。</span><span class="sxs-lookup"><span data-stu-id="37ace-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="37ace-213">**データソースの追加**を選択すると、コンフィギュレーションされた式にパラメーターを追加できます。</span><span class="sxs-lookup"><span data-stu-id="37ace-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![データ ソース フィールド](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="37ace-215">計算済みフィールドを追加するために式を定義する</span><span class="sxs-lookup"><span data-stu-id="37ace-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="37ace-216">**フォーミュラ** フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="37ace-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="37ace-217">**WHERE(\@.集計 2、 \@.集計 2.グループ化.レベル =**</span><span class="sxs-lookup"><span data-stu-id="37ace-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="37ace-218">データ ソースのリストで、**課税レベル** パラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="37ace-219">**データソースの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="37ace-220">**フォーミュラ** フィールドで、次の式を確定します。</span><span class="sxs-lookup"><span data-stu-id="37ace-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="37ace-221">**WHERE(\@.集計 2, \@.集計 2.グループ化.レベル = '課税レベル')**</span><span class="sxs-lookup"><span data-stu-id="37ace-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="37ace-222">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-222">Select **Save**.</span></span>

    ![データ ソース フィールドの情報](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="37ace-224">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="37ace-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="37ace-225">新しい計算済みフィールドの追加を完了する</span><span class="sxs-lookup"><span data-stu-id="37ace-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="37ace-226">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-226">Select **OK**.</span></span>

<span data-ttu-id="37ace-227">**フォーマット デザイナー** ページ上で、コンフィギュレーションされパラメーター化された計算済みフィールド **レベル**には、**文字列**引数が必要です。</span><span class="sxs-lookup"><span data-stu-id="37ace-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![計算済みフィールド レベルの展開されたリスト](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="37ace-229">バインディング フォーマット要素のため、コンフィギュレーションされた計算済みフィールドを使用する</span><span class="sxs-lookup"><span data-stu-id="37ace-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="37ace-230">**モデル.データ 2.レベル**を選択し、コンフィギュレーションされた計算済みフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="37ace-231">**明細書.課税.標準**形式要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="37ace-232">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-232">Select **Bind**.</span></span>
4. <span data-ttu-id="37ace-233">**はい**を選択し、選択された形式要素のすべての入れ子になった形式内で、新しいデータ ソース **レベル**によって、現在使用されているデータ ソース **レベル 1** が置き換えられることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37ace-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="37ace-234">適用したバインディングは、パラメーター化された計算済みフィールドの呼び出しとして作成されました。</span><span class="sxs-lookup"><span data-stu-id="37ace-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="37ace-235">既定では、バインド形式要素の名前は、次の条件下で、パラメーター化された計算済みフィールドに対する引数として使用されます。</span><span class="sxs-lookup"><span data-stu-id="37ace-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="37ace-236">計算済みフィールドは 1 つのパラメータを使用するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="37ace-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="37ace-237">このパラメータのデータ タイプは、**文字列**として定義されています。</span><span class="sxs-lookup"><span data-stu-id="37ace-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="37ace-238">バインド形式要素の名前が空白の場合、この要素のデータ ソース名は、適用したバインディングで使用されます。</span><span class="sxs-lookup"><span data-stu-id="37ace-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="37ace-239">**明細書.課税.減額**形式要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="37ace-240">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-240">Select **Bind**.</span></span>
7. <span data-ttu-id="37ace-241">**はい**を選択し、選択された形式要素の下にあるすべての入れ子になった形式内で、新しいデータ ソース **レベル**によって、現在使用されているデータ ソース **レベル 2** が置き換えられることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37ace-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="37ace-242">**明細書.課税.なし**形式要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="37ace-243">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-243">Select **Bind**.</span></span>
10. <span data-ttu-id="37ace-244">**はい**を選択し、選択された形式要素の下にあるすべての入れ子になった形式内で、新しいデータ ソース **レベル**によって、現在使用されているデータ ソース **レベル 3** が置き換えられることを確認します。</span><span class="sxs-lookup"><span data-stu-id="37ace-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="37ace-245">課税レベル (たとえば**モデル.データ 2.レベル ("減額")** テキスト値として) を表す XML 要素に対するパラメーター化された計算済みフィールドの引数を指定する場合、入れ子にされた XML 属性に対して同じ操作をする必要はありません。それらのバインドは、親レベル (**モデル.データ 2.レベル.集計された.ベース**、**モデル.データ 2.レベル ("減額")** 集計された.ベースではない) で定義されている引数の値を自動的に継承します。</span><span class="sxs-lookup"><span data-stu-id="37ace-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="37ace-246">どのパラメーター化された計算済みフィールドの繰り返し呼び出しも、サポートされません。</span><span class="sxs-lookup"><span data-stu-id="37ace-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="37ace-247">**式の編集**を選択して、選択したバインドの中でパラメーター化された計算済みフィールドの既定で適用される引数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="37ace-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="37ace-248">この引数が見つからない場合、実行時にエラーが発生する可能性があります。そのような状況は、現在の形式が検証されたときに、ユーザーに通知されます。</span><span class="sxs-lookup"><span data-stu-id="37ace-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![検証時の警告の通知](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="37ace-250">パラメーター化された計算済みフィールドをコンフィギュレーションし、レコードを返す</span><span class="sxs-lookup"><span data-stu-id="37ace-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="37ace-251">パラメーター化された計算済みフィールドがレコードを返す場合、このレコードの個々のフィールド バインドを形式要素にサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="37ace-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="37ace-252">そのような場合、パラメーター化された計算済みフィールドを呼び出す、引数の値を含む親バインドがありません。この値は、1 つのレコード フィールドのバインドで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37ace-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="37ace-253">新しい計算済みフィールドの追加を開始する</span><span class="sxs-lookup"><span data-stu-id="37ace-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="37ace-254">**モデル.データ 2** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="37ace-255">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-255">Select **Add**.</span></span>
3. <span data-ttu-id="37ace-256">**機能\\計算済みフィールド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="37ace-257">**名前**フィールドに、**レベル レコード**と入力します。</span><span class="sxs-lookup"><span data-stu-id="37ace-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="37ace-258">**式の編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="37ace-259">計算済みフィールドを追加するためにパラメーターを定義する</span><span class="sxs-lookup"><span data-stu-id="37ace-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="37ace-260">**パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="37ace-261">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-261">Select **New**.</span></span>
3. <span data-ttu-id="37ace-262">**名前**フィールドに、**課税レベル**と入力します。</span><span class="sxs-lookup"><span data-stu-id="37ace-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="37ace-263">**タイプ**フィールドで、**文字列**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="37ace-264">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="37ace-265">計算済みフィールドを追加するために式を定義する</span><span class="sxs-lookup"><span data-stu-id="37ace-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="37ace-266">**フォーミュラ** フィールドで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="37ace-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="37ace-267">**FIRSTORNULL(\@.レベル(**</span><span class="sxs-lookup"><span data-stu-id="37ace-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="37ace-268">**課税レベル** パラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="37ace-269">**データソースの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="37ace-270">**フォーミュラ** フィールドで、手順 1 で入力したものに **' 課税レベル '))** を上書きし、式をこのように確定します。</span><span class="sxs-lookup"><span data-stu-id="37ace-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="37ace-271">**FIRSTORNULL(\@.レベル ('課税レベル'))**</span><span class="sxs-lookup"><span data-stu-id="37ace-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="37ace-272">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-272">Select **Save**.</span></span>
6. <span data-ttu-id="37ace-273">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="37ace-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="37ace-274">新しい計算済みフィールドの追加を完了する</span><span class="sxs-lookup"><span data-stu-id="37ace-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="37ace-275">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="37ace-276">形式要素をバインドするため、コンフィギュレーションされた計算済みフィールドを使用する</span><span class="sxs-lookup"><span data-stu-id="37ace-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="37ace-277">**モデル.データ 2.レベル レコード**を展開し、コンフィギュレーションされた計算済みフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="37ace-278">コンフィギュレーションされた計算済みフィールドの、**モデル.データ 2.レベル レコード.集計**コンテナーを展開します。</span><span class="sxs-lookup"><span data-stu-id="37ace-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="37ace-279">**モデル.データ 2.レベル レコード.集計された.ベース** フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="37ace-280">**明細書.課税.なし**形式要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="37ace-281">**バインドの解除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="37ace-282">**明細書.課税.なし.ベース** 形式要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="37ace-283">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-283">Select **Bind**.</span></span>
8. <span data-ttu-id="37ace-284">**式の編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="37ace-285">式を、**モデル.データ 2.レベル レコード (" なし ") 集計された.ベース**に変更します。</span><span class="sxs-lookup"><span data-stu-id="37ace-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![更新された式](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="37ace-287">使用されていない計算済みフィールドを削除する</span><span class="sxs-lookup"><span data-stu-id="37ace-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="37ace-288">**モデル.データ 2.レベル 1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="37ace-289">**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-289">Select **Delete**.</span></span>
3. <span data-ttu-id="37ace-290">**モデル.データ 2.レベル 2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="37ace-291">**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-291">Select **Delete**.</span></span>
5. <span data-ttu-id="37ace-292">**モデル.データ 2.レベル 3** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="37ace-293">**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-293">Select **Delete**.</span></span>
7. <span data-ttu-id="37ace-294">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="37ace-295">形式バインドの中で、同じ計算済フィールド **モデル.データ 2.レベル**が複数回再使用されました。</span><span class="sxs-lookup"><span data-stu-id="37ace-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="37ace-296">複数の同じようなフィールドに対してするよりも、1 つの計算済みフィールドを使用および管理する方がはるかに簡単です。</span><span class="sxs-lookup"><span data-stu-id="37ace-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="37ace-297">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="37ace-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="37ace-298">派生形式の調整したバージョンを完了する。</span><span class="sxs-lookup"><span data-stu-id="37ace-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="37ace-299">**バージョン** クイック タブで、**ステータスの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="37ace-300">**完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="37ace-301">派生形式の完了したバージョンをエクスポートする</span><span class="sxs-lookup"><span data-stu-id="37ace-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="37ace-302">コンフィギュレーション ツリーで、**パラメーター化された呼び出しを知るための形式 (カスタム)** 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="37ace-303">**バージョン** クイック タブで、完成したバージョン 1.1.1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="37ace-304">**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="37ace-305">**XML ファイルとしてエクスポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="37ace-306">ダウンロードしたコンフィギュレーションを、XML 形式でローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="37ace-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="37ace-307">ER フォーマットのテスト</span><span class="sxs-lookup"><span data-stu-id="37ace-307">Test ER formats</span></span> 
<span data-ttu-id="37ace-308">初期のおよび改善されたER フォーマットを実行して、コンフィギュレーションされパラメーター化された計算済みフィールドが正しく動作することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="37ace-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="37ace-309">ER コンフィギュレーションをインポートする</span><span class="sxs-lookup"><span data-stu-id="37ace-309">Import ER configurations</span></span>
<span data-ttu-id="37ace-310">**RCS** タイプの ER レポジトリを使用して、確認済みのコンフィギュレーションを RCS からインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="37ace-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="37ace-311">既に、[規制コンフィギュレーション サービスからの電子申告コンフィギュレーションのインポート](rcs-download-configurations.md) のトピックにある手順を実行している場合は、コンフィギュレーションされた ER リポジトリを使用し、このトピックの前の方で説明したコンフィギュレーションを環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="37ace-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="37ace-312">そうでない場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="37ace-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="37ace-313">会社 **DEMF** を選択し、既定のダッシュボードで**電子申告**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="37ace-314">**コンフィギュレーションをレポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="37ace-315">Microsoft ダウンロード センターから、コンフィギュレーションを次の順序でインポートします。データ モデル、モデル マッピング、フォーマット。</span><span class="sxs-lookup"><span data-stu-id="37ace-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="37ace-316">各 ER コンフィギュレーションごとに次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="37ace-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="37ace-317">**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="37ace-318">**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="37ace-319">**参照**を選択し、必要な ER コンフィギュレーションを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="37ace-320">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-320">Select **OK**.</span></span>

4. <span data-ttu-id="37ace-321">RCS からエクスポートされた**パラメーター化された呼び出しを知るための形式 (カスタム)** フォーマットの完了したバージョン 1.1.1 をインポートします。</span><span class="sxs-lookup"><span data-stu-id="37ace-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="37ace-322">**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="37ace-323">**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="37ace-324">**参照**を選択し、XML 形式でローカルに保存されている**パラメーター化された呼び出しを知るための形式 (カスタム)** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="37ace-325">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="37ace-326">ER フォーマットの実行</span><span class="sxs-lookup"><span data-stu-id="37ace-326">Run ER formats</span></span>

1. <span data-ttu-id="37ace-327">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し**の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="37ace-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="37ace-328">**パラメーター化された呼び出しを知るための形式**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="37ace-329">最上部のリボンにある**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="37ace-330">ローカルに生成された出力を保存します。</span><span class="sxs-lookup"><span data-stu-id="37ace-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="37ace-331">**パラメーター化された呼び出しを知るための形式 (カスタム)** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="37ace-332">最上部のリボンにある**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ace-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="37ace-333">生成された出力をローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="37ace-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="37ace-334">生成された出力の内容を比較します。</span><span class="sxs-lookup"><span data-stu-id="37ace-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37ace-335">追加リソース</span><span class="sxs-lookup"><span data-stu-id="37ace-335">Additional resources</span></span>
[<span data-ttu-id="37ace-336">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="37ace-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
