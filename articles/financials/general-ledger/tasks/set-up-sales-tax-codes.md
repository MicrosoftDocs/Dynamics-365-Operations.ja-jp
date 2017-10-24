--- 
title: "消費税コードを設定します"
description: "売上税コードは、法人が計算、収集、税務当局への支払いの義務のあるそれぞれの間接税または関税について作成されます。"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 968f4bb9f7d54cdb4de4f7842ed1777c9a9acd64
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="e24af-103">消費税コードを設定します</span><span class="sxs-lookup"><span data-stu-id="e24af-103">Set up sales tax codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e24af-104">売上税コードは、法人が計算、収集、税務当局への支払いの義務のあるそれぞれの間接税または関税について作成されます。</span><span class="sxs-lookup"><span data-stu-id="e24af-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="e24af-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="e24af-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="e24af-106">[税] > [間接税] > [売上税] > [売上税コード] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e24af-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="e24af-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e24af-107">Click New.</span></span>
3. <span data-ttu-id="e24af-108">[売上税コード] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e24af-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="e24af-109">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e24af-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e24af-110">[決済期間] を選択すると、この売上税の報告と支払いを行う売上税所轄官庁の指定や、その間隔の指定ができます。</span><span class="sxs-lookup"><span data-stu-id="e24af-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="e24af-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e24af-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e24af-112">総勘定元帳に売上税を転記する主勘定を指定するには、[元帳転記グループ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e24af-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="e24af-113">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e24af-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="e24af-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e24af-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="e24af-115">[計算] クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="e24af-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="e24af-116">[計算] クイックタブには、売上税額の計算方法を制御する複数のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="e24af-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="e24af-117">[アクション] ペインで [売上税コード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e24af-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="e24af-118">[値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e24af-118">Click Values.</span></span>
13. <span data-ttu-id="e24af-119">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="e24af-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e24af-120">税コードの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e24af-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="e24af-121">[計算] クイック タブの [元] フィールドで、単位あたりの金額がオンの場合、売上税金額の計算では、値にトランザクションの数量が乗算されます。</span><span class="sxs-lookup"><span data-stu-id="e24af-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="e24af-122">税コードが単位に基づく税でない場合、値は、売上税金額を計算するためにこの税コードの発生元に適用される割合を示す値になります。</span><span class="sxs-lookup"><span data-stu-id="e24af-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="e24af-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e24af-123">Click Save.</span></span>
16. <span data-ttu-id="e24af-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e24af-124">Close the page.</span></span>
17. <span data-ttu-id="e24af-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e24af-125">Click Save.</span></span>


