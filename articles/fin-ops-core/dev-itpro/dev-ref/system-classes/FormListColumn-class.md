---
title: FormListColumn クラス
description: このトピックでは、FormListColumn クラスについて説明します。
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
ms.openlocfilehash: 7bb4e5433514521e310182ddb33c7b4bbaf4e46e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502931"
---
# <a name="class-formlistcolumn"></a>クラス FormListColumn

[!include [banner](../../includes/banner.md)]

```xpp
class FormListColumn extends Object
```

FormListColumn クラスは、フォームのリスト列機能を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                      | 説明                                               |
|-------------------------------------------------------------|-----------------------------------------------------------|
| public FormListFormat format(\[FormListFormat value\])      |                                                           |
| public int image(\[int value\])                             |                                                           |
| public int order(\[int value\])                             |                                                           |
| public int subItem(\[int value\])                           |                                                           |
| public str text(\[str value\])                              |                                                           |
| public str toString()                                       | クラス ハンドルと名前を含む文字列を返します。 |
| public int width(\[int value\])                             | コントロールの幅を取得または設定します。                    |
| public void new(\[str Text\], \[int ColNo\], \[int Width\]) | Object クラスの新しいインスタンスを初期化します。           |
| public void finalize()                                      |                                                           |

## <a name="method-format"></a>メソッド format

```xpp
public FormListFormat format([FormListFormat value])
```

### <a name="parameters---format"></a>パラメーター - format

値  

### <a name="return-value---format"></a>戻り値 - format

## <a name="method-image"></a>メソッド image

```xpp
public int image([int value])
```

### <a name="parameters---image"></a>パラメーター - image

値  

### <a name="return-value---image"></a>戻り値 - image

## <a name="method-order"></a>メソッド order

```xpp
public int order([int value])
```

### <a name="parameters---order"></a>パラメーター - order

値  

### <a name="return-value---order"></a>戻り値 - order

## <a name="method-subitem"></a>メソッド subItem

```xpp
public int subItem([int value])
```

### <a name="parameters---subitem"></a>パラメーター - subItem

値  

### <a name="return-value---subitem"></a>戻り値 - subItem

## <a name="method-text"></a>メソッド text

```xpp
public str text([str value])
```

### <a name="parameters---text"></a>パラメーター - text

値  

### <a name="return-value---text"></a>戻り値 - text

## <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前を含む文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

クラスのテキスト表現。

## <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

```xpp
public int width([int value])
```

### <a name="parameters---width"></a>パラメーター - width

値  
リストの列幅として割り当てる値 (オプション)。

### <a name="return-value---width"></a>戻り値 - width

ピクセル単位のコントロールの幅。

### <a name="remarks---width"></a>備考 - width

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します。

| モード             | 幅計算                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| -1 � 正確       | コントロールのピクセル単位の正確な幅が使用されます。                                         |
| 0 � 自動         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 � 列の幅 | フォームのレイアウトによって、コントロールの幅が決まります。                               |

幅と幅計算モードは別々に設定できます。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new([str Text], [int ColNo], [int Width])
```

### <a name="parameters---new"></a>パラメーター - new

テキスト  

<!-- -->

ColNo  

<!-- -->

Width  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

