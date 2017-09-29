--- 
title: "特別償却の設定"
description: "この手順では、特別減価償却費を作成する方法およびそれを固定資産帳簿に関連付ける方法を説明します。"
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7e6ebb13084626b477b6e0b24acdc09e2c0d3d6d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="eff42-103">特別償却の設定</span><span class="sxs-lookup"><span data-stu-id="eff42-103">Set up bonus depreciation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eff42-104">この手順では、特別減価償却費を作成する方法およびそれを固定資産帳簿に関連付ける方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="eff42-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="eff42-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="eff42-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="eff42-106">特別減価償却費の作成</span><span class="sxs-lookup"><span data-stu-id="eff42-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="eff42-107">[固定資産] > [設定] > [特別減価償却費] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eff42-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="eff42-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eff42-108">Click New.</span></span>
3. <span data-ttu-id="eff42-109">[特別減価償却費] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eff42-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="eff42-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eff42-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="eff42-111">[割合] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eff42-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="eff42-112">割合が表示されなかった場合は金額を設定します。</span><span class="sxs-lookup"><span data-stu-id="eff42-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="eff42-113">特別減価償却費を固定資産グループ帳簿と関連付ける</span><span class="sxs-lookup"><span data-stu-id="eff42-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="eff42-114">[固定資産] > [設定] > [固定資産グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eff42-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="eff42-115">一覧で、特別減価償却費に関連する固定資産グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="eff42-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="eff42-116">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eff42-116">Click Books.</span></span>
4. <span data-ttu-id="eff42-117">一覧で、特別減価償却費に関連する帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="eff42-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="eff42-118">[特別減価償却費] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eff42-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="eff42-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eff42-119">Click New.</span></span>
7. <span data-ttu-id="eff42-120">[特別減価償却費] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="eff42-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="eff42-121">割合または金額の既定値は特別減価償却費の設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="eff42-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="eff42-122">[優先順位] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eff42-122">In the Priority field, enter a number.</span></span>


