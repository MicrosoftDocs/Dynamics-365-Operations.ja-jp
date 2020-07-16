---
title: MenuItem クラス
description: このトピックでは､MenuItem クラスについて説明します。
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
ms.openlocfilehash: a4e6bf5ee11fa90aaa588becc193b1e34e35df04
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502577"
---
# <a name="class-menuitem"></a>クラス MenuItem

[!include [banner](../../includes/banner.md)]

```xpp
class MenuItem extends TreeNode
```

MenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

メニュー項目は、メニュー機能のユーザー インターフェイスを表します。 メニュー項目は、ユーザーがメニュー項目を選択するときに実行される MenuFunction オブジェクトにリンクされます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str allowRootNavigation(\[str value\])              |                                                                                                                                               |
| public boolean isDisplayedInContentArea(\[boolean value\]) |                                                                                                                                               |
| public str label(\[str name\])                             |                                                                                                                                               |
| public str menuFunctionName(\[str name\])                  |                                                                                                                                               |
| public str menuItemName(\[str value\])                     |                                                                                                                                               |
| public MenuItemType menuItemType(\[MenuItemType value\])   |                                                                                                                                               |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public str parameter(\[str parameter\])                    |                                                                                                                                               |
| public str parameters(\[str value\])                       | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                        |
| public str shortCut(\[str value\])                         |                                                                                                                                               |
| public boolean showParentModule(\[boolean value\])         |                                                                                                                                               |
| public boolean visible(\[boolean value\])                  |                                                                                                                                               |
| public str webTarget(\[str value\])                        |                                                                                                                                               |

## <a name="method-allowrootnavigation"></a>メソッド allowRootNavigation

```xpp
public str allowRootNavigation([str value])
```

### <a name="parameters---allowrootnavigation"></a>パラメーター - allowRootNavigation

値  

### <a name="return-value---allowrootnavigation"></a>戻り値 - allowRootNavigation

## <a name="method-isdisplayedincontentarea"></a>メソッド isDisplayedInContentArea

```xpp
public boolean isDisplayedInContentArea([boolean value])
```

### <a name="parameters---isdisplayedincontentarea"></a>パラメーター - isDisplayedInContentArea

値  

### <a name="return-value---isdisplayedincontentarea"></a>戻り値 - isDisplayedInContentArea

## <a name="method-label"></a>メソッド label

```xpp
public str label([str name])
```

### <a name="parameters---label"></a>パラメーター - label

名前  

### <a name="return-value---label"></a>戻り値 - label

## <a name="method-menufunctionname"></a>メソッド menuFunctionName

```xpp
public str menuFunctionName([str name])
```

### <a name="parameters---menufunctionname"></a>パラメーター - menuFunctionName

名前  

### <a name="return-value---menufunctionname"></a>戻り値 - menuFunctionName

## <a name="method-menuitemname"></a>メソッド menuItemName

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a>パラメーター - menuItemName

値  

### <a name="return-value---menuitemname"></a>戻り値 - menuItemName

## <a name="method-menuitemtype"></a>メソッド menuItemType

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a>パラメーター - menuItemType

値  

### <a name="return-value---menuitemtype"></a>戻り値 - menuItemType

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

## <a name="method-parameter"></a>メソッド parameter

```xpp
public str parameter([str parameter])
```

### <a name="parameters---parameter"></a>パラメーター - parameter

パラメーター  

### <a name="return-value---parameter"></a>戻り値 - パラメータ

## <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a>パラメーター - parameters

値  

### <a name="return-value---parameters"></a>戻り値 - parameters

オブジェクトに渡されるパラメーターのリスト。

### <a name="remarks---parameters"></a>備考 - パラメータ

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

## <a name="method-shortcut"></a>メソッド shortCut

```xpp
public str shortCut([str value])
```

### <a name="parameters---shortcut"></a>パラメーター - shortCut 

値  

### <a name="return-value---shortcut"></a>戻り値 - shortCut

## <a name="method-showparentmodule"></a>メソッド showParentModule

```xpp
public boolean showParentModule([boolean value])
```

### <a name="parameters---showparentmodule"></a>パラメーター - showParentModule

値  

### <a name="return-value---showparentmodule"></a>戻り値 - showParentModule

## <a name="method-visible"></a>メソッド visible

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  

### <a name="return-value---visible"></a>戻り値 - visible

## <a name="method-webtarget"></a>メソッド webTarget

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a>パラメーター - webTarget

値  

### <a name="return-value---webtarget"></a>戻り値 - webTarget

