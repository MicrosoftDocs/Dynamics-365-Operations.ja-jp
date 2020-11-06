---
title: 仕入先の検索
description: 特定の基準に基づく仕入先の検索方法を習得します。
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc28deb979fe8dc4e31befe6d4d5f6f91388f13e
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018055"
---
# <a name="search-for-vendors"></a><span data-ttu-id="3b1d2-103">仕入先の検索</span><span class="sxs-lookup"><span data-stu-id="3b1d2-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b1d2-104">特定の基準に基づく仕入先の検索方法を習得します。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="3b1d2-105">この例では、特定の調達カテゴリに対して承認されていて、特定の国に基本住所をもっている仕入先の検索方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="3b1d2-106">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="3b1d2-107">通常、このタスクを実行するのは、調達担当者です。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="3b1d2-108">[調達] > [仕入先] > [仕入先の検索]の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="3b1d2-109">[調達カテゴリの選択] ページを開くには、プラス アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="3b1d2-110">ツリーで、「CORP PROCUREMENT CATEGORIES\OFFICE MACHINES」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="3b1d2-111">タスク ガイドのこの手順を実行している場合は、正しいノードを選択する前に、[ロック解除] ボタンのクリックが必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="3b1d2-112">USMF を使用していない場合は、カテゴリから 1 つを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="3b1d2-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-113">Click Add.</span></span>
    * <span data-ttu-id="3b1d2-114">複数のカテゴリをここで選択することができます。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="3b1d2-115">これを行う場合は、検索では、少なくとも 1 つのカテゴリに対して承認されている仕入先をすべて探します。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="3b1d2-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-116">Click OK.</span></span>
6. <span data-ttu-id="3b1d2-117">[国/地域] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="3b1d2-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b1d2-118">Click OK.</span></span>

