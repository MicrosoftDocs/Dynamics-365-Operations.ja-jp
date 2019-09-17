---
title: Dynamics 365 for Talent の新機能および変更された機能 (2019 年 8 月 27 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a405ee96c36dd803fb46894ab58eca9dbfd81b5f
ms.sourcegitcommit: 097492a9e4f53a5e1fd5385d8764798518326818
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/29/2019
ms.locfileid: "1927989"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a><span data-ttu-id="84236-103">Dynamics 365 for Talent の新機能および変更された機能 (2019 年 8 月 27 日)</span><span class="sxs-lookup"><span data-stu-id="84236-103">What's new or changed in Dynamics 365 for Talent (August 27, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84236-104">このトピックでは、Dynamics 365 for Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="84236-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="84236-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="84236-105">Changes in Attract</span></span>

<span data-ttu-id="84236-106">今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="84236-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="84236-107">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="84236-107">Changes in Onboard</span></span>

<span data-ttu-id="84236-108">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="84236-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="84236-109">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="84236-109">Changes in Core HR</span></span>

<span data-ttu-id="84236-110">このセクションに記載された変更は、ビルド番号 8.1.2447 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="84236-110">Changes described in this section apply to build number 8.1.2447.</span></span> <span data-ttu-id="84236-111">ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="84236-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a><span data-ttu-id="84236-112">プレビュー機能は、サンドボックス インスタンスでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="84236-112">Preview features are enabled only in sandbox instances</span></span>

<span data-ttu-id="84236-113">Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを実稼働またはサンドボックスのどちらかに指定することができます。</span><span class="sxs-lookup"><span data-stu-id="84236-113">When you provision a new instance of Talent, you can specify whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="84236-114">サンドボックス タイプのインスタンスにより、新機能を事前にテストできるようになります。</span><span class="sxs-lookup"><span data-stu-id="84236-114">Instances of the Sandbox type allow for early testing of new features.</span></span> <span data-ttu-id="84236-115">既存の Talent のインスタンスすべては、実稼働インスタンス タイプに更新されます。</span><span class="sxs-lookup"><span data-stu-id="84236-115">All existing Talent instances will be updated to the Production instance type.</span></span> <span data-ttu-id="84236-116">既存のインスタンスのいずれかをサンドボックス インスタンス タイプに更新する場合は、変更要求を開始するよう サポート に連絡してください。</span><span class="sxs-lookup"><span data-stu-id="84236-116">If you want one of your existing instances to be updated to the Sandbox instance type, contact Support to initiate the change request.</span></span>

<span data-ttu-id="84236-117">変更を公開する方法の詳細については、[Talent のプロビジョニング](./provisioning-talent.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84236-117">For more information about how changes are published, see [Provision Talent](./provisioning-talent.md).</span></span>

### <a name="view-extended-information-for-performance-in-manager-self-service"></a><span data-ttu-id="84236-118">マネージャー セルフサービスの業績に関する追加情報の確認</span><span class="sxs-lookup"><span data-stu-id="84236-118">View extended information for performance in manager self-service</span></span>

<span data-ttu-id="84236-119">新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="84236-119">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="84236-120">現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行をすることができます。</span><span class="sxs-lookup"><span data-stu-id="84236-120">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="84236-121">また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスを確実に、スムーズに行うことができます。</span><span class="sxs-lookup"><span data-stu-id="84236-121">In addition, direct managers and their employees can maintain and update performance journals to help ensure that the performance review process goes smoothly.</span></span> <span data-ttu-id="84236-122">この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="84236-122">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a><span data-ttu-id="84236-123">従業員が会社に存在する場合、法人を削除することは許可されていません (339849)</span><span class="sxs-lookup"><span data-stu-id="84236-123">Deleting legal entities isn't allowed if employees exist within the company (339849)</span></span>

<span data-ttu-id="84236-124">この変更により、法人に従業員および他の関連データが存在する場合、会社を削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="84236-124">With this change, you can't remove or delete companies if employees and other related data exist for the legal entity.</span></span>

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a><span data-ttu-id="84236-125">報酬管理ビジネス インテリジェンス分析が報酬ワークスペースと一致しません (322493)</span><span class="sxs-lookup"><span data-stu-id="84236-125">Compensation management business intelligence analytics don't match on the compensation workspace (322493)</span></span>

<span data-ttu-id="84236-126">このリリースで、報酬分析は、従業員に割り当てられたプランを正確に反映するように調整されました。</span><span class="sxs-lookup"><span data-stu-id="84236-126">In this release, compensation analytics have been adjusted to accurately reflect the plans assigned to employees.</span></span>

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a><span data-ttu-id="84236-127">ワークフロー プレースホルダー %company% は、ワークフローを通じて従業員を雇用する時に DAT を表示します (343905)</span><span class="sxs-lookup"><span data-stu-id="84236-127">Workflow placeholder %company% displays DAT when hiring employees through workflow (343905)</span></span>

<span data-ttu-id="84236-128">このリリースにより、会社のプレースホルダーは、新しい従業員の雇用に関連付けられている法人を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="84236-128">With this release, the company placeholder displays the legal entity that is associated with the employment of the new employee.</span></span>

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a><span data-ttu-id="84236-129">失効日が設定されている場合、CDSJobPosition エンティティはエラーを表示します (349387)</span><span class="sxs-lookup"><span data-stu-id="84236-129">The CDSJobPosition entity displays an error when valid to date is set (349387)</span></span>

<span data-ttu-id="84236-130">このリリースで、**CDSJobPosition** エンティティ上の **職位の詳細**および**職位の期間**データ ソースについて、Common Data Service から **有効日**フィールドに編集することが許可されています。</span><span class="sxs-lookup"><span data-stu-id="84236-130">In this release, the **Position detail** and the **Position duration** data sources on the **CDSJobPosition** entity allow for edits from Common Data Service to the **Date effective** fields.</span></span> 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a><span data-ttu-id="84236-131">従業員の退職について、最終勤務日が割り当て終了日に設定されます (332496)</span><span class="sxs-lookup"><span data-stu-id="84236-131">For employee termination, the last day worked is populated on Assignment end date (332496)</span></span>

<span data-ttu-id="84236-132">この変更により、職位の**割り当て終了日**が**雇用終了日**に既定で設定されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="84236-132">This change now defaults the position **Assignment end date** to the **Employment end date**.</span></span> <span data-ttu-id="84236-133">これらの既定値は、データの入力時に変更できます。</span><span class="sxs-lookup"><span data-stu-id="84236-133">You can change these defaults while entering data.</span></span>

### <a name="legal-entities-arent-limited-with-hire-338871"></a><span data-ttu-id="84236-134">法人は雇用に関して制限されていません (338871)</span><span class="sxs-lookup"><span data-stu-id="84236-134">Legal entities aren't limited with hire (338871)</span></span>
 
<span data-ttu-id="84236-135">この変更により雇用プロセスが制限され、ユーザーがアクセスできる法人のみが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="84236-135">This change restricts the hiring process to only show those legal entities the user has access to.</span></span>  

## <a name="in-preview"></a><span data-ttu-id="84236-136">プレビュー</span><span class="sxs-lookup"><span data-stu-id="84236-136">In preview</span></span>

### <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="84236-137">合理化された従業員の入力とナビゲーション</span><span class="sxs-lookup"><span data-stu-id="84236-137">Streamlined employee entry and navigation</span></span>

<span data-ttu-id="84236-138">この機能は、サンドボックスおよび試用環境で使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="84236-138">This functionality is now available in sandbox and trial environments.</span></span> <span data-ttu-id="84236-139">この機能を有効にするには、**システム管理 > リンク > 設定 > システム パラメーター > プレビュー機能**に移動します。</span><span class="sxs-lookup"><span data-stu-id="84236-139">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="84236-140">**拡張された作業者フォームおよびナビゲーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="84236-140">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="84236-141">これにより、これらの変更がすべてのユーザーに対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="84236-141">This enables these changes for all users.</span></span> <span data-ttu-id="84236-142">このオプションはいつでもオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="84236-142">You can turn this option off at any time.</span></span>

<span data-ttu-id="84236-143">詳細については、[合理化された従業員の入力とナビゲーション](./streamlined-employee-entry.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84236-143">For more information, see [Streamlined employee entry and navigation](./streamlined-employee-entry.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="84236-144">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="84236-144">Coming soon</span></span>

### <a name="platform-update-29"></a><span data-ttu-id="84236-145">プラットフォーム update 29</span><span class="sxs-lookup"><span data-stu-id="84236-145">Platform update 29</span></span>

<span data-ttu-id="84236-146">プラットフォーム更新プログラム 29 に関する詳細については [Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 29 (2019 年 10 月) のプレビュー機能](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84236-146">For more details about Platform update 29, see [Preview features in Dynamics 365 for Finance and Operations platform update 29 (October 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).</span></span>
