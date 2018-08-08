---
title: "品目の交換注文の作成"
description: "品目交換注文は通常、製品が返品され、検査された後で作成されます。"
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 784a2522c27e8131f211ffc52319552b3b928cc3
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="create-an-item-replacement-order"></a><span data-ttu-id="d1176-103">品目の交換注文の作成</span><span class="sxs-lookup"><span data-stu-id="d1176-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d1176-104">品目交換注文は通常、製品が返品され、検査された後で作成されます。</span><span class="sxs-lookup"><span data-stu-id="d1176-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="d1176-105">ただし、品目が返品される前に交換する必要がある場合、または元の品目が返品されない場合は、返品注文を作成した後ですぐに品目交換注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="d1176-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="d1176-106">返品品目を受け取った後の交換注文の作成</span><span class="sxs-lookup"><span data-stu-id="d1176-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="d1176-107">**販売とマーケティング** \> **共通** \> **返品注文** \> **すべての返品注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1176-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="d1176-108">新しい返品注文を作成するか、一覧から返品注文を選択して**返品注文 - RMA 番号: %1、%2**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="d1176-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="d1176-109">**返品行**をクリックして、**交換品目**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1176-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="d1176-110">返品品目と置き換える品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1176-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="d1176-111">品目の詳細を入力し、**適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1176-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="d1176-112">返品注文の梱包明細を生成するには**梱包明細**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1176-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="d1176-113">選択した交換品目に対して販売注文が生成されます。</span><span class="sxs-lookup"><span data-stu-id="d1176-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="d1176-114">販売注文が交換品目に対して作成された後、販売契約書が自動的に検索され、適用できる販売契約書がある場合、販売注文に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d1176-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="d1176-115">返品品目を受け取る前の交換注文の作成</span><span class="sxs-lookup"><span data-stu-id="d1176-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="d1176-116">**販売とマーケティング** \> **共通** \> **返品注文** \> **すべての返品注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1176-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="d1176-117">新しい返品注文を作成するか、一覧から返品注文を選択して**返品注文 - RMA 番号: %1、%2**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="d1176-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="d1176-118">返品品目の販売注文を確認するには、**販売注文の検索**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1176-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="d1176-119">**販売注文の検索**フォームを完了し、**OK**をクリックしてフォームを閉じ、**返品注文 - RMA 番号: %1、%2**フォームに返します。</span><span class="sxs-lookup"><span data-stu-id="d1176-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="d1176-120">返品品目の販売注文明細行が返品注文にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d1176-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="d1176-121">**交換注文**をクリックして**販売注文の作成**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="d1176-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="d1176-122">**返品注文明細行のコピー**チェック ボックスをオンにして、**返品注文 - RMA 番号: %1、%2** フォームで選択した返品注文からこの販売注文に詳細を転送します。</span><span class="sxs-lookup"><span data-stu-id="d1176-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="d1176-123">必要に応じて、詳細を入力または変更します。</span><span class="sxs-lookup"><span data-stu-id="d1176-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="d1176-124">ステップ 3 で販売注文を識別し、返品品目の販売注文明細行が販売契約書にリンクされている場合、品目交換注文の該当する販売契約書 ID は**販売契約書 ID**フィールドに自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1176-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="d1176-125">**OK**をクリックして**販売注文の作成**フォームを閉じて**販売注文** フォームを開き、ここで新しい販売注文の情報を入力し続けることができます。</span><span class="sxs-lookup"><span data-stu-id="d1176-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="d1176-126">任意の該当する返品注文明細行は新しい販売注文にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d1176-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="d1176-127">販売契約書の ID が**販売契約書 ID**フィールドに自動的に表示される場合、販売契約書は品目交換注文の販売注文ヘッダーにリンク済みです。</span><span class="sxs-lookup"><span data-stu-id="d1176-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="d1176-128">実施されていない販売契約書に適用可能な確約があり、その販売契約書の期限が切れる前に販売注文が作成される場合、販売契約書の明細行と販売注文の明細行の間にリンクが設定されます。</span><span class="sxs-lookup"><span data-stu-id="d1176-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="d1176-129">したがって、品目の価格などの販売契約書からの情報は、新しい販売注文の明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d1176-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  



