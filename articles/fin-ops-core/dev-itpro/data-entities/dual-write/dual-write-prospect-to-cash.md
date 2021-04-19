---
title: 二重書き込みの見込顧客を現金化
description: このトピックでは、二重書き込みの見込顧客を現金化に関する情報を提供します。
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 33ed1c7f69fa92bbd123042a139dd8fd0ee3e73a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754091"
---
# <a name="prospect-to-cash-in-dual-write"></a><span data-ttu-id="6520a-103">二重書き込みの見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="6520a-103">Prospect-to-cash in dual-write</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="6520a-104">ほとんどの企業にとって重要な目標は、見込顧客を顧客に変換し、その顧客との継続的な取引関係を維持することです。</span><span class="sxs-lookup"><span data-stu-id="6520a-104">An important goal of most businesses is to convert prospects to customers and then maintain an ongoing business relationship with those customers.</span></span> <span data-ttu-id="6520a-105">Microsoft Dynamics 365 アプリでは、見込顧客を現金化のプロセスが見積または注文処理のワークフローで行われ、財務の調整と認識が行われます。</span><span class="sxs-lookup"><span data-stu-id="6520a-105">In Microsoft Dynamics 365 apps, the prospect-to-cash process occurs through quotations or order processing workflows, and the financials are reconciled and recognized.</span></span> <span data-ttu-id="6520a-106">二重書き込みによる見込顧客を現金化の統合により、見積と、Dynamics 365 Sales または Dynamics 365 Supply Chain Management のいずれかの方法で発生した注文を取得し、両方のアプリで見積と注文を使用できるようにするワークフローが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-106">Integration of prospect-to-cash with dual-write creates a workflow that takes a quotation and an order that originate in either Dynamics 365 Sales or Dynamics 365 Supply Chain Management, and makes the quotation and order available in both apps.</span></span>

<span data-ttu-id="6520a-107">アプリ インターフェイスでは、処理のステータスおよび請求書情報にリアル タイムでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6520a-107">In the app interfaces, you can access the processing statuses and invoice information in real time.</span></span> <span data-ttu-id="6520a-108">したがって、見積と注文を再作成することなく、Supply Chain Management の製品在庫、在庫処理、およびフルフィルメントなどの機能をより簡単に管理することができます。</span><span class="sxs-lookup"><span data-stu-id="6520a-108">Therefore, you can more easily manage functions such as product stocking, inventory handling, and fulfillment in Supply Chain Management, without having to re-create the quotations and orders.</span></span>

![見込顧客を現金化への二重書き込みデータフロー](../dual-write/media/dual-write-prospect-to-cash[1].png)

<span data-ttu-id="6520a-110">顧客と連絡先の統合については、[統合された顧客マスター](customer-mapping.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6520a-110">For information about customer and contact integration, see [Integrated customer master](customer-mapping.md).</span></span> <span data-ttu-id="6520a-111">成果物統合については、[統一された製品経験](product-mapping.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6520a-111">For information about product integration, see [Unified product experience](product-mapping.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6520a-112">Dynamics 365 Sales では、見込顧客と顧客の両方が、**RelationshipType** 列が **見込顧客** または **顧客** である **アカウント** テーブル内のレコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="6520a-112">In Dynamics 365 Sales, both prospect and customer refer to a record in the **Account** table where the **RelationshipType** column is either **Prospect** or **Customer**.</span></span> <span data-ttu-id="6520a-113">ビジネス ロジックに、最初に見込み客として、次に顧客として **アカウント** レコードを作成して承認する **アカウント** 認定プロセスが含まれる場合、そのレコードは顧客 (`RelationshipType=Customer`) の場合にのみ Finance and Operations アプリに同期されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-113">If your business logic includes an **Account** qualification process where the **Account** record is created and qualified as a prospect first and then as a customer, that record synchronizes to the Finance and Operations app only when it is a customer (`RelationshipType=Customer`).</span></span> <span data-ttu-id="6520a-114">**アカウント** 行を見込顧客として同期する場合は、見込顧客データを統合するカスタム マップが必要です。</span><span class="sxs-lookup"><span data-stu-id="6520a-114">If you want the **Account** row to synchronize as a prospect, then you need a custom map to integrate the prospect data.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="6520a-115">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="6520a-115">Prerequisites and mapping setup</span></span>

<span data-ttu-id="6520a-116">販売見積を同期するためには、次の設定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-116">Before you can sync sales quotations, you must update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="6520a-117">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="6520a-117">Setup in Sales</span></span>

<span data-ttu-id="6520a-118">Sales で、**設定 \> 管理 \> システム設定 \> 販売** の順にクリックし、次の設定が使用されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6520a-118">In Sales, go to **Settings \> Administration \> System settings \> Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="6520a-119">**システム プライジング計算の使用** システム オプションが、**はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="6520a-119">The **Use system prizing calculation** system option is set to **Yes**.</span></span>
- <span data-ttu-id="6520a-120">**割引の計算方法** 列が、**明細行品目** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="6520a-120">The **Discount calculation method** column is set to **Line item**.</span></span>

### <a name="sites-and-warehouses"></a><span data-ttu-id="6520a-121">サイトと倉庫</span><span class="sxs-lookup"><span data-stu-id="6520a-121">Sites and warehouses</span></span>

<span data-ttu-id="6520a-122">Supply Chain Management では、見積明細行と注文明細行に対して **サイト** と **倉庫** 列が必要です。</span><span class="sxs-lookup"><span data-stu-id="6520a-122">In Supply Chain Management, the **Site** and **warehouse** columns are required for quotation lines and order lines.</span></span> <span data-ttu-id="6520a-123">サイトと倉庫を既定の注文設定で設定した場合、これらの列は、見積明細行または注文明細行に製品を追加したときに自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-123">If you set the site and warehouse in the default order settings, those columns will automatically be set when you add a product to a quotation line or an order line.</span></span> 

### <a name="number-sequences-for-quotations-and-orders"></a><span data-ttu-id="6520a-124">見積と注文の番号順序</span><span class="sxs-lookup"><span data-stu-id="6520a-124">Number sequences for quotations and orders</span></span>

<span data-ttu-id="6520a-125">Sales および Supply Chain Management で見積と注文が作成され同期されている場合、Supply Chain Management と販売の番号順序は接続されていません。</span><span class="sxs-lookup"><span data-stu-id="6520a-125">The number sequences for Supply Chain Management and Sales aren't connected when quotations and orders are created and synced in Sales and Supply Chain Management.</span></span> <span data-ttu-id="6520a-126">Sales で作成された販売注文が Supply Chain Management に同期されている場合は、Supply Chain Management の販売注文番号も同じになります。</span><span class="sxs-lookup"><span data-stu-id="6520a-126">If a sales order that is created in Sales is synced to Supply Chain Management, it has the same sales order number in Supply Chain Management.</span></span> <span data-ttu-id="6520a-127">販売注文番号が重複しないようにするには、2 つのアプリで別の番号順序システムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-127">To help ensure that the sales order number isn't duplicated, you must use different number sequence systems in the two apps.</span></span>

<span data-ttu-id="6520a-128">たとえば、Supply Chain Management の番号順序は **1、2、3、4、5** となり、売上の番号順序は **100、99、98、...** となります。Sales で 100 の販売注文を作成する場合は、最終的に、Supply Chain Management に既に存在する注文番号が生成されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-128">For example, the number sequence in Supply Chain Management is **1, 2, 3, 4, 5, ...**, and the number sequence in Sales is **100, 99, 98, ...**. If you create 100 sales orders in Sales, an order number will eventually be generated that already exists in Supply Chain Management.</span></span> <span data-ttu-id="6520a-129">つまり、2 つの番号順序は、Supply Chain Management および Sales で販売注文が作成されるときに、最終的に重複します。</span><span class="sxs-lookup"><span data-stu-id="6520a-129">In other words, the two number sequences will eventually overlap as sales orders are created in Supply Chain Management and Sales.</span></span> <span data-ttu-id="6520a-130">代わりに、Supply Chain Management で **F1、F2、F3、...** などの番号順序や Sales で **C1、C2、C3、...** などの番号順序を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6520a-130">Instead, you might use a number sequence such as **F1, F2, F3, ...** in Supply Chain Management and a number sequence such as **C1, C2, C3, ...** in Sales.</span></span> <span data-ttu-id="6520a-131">これらの番号順序では重複する販売注文番号が作成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="6520a-131">These number sequences will never produce duplicate sales order numbers.</span></span>

## <a name="sales-quotations"></a><span data-ttu-id="6520a-132">販売見積</span><span class="sxs-lookup"><span data-stu-id="6520a-132">Sales quotations</span></span>

<span data-ttu-id="6520a-133">販売見積が Sales または Supply Chain Management で作成されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-133">Sales quotations can be created in either Sales or Supply Chain Management.</span></span> <span data-ttu-id="6520a-134">Sales で見積を作成すると、その見積がリアル タイムで Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-134">If you create a quotation in Sales, it's synced to Supply Chain Management in real time.</span></span> <span data-ttu-id="6520a-135">同様に、Supply Chain Management で見積を作成すると、その見積がリアル タイムで Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-135">Likewise, if you create a quotation in Supply Chain Management, it's synced to Sales in real time.</span></span> <span data-ttu-id="6520a-136">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="6520a-136">Note the following points:</span></span>

+ <span data-ttu-id="6520a-137">見積の製品に割引を追加できます。</span><span class="sxs-lookup"><span data-stu-id="6520a-137">You can add a discount to the product on the quotation.</span></span> <span data-ttu-id="6520a-138">この場合、割引は Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-138">In this case, the discount will be synced to Supply Chain Management.</span></span> <span data-ttu-id="6520a-139">**割引**、**諸費用**、**税** 列は、ヘッダーで Supply Chain Management の設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-139">The **Discount**, **Charges**, and **Tax** columns on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="6520a-140">この設定では、統合マッピングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6520a-140">This setup doesn't support integration mapping.</span></span> <span data-ttu-id="6520a-141">代わりに、**価格**、**割引**、**諸費用**、**税** の各列は、Supply Chain Management で管理および処理されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-141">Instead, the **Price**, **Discount**, **Charge**, and **Tax** columns are maintained and handled in Supply Chain Management.</span></span>
+ <span data-ttu-id="6520a-142">販売見積ヘッダーの **割引 %**、**割引**、**送料** 列は、読み取り専用列です。</span><span class="sxs-lookup"><span data-stu-id="6520a-142">The **Discount %**, **Discount**, and **Freight Amount** columns on the sales quotation header are read-only columns.</span></span>
+ <span data-ttu-id="6520a-143">**運賃条件**、**配送条件**、**送付方法**、および **配送モード** 列は、既定のマッピングの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="6520a-143">The **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** columns aren't part of the default mappings.</span></span> <span data-ttu-id="6520a-144">これらの列をマップするには、テーブルが同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-144">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synced between.</span></span>

<span data-ttu-id="6520a-145">また、Field Service ソリューションも使用している場合は、**見積明細行の簡易作成** パラメータを再度有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-145">If you are also using the Field Service solution, make sure to re-enable the **Quote Line Quick Create** parameter.</span></span> <span data-ttu-id="6520a-146">このパラメータを再度有効にすると、簡易作成機能を使用して、見積明細行の作成を続行することができます。</span><span class="sxs-lookup"><span data-stu-id="6520a-146">Re-enabling the parameter lets you continue creating quote lines using the quick create function.</span></span>
1. <span data-ttu-id="6520a-147">Dynamics 365 Sales アプリケーションに移動します。</span><span class="sxs-lookup"><span data-stu-id="6520a-147">Navigate to your Dynamics 365 Sales application.</span></span>
2. <span data-ttu-id="6520a-148">ナビゲーション バー上部の設定アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6520a-148">Select the settings icon in the top navigation bar.</span></span>
3. <span data-ttu-id="6520a-149">**詳細設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6520a-149">Select **Advanced Settings**.</span></span>
4. <span data-ttu-id="6520a-150">**システムのカスタマイズ** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6520a-150">Choose the **Customize the System** option.</span></span>
5. <span data-ttu-id="6520a-151">**見積明細行** のメニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="6520a-151">Select the **Quote Line** menu item.</span></span>
6. <span data-ttu-id="6520a-152">**データ サービス** セクションに移動し、**簡易作成を許可する** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="6520a-152">Go to the **Data Services** section and select the **Allow quick create** checkbox.</span></span>

## <a name="sales-orders"></a><span data-ttu-id="6520a-153">販売注文</span><span class="sxs-lookup"><span data-stu-id="6520a-153">Sales orders</span></span>

<span data-ttu-id="6520a-154">販売注文が Sales または Supply Chain Management のいずれかで作成されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-154">Sales orders can be created in either Sales or Supply Chain Management.</span></span> <span data-ttu-id="6520a-155">Sales で販売注文を作成すると、その見積がリアル タイムで Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-155">If you create a sales order in Sales, it's synced to Supply Chain Management in real time.</span></span> <span data-ttu-id="6520a-156">同様に、Supply Chain Management で販売注文を作成すると、その見積もりがリアル タイムで Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-156">Likewise, if you create a sales order in Supply Chain Management, it's synced to Sales in real time.</span></span> <span data-ttu-id="6520a-157">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="6520a-157">Note the following points:</span></span>

+ <span data-ttu-id="6520a-158">Dynamics 365 Sales でリスト外製品は、Dynamics 365 Supply Chain Management では製品カテゴリとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-158">Write-in products on Dynamics 365 Sales will appear as product categories in Dynamics 365 Supply Chain Management.</span></span>
+ <span data-ttu-id="6520a-159">割引計算と丸め:</span><span class="sxs-lookup"><span data-stu-id="6520a-159">Discount calculation and rounding:</span></span>

    - <span data-ttu-id="6520a-160">Sales での割引計算モデルは、Supply Chain Management の割引計算モデルとは異なります。</span><span class="sxs-lookup"><span data-stu-id="6520a-160">The discount calculation model in Sales differs from the discount calculation model in Supply Chain Management.</span></span> <span data-ttu-id="6520a-161">Supply Chain Management では、販売注文明細行の最終的な割引金額は、割引額と割引率の組み合わせの結果です。</span><span class="sxs-lookup"><span data-stu-id="6520a-161">In Supply Chain Management, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="6520a-162">この最終割引額をライン上の数量で割ると、丸め処理が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-162">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="6520a-163">ただし、この丸め処理単位の割引額が Sales に同期されている場合は、この丸め処理は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="6520a-163">However, this rounding isn't considered if a rounded per-unit discount amount is synced to Sales.</span></span> <span data-ttu-id="6520a-164">Supply Chain Management の販売明細行からの全額割引が Sales に正しく同期されるようにするには、全額を明細行の数量で除算せずに同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-164">To help ensure that the full discount amount from a sales line in Supply Chain Management is correctly synced to Sales, the full amount must be synced without being divided by the line quantity.</span></span> <span data-ttu-id="6520a-165">したがって、Sales で割引の計算方法を **明細行品目** として定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-165">Therefore, you must define the discount calculation method as **Line item** in Sales.</span></span>
    - <span data-ttu-id="6520a-166">販売注文行が Sales から Supply Chain Management に同期される場合、明細行全体の割引額が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-166">When a sales order line is synced from Sales to Supply Chain Management, the full line discount amount is used.</span></span> <span data-ttu-id="6520a-167">Supply Chain Management には、明細行の完全な割引金額を格納できる列がないため、金額は数量で除算されて、**行割引** 列に格納されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-167">Because Supply Chain Management has no column that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** column.</span></span> <span data-ttu-id="6520a-168">この区分中に発生する丸めは、販売明細行の **販売費用** 列に保管されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-168">Any rounding that occurs during this division is stored in the **Sales charges** column on the sales line.</span></span>

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a><span data-ttu-id="6520a-169">例: Sales から Supply Chain Management への同期</span><span class="sxs-lookup"><span data-stu-id="6520a-169">Example: Synchronization from Sales to Supply Chain Management</span></span>

<span data-ttu-id="6520a-170">次の販売注文があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-170">You have the following sales order:</span></span>

+ <span data-ttu-id="6520a-171">**Sales:** 数量 = 3、行あたりの割引 = 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="6520a-171">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
+ <span data-ttu-id="6520a-172">**Supply Chain Management:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01</span><span class="sxs-lookup"><span data-stu-id="6520a-172">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = –$0.01</span></span>

<span data-ttu-id="6520a-173">Supply Chain Management から Sales に同期すると、次の結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="6520a-173">If you sync from Supply Chain Management to Sales, you get the following result:</span></span>

+ <span data-ttu-id="6520a-174">**Supply Chain Management:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01</span><span class="sxs-lookup"><span data-stu-id="6520a-174">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = –$0.01</span></span>
+ <span data-ttu-id="6520a-175">**Sales:** 数量 = 3、行あたりの割引 = (3 × 3.33 USD) + 0.01 USD = 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="6520a-175">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="dual-write-solution-for-sales"></a><span data-ttu-id="6520a-176">Sales のための二重書き込みソリューション</span><span class="sxs-lookup"><span data-stu-id="6520a-176">Dual-write solution for Sales</span></span>

<span data-ttu-id="6520a-177">新しい列が **注文** テーブルに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-177">New columns have been added to the **Order** table and appear on the page.</span></span> <span data-ttu-id="6520a-178">これらの列のほとんどは、Sales の **統合** タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-178">Most of these columns appear on the **Integration** tab in Sales.</span></span> <span data-ttu-id="6520a-179">状態列がどのようにマッピングされるかについての詳細は、[販売注文の状態列のマッピングを設定する](sales-status-map.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6520a-179">To learn more about how the status columns are mapped, see [Set up the mapping for sales order status columns](sales-status-map.md).</span></span>

+ <span data-ttu-id="6520a-180">**販売注文** ページに **請求書作成** または **注文のキャンセル** ボタンは Sales に表示されません。</span><span class="sxs-lookup"><span data-stu-id="6520a-180">The **Create Invoice** and **Cancel Order** buttons on the **Sales order** page are hidden in Sales.</span></span>
+ <span data-ttu-id="6520a-181">**販売注文状態** は **有効** のままにすると、Supply Chain Management からの変更が Sales の販売注文に流れるようにします。</span><span class="sxs-lookup"><span data-stu-id="6520a-181">The **Sales order status** value will remain **Active** to help ensure that changes from Supply Chain Management can flow to the sales order in Sales.</span></span> <span data-ttu-id="6520a-182">この動作を管理するためには、既定の **ステイトコード \[ステータス\]** 値を **有効** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6520a-182">To control this behavior, set the default **Statecode \[Status\]** value to **Active**.</span></span>

## <a name="invoices"></a><span data-ttu-id="6520a-183">請求書</span><span class="sxs-lookup"><span data-stu-id="6520a-183">Invoices</span></span>

<span data-ttu-id="6520a-184">売上請求書が Supply Chain Management で作成され、Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-184">Sales invoices are created in Supply Chain Management and synced to Sales.</span></span> <span data-ttu-id="6520a-185">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="6520a-185">Note the following points:</span></span>

+ <span data-ttu-id="6520a-186">**請求書番号** 列が **請求書** テーブルに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-186">An **Invoice number** column has been added to the **Invoice** table and appears on the page.</span></span>
+ <span data-ttu-id="6520a-187">請求書が Supply Chain Management で作成され、Sales に同期されるため、**販売注文** ページの **請求書の作成** ボタンは非表示になります。</span><span class="sxs-lookup"><span data-stu-id="6520a-187">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synced to Sales.</span></span> <span data-ttu-id="6520a-188">請求書が Supply Chain Management から同期されるため、**請求書** ページは編集できません。</span><span class="sxs-lookup"><span data-stu-id="6520a-188">The **Invoice** page can't be edited, because invoices will be synced from Supply Chain Management.</span></span>
+ <span data-ttu-id="6520a-189">Supply Chain Management からの関連請求書が Sales に同期されると、**販売注文状態** 値は自動的に **請求済** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-189">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synced to Sales.</span></span> <span data-ttu-id="6520a-190">さらに、請求書の作成元である販売注文の所有者は、請求書の所有者として割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6520a-190">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="6520a-191">したがって、販売注文書の所有者は、請求書を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="6520a-191">Therefore, the owner of the sales order can view the invoice.</span></span>
+ <span data-ttu-id="6520a-192">**運賃条件**、**配送条件**、および **配送モード** 列は既定のマッピングには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="6520a-192">The **Freight terms**, **Delivery terms**, and **Delivery mode** columns aren't included in the default mappings.</span></span> <span data-ttu-id="6520a-193">これらの列をマップするには、テーブルが同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-193">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synced between.</span></span>

## <a name="templates"></a><span data-ttu-id="6520a-194">テンプレート</span><span class="sxs-lookup"><span data-stu-id="6520a-194">Templates</span></span>

<span data-ttu-id="6520a-195">次の表に示されているように、見込顧客を現金化するには、データ操作中に連携して動作するコア テーブル マップのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6520a-195">Prospect-to-cash includes a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="6520a-196">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="6520a-196">Finance and Operations apps</span></span> | <span data-ttu-id="6520a-197">Customer Engagement アプリ</span><span class="sxs-lookup"><span data-stu-id="6520a-197">Customer engagement apps</span></span> | <span data-ttu-id="6520a-198">説明</span><span class="sxs-lookup"><span data-stu-id="6520a-198">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="6520a-199">売上請求書ヘッダー V2</span><span class="sxs-lookup"><span data-stu-id="6520a-199">Sales invoice headers V2</span></span>    | <span data-ttu-id="6520a-200">請求書</span><span class="sxs-lookup"><span data-stu-id="6520a-200">invoices</span></span>                          | <span data-ttu-id="6520a-201">Finance and Operations アプリの売上請求書ヘッダー V2 テーブルには、販売注文と自由形式の 請求書が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6520a-201">The Sales invoice headers V2 table in the Finance and Operations app contains invoices for sales orders and free text invoices.</span></span> <span data-ttu-id="6520a-202">Dataverse では、自由形式の請求書ドキュメントを除外するデュアル書き込み用のフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6520a-202">A filter is applied in Dataverse for dual-write that will filter out any free text invoice documents.</span></span> |
| <span data-ttu-id="6520a-203">売上請求書明細行 V2</span><span class="sxs-lookup"><span data-stu-id="6520a-203">Sales invoice lines V2</span></span>      | <span data-ttu-id="6520a-204">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="6520a-204">invoicedetails</span></span>                    |             |
| <span data-ttu-id="6520a-205">CDS 販売注文ヘッダー</span><span class="sxs-lookup"><span data-stu-id="6520a-205">CDS sales order headers</span></span>     | <span data-ttu-id="6520a-206">販売注文</span><span class="sxs-lookup"><span data-stu-id="6520a-206">salesorders</span></span>                       |             |
| <span data-ttu-id="6520a-207">CDS 販売注文明細行</span><span class="sxs-lookup"><span data-stu-id="6520a-207">CDS sales order lines</span></span>       | <span data-ttu-id="6520a-208">販売注文詳細</span><span class="sxs-lookup"><span data-stu-id="6520a-208">salesorderdetails</span></span>                 |             |
| <span data-ttu-id="6520a-209">販売注文元コード</span><span class="sxs-lookup"><span data-stu-id="6520a-209">Sales order origin codes</span></span>    | <span data-ttu-id="6520a-210">msdyn\_販売注文元</span><span class="sxs-lookup"><span data-stu-id="6520a-210">msdyn\_salesorderorigins</span></span>          |             |
| <span data-ttu-id="6520a-211">CDS 販売見積ヘッダー</span><span class="sxs-lookup"><span data-stu-id="6520a-211">CDS sales quotation header</span></span>  | <span data-ttu-id="6520a-212">見積</span><span class="sxs-lookup"><span data-stu-id="6520a-212">quotes</span></span>                            |             |
| <span data-ttu-id="6520a-213">CDS 販売見積明細行</span><span class="sxs-lookup"><span data-stu-id="6520a-213">CDS sales quotation lines</span></span>   | <span data-ttu-id="6520a-214">見積詳細</span><span class="sxs-lookup"><span data-stu-id="6520a-214">quotedetails</span></span>                      |             |

<span data-ttu-id="6520a-215">見込顧客の現金化に関連するコア テーブル マップは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="6520a-215">Here are the related core table maps for prospect-to-cash:</span></span>

+ [<span data-ttu-id="6520a-216">顧客 V3 を アカウントへ</span><span class="sxs-lookup"><span data-stu-id="6520a-216">Customers V3 to accounts</span></span>](customer-mapping.md#customers-v3-to-accounts)
+ [<span data-ttu-id="6520a-217">CDS 連絡先 V2 を連絡先へ</span><span class="sxs-lookup"><span data-stu-id="6520a-217">CDS Contacts V2 to contacts</span></span>](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [<span data-ttu-id="6520a-218">顧客 V3 を連絡先へ</span><span class="sxs-lookup"><span data-stu-id="6520a-218">Customers V3 to contacts</span></span>](customer-mapping.md#customers-v3-to-contacts)
+ [<span data-ttu-id="6520a-219">リリース済製品 V2 を msdyn_sharedproductdetails へ</span><span class="sxs-lookup"><span data-stu-id="6520a-219">Released products V2 to msdyn_sharedproductdetails</span></span>](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [<span data-ttu-id="6520a-220">すべての製品を msdyn_globalproducts へ</span><span class="sxs-lookup"><span data-stu-id="6520a-220">All products to msdyn_globalproducts</span></span>](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [<span data-ttu-id="6520a-221">価格表</span><span class="sxs-lookup"><span data-stu-id="6520a-221">Pricelist</span></span>](product-mapping.md)

## <a name="limitations"></a><span data-ttu-id="6520a-222">制限</span><span class="sxs-lookup"><span data-stu-id="6520a-222">Limitations</span></span>
- <span data-ttu-id="6520a-223">返品注文はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6520a-223">Return orders are not supported.</span></span>
- <span data-ttu-id="6520a-224">訂正票はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6520a-224">Credit notes are not supported.</span></span>
- <span data-ttu-id="6520a-225">顧客や仕入先など、マスタ データに対して財務分析コードを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6520a-225">Financial dimensions must be set for the master data, for example, customer and vendor.</span></span> <span data-ttu-id="6520a-226">顧客が見積書または販売注文に追加されると、顧客レコード に関連付けられている財務分析コードが自動的に注文にフローします。</span><span class="sxs-lookup"><span data-stu-id="6520a-226">When a customer is added to a quotation or sales order, the financial dimensions associated with the customer record flow to the order automatically.</span></span> <span data-ttu-id="6520a-227">現在、デュアル書き込みにはマスター データの財務分析コード データは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="6520a-227">Currently dual-write does not include financial dimensions data for master data.</span></span> 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]