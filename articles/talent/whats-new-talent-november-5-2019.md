---
title: Dynamics 365 Talent (2019 年 11 月 5 日) の新機能または変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a81209c3c4a95ee51668533d40d4aecc1d58b9
ms.sourcegitcommit: a46fb06138f7f82e973dca3157d30f9b21d3a70b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778385"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a><span data-ttu-id="02e23-103">Dynamics 365 Talent (2019 年 11 月 5 日) の新機能または変更された機能</span><span class="sxs-lookup"><span data-stu-id="02e23-103">What's new or changed in Dynamics 365 Talent (November 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="02e23-104">このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="02e23-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="02e23-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="02e23-105">Changes in Attract</span></span>

<span data-ttu-id="02e23-106">今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02e23-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="02e23-107">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="02e23-107">Changes in Onboard</span></span>

<span data-ttu-id="02e23-108">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02e23-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="02e23-109">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="02e23-109">Changes in Core HR</span></span>

<span data-ttu-id="02e23-110">このセクションに記載された変更は、ビルド番号 8.1.2598 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="02e23-110">Changes described in this section apply to build number 8.1.2598.</span></span> <span data-ttu-id="02e23-111">ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="02e23-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="copy-a-core-hr-instance"></a><span data-ttu-id="02e23-112">Core HR インスタンスのコピー</span><span class="sxs-lookup"><span data-stu-id="02e23-112">Copy a Core HR instance</span></span>

<span data-ttu-id="02e23-113">今週のリリースでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics 365 Talent: Core HR のデータベースをサンドボックス環境にコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="02e23-113">In this week's release, you can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Talent: Core HR database to a sandbox environment.</span></span> <span data-ttu-id="02e23-114">別のサンドボックス環境を使用する場合は、その環境から対象のサンドボックス環境にデータベースをコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="02e23-114">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span> <span data-ttu-id="02e23-115">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02e23-115">For more information, see:</span></span>

- <span data-ttu-id="02e23-116">Dynamics 365: 2019 リリース ウェーブ 2 プランの、[より広範な環境管理](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management)</span><span class="sxs-lookup"><span data-stu-id="02e23-116">[Broader environment management](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) in the Dynamics 365: 2019 release wave 2 plan</span></span>

- <span data-ttu-id="02e23-117">Talent のドキュメントに、[Core HR インスタンスをコピー](hr-copy-instance.md)</span><span class="sxs-lookup"><span data-stu-id="02e23-117">[Copy a Core HR instance](hr-copy-instance.md) in Talent documentation</span></span>

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a><span data-ttu-id="02e23-118">Common Data Service 統合が有効になっている場合、Common Data Service統合バッチ ジョブが作成されない (388030)</span><span class="sxs-lookup"><span data-stu-id="02e23-118">Common Data Service integration batch jobs aren't created when Common Data Service integration is enabled (388030)</span></span>

<span data-ttu-id="02e23-119">この変更により、有効になったときに、Common Data Service 統合のバッチ ジョブが作成されます。</span><span class="sxs-lookup"><span data-stu-id="02e23-119">This change will create batch jobs for Common Data Service integration when it's enabled.</span></span>

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a><span data-ttu-id="02e23-120">HcmPersonImageEntity でアップロード時に従業員の画像サイズが変更されない (369469)</span><span class="sxs-lookup"><span data-stu-id="02e23-120">The HcmPersonImageEntity doesn't resize the person image when uploaded (369469)</span></span>

<span data-ttu-id="02e23-121">今週のリリースにより、パフォーマンス向上のため、データ管理を使用してインポートした際、画像サイズの変更方法が変わりました。</span><span class="sxs-lookup"><span data-stu-id="02e23-121">This week's release changes how images are resized for better performance when imported through data management.</span></span>

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a><span data-ttu-id="02e23-122">職位の割り当て可能日が、有効化した日より以前になることがある (340103)</span><span class="sxs-lookup"><span data-stu-id="02e23-122">A position's Available for assignment date can be earlier than the Activation date (340103)</span></span>

<span data-ttu-id="02e23-123">この変更により、職位が**有効化した日**より以前に**割り当て可能日**を選択した場合に警告が表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="02e23-123">With this change, a warning will appear if you select an **Available for assignment date** that's earlier than the position's **Activation date**.</span></span>

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a><span data-ttu-id="02e23-124">ステップベースの計画では従業員セルフサービスで報酬変更要求を作成できない (376872)</span><span class="sxs-lookup"><span data-stu-id="02e23-124">Can't create a compensation change request in employee self-service for step-based plans (376872)</span></span>

<span data-ttu-id="02e23-125">このリリースにより、ステップベースの計画で従業員セルフサービスを使用して報酬の変更を要求する場合に発生する問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="02e23-125">This release corrects an issue when requesting compensation changes through employee self-service for step-based plans.</span></span> 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a><span data-ttu-id="02e23-126">説明が 30 文字 (Core HR では 60 文字) を超えている場合、理由コードが Common Data Service に同期されない (352682)</span><span class="sxs-lookup"><span data-stu-id="02e23-126">Reason code doesn't sync to Common Data Service if the description is longer than 30 characters, Core HR allows 60 (352682)</span></span>

<span data-ttu-id="02e23-127">この変更により、30 文字を超える理由コードが Common Data Service で更新されます。</span><span class="sxs-lookup"><span data-stu-id="02e23-127">with this change, reason codes with more than 30 characters will be updated in Common Data Service.</span></span> <span data-ttu-id="02e23-128">Common Data Service で行われた変更は、Talent にも反映されます。</span><span class="sxs-lookup"><span data-stu-id="02e23-128">Changes made in Common Data Service will also be reflected back in Talent.</span></span>

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a><span data-ttu-id="02e23-129">Talent から Finance and Operations への住所統合 (351961)</span><span class="sxs-lookup"><span data-stu-id="02e23-129">Address integration from Talent to Finance and Operations (351961)</span></span>

<span data-ttu-id="02e23-130">このリリースにより、Talent で更新された住所が Finance and Operations では更新されないという問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="02e23-130">This release fixes an issue where addresses updated in Talent weren't updating in Finance and Operations.</span></span> <span data-ttu-id="02e23-131">住所のブロックに対する変更が更新されます。</span><span class="sxs-lookup"><span data-stu-id="02e23-131">Changes to address blocks will now update.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="02e23-132">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="02e23-132">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="02e23-133">業績の確認の印刷</span><span class="sxs-lookup"><span data-stu-id="02e23-133">Print performance reviews</span></span>

<span data-ttu-id="02e23-134">詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02e23-134">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="02e23-135">機能管理ワークスペース</span><span class="sxs-lookup"><span data-stu-id="02e23-135">Feature management workspace</span></span>

<span data-ttu-id="02e23-136">機能は、すべてのリリースで追加および更新されます</span><span class="sxs-lookup"><span data-stu-id="02e23-136">Features are added and updated in every release.</span></span> <span data-ttu-id="02e23-137">機能管理エクスペリエンスは、各リリースで提供されている機能のリストを表示できるワークスペースを提供します。</span><span class="sxs-lookup"><span data-stu-id="02e23-137">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="02e23-138">既定では、新機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="02e23-138">By default, new features are turned off.</span></span> <span data-ttu-id="02e23-139">ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。</span><span class="sxs-lookup"><span data-stu-id="02e23-139">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="02e23-140">機能管理に伴う変更の詳細については、[機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02e23-140">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
