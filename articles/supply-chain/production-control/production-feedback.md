---
title: "生産フィードバック"
description: "この記事は、作業者に生産ジョブに関するフィードバックを与える生産フィードバックに関する情報を提供します。 この記事には、生産フィードバックを更新するさまざまな方法に関する情報が含まれます。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1086852bd5193d70e9bde69d349a8d787deee094
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="production-feedback"></a><span data-ttu-id="c8520-104">生産フィードバック</span><span class="sxs-lookup"><span data-stu-id="c8520-104">Production feedback</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c8520-105">この記事は、作業者に生産ジョブに関するフィードバックを与える生産フィードバックに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c8520-105">This article provides information about production feedback, which gives workers feedback about production jobs.</span></span> <span data-ttu-id="c8520-106">この記事には、生産フィードバックを更新するさまざまな方法に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c8520-106">The article includes information about the various ways that production feedback can be updated.</span></span>

<span data-ttu-id="c8520-107">生産フィードバックは、作業者に、生産ジョブに関するフィードバックを提供します。</span><span class="sxs-lookup"><span data-stu-id="c8520-107">Production feedback gives workers feedback about production jobs.</span></span> <span data-ttu-id="c8520-108">製造オーダーの時間や材料消費、工程の数量および状態、ジョブや工程の失敗原因になったエラーを記録しています。</span><span class="sxs-lookup"><span data-stu-id="c8520-108">It records time and material consumption on production orders, operation quantities and status, and errors that cause a job or operation to fail.</span></span> <span data-ttu-id="c8520-109">生産フィードバックは、製造オーダーに関連付けられた仕訳帳で更新できます。</span><span class="sxs-lookup"><span data-stu-id="c8520-109">Production feedback can be updated in journals that are related to production orders.</span></span> <span data-ttu-id="c8520-110">**生産ジョブ カード**と**生産工順カード**の仕訳帳を使用して、ジョブや工程ごとの時間と数量を報告することができます。</span><span class="sxs-lookup"><span data-stu-id="c8520-110">The **Production job card** and **Production route card** journals are used to report time and quantities per job or operation.</span></span> <span data-ttu-id="c8520-111">最後のジョブまたは工程に関するレポートで、完成品の数量を完了として報告できます。</span><span class="sxs-lookup"><span data-stu-id="c8520-111">For reporting about the last job or operation, quantities on the finished product can be reported as finished.</span></span> <span data-ttu-id="c8520-112">生産フィードバックは、**ジョブ カード ターミナル** ページと**ジョブ カードのデバイス** ページで更新できます。</span><span class="sxs-lookup"><span data-stu-id="c8520-112">Production feedback can also be updated on the **Job card terminal** and **Job card device** pages.</span></span> <span data-ttu-id="c8520-113">これらのページは、作業現場での生産フィードバックの更新を有効にして、**生産管理**モジュールの製造実行の機能の一部となります。</span><span class="sxs-lookup"><span data-stu-id="c8520-113">These pages enable production feedback to be updated on the shop floor and are part of the manufacturing execution functionality in the **Production control** module.</span></span> <span data-ttu-id="c8520-114">**ジョブ カード ターミナル** ページには、コンフィギュレーション可能なユーザー インターフェイスがあり、選択した作業領域について、リリースされたジョブの一覧を優先付けされた順序で表示できます。</span><span class="sxs-lookup"><span data-stu-id="c8520-114">The **Job card terminal** page has a configurable user interface that shows a list of the released jobs in a prioritized order for a selected work area.</span></span> <span data-ttu-id="c8520-115">また、ジョブのバンドル、チーム作業などの詳細オプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="c8520-115">It also offers advanced options such as job bundling and team work.</span></span> <span data-ttu-id="c8520-116">**ジョブ カードのデバイス** ページには、タッチに最適化されたユーザー インターフェイスがあります。</span><span class="sxs-lookup"><span data-stu-id="c8520-116">The **Job card device** page has a touch-optimized user interface.</span></span> <span data-ttu-id="c8520-117">両方のページの生産フィードバックは、生産仕訳帳から更新されます。</span><span class="sxs-lookup"><span data-stu-id="c8520-117">Production feedback on both pages is updated from the production journals.</span></span>




