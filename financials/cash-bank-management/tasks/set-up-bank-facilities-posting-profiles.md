--- 
title: "信用保証状についての銀行融資と転記プロファイルの設定"
description: "このタスクは、信用保証状を処理するために必要な銀行融資と転記プロファイルを作成します。"
author: kweekley
manager: AnnBe
ms.date: 02/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c23fe66c58e9ceff74469cc8eab61eb606c57ee1
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="53025-103">信用保証状についての銀行融資と転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="53025-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53025-104">このタスクは、信用保証状を処理するために必要な銀行融資と転記プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="53025-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="53025-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="53025-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="53025-106">一般会計パラメーター</span><span class="sxs-lookup"><span data-stu-id="53025-106">General ledger parameter</span></span>
1. <span data-ttu-id="53025-107">[現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="53025-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="53025-108">[銀行ドキュメント] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="53025-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="53025-109">[信用保証状の有効化] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="53025-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="53025-110">[トランザクション仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="53025-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="53025-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="53025-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="53025-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="53025-113">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="53025-114">信用保証状の番号と信用保証状トランザクションの参照の番号順序コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="53025-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="53025-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-115">Click Save.</span></span>
9. <span data-ttu-id="53025-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53025-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="53025-117">銀行融資の作成</span><span class="sxs-lookup"><span data-stu-id="53025-117">Create Bank facility</span></span>
1. <span data-ttu-id="53025-118">[現金および銀行管理] > [設定] > [銀行融資] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="53025-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="53025-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-119">Click New.</span></span>
3. <span data-ttu-id="53025-120">[融資グループ] フィールドに、信用保証状トランザクションの銀行融資グループ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="53025-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="53025-121">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53025-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="53025-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-122">Click Save.</span></span>
6. <span data-ttu-id="53025-123">[融資タイプ] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="53025-124">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-124">Click New.</span></span>
8. <span data-ttu-id="53025-125">[融資タイプ] フィールドに、銀行融資契約に関連する銀行融資タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="53025-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="53025-126">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53025-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="53025-127">[融資グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="53025-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="53025-128">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="53025-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="53025-129">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="53025-130">[融資の種類] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="53025-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="53025-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-131">Click Save.</span></span>
15. <span data-ttu-id="53025-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53025-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="53025-133">銀行転記プロファイル</span><span class="sxs-lookup"><span data-stu-id="53025-133">Bank posting profile</span></span>
1. <span data-ttu-id="53025-134">[現金および銀行管理] > [設定] > [銀行ドキュメントの転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="53025-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="53025-135">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-135">Click New.</span></span>
3. <span data-ttu-id="53025-136">[アカウント/グループ番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="53025-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="53025-137">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="53025-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="53025-138">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="53025-139">[決済勘定] フィールドで、決済の主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="53025-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="53025-140">[手数料勘定] フィールドで、経費トランザクションの勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="53025-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="53025-141">[保証金勘定] フィールドで、マージン トランザクションの勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="53025-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="53025-142">[清算勘定] フィールドで、信用保証状トランザクションの清算勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="53025-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="53025-143">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53025-143">Click Save.</span></span>
11. <span data-ttu-id="53025-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53025-144">Close the page.</span></span>

