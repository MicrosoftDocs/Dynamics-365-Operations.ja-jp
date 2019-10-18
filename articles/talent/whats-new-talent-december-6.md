---
title: Dynamics 365 Talent Core HR (2018 年 12 月 6 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
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
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 73e0875c3e072bc29050a096888459c6e4bb1b7b
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025959"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-december-6-2018"></a><span data-ttu-id="235e0-103">Dynamics 365 Talent: Core HR (2018 年 12 月 6 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="235e0-103">What's new or changed in Dynamics 365 Talent: Core HR (December 6, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="235e0-104">**ビルド 8.1.2071**</span><span class="sxs-lookup"><span data-stu-id="235e0-104">**Build 8.1.2071**</span></span>

<span data-ttu-id="235e0-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="235e0-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="platform-update-22-for-finance-and-operations"></a><span data-ttu-id="235e0-106">Finance and Operations のプラットフォーム更新プログラム 22</span><span class="sxs-lookup"><span data-stu-id="235e0-106">Platform update 22 for Finance and Operations</span></span>

### <a name="export-up-to-1-million-rows-to-excel"></a><span data-ttu-id="235e0-107">最大 100 万行を Excel にエクスポート</span><span class="sxs-lookup"><span data-stu-id="235e0-107">Export up to 1 million rows to Excel</span></span>

<span data-ttu-id="235e0-108">Excel へのエクスポート機能は、Talent のグリッドから最大 100 万行をエクスポートできるように構成されました。以前の 10,000 行の制限から大幅に上昇しました。</span><span class="sxs-lookup"><span data-stu-id="235e0-108">The Export to Excel feature can now be configured to allow users to export up to 1 million rows from a grid in Talent, a substantial increase from the previous 10,000-row limit.</span></span> 

### <a name="restyled-personalization-toolbar"></a><span data-ttu-id="235e0-109">個人用設定ツールバーの再編成</span><span class="sxs-lookup"><span data-stu-id="235e0-109">Restyled personalization toolbar</span></span>

<span data-ttu-id="235e0-110">個人用設定ツールバーが Finance and Operations のプラットフォーム更新 22 で再編成され、ユーザーが Talent でエクスペリエンスを簡単にカスタマイズできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="235e0-110">The personalization toolbar has been restyled in Platform update 22 for Finance and Operations to help users more easily tailor their own experiences in Talent.</span></span> <span data-ttu-id="235e0-111">次の変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="235e0-111">The following changes were made:</span></span> 

-  <span data-ttu-id="235e0-112">各個人用設定ツールの名前がアイコンと共に表示されるようになったため、ユーザーが使おうと思っているツールをすばやく認識できます。</span><span class="sxs-lookup"><span data-stu-id="235e0-112">The name of each personalization tool is now shown along with an icon, which helps users quickly recognize the tool they are interested in using.</span></span>
-  <span data-ttu-id="235e0-113">現在のツールを使用する方法についての説明も表示され、必要な個人用設定を行う方法を理解するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="235e0-113">The description for how to use the current tool is also now shown, which helps users understand how to make the needed personalizations.</span></span>  
-  <span data-ttu-id="235e0-114">ツールバーの一番左にある特定の領域にドラッグ アンド ドロップすることで、個人用設定ツールバー全体を画面内で移動できます。</span><span class="sxs-lookup"><span data-stu-id="235e0-114">The entire personalization toolbar can be moved across the screen by dragging and dropping on a specific region at the far left of the toolbar.</span></span> <span data-ttu-id="235e0-115">これにより、ユーザーは以前はツールバーによって見えにくかった要素をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="235e0-115">This allows users to personalize elements that were previously obscured by the toolbar.</span></span>   

### <a name="optimized-is-one-of-filtering-experience"></a><span data-ttu-id="235e0-116">「次の値のいずれか」のフィルタリング結果を最適化</span><span class="sxs-lookup"><span data-stu-id="235e0-116">Optimized "is one of" filtering experience</span></span>

<span data-ttu-id="235e0-117">「次の値のいずれか」フィルター演算子は、フィルター ウィンドウおよびグリッド ヘッダーのドロップダウン リストを使用する場合にほとんどのフィールドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="235e0-117">The "is one of" filtering operator is available for most fields when using the Filter Pane and grid header drop-down lists.</span></span> <span data-ttu-id="235e0-118">この演算子により、複数の値に基づいてフィールドをフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="235e0-118">This operator allows a user to filter a field based on multiple values.</span></span> <span data-ttu-id="235e0-119">「次の値のいずれか」演算子の新機能と向上したエクスペリエンスは Finance and Operations のプラットフォーム更新 22 で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="235e0-119">A new and improved experience for the "is one of" operator is available in Platform update 22 for Finance and Operations.</span></span> <span data-ttu-id="235e0-120">詳しくは、[「次の値のいずれか」のフィルタリング結果の最適化](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="235e0-120">To learn more, see [Optimized "is one of" filtering experience](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering).</span></span>

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a><span data-ttu-id="235e0-121">"次の値のいずれか" 演算子を使って Excel からフィルター フィールドにリストを貼り付け</span><span class="sxs-lookup"><span data-stu-id="235e0-121">Paste lists from Excel into filter fields with the "is one of" operator</span></span>

<span data-ttu-id="235e0-122">一部のタスクでは、Talent でデータのフィルター処理に使用する値の一覧が Excel に表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="235e0-122">For some tasks, users might have a list of values in Excel that they'd like to use to filter data in Talent.</span></span> <span data-ttu-id="235e0-123">たとえば、人事管理ユーザーは、システムで追加の調査を必要とする一連の従業員をレポートから特定している可能性があり、このユーザーが Excel から Talent のフィルター フィールドに直接リストをコピーできると最適な場合があります。</span><span class="sxs-lookup"><span data-stu-id="235e0-123">For example, a Human Resource user might have identified a set of employees from a report that need additional research in the system, and it would be ideal for this user to be able to copy the list directly from Excel into a filter field in Talent.</span></span>

<span data-ttu-id="235e0-124">Finance and Operations のプラットフォーム更新 22 以降では、フィルター ウィンドウおよびグリッド列フィルターの「次の値のいずれか」演算子が、フィルター フィールドに直接貼り付けることができるように、Excel からコピーされたリストを認識するようになりました。</span><span class="sxs-lookup"><span data-stu-id="235e0-124">Starting in Platform update 22 for Finance and Operations, the "is one of" operator in the Filter Pane and grid column filtering now recognizes lists copied from Excel so that they can be pasted directly into a filter field.</span></span> <span data-ttu-id="235e0-125">これには、Excel のさまざまな行と列からコピーされた値のコレクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="235e0-125">This includes a collection of values copied from different rows and columns in Excel.</span></span> <span data-ttu-id="235e0-126">この機能の詳細については、["次の値のいずれか" 演算子を使用して Excel からフィルター フィールドに一覧を貼り付ける](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="235e0-126">To learn more about this feature, see [Paste lists from Excel into filter fields with the "is one of" operator](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel).</span></span>

## <a name="in-preview"></a><span data-ttu-id="235e0-127">プレビュー</span><span class="sxs-lookup"><span data-stu-id="235e0-127">In preview</span></span>

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="235e0-128">Talent と Dayforce 間の UK 給与統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="235e0-128">Configure UK payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="235e0-129">Talent および Ceridian Dayforce の統合は、英国のプレビューで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="235e0-129">The integration between Talent and Ceridian Dayforce is available in preview for the UK.</span></span> <span data-ttu-id="235e0-130">詳細については、次のトピックを参照してください。[Talent と Dayforce の間での給与統合のコンフィギュレーション](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration)</span><span class="sxs-lookup"><span data-stu-id="235e0-130">Refer to the following topic for more information, [Configure the payroll integration between Talent and Dayforce](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="235e0-131">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="235e0-131">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="235e0-132">休暇と欠勤: 未来の休暇と休暇残高の予測</span><span class="sxs-lookup"><span data-stu-id="235e0-132">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="235e0-133">従業員が休暇を予測し、現在の休暇残高に影響を与えずに将来の休暇時間要求ができるようにするための変更が行われたため、休暇残高の表示方法も変更されました。</span><span class="sxs-lookup"><span data-stu-id="235e0-133">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="235e0-134">現在表示されている使用可能な残高は、現在までの見越しおよび承認されたすべての休暇申請を含む申請に対して利用可能な休暇の量です。</span><span class="sxs-lookup"><span data-stu-id="235e0-134">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="235e0-135">予測機能がリリースされると、表示されている残高は、現在までの見越額および申請を含めて、現在の休暇の残高に変更されます。</span><span class="sxs-lookup"><span data-stu-id="235e0-135">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="235e0-136">従業員およびマネージャーの両方が、**休暇**カードと**残高休暇**ウィンドウにある従業員およびマネージャー セルフ サービスで更新された残高を参照できます。</span><span class="sxs-lookup"><span data-stu-id="235e0-136">Employees and managers will see these updated balances in employee and manager self service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="235e0-137">**人員**ワークスペースと従業員の**割り当て済の休暇計画**ウィンドウにある更新済みの残高は HR マネージャーが参照できます。</span><span class="sxs-lookup"><span data-stu-id="235e0-137">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="other-changes"></a><span data-ttu-id="235e0-138">その他の変更</span><span class="sxs-lookup"><span data-stu-id="235e0-138">Other changes</span></span> 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a><span data-ttu-id="235e0-139">退職コードは、作業者の職位割り当てレコードには設定されません</span><span class="sxs-lookup"><span data-stu-id="235e0-139">Termination code is not populated to the worker position assignment record</span></span>

<span data-ttu-id="235e0-140">退職処理中に職位割り当てレコードの理由コードを入力する変更が実装されています。</span><span class="sxs-lookup"><span data-stu-id="235e0-140">A change has been implemented that populates the reason code on the position assignment record during the termination process.</span></span>

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a><span data-ttu-id="235e0-141">追加情報のために必要な使用中の個人番号の検証</span><span class="sxs-lookup"><span data-stu-id="235e0-141">Validation for personnel number being in-use needs additional details</span></span>

<span data-ttu-id="235e0-142">新しい番号が生成できない時、問題をわかりやすくするため、番号順序が使用中の場合、追加情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="235e0-142">Additional information is displayed when number sequences are in use, to better understand issues when a new number cannot be generated.</span></span>
 
### <a name="attachments-buttons-not-available-for-workers"></a><span data-ttu-id="235e0-143">作業者は添付ファイルボタンを使用できません</span><span class="sxs-lookup"><span data-stu-id="235e0-143">Attachments buttons not available for workers</span></span>

<span data-ttu-id="235e0-144">添付ファイルを修正するための変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="235e0-144">Changes have been made to correct attachments.</span></span> <span data-ttu-id="235e0-145">作業者に新しい添付ファイルを追加する時、作業者ウィンドウの情報ボックスが開いている場合は**新規**および**編集**ボタンが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="235e0-145">When adding a new attachment to a worker, the **New** and **Edit** buttons are now available when FactBoxes are open on the worker window.</span></span> 

## <a name="known-issues"></a><span data-ttu-id="235e0-146">既知の問題</span><span class="sxs-lookup"><span data-stu-id="235e0-146">Known issues</span></span>

### <a name="mapping-errors-in-the-integration-with-finance"></a><span data-ttu-id="235e0-147">Finance との統合のマッピング エラー</span><span class="sxs-lookup"><span data-stu-id="235e0-147">Mapping errors in the integration with Finance</span></span>

<span data-ttu-id="235e0-148">次の問題は、Talent を Finance と統合するための現在のテンプレートで識別されています。</span><span class="sxs-lookup"><span data-stu-id="235e0-148">The following issues have been identified in the current template for integrating Talent with Finance.</span></span> <span data-ttu-id="235e0-149">新しいテンプレートは、間もなく公開され、作成されたすべての新しい統合プロジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="235e0-149">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="235e0-150">既存の統合プロジェクトのために、タスク マッピングを更新できます。</span><span class="sxs-lookup"><span data-stu-id="235e0-150">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="235e0-151">更新されたマッピングについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="235e0-151">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="235e0-152">ジョブ職位から職位親ジョブ割り当てタスクはデータが統合されていません。</span><span class="sxs-lookup"><span data-stu-id="235e0-152">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="235e0-153">この問題は現在調査中です。</span><span class="sxs-lookup"><span data-stu-id="235e0-153">This is an issue that is currently being researched.</span></span> <span data-ttu-id="235e0-154">現在のマッピングに回避策はありません。</span><span class="sxs-lookup"><span data-stu-id="235e0-154">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="235e0-155">部門から作業単位タスクは、次のマッピングの更新が必要です。</span><span class="sxs-lookup"><span data-stu-id="235e0-155">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="235e0-156">既存のソース フィールド</span><span class="sxs-lookup"><span data-stu-id="235e0-156">Existing source field</span></span>          | <span data-ttu-id="235e0-157">新規ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="235e0-157">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="235e0-158">cdm_description (説明)</span><span class="sxs-lookup"><span data-stu-id="235e0-158">cdm_description (Description)</span></span>  | <span data-ttu-id="235e0-159">cdm_name (名前)</span><span class="sxs-lookup"><span data-stu-id="235e0-159">cdm_name (Name)</span></span>  |

<span data-ttu-id="235e0-160">追加のマッピングも追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="235e0-160">An additional mapping also needs to be added.</span></span> <span data-ttu-id="235e0-161">最後の**なし**フィールドを選択して、次のマッピングを追加します。</span><span class="sxs-lookup"><span data-stu-id="235e0-161">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="235e0-162">ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="235e0-162">Source field</span></span>                   | <span data-ttu-id="235e0-163">出力先フィールド</span><span class="sxs-lookup"><span data-stu-id="235e0-163">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="235e0-164">cdm_description (説明)</span><span class="sxs-lookup"><span data-stu-id="235e0-164">cdm_description (Description)</span></span>  | <span data-ttu-id="235e0-165">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="235e0-165">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="235e0-166">更新されたマッピングは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="235e0-166">The updated mappings should look like this.</span></span>

![部門から作業単位タスク](./media/DepartmentMapping.png)


<span data-ttu-id="235e0-168">ジョブからジョブ詳細タスクへは、次のマッピングの更新が必要です。</span><span class="sxs-lookup"><span data-stu-id="235e0-168">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="235e0-169">既存のソース フィールド</span><span class="sxs-lookup"><span data-stu-id="235e0-169">Existing source field</span></span>          | <span data-ttu-id="235e0-170">新規ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="235e0-170">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="235e0-171">cdm_name (名前)</span><span class="sxs-lookup"><span data-stu-id="235e0-171">cdm_name (Name)</span></span>                | <span data-ttu-id="235e0-172">cdm_description (説明)</span><span class="sxs-lookup"><span data-stu-id="235e0-172">cdm_description (Description)</span></span>      |
| <span data-ttu-id="235e0-173">cdm_name (名前)</span><span class="sxs-lookup"><span data-stu-id="235e0-173">cdm_name (Description)</span></span>         | <span data-ttu-id="235e0-174">cdm_jobdescription (職務明細書)</span><span class="sxs-lookup"><span data-stu-id="235e0-174">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="235e0-175">更新されたマッピングは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="235e0-175">The updated mappings should look like this.</span></span>

![ジョブからジョブ詳細タスク](./media/JobMapping.png)

<span data-ttu-id="235e0-177">作業者から作業タスクへは、次のマッピングの更新が必要です。</span><span class="sxs-lookup"><span data-stu-id="235e0-177">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="235e0-178">既存のソース フィールド</span><span class="sxs-lookup"><span data-stu-id="235e0-178">Existing source field</span></span>                 | <span data-ttu-id="235e0-179">新規ソース フィールド</span><span class="sxs-lookup"><span data-stu-id="235e0-179">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="235e0-180">cdm_emailaddress1 (電子メール アドレス 1)</span><span class="sxs-lookup"><span data-stu-id="235e0-180">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="235e0-181">cdm_primaryemailaddress (主要な電子メール アドレス</span><span class="sxs-lookup"><span data-stu-id="235e0-181">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="235e0-182">cdm_telephone1 (電話1)</span><span class="sxs-lookup"><span data-stu-id="235e0-182">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="235e0-183">cdm_primarytelephone (代表電話)</span><span class="sxs-lookup"><span data-stu-id="235e0-183">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="235e0-184">性別フィールドの変換は、更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="235e0-184">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="235e0-185">性別の**fn** (機能) マップを選択し、次の値のマッピングを更新します。</span><span class="sxs-lookup"><span data-stu-id="235e0-185">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

<span data-ttu-id="235e0-186">| Common Data Service 値   | Finance and Operations 値 | | ------------|------------------ -----------| | 75440000    | 男性                         | | 75440001    | 女性                       | | 75440002    | なし                         | | 75440003    | 一般                  |</span><span class="sxs-lookup"><span data-stu-id="235e0-186">| Common Data Service Value   | Finance and Operations value | | ------------|------------------ -----------| | 75440000    | Male                         | | 75440001    | Female                       | | 75440002    | None                         | | 75440003    | NonSpecific                  |</span></span>

<span data-ttu-id="235e0-187">更新されたマッピングは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="235e0-187">The updated mappings should look like this.</span></span>

![作業者から作業者タスク](./media/WorkerMapping.png)

![性別フィールドの変換](./media/WorkerTransform.png)

