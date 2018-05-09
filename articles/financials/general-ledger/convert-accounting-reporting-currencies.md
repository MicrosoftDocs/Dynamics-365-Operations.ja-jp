---
title: "会計またはレポートの通貨換算"
description: "会計通貨やレポート通貨を変更する必要のある会社には、2 つの選択肢があります。"
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f05020dfde0b985faf3a6b9dc72f94a6d87e7968
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="convert-accounting-or-reporting-currencies"></a><span data-ttu-id="7ae44-103">会計またはレポートの通貨換算</span><span class="sxs-lookup"><span data-stu-id="7ae44-103">Convert accounting or reporting currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ae44-104">会計通貨やレポート通貨を変更する必要のある会社には、2 つの選択肢があります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-104">A company that must change its accounting currency or reporting currency has two options.</span></span> <span data-ttu-id="7ae44-105">1 つ目の選択肢は、新しい会社を作成して新規に開始することです。</span><span class="sxs-lookup"><span data-stu-id="7ae44-105">The first option is to create a new company and start fresh.</span></span> <span data-ttu-id="7ae44-106">2 番目の選択肢は、会計通貨とレポート通貨の換算プロセスを実行することです。</span><span class="sxs-lookup"><span data-stu-id="7ae44-106">The second option is to run the accounting and reporting currency conversion process.</span></span> <span data-ttu-id="7ae44-107">これは、システムのすべてのトランザクションを変更する、長い実行時間のプロセスです。</span><span class="sxs-lookup"><span data-stu-id="7ae44-107">This is a very long-running process that changes every transaction in the system.</span></span> <span data-ttu-id="7ae44-108">また、プロセスを実行する前に、設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="7ae44-108">Some setup is also required before the process can be run.</span></span>

## <a name="preparing-the-legal-entity-for-currency-conversion"></a><span data-ttu-id="7ae44-109">通貨の換算用の法人の準備</span><span class="sxs-lookup"><span data-stu-id="7ae44-109">Preparing the legal entity for currency conversion</span></span>
<span data-ttu-id="7ae44-110">その法人の通貨を換算できるようにするには、顧客および仕入先勘定の外貨再評価金額を元に戻し、前会計年度を閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-110">Before you can convert the legal entity’s currency, you must revert any foreign currency revaluation amounts for customer and vendor accounts, and close the previous fiscal years.</span></span> <span data-ttu-id="7ae44-111">また、変換用のデータベースを準備し、それから通貨換算を実行中の法人の口座に必要な変更を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-111">You must also prepare the database for the conversion, and then make the required changes to the legal entity’s account that is undergoing the currency conversion.</span></span> <span data-ttu-id="7ae44-112">通貨の換算を完了したら、実行の必要な追加手順がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-112">After you have completed a currency conversion, you must complete some additional procedures.</span></span> <span data-ttu-id="7ae44-113">実行する必要がありるのは、換算した金額の丸め差額の調整、業務統計の再計算、元帳トランザクションの仕訳入力、換算ツールへのアクセスの制限、顧客勘定および仕入先勘定の外貨金額の再評価です。</span><span class="sxs-lookup"><span data-stu-id="7ae44-113">You must reconcile rounding differences in converted amounts, recalculate business statistics, journalize the ledger transactions, limit access to the conversion tool, and revalue foreign currency amounts for customer and vendor accounts.</span></span>

## <a name="setting-up-accounts-for-automatic-transactions"></a><span data-ttu-id="7ae44-114">自動トランザクションの勘定の設定</span><span class="sxs-lookup"><span data-stu-id="7ae44-114">Setting up accounts for automatic transactions</span></span>
<span data-ttu-id="7ae44-115">通貨の換算プロセスの間に、その差益または差損、または小額差分は、**自動トランザクションの勘定**ページで定義された勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-115">During the currency conversion process, gains or losses, or penny differences, are posted to the accounts that are defined on the **Accounts for automatic transactions** page.</span></span> <span data-ttu-id="7ae44-116">主勘定は、換算プロセスを実行する前に、次のタイプのトランザクションに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-116">Main accounts must be assigned to the following types of transaction before the conversion process is run:</span></span>

-   <span data-ttu-id="7ae44-117">会計通貨換算差益</span><span class="sxs-lookup"><span data-stu-id="7ae44-117">Accounting currency conversion gain</span></span>
-   <span data-ttu-id="7ae44-118">会計通貨換算差損</span><span class="sxs-lookup"><span data-stu-id="7ae44-118">Accounting currency conversion loss</span></span>
-   <span data-ttu-id="7ae44-119">会計通貨での小額差分</span><span class="sxs-lookup"><span data-stu-id="7ae44-119">Penny difference in accounting currency</span></span>
-   <span data-ttu-id="7ae44-120">レポート通貨における小額差分</span><span class="sxs-lookup"><span data-stu-id="7ae44-120">Penny difference in reporting currency</span></span>
-   <span data-ttu-id="7ae44-121">期末結果</span><span class="sxs-lookup"><span data-stu-id="7ae44-121">Year-end result</span></span>

## <a name="posting-rounding-differences-and-sum-recalculations"></a><span data-ttu-id="7ae44-122">丸め誤差の転記と合計の再計算</span><span class="sxs-lookup"><span data-stu-id="7ae44-122">Posting rounding differences and sum recalculations</span></span>
<span data-ttu-id="7ae44-123">次の情報は丸め差額が発生する状況を説明します。</span><span class="sxs-lookup"><span data-stu-id="7ae44-123">The following information explains where differences in rounding might occur:</span></span>

-   <span data-ttu-id="7ae44-124">製品価格がゼロに換算された場合、レポートが生成され、製品番号、モジュール タイプ、換算前の価格、および単位を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-124">If product prices have been converted to 0 (zero), a report is generated that shows the product number, module type, price before the conversion, and unit.</span></span>
-   <span data-ttu-id="7ae44-125">売上税と一般会計間の丸め誤差が一般仕訳帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-125">Rounding differences between sales tax and the general ledger are posted to the general journal.</span></span>
-   <span data-ttu-id="7ae44-126">外貨再評価の金額が再計算され、顧客および仕入先トランザクションの金額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-126">Foreign currency revaluation amounts are recalculated, and customer and vendor transaction amounts are recalculated.</span></span>
-   <span data-ttu-id="7ae44-127">顧客および仕入先決済レコードは、顧客トランザクションおよび仕入先トランザクションごとの丸め誤差で作成されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-127">Customer and vendor settlement records are created for rounding differences for each customer and vendor transaction.</span></span>
-   <span data-ttu-id="7ae44-128">顧客および仕入先の丸め誤差は一般仕訳帳へ転記されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-128">Rounding differences for customers and vendors are posted to the general journal.</span></span>
-   <span data-ttu-id="7ae44-129">原価計算済在庫トランザクションの決済原価金額および原価調整金額は再計算されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-129">Settled cost amounts and cost adjustment amounts in closed inventory transactions are recalculated.</span></span>
-   <span data-ttu-id="7ae44-130">在庫管理の丸め誤差が一般仕訳帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-130">Rounding differences in Inventory management are posted to the general journal.</span></span>
-   <span data-ttu-id="7ae44-131">手持在庫が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-131">On-hand inventory is recalculated.</span></span>
-   <span data-ttu-id="7ae44-132">仕訳元帳の合計金額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-132">Total amounts in ledger journals are recalculated.</span></span>
-   <span data-ttu-id="7ae44-133">元帳の決算シートが再計算されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-133">Ledger closing sheets are recalculated.</span></span>
-   <span data-ttu-id="7ae44-134">元帳残高が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-134">Ledger balances are recalculated.</span></span>
-   <span data-ttu-id="7ae44-135">一般会計の丸め誤差が一般仕訳帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-135">Rounding differences in General ledger are posted to the general journal.</span></span>
-   <span data-ttu-id="7ae44-136">元帳開始トランザクションが再計算されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-136">Opening ledger transactions are recalculated.</span></span>
-   <span data-ttu-id="7ae44-137">元帳残高の最終金額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-137">The final amount in the ledger balances is calculated.</span></span>

<span data-ttu-id="7ae44-138">新しい勘定科目通貨に換算し、合計金額の再計算または丸め誤差の転記時にエラーが発生した場合、  **元帳会計通貨の換算**ページを閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-138">If you're converting to a new ledger accounting currency, and an error occurs during the recalculation of total amounts or the posting of rounding differences, you must close the **Ledger accounting currency conversion** page.</span></span> <span data-ttu-id="7ae44-139">その後、合計金額が再計算され、丸め誤差が転記されます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-139">The total amounts are then recalculated, and the rounding differences are posted.</span></span>

## <a name="processing-the-currency-conversion"></a><span data-ttu-id="7ae44-140">通貨換算の処理</span><span class="sxs-lookup"><span data-stu-id="7ae44-140">Processing the currency conversion</span></span>
<span data-ttu-id="7ae44-141">通貨の換算プロセスを開始するとき、すべてのユーザーはシステムからサイン アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-141">When you start the currency conversion process, all users must be signed out of the system.</span></span> <span data-ttu-id="7ae44-142">元帳通貨、レポート通貨、為替レートを新規に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-142">You must define the new ledger or reporting currency, and the exchange rates.</span></span> <span data-ttu-id="7ae44-143">**OK**をクリックすると、プロセスを実行し、システムのすべてのトランザクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="7ae44-143">When you click **OK**, the process runs and updates every transaction in the system.</span></span> <span data-ttu-id="7ae44-144">通貨換算は、非常に長いプロセスです。</span><span class="sxs-lookup"><span data-stu-id="7ae44-144">Currency conversion is a very long process.</span></span> <span data-ttu-id="7ae44-145">完了すると、**元帳**ページで会計通貨やレポート通貨が更新されたことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-145">When it's completed, you will see that the accounting or reporting currency is updated on the **Ledger** page.</span></span>

## <a name="completing-the-currency-conversion"></a><span data-ttu-id="7ae44-146">通貨換算の完了</span><span class="sxs-lookup"><span data-stu-id="7ae44-146">Completing the currency conversion</span></span>
<span data-ttu-id="7ae44-147">通貨の換算後は、すべての調整レポートを再度生成して、換算済金額がすべて正確であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-147">After the currency conversion, you must generate all reconciliation reports again to make sure that all converted amounts are correct.</span></span>

-   <span data-ttu-id="7ae44-148">元帳会計通貨の換算により丸め差額が発生した場合、その差額は、丸め差額が発生した伝票を使用しても転記されません。</span><span class="sxs-lookup"><span data-stu-id="7ae44-148">If the conversion of the ledger accounting currency causes rounding differences, these differences aren't posted by using the voucher where the rounding difference occurred.</span></span> <span data-ttu-id="7ae44-149">代わりに、換算転記用に入力された伝票を使用して、丸め差額を転記します。</span><span class="sxs-lookup"><span data-stu-id="7ae44-149">Instead, the differences are posted by using the voucher that was entered for the conversion postings.</span></span> <span data-ttu-id="7ae44-150">換算後は、伝票と日付で確認が行われるすべてのレポートに、これらの丸め差額が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-150">After the conversion, all reports that check by voucher and date include these rounding differences.</span></span> <span data-ttu-id="7ae44-151">この動作は正しいので無視してかまいません。</span><span class="sxs-lookup"><span data-stu-id="7ae44-151">This behavior is correct and can be ignored.</span></span>
-   <span data-ttu-id="7ae44-152">顧客と仕入先の調整レポートの合計行に表示された金額に差があり、換算前には差額が存在しなかった場合は、この差額を転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ae44-152">If the customer and vendor reconciliation reports display a difference amount on the total line, and no difference amount existed before the conversion, this difference amount must be posted.</span></span> <span data-ttu-id="7ae44-153">この勘定は顧客および仕入先の集計勘定です。</span><span class="sxs-lookup"><span data-stu-id="7ae44-153">The account is the summary account for customers and vendors.</span></span> <span data-ttu-id="7ae44-154">相手勘定は、換算差損または換算利益の勘定科目です。</span><span class="sxs-lookup"><span data-stu-id="7ae44-154">The offset account is the ledger account for conversion loss or conversion profit.</span></span>

<span data-ttu-id="7ae44-155">元帳トランザクション仕訳帳がすべて削除されたら、元帳トランザクションを仕訳入力できます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-155">When all ledger transaction journals have been deleted, you can journalize the ledger transactions.</span></span> <span data-ttu-id="7ae44-156">[総勘定元帳] &gt; [定期処理] &gt; [仕訳帳] &gt; [仕訳] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7ae44-156">Click **General ledger** &gt; **Periodic** &gt; **Journals** &gt; **Journalizing**.</span></span> <span data-ttu-id="7ae44-157">再評価が必要な場合、通貨換算後に外貨金額を再評価できます。</span><span class="sxs-lookup"><span data-stu-id="7ae44-157">You can revalue foreign currency amounts after the currency conversion, if revaluation is required.</span></span> <span data-ttu-id="7ae44-158">外貨金額の再評価は、再評価の**方法**フィールドで**標準**を選択して行います。</span><span class="sxs-lookup"><span data-stu-id="7ae44-158">You revalue foreign currency amounts by selecting **Standard** in the **Method** field for the revaluation.</span></span>

<span data-ttu-id="7ae44-159">詳細については、[転記された仕訳入力の仕訳](tasks/journalize-posted-journal-entries.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ae44-159">For more information, see [Journalize posted journal entries](tasks/journalize-posted-journal-entries.md).</span></span>


