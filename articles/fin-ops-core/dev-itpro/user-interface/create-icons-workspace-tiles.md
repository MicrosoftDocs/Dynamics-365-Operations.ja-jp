---
title: ワークスペース タイル用のアイコンの作成
description: このトピックでは、アイコンを作成してカスタム ワークスペース タイルに割り当てるためのガイドラインと推奨事項について説明します。
author: jasongre
manager: AnnBe
ms.date: 08/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 141853
ms.assetid: 4f78c3a4-011f-4ebd-bada-98e77d43821e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 3c7c0e8b7edf46cab677d3b8149fdc9509132de5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682457"
---
# <a name="create-icons-for-workspace-tiles"></a><span data-ttu-id="9dbec-103">ワークスペース タイル用のアイコンの作成</span><span class="sxs-lookup"><span data-stu-id="9dbec-103">Create icons for workspace tiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9dbec-104">このトピックでは、アイコンを作成してカスタム ワークスペース タイルに割り当てるためのガイドラインと推奨事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="9dbec-104">This topic provides guidelines and recommendations for creating and assigning icons to custom workspace tiles.</span></span>  

<span data-ttu-id="9dbec-105">ダッシュボードには、ユーザーがアクセスできる一連のワークスペース タイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9dbec-105">The dashboard contains a set of workspace tiles to which the user has access.</span></span> <span data-ttu-id="9dbec-106">これらのタイルにはそれぞれ、ワークスペースに固有のアイコンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9dbec-106">Each of these tiles contains an icon specific to that workspace.</span></span> <span data-ttu-id="9dbec-107">Microsoft が提供する初期状態のワークスペースでは、ワークスペースタイルに使用されるアイコンは、一般に [Dynamics の記号フォント](symbol-font.md) の記号に対応しています。</span><span class="sxs-lookup"><span data-stu-id="9dbec-107">For out-of-the-box workspaces provided by Microsoft, the icons used on the workspace tiles generally correspond to a symbol from the [Dynamics Symbol font](symbol-font.md).</span></span> <span data-ttu-id="9dbec-108">このトピックでは、Microsoft 認定パートナーまたは個別のユーザーが作成したワークスペースに、アイコンの作成とタイルの割り当てをするにあたってのガイドラインと推奨事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="9dbec-108">This topic discusses the guidelines and recommendations for creating and assigning icons to tiles for workspaces created by Microsoft Certified Partners or individual customers.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="9dbec-109">実装詳細</span><span class="sxs-lookup"><span data-stu-id="9dbec-109">Implementation details</span></span>
<span data-ttu-id="9dbec-110">ワークスペースのアイコンとしては、 AOT リソースのアイコンを使用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="9dbec-110">For workspace icons, we recommend using an AOT resource for the icon.</span></span> <span data-ttu-id="9dbec-111">既成のシンボルは機能しますが、複数のワークスペースが同じアイコンを使用することがないように、独自のシンボルを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9dbec-111">While the out-of-the-box symbols will work, we recommend creating your own so that multiple workspaces don't use the same icons.</span></span> <span data-ttu-id="9dbec-112">アイコンが必要となるワークスペースについては、以下のガイドラインに従って新しいイメージファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9dbec-112">For each workspace that needs an icon, create a new image file that adheres to the guidelines below.</span></span> <span data-ttu-id="9dbec-113">製品の新しいバージョンに対する推奨ガイダンスが変更されたことに留意してください。</span><span class="sxs-lookup"><span data-stu-id="9dbec-113">Note that the recommended guidance for newer versions of the product has changed.</span></span>

### <a name="modeling-details"></a><span data-ttu-id="9dbec-114">モデリングの詳細</span><span class="sxs-lookup"><span data-stu-id="9dbec-114">Modeling details</span></span>

<span data-ttu-id="9dbec-115">ワークフローのタイルを作成する際には、以下のイドラインに従う必要があります:</span><span class="sxs-lookup"><span data-stu-id="9dbec-115">When you create a workspace tile, you need to follow these guidelines:</span></span>

-   <span data-ttu-id="9dbec-116">新しいアイコンごとに AOTResource を追加します。</span><span class="sxs-lookup"><span data-stu-id="9dbec-116">Add an AOTResource for each new icon.</span></span>
-   <span data-ttu-id="9dbec-117">ワークスペースに対応するタイルで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9dbec-117">On the tile corresponding to the workspace, set the following properties:</span></span>
    -   <span data-ttu-id="9dbec-118">ImageLocation=AOTResource</span><span class="sxs-lookup"><span data-stu-id="9dbec-118">ImageLocation=AOTResource</span></span>
    -   <span data-ttu-id="9dbec-119">NormalImage=&lt;AOTResource の名前&gt;</span><span class="sxs-lookup"><span data-stu-id="9dbec-119">NormalImage=&lt;name of AOTResource&gt;</span></span>

## <a name="icon-creation"></a><span data-ttu-id="9dbec-120">アイコン作成</span><span class="sxs-lookup"><span data-stu-id="9dbec-120">Icon creation</span></span>
<span data-ttu-id="9dbec-121">カスタム ワークスペース タイルのイメージ作成についてのガイドラインは以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9dbec-121">Guidelines for creating images for custom workspace tiles are below.</span></span> <span data-ttu-id="9dbec-122">推奨している画像のサイズとアイコンは、標準のワークスペースアイコンをもとにしています。</span><span class="sxs-lookup"><span data-stu-id="9dbec-122">The recommended dimensions for the image and icon are based on the out-of-the-box workspace icons.</span></span> <span data-ttu-id="9dbec-123">他の画像サイズも許容されますが、画像全体の相対的なサイズと位置は、画像サイズに関係なく維持される必要があります。</span><span class="sxs-lookup"><span data-stu-id="9dbec-123">While images of other sizes are allowed, the size and positioning of the icon relative to the full image should be maintained regardless of the image size.</span></span>  

<span data-ttu-id="9dbec-124">これらの推奨事項に従って、ワーク スペースのアイコンのスタイルとサイズが、他のワーク スペースのアイコンと同一のものであり、ワーク スペースのアイコンの内容が画像に適用されている CSS によって加工されないようことに留意してください。</span><span class="sxs-lookup"><span data-stu-id="9dbec-124">Following these recommendations ensures that your workspace icon matches the styling and size of other workspace icons and that the content of your workspace icon does not get cropped by the CSS applied to the image.</span></span>

### <a name="images-for-platform-update-29-or-later"></a><span data-ttu-id="9dbec-125">プラットフォーム更新プログラム 29 またはそれ以降における画像</span><span class="sxs-lookup"><span data-stu-id="9dbec-125">Images for Platform update 29 or later</span></span>
-   <span data-ttu-id="9dbec-126">イメージ ファイルは、縦横比が 1:1 の PNG ファイルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9dbec-126">The image file should be a PNG file with a 1:1 aspect ratio.</span></span>
-   <span data-ttu-id="9dbec-127">推奨する画像サイズは 50 x 50 ピクセルで、アイコンは中央部分の **30 x 30 px** ピクセルに収まるように配置します (以下の図を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="9dbec-127">The recommended image size is 50 x 50 pixels, with the icon being contained within a centered **30 x 30 px** square (see the illustration below).</span></span>
-   <span data-ttu-id="9dbec-128">アイコンは、 **白い背景で透明性のあるコンテンツ** となっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9dbec-128">The icon should have a **white background with transparent content**.</span></span> 
-   <span data-ttu-id="9dbec-129">フレームワークによって、イメージの透明な部分に既定の背景色が設定され、既存のユーザーのテーマに一致します。</span><span class="sxs-lookup"><span data-stu-id="9dbec-129">The framework will set a default background color for the transparent portions of your image so that it will match the current user theme.</span></span>

### <a name="images-for-platform-update-28-or-earlier"></a><span data-ttu-id="9dbec-130">プラットフォーム更新プログラム 28 またはそれ以前における画像</span><span class="sxs-lookup"><span data-stu-id="9dbec-130">Images for Platform update 28 or earlier</span></span>
-   <span data-ttu-id="9dbec-131">イメージ ファイルは、縦横比が 1:1 の PNG ファイルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9dbec-131">The image file should be a PNG file with a 1:1 aspect ratio.</span></span>
-   <span data-ttu-id="9dbec-132">推奨する画像サイズは 50 x 50 ピクセルで、アイコンは中央部分の **21 x 21 px** ピクセルに収まるように配置します (以下の図を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="9dbec-132">The recommended image size is 50 x 50 pixels, with the icon being contained within a centered **21 x 21 px** square (see the illustration below).</span></span>
-   <span data-ttu-id="9dbec-133">アイコンは、 **透明性のある背景で白いコンテンツ** となっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9dbec-133">The icon should have a **transparent background with white content**.</span></span>
-   <span data-ttu-id="9dbec-134">フレームワークによって、イメージの透明な部分に既定の背景色が設定され、既存のユーザーのテーマに一致します。</span><span class="sxs-lookup"><span data-stu-id="9dbec-134">The framework will set a default background color for the transparent portions of your image so that it will match the current user theme.</span></span>

## <a name="example"></a><span data-ttu-id="9dbec-135">例</span><span class="sxs-lookup"><span data-stu-id="9dbec-135">Example</span></span> 
<span data-ttu-id="9dbec-136">新しいワークスペースに使用される次のイメージ/アイコンを検討します。</span><span class="sxs-lookup"><span data-stu-id="9dbec-136">Consider the following image/icon that is to be used for a new workspace.</span></span> 

<span data-ttu-id="9dbec-137">[![新しいワークスペースに使用されるアイコン](./media/newlogo3.png)](./media/newlogo3.png)</span><span class="sxs-lookup"><span data-stu-id="9dbec-137">[![Icon to be used for a new workspace](./media/newlogo3.png)](./media/newlogo3.png)</span></span> 

### <a name="platform-update-29-or-later"></a><span data-ttu-id="9dbec-138">プラットフォーム更新プログラム 29 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="9dbec-138">Platform update 29 or later</span></span> 

<span data-ttu-id="9dbec-139">このアイコンは、 **白い背景と透明性のあるコンテンツを持つ** 画像に変換され、アイコンは以下の図のように大きなイメージキャンバスの中央に配置されます。</span><span class="sxs-lookup"><span data-stu-id="9dbec-139">This icon would be converted to an image with a **white background and transparent content** with the icon centered in a larger image canvas as shown.</span></span>  

![新しいガイダンスに従った ワークスペース アイコン](./media/baseIcon_img_PU29.png) 

<span data-ttu-id="9dbec-141">これが推奨サイズ設定とどのように関連しているかを理解するには、以下の新しい推奨サイズ設定を合成したワークスペース アイコンを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9dbec-141">To understand how this relates to the sizing recommendations, here is the workspace icon image overload with the new sizing recommendations.</span></span>   

![新しい推奨サイズ設定のワークスペース アイコン](./media/baseIcon_Guides_PU29.png) 

<span data-ttu-id="9dbec-143">この画像をワークスペース タイルで使用すると、ダッシュ ボードには次の結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="9dbec-143">Using this image on a workspace tile yields the following result on the dashboard.</span></span> 

<span data-ttu-id="9dbec-144">[![ワークスペース タイルで画像を使用するときのダッシュボードでの結果](./media/newWorkspaceIcon_PU29.png)](./media/newWorkspaceIcon_PU29.png)</span><span class="sxs-lookup"><span data-stu-id="9dbec-144">[![Result on the dashboard when image used on workspace tile](./media/newWorkspaceIcon_PU29.png)](./media/newWorkspaceIcon_PU29.png)</span></span>                


### <a name="platform-update-28-or-earlier"></a><span data-ttu-id="9dbec-145">プラットフォーム更新プログラム 28 またはそれ以前</span><span class="sxs-lookup"><span data-stu-id="9dbec-145">Platform update 28 or earlier</span></span>
<span data-ttu-id="9dbec-146">旧バージョンの製品では、アイコンは透明な背景と白いコンテンツを持つ画像に変換され、アイコンは以下の図のようにイメージキャンバスの中央に配置されます。</span><span class="sxs-lookup"><span data-stu-id="9dbec-146">For older versions of the product, the icon would be converted to an image with a transparent background and white content with the icon centered in the image canvas as shown.</span></span> 

![古いのバージョンのワークスペース アイコン](./media/newicon.png) 

<span data-ttu-id="9dbec-148">これが推奨サイズ設定とどのように関連しているかを理解するには、以下の古い推奨サイズ設定を合成したワークスペース アイコンを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9dbec-148">To understand how this relates to the sizing recommendations, here is the workspace icon image overload with the previous sizing recommendations.</span></span>   

![古い推奨サイズ設定のワークスペース アイコン](./media/newicon_guides.png) 

<span data-ttu-id="9dbec-150">この画像をワークスペース タイルで使用すると、ダッシュ ボードには次の結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="9dbec-150">Using this image on a workspace tile yields the following result on the dashboard.</span></span> 

<span data-ttu-id="9dbec-151">[![ワークスペース タイルで画像を使用するときのダッシュボードでの結果](./media/newworkspaceicon.png)](./media/newworkspaceicon.png)</span><span class="sxs-lookup"><span data-stu-id="9dbec-151">[![Result on the dashboard when image used on workspace tile](./media/newworkspaceicon.png)](./media/newworkspaceicon.png)</span></span>                




