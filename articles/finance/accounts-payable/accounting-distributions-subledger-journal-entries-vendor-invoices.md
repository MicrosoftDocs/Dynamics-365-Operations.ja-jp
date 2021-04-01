---
title: 仕入先請求書の勘定配布と元帳仕訳入力
description: 勘定配布は、仕入先請求書における経費、税金、または手数料などの計上方法など、金額をどのように計上するかを定義します。 仕入先請求書を仕訳入力するときに計上しなければならない金額にはいずれも一つ以上の勘定配布があります。
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0ad3124963dda33f44cf8ba6e6bb466029b2651
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252196"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a><span data-ttu-id="cd74c-104">仕入先請求書の勘定配布と元帳仕訳入力</span><span class="sxs-lookup"><span data-stu-id="cd74c-104">Accounting distributions and journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd74c-105">勘定配布は、仕入先請求書における経費、税金、または手数料などの計上方法など、金額をどのように計上するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="cd74c-106">仕入先請求書を仕訳入力するときに計上しなければならない金額にはいずれも一つ以上の勘定配布があります。</span><span class="sxs-lookup"><span data-stu-id="cd74c-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="cd74c-107">勘定配布</span><span class="sxs-lookup"><span data-stu-id="cd74c-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="cd74c-108">[仕入先請求書] ページでは、次のボタンで、仕入先請求書の各金額の勘定配布を表示したり、場合によっては変更できます。</span><span class="sxs-lookup"><span data-stu-id="cd74c-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="cd74c-109">**金額の配分** – 税または請求金額などの明細行と子行の勘定配布を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="cd74c-110">売上税トランザクション ページまたは諸費用トランザクション ページから子明細行の勘定配布を直接表示または変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="cd74c-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="cd74c-111">手数料や通貨の丸め金額など、仕入先請求書のヘッダー金額を変更します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="cd74c-112">仕入先請求書明細行金額を変更します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="cd74c-113">**配分の表示** – すべての伝票の明細行の勘定配布を表示します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="cd74c-114">このビューで勘定配布を変更できません。</span><span class="sxs-lookup"><span data-stu-id="cd74c-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="cd74c-115">表示のヘッダーと明細金額。</span><span class="sxs-lookup"><span data-stu-id="cd74c-115">View header and line amounts.</span></span>

<span data-ttu-id="cd74c-116">仕入先請求書で発注書を参照する場合、在庫がない品目が含まれる明細行では、勘定配布の分割や変更ができます。</span><span class="sxs-lookup"><span data-stu-id="cd74c-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="cd74c-117">仕入先請求書明細行が発注書明細行を参照しない場合、勘定を削除できます。</span><span class="sxs-lookup"><span data-stu-id="cd74c-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="cd74c-118">手数料、税金、行割引の明細行は、分割や削除ができません。</span><span class="sxs-lookup"><span data-stu-id="cd74c-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="cd74c-119">勘定科目は変更できますが、金額や割合は変更できません。</span><span class="sxs-lookup"><span data-stu-id="cd74c-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="cd74c-120">親行に在庫されていない品目が含まれ、勘定配布が分割されている場合、子の明細行は親行の財務分析コードに合わせて自動的に分割されます。</span><span class="sxs-lookup"><span data-stu-id="cd74c-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="cd74c-121">子の行の勘定配布は追加的に分割または削除できませんが、子明細行の設定に応じて、子の行の勘定配布の勘定科目を変更できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd74c-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="cd74c-122">金額の配分</span><span class="sxs-lookup"><span data-stu-id="cd74c-122">Distributing amounts</span></span>
<span data-ttu-id="cd74c-123">仕入先請求書を入力するとき、各金額は以下のように配置されます。</span><span class="sxs-lookup"><span data-stu-id="cd74c-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd74c-124">仕入先請求書明細行のタイプ</span><span class="sxs-lookup"><span data-stu-id="cd74c-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="cd74c-125">表示する主勘定のソースを決定する優先順位</span><span class="sxs-lookup"><span data-stu-id="cd74c-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="cd74c-126">表示される既定の財務分析コードを決定する優先順位</span><span class="sxs-lookup"><span data-stu-id="cd74c-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd74c-127">在庫製品</span><span class="sxs-lookup"><span data-stu-id="cd74c-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="cd74c-128">発注書明細行の勘定配布。</span><span class="sxs-lookup"><span data-stu-id="cd74c-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-129">[転記] ページで [製品の購買支出] が選択されている場合の [主勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-130">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-131">仕入先請求書では既定の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd74c-132">調達カテゴリまたは在庫にない製品</span><span class="sxs-lookup"><span data-stu-id="cd74c-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="cd74c-133">発注書明細行の勘定配布、仕入先請求書明細行が発注書明細行を参照する場合。</span><span class="sxs-lookup"><span data-stu-id="cd74c-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-134">[転記] ページで [支出の購買支出] が選択されている場合の [主勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-135">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-136">主勘定が配賦勘定の場合、配賦勘定定義の既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="cd74c-137">仕入先請求書では既定の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="cd74c-138">仕入先請求書明細行の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-139">[勘定科目表] ページで、主勘定の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd74c-140">固定資産</span><span class="sxs-lookup"><span data-stu-id="cd74c-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="cd74c-141">発注書明細行の勘定配布、仕入先請求書明細行が発注書明細行を参照する場合。</span><span class="sxs-lookup"><span data-stu-id="cd74c-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-142">[仕入先請求書] フォームの [トランザクション タイプ] フィールドで [取得] を選択した場合は、[固定資産の転記プロファイル] ページで [取得] が選択されているときの [主勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="cd74c-143">[トランザクション タイプ] フィールドで [取得原価調整] を選択した場合は、[固定資産の転記プロファイル] ページで [取得原価調整] が選択されているときの [主勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-144">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-145">仕入先請求書明細行の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-146">[勘定科目表] ページで、主勘定の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd74c-147">仕入先請求書明細行で定義したプロジェクト。</span><span class="sxs-lookup"><span data-stu-id="cd74c-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="cd74c-148">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-149">[プロジェクト グループ] ページで [原価の転記 - 品目] に [残高] を選択している場合は、[元帳転記の設定] ページで [原価] を選択しているときの [主勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="cd74c-150">[プロジェクト グループ] ページで [原価の転記 - 品目] に [損益] を選択している場合は、[元帳転記の設定] ページで [原価 - 品目] を選択しているときの [主勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-151">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd74c-152">行割引</span><span class="sxs-lookup"><span data-stu-id="cd74c-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="cd74c-153">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-154">[転記] ページで [割引] を選択しているときの [主勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="cd74c-155">割引の主勘定が転記プロファイルで定義されていない場合、発注書明細行の拡張価格の勘定配布。</span><span class="sxs-lookup"><span data-stu-id="cd74c-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-156">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-157">仕入先請求書明細行の拡張価格の勘定配布にある財務分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-158">仕入先請求書明細行の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-159">[勘定科目表] ページで、主勘定の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd74c-160">発注書明細行の [価格と割引] タブで入力する購買請求金額</span><span class="sxs-lookup"><span data-stu-id="cd74c-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="cd74c-161">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-162">発注書明細行の拡張価格の勘定配布。</span><span class="sxs-lookup"><span data-stu-id="cd74c-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-163">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-164">仕入先請求書明細行の拡張価格の勘定配布にある財務分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd74c-165">明細行手数料</span><span class="sxs-lookup"><span data-stu-id="cd74c-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="cd74c-166">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-167">[雑費コード] フォームの [借方タイプ] フィールドで [勘定科目] を選択した場合、[雑費コード] ページの [借方勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="cd74c-168">[雑費コード] フォームの [借方タイプ] フィールドで [品目] を選択した場合、発注書明細行の拡張価格の勘定配布。</span><span class="sxs-lookup"><span data-stu-id="cd74c-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-169">[雑費コード] フォームの [借方タイプ] フィールドで [顧客/仕入先] を選択した場合、[雑費コード] ページの [貸方勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-170">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-171">仕入先請求書明細行の拡張価格の勘定配布にある財務分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-172">仕入先請求書明細行の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-173">[勘定科目表] ページで、主勘定の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd74c-174">次の条件の税:</span><span class="sxs-lookup"><span data-stu-id="cd74c-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="cd74c-175">[米国課税ルールの適用] オプションが [総勘定元帳パラメーター] ページで選択されています。</span><span class="sxs-lookup"><span data-stu-id="cd74c-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="cd74c-176">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-177">拡張価格または請求金額の勘定配布。</span><span class="sxs-lookup"><span data-stu-id="cd74c-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-178">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-179">仕入先請求書明細行の拡張価格の勘定配布にある財務分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-180">仕入先請求書明細行の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd74c-181">次の条件の税:</span><span class="sxs-lookup"><span data-stu-id="cd74c-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="cd74c-182">[米国課税ルールの適用] オプションが [総勘定元帳パラメーター] ページで選択されていません。</span><span class="sxs-lookup"><span data-stu-id="cd74c-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="cd74c-183">売上税グループの [利用税] フィールドが、[売上税グループ] ページで選択されていません。</span><span class="sxs-lookup"><span data-stu-id="cd74c-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="cd74c-184">税額が回収可能な場合は、[元帳転記グループ] ページの [売上税収入] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="cd74c-185">税金を回収できない場合、請求金額の拡張価格または勘定配布。</span><span class="sxs-lookup"><span data-stu-id="cd74c-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-186">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-187">仕入先請求書明細行の請求金額の拡張価格または勘定配布にある財務分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-188">仕入先請求書明細行の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-189">[勘定科目表] ページで、主勘定の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd74c-190">次の条件の税:</span><span class="sxs-lookup"><span data-stu-id="cd74c-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="cd74c-191">[米国課税ルールの適用] オプションが [総勘定元帳パラメーター] ページで選択されていません。</span><span class="sxs-lookup"><span data-stu-id="cd74c-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="cd74c-192">売上税グループの [利用税] フィールドが、[売上税グループ] ページで選択されています。</span><span class="sxs-lookup"><span data-stu-id="cd74c-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="cd74c-193">税額が回収可能な場合は、[元帳転記グループ] ページの [売上税収入] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="cd74c-194">税額が回収不能な場合は、[元帳転記グループ] ページの [使用税経費] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-195">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-196">仕入先請求書明細行の請求金額の拡張価格または勘定配布にある財務分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-197">仕入先請求書明細行の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-198">[勘定科目表] ページで、主勘定の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd74c-199">ヘッダー請求金額</span><span class="sxs-lookup"><span data-stu-id="cd74c-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="cd74c-200">[雑費コード] フォームの [借方タイプ] フィールドで [勘定科目] を選択した場合、[雑費コード] ページの [借方勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="cd74c-201">[雑費コード] フォームの [借方タイプ] フィールドで [顧客/仕入先] を選択した場合、[雑費コード] ページの [貸方勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-202">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-203">主勘定が配賦勘定の場合、配賦勘定定義の既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="cd74c-204">仕入先請求書ヘッダーにある財務分析コードの既定のテンプレートの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="cd74c-205">仕入先請求書明細行の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-206">[勘定科目表] ページで、主勘定の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd74c-207">ヘッダー割引</span><span class="sxs-lookup"><span data-stu-id="cd74c-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="cd74c-208">[自動トランザクションの勘定] ページの、仕入先請求書の割引転記のタイプについての [主勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="cd74c-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="cd74c-209">請求書明細行が発注書明細行を参照する場合、発注書明細行の勘定配布を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="cd74c-210">仕入先請求書明細行の拡張価格の勘定配布にある財務分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-211">仕入先請求書明細行の財務分析コード値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="cd74c-212">[勘定科目表] ページで、主勘定の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="cd74c-213">税の配分</span><span class="sxs-lookup"><span data-stu-id="cd74c-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="cd74c-214">税金の勘定配布は、税金が計算されるまで作成できません。</span><span class="sxs-lookup"><span data-stu-id="cd74c-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="cd74c-215">売上税を計算するには、[仕入先請求書] ページで次の作業のいずれかを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd74c-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="cd74c-216">請求金額の合計を表示する。</span><span class="sxs-lookup"><span data-stu-id="cd74c-216">View the invoice total.</span></span>
-   <span data-ttu-id="cd74c-217">売上税を表示する。</span><span class="sxs-lookup"><span data-stu-id="cd74c-217">View the sales tax.</span></span>
-   <span data-ttu-id="cd74c-218">補助元帳を表示する。</span><span class="sxs-lookup"><span data-stu-id="cd74c-218">View the subledger journal.</span></span>
-   <span data-ttu-id="cd74c-219">全仕入先請求書の勘定配布を表示します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="cd74c-220">仕入先請求書を保留にします。</span><span class="sxs-lookup"><span data-stu-id="cd74c-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="cd74c-221">仕入先請求書の転記</span><span class="sxs-lookup"><span data-stu-id="cd74c-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="cd74c-222">仕入先請求書の関連会社の補助元帳仕訳帳</span><span class="sxs-lookup"><span data-stu-id="cd74c-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="cd74c-223">仕入先請求書を転記する前に、請求書が正しい勘定に転記されていることを確認するため、借方と貸方がある請求書の全勘定項目を表示できます。</span><span class="sxs-lookup"><span data-stu-id="cd74c-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="cd74c-224">全勘定項目の表示は補助元帳と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="cd74c-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="cd74c-225">仕入先請求書に仕訳入力する前に、プレビューした結果、補助元帳仕訳が正しくない場合、補助元帳仕訳は変更できません。</span><span class="sxs-lookup"><span data-stu-id="cd74c-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="cd74c-226">代わりに、勘定配布または転記プロファイルを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd74c-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="cd74c-227">勘定配布は、勘定項目の借方または貸方のいずれか一方を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cd74c-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="cd74c-228">相殺補助元帳仕訳勘定項目は、仕入先勘定または税などの転記プロファイルから作成します。</span><span class="sxs-lookup"><span data-stu-id="cd74c-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]