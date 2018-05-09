--- 
title: "法人間での固定資産減価償却の計算"
description: "この手順では、複数の法人組織に対して減価償却プロセスを設定して実行する方法を示します。"
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 77df61bd85d3c296e44d3a2cfb0fce8b16eaaf9f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="99850-103">法人間での固定資産減価償却の計算</span><span class="sxs-lookup"><span data-stu-id="99850-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99850-104">固定資産減価償却は、単一のステップで複数の法人に対して実行することができます。</span><span class="sxs-lookup"><span data-stu-id="99850-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="99850-105">この手順では、複数の法人組織に対してプロセスを設定して実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="99850-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="99850-106">会計士の役割を使用します。</span><span class="sxs-lookup"><span data-stu-id="99850-106">It uses the accountant role.</span></span>  

<span data-ttu-id="99850-107">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="99850-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="99850-108">ステップ (16) サブタスク: 会社間の減価償却実行ジャーナルを設定します。</span><span class="sxs-lookup"><span data-stu-id="99850-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="99850-109">最初に、各法人で実行される会社間の減価償却で使用するジャーナルを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99850-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="99850-110">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="99850-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="99850-111">固定資産提案セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="99850-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="99850-112">法人組織の各転記階層に使用する仕訳帳名を含むレコードを登録します。</span><span class="sxs-lookup"><span data-stu-id="99850-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="99850-113">伝票が総勘定元帳に転記されない場合、未転記レイヤーは、関連する仕訳で選択される必要があります。</span><span class="sxs-lookup"><span data-stu-id="99850-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="99850-114">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99850-114">Click Add.</span></span> 
4. <span data-ttu-id="99850-115">[転記階層] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="99850-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="99850-116">[仕訳帳名] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="99850-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="99850-117">各法人の固定資産のパラメータのページで仕訳帳の設定を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="99850-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="99850-118">下位タスク: 減価償却額を計算します。</span><span class="sxs-lookup"><span data-stu-id="99850-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="99850-119">法人間で減価償却を開始するには、[減価償却提案の作成] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="99850-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="99850-120">[固定資産] > [仕訳入力] > [償却提案の作成] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="99850-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="99850-121">[転記階層] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="99850-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="99850-122">仕訳帳名は固定資産のパラメータが既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="99850-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="99850-123">現在の法人をここで変更できます。</span><span class="sxs-lookup"><span data-stu-id="99850-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="99850-124">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="99850-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="99850-125">減価償却の対象として法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="99850-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="99850-126">固定資産パラメータページで固定資産提案に対して設定された仕訳を持つ法人のみがリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="99850-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="99850-127">有効になっている場合、転記仕訳帳のオプションは、減価償却の仕訳帳が作成されると自動的に転記します。</span><span class="sxs-lookup"><span data-stu-id="99850-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="99850-128">選択されていない場合、仕訳帳は作成されるが転記されないため、転記の前に詳細を確認できます。</span><span class="sxs-lookup"><span data-stu-id="99850-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="99850-129">[仕訳帳の転記] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="99850-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="99850-130">フィルター フィールドには、この減価償却実行に対して選択された法人のすべての固定資産、グループ、および帳簿が含まれます。</span><span class="sxs-lookup"><span data-stu-id="99850-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="99850-131">バッチ処理オプションが既定で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="99850-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="99850-132">このオプションを有効にすると、減価償却の仕訳帳の作成と転記がバック グラウンドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="99850-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="99850-133">[仕訳帳の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99850-133">Click Create journal.</span></span> 
10. <span data-ttu-id="99850-134">それぞれの法人で作成された減価償却の仕訳帳を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99850-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="99850-135">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="99850-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

