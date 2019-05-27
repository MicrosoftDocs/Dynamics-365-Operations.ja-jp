---
title: 既存のかんばんルールを複製して新しいかんばんルールを作成
description: この手順では、既存のかんばんルールの複製の作成を中心に説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f72dbca0debf9e6a03ee700a979d4f4c110f819
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559857"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="a943c-103">既存のかんばんルールを複製して新しいかんばんルールを作成</span><span class="sxs-lookup"><span data-stu-id="a943c-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a943c-104">この手順では、既存のかんばんルールの複製の作成を中心に説明します。</span><span class="sxs-lookup"><span data-stu-id="a943c-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="a943c-105">これは、既存のかんばんルールに基づいて新しいかんばんルールを作成する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="a943c-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="a943c-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="a943c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a943c-107">この手順は、変更された生産フローまたは新しい補充ルールに対する生産を準備している、プロセス エンジニアまたはバリュー ストリーム マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="a943c-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="a943c-108">かんばんルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="a943c-108">Select a kanban rule</span></span>
1. <span data-ttu-id="a943c-109">[かんばんルール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="a943c-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="a943c-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a943c-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a943c-111">製品 M0006 のかんばんルール 000017 を選択します。</span><span class="sxs-lookup"><span data-stu-id="a943c-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="a943c-112">かんばんルールの複製</span><span class="sxs-lookup"><span data-stu-id="a943c-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="a943c-113">[かんばんルールの複製] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a943c-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="a943c-114">かんばんルールの複製をする場合、タイプ、日付、活動、および製品の選択を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="a943c-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="a943c-115">次の手順でこの手順の製品を変更します。</span><span class="sxs-lookup"><span data-stu-id="a943c-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="a943c-116">[製品] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a943c-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="a943c-117">M0007 を選択します。</span><span class="sxs-lookup"><span data-stu-id="a943c-117">Select M0007.</span></span>  
3. <span data-ttu-id="a943c-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a943c-118">Click OK.</span></span>
    * <span data-ttu-id="a943c-119">かんばんルール 000017 の複製が作成されることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="a943c-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

