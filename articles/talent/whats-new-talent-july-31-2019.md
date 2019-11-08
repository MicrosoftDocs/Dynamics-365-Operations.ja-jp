---
title: Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 30 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 07/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 3676a0a1fa77285d0203e8e49725cb1c1b742d39
ms.sourcegitcommit: 029c1882bef558b6a45843548e94ab8369ed9870
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2019
ms.locfileid: "2651714"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-30-2019"></a><span data-ttu-id="31981-103">Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 30 日)</span><span class="sxs-lookup"><span data-stu-id="31981-103">What's new or changed in Dynamics 365 Talent (July 30, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="31981-104">このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="31981-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="31981-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="31981-105">Changes in Attract</span></span>
<span data-ttu-id="31981-106">今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31981-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="31981-107">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="31981-107">Changes in Onboard</span></span>
<span data-ttu-id="31981-108">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31981-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="31981-109">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="31981-109">Changes in Core HR</span></span>
<span data-ttu-id="31981-110">このセクションに記載された変更は、ビルド番号 8.1.2409 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="31981-110">Changes described in this section apply to build number 8.1.2409.</span></span>


### <a name="region-support-for-canada-and-southeast-asia"></a><span data-ttu-id="31981-111">カナダおよび東南アジアの地域サポート</span><span class="sxs-lookup"><span data-stu-id="31981-111">Region support for Canada and Southeast Asia</span></span>

<span data-ttu-id="31981-112">2019 年 8 月 1 日に、カナダおよび東南アジアの地域で Talent が使用可能になることをお知らせします。</span><span class="sxs-lookup"><span data-stu-id="31981-112">We are pleased to announce that Canada and Southeast Asia regions will be available for Talent on August 1, 2019.</span></span> <span data-ttu-id="31981-113">この変更により、カナダおよびアジアの地域で環境を作成できるようになり、それらの場所だけですべての Talent データが管理されるようになります。</span><span class="sxs-lookup"><span data-stu-id="31981-113">With this change, you can create environments in the Canadian and Asian regions, and all Talent data will be maintained solely within those locations.</span></span> <span data-ttu-id="31981-114">新しい環境ダイアログで場所を選択し、[Talent のプロビジョニング](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) で説明されているように、その環境を LCS での Talent のプロビジョニングに使用することにより、新しい地域に環境を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="31981-114">You can create an environment in these new regions by selecting the location in the New Environment dialog and use that environment to provision Talent in LCS as described in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="31981-115">他の地域からカナダおよびアジア地域への既存のプロジェクトのデータ移行はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="31981-115">Data migration of existing projects from other regions to the Canadian and Asian regions is not supported.</span></span> <span data-ttu-id="31981-116">新しいプロジェクトのみ、これら新しくサポートされる地域にプロビジョニングできます。</span><span class="sxs-lookup"><span data-stu-id="31981-116">Only new projects can be provisioned to these new supported regions.</span></span>

### <a name="new-active-positions-list-page"></a><span data-ttu-id="31981-117">新しい有効な職位のリスト ページ</span><span class="sxs-lookup"><span data-stu-id="31981-117">New Active positions list page</span></span>

<span data-ttu-id="31981-118">職位に基づくリストのオプションには、**すべての職位**、**有効な職位**、**空いている職位**、および**無効な職位**が含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="31981-118">The options for position-based lists now include: **All positions**, **Active positions**, **Open positions**, and **Inactive positions**.</span></span> <span data-ttu-id="31981-119">新しい**有効な職位**のリスト ページには、現在の日付の時点で有効になっている職位 (オープンまたは入力済み) のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="31981-119">The new **Active positions** list page displays only those positions, open or filled, that are active as of the current date.</span></span> 

### <a name="allow-course-participants-to-be-added-to-open-courses"></a><span data-ttu-id="31981-120">コース参加者の空きのあるコースへの追加を許可する</span><span class="sxs-lookup"><span data-stu-id="31981-120">Allow course participants to be added to open courses</span></span>

<span data-ttu-id="31981-121">今週の変更により、直属の部下のみを空きのあるコースに登録できるという問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="31981-121">This week's changes correct an issue where only direct reports can be registered for open courses.</span></span>

### <a name="fte-analysis-displaying-incorrect-fte-number"></a><span data-ttu-id="31981-122">FTE 分析で正しくない FTE 番号が表示される</span><span class="sxs-lookup"><span data-stu-id="31981-122">FTE Analysis displaying incorrect FTE number</span></span>

<span data-ttu-id="31981-123">**FTE 分析**は、**人事管理**の**分析**タブで修正されました。</span><span class="sxs-lookup"><span data-stu-id="31981-123">**FTE analysis** has been corrected on the **Analytics** tab for **Personnel management**.</span></span>

### <a name="final-comments-label-translation"></a><span data-ttu-id="31981-124">最終コメント ラベルの翻訳</span><span class="sxs-lookup"><span data-stu-id="31981-124">Final comments label translation</span></span>

<span data-ttu-id="31981-125">**最終コメント** ラベルが確認フォームで翻訳されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="31981-125">The **Final comments** label is now translated in the review form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="31981-126">プレビュー</span><span class="sxs-lookup"><span data-stu-id="31981-126">In preview</span></span>

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a><span data-ttu-id="31981-127">プレビュー機能は、サンドボックス インスタンスでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="31981-127">Preview features are enabled only in sandbox instances</span></span>

<span data-ttu-id="31981-128">Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを**実稼働**または**サンドボックス**のどちらかに指定することができます。</span><span class="sxs-lookup"><span data-stu-id="31981-128">When you provision a new instance of Talent, you can specify whether the instance type is **Production** or **Sandbox**.</span></span> <span data-ttu-id="31981-129">**サンドボックス** タイプのインスタンスにより、新機能を事前にテストできるようになります。</span><span class="sxs-lookup"><span data-stu-id="31981-129">Instances of the **Sandbox** type allow for early testing of new features.</span></span> <span data-ttu-id="31981-130">既存の Talent のインスタンスすべては、**実稼働**インスタンス タイプに更新されます。</span><span class="sxs-lookup"><span data-stu-id="31981-130">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="31981-131">既存のインスタンスのいずれかを**サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) に連絡してください。</span><span class="sxs-lookup"><span data-stu-id="31981-131">If you want one of your existing instances to be updated to the **Sandbox** instance type, contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

<span data-ttu-id="31981-132">変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31981-132">For more information about how changes are published, see [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

### <a name="view-extended-information-for-performance-in-manager-self-service"></a><span data-ttu-id="31981-133">マネージャー セルフサービスの業績に関する追加情報の確認</span><span class="sxs-lookup"><span data-stu-id="31981-133">View extended information for performance in manager self-service</span></span>

<span data-ttu-id="31981-134">新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="31981-134">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="31981-135">現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行をすることができます。</span><span class="sxs-lookup"><span data-stu-id="31981-135">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="31981-136">また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスを確実に、スムーズに行うことができます。</span><span class="sxs-lookup"><span data-stu-id="31981-136">In addition, direct managers and their employees can maintain and update performance journals to help ensure that the performance review process goes smoothly.</span></span> <span data-ttu-id="31981-137">この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="31981-137">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>
