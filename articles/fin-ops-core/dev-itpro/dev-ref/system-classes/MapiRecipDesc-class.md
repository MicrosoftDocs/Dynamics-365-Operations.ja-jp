---
title: MapiRecipDesc クラス
description: このトピックでは、MapiRecipDesc クラスについて説明します。
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
ms.openlocfilehash: 9ac4acbacaa3a4f82247ab9448e37a8fcc21e07b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502578"
---
# <a name="class-mapirecipdesc"></a>クラス MapiRecipDesc

[!include [banner](../../includes/banner.md)]

```xpp
class MapiRecipDesc extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                    | 説明                                                                                                                                   |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str address(\[str Address\])       |                                                                                                                                               |
| public str name(\[str Name\])             | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int recipClass(\[int RecipClass\]) |                                                                                                                                               |
| public void new()                         | MapiRecipDesc クラスの新しいインスタンスを初期化します。                                                                                        |
| public void finalize()                    |                                                                                                                                               |

## <a name="method-address"></a>メソッド address

```xpp
public str address([str Address])
```

### <a name="parameters---address"></a>パラメーター - address

アドレス  

### <a name="return-value---address"></a>戻り値 - address

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str Name])
```

### <a name="parameters---name"></a>パラメーター - name

氏名  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-recipclass"></a>メソッド recipClass

```xpp
public int recipClass([int RecipClass])
```

### <a name="parameters---recipclass"></a>パラメーター - recipClass

RecipClass  

### <a name="return-value---recipclass"></a>戻り値 - recipClass

## <a name="method-new"></a>メソッド new

MapiRecipDesc クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

