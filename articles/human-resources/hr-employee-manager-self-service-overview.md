---
title: 従業員およびマネージャー セルフサービスの概要
description: この記事では、従業員およびマネージャ セルフサービス ワークスペースの概要を説明します。
author: andreabichsel
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1aadd17b35992af1e79750427fae62e9bd4ff7a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113238"
---
# <a name="employee-and-manager-self-service-overview"></a><span data-ttu-id="764ac-103">従業員およびマネージャー セルフサービスの概要</span><span class="sxs-lookup"><span data-stu-id="764ac-103">Employee and Manager self service overview</span></span>

<span data-ttu-id="764ac-104">この記事では、従業員およびマネージャ セルフサービス ワークスペースの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="764ac-104">This article provides an overview of the employee and manager self service workspace.</span></span>

## <a name="edit-personal-details"></a><span data-ttu-id="764ac-105">個人的な詳細情報の編集</span><span class="sxs-lookup"><span data-stu-id="764ac-105">Edit personal details</span></span>

<span data-ttu-id="764ac-106">個人情報を追加または変更する必要がある場合は、[個人情報の編集](hr-employee-manager-self-service-edit-personal-information.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="764ac-106">If you need to add or change any personal information, see [Edit personal information](hr-employee-manager-self-service-edit-personal-information.md).</span></span>

## <a name="user-not-assigned-to-a-worker-record"></a><span data-ttu-id="764ac-107">従業員レコードに割り当てられていないユーザー</span><span class="sxs-lookup"><span data-stu-id="764ac-107">User not assigned to a worker record</span></span>

<span data-ttu-id="764ac-108">ユーザーを **ユーザー** ページの **作業者** レコードにリンクしていない場合は、次のメッセージが表示されます :</span><span class="sxs-lookup"><span data-stu-id="764ac-108">If you haven't linked your user to a **Worker** record in the **Users** page, the following message will display:</span></span>

<span data-ttu-id="764ac-109">**ユーザー ID がシステム内の従業員レコードに関連付けられていません。この関連付けがされるまでは、情報の表示や更新をすることはできません。マネージャーまたはサポート チームにお問い合わせください。**</span><span class="sxs-lookup"><span data-stu-id="764ac-109">**Your user ID is not associated with your employee record in the system. You won't be able to view or update your information until it is. Contact your manager or support team for assistance.**</span></span>

<span data-ttu-id="764ac-110">ユーザーを **作業者** レコードに関連付けるには、**ユーザー** に移動し、ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="764ac-110">To associate a user with a **Worker** record, navigate to **Users** and select the user.</span></span> <span data-ttu-id="764ac-111">**編集** を選択し、フォームの **個人** フィールドに適切な作業者を追加し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="764ac-111">Select **Edit**, add the corresponding worker in the **Person** field on the form, and the select **Save**.</span></span> <span data-ttu-id="764ac-112">これで、従業員セルフ サービスにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="764ac-112">You should now have access to Employee self service.</span></span>

## <a name="security-requirements-for-employee-and-manager-self-service"></a><span data-ttu-id="764ac-113">従業員およびマネージャー セルフサービスのセキュリティ要件</span><span class="sxs-lookup"><span data-stu-id="764ac-113">Security requirements for Employee and Manager self service</span></span>

<span data-ttu-id="764ac-114">従業員およびマネージャー セルフサービスには二つのセキュリティ ロールが必要となります :</span><span class="sxs-lookup"><span data-stu-id="764ac-114">Employee and Manager self service require two security roles:</span></span>

- <span data-ttu-id="764ac-115">従業員には従業員ロールを必要となります。</span><span class="sxs-lookup"><span data-stu-id="764ac-115">Employees require the Employee role.</span></span>
- <span data-ttu-id="764ac-116">管理職には、従業員とマネージャーの両方のロールが必要となります。</span><span class="sxs-lookup"><span data-stu-id="764ac-116">Managers require both the Employee and Manager roles.</span></span>

>[!NOTE]
><span data-ttu-id="764ac-117">従業員およびマネージャーのワークスペースへのアクセスが許可されている場合は、カスタムロールを使用して従業員およびマネージャー セルフサービスにアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-117">You can also use custom roles to access Employee and Manager self service as long as they've been granted access to Employee and Manager workspaces.</span></span><br>
><span data-ttu-id="764ac-118">従業員情報へのマネージャーのアクセスは、Human Resources で定義されている現在の職位ラインの階層に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="764ac-118">Manager access to employee information is based on the current position line hierarchy defined in Human Resources.</span></span>

## <a name="employee-self-service"></a><span data-ttu-id="764ac-119">従業員セルフ サービス</span><span class="sxs-lookup"><span data-stu-id="764ac-119">Employee self service</span></span>

<span data-ttu-id="764ac-120">**個人情報** タブには、従業員セルフサービスに関する次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-120">The **My information** tab displays the following information for Employee self service.</span></span>  

### <a name="summary"></a><span data-ttu-id="764ac-121">集計</span><span class="sxs-lookup"><span data-stu-id="764ac-121">Summary</span></span>

<span data-ttu-id="764ac-122">**自分に割り当てられた作業** には、従業員に割り当てられているすべての承認とワークフロー項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-122">**Work items assigned to me** displays all approvals and workflow items that are assigned to the employee.</span></span> <span data-ttu-id="764ac-123">ユーザーにメールを送信するワークフロー項目をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-123">You can configure workflow items to send emails to the user.</span></span>

<span data-ttu-id="764ac-124">**自分に割り当てられたアンケート** には、従業員またはグループに直接割り当てられているすべてのスケジュール済アンケートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-124">**Questionnaires assigned to me** display all scheduled questionnaires assigned directly to the employee or group.</span></span>

<span data-ttu-id="764ac-125">**会社ディレクトリ** では、従業員が組織内の個人に関連する情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-125">**Company directory** lets employees look up information related to individuals in the organization.</span></span> <span data-ttu-id="764ac-126">公開連絡先情報はすべての従業員が利用できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-126">Public contact information is available to all employees.</span></span> <span data-ttu-id="764ac-127">会社ディレクトリは、従業員がログインした会社に制限されています。</span><span class="sxs-lookup"><span data-stu-id="764ac-127">The company directory is restricted to the company that the employee has signed into.</span></span>

<span data-ttu-id="764ac-128">**チーム カレンダー** には、チームのカレンダー情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-128">**Team calendar** shows your team's calendar information.</span></span> <span data-ttu-id="764ac-129">詳細については、[チームおよび会社カレンダーの表示](hr-employee-self-service-calendar.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="764ac-129">For more information, see [View team and company calendars](hr-employee-self-service-calendar.md).</span></span>

### <a name="my-career-information"></a><span data-ttu-id="764ac-130">自分のキャリア情報</span><span class="sxs-lookup"><span data-stu-id="764ac-130">My career information</span></span>

<span data-ttu-id="764ac-131">従業員セルフサービスの **自分の経歴情報** セクションには、休暇と欠勤、パフォーマンス管理、コンピテンシー、福利厚生、作業、および添付ファイルに関連するカードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="764ac-131">The **My career information** section of Employee self-service contains cards related to Leave and Absence, Performance Management, Competencies, Benefits, Tasks, and Attachments.</span></span>

<span data-ttu-id="764ac-132">**休暇残高** カードは、登録された計画の残高を表示します。</span><span class="sxs-lookup"><span data-stu-id="764ac-132">The **Time Off Balances** card displays the balances for any enrolled plans.</span></span> <span data-ttu-id="764ac-133">このカードでは、見越計上方法に基づいて残高を予測します。</span><span class="sxs-lookup"><span data-stu-id="764ac-133">This card forecasts your balance based on your accrual method.</span></span> <span data-ttu-id="764ac-134">休暇リクエストを入力および送信して、承認ワークフロー プロセスを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-134">You can enter and submit time-off requests, which will then go through an approval workflow process.</span></span> <span data-ttu-id="764ac-135">休暇と欠勤の管理の詳細については、[休暇と欠勤の概要](hr-leave-and-absence-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="764ac-135">For more information about Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

<span data-ttu-id="764ac-136">**タスク** カードでは、割り当てられているタスクを表示したり、タスクを表示および管理できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-136">The **Tasks** card displays tasks that are assigned to you and lets you view and manage them.</span></span>

<span data-ttu-id="764ac-137">**次の登録済コース** カードには、登録した次のコースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-137">The **Next Registered Course** card displays the next course you're registered for.</span></span> <span data-ttu-id="764ac-138">すべてのオープン コースは表示および登録できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-138">You can view and register for any open courses.</span></span> <span data-ttu-id="764ac-139">サインアップのために開いているすべてのコースは、**開始済** のステータスとなっており、このカードで従業員は自動登録できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-139">All courses that are open for sign-up have a status of **Started**, and allow employees to self-register appear on this card.</span></span> <span data-ttu-id="764ac-140">組織の設定に応じて、コース登録には承認プロセスが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="764ac-140">Depending on your organization's settings, your course registration might go through an approval process.</span></span>

<span data-ttu-id="764ac-141">**証明書** カードには、現在の日付から一番最初に期限が切れる証明書の有効期限と証明書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-141">The **Certificates** card displays the certificate and expiration date of the certificate expiring closest to the current date.</span></span> <span data-ttu-id="764ac-142">証明書の更新、追加、または削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-142">You can update, add, or remove certificates.</span></span> <span data-ttu-id="764ac-143">組織の設定に応じて、証明書の更新には承認プロセスが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="764ac-143">Depending on your organization's settings, certificate updates might go through an approval process.</span></span>

<span data-ttu-id="764ac-144">**次にスケジュールされたレビュー** カードでは、次のパフォーマンス レビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-144">The **Next Scheduled Review** card displays your next performance review.</span></span> <span data-ttu-id="764ac-145">新しいレビューは、このカードから開始できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-145">You can start a new review from this card.</span></span> <span data-ttu-id="764ac-146">管理者または人事担当者は、レビューを開始することもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-146">Your manager or HR representative can also initiate reviews.</span></span> <span data-ttu-id="764ac-147">組織の設定によっては、このカードから終了レビューを表示、更新、または送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-147">Depending on your organization's settings, you might also be able to view, update, and submit exit reviews from this card.</span></span>

<span data-ttu-id="764ac-148">目標は、**パフォーマンス目標** カードを使用して管理することができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-148">You can manage your goals with the **Performance Goals** card.</span></span> <span data-ttu-id="764ac-149">このカードには、各ステータス (**未開始**、**順調**、**要改善**) における目標数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-149">This card displays the number of goals you have in each status (**Not started**, **On track**, and **Needs improvement**).</span></span> <span data-ttu-id="764ac-150">割り当てられているロール ベースのセキュリティに応じて、目標の作成、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-150">You can create, update, and remove goals, depending on your assigned role-based security.</span></span> <span data-ttu-id="764ac-151">必要に応じて、グループまたはテンプレートから新しい目標を追加できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-151">If you want, you can add new goals from groups or templates.</span></span> <span data-ttu-id="764ac-152">また、管理職と HR は、従業員の代わりに目標を作成し、各目標の詳細を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-152">Managers and HR can also create goals on behalf of employees and determine how detailed each goal will be.</span></span> <span data-ttu-id="764ac-153">管理者と従業員は、目標に関する共同作業や、活動、測定、ステータスの更新を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-153">Managers and employees can collaborate on goals and update activities, measurements, and status.</span></span> <span data-ttu-id="764ac-154">添付ファイルを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-154">You can also include attachments.</span></span>

<span data-ttu-id="764ac-155">**スキル** カードに関する既存のスキルを表示できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-155">You can view your existing skills on the **Skills** card.</span></span> <span data-ttu-id="764ac-156">スキルを更新したり、新しいスキルを追加したり、不要になったスキルを削除したりできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-156">You can update skills, add new ones, or remove any that are no longer relevant.</span></span> <span data-ttu-id="764ac-157">組織の設定に応じて、スキルの変更には承認プロセスが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="764ac-157">Depending on your organization's settings, changes to your skills might go through an approval process.</span></span>

<span data-ttu-id="764ac-158">**報酬** カードを通じて現在の報酬を表示できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-158">You can view your current compensation through the **Compensation** card.</span></span> <span data-ttu-id="764ac-159">**表示** を選択すると、年間支払と前回の昇給金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-159">Select **Show** to view your annual pay and last increase amount.</span></span> <span data-ttu-id="764ac-160">複数の会社で雇われている場合は、各年間の金額がカードに表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-160">If you're employed in more than one company, each annual amount displays on the card.</span></span> <span data-ttu-id="764ac-161">詳細な報酬履歴を表示するには、年収を選択して **固定報酬と変動報酬の履歴** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="764ac-161">To view your detailed compensation history, select the annual salary amount to open the **Fixed and variable compensation history** form.</span></span> <span data-ttu-id="764ac-162">将来の報酬はこのフォームに表示されません。</span><span class="sxs-lookup"><span data-stu-id="764ac-162">Future compensation doesn't display in this form.</span></span> <span data-ttu-id="764ac-163">複数の雇用がある場合は、各会社にログインせずに、このフォーム内の会社間を切り替えて報酬履歴を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-163">If you have more than one employment, you can switch between companies within this form to view your compensation history without logging into each company.</span></span>

<span data-ttu-id="764ac-164">**添付ファイル** カードを使用してドキュメントを表示および管理します。</span><span class="sxs-lookup"><span data-stu-id="764ac-164">View and manage documents with the **Attachments** card.</span></span> <span data-ttu-id="764ac-165">すべての **外部** 添付ファイルを管理できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-165">You can manage all **External** attachments.</span></span> <span data-ttu-id="764ac-166">HR と従業員の両方が、従業員セルフサービスまたは **作業者** フォームを使用して添付ファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-166">Both HR and employees can add attachments through Employee self service or the **Worker** form.</span></span> <span data-ttu-id="764ac-167">添付ファイルは、既定では **外部** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-167">Attachments are set to **External** by default.</span></span>

### <a name="additional-information"></a><span data-ttu-id="764ac-168">追加情報</span><span class="sxs-lookup"><span data-stu-id="764ac-168">Additional information</span></span>

<span data-ttu-id="764ac-169">このセクションでは、**自分の求人情報** セクションのような、その他の従業員セルフサービス領域へのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="764ac-169">This section provides links to other Employee self service areas, similar to the **My Career Information** section.</span></span>

<span data-ttu-id="764ac-170">**福利厚生** リンクを使用して、福利厚生を登録します。</span><span class="sxs-lookup"><span data-stu-id="764ac-170">Sign up for benefits through the **Benefits** link.</span></span> <span data-ttu-id="764ac-171">福利厚生の管理についての詳細は、[福利厚生の概要](hr-benefits-management-overview.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="764ac-171">For more information about Benefits management, see [Benefits overview](hr-benefits-management-overview.md)</span></span>

<span data-ttu-id="764ac-172">**パフォーマンス** では、**業績仕訳** を選択して業績目標とレビューの両方に使用する業績仕訳エントリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-172">Under **Performance**, you can select **Performance journals** to create performance journal entries to use on both performance goals and reviews.</span></span> <span data-ttu-id="764ac-173">**フィードバックの送信** を選択して、組織内の他の従業員に対するフィードバックを提供できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-173">You can select **Send feedback** to provide feedback for other employees within your organization.</span></span> <span data-ttu-id="764ac-174">組織の設定に応じて、メールが受信者、送信者、および管理者に送信される場合があります。</span><span class="sxs-lookup"><span data-stu-id="764ac-174">Depending on your organization's settings, emails might be sent to the recipient, sender, and managers.</span></span> <span data-ttu-id="764ac-175">組織内のすべての従業員にフィードバックを送信できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-175">You can send feedback to all employees within the organization.</span></span> <span data-ttu-id="764ac-176">フィードバックの送信は会社によって制限されません。</span><span class="sxs-lookup"><span data-stu-id="764ac-176">Sending feedback isn't restricted by company.</span></span>

<span data-ttu-id="764ac-177">**コンピテンシー** の下では、**コース**、**教育**、**要職**、および **職務経験** を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-177">Under **Competencies**, you can make changes to **Courses**, **Education**, **Positions of trust**, and **Professional experience**.</span></span> <span data-ttu-id="764ac-178">組織の設定に応じて、コンピテンシーの更新には承認プロセスが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="764ac-178">Depending on your organization's settings, updates to these competencies might go through an approval process.</span></span>

<span data-ttu-id="764ac-179">ジョブの詳細は、**組織** の下に表示できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-179">You can view job details under **Organization**.</span></span> <span data-ttu-id="764ac-180">ジョブの詳細には、基本職位のスキル、証明書、および担当領域が含まれます。</span><span class="sxs-lookup"><span data-stu-id="764ac-180">Job details include skills, certificates, and areas of responsibility for your primary position.</span></span> <span data-ttu-id="764ac-181">また、自分がチェックアウトした貸与された設備を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-181">You can also see any loaned equipment checked out to you.</span></span> <span data-ttu-id="764ac-182">組織の設定に応じて、賃与された設備の変更には承認プロセスが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="764ac-182">Depending on your organization's settings, changes to loaned equipment might go through an approval process.</span></span>

<span data-ttu-id="764ac-183">**アンケート** では、完了したアンケートを表示できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-183">Under **Questionnaire**, you can see completed questionnaires.</span></span> <span data-ttu-id="764ac-184">また、完了していない会社全体のアンケートを見ることもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-184">You can also see company-wide questionnaires that haven't been completed.</span></span> <span data-ttu-id="764ac-185">いつでもアンケートを完了することができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-185">You can choose to complete a questionnaire at any time.</span></span> <span data-ttu-id="764ac-186">アンケートの作成者は、アンケートを適用できるタイムフレームとアンケートの適用者を決定できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-186">The author of the questionnaire can determine the time frame and for whom the questionnaire is applicable.</span></span>

<span data-ttu-id="764ac-187">**人事管理パラメータ** では、ユーザー定義のリンクをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-187">You can configure user-defined links in **Human Resources parameters**.</span></span> <span data-ttu-id="764ac-188">たとえば、支払明細書、年度末のドキュメント、または外部ソリューションへのリンクを定義できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-188">For example, you can define links to pay statements, year-end documentation, or external solutions.</span></span> <span data-ttu-id="764ac-189">これらのリンクは、このセクションの下部に表示されますが、パーソナル化を使用して移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-189">These links display at the bottom of this section, but you can move them by using personalization.</span></span>

<span data-ttu-id="764ac-190"> 従業員セルフサービスワークスペース内に Power Apps を埋め込むことによって追加のタブを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-190">You can also create additional tabs by embedding Power Apps within the Employee self service workspace.</span></span> <span data-ttu-id="764ac-191">**設定** メニューを使用して、任意の Power Apps を使ってページをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="764ac-191">Use the **Settings** menu to personalize the page with any Power Apps.</span></span> <span data-ttu-id="764ac-192">**設定** メニューで、Power App の追加、詳細の入力、アプリの挿入を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-192">In the **Settings** menu, you can choose to add a Power App, complete the details, and insert the app.</span></span> <span data-ttu-id="764ac-193">既定では、Power Apps はシーケンスの最初のタブとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-193">By default, Power Apps appears as the first tab in the sequence.</span></span> <span data-ttu-id="764ac-194">この順序は、標準のパーソナル化を使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-194">You can change the order by using standard personalization.</span></span>

## <a name="my-team"></a><span data-ttu-id="764ac-195">自分のチーム</span><span class="sxs-lookup"><span data-stu-id="764ac-195">My team</span></span>

<span data-ttu-id="764ac-196">**自分のチーム** タブには、マネージャー セルフサービスに関する次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-196">The **My team** tab displays the following information for Manager self service.</span></span> <span data-ttu-id="764ac-197">**自分のチーム** タブには、マネージャのみがアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-197">Only managers can access the **My team** tab.</span></span>

### <a name="personnel-actions"></a><span data-ttu-id="764ac-198">個人のアクション</span><span class="sxs-lookup"><span data-stu-id="764ac-198">Personnel actions</span></span>

<span data-ttu-id="764ac-199">個人アクションは、**人事管理の共有パラメータ** および **人事管理パラメータ** 内のコンフィギュレーション オプションに基づいて表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-199">Personnel actions display based on configuration options within **Human resources shared parameters** and **Human resources parameters**.</span></span> <span data-ttu-id="764ac-200">**従業員** を有効にすると、個人アクションが次のような新しいメニューオプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="764ac-200">When enabled for **Workers**, personnel actions enable new menu options, including:</span></span>

- <span data-ttu-id="764ac-201">**新しい従業員の要求**</span><span class="sxs-lookup"><span data-stu-id="764ac-201">**Request new employee**</span></span>
- <span data-ttu-id="764ac-202">**新しい契約社員の要求**</span><span class="sxs-lookup"><span data-stu-id="764ac-202">**Request new contractor**</span></span>
- <span data-ttu-id="764ac-203">**作業者の再割り当てを要求**</span><span class="sxs-lookup"><span data-stu-id="764ac-203">**Request worker reassignment**</span></span>
- <span data-ttu-id="764ac-204">**退職要求**</span><span class="sxs-lookup"><span data-stu-id="764ac-204">**Request termination**</span></span>
- <span data-ttu-id="764ac-205">**報酬の変更を要求**</span><span class="sxs-lookup"><span data-stu-id="764ac-205">**Request compensation change**</span></span>

<span data-ttu-id="764ac-206">これらのオプションをコンフィギュレーションして、オプションのレビューおよび承認のワークフローを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-206">You can configure these options to go through an optional review and approval workflow.</span></span>

<span data-ttu-id="764ac-207">**職位アクション** を有効にすると、次のオプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="764ac-207">Enabling **Position actions** enable the following options:</span></span>

- <span data-ttu-id="764ac-208">**新しい職位の要求**</span><span class="sxs-lookup"><span data-stu-id="764ac-208">**Request new position**</span></span>
- <span data-ttu-id="764ac-209">**職位の詳細の変更依頼**</span><span class="sxs-lookup"><span data-stu-id="764ac-209">**Request change to position details**</span></span>

<span data-ttu-id="764ac-210">これらのオプションをコンフィギュレーションして、オプションのレビューおよび承認のワークフローを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-210">You can also configure these options to go through an optional review and approval workflow.</span></span>

### <a name="summary"></a><span data-ttu-id="764ac-211">集計</span><span class="sxs-lookup"><span data-stu-id="764ac-211">Summary</span></span>

<span data-ttu-id="764ac-212">**概要** セクションの情報は、**人事リソース パラメータ** で HR が選択したオプションによって異なります。</span><span class="sxs-lookup"><span data-stu-id="764ac-212">Information in the **Summary** section depends on the options HR has selected in **Human resource parameters**.</span></span> <span data-ttu-id="764ac-213">**人事管理パラメータ** ページの **マネージャー セルフサービス** タブで、有効期限が切れるレコードとオープン職位を表示するためのオプションをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-213">On the **Manager self service** tab of the **Human Resources parameters** page, you can configure options for displaying expiring records and open positions.</span></span> <span data-ttu-id="764ac-214">これらのオプションを有効にすると、マネージャーが **概要** セクションで見れるものを決定します。</span><span class="sxs-lookup"><span data-stu-id="764ac-214">Enabling these options determines what managers can see in the **Summary** section.</span></span>

<span data-ttu-id="764ac-215">マネージャーに対して次のタイルをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-215">You can configure the following tiles for managers:</span></span>

- <span data-ttu-id="764ac-216">**期限が切れる自分のチームの証明書**</span><span class="sxs-lookup"><span data-stu-id="764ac-216">**Certificates expiring for my team**</span></span>
- <span data-ttu-id="764ac-217">**期限が切れる自分のチームの ID 番号**</span><span class="sxs-lookup"><span data-stu-id="764ac-217">**Identification numbers expiring for my team**</span></span>
- <span data-ttu-id="764ac-218">**期限が切れる自分のチームの猶予期間**</span><span class="sxs-lookup"><span data-stu-id="764ac-218">**Probations expiring for my team**</span></span>
- <span data-ttu-id="764ac-219">**期限が切れる自分のチームの審査**</span><span class="sxs-lookup"><span data-stu-id="764ac-219">**Screenings expiring for my team**</span></span>
- <span data-ttu-id="764ac-220">**期限が切れる自分のチームのテスト**</span><span class="sxs-lookup"><span data-stu-id="764ac-220">**Tests expiring for my team**</span></span>
- <span data-ttu-id="764ac-221">**直接レポートまたは拡張レポートの空いている職位**</span><span class="sxs-lookup"><span data-stu-id="764ac-221">**Open positions for direct and/or extended reports**</span></span>
- <span data-ttu-id="764ac-222">**自分のチームの保留中の休暇リクエスト**</span><span class="sxs-lookup"><span data-stu-id="764ac-222">**Pending time off requests for my team**</span></span>
- <span data-ttu-id="764ac-223">**チームのスキル評価**</span><span class="sxs-lookup"><span data-stu-id="764ac-223">**Team skills assessment**</span></span>
- <span data-ttu-id="764ac-224">**スキル ギャップ分析**</span><span class="sxs-lookup"><span data-stu-id="764ac-224">**Skill gap analysis**</span></span>
- <span data-ttu-id="764ac-225">**チーム業績仕訳**</span><span class="sxs-lookup"><span data-stu-id="764ac-225">**Team performance journals**</span></span>
- <span data-ttu-id="764ac-226">**チーム業績目標**</span><span class="sxs-lookup"><span data-stu-id="764ac-226">**Team performance goals**</span></span>
- <span data-ttu-id="764ac-227">**チーム業績の確認**</span><span class="sxs-lookup"><span data-stu-id="764ac-227">**Team performance reviews**</span></span>
- <span data-ttu-id="764ac-228">**退職予定の作業者**</span><span class="sxs-lookup"><span data-stu-id="764ac-228">**Exiting workers**</span></span>

<span data-ttu-id="764ac-229">マネージャーに対して次のオプションをコンフィギュレーションして、自分の直属の部下に代わって変更を加えたり、休暇リクエストを追加したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-229">You can configure the following options for managers to make changes or add leave requests on behalf of their direct reports:</span></span>

- <span data-ttu-id="764ac-230">証明書</span><span class="sxs-lookup"><span data-stu-id="764ac-230">Certificates</span></span>
- <span data-ttu-id="764ac-231">コース</span><span class="sxs-lookup"><span data-stu-id="764ac-231">Courses</span></span>
- <span data-ttu-id="764ac-232">貸与品目</span><span class="sxs-lookup"><span data-stu-id="764ac-232">Loan items</span></span>
- <span data-ttu-id="764ac-233">スキル</span><span class="sxs-lookup"><span data-stu-id="764ac-233">Skills</span></span>
- <span data-ttu-id="764ac-234">休暇申請</span><span class="sxs-lookup"><span data-stu-id="764ac-234">Leave and absence requests</span></span>

### <a name="my-team-information"></a><span data-ttu-id="764ac-235">自分のチーム情報</span><span class="sxs-lookup"><span data-stu-id="764ac-235">My team information</span></span>

<span data-ttu-id="764ac-236">自分のチーム情報を使用すると、マネージャーは直属の部下や拡張レポートを表示して更新できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-236">My team information allows managers to view and update direct and extended reports.</span></span> <span data-ttu-id="764ac-237">拡張レポートにアクセスするには、指示を出した従業員を選択し、カードで **チームを表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="764ac-237">To access extended reports, select the employee who has directs, and then choose **View team** on the card.</span></span> <span data-ttu-id="764ac-238">すべての同じオプションは、直属の部下として拡張レポートに適用されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-238">All of the same options apply to extended reports as direct reports.</span></span> 

#### <a name="summary-tab"></a><span data-ttu-id="764ac-239">概要タブ</span><span class="sxs-lookup"><span data-stu-id="764ac-239">Summary tab</span></span>

<span data-ttu-id="764ac-240">**概要** タブでは、直属の部下のクイックビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="764ac-240">The **Summary** tab provides a quick view of your direct reports.</span></span> <span data-ttu-id="764ac-241">直属の部下の下に作業者がいる場合も、カードには直属の部下の数を **チームの表示** ボタンと共に上部セクションに表示します。</span><span class="sxs-lookup"><span data-stu-id="764ac-241">If a direct report also has workers reporting to them, the card displays the number of direct reports in the upper section, along with a **View team** button.</span></span> <span data-ttu-id="764ac-242">各カードの上のオプションは、選択された従業員に適用されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-242">Options above each card apply to the selected employee.</span></span> <span data-ttu-id="764ac-243">たとえば、従業員の代理として休暇リクエストを入力する場合は、その従業員を選択し、カードの上の **休暇リクエスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="764ac-243">For example, if you want to enter a leave request on behalf of an employee, you select the employee and then choose **Request time off** above the cards.</span></span> 

<span data-ttu-id="764ac-244">従業員を選択した後に、**詳細** ボタンを選択した場合は、次のオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-244">If you select the **Details** button after selecting an employee, the following options display:</span></span>

- <span data-ttu-id="764ac-245">**証明書**</span><span class="sxs-lookup"><span data-stu-id="764ac-245">**Certificates**</span></span>
- <span data-ttu-id="764ac-246">**報酬**</span><span class="sxs-lookup"><span data-stu-id="764ac-246">**Compensation**</span></span>
- <span data-ttu-id="764ac-247">**コース**</span><span class="sxs-lookup"><span data-stu-id="764ac-247">**Courses**</span></span>
- <span data-ttu-id="764ac-248">**確認**</span><span class="sxs-lookup"><span data-stu-id="764ac-248">**Reviews**</span></span>
- <span data-ttu-id="764ac-249">**休暇**</span><span class="sxs-lookup"><span data-stu-id="764ac-249">**Time off**</span></span>
- <span data-ttu-id="764ac-250">**貸与品目**</span><span class="sxs-lookup"><span data-stu-id="764ac-250">**Loaned items**</span></span>
- <span data-ttu-id="764ac-251">**業績目標**</span><span class="sxs-lookup"><span data-stu-id="764ac-251">**Performance goals**</span></span>
- <span data-ttu-id="764ac-252">**登録済コース**</span><span class="sxs-lookup"><span data-stu-id="764ac-252">**Registered courses**</span></span>
- <span data-ttu-id="764ac-253">**スキル**</span><span class="sxs-lookup"><span data-stu-id="764ac-253">**Skills**</span></span>
- <span data-ttu-id="764ac-254">**フィードバックの送信**</span><span class="sxs-lookup"><span data-stu-id="764ac-254">**Send feedback**</span></span>

<span data-ttu-id="764ac-255">組織の設定に応じて、変更か表示のいずれか一方のみを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-255">Depending on your organization's settings, you can either make changes or view only.</span></span>

#### <a name="position-tab"></a><span data-ttu-id="764ac-256">職位タブ</span><span class="sxs-lookup"><span data-stu-id="764ac-256">Position tab</span></span>

<span data-ttu-id="764ac-257">**職位** タブは、主要職位にある従業員の概要ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="764ac-257">The **Positions** tab provides a summary view of employees in their primary position.</span></span> <span data-ttu-id="764ac-258">名前、タイル、部門が各カードのヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-258">Name, tile, and department displays in the heading area of each card.</span></span> <span data-ttu-id="764ac-259">このカードの内容は次の通りです。</span><span class="sxs-lookup"><span data-stu-id="764ac-259">This card includes:</span></span>

- <span data-ttu-id="764ac-260">**勤続日数** - 作業者フォームの作業者の概要セクションから表示されます</span><span class="sxs-lookup"><span data-stu-id="764ac-260">**Seniority date** - Displayed from the worker summary section of the worker form</span></span>
- <span data-ttu-id="764ac-261">**勤続年数** - 従業員の雇用開始日に基づいて計算されます</span><span class="sxs-lookup"><span data-stu-id="764ac-261">**Years of service** - Calculated based on the employee's employment start date</span></span>
- <span data-ttu-id="764ac-262">**前の職位の数** - 職位履歴に基づき、この番号を選択すると、以前に保留したすべての職位の詳細ビューが開きます</span><span class="sxs-lookup"><span data-stu-id="764ac-262">**Number of previous positions** - Based on position history, selecting this number opens the detailed view of all previously held positions</span></span>
- <span data-ttu-id="764ac-263">**生年月日** - 従業員の生年月日の月と日</span><span class="sxs-lookup"><span data-stu-id="764ac-263">**Birth date** - The month and day of the employee's birth date</span></span>

<span data-ttu-id="764ac-264">直属の部下と拡張レポート両方の職位データを表示できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-264">You can view position data for both direct and extended reports.</span></span>

#### <a name="compensation-tab"></a><span data-ttu-id="764ac-265">報酬タブ</span><span class="sxs-lookup"><span data-stu-id="764ac-265">Compensation tab</span></span>

<span data-ttu-id="764ac-266">**報酬** タブは、従業員の年収を表示します。</span><span class="sxs-lookup"><span data-stu-id="764ac-266">The **Compensation** tab displays the employee's annual salary.</span></span> <span data-ttu-id="764ac-267">会社識別子は給与金額の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-267">A company identifier displays under the salary amount.</span></span> <span data-ttu-id="764ac-268">従業員が複数の雇用を持ち、複数の法人から支払を受ける場合、従業員には複数の報酬プランがあります。</span><span class="sxs-lookup"><span data-stu-id="764ac-268">If an employee has more than one employment and is getting paid from multiple legal entities, the employee will have multiple compensation plans.</span></span> <span data-ttu-id="764ac-269">会社を切り替えることなく、法人間のすべての報酬プランを表示するには、**Human Resources > 共有パラメータ > 詳細なアクセス > 会社間報酬の有効化** で、相互補償を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="764ac-269">To see all compensation plans across legal entities without switching companies, you must enable cross compensation under **Human Resources > Shared parameters > Advanced access > Enable cross company compensation**.</span></span>

<span data-ttu-id="764ac-270">報酬履歴を表示するには、給与金額を選択して、**詳細** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="764ac-270">To view compensation history, select the salary amount to open the **Details** form.</span></span> <span data-ttu-id="764ac-271">**報酬** フォームには、現在と過去の固定報酬レコードと変動報酬レコードだけが表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-271">Only current and historical fixed and variable compensation records display in the **Compensation** form.</span></span> <span data-ttu-id="764ac-272">従業員に複数の雇用がある場合は、会社間を切り替えて各会社の報酬履歴を表示したり、Human Resources　の共有パラメーターで会社間報酬を有効にして、すべての報酬プランを表示したりできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-272">If an employee has more than one employment, you can switch between companies to view compensation history in each company or enable cross company compensation in Human Resources Shared parameters to view all compensation plans.</span></span>

<span data-ttu-id="764ac-273">直属の部下と拡張レポート両方の報酬を表示できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-273">You can view compensation for both direct and extended reports.</span></span>

#### <a name="leave-and-absence-tab"></a><span data-ttu-id="764ac-274">休暇タブ</span><span class="sxs-lookup"><span data-stu-id="764ac-274">Leave and absence tab</span></span>

<span data-ttu-id="764ac-275">**休暇** タブには、活動がある従業員の上部残高が表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-275">The **Leave and absence** tab displays the top balances for employees that have activity.</span></span> <span data-ttu-id="764ac-276">アクションの実行や活動の全一覧を表示するには、**詳細** を選択して、**休暇** を選択します。</span><span class="sxs-lookup"><span data-stu-id="764ac-276">To take action or view a full list of activities, select **Details** and then select **Time off**.</span></span> <span data-ttu-id="764ac-277">**休暇** フォームでは、残高、要求、承認済の休暇、および予測残高を表示して、従業員が時間を管理しやすくすることができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-277">On the **Time off** form, you can view balances, requests, approved time off, and forecast balances to help employees better manage time.</span></span> <span data-ttu-id="764ac-278">組織の設定によっては、自分の直属の部下と拡張レポートの休暇を要求することもできます。</span><span class="sxs-lookup"><span data-stu-id="764ac-278">Depending on your organization's settings, you can also request time off for your directs and extended reports.</span></span>

#### <a name="performance-goals-tab"></a><span data-ttu-id="764ac-279">業績目標タブ</span><span class="sxs-lookup"><span data-stu-id="764ac-279">Performance goals tab</span></span>

<span data-ttu-id="764ac-280">**業績目標** タブは、ステータス別の業績目標の集計が示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-280">The **Performance goals** tab summarizes performance goals by status.</span></span> <span data-ttu-id="764ac-281">ステータスの数値を選択するか、または **詳細** から業績目標を選択して、従業員のすべての目標を表示します。</span><span class="sxs-lookup"><span data-stu-id="764ac-281">Select a number for a status or select performance goals from the **Details** to see all goals for an employee.</span></span> <span data-ttu-id="764ac-282">マネージャと従業員は、目標の期間にわたって必要に応じて目標を更新できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-282">Managers and employees can update goals as needed over the duration of the goal.</span></span>

<span data-ttu-id="764ac-283">マネージャは、**自分のチーム** の **概要** セクションにある **チームの業績目標** を通して、チームのすべての目標を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-283">Managers can see all goals for their team through the **Team performance goals** tile in the **Summary** section of **My team**.</span></span>

#### <a name="reviews-tab"></a><span data-ttu-id="764ac-284">レビュー タブ</span><span class="sxs-lookup"><span data-stu-id="764ac-284">Reviews tab</span></span>

<span data-ttu-id="764ac-285">**レビュー** タブは、**進行中**、**レビュー待ち**、**最終レビュー** の各状態における従業員の評価の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="764ac-285">The **Reviews** tab summarizes the reviews the employee has in each state: **In progress**, **Ready for review**, and **Final review**.</span></span> <span data-ttu-id="764ac-286">従業員のレビューにアクセスするには、**詳細** ボタンを選択し、共同作業を行うためにレビューをする を選択します。</span><span class="sxs-lookup"><span data-stu-id="764ac-286">To access an employee's review, select the **Details** button and then select reviews to collaborate on.</span></span> <span data-ttu-id="764ac-287">レビューがワークフロー プロセス内のどこにあるかに基づいて、レビューを更新できるかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="764ac-287">Based on where a review is within the workflow process, you can see if the review is available for updating.</span></span> 

<span data-ttu-id="764ac-288">**自分のチーム** の **概要** セクションにある **チームの業績目標のレビュー** を通して、自分のチームのすべての目標を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="764ac-288">You can see all reviews for your team through the **Team performance reviews** tile in the **Summary** section of **My team**.</span></span>