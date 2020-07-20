---
title: Menu クラス
description: このトピックでは､Menu クラスについて説明します。
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
ms.openlocfilehash: aeeff8db3a02c8246550fa6f0a2a71c1f8bfc3ca
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502576"
---
# <a name="class-menu"></a>クラス メニュー

[!include [banner](../../includes/banner.md)]

```xpp
class Menu extends TreeNode
```

メニュー システム クラスを使用すると、メニュー オブジェクトのいずれかをコードから構成および実行できます。

## <a name="remarks"></a>備考

TreeNode システム クラスは、アプリケーション オブジェクト ツリー (AOT) で、メニューへのより一般的なアプローチとして機能します。 サブメニューやメニュー項目などのメニュー内容を作成または操作するには、Menu クラスを使用します。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                   | 説明                                                                                                               |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])                                      | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                |
| public Date changedDate(\[Date value\])                                  | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                             |
| public str changedTime(\[str value\])                                    | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\]) | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                       |
| public str countryRegionCodes(\[str value\])                             |                                                                                                                           |
| public str createdBy(\[str value\])                                      | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                     |
| public Date creationDate(\[Date value\])                                 | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                  |
| public str creationTime(\[str value\])                                   |                                                                                                                           |
| public str disabledImage(\[str value\])                                  | コントロールの無効な画像を取得または設定します。                                                                            |
| public int disabledImageLocation(\[int value\])                          |                                                                                                                           |
| public int disabledResource(\[int value\])                               | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                            |
| public int imageLocation(\[int value\])                                  |                                                                                                                           |
| public str label(\[str value\])                                          | コントロールのラベルを取得または設定します。                                                                                     |
| public str menuFunctionName(\[str name\])                                |                                                                                                                           |
| public str menuItemName(\[str value\])                                   |                                                                                                                           |
| public MenuItemType menuItemType(\[MenuItemType value\])                 |                                                                                                                           |
| public str menuName()                                                    |                                                                                                                           |
| public str name(\[str value\])                                           | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededAccessLevel(\[int value\])                              | MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。                                                   |
| public str normalImage(\[str value\])                                    |                                                                                                                           |
| public int normalResource(\[int value\])                                 |                                                                                                                           |
| public Guid origin(\[Guid value\])                                       |                                                                                                                           |
| public str parameter(\[str parameter\])                                  |                                                                                                                           |
| public str parameters(\[str value\])                                     | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                    |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                |                                                                                                                           |
| public boolean setCompany(\[boolean value\])                             |                                                                                                                           |
| public str shortCut(\[str value\])                                       |                                                                                                                           |
| public boolean showParentModule(\[boolean value\])                       |                                                                                                                           |
| public boolean visible(\[boolean value\])                                |                                                                                                                           |
| public str webTarget(\[str value\])                                      |                                                                                                                           |
| public void save()                                                       |                                                                                                                           |
| public void new(str Name)                                                | TreeNode クラスの新しいインスタンスを初期化します。                                                                         |
| public void makeWebMenu(Object outputClass)                              |                                                                                                                           |
| public void addMenuitem(xMenuFunction menuFunction)                      | メニューにメニュー項目を追加します。                                                                                             |
| public void setTreeNodeName(str name)                                    |                                                                                                                           |
| public void addMenuReference(Menu menu)                                  |                                                                                                                           |
| public void addSubmenu(str name)                                         | メニューにサブメニューを追加します。                                                                                               |
| public void addSeparator()                                               | メニューにメニューの区切りを追加します。                                                                                        |

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

## <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a>パラメーター - countryRegionCodes

値  

### <a name="return-value---countryregioncodes"></a>戻り値 - countryRegionCodes

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

## <a name="method-disabledimage"></a>メソッド disabledImage

コントロールの無効な画像を取得または設定します。

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a>パラメーター - disabledImage

値  

### <a name="return-value---disabledimage"></a>戻り値 - disabledImage

画像ファイルのフル ネーム。 システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。

### <a name="remarks---disabledimage"></a>備考 - disabledImage

このプロパティは、disabledResource プロパティに優先します。 これらのプロパティの両方が設定されている場合に使用されます。

## <a name="method-disabledimagelocation"></a>メソッド disabledImageLocation

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a>パラメーター - disabledImageLocation

値  

### <a name="return-value---disabledimagelocation"></a>戻り値 - disabledImageLocation

## <a name="method-disabledresource"></a>メソッド disabledResource

無効なボタン画像として使用する画像リソース ID を取得または設定します。

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a>パラメーター - disabledResource

値  

### <a name="return-value---disabledresource"></a>戻り値 - disabledResource

無効なボタン画像として使用する画像リソース ID。 アイコンとビットマップ イメージの両方がサポートされます。

## <a name="method-imagelocation"></a>メソッド imageLocation

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a>パラメーター - imageLocation

値  

### <a name="return-value---imagelocation"></a>戻り値 - imageLocation

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

## <a name="method-menuname"></a>メソッド menuName

```xpp
public str menuName()
```

### <a name="return-value---menuname"></a>戻り値 - menuName

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

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

-   AccessType::NoAccess。
-   AccessType::View。
-   AccessType::Edit。
-   AccessType::Add。
-   AccessType::Delete。

## <a name="method-normalimage"></a>メソッド normalImage

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a>パラメーター - normalImage

値  

### <a name="return-value---normalimage"></a>戻り値 - normalImage

## <a name="method-normalresource"></a>メソッド normalResource

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a>パラメーター - normalResource

値  

### <a name="return-value---normalresource"></a>戻り値 - normalResource

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

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

### <a name="remarks---parameters"></a>備考 - parameters

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

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

## <a name="method-save"></a>メソッド save

```xpp
public void save()
```

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new(str Name)
```

### <a name="parameters---new"></a>パラメーター - new

氏名  

## <a name="method-makewebmenu"></a>メソッド makeWebMenu

```xpp
public void makeWebMenu(Object outputClass)
```

### <a name="parameters---makewebmenu"></a>パラメーター - makeWebMenu

outputClass  

## <a name="method-addmenuitem"></a>メソッド addMenuitem

メニューにメニュー項目を追加します。

```xpp
public void addMenuitem(xMenuFunction menuFunction)
```

### <a name="parameters---addmenuitem"></a>パラメーター - addMenuitem

menuFunction  
追加するメニュー項目。

## <a name="method-settreenodename"></a>メソッド setTreeNodeName

```xpp
public void setTreeNodeName(str name)
```

### <a name="parameters---settreenodename"></a>パラメーター - setTreeNodeName

名前  

## <a name="method-addmenureference"></a>メソッド addMenuReference

```xpp
public void addMenuReference(Menu menu)
```

### <a name="parameters---addmenureference"></a>パラメーター - addMenuReference

メニュー  

## <a name="method-addsubmenu"></a>メソッド addSubmenu

メニューにサブメニューを追加します。

```xpp
public void addSubmenu(str name)
```

### <a name="parameters---addsubmenu"></a>パラメーター - addSubmenu

名前  
メニューに追加するサブメニューの名前に評価される文字列式。

## <a name="method-addseparator"></a>メソッド addSeparator

メニューにメニューの区切りを追加します。

```xpp
public void addSeparator()
```

