---
title: 測定単位の管理
description: このトピックでは、測定単位の定義方法、単位の翻訳の提供方法とその説明、および関連する単位の換算ルールの定義方法を示します。
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921344"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="649cb-103">測定単位の管理</span><span class="sxs-lookup"><span data-stu-id="649cb-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="649cb-104">このトピックでは、測定単位の定義方法、単位の翻訳の提供方法とその説明、および関連する単位の換算ルールの定義方法を示します。</span><span class="sxs-lookup"><span data-stu-id="649cb-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="649cb-105">単位ページを開く</span><span class="sxs-lookup"><span data-stu-id="649cb-105">Open the Units page</span></span>

<span data-ttu-id="649cb-106">システムで使用できる測定単位を作成して使用するには、**組織管理 \> 設定 \> 単位 \> 単位** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="649cb-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="649cb-107">このトピックの残りのセクションでは、**単位** ページで実行できる操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="649cb-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="649cb-108">標準単位および換算を作成する</span><span class="sxs-lookup"><span data-stu-id="649cb-108">Create standard units and conversions</span></span>

<span data-ttu-id="649cb-109">システムにメートル単位または米国の慣例的単位 (USCS) の最も一般的に使用される測定単位がまだ含まれていない場合は、単位セットアップ ウィザードを使用すると、基本単位の定義と換算をすばやく開始できます。</span><span class="sxs-lookup"><span data-stu-id="649cb-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="649cb-110">ウィザードを完了するには、アクション ウィンドウで **単位作成ウィザード** を選択してから、画面に表示される指示に従います。</span><span class="sxs-lookup"><span data-stu-id="649cb-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="649cb-111">測定単位を作成または編集する</span><span class="sxs-lookup"><span data-stu-id="649cb-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="649cb-112">測定単位を作成または編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="649cb-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="649cb-113">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="649cb-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="649cb-114">既存の単位を編集するには、一覧ウィンドウで既存の単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="649cb-115">新しい単位を作成するには、アクション ウィンドウで **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="649cb-116">レコードのヘッダーで、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="649cb-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="649cb-117">**単位** – システム言語で単位を参照するために使用する ID または記号を入力します。</span><span class="sxs-lookup"><span data-stu-id="649cb-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="649cb-118">通常、この ID または記号は単位に共通する省略形です (例:*ea* は各々、または *cm* はセンチメートルを表す)。</span><span class="sxs-lookup"><span data-stu-id="649cb-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="649cb-119">**説明** – システム言語で単位の内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="649cb-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="649cb-120">通常、この名前は単位の正式名称です (*各々* または *センチメートル* など)。</span><span class="sxs-lookup"><span data-stu-id="649cb-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="649cb-121">**一般** クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="649cb-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="649cb-122">**単位クラス** – 単位が測定するプロパティ (長さ、領域、質量、数量など) を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="649cb-123">**単位系** – 単位が属する測定システム (*メートル単位* または *米国の慣例的単位*) を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="649cb-124">**基本単位** – このオプションを *はい* に設定して、現在の単位を単位クラスの基本単位として使用します。</span><span class="sxs-lookup"><span data-stu-id="649cb-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="649cb-125">この場合、単位クラスの基本単位と各追加単位間の換算係数を指定するだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="649cb-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="649cb-126">その後、システムはその単位クラスのすべての単位間で換算できます。</span><span class="sxs-lookup"><span data-stu-id="649cb-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="649cb-127">したがって、換算設定が簡単になります。</span><span class="sxs-lookup"><span data-stu-id="649cb-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="649cb-128">たとえば、ガロンが *体積* 単位クラスの基本単位である場合は、クオートからガロン、およびパイントからガロンへの換算係数を設定するだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="649cb-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="649cb-129">その後、システムはクオートからパイントにも換算できます。</span><span class="sxs-lookup"><span data-stu-id="649cb-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="649cb-130">単位クラスごとに使用できる基本単位は 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="649cb-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="649cb-131">**システム単位** – このオプションを *はい* に設定して、現在の単位を単位クラスの指定されていないすべての測定の想定単位として使用します。</span><span class="sxs-lookup"><span data-stu-id="649cb-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="649cb-132">たとえば、数量の入力に使用されるフィールドで単位を指定できない場合 (ユーザーが単位を選択しない場合)、システムは *数量* 単位クラスのシステム単位として設定された単位を使用します。</span><span class="sxs-lookup"><span data-stu-id="649cb-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="649cb-133">単位クラスごとに使用できるシステム単位は 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="649cb-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="649cb-134">**小数点以下の精度** – 現在の単位に指定された値、またはその単位に換算される値を丸める小数点以下の桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="649cb-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="649cb-135">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="649cb-136">単位の変換の定義</span><span class="sxs-lookup"><span data-stu-id="649cb-136">Define unit translations</span></span>

<span data-ttu-id="649cb-137">ID または記号の翻訳と測定単位の説明を定義するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="649cb-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="649cb-138">翻訳を作成する単位を作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="649cb-139">アクション ウィンドウで、**単位のテキスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="649cb-140">**単位のテキスト** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="649cb-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="649cb-141">このページを使用して、選択した単位に対する ID または記号の翻訳を定義します。</span><span class="sxs-lookup"><span data-stu-id="649cb-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="649cb-142">これらの翻訳は、顧客固有または仕入先固有の言語で外部ドキュメントに使用できます。</span><span class="sxs-lookup"><span data-stu-id="649cb-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="649cb-143">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="649cb-144">**言語** フィールドで、単位 ID または記号を翻訳する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="649cb-145">**テキスト** フィールドに、選択した言語で単位 ID または記号の翻訳を入力します。</span><span class="sxs-lookup"><span data-stu-id="649cb-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="649cb-146">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="649cb-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="649cb-147">Close the page.</span></span>
1. <span data-ttu-id="649cb-148">**アクション ウィンドウ** で、**翻訳済単位の説明** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="649cb-149">**翻訳済単位の説明** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="649cb-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="649cb-150">このページを使用して、選択した単位に対する言語固有の説明を定義します。</span><span class="sxs-lookup"><span data-stu-id="649cb-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="649cb-151">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="649cb-152">**言語** フィールドで、単位の説明を翻訳する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="649cb-153">**説明** フィールドに、選択した言語で単位の説明の翻訳を入力します。</span><span class="sxs-lookup"><span data-stu-id="649cb-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="649cb-154">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="649cb-155">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="649cb-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="649cb-156">単位換算ルールの定義</span><span class="sxs-lookup"><span data-stu-id="649cb-156">Define unit conversion rules</span></span>

<span data-ttu-id="649cb-157">測定単位間の換算のルールを定義するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="649cb-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="649cb-158">換算ルールを定義する単位を作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="649cb-159">アクション ウィンドウで、**単位換算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="649cb-160">**単位換算** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="649cb-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="649cb-161">このページを使用して、選択された単位を単位クラスの他の単位との間で換算するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="649cb-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="649cb-162">設定する換算のタイプに応じて、次のいずれかのタブを選択します:</span><span class="sxs-lookup"><span data-stu-id="649cb-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="649cb-163">**標準換算** – すべての製品の標準換算ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="649cb-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="649cb-164">**クラス内換算** – 同じ単位クラス内の単位に対する製品固有の換算ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="649cb-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="649cb-165">**クラス間換算** – 単位クラス間の単位に対する製品固有の換算ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="649cb-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="649cb-166">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="649cb-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="649cb-167">新しい換算を作成するには、ツール バーで **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="649cb-168">既存の換算を編集するには、グリッドで換算を選択してから、ツール バーで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="649cb-169">表示されるドロップダウン ダイアログ ボックスで、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="649cb-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="649cb-170">**製品** – 換算を適用する特定の製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="649cb-171">このフィールドは、クラス内およびクラス間の換算の場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="649cb-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="649cb-172">**式のレイアウト** – このフィールドを *簡易* に設定して、単一係数を持つ簡易換算を指定します。</span><span class="sxs-lookup"><span data-stu-id="649cb-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="649cb-173">フィールドを *詳細* に設定して、より複雑な方程式を設定します。</span><span class="sxs-lookup"><span data-stu-id="649cb-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="649cb-174">詳細な方程式の形式は、単位クラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="649cb-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="649cb-175">**開始単位** – このフィールドには、選択した単位が表示されます。</span><span class="sxs-lookup"><span data-stu-id="649cb-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="649cb-176">通常、値は変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="649cb-176">Usually, you should not change the value.</span></span> <span data-ttu-id="649cb-177">(値を変更する場合は、保存後に新しい換算を表示するために、選択した単位の **単位換算** ページを開く必要があります。)</span><span class="sxs-lookup"><span data-stu-id="649cb-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="649cb-178">**終了単位** – 換算する単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="649cb-179">**丸め** – 選択した単位の **小数点以下の精度** 値に基づいて、端数の丸め方法を選択します (*最も近い値*、*切り上げ*、*切り下げ*)。</span><span class="sxs-lookup"><span data-stu-id="649cb-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="649cb-180">**換算式** – ドロップダウン ダイアログ ボックスの上部にある残りのフィールドを使用して、2 つの単位間で換算する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="649cb-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="649cb-181">使用可能なフィールドは、選択した単位クラスおよび式のレイアウトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="649cb-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="649cb-182">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="649cb-182">Select **OK**.</span></span>
1. <span data-ttu-id="649cb-183">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="649cb-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="649cb-184">製品バリアントごとに単位換算を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="649cb-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="649cb-185">詳細については、[製品バリアントごとの測定単位の換算](../uom-conversion-per-product-variant.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="649cb-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
