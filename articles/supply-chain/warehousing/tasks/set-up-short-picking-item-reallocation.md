---
title: 品目再配賦の未処理ピッキングの設定
description: このトピックでは、指定された場所に在庫が不十分な場合に、倉庫作業者が他の倉庫を素早く見つけることができるようにする方法について説明します。
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8baf846d65e6fefe9ca575b5af5a2dbceac666
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976891"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="f1717-103">品目再配賦の未処理ピッキングの設定</span><span class="sxs-lookup"><span data-stu-id="f1717-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1717-104">この手順では、指定された場所に在庫が不十分な場合に、倉庫作業者が他の倉庫を素早く見つけることができるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f1717-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="f1717-105">再配賦プロセスは、**例外作業** によって制御され、倉庫の **作業者** によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="f1717-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="f1717-106">自動、手動、またはその両方の再配賦プロセスを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f1717-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="f1717-107">自動再配賦 - 場所ディレクティブを使用して、商品が別の場所にあるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="f1717-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="f1717-108">可能な場合は、作業が更新され、倉庫のユーザーは別の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="f1717-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="f1717-109">手動再配賦 - 倉庫のユーザーは、商品の未引当数量を持つ 1 つ以上の場所から選択することができます。</span><span class="sxs-lookup"><span data-stu-id="f1717-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="f1717-110">自動と手動 - システムが自動再配賦を実行できず、未引当数量で場所を使用できる場合は、場所を選択するようにユーザーにメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f1717-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="f1717-111">作業例外を設定します</span><span class="sxs-lookup"><span data-stu-id="f1717-111">Set up work exceptions</span></span>
<span data-ttu-id="f1717-112">倉庫作業者が処理している出荷のニーズに基づいて選択を行えるように、異なる品目の再配置ポリシーでいくつかの作業の例外を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="f1717-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="f1717-113">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="f1717-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="f1717-114">**ナビゲーション ウィンドウ** で、**倉庫管理 > 設定 > 作業 > 例外作業** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f1717-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="f1717-115">**新規** をクリックする</span><span class="sxs-lookup"><span data-stu-id="f1717-115">Click **New**</span></span> 
3. <span data-ttu-id="f1717-116">**例外作業コード** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f1717-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="f1717-117">これがこの例外のタイトルになります。</span><span class="sxs-lookup"><span data-stu-id="f1717-117">This will be the title of this exception .</span></span> <span data-ttu-id="f1717-118">たとえば、ショートピッキングに関するマニュアルなど。</span><span class="sxs-lookup"><span data-stu-id="f1717-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="f1717-119">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f1717-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="f1717-120">これが、この例外の使用方法についての簡単な説明になります。</span><span class="sxs-lookup"><span data-stu-id="f1717-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="f1717-121">たとえば、ショートピッキング - 品目は使用できません。</span><span class="sxs-lookup"><span data-stu-id="f1717-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="f1717-122">**例外** タイプ フィールドで、**ショートピック** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f1717-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="f1717-123">**在庫調整** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="f1717-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="f1717-124">選択した場合、在庫が簡単なピッキング場所の 0 に自動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="f1717-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="f1717-125">**既定の調整タイプ コード** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f1717-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="f1717-126">たとえば、USMF では、**Res Adj Out を削除する** を選択できます。 各調整タイプコードには、名前、説明、在庫仕訳帳名、および **引当の削除** の 4 つの特性が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1717-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="f1717-127">**引当の削除** が有効になっている場合は、ショートピッキングされた注文明細行の引当が削除されます。</span><span class="sxs-lookup"><span data-stu-id="f1717-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="f1717-128">**品目の再配賦** フィールドで、手動などの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="f1717-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="f1717-129">手動または自動および手動を選択した場合、倉庫従事者は手動での再配分を実行できなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f1717-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="f1717-130">手作業による品目再配分を使用する作業者を設定します。</span><span class="sxs-lookup"><span data-stu-id="f1717-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="f1717-131">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="f1717-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="f1717-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f1717-132">Close the page.</span></span>
2. <span data-ttu-id="f1717-133">**ナビゲーション ウィンドウ** で、**倉庫管理 > 設定 > 作業者** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f1717-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="f1717-134">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1717-134">Click **Edit**.</span></span>
4. <span data-ttu-id="f1717-135">一覧で、作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="f1717-135">In the list, select worker.</span></span> <span data-ttu-id="f1717-136">たとえば、Julia Funderburk を選択します。</span><span class="sxs-lookup"><span data-stu-id="f1717-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="f1717-137">**ユーザー** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="f1717-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="f1717-138">一覧から **ユーザー ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f1717-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="f1717-139">例えば 24 です。</span><span class="sxs-lookup"><span data-stu-id="f1717-139">For example, 24.</span></span>
7. <span data-ttu-id="f1717-140">**作業** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="f1717-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="f1717-141">**手動による再配賦を許可** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f1717-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
