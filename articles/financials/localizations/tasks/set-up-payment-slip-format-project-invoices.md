--- 
title: "プロジェクト請求書の支払伝票形式の設定"
description: "通常、企業は、顧客に役立つように印刷した支払伝票を請求書に添付し、転記および決済用に支払参照を提供します。"
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 02/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9700571110a1b488e250dd8ee7b8c5c8f15cbc01
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-payment-slip-format-for-project-invoices"></a><span data-ttu-id="30318-103">プロジェクト請求書の支払伝票形式の設定</span><span class="sxs-lookup"><span data-stu-id="30318-103">Set up payment slip format for project invoices</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30318-104">通常、企業は、顧客に役立つように印刷した支払伝票を請求書に添付し、転記および決済用に支払参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="30318-104">Businesses commonly attach printed payment slips to invoices to assist customers and provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="30318-105">支払伝票は、売上請求書、自由書式の請求書に加え、プロジェクトまたはサービスの請求書、督促状、利子計算書、取引明細書に使用できます。</span><span class="sxs-lookup"><span data-stu-id="30318-105">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span> <span data-ttu-id="30318-106">支払伝票を処理するには、最初に債権者 ID 番号と支払伝票関連ドキュメントの形式を設定します。</span><span class="sxs-lookup"><span data-stu-id="30318-106">To process payment slips, first set up your creditor identification number and payment slip attachment formats.</span></span>

<span data-ttu-id="30318-107">この手順では、DEMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="30318-107">This procedure uses the DEMF demo company.</span></span> 

<span data-ttu-id="30318-108">この機能は、基本住所がデンマークにある法人でのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="30318-108">This functionality is available for legal entities whose primary address is in Denmark.</span></span>


## <a name="set-up-a-creditor-id-number"></a><span data-ttu-id="30318-109">債権者 ID 番号の設定</span><span class="sxs-lookup"><span data-stu-id="30318-109">Set up a creditor ID number</span></span>
1. <span data-ttu-id="30318-110">[組織管理] > [組織] > [法人] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="30318-110">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="30318-111">[銀行口座情報] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="30318-111">Expand or collapse the Bank account information section.</span></span>
3. <span data-ttu-id="30318-112">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-112">Click Edit.</span></span>
4. <span data-ttu-id="30318-113">[FI 債権者 ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30318-113">In the FI-Creditor ID field, type a value.</span></span>
5. <span data-ttu-id="30318-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-114">Click Save.</span></span>
6. <span data-ttu-id="30318-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="30318-115">Close the page.</span></span>

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a><span data-ttu-id="30318-116">請求書、利子計算書、督促状、および取引明細書の支払伝票形式の設定</span><span class="sxs-lookup"><span data-stu-id="30318-116">Set up a payment slip format for invoices, notes, letters, and statements</span></span>
1. <span data-ttu-id="30318-117">[売掛金勘定] > [設定] > [フォーム] > [フォーム設定] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="30318-117">Go to Accounts receivable > Setup > Forms > Form setup.</span></span>
2. <span data-ttu-id="30318-118">[請求書] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-118">Click the Invoice tab.</span></span>
3. <span data-ttu-id="30318-119">[顧客請求書] フィールドの [関連する支払添付書類] で、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-119">In the Associated payment attachment on customer invoice field, select an option.</span></span>
    * <span data-ttu-id="30318-120">[なし] – 支払伝票を印刷しません。</span><span class="sxs-lookup"><span data-stu-id="30318-120">None – Do not print a payment slip.</span></span> <span data-ttu-id="30318-121">支払額がデンマーク クローネ (DKK) 以外の通貨場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-121">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="30318-122">[FIK 751] – 支払伝票に支払額および期日を手動で書き込む場合は、FIK 751 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-122">FIK 751 – Print an FIK 751 payment slip if you intend to manually write the payment amount and due date on the payment slip.</span></span>   <span data-ttu-id="30318-123">[FIK 752] – 支払金額と期日事前が事前に印刷されたコンピュータで生成した支払伝票を使用する場合、FIK 752 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-123">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
4. <span data-ttu-id="30318-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-124">Click Save.</span></span>
5. <span data-ttu-id="30318-125">[自由書式の請求書] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-125">Click the Free text invoice tab.</span></span>
6. <span data-ttu-id="30318-126">[自由書式の請求書] フィールドの [関連する支払添付書類] で、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-126">In the Associated payment attachment on free text invoice field, select an option.</span></span>
    * <span data-ttu-id="30318-127">[なし] – 支払伝票を印刷しません。</span><span class="sxs-lookup"><span data-stu-id="30318-127">None – Do not print a payment slip.</span></span> <span data-ttu-id="30318-128">支払額がデンマーク クローネ (DKK) 以外の通貨場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-128">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="30318-129">[FIK 751] – 支払伝票に支払額および期日を手動で作成する場合は、FIK 751 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-129">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="30318-130">[FIK 752] – 支払金額と期日事前が事前に印刷されたコンピュータで生成した支払伝票を使用する場合、FIK 752 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-130">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
7. <span data-ttu-id="30318-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-131">Click Save.</span></span>
8. <span data-ttu-id="30318-132">[利子計算書] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-132">Click the Interest note tab.</span></span>
9. <span data-ttu-id="30318-133">[利子計算書] フィールドの [関連する支払添付書類] で、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-133">In the Associated payment attachment on interest note field, select an option.</span></span>
    * <span data-ttu-id="30318-134">[なし] – 支払伝票を印刷しません。</span><span class="sxs-lookup"><span data-stu-id="30318-134">None – Do not print a payment slip.</span></span> <span data-ttu-id="30318-135">支払額がデンマーク クローネ (DKK) 以外の通貨場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-135">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="30318-136">[FIK 751] – 支払伝票に支払額および期日を手動で作成する場合は、FIK 751 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-136">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="30318-137">[FIK 752] – 支払金額と期日事前が事前に印刷されたコンピュータで生成した支払伝票を使用する場合、FIK 752 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-137">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
10. <span data-ttu-id="30318-138">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-138">Click Save.</span></span>
11. <span data-ttu-id="30318-139">[督促状] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-139">Click the Collection letter tab.</span></span>
12. <span data-ttu-id="30318-140">[督促状] フィールドの [関連する支払添付書類] で、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-140">In the Associated payment attachment on collection letter field, select an option.</span></span>
    * <span data-ttu-id="30318-141">[なし] – 支払伝票を印刷しません。</span><span class="sxs-lookup"><span data-stu-id="30318-141">None – Do not print a payment slip.</span></span> <span data-ttu-id="30318-142">支払額がデンマーク クローネ (DKK) 以外の通貨場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-142">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="30318-143">[FIK 751] – 支払伝票に支払額および期日を手動で作成する場合は、FIK 751 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-143">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="30318-144">[FIK 752] – 支払金額と期日事前が事前に印刷されたコンピュータで生成した支払伝票を使用する場合、FIK 752 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-144">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
13. <span data-ttu-id="30318-145">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-145">Click Save.</span></span>
14. <span data-ttu-id="30318-146">[勘定明細書] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-146">Click the Account statement tab.</span></span>
15. <span data-ttu-id="30318-147">[勘定明細書] フィールドの [関連する支払添付書類] で、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-147">In the Associated payment attachment on account statement field, select an option.</span></span>
    * <span data-ttu-id="30318-148">[なし] – 支払伝票を印刷しません。</span><span class="sxs-lookup"><span data-stu-id="30318-148">None – Do not print a payment slip.</span></span> <span data-ttu-id="30318-149">支払額がデンマーク クローネ (DKK) 以外の通貨場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="30318-149">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="30318-150">[FIK 751] – 支払伝票に支払額および期日を手動で作成する場合は、FIK 751 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-150">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="30318-151">[FIK 752] – 支払金額と期日事前が事前に印刷されたコンピュータで生成した支払伝票を使用する場合、FIK 752 支払伝票を印刷します。</span><span class="sxs-lookup"><span data-stu-id="30318-151">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
16. <span data-ttu-id="30318-152">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30318-152">Click Save.</span></span>
17. <span data-ttu-id="30318-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="30318-153">Close the page.</span></span>

