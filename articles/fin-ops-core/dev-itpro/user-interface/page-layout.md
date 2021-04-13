---
title: Web クライアントのページ レイアウト
description: このトピックでは、Web クライアントのレイアウトについて説明します。 レイアウトは、ページ上にコントロールを表示する方法を指定するデザイン プロセスです。
author: jasongre
ms.date: 01/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 28251
ms.assetid: 1cfa479c-71fa-4eb6-8d12-ad4d65c8ecf3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b23a1d3a90c436d169f8adaa818b7d3baf8bd41
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745705"
---
# <a name="page-layout-in-the-web-client"></a><span data-ttu-id="62a58-104">Web クライアントのページ レイアウト</span><span class="sxs-lookup"><span data-stu-id="62a58-104">Page layout in the web client</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62a58-105">このトピックでは、Web クライアントのレイアウトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="62a58-105">This topic discusses layout in the web client.</span></span> <span data-ttu-id="62a58-106">レイアウトは、ページ上にコントロールを表示する方法を指定するデザイン プロセスです。</span><span class="sxs-lookup"><span data-stu-id="62a58-106">Layout is a design process that specifies how controls appear on a page.</span></span> 

<a name="introduction"></a><span data-ttu-id="62a58-107">はじめに</span><span class="sxs-lookup"><span data-stu-id="62a58-107">Introduction</span></span>
------------

<span data-ttu-id="62a58-108">レイアウトは、ページ上のコントロールを Web クライアントで表示する方法を指定するデザイン プロセスです。</span><span class="sxs-lookup"><span data-stu-id="62a58-108">Layout is a design process that specifies how the controls on a page appear in the web client.</span></span> <span data-ttu-id="62a58-109">レイアウトはコンテナー コントロール内で発生します。</span><span class="sxs-lookup"><span data-stu-id="62a58-109">Layout occurs within container controls.</span></span> <span data-ttu-id="62a58-110">次のテーブルに、コンテナー コントロールの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="62a58-110">The following table lists the container controls.</span></span>

| <span data-ttu-id="62a58-111">コンテナー</span><span class="sxs-lookup"><span data-stu-id="62a58-111">Container</span></span>   | <span data-ttu-id="62a58-112">説明</span><span class="sxs-lookup"><span data-stu-id="62a58-112">Description</span></span>                                                                                                                                            |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a58-113">Form.Design</span><span class="sxs-lookup"><span data-stu-id="62a58-113">Form.Design</span></span> | <span data-ttu-id="62a58-114">ページのルート。</span><span class="sxs-lookup"><span data-stu-id="62a58-114">The root of the page.</span></span> <span data-ttu-id="62a58-115">これは、特殊なコンテナーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="62a58-115">It functions as a special kind of container.</span></span>                                                                                     |
| <span data-ttu-id="62a58-116">グループ化</span><span class="sxs-lookup"><span data-stu-id="62a58-116">Group</span></span>       | <span data-ttu-id="62a58-117">汎用コンテナー コントロール。</span><span class="sxs-lookup"><span data-stu-id="62a58-117">The general-purpose container control.</span></span> <span data-ttu-id="62a58-118">グループ コントロールは必要に応じて入れ子にできます。</span><span class="sxs-lookup"><span data-stu-id="62a58-118">Group controls can be nested as required.</span></span>                                                                       |
| <span data-ttu-id="62a58-119">タブ</span><span class="sxs-lookup"><span data-stu-id="62a58-119">Tab</span></span>         | <span data-ttu-id="62a58-120">TabPage コントロールを含み、**タブ**、**クイックタブ**、**垂直タブ**、および **パノラマ** など多くの **Tab.Style** 値を持つコントロールです。</span><span class="sxs-lookup"><span data-stu-id="62a58-120">A control that contains TabPage controls and has many possible **Tab.Style** values, such as **Tab**, **FastTab**, **Vertical Tab**, and **Panorama**.</span></span> |
| <span data-ttu-id="62a58-121">TabPage</span><span class="sxs-lookup"><span data-stu-id="62a58-121">TabPage</span></span>     | <span data-ttu-id="62a58-122">各 TabPage コントロールの表示形式は、その **Tab.Style** 値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="62a58-122">The appearance of each TabPage control depends on its **Tab.Style** value.</span></span>                                                                             |
| <span data-ttu-id="62a58-123">ボタン グループ</span><span class="sxs-lookup"><span data-stu-id="62a58-123">ButtonGroup</span></span> | <span data-ttu-id="62a58-124">ボタンを含むグループ コントロールの特殊なタイプ。</span><span class="sxs-lookup"><span data-stu-id="62a58-124">A special type of Group control that contains buttons.</span></span>                                                                                                 |

<span data-ttu-id="62a58-125">グリッドとは、柔軟なサイズ変更 (**SizeToAvailable**) などいくつかのコンテナ動作を持つ特殊なタイプのコントロールです。</span><span class="sxs-lookup"><span data-stu-id="62a58-125">A grid is a special type of control that has some container behaviors, such as flexible sizing (**SizeToAvailable**).</span></span> <span data-ttu-id="62a58-126">ただし、グリッドには特別な視覚化があり、汎用のコンテナー コントロールではありません。</span><span class="sxs-lookup"><span data-stu-id="62a58-126">However, a grid has special visualizations and isn't a general-purpose container control.</span></span>

## <a name="layout-dynamics-ax-2012-vs-finance-and-operations-apps"></a><span data-ttu-id="62a58-127">レイアウト: Dynamics AX 2012 vs. Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="62a58-127">Layout: Dynamics AX 2012 vs. Finance and Operations apps</span></span>
### <a name="layout-in-dynamics-ax-2012"></a><span data-ttu-id="62a58-128">Dynamics AX 2012 でのレイアウト</span><span class="sxs-lookup"><span data-stu-id="62a58-128">Layout in Dynamics AX 2012</span></span>

<span data-ttu-id="62a58-129">Microsoft Dynamics AX 2012 では、コンテナーのコントロールの配置はほとんど必ず縦で、列を手動で設定して水平に拡大します。</span><span class="sxs-lookup"><span data-stu-id="62a58-129">In Microsoft Dynamics AX 2012, the arrangement of controls in containers is almost always vertical, and columns are manually set to provide some horizontal spread.</span></span>

### <a name="examples"></a><span data-ttu-id="62a58-130">例</span><span class="sxs-lookup"><span data-stu-id="62a58-130">Examples</span></span>

<span data-ttu-id="62a58-131">**列** = **1** 1 2 3 **列** = **2** 1 4 2 5 3 Dynamics AX 2012 では、**高さ** プロパティと **幅h** プロパティを使用してサイジングできます。</span><span class="sxs-lookup"><span data-stu-id="62a58-131">**Columns**=**1** 1 2 3 **Columns**=**2** 1 4 2 5 3 In Dynamics AX 2012, sizing is achieved via the **Height** and **Width** properties.</span></span> <span data-ttu-id="62a58-132">**高さ** および **幅** が **自動** と設定されている場合、サイズは子コントロールが必要とする大きさになります。</span><span class="sxs-lookup"><span data-stu-id="62a58-132">If **Height** and **Width** are set to **Auto**, the size is as large as the child controls require.</span></span> <span data-ttu-id="62a58-133">**高さ** および **幅** が **列** に設定されている場合、コンテナーは親コンテナー内に収まる大きさになります。</span><span class="sxs-lookup"><span data-stu-id="62a58-133">If **Height** and **Width** are set to **Column**, the container is as large as it can be within the parent container.</span></span> <span data-ttu-id="62a58-134">既定では、**高さ** と **幅** はすべてのコンテナーに対して **自動** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="62a58-134">By default, **Height** and **Width** are set to **Auto** for every container.</span></span>

### <a name="layout-in-finance-and-operations"></a><span data-ttu-id="62a58-135">Finance and Operations のレイアウト</span><span class="sxs-lookup"><span data-stu-id="62a58-135">Layout in Finance and Operations</span></span> 

<span data-ttu-id="62a58-136">Finance and Operations では、レイアウトが Dynamics AX 2012 でのレイアウトを制御する同じ基本的なプロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-136">In Finance and Operations, layout is controlled by the same basic properties that control layout in Dynamics AX 2012.</span></span> <span data-ttu-id="62a58-137">ただし、応答性の良いレイアウトをサポートするため、追加のオプションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="62a58-137">However, additional options have been added to support a more responsive layout.</span></span> <span data-ttu-id="62a58-138">特に、ページのレイアウトは次の要因に基づいています。</span><span class="sxs-lookup"><span data-stu-id="62a58-138">In particular, the layout of a page is based on the following factors:</span></span>

-   <span data-ttu-id="62a58-139">**ArrangeMethod** プロパティによって指定される配置メソッド。</span><span class="sxs-lookup"><span data-stu-id="62a58-139">The arrangement method that is specified by the **ArrangeMethod** property.</span></span>
-   <span data-ttu-id="62a58-140">**列** プロパティで指定された列。</span><span class="sxs-lookup"><span data-stu-id="62a58-140">The columns that are specified by the **Columns** property.</span></span>
-   <span data-ttu-id="62a58-141">**HeightMode**、**WidthMode**、**Height**、**Width** の各プロパティにより指定されているサイズ変更。</span><span class="sxs-lookup"><span data-stu-id="62a58-141">The sizing that is specified by the **HeightMode**, **WidthMode**, **Height**, and **Width** properties.</span></span>

## <a name="arrangemethod-property"></a><span data-ttu-id="62a58-142">ArrangeMethod プロパティ</span><span class="sxs-lookup"><span data-stu-id="62a58-142">ArrangeMethod property</span></span>
<span data-ttu-id="62a58-143">**ArrangeMethod** プロパティは、コンテナーの基準配置方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="62a58-143">The **ArrangeMethod** property specifies a base arrangement method for a container.</span></span> <span data-ttu-id="62a58-144">このプロパティでは、AX 2012 からすべてのオプションが Finance and Operations アプリに設定されています。</span><span class="sxs-lookup"><span data-stu-id="62a58-144">For this property, Finance and Operations apps have all the options from AX 2012.</span></span> <span data-ttu-id="62a58-145">パノラマのタイル レイアウトを対象にした **HorizontalWrap** も含まれています。</span><span class="sxs-lookup"><span data-stu-id="62a58-145">However, they also have a **HorizontalWrap** option that is intended for tile layouts in panoramas.</span></span> <span data-ttu-id="62a58-146">次のテーブルでは、**ArrangeMethod** プロパティのさまざまなオプションについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="62a58-146">The following table describes the various options for the **ArrangeMethod** property.</span></span>

| <span data-ttu-id="62a58-147">オプション</span><span class="sxs-lookup"><span data-stu-id="62a58-147">Option</span></span>          | <span data-ttu-id="62a58-148">説明</span><span class="sxs-lookup"><span data-stu-id="62a58-148">Description</span></span>                                                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a58-149">垂直</span><span class="sxs-lookup"><span data-stu-id="62a58-149">Vertical</span></span>        | <span data-ttu-id="62a58-150">コントロールは垂直に配置されています。</span><span class="sxs-lookup"><span data-stu-id="62a58-150">Controls are arranged vertically.</span></span> <span data-ttu-id="62a58-151">列も使用されている場合は、コントロールは生成された列の内部で垂直方向に配置されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-151">If columns are also used, controls are arranged vertically inside the generated columns.</span></span> <span data-ttu-id="62a58-152">このオプションは、グループおよび **Tab.Style** が **パノラマ** 以外の値に設定されている TabPages の既定値です。</span><span class="sxs-lookup"><span data-stu-id="62a58-152">This option is the default value for Groups and for TabPages where **Tab.Style** is set to a value other than **Panorama**.</span></span> |
| <span data-ttu-id="62a58-153">HorizontalLeft</span><span class="sxs-lookup"><span data-stu-id="62a58-153">HorizontalLeft</span></span>  | <span data-ttu-id="62a58-154">コントロールは水平方向に配置され、親コンテナーの内部で左揃えおよび下揃えになります。</span><span class="sxs-lookup"><span data-stu-id="62a58-154">Controls are arranged horizontally, and they are left-aligned and bottom-aligned inside the parent container.</span></span> |
| <span data-ttu-id="62a58-155">HorizontalRight</span><span class="sxs-lookup"><span data-stu-id="62a58-155">HorizontalRight</span></span> | <span data-ttu-id="62a58-156">コントロールは水平方向に配置され、親コンテナーの内部で右揃えおよび下揃えになります。</span><span class="sxs-lookup"><span data-stu-id="62a58-156">Controls are arranged horizontally, and they are right-aligned and bottom-aligned inside the parent container.</span></span> |
| <span data-ttu-id="62a58-157">HorizontalWrap</span><span class="sxs-lookup"><span data-stu-id="62a58-157">HorizontalWrap</span></span>  | <span data-ttu-id="62a58-158">コントロールは水平方向に折り返された固定幅の列の内側に配置されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-158">Controls are arranged inside columns of fixed width that wrap horizontally.</span></span> <span data-ttu-id="62a58-159">このオプションは通常、パノラマ セクションのタイル レイアウトに使用されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-159">This option is typically used for tile layouts in panorama sections.</span></span> <span data-ttu-id="62a58-160">これは **Tab.Style** が **パノラマ** に設定されている TabPages の規定値です。</span><span class="sxs-lookup"><span data-stu-id="62a58-160">It's the default value for TabPages where **Tab.Style** is set to **Panorama**.</span></span> |

## <a name="columnsmode-property"></a><span data-ttu-id="62a58-161">ColumnsMode プロパティ</span><span class="sxs-lookup"><span data-stu-id="62a58-161">ColumnsMode property</span></span>
<span data-ttu-id="62a58-162">**ColumnsMode** プロパティの場合、Finance and Operations アプリにはレスポンシブ レイアウトをサポートする **塗りつぶし** オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="62a58-162">For the **ColumnsMode** property, Finance and Operations apps have a **Fill** option to support responsive layouts.</span></span> <span data-ttu-id="62a58-163">プロパティをこの値に設定すると、列は必要に応じて自動的にフローされます。</span><span class="sxs-lookup"><span data-stu-id="62a58-163">When the property is set to this value, columns automatically flow as required.</span></span> <span data-ttu-id="62a58-164">次のテーブルでは、**ColumnsMode** プロパティのさまざまなオプションについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="62a58-164">The following table describes the various options for the **ColumnsMode** property.</span></span>

| <span data-ttu-id="62a58-165">オプション</span><span class="sxs-lookup"><span data-stu-id="62a58-165">Option</span></span> | <span data-ttu-id="62a58-166">説明</span><span class="sxs-lookup"><span data-stu-id="62a58-166">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a58-167">塗りつぶし</span><span class="sxs-lookup"><span data-stu-id="62a58-167">Fill</span></span>   | <span data-ttu-id="62a58-168">コンテナー タイプに応じて、使用可能な水平領域または垂直領域を満たす列が生成されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-168">Columns are generated to fill the available horizontal space or vertical space, depending on the container type.</span></span> <span data-ttu-id="62a58-169">コンテナーがパノラマ スタイル タブである場合、このオプションにより、縦軸に沿ってコンテナーを塗りつぶす列が生成されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-169">If the container is a Panorama-style tab, this option generates columns to fill it along the vertical axis.</span></span> <span data-ttu-id="62a58-170">他のすべてのコンテナー (グループ、タブ スタイルのタブ、およびタブの他のすべてのスタイル) では、このオプションは水平軸に沿ってコンテナーを塗りつぶす列を生成します。</span><span class="sxs-lookup"><span data-stu-id="62a58-170">For all other containers (Groups, Tab-style Tabs, and all other styles of Tabs), this option generates columns to fill the container along the horizontal axis.</span></span> |
| <span data-ttu-id="62a58-171">開始日固定</span><span class="sxs-lookup"><span data-stu-id="62a58-171">Fixed</span></span>  | <span data-ttu-id="62a58-172">**列** プロパティが生成する必要がある列の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="62a58-172">Specify the number of columns that the **Columns** property should generate.</span></span> <span data-ttu-id="62a58-173">コントロールは列の間で均等に分散され、順序が維持されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-173">Controls are evenly distributed among the columns, and their order is maintained.</span></span> <span data-ttu-id="62a58-174">コントロールは、列の間で均等に分配できない場合、一番左の列は追加のコントロールが最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-174">If the controls can't be distributed evenly among the columns, the leftmost columns receive extra controls first.</span></span> <span data-ttu-id="62a58-175">このオプションは、すべてのコントロールの既定値です。</span><span class="sxs-lookup"><span data-stu-id="62a58-175">This option is the default value for all controls.</span></span>                                                          |

## <a name="heightmodewidthmode-properties"></a><span data-ttu-id="62a58-176">HeightMode/WidthMode プロパティ</span><span class="sxs-lookup"><span data-stu-id="62a58-176">HeightMode/WidthMode properties</span></span>
<span data-ttu-id="62a58-177">Finance and Operations アプリでは、サイズ変更はサイズ プロパティの 2 つのペアを使用して行われます: **WidthMode** と **幅** および **HeightMode** と **高さ** です。</span><span class="sxs-lookup"><span data-stu-id="62a58-177">In Finance and Operations apps, sizing is done via two pairs of size properties: **WidthMode** and **Width**, and **HeightMode** and **Height**.</span></span> <span data-ttu-id="62a58-178">次のテーブルは、これらのプロパティのさまざまなオプションについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="62a58-178">The following table describes the various options for these properties.</span></span>

| <span data-ttu-id="62a58-179">オプション</span><span class="sxs-lookup"><span data-stu-id="62a58-179">Option</span></span>          | <span data-ttu-id="62a58-180">説明</span><span class="sxs-lookup"><span data-stu-id="62a58-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a58-181">SizeToAvailable</span><span class="sxs-lookup"><span data-stu-id="62a58-181">SizeToAvailable</span></span> | <span data-ttu-id="62a58-182">親コンテナーの内部の垂直 (または水平) 軸に沿って、使用可能な領域を入力します。</span><span class="sxs-lookup"><span data-stu-id="62a58-182">Fill the available space along the vertical (or horizontal) axis inside the parent container.</span></span> <span data-ttu-id="62a58-183">コンテナーに高さ (または幅) を提供することができる兄弟コンテナーが存在している場合を除いて、親コンテナーに **SizeToContent** 高さ (または幅) があり、子コンテナーの高さ (または幅) も **SizeToContent** である場合。</span><span class="sxs-lookup"><span data-stu-id="62a58-183">If the parent container has **SizeToContent** height (or width), the child's height (or width) is also **SizeToContent**, unless there is a sibling in the container that can provide a height (or width).</span></span> <span data-ttu-id="62a58-184">このオプションは、(すべてのスタイルの) グリッドとタブの既定値です。</span><span class="sxs-lookup"><span data-stu-id="62a58-184">This option is the default value for Grids and Tabs (of all styles).</span></span> |
| <span data-ttu-id="62a58-185">SizeToContent</span><span class="sxs-lookup"><span data-stu-id="62a58-185">SizeToContent</span></span>   | <span data-ttu-id="62a58-186">コンテナーの高さ (または幅) は、その内容の高さ (または幅) にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62a58-186">The height (or width) of the container should be the height (or width) of its contents.</span></span> <span data-ttu-id="62a58-187">このオプションは、グループとタブ以外のすべてのコントロールの既定値です。</span><span class="sxs-lookup"><span data-stu-id="62a58-187">This option is the default value for Groups and all other controls except Tabs.</span></span> <span data-ttu-id="62a58-188">常に拡張されていない FastTabs も、**SizeToContent** 高さがあります。</span><span class="sxs-lookup"><span data-stu-id="62a58-188">FastTabs that aren't always expanded also have **SizeToContent** height.</span></span> |
| <span data-ttu-id="62a58-189">マニュアル</span><span class="sxs-lookup"><span data-stu-id="62a58-189">Manual</span></span>          | <span data-ttu-id="62a58-190">高さ (または幅) は手動でサイズ設定されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-190">The height (or width) is manually sized.</span></span> <span data-ttu-id="62a58-191">**HeightMode** (または **WidthMode**) を **手動** に設定してから、**高さ** (または **幅**) を固定ピクセル数に設定します。</span><span class="sxs-lookup"><span data-stu-id="62a58-191">Set **HeightMode** (or **WidthMode**) to **Manual**, and then set **Height** (or **Width**) to a fixed number of pixels.</span></span><p><span data-ttu-id="62a58-192">**注記:** Microsoft では、手動の高さおよび幅はフォーム密度の変更には対応していないため、使用しないようにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="62a58-192">**Note:** Microsoft doesn't recommend that you use manual heights and widths, because they don't adapt to changes in form density.</span></span></p> |

<span data-ttu-id="62a58-193">これらのプロパティに **自動** の値を使用すると、動作は自動的に決定されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-193">Note that if a value of **Auto** is used for these properties, the behavior is automatically determined at runtime.</span></span> <span data-ttu-id="62a58-194">通常、これらのプロパティの **自動** の値は、AX 2012 の場合と同様に **SizeToContent** の値と同じ動作になります。</span><span class="sxs-lookup"><span data-stu-id="62a58-194">Typically, a value of **Auto** for these properties causes the same behavior as a value of **SizeToContent**, as in AX 2012.</span></span>

## <a name="interactions-between-the-arrangemethod-and-columns-properties"></a><span data-ttu-id="62a58-195">ArrangeMethod および列のプロパティの相互関係</span><span class="sxs-lookup"><span data-stu-id="62a58-195">Interactions between the ArrangeMethod and Columns properties</span></span>
<span data-ttu-id="62a58-196">**ArrangeMethod**=**HorizontalLeft** または **HorizontalRight** の場合、アイテムが厳密な水平配置でレイアウトされ、折り返しが使用されないため、**列** プロパティは無効です。</span><span class="sxs-lookup"><span data-stu-id="62a58-196">If **ArrangeMethod**=**HorizontalLeft** or **HorizontalRight**, the **Columns** property has no effect, because items are laid out in strict horizontal arrangement and no wrapping is used.</span></span> <span data-ttu-id="62a58-197">**ArrangeMethod**=**縦** の場合、列は垂直に配置され、コントロールは列 (**Fixed**) 間で均等に分散されるか、または利用可能な水平または垂直空間 (**入力**) を埋めるために分散されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-197">If **ArrangeMethod**=**Vertical**, columns are arranged vertically, and the controls are either distributed evenly among the columns (**Fixed**), or distributed to fill the available horizontal or vertical space (**Fill**).</span></span> <span data-ttu-id="62a58-198">**ArrangeMethod**=**HorizontalWrap** の場合、列が配置され、280 px の固定列幅で水平ラッピングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-198">If **ArrangeMethod**=**HorizontalWrap**, columns are arranged, and horizontal wrapping is used at a fixed column width of 280 px.</span></span> <span data-ttu-id="62a58-199">このオプションは通常、タイル レイアウトをラップするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-199">Typically, this option is used to wrap tile layouts.</span></span>

### <a name="examples"></a><span data-ttu-id="62a58-200">例</span><span class="sxs-lookup"><span data-stu-id="62a58-200">Examples</span></span>

#### <a name="arrangemethodhorizontalwrap"></a><span data-ttu-id="62a58-201">ArrangeMethod=HorizontalWrap</span><span class="sxs-lookup"><span data-stu-id="62a58-201">ArrangeMethod=HorizontalWrap</span></span>

<span data-ttu-id="62a58-202">**ArrangeMethod**=**HorizontalWrap** および **列**= **1**</span><span class="sxs-lookup"><span data-stu-id="62a58-202">**ArrangeMethod**=**HorizontalWrap** and **Columns**=**1**</span></span>

<table>
  <tr><td><span data-ttu-id="62a58-203">1 &nbsp; 2</span><span class="sxs-lookup"><span data-stu-id="62a58-203">1 &nbsp; 2</span></span></td></tr>
  <tr><td><span data-ttu-id="62a58-204">3 &nbsp; 4</span><span class="sxs-lookup"><span data-stu-id="62a58-204">3 &nbsp; 4</span></span></td></tr>
  <tr><td><span data-ttu-id="62a58-205">5 &nbsp; 6</span><span class="sxs-lookup"><span data-stu-id="62a58-205">5 &nbsp; 6</span></span></td></tr>
  <tr><td><span data-ttu-id="62a58-206">7 &nbsp; 8</span><span class="sxs-lookup"><span data-stu-id="62a58-206">7 &nbsp; 8</span></span></td></tr>
  <tr><td><span data-ttu-id="62a58-207">9</span><span class="sxs-lookup"><span data-stu-id="62a58-207">9</span></span></td></tr>
</table>

<span data-ttu-id="62a58-208">**ArrangeMethod**=**HorizontalWrap** および **列**= **2**</span><span class="sxs-lookup"><span data-stu-id="62a58-208">**ArrangeMethod**=**HorizontalWrap** and **Columns**=**2**</span></span>

<table>
  <tr>
    <td><span data-ttu-id="62a58-209">1 &nbsp; 2</span><span class="sxs-lookup"><span data-stu-id="62a58-209">1 &nbsp; 2</span></span></td>
    <td><span data-ttu-id="62a58-210">6 &nbsp; 7</span><span class="sxs-lookup"><span data-stu-id="62a58-210">6 &nbsp; 7</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-211">3 &nbsp; 4</span><span class="sxs-lookup"><span data-stu-id="62a58-211">3 &nbsp; 4</span></span></td>
    <td><span data-ttu-id="62a58-212">8 &nbsp; 9</span><span class="sxs-lookup"><span data-stu-id="62a58-212">8 &nbsp; 9</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-213">5</span><span class="sxs-lookup"><span data-stu-id="62a58-213">5</span></span></td>
    <td></td>
  </tr>
</table>

<span data-ttu-id="62a58-214">**ArrangeMethod**=**HorizontalWrap** および **列**=**塗りつぶし**</span><span class="sxs-lookup"><span data-stu-id="62a58-214">**ArrangeMethod**=**HorizontalWrap** and **Columns**=**Fill**</span></span>

<span data-ttu-id="62a58-215">この例では、コンテナーの高さに合わせることができるのは 3 行の品目だけであると仮定します。</span><span class="sxs-lookup"><span data-stu-id="62a58-215">For this example, we assume that only three lines of items can fit in the container height.</span></span>

<table>
  <tr>
    <td><span data-ttu-id="62a58-216">1 &nbsp; 2</span><span class="sxs-lookup"><span data-stu-id="62a58-216">1 &nbsp; 2</span></span></td>
    <td><span data-ttu-id="62a58-217">7 &nbsp; &nbsp; 8</span><span class="sxs-lookup"><span data-stu-id="62a58-217">7 &nbsp; &nbsp; 8</span></span></td>
    <td><span data-ttu-id="62a58-218">13 &nbsp; 14</span><span class="sxs-lookup"><span data-stu-id="62a58-218">13 &nbsp; 14</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-219">3 &nbsp; 4</span><span class="sxs-lookup"><span data-stu-id="62a58-219">3 &nbsp; 4</span></span></td>
    <td><span data-ttu-id="62a58-220">9 &nbsp; &nbsp; 10</span><span class="sxs-lookup"><span data-stu-id="62a58-220">9 &nbsp; &nbsp; 10</span></span></td>
    <td><span data-ttu-id="62a58-221">15</span><span class="sxs-lookup"><span data-stu-id="62a58-221">15</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-222">5 &nbsp; 6</span><span class="sxs-lookup"><span data-stu-id="62a58-222">5 &nbsp; 6</span></span></td>
    <td><span data-ttu-id="62a58-223">11 &nbsp; 12</span><span class="sxs-lookup"><span data-stu-id="62a58-223">11 &nbsp; 12</span></span></td>
    <td></td>
  </tr>
</table>

#### <a name="arrangemethodvertical"></a><span data-ttu-id="62a58-224">ArrangeMethod=Vertical</span><span class="sxs-lookup"><span data-stu-id="62a58-224">ArrangeMethod=Vertical</span></span>

<span data-ttu-id="62a58-225">**ArrangeMethod**= **垂直** および **列**= **1**</span><span class="sxs-lookup"><span data-stu-id="62a58-225">**ArrangeMethod**=**Vertical** and **Columns**=**1**</span></span>

<table>
  <tr><td><span data-ttu-id="62a58-226">1</span><span class="sxs-lookup"><span data-stu-id="62a58-226">1</span></span> </td></tr>
  <tr><td><span data-ttu-id="62a58-227">2</span><span class="sxs-lookup"><span data-stu-id="62a58-227">2</span></span></td></tr>
  <tr><td><span data-ttu-id="62a58-228">3</span><span class="sxs-lookup"><span data-stu-id="62a58-228">3</span></span></td></tr>
  <tr><td><span data-ttu-id="62a58-229">...</span><span class="sxs-lookup"><span data-stu-id="62a58-229">...</span></span></td></tr>
</table>

<span data-ttu-id="62a58-230">**ArrangeMethod**= **垂直** および **列**= **2**</span><span class="sxs-lookup"><span data-stu-id="62a58-230">**ArrangeMethod**=**Vertical** and **Columns**=**2**</span></span>

<table>
  <tr>
    <td><span data-ttu-id="62a58-231">1</span><span class="sxs-lookup"><span data-stu-id="62a58-231">1</span></span></td><td><span data-ttu-id="62a58-232">5</span><span class="sxs-lookup"><span data-stu-id="62a58-232">5</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-233">2</span><span class="sxs-lookup"><span data-stu-id="62a58-233">2</span></span></td><td><span data-ttu-id="62a58-234">6</span><span class="sxs-lookup"><span data-stu-id="62a58-234">6</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-235">3</span><span class="sxs-lookup"><span data-stu-id="62a58-235">3</span></span></td><td><span data-ttu-id="62a58-236">7</span><span class="sxs-lookup"><span data-stu-id="62a58-236">7</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-237">4</span><span class="sxs-lookup"><span data-stu-id="62a58-237">4</span></span></td><td><span data-ttu-id="62a58-238">8</span><span class="sxs-lookup"><span data-stu-id="62a58-238">8</span></span></td>
  </tr>
</table>

<span data-ttu-id="62a58-239">**ArrangeMethod**= **垂直** および **列**=**塗りつぶし**</span><span class="sxs-lookup"><span data-stu-id="62a58-239">**ArrangeMethod**=**Vertical** and **Columns**=**Fill**</span></span>

<span data-ttu-id="62a58-240">この例では、コンテナーの高さに合わせることができるのは 3 行の品目だけであると仮定します。</span><span class="sxs-lookup"><span data-stu-id="62a58-240">For this example, we assume that only three lines of items can fit in the container height.</span></span>

<table>
  <tr>
    <td><span data-ttu-id="62a58-241">1</span><span class="sxs-lookup"><span data-stu-id="62a58-241">1</span></span></td><td><span data-ttu-id="62a58-242">4</span><span class="sxs-lookup"><span data-stu-id="62a58-242">4</span></span></td><td><span data-ttu-id="62a58-243">7</span><span class="sxs-lookup"><span data-stu-id="62a58-243">7</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-244">2</span><span class="sxs-lookup"><span data-stu-id="62a58-244">2</span></span></td><td><span data-ttu-id="62a58-245">5</span><span class="sxs-lookup"><span data-stu-id="62a58-245">5</span></span></td><td><span data-ttu-id="62a58-246">8</span><span class="sxs-lookup"><span data-stu-id="62a58-246">8</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-247">3</span><span class="sxs-lookup"><span data-stu-id="62a58-247">3</span></span></td><td><span data-ttu-id="62a58-248">6</span><span class="sxs-lookup"><span data-stu-id="62a58-248">6</span></span></td>
  </tr>
</table>

<span data-ttu-id="62a58-249">クイック タブ上で **ArrangeMethod**= **垂直** および **列**=**塗りつぶし**</span><span class="sxs-lookup"><span data-stu-id="62a58-249">**ArrangeMethod**=**Vertical** and **Columns**=**Fill** on a FastTab</span></span>

<span data-ttu-id="62a58-250">この例では、クイック タブの幅が 4 列に収まると仮定します。</span><span class="sxs-lookup"><span data-stu-id="62a58-250">For this example, we assume that the width of the FastTab can fit four columns.</span></span>

<table>
  <tr>
    <td><span data-ttu-id="62a58-251">1</span><span class="sxs-lookup"><span data-stu-id="62a58-251">1</span></span></td><td><span data-ttu-id="62a58-252">3</span><span class="sxs-lookup"><span data-stu-id="62a58-252">3</span></span></td><td><span data-ttu-id="62a58-253">5</span><span class="sxs-lookup"><span data-stu-id="62a58-253">5</span></span></td><td><span data-ttu-id="62a58-254">7</span><span class="sxs-lookup"><span data-stu-id="62a58-254">7</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="62a58-255">2</span><span class="sxs-lookup"><span data-stu-id="62a58-255">2</span></span></td><td><span data-ttu-id="62a58-256">4</span><span class="sxs-lookup"><span data-stu-id="62a58-256">4</span></span></td><td><span data-ttu-id="62a58-257">6</span><span class="sxs-lookup"><span data-stu-id="62a58-257">6</span></span></td><td><span data-ttu-id="62a58-258">8</span><span class="sxs-lookup"><span data-stu-id="62a58-258">8</span></span></td>
  </tr>
</table>

## <a name="breakable-groups"></a><span data-ttu-id="62a58-259">Breakable グループ</span><span class="sxs-lookup"><span data-stu-id="62a58-259">Breakable groups</span></span>
<span data-ttu-id="62a58-260">**ColumnsMode** を **塗りつぶし** に設定して列を動的に作成するとき、利用可能な領域の量に基づいて、フィールドのグループを複数の列に分割できます。</span><span class="sxs-lookup"><span data-stu-id="62a58-260">When you set **ColumnsMode** to **Fill** to dynamically create columns, based on the amount of available space, groups of fields can be split into multiple columns.</span></span> <span data-ttu-id="62a58-261">開発者はグループ コントロールの **Breakable** プロパティで、グループ内のコントロールが列間で配布されないことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="62a58-261">The **Breakable** property on Group controls lets developers ensure that controls in a group aren't distributed across columns.</span></span> <span data-ttu-id="62a58-262">このプロパティの既定値は、**はい** で、グループの内容がグループ間で分割できることを示します。</span><span class="sxs-lookup"><span data-stu-id="62a58-262">The default value for this property is **Yes**, which indicates that the contents of the group can be split between groups.</span></span> <span data-ttu-id="62a58-263">常にグループ化しておくには、**Breakable** を **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="62a58-263">To keep a group together all the time, set **Breakable** to **No**.</span></span> <span data-ttu-id="62a58-264">**Breakable** は入れ子のグループの最初のレベルにのみ適用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="62a58-264">Note that **Breakable** applies only to the first level in nested groups.</span></span>

## <a name="guidelines-for-using-layout-properties"></a><span data-ttu-id="62a58-265">レイアウト プロパティを使用するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="62a58-265">Guidelines for using layout properties</span></span>
### <a name="columnsmodefill"></a><span data-ttu-id="62a58-266">ColumnsMode=Fill</span><span class="sxs-lookup"><span data-stu-id="62a58-266">ColumnsMode=Fill</span></span>

-   <span data-ttu-id="62a58-267">**ColumnsMode** を **入力** に設定したコンテナーを入れ子にしないでください。</span><span class="sxs-lookup"><span data-stu-id="62a58-267">Don't nest containers that have **ColumnsMode** set to **Fill**.</span></span> <span data-ttu-id="62a58-268">空き領域を応答として埋めるコントロールやフィールドの直接の親コンテナーでのみ **ColumnsMode** を **Fill** に設定します。</span><span class="sxs-lookup"><span data-stu-id="62a58-268">Set **ColumnsMode** to **Fill** only on the direct parent container of the controls/fields that you want to responsively fill the available space.</span></span>
-   <span data-ttu-id="62a58-269">**ColumnsMode** を **入力** に設定したコンテナーのどの子コントロールでも、**HeightMode** を **SizeToAvailable** に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="62a58-269">Don't set **HeightMode** to **SizeToAvailable** on any child controls of a container that has **ColumnsMode** set to **Fill**.</span></span> <span data-ttu-id="62a58-270">**ColumnsMode**=**Fill** は、列間のすべてのコントロールの平均の高さを計算して、可能な限り均等に調整しようとします。</span><span class="sxs-lookup"><span data-stu-id="62a58-270">**ColumnsMode**=**Fill** tries to calculate an average height of all controls across columns to balance them as much as possible.</span></span> <span data-ttu-id="62a58-271">しかし、レイアウト CSS および計算は **SizeToAvailable** の子を処理できず、およびこの設定は必ずしも意味がありません。</span><span class="sxs-lookup"><span data-stu-id="62a58-271">However, our layout CSS and calculations can't handle **SizeToAvailable** children, and this setting doesn't necessarily make sense.</span></span>
-   <span data-ttu-id="62a58-272">**ColumnsMode** を **入力** に設定したコンテナーのどの子コントロールでも、**WidhMode** を **SizeToAvailable** に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="62a58-272">Don't set **WidthMode** to **SizeToAvailable** on any child controls of a container that has **ColumnsMode** set to **Fill**.</span></span> <span data-ttu-id="62a58-273">それ以外の場合、子コントロールは利用可能なすべての幅を占め、すべてのコントロールが 1 つの列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="62a58-273">Otherwise, the child controls will take up all the available width, and all controls will appear in one column.</span></span>
-   <span data-ttu-id="62a58-274">**ColumnsMode**=**入力** のコンテナーは、**WidthMode** を **SizeToAvailable** (タブやグループなどの入力幅コンテナーを使用している場合) または **HeightMode** を **SizeToAvailable** (パノラマ セクションなどの入力高さコンテナーを使用している場合) に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62a58-274">Container that have **ColumnsMode**=**Fill** should have **WidthMode** set to **SizeToAvailable** (if you're using fill-width containers such as Tabs and Groups) or **HeightMode** set to **SizeToAvailable** (if you're using fill-height containers such as Panorama sections).</span></span>

### <a name="heightmodewidthmodesizetoavailable"></a><span data-ttu-id="62a58-275">HeightMode/WidthMode=SizeToAvailable</span><span class="sxs-lookup"><span data-stu-id="62a58-275">HeightMode/WidthMode=SizeToAvailable</span></span>

-    <span data-ttu-id="62a58-276">**WidthMode**=**SizeToAvailable** を使用する場合は、フォーム内の親コンテナーに、**WidthMode** を **SizeToContent** にではなく、**SizeToAvailable** に設定するよう確認します。</span><span class="sxs-lookup"><span data-stu-id="62a58-276">If you use **WidthMode**=**SizeToAvailable**, make sure that parent containers in the form have **WidthMode** set to **SizeToAvailable**, not **SizeToContent**.</span></span> <span data-ttu-id="62a58-277">**SizeToContent** 内部のコンテナー **SizeToAvailable** コンテナー を上書きして **SizeToContent** コンテナーになります。</span><span class="sxs-lookup"><span data-stu-id="62a58-277">**SizeToAvailable** containers inside **SizeToContent** containers are overridden and become **SizeToContent** containers.</span></span>


<a name="additional-resources"></a><span data-ttu-id="62a58-278">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="62a58-278">Additional resources</span></span>
--------

[<span data-ttu-id="62a58-279">ユーザー インターフェイス開発ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="62a58-279">User interface development home page</span></span>](user-interface-development-home-page.md)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]