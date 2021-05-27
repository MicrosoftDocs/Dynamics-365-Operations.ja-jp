---
title: 不適合の工程
description: このトピックでは、不適合の工程を作成および使用する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022207"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="5e397-103">不適合の工程</span><span class="sxs-lookup"><span data-stu-id="5e397-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e397-104">このトピックでは、不適合の工程を作成および使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e397-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="5e397-105">**工程** ページを使用して、承認済の不適合に対して実行される作業の分類を定義します。</span><span class="sxs-lookup"><span data-stu-id="5e397-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="5e397-106">関連する工程を不適合に割り当てるときに、関連する材料、労働時間、諸経費など、その工程を実行するために必要な詳細を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5e397-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="5e397-107">システムはこの情報を使用して、工程の見積原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="5e397-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="5e397-108">詳細情報および見積原価は、参考目的で提供されます。</span><span class="sxs-lookup"><span data-stu-id="5e397-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="5e397-109">品質に関連する工程は、生産工順に対して定義できる工程とは異なります。</span><span class="sxs-lookup"><span data-stu-id="5e397-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="5e397-110">不適合に関連する行程で使用される原価、時間、および品目を追跡できますが、入力するデータは情報提供にすぎません。</span><span class="sxs-lookup"><span data-stu-id="5e397-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="5e397-111">総勘定元帳、在庫の補助元帳、または **時刻と出勤** モジュールと自動的に統合されません。</span><span class="sxs-lookup"><span data-stu-id="5e397-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="5e397-112">行程の例</span><span class="sxs-lookup"><span data-stu-id="5e397-112">Examples of operations</span></span>

<span data-ttu-id="5e397-113">製造会社に勤務しているとします。</span><span class="sxs-lookup"><span data-stu-id="5e397-113">You work for a manufacturing company.</span></span> <span data-ttu-id="5e397-114">品質テストに合格しなかった品目に対して不適合が作成および承認されました。</span><span class="sxs-lookup"><span data-stu-id="5e397-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="5e397-115">問題が機械のベアリング不良に関連していることを示す修正が作成されました。</span><span class="sxs-lookup"><span data-stu-id="5e397-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="5e397-116">ベアリングを交換するには、いくつかの手順が必要であり、各工程の責任が追跡されます。</span><span class="sxs-lookup"><span data-stu-id="5e397-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="5e397-117">たとえば、次の手順が必要になる場合があります:</span><span class="sxs-lookup"><span data-stu-id="5e397-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="5e397-118">生産ラインが停止され、定期クリーンアウトが実行されます。</span><span class="sxs-lookup"><span data-stu-id="5e397-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="5e397-119">メンテナンス担当者がベアリングを交換します。</span><span class="sxs-lookup"><span data-stu-id="5e397-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="5e397-120">品質保証の担当者は、電源を入れる前に機械を検査します。</span><span class="sxs-lookup"><span data-stu-id="5e397-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="5e397-121">この例では、実行する必要がある作業を表すため次の行程を作成できます:</span><span class="sxs-lookup"><span data-stu-id="5e397-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="5e397-122">生産ラインを停止します。</span><span class="sxs-lookup"><span data-stu-id="5e397-122">Stop the production line.</span></span>
- <span data-ttu-id="5e397-123">生産ラインをクリーンアウトします。</span><span class="sxs-lookup"><span data-stu-id="5e397-123">Clean out the production line.</span></span>
- <span data-ttu-id="5e397-124">機械メンテナンスを実行します。</span><span class="sxs-lookup"><span data-stu-id="5e397-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="5e397-125">機械を検査します。</span><span class="sxs-lookup"><span data-stu-id="5e397-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="5e397-126">行程を作成する</span><span class="sxs-lookup"><span data-stu-id="5e397-126">Create an operation</span></span>

1. <span data-ttu-id="5e397-127">**在庫管理 \> 設定 \> 品質管理 \> 工程** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5e397-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="5e397-128">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="5e397-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5e397-129">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="5e397-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5e397-130">**行程** – 行程の固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e397-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="5e397-131">**説明** – 行程の詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e397-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="5e397-132">**タイプ** – 工程が特定のタイプの注文に関連する不適合でのみ使用できる場合は、注文タイプ (*発注書* または *販売注文*) を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e397-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="5e397-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5e397-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e397-134">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5e397-134">Additional resources</span></span>

- [<span data-ttu-id="5e397-135">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="5e397-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="5e397-136">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="5e397-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="5e397-137">不適合の作成および処理</span><span class="sxs-lookup"><span data-stu-id="5e397-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="5e397-138">不適合の承認を担当する作業者</span><span class="sxs-lookup"><span data-stu-id="5e397-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="5e397-139">不適合の検査ゾーン</span><span class="sxs-lookup"><span data-stu-id="5e397-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="5e397-140">不適合の診断タイプ</span><span class="sxs-lookup"><span data-stu-id="5e397-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="5e397-141">不適合の品質諸費用</span><span class="sxs-lookup"><span data-stu-id="5e397-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="5e397-142">不適合の問題タイプ</span><span class="sxs-lookup"><span data-stu-id="5e397-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="5e397-143">倉庫プロセスに対する品質管理</span><span class="sxs-lookup"><span data-stu-id="5e397-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
