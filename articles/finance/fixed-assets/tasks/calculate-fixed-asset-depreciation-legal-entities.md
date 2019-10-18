---
title: 法人間での固定資産減価償却の計算
description: 固定資産減価償却は、単一のステップで複数の法人に対して実行することができます。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 500aa71e57f9c1ac8d1a2a080468381bc248741c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187018"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="683d9-103">法人間での固定資産減価償却の計算</span><span class="sxs-lookup"><span data-stu-id="683d9-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="683d9-104">固定資産減価償却は、単一のステップで複数の法人に対して実行することができます。</span><span class="sxs-lookup"><span data-stu-id="683d9-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="683d9-105">この手順では、複数の法人組織に対してプロセスを設定して実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="683d9-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="683d9-106">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="683d9-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="683d9-107">会社間の減価償却実行ジャーナルを設定します</span><span class="sxs-lookup"><span data-stu-id="683d9-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="683d9-108">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="683d9-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="683d9-109">固定資産提案セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="683d9-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="683d9-110">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="683d9-110">Click Add.</span></span>
4. <span data-ttu-id="683d9-111">[転記階層] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="683d9-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="683d9-112">[仕訳帳名] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="683d9-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="683d9-113">各法人の固定資産のパラメータのページで仕訳帳の設定を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="683d9-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="683d9-114">減価償却</span><span class="sxs-lookup"><span data-stu-id="683d9-114">Depreciation run</span></span>
1. <span data-ttu-id="683d9-115">[固定資産] > [仕訳入力] > [償却提案の作成] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="683d9-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="683d9-116">[転記階層] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="683d9-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="683d9-117">仕訳帳名は固定資産のパラメータが既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="683d9-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="683d9-118">現在の法人をここで変更できます。</span><span class="sxs-lookup"><span data-stu-id="683d9-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="683d9-119">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="683d9-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="683d9-120">減価償却の対象として法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="683d9-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="683d9-121">固定資産パラメータページで固定資産提案に対して設定された仕訳を持つ法人のみがリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="683d9-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="683d9-122">[仕訳帳の転記] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="683d9-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="683d9-123">フィルター フィールドには、この減価償却実行に対して選択された法人のすべての固定資産、グループ、および帳簿が含まれます。</span><span class="sxs-lookup"><span data-stu-id="683d9-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="683d9-124">バッチ処理オプションが既定で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="683d9-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="683d9-125">このオプションを有効にすると、減価償却の仕訳帳の作成と転記がバック グラウンドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="683d9-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="683d9-126">[仕訳帳の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="683d9-126">Click Create journal.</span></span>
6. <span data-ttu-id="683d9-127">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="683d9-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
