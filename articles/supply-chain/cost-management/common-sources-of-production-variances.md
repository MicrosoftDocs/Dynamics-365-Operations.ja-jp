---
title: 製造差異の一般的な発生源
description: この記事は、製造差異のタイプごとの一般的な発生源について説明します。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55d108ff71f0af773fa521833d57ce96d36251fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008244"
---
# <a name="common-sources-of-production-variances"></a><span data-ttu-id="cf23c-103">製造差異の一般的な発生源</span><span class="sxs-lookup"><span data-stu-id="cf23c-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf23c-104">この記事は、製造差異のタイプごとの一般的な発生源について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf23c-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="cf23c-105">**ロット サイズ** の差異の一般的な発生源を次に示します。</span><span class="sxs-lookup"><span data-stu-id="cf23c-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="cf23c-106">製造オーダーの商品数量が、標準原価計算で使用される計算数量と異なる。</span><span class="sxs-lookup"><span data-stu-id="cf23c-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="cf23c-107">この数量は、固定費を償却するための基準を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf23c-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="cf23c-108">製造オーダー内の固定費の金額が、標準原価計算で使用される固定費と異なる。</span><span class="sxs-lookup"><span data-stu-id="cf23c-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="cf23c-109">製造オーダー内の固定費は、さまざまな理由で異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cf23c-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="cf23c-110">たとえば、固定費には次の要因が反映されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="cf23c-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="cf23c-111">生産部品表 (BOM) または工順の手動による変更</span><span class="sxs-lookup"><span data-stu-id="cf23c-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="cf23c-112">製造オーダーを作成時に異なる BOM バージョンまたは工順バージョンの選択</span><span class="sxs-lookup"><span data-stu-id="cf23c-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="cf23c-113">品目に割り当てられる BOM バージョンまたは工順バージョンの計画技術変更</span><span class="sxs-lookup"><span data-stu-id="cf23c-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="cf23c-114">**生産価格** の差異の一般的な発生源を次に示します。</span><span class="sxs-lookup"><span data-stu-id="cf23c-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="cf23c-115">報告された工順工程の消費に対する原価カテゴリ (および原価カテゴリ価格) が、標準原価計算で使用される原価カテゴリと異なる。</span><span class="sxs-lookup"><span data-stu-id="cf23c-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="cf23c-116">原価カテゴリ価格の有効原価が、標準原価計算で使用される原価カテゴリ価格と異なる。</span><span class="sxs-lookup"><span data-stu-id="cf23c-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="cf23c-117">**生産数量** の差異の一般的な発生源を次に示します。</span><span class="sxs-lookup"><span data-stu-id="cf23c-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="cf23c-118">材料コンポーネントの過剰出庫または過少出庫。</span><span class="sxs-lookup"><span data-stu-id="cf23c-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="cf23c-119">工順工程の過剰レポート時間または過少レポート時間。</span><span class="sxs-lookup"><span data-stu-id="cf23c-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="cf23c-120">注文数量に比例した親品目の適正数量からの過剰入庫または過少入庫。</span><span class="sxs-lookup"><span data-stu-id="cf23c-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="cf23c-121">ただし、製造オーダー用の注文数量に基づいて、コンポーネントの発行と工程報告は完了しています。</span><span class="sxs-lookup"><span data-stu-id="cf23c-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="cf23c-122">**生産代替** の差異の一般的な発生源を次に示します。</span><span class="sxs-lookup"><span data-stu-id="cf23c-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="cf23c-123">生産 BOM に含まれていない材料コンポーネントの出庫。</span><span class="sxs-lookup"><span data-stu-id="cf23c-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="cf23c-124">生産 BOM にコンポーネントを手動追加し、そのコンポーネントを消費済としてレポート。</span><span class="sxs-lookup"><span data-stu-id="cf23c-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="cf23c-125">品目を生産 BOM に手動追加せずに、消費済としてレポート。</span><span class="sxs-lookup"><span data-stu-id="cf23c-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="cf23c-126">工程を生産工順に手動追加し、その工程を消費済としてレポート。</span><span class="sxs-lookup"><span data-stu-id="cf23c-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="cf23c-127">製造オーダーの作成時に別の BOM バージョンを選択。その BOM バージョンは、標準原価計算で使用されるものと異なっている。</span><span class="sxs-lookup"><span data-stu-id="cf23c-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="cf23c-128">製造オーダーの作成時に別の工順バージョンを選択。その工順バージョンは、標準原価計算で使用されるものと異なっている。</span><span class="sxs-lookup"><span data-stu-id="cf23c-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>




