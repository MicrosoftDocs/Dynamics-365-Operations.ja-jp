---
title: FormPart クラス
description: このトピックでは、FormPart クラスについて説明します。
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
ms.openlocfilehash: da0592a0b720a9e64cf16d609f0d4ce577e398b3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502913"
---
# <a name="class-formpart"></a>クラス FormPart

[!include [banner](../../includes/banner.md)]

```xpp
class FormPart extends TreeNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                       | 説明                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str caption(\[str value\])            | コントロールのキャプションを取得または設定します。                                                                                                   |
| public str form(\[str value\])               |                                                                                                                                           |
| public str managedContentItem(\[str value\]) |                                                                                                                                           |
| public str name(\[str value\])               | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])           |                                                                                                                                           |
| public void new()                            | FormPart クラスの新しいインスタンスを初期化します。                                                                                         |

## <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a>パラメーター - caption

値  

### <a name="return-value---caption"></a>戻り値 - caption

コントロールのキャプションとして使用される文字列。

## <a name="method-form"></a>メソッド form

```xpp
public str form([str value])
```

### <a name="parameters---form"></a>パラメーター - form

値  

### <a name="return-value---form"></a>戻り値 - form

## <a name="method-managedcontentitem"></a>メソッド managedContentItem

```xpp
public str managedContentItem([str value])
```

### <a name="parameters---managedcontentitem"></a>パラメーター - managedContentItem

値  

### <a name="return-value---managedcontentitem"></a>戻り値 - managedContentItem

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-new"></a>メソッド new

FormPart クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

