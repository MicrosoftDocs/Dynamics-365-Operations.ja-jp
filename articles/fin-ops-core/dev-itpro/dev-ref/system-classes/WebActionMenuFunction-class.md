---
title: WebActionMenuFunction クラス
description: このトピックでは、WebActionMenuFunction クラスについて説明します。
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
ms.openlocfilehash: 1d8ec6e7110dcf706ee92d5edfb911801bcc2d66
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502776"
---
# <a name="class-webactionmenufunction"></a>クラス WebActionMenuFunction

[!include [banner](../../includes/banner.md)]


```xpp
class WebActionMenuFunction extends WebMenuFunction
```

WebActionMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                   | 説明                                                                                                 |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| public boolean big(\[boolean value\])                    |                                                                                                             |
| public int correctPermissions(\[int value\])             |                                                                                                             |
| public int createPermissions(\[int value\])              |                                                                                                             |
| public int deletePermissions(\[int value\])              |                                                                                                             |
| public int enumParameter(\[int value\])                  | MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。 |
| public EnumId enumTypeParameter(\[EnumId value\])        | MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。                                     |
| public int imageLocation(\[int value\])                  |                                                                                                             |
| public str linkedPermissionObject(\[str value\])         |                                                                                                             |
| public str linkedPermissionObjectChild(\[str value\])    |                                                                                                             |
| public int linkedPermissionType(\[int value\])           |                                                                                                             |
| public int maintainUserLicense(\[int value\])            | Microsoft 社内のみで使用。                                                                                |
| public boolean multiSelect(\[boolean value\])            |                                                                                                             |
| public boolean needsRecord(\[boolean value\])            |                                                                                                             |
| public str normalImage(\[str value\])                    |                                                                                                             |
| public int normalResource(\[int value\])                 |                                                                                                             |
| public str object(\[str value\])                         | MenuFunction クラスが実行するオブジェクトを取得または設定します。                                                   |
| public int objectType(\[int value\])                     |                                                                                                             |
| public Guid origin(\[Guid value\])                       |                                                                                                             |
| public str parameters(\[str value\])                     | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。      |
| public int readPermissions(\[int value\])                |                                                                                                             |
| public str reportDesign(\[str value\])                   |                                                                                                             |
| public int runOn(\[int value\])                          |                                                                                                             |
| public int updatePermissions(\[int value\])              |                                                                                                             |
| public int viewUserLicense(\[int value\])                | Microsoft 社内のみで使用。                                                                                |
| ::public static void runCalled(str name, \[xArgs args\]) |                                                                                                             |
| public void AOTrun(\[xArgs args\])                       | アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。             |
| ::public static void runClient(str name, \[xArgs args\]) |                                                                                                             |
| public void run(\[xArgs args\])                          |                                                                                                             |
| public void new(str name)                                | TreeNode クラスの新しいインスタンスを初期化します。                                                           |
| ::public static void runServer(str name, \[xArgs args\]) |                                                                                                             |

## <a name="method-big"></a>メソッド big

```xpp
public boolean big([boolean value])
```

### <a name="parameters---big"></a>パラメーター - big

値  

### <a name="return-value---big"></a>戻り値 - big

## <a name="method-correctpermissions"></a>メソッド correctPermissions

```xpp
public int correctPermissions([int value])
```

### <a name="parameters---correctpermissions"></a>パラメーター - correctPermissions

値  

### <a name="return-value---correctpermissions"></a>戻り値 - correctPermissions

## <a name="method-createpermissions"></a>メソッド createPermissions

```xpp
public int createPermissions([int value])
```

### <a name="parameters---createpermissions"></a>パラメーター - createPermissions

値  

### <a name="return-value---createpermissions"></a>戻り値 - createPermissions

## <a name="method-deletepermissions"></a>メソッド deletePermissions

```xpp
public int deletePermissions([int value])
```

### <a name="parameters---deletepermissions"></a>パラメーター - deletePermissions

値  

### <a name="return-value---deletepermissions"></a>戻り値 - deletePermissions

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

## <a name="method-imagelocation"></a>メソッド imageLocation

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a>パラメーター - imageLocation

値  

### <a name="return-value---imagelocation"></a>戻り値 - imageLocation

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

Microsoft 社内のみで使用。

```xpp
public int maintainUserLicense([int value])
```

### <a name="parameters---maintainuserlicense"></a>パラメーター - maintainUserLicense

値  
新しいユーザー ライセンス。

### <a name="return-value---maintainuserlicense"></a>戻り値 - maintainUserLicense

ユーザー ライセンス。

## <a name="method-multiselect"></a>メソッド multiSelect

```xpp
public boolean multiSelect([boolean value])
```

### <a name="parameters---multiselect"></a>パラメーター - multiSelect

値  

### <a name="return-value---multiselect"></a>戻り値 - multiSelect

## <a name="method-needsrecord"></a>メソッド needsRecord

```xpp
public boolean needsRecord([boolean value])
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

MenuFunction クラスが実行するオブジェクトを取得または設定します。

```xpp
public str object([str value])
```

### <a name="parameters---object"></a>パラメーター - object

値  

### <a name="return-value---object"></a>戻り値 - object

MenuFunction クラスが実行するオブジェクト。

### <a name="remarks---object"></a>備考 - object

プロパティ値は、次のオブジェクトのいずれかである場合があります。

-   フォーム
-   報告
-   ジョブ
-   クラス
-   クエリ

## <a name="method-objecttype"></a>メソッド objectType

```xpp
public int objectType([int value])
```

### <a name="parameters---objecttype"></a>パラメーター - objectType

値  

### <a name="return-value---objecttype"></a>戻り値 - objectType

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

## <a name="method-updatepermissions"></a>メソッド updatePermissions

```xpp
public int updatePermissions([int value])
```

### <a name="parameters---updatepermissions"></a>パラメーター - updatePermissions

値  

### <a name="return-value---updatepermissions"></a>戻り値 - updatePermissions

## <a name="method-viewuserlicense"></a>メソッド viewUserLicense

Microsoft 社内のみで使用。

```xpp
public int viewUserLicense([int value])
```

### <a name="parameters---viewuserlicense"></a>パラメーター - viewUserLicense

値  
表示するユーザー ライセンス。

### <a name="return-value---viewuserlicense"></a>戻り値 - viewUserLicense

ユーザー ライセンス。

## <a name="method-runcalled"></a>メソッド runCalled

```xpp
public static void runCalled(str name, [xArgs args])
```

### <a name="parameters---runcalled"></a>パラメーター - runCalled

名前  

<!-- -->

args  

## <a name="method-aotrun"></a>メソッド AOTrun

アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。

```xpp
public void AOTrun([xArgs args])
```

### <a name="parameters---aotrun"></a>パラメーター - AOTrun

args  

## <a name="method-runclient"></a>メソッド runClient

```xpp
public static void runClient(str name, [xArgs args])
```

### <a name="parameters---runclient"></a>パラメーター - runClient

名前  

<!-- -->

args  

## <a name="method-run"></a>メソッド run

```xpp
public void run([xArgs args])
```

### <a name="parameters---run"></a>パラメーター - run

args  

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new(str name)
```

### <a name="parameters---new"></a>パラメーター - new

名前  

## <a name="method-runserver"></a>メソッド runServer

```xpp
public static void runServer(str name, [xArgs args])
```

### <a name="parameters---runserver"></a>パラメーター - runServer

名前  

<!-- -->

args  

