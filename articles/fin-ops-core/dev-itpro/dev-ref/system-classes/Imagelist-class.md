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
# <a name="class-imagelist"></a>クラス Imagelist

[!include [banner](../../includes/banner.md)]

```xpp
class Imagelist extends BinData
```

Imagelist クラスを使用すると、イメージの一覧を操作できます。

## <a name="remarks"></a>備考

1 つの画像を操作するには、イメージ クラスを使用します。

## <a name="examples"></a>例

次の例では、イメージ リストを作成し、Shell32.dll ファイルにアイコンを追加します。 一覧の 4 番目のメンバーを削除します。

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

## <a name="methods"></a>メソッド

| 方法                                                                         | 説明                                                                                                                        |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| public int add(Image image)                                                    | イメージ リストに新しい画像を追加します。                                                                                                |
| public boolean autoResize(\[boolean value\])                                   | 新しいイメージを自動的にサイズ変更するかどうかを決定するブール値の autoResize フラグを設定します。                                   |
| public int clear()                                                             | イメージ リストからすべての画像を削除します。                                                                                            |
| public int count()                                                             | 画像リスト内のイメージの数を取得します。                                                                                   |
| public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)             | イメージのドラッグを開始します。                                                                                                          |
| public boolean dragEnd()                                                       | ドラッグ操作を終了します。                                                                                                             |
| public boolean dragEnter(int hWnd, int x, int y)                               | ドラッグ操作中に指定されたウィンドウの更新をロックし、ウィンドウの指定された位置にドラッグ イメージを表示します。 |
| public boolean dragLeave(int hWnd)                                             | 指定したウィンドウのロックを解除し、ドラッグ イメージを非表示にして、ウィンドウを更新します。                                           |
| public boolean dragMove(int x, int y)                                          | ドラッグ アンド ドロップ操作中にドラッグされているイメージを移動します。                                                            |
| public boolean dragShowImage(boolean show)                                     | ドラッグされている画像の表示と非表示を切り替えます。                                                                                    |
| public int height()                                                            | イメージ リスト内のイメージの高さ (ピクセル単位) を取得します。                                                                  |
| public int loadIcons(str moduleName)                                           | イメージ リストに、指定されたリソースからアイコンを読み込みます。                                                                       |
| public int remove(int imageIdx)                                                | イメージ リストから画像を削除します。                                                                                               |
| public int replace(int imageIdx, Image image)                                  | リスト内の既存の画像を置き換えます。                                                                                            |
| public boolean setOverlayImage(int imageIdx, int overlayIdx)                   | オーバーレイ マスクとして使用する画像の一覧に、画像を追加します。                                                                       |
| public int width()                                                             | イメージ リスト内のイメージの幅 (ピクセル単位) を取得します。                                                                   |
| ::public static int iconHeight()                                               | 標準アイコンの高さのシステム メトリックを取得します。                                                                    |
| ::public static int iconWidth()                                                | 標準アイコンの幅のシステム メトリックを取得します。                                                                     |
| ::public static int smallIconHeight()                                          | 小さなアイコンの高さのシステム メトリックを取得します。                                                                       |
| ::public static int smallIconWidth()                                           | 小さなアイコンの幅のシステム メトリックを取得します。                                                                        |
| public void maskColor(int Color)                                               | マスキング色を設定します。                                                                                                            |
| public void draw(int HDC, int imageIdx, int x, int y, \[boolean transparent\]) | 指定されたデバイス コンテキストで画像リスト項目を描画します。                                                                          |
| public void finalize()                                                         |                                                                                                                                    |
| public void new(int cx, int cy, \[boolean transparent\])                       | 画像を保持する新しい空のリストを作成します。                                                                                           |

## <a name="method-add"></a>メソッド add

イメージ リストに新しい画像を追加します。

```xpp
public int add(Image image)
```

### <a name="parameters---add"></a>パラメーター - add

画像  
リストに追加する新しい画像。

### <a name="return-value---add"></a>戻り値 - add

メソッドが成功した場合、0 です。

### <a name="remarks---add"></a>備考 - add

autoResize メソッドを使用すると、リストに追加するときにイメージのサイズを自動的に変更することができます。

### <a name="examples---add"></a>例 - add

次の例では、新しいイメージ リストを作成し、3 つのイメージを追加します。

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

## <a name="method-autoresize"></a>メソッド autoResize

新しいイメージを自動的にサイズ変更するかどうかを決定するブール値の autoResize フラグを設定します。

```xpp
public boolean autoResize([boolean value])
```

### <a name="parameters---autoresize"></a>パラメーター - autoResize

値  
autoResize フラグが設定されているかどうかを示すブール値; オプション。

### <a name="return-value---autoresize"></a>戻り値 - autoResize

### <a name="remarks---autoresize"></a>備考 - autoResize

autoResize フラッグが true に設定されている場合、リストに追加する任意の画像サイズは、画像リストの作成時に指定された分析コードに自動的に再調整されます。

## <a name="method-clear"></a>メソッド clear

イメージ リストからすべての画像を削除します。

```xpp
public int clear()
```

### <a name="return-value---clear"></a>戻り値 - clear

メソッドが成功した場合、0 です。

## <a name="method-count"></a>メソッド count

画像リスト内のイメージの数を取得します。

```xpp
public int count()
```

### <a name="return-value---count"></a>戻り値 - count

リスト内の画像の数を表す整数。

### <a name="examples---count"></a>例 - count

次の例では、イメージ リストを作成し、shell.dll ファイルからアイコンを読み込み、リスト内のイメージの数を出力します。

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

## <a name="method-dragbegin"></a>メソッド dragBegin

イメージのドラッグを開始します。

```xpp
public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)
```

### <a name="parameters---dragbegin"></a>パラメーター - dragBegin

imageIdx  
画像の左上隅を基準とした、ドラッグ位置の Y 座標。

<!-- -->

hotSpotX  
画像の左上隅を基準とした、ドラッグ位置の Y 座標。

<!-- -->

hotSpotY  
画像の左上隅を基準とした、ドラッグ位置の Y 座標。

### <a name="return-value---dragbegin"></a>戻り値 - dragBegin

メソッドが成功した場合は 1 です。

### <a name="remarks---dragbegin"></a>備考 - dragBegin

残りのドラッグ操作は、dragEnter、dragMove、dragLeave、dragEnd の各メソッドで指定します。

## <a name="method-dragend"></a>メソッド dragEnd

ドラッグ操作を終了します。

```xpp
public boolean dragEnd()
```

### <a name="return-value---dragend"></a>戻り値 - dragEnd

メソッドが成功した場合は 1、それ以外の場合は 0 です。

### <a name="remarks---dragend"></a>備考 - dragEnd

残りのドラッグ操作は、dragBegin、dragEnter、dragMove、dragLeave の各メソッドで指定します。

## <a name="method-dragenter"></a>メソッド dragEnter

ドラッグ操作中に指定されたウィンドウの更新をロックし、ウィンドウの指定された位置にドラッグ イメージを表示します。

```xpp
public boolean dragEnter(int hWnd, int x, int y)
```

### <a name="parameters---dragenter"></a>パラメーター - dragEnter

hWnd  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

<!-- -->

x  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

<!-- -->

y  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

### <a name="return-value---dragenter"></a>戻り値 - dragEnter

メソッドが成功した場合は 1、それ以外の場合は 0 です。

### <a name="remarks---dragenter"></a>備考 - dragEnter

ドラッグ操作を開始するには、dragBegin メソッドを呼び出します。 残りのドラッグ操作は、dragMove、dragLeave、dragEnd の各メソッドで指定します。

## <a name="method-dragleave"></a>メソッド dragLeave

指定したウィンドウのロックを解除し、ドラッグ イメージを非表示にして、ウィンドウを更新します。

```xpp
public boolean dragLeave(int hWnd)
```

### <a name="parameters---dragleave"></a>パラメーター - dragLeave

hWnd  
ドラッグ イメージを所有するウィンドウのハンドルです。

### <a name="return-value---dragleave"></a>戻り値 - dragLeave

メソッドが成功した場合は 1、それ以外の場合は 0 です。

### <a name="remarks---dragleave"></a>備考 - dragLeave

残りのドラッグ操作は、dragBegin、dragEnter、dragMove、dragEnd の各メソッドで指定します。

## <a name="method-dragmove"></a>メソッド dragMove

ドラッグ アンド ドロップ操作中にドラッグされているイメージを移動します。

```xpp
public boolean dragMove(int x, int y)
```

### <a name="parameters---dragmove"></a>パラメーター - dragMove

x  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

<!-- -->

y  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

### <a name="return-value---dragmove"></a>戻り値 - dragMove

メソッドが成功した場合は 1、それ以外の場合は 0 です。

### <a name="remarks---dragmove"></a>備考 - dragMove

ドラッグ操作を開始するには、dragBegin メソッドを呼び出してから dragEnter メソッドを呼び出します。 残りのドラッグ操作は、dragLeave メソッドおよび dragEnd メソッドで指定します。

## <a name="method-dragshowimage"></a>メソッド dragShowImage

ドラッグされている画像の表示と非表示を切り替えます。

```xpp
public boolean dragShowImage(boolean show)
```

### <a name="parameters---dragshowimage"></a>パラメーター - dragShowImage

show  
画像を表示するかどうかを指定する値。

### <a name="return-value---dragshowimage"></a>戻り値 - dragShowImage

## <a name="method-height"></a>メソッド height

イメージ リスト内のイメージの高さ (ピクセル単位) を取得します。

```xpp
public int height()
```

### <a name="return-value---height"></a>戻り値 - height

画像の高さをピクセル単位で表す整数。

### <a name="remarks---height"></a>備考 - height

リスト内の画像の高さは、リストをインスタンス化するときに設定されます。

### <a name="examples---height"></a>例 - height

次の例では、イメージ リストを作成し、イメージの高さと幅を iconWidth メソッドと iconHeight メソッドで指定された寸法に設定します。 一覧内のイメージの高さを出力します。

```xpp
Imagelist list; 
list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight()); 
print list.height();   
pause;
```

## <a name="method-loadicons"></a>メソッド loadIcons

イメージ リストに、指定されたリソースからアイコンを読み込みます。

```xpp
public int loadIcons(str moduleName)
```

### <a name="parameters---loadicons"></a>パラメーター - loadIcons

moduleName  
イメージの読み込み元ファイルの名前。

### <a name="return-value---loadicons"></a>戻り値 - loadIcons

メソッドが成功した場合、0 です。

### <a name="examples---loadicons"></a>例 - loadIcons

次の例では、イメージのリストを作成し、shell32.dll ファイルに含まれるイメージをロードします。

```xpp
Imagelist list; 
list = new Imagelist(Imagelist::iconWidth(),Imagelist::iconHeight()); 
list.loadIcons('shell32.dll');
```

## <a name="method-remove"></a>メソッド remove

イメージ リストから画像を削除します。

```xpp
public int remove(int imageIdx)
```

### <a name="parameters---remove"></a>パラメーター - remove

imageIdx  
一覧から削除する画像の位置。

### <a name="return-value---remove"></a>戻り値 - remove

メソッドが成功した場合、0 です。

### <a name="examples---remove"></a>例 - remove

次の例では、イメージ リストを作成し、アイコンを shell32.dll ファイルに追加して、リストの 4 番目のメンバーを削除します。

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

## <a name="method-replace"></a>メソッド replace

リスト内の既存の画像を置き換えます。

```xpp
public int replace(int imageIdx, Image image)
```

### <a name="parameters---replace"></a>パラメーター - replace

imageIdx  
既存のイメージを置き換えるために使用するイメージ。

<!-- -->

画像  
既存のイメージを置き換えるために使用するイメージ。

### <a name="return-value---replace"></a>戻り値 - replace

メソッドが成功した場合、0 です。

## <a name="method-setoverlayimage"></a>メソッド setOverlayImage

オーバーレイ マスクとして使用する画像の一覧に、画像を追加します。

```xpp
public boolean setOverlayImage(int imageIdx, int overlayIdx)
```

### <a name="parameters---setoverlayimage"></a>パラメーター - setOverlayImage

imageIdx  
オーバーレイ マスクの 1 から始まるインデックス。

<!-- -->

overlayIdx  
オーバーレイ マスクの 1 から始まるインデックス。

### <a name="return-value---setoverlayimage"></a>戻り値 - setOverlayImage

メソッドが成功した場合は 1 です。

### <a name="examples---setoverlayimage"></a>例 - setOverlayImage

次の例では、3 つのイメージを持つイメージ リストを作成し、最後のイメージをオーバーレイ マスクとして設定します。

```xpp
Imagelist list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight() ); 
list.add(new Image(824)); // Image 0 
list.add(new Image(815)); // Image 1 
list.add(new Image(936)); //Image 2 
list.setOverlayImage (2,1);
```

## <a name="method-width"></a>メソッド width

イメージ リスト内のイメージの幅 (ピクセル単位) を取得します。

```xpp
public int width()
```

### <a name="return-value---width"></a>戻り値 - width

画像の幅をピクセル単位で表す整数。

### <a name="remarks---width"></a>備考 - width

リスト内の画像の幅は、リストをインスタンス化するときに設定されます。

### <a name="examples---width"></a>例 - width

次の例では、アイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの幅をリストに出力します。

```xpp
Imagelist list; 
list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight()); 
print list.width();   
pause;
```

## <a name="method-iconheight"></a>メソッド iconHeight

標準アイコンの高さのシステム メトリックを取得します。

```xpp
public static int iconHeight()
```

### <a name="return-value---iconheight"></a>戻り値 - iconHeight

標準アイコンの高さを表す整数。

### <a name="examples---iconheight"></a>例 - iconHeight

次の例では、イメージのリストを作成し、標準のアイコンの幅と高さに設定します。

```xpp
ImageList list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight());
```

## <a name="method-iconwidth"></a>メソッド iconWidth

標準アイコンの幅のシステム メトリックを取得します。

```xpp
public static int iconWidth()
```

### <a name="return-value---iconwidth"></a>戻り値 - iconWidth

標準アイコンの幅を表す整数。

### <a name="examples---iconwidth"></a>例 - iconWidth

次の例では、イメージのリストを作成し、標準のアイコンの幅と高さに設定します。

```xpp
ImageList list = new Imagelist( 
    Imagelist::iconWidth(), 
    Imagelist::iconHeight());
```

## <a name="method-smalliconheight"></a>メソッド smallIconHeight

小さなアイコンの高さのシステム メトリックを取得します。

```xpp
public static int smallIconHeight()
```

### <a name="return-value---smalliconheight"></a>戻り値 - smallIconHeight

小さなアイコンの高さを表す整数。

### <a name="examples---smalliconheight"></a>例 - smallIconHeight

次の例では、小さなアイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの高さをリストに出力します。

```xpp
Imagelist list = new Imagelist( 
    Imagelist::smallIconWidth(), 
    Imagelist::smallIconHeight()); 
print list.height();   
pause;
```

## <a name="method-smalliconwidth"></a>メソッド smallIconWidth

小さなアイコンの幅のシステム メトリックを取得します。

```xpp
public static int smallIconWidth()
```

### <a name="return-value---smalliconwidth"></a>戻り値 - smallIconWidth

小さなアイコンの幅を表す整数。

### <a name="examples---smalliconwidth"></a>例 - smallIconWidth

次の例では、小さなアイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの幅をリストに出力します。

```xpp
Imagelist list = new Imagelist( 
   Imagelist::smallIconWidth(), 
   Imagelist::smallIconHeight()); 
print list.width();   
pause;
```

## <a name="method-maskcolor"></a>メソッド maskColor

マスキング色を設定します。

```xpp
public void maskColor(int Color)
```

### <a name="parameters---maskcolor"></a>パラメーター - maskColor

色  
ARGB 値としての色。

## <a name="method-draw"></a>メソッド draw

指定されたデバイス コンテキストで画像リスト項目を描画します。

```xpp
public void draw(int HDC, int imageIdx, int x, int y, [boolean transparent])
```

### <a name="parameters---draw"></a>パラメーター - draw

HDC  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

<!-- -->

imageIdx  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

<!-- -->

x  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

<!-- -->

y  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

<!-- -->

透明  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

画像を保持する新しい空のリストを作成します。

```xpp
public void new(int cx, int cy, [boolean transparent])
```

### <a name="parameters---new"></a>パラメーター - new

cx  

<!-- -->

cy  

<!-- -->

透明  

### <a name="remarks---new"></a>備考 - new

autoResize メソッドを使用すると、リストに追加するときにイメージのサイズを自動的に変更することができます。

### <a name="examples---new"></a>例 - new

次の例では、標準アイコンの幅と高さの項目を保持するイメージ リストを作成します。

```xpp
Imagelist list; 
list = new Imagelist( 
   Imagelist::iconWidth(), 
   Imagelist::iconHeight());
```

