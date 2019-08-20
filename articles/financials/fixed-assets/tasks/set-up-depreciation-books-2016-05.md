---
title: 資産減価償却簿の設定 (2016 年 5 月)
description: このタスク ガイドでは、新しい減価償却簿が作成さし、固定資産グループに関連付けます。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839860"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="53430-103">資産減価償却簿の設定 (2016 年 5 月)</span><span class="sxs-lookup"><span data-stu-id="53430-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53430-104">このタスク ガイドでは、新しい減価償却簿が作成さし、固定資産グループに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="53430-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="53430-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="53430-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="53430-106">減価償却簿の作成</span><span class="sxs-lookup"><span data-stu-id="53430-106">Create a depreciation book</span></span>
1. <span data-ttu-id="53430-107">[固定資産] > [設定] > [減価償却簿] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="53430-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="53430-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53430-108">Click New.</span></span>
3. <span data-ttu-id="53430-109">[減価償却簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53430-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="53430-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53430-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="53430-111">[減価償却の計算] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="53430-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="53430-112">[減価償却プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="53430-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="53430-113">一覧で、目的の減価償却プロファイルを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="53430-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="53430-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53430-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="53430-115">[代替減価償却プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="53430-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="53430-116">一覧で、目的の減価償却プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="53430-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="53430-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53430-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="53430-118">特別減価償却プロファイルは、特殊な状況で資産の割増償却に使用されます。</span><span class="sxs-lookup"><span data-stu-id="53430-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="53430-119">たとえば、自然災害の結果の減価償却を記録する場合などに、このフィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="53430-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="53430-120">[基準調整を含む減価償却調整を作成する] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="53430-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="53430-121">[カレンダー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="53430-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="53430-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53430-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="53430-123">減価償却簿を固定資産グループに関連付ける</span><span class="sxs-lookup"><span data-stu-id="53430-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="53430-124">[固定資産グループ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53430-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="53430-125">[固定資産グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="53430-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="53430-126">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="53430-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="53430-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="53430-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="53430-128">[減価償却方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="53430-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="53430-129">[耐用年数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53430-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="53430-130">耐用年数を設定した後に減価償却期間のフィールド値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="53430-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

