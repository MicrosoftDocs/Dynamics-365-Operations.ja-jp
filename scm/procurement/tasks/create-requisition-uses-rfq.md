--- 
title: "RFQ を使用する要求の作成"
description: "このガイドでは、価格および仕入先情報を RFQ プロセスから購買要求へ追加する方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d97ccd15031b2f7398486eee4a716ecef5e9dafd
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="a639e-103">RFQ を使用する要求の作成</span><span class="sxs-lookup"><span data-stu-id="a639e-103">Create a requisition that uses an RFQ</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a639e-104">このガイドでは、価格および仕入先情報を RFQ プロセスから購買要求へ追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a639e-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="a639e-105">このガイドで表示される例は USMF のデモ データ会社で使用でき、すべての手順を完了するためには管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a639e-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="a639e-106">このガイドのタスクは、調達担当者によって通常実行されます。</span><span class="sxs-lookup"><span data-stu-id="a639e-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="a639e-107">要求の作成</span><span class="sxs-lookup"><span data-stu-id="a639e-107">Create a requisition</span></span>
1. <span data-ttu-id="a639e-108">[調達] > [購買要求] > [自分自身が作成した購買要求] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a639e-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="a639e-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-109">Click New.</span></span>
3. <span data-ttu-id="a639e-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a639e-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a639e-111">[要求日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a639e-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="a639e-112">[会計日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a639e-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="a639e-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-113">Click OK.</span></span>
7. <span data-ttu-id="a639e-114">[理由] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a639e-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="a639e-115">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-115">Click Add line.</span></span>
9. <span data-ttu-id="a639e-116">[調達カテゴリー] フィールドで、ツリーのカテゴリーを選択し、[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="a639e-117">[製品名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a639e-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="a639e-118">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a639e-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="a639e-119">[単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a639e-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="a639e-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-120">Click Save.</span></span>
14. <span data-ttu-id="a639e-121">[ワークフロー] をクリックすると、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a639e-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="a639e-122">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-122">Click Submit.</span></span>
16. <span data-ttu-id="a639e-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a639e-123">Close the page.</span></span>
17. <span data-ttu-id="a639e-124">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="a639e-125">ワークフロー タスクの再割り当て</span><span class="sxs-lookup"><span data-stu-id="a639e-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="a639e-126">次のタスクは、RFQ を作成し、製品の仕入先から入札を取得します。</span><span class="sxs-lookup"><span data-stu-id="a639e-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="a639e-127">USMF のデモ データでは、要求ワークフローとルールが共に設定されているため、仕入先が選択されていない場合、または単価が明細行に対して 0 の場合でも、RFQ を作成する特定の作業者にタスクが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="a639e-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="a639e-128">このガイドで続行するには、別のユーザー (自分自身) にそのタスクを再度割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a639e-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="a639e-129">自分が管理者としてログインしている場合にのみこれを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a639e-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="a639e-130">[ワークフロー] をクリックすると、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a639e-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="a639e-131">[履歴の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-131">Click View history.</span></span>
3. <span data-ttu-id="a639e-132">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="a639e-132">Refresh the page.</span></span>
4. <span data-ttu-id="a639e-133">[追跡の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a639e-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="a639e-134">ツリーで、「『行ワークフローが有効化された』から始まる行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a639e-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="a639e-135">[ワークフローの詳細の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-135">Click View workflow details.</span></span>
7. <span data-ttu-id="a639e-136">作業項目セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a639e-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="a639e-137">[再割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-137">Click Reassign.</span></span>
9. <span data-ttu-id="a639e-138">[ユーザー] フィールドで、[管理者] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a639e-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="a639e-139">[再割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-139">Click Reassign.</span></span>
11. <span data-ttu-id="a639e-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a639e-140">Close the page.</span></span>
12. <span data-ttu-id="a639e-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a639e-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="a639e-142">RFQ の作成</span><span class="sxs-lookup"><span data-stu-id="a639e-142">Create an RFQ</span></span>
1. <span data-ttu-id="a639e-143">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="a639e-143">Refresh the page.</span></span>
2. <span data-ttu-id="a639e-144">[見積依頼] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="a639e-145">[購買組織] フィールドで、「USMF」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a639e-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="a639e-146">要求明細行で同じ法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a639e-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="a639e-147">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="a639e-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a639e-148">自分の購買要求に複数の明細行がある場合は、RFQ に追加するすべての明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="a639e-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="a639e-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-149">Click OK.</span></span>
6. <span data-ttu-id="a639e-150">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="a639e-150">Refresh the page.</span></span>
7. <span data-ttu-id="a639e-151">情報ボックスを開き、関連ドキュメントのセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a639e-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="a639e-152">既に情報ボックスが開いている場合があります。</span><span class="sxs-lookup"><span data-stu-id="a639e-152">You may already have the FactBox open.</span></span> <span data-ttu-id="a639e-153">[行/ヘッダー] 切り替えボタンの右側にある矢印がついたアイコンを探します。</span><span class="sxs-lookup"><span data-stu-id="a639e-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="a639e-154">矢印が右を指している場合は、情報ボックスが既に開いています。</span><span class="sxs-lookup"><span data-stu-id="a639e-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="a639e-155">矢印が左を指している場合は、矢印をクリックし情報ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="a639e-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="a639e-156">[見積依頼] フィールドのリンクをクリックし、先ほど作成した RFQ を開きます。</span><span class="sxs-lookup"><span data-stu-id="a639e-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="a639e-157">[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-157">Click Header.</span></span>
10. <span data-ttu-id="a639e-158">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-158">Click Add.</span></span>
11. <span data-ttu-id="a639e-159">[仕入先] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a639e-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="a639e-160">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-160">Click Add.</span></span>
13. <span data-ttu-id="a639e-161">[仕入先] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a639e-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="a639e-162">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-162">Click Send.</span></span>
15. <span data-ttu-id="a639e-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-163">Click OK.</span></span>
16. <span data-ttu-id="a639e-164">[入力] をクリックして回答します。</span><span class="sxs-lookup"><span data-stu-id="a639e-164">Click Enter reply.</span></span>
17. <span data-ttu-id="a639e-165">[アクション ペイン] で、[返信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="a639e-166">[データのコピー] をクリックして返信します。</span><span class="sxs-lookup"><span data-stu-id="a639e-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="a639e-167">これにより、数量や日付などのデータが RFQ から返信へコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a639e-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="a639e-168">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a639e-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="a639e-169">これは、仕入先から受け取った価格です。</span><span class="sxs-lookup"><span data-stu-id="a639e-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="a639e-170">仕入先からの追加情報を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="a639e-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="a639e-171">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-171">Click Accept.</span></span>
21. <span data-ttu-id="a639e-172">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="a639e-173">仕入先および価格が請求に転送されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a639e-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="a639e-174">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a639e-174">Close the page.</span></span>
2. <span data-ttu-id="a639e-175">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-175">Click Lines.</span></span>
3. <span data-ttu-id="a639e-176">[関連情報] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-176">Click Related information.</span></span>
4. <span data-ttu-id="a639e-177">[購買要求] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="a639e-178">RFQ の移動明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="a639e-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="a639e-179">価格および仕入先が要求書にコピーされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a639e-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="a639e-180">[ワークフロー] をクリックすると、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a639e-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="a639e-181">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-181">Click Complete.</span></span>
8. <span data-ttu-id="a639e-182">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a639e-182">Close the page.</span></span>
9. <span data-ttu-id="a639e-183">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a639e-183">Click Complete.</span></span>

