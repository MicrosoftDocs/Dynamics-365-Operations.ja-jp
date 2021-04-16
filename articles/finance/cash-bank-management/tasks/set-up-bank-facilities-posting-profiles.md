---
title: 信用保証状についての銀行融資と転記プロファイルの設定
description: このタスクは、信用保証状を処理するために必要な銀行融資と転記プロファイルを作成します。
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1147650944ba40d1c8054444c09db9c5ee97bde3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834623"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="8571e-103">信用保証状についての銀行融資と転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="8571e-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8571e-104">このタスクは、信用保証状を処理するために必要な銀行融資と転記プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="8571e-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="8571e-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="8571e-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="8571e-106">一般会計パラメーター</span><span class="sxs-lookup"><span data-stu-id="8571e-106">General ledger parameter</span></span>
1. <span data-ttu-id="8571e-107">[現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8571e-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="8571e-108">[銀行ドキュメント] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8571e-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="8571e-109">[信用保証状の有効化] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8571e-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="8571e-110">[トランザクション仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8571e-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8571e-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8571e-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="8571e-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8571e-113">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="8571e-114">信用保証状の番号と信用保証状トランザクションの参照の番号順序コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="8571e-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="8571e-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-115">Click Save.</span></span>
9. <span data-ttu-id="8571e-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8571e-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="8571e-117">銀行融資の作成</span><span class="sxs-lookup"><span data-stu-id="8571e-117">Create Bank facility</span></span>
1. <span data-ttu-id="8571e-118">[現金および銀行管理] > [設定] > [銀行融資] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8571e-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="8571e-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-119">Click New.</span></span>
3. <span data-ttu-id="8571e-120">[融資グループ] フィールドに、信用保証状トランザクションの銀行融資グループ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="8571e-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="8571e-121">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8571e-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8571e-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-122">Click Save.</span></span>
6. <span data-ttu-id="8571e-123">[融資タイプ] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="8571e-124">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-124">Click New.</span></span>
8. <span data-ttu-id="8571e-125">[融資タイプ] フィールドに、銀行融資契約に関連する銀行融資タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8571e-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="8571e-126">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8571e-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="8571e-127">[融資グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8571e-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8571e-128">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8571e-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="8571e-129">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="8571e-130">[融資の種類] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8571e-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="8571e-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-131">Click Save.</span></span>
15. <span data-ttu-id="8571e-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8571e-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="8571e-133">銀行転記プロファイル</span><span class="sxs-lookup"><span data-stu-id="8571e-133">Bank posting profile</span></span>
1. <span data-ttu-id="8571e-134">[現金および銀行管理] > [設定] > [銀行ドキュメントの転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8571e-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="8571e-135">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-135">Click New.</span></span>
3. <span data-ttu-id="8571e-136">[アカウント/グループ番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8571e-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8571e-137">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8571e-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8571e-138">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8571e-139">[決済勘定] フィールドで、決済の主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="8571e-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="8571e-140">[手数料勘定] フィールドで、経費トランザクションの勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="8571e-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="8571e-141">[保証金勘定] フィールドで、マージン トランザクションの勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="8571e-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="8571e-142">[清算勘定] フィールドで、信用保証状トランザクションの清算勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="8571e-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="8571e-143">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8571e-143">Click Save.</span></span>
11. <span data-ttu-id="8571e-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8571e-144">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]