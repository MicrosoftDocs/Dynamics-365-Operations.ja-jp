---
title: 仕入先からのカテゴリ要求
description: このトピックでは、仕入先が勘定の調達カテゴリを要求する方法について説明します。 また、調達エージェントが完了する承認プロセスについても説明します。
author: kamaybac
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1951f85f84c3b8b2d42f49d5f464d90d410ebfa2
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015954"
---
# <a name="category-requests-from-vendors"></a><span data-ttu-id="712c8-104">仕入先からのカテゴリ要求</span><span class="sxs-lookup"><span data-stu-id="712c8-104">Category requests from vendors</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="712c8-105">カテゴリ要求プロセスにより、仕入先は新しい調達カテゴリを勘定に関連付けるよう要求することができます。</span><span class="sxs-lookup"><span data-stu-id="712c8-105">The category request process lets vendors request that new procurement categories be associated with their account.</span></span> <span data-ttu-id="712c8-106">その後、それらの調達カテゴリを関連する調達プロセスで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="712c8-106">Those procurement categories can then be used by the related procurement and sourcing processes.</span></span> <span data-ttu-id="712c8-107">(詳細については、[調達カテゴリの概要](procurement-catalogs.md)を参照してください。)</span><span class="sxs-lookup"><span data-stu-id="712c8-107">(For more information, see [Procurement catalogs overview](procurement-catalogs.md).)</span></span>

<span data-ttu-id="712c8-108">カテゴリ要求は、**仕入先情報** ワークスペースの仕入先によって開始されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-108">Category requests are initiated by vendors in the **Vendor information** workspace.</span></span> <span data-ttu-id="712c8-109">その後、確認および承認のためにエージェンシーに提出されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-109">They are then submitted to your agency for review and approval.</span></span> <span data-ttu-id="712c8-110">承認されたカテゴリは、仕入先の勘定の調達カテゴリの一覧に追加されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-110">Approved categories are added to the list of procurement categories for the vendor's account.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="712c8-111">システムで機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="712c8-111">Turn on the feature in your system</span></span>

<span data-ttu-id="712c8-112">このトピックで説明する機能がシステムにまだ含されていない場合、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)に移動し、*仕入先コラボレーションを通して仕入先が調達カテゴリを適用するのを許可* 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="712c8-112">If your system doesn't already include the feature that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Allow vendors to apply for procurement categories through vendor collaboration* feature.</span></span>

<span data-ttu-id="712c8-113">この機能を有効にした後も、調達カテゴリを仕入先の勘定に手動で追加することができます。</span><span class="sxs-lookup"><span data-stu-id="712c8-113">After the feature is turned on, you can still manually add procurement categories to vendor accounts.</span></span> <span data-ttu-id="712c8-114">詳細については、[特定の調達カテゴリに対する仕入先の承認](tasks/approve-vendors-specific-procurement-categories.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="712c8-114">For information, see [Approve vendors for specific procurement categories](tasks/approve-vendors-specific-procurement-categories.md).</span></span>

## <a name="vendor-collaboration-requirements"></a><span data-ttu-id="712c8-115">仕入先コラボレーションの要件</span><span class="sxs-lookup"><span data-stu-id="712c8-115">Vendor collaboration requirements</span></span>

<span data-ttu-id="712c8-116">仕入先がカテゴリ要求を操作するには、仕入先コラボレーションに設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="712c8-116">Before a vendor can interact with category requests, it must be set up for vendor collaboration.</span></span>

<span data-ttu-id="712c8-117">仕入先には、少なくとも 1 人の仕入先コラボレーション ユーザーが必要です。</span><span class="sxs-lookup"><span data-stu-id="712c8-117">The vendor must have at least one vendor collaboration user.</span></span> <span data-ttu-id="712c8-118">カテゴリ要求を作成および送信できるのは、*仕入先管理者 (外部)* セキュリティ ロールを持つ仕入先ユーザーのみです。</span><span class="sxs-lookup"><span data-stu-id="712c8-118">Only vendor users with the *Vendor admin (external)* security role can create and submit category requests.</span></span>

<span data-ttu-id="712c8-119">詳細については、「[仕入先コラボレーションの設定と管理](set-up-maintain-vendor-collaboration.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="712c8-119">For more information, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span>

## <a name="set-up-the-vendor-category-request-workflow"></a><span data-ttu-id="712c8-120">仕入先カテゴリ要求ワークフローの設定</span><span class="sxs-lookup"><span data-stu-id="712c8-120">Set up the Vendor category request workflow</span></span>

<span data-ttu-id="712c8-121">*仕入先カテゴリ要求* ワークフローは、調達ワークフローで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="712c8-121">The *Vendor category request* workflow must be set up in the procurement and sourcing workflows.</span></span> <span data-ttu-id="712c8-122">仕入先は、確認および承認ができる新しいカテゴリ要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="712c8-122">Vendors will submit new category requests that you can review and approve.</span></span> <span data-ttu-id="712c8-123">要求された調達カテゴリは、カテゴリ要求が承認された後で、仕入先の勘定に追加されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-123">Requested procurement categories are added to a vendor account after a category request is approved.</span></span>

<span data-ttu-id="712c8-124">次の例は、1 人の承認者を持つ簡単な *仕入先カテゴリ要求* ワークフローを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="712c8-124">The following example shows how to set up a simple *Vendor category request* workflow that has a single approver.</span></span> <span data-ttu-id="712c8-125">内部プロセスを確認し、エージェンシーに適切なワークフロー設定を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="712c8-125">You must review your internal processes to determine the appropriate workflow setup for your agency.</span></span>

1. <span data-ttu-id="712c8-126">**調達 \> セットアップ \> 調達ワークフロー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="712c8-126">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing workflows**.</span></span>
1. <span data-ttu-id="712c8-127">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="712c8-128">ダイアログ ボックスで、**仕入先カテゴリ要求ワークフロー** を選択してワークフロー エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="712c8-128">In the dialog box, select **Vendor category request workflow** to open the workflow editor.</span></span>
1. <span data-ttu-id="712c8-129">ワークフロー エディターにサインインします。</span><span class="sxs-lookup"><span data-stu-id="712c8-129">Sign in to the workflow editor.</span></span>
1. <span data-ttu-id="712c8-130">アクション ウィンドウで、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-130">On the Action Pane, select **Properties**.</span></span>
1. <span data-ttu-id="712c8-131">ワークフローの **プロパティ** ページの **送信指示** フィールドに指示のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-131">On the **Properties** page for the workflow, in the **Submission instructions** field, enter instruction text.</span></span> <span data-ttu-id="712c8-132">カテゴリ要求を送信するとき、仕入先に指示が表示されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-132">The instructions will be visible to vendors when they submit a category request.</span></span>
1. <span data-ttu-id="712c8-133">**プロパティ** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="712c8-133">Close the **Properties** page.</span></span>
1. <span data-ttu-id="712c8-134">**新しいカテゴリ要求を承認** ワークフロー要素をキャンバスの上にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="712c8-134">Drag the **Approve new category request** workflow element onto the canvas.</span></span>
1. <span data-ttu-id="712c8-135">**開始** ワークフロー要素から **新しいカテゴリ要求の承認** ワークフロー要素へのリンクをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="712c8-135">Drag a link from the **Start** workflow element to the **Approve new category request** workflow element.</span></span>
1. <span data-ttu-id="712c8-136">**新しいカテゴリ要求の承認** ワークフロー要素から **終了** ワークフロー要素へのリンクをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="712c8-136">Drag a link from the **Approve new category request** workflow element to the **End** workflow element.</span></span>
1. <span data-ttu-id="712c8-137">**新しいカテゴリ要求の承認** ワークフロー要素をダブルタップ (またはダブルクリック) します。</span><span class="sxs-lookup"><span data-stu-id="712c8-137">Double-tap (or double-click) the **Approve new category request** workflow element.</span></span>
1. <span data-ttu-id="712c8-138">**手順 1** ワークフロー要素を選択したまま (または右クリック) にしてから、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-138">Select and hold (or right-click) the **Step 1** workflow element, and then select **Properties**.</span></span>
1. <span data-ttu-id="712c8-139">ワークフロー要素の **プロパティ** ページの **作業項目の件名** フィールドに件名のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-139">On the **Properties** page for the workflow element, in the **Work item subject** field, enter subject text.</span></span> <span data-ttu-id="712c8-140">このテキストは、**自分自身に割り当てられた作業項目** ページの **件名** フィールドの値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-140">This text will be shown as the value of the **Subject** field on the **Work items assigned to me** page.</span></span>
1. <span data-ttu-id="712c8-141">**作業項目の指示** フィールドで、指示のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-141">In the **Work item instructions** field, enter instruction text.</span></span> <span data-ttu-id="712c8-142">指示は、カテゴリ要求のアクション ウィンドウで **ワークフロー** を選択したときに、承認者に対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-142">The instructions will be visible to approvers when they select **Workflow** on the Action Pane of a category request.</span></span>
1. <span data-ttu-id="712c8-143">左側のウィンドウで、**割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-143">In the left pane, select **Assignment**.</span></span>
1. <span data-ttu-id="712c8-144">**割り当てタイプ** タブで、**このワークフロー要素にユーザーを割り当てる** を *ユーザー* に設定します。</span><span class="sxs-lookup"><span data-stu-id="712c8-144">On the **Assignment type** tab, set **Assign users to this workflow element** to *User*.</span></span>
1. <span data-ttu-id="712c8-145">**ユーザー** タブの **利用可能なユーザー** の一覧で承認者を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-145">On the **User** tab, in the **Available users** list, select an approver.</span></span> <span data-ttu-id="712c8-146">たとえば、調達部門のユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-146">For example, select a user in the Procurement department.</span></span>
1. <span data-ttu-id="712c8-147">右矢印ボタン (**\>**) を選択して、承認者を **選択したユーザー** の一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="712c8-147">Select the right arrow button (**\>**) to move the approver to the **Selected users** list.</span></span>
1. <span data-ttu-id="712c8-148">**プロパティ** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="712c8-148">Close the **Properties** page.</span></span>
1. <span data-ttu-id="712c8-149">**保存して終了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-149">Select **Save and close**.</span></span>
1. <span data-ttu-id="712c8-150">**バージョンのメモ** フィールドで、ワークフローに関するメモを入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-150">In the **Version notes** field, enter notes about the workflow.</span></span>
1. <span data-ttu-id="712c8-151">**OK** を選択して、ワークフローを保存します。</span><span class="sxs-lookup"><span data-stu-id="712c8-151">Select **OK** to save the workflow.</span></span>
1. <span data-ttu-id="712c8-152">ワークフローのテストを開始する準備ができたとき、**新しいバージョンの有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-152">If you're ready to start to test the workflow, select **Activate the new version**.</span></span> <span data-ttu-id="712c8-153">それ以外の場合は、**新しいバージョンを有効にしない** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-153">Otherwise, select **Do not activate the new version**.</span></span>
1. <span data-ttu-id="712c8-154">**OK** を選択して、ワークフローの設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="712c8-154">Select **OK** to complete the workflow setup.</span></span>

> [!TIP]
> <span data-ttu-id="712c8-155">エージェンシーがカテゴリ要求の承認を必要としない場合、自動承認のワークフローを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="712c8-155">If your agency doesn't require approval of category requests, you should configure the workflow for automatic approval.</span></span>

<span data-ttu-id="712c8-156">ワークフローの設定方法に関する詳細については、[ワークフロー システムの概要](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="712c8-156">For more information about how to set up workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).</span></span>

## <a name="create-and-submit-a-category-request"></a><span data-ttu-id="712c8-157">カテゴリ要求の作成と送信</span><span class="sxs-lookup"><span data-stu-id="712c8-157">Create and submit a category request</span></span>

<span data-ttu-id="712c8-158">このセクションでは、仕入先が **仕入先情報** ワークスペースを使用してカテゴリ要求の作成、編集、表示、および送信を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="712c8-158">This section describes how vendors can use the **Vendor information** workspace to create, edit, view, and submit category requests.</span></span>

### <a name="start-a-new-request"></a><span data-ttu-id="712c8-159">新しい要求を開始する</span><span class="sxs-lookup"><span data-stu-id="712c8-159">Start a new request</span></span>

<span data-ttu-id="712c8-160">新しいカテゴリ要求を開始するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-160">To start a new category request, follow these steps.</span></span>

1. <span data-ttu-id="712c8-161">**仕入先情報** ワークスペースで、**カテゴリ要求** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-161">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="712c8-162">**カテゴリ要求** ページのアクション ウィンドウで、**新しい要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-162">On the **Category requests** page, on the Action Pane, select **New category request**.</span></span>
1. <span data-ttu-id="712c8-163">**新しいカテゴリ要求** ダイアログ ボックスで、ツリーを移動させるかリスト上部にあるフィルターを使用して、適用するカテゴリを検索します。</span><span class="sxs-lookup"><span data-stu-id="712c8-163">In the **New category request** dialog box, find the category that you want to apply for by navigating the tree and/or using the filter at the top of the list.</span></span> <span data-ttu-id="712c8-164">各関連カテゴリのチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="712c8-164">Select the checkbox for each relevant category.</span></span>

    <span data-ttu-id="712c8-165">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="712c8-165">Note the following points:</span></span>

    - <span data-ttu-id="712c8-166">仕入先の勘定で現在有効なカテゴリが選択済みとして表示され、削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="712c8-166">Categories that are currently active on your vendor account are shown as selected and can't be removed.</span></span>
    - <span data-ttu-id="712c8-167">1 つのカテゴリ要求で複数の調達カテゴリを要求することができます。</span><span class="sxs-lookup"><span data-stu-id="712c8-167">You can request multiple procurement categories in a single category request.</span></span>

1. <span data-ttu-id="712c8-168">**OK** を選択して、要求の下書きを作成します。</span><span class="sxs-lookup"><span data-stu-id="712c8-168">Select **OK** to create the draft request.</span></span>

    <span data-ttu-id="712c8-169">新しい要求の下書きが **カテゴリ要求** ページに表示されました。</span><span class="sxs-lookup"><span data-stu-id="712c8-169">The new draft request now appears on the **Category requests** page.</span></span>

1. <span data-ttu-id="712c8-170">新しい要求の下書きを開き、必要に応じて確認および編集をします。</span><span class="sxs-lookup"><span data-stu-id="712c8-170">Open the new draft request to review and edit it as required.</span></span>

    - <span data-ttu-id="712c8-171">現在、要求に含まれているカテゴリの一覧を表示するには、**要求されたカテゴリ** クイックタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-171">To view the list of categories that are currently included in the request, select the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="712c8-172">有効なカテゴリを表示するには、ページの右側にある **有効なカテゴリ** の情報ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="712c8-172">To view your active categories, open the **Active categories** FactBox on the right side of the page.</span></span>
    - <span data-ttu-id="712c8-173">要求にカテゴリを追加するには、**要求されたカテゴリ** クイックタブでツールバーの **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-173">To add a category to the request, select **Add** on the toolbar on the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="712c8-174">要求からカテゴリを削除するには、**要求されたカテゴリ** クイックタブでカテゴリを選択し、ツールバーの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-174">To remove a category from the request, select the category on the **Requested categories** FastTab, and then select **Remove** on the toolbar.</span></span>
    - <span data-ttu-id="712c8-175">要求にドキュメントを添付するには、アクション ウィンドウで **添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-175">To attach a document to the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="712c8-176">添付されたドキュメントは、承認者がカテゴリ要求を確認するときに使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="712c8-176">Attached documents will be available to approvers when they review the category request.</span></span>
    - <span data-ttu-id="712c8-177">要求から添付されたドキュメントを削除するには、アクション ウィンドウで **添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-177">To remove an attached document from the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="712c8-178">削除するドキュメントを選択し、アクション ウィンドウの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-178">Select the document to remove, and then select **Delete** on the Action Pane.</span></span>

1. <span data-ttu-id="712c8-179">要求を送信する準備ができたとき、アクション ウィンドウで **送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-179">If you're ready to submit the request, select **Submit** on the Action Pane.</span></span> <span data-ttu-id="712c8-180">それ以外の場合、ページを閉じて、この手順の残りのステップをスキップします。</span><span class="sxs-lookup"><span data-stu-id="712c8-180">Otherwise, just close the page and skip the remaining steps of this procedure.</span></span> <span data-ttu-id="712c8-181">後で要求に戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="712c8-181">You can then return to the request later.</span></span>
1. <span data-ttu-id="712c8-182">表示された送信指示を読み、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-182">Read any submission instructions that appear, and then select **Submit**.</span></span>
1. <span data-ttu-id="712c8-183">**コメント** ボックスに、必要な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-183">In the **Comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="712c8-184">**送信** を選択して、要求を完了します。</span><span class="sxs-lookup"><span data-stu-id="712c8-184">Then select **Submit** to complete the request.</span></span>

### <a name="edit-a-draft-or-recalled-request"></a><span data-ttu-id="712c8-185">下書きまたは取り消された要求の編集</span><span class="sxs-lookup"><span data-stu-id="712c8-185">Edit a draft or recalled request</span></span>

<span data-ttu-id="712c8-186">下書きまたは取り消されたカテゴリ要求を編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-186">To edit a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="712c8-187">**仕入先情報** ワークスペースで、**カテゴリ要求** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-187">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="712c8-188">下書きまたは取り消された要求を選択し、開きます。</span><span class="sxs-lookup"><span data-stu-id="712c8-188">Select the draft or recalled request to open it.</span></span>
1. <span data-ttu-id="712c8-189">必要に応じて要求を編集し、閉じるかまたは前の手順の説明に従って送信します。</span><span class="sxs-lookup"><span data-stu-id="712c8-189">Edit the request as required, and then either close it or submit it as described in the previous procedure.</span></span>

### <a name="submit-a-draft-or-recalled-request"></a><span data-ttu-id="712c8-190">下書きまたは取り消された要求の送信</span><span class="sxs-lookup"><span data-stu-id="712c8-190">Submit a draft or recalled request</span></span>

<span data-ttu-id="712c8-191">下書きまたは取り消されたカテゴリ要求を送信するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-191">To submit a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="712c8-192">**仕入先情報** ワークスペースで、**カテゴリ要求** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-192">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="712c8-193">送信する下書きまたは取り消された要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-193">Select the draft or recalled request that you want to submit.</span></span>
1. <span data-ttu-id="712c8-194">アクション ウィンドウで、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-194">On the Action Pane, select **Submit**.</span></span>
1. <span data-ttu-id="712c8-195">表示された送信指示を読み、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-195">Read any submission instructions that appear, and then select **Submit**.</span></span>
1. <span data-ttu-id="712c8-196">**コメント** ボックスに、必要な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-196">In the **Comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="712c8-197">**送信** を選択して、要求を完了します。</span><span class="sxs-lookup"><span data-stu-id="712c8-197">Then select **Submit** to complete the request.</span></span>

    <span data-ttu-id="712c8-198">カテゴリ要求の状態が、次の値のいずれかに変更されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-198">The status of the category request is changed to one of the following values:</span></span>

    - <span data-ttu-id="712c8-199">_確認待ち_ – 要求はワークフローにあります。</span><span class="sxs-lookup"><span data-stu-id="712c8-199">_Pending review_ – The request is in the workflow.</span></span>
    - <span data-ttu-id="712c8-200">_保留中の承認_ – 承認が必要です。</span><span class="sxs-lookup"><span data-stu-id="712c8-200">_Pending approval_ – Approval is required.</span></span>

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a><span data-ttu-id="712c8-201">まだ承認されていない送信済の要求の取り消し</span><span class="sxs-lookup"><span data-stu-id="712c8-201">Recall a submitted request that hasn't yet been approved</span></span>

<span data-ttu-id="712c8-202">送信済でまだ承認されていないカテゴリ要求を取り消するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-202">To recall a category request that has been submitted but hasn't yet been approved, follow these steps.</span></span>

1. <span data-ttu-id="712c8-203">**仕入先情報** ワークスペースで、**カテゴリ要求** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-203">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="712c8-204">取り消す保留中の要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-204">Select the pending request that you want to recall.</span></span>
1. <span data-ttu-id="712c8-205">アクション ウィンドウで、**取り消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-205">On the Action Pane, select **Recall**.</span></span>
1. <span data-ttu-id="712c8-206">**コメントの入力** ボックスに、必要な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-206">In the **Enter a comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="712c8-207">**送信** を選択して、要求を完了します。</span><span class="sxs-lookup"><span data-stu-id="712c8-207">Then select **Submit** to complete the request.</span></span>

    <span data-ttu-id="712c8-208">カテゴリ要求の状態が _取消済_ に変更されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-208">The status of the category request is changed to _Canceled_.</span></span> <span data-ttu-id="712c8-209">要求は、削除または再送信するまでこのステータスに保持されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-209">The request will remain in this status until you delete or resubmit it.</span></span>

### <a name="delete-a-draft-or-recalled-request"></a><span data-ttu-id="712c8-210">下書きまたは取り消された要求の削除</span><span class="sxs-lookup"><span data-stu-id="712c8-210">Delete a draft or recalled request</span></span>

<span data-ttu-id="712c8-211">下書きまたは取り消されたカテゴリ要求を削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-211">To delete a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="712c8-212">**仕入先情報** ワークスペースで、**カテゴリ要求** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-212">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="712c8-213">削除する下書きまたは取り消された要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-213">Select the draft or recalled request that you want to delete.</span></span>
1. <span data-ttu-id="712c8-214">アクション ウィンドウで **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-214">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="712c8-215">**はい** を選択して削除を確認します。</span><span class="sxs-lookup"><span data-stu-id="712c8-215">Select **Yes** to confirm the deletion.</span></span>

### <a name="view-completed-requests"></a><span data-ttu-id="712c8-216">完了した要求の表示</span><span class="sxs-lookup"><span data-stu-id="712c8-216">View completed requests</span></span>

<span data-ttu-id="712c8-217">完了した要求を表示するには、**仕入先情報** ワークスペースを開き、**カテゴリ要求** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-217">To view completed requests, open the **Vendor information** workspace and select the **Category requests** tile.</span></span> <span data-ttu-id="712c8-218">完了したカテゴリ要求には、次のいずれかのステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="712c8-218">Category requests that have been completed will have one of the following statuses:</span></span>

- <span data-ttu-id="712c8-219">_承認済_ – 要求は承認されました。</span><span class="sxs-lookup"><span data-stu-id="712c8-219">_Approved_ – The request was approved.</span></span> <span data-ttu-id="712c8-220">新しく追加したカテゴリを表示するには、**仕入先情報** ワークスペースに戻り、左側のウィンドウの **詳細** ドロップダウン リストを開き、**カテゴリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-220">To view the newly added categories, go back to the **Vendor information** workspace, open the **More details** drop-down list in the left pane, and then select **Categories**.</span></span>
- <span data-ttu-id="712c8-221">_拒否済_ – 要求は拒否されました。</span><span class="sxs-lookup"><span data-stu-id="712c8-221">_Rejected_ – The request was rejected.</span></span> <span data-ttu-id="712c8-222">必要に応じて、新しいカテゴリ要求を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="712c8-222">You can create a new category request as required.</span></span>

## <a name="review-category-requests"></a><span data-ttu-id="712c8-223">カテゴリ要求の確認</span><span class="sxs-lookup"><span data-stu-id="712c8-223">Review category requests</span></span>

<span data-ttu-id="712c8-224">このセクションでは、仕入先が送信したカテゴリ要求を承認、拒否、および委任する方法、および完了した要求を表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="712c8-224">This section explains how to approve, reject, and delegate category requests that vendors submitted, and how to view completed requests.</span></span> <span data-ttu-id="712c8-225">これらのワークフロー アクションは、カテゴリ要求全体に対して行われます。</span><span class="sxs-lookup"><span data-stu-id="712c8-225">These workflow actions are for the whole category request.</span></span>

### <a name="view-category-requests"></a><span data-ttu-id="712c8-226">カテゴリ要求の表示</span><span class="sxs-lookup"><span data-stu-id="712c8-226">View category requests</span></span>

<span data-ttu-id="712c8-227">カテゴリ要求を表示するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-227">To view category requests, follow these steps.</span></span>

1. <span data-ttu-id="712c8-228">**調達 \> 仕入先 \> 仕入先のコラボレーション要求 \> カテゴリ要求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="712c8-228">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>

    <span data-ttu-id="712c8-229">**カテゴリ要求** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-229">The **Category requests** page appears.</span></span> <span data-ttu-id="712c8-230">既定のページ ビューには、ステータスが *保留中のアクション* であるカテゴリ要求が表示されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-230">The default page view shows category requests that have a status of *Pending action*.</span></span>

1. <span data-ttu-id="712c8-231">すべての要求を表示するには、**要求の表示** フィールドで *すべて* を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-231">To view all requests, select *All* in the **Show requests** field.</span></span>
1. <span data-ttu-id="712c8-232">要求を開き、必要に応じて確認および編集をします。</span><span class="sxs-lookup"><span data-stu-id="712c8-232">Open a request to review and edit it as required.</span></span>

    - <span data-ttu-id="712c8-233">現在、要求に含まれているカテゴリの一覧を表示するには、**要求されたカテゴリ** クイックタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-233">To view the list of categories that are currently included in the request, select the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="712c8-234">有効なカテゴリを表示するには、ページの右側にある **有効なカテゴリ** の情報ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="712c8-234">To view the active categories, open the **Active categories** FactBox on the right side of the page.</span></span>
    - <span data-ttu-id="712c8-235">ドキュメントが送信された場合、アクション ウィンドウの **添付ファイル** (紙クリップ) ボタンに、添付されたドキュメントの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-235">If documents were submitted, the  **Attachments** (paper clip) button on the Action Pane shows a count of the attached documents.</span></span> <span data-ttu-id="712c8-236">添付されたドキュメントを表示するには、**添付ファイル** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-236">To view attached documents, select the **Attachments** button.</span></span> <span data-ttu-id="712c8-237">表示するドキュメントを選択し、**開く** を選択して表示します。</span><span class="sxs-lookup"><span data-stu-id="712c8-237">Then select the document to view and select **Open** to view it.</span></span>
    - <span data-ttu-id="712c8-238">要求にドキュメントを添付するには、アクション ウィンドウで **添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-238">To attach a document to the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="712c8-239">添付されたドキュメントは、承認者がカテゴリ要求を確認するときに使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="712c8-239">Attached documents will be available to approvers when they review the category request.</span></span>
    - <span data-ttu-id="712c8-240">要求から添付されたドキュメントを削除するには、アクション ウィンドウで **添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-240">To remove an attached document from the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="712c8-241">削除するドキュメントを選択し、アクション ウィンドウの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-241">Select the document to remove, and then select **Delete** on the Action Pane.</span></span>
    - <span data-ttu-id="712c8-242">ワークフロー履歴を表示するには、アクション ウィンドウで **ワークフロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-242">To view the workflow history, select **Workflow** on the Action Pane.</span></span> <span data-ttu-id="712c8-243">ワークフロー オプションで、**詳細** を選択し、**ワークフロー履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-243">In the workflow options, select **More** and then **Workflow history**.</span></span> <span data-ttu-id="712c8-244">**ワークフロー履歴** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-244">The **Workflow history** page appears.</span></span>

### <a name="approve-a-pending-category-request"></a><span data-ttu-id="712c8-245">保留中のカテゴリ要求の承認</span><span class="sxs-lookup"><span data-stu-id="712c8-245">Approve a pending category request</span></span>

<span data-ttu-id="712c8-246">保留中のカテゴリ要求を承認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-246">To approve a pending category request, follow these steps.</span></span>

1. <span data-ttu-id="712c8-247">**調達 \> 仕入先 \> 仕入先のコラボレーション要求 \> カテゴリ要求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="712c8-247">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="712c8-248">承認する保留中の要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-248">Select the pending request to approve.</span></span>
1. <span data-ttu-id="712c8-249">カテゴリ要求を確認します。</span><span class="sxs-lookup"><span data-stu-id="712c8-249">Review the category request.</span></span>
1. <span data-ttu-id="712c8-250">オプション: **一般** クイックタブの **理由コード** フィールドで、理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-250">Optional: On the **General** FastTab, in the **Reason code** field, select a reason code.</span></span> <span data-ttu-id="712c8-251">次に、**理由コメント** フィールドに理由コードに関するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-251">Then, in the **Reason comment** field, enter a comment about the reason code.</span></span>
1. <span data-ttu-id="712c8-252">アクション ウィンドウで、**ワークフロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-252">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="712c8-253">ワークフロー オプションで、**承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-253">In the workflow options, select **Approve**.</span></span>
1. <span data-ttu-id="712c8-254">**コメント** フィールドに、必要な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-254">In the **Comment** field, enter any additional information that is required.</span></span> <span data-ttu-id="712c8-255">**承認** を選択して、要求を完了します。</span><span class="sxs-lookup"><span data-stu-id="712c8-255">Then select **Approve** to complete the request.</span></span>

    <span data-ttu-id="712c8-256">カテゴリ要求のステータスが _承認済_ に変更され、調達カテゴリが仕入先の勘定に追加されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-256">The status of the category request is changed to _Approved_, and the procurement categories are added to the vendor account.</span></span>

### <a name="reject-a-pending-category-request"></a><span data-ttu-id="712c8-257">保留中のカテゴリ要求の拒否</span><span class="sxs-lookup"><span data-stu-id="712c8-257">Reject a pending category request</span></span>

<span data-ttu-id="712c8-258">保留中のカテゴリ要求を拒否するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-258">To reject a pending category request, follow these steps.</span></span>

1. <span data-ttu-id="712c8-259">**調達 \> 仕入先 \> 仕入先のコラボレーション要求 \> カテゴリ要求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="712c8-259">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="712c8-260">拒否する保留中の要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-260">Select the pending request to reject.</span></span>
1. <span data-ttu-id="712c8-261">カテゴリ要求を確認します。</span><span class="sxs-lookup"><span data-stu-id="712c8-261">Review the category request.</span></span>
1. <span data-ttu-id="712c8-262">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-262">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="712c8-263">**一般** クイックタブの **理由コード** フィールドで、理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-263">On the **General** FastTab, in the **Reason code** field, select a reason code.</span></span> <span data-ttu-id="712c8-264">次に、**理由コメント** フィールドに理由コードに関するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-264">Then, in the **Reason comment** field, enter a comment about the reason code.</span></span>
1. <span data-ttu-id="712c8-265">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-265">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="712c8-266">アクション ウィンドウで、**ワークフロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-266">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="712c8-267">ワークフロー オプションで、**詳細** を選択し、**拒否** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-267">In the workflow options, select **More** and then **Reject**.</span></span>
1. <span data-ttu-id="712c8-268">**コメント** フィールドに、必要な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-268">In the **Comment** field, enter any additional information that is required.</span></span> <span data-ttu-id="712c8-269">**拒否** を選択して、要求を完了します。</span><span class="sxs-lookup"><span data-stu-id="712c8-269">Then select **Reject** to complete the request.</span></span>

    <span data-ttu-id="712c8-270">カテゴリ要求の状態が _拒否済_ に変更されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-270">The status of the category request is changed to _Rejected_.</span></span> <span data-ttu-id="712c8-271">この時点で、仕入先は必要に応じて新しいカテゴリ要求を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="712c8-271">At this point, the vendor can create a new category request as required.</span></span>

### <a name="delegate-a-pending-category-request"></a><span data-ttu-id="712c8-272">保留中のカテゴリ要求の委任</span><span class="sxs-lookup"><span data-stu-id="712c8-272">Delegate a pending category request</span></span>

<span data-ttu-id="712c8-273">保留中のカテゴリ要求を別のユーザーに委任するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-273">To delegate a pending category request to another user, follow these steps.</span></span>

1. <span data-ttu-id="712c8-274">**調達 \> 仕入先 \> 仕入先のコラボレーション要求 \> カテゴリ要求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="712c8-274">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="712c8-275">承認する保留中の要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-275">Select the pending request that you want to approve.</span></span>
1. <span data-ttu-id="712c8-276">アクション ウィンドウで、**ワークフロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-276">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="712c8-277">ワークフロー オプションで、**詳細** を選択し、**委任** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-277">In the workflow options, select **More** and then **Delegate**.</span></span>
1. <span data-ttu-id="712c8-278">**ユーザー** フィールドで、カテゴリ要求の確認を割り当てるユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-278">In the **User** field, select the user to assign the category request to for review.</span></span>
1. <span data-ttu-id="712c8-279">**コメント** フィールドに、必要な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="712c8-279">In the **Comment** field, enter any additional information that is required.</span></span>
1. <span data-ttu-id="712c8-280">**委任** を選択して、委任を完了します。</span><span class="sxs-lookup"><span data-stu-id="712c8-280">Select **Delegate** to complete the delegation.</span></span> <span data-ttu-id="712c8-281">選択したユーザーはカテゴリ要求を確認できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="712c8-281">The selected user can now review the category request.</span></span>

### <a name="view-procurement-categories-for-a-vendor"></a><span data-ttu-id="712c8-282">仕入先の調達カテゴリの表示</span><span class="sxs-lookup"><span data-stu-id="712c8-282">View procurement categories for a vendor</span></span>

<span data-ttu-id="712c8-283">カテゴリ要求が承認された後で仕入先の調達カテゴリを表示するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="712c8-283">To view procurement categories for a vendor after a category request is approved, follow these steps.</span></span>

1. <span data-ttu-id="712c8-284">**調達 \> 仕入先 \> すべての仕入先** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="712c8-284">Go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="712c8-285">**すべての仕入先** ページで、調達カテゴリを表示する仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-285">On the **All vendors** page, select the vendor that you want to view procurement categories for.</span></span>
1. <span data-ttu-id="712c8-286">アクション ウィンドウで、**一般** タブを開き、**設定** グループから、**カテゴリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="712c8-286">On the Action Pane, open the **General** tab and, from the **Set up** group, select **Categories**.</span></span>

    <span data-ttu-id="712c8-287">**カテゴリ** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-287">The **Categories** page appears.</span></span> <span data-ttu-id="712c8-288">**調達** クイックタブに、カテゴリ要求を通じて追加された調達カテゴリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="712c8-288">The **Procurement** FastTab shows procurement categories that were added through the category request.</span></span>

1. <span data-ttu-id="712c8-289">**調達** クイックタブで、必要に応じて変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="712c8-289">On the **Procurement** FastTab, you can make changes if needed.</span></span> <span data-ttu-id="712c8-290">たとえば、**仕入先カテゴリ ステータス** フィールドを _優先_ に設定できます。</span><span class="sxs-lookup"><span data-stu-id="712c8-290">For example, you can set the **Vendor category status** field to _Preferred_.</span></span>
