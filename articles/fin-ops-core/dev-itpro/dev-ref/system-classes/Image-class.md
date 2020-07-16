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
# <a name="class-image"></a>クラス イメージ

[!include [banner](../../includes/banner.md)]

```xpp
class Image extends BinData
```

読み込み、保存、および画像を操作するためのメソッドを提供します。 複数のイメージを同時に操作する場合は、Imagelist クラスを使用します。

## <a name="remarks"></a>備考

次のファイル タイプからイメージ オブジェクトを作成することができます。

-   ラスター (ビットマップ) 形式 - .bmp、.gif、.jpg、.png、.tiff、.exif
-   ベクター形式 - .emf および .wmf

複数のイメージを同時に操作する場合は、Imagelist クラスを使用します。 次のファイル タイプからイメージ オブジェクトを作成することができます。

-   ラスター (ビットマップである) 形式 - .bmp、.gif、.jpg、.png、.tiff、.exif
-   ベクター形式 - .emf および .wmf

イメージ クラスは、クライアントにバインドされます。 ファイル操作に伴うセキュリティ上のリスクのため、クラスをサーバーから実行できなくなりました。

## <a name="examples"></a>例

次の例では、Picture.jpg の高さをピクセル単位で出力します。

```xpp
Image img = new  Image(); 
img.loadFile(@'C:\MyPictures\Picture.jpg'); 
print img.height(); 
pause;
```

## <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public int captureScreen(int left, int top, int right, int bottom)                                          | パラメータ リストで指定された座標を使用して、スクリーンからイメージをキャプチャします。                                           |
| public int captureWindow(int hWnd)                                                                          | パラメータとして指定されたハンドルを使用して、ウィンドウをイメージとしてキャプチャします。                                                              |
| public int clipboardCopy()                                                                                  | イメージをクリップボードにコピーします。                                                                                                             |
| public int clipboardPaste()                                                                                 | システムのクリップボードの内容で既存のイメージを上書きします。                                                                        |
| public int copyImage(Image image)                                                                           | 現在のイメージ オブジェクトをコピーします。                                                                                                              |
| public int createImage(int Width, int Height, int BitsPerPixel)                                             | パラメーターで指定された幅、高さ、および色深度を持つ空のビットマップ画像を作成します。                                         |
| public int crop(int x, int y, int w, int h)                                                                 | 画像をトリミングします。                                                                                                                              |
| public int displayImage(Int64 HDC, \[int Mode\], \[int Xpos\], \[int Ypos\], \[int Width\], \[int Height\]) | HDC パラメーターで指定されたデバイス コンテキストに画像を描画します。                                                                        |
| public Int64 exportBitmap()                                                                                 | 画像のハンドルを取得します。                                                                                                                  |
| public int flip(FlipType FlipType)                                                                          | 画像を垂直または水平方向に 180 度回転します。                                                                          |
| public container getImageDimensionUnits()                                                                   |                                                                                                                                               |
| public int getPixel(int x, int y)                                                                           | パラメーターで指定されたポイントで、ピクセルの ARGB カラーの値を取得します。                                                 |
| public int height()                                                                                         | ピクセル単位の画像の高さを取得します。                                                                                                  |
| public container imageInfo()                                                                                | 画像の幅、高さ、色深度を取得します。                                                                                    |
| public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)                           | センター座標 x および y で半径により定義された円内のスポットライト効果を生成します。                                      |
| public int importBitmap(Int64 hBitmap)                                                                      | hBitmap パラメータで指定されたイメージからビットマップをクローンします。                                                                    |
| public int importFileIcon(str fileName)                                                                     | ファイルに使用されているアイコンをコピーすることにより、fileName パラメーターで指定されたファイルからアイコンを作成します。                              |
| public int importIcon(str fileName, int iconIdx)                                                            | 実行可能ファイルからアイコンへのハンドルを取得します。 このアイコンは、fileName および iconIdx パラメーターで指定します。 |
| public int loadImage(str fileName)                                                                          | fileName パラメーターで指定されたファイルからイメージを読み込みます。                                                                             |
| public int loadResource(int id)                                                                             | Ax32.exe からリソースを読み込みます。                                                                                                               |
| public int promoteColor(int noOfColorBits)                                                                  | 画像の色深度を向上させます。                                                                                                       |
| public int reduceColorOctree(int maxColors)                                                                 | 画像の色深度を減少させます。                                                                                                          |
| public int removeImage()                                                                                    | 画像に関するデータを削除します。オブジェクトはまだ存在しますが、データを持ちません。                                                                    |
| public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)                         | newWidth および newHeight パラメーターにより指定されたサイズに画像をサイズ変更します。                                                     |
| public int rotate(RotateType RotateType)                                                                    | 画像を回転します。                                                                                                                            |
| public int saveImage(str fileName, \[ImageSaveType Type\])                                                  | 指定されたファイル名に画像を保存します。                                                                                                   |
| public ImageSaveType saveType(\[ImageSaveType Type\])                                                       | イメージ デコーダを取得または設定します。                                                                                                               |
| public int setPixel(int x, int y, int pixel)                                                                | x と y パラメーターで指定されているピクセルの色を設定します。                                                                     |
| public int transparent(\[boolean Set\], \[int RValue\], \[int GValue\], \[int BValue\])                     | 画像の透明な色を設定します。                                                                                                     |
| public int width()                                                                                          | ピクセル単位の画像の幅を取得します。                                                                                                   |
| ::public static int canLoad(str filename)                                                                   | 画像ファイルが存在し、開くことができるかどうかを決定します。                                                                                    |
| ::public static container loadExt(int idx)                                                                  | Image クラスでサポートされているファイル形式の拡張機能の一覧を取得します。                                                 |
| ::public static int resourceType(int resourceIdx)                                                           | 特定のリソースがビットマップかアイコンかを判別します。                                                                              |
| ::public static int rgb(int R, int G, int B)                                                                | RGB 値を ARGB 値に変換します。                                                                                                       |
| ::public static int validResource(int id)                                                                   | id パラメータで指定されたリソースが有効かどうかを判定します。                                                                       |
| public void new(\[AnyType image\], \[int width\], \[int height\])                                           | 新しい画像を作成します                                                                                                                          |
| public void displayOrign(int Xpos, int Ypos)                                                                | オリジナルの発注元 (0, 0) から、オフセット (X, Y) を指定できるようにします。                                                                      |
| public void finalize()                                                                                      |                                                                                                                                               |

## <a name="method-capturescreen"></a>メソッド captureScreen

パラメータ リストで指定された座標を使用して、スクリーンからイメージをキャプチャします。

```xpp
public int captureScreen(int left, int top, int right, int bottom)
```

### <a name="parameters---capturescreen"></a>パラメーター - captureScreen

left  
キャプチャする画面の右下隅部分の Y 座標です。

<!-- -->

戻る  
キャプチャする画面の右下隅部分の Y 座標です。

<!-- -->

権限  
キャプチャする画面の右下隅部分の Y 座標です。

<!-- -->

bottom  
キャプチャする画面の右下隅部分の Y 座標です。

### <a name="return-value---capturescreen"></a>戻り値 - captureScreen

0 は、成功を示します。 その他の値はエラーを示します。

### <a name="examples---capturescreen"></a>例 - captureScreen

次の例では、画面の一部をキャプチャし、test.bmp という名前のファイルに保存します。

```xpp
Image img = new Image(); 
img.captureScreen(0, 0, 100, 100); 
img.saveFile(@'C:\test.bmp');
```

## <a name="method-capturewindow"></a>メソッド captureWindow

パラメータとして指定されたハンドルを使用して、ウィンドウをイメージとしてキャプチャします。

```xpp
public int captureWindow(int hWnd)
```

### <a name="parameters---capturewindow"></a>パラメーター - captureWindow

hWnd  
キャプチャするウィンドウのハンドル。整数として指定する必要があります。

### <a name="return-value---capturewindow"></a>戻り値 - captureWindow

0 は、成功を示し、それ以外の場合は、失敗を示します。

## <a name="method-clipboardcopy"></a>メソッド clipboardCopy

イメージをクリップボードにコピーします。

```xpp
public int clipboardCopy()
```

### <a name="return-value---clipboardcopy"></a>戻り値 - clipboardCopy

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="examples---clipboardcopy"></a>例 - clipboardCopy

次の例では、Test.bmp という名前のファイルからコンテンツをコピーします。

```xpp
Image img = new Image(); 
img.loadFile(@'C:\Test.bmp'); 
img.clipboardCopy(); 
// Image can now be pasted into an application.
```

## <a name="method-clipboardpaste"></a>メソッド clipboardPaste

システムのクリップボードの内容で既存のイメージを上書きします。

```xpp
public int clipboardPaste()
```

### <a name="return-value---clipboardpaste"></a>戻り値 - clipboardPaste

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="remarks---clipboardpaste"></a>備考 - clipboardPaste

正常に使用されるメソッドについては、クリップボードにコンテンツが必要です。

### <a name="examples---clipboardpaste"></a>例 - clipboardPaste

次の例では、以前にクリップボードにコピーされたコンテンツを使用して新しいイメージ ファイルを作成します。

```xpp
Image img = new Image();
// Copy an image to the clipboard before this test 
img.clipboardPaste(); 
img.saveFile(@'C:\test.jpg');
```

## <a name="method-copyimage"></a>メソッド copyImage

現在のイメージ オブジェクトをコピーします。

```xpp
public int copyImage(Image image)
```

### <a name="parameters---copyimage"></a>パラメーター - copyImage

画像  
コピーする画像。

### <a name="return-value---copyimage"></a>戻り値 - copyImage

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="examples---copyimage"></a>例 - copyImage

次の例では、2 つの新しいイメージを作成し、1 つのイメージの内容をもう一方のイメージの内容で上書きします。

```xpp
Image img =  new Image(); 
Image img2 = new Image(); 
img.loadFile(@'C:\test.bmp'); 
img2.loadFile(@'C:\test2.bmp'); 
img2.copyImage(img); //img2 now the same as img
```

## <a name="method-createimage"></a>メソッド createImage

パラメーターで指定された幅、高さ、および色深度を持つ空のビットマップ画像を作成します。

```xpp
public int createImage(int Width, int Height, int BitsPerPixel)
```

### <a name="parameters---createimage"></a>パラメーター - createImage

Width  
画像の色深度。 有効値は 1、4、8、16、24、32 です。

<!-- -->

高さ  
画像の色深度。 有効値は 1、4、8、16、24、32 です。

<!-- -->

BitsPerPixel  
画像の色深度。 有効値は 1、4、8、16、24、32 です。

### <a name="return-value---createimage"></a>戻り値 - createImage

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="examples---createimage"></a>例 - createImage

次の例では、高さと幅が 16 ピクセル、色深度がピクセルあたり 32 ビットのイメージを作成します。

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

## <a name="method-crop"></a>メソッド crop

画像をトリミングします。

```xpp
public int crop(int x, int y, int w, int h)
```

### <a name="parameters---crop"></a>パラメーター - crop

x  
点 (x、y) からトリミングする領域の高さ。

<!-- -->

y  
点 (x、y) からトリミングする領域の高さ。

<!-- -->

w  
点 (x、y) からトリミングする領域の高さ。

<!-- -->

h  
点 (x、y) からトリミングする領域の高さ。

### <a name="return-value---crop"></a>戻り値 - crop

0 は、成功を示し、それ以外の場合は、失敗を示します。

## <a name="method-displayimage"></a>メソッド displayImage

HDC パラメーターで指定されたデバイス コンテキストに画像を描画します。

```xpp
public int displayImage(Int64 HDC, [int Mode], [int Xpos], [int Ypos], [int Width], [int Height])
```

### <a name="parameters---displayimage"></a>パラメーター - displayImage

HDC  
オプションのパラメーター。

<!-- -->

モード  
オプションのパラメーター。

<!-- -->

Xpos  
オプションのパラメーター。

<!-- -->

Ypos  
オプションのパラメーター。

<!-- -->

幅  
オプションのパラメーター。

<!-- -->

Height  
オプションのパラメーター。

### <a name="return-value---displayimage"></a>戻り値 - displayImage

0 は、成功を示し、それ以外の場合は、失敗を示します。

## <a name="method-exportbitmap"></a>メソッド exportBitmap

画像のハンドルを取得します。

```xpp
public Int64 exportBitmap()
```

### <a name="return-value---exportbitmap"></a>戻り値 - exportBitmap

画像のハンドル を表す整数。

### <a name="examples---exportbitmap"></a>例 - exportBitmap

次の例では、イメージのハンドルを取得し、ハンドルを使用してイメージを複製します。

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

## <a name="method-flip"></a>メソッド flip

画像を垂直または水平方向に 180 度回転します。

```xpp
public int flip(FlipType FlipType)
```

### <a name="parameters---flip"></a>パラメーター - flip

FlipType  
イメージを反転させる方法を決定する FlipType 列挙。

### <a name="return-value---flip"></a>戻り値 - flip

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="remarks---flip"></a>備考 - flip

FlipType パラメーターの使用可能な値は FlipType システム列挙で使用可能な次の値です。

|     |                    |                                                          |
|-----|--------------------|----------------------------------------------------------|
| 0   | RotateNoneFlipNone | 反転なし                                                  |
| 1   | RotateNoneFlipX    | 画像を水平方向に 180 度回転します。 |
| 2   | RotateNoneFlipX    | 画像を垂直方向に 180 度回転します。   |

## <a name="method-getimagedimensionunits"></a>メソッド getImageDimensionUnits

```xpp
public container getImageDimensionUnits()
```

### <a name="return-value---getimagedimensionunits"></a>戻り値 - getImageDimensionUnits

## <a name="method-getpixel"></a>メソッド getPixel

パラメーターで指定されたポイントで、ピクセルの ARGB カラーの値を取得します。

```xpp
public int getPixel(int x, int y)
```

### <a name="parameters---getpixel"></a>パラメーター - getPixel

x  
ピクセルの垂直座標。

<!-- -->

y  
ピクセルの垂直座標。

### <a name="return-value---getpixel"></a>戻り値 - getPixel

ピクセルの ARGB 値である整数 (RGB カラーの 32 ビット表示) 。

## <a name="method-height"></a>メソッド height

ピクセル単位の画像の高さを取得します。

```xpp
public int height()
```

### <a name="return-value---height"></a>戻り値 - height

画像の高さをピクセル単位で表す整数。

### <a name="examples---height"></a>例 - height

次の例では、test.bmp に含まれるイメージの高さを出力します。

```xpp
Image img = new Image(); 
img.loadFile(@'C:\test.bmp'); 
print img.height(); 
pause;
```

## <a name="method-imageinfo"></a>メソッド imageInfo

画像の幅、高さ、色深度を取得します。

```xpp
public container imageInfo()
```

### <a name="return-value---imageinfo"></a>戻り値 - imageInfo

画像の幅、画像の高さ、およびピクセルあたりのビット数を指定する値を保持するコンテナーです。

### <a name="examples---imageinfo"></a>例 - imageInfo

次の例では、イメージ test.bmp の幅と高さを出力し、ピクセルあたりのビット数で色深度を指定しています。

```xpp
Image img = new Image(); 
container c; 
img.loadFile(@'C:\Test.bmp'); 
c = img.imageInfo(); 
print con2str(c); 
pause;
```

## <a name="method-imagespotlight"></a>メソッド imageSpotlight

センター座標 x および y で半径により定義された円内のスポットライト効果を生成します。

```xpp
public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)
```

### <a name="parameters---imagespotlight"></a>パラメーター - imageSpotlight

x  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

<!-- -->

y  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

<!-- -->

radius  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

<!-- -->

平滑化  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

<!-- -->

intensity  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

### <a name="return-value---imagespotlight"></a>戻り値 - imageSpotlight

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="remarks---imagespotlight"></a>備考 - imageSpotlight

円内のピクセルは変更されませんが、イメージ内の他のピクセルはその明度を減らすことで暗くなります。

## <a name="method-importbitmap"></a>メソッド importBitmap

hBitmap パラメータで指定されたイメージからビットマップをクローンします。

```xpp
public int importBitmap(Int64 hBitmap)
```

### <a name="parameters---importbitmap"></a>パラメーター - importBitmap

hBitmap  
複製する画像のハンドルです。

### <a name="return-value---importbitmap"></a>戻り値 - importBitmap

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="examples---importbitmap"></a>例 - importBitmap

次の例では、イメージのハンドルを取得してから、importBitmap メソッドを使用してイメージを複製します。

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

## <a name="method-importfileicon"></a>メソッド importFileIcon

ファイルに使用されているアイコンをコピーすることにより、fileName パラメーターで指定されたファイルからアイコンを作成します。

```xpp
public int importFileIcon(str fileName)
```

### <a name="parameters---importfileicon"></a>パラメーター - importFileIcon

fileName  
アイコンを作成するファイルの名前とパス。

### <a name="return-value---importfileicon"></a>戻り値 - importFileIcon

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="examples---importfileicon"></a>例 - importFileIcon

次の例では、ファイル test.bmp に使用されているアイコンをコピーします。

```xpp
Image img = new Image(); 
img.importFileIcon(@'C:\test.bmp'); 
img.clipboardCopy(); 
// Icon used for test.bmp can now be pasted into an application.
```

## <a name="method-importicon"></a>メソッド importIcon

実行可能ファイルからアイコンへのハンドルを取得します。 このアイコンは、fileName および iconIdx パラメーターで指定します。

```xpp
public int importIcon(str fileName, int iconIdx)
```

### <a name="parameters---importicon"></a>パラメーター - importIcon

fileName  
指定したファイル内のリソース。

<!-- -->

iconIdx  
指定したファイル内のリソース。

### <a name="return-value---importicon"></a>戻り値 - importIcon

0 は、成功を示し、それ以外の場合は、失敗を示します。

## <a name="method-loadimage"></a>メソッド loadImage

fileName パラメーターで指定されたファイルからイメージを読み込みます。

```xpp
public int loadImage(str fileName)
```

### <a name="parameters---loadimage"></a>パラメーター - loadImage

fileName  
画像を読み込む元となるリソース。

### <a name="return-value---loadimage"></a>戻り値 - loadImage

0 は、成功を示し、それ以外の場合は、失敗を示します。

## <a name="method-loadresource"></a>メソッド loadResource

パラメーター - validResource

```xpp
public int loadResource(int id)
```

### <a name="parameters---loadresource"></a>パラメーター - loadResource

id  
読み込むリソースの ID。 リソースの値は、Resources マクロにあります。

### <a name="return-value---loadresource"></a>戻り値 - loadResource

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="examples---loadresource"></a>例 - loadResource

次の例では、イメージ リストに 2つ のリソースを追加します。

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

## <a name="method-promotecolor"></a>メソッド promoteColor

画像の色深度を向上させます。

```xpp
public int promoteColor(int noOfColorBits)
```

### <a name="parameters---promotecolor"></a>パラメーター - promoteColor

noOfColorBits  
イメージのレベルを上げるビット数。

### <a name="return-value---promotecolor"></a>戻り値 - promoteColor

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="remarks---promotecolor"></a>備考 - promoteColor

このメソッドは次を推進します。

-   8 ビット画像を 24、32 ビットに。
-   4 ビット画像を 8、24、32 ビットに。
-   1 ビット画像を 4、8、24、32 ビットに。

### <a name="examples---promotecolor"></a>例 - promoteColor

次の例では、イメージの色深度が 8 ビット以上でない場合は、ピクセルあたり 8 ビットに増やしています。

```xpp
Image img = new Image(); 
img.loadFile(@'C:\test.bmp'); 
if (conpeek(img.imageInfo(),3) <8) 
{ 
    img.promoteColor(8); 
}
```

## <a name="method-reducecoloroctree"></a>メソッド reduceColorOctree

画像の色深度を減少させます。

```xpp
public int reduceColorOctree(int maxColors)
```

### <a name="parameters---reducecoloroctree"></a>パラメーター - reduceColorOctree

maxColors  
最大色数。

### <a name="return-value---reducecoloroctree"></a>戻り値 - reduceColorOctree

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="remarks---reducecoloroctree"></a>戻り値 - reduceColorOctree

このメソッドは、他の指示が maxColors パラメーターで指定されていない限り、24 ビット イメージを 8 ビットに、または 8 ビット イメージを 4 ビットに縮小します。 MaxColors パラメーターが 16 以下の場合は、4 ビット イメージが生成されます。 MaxColors が 16 を超える場合は、8 ビット画像が生成されます。

## <a name="method-removeimage"></a>メソッド removeImage

画像に関するデータを削除します。オブジェクトはまだ存在しますが、データを持ちません。

```xpp
public int removeImage()
```

### <a name="return-value---removeimage"></a>戻り値 - removeImage

0 は、成功を示し、それ以外の場合は、失敗を示します。

## <a name="method-resize"></a>メソッド resize

newWidth および newHeight パラメーターにより指定されたサイズに画像をサイズ変更します。

```xpp
public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)
```

### <a name="parameters---resize"></a>パラメーター - resize

newWidth  
resizing メソッド。

<!-- -->

newHeight  
resizing メソッド。

<!-- -->

InterpolationMode  
resizing メソッド。

### <a name="return-value---resize"></a>戻り値 - resize

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="remarks---resize"></a>備考 - resize

InterpolationMode パラメーターの使用可能な値は InterpolationMode システム列挙で使用可能な次の値です。

|     |                                      |                                                                                                                                                                        |
|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0   | InterpolationModeDefault             | 既定の補間モードを指定します。                                                                                                                              |
| 1   | InterpolationModeLowQuality          | 低品質モードを指定します。                                                                                                                                          |
| 2   | InterpolationModeHighQuality         | 高品質モードを指定します。                                                                                                                                         |
| 3   | InterpolationModeBilinear            | 線状補間を指定します。 事前フィルター処理は行われません。 このメソッドは、画像を元のサイズの 50％ 以下に縮小するのには適していません。                         |
| 4   | InterpolationModeBicubic             | バイキュービック補間を指定します。 事前フィルター処理は行われません。 このメソッドは、画像を元のサイズの 25％ 以下に縮小するのには適していません。                          |
| 5   | InterpolationModeNearestNeighbor     | ニアレストネイバー補間を指定します。                                                                                                                              |
| 6   | InterpolationModeHighQualityBilinear | 高品質な線状補間を指定します。 高品質圧縮を確実に行うため、事前フィルター処理が実行されます。                                                           |
| 7   | InterpolationModeHighQualityBicubic  | 高品質なバイキュービック補間を指定します。 高品質圧縮を確実に行うため、事前フィルター処理が実行されます。 このモードでは、最高品質の変換画像が生成されます。 |

## <a name="method-rotate"></a>メソッド rotate

画像を回転します。

```xpp
public int rotate(RotateType RotateType)
```

### <a name="parameters---rotate"></a>パラメータ - rotate

RotateType  
イメージを回転する量。

### <a name="return-value---rotate"></a>備考 - rotate

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="remarks---rotate"></a>備考 - rotate

RotateType パラメーターの使用可能な値は RotateType システム列挙で使用可能な次の値です。

|     |                    |                          |
|-----|--------------------|--------------------------|
| 0   | RotateNoneFlipNone | 回転なし。             |
| 1   | Rotate90FlipNone   | 90 度回転します。  |
| 2   | Rotate180FlipNone  | 180 度回転します。 |
| 3   | Rotate270FlipNone  | 270 度回転します。 |

## <a name="method-saveimage"></a>メソッド saveImage

指定されたファイル名に画像を保存します。

```xpp
public int saveImage(str fileName, [ImageSaveType Type])
```

### <a name="parameters---saveimage"></a>パラメーター - saveImage

fileName  
ファイル拡張子で指定された形式とは異なる形式でファイルを保存するように指定できる ImageSaveType (オプション)。

<!-- -->

種類  
ファイル拡張子で指定された形式とは異なる形式でファイルを保存するように指定できる ImageSaveType (オプション)。

### <a name="return-value---saveimage"></a>戻り値 - saveImage

メソッドが成功した場合、0 です。

### <a name="remarks---saveimage"></a>備考 - saveImage

Type パラメーターの使用可能な値は ImageSaveType システム列挙で使用可能な値です。 たとえば、.jpg ファイルとして test.bmp を保存することができます。

|     |                |
|-----|----------------|
| 0   | \_エクステンションの使用 |
| 1   | BMP            |
| 2   | GIF            |
| 3   | JPG            |
| 4   | PNG            |
| 5   | TIFF           |
| 6   | BMP\_UNCOMP    |
| 7   | TIF\_UNCOMP    |

### <a name="examples---saveimage"></a>例 - saveImage

次の例では、画面の一部をファイルにキャプチャし、その画像をロードします。

```xpp
Image img = new Image(); 
img.captureScreen(0, 0, 100, 100); 
img.saveImage(@'C:\test.bmp'); 
img.loadFile(@'C:\test.bmp');
```

## <a name="method-savetype"></a>メソッド saveType

イメージ デコーダを取得または設定します。

```xpp
public ImageSaveType saveType([ImageSaveType Type])
```

### <a name="parameters---savetype"></a>パラメーター - saveType

種類  
設定するデコーダのタイプ (オプション)。

### <a name="return-value---savetype"></a>戻り値 - saveType

### <a name="remarks---savetype"></a>備考 - saveType

Type パラメーターの使用可能な値は ImageSaveType システム列挙で使用可能な次の値です。

|     |                |
|-----|----------------|
| 0   | \_エクステンションの使用 |
| 1   | BMP            |
| 2   | GIF            |
| 3   | JPG            |
| 4   | PNG            |
| 5   | TIFF           |
| 6   | BMP\_UNCOMP    |
| 7   | TIF\_UNCOMP    |

## <a name="method-setpixel"></a>メソッド setPixel

x と y パラメーターで指定されているピクセルの色を設定します。

```xpp
public int setPixel(int x, int y, int pixel)
```

### <a name="parameters---setpixel"></a>パラメーター - setPixel

x  
使用する色の ARGB 値。

<!-- -->

y  
使用する色の ARGB 値。

<!-- -->

pixel  
使用する色の ARGB 値。

### <a name="return-value---setpixel"></a>備考 - setPixel

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="remarks---setpixel"></a>備考 - setPixel

RGB カラー値を ARGB 値に変換するには、Image::rgb メソッドを使用します。

## <a name="method-transparent"></a>メソッド transparent

画像の透明な色を設定します。

```xpp
public int transparent([boolean Set], [int RValue], [int GValue], [int BValue])
```

### <a name="parameters---transparent"></a>パラメーター - transparent

セット  
設定する色の青の値; オプション。

<!-- -->

RValue  
設定する色の青の値; オプション。

<!-- -->

GValue  
設定する色の青の値; オプション。

<!-- -->

BValue  
設定する色の青の値; オプション。

### <a name="return-value---transparent"></a>戻り値 - transparent

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="remarks---transparent"></a>備考 - transparent

入力パラメーターのいずれかがない場合は、画像内の位置 (0, 0) での色が使用されます。 色を指定する場合、パラメーター 2 から 4 を使用すると、RGB カラーとして表記されます。

## <a name="method-width"></a>メソッド width

ピクセル単位の画像の幅を取得します。

```xpp
public int width()
```

### <a name="return-value---width"></a>戻り値 - width

画像の幅をピクセル単位で表す整数。

### <a name="examples---width"></a>例 - width

次の例では、test.bmp ファイル内のイメージの幅を出力します。

```xpp
Image img = new Image(); 
img.loadFile(@'C:\test.bmp'); 
print img.width(); 
pause;
```

## <a name="method-canload"></a>メソッド canLoad

画像ファイルが存在し、開くことができるかどうかを決定します。

```xpp
public static int canLoad(str filename)
```

### <a name="parameters---canload"></a>パラメーター - canLoad

filename  
確認するファイルの名前とパス。

### <a name="return-value---canload"></a>戻り値 - canLoad

画像が検索され、開くことができる場合は 1、それ以外の場合、0 です。

## <a name="method-loadext"></a>メソッド loadExt

Image クラスでサポートされているファイル形式の拡張機能の一覧を取得します。

```xpp
public static container loadExt(int idx)
```

### <a name="parameters---loadext"></a>パラメーター - loadExt

idx  

### <a name="return-value---loadext"></a>戻り値 - loadExt

サポートされているファイル形式の一覧を保持するコンテナーです。

## <a name="method-resourcetype"></a>メソッド resourceType

特定のリソースがビットマップかアイコンかを判別します。

```xpp
public static int resourceType(int resourceIdx)
```

### <a name="parameters---resourcetype"></a>パラメーター - resourceType

resourceIdx  
読み込むリソースの ID。

### <a name="return-value---resourcetype"></a>戻り値 - resourceType

画像がビットマップの場合は 0、アイコンの場合は 1 です。

### <a name="remarks---resourcetype"></a>備考 - resourceType

リソースの値は、Resources マクロにあります。

### <a name="examples---resourcetype"></a>例 - resourceType

次の例では、リソース 3020 がアイコンかビットマップかどうかをテストします。

```xpp
Resource 
print Image::resourceType(3020); 
pause;
```

## <a name="method-rgb"></a>メソッド rgb

RGB 値を ARGB 値に変換します。

```xpp
public static int rgb(int R, int G, int B)
```

### <a name="parameters---rgb"></a>戻り値 - rgb

R  
色の青の値。

<!-- -->

G  
色の青の値。

<!-- -->

B  
色の青の値。

### <a name="return-value---rgb"></a>戻り値 - rgb

パラメーターで指定された色の ARGB 値を表す整数。

## <a name="method-validresource"></a>メソッド validResource

id パラメータで指定されたリソースが有効かどうかを判定します。

```xpp
public static int validResource(int id)
```

### <a name="parameters---validresource"></a>パラメーター - validResource

id  
チェックするリソースの ID。

### <a name="return-value---validresource"></a>戻り値 - validResource

ID が有効な場合、0 です。

## <a name="method-new"></a>メソッド new

新しい画像を作成します

```xpp
public void new([AnyType image], [int width], [int height])
```

### <a name="parameters---new"></a>パラメーター - new

画像  
ピクセル単位の画像の高さ (オプション)。

<!-- -->

width  
ピクセル単位の画像の高さ (オプション)。

<!-- -->

height  
ピクセル単位の画像の高さ (オプション)。

### <a name="remarks---new"></a>備考 - new

パラメーターを指定する必要はありませんが、イメージの内容とサイズを指定することができます。 画像パラメーターについては、ファイル名および場所、リソース、配列での特定の画像、または別の画像オブジェクトを指定できます。

### <a name="examples---new"></a>例 - new

次の例は、新しいイメージ オブジェクトの既存のコンテンツをオプションで指定する方法を示しています。

```xpp
Image img1 = new Image(@"C:\MyPicture.jpg", 100, 100); 
Image img2 = new Image(121,100, 100); // Uses resource 121 in Ax32.exe 
Image img4 = new Image(img1, 200, 200);
```

## <a name="method-displayorign"></a>メソッド displayOrign

オリジナルの発注元 (0, 0) から、オフセット (X, Y) を指定できるようにします。

```xpp
public void displayOrign(int Xpos, int Ypos)
```

### <a name="parameters---displayorign"></a>パラメーター - displayOrign

Xpos  
原点に対する新しい Y (垂直) 座標。

<!-- -->

Ypos  
原点に対する新しい Y (垂直) 座標。

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

