---
title: WebMenu クラス
description: このトピックでは、WebMenu クラスについて説明します。
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
ms.openlocfilehash: b4bb194e176a806723891d8ded07513e6a1e7c2e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503004"
---
# <a name="class-webmenu"></a>クラス WebMenu

[!include [banner](../../includes/banner.md)]

```xpp
class WebMenu extends TreeNode
```

WebMenu クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                   | 説明                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])                                      | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])                                  | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                 |
| public str changedTime(\[str value\])                                    | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                 |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\]) | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                           |
| public str createdBy(\[str value\])                                      | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])                                 | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                      |
| public str creationTime(\[str value\])                                   |                                                                                                                                               |
| public boolean highlightSelected(\[boolean value\])                      |                                                                                                                                               |
| public str label(\[str value\])                                          | コントロールのラベルを取得または設定します。                                                                                                         |
| public str menuItemName(\[str value\])                                   |                                                                                                                                               |
| public WebMenuItemType menuItemType(\[WebMenuItemType value\])           |                                                                                                                                               |
| public str menuName()                                                    |                                                                                                                                               |
| public str name(\[str value\])                                           | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededAccessLevel(\[int value\])                              | MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。                                                                       |
| public Guid origin(\[Guid value\])                                       |                                                                                                                                               |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                |                                                                                                                                               |
| public boolean setCompany(\[boolean value\])                             |                                                                                                                                               |
| public boolean showParentModule(\[boolean value\])                       |                                                                                                                                               |
| public str webTarget(\[str value\])                                      |                                                                                                                                               |
| public void addSeparator()                                               |                                                                                                                                               |
| public void makeMenu(Object outputClass)                                 |                                                                                                                                               |
| public void addSubmenu(str name)                                         |                                                                                                                                               |
| public void new(str Name)                                                | TreeNode クラスの新しいインスタンスを初期化します。                                                                                             |
| public void addMenuitem(WebMenuFunction webMenuFunction)                 |                                                                                                                                               |

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

コントロールに割り当てられるコンフィギュレーションの ID。

### <a name="remarks---configurationkey"></a>備考 - configurationKey

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  

### <a name="return-value---creationdate"></a>戻り値 - creationDate

アプリケーション オブジェクトが作成された日付。

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-highlightselected"></a>メソッド highlightSelected

```xpp
public boolean highlightSelected([boolean value])
```

### <a name="parameters---highlightselected"></a>パラメーター - highlightSelected

値  

### <a name="return-value---highlightselected"></a>戻り値 - highlightSelected

## <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

```xpp
public str label([str value])
```

### <a name="parameters---label"></a>パラメーター - label

値  

### <a name="return-value---label"></a>戻り値 - label

ラベル文字列の現在の値。

### <a name="remarks---label"></a>備考 - label

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

## <a name="method-menuitemname"></a>メソッド menuItemName

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a>パラメーター - menuItemName

値  

### <a name="return-value---menuitemname"></a>戻り値 - menuItemName

## <a name="method-menuitemtype"></a>メソッド menuItemType

```xpp
public WebMenuItemType menuItemType([WebMenuItemType value])
```

### <a name="parameters---menuitemtype"></a>パラメーター - menuItemType

値  

### <a name="return-value---menuitemtype"></a>戻り値 - menuItemType

## <a name="method-menuname"></a>メソッド menuName

```xpp
public str menuName()
```

### <a name="return-value---menuname"></a>戻り値 - menuName

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

## <a name="method-neededaccesslevel"></a>メソッド neededAccessLevel

MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。

```xpp
public int neededAccessLevel([int value])
```

### <a name="parameters---neededaccesslevel"></a>パラメーター - neededAccessLevel

値  

### <a name="return-value---neededaccesslevel"></a>戻り値 - neededAccessLevel

neededAccessLevel プロパティの現在の値。

### <a name="remarks---neededaccesslevel"></a>備考 - neededAccessLevel

AccessType システム列挙値の使用可能な値は次のとおりです。

-   AccessType::NoAccess
-   AccessType::View
-   AccessType::Edit
-   AccessType::Add
-   AccessType::Delete

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-securitykey"></a>メソッド securityKey

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  

### <a name="return-value---securitykey"></a>戻り値 - securityKey

## <a name="method-setcompany"></a>メソッド setCompany

```xpp
public boolean setCompany([boolean value])
```

### <a name="parameters---setcompany"></a>パラメーター - setCompany

値  

### <a name="return-value---setcompany"></a>戻り値 - setCompany

## <a name="method-showparentmodule"></a>メソッド showParentModule

```xpp
public boolean showParentModule([boolean value])
```

### <a name="parameters---showparentmodule"></a>パラメーター - showParentModule

値  

### <a name="return-value---showparentmodule"></a>戻り値 - showParentModule

## <a name="method-webtarget"></a>メソッド webTarget

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a>パラメーター - webTarget

値  

### <a name="return-value---webtarget"></a>戻り値 - webTarget

## <a name="method-addseparator"></a>メソッド addSeparator

```xpp
public void addSeparator()
```

## <a name="method-makemenu"></a>メソッド makeMenu

```xpp
public void makeMenu(Object outputClass)
```

### <a name="parameters---makemenu"></a>パラメーター - makeMenu

outputClass  

## <a name="method-addsubmenu"></a>メソッド addSubmenu

```xpp
public void addSubmenu(str name)
```

### <a name="parameters---addsubmenu"></a>パラメーター - addSubmenu

名前  

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new(str Name)
```

### <a name="parameters---new"></a>パラメーター - new

氏名  

## <a name="method-addmenuitem"></a>メソッド addMenuitem

```xpp
public void addMenuitem(WebMenuFunction webMenuFunction)
```

### <a name="parameters---addmenuitem"></a>パラメーター - addMenuitem

webMenuFunction  

