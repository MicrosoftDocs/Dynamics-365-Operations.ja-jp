---
title: 製品バリアントごとの測定単位の変換
description: このトピックでは、測定単位の変換を製品バリアントに設定する方法について説明します。 これには、設定の例が含まれています。
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 71d35d47a703f0931ba3b4ab5df21c7199c7ea5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432251"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="226ed-104">製品バリアントごとの測定単位の変換</span><span class="sxs-lookup"><span data-stu-id="226ed-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="226ed-105">このトピックでは、測定単位の変換を様々な製品バリアントに設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="226ed-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="226ed-106">管理する必要がある複数の製品を作成する代わりに、製品のバリエーションを使用して1つの製品のバリエーションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="226ed-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="226ed-107">たとえば、製品バリアントは、特定のサイズと色の T シャツである場合があります。</span><span class="sxs-lookup"><span data-stu-id="226ed-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="226ed-108">これまでは、製品マスターに対してのみ単位換算を設定できました。</span><span class="sxs-lookup"><span data-stu-id="226ed-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="226ed-109">そのため、すべての製品バリアントには、同じ単位換算規則が適用されていました。</span><span class="sxs-lookup"><span data-stu-id="226ed-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="226ed-110">ただし、*製品バリアントの測定単位換算* 機能が有効になっている場合で、T シャツが箱単位で販売されている場合、箱に詰められる T シャツの枚数が T シャツのサイズによって異なる場合、異なるシャツのサイズと梱包に使用する箱の間に単位変換を設定することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="226ed-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="226ed-111">システムで機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="226ed-111">Turn on the feature in your system</span></span>

<span data-ttu-id="226ed-112">この機能がシステムに表示されない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)に移動し、*製品バリアントの単位換算* 機能を有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="226ed-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="226ed-113">バリアントごとの単位変換の製品の設定</span><span class="sxs-lookup"><span data-stu-id="226ed-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="226ed-114">製品バリアントは、製品マスターである製品に対してのみ作成することができます。</span><span class="sxs-lookup"><span data-stu-id="226ed-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="226ed-115">詳細については、[製品マスターの作成](tasks/create-product-master.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="226ed-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="226ed-116">*製品バリアントの単位換算* 機能は、キャッチ ウェイト プロセスに設定されている製品には使用できません。</span><span class="sxs-lookup"><span data-stu-id="226ed-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="226ed-117">バリアントごとの単位変換に対応する製品マスターを構成するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="226ed-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="226ed-118">**製品情報管理 \> 製品 \> 製品マスター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="226ed-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="226ed-119">製品マスターを作成する、または起動して、 **製品の詳細ページ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="226ed-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="226ed-120">**測定単位の変換を有効にする** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="226ed-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="226ed-121">アクション ウィンドウ、**製品** タブの、**設定** グループで、**単位換算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="226ed-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="226ed-122">**単位換算** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="226ed-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="226ed-123">次のいずれかのタブを選択します:</span><span class="sxs-lookup"><span data-stu-id="226ed-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="226ed-124">**クラス内変換** : このタブを選択すると、同じユニット クラスに属するユニット間での変換が可能になります。</span><span class="sxs-lookup"><span data-stu-id="226ed-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="226ed-125">**クラス間変換** : このタブを選択すると、異なるユニットクラスに属するユニット間での変換が可能になります。</span><span class="sxs-lookup"><span data-stu-id="226ed-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="226ed-126">**新規** を選択して新しい単位換算を追加します。</span><span class="sxs-lookup"><span data-stu-id="226ed-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="226ed-127">次のいずれかの値に **変換の作成** フィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="226ed-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="226ed-128">**製品** – この値を選択すると、商品マスタに単位変換を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="226ed-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="226ed-129">この単位換算は、単位換算が定義されていないすべての製品バリアントの代替として使用されます。</span><span class="sxs-lookup"><span data-stu-id="226ed-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="226ed-130">**製品バリアント** – この値を選択すると、特定の製品バリアントに対して単位変換を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="226ed-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="226ed-131">バリアントを選択するには、**製品バリアント** フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="226ed-131">Use the **Product variant** field to select the variant.</span></span>

    ![![新たな単位換算を追加する](media/uom-new-conversion.png "新たな単位換算を追加する")](media/uom-new-conversion.png "Adding a new unit conversion")

1. <span data-ttu-id="226ed-133">単位換算の設定に用意されているその他のフィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="226ed-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="226ed-134">**OK** を選択して、新しい単位換算を保存します。</span><span class="sxs-lookup"><span data-stu-id="226ed-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="226ed-135">**単位換算** ページは、以下のいずれかのページから、製品または製品バリアントの単位変換ページを開くことができます:</span><span class="sxs-lookup"><span data-stu-id="226ed-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="226ed-136">製品の詳細</span><span class="sxs-lookup"><span data-stu-id="226ed-136">Product details</span></span>
> - <span data-ttu-id="226ed-137">リリース済製品の詳細</span><span class="sxs-lookup"><span data-stu-id="226ed-137">Released products details</span></span>
> - <span data-ttu-id="226ed-138">リリース済製品バリアント</span><span class="sxs-lookup"><span data-stu-id="226ed-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="226ed-139">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="226ed-139">Example scenario</span></span>

<span data-ttu-id="226ed-140">このシナリオでは、ある会社が T シャツを S、M、L、XL サイズで販売しています。</span><span class="sxs-lookup"><span data-stu-id="226ed-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="226ed-141">T シャツは製品として定義されており、異なるサイズはその製品のバリアントとして定義されています。</span><span class="sxs-lookup"><span data-stu-id="226ed-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="226ed-142">シャツは箱に梱包されます。</span><span class="sxs-lookup"><span data-stu-id="226ed-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="226ed-143">サイズが S、M、L の場合、各ボックスには 5 つのシャツが入ります。</span><span class="sxs-lookup"><span data-stu-id="226ed-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="226ed-144">ただし、XL サイズの場合は、1 箱に 4 枚までしかシャツが入りません。</span><span class="sxs-lookup"><span data-stu-id="226ed-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="226ed-145">会社は *個* 単位で T シャツの異なるバリアントを追跡したいと考えていますが、T シャツは *箱* 単位で販売されています。</span><span class="sxs-lookup"><span data-stu-id="226ed-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="226ed-146">サイズが S、M、L の場合、在庫単位と販売単位の換算は1箱＝5個となります。</span><span class="sxs-lookup"><span data-stu-id="226ed-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="226ed-147">XL サイズの場合は、換算は1箱＝4個となります。</span><span class="sxs-lookup"><span data-stu-id="226ed-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="226ed-148">**T シャツ** 製品の **リリース済商品の詳細** ページから、**単位換算** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="226ed-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="226ed-149">**単位変換** ページで、**XL** でリリースされた製品バリアントに対して、以下のようなユニット変換を設定します。</span><span class="sxs-lookup"><span data-stu-id="226ed-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="226ed-150">フィールド</span><span class="sxs-lookup"><span data-stu-id="226ed-150">Field</span></span>                 | <span data-ttu-id="226ed-151">設定</span><span class="sxs-lookup"><span data-stu-id="226ed-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="226ed-152">次の変換の作成: </span><span class="sxs-lookup"><span data-stu-id="226ed-152">Create conversion for</span></span> | <span data-ttu-id="226ed-153">製品バリアント</span><span class="sxs-lookup"><span data-stu-id="226ed-153">Product variant</span></span>         |
    | <span data-ttu-id="226ed-154">製品バリアント</span><span class="sxs-lookup"><span data-stu-id="226ed-154">Product variant</span></span>       | <span data-ttu-id="226ed-155">T シャツ : : XL : :</span><span class="sxs-lookup"><span data-stu-id="226ed-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="226ed-156">開始単位</span><span class="sxs-lookup"><span data-stu-id="226ed-156">From unit</span></span>             | <span data-ttu-id="226ed-157">ボックス</span><span class="sxs-lookup"><span data-stu-id="226ed-157">Boxes</span></span>                   |
    | <span data-ttu-id="226ed-158">係数</span><span class="sxs-lookup"><span data-stu-id="226ed-158">Factor</span></span>                | <span data-ttu-id="226ed-159">4</span><span class="sxs-lookup"><span data-stu-id="226ed-159">4</span></span>                       |
    | <span data-ttu-id="226ed-160">終了単位</span><span class="sxs-lookup"><span data-stu-id="226ed-160">To Unit</span></span>               | <span data-ttu-id="226ed-161">個</span><span class="sxs-lookup"><span data-stu-id="226ed-161">Pieces</span></span>                  |

1. <span data-ttu-id="226ed-162">**S**、**M** 、**L** の製品バリアントはすべて、*箱* 単位と *個* 単位の間の単位変換が同じであるため、製品マスター上で以下の単位変換を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="226ed-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="226ed-163">フィールド</span><span class="sxs-lookup"><span data-stu-id="226ed-163">Field</span></span>                 | <span data-ttu-id="226ed-164">設定</span><span class="sxs-lookup"><span data-stu-id="226ed-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="226ed-165">次の変換の作成: </span><span class="sxs-lookup"><span data-stu-id="226ed-165">Create conversion for</span></span> | <span data-ttu-id="226ed-166">品目</span><span class="sxs-lookup"><span data-stu-id="226ed-166">Product</span></span> |
    | <span data-ttu-id="226ed-167">品目</span><span class="sxs-lookup"><span data-stu-id="226ed-167">Product</span></span>               | <span data-ttu-id="226ed-168">T シャツ</span><span class="sxs-lookup"><span data-stu-id="226ed-168">T-Shirt</span></span> |
    | <span data-ttu-id="226ed-169">開始単位</span><span class="sxs-lookup"><span data-stu-id="226ed-169">From unit</span></span>             | <span data-ttu-id="226ed-170">ボックス</span><span class="sxs-lookup"><span data-stu-id="226ed-170">Boxes</span></span>   |
    | <span data-ttu-id="226ed-171">係数</span><span class="sxs-lookup"><span data-stu-id="226ed-171">Factor</span></span>                | <span data-ttu-id="226ed-172">5</span><span class="sxs-lookup"><span data-stu-id="226ed-172">5</span></span>       |
    | <span data-ttu-id="226ed-173">終了単位</span><span class="sxs-lookup"><span data-stu-id="226ed-173">To Unit</span></span>               | <span data-ttu-id="226ed-174">個</span><span class="sxs-lookup"><span data-stu-id="226ed-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="226ed-175">Excel を使用した単位変換の更新</span><span class="sxs-lookup"><span data-stu-id="226ed-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="226ed-176">製品に、単位換算が異なる多数の製品バリアントがある場合は、単位換算を Microsoft Excel ブックにエクスポートし、それらを更新して、Dynamics 365 Supply Chain Management で再度発行することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="226ed-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="226ed-177">単位換算を Excel にエクスポートするには、**単位換算** ページのアクション ウィンドウで、 **Microsoft Office で開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="226ed-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="226ed-178">追加リソース</span><span class="sxs-lookup"><span data-stu-id="226ed-178">Additional resources</span></span>

[<span data-ttu-id="226ed-179">測定単位の管理</span><span class="sxs-lookup"><span data-stu-id="226ed-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)
