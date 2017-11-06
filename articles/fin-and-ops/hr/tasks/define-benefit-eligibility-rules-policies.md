--- 
title: "給付金の適格性ルールおよびポリシーの定義"
description: "この記録は、給付金の適格性ルールとポリシーを作成する方法、給付金にルールを割り当てる方法を示します。"
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c570574d15bbc55b4d0d79b8e62d74adcc15b387
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="82020-103">給付金の適格性ルールおよびポリシーの定義</span><span class="sxs-lookup"><span data-stu-id="82020-103">Define benefit eligibility rules and policies</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82020-104">この記録は、給付金の適格性ルールとポリシーを作成する方法、給付金にルールを割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="82020-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="82020-105">この記録の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="82020-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="82020-106">給付金の適格性ポリシー ルールのタイプを作成する</span><span class="sxs-lookup"><span data-stu-id="82020-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="82020-107">[人事管理] > [給付金] > [適格性] > [給付金の適格性ポリシー タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82020-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="82020-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-108">Click New.</span></span>
3. <span data-ttu-id="82020-109">[ルール名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="82020-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="82020-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="82020-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82020-111">[クエリ名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="82020-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="82020-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="82020-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-113">Click Save.</span></span>
8. <span data-ttu-id="82020-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="82020-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="82020-115">給付金の適格性ポリシー</span><span class="sxs-lookup"><span data-stu-id="82020-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="82020-116">[人事管理] > [給付金] > [適格性] > [給付金の適格性ポリシ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82020-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="82020-117">既存の給付金のポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="82020-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="82020-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="82020-119">[ポリシーの組織] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="82020-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="82020-120">ポリシーに追加する組織をここで追加、または削除できます。</span><span class="sxs-lookup"><span data-stu-id="82020-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="82020-121">[ポリシー ルール] のセクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="82020-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="82020-122">一覧で、以前に作成したポリシー ルールを検索します。</span><span class="sxs-lookup"><span data-stu-id="82020-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="82020-123">[ポリシー ルールの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="82020-124">[有効日] フィールドに、有効にするポリシーの有効日を入力します。</span><span class="sxs-lookup"><span data-stu-id="82020-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="82020-125">有効日と終了日の設定により、ポリシー ルールを修正でき、それらの変更を有効化するときに、ポリシーへの変更を行う手間が省かれます。</span><span class="sxs-lookup"><span data-stu-id="82020-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="82020-126">たとえば、販売マネージャにのみルールを適用する場合、職位は販売マネージャーであることを説明する [Where] 句を作成できます。</span><span class="sxs-lookup"><span data-stu-id="82020-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="82020-127">ルールでは、複数の [Where] ステートメントを AND と OR で結合して使用できます。</span><span class="sxs-lookup"><span data-stu-id="82020-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="82020-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-128">Click OK.</span></span>
11. <span data-ttu-id="82020-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="82020-129">Close the page.</span></span>
12. <span data-ttu-id="82020-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="82020-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="82020-131">ルールに寄付金を割り当てる</span><span class="sxs-lookup"><span data-stu-id="82020-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="82020-132">[人事管理] > [福利厚生] > [福利厚生] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="82020-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="82020-133">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="82020-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="82020-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="82020-135">[適格性ルール] のセクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="82020-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="82020-136">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-136">Click Edit.</span></span>
6. <span data-ttu-id="82020-137">[適格性] フィールドで、「ルール ベース」を一覧から選択します。</span><span class="sxs-lookup"><span data-stu-id="82020-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="82020-138">[ルール タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="82020-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="82020-139">一覧で、以前に作成したルールを検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="82020-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="82020-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="82020-141">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="82020-141">Click Save.</span></span>
11. <span data-ttu-id="82020-142">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="82020-142">Close the form.</span></span>

