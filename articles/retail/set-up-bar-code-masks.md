---
title: "バーコード マスクの設定"
description: "このトピックでは、バーコード マスク文字、バーコード マスクの設定方法、バーコードにバーコード マスクを割り当てる方法について説明します。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e61524feab1b06f4a863a140b883bf8fe49af1e2
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-bar-code-masks"></a><span data-ttu-id="63f8b-103">バーコード マスクの設定</span><span class="sxs-lookup"><span data-stu-id="63f8b-103">Set up bar code masks</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="63f8b-104">このトピックでは、バーコード マスク文字、バーコード マスクの設定方法、バーコードにバーコード マスクを割り当てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-104">This topic describes how to set up bar code mask characters, bar code masks, and how to assign bar code masks to bar codes.</span></span>

<a name="set-up-bar-code-mask-characters"></a><span data-ttu-id="63f8b-105">バーコード マスク文字の設定</span><span class="sxs-lookup"><span data-stu-id="63f8b-105">Set up bar code mask characters</span></span>
-------------------------------

<span data-ttu-id="63f8b-106">バーコード マスクは、バーコードを作成し、販売時点管理 (POS) にスキャンするバーコードをすばやく識別するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="63f8b-106">Bar code masks are used to create bar codes and to quickly identify bar codes that are scanned into the point of sale (POS).</span></span> <span data-ttu-id="63f8b-107">マスクは作成するバーコードのフォーマットを示すプレースホルダとして機能する文字で構成されます。</span><span class="sxs-lookup"><span data-stu-id="63f8b-107">Masks are comprised of characters which act as placeholders that indicate the format for the bar codes that will be created.</span></span> <span data-ttu-id="63f8b-108">バーコード マスクをコンフィギュレーションするには、バーコード マスク文字を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f8b-108">To configure a bar code mask, you need to set up bar code mask characters.</span></span> <span data-ttu-id="63f8b-109">[**小売**] &gt; [**在庫管理**] &gt; [**バーコードとラベル**] &gt; [**マスク文字**] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-109">Go to **Retail** &gt; **Inventory management** &gt; **Barcodes and labels** &gt; **Mask characters**.</span></span> <span data-ttu-id="63f8b-110">[**新規**] をクリックして、バーコード マスク文字を作成します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-110">Click **New** to create bar code mask characters.</span></span> <span data-ttu-id="63f8b-111">マスク文字は、次のバーコード データを表示するように作成できます。</span><span class="sxs-lookup"><span data-stu-id="63f8b-111">Mask characters can be created to indicate the following bar code data.</span></span>

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63f8b-112">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="63f8b-112">**Field**</span></span>            | <span data-ttu-id="63f8b-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="63f8b-113">**Description**</span></span>                                                                                                 |
| <span data-ttu-id="63f8b-114">**品目**</span><span class="sxs-lookup"><span data-stu-id="63f8b-114">**Product**</span></span>          | <span data-ttu-id="63f8b-115">製品 ID のプレースホルダー。</span><span class="sxs-lookup"><span data-stu-id="63f8b-115">Placeholder for product ID.</span></span>                                                                                     |
| <span data-ttu-id="63f8b-116">**任意の数**</span><span class="sxs-lookup"><span data-stu-id="63f8b-116">**Any number**</span></span>       | <span data-ttu-id="63f8b-117">バーコードにハードコーディングされる数を指定するのに使用します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-117">Used to specify a number that will be hard coded in bar codes.</span></span>                                                  |
| <span data-ttu-id="63f8b-118">**チェック ディジット**</span><span class="sxs-lookup"><span data-stu-id="63f8b-118">**Check digit**</span></span>      | <span data-ttu-id="63f8b-119">バーコード マスクのバーコード形式が、バーコードの妥当性を確認するのにチェック ディジットを使用することを示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-119">Indicates that the bar code format in a bar code mask uses a check digit to confirm the validity of a bar code.</span></span> |
| <span data-ttu-id="63f8b-120">**サイズ ディジット**</span><span class="sxs-lookup"><span data-stu-id="63f8b-120">**Size digit**</span></span>       | <span data-ttu-id="63f8b-121">サイズが含まれる製品バリアントのために作成されたバーコードのサイズを示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-121">Indicates size in a bar code created for a product variant which includes size.</span></span>                                 |
| <span data-ttu-id="63f8b-122">**カラー ディジット**</span><span class="sxs-lookup"><span data-stu-id="63f8b-122">**Color digit**</span></span>      | <span data-ttu-id="63f8b-123">色が含まれる製品バリアントのために作成されたバーコードの色を示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-123">Indicates color in a bar code created for a product variant which includes color.</span></span>                               |
| <span data-ttu-id="63f8b-124">**スタイル ディジット**</span><span class="sxs-lookup"><span data-stu-id="63f8b-124">**Style digit**</span></span>      | <span data-ttu-id="63f8b-125">スタイルが含まれる製品バリアントのために作成されたバーコードのスタイルを示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-125">Indicates style in a bar code created for a product variant which includes a style.</span></span>                             |
| <span data-ttu-id="63f8b-126">**EAN ライセンス コード**</span><span class="sxs-lookup"><span data-stu-id="63f8b-126">**EAN license code**</span></span> | <span data-ttu-id="63f8b-127">EAN ライセンス コードに対して発行された EAN ライセンスのプレースホルダー。</span><span class="sxs-lookup"><span data-stu-id="63f8b-127">Placeholder for EAN license issued for EAN license codes.</span></span>                                                       |
| <span data-ttu-id="63f8b-128">[**価格**]</span><span class="sxs-lookup"><span data-stu-id="63f8b-128">**Price**</span></span>            | <span data-ttu-id="63f8b-129">価格埋め込みバーコードの価格を示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-129">Indicates price for price embedded bar codes.</span></span>                                                                   |
| <span data-ttu-id="63f8b-130">**数量**</span><span class="sxs-lookup"><span data-stu-id="63f8b-130">**Quantity**</span></span>         | <span data-ttu-id="63f8b-131">数量/ランダムな重量埋め込みバーコードの数量を表示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-131">Indicates quantity in quantity/random weight embedded bar codes.</span></span>                                                |
| <span data-ttu-id="63f8b-132">**従業員**</span><span class="sxs-lookup"><span data-stu-id="63f8b-132">**Employee**</span></span>         | <span data-ttu-id="63f8b-133">バーコード POS ログインに使用する従業員 ID 番号のバーコード区分を示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-133">Indicates bar code segment for employee ID number used for bar code POS login.</span></span>                                  |
| <span data-ttu-id="63f8b-134">**顧客**</span><span class="sxs-lookup"><span data-stu-id="63f8b-134">**Customer**</span></span>         | <span data-ttu-id="63f8b-135">顧客 ID 区分を示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-135">Indicates customer ID segment.</span></span>                                                                                  |
| <span data-ttu-id="63f8b-136">**データ入力**</span><span class="sxs-lookup"><span data-stu-id="63f8b-136">**Data entry**</span></span>       | <span data-ttu-id="63f8b-137">*まだ実装されていません。*</span><span class="sxs-lookup"><span data-stu-id="63f8b-137">*Not yet implemented.*</span></span>                                                                                          |
| <span data-ttu-id="63f8b-138">**割引コード**</span><span class="sxs-lookup"><span data-stu-id="63f8b-138">**Discount code**</span></span>    | <span data-ttu-id="63f8b-139">Dynamics 365 for Retail Spring 2017 リリース時点での*償却*。</span><span class="sxs-lookup"><span data-stu-id="63f8b-139">*Depreciated* as of Dynamics 365 for Retail Spring 2017 release.</span></span> <span data-ttu-id="63f8b-140">以前: 販売時点のトランザクションに割引を追加するのに使用されるバーコードの割引コードを示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-140">Previously: Indicates discount code for a bar code that's used to add a discount to a point of sale transaction.</span></span>                                                                   |
| <span data-ttu-id="63f8b-141">**クーポン コード**</span><span class="sxs-lookup"><span data-stu-id="63f8b-141">**Coupon code**</span></span>      | <span data-ttu-id="63f8b-142">小売注文に割引を追加するために使用するバーコードのクーポン コードを示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-142">Indicates coupon code for a bar code used to add a discount to a retail order.</span></span> <span data-ttu-id="63f8b-143">これは割引コードが置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="63f8b-143">This replaced discount code.</span></span>     |
| <span data-ttu-id="63f8b-144">**ギフト カード**</span><span class="sxs-lookup"><span data-stu-id="63f8b-144">**Gift card**</span></span>        | <span data-ttu-id="63f8b-145">ギフト カードの発行またはギフト カードでの支払い時のギフト カード番号を示します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-145">Indicates a gift card number when issuing or paying by gift card.</span></span>                                               |
| <span data-ttu-id="63f8b-146">**ロイヤルティ カード**</span><span class="sxs-lookup"><span data-stu-id="63f8b-146">**Loyalty card**</span></span>     | <span data-ttu-id="63f8b-147">ロイヤルティ顧客をトランザクションに追加し、ロイヤルティでの支払時に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="63f8b-147">Adds a loyalty customer to the transaction, and can be used when paying by loyalty.</span></span>                             |

## <a name="define-bar-code-masks"></a><span data-ttu-id="63f8b-148">バーコード マスクの定義</span><span class="sxs-lookup"><span data-stu-id="63f8b-148">Define bar code masks</span></span>
<span data-ttu-id="63f8b-149">バーコード マスク文字を必要なバーコード マスクに指定した後、[**小売**] &gt; [**在庫管理**] &gt; [**バーコードとラベル**] &gt; [**バーコード マスク設定**] に移動します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-149">After bar code mask characters are specified for the necessary bar code masks, go to **Retail** &gt; **Inventory management** &gt; **Barcodes and labels** &gt; **Barcode mask setup**.</span></span> <span data-ttu-id="63f8b-150">このページでは、以前に指定された文字を使用するバーコード マスクを定義できます。</span><span class="sxs-lookup"><span data-stu-id="63f8b-150">On this page, you can define bar code masks that use the previously specified characters.</span></span> <span data-ttu-id="63f8b-151">これらのバーコード マスクはバーコードを生成する際に使用し、POS.でスキャンしたバーコードの識別にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="63f8b-151">These bar code masks will be used when generating bar codes and will also help to identify bar codes scanned at the POS.</span></span>

1.  <span data-ttu-id="63f8b-152">[**新規**] をクリックして、新しいバーコード マスク文字を作成します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-152">Click **New** to create a new bar code mask.</span></span>
2.  <span data-ttu-id="63f8b-153">[**マスク ID**] と [**説明**] フィールドに値を入力し、[**タイプ**] フィールドでバーコード マスクのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-153">Enter values in the **Mask ID** and **Description** fields, and then select a bar code mask type in the **Type** field.</span></span>
3.  <span data-ttu-id="63f8b-154">[**一般**] セクションでは、[**バーコード標準**] フィールドで値を選択し、必要な場合はバーコードの接頭語を指定します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-154">In the **General** section, select a value in the **Bar code standard** field, and then specify the bar code prefix, if one is required.</span></span>
4.  <span data-ttu-id="63f8b-155">[**バーコード マスク区分**] セクションでは、作成するバーコードで使用するバーコード区分を加えます。</span><span class="sxs-lookup"><span data-stu-id="63f8b-155">In the **Bar code mask segment** section, add bar code segments that will be used in the bar code to be created.</span></span>

<span data-ttu-id="63f8b-156">例として、「製品」マスク ID でバーコード マスクを作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="63f8b-156">As an example, to create a bar code mask with mask ID 'Product', you'd do the following:</span></span>

1.  <span data-ttu-id="63f8b-157">新しいバーコード マスクを作成し、「製品」タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-157">Create a new bar code mask and select type ‘Product’.</span></span>
2.  <span data-ttu-id="63f8b-158">バーコード標準を、例えば「コード 39」と選択します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-158">Select a bar code standard, for example, 'Code 39'.</span></span>
3.  <span data-ttu-id="63f8b-159">バーコードを容易に識別するために使用する接頭語を指定します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-159">Provide a prefix to be used to easily identify the bar code.</span></span> <span data-ttu-id="63f8b-160">たとえば、「22」を選択します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-160">For example, ‘22’.</span></span>
4.  <span data-ttu-id="63f8b-161">マスク区分を追加します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-161">Add a mask segment.</span></span> <span data-ttu-id="63f8b-162">「製品」マスク区分が選択されます。</span><span class="sxs-lookup"><span data-stu-id="63f8b-162">The ‘Product’ mask segment will be selected.</span></span>
5.  <span data-ttu-id="63f8b-163">製品区分の長さを、例えば「10」と指定します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-163">Provide a length for the product segment, for example, ‘10’.</span></span> <span data-ttu-id="63f8b-164">長さは店舗で一般的に使用される製品 ID の長さに一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f8b-164">The length should match the length of a product ID commonly used in the store.</span></span> <span data-ttu-id="63f8b-165">マスクはプレビューとして [**マスク**] の下の [**一般**] セクションで表示されます。</span><span class="sxs-lookup"><span data-stu-id="63f8b-165">The mask will be displayed as a preview in the **General** section under **Mask**.</span></span>

## <a name="assign-bar-code-masks-to-bar-codes"></a><span data-ttu-id="63f8b-166">バーコードにバーコード マスクを割り当てる</span><span class="sxs-lookup"><span data-stu-id="63f8b-166">Assign bar code masks to bar codes</span></span>
<span data-ttu-id="63f8b-167">バーコード マスクは、使用する前にバーコードに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f8b-167">Bar codes masks must be assigned to bar codes before they can be used.</span></span> <span data-ttu-id="63f8b-168">引き続き前の例を用いると、バーコードにバーコード マスクを割り当てるには次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="63f8b-168">Continuing with the previous example, to assign the bar code mask to a bar code, do the following:</span></span>

1.  <span data-ttu-id="63f8b-169">[**組織管理**] &gt; [**設定**] &gt; [**バーコード**] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-169">Go to **Organization administration** &gt; **Setup** &gt; **Bar codes**.</span></span> <span data-ttu-id="63f8b-170">[**新規**] をクリックして新しいバーコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-170">Click **New** to create a new bar code.</span></span>
2.  <span data-ttu-id="63f8b-171">[**バーコード** **設定**] と [設定] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-171">Enter values in the **Barcode** **setup** and **Setup **fields.</span></span>
3.  <span data-ttu-id="63f8b-172">[**一般**] セクションでは、[**バーコード タイプ**] フィールドで「コード 39」を選択します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-172">In the **General** section, in the **Bar code type** field, select ‘Code 39’.</span></span> <span data-ttu-id="63f8b-173">[**マスク** **ID**] フィールドでは、以前に作成した「製品」マスクを選択します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-173">In the **Mask** **ID** field, select the ‘Product’ mask previously created.</span></span>
4.  <span data-ttu-id="63f8b-174">[**サイズ**] で「12」を入力します。</span><span class="sxs-lookup"><span data-stu-id="63f8b-174">Under **Size**, enter ‘12’.</span></span>
5.  <span data-ttu-id="63f8b-175">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63f8b-175">Click **Save**.</span></span>

<span data-ttu-id="63f8b-176">これで、バーコード マスクを使用して製品のバーコードを作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="63f8b-176">The bar code mask can now be used to create bar codes for products.</span></span> <span data-ttu-id="63f8b-177">上記の手順は製品のバーコード マスクを作成する方法の例ですが、サポートされている他のバーコード タイプのバーコード マスクを作成する方法も示しています。</span><span class="sxs-lookup"><span data-stu-id="63f8b-177">The above steps are examples of how to create bar code masks for products, but they also illustrate how to create bar code masks for any of the other supported bar code types.</span></span> <span data-ttu-id="63f8b-178">バーコード マスク、タイプ、また長さは、特定の環境における使用に合わせて調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f8b-178">Bar code masks, types, and lengths should be adjusted for use in your specific environment.</span></span>




