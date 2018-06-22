---
title: "W クラス"
description: "文字 W で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 55901
ms.assetid: ca08dc94-1481-4ac0-80f4-d092da5c1c90
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: ffc27f5df568b9122fb774ded2c0b9184314b7e6
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="w-classes"></a>W クラス

[!include [banner](../includes/banner.md)]

文字 W で始まるシステム API クラス。

<a name="class-webactionmenufunction"></a>クラス WebActionMenuFunction
---------------------------

    class WebActionMenuFunction extends WebMenuFunction

WebActionMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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
| public void AOTrun(\[xArgs args\])                       | Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。             |
| ::public static void runClient(str name, \[xArgs args\]) |                                                                                                             |
| public void run(\[xArgs args\])                          |                                                                                                             |
| public void new(str name)                                | TreeNode クラスの新しいインスタンスを初期化します。                                                           |
| ::public static void runServer(str name, \[xArgs args\]) |                                                                                                             |

### <a name="method-big"></a>メソッド big

    public boolean big([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-correctpermissions"></a>メソッド correctPermissions

    public int correctPermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-createpermissions"></a>メソッド createPermissions

    public int createPermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-deletepermissions"></a>メソッド deletePermissions

    public int deletePermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-enumparameter"></a>メソッド enumParameter

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。

    public int enumParameter([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。

### <a name="method-enumtypeparameter"></a>メソッド enumTypeParameter

MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスの enumTypeParameter プロパティ。

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linkedpermissionobject"></a>メソッド linkedPermissionObject

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linkedpermissionobjectchild"></a>メソッド linkedPermissionObjectChild

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linkedpermissiontype"></a>メソッド linkedPermissionType

    public int linkedPermissionType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-maintainuserlicense"></a>メソッド maintainUserLicense

Microsoft 社内のみで使用。

    public int maintainUserLicense([int value])

#### <a name="parameters"></a>パラメーター

値  
新しいユーザー ライセンス。

#### <a name="return-value"></a>戻り値

ユーザー ライセンス。

### <a name="method-multiselect"></a>メソッド multiSelect

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-needsrecord"></a>メソッド needsRecord

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalimage"></a>メソッド normalImage

    public str normalImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalresource"></a>メソッド normalResource

    public int normalResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-object"></a>メソッド object

MenuFunction クラスが実行するオブジェクトを取得または設定します。

    public str object([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスが実行するオブジェクト。

#### <a name="remarks"></a>備考

プロパティ値は、次のオブジェクトのいずれかである場合があります。

-   フォーム
-   レポート 
-   ジョブ
-   クラス
-   クエリ

### <a name="method-objecttype"></a>メソッド objectType

    public int objectType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-readpermissions"></a>メソッド readPermissions

    public int readPermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-reportdesign"></a>メソッド reportDesign

    public str reportDesign([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-runon"></a>メソッド runOn

    public int runOn([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-updatepermissions"></a>メソッド updatePermissions

    public int updatePermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-viewuserlicense"></a>メソッド viewUserLicense

Microsoft 社内のみで使用。

    public int viewUserLicense([int value])

#### <a name="parameters"></a>パラメーター

値  
表示するユーザー ライセンス。

#### <a name="return-value"></a>戻り値

ユーザー ライセンス。

### <a name="method-runcalled"></a>メソッド runCalled

    public static void runCalled(str name, [xArgs args])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

args  

### <a name="method-aotrun"></a>メソッド AOTrun

Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。

    public void AOTrun([xArgs args])

#### <a name="parameters"></a>パラメーター

args  

### <a name="method-runclient"></a>メソッド runClient

    public static void runClient(str name, [xArgs args])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

args  

### <a name="method-run"></a>メソッド run

    public void run([xArgs args])

#### <a name="parameters"></a>パラメーター

args  

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str name)

#### <a name="parameters"></a>パラメーター

名前  

### <a name="method-runserver"></a>メソッド runServer

    public static void runServer(str name, [xArgs args])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

args  

## <a name="class-webcontentitem"></a>クラス WebContentItem
    class WebContentItem extends SecureNode

WebContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                            | 説明                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])               | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])           | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])             | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])               | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])          | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])            |                                                                                                                                           |
| public int enumParameter(\[int value\])           | MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。                               |
| public EnumId enumTypeParameter(\[EnumId value\]) | MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。                                                                   |
| public str helpText(\[str value\])                | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public str label(\[str value\])                   | コントロールのラベルを取得または設定します。                                                                                                     |
| public str name(\[str value\])                    | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public str object(\[str value\])                  | MenuFunction クラスが実行するオブジェクトを取得または設定します。                                                                                 |
| public int objectType(\[int value\])              |                                                                                                                                           |
| public Guid origin(\[Guid value\])                |                                                                                                                                           |
| public str parameters(\[str value\])              | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                    |
| public str reportDesign(\[str value\])            |                                                                                                                                           |

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-enumparameter"></a>メソッド enumParameter

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。

    public int enumParameter([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。

### <a name="method-enumtypeparameter"></a>メソッド enumTypeParameter

MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスの enumTypeParameter プロパティ。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ダイアログ ボックス。 ヘルプ テキストは、250文字以下である必要があります。

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-object"></a>メソッド object

MenuFunction クラスが実行するオブジェクトを取得または設定します。

    public str object([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスが実行するオブジェクト。

#### <a name="remarks"></a>備考

プロパティ値は、次のオブジェクトのいずれかである場合があります。

-   フォーム
-   レポート 
-   ジョブ
-   クラス
-   クエリ

### <a name="method-objecttype"></a>メソッド objectType

    public int objectType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-reportdesign"></a>メソッド reportDesign

    public str reportDesign([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

## <a name="class-webcontrolnode"></a>クラス webControlNode
    class webControlNode extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                        | 説明                                                                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                     | このノードのソース コードを返します。                                                                                                         |
| public str changedBy(\[str value\])                           | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])                       | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                 |
| public str changedTime(\[str value\])                         | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                 |
| public str createdBy(\[str value\])                           | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])                      | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                      |
| public str creationTime(\[str value\])                        |                                                                                                                                               |
| public str filename(\[str value\])                            |                                                                                                                                               |
| public List getRelatedWebControls(\[boolean firstLevelOnly\]) | この Web コントロールに関連する Web コントロールの一覧を取得します。                                                                              |
| public str helpText(\[str value\])                            | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                      |
| public str name(\[str value\])                                | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                            |                                                                                                                                               |
| public str relativePath(\[str value\])                        |                                                                                                                                               |
| public str version(\[str value\])                             |                                                                                                                                               |
| ::public static webControlNode createFromFile(str fileName)   |                                                                                                                                               |
| public void AOTsetSource(str source, \[boolean isStatic\])    | このノードのソース コードを設定します。                                                                                                            |

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-filename"></a>メソッド filename

    public str filename([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getrelatedwebcontrols"></a>メソッド getRelatedWebControls

この Web コントロールに関連する Web コントロールの一覧を取得します。

    public List getRelatedWebControls([boolean firstLevelOnly])

#### <a name="parameters"></a>パラメーター

firstLevelOnly  
Web コントロールの最初のレベルのみがオンになっているかどうかを示す値。

#### <a name="return-value"></a>戻り値

関連する Web コントロールの一覧。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-relativepath"></a>メソッド relativePath

    public str relativePath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-version"></a>メソッド version

    public str version([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-createfromfile"></a>メソッド createFromFile

    public static webControlNode createFromFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

#### <a name="return-value"></a>戻り値

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
メソッドが静的かどうかを指定する値 (オプション)。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値 (オプション)。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

## <a name="class-webdisplaycontentitem"></a>クラス WebDisplayContentItem
    class WebDisplayContentItem extends WebContentItem

WebDisplayContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                    | 説明                          |
|---------------------------|--------------------------------------|
| public void new(str name) | 新しい WebDisplayContentItem を作成します。 |

### <a name="method-new"></a>メソッド new

新しい WebDisplayContentItem を作成します。

    public void new(str name)

#### <a name="parameters"></a>パラメーター

名前  

## <a name="class-webletitem"></a>クラス WebletItem
    class WebletItem extends SecureNode

WebletItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                            | 説明                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])               | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])           | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                 |
| public str changedTime(\[str value\])             | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                 |
| public str createdBy(\[str value\])               | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])          | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                      |
| public str creationTime(\[str value\])            |                                                                                                                                               |
| public int enumParameter(\[int value\])           | MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。                                   |
| public EnumId enumTypeParameter(\[EnumId value\]) | MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。                                                                       |
| public str helpText(\[str value\])                | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                      |
| public str label(\[str value\])                   | コントロールのラベルを取得または設定します。                                                                                                         |
| public str name(\[str value\])                    | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public str object(\[str value\])                  | MenuFunction クラスが実行するオブジェクトを取得または設定します。                                                                                     |
| public int objectType(\[int value\])              |                                                                                                                                               |
| public Guid origin(\[Guid value\])                |                                                                                                                                               |
| public str parameters(\[str value\])              | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                        |
| public str reportDesign(\[str value\])            |                                                                                                                                               |
| public void new(str name)                         | Microsoft 社内のみで使用。                                                                                                                  |

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-enumparameter"></a>メソッド enumParameter

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。

    public int enumParameter([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。

### <a name="method-enumtypeparameter"></a>メソッド enumTypeParameter

MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスの enumTypeParameter プロパティ。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-object"></a>メソッド object

MenuFunction クラスが実行するオブジェクトを取得または設定します。

    public str object([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスが実行するオブジェクト。

#### <a name="remarks"></a>備考

プロパティ値は、次のオブジェクトのいずれかである場合があります。

-   フォーム。
-   レポート。
-   ジョブ。
-   クラス。
-   クエリ。

### <a name="method-objecttype"></a>メソッド objectType

    public int objectType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-reportdesign"></a>メソッド reportDesign

    public str reportDesign([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Microsoft 社内のみで使用。

    public void new(str name)

#### <a name="parameters"></a>パラメーター

名前  

## <a name="class-weblistdefnode"></a>クラス webListDefNode
    class webListDefNode extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | このノードのソース コードを返します。                                                                                                     |
| public str changedBy(\[str value\])                        | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])                    | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])                      | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])                        | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])                   | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])                     |                                                                                                                                           |
| public str helpText(\[str value\])                         | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public boolean mOSSOnly(\[boolean value\])                 |                                                                                                                                           |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                         |                                                                                                                                           |
| public str pageTitle(\[str value\])                        |                                                                                                                                           |
| public boolean publicPage(\[boolean value\])               |                                                                                                                                           |
| public str uRL(\[str value\])                              |                                                                                                                                           |
| public str webModule(\[str value\])                        |                                                                                                                                           |
| public void AOTsetSource(str source, \[boolean isStatic\]) | このノードのソース コードを設定します。                                                                                                        |
| public void new(str name)                                  | TreeNode クラスの新しいインスタンスを初期化します。                                                                                         |

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-mossonly"></a>メソッド mOSSOnly

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-pagetitle"></a>メソッド pageTitle

    public str pageTitle([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-publicpage"></a>メソッド publicPage

    public boolean publicPage([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-url"></a>メソッド uRL

    public str uRL([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-webmodule"></a>メソッド webModule

    public str webModule([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
メソッドが静的かどうかを指定する値 (オプション)。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値 (オプション)。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str name)

#### <a name="parameters"></a>パラメーター

名前  

## <a name="class-webmanagedcontentitem"></a>クラス WebManagedContentItem
    class WebManagedContentItem extends WebContentItem

このクラスを使用して、コンテンツをページに追加するために EP で使用する webManagedContentItem を作成します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                    | 説明                                                 |
|---------------------------|-------------------------------------------------------------|
| public void new(str name) | 渡された名前で新しい webManagedContentItem を作成します。 |

### <a name="method-new"></a>メソッド new

渡された名前で新しい webManagedContentItem を作成します。

    public void new(str name)

#### <a name="parameters"></a>パラメーター

名前  
新しい webManagedContentItem に名前を付けます。

## <a name="class-webmenu"></a>クラス WebMenu
    class WebMenu extends TreeNode

WebMenu クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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
| public str name(\[str value\])                                           | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
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

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-highlightselected"></a>メソッド highlightSelected

    public boolean highlightSelected([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemtype"></a>メソッド menuItemType

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuname"></a>メソッド menuName

    public str menuName()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededaccesslevel"></a>メソッド neededAccessLevel

MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。

    public int neededAccessLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

neededAccessLevel プロパティの現在の値。

#### <a name="remarks"></a>備考

AccessType システム列挙値の使用可能な値は次のとおりです。

-   AccessType::NoAccess
-   AccessType::View
-   AccessType::Edit
-   AccessType::Add
-   AccessType::Delete

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-setcompany"></a>メソッド setCompany

    public boolean setCompany([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showparentmodule"></a>メソッド showParentModule

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-webtarget"></a>メソッド webTarget

    public str webTarget([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-addseparator"></a>メソッド addSeparator

    public void addSeparator()

### <a name="method-makemenu"></a>メソッド makeMenu

    public void makeMenu(Object outputClass)

#### <a name="parameters"></a>パラメーター

outputClass  

### <a name="method-addsubmenu"></a>メソッド addSubmenu

    public void addSubmenu(str name)

#### <a name="parameters"></a>パラメーター

名前  

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str Name)

#### <a name="parameters"></a>パラメーター

氏名  

### <a name="method-addmenuitem"></a>メソッド addMenuitem

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a>パラメーター

webMenuFunction  

## <a name="class-webmenufunction"></a>クラス WebMenuFunction
    class WebMenuFunction extends SecureNode

WebMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                           | 説明                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])                                                              | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])                                                          | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                 |
| public str changedTime(\[str value\])                                                            | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                 |
| public str createdBy(\[str value\])                                                              | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])                                                         | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                      |
| public str creationTime(\[str value\])                                                           |                                                                                                                                               |
| public str helpText(\[str value\])                                                               | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                      |
| public str label(\[str value\])                                                                  | コントロールのラベルを取得または設定します。                                                                                                         |
| public str name(\[str value\])                                                                   | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                                                               |                                                                                                                                               |
| ::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType) |                                                                                                                                               |

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-createwebmenufunction"></a>メソッド createWebMenuFunction

    public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

webMenuItemType  

#### <a name="return-value"></a>戻り値

## <a name="class-webmenuitem"></a>クラス WebMenuItem
    class WebMenuItem extends TreeNode

WebMenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                         | 説明                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str label()                                             |                                                                                                                                           |
| public str menuItemName(\[str value\])                         |                                                                                                                                           |
| public WebMenuItemType menuItemType(\[WebMenuItemType value\]) |                                                                                                                                           |
| public str name(\[str value\])                                 | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public str parameters(\[str value\])                           | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                    |
| public boolean showParentModule(\[boolean value\])             |                                                                                                                                           |

### <a name="method-label"></a>メソッド label

    public str label()

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemtype"></a>メソッド menuItemType

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-showparentmodule"></a>メソッド showParentModule

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

## <a name="class-webmodulenode"></a>クラス webModuleNode
    class webModuleNode extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                   | 説明                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])                                      | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                     |
| public Date changedDate(\[Date value\])                                  | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                  |
| public str changedTime(\[str value\])                                    | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                  |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\]) | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                            |
| public str createdBy(\[str value\])                                      | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                          |
| public Date creationDate(\[Date value\])                                 | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                       |
| public str creationTime(\[str value\])                                   |                                                                                                                                                |
| public boolean extendedDataSecurity(\[boolean value\])                   |                                                                                                                                                |
| public boolean inheritNavigation(\[boolean value\])                      |                                                                                                                                                |
| public boolean inheritPermissions(\[boolean value\])                     |                                                                                                                                                |
| public str label(\[str value\])                                          | コントロールのラベルを取得または設定します。                                                                                                          |
| public str masterPage(\[str value\])                                     |                                                                                                                                                |
| public str menuItemName(\[str value\])                                   |                                                                                                                                                |
| public WebMenuItemType menuItemType(\[WebMenuItemType value\])           |                                                                                                                                                |
| public str moduleName()                                                  |                                                                                                                                                |
| public str modulePath()                                                  |                                                                                                                                                |
| public str name(\[str value\])                                           | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededAccessLevel(\[int value\])                              | MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。                                                                        |
| public Guid origin(\[Guid value\])                                       |                                                                                                                                                |
| public boolean publicModule(\[boolean value\])                           |                                                                                                                                                |
| public str quickLaunch(\[str value\])                                    |                                                                                                                                                |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                |                                                                                                                                                |
| public boolean showLink(\[boolean value\])                               |                                                                                                                                                |
| public boolean showParentModule(\[boolean value\])                       |                                                                                                                                                |
| public void addSubModule(str name)                                       |                                                                                                                                                |
| public void new(str Name)                                                | TreeNode クラスの新しいインスタンスを初期化します。                                                                                              |
| public void addMenuitem(WebMenuFunction webMenuFunction)                 |                                                                                                                                                |

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-extendeddatasecurity"></a>メソッド extendedDataSecurity

    public boolean extendedDataSecurity([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-inheritnavigation"></a>メソッド inheritNavigation

    public boolean inheritNavigation([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-inheritpermissions"></a>メソッド inheritPermissions

    public boolean inheritPermissions([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-masterpage"></a>メソッド masterPage

    public str masterPage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemtype"></a>メソッド menuItemType

    public WebMenuItemType menuItemType([WebMenuItemType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-modulename"></a>メソッド moduleName

    public str moduleName()

#### <a name="return-value"></a>戻り値

### <a name="method-modulepath"></a>メソッド modulePath

    public str modulePath()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededaccesslevel"></a>メソッド neededAccessLevel

MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。

    public int neededAccessLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

neededAccessLevel プロパティの現在の値。

#### <a name="remarks"></a>備考

AccessType システム列挙値の使用可能な値は次のとおりです。

-   AccessType::NoAccess
-   AccessType::View
-   AccessType::Edit
-   AccessType::Add
-   AccessType::Delete

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-publicmodule"></a>メソッド publicModule

    public boolean publicModule([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-quicklaunch"></a>メソッド quickLaunch

    public str quickLaunch([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showlink"></a>メソッド showLink

    public boolean showLink([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showparentmodule"></a>メソッド showParentModule

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-addsubmodule"></a>メソッド addSubModule

    public void addSubModule(str name)

#### <a name="parameters"></a>パラメーター

名前  

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str Name)

#### <a name="parameters"></a>パラメーター

氏名  

### <a name="method-addmenuitem"></a>メソッド addMenuitem

    public void addMenuitem(WebMenuFunction webMenuFunction)

#### <a name="parameters"></a>パラメーター

webMenuFunction  

## <a name="class-weboutputcontentitem"></a>クラス WebOutputContentItem
    class WebOutputContentItem extends WebContentItem

このクラスは、x++ の WebOutputContentItem を表します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                    | 説明                         |
|---------------------------|-------------------------------------|
| public void new(str name) | 新しい WebOutputContentItem を作成します。 |

### <a name="method-new"></a>メソッド new

新しい WebOutputContentItem を作成します。

    public void new(str name)

#### <a name="parameters"></a>パラメーター

名前  

## <a name="class-webpagedefnode"></a>クラス webPageDefNode
    class webPageDefNode extends TreeNode

webPageDefNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | ノードのソースを取得します。                                                                                                              |
| public str changedBy(\[str value\])                        | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])                    | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])                      | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])                        | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])                   | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])                     |                                                                                                                                           |
| public str helpText(\[str value\])                         | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public str imageResource(\[str value\])                    |                                                                                                                                           |
| public boolean mOSSOnly(\[boolean value\])                 |                                                                                                                                           |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                         |                                                                                                                                           |
| public str pageTitle(\[str value\])                        |                                                                                                                                           |
| public str parentPage(\[str value\])                       |                                                                                                                                           |
| public boolean publicPage(\[boolean value\])               |                                                                                                                                           |
| public str uRL(\[str value\])                              |                                                                                                                                           |
| public boolean useContext(\[boolean value\])               |                                                                                                                                           |
| public str webModule(\[str value\])                        |                                                                                                                                           |
| public str wSSHelpTopic(\[str value\])                     |                                                                                                                                           |
| public void new(str name)                                  | 新しい webPageDefNode の作成。                                                                                                             |
| public void AOTsetSource(str source, \[boolean isStatic\]) | 指定した文字列に webPageDefNode のソースを設定します。                                                                                 |

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

ノードのソースを取得します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ノードのソース。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-imageresource"></a>メソッド imageResource

    public str imageResource([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mossonly"></a>メソッド mOSSOnly

    public boolean mOSSOnly([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-pagetitle"></a>メソッド pageTitle

    public str pageTitle([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parentpage"></a>メソッド parentPage

    public str parentPage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-publicpage"></a>メソッド publicPage

    public boolean publicPage([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-url"></a>メソッド uRL

    public str uRL([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-usecontext"></a>メソッド useContext

    public boolean useContext([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-webmodule"></a>メソッド webModule

    public str webModule([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-wsshelptopic"></a>メソッド wSSHelpTopic

    public str wSSHelpTopic([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

新しい webPageDefNode の作成。

    public void new(str name)

#### <a name="parameters"></a>パラメーター

名前  

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

指定した文字列に webPageDefNode のソースを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
ソースが静的であるかどうかのマークを付けるオプションのパラメーター。

<!-- -->

isStatic  
ソースが静的であるかどうかのマークを付けるオプションのパラメーター。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

## <a name="class-webstaticfilenode"></a>クラス webStaticFileNode
    class webStaticFileNode extends TreeNode

webStaticFileNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | ノードのソースを取得します。                                                                                                              |
| public str changedBy(\[str value\])                        | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])                    | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])                      | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])                        | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])                   | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])                     |                                                                                                                                           |
| public str filename(\[str value\])                         |                                                                                                                                           |
| public str helpText(\[str value\])                         | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                         |                                                                                                                                           |
| public str relativePath(\[str value\])                     |                                                                                                                                           |
| public str version(\[str value\])                          |                                                                                                                                           |
| public void AOTsetSource(str source, \[boolean isStatic\]) | 指定した文字列に静的ファイル ノードのソースを設定します。                                                                              |

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

ノードのソースを取得します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ノードのソース。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-filename"></a>メソッド filename

    public str filename([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-relativepath"></a>メソッド relativePath

    public str relativePath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-version"></a>メソッド version

    public str version([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

指定した文字列に静的ファイル ノードのソースを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
提供されるソースが静的であるかどうかを示すオプションのパラメーター。

<!-- -->

isStatic  
提供されるソースが静的であるかどうかを示すオプションのパラメーター。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

## <a name="class-weburlmenufunction"></a>クラス WebUrlMenuFunction
    class WebUrlMenuFunction extends WebMenuFunction

WebUrlMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                | 説明                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| public boolean big(\[boolean value\])                 |                                                                                                        |
| public int closeDialogBehavior(\[int value\])         |                                                                                                        |
| public int correctPermissions(\[int value\])          |                                                                                                        |
| public int createPermissions(\[int value\])           |                                                                                                        |
| public int deletePermissions(\[int value\])           |                                                                                                        |
| public boolean hideActionPane(\[boolean value\])      |                                                                                                        |
| public boolean homePage(\[boolean value\])            |                                                                                                        |
| public int imageLocation(\[int value\])               |                                                                                                        |
| public str linkedPermissionObject(\[str value\])      |                                                                                                        |
| public str linkedPermissionObjectChild(\[str value\]) |                                                                                                        |
| public int linkedPermissionType(\[int value\])        |                                                                                                        |
| public int maintainUserLicense(\[int value\])         | Microsoft 社内のみで使用。                                                                           |
| public boolean multiSelect(\[boolean value\])         |                                                                                                        |
| public boolean needsRecord(\[boolean value\])         |                                                                                                        |
| public str normalImage(\[str value\])                 |                                                                                                        |
| public int normalResource(\[int value\])              |                                                                                                        |
| public Guid origin(\[Guid value\])                    |                                                                                                        |
| public str pageDefinition(\[str value\])              |                                                                                                        |
| public str parameters(\[str value\])                  | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。 |
| public int readPermissions(\[int value\])             |                                                                                                        |
| public int updatePermissions(\[int value\])           |                                                                                                        |
| public str uRL(\[str value\])                         |                                                                                                        |
| public int viewUserLicense(\[int value\])             | Microsoft 社内のみで使用。                                                                           |
| public int windowMode(\[int value\])                  |                                                                                                        |
| public str windowParameters(\[str value\])            |                                                                                                        |
| public int windowSize(\[int value\])                  |                                                                                                        |
| public void new(str name)                             | TreeNode クラスの新しいインスタンスを初期化します。                                                      |

### <a name="method-big"></a>メソッド big

    public boolean big([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-closedialogbehavior"></a>メソッド closeDialogBehavior

    public int closeDialogBehavior([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-correctpermissions"></a>メソッド correctPermissions

    public int correctPermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-createpermissions"></a>メソッド createPermissions

    public int createPermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-deletepermissions"></a>メソッド deletePermissions

    public int deletePermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hideactionpane"></a>メソッド hideActionPane

    public boolean hideActionPane([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-homepage"></a>メソッド homePage

    public boolean homePage([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linkedpermissionobject"></a>メソッド linkedPermissionObject

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linkedpermissionobjectchild"></a>メソッド linkedPermissionObjectChild

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linkedpermissiontype"></a>メソッド linkedPermissionType

    public int linkedPermissionType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-maintainuserlicense"></a>メソッド maintainUserLicense

Microsoft 社内のみで使用。

    public int maintainUserLicense([int value])

#### <a name="parameters"></a>パラメーター

値  
新しいユーザー ライセンス。

#### <a name="return-value"></a>戻り値

ユーザー ライセンス。

### <a name="method-multiselect"></a>メソッド multiSelect

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-needsrecord"></a>メソッド needsRecord

    public boolean needsRecord([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalimage"></a>メソッド normalImage

    public str normalImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalresource"></a>メソッド normalResource

    public int normalResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-pagedefinition"></a>メソッド pageDefinition

    public str pageDefinition([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-readpermissions"></a>メソッド readPermissions

    public int readPermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-updatepermissions"></a>メソッド updatePermissions

    public int updatePermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-url"></a>メソッド uRL

    public str uRL([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-viewuserlicense"></a>メソッド viewUserLicense

Microsoft 社内のみで使用。

    public int viewUserLicense([int value])

#### <a name="parameters"></a>パラメーター

値  
表示するユーザー ライセンス。

#### <a name="return-value"></a>戻り値

ユーザー ライセンス。

### <a name="method-windowmode"></a>メソッド windowMode

    public int windowMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-windowparameters"></a>メソッド windowParameters

    public str windowParameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-windowsize"></a>メソッド windowSize

    public int windowSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str name)

#### <a name="parameters"></a>パラメーター

名前  

## <a name="class-winapinative"></a>クラス WinAPINative
    class WinAPINative extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                  | 説明                                           |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| ::public static Int64 createFontIndirect(Binary logfont)                                                                |                                                       |
| ::public static boolean deleteObject(Int64 hGDIObject)                                                                  |                                                       |
| ::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths) |                                                       |
| ::public static int getDeviceCaps(Int64 hDC, int index)                                                                 |                                                       |
| ::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])                              |                                                       |
| ::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])                                                    |                                                       |
| ::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)                                           |                                                       |
| ::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)                                                       |                                                       |
| ::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)                        |                                                       |
| ::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)                                                         |                                                       |
| private void new()                                                                                                      | WinAPINative クラスの新しいインスタンスを初期化します。 |

### <a name="method-createfontindirect"></a>メソッド createFontIndirect

    public static Int64 createFontIndirect(Binary logfont)

#### <a name="parameters"></a>パラメーター

logfont  

#### <a name="return-value"></a>戻り値

### <a name="method-deleteobject"></a>メソッド deleteObject

    public static boolean deleteObject(Int64 hGDIObject)

#### <a name="parameters"></a>パラメーター

hGDIObject  

#### <a name="return-value"></a>戻り値

### <a name="method-getcharabcwidthsi"></a>メソッド getCharABCWidthsI

    public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)

#### <a name="parameters"></a>パラメーター

hDC  

<!-- -->

firstGlyphIndex  

<!-- -->

glyphIndicesCount  

<!-- -->

charWidths  

#### <a name="return-value"></a>戻り値

### <a name="method-getdevicecaps"></a>メソッド getDeviceCaps

    public static int getDeviceCaps(Int64 hDC, int index)

#### <a name="parameters"></a>パラメーター

hDC  

<!-- -->

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-getfontdata"></a>メソッド getFontData

    public static int getFontData(Int64 hDC, int dwTable, int dwOffset, [Binary pvBuffer])

#### <a name="parameters"></a>パラメーター

hDC  

<!-- -->

dwTable  

<!-- -->

dwOffset  

<!-- -->

pvBuffer  

#### <a name="return-value"></a>戻り値

### <a name="method-getfontunicoderanges"></a>メソッド getFontUnicodeRanges

    public static int getFontUnicodeRanges(Int64 hDC, [Binary lpgs])

#### <a name="parameters"></a>パラメーター

hDC  

<!-- -->

lpgs  

#### <a name="return-value"></a>戻り値

### <a name="method-getglyphindices"></a>メソッド getGlyphIndices

    public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)

#### <a name="parameters"></a>パラメーター

hDC  

<!-- -->

lpstr  

<!-- -->

pgi  

<!-- -->

fl  

#### <a name="return-value"></a>戻り値

### <a name="method-gettextmetrics"></a>メソッド getTextMetrics

    public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)

#### <a name="parameters"></a>パラメーター

hDC  

<!-- -->

lpMetrics  

#### <a name="return-value"></a>戻り値

### <a name="method-getuniscribeglyphindices"></a>メソッド getUniscribeGlyphIndices

    public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)

#### <a name="parameters"></a>パラメーター

hDC  

<!-- -->

hGDIObject  

<!-- -->

lpstr  

<!-- -->

pgi  

#### <a name="return-value"></a>戻り値

### <a name="method-selectobject"></a>メソッド selectObject

    public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)

#### <a name="parameters"></a>パラメーター

hDC  

<!-- -->

hGDIObject  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

WinAPINative クラスの新しいインスタンスを初期化します。

    private void new()




