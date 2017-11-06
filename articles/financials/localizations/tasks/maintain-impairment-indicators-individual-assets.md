--- 
title: "個別資産の減損インジケーターの管理 (日本)"
description: "このタスクを使用して、個別資産の減損インジケーターの管理方法を把握します。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 637779191db297695e632f6bdd0e52457ee3d45b
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-impairment-indicators-on-individual-assets-japan"></a><span data-ttu-id="dced2-103">個別資産の減損インジケーターの管理 (日本)</span><span class="sxs-lookup"><span data-stu-id="dced2-103">Maintain impairment indicators on individual assets (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dced2-104">このタスクを使用して、個別資産の減損インジケーターの管理方法を把握します。</span><span class="sxs-lookup"><span data-stu-id="dced2-104">Use this task to learn how to maintain impairment indicators on individual assets.</span></span>



<span data-ttu-id="dced2-105">この手順を実行する前に、「減損会計の共通パラメーターの設定」タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="dced2-105">Run the task 'Setup impairment accounting common parameters' prior to this running this procedure.</span></span> 



<span data-ttu-id="dced2-106">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="dced2-106">This task uses the JPMF demo company data.</span></span>


## <a name="update-impairment-indicator-on-a-single-fixed-asset"></a><span data-ttu-id="dced2-107">単一の固定資産の減損インジケーターを更新</span><span class="sxs-lookup"><span data-stu-id="dced2-107">Update impairment indicator on a single fixed asset</span></span>
1. <span data-ttu-id="dced2-108">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="dced2-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="dced2-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="dced2-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dced2-110">例: TOOLM-000006</span><span class="sxs-lookup"><span data-stu-id="dced2-110">Example: TOOLM-000006</span></span>  
3. <span data-ttu-id="dced2-111">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dced2-111">Click Books.</span></span>
4. <span data-ttu-id="dced2-112">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dced2-112">Click Functions.</span></span>
5. <span data-ttu-id="dced2-113">[減損インジケーターの更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dced2-113">Click Update impairment indicators.</span></span>
6. <span data-ttu-id="dced2-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dced2-114">Click New.</span></span>
7. <span data-ttu-id="dced2-115">[日付の変更] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-115">In the Modify date field, enter a date.</span></span>
    * <span data-ttu-id="dced2-116">例: 2013-04-01</span><span class="sxs-lookup"><span data-stu-id="dced2-116">Example: 2013-04-01</span></span>  
8. <span data-ttu-id="dced2-117">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="dced2-118">[割引前キャッシュ フロー] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-118">In the Undiscounted cash flow field, enter a number.</span></span>
    * <span data-ttu-id="dced2-119">この例では、フィールドに「3900000」を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-119">In this example, enter field '3900000.'</span></span>  
10. <span data-ttu-id="dced2-120">[回収可能金額] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-120">In the Recoverable amount field, enter a number.</span></span>
    * <span data-ttu-id="dced2-121">この例では、フィールドに「3350226」を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-121">In this example, enter field '3350226.'</span></span>  
11. <span data-ttu-id="dced2-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dced2-122">Click Save.</span></span>

## <a name="update-impairment-indicator-on-the-impairment-management-form"></a><span data-ttu-id="dced2-123">減損管理フォームの減損のインジケーターを更新</span><span class="sxs-lookup"><span data-stu-id="dced2-123">Update impairment indicator on the impairment management form</span></span>
1. <span data-ttu-id="dced2-124">次の順に移動します: [固定資産] ></span><span class="sxs-lookup"><span data-stu-id="dced2-124">Go to Fixed assets > ..</span></span> <span data-ttu-id="dced2-125">> ..</span><span class="sxs-lookup"><span data-stu-id="dced2-125">> ..</span></span> <span data-ttu-id="dced2-126">> [減損管理]。</span><span class="sxs-lookup"><span data-stu-id="dced2-126">> Impairment management.</span></span>
2. <span data-ttu-id="dced2-127">[クエリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dced2-127">Click Query.</span></span>
3. <span data-ttu-id="dced2-128">固定資産グループの行の、[基準] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="dced2-128">In the Criteria field for the fixed asset group row, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dced2-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dced2-129">Click OK.</span></span>
5. <span data-ttu-id="dced2-130">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="dced2-130">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dced2-131">TOOLM-000007</span><span class="sxs-lookup"><span data-stu-id="dced2-131">TOOLM-000007</span></span>  
6. <span data-ttu-id="dced2-132">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="dced2-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dced2-133">TOOLM-000008</span><span class="sxs-lookup"><span data-stu-id="dced2-133">TOOLM-000008</span></span>  
7. <span data-ttu-id="dced2-134">[減損インジケーターの更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dced2-134">Click Update impairment indicators.</span></span>
8. <span data-ttu-id="dced2-135">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="dced2-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dced2-136">固定資産番号「TOOLM-000007」を持つレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="dced2-136">Select the record with Fixed asset number 'TOOLM-000007.'</span></span>  
9. <span data-ttu-id="dced2-137">[日付の変更] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-137">In the Modify date field, enter a date.</span></span>
    * <span data-ttu-id="dced2-138">日付を定義 = 2013-04-01</span><span class="sxs-lookup"><span data-stu-id="dced2-138">Define date = 2013-04-01</span></span>  
10. <span data-ttu-id="dced2-139">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="dced2-140">[割引前キャッシュ フロー] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-140">In the Undiscounted cash flow field, enter a number.</span></span>
    * <span data-ttu-id="dced2-141">2500000.00 を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-141">Enter 2500000.00.</span></span>  
12. <span data-ttu-id="dced2-142">[回収可能金額] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-142">In the Recoverable amount field, enter a number.</span></span>
    * <span data-ttu-id="dced2-143">入力 = 2000000.00。</span><span class="sxs-lookup"><span data-stu-id="dced2-143">Enter = 2000000.00.</span></span>  
13. <span data-ttu-id="dced2-144">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="dced2-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dced2-145">固定資産番号「TOOLM-000008」を持つ行を選択します。</span><span class="sxs-lookup"><span data-stu-id="dced2-145">Select the row with Fixed asset number 'TOOLM-000008.'</span></span>  
14. <span data-ttu-id="dced2-146">[日付の変更] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-146">In the Modify date field, enter a date.</span></span>
15. <span data-ttu-id="dced2-147">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-147">In the Description field, type a value.</span></span>
16. <span data-ttu-id="dced2-148">[割引前キャッシュ フロー] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-148">In the Undiscounted cash flow field, enter a number.</span></span>
    * <span data-ttu-id="dced2-149">2000000.00 を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-149">Enter 2000000.00.</span></span>  
17. <span data-ttu-id="dced2-150">[回収可能金額] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-150">In the Recoverable amount field, enter a number.</span></span>
    * <span data-ttu-id="dced2-151">1500000.00 を入力します。</span><span class="sxs-lookup"><span data-stu-id="dced2-151">Enter 1500000.00.</span></span>  
18. <span data-ttu-id="dced2-152">[インジケーターの更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dced2-152">Click Update indicator.</span></span>

