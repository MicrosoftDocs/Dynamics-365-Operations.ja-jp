---
title: "在庫仕訳帳"
description: "この記事では、在庫仕訳帳を使用してさまざまなタイプの物理在庫トランザクションを転記する方法について説明します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 6dfb82acb5dafd365d878949b35d4fe6ff58793d
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="inventory-journals"></a><span data-ttu-id="6985e-103">在庫仕訳帳</span><span class="sxs-lookup"><span data-stu-id="6985e-103">Inventory journals</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="6985e-104">この記事では、在庫仕訳帳を使用してさまざまなタイプの物理在庫トランザクションを転記する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6985e-104">This article describes how you can use inventory journals to post various types of physical inventory transactions.</span></span>

<span data-ttu-id="6985e-105">Microsoft Dynamics 365 for Finance and Operations の在庫仕訳帳は、払出と入荷の転記、在庫移動、部品表 (BOM) の作成など、さまざまなタイプの現物在庫トランザクション転記に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6985e-105">The inventory journals in Microsoft Dynamics 365 for Finance and Operations are used to post physical inventory transactions of various types, such as the posting of issues and receipts, inventory movements, the creation of bills of materials (BOMs), and the reconciliation of physical inventory.</span></span> <span data-ttu-id="6985e-106">これらの在庫仕訳帳はすべて同様の方法で使用されますが、異なるタイプに分類されます。</span><span class="sxs-lookup"><span data-stu-id="6985e-106">All these inventory journals are used in a similar way, but they are divided into different types.</span></span>

## <a name="types-of-inventory-journals"></a><span data-ttu-id="6985e-107">在庫仕訳帳のタイプ</span><span class="sxs-lookup"><span data-stu-id="6985e-107">Types of inventory journals</span></span>
<span data-ttu-id="6985e-108">次の在庫仕訳帳タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-108">The following types of inventory journals are available:</span></span>

-   <span data-ttu-id="6985e-109">移動</span><span class="sxs-lookup"><span data-stu-id="6985e-109">Movement</span></span>
-   <span data-ttu-id="6985e-110">在庫調整</span><span class="sxs-lookup"><span data-stu-id="6985e-110">Inventory adjustment</span></span>
-   <span data-ttu-id="6985e-111">移動</span><span class="sxs-lookup"><span data-stu-id="6985e-111">Transfer</span></span>
-   <span data-ttu-id="6985e-112">BOM</span><span class="sxs-lookup"><span data-stu-id="6985e-112">BOM</span></span>
-   <span data-ttu-id="6985e-113">品目到着</span><span class="sxs-lookup"><span data-stu-id="6985e-113">Item arrival</span></span>
-   <span data-ttu-id="6985e-114">生産入力</span><span class="sxs-lookup"><span data-stu-id="6985e-114">Production input</span></span>
-   <span data-ttu-id="6985e-115">棚卸</span><span class="sxs-lookup"><span data-stu-id="6985e-115">Counting</span></span>
-   <span data-ttu-id="6985e-116">タグ棚卸</span><span class="sxs-lookup"><span data-stu-id="6985e-116">Tag counting</span></span>

### <a name="movement"></a><span data-ttu-id="6985e-117">移動</span><span class="sxs-lookup"><span data-stu-id="6985e-117">Movement</span></span>

<span data-ttu-id="6985e-118">在庫移動仕訳帳を使用している場合、在庫を追加するときに品目に原価を追加できますが、仕訳帳を作成するときに総勘定元帳の相手勘定を指定して、特定の総勘定元帳勘定に追加の原価を手動で割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6985e-118">When you use an inventory movement journal, you can add cost to an item when you add inventory, but you must manually allocate the additional cost to a particular general ledger account by specifying a general ledger offset account when you create the journal.</span></span> <span data-ttu-id="6985e-119">この在庫仕訳帳タイプは、別の部門に対して品目を経費として扱う場合、または経費の目的で在庫から品目を削除する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="6985e-119">This inventory journal type is useful if you want to expense an item against a different department, or if you want to remove items from inventory for expense purposes.</span></span>

### <a name="inventory-adjustment"></a><span data-ttu-id="6985e-120">在庫調整</span><span class="sxs-lookup"><span data-stu-id="6985e-120">Inventory adjustment</span></span>

<span data-ttu-id="6985e-121">在庫調整仕訳帳を使用している場合、在庫を追加するときに品目に原価を追加できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-121">When you use an inventory adjustment journal, you can add cost to an item when you add inventory.</span></span> <span data-ttu-id="6985e-122">追加の原価は、品目グループの転記プロファイルの設定に基づいて特定の総勘定元帳勘定に自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="6985e-122">The additional cost is automatically posted to a specific general ledger account, based on the setup of the item group posting profile.</span></span> <span data-ttu-id="6985e-123">品目が既定の総勘定元帳の相手勘定を保持する必要がある場合に在庫数量に対する損益を更新するために、この在庫仕訳帳タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="6985e-123">Use this inventory journal type to update gains and losses to inventory quantities when the item should keep its default general ledger offset account.</span></span> <span data-ttu-id="6985e-124">在庫調整仕訳帳を転記すると、在庫入庫または払出が転記され、在庫金額が変更され、元帳トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6985e-124">When you post an inventory adjustment journal, an inventory receipt or issue is posted, the inventory values are changed, and ledger transactions are created.</span></span>

### <a name="transfer"></a><span data-ttu-id="6985e-125">移動</span><span class="sxs-lookup"><span data-stu-id="6985e-125">Transfer</span></span>

<span data-ttu-id="6985e-126">原価の意味を関連付けずに、場所別在庫、バッチ、または製品バリアント間で品目を移動するために移動仕訳帳を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-126">You can use transfer journals to transfer items between stocking locations, batches, or product variants without associating any cost implications.</span></span> <span data-ttu-id="6985e-127">たとえば、ある倉庫から同じ会社内の別の倉庫に品目を移動できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-127">For example, you can transfer items from one warehouse to another warehouse within the same company.</span></span> <span data-ttu-id="6985e-128">移動仕訳帳を使用する場合、「開始」在庫分析コードと「終了」在庫分析コードの両方を指定する必要があります (たとえば、サイトと倉庫の場合)。</span><span class="sxs-lookup"><span data-stu-id="6985e-128">When you use a transfer journal, you must specify both the "from" and "to" inventory dimensions (for example, for Site and Warehouse).</span></span> <span data-ttu-id="6985e-129">定義した在庫分析コードの手持在庫が、それに応じて変更されます。</span><span class="sxs-lookup"><span data-stu-id="6985e-129">The on-hand inventory for the defined inventory dimensions is changed accordingly.</span></span> <span data-ttu-id="6985e-130">在庫移動は、材料の移動を即時で反映します。</span><span class="sxs-lookup"><span data-stu-id="6985e-130">Inventory transfers reflect the immediate movement of material.</span></span> <span data-ttu-id="6985e-131">輸送中在庫は追跡されません。</span><span class="sxs-lookup"><span data-stu-id="6985e-131">In-transit inventory isn't tracked.</span></span> <span data-ttu-id="6985e-132">輸送中在庫を追跡する必要がある場合、代わりに移動オーダーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6985e-132">If in-transit inventory must be tracked, you should use a transfer order instead.</span></span> <span data-ttu-id="6985e-133">振替仕訳帳を転記する場合、各仕訳帳明細行につき、2 つの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6985e-133">When you post a transfer journal, two inventory transactions are created for each journal line:</span></span>

-   <span data-ttu-id="6985e-134">「移動元」の場所での在庫払出</span><span class="sxs-lookup"><span data-stu-id="6985e-134">An inventory issue at the "from" location</span></span>
-   <span data-ttu-id="6985e-135">「移動先」の場所での在庫入庫</span><span class="sxs-lookup"><span data-stu-id="6985e-135">An inventory receipt at the "to" location</span></span>

### <a name="bom"></a><span data-ttu-id="6985e-136">BOM</span><span class="sxs-lookup"><span data-stu-id="6985e-136">BOM</span></span>

<span data-ttu-id="6985e-137">BOM を完了済と報告する場合、BOM 仕訳帳を作成できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-137">When you report a BOM as finished, you can create a BOM journal.</span></span> <span data-ttu-id="6985e-138">BOM 仕訳帳を使用して、BOM を直接転記できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-138">By using a BOM journal, you can post the BOM directly.</span></span> <span data-ttu-id="6985e-139">この転記は、関連付けられた BOM と BOMに含まれる製品の在庫払出とともに、製品の在庫入庫を生成します。</span><span class="sxs-lookup"><span data-stu-id="6985e-139">This posting generates an inventory receipt of the product, together with an associated BOM and an inventory issue of the products that are included in the BOM.</span></span> <span data-ttu-id="6985e-140">この在庫仕訳帳のタイプは、工順が必要ではない場合に単純かつ大量の生産シナリオに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6985e-140">This inventory journal type is useful in simple or high-volume production scenarios where routes aren't required.</span></span>

### <a name="item-arrival"></a><span data-ttu-id="6985e-141">品目到着</span><span class="sxs-lookup"><span data-stu-id="6985e-141">Item arrival</span></span>

<span data-ttu-id="6985e-142">着荷仕訳帳を使用して、品目の入庫を登録することができます (たとえば、発注書から)。</span><span class="sxs-lookup"><span data-stu-id="6985e-142">You can use the item arrival journal to register the receipt of items (for example, from purchase orders).</span></span> <span data-ttu-id="6985e-143">着荷仕訳帳は、**着荷の概要**ページから着荷管理の一部として作成するか、**品目到着**ページから手動で仕訳入力を作成できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-143">An item arrival journal can be created as part of arrival management from the **Arrival overview** page, or you can manually create a journal entry from the **Item arrival** page.</span></span> <span data-ttu-id="6985e-144">着荷仕訳帳名を有効にしてピッキング場所を確認する場合、Finance and Operations は受け取った品目の場所を検索し、スペースがある場合、受入品目の行先の場所を生成します。</span><span class="sxs-lookup"><span data-stu-id="6985e-144">If you enable the item arrival journal name to check for picking locations, Finance and Operations looks for a location for received items and, if there is room, generates location destinations for the incoming items.</span></span>

### <a name="production-input"></a><span data-ttu-id="6985e-145">生産入力</span><span class="sxs-lookup"><span data-stu-id="6985e-145">Production input</span></span>

<span data-ttu-id="6985e-146">生産入力仕訳帳は、着荷仕訳帳のように機能しますが、製造オーダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="6985e-146">Production input journals work like the item arrival journals but are used for production orders.</span></span>

### <a name="counting"></a><span data-ttu-id="6985e-147">棚卸</span><span class="sxs-lookup"><span data-stu-id="6985e-147">Counting</span></span>

<span data-ttu-id="6985e-148">棚卸仕訳帳によって、品目や品目グループに登録される現在の手持在庫を修正でき、実際の現物棚卸を転記して、差を調整するために必要な調整を行えます。</span><span class="sxs-lookup"><span data-stu-id="6985e-148">Counting journals let you correct the current on-hand inventory that is registered for items or groups of items, and then post the actual physical count, so that you can make the adjustments that are required in order to reconcile the differences.</span></span> <span data-ttu-id="6985e-149">さまざまな特性を持つ品目を棚卸仕訳帳に含められるように、棚卸ポリシーを棚卸グループと関連付けて、これらの品目をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-149">You can associate counting policies with counting groups to help group items that have various characteristics, so that those items can be included in a counting journal.</span></span> <span data-ttu-id="6985e-150">たとえば、棚卸グループを設定して、特定の頻度を持つ品目の棚卸や、在庫が特定のレベルまで落ちた場合の品目の棚卸が可能です。</span><span class="sxs-lookup"><span data-stu-id="6985e-150">For example, you can set up counting groups to count items that have a specific frequency, or to count items when stock falls to a particular level.</span></span> <span data-ttu-id="6985e-151">棚卸グループを定義する方法の詳細については、「[在庫棚卸プロセスの定義 (タスク ガイド)](tasks/define-inventory-counting-processes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6985e-151">For information about how to define counting groups, see [Define inventory counting processes (Task guide)](tasks/define-inventory-counting-processes.md).</span></span>

### <a name="tag-counting"></a><span data-ttu-id="6985e-152">タグ棚卸</span><span class="sxs-lookup"><span data-stu-id="6985e-152">Tag counting</span></span>

<span data-ttu-id="6985e-153">タグ棚卸仕訳帳は、番号を付けられたタグをロット番号に割り当てるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6985e-153">Tag counting journals are used to assign a numbered tag to a count lot.</span></span> <span data-ttu-id="6985e-154">タグには、タグ番号、品目番号と品目数量を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6985e-154">The tag should contain a tag number, item number, and item quantity.</span></span> <span data-ttu-id="6985e-155">タグが 1 回だけ使用され、すべてのタグが使用されていることを保証するには、固有の番号順序を持つタグの一意のセットが、すべての品目番号に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="6985e-155">To help guarantee that a tag is used only one time, and that all tags are used, every item number should have a unique set of tags that has its own number sequence.</span></span> <span data-ttu-id="6985e-156">3 つのステータス値を各タグに設定できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-156">Three status values can be set for each tag:</span></span>

-   <span data-ttu-id="6985e-157">**使用済** – このタグで棚卸が行われた品目番号。</span><span class="sxs-lookup"><span data-stu-id="6985e-157">**Used** – The item number is counted for this tag.</span></span>
-   <span data-ttu-id="6985e-158">**無効** – このタグで無効にされた品目番号。</span><span class="sxs-lookup"><span data-stu-id="6985e-158">**Voided** – The item number is voided for this tag.</span></span>
-   <span data-ttu-id="6985e-159">**なし** – このタグで品目番号がないもの。</span><span class="sxs-lookup"><span data-stu-id="6985e-159">**Missing** – The item number is missing for this tag.</span></span>

<span data-ttu-id="6985e-160">タグ棚卸仕訳帳を転記すると、タグ棚卸仕訳帳明細行に基づいて新しい棚卸仕訳帳が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6985e-160">When you post a tag counting journal, a new counting journal is created, based on the tag counting journal lines.</span></span> <span data-ttu-id="6985e-161">タグ棚卸に関する詳細については、「[在庫タグ棚卸](inventory-tag-counting.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6985e-161">For more information about tag counting, see [Inventory tag counting](inventory-tag-counting.md).</span></span>

## <a name="working-with-journals"></a><span data-ttu-id="6985e-162">仕訳帳の使用</span><span class="sxs-lookup"><span data-stu-id="6985e-162">Working with journals</span></span>
<span data-ttu-id="6985e-163">仕訳帳明細行には、一度に 1 人のユーザーのみがアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6985e-163">A journal can be accessed by only one user at a time.</span></span> <span data-ttu-id="6985e-164">仕訳帳明細行を作成するために複数のユーザーが仕訳帳に同時にアクセスする必要がある場合、これらのユーザーは情報の上書きを回避するために現在使用されていない仕訳帳を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6985e-164">If several users must access journals at the same time to create journal lines, those users must select journals that aren't currently being used, to prevent information from being overwritten.</span></span> <span data-ttu-id="6985e-165">複数の部門が同じ仕訳帳タイプを使用する状況では、複数の仕訳帳名 (たとえば、部門ごとに 1 つ) を作成すると便利です。</span><span class="sxs-lookup"><span data-stu-id="6985e-165">In situations where multiple departments use the same journal type, it's helpful to create multiple journal names (for example, one per department).</span></span> <span data-ttu-id="6985e-166">また、各転記ルーティンがそれぞれ固有の在庫仕訳帳に入力されるように仕訳帳を分割しておくと便利です。</span><span class="sxs-lookup"><span data-stu-id="6985e-166">It can also be helpful to divide journals so that each posting routine is entered in its own unique inventory journal.</span></span> <span data-ttu-id="6985e-167">在庫トランザクションに関連付けれられた転記ルーティンについて、定期的な在庫調整用の仕訳帳と、棚卸用の別の仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="6985e-167">For posting routines that are associated with inventory transactions, create one journal for periodic inventory adjustments and another for inventory counting.</span></span>

## <a name="posting-journal-lines"></a><span data-ttu-id="6985e-168">仕訳帳明細行の転記</span><span class="sxs-lookup"><span data-stu-id="6985e-168">Posting journal lines</span></span>
<span data-ttu-id="6985e-169">追加トランザクションから品目をロックするまで、作成した仕訳帳明細行をいつでも転記できます。</span><span class="sxs-lookup"><span data-stu-id="6985e-169">You can post the journal lines that you create at any time until you've locked an item from additional transactions.</span></span> <span data-ttu-id="6985e-170">明細行を転記せずに仕訳帳を閉じても、仕訳帳に入力したデータはその仕訳帳にそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="6985e-170">The data that you enter in a journal remains in that journal, even if you close the journal without posting the lines.</span></span>

