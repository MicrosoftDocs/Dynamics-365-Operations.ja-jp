---
title: POS のクライアント イメージ
description: このトピックは、小売環境で POS クライアント イメージ管理に関連する機能を実装するユーザーを対象としています。 実装の計画時に考慮すべき実装のヒントとガイダンスについて説明します。
author: josaw1
manager: annbe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: cbittner
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: c80266a06a3b90dc6be5f3a5dea416b6e7656ed7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004677"
---
# <a name="client-images-in-pos"></a><span data-ttu-id="68384-104">POS のクライアント イメージ</span><span class="sxs-lookup"><span data-stu-id="68384-104">Client images in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="68384-105">このトピックは、小売環境で POS (販売時点管理) クライアント イメージ管理に関連する機能を実装するユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="68384-105">This topic is intended for people who implement functionality related to point of sale (POS) client image management in a retail environment.</span></span> <span data-ttu-id="68384-106">実装の計画時に考慮すべきヒントとガイダンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="68384-106">It provides tips and guidance to consider when planning an implementation.</span></span>

<span data-ttu-id="68384-107">このガイドは、クラウド POSと Modern POS の両方に適用されます。これにより、ストアでのユーザー エクスペリエンスを強化し、アップセル、クロスセル、顧客サービスなどの顧客中心のシナリオをサポートするために使用できるイメージ ファイル サイズの処理とイメージのタイプに関する一般情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="68384-107">This guidance applies to both Cloud POS and Modern POS, and provides some general information about image file size handling and types of images that can be used to enrich the user experience with the store and support customer-focused scenarios like up-selling, cross-selling, and clientelling.</span></span> <span data-ttu-id="68384-108">ようこそ画面イメージ、カテゴリ イメージ、および製品イメージは、使用できるイメージ タイプの一例です。</span><span class="sxs-lookup"><span data-stu-id="68384-108">Welcome screen images, category images, and product images are examples of types of images that you can use.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="68384-109">実装の考慮事項</span><span class="sxs-lookup"><span data-stu-id="68384-109">Implementation considerations</span></span>

- <span data-ttu-id="68384-110">**ファイル サイズ** - さまざまなタイプのイメージをロードしながら、POS クライアント ユーザー インターフェイス (UI) とパフォーマンスの応答性を維持するために、使用目的に応じて適切なファイル サイズになるようにイメージを準備することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="68384-110">**File size** - In order to maintain responsiveness of the POS client user interface (UI) and performance while loading different kinds of images, we recommend that you prepare your images to be an appropriate file size respective to the purpose of use.</span></span> <span data-ttu-id="68384-111">たとえば、Contoso デモ データ内の製品およびカテゴリのイメージのサイズは、500 x 500 または 580 x 580 ピクセルです。</span><span class="sxs-lookup"><span data-stu-id="68384-111">For example, product and category images in the Contoso demo data are sized at 500 x 500 or 580 x 580 pixels.</span></span>

- <span data-ttu-id="68384-112">**イメージ サイズ** - POS デバイスの画面とディスプレイは、適正なイメージ サイズ (長さと幅) を事前に決定します。</span><span class="sxs-lookup"><span data-stu-id="68384-112">**Image size** - The screens and displays of the POS devices will pre-determine reasonable image sizes (length and width).</span></span> <span data-ttu-id="68384-113">イメージ サイズは、意図した画面サイズにできるだけ近づける必要があります。</span><span class="sxs-lookup"><span data-stu-id="68384-113">You should size the image as close to your intended screen size as possible.</span></span> <span data-ttu-id="68384-114">例については、以下の「実装の例」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="68384-114">For an example, see the "Implementation example" section below.</span></span>

- <span data-ttu-id="68384-115">**解決策** - 考慮すべき重要なパラメーターは、1 インチあたりのドット数 (dpi)、または画面解像度の場合は 1 インチあたりのピクセル数 (ppi) です。</span><span class="sxs-lookup"><span data-stu-id="68384-115">**Resolution** - An important parameter to consider is the dots per inch (dpi), or for screen resolution, pixel per inch (ppi).</span></span> <span data-ttu-id="68384-116">POS クライアント イメージは印刷されないため、Web 上で画像を表示するための共通 dpi 設定は適切なガイドラインです (72 ~ 150 dpi)。</span><span class="sxs-lookup"><span data-stu-id="68384-116">Because POS client images will not be printed, the common dpi setting for rendering images on the web is a good guideline (72 to 150 dpi).</span></span> <span data-ttu-id="68384-117">Contoso デモ イメージ ファイルは、通常 96 dpiで表示されます。</span><span class="sxs-lookup"><span data-stu-id="68384-117">Contoso demo image files are typically rendered to 96 dpi.</span></span> <span data-ttu-id="68384-118">高解像度のデバイスの場合、実際のピクセルではなく、オペレーティング システム (OS) のスケーリングを考慮し、有効な解像度を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68384-118">For high resolution devices, you should take operating system (OS) scaling into account and use the effective resolution, rather than the actual pixels.</span></span>

- <span data-ttu-id="68384-119">**ファイル タイプ** –  \*.png または \*.jpg イメージ ファイル タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="68384-119">**File types** – You can use \*.png or \*.jpg image file types.</span></span> <span data-ttu-id="68384-120">ほとんどの場合、\*.jpg のサイズは小さくなります。</span><span class="sxs-lookup"><span data-stu-id="68384-120">In most cases, \*.jpg are smaller in size.</span></span>

## <a name="implementation-example"></a><span data-ttu-id="68384-121">実装の例</span><span class="sxs-lookup"><span data-stu-id="68384-121">Implementation example</span></span> 
<span data-ttu-id="68384-122">1366 x 768 ピクセルの解像度と Contoso デモ データに類似した画面レイアウトを備えた一般的な 18.5 インチ PO Sディスプレイで、キャンバスの 3 分の 2 をカバーするウェルカム画面イメージを作成するには、画面の長さと幅よりもそれほど高くない解像度の画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="68384-122">To create a welcome screen image that covers two-thirds of the canvas on a common 18.5 inch POS display with a 1366 x 768 pixel resolution and a screen layout similar to Contoso demo data, choose an image with resolution that is not much higher than the length and width of the screen.</span></span> <span data-ttu-id="68384-123">この例では、911 x 512 ピクセルの解像度で十分です。</span><span class="sxs-lookup"><span data-stu-id="68384-123">In this example, 911 x 512 pixel resolution is sufficient.</span></span> <span data-ttu-id="68384-124">長さと幅に比較的高い解像度を選択しても、低い dpi 設定を維持すると、ファイル サイズは適度に小さくなります。</span><span class="sxs-lookup"><span data-stu-id="68384-124">Selecting a relatively high resolution for length and width but keeping a low dpi setting will still result in reasonably small file sizes.</span></span>
