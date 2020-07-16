---
title: Imagelist クラス
description: このトピックでは、Imagelist クラスについて説明します。
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
ms.openlocfilehash: 1d2a8997548723d39f2b29b51908e306407bfd63
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502598"
---
# <a name="class-imagelist"></a><span data-ttu-id="17e99-103">クラス Imagelist</span><span class="sxs-lookup"><span data-stu-id="17e99-103">Class Imagelist</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Imagelist extends BinData
```

<span data-ttu-id="17e99-104">Imagelist クラスを使用すると、イメージの一覧を操作できます。</span><span class="sxs-lookup"><span data-stu-id="17e99-104">The Imagelist class lets you work with a list of images.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e99-105">備考</span><span class="sxs-lookup"><span data-stu-id="17e99-105">Remarks</span></span>

<span data-ttu-id="17e99-106">1 つの画像を操作するには、イメージ クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="17e99-106">To work with a single image, use the Image class.</span></span>

## <a name="examples"></a><span data-ttu-id="17e99-107">例</span><span class="sxs-lookup"><span data-stu-id="17e99-107">Examples</span></span>

<span data-ttu-id="17e99-108">次の例では、イメージ リストを作成し、Shell32.dll ファイルにアイコンを追加します。</span><span class="sxs-lookup"><span data-stu-id="17e99-108">The following example creates an image list and adds the icons in the Shell32.dll file.</span></span> <span data-ttu-id="17e99-109">一覧の 4 番目のメンバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="17e99-109">It then deletes the fourth member of the list.</span></span>

```xpp
Imagelist list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight() ); 
list.loadIcons('shell32.dll'); 
print list.count(); 
list.remove(4); 
print list.count(); 
pause;
```

## <a name="methods"></a><span data-ttu-id="17e99-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="17e99-110">Methods</span></span>

| <span data-ttu-id="17e99-111">方法</span><span class="sxs-lookup"><span data-stu-id="17e99-111">Method</span></span>                                                                         | <span data-ttu-id="17e99-112">説明</span><span class="sxs-lookup"><span data-stu-id="17e99-112">Description</span></span>                                                                                                                        |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e99-113">public int add(Image image)</span><span class="sxs-lookup"><span data-stu-id="17e99-113">public int add(Image image)</span></span>                                                    | <span data-ttu-id="17e99-114">イメージ リストに新しい画像を追加します。</span><span class="sxs-lookup"><span data-stu-id="17e99-114">Adds a new image to the image list.</span></span>                                                                                                |
| <span data-ttu-id="17e99-115">public boolean autoResize(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="17e99-115">public boolean autoResize(\[boolean value\])</span></span>                                   | <span data-ttu-id="17e99-116">新しいイメージを自動的にサイズ変更するかどうかを決定するブール値の autoResize フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-116">Sets the Boolean autoResize flag, which determines whether new images are automatically resized.</span></span>                                   |
| <span data-ttu-id="17e99-117">public int clear()</span><span class="sxs-lookup"><span data-stu-id="17e99-117">public int clear()</span></span>                                                             | <span data-ttu-id="17e99-118">イメージ リストからすべての画像を削除します。</span><span class="sxs-lookup"><span data-stu-id="17e99-118">Removes all images from the image list.</span></span>                                                                                            |
| <span data-ttu-id="17e99-119">public int count()</span><span class="sxs-lookup"><span data-stu-id="17e99-119">public int count()</span></span>                                                             | <span data-ttu-id="17e99-120">画像リスト内のイメージの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-120">Retrieves the number of images in an image list.</span></span>                                                                                   |
| <span data-ttu-id="17e99-121">public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)</span><span class="sxs-lookup"><span data-stu-id="17e99-121">public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)</span></span>             | <span data-ttu-id="17e99-122">イメージのドラッグを開始します。</span><span class="sxs-lookup"><span data-stu-id="17e99-122">Begins dragging an image.</span></span>                                                                                                          |
| <span data-ttu-id="17e99-123">public boolean dragEnd()</span><span class="sxs-lookup"><span data-stu-id="17e99-123">public boolean dragEnd()</span></span>                                                       | <span data-ttu-id="17e99-124">ドラッグ操作を終了します。</span><span class="sxs-lookup"><span data-stu-id="17e99-124">Ends a drag operation.</span></span>                                                                                                             |
| <span data-ttu-id="17e99-125">public boolean dragEnter(int hWnd, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="17e99-125">public boolean dragEnter(int hWnd, int x, int y)</span></span>                               | <span data-ttu-id="17e99-126">ドラッグ操作中に指定されたウィンドウの更新をロックし、ウィンドウの指定された位置にドラッグ イメージを表示します。</span><span class="sxs-lookup"><span data-stu-id="17e99-126">Locks updates to the specified window during a drag operation and displays the drag image at the specified position in the window.</span></span> |
| <span data-ttu-id="17e99-127">public boolean dragLeave(int hWnd)</span><span class="sxs-lookup"><span data-stu-id="17e99-127">public boolean dragLeave(int hWnd)</span></span>                                             | <span data-ttu-id="17e99-128">指定したウィンドウのロックを解除し、ドラッグ イメージを非表示にして、ウィンドウを更新します。</span><span class="sxs-lookup"><span data-stu-id="17e99-128">Unlocks the specified window and hides the drag image, so that the window to be updated.</span></span>                                           |
| <span data-ttu-id="17e99-129">public boolean dragMove(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="17e99-129">public boolean dragMove(int x, int y)</span></span>                                          | <span data-ttu-id="17e99-130">ドラッグ アンド ドロップ操作中にドラッグされているイメージを移動します。</span><span class="sxs-lookup"><span data-stu-id="17e99-130">Moves the image that is being dragged during a drag-and-drop operation.</span></span>                                                            |
| <span data-ttu-id="17e99-131">public boolean dragShowImage(boolean show)</span><span class="sxs-lookup"><span data-stu-id="17e99-131">public boolean dragShowImage(boolean show)</span></span>                                     | <span data-ttu-id="17e99-132">ドラッグされている画像の表示と非表示を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="17e99-132">Shows or hides the image that is being dragged.</span></span>                                                                                    |
| <span data-ttu-id="17e99-133">public int height()</span><span class="sxs-lookup"><span data-stu-id="17e99-133">public int height()</span></span>                                                            | <span data-ttu-id="17e99-134">イメージ リスト内のイメージの高さ (ピクセル単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-134">Retrieves the height, in pixels, of the images in the image list.</span></span>                                                                  |
| <span data-ttu-id="17e99-135">public int loadIcons(str moduleName)</span><span class="sxs-lookup"><span data-stu-id="17e99-135">public int loadIcons(str moduleName)</span></span>                                           | <span data-ttu-id="17e99-136">イメージ リストに、指定されたリソースからアイコンを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="17e99-136">Loads icons from the specified resource into the image list.</span></span>                                                                       |
| <span data-ttu-id="17e99-137">public int remove(int imageIdx)</span><span class="sxs-lookup"><span data-stu-id="17e99-137">public int remove(int imageIdx)</span></span>                                                | <span data-ttu-id="17e99-138">イメージ リストから画像を削除します。</span><span class="sxs-lookup"><span data-stu-id="17e99-138">Removes an image from an image list.</span></span>                                                                                               |
| <span data-ttu-id="17e99-139">public int replace(int imageIdx, Image image)</span><span class="sxs-lookup"><span data-stu-id="17e99-139">public int replace(int imageIdx, Image image)</span></span>                                  | <span data-ttu-id="17e99-140">リスト内の既存の画像を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="17e99-140">Replaces an existing image in the list.</span></span>                                                                                            |
| <span data-ttu-id="17e99-141">public boolean setOverlayImage(int imageIdx, int overlayIdx)</span><span class="sxs-lookup"><span data-stu-id="17e99-141">public boolean setOverlayImage(int imageIdx, int overlayIdx)</span></span>                   | <span data-ttu-id="17e99-142">オーバーレイ マスクとして使用する画像の一覧に、画像を追加します。</span><span class="sxs-lookup"><span data-stu-id="17e99-142">Adds an image to the list of images to use as overlay masks.</span></span>                                                                       |
| <span data-ttu-id="17e99-143">public int width()</span><span class="sxs-lookup"><span data-stu-id="17e99-143">public int width()</span></span>                                                             | <span data-ttu-id="17e99-144">イメージ リスト内のイメージの幅 (ピクセル単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-144">Retrieves the width, in pixels, of the images in the image list.</span></span>                                                                   |
| <span data-ttu-id="17e99-145">::public static int iconHeight()</span><span class="sxs-lookup"><span data-stu-id="17e99-145">::public static int iconHeight()</span></span>                                               | <span data-ttu-id="17e99-146">標準アイコンの高さのシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-146">Retrieves the system metrics for the height of a standard icon.</span></span>                                                                    |
| <span data-ttu-id="17e99-147">::public static int iconWidth()</span><span class="sxs-lookup"><span data-stu-id="17e99-147">::public static int iconWidth()</span></span>                                                | <span data-ttu-id="17e99-148">標準アイコンの幅のシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-148">Retrieves the system metrics for the width of a standard icon.</span></span>                                                                     |
| <span data-ttu-id="17e99-149">::public static int smallIconHeight()</span><span class="sxs-lookup"><span data-stu-id="17e99-149">::public static int smallIconHeight()</span></span>                                          | <span data-ttu-id="17e99-150">小さなアイコンの高さのシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-150">Retrieves the system metrics for the height of a small icon.</span></span>                                                                       |
| <span data-ttu-id="17e99-151">::public static int smallIconWidth()</span><span class="sxs-lookup"><span data-stu-id="17e99-151">::public static int smallIconWidth()</span></span>                                           | <span data-ttu-id="17e99-152">小さなアイコンの幅のシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-152">Retrieves the system metrics for the width of a small icon.</span></span>                                                                        |
| <span data-ttu-id="17e99-153">public void maskColor(int Color)</span><span class="sxs-lookup"><span data-stu-id="17e99-153">public void maskColor(int Color)</span></span>                                               | <span data-ttu-id="17e99-154">マスキング色を設定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-154">Sets the masking color.</span></span>                                                                                                            |
| <span data-ttu-id="17e99-155">public void draw(int HDC, int imageIdx, int x, int y, \[boolean transparent\])</span><span class="sxs-lookup"><span data-stu-id="17e99-155">public void draw(int HDC, int imageIdx, int x, int y, \[boolean transparent\])</span></span> | <span data-ttu-id="17e99-156">指定されたデバイス コンテキストで画像リスト項目を描画します。</span><span class="sxs-lookup"><span data-stu-id="17e99-156">Draws an image list item in the specified device context.</span></span>                                                                          |
| <span data-ttu-id="17e99-157">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="17e99-157">public void finalize()</span></span>                                                         |                                                                                                                                    |
| <span data-ttu-id="17e99-158">public void new(int cx, int cy, \[boolean transparent\])</span><span class="sxs-lookup"><span data-stu-id="17e99-158">public void new(int cx, int cy, \[boolean transparent\])</span></span>                       | <span data-ttu-id="17e99-159">画像を保持する新しい空のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="17e99-159">Creates a new empty list to hold images.</span></span>                                                                                           |

## <a name="method-add"></a><span data-ttu-id="17e99-160">メソッド add</span><span class="sxs-lookup"><span data-stu-id="17e99-160">Method add</span></span>

<span data-ttu-id="17e99-161">イメージ リストに新しい画像を追加します。</span><span class="sxs-lookup"><span data-stu-id="17e99-161">Adds a new image to the image list.</span></span>

```xpp
public int add(Image image)
```

### <a name="parameters---add"></a><span data-ttu-id="17e99-162">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="17e99-162">Parameters - add</span></span>

<span data-ttu-id="17e99-163">画像</span><span class="sxs-lookup"><span data-stu-id="17e99-163">image</span></span>  
<span data-ttu-id="17e99-164">リストに追加する新しい画像。</span><span class="sxs-lookup"><span data-stu-id="17e99-164">The new image to add to the list.</span></span>

### <a name="return-value---add"></a><span data-ttu-id="17e99-165">戻り値 - add</span><span class="sxs-lookup"><span data-stu-id="17e99-165">Return Value - add</span></span>

<span data-ttu-id="17e99-166">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-166">0 if the method is successful.</span></span>

### <a name="remarks---add"></a><span data-ttu-id="17e99-167">備考 - add</span><span class="sxs-lookup"><span data-stu-id="17e99-167">Remarks - add</span></span>

<span data-ttu-id="17e99-168">autoResize メソッドを使用すると、リストに追加するときにイメージのサイズを自動的に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="17e99-168">You can use the autoResize method to automatically resize images when you add them to the list.</span></span>

### <a name="examples---add"></a><span data-ttu-id="17e99-169">例 - add</span><span class="sxs-lookup"><span data-stu-id="17e99-169">Examples - add</span></span>

<span data-ttu-id="17e99-170">次の例では、新しいイメージ リストを作成し、3 つのイメージを追加します。</span><span class="sxs-lookup"><span data-stu-id="17e99-170">The following example creates a new image list and adds three images to it.</span></span>

```xpp
ImageList list = new Imagelist( 
    Imagelist::smallIconWidth(), 
    Imagelist::smallIconHeight()); 
list.add(new Image(3104)); 
list.add(new Image(1097)); 
list.add(new Image(1200)); 
// Prints 3 
print list.count(); 
pause;
```

## <a name="method-autoresize"></a><span data-ttu-id="17e99-171">メソッド autoResize</span><span class="sxs-lookup"><span data-stu-id="17e99-171">Method autoResize</span></span>

<span data-ttu-id="17e99-172">新しいイメージを自動的にサイズ変更するかどうかを決定するブール値の autoResize フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-172">Sets the Boolean autoResize flag, which determines whether new images are automatically resized.</span></span>

```xpp
public boolean autoResize([boolean value])
```

### <a name="parameters---autoresize"></a><span data-ttu-id="17e99-173">パラメーター - autoResize</span><span class="sxs-lookup"><span data-stu-id="17e99-173">Parameters - autoResize</span></span>

<span data-ttu-id="17e99-174">値</span><span class="sxs-lookup"><span data-stu-id="17e99-174">value</span></span>  
<span data-ttu-id="17e99-175">autoResize フラグが設定されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="17e99-175">A Boolean value that determines whether the autoResize flag is set; optional.</span></span>

### <a name="return-value---autoresize"></a><span data-ttu-id="17e99-176">戻り値 - autoResize</span><span class="sxs-lookup"><span data-stu-id="17e99-176">Return Value - autoResize</span></span>

### <a name="remarks---autoresize"></a><span data-ttu-id="17e99-177">備考 - autoResize</span><span class="sxs-lookup"><span data-stu-id="17e99-177">Remarks - autoResize</span></span>

<span data-ttu-id="17e99-178">autoResize フラッグが true に設定されている場合、リストに追加する任意の画像サイズは、画像リストの作成時に指定された分析コードに自動的に再調整されます。</span><span class="sxs-lookup"><span data-stu-id="17e99-178">If the autoResize flag is set to true, any image that you add to the list is automatically resized to the dimensions that were specified when you created the image list.</span></span>

## <a name="method-clear"></a><span data-ttu-id="17e99-179">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="17e99-179">Method clear</span></span>

<span data-ttu-id="17e99-180">イメージ リストからすべての画像を削除します。</span><span class="sxs-lookup"><span data-stu-id="17e99-180">Removes all images from the image list.</span></span>

```xpp
public int clear()
```

### <a name="return-value---clear"></a><span data-ttu-id="17e99-181">戻り値 - clear</span><span class="sxs-lookup"><span data-stu-id="17e99-181">Return Value - clear</span></span>

<span data-ttu-id="17e99-182">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-182">0 if the method is successful.</span></span>

## <a name="method-count"></a><span data-ttu-id="17e99-183">メソッド count</span><span class="sxs-lookup"><span data-stu-id="17e99-183">Method count</span></span>

<span data-ttu-id="17e99-184">画像リスト内のイメージの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-184">Retrieves the number of images in an image list.</span></span>

```xpp
public int count()
```

### <a name="return-value---count"></a><span data-ttu-id="17e99-185">戻り値 - count</span><span class="sxs-lookup"><span data-stu-id="17e99-185">Return Value - count</span></span>

<span data-ttu-id="17e99-186">リスト内の画像の数を表す整数。</span><span class="sxs-lookup"><span data-stu-id="17e99-186">An integer that represents the number of images in the list.</span></span>

### <a name="examples---count"></a><span data-ttu-id="17e99-187">例 - count</span><span class="sxs-lookup"><span data-stu-id="17e99-187">Examples - count</span></span>

<span data-ttu-id="17e99-188">次の例では、イメージ リストを作成し、shell.dll ファイルからアイコンを読み込み、リスト内のイメージの数を出力します。</span><span class="sxs-lookup"><span data-stu-id="17e99-188">The following example creates an image list, loads icons from the shell.dll file, and then prints the number of images in the list.</span></span>

```xpp
Imagelist list; 
int       counter; 
list = new Imagelist( 
   Imagelist::iconWidth(), 
   Imagelist::iconHeight() ); 
list.loadIcons('shell32.dll'); 
print list.count(); 
pause;
```

## <a name="method-dragbegin"></a><span data-ttu-id="17e99-189">メソッド dragBegin</span><span class="sxs-lookup"><span data-stu-id="17e99-189">Method dragBegin</span></span>

<span data-ttu-id="17e99-190">イメージのドラッグを開始します。</span><span class="sxs-lookup"><span data-stu-id="17e99-190">Begins dragging an image.</span></span>

```xpp
public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)
```

### <a name="parameters---dragbegin"></a><span data-ttu-id="17e99-191">パラメーター - dragBegin</span><span class="sxs-lookup"><span data-stu-id="17e99-191">Parameters - dragBegin</span></span>

<span data-ttu-id="17e99-192">imageIdx</span><span class="sxs-lookup"><span data-stu-id="17e99-192">imageIdx</span></span>  
<span data-ttu-id="17e99-193">画像の左上隅を基準とした、ドラッグ位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="17e99-193">The Y-coordinate of the drag position, relative to the upper-left corner of the image.</span></span>

<!-- -->

<span data-ttu-id="17e99-194">hotSpotX</span><span class="sxs-lookup"><span data-stu-id="17e99-194">hotSpotX</span></span>  
<span data-ttu-id="17e99-195">画像の左上隅を基準とした、ドラッグ位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="17e99-195">The Y-coordinate of the drag position, relative to the upper-left corner of the image.</span></span>

<!-- -->

<span data-ttu-id="17e99-196">hotSpotY</span><span class="sxs-lookup"><span data-stu-id="17e99-196">hotSpotY</span></span>  
<span data-ttu-id="17e99-197">画像の左上隅を基準とした、ドラッグ位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="17e99-197">The Y-coordinate of the drag position, relative to the upper-left corner of the image.</span></span>

### <a name="return-value---dragbegin"></a><span data-ttu-id="17e99-198">戻り値 - dragBegin</span><span class="sxs-lookup"><span data-stu-id="17e99-198">Return Value - dragBegin</span></span>

<span data-ttu-id="17e99-199">メソッドが成功した場合は 1 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-199">1 if the method is successful.</span></span>

### <a name="remarks---dragbegin"></a><span data-ttu-id="17e99-200">備考 - dragBegin</span><span class="sxs-lookup"><span data-stu-id="17e99-200">Remarks - dragBegin</span></span>

<span data-ttu-id="17e99-201">残りのドラッグ操作は、dragEnter、dragMove、dragLeave、dragEnd の各メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-201">The rest of the drag operation is specified by the dragEnter, dragMove, dragLeave, and dragEnd methods.</span></span>

## <a name="method-dragend"></a><span data-ttu-id="17e99-202">メソッド dragEnd</span><span class="sxs-lookup"><span data-stu-id="17e99-202">Method dragEnd</span></span>

<span data-ttu-id="17e99-203">ドラッグ操作を終了します。</span><span class="sxs-lookup"><span data-stu-id="17e99-203">Ends a drag operation.</span></span>

```xpp
public boolean dragEnd()
```

### <a name="return-value---dragend"></a><span data-ttu-id="17e99-204">戻り値 - dragEnd</span><span class="sxs-lookup"><span data-stu-id="17e99-204">Return Value - dragEnd</span></span>

<span data-ttu-id="17e99-205">メソッドが成功した場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-205">1 if the method is successful; otherwise, 0.</span></span>

### <a name="remarks---dragend"></a><span data-ttu-id="17e99-206">備考 - dragEnd</span><span class="sxs-lookup"><span data-stu-id="17e99-206">Remarks - dragEnd</span></span>

<span data-ttu-id="17e99-207">残りのドラッグ操作は、dragBegin、dragEnter、dragMove、dragLeave の各メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-207">The rest of the drag operation is specified by the dragBegin, dragEnter, dragMove, and dragLeave methods.</span></span>

## <a name="method-dragenter"></a><span data-ttu-id="17e99-208">メソッド dragEnter</span><span class="sxs-lookup"><span data-stu-id="17e99-208">Method dragEnter</span></span>

<span data-ttu-id="17e99-209">ドラッグ操作中に指定されたウィンドウの更新をロックし、ウィンドウの指定された位置にドラッグ イメージを表示します。</span><span class="sxs-lookup"><span data-stu-id="17e99-209">Locks updates to the specified window during a drag operation and displays the drag image at the specified position in the window.</span></span>

```xpp
public boolean dragEnter(int hWnd, int x, int y)
```

### <a name="parameters---dragenter"></a><span data-ttu-id="17e99-210">パラメーター - dragEnter</span><span class="sxs-lookup"><span data-stu-id="17e99-210">Parameters - dragEnter</span></span>

<span data-ttu-id="17e99-211">hWnd</span><span class="sxs-lookup"><span data-stu-id="17e99-211">hWnd</span></span>  
<span data-ttu-id="17e99-212">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="17e99-212">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

<!-- -->

<span data-ttu-id="17e99-213">x</span><span class="sxs-lookup"><span data-stu-id="17e99-213">x</span></span>  
<span data-ttu-id="17e99-214">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="17e99-214">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

<!-- -->

<span data-ttu-id="17e99-215">y</span><span class="sxs-lookup"><span data-stu-id="17e99-215">y</span></span>  
<span data-ttu-id="17e99-216">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="17e99-216">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

### <a name="return-value---dragenter"></a><span data-ttu-id="17e99-217">戻り値 - dragEnter</span><span class="sxs-lookup"><span data-stu-id="17e99-217">Return Value - dragEnter</span></span>

<span data-ttu-id="17e99-218">メソッドが成功した場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-218">1 if the method is successful; otherwise, 0.</span></span>

### <a name="remarks---dragenter"></a><span data-ttu-id="17e99-219">備考 - dragEnter</span><span class="sxs-lookup"><span data-stu-id="17e99-219">Remarks - dragEnter</span></span>

<span data-ttu-id="17e99-220">ドラッグ操作を開始するには、dragBegin メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="17e99-220">To start the drag operation, call the dragBegin method.</span></span> <span data-ttu-id="17e99-221">残りのドラッグ操作は、dragMove、dragLeave、dragEnd の各メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-221">The rest of the drag operation is specified by the dragMove, dragLeave, and dragEnd methods.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="17e99-222">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="17e99-222">Method dragLeave</span></span>

<span data-ttu-id="17e99-223">指定したウィンドウのロックを解除し、ドラッグ イメージを非表示にして、ウィンドウを更新します。</span><span class="sxs-lookup"><span data-stu-id="17e99-223">Unlocks the specified window and hides the drag image, so that the window to be updated.</span></span>

```xpp
public boolean dragLeave(int hWnd)
```

### <a name="parameters---dragleave"></a><span data-ttu-id="17e99-224">パラメーター - dragLeave</span><span class="sxs-lookup"><span data-stu-id="17e99-224">Parameters - dragLeave</span></span>

<span data-ttu-id="17e99-225">hWnd</span><span class="sxs-lookup"><span data-stu-id="17e99-225">hWnd</span></span>  
<span data-ttu-id="17e99-226">ドラッグ イメージを所有するウィンドウのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="17e99-226">The handle to the window that owns the drag image.</span></span>

### <a name="return-value---dragleave"></a><span data-ttu-id="17e99-227">戻り値 - dragLeave</span><span class="sxs-lookup"><span data-stu-id="17e99-227">Return Value - dragLeave</span></span>

<span data-ttu-id="17e99-228">メソッドが成功した場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-228">1 if the method is successful; otherwise, 0.</span></span>

### <a name="remarks---dragleave"></a><span data-ttu-id="17e99-229">備考 - dragLeave</span><span class="sxs-lookup"><span data-stu-id="17e99-229">Remarks - dragLeave</span></span>

<span data-ttu-id="17e99-230">残りのドラッグ操作は、dragBegin、dragEnter、dragMove、dragEnd の各メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-230">The rest of the drag operation is specified by the dragBegin, dragEnter, dragMove, and dragEnd methods.</span></span>

## <a name="method-dragmove"></a><span data-ttu-id="17e99-231">メソッド dragMove</span><span class="sxs-lookup"><span data-stu-id="17e99-231">Method dragMove</span></span>

<span data-ttu-id="17e99-232">ドラッグ アンド ドロップ操作中にドラッグされているイメージを移動します。</span><span class="sxs-lookup"><span data-stu-id="17e99-232">Moves the image that is being dragged during a drag-and-drop operation.</span></span>

```xpp
public boolean dragMove(int x, int y)
```

### <a name="parameters---dragmove"></a><span data-ttu-id="17e99-233">パラメーター - dragMove</span><span class="sxs-lookup"><span data-stu-id="17e99-233">Parameters - dragMove</span></span>

<span data-ttu-id="17e99-234">x</span><span class="sxs-lookup"><span data-stu-id="17e99-234">x</span></span>  
<span data-ttu-id="17e99-235">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="17e99-235">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

<!-- -->

<span data-ttu-id="17e99-236">y</span><span class="sxs-lookup"><span data-stu-id="17e99-236">y</span></span>  
<span data-ttu-id="17e99-237">ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。</span><span class="sxs-lookup"><span data-stu-id="17e99-237">The Y-coordinate at which to display the drag icon, relative to the upper-left corner of the window.</span></span>

### <a name="return-value---dragmove"></a><span data-ttu-id="17e99-238">戻り値 - dragMove</span><span class="sxs-lookup"><span data-stu-id="17e99-238">Return Value - dragMove</span></span>

<span data-ttu-id="17e99-239">メソッドが成功した場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-239">1 if the method is successful; otherwise, 0.</span></span>

### <a name="remarks---dragmove"></a><span data-ttu-id="17e99-240">備考 - dragMove</span><span class="sxs-lookup"><span data-stu-id="17e99-240">Remarks - dragMove</span></span>

<span data-ttu-id="17e99-241">ドラッグ操作を開始するには、dragBegin メソッドを呼び出してから dragEnter メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="17e99-241">To start the drag operation, call the dragBegin method and then the dragEnter method.</span></span> <span data-ttu-id="17e99-242">残りのドラッグ操作は、dragLeave メソッドおよび dragEnd メソッドで指定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-242">The rest of the drag operation is specified by the dragLeave and dragEnd methods.</span></span>

## <a name="method-dragshowimage"></a><span data-ttu-id="17e99-243">メソッド dragShowImage</span><span class="sxs-lookup"><span data-stu-id="17e99-243">Method dragShowImage</span></span>

<span data-ttu-id="17e99-244">ドラッグされている画像の表示と非表示を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="17e99-244">Shows or hides the image that is being dragged.</span></span>

```xpp
public boolean dragShowImage(boolean show)
```

### <a name="parameters---dragshowimage"></a><span data-ttu-id="17e99-245">パラメーター - dragShowImage</span><span class="sxs-lookup"><span data-stu-id="17e99-245">Parameters - dragShowImage</span></span>

<span data-ttu-id="17e99-246">show</span><span class="sxs-lookup"><span data-stu-id="17e99-246">show</span></span>  
<span data-ttu-id="17e99-247">画像を表示するかどうかを指定する値。</span><span class="sxs-lookup"><span data-stu-id="17e99-247">A value that specifies whether to show the image.</span></span>

### <a name="return-value---dragshowimage"></a><span data-ttu-id="17e99-248">戻り値 - dragShowImage</span><span class="sxs-lookup"><span data-stu-id="17e99-248">Return Value - dragShowImage</span></span>

## <a name="method-height"></a><span data-ttu-id="17e99-249">メソッド height</span><span class="sxs-lookup"><span data-stu-id="17e99-249">Method height</span></span>

<span data-ttu-id="17e99-250">イメージ リスト内のイメージの高さ (ピクセル単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-250">Retrieves the height, in pixels, of the images in the image list.</span></span>

```xpp
public int height()
```

### <a name="return-value---height"></a><span data-ttu-id="17e99-251">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="17e99-251">Return Value - height</span></span>

<span data-ttu-id="17e99-252">画像の高さをピクセル単位で表す整数。</span><span class="sxs-lookup"><span data-stu-id="17e99-252">An integer that represents the height of the images in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="17e99-253">備考 - height</span><span class="sxs-lookup"><span data-stu-id="17e99-253">Remarks - height</span></span>

<span data-ttu-id="17e99-254">リスト内の画像の高さは、リストをインスタンス化するときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="17e99-254">The height of the images in the list is set when you instantiate the list.</span></span>

### <a name="examples---height"></a><span data-ttu-id="17e99-255">例 - height</span><span class="sxs-lookup"><span data-stu-id="17e99-255">Examples - height</span></span>

<span data-ttu-id="17e99-256">次の例では、イメージ リストを作成し、イメージの高さと幅を iconWidth メソッドと iconHeight メソッドで指定された寸法に設定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-256">The following example creates an image list, and sets the height and width of the images to the dimensions that are specified by the iconWidth and iconHeight methods.</span></span> <span data-ttu-id="17e99-257">一覧内のイメージの高さを出力します。</span><span class="sxs-lookup"><span data-stu-id="17e99-257">It then prints the height of images in the list.</span></span>

```xpp
Imagelist list; 
list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight()); 
print list.height();   
pause;
```

## <a name="method-loadicons"></a><span data-ttu-id="17e99-258">メソッド loadIcons</span><span class="sxs-lookup"><span data-stu-id="17e99-258">Method loadIcons</span></span>

<span data-ttu-id="17e99-259">イメージ リストに、指定されたリソースからアイコンを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="17e99-259">Loads icons from the specified resource into the image list.</span></span>

```xpp
public int loadIcons(str moduleName)
```

### <a name="parameters---loadicons"></a><span data-ttu-id="17e99-260">パラメーター - loadIcons</span><span class="sxs-lookup"><span data-stu-id="17e99-260">Parameters - loadIcons</span></span>

<span data-ttu-id="17e99-261">moduleName</span><span class="sxs-lookup"><span data-stu-id="17e99-261">moduleName</span></span>  
<span data-ttu-id="17e99-262">イメージの読み込み元ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="17e99-262">The name of the file from which to load images.</span></span>

### <a name="return-value---loadicons"></a><span data-ttu-id="17e99-263">戻り値 - loadIcons</span><span class="sxs-lookup"><span data-stu-id="17e99-263">Return Value - loadIcons</span></span>

<span data-ttu-id="17e99-264">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-264">0 if the method is successful.</span></span>

### <a name="examples---loadicons"></a><span data-ttu-id="17e99-265">例 - loadIcons</span><span class="sxs-lookup"><span data-stu-id="17e99-265">Examples - loadIcons</span></span>

<span data-ttu-id="17e99-266">次の例では、イメージのリストを作成し、shell32.dll ファイルに含まれるイメージをロードします。</span><span class="sxs-lookup"><span data-stu-id="17e99-266">The following example creates a list of images and then loads the images that are contained in the shell32.dll file.</span></span>

```xpp
Imagelist list; 
list = new Imagelist(Imagelist::iconWidth(),Imagelist::iconHeight()); 
list.loadIcons('shell32.dll');
```

## <a name="method-remove"></a><span data-ttu-id="17e99-267">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="17e99-267">Method remove</span></span>

<span data-ttu-id="17e99-268">イメージ リストから画像を削除します。</span><span class="sxs-lookup"><span data-stu-id="17e99-268">Removes an image from an image list.</span></span>

```xpp
public int remove(int imageIdx)
```

### <a name="parameters---remove"></a><span data-ttu-id="17e99-269">パラメーター - remove</span><span class="sxs-lookup"><span data-stu-id="17e99-269">Parameters - remove</span></span>

<span data-ttu-id="17e99-270">imageIdx</span><span class="sxs-lookup"><span data-stu-id="17e99-270">imageIdx</span></span>  
<span data-ttu-id="17e99-271">一覧から削除する画像の位置。</span><span class="sxs-lookup"><span data-stu-id="17e99-271">The position of the image to remove from the list.</span></span>

### <a name="return-value---remove"></a><span data-ttu-id="17e99-272">戻り値 - remove</span><span class="sxs-lookup"><span data-stu-id="17e99-272">Return Value - remove</span></span>

<span data-ttu-id="17e99-273">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-273">0 if the method is successful.</span></span>

### <a name="examples---remove"></a><span data-ttu-id="17e99-274">例 - remove</span><span class="sxs-lookup"><span data-stu-id="17e99-274">Examples - remove</span></span>

<span data-ttu-id="17e99-275">次の例では、イメージ リストを作成し、アイコンを shell32.dll ファイルに追加して、リストの 4 番目のメンバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="17e99-275">The following example creates an image list, adds the icons in shell32.dll file, and then deletes the fourth member of the list.</span></span>

```xpp
Imagelist list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight() ); 
list.loadIcons('shell32.dll'); 
print list.count(); 
list.remove(4); 
print list.count(); 
pause;
```

## <a name="method-replace"></a><span data-ttu-id="17e99-276">メソッド replace</span><span class="sxs-lookup"><span data-stu-id="17e99-276">Method replace</span></span>

<span data-ttu-id="17e99-277">リスト内の既存の画像を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="17e99-277">Replaces an existing image in the list.</span></span>

```xpp
public int replace(int imageIdx, Image image)
```

### <a name="parameters---replace"></a><span data-ttu-id="17e99-278">パラメーター - replace</span><span class="sxs-lookup"><span data-stu-id="17e99-278">Parameters - replace</span></span>

<span data-ttu-id="17e99-279">imageIdx</span><span class="sxs-lookup"><span data-stu-id="17e99-279">imageIdx</span></span>  
<span data-ttu-id="17e99-280">既存のイメージを置き換えるために使用するイメージ。</span><span class="sxs-lookup"><span data-stu-id="17e99-280">The image to use to replace the existing image.</span></span>

<!-- -->

<span data-ttu-id="17e99-281">画像</span><span class="sxs-lookup"><span data-stu-id="17e99-281">image</span></span>  
<span data-ttu-id="17e99-282">既存のイメージを置き換えるために使用するイメージ。</span><span class="sxs-lookup"><span data-stu-id="17e99-282">The image to use to replace the existing image.</span></span>

### <a name="return-value---replace"></a><span data-ttu-id="17e99-283">戻り値 - replace</span><span class="sxs-lookup"><span data-stu-id="17e99-283">Return Value - replace</span></span>

<span data-ttu-id="17e99-284">メソッドが成功した場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-284">0 if the method is successful.</span></span>

## <a name="method-setoverlayimage"></a><span data-ttu-id="17e99-285">メソッド setOverlayImage</span><span class="sxs-lookup"><span data-stu-id="17e99-285">Method setOverlayImage</span></span>

<span data-ttu-id="17e99-286">オーバーレイ マスクとして使用する画像の一覧に、画像を追加します。</span><span class="sxs-lookup"><span data-stu-id="17e99-286">Adds an image to the list of images to use as overlay masks.</span></span>

```xpp
public boolean setOverlayImage(int imageIdx, int overlayIdx)
```

### <a name="parameters---setoverlayimage"></a><span data-ttu-id="17e99-287">パラメーター - setOverlayImage</span><span class="sxs-lookup"><span data-stu-id="17e99-287">Parameters - setOverlayImage</span></span>

<span data-ttu-id="17e99-288">imageIdx</span><span class="sxs-lookup"><span data-stu-id="17e99-288">imageIdx</span></span>  
<span data-ttu-id="17e99-289">オーバーレイ マスクの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="17e99-289">The one-based index of the overlay mask.</span></span>

<!-- -->

<span data-ttu-id="17e99-290">overlayIdx</span><span class="sxs-lookup"><span data-stu-id="17e99-290">overlayIdx</span></span>  
<span data-ttu-id="17e99-291">オーバーレイ マスクの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="17e99-291">The one-based index of the overlay mask.</span></span>

### <a name="return-value---setoverlayimage"></a><span data-ttu-id="17e99-292">戻り値 - setOverlayImage</span><span class="sxs-lookup"><span data-stu-id="17e99-292">Return Value - setOverlayImage</span></span>

<span data-ttu-id="17e99-293">メソッドが成功した場合は 1 です。</span><span class="sxs-lookup"><span data-stu-id="17e99-293">1 if the method is successful.</span></span>

### <a name="examples---setoverlayimage"></a><span data-ttu-id="17e99-294">例 - setOverlayImage</span><span class="sxs-lookup"><span data-stu-id="17e99-294">Examples - setOverlayImage</span></span>

<span data-ttu-id="17e99-295">次の例では、3 つのイメージを持つイメージ リストを作成し、最後のイメージをオーバーレイ マスクとして設定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-295">The following example creates an image list that has three images and then sets the last image as an overlay mask.</span></span>

```xpp
Imagelist list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight() ); 
list.add(new Image(824)); // Image 0 
list.add(new Image(815)); // Image 1 
list.add(new Image(936)); //Image 2 
list.setOverlayImage (2,1);
```

## <a name="method-width"></a><span data-ttu-id="17e99-296">メソッド width</span><span class="sxs-lookup"><span data-stu-id="17e99-296">Method width</span></span>

<span data-ttu-id="17e99-297">イメージ リスト内のイメージの幅 (ピクセル単位) を取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-297">Retrieves the width, in pixels, of the images in the image list.</span></span>

```xpp
public int width()
```

### <a name="return-value---width"></a><span data-ttu-id="17e99-298">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="17e99-298">Return Value - width</span></span>

<span data-ttu-id="17e99-299">画像の幅をピクセル単位で表す整数。</span><span class="sxs-lookup"><span data-stu-id="17e99-299">An integer that represents the width of the images in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="17e99-300">備考 - width</span><span class="sxs-lookup"><span data-stu-id="17e99-300">Remarks - width</span></span>

<span data-ttu-id="17e99-301">リスト内の画像の幅は、リストをインスタンス化するときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="17e99-301">The width of the images in the list is set when you instantiate the list.</span></span>

### <a name="examples---width"></a><span data-ttu-id="17e99-302">例 - width</span><span class="sxs-lookup"><span data-stu-id="17e99-302">Examples - width</span></span>

<span data-ttu-id="17e99-303">次の例では、アイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの幅をリストに出力します。</span><span class="sxs-lookup"><span data-stu-id="17e99-303">The following example creates an image list that has the standard height and width for icons, and then prints the width of images in the list.</span></span>

```xpp
Imagelist list; 
list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight()); 
print list.width();   
pause;
```

## <a name="method-iconheight"></a><span data-ttu-id="17e99-304">メソッド iconHeight</span><span class="sxs-lookup"><span data-stu-id="17e99-304">Method iconHeight</span></span>

<span data-ttu-id="17e99-305">標準アイコンの高さのシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-305">Retrieves the system metrics for the height of a standard icon.</span></span>

```xpp
public static int iconHeight()
```

### <a name="return-value---iconheight"></a><span data-ttu-id="17e99-306">戻り値 - iconHeight</span><span class="sxs-lookup"><span data-stu-id="17e99-306">Return Value - iconHeight</span></span>

<span data-ttu-id="17e99-307">標準アイコンの高さを表す整数。</span><span class="sxs-lookup"><span data-stu-id="17e99-307">An integer that represents the height of a standard icon.</span></span>

### <a name="examples---iconheight"></a><span data-ttu-id="17e99-308">例 - iconHeight</span><span class="sxs-lookup"><span data-stu-id="17e99-308">Examples - iconHeight</span></span>

<span data-ttu-id="17e99-309">次の例では、イメージのリストを作成し、標準のアイコンの幅と高さに設定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-309">The following example creates a list of images, and then sets them to the standard icon width and height.</span></span>

```xpp
ImageList list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight());
```

## <a name="method-iconwidth"></a><span data-ttu-id="17e99-310">メソッド iconWidth</span><span class="sxs-lookup"><span data-stu-id="17e99-310">Method iconWidth</span></span>

<span data-ttu-id="17e99-311">標準アイコンの幅のシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-311">Retrieves the system metrics for the width of a standard icon.</span></span>

```xpp
public static int iconWidth()
```

### <a name="return-value---iconwidth"></a><span data-ttu-id="17e99-312">戻り値 - iconWidth</span><span class="sxs-lookup"><span data-stu-id="17e99-312">Return Value - iconWidth</span></span>

<span data-ttu-id="17e99-313">標準アイコンの幅を表す整数。</span><span class="sxs-lookup"><span data-stu-id="17e99-313">An integer that represents the width of a standard icon.</span></span>

### <a name="examples---iconwidth"></a><span data-ttu-id="17e99-314">例 - iconWidth</span><span class="sxs-lookup"><span data-stu-id="17e99-314">Examples - iconWidth</span></span>

<span data-ttu-id="17e99-315">次の例では、イメージのリストを作成し、標準のアイコンの幅と高さに設定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-315">The following example creates a list of images, and then sets them to the standard icon width and height.</span></span>

```xpp
ImageList list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight());
```

## <a name="method-smalliconheight"></a><span data-ttu-id="17e99-316">メソッド smallIconHeight</span><span class="sxs-lookup"><span data-stu-id="17e99-316">Method smallIconHeight</span></span>

<span data-ttu-id="17e99-317">小さなアイコンの高さのシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-317">Retrieves the system metrics for the height of a small icon.</span></span>

```xpp
public static int smallIconHeight()
```

### <a name="return-value---smalliconheight"></a><span data-ttu-id="17e99-318">戻り値 - smallIconHeight</span><span class="sxs-lookup"><span data-stu-id="17e99-318">Return Value - smallIconHeight</span></span>

<span data-ttu-id="17e99-319">小さなアイコンの高さを表す整数。</span><span class="sxs-lookup"><span data-stu-id="17e99-319">An integer that represents the height of a small icon.</span></span>

### <a name="examples---smalliconheight"></a><span data-ttu-id="17e99-320">例 - smallIconHeight</span><span class="sxs-lookup"><span data-stu-id="17e99-320">Examples - smallIconHeight</span></span>

<span data-ttu-id="17e99-321">次の例では、小さなアイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの高さをリストに出力します。</span><span class="sxs-lookup"><span data-stu-id="17e99-321">The following example creates an image list that has the standard height and width for small icons, and then prints the height of images in the list.</span></span>

```xpp
Imagelist list = new Imagelist( 
    Imagelist::smallIconWidth(), 
    Imagelist::smallIconHeight()); 
print list.height();   
pause;
```

## <a name="method-smalliconwidth"></a><span data-ttu-id="17e99-322">メソッド smallIconWidth</span><span class="sxs-lookup"><span data-stu-id="17e99-322">Method smallIconWidth</span></span>

<span data-ttu-id="17e99-323">小さなアイコンの幅のシステム メトリックを取得します。</span><span class="sxs-lookup"><span data-stu-id="17e99-323">Retrieves the system metrics for the width of a small icon.</span></span>

```xpp
public static int smallIconWidth()
```

### <a name="return-value---smalliconwidth"></a><span data-ttu-id="17e99-324">戻り値 - smallIconWidth</span><span class="sxs-lookup"><span data-stu-id="17e99-324">Return Value - smallIconWidth</span></span>

<span data-ttu-id="17e99-325">小さなアイコンの幅を表す整数。</span><span class="sxs-lookup"><span data-stu-id="17e99-325">An integer that represents the width of a small icon.</span></span>

### <a name="examples---smalliconwidth"></a><span data-ttu-id="17e99-326">例 - smallIconWidth</span><span class="sxs-lookup"><span data-stu-id="17e99-326">Examples - smallIconWidth</span></span>

<span data-ttu-id="17e99-327">次の例では、小さなアイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの幅をリストに出力します。</span><span class="sxs-lookup"><span data-stu-id="17e99-327">The following example creates an image list that has the standard height and width for small icons, and then prints the width of images in the list.</span></span>

```xpp
Imagelist list = new Imagelist( 
   Imagelist::smallIconWidth(), 
   Imagelist::smallIconHeight()); 
print list.width();   
pause;
```

## <a name="method-maskcolor"></a><span data-ttu-id="17e99-328">メソッド maskColor</span><span class="sxs-lookup"><span data-stu-id="17e99-328">Method maskColor</span></span>

<span data-ttu-id="17e99-329">マスキング色を設定します。</span><span class="sxs-lookup"><span data-stu-id="17e99-329">Sets the masking color.</span></span>

```xpp
public void maskColor(int Color)
```

### <a name="parameters---maskcolor"></a><span data-ttu-id="17e99-330">パラメーター - maskColor</span><span class="sxs-lookup"><span data-stu-id="17e99-330">Parameters - maskColor</span></span>

<span data-ttu-id="17e99-331">色</span><span class="sxs-lookup"><span data-stu-id="17e99-331">Color</span></span>  
<span data-ttu-id="17e99-332">ARGB 値としての色。</span><span class="sxs-lookup"><span data-stu-id="17e99-332">The color as an ARGB value.</span></span>

## <a name="method-draw"></a><span data-ttu-id="17e99-333">メソッド draw</span><span class="sxs-lookup"><span data-stu-id="17e99-333">Method draw</span></span>

<span data-ttu-id="17e99-334">指定されたデバイス コンテキストで画像リスト項目を描画します。</span><span class="sxs-lookup"><span data-stu-id="17e99-334">Draws an image list item in the specified device context.</span></span>

```xpp
public void draw(int HDC, int imageIdx, int x, int y, [boolean transparent])
```

### <a name="parameters---draw"></a><span data-ttu-id="17e99-335">パラメーター - draw</span><span class="sxs-lookup"><span data-stu-id="17e99-335">Parameters - draw</span></span>

<span data-ttu-id="17e99-336">HDC</span><span class="sxs-lookup"><span data-stu-id="17e99-336">HDC</span></span>  
<span data-ttu-id="17e99-337">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="17e99-337">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

<!-- -->

<span data-ttu-id="17e99-338">imageIdx</span><span class="sxs-lookup"><span data-stu-id="17e99-338">imageIdx</span></span>  
<span data-ttu-id="17e99-339">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="17e99-339">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

<!-- -->

<span data-ttu-id="17e99-340">x</span><span class="sxs-lookup"><span data-stu-id="17e99-340">x</span></span>  
<span data-ttu-id="17e99-341">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="17e99-341">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

<!-- -->

<span data-ttu-id="17e99-342">y</span><span class="sxs-lookup"><span data-stu-id="17e99-342">y</span></span>  
<span data-ttu-id="17e99-343">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="17e99-343">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

<!-- -->

<span data-ttu-id="17e99-344">透明</span><span class="sxs-lookup"><span data-stu-id="17e99-344">transparent</span></span>  
<span data-ttu-id="17e99-345">背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="17e99-345">A Boolean value that indicates whether the image is drawn transparently by using the mask, regardless of background color; optional.</span></span>

## <a name="method-finalize"></a><span data-ttu-id="17e99-346">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="17e99-346">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="17e99-347">メソッド new</span><span class="sxs-lookup"><span data-stu-id="17e99-347">Method new</span></span>

<span data-ttu-id="17e99-348">画像を保持する新しい空のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="17e99-348">Creates a new empty list to hold images.</span></span>

```xpp
public void new(int cx, int cy, [boolean transparent])
```

### <a name="parameters---new"></a><span data-ttu-id="17e99-349">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="17e99-349">Parameters - new</span></span>

<span data-ttu-id="17e99-350">cx</span><span class="sxs-lookup"><span data-stu-id="17e99-350">cx</span></span>  

<!-- -->

<span data-ttu-id="17e99-351">cy</span><span class="sxs-lookup"><span data-stu-id="17e99-351">cy</span></span>  

<!-- -->

<span data-ttu-id="17e99-352">透明</span><span class="sxs-lookup"><span data-stu-id="17e99-352">transparent</span></span>  

### <a name="remarks---new"></a><span data-ttu-id="17e99-353">備考 - new</span><span class="sxs-lookup"><span data-stu-id="17e99-353">Remarks - new</span></span>

<span data-ttu-id="17e99-354">autoResize メソッドを使用すると、リストに追加するときにイメージのサイズを自動的に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="17e99-354">You can use the autoResize method to automatically resize images when you add them to the list.</span></span>

### <a name="examples---new"></a><span data-ttu-id="17e99-355">例 - new</span><span class="sxs-lookup"><span data-stu-id="17e99-355">Examples - new</span></span>

<span data-ttu-id="17e99-356">次の例では、標準アイコンの幅と高さの項目を保持するイメージ リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="17e99-356">The following example creates an image list to hold items of the standard icon width and height.</span></span>

```xpp
Imagelist list; 
list = new Imagelist( 
   Imagelist::iconWidth(), 
   Imagelist::iconHeight());
```

