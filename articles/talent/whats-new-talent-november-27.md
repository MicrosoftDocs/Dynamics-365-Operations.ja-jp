---
title: "Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 11 月 27 日)"
description: "このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 48e2eea2cc986edc49d5192945c3d913c3bb9756
ms.openlocfilehash: 6bd049bfe4639136276ab2f14e6310e45d1254f2
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a><span data-ttu-id="6c656-103">Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 11 月 27 日)</span><span class="sxs-lookup"><span data-stu-id="6c656-103">What's new or changed in Dynamics 365 for Talent Core HR (November 27, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c656-104">**ビルド 8.1.2064**</span><span class="sxs-lookup"><span data-stu-id="6c656-104">**Build 8.1.2064**</span></span>

<span data-ttu-id="6c656-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c656-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="6c656-106">変更</span><span class="sxs-lookup"><span data-stu-id="6c656-106">Changes</span></span>

### <a name="unable-to-create-a-note-in-case-management"></a><span data-ttu-id="6c656-107">ケース管理にメモを作成できない</span><span class="sxs-lookup"><span data-stu-id="6c656-107">Unable to create a note in Case Management</span></span>

<span data-ttu-id="6c656-108">ケース管理のケース ログでメモを編集または作成しようとするときの問題のために、変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="6c656-108">A change has been made for an issue when attempting to edit or create a note in the case log of Case Management.</span></span>

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a><span data-ttu-id="6c656-109">報酬のワークスペースの分析タブでの誤った表記の単語</span><span class="sxs-lookup"><span data-stu-id="6c656-109">Misspelled word on the analytics tab in the compensation workspace</span></span> 

<span data-ttu-id="6c656-110">報酬ワークスペースの、報酬分析グラフの「Ethnic Origin」のスペルを修正するための変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="6c656-110">A change has been made to correct the spelling of 'Ethnic Origin' in the compensation analytics chart in the compensation workspace.</span></span>

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a><span data-ttu-id="6c656-111">従業員セルフ サービス ワークスペースは、ユーザーが作業者に割り当てられていないときには表示されない</span><span class="sxs-lookup"><span data-stu-id="6c656-111">Employee self-service workspace not displaying when a user isn't assigned to a worker</span></span> 

<span data-ttu-id="6c656-112">**従業員セルフ サービス** ワークスペースが、作業者に割り当てられていないユーザーの起動時の最初のページとして選択されているときに変更されました。</span><span class="sxs-lookup"><span data-stu-id="6c656-112">A change has been made when the **Employee self-service** workspace is selected as the initial page on startup for a user who is not assigned to a worker.</span></span> <span data-ttu-id="6c656-113">この状況では、既定のダッシュ ボードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c656-113">In this situation, the default dashboard will be displayed.</span></span>

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a><span data-ttu-id="6c656-114">休暇と欠勤エラー: オブジェクト参照がオブジェクトのインスタンスに設定されていない</span><span class="sxs-lookup"><span data-stu-id="6c656-114">Leave and Absence error: Object reference not set to an instance of an object</span></span>

<span data-ttu-id="6c656-115">**自分自身に割り当てられた作業項目**リストに休暇と欠勤の記録を承認した後、このエラーを修正するための休暇と欠勤への変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="6c656-115">Changes have been made to Leave and Absence to correct this error after approving leave and absence records in the **Work items assigned to me** list.</span></span>

### <a name="unable-to-recall-an-image-workflow"></a><span data-ttu-id="6c656-116">イメージのワークフローを取り消すことができない</span><span class="sxs-lookup"><span data-stu-id="6c656-116">Unable to recall an image workflow</span></span>

<span data-ttu-id="6c656-117">イメージのワークフローを取り消した後は、ワークフローは「キャンセル済」に設定され、従業員セルフ サービス ワークスペースの既存の要求を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="6c656-117">After recalling an image workflow, the workflow will be set to "cancelled" and the existing request can be deleted in the employee self-service workspace.</span></span>

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a><span data-ttu-id="6c656-118">退職後に何度も表示される再雇用された従業員や契約社員</span><span class="sxs-lookup"><span data-stu-id="6c656-118">Rehired employees or contractors show up multiple times after termination</span></span> 

<span data-ttu-id="6c656-119">この更新により、再雇用されて退職した従業員は退職リストに 1 回のみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c656-119">With this update, terminated employees that are rehired will only display one time in the exited list.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="6c656-120">既知の問題</span><span class="sxs-lookup"><span data-stu-id="6c656-120">Known issue</span></span>

- <span data-ttu-id="6c656-121">**問題**: 作業者に新しい添付ファイルを追加する時、**新規**および**編集**ボタンが灰色表示になります。</span><span class="sxs-lookup"><span data-stu-id="6c656-121">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="6c656-122">**回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c656-122">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="6c656-123">**作業者**ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="6c656-123">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="6c656-124">(この問題は次のプラットフォーム更新プログラムで修正されます。)</span><span class="sxs-lookup"><span data-stu-id="6c656-124">(This issue will be fixed in the next platform update.)</span></span>

