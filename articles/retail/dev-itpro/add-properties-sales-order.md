---
title: プロパティを販売注文に追加
description: 販売注文のプロパティをカスタマイズすることにより、オンライン ストアから追加データを送信して業務プロセスの要件を満たすことができます。 この記事では、販売注文にプロパティを追加する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 44351
ms.assetid: dd9b86cb-630a-4429-9aea-8ba4c4723baa
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dcd139698cc611cc1abcd128a787e994d732e0d4
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833097"
---
# <a name="add-properties-to-sales-orders"></a><span data-ttu-id="3bd19-104">プロパティを販売注文に追加</span><span class="sxs-lookup"><span data-stu-id="3bd19-104">Add properties to sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3bd19-105">販売注文のプロパティをカスタマイズすることにより、オンライン ストアから追加データを送信して業務プロセスの要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="3bd19-105">By customizing the properties of sales orders, you can send additional data from your online store to meet the requirements of your business processes.</span></span> <span data-ttu-id="3bd19-106">この記事では、販売注文にプロパティを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-106">This article explains how to add properties to a sales order.</span></span>

<span data-ttu-id="3bd19-107">スターター ストアには、注文トランザクション中にデータを取得するために使用できる販売注文プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="3bd19-107">The starter store has sales order properties that you can use to capture data during order transactions.</span></span> <span data-ttu-id="3bd19-108">ただし、販売注文のプロパティを拡張し、注文トランザクション中に追加データを送信するすることができます。</span><span class="sxs-lookup"><span data-stu-id="3bd19-108">However, you can extend the sales order properties to send additional data during order transactions.</span></span> <span data-ttu-id="3bd19-109">たとえば、品目が贈物用に包装されるべきかを示す **GiftWrap** 属性を追加できます。</span><span class="sxs-lookup"><span data-stu-id="3bd19-109">For example, you can add a **GiftWrap** attribute to indicate that an item should be gift-wrapped.</span></span> <span data-ttu-id="3bd19-110">販売注文のプロパティをカスタマイズするには、次の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bd19-110">To customize sales order properties, you must complete the following tasks:</span></span>

1.  <span data-ttu-id="3bd19-111">属性を作成します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-111">Create an attribute.</span></span>
2.  <span data-ttu-id="3bd19-112">属性グループに属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-112">Add the attribute to an attribute group.</span></span>
3.  <span data-ttu-id="3bd19-113">オンライン ストアに属性グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3bd19-113">Assign the attribute group to your online store.</span></span>
4.  <span data-ttu-id="3bd19-114">販売注文書で属性を設定します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-114">Set the attribute on a sales order.</span></span>

## <a name="create-an-attribute"></a><span data-ttu-id="3bd19-115">属性を作成します</span><span class="sxs-lookup"><span data-stu-id="3bd19-115">Create an attribute</span></span>
<span data-ttu-id="3bd19-116">属性を作成するには、属性タイプを定義してから、新しい属性に属性タイプを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bd19-116">To create an attribute, you must define an attribute type and then assign the attribute type to your new attribute.</span></span> <span data-ttu-id="3bd19-117">この例では、事前定義済みの属性タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-117">In this example, you use a pre-defined attribute type.</span></span>

1.  <span data-ttu-id="3bd19-118">クライアントで、**製品情報管理** &gt; **設定** &gt; **カテゴリと属性** &gt; **属性**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-118">In the client, click **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attributes**.</span></span>
2.  <span data-ttu-id="3bd19-119">**新規**をクリックし、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-119">Click **New**, and enter the following values.</span></span>

    | <span data-ttu-id="3bd19-120">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3bd19-120">Property</span></span>       | <span data-ttu-id="3bd19-121">先頭値</span><span class="sxs-lookup"><span data-stu-id="3bd19-121">Value</span></span>        |
    |----------------|--------------|
    | <span data-ttu-id="3bd19-122">氏名</span><span class="sxs-lookup"><span data-stu-id="3bd19-122">Name</span></span>           | <span data-ttu-id="3bd19-123">GiftWrap</span><span class="sxs-lookup"><span data-stu-id="3bd19-123">GiftWrap</span></span>     |
    | <span data-ttu-id="3bd19-124">フレンドリ名</span><span class="sxs-lookup"><span data-stu-id="3bd19-124">Friendly name</span></span>  | <span data-ttu-id="3bd19-125">ギフト ラップ</span><span class="sxs-lookup"><span data-stu-id="3bd19-125">Gift wrap</span></span>    |
    | <span data-ttu-id="3bd19-126">属性タイプ</span><span class="sxs-lookup"><span data-stu-id="3bd19-126">Attribute type</span></span> | <span data-ttu-id="3bd19-127">StringDomain</span><span class="sxs-lookup"><span data-stu-id="3bd19-127">StringDomain</span></span> |

## <a name="add-the-attribute-to-an-attribute-group"></a><span data-ttu-id="3bd19-128">属性グループへの属性の追加</span><span class="sxs-lookup"><span data-stu-id="3bd19-128">Add the attribute to an attribute group</span></span>
<span data-ttu-id="3bd19-129">属性を定義した後は、属性グループを追加する事ができます。</span><span class="sxs-lookup"><span data-stu-id="3bd19-129">After you define an attribute, you can add it to an attribute group.</span></span>

1.  <span data-ttu-id="3bd19-130">**製品情報管理** &gt; **設定** &gt; **カテゴリと属性** &gt; **属性グループ**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-130">Click **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attribute groups**.</span></span>
2.  <span data-ttu-id="3bd19-131">**新規**をクリックし、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-131">Click **New**, and enter the following values.</span></span>

    | <span data-ttu-id="3bd19-132">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3bd19-132">Property</span></span>      | <span data-ttu-id="3bd19-133">先頭値</span><span class="sxs-lookup"><span data-stu-id="3bd19-133">Value</span></span>                       |
    |---------------|-----------------------------|
    | <span data-ttu-id="3bd19-134">氏名</span><span class="sxs-lookup"><span data-stu-id="3bd19-134">Name</span></span>          | <span data-ttu-id="3bd19-135">SalesOrderGroup</span><span class="sxs-lookup"><span data-stu-id="3bd19-135">SalesOrderGroup</span></span>             |
    | <span data-ttu-id="3bd19-136">フレンドリ名</span><span class="sxs-lookup"><span data-stu-id="3bd19-136">Friendly name</span></span> | <span data-ttu-id="3bd19-137">販売注文属性グループ</span><span class="sxs-lookup"><span data-stu-id="3bd19-137">Sales order attribute group</span></span> |
    | <span data-ttu-id="3bd19-138">説明</span><span class="sxs-lookup"><span data-stu-id="3bd19-138">Description</span></span>   | <span data-ttu-id="3bd19-139">販売注文属性グループ</span><span class="sxs-lookup"><span data-stu-id="3bd19-139">Sales order attribute group</span></span> |

3.  <span data-ttu-id="3bd19-140">**属性**クイック タブで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-140">On the **Attributes** FastTab, click **Add**.</span></span>
4.  <span data-ttu-id="3bd19-141">**GiftWrap** を選択し、**選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-141">Select **GiftWrap**, and then click **Select**.</span></span>
5.  <span data-ttu-id="3bd19-142">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-142">Click **OK**.</span></span>

## <a name="assign-the-attribute-group-to-your-online-store"></a><span data-ttu-id="3bd19-143">オンライン ストアに属性グループを割り当てます</span><span class="sxs-lookup"><span data-stu-id="3bd19-143">Assign the attribute group to your online store</span></span>
<span data-ttu-id="3bd19-144">属性グループを作成した後は、オンライン ストアに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="3bd19-144">After you create an attribute group, you can assign it to your online store.</span></span>

1.  <span data-ttu-id="3bd19-145">**小売** &gt; **チャンネル** &gt; **オンライン ストア**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-145">Click **Retail** &gt; **Channels** &gt; **Online stores**.</span></span>
2.  <span data-ttu-id="3bd19-146">**オンライン ストア** リストで、店舗をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-146">In the **Online stores** list, double-click your store.</span></span>
3.  <span data-ttu-id="3bd19-147">**設定**タブで、**販売注文属性**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-147">On the **Set up** tab, click **Sales order attributes**.</span></span>
4.  <span data-ttu-id="3bd19-148">**チャネル属性グループ**ページで、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-148">On the **Channel attribute groups** page, click **New**.</span></span>
5.  <span data-ttu-id="3bd19-149">**名前**フィールドで **SalesOrderGroup** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-149">In the **Name** field, select **SalesOrderGroup**.</span></span>

## <a name="set-the-attribute-on-a-sales-order"></a><span data-ttu-id="3bd19-150">販売注文書で属性を設定</span><span class="sxs-lookup"><span data-stu-id="3bd19-150">Set the attribute on a sales order</span></span>
<span data-ttu-id="3bd19-151">Commerce Runtime 内にビジネス ロジックを追加することにより属性を販売注文に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="3bd19-151">You can add the attribute to a sales order by adding business logic in the commerce runtime.</span></span> <span data-ttu-id="3bd19-152">次のコードを追加して、カートに属性を追加し、カートを保存します。それから、カートから受注を作成します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-152">Add the following code to add the attribute to the cart, save the cart, and then create a sales order from the cart.</span></span>

    var cart = orderManager.GetCart(cartId, accountNumber, false);
    cart.AttributeValues.Add(new AttributeTextValue { Name = "GiftWrap", TextValue = "Yes" });
    orderManager.SaveCart(cart);
    orderManager.CreateOrderFromCart(...);

## <a name="next-steps"></a><span data-ttu-id="3bd19-153">次のステップ</span><span class="sxs-lookup"><span data-stu-id="3bd19-153">Next steps</span></span>
<span data-ttu-id="3bd19-154">Commerce Runtime で販売注文を作成した後は、新しい属性を表示できます。</span><span class="sxs-lookup"><span data-stu-id="3bd19-154">After you create a sales order in the commerce runtime, you can view the new attribute.</span></span>

### <a name="view-the-attribute"></a><span data-ttu-id="3bd19-155">属性の表示</span><span class="sxs-lookup"><span data-stu-id="3bd19-155">View the attribute</span></span>

1.  <span data-ttu-id="3bd19-156">クライアントで、**小売** &gt; **小売 IT** &gt; **配送スケジュール**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-156">In the client, click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
2.  <span data-ttu-id="3bd19-157">**P-0001\_OC** ジョブを実行し、オンライン チャネルとして POS トランザクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-157">Run the **P-0001\_OC** job to run POS transactions in the online channel.</span></span>
3.  <span data-ttu-id="3bd19-158">**小売** &gt; **小売 IT** &gt; **注文の同期**の順にクリックして販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="3bd19-158">Click **Retail** &gt; **Retail IT** &gt; **Synchronize orders** to create a sales order.</span></span>
4.  <span data-ttu-id="3bd19-159">**小売** &gt; **照会およびレポート** &gt; **販売注文** &gt; **すべての販売注文**の順番にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-159">Click **Retail** &gt; **Inquiries and reports** &gt; **Sales orders** &gt; **All sales orders**.</span></span>
5.  <span data-ttu-id="3bd19-160">**小売**タブで、**小売属性**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3bd19-160">On the **Retail** tab, and click **Retail attributes**.</span></span> <span data-ttu-id="3bd19-161">作成した属性を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bd19-161">You should see the attribute that you created.</span></span>




