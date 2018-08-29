--- 
title: "新しい福利厚生の作成"
description: "このタスクは、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。"
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 46a499caca0c7c39961d9aab04e046aa067f9779
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="create-new-benefits"></a><span data-ttu-id="22ca2-103">新しい福利厚生の作成</span><span class="sxs-lookup"><span data-stu-id="22ca2-103">Create new benefits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22ca2-104">このタスクは、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="22ca2-105">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="22ca2-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="22ca2-106">このタスクは、報酬と給付金マネージャーのために用意されています。</span><span class="sxs-lookup"><span data-stu-id="22ca2-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="22ca2-107">給付金の要素の作成</span><span class="sxs-lookup"><span data-stu-id="22ca2-107">Create benefit elements</span></span>
1. <span data-ttu-id="22ca2-108">[人事管理] > [給付金] > [設定] > [給付金の要素] に移動します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-108">Go to Human resources > Benefits > Setup > Benefit elements.</span></span>
2. <span data-ttu-id="22ca2-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ca2-109">Click New.</span></span>
3. <span data-ttu-id="22ca2-110">[タイプ] フィールドに、作成する福利厚生タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-110">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="22ca2-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22ca2-112">[同時登録] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-112">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="22ca2-113">複数の医療プランに登録する従業員の能力を制限するには、[種類ごとに 1 つの登録] を選択します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-113">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="22ca2-114">[給与カテゴリ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-114">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="22ca2-115">[計画] タブをクリックします</span><span class="sxs-lookup"><span data-stu-id="22ca2-115">Click the Plans tab.</span></span>
8. <span data-ttu-id="22ca2-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ca2-116">Click New.</span></span>
9. <span data-ttu-id="22ca2-117">[計画] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-117">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="22ca2-118">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-118">In the Description field, type a value.</span></span>
11. <span data-ttu-id="22ca2-119">[タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-119">In the Type field, enter or select a value.</span></span>
12. <span data-ttu-id="22ca2-120">[給与の影響] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-120">In the Payroll impact field, select an option.</span></span>
13. <span data-ttu-id="22ca2-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ca2-121">Click Save.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="22ca2-122">給付金の作成</span><span class="sxs-lookup"><span data-stu-id="22ca2-122">Create a benefit</span></span>
1. <span data-ttu-id="22ca2-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22ca2-123">Close the page.</span></span>
2. <span data-ttu-id="22ca2-124">[人事管理] > [福利厚生] > [福利厚生] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-124">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="22ca2-125">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="22ca2-125">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="22ca2-126">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-126">In the Plan field, enter or select a value.</span></span>
5. <span data-ttu-id="22ca2-127">[オプション] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-127">In the Option field, enter or select a value.</span></span>
6. <span data-ttu-id="22ca2-128">[有効開始] フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="22ca2-128">In the Effective field, enter a date and time.</span></span>
7. <span data-ttu-id="22ca2-129">[福利厚生の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ca2-129">Click Create benefit.</span></span>


