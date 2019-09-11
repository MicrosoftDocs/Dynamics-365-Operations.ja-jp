---
title: 使用品目
description: このトピックでは、資産管理における品目の使用場所の概要の取得方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918329"
---
# <a name="item-where-used"></a><span data-ttu-id="3d70f-103">使用品目</span><span class="sxs-lookup"><span data-stu-id="3d70f-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3d70f-104">特定の品目の計算を行って、資産管理でその品目が使用された場所の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="3d70f-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="3d70f-105">結果は、品目が有効期間中に使用されたコンテキストを示します。</span><span class="sxs-lookup"><span data-stu-id="3d70f-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="3d70f-106">**品目の使用場所**ページは、メインの資産管理メニューから開くことができます。また、次のページからもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3d70f-106">The **Item where used** page can be opened from the main Asset management menu, and it can also be accessed from the following pages:</span></span>

[<span data-ttu-id="3d70f-107">資産 BOM</span><span class="sxs-lookup"><span data-stu-id="3d70f-107">Asset BOM</span></span>](../objects/object-BOM.md)

[<span data-ttu-id="3d70f-108">資産タイプの既定の予備部品</span><span class="sxs-lookup"><span data-stu-id="3d70f-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

[<span data-ttu-id="3d70f-109">メンテナンス作業タイプの既定の予測の品目予測</span><span class="sxs-lookup"><span data-stu-id="3d70f-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[<span data-ttu-id="3d70f-110">作業指示書メンテナンス予測</span><span class="sxs-lookup"><span data-stu-id="3d70f-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

[<span data-ttu-id="3d70f-111">作業指示書購買要求</span><span class="sxs-lookup"><span data-stu-id="3d70f-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

[<span data-ttu-id="3d70f-112">作業指示書の購買</span><span class="sxs-lookup"><span data-stu-id="3d70f-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="3d70f-113">品目の使用場所の計算</span><span class="sxs-lookup"><span data-stu-id="3d70f-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="3d70f-114">**資産管理** > **照会** > **品目の使用場所**をクリックするか、または前に説明したいずれかのページで**品目の使用場所**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70f-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="3d70f-115">**品目の使用場所**ダイアログで、**品目番号**フィールドで計算を実行する品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70f-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="3d70f-116">**レベル** フィールドを使用すると、機能の場所に関する品目明細行の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3d70f-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> <span data-ttu-id="3d70f-117">たとえば、フィールドに「1」という番号を挿入し、複数レベルの機能の場所の構造がある場合、機能の場所に対するすべての品目明細行が最上位レベルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d70f-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="3d70f-118">したがって、明細行の関係または数量が下位レベルにある機能の場所から追加される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3d70f-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="3d70f-119">**レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能の場所レベルのすべての品目明細行を示す詳細結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d70f-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="3d70f-120">**含める**セクションで、計算に含めるトグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70f-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="3d70f-121">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="3d70f-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="3d70f-122">**品目の使用場所**タブ > **グループ化**アクション ウィンドウ グループで、関連するボタンを選択すると、計算の必要な詳細レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d70f-122">On the **Item where used** tab > **Group by...** action pane groups, select the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="3d70f-123">選択したアクション ウィンドウ ボタンが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d70f-123">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="3d70f-124">ボタンをクリックして、有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="3d70f-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="3d70f-125">品目に関連する分析コードを表示する場合は、**分析コードの表示**をクリックして、表示する分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d70f-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

<span data-ttu-id="3d70f-126">次の図では、品目番号「1000」の品目の使用場所の計算例を示しています。</span><span class="sxs-lookup"><span data-stu-id="3d70f-126">In the figure below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![図 1](media/12-controlling-and-reporting.png)

