---
title: 画像の焦点のカスタマイズ
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像焦点のカスタマイズについて説明します。
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 962caff0e8e41487231c6075fa7b2df2a59dca48
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799304"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="e8c1f-103">画像の中心のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="e8c1f-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8c1f-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像焦点のカスタマイズについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="e8c1f-105">画像が Commerce サイト ビルダーのメディア ライブラリーにアップロードされると、システムによって画像の焦点が決定されます。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-105">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="e8c1f-106">たとえば、画像に人物が含まれている場合、既定では、システムによって焦点が人物の顔に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-106">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="e8c1f-107">ほとんどの場合、自動的に設定される焦点ポイントはすべてのビューポートに対して有効ですが、場合によっては、画像の特定の部分が常に表示されるように焦点を調整することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-107">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="e8c1f-108">画像のカスタム焦点の定義</span><span class="sxs-lookup"><span data-stu-id="e8c1f-108">Define a custom focal point for an image</span></span>

<span data-ttu-id="e8c1f-109">画像のカスタム焦点を定義するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-109">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="e8c1f-110">Commerce サイト ビルダーの左側のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-110">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="e8c1f-111">メイン ウィンドウで、変更する画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-111">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="e8c1f-112">コマンド バーで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-112">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="e8c1f-113">画像を選択して、**編集モード** を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-113">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="e8c1f-114">**編集モード** で、**焦点を変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-114">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="e8c1f-115">画像上に、円形の焦点コントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-115">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="e8c1f-116">焦点コントロールを選択して、目的の焦点の上に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-116">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="e8c1f-117">完了したら、コマンド バーで **保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c1f-117">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8c1f-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e8c1f-118">Additional resources</span></span>

[<span data-ttu-id="e8c1f-119">デジタル資産管理の概要</span><span class="sxs-lookup"><span data-stu-id="e8c1f-119">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="e8c1f-120">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="e8c1f-120">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="e8c1f-121">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="e8c1f-121">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="e8c1f-122">ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="e8c1f-122">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="e8c1f-123">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="e8c1f-123">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="e8c1f-124">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="e8c1f-124">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
