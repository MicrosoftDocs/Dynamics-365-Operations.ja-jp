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
ms.openlocfilehash: ca8e66fba5043c860498aa1367dd760f98fa9bf4
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188398"
---
# <a name="page-layout-in-the-web-client"></a><span data-ttu-id="823cf-104">Web クライアントのページ レイアウト</span><span class="sxs-lookup"><span data-stu-id="823cf-104">Page layout in the web client</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="823cf-105">このトピックでは、Web クライアントのレイアウトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="823cf-105">This topic discusses layout in the web client.</span></span> <span data-ttu-id="823cf-106">レイアウトは、ページ上にコントロールを表示する方法を指定するデザイン プロセスです。</span><span class="sxs-lookup"><span data-stu-id="823cf-106">Layout is a design process that specifies how controls appear on a page.</span></span> 

## <a name="introduction"></a><span data-ttu-id="823cf-107">はじめに</span><span class="sxs-lookup"><span data-stu-id="823cf-107">Introduction</span></span>

<span data-ttu-id="823cf-108">レイアウトは、ページ上のコントロールを Web クライアントで表示する方法を指定するデザイン プロセスです。</span><span class="sxs-lookup"><span data-stu-id="823cf-108">Layout is a design process that specifies how the controls on a page appear in the web client.</span></span> <span data-ttu-id="823cf-109">レイアウトはコンテナー コントロール内で発生します。</span><span class="sxs-lookup"><span data-stu-id="823cf-109">Layout occurs within container controls.</span></span> <span data-ttu-id="823cf-110">次のテーブルに、コンテナー コントロールの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="823cf-110">The following table lists the container controls.</span></span>

| <span data-ttu-id="823cf-111">コンテナー</span><span class="sxs-lookup"><span data-stu-id="823cf-111">Container</span></span>   | <span data-ttu-id="823cf-112">説明</span><span class="sxs-lookup"><span data-stu-id="823cf-112">Description</span></span>                                                                                                                                            |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823cf-113">Form.Design</span><span class="sxs-lookup"><span data-stu-id="823cf-113">Form.Design</span></span> | <span data-ttu-id="823cf-114">ページのルート。</span><span class="sxs-lookup"><span data-stu-id="823cf-114">The root of the page.</span></span> <span data-ttu-id="823cf-115">これは、特殊なコンテナーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="823cf-115">It functions as a special kind of container.</span></span>                                                                                     |
| <span data-ttu-id="823cf-116">グループ化</span><span class="sxs-lookup"><span data-stu-id="823cf-116">Group</span></span>       | <span data-ttu-id="823cf-117">汎用コンテナー コントロール。</span><span class="sxs-lookup"><span data-stu-id="823cf-117">The general-purpose container control.</span></span> <span data-ttu-id="823cf-118">グループ コントロールは必要に応じて入れ子にできます。</span><span class="sxs-lookup"><span data-stu-id="823cf-118">Group controls can be nested as required.</span></span>                                                                       |
| <span data-ttu-id="823cf-119">タブ</span><span class="sxs-lookup"><span data-stu-id="823cf-119">Tab</span></span>         | <span data-ttu-id="823cf-120">TabPage コントロールを含み、**タブ**、**クイックタブ**、**垂直タブ**、および **パノラマ** など多くの **Tab.Style** 値を持つコントロールです。</span><span class="sxs-lookup"><span data-stu-id="823cf-120">A control that contains TabPage controls and has many possible **Tab.Style** values, such as **Tab**, **FastTab**, **Vertical Tab**, and **Panorama**.</span></span> |
| <span data-ttu-id="823cf-121">TabPage</span><span class="sxs-lookup"><span data-stu-id="823cf-121">TabPage</span></span>     | <span data-ttu-id="823cf-122">各 TabPage コントロールの表示形式は、その **Tab.Style** 値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="823cf-122">The appearance of each TabPage control depends on its **Tab.Style** value.</span></span>                                                                             |
| <span data-ttu-id="823cf-123">ボタン グループ</span><span class="sxs-lookup"><span data-stu-id="823cf-123">ButtonGroup</span></span> | <span data-ttu-id="823cf-124">ボタンを含むグループ コントロールの特殊なタイプ。</span><span class="sxs-lookup"><span data-stu-id="823cf-124">A special type of Group control that contains buttons.</span></span>                                                                                                 |

<span data-ttu-id="823cf-125">グリッドとは、柔軟なサイズ変更 (**SizeToAvailable**) などいくつかのコンテナ動作を持つ特殊なタイプのコントロールです。</span><span class="sxs-lookup"><span data-stu-id="823cf-125">A grid is a special type of control that has some container behaviors, such as flexible sizing (**SizeToAvailable**).</span></span> <span data-ttu-id="823cf-126">ただし、グリッドには特別な視覚化があり、汎用のコンテナー コントロールではありません。</span><span class="sxs-lookup"><span data-stu-id="823cf-126">However, a grid has special visualizations and isn't a general-purpose container control.</span></span>

## <a name="layout-dynamics-ax-2012-vs-finance-and-operations-apps"></a><span data-ttu-id="823cf-127">レイアウト: Dynamics AX 2012 vs. Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="823cf-127">Layout: Dynamics AX 2012 vs. Finance and Operations apps</span></span>
### <a name="layout-in-dynamics-ax-2012"></a><span data-ttu-id="823cf-128">Dynamics AX 2012 でのレイアウト</span><span class="sxs-lookup"><span data-stu-id="823cf-128">Layout in Dynamics AX 2012</span></span>

<span data-ttu-id="823cf-129">Microsoft Dynamics AX 2012 では、コンテナーのコントロールの配置はほとんど必ず縦で、列を手動で設定して水平に拡大します。</span><span class="sxs-lookup"><span data-stu-id="823cf-129">In Microsoft Dynamics AX 2012, the arrangement of controls in containers is almost always vertical, and columns are manually set to provide some horizontal spread.</span></span>

### <a name="examples"></a><span data-ttu-id="823cf-130">例</span><span class="sxs-lookup"><span data-stu-id="823cf-130">Examples</span></span>

<span data-ttu-id="823cf-131">**列** = **1** 1 2 3 **列** = **2** 1 4 2 5 3 Dynamics AX 2012 では、**高さ** プロパティと **幅h** プロパティを使用してサイジングできます。</span><span class="sxs-lookup"><span data-stu-id="823cf-131">**Columns**=**1** 1 2 3 **Columns**=**2** 1 4 2 5 3 In Dynamics AX 2012, sizing is achieved via the **Height** and **Width** properties.</span></span> <span data-ttu-id="823cf-132">**高さ** および **幅** が **自動** と設定されている場合、サイズは子コントロールが必要とする大きさになります。</span><span class="sxs-lookup"><span data-stu-id="823cf-132">If **Height** and **Width** are set to **Auto**, the size is as large as the child controls require.</span></span> <span data-ttu-id="823cf-133">**高さ** および **幅** が **列** に設定されている場合、コンテナーは親コンテナー内に収まる大きさになります。</span><span class="sxs-lookup"><span data-stu-id="823cf-133">If **Height** and **Width** are set to **Column**, the container is as large as it can be within the parent container.</span></span> <span data-ttu-id="823cf-134">既定では、**高さ** と **幅** はすべてのコンテナーに対して **自動** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="823cf-134">By default, **Height** and **Width** are set to **Auto** for every container.</span></span>

### <a name="layout-in-finance-and-operations"></a><span data-ttu-id="823cf-135">Finance and Operations のレイアウト</span><span class="sxs-lookup"><span data-stu-id="823cf-135">Layout in Finance and Operations</span></span> 

<span data-ttu-id="823cf-136">Finance and Operations では、レイアウトが Dynamics AX 2012 でのレイアウトを制御する同じ基本的なプロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-136">In Finance and Operations, layout is controlled by the same basic properties that control layout in Dynamics AX 2012.</span></span> <span data-ttu-id="823cf-137">ただし、応答性の良いレイアウトをサポートするため、追加のオプションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="823cf-137">However, additional options have been added to support a more responsive layout.</span></span> <span data-ttu-id="823cf-138">特に、ページのレイアウトは次の要因に基づいています。</span><span class="sxs-lookup"><span data-stu-id="823cf-138">In particular, the layout of a page is based on the following factors:</span></span>

-   <span data-ttu-id="823cf-139">**ArrangeMethod** プロパティによって指定される配置メソッド。</span><span class="sxs-lookup"><span data-stu-id="823cf-139">The arrangement method that is specified by the **ArrangeMethod** property.</span></span>
-   <span data-ttu-id="823cf-140">**列** プロパティで指定された列。</span><span class="sxs-lookup"><span data-stu-id="823cf-140">The columns that are specified by the **Columns** property.</span></span>
-   <span data-ttu-id="823cf-141">**HeightMode**、**WidthMode**、**Height**、**Width** の各プロパティにより指定されているサイズ変更。</span><span class="sxs-lookup"><span data-stu-id="823cf-141">The sizing that is specified by the **HeightMode**, **WidthMode**, **Height**, and **Width** properties.</span></span>

## <a name="arrangemethod-property"></a><span data-ttu-id="823cf-142">ArrangeMethod プロパティ</span><span class="sxs-lookup"><span data-stu-id="823cf-142">ArrangeMethod property</span></span>
<span data-ttu-id="823cf-143">**ArrangeMethod** プロパティは、コンテナーの基準配置方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="823cf-143">The **ArrangeMethod** property specifies a base arrangement method for a container.</span></span> <span data-ttu-id="823cf-144">このプロパティでは、AX 2012 からすべてのオプションが Finance and Operations アプリに設定されています。</span><span class="sxs-lookup"><span data-stu-id="823cf-144">For this property, Finance and Operations apps have all the options from AX 2012.</span></span> <span data-ttu-id="823cf-145">パノラマのタイル レイアウトを対象にした **HorizontalWrap** も含まれています。</span><span class="sxs-lookup"><span data-stu-id="823cf-145">However, they also have a **HorizontalWrap** option that is intended for tile layouts in panoramas.</span></span> <span data-ttu-id="823cf-146">次のテーブルでは、**ArrangeMethod** プロパティのさまざまなオプションについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="823cf-146">The following table describes the various options for the **ArrangeMethod** property.</span></span>

| <span data-ttu-id="823cf-147">オプション</span><span class="sxs-lookup"><span data-stu-id="823cf-147">Option</span></span>          | <span data-ttu-id="823cf-148">説明</span><span class="sxs-lookup"><span data-stu-id="823cf-148">Description</span></span>                                                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823cf-149">垂直</span><span class="sxs-lookup"><span data-stu-id="823cf-149">Vertical</span></span>        | <span data-ttu-id="823cf-150">コントロールは垂直に配置されています。</span><span class="sxs-lookup"><span data-stu-id="823cf-150">Controls are arranged vertically.</span></span> <span data-ttu-id="823cf-151">列も使用されている場合は、コントロールは生成された列の内部で垂直方向に配置されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-151">If columns are also used, controls are arranged vertically inside the generated columns.</span></span> <span data-ttu-id="823cf-152">このオプションは、グループおよび **Tab.Style** が **パノラマ** 以外の値に設定されている TabPages の既定値です。</span><span class="sxs-lookup"><span data-stu-id="823cf-152">This option is the default value for Groups and for TabPages where **Tab.Style** is set to a value other than **Panorama**.</span></span> |
| <span data-ttu-id="823cf-153">HorizontalLeft</span><span class="sxs-lookup"><span data-stu-id="823cf-153">HorizontalLeft</span></span>  | <span data-ttu-id="823cf-154">コントロールは水平方向に配置され、親コンテナーの内部で左揃えおよび下揃えになります。</span><span class="sxs-lookup"><span data-stu-id="823cf-154">Controls are arranged horizontally, and they are left-aligned and bottom-aligned inside the parent container.</span></span> |
| <span data-ttu-id="823cf-155">HorizontalRight</span><span class="sxs-lookup"><span data-stu-id="823cf-155">HorizontalRight</span></span> | <span data-ttu-id="823cf-156">コントロールは水平方向に配置され、親コンテナーの内部で右揃えおよび下揃えになります。</span><span class="sxs-lookup"><span data-stu-id="823cf-156">Controls are arranged horizontally, and they are right-aligned and bottom-aligned inside the parent container.</span></span> |
| <span data-ttu-id="823cf-157">HorizontalWrap</span><span class="sxs-lookup"><span data-stu-id="823cf-157">HorizontalWrap</span></span>  | <span data-ttu-id="823cf-158">コントロールは水平方向に折り返された固定幅の列の内側に配置されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-158">Controls are arranged inside columns of fixed width that wrap horizontally.</span></span> <span data-ttu-id="823cf-159">このオプションは通常、パノラマ セクションのタイル レイアウトに使用されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-159">This option is typically used for tile layouts in panorama sections.</span></span> <span data-ttu-id="823cf-160">これは **Tab.Style** が **パノラマ** に設定されている TabPages の規定値です。</span><span class="sxs-lookup"><span data-stu-id="823cf-160">It's the default value for TabPages where **Tab.Style** is set to **Panorama**.</span></span> |

## <a name="columnsmode-property"></a><span data-ttu-id="823cf-161">ColumnsMode プロパティ</span><span class="sxs-lookup"><span data-stu-id="823cf-161">ColumnsMode property</span></span>
<span data-ttu-id="823cf-162">**ColumnsMode** プロパティの場合、Finance and Operations アプリにはレスポンシブ レイアウトをサポートする **塗りつぶし** オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="823cf-162">For the **ColumnsMode** property, Finance and Operations apps have a **Fill** option to support responsive layouts.</span></span> <span data-ttu-id="823cf-163">プロパティをこの値に設定すると、列は必要に応じて自動的にフローされます。</span><span class="sxs-lookup"><span data-stu-id="823cf-163">When the property is set to this value, columns automatically flow as required.</span></span> <span data-ttu-id="823cf-164">次のテーブルでは、**ColumnsMode** プロパティのさまざまなオプションについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="823cf-164">The following table describes the various options for the **ColumnsMode** property.</span></span>

| <span data-ttu-id="823cf-165">オプション</span><span class="sxs-lookup"><span data-stu-id="823cf-165">Option</span></span> | <span data-ttu-id="823cf-166">説明</span><span class="sxs-lookup"><span data-stu-id="823cf-166">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823cf-167">塗りつぶし</span><span class="sxs-lookup"><span data-stu-id="823cf-167">Fill</span></span>   | <span data-ttu-id="823cf-168">コンテナー タイプに応じて、使用可能な水平領域または垂直領域を満たす列が生成されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-168">Columns are generated to fill the available horizontal space or vertical space, depending on the container type.</span></span> <span data-ttu-id="823cf-169">コンテナーがパノラマ スタイル タブである場合、このオプションにより、縦軸に沿ってコンテナーを塗りつぶす列が生成されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-169">If the container is a Panorama-style tab, this option generates columns to fill it along the vertical axis.</span></span> <span data-ttu-id="823cf-170">他のすべてのコンテナー (グループ、タブ スタイルのタブ、およびタブの他のすべてのスタイル) では、このオプションは水平軸に沿ってコンテナーを塗りつぶす列を生成します。</span><span class="sxs-lookup"><span data-stu-id="823cf-170">For all other containers (Groups, Tab-style Tabs, and all other styles of Tabs), this option generates columns to fill the container along the horizontal axis.</span></span> |
| <span data-ttu-id="823cf-171">開始日固定</span><span class="sxs-lookup"><span data-stu-id="823cf-171">Fixed</span></span>  | <span data-ttu-id="823cf-172">**列** プロパティが生成する必要がある列の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="823cf-172">Specify the number of columns that the **Columns** property should generate.</span></span> <span data-ttu-id="823cf-173">コントロールは列の間で均等に分散され、順序が維持されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-173">Controls are evenly distributed among the columns, and their order is maintained.</span></span> <span data-ttu-id="823cf-174">コントロールは、列の間で均等に分配できない場合、一番左の列は追加のコントロールが最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-174">If the controls can't be distributed evenly among the columns, the leftmost columns receive extra controls first.</span></span> <span data-ttu-id="823cf-175">このオプションは、すべてのコントロールの既定値です。</span><span class="sxs-lookup"><span data-stu-id="823cf-175">This option is the default value for all controls.</span></span>                                                          |

## <a name="heightmodewidthmode-properties"></a><span data-ttu-id="823cf-176">HeightMode/WidthMode プロパティ</span><span class="sxs-lookup"><span data-stu-id="823cf-176">HeightMode/WidthMode properties</span></span>
<span data-ttu-id="823cf-177">Finance and Operations アプリでは、サイズ変更はサイズ プロパティの 2 つのペアを使用して行われます: **WidthMode** と **幅** および **HeightMode** と **高さ** です。</span><span class="sxs-lookup"><span data-stu-id="823cf-177">In Finance and Operations apps, sizing is done via two pairs of size properties: **WidthMode** and **Width**, and **HeightMode** and **Height**.</span></span> <span data-ttu-id="823cf-178">次のテーブルは、これらのプロパティのさまざまなオプションについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="823cf-178">The following table describes the various options for these properties.</span></span>

| <span data-ttu-id="823cf-179">オプション</span><span class="sxs-lookup"><span data-stu-id="823cf-179">Option</span></span>          | <span data-ttu-id="823cf-180">説明</span><span class="sxs-lookup"><span data-stu-id="823cf-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823cf-181">SizeToAvailable</span><span class="sxs-lookup"><span data-stu-id="823cf-181">SizeToAvailable</span></span> | <span data-ttu-id="823cf-182">親コンテナーの内部の垂直 (または水平) 軸に沿って、使用可能な領域を入力します。</span><span class="sxs-lookup"><span data-stu-id="823cf-182">Fill the available space along the vertical (or horizontal) axis inside the parent container.</span></span> <span data-ttu-id="823cf-183">コンテナーに高さ (または幅) を提供することができる兄弟コンテナーが存在している場合を除いて、親コンテナーに **SizeToContent** 高さ (または幅) があり、子コンテナーの高さ (または幅) も **SizeToContent** である場合。</span><span class="sxs-lookup"><span data-stu-id="823cf-183">If the parent container has **SizeToContent** height (or width), the child's height (or width) is also **SizeToContent**, unless there is a sibling in the container that can provide a height (or width).</span></span> <span data-ttu-id="823cf-184">このオプションは、(すべてのスタイルの) グリッドとタブの既定値です。</span><span class="sxs-lookup"><span data-stu-id="823cf-184">This option is the default value for Grids and Tabs (of all styles).</span></span> |
| <span data-ttu-id="823cf-185">SizeToContent</span><span class="sxs-lookup"><span data-stu-id="823cf-185">SizeToContent</span></span>   | <span data-ttu-id="823cf-186">コンテナーの高さ (または幅) は、その内容の高さ (または幅) にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="823cf-186">The height (or width) of the container should be the height (or width) of its contents.</span></span> <span data-ttu-id="823cf-187">このオプションは、グループとタブ以外のすべてのコントロールの既定値です。</span><span class="sxs-lookup"><span data-stu-id="823cf-187">This option is the default value for Groups and all other controls except Tabs.</span></span> <span data-ttu-id="823cf-188">常に拡張されていない FastTabs も、**SizeToContent** 高さがあります。</span><span class="sxs-lookup"><span data-stu-id="823cf-188">FastTabs that aren't always expanded also have **SizeToContent** height.</span></span> |
| <span data-ttu-id="823cf-189">マニュアル</span><span class="sxs-lookup"><span data-stu-id="823cf-189">Manual</span></span>          | <span data-ttu-id="823cf-190">高さ (または幅) は手動でサイズ設定されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-190">The height (or width) is manually sized.</span></span> <span data-ttu-id="823cf-191">**HeightMode** (または **WidthMode**) を **手動** に設定してから、**高さ** (または **幅**) を固定ピクセル数に設定します。</span><span class="sxs-lookup"><span data-stu-id="823cf-191">Set **HeightMode** (or **WidthMode**) to **Manual**, and then set **Height** (or **Width**) to a fixed number of pixels.</span></span><p><span data-ttu-id="823cf-192">**注記:** Microsoft では、手動の高さおよび幅はフォーム密度の変更には対応していないため、使用しないようにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="823cf-192">**Note:** Microsoft doesn't recommend that you use manual heights and widths, because they don't adapt to changes in form density.</span></span></p> |

<span data-ttu-id="823cf-193">これらのプロパティに **自動** の値を使用すると、動作は自動的に決定されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-193">Note that if a value of **Auto** is used for these properties, the behavior is automatically determined at runtime.</span></span> <span data-ttu-id="823cf-194">通常、これらのプロパティの **自動** の値は、AX 2012 の場合と同様に **SizeToContent** の値と同じ動作になります。</span><span class="sxs-lookup"><span data-stu-id="823cf-194">Typically, a value of **Auto** for these properties causes the same behavior as a value of **SizeToContent**, as in AX 2012.</span></span>

## <a name="interactions-between-the-arrangemethod-and-columns-properties"></a><span data-ttu-id="823cf-195">ArrangeMethod および列のプロパティの相互関係</span><span class="sxs-lookup"><span data-stu-id="823cf-195">Interactions between the ArrangeMethod and Columns properties</span></span>
<span data-ttu-id="823cf-196">**ArrangeMethod**=**HorizontalLeft** または **HorizontalRight** の場合、アイテムが厳密な水平配置でレイアウトされ、折り返しが使用されないため、**列** プロパティは無効です。</span><span class="sxs-lookup"><span data-stu-id="823cf-196">If **ArrangeMethod**=**HorizontalLeft** or **HorizontalRight**, the **Columns** property has no effect, because items are laid out in strict horizontal arrangement and no wrapping is used.</span></span> <span data-ttu-id="823cf-197">**ArrangeMethod**=**縦** の場合、列は垂直に配置され、コントロールは列 (**Fixed**) 間で均等に分散されるか、または利用可能な水平または垂直空間 (**入力**) を埋めるために分散されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-197">If **ArrangeMethod**=**Vertical**, columns are arranged vertically, and the controls are either distributed evenly among the columns (**Fixed**), or distributed to fill the available horizontal or vertical space (**Fill**).</span></span> <span data-ttu-id="823cf-198">**ArrangeMethod**=**HorizontalWrap** の場合、列が配置され、280 px の固定列幅で水平ラッピングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-198">If **ArrangeMethod**=**HorizontalWrap**, columns are arranged, and horizontal wrapping is used at a fixed column width of 280 px.</span></span> <span data-ttu-id="823cf-199">このオプションは通常、タイル レイアウトをラップするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-199">Typically, this option is used to wrap tile layouts.</span></span>

### <a name="examples"></a><span data-ttu-id="823cf-200">例</span><span class="sxs-lookup"><span data-stu-id="823cf-200">Examples</span></span>

#### <a name="arrangemethodhorizontalwrap"></a><span data-ttu-id="823cf-201">ArrangeMethod=HorizontalWrap</span><span class="sxs-lookup"><span data-stu-id="823cf-201">ArrangeMethod=HorizontalWrap</span></span>

<span data-ttu-id="823cf-202">**ArrangeMethod**=**HorizontalWrap** および **列**= **1**</span><span class="sxs-lookup"><span data-stu-id="823cf-202">**ArrangeMethod**=**HorizontalWrap** and **Columns**=**1**</span></span>

<table>
  <tr><td><span data-ttu-id="823cf-203">1 &nbsp; 2</span><span class="sxs-lookup"><span data-stu-id="823cf-203">1 &nbsp; 2</span></span></td></tr>
  <tr><td><span data-ttu-id="823cf-204">3 &nbsp; 4</span><span class="sxs-lookup"><span data-stu-id="823cf-204">3 &nbsp; 4</span></span></td></tr>
  <tr><td><span data-ttu-id="823cf-205">5 &nbsp; 6</span><span class="sxs-lookup"><span data-stu-id="823cf-205">5 &nbsp; 6</span></span></td></tr>
  <tr><td><span data-ttu-id="823cf-206">7 &nbsp; 8</span><span class="sxs-lookup"><span data-stu-id="823cf-206">7 &nbsp; 8</span></span></td></tr>
  <tr><td><span data-ttu-id="823cf-207">9</span><span class="sxs-lookup"><span data-stu-id="823cf-207">9</span></span></td></tr>
</table>

<span data-ttu-id="823cf-208">**ArrangeMethod**=**HorizontalWrap** および **列**= **2**</span><span class="sxs-lookup"><span data-stu-id="823cf-208">**ArrangeMethod**=**HorizontalWrap** and **Columns**=**2**</span></span>

<table>
  <tr>
    <td><span data-ttu-id="823cf-209">1 &nbsp; 2</span><span class="sxs-lookup"><span data-stu-id="823cf-209">1 &nbsp; 2</span></span></td>
    <td><span data-ttu-id="823cf-210">6 &nbsp; 7</span><span class="sxs-lookup"><span data-stu-id="823cf-210">6 &nbsp; 7</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-211">3 &nbsp; 4</span><span class="sxs-lookup"><span data-stu-id="823cf-211">3 &nbsp; 4</span></span></td>
    <td><span data-ttu-id="823cf-212">8 &nbsp; 9</span><span class="sxs-lookup"><span data-stu-id="823cf-212">8 &nbsp; 9</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-213">5</span><span class="sxs-lookup"><span data-stu-id="823cf-213">5</span></span></td>
    <td></td>
  </tr>
</table>

<span data-ttu-id="823cf-214">**ArrangeMethod**=**HorizontalWrap** および **列**=**塗りつぶし**</span><span class="sxs-lookup"><span data-stu-id="823cf-214">**ArrangeMethod**=**HorizontalWrap** and **Columns**=**Fill**</span></span>

<span data-ttu-id="823cf-215">この例では、コンテナーの高さに合わせることができるのは 3 行の品目だけであると仮定します。</span><span class="sxs-lookup"><span data-stu-id="823cf-215">For this example, we assume that only three lines of items can fit in the container height.</span></span>

<table>
  <tr>
    <td><span data-ttu-id="823cf-216">1 &nbsp; 2</span><span class="sxs-lookup"><span data-stu-id="823cf-216">1 &nbsp; 2</span></span></td>
    <td><span data-ttu-id="823cf-217">7 &nbsp; &nbsp; 8</span><span class="sxs-lookup"><span data-stu-id="823cf-217">7 &nbsp; &nbsp; 8</span></span></td>
    <td><span data-ttu-id="823cf-218">13 &nbsp; 14</span><span class="sxs-lookup"><span data-stu-id="823cf-218">13 &nbsp; 14</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-219">3 &nbsp; 4</span><span class="sxs-lookup"><span data-stu-id="823cf-219">3 &nbsp; 4</span></span></td>
    <td><span data-ttu-id="823cf-220">9 &nbsp; &nbsp; 10</span><span class="sxs-lookup"><span data-stu-id="823cf-220">9 &nbsp; &nbsp; 10</span></span></td>
    <td><span data-ttu-id="823cf-221">15</span><span class="sxs-lookup"><span data-stu-id="823cf-221">15</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-222">5 &nbsp; 6</span><span class="sxs-lookup"><span data-stu-id="823cf-222">5 &nbsp; 6</span></span></td>
    <td><span data-ttu-id="823cf-223">11 &nbsp; 12</span><span class="sxs-lookup"><span data-stu-id="823cf-223">11 &nbsp; 12</span></span></td>
    <td></td>
  </tr>
</table>

#### <a name="arrangemethodvertical"></a><span data-ttu-id="823cf-224">ArrangeMethod=Vertical</span><span class="sxs-lookup"><span data-stu-id="823cf-224">ArrangeMethod=Vertical</span></span>

<span data-ttu-id="823cf-225">**ArrangeMethod**= **垂直** および **列**= **1**</span><span class="sxs-lookup"><span data-stu-id="823cf-225">**ArrangeMethod**=**Vertical** and **Columns**=**1**</span></span>

<table>
  <tr><td><span data-ttu-id="823cf-226">1</span><span class="sxs-lookup"><span data-stu-id="823cf-226">1</span></span> </td></tr>
  <tr><td><span data-ttu-id="823cf-227">2</span><span class="sxs-lookup"><span data-stu-id="823cf-227">2</span></span></td></tr>
  <tr><td><span data-ttu-id="823cf-228">3</span><span class="sxs-lookup"><span data-stu-id="823cf-228">3</span></span></td></tr>
  <tr><td><span data-ttu-id="823cf-229">...</span><span class="sxs-lookup"><span data-stu-id="823cf-229">...</span></span></td></tr>
</table>

<span data-ttu-id="823cf-230">**ArrangeMethod**= **垂直** および **列**= **2**</span><span class="sxs-lookup"><span data-stu-id="823cf-230">**ArrangeMethod**=**Vertical** and **Columns**=**2**</span></span>

<table>
  <tr>
    <td><span data-ttu-id="823cf-231">1</span><span class="sxs-lookup"><span data-stu-id="823cf-231">1</span></span></td><td><span data-ttu-id="823cf-232">5</span><span class="sxs-lookup"><span data-stu-id="823cf-232">5</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-233">2</span><span class="sxs-lookup"><span data-stu-id="823cf-233">2</span></span></td><td><span data-ttu-id="823cf-234">6</span><span class="sxs-lookup"><span data-stu-id="823cf-234">6</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-235">3</span><span class="sxs-lookup"><span data-stu-id="823cf-235">3</span></span></td><td><span data-ttu-id="823cf-236">7</span><span class="sxs-lookup"><span data-stu-id="823cf-236">7</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-237">4</span><span class="sxs-lookup"><span data-stu-id="823cf-237">4</span></span></td><td><span data-ttu-id="823cf-238">8</span><span class="sxs-lookup"><span data-stu-id="823cf-238">8</span></span></td>
  </tr>
</table>

<span data-ttu-id="823cf-239">**ArrangeMethod**= **垂直** および **列**=**塗りつぶし**</span><span class="sxs-lookup"><span data-stu-id="823cf-239">**ArrangeMethod**=**Vertical** and **Columns**=**Fill**</span></span>

<span data-ttu-id="823cf-240">この例では、コンテナーの高さに合わせることができるのは 3 行の品目だけであると仮定します。</span><span class="sxs-lookup"><span data-stu-id="823cf-240">For this example, we assume that only three lines of items can fit in the container height.</span></span>

<table>
  <tr>
    <td><span data-ttu-id="823cf-241">1</span><span class="sxs-lookup"><span data-stu-id="823cf-241">1</span></span></td><td><span data-ttu-id="823cf-242">4</span><span class="sxs-lookup"><span data-stu-id="823cf-242">4</span></span></td><td><span data-ttu-id="823cf-243">7</span><span class="sxs-lookup"><span data-stu-id="823cf-243">7</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-244">2</span><span class="sxs-lookup"><span data-stu-id="823cf-244">2</span></span></td><td><span data-ttu-id="823cf-245">5</span><span class="sxs-lookup"><span data-stu-id="823cf-245">5</span></span></td><td><span data-ttu-id="823cf-246">8</span><span class="sxs-lookup"><span data-stu-id="823cf-246">8</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-247">3</span><span class="sxs-lookup"><span data-stu-id="823cf-247">3</span></span></td><td><span data-ttu-id="823cf-248">6</span><span class="sxs-lookup"><span data-stu-id="823cf-248">6</span></span></td>
  </tr>
</table>

<span data-ttu-id="823cf-249">クイック タブ上で **ArrangeMethod**= **垂直** および **列**=**塗りつぶし**</span><span class="sxs-lookup"><span data-stu-id="823cf-249">**ArrangeMethod**=**Vertical** and **Columns**=**Fill** on a FastTab</span></span>

<span data-ttu-id="823cf-250">この例では、クイック タブの幅が 4 列に収まると仮定します。</span><span class="sxs-lookup"><span data-stu-id="823cf-250">For this example, we assume that the width of the FastTab can fit four columns.</span></span>

<table>
  <tr>
    <td><span data-ttu-id="823cf-251">1</span><span class="sxs-lookup"><span data-stu-id="823cf-251">1</span></span></td><td><span data-ttu-id="823cf-252">3</span><span class="sxs-lookup"><span data-stu-id="823cf-252">3</span></span></td><td><span data-ttu-id="823cf-253">5</span><span class="sxs-lookup"><span data-stu-id="823cf-253">5</span></span></td><td><span data-ttu-id="823cf-254">7</span><span class="sxs-lookup"><span data-stu-id="823cf-254">7</span></span></td>
  </tr>
  <tr>
    <td><span data-ttu-id="823cf-255">2</span><span class="sxs-lookup"><span data-stu-id="823cf-255">2</span></span></td><td><span data-ttu-id="823cf-256">4</span><span class="sxs-lookup"><span data-stu-id="823cf-256">4</span></span></td><td><span data-ttu-id="823cf-257">6</span><span class="sxs-lookup"><span data-stu-id="823cf-257">6</span></span></td><td><span data-ttu-id="823cf-258">8</span><span class="sxs-lookup"><span data-stu-id="823cf-258">8</span></span></td>
  </tr>
</table>

## <a name="breakable-groups"></a><span data-ttu-id="823cf-259">Breakable グループ</span><span class="sxs-lookup"><span data-stu-id="823cf-259">Breakable groups</span></span>
<span data-ttu-id="823cf-260">**ColumnsMode** を **塗りつぶし** に設定して列を動的に作成するとき、利用可能な領域の量に基づいて、フィールドのグループを複数の列に分割できます。</span><span class="sxs-lookup"><span data-stu-id="823cf-260">When you set **ColumnsMode** to **Fill** to dynamically create columns, based on the amount of available space, groups of fields can be split into multiple columns.</span></span> <span data-ttu-id="823cf-261">開発者はグループ コントロールの **Breakable** プロパティで、グループ内のコントロールが列間で配布されないことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="823cf-261">The **Breakable** property on Group controls lets developers ensure that controls in a group aren't distributed across columns.</span></span> <span data-ttu-id="823cf-262">このプロパティの既定値は、**はい** で、グループの内容がグループ間で分割できることを示します。</span><span class="sxs-lookup"><span data-stu-id="823cf-262">The default value for this property is **Yes**, which indicates that the contents of the group can be split between groups.</span></span> <span data-ttu-id="823cf-263">常にグループ化しておくには、**Breakable** を **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="823cf-263">To keep a group together all the time, set **Breakable** to **No**.</span></span> <span data-ttu-id="823cf-264">**Breakable** は入れ子のグループの最初のレベルにのみ適用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="823cf-264">Note that **Breakable** applies only to the first level in nested groups.</span></span>

## <a name="guidelines-for-using-layout-properties"></a><span data-ttu-id="823cf-265">レイアウト プロパティを使用するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="823cf-265">Guidelines for using layout properties</span></span>
### <a name="columnsmodefill"></a><span data-ttu-id="823cf-266">ColumnsMode=Fill</span><span class="sxs-lookup"><span data-stu-id="823cf-266">ColumnsMode=Fill</span></span>

-   <span data-ttu-id="823cf-267">**ColumnsMode** を **入力** に設定したコンテナーを入れ子にしないでください。</span><span class="sxs-lookup"><span data-stu-id="823cf-267">Don't nest containers that have **ColumnsMode** set to **Fill**.</span></span> <span data-ttu-id="823cf-268">空き領域を応答として埋めるコントロールやフィールドの直接の親コンテナーでのみ **ColumnsMode** を **Fill** に設定します。</span><span class="sxs-lookup"><span data-stu-id="823cf-268">Set **ColumnsMode** to **Fill** only on the direct parent container of the controls/fields that you want to responsively fill the available space.</span></span>
-   <span data-ttu-id="823cf-269">**ColumnsMode** を **入力** に設定したコンテナーのどの子コントロールでも、**HeightMode** を **SizeToAvailable** に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="823cf-269">Don't set **HeightMode** to **SizeToAvailable** on any child controls of a container that has **ColumnsMode** set to **Fill**.</span></span> <span data-ttu-id="823cf-270">**ColumnsMode**=**Fill** は、列間のすべてのコントロールの平均の高さを計算して、可能な限り均等に調整しようとします。</span><span class="sxs-lookup"><span data-stu-id="823cf-270">**ColumnsMode**=**Fill** tries to calculate an average height of all controls across columns to balance them as much as possible.</span></span> <span data-ttu-id="823cf-271">しかし、レイアウト CSS および計算は **SizeToAvailable** の子を処理できず、およびこの設定は必ずしも意味がありません。</span><span class="sxs-lookup"><span data-stu-id="823cf-271">However, our layout CSS and calculations can't handle **SizeToAvailable** children, and this setting doesn't necessarily make sense.</span></span>
-   <span data-ttu-id="823cf-272">**ColumnsMode** を **入力** に設定したコンテナーのどの子コントロールでも、**WidhMode** を **SizeToAvailable** に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="823cf-272">Don't set **WidthMode** to **SizeToAvailable** on any child controls of a container that has **ColumnsMode** set to **Fill**.</span></span> <span data-ttu-id="823cf-273">それ以外の場合、子コントロールは利用可能なすべての幅を占め、すべてのコントロールが 1 つの列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="823cf-273">Otherwise, the child controls will take up all the available width, and all controls will appear in one column.</span></span>
-   <span data-ttu-id="823cf-274">**ColumnsMode**=**入力** のコンテナーは、**WidthMode** を **SizeToAvailable** (タブやグループなどの入力幅コンテナーを使用している場合) または **HeightMode** を **SizeToAvailable** (パノラマ セクションなどの入力高さコンテナーを使用している場合) に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="823cf-274">Container that have **ColumnsMode**=**Fill** should have **WidthMode** set to **SizeToAvailable** (if you're using fill-width containers such as Tabs and Groups) or **HeightMode** set to **SizeToAvailable** (if you're using fill-height containers such as Panorama sections).</span></span>

### <a name="heightmodewidthmodesizetoavailable"></a><span data-ttu-id="823cf-275">HeightMode/WidthMode=SizeToAvailable</span><span class="sxs-lookup"><span data-stu-id="823cf-275">HeightMode/WidthMode=SizeToAvailable</span></span>

-    <span data-ttu-id="823cf-276">**WidthMode**=**SizeToAvailable** を使用する場合は、フォーム内の親コンテナーに、**WidthMode** を **SizeToContent** にではなく、**SizeToAvailable** に設定するよう確認します。</span><span class="sxs-lookup"><span data-stu-id="823cf-276">If you use **WidthMode**=**SizeToAvailable**, make sure that parent containers in the form have **WidthMode** set to **SizeToAvailable**, not **SizeToContent**.</span></span> <span data-ttu-id="823cf-277">**SizeToContent** 内部のコンテナー **SizeToAvailable** コンテナー を上書きして **SizeToContent** コンテナーになります。</span><span class="sxs-lookup"><span data-stu-id="823cf-277">**SizeToAvailable** containers inside **SizeToContent** containers are overridden and become **SizeToContent** containers.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="823cf-278">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="823cf-278">Additional resources</span></span>

[<span data-ttu-id="823cf-279">ユーザー インターフェイス開発ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="823cf-279">User interface development home page</span></span>](user-interface-development-home-page.md)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]