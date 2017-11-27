---
title: "仕入先リベート"
description: "このトピックでは、仕入先のリベートを作業する場合に実行する、最も一般的なタスクの概要を示します。 仕入先のリベートは、取得したリベートを管理、追跡、および申請するために必要なタスクを自動化することにより、仕入れ先のリベートプログラムを会社が効率的に管理できるようにします。"
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ae5ee60238b951779c7790870e6c6adfba55d7d
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-rebates"></a><span data-ttu-id="1166e-104">仕入先リベート</span><span class="sxs-lookup"><span data-stu-id="1166e-104">Vendor rebates</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="1166e-105">仕入先のリベートは、取得したリベートを管理、追跡、および申請するために必要なタスクを自動化することにより、仕入れ先のリベートプログラムを会社が効率的に管理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="1166e-105">Vendor rebates help companies better manage their supplier rebate programs by automating tasks that are required in order to administer, track, and claim rebates that are earned.</span></span>

<span data-ttu-id="1166e-106">このトピックでは、仕入先のリベートを作業する場合に実行する、最も一般的なタスクの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="1166e-106">This topic provides an overview of the most common tasks that you might want to perform when you work with vendor rebates.</span></span> <span data-ttu-id="1166e-107">概要では、次の作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="1166e-107">The overview covers the following tasks:</span></span>

- <span data-ttu-id="1166e-108">リベート契約の詳細をレビューします。</span><span class="sxs-lookup"><span data-stu-id="1166e-108">Review details of a rebate agreement.</span></span>
- <span data-ttu-id="1166e-109">リベートの条件を満たす注文を識別し、リベートの請求を生成します。</span><span class="sxs-lookup"><span data-stu-id="1166e-109">Identify orders that qualify for rebates, and generate rebate claims.</span></span>
- <span data-ttu-id="1166e-110">請求を確認および承認する。</span><span class="sxs-lookup"><span data-stu-id="1166e-110">Review and approve claims.</span></span>

## <a name="audience-and-purpose"></a><span data-ttu-id="1166e-111">対象者および目的</span><span class="sxs-lookup"><span data-stu-id="1166e-111">Audience and purpose</span></span>

<span data-ttu-id="1166e-112">このトピックの情報は、エンタープライズの会社での業務の意思決定者、購買マネージャーなどの職位、最高財務責任者 (CFO)、および会計マネージャーなどの、次の職責を対象としています。</span><span class="sxs-lookup"><span data-stu-id="1166e-112">The information in this topic is intended for business decision makers in enterprise companies, in positions such as purchase manager, chief financial officer (CFO), and accounting manager, who have the following responsibilities:</span></span>

- <span data-ttu-id="1166e-113">仕入先の価格、割引、リベート契約の交渉。</span><span class="sxs-lookup"><span data-stu-id="1166e-113">Negotiate vendor price, discount, and rebate agreements.</span></span>
- <span data-ttu-id="1166e-114">リベートの請求、および支払の回収を処理するスタッフの管理。</span><span class="sxs-lookup"><span data-stu-id="1166e-114">Manage staff that processes rebate claims and collects payments.</span></span>
- <span data-ttu-id="1166e-115">最も有利な価格での在庫の注文。</span><span class="sxs-lookup"><span data-stu-id="1166e-115">Order inventory at the best possible prices.</span></span>

<span data-ttu-id="1166e-116">これらの職位のユーザーは、これらの目標を達成する方法を求めています。</span><span class="sxs-lookup"><span data-stu-id="1166e-116">People in these positions are looking for ways to achieve various goals.</span></span> <span data-ttu-id="1166e-117">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="1166e-117">Here are some examples:</span></span>

- <span data-ttu-id="1166e-118">さまざまなタイプの仕入先のプロモーションプログラム、およびリベートの条件に柔軟に対応します。</span><span class="sxs-lookup"><span data-stu-id="1166e-118">Flexibly accommodate different types of vendor promotion programs and rebate conditions.</span></span>
- <span data-ttu-id="1166e-119">管理の負担、およびプロモーションのパフォーマンスの監視と請求の処理に関連付けられるエラーを減らします。</span><span class="sxs-lookup"><span data-stu-id="1166e-119">Reduce the administrative burden and errors that are associated with monitoring promotion performance and processing claims.</span></span>
- <span data-ttu-id="1166e-120">将来の売掛金の見越計上によりキャッシュフロー予測の精度が高まります。</span><span class="sxs-lookup"><span data-stu-id="1166e-120">Improve cash flow forecasts by accruing for future receivables.</span></span>
- <span data-ttu-id="1166e-121">リベートについて、仕入れ先との進行中、および将来の交渉に関する定量化された基準があります。</span><span class="sxs-lookup"><span data-stu-id="1166e-121">Have a quantified basis for ongoing and future negotiations with vendors about rebates.</span></span>

## <a name="review-details-of-a-vendor-rebate-agreement"></a><span data-ttu-id="1166e-122">仕入れ先リベート契約の詳細をレビューします。</span><span class="sxs-lookup"><span data-stu-id="1166e-122">Review details of a vendor rebate agreement</span></span>
<span data-ttu-id="1166e-123">仕入先リベート契約は、指定した交渉条件、および事前に設定した発注目標と引き換えに会社が金銭報酬を得ることができる条件を示した、仕入れ先との契約の記録です。</span><span class="sxs-lookup"><span data-stu-id="1166e-123">A vendor rebate agreement is a record of a contract with a vendor that specifies the negotiated terms and conditions under which the company qualifies for a monetary reward in return for achieving preset purchase targets.</span></span> <span data-ttu-id="1166e-124">仕入先リベート契約は**リベート契約**ページに記録されています。</span><span class="sxs-lookup"><span data-stu-id="1166e-124">Vendor rebate agreements are recorded on the **Rebate agreements** page.</span></span>

<span data-ttu-id="1166e-125">**仕入先のリベート契約**ページを開き、**調達**&gt;**仕入れ先のリベート**&gt;**リベート契約**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-125">To open the **Vendor rebate agreements** page, select **Procurement and sourcing** &gt; **Vendor rebates** &gt; **Rebate agreements**.</span></span>

![購買契約](media/purchase-agreement.PNG)

<span data-ttu-id="1166e-127">**仕入先リベート契約** ページで、仕入先契約の交渉による条件に関する詳細を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="1166e-127">On the **Vendor rebate agreements** page, you can view details about the negotiated conditions of a vendor agreement.</span></span>

<span data-ttu-id="1166e-128">契約書のヘッダーは、リベートの条件を満たす会社の一般的な条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="1166e-128">The agreement’s header specifies the general conditions that qualify a company for rebates.</span></span> <span data-ttu-id="1166e-129">実際には、特定の数量の特定の製品を購入したとき、ヘッダー情報は仕入れ先にリベートの付与を指定します。</span><span class="sxs-lookup"><span data-stu-id="1166e-129">In effect, the header information specifies that a vendor grants a rebate when a specific product is bought in a specific quantity.</span></span> <span data-ttu-id="1166e-130">ヘッダーで、リベートオプション、および計算日タイプの測定単位も指定します。</span><span class="sxs-lookup"><span data-stu-id="1166e-130">On the header, you also specify the unit of measure rebate option and the calculation date type.</span></span>

- <span data-ttu-id="1166e-131">**リベート オプションの測定単位**フィールドの**全般**タブで、測定単位がリベート請求を行う購買注文明細行の条件であるかどうかを定義できます。</span><span class="sxs-lookup"><span data-stu-id="1166e-131">On the **General** tab, in the **Unit of measure rebate option** field, you can define whether a unit of measure should be a condition for the purchase order line to qualify for a rebate claim.</span></span> 

    - <span data-ttu-id="1166e-132">**変換** – 購買注文明細行が、リベート契約ごとの仕入先リベートに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-132">**Convert** – A purchase order line qualifies for a vendor rebate per the rebate agreement.</span></span> <span data-ttu-id="1166e-133">明細行に適用される測定単位に関係なくリベートを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="1166e-133">You will receive a rebate regardless of the unit of measure that is applied on the line.</span></span>
    - <span data-ttu-id="1166e-134">**完全一致** – リベートを適用するには、購買注文明細行は契約で指定されたものと同じ測定単位を持っていなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1166e-134">**Exact match** – To qualify for a rebate, a purchase line must have the same unit of measure that is specified on the agreement.</span></span>

- <span data-ttu-id="1166e-135">**計算日タイプ**フィールド内の**全般**タブ上で、リベート契約の有効期間内で、購買を行うかどうかの決定に使用する日を選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-135">On the **General** tab, in the **Calculation date type** field, select the date that is used to determine whether the purchase occurs in the validity period of the rebate agreement.</span></span>

    - <span data-ttu-id="1166e-136">**作成日** – 発注書の作成日を使用します。</span><span class="sxs-lookup"><span data-stu-id="1166e-136">**Created** – Use the creation date of the purchase order.</span></span>
    - <span data-ttu-id="1166e-137">**配送指定日** – 指定された配送日を使用します。</span><span class="sxs-lookup"><span data-stu-id="1166e-137">**Requested delivery** – Use the requested delivery date.</span></span>

<span data-ttu-id="1166e-138">契約明細行に、仕入先リベート契約をさらに詳細に指定できます。</span><span class="sxs-lookup"><span data-stu-id="1166e-138">On the agreement lines, you can specify the vendor rebate agreement in more detail.</span></span>

- <span data-ttu-id="1166e-139">**購買の累計基準**フィールドで、リベート請求の計算を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1166e-139">In the **Cumulate purchase by** field, you can set the calculation of the rebate claim.</span></span> <span data-ttu-id="1166e-140">期間 (週、月、年、有効期間またはカスタマイズされた期間) に依存する量を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1166e-140">The amount can be set to depend on a period (of week, month, year, lifetime or a customized period).</span></span> <span data-ttu-id="1166e-141">**請求書**の値は、購買注文明細行が請求されるたびにリベート請求が毎回決定されることを示します。</span><span class="sxs-lookup"><span data-stu-id="1166e-141">The **Invoice** value indicates that a rebate claim will be determined every time that a purchase order line is invoiced.</span></span>
- <span data-ttu-id="1166e-142">**取得元**フィールドでは、リベート計算の基準を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="1166e-142">In the **Taken from** field, you can specify the basis for the rebate calculation.</span></span>

    - <span data-ttu-id="1166e-143">**総計** – 品目の価格総額に基づいてリベートが計算されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-143">**Gross** – The rebate is calculated based on the gross price of the item.</span></span>
    - <span data-ttu-id="1166e-144">**正味** – リベートは品目の正味価格 (他の割引適用後の価格) に基づき計算されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-144">**Net** – The rebate is calculated based on the net price of the item (that is, the price after other discounts have been applied).</span></span>

- <span data-ttu-id="1166e-145">**リベート プログラム見越勘定**および**リベート プログラム経費勘定**フィールドは、
承認と処理の間の中間のステージで受け取る未収リベート金額の勘定番号を示します。</span><span class="sxs-lookup"><span data-stu-id="1166e-145">The **Rebate program accrual account** and **Rebate program expense account** fields specify account numbers that will receive accrued rebate amounts during the intermediate stage between approval and processing.</span></span>
- <span data-ttu-id="1166e-146">**承認必須**オプションが**はい**にセットされた時、リベート請求が計上、もしくは支払われる前にリベート請求を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1166e-146">When the **Approval required** option is set to **Yes**, the rebate claim must be approved before it can be accrued or paid out.</span></span>
- <span data-ttu-id="1166e-147">**リベート改行タイプ**フィールドにはリベートの基準が示されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-147">The **Rebate line break type** field specifies the basis for the rebates.</span></span>

    - <span data-ttu-id="1166e-148">**数量** – リベートがボリュームベースになります。</span><span class="sxs-lookup"><span data-stu-id="1166e-148">**Quantity** – The rebates are volume-based.</span></span>
    - <span data-ttu-id="1166e-149">**金額** – リベートが金額ベースになります。</span><span class="sxs-lookup"><span data-stu-id="1166e-149">**Amount** – The rebates are amount-based.</span></span>

- <span data-ttu-id="1166e-150">**明細**クイック タブでは、各数量層が、リベートの許可をどのようにさまざまに設定できるか表示することができます。</span><span class="sxs-lookup"><span data-stu-id="1166e-150">On the **Lines** FastTab, you can see how different quantity tiers can be set up to grant different rebates.</span></span> <span data-ttu-id="1166e-151">たとえば、前述の図では、**範囲の開始値**および**範囲の終了値**フィールドは、10 から 19 ユニットの製品の数量ではユニット毎に USD 15 のリベートが支払われることを示しています。</span><span class="sxs-lookup"><span data-stu-id="1166e-151">For example, in the previous illustration, the **From value** and **To value** fields indicate that a product quantity between 10 and 19 units will qualify for a rebate of USD 15 per unit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1166e-152">**範囲の開始値**は含まれ、**範囲の終了値**は含まれません。</span><span class="sxs-lookup"><span data-stu-id="1166e-152">The **From value** value is inclusive, whereas the **To value** value is exclusive.</span></span> <span data-ttu-id="1166e-153">たとえば、**リベート改行タイプ**フィールドに**数量**が設定されていて、**範囲の開始値**フィールドに **1** を、**範囲の終了値**に **3** を入力します。</span><span class="sxs-lookup"><span data-stu-id="1166e-153">For example, the **Rebate line break type** field is set to **Quantity**, and you enter **1** in the **From value** field and **3** in the **To value** field.</span></span> <span data-ttu-id="1166e-154">この場合は、1 つか 2 つの品目を購入する際にリベート金額が適用されますが、3 つ目を購入する際は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1166e-154">In this case, the rebate amount applies when you purchase one or two items, but not when you purchase three items.</span></span>

- <span data-ttu-id="1166e-155">**ワークフローの承認状態**フィールドで、**承認済**値は契約の条件を満たしている発注書に契約が適用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="1166e-155">In the **Workflow approval status** field, the **Approved** value indicates that the agreement can be applied to purchase orders that meet the agreement’s conditions.</span></span>

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a><span data-ttu-id="1166e-156">リベートの条件を満たす注文を識別し、リベートの請求を生成します</span><span class="sxs-lookup"><span data-stu-id="1166e-156">Identify orders that qualify for rebates, and generate rebate claims</span></span>

<span data-ttu-id="1166e-157">リベート契約を行っている仕入れ先から発注書が配置されると、プログラムは仕入れ先からの今後の支払いクレジットを識別します。</span><span class="sxs-lookup"><span data-stu-id="1166e-157">When purchase orders are placed with a vendor that the company has a rebate agreement with, the program identifies any future vendor credit payments.</span></span> <span data-ttu-id="1166e-158">発注書にリベートが適用された場合、請求書が転機されるとすぐ、リベート請求がすべての注文明細行で生成されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-158">If the purchase orders qualify for a rebate, a rebate claim is generated for every order line as soon as a purchase invoice has been posted.</span></span> <span data-ttu-id="1166e-159">これは、自動プロセスです。</span><span class="sxs-lookup"><span data-stu-id="1166e-159">This process is automatic.</span></span> <span data-ttu-id="1166e-160">その後、予定のリベートを確認すること、およびリベートの利益率と製品コストへの影響を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="1166e-160">Later, you can review the expected rebates and see the impact of those rebates on the product’s cost and profit margin.</span></span>

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a><span data-ttu-id="1166e-161">仕入先のリベート契約ごとの購買注文明細行に適用されるリベートの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="1166e-161">View details of rebates that are applied to a purchase order line per the vendor rebate agreement</span></span>
1. <span data-ttu-id="1166e-162">**発注書**ページで注文明細行を選択し、**発注書明細行**&gt;**表示**&gt;**価格の詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-162">On the **Purchase order** page, select an order line, and then select **Purchase order line** &gt; **View** &gt; **Price details**.</span></span>
2. <span data-ttu-id="1166e-163">**価格の詳細**ページで、**リベート**クイックタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-163">On the **Price details** page, select the **Rebates** FastTab.</span></span>

<span data-ttu-id="1166e-164">リベートの情報は、**価格の詳細**ページの**利益見積**のセクションにある**仕入先リベート** フィールドでも表示されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-164">The rebate information is also shown in the **Vendor rebate** field in the **Margin estimation** section of the **Price details** page.</span></span>

> [!NOTE]
> <span data-ttu-id="1166e-165">**調達パラメーター**ページの**価格**タブで、**価格の詳細の有効化**オプションが**はい**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1166e-165">On the **Procurement and sourcing parameters** page, on the **Prices** tab, verify that the **Enable price details** option is set to **Yes**.</span></span> <span data-ttu-id="1166e-166">オプションが**いいえ**に設定されている場合、リベートを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="1166e-166">If the option is set to **No**, you won’t be able to view the rebates.</span></span>

## <a name="review-and-approve-claims"></a><span data-ttu-id="1166e-167">請求を確認および承認する</span><span class="sxs-lookup"><span data-stu-id="1166e-167">Review and approve claims</span></span>
<span data-ttu-id="1166e-168">生成されるリベート請求は、仕入先からの予測される将来の支払いを表します。</span><span class="sxs-lookup"><span data-stu-id="1166e-168">Rebate claims that are generated represent the future payments that can be expected from the vendor.</span></span> <span data-ttu-id="1166e-169">契約の所有者は通常、貸方票が仕入先に発行される前に請求の確認を行い承認します。</span><span class="sxs-lookup"><span data-stu-id="1166e-169">Before a credit note is issued to the vendor, the agreement owner typically wants to review the claims and approve them.</span></span> <span data-ttu-id="1166e-170">ただし、請求のステータスの注記が、その請求が承認プロセスを実行する準備ができているかどうか決定します。</span><span class="sxs-lookup"><span data-stu-id="1166e-170">However, note that the status of a claim determines whether the claim is ready to go through the approval process.</span></span>

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a><span data-ttu-id="1166e-171">請求と承認プロセスへの影響の状態</span><span class="sxs-lookup"><span data-stu-id="1166e-171">The status of claims and the effect on the approval process</span></span>
<span data-ttu-id="1166e-172">請求が生成された時、リベートが累積的基準で適用されている場合、その状態が**計算対象**に設定され、リベートが請求書ごとに適用されている場合、その状態が**計算済**に設定されます。
</span><span class="sxs-lookup"><span data-stu-id="1166e-172">When a claim is generated, its status is set to **To be calculated** if the rebate is granted on a cumulative basis or **Calculated** if the rebate is granted per invoice.</span></span> <span data-ttu-id="1166e-173">請求の状態が**計算対象**の場合、その請求は、累計機能で行われる計算プロセスを実行しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1166e-173">If the status of a claim is **To be calculated**, the claim must go through a calculation process that is handled by the Cumulate function.</span></span> <span data-ttu-id="1166e-174">**計算済**状態の請求のみ、承認プロセスに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1166e-174">Only claims that have a status of **Calculated** can be included in the approval process.</span></span>

> [!NOTE]
> <span data-ttu-id="1166e-175">仕入先のリベート契約の**承認が必要**オプションが**いいえ**に設定されている場合、生成される請求はすべて**承認済**の状態になります。</span><span class="sxs-lookup"><span data-stu-id="1166e-175">If the **Approval required** option on a vendor rebate agreement is set to **No**, any claims that are generated will have a status of **Approved**.</span></span> <span data-ttu-id="1166e-176">累積的な基準が適用されている請求の場合は、請求の承認が必須です。</span><span class="sxs-lookup"><span data-stu-id="1166e-176">The approval is mandatory for claims that are granted on a cumulative basis.</span></span>

### <a name="approve-claims-and-view-postings-and-invoice-details"></a><span data-ttu-id="1166e-177">請求の承認、および転記と請求書の詳細の表示</span><span class="sxs-lookup"><span data-stu-id="1166e-177">Approve claims, and view postings and invoice details</span></span>
<span data-ttu-id="1166e-178">請求が承認された時、買掛金勘定 (A/P) で処理されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-178">When claims have been approved, they can be processed by Accounts payable (A/P).</span></span> <span data-ttu-id="1166e-179">リベート請求金額のクレジット メモ (仕入先請求書) は、自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-179">A credit memo (vendor invoice) for the rebate claim amount is automatically generated.</span></span> <span data-ttu-id="1166e-180">クレジットは仕入先残高に追加することができ、A/P チームは通常の決済プロセスに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1166e-180">The credit can then be added to the vendor balance, and the A/P team can include it in the regular settlement process.</span></span>

1. <span data-ttu-id="1166e-181">**調達**&gt;**仕入先リベート**&gt;**リベート請求**を選択して、リベート請求を開きます。</span><span class="sxs-lookup"><span data-stu-id="1166e-181">Select **Procurement and sourcing** &gt; **Vendor Rebates** &gt; **Rebate claims** to open a rebate claim.</span></span>
2. <span data-ttu-id="1166e-182">リベート請求を閉じます。</span><span class="sxs-lookup"><span data-stu-id="1166e-182">Close the rebate claim.</span></span>
3. <span data-ttu-id="1166e-183">請求をマークしてから、アクション ペインにある**承認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-183">Mark the claim, and then, on the Action Pane, select **Approve**.</span></span>
4. <span data-ttu-id="1166e-184">**仕入先**フィールドの要求ページで、リベートの受け取りを承認した仕入先を選択し、それから **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-184">On the request page, in the **Vendor** field, select the vendor that you’re authorized to receive a rebate from, and then select **OK**.</span></span>

    <span data-ttu-id="1166e-185">リベート見越計上仕訳帳が請求金額に転記されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-185">A Rebate accrual journal is posted for the claim amount.</span></span> <span data-ttu-id="1166e-186">この転記は、予定仕入先貸方の見越計上仕入先リベートの未収勘定の借方に記入し、予定利益の中間見越計上仕入先リベートを適用した勘定の貸方に記入します。</span><span class="sxs-lookup"><span data-stu-id="1166e-186">This posting debits the Accrued Vendor Rebates Receivable account for the expected vendor credit and credits the interim Accrued Vendor Rebates Received account for the expected gain.</span></span>

    ![メッセージ](media/message.png)

5. <span data-ttu-id="1166e-188">リベートの一覧から明細行を選択します。次に、アクション ペインで**リベート トランザクション**を選択し、リベート見越計上の転記用の仕分けバッチ番号の参照、および移動を行います。</span><span class="sxs-lookup"><span data-stu-id="1166e-188">In the rebate list, select the line, and then, on the Action Pane, select **Rebate transactions** to see and navigate to the journal batch number for this rebate accrual posting.</span></span>

    <span data-ttu-id="1166e-189">通常の A/P プロセスに対する請求を移動するためには、A/P 係は実行中のプロセス機能でリベート請求処理を完了していなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1166e-189">To move the claims to the regular A/P process, the A/P clerk must now complete the rebate claim handling by running the Process function.</span></span>

6. <span data-ttu-id="1166e-190">アクション ペインで**プロセス**を選択し、**フィルター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-190">On the Action Pane, select **Process**, and then select **Filter**.</span></span> <span data-ttu-id="1166e-191">**仕入先**フィールドの**基準**フィールドで、リベート請求をプロセスしたい仕入先を選択します。その他の関連するフィルターを選択し、そして **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-191">In the **Criteria** field for the **Vendor account** field, select the vendor to process rebate claims for, select other relevant filters, and then select **OK**.</span></span>

    <span data-ttu-id="1166e-192">メッセージバー、および次のイベントが発生したことを示す**完了**に状態が変化するファクト。</span><span class="sxs-lookup"><span data-stu-id="1166e-192">The message bars and the fact that the status is changed to **Completed** indicate that the following events have occurred:</span></span>

    - <span data-ttu-id="1166e-193">リベート見越し計上仕訳帳の転記が、見越し売掛金、および経費勘定の以前の中間納付を取り消します。</span><span class="sxs-lookup"><span data-stu-id="1166e-193">A Rebate accrual journal posting has reversed the previous interim amounts on the accrual receivable and expense accounts.</span></span>
    - <span data-ttu-id="1166e-194">リベート金額の仕入先請求書 (訂正票) が作成されました。</span><span class="sxs-lookup"><span data-stu-id="1166e-194">A vendor invoice (credit note) for the rebate amount has been created.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1166e-195">**調達パラメーター**ページの [**リベート プログラム**] タブにある**手動による請求書の転記**オプションの設定は、請求処理の一部として仕入先請求書を手動または自動で転記するか決定します。</span><span class="sxs-lookup"><span data-stu-id="1166e-195">The setting of the **Manual invoice posting** option on the **Rebate program** tab of the **Procurement and sourcing parameters** page determines whether a vendor invoice is posted manually or automatically as part of claim processing.</span></span>

    - <span data-ttu-id="1166e-196">仕入先請求書が転記された時、自動または手動で、仕入先の買掛金勘定は借方に転記され、割引が適用された勘定が貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-196">When the vendor invoice is posted, either automatically or manually, the vendor’s Payable account has been debited, and the Discounts and Allowances Received account has been credited.</span></span>

        > [!NOTE] 
        > <span data-ttu-id="1166e-197">リベートの仕入請求書明細行に使用された調達カテゴリに、割引が適用された勘定番号が指定されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-197">The Discounts and Allowances Received account number is specified for the procurement category that is used on the purchase invoice line for the rebate.</span></span> <span data-ttu-id="1166e-198">さらに、調達カテゴリは**調達パラメーター**ページの [**リベート プログラム**] タブに設定されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-198">The procurement category, in turn, is set on the **Rebate program** tab of the **Procurement and sourcing parameters** page.</span></span>

7. <span data-ttu-id="1166e-199">リベートの一覧から明細行を選択します。次に、アクション ペインで**リベート トランザクション**を選択し、リベート見越計上および仕入先請求書番号の仕分けバッチ番号の参照、および移動を行います。</span><span class="sxs-lookup"><span data-stu-id="1166e-199">In the rebate list, select the line, and then, on the Action Pane, select **Rebate transactions** to see and navigate to the journal batch number for this rebate accrual posting and also the vendor invoice number.</span></span>
8. <span data-ttu-id="1166e-200">仕入先請求書トランザクションの明細行を選択し、次に、アクション ペインの [**仕入先請求書**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-200">Select the line for the vendor invoice transaction, and then, on the Action Pane, select **Vendor invoice**.</span></span> <span data-ttu-id="1166e-201">仕入先請求書が転記されている場合、請求仕訳帳が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-201">If the vendor invoice has been posted, you will see the Invoice journal.</span></span> <span data-ttu-id="1166e-202">それ以外の場合、手動での転記が必要な保留中の仕入先請求書として表示されます。</span><span class="sxs-lookup"><span data-stu-id="1166e-202">Otherwise, you will see the vendor invoice as a pending vendor invoice that requires manual posting.</span></span>

    <span data-ttu-id="1166e-203">請求明細行は**コミッションおよびリベート**調達カテゴリの仕入先請求書の詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="1166e-203">The invoice line specifies the details of the vendor invoice for the **Commissions and Rebates** procurement category.</span></span>

9. <span data-ttu-id="1166e-204">**すべての仕入先**ページからリベートを受け取った仕入先を選択し、次に、アクション ペインの [**トランザクション**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1166e-204">On the **All vendors** page, select the vendor that you receive a rebate from, and then, on the Action Pane, select **Transactions**.</span></span> <span data-ttu-id="1166e-205">請求書の明細行を検索します。</span><span class="sxs-lookup"><span data-stu-id="1166e-205">Find the line for the invoice.</span></span> <span data-ttu-id="1166e-206">リベート金額が仕入先残高に追加されています。</span><span class="sxs-lookup"><span data-stu-id="1166e-206">The rebate amount has now been added to the vendor balance.</span></span>

## <a name="summary"></a><span data-ttu-id="1166e-207">集計</span><span class="sxs-lookup"><span data-stu-id="1166e-207">Summary</span></span>
<span data-ttu-id="1166e-208">仕入先リベートの処理には、うんざりさせられる手動での複数の追跡タスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1166e-208">The process for handling vendor rebates involves multiple manual tracking tasks that are often tedious.</span></span> <span data-ttu-id="1166e-209">仕入先リベートの管理機能はこれらのタスクを自動化することにより、次のプロセスへの移行が容易になります。</span><span class="sxs-lookup"><span data-stu-id="1166e-209">By automating these tasks, the vendor rebate management feature can help you move through the following processes:</span></span>

- <span data-ttu-id="1166e-210">正確なリベート請求の作成</span><span class="sxs-lookup"><span data-stu-id="1166e-210">Generating accurate rebate claims</span></span>
- <span data-ttu-id="1166e-211">一般会計で予定された売掛および中間利益の発生。</span><span class="sxs-lookup"><span data-stu-id="1166e-211">Accruing the expected receivable and interim gain in the general ledger</span></span>
- <span data-ttu-id="1166e-212">割引の期日を迎えた仕入先残高と損益計算書の更新</span><span class="sxs-lookup"><span data-stu-id="1166e-212">Updating the vendor balance and the income statement with the allowance that is due</span></span>

