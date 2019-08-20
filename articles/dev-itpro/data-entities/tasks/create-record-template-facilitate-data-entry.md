---
title: データ入力を容易にするレコード テンプレートの作成
description: この手順は、よく使用されるフィールド値を新しいレコードごとに明示的に入力する必要をなくなるようにする、レコード テンプレートの作成方法を示します。
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b2ba56b6146f2495fb6a53c3cef9f549b1ad837
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848210"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="d623c-103">データ入力を容易にするレコード テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="d623c-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d623c-104">この手順は、よく使用されるフィールド値を新しいレコードごとに明示的に入力する必要をなくなるようにする、レコード テンプレートの作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d623c-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="d623c-105">この手順では、固定資産に追加する必要がある新しいラップトップのレコードを新規作成します。</span><span class="sxs-lookup"><span data-stu-id="d623c-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="d623c-106">この手順では、USMF というサンプル会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="d623c-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="d623c-107">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="d623c-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="d623c-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d623c-108">Click New.</span></span>
3. <span data-ttu-id="d623c-109">[固定資産グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d623c-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="d623c-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d623c-111">たとえば、「企業潜在顧客のラップトップ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="d623c-112">[検索名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="d623c-113">たとえば、「ラップトップ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="d623c-114">[技術情報] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d623c-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="d623c-115">[製造業者] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="d623c-116">[モデル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="d623c-117">[年始] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="d623c-118">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d623c-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="d623c-119">[レコード情報] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d623c-119">Click Record info.</span></span>
12. <span data-ttu-id="d623c-120">[ユーザー テンプレート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d623c-120">Click User template.</span></span>
13. <span data-ttu-id="d623c-121">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d623c-122">たとえば、「企業のラップトップ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="d623c-123">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d623c-124">たとえば、「企業のラップトップ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d623c-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="d623c-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d623c-125">Click OK.</span></span>
16. <span data-ttu-id="d623c-126">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d623c-126">Click Close.</span></span>

