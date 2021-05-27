---
title: 事前定義された製品バリアントの作成
description: この手順では、製品分析コードの組み合わせを使用する製品マスターの製品バリアントの作成を説明します。
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f78441445baecba279f96eb3935d9ebbb4ff03f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021911"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="e074c-103">事前定義された製品バリアント</span><span class="sxs-lookup"><span data-stu-id="e074c-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="e074c-104">シナリオ例: 事前定義された製品バリアントの作成</span><span class="sxs-lookup"><span data-stu-id="e074c-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="e074c-105">このシナリオ例では、製品分析コードの組み合わせを使用する製品マスターの製品バリアントを作成ずる方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e074c-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e074c-106">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="e074c-106">Make demo data available</span></span>

<span data-ttu-id="e074c-107">ここで推奨されている値を使用してこのシナリオを実行するには、デモ データがインストールされている必要があり、法人として *USMF* を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e074c-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="e074c-108">ステップ 1: 製品マスターの作成</span><span class="sxs-lookup"><span data-stu-id="e074c-108">Step 1: Create a product master</span></span>

<span data-ttu-id="e074c-109">製品マスターを作成するには:</span><span class="sxs-lookup"><span data-stu-id="e074c-109">To create a product master:</span></span>

1. <span data-ttu-id="e074c-110">**製品情報管理 > 製品 > 製品マスター** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="e074c-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-111">Select **New**.</span></span>
1. <span data-ttu-id="e074c-112">**製品番号** フィールドにまだ番号が表示できない場合は、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="e074c-113">これは、フィールドに番号順序が設定されていない場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="e074c-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="e074c-114">**製品名** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="e074c-115">**製品分析コード グループ** フィールドで、製品分析コード グループ *SizeCol* (サイズおよび色) を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="e074c-116">**OK** を選択して新しい製品マスターを作成し開きます。</span><span class="sxs-lookup"><span data-stu-id="e074c-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="e074c-117">ステップ 2: 製品分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="e074c-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="e074c-118">この例では、手動で製品分析コードを入力する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e074c-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="e074c-119">使用する製品分析コードの値を含むサイズ、色、またはスタイル グループを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="e074c-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="e074c-120">製品分析コードを追加するには:</span><span class="sxs-lookup"><span data-stu-id="e074c-120">To add product dimensions:</span></span>

1. <span data-ttu-id="e074c-121">新しい製品マスターを開いたまま、アクション ペインで **製品分析コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="e074c-122">**サイズ** タブを開き、ツールバーの **新規** を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="e074c-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="e074c-123">新しい行に対して、次の設定を行います。</span><span class="sxs-lookup"><span data-stu-id="e074c-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="e074c-124">**サイズ:** サイズの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="e074c-125">**名前:** サイズの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="e074c-126">ツールバーで **新規** を選択し、新しい **サイズ** および **名前** を使用して、グリッドに 2 番目のサイズを追加します。</span><span class="sxs-lookup"><span data-stu-id="e074c-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="e074c-127">**色** タブを開き、ツールバーの **新規** を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="e074c-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="e074c-128">新しい行に対して、次の設定を行います。</span><span class="sxs-lookup"><span data-stu-id="e074c-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="e074c-129">**色:** 色の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="e074c-130">**名前:** 色の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="e074c-131">ツールバーで **新規** を選択し、新しい **色** および **名前** を使用して、グリッドに 2 番目の色を追加します。</span><span class="sxs-lookup"><span data-stu-id="e074c-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="e074c-132">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-132">Select **Save**.</span></span>
1. <span data-ttu-id="e074c-133">ページを閉じて、新しい製品マスターに戻ります。</span><span class="sxs-lookup"><span data-stu-id="e074c-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="e074c-134">ステップ 3: 製品バリアントの生成</span><span class="sxs-lookup"><span data-stu-id="e074c-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="e074c-135">このセクションでは、*バリアント提案ページの改善* 機能が有効になっていない場合に製品バリアントを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e074c-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="e074c-136">この機能を利用できる場合に製品バリアントを生成する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e074c-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="e074c-137">製品バリアントを生成するには:</span><span class="sxs-lookup"><span data-stu-id="e074c-137">To generate product variants:</span></span>

1. <span data-ttu-id="e074c-138">新しい製品マスターを開いたまま、アクション ペインで **製品バリアント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="e074c-139">アクション ペインで、**バリアントの提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="e074c-140">システムは、製品に対して定義されたサイズと色のすべての可能な組み合わせを含む一覧を生成します。</span><span class="sxs-lookup"><span data-stu-id="e074c-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="e074c-141">ツールバーで、**すべて選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="e074c-142">この例では、すべての可能なバリアントを選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="e074c-143">可能な製品分析コードの組み合わせのサブセットのみを使用する場合は、必要に応じて必要なチェック ボックスのみをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e074c-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="e074c-144">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-144">Select **Create**.</span></span>
1. <span data-ttu-id="e074c-145">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="e074c-146">バリアント提案の改善</span><span class="sxs-lookup"><span data-stu-id="e074c-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="e074c-147">*バリアント提案ページの改善* 機能を使用すると、**バリアント提案** ページが改善され、製品分析コードの組み合わせが多い会社のパフォーマンスと操作性問題に対処できます。</span><span class="sxs-lookup"><span data-stu-id="e074c-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="e074c-148">バリアント提案を生成する製品分析コード値を選択するプロセスの強化により、関連する製品バリアントの識別とリリースをより迅速かつ簡単に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e074c-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="e074c-149">この機能により、次の改善が追加されました。</span><span class="sxs-lookup"><span data-stu-id="e074c-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="e074c-150">**バリアント提案の繰延生成:** 最初に開いたときに、**バリアント提案** ページに提案が表示されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="e074c-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="e074c-151">代わりに、必要な値を明示的に選択してから、**提案** ボタンを選択して組み合わせを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e074c-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="e074c-152">これにより、プロセスが可視化され対話型になります。</span><span class="sxs-lookup"><span data-stu-id="e074c-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="e074c-153">**分析コード値の選択:** 多くの分析コード値がある場合は、通常、そのうちのいくつかを含むバリアント提案を生成します (新しい色やスタイルのセットを導入する場合など)。</span><span class="sxs-lookup"><span data-stu-id="e074c-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="e074c-154">改善されたデザインで、製品バリアント提案を生成する分析コード値を選択できます。</span><span class="sxs-lookup"><span data-stu-id="e074c-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="e074c-155">これにより、提案されるバリアントの関連性が大幅に増加し、システム パフォーマンスとユーザーの生産性の両方が向上します。</span><span class="sxs-lookup"><span data-stu-id="e074c-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="e074c-156">バリアント提案ページの改善機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="e074c-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="e074c-157">*バリアント提案ページの改善* 機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e074c-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="e074c-158">管理者は、[機能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e074c-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e074c-159">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="e074c-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e074c-160">**モジュール :** *製品情報管理*</span><span class="sxs-lookup"><span data-stu-id="e074c-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="e074c-161">**機能名:** *バリアント提案ページの改善*</span><span class="sxs-lookup"><span data-stu-id="e074c-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="e074c-162">改善されたバリアント提案に関する作業</span><span class="sxs-lookup"><span data-stu-id="e074c-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="e074c-163">*バリアント提案ページの改善* 機能が有効になっている場合に製品バリアントを生成するには:</span><span class="sxs-lookup"><span data-stu-id="e074c-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="e074c-164">前のセクションで説明したように、製品マスターを開くか作成し、必要な製品分析コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="e074c-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="e074c-165">製品マスターを開いたまま、アクション ペインで **製品バリアント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="e074c-166">アクション ペインで、**バリアントの提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="e074c-167">各分析コードに使用する値を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="e074c-168">上部のツールバーで、**提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="e074c-169">システムは、選択したサイズと色のすべての可能な組み合わせを含む一覧を生成します。</span><span class="sxs-lookup"><span data-stu-id="e074c-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="e074c-170">**提案されるバリアント** クイック タブで、使用する製品分析コードの組み合わせごとにチェック ボックスをオンにするか、ツールバーの **すべて選択** を選択してすべてのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="e074c-171">**作成** を選択して、バリアントを現在の製品マスターに追加します。</span><span class="sxs-lookup"><span data-stu-id="e074c-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
