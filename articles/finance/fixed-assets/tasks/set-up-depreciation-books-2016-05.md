---
title: 減価償却簿の設定
description: この手順では、新しい減価償却簿を作成し、それを固定資産グループに関連付けるプロセスを順を追って説明します。
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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd65cb77872b3e2f74402cf8c92c8b8989cea6ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224696"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="0ed4b-103">減価償却簿の設定</span><span class="sxs-lookup"><span data-stu-id="0ed4b-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ed4b-104">この手順では、新しい減価償却簿を作成し、それを固定資産グループに関連付けるプロセスを順を追って説明します。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="0ed4b-105">減価償却簿の作成</span><span class="sxs-lookup"><span data-stu-id="0ed4b-105">Create a depreciation book</span></span>
1. <span data-ttu-id="0ed4b-106">[固定資産] > [設定] > [減価償却簿] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="0ed4b-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-107">Click New.</span></span>
3. <span data-ttu-id="0ed4b-108">[減価償却簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="0ed4b-109">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0ed4b-110">[減価償却の計算] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="0ed4b-111">[減価償却プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0ed4b-112">一覧で、目的の減価償却プロファイルを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="0ed4b-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0ed4b-114">[代替減価償却プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0ed4b-115">一覧で、目的の減価償却プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="0ed4b-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0ed4b-117">特別減価償却プロファイルは、特殊な状況で資産の割増償却に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="0ed4b-118">たとえば、自然災害の結果の減価償却を記録する場合などに、このフィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="0ed4b-119">[基準調整を含む減価償却調整を作成する] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="0ed4b-120">[カレンダー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="0ed4b-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="0ed4b-122">減価償却簿を固定資産グループに関連付ける</span><span class="sxs-lookup"><span data-stu-id="0ed4b-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="0ed4b-123">[固定資産グループ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="0ed4b-124">[固定資産グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0ed4b-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0ed4b-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0ed4b-127">[減価償却方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="0ed4b-128">[耐用年数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="0ed4b-129">耐用年数を設定した後に減価償却期間のフィールド値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="0ed4b-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]