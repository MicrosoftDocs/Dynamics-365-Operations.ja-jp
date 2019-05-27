---
title: 仕入先トランザクション リスト ページ
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の仕入先トランザクション リスト ページについての情報を提供します。
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 99a169bd51e14f15c085f7547ec240b2787258cc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564765"
---
# <a name="vendor-transactions-list-page"></a><span data-ttu-id="426e2-103">仕入先トランザクション リスト ページ</span><span class="sxs-lookup"><span data-stu-id="426e2-103">Vendor transactions list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="426e2-104">決済を表示する</span><span class="sxs-lookup"><span data-stu-id="426e2-104">View settlements</span></span>

<span data-ttu-id="426e2-105">アクション ペインの**決済の表示**ボタンは、決済履歴にすばやくアクセスしたり、決済トランザクションの詳細情報について説明したりします。</span><span class="sxs-lookup"><span data-stu-id="426e2-105">The **View settlements** button on the Action Pane provides quick access to the settlement history and detailed information about the settlement transaction.</span></span> <span data-ttu-id="426e2-106">同じ決済に含まれていたり、または同じ支払仕訳帳で作成された支払である場合、選択したトランザクションに関連する追加トランザクションを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="426e2-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="426e2-107">**買掛金管理 \> すべての仕入先**を選択します。</span><span class="sxs-lookup"><span data-stu-id="426e2-107">Select **Accounts payable \> All vendors**.</span></span>
2. <span data-ttu-id="426e2-108">トランザクションのある仕入先を選択してから、アクション ウィンドウの、**仕入先**タブで、**トランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="426e2-108">Select a vendor that has transactions, and then, on the Action Pane, on the **Vendor** tab, select **Transactions**.</span></span>
3. <span data-ttu-id="426e2-109">調査を行うにはトランザクションを選択して、アクション ペイン上で**決済を表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="426e2-109">Select a transaction to research, and then, on the Action Pane, select **View settlements**.</span></span>

    <span data-ttu-id="426e2-110">**決済の表示**ダイアログ ボックスが表示され、選択したトランザクションとそれに対して決済されたすべてのドキュメントを表示します。</span><span class="sxs-lookup"><span data-stu-id="426e2-110">The **View settlements** dialog box appears, and shows the selected transaction and all documents that have been settled against it.</span></span> <span data-ttu-id="426e2-111">このダイアログ ボックスは、決済履歴の表示と似ていますが、関連するすべてのドキュメントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="426e2-111">This dialog box resembles the settlement history view, but it includes all related documents.</span></span>

4. <span data-ttu-id="426e2-112">ダイアログ ボックスでは、さまざまなタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="426e2-112">In the dialog box, you can perform various tasks.</span></span> <span data-ttu-id="426e2-113">次の 1 つまたは複数の伝票を選択してから、次のいずれかのボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="426e2-113">Select one or more vouchers, and then select one of the following buttons:</span></span>

    - <span data-ttu-id="426e2-114">**関連項目を表示する** – 一覧に表示されているドキュメントが作成された仕訳帳で作成された仕入先の、すべての支払仕訳帳トランザクションと一般仕訳帳トランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="426e2-114">**View related** – Show all the payment journal transactions and general journal tranactions for the vendor that were created in the journals in which the documents shown in the list were created.</span></span> <span data-ttu-id="426e2-115">たとえば、支払が表示されている場合は、その支払が作成された支払仕訳帳のすべての支払が表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-115">For example, if a payment is shown, then all of the payments in the payment journal in which it was created will be shown.</span></span> <span data-ttu-id="426e2-116">請求書または支払が表示されていて、それが一般仕訳帳で作成された場合は、それが作成された一般仕訳帳のすべてのドキュメントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-116">If an invoice or payment is shown and it was created in a general journal, then all of the documents in the general journal in which it was created will be shown.</span></span> <span data-ttu-id="426e2-117">ドキュメントのリストに関連するすべての決済も表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-117">All the settlements that are related to list of documents are also shown.</span></span> <span data-ttu-id="426e2-118">関連する支払が表示されているときは、ボタンのラベルで**決済を表示**に変更します。</span><span class="sxs-lookup"><span data-stu-id="426e2-118">While you're viewing related payments, the label of this button changes to **View settlements**.</span></span> <span data-ttu-id="426e2-119">**決済の表示**を選択して、**決済の表示**ダイアログ ボックスを最初に開いたときに表示されるトランザクションのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="426e2-119">Select **View settlements** to show only the transactions that were shown when you first opened the **View settlements** dialog box.</span></span>
    - <span data-ttu-id="426e2-120">**履歴の表示** – 伝票の決済履歴を表示します。</span><span class="sxs-lookup"><span data-stu-id="426e2-120">**View history** – Show the settlement history for the vouchers.</span></span> <span data-ttu-id="426e2-121">**閉じる**を選択して、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="426e2-121">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="426e2-122">**会計の表示** – 選択した伝票に関連するすべての伝票を表示します。</span><span class="sxs-lookup"><span data-stu-id="426e2-122">**View accounting** – Show all vouchers that are related to the selected documents.</span></span> <span data-ttu-id="426e2-123">**閉じる**を選択して、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="426e2-123">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="426e2-124">**エクスポート** – 選択した伝票を Microsoft Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="426e2-124">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
    - <span data-ttu-id="426e2-125">**トランザクションの決済** – 選択した元のドキュメントが完全に決済されなかった場合のみ、このボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-125">**Settle transactions** – This button appears only if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="426e2-126">このボタンを選択すると、**トランザクションの決済**ダイアログ ボックスが表示され、決済するトランザクションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="426e2-126">When you select this button, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="426e2-127">**決済を元に戻す** – 選択した元のドキュメントが完全に決済された場合のみ、このボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-127">**Undo settlements** – This button appears only if the original document that was selected was fully settled.</span></span> <span data-ttu-id="426e2-128">このボタンを選択すると、**決済を元に戻す**ダイアログ ボックスが表示され、そのドキュメントで実行された決済を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="426e2-128">When you select this button, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>

## <a name="global-transactions"></a><span data-ttu-id="426e2-129">グローバル トランザクション</span><span class="sxs-lookup"><span data-stu-id="426e2-129">Global transactions</span></span>

<span data-ttu-id="426e2-130">**グローバル トランザクション** ボタンは**仕入先トランザクション** リスト ページでも表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-130">The **Global transactions** button also displays on the **Vendor transactions** list page.</span></span> <span data-ttu-id="426e2-131">このボタンを使用して、すべての法人間で仕入先のすべてのトランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="426e2-131">This button lets you view all transactions for a vendor across all legal entities.</span></span> <span data-ttu-id="426e2-132">**仕入先トランザクション**リスト ページでは、ユーザーのセキュリティ設定に基づいて、ユーザーがアクセスする法人に対してのみトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-132">The **Vendor transactions** list page shows transactions only for the legal entities that the user has access to, based on his or her security settings.</span></span>

<span data-ttu-id="426e2-133">リスト ページでは、開始した仕入先として同じ関係者 ID を持つ仕入先に対するすべてのトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-133">The list page will show all transactions for vendors that have the same party ID as the vendor that you started with.</span></span> <span data-ttu-id="426e2-134">たとえば、1 つの法人の仕入先 US-001 に別の法人の仕入先 DE-001と同じ関係者 ID がある場合、両方の仕入先 ID のすべてのトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-134">For example, if vendor US-001 in one legal entity has the same party ID as vendor DE-001 in another legal entity, all transactions for both vendor IDs are shown.</span></span>

<span data-ttu-id="426e2-135">**仕入先トランザクション**リスト ページのメニューは、トランザクションの法人によって異なります。</span><span class="sxs-lookup"><span data-stu-id="426e2-135">The menus on the **Vendor transactions** list page vary, depending on the legal entity for the transaction.</span></span> <span data-ttu-id="426e2-136">たとえば、機能がスイスの法人のためのみに利用可能な場合、その機能のメニュー オプションはスイスのトランザクションが選択されているときのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-136">For example, if a feature is available only for Swiss legal entities, the menu options for that feature appear only when a Swiss transaction is selected.</span></span>

<span data-ttu-id="426e2-137">機能にアクセスするには、以下の手順を行います。</span><span class="sxs-lookup"><span data-stu-id="426e2-137">To access the feature, follow these steps.</span></span>

1. <span data-ttu-id="426e2-138">**買掛金管理** \> **すべての仕入先**を選択します。</span><span class="sxs-lookup"><span data-stu-id="426e2-138">Select **Accounts payable** \> **All vendors**.</span></span>
2. <span data-ttu-id="426e2-139">仕入先を選択してから、アクション ウィンドウの、**仕入先**タブの、**トランザクション**グループで、**グローバル トランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="426e2-139">Select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Global transactions**.</span></span>

## <a name="more-transaction-filters"></a><span data-ttu-id="426e2-140">詳細トランザクション フィルター</span><span class="sxs-lookup"><span data-stu-id="426e2-140">More transaction filters</span></span>

<span data-ttu-id="426e2-141">オープン トランザクションを表示するフィルターは、より多くのトランザクションの組み合わせを見ることができる新しいフィルターで置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="426e2-141">The filter for showing open transactions has been replaced with a new filter that lets you view more combinations of transactions.</span></span> <span data-ttu-id="426e2-142">**表示**フィールドで次のオプションが利用できます。</span><span class="sxs-lookup"><span data-stu-id="426e2-142">The following options are available in the **Show** field:</span></span>

- <span data-ttu-id="426e2-143">**すべて** – 選択した仕入先 (未処理および決算済) のすべてのトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="426e2-143">**All** – Show all transactions for the selected vendors (open and closed).</span></span>
- <span data-ttu-id="426e2-144">**決済済** - 完全に決済および決済されたトランザクションのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="426e2-144">**Closed** – Show only transactions that have been fully settled and closed.</span></span>
- <span data-ttu-id="426e2-145">**未処理** - 完全に決済されていないトランザクションのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="426e2-145">**Open** – Show only transactions that haven't been fully settled.</span></span>
- <span data-ttu-id="426e2-146">**未処理のトランザクション (指定日以降に決算されたトランザクションを含む)** – 指定した日付以降に完全に決済されていないトランザクションのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="426e2-146">**Open including closed on or after date** – Show only transactions that haven't been fully settled on or after a date that you specify.</span></span> <span data-ttu-id="426e2-147">このオプションを選択するときに、フィルターの隣に表示される日付を変更できます。</span><span class="sxs-lookup"><span data-stu-id="426e2-147">When you select this option, you can change the date that is shown next to the filter.</span></span> <span data-ttu-id="426e2-148">トランザクションが現在の日付の時点で完全に決済されても、指定する日付以降に**前回決済日時**値を持つトランザクションはリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-148">Transactions that have a **Last settlement date** value on or after the date that you specify are shown in the list, even if those transactions are fully settled as of the current date.</span></span> <span data-ttu-id="426e2-149">ただし残高は、選択された日付ではなく、現在の日付の時点で表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-149">However, the balance represents the balances as of the current date, not as of the selected date.</span></span>

<span data-ttu-id="426e2-150">**通貨の再評価を非表示にする**チェック ボックスを選択して、通貨換算のトランザクションを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="426e2-150">Select the **Hide currency revaluations** check box to hide currency translation transactions.</span></span>

## <a name="modify-due-dates-and-discount-dates"></a><span data-ttu-id="426e2-151">期日および割引の日付を変更</span><span class="sxs-lookup"><span data-stu-id="426e2-151">Modify due dates and discount dates</span></span>

<span data-ttu-id="426e2-152">未処理の顧客トランザクションのために、期日および割引の日付を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="426e2-152">You can update due dates and discount dates for open customer transactions.</span></span> <span data-ttu-id="426e2-153">8.1 リリースで、**仕入先トランザクション** リスト ページに期日を追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="426e2-153">In release 8.1, you can now add due dates to the **Vendor transactions** list page.</span></span> <span data-ttu-id="426e2-154">**仕入先トランザクション**リスト ページで期日をクリックして、**期日および現金割引日を更新する**ダイアログ ボックスで期日、割引日、支払条件、および現金割引条件を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="426e2-154">By clicking on the due date in the **Vendor transactions** list page, you can also change due dates, discount dates, payment terms, and cash discount terms in the **Update due date and cash discount dates**  dialog box.</span></span>

### <a name="activate-the-feature"></a><span data-ttu-id="426e2-155">機能の有効化</span><span class="sxs-lookup"><span data-stu-id="426e2-155">Activate the feature</span></span>

<span data-ttu-id="426e2-156">**期日および現金割引日を更新する**ダイアログ ボックスを使用して、**仕入先トランザクション**リスト ページに期日を追加し、トランザクションの支払設定を変更するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="426e2-156">To add due dates to the **Vendor transactions** list page and change payment settings for a transaction by using the **Update due date and cash discount dates** dialog box, follow these steps.</span></span>

1. <span data-ttu-id="426e2-157">**買掛金勘定 \> 設定 \> 買掛金勘定パラメーター**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="426e2-157">Select **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="426e2-158">**決済**タブで、**期日を表示し編集を許可する**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="426e2-158">On the **Settlements** tab, set the **Show due date and allow edit** option to **Yes**.</span></span>
3. <span data-ttu-id="426e2-159">この機能を有効にするため、新しいフィールドが仕入先トランザクションに追加されました。</span><span class="sxs-lookup"><span data-stu-id="426e2-159">To enable this feature, new fields have been added to vendor transactions.</span></span> <span data-ttu-id="426e2-160">これらのフィールドは、新しいトランザクションが完了したときに入力されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-160">Those fields will be filled in when a new transaction is completed.</span></span> <span data-ttu-id="426e2-161">**期日および現金割引の日付を更新**ダイアログ ボックスを開くときに入力されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-161">They will also be filled in when you open the **Update due date and cash discount dates** dialog box.</span></span> <span data-ttu-id="426e2-162">**期日を表示し編集を許可**オプションを**はい**に設定するときに、**支払情報を更新**ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-162">When you set the **Show due date and allow edit** option to **Yes**, you will see the **Update payment information** dialog box.</span></span>  <span data-ttu-id="426e2-163">直ちに既存のトランザクションを更新するには、**すべての既存のトランザクションを更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="426e2-163">To update existing transactions immediately, select **Update all existing transactions**.</span></span> <span data-ttu-id="426e2-164">あるいは、新しいトランザクションに対してのみのフィールドに入力するには、**更新なしで続行する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="426e2-164">Alternatively, to fill in the fields only for new transactions, select **Continue without update**.</span></span>

<span data-ttu-id="426e2-165">**仕入先トランザクション** リスト ページに期日を追加し、トランザクションの期日および現金割引日を簡単に変更できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="426e2-165">The due date is now added to the **Vendor transactions** list page, so you can easily modify the due date and cash discount dates for transactions.</span></span>

### <a name="modify-the-payment-settings"></a><span data-ttu-id="426e2-166">支払設定を変更</span><span class="sxs-lookup"><span data-stu-id="426e2-166">Modify the payment settings</span></span>

<span data-ttu-id="426e2-167">**仕入先トランザクション**リスト ページでは、仕入先のすべてのトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-167">The **Vendor transactions** list page shows all transactions for a vendor.</span></span> <span data-ttu-id="426e2-168">トランザクションの期日を選択すると、ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-168">When you select the due date for a transaction, a dialog box appears.</span></span> <span data-ttu-id="426e2-169">このダイアログ ボックスでは、期日および割引の計算の基準日、期日、支払条件、現金割引の条件および現金割引の日付の基準日が表示されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-169">This dialog box shows the base date for due date and discount calculations, due date, payment terms, cash discount terms, and cash discount dates.</span></span>

<span data-ttu-id="426e2-170">各フィールドは編集時、トランザクションに異なる効果をもたらします。</span><span class="sxs-lookup"><span data-stu-id="426e2-170">Each field has a different effect on the transaction when you edit it:</span></span>

- <span data-ttu-id="426e2-171">**基準日の編集** - 期日および割引日は、基準日が文書日付であるかのように変更されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-171">**Edit the base date** - The due date and discount dates are changed as if the base date is the document date.</span></span>
- <span data-ttu-id="426e2-172">**期日の編集** - 期日のみが変更されます</span><span class="sxs-lookup"><span data-stu-id="426e2-172">**Edit the due date** - Only the due date is changed</span></span>
- <span data-ttu-id="426e2-173">**割引日を編集** - 割引日のみが変更されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-173">**Edit the discount dates** - Only the discount dates are changed.</span></span>
- <span data-ttu-id="426e2-174">**支払条件を編集** - 基準日および支払条件に基づき、期日は変更されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-174">**Edit the payment terms** - The due date is changed, based on the base date and the payment terms.</span></span>
- <span data-ttu-id="426e2-175">**現金割引の条件を編集** - 基準日と現金割引条件に基づき、現金割引は変更されます。</span><span class="sxs-lookup"><span data-stu-id="426e2-175">**Edit the cash discount terms** - The cash discounts are changed, based on the base date and the cash discount terms.</span></span>

<span data-ttu-id="426e2-176">支払設定の編集を終えたら、**閉じる**を選び変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="426e2-176">When you've finished editing the payment settings, select **Close** to save your changes.</span></span>
