---
title: 既存のかんばんルールを複製して新しいかんばんルールを作成
description: この手順では、既存のかんばんルールの複製の作成を中心に説明します。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84a0093d95c2f7084c7a0ed17f8b2f86d654b5d7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212216"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="78b7d-103">既存のかんばんルールを複製して新しいかんばんルールを作成</span><span class="sxs-lookup"><span data-stu-id="78b7d-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78b7d-104">この手順では、既存のかんばんルールの複製の作成を中心に説明します。</span><span class="sxs-lookup"><span data-stu-id="78b7d-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="78b7d-105">これは、既存のかんばんルールに基づいて新しいかんばんルールを作成する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="78b7d-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="78b7d-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="78b7d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="78b7d-107">この手順は、変更された生産フローまたは新しい補充ルールに対する生産を準備している、プロセス エンジニアまたはバリュー ストリーム マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="78b7d-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="78b7d-108">かんばんルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="78b7d-108">Select a kanban rule</span></span>
1. <span data-ttu-id="78b7d-109">[かんばんルール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="78b7d-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="78b7d-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="78b7d-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="78b7d-111">製品 M0006 のかんばんルール 000017 を選択します。</span><span class="sxs-lookup"><span data-stu-id="78b7d-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="78b7d-112">かんばんルールの複製</span><span class="sxs-lookup"><span data-stu-id="78b7d-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="78b7d-113">[かんばんルールの複製] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7d-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="78b7d-114">かんばんルールの複製をする場合、タイプ、日付、活動、および製品の選択を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="78b7d-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="78b7d-115">次の手順でこの手順の製品を変更します。</span><span class="sxs-lookup"><span data-stu-id="78b7d-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="78b7d-116">[製品] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="78b7d-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="78b7d-117">M0007 を選択します。</span><span class="sxs-lookup"><span data-stu-id="78b7d-117">Select M0007.</span></span>  
3. <span data-ttu-id="78b7d-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7d-118">Click OK.</span></span>
    * <span data-ttu-id="78b7d-119">かんばんルール 000017 の複製が作成されることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="78b7d-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

