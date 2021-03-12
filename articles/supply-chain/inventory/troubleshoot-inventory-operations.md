---
title: 在庫操作のトラブルシューティング
description: このトピックでは、在庫操作で作業をする際に発生する可能性がある問題の修正方法について説明します。
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967158"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="5d574-103">在庫操作のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="5d574-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d574-104">このトピックでは、在庫操作で作業をする際に発生する可能性がある問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5d574-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="5d574-105">在庫仕訳帳の "ワークフロー" ドロップダウン ダイアログ ボックスが見つらない。</span><span class="sxs-lookup"><span data-stu-id="5d574-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d574-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="5d574-106">Issue description</span></span>

<span data-ttu-id="5d574-107">仕訳帳ページには **ワークフロー** ドロップダウン ダイアログ ボックスが表示されないか、関連するワークフロー操作を選択できません。</span><span class="sxs-lookup"><span data-stu-id="5d574-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="5d574-108">この問題は、次のサブセクションで説明するように、3 つの理由で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="5d574-109">問題の解決 1</span><span class="sxs-lookup"><span data-stu-id="5d574-109">Issue resolution 1</span></span>

<span data-ttu-id="5d574-110">すべてのユーザーに問題が適用される場合は、承認ワークフローが仕訳帳名に割り当てられていないため、問題が発生している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="5d574-111">問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5d574-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="5d574-112">**在庫管理 &gt; 設定 &gt; 仕訳帳名 &gt; 在庫** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d574-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="5d574-113">リスト ペイン列から仕訳帳名を選択して、設定ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="5d574-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="5d574-114">**一般** クイック タブで、**承認ワークフロー** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="5d574-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="5d574-115">変更の確認を求められたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d574-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="5d574-116">**ワークフロー** フィールドで、選択した仕訳帳名にに使用するワークフローを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d574-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="5d574-117">問題の解決 2</span><span class="sxs-lookup"><span data-stu-id="5d574-117">Issue resolution 2</span></span>

<span data-ttu-id="5d574-118">ワークフローでカスタマイズされたコードを使用している場合、システムをアップグレードすると問題が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="5d574-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="5d574-119">たとえば、仕訳帳ワークフローで **送信** ボタンはグレー表示され、送信を承認するために選択できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="5d574-120">**送信** ボタンがグレー表示されている場合、ワークフローはカスタマイズされている場合があります (つまり、ワークフローの方法。`FormDataUtil` の `canSubmitToWorkflow()` は拡張されています)。</span><span class="sxs-lookup"><span data-stu-id="5d574-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="5d574-121">この問題を修正するには、次の例で構造を使用する `canSubmitToWorkflow()` の方法を拡張する方法を変更します。</span><span class="sxs-lookup"><span data-stu-id="5d574-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="5d574-122">問題の解決 3</span><span class="sxs-lookup"><span data-stu-id="5d574-122">Issue resolution 3</span></span>

<span data-ttu-id="5d574-123">特定のユーザーにのみ問題が適用される場合、そのユーザーには、在庫仕訳帳に対するワークフロー操作の実行に必要なセキュリティ特権が付与されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="5d574-124">影響を受ける各ユーザーに *在庫仕訳帳ワークフロー の維持* のセキュリティ特権が付与されているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5d574-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="5d574-125">既定では、この特権は同じ名前の関税に割り当てされ、その関税は *倉庫作業者* と *倉庫マネージャ* のロールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="5d574-126">在庫仕訳帳の状態がシステム ロック状態のままで、ワークフロー バッチ ジョブが機能しない。</span><span class="sxs-lookup"><span data-stu-id="5d574-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d574-127">問題の説明</span><span class="sxs-lookup"><span data-stu-id="5d574-127">Issue description</span></span>

<span data-ttu-id="5d574-128">使用している在庫仕訳帳の 1 つが、ある操作によってロックされ、変更後はリリースされません。</span><span class="sxs-lookup"><span data-stu-id="5d574-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="5d574-129">たとえば、転記中に不明なエラーが発生した場合 (システム ロック操作)、仕訳帳はシステム ロック状態のままです。</span><span class="sxs-lookup"><span data-stu-id="5d574-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="5d574-130">この場合、ワークフロー作業項目ハンドラーは検証をロックしている間にエラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="5d574-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5d574-131">問題の解決</span><span class="sxs-lookup"><span data-stu-id="5d574-131">Issue resolution</span></span>

<span data-ttu-id="5d574-132">Supply Chain Management の SQL Server インスタンスにログインし、**InventJournalTable.SystemBlocked** が *1* に設定されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5d574-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="5d574-133">その場合は、仕訳帳がロックの状態ではない事を確認してから、**InventJournalTable.SystemBlocked** を *0* にリセットしてください。</span><span class="sxs-lookup"><span data-stu-id="5d574-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="5d574-134">自分の在庫仕訳帳ワークフローは完了したことがなく、仕訳帳を編集したり転記したりできません。</span><span class="sxs-lookup"><span data-stu-id="5d574-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d574-135">問題の説明</span><span class="sxs-lookup"><span data-stu-id="5d574-135">Issue description</span></span>

<span data-ttu-id="5d574-136">仕訳帳承認ワークフローを送信すると、ワークフロー処理の応答が停止され、仕訳帳を編集または処理できます。</span><span class="sxs-lookup"><span data-stu-id="5d574-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5d574-137">問題の解決</span><span class="sxs-lookup"><span data-stu-id="5d574-137">Issue resolution</span></span>

<span data-ttu-id="5d574-138">ワークフロー処理が完了しないのはいくつかの理由があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="5d574-139">次の問題を確認してください。</span><span class="sxs-lookup"><span data-stu-id="5d574-139">Check for the following issues:</span></span>

- <span data-ttu-id="5d574-140">**在庫管理 &gt; 設定 &gt; 在庫管理ワークフロー** に移動し、影響を受けるワークフローの構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="5d574-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="5d574-141">詳細については、[仕訳帳承認ワークフロー](inventory-journal-workflow.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d574-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="5d574-142">ワークフローに例外またはエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="5d574-143">影響を受けるワークフローの作業項目履歴を確認して、ワークフローを終了する申請エラーが含まれるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5d574-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="5d574-144">在庫仕訳帳は、承認されている場合にのみ更新または編集できます。</span><span class="sxs-lookup"><span data-stu-id="5d574-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="5d574-145">リコールが有効な場合は、仕訳帳を取り消してみてください。</span><span class="sxs-lookup"><span data-stu-id="5d574-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="5d574-146">ワークフロー バッチ ジョブの実行が複数の理由で中断される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="5d574-147">このような理由の一部は、ワークフロー フレームワークの問題が原因である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="5d574-148">在庫仕訳帳ワークフロー条件は、行レベルではなく仕訳帳レベルでのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d574-149">問題の説明</span><span class="sxs-lookup"><span data-stu-id="5d574-149">Issue description</span></span>

<span data-ttu-id="5d574-150">たとえば、原価金額に対して在庫仕訳帳のワークフロー条件を設定しようとする場合に、この問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="5d574-151">この条件を設定して、原価金額が 100 未満の場合にのみ手順 1 が実行されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="5d574-152">その後他の条件を設定して、原価金額が 100 以上の場合にのみ手順 2 が実行されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="5d574-153">その後、ワークフローを実行するとワークフロー履歴に表示される行は 1 行のみです。送信された値に関係なく、常に最初の条件が *真* として評価されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="5d574-154">問題の回避策</span><span class="sxs-lookup"><span data-stu-id="5d574-154">Issue workaround</span></span>

<span data-ttu-id="5d574-155">現在のリリースでは、在庫ワークフロー条件は、行レベルではなく仕訳帳レベルでのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="5d574-156">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="5d574-156">This behavior is by design.</span></span> <span data-ttu-id="5d574-157">条件基準は、仕訳帳レベルの属性に対してだけ設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5d574-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="5d574-158">手持在庫リスト ページのフィルター ペインでは、期待した通りの結果のフィルタ処理は行されません。</span><span class="sxs-lookup"><span data-stu-id="5d574-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d574-159">問題の説明</span><span class="sxs-lookup"><span data-stu-id="5d574-159">Issue description</span></span>

<span data-ttu-id="5d574-160">**手持在庫リスト**  ページのフィルター ペインにあるフィルタ―では、期待した通りの結果のフィルタ処理は行されません。</span><span class="sxs-lookup"><span data-stu-id="5d574-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5d574-161">問題の解決</span><span class="sxs-lookup"><span data-stu-id="5d574-161">Issue resolution</span></span>

<span data-ttu-id="5d574-162">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="5d574-162">This behavior is by design.</span></span>

<span data-ttu-id="5d574-163"> *\*手持在庫リスト**  ページは、使用可能なすべての分析コードを含む詳細な手持在庫テーブルから構成されています。</span><span class="sxs-lookup"><span data-stu-id="5d574-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="5d574-164">ただし、このページの一覧には概要情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="5d574-165">そのため、表示される分析コードに応じて値を集計することで、ソース テーブルからの行を結合することができます。</span><span class="sxs-lookup"><span data-stu-id="5d574-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="5d574-166">フィルターペインで設定したフィルターは、集計リストではなく、ソース テーブルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="5d574-167">[これらの例](inventory-on-hand-list.md#examples) で示すように、この動作によって予期しない結果が生成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="5d574-168">ただし、 [グリッドで指定されているフィルタ](inventory-on-hand-list.md#grid-filters) は集計リストに適用され  *ません* 。</span><span class="sxs-lookup"><span data-stu-id="5d574-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="5d574-169">これらのフィルターには、グリッドの上部にクイック フィルターが含まれており、各列のヘッダーに対してフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="5d574-170">在庫仕訳帳で単位数量と単位数量が正しく機能しない。</span><span class="sxs-lookup"><span data-stu-id="5d574-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d574-171">問題の説明</span><span class="sxs-lookup"><span data-stu-id="5d574-171">Issue description</span></span>

<span data-ttu-id="5d574-172">在庫仕訳帳の単位と数量を使用すると、次のいずれかの問題が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="5d574-173">リリースされた製品に換算単位が設定されている間は、在庫仕訳帳に単位数量または単位数量は表示されません。また、在庫仕訳帳で単位を変更したりは変更できます。</span><span class="sxs-lookup"><span data-stu-id="5d574-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="5d574-174">在庫仕訳帳には **数量** フィールドと **単位** フィールドが表示されますが、**単位数量** フィールド は表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="5d574-175">単位を変更して数量を入力して仕訳帳を転記すると、仕訳帳には引き続きその数量の元の測定単位が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5d574-176">問題の解決</span><span class="sxs-lookup"><span data-stu-id="5d574-176">Issue resolution</span></span>

<span data-ttu-id="5d574-177">この問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5d574-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="5d574-178">**機能管理** ワークスペースで、*在庫仕訳帳の測定単位と単位数量の使用* 機能が有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5d574-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="5d574-179">この機能により、**単位** と **単位数量** フィールドが仕訳帳に追加されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="5d574-180">機能が有効になった後は、次の方法で **数量**、**単位数量**、**単位** フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d574-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="5d574-181">**数量** - リリースされた製品に対して定義されている既定の単位を使用して数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d574-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="5d574-182">ただし、既定の単位自体は、ここには表示されません。</span><span class="sxs-lookup"><span data-stu-id="5d574-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="5d574-183">既定の単位と **単位** フィールドで選択した単位の間に換算が設定されている場合、**数量** フィールドは、**単位数量** フィールドと **単位** フィールドでの選択内容に基づいて自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="5d574-184">**単位数量** – **単位** フィールドで選択された単位を使った数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d574-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="5d574-185">**単位** - **単位数量** フィールドの値に適用する単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d574-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="5d574-186">"最小在庫管理単位の最大小数点以下桁数は 0 です" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d574-187">問題の説明</span><span class="sxs-lookup"><span data-stu-id="5d574-187">Issue description</span></span>

<span data-ttu-id="5d574-188">在庫トランザクションや在庫予約を転記しようとする場合、"最小在庫管理単位の最大小数点以下の桁数は 0 です" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5d574-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="5d574-189">この問題は、在庫トランザクションの数量が、フィールドでサポートされる精度レベルを下回る小数の値として指定されている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="5d574-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="5d574-190">たとえば、在庫トランザクションに対して数量 *0.5* が指定されている一方で、サポートされているのは整数数量のみです。</span><span class="sxs-lookup"><span data-stu-id="5d574-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="5d574-191">したがって、値は *0.5* の代わりに *1* にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d574-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5d574-192">問題の解決</span><span class="sxs-lookup"><span data-stu-id="5d574-192">Issue resolution</span></span>

1. <span data-ttu-id="5d574-193">在庫トランザクションの数量を丸めるには、SQL Server インスタンスで次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="5d574-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="5d574-194">このスクリプトは **inventTrans** テーブルの値を修正します。</span><span class="sxs-lookup"><span data-stu-id="5d574-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="5d574-195">**修正エラー** オプションが有効になっているという一貫性の確認を実行します。</span><span class="sxs-lookup"><span data-stu-id="5d574-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="5d574-196">このチェックは、**inventSum** テーブルの値を修正します。</span><span class="sxs-lookup"><span data-stu-id="5d574-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d574-197">実稼働環境でスクリプトを実行する前に、必要に応じてスクリプトを入念に編集し、テスト環境でテストしてから、結果のデータを確認することを強く推奨します。</span><span class="sxs-lookup"><span data-stu-id="5d574-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>
