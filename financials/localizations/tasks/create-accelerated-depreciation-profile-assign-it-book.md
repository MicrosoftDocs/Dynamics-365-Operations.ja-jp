--- 
title: "増加償却プロファイルの作成および帳簿への割り当て (日本)"
description: "日本では、ほかの減価償却方法と同様、加速償却に減価償却プロファイルが必要です。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ee755cb1e2ee6beb811247c0f9e67d847257205e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-accelerated-depreciation-profile-and-assign-it-to-book-japan"></a><span data-ttu-id="546cb-103">増加償却プロファイルの作成および帳簿への割り当て (日本)</span><span class="sxs-lookup"><span data-stu-id="546cb-103">Create an accelerated depreciation profile and assign it to book (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="546cb-104">日本では、ほかの減価償却方法と同様、加速償却に減価償却プロファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="546cb-104">For Japan, accelerated depreciation requires configuration of a depreciation profile, just like other depreciation methods.</span></span> 



<span data-ttu-id="546cb-105">この手順では、増加償却用の減価償却プロファイルの作成方法および帳簿への割り当て方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="546cb-105">Use this procedure to learn how to create a depreciation profile for accelerated depreciation and assign it to a book.</span></span> 



<span data-ttu-id="546cb-106">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="546cb-106">In order to complete this procedure, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="546cb-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="546cb-107">This procedure was created using the demo data company JPMF.</span></span>


## <a name="create-a-depreciation-profile"></a><span data-ttu-id="546cb-108">減価償却プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="546cb-108">Create a depreciation profile</span></span>
1. <span data-ttu-id="546cb-109">[固定資産] > [設定] > [減価償却プロファイル] に移動します。</span><span class="sxs-lookup"><span data-stu-id="546cb-109">Go to Fixed assets > Setup > Depreciation profiles.</span></span>
2. <span data-ttu-id="546cb-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="546cb-110">Click New.</span></span>
3. <span data-ttu-id="546cb-111">[減価償却プロファイル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="546cb-111">In the Depreciation profile field, type a value.</span></span>
4. <span data-ttu-id="546cb-112">後で参照できるよう [減価償却プロファイル] フィールドの値をメモします。</span><span class="sxs-lookup"><span data-stu-id="546cb-112">Note the value in the Depreciation profile field to reference later</span></span>
5. <span data-ttu-id="546cb-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="546cb-113">In the Name field, type a value.</span></span>
6. <span data-ttu-id="546cb-114">[方法] フィールドで「加速」を選択します。</span><span class="sxs-lookup"><span data-stu-id="546cb-114">In the Method field, select 'Accelerated'.</span></span>
7. <span data-ttu-id="546cb-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="546cb-115">Click Save.</span></span>

## <a name="assign-the-depreciation-profile-to-a-book"></a><span data-ttu-id="546cb-116">減価償却プロファイルの帳簿への割り当て</span><span class="sxs-lookup"><span data-stu-id="546cb-116">Assign the depreciation profile to a book</span></span>
1. <span data-ttu-id="546cb-117">[固定資産] > [設定] > [帳簿] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="546cb-117">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="546cb-118">増加償却プロファイルを割り当てる帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="546cb-118">Select the book to assign the accelerated depreciation profile to.</span></span>
3. <span data-ttu-id="546cb-119">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="546cb-119">Click Edit.</span></span>
4. <span data-ttu-id="546cb-120">事前にメモした値を [加速償却プロファイル] に使用します。</span><span class="sxs-lookup"><span data-stu-id="546cb-120">Use the value noted previously in the Accelerated depreciation profile field</span></span>
5. <span data-ttu-id="546cb-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="546cb-121">Click Save.</span></span>


