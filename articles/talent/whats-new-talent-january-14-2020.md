---
title: Dynamics 365 Talent (2020 年 1 月 14 日) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/14/2020
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
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4992b42bae5edac0f588f08cd6b47ac2795f4c5d
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974479"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-14-2020"></a><span data-ttu-id="8e47e-103">Dynamics 365 Talent (2020 年 1 月 14 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="8e47e-103">What's new or changed in Dynamics 365 Talent (January 14, 2020)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e47e-104">この記事では、Dynamics 365 Talent の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8e47e-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="8e47e-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="8e47e-105">Changes in Attract</span></span>

<span data-ttu-id="8e47e-106">今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8e47e-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="8e47e-107">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="8e47e-107">Changes in Onboard</span></span>

<span data-ttu-id="8e47e-108">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8e47e-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="8e47e-109">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="8e47e-109">Changes in Core HR</span></span>

<span data-ttu-id="8e47e-110">このセクションに記載された変更は、ビルド番号 8.1.2709 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="8e47e-110">Changes described in this section apply to build number 8.1.2709.</span></span> <span data-ttu-id="8e47e-111">ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="8e47e-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="system-unable-to-generate-calendar-days-when-importing-through-data-management-framework-381195"></a><span data-ttu-id="8e47e-112">データ管理フレームワーク経由のインポート時に、システムでカレンダー日を生成できない (381195)</span><span class="sxs-lookup"><span data-stu-id="8e47e-112">System unable to generate calendar days when importing through Data Management Framework (381195)</span></span>

<span data-ttu-id="8e47e-113">この変更により、カレンダー日をインポートするとエラー**無効な日付形式**が生成される問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="8e47e-113">This change corrects an issue where importing calendar days generates the error **Invalid date format**.</span></span> <span data-ttu-id="8e47e-114">このエラーが発生すると、作業カレンダー日単位明細行は作成されません。</span><span class="sxs-lookup"><span data-stu-id="8e47e-114">This error prevents the creation of work calendar date lines.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="8e47e-115">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="8e47e-115">Coming soon</span></span>

<span data-ttu-id="8e47e-116">次の変更により、新しい Common Data Service ソリューションがまもなく利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="8e47e-116">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="8e47e-117">説明</span><span class="sxs-lookup"><span data-stu-id="8e47e-117">Description</span></span> | <span data-ttu-id="8e47e-118">計上額</span><span class="sxs-lookup"><span data-stu-id="8e47e-118">Change</span></span> |
| --- | --- |
| <span data-ttu-id="8e47e-119">**職務/職位**エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="8e47e-119">**Job/Position** entity changes</span></span> | <ul><li><span data-ttu-id="8e47e-120">追加された**報酬地域**</span><span class="sxs-lookup"><span data-stu-id="8e47e-120">**Compensation region** added</span></span></li><li><span data-ttu-id="8e47e-121">追加された**財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="8e47e-121">**Financial dimensions** added</span></span></li></ul> |
| <span data-ttu-id="8e47e-122">**作業者**エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="8e47e-122">**Worker** entity changes</span></span> | <ul><li><span data-ttu-id="8e47e-123">追加された**名前の順序**</span><span class="sxs-lookup"><span data-stu-id="8e47e-123">**Name sequence** added</span></span></li><li><span data-ttu-id="8e47e-124">追加された**自宅から作業**</span><span class="sxs-lookup"><span data-stu-id="8e47e-124">**Works from home** added</span></span></li><li><span data-ttu-id="8e47e-125">追加された**言語**</span><span class="sxs-lookup"><span data-stu-id="8e47e-125">**Language** added</span></span></li><li><span data-ttu-id="8e47e-126">追加された**勤続日数**</span><span class="sxs-lookup"><span data-stu-id="8e47e-126">**Seniority date** added</span></span></li><li><span data-ttu-id="8e47e-127">追加された**記念日**</span><span class="sxs-lookup"><span data-stu-id="8e47e-127">**Anniversary date** added</span></span></li><li><span data-ttu-id="8e47e-128">追加された**元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="8e47e-128">**Original hire date** added</span></span></li></ul> |
| <span data-ttu-id="8e47e-129">**雇用**エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="8e47e-129">**Employment** entity changes</span></span> | <ul><li><span data-ttu-id="8e47e-130">追加された**財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="8e47e-130">**Financial dimensions** added</span></span></li><li><span data-ttu-id="8e47e-131">追加された**退職理由**</span><span class="sxs-lookup"><span data-stu-id="8e47e-131">**Termination reason** added</span></span></li><li><span data-ttu-id="8e47e-132">**移行日**から名前変更された**退職日**</span><span class="sxs-lookup"><span data-stu-id="8e47e-132">**Termination date** renamed from **Transition date**</span></span></li><li><span data-ttu-id="8e47e-133">追加された**猶予期間**</span><span class="sxs-lookup"><span data-stu-id="8e47e-133">**Probation date** added</span></span></li></ul> |
| <span data-ttu-id="8e47e-134">**作業者住所**エンティティの変更</span><span class="sxs-lookup"><span data-stu-id="8e47e-134">**Worker address** entity changes</span></span> | <ul><li><span data-ttu-id="8e47e-135">追加された**番地**</span><span class="sxs-lookup"><span data-stu-id="8e47e-135">**Street address** added</span></span></li><li><span data-ttu-id="8e47e-136">廃止としてマークされた**住所行 1**、**住所行 2**、および**住所行 3**</span><span class="sxs-lookup"><span data-stu-id="8e47e-136">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span></li></ul> |
| <span data-ttu-id="8e47e-137">新しい変動報酬の設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="8e47e-137">New variable compensation setup entities</span></span> | <ul><li><span data-ttu-id="8e47e-138">**変動報酬プラン タイプ**</span><span class="sxs-lookup"><span data-stu-id="8e47e-138">**Compensation variable plan type**</span></span></li><li><span data-ttu-id="8e47e-139">**変動報酬プラン**</span><span class="sxs-lookup"><span data-stu-id="8e47e-139">**Compensation variable plan**</span></span></li><li><span data-ttu-id="8e47e-140">**給付ルール**</span><span class="sxs-lookup"><span data-stu-id="8e47e-140">**Vesting rules**</span></span></li><li><span data-ttu-id="8e47e-141">**変動報酬プラン レベル**</span><span class="sxs-lookup"><span data-stu-id="8e47e-141">**Compensation variable plan level**</span></span></li></ul> |
| <span data-ttu-id="8e47e-142">新しい**作業者カレンダー雇用**エンティティ</span><span class="sxs-lookup"><span data-stu-id="8e47e-142">New **Worker calender employment** entity</span></span> | <ul><li><span data-ttu-id="8e47e-143">追加された**作業カレンダー エンティティ**</span><span class="sxs-lookup"><span data-stu-id="8e47e-143">**Work calendar entity** added</span></span></li></ul> |
