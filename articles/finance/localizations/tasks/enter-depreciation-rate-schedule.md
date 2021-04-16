---
title: 償却率表の入力および減価償却プロファイルへの関連付け
description: 日本では、固定資産減価償却率は政府機関によって発表されます。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepRate_JP, AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8518e11a8be809fc58a5c79c47e6ce8c64b32c7b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822613"
---
# <a name="enter-depreciation-rate-schedule-and-associate-to-depreciation-profile"></a><span data-ttu-id="9dc48-103">償却率表の入力および減価償却プロファイルへの関連付け</span><span class="sxs-lookup"><span data-stu-id="9dc48-103">Enter depreciation rate schedule and associate to depreciation profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9dc48-104">日本では、固定資産減価償却率は政府機関によって発表されます。</span><span class="sxs-lookup"><span data-stu-id="9dc48-104">In Japan, the fixed asset depreciation rate is released by a government agency.</span></span> <span data-ttu-id="9dc48-105">償却率表はシステムに入力することができます。</span><span class="sxs-lookup"><span data-stu-id="9dc48-105">You can enter the depreciation rate schedule into the system.</span></span> <span data-ttu-id="9dc48-106">償却率表は、ファイルからインポートできるようデータ エンティティとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="9dc48-106">The depreciation rate schedule is implemented as a data entity so that it can be imported from a file.</span></span> 



<span data-ttu-id="9dc48-107">このタスクでは、償却率表の変更および減価償却プロファイルとの関連付けの方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9dc48-107">Use this task to learn how to modify the depreciation rate schedule and associate it to a depreciation profile.</span></span> <span data-ttu-id="9dc48-108">このタスクではインポートは実行しません。</span><span class="sxs-lookup"><span data-stu-id="9dc48-108">The import is not covered in this task.</span></span> 



<span data-ttu-id="9dc48-109">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9dc48-109">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="9dc48-110">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="9dc48-110">This task uses the JPMF demo company data.</span></span>


## <a name="modify-a-depreciation-rate-schedule"></a><span data-ttu-id="9dc48-111">償却率表の変更</span><span class="sxs-lookup"><span data-stu-id="9dc48-111">Modify a depreciation rate schedule</span></span>
1. <span data-ttu-id="9dc48-112">[固定資産] > [設定] > [償却率表] > [償却率表] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9dc48-112">Go to Fixed assets > Setup > Depreciation rate schedules > Depreciation rate schedules.</span></span>
2. <span data-ttu-id="9dc48-113">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9dc48-113">Click Edit.</span></span>
3. <span data-ttu-id="9dc48-114">[耐用年数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9dc48-114">In the Service life field, enter a number.</span></span>
4. <span data-ttu-id="9dc48-115">[減価償却レート] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9dc48-115">In the Depreciation rate field, enter a number.</span></span>
5. <span data-ttu-id="9dc48-116">[改定償却率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9dc48-116">In the Revised depreciation rate field, enter a number.</span></span>
6. <span data-ttu-id="9dc48-117">[保証率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9dc48-117">In the Guaranteed depreciation rate field, enter a number.</span></span>

## <a name="associate-a-depreciation-rate-schedule-to-a-depreciation-profile"></a><span data-ttu-id="9dc48-118">償却率表と減価償却プロファイルの関連付け</span><span class="sxs-lookup"><span data-stu-id="9dc48-118">Associate a depreciation rate schedule to a depreciation profile</span></span> 
1. <span data-ttu-id="9dc48-119">[固定資産] > [設定] > [減価償却プロファイル] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9dc48-119">Go to Fixed assets > Setup > Depreciation profiles.</span></span>
2. <span data-ttu-id="9dc48-120">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9dc48-120">Click Edit.</span></span>
3. <span data-ttu-id="9dc48-121">[償却率表] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9dc48-121">In the Depreciation rate schedule field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9dc48-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9dc48-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9dc48-123">前のタスクで変更した減価償却スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="9dc48-123">Select the depreciation schedule that you modified in the earlier task.</span></span>  
5. <span data-ttu-id="9dc48-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9dc48-124">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]