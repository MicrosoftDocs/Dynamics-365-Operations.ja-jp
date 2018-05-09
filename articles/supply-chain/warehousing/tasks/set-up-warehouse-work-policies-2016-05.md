--- 
title: "倉庫作業ポリシーの設定"
description: "倉庫のプロセスは倉庫作業を常に含みません。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: af2e01ccf570bbc647784351752ecb5c7c7d7595
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="b0c98-103">倉庫作業ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="b0c98-103">Set up warehouse work policies</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0c98-104">倉庫のプロセスは倉庫作業を常に含みません。</span><span class="sxs-lookup"><span data-stu-id="b0c98-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="b0c98-105">作業ポリシーを定義して、原材料のピッキングの作業の作成、および特定の場所での一連の製品に対する完成品のプット アウェイを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="b0c98-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="b0c98-106">デモ データの会社 USMF がこの記録の作成に使用されました。</span><span class="sxs-lookup"><span data-stu-id="b0c98-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="b0c98-107">このタスク ガイドでは、Dynamics AX アプリケーション 7.0.1 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="b0c98-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="b0c98-108">[倉庫管理] > [設定] > [作業] > [作業ポリシー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="b0c98-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-109">Click New.</span></span>
3. <span data-ttu-id="b0c98-110">[作業ポリシー名] フィールドに、「プット アウェイ作業なし」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="b0c98-111">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-111">Click Save.</span></span>
5. <span data-ttu-id="b0c98-112">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-112">Click Add.</span></span>
6. <span data-ttu-id="b0c98-113">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b0c98-114">[ワーク オーダー タイプ] フィールドで、[完成品のプット アウェイ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="b0c98-115">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-115">Click Add.</span></span>
9. <span data-ttu-id="b0c98-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="b0c98-117">[ワーク オーダー タイプ] フィールドで、[連産物と副産物のプット アウェイ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="b0c98-118">[在庫場所] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="b0c98-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-119">Click Add.</span></span>
13. <span data-ttu-id="b0c98-120">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="b0c98-121">倉庫の一覧で、「51」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="b0c98-122">[場所] フィールドで「001」を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="b0c98-123">[製品] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-123">Expand the Products section.</span></span>
17. <span data-ttu-id="b0c98-124">[製品の選択] フィールドで、[選択済] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="b0c98-125">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-125">Click Add.</span></span>
19. <span data-ttu-id="b0c98-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="b0c98-127">[品目番号] フィールドで、「L0101」を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b0c98-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="b0c98-128">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0c98-128">Click Save.</span></span>


