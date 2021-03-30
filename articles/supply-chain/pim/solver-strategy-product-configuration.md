---
title: 製品コンフィギュレーションのソルバー戦略
description: このトピックでは、製品のコンフィギュレーションのパフォーマンスを向上させるためにソルバー戦略を使用する方法について説明します。
author: cvocph
manager: tfehr
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c368fe3ede2818f28e2063ae22cdfd49cd9bc68f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244186"
---
# <a name="solver-strategy-for-product-configuration"></a><span data-ttu-id="00dab-103">製品コンフィギュレーションのソルバー戦略</span><span class="sxs-lookup"><span data-stu-id="00dab-103">Solver strategy for product configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00dab-104">このトピックでは、製品のコンフィギュレーションのパフォーマンスを向上させるためにソルバー戦略を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="00dab-104">This topic describes how you can use the solver strategy to improve the performance of product configuration.</span></span>

<span data-ttu-id="00dab-105">ソルバー戦略の概念は最初に Microsoft Dynamics AX 2012 R2 の累積更新プログラム 7 (CU7) に導入されました。</span><span class="sxs-lookup"><span data-stu-id="00dab-105">The concept of solver strategies was first introduced in Cumulative update 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span></span> <span data-ttu-id="00dab-106">そして、Microsoft Dynamics AX 2012 R3 と Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 の累積更新プログラム 8 (CU8) に拡張されました。</span><span class="sxs-lookup"><span data-stu-id="00dab-106">It was extended in Cumulative update 8 (CU8) for Microsoft Dynamics AX 2012 R3 and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>

<span data-ttu-id="00dab-107">現在、ソルバー戦略概念は次の方法で構成されています。</span><span class="sxs-lookup"><span data-stu-id="00dab-107">The solver strategy concept now consists of the following strategies:</span></span>

- <span data-ttu-id="00dab-108">既定</span><span class="sxs-lookup"><span data-stu-id="00dab-108">Default</span></span>
- <span data-ttu-id="00dab-109">最小ドメインを先頭にする</span><span class="sxs-lookup"><span data-stu-id="00dab-109">Minimal domains first</span></span>
- <span data-ttu-id="00dab-110">トップダウン</span><span class="sxs-lookup"><span data-stu-id="00dab-110">Top-down</span></span>
- <span data-ttu-id="00dab-111">Z3</span><span class="sxs-lookup"><span data-stu-id="00dab-111">Z3</span></span>

## <a name="solver-strategy"></a><span data-ttu-id="00dab-112">ソルバー戦略</span><span class="sxs-lookup"><span data-stu-id="00dab-112">Solver strategy</span></span> 

<span data-ttu-id="00dab-113">製品コンフィギュレーション モデルは、[制約充足問題 (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf) として作成できます。</span><span class="sxs-lookup"><span data-stu-id="00dab-113">A product configuration model can be formulated as a [constraint satisfaction problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span></span> <span data-ttu-id="00dab-114">Microsoft Solver Foundation (MSF) では、製品コンフィギュレーション モデルから使用できる CSPs を解決するために、ソルバー戦略の 2 つのタイプを提供します。</span><span class="sxs-lookup"><span data-stu-id="00dab-114">Microsoft Solver Foundation (MSF) provides two types of solver strategies to solve the CSPs that can be used from product configuration models.</span></span> <span data-ttu-id="00dab-115">これらのソルバー戦略は、[ヒューリスティック](https://techterms.com/definition/heuristic) に依存しています。これらは、問題が解決されたときに CSPs の変数が考慮される順序を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="00dab-115">These solver strategies rely on [heuristics](https://techterms.com/definition/heuristic), which are used to determine the order that the variables of the CSPs are considered in when the problem is being solved.</span></span> <span data-ttu-id="00dab-116">ヒューリスティックは、問題または問題のクラスが解決されているときに、パフォーマンスに大きな影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="00dab-116">Heuristics can significantly affect performance when a problem or class of problems is being solved.</span></span>

<span data-ttu-id="00dab-117">製品コンフィギュレーション モデルのソルバー戦略は、どのソルバーがヒューリスティックで使用されているかを決定します。</span><span class="sxs-lookup"><span data-stu-id="00dab-117">The solver strategy for product configuration models determines which solver is used with heuristics.</span></span> <span data-ttu-id="00dab-118">**既定の**、**最小ドメインを先頭にする**、および **トップダウン** の戦略は MSF から 2 つのソルバーを使用します。一方、**Z3** 戦略は Z3 ソルバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="00dab-118">The **Default**, **Minimal domains first**, and **Top-down** strategies use the two solvers from MSF, whereas the **Z3** strategy uses the Z3 solver.</span></span> 

<span data-ttu-id="00dab-119">実際の顧客実装調査によると、製品コンフィギュレーション モデルのソルバー戦略の変更が、応答時間を数分から数ミリ秒に短縮することが可能だと示しています。</span><span class="sxs-lookup"><span data-stu-id="00dab-119">Real customer implementation studies have shown that a change in the solver strategy for a product configuration model can reduce the response time from minutes to milliseconds.</span></span> <span data-ttu-id="00dab-120">したがって、製品コンフィギュレーション モデルの最も効率的な戦略を見つけるため、さまざまなソルバー戦略に挑戦する価値はあります。</span><span class="sxs-lookup"><span data-stu-id="00dab-120">Therefore, it's worth the effort to try different solver strategies to find the most efficient strategy for your product configuration model.</span></span>

## <a name="change-the-settings-for-the-solver-strategy"></a><span data-ttu-id="00dab-121">ソルバー戦略の設定を変更</span><span class="sxs-lookup"><span data-stu-id="00dab-121">Change the settings for the solver strategy</span></span>

<span data-ttu-id="00dab-122">ソルバー戦略を変更するには、アクション ペイン上の **製品コンフィギュレーション モデル** ページで、**モデルのプロパティ** を選びます。</span><span class="sxs-lookup"><span data-stu-id="00dab-122">To change the solver strategy, on the **Product configuration models** page, on the Action Pane, select **Model properties**.</span></span> <span data-ttu-id="00dab-123">そして、**モデルの詳細の編集** ダイアログ ボックスで、ソルバー戦略を選択します。</span><span class="sxs-lookup"><span data-stu-id="00dab-123">Then, in the **Edit the model details** dialog box, select a solver strategy.</span></span>

<span data-ttu-id="00dab-124">[![ソルバー戦略を変更](./media/solver-strategy.png)](./media/solver-strategy.png)</span><span class="sxs-lookup"><span data-stu-id="00dab-124">[![Changing the solver strategy](./media/solver-strategy.png)](./media/solver-strategy.png)</span></span>

<span data-ttu-id="00dab-125">現時点では、どのソルバー戦略が制約ベースの製品コンフィギュレーションの最も効率的な戦略になるかを自動的に検出するロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="00dab-125">Currently, there is no logic that automatically detects which solver strategy will be the most efficient strategy for constraint-based product configuration.</span></span> <span data-ttu-id="00dab-126">そのため、1 つずつソルバー戦略を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="00dab-126">Therefore, you must try the solver strategies one by one.</span></span>

<span data-ttu-id="00dab-127">次の表では、さまざまなシナリオで使用するソルバー戦略に関する推奨事項を提供します。</span><span class="sxs-lookup"><span data-stu-id="00dab-127">The following table provides recommendations about the solver strategy to use in various scenarios.</span></span>

| <span data-ttu-id="00dab-128">ソルバー戦略</span><span class="sxs-lookup"><span data-stu-id="00dab-128">Solver strategy</span></span>      | <span data-ttu-id="00dab-129">このシナリオの戦略を使用</span><span class="sxs-lookup"><span data-stu-id="00dab-129">Use the strategy in this scenario</span></span> |
|----------------------|-----------------------------------|
| <span data-ttu-id="00dab-130">既定</span><span class="sxs-lookup"><span data-stu-id="00dab-130">Default</span></span>              | <span data-ttu-id="00dab-131">**既定の** 戦略は、テーブル制約に依存するモデルを解決するために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="00dab-131">The **Default** strategy has been optimized to solve models that rely on table constraints.</span></span> <span data-ttu-id="00dab-132">顧客実装調査によると、この戦略はテーブル制約が広く使用されているシナリオで最も効率的な戦略だと示しています。</span><span class="sxs-lookup"><span data-stu-id="00dab-132">Customer implementation studies have shown that this strategy is the most efficient strategy in scenarios where table constraints are used extensively.</span></span> |
| <span data-ttu-id="00dab-133">最小ドメインを先頭にする</span><span class="sxs-lookup"><span data-stu-id="00dab-133">Minimal domains first</span></span> | <span data-ttu-id="00dab-134">**最小限ドメインを先頭にする** および **トップダウン** 戦略は、密接な関係です。</span><span class="sxs-lookup"><span data-stu-id="00dab-134">The **Minimal domains first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="00dab-135">顧客実装調査は、**トップダウン** 戦略が、**最小ドメインを先頭にする** 戦略より優れていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="00dab-135">Customer implementation studies have shown that the **Top-down** strategy, outperforms the **Minimal domains first** strategy.</span></span> <span data-ttu-id="00dab-136">ただし、**最小ドメインを先頭にする** 戦略は下位互換性の製品に保管されています。</span><span class="sxs-lookup"><span data-stu-id="00dab-136">However, the **Minimal domains first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="00dab-137">これら両方のソルバー戦略は、テーブル制約が使用されないくつかの算術式を含むモデルを解くことでより効率的であることが示されています。</span><span class="sxs-lookup"><span data-stu-id="00dab-137">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="00dab-138">ただし、場合により、**既定** 戦略はこれら 2 つの戦略より優れています。</span><span class="sxs-lookup"><span data-stu-id="00dab-138">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="00dab-139">そのため、それぞれの戦略を試してください。</span><span class="sxs-lookup"><span data-stu-id="00dab-139">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="00dab-140">トップダウン</span><span class="sxs-lookup"><span data-stu-id="00dab-140">Top-down</span></span>             | <span data-ttu-id="00dab-141">**最小限ドメインを先頭にする** および **トップダウン** 戦略は、密接な関係です。</span><span class="sxs-lookup"><span data-stu-id="00dab-141">The **Minimal domains first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="00dab-142">顧客実装調査は、**トップダウン** 戦略が、**最小ドメインを先頭にする** 戦略より優れていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="00dab-142">Customer implementation studies have shown that the **Top-down** strategy, outperforms the **Minimal domains first** strategy.</span></span> <span data-ttu-id="00dab-143">ただし、**最小ドメインを先頭にする** 戦略は下位互換性の製品に保管されています。</span><span class="sxs-lookup"><span data-stu-id="00dab-143">However, the **Minimal domains first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="00dab-144">これら両方のソルバー戦略は、テーブル制約が使用されないくつかの算術式を含むモデルを解くことでより効率的であることが示されています。</span><span class="sxs-lookup"><span data-stu-id="00dab-144">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="00dab-145">ただし、場合により、**既定** 戦略はこれら 2 つの戦略より優れています。</span><span class="sxs-lookup"><span data-stu-id="00dab-145">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="00dab-146">そのため、それぞれの戦略を試してください。</span><span class="sxs-lookup"><span data-stu-id="00dab-146">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="00dab-147">Z3</span><span class="sxs-lookup"><span data-stu-id="00dab-147">Z3</span></span>                   | <span data-ttu-id="00dab-148">既定のソルバー戦略として、**Z3** 戦略の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="00dab-148">We recommend that you use the **Z3** strategy as the default solver strategy.</span></span> <span data-ttu-id="00dab-149">パフォーマンスとスケーラビリティがについて考慮する場合は、その他の戦略を評価することができます。</span><span class="sxs-lookup"><span data-stu-id="00dab-149">If you're concerned about performance and scalability, you can evaluate the other strategies.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="00dab-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="00dab-150">Additional resources</span></span>

[<span data-ttu-id="00dab-151">製品コンフィギュレーションの概要</span><span class="sxs-lookup"><span data-stu-id="00dab-151">Product configuration overview</span></span>](build-product-configuration-model.md)

[<span data-ttu-id="00dab-152">ヒューリスティック</span><span class="sxs-lookup"><span data-stu-id="00dab-152">Heuristics</span></span>](https://techterms.com/definition/heuristic)

[<span data-ttu-id="00dab-153">制約充足問題</span><span class="sxs-lookup"><span data-stu-id="00dab-153">Constraint Satisfaction Problem</span></span>](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]