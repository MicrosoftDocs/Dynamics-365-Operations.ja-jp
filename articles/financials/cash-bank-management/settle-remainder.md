---
title: "残余決済"
description: "その金額を勘定科目に適用することで、決済活動から残りの金額を決済することができます。"
author: mikefalkner
manager: aolson
ms.date: 10/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 18eaadf417ce6d0aacf0b13b3e4f857e06031e66
ms.openlocfilehash: 408a36a7cf221463b38260bd8830b422e58ccb64
ms.contentlocale: ja-jp
ms.lasthandoff: 01/22/2019

---

# <a name="settle-remainder"></a><span data-ttu-id="4a4f9-103">残余決済</span><span class="sxs-lookup"><span data-stu-id="4a4f9-103">Settle remainder</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a4f9-104">その金額を勘定科目または他の顧客に適用することで、決済活動から残りの金額を決済することができます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-104">You can settle the amount remaining from settlement activity by applying that amount to a ledger account or another customer.</span></span> <span data-ttu-id="4a4f9-105">仕訳帳に入力された金額を決済するとき、または未処理トランザクションのみを決済するときに、残りの部分を決済できます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-105">You can settle the remainder when you are settling amounts entered into a journal or when you are only settling open transactions.</span></span>

## <a name="setting-up-defaults"></a><span data-ttu-id="4a4f9-106">既定値の設定</span><span class="sxs-lookup"><span data-stu-id="4a4f9-106">Setting up defaults</span></span> 
<span data-ttu-id="4a4f9-107">残余決済機能を有効にして、残余決済を使用する前に、既定の設定を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-107">You must enable the Settle remainder feature and set up the default settings before you use Settle remainder</span></span>

1)  <span data-ttu-id="4a4f9-108">**売掛金 > パラメーター > 決済**または**買掛金 > パラメーター > 決済**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-108">Click **Accounts receivable > Parameters > Settlements** or **Accounts payable > Parameters > Settlements**</span></span>
2)  <span data-ttu-id="4a4f9-109">**決済**タブを選択し、**残余決済の有効化**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-109">Select the **Settlement** tab and click **Enable settle remainder**</span></span>
3)  <span data-ttu-id="4a4f9-110">**既定の理由コード**で、既定の理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-110">In **Default reason code**, select a default reason code.</span></span> <span data-ttu-id="4a4f9-111">**売掛金 > 設定 > 顧客損金処理理由コード**または**買掛金 > 設定 > 顧客損金処理理由コード**で、理由コードは既に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-111">The reason codes must have already been set up in **Accounts receivable > Setup > Customer write-off reason codes** or **Accounts payable > Setup > Customer write-off reason codes**.</span></span> <span data-ttu-id="4a4f9-112">**既定の残余決済勘定**は、で損金処理理由コードに割り当てられる既定勘定になります。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-112">The **Default settle remainder account** will default to the account assigned to the write-off reason code.</span></span>
3)  <span data-ttu-id="4a4f9-113">**既定の残余決済勘定**を必要に応じて更新します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-113">Update the **Default settle remainder account** as needed.</span></span>
4)  <span data-ttu-id="4a4f9-114">**既定の仕訳帳名**で、未処理トランザクションのみを決済する際に支払仕訳帳を作成する場合、使用する支払仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-114">In the **Default journal name**, select a payment journal that will be used if you want to create a payment journal when you only settling open transactions.</span></span> <span data-ttu-id="4a4f9-115">残余決済機能を有効にした場合は、既定の仕訳帳名を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-115">If you enable the settle remainder feature, you must add a default journal name.</span></span>

## <a name="settle-remainder-from-a-journal"></a><span data-ttu-id="4a4f9-116">仕訳帳の残余を決済します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-116">Settle remainder from a journal</span></span>
<span data-ttu-id="4a4f9-117">**残余決済**機能を有効にしない場合でも、引き続き仕訳帳にトランザクションを入力し、過去に行われたようにそれに対してトランザクションを決済することができます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-117">If you do not enable the **Settle remainder** feature, you can still enter a transaction in a journal and then settle transactions against it as you have done in the past.</span></span> <span data-ttu-id="4a4f9-118">**OK** ボタンをクリックすると、請求書の未処理残高が現金金額から差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-118">When you click the **OK** button, the open balance on the invoice is reduced by the cash amount.</span></span> <span data-ttu-id="4a4f9-119">現金で請求書が完全に決済されない場合、請求書は後で決済される残高で未処理のままになります。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-119">If the cash does not fully settle the invoice, the invoice is left open with a remaining amount to be settled at a later time.</span></span>

<span data-ttu-id="4a4f9-120">**残余決済**機能が有効な場合、残高を勘定科目に決済することができます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-120">When the **Settle remainder** feature is enabled, you can settle the remaining amount to a ledger account.</span></span> <span data-ttu-id="4a4f9-121">請求書を未処理のままにする代わりに、残高を別の顧客勘定 (顧客トランザクション用) または別の仕入先 (仕入先トランザクション用) に転記することもできます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-121">You can also transfer the remainder to another customer account (for customer transactions) or another vendor (for vendor transactions) instead of leaving the invoices open.</span></span> 

<span data-ttu-id="4a4f9-122">**決済**ページで残余決済するために、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-122">To settle the remainder from the **Settlement** page, perform the following steps:</span></span>

1)  <span data-ttu-id="4a4f9-123">**決済**ページで、決済する請求書またはトランザクションをマークします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-123">On the **Settlement** page, mark the invoices or transactions that you want to settle.</span></span>
2)  <span data-ttu-id="4a4f9-124">**残余決済**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-124">Click the **Settle remainder** button.</span></span>
3)  <span data-ttu-id="4a4f9-125">ダイアログ ボックスが表示され、元帳勘定に対して決済される金額、残余決済に使用される日付、パラメーターからの既定の理由コード、およびパラメーターからの既定の勘定が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-125">A dialog box will display, showing the amount that will be settled against a ledger account, the date that will be used to settle the remainder, the default reason code from the parameters, and the default account from the parameters.</span></span> 
4)  <span data-ttu-id="4a4f9-126">既定の理由を変更する場合は、新しい決済の理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-126">Select a new settlement reason if you want to change the default reason.</span></span> <span data-ttu-id="4a4f9-127">決済勘定は、理由コードに関連付けられている勘定に変更されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-127">The settlement account will be changed to the account associated with the reason code.</span></span>
5)  <span data-ttu-id="4a4f9-128">変更する場合は、決済勘定を編集します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-128">Edit the settlement account if you want to change it.</span></span>
6)  <span data-ttu-id="4a4f9-129">顧客トランザクションを決済していて残金を別の顧客に振り替えたい場合は、**顧客勘定に対して残余決済する**で顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-129">If you are settling customer transactions and you want the remainder to be moved to another customer, then select a customer in the **Settle remainder against customer account**.</span></span> <span data-ttu-id="4a4f9-130">仕入先トランザクションを決済していて残金を別の仕入先に振り替えたい場合は、**仕入先勘定に対して残余決済する**で仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-130">If you are settling vendor transactions and you want the remainder to be moved to another vendor, then select a vendor in the **Settle remainder against vendor account**.</span></span>
6)  <span data-ttu-id="4a4f9-131">**残余決済**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-131">Click **Settle remainder**.</span></span>
7)  <span data-ttu-id="4a4f9-132">**仕訳帳**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-132">The **Journal** page will display.</span></span> <span data-ttu-id="4a4f9-133">追加の仕訳帳明細行は、金額として残余決済金額を使用し、相手勘定として残余決済勘定を使用して、仕訳に追加されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-133">An additional journal line will be added to the journal with the settle remainder amount as the amount and with the settlement remainder account as the offset account.</span></span> <span data-ttu-id="4a4f9-134">他の顧客または仕入先に決済金額を転記できるように顧客または仕入先を追加した場合は、その顧客または仕入先に決済金額を転記するための明細行が仕訳帳に追加されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-134">If you added a customer or vendor so that you can move the settlement amount to another customer or vendor, then an additional line will be added to the journal to move the settlement amount to that customer or vendor.</span></span>

<span data-ttu-id="4a4f9-135">仕訳帳を転記すると、未処理トランザクションが完全に決済されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-135">When you post the journal, the open transaction will be fully settled.</span></span> 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a><span data-ttu-id="4a4f9-136">未処理トランザクションのみを決済するときに、残余決済をします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-136">Settle remainder when you are only settling open transactions</span></span>
<span data-ttu-id="4a4f9-137">仕訳帳なしの未処理トランザクションを決済するときにも、残余決済ができます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-137">You can also settle the remainder when you are settling open transactions without a journal.</span></span>

<span data-ttu-id="4a4f9-138">残余決済をするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-138">To settle the remainder, perform the following steps:</span></span>

1)  <span data-ttu-id="4a4f9-139">**決済**ページで、決済する請求書またはトランザクションをマークします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-139">On the **Settlement** page, mark the invoices or transactions that you want to settle</span></span>
2)  <span data-ttu-id="4a4f9-140">**残余決済**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-140">Click on **Settle remainder**</span></span>
3)  <span data-ttu-id="4a4f9-141">ダイアログ ボックスが表示され、元帳勘定に対して決済される金額、残余決済に使用される日付、パラメーターからの既定の理由コード、およびパラメーターからの既定の勘定が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-141">A dialog box will display, showinh the amount that will be settled against a ledger account, the date that will be used to settle the remainder, the default reason code from the parameters, and the default account from the parameters.</span></span> 
4)  <span data-ttu-id="4a4f9-142">既定の理由を変更する場合は、新しい決済の理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-142">Select a new settlement reason if you want to change the default reason.</span></span> <span data-ttu-id="4a4f9-143">決済勘定は、理由コードに関連付けられている勘定に変更されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-143">The settlement account will be changed to the account associated with the reason code.</span></span>
5)  <span data-ttu-id="4a4f9-144">変更する場合は、**決済勘定**を編集します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-144">Edit the **settlement account** if you want to change it.</span></span>
6)  <span data-ttu-id="4a4f9-145">顧客トランザクションを決済していて残金を別の顧客に振り替えたい場合は、**顧客勘定に対して残余決済する**で顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-145">If you are settling customer transactions and you want the remainder to be moved to another customer, then select a customer in the **Settle remainder against customer account**.</span></span> <span data-ttu-id="4a4f9-146">仕入先トランザクションを決済していて残金を別の仕入先に振り替えたい場合は、 **仕入先勘定に対する残余決済**で仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-146">If you are settling vendor transactions and you want the remainder to be moved to another vendor, then select a vendor in the **Settle remainder against vendor account**</span></span>
7)  <span data-ttu-id="4a4f9-147">また、決済残高を含む支払仕訳帳を作成するか、または仕訳帳なしで転記するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-147">You can also choose to create a payment journal with the settlement remainder or just post it without a journal.</span></span> <span data-ttu-id="4a4f9-148">支払仕訳帳を作成するには、**仕訳帳で編集**で**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-148">Select **Yes** for **Edit in journal** to create a payment journal.</span></span> <span data-ttu-id="4a4f9-149">作成した支払仕訳帳を編集することができます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-149">You will be able to edit the payment journal that you create.</span></span>
8)  <span data-ttu-id="4a4f9-150">**残余決済**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-150">Click **Settle remainder**.</span></span> <span data-ttu-id="4a4f9-151">仕訳帳を作成することを選択した場合、ボタンは**仕訳帳の作成**に変わります。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-151">If you chose to create a journal, the button will change to **Create journal**.</span></span> <span data-ttu-id="4a4f9-152">代わりに、**仕訳帳の作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-152">Click **Create journal** instead.</span></span>
9)  <span data-ttu-id="4a4f9-153">支払仕訳帳を作成した場合は、**残余決済**をクリックした後に仕訳帳ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-153">If you created a payment journal, the journal page will open after you click **Settle remainder**.</span></span> <span data-ttu-id="4a4f9-154">仕訳帳明細行は、金額として残余決済金額を使用し、相手勘定として残余決済勘定を使用して、仕訳に追加されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-154">A journal line will be added to the journal with the settle remainder amount as the amount and with the settlement remainder account as the offset account.</span></span> <span data-ttu-id="4a4f9-155">他の顧客または仕入先に決済金額を転記できるように顧客または仕入先を追加した場合は、その顧客または仕入先に決済金額を転記するための明細行が仕訳帳に追加されます。</span><span class="sxs-lookup"><span data-stu-id="4a4f9-155">If you added a customer or vendor so that you can move the settlement amount to another customer or vendor, then an additional line will be added to the journal to move the settlement amount to that customer or vendor.</span></span>

