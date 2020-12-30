---
title: 機能の管理
description: Dynamics 365 Human Resources で新機能をオンまたはオフにする方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9176e9519c3bf65ef7a4f1b5ae43dbeb411750f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419411"
---
# <a name="manage-features"></a><span data-ttu-id="6f869-103">機能の管理</span><span class="sxs-lookup"><span data-stu-id="6f869-103">Manage features</span></span>

<span data-ttu-id="6f869-104">Microsoft Dynamics 365 Human Resources の新機能の継続的なロールアウトの一環として、お客様にできるだけ早く新しい機能を体験していただきたいと思います。</span><span class="sxs-lookup"><span data-stu-id="6f869-104">As part of our continuous rollout of new capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="6f869-105">一般公開される準備がほぼ整っており、広範なテストを経たプレビュー機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f869-105">We provide preview features, which are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="6f869-106">一般提供にリリースする前に、顧客フィードバックおよび検証の最終ラウンドを探しています。</span><span class="sxs-lookup"><span data-stu-id="6f869-106">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="6f869-107">Human Resources の新機能に関する詳細は、[Human Resources の新機能](hr-admin-whats-new.md) および [Dynamics 365 と Power Platform リリース プラン](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f869-107">For more information about new features in Human Resources, see [What's new in Human Resources](hr-admin-whats-new.md) and [Dynamics 365 and Power Platform Release Plan](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).</span></span>

<span data-ttu-id="6f869-108">**機能管理** ワークスペースでは、各リリースで可能になる機能の一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="6f869-108">The **Feature management** workspace provides a list of features delivered in each release.</span></span> <span data-ttu-id="6f869-109">既定では、新機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="6f869-109">By default, new features are turned off.</span></span> <span data-ttu-id="6f869-110">ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。</span><span class="sxs-lookup"><span data-stu-id="6f869-110">You can use the workspace to turn them on and view the documentation for them.</span></span> <span data-ttu-id="6f869-111">機能管理の詳細については [機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f869-111">For more information about Feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="6f869-112">すべての新機能は少なくとも 30 日間、通常は 30-60 日間、プレビューのままになります。</span><span class="sxs-lookup"><span data-stu-id="6f869-112">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="6f869-113">主な機能は、通常、プレビュー期間に従って毎年 10 月と 4 月に使用可能です。</span><span class="sxs-lookup"><span data-stu-id="6f869-113">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="6f869-114">**機能管理** ワークスペースに新しい機能が表示されたら、すぐにそれらをオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="6f869-114">As soon as you see new capabilities in the **Feature management** workspace, you can turn them on.</span></span> <span data-ttu-id="6f869-115">一部の機能は既定でオンになっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="6f869-115">Some features may be on by default.</span></span>

<span data-ttu-id="6f869-116">機能が一般に使用可能になったら、運用環境でオンまたはオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="6f869-116">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="6f869-117">**機能管理** ワークスペースは、プレビュー機能が必須になるタイミングを示します。</span><span class="sxs-lookup"><span data-stu-id="6f869-117">The **Feature management** workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="6f869-118">この日付は、通常、半年のリリース計画に沿って 10 月 1 日または 4 月 1 日になっています。</span><span class="sxs-lookup"><span data-stu-id="6f869-118">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="6f869-119">必須機能を無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6f869-119">You can't turn off mandatory features.</span></span> <span data-ttu-id="6f869-120">必須になるまでは、すべての環境で機能を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6f869-120">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="6f869-121">プレビュー機能の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="6f869-121">Enable or disable preview features</span></span>

<span data-ttu-id="6f869-122">プレビュー機能にアクセスするには、まず、環境でプレビュー機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f869-122">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="6f869-123">プレビュー機能の有効化または無効化は、環境に特有のものです。</span><span class="sxs-lookup"><span data-stu-id="6f869-123">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f869-124">プレビュー機能は **サンドボックス** 環境でのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="6f869-124">Preview features are only available in **Sandbox** environments.</span></span> <span data-ttu-id="6f869-125">プレビュー機能をオンにすると、その環境内の組織にいるすべてのユーザーに対してその機能が有効になります。</span><span class="sxs-lookup"><span data-stu-id="6f869-125">When you turn on a preview feature, you enable it for all users in your organization who are in that environment.</span></span> <span data-ttu-id="6f869-126">プレビュー機能をオフにすると、プレビュー機能が無効になり、ユーザーがアクセスできないようになります。</span><span class="sxs-lookup"><span data-stu-id="6f869-126">When you turn off the preview feature, you disable it and make it inaccessible to your users.</span></span> <span data-ttu-id="6f869-127">プレビュー機能は、Human Resources でサポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="6f869-127">Preview features have limited support in Human Resources.</span></span> <span data-ttu-id="6f869-128">プライバシーとセキュリティ対策の使用は少なく、Human Resources サービス レベル アグリーメント (SLA) には含まれません。</span><span class="sxs-lookup"><span data-stu-id="6f869-128">They might use fewer privacy and security measures, and they aren't included in the Human Resources service level agreement (SLA).</span></span> <span data-ttu-id="6f869-129">個人のデータ (つまり、ユーザーを識別する任意の情報)、または法律上または規制順守要件の対象となるその他のデータを処理するプレビュー機能を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="6f869-129">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

1. <span data-ttu-id="6f869-130">人事管理では、**システム管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f869-130">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="6f869-131">**機能管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f869-131">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="6f869-132">プレビュー機能を有効にするには、一覧から選択して **有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f869-132">To enable a preview feature, select it from the list, and then select **Enable**.</span></span> <span data-ttu-id="6f869-133">プレビュー機能を無効にするには、一覧から選択して **無効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f869-133">To disable a preview feature, select it from the list, and then select **Disable**.</span></span>

## <a name="enable-or-disable-benefits-management"></a><span data-ttu-id="6f869-134">福利厚生の管理の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="6f869-134">Enable or disable Benefits management</span></span>

<span data-ttu-id="6f869-135">福利厚生の管理を有効にするには、[プレビュー機能の有効化または無効化](hr-admin-manage-features.md?enable-or-disable-preview-features) と同じ手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f869-135">To enable Benefits management, use the same procedure in [Enable or disable preview features](hr-admin-manage-features.md?enable-or-disable-preview-features).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f869-136">有効にした後は、**実稼働** 環境で福利厚生の管理を無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6f869-136">You can't disable Benefits management in a **Production** environment after you enable it.</span></span> <span data-ttu-id="6f869-137">ただし、**サンドボックス** 環境では、福利厚生の管理を無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6f869-137">You can disable Benefits management in **Sandbox** environments, however.</span></span>

<span data-ttu-id="6f869-138">給付金管理の構成と使用の詳細については、[給付金管理の概要](hr-benefits-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f869-138">For more information about Benefits management configuration and use, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

<span data-ttu-id="6f869-139">給付金管理では、**給付金** ワークスペースの機能が置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="6f869-139">Benefits management replaces functionality in the **Benefits** workspace.</span></span> <span data-ttu-id="6f869-140">給付金管理のプレビュー機能を有効にすると、**給付金** ワークスペースの次のフォームにアクセスできなくなります。</span><span class="sxs-lookup"><span data-stu-id="6f869-140">When you enable the Benefits management preview feature, you can no longer access the following forms in the **Benefits** workspace:</span></span>

- <span data-ttu-id="6f869-141">**福利厚生**</span><span class="sxs-lookup"><span data-stu-id="6f869-141">**Benefits**</span></span>
- <span data-ttu-id="6f869-142">**給付金の要素**</span><span class="sxs-lookup"><span data-stu-id="6f869-142">**Benefit elements**</span></span>
- <span data-ttu-id="6f869-143">**貢献度計算レート**</span><span class="sxs-lookup"><span data-stu-id="6f869-143">**Contribution calculation rates**</span></span>
- <span data-ttu-id="6f869-144">**給付金登録の結果**</span><span class="sxs-lookup"><span data-stu-id="6f869-144">**Benefit enrollment results**</span></span>
- <span data-ttu-id="6f869-145">**給付金の期限切れと延長の結果**</span><span class="sxs-lookup"><span data-stu-id="6f869-145">**Benefit expiration and extension results**</span></span>
- <span data-ttu-id="6f869-146">**給付金の適格性ポリシー ルール タイプ**</span><span class="sxs-lookup"><span data-stu-id="6f869-146">**Benefit eligibility policy rule types**</span></span>
- <span data-ttu-id="6f869-147">**給付金の適格性ポリシー**</span><span class="sxs-lookup"><span data-stu-id="6f869-147">**Benefit eligibility policies**</span></span>
- <span data-ttu-id="6f869-148">**適格性イベント**</span><span class="sxs-lookup"><span data-stu-id="6f869-148">**Eligibility events**</span></span>

<span data-ttu-id="6f869-149">これらのフォームの情報は、読み取り専用モードで表示できます。</span><span class="sxs-lookup"><span data-stu-id="6f869-149">You can view the information in these forms in read-only mode.</span></span> <span data-ttu-id="6f869-150">情報を編集する場合は、まず福利厚生の管理を無効にする必要があります (**サンドボックス** 環境にのみ適用)。</span><span class="sxs-lookup"><span data-stu-id="6f869-150">If you want to edit the information, you must first disable Benefits management (applicable to **Sandbox** environments only).</span></span>

## <a name="enable-or-disable-leave-and-absence"></a><span data-ttu-id="6f869-151">休暇および欠勤の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="6f869-151">Enable or disable Leave and absence</span></span>

<span data-ttu-id="6f869-152">休暇および欠勤を有効にするには、[プレビュー機能の有効化または無効化](hr-admin-manage-features.md?enable-or-disable-preview-features) と同じ手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f869-152">To enable Leave and absence, use the same procedure in [Enable or disable preview features](hr-admin-manage-features.md?enable-or-disable-preview-features).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f869-153">有効にした後に 休暇および欠勤の **複数の休暇タイプ** 機能を無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6f869-153">You can’t disable the **Multiple leave types** feature in Leave and absence after you enable it.</span></span> <span data-ttu-id="6f869-154">これは、**サンドボックス** 環境と **実稼働** 環境の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f869-154">This applies to both **Sandbox** and **Production** environments.</span></span>

<span data-ttu-id="6f869-155">休暇および欠勤のプレビュー機能の詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f869-155">For more information about preview features in Leave and absence, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

## <a name="send-us-feedback"></a><span data-ttu-id="6f869-156">フィードバックをお送りください</span><span class="sxs-lookup"><span data-stu-id="6f869-156">Send us feedback</span></span>

<span data-ttu-id="6f869-157">これらのプレビュー機能の使用経験に関するご意見をお聞かせください。</span><span class="sxs-lookup"><span data-stu-id="6f869-157">We want to hear from you about your experience with preview features.</span></span> <span data-ttu-id="6f869-158">その他の機能を使用する際に、以下のサイトにて、フィードバックを定期的に転記することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f869-158">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="6f869-159">[コミュニティ](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – このサイトは、ユーザーが使用ケースを説明したり、質問したり、およびコミュニティ ヘルプを得られる優れたリソースです。</span><span class="sxs-lookup"><span data-stu-id="6f869-159">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="6f869-160">製品に必要な機能、または既存の機能に対して行われるべき変更についてお知らせください。</span><span class="sxs-lookup"><span data-stu-id="6f869-160">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="6f869-161">[Human Resources のアイデア](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources) で製品アイデアを提案します。</span><span class="sxs-lookup"><span data-stu-id="6f869-161">Suggest product ideas on [Human Resources ideas](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).</span></span>
    
<span data-ttu-id="6f869-162">フィードバックまたは製品のレビューの送信には個人データ (ユーザーを識別できる任意の情報) を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="6f869-162">Please don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="6f869-163">収集した情報はさらに分析されることがありますが、該当するプライバシーに関する法律の下で要求に回答するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="6f869-163">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="6f869-164">これらのプログラムで個別に収集された個人データは、[Microsoft のプライバシーに関する声明](https://privacy.microsoft.com/privacystatement) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="6f869-164">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="see-also"></a><span data-ttu-id="6f869-165">参照</span><span class="sxs-lookup"><span data-stu-id="6f869-165">See also</span></span>

- [<span data-ttu-id="6f869-166">Human Resources の新機能</span><span class="sxs-lookup"><span data-stu-id="6f869-166">What's new in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="6f869-167">Dynamics 365 および Power Platform リリース プラン</span><span class="sxs-lookup"><span data-stu-id="6f869-167">Dynamics 365 and Power Platform Release Plan</span></span>](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)