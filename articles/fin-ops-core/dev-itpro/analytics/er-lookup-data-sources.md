---
title: ER アプリケーション固有のパラメータを使用するルックアップ データ ソースのコンフィギュレーション
description: このトピックでは、ER アプリケーション固有のパラメーターを使用して電子申告 (ER) 形式のルックアップ データ ソースを構成する方法について説明します。
author: NickSelin
ms.date: 04/02/2021
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
ms.openlocfilehash: 131d14f1f1aa329bd71b1f8a4015192736bd8e44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022578"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a><span data-ttu-id="cfa17-103">ER アプリケーション固有のパラメータを使用するルックアップ データ ソースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cfa17-103">Configure Lookup data sources to use ER application-specific parameters</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cfa17-104">[電子申告 (ER)](general-electronic-reporting.md) アプリケーション固有のパラメーター機能を使用すると、データ フィルターを ER 形式に構成して、一連の抽象的なルールに基づくようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-104">The [Electronic reporting (ER)](general-electronic-reporting.md) application-specific parameters feature lets you configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="cfa17-105">このルール セットは、ER 形式で使用可能な **ルックアップ** タイプのデータ ソースを使用するように構成できます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-105">This set of rules can be configured to use the data source of the **Lookup** type that is available in an ER format.</span></span> <span data-ttu-id="cfa17-106">対応する ER 形式と現在の法人データの **ルックアップ** データ ソース設定に基づいて自動的に生成されるユーザー インターフェイス (UI) を使用して、ER コンポーネント デザイナーを超えた実際のルールを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-106">You can then specify real rules beyond the ER components designers by using the user interface (UI) that is automatically generated based on the settings of the **Lookup** data source of the corresponding ER format and the current legal entity data.</span></span> <span data-ttu-id="cfa17-107">最終的には、この ER 形式を実行するとき、指定したルールは ER 形式の **ルックアップ** データ ソースによってアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-107">Eventually, the specified rules will be accessed by the ER format's **Lookup** data source when this ER format is executed.</span></span>

> [!NOTE]
> <span data-ttu-id="cfa17-108">編集可能な ER 形式の構成されたデータ ソースを使用して、実際のルールの構成に使用するアプリケーション データを指定します。</span><span class="sxs-lookup"><span data-stu-id="cfa17-108">Use the configured data sources of the editable ER format to specify what application data is used to configure real rules.</span></span>

<span data-ttu-id="cfa17-109">[ER Operations デザイナー](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) を使用して、**ルックアップ** タイプのデータ ソースを ER 形式で移動します。</span><span class="sxs-lookup"><span data-stu-id="cfa17-109">Use the [ER Operations designer](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) to bring a data source of the **Lookup** type in to your ER format.</span></span> <span data-ttu-id="cfa17-110">次を含め、データ ソースを構成して、抽象的なルールの表示方法を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfa17-110">The data source must be configured to describe how your abstract rules look, including the following:</span></span>

   - <span data-ttu-id="cfa17-111">1 つのルールを指定するために値が指定されている特定のデータ型のパラメーター セット。</span><span class="sxs-lookup"><span data-stu-id="cfa17-111">The parameter set of certain data type whose value is provided to specify a single rule.</span></span>
   - <span data-ttu-id="cfa17-112">このルールがその他よりも最も適していると見なされる場合に 1 つのルールによって返される特定のデータ型の値の型。</span><span class="sxs-lookup"><span data-stu-id="cfa17-112">The value type of certain data type that is returned by a single rule when this rule is considered the most appropriate among others.</span></span>

<span data-ttu-id="cfa17-113">構成された任意のルールによって返される値の型に応じて、次のタイプの **ルックアップ** データ ソースを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-113">You can configure the following types of **Lookup** data sources depending on the type of value that is returned by any configured rule:</span></span>

   - <span data-ttu-id="cfa17-114">モデル列挙値が返される必要がある場合は、**データ モデル\ルックアップ** タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="cfa17-114">Use the **Data model\Lookup** type when a model enumeration value must be returned.</span></span>
   - <span data-ttu-id="cfa17-115">アプリケーションの列挙値またはアプリケーションの [拡張データ型](../extensibility/extensible-edts.md) の値を返す必要がある場合は、**Dynamics 365 工程\ルックアップ** タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="cfa17-115">Use the **Dynamics 365 Operations\Lookup** type when an application enumeration value or an application [extended data type](../extensibility/extensible-edts.md) value must be returned.</span></span>
   - <span data-ttu-id="cfa17-116">形式列挙値が返される必要がある場合は、**形式列挙型\ルックアップ** タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="cfa17-116">Use the **Format enumeration\Lookup** type when a format enumeration value must be returned.</span></span>

<span data-ttu-id="cfa17-117">次の図は、サンプルの ER 形式で形式列挙型を構成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-117">The following illustration shows how a format enumeration can be configured in the sample ER format.</span></span>

   ![構成されたルックアップ データ ソースの基礎として形式列挙型を表示する](./media/er-lookup-data-sources-img1.gif)

<span data-ttu-id="cfa17-119">次の図は、さまざまなタイプの税を生成されたレポートとは別のセクションで報告するように構成された形式コンポーネントを示しています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-119">The following illustration shows the format components that were configured to report different type of taxes in a different section of a generated report.</span></span>

   ![さまざまなタイプの税を個別に報告する形式セクションを表示する](./media/er-lookup-data-sources-img2.png)

<span data-ttu-id="cfa17-121">次の図は、ER Operations デザイナーによって、**形式列挙型\ルックアップ** タイプのデータ ソースの追加を許可する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-121">The following illustration shows how the ER Operations designer allows the addition of a data source of the **Format enumeration\Lookup** type.</span></span>  <span data-ttu-id="cfa17-122">追加したデータ ソースは、`List of taxation levels` 形式列挙型の値を返すするように構成されています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-122">The added data source is configured as returning a value of the `List of taxation levels` format enumeration.</span></span>

   ![形式列挙型\ルックアップ タイプの ER データ ソースを追加する](./media/er-lookup-data-sources-img3.gif)

<span data-ttu-id="cfa17-124">次の図は、追加されたデータ ソースが、**モデル** データ ソース内の **Model.Data.Tax** レコード リストの **コード** フィールドを、すべての構成済みルールに対して指定される必要のあるパラメーターとして使用するよう構成される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-124">The following illustration shows how the added data source is configured to use the **Code** field of the **Model.Data.Tax** record list of the **Model** data source as a parameter that must be specified for every configured rule.</span></span>

![形式列挙型\ルックアップ タイプの追加データ ソースのパラメータのコンフィギュレーション](./media/er-lookup-data-sources-img4.gif)

<span data-ttu-id="cfa17-126">追加された `Model.Data.Tax` データ ソースは、**TaxTable** アプリケーション テーブルのレコードにアクセスすることにより、すべての構成済みルールに対して税コードを指定するように構成されます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-126">The added `Model.Data.Tax` data source is configured to specify a tax code for every configured rule by accessing records of the **TaxTable** application table.</span></span>

   ![1 つの会社の形式列挙型\ルックアップ タイプのルックアップ データ ソースの確認](./media/er-lookup-data-sources-img5.gif)

<span data-ttu-id="cfa17-128">自動的に構成済みデータ ソースの構造にアラインされた UI を使用して、選択した ER 形式のルックアップ ルールを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-128">You can set up the lookup rules for the selected ER format by using the UI that is automatically aligned with the structure of the configured data source.</span></span> <span data-ttu-id="cfa17-129">現在、この UI は、各ルールについて、戻り値をパラメーターとしての税コードと同様に `List of taxation levels` 形式として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfa17-129">Currently, this UI requires that for each rule, you specify the returned value as the `List of taxation levels` format enumeration value as well as the tax code as a parameter.</span></span>

   ![構成済みデータ ソースのルールを設定する](./media/er-lookup-data-sources-img6.gif)

<span data-ttu-id="cfa17-131">次の図は、**計算済みフィールド** タイプの `Model.Data.Summary.LevelByLookup` データ ソースを、必要なパラメーターを提供する **ルックアップ** データ ソースを呼び出すように構成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-131">The following illustration shows how the `Model.Data.Summary.LevelByLookup` data source of the **Calculated field** type can be configured to call the configured **Lookup** data source providing the required parameters.</span></span> <span data-ttu-id="cfa17-132">実行時にこの呼び出しを処理するために、ER は定義された順序で構成されたルールの一覧を確認し、指定された条件を満たす最初のルールを探します。</span><span class="sxs-lookup"><span data-stu-id="cfa17-132">To process this call at runtime, ER goes through the list of configured rules in the defined sequence to locate the first rule that satisfies the provided conditions.</span></span> <span data-ttu-id="cfa17-133">この例は、指定された税コードと一致する税コードを含むルールです。</span><span class="sxs-lookup"><span data-stu-id="cfa17-133">In this example, it's the rule that contains the tax code that matches the provided one.</span></span> <span data-ttu-id="cfa17-134">このため、最も適しているルールが検索され、検索されたルールに対して構成されている列挙値が、このデータ ソースによって返されます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-134">As the result, the most appropriate rule is found and the enumeration value that is configured for the found rule is returned by this data source.</span></span>

> [!NOTE]
> <span data-ttu-id="cfa17-135">該当するルールが見つからない場合に、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-135">An exception is thrown when no applicable rule is found.</span></span> <span data-ttu-id="cfa17-136">これらの例外を回避するために、ルール一覧の最後に追加のルールを構成して、構成されていない値または値が指定されなかったケースを処理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="cfa17-136">To prevent these exceptions, configure additional rules at the end of the rules list to handle cases when a non-configured value or no value is provided.</span></span> <span data-ttu-id="cfa17-137">それに応じて **\*空白でない** と **\*空白** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="cfa17-137">Use the **\*Not blank**\* and **\*Blank**\* options accordingly.</span></span>  
>
> ![データ ソースを追加して、構成済みのルックアップ データ ソースを呼び出す](./media/er-lookup-data-sources-img7.png)

<span data-ttu-id="cfa17-139">編集可能なルックアップ データ ソースに対して **会社間** オプションを **はい** に設定する場合、必要な新しい **会社** パラメーターが、このデータ ソースのパラメーター セットに追加されます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-139">When you set the **Cross-company** option to **Yes** for the editable lookup data source, you add a new required **Company** parameter to the set of parameters of this data source.</span></span> <span data-ttu-id="cfa17-140">ルックアップ データ ソースが呼び出される場合、実行時に **会社** パラメーターの値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfa17-140">The value of the **Company** parameter must be specified at runtime when the lookup data source is called.</span></span> <span data-ttu-id="cfa17-141">会社コードが実行時に指定された場合、この会社に対して構成されたルールを使用して最も適切なルールが検索され、対応する値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-141">When the company code is specified at runtime, the rules configured for this company are used to find the most appropriate rule, and the corresponding value is returned.</span></span> <span data-ttu-id="cfa17-142">次の図は、この実行方法および編集可能なデータ ソースのパラメーター セットの変更方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-142">The following illustration shows how you can do this and how the set of parameters of the editable data source is changed.</span></span>

   ![会社間の形式列挙型\ルックアップ タイプのルックアップ データ ソースの確認](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> <span data-ttu-id="cfa17-144">すべての会社を個別に選択して、編集可能な ER 形式のルックアップ データ ソースのルール セットを構成します。</span><span class="sxs-lookup"><span data-stu-id="cfa17-144">Select every company seperately to configure the set of rules for this lookup data source of the editable ER format.</span></span> <span data-ttu-id="cfa17-145">ルックアップ設定が完了していない会社のコードを使用して会社間ルックアップが呼び出される場合、実行時に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-145">An exception is thrown at runtime when the cross-company lookup is called with the code of the company for which the lookup setting was not completed.</span></span>
>
> <span data-ttu-id="cfa17-146">会社間の **ルックアップ** データ ソースを使用して ER 形式を実行し、このデータ ソースの範囲内ですべての会社のデータにアクセスするユーザーにアクセス許可が与えられていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cfa17-146">Make sure that you grant permissions for a user who runs the ER format with the cross-company **Lookup** data source to access the data of every company that is in scope of this data source.</span></span> <span data-ttu-id="cfa17-147">それ以外の場合は、実行時に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-147">Otherwise, an exception is thrown at runtime.</span></span>

<span data-ttu-id="cfa17-148">バージョン 10.0.19 から、**ルックアップ** データ ソースの拡張機能が使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="cfa17-148">Starting in version 10.0.19, the extended capabilities of the **Lookup** data sources are available.</span></span> <span data-ttu-id="cfa17-149">編集可能なルックアップ データ ソースに対して **拡張** オプションを **はい** に設定すると、構成済みルックアップ データ ソースは、構成済みのルール セットを分析する追加機能を提供する構造化されたデータ ソースに変換されます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-149">When you set the **Extended** option to **Yes** for the editable lookup data source, the configured lookup data source is transformed to the structured data source that offers the additional capabilities to analyze the configured set of rules.</span></span> <span data-ttu-id="cfa17-150">次の図は、このトランザクションを示しています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-150">The following illustration shows this transformation.</span></span>

   ![形式列挙型\ルックアップ タイプの構造化されたルックアップ データ ソースの確認](./media/er-lookup-data-sources-img9.gif)

- <span data-ttu-id="cfa17-152">**ルックアップ** のサブ項目は、指定されたパラメーター セットに基づいて構成済みのルール セットから最も適したルールを検索する関数として設計されています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-152">The **Lookup** sub-item is designed as a function to find the most appropriate rule from the set of configurable rules based on the provided set of parameters.</span></span>
- <span data-ttu-id="cfa17-153">**IsLookupResultSet** サブ項目は、指定された列挙値が戻り値として構成されたルールが少なくとも 1 つ含まれている場合に、基本列挙型データ ソースの値を受け入れ、**True** の *ブール* 値を返す関数として設計されています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-153">The **IsLookupResultSet** sub-item is designed as a function to accept the provided value of the base enumeration data source and return the *Boolean* value of **True** when the set of rules contain at least one rule for which the provided enumeration value was configured as a returned value.</span></span> <span data-ttu-id="cfa17-154">指定された列挙値を返すよう構成されたルールがない場合、関数は **False** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="cfa17-154">This function returns the *Boolean* value of **False** when there are no rules configured to return the provided enumeration value.</span></span>
- <span data-ttu-id="cfa17-155">**設定** のサブ項目は、レコード リストのレコードとして構成済みのルール セットを返す関数として設計されています。</span><span class="sxs-lookup"><span data-stu-id="cfa17-155">The **Setting** sub-item is designed as a function that returns the set of configured rules as records of a record list.</span></span> <span data-ttu-id="cfa17-156">戻り値および構成済みルールのパラメーター セットは、返されるすべてのレコードで、関連するデータ型のフィールドとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-156">The returned values and the set of parameters of the configured rules are presented in every returned record as fields of the relevant data types:</span></span>

    - <span data-ttu-id="cfa17-157">戻り値は、**ルックアップの結果** フィールドとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="cfa17-157">The returned value is presented as the **Lookup result** field.</span></span>
    - <span data-ttu-id="cfa17-158">構成済みのパラメーターは、パラメーターの名前を持つフィールドとして表示されます (この例では **コード** フィールド)。</span><span class="sxs-lookup"><span data-stu-id="cfa17-158">The configured parameters are presented as fields having names of parameters (**Code** field in this example).</span></span>

<span data-ttu-id="cfa17-159">**ルックアップ** データ ソースの構成方法の詳細については、[法人ごとに指定されたパラメーターを使用するよう電子申告形式を構成する](er-app-specific-parameters-configure-format.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfa17-159">For more information about to how configure the **Lookup** data source, see [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md).</span></span> <span data-ttu-id="cfa17-160">ルックアップ ルールを設定する方法については、[法人ごとの電子申告形式のパラメーターの設定](er-app-specific-parameters-set-up.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfa17-160">To learn how to set the Lookup rules, see [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cfa17-161">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cfa17-161">Additional resources</span></span>

[<span data-ttu-id="cfa17-162">法人ごとに指定されたパラメーターを使用するよう電子申告形式を構成する</span><span class="sxs-lookup"><span data-stu-id="cfa17-162">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)

[<span data-ttu-id="cfa17-163">法人ごとの電子申告形式のパラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="cfa17-163">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)
