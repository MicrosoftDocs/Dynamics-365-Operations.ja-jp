---
title: 顧客支払の預金
description: 顧客支払を預金します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afbf74d1cf3dc87e97dda0873115b5c7fa49ca3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834466"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="b3779-103">顧客支払の預金</span><span class="sxs-lookup"><span data-stu-id="b3779-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3779-104">顧客支払を預金します。</span><span class="sxs-lookup"><span data-stu-id="b3779-104">Deposit customer payments.</span></span> <span data-ttu-id="b3779-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3779-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b3779-106">[売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3779-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b3779-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3779-107">Click New.</span></span>
3. <span data-ttu-id="b3779-108">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3779-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b3779-109">支払仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3779-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="b3779-110">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3779-110">Click Lines.</span></span>
6. <span data-ttu-id="b3779-111">[口座] フィールドで、支払を記録している顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3779-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="b3779-112">[貸方] フィールドに支払金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3779-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="b3779-113">金額を空白にし、支払済み請求書を選択してシステムに計算させることができます。</span><span class="sxs-lookup"><span data-stu-id="b3779-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="b3779-114">[支払参照] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3779-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="b3779-115">支払の参照は、入力する支払の小切手番号にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b3779-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="b3779-116">預金伝票に支払を含めるためには、支払参照が必要となります。</span><span class="sxs-lookup"><span data-stu-id="b3779-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="b3779-117">[預金伝票の使用] ボックスをマークします。</span><span class="sxs-lookup"><span data-stu-id="b3779-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="b3779-118">支払額を預金残高に含める場合、この設定を「はい」に変更します。</span><span class="sxs-lookup"><span data-stu-id="b3779-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="b3779-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3779-119">Click New.</span></span>
11. <span data-ttu-id="b3779-120">[口座] フィールドで、次回に支払う顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3779-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="b3779-121">[貸方] フィールドに支払金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3779-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="b3779-122">[支払参照] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3779-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="b3779-123">[預金伝票の使用] ボックスをマークします。</span><span class="sxs-lookup"><span data-stu-id="b3779-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="b3779-124">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3779-124">Click Post.</span></span>
    * <span data-ttu-id="b3779-125">預金伝票を生成する前に、支払は転記されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b3779-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="b3779-126">これは、預金伝票が生成された後に支払が変更しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="b3779-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="b3779-127">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3779-127">Click Functions.</span></span>
17. <span data-ttu-id="b3779-128">[預金伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3779-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="b3779-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3779-129">Click OK.</span></span>
    * <span data-ttu-id="b3779-130">最初のページは預金伝票を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3779-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="b3779-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3779-131">Click OK.</span></span>
    * <span data-ttu-id="b3779-132">2 番目の手順は、預金伝票を印刷することですが、この手順は必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="b3779-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

