---
title: 元伝票の監査ポリシーの定義
description: このトピックでは、監査ポリシー ルールを設定および実行する方法について説明します。
author: panolte
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 545ed1ee9faea8aac9a39e5812e815c85e2dd9a8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240789"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="9ea6a-103">元伝票の監査ポリシーの定義</span><span class="sxs-lookup"><span data-stu-id="9ea6a-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ea6a-104">このトピックでは、監査ポリシー ルールを設定および実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="9ea6a-105">この例では、ホテル経費タイプの経費精算書を使用しています。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="9ea6a-106">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="9ea6a-107">監査担当者ロールには、これらのタスクを実行する適切なアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="9ea6a-108">ナビゲーション ウィンドウで、**モジュール > 監査ワークベンチ > 設定 > ポリシー ルール タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="9ea6a-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-109">Select **New**.</span></span>
3. <span data-ttu-id="9ea6a-110">**ルール名** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="9ea6a-111">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9ea6a-112">**クエリ名** フィールドで **経費精算書の明細行** を選択する</span><span class="sxs-lookup"><span data-stu-id="9ea6a-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="9ea6a-113">**クエリ タイプ** フィールドで、**集計** を選択する</span><span class="sxs-lookup"><span data-stu-id="9ea6a-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="9ea6a-114">**法人** フィールドで **法人** を選択する</span><span class="sxs-lookup"><span data-stu-id="9ea6a-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="9ea6a-115">**文書日付の参照** フィールドで、**変更日時** を選択する</span><span class="sxs-lookup"><span data-stu-id="9ea6a-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="9ea6a-116">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-116">Select **Save**.</span></span>
10. <span data-ttu-id="9ea6a-117">ナビゲーション ウィンドウで、**モジュール > 監査ワークベンチ > 設定 > 監査ポリシー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="9ea6a-118">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-118">Select **New**.</span></span>
12. <span data-ttu-id="9ea6a-119">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="9ea6a-120">**ポリシーの組織** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="9ea6a-121">ツリーで、**Contoso Entertainment System USA** を選択してから、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="9ea6a-122">ツリーで、**Contoso Consulting USA** を選択してから、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="9ea6a-123">ツリーで、**Contoso Retail USA** を選択してから、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="9ea6a-124">**ポリシーの組織** セクションを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="9ea6a-125">**ポリシー ルール** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="9ea6a-126">一覧で、以前に作成したポリシー ルールを見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="9ea6a-127">**ポリシー ルールの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="9ea6a-128">**有効日** フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="9ea6a-129">**フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-129">Select **Filter**.</span></span>
23. <span data-ttu-id="9ea6a-130">一覧で、**経費カテゴリ** の行を選択し、詳細を **ホテル** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="9ea6a-131">**基準** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="9ea6a-132">**集計** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="9ea6a-133">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-133">Select **Add**.</span></span>
27. <span data-ttu-id="9ea6a-134">一覧で、**トランザクション金額** の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="9ea6a-135">**フィールド** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="9ea6a-136">**集計関数** フィールドで、**合計** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="9ea6a-137">**グループ化** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="9ea6a-138">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-138">Select **Add**.</span></span>
32. <span data-ttu-id="9ea6a-139">一覧で、**従業員** の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="9ea6a-140">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-140">Select **Add**.</span></span>
34. <span data-ttu-id="9ea6a-141">一覧で、**経費カテゴリ** の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="9ea6a-142">**フィールド** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="9ea6a-143">**HAVING** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="9ea6a-144">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-144">Select **Add**.</span></span>
38. <span data-ttu-id="9ea6a-145">**トランザクション金額** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="9ea6a-146">**フィールド** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="9ea6a-147">**集計関数** フィールドで、**合計** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="9ea6a-148">**基準** フィールドで、`>2000` と入力します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="9ea6a-149">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-149">Select **OK**.</span></span>
43. <span data-ttu-id="9ea6a-150">**テスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-150">Select **Test**.</span></span>
44. <span data-ttu-id="9ea6a-151">**ドキュメントの選択の開始日** フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="9ea6a-152">**ドキュメントの選択の終了日** フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="9ea6a-153">**テストの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-153">Select **Run test**.</span></span>
47. <span data-ttu-id="9ea6a-154">アクション ウィンドウで、**監査ポリシー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="9ea6a-155">**追加オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="9ea6a-156">**開始日** フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="9ea6a-157">**終了日** フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="9ea6a-158">**バッチ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-158">Select **Batch**.</span></span>
52. <span data-ttu-id="9ea6a-159">**バックグラウンドで実行** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="9ea6a-160">**バッチ処理** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="9ea6a-161">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-161">Select **OK**.</span></span>
55. <span data-ttu-id="9ea6a-162">ナビゲーション ウィンドウで、**モジュール > 監査ワークベンチ > 設定 > 監査ケース** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="9ea6a-163">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="9ea6a-164">**関連** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="9ea6a-165">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea6a-165">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]