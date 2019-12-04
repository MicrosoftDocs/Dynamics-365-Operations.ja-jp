---
title: 在庫仕訳帳
description: このトピックでは、在庫仕訳帳を使用してさまざまなタイプの物理在庫トランザクションを転記する方法について説明します。
author: perlynne
manager: AnnBe
ms.date: 04/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6774a41887e74bfdb1fa6a9221264b0c8454c70
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814355"
---
# <a name="inventory-journals"></a><span data-ttu-id="cddef-103">在庫仕訳帳</span><span class="sxs-lookup"><span data-stu-id="cddef-103">Inventory journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cddef-104">このトピックでは、在庫仕訳帳を使用してさまざまなタイプの物理在庫トランザクションを転記する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cddef-104">This topic describes how you can use inventory journals to post various types of physical inventory transactions.</span></span>

<span data-ttu-id="cddef-105">Supply Chain Management の在庫仕訳帳は、払出と入荷の転記、在庫移動、部品表 (BOM) の作成、現物在庫の調整など、さまざまなタイプの現物在庫トランザクション転記に使用されます。</span><span class="sxs-lookup"><span data-stu-id="cddef-105">The inventory journals in Supply Chain Management are used to post physical inventory transactions of various types, such as the posting of issues and receipts, inventory movements, the creation of bills of materials (BOMs), and the reconciliation of physical inventory.</span></span> <span data-ttu-id="cddef-106">これらの在庫仕訳帳はすべて同様の方法で使用されますが、異なるタイプに分類されます。</span><span class="sxs-lookup"><span data-stu-id="cddef-106">All these inventory journals are used in a similar way, but they are divided into different types.</span></span>

## <a name="types-of-inventory-journals"></a><span data-ttu-id="cddef-107">在庫仕訳帳のタイプ</span><span class="sxs-lookup"><span data-stu-id="cddef-107">Types of inventory journals</span></span>
<span data-ttu-id="cddef-108">次の在庫仕訳帳タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-108">The following types of inventory journals are available:</span></span>

-   <span data-ttu-id="cddef-109">移動</span><span class="sxs-lookup"><span data-stu-id="cddef-109">Movement</span></span>
-   <span data-ttu-id="cddef-110">在庫調整</span><span class="sxs-lookup"><span data-stu-id="cddef-110">Inventory adjustment</span></span>
-   <span data-ttu-id="cddef-111">移動</span><span class="sxs-lookup"><span data-stu-id="cddef-111">Transfer</span></span>
-   <span data-ttu-id="cddef-112">BOM</span><span class="sxs-lookup"><span data-stu-id="cddef-112">BOM</span></span>
-   <span data-ttu-id="cddef-113">品目到着</span><span class="sxs-lookup"><span data-stu-id="cddef-113">Item arrival</span></span>
-   <span data-ttu-id="cddef-114">生産入力</span><span class="sxs-lookup"><span data-stu-id="cddef-114">Production input</span></span>
-   <span data-ttu-id="cddef-115">棚卸</span><span class="sxs-lookup"><span data-stu-id="cddef-115">Counting</span></span>
-   <span data-ttu-id="cddef-116">タグ棚卸</span><span class="sxs-lookup"><span data-stu-id="cddef-116">Tag counting</span></span>

### <a name="movement"></a><span data-ttu-id="cddef-117">移動</span><span class="sxs-lookup"><span data-stu-id="cddef-117">Movement</span></span>

<span data-ttu-id="cddef-118">在庫移動仕訳帳を使用している場合、在庫を追加するときに品目に原価を追加できますが、仕訳帳を作成するときに総勘定元帳の相手勘定を指定して、特定の総勘定元帳勘定に追加の原価を手動で割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cddef-118">When you use an inventory movement journal, you can add cost to an item when you add inventory, but you must manually allocate the additional cost to a particular general ledger account by specifying a general ledger offset account when you create the journal.</span></span> <span data-ttu-id="cddef-119">この在庫仕訳帳タイプは、既定の転記勘定を上書きするのに役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="cddef-119">This inventory journal type is useful if you want to overwrite the default posting accounts.</span></span>

### <a name="inventory-adjustment"></a><span data-ttu-id="cddef-120">在庫調整</span><span class="sxs-lookup"><span data-stu-id="cddef-120">Inventory adjustment</span></span>

<span data-ttu-id="cddef-121">在庫調整仕訳帳を使用している場合、在庫を追加するときに品目に原価を追加できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-121">When you use an inventory adjustment journal, you can add cost to an item when you add inventory.</span></span> <span data-ttu-id="cddef-122">追加の原価は、品目グループの転記プロファイルの設定に基づいて特定の総勘定元帳勘定に自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="cddef-122">The additional cost is automatically posted to a specific general ledger account, based on the setup of the item group posting profile.</span></span> <span data-ttu-id="cddef-123">品目が既定の総勘定元帳の相手勘定を保持する必要がある場合に在庫数量に対する損益を更新するために、この在庫仕訳帳タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="cddef-123">Use this inventory journal type to update gains and losses to inventory quantities when the item should keep its default general ledger offset account.</span></span> <span data-ttu-id="cddef-124">在庫調整仕訳帳を転記すると、在庫入庫または払出が転記され、在庫金額が変更され、元帳トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="cddef-124">When you post an inventory adjustment journal, an inventory receipt or issue is posted, the inventory values are changed, and ledger transactions are created.</span></span>

### <a name="transfer"></a><span data-ttu-id="cddef-125">移動</span><span class="sxs-lookup"><span data-stu-id="cddef-125">Transfer</span></span>

<span data-ttu-id="cddef-126">原価の意味を関連付けずに、場所別在庫、バッチ、または製品バリアント間で品目を移動するために移動仕訳帳を使用できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-126">You can use transfer journals to transfer items between stocking locations, batches, or product variants without associating any cost implications.</span></span> <span data-ttu-id="cddef-127">たとえば、ある倉庫から同じ会社内の別の倉庫に品目を移動できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-127">For example, you can transfer items from one warehouse to another warehouse within the same company.</span></span> <span data-ttu-id="cddef-128">移動仕訳帳を使用する場合、「開始」在庫分析コードと「終了」在庫分析コードの両方を指定する必要があります (たとえば、サイトと倉庫の場合)。</span><span class="sxs-lookup"><span data-stu-id="cddef-128">When you use a transfer journal, you must specify both the "from" and "to" inventory dimensions (for example, for Site and Warehouse).</span></span> <span data-ttu-id="cddef-129">定義した在庫分析コードの手持在庫が、それに応じて変更されます。</span><span class="sxs-lookup"><span data-stu-id="cddef-129">The on-hand inventory for the defined inventory dimensions is changed accordingly.</span></span> <span data-ttu-id="cddef-130">在庫移動は、材料の移動を即時で反映します。</span><span class="sxs-lookup"><span data-stu-id="cddef-130">Inventory transfers reflect the immediate movement of material.</span></span> <span data-ttu-id="cddef-131">輸送中在庫は追跡されません。</span><span class="sxs-lookup"><span data-stu-id="cddef-131">In-transit inventory isn't tracked.</span></span> <span data-ttu-id="cddef-132">輸送中在庫を追跡する必要がある場合、代わりに移動オーダーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cddef-132">If in-transit inventory must be tracked, you should use a transfer order instead.</span></span> <span data-ttu-id="cddef-133">振替仕訳帳を転記する場合、各仕訳帳明細行につき、2 つの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="cddef-133">When you post a transfer journal, two inventory transactions are created for each journal line:</span></span>

-   <span data-ttu-id="cddef-134">「移動元」の場所での在庫払出。</span><span class="sxs-lookup"><span data-stu-id="cddef-134">An inventory issue at the "from" location.</span></span>
-   <span data-ttu-id="cddef-135">「移動先」の場所での在庫入庫。</span><span class="sxs-lookup"><span data-stu-id="cddef-135">An inventory receipt at the "to" location.</span></span>

### <a name="bom"></a><span data-ttu-id="cddef-136">BOM</span><span class="sxs-lookup"><span data-stu-id="cddef-136">BOM</span></span>

<span data-ttu-id="cddef-137">BOM を完了済と報告する場合、BOM 仕訳帳を作成できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-137">When you report a BOM as finished, you can create a BOM journal.</span></span> <span data-ttu-id="cddef-138">BOM 仕訳帳を使用して、BOM を直接転記できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-138">By using a BOM journal, you can post the BOM directly.</span></span> <span data-ttu-id="cddef-139">この転記は、関連付けられた BOM と BOMに含まれる製品の在庫払出とともに、製品の在庫入庫を生成します。</span><span class="sxs-lookup"><span data-stu-id="cddef-139">This posting generates an inventory receipt of the product, together with an associated BOM and an inventory issue of the products that are included in the BOM.</span></span> <span data-ttu-id="cddef-140">この在庫仕訳帳のタイプは、工順が必要ではない場合に単純かつ大量の生産シナリオに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cddef-140">This inventory journal type is useful in simple or high-volume production scenarios where routes aren't required.</span></span>

### <a name="item-arrival"></a><span data-ttu-id="cddef-141">品目到着</span><span class="sxs-lookup"><span data-stu-id="cddef-141">Item arrival</span></span>

<span data-ttu-id="cddef-142">着荷仕訳帳を使用して、品目の入庫を登録することができます (たとえば、発注書から)。</span><span class="sxs-lookup"><span data-stu-id="cddef-142">You can use the item arrival journal to register the receipt of items (for example, from purchase orders).</span></span> <span data-ttu-id="cddef-143">着荷仕訳帳は、**着荷の概要**ページから着荷管理の一部として作成するか、**品目到着**ページから手動で仕訳入力を作成できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-143">An item arrival journal can be created as part of arrival management from the **Arrival overview** page, or you can manually create a journal entry from the **Item arrival** page.</span></span> <span data-ttu-id="cddef-144">着荷仕訳帳名を有効にしてピッキング場所を確認する場合、Supply Chain Management は受け取った品目の場所を検索し、スペースがある場合、受入品目の行先の場所を生成します。</span><span class="sxs-lookup"><span data-stu-id="cddef-144">If you enable the item arrival journal name to check for picking locations, Supply Chain Management looks for a location for received items and, if there is room, generates location destinations for the incoming items.</span></span>

### <a name="production-input"></a><span data-ttu-id="cddef-145">生産入力</span><span class="sxs-lookup"><span data-stu-id="cddef-145">Production input</span></span>

<span data-ttu-id="cddef-146">生産入力仕訳帳は、着荷仕訳帳のように機能しますが、製造オーダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="cddef-146">Production input journals work like the item arrival journals but are used for production orders.</span></span>

### <a name="counting"></a><span data-ttu-id="cddef-147">棚卸</span><span class="sxs-lookup"><span data-stu-id="cddef-147">Counting</span></span>

<span data-ttu-id="cddef-148">棚卸仕訳帳によって、品目や品目グループに登録される現在の手持在庫を修正でき、実際の現物棚卸を転記して、差を調整するために必要な調整を行えます。</span><span class="sxs-lookup"><span data-stu-id="cddef-148">Counting journals let you correct the current on-hand inventory that is registered for items or groups of items, and then post the actual physical count, so that you can make the adjustments that are required to reconcile the differences.</span></span> <span data-ttu-id="cddef-149">さまざまな特性を持つ品目を棚卸仕訳帳に含められるように、棚卸ポリシーを棚卸グループと関連付けて、これらの品目をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-149">You can associate counting policies with counting groups to help group items that have various characteristics, so that those items can be included in a counting journal.</span></span> <span data-ttu-id="cddef-150">たとえば、棚卸グループを設定して、特定の頻度を持つ品目の棚卸や、在庫が特定のレベルまで落ちた場合の品目の棚卸が可能です。</span><span class="sxs-lookup"><span data-stu-id="cddef-150">For example, you can set up counting groups to count items that have a specific frequency, or to count items when stock falls to a particular level.</span></span> <span data-ttu-id="cddef-151">棚卸グループを定義する方法の詳細については、「[在庫棚卸プロセスの定義](tasks/define-inventory-counting-processes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cddef-151">For information about how to define counting groups, see [Define inventory counting processes](tasks/define-inventory-counting-processes.md).</span></span>

### <a name="tag-counting"></a><span data-ttu-id="cddef-152">タグ棚卸</span><span class="sxs-lookup"><span data-stu-id="cddef-152">Tag counting</span></span>

<span data-ttu-id="cddef-153">タグ棚卸仕訳帳は、番号を付けられたタグをロット番号に割り当てるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cddef-153">Tag counting journals are used to assign a numbered tag to a count lot.</span></span> <span data-ttu-id="cddef-154">タグには、タグ番号、品目番号と品目数量を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="cddef-154">The tag should contain a tag number, item number, and item quantity.</span></span> <span data-ttu-id="cddef-155">タグが 1 回だけ使用され、すべてのタグが使用されていることを確認するには、固有の番号順序を持つタグの一意のセットが、すべての品目番号に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="cddef-155">To ensure that a tag is used only one time, and that all tags are used, every item number should have a unique set of tags that has its own number sequence.</span></span> <span data-ttu-id="cddef-156">3 つのステータス値を各タグに設定できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-156">Three status values can be set for each tag:</span></span>

-   <span data-ttu-id="cddef-157">**使用済** – このタグで棚卸が行われた品目番号。</span><span class="sxs-lookup"><span data-stu-id="cddef-157">**Used** – The item number is counted for this tag.</span></span>
-   <span data-ttu-id="cddef-158">**無効** – このタグで無効にされた品目番号。</span><span class="sxs-lookup"><span data-stu-id="cddef-158">**Voided** – The item number is voided for this tag.</span></span>
-   <span data-ttu-id="cddef-159">**なし** – このタグで品目番号がないもの。</span><span class="sxs-lookup"><span data-stu-id="cddef-159">**Missing** – The item number is missing for this tag.</span></span>

<span data-ttu-id="cddef-160">タグ棚卸仕訳帳を転記すると、タグ棚卸仕訳帳明細行に基づいて新しい棚卸仕訳帳が作成されます。</span><span class="sxs-lookup"><span data-stu-id="cddef-160">When you post a tag counting journal, a new counting journal is created, based on the tag counting journal lines.</span></span> <span data-ttu-id="cddef-161">タグ棚卸に関する詳細については、「[在庫タグ棚卸](inventory-tag-counting.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cddef-161">For more information about tag counting, see [Inventory tag counting](inventory-tag-counting.md).</span></span>

## <a name="working-with-journals"></a><span data-ttu-id="cddef-162">仕訳帳の使用</span><span class="sxs-lookup"><span data-stu-id="cddef-162">Working with journals</span></span>
<span data-ttu-id="cddef-163">仕訳帳明細行には、一度に 1 人のユーザーのみがアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="cddef-163">A journal can be accessed by only one user at a time.</span></span> <span data-ttu-id="cddef-164">仕訳帳明細行を作成するために複数のユーザーが仕訳帳に同時にアクセスする必要がある場合、これらのユーザーは情報の上書きを回避するために現在使用されていない仕訳帳を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cddef-164">If several users must access journals at the same time to create journal lines, those users must select journals that aren't currently being used, to prevent information from being overwritten.</span></span> <span data-ttu-id="cddef-165">複数の部門が同じ仕訳帳タイプを使用する状況では、複数の仕訳帳名 (たとえば、部門ごとに 1 つ) を作成すると便利です。</span><span class="sxs-lookup"><span data-stu-id="cddef-165">In situations where multiple departments use the same journal type, it's helpful to create multiple journal names (for example, one per department).</span></span> <span data-ttu-id="cddef-166">また、各転記ルーティンがそれぞれ固有の在庫仕訳帳に入力されるように仕訳帳を分割しておくと便利です。</span><span class="sxs-lookup"><span data-stu-id="cddef-166">It can also be helpful to divide journals so that each posting routine is entered in its own unique inventory journal.</span></span> <span data-ttu-id="cddef-167">在庫トランザクションに関連付けれられた転記ルーティンについて、定期的な在庫調整用の仕訳帳と、棚卸用の別の仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="cddef-167">For posting routines that are associated with inventory transactions, create one journal for periodic inventory adjustments and another for inventory counting.</span></span>

## <a name="posting-journal-lines"></a><span data-ttu-id="cddef-168">仕訳帳明細行の転記</span><span class="sxs-lookup"><span data-stu-id="cddef-168">Posting journal lines</span></span>
<span data-ttu-id="cddef-169">追加トランザクションから品目をロックするまで、作成した仕訳帳明細行をいつでも転記できます。</span><span class="sxs-lookup"><span data-stu-id="cddef-169">You can post the journal lines that you create at any time until you've locked an item from additional transactions.</span></span> <span data-ttu-id="cddef-170">明細行を転記せずに仕訳帳を閉じても、仕訳帳に入力したデータはその仕訳帳にそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="cddef-170">The data that you enter in a journal remains in that journal, even if you close the journal without posting the lines.</span></span>

## <a name="data-entity-support-for-inventory-journals"></a><span data-ttu-id="cddef-171">在庫仕訳帳のデータ エンティティ サポート</span><span class="sxs-lookup"><span data-stu-id="cddef-171">Data entity support for inventory journals</span></span>

<span data-ttu-id="cddef-172">データ エンティティは、次のタイプの統合シナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="cddef-172">Data entities support the following types of integration scenarios:</span></span>
-    <span data-ttu-id="cddef-173">同期サービス (OData)</span><span class="sxs-lookup"><span data-stu-id="cddef-173">Synchronous service (OData)</span></span>
-  <span data-ttu-id="cddef-174">非同期の統合</span><span class="sxs-lookup"><span data-stu-id="cddef-174">Asynchronous integration</span></span>

<span data-ttu-id="cddef-175">詳細については、「[データ エンティティ](../../dev-itpro/data-entities/data-entities.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cddef-175">For more information, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

> [!NOTE]
> <span data-ttu-id="cddef-176">すべての在庫仕訳帳が OData 対応ではないため、Excel データ コネクタを使用してデータを発行し、更新し、Supply Chain Management に再インポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="cddef-176">Not all inventory journals are OData-enabled, therefore you cannot use the Excel data connector to get data published, updated, and imported back to Supply Chain Management.</span></span> 

<span data-ttu-id="cddef-177">仕訳帳データ エンティティ間の別の違いは、ヘッダーと明細行のデータの両方を含む複合エンティティを使用する機能です。</span><span class="sxs-lookup"><span data-stu-id="cddef-177">Another difference between the journal data entities is the ability to use composite entities that include both the header and line data.</span></span> <span data-ttu-id="cddef-178">現時点では、複合エンティティを以下のものに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cddef-178">Currently, you can use the composite entities for:</span></span>
-   <span data-ttu-id="cddef-179">在庫調整仕訳帳</span><span class="sxs-lookup"><span data-stu-id="cddef-179">Inventory adjustment journal</span></span>
-   <span data-ttu-id="cddef-180">在庫移動仕訳帳</span><span class="sxs-lookup"><span data-stu-id="cddef-180">Inventory movement journal</span></span>

<span data-ttu-id="cddef-181">これらの 2 つの在庫仕訳帳は *在庫の初期化* シナリオのみをデータ管理インポート プロジェクトの一部としてサポートします 。</span><span class="sxs-lookup"><span data-stu-id="cddef-181">These two inventory journals only support the *Initialize stock* scenario as part of a data management import project:</span></span>
-  <span data-ttu-id="cddef-182">仕訳帳ヘッダー番号が指定されていないが、仕訳帳タイプの番号順序が指定されている場合、インポート ジョブは 1000 明細行ごとの仕訳帳ヘッダーを自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="cddef-182">When a journal header number is not specified, but a number sequence is specified for the journal type, the import job will automatically create journal headers per 1000 lines.</span></span> <span data-ttu-id="cddef-183">たとえば、2020 明細行をインポートすると、次の 3 つの仕訳帳ヘッダーとなります。</span><span class="sxs-lookup"><span data-stu-id="cddef-183">For example, importing 2020 lines will result in the following three journal headers:</span></span>
    -  <span data-ttu-id="cddef-184">ヘッダー 1: 1000 明細行を含みます</span><span class="sxs-lookup"><span data-stu-id="cddef-184">Header 1: will contain 1000 lines</span></span>
    -  <span data-ttu-id="cddef-185">ヘッダー 2: 1000 明細行を含みます</span><span class="sxs-lookup"><span data-stu-id="cddef-185">Header 2: will contain 1000 lines</span></span>
    -  <span data-ttu-id="cddef-186">ヘッダー 3: 20 明細行を含みます</span><span class="sxs-lookup"><span data-stu-id="cddef-186">Header 3: will contain 20 lines</span></span>
-  <span data-ttu-id="cddef-187">在庫分析コードごとに固有の明細行情報が存在することが前提となり、それは製品、保管、および追跡用分析コードである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cddef-187">It is assumed that unique line information exists per inventory dimension, which can be a product, storage, and tracking dimension.</span></span> <span data-ttu-id="cddef-188">したがって、同じインポート プロジェクト内で明細行の日付フィールドのみが異なる、仕訳帳明細行をインポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="cddef-188">Therefore, it’s not possible to import journal lines where only the date field differs on the lines within the same import project.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cddef-189">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="cddef-189">Additional resources</span></span>

[<span data-ttu-id="cddef-190">データ エンティティ</span><span class="sxs-lookup"><span data-stu-id="cddef-190">Data entities</span></span>](../../dev-itpro/data-entities/data-entities.md)
