---
title: ワークスペース タイル用のアイコンの作成
description: このトピックでは、アイコンを作成してカスタム ワークスペース タイルに割り当てるためのガイドラインと推奨事項について説明します。
author: jasongre
ms.date: 01/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 141853
ms.assetid: 4f78c3a4-011f-4ebd-bada-98e77d43821e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 435cf2c9c1323fe70954813f0c0f1f212d9abe3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752660"
---
# <a name="create-icons-for-workspace-tiles"></a><span data-ttu-id="6862f-103">ワークスペース タイル用のアイコンの作成</span><span class="sxs-lookup"><span data-stu-id="6862f-103">Create icons for workspace tiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6862f-104">このトピックでは、アイコンを作成してカスタム ワークスペース タイルに割り当てるためのガイドラインと推奨事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="6862f-104">This topic provides guidelines and recommendations for creating and assigning icons to custom workspace tiles.</span></span>  

<span data-ttu-id="6862f-105">ダッシュボードには、ユーザーがアクセスできる一連のワークスペース タイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6862f-105">The dashboard contains a set of workspace tiles to which the user has access.</span></span> <span data-ttu-id="6862f-106">これらのタイルにはそれぞれ、ワークスペースに固有のアイコンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6862f-106">Each of these tiles contains an icon specific to that workspace.</span></span> <span data-ttu-id="6862f-107">Microsoft が提供する初期状態のワークスペースでは、ワークスペースタイルに使用されるアイコンは、一般に [Dynamics の記号フォント](symbol-font.md) の記号に対応しています。</span><span class="sxs-lookup"><span data-stu-id="6862f-107">For out-of-the-box workspaces provided by Microsoft, the icons used on the workspace tiles generally correspond to a symbol from the [Dynamics Symbol font](symbol-font.md).</span></span> <span data-ttu-id="6862f-108">このトピックでは、Microsoft 認定パートナーまたは個別のユーザーが作成したワークスペースに、アイコンの作成とタイルの割り当てをするにあたってのガイドラインと推奨事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="6862f-108">This topic discusses the guidelines and recommendations for creating and assigning icons to tiles for workspaces created by Microsoft Certified Partners or individual customers.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="6862f-109">実装詳細</span><span class="sxs-lookup"><span data-stu-id="6862f-109">Implementation details</span></span>
<span data-ttu-id="6862f-110">ワークスペースのアイコンとしては、 AOT リソースのアイコンを使用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="6862f-110">For workspace icons, we recommend using an AOT resource for the icon.</span></span> <span data-ttu-id="6862f-111">既成のシンボルは機能しますが、複数のワークスペースが同じアイコンを使用することがないように、独自のシンボルを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6862f-111">While the out-of-the-box symbols will work, we recommend creating your own so that multiple workspaces don't use the same icons.</span></span> <span data-ttu-id="6862f-112">アイコンが必要となるワークスペースについては、以下のガイドラインに従って新しいイメージファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="6862f-112">For each workspace that needs an icon, create a new image file that adheres to the guidelines below.</span></span> <span data-ttu-id="6862f-113">製品の新しいバージョンに対する推奨ガイダンスが変更されたことに留意してください。</span><span class="sxs-lookup"><span data-stu-id="6862f-113">Note that the recommended guidance for newer versions of the product has changed.</span></span>

### <a name="modeling-details"></a><span data-ttu-id="6862f-114">モデリングの詳細</span><span class="sxs-lookup"><span data-stu-id="6862f-114">Modeling details</span></span>

<span data-ttu-id="6862f-115">ワークフローのタイルを作成する際には、以下のイドラインに従う必要があります:</span><span class="sxs-lookup"><span data-stu-id="6862f-115">When you create a workspace tile, you need to follow these guidelines:</span></span>

-   <span data-ttu-id="6862f-116">新しいアイコンごとに AOTResource を追加します。</span><span class="sxs-lookup"><span data-stu-id="6862f-116">Add an AOTResource for each new icon.</span></span>
-   <span data-ttu-id="6862f-117">ワークスペースに対応するタイルで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6862f-117">On the tile corresponding to the workspace, set the following properties:</span></span>
    -   <span data-ttu-id="6862f-118">ImageLocation=AOTResource</span><span class="sxs-lookup"><span data-stu-id="6862f-118">ImageLocation=AOTResource</span></span>
    -   <span data-ttu-id="6862f-119">NormalImage=&lt;AOTResource の名前&gt;</span><span class="sxs-lookup"><span data-stu-id="6862f-119">NormalImage=&lt;name of AOTResource&gt;</span></span>

## <a name="icon-creation"></a><span data-ttu-id="6862f-120">アイコン作成</span><span class="sxs-lookup"><span data-stu-id="6862f-120">Icon creation</span></span>
<span data-ttu-id="6862f-121">カスタム ワークスペース タイルのイメージ作成についてのガイドラインは以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6862f-121">Guidelines for creating images for custom workspace tiles are below.</span></span> <span data-ttu-id="6862f-122">推奨している画像のサイズとアイコンは、標準のワークスペースアイコンをもとにしています。</span><span class="sxs-lookup"><span data-stu-id="6862f-122">The recommended dimensions for the image and icon are based on the out-of-the-box workspace icons.</span></span> <span data-ttu-id="6862f-123">他の画像サイズも許容されますが、画像全体の相対的なサイズと位置は、画像サイズに関係なく維持される必要があります。</span><span class="sxs-lookup"><span data-stu-id="6862f-123">While images of other sizes are allowed, the size and positioning of the icon relative to the full image should be maintained regardless of the image size.</span></span>  

<span data-ttu-id="6862f-124">これらの推奨事項に従って、ワーク スペースのアイコンのスタイルとサイズが、他のワーク スペースのアイコンと同一のものであり、ワーク スペースのアイコンの内容が画像に適用されている CSS によって加工されないようことに留意してください。</span><span class="sxs-lookup"><span data-stu-id="6862f-124">Following these recommendations ensures that your workspace icon matches the styling and size of other workspace icons and that the content of your workspace icon does not get cropped by the CSS applied to the image.</span></span>

-   <span data-ttu-id="6862f-125">イメージ ファイルは、縦横比が 1:1 の PNG ファイルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6862f-125">The image file should be a PNG file with a 1:1 aspect ratio.</span></span>
-   <span data-ttu-id="6862f-126">推奨される最小画像サイズは、50 × 50 ピクセル (px) で、アイコンは画像の中央に位置する四角に含まれます。</span><span class="sxs-lookup"><span data-stu-id="6862f-126">The recommended minimum image size is 50 × 50 pixels (px), where the icon is contained in a square that is centered in the image.</span></span> <span data-ttu-id="6862f-127">最低 50 × 50 px の画像サイズの場合、アイコンは画像中央の **30 × 30 px** 四方 に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6862f-127">For the minimum 50 × 50 px image size, the icon should be contained in a **30 × 30 px** square in the center of the image.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6862f-128">標準のワークスペース アイコンとカスタム ワークスペース アイコンの鮮明さは、ズーム レベルで異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6862f-128">The crispness of out-of-box workspace icons and custom workspace icons might differ at different zoom levels.</span></span> <span data-ttu-id="6862f-129">この違いの理由は、PNG形式の画像が固定解像度を持っているのに対し、標準のワークスペース アイコンはフォントがスムーズに拡大縮小するからです。</span><span class="sxs-lookup"><span data-stu-id="6862f-129">The reason for this difference is that images in PNG format have a fixed resolution, whereas out-of-box workspace icons are font glyphs that scale smoothly.</span></span> <span data-ttu-id="6862f-130">異なるズーム レベルでの解像度を向上するには、同じ相対分析コードで大きな画像を作成することを考慮します。</span><span class="sxs-lookup"><span data-stu-id="6862f-130">For better resolution at different zoom levels, consider creating larger images with the same relative dimensions.</span></span> <span data-ttu-id="6862f-131">たとえば、200 ×200 px または 400 × 400 px の画像を作成します。</span><span class="sxs-lookup"><span data-stu-id="6862f-131">For example, create 200 × 200 px or 400 × 400 px images.</span></span>

-   <span data-ttu-id="6862f-132">アイコンは、 **白い背景で透明性のあるコンテンツ** となっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6862f-132">The icon should have a **white background with transparent content**.</span></span> 
-   <span data-ttu-id="6862f-133">フレームワークによって、イメージの透明な部分に既定の背景色が設定され、既存のユーザーのテーマに一致します。</span><span class="sxs-lookup"><span data-stu-id="6862f-133">The framework will set a default background color for the transparent portions of your image so that it will match the current user theme.</span></span>


## <a name="example"></a><span data-ttu-id="6862f-134">例</span><span class="sxs-lookup"><span data-stu-id="6862f-134">Example</span></span> 
<span data-ttu-id="6862f-135">新しいワークスペースに使用される次のイメージ/アイコンを検討します。</span><span class="sxs-lookup"><span data-stu-id="6862f-135">Consider the following image/icon that is to be used for a new workspace.</span></span> 

<span data-ttu-id="6862f-136">[![新しいワークスペースに使用されるアイコン](./media/newlogo3.png)](./media/newlogo3.png)</span><span class="sxs-lookup"><span data-stu-id="6862f-136">[![Icon to be used for a new workspace](./media/newlogo3.png)](./media/newlogo3.png)</span></span> 


<span data-ttu-id="6862f-137">このアイコンは、 **白い背景と透明性のあるコンテンツを持つ** 画像に変換され、アイコンは以下の図のように大きなイメージキャンバスの中央に配置されます。</span><span class="sxs-lookup"><span data-stu-id="6862f-137">This icon would be converted to an image with a **white background and transparent content** with the icon centered in a larger image canvas as shown.</span></span>  

![新しいガイダンスに従った ワークスペース アイコン](./media/baseIcon_img_PU29.png) 

<span data-ttu-id="6862f-139">これが推奨サイズ設定とどのように関連しているかを理解するには、以下の新しい推奨サイズ設定を合成したワークスペース アイコンを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6862f-139">To understand how this relates to the sizing recommendations, here is the workspace icon image overload with the new sizing recommendations.</span></span>   

![新しい推奨サイズ設定のワークスペース アイコン](./media/baseIcon_Guides_PU29.png) 

<span data-ttu-id="6862f-141">この画像をワークスペース タイルで使用すると、ダッシュ ボードには次の結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="6862f-141">Using this image on a workspace tile yields the following result on the dashboard.</span></span> 

<span data-ttu-id="6862f-142">[![ワークスペース タイルで画像を使用するときのダッシュボードでの結果](./media/newWorkspaceIcon_PU29.png)](./media/newWorkspaceIcon_PU29.png)</span><span class="sxs-lookup"><span data-stu-id="6862f-142">[![Result on the dashboard when image used on workspace tile](./media/newWorkspaceIcon_PU29.png)](./media/newWorkspaceIcon_PU29.png)</span></span>                






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]