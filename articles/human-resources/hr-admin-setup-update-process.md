---
title: 更新プロセス
description: Microsoft Dynamics 365 Human Resources は、アプリケーションとプラットフォームの変更のための、継続的な自動サービス更新を提供するサービス (SaaS) としての真のソフトウェアです。
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d841a026f589d774ec5ada3ac9adcc84dde9aee1
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527813"
---
# <a name="update-process"></a><span data-ttu-id="b5e72-103">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="b5e72-103">Update process</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b5e72-104">Microsoft Dynamics 365 Human Resources は、継続的な自動サービス更新を提供するサービス (SaaS) としての真のソフトウェアです。</span><span class="sxs-lookup"><span data-stu-id="b5e72-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="b5e72-105">これらの更新には、定期的な更新を含むサービスに対する重要な改良を提供する、アプリケーションとプラットフォーム両方の変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="b5e72-106">更新ポリシー</span><span class="sxs-lookup"><span data-stu-id="b5e72-106">Update policy</span></span>

<span data-ttu-id="b5e72-107">更新はすべての環境に対して一定の調子でリリースされます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="b5e72-108">人事管理は、[Microsoft Lifecycle ポリシー](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)に従ってサポートされていて、製品サポートの使用可能性における一貫した予測可能なガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="b5e72-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="b5e72-109">リリースの頻度</span><span class="sxs-lookup"><span data-stu-id="b5e72-109">Release cadence</span></span> 

<span data-ttu-id="b5e72-110">人事管理の更新は、すべての環境に自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="b5e72-111">人事管理には次の 2 つの種類のリリースがあります:</span><span class="sxs-lookup"><span data-stu-id="b5e72-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="b5e72-112">**サービスの更新**: バグ修正および新機能を含む、隔週でリリースされる更新プログラム。</span><span class="sxs-lookup"><span data-stu-id="b5e72-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="b5e72-113">サービス更新には、リリース時に該当するプラットの更新も含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="b5e72-114">プラットフォーム更新がリリースされた時期を把握するには、[表 3: Platform リリース](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5e72-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="b5e72-115">隔週の更新では、地域全体に段階的に展開されます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="b5e72-116">隔週の更新についての詳細は、[Dynamics 365 Human Resources の新機能および変更された機能](hr-admin-whats-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5e72-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="b5e72-117">特に断りのない限り、サポートされているすべてのデータ センターが隔週で更新されます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="b5e72-118">米国、オーストラリア、ヨーロッパ、英国、アジア、カナダが隔週の更新プログラムに含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5e72-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="b5e72-119">**Common Data Service ソリューションの更新**: これらの更新は、必要に応じて約 6 週間ごとに行われます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="b5e72-120">この中には、新規エンティティと Common Data Service の既存のエンティティに対する変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5e72-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="b5e72-121">これらの更新は、隔週の更新と同じ地域に対してリリースされ、すべてのデータ センターを通じてレプリケートされるまでに約 6 週間かかります。</span><span class="sxs-lookup"><span data-stu-id="b5e72-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="b5e72-122">ソリューションの更新は、隔週のサービス プログラムの更新と一致しない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="b5e72-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="b5e72-123">リリースされたすべてのデータセンターで、ソリューションの更新が使用できます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="b5e72-124">更新の複製が自動的に行われるのを待機したくない場合は、すべてのデータ センターの任意の環境にこれらの更新を手動で適用することができます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="b5e72-125">必要に応じて、人事管理では次のタイプの修正も用意されています:</span><span class="sxs-lookup"><span data-stu-id="b5e72-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="b5e72-126">**リビジョン（修正プログラム）**: 隔週のサービス更新プログラムのリリースとは別に、またはその他の方法で実行される可能性のあるバグ修正</span><span class="sxs-lookup"><span data-stu-id="b5e72-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="b5e72-127">**緊急の修正**: 本質的にスタンド アロンである事前対応および事後対応の修正プログラムには、サイトの問題を解決するための構成のみ、またはコードの変更が含まれる場合があり、隔週のサービス更新のリリースとは別に発生することができます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="b5e72-128">リリースは、内部環境で確認、テスト、および検証されます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="b5e72-129">ビルドがサインオフされた後、その後、生産に配置されます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="b5e72-130">2020 年のリリース 間隔の例外</span><span class="sxs-lookup"><span data-stu-id="b5e72-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="b5e72-131">休日を考慮した、2020 年 11 月と 12 月のリリース スケジュールは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="b5e72-131">To account for holidays, the release schedule for November and December 2020 is as follows:</span></span>

- <span data-ttu-id="b5e72-132">11 月リリース: 11 月 2 日 - 11 月 13 日</span><span class="sxs-lookup"><span data-stu-id="b5e72-132">November release: November 2 - November 13</span></span>
- <span data-ttu-id="b5e72-133">12 月リリース: 11 月 30 日 - 12 月 11 日</span><span class="sxs-lookup"><span data-stu-id="b5e72-133">December release: November 30 - December 11</span></span>
 
<span data-ttu-id="b5e72-134">2 週間のリリース頻度は、2021 年 1 月 11 日に通常どおり再開します。</span><span class="sxs-lookup"><span data-stu-id="b5e72-134">The two-week release cadence will resume as usual on January 11, 2021.</span></span>

## <a name="communications"></a><span data-ttu-id="b5e72-135">通信</span><span class="sxs-lookup"><span data-stu-id="b5e72-135">Communications</span></span>

<span data-ttu-id="b5e72-136">人事管理の作業の内容と、次の場所でリリースされた機能について検索できます:</span><span class="sxs-lookup"><span data-stu-id="b5e72-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="b5e72-137">Dynamics 365 Human Resources ロードマップ</span><span class="sxs-lookup"><span data-stu-id="b5e72-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="b5e72-138">Dynamics 365 リリース プラン</span><span class="sxs-lookup"><span data-stu-id="b5e72-138">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="b5e72-139">Dynamics 365 Human Resources での新機能と変更</span><span class="sxs-lookup"><span data-stu-id="b5e72-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="b5e72-140">[Lifecycle Services (LCS) での問題検索](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (プラットフォームに関連するバグのみ)</span><span class="sxs-lookup"><span data-stu-id="b5e72-140">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="b5e72-141">人事管理のブログ</span><span class="sxs-lookup"><span data-stu-id="b5e72-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="b5e72-142">人事管理 Yammer コミュニティ</span><span class="sxs-lookup"><span data-stu-id="b5e72-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="b5e72-143">サンドボックス環境におけるプレビュー機能</span><span class="sxs-lookup"><span data-stu-id="b5e72-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="b5e72-144">サンドボックス環境でプレビュー機能を検証してから、実働環境で有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="b5e72-145">機能の有効化についての詳細は、[機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5e72-145">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="b5e72-146">すべての新機能は少なくとも 30 日間、通常は30-60日間、プレビューのままになります。</span><span class="sxs-lookup"><span data-stu-id="b5e72-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="b5e72-147">主な機能は、通常、プレビュー期間に従って毎年 10 月と 4 月に使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b5e72-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="b5e72-148">機能管理ワークスペースに新しい機能が表示されたら、すぐにそれらをオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="b5e72-149">一部の機能は既定でオンになっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5e72-149">Some features may be on by default.</span></span>

<span data-ttu-id="b5e72-150">場合によっては、通常は整数機能が有効になりますが、オフにすることはできません (機能管理ワークスペースなど)。</span><span class="sxs-lookup"><span data-stu-id="b5e72-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="b5e72-151">機能が一般に使用可能になったら、運用環境でオンまたはオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="b5e72-152">機能管理ワークスペースは、プレビュー機能が必須になるタイミングを示します。</span><span class="sxs-lookup"><span data-stu-id="b5e72-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="b5e72-153">この日付は、通常、半年のリリース計画に沿って 10 月 1 日または 4 月 1 日になっています。</span><span class="sxs-lookup"><span data-stu-id="b5e72-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="b5e72-154">必須機能を無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b5e72-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="b5e72-155">必須になるまでは、すべての環境で機能を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b5e72-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="b5e72-156">サンドボックス環境またはトライアル環境で機能をプレビューすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5e72-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="b5e72-157">データを使用して新しい機能を完成させるには、現在の実稼働環境またはデータベースのコピーをサンドボックス環境に作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5e72-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="b5e72-158">サンドボックス環境のプロビジョニングの詳細については、[人事管理プロジェクトのプロビジョニング](hr-admin-setup-provision.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5e72-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="b5e72-159">テスト環境を削除するには、[インスタンスの削除](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5e72-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="b5e72-160">バグのレポート</span><span class="sxs-lookup"><span data-stu-id="b5e72-160">Report bugs</span></span>

<span data-ttu-id="b5e72-161">プレビュー機能をテストしたり、新機能を試す間に、期待どおりに機能しない項目が見つかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5e72-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="b5e72-162">バグは、[Microsoft Dynamics 365 サポート](https://dynamics.microsoft.com/support/) を通じて報告してください。</span><span class="sxs-lookup"><span data-stu-id="b5e72-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="b5e72-163">参照</span><span class="sxs-lookup"><span data-stu-id="b5e72-163">See also</span></span>

[<span data-ttu-id="b5e72-164">Dynamics 365 および Power Platform リリース プラン</span><span class="sxs-lookup"><span data-stu-id="b5e72-164">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="b5e72-165">Dynamics 365 人事管理の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="b5e72-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="b5e72-166">ソフトウェアのライフサイクル ポリシー</span><span class="sxs-lookup"><span data-stu-id="b5e72-166">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

