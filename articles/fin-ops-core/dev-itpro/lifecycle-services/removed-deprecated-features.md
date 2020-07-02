---
title: Lifecycle Services (LCS) の削除済み、または非推奨の機能
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) から削除された、または削除される予定の機能について説明します。
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e571cc26f55e0bd7a1eef301e193921e0b3f8e31
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454698"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="92f4c-103">Lifecycle Services (LCS) の削除済み、または非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="92f4c-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="92f4c-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) の削除済み、または非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="92f4c-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="92f4c-105">*削除された*フィーチャーはサービスではもう使用できません。</span><span class="sxs-lookup"><span data-stu-id="92f4c-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="92f4c-106">*非推奨* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="92f4c-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="92f4c-107">このリストは、自身の計画を立てる際に、これらの削除や非推奨を検討できるように提供されます。</span><span class="sxs-lookup"><span data-stu-id="92f4c-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="92f4c-108">2019 年 10 月の発表</span><span class="sxs-lookup"><span data-stu-id="92f4c-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="92f4c-109">ビジネス プロセス モデラーのフローチャートの図</span><span class="sxs-lookup"><span data-stu-id="92f4c-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="92f4c-110"><strong>廃止 / 削除の理由</strong></span><span class="sxs-lookup"><span data-stu-id="92f4c-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="92f4c-111">レガシ デザインによって使用率が低くなったため、ビジネス プロセス モデラ― (BPM) のフローチャート図コンポーネントを廃止しています。</span><span class="sxs-lookup"><span data-stu-id="92f4c-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92f4c-112"><strong>別の機能での置き換え?</strong></span><span class="sxs-lookup"><span data-stu-id="92f4c-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="92f4c-113">いいえ</span><span class="sxs-lookup"><span data-stu-id="92f4c-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92f4c-114"><strong>影響を受ける領域</strong></span><span class="sxs-lookup"><span data-stu-id="92f4c-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="92f4c-115">ビジネス プロセス モデラー</span><span class="sxs-lookup"><span data-stu-id="92f4c-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92f4c-116"><strong>ステータス</strong></span><span class="sxs-lookup"><span data-stu-id="92f4c-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="92f4c-117">非推奨: BPM のフローチャート図コンポーネントは、2020 年に削除されることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="92f4c-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="92f4c-118">次の機能は削除されます:</span><span class="sxs-lookup"><span data-stu-id="92f4c-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="92f4c-119">すべてのフローチャートは読み取り専用で、編集できません。</span><span class="sxs-lookup"><span data-stu-id="92f4c-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="92f4c-120">フローチャート活動に関連付けられているシェイプ プロパティも使用できません。</span><span class="sxs-lookup"><span data-stu-id="92f4c-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="92f4c-121">これらのフローチャートには、自動生成される既定のフローチャートと、既定のフローチャートに基づいて変更されるカスタマイズ フローチャートの両方が含まれます。</span><span class="sxs-lookup"><span data-stu-id="92f4c-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="92f4c-122">このプロセス ステップは読み取り専用で、編集できません。</span><span class="sxs-lookup"><span data-stu-id="92f4c-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="92f4c-123">レガシ フィット/ギャップ分析機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="92f4c-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="92f4c-124">したがって、ギャップ リストは自動的に作成されず、エクスポートすることもできません。</span><span class="sxs-lookup"><span data-stu-id="92f4c-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="92f4c-125"><strong>注記:</strong>この機能は以前に廃止され、Microsoft Azure DevOps 統合によって置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="92f4c-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="92f4c-126">フローチャートのバージョン履歴は使用できません。</span><span class="sxs-lookup"><span data-stu-id="92f4c-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
