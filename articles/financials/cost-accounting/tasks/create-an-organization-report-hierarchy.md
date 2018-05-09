--- 
title: "組織レポート階層の作成"
description: "組織をレポートするためのレポート階層を作成するには、この手順を使用します。"
author: YuyuScheller
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69fccd6b59e25fe0f39c107c59c1682cc545ebd2
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="9ddc8-103">組織レポート階層の作成</span><span class="sxs-lookup"><span data-stu-id="9ddc8-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ddc8-104">組織をレポートするためのレポート階層を作成するには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="9ddc8-105">この記録は、組織全体のレポートの構造が作成されるまで続行できるように、分析コード階層を使って説明することを目的とします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="9ddc8-106">この記録では、USP2 デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="9ddc8-107">[原価会計] > [分析コード] > [分析コード階層] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="9ddc8-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-108">Click New.</span></span>
3. <span data-ttu-id="9ddc8-109">[HierarchyTypeComboBox] フィールドでは、「分析コード分類階層」を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="9ddc8-110">[分析コード分類階層] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="9ddc8-111">[分析コード分類階層] タイプはルールの定義、およびレポート用に使用します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="9ddc8-112">コスト オブジェクト、コスト要素、および統計分析コードなどのすべての分析コードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="9ddc8-113">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-113">Click Create.</span></span>
5. <span data-ttu-id="9ddc8-114">[分析コード階層名] フィールドで、「組織 USP2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="9ddc8-115">[分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="9ddc8-116">[コスト センター] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="9ddc8-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-117">Click Save.</span></span>
8. <span data-ttu-id="9ddc8-118">[階層の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="9ddc8-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-119">Click New.</span></span>
10. <span data-ttu-id="9ddc8-120">[ノード名] フィールドで、「CEO」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="9ddc8-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-121">Click Save.</span></span>
12. <span data-ttu-id="9ddc8-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-122">Click New.</span></span>
13. <span data-ttu-id="9ddc8-123">[ノード名] フィールドで、「CEO コスト センター」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="9ddc8-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-124">Click Save.</span></span>
15. <span data-ttu-id="9ddc8-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-125">Click New.</span></span>
16. <span data-ttu-id="9ddc8-126">[ノード名] フィールドで、「地域 East」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="9ddc8-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-127">Click Save.</span></span>
18. <span data-ttu-id="9ddc8-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-128">Click New.</span></span>
19. <span data-ttu-id="9ddc8-129">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="9ddc8-130">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9ddc8-131">ノードに対応する分析コード メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="9ddc8-132">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-132">Click Save.</span></span>
22. <span data-ttu-id="9ddc8-133">ツリーで、「組織 USP2\CEO\CEO コスト センター」を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="9ddc8-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-134">Click New.</span></span>
24. <span data-ttu-id="9ddc8-135">[ノード名] フィールドで、「地域 West」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="9ddc8-136">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-136">Click Save.</span></span>
26. <span data-ttu-id="9ddc8-137">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-137">Click New.</span></span>
27. <span data-ttu-id="9ddc8-138">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="9ddc8-139">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9ddc8-140">ノードに対応する分析コード メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="9ddc8-141">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-141">Click Save.</span></span>
30. <span data-ttu-id="9ddc8-142">ツリーで、「組織 USP2\CEO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="9ddc8-143">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-143">Click New.</span></span>
32. <span data-ttu-id="9ddc8-144">[ノード名] フィールドで、「CFO コスト センター」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="9ddc8-145">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-145">Click Save.</span></span>
34. <span data-ttu-id="9ddc8-146">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-146">Click New.</span></span>
35. <span data-ttu-id="9ddc8-147">[ノード名] フィールドで、「マーケティング キャンペーン」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="9ddc8-148">[ノード名] フィールドで、「マーケティング キャンペーン」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="9ddc8-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-149">Click Save.</span></span>
38. <span data-ttu-id="9ddc8-150">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-150">Click New.</span></span>
39. <span data-ttu-id="9ddc8-151">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="9ddc8-152">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9ddc8-153">ノードに対応する分析コード メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="9ddc8-154">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-154">Click Save.</span></span>
42. <span data-ttu-id="9ddc8-155">ツリーで、「組織 USP2\CEO\CFO コスト センター」を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="9ddc8-156">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-156">Click New.</span></span>
44. <span data-ttu-id="9ddc8-157">[ノード名] フィールドで、「取引の表示」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="9ddc8-158">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-158">Click Save.</span></span>
46. <span data-ttu-id="9ddc8-159">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-159">Click New.</span></span>
47. <span data-ttu-id="9ddc8-160">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="9ddc8-161">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9ddc8-162">ノードに対応する分析コード メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="9ddc8-163">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-163">Click Save.</span></span>
50. <span data-ttu-id="9ddc8-164">ツリーで、「組織 USP2\CEO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="9ddc8-165">[ノード名] フィールドで、「CIO コスト センター」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="9ddc8-166">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-166">Click Save.</span></span>
53. <span data-ttu-id="9ddc8-167">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-167">Click New.</span></span>
54. <span data-ttu-id="9ddc8-168">[ノード名] フィールドで、「コール センター」を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="9ddc8-169">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-169">Click Save.</span></span>
56. <span data-ttu-id="9ddc8-170">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-170">Click New.</span></span>
57. <span data-ttu-id="9ddc8-171">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="9ddc8-172">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9ddc8-173">ノードに対応する分析コード メンバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="9ddc8-174">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddc8-174">Click Save.</span></span>


