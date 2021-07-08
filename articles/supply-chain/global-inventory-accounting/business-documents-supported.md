---
title: グローバル在庫会計でサポートされるビジネス ドキュメント
description: このトピックでは、グローバル在庫会計でサポートされるビジネス ドキュメントの一覧を示します。 また、発注書ドキュメントの詳細例も提供します。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 311c894d709985d0d053b0ec3a317142aa582c39
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273187"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a><span data-ttu-id="225e0-104">グローバル在庫会計でサポートされるビジネス ドキュメント</span><span class="sxs-lookup"><span data-stu-id="225e0-104">Business documents supported by Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="225e0-105">グローバル在庫会計アドインが完全に設定された後、Microsoft Dynamics 365 Supply Chain Management に入力されている在庫関連のドキュメントを処理できます。</span><span class="sxs-lookup"><span data-stu-id="225e0-105">After the Global Inventory Accounting Add-in is fully set up, it's ready to process inventory-related documents that are entered in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="supported-business-documents"></a><span data-ttu-id="225e0-106">サポートされたビジネス ドキュメント</span><span class="sxs-lookup"><span data-stu-id="225e0-106">Supported business documents</span></span>

<span data-ttu-id="225e0-107">ビジネス ドキュメントには 2 つの種類があります。</span><span class="sxs-lookup"><span data-stu-id="225e0-107">There are two types of business documents:</span></span>

- <span data-ttu-id="225e0-108">**仕訳帳が作成されているドキュメント** – これらのドキュメントには、製品受領書、購買請求書、梱包明細、および売上請求書のドキュメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="225e0-108">**Documents that have a journal** – These documents include product receipt, purchase invoice, packing slip, and sales invoice documents.</span></span>
- <span data-ttu-id="225e0-109">**仕訳帳が作成されていないドキュメント** – これらのドキュメントには、棚卸、移動、および在庫調整のドキュメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="225e0-109">**Documents that don't have a journal** – These documents include counting, movement, and inventory adjustment documents.</span></span>

<span data-ttu-id="225e0-110">このトピックでは、プロセスを示す例として発注書を使用します。</span><span class="sxs-lookup"><span data-stu-id="225e0-110">Later in this topic, purchase orders will be used as an example to illustrate the process.</span></span>

<span data-ttu-id="225e0-111">次の表に、現在のリリースでサポートされているドキュメントの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="225e0-111">The following table lists the documents that the current release supports.</span></span>

| <span data-ttu-id="225e0-112">文書種類</span><span class="sxs-lookup"><span data-stu-id="225e0-112">Document type</span></span>      | <span data-ttu-id="225e0-113">伝票</span><span class="sxs-lookup"><span data-stu-id="225e0-113">Document</span></span>        |
|--------------------|-----------------|
| <span data-ttu-id="225e0-114">発注書</span><span class="sxs-lookup"><span data-stu-id="225e0-114">Purchase Order</span></span>     | <span data-ttu-id="225e0-115">製品受領書</span><span class="sxs-lookup"><span data-stu-id="225e0-115">Product Receipt</span></span> |
| <span data-ttu-id="225e0-116">発注書</span><span class="sxs-lookup"><span data-stu-id="225e0-116">Purchase Order</span></span>     | <span data-ttu-id="225e0-117">請求書</span><span class="sxs-lookup"><span data-stu-id="225e0-117">Invoice</span></span>         |
| <span data-ttu-id="225e0-118">販売注文</span><span class="sxs-lookup"><span data-stu-id="225e0-118">Sales Order</span></span>        | <span data-ttu-id="225e0-119">梱包明細</span><span class="sxs-lookup"><span data-stu-id="225e0-119">Packing slip</span></span>    |
| <span data-ttu-id="225e0-120">販売注文</span><span class="sxs-lookup"><span data-stu-id="225e0-120">Sales Order</span></span>        | <span data-ttu-id="225e0-121">請求書</span><span class="sxs-lookup"><span data-stu-id="225e0-121">Invoice</span></span>         |
| <span data-ttu-id="225e0-122">在庫仕訳帳</span><span class="sxs-lookup"><span data-stu-id="225e0-122">Inventory Journals</span></span> | <span data-ttu-id="225e0-123">振替</span><span class="sxs-lookup"><span data-stu-id="225e0-123">Movement</span></span>        |
| <span data-ttu-id="225e0-124">在庫仕訳帳</span><span class="sxs-lookup"><span data-stu-id="225e0-124">Inventory Journals</span></span> | <span data-ttu-id="225e0-125">調整</span><span class="sxs-lookup"><span data-stu-id="225e0-125">Adjustment</span></span>      |
| <span data-ttu-id="225e0-126">在庫仕訳帳</span><span class="sxs-lookup"><span data-stu-id="225e0-126">Inventory Journals</span></span> | <span data-ttu-id="225e0-127">棚卸</span><span class="sxs-lookup"><span data-stu-id="225e0-127">Counting</span></span>        |
| <span data-ttu-id="225e0-128">在庫仕訳帳</span><span class="sxs-lookup"><span data-stu-id="225e0-128">Inventory Journals</span></span> | <span data-ttu-id="225e0-129">譲渡</span><span class="sxs-lookup"><span data-stu-id="225e0-129">Transfer</span></span>        |
| <span data-ttu-id="225e0-130">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="225e0-130">Transfer Order</span></span>     | <span data-ttu-id="225e0-131">出荷</span><span class="sxs-lookup"><span data-stu-id="225e0-131">Shipment</span></span>        |
| <span data-ttu-id="225e0-132">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="225e0-132">Transfer Order</span></span>     | <span data-ttu-id="225e0-133">受入</span><span class="sxs-lookup"><span data-stu-id="225e0-133">Receive</span></span>         |

> [!IMPORTANT]
> <span data-ttu-id="225e0-134">グローバル在庫会計では、Supply Chain Management に入力されたドキュメントを非同期で処理します。</span><span class="sxs-lookup"><span data-stu-id="225e0-134">Global Inventory Accounting asynchronously processes the documents that are entered in Supply Chain Management.</span></span> <span data-ttu-id="225e0-135">問題のあるドキュメントに対するエラー メッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="225e0-135">No error messages will be shown for problematic documents.</span></span>

## <a name="example-purchase-order"></a><span data-ttu-id="225e0-136">例: 発注書</span><span class="sxs-lookup"><span data-stu-id="225e0-136">Example: Purchase order</span></span>

### <a name="product-receipt"></a><span data-ttu-id="225e0-137">製品受領書</span><span class="sxs-lookup"><span data-stu-id="225e0-137">Product receipt</span></span>

<span data-ttu-id="225e0-138">製品受領書を通常の方法で転記します。</span><span class="sxs-lookup"><span data-stu-id="225e0-138">Post product receipts in the usual way.</span></span> <span data-ttu-id="225e0-139">**全ての発注書** ページで発注書を選び、アクション ページの **受領** タブで、**製品受領書** を選び **製品受領書仕訳帳** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="225e0-139">On the **All purchase orders** page, select a purchase order, and then, on the Action Pane, on the **Receive** tab, select **Product receipt** to open the **Product receipt journal** page.</span></span> <span data-ttu-id="225e0-140">各行に対して、運用イベントおよびグローバル在庫会計イベントが生成されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-140">An operation event and a Global Invntroy Accounting event are generated for each line.</span></span> <span data-ttu-id="225e0-141">したがって、**行** タブで **在庫 \> イベントと測定** を選び **イベントと測定** ページを開きます。.</span><span class="sxs-lookup"><span data-stu-id="225e0-141">Therefore, select the **Lines** tab, and then select **Inventory \> Events and measurements** to open the **Events and measurements** page.</span></span>

<span data-ttu-id="225e0-142">グローバル在庫会計は、イベントと測定に基づく会計システムです。</span><span class="sxs-lookup"><span data-stu-id="225e0-142">Global Inventory Accounting is an accounting system that is based on events and measurements.</span></span> <span data-ttu-id="225e0-143">**イベントと測定** ページの測定ライン グリッドで測定一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-143">The measurement line grid on the **Events and measurements** page shows a list of measurements.</span></span> <span data-ttu-id="225e0-144">各測定には分析コードの一覧があります。</span><span class="sxs-lookup"><span data-stu-id="225e0-144">Each measurement has a list of dimensions.</span></span>

<span data-ttu-id="225e0-145">各操作イベントに対して、次の 2 種類の測定があります。</span><span class="sxs-lookup"><span data-stu-id="225e0-145">For each operation event, there are two types of measurement:</span></span>

- <span data-ttu-id="225e0-146">**操作測定** – これらの測定は、ビジネス ドキュメントを一般的な用語で表します。</span><span class="sxs-lookup"><span data-stu-id="225e0-146">**Operations measurements** – These measurements describe business documents in generic terms.</span></span> <span data-ttu-id="225e0-147">1 つの測定は、ドキュメントで使用される測定単位を使用する製品数量です。</span><span class="sxs-lookup"><span data-stu-id="225e0-147">One measurement is the product quantity using the unit of measure that is used in the document.</span></span> <span data-ttu-id="225e0-148">また、拡張価格、割引率、行の請求額など、在庫値に影響を与える測定があります。</span><span class="sxs-lookup"><span data-stu-id="225e0-148">There are also measurements that affect the inventory value, such as extended price, discount, discount percent, and line charge.</span></span>
- <span data-ttu-id="225e0-149">**リソース会計測定** – これらの測定は、在庫レジスターの視点から取得されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-149">**Resource accounting measurements** – These measurements are from the inventory register perspective.</span></span> <span data-ttu-id="225e0-150">在庫分析コードは、在庫単位での在庫に対するドキュメントの影響を説明します。</span><span class="sxs-lookup"><span data-stu-id="225e0-150">They describe the document's impact on the inventory in the inventory unit of measure.</span></span> <span data-ttu-id="225e0-151">複数の在庫登録がある場合には、リソース会計測定の複数行があります。</span><span class="sxs-lookup"><span data-stu-id="225e0-151">If there are multiple inventory registrations, there are multiple lines of resource accounting measurements.</span></span>

<span data-ttu-id="225e0-152">分析コードは、次の方法で整理されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-152">The dimensions are organized in the following way:</span></span>

- <span data-ttu-id="225e0-153">**二重性** – 二重性は、経済イベントに参加する担当者を表します。</span><span class="sxs-lookup"><span data-stu-id="225e0-153">**Duality** – Duality describes the agents who participate in the economic events.</span></span> <span data-ttu-id="225e0-154">外部のビジネス ドキュメントの場合は、文書が入力される法人を示し、二重分析コードは仕入先や顧客などについて説明します。</span><span class="sxs-lookup"><span data-stu-id="225e0-154">For external business documents, the primal dimensions describe the legal entity where the document is entered, whereas the dual dimensions describe the vendor, customer, and so on.</span></span> <span data-ttu-id="225e0-155">内部の業務ドキュメント (移動注文など) の場合、デュアル分析コードは倉庫を示します。</span><span class="sxs-lookup"><span data-stu-id="225e0-155">For internal business documents (for example, transfer orders), the dual dimensions describe the counterpart warehouse.</span></span>
- <span data-ttu-id="225e0-156">**分析コード タイプ** – 分析コード タイプによって分析コードが分類されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-156">**Dimension type** – Dimension types categorize the dimensions.</span></span>
- <span data-ttu-id="225e0-157">**分析コード** – 分析コードの名前。</span><span class="sxs-lookup"><span data-stu-id="225e0-157">**Dimension** – The name of the dimension.</span></span>
- <span data-ttu-id="225e0-158">**分析コード値** – 分析コードの値。</span><span class="sxs-lookup"><span data-stu-id="225e0-158">**Dimension value** – The value of the dimension.</span></span>

### <a name="global-inventory-accounting-event"></a><span data-ttu-id="225e0-159">グローバル在庫会計イベント</span><span class="sxs-lookup"><span data-stu-id="225e0-159">Global Inventory Accounting event</span></span>

<span data-ttu-id="225e0-160">グローバル在庫会計では、運用イベントおよび測定が入力として使用されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-160">Global Inventory Accounting takes the operational events and measurements as input.</span></span> <span data-ttu-id="225e0-161">関連付けられた通貨と規則に基づいて、関連する各元帳に対して適切な会計が実行されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-161">It then does the appropriate accounting for each related ledger, based on the attached currency and convention.</span></span> <span data-ttu-id="225e0-162">**グローバル在庫会計イベントおよび測定** を選択して、グローバル在庫会計イベントを表示できます。</span><span class="sxs-lookup"><span data-stu-id="225e0-162">You can select **Global inventory accounting events and measurements** to view the Global Inventory Accounting event.</span></span> <span data-ttu-id="225e0-163">グローバル在庫会計イベントは、運用イベントと同じ方法に従いますが、異なる測定を使用します。</span><span class="sxs-lookup"><span data-stu-id="225e0-163">The Global Inventory Accounting event follows the same methodology as operation events, but it uses different measurements.</span></span> <span data-ttu-id="225e0-164">測定タイプには、製品原価数量、製品原価、差異の 3 つの主要なタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="225e0-164">There are three major measurement types: product cost quantity, product cost, and variance.</span></span>

<span data-ttu-id="225e0-165">小計勘定は、測定をさらに分類するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-165">Subledger accounts are used to further classify the measurements.</span></span> <span data-ttu-id="225e0-166">複数の元帳が作成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="225e0-166">There might be multiple ledgers.</span></span> <span data-ttu-id="225e0-167">これらの元帳は、ドキュメントが入力される法人にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="225e0-167">These ledgers are linked to the legal entity where the document is entered.</span></span> <span data-ttu-id="225e0-168">**元帳** フィールドの値を変更することで、各元帳のイベントと測定値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="225e0-168">You can view the events and measurements for each ledger by changing the value of the **Ledger** field.</span></span>

### <a name="cost-element"></a><span data-ttu-id="225e0-169">原価要素</span><span class="sxs-lookup"><span data-stu-id="225e0-169">Cost element</span></span>

<span data-ttu-id="225e0-170">元帳に関連付けられた原価要素ポリシーに基づいて、システムは在庫原価に影響を与える各会計に関連付けられた運用イベント測定に、原価要素を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="225e0-170">Based on the cost element policy that is attached to the ledger, the system assigns a cost element to each accounted operation event measurement that affects the inventory cost.</span></span> <span data-ttu-id="225e0-171">これらの測定には、拡張価格、割引、割引率、および行費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="225e0-171">These measurements include extended price, discount, discount percent, and line charge.</span></span>

### <a name="measurement-line-details"></a><span data-ttu-id="225e0-172">測定明細行の詳細</span><span class="sxs-lookup"><span data-stu-id="225e0-172">Measurement line details</span></span>

<span data-ttu-id="225e0-173">**概要** タブには、関連付けられたポリシーの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-173">The **Overview** tab shows the details of the attached policies.</span></span> <span data-ttu-id="225e0-174">原価対象分析コードは、原価対象ポリシーに基づいて原価対象を表示します。</span><span class="sxs-lookup"><span data-stu-id="225e0-174">The cost object dimensions show the cost object, based on the cost object policy.</span></span> <span data-ttu-id="225e0-175">原価フローの前提条件が *特定 – バッチ* である場合、特定 ID 分析コードはバッチ番号を表示します。</span><span class="sxs-lookup"><span data-stu-id="225e0-175">Specific identification dimensions show the batch number if the cost flow assumption is *Specific – Batch*.</span></span>

### <a name="purchase-invoice"></a><span data-ttu-id="225e0-176">仕入請求書</span><span class="sxs-lookup"><span data-stu-id="225e0-176">Purchase invoice</span></span>

<span data-ttu-id="225e0-177">請求書を通常の方法で転記します。</span><span class="sxs-lookup"><span data-stu-id="225e0-177">Post the invoice in the usual way.</span></span> <span data-ttu-id="225e0-178">その後、アクション ウィンドウの **請求書** タブの **仕訳帳** グループで、**請求書** を選択して請求仕訳帳を開きます。</span><span class="sxs-lookup"><span data-stu-id="225e0-178">Then, on the Action Pane, on the **Invoice** tab, in the **Journals** group, select **Invoice** to open the invoice journal.</span></span> <span data-ttu-id="225e0-179">各行に対して、運用イベントおよびグローバル在庫会計イベントが生成されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-179">An operation event and a Global Inventory Accounting event are generated for each line.</span></span> <span data-ttu-id="225e0-180">したがって、**行** タブで **在庫 \> イベントと測定** を選び **イベントと測定** ページを開きます。.</span><span class="sxs-lookup"><span data-stu-id="225e0-180">Therefore, select the **Lines** tab, and then select **Inventory \> Events and measurements** to open the **Events and measurements** page.</span></span> <span data-ttu-id="225e0-181">**イベントと測定** ページには、同じ測定タイプが表示されます。</span><span class="sxs-lookup"><span data-stu-id="225e0-181">The **Events and measurements** page shows the same measure type.</span></span> <span data-ttu-id="225e0-182">ただし、このページにはメジャー ロールとメジャー モディファイアーが表示される場合があるので、代理店 (法人) に対する影響は異なります。</span><span class="sxs-lookup"><span data-stu-id="225e0-182">However, because the page shows a different measure role and measure modifier, the impact on the agent (legal entity) differs.</span></span>

<span data-ttu-id="225e0-183">**グローバル在庫会計イベントおよび測定** を選択して、グローバル在庫会計イベントを表示できます。</span><span class="sxs-lookup"><span data-stu-id="225e0-183">Select **Global inventory accounting events and measurements** to view the Global Inventory Accounting event.</span></span> <span data-ttu-id="225e0-184">この場合、在庫数量と原価は、*請求されていない在庫を受け取った商品* の補助勘定科目から、*購入済商品の原価* の補助勘定科目にフローされます。</span><span class="sxs-lookup"><span data-stu-id="225e0-184">The inventory quantity and cost now flow out from the *Goods received not invoiced inventory* subledger account and into the *Cost of goods purchased* subledger account.</span></span>
