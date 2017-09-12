---
title: " 会計またはレポートの通貨換算"
description: 
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 363543f8befacbf2e1b3ab28e6b9f14a5caf3c10
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a><span data-ttu-id="c6d8d-102"> 会計またはレポートの通貨換算</span><span class="sxs-lookup"><span data-stu-id="c6d8d-102">Convert accounting or reporting currencies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c6d8d-103">会計通貨やレポート通貨を変更する必要のある会社には、2 つの選択肢があります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-103">A company that must change its accounting currency or reporting currency has two options.</span></span> <span data-ttu-id="c6d8d-104">1 つ目の選択肢は、新しい会社を作成して新規に開始することです。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-104">The first option is to create a new company and start fresh.</span></span> <span data-ttu-id="c6d8d-105">2 番目の選択肢は、会計通貨とレポート通貨の換算プロセスを実行することです。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-105">The second option is to run the accounting and reporting currency conversion process.</span></span> <span data-ttu-id="c6d8d-106">これは、システムのすべてのトランザクションを変更する、長い実行時間のプロセスです。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-106">This is a very long-running process that changes every transaction in the system.</span></span> <span data-ttu-id="c6d8d-107">また、プロセスを実行する前に、設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-107">Some setup is also required before the process can be run.</span></span>

## <a name="preparing-the-legal-entity-for-currency-conversion"></a><span data-ttu-id="c6d8d-108">通貨の換算用の法人の準備</span><span class="sxs-lookup"><span data-stu-id="c6d8d-108">Preparing the legal entity for currency conversion</span></span>
<span data-ttu-id="c6d8d-109">その法人の通貨を換算できるようにするには、顧客および仕入先勘定の外貨再評価金額を元に戻し、前会計年度を閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-109">Before you can convert the legal entity’s currency, you must revert any foreign currency revaluation amounts for customer and vendor accounts, and close the previous fiscal years.</span></span> <span data-ttu-id="c6d8d-110">また、変換用のデータベースを準備し、それから通貨換算を実行中の法人の口座に必要な変更を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-110">You must also prepare the database for the conversion, and then make the required changes to the legal entity’s account that is undergoing the currency conversion.</span></span> <span data-ttu-id="c6d8d-111">通貨の換算を完了したら、実行の必要な追加手順がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-111">After you have completed a currency conversion, you must complete some additional procedures.</span></span> <span data-ttu-id="c6d8d-112">実行する必要がありるのは、換算した金額の丸め差額の調整、業務統計の再計算、元帳トランザクションの仕訳入力、換算ツールへのアクセスの制限、顧客勘定および仕入先勘定の外貨金額の再評価です。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-112">You must reconcile rounding differences in converted amounts, recalculate business statistics, journalize the ledger transactions, limit access to the conversion tool, and revalue foreign currency amounts for customer and vendor accounts.</span></span>

## <a name="setting-up-accounts-for-automatic-transactions"></a><span data-ttu-id="c6d8d-113">自動トランザクションの勘定の設定</span><span class="sxs-lookup"><span data-stu-id="c6d8d-113">Setting up accounts for automatic transactions</span></span>
<span data-ttu-id="c6d8d-114">通貨の換算プロセスの間に、その差益または差損、または小額差分は、**自動トランザクションの勘定**ページで定義された勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-114">During the currency conversion process, gains or losses, or penny differences, are posted to the accounts that are defined on the **Accounts for automatic transactions** page.</span></span> <span data-ttu-id="c6d8d-115">主勘定は、換算プロセスを実行する前に、次のタイプのトランザクションに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-115">Main accounts must be assigned to the following types of transaction before the conversion process is run:</span></span>

-   <span data-ttu-id="c6d8d-116">会計通貨換算差益</span><span class="sxs-lookup"><span data-stu-id="c6d8d-116">Accounting currency conversion gain</span></span>
-   <span data-ttu-id="c6d8d-117">会計通貨換算差損</span><span class="sxs-lookup"><span data-stu-id="c6d8d-117">Accounting currency conversion loss</span></span>
-   <span data-ttu-id="c6d8d-118">会計通貨での小額差分</span><span class="sxs-lookup"><span data-stu-id="c6d8d-118">Penny difference in accounting currency</span></span>
-   <span data-ttu-id="c6d8d-119">レポート通貨における小額差分</span><span class="sxs-lookup"><span data-stu-id="c6d8d-119">Penny difference in reporting currency</span></span>
-   <span data-ttu-id="c6d8d-120">期末結果</span><span class="sxs-lookup"><span data-stu-id="c6d8d-120">Year-end result</span></span>

## <a name="posting-rounding-differences-and-sum-recalculations"></a><span data-ttu-id="c6d8d-121">丸め誤差の転記と合計の再計算</span><span class="sxs-lookup"><span data-stu-id="c6d8d-121">Posting rounding differences and sum recalculations</span></span>
<span data-ttu-id="c6d8d-122">次の情報は丸め差額が発生する状況を説明します。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-122">The following information explains where differences in rounding might occur:</span></span>

-   <span data-ttu-id="c6d8d-123">製品価格がゼロに換算された場合、レポートが生成され、製品番号、モジュール タイプ、換算前の価格、および単位を確認できます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-123">If product prices have been converted to 0 (zero), a report is generated that shows the product number, module type, price before the conversion, and unit.</span></span>
-   <span data-ttu-id="c6d8d-124">売上税と一般会計間の丸め誤差が一般仕訳帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-124">Rounding differences between sales tax and the general ledger are posted to the general journal.</span></span>
-   <span data-ttu-id="c6d8d-125">外貨再評価の金額が再計算され、顧客および仕入先トランザクションの金額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-125">Foreign currency revaluation amounts are recalculated, and customer and vendor transaction amounts are recalculated.</span></span>
-   <span data-ttu-id="c6d8d-126">顧客および仕入先決済レコードは、顧客トランザクションおよび仕入先トランザクションごとの丸め誤差で作成されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-126">Customer and vendor settlement records are created for rounding differences for each customer and vendor transaction.</span></span>
-   <span data-ttu-id="c6d8d-127">顧客および仕入先の丸め誤差は一般仕訳帳へ転記されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-127">Rounding differences for customers and vendors are posted to the general journal.</span></span>
-   <span data-ttu-id="c6d8d-128">原価計算済在庫トランザクションの決済原価金額および原価調整金額は再計算されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-128">Settled cost amounts and cost adjustment amounts in closed inventory transactions are recalculated.</span></span>
-   <span data-ttu-id="c6d8d-129">在庫管理の丸め誤差が一般仕訳帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-129">Rounding differences in Inventory management are posted to the general journal.</span></span>
-   <span data-ttu-id="c6d8d-130">手持在庫が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-130">On-hand inventory is recalculated.</span></span>
-   <span data-ttu-id="c6d8d-131">仕訳元帳の合計金額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-131">Total amounts in ledger journals are recalculated.</span></span>
-   <span data-ttu-id="c6d8d-132">元帳の決算シートが再計算されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-132">Ledger closing sheets are recalculated.</span></span>
-   <span data-ttu-id="c6d8d-133">元帳残高が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-133">Ledger balances are recalculated.</span></span>
-   <span data-ttu-id="c6d8d-134">一般会計の丸め誤差が一般仕訳帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-134">Rounding differences in General ledger are posted to the general journal.</span></span>
-   <span data-ttu-id="c6d8d-135">元帳開始トランザクションが再計算されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-135">Opening ledger transactions are recalculated.</span></span>
-   <span data-ttu-id="c6d8d-136">元帳残高の最終金額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-136">The final amount in the ledger balances is calculated.</span></span>

<span data-ttu-id="c6d8d-137">新しい勘定科目通貨に換算し、合計金額の再計算または丸め誤差の転記時にエラーが発生した場合、  **元帳会計通貨の換算**ページを閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-137">If you're converting to a new ledger accounting currency, and an error occurs during the recalculation of total amounts or the posting of rounding differences, you must close the **Ledger accounting currency conversion** page.</span></span> <span data-ttu-id="c6d8d-138">その後、合計金額が再計算され、丸め誤差が転記されます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-138">The total amounts are then recalculated, and the rounding differences are posted.</span></span>

## <a name="processing-the-currency-conversion"></a><span data-ttu-id="c6d8d-139">通貨換算の処理</span><span class="sxs-lookup"><span data-stu-id="c6d8d-139">Processing the currency conversion</span></span>
<span data-ttu-id="c6d8d-140">通貨の換算プロセスを開始するとき、すべてのユーザーはシステムからサイン アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-140">When you start the currency conversion process, all users must be signed out of the system.</span></span> <span data-ttu-id="c6d8d-141">元帳通貨、レポート通貨、為替レートを新規に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-141">You must define the new ledger or reporting currency, and the exchange rates.</span></span> <span data-ttu-id="c6d8d-142">**OK**をクリックすると、プロセスを実行し、システムのすべてのトランザクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-142">When you click **OK**, the process runs and updates every transaction in the system.</span></span> <span data-ttu-id="c6d8d-143">通貨換算は、非常に長いプロセスです。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-143">Currency conversion is a very long process.</span></span> <span data-ttu-id="c6d8d-144">完了すると、**元帳**ページで会計通貨やレポート通貨が更新されたことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-144">When it's completed, you will see that the accounting or reporting currency is updated on the **Ledger** page.</span></span>

## <a name="completing-the-currency-conversion"></a><span data-ttu-id="c6d8d-145">通貨換算の完了</span><span class="sxs-lookup"><span data-stu-id="c6d8d-145">Completing the currency conversion</span></span>
<span data-ttu-id="c6d8d-146">通貨の換算後は、すべての調整レポートを再度生成して、換算済金額がすべて正確であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-146">After the currency conversion, you must generate all reconciliation reports again to make sure that all converted amounts are correct.</span></span>

-   <span data-ttu-id="c6d8d-147">元帳会計通貨の換算により丸め差額が発生した場合、その差額は、丸め差額が発生した伝票を使用しても転記されません。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-147">If the conversion of the ledger accounting currency causes rounding differences, these differences aren't posted by using the voucher where the rounding difference occurred.</span></span> <span data-ttu-id="c6d8d-148">代わりに、換算転記用に入力された伝票を使用して、丸め差額を転記します。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-148">Instead, the differences are posted by using the voucher that was entered for the conversion postings.</span></span> <span data-ttu-id="c6d8d-149">換算後は、伝票と日付で確認が行われるすべてのレポートに、これらの丸め差額が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-149">After the conversion, all reports that check by voucher and date include these rounding differences.</span></span> <span data-ttu-id="c6d8d-150">この動作は正しいので無視してかまいません。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-150">This behavior is correct and can be ignored.</span></span>
-   <span data-ttu-id="c6d8d-151">顧客と仕入先の調整レポートの合計行に表示された金額に差があり、換算前には差額が存在しなかった場合は、この差額を転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-151">If the customer and vendor reconciliation reports display a difference amount on the total line, and no difference amount existed before the conversion, this difference amount must be posted.</span></span> <span data-ttu-id="c6d8d-152">この勘定は顧客および仕入先の集計勘定です。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-152">The account is the summary account for customers and vendors.</span></span> <span data-ttu-id="c6d8d-153">相手勘定は、換算差損または換算利益の勘定科目です。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-153">The offset account is the ledger account for conversion loss or conversion profit.</span></span>

<span data-ttu-id="c6d8d-154">元帳トランザクション仕訳帳がすべて削除されたら、元帳トランザクションを仕訳入力できます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-154">When all ledger transaction journals have been deleted, you can journalize the ledger transactions.</span></span> <span data-ttu-id="c6d8d-155">[**総勘定元帳**] &gt; [**定期処理**] &gt; [**仕訳帳**] &gt; [**仕訳**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-155">Click **General ledger** &gt; **Periodic** &gt; **Journals** &gt; **Journalizing**.</span></span> <span data-ttu-id="c6d8d-156">再評価が必要な場合、通貨換算後に外貨金額を再評価できます。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-156">You can revalue foreign currency amounts after the currency conversion, if revaluation is required.</span></span> <span data-ttu-id="c6d8d-157">外貨金額の再評価は、再評価の**方法**フィールドで**標準**を選択して行います。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-157">You revalue foreign currency amounts by selecting **Standard** in the **Method** field for the revaluation.</span></span>

<span data-ttu-id="c6d8d-158">詳細については、[転記された仕訳入力の仕訳](tasks/journalize-posted-journal-entries.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6d8d-158">For more information, see [Journalize posted journal entries](tasks/journalize-posted-journal-entries.md).</span></span>


