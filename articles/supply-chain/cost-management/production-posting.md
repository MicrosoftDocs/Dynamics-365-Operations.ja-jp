---
title: "生産の転記"
description: "この記事は、生産プロセスの、異なるタイプの転記について説明します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 413bf76b40ec1e6d00322605900a71f163c9396c
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="production-posting"></a><span data-ttu-id="8e31e-103">生産の転記</span><span class="sxs-lookup"><span data-stu-id="8e31e-103">Production posting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8e31e-104">この記事は、生産プロセスの、異なるタイプの転記について説明します。</span><span class="sxs-lookup"><span data-stu-id="8e31e-104">This article provides information about different types of postings in the production process.</span></span>

<span data-ttu-id="8e31e-105">生産の転記活動は、次のセクションで説明する生産プロセスの後に行います。</span><span class="sxs-lookup"><span data-stu-id="8e31e-105">Production posting activities follow production processes that are described in the sections below.</span></span>

## <a name="material-consumption"></a><span data-ttu-id="8e31e-106">材料消費量</span><span class="sxs-lookup"><span data-stu-id="8e31e-106">Material consumption</span></span>
<span data-ttu-id="8e31e-107">生産ピッキング リスト仕訳帳の転記時に、材料が生産中に消費されるように登録されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-107">Materials are registered as consumed during production when the production picking list journal is posted.</span></span> <span data-ttu-id="8e31e-108">このプロセスは、手持在庫を差し引く払出トランザクションを生成します。</span><span class="sxs-lookup"><span data-stu-id="8e31e-108">This process generates issue transactions that deduct the on-hand inventory.</span></span> <span data-ttu-id="8e31e-109">生産パラメーターで、処理中の原材料 (仕掛品 \[WIP\]) の値を元帳に転記するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-109">In the production parameters, you can specify whether the value of raw materials that are in progress (work in process \[WIP\]) should be posted in the ledger.</span></span> <span data-ttu-id="8e31e-110">処理中の原材料 (WIP) の値は、専用のピッキング リストの勘定と専用のピッキング リスト相手勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-110">The value of raw materials that are in progress (WIP) is then posted to a dedicated Picking list account and a dedicated Picking list offset account.</span></span>

## <a name="time-consumption"></a><span data-ttu-id="8e31e-111">時間消費量</span><span class="sxs-lookup"><span data-stu-id="8e31e-111">Time consumption</span></span>
<span data-ttu-id="8e31e-112">作業者が生産ジョブに費やした時間は、工順カード仕訳帳またはジョブ カード仕訳帳に記録されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-112">The time that workers spend on production jobs is recorded in the Route card journal or the Job card journal.</span></span> <span data-ttu-id="8e31e-113">これらの仕訳帳を転記すると、処理中のリソース (WIP) の専用アカウントへの元帳転記が処理されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-113">When these journals are posted, ledger posting to a dedicated account for resources that are in progress (WIP) is processed.</span></span> <span data-ttu-id="8e31e-114">この転記は、製造オーダーに費やした時間の値を表します。</span><span class="sxs-lookup"><span data-stu-id="8e31e-114">This posting represents the value of the time that is spent on the production order.</span></span> <span data-ttu-id="8e31e-115">製造オーダーが完了報告されると、仕掛品勘定が決済されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-115">After the production order is registered as ended, the WIP accounts are settled.</span></span>

## <a name="reporting-finished-goods-and-error-quantities"></a><span data-ttu-id="8e31e-116">完成品とエラー数量のレポート</span><span class="sxs-lookup"><span data-stu-id="8e31e-116">Reporting finished goods and error quantities</span></span>
<span data-ttu-id="8e31e-117">製造オーダーが完了済として報告されると、完了した完成品の在庫管理が完了レポート仕訳帳を介して更新されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-117">When a production order is reported as finished, the quantity of the finished goods that have been completed is updated in Inventory management through the Report as finished journal.</span></span> <span data-ttu-id="8e31e-118">生産パラメーターで設定できる仕掛品 (WIP) 会計を使用している場合、WIP 勘定を節約し、完成品在庫を増やすため、元帳兼用仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="8e31e-118">If you're using WIP accounting, which can be set up in the production parameters, a ledger journal is made to reduce the WIP accounts and increase the inventory of the finished goods.</span></span> <span data-ttu-id="8e31e-119">仕訳帳は製品に対して定義されている標準原価を使用します。</span><span class="sxs-lookup"><span data-stu-id="8e31e-119">The journal uses the standard cost that is defined for the product.</span></span>

## <a name="ending-the-production-order"></a><span data-ttu-id="8e31e-120">製造オーダーの終了</span><span class="sxs-lookup"><span data-stu-id="8e31e-120">Ending the production order</span></span>
<span data-ttu-id="8e31e-121">製造オーダーを終了する前に、生産した数量に対して実績原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="8e31e-121">Before a production order is ended, actual costs are calculated for the quantity that was produced.</span></span> <span data-ttu-id="8e31e-122">材料費、労務費、および間接費のすべての見積原価が取り消され、実績原価に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-122">All estimated costs of material, labor, and overhead are reversed and replaced with actual costs.</span></span> <span data-ttu-id="8e31e-123">完成した品目の全体的な原価は、在庫の受入勘定の借方と、在庫の払出勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-123">The overall cost of the finished item is debited from the inventory Receipt account and credited to the inventory Issues account.</span></span> <span data-ttu-id="8e31e-124">原価計算を実行するときに [**終了済**] チェック ボックスをオンにすると、製造オーダーのステータスが [**終了済**] に変更されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-124">If you select the **End job** check box when you run the cost calculation, the status of the production order is changed to **Ended**.</span></span> <span data-ttu-id="8e31e-125">この状態により、完了した製造オーダーに、新たな原価が誤って転記されるのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-125">This status prevents any additional costs from being unintentionally posted to a completed production order.</span></span> <span data-ttu-id="8e31e-126">完了報告時に報告されるエラー数量の値を、完了報告された適正数量に割り当てるように指定することができます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-126">You can specify that the value of error quantities that are reported during reporting as finished should be allocated to the good quantities that are reported as finished.</span></span> <span data-ttu-id="8e31e-127">また、エラー数量の値が専用の仕損勘定に転記する必要があることを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-127">Alternatively, you can specify that the value of error quantities should be posted to a dedicated scrap account.</span></span>

## <a name="controlling-the-level-of-ledger-posting"></a><span data-ttu-id="8e31e-128">元帳転記レベルの制御</span><span class="sxs-lookup"><span data-stu-id="8e31e-128">Controlling the level of ledger posting</span></span>
<span data-ttu-id="8e31e-129">[**生産管理パラメーター**] では、[**元帳転記**] フィールドで生産プロセスの元帳転記のレベルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-129">In the **Production control parameters**, you can use the **Ledger posting** field to set the level of ledger posting for production processes.</span></span> <span data-ttu-id="8e31e-130">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8e31e-130">The following values are available:</span></span>

-   <span data-ttu-id="8e31e-131">[**品目およびリソース**] – 原材料および完成品の品目グループに設定される勘定科目を使用します。</span><span class="sxs-lookup"><span data-stu-id="8e31e-131">**Item and resource** – Use the ledger accounts that are set up on the item groups for raw materials and finished goods.</span></span> <span data-ttu-id="8e31e-132">時間消費のために仕掛品が工順工程のリソースまたはリソース グループから取得されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-132">WIP for time consumption is taken from resource or resource group from the route operations.</span></span>
-   <span data-ttu-id="8e31e-133">[**品目とカテゴリ**] – 原材料および完成品の品目グループに設定される勘定科目を使用します。</span><span class="sxs-lookup"><span data-stu-id="8e31e-133">**Item and category** – Use the ledger accounts that are set up on the item groups for raw materials and finished goods.</span></span> <span data-ttu-id="8e31e-134">時間消費のために仕掛品が工順工程に関連付けられる原価カテゴリから取得されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-134">WIP for time consumption is taken from the cost categories that are associated with the route operations.</span></span>
-   <span data-ttu-id="8e31e-135">[**生産グループ**] – 材料と時間消費の両方の生産グループで設定された勘定科目を使用します。</span><span class="sxs-lookup"><span data-stu-id="8e31e-135">**Production groups** – Use the ledger accounts that are set up on the production groups for both material and time consumption.</span></span> <span data-ttu-id="8e31e-136">生産グループはリリースされた製品に関連付けられ、その注文が作成されると製造オーダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-136">The production groups are associated with the released products and copied to the production orders when those orders are created.</span></span> <span data-ttu-id="8e31e-137">製造オーダーへの転記は、製造オーダーに関連付けられる生産グループに従います。</span><span class="sxs-lookup"><span data-stu-id="8e31e-137">The posting on the production orders will then follow the production groups that are associated with the production order.</span></span>

<span data-ttu-id="8e31e-138">**メモ:** 完成した品目の原価計算に標準の方法が使用された場合は、最終的なトランザクションにも反映されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-138">**Note:** If the standard method for calculating the cost of the finished item was used, the final transactions reflect this fact.</span></span> <span data-ttu-id="8e31e-139">実際原価と標準の方法で計算された原価との間に相違があった場合は、差額が利益または損失を示す勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="8e31e-139">If actual costs and the costs that are calculated by using the standard method differ, the difference is posted to the account that shows profit or loss.</span></span>




