---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 26 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b23860a7eda0ec9d75cca04728b7fc11d01bf967
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812744"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a><span data-ttu-id="d5249-103">Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 26 日)</span><span class="sxs-lookup"><span data-stu-id="d5249-103">What's new or changed in Dynamics 365 Talent (March 26, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5249-104">このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d5249-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="d5249-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="d5249-105">Changes in Attract</span></span>

### <a name="enhancements-to-interview-scheduling"></a><span data-ttu-id="d5249-106">面接のスケジューリングを拡張します</span><span class="sxs-lookup"><span data-stu-id="d5249-106">Enhancements to interview scheduling</span></span>
<span data-ttu-id="d5249-107">面接のスケジューリングでは、次の機能拡張が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="d5249-107">The following enhancements are available in interview scheduling.</span></span>

- <span data-ttu-id="d5249-108">採用担当者または採用マネージャーは、面接者にフィードバックを送信するよう手動でアラームをトリガーできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d5249-108">Recruiters or hiring managers can now manually trigger a reminder for an interviewer to submit their feedback.</span></span> <span data-ttu-id="d5249-109">アラーム用の関連付けられている電子メール テンプレートも設定可能です。</span><span class="sxs-lookup"><span data-stu-id="d5249-109">The associated email template for the reminder is configurable as well.</span></span>
- <span data-ttu-id="d5249-110">面接の概要を候補者と共有中は、面接スケジューラは、面接者の名前を非表示にし、インタビューの概要ビューから行を非表示にすることを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d5249-110">While sharing the interview summary with the candidate, the interview scheduler can choose to hide the names of the interviewers and also choose to hide rows from the interview summary view.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="d5249-111">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="d5249-111">Changes in Onboard</span></span>

### <a name="embedded-images-in-activities"></a><span data-ttu-id="d5249-112">活動の埋め込み画像</span><span class="sxs-lookup"><span data-stu-id="d5249-112">Embedded images in activities</span></span>
<span data-ttu-id="d5249-113">画像を直接活動に埋め込むことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d5249-113">You can now embed images directly into activities.</span></span> <span data-ttu-id="d5249-114">Web から画像をコピーして貼り付けることができるほかに、ローカル ファイル システムから画像をアップロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d5249-114">In addition to being able to copy and paste images from the web, you can upload images from your local file system.</span></span> <span data-ttu-id="d5249-115">活動のサイズは、1 MB に制限されます。</span><span class="sxs-lookup"><span data-stu-id="d5249-115">The size of the activity is limited to 1 MB.</span></span> <span data-ttu-id="d5249-116">画像が大きすぎる場合は、サイズを変更し、もう一度アップロードしてください。</span><span class="sxs-lookup"><span data-stu-id="d5249-116">If the image is too large, resize and try to upload again.</span></span>

<span data-ttu-id="d5249-117">[![マッピング](./media/embedimages.png)](./media/embedimages.png)</span><span class="sxs-lookup"><span data-stu-id="d5249-117">[![Mapping](./media/embedimages.png)](./media/embedimages.png)</span></span>

<span data-ttu-id="d5249-118">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5249-118">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="d5249-119">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="d5249-119">Changes in Core HR</span></span>
<span data-ttu-id="d5249-120">**ビルド 8.1.2210**</span><span class="sxs-lookup"><span data-stu-id="d5249-120">**Build 8.1.2210**</span></span>

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a><span data-ttu-id="d5249-121">Common Data Service でエンティティに選択可能なカスタム フィールド サポート</span><span class="sxs-lookup"><span data-stu-id="d5249-121">Custom field support available for select entities in Common Data Service</span></span> 

<span data-ttu-id="d5249-122">次の Common Data Service エンティティは、Talent で作成した顧客のフィールドに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="d5249-122">The following Common Data Service entities now support customer fields created in Talent:</span></span>

- <span data-ttu-id="d5249-123">ワーカー</span><span class="sxs-lookup"><span data-stu-id="d5249-123">Worker</span></span>
- <span data-ttu-id="d5249-124">出身民族</span><span class="sxs-lookup"><span data-stu-id="d5249-124">Ethnic origin</span></span>
- <span data-ttu-id="d5249-125">退役軍人ステータス</span><span class="sxs-lookup"><span data-stu-id="d5249-125">Veteran status</span></span>
- <span data-ttu-id="d5249-126">言語コード</span><span class="sxs-lookup"><span data-stu-id="d5249-126">Language code</span></span>
- <span data-ttu-id="d5249-127">ジョブ</span><span class="sxs-lookup"><span data-stu-id="d5249-127">Job</span></span>
- <span data-ttu-id="d5249-128">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="d5249-128">Job type</span></span>
- <span data-ttu-id="d5249-129">職務権限</span><span class="sxs-lookup"><span data-stu-id="d5249-129">Job function</span></span>
- <span data-ttu-id="d5249-130">配置</span><span class="sxs-lookup"><span data-stu-id="d5249-130">Position</span></span>
- <span data-ttu-id="d5249-131">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="d5249-131">Position type</span></span>
 
### <a name="employment-history-not-displayed-chronologically"></a><span data-ttu-id="d5249-132">雇用履歴は時系列順に表示されていません</span><span class="sxs-lookup"><span data-stu-id="d5249-132">Employment history not displayed chronologically</span></span>
<span data-ttu-id="d5249-133">この変更により、雇用履歴ページに会社とは関係なく雇用記録が時系列順で表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d5249-133">With this change, the employment history page now displays employment records chronologically, independent of company.</span></span> <span data-ttu-id="d5249-134">並び替えのオプションを使用して会社別に並び替えることもできます。</span><span class="sxs-lookup"><span data-stu-id="d5249-134">You can also use sorting options to sort by company.</span></span>

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a><span data-ttu-id="d5249-135">会社ごとにセキュリティを制限している場合、固定報酬プランは表示されません。</span><span class="sxs-lookup"><span data-stu-id="d5249-135">Fixed compensation plans don't appear when restricting user by company in security.</span></span>
<span data-ttu-id="d5249-136">今回のリリースでは、会社ごとにセキュリティを制限している場合、固定報酬プランが表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d5249-136">In this release, fixed compensation plans now appear when restricting users by company in security.</span></span> <span data-ttu-id="d5249-137">すべてのセキュリティ設定が遵守され、ユーザーにアクセス許可がある会社に対しては固定プランが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5249-137">All security settings will be honored, and fixed plans will appear for those companies the user has permissions to access.</span></span> 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a><span data-ttu-id="d5249-138">Talent の Excel で開くオプションを使用してジョブ レコードを削除できない</span><span class="sxs-lookup"><span data-stu-id="d5249-138">Can't delete Job records using Open in Excel option in Talent</span></span>
<span data-ttu-id="d5249-139">このリリースでは、Talent の **Excel で開く**オプションを使用して、ジョブ レコードを削除できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d5249-139">With this release, you can now remove job records by using the **Open in Excel** option in Talent.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="d5249-140">Common Data Service へのアップグレード</span><span class="sxs-lookup"><span data-stu-id="d5249-140">Upgrade to Common Data Service</span></span>
<span data-ttu-id="d5249-141">Common Data Service へのアップグレードの期限が近づいています。</span><span class="sxs-lookup"><span data-stu-id="d5249-141">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="d5249-142">データベースをアップグレードする必要があるかどうかを決定するために、Power Apps 管理者センターにサインインします。</span><span class="sxs-lookup"><span data-stu-id="d5249-142">Sign in to the Power Apps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="d5249-143">期限およびアップグレードに必要な手順の詳細については、[Common Data Service へのアップグレード](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5249-143">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="in-preview"></a><span data-ttu-id="d5249-144">プレビュー</span><span class="sxs-lookup"><span data-stu-id="d5249-144">In preview</span></span>

<span data-ttu-id="d5249-145">プレビュー機能の有効化については、[Microsoft Dynamics 365 Talent のプレビュー機能の利用](./access-preview-feature.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5249-145">For information about enabling preview features, see [Access preview features in Microsoft Dynamics 365 Talent](./access-preview-feature.md).</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="d5249-146">理由コードを休暇タイプに指定できるようにする</span><span class="sxs-lookup"><span data-stu-id="d5249-146">Allow reason codes to be specified on leave types</span></span>
<span data-ttu-id="d5249-147">組織は、休暇申請に関連する追加情報が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="d5249-147">Organizations might need additional information related to time off requests.</span></span> <span data-ttu-id="d5249-148">この情報を取得するには、従業員は休暇申請に理由コードを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5249-148">To get this information, employees need to include a reason code on their time off requests.</span></span> <span data-ttu-id="d5249-149">このリリースでは、休暇タイプに関連付けられている理由コードを指定し、従業員が休暇申請で理由コードを選択できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d5249-149">With this release, you can now specify the reason codes associated with a given leave type and enable employees to select a reason code on their time off requests.</span></span>

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a><span data-ttu-id="d5249-150">特定の休暇タイプの休暇を送信するときに必要となる理由コードを設定する</span><span class="sxs-lookup"><span data-stu-id="d5249-150">Configure reason codes to be required when submitting time off for certain leave types</span></span>
<span data-ttu-id="d5249-151">従業員が休暇を送信するときに、組織は特定の休暇タイプに理由コードを設定することを要求することがあります。</span><span class="sxs-lookup"><span data-stu-id="d5249-151">Organizations might require reason codes to be set on specific leave types when employees submit time off.</span></span> <span data-ttu-id="d5249-152">これは、その国/地域の法的な要求事項または会社ポリシーに基づいて必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d5249-152">This may be required based on a regulatory requirement in their country/region or a company policy.</span></span> <span data-ttu-id="d5249-153">このリリースでは、HR が理由コードを必要とする休暇タイプを指定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d5249-153">This release provides the ability for HR to specify which leave types require a reason code.</span></span> <span data-ttu-id="d5249-154">これは、休暇に理由コードが必要なところで、従業員が休暇申請を送信したときに実施されます。</span><span class="sxs-lookup"><span data-stu-id="d5249-154">This will be enforced when employees submit time off requests where the leave requires a reason code.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="d5249-155">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="d5249-155">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="d5249-156">高度な報酬セキュリティ (固定および変動)</span><span class="sxs-lookup"><span data-stu-id="d5249-156">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="d5249-157">多くの組織では、報酬および福利厚生の管理者は特定の報酬レコードにのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d5249-157">In many organizations, compensation and benefits managers might only have access to certain compensation records.</span></span> <span data-ttu-id="d5249-158">これらは、経営幹部または地域の従業員向けのものである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d5249-158">These could be for executives or regional employees.</span></span> <span data-ttu-id="d5249-159">この変更により、HR は組織内のさまざまな従業員グループの報酬プランを管理および維持できます。</span><span class="sxs-lookup"><span data-stu-id="d5249-159">With this change, HR can manage and maintain the compensation plans for different employee groups in the organization.</span></span> <span data-ttu-id="d5249-160">固定および変動プランにはセキュリティ ロールを割り当てることができます。これは、プランへのアクセス権とプランに関連する従業員データ (給与または特別償却レコードなど) を決定します。</span><span class="sxs-lookup"><span data-stu-id="d5249-160">You can assign security roles to fixed and variable plans that determine access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="d5249-161">アクセス権を付与されたロールのみが、これらの従業員の報酬を処理できます。</span><span class="sxs-lookup"><span data-stu-id="d5249-161">Only the roles granted with access can process compensation for these employees.</span></span>

###  <a name="email-support-for-alerts"></a><span data-ttu-id="d5249-162">アラートの電子メールサポート</span><span class="sxs-lookup"><span data-stu-id="d5249-162">Email support for alerts</span></span>
<span data-ttu-id="d5249-163">Finance and Operations のプラットフォーム更新プログラム 25 では、あるイベントによってトリガーされた時、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d5249-163">With Platform update 25 for Finance and Operations, users can create alert rules that automatically dispatch email notifications to contacts when triggered by an event.</span></span> 

### <a name="duplicate-employee-checks-user-interface-changes"></a><span data-ttu-id="d5249-164">重複する従業員チェック : ユーザー インターフェイスの変更</span><span class="sxs-lookup"><span data-stu-id="d5249-164">Duplicate employee checks: User interface changes</span></span>
<span data-ttu-id="d5249-165">この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="d5249-165">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="d5249-166">提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。</span><span class="sxs-lookup"><span data-stu-id="d5249-166">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="d5249-167">データ入力の中断を回避するために、重複フォームは自動的に開きません。</span><span class="sxs-lookup"><span data-stu-id="d5249-167">To avoid interrupting data entry, the duplicates form doesn't open automatically.</span></span>
