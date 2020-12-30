---
title: Dynamics 365 Talent - Core HR (2018 年 9 月 17 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
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
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 20d3da65028b455ab1602e3a8b443ea7e585b1f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461782"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-17-2018"></a><span data-ttu-id="3e406-103">Dynamics 365 Talent - Core HR (2018 年 9 月 17 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="3e406-103">What's new or changed in Dynamics 365 Talent - Core HR (September 17, 2018)</span></span>

<span data-ttu-id="3e406-104">**ビルド 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="3e406-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="3e406-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="3e406-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="3e406-106">休暇と欠勤 – 作業時間に基づく見越計上時間</span><span class="sxs-lookup"><span data-stu-id="3e406-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="3e406-107">新しい見越計上タイプが休暇計画に追加されました。</span><span class="sxs-lookup"><span data-stu-id="3e406-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="3e406-108">見越計上スケジュールは、勤続月数または作業時間に基づくようになりました。</span><span class="sxs-lookup"><span data-stu-id="3e406-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="3e406-109">詳細については、[作業時間に基づいて休暇を見越計上する](leave-accrue-hours-worked.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e406-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18-for-finance-and-operations"></a><span data-ttu-id="3e406-110">Finance and Operations のプラットフォーム更新プログラム 18</span><span class="sxs-lookup"><span data-stu-id="3e406-110">Platform update 18 for Finance and Operations</span></span>

<span data-ttu-id="3e406-111">Finance and Operations のプラットフォーム更新プログラム 18 は Talent リリースの一部になりました。</span><span class="sxs-lookup"><span data-stu-id="3e406-111">Platform update 18 for Finance and Operations is now part of the Talent release.</span></span> 

-   <span data-ttu-id="3e406-112">必須フィールドおよびその他のフィールドは、個人用設定により非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3e406-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="3e406-113">これによりユーザーは、ビジネス ロジックにより既定に設定されている必須フィールドが表示されない、簡略化された経験を作成できます。</span><span class="sxs-lookup"><span data-stu-id="3e406-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="3e406-114">非表示の必須フィールドは、保存しようとするときに空の場合には一時的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3e406-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="3e406-115">Finance and Operations のプラットフォーム更新プログラム 18 では、Talent Web クライアントは Microsoft Fluent Design とのビジュアルに対応するようになります。</span><span class="sxs-lookup"><span data-stu-id="3e406-115">In Platform update 18 for Finance and Operations, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="3e406-116">フィールドが “読み取りモード“ である場合、単にフィールドで編集オプションを選択して、編集するフォームを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="3e406-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="3e406-117">読み取りモードでのフィールドの表示方法を変更します。</span><span class="sxs-lookup"><span data-stu-id="3e406-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="3e406-118">ワークスペースとページのヘッダーは太字です。</span><span class="sxs-lookup"><span data-stu-id="3e406-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="3e406-119">非置き換えルックアップの動作が改良されました。</span><span class="sxs-lookup"><span data-stu-id="3e406-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="3e406-120">詳細については、[非置き換えルックアップの動作の改良](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/non-replacing-lookups) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e406-120">For more information, see [Improved behavior for non-replacing lookups](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/non-replacing-lookups).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="3e406-121">バグ修正</span><span class="sxs-lookup"><span data-stu-id="3e406-121">Bug fixes</span></span>

<span data-ttu-id="3e406-122">このリリースには ACA、ADA、および I9 への参照を含むいくつかの追加のバグ修正が含まれ、米国企業でのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="3e406-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
