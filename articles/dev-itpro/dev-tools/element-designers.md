---
title: 要素デザイナー
description: この記事では、要素デザイナーを確認し、それらを使用する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 79871
ms.assetid: 636a4e41-f772-477f-bde8-538a09a79f6e
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3b91aa6f753a05a78c674676b07febe27a2aac5
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833550"
---
# <a name="element-designers"></a><span data-ttu-id="c8bd3-103">要素デザイナー</span><span class="sxs-lookup"><span data-stu-id="c8bd3-103">Element designers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8bd3-104">この記事では、要素デザイナーを確認し、それらを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-104">This topic reviews the element designers and explains how to use them.</span></span> <span data-ttu-id="c8bd3-105">このツールには、プログラム内の要素の種類ごとのデザイナーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-105">The tools contain designers for each kind of element in the program.</span></span> <span data-ttu-id="c8bd3-106">要素を作成または変更するときは、これらのデザイナーを使用します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-106">You use these designers when you create or modify elements.</span></span>

### <a name="open-an-element-designer"></a><span data-ttu-id="c8bd3-107">要素デザイナーを開く</span><span class="sxs-lookup"><span data-stu-id="c8bd3-107">Open an element designer</span></span>

<span data-ttu-id="c8bd3-108">要素デザイナーを開くには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-108">To open an element designer, follow these steps.</span></span>

1.  <span data-ttu-id="c8bd3-109">プロジェクトまたはアプリケーション エクスプ ローラーで要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-109">Find the element in the project or in Application Explorer.</span></span>
2.  <span data-ttu-id="c8bd3-110">要素を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-110">Right-click the element.</span></span> <span data-ttu-id="c8bd3-111">アプリケーション エクスプローラーで、**デザイナーを開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-111">In Application Explorer, click **Open designer**.</span></span> <span data-ttu-id="c8bd3-112">プロジェクトで、**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-112">In the project, click **Open**.</span></span>
3.  <span data-ttu-id="c8bd3-113">要素デザイナーのノードを展開して、要素の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-113">Expand the nodes in the element designer to see the details about the element.</span></span>

### <a name="node-properties"></a><span data-ttu-id="c8bd3-114">ノードのプロパティ</span><span class="sxs-lookup"><span data-stu-id="c8bd3-114">Node properties</span></span>

<span data-ttu-id="c8bd3-115">要素デザイナーで個々のノードを選択すると、Visual Studio の**プロパティ** ウィンドウに、そのノードのさまざまなプロパティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-115">When you select the individual nodes in the element designer, the **Properties** pane in Visual Studio shows the various properties for that node.</span></span> <span data-ttu-id="c8bd3-116">要素の特性のほとんどは、これらのプロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-116">Most of the characteristics of an element are controlled by these properties.</span></span> <span data-ttu-id="c8bd3-117">たとえば、次の図は、FMCustomer テーブルの要素デザイナーを表示します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-117">For example, the following illustration shows the element designer for the FMCustomer table.</span></span> <span data-ttu-id="c8bd3-118">最上位ノードが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-118">Notice that the top-level node is selected.</span></span> 

<span data-ttu-id="c8bd3-119">[![18\_DevoToolsConcept](./media/18_devotoolsconcept.png)](./media/18_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="c8bd3-119">[![18\_DevoToolsConcept](./media/18_devotoolsconcept.png)](./media/18_devotoolsconcept.png)</span></span>

<span data-ttu-id="c8bd3-120">次の図は、選択されているトップレベルのノードに対応する、テーブルのプロパティのセットを示しています。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-120">The following illustration shows the set of properties for the table, which corresponds to the top-level node that is selected.</span></span> 

<span data-ttu-id="c8bd3-121">[![19\_DevoToolsConcept](./media/19_devotoolsconcept.png)](./media/19_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="c8bd3-121">[![19\_DevoToolsConcept](./media/19_devotoolsconcept.png)](./media/19_devotoolsconcept.png)</span></span> 

<span data-ttu-id="c8bd3-122">各要素ノードには、適用される一連のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-122">Each node for the element will have a set of properties that applies to it.</span></span> <span data-ttu-id="c8bd3-123">操作するプロパティを見つけやすいようにするには、**プロパティ** ウィンドウの上部にあるボタンを使用して、表示方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-123">To make it easier to find the properties that you want to work with, use the buttons at the top of the **Properties** pane to control how they are displayed.</span></span> <span data-ttu-id="c8bd3-124">プロパティは、次の方法で配置できます。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-124">The properties can be arranged in the following ways.</span></span>

| <span data-ttu-id="c8bd3-125">組織</span><span class="sxs-lookup"><span data-stu-id="c8bd3-125">Organization</span></span> | <span data-ttu-id="c8bd3-126">説明</span><span class="sxs-lookup"><span data-stu-id="c8bd3-126">Description</span></span>                                                                                                   |
|--------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bd3-127">アルファベット順</span><span class="sxs-lookup"><span data-stu-id="c8bd3-127">Alphabetical</span></span> | <span data-ttu-id="c8bd3-128">アルファベット順にプロパティを配置します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-128">Arrange the properties in alphabetical order.</span></span>                                                                 |
| <span data-ttu-id="c8bd3-129">分類済</span><span class="sxs-lookup"><span data-stu-id="c8bd3-129">Categorized</span></span>  | <span data-ttu-id="c8bd3-130">プロパティをノード タイプの標準カテゴリに配置します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-130">Arrange the properties into standard categories for the node type.</span></span>                                            |
| <span data-ttu-id="c8bd3-131">変更済</span><span class="sxs-lookup"><span data-stu-id="c8bd3-131">Changed</span></span>      | <span data-ttu-id="c8bd3-132">プロパティを、変更されたものとデフォルト値を使用するものに分割します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-132">Divide the properties into those that have been changed and those that use the default values.</span></span>                |
| <span data-ttu-id="c8bd3-133">頻度</span><span class="sxs-lookup"><span data-stu-id="c8bd3-133">Frequency</span></span>    | <span data-ttu-id="c8bd3-134">プロパティが頻繁に、ときどき、または稀に変更されるかどうかに基づき、プロパティをカテゴリに分割します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-134">Divide the properties into categories, based on whether a property is often, occasionally, or rarely changed.</span></span> |

### <a name="working-with-nodes"></a><span data-ttu-id="c8bd3-135">ノードでの作業</span><span class="sxs-lookup"><span data-stu-id="c8bd3-135">Working with nodes</span></span>

<span data-ttu-id="c8bd3-136">要素を作成または変更するとき、その要素のノードの追加または削除が必要ことがよくあります。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-136">When you create or modify elements, you will often find that you must add or remove nodes for the element.</span></span> <span data-ttu-id="c8bd3-137">たとえば、テーブルにフィールドを追加するには、テーブル要素の**フィールド**ノードを右クリックして、**新規**を指し、次に追加するフィールドのタイプをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-137">For example, to add a field to a table, right-click the **Fields** node for the table element, point to **New**, and then click the type of field to add.</span></span> 

<span data-ttu-id="c8bd3-138">[![20\_DevoToolsConcept](./media/20_devotoolsconcept.png)](./media/20_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="c8bd3-138">[![20\_DevoToolsConcept](./media/20_devotoolsconcept.png)](./media/20_devotoolsconcept.png)</span></span> 

<span data-ttu-id="c8bd3-139">ノードを削除するには、そのノードをクリックしてから、**削除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-139">To remove a node, right-click the node, and then click **Delete**.</span></span> <span data-ttu-id="c8bd3-140">ノードのために他のアクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-140">You can also perform other actions for a node.</span></span> <span data-ttu-id="c8bd3-141">ノードの名前を変更したり、ノードを複製したり、ノードの一覧で、上下に移動させたりします。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-141">You rename a node, duplicate a node, or move the node up or down in the node list.</span></span>

### <a name="searching-element-nodes"></a><span data-ttu-id="c8bd3-142">要素のノードを検索中</span><span class="sxs-lookup"><span data-stu-id="c8bd3-142">Searching element nodes</span></span>

<span data-ttu-id="c8bd3-143">場合によっては、要素のノード リストが長くなるため、探している特定のノードが見つけにくくなります。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-143">Sometimes, the node list for an element can be long, so that it's difficult to find the specific node that you're looking for.</span></span> <span data-ttu-id="c8bd3-144">各要素デザイナーの上部に検索バーがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-144">Notice that there is a search bar at the top of each element designer.</span></span> <span data-ttu-id="c8bd3-145">検索する文字列を入力すると、検索文字列に一致するノードのみが含まれるようにノード リストがフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-145">You can enter a string to search for, and the node list will be filtered to include only the nodes that match the search string.</span></span> <span data-ttu-id="c8bd3-146">たとえば、次の図は、「電子メール」検索用語が適用された後の FMCustomer テーブルの要素デザイナーを表示します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-146">For example, the following illustration shows the element designer for the FMCustomer table after the “Email” search term was applied.</span></span> <span data-ttu-id="c8bd3-147">その検索文字列に一致する名前を持つノードのみ要素デザイナーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-147">Only nodes that have names that match that search term appear in the element designer.</span></span> 

<span data-ttu-id="c8bd3-148">[![21\_DevoToolsConcept](./media/21_devotoolsconcept.png)](./media/21_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="c8bd3-148">[![21\_DevoToolsConcept](./media/21_devotoolsconcept.png)](./media/21_devotoolsconcept.png)</span></span> 

<span data-ttu-id="c8bd3-149">カスタマイズ要素または拡張要素を扱っている場合、検索文字列の先頭に **c:** (「カスタマイズ要素」の場合) または **e:** (「拡張要素」の場合) を付けて、カスタマイズまたは拡張機能のみをそれぞれ返すことができます。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-149">If you're working with a customization element or an extension element, you can prefix your search string with **c:** (for "customization elements") or **e:** (for "extension elements") to return only customizations or extensions, respectively.</span></span> <span data-ttu-id="c8bd3-150">**例**</span><span class="sxs-lookup"><span data-stu-id="c8bd3-150">**Examples**</span></span>

-   <span data-ttu-id="c8bd3-151">**e:** は現在の要素に属するすべての拡張子を返します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-151">**e:** returns all extensions that belong to the current element.</span></span>
-   <span data-ttu-id="c8bd3-152">**c:** 現在の要素に属するすべてのカスタマイズを返します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-152">**c:** returns all customizations that belong to the current element.</span></span>
-   <span data-ttu-id="c8bd3-153">**e:Email** は顧客名に文字列「電子メール」が含まれているすべてのカスタマイズ ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-153">**e:Email** returns all extension nodes that have the string "Email" in their name.</span></span>
-   <span data-ttu-id="c8bd3-154">**c:Email** 顧客名に文字列「電子メール」が含まれているすべてのカスタマイズ ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-154">**c:Email** returns all customization nodes that have the string "Email" in their name.</span></span>

### <a name="navigating-to-related-elements"></a><span data-ttu-id="c8bd3-155">関連する要素への移動</span><span class="sxs-lookup"><span data-stu-id="c8bd3-155">Navigating to related elements</span></span>

<span data-ttu-id="c8bd3-156">要素デザイナのノード値は、多くの場合、別の要素への参照です。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-156">The value of a node in the element designer is often a reference to another element.</span></span> <span data-ttu-id="c8bd3-157">たとえば、テーブル要素内のフィールド ノードは、通常拡張データ型 (EDT) 要素に基づいています。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-157">For example, a field node in a table element is typically based on an extended data type (EDT) element.</span></span> <span data-ttu-id="c8bd3-158">要素デザイナーでノードを右クリックするとき、**&lt;要素&gt;に移動** コマンドをクリックして、関連要素に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-158">When you right-click a node in the element designer, you can click the **Go to &lt;element&gt;** command to navigate to that related element.</span></span> <span data-ttu-id="c8bd3-159">たとえば、FMVehicle テーブルのフィールドの一覧で **FuelType** ノードを右クリックするとき、**基本列挙 FMFuelType に移動する**をクリックして、フィールドを定義するために使用される基本列挙を表示します。</span><span class="sxs-lookup"><span data-stu-id="c8bd3-159">For example, when you right-click the **FuelType** node in the list of fields for the FMVehicle table, you can click **Go to Base Enum FMFuelType** to show the base enumeration that is used to define the field.</span></span> 

<span data-ttu-id="c8bd3-160">[![22\_DevoToolsConcept](./media/22_devotoolsconcept.png)](./media/22_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="c8bd3-160">[![22\_DevoToolsConcept](./media/22_devotoolsconcept.png)](./media/22_devotoolsconcept.png)</span></span>



