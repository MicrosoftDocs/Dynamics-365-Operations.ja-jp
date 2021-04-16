---
title: 計算済みフィールド タイプの ER データ ソースの、パラメーター化された呼び出しをサポートする
description: このトピックでは、ER データ ソースに対して計算済みフィールド タイプを使用する方法について説明します。
author: NickSelin
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 897133a27f9d3da2f576ce675c0949f824cde881
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749492"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="92d07-103">計算済みフィールド タイプの ER データ ソースの、パラメーター化された呼び出しをサポートする</span><span class="sxs-lookup"><span data-stu-id="92d07-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92d07-104">このトピックでは、**計算済みフィールド** タイプを使用して電子レポート (ER) データ ソースをデザインする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="92d07-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="92d07-105">このデータソースには ER 式が含まれている可能性があり、この式を実行すると、このデータ ソースを呼び出すバインドで構成されているパラメータ引数の値によって制御することができます。</span><span class="sxs-lookup"><span data-stu-id="92d07-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="92d07-106">このようなデータ ソースのパラメーター化された呼び出しを構成することにより、1 つのデータ ソースを多数のバインドで再利用できます。これにより、ER モデル マッピングまたは ER フォーマットで構成する必要があるデータ ソースの総数を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="92d07-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="92d07-107">また、構成済みの ER コンポーネントが簡素化され、これにより保守コストおよび他の消費者が使用するコストが削減されます。</span><span class="sxs-lookup"><span data-stu-id="92d07-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="92d07-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="92d07-108">Prerequisites</span></span>
<span data-ttu-id="92d07-109">このトピックの例を完了するには、次のアクセスが必要です:</span><span class="sxs-lookup"><span data-stu-id="92d07-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="92d07-110">これらのロールにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="92d07-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="92d07-111">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="92d07-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="92d07-112">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="92d07-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="92d07-113">システム管理者</span><span class="sxs-lookup"><span data-stu-id="92d07-113">System administrator</span></span>

- <span data-ttu-id="92d07-114">次のいずれかのロールで、Finance and Operations と同じテナントに対してプロビジョニングされている Regulatory Configuration Services (RCS) にアクセスします:</span><span class="sxs-lookup"><span data-stu-id="92d07-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="92d07-115">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="92d07-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="92d07-116">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="92d07-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="92d07-117">システム管理者</span><span class="sxs-lookup"><span data-stu-id="92d07-117">System administrator</span></span>

<span data-ttu-id="92d07-118">次のファイルをローカルにダウンロードして保存する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="92d07-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="92d07-119">**コンテンツ**</span><span class="sxs-lookup"><span data-stu-id="92d07-119">**Content**</span></span>                           | <span data-ttu-id="92d07-120">**ファイル名**</span><span class="sxs-lookup"><span data-stu-id="92d07-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92d07-121">ER データ モデル構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="92d07-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="92d07-122">パラメーター化された呼び出し version.1.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="92d07-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="92d07-123">ER メタデータ構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="92d07-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="92d07-124">パラメーター化された呼び出し version.1.xml を知るためのメタデータ</span><span class="sxs-lookup"><span data-stu-id="92d07-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="92d07-125">ER モデル マッピング構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="92d07-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="92d07-126">パラメーター化された呼び出し version.1.1.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="92d07-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="92d07-127">ER フォーマット構成のサンプル</span><span class="sxs-lookup"><span data-stu-id="92d07-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="92d07-128">パラメーター化された呼び出し version.1.1.xml を知るための形式</span><span class="sxs-lookup"><span data-stu-id="92d07-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="92d07-129">RCS インスタンスにサインインする</span><span class="sxs-lookup"><span data-stu-id="92d07-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="92d07-130">この例では、サンプル会社 Litware, Inc. 用に、コンフィギュレーションを作成します。まず、RCS で、手順 [コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md) にあるステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d07-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="92d07-131">既定のダッシュボードで、**電子申告** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="92d07-132">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="92d07-133">ダウンロードしたコンフィギュレーションを、次の順序で RCS にインポートします。データ モデル、メタデータ、モデル マッピング、フォーマット。</span><span class="sxs-lookup"><span data-stu-id="92d07-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="92d07-134">各 ER コンフィギュレーションごとに次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="92d07-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="92d07-135">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="92d07-136">**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="92d07-137">**参照** を選択してから、必要な ER コンフィギュレーションを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="92d07-138">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="92d07-139">指定された ER ソリューションを確認する</span><span class="sxs-lookup"><span data-stu-id="92d07-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="92d07-140">モデル マッピングを確認する</span><span class="sxs-lookup"><span data-stu-id="92d07-140">Review model mapping</span></span>

1. <span data-ttu-id="92d07-141">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し** の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="92d07-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="92d07-142">**パラメーター化された呼び出しを知るためのマッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="92d07-143">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92d07-143">Select **Designer**.</span></span>
4. <span data-ttu-id="92d07-144">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92d07-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="92d07-145">この ER モデルマッピングは、次のように設計されています。</span><span class="sxs-lookup"><span data-stu-id="92d07-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="92d07-146">**TaxTable** テーブルに存在する税コード (**税** データ ソース) のリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="92d07-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="92d07-147">**TaxTrans** テーブルに存在する税トランザクション (**トランザクション** データ ソース) のリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="92d07-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="92d07-148">取得したトランザクション (**Gr** データ ソース) のリストを、税コード別にグループ化します。</span><span class="sxs-lookup"><span data-stu-id="92d07-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="92d07-149">税コードごとに集計された値に従って、グループ化されたトランザクションを計算します。</span><span class="sxs-lookup"><span data-stu-id="92d07-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="92d07-150">税基準値の合計。</span><span class="sxs-lookup"><span data-stu-id="92d07-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="92d07-151">税額の合計。</span><span class="sxs-lookup"><span data-stu-id="92d07-151">Sum of tax values.</span></span>
            - <span data-ttu-id="92d07-152">適用される税率の最小値。</span><span class="sxs-lookup"><span data-stu-id="92d07-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="92d07-153">このコンフィギュレーションのモデル マッピングは、このモデルに対して作成され Finance and Operations で実行される、すべての ER フォーマットの基本データ モデルを実装します。</span><span class="sxs-lookup"><span data-stu-id="92d07-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="92d07-154">その結果、**税** および **Gr** データ ソースの内容は、抽象データ ソースなどの ER フォーマットに対して公開されます。</span><span class="sxs-lookup"><span data-stu-id="92d07-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![税および Gr データ ソースを表示するモデル マッピング デザイナー ページ](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="92d07-156">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92d07-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="92d07-157">**モデル マッピング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92d07-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="92d07-158">形式の確認</span><span class="sxs-lookup"><span data-stu-id="92d07-158">Review format</span></span>

1. <span data-ttu-id="92d07-159">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し** の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="92d07-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="92d07-160">**パラメーター化された呼び出しを知るための形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="92d07-161">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92d07-161">Select **Designer**.</span></span> <span data-ttu-id="92d07-162">この ER フォーマットは次のように設計されています。</span><span class="sxs-lookup"><span data-stu-id="92d07-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="92d07-163">税明細書を XML 形式で生成します。</span><span class="sxs-lookup"><span data-stu-id="92d07-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="92d07-164">税明細書に以下の課税レベルを提示します。標準、減額、なし。</span><span class="sxs-lookup"><span data-stu-id="92d07-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="92d07-165">各レベルで詳細条件を持つ、各課税レベルにおける複数の詳細を提示します。</span><span class="sxs-lookup"><span data-stu-id="92d07-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![形式デザイナーのページ](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="92d07-167">**マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="92d07-168">**モデル**、**データ、** および **集計** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="92d07-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="92d07-169">計算済みフィールド **モデル.データ.集計.レベル** は、その **モデル.データ.集計** データ ソースから実行時に取得できるすべての税コードのテキスト値として、(**標準**、**減額**、**なし、** または **その他**) の課税レベル コードを返す式が含まれます。</span><span class="sxs-lookup"><span data-stu-id="92d07-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![パラメーター化された呼び出しを知るためのモデルの、データ モデル詳細を表示するフォーマット デザイナー ページ](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="92d07-171">**モデル**.**データ 2** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="92d07-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="92d07-172">**モデル**.**データ 2. 集計 2** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="92d07-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="92d07-173">この **モデル**.**データ2.集計2** データ ソースは、課税レベル (**モデル.データ.集計.レベル** 計算済みフィールドによって返されます) によって **モデル.データ.集計** データ ソース トランザクション の詳細をグループ化し、集計を計算するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="92d07-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![モデル.データ 2.集計 2 データ ソースの詳細を表示する形式デザイナー ページ](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="92d07-175">計算済みフィールドの **モデル**.**データ 2.レベル 1** 、**モデル**.**データ 2.レベル 2** 、および **モデル**.**データ 2.レベル 3** を確認します。</span><span class="sxs-lookup"><span data-stu-id="92d07-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="92d07-176">これらの計算済みフィールドは、**モデル**.**データ 2.集計 2** レコード リストをフィルターするために使用され、特定の課税レベルを表すレコードだけを返します。</span><span class="sxs-lookup"><span data-stu-id="92d07-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="92d07-177">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92d07-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="92d07-178">派生形式を作成する</span><span class="sxs-lookup"><span data-stu-id="92d07-178">Create a derived format</span></span>
<span data-ttu-id="92d07-179">既存の 3 つのフィールドを使用するのではなく、必要な課税レベルをフィルターする 1 つの計算済みフィールドを追加することにより、指定された形式を改善することができます。**モデル**.**データ 2.レベル 1** 、**モデル**.**データ 2.レベル 2 、** および **モデル**.**データ 2.レベル 3** 。</span><span class="sxs-lookup"><span data-stu-id="92d07-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="92d07-180">必要な課税レベルは、この新しい計算済みフィールドが呼び出される場所に指定できます。</span><span class="sxs-lookup"><span data-stu-id="92d07-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="92d07-181">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し** の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="92d07-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="92d07-182">**パラメーター化された呼び出しを知るための形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="92d07-183">**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="92d07-184">**名前から派生: パラメーター化された呼び出しを知るための形式、Microsoft** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="92d07-185">**名前** フィールドに、**パラメーター化された呼び出しを知るための形式 (カスタム)** を入力します。</span><span class="sxs-lookup"><span data-stu-id="92d07-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="92d07-186">**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="92d07-187">レコード一覧を返すパラメーター化された計算済みフィールドを、コンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="92d07-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="92d07-188">新しい計算済みフィールドの追加を開始する</span><span class="sxs-lookup"><span data-stu-id="92d07-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="92d07-189">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92d07-189">Select **Designer**.</span></span>
2. <span data-ttu-id="92d07-190">**展開/折りたたみ** を選択し、すべての形式項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="92d07-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="92d07-191">**マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="92d07-192">**モデル** 項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="92d07-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="92d07-193">**モデル.データ 2** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="92d07-194">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-194">Select **Add**.</span></span>
7. <span data-ttu-id="92d07-195">**機能\\計算済みフィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="92d07-196">**名前** フィールドに、**レベル** と入力します。</span><span class="sxs-lookup"><span data-stu-id="92d07-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="92d07-197">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="92d07-198">計算済みフィールドを追加するためにパラメーターを定義する</span><span class="sxs-lookup"><span data-stu-id="92d07-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="92d07-199">**パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="92d07-200">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-200">Select **New**.</span></span>
3. <span data-ttu-id="92d07-201">**名前** フィールドに、**課税レベル** と入力します。</span><span class="sxs-lookup"><span data-stu-id="92d07-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="92d07-202">**タイプ** フィールドで、**文字列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="92d07-203">パラメーター引数のタイプを指定するために使用できるのは、プリミティブ データ型だけです。</span><span class="sxs-lookup"><span data-stu-id="92d07-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="92d07-204">そのため、**レコード リスト**、**レコード**、および **列挙** タイプはこの目的では使用できません。</span><span class="sxs-lookup"><span data-stu-id="92d07-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="92d07-205">1 つの計算済みフィールドに対して指定できるパラメーターの最大数は、8 です。</span><span class="sxs-lookup"><span data-stu-id="92d07-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![パラメーター データ ソース リスト](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="92d07-207">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-207">Select **OK**.</span></span>

<span data-ttu-id="92d07-208">このパラメーターを追加することにより、この計算済みフィールドを呼び出すために満たすべき条件が指定されます。</span><span class="sxs-lookup"><span data-stu-id="92d07-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="92d07-209">この計算済みフィールドを呼び出す際、**課税レベル** パラメーターの引数を、**文字列** 形式の値として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d07-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="92d07-210">コンテナーに存在する計算済みフィールド (**レコード リスト**、**レコード**、または **コンテナー**) に対してのみ、パラメーターを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d07-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="92d07-211">コンフィギュレーションされたパラメーターは、この計算済みフィールドのためのデータ ソースのリスト内で使用できます。</span><span class="sxs-lookup"><span data-stu-id="92d07-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="92d07-212">**データソースの追加** を選択すると、コンフィギュレーションされた式にパラメーターを追加できます。</span><span class="sxs-lookup"><span data-stu-id="92d07-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![データ ソース フィールド](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="92d07-214">計算済みフィールドを追加するために式を定義する</span><span class="sxs-lookup"><span data-stu-id="92d07-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="92d07-215">**フォーミュラ** フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="92d07-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="92d07-216">**WHERE(\@.集計 2、 \@.集計 2.グループ化.レベル =**</span><span class="sxs-lookup"><span data-stu-id="92d07-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="92d07-217">データ ソースのリストで、**課税レベル** パラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="92d07-218">**データソースの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="92d07-219">**フォーミュラ** フィールドで、次の式を確定します。</span><span class="sxs-lookup"><span data-stu-id="92d07-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="92d07-220">**WHERE(\@.集計 2, \@.集計 2.グループ化.レベル = '課税レベル')**</span><span class="sxs-lookup"><span data-stu-id="92d07-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="92d07-221">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-221">Select **Save**.</span></span>

    ![データ ソース フィールドの情報](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="92d07-223">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92d07-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="92d07-224">新しい計算済みフィールドの追加を完了する</span><span class="sxs-lookup"><span data-stu-id="92d07-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="92d07-225">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-225">Select **OK**.</span></span>

<span data-ttu-id="92d07-226">**フォーマット デザイナー** ページ上で、コンフィギュレーションされパラメーター化された計算済みフィールド **レベル** には、**文字列** 引数が必要です。</span><span class="sxs-lookup"><span data-stu-id="92d07-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![計算済みフィールド レベルの展開されたリスト](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements&quot;></a><span data-ttu-id=&quot;92d07-228&quot;>バインディング フォーマット要素のため、コンフィギュレーションされた計算済みフィールドを使用する</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-228&quot;>Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id=&quot;92d07-229&quot;>**モデル.データ 2.レベル** を選択し、コンフィギュレーションされた計算済みフィールドを選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-229&quot;>Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id=&quot;92d07-230&quot;>**明細書.課税.標準** 形式要素を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-230&quot;>Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id=&quot;92d07-231&quot;>**バインド** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-231&quot;>Select **Bind**.</span></span>
4. <span data-ttu-id=&quot;92d07-232&quot;>**はい** を選択し、選択された形式要素のすべての入れ子になった形式内で、新しいデータ ソース **レベル** によって、現在使用されているデータ ソース **レベル 1** が置き換えられることを確認します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-232&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id=&quot;92d07-233&quot;>適用したバインディングは、パラメーター化された計算済みフィールドの呼び出しとして作成されました。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-233&quot;>Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id=&quot;92d07-234&quot;>既定では、バインド形式要素の名前は、次の条件下で、パラメーター化された計算済みフィールドに対する引数として使用されます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-234&quot;>By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id=&quot;92d07-235&quot;>計算済みフィールドは 1 つのパラメータを使用するようにコンフィギュレーションされています。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-235&quot;>The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id=&quot;92d07-236&quot;>このパラメータのデータ タイプは、**文字列** として定義されています。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-236&quot;>The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id=&quot;92d07-237&quot;>バインド形式要素の名前が空白の場合、この要素のデータ ソース名は、適用したバインディングで使用されます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-237&quot;>When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id=&quot;92d07-238&quot;>**明細書.課税.減額** 形式要素を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-238&quot;>Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id=&quot;92d07-239&quot;>**バインド** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-239&quot;>Select **Bind**.</span></span>
7. <span data-ttu-id=&quot;92d07-240&quot;>**はい** を選択し、選択された形式要素の下にあるすべての入れ子になった形式内で、新しいデータ ソース **レベル** によって、現在使用されているデータ ソース **レベル 2** が置き換えられることを確認します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-240&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id=&quot;92d07-241&quot;>**明細書.課税.なし** 形式要素を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-241&quot;>Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id=&quot;92d07-242&quot;>**バインド** を選択します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-242&quot;>Select **Bind**.</span></span>
10. <span data-ttu-id=&quot;92d07-243&quot;>**はい** を選択し、選択された形式要素の下にあるすべての入れ子になった形式内で、新しいデータ ソース **レベル** によって、現在使用されているデータ ソース **レベル 3** が置き換えられることを確認します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;92d07-243&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id=&quot;92d07-244&quot;>課税レベル (たとえば **モデル.データ 2.レベル (&quot;減額")** テキスト値として) を表す XML 要素に対するパラメーター化された計算済みフィールドの引数を指定する場合、入れ子にされた XML 属性に対して同じ操作をする必要はありません。それらのバインドは、親レベル (**モデル.データ 2.レベル.集計された.ベース**、**モデル.データ 2.レベル ("減額")** 集計された.ベースではない) で定義されている引数の値を自動的に継承します。</span><span class="sxs-lookup"><span data-stu-id="92d07-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="92d07-245">どのパラメーター化された計算済みフィールドの繰り返し呼び出しも、サポートされません。</span><span class="sxs-lookup"><span data-stu-id="92d07-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="92d07-246">**式の編集** を選択して、選択したバインドの中でパラメーター化された計算済みフィールドの既定で適用される引数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="92d07-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="92d07-247">この引数が見つからない場合、実行時にエラーが発生する可能性があります。そのような状況は、現在の形式が検証されたときに、ユーザーに通知されます。</span><span class="sxs-lookup"><span data-stu-id="92d07-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![検証時の警告の通知](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="92d07-249">パラメーター化された計算済みフィールドをコンフィギュレーションし、レコードを返す</span><span class="sxs-lookup"><span data-stu-id="92d07-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="92d07-250">パラメーター化された計算済みフィールドがレコードを返す場合、このレコードの個々のフィールド バインドを形式要素にサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d07-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="92d07-251">そのような場合、パラメーター化された計算済みフィールドを呼び出す、引数の値を含む親バインドがありません。この値は、1 つのレコード フィールドのバインドで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d07-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="92d07-252">新しい計算済みフィールドの追加を開始する</span><span class="sxs-lookup"><span data-stu-id="92d07-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="92d07-253">**モデル.データ 2** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="92d07-254">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-254">Select **Add**.</span></span>
3. <span data-ttu-id="92d07-255">**機能\\計算済みフィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="92d07-256">**名前** フィールドに、**レベル レコード** と入力します。</span><span class="sxs-lookup"><span data-stu-id="92d07-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="92d07-257">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="92d07-258">計算済みフィールドを追加するためにパラメーターを定義する</span><span class="sxs-lookup"><span data-stu-id="92d07-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="92d07-259">**パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="92d07-260">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-260">Select **New**.</span></span>
3. <span data-ttu-id="92d07-261">**名前** フィールドに、**課税レベル** と入力します。</span><span class="sxs-lookup"><span data-stu-id="92d07-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="92d07-262">**タイプ** フィールドで、**文字列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="92d07-263">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="92d07-264">計算済みフィールドを追加するために式を定義する</span><span class="sxs-lookup"><span data-stu-id="92d07-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="92d07-265">**フォーミュラ** フィールドで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="92d07-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="92d07-266">**FIRSTORNULL(\@.レベル(**</span><span class="sxs-lookup"><span data-stu-id="92d07-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="92d07-267">**課税レベル** パラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="92d07-268">**データソースの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="92d07-269">**フォーミュラ** フィールドで、手順 1 で入力したものに **' 課税レベル '))** を上書きし、式をこのように確定します。</span><span class="sxs-lookup"><span data-stu-id="92d07-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="92d07-270">**FIRSTORNULL(\@.レベル ('課税レベル'))**</span><span class="sxs-lookup"><span data-stu-id="92d07-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="92d07-271">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-271">Select **Save**.</span></span>
6. <span data-ttu-id="92d07-272">**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92d07-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="92d07-273">新しい計算済みフィールドの追加を完了する</span><span class="sxs-lookup"><span data-stu-id="92d07-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="92d07-274">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="92d07-275">形式要素をバインドするため、コンフィギュレーションされた計算済みフィールドを使用する</span><span class="sxs-lookup"><span data-stu-id="92d07-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="92d07-276">**モデル.データ 2.レベル レコード** を展開し、コンフィギュレーションされた計算済みフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="92d07-277">コンフィギュレーションされた計算済みフィールドの、**モデル.データ 2.レベル レコード.集計** コンテナーを展開します。</span><span class="sxs-lookup"><span data-stu-id="92d07-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="92d07-278">**モデル.データ 2.レベル レコード.集計された.ベース** フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="92d07-279">**明細書.課税.なし** 形式要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="92d07-280">**バインドの解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="92d07-281">**明細書.課税.なし.ベース** 形式要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="92d07-282">**バインド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-282">Select **Bind**.</span></span>
8. <span data-ttu-id="92d07-283">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="92d07-284">式を、**モデル.データ 2.レベル レコード (" なし ") 集計された.ベース** に変更します。</span><span class="sxs-lookup"><span data-stu-id="92d07-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![更新された式](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="92d07-286">使用されていない計算済みフィールドを削除する</span><span class="sxs-lookup"><span data-stu-id="92d07-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="92d07-287">**モデル.データ 2.レベル 1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="92d07-288">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-288">Select **Delete**.</span></span>
3. <span data-ttu-id="92d07-289">**モデル.データ 2.レベル 2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="92d07-290">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-290">Select **Delete**.</span></span>
5. <span data-ttu-id="92d07-291">**モデル.データ 2.レベル 3** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="92d07-292">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-292">Select **Delete**.</span></span>
7. <span data-ttu-id="92d07-293">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="92d07-294">形式バインドの中で、同じ計算済フィールド **モデル.データ 2.レベル** が複数回再使用されました。</span><span class="sxs-lookup"><span data-stu-id="92d07-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="92d07-295">複数の同じようなフィールドに対してするよりも、1 つの計算済みフィールドを使用および管理する方がはるかに簡単です。</span><span class="sxs-lookup"><span data-stu-id="92d07-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="92d07-296">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92d07-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="92d07-297">派生形式の調整したバージョンを完了する。</span><span class="sxs-lookup"><span data-stu-id="92d07-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="92d07-298">**バージョン** クイック タブで、**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="92d07-299">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="92d07-300">派生形式の完了したバージョンをエクスポートする</span><span class="sxs-lookup"><span data-stu-id="92d07-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="92d07-301">コンフィギュレーション ツリーで、**パラメーター化された呼び出しを知るための形式 (カスタム)** 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="92d07-302">**バージョン** クイック タブで、完成したバージョン 1.1.1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="92d07-303">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="92d07-304">**XML ファイルとしてエクスポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="92d07-305">ダウンロードしたコンフィギュレーションを、XML 形式でローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="92d07-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="92d07-306">ER フォーマットのテスト</span><span class="sxs-lookup"><span data-stu-id="92d07-306">Test ER formats</span></span> 
<span data-ttu-id="92d07-307">初期のおよび改善されたER フォーマットを実行して、コンフィギュレーションされパラメーター化された計算済みフィールドが正しく動作することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="92d07-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="92d07-308">ER コンフィギュレーションをインポートする</span><span class="sxs-lookup"><span data-stu-id="92d07-308">Import ER configurations</span></span>
<span data-ttu-id="92d07-309">**RCS** タイプの ER レポジトリを使用して、確認済みのコンフィギュレーションを RCS からインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="92d07-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="92d07-310">既に、[規制コンフィギュレーション サービス (RCS) からの電子申告 (ER) コンフィギュレーションのインポート](rcs-download-configurations.md) のトピックにある手順を実行している場合は、コンフィギュレーションされた ER リポジトリを使用し、このトピックの前の方で説明したコンフィギュレーションを環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="92d07-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="92d07-311">そうでない場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="92d07-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="92d07-312">会社 **DEMF** を選択し、既定のダッシュボードで **電子申告** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="92d07-313">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="92d07-314">Microsoft ダウンロード センターから、コンフィギュレーションを次の順序でインポートします。データ モデル、モデル マッピング、フォーマット。</span><span class="sxs-lookup"><span data-stu-id="92d07-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="92d07-315">各 ER コンフィギュレーションごとに次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="92d07-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="92d07-316">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="92d07-317">**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="92d07-318">**参照** を選択し、必要な ER コンフィギュレーションを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="92d07-319">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-319">Select **OK**.</span></span>

4. <span data-ttu-id="92d07-320">RCS からエクスポートされた **パラメーター化された呼び出しを知るための形式 (カスタム)** フォーマットの完了したバージョン 1.1.1 をインポートします。</span><span class="sxs-lookup"><span data-stu-id="92d07-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="92d07-321">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="92d07-322">**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="92d07-323">**参照** を選択し、XML 形式でローカルに保存されている **パラメーター化された呼び出しを知るための形式 (カスタム)** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="92d07-324">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="92d07-325">ER フォーマットの実行</span><span class="sxs-lookup"><span data-stu-id="92d07-325">Run ER formats</span></span>

1. <span data-ttu-id="92d07-326">コンフィギュレーション ツリーで、**モデルのコンテンツを展開しパラメーター化された呼び出し** の項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="92d07-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="92d07-327">**パラメーター化された呼び出しを知るための形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="92d07-328">最上部のリボンにある **実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="92d07-329">ローカルに生成された出力を保存します。</span><span class="sxs-lookup"><span data-stu-id="92d07-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="92d07-330">**パラメーター化された呼び出しを知るための形式 (カスタム)** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="92d07-331">最上部のリボンにある **実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92d07-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="92d07-332">生成された出力をローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="92d07-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="92d07-333">生成された出力の内容を比較します。</span><span class="sxs-lookup"><span data-stu-id="92d07-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92d07-334">追加リソース</span><span class="sxs-lookup"><span data-stu-id="92d07-334">Additional resources</span></span>

- [<span data-ttu-id="92d07-335">電子申告 (ER) のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="92d07-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="92d07-336">パラメーター化された計算フィールドのデータ ソースを追加して、ER ソリューションのパフォーマンスを向上させる</span><span class="sxs-lookup"><span data-stu-id="92d07-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]