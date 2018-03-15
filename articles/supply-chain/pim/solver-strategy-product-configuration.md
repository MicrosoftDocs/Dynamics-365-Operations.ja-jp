---
title: "製品コンフィギュレーションのソルバー戦略"
description: "このトピックでは、製品のコンフィギュレーションのパフォーマンスを向上させるためにソルバー戦略を使用する方法について説明します。"
author: cvocph
manager: AnnBe
ms.date: 01/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 4544128e580b30b14a6236a9a6147ff0a8641d72
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---

# <a name="solver-strategy-for-product-configuration"></a><span data-ttu-id="cdccc-103">製品コンフィギュレーションのソルバー戦略</span><span class="sxs-lookup"><span data-stu-id="cdccc-103">Solver strategy for product configuration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cdccc-104">このトピックでは、製品のコンフィギュレーションのパフォーマンスを向上させるためにソルバー戦略を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cdccc-104">This topic describes how you can use the solver strategy to improve the performance of product configuration.</span></span>

<span data-ttu-id="cdccc-105">ソルバー戦略の概念は最初に Microsoft Dynamics AX 2012 R2 の累積更新プログラム (CU7) に導入されました。</span><span class="sxs-lookup"><span data-stu-id="cdccc-105">The concept of solver strategies was first introduced in Cumulative update 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span></span> <span data-ttu-id="cdccc-106">そして、Microsoft Dynamics AX 2012 R3 と Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 の累積更新プログラム 8 (CU8) に拡張されました。</span><span class="sxs-lookup"><span data-stu-id="cdccc-106">It was extended in Cumulative update 8 (CU8) for Microsoft Dynamics AX 2012 R3 and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>

<span data-ttu-id="cdccc-107">現在、ソルバー戦略概念は次の方法で構成されています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-107">The solver strategy concept now consists of the following strategies:</span></span>

- <span data-ttu-id="cdccc-108">既定</span><span class="sxs-lookup"><span data-stu-id="cdccc-108">Default</span></span>
- <span data-ttu-id="cdccc-109">最小ドメインを先頭にする</span><span class="sxs-lookup"><span data-stu-id="cdccc-109">Minimal domains first</span></span>
- <span data-ttu-id="cdccc-110">トップダウン</span><span class="sxs-lookup"><span data-stu-id="cdccc-110">Top-down</span></span>
- <span data-ttu-id="cdccc-111">Z3</span><span class="sxs-lookup"><span data-stu-id="cdccc-111">Z3</span></span>

## <a name="solver-strategy"></a><span data-ttu-id="cdccc-112">ソルバー戦略</span><span class="sxs-lookup"><span data-stu-id="cdccc-112">Solver strategy</span></span> 

<span data-ttu-id="cdccc-113">製品コンフィギュレーション モデルは、[制約充足問題 (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf) として作成できます。</span><span class="sxs-lookup"><span data-stu-id="cdccc-113">A product configuration model can be formulated as a [constraint satisfaction problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span></span> <span data-ttu-id="cdccc-114">Microsoft Solver Foundation (MSF) では、製品コンフィギュレーション モデルから使用できる CSPs を解決するために、ソルバー戦略の 2 つのタイプを提供します。</span><span class="sxs-lookup"><span data-stu-id="cdccc-114">Microsoft Solver Foundation (MSF) provides two types of solver strategies to solve the CSPs that can be used from product configuration models.</span></span> <span data-ttu-id="cdccc-115">これらのソルバー戦略は、[ヒューリスティック](https://techterms.com/definition/heuristic) に依存しています。これらは、問題が解決されたときに CSPs の変数が考慮される順序を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cdccc-115">These solver strategies rely on [heuristics](https://techterms.com/definition/heuristic), which are used to determine the order that the variables of the CSPs are considered in when the problem is being solved.</span></span> <span data-ttu-id="cdccc-116">ヒューリスティックは、問題または問題のクラスが解決されているときに、パフォーマンスに大きな影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cdccc-116">Heuristics can significantly affect performance when a problem or class of problems is being solved.</span></span>

<span data-ttu-id="cdccc-117">Finance and Operations において、製品コンフィギュレーション モデルのソルバー戦略は、どのソルバーがヒューリスティックで使用されているかを決定します。</span><span class="sxs-lookup"><span data-stu-id="cdccc-117">In Finance and Operations, the solver strategy for product configuration models determines which solver is used with heuristics.</span></span> <span data-ttu-id="cdccc-118">[**既定の**]、[**最小ドメインを先頭にする**]、および [**トップダウン**] の戦略は MSF から 2 つのソルバーを使用します。一方、[**Z3**] 戦略は Z3 ソルバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="cdccc-118">The **Default**, **Minimal domains first**, and **Top-down** strategies use the two solvers from MSF, whereas the **Z3** strategy uses the Z3 solver.</span></span> 

<span data-ttu-id="cdccc-119">実際の顧客実装調査によると、製品コンフィギュレーション モデルのソルバー戦略の変更が、応答時間を数分から数ミリ秒に短縮することが可能だと示しています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-119">Real customer implementation studies have shown that a change in the solver strategy for a product configuration model can reduce the response time from minutes to milliseconds.</span></span> <span data-ttu-id="cdccc-120">したがって、製品コンフィギュレーション モデルの最も効率的な戦略を見つけるため、さまざまなソルバー戦略に挑戦する価値はあります。</span><span class="sxs-lookup"><span data-stu-id="cdccc-120">Therefore, it's worth the effort to try different solver strategies to find the most efficient strategy for your product configuration model.</span></span>

## <a name="change-the-settings-for-the-solver-strategy"></a><span data-ttu-id="cdccc-121">ソルバー戦略の設定を変更</span><span class="sxs-lookup"><span data-stu-id="cdccc-121">Change the settings for the solver strategy</span></span>

<span data-ttu-id="cdccc-122">ソルバー戦略を変更するには、アクション ペイン上の [**製品コンフィギュレーション モデル**] ページで、[**モデルのプロパティ**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="cdccc-122">To change the solver strategy, on the **Product configuration models** page, on the Action Pane, select **Model properties**.</span></span> <span data-ttu-id="cdccc-123">そして、[**モデルの詳細の編集**] ダイアログ ボックスで、ソルバー戦略を選択します。</span><span class="sxs-lookup"><span data-stu-id="cdccc-123">Then, in the **Edit the model details** dialog box, select a solver strategy.</span></span>

<span data-ttu-id="cdccc-124">[![ソルバー戦略を変更](./media/solver-strategy.png)](./media/solver-strategy.png)</span><span class="sxs-lookup"><span data-stu-id="cdccc-124">[![Changing the solver strategy](./media/solver-strategy.png)](./media/solver-strategy.png)</span></span>

<span data-ttu-id="cdccc-125">現時点では、どのソルバー戦略が制約ベースの製品コンフィギュレーションの最も効率的な戦略になるかを自動的に検出するロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="cdccc-125">Currently, there is no logic that automatically detects which solver strategy will be the most efficient strategy for constraint-based product configuration.</span></span> <span data-ttu-id="cdccc-126">そのため、1 つずつソルバー戦略を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdccc-126">Therefore, you must try the solver strategies one by one.</span></span>

<span data-ttu-id="cdccc-127">次の表では、さまざまなシナリオで使用するソルバー戦略に関する推奨事項を提供します。</span><span class="sxs-lookup"><span data-stu-id="cdccc-127">The following table provides recommendations about the solver strategy to use in various scenarios.</span></span>

| <span data-ttu-id="cdccc-128">ソルバー戦略</span><span class="sxs-lookup"><span data-stu-id="cdccc-128">Solver strategy</span></span>      | <span data-ttu-id="cdccc-129">このシナリオの戦略を使用</span><span class="sxs-lookup"><span data-stu-id="cdccc-129">Use the strategy in this scenario</span></span> |
|----------------------|-----------------------------------|
| <span data-ttu-id="cdccc-130">既定</span><span class="sxs-lookup"><span data-stu-id="cdccc-130">Default</span></span>              | <span data-ttu-id="cdccc-131">[**既定の**] 戦略は、テーブル制約に依存するモデルを解決するために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-131">The **Default** strategy has been optimized to solve models that rely on table constraints.</span></span> <span data-ttu-id="cdccc-132">顧客実装調査によると、この戦略はテーブル制約が広く使用されているシナリオで最も効率的な戦略だと示しています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-132">Customer implementation studies have shown that this strategy is the most efficient strategy in scenarios where table constraints are used extensively.</span></span> |
| <span data-ttu-id="cdccc-133">最小ドメインを先頭にする</span><span class="sxs-lookup"><span data-stu-id="cdccc-133">Minimal domain first</span></span> | <span data-ttu-id="cdccc-134">[**最小限ドメインを先頭にする**] および [**トップダウン**] 戦略は、密接な関係です。</span><span class="sxs-lookup"><span data-stu-id="cdccc-134">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="cdccc-135">顧客実装調査によると、CU8 に導入された [**トップダウン**] 戦略が、[**最小ドメインを先頭にする**] 戦略より優れていることを示します。</span><span class="sxs-lookup"><span data-stu-id="cdccc-135">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="cdccc-136">ただし、[**最小ドメインを先頭にする**] 戦略は下位互換性の製品に保管されています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-136">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="cdccc-137">これら両方のソルバー戦略は、テーブル制約が使用されないくつかの算術式を含むモデルを解くことでより効率的であることが示されています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-137">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="cdccc-138">ただし、場合により、[**既定**] 戦略はこれら 2 つの戦略より優れています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-138">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="cdccc-139">そのため、それぞれの戦略を試してください。</span><span class="sxs-lookup"><span data-stu-id="cdccc-139">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="cdccc-140">トップダウン</span><span class="sxs-lookup"><span data-stu-id="cdccc-140">Top-down</span></span>             | <span data-ttu-id="cdccc-141">[**最小限ドメインを先頭にする**] および [**トップダウン**] 戦略は、密接な関係です。</span><span class="sxs-lookup"><span data-stu-id="cdccc-141">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="cdccc-142">顧客実装調査によると、CU8 に導入された [**トップダウン**] 戦略が、[**最小ドメインを先頭にする**] 戦略より優れていることを示します。</span><span class="sxs-lookup"><span data-stu-id="cdccc-142">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="cdccc-143">ただし、[**最小ドメインを先頭にする**] 戦略は下位互換性の製品に保管されています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-143">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="cdccc-144">これら両方のソルバー戦略は、テーブル制約が使用されないくつかの算術式を含むモデルを解くことでより効率的であることが示されています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-144">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="cdccc-145">ただし、場合により、[**既定**] 戦略はこれら 2 つの戦略より優れています。</span><span class="sxs-lookup"><span data-stu-id="cdccc-145">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="cdccc-146">そのため、それぞれの戦略を試してください。</span><span class="sxs-lookup"><span data-stu-id="cdccc-146">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="cdccc-147">Z3</span><span class="sxs-lookup"><span data-stu-id="cdccc-147">Z3</span></span>                   | <span data-ttu-id="cdccc-148">既定のソルバー戦略として、[**Z3**] 戦略の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cdccc-148">We recommend that you use the **Z3** strategy as the default solver strategy.</span></span> <span data-ttu-id="cdccc-149">パフォーマンスとスケーラビリティがについて考慮する場合は、その他の戦略を評価することができます。</span><span class="sxs-lookup"><span data-stu-id="cdccc-149">If you're concerned about performance and scalability, you can evaluate the other strategies.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="cdccc-150">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="cdccc-150">Additional resources</span></span>

[<span data-ttu-id="cdccc-151">製品コンフィギュレーション モデルの構築</span><span class="sxs-lookup"><span data-stu-id="cdccc-151">Build product configuration model</span></span>](build-product-configuration-model.md)

[<span data-ttu-id="cdccc-152">ヒューリスティック</span><span class="sxs-lookup"><span data-stu-id="cdccc-152">Heuristics</span></span>](https://techterms.com/definition/heuristic)

[<span data-ttu-id="cdccc-153">制約充足問題</span><span class="sxs-lookup"><span data-stu-id="cdccc-153">Constraint Satisfaction Problem</span></span>](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)

