---
title: リベート管理モジュールの概要
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management のリベート管理モジュールの概要を示します。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: d271d70791a8fe4ad1581ae8a150ad13bffc7a94
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271056"
---
# <a name="rebate-management-module-overview"></a><span data-ttu-id="6aa89-103">リベート管理モジュールの概要</span><span class="sxs-lookup"><span data-stu-id="6aa89-103">Rebate management module overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6aa89-104">**リベート管理** モジュールを使用して、取引とその顧客または仕入先との間で契約、取引、または契約を作成し、リベート、控除、ロイヤリティを計算 できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-104">You can use the **Rebate management** module to create contracts, deals, or agreements between your business and its customers or vendors, so that you can calculate rebates, deductions, and royalties.</span></span> <span data-ttu-id="6aa89-105">リベート管理では、ユーザーが効率的にリベートトランザクションを作成、確認、処理できる中央の場所で、リベート トランザクションと控除トランザクションを追跡および管理します。</span><span class="sxs-lookup"><span data-stu-id="6aa89-105">Rebate management tracks and maintains rebate and deduction transactions in a central location where users can effectively create, review, and process them.</span></span>

<span data-ttu-id="6aa89-106">リベート管理では、*リベート* の作成、管理、処理をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6aa89-106">Rebate management supports the creation, maintenance, and processing of *rebates*.</span></span> <span data-ttu-id="6aa89-107">リベートは、販売者または買い手が購買価格の一部を返品する方法です。</span><span class="sxs-lookup"><span data-stu-id="6aa89-107">A rebate is the return of part of the purchase price by a seller or a buyer.</span></span> <span data-ttu-id="6aa89-108">リベートは通常、特定の期間に特定の数量または商品価値を購入した場合に基づいて実行されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-108">Rebates are typically based on the purchase of a specific quantity or value of goods during a specific period.</span></span> <span data-ttu-id="6aa89-109">割引とは異なり、リベートは購買金額が完全に請求された後に行われます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-109">Unlike discounts, rebates are done after the purchase amount is fully invoiced.</span></span>

<span data-ttu-id="6aa89-110">リベート管理では、*控除* もサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-110">Rebate management also supports *deductions*.</span></span> <span data-ttu-id="6aa89-111">控除とは、権利付与、著作権、特許などの知的財産を使用するライセンスか特権、あるいは権限、あるいは権限の付与によって生み出される報酬、検討事項、または手数料です。また、権限付与などの目的でナチュラル リソースを使用する特権のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="6aa89-111">A deduction is compensation, a consideration, or a fee that is paid either for a license or the privilege to use intellectual property such as a brand, copyright, or patent, or for the privilege to use a natural resource for a purpose such as for fishing, hunting, or mining.</span></span> <span data-ttu-id="6aa89-112">控除は通常、実現利用の収益または利益の割合として計算されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-112">Deductions are usually calculated as a percentage of the revenue or profit from realized use.</span></span> <span data-ttu-id="6aa89-113">知的財産または自然リソースが多く使用される場合、控除額が多く適用されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-113">The more the intellectual property or natural resource is used, the greater the deduction that is realized.</span></span>

<span data-ttu-id="6aa89-114">また、リベート管理では、顧客 *ロイヤリティ* もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6aa89-114">Additionally, Rebate management supports customer *royalties*.</span></span> <span data-ttu-id="6aa89-115">ロイヤリティは、ある当事者が資産を使用する権利のためにライセンスを得た場合または変更を行う支払です。</span><span class="sxs-lookup"><span data-stu-id="6aa89-115">Royalties are payments that one party makes to the licensee or franchisee for the right to use an asset.</span></span>

<span data-ttu-id="6aa89-116">リベート管理を使用すると、規定、リベート、元帳の転記プロファイルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-116">Rebate management lets you define posting profiles for provisions, rebates, and write-offs.</span></span> <span data-ttu-id="6aa89-117">さらに、特定の顧客または仕入先に対して転記を定義できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-117">Furthermore, the postings can be defined for a specific customer or vendor.</span></span> <span data-ttu-id="6aa89-118">これにより、一部の顧客シナリオや仕入先シナリオには適用されない取引を転記によって追跡できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-118">In this way, deals that don't apply to all customer or vendor scenarios can be tracked via postings.</span></span>

<span data-ttu-id="6aa89-119">リベート トランザクションは、バッチ ジョブで選択やスケジュールされた計算方法に基づいて自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-119">Rebate transactions are automatically generated, based on the calculation method that is selected and scheduled in batch jobs.</span></span> <span data-ttu-id="6aa89-120">また、契約を管理、確認、承認するためのワークフローも設定できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-120">Additionally, you can set up workflows to manage, review, and approve agreements.</span></span>

## <a name="basis-calculation"></a><span data-ttu-id="6aa89-121">計算基準</span><span class="sxs-lookup"><span data-stu-id="6aa89-121">Basis calculation</span></span>

<span data-ttu-id="6aa89-122">顧客リベート、顧客ロイヤリティ、仕入先リベートはすべて、業務要件に応じて異なる基準を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-122">Customer rebates, customer royalties, and vendor rebates can all use a different basis, depending on your business requirements:</span></span>

- <span data-ttu-id="6aa89-123">顧客リベートは、販売注文、配送メモ、または請求書に基づいて設定できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-123">Customer rebates can be based on sales orders, delivery notes, or invoices.</span></span>
- <span data-ttu-id="6aa89-124">顧客ロイヤリティは、販売注文、配送メモ、または支払い済みの請求書に基づいて設定できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-124">Customer royalties can be based on sales orders, delivery notes, or paid invoices.</span></span>
- <span data-ttu-id="6aa89-125">仕入先リベートは、発注書や販売注文に基づく場合があります。</span><span class="sxs-lookup"><span data-stu-id="6aa89-125">Vendor rebates can be based on either purchase orders or sales orders.</span></span> <span data-ttu-id="6aa89-126">リベート仕入先から購入され、売上請求書を通じて顧客に販売される製品に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-126">They can be calculated based on products that are purchased from the rebate vendor and sold to customers via sales invoices.</span></span>

## <a name="flexible-calculations"></a><span data-ttu-id="6aa89-127">柔軟な計算</span><span class="sxs-lookup"><span data-stu-id="6aa89-127">Flexible calculations</span></span>

<span data-ttu-id="6aa89-128">リベート計算期間は、顧客取引と仕入先取引の両方で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-128">Rebate calculation periods are available for both customer deals and vendor deals.</span></span> <span data-ttu-id="6aa89-129">計算期間は、契約の長さ、計算頻度、計算期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="6aa89-129">A calculation period defines the length of the deal, the calculation frequency, and the calculation period.</span></span> <span data-ttu-id="6aa89-130">リベートは、リベート期間中の、資格のある製品の販売注文数量または金額に基づいて見越計上できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-130">The rebates can be accrued based on the sales order quantities or amounts for qualified products during the rebate period.</span></span>

<span data-ttu-id="6aa89-131">各契約の計算に対して、次の期間を設定できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-131">For each agreement calculation, any of the following periods can be set:</span></span>

- <span data-ttu-id="6aa89-132">請求書</span><span class="sxs-lookup"><span data-stu-id="6aa89-132">Invoice</span></span>
- <span data-ttu-id="6aa89-133">日</span><span class="sxs-lookup"><span data-stu-id="6aa89-133">Day</span></span>
- <span data-ttu-id="6aa89-134">週</span><span class="sxs-lookup"><span data-stu-id="6aa89-134">Week</span></span>
- <span data-ttu-id="6aa89-135">月</span><span class="sxs-lookup"><span data-stu-id="6aa89-135">Month</span></span>
- <span data-ttu-id="6aa89-136">四半期</span><span class="sxs-lookup"><span data-stu-id="6aa89-136">Quarter</span></span>
- <span data-ttu-id="6aa89-137">年</span><span class="sxs-lookup"><span data-stu-id="6aa89-137">Year</span></span>
- <span data-ttu-id="6aa89-138">カスタマイズされた期間</span><span class="sxs-lookup"><span data-stu-id="6aa89-138">Customized period</span></span>
- <span data-ttu-id="6aa89-139">以前に表示した任意の期間の任意の倍数</span><span class="sxs-lookup"><span data-stu-id="6aa89-139">Any multiple of any of the previously listed periods</span></span>

<span data-ttu-id="6aa89-140">この計算は、個々の顧客と製品、顧客と製品のグループ、またはすべての顧客と製品に適用できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-140">The calculation can be applied to individual customers and products, groups of customers and products, or all customers and products.</span></span> <span data-ttu-id="6aa89-141">複数の詳細明細行を持つリベートには、異なる資格日の範囲を設定できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-141">Rebates that have multiple detail lines can have different qualifying date ranges.</span></span> <span data-ttu-id="6aa89-142">プロビジョニング期間とクレーム期間は異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6aa89-142">The provision and claim periods can differ.</span></span> <span data-ttu-id="6aa89-143">たとえば、プロビジョニングは毎日処理されるのに対し、クレームは毎月 1 回処理します。</span><span class="sxs-lookup"><span data-stu-id="6aa89-143">For example, provisions can be processed every day, whereas claims are processed once per month.</span></span>

<span data-ttu-id="6aa89-144">リベートは、さまざまなパラメータに基づいて設定できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-144">Rebates can be configured based on many different parameters.</span></span> <span data-ttu-id="6aa89-145">たとえば、割合、レート、または固定金額として構成できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-145">For example, they can be configured as a percentage, a rate, or a fixed amount.</span></span> <span data-ttu-id="6aa89-146">主要な計算方法は次の 4 種類があります。</span><span class="sxs-lookup"><span data-stu-id="6aa89-146">There are four main calculation methods:</span></span>

- <span data-ttu-id="6aa89-147">段階的</span><span class="sxs-lookup"><span data-stu-id="6aa89-147">Stepped</span></span>
- <span data-ttu-id="6aa89-148">累計</span><span class="sxs-lookup"><span data-stu-id="6aa89-148">Cumulative</span></span>
- <span data-ttu-id="6aa89-149">ローリング</span><span class="sxs-lookup"><span data-stu-id="6aa89-149">Rolling</span></span>
- <span data-ttu-id="6aa89-150">合計金額</span><span class="sxs-lookup"><span data-stu-id="6aa89-150">Total value</span></span>

<span data-ttu-id="6aa89-151">正味金額に基づいてリベートを計算するためにリベートを設定するかどうかに応じて、リベートの計算結果を他のリベートから減額もできます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-151">Rebate calculation results can also be reduced by other rebates, depending on whether the rebate is set up to calculate based on the net amount.</span></span>

<span data-ttu-id="6aa89-152">仕入先側では、販売注文に基づくリベートは先入れ先出し (FIFO) ルール、最新の購買価格、平均購買価格、または販売価格に基づいて価格を計算できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-152">On the vendor side, rebates that are based on sales orders can calculate the price based on a first in, first out (FIFO) rule, the latest purchase price, the average purchase price, or the sales price.</span></span>

## <a name="rebate-target-transactions"></a><span data-ttu-id="6aa89-153">リベート ターゲット トランザクション</span><span class="sxs-lookup"><span data-stu-id="6aa89-153">Rebate target transactions</span></span>

<span data-ttu-id="6aa89-154">リベート取引または契約によって生成される出力は、財務または品目です。</span><span class="sxs-lookup"><span data-stu-id="6aa89-154">The outputs that the rebate deal or agreement generates can be financials or items.</span></span>

<span data-ttu-id="6aa89-155">財務出力は、転記プロファイルから協定に割り当てられる支払タイプによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-155">Financial outputs are determined by the payment type that is assigned to the agreement from the posting profile.</span></span> <span data-ttu-id="6aa89-156">これらの出力には、顧客控除仕訳帳、自由形式請求書、仕入先請求書が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-156">These outputs can include customer deduction journals, free text invoices, and vendor invoices.</span></span> <span data-ttu-id="6aa89-157">監査目的で、財務リベート ターゲット トランザクションには、元のリベート契約への照会が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-157">For auditing purposes, financial rebate target transactions include a reference to the originating rebate agreement.</span></span>

<span data-ttu-id="6aa89-158">品目の出力によって、顧客リベートの無料の品目販売注文と、仕入先リベートの発注書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-158">Item outputs create a free item sales order for customer rebates and a purchase order for vendor rebates.</span></span> <span data-ttu-id="6aa89-159">品目リベート ターゲット トランザクションには、自由品目の販売注文または発注書に入力するリベートの参照を決定するオプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-159">Item rebate target transactions contain options to determine which rebate reference should be entered on the free item sales order or purchase order.</span></span>

## <a name="accurate-rebate-calculations"></a><span data-ttu-id="6aa89-160">正確なリベート計算</span><span class="sxs-lookup"><span data-stu-id="6aa89-160">Accurate rebate calculations</span></span>

<span data-ttu-id="6aa89-161">関連付けられた取引、計算の頻度、計算の基準、選択された計算方法の組み合わせによって、リベート計算の精度と精度を決めます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-161">The combination of the associated deals, the frequency of the calculations, the calculation basis, and the calculation method that is selected determines the accuracy and precision of rebate calculations.</span></span> <span data-ttu-id="6aa89-162">リベートのプロビジョニングは、転記された価値および請求額を見越計上するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-162">Rebate provisions can be used to accrue posted and claimed values.</span></span>

<span data-ttu-id="6aa89-163">プロビジョニングは、毎日、毎週、毎月、またはカスタム期間に従って管理できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-163">Provisions can be managed daily, weekly, monthly, or according to a custom period.</span></span> <span data-ttu-id="6aa89-164">ただし、この機能は、プロビジョニング頻度と同じかそれより長い定義済みの頻度で、リベートの割り当てまたは支払を行ったり、リベートの支払いを受け取ったりすることができます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-164">However, the functionality can allocate or pay the rebate, or receive payment of it, at any defined frequency that is the same length as or longer than the provision frequency.</span></span> <span data-ttu-id="6aa89-165">損金処理ではリベートと同じ頻度が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-165">Write-off uses the same frequency as the rebate.</span></span> <span data-ttu-id="6aa89-166">ユーザーは、支払期間中いつでも簡単に計画額または支払額を調整できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-166">Users can easily adjust a plan or payment amounts at any time during the payout.</span></span>

<span data-ttu-id="6aa89-167">ユーザーは、2 つの手順で取引または繰り入を処理する必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="6aa89-167">Users no longer have to handle deals or provisions in two steps.</span></span> <span data-ttu-id="6aa89-168">プロビジョニングと書き替えは、元帳に直接転記されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-168">Provisions and write-offs are posted directly to the ledger.</span></span> <span data-ttu-id="6aa89-169">また、訂正票は自動的に作成できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-169">Additionally, credit notes can be created automatically.</span></span> <span data-ttu-id="6aa89-170">このため、買掛金勘定と売掛金勘定は完全に統合されています。</span><span class="sxs-lookup"><span data-stu-id="6aa89-170">Therefore, there is full integration with accounts payable and accounts receivable.</span></span> <span data-ttu-id="6aa89-171">この処理では、決済割引、支払済請求書、取引割引、既存の貸方表が考慮され、金額と金額が正確に計算できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-171">During processing, the calculations can consider settlement discounts, paid invoices, trade discounts, and existing credit notes to ensure that amounts and values are accurately calculated.</span></span>

<span data-ttu-id="6aa89-172">リベートを計算すると、転記が行われる前に確認できるトランザクションがプロセスによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-172">When rebates are calculated, the process creates transactions that can be reviewed before posting occurs.</span></span> <span data-ttu-id="6aa89-173">別のプロセスは、リベート管理トランザクションを転記することです。</span><span class="sxs-lookup"><span data-stu-id="6aa89-173">A separate process posts rebate management transactions.</span></span> <span data-ttu-id="6aa89-174">提案されたトランザクションへの転記時に、仕訳帳、貸方伝票、または借方トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-174">A journal, credit note, or debit transaction can then be created during posting to proposed transactions.</span></span> <span data-ttu-id="6aa89-175">レポート明細書とトランザクション リストは、コンプライアンス、有効性、透明性を確保するために取得できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-175">Reporting statements and transaction listings can be obtained to ensure compliance, effectiveness, and transparency.</span></span>


## <a name="guaranteed-royalty-payments"></a><span data-ttu-id="6aa89-176">保証ロイヤリティ支払</span><span class="sxs-lookup"><span data-stu-id="6aa89-176">Guaranteed royalty payments</span></span>

<span data-ttu-id="6aa89-177">リベート管理では、最小が保証されている場合でも、自動支払生成により、ロイヤリティをすばやく簡単に処理できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-177">In Rebate management, automatic payment generation enables royalties to be handled quickly and easily, even when guaranteed minimums apply.</span></span> 

## <a name="maximizing-spend-versus-rebates"></a><span data-ttu-id="6aa89-178">支出とリベートの最大化</span><span class="sxs-lookup"><span data-stu-id="6aa89-178">Maximizing spend versus rebates</span></span>

<span data-ttu-id="6aa89-179">仕入先や製品を地域別にグループ化し、トランザクションの国または地域に応じて提供できるサービスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-179">Vendors and products can be grouped by territory, and different offers can be provided, depending on the country or region of the transaction.</span></span> <span data-ttu-id="6aa89-180">ユーザーが製品を選択すると、含まれる品目と、リベート決済で使用される品目の数を定義できます。</span><span class="sxs-lookup"><span data-stu-id="6aa89-180">When users select products, they can define the items that are included and the number of items that will be used in the rebate settlement.</span></span>
