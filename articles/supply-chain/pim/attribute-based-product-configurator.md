---
title: 制約ベースの製品コンフィギュレーションの属性ベースの販売価格
description: このトピックでは、物理的な部品表と工順ではなく、コンポーネントと属性に基づく販売価格の販売価格モデルを作成する方法について説明します。
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: cba4b1eac33ae53e214297728c1cdf2710ebd9d9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007919"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a><span data-ttu-id="71ff1-103">制約ベースの製品コンフィギュレーションの属性ベースの販売価格</span><span class="sxs-lookup"><span data-stu-id="71ff1-103">Attribute-based sales prices for constraint-based product configuration</span></span>

<span data-ttu-id="71ff1-104">このトピックでは、物理的な部品表と工順ではなく、コンポーネントと属性に基づく販売価格の販売価格モデルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-104">This topic describes how to build sales price models with sales prices based on components and attributes rather than on the physical bill of material and the route.</span></span> <span data-ttu-id="71ff1-105">製品コンフィギュレーション モデルごとに、複数の販売価格モデルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-105">You can build several sales price models for each product configuration model.</span></span>

## <a name="set-relevant-product-information-management-parameters"></a><span data-ttu-id="71ff1-106">関連する製品情報管理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="71ff1-106">Set relevant product information management parameters</span></span>

<span data-ttu-id="71ff1-107">価格モデルの作成を開始する前に、販売価格モデルを作成するときに使用する既定の通貨を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71ff1-107">Before you start building your price models, you must define a default currency, which is used when you build your sales price models.</span></span> <span data-ttu-id="71ff1-108">すべての注文明細行または見積明細行の価格内訳を含む Microsoft Excel ファイルを添付するかどうかを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-108">You can also choose whether to attach a Microsoft Excel file with a price breakdown for all order or quotation lines.</span></span> <span data-ttu-id="71ff1-109">価格内訳により、コンフィギュレーション済みの製品に対する特定の販売価格に到達した方法について顧客と詳細情報を共有することができます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-109">The price breakdown will enable you to share details with customers about how you arrived at a specific sales price for a configured product.</span></span>

<span data-ttu-id="71ff1-110">既定の通貨を設定する方法は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="71ff1-110">To set your default currency:</span></span>

1. <span data-ttu-id="71ff1-111">**製品情報管理 \> 設定 \> 製品情報管理パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-111">Go to  **Product information management \> Setup \> Product information management parameters**.</span></span>
1. <span data-ttu-id="71ff1-112">**制約ベースの製品コンフィギュレーション モデル** のタブを開きます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-112">Open the **Constraint-Based product configuration models** tab.</span></span>
1. <span data-ttu-id="71ff1-113">**既定の通貨** ドロップダウン リストを開き、通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-113">Open the **Default currency** drop-down list and select your currency.</span></span>

    <span data-ttu-id="71ff1-114">![制約ベースの製品コンフィギュレーションの既定の通貨を設定する](media/prod-config-currency.png "制約ベースの製品コンフィギュレーションの既定の通貨を設定する")</span><span class="sxs-lookup"><span data-stu-id="71ff1-114">![Set the default currency for constraint-based product configuration](media/prod-config-currency.png "Set the default currency for constraint-based product configuration")</span></span>

1. <span data-ttu-id="71ff1-115">すべての注文明細行または見積明細行に対して価格内訳を含む Excel ファイルを関連付ける場合、**価格モデル** のセクションで **添付** を *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-115">If you'd like to attach an Excel file with a price breakdown for all order or quotation lines, then in the **Price model** section, set **Attach** to *Yes*.</span></span>

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a><span data-ttu-id="71ff1-116">販売価格モデルの作成</span><span class="sxs-lookup"><span data-stu-id="71ff1-116">Build your sales price models</span></span>

<span data-ttu-id="71ff1-117">販売価格モデルを作成する方法は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="71ff1-117">To build a sales price model:</span></span>

1. <span data-ttu-id="71ff1-118">**製品情報管理 \> 製品 \> 製品コンフィギュレーション モデル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-118">Go to  **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="71ff1-119">ターゲットにする製品構成モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-119">Select the target product configuration model.</span></span>
1. <span data-ttu-id="71ff1-120">アクション ウィンドウで、**モデル** タブを開き、**設定** グループから、**価格モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-120">On the Action pane, open the **Model** tab and, from the **Set up** group, select **Price models**.</span></span>
1. <span data-ttu-id="71ff1-121">**価格モデル** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-121">The **Price models** page opens.</span></span>
1. <span data-ttu-id="71ff1-122">価格モデルを選択するか、または新しいモデルをグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-122">Select a price model or add a new one to the grid.</span></span>
1. <span data-ttu-id="71ff1-123">**編集** を選択すると、選択したモデルの編集ページが開き、次の機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-123">Select **Edit** to open the edit page for your selected model, which provides the following features:</span></span>
    - <span data-ttu-id="71ff1-124">フォームのヘッダーに既定の通貨が表示され、価格設定に新しい通貨を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-124">The header of the form shows the default currency and lets you add new currencies for your price setup.</span></span>
    - <span data-ttu-id="71ff1-125">左のウィンドウには、製品モデルのすべてのコンポーネントとユーザー要件が表示されます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-125">The left pane shows all the components and user requirements of the product model.</span></span> <span data-ttu-id="71ff1-126">製品モデル ツリーの各ノードには、1 つの基準価格式と、任意の数の式のルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-126">Each node in the product model tree can have one base-price expression and an optional number of expression rules.</span></span> <span data-ttu-id="71ff1-127">式のルールは条件と式で構成され、各式のルールは製品の価格を管理するのに役立つ製品オプションを対象としています。</span><span class="sxs-lookup"><span data-stu-id="71ff1-127">An expression rule consists of a condition and an expression and each expression rule covers a product option that helps control the price of the product.</span></span>
    - <span data-ttu-id="71ff1-128">条件と式を作成するとき、製品モデルの計算で使用可能な演算子を同じく使用できます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-128">When you build your conditions and expressions, you have the same operators available as for calculations in a product model.</span></span> <span data-ttu-id="71ff1-129">式エディターでは、条件と式の両方もサポートされます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-129">The expression editor also supports both conditions and expressions.</span></span>
1. <span data-ttu-id="71ff1-130">左の列でノードを選択し、前の手順で説明されている機能を使用して、その価格ルールを設定します (この手順の後で示される例も参照してください)。</span><span class="sxs-lookup"><span data-stu-id="71ff1-130">Select a node in the left column and then use the features described in the previous step to establish pricing rules for it (see also the example provided after this procedure).</span></span> <span data-ttu-id="71ff1-131">必要に応じて、ノードごとにこの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-131">Repeat this step for each node as needed.</span></span>

<span data-ttu-id="71ff1-132">次の例では、顧客が選択したコンフィギュレーションに応じて、次の 5 つのうち 1 つ以上の式ルールによって変更可能で、静的な数字である 899.95 EUR という基本価格を示します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-132">The following example shows a base price of a static number of 899.95 EUR, which can be modified by one or more of the following five expression rules, depending on the configuration selected by the customer:</span></span>

- <span data-ttu-id="71ff1-133">白いキャビネット仕上げの場合、59.95 EUR 減算します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-133">For white cabinet finish, subtract 59.95 EUR.</span></span>
- <span data-ttu-id="71ff1-134">角の保護については、35.95 EUR 加算します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-134">For corner protection, add 35.95 EUR.</span></span>
- <span data-ttu-id="71ff1-135">金属のフロント グリルの場合、89.95 EUR 加算します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-135">For a metal front grill, add 89.95 EUR.</span></span>
- <span data-ttu-id="71ff1-136">ローズウッド キャビネット仕上げの場合、119.95 EUR 加算します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-136">For rosewood cabinet finish, add 119.95 EUR.</span></span>
- <span data-ttu-id="71ff1-137">スピーカの高さは単位ごとに 12.95 EUR 加算します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-137">Add 12.95 EUR for each unit of speaker height.</span></span>

<span data-ttu-id="71ff1-138">![価格モデルの例](media/prod-config-rules-example.png "価格モデルの例")</span><span class="sxs-lookup"><span data-stu-id="71ff1-138">![Example price model](media/prod-config-rules-example.png "Example price model")</span></span>

## <a name="add-support-for-multiple-currencies"></a><span data-ttu-id="71ff1-139">複数通貨のサポートを追加する</span><span class="sxs-lookup"><span data-stu-id="71ff1-139">Add support for multiple currencies</span></span>

<span data-ttu-id="71ff1-140">コンフィギュレーション可能な製品を販売する場合、価格が顧客の通貨で明示的に設定されているかどうかシステムが確認します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-140">When a configurable product is sold, the system checks whether the prices have been set explicitly in the currency of the customer.</span></span> <span data-ttu-id="71ff1-141">その場合、明示的な値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-141">If so, the explicit values are used.</span></span> <span data-ttu-id="71ff1-142">それ以外の場合は、システムは、販売会社に対して設定された通貨為替レートを使用して、既定の通貨の値を顧客の通貨に変換します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-142">If not, the system uses the currency exchange rates established for the sales company to convert the default currency value to the customer's currency.</span></span>

<span data-ttu-id="71ff1-143">追加通貨で明示的な価格を追加する方法は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="71ff1-143">To add explicit prices in an additional currency:</span></span>

1. <span data-ttu-id="71ff1-144">[販売価格モデルの作成](#build-price-model) で説明されているように、価格モデルの編集ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-144">Open the edit page for your price model, as described in [Build your sales price models](#build-price-model).</span></span>
1. <span data-ttu-id="71ff1-145">価格モデルのヘッダーで **追加** ボタンを選択し、使用可能な通貨を一覧表示する **通貨** ドロップダウン ダイアログボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-145">Select the **Add** button in the header of the price model to open the **Currencies** drop-down dialog box, which lists the available currencies.</span></span>
1. <span data-ttu-id="71ff1-146">**通貨** ドロップダウン ダイアログボックスで追加する通貨を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-146">Select the currency you want to add in the **Currencies** drop-down dialog box and then select **OK**.</span></span>
1. <span data-ttu-id="71ff1-147">**現在の通貨** ドロップダウン リストに、追加したばかりの通貨に加え、以前に追加された他の通貨すべてが含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="71ff1-147">The **Current currency** drop-down list now includes the currency that you just added, plus any other currencies that may have been added previously.</span></span> <span data-ttu-id="71ff1-148">新しい通貨を選択し、**式ルール** セクションのグリッドに 2 つの式フィールドが含まれていることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="71ff1-148">Select your new currency and notice that the grid in the **Expression rules** section now includes two expression fields:</span></span>
    - <span data-ttu-id="71ff1-149">**式** - **現在の通貨** に対して現在選択されている通貨を使用して価格を検索する式 (または定数値) を示しています。</span><span class="sxs-lookup"><span data-stu-id="71ff1-149">**Expression** - Shows the expression (or constant value) for finding the price using the currency currently selected for **Current currency**.</span></span>
    - <span data-ttu-id="71ff1-150">**既定の式** - 現在、(**現在の通貨** フィールドに表示されている) 既定値を使用して価格を検索する式 (または定数値) を示しています。</span><span class="sxs-lookup"><span data-stu-id="71ff1-150">**Default expressions** - Shows the expression (or constant value) for finding the price using the default currently (shown in the **Default currency** field).</span></span>

    > [!NOTE]
    > <span data-ttu-id="71ff1-151">式ルールに対する **条件** フィールドは、既定の通貨によって「所有」されており、他の通貨に対する条件を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="71ff1-151">The **Condition** field for the expression rules is "owned" by the default currency, which means that you can't modify the condition for other currencies.</span></span> <span data-ttu-id="71ff1-152">また、既定の通貨以外の通貨が **現在の通貨** として選択されている場合、新しい式のルールを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="71ff1-152">You also can't add new expression rules while a currency other than the default currency is selected as the **Current currency**.</span></span>
1. <span data-ttu-id="71ff1-153">現在の通貨に応じて、**式** 列の値を編集します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-153">Edit values in the **Expression** column as needed for the current currency.</span></span>

<span data-ttu-id="71ff1-154">次の例では、_EUR_ が既定の通貨であり、_USD_ は追加の通貨として追加されています。</span><span class="sxs-lookup"><span data-stu-id="71ff1-154">In the example below, _EUR_ is the default currency, and _USD_ has been added as an additional currency.</span></span>

<span data-ttu-id="71ff1-155">![複数の通貨を使用するモデルの例](media/prod-config-rules-currency-example.png "複数の通貨を使用するモデルの例")</span><span class="sxs-lookup"><span data-stu-id="71ff1-155">![Example of a model with multiple currencies](media/prod-config-rules-currency-example.png "Example of a model with multiple currencies")</span></span>

> [!NOTE]
> <span data-ttu-id="71ff1-156">既定以外の通貨に対して一意となる式ルールを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="71ff1-156">You can't add expression rules that are unique for a non-default currency.</span></span> <span data-ttu-id="71ff1-157">既定の通貨以外の通貨にのみ関連する式ルールを作成するには、既定の通貨の価格式を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-157">To create expression rules that would be relevant only for a currency other than the default currency, set the price expression for the default currency to zero.</span></span> <span data-ttu-id="71ff1-158">その後、既定以外の通貨に適切な式を設定します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-158">Then set the appropriate expression for the non-default currency.</span></span>

## <a name="test-your-price-model"></a><span data-ttu-id="71ff1-159">価格モデルのテスト</span><span class="sxs-lookup"><span data-stu-id="71ff1-159">Test your price model</span></span>

<span data-ttu-id="71ff1-160">コンフィギュレーション セッションで販売価格が機能する方法についてテストするには、[販売価格モデルの作成](#build-price-model) で説明されているように、価格モデルの編集ページを開き、アクション ウィンドウの **テスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-160">To test how the sales prices work in a configuration session, open the edit page for your price model, as described in [Build your sales price models](#build-price-model) and then select  **Test** on the Action Pane.</span></span> <span data-ttu-id="71ff1-161">**製品モデルのテスト** ダイアログ ボックスが開き、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-161">The **Test product model** dialog box opens, where you can do the following:</span></span>

- <span data-ttu-id="71ff1-162">ここで提供されるコンフィギュレーション設定を使用して製品オプションを選択し、**価格および出荷日** について表示されている値への影響を確認します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-162">Use the configuration settings offered here to select product options and then see how they affect the value shown for **Price and ship date**.</span></span>
- <span data-ttu-id="71ff1-163">**価格内訳の表示** を選択し、価格の計算方法に関する完全な詳細情報を示す Excel ドキュメントをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="71ff1-163">Select **View price breakdown** to download an Excel document that shows full details about how the price was calculated.</span></span>

<span data-ttu-id="71ff1-164">![製品モデルのテスト](media/prod-config-test.png "製品モデルのテスト")</span><span class="sxs-lookup"><span data-stu-id="71ff1-164">![Test your product model](media/prod-config-test.png "Test your product model")</span></span>

<span data-ttu-id="71ff1-165">ダウンロードされたスプレッドシートには、絶対値と利益率の両方が有効な価格要素ごとに割合で表示されます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-165">The downloaded spreadsheet shows both the absolute value and the contribution as a percentage for each active price element.</span></span> <span data-ttu-id="71ff1-166">**製品情報管理パラメーター** ページで **添付** 価格モデル オプションを設定した場合、この Excel シートが注文明細行または見積明細行に添付されます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-166">If you have set the **Attach** price model option on the **Product information management parameters** page, this Excel sheet gets attached to the order or quotation line.</span></span>

<span data-ttu-id="71ff1-167">![価格内訳を示す Excel スプレッドシート](media/prod-config-excel-example.png "価格内訳を示す Excel スプレッドシート")</span><span class="sxs-lookup"><span data-stu-id="71ff1-167">![Excel spreadsheet showing price breakdown](media/prod-config-excel-example.png "Excel spreadsheet showing price breakdown")</span></span>

## <a name="set-up-selection-criteria-for-price-models"></a><span data-ttu-id="71ff1-168">価格モデルの選択基準を設定する</span><span class="sxs-lookup"><span data-stu-id="71ff1-168">Set up selection criteria for price models</span></span>

<span data-ttu-id="71ff1-169">価格モデルが設定されている場合、少なくとも 1 つの選択基準を設定し、見積または注文をコンフィギュレーションするときに価格モデルが選択されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="71ff1-169">When your price models are in place, you must establish at least one selection criterion to pick up the price model when you configure to quote or to order.</span></span> <span data-ttu-id="71ff1-170">これを行うには、1 つ以上のクエリを設定します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-170">You'll do this by setting up one or more queries.</span></span> <span data-ttu-id="71ff1-171">販売価格モデルが一致した組み合わせについて、クエリによって、特定の顧客、地域、期間、およびその他の基準に対する販売価格を対象とした優れた柔軟性が提供されます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-171">In a combination with matching sales price models, the queries provide great flexibility in targeting sales prices for particular customers, regions, periods, and other criteria.</span></span>

<span data-ttu-id="71ff1-172">価格モデルの選択基準を設定する方法は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="71ff1-172">To set up selection criteria for price models:</span></span>

1. <span data-ttu-id="71ff1-173">**製品情報管理 \> 製品 \> 製品コンフィギュレーション モデル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-173">Go to  **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="71ff1-174">ターゲットにする製品構成モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-174">Select the target product configuration model.</span></span>
1. <span data-ttu-id="71ff1-175">アクション ウィンドウで、**モデル** タブを開き、**設定** グループから、**価格モデル基準** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-175">On the Action pane, open the **Model** tab and, from the **Set up** group, select **Price model criteria**.</span></span> <span data-ttu-id="71ff1-176">**価格モデル基準** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-176">The **Price model criteria** page opens.</span></span>
1. <span data-ttu-id="71ff1-177">必要なクエリ行がまだ存在しない場合、アクション ウィンドウの **新規** を選択して新しい行をグリッドに追加し、次の設定をします。</span><span class="sxs-lookup"><span data-stu-id="71ff1-177">If the query row you need doesn't exist yet, select **New** on the Action Pane to add a new row to the grid and make the following settings for it:</span></span>
    - <span data-ttu-id="71ff1-178">**名前** - この行の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-178">**Name** - Enter a name for this row.</span></span>
    - <span data-ttu-id="71ff1-179">**説明** - クエリとその目的を簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-179">**Description** - Briefly describe the query and what it is for.</span></span>
    - <span data-ttu-id="71ff1-180">**価格モデル** - トリガー時にクエリが適用される [価格モデル](#build-price-model) を選択します (現在のコンフィギュレーション モデルから)。</span><span class="sxs-lookup"><span data-stu-id="71ff1-180">**Price model** - Select a [price model](#build-price-model) (from the current configuration model) that the query will apply when triggered.</span></span>
    - <span data-ttu-id="71ff1-181">**注文タイプ** - クエリを適用する注文のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-181">**Order type** - Select the type of order where the query will apply.</span></span>
    - <span data-ttu-id="71ff1-182">**発効日** - クエリを適用する最初の日を指定します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-182">**Valid from** - Specify the first day when the query will apply.</span></span>
    - <span data-ttu-id="71ff1-183">**有効期限** - クエリを適用する最後の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-183">**Expire by** - Specify the last date when the query will apply.</span></span>

    <span data-ttu-id="71ff1-184">![価格モデル基準](media/prod-config-price-model-criteria.png "価格モデル基準")</span><span class="sxs-lookup"><span data-stu-id="71ff1-184">![Price model criteria](media/prod-config-price-model-criteria.png "Price model criteria")</span></span>

1. <span data-ttu-id="71ff1-185">定義するクエリの行を選択し、**アクション ウィンドウ** で **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-185">Select the row for the query you want to define and then select **Edit** on the **Action Pane**.</span></span> <span data-ttu-id="71ff1-186">クエリ デザイナー ダイアログボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-186">The query designer dialog box opens.</span></span> <span data-ttu-id="71ff1-187">Supply Chain Management のクエリ デザイナーと同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-187">It works like most query designers in Supply Chain Management.</span></span> <span data-ttu-id="71ff1-188">これを使用して、選択した行の価格モデルを適用する条件を定義します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-188">Use it to define the conditions under which the price model for the row you selected should be applied.</span></span>

1. <span data-ttu-id="71ff1-189">必要なクエリごとに手順 4-5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-189">Repeat steps 4-5 for each query you require.</span></span>
    > [!TIP]
    > <span data-ttu-id="71ff1-190">追加する必要がある行に似ている既存の行をコピーすることによって、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-190">You can save time by copying an existing row that is already similar to a new one that you need to add.</span></span> <span data-ttu-id="71ff1-191">これを行うには、対象となる行を選択し、アクション ウィンドウの **複製** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-191">To do this, select a target row and then select **Duplicate** on the Action Pane.</span></span>

1. <span data-ttu-id="71ff1-192">基準の設定が完了したら、**価格モデルの基準** リストで適切な順序に並び替えます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-192">When you have finished setting up your criteria, arrange them into the proper order in the **Price model criteria** list.</span></span> <span data-ttu-id="71ff1-193">行の位置変更をするには、行を選択し、アクション ウィンドウの **アップ** または **ダウン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-193">To reposition a row, select the row and then select **Up** or **Down** on the Action Pane.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="71ff1-194">コンフィギュレーション時に、システムはリストの先頭から検索を開始し、見積または注文明細行のデータに一致する最初のクエリを使用します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-194">At configuration time, the system starts searching from the top of the list and uses the first query that matches the data on the quote or the order line.</span></span> <span data-ttu-id="71ff1-195">したがって、最も特定的なクエリを先頭に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71ff1-195">Therefore, you must put your most specific queries on top.</span></span> <span data-ttu-id="71ff1-196">一般なクエリをリストの先頭に配置した場合、正確な顧客を対象にしているクエリ、またはコンフィギュレーションに応じたクエリが一覧の下の方に存在する可能性がありますが、これが使用されます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-196">If you place a general query at the top of the list, this is the one that will be used even though there might be a query further down the list that targets the exact customer or prospect of the configuration.</span></span>

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a><span data-ttu-id="71ff1-197">属性ベースの販売価格を製品モデルのバージョンに設定する</span><span class="sxs-lookup"><span data-stu-id="71ff1-197">Set attribute-based sales prices for the product model version</span></span>

<span data-ttu-id="71ff1-198">最後の手順は、製品モデルのバージョンに属性ベースの販売価格を指定することです。</span><span class="sxs-lookup"><span data-stu-id="71ff1-198">The final step is to specify attribute-based sales prices for the product model version.</span></span> <span data-ttu-id="71ff1-199">これを行うには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-199">To do this:</span></span>

1. <span data-ttu-id="71ff1-200">**製品情報管理 \> 製品 \> 製品コンフィギュレーション モデル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-200">Go to  **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="71ff1-201">ターゲットにする製品構成モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-201">Select the target product configuration model.</span></span>
1. <span data-ttu-id="71ff1-202">アクション ウィンドウで、**モデル** タブを開き、**製品モデルの詳細** グループから、**バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-202">On the Action Pane, open the **Model** tab and, from the **Product model details** group, select **Versions**.</span></span>
1. <span data-ttu-id="71ff1-203">**バージョン** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="71ff1-203">The **Versions** page opens.</span></span> <span data-ttu-id="71ff1-204">**価格決定方法** が **属性ベース** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="71ff1-204">Make sure the **Pricing method** is set to **Attribute based**.</span></span>
    <span data-ttu-id="71ff1-205">![価格決定方法を属性ベースに設定する](media/prod-config-versions.png "価格決定方法を属性ベースに設定する")</span><span class="sxs-lookup"><span data-stu-id="71ff1-205">![Set the pricing method to attribute based](media/prod-config-versions.png "Set the pricing method to attribute based")</span></span>
