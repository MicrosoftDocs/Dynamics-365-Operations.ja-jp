---
title: "仕入先トランザクション リスト ページ"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations の仕入先トランザクション リスト ページについての情報を提供します。"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 53740f6ed0d463de5ba962f1ba15b208634a0739
ms.contentlocale: ja-jp
ms.lasthandoff: 10/01/2018

---

# <a name="vendor-transactions-list-page"></a><span data-ttu-id="be7a6-103">仕入先トランザクション リスト ページ</span><span class="sxs-lookup"><span data-stu-id="be7a6-103">Vendor transactions list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="be7a6-104">決済を表示する</span><span class="sxs-lookup"><span data-stu-id="be7a6-104">View settlements</span></span>

<span data-ttu-id="be7a6-105">アクション ペインの**決済の表示**ボタンは、決済履歴にすばやくアクセスしたり、決済トランザクション全体についての詳細を説明したりします。</span><span class="sxs-lookup"><span data-stu-id="be7a6-105">The **View settlements** button on the Action Pane provides quick access to the settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="be7a6-106">同じ決済に含まれていたり、または同じ支払仕訳帳で作成された支払である場合、選択したトランザクションに関連する追加トランザクションを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="be7a6-107">**買掛金管理 \> すべての仕入先**を選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-107">Select **Accounts payable \> All vendors**.</span></span>
2. <span data-ttu-id="be7a6-108">トランザクションのある仕入先を選択してから、アクション ウィンドウの、**仕入先**タブで、**トランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-108">Select a vendor that has transactions, and then, on the Action Pane, on the **Vendor** tab, select **Transactions**.</span></span>
3. <span data-ttu-id="be7a6-109">調査を行うにはトランザクションを選択して、アクション ペイン上で**決済を表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-109">Select a transaction to research, and then, on the Action Pane, select **View settlements**.</span></span>

    <span data-ttu-id="be7a6-110">**決済の表示**ダイアログ ボックスが表示され、選択したトランザクションとそれに対して決済されたすべてのドキュメントを表示します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-110">The **View settlements** dialog box appears, and shows the selected transaction and all documents that have been settled against it.</span></span> <span data-ttu-id="be7a6-111">このダイアログ ボックスは、決済履歴の表示と似ていますが、関連するすべてのドキュメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="be7a6-111">This dialog box resembles the settlement history view, but it includes all related documents.</span></span>

4. <span data-ttu-id="be7a6-112">ダイアログ ボックスでは、さまざまなタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-112">In the dialog box, you can perform various tasks.</span></span> <span data-ttu-id="be7a6-113">次の 1 つまたは複数の伝票を選択してから、次のいずれかのボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-113">Select one or more vouchers, and then select one of the following buttons:</span></span>

    - <span data-ttu-id="be7a6-114">**関連項目の表示** – 選択したドキュメントに関連する支払仕訳帳で作成されたすべての支払仕訳帳トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-114">**View related** – Show all the payment journal transactions that were created in the payment journal that is related to the selected document.</span></span> <span data-ttu-id="be7a6-115">さらに、これらの支払に関連するすべての決済が表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-115">In addition, all the settlements that are related to those payments are shown.</span></span> <span data-ttu-id="be7a6-116">関連する支払が表示されているときは、ボタンのラベルで**決済を表示**に変更します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-116">While you're viewing related payments, the label of this button changes to **View settlements**.</span></span> <span data-ttu-id="be7a6-117">**決済の表示**を選択して、**決済の表示**ダイアログ ボックスを最初に開いたときに表示されるトランザクションのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-117">Select **View settlements** to show only the transactions that were shown when you first opened the **View settlements** dialog box.</span></span>
    - <span data-ttu-id="be7a6-118">**履歴の表示** – 伝票の決済履歴を表示します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-118">**View history** – Show the settlement history for the vouchers.</span></span> <span data-ttu-id="be7a6-119">**閉じる**を選択して、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-119">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="be7a6-120">**会計の表示** – 選択した伝票に関連するすべての伝票を表示します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-120">**View accounting** – Show all vouchers that are related to the selected documents.</span></span> <span data-ttu-id="be7a6-121">**閉じる**を選択して、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-121">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="be7a6-122">**エクスポート**: 選択した伝票を Microsoft Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="be7a6-122">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
    - <span data-ttu-id="be7a6-123">**トランザクションの決済** – 選択した元のドキュメントが完全に決済されなかった場合のみ、このボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-123">**Settle transactions** – This button appears only if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="be7a6-124">このボタンを選択すると、**トランザクションの決済**ダイアログ ボックスが表示され、決済するトランザクションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-124">When you select this button, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="be7a6-125">**決済を元に戻す** – 選択した元のドキュメントが完全に決済された場合のみ、このボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-125">**Undo settlements** – This button appears only if the original document that was selected was fully settled.</span></span> <span data-ttu-id="be7a6-126">このボタンを選択すると、**決済を元に戻す**ダイアログ ボックスが表示され、そのドキュメントで実行された決済を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-126">When you select this button, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>

## <a name="global-transactions"></a><span data-ttu-id="be7a6-127">グローバル トランザクション</span><span class="sxs-lookup"><span data-stu-id="be7a6-127">Global transactions</span></span>

<span data-ttu-id="be7a6-128">**グローバル トランザクション**ボタンが仕入先に追加されました。</span><span class="sxs-lookup"><span data-stu-id="be7a6-128">The **Global transactions** button has been added to the vendor.</span></span> <span data-ttu-id="be7a6-129">このボタンを使用して、すべての法人間で仕入先のすべてのトランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-129">This button lets you view all transactions for a vendor across all legal entities.</span></span> <span data-ttu-id="be7a6-130">**仕入先トランザクション**リスト ページでは、ユーザーのセキュリティ設定に基づいて、ユーザーがアクセスする法人に対してのみトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-130">The **Vendor transactions** list page shows transactions only for the legal entities that the user has access to, based on his or her security settings.</span></span>

<span data-ttu-id="be7a6-131">リスト ページでは、開始した仕入先として同じ関係者 ID を持つ仕入先に対するすべてのトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-131">The list page will show all transactions for vendors that have the same party ID as the vendor that you started with.</span></span> <span data-ttu-id="be7a6-132">たとえば、1 つの法人の仕入先 US-001 に別の法人の仕入先 DE-001と同じ関係者 ID がある場合、両方の仕入先 ID のすべてのトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-132">For example, if vendor US-001 in one legal entity has the same party ID as vendor DE-001 in another legal entity, all transactions for both vendor IDs are shown.</span></span>

<span data-ttu-id="be7a6-133">**仕入先トランザクション**リスト ページのメニューは、トランザクションの法人によって異なります。</span><span class="sxs-lookup"><span data-stu-id="be7a6-133">The menus on the **Vendor transactions** list page vary, depending on the legal entity for the transaction.</span></span> <span data-ttu-id="be7a6-134">たとえば、機能がスイスの法人のためのみに利用可能な場合、その機能のメニュー オプションはスイスのトランザクションが選択されているときのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-134">For example, if a feature is available only for Swiss legal entities, the menu options for that feature appear only when a Swiss transaction is selected.</span></span>

<span data-ttu-id="be7a6-135">機能にアクセスするには、以下の手順を行います。</span><span class="sxs-lookup"><span data-stu-id="be7a6-135">To access the feature, follow these steps.</span></span>

1. <span data-ttu-id="be7a6-136">**買掛金管理** \> **すべての仕入先**を選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-136">Select **Accounts payable** \> **All vendors**.</span></span>
2. <span data-ttu-id="be7a6-137">仕入先を選択してから、アクション ウィンドウの、**仕入先**タブの、**トランザクション**グループで、**グローバル トランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-137">Select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Global transactions**.</span></span>

## <a name="more-transaction-filters"></a><span data-ttu-id="be7a6-138">詳細トランザクション フィルター</span><span class="sxs-lookup"><span data-stu-id="be7a6-138">More transaction filters</span></span>

<span data-ttu-id="be7a6-139">オープン トランザクションを表示するフィルターは、より多くのトランザクションの組み合わせを見ることができる新しいフィルターで置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="be7a6-139">The filter for showing open transactions has been replaced with a new filter that lets you view more combinations of transactions.</span></span> <span data-ttu-id="be7a6-140">**表示**フィールドで次のオプションが利用できます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-140">The following options are available in the **Show** field:</span></span>

- <span data-ttu-id="be7a6-141">**すべて** – 選択した仕入先 (未処理および決算済) のすべてのトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-141">**All** – Show all transactions for the selected vendors (open and closed).</span></span>
- <span data-ttu-id="be7a6-142">**決済済** - 完全に決済および決済されたトランザクションのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-142">**Closed** – Show only transactions that have been fully settled and closed.</span></span>
- <span data-ttu-id="be7a6-143">**未処理** - 完全に決済されていないトランザクションのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-143">**Open** – Show only transactions that haven't been fully settled.</span></span>
- <span data-ttu-id="be7a6-144">**現時点での未処理** - 指定した日付の時点で完全に決済されていないトランザクションのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-144">**Open as of date** – Show only transactions that haven't been fully settled as of a date that you specify.</span></span> <span data-ttu-id="be7a6-145">このオプションを選択するときに、フィルターの隣に表示される日付を変更できます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-145">When you select this option, you can change the date that is shown next to the filter.</span></span> <span data-ttu-id="be7a6-146">トランザクションが現在の日付の時点で完全に決済されても、指定する日付の後に**前回決済日時**値を持つトランザクションはリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-146">Transactions that have a **Last settlement date** value after the date that you specify are shown in the list, even if those transactions are fully settled as of the current date.</span></span> <span data-ttu-id="be7a6-147">ただし残高は、選択された日付ではなく、現在の日付の時点で表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-147">However, the balance represents the balances as of the current date, not as of the selected date.</span></span>

<span data-ttu-id="be7a6-148">通貨換算のトランザクションを非表示にすることができるフィルターが追加れました。</span><span class="sxs-lookup"><span data-stu-id="be7a6-148">A filter has also been added that lets you hide currency translation transactions.</span></span> <span data-ttu-id="be7a6-149">**通貨の再評価を非表示にする**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-149">Just select the **Hide currency revaluations** check box.</span></span>

## <a name="more-easily-modify-due-dates-and-discount-dates"></a><span data-ttu-id="be7a6-150">期日および割引の日付をより簡単に変更</span><span class="sxs-lookup"><span data-stu-id="be7a6-150">More easily modify due dates and discount dates</span></span>

<span data-ttu-id="be7a6-151">未処理の顧客トランザクションのために、期日および割引の日付を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-151">You can update due dates and discount dates for open customer transactions.</span></span> <span data-ttu-id="be7a6-152">8.1 リリースで、エクスペリエンスが強化されました。</span><span class="sxs-lookup"><span data-stu-id="be7a6-152">In release 8.1, the experience has been improved.</span></span> <span data-ttu-id="be7a6-153">**仕入先トランザクション**リスト ページに期日を追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="be7a6-153">You can now add due dates to the **Vendor transactions** list page.</span></span> <span data-ttu-id="be7a6-154">**仕入先トランザクション**リスト ページで期日をクリックして、**期日および現金割引日を更新する**ダイアログ ボックスで期日、割引日、支払条件、および現金割引条件を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-154">By clicking on the due date in the **Vendor transactions** list page, you can also change due dates, discount dates, payment terms, and cash discount terms in the **Update due date and cash discount dates**  dialog box.</span></span>

### <a name="activate-the-feature"></a><span data-ttu-id="be7a6-155">機能の有効化</span><span class="sxs-lookup"><span data-stu-id="be7a6-155">Activate the feature</span></span>

<span data-ttu-id="be7a6-156">**期日および現金割引日を更新する**ダイアログ ボックスを使用して、**仕入先トランザクション**リスト ページに期日を追加し、トランザクションの支払設定を変更するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="be7a6-156">To add due dates to the **Vendor transactions** list page and change payment settings for a transaction by using the **Update due date and cash discount dates** dialog box, follow these steps.</span></span>

1. <span data-ttu-id="be7a6-157">**買掛金勘定 \> 設定 \> 買掛金勘定パラメーター**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-157">Select **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="be7a6-158">**決済**タブで、**期日を表示し編集を許可する**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-158">On the **Settlements** tab, Set the **Show due date and allow edit** option to **Yes**.</span></span>
3. <span data-ttu-id="be7a6-159">この機能を有効にするため、新しいフィールドが仕入先トランザクションに追加されました。</span><span class="sxs-lookup"><span data-stu-id="be7a6-159">To enable this feature, new fields have been added to vendor transactions.</span></span> <span data-ttu-id="be7a6-160">これらのフィールドは、新しいトランザクションが完了したときに入力されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-160">Those fields will be filled in when a new transaction is completed.</span></span> <span data-ttu-id="be7a6-161">**期日および現金割引の日付を更新**ダイアログ ボックスを開くときに入力されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-161">They will also be filled in when you open the **Update due date and cash discount dates** dialog box.</span></span> <span data-ttu-id="be7a6-162">**期日を表示し編集を許可**オプションを**はい**に設定するときに、**支払情報を更新**ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-162">When you set the **Show due date and allow edit** option to **Yes**, you will see the **Update payment information** dialog box.</span></span>  <span data-ttu-id="be7a6-163">直ちに既存のトランザクションを更新するには、**すべての既存のトランザクションを更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-163">To update existing transactions immediately, select **Update all existing transactions**.</span></span> <span data-ttu-id="be7a6-164">あるいは、新しいトランザクションに対してのみのフィールドに入力するには、**更新なしで続行する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-164">Alternatively, to fill in the fields only for new transactions, select **Continue without update**.</span></span>

<span data-ttu-id="be7a6-165">**仕入先トランザクション**リスト ページに期日を追加できるようになり、トランザクションの期日および現金割引日をより簡単に変更できます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-165">The due date is now added to the **Vendor transactions** list page, and you can more easily modify the due date and cash discount dates for transactions.</span></span>

### <a name="modify-the-payment-settings"></a><span data-ttu-id="be7a6-166">支払設定を変更</span><span class="sxs-lookup"><span data-stu-id="be7a6-166">Modify the payment settings</span></span>

<span data-ttu-id="be7a6-167">**仕入先トランザクション**リスト ページでは、仕入先のすべてのトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-167">The **Vendor transactions** list page shows all transactions for a vendor.</span></span> <span data-ttu-id="be7a6-168">トランザクションの期日を選択すると、ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-168">When you select the due date for a transaction, a dialog box appears.</span></span> <span data-ttu-id="be7a6-169">このダイアログ ボックスでは、期日および割引の計算の基準日、期日、支払条件、現金割引の条件および現金割引の日付の基準日が表示されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-169">This dialog box shows the base date for due date and discount calculations, the due date, the payment terms, the cash discount terms, and the cash discount dates.</span></span>

<span data-ttu-id="be7a6-170">各フィールドは編集時、トランザクションに異なる効果をもたらします。</span><span class="sxs-lookup"><span data-stu-id="be7a6-170">Each field has a different effect on the transaction when you edit it:</span></span>

- <span data-ttu-id="be7a6-171">**基準日の編集:** 期日および割引日は、基準日が文書日付であるかのように変更されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-171">**Edit the base date:** The due date and discount dates are changed as if the base date is the document date.</span></span>
- <span data-ttu-id="be7a6-172">**期日の編集:** 期日のみが変更されます</span><span class="sxs-lookup"><span data-stu-id="be7a6-172">**Edit the due date:** Only the due date is changed</span></span>
- <span data-ttu-id="be7a6-173">**割引日を編集:** 割引日のみが変更されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-173">**Edit the discount dates:** Only the discount dates are changed.</span></span>
- <span data-ttu-id="be7a6-174">**支払条件を編集:** 基準日および支払条件に基づき、期日は変更されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-174">**Edit the payment terms:** The due date is changed, based on the base date and the payment terms.</span></span>
- <span data-ttu-id="be7a6-175">**現金割引の条件を編集:** 基準日と現金割引条件に基づき、現金割引は変更されます。</span><span class="sxs-lookup"><span data-stu-id="be7a6-175">**Edit the cash discount terms:** The cash discounts are changed, based on the base date and the cash discount terms.</span></span>

<span data-ttu-id="be7a6-176">支払設定の編集を終えたら、**閉じる**を選び変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="be7a6-176">When you've finished editing the payment settings, select **Close** to save your changes.</span></span>

