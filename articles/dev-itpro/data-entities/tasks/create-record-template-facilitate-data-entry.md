--- 
title: "データ入力を容易にするレコード テンプレートの作成"
description: "この手順は、よく使用されるフィールド値を新しいレコードごとに明示的に入力する必要をなくなるようにする、レコード テンプレートの作成方法を示します。"
author: sericks007
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6f8d804133f8e9c6f47420d41df8d9430381e2fe
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="c15b1-103">データ入力を容易にするレコード テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="c15b1-103">Create a record template to facilitate data entry</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c15b1-104">この手順は、よく使用されるフィールド値を新しいレコードごとに明示的に入力する必要をなくなるようにする、レコード テンプレートの作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="c15b1-105">この手順では、固定資産に追加する必要がある新しいラップトップのレコードを新規作成します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="c15b1-106">この手順では、USMF というサンプル会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="c15b1-107">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="c15b1-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c15b1-108">Click New.</span></span>
3. <span data-ttu-id="c15b1-109">[固定資産グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="c15b1-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c15b1-111">たとえば、「企業潜在顧客のラップトップ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="c15b1-112">[検索名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="c15b1-113">たとえば、「ラップトップ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="c15b1-114">[技術情報] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="c15b1-115">[製造業者] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="c15b1-116">[モデル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="c15b1-117">[年始] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="c15b1-118">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c15b1-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="c15b1-119">[レコード情報] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c15b1-119">Click Record info.</span></span>
12. <span data-ttu-id="c15b1-120">[ユーザー テンプレート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c15b1-120">Click User template.</span></span>
13. <span data-ttu-id="c15b1-121">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c15b1-122">たとえば、「企業のラップトップ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="c15b1-123">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c15b1-124">たとえば、「企業のラップトップ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c15b1-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="c15b1-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c15b1-125">Click OK.</span></span>
16. <span data-ttu-id="c15b1-126">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c15b1-126">Click Close.</span></span>


