---
title: 新しい給付金の作成
description: このタスクは、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 1a41b5afed0a96383c99d60708ef3a6791e82df7
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009744"
---
# <a name="create-a-new-benefit"></a><span data-ttu-id="5a128-103">新しい給付金の作成</span><span class="sxs-lookup"><span data-stu-id="5a128-103">Create a new benefit</span></span>

<span data-ttu-id="5a128-104">このタスクは、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5a128-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="5a128-105">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="5a128-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="5a128-106">このタスクは、報酬と給付金マネージャーのために用意されています。</span><span class="sxs-lookup"><span data-stu-id="5a128-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="5a128-107">給付金の要素の作成</span><span class="sxs-lookup"><span data-stu-id="5a128-107">Create benefit elements</span></span>
1. <span data-ttu-id="5a128-108">[人事管理] > [給付金] > [設定] > [給付金の要素] に移動します。</span><span class="sxs-lookup"><span data-stu-id="5a128-108">Go to Human resources > Benefits > Setup > Benefit elements.</span></span>
2. <span data-ttu-id="5a128-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a128-109">Click New.</span></span>
3. <span data-ttu-id="5a128-110">[タイプ] フィールドに、作成する福利厚生タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a128-110">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="5a128-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a128-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5a128-112">[同時登録] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5a128-112">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="5a128-113">複数の医療プランに登録する従業員の能力を制限するには、[種類ごとに 1 つの登録] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a128-113">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="5a128-114">[給与カテゴリ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5a128-114">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="5a128-115">[計画] タブをクリックします</span><span class="sxs-lookup"><span data-stu-id="5a128-115">Click the Plans tab.</span></span>
8. <span data-ttu-id="5a128-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a128-116">Click New.</span></span>
9. <span data-ttu-id="5a128-117">[計画] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a128-117">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="5a128-118">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a128-118">In the Description field, type a value.</span></span>
11. <span data-ttu-id="5a128-119">[タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5a128-119">In the Type field, enter or select a value.</span></span>
12. <span data-ttu-id="5a128-120">[給与の影響] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5a128-120">In the Payroll impact field, select an option.</span></span>
13. <span data-ttu-id="5a128-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a128-121">Click Save.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="5a128-122">給付金の作成</span><span class="sxs-lookup"><span data-stu-id="5a128-122">Create a benefit</span></span>
1. <span data-ttu-id="5a128-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5a128-123">Close the page.</span></span>
2. <span data-ttu-id="5a128-124">[人事管理] > [福利厚生] > [福利厚生] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5a128-124">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="5a128-125">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="5a128-125">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="5a128-126">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5a128-126">In the Plan field, enter or select a value.</span></span>
5. <span data-ttu-id="5a128-127">[オプション] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5a128-127">In the Option field, enter or select a value.</span></span>
6. <span data-ttu-id="5a128-128">[有効開始] フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a128-128">In the Effective field, enter a date and time.</span></span>
7. <span data-ttu-id="5a128-129">[福利厚生の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a128-129">Click Create benefit.</span></span>

