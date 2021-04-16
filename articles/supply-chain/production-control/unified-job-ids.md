---
title: ジョブ ID の統合番号順序
description: この機能により、生産管理、製造の実行、および時間/出席モジュール用のジョブ ID を生成する、単一の統合番号順序が提供されます。
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824945"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="72fed-103">ジョブ ID の統合番号順序</span><span class="sxs-lookup"><span data-stu-id="72fed-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72fed-104">この機能により、生産管理、製造の実行、および時間/出席モジュール用のジョブ ID を生成する、単一の統合番号順序が提供されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="72fed-105">以前は、これらのモジュールごとに異なる番号順序を選択する必要があります。これらの順序の 2 つ以上で同一の形式を使用した場合に、ジョブ ID が競合する場合があります。</span><span class="sxs-lookup"><span data-stu-id="72fed-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="72fed-106">このような競合によってデータが破損する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="72fed-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="72fed-107">システムでこの機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="72fed-107">Turn on this feature for your system</span></span>

<span data-ttu-id="72fed-108">このトピックで説明する機能がシステムにまだ含まれていない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*ジョブ ID の統一された番号シーケンス* 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="72fed-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="72fed-109">ジョブ ID の統合番号シーケンスの設定</span><span class="sxs-lookup"><span data-stu-id="72fed-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="72fed-110">この機能を有効にすると、生産管理、製造の実行、時間/出席モジュールのパラメータ ページにある既存の **ジョブ ID** 番号シーケンス設定は廃止され、新しい **統合ジョブ ID** フィールドが追加されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="72fed-111">**統合ジョブ ID** の値は 3 つのモジュールすべてで共有するため、すべてのモジュールが同じ番号順序 を参照することができます。</span><span class="sxs-lookup"><span data-stu-id="72fed-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="72fed-112">したがって、ジョブ ID は 3 つのモジュールすべてで一意であり、競合は発生しません。</span><span class="sxs-lookup"><span data-stu-id="72fed-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="72fed-113">ジョブ ID の統一番号シーケンスを設定するには:</span><span class="sxs-lookup"><span data-stu-id="72fed-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="72fed-114">前のセクションで説明されている手順に従って機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="72fed-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="72fed-115">統合ジョブの ID に使用する番号順序を識別するか、新しい番号シーケンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="72fed-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="72fed-116">詳細については、[番号順序の概要](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72fed-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="72fed-117">**生産管理パラメータ**、**製造の実行パラメータ**、または **時間と出席 パラメータ** ページに移動 します。</span><span class="sxs-lookup"><span data-stu-id="72fed-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="72fed-118">これらのページでこの設定を行う場合、他のすべてのページが自動的に更新されるので、どちらを選択しても問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="72fed-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="72fed-119">パラメータ ページの **番号シーケンス** タブを開きます。</span><span class="sxs-lookup"><span data-stu-id="72fed-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="72fed-120">前に特定した **番号シーケンスコード** をグリッドの **統合したジョブ ID** 行に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="72fed-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
