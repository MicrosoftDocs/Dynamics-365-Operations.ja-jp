---
title: "小売販売のクーポンの作成"
description: "このトピックでは、小売クーポンの概要と設定方法について説明します。"
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: f68671ea2971d1226bd6b878c41d2dae0d47b4a2
ms.contentlocale: ja-jp
ms.lasthandoff: 01/19/2018

---

# <a name="create-coupons-for-retail-sales"></a><span data-ttu-id="3faa5-103">小売販売のクーポンの作成</span><span class="sxs-lookup"><span data-stu-id="3faa5-103">Create coupons for retail sales</span></span>

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a><span data-ttu-id="3faa5-104">クーポンの概要</span><span class="sxs-lookup"><span data-stu-id="3faa5-104">Overview of coupons</span></span>

<span data-ttu-id="3faa5-105">クーポンは、トランザクションに小売割引を追加するために使用するコードおよびバーコードです。</span><span class="sxs-lookup"><span data-stu-id="3faa5-105">Coupons are codes and bar codes that are used to add retail discounts to transactions.</span></span> <span data-ttu-id="3faa5-106">各クーポンには複数のコードを使用でき、各コードに独自の有効日を設定できます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-106">Each coupon can have multiple codes, and each code can have its own effective dates.</span></span> 

<span data-ttu-id="3faa5-107">各クーポンは 1 つの小売割引に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-107">Each coupon is related to one retail discount.</span></span> <span data-ttu-id="3faa5-108">割引に関連付けられている価格グループは、クーポンまたはクーポンが有効なチャンネルを使用できる顧客を定義します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-108">The price groups that are associated with the discount define the customers that can use a coupon or the channels where a coupon is valid.</span></span> 

<span data-ttu-id="3faa5-109">基本的に、クーポンは小売割引での追加の検証です。</span><span class="sxs-lookup"><span data-stu-id="3faa5-109">Essentially, coupons are additional validation on top of retail discounts.</span></span> <span data-ttu-id="3faa5-110">クーポンによって、必要なクーポン コードおよびバーコードがこれらのコードの日付範囲と共に提供されます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-110">The coupon provides the coupon codes and bar codes that are required, together with date ranges for those codes.</span></span> <span data-ttu-id="3faa5-111">クーポンでは、オプションの使用制限と顧客に必要なプロパティも提供されます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-111">The coupon also provides optional usage limits and customer required properties.</span></span> <span data-ttu-id="3faa5-112">割引は、クーポンが有効な製品のセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-112">The discount provides the set of products that the coupon is valid for.</span></span> <span data-ttu-id="3faa5-113">割引の価格グループは、クーポンが有効な顧客、チャンネル、またはカタログのセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-113">The price groups for the discount provide the set of customers, channels, or catalogs that the coupon is valid for.</span></span>

<span data-ttu-id="3faa5-114">クーポンを作成するには、割引とクーポンを別に作成します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-114">To create a coupon, you create the discount and the coupon separately.</span></span> <span data-ttu-id="3faa5-115">Microsoft Dynamics 365 for Retail のクーポン ページで割引を選択することでそれらをリンクします。</span><span class="sxs-lookup"><span data-stu-id="3faa5-115">You then link them by selecting the discount on the coupon page in Microsoft Dynamics 365 for Retail.</span></span> 

> [!NOTE]
> <span data-ttu-id="3faa5-116">クーポンを割引にリンクすると、Microsoft Dynamics 365 for Retail の割引ページのいくつかのフィールドは、クーポンの設定で管理されているため読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="3faa5-116">After a coupon is linked to a discount, several fields on the discount page in Microsoft Dynamics 365 for Retail become read-only, because they are managed by the coupon’s settings.</span></span> <span data-ttu-id="3faa5-117">これらのフィールドには、ステータスと標準の日付範囲のフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-117">These fields include the fields for the status and standard date ranges.</span></span>

### <a name="limited-use-coupons"></a><span data-ttu-id="3faa5-118">専用クーポン</span><span class="sxs-lookup"><span data-stu-id="3faa5-118">Limited-use coupons</span></span>

<span data-ttu-id="3faa5-119">専用クーポンとして、クーポンを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-119">Coupons can be configured as limited-use coupons.</span></span> <span data-ttu-id="3faa5-120">使用制限は、顧客またはチャンネルごと、またはグローバルな制限として定義できます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-120">The usage limit can be defined per customer or channel, or as a global limit.</span></span> <span data-ttu-id="3faa5-121">POS または販売注文入力時にコードまたはバーコードを入力またはスキャンする際に、この制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-121">This limit is enforced when the code or bar code is entered or scanned in POS or during sales order entry.</span></span> <span data-ttu-id="3faa5-122">クーポンは、関連付けられている注文の完了時に使用されたものとして記録されます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-122">A coupon is recorded as used when an order is completed that has the coupon associated with it.</span></span>

<span data-ttu-id="3faa5-123">制限は、クーポンのクーポン コードごとに適用されます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-123">The limit is enforced per coupon code on a coupon.</span></span> <span data-ttu-id="3faa5-124">たとえば、2 つのクーポン コードを持つ 1 回のみ使用のクーポンは、各クーポン コード 1 回で 2 回使用できます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-124">For example, a single-use coupon that has two coupon codes can be used two times: one time for each coupon code.</span></span> <span data-ttu-id="3faa5-125">クーポンの各コードは、個別に有効に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-125">Each code on a coupon can be independently set to active.</span></span>

## <a name="managing-coupons"></a><span data-ttu-id="3faa5-126">クーポンの管理</span><span class="sxs-lookup"><span data-stu-id="3faa5-126">Managing coupons</span></span>

<span data-ttu-id="3faa5-127">割引とクーポンは別に作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3faa5-127">You must create the discount and the coupon separately.</span></span> <span data-ttu-id="3faa5-128">クーポン ページで割引を選択することでそれらをリンクします。</span><span class="sxs-lookup"><span data-stu-id="3faa5-128">You then link them by selecting the discount on the coupon page.</span></span> <span data-ttu-id="3faa5-129">クーポンを割引にリンクすると、割引のいくつかのフィールドは、クーポンの設定で管理されているため読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="3faa5-129">After you link a coupon to a discount, several fields for the discount become read-only, because they are managed by the coupon's settings.</span></span> <span data-ttu-id="3faa5-130">これらのフィールドには、ステータスと標準の日付範囲のフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-130">These fields include the fields for the status and standard date ranges.</span></span>  

<span data-ttu-id="3faa5-131">基本的に、クーポンは小売割引での追加の検証になります。</span><span class="sxs-lookup"><span data-stu-id="3faa5-131">Essentially, coupons are now additional validation on top of retail discounts.</span></span> <span data-ttu-id="3faa5-132">クーポンによって、クーポン コードおよびバーコードが日付範囲、使用制限、顧客に必要なプロパティと共に提供されます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-132">The coupon provides the coupon codes and bar codes, together with date ranges, the usage limits, and the customer required property.</span></span> <span data-ttu-id="3faa5-133">割引は、クーポンが有効な製品のセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-133">The discount provides the set of products that the coupon is valid for.</span></span> <span data-ttu-id="3faa5-134">割引の価格グループは、クーポンが有効な顧客、チャンネル、またはカタログのセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-134">The discount's price groups provide the set of customers, channels, or catalogs that the coupon is valid for.</span></span>

## <a name="system-setup-for-coupons"></a><span data-ttu-id="3faa5-135">クーポンのシステム設定</span><span class="sxs-lookup"><span data-stu-id="3faa5-135">System setup for coupons</span></span> 

<span data-ttu-id="3faa5-136">クーポンを設定する前に、クーポンのバーコードおよび 2 つのクーポン番号順序を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3faa5-136">Before you can set up a coupon, you must set up the coupon bar code and two coupon number sequences.</span></span> 

1.  <span data-ttu-id="3faa5-137">**マスク文字**ページで、クーポン コードに対して新しいマスク文字を作成します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-137">On the **Mask characters** page, create a new mask character for the coupon code.</span></span> <span data-ttu-id="3faa5-138">未使用の文字をどれでも選択できます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-138">You can select any unused character.</span></span>
2.  <span data-ttu-id="3faa5-139">**バーコード マスクの設定**ページで、新しいバーコード マスクを作成します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-139">On the **Bar code mask setup** page, create a new bar code mask.</span></span> <span data-ttu-id="3faa5-140">[**タイプ**] フィールドを [**クーポン**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-140">Set the **Type** field to **Coupon**.</span></span>
3.  <span data-ttu-id="3faa5-141">**バーコード設定**ページで、作成したバーコード マスクを使用する新しいバーコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-141">On the **Bar code setup** page, create a new bar code that uses the bar code mask that you just created.</span></span>
4.  <span data-ttu-id="3faa5-142">**番号順序**ページで、2 つの新しい番号順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-142">On the **Number sequences** page, create two new number sequences.</span></span> <span data-ttu-id="3faa5-143">1 つの順序は、クーポン コード ID 用で、もう 1 つはクーポン番号用です。</span><span class="sxs-lookup"><span data-stu-id="3faa5-143">One sequence is for the coupon code ID, and the other sequence is for the coupon number.</span></span> <span data-ttu-id="3faa5-144">クーポン コード ID は、クーポンの各クーポン コードに対する一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="3faa5-144">The coupon code ID is the unique identifier for each coupon code for a coupon.</span></span> <span data-ttu-id="3faa5-145">クーポン番号はクーポンに対する一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="3faa5-145">The coupon number is the unique identifier for a coupon.</span></span> <span data-ttu-id="3faa5-146">各クーポンには、クーポンをトリガーする複数のコードとバーコードを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-146">Each coupon can have multiple codes and bar codes that trigger the coupon.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3faa5-147">両方の番号順序において、[**スコープ**] フィールドを [**会社**] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3faa5-147">For both number sequences, you must set the **Scope** field to **Company**.</span></span> <span data-ttu-id="3faa5-148">ほとんどの場合、両方の番号順序を自動的に生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3faa5-148">In most cases, you should automatically generate both sequence numbers.</span></span>

5.  <span data-ttu-id="3faa5-149">**小売共有パラメーター** ページの [**バーコード**] タブで、先ほど作成したバーコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-149">On the **Retail shared parameters** page, on the **Bar codes** tab, select the bar code that you created earlier.</span></span>
6.  <span data-ttu-id="3faa5-150">**小売パラメーター** ページの [**番号順序**] タブで、クーポン番号およびクーポン コード ID に対して作成した番号順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-150">On the **Retail parameters** page, on the **Number sequences** tab, select the number sequences that you created for the coupon number and coupon code ID.</span></span>
7.  <span data-ttu-id="3faa5-151">これで、**クーポン** ページを開いて、新しいクーポンを作成できます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-151">You can now open the **Coupons** page and create new coupons.</span></span>

## <a name="the-effect-of-partial-updates-on-coupons"></a><span data-ttu-id="3faa5-152">クーポンに対する部分的な更新の影響</span><span class="sxs-lookup"><span data-stu-id="3faa5-152">The effect of partial updates on coupons</span></span>

<span data-ttu-id="3faa5-153">クーポン機能は、Dynamics 365 for Retail の複数の異なる機能で構成されています。</span><span class="sxs-lookup"><span data-stu-id="3faa5-153">Coupon functionality comprises multiple distinct features in Dynamics 365 for Retail.</span></span> <span data-ttu-id="3faa5-154">Microsoft Dynamics 365 for Retail の本社 (HQ) とチャンネルは、コンポーネント間で部分的に更新することができます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-154">Microsoft Dynamics 365 for Retail headquarters (HQ) and the channel can be partially updated across components.</span></span> <span data-ttu-id="3faa5-155">したがって、部分的な更新が全体としてのクーポン機能にどれほど影響するのか理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="3faa5-155">Therefore, it's important that you understand how partial updates affect coupon functionality as a whole.</span></span>

- <span data-ttu-id="3faa5-156">**HQ は部分的に更新されますが、Retail サーバーと POS は更新されません。**</span><span class="sxs-lookup"><span data-stu-id="3faa5-156">**HQ is partially updated, but Retail server and POS aren't updated.**</span></span> <span data-ttu-id="3faa5-157">HQ 更新では、クーポンと割引ページが更新され、小売価格エンジンも更新されます。</span><span class="sxs-lookup"><span data-stu-id="3faa5-157">In an HQ update, the coupon and discount pages are updated, and the retail price engine is also updated.</span></span> <span data-ttu-id="3faa5-158">これら 2 つのコンポーネントの一方だけが更新された場合、小売用の一部のページで価格計算データが一致しなくなります。</span><span class="sxs-lookup"><span data-stu-id="3faa5-158">If only one of those two components is updated, some pages in Retail won’t match the price calculation data.</span></span> <span data-ttu-id="3faa5-159">そのため、予期しない割引の計算やエラーが、割引の計算時に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3faa5-159">Therefore, unexpected discount calculations or errors might occur during discount calculations.</span></span>
- <span data-ttu-id="3faa5-160">**HQ は更新されますが、Retail サーバーと POS は更新されません (N-1)。**</span><span class="sxs-lookup"><span data-stu-id="3faa5-160">**HQ is updated, but Retail server and POS aren't updated (N-1).**</span></span> <span data-ttu-id="3faa5-161">すべての小売店舗を同時に更新できるわけではないため、小売店舗を更新する前に、HQ を更新することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3faa5-161">Because not all retail stores can be updated at the same time, we recommend that you update HQ before you update retail stores.</span></span> <span data-ttu-id="3faa5-162">N-1 シナリオでは、クーポンに関連する新しい機能は、まだ更新されていない店舗では使用できません。</span><span class="sxs-lookup"><span data-stu-id="3faa5-162">In the N-1 scenario, new functionality that is related to coupons won't be available in stores that haven’t been updated yet.</span></span> <span data-ttu-id="3faa5-163">たとえば、クーポン機能では、明細行の「除外」について説明します。</span><span class="sxs-lookup"><span data-stu-id="3faa5-163">For example, the coupon functionality introduces “exclude” lines.</span></span> <span data-ttu-id="3faa5-164">割引に明細行の除外を使用する場合は、以前のバージョンを実行している小売店舗では適用されません。</span><span class="sxs-lookup"><span data-stu-id="3faa5-164">If you use exclude lines on a discount, they won't be applied in a retail store that is running an earlier version.</span></span>
- <span data-ttu-id="3faa5-165">**HQ は更新されず、Retail サーバーと POS が更新されます (N+1)。**</span><span class="sxs-lookup"><span data-stu-id="3faa5-165">**HQ isn't updated, but Retail server and POS are updated (N+1).**</span></span> <span data-ttu-id="3faa5-166">Retail サーバーで更新された価格エンジンで価格の計算時にレガシ割引コードを処理できるので、このシナリオでは更新による機能の影響はありません。</span><span class="sxs-lookup"><span data-stu-id="3faa5-166">Because the updated price engine in Retail server can handle legacy discount codes during price calculations, the update should have no functional impact in this scenario.</span></span>

