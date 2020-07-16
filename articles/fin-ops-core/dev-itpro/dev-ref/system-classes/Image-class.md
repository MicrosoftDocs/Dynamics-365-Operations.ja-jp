---
title: Image クラス
description: このトピックでは、Image クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 596a07c9880c07b24b2309f34263ab88853113c4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502902"
---
# <a name="class-image"></a><span data-ttu-id="0f8ef-103">クラス イメージ</span><span class="sxs-lookup"><span data-stu-id="0f8ef-103">Class Image</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Image extends BinData
```

<span data-ttu-id="0f8ef-104">読み込み、保存、および画像を操作するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-104">Provides methods for loading, saving, and manipulating images.</span></span> <span data-ttu-id="0f8ef-105">複数のイメージを同時に操作する場合は、Imagelist クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-105">If you want to manipulate several images at the same time, use the Imagelist Class.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f8ef-106">備考</span><span class="sxs-lookup"><span data-stu-id="0f8ef-106">Remarks</span></span>

<span data-ttu-id="0f8ef-107">次のファイル タイプからイメージ オブジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-107">You can construct Image objects from the following file types:</span></span>

-   <span data-ttu-id="0f8ef-108">ラスター (ビットマップ) 形式 - .bmp、.gif、.jpg、.png、.tiff、.exif</span><span class="sxs-lookup"><span data-stu-id="0f8ef-108">Raster (bitmap) formats - .bmp, .gif, .jpg, .png, .tiff, and .exif</span></span>
-   <span data-ttu-id="0f8ef-109">ベクター形式 - .emf および .wmf</span><span class="sxs-lookup"><span data-stu-id="0f8ef-109">Vector formats - .emf and .wmf</span></span>

<span data-ttu-id="0f8ef-110">複数のイメージを同時に操作する場合は、Imagelist クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-110">If you want to work with several images at the same time, use the Imagelist class.</span></span> <span data-ttu-id="0f8ef-111">次のファイル タイプからイメージ オブジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-111">You can construct the Image objects from the following file types:</span></span>

-   <span data-ttu-id="0f8ef-112">ラスター (ビットマップである) 形式 - .bmp、.gif、.jpg、.png、.tiff、.exif</span><span class="sxs-lookup"><span data-stu-id="0f8ef-112">Raster, which is a bitmap, formats - .bmp, .gif, .jpg, .png, .tiff, and .exif</span></span>
-   <span data-ttu-id="0f8ef-113">ベクター形式 - .emf および .wmf</span><span class="sxs-lookup"><span data-stu-id="0f8ef-113">Vector formats - .emf and .wmf</span></span>

<span data-ttu-id="0f8ef-114">イメージ クラスは、クライアントにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-114">The Image class is bound to the client.</span></span> <span data-ttu-id="0f8ef-115">ファイル操作に伴うセキュリティ上のリスクのため、クラスをサーバーから実行できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-115">The class can no longer be run from the server because of the security risks that are associated with file handling.</span></span>

## <a name="examples"></a><span data-ttu-id="0f8ef-116">例</span><span class="sxs-lookup"><span data-stu-id="0f8ef-116">Examples</span></span>

<span data-ttu-id="0f8ef-117">次の例では、Picture.jpg の高さをピクセル単位で出力します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-117">The following example prints the height of Picture.jpg in pixels.</span></span>

```xpp
Image img = new  Image(); 
img.loadFile(@'C:\MyPictures\Picture.jpg'); 
print img.height(); 
pause;
```

## <a name="methods"></a><span data-ttu-id="0f8ef-118">メソッド</span><span class="sxs-lookup"><span data-stu-id="0f8ef-118">Methods</span></span>

| <span data-ttu-id="0f8ef-119">方法</span><span class="sxs-lookup"><span data-stu-id="0f8ef-119">Method</span></span>                                                                                                      | <span data-ttu-id="0f8ef-120">説明</span><span class="sxs-lookup"><span data-stu-id="0f8ef-120">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8ef-121">public int captureScreen(int left, int top, int right, int bottom)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-121">public int captureScreen(int left, int top, int right, int bottom)</span></span>                                          | <span data-ttu-id="0f8ef-122">パラメータ リストで指定された座標を使用して、スクリーンからイメージをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-122">Captures an image from the screen by using the coordinates that are supplied in the parameter list.</span></span>                                           |
| <span data-ttu-id="0f8ef-123">public int captureWindow(int hWnd)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-123">public int captureWindow(int hWnd)</span></span>                                                                          | <span data-ttu-id="0f8ef-124">パラメータとして指定されたハンドルを使用して、ウィンドウをイメージとしてキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-124">Captures a window as an image, using the handle that is supplied as a parameter.</span></span>                                                              |
| <span data-ttu-id="0f8ef-125">public int clipboardCopy()</span><span class="sxs-lookup"><span data-stu-id="0f8ef-125">public int clipboardCopy()</span></span>                                                                                  | <span data-ttu-id="0f8ef-126">イメージをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-126">Copies an image to the clipboard.</span></span>                                                                                                             |
| <span data-ttu-id="0f8ef-127">public int clipboardPaste()</span><span class="sxs-lookup"><span data-stu-id="0f8ef-127">public int clipboardPaste()</span></span>                                                                                 | <span data-ttu-id="0f8ef-128">システムのクリップボードの内容で既存のイメージを上書きします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-128">Overwrites an existing image with the content of the system clipboard.</span></span>                                                                        |
| <span data-ttu-id="0f8ef-129">public int copyImage(Image image)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-129">public int copyImage(Image image)</span></span>                                                                           | <span data-ttu-id="0f8ef-130">現在のイメージ オブジェクトをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-130">Copies the current image object.</span></span>                                                                                                              |
| <span data-ttu-id="0f8ef-131">public int createImage(int Width, int Height, int BitsPerPixel)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-131">public int createImage(int Width, int Height, int BitsPerPixel)</span></span>                                             | <span data-ttu-id="0f8ef-132">パラメーターで指定された幅、高さ、および色深度を持つ空のビットマップ画像を作成します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-132">Creates an empty bitmap image with the width, height, and color depth as specified by the parameters.</span></span>                                         |
| <span data-ttu-id="0f8ef-133">public int crop(int x, int y, int w, int h)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-133">public int crop(int x, int y, int w, int h)</span></span>                                                                 | <span data-ttu-id="0f8ef-134">画像をトリミングします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-134">Crops the image.</span></span>                                                                                                                              |
| <span data-ttu-id="0f8ef-135">public int displayImage(Int64 HDC, \[int Mode\], \[int Xpos\], \[int Ypos\], \[int Width\], \[int Height\])</span><span class="sxs-lookup"><span data-stu-id="0f8ef-135">public int displayImage(Int64 HDC, \[int Mode\], \[int Xpos\], \[int Ypos\], \[int Width\], \[int Height\])</span></span> | <span data-ttu-id="0f8ef-136">HDC パラメーターで指定されたデバイス コンテキストに画像を描画します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-136">Draws an image with the device context specified by the HDC parameter.</span></span>                                                                        |
| <span data-ttu-id="0f8ef-137">public Int64 exportBitmap()</span><span class="sxs-lookup"><span data-stu-id="0f8ef-137">public Int64 exportBitmap()</span></span>                                                                                 | <span data-ttu-id="0f8ef-138">画像のハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-138">Gets a handle for the image.</span></span>                                                                                                                  |
| <span data-ttu-id="0f8ef-139">public int flip(FlipType FlipType)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-139">public int flip(FlipType FlipType)</span></span>                                                                          | <span data-ttu-id="0f8ef-140">画像を垂直または水平方向に 180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-140">Rotates the image 180 degrees in a vertical or horizontal direction.</span></span>                                                                          |
| <span data-ttu-id="0f8ef-141">public container getImageDimensionUnits()</span><span class="sxs-lookup"><span data-stu-id="0f8ef-141">public container getImageDimensionUnits()</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="0f8ef-142">public int getPixel(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-142">public int getPixel(int x, int y)</span></span>                                                                           | <span data-ttu-id="0f8ef-143">パラメーターで指定されたポイントで、ピクセルの ARGB カラーの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-143">Retrieves the ARGB color value of the pixel at the point that is specified by the parameters.</span></span>                                                 |
| <span data-ttu-id="0f8ef-144">public int height()</span><span class="sxs-lookup"><span data-stu-id="0f8ef-144">public int height()</span></span>                                                                                         | <span data-ttu-id="0f8ef-145">ピクセル単位の画像の高さを取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-145">Retrieves the height of the image in pixels.</span></span>                                                                                                  |
| <span data-ttu-id="0f8ef-146">public container imageInfo()</span><span class="sxs-lookup"><span data-stu-id="0f8ef-146">public container imageInfo()</span></span>                                                                                | <span data-ttu-id="0f8ef-147">画像の幅、高さ、色深度を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-147">Retrieves the width, height, and color depth of the image.</span></span>                                                                                    |
| <span data-ttu-id="0f8ef-148">public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-148">public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)</span></span>                           | <span data-ttu-id="0f8ef-149">センター座標 x および y で半径により定義された円内のスポットライト効果を生成します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-149">Produces a spotlight effect within the circle that is defined by radius with center coordinates x and y.</span></span>                                      |
| <span data-ttu-id="0f8ef-150">public int importBitmap(Int64 hBitmap)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-150">public int importBitmap(Int64 hBitmap)</span></span>                                                                      | <span data-ttu-id="0f8ef-151">hBitmap パラメータで指定されたイメージからビットマップをクローンします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-151">Clones a bitmap from the image that is specified by the hBitmap parameter.</span></span>                                                                    |
| <span data-ttu-id="0f8ef-152">public int importFileIcon(str fileName)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-152">public int importFileIcon(str fileName)</span></span>                                                                     | <span data-ttu-id="0f8ef-153">ファイルに使用されているアイコンをコピーすることにより、fileName パラメーターで指定されたファイルからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-153">Creates an icon from the file specified by the fileName parameter by copying the icon that is used for the file.</span></span>                              |
| <span data-ttu-id="0f8ef-154">public int importIcon(str fileName, int iconIdx)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-154">public int importIcon(str fileName, int iconIdx)</span></span>                                                            | <span data-ttu-id="0f8ef-155">実行可能ファイルからアイコンへのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-155">Retrieves a handle to an icon from an executable file.</span></span> <span data-ttu-id="0f8ef-156">このアイコンは、fileName および iconIdx パラメーターで指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-156">The icon is specified by the fileName and iconIdx parameters.</span></span> |
| <span data-ttu-id="0f8ef-157">public int loadImage(str fileName)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-157">public int loadImage(str fileName)</span></span>                                                                          | <span data-ttu-id="0f8ef-158">fileName パラメーターで指定されたファイルからイメージを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-158">Loads an image from the file specified by the fileName parameter.</span></span>                                                                             |
| <span data-ttu-id="0f8ef-159">public int loadResource(int id)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-159">public int loadResource(int id)</span></span>                                                                             | <span data-ttu-id="0f8ef-160">Ax32.exe からリソースを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-160">Loads a resource from Ax32.exe.</span></span>                                                                                                               |
| <span data-ttu-id="0f8ef-161">public int promoteColor(int noOfColorBits)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-161">public int promoteColor(int noOfColorBits)</span></span>                                                                  | <span data-ttu-id="0f8ef-162">画像の色深度を向上させます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-162">Increases the color depth of the image.</span></span>                                                                                                       |
| <span data-ttu-id="0f8ef-163">public int reduceColorOctree(int maxColors)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-163">public int reduceColorOctree(int maxColors)</span></span>                                                                 | <span data-ttu-id="0f8ef-164">画像の色深度を減少させます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-164">Reduces the color depth of an image.</span></span>                                                                                                          |
| <span data-ttu-id="0f8ef-165">public int removeImage()</span><span class="sxs-lookup"><span data-stu-id="0f8ef-165">public int removeImage()</span></span>                                                                                    | <span data-ttu-id="0f8ef-166">画像に関するデータを削除します。オブジェクトはまだ存在しますが、データを持ちません。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-166">Removes the data about an image; the object still exists, but has no data.</span></span>                                                                    |
| <span data-ttu-id="0f8ef-167">public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-167">public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)</span></span>                         | <span data-ttu-id="0f8ef-168">newWidth および newHeight パラメーターにより指定されたサイズに画像をサイズ変更します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-168">Resizes the image to the size that is specified by the newWidth and newHeight parameters.</span></span>                                                     |
| <span data-ttu-id="0f8ef-169">public int rotate(RotateType RotateType)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-169">public int rotate(RotateType RotateType)</span></span>                                                                    | <span data-ttu-id="0f8ef-170">画像を回転します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-170">Rotates the image.</span></span>                                                                                                                            |
| <span data-ttu-id="0f8ef-171">public int saveImage(str fileName, \[ImageSaveType Type\])</span><span class="sxs-lookup"><span data-stu-id="0f8ef-171">public int saveImage(str fileName, \[ImageSaveType Type\])</span></span>                                                  | <span data-ttu-id="0f8ef-172">指定されたファイル名に画像を保存します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-172">Saves the image to the specified file name.</span></span>                                                                                                   |
| <span data-ttu-id="0f8ef-173">public ImageSaveType saveType(\[ImageSaveType Type\])</span><span class="sxs-lookup"><span data-stu-id="0f8ef-173">public ImageSaveType saveType(\[ImageSaveType Type\])</span></span>                                                       | <span data-ttu-id="0f8ef-174">イメージ デコーダを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-174">Gets or sets the image decoder.</span></span>                                                                                                               |
| <span data-ttu-id="0f8ef-175">public int setPixel(int x, int y, int pixel)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-175">public int setPixel(int x, int y, int pixel)</span></span>                                                                | <span data-ttu-id="0f8ef-176">x と y パラメーターで指定されているピクセルの色を設定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-176">Sets the color for the pixel that is specified by the x and y parameters.</span></span>                                                                     |
| <span data-ttu-id="0f8ef-177">public int transparent(\[boolean Set\], \[int RValue\], \[int GValue\], \[int BValue\])</span><span class="sxs-lookup"><span data-stu-id="0f8ef-177">public int transparent(\[boolean Set\], \[int RValue\], \[int GValue\], \[int BValue\])</span></span>                     | <span data-ttu-id="0f8ef-178">画像の透明な色を設定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-178">Sets the transparent color for the image.</span></span>                                                                                                     |
| <span data-ttu-id="0f8ef-179">public int width()</span><span class="sxs-lookup"><span data-stu-id="0f8ef-179">public int width()</span></span>                                                                                          | <span data-ttu-id="0f8ef-180">ピクセル単位の画像の幅を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-180">Retrieves the width of the image in pixels.</span></span>                                                                                                   |
| <span data-ttu-id="0f8ef-181">::public static int canLoad(str filename)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-181">::public static int canLoad(str filename)</span></span>                                                                   | <span data-ttu-id="0f8ef-182">画像ファイルが存在し、開くことができるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-182">Determines whether an image file exists and can be opened.</span></span>                                                                                    |
| <span data-ttu-id="0f8ef-183">::public static container loadExt(int idx)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-183">::public static container loadExt(int idx)</span></span>                                                                  | <span data-ttu-id="0f8ef-184">Image クラスでサポートされているファイル形式の拡張機能の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-184">Retrieves a list of the extensions of the file formats that are supported by the Image class.</span></span>                                                 |
| <span data-ttu-id="0f8ef-185">::public static int resourceType(int resourceIdx)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-185">::public static int resourceType(int resourceIdx)</span></span>                                                           | <span data-ttu-id="0f8ef-186">特定のリソースがビットマップかアイコンかを判別します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-186">Determines whether a particular resource is a bitmap or an icon.</span></span>                                                                              |
| <span data-ttu-id="0f8ef-187">::public static int rgb(int R, int G, int B)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-187">::public static int rgb(int R, int G, int B)</span></span>                                                                | <span data-ttu-id="0f8ef-188">RGB 値を ARGB 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-188">Converts an RGB value to an ARGB value.</span></span>                                                                                                       |
| <span data-ttu-id="0f8ef-189">::public static int validResource(int id)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-189">::public static int validResource(int id)</span></span>                                                                   | <span data-ttu-id="0f8ef-190">id パラメータで指定されたリソースが有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-190">Determines whether the resource specified by the id parameter is valid.</span></span>                                                                       |
| <span data-ttu-id="0f8ef-191">public void new(\[AnyType image\], \[int width\], \[int height\])</span><span class="sxs-lookup"><span data-stu-id="0f8ef-191">public void new(\[AnyType image\], \[int width\], \[int height\])</span></span>                                           | <span data-ttu-id="0f8ef-192">新しい画像を作成します</span><span class="sxs-lookup"><span data-stu-id="0f8ef-192">Creates a new image.</span></span>                                                                                                                          |
| <span data-ttu-id="0f8ef-193">public void displayOrign(int Xpos, int Ypos)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-193">public void displayOrign(int Xpos, int Ypos)</span></span>                                                                | <span data-ttu-id="0f8ef-194">オリジナルの発注元 (0, 0) から、オフセット (X, Y) を指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-194">Enables you to specify an offset (X, Y) from the original origin (0, 0).</span></span>                                                                      |
| <span data-ttu-id="0f8ef-195">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="0f8ef-195">public void finalize()</span></span>                                                                                      |                                                                                                                                               |

## <a name="method-capturescreen"></a><span data-ttu-id="0f8ef-196">メソッド captureScreen</span><span class="sxs-lookup"><span data-stu-id="0f8ef-196">Method captureScreen</span></span>

<span data-ttu-id="0f8ef-197">パラメータ リストで指定された座標を使用して、スクリーンからイメージをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-197">Captures an image from the screen by using the coordinates that are supplied in the parameter list.</span></span>

```xpp
public int captureScreen(int left, int top, int right, int bottom)
```

### <a name="parameters---capturescreen"></a><span data-ttu-id="0f8ef-198">パラメーター - captureScreen</span><span class="sxs-lookup"><span data-stu-id="0f8ef-198">Parameters - captureScreen</span></span>

<span data-ttu-id="0f8ef-199">left</span><span class="sxs-lookup"><span data-stu-id="0f8ef-199">left</span></span>  
<span data-ttu-id="0f8ef-200">キャプチャする画面の右下隅部分の Y 座標です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-200">Y coordinate of the lower-right corner of the part of the screen that you want to capture.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-201">戻る</span><span class="sxs-lookup"><span data-stu-id="0f8ef-201">top</span></span>  
<span data-ttu-id="0f8ef-202">キャプチャする画面の右下隅部分の Y 座標です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-202">Y coordinate of the lower-right corner of the part of the screen that you want to capture.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-203">権限</span><span class="sxs-lookup"><span data-stu-id="0f8ef-203">right</span></span>  
<span data-ttu-id="0f8ef-204">キャプチャする画面の右下隅部分の Y 座標です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-204">Y coordinate of the lower-right corner of the part of the screen that you want to capture.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-205">bottom</span><span class="sxs-lookup"><span data-stu-id="0f8ef-205">bottom</span></span>  
<span data-ttu-id="0f8ef-206">キャプチャする画面の右下隅部分の Y 座標です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-206">Y coordinate of the lower-right corner of the part of the screen that you want to capture.</span></span>

### <a name="return-value---capturescreen"></a><span data-ttu-id="0f8ef-207">戻り値 - captureScreen</span><span class="sxs-lookup"><span data-stu-id="0f8ef-207">Return Value - captureScreen</span></span>

<span data-ttu-id="0f8ef-208">0 は、成功を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-208">0 indicates success.</span></span> <span data-ttu-id="0f8ef-209">その他の値はエラーを示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-209">Other values indicate failure.</span></span>

### <a name="examples---capturescreen"></a><span data-ttu-id="0f8ef-210">例 - captureScreen</span><span class="sxs-lookup"><span data-stu-id="0f8ef-210">Examples - captureScreen</span></span>

<span data-ttu-id="0f8ef-211">次の例では、画面の一部をキャプチャし、test.bmp という名前のファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-211">The following example captures a part of the screen and saves it to a file that is named test.bmp.</span></span>

```xpp
Image img = new Image(); 
img.captureScreen(0, 0, 100, 100); 
img.saveFile(@'C:\test.bmp');
```

## <a name="method-capturewindow"></a><span data-ttu-id="0f8ef-212">メソッド captureWindow</span><span class="sxs-lookup"><span data-stu-id="0f8ef-212">Method captureWindow</span></span>

<span data-ttu-id="0f8ef-213">パラメータとして指定されたハンドルを使用して、ウィンドウをイメージとしてキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-213">Captures a window as an image, using the handle that is supplied as a parameter.</span></span>

```xpp
public int captureWindow(int hWnd)
```

### <a name="parameters---capturewindow"></a><span data-ttu-id="0f8ef-214">パラメーター - captureWindow</span><span class="sxs-lookup"><span data-stu-id="0f8ef-214">Parameters - captureWindow</span></span>

<span data-ttu-id="0f8ef-215">hWnd</span><span class="sxs-lookup"><span data-stu-id="0f8ef-215">hWnd</span></span>  
<span data-ttu-id="0f8ef-216">キャプチャするウィンドウのハンドル。整数として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-216">The handle to the window that you want to capture which must be supplied as an integer.</span></span>

### <a name="return-value---capturewindow"></a><span data-ttu-id="0f8ef-217">戻り値 - captureWindow</span><span class="sxs-lookup"><span data-stu-id="0f8ef-217">Return Value - captureWindow</span></span>

<span data-ttu-id="0f8ef-218">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-218">0 indicates success; otherwise, failure.</span></span>

## <a name="method-clipboardcopy"></a><span data-ttu-id="0f8ef-219">メソッド clipboardCopy</span><span class="sxs-lookup"><span data-stu-id="0f8ef-219">Method clipboardCopy</span></span>

<span data-ttu-id="0f8ef-220">イメージをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-220">Copies an image to the clipboard.</span></span>

```xpp
public int clipboardCopy()
```

### <a name="return-value---clipboardcopy"></a><span data-ttu-id="0f8ef-221">戻り値 - clipboardCopy</span><span class="sxs-lookup"><span data-stu-id="0f8ef-221">Return Value - clipboardCopy</span></span>

<span data-ttu-id="0f8ef-222">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-222">0 indicates success; otherwise, failure.</span></span>

### <a name="examples---clipboardcopy"></a><span data-ttu-id="0f8ef-223">例 - clipboardCopy</span><span class="sxs-lookup"><span data-stu-id="0f8ef-223">Examples - clipboardCopy</span></span>

<span data-ttu-id="0f8ef-224">次の例では、Test.bmp という名前のファイルからコンテンツをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-224">The following example copies the content from a file that is named Test.bmp.</span></span>

```xpp
Image img = new Image(); 
img.loadFile(@'C:\Test.bmp'); 
img.clipboardCopy(); 
// Image can now be pasted into an application.
```

## <a name="method-clipboardpaste"></a><span data-ttu-id="0f8ef-225">メソッド clipboardPaste</span><span class="sxs-lookup"><span data-stu-id="0f8ef-225">Method clipboardPaste</span></span>

<span data-ttu-id="0f8ef-226">システムのクリップボードの内容で既存のイメージを上書きします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-226">Overwrites an existing image with the content of the system clipboard.</span></span>

```xpp
public int clipboardPaste()
```

### <a name="return-value---clipboardpaste"></a><span data-ttu-id="0f8ef-227">戻り値 - clipboardPaste</span><span class="sxs-lookup"><span data-stu-id="0f8ef-227">Return Value - clipboardPaste</span></span>

<span data-ttu-id="0f8ef-228">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-228">0 indicates success; otherwise, failure.</span></span>

### <a name="remarks---clipboardpaste"></a><span data-ttu-id="0f8ef-229">備考 - clipboardPaste</span><span class="sxs-lookup"><span data-stu-id="0f8ef-229">Remarks - clipboardPaste</span></span>

<span data-ttu-id="0f8ef-230">正常に使用されるメソッドについては、クリップボードにコンテンツが必要です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-230">For the method to be used successfully, the clipboard must have content.</span></span>

### <a name="examples---clipboardpaste"></a><span data-ttu-id="0f8ef-231">例 - clipboardPaste</span><span class="sxs-lookup"><span data-stu-id="0f8ef-231">Examples - clipboardPaste</span></span>

<span data-ttu-id="0f8ef-232">次の例では、以前にクリップボードにコピーされたコンテンツを使用して新しいイメージ ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-232">The following example creates a new image file by using contents previously copied to the clipboard.</span></span>

```xpp
Image img = new Image();
// Copy an image to the clipboard before this test 
img.clipboardPaste(); 
img.saveFile(@'C:\test.jpg');
```

## <a name="method-copyimage"></a><span data-ttu-id="0f8ef-233">メソッド copyImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-233">Method copyImage</span></span>

<span data-ttu-id="0f8ef-234">現在のイメージ オブジェクトをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-234">Copies the current image object.</span></span>

```xpp
public int copyImage(Image image)
```

### <a name="parameters---copyimage"></a><span data-ttu-id="0f8ef-235">パラメーター - copyImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-235">Parameters - copyImage</span></span>

<span data-ttu-id="0f8ef-236">画像</span><span class="sxs-lookup"><span data-stu-id="0f8ef-236">image</span></span>  
<span data-ttu-id="0f8ef-237">コピーする画像。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-237">The image to be copied.</span></span>

### <a name="return-value---copyimage"></a><span data-ttu-id="0f8ef-238">戻り値 - copyImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-238">Return Value - copyImage</span></span>

<span data-ttu-id="0f8ef-239">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-239">0 indicates success; otherwise, failure.</span></span>

### <a name="examples---copyimage"></a><span data-ttu-id="0f8ef-240">例 - copyImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-240">Examples - copyImage</span></span>

<span data-ttu-id="0f8ef-241">次の例では、2 つの新しいイメージを作成し、1 つのイメージの内容をもう一方のイメージの内容で上書きします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-241">The following example creates two new images and then overwrites the contents of one image with the contents of the other.</span></span>

```xpp
Image img =  new Image(); 
Image img2 = new Image(); 
img.loadFile(@'C:\test.bmp'); 
img2.loadFile(@'C:\test2.bmp'); 
img2.copyImage(img); //img2 now the same as img
```

## <a name="method-createimage"></a><span data-ttu-id="0f8ef-242">メソッド createImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-242">Method createImage</span></span>

<span data-ttu-id="0f8ef-243">パラメーターで指定された幅、高さ、および色深度を持つ空のビットマップ画像を作成します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-243">Creates an empty bitmap image with the width, height, and color depth as specified by the parameters.</span></span>

```xpp
public int createImage(int Width, int Height, int BitsPerPixel)
```

### <a name="parameters---createimage"></a><span data-ttu-id="0f8ef-244">パラメーター - createImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-244">Parameters - createImage</span></span>

<span data-ttu-id="0f8ef-245">Width</span><span class="sxs-lookup"><span data-stu-id="0f8ef-245">Width</span></span>  
<span data-ttu-id="0f8ef-246">画像の色深度。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-246">The color depth of the image.</span></span> <span data-ttu-id="0f8ef-247">有効値は 1、4、8、16、24、32 です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-247">Possible values are 1, 4, 8, 16, 24, and 32.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-248">高さ</span><span class="sxs-lookup"><span data-stu-id="0f8ef-248">Height</span></span>  
<span data-ttu-id="0f8ef-249">画像の色深度。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-249">The color depth of the image.</span></span> <span data-ttu-id="0f8ef-250">有効値は 1、4、8、16、24、32 です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-250">Possible values are 1, 4, 8, 16, 24, and 32.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-251">BitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="0f8ef-251">BitsPerPixel</span></span>  
<span data-ttu-id="0f8ef-252">画像の色深度。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-252">The color depth of the image.</span></span> <span data-ttu-id="0f8ef-253">有効値は 1、4、8、16、24、32 です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-253">Possible values are 1, 4, 8, 16, 24, and 32.</span></span>

### <a name="return-value---createimage"></a><span data-ttu-id="0f8ef-254">戻り値 - createImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-254">Return Value - createImage</span></span>

<span data-ttu-id="0f8ef-255">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-255">0 indicates success; otherwise, failure.</span></span>

### <a name="examples---createimage"></a><span data-ttu-id="0f8ef-256">例 - createImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-256">Examples - createImage</span></span>

<span data-ttu-id="0f8ef-257">次の例では、高さと幅が 16 ピクセル、色深度がピクセルあたり 32 ビットのイメージを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-257">The following example creates an image with a height and width of 16 pixels, and a color depth of 32 bits per pixel.</span></span>

```xpp
int i;
int j;
Image image;
image.createImage(
    Imagelist::smallIconWidth(),
    Imagelist::smallIconHeight(),
    32);
for (i=0; i < Imagelist::smallIconWidth(); i++)
{
    for (j=0; j < Imagelist::smallIconHeight(); j++)
    {
        if (i >= Imagelist::smallIconWidth()-2)
        {
            image.setPixel(i, j, WinAPI::RGB2int(0, 255, 255));
        }
        else
        {
            image.setPixel(i, j, WinAPI::imageTransparentColor());
        }
    }
}
```

## <a name="method-crop"></a><span data-ttu-id="0f8ef-258">メソッド crop</span><span class="sxs-lookup"><span data-stu-id="0f8ef-258">Method crop</span></span>

<span data-ttu-id="0f8ef-259">画像をトリミングします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-259">Crops the image.</span></span>

```xpp
public int crop(int x, int y, int w, int h)
```

### <a name="parameters---crop"></a><span data-ttu-id="0f8ef-260">パラメーター - crop</span><span class="sxs-lookup"><span data-stu-id="0f8ef-260">Parameters - crop</span></span>

<span data-ttu-id="0f8ef-261">x</span><span class="sxs-lookup"><span data-stu-id="0f8ef-261">x</span></span>  
<span data-ttu-id="0f8ef-262">点 (x、y) からトリミングする領域の高さ。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-262">The height of the region that you want to crop from the point (x, y).</span></span>

<!-- -->

<span data-ttu-id="0f8ef-263">y</span><span class="sxs-lookup"><span data-stu-id="0f8ef-263">y</span></span>  
<span data-ttu-id="0f8ef-264">点 (x、y) からトリミングする領域の高さ。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-264">The height of the region that you want to crop from the point (x, y).</span></span>

<!-- -->

<span data-ttu-id="0f8ef-265">w</span><span class="sxs-lookup"><span data-stu-id="0f8ef-265">w</span></span>  
<span data-ttu-id="0f8ef-266">点 (x、y) からトリミングする領域の高さ。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-266">The height of the region that you want to crop from the point (x, y).</span></span>

<!-- -->

<span data-ttu-id="0f8ef-267">h</span><span class="sxs-lookup"><span data-stu-id="0f8ef-267">h</span></span>  
<span data-ttu-id="0f8ef-268">点 (x、y) からトリミングする領域の高さ。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-268">The height of the region that you want to crop from the point (x, y).</span></span>

### <a name="return-value---crop"></a><span data-ttu-id="0f8ef-269">戻り値 - crop</span><span class="sxs-lookup"><span data-stu-id="0f8ef-269">Return Value - crop</span></span>

<span data-ttu-id="0f8ef-270">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-270">0 indicates success; otherwise, failure.</span></span>

## <a name="method-displayimage"></a><span data-ttu-id="0f8ef-271">メソッド displayImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-271">Method displayImage</span></span>

<span data-ttu-id="0f8ef-272">HDC パラメーターで指定されたデバイス コンテキストに画像を描画します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-272">Draws an image with the device context specified by the HDC parameter.</span></span>

```xpp
public int displayImage(Int64 HDC, [int Mode], [int Xpos], [int Ypos], [int Width], [int Height])
```

### <a name="parameters---displayimage"></a><span data-ttu-id="0f8ef-273">パラメーター - displayImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-273">Parameters - displayImage</span></span>

<span data-ttu-id="0f8ef-274">HDC</span><span class="sxs-lookup"><span data-stu-id="0f8ef-274">HDC</span></span>  
<span data-ttu-id="0f8ef-275">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-275">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-276">モード</span><span class="sxs-lookup"><span data-stu-id="0f8ef-276">Mode</span></span>  
<span data-ttu-id="0f8ef-277">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-277">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-278">Xpos</span><span class="sxs-lookup"><span data-stu-id="0f8ef-278">Xpos</span></span>  
<span data-ttu-id="0f8ef-279">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-279">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-280">Ypos</span><span class="sxs-lookup"><span data-stu-id="0f8ef-280">Ypos</span></span>  
<span data-ttu-id="0f8ef-281">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-281">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-282">幅</span><span class="sxs-lookup"><span data-stu-id="0f8ef-282">Width</span></span>  
<span data-ttu-id="0f8ef-283">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-283">Optional parameter.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-284">Height</span><span class="sxs-lookup"><span data-stu-id="0f8ef-284">Height</span></span>  
<span data-ttu-id="0f8ef-285">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-285">Optional parameter.</span></span>

### <a name="return-value---displayimage"></a><span data-ttu-id="0f8ef-286">戻り値 - displayImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-286">Return Value - displayImage</span></span>

<span data-ttu-id="0f8ef-287">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-287">0 indicates success; otherwise, failure.</span></span>

## <a name="method-exportbitmap"></a><span data-ttu-id="0f8ef-288">メソッド exportBitmap</span><span class="sxs-lookup"><span data-stu-id="0f8ef-288">Method exportBitmap</span></span>

<span data-ttu-id="0f8ef-289">画像のハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-289">Gets a handle for the image.</span></span>

```xpp
public Int64 exportBitmap()
```

### <a name="return-value---exportbitmap"></a><span data-ttu-id="0f8ef-290">戻り値 - exportBitmap</span><span class="sxs-lookup"><span data-stu-id="0f8ef-290">Return Value - exportBitmap</span></span>

<span data-ttu-id="0f8ef-291">画像のハンドル を表す整数。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-291">An integer that represents the handle for the image.</span></span>

### <a name="examples---exportbitmap"></a><span data-ttu-id="0f8ef-292">例 - exportBitmap</span><span class="sxs-lookup"><span data-stu-id="0f8ef-292">Examples - exportBitmap</span></span>

<span data-ttu-id="0f8ef-293">次の例では、イメージのハンドルを取得し、ハンドルを使用してイメージを複製します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-293">The following example retrieves the handle for an image and then uses the handle to clone the image.</span></span>

```xpp
{ 
    int hdlBitmap; 
    Image img = new Image(); 
    Image img2 = new Image(); 
    img.loadImage(@'C:\MyImage.bmp'); 
    //Set hdlBitmap to handle for MyImage.bmp 
    hdlBitmap = img.exportBitmap(); 
    //Load MyImage.bmp to img2 using image handle 
    if (hdlBitmap) 
    { 
        img2.importBitmap(hdlBitmap); 
    } 
}
```

## <a name="method-flip"></a><span data-ttu-id="0f8ef-294">メソッド flip</span><span class="sxs-lookup"><span data-stu-id="0f8ef-294">Method flip</span></span>

<span data-ttu-id="0f8ef-295">画像を垂直または水平方向に 180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-295">Rotates the image 180 degrees in a vertical or horizontal direction.</span></span>

```xpp
public int flip(FlipType FlipType)
```

### <a name="parameters---flip"></a><span data-ttu-id="0f8ef-296">パラメーター - flip</span><span class="sxs-lookup"><span data-stu-id="0f8ef-296">Parameters - flip</span></span>

<span data-ttu-id="0f8ef-297">FlipType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-297">FlipType</span></span>  
<span data-ttu-id="0f8ef-298">イメージを反転させる方法を決定する FlipType 列挙。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-298">A FlipType enumeration that determines the way in which the image is flipped.</span></span>

### <a name="return-value---flip"></a><span data-ttu-id="0f8ef-299">戻り値 - flip</span><span class="sxs-lookup"><span data-stu-id="0f8ef-299">Return Value - flip</span></span>

<span data-ttu-id="0f8ef-300">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-300">0 indicates success; otherwise, failure.</span></span>

### <a name="remarks---flip"></a><span data-ttu-id="0f8ef-301">備考 - flip</span><span class="sxs-lookup"><span data-stu-id="0f8ef-301">Remarks - flip</span></span>

<span data-ttu-id="0f8ef-302">FlipType パラメーターの使用可能な値は FlipType システム列挙で使用可能な次の値です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-302">The possible values for the FlipType parameter are those available in the FlipType system enum:</span></span>

|     |                    |                                                          |
|-----|--------------------|----------------------------------------------------------|
| <span data-ttu-id="0f8ef-303">0</span><span class="sxs-lookup"><span data-stu-id="0f8ef-303">0</span></span>   | <span data-ttu-id="0f8ef-304">RotateNoneFlipNone</span><span class="sxs-lookup"><span data-stu-id="0f8ef-304">RotateNoneFlipNone</span></span> | <span data-ttu-id="0f8ef-305">反転なし</span><span class="sxs-lookup"><span data-stu-id="0f8ef-305">No flip</span></span>                                                  |
| <span data-ttu-id="0f8ef-306">1</span><span class="sxs-lookup"><span data-stu-id="0f8ef-306">1</span></span>   | <span data-ttu-id="0f8ef-307">RotateNoneFlipX</span><span class="sxs-lookup"><span data-stu-id="0f8ef-307">RotateNoneFlipX</span></span>    | <span data-ttu-id="0f8ef-308">画像を水平方向に 180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-308">Rotates the image 180 degrees in a horizontal direction.</span></span> |
| <span data-ttu-id="0f8ef-309">2</span><span class="sxs-lookup"><span data-stu-id="0f8ef-309">2</span></span>   | <span data-ttu-id="0f8ef-310">RotateNoneFlipX</span><span class="sxs-lookup"><span data-stu-id="0f8ef-310">RotateNoneFlipY</span></span>    | <span data-ttu-id="0f8ef-311">画像を垂直方向に 180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-311">Rotates the image 180 degrees in a vertical direction.</span></span>   |

## <a name="method-getimagedimensionunits"></a><span data-ttu-id="0f8ef-312">メソッド getImageDimensionUnits</span><span class="sxs-lookup"><span data-stu-id="0f8ef-312">Method getImageDimensionUnits</span></span>

```xpp
public container getImageDimensionUnits()
```

### <a name="return-value---getimagedimensionunits"></a><span data-ttu-id="0f8ef-313">戻り値 - getImageDimensionUnits</span><span class="sxs-lookup"><span data-stu-id="0f8ef-313">Return Value - getImageDimensionUnits</span></span>

## <a name="method-getpixel"></a><span data-ttu-id="0f8ef-314">メソッド getPixel</span><span class="sxs-lookup"><span data-stu-id="0f8ef-314">Method getPixel</span></span>

<span data-ttu-id="0f8ef-315">パラメーターで指定されたポイントで、ピクセルの ARGB カラーの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-315">Retrieves the ARGB color value of the pixel at the point that is specified by the parameters.</span></span>

```xpp
public int getPixel(int x, int y)
```

### <a name="parameters---getpixel"></a><span data-ttu-id="0f8ef-316">パラメーター - getPixel</span><span class="sxs-lookup"><span data-stu-id="0f8ef-316">Parameters - getPixel</span></span>

<span data-ttu-id="0f8ef-317">x</span><span class="sxs-lookup"><span data-stu-id="0f8ef-317">x</span></span>  
<span data-ttu-id="0f8ef-318">ピクセルの垂直座標。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-318">The vertical coordinate of the pixel.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-319">y</span><span class="sxs-lookup"><span data-stu-id="0f8ef-319">y</span></span>  
<span data-ttu-id="0f8ef-320">ピクセルの垂直座標。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-320">The vertical coordinate of the pixel.</span></span>

### <a name="return-value---getpixel"></a><span data-ttu-id="0f8ef-321">戻り値 - getPixel</span><span class="sxs-lookup"><span data-stu-id="0f8ef-321">Return Value - getPixel</span></span>

<span data-ttu-id="0f8ef-322">ピクセルの ARGB 値である整数 (RGB カラーの 32 ビット表示) 。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-322">An integer that is the ARGB value of the pixel (a 32-bit representation of an RGB color).</span></span>

## <a name="method-height"></a><span data-ttu-id="0f8ef-323">メソッド height</span><span class="sxs-lookup"><span data-stu-id="0f8ef-323">Method height</span></span>

<span data-ttu-id="0f8ef-324">ピクセル単位の画像の高さを取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-324">Retrieves the height of the image in pixels.</span></span>

```xpp
public int height()
```

### <a name="return-value---height"></a><span data-ttu-id="0f8ef-325">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="0f8ef-325">Return Value - height</span></span>

<span data-ttu-id="0f8ef-326">画像の高さをピクセル単位で表す整数。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-326">An integer that represents the height of the image in pixels.</span></span>

### <a name="examples---height"></a><span data-ttu-id="0f8ef-327">例 - height</span><span class="sxs-lookup"><span data-stu-id="0f8ef-327">Examples - height</span></span>

<span data-ttu-id="0f8ef-328">次の例では、test.bmp に含まれるイメージの高さを出力します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-328">The following example prints out the height of the image that is contained in test.bmp.</span></span>

```xpp
Image img = new Image(); 
img.loadFile(@'C:\test.bmp'); 
print img.height(); 
pause;
```

## <a name="method-imageinfo"></a><span data-ttu-id="0f8ef-329">メソッド imageInfo</span><span class="sxs-lookup"><span data-stu-id="0f8ef-329">Method imageInfo</span></span>

<span data-ttu-id="0f8ef-330">画像の幅、高さ、色深度を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-330">Retrieves the width, height, and color depth of the image.</span></span>

```xpp
public container imageInfo()
```

### <a name="return-value---imageinfo"></a><span data-ttu-id="0f8ef-331">戻り値 - imageInfo</span><span class="sxs-lookup"><span data-stu-id="0f8ef-331">Return Value - imageInfo</span></span>

<span data-ttu-id="0f8ef-332">画像の幅、画像の高さ、およびピクセルあたりのビット数を指定する値を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-332">A container that holds values that specify the width of the image, the height of the image, and the number of bits per pixel.</span></span>

### <a name="examples---imageinfo"></a><span data-ttu-id="0f8ef-333">例 - imageInfo</span><span class="sxs-lookup"><span data-stu-id="0f8ef-333">Examples - imageInfo</span></span>

<span data-ttu-id="0f8ef-334">次の例では、イメージ test.bmp の幅と高さを出力し、ピクセルあたりのビット数で色深度を指定しています。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-334">The following example prints out the width and height of the image test.bmp, and specifies the color depth in bits per pixel.</span></span>

```xpp
Image img = new Image(); 
container c; 
img.loadFile(@'C:\Test.bmp'); 
c = img.imageInfo(); 
print con2str(c); 
pause;
```

## <a name="method-imagespotlight"></a><span data-ttu-id="0f8ef-335">メソッド imageSpotlight</span><span class="sxs-lookup"><span data-stu-id="0f8ef-335">Method imageSpotlight</span></span>

<span data-ttu-id="0f8ef-336">センター座標 x および y で半径により定義された円内のスポットライト効果を生成します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-336">Produces a spotlight effect within the circle that is defined by radius with center coordinates x and y.</span></span>

```xpp
public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)
```

### <a name="parameters---imagespotlight"></a><span data-ttu-id="0f8ef-337">パラメーター - imageSpotlight</span><span class="sxs-lookup"><span data-stu-id="0f8ef-337">Parameters - imageSpotlight</span></span>

<span data-ttu-id="0f8ef-338">x</span><span class="sxs-lookup"><span data-stu-id="0f8ef-338">x</span></span>  
<span data-ttu-id="0f8ef-339">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-339">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="0f8ef-340">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-340">The possible values are between 0 and 100 (%).</span></span>

<!-- -->

<span data-ttu-id="0f8ef-341">y</span><span class="sxs-lookup"><span data-stu-id="0f8ef-341">y</span></span>  
<span data-ttu-id="0f8ef-342">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-342">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="0f8ef-343">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-343">The possible values are between 0 and 100 (%).</span></span>

<!-- -->

<span data-ttu-id="0f8ef-344">radius</span><span class="sxs-lookup"><span data-stu-id="0f8ef-344">radius</span></span>  
<span data-ttu-id="0f8ef-345">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-345">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="0f8ef-346">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-346">The possible values are between 0 and 100 (%).</span></span>

<!-- -->

<span data-ttu-id="0f8ef-347">平滑化</span><span class="sxs-lookup"><span data-stu-id="0f8ef-347">smoothing</span></span>  
<span data-ttu-id="0f8ef-348">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-348">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="0f8ef-349">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-349">The possible values are between 0 and 100 (%).</span></span>

<!-- -->

<span data-ttu-id="0f8ef-350">intensity</span><span class="sxs-lookup"><span data-stu-id="0f8ef-350">intensity</span></span>  
<span data-ttu-id="0f8ef-351">周辺のピクセルの強度。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-351">The intensity of the surrounding pixels.</span></span> <span data-ttu-id="0f8ef-352">可能な値は 0 ～ 100 (%) までです。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-352">The possible values are between 0 and 100 (%).</span></span>

### <a name="return-value---imagespotlight"></a><span data-ttu-id="0f8ef-353">戻り値 - imageSpotlight</span><span class="sxs-lookup"><span data-stu-id="0f8ef-353">Return Value - imageSpotlight</span></span>

<span data-ttu-id="0f8ef-354">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-354">0 indicates success; otherwise, failure.</span></span>

### <a name="remarks---imagespotlight"></a><span data-ttu-id="0f8ef-355">備考 - imageSpotlight</span><span class="sxs-lookup"><span data-stu-id="0f8ef-355">Remarks - imageSpotlight</span></span>

<span data-ttu-id="0f8ef-356">円内のピクセルは変更されませんが、イメージ内の他のピクセルはその明度を減らすことで暗くなります。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-356">The pixels within the circle are unchanged, but the other pixels in the image are darkened by reducing their intensity.</span></span>

## <a name="method-importbitmap"></a><span data-ttu-id="0f8ef-357">メソッド importBitmap</span><span class="sxs-lookup"><span data-stu-id="0f8ef-357">Method importBitmap</span></span>

<span data-ttu-id="0f8ef-358">hBitmap パラメータで指定されたイメージからビットマップをクローンします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-358">Clones a bitmap from the image that is specified by the hBitmap parameter.</span></span>

```xpp
public int importBitmap(Int64 hBitmap)
```

### <a name="parameters---importbitmap"></a><span data-ttu-id="0f8ef-359">パラメーター - importBitmap</span><span class="sxs-lookup"><span data-stu-id="0f8ef-359">Parameters - importBitmap</span></span>

<span data-ttu-id="0f8ef-360">hBitmap</span><span class="sxs-lookup"><span data-stu-id="0f8ef-360">hBitmap</span></span>  
<span data-ttu-id="0f8ef-361">複製する画像のハンドルです。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-361">The handle to the image that you clone.</span></span>

### <a name="return-value---importbitmap"></a><span data-ttu-id="0f8ef-362">戻り値 - importBitmap</span><span class="sxs-lookup"><span data-stu-id="0f8ef-362">Return Value - importBitmap</span></span>

<span data-ttu-id="0f8ef-363">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-363">0 indicates success; otherwise, failure.</span></span>

### <a name="examples---importbitmap"></a><span data-ttu-id="0f8ef-364">例 - importBitmap</span><span class="sxs-lookup"><span data-stu-id="0f8ef-364">Examples - importBitmap</span></span>

<span data-ttu-id="0f8ef-365">次の例では、イメージのハンドルを取得してから、importBitmap メソッドを使用してイメージを複製します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-365">The following example retrieves the handle for an image and then uses the importBitmap method to clone the image.</span></span>

```xpp
{ 
    int hdlBitmap; 
    Image img = new Image(); 
    Image img2 = new Image(); 
    img.loadImage(@'C:\MyImage.bmp'); 
    //Set hdlBitmap to handle for MyImage.bmp 
    hdlBitmap = img.exportBitmap(); 
    //Load MyImage.bmp to img2 using image handle 
    if (hdlBitmap) 
    { 
        img2.importBitmap(hdlBitmap); 
    } 
}
```

## <a name="method-importfileicon"></a><span data-ttu-id="0f8ef-366">メソッド importFileIcon</span><span class="sxs-lookup"><span data-stu-id="0f8ef-366">Method importFileIcon</span></span>

<span data-ttu-id="0f8ef-367">ファイルに使用されているアイコンをコピーすることにより、fileName パラメーターで指定されたファイルからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-367">Creates an icon from the file specified by the fileName parameter by copying the icon that is used for the file.</span></span>

```xpp
public int importFileIcon(str fileName)
```

### <a name="parameters---importfileicon"></a><span data-ttu-id="0f8ef-368">パラメーター - importFileIcon</span><span class="sxs-lookup"><span data-stu-id="0f8ef-368">Parameters - importFileIcon</span></span>

<span data-ttu-id="0f8ef-369">fileName</span><span class="sxs-lookup"><span data-stu-id="0f8ef-369">fileName</span></span>  
<span data-ttu-id="0f8ef-370">アイコンを作成するファイルの名前とパス。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-370">The name and the path of the file from which you create an icon.</span></span>

### <a name="return-value---importfileicon"></a><span data-ttu-id="0f8ef-371">戻り値 - importFileIcon</span><span class="sxs-lookup"><span data-stu-id="0f8ef-371">Return Value - importFileIcon</span></span>

<span data-ttu-id="0f8ef-372">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-372">0 indicates success; otherwise, failure.</span></span>

### <a name="examples---importfileicon"></a><span data-ttu-id="0f8ef-373">例 - importFileIcon</span><span class="sxs-lookup"><span data-stu-id="0f8ef-373">Examples - importFileIcon</span></span>

<span data-ttu-id="0f8ef-374">次の例では、ファイル test.bmp に使用されているアイコンをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-374">The following example copies the icon that is used for the file test.bmp.</span></span>

```xpp
Image img = new Image(); 
img.importFileIcon(@'C:\test.bmp'); 
img.clipboardCopy(); 
// Icon used for test.bmp can now be pasted into an application.
```

## <a name="method-importicon"></a><span data-ttu-id="0f8ef-375">メソッド importIcon</span><span class="sxs-lookup"><span data-stu-id="0f8ef-375">Method importIcon</span></span>

<span data-ttu-id="0f8ef-376">実行可能ファイルからアイコンへのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-376">Retrieves a handle to an icon from an executable file.</span></span> <span data-ttu-id="0f8ef-377">このアイコンは、fileName および iconIdx パラメーターで指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-377">The icon is specified by the fileName and iconIdx parameters.</span></span>

```xpp
public int importIcon(str fileName, int iconIdx)
```

### <a name="parameters---importicon"></a><span data-ttu-id="0f8ef-378">パラメーター - importIcon</span><span class="sxs-lookup"><span data-stu-id="0f8ef-378">Parameters - importIcon</span></span>

<span data-ttu-id="0f8ef-379">fileName</span><span class="sxs-lookup"><span data-stu-id="0f8ef-379">fileName</span></span>  
<span data-ttu-id="0f8ef-380">指定したファイル内のリソース。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-380">The resource within the specified file.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-381">iconIdx</span><span class="sxs-lookup"><span data-stu-id="0f8ef-381">iconIdx</span></span>  
<span data-ttu-id="0f8ef-382">指定したファイル内のリソース。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-382">The resource within the specified file.</span></span>

### <a name="return-value---importicon"></a><span data-ttu-id="0f8ef-383">戻り値 - importIcon</span><span class="sxs-lookup"><span data-stu-id="0f8ef-383">Return Value - importIcon</span></span>

<span data-ttu-id="0f8ef-384">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-384">0 indicates success; otherwise, failure.</span></span>

## <a name="method-loadimage"></a><span data-ttu-id="0f8ef-385">メソッド loadImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-385">Method loadImage</span></span>

<span data-ttu-id="0f8ef-386">fileName パラメーターで指定されたファイルからイメージを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-386">Loads an image from the file specified by the fileName parameter.</span></span>

```xpp
public int loadImage(str fileName)
```

### <a name="parameters---loadimage"></a><span data-ttu-id="0f8ef-387">パラメーター - loadImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-387">Parameters - loadImage</span></span>

<span data-ttu-id="0f8ef-388">fileName</span><span class="sxs-lookup"><span data-stu-id="0f8ef-388">fileName</span></span>  
<span data-ttu-id="0f8ef-389">画像を読み込む元となるリソース。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-389">The resource from which you want to load the image.</span></span>

### <a name="return-value---loadimage"></a><span data-ttu-id="0f8ef-390">戻り値 - loadImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-390">Return Value - loadImage</span></span>

<span data-ttu-id="0f8ef-391">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-391">0 indicates success; otherwise, failure.</span></span>

## <a name="method-loadresource"></a><span data-ttu-id="0f8ef-392">メソッド loadResource</span><span class="sxs-lookup"><span data-stu-id="0f8ef-392">Method loadResource</span></span>

<span data-ttu-id="0f8ef-393">パラメーター - validResource</span><span class="sxs-lookup"><span data-stu-id="0f8ef-393">Loads a resource from Ax32.exe.</span></span>

```xpp
public int loadResource(int id)
```

### <a name="parameters---loadresource"></a><span data-ttu-id="0f8ef-394">パラメーター - loadResource</span><span class="sxs-lookup"><span data-stu-id="0f8ef-394">Parameters - loadResource</span></span>

<span data-ttu-id="0f8ef-395">id</span><span class="sxs-lookup"><span data-stu-id="0f8ef-395">id</span></span>  
<span data-ttu-id="0f8ef-396">読み込むリソースの ID。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-396">The ID of the resource that you want to load.</span></span> <span data-ttu-id="0f8ef-397">リソースの値は、Resources マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-397">Values of resources can be found in the Resources macro.</span></span>

### <a name="return-value---loadresource"></a><span data-ttu-id="0f8ef-398">戻り値 - loadResource</span><span class="sxs-lookup"><span data-stu-id="0f8ef-398">Return Value - loadResource</span></span>

<span data-ttu-id="0f8ef-399">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-399">0 indicates success; otherwise, failure.</span></span>

### <a name="examples---loadresource"></a><span data-ttu-id="0f8ef-400">例 - loadResource</span><span class="sxs-lookup"><span data-stu-id="0f8ef-400">Examples - loadResource</span></span>

<span data-ttu-id="0f8ef-401">次の例では、イメージ リストに 2つ のリソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-401">The following example adds two resources to an image list.</span></span>

```xpp
Resource 
Image img; 
ImageList imageList; 
imageList = new Imagelist( 
    Imagelist::smallIconWidth(), 
    Imagelist::smallIconHeight()); 
img = new Image(); 
img.loadResource(#RES_NODE_CLOSED); 
imageList.add(img); 
img = new Image(); 
img.loadResource(#RES_NODE_OPEN); 
imageList.add(img);
```

## <a name="method-promotecolor"></a><span data-ttu-id="0f8ef-402">メソッド promoteColor</span><span class="sxs-lookup"><span data-stu-id="0f8ef-402">Method promoteColor</span></span>

<span data-ttu-id="0f8ef-403">画像の色深度を向上させます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-403">Increases the color depth of the image.</span></span>

```xpp
public int promoteColor(int noOfColorBits)
```

### <a name="parameters---promotecolor"></a><span data-ttu-id="0f8ef-404">パラメーター - promoteColor</span><span class="sxs-lookup"><span data-stu-id="0f8ef-404">Parameters - promoteColor</span></span>

<span data-ttu-id="0f8ef-405">noOfColorBits</span><span class="sxs-lookup"><span data-stu-id="0f8ef-405">noOfColorBits</span></span>  
<span data-ttu-id="0f8ef-406">イメージのレベルを上げるビット数。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-406">The number of bits that you want to promote the image to.</span></span>

### <a name="return-value---promotecolor"></a><span data-ttu-id="0f8ef-407">戻り値 - promoteColor</span><span class="sxs-lookup"><span data-stu-id="0f8ef-407">Return Value - promoteColor</span></span>

<span data-ttu-id="0f8ef-408">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-408">0 indicates success; otherwise, failure.</span></span>

### <a name="remarks---promotecolor"></a><span data-ttu-id="0f8ef-409">備考 - promoteColor</span><span class="sxs-lookup"><span data-stu-id="0f8ef-409">Remarks - promoteColor</span></span>

<span data-ttu-id="0f8ef-410">このメソッドは次を推進します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-410">The method promotes:</span></span>

-   <span data-ttu-id="0f8ef-411">8 ビット画像を 24、32 ビットに。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-411">8-bit images to 24 or 32 bits.</span></span>
-   <span data-ttu-id="0f8ef-412">4 ビット画像を 8、24、32 ビットに。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-412">4-bit images to 8, 24, or 32 bits.</span></span>
-   <span data-ttu-id="0f8ef-413">1 ビット画像を 4、8、24、32 ビットに。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-413">1-bit images to 4, 8, 24, or 32 bits.</span></span>

### <a name="examples---promotecolor"></a><span data-ttu-id="0f8ef-414">例 - promoteColor</span><span class="sxs-lookup"><span data-stu-id="0f8ef-414">Examples - promoteColor</span></span>

<span data-ttu-id="0f8ef-415">次の例では、イメージの色深度が 8 ビット以上でない場合は、ピクセルあたり 8 ビットに増やしています。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-415">The following example increases the color depth of an image to 8 bits per pixel, unless it is already 8 or more.</span></span>

```xpp
Image img = new Image(); 
img.loadFile(@'C:\test.bmp'); 
if (conpeek(img.imageInfo(),3) <8) 
{ 
    img.promoteColor(8); 
}
```

## <a name="method-reducecoloroctree"></a><span data-ttu-id="0f8ef-416">メソッド reduceColorOctree</span><span class="sxs-lookup"><span data-stu-id="0f8ef-416">Method reduceColorOctree</span></span>

<span data-ttu-id="0f8ef-417">画像の色深度を減少させます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-417">Reduces the color depth of an image.</span></span>

```xpp
public int reduceColorOctree(int maxColors)
```

### <a name="parameters---reducecoloroctree"></a><span data-ttu-id="0f8ef-418">パラメーター - reduceColorOctree</span><span class="sxs-lookup"><span data-stu-id="0f8ef-418">Parameters - reduceColorOctree</span></span>

<span data-ttu-id="0f8ef-419">maxColors</span><span class="sxs-lookup"><span data-stu-id="0f8ef-419">maxColors</span></span>  
<span data-ttu-id="0f8ef-420">最大色数。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-420">The maximum number of colors.</span></span>

### <a name="return-value---reducecoloroctree"></a><span data-ttu-id="0f8ef-421">戻り値 - reduceColorOctree</span><span class="sxs-lookup"><span data-stu-id="0f8ef-421">Return Value - reduceColorOctree</span></span>

<span data-ttu-id="0f8ef-422">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-422">0 indicates success; otherwise, failure.</span></span>

### <a name="remarks---reducecoloroctree"></a><span data-ttu-id="0f8ef-423">戻り値 - reduceColorOctree</span><span class="sxs-lookup"><span data-stu-id="0f8ef-423">Remarks - reduceColorOctree</span></span>

<span data-ttu-id="0f8ef-424">このメソッドは、他の指示が maxColors パラメーターで指定されていない限り、24 ビット イメージを 8 ビットに、または 8 ビット イメージを 4 ビットに縮小します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-424">The method reduces a 24-bit image to 8 bits, or an 8-bit image to 4 bits, unless other instructions are specified in the maxColors parameter.</span></span> <span data-ttu-id="0f8ef-425">MaxColors パラメーターが 16 以下の場合は、4 ビット イメージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-425">If the maxColors parameter is less than or equal to 16, a 4-bit image is produced.</span></span> <span data-ttu-id="0f8ef-426">MaxColors が 16 を超える場合は、8 ビット画像が生成されます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-426">If maxColors is more than 16, an 8-bit image is produced.</span></span>

## <a name="method-removeimage"></a><span data-ttu-id="0f8ef-427">メソッド removeImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-427">Method removeImage</span></span>

<span data-ttu-id="0f8ef-428">画像に関するデータを削除します。オブジェクトはまだ存在しますが、データを持ちません。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-428">Removes the data about an image; the object still exists, but has no data.</span></span>

```xpp
public int removeImage()
```

### <a name="return-value---removeimage"></a><span data-ttu-id="0f8ef-429">戻り値 - removeImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-429">Return Value - removeImage</span></span>

<span data-ttu-id="0f8ef-430">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-430">0 indicates success; otherwise, failure.</span></span>

## <a name="method-resize"></a><span data-ttu-id="0f8ef-431">メソッド resize</span><span class="sxs-lookup"><span data-stu-id="0f8ef-431">Method resize</span></span>

<span data-ttu-id="0f8ef-432">newWidth および newHeight パラメーターにより指定されたサイズに画像をサイズ変更します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-432">Resizes the image to the size that is specified by the newWidth and newHeight parameters.</span></span>

```xpp
public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)
```

### <a name="parameters---resize"></a><span data-ttu-id="0f8ef-433">パラメーター - resize</span><span class="sxs-lookup"><span data-stu-id="0f8ef-433">Parameters - resize</span></span>

<span data-ttu-id="0f8ef-434">newWidth</span><span class="sxs-lookup"><span data-stu-id="0f8ef-434">newWidth</span></span>  
<span data-ttu-id="0f8ef-435">resizing メソッド。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-435">The resizing method.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-436">newHeight</span><span class="sxs-lookup"><span data-stu-id="0f8ef-436">newHeight</span></span>  
<span data-ttu-id="0f8ef-437">resizing メソッド。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-437">The resizing method.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-438">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="0f8ef-438">InterpolationMode</span></span>  
<span data-ttu-id="0f8ef-439">resizing メソッド。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-439">The resizing method.</span></span>

### <a name="return-value---resize"></a><span data-ttu-id="0f8ef-440">戻り値 - resize</span><span class="sxs-lookup"><span data-stu-id="0f8ef-440">Return Value - resize</span></span>

<span data-ttu-id="0f8ef-441">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-441">0 indicates success; otherwise, failure.</span></span>

### <a name="remarks---resize"></a><span data-ttu-id="0f8ef-442">備考 - resize</span><span class="sxs-lookup"><span data-stu-id="0f8ef-442">Remarks - resize</span></span>

<span data-ttu-id="0f8ef-443">InterpolationMode パラメーターの使用可能な値は InterpolationMode システム列挙で使用可能な次の値です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-443">The possible values for the InterpolationMode parameter are those available in the InterpolationMode system enum:</span></span>

|     |                                      |                                                                                                                                                                        |
|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8ef-444">0</span><span class="sxs-lookup"><span data-stu-id="0f8ef-444">0</span></span>   | <span data-ttu-id="0f8ef-445">InterpolationModeDefault</span><span class="sxs-lookup"><span data-stu-id="0f8ef-445">InterpolationModeDefault</span></span>             | <span data-ttu-id="0f8ef-446">既定の補間モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-446">Specifies the default interpolation mode.</span></span>                                                                                                                              |
| <span data-ttu-id="0f8ef-447">1</span><span class="sxs-lookup"><span data-stu-id="0f8ef-447">1</span></span>   | <span data-ttu-id="0f8ef-448">InterpolationModeLowQuality</span><span class="sxs-lookup"><span data-stu-id="0f8ef-448">InterpolationModeLowQuality</span></span>          | <span data-ttu-id="0f8ef-449">低品質モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-449">Specifies a low-quality mode.</span></span>                                                                                                                                          |
| <span data-ttu-id="0f8ef-450">2</span><span class="sxs-lookup"><span data-stu-id="0f8ef-450">2</span></span>   | <span data-ttu-id="0f8ef-451">InterpolationModeHighQuality</span><span class="sxs-lookup"><span data-stu-id="0f8ef-451">InterpolationModeHighQuality</span></span>         | <span data-ttu-id="0f8ef-452">高品質モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-452">Specifies a high-quality mode.</span></span>                                                                                                                                         |
| <span data-ttu-id="0f8ef-453">3</span><span class="sxs-lookup"><span data-stu-id="0f8ef-453">3</span></span>   | <span data-ttu-id="0f8ef-454">InterpolationModeBilinear</span><span class="sxs-lookup"><span data-stu-id="0f8ef-454">InterpolationModeBilinear</span></span>            | <span data-ttu-id="0f8ef-455">線状補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-455">Specifies bilinear interpolation.</span></span> <span data-ttu-id="0f8ef-456">事前フィルター処理は行われません。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-456">No pre-filtering is done.</span></span> <span data-ttu-id="0f8ef-457">このメソッドは、画像を元のサイズの 50％ 以下に縮小するのには適していません。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-457">This method is not suitable for shrinking an image below 50% of its original size.</span></span>                         |
| <span data-ttu-id="0f8ef-458">4</span><span class="sxs-lookup"><span data-stu-id="0f8ef-458">4</span></span>   | <span data-ttu-id="0f8ef-459">InterpolationModeBicubic</span><span class="sxs-lookup"><span data-stu-id="0f8ef-459">InterpolationModeBicubic</span></span>             | <span data-ttu-id="0f8ef-460">バイキュービック補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-460">Specifies bicubic interpolation.</span></span> <span data-ttu-id="0f8ef-461">事前フィルター処理は行われません。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-461">No pre-filtering is done.</span></span> <span data-ttu-id="0f8ef-462">このメソッドは、画像を元のサイズの 25％ 以下に縮小するのには適していません。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-462">This method is not suitable for shrinking an image below 25% of its original size.</span></span>                          |
| <span data-ttu-id="0f8ef-463">5</span><span class="sxs-lookup"><span data-stu-id="0f8ef-463">5</span></span>   | <span data-ttu-id="0f8ef-464">InterpolationModeNearestNeighbor</span><span class="sxs-lookup"><span data-stu-id="0f8ef-464">InterpolationModeNearestNeighbor</span></span>     | <span data-ttu-id="0f8ef-465">ニアレストネイバー補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-465">Specifies nearest-neighbor interpolation.</span></span>                                                                                                                              |
| <span data-ttu-id="0f8ef-466">6</span><span class="sxs-lookup"><span data-stu-id="0f8ef-466">6</span></span>   | <span data-ttu-id="0f8ef-467">InterpolationModeHighQualityBilinear</span><span class="sxs-lookup"><span data-stu-id="0f8ef-467">InterpolationModeHighQualityBilinear</span></span> | <span data-ttu-id="0f8ef-468">高品質な線状補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-468">Specifies high-quality, bilinear interpolation.</span></span> <span data-ttu-id="0f8ef-469">高品質圧縮を確実に行うため、事前フィルター処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-469">Pre-filtering is performed to ensure high-quality shrinking.</span></span>                                                           |
| <span data-ttu-id="0f8ef-470">7</span><span class="sxs-lookup"><span data-stu-id="0f8ef-470">7</span></span>   | <span data-ttu-id="0f8ef-471">InterpolationModeHighQualityBicubic</span><span class="sxs-lookup"><span data-stu-id="0f8ef-471">InterpolationModeHighQualityBicubic</span></span>  | <span data-ttu-id="0f8ef-472">高品質なバイキュービック補間を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-472">Specifies high-quality, bicubic interpolation.</span></span> <span data-ttu-id="0f8ef-473">高品質圧縮を確実に行うため、事前フィルター処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-473">Pre-filtering is performed to ensure high-quality shrinking.</span></span> <span data-ttu-id="0f8ef-474">このモードでは、最高品質の変換画像が生成されます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-474">This mode produces the highest quality transformed images.</span></span> |

## <a name="method-rotate"></a><span data-ttu-id="0f8ef-475">メソッド rotate</span><span class="sxs-lookup"><span data-stu-id="0f8ef-475">Method rotate</span></span>

<span data-ttu-id="0f8ef-476">画像を回転します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-476">Rotates the image.</span></span>

```xpp
public int rotate(RotateType RotateType)
```

### <a name="parameters---rotate"></a><span data-ttu-id="0f8ef-477">パラメータ - rotate</span><span class="sxs-lookup"><span data-stu-id="0f8ef-477">Parameters - rotate</span></span>

<span data-ttu-id="0f8ef-478">RotateType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-478">RotateType</span></span>  
<span data-ttu-id="0f8ef-479">イメージを回転する量。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-479">The amount to rotate the image by.</span></span>

### <a name="return-value---rotate"></a><span data-ttu-id="0f8ef-480">備考 - rotate</span><span class="sxs-lookup"><span data-stu-id="0f8ef-480">Return Value - rotate</span></span>

<span data-ttu-id="0f8ef-481">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-481">0 indicates success; otherwise, failure.</span></span>

### <a name="remarks---rotate"></a><span data-ttu-id="0f8ef-482">備考 - rotate</span><span class="sxs-lookup"><span data-stu-id="0f8ef-482">Remarks - rotate</span></span>

<span data-ttu-id="0f8ef-483">RotateType パラメーターの使用可能な値は RotateType システム列挙で使用可能な次の値です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-483">The possible values for the RotateType parameter are those available in the RotateType system enum:</span></span>

|     |                    |                          |
|-----|--------------------|--------------------------|
| <span data-ttu-id="0f8ef-484">0</span><span class="sxs-lookup"><span data-stu-id="0f8ef-484">0</span></span>   | <span data-ttu-id="0f8ef-485">RotateNoneFlipNone</span><span class="sxs-lookup"><span data-stu-id="0f8ef-485">RotateNoneFlipNone</span></span> | <span data-ttu-id="0f8ef-486">回転なし。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-486">No rotation.</span></span>             |
| <span data-ttu-id="0f8ef-487">1</span><span class="sxs-lookup"><span data-stu-id="0f8ef-487">1</span></span>   | <span data-ttu-id="0f8ef-488">Rotate90FlipNone</span><span class="sxs-lookup"><span data-stu-id="0f8ef-488">Rotate90FlipNone</span></span>   | <span data-ttu-id="0f8ef-489">90 度回転します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-489">Rotation by 90 degrees.</span></span>  |
| <span data-ttu-id="0f8ef-490">2</span><span class="sxs-lookup"><span data-stu-id="0f8ef-490">2</span></span>   | <span data-ttu-id="0f8ef-491">Rotate180FlipNone</span><span class="sxs-lookup"><span data-stu-id="0f8ef-491">Rotate180FlipNone</span></span>  | <span data-ttu-id="0f8ef-492">180 度回転します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-492">Rotation by 180 degrees.</span></span> |
| <span data-ttu-id="0f8ef-493">3</span><span class="sxs-lookup"><span data-stu-id="0f8ef-493">3</span></span>   | <span data-ttu-id="0f8ef-494">Rotate270FlipNone</span><span class="sxs-lookup"><span data-stu-id="0f8ef-494">Rotate270FlipNone</span></span>  | <span data-ttu-id="0f8ef-495">270 度回転します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-495">Rotation by 270 degrees.</span></span> |

## <a name="method-saveimage"></a><span data-ttu-id="0f8ef-496">メソッド saveImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-496">Method saveImage</span></span>

<span data-ttu-id="0f8ef-497">指定されたファイル名に画像を保存します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-497">Saves the image to the specified file name.</span></span>

```xpp
public int saveImage(str fileName, [ImageSaveType Type])
```

### <a name="parameters---saveimage"></a><span data-ttu-id="0f8ef-498">パラメーター - saveImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-498">Parameters - saveImage</span></span>

<span data-ttu-id="0f8ef-499">fileName</span><span class="sxs-lookup"><span data-stu-id="0f8ef-499">fileName</span></span>  
<span data-ttu-id="0f8ef-500">ファイル拡張子で指定された形式とは異なる形式でファイルを保存するように指定できる ImageSaveType (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-500">An ImageSaveType that enables you to specify that the file should be saved as a different format from that specified by the file extension; optional.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-501">種類</span><span class="sxs-lookup"><span data-stu-id="0f8ef-501">Type</span></span>  
<span data-ttu-id="0f8ef-502">ファイル拡張子で指定された形式とは異なる形式でファイルを保存するように指定できる ImageSaveType (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-502">An ImageSaveType that enables you to specify that the file should be saved as a different format from that specified by the file extension; optional.</span></span>

### <a name="return-value---saveimage"></a><span data-ttu-id="0f8ef-503">戻り値 - saveImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-503">Return Value - saveImage</span></span>

<span data-ttu-id="0f8ef-504">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-504">0 if the method was successful.</span></span>

### <a name="remarks---saveimage"></a><span data-ttu-id="0f8ef-505">備考 - saveImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-505">Remarks - saveImage</span></span>

<span data-ttu-id="0f8ef-506">Type パラメーターの使用可能な値は ImageSaveType システム列挙で使用可能な値です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-506">The possible values for the Type parameter are those available in the ImageSaveType system enum.</span></span> <span data-ttu-id="0f8ef-507">たとえば、.jpg ファイルとして test.bmp を保存することができます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-507">For example, you could save test.bmp as a .jpg file.</span></span>

|     |                |
|-----|----------------|
| <span data-ttu-id="0f8ef-508">0</span><span class="sxs-lookup"><span data-stu-id="0f8ef-508">0</span></span>   | <span data-ttu-id="0f8ef-509">\_エクステンションの使用</span><span class="sxs-lookup"><span data-stu-id="0f8ef-509">Use\_Extension</span></span> |
| <span data-ttu-id="0f8ef-510">1</span><span class="sxs-lookup"><span data-stu-id="0f8ef-510">1</span></span>   | <span data-ttu-id="0f8ef-511">BMP</span><span class="sxs-lookup"><span data-stu-id="0f8ef-511">BMP</span></span>            |
| <span data-ttu-id="0f8ef-512">2</span><span class="sxs-lookup"><span data-stu-id="0f8ef-512">2</span></span>   | <span data-ttu-id="0f8ef-513">GIF</span><span class="sxs-lookup"><span data-stu-id="0f8ef-513">GIF</span></span>            |
| <span data-ttu-id="0f8ef-514">3</span><span class="sxs-lookup"><span data-stu-id="0f8ef-514">3</span></span>   | <span data-ttu-id="0f8ef-515">JPG</span><span class="sxs-lookup"><span data-stu-id="0f8ef-515">JPG</span></span>            |
| <span data-ttu-id="0f8ef-516">4</span><span class="sxs-lookup"><span data-stu-id="0f8ef-516">4</span></span>   | <span data-ttu-id="0f8ef-517">PNG</span><span class="sxs-lookup"><span data-stu-id="0f8ef-517">PNG</span></span>            |
| <span data-ttu-id="0f8ef-518">5</span><span class="sxs-lookup"><span data-stu-id="0f8ef-518">5</span></span>   | <span data-ttu-id="0f8ef-519">TIFF</span><span class="sxs-lookup"><span data-stu-id="0f8ef-519">TIFF</span></span>           |
| <span data-ttu-id="0f8ef-520">6</span><span class="sxs-lookup"><span data-stu-id="0f8ef-520">6</span></span>   | <span data-ttu-id="0f8ef-521">BMP\_UNCOMP</span><span class="sxs-lookup"><span data-stu-id="0f8ef-521">BMP\_UNCOMP</span></span>    |
| <span data-ttu-id="0f8ef-522">7</span><span class="sxs-lookup"><span data-stu-id="0f8ef-522">7</span></span>   | <span data-ttu-id="0f8ef-523">TIF\_UNCOMP</span><span class="sxs-lookup"><span data-stu-id="0f8ef-523">TIF\_UNCOMP</span></span>    |

### <a name="examples---saveimage"></a><span data-ttu-id="0f8ef-524">例 - saveImage</span><span class="sxs-lookup"><span data-stu-id="0f8ef-524">Examples - saveImage</span></span>

<span data-ttu-id="0f8ef-525">次の例では、画面の一部をファイルにキャプチャし、その画像をロードします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-525">The following example captures part of the screen to a file, and then loads that image.</span></span>

```xpp
Image img = new Image(); 
img.captureScreen(0, 0, 100, 100); 
img.saveImage(@'C:\test.bmp'); 
img.loadFile(@'C:\test.bmp');
```

## <a name="method-savetype"></a><span data-ttu-id="0f8ef-526">メソッド saveType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-526">Method saveType</span></span>

<span data-ttu-id="0f8ef-527">イメージ デコーダを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-527">Gets or sets the image decoder.</span></span>

```xpp
public ImageSaveType saveType([ImageSaveType Type])
```

### <a name="parameters---savetype"></a><span data-ttu-id="0f8ef-528">パラメーター - saveType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-528">Parameters - saveType</span></span>

<span data-ttu-id="0f8ef-529">種類</span><span class="sxs-lookup"><span data-stu-id="0f8ef-529">Type</span></span>  
<span data-ttu-id="0f8ef-530">設定するデコーダのタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-530">The type of decoder that you want to set; optional.</span></span>

### <a name="return-value---savetype"></a><span data-ttu-id="0f8ef-531">戻り値 - saveType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-531">Return Value - saveType</span></span>

### <a name="remarks---savetype"></a><span data-ttu-id="0f8ef-532">備考 - saveType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-532">Remarks - saveType</span></span>

<span data-ttu-id="0f8ef-533">Type パラメーターの使用可能な値は ImageSaveType システム列挙で使用可能な次の値です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-533">The possible values for the Type parameter are those available in the ImageSaveType system enum:</span></span>

|     |                |
|-----|----------------|
| <span data-ttu-id="0f8ef-534">0</span><span class="sxs-lookup"><span data-stu-id="0f8ef-534">0</span></span>   | <span data-ttu-id="0f8ef-535">\_エクステンションの使用</span><span class="sxs-lookup"><span data-stu-id="0f8ef-535">Use\_Extension</span></span> |
| <span data-ttu-id="0f8ef-536">1</span><span class="sxs-lookup"><span data-stu-id="0f8ef-536">1</span></span>   | <span data-ttu-id="0f8ef-537">BMP</span><span class="sxs-lookup"><span data-stu-id="0f8ef-537">BMP</span></span>            |
| <span data-ttu-id="0f8ef-538">2</span><span class="sxs-lookup"><span data-stu-id="0f8ef-538">2</span></span>   | <span data-ttu-id="0f8ef-539">GIF</span><span class="sxs-lookup"><span data-stu-id="0f8ef-539">GIF</span></span>            |
| <span data-ttu-id="0f8ef-540">3</span><span class="sxs-lookup"><span data-stu-id="0f8ef-540">3</span></span>   | <span data-ttu-id="0f8ef-541">JPG</span><span class="sxs-lookup"><span data-stu-id="0f8ef-541">JPG</span></span>            |
| <span data-ttu-id="0f8ef-542">4</span><span class="sxs-lookup"><span data-stu-id="0f8ef-542">4</span></span>   | <span data-ttu-id="0f8ef-543">PNG</span><span class="sxs-lookup"><span data-stu-id="0f8ef-543">PNG</span></span>            |
| <span data-ttu-id="0f8ef-544">5</span><span class="sxs-lookup"><span data-stu-id="0f8ef-544">5</span></span>   | <span data-ttu-id="0f8ef-545">TIFF</span><span class="sxs-lookup"><span data-stu-id="0f8ef-545">TIFF</span></span>           |
| <span data-ttu-id="0f8ef-546">6</span><span class="sxs-lookup"><span data-stu-id="0f8ef-546">6</span></span>   | <span data-ttu-id="0f8ef-547">BMP\_UNCOMP</span><span class="sxs-lookup"><span data-stu-id="0f8ef-547">BMP\_UNCOMP</span></span>    |
| <span data-ttu-id="0f8ef-548">7</span><span class="sxs-lookup"><span data-stu-id="0f8ef-548">7</span></span>   | <span data-ttu-id="0f8ef-549">TIF\_UNCOMP</span><span class="sxs-lookup"><span data-stu-id="0f8ef-549">TIF\_UNCOMP</span></span>    |

## <a name="method-setpixel"></a><span data-ttu-id="0f8ef-550">メソッド setPixel</span><span class="sxs-lookup"><span data-stu-id="0f8ef-550">Method setPixel</span></span>

<span data-ttu-id="0f8ef-551">x と y パラメーターで指定されているピクセルの色を設定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-551">Sets the color for the pixel that is specified by the x and y parameters.</span></span>

```xpp
public int setPixel(int x, int y, int pixel)
```

### <a name="parameters---setpixel"></a><span data-ttu-id="0f8ef-552">パラメーター - setPixel</span><span class="sxs-lookup"><span data-stu-id="0f8ef-552">Parameters - setPixel</span></span>

<span data-ttu-id="0f8ef-553">x</span><span class="sxs-lookup"><span data-stu-id="0f8ef-553">x</span></span>  
<span data-ttu-id="0f8ef-554">使用する色の ARGB 値。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-554">The ARGB value of the color that you want to use.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-555">y</span><span class="sxs-lookup"><span data-stu-id="0f8ef-555">y</span></span>  
<span data-ttu-id="0f8ef-556">使用する色の ARGB 値。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-556">The ARGB value of the color that you want to use.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-557">pixel</span><span class="sxs-lookup"><span data-stu-id="0f8ef-557">pixel</span></span>  
<span data-ttu-id="0f8ef-558">使用する色の ARGB 値。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-558">The ARGB value of the color that you want to use.</span></span>

### <a name="return-value---setpixel"></a><span data-ttu-id="0f8ef-559">備考 - setPixel</span><span class="sxs-lookup"><span data-stu-id="0f8ef-559">Return Value - setPixel</span></span>

<span data-ttu-id="0f8ef-560">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-560">0 indicates success; otherwise, failure.</span></span>

### <a name="remarks---setpixel"></a><span data-ttu-id="0f8ef-561">備考 - setPixel</span><span class="sxs-lookup"><span data-stu-id="0f8ef-561">Remarks - setPixel</span></span>

<span data-ttu-id="0f8ef-562">RGB カラー値を ARGB 値に変換するには、Image::rgb メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-562">To convert an RGB color value to an ARGB value, use the Image::rgb Method.</span></span>

## <a name="method-transparent"></a><span data-ttu-id="0f8ef-563">メソッド transparent</span><span class="sxs-lookup"><span data-stu-id="0f8ef-563">Method transparent</span></span>

<span data-ttu-id="0f8ef-564">画像の透明な色を設定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-564">Sets the transparent color for the image.</span></span>

```xpp
public int transparent([boolean Set], [int RValue], [int GValue], [int BValue])
```

### <a name="parameters---transparent"></a><span data-ttu-id="0f8ef-565">パラメーター - transparent</span><span class="sxs-lookup"><span data-stu-id="0f8ef-565">Parameters - transparent</span></span>

<span data-ttu-id="0f8ef-566">セット</span><span class="sxs-lookup"><span data-stu-id="0f8ef-566">Set</span></span>  
<span data-ttu-id="0f8ef-567">設定する色の青の値; オプション。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-567">Blue value of the color that you want to set; optional.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-568">RValue</span><span class="sxs-lookup"><span data-stu-id="0f8ef-568">RValue</span></span>  
<span data-ttu-id="0f8ef-569">設定する色の青の値; オプション。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-569">Blue value of the color that you want to set; optional.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-570">GValue</span><span class="sxs-lookup"><span data-stu-id="0f8ef-570">GValue</span></span>  
<span data-ttu-id="0f8ef-571">設定する色の青の値; オプション。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-571">Blue value of the color that you want to set; optional.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-572">BValue</span><span class="sxs-lookup"><span data-stu-id="0f8ef-572">BValue</span></span>  
<span data-ttu-id="0f8ef-573">設定する色の青の値; オプション。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-573">Blue value of the color that you want to set; optional.</span></span>

### <a name="return-value---transparent"></a><span data-ttu-id="0f8ef-574">戻り値 - transparent</span><span class="sxs-lookup"><span data-stu-id="0f8ef-574">Return Value - transparent</span></span>

<span data-ttu-id="0f8ef-575">0 は、成功を示し、それ以外の場合は、失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-575">0 to indicate success; otherwise, failure.</span></span>

### <a name="remarks---transparent"></a><span data-ttu-id="0f8ef-576">備考 - transparent</span><span class="sxs-lookup"><span data-stu-id="0f8ef-576">Remarks - transparent</span></span>

<span data-ttu-id="0f8ef-577">入力パラメーターのいずれかがない場合は、画像内の位置 (0, 0) での色が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-577">If any of the input parameters are missing, the color at the point (0,0) in the image is used.</span></span> <span data-ttu-id="0f8ef-578">色を指定する場合、パラメーター 2 から 4 を使用すると、RGB カラーとして表記されます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-578">If you want to specify a color, this is expressed as an RGB color by using parameters 2 to 4.</span></span>

## <a name="method-width"></a><span data-ttu-id="0f8ef-579">メソッド width</span><span class="sxs-lookup"><span data-stu-id="0f8ef-579">Method width</span></span>

<span data-ttu-id="0f8ef-580">ピクセル単位の画像の幅を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-580">Retrieves the width of the image in pixels.</span></span>

```xpp
public int width()
```

### <a name="return-value---width"></a><span data-ttu-id="0f8ef-581">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="0f8ef-581">Return Value - width</span></span>

<span data-ttu-id="0f8ef-582">画像の幅をピクセル単位で表す整数。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-582">An integer that represents the width of the image in pixels.</span></span>

### <a name="examples---width"></a><span data-ttu-id="0f8ef-583">例 - width</span><span class="sxs-lookup"><span data-stu-id="0f8ef-583">Examples - width</span></span>

<span data-ttu-id="0f8ef-584">次の例では、test.bmp ファイル内のイメージの幅を出力します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-584">The following example prints out the width of the image in the test.bmp file.</span></span>

```xpp
Image img = new Image(); 
img.loadFile(@'C:\test.bmp'); 
print img.width(); 
pause;
```

## <a name="method-canload"></a><span data-ttu-id="0f8ef-585">メソッド canLoad</span><span class="sxs-lookup"><span data-stu-id="0f8ef-585">Method canLoad</span></span>

<span data-ttu-id="0f8ef-586">画像ファイルが存在し、開くことができるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-586">Determines whether an image file exists and can be opened.</span></span>

```xpp
public static int canLoad(str filename)
```

### <a name="parameters---canload"></a><span data-ttu-id="0f8ef-587">パラメーター - canLoad</span><span class="sxs-lookup"><span data-stu-id="0f8ef-587">Parameters - canLoad</span></span>

<span data-ttu-id="0f8ef-588">filename</span><span class="sxs-lookup"><span data-stu-id="0f8ef-588">filename</span></span>  
<span data-ttu-id="0f8ef-589">確認するファイルの名前とパス。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-589">The name and path of the file to check.</span></span>

### <a name="return-value---canload"></a><span data-ttu-id="0f8ef-590">戻り値 - canLoad</span><span class="sxs-lookup"><span data-stu-id="0f8ef-590">Return Value - canLoad</span></span>

<span data-ttu-id="0f8ef-591">画像が検索され、開くことができる場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-591">1 if the image is found and can be opened; otherwise, 0.</span></span>

## <a name="method-loadext"></a><span data-ttu-id="0f8ef-592">メソッド loadExt</span><span class="sxs-lookup"><span data-stu-id="0f8ef-592">Method loadExt</span></span>

<span data-ttu-id="0f8ef-593">Image クラスでサポートされているファイル形式の拡張機能の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-593">Retrieves a list of the extensions of the file formats that are supported by the Image class.</span></span>

```xpp
public static container loadExt(int idx)
```

### <a name="parameters---loadext"></a><span data-ttu-id="0f8ef-594">パラメーター - loadExt</span><span class="sxs-lookup"><span data-stu-id="0f8ef-594">Parameters - loadExt</span></span>

<span data-ttu-id="0f8ef-595">idx</span><span class="sxs-lookup"><span data-stu-id="0f8ef-595">idx</span></span>  

### <a name="return-value---loadext"></a><span data-ttu-id="0f8ef-596">戻り値 - loadExt</span><span class="sxs-lookup"><span data-stu-id="0f8ef-596">Return Value - loadExt</span></span>

<span data-ttu-id="0f8ef-597">サポートされているファイル形式の一覧を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-597">A container that holds a list of the supported file formats.</span></span>

## <a name="method-resourcetype"></a><span data-ttu-id="0f8ef-598">メソッド resourceType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-598">Method resourceType</span></span>

<span data-ttu-id="0f8ef-599">特定のリソースがビットマップかアイコンかを判別します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-599">Determines whether a particular resource is a bitmap or an icon.</span></span>

```xpp
public static int resourceType(int resourceIdx)
```

### <a name="parameters---resourcetype"></a><span data-ttu-id="0f8ef-600">パラメーター - resourceType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-600">Parameters - resourceType</span></span>

<span data-ttu-id="0f8ef-601">resourceIdx</span><span class="sxs-lookup"><span data-stu-id="0f8ef-601">resourceIdx</span></span>  
<span data-ttu-id="0f8ef-602">読み込むリソースの ID。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-602">The ID of the resource that you want to load.</span></span>

### <a name="return-value---resourcetype"></a><span data-ttu-id="0f8ef-603">戻り値 - resourceType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-603">Return Value - resourceType</span></span>

<span data-ttu-id="0f8ef-604">画像がビットマップの場合は 0、アイコンの場合は 1 です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-604">0 if the image is a bitmap; 1 if it is an icon.</span></span>

### <a name="remarks---resourcetype"></a><span data-ttu-id="0f8ef-605">備考 - resourceType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-605">Remarks - resourceType</span></span>

<span data-ttu-id="0f8ef-606">リソースの値は、Resources マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-606">The values of resources can be found in the Resources macro.</span></span>

### <a name="examples---resourcetype"></a><span data-ttu-id="0f8ef-607">例 - resourceType</span><span class="sxs-lookup"><span data-stu-id="0f8ef-607">Examples - resourceType</span></span>

<span data-ttu-id="0f8ef-608">次の例では、リソース 3020 がアイコンかビットマップかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-608">The following example tests whether resource 3020 is an icon or a bitmap.</span></span>

```xpp
Resource 
print Image::resourceType(3020); 
pause;
```

## <a name="method-rgb"></a><span data-ttu-id="0f8ef-609">メソッド rgb</span><span class="sxs-lookup"><span data-stu-id="0f8ef-609">Method rgb</span></span>

<span data-ttu-id="0f8ef-610">RGB 値を ARGB 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-610">Converts an RGB value to an ARGB value.</span></span>

```xpp
public static int rgb(int R, int G, int B)
```

### <a name="parameters---rgb"></a><span data-ttu-id="0f8ef-611">戻り値 - rgb</span><span class="sxs-lookup"><span data-stu-id="0f8ef-611">Parameters - rgb</span></span>

<span data-ttu-id="0f8ef-612">R</span><span class="sxs-lookup"><span data-stu-id="0f8ef-612">R</span></span>  
<span data-ttu-id="0f8ef-613">色の青の値。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-613">The blue value of the color.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-614">G</span><span class="sxs-lookup"><span data-stu-id="0f8ef-614">G</span></span>  
<span data-ttu-id="0f8ef-615">色の青の値。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-615">The blue value of the color.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-616">B</span><span class="sxs-lookup"><span data-stu-id="0f8ef-616">B</span></span>  
<span data-ttu-id="0f8ef-617">色の青の値。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-617">The blue value of the color.</span></span>

### <a name="return-value---rgb"></a><span data-ttu-id="0f8ef-618">戻り値 - rgb</span><span class="sxs-lookup"><span data-stu-id="0f8ef-618">Return Value - rgb</span></span>

<span data-ttu-id="0f8ef-619">パラメーターで指定された色の ARGB 値を表す整数。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-619">An integer that represents the ARGB value of the color that is specified by the parameters.</span></span>

## <a name="method-validresource"></a><span data-ttu-id="0f8ef-620">メソッド validResource</span><span class="sxs-lookup"><span data-stu-id="0f8ef-620">Method validResource</span></span>

<span data-ttu-id="0f8ef-621">id パラメータで指定されたリソースが有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-621">Determines whether the resource specified by the id parameter is valid.</span></span>

```xpp
public static int validResource(int id)
```

### <a name="parameters---validresource"></a><span data-ttu-id="0f8ef-622">パラメーター - validResource</span><span class="sxs-lookup"><span data-stu-id="0f8ef-622">Parameters - validResource</span></span>

<span data-ttu-id="0f8ef-623">id</span><span class="sxs-lookup"><span data-stu-id="0f8ef-623">id</span></span>  
<span data-ttu-id="0f8ef-624">チェックするリソースの ID。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-624">The ID of the resource that you want to check.</span></span>

### <a name="return-value---validresource"></a><span data-ttu-id="0f8ef-625">戻り値 - validResource</span><span class="sxs-lookup"><span data-stu-id="0f8ef-625">Return Value - validResource</span></span>

<span data-ttu-id="0f8ef-626">ID が有効な場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-626">0 if the ID is valid.</span></span>

## <a name="method-new"></a><span data-ttu-id="0f8ef-627">メソッド new</span><span class="sxs-lookup"><span data-stu-id="0f8ef-627">Method new</span></span>

<span data-ttu-id="0f8ef-628">新しい画像を作成します</span><span class="sxs-lookup"><span data-stu-id="0f8ef-628">Creates a new image.</span></span>

```xpp
public void new([AnyType image], [int width], [int height])
```

### <a name="parameters---new"></a><span data-ttu-id="0f8ef-629">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="0f8ef-629">Parameters - new</span></span>

<span data-ttu-id="0f8ef-630">画像</span><span class="sxs-lookup"><span data-stu-id="0f8ef-630">image</span></span>  
<span data-ttu-id="0f8ef-631">ピクセル単位の画像の高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-631">The height of the image in pixels; optional.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-632">width</span><span class="sxs-lookup"><span data-stu-id="0f8ef-632">width</span></span>  
<span data-ttu-id="0f8ef-633">ピクセル単位の画像の高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-633">The height of the image in pixels; optional.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-634">height</span><span class="sxs-lookup"><span data-stu-id="0f8ef-634">height</span></span>  
<span data-ttu-id="0f8ef-635">ピクセル単位の画像の高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-635">The height of the image in pixels; optional.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="0f8ef-636">備考 - new</span><span class="sxs-lookup"><span data-stu-id="0f8ef-636">Remarks - new</span></span>

<span data-ttu-id="0f8ef-637">パラメーターを指定する必要はありませんが、イメージの内容とサイズを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-637">You do not need to specify any parameters, but it is possible to specify the image contents and size.</span></span> <span data-ttu-id="0f8ef-638">画像パラメーターについては、ファイル名および場所、リソース、配列での特定の画像、または別の画像オブジェクトを指定できます。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-638">For the image parameter, you can specify a file name and location, a resource, a particular image in an array, or another Image object.</span></span>

### <a name="examples---new"></a><span data-ttu-id="0f8ef-639">例 - new</span><span class="sxs-lookup"><span data-stu-id="0f8ef-639">Examples - new</span></span>

<span data-ttu-id="0f8ef-640">次の例は、新しいイメージ オブジェクトの既存のコンテンツをオプションで指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-640">The following examples illustrate how you can optionally specify the existing content for the new image object.</span></span>

```xpp
Image img1 = new Image(@"C:\MyPicture.jpg", 100, 100); 
Image img2 = new Image(121,100, 100); // Uses resource 121 in Ax32.exe 
Image img4 = new Image(img1, 200, 200);
```

## <a name="method-displayorign"></a><span data-ttu-id="0f8ef-641">メソッド displayOrign</span><span class="sxs-lookup"><span data-stu-id="0f8ef-641">Method displayOrign</span></span>

<span data-ttu-id="0f8ef-642">オリジナルの発注元 (0, 0) から、オフセット (X, Y) を指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-642">Enables you to specify an offset (X, Y) from the original origin (0, 0).</span></span>

```xpp
public void displayOrign(int Xpos, int Ypos)
```

### <a name="parameters---displayorign"></a><span data-ttu-id="0f8ef-643">パラメーター - displayOrign</span><span class="sxs-lookup"><span data-stu-id="0f8ef-643">Parameters - displayOrign</span></span>

<span data-ttu-id="0f8ef-644">Xpos</span><span class="sxs-lookup"><span data-stu-id="0f8ef-644">Xpos</span></span>  
<span data-ttu-id="0f8ef-645">原点に対する新しい Y (垂直) 座標。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-645">New Y (vertical) coordinate for the origin.</span></span>

<!-- -->

<span data-ttu-id="0f8ef-646">Ypos</span><span class="sxs-lookup"><span data-stu-id="0f8ef-646">Ypos</span></span>  
<span data-ttu-id="0f8ef-647">原点に対する新しい Y (垂直) 座標。</span><span class="sxs-lookup"><span data-stu-id="0f8ef-647">New Y (vertical) coordinate for the origin.</span></span>

## <a name="method-finalize"></a><span data-ttu-id="0f8ef-648">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="0f8ef-648">Method finalize</span></span>

```xpp
public void finalize()
```

