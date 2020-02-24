---
title: プロセスの更新
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1817e072805bafbf0d5a9eb2698ef75abc75ad68
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031093"
---
# <a name="update-process"></a><span data-ttu-id="02f95-102">プロセスの更新</span><span class="sxs-lookup"><span data-stu-id="02f95-102">Update process</span></span>

<span data-ttu-id="02f95-103">Microsoft Dynamics 365 Human Resources は、継続的な自動サービス更新を提供するサービス (SaaS) としての真のソフトウェアです。</span><span class="sxs-lookup"><span data-stu-id="02f95-103">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="02f95-104">これらの更新には、定期的な更新を含むサービスに対する重要な改良を提供する、アプリケーションとプラットフォーム両方の変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="02f95-104">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="02f95-105">更新ポリシー</span><span class="sxs-lookup"><span data-stu-id="02f95-105">Update policy</span></span>

<span data-ttu-id="02f95-106">更新はすべての環境に対して一定の調子でリリースされます。</span><span class="sxs-lookup"><span data-stu-id="02f95-106">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="02f95-107">人事管理は、[Microsoft Lifecycle ポリシー](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)に従ってサポートされていて、製品サポートの使用可能性における一貫した予測可能なガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="02f95-107">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="02f95-108">リリースの頻度</span><span class="sxs-lookup"><span data-stu-id="02f95-108">Release cadence</span></span>

<span data-ttu-id="02f95-109">人事管理の更新は、すべての環境に自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="02f95-109">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="02f95-110">人事管理には次の 2 つの種類のリリースがあります:</span><span class="sxs-lookup"><span data-stu-id="02f95-110">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="02f95-111">**サービス更新**: バグ修正および新機能を含む週 1 回の更新。</span><span class="sxs-lookup"><span data-stu-id="02f95-111">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="02f95-112">サービス更新には、リリース時に該当するプラットの更新も含まれます。</span><span class="sxs-lookup"><span data-stu-id="02f95-112">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="02f95-113">プラットフォーム更新がリリースされた時期を把握するには、[表 3: Platform リリース](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02f95-113">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="02f95-114">毎週の更新は通常水曜日にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="02f95-114">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="02f95-115">毎週の更新についての詳細は、[Dynamics 365 Human Resources の新機能および変更された機能](https://docs.microsoft.com/dynamics365/talent/whats-new) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02f95-115">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="02f95-116">特に断りのない限り、サポートされているすべてのデータセンターが毎週更新されます。</span><span class="sxs-lookup"><span data-stu-id="02f95-116">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="02f95-117">毎週の更新は、通常は水曜日に開始され、日曜日に完了します。</span><span class="sxs-lookup"><span data-stu-id="02f95-117">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="02f95-118">米国、オーストラリア、ヨーロッパ、英国、アジア、およびカナダ地域が毎週の更新プログラムに含まれています。</span><span class="sxs-lookup"><span data-stu-id="02f95-118">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="02f95-119">**Common Data Service ソリューションの更新**: これらの更新は、必要に応じて約 6 週間ごとに行われます。</span><span class="sxs-lookup"><span data-stu-id="02f95-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="02f95-120">この中には、新規エンティティと Common Data Service の既存のエンティティに対する変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02f95-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="02f95-121">これらの更新は、週単位の更新と同じ地域に対してリリースされ、すべてのデータ センターを通じてレプリケートされるまでに約 6 週間かかります。</span><span class="sxs-lookup"><span data-stu-id="02f95-121">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="02f95-122">ソリューションび更新は、毎週のサービス更新と一致しない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="02f95-122">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="02f95-123">次の表は、スケジュールの例を示します。</span><span class="sxs-lookup"><span data-stu-id="02f95-123">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="02f95-124">週</span><span class="sxs-lookup"><span data-stu-id="02f95-124">Week</span></span> | <span data-ttu-id="02f95-125">更新タイプ</span><span class="sxs-lookup"><span data-stu-id="02f95-125">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="02f95-126">1</span><span class="sxs-lookup"><span data-stu-id="02f95-126">1</span></span> | <span data-ttu-id="02f95-127">サービス更新 (すべての地域)</span><span class="sxs-lookup"><span data-stu-id="02f95-127">Service update (all regions)</span></span> |
| <span data-ttu-id="02f95-128">2</span><span class="sxs-lookup"><span data-stu-id="02f95-128">2</span></span> | <span data-ttu-id="02f95-129">サービスの更新 (すべての地域) + ソリューションの更新 (Week 1 地域)</span><span class="sxs-lookup"><span data-stu-id="02f95-129">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="02f95-130">3</span><span class="sxs-lookup"><span data-stu-id="02f95-130">3</span></span> | <span data-ttu-id="02f95-131">サービスの更新 (すべての地域) + ソリューションの更新 (Week 2 地域)</span><span class="sxs-lookup"><span data-stu-id="02f95-131">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="02f95-132">4</span><span class="sxs-lookup"><span data-stu-id="02f95-132">4</span></span> | <span data-ttu-id="02f95-133">サービスの更新 (すべての地域) + ソリューションの更新 (Week 3 地域)</span><span class="sxs-lookup"><span data-stu-id="02f95-133">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="02f95-134">5</span><span class="sxs-lookup"><span data-stu-id="02f95-134">5</span></span> | <span data-ttu-id="02f95-135">サービスの更新 (すべての地域) + ソリューションの更新 (Week 4 地域)</span><span class="sxs-lookup"><span data-stu-id="02f95-135">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="02f95-136">6</span><span class="sxs-lookup"><span data-stu-id="02f95-136">6</span></span> | <span data-ttu-id="02f95-137">サービスの更新 (すべての地域) + ソリューションの更新 (Week 5 地域)</span><span class="sxs-lookup"><span data-stu-id="02f95-137">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="02f95-138">7</span><span class="sxs-lookup"><span data-stu-id="02f95-138">7</span></span> | <span data-ttu-id="02f95-139">サービスの更新 (すべての地域) + ソリューションの更新 (Week 6 地域)</span><span class="sxs-lookup"><span data-stu-id="02f95-139">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="02f95-140">8</span><span class="sxs-lookup"><span data-stu-id="02f95-140">8</span></span> | <span data-ttu-id="02f95-141">サービス更新 (すべての地域)</span><span class="sxs-lookup"><span data-stu-id="02f95-141">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="02f95-142">リリースされたすべてのデータセンターで、ソリューションの更新が使用できます。</span><span class="sxs-lookup"><span data-stu-id="02f95-142">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="02f95-143">更新の複製が自動的に行われるのを待機したくない場合は、すべてのデータ センターの任意の環境にこれらの更新を手動で適用することができます。</span><span class="sxs-lookup"><span data-stu-id="02f95-143">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="02f95-144">必要に応じて、人事管理では次のタイプの修正も用意されています:</span><span class="sxs-lookup"><span data-stu-id="02f95-144">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="02f95-145">**リビジョン (修正プログラム)**: 週単位のサービス更新プログラムのリリースとは別に、またはその他の方法で発生する可能性のあるバグ修正</span><span class="sxs-lookup"><span data-stu-id="02f95-145">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="02f95-146">**緊急の修正**: 本質的にスタンドアロンである予防的なおよび李アクティブな修正プログラムには、サイトの問題を解決するためのコンフィギュレーションのみまたはコードの変更が含まれる場合があり、毎週のサービス更新リリースとは別に発生することができます。</span><span class="sxs-lookup"><span data-stu-id="02f95-146">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="02f95-147">リリースは、内部環境で確認、テスト、および検証されます。</span><span class="sxs-lookup"><span data-stu-id="02f95-147">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="02f95-148">ビルドがサインオフされた後、その後、生産に配置されます。</span><span class="sxs-lookup"><span data-stu-id="02f95-148">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="02f95-149">2019 での例外</span><span class="sxs-lookup"><span data-stu-id="02f95-149">Exceptions in 2019</span></span>

<span data-ttu-id="02f95-150">次の日付は、通常のリリース スケジュールに対する例外です:</span><span class="sxs-lookup"><span data-stu-id="02f95-150">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="02f95-151">日</span><span class="sxs-lookup"><span data-stu-id="02f95-151">Date</span></span> | <span data-ttu-id="02f95-152">説明</span><span class="sxs-lookup"><span data-stu-id="02f95-152">Description</span></span> |
| --- | --- |
| <span data-ttu-id="02f95-153">11 月 25 日の週</span><span class="sxs-lookup"><span data-stu-id="02f95-153">Week of November 25</span></span> | <span data-ttu-id="02f95-154">更新なし</span><span class="sxs-lookup"><span data-stu-id="02f95-154">No updates</span></span> |
| <span data-ttu-id="02f95-155">12 月 16 日の週</span><span class="sxs-lookup"><span data-stu-id="02f95-155">Week of December 16</span></span> | <span data-ttu-id="02f95-156">マイナー更新のみ</span><span class="sxs-lookup"><span data-stu-id="02f95-156">Minor updates only</span></span> |
| <span data-ttu-id="02f95-157">12 月 23 日の週</span><span class="sxs-lookup"><span data-stu-id="02f95-157">Week of December 23</span></span> | <span data-ttu-id="02f95-158">更新なし</span><span class="sxs-lookup"><span data-stu-id="02f95-158">No updates</span></span> |
| <span data-ttu-id="02f95-159">12 月 30 日の週</span><span class="sxs-lookup"><span data-stu-id="02f95-159">Week of December 30</span></span> | <span data-ttu-id="02f95-160">更新なし</span><span class="sxs-lookup"><span data-stu-id="02f95-160">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="02f95-161">通信</span><span class="sxs-lookup"><span data-stu-id="02f95-161">Communications</span></span>

<span data-ttu-id="02f95-162">人事管理の作業の内容と、次の場所でリリースされた機能について検索できます:</span><span class="sxs-lookup"><span data-stu-id="02f95-162">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="02f95-163">Dynamics 365 Human Resources ロードマップ</span><span class="sxs-lookup"><span data-stu-id="02f95-163">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="02f95-164">Dynamics 365 リリース プラン</span><span class="sxs-lookup"><span data-stu-id="02f95-164">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="02f95-165">Dynamics 365 Human Resources での新機能と変更</span><span class="sxs-lookup"><span data-stu-id="02f95-165">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="02f95-166">[Lifecycle Services (LCS) での問題検索](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (プラットフォームに関連するバグのみ)</span><span class="sxs-lookup"><span data-stu-id="02f95-166">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="02f95-167">人事管理のブログ</span><span class="sxs-lookup"><span data-stu-id="02f95-167">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="02f95-168">人事管理 Yammer コミュニティ</span><span class="sxs-lookup"><span data-stu-id="02f95-168">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="02f95-169">サンドボックス環境におけるプレビュー機能</span><span class="sxs-lookup"><span data-stu-id="02f95-169">Preview features in a sandbox environment</span></span>

<span data-ttu-id="02f95-170">サンドボックス環境でプレビュー機能を検証してから、実働環境で有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="02f95-170">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="02f95-171">機能の有効化についての詳細は、[機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02f95-171">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="02f95-172">すべての新機能は少なくとも 30 日間、通常は30-60日間、プレビューのままになります。</span><span class="sxs-lookup"><span data-stu-id="02f95-172">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="02f95-173">主な機能は、通常、プレビュー期間に従って毎年 10 月と 4 月に使用可能です。</span><span class="sxs-lookup"><span data-stu-id="02f95-173">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="02f95-174">機能管理ワークスペースに新しい機能が表示されたら、すぐにそれらをオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="02f95-174">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="02f95-175">一部の機能は既定でオンになっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="02f95-175">Some features may be on by default.</span></span>

<span data-ttu-id="02f95-176">場合によっては、通常は整数機能が有効になりますが、オフにすることはできません (機能管理ワークスペースなど)。</span><span class="sxs-lookup"><span data-stu-id="02f95-176">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="02f95-177">機能が一般に使用可能になったら、運用環境でオンまたはオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="02f95-177">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="02f95-178">機能管理ワークスペースは、プレビュー機能が必須になるタイミングを示します。</span><span class="sxs-lookup"><span data-stu-id="02f95-178">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="02f95-179">この日付は、通常、半年のリリース計画に沿って 10 月 1 日または 4 月 1 日になっています。</span><span class="sxs-lookup"><span data-stu-id="02f95-179">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="02f95-180">必須機能を無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="02f95-180">You can't turn off mandatory features.</span></span> <span data-ttu-id="02f95-181">必須になるまでは、すべての環境で機能を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="02f95-181">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="02f95-182">サンドボックス環境またはトライアル環境で機能をプレビューすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="02f95-182">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="02f95-183">データを使用して新しい機能を完成させるには、現在の実稼働環境またはデータベースのコピーをサンドボックス環境に作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="02f95-183">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="02f95-184">サンドボックス環境のプロビジョニングの詳細については、[人事管理プロジェクトのプロビジョニング](hr-admin-setup-provision.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02f95-184">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="02f95-185">テスト環境を削除するには、[インスタンスの削除](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02f95-185">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="02f95-186">バグのレポート</span><span class="sxs-lookup"><span data-stu-id="02f95-186">Report bugs</span></span>

<span data-ttu-id="02f95-187">プレビュー機能をテストしたり、新機能を試す間に、期待どおりに機能しない項目が見つかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="02f95-187">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="02f95-188">バグは、[Microsoft Dynamics 365 サポート](https://dynamics.microsoft.com/support/) を通じて報告してください。</span><span class="sxs-lookup"><span data-stu-id="02f95-188">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="02f95-189">参照</span><span class="sxs-lookup"><span data-stu-id="02f95-189">See also</span></span>

- [<span data-ttu-id="02f95-190">Dynamics 365 および Power Platform リリース プラン</span><span class="sxs-lookup"><span data-stu-id="02f95-190">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="02f95-191">Dynamics 365 人事管理の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="02f95-191">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="02f95-192">ソフトウェアのライフサイクル ポリシー</span><span class="sxs-lookup"><span data-stu-id="02f95-192">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

