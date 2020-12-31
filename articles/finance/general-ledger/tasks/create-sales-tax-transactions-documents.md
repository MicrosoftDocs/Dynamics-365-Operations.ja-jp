---
title: ドキュメントの売上税トランザクションの作成
description: ドキュメントの売上税は、ドキュメント明細行の売上税グループと品目売上税グループを指定することにより計算されます。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11e006e41f467a594521dfc601f46b4d1b492ce5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445271"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="d7122-103">ドキュメントの売上税トランザクションの作成</span><span class="sxs-lookup"><span data-stu-id="d7122-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7122-104">ドキュメントの売上税は、ドキュメント明細行の売上税グループと品目売上税グループを指定することにより計算されます。</span><span class="sxs-lookup"><span data-stu-id="d7122-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="d7122-105">これらはマスター データから既定値が取得されますが、必要に応じて手動で変更できます。</span><span class="sxs-lookup"><span data-stu-id="d7122-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="d7122-106">計算済売上税は、明細行とドキュメント レベルで確認できます。</span><span class="sxs-lookup"><span data-stu-id="d7122-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="d7122-107">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="d7122-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d7122-108">[売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d7122-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="d7122-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-109">Click New.</span></span>
3. <span data-ttu-id="d7122-110">[顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7122-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d7122-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d7122-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d7122-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d7122-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-113">Click OK.</span></span>
7. <span data-ttu-id="d7122-114">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d7122-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d7122-115">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7122-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d7122-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d7122-117">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7122-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="d7122-118">[明細行の詳細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="d7122-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="d7122-119">[設定] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="d7122-120">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7122-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="d7122-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d7122-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="d7122-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="d7122-123">[財務] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-123">Click Financials.</span></span>
17. <span data-ttu-id="d7122-124">[売上税] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-124">Click Sales tax.</span></span>
18. <span data-ttu-id="d7122-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-125">Click OK.</span></span>
19. <span data-ttu-id="d7122-126">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-126">Click Add line.</span></span>
20. <span data-ttu-id="d7122-127">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d7122-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="d7122-128">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7122-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="d7122-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d7122-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="d7122-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="d7122-131">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7122-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="d7122-132">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7122-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="d7122-133">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d7122-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="d7122-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="d7122-135">[アクション] ペインで [販売] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="d7122-136">[売上税] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-136">Click Sales tax.</span></span>
30. <span data-ttu-id="d7122-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7122-137">Click OK.</span></span>

