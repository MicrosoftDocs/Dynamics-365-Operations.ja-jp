---
title: xMenuFunction クラス
description: このトピックでは、xMenuFunction クラスについて説明します。
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
ms.openlocfilehash: 0cdefef3ddf8fc9b6dbeeaeb3a2a362e8e304de2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502758"
---
# <a name="class-xmenufunction"></a>クラス xMenuFunction

[!include [banner](../../includes/banner.md)]

```xpp
class xMenuFunction extends SecureNode
```

xMenuFunction クラスは、フォーム、レポート、ジョブ、クラス、クエリにアクセスして実行するための簡単な方法を提供する、他のオブジェクトへのインターフェイスを表します。

## <a name="remarks"></a>備考

xMenuFunction オブジェクトとそのメソッドおよびプロパティを使用して、アプリケーション オブジェクトを参照します。 たとえば、次のことを実行できます。

-   Run メソッドを使用してプロパティで参照されるオブジェクトを実行する
-   xMenuFunction オブジェクトを作成し、そのオブジェクトが実行する (または参照する) オブジェクトへの参照を作成します。 これにより、オブジェクトを実行する前に渡された引数を操作できます

注記: このシステム クラスは、AOT 内の MenuItem ノードを表します。 このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                  | 説明                                                                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])                                                                     | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])                                                                 | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                        |
| public str changedTime(\[str value\])                                                                   | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                        |
| public boolean checkAccessRights()                                                                      |                                                                                                                                           |
| public int copyCallerQuery(\[int value\])                                                               |                                                                                                                                           |
| public int correctPermissions(\[int value\])                                                            |                                                                                                                                           |
| public str countryRegionCodes(\[str value\])                                                            |                                                                                                                                           |
| public ObjectRun create(\[xArgs args\])                                                                 | アプリケーション オブジェクトへの参照を作成して返します。                                                           |
| public str createdBy(\[str value\])                                                                     | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public int createPermissions(\[int value\])                                                             |                                                                                                                                           |
| public Date creationDate(\[Date value\])                                                                | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])                                                                  |                                                                                                                                           |
| public int deletePermissions(\[int value\])                                                             |                                                                                                                                           |
| public str disabledImage(\[str value\])                                                                 | コントロールの無効な画像を取得または設定します。                                                                                            |
| public int disabledImageLocation(\[int value\])                                                         |                                                                                                                                           |
| public int disabledResource(\[int value\])                                                              | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                            |
| public int enumParameter(\[int value\])                                                                 | MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。                               |
| public EnumId enumTypeParameter(\[EnumId value\])                                                       | MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。                                                                   |
| public int formViewOption(\[int value\])                                                                |                                                                                                                                           |
| public Query getRootQuery()                                                                             |                                                                                                                                           |
| public boolean hasRunPermissions(\[xArgs args\])                                                        | xMenuFunction オブジェクトに実行権限があり、run() が正常に呼び出されるかどうかをチェックします。                                          |
| public str helpText(\[str value\])                                                                      | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public int imageLocation(\[int value\])                                                                 |                                                                                                                                           |
| public str label(\[str value\])                                                                         | コントロールのラベルを取得または設定します。                                                                                                     |
| public str linkedPermissionObject(\[str value\])                                                        |                                                                                                                                           |
| public str linkedPermissionObjectChild(\[str value\])                                                   |                                                                                                                                           |
| public int linkedPermissionType(\[int value\])                                                          |                                                                                                                                           |
| public int maintainUserLicense(\[int value\])                                                           |                                                                                                                                           |
| public boolean multiSelect(\[boolean value\])                                                           |                                                                                                                                           |
| public str name(\[str value\])                                                                          | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int needsRecord(\[int value\])                                                                   |                                                                                                                                           |
| public str normalImage(\[str value\])                                                                   |                                                                                                                                           |
| public int normalResource(\[int value\])                                                                |                                                                                                                                           |
| public str object(\[str value\])                                                                        | MenuFunction クラスにより実行されるオブジェクトを取得または設定します。                                                                            |
| public int objectType(\[int value\])                                                                    |                                                                                                                                           |
| public int openMode(\[int value\])                                                                      |                                                                                                                                           |
| public Guid origin(\[Guid value\])                                                                      |                                                                                                                                           |
| public str parameters(\[str value\])                                                                    | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                    |
| public str query(\[str value\])                                                                         |                                                                                                                                           |
| public int readPermissions(\[int value\])                                                               |                                                                                                                                           |
| public str reportDesign(\[str value\])                                                                  |                                                                                                                                           |
| public int runOn(\[int value\])                                                                         |                                                                                                                                           |
| public MenuItemType type()                                                                              |                                                                                                                                           |
| public int updatePermissions(\[int value\])                                                             |                                                                                                                                           |
| public int viewUserLicense(\[int value\])                                                               |                                                                                                                                           |
| public str web(\[str value\])                                                                           |                                                                                                                                           |
| public int webAccess(\[int value\])                                                                     |                                                                                                                                           |
| public str webMenuItemName(\[str value\])                                                               |                                                                                                                                           |
| public str webPage(\[str value\])                                                                       |                                                                                                                                           |
| public boolean webSecureTransaction(\[boolean value\])                                                  |                                                                                                                                           |
| public void run(\[xArgs args\])                                                                         | xMenuFunction オブジェクトを実行します。                                                                                                            |
| ::public static void runCalled(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\]) |                                                                                                                                           |
| ::public static void runClient(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\]) |                                                                                                                                           |
| ::public static void runServer(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\]) |                                                                                                                                           |
| public void new(str Name, MenuItemType type)                                                            | xMenuFunction の名前と MenuItemType を xMenuFunction コンストラクターに渡して、新しい xMenuFunction オブジェクトを作成します。                     |
| public void AOTrun(\[xArgs args\])                                                                      | アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。                                                                  |

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  
設定する値 (オプション)。

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  
設定する値 (オプション)。

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  
設定する値 (オプション)。

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-checkaccessrights"></a>メソッド checkAccessRights

```xpp
public boolean checkAccessRights()
```

### <a name="return-value---checkaccessrights"></a>戻り値 - checkAccessRights

## <a name="method-copycallerquery"></a>メソッド copyCallerQuery

```xpp
public int copyCallerQuery([int value])
```

### <a name="parameters---copycallerquery"></a>パラメーター - copyCallerQuery

値  

### <a name="return-value---copycallerquery"></a>戻り値 - copyCallerQuery

## <a name="method-correctpermissions"></a>メソッド correctPermissions

```xpp
public int correctPermissions([int value])
```

### <a name="parameters---correctpermissions"></a>パラメーター - correctPermissions

値  

### <a name="return-value---correctpermissions"></a>戻り値 - correctPermissions

## <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a>パラメーター - countryRegionCodes

値  

### <a name="return-value---countryregioncodes"></a>戻り値 - countryRegionCodes

## <a name="method-create"></a>メソッド create

アプリケーション オブジェクトへの参照を作成して返します。

```xpp
public ObjectRun create([xArgs args])
```

### <a name="parameters---create"></a>パラメーター - create

args  
xArgs クラス オブジェクト。オプション。

### <a name="return-value---create"></a>戻り値 - create

アプリケーション オブジェクトへの参照。

### <a name="remarks---create"></a>備考 - create

このメソッドは、アプリケーション オブジェクトの作成に使用されます。 返されるオブジェクトは、オブジェクト変数に割り当てられます。 init 関数は create 関数によって呼び出されることに注意してください。 したがって、それを呼び出すべきではありません。

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-createpermissions"></a>メソッド createPermissions

```xpp
public int createPermissions([int value])
```

### <a name="parameters---createpermissions"></a>パラメーター - createPermissions

値  

### <a name="return-value---createpermissions"></a>戻り値 - createPermissions

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

## <a name="method-deletepermissions"></a>メソッド deletePermissions

```xpp
public int deletePermissions([int value])
```

### <a name="parameters---deletepermissions"></a>パラメーター - deletePermissions

値  

### <a name="return-value---deletepermissions"></a>戻り値 - deletePermissions

## <a name="method-disabledimage"></a>メソッド disabledImage

コントロールの無効な画像を取得または設定します。

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a>パラメーター - disabledImage

値  

### <a name="return-value---disabledimage"></a>戻り値 - disabledImage

画像ファイルのフル ネーム。システムは GDI でサポートされているすべての画像形式をサポートしています。

### <a name="remarks---disabledimage"></a>備考 - disabledImage

このプロパティは、disabledResource プロパティ値に優先します。 これらのプロパティの両方が設定されている場合に使用されます。

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

## <a name="method-enumparameter"></a>メソッド enumParameter

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。

```xpp
public int enumParameter([int value])
```

### <a name="parameters---enumparameter"></a>パラメーター - enumParameter

値  

### <a name="return-value---enumparameter"></a>戻り値 - enumParameter

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。

## <a name="method-enumtypeparameter"></a>メソッド enumTypeParameter

MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。

```xpp
public EnumId enumTypeParameter([EnumId value])
```

### <a name="parameters---enumtypeparameter"></a>パラメーター - enumTypeParameter

値  

### <a name="return-value---enumtypeparameter"></a>戻り値 - enumTypeParameter

MenuFunction クラスの enumTypeParameter プロパティ。

## <a name="method-formviewoption"></a>メソッド formViewOption

```xpp
public int formViewOption([int value])
```

### <a name="parameters---formviewoption"></a>パラメーター - formViewOption

値  

### <a name="return-value---formviewoption"></a>戻り値 - formViewOption

## <a name="method-getrootquery"></a>メソッド getRootQuery

```xpp
public Query getRootQuery()
```

### <a name="return-value---getrootquery"></a>戻り値 - getRootQuery

## <a name="method-hasrunpermissions"></a>メソッド hasRunPermissions

xMenuFunction オブジェクトに実行権限があり、run() が正常に呼び出されるかどうかをチェックします。

```xpp
public boolean hasRunPermissions([xArgs args])
```

### <a name="parameters---hasrunpermissions"></a>パラメーター - hasRunPermissions

args  
run() メソッドに渡される xArgs クラス オブジェクト。オプション。

### <a name="return-value---hasrunpermissions"></a>戻り値 - hasRunPermissions

run() を正常に呼び出すために必要なアクセス許可が存在する場合は true。

### <a name="remarks---hasrunpermissions"></a>備考 - hasRunPermissions

この関数は、アクセス許可が失敗した場合にスローされることがあります。

## <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  

### <a name="return-value---helptext"></a>戻り値 - helpText

画面の下部に表示される文字列。

### <a name="remarks---helptext"></a>備考 - helpText

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

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

## <a name="method-linkedpermissionobject"></a>メソッド linkedPermissionObject

```xpp
public str linkedPermissionObject([str value])
```

### <a name="parameters---linkedpermissionobject"></a>パラメーター - linkedPermissionObject

値  

### <a name="return-value---linkedpermissionobject"></a>戻り値 - linkedPermissionObject

## <a name="method-linkedpermissionobjectchild"></a>メソッド linkedPermissionObjectChild

```xpp
public str linkedPermissionObjectChild([str value])
```

### <a name="parameters---linkedpermissionobjectchild"></a>パラメーター - linkedPermissionObjectChild

値  

### <a name="return-value---linkedpermissionobjectchild"></a>戻り値 - linkedPermissionObjectChild

## <a name="method-linkedpermissiontype"></a>メソッド linkedPermissionType

```xpp
public int linkedPermissionType([int value])
```

### <a name="parameters---linkedpermissiontype"></a>パラメーター - linkedPermissionType

値  

### <a name="return-value---linkedpermissiontype"></a>戻り値 - linkedPermissionType

## <a name="method-maintainuserlicense"></a>メソッド maintainUserLicense

```xpp
public int maintainUserLicense([int value])
```

### <a name="parameters---maintainuserlicense"></a>パラメーター - maintainUserLicense

値  

### <a name="return-value---maintainuserlicense"></a>戻り値 - maintainUserLicense

## <a name="method-multiselect"></a>メソッド multiSelect

```xpp
public boolean multiSelect([boolean value])
```

### <a name="parameters---multiselect"></a>パラメーター - multiSelect

値  

### <a name="return-value---multiselect"></a>戻り値 - multiSelect

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

## <a name="method-needsrecord"></a>メソッド needsRecord

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a>パラメーター - needsRecord

値  

### <a name="return-value---needsrecord"></a>戻り値 - needsRecord

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

## <a name="method-object"></a>メソッド object

MenuFunction クラスにより実行されるオブジェクトを取得または設定します。

```xpp
public str object([str value])
```

### <a name="parameters---object"></a>パラメーター - object

値  

### <a name="return-value---object"></a>戻り値 - object

MenuFunction クラスにより実行されるオブジェクト。

### <a name="remarks---object"></a>備考 - object

プロパティ値は、次のオブジェクトのいずれかである場合があります。

-   フォーム。
-   レポート。
-   ジョブ。
-   クラス。
-   クエリ。

## <a name="method-objecttype"></a>メソッド objectType

```xpp
public int objectType([int value])
```

### <a name="parameters---objecttype"></a>パラメーター - objectType

値  

### <a name="return-value---objecttype"></a>戻り値 - objectType

## <a name="method-openmode"></a>メソッド openMode

```xpp
public int openMode([int value])
```

### <a name="parameters---openmode"></a>パラメーター - openMode

値  

### <a name="return-value---openmode"></a>戻り値 - openMode

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

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

## <a name="method-query"></a>メソッド query

```xpp
public str query([str value])
```

### <a name="parameters---query"></a>パラメーター - query

値  

### <a name="return-value---query"></a>戻り値 - query

## <a name="method-readpermissions"></a>メソッド readPermissions

```xpp
public int readPermissions([int value])
```

### <a name="parameters---readpermissions"></a>パラメーター - readPermissions

値  

### <a name="return-value---readpermissions"></a>戻り値 - readPermissions

## <a name="method-reportdesign"></a>メソッド reportDesign

```xpp
public str reportDesign([str value])
```

### <a name="parameters---reportdesign"></a>パラメーター - reportDesign

値  

### <a name="return-value---reportdesign"></a>戻り値 - reportDesign

## <a name="method-runon"></a>メソッド runOn

```xpp
public int runOn([int value])
```

### <a name="parameters---runon"></a>パラメーター - runOn

値  

### <a name="return-value---runon"></a>戻り値 - runOn

## <a name="method-type"></a>メソッドのタイプ

```xpp
public MenuItemType type()
```

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-updatepermissions"></a>メソッド updatePermissions

```xpp
public int updatePermissions([int value])
```

### <a name="parameters---updatepermissions"></a>パラメーター - updatePermissions

値  

### <a name="return-value---updatepermissions"></a>戻り値 - updatePermissions

## <a name="method-viewuserlicense"></a>メソッド viewUserLicense

```xpp
public int viewUserLicense([int value])
```

### <a name="parameters---viewuserlicense"></a>パラメーター - viewUserLicense

値  

### <a name="return-value---viewuserlicense"></a>戻り値 - viewUserLicense

## <a name="method-web"></a>メソッド web

```xpp
public str web([str value])
```

### <a name="parameters---web"></a>パラメーター - web

値  

### <a name="return-value---web"></a>戻り値 - web

## <a name="method-webaccess"></a>メソッド webAccess

```xpp
public int webAccess([int value])
```

### <a name="parameters---webaccess"></a>パラメーター - webAccess

値  

### <a name="return-value---webaccess"></a>戻り値 - webAccess

## <a name="method-webmenuitemname"></a>メソッド webMenuItemName

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a>パラメーター - webMenuItemName

値  

### <a name="return-value---webmenuitemname"></a>戻り値 - webMenuItemName

## <a name="method-webpage"></a>メソッド webPage

```xpp
public str webPage([str value])
```

### <a name="parameters---webpage"></a>パラメーター - webPage

値  

### <a name="return-value---webpage"></a>戻り値 - webPage

## <a name="method-websecuretransaction"></a>メソッド webSecureTransaction

```xpp
public boolean webSecureTransaction([boolean value])
```

### <a name="parameters---websecuretransaction"></a>パラメーター - webSecureTransaction

値  

### <a name="return-value---websecuretransaction"></a>戻り値 - webSecureTransaction

## <a name="method-run"></a>メソッド run

xMenuFunction オブジェクトを実行します。

```xpp
public void run([xArgs args])
```

### <a name="parameters---run"></a>パラメーター - run

args  
xArgs クラス オブジェクト。オプション。

### <a name="remarks---run"></a>備考 - run

この関数は、コードから xMenuFunction オブジェクトを実行するために使用されます。

## <a name="method-runcalled"></a>メソッド runCalled

```xpp
public static void runCalled(str Name, MenuItemType type, [boolean setContextMenu], [xArgs args])
```

### <a name="parameters---runcalled"></a>パラメーター - runCalled

氏名  

<!-- -->

タイプ  

<!-- -->

setContextMenu  

<!-- -->

args  

## <a name="method-runclient"></a>メソッド runClient

```xpp
public static void runClient(str Name, MenuItemType type, [boolean setContextMenu], [xArgs args])
```

### <a name="parameters---runclient"></a>パラメーター - runClient

氏名  

<!-- -->

タイプ  

<!-- -->

setContextMenu  

<!-- -->

args  

## <a name="method-runserver"></a>メソッド runServer

```xpp
public static void runServer(str Name, MenuItemType type, [boolean setContextMenu], [xArgs args])
```

### <a name="parameters---runserver"></a>パラメーター - runServer

氏名  

<!-- -->

タイプ  

<!-- -->

setContextMenu  

<!-- -->

args  

## <a name="method-new"></a>メソッド new

xMenuFunction の名前と MenuItemType を xMenuFunction コンストラクターに渡して、新しい xMenuFunction オブジェクトを作成します。

```xpp
public void new(str Name, MenuItemType type)
```

### <a name="parameters---new"></a>パラメーター - new

氏名  
MenuItemType システム列挙型の定数: MenuItemType::Display、MenuItemType::Output、または MenuItemType::Action。

<!-- -->

タイプ  
MenuItemType システム列挙型の定数: MenuItemType::Display、MenuItemType::Output、または MenuItemType::Action。

### <a name="remarks---new"></a>備考 - new

xMenuFunction オブジェクトを作成するとき、パラメータは既存の xMenuFunction を一意に識別する必要があります。 それ以外の場合は、Exception::Internal がスローされます。

## <a name="method-aotrun"></a>メソッド AOTrun

アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。

```xpp
public void AOTrun([xArgs args])
```

### <a name="parameters---aotrun"></a>パラメーター - AOTrun

args  

