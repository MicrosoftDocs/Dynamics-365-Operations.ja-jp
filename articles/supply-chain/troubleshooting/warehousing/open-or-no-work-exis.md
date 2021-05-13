---
title: 作業が未完了または不足しているため、出荷を確認できない
description: 作業が未完了または不足しているため、出荷を確認できない
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938505"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="62084-103">作業が未完了または不足しているため、出荷を確認できない</span><span class="sxs-lookup"><span data-stu-id="62084-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="62084-104">エラーコード: WAX515</span><span class="sxs-lookup"><span data-stu-id="62084-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="62084-105">現象</span><span class="sxs-lookup"><span data-stu-id="62084-105">Symptoms</span></span>

<span data-ttu-id="62084-106">出荷を確認しようとすると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="62084-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="62084-107">積荷 %1 の出荷を確定できませんでした。積荷のすべての作業を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62084-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="62084-108">したがって、積荷の出荷を確認できません。</span><span class="sxs-lookup"><span data-stu-id="62084-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="62084-109">原因</span><span class="sxs-lookup"><span data-stu-id="62084-109">Cause</span></span>

<span data-ttu-id="62084-110">積荷または出荷は現在、出荷確認に失敗した状態になっています。</span><span class="sxs-lookup"><span data-stu-id="62084-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="62084-111">出荷を確認する前に、少なくとも積荷の一部の作業が存在し、そのすべての作業の状態が *終了済* または *キャンセル済* である必要があります。</span><span class="sxs-lookup"><span data-stu-id="62084-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="62084-112">解像度</span><span class="sxs-lookup"><span data-stu-id="62084-112">Resolution</span></span>

<span data-ttu-id="62084-113">積荷または出荷に対して関連する販売注文または移動オーダーを確認し、関連作業がすべて完了またはキャンセルされたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="62084-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="62084-114">複数のページで出荷と積荷を処理できます。</span><span class="sxs-lookup"><span data-stu-id="62084-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="62084-115">次のサブセクションでは、いくつかの例を示します。</span><span class="sxs-lookup"><span data-stu-id="62084-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="62084-116">すべての積荷ページ</span><span class="sxs-lookup"><span data-stu-id="62084-116">All loads page</span></span>

1. <span data-ttu-id="62084-117">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="62084-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="62084-118">発送が確認できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="62084-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="62084-119">アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62084-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="62084-120">各作業 ID の状態を検査します。</span><span class="sxs-lookup"><span data-stu-id="62084-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="62084-121">状態が *終了済* または *キャンセル済* でない各作業 ID をフォローアップします。</span><span class="sxs-lookup"><span data-stu-id="62084-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="62084-122">すべての作業 ID の状態が *終了済* または *キャンセル済* である場合は、もう一度やり直して出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="62084-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="62084-123">すべての出荷ページ</span><span class="sxs-lookup"><span data-stu-id="62084-123">All shipments page</span></span>

1. <span data-ttu-id="62084-124">**倉庫管理 \> 出荷 \> すべての出荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="62084-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="62084-125">確認できない出荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="62084-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="62084-126">アクション ウィンドウの **出荷** タブの、**作業** グループで、**作業詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62084-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="62084-127">各作業 ID の状態を検査します。</span><span class="sxs-lookup"><span data-stu-id="62084-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="62084-128">状態が *終了済* または *キャンセル済* でない各作業 ID をフォローアップします。</span><span class="sxs-lookup"><span data-stu-id="62084-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="62084-129">すべての作業 ID の状態が *終了済* または *キャンセル済* である場合は、もう一度やり直して出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="62084-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="62084-130">すべての作業ページ</span><span class="sxs-lookup"><span data-stu-id="62084-130">All work page</span></span>

1. <span data-ttu-id="62084-131">**倉庫管理 \> 作業 \> すべての作業** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="62084-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="62084-132">出荷を確認できない注文番号の作業を選択します。</span><span class="sxs-lookup"><span data-stu-id="62084-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="62084-133">アクション ウィンドウの **出荷** タブの、**出荷** グループで、**出荷の確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62084-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="62084-134">各作業 ID の状態を検査します。</span><span class="sxs-lookup"><span data-stu-id="62084-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="62084-135">状態が *終了済* または *キャンセル済* でない各作業 ID をフォローアップします。</span><span class="sxs-lookup"><span data-stu-id="62084-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="62084-136">すべての作業 ID の状態が *終了済* または *キャンセル済* である場合は、もう一度やり直して出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="62084-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
