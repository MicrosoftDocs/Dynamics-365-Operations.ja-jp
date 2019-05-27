---
title: 仕入先請求書の売上税の計算と調整
description: オリジナルの元伝票が計算と異なる税額を表示している場合、転記前にこれらの金額を調整できます。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545174"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="e99fb-103">仕入先請求書の売上税の計算と調整</span><span class="sxs-lookup"><span data-stu-id="e99fb-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e99fb-104">オリジナルの元伝票が計算と異なる税額を表示している場合、転記前にこれらの金額を調整できます。</span><span class="sxs-lookup"><span data-stu-id="e99fb-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="e99fb-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="e99fb-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="e99fb-106">[買掛金勘定] > [請求書] > [請求仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e99fb-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="e99fb-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-107">Click New.</span></span>
3. <span data-ttu-id="e99fb-108">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e99fb-109">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e99fb-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e99fb-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e99fb-111">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-111">Click Lines.</span></span>
7. <span data-ttu-id="e99fb-112">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="e99fb-113">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e99fb-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="e99fb-114">[請求書] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e99fb-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="e99fb-115">[貸方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e99fb-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="e99fb-116">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e99fb-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="e99fb-117">[売上税] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-117">Click Sales tax.</span></span>
13. <span data-ttu-id="e99fb-118">[実際の売上税の合計金額] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e99fb-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="e99fb-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-119">Click OK.</span></span>
15. <span data-ttu-id="e99fb-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-120">Click Save.</span></span>
16. <span data-ttu-id="e99fb-121">[売上税] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-121">Click Sales tax.</span></span>
17. <span data-ttu-id="e99fb-122">[調整] タブで、売上税コードごとに売上税金額を調整できます。</span><span class="sxs-lookup"><span data-stu-id="e99fb-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="e99fb-123">[計算上の金額から実績をリセット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="e99fb-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-124">Click OK.</span></span>
20. <span data-ttu-id="e99fb-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e99fb-125">Click Save.</span></span>

