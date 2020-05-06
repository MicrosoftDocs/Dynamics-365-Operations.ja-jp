---
title: 二重書き込みの見込顧客を現金化
description: このトピックでは、二重書き込みの見込顧客を現金化に関する情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 57aabeef0ee94b4b13bbe6e3925bcafe1e809ab2
ms.sourcegitcommit: 984604fd651d74aa49a2d7513f096faaf49f9f27
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/18/2020
ms.locfileid: "3270291"
---
# <a name="prospect-to-cash-in-dual-write"></a><span data-ttu-id="df22b-103">二重書き込みの見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="df22b-103">Prospect-to-cash in dual-write</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="df22b-104">ほとんどの企業にとって重要な目標は、見込顧客を顧客に変換し、その顧客との継続的な取引関係を維持することです。</span><span class="sxs-lookup"><span data-stu-id="df22b-104">An important goal of most businesses is to convert prospects to customers and then maintain an ongoing business relationship with those customers.</span></span> <span data-ttu-id="df22b-105">Microsoft Dynamics 365 アプリでは、見込顧客を現金化のプロセスが見積または注文処理のワークフローで行われ、財務の調整と認識が行われます。</span><span class="sxs-lookup"><span data-stu-id="df22b-105">In Microsoft Dynamics 365 apps, the prospect-to-cash process occurs through quotations or order processing workflows, and the financials are reconciled and recognized.</span></span> <span data-ttu-id="df22b-106">二重書き込みによる見込顧客を現金化の統合により、見積と、Dynamics 365 Sales または Dynamics 365 Supply Chain Management のいずれかの方法で発生した注文を取得し、両方のアプリで見積と注文を使用できるようにするワークフローが作成されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-106">Integration of prospect-to-cash with dual-write creates a workflow that takes a quotation and an order that originate in either Dynamics 365 Sales or Dynamics 365 Supply Chain Management, and makes the quotation and order available in both apps.</span></span>

<span data-ttu-id="df22b-107">アプリ インターフェイスでは、処理のステータスおよび請求書情報にリアル タイムでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="df22b-107">In the app interfaces, you can access the processing statuses and invoice information in real time.</span></span> <span data-ttu-id="df22b-108">したがって、見積と注文を再作成することなく、Supply Chain Management の製品在庫、在庫処理、およびフルフィルメントなどの機能をより簡単に管理することができます。</span><span class="sxs-lookup"><span data-stu-id="df22b-108">Therefore, you can more easily manage functions such as product stocking, inventory handling, and fulfillment in Supply Chain Management, without having to re-create the quotations and orders.</span></span>

![見込顧客を現金化への二重書き込みデータフロー](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="df22b-110">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="df22b-110">Prerequisites and mapping setup</span></span>

<span data-ttu-id="df22b-111">販売見積を同期するためには、次の設定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df22b-111">Before you can sync sales quotations, you must update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="df22b-112">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="df22b-112">Setup in Sales</span></span>

<span data-ttu-id="df22b-113">Sales で、**設定 \> 管理 \> システム設定 \> 販売**の順にクリックし、次の設定が使用されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="df22b-113">In Sales, go to **Settings \> Administration \> System settings \> Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="df22b-114">**システム プライジング計算の使用**システム オプションが、**はい**に設定されています。</span><span class="sxs-lookup"><span data-stu-id="df22b-114">The **Use system prizing calculation** system option is set to **Yes**.</span></span>
- <span data-ttu-id="df22b-115">**割引の計算方法** フィールドが、**明細行品目** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="df22b-115">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="sites-and-warehouses"></a><span data-ttu-id="df22b-116">サイトと倉庫</span><span class="sxs-lookup"><span data-stu-id="df22b-116">Sites and warehouses</span></span>

<span data-ttu-id="df22b-117">Supply Chain Management では、見積明細行と注文明細行に対して**サイト**と**倉庫**フィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="df22b-117">In Supply Chain Management, the **Site** and **warehouse** fields are required for quotation lines and order lines.</span></span> <span data-ttu-id="df22b-118">サイトと倉庫を既定の注文設定に設定した場合、これらのフィールドは、見積明細行または注文明細行に製品を追加したときに自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-118">If you set the site and warehouse in the default order settings, those fields will automatically be set when you add a product to a quotation line or an order line.</span></span> 

### <a name="number-sequences-for-quotations-and-orders"></a><span data-ttu-id="df22b-119">見積と注文の番号順序</span><span class="sxs-lookup"><span data-stu-id="df22b-119">Number sequences for quotations and orders</span></span>

<span data-ttu-id="df22b-120">Sales および Supply Chain Management で見積と注文が作成され同期されている場合、Supply Chain Management と販売の番号順序は接続されていません。</span><span class="sxs-lookup"><span data-stu-id="df22b-120">The number sequences for Supply Chain Management and Sales aren't connected when quotations and orders are created and synced in Sales and Supply Chain Management.</span></span> <span data-ttu-id="df22b-121">Sales で作成された販売注文が Supply Chain Management に同期されている場合は、Supply Chain Management の販売注文番号も同じになります。</span><span class="sxs-lookup"><span data-stu-id="df22b-121">If a sales order that is created in Sales is synced to Supply Chain Management, it has the same sales order number in Supply Chain Management.</span></span> <span data-ttu-id="df22b-122">販売注文番号が重複しないようにするには、2 つのアプリで別の番号順序システムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df22b-122">To help ensure that the sales order number isn't duplicated, you must use different number sequence systems in the two apps.</span></span>

<span data-ttu-id="df22b-123">たとえば、Supply Chain Management の番号順序は **1、2、3、4、5** となり、売上の番号順序は **100、99、98、...** となります。Sales で 100 の販売注文を作成する場合は、最終的に、Supply Chain Management に既に存在する注文番号が生成されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-123">For example, the number sequence in Supply Chain Management is **1, 2, 3, 4, 5, ...**, and the number sequence in Sales is **100, 99, 98, ...**. If you create 100 sales orders in Sales, an order number will eventually be generated that already exists in Supply Chain Management.</span></span> <span data-ttu-id="df22b-124">つまり、2 つの番号順序は、Supply Chain Management および Sales で販売注文が作成されるときに、最終的に重複します。</span><span class="sxs-lookup"><span data-stu-id="df22b-124">In other words, the two number sequences will eventually overlap as sales orders are created in Supply Chain Management and Sales.</span></span> <span data-ttu-id="df22b-125">代わりに、Supply Chain Management で **F1、F2、F3、...** などの番号順序や Sales で **C1、C2、C3、...** などの番号順序を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="df22b-125">Instead, you might use a number sequence such as **F1, F2, F3, ...** in Supply Chain Management and a number sequence such as **C1, C2, C3, ...** in Sales.</span></span> <span data-ttu-id="df22b-126">これらの番号順序では重複する販売注文番号が作成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="df22b-126">These number sequences will never produce duplicate sales order numbers.</span></span>

## <a name="sales-quotations"></a><span data-ttu-id="df22b-127">販売見積</span><span class="sxs-lookup"><span data-stu-id="df22b-127">Sales quotations</span></span>

<span data-ttu-id="df22b-128">販売見積が Sales または Supply Chain Management で作成されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-128">Sales quotations can be created in either Sales or Supply Chain Management.</span></span> <span data-ttu-id="df22b-129">Sales で見積を作成すると、その見積がリアル タイムで Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-129">If you create a quotation in Sales, it's synced to Supply Chain Management in real time.</span></span> <span data-ttu-id="df22b-130">同様に、Supply Chain Management で見積を作成すると、その見積がリアル タイムで Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-130">Likewise, if you create a quotation in Supply Chain Management, it's synced to Sales in real time.</span></span> <span data-ttu-id="df22b-131">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="df22b-131">Note the following points:</span></span>

+ <span data-ttu-id="df22b-132">見積の製品に割引を追加できます。</span><span class="sxs-lookup"><span data-stu-id="df22b-132">You can add a discount to the product on the quotation.</span></span> <span data-ttu-id="df22b-133">この場合、割引は Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-133">In this case, the discount will be synced to Supply Chain Management.</span></span> <span data-ttu-id="df22b-134">**割引**、**請求**、および **税** フィールドは、ヘッダーで Supply Chain Management の設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-134">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="df22b-135">この設定では、統合マッピングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="df22b-135">This setup doesn't support integration mapping.</span></span> <span data-ttu-id="df22b-136">代わりに、**価格**、**割引**、**請求金額**、および**税**の各フィールドは、Supply Chain Management で管理および処理されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-136">Instead, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Supply Chain Management.</span></span>
+ <span data-ttu-id="df22b-137">販売見積ヘッダーの読み取り専用フィールドの**割引 %**、**割引**、**貨物量**。</span><span class="sxs-lookup"><span data-stu-id="df22b-137">The **Discount %**, **Discount**, and **Freight Amount** fields on the sales quotation header are read-only fields.</span></span>
+ <span data-ttu-id="df22b-138">**運賃条件**、**配送条件**、**送付方法**、および**配送モード** フィールドは、既定のマッピングの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="df22b-138">The **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="df22b-139">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df22b-139">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synced between.</span></span>

<span data-ttu-id="df22b-140">また、Field Service ソリューションを使用している場合は、**見積明細行の簡易作成**パラメータを再度有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="df22b-140">If you are also using the Field Service solution, make sure to re-enable the **Quote Line Quick Craete** parameter.</span></span> <span data-ttu-id="df22b-141">このパラメータを再度有効にすると、簡易作成機能を使用して、見積明細行の作成を続行することができます。</span><span class="sxs-lookup"><span data-stu-id="df22b-141">Re-enabling the parameter lets you to continue creating quote lines using the quick create function.</span></span>
1. <span data-ttu-id="df22b-142">Dynamics 365 Sales アプリケーションに移動します。</span><span class="sxs-lookup"><span data-stu-id="df22b-142">Navigate to your Dynamics 365 Sales application.</span></span>
2. <span data-ttu-id="df22b-143">ナビゲーション バー上部の設定アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="df22b-143">Select the settings icon in the top navigation bar.</span></span>
3. <span data-ttu-id="df22b-144">**詳細設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df22b-144">Select **Advanced Settings**.</span></span>
4. <span data-ttu-id="df22b-145">**システムのカスタマイズ** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="df22b-145">Choose the **Customize the System** option.</span></span>
5. <span data-ttu-id="df22b-146">**見積明細行** のメニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="df22b-146">Select the **Quote Line** menu item.</span></span>
6. <span data-ttu-id="df22b-147">**データ サービス** セクションに移動し、**簡易作成を許可する** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="df22b-147">Go to the **Data Services** section and select the **Allow quick create** checkbox.</span></span>

## <a name="sales-orders"></a><span data-ttu-id="df22b-148">販売注文</span><span class="sxs-lookup"><span data-stu-id="df22b-148">Sales orders</span></span>

<span data-ttu-id="df22b-149">販売注文が Sales または Supply Chain Management のいずれかで作成されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-149">Sales orders can be created in either Sales or Supply Chain Management.</span></span> <span data-ttu-id="df22b-150">Sales で販売注文を作成すると、その見積がリアル タイムで Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-150">If you create a sales order in Sales, it's synced to Supply Chain Management in real time.</span></span> <span data-ttu-id="df22b-151">同様に、Supply Chain Management で販売注文を作成すると、その見積もりがリアル タイムで Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-151">Likewise, if you create a sales order in Supply Chain Management, it's synced to Sales in real time.</span></span> <span data-ttu-id="df22b-152">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="df22b-152">Note the following points:</span></span>

+ <span data-ttu-id="df22b-153">注文のすべての製品が Finance and Operations アプリから出荷されている場合にのみ、Sales から注文を有効にして同期できます。</span><span class="sxs-lookup"><span data-stu-id="df22b-153">You can activate and sync orders from Sales only if all the products on the order come from Finance and Operations apps.</span></span> <span data-ttu-id="df22b-154">したがって、リスト外製品は存在しません。</span><span class="sxs-lookup"><span data-stu-id="df22b-154">Therefore, there can be no write-in products.</span></span>
+ <span data-ttu-id="df22b-155">割引計算と丸め:</span><span class="sxs-lookup"><span data-stu-id="df22b-155">Discount calculation and rounding:</span></span>

    - <span data-ttu-id="df22b-156">Sales での割引計算モデルは、Supply Chain Management の割引計算モデルとは異なります。</span><span class="sxs-lookup"><span data-stu-id="df22b-156">The discount calculation model in Sales differs from the discount calculation model in Supply Chain Management.</span></span> <span data-ttu-id="df22b-157">Supply Chain Management では、販売注文明細行の最終的な割引金額は、割引額と割引率の組み合わせの結果です。</span><span class="sxs-lookup"><span data-stu-id="df22b-157">In Supply Chain Management, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="df22b-158">この最終割引額をライン上の数量で割ると、丸め処理が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="df22b-158">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="df22b-159">ただし、この丸め処理単位の割引額が Sales に同期されている場合は、この丸め処理は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="df22b-159">However, this rounding isn't considered if a rounded per-unit discount amount is synced to Sales.</span></span> <span data-ttu-id="df22b-160">Supply Chain Management の販売明細行からの全額割引が Sales に正しく同期されるようにするには、全額を明細行の数量で除算せずに同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="df22b-160">To help ensure that the full discount amount from a sales line in Supply Chain Management is correctly synced to Sales, the full amount must be synced without being divided by the line quantity.</span></span> <span data-ttu-id="df22b-161">したがって、Sales で割引の計算方法を**明細行品目**として定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df22b-161">Therefore, you must define the discount calculation method as **Line item** in Sales.</span></span>
    - <span data-ttu-id="df22b-162">販売注文行が Sales から Supply Chain Management に同期される場合、明細行全体の割引額が使用されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-162">When a sales order line is synced from Sales to Supply Chain Management, the full line discount amount is used.</span></span> <span data-ttu-id="df22b-163">Supply Chain Management には、明細行の完全な割引金額を格納できるフィールドがないため、金額は数量で除算されて、**行割引**フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-163">Because Supply Chain Management has no field that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** field.</span></span> <span data-ttu-id="df22b-164">この区分中に発生する丸めは、販売明細行の**販売費用**フィールドに保管されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-164">Any rounding that occurs during this division is stored in the **Sales charges** field on the sales line.</span></span>

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a><span data-ttu-id="df22b-165">例: Sales から Supply Chain Management への同期</span><span class="sxs-lookup"><span data-stu-id="df22b-165">Example: Synchronization from Sales to Supply Chain Management</span></span>

<span data-ttu-id="df22b-166">次の販売注文があります。</span><span class="sxs-lookup"><span data-stu-id="df22b-166">You have the following sales order:</span></span>

+ <span data-ttu-id="df22b-167">**Sales:** 数量 = 3、行あたりの割引 = 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="df22b-167">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
+ <span data-ttu-id="df22b-168">**Supply Chain Management:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01</span><span class="sxs-lookup"><span data-stu-id="df22b-168">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = –$0.01</span></span>

<span data-ttu-id="df22b-169">Supply Chain Management から Sales に同期すると、次の結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="df22b-169">If you sync from Supply Chain Management to Sales, you get the following result:</span></span>

+ <span data-ttu-id="df22b-170">**Supply Chain Management:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01</span><span class="sxs-lookup"><span data-stu-id="df22b-170">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = –$0.01</span></span>
+ <span data-ttu-id="df22b-171">**Sales:** 数量 = 3、行あたりの割引 = (3 × 3.33 USD) + 0.01 USD = 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="df22b-171">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="dual-write-solution-for-sales"></a><span data-ttu-id="df22b-172">Sales のための二重書き込みソリューション</span><span class="sxs-lookup"><span data-stu-id="df22b-172">Dual-write solution for Sales</span></span>

<span data-ttu-id="df22b-173">新しいフィールドが**注文**エンティティに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-173">New fields have been added to the **Order** entity and appear on the page.</span></span> <span data-ttu-id="df22b-174">これらのフィールドのほとんどは、Sales の**統合**タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-174">Most of these fields appear on the **Integration** tab in Sales.</span></span> <span data-ttu-id="df22b-175">特殊なフィールドがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="df22b-175">There are a few special fields:</span></span>

+ <span data-ttu-id="df22b-176">**処理状態**フィールドには、Supply Chain Management の注文の処理ステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-176">The **Processing status** field shows the processing status of the order in Supply Chain Management.</span></span> <span data-ttu-id="df22b-177">このフィールドはロックされており、Supply Chain Management からの注文のステータスのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="df22b-177">This field is locked and shows only the status of the order from Supply Chain Management.</span></span> <span data-ttu-id="df22b-178">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="df22b-178">The following values are available:</span></span>

    + <span data-ttu-id="df22b-179">**有効** – **有効**ボタンを使用すると、受注後のステータスが Sales で有効になります。</span><span class="sxs-lookup"><span data-stu-id="df22b-179">**Active** – The status after the order is activated in Sales by using the **Activate** button.</span></span>
    + <span data-ttu-id="df22b-180">**確定済**</span><span class="sxs-lookup"><span data-stu-id="df22b-180">**Confirmed**</span></span>
    + <span data-ttu-id="df22b-181">**配送済**</span><span class="sxs-lookup"><span data-stu-id="df22b-181">**Delivered**</span></span>
    + <span data-ttu-id="df22b-182">**請求済**</span><span class="sxs-lookup"><span data-stu-id="df22b-182">**Invoiced**</span></span>
    + <span data-ttu-id="df22b-183">**一部配出荷**</span><span class="sxs-lookup"><span data-stu-id="df22b-183">**Partially Delivered**</span></span>
    + <span data-ttu-id="df22b-184">**一部請求済**</span><span class="sxs-lookup"><span data-stu-id="df22b-184">**Partially Invoiced**</span></span>
    + <span data-ttu-id="df22b-185">**ピッキング済**</span><span class="sxs-lookup"><span data-stu-id="df22b-185">**Picked**</span></span>
    + <span data-ttu-id="df22b-186">**取消済**</span><span class="sxs-lookup"><span data-stu-id="df22b-186">**Canceled**</span></span>

    <span data-ttu-id="df22b-187">次の表に、処理ステータスを **CRM ステータス コード**値にマップする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="df22b-187">The following table shows how the processing status is mapped to the **CRM status code** value.</span></span>

    | <span data-ttu-id="df22b-188">処理状態</span><span class="sxs-lookup"><span data-stu-id="df22b-188">Processing status</span></span>           | <span data-ttu-id="df22b-189">CRM 状態 コード</span><span class="sxs-lookup"><span data-stu-id="df22b-189">CRM status code</span></span>    |
    |-----------------------------|--------------------|
    | <span data-ttu-id="df22b-190">使用可能</span><span class="sxs-lookup"><span data-stu-id="df22b-190">Active</span></span>                      | <span data-ttu-id="df22b-191">新規/保留中/保留中</span><span class="sxs-lookup"><span data-stu-id="df22b-191">New/Pending/Onhold</span></span> |
    | <span data-ttu-id="df22b-192">確認済/ピッキング済</span><span class="sxs-lookup"><span data-stu-id="df22b-192">Confirmed/Picked</span></span>            | <span data-ttu-id="df22b-193">処理中</span><span class="sxs-lookup"><span data-stu-id="df22b-193">In Progress</span></span>        |
    | <span data-ttu-id="df22b-194">一部出荷済</span><span class="sxs-lookup"><span data-stu-id="df22b-194">Partially Delivered</span></span>         | <span data-ttu-id="df22b-195">部分的</span><span class="sxs-lookup"><span data-stu-id="df22b-195">Partial</span></span>            |
    | <span data-ttu-id="df22b-196">配送済</span><span class="sxs-lookup"><span data-stu-id="df22b-196">Delivered</span></span>                   | <span data-ttu-id="df22b-197">完了</span><span class="sxs-lookup"><span data-stu-id="df22b-197">Complete</span></span>           |
    | <span data-ttu-id="df22b-198">請求済/一部請求済</span><span class="sxs-lookup"><span data-stu-id="df22b-198">Invoiced/Partially Invoiced</span></span> | <span data-ttu-id="df22b-199">請求済</span><span class="sxs-lookup"><span data-stu-id="df22b-199">Invoiced</span></span>           |
    | <span data-ttu-id="df22b-200">取消済</span><span class="sxs-lookup"><span data-stu-id="df22b-200">Canceled</span></span>                    | <span data-ttu-id="df22b-201">通貨なし</span><span class="sxs-lookup"><span data-stu-id="df22b-201">No Money</span></span>           |

+ <span data-ttu-id="df22b-202">**販売注文**ページに**請求書作成**または**注文のキャンセル** ボタンは Sales に表示されません。</span><span class="sxs-lookup"><span data-stu-id="df22b-202">The **Create Invoice** and **Cancel Order** buttons on the **Sales order** page are hidden in Sales.</span></span>
+ <span data-ttu-id="df22b-203">**販売注文状態**は**有効**のままにすると、Supply Chain Management からの変更が Sales の販売注文に流れるようにします。</span><span class="sxs-lookup"><span data-stu-id="df22b-203">The **Sales order status** value will remain **Active** to help ensure that changes from Supply Chain Management can flow to the sales order in Sales.</span></span> <span data-ttu-id="df22b-204">この動作を管理するためには、既定の**ステイトコード \[ステータス\]** 値を**有効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="df22b-204">To control this behavior, set the default **Statecode \[Status\]** value to **Active**.</span></span>

## <a name="invoices"></a><span data-ttu-id="df22b-205">請求書</span><span class="sxs-lookup"><span data-stu-id="df22b-205">Invoices</span></span>

<span data-ttu-id="df22b-206">売上請求書が Supply Chain Management で作成され、Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-206">Sales invoices are created in Supply Chain Management and synced to Sales.</span></span> <span data-ttu-id="df22b-207">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="df22b-207">Note the following points:</span></span>

+ <span data-ttu-id="df22b-208">**請求書番号**フィールドが**請求書**エンティティに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-208">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
+ <span data-ttu-id="df22b-209">請求書が Supply Chain Management で作成され、Sales に同期されるため、**販売注文**ページの**請求書の作成**ボタンは非表示になります。</span><span class="sxs-lookup"><span data-stu-id="df22b-209">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synced to Sales.</span></span> <span data-ttu-id="df22b-210">請求書が Supply Chain Management から同期されるため、**請求書**ページは編集できません。</span><span class="sxs-lookup"><span data-stu-id="df22b-210">The **Invoice** page can't be edited, because invoices will be synced from Supply Chain Management.</span></span>
+ <span data-ttu-id="df22b-211">Supply Chain Management からの関連請求書が Sales に同期されると、**販売注文状態**値は自動的に**請求済**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="df22b-211">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synced to Sales.</span></span> <span data-ttu-id="df22b-212">さらに、請求書の作成元である販売注文の所有者は、請求書の所有者として割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="df22b-212">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="df22b-213">したがって、販売注文書の所有者は、請求書を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="df22b-213">Therefore, the owner of the sales order can view the invoice.</span></span>
+ <span data-ttu-id="df22b-214">**運賃条件**、**配送条件**、および**荷渡方法**フィールドは既定のマッピングには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="df22b-214">The **Freight terms**, **Delivery terms**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="df22b-215">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df22b-215">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synced between.</span></span>

## <a name="templates"></a><span data-ttu-id="df22b-216">テンプレート</span><span class="sxs-lookup"><span data-stu-id="df22b-216">Templates</span></span>

<span data-ttu-id="df22b-217">次の表に示されているように、見込顧客を現金化するには、データ操作中に連携して動作するコア エンティティ マップのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="df22b-217">Prospect-to-cash includes a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="df22b-218">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="df22b-218">Finance and Operations apps</span></span> | <span data-ttu-id="df22b-219">Dynamics 365 のモデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="df22b-219">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="df22b-220">説明</span><span class="sxs-lookup"><span data-stu-id="df22b-220">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="df22b-221">売上請求書ヘッダー V2</span><span class="sxs-lookup"><span data-stu-id="df22b-221">Sales invoice headers V2</span></span>    | <span data-ttu-id="df22b-222">請求書</span><span class="sxs-lookup"><span data-stu-id="df22b-222">invoices</span></span>                          |             |
| <span data-ttu-id="df22b-223">売上請求書明細行 V2</span><span class="sxs-lookup"><span data-stu-id="df22b-223">Sales invoice lines V2</span></span>      | <span data-ttu-id="df22b-224">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="df22b-224">invoicedetails</span></span>                    |             |
| <span data-ttu-id="df22b-225">CDS 販売注文ヘッダー</span><span class="sxs-lookup"><span data-stu-id="df22b-225">CDS sales order headers</span></span>     | <span data-ttu-id="df22b-226">販売注文</span><span class="sxs-lookup"><span data-stu-id="df22b-226">salesorders</span></span>                       |             |
| <span data-ttu-id="df22b-227">CDS 販売注文明細行</span><span class="sxs-lookup"><span data-stu-id="df22b-227">CDS sales order lines</span></span>       | <span data-ttu-id="df22b-228">販売注文詳細</span><span class="sxs-lookup"><span data-stu-id="df22b-228">salesorderdetails</span></span>                 |             |
| <span data-ttu-id="df22b-229">販売注文元コード</span><span class="sxs-lookup"><span data-stu-id="df22b-229">Sales order origin codes</span></span>    | <span data-ttu-id="df22b-230">msdyn\_販売注文元</span><span class="sxs-lookup"><span data-stu-id="df22b-230">msdyn\_salesorderorigins</span></span>          |             |
| <span data-ttu-id="df22b-231">CDS 販売見積ヘッダー</span><span class="sxs-lookup"><span data-stu-id="df22b-231">CDS sales quotation header</span></span>  | <span data-ttu-id="df22b-232">見積</span><span class="sxs-lookup"><span data-stu-id="df22b-232">quotes</span></span>                            |             |
| <span data-ttu-id="df22b-233">CDS 販売見積明細行</span><span class="sxs-lookup"><span data-stu-id="df22b-233">CDS sales quotation lines</span></span>   | <span data-ttu-id="df22b-234">見積詳細</span><span class="sxs-lookup"><span data-stu-id="df22b-234">quotedetails</span></span>                      |             |

<span data-ttu-id="df22b-235">見込顧客の現金化に関連するコア エンティティ マップは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="df22b-235">Here are the related core entity maps for prospect-to-cash:</span></span>

+ [<span data-ttu-id="df22b-236">顧客 V3 を アカウントへ</span><span class="sxs-lookup"><span data-stu-id="df22b-236">Customers V3 to accounts</span></span>](customer-mapping.md#customers-v3-to-accounts)
+ [<span data-ttu-id="df22b-237">CDS 連絡先 V2 を連絡先へ</span><span class="sxs-lookup"><span data-stu-id="df22b-237">CDS Contacts V2 to contacts</span></span>](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [<span data-ttu-id="df22b-238">顧客 V3 を連絡先へ</span><span class="sxs-lookup"><span data-stu-id="df22b-238">Customers V3 to contacts</span></span>](customer-mapping.md#customers-v3-to-contacts)
+ [<span data-ttu-id="df22b-239">リリース済製品 V2 を msdyn_sharedproductdetails へ</span><span class="sxs-lookup"><span data-stu-id="df22b-239">Released products V2 to msdyn_sharedproductdetails</span></span>](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [<span data-ttu-id="df22b-240">すべての製品を msdyn_globalproducts へ</span><span class="sxs-lookup"><span data-stu-id="df22b-240">All products to msdyn_globalproducts</span></span>](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [<span data-ttu-id="df22b-241">価格表</span><span class="sxs-lookup"><span data-stu-id="df22b-241">Pricelist</span></span>](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
