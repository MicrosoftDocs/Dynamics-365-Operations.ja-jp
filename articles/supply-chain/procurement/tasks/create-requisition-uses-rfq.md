---
title: RFQ を使用する要求の作成
description: このトピックでは、価格および仕入先情報を RFQ プロセスから購買要求へ追加する方法について説明します。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e67dafd02a3b2a38832d8a4f0e9809adffcbb80
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211841"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="c37e5-103">RFQ を使用する要求の作成</span><span class="sxs-lookup"><span data-stu-id="c37e5-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c37e5-104">このトピックでは、価格および仕入先情報を RFQ プロセスから購買要求へ追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="c37e5-105">このガイドで表示される例は USMF のデモ データ会社で使用でき、すべての手順を完了するためには管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c37e5-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="c37e5-106">このガイドのタスクは、調達担当者によって通常実行されます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="c37e5-107">要求の作成</span><span class="sxs-lookup"><span data-stu-id="c37e5-107">Create a requisition</span></span>
1. <span data-ttu-id="c37e5-108">ナビゲーション ウィンドウで、**モジュール > 調達 > 購買要求 > 自分自身が作成した購買要求** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="c37e5-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-109">Select **New**.</span></span>
3. <span data-ttu-id="c37e5-110">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="c37e5-111">**要求日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="c37e5-112">**会計日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="c37e5-113">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-113">Select **OK**.</span></span>
7. <span data-ttu-id="c37e5-114">**理由** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="c37e5-115">**明細行の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-115">Select **Add line**.</span></span>
9. <span data-ttu-id="c37e5-116">**調達カテゴリ** フィールドで、ツリーのカテゴリーを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="c37e5-117">**製品名** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="c37e5-118">**数量** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="c37e5-119">**単位** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="c37e5-120">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-120">Select **Save**.</span></span>
14. <span data-ttu-id="c37e5-121">**ワークフロー** を選択して、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="c37e5-122">**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-122">Select **Submit**.</span></span>
16. <span data-ttu-id="c37e5-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-123">Close the page.</span></span>
17. <span data-ttu-id="c37e5-124">**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="c37e5-125">ワークフロー タスクの再割り当て</span><span class="sxs-lookup"><span data-stu-id="c37e5-125">Reassign a workflow task</span></span>
<span data-ttu-id="c37e5-126">次のタスクは、RFQ を作成し、製品の仕入先から入札を取得します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="c37e5-127">USMF のデモ データでは、要求ワークフローとルールが共に設定されているため、仕入先が選択されていない場合、または単価が明細行に対して 0 の場合でも、RFQ を作成する特定の作業者にタスクが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="c37e5-128">このガイドで続行するには、別のユーザー (自分自身) にそのタスクを再度割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c37e5-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="c37e5-129">自分が管理者としてログインしている場合にのみこれを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="c37e5-130">**ワークフロー** を選択して、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="c37e5-131">**履歴の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-131">Select **View history**.</span></span>
3. <span data-ttu-id="c37e5-132">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-132">Refresh the page.</span></span>
4. <span data-ttu-id="c37e5-133">**追跡の詳細** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="c37e5-134">ツリーで、“行のワークフローが有効化された“ から始まる行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="c37e5-135">**ワークフローの詳細を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="c37e5-136">**作業項目** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="c37e5-137">**再割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="c37e5-138">**ユーザー** フィールドで、**管理者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="c37e5-139">**再割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="c37e5-140">2 つのページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="c37e5-141">RFQ の作成</span><span class="sxs-lookup"><span data-stu-id="c37e5-141">Create an RFQ</span></span>

1. <span data-ttu-id="c37e5-142">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-142">Refresh the page.</span></span>
2. <span data-ttu-id="c37e5-143">**見積依頼** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="c37e5-144">**購買組織** フィールドで、**USMF** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="c37e5-145">要求明細行と同じ法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c37e5-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="c37e5-146">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c37e5-146">In the list, mark the selected row.</span></span> <span data-ttu-id="c37e5-147">自分の購買要求に複数の明細行がある場合は、RFQ に追加するすべての明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="c37e5-148">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-148">Select **OK**.</span></span>
6. <span data-ttu-id="c37e5-149">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-149">Refresh the page.</span></span>
7. <span data-ttu-id="c37e5-150">情報ボックスが開いていることを確認し、**関連ドキュメント** のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="c37e5-151">**見積依頼** フィールドのリンクを選択し、先ほど作成した RFQ を開きます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="c37e5-152">**ヘッダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-152">Select **Header**.</span></span>
10. <span data-ttu-id="c37e5-153">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-153">Select **Add**.</span></span>
11. <span data-ttu-id="c37e5-154">**仕入先** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="c37e5-155">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-155">Select **Add**.</span></span>
13. <span data-ttu-id="c37e5-156">**仕入先** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="c37e5-157">**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-157">Select **Send**.</span></span>
15. <span data-ttu-id="c37e5-158">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-158">Select **OK**.</span></span>
16. <span data-ttu-id="c37e5-159">**回答の入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="c37e5-160">アクション ペインで、**返信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="c37e5-161">**データを返信にコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="c37e5-162">これにより、数量や日付などのデータが RFQ から返信へコピーされます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="c37e5-163">**単価** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="c37e5-164">これは、仕入先から受け取った価格です。</span><span class="sxs-lookup"><span data-stu-id="c37e5-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="c37e5-165">仕入先からの追加情報を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="c37e5-166">**受け入れる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-166">Select **Accept**.</span></span>
21. <span data-ttu-id="c37e5-167">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="c37e5-168">仕入先および価格が請求に転送されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="c37e5-169">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-169">Close the page.</span></span>
2. <span data-ttu-id="c37e5-170">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-170">Select **Lines**.</span></span>
3. <span data-ttu-id="c37e5-171">**関連情報** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-171">Select **Related information**.</span></span>
4. <span data-ttu-id="c37e5-172">**購買要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="c37e5-173">RFQ の移動明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="c37e5-174">価格および仕入先が要求書にコピーされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="c37e5-175">**ワークフロー** を選択して、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="c37e5-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="c37e5-176">[完了] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-176">Select Complete.</span></span>
8. <span data-ttu-id="c37e5-177">ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-177">Select the page.</span></span>
9. <span data-ttu-id="c37e5-178">[完了] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c37e5-178">Select Complete.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]