---
title: 候補者のプロファイルおよび応募のソースの追跡
description: このトピックでは、候補者のプロファイルおよびアプリケーションのソースの追跡に関する情報を提供します。
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 5b368e97a716cd1ce4f668c2a97326877a2d3dff
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551890"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a><span data-ttu-id="5a715-103">候補者のプロファイルおよび応募のソースの追跡</span><span class="sxs-lookup"><span data-stu-id="5a715-103">Track sources for candidate profiles and applications</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="5a715-104">このトピックに記載されている機能は、プレビュー レビュー リリースの一部として、対象とするユーザーが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="5a715-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="5a715-105">コンテンツおよび機能は、変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="5a715-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="5a715-106">この機能を使用するには、Attract の**管理者設定**を使用して有効にするよう管理者に依頼してください。</span><span class="sxs-lookup"><span data-stu-id="5a715-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="5a715-107">将来のリリースでは、ソース追跡レポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="5a715-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="5a715-108">詳細については、[Talent のプレビュー機能の利用](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a715-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="5a715-109">候補者が職務に応募すると、Attract は自動的に申請のソースを追跡し、採用活動に役立つ貴重な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a715-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="5a715-110">採用担当者および採用マネージャーは、職務または人材プールに候補者を手動で追加するときに、アプリケーション ソースを選択できます。</span><span class="sxs-lookup"><span data-stu-id="5a715-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="5a715-111">アプリケーション ソースは、**活動**タブ下のアプリケーション活動の詳細、および人材プールの**プロファイル**で利用可能なアプリケーション履歴を確認できます。</span><span class="sxs-lookup"><span data-stu-id="5a715-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="5a715-112">アプリケーションおよび人材プールの**プロファイル**タブの候補者の詳細から、候補者のプロファイルソースを検索できます。</span><span class="sxs-lookup"><span data-stu-id="5a715-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="5a715-113">プロセス テンプレートについては、[包括採用アドオン](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a715-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="5a715-114">構成済みのソース</span><span class="sxs-lookup"><span data-stu-id="5a715-114">Pre-configured sources</span></span>

<span data-ttu-id="5a715-115">既定のソース リストには、一般的なアプリケーションソースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a715-115">The default source list contains common application sources.</span></span> <span data-ttu-id="5a715-116">**職務ボード**および**ソーシャル ネットワーク**のような、一部のソース タイプには追加のソースの詳細があります。</span><span class="sxs-lookup"><span data-stu-id="5a715-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="5a715-117">たとえば、**ソーシャル ネットワーク**には Facebook および Twitter が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5a715-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="5a715-118">**照会**ソース タイプでは、参照先として内部従業員を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="5a715-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="5a715-119">既定のソース リストには、次の構成済みのソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5a715-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="5a715-120">Attract キャリア サイト</span><span class="sxs-lookup"><span data-stu-id="5a715-120">Attract career site</span></span>

-   <span data-ttu-id="5a715-121">代理店</span><span class="sxs-lookup"><span data-stu-id="5a715-121">Agency</span></span>

-   <span data-ttu-id="5a715-122">キャリアフェア</span><span class="sxs-lookup"><span data-stu-id="5a715-122">Career Fair</span></span>

-   <span data-ttu-id="5a715-123">会社のマーケティング</span><span class="sxs-lookup"><span data-stu-id="5a715-123">Company Marketing</span></span>

-   <span data-ttu-id="5a715-124">会議 & 取引の表示</span><span class="sxs-lookup"><span data-stu-id="5a715-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="5a715-125">職務協会</span><span class="sxs-lookup"><span data-stu-id="5a715-125">Professional Association</span></span>

-   <span data-ttu-id="5a715-126">職務ボード</span><span class="sxs-lookup"><span data-stu-id="5a715-126">Job board</span></span>

    -   <span data-ttu-id="5a715-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="5a715-127">Indeed</span></span>

    -   <span data-ttu-id="5a715-128">Seek</span><span class="sxs-lookup"><span data-stu-id="5a715-128">Seek</span></span>

    -   <span data-ttu-id="5a715-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="5a715-129">CareerBuilder</span></span>

    -   <span data-ttu-id="5a715-130">Google Jobs</span><span class="sxs-lookup"><span data-stu-id="5a715-130">Google Jobs</span></span>

    -   <span data-ttu-id="5a715-131">Xing</span><span class="sxs-lookup"><span data-stu-id="5a715-131">Xing</span></span>

    -   <span data-ttu-id="5a715-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="5a715-132">Glassdoor</span></span>

    -   <span data-ttu-id="5a715-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="5a715-133">Monster Jobs</span></span>

-   <span data-ttu-id="5a715-134">雑誌 & 出版物</span><span class="sxs-lookup"><span data-stu-id="5a715-134">Magazines & Publications</span></span>

-   <span data-ttu-id="5a715-135">ソーシャル ネットワーク</span><span class="sxs-lookup"><span data-stu-id="5a715-135">Social Network</span></span>

    -   <span data-ttu-id="5a715-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="5a715-136">Facebook</span></span>

    -   <span data-ttu-id="5a715-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="5a715-137">Twitter</span></span>

-   <span data-ttu-id="5a715-138">大学の採用</span><span class="sxs-lookup"><span data-stu-id="5a715-138">University Recruiting</span></span>

-   <span data-ttu-id="5a715-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="5a715-139">LinkedIn</span></span>

-   <span data-ttu-id="5a715-140">分類</span><span class="sxs-lookup"><span data-stu-id="5a715-140">Classifieds</span></span>

-   <span data-ttu-id="5a715-141">照会</span><span class="sxs-lookup"><span data-stu-id="5a715-141">Referral</span></span>

-   <span data-ttu-id="5a715-142">採用担当者が追加</span><span class="sxs-lookup"><span data-stu-id="5a715-142">Added by Recruiter</span></span>

-   <span data-ttu-id="5a715-143">外</span><span class="sxs-lookup"><span data-stu-id="5a715-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="5a715-144">ソース リストをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="5a715-144">Customize the source list</span></span> 

<span data-ttu-id="5a715-145">追加のアプリケーション ソースを含めるようにソース リストを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="5a715-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="5a715-146">リストをカスタマイズするには、[Attract のオプション セットの拡張する](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5a715-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="5a715-147">追加のソース含めるために **TalentSource** エンティティを編集する。</span><span class="sxs-lookup"><span data-stu-id="5a715-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="5a715-148">ユーザー インターフェイス (UI) への悪影響を回避するため、以下の場合、**TalentCategory** 列挙値（名前ではない）を編集または削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="5a715-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="5a715-149">**照会**</span><span class="sxs-lookup"><span data-stu-id="5a715-149">**Referral**</span></span>
- <span data-ttu-id="5a715-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="5a715-150">**LinkedIn**</span></span>
- <span data-ttu-id="5a715-151">**外**</span><span class="sxs-lookup"><span data-stu-id="5a715-151">**Other**</span></span>

<span data-ttu-id="5a715-152">代わりに、他のタイプのソースを追加するために **TalentSource** 列挙を拡張できます。</span><span class="sxs-lookup"><span data-stu-id="5a715-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
