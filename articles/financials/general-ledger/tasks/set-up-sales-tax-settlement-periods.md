--- 
title: "消費税精算期間を設定します"
description: "売上税決済期間は、売上税の報告および支払が必要な間隔についての情報を含みます。"
author: twheeloc
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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6de8dbd33a02183ee8bafca720c3738e8eac44e8
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="ca14d-103">消費税精算期間を設定します</span><span class="sxs-lookup"><span data-stu-id="ca14d-103">Set up sales tax settlement periods</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca14d-104">売上税決済期間は、売上税の報告および支払が必要な間隔についての情報を含みます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="ca14d-105">決済プロセスは、特定の日付範囲の決済期間に実行できます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="ca14d-106">決済期間に関連付けられたすべての税コードが決済されます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="ca14d-107">関連する売上税所轄官庁の設定に応じて、未払税金は仕入先または総勘定元帳勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="ca14d-108">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="ca14d-109">[税] > [間接税] > [売上税] > [売上税決済期間] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="ca14d-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca14d-110">Click New.</span></span>
3. <span data-ttu-id="ca14d-111">[決済期間] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="ca14d-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ca14d-113">[所轄官庁] フィールドで、決済期間について作成されたレポートおよび支払を受け取る売上税所轄官庁を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="ca14d-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ca14d-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca14d-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ca14d-116">[支払条件] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ca14d-117">関連する売上税所轄官庁を仕入先として設定すると、売上税の決済により、未処理の仕入先請求書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="ca14d-118">支払条件では、未処理の仕入先請求書の期日を定義します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="ca14d-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ca14d-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca14d-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ca14d-121">決済期間間隔のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="ca14d-122">期間毎の間隔の単位の単位数を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="ca14d-123">たとえば、四半期は 3 か月あります。</span><span class="sxs-lookup"><span data-stu-id="ca14d-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="ca14d-124">[売上税決済にバッチ処理を使用する] のチェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="ca14d-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="ca14d-125">決済期間の決済プロセスは、バックグラウンドのバッチ ジョブとして処理することができます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="ca14d-126">これは、期間内に大量の税トランザクションを処理する必要があるときにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ca14d-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="ca14d-127">[間隔] タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="ca14d-128">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca14d-128">Click Add.</span></span>
16. <span data-ttu-id="ca14d-129">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="ca14d-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="ca14d-130">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="ca14d-131">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca14d-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="ca14d-132">[新しい間隔] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca14d-132">Click New period interval.</span></span>
    * <span data-ttu-id="ca14d-133">最初の間隔を入力すると、新しい期間は自動的に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="ca14d-134">必要に応じて、新しい間隔を後で追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="ca14d-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ca14d-135">Close the page.</span></span>


