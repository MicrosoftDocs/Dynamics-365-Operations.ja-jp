--- 
title: "仕入先請求書の売上税の計算と調整"
description: "オリジナルの元伝票が計算と異なる税額を表示している場合、転記前にこれらの金額を調整できます。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1af9228e5efd2cd6e414eebf766bb3475b44a360
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="bb7e9-103">仕入先請求書の売上税の計算と調整</span><span class="sxs-lookup"><span data-stu-id="bb7e9-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb7e9-104">オリジナルの元伝票が計算と異なる税額を表示している場合、転記前にこれらの金額を調整できます。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="bb7e9-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="bb7e9-106">[買掛金勘定] > [請求書] > [請求仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="bb7e9-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-107">Click New.</span></span>
3. <span data-ttu-id="bb7e9-108">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="bb7e9-109">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bb7e9-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bb7e9-111">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-111">Click Lines.</span></span>
7. <span data-ttu-id="bb7e9-112">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="bb7e9-113">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="bb7e9-114">[請求書] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="bb7e9-115">[貸方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="bb7e9-116">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="bb7e9-117">[売上税] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-117">Click Sales tax.</span></span>
13. <span data-ttu-id="bb7e9-118">[実際の売上税の合計金額] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="bb7e9-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-119">Click OK.</span></span>
15. <span data-ttu-id="bb7e9-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-120">Click Save.</span></span>
16. <span data-ttu-id="bb7e9-121">[売上税] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-121">Click Sales tax.</span></span>
17. <span data-ttu-id="bb7e9-122">[調整] タブで、売上税コードごとに売上税金額を調整できます。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="bb7e9-123">[計算上の金額から実績をリセット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="bb7e9-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-124">Click OK.</span></span>
20. <span data-ttu-id="bb7e9-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb7e9-125">Click Save.</span></span>


