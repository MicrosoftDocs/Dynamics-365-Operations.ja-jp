---
title: 積荷構築ワークベンチ
description: このトピックでは、積荷構築ワークベンチを操作する方法について説明します。
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b8633adbab43c95366d42cf409f5e508771c906
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809041"
---
# <a name="load-building-workbench"></a><span data-ttu-id="28ee1-103">積荷構築ワークベンチ</span><span class="sxs-lookup"><span data-stu-id="28ee1-103">Load building workbench</span></span>

<span data-ttu-id="28ee1-104">負荷構築ワークベンチを使用すると、荷重を作成するときに荷重構築戦略を適用できます。</span><span class="sxs-lookup"><span data-stu-id="28ee1-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="28ee1-105">積荷構築戦略の作成</span><span class="sxs-lookup"><span data-stu-id="28ee1-105">Create a load building strategy</span></span>

<span data-ttu-id="28ee1-106">積荷構築戦略を使用して自動的に積荷を構築します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="28ee1-107">この機能は、次のような場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="28ee1-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="28ee1-108">特定の製品セットを定期的に出荷する場合は、毎回同じ積荷を構築する必要がないので、積荷戦略で時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="28ee1-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="28ee1-109">積荷が半中途半端になるのを回避して効率を最大にする必要がある場合は、積荷戦略を使用すると、可能な限り多くの積荷を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="28ee1-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="28ee1-110">`TMSLoadBuildingVolumeStrategy` という名前の積荷構築戦略クラスは、*ボリュームベースの積荷構築戦略* という名前の積荷構築戦略を提供します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="28ee1-111">この戦略を使用すると、積荷テンプレートの高さと重量に対して指定される最大値を使用できるし、または新しい値を入力して設定を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="28ee1-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="28ee1-112">この方法は、最初から用意されている唯一の戦略です。</span><span class="sxs-lookup"><span data-stu-id="28ee1-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="28ee1-113">(ただし、いくつかのカスタム戦略がある場合があります。)</span><span class="sxs-lookup"><span data-stu-id="28ee1-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="28ee1-114">最初から用意されている *ボリュームベースの積荷構築戦略* を使用するには、**積荷構築ワークベンチ** ページ (**輸送管理 &gt; 計画 &gt; 積荷構築ワークベンチ**) の **積荷構築戦略** フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="28ee1-115">積荷構築戦略を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28ee1-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="28ee1-116">**輸送管理 &gt; 設定 &gt; 積荷構築 &gt; 積荷構築戦略** に移動します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="28ee1-117">アクション ウィンドウの **クラスリストの生成** を選択し、利用可能なすべてのクラスの最新バージョンがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="28ee1-118">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="28ee1-119">戦略の一意の名前を入力し、それに対して積荷構築計画クラスを選択し、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="28ee1-120">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="28ee1-121">アクション ウィンドウで、**パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="28ee1-122">**積荷構築戦略パラメータ** ページで、一覧から **容積能力** を選択し、**値** フィールドに、新しい積荷構築戦略に適用する積荷の合計容積能力の割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="28ee1-123">一覧から **可搬重量** を選択し、**値** フィールドに、新しい積荷構築戦略に適用する積荷の合計可搬重量の割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="28ee1-124">**積荷構築戦略パラメータ** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="28ee1-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="28ee1-125">**積荷構築戦略** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="28ee1-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="28ee1-126">これで、積荷構築戦略を積荷構築テンプレートに割り当てることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="28ee1-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="28ee1-127">また、それを積荷計画ワークベンチで直接使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="28ee1-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="28ee1-128">積荷構築ワークベンチでの積荷構築戦略の使用</span><span class="sxs-lookup"><span data-stu-id="28ee1-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="28ee1-129">**配送管理 &gt; 計画 &gt; 積荷構築ワークベンチ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="28ee1-130">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="28ee1-131">**積荷構築戦略** フィールドで戦略を選択します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="28ee1-132">積荷構築テンプレートを定義して、それに積荷構築戦略を割り当てた場合は、アクション ウィンドウの **テンプレートの管理** タブで、**テンプレートの適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="28ee1-133">次に、**構築テンプレートの適用** ドロップダウン ダイアログ ボックスで、**積荷構築テンプレート名** フィールドのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="28ee1-134">**積荷テンプレート シーケンス** クイック タブで、1 つまたは複数の[積荷テンプレート](load-template.md)を選択します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="28ee1-135">ワークベンチは、ここで指定された順序で、これらのタイプのコンテナーに負荷を適合させようとします。</span><span class="sxs-lookup"><span data-stu-id="28ee1-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="28ee1-136">通常、リストの一番上に最小のコンテナーを配置して、可能な限り最小のコンテナーが最初に選択されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28ee1-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="28ee1-137">アクション ウィンドウで、**積荷の提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="28ee1-138">提案された積荷および積荷明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="28ee1-139">アクション ウィンドウで **積荷の作成** を選択して、**積荷明細行の提案** クイック タブの元伝票明細行に基づく積荷を作成します。</span><span class="sxs-lookup"><span data-stu-id="28ee1-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="28ee1-140">**積荷構築ワークベンチ** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="28ee1-140">Close the **Load building workbench** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]