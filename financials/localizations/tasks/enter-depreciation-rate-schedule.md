--- 
title: "償却率表の入力および減価償却プロファイルへの関連付け (日本)"
description: "日本では、固定資産減価償却率は政府機関によって発表されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/16/2016
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
ms.openlocfilehash: 3a35970354107da6ca2449a6c07f5afe3f4d2e17
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="enter-a-depreciation-rate-schedule-and-associate-to-a-depreciation-profile-japan"></a><span data-ttu-id="3063e-103">償却率表の入力および減価償却プロファイルへの関連付け (日本)</span><span class="sxs-lookup"><span data-stu-id="3063e-103">Enter a depreciation rate schedule and associate to a depreciation profile (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3063e-104">日本では、固定資産減価償却率は政府機関によって発表されます。</span><span class="sxs-lookup"><span data-stu-id="3063e-104">In Japan, the fixed asset depreciation rate is released by a government agency.</span></span> <span data-ttu-id="3063e-105">償却率表はシステムに入力することができます。</span><span class="sxs-lookup"><span data-stu-id="3063e-105">You can enter the depreciation rate schedule into the system.</span></span> <span data-ttu-id="3063e-106">償却率表は、ファイルからインポートできるようデータ エンティティとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="3063e-106">The depreciation rate schedule is implemented as a data entity so that it can be imported from a file.</span></span> 



<span data-ttu-id="3063e-107">このタスクでは、償却率表の変更および減価償却プロファイルとの関連付けの方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3063e-107">Use this task to learn how to modify the depreciation rate schedule and associate it to a depreciation profile.</span></span> <span data-ttu-id="3063e-108">このタスクではインポートは実行しません。</span><span class="sxs-lookup"><span data-stu-id="3063e-108">The import is not covered in this task.</span></span> 



<span data-ttu-id="3063e-109">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3063e-109">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="3063e-110">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="3063e-110">This task uses the JPMF demo company data.</span></span>


## <a name="modify-a-depreciation-rate-schedule"></a><span data-ttu-id="3063e-111">償却率表の変更</span><span class="sxs-lookup"><span data-stu-id="3063e-111">Modify a depreciation rate schedule</span></span>
1. <span data-ttu-id="3063e-112">[固定資産] > [設定] > [償却率表] > [償却率表] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3063e-112">Go to Fixed assets > Setup > Depreciation rate schedules > Depreciation rate schedules.</span></span>
2. <span data-ttu-id="3063e-113">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3063e-113">Click Edit.</span></span>
3. <span data-ttu-id="3063e-114">[耐用年数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3063e-114">In the Service life field, enter a number.</span></span>
4. <span data-ttu-id="3063e-115">[減価償却レート] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3063e-115">In the Depreciation rate field, enter a number.</span></span>
5. <span data-ttu-id="3063e-116">[改定償却率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3063e-116">In the Revised depreciation rate field, enter a number.</span></span>
6. <span data-ttu-id="3063e-117">[保証率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3063e-117">In the Guaranteed depreciation rate field, enter a number.</span></span>

## <a name="associate-a-depreciation-rate-schedule-to-a-depreciation-profile"></a><span data-ttu-id="3063e-118">償却率表と減価償却プロファイルの関連付け</span><span class="sxs-lookup"><span data-stu-id="3063e-118">Associate a depreciation rate schedule to a depreciation profile</span></span> 
1. <span data-ttu-id="3063e-119">[固定資産] > [設定] > [減価償却プロファイル] に移動します。</span><span class="sxs-lookup"><span data-stu-id="3063e-119">Go to Fixed assets > Setup > Depreciation profiles.</span></span>
2. <span data-ttu-id="3063e-120">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3063e-120">Click Edit.</span></span>
3. <span data-ttu-id="3063e-121">[償却率表] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="3063e-121">In the Depreciation rate schedule field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3063e-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3063e-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3063e-123">前のタスクで変更した減価償却スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="3063e-123">Select the depreciation schedule that you modified in the earlier task.</span></span>  
5. <span data-ttu-id="3063e-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3063e-124">Click Save.</span></span>


