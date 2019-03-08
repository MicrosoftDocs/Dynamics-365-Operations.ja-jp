---
title: 製品バリアントごとの測定単位の変換
description: このトピックでは、測定単位の変換を製品バリアントに設定する方法について説明します。
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "345930"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="e4c75-103">製品バリアントごとの測定単位の変換</span><span class="sxs-lookup"><span data-stu-id="e4c75-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="e4c75-104">このトピックでは、測定単位の変換を製品バリアントに設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e4c75-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="e4c75-105">これには、設定の例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e4c75-105">It includes an example of the setup.</span></span>

<span data-ttu-id="e4c75-106">この機能により、会社は同じ製品のバリアント間で異なる単位換算を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="e4c75-107">このトピックでは次の例が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-107">The following example is used in this topic.</span></span> <span data-ttu-id="e4c75-108">ある会社が S、M、L および XL のサイズの T シャツを販売しています。</span><span class="sxs-lookup"><span data-stu-id="e4c75-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="e4c75-109">T シャツは製品として定義され、また製品のバリアントとして異なるサイズが定義されています。</span><span class="sxs-lookup"><span data-stu-id="e4c75-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="e4c75-110">T シャツはボックスに梱包することができ、1 つのボックスに 5 枚の T シャツが入りますが、XL サイズは 4 枚だけ入ります。</span><span class="sxs-lookup"><span data-stu-id="e4c75-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="e4c75-111">会社は**個**単位で T シャツの異なるバリアントを追跡する必要がありますが、T シャツは**ボックス**単位で販売されています。</span><span class="sxs-lookup"><span data-stu-id="e4c75-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="e4c75-112">在庫単位と販売単位の間の変換は 1 ボックス = 5 個で、XL のバリアントの場合は 1 ボックス = 4 個になります。</span><span class="sxs-lookup"><span data-stu-id="e4c75-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="e4c75-113">セットアップ</span><span class="sxs-lookup"><span data-stu-id="e4c75-113">Setup</span></span>

<span data-ttu-id="e4c75-114">**製品情報パラメーター** ページの**測定単位変換の有効化**オプションを使用し、**すべてのプロセス**に有効化された製品、または**倉庫プロセス**にのみ有効化された製品の機能を使用してパラメーターを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="e4c75-115">バリアントごとの単位変換の製品の設定</span><span class="sxs-lookup"><span data-stu-id="e4c75-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="e4c75-116">製品バリアントは**製品サブタイプ**の製品に対してのみ作成することができます: **製品マスター**。</span><span class="sxs-lookup"><span data-stu-id="e4c75-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="e4c75-117">詳細については、[製品マスターの作成](tasks/create-product-master.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4c75-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="e4c75-118">この機能は CW プロセスに設定されている製品には有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="e4c75-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="e4c75-119">製品マスターの作成中に、**製品の詳細**ページの**測定単位の変換の有効化**オプションを使用して測定単位の変換を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e4c75-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="e4c75-120">製品マスターとリリース済製品バリアントが作成された場合、バリアントごとに単位変換を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="e4c75-121">次のページの製品または製品バリアントのコンテキスト内で単位変換ページを開くためのメニュー項目については、こちらをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e4c75-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="e4c75-122">**製品の詳細**ページ</span><span class="sxs-lookup"><span data-stu-id="e4c75-122">**Product details** page</span></span>
-   <span data-ttu-id="e4c75-123">**リリース済製品の詳細**ページ</span><span class="sxs-lookup"><span data-stu-id="e4c75-123">**Released products details** page</span></span>
-   <span data-ttu-id="e4c75-124">**リリース済製品のバリアント** ページ</span><span class="sxs-lookup"><span data-stu-id="e4c75-124">**Released product variants** page</span></span>

<span data-ttu-id="e4c75-125">製品マスターまたはリリース済製品のバリアントのコンテキストで**単位変換**ページを開く場合、製品または製品バリアントに対して単位変換を設定するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="e4c75-126">**次の変換の作成**フィールドで、**製品バリアント**または**製品**のいずれかを選択することによって行います。</span><span class="sxs-lookup"><span data-stu-id="e4c75-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="e4c75-127">製品バリアント</span><span class="sxs-lookup"><span data-stu-id="e4c75-127">Product variant</span></span>

<span data-ttu-id="e4c75-128">**製品バリアント**を選択した場合、**製品バリアント** フィールドにおいてどのバリアントに対して単位変換を設定するかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="e4c75-129">品目</span><span class="sxs-lookup"><span data-stu-id="e4c75-129">Product</span></span>

<span data-ttu-id="e4c75-130">**製品**を選択した場合、製品マスターに対して単位変換を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="e4c75-131">この単位変換は、単位変換が定義されていないすべての製品バリアントに適用されます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="e4c75-132">例</span><span class="sxs-lookup"><span data-stu-id="e4c75-132">Example</span></span>

<span data-ttu-id="e4c75-133">製品マスター **T シャツ**には、S、M、L および XL の 4 つのリリース済製品バリアントがあります。</span><span class="sxs-lookup"><span data-stu-id="e4c75-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="e4c75-134">T シャツはボックスに梱包することができ、1 つのボックスに 5 枚の T シャツが入りますが、XL サイズは 4 枚だけ入ります。</span><span class="sxs-lookup"><span data-stu-id="e4c75-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="e4c75-135">最初に、**T シャツ**のリリース済製品の詳細ページから**単位変換**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="e4c75-136">**単位変換**ページで、リリース済製品バリアント XL に対する単位変換を設定します。</span><span class="sxs-lookup"><span data-stu-id="e4c75-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="e4c75-137">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="e4c75-137">**Field**</span></span>             | <span data-ttu-id="e4c75-138">**設定**</span><span class="sxs-lookup"><span data-stu-id="e4c75-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="e4c75-139">次の変換の作成: </span><span class="sxs-lookup"><span data-stu-id="e4c75-139">Create conversion for</span></span> | <span data-ttu-id="e4c75-140">製品バリアント</span><span class="sxs-lookup"><span data-stu-id="e4c75-140">Product variant</span></span>         |
| <span data-ttu-id="e4c75-141">製品バリアント</span><span class="sxs-lookup"><span data-stu-id="e4c75-141">Product variant</span></span>       | <span data-ttu-id="e4c75-142">T シャツ : : XL : :</span><span class="sxs-lookup"><span data-stu-id="e4c75-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="e4c75-143">開始単位</span><span class="sxs-lookup"><span data-stu-id="e4c75-143">From unit</span></span>             | <span data-ttu-id="e4c75-144">ボックス</span><span class="sxs-lookup"><span data-stu-id="e4c75-144">Boxes</span></span>                   |
| <span data-ttu-id="e4c75-145">係数</span><span class="sxs-lookup"><span data-stu-id="e4c75-145">Factor</span></span>                | <span data-ttu-id="e4c75-146">4</span><span class="sxs-lookup"><span data-stu-id="e4c75-146">4</span></span>                       |
| <span data-ttu-id="e4c75-147">終了単位</span><span class="sxs-lookup"><span data-stu-id="e4c75-147">To Unit</span></span>               | <span data-ttu-id="e4c75-148">個</span><span class="sxs-lookup"><span data-stu-id="e4c75-148">Pieces</span></span>                  |

<span data-ttu-id="e4c75-149">リリース済製品バリアント S、M および L の場合、ボックスと個の間の単位変換は同じであり、これらの製品バリアントに対して製品マスター上で単位変換を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="e4c75-150">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="e4c75-150">**Field**</span></span>             | <span data-ttu-id="e4c75-151">**設定**</span><span class="sxs-lookup"><span data-stu-id="e4c75-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="e4c75-152">次の変換の作成: </span><span class="sxs-lookup"><span data-stu-id="e4c75-152">Create conversion for</span></span> | <span data-ttu-id="e4c75-153">品目</span><span class="sxs-lookup"><span data-stu-id="e4c75-153">Product</span></span>     |
| <span data-ttu-id="e4c75-154">品目</span><span class="sxs-lookup"><span data-stu-id="e4c75-154">Product</span></span>               | <span data-ttu-id="e4c75-155">T シャツ</span><span class="sxs-lookup"><span data-stu-id="e4c75-155">T-Shirt</span></span>     |
| <span data-ttu-id="e4c75-156">開始単位</span><span class="sxs-lookup"><span data-stu-id="e4c75-156">From unit</span></span>             | <span data-ttu-id="e4c75-157">ボックス</span><span class="sxs-lookup"><span data-stu-id="e4c75-157">Boxes</span></span>       |
| <span data-ttu-id="e4c75-158">係数</span><span class="sxs-lookup"><span data-stu-id="e4c75-158">Factor</span></span>                | <span data-ttu-id="e4c75-159">5</span><span class="sxs-lookup"><span data-stu-id="e4c75-159">5</span></span>           |
| <span data-ttu-id="e4c75-160">終了単位</span><span class="sxs-lookup"><span data-stu-id="e4c75-160">To Unit</span></span>               | <span data-ttu-id="e4c75-161">個</span><span class="sxs-lookup"><span data-stu-id="e4c75-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="e4c75-162">Excel を使用した単位変換の更新</span><span class="sxs-lookup"><span data-stu-id="e4c75-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="e4c75-163">製品に異なる単位変換を持つ製品バリアントが多くある場合、**単位変換**ページから Excel スプレッドシートに単位変換をエクスポートして変換を更新し、Finance and Operations に再度発行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e4c75-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="e4c75-164">Excel にエクスポートし、編集を再度 Finance and Operations に発行するオプションは、**単位変換**ページのアクション ペインの **Microsoft Office で開く**メニューから有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e4c75-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
