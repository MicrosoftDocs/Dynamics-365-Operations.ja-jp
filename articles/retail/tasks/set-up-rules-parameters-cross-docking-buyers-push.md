--- 
title: "クロス ドッキングおよび集中的購買のルールとパラメーターの設定"
description: "この手順では、補充ルールを作成するための手順を示します。"
author: josaw1
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1ff41a18be066b6f32c5172bda38c389e7f34128
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="39a4a-103">クロス ドッキングおよび集中的購買のルールとパラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="39a4a-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="39a4a-104">この手順では、補充ルールを作成するための手順を示します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="39a4a-105">クロスドッキングと集中的購買を実行するときに、補充ルールを製品の店舗への配分を管理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="39a4a-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="39a4a-106">補充ルールは、店舗または店舗グループに対して設定できます。</span><span class="sxs-lookup"><span data-stu-id="39a4a-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="39a4a-107">ルールの行ごとに定義された重量によって、補充ルールをクロスドッキングまたは集中的購買で配分方法として使用する場合に、店舗間で配分される製品の数量が制御されます。</span><span class="sxs-lookup"><span data-stu-id="39a4a-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="39a4a-108">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="39a4a-109">[補充ルール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="39a4a-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="39a4a-110">Click New.</span></span>
3. <span data-ttu-id="39a4a-111">[補充ルール] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="39a4a-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="39a4a-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="39a4a-113">Click Save.</span></span>
6. <span data-ttu-id="39a4a-114">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="39a4a-114">Click Add.</span></span>
7. <span data-ttu-id="39a4a-115">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="39a4a-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="39a4a-116">補充階層またはタイプのチャンネルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="39a4a-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="39a4a-117">この値によって、名前で選択した内容がチャンネルの階層または特定のチャンネルであるかが管理されます。</span><span class="sxs-lookup"><span data-stu-id="39a4a-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="39a4a-118">この例では、補充階層として設定を保持します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="39a4a-119">[名前] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="39a4a-120">既定の重量の値は、倉庫で定義された重量から入力されます。</span><span class="sxs-lookup"><span data-stu-id="39a4a-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="39a4a-121">この重量を補充ルールで使用できます。また、[重量] フィールドに新しい重量を入力できます。</span><span class="sxs-lookup"><span data-stu-id="39a4a-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="39a4a-122">[重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="39a4a-123">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="39a4a-123">Click Add.</span></span>
11. <span data-ttu-id="39a4a-124">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="39a4a-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="39a4a-125">[タイプ] フィールドで [チャンネル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="39a4a-126">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="39a4a-127">[重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="39a4a-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="39a4a-128">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="39a4a-128">Click Save.</span></span>


