---
title: 画像のトリミング
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像のトリミング方法について説明します。
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2cf8d43062ec527755fdf1a28f0ea3ceac1fbc15
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003831"
---
# <a name="crop-images"></a><span data-ttu-id="16eec-103">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="16eec-103">Crop images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="16eec-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像のトリミング方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16eec-104">This topic describes how to crop images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="16eec-105">概要</span><span class="sxs-lookup"><span data-stu-id="16eec-105">Overview</span></span>

<span data-ttu-id="16eec-106">Commerce サイト ビルダーのメディア ライブラリーを使用すると、画像をトリミングして、さまざまな種類のモジュールとビューポートに対して最適化することができます。</span><span class="sxs-lookup"><span data-stu-id="16eec-106">The Commerce site builder Media Library allows you to crop images to optimize them for different module types and viewports.</span></span>

## <a name="crop-an-image"></a><span data-ttu-id="16eec-107">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="16eec-107">Crop an image</span></span>

<span data-ttu-id="16eec-108">サイト ビルダーの画像をトリミングするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="16eec-108">To crop an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="16eec-109">Commerce サイト ビルダーの左側のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16eec-109">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="16eec-110">メイン ウィンドウで、変更する画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="16eec-110">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="16eec-111">コマンド バーで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16eec-111">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="16eec-112">画像を選択して、**編集モード** を入力します。</span><span class="sxs-lookup"><span data-stu-id="16eec-112">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="16eec-113">**編集モード** で、**モジュール別に画像編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16eec-113">Under **Edit Mode**, select **Edit View by Module**.</span></span>
1. <span data-ttu-id="16eec-114">**モジュール** ドロップダウン メニューから、モジュール タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="16eec-114">From the **Module** drop-down menu, select the module type.</span></span>
1. <span data-ttu-id="16eec-115">**ビュー タイプ** ドロップダウン メニューから、画像の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="16eec-115">From the **View type** drop-down menu, select the view type.</span></span>
1. <span data-ttu-id="16eec-116">**配置** ドロップダウン メニューから、画像配置を選択します。</span><span class="sxs-lookup"><span data-stu-id="16eec-116">From the **Placement** drop-down menu, select the image placement.</span></span>
1. <span data-ttu-id="16eec-117">**ビューポート** ドロップダウン メニューから、ビューポート サイズを選択します。</span><span class="sxs-lookup"><span data-stu-id="16eec-117">From the **Viewport** drop-down menu, select the viewport size.</span></span>
1. <span data-ttu-id="16eec-118">画像は、トリミング領域を表す区分に重ねて付けられます。</span><span class="sxs-lookup"><span data-stu-id="16eec-118">The image is overlaid with the area representing the crop region.</span></span> <span data-ttu-id="16eec-119">必要に応じて、トリミング領域を移動し、サイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="16eec-119">Move and resize the crop region as needed.</span></span> <span data-ttu-id="16eec-120">縦横比は自動的に管理されます。</span><span class="sxs-lookup"><span data-stu-id="16eec-120">The aspect ratio will be maintained automatically.</span></span>
1. <span data-ttu-id="16eec-121">完了したら、コマンド バーで **保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16eec-121">When you're done, on the command bar, select **Save**, and then select **Finish editing**.</span></span> 

<span data-ttu-id="16eec-122">カスタム トリミングの完了後、画像の変更はすぐに有効になります。</span><span class="sxs-lookup"><span data-stu-id="16eec-122">After custom cropping is completed, image modifications will take effect almost immediately.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16eec-123">追加リソース</span><span class="sxs-lookup"><span data-stu-id="16eec-123">Additional resources</span></span>

[<span data-ttu-id="16eec-124">資産管理の概要をデジタル化</span><span class="sxs-lookup"><span data-stu-id="16eec-124">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="16eec-125">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="16eec-125">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="16eec-126">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="16eec-126">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="16eec-127">ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="16eec-127">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="16eec-128">画像の中心のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="16eec-128">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="16eec-129">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="16eec-129">Upload and serve static files</span></span>](upload-serve-static-files.md)
