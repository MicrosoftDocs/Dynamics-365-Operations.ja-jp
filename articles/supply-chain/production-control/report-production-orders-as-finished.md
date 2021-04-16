---
title: 製造オーダーの完了済としての報告
description: 完了レポートは生産ステージです。 この段階では、完成品は製造オーダーから在庫へ報告され、移動されます。
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 533e3e5b3187f45a5f873bd6951dd0df89a88210
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819355"
---
# <a name="report-production-orders-as-finished"></a><span data-ttu-id="8055b-104">製造オーダーの完了済としての報告</span><span class="sxs-lookup"><span data-stu-id="8055b-104">Report production orders as finished</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8055b-105">完了レポートは生産ステージです。</span><span class="sxs-lookup"><span data-stu-id="8055b-105">Report as finished is a production stage.</span></span> <span data-ttu-id="8055b-106">この段階では、完成品は製造オーダーから在庫へ報告され、移動されます。</span><span class="sxs-lookup"><span data-stu-id="8055b-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="8055b-107">製造オーダーで完成品の完了数が完了として報告があると、在庫の手持在庫として更新されます。</span><span class="sxs-lookup"><span data-stu-id="8055b-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="8055b-108">元の計画オーダー数量の一部の数量を完了報告できます。</span><span class="sxs-lookup"><span data-stu-id="8055b-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="8055b-109">数量の完了を報告するときに、関連するエラーとともにエラー数量を報告することもできます。</span><span class="sxs-lookup"><span data-stu-id="8055b-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="8055b-110">製造オーダーが [完了報告済] ステージに達すると、これ以上の数量は製造オーダーで報告されません。</span><span class="sxs-lookup"><span data-stu-id="8055b-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="8055b-111">次の特性は、**完了レポート** プロセスと関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="8055b-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="8055b-112">原材料の消費と、報告済数量 (バック フラッシュ) に比例する時間を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8055b-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="8055b-113">プット アウェイ作業は倉庫プロセスに有効になる品目に対して生成できます。</span><span class="sxs-lookup"><span data-stu-id="8055b-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="8055b-114">完成品の予定または標準原価の値は、勘定科目に報告されるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="8055b-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="8055b-115">品質指示は品質関連の設定に基づいて、報告された数量に対して作成できます。</span><span class="sxs-lookup"><span data-stu-id="8055b-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="8055b-116">数量が出荷場所に報告されます。</span><span class="sxs-lookup"><span data-stu-id="8055b-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="8055b-117">倉庫の作業は、出荷場所からプット アウェイ作業の場所のディレクティブによって定義される最終目的地に数量を移動するために生成されます。</span><span class="sxs-lookup"><span data-stu-id="8055b-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="8055b-118">品質指示は、品質関連が設定されている場合に、製造オーダーの完了報告時に作成できます。</span><span class="sxs-lookup"><span data-stu-id="8055b-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="8055b-119">完了レポートする製造オーダーの設定</span><span class="sxs-lookup"><span data-stu-id="8055b-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="8055b-120">標準の製造オーダー更新機能を使用するか、工順およびジョブ カード仕訳帳か、仕訳帳の **完了レポート** を使用して、製造オーダーのステータスを **完了レポート** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="8055b-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="8055b-121">製造オーダーの最後のジョブを報告するときに、ジョブ カード ターミナル、ジョブ カード デバイスのページを使用してステージを **完了レポート** に更新できます。</span><span class="sxs-lookup"><span data-stu-id="8055b-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="8055b-122">最後に、ハンドヘルド デバイスの倉庫のソリューションのプロセスとして **完了レポート** オプションを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="8055b-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]