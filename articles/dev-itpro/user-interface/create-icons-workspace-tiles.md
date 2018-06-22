---
title: "ワークスペース タイル用のアイコンの作成"
description: "このトピックでは、アイコンを作成してカスタム ワークスペース タイルに割り当てるためのガイドラインと推奨事項について説明します。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 141853
ms.assetid: 4f78c3a4-011f-4ebd-bada-98e77d43821e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3cd0c01303412c304db6cb8be9549f02f3b26df4
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="create-icons-for-workspace-tiles"></a><span data-ttu-id="64c9c-103">ワークスペース タイル用のアイコンの作成</span><span class="sxs-lookup"><span data-stu-id="64c9c-103">Create icons for workspace tiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64c9c-104">このトピックでは、アイコンを作成してカスタム ワークスペース タイルに割り当てるためのガイドラインと推奨事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="64c9c-104">This topic provides guidelines and recommendations for creating and assigning icons to custom workspace tiles.</span></span>  

<span data-ttu-id="64c9c-105">ダッシュボードには、ユーザーがアクセスできる一連のワークスペース タイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="64c9c-105">The dashboard contains a set of workspace tiles to which the user has access.</span></span> <span data-ttu-id="64c9c-106">これらのタイルにはそれぞれ、ワークスペースに固有のアイコンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="64c9c-106">Each of these tiles contains an icon specific to that workspace.</span></span> <span data-ttu-id="64c9c-107">Microsoft により提供された追加設定なしのワークスペースについては、ワークスペースタイルで使用されるアイコンは一般的に [記号フォント](symbol-font.md) からの記号に対応します。</span><span class="sxs-lookup"><span data-stu-id="64c9c-107">For out-of-the-box workspaces provided by Microsoft, the icons used on the workspace tiles generally correspond to a symbol from the [Symbol font](symbol-font.md).</span></span> <span data-ttu-id="64c9c-108">この記事では、マイクロソフト認定パートナーまたは個人のお客様が作成したワークスペースのアイコンを作成してタイルに割り当てるためのガイドラインと推奨事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="64c9c-108">This article discusses the guidelines and recommendations for creating and assigning icons to tiles for workspaces created by Microsoft Certified Partners or individual customers.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="64c9c-109">実装詳細</span><span class="sxs-lookup"><span data-stu-id="64c9c-109">Implementation details</span></span>
### <a name="icon-creation"></a><span data-ttu-id="64c9c-110">アイコン作成</span><span class="sxs-lookup"><span data-stu-id="64c9c-110">Icon creation</span></span>

<span data-ttu-id="64c9c-111">ワークスペース アイコンについては、アイコンの AOT リソースを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="64c9c-111">For workspace icons we recommend using an AOT resource for the icon.</span></span> <span data-ttu-id="64c9c-112">既成のシンボルは機能しますが、複数のワークスペースが同じアイコンを使用することがないように、独自のシンボルを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="64c9c-112">While the out-of-the-box symbols will work, we recommend creating your own so that multiple workspaces don't use the same icons.</span></span> <span data-ttu-id="64c9c-113">アイコンが必要な各ワークスペースについては、以下のガイドラインに準拠している新しい画像ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="64c9c-113">For each workspace that needs an icon, create a new image file that adheres to the following guidelines:</span></span>

-   <span data-ttu-id="64c9c-114">イメージ ファイルは、縦横比が 1:1 の PNG ファイルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c9c-114">The image file should be a PNG file with a 1:1 aspect ratio.</span></span>
-   <span data-ttu-id="64c9c-115">アイコンは白いコンテンツの透明な背景にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c9c-115">The icon should have a transparent background with white content.</span></span> <span data-ttu-id="64c9c-116">このフレームワークはテーマに合わせて既定の背景色を設定します。</span><span class="sxs-lookup"><span data-stu-id="64c9c-116">The framework will then set a default background color to match the theme.</span></span>
-   <span data-ttu-id="64c9c-117">推奨画像サイズは、アイコンが中央の 21 x 21 ピクセルの正方形内に配置されている、50 x 50 ピクセルです (下図参照)。</span><span class="sxs-lookup"><span data-stu-id="64c9c-117">The recommended image size is 50 x 50 pixels, with the icon being contained within a centered 21 x 21 px square (see the illustration below).</span></span>
    -   <span data-ttu-id="64c9c-118">推奨される画像とアイコンのサイズは、すぐに使用できるワークスペースに対応しています。</span><span class="sxs-lookup"><span data-stu-id="64c9c-118">The recommended image and icon sizes correspond to the out-of-the-box workspaces.</span></span> <span data-ttu-id="64c9c-119">大きいイメージは使用できません。ただし、フル イメージに関連するアイコンのサイズと配置はイメージのサイズに関係なく保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c9c-119">Larger images are allowed; however, the size and positioning of the icon relative to the full image should be maintained regardless of image size.</span></span>
    -   <span data-ttu-id="64c9c-120">この推奨に従うことにより、以下の点ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="64c9c-120">Following this recommendation ensures the following:</span></span>
        -   <span data-ttu-id="64c9c-121">ワークスペース アイコンは、他のワークスペース アイコンのサイズと一致します。</span><span class="sxs-lookup"><span data-stu-id="64c9c-121">Your workspace icon matches the size of other workspace icons.</span></span>
        -   <span data-ttu-id="64c9c-122">ワークスペースのアイコンのコンテンツは、画像を円としてレンダリングする CSS によってトリミングされません。</span><span class="sxs-lookup"><span data-stu-id="64c9c-122">The content of your workspace icon does not get cropped by the CSS that renders the image as a circle.</span></span>

![workspaceIconSizing](./media/workspaceiconsizing.png)

### <a name="modeling-details"></a><span data-ttu-id="64c9c-124">モデリングの詳細</span><span class="sxs-lookup"><span data-stu-id="64c9c-124">Modeling details</span></span>

<span data-ttu-id="64c9c-125">ワークスペース タイルを作成するときは、次のガイドラインに準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c9c-125">As you create a workspace tile, adhere to the following guidelines:</span></span>

-   <span data-ttu-id="64c9c-126">新しいアイコンごとに AOTResource を追加します。</span><span class="sxs-lookup"><span data-stu-id="64c9c-126">Add an AOTResource for each new icon.</span></span>
-   <span data-ttu-id="64c9c-127">ワークスペースに対応するタイルで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="64c9c-127">On the tile corresponding to the workspace, set the following properties:</span></span>
    -   <span data-ttu-id="64c9c-128">ImageLocation=AOTResource</span><span class="sxs-lookup"><span data-stu-id="64c9c-128">ImageLocation=AOTResource</span></span>
    -   <span data-ttu-id="64c9c-129">NormalImage=&lt;AOTResource の名前&gt;</span><span class="sxs-lookup"><span data-stu-id="64c9c-129">NormalImage=&lt;name of AOTResource&gt;</span></span>

## <a name="example"></a><span data-ttu-id="64c9c-130">例</span><span class="sxs-lookup"><span data-stu-id="64c9c-130">Example</span></span>
<span data-ttu-id="64c9c-131">新しいワークスペースに使用される次のイメージ/アイコンを検討します。</span><span class="sxs-lookup"><span data-stu-id="64c9c-131">Consider the following image/icon that is to be used for a new workspace.</span></span> 

<span data-ttu-id="64c9c-132">[![newLogo3](./media/newlogo3.png)](./media/newlogo3.png)</span><span class="sxs-lookup"><span data-stu-id="64c9c-132">[![newLogo3](./media/newlogo3.png)](./media/newlogo3.png)</span></span> 

<span data-ttu-id="64c9c-133">このアイコンは透明な背景を持つイメージに変換され、アイコンの白いコンテンツは大きなイメージ キャンバスの中央に配置されます。</span><span class="sxs-lookup"><span data-stu-id="64c9c-133">This icon would be converted to an image with a transparent background, and white content with the icon centered in a larger image canvas.</span></span> 

![newIcon](./media/newicon.png) 

<span data-ttu-id="64c9c-135">ワークスペース アイコンのイメージ</span><span class="sxs-lookup"><span data-stu-id="64c9c-135">Workspace icon image</span></span>

![newIcon\_guides](./media/newicon_guides.png) 

<span data-ttu-id="64c9c-137">ワークスペース アイコンのイメージは、アイコンのために取り分けられた領域とともに、タイル上の可視の循環部分を表示するために重ねて表示されます。</span><span class="sxs-lookup"><span data-stu-id="64c9c-137">Workspace icon image overlaid to show the circular portion visible on the tile as well as the area set aside for the icon.</span></span>

<span data-ttu-id="64c9c-138">この画像をワークスペース タイルで使用すると、ダッシュ ボードには次の結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="64c9c-138">Using this image on a workspace tile yields the following result on the dashboard.</span></span> 

<span data-ttu-id="64c9c-139">[![newWorkspaceIcon](./media/newworkspaceicon.png)](./media/newworkspaceicon.png)</span><span class="sxs-lookup"><span data-stu-id="64c9c-139">[![newWorkspaceIcon](./media/newworkspaceicon.png)](./media/newworkspaceicon.png)</span></span>                




