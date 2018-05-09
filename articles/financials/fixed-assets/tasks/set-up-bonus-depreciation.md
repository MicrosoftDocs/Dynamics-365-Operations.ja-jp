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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b855502c67ae6889c44ba30d8ea5771b1e723484
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="be6f3-103">特別償却の設定</span><span class="sxs-lookup"><span data-stu-id="be6f3-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be6f3-104">この手順では、特別減価償却費を作成する方法およびそれを固定資産帳簿に関連付ける方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="be6f3-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="be6f3-106">特別減価償却費の作成</span><span class="sxs-lookup"><span data-stu-id="be6f3-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="be6f3-107">[固定資産] > [設定] > [特別減価償却費] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="be6f3-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be6f3-108">Click New.</span></span>
3. <span data-ttu-id="be6f3-109">[特別減価償却費] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="be6f3-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="be6f3-111">[割合] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="be6f3-112">割合が表示されなかった場合は金額を設定します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="be6f3-113">特別減価償却費を固定資産グループ帳簿と関連付ける</span><span class="sxs-lookup"><span data-stu-id="be6f3-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="be6f3-114">[固定資産] > [設定] > [固定資産グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="be6f3-115">一覧で、特別減価償却費に関連する固定資産グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="be6f3-116">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be6f3-116">Click Books.</span></span>
4. <span data-ttu-id="be6f3-117">一覧で、特別減価償却費に関連する帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="be6f3-118">[特別減価償却費] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be6f3-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="be6f3-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be6f3-119">Click New.</span></span>
7. <span data-ttu-id="be6f3-120">[特別減価償却費] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="be6f3-121">割合または金額の既定値は特別減価償却費の設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="be6f3-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="be6f3-122">[優先順位] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be6f3-122">In the Priority field, enter a number.</span></span>


