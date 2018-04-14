---
title: "新規製造品目の標準原価の更新"
description: "この記事は、新規製造品目の標準原価の更新についてのガイダンスを提供します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f60f7932ce79b23b1656d6947fcb321f9484869d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="update-standard-costs-for-a-new-manufactured-item"></a><span data-ttu-id="eb4ad-103">新規製造品目の標準原価の更新</span><span class="sxs-lookup"><span data-stu-id="eb4ad-103">Update standard costs for a new manufactured item</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="eb4ad-104">この記事は、新規製造品目の標準原価の更新についてのガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-104">This article provides guidance for updating standard costs for a new manufactured item.</span></span> 

<span data-ttu-id="eb4ad-105">次のガイドラインでは、標準原価の更新に 2 バージョンによるアプローチを使用することを想定しています。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-105">The following guidelines assume that you use a two-version approach to update standard costs.</span></span> <span data-ttu-id="eb4ad-106">この方法では、1 つの原価計算バージョンに、凍結された期間の最初に定義されている標準原価が含まれ、もう 1 つの原価計算バージョンに、新しい製造品目に関係のある差分更新が含まれます。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates that pertain to the new manufactured items.</span></span> <span data-ttu-id="eb4ad-107">差分更新は第 2 の原価計算バージョンに原価レコードとして入力され、最終的には有効になります。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-107">The incremental updates are entered as cost records in the second costing version, and eventually they are enabled.</span></span> <span data-ttu-id="eb4ad-108">2 バージョン方式では第 2 の原価バージョンを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-108">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="eb4ad-109">原価バージョンの定義に関するガイドラインは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-109">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="eb4ad-110">[**標準原価**] の原価タイプを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-110">Assign a costing type of **Standard cost**.</span></span>
-   <span data-ttu-id="eb4ad-111">**2016-UPDATES** など、原価バージョンの内容を示すわかりやすい識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-111">Assign a significant identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="eb4ad-112">[**価格タイプを許可**] フィールド グループで、[**原価価格**] が [**はい**] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-112">In the **Allow price types** field group, make sure that **Cost price** is set to **Yes**.</span></span>
-   <span data-ttu-id="eb4ad-113">すべてのサイトの原価レコードの入力を許可します (つまり、[**サイト**] フィールドを空白のままにします)。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-113">Allow cost records to be entered for all sites (that is, leave the **Site** field blank).</span></span> <span data-ttu-id="eb4ad-114">サイトを入力すると、原価レコードはそのサイトに対してのみ入力できます。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-114">If you enter a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="eb4ad-115">[**有効**] の予備原則を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-115">Use a fallback principle of **Active**.</span></span>

<span data-ttu-id="eb4ad-116">凍結された期間全体に新しい製造品目を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-116">To add new manufacturing items throughout the frozen period, follow these steps.</span></span>

1.  <span data-ttu-id="eb4ad-117">差分更新を含む 2 番目の原価計算バージョンに入力する原価レコードを有効にするには [**原価バージョン設定**] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-117">Use the **Costing version setup** page to enable cost records to be entered into the second costing version that contains the incremental updates.</span></span> <span data-ttu-id="eb4ad-118">保留中原価の有効化を禁止します。その場合、有効化は、保留中原価を完全かつ正確に定義した後で許可されます。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-118">Prevent the activation of pending costs, where activation is allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="eb4ad-119">原価バージョンのポリシーとして空白の開始日を指定し、各原価レコードを入力するときに開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-119">Indicate a blank from-date as a policy in the costing version, and then enter the from-date when you enter each cost record.</span></span> <span data-ttu-id="eb4ad-120">開始日は、新しい品目が購入または製造されるより前の日付を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-120">The from-date should represent a date before the new items are purchased or manufactured.</span></span>
2.  <span data-ttu-id="eb4ad-121">[**品目価格**] ページを使用して、新しい購入品目の原価レコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-121">Use the **Item price** page to enter cost records for new purchased items.</span></span> <span data-ttu-id="eb4ad-122">原価レコードごとに、差分更新を含む原価バージョンを入力し、新しい製造品目の予定製造日より前の開始日を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-122">For each cost record, enter the costing version that contains incremental updates, and use a from-date that comes before the expected manufacturing date for new manufactured items.</span></span>
3.  <span data-ttu-id="eb4ad-123">[**計算**] ページを使用して、新しい製造品目の原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-123">Calculate the cost of new manufactured items by using the **Calculation** page.</span></span> <span data-ttu-id="eb4ad-124">[**原価バージョンの保守**] ページから [**計算**] ページを開き、差分更新を含む原価計算バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-124">Open the **Calculation** page from the **Costing version maintenance** page, and then select the costing version that contains the incremental updates.</span></span> <span data-ttu-id="eb4ad-125">選択条件を使用して、新しい製造品目とその任意の製造コンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-125">Use the selection criteria to specify the new manufactured item and any one of its manufactured components.</span></span> <span data-ttu-id="eb4ad-126">複数レベルの製品構造では、新しい製造品目をコンポーネントとして含む任意の親品目を指定することも必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-126">In a multilevel product structure, you might also have to specify any parent item that contains the new manufactured items as a component.</span></span> <span data-ttu-id="eb4ad-127">新しい製造品目の製造の開始に対応する部品表 (BOM) 計算の開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-127">Enter a from-date for the bill of materials (BOM) calculation that corresponds to the start of manufacturing for the new manufactured items.</span></span> <span data-ttu-id="eb4ad-128">有効日は、品目の BOM バージョンおよび工順バージョンの有効日の範囲内である必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-128">The from-date should be in the effective dates for the item’s BOM version and route version.</span></span> <span data-ttu-id="eb4ad-129">**メモ:** 原価レコードが見つからない場合は、それが新しい製造品目である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-129">**Note:** A missing cost record can indicate a new manufactured item.</span></span> <span data-ttu-id="eb4ad-130">BOM 計算は、原価が見つからない品目に限定できます。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-130">BOM calculations can be limited to items that have missing costs.</span></span>
4.  <span data-ttu-id="eb4ad-131">新しい製造品目に対して計算された原価が完全で正しいことを検証します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-131">Verify the completeness and accuracy of the calculated costs for new manufactured items.</span></span> <span data-ttu-id="eb4ad-132">各品目原価レコードに対して算出された原価、および警告メッセージの情報ログを確認するには、[**完了**] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-132">Use the **Complete** page to review the calculated costs for each item cost record, and also review any Infolog warning messages.</span></span> <span data-ttu-id="eb4ad-133">または、[**計算**] ページを使用して、計算された原価の一覧を確認します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-133">Alternatively, use the **Calculation** page to review the calculated costs.</span></span>
5.  <span data-ttu-id="eb4ad-134">[**原価バージョン設定**] ページを使用して、2 番目の原価バージョンの保留中の原価レコードを有効化できるように、ブロック フラグを変更します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-134">Use the **Costing version setup** page to change the blocking flag to allow activation of the pending cost records in the second costing version.</span></span>
6.  <span data-ttu-id="eb4ad-135">[**価格の有効化**] ページ ([**原価バージョンの保守**] ページから開く) を使用して、2 番目の原価バージョンのすべての保留中の原価レコードを有効化できます。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-135">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to enable all pending cost records in the second costing version.</span></span> <span data-ttu-id="eb4ad-136">[**品目価格**] ページの [**有効化**] ボタンをクリックすることにより、個々の品目の保留中の原価レコードを有効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-136">You can also enable the pending cost records for individual items by clicking the **Activate** button on the **Item price** page.</span></span>
7.  <span data-ttu-id="eb4ad-137">追加のデータ管理を禁止するには、[**原価バージョン設定**] ページを使用して、2 番目の原価バージョンのブロック フラグを変更します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-137">Use the **Costing version setup** page to change the blocking flags in the second costing version to prevent additional data maintenance.</span></span> <span data-ttu-id="eb4ad-138">ブロック ポリシーは、新しい保留中の原価の入力と、保留中の原価の有効化を禁止します。</span><span class="sxs-lookup"><span data-stu-id="eb4ad-138">The blocking policies prevent the entry of new pending costs and the activation of pending costs.</span></span>





