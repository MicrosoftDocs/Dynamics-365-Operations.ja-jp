---
title: xArgs クラス
description: このトピックでは、xArgs クラスについて説明します。
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
ms.openlocfilehash: af53fba162249101e502e770fb306682770bfdff
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502995"
---
# <a name="class-xargs"></a>クラス xArgs

[!include [banner](../../includes/banner.md)]

```xpp
class xArgs extends Object
```

xArgs クラスは、アプリケーション オブジェクト間の名前、呼び出し元、パラメーターなどの引数を渡すために使用されます。

## <a name="remarks"></a>備考

フォーム、レポートおよびクエリはすべてこのクラスを、コンストラクターで最初の引数として使用します。 このクラスを使用する適切な方法は、xArgs オブジェクトを作成し、名前文字列を指定してから、フォーム コンストラクタまたは ClassFactory メソッドに xArgs オブジェクトを渡すことです。 これらのクラスの中の 1 つに渡された xArgs オブジェクトを参照する場合は、そのクラスの args メソッドを使用してアクセスできます。 追加情報を新しいクラスに渡すために使用できるメソッドは 4 つあります。

-   parm - 文字列を渡すため
-   parmEnum および parmEnumType メソッド - 列挙値を渡すため
-   parmObject メソッド - 任意の型のオブジェクトを渡すため

呼び出し元から送信された xArgs クラスのインスタンスは、カーネルによって自動的に、または呼び出し元によって明示的に作成されます。 呼び出し元がメニュー項目を使用してオブジェクトを呼び出すとき、カーネル コードによって、xArgs クラスのインスタンスが作成されます。 メニュー項目名は、使用するメニュー項目の名前に設定されます。 メニュー項目に、EnumParameter、Parameters、EnumParameter、または EnumTypeParameter プロパティが設定されている場合、カーネルは xArgs クラスのこのインスタンスに対して Parm、ParmEnum、または ParmEnumType プロパティの値を設定します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                       | 説明                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| public boolean allowUseOfPreloadedForm(\[boolean value\])                                                    | このインスタンスに対して起動されたフォームが、プリロードされたフォーム プールから取得されたものかどうかを判定します。                                             |
| public int arrIdx(\[int value\])                                                                             |                                                                                                                                       |
| public Object caller(\[Object value\])                                                                       | xArgs クラスのこのインスタンスを作成したオブジェクトのインスタンスを取得または設定します。                                                |
| public IDispatcherProxy callerDispatcher()                                                                   |                                                                                                                                       |
| public FormControl callerFormControl(\[FormControl value\])                                                  |                                                                                                                                       |
| public str callerName()                                                                                      |                                                                                                                                       |
| public UtilElementType callerType()                                                                          |                                                                                                                                       |
| public Guid callerId()                                                                                       |                                                                                                                                       |
| public str clientId(\[str value\])                                                                           |                                                                                                                                       |
| public CopyCallerQuery copyCallerQuery(\[CopyCallerQuery value\])                                            |                                                                                                                                       |
| public TableId dataset()                                                                                     | 呼び出し元オブジェクトが動作しているテーブルのテーブル ID を取得します。                                                                 |
| public str designName(\[str value\])                                                                         | レポートまたはフォームでデザインを示す文字列を取得または設定します。                                                                    |
| public ExtendedTypeId extType(\[ExtendedTypeId edt\], \[int arrayIndex\])                                    |                                                                                                                                       |
| public FormViewOption formViewOption(\[FormViewOption value\])                                               |                                                                                                                                       |
| public InitialQueryParameter initialQuery(\[InitialQueryParameter initialQueryParameter\])                   |                                                                                                                                       |
| public FieldId lookupField(\[FieldId value\])                                                                | 指定されたレコードの検索に使用するテーブルのフィールド ID を取得または設定します。                                                            |
| public Common lookupRecord(\[Common value\])                                                                 | 指定されたテーブルのレコードを検索します。                                                                                                |
| public TableId lookupTable(\[TableId value\])                                                                |                                                                                                                                       |
| public str lookupValue(\[str value\])                                                                        | テーブルのフィールドで値を検索する LookupField メソッドで使用する文字列を取得または設定します。                                       |
| public str managedContentItemName(\[str value\])                                                             |                                                                                                                                       |
| public str menuItemName(\[str value\])                                                                       | アプリケーション オブジェクトを開始するのに使用するメニュー項目の名前を取得または設定します。                                                        |
| public MenuItemType menuItemType(\[MenuItemType value\])                                                     | アプリケーション オブジェクトの呼び出しを開始するのに使用するメニュー項目のタイプを取得または設定します。                                                 |
| public MultiSelectionContext multiSelectionContext()                                                         |                                                                                                                                       |
| public str name(\[str value\])                                                                               | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。             |
| public Object object(\[Object value\])                                                                       | 新しいインスタンスを開く対象となるオブジェクトのアプリケーション名を取得および設定します。                                                    |
| public OpenMode openMode(\[OpenMode value\])                                                                 |                                                                                                                                       |
| public Int64 parentWnd(\[Int64 value\])                                                                      |                                                                                                                                       |
| public str parm(\[str value\])                                                                               | 呼び出されるオブジェクトのさまざまな情報を指定する文字列を取得または設定します。                                                 |
| public AnyType parmEnum(\[int value\])                                                                       | parmEnumType メソッドで指定されている列挙型の列挙値を取得または設定します。                              |
| public int parmEnumType(\[int value\])                                                                       | 任意の列挙タイプの ID 値を取得または設定します。                                                                                    |
| public Object parmObject(\[Object value\])                                                                   | 呼び出されるオブジェクトに渡す任意のオブジェクトのインスタンスを取得または設定します。                                                                 |
| public Common record(\[Common value\])                                                                       | 呼び出し元オブジェクトが動作しているテーブルのレコードを取得または設定します。                                                         |
| public FieldId refField(\[FieldId value\])                                                                   |                                                                                                                                       |
| public str getRequestContextQuery()                                                                          |                                                                                                                                       |
| public str requestContextQuery(str value)                                                                    |                                                                                                                                       |
| public FieldId selectField(\[FieldId value\])                                                                |                                                                                                                                       |
| public str toString()                                                                                        | xArgs のインスタンスの文字列形式を取得します。                                                                        |
| public boolean applyRecordAsDynalink(\[boolean applyAsDynalink\])                                            |                                                                                                                                       |
| public void onCallerChanged(\[Object value\])                                                                |                                                                                                                                       |
| public void new(\[AnyType nameOrCaller\], \[Object object\])                                                 | このクラスのインスタンスを構築します。このインスタンスは、FormRun クラスや ReportRun クラスなどの上位クラスに情報を渡すために使用されます。 |
| public void finalize()                                                                                       | メモリから xArgs クラスの現在のインスタンスを削除します。                                                                          |
| public void setupArgs(str parm, int enumType, AnyType enumValue, \[str menuItemName\], \[int menuItemType\]) |                                                                                                                                       |

## <a name="method-allowuseofpreloadedform"></a>メソッド allowUseOfPreloadedForm

このインスタンスに対して起動されたフォームが、プリロードされたフォーム プールから取得されたものかどうかを判定します。

```xpp
public boolean allowUseOfPreloadedForm([boolean value])
```

### <a name="parameters---allowuseofpreloadedform"></a>パラメーター - allowUseOfPreloadedForm

値  
読み込まれたフォームがプリロードされたフォーム プールから取得できるかどうかを決定するブール値。

### <a name="return-value---allowuseofpreloadedform"></a>戻り値 - allowUseOfPreloadedForm

このインスタンスのために起動されるフォームが事前に読み込まれたフォーム プールから取得される可能性がある場合は true。それ以外の場合は、false。

### <a name="remarks---allowuseofpreloadedform"></a>備考 - allowUseOfPreloadedForm

事前に読み込まれているフォームの使用は、既定で許可されています。 事前に読み込まれたフォームを使用して悪影響があった場合にのみ、これを false に設定します。

## <a name="method-arridx"></a>メソッド arrIdx

```xpp
public int arrIdx([int value])
```

### <a name="parameters---arridx"></a>パラメーター - arrIdx

値  

### <a name="return-value---arridx"></a>戻り値 - arrIdx

## <a name="method-caller"></a>メソッド caller

xArgs クラスのこのインスタンスを作成したオブジェクトのインスタンスを取得または設定します。

```xpp
public Object caller([Object value])
```

### <a name="parameters---caller"></a>パラメーター - caller

値  
設定する値 (オプション)。

### <a name="return-value---caller"></a>戻り値 - caller

呼び出し元オブジェクトの現在のインスタンス。

## <a name="method-callerdispatcher"></a>メソッド callerDispatcher

```xpp
public IDispatcherProxy callerDispatcher()
```

### <a name="return-value---callerdispatcher"></a>戻り値 - callerDispatcher

## <a name="method-callerformcontrol"></a>メソッド callerFormControl

```xpp
public FormControl callerFormControl([FormControl value])
```

### <a name="parameters---callerformcontrol"></a>パラメーター - callerFormControl

値  

### <a name="return-value---callerformcontrol"></a>戻り値 - callerFormControl

## <a name="method-callername"></a>メソッド callerName

```xpp
public str callerName()
```

### <a name="return-value---callername"></a>戻り値 - callerName

## <a name="method-callertype"></a>メソッド callerType

```xpp
public UtilElementType callerType()
```

### <a name="return-value---callertype"></a>戻り値 - callerType

## <a name="method-callerid"></a>メソッド callerId

```xpp
public Guid callerId()
```

### <a name="return-value---callerid"></a>戻り値 - callerId

## <a name="method-clientid"></a>メソッド clientId

```xpp
public str clientId([str value])
```

### <a name="parameters---clientid"></a>パラメーター - clientId

値  

### <a name="return-value---clientid"></a>戻り値 - clientId

## <a name="method-copycallerquery"></a>メソッド copyCallerQuery

```xpp
public CopyCallerQuery copyCallerQuery([CopyCallerQuery value])
```

### <a name="parameters---copycallerquery"></a>パラメーター - copyCallerQuery

値  

### <a name="return-value---copycallerquery"></a>戻り値 - copyCallerQuery

## <a name="method-dataset"></a>メソッド dataset

呼び出し元オブジェクトが動作しているテーブルのテーブル ID を取得します。

```xpp
public TableId dataset()
```

### <a name="return-value---dataset"></a>戻り値 - dataset

呼び出し元オブジェクトが動作しているテーブルのテーブル ID。

### <a name="remarks---dataset"></a>備考 - dataset

戻り値は、レコード メソッドで呼び出し元から転送されているレコードの種類を識別するために、頻繁に使用されます。

## <a name="method-designname"></a>メソッド designName

レポートまたはフォームでデザインを示す文字列を取得または設定します。

```xpp
public str designName([str value])
```

### <a name="parameters---designname"></a>パラメーター - designName

値  
設定する値 (オプション)。

### <a name="return-value---designname"></a>戻り値 - designName

## <a name="method-exttype"></a>メソッド extType

```xpp
public ExtendedTypeId extType([ExtendedTypeId edt], [int arrayIndex])
```

### <a name="parameters---exttype"></a>パラメーター - extType

edt  

<!-- -->

arrayIndex  

### <a name="return-value---exttype"></a>戻り値 - extType

## <a name="method-formviewoption"></a>メソッド formViewOption

```xpp
public FormViewOption formViewOption([FormViewOption value])
```

### <a name="parameters---formviewoption"></a>パラメーター - formViewOption

値  

### <a name="return-value---formviewoption"></a>戻り値 - formViewOption

## <a name="method-initialquery"></a>メソッド initialQuery

```xpp
public InitialQueryParameter initialQuery([InitialQueryParameter initialQueryParameter])
```

### <a name="parameters---initialquery"></a>パラメーター - initialQuery

initialQueryParameter  

### <a name="return-value---initialquery"></a>戻り値 - initialQuery

## <a name="method-lookupfield"></a>メソッド lookupField

指定されたレコードの検索に使用するテーブルのフィールド ID を取得または設定します。

```xpp
public FieldId lookupField([FieldId value])
```

### <a name="parameters---lookupfield"></a>パラメーター - lookupField

値  
設定する値 (オプション)。

### <a name="return-value---lookupfield"></a>戻り値 - lookupField

指定されたレコードを検索するために使用するテーブル内のフィールドのフィールド ID。

### <a name="remarks---lookupfield"></a>備考 - lookupField

戻り値は、呼び出されたオブジェクトが LookupRecord メソッド内の指定されたレコードまたは LookupValue メソッドで指定された文字列を検索するために、使用されます。 たとえば、以下を使用して検索するフィールドを設定することができます: xArgs.lookupField(fieldnum(TableName, FieldName));

## <a name="method-lookuprecord"></a>メソッド lookupRecord

指定されたテーブルのレコードを検索します。

```xpp
public Common lookupRecord([Common value])
```

### <a name="parameters---lookuprecord"></a>パラメーター - lookupRecord

値  
レコードを検索するテーブル。

### <a name="return-value---lookuprecord"></a>戻り値 - lookupRecord

指定されたテーブルのレコード。

### <a name="remarks---lookuprecord"></a>備考 - lookupRecord

このメソッドは、呼び出されたオブジェクトが lookupField メソッドから返されるフィールド ID と組み合わせて使用され、このメソッドによって返されるレコード内のフィールドの値を検索します。

## <a name="method-lookuptable"></a>メソッド lookupTable

```xpp
public TableId lookupTable([TableId value])
```

### <a name="parameters---lookuptable"></a>パラメーター - lookupTable

値  

### <a name="return-value---lookuptable"></a>戻り値 - lookupTable

## <a name="method-lookupvalue"></a>メソッド lookupValue

テーブルのフィールドで値を検索する LookupField メソッドで使用する文字列を取得または設定します。

```xpp
public str lookupValue([str value])
```

### <a name="parameters---lookupvalue"></a>パラメーター - lookupValue

値  
設定する値 (オプション)。

### <a name="return-value---lookupvalue"></a>戻り値 - lookupValue

LookupField メソッドで値を検索するために使用する文字列。

## <a name="method-managedcontentitemname"></a>メソッド managedContentItemName

```xpp
public str managedContentItemName([str value])
```

### <a name="parameters---managedcontentitemname"></a>パラメーター - managedContentItemName

値  

### <a name="return-value---managedcontentitemname"></a>戻り値 - managedContentItemName

## <a name="method-menuitemname"></a>メソッド menuItemName

アプリケーション オブジェクトを開始するのに使用するメニュー項目の名前を取得または設定します。

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a>パラメーター - menuItemName

値  
設定する値 (オプション)。

### <a name="return-value---menuitemname"></a>戻り値 - menuItemName

アプリケーション オブジェクトを開始するのに使用するメニュー項目の名前。

### <a name="remarks---menuitemname"></a>備考 - menuItemName

たとえば、メニュー項目を設定するには、以下を使用できます: xArgs.menuItemName(menuitemdisplaystr(CostingVersionPeriodic));

## <a name="method-menuitemtype"></a>メソッド menuItemType

アプリケーション オブジェクトの呼び出しを開始するのに使用するメニュー項目のタイプを取得または設定します。

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a>パラメーター - menuItemType

値  
設定する値 (オプション)。

### <a name="return-value---menuitemtype"></a>戻り値 - menuItemType

アプリケーション オブジェクトの呼び出しを開始するのに使用するメニュー項目のタイプ。

### <a name="remarks---menuitemtype"></a>備考 - menuItemType

メニュー項目タイプは、表示、出力、またはアクションの列挙型のいずれかになります。

## <a name="method-multiselectioncontext"></a>メソッド multiSelectionContext

```xpp
public MultiSelectionContext multiSelectionContext()
```

### <a name="return-value---multiselectioncontext"></a>戻り値 - multiSelectionContext

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  
設定する値 (オプション)。

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることができます。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

たとえば、アプリケーション オブジェクトからフォームを呼び出すには、args.name(formstr(FormName)); を使用できます。

## <a name="method-object"></a>メソッド object

新しいインスタンスを開く対象となるオブジェクトのアプリケーション名を取得および設定します。

```xpp
public Object object([Object value])
```

### <a name="parameters---object"></a>パラメーター - object

値  
設定する値 (オプション)。

### <a name="return-value---object"></a>戻り値 - object

新しいインスタンスを開く対象となるオブジェクトのアプリケーション名。

### <a name="remarks---object"></a>備考 - object

value パラメーターは、次のオブジェクトのいずれかのタイプである場合があります。

-   フォーム
-   報告
-   ジョブ
-   クラス
-   クエリ。

## <a name="method-openmode"></a>メソッド openMode

```xpp
public OpenMode openMode([OpenMode value])
```

### <a name="parameters---openmode"></a>パラメーター - openMode

値  

### <a name="return-value---openmode"></a>戻り値 - openMode

## <a name="method-parentwnd"></a>メソッド parentWnd

```xpp
public Int64 parentWnd([Int64 value])
```

### <a name="parameters---parentwnd"></a>パラメーター - parentWnd

値  

### <a name="return-value---parentwnd"></a>戻り値 - parentWnd

## <a name="method-parm"></a>メソッド parm

呼び出されるオブジェクトのさまざまな情報を指定する文字列を取得または設定します。

```xpp
public str parm([str value])
```

### <a name="parameters---parm"></a>パラメーター - parm

値  
設定する値 (オプション)。

### <a name="return-value---parm"></a>戻り値 - parm

呼び出されるオブジェクトのさまざまな情報を指定する文字列の値。

## <a name="method-parmenum"></a>メソッド parmEnum

parmEnumType メソッドで指定されている列挙型の列挙値を取得または設定します。

```xpp
public AnyType parmEnum([int value])
```

### <a name="parameters---parmenum"></a>パラメーター - parmEnum

値  
設定する列挙型のキー。オプション。

### <a name="return-value---parmenum"></a>戻り値 - parmEnum

parmEnumType メソッドで指定されている列挙型の列挙値。

### <a name="remarks---parmenum"></a>備考 - parmEnum

このメソッドは、次の parmEnumType メソッドでよく使用されます: args.parmEnumType(enumnum(AssetBookType));args.parmEnumType(enumnum(AssetBookType));

## <a name="method-parmenumtype"></a>メソッド parmEnumType

任意の列挙タイプの ID 値を取得または設定します。

```xpp
public int parmEnumType([int value])
```

### <a name="parameters---parmenumtype"></a>パラメーター - parmEnumType

値  
設定する値 (オプション)。

### <a name="return-value---parmenumtype"></a>戻り値 - parmEnumType

列挙型の ID 値。

### <a name="remarks---parmenumtype"></a>備考 - parmEnumType

このメソッドは、parmEnum メソッドとともに使用され、呼び出されたオブジェクトに列挙型の特定の値を送信します。 例: args.parmEnumType(enumnum(AssetBookType));args.parmEnum(AssetBookType::ValueModel);

## <a name="method-parmobject"></a>メソッド parmObject

呼び出されるオブジェクトに渡す任意のオブジェクトのインスタンスを取得または設定します。

```xpp
public Object parmObject([Object value])
```

### <a name="parameters---parmobject"></a>パラメーター - parmObject

値  
設定する値 (オプション)。

### <a name="return-value---parmobject"></a>戻り値 - parmObject

呼び出されるオブジェクトに渡すオブジェクトのインスタンス。

### <a name="remarks---parmobject"></a>備考 - parmObject

オブジェクト多くの場合、クラスになります。

## <a name="method-record"></a>メソッド record

呼び出し元オブジェクトが動作しているテーブルのレコードを取得または設定します。

```xpp
public Common record([Common value])
```

### <a name="parameters---record"></a>パラメーター - record

値  
設定する値 (オプション)。

### <a name="return-value---record"></a>戻り値 - record

呼び出し元オブジェクトが動作しているテーブルのレコード。

### <a name="remarks---record"></a>備考 - record

このメソッドは、呼び出し元のオブジェクトが現在使用しているレコードの値にアクセスするために使用されます。

## <a name="method-reffield"></a>メソッド refField

```xpp
public FieldId refField([FieldId value])
```

### <a name="parameters---reffield"></a>パラメーター - refField

値  

### <a name="return-value---reffield"></a>戻り値 - refField

## <a name="method-getrequestcontextquery"></a>メソッド getRequestContextQuery

```xpp
public str getRequestContextQuery()
```

### <a name="return-value---getrequestcontextquery"></a>戻り値 - getRequestContextQuery

## <a name="method-requestcontextquery"></a>メソッド requestContextQuery

```xpp
public str requestContextQuery(str value)
```

### <a name="parameters---requestcontextquery"></a>パラメーター - requestContextQuery

値  

### <a name="return-value---requestcontextquery"></a>戻り値 - requestContextQuery

## <a name="method-selectfield"></a>メソッド selectField

```xpp
public FieldId selectField([FieldId value])
```

### <a name="parameters---selectfield"></a>パラメーター - selectField

値  

### <a name="return-value---selectfield"></a>戻り値 - selectField

## <a name="method-tostring"></a>メソッド toString

xArgs のインスタンスの文字列形式を取得します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

xArgs クラスのインスタンスの説明を含む文字列。

## <a name="method-applyrecordasdynalink"></a>メソッド applyRecordAsDynalink

```xpp
public boolean applyRecordAsDynalink([boolean applyAsDynalink])
```

### <a name="parameters---applyrecordasdynalink"></a>パラメーター - applyRecordAsDynalink

applyAsDynalink  

### <a name="return-value---applyrecordasdynalink"></a>戻り値 - applyRecordAsDynalink

## <a name="method-oncallerchanged"></a>メソッド onCallerChanged

```xpp
public void onCallerChanged([Object value])
```

### <a name="parameters---oncallerchanged"></a>パラメーター - onCallerChanged

値  

## <a name="method-new"></a>メソッド new

このクラスのインスタンスを構築します。このインスタンスは、FormRun クラスや ReportRun クラスなどの上位クラスに情報を渡すために使用されます。

```xpp
public void new([AnyType nameOrCaller], [Object object])
```

### <a name="parameters---new"></a>パラメーター - new

nameOrCaller  
オブジェクトの引数。オプション。 このパラメーターは、xArgs クラスのインスタンスを作成するために使用され、nameOrCaller パラメーターが呼び出し元の引数である場合に使用されます。

<!-- -->

オブジェクト  
オブジェクトの引数。オプション。 このパラメーターは、xArgs クラスのインスタンスを作成するために使用され、nameOrCaller パラメーターが呼び出し元の引数である場合に使用されます。

### <a name="remarks---new"></a>備考 - new

xArgs オブジェクトを作成するには、(呼び出し元、オブジェクト) のペアまたは Name 引数を指定します。 どちらの引数もオプションであり適切な方法を呼び出すことによって構築した後すべての値を設定することができます。

## <a name="method-finalize"></a>メソッド finalize

メモリから xArgs クラスの現在のインスタンスを削除します。

```xpp
public void finalize()
```

## <a name="method-setupargs"></a>メソッド setupArgs

```xpp
public void setupArgs(str parm, int enumType, AnyType enumValue, [str menuItemName], [int menuItemType])
```

### <a name="parameters---setupargs"></a>パラメーター - setupArgs

parm  

<!-- -->

enumType  

<!-- -->

enumValue  

<!-- -->

menuItemName  

<!-- -->

menuItemType  

