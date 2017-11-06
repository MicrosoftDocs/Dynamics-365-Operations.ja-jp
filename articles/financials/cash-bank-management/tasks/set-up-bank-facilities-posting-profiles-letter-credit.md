--- 
title: "信用状についての銀行融資と転記プロファイルの設定"
description: "この手順では、信用状のプロセスを必要とする銀行融資と転記プロファイルの作成を説明します。"
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 43422627f8529768ab9377c04568da531d6565c6
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="04704-103">信用状についての銀行融資と転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="04704-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04704-104">この手順では、信用状のプロセスを必要とする銀行融資と転記プロファイルの作成を説明します。</span><span class="sxs-lookup"><span data-stu-id="04704-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="04704-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="04704-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="04704-106">一般会計パラメーター</span><span class="sxs-lookup"><span data-stu-id="04704-106">General ledger parameter</span></span>
1. <span data-ttu-id="04704-107">[現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="04704-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="04704-108">[銀行ドキュメント] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="04704-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="04704-109">[輸入信用状の有効化] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="04704-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="04704-110">[輸出信用状の有効化] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="04704-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="04704-111">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-111">Click Save.</span></span>
6. <span data-ttu-id="04704-112">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="04704-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="04704-113">銀行融資の作成</span><span class="sxs-lookup"><span data-stu-id="04704-113">Create Bank facility</span></span>
1. <span data-ttu-id="04704-114">[現金および銀行管理] > [設定] > [銀行融資] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="04704-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="04704-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-115">Click New.</span></span>
3. <span data-ttu-id="04704-116">[融資グループ] フィールドで、銀行融資グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="04704-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="04704-117">[説明] フィールドに、銀行融資グループの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="04704-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="04704-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-118">Click Save.</span></span>
6. <span data-ttu-id="04704-119">[融資タイプ] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="04704-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-120">Click New.</span></span>
8. <span data-ttu-id="04704-121">[融資タイプ] フィールドに、固有のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="04704-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="04704-122">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04704-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="04704-123">[融資グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="04704-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="04704-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="04704-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="04704-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="04704-126">[融資の種類] フィールドで、銀行融資の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="04704-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="04704-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-127">Click Save.</span></span>
15. <span data-ttu-id="04704-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="04704-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="04704-129">銀行転記プロファイル</span><span class="sxs-lookup"><span data-stu-id="04704-129">Bank posting profile</span></span>
1. <span data-ttu-id="04704-130">[現金および銀行管理] > [設定] > [銀行ドキュメントの転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="04704-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="04704-131">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-131">Click New.</span></span>
3. <span data-ttu-id="04704-132">[アカウント/グループ番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="04704-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="04704-133">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="04704-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="04704-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="04704-135">決済の主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="04704-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="04704-136">この勘定は、キャッシュ フロー予測の計算時に使用されます。</span><span class="sxs-lookup"><span data-stu-id="04704-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="04704-137">[手数料勘定] フィールドで、経費トランザクションの勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="04704-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="04704-138">[保証金勘定] フィールドで、マージン トランザクションの勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="04704-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="04704-139">この勘定は、開始差益の転記時に借方に転記され、支払の転記時に貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="04704-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="04704-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04704-140">Click Save.</span></span>

