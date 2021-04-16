---
title: 積荷テンプレート
description: このトピックでは、積荷テンプレートの設定方法と、新しい積荷に積荷テンプレートを関連付ける方法について説明します。
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 175c8017b14cc298cdaa00031f8450015a747786
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831509"
---
# <a name="load-templates"></a><span data-ttu-id="7cd68-103">積荷テンプレート</span><span class="sxs-lookup"><span data-stu-id="7cd68-103">Load templates</span></span>

<span data-ttu-id="7cd68-104">新しい積荷を作成する場合は、積荷テンプレートを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="7cd68-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="7cd68-105">積荷テンプレートには、機器に関する情報、および積荷の高さ、幅、深さ、容積などの測定値に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7cd68-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="7cd68-106">このトピックでは、積荷テンプレートの設定方法と、新しい積荷に積荷テンプレートを関連付ける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="7cd68-107">積荷テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="7cd68-107">Set up a load template</span></span>

1. <span data-ttu-id="7cd68-108">**輸送管理 \> 設定 \> 積荷構築 \> 積荷テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="7cd68-109">アクション ウィンドウで **新規** を選択し新しいテンプレートを追加するか、**編集** をクリックして既存のテンプレートを編集します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="7cd68-110">新規または既存のテンプレートの行で、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="7cd68-111">**積荷テンプレート ID** – 積荷テンプレートの一意識別子 (ID) を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="7cd68-112">**設備** – 積荷の出荷に使用する設備を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="7cd68-113">**積荷の高さ**、**積荷の幅**、および **積荷の奥行き** – 積荷の寸法を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="7cd68-114">**最大積載容積** と **最大積載重量** – 積荷の最大積載容積と重量を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="7cd68-115">**最大積載総重量** ー 積荷の最大積載総重量を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="7cd68-116">積荷の総重量には、風袋重量と積載重量の両方が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7cd68-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="7cd68-117">**貨物の最大個数** – 積荷に含めることができる貨物の最大個数を入力します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="7cd68-118">**貨物を床積みにする** – 床積みを使用するには、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7cd68-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="7cd68-119">床積みのシナリオでは、ボックスをコンテナー内に床から天井まで床一面に積み重ねて、収容能力を最大限にします。</span><span class="sxs-lookup"><span data-stu-id="7cd68-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="7cd68-120">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="7cd68-121">新しい積荷に積荷テンプレートを関連付け</span><span class="sxs-lookup"><span data-stu-id="7cd68-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="7cd68-122">**配送管理 \> 計画 \> 積荷計画ワークベンチ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="7cd68-123">ページの上部で、積荷を作成するソース ドキュメントのタイプに応じて、**出荷**、**販売明細行**、**移動明細行**、または **購買注文明細行** のタブのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="7cd68-124">積荷を計画する特定のドキュメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="7cd68-125">アクション ウィンドウの、**供給と需要** タブの **追加** グループで、**新しい積荷へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="7cd68-126">**積荷テンプレートの割り当て** ダイアログ ボックスの、**積荷テンプレート ID** フィールドで、適用するテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="7cd68-127">テンプレートを適用するには、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cd68-127">Select **OK** to apply the template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]