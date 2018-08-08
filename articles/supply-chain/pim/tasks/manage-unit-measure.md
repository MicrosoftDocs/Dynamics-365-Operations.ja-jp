--- 
title: "測定単位の管理"
description: "この手順は、測定単位の定義方法、単位の翻訳の提供方法とその説明、および関連する単位の変換ルールの定義方法を示します。"
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 49c2df35e03d1e633379eab49aea54a549cd3d62
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="3aa41-103">測定単位の管理</span><span class="sxs-lookup"><span data-stu-id="3aa41-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3aa41-104">この手順は、測定単位の定義方法、単位の翻訳の提供方法とその説明、および関連する単位の変換ルールの定義方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="3aa41-105">デモ データまたは独自のデータを使用して、この手順を確認できます。</span><span class="sxs-lookup"><span data-stu-id="3aa41-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="3aa41-106">[リリース済製品の保守] に移動します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="3aa41-107">[単位] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="3aa41-108">測定単位の作成</span><span class="sxs-lookup"><span data-stu-id="3aa41-108">Create a unit of measure</span></span>
1. <span data-ttu-id="3aa41-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-109">Click New.</span></span>
2. <span data-ttu-id="3aa41-110">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="3aa41-111">測定単位を参照するときに使用する ID または記号を入力します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="3aa41-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3aa41-113">システム言語で測定単位の内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="3aa41-114">[単位クラス] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="3aa41-115">単位クラスは、測定単位が含まれる、領域、質量、または数量などの論理グループを定義します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="3aa41-116">[小数点以下の精度] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="3aa41-117">測定単位に対する計算を完了する場合、変換後の測定単位を丸める必要があるときの小数点以下の桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="3aa41-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="3aa41-119">単位の変換の定義</span><span class="sxs-lookup"><span data-stu-id="3aa41-119">Define unit translations</span></span>
1. <span data-ttu-id="3aa41-120">[単位のテキスト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-120">Click Unit texts.</span></span>
2. <span data-ttu-id="3aa41-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-121">Click New.</span></span>
    * <span data-ttu-id="3aa41-122">顧客または仕入先の固有言語で外部ドキュメントに使用する測定単位を表す ID または記号の翻訳を作成するには、単位テキストを使用します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="3aa41-123">[言語] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="3aa41-124">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="3aa41-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-125">Click Save.</span></span>
6. <span data-ttu-id="3aa41-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3aa41-126">Close the page.</span></span>
7. <span data-ttu-id="3aa41-127">[翻訳済単位の説明] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="3aa41-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-128">Click New.</span></span>
    * <span data-ttu-id="3aa41-129">測定単位に言語固有の説明を定義します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="3aa41-130">[言語] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="3aa41-131">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="3aa41-132">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-132">Click Save.</span></span>
12. <span data-ttu-id="3aa41-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3aa41-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="3aa41-134">単位換算ルールの定義</span><span class="sxs-lookup"><span data-stu-id="3aa41-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="3aa41-135">[単位換算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="3aa41-136">選択された単位クラスでの、他の測定単位への（からの）測定単位の変換に関するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="3aa41-137">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3aa41-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="3aa41-138">[係数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="3aa41-139">[開始単位] から [終了単位] を導くための換算率。</span><span class="sxs-lookup"><span data-stu-id="3aa41-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="3aa41-140">たとえば、センチメートルからメートルへの換算率は 100 になります (100 センチメートル = 1 メートル)。</span><span class="sxs-lookup"><span data-stu-id="3aa41-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="3aa41-141">[終了単位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="3aa41-142">[丸め] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="3aa41-143">変換された値の丸め方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="3aa41-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="3aa41-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3aa41-144">Click OK.</span></span>
7. <span data-ttu-id="3aa41-145">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3aa41-145">Close the page.</span></span>


