---
title: Dynamics 365 Talent - Core HR (2019 年 1 月 11 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38be1da69d8443fd76a81f439f000602ddb75bab
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010386"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-january-11-2019"></a><span data-ttu-id="83ec6-103">Dynamics 365 Talent: Core HR (2019 年 1 月 11 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="83ec6-103">What's new or changed in Dynamics 365 Talent: Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83ec6-104">**ビルド 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="83ec6-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="83ec6-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="83ec6-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="83ec6-106">変更</span><span class="sxs-lookup"><span data-stu-id="83ec6-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="83ec6-107">利用可能な残高を予測して休暇要求を検証</span><span class="sxs-lookup"><span data-stu-id="83ec6-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="83ec6-108">今回のリリースで行われた変更では、従業員が現在の残高から差し引くことがなく、将来の休暇期間を依頼できるようにします。</span><span class="sxs-lookup"><span data-stu-id="83ec6-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="83ec6-109">将来行われる要求に標準のワークフローが使用されます。</span><span class="sxs-lookup"><span data-stu-id="83ec6-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="83ec6-110">詳細については、[作業時間に基づいて休暇を見越計上する](leave-accrue-hours-worked.md) をお読みください。</span><span class="sxs-lookup"><span data-stu-id="83ec6-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="83ec6-111">ESS および人員で予測休暇残高を表示</span><span class="sxs-lookup"><span data-stu-id="83ec6-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="83ec6-112">このフィーチャーにより、HR、管理者、および従業員による将来の休暇期間の残高の表示が可能になります。</span><span class="sxs-lookup"><span data-stu-id="83ec6-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="83ec6-113">従業員は、**従業員セルフ サービス** ワークスペースで将来の残高を確認でき、HR は**人員**ワークスペースを使用して同じ情報にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="83ec6-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="83ec6-114">休暇の残高を変更するための通知</span><span class="sxs-lookup"><span data-stu-id="83ec6-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="83ec6-115">休暇の残高は、従業員の現在の残高を表示します。</span><span class="sxs-lookup"><span data-stu-id="83ec6-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="83ec6-116">将来の残高は、**従業員セルフ サービス**および**人員**ワークスペースで「現在の日付」を入力して予測残高を計算することで利用できます。</span><span class="sxs-lookup"><span data-stu-id="83ec6-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="83ec6-117">次のエリアの予測残高を表示するためのナビゲーションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="83ec6-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="83ec6-118">**従業員セルフ サービス** ワークスペース上の**休暇**カード。</span><span class="sxs-lookup"><span data-stu-id="83ec6-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="83ec6-119">**マネージャー セルフ サービス** ワークスペース上の**休暇および欠勤**カード。</span><span class="sxs-lookup"><span data-stu-id="83ec6-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="83ec6-120">**人員**ワークスペース上の**休暇および欠勤**ページ。</span><span class="sxs-lookup"><span data-stu-id="83ec6-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="83ec6-121">変動報酬プラン (現金プラン) の小数点以下の許可</span><span class="sxs-lookup"><span data-stu-id="83ec6-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="83ec6-122">変動現金報酬および計画は、金額に対する柔軟性が追加され、小数点以下の値が上書きされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="83ec6-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="83ec6-123">プラン保存後の変動報酬登録の日付変更の不可</span><span class="sxs-lookup"><span data-stu-id="83ec6-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="83ec6-124">この変更により、計画の保存後に計画終了日を更新 (延長または期限切れ) することができます。</span><span class="sxs-lookup"><span data-stu-id="83ec6-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="83ec6-125">開始日と終了日に関係なく、プランを有効化または無効化することはできます。</span><span class="sxs-lookup"><span data-stu-id="83ec6-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="83ec6-126">給与管理者セキュリティロールを割り当てられたときに利用可能な給与情報</span><span class="sxs-lookup"><span data-stu-id="83ec6-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="83ec6-127">要求プロセス中に給与管理者のロールが給与情報にアクセスできるように更新されました。</span><span class="sxs-lookup"><span data-stu-id="83ec6-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="83ec6-128">従業員セルフ サービス | タイルからの職位階層のドリルダウンで親ノードを取得できません</span><span class="sxs-lookup"><span data-stu-id="83ec6-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="83ec6-129">職位階層を新しいワークスペースに追加して組織構造内を移動するときに発生するエラーを解消するための変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="83ec6-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="83ec6-130">個人番号順序が使用されているときの新しい検証メッセージ</span><span class="sxs-lookup"><span data-stu-id="83ec6-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="83ec6-131">従業員を採用し、次の従業員番号が使用されているときの問題を明確にするために変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="83ec6-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="83ec6-132">初期起動ページとして選択された従業員セルフ サービス ワークスペース</span><span class="sxs-lookup"><span data-stu-id="83ec6-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="83ec6-133">**従業員セルフ サービス** ワークスペースがユーザーの初期起動ページとして選択されており、そのユーザーに従業員ロールが割り当てられていない場合、システムは既定のダッシュボードにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="83ec6-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="83ec6-134">退職理由コードが職位の割り当てレコードを更新</span><span class="sxs-lookup"><span data-stu-id="83ec6-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="83ec6-135">退職の理由コードは、従業員の退職および職位の終了に際して職位の割り当てを更新するようになりました。</span><span class="sxs-lookup"><span data-stu-id="83ec6-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
