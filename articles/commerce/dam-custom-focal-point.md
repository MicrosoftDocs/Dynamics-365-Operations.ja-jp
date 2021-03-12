---
title: 画像の焦点のカスタマイズ
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像焦点のカスタマイズについて説明します。
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
ms.openlocfilehash: 9c8fc9a1f944d24aff3ab2923ca2715209a674e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972935"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="66f1c-103">画像の焦点のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="66f1c-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="66f1c-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの画像焦点のカスタマイズについて説明します。</span><span class="sxs-lookup"><span data-stu-id="66f1c-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="66f1c-105">概要</span><span class="sxs-lookup"><span data-stu-id="66f1c-105">Overview</span></span>

<span data-ttu-id="66f1c-106">画像が Commerce サイト ビルダーのメディア ライブラリーにアップロードされると、システムによって画像の焦点が決定されます。</span><span class="sxs-lookup"><span data-stu-id="66f1c-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="66f1c-107">たとえば、画像に人物が含まれている場合、既定では、システムによって焦点が人物の顔に設定されます。</span><span class="sxs-lookup"><span data-stu-id="66f1c-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="66f1c-108">ほとんどの場合、自動的に設定される焦点ポイントはすべてのビューポートに対して有効ですが、場合によっては、画像の特定の部分が常に表示されるように焦点を調整することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="66f1c-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="66f1c-109">画像のカスタム焦点の定義</span><span class="sxs-lookup"><span data-stu-id="66f1c-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="66f1c-110">画像のカスタム焦点を定義するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66f1c-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="66f1c-111">Commerce サイト ビルダーの左側のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66f1c-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="66f1c-112">メイン ウィンドウで、変更する画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="66f1c-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="66f1c-113">コマンド バーで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66f1c-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="66f1c-114">画像を選択して、**編集モード** を入力します。</span><span class="sxs-lookup"><span data-stu-id="66f1c-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="66f1c-115">**編集モード** で、**焦点を変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66f1c-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="66f1c-116">画像上に、円形の焦点コントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66f1c-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="66f1c-117">焦点コントロールを選択して、目的の焦点の上に移動します。</span><span class="sxs-lookup"><span data-stu-id="66f1c-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="66f1c-118">完了したら、コマンド バーで **保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66f1c-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66f1c-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="66f1c-119">Additional resources</span></span>

[<span data-ttu-id="66f1c-120">デジタル資産管理の概要</span><span class="sxs-lookup"><span data-stu-id="66f1c-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="66f1c-121">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="66f1c-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="66f1c-122">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="66f1c-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="66f1c-123">ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="66f1c-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="66f1c-124">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="66f1c-124">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="66f1c-125">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="66f1c-125">Upload and serve static files</span></span>](upload-serve-static-files.md)
