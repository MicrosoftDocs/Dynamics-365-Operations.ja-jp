---
title: FormTreeItem クラス
description: このトピックでは、FormTreeItem クラスについて説明します。
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
ms.openlocfilehash: 43ab30c19eaaffb3f379971e548b32567c68d714
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502909"
---
# <a name="class-formtreeitem"></a>クラス FormTreeItem

[!include [banner](../../includes/banner.md)]

```xpp
class FormTreeItem extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                           | 説明                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| public int children(\[int value\])                                               |                                                                            |
| public AnyType data(\[AnyType value\])                                           |                                                                            |
| public int idx()                                                                 |                                                                            |
| public int image(\[int value\])                                                  |                                                                            |
| public int overlayImage(\[int value\])                                           |                                                                            |
| public int selectedImage(\[int value\])                                          |                                                                            |
| public boolean stateBold(\[boolean value\])                                      |                                                                            |
| public FormTreeCheckedState stateChecked(\[FormTreeCheckedState value\])         |                                                                            |
| public boolean stateCut(\[boolean value\])                                       |                                                                            |
| public boolean stateDropHilited(\[boolean value\])                               |                                                                            |
| public boolean stateExpanded(\[boolean value\])                                  |                                                                            |
| public boolean stateExpandedOnce(\[boolean value\])                              |                                                                            |
| public int stateImage(\[int value\])                                             |                                                                            |
| public boolean stateSelected(\[boolean value\])                                  |                                                                            |
| public str text(\[str value\])                                                   | コントロールのテキストを設定するか返します。                                  |
| public str toString()                                                            | FormTreeItem クラスのインスタンスの文字列表現を返します。 |
| public void new(\[str Text\], \[int Image\], \[int children\], \[AnyType Data\]) | Object クラスの新しいインスタンスを初期化します。                            |
| public void finalize()                                                           |                                                                            |

## <a name="method-children"></a>メソッド children

```xpp
public int children([int value])
```

### <a name="parameters---children"></a>パラメーター - children

値  

### <a name="return-value---children"></a>戻り値 - children

## <a name="method-data"></a>メソッド data

```xpp
public AnyType data([AnyType value])
```

### <a name="parameters---data"></a>パラメーター - data

値  

### <a name="return-value---data"></a>戻り値 - data

## <a name="method-idx"></a>メソッド idx

```xpp
public int idx()
```

### <a name="return-value---idx"></a>戻り値 - idx

## <a name="method-image"></a>メソッド image

```xpp
public int image([int value])
```

### <a name="parameters---image"></a>パラメーター - image

値  

### <a name="return-value---image"></a>戻り値 - image

## <a name="method-overlayimage"></a>メソッド overlayImage

```xpp
public int overlayImage([int value])
```

### <a name="parameters---overlayimage"></a>パラメーター - overlayImage

値  

### <a name="return-value---overlayimage"></a>戻り値 - overlayImage

## <a name="method-selectedimage"></a>メソッド selectedImage

```xpp
public int selectedImage([int value])
```

### <a name="parameters---selectedimage"></a>パラメーター - selectedImage

値  

### <a name="return-value---selectedimage"></a>戻り値 - selectedImage

## <a name="method-statebold"></a>メソッド stateBold

```xpp
public boolean stateBold([boolean value])
```

### <a name="parameters---statebold"></a>パラメーター - stateBold

値  

### <a name="return-value---statebold"></a>戻り値 - stateBold

## <a name="method-statechecked"></a>メソッド stateChecked

```xpp
public FormTreeCheckedState stateChecked([FormTreeCheckedState value])
```

### <a name="parameters---statechecked"></a>パラメーター - stateChecked

値  

### <a name="return-value---statechecked"></a>戻り値 - stateChecked

## <a name="method-statecut"></a>メソッド stateCut

```xpp
public boolean stateCut([boolean value])
```

### <a name="parameters---statecut"></a>パラメーター - stateCut

値  

### <a name="return-value---statecut"></a>戻り値 - stateCut

## <a name="method-statedrophilited"></a>メソッド stateDropHilited

```xpp
public boolean stateDropHilited([boolean value])
```

### <a name="parameters---statedrophilited"></a>パラメーター - stateDropHilited

値  

### <a name="return-value---statedrophilited"></a>戻り値 - stateDropHilited

## <a name="method-stateexpanded"></a>メソッド stateExpanded

```xpp
public boolean stateExpanded([boolean value])
```

### <a name="parameters---stateexpanded"></a>パラメーター - stateExpanded

値  

### <a name="return-value---stateexpanded"></a>戻り値 - stateExpanded

## <a name="method-stateexpandedonce"></a>メソッド stateExpandedOnce

```xpp
public boolean stateExpandedOnce([boolean value])
```

### <a name="parameters---stateexpandedonce"></a>戻り値 - stateExpandedOnce

値  

### <a name="return-value---stateexpandedonce"></a>戻り値 - stateExpandedOnce

## <a name="method-stateimage"></a>メソッド stateImage

```xpp
public int stateImage([int value])
```

### <a name="parameters---stateimage"></a>パラメーター - stateImage

値  

### <a name="return-value---stateimage"></a>戻り値 - stateImage

## <a name="method-stateselected"></a>メソッド stateSelected

```xpp
public boolean stateSelected([boolean value])
```

### <a name="parameters---stateselected"></a>パラメーター - stateSelected

値  

### <a name="return-value---stateselected"></a>戻り値 - stateSelected

## <a name="method-text"></a>メソッド text

コントロールのテキストを設定するか返します。

```xpp
public str text([str value])
```

### <a name="parameters---text"></a>パラメーター - text

値  
コントロールのテキストとして割り当てる値 (オプション)。

### <a name="return-value---text"></a>戻り値 - text

コントロールのテキスト。コントロールにテキストが割り当てられていない場合は空の文字列。

## <a name="method-tostring"></a>メソッド toString

FormTreeItem クラスのインスタンスの文字列表現を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

FormTreeItem クラスのインスタンスの説明を含む文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。

### <a name="examples---tostring"></a>例 - toString

次の例は、toString メソッドの使用方法を示しています。

```xpp
print objFormTreeItem.toString();
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new([str Text], [int Image], [int children], [AnyType Data])
```

### <a name="parameters---new"></a>パラメーター - new

テキスト  

<!-- -->

画像  

<!-- -->

children  

<!-- -->

データ  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

