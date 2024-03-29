---
title: サーバー側の開発 (ワークスペース X++ API)
description: この記事では、携帯電話アプリをサポートするプラットフォームについて説明します。このプラットフォームは、充実したオフラインおよびモバイルの相互関係、および使いやすいデザイナー エクスペリエンスを提供します。
author: jasongre
ms.date: 05/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.custom: 255544
ms.openlocfilehash: 5040a0e0bde9ff5b690af7b43b23c8b8c9982c32
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284397"
---
# <a name="server-side-development-workspace-x-apis"></a>サーバー側の開発 (ワークスペース X++ API)

[!include [banner](../../includes/banner.md)]
[!include [mobile app deprecated](../../includes/mobile-app-deprecation-banner.md)]

## <a name="class-sysappactionattribute"></a>クラス SysAppActionAttribute

ワークスペースのアクションを定義するメソッドの修飾に使用される SysAppActionAttribute

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppActionAttribute クラスの新しいインスタンスを作成する |
| pageMethodName | str | このタスクが存在するページを形成する Page メソッド名を取得します |
| actionTitle | str | アクション タイトルの取得 |
| actionDescription | str | アクション説明の取得 |
| crudOperationType | SysAppCRUDOperation | 作成、更新、削除などの CRUD 操作タイプを取得 |

### <a name="method-new"></a>メソッド new

SysAppActionAttribute クラスの新しいインスタンスを作成する

```xpp
public void new ([str _actionTitle], [str _actionDescription], [SysAppCRUDOperation _crudOperationType], [str _pageMethodName])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|
| _actionTitle | str | はい | アクション タイトル
| _actionDescription | str | はい | アクション説明
| _crudOperationType | SysAppCRUDOperation | はい | 作成、更新、削除などの CRUD の操作
| _pageMethodName | str | はい | 親ページを構築するメソッドの名前

### <a name="method-pagemethodname"></a>メソッド pageMethodName

このタスクが存在するページを形成する Page メソッド名を取得します

```xpp
public str pageMethodName ()
```

#### <a name="return-value"></a>戻り値

このタスクが存在するページを形成する Page メソッド名

### <a name="method-actiontitle"></a>メソッド actionTitle

アクション タイトルの取得

```xpp
public str actionTitle ()
```

#### <a name="return-value"></a>戻り値

アクション タイトル

### <a name="method-actiondescription"></a>メソッド actionDescription

アクション説明の取得

```xpp
public str actionDescription ()
```

#### <a name="return-value"></a>戻り値

ページの説明

### <a name="method-crudoperationtype"></a>メソッド crudOperationType

作成、更新、削除などの CRUD 操作タイプを取得

```xpp
public SysAppCRUDOperation crudOperationType ()
```

#### <a name="return-value"></a>戻り値

作成、更新、削除などの CRUD 操作タイプ

## <a name="class-sysappactionmetadata"></a>クラス SysAppActionMetadata

このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。

### <a name="methods"></a>方法

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 |  |
| getActionName | str | アクション名を返します |
| actionTitle | str | アクション タイトルの取得または設定 |
| actionDescription | str | アクションの説明の取得または設定 |
| actionHidden | ブール値 | アクションが非表示かどうかを取得または設定 |
| actionOrder | int | アクション順序の取得または設定 |
| getControl | SysAppControlMetadata | 指定されたコントロールの名前を持つ現在のアクションのコントロールを返します |
| getControlEnumerator | MapEnumerator | アクションの制御を列挙するために使用できるマップ列挙子を返します。  ここで、Key はコントロール名で、値は SysAppControlMetadata 型です |

### <a name="method-new"></a>メソッド new

```xpp
public void new (Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata _taskmetadata)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|
| _taskmetadata | Microsoft.Dynamics.Client.ServerForm.App.TaskMetadata | False |

### <a name="method-getactionname"></a>メソッド getActionName

アクション名を返します

```xpp
public str getActionName ()
```

#### <a name="return-value"></a>戻り値

アクション名

### <a name="method-actiontitle"></a>メソッド actionTitle

アクション タイトルの取得または設定

```xpp
public str actionTitle ([str _actionTitle])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|
| _actionTitle | str | はい | アクション タイトル

#### <a name="return-value"></a>戻り値

アクション タイトル

### <a name="method-actiondescription"></a>メソッド actionDescription

アクションの説明の取得または設定

```xpp
public str actionDescription ([str _actionDescription])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|
| _actionDescription | str | はい | アクションの説明

#### <a name="return-value"></a>戻り値

アクションの説明

### <a name="method-actionhidden"></a>メソッド actionHidden

アクションが非表示かどうかを取得または設定

```xpp
public boolean actionHidden ([boolean _actionHidden])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|
| _actionHidden | ブール値 | はい | アクションの非表示値

#### <a name="return-value"></a>戻り値

アクションが非表示の場合は true。それ以外の場合は、false。

### <a name="method-actionorder"></a>メソッド actionOrder

アクション順序の取得または設定

```xpp
public int actionOrder ([int _actionOrder])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|
| _actionOrder | int | はい | アクションの順序

#### <a name="return-value"></a>戻り値

アクションの順序

### <a name="method-getcontrol"></a>メソッド getControl

指定されたコントロールの名前を持つ現在のアクションのコントロールを返します

```xpp
public SysAppControlMetadata getControl (str _controlName)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|
| _controlName | str | False | コントロールを検索するために使用されるコントロール名

#### <a name="return-value"></a>戻り値

指定されたコントロール名を持つコントロールがアクションに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null

### <a name="method-getcontrolenumerator"></a>メソッド getControlEnumerator

アクションの制御を列挙するために使用できるマップ列挙子を返します。  ここで、Key はコントロール名で、値は SysAppControlMetadata 型です

```xpp
public MapEnumerator getControlEnumerator ()
```

#### <a name="return-value"></a>戻り値

マップ列挙子

## <a name="class-sysappattributehelper"></a>クラス SysAppAttributeHelper

拡張されたすべてのクラスから属性を取得するための SysAppAttributeHelper クラス

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| getAttributeFromClass | SysAttribute | クラスから属性を取得します |

### <a name="method-getattributefromclass"></a>メソッド getAttributeFromClass

クラスから属性を取得します

```xpp
public SysAttribute getAttributeFromClass (SysDictClass _sysClass, SysAppAttributeType _attributeType)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|
| _sysClass | SysDictClass | False | 属性が必要なクラス
| _attributeType | SysAppAttributeType | False | SysAppEntityAttribute と同様の属性の型

## <a name="class-sysappcollectionattribute"></a>クラス SysAppCollectionAttribute

リスト コントロールを形成するメソッドの修飾に使用される SysAppCollectionAttribute

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | コンストラクター |

### <a name="method-new"></a>メソッド new

コンストラクター

```xpp
public void new (str _itemContractName, [str _label], [str _relationshipName])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|
| _itemContractName | str | False | リスト項目のデータ契約名
| _label | str | はい | リスト コントロール ラベル
| _relationshipName | str | はい | 関係名。 既定では、一覧項目のエンティティ名はリレーションシップ名として使用します。

## <a name="class-sysappcontrolmetadata"></a>クラス SysAppControlMetadata

容易にする管理対象 ControlMetadata オブジェクト上の X++ ラッパーを表します。  X++ オブジェクトとしてオブジェクトを回覧

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | コントロールのメタデータの新しいインスタンスを作成する |
| getBaseLanguageId | str | アプリケーションの基本言語 ID を返します |
| getControlName | str | コントロール名を返します |
| controlLabel | str | コントロール ラベルの取得および設定 |
| controlHidden | ブール値 | コントロールを非表示にするかどうかの取得および設定 |
| controlOrder | int | コントロール順序の取得または設定 |
| controlMandatory | ブール値 | 必須コントロールの取得または設定 |
| controlAllowNegative | ブール値 | 負の値を許可するコントロールを取得または設定します |
| controlMaxLength | int | コントロールの最大長の取得または設定 |
| getProperty | `anytype` | キーによって参照されるコントロール プロパティを取得します。 |
| setProperty | 無効 | キーによって参照されるコントロール プロパティを設定します。 |

### <a name="method-new"></a>メソッド new

コントロールのメタデータの新しいインスタンスを作成する

```xpp
public void new (Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata _controlMetadata, [str _baseLanguageId])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _controlMetadata | Microsoft.Dynamics.Client.ServerForm.App.ControlMetadata | False | controlMetadata オブジェクト
| _baseLanguageId | str | はい | 基本言語

### <a name="method-getbaselanguageid"></a>メソッド getBaseLanguageId

アプリケーションの基本言語 ID を返します

```xpp
public str getBaseLanguageId ()
```

#### <a name="return-value"></a>戻り値

基本言語 ID

### <a name="method-getcontrolname"></a>メソッド getControlName

コントロール名を返します

```xpp
public str getControlName ()
```

#### <a name="return-value"></a>戻り値

コントロールの名前。

### <a name="method-controllabel"></a>メソッド controlLabel

コントロール ラベルの取得および設定

```xpp
public str controlLabel ([str _controlLabel])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _controlLabel | str | はい | コントロール ラベル

#### <a name="return-value"></a>戻り値

コントロール ラベル

### <a name="method-controlhidden"></a>メソッド controlHidden

コントロールを非表示にするかどうかの取得および設定

```xpp
public boolean controlHidden ([boolean _controlHidden])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _controlHidden | ブール値 | はい | 非表示値の制御

#### <a name="return-value"></a>戻り値

コントロールが非表示の場合は true。それ以外の場合は、false。

### <a name="method-controlorder"></a>メソッド controlOrder

コントロール順序の取得または設定

```xpp
public int controlOrder ([int _controlOrder])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _controlOrder | int | はい | コントロール順序

#### <a name="return-value"></a>戻り値

コントロール順序

### <a name="method-controlmandatory"></a>メソッド controlMandatory

必須コントロールの取得または設定

```xpp
public boolean controlMandatory ([boolean _controlMandatory])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _controlMandatory | ブール値 | はい | 必須のコントロール

#### <a name="return-value"></a>戻り値

必須のコントロール

### <a name="method-controlallownegative"></a>メソッド controlAllowNegative

負の値を許可するコントロールを取得または設定します

```xpp
public boolean controlAllowNegative ([boolean _controlAllowNegative])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _controlAllowNegative | ブール型 | True | コントロールは負の値を許可します

#### <a name="return-value"></a>戻り値

コントロールは負の値を許可します

### <a name="method-controlmaxlength"></a>メソッド controlMaxLength

コントロールの最大長の取得または設定

```xpp
public int controlMaxLength ([int _controlMaxLength])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _controlMaxLength | int | はい | コントロールの最大長

#### <a name="return-value"></a>戻り値

コントロールの最大長

### <a name="method-getproperty"></a>メソッド getProperty

キーによって参照されるコントロール プロパティを取得します。

```xpp
public anytype getProperty (str _key)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _key | str | False | コントロール プロパティの名前。

#### <a name="return-value"></a>戻り値

プロパティ値。

### <a name="method-setproperty"></a>メソッド setProperty

キーによって参照されるコントロール プロパティを設定します。

```xpp
public void setProperty (str _key, anytype _value)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _key | str | False | コントロール プロパティの名前。
| _value | anytype | False | コントロール プロパティの値

## <a name="class-sysappentityattribute"></a>クラス SysAppEntityAttribute

データ契約エンティティの修飾に使用される SysAppEntityAttribute

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | コンストラクター |
| 名前 | str | エンティティの名前の取得 |
| entityKey | str | エンティティ キーの取得 |

### <a name="method-new"></a>メソッド new

コンストラクター

```xpp
public void new (str _name, str _entityKey)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _name | str | False | エンティティ名
| _entityKey | str | False | エンティティのキーの名前

### <a name="method-name"></a>メソッド名

エンティティの名前の取得

```xpp
public str name ()
```

#### <a name="return-value"></a>戻り値

エンティティの名前

### <a name="method-entitykey"></a>メソッド entityKey

エンティティ キーの取得

```xpp
public str entityKey ()
```

#### <a name="return-value"></a>戻り値

エンティティ キー

## <a name="class-sysappentitycontext"></a>クラス SysAppEntityContext

エンティティ コンテキストを定義するために使用される SysAppEntityContext

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| constructFromParams | SysAppEntityContext | entityName と entityId から SysAppEntityContext を構築します。 |
| constructFromBuffer | SysAppEntityContext | テーブル バッファーから SysAppEntityContext を構築 |
| entityName | str | フィルターを適用するエンティティ名 |
| entityId | str | フィルターを適用するフィールド値 |

### <a name="method-constructfromparams"></a>メソッド constructFromParams

entityName と entityId から SysAppEntityContext を構築します。

```xpp
public SysAppEntityContext constructFromParams (str _entityName, str _entityId)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _entityName | str | False | エンティティ名
| _entityId | str | False | エンティティの値

#### <a name="return-value"></a>戻り値

SysAppEntityContext のインスタンス

### <a name="method-constructfrombuffer"></a>メソッド constructFromBuffer

テーブル バッファーから SysAppEntityContext を構築

```xpp
public SysAppEntityContext constructFromBuffer (Common _tableBuffer)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _tableBuffer | 共通 | False | エンティティを形成するテーブル バッファ

#### <a name="return-value"></a>戻り値

SysAppEntityContext のインスタンス

### <a name="method-entityname"></a>メソッド entityName

フィルターを適用するエンティティ名

```xpp
public str entityName ([str _entityName])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _entityName | str | はい | エンティティ名

#### <a name="return-value"></a>戻り値

エンティティ名

### <a name="method-entityid"></a>メソッド entityId

フィルターを適用するフィールド値

```xpp
public str entityId ([str _entityId])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _entityId | str | はい | エンティティの値

#### <a name="return-value"></a>戻り値

エンティティの値

## <a name="class-sysappfieldattribute"></a>クラス SysAppFieldAttribute

連結フィールドを形成するメソッドの修飾に使用される SysAppFieldAttribute

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppFieldAttribute クラスの新しいインスタンスを作成する |

### <a name="method-new"></a>メソッド new

SysAppFieldAttribute クラスの新しいインスタンスを作成する

```xpp
public void new (str _fieldName, str _label)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _fieldName | str | False | コントロールがバインドされるエンティティ フィールド名
| _label | str | False | コントロール ラベル

## <a name="class-sysappfieldmultiselecthelper"></a>クラス SysAppFieldMultiSelectHelper

D365 モバイル アプリケーションで使用される複数のシナリオを選択するためのヘルパー メソッドを提供するヘルパー クラス。

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する |
| getSelectedRecIds | コンテナー | 選択されたレコードの recIds のコンテナーを返します |
| getSelectedValues | コンテナー | 選択した値のコンテナーを返します |
| getSelectedRecords | 共通 | 選択したすべてのレコードを含むバッファーを返します。  バッファが temp. としてマークされます。  後で、while-Select はすべてのレコードを反復処理するために使用できます |
| setControlValue | 無効 | 複数選択コントロール値を設定するセッター |

### <a name="method-new"></a>メソッド new

SysAppFieldMultiSelectHelper クラスの新しいインスタンスを作成する

```xpp
public void new (TableId _multiSelectTableId, FieldId _valueFieldId, FormStringControl _multiSelectControl)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _multiSelectTableId | TableId | False | フィールドのバッキング tableId。
| _valueFieldId | FieldId | False | 複数選択コントロールに表示されるフィールドの fieldId
| _multiSelectControl | FormStringControl | False | 複数選択コントロールになる文字列コントロール

### <a name="method-getselectedrecids"></a>メソッド getSelectedRecIds

選択されたレコードの recIds のコンテナーを返します

```xpp
public container getSelectedRecIds ()
```

#### <a name="return-value"></a>戻り値

選択されたレコードの recOds のコンテナー

### <a name="method-getselectedvalues"></a>メソッド getSelectedValues

選択した値のコンテナーを返します

```xpp
public container getSelectedValues ()
```

#### <a name="return-value"></a>戻り値

選択した値のコンテナー

### <a name="method-getselectedrecords"></a>メソッド getSelectedRecords

選択したすべてのレコードを含むバッファーを返します。  バッファが temp. としてマークされます。  後で、while-Select はすべてのレコードを反復処理するために使用できます

```xpp
public Common getSelectedRecords ()
```

#### <a name="return-value"></a>戻り値

選択したすべてのレコードを含むバッファー

### <a name="method-setcontrolvalue"></a>メソッド setControlValue

複数選択コントロール値を設定するセッター

```xpp
public void setControlValue (str _value)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _value | str | False | SysAppFieldMultiSelectHelper によって使用されるコロン区切り値

## <a name="class-sysappfiltercontext"></a>クラス SysAppFilterContext

コンテキスト値を保持している SysAppFilterContext クラス

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| entityName | str | フィルターを適用するエンティティ名 |
| filterFieldName | str | フィルターを適用するフィールド名 |
| filterFieldValueList | リスト | フィルター処理動作に基づくフィルターの一覧フィールド値の取得 |
| 演算子 | str | 結果のフェッチに使用される演算子 |
| addFilterFieldValue | 無効 | フィルター フィールド値の追加 |

### <a name="method-entityname"></a>メソッド entityName

フィルターを適用するエンティティ名

```xpp
public str entityName ([str _entityName])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _entityName | str | はい | フィルターを適用するエンティティ名

#### <a name="return-value"></a>戻り値

フィルターを適用するエンティティ名

### <a name="method-filterfieldname"></a>メソッド filterFieldName

フィルターを適用するフィールド名

```xpp
public str filterFieldName ([str _filterFieldName])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _filterFieldName | str | はい | フィルターを適用するフィールド名

#### <a name="return-value"></a>戻り値

フィルターを適用するフィールド名

### <a name="method-filterfieldvaluelist"></a>メソッド filterFieldValueList

フィルター処理動作に基づくフィルターの一覧フィールド値の取得

```xpp
public List filterFieldValueList ()
```

#### <a name="return-value"></a>戻り値

フィルター処理動作に基づくフィルターの一覧フィールド値

### <a name="method-operator"></a>メソッド operator

結果のフェッチに使用される演算子

```xpp
public str operator ([str _operator])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _operator | str | はい | 結果のフェッチに使用される演算子

#### <a name="return-value"></a>戻り値

結果のフェッチに使用される演算子

### <a name="method-addfilterfieldvalue"></a>メソッド addFilterFieldValue

フィルター フィールド値の追加

```xpp
public void addFilterFieldValue ( _filterFieldValueList)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _filterFieldValueList |  | False | フィルター処理動作に基づくフィルター フィールド値

## <a name="class-sysapplookupattribute"></a>クラス SysAppLookUpAttribute

ルックアップ ページでもあるページの修飾に使用される SysAppPageAttribute

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppLookUpAttribute クラスの新しいインスタンスを作成する |
| displayFieldName | str | ルックアップ コントロールの表示フィールド名を取得します。 |
| valueFieldName | str | ルックアップ コントロールのフィールド名の値の取得 |

### <a name="method-new"></a>メソッド new

SysAppLookUpAttribute クラスの新しいインスタンスを作成する

```xpp
public void new (str _displayFieldName, str _valueFieldName)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _displayFieldName | str | False | ルックアップ表示フィールド。 ルックアップ ページの任意のコントロールの名前
| _valueFieldName | str | False | ルックアップの値フィールド。 ルックアップ ページを構築しているルート データ コントラクトによって形成されたコントロールの名前

### <a name="method-displayfieldname"></a>メソッド displayFieldName

ルックアップ コントロールの表示フィールド名を取得します。

```xpp
public str displayFieldName ()
```

#### <a name="return-value"></a>戻り値

ルックアップ コントロールの表示フィールド名

### <a name="method-valuefieldname"></a>メソッド valueFieldName

ルックアップ コントロールのフィールド名の値の取得

```xpp
public str valueFieldName ()
```

#### <a name="return-value"></a>戻り値

ルックアップ コントロールのフィールド名値

## <a name="class-sysapplookupfieldattribute"></a>クラス SysAppLookupFieldAttribute

アクションのフィールドのルックアップの修飾に使用される SysAppLookupFieldAttribute

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する |
| entityName | str | ルックアップ ページが関連するエンティティの名前の取得 |

### <a name="method-new"></a>メソッド new

SysAppLookupFieldAttribute クラスの新しいインスタンスを作成する

```xpp
public void new ( _name)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _name |  | False | ルックアップ ページが関連するエンティティの名前

### <a name="method-entityname"></a>メソッド entityName

ルックアップ ページが関連するエンティティの名前の取得

```xpp
public str entityName ()
```

#### <a name="return-value"></a>戻り値

エンティティの名前

## <a name="class-sysapppageattribute"></a>クラス SysAppPageAttribute

ワークスペースのページを定義するメソッドの修飾に使用される SysAppPageAttribute

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppPageAttribute クラスの新しいインスタンスを作成する |
| pageTitle | str | ページのページのタイトルの取得 |
| pageDescription | str | ページの説明の取得 |

### <a name="method-new"></a>メソッド new

SysAppPageAttribute クラスの新しいインスタンスを作成する

```xpp
public void new ([str _pageTitle], [str _pageDescription])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _pageTitle | str | はい | ページ タイトル
| _pageDescription | str | はい | ページの説明

### <a name="method-pagetitle"></a>メソッド pageTitle

ページのページのタイトルの取得

```xpp
public str pageTitle ()
```

#### <a name="return-value"></a>戻り値

ページ タイトル

### <a name="method-pagedescription"></a>メソッド pageDescription

ページの説明の取得

```xpp
public str pageDescription ()
```

#### <a name="return-value"></a>戻り値

ページの説明

## <a name="class-sysapppagemetadata"></a>クラス SysAppPageMetadata

このクラスを使用すると、AX モバイル ワークスペースのページ メタデータにアクセスして更新できます。

### <a name="methods"></a>方法

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 |  |
| getPageName | str | ページ名を返します |
| pageTitle | str | ページ タイトルの取得および設定 |
| pageDescription | str | ページの説明の取得または設定 |
| pageHidden | ブール値 | ワークスペースでページを表示にするかどうかの取得および設定 |
| pageOrder | int | ページ順序の取得または設定 |
| getControl | SysAppControlMetadata | 指定されたコントロールの名前を持つ現在のページのコントロールを返します |
| getControlEnumerator | MapEnumerator | ページ コントロールを列挙するために使用できるマップ列挙子を返します。  ここで、Key はコントロール名で、値は SysAppControlMetadata 型です |

### <a name="method-new"></a>メソッド new

```xpp
public void new (Microsoft.Dynamics.Client.ServerForm.App.PageMetadata _pageMetadata)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _pageMetadata | Microsoft.Dynamics.Client.ServerForm.App.PageMetadata | False |

### <a name="method-getpagename"></a>メソッド getPageName

ページ名を返します

```xpp
public str getPageName ()
```

#### <a name="return-value"></a>戻り値

ページ名

### <a name="method-pagetitle"></a>メソッド pageTitle

ページ タイトルの取得および設定

```xpp
public str pageTitle ([str _pageTitle])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _pageTitle | str | はい | ページ タイトル

#### <a name="return-value"></a>戻り値

ページ タイトル

### <a name="method-pagedescription"></a>メソッド pageDescription

ページの説明の取得または設定

```xpp
public str pageDescription ([str _pageDescription])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _pageDescription | str | はい | ページの説明

#### <a name="return-value"></a>戻り値

ページの説明>

### <a name="method-pagehidden"></a>メソッド pageHidden

ワークスペースでページを表示にするかどうかの取得および設定

```xpp
public boolean pageHidden ([boolean _pageHidden])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _pageHidden | ブール値 | はい | ページの非表示の値

#### <a name="return-value"></a>戻り値

ワークスペースに現在のページが表示されない場合は true。それ以外の場合 false。

### <a name="method-pageorder"></a>メソッド pageOrder

ページ順序の取得または設定

```xpp
public int pageOrder ([int _pageOrder])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _pageOrder | int | はい | ページの順序

#### <a name="return-value"></a>戻り値

ページの順序

### <a name="method-getcontrol"></a>メソッド getControl

指定されたコントロールの名前を持つ現在のページのコントロールを返します

```xpp
public SysAppControlMetadata getControl (str _controlName)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _controlName | str | False | コントロールを検索するために使用されるコントロール名

#### <a name="return-value"></a>戻り値

指定されたコントロール名を持つコントロールがページに存在する場合、SysAppControlMetadata のオブジェクトは返されます。それ以外の場合は null

### <a name="method-getcontrolenumerator"></a>メソッド getControlEnumerator

ページ コントロールを列挙するために使用できるマップ列挙子を返します。  ここで、Key はコントロール名で、値は SysAppControlMetadata 型です

```xpp
public MapEnumerator getControlEnumerator ()
```

#### <a name="return-value"></a>戻り値

マップ列挙子

## <a name="class-sysappprojectionattribute"></a>クラス SysAppProjectionAttribute

非連結フィールドを形成するメソッドの修飾に使用される SysAppProjectionAttribute

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する |

### <a name="method-new"></a>メソッド new

SysAppControlMetadataAttributes クラスの新しいインスタンスを作成する

```xpp
public void new (str _label)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _label | str | False | コントロール ラベル

## <a name="class-sysapprelationalattribute"></a>クラス SysAppRelationalAttribute

参照コントロールの修飾に使用される SysAppRelationalAttribute

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | コンストラクター |

### <a name="method-new"></a>メソッド new

コンストラクター

```xpp
public void new ([str _name])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _name | str | はい | 参照されるエンティティのプロパティ名

## <a name="class-sysapprequestparams"></a>クラス SysAppRequestParams

詳細とアクション ページを生成するための X++ メソッドのクラスをリクエスト

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| entityContext | SysAppEntityContext | 要求のエンティティ コンテキスト |
| filterContext | リスト | フィルター コンテキストの SysAppFilterContext のリスト |

### <a name="method-entitycontext"></a>メソッド entityContext

要求のエンティティ コンテキスト

```xpp
public SysAppEntityContext entityContext ([SysAppEntityContext _entityContext])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _entityContext | SysAppEntityContext | はい | 要求のエンティティ コンテキスト

#### <a name="return-value"></a>戻り値

要求のエンティティ コンテキスト

### <a name="method-filtercontext"></a>メソッド filterContext

フィルター コンテキストの SysAppFilterContext のリスト

```xpp
public List filterContext ([List _filterContext])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _filterContext | リスト | はい | ページのフィルター コンテキストの SysAppFilterContext のリスト

#### <a name="return-value"></a>戻り値

ページのフィルター コンテキストの SysAppFilterContext のリスト

## <a name="class-sysappresponse"></a>クラス SysAppResponse

SysAppResponse クラス。  このクラスは、生成されたページおよびアクションのレスポンス オブジェクトを保持します。

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 |  |
| jobId | str | 要求のジョブ ID |
| データ | Microsoft.Dynamics.Client.ServerForm.App.CompositeData | ページのデータ |
| failedInAppCall | ブール値 | ページのデータ |
| commits | 一覧 | タスクが完了した後にコミットします。 |
| メッセージ | 一覧 | 要求のジョブ ID |
| addMessage | 無効 | メッセージの追加 |
| addCommit | 無効 | コミットの追加 |

### <a name="method-new"></a>メソッド new

```xpp
public void new ()
```

### <a name="method-jobid"></a>メソッド jobId

要求のジョブ ID

```xpp
public str jobId ()
```

#### <a name="return-value"></a>戻り値

要求のジョブ ID

### <a name="method-data"></a>メソッド data

ページのデータ

```xpp
public Microsoft.Dynamics.Client.ServerForm.App.CompositeData data ([Microsoft.Dynamics.Client.ServerForm.App.CompositeData _data])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _data | Microsoft.Dynamics.Client.ServerForm.App.CompositeData | はい | ページのデータ

#### <a name="return-value"></a>戻り値

ページのデータ

### <a name="method-failedinappcall"></a>メソッド failedInAppCall

ページのデータ

```xpp
public boolean failedInAppCall ([boolean _failedInAppCall])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _failedInAppCall | ブール値 | はい | アプリケーション コードの呼び出しに失敗した場合は true に設定します。

#### <a name="return-value"></a>戻り値

アプリケーション コードの呼び出しに失敗した場合は true です。

### <a name="method-commits"></a>メソッド commits

タスクが完了した後にコミットします。

```xpp
public List commits ()
```

#### <a name="return-value"></a>戻り値

タスクが完了した後にコミットします。

### <a name="method-messages"></a>メソッド messages

要求のジョブ ID

```xpp
public List messages ()
```

#### <a name="return-value"></a>戻り値

タスクが完了した後のメッセージ

### <a name="method-addmessage"></a>メソッド addMessage

メッセージの追加

```xpp
public void addMessage (SysAppResponseMessage _message)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _message | SysAppResponseMessage | False | SysAppResponseMessage オブジェクトとしてのメッセージ

### <a name="method-addcommit"></a>メソッド addCommit

コミットの追加

```xpp
public void addCommit (SysAppEntityContext _entityContext)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _entityContext | SysAppEntityContext | False | 確定済エンティティのエンティティ名とエンティティ ID を含むエンティティ コンテキスト

## <a name="class-sysappresponsemessage"></a>クラス SysAppResponseMessage

応答メッセージの SysAppResponseMessage クラス

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppResponseMessage クラスの新しいインスタンスを作成する |
| テキスト | str | メッセージ テキストの取得 |
| タイプ | SysAppMessageType | メッセージ タイプを取得します: 情報、エラー、警告 |

### <a name="method-new"></a>メソッド new

SysAppResponseMessage クラスの新しいインスタンスを作成する

```xpp
public void new (str _text, [SysAppMessageType _type])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _text | str | False | メッセージ テキスト
| _type | SysAppMessageType | はい | メッセージ タイプ: 情報、エラー、警告

### <a name="method-text"></a>メソッド text

メッセージ テキストの取得

```xpp
public str text ()
```

#### <a name="return-value"></a>戻り値

メッセージ テキスト

### <a name="method-type"></a>メソッドのタイプ

メッセージ タイプを取得します: 情報、エラー、警告

```xpp
public SysAppMessageType type ()
```

#### <a name="return-value"></a>戻り値

メッセージ タイプ: 情報、エラー、警告

## <a name="class-sysappsecurityattribute"></a>クラス SysAppSecurityAttribute

ページおよびアクションを形成するメソッドの修飾に使用される SysAppSecurityAttribute。  ページまたはアクションのセキュリティ属性を指定します

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppSecurityAttribute クラスの新しいインスタンスを作成します。  これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます |
| menuItemType | MenuItemType | ページのメニュー項目タイプの取得 |
| menuItemName | MenuItemName | ページのメニュー項目名の取得 |

### <a name="method-new"></a>メソッド new

SysAppSecurityAttribute クラスの新しいインスタンスを作成します。  これは、ログインしたユーザーが指定されたメニュー項目とメニュー項目の種類にアクセスできるかどうかを確認するのに役立ちます

```xpp
public void new ([MenuItemName _menuItemName], [MenuItemType _menuItemType])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _menuItemName | MenuItemName | はい | ページのメニュー項目名
| _menuItemType | MenuItemType | True | アクション、表示、または出力など、ページのメニュー項目タイプ

### <a name="method-menuitemtype"></a>メソッド menuItemType

ページのメニュー項目タイプの取得

```xpp
public MenuItemType menuItemType ()
```

#### <a name="return-value"></a>戻り値

ページのメニュー項目タイプ

### <a name="method-menuitemname"></a>メソッド menuItemName

ページのメニュー項目名の取得

```xpp
public MenuItemName menuItemName ()
```

#### <a name="return-value"></a>戻り値

ページのメニュー項目名

## <a name="class-sysappworkspace"></a>クラス SysAppWorkspace

これは、 モバイル ワークスペースの基本クラスです。 モバイル ワークスペース クラスは、このクラスから拡張する必要があります

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| getEnumValues | リスト | ワークスペースの初期化中に呼び出されます。 AX モバイルに返される列挙型の値を変更するために使用できます |
| getWorkspaceMetadata | SysAppWorkspaceMetadata | ワークスペースの初期化中に呼び出されます。 ワークスペースのメタデータを変更するために使用できます |
| onBeginAppJob | 無効 | AX モバイル ジョブの実行開始前の呼び出し |
| onEndAppJob | 無効 | AX モバイル ジョブの実行の終了後の呼び出し |
| workspaceHidden | ブール値 | ワークスペースを非表示にするかどうかを制御するために使用できます。  現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。  クラスに属性が指定されていない場合は常に false を返します |

### <a name="method-getenumvalues"></a>メソッド getEnumValues

ワークスペースの初期化中に呼び出されます。 AX モバイルに返される列挙型の値を変更するために使用できます

```xpp
public List getEnumValues (EnumName _enumName)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _enumName | EnumName | False | 列挙名

#### <a name="return-value"></a>戻り値

列挙値の一覧

### <a name="method-getworkspacemetadata"></a>メソッド getWorkspaceMetadata

ワークスペースの初期化中に呼び出されます。 ワークスペースのメタデータを変更するために使用できます

```xpp
public SysAppWorkspaceMetadata getWorkspaceMetadata ()
```

#### <a name="return-value"></a>戻り値

ワークスペース メタデータを表すオブジェクト

### <a name="method-onbeginappjob"></a>メソッド onBeginAppJob

AX モバイル ジョブの実行開始前の呼び出し

```xpp
public void onBeginAppJob (SysAppJobRequest _sysAppJobRequest)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _sysAppJobRequest | SysAppJobRequest | False | ジョブ要求パラメーターを含むクラス

### <a name="method-onendappjob"></a>メソッド onEndAppJob

AX モバイル ジョブの実行の終了後の呼び出し

```xpp
public void onEndAppJob (SysAppJobResponse _sysAppJobResponse)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _sysAppJobResponse | SysAppJobResponse | False | ジョブ応答パラメーターを含むクラス

### <a name="method-workspacehidden"></a>メソッド workspaceHidden

ワークスペースを非表示にするかどうかを制御するために使用できます。  現在のユーザーに、ワークスペース クラスの SysAppWorkspaceSecurityAttribute で指定されたアクセス メニュー項目があることを確認します。  クラスに属性が指定されていない場合は常に false を返します

```xpp
public boolean workspaceHidden ()
```

#### <a name="return-value"></a>戻り値

ワークスペースが非表示の場合は true を返します。それ以外の場合は、false を返します

## <a name="class-sysappworkspaceattribute"></a>クラス SysAppWorkspaceAttribute

SysAppWorkspace から拡張されたクラスに適用されます。

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する |
| AppId | str | ワークスペースの AppId の取得または設定 |
| AppResourceName | str | ワークスペースを含む AOT リソース名の取得または設定 |
| WorkspaceHidden | ブール型 | ワークスペースがデザイナーに非表示かどうかを取得または設定 |

### <a name="method-new"></a>メソッド new

SysAppWorkspaceAttribute クラスの新しいインスタンスを作成する

```xpp
public void new (str _appId, [str _appResourceName], [boolean _workspaceHidden])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _appId | str | False | ワークスペースの appId
| _appResourceName | str | True | ワークスペースを含む AOT リソース名
| _workspaceHidden | ブール型 | True | ワークスペースはデザイナーには表示されません

### <a name="method-appid"></a>メソッド AppId

ワークスペースの AppId の取得または設定

```xpp
public str AppId ([str _appId])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _appId | str | はい | ワークスペースの AppId

#### <a name="return-value"></a>戻り値

ワークスペースの AppId

### <a name="method-appresourcename"></a>メソッド AppResourceName

ワークスペースを含む AOT リソース名の取得または設定

```xpp
public str AppResourceName ([str _appResourceName])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _appResourceName | str | True | ワークスペースを含む AOT リソース名

#### <a name="return-value"></a>戻り値

ワークスペースを含む AOT リソース名

### <a name="method-workspacehidden"></a>メソッド WorkspaceHidden

ワークスペースがデザイナーに非表示かどうかを取得または設定

```xpp
public boolean WorkspaceHidden ([boolean _workspaceHidden])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _workspaceHidden | ブール値 | はい | 非表示のワークスペース

#### <a name="return-value"></a>戻り値

ワークスペースがデザイナーに非表示かどうか

## <a name="class-sysappworkspacemetadata"></a>クラス SysAppWorkspaceMetadata

このクラスを使用すると、AX モバイル ワーク スペースのアクション メタデータにアクセスして更新できます。

### <a name="methods"></a>方法

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 |  |
| addConfig | 無効 | モバイル ワークスペース メタデータにカスタム構成を追加します。 |
| getPage | SysAppPageMetadata | 提供される pageName を持つページを返します |
| getPageEnumerator | MapEnumerator | ワークスペース ページを列挙するために使用できるマップ列挙子を返します。  ここで、key はページ名で、値は SysAppPageMetadata 型です |
| getAction | SysAppActionMetadata | 提供される actionName を持つアクションを返します |
| getActionEnumerator | MapEnumerator | ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。  ここで、key はアクション名で、値は SysAppActionMetadata 型です |
| getPageNameForRecordingId | str | 指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します |
| getActionNameForRecordingId | str | 指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します |
| workspaceTitle | str | ワークスペース タイトルの取得および設定 |
| workspaceDescription | str | ワークスペースの説明の取得および設定 |

### <a name="method-new"></a>メソッド new

```xpp
public void new (str _appId, [SysAppWorkspaceAttribute _attribute])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _appId | str | False |
| _attribute | SysAppWorkspaceAttribute | はい |

### <a name="method-addconfig"></a>メソッド addConfig

モバイル ワークスペース メタデータにカスタム構成を追加します。

```xpp
public void addConfig (str _configName, object _configValue)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _configName | str | False | コンフィギュレーション名
| _configValue | オブジェクト | False | X++ データ契約クラスのオブジェクト

### <a name="method-getpage"></a>メソッド getPage

提供される pageName を持つページを返します

```xpp
public SysAppPageMetadata getPage (str _pageName)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _pageName | str | False | ページ名

#### <a name="return-value"></a>戻り値

指定した名前を持つページが存在する場合は pageMetadata を返します。それ以外の場合は null を返します

### <a name="method-getpageenumerator"></a>メソッド getPageEnumerator

ワークスペース ページを列挙するために使用できるマップ列挙子を返します。  ここで、key はページ名で、値は SysAppPageMetadata 型です

```xpp
public MapEnumerator getPageEnumerator ()
```

#### <a name="return-value"></a>戻り値

マップ列挙子

### <a name="method-getaction"></a>メソッド getAction

提供される actionName を持つアクションを返します

```xpp
public SysAppActionMetadata getAction (str _actionName)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _actionName | str | False | アクション名

#### <a name="return-value"></a>戻り値

指定した名前を持つアクションが存在する場合は ActionMetadata を返します。それ以外の場合は null を返します

### <a name="method-getactionenumerator"></a>メソッド getActionEnumerator

ワークスペース アクションを列挙するために使用できるマップ列挙子を返します。  ここで、key はアクション名で、値は SysAppActionMetadata 型です

```xpp
public MapEnumerator getActionEnumerator ()
```

#### <a name="return-value"></a>戻り値

マップ列挙子

### <a name="method-getpagenameforrecordingid"></a>メソッド getPageNameForRecordingId

指定された recordingId がワークスペース ページによって使用されている場合、pageName を返します

```xpp
public str getPageNameForRecordingId (str _recordingId)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _recordingId | str | False | recordingId

#### <a name="return-value"></a>戻り値

指定された recordingId をワークスペース ページで使用している場合のページ名です。それ以外は空の文字列です。

### <a name="method-getactionnameforrecordingid"></a>メソッド getActionNameForRecordingId

指定された recordingId がワークスペース アクションによって使用されている場合、actionName を返します

```xpp
public str getActionNameForRecordingId (str _recordingId)
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _recordingId | str | False | recordingId

#### <a name="return-value"></a>戻り値

指定された recordingId をワークスペース アクションで使用している場合のアクション名です。それ以外は空の文字列です

### <a name="method-workspacetitle"></a>メソッド workspaceTitle

ワークスペース タイトルの取得および設定

```xpp
public str workspaceTitle ([str _workspaceTitle])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _workspaceTitle | str | はい | ワークスペースのタイトル

#### <a name="return-value"></a>戻り値

ワークスペースのタイトル

### <a name="method-workspacedescription"></a>メソッド workspaceDescription

ワークスペースの説明の取得および設定

```xpp
public str workspaceDescription ([str _workspaceDescription])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _workspaceDescription | str | はい | ワークスペースの説明

#### <a name="return-value"></a>戻り値

ワークスペースの説明

## <a name="class-sysappworkspacesecurityattribute"></a>クラス SysAppWorkspaceSecurityAttribute

この属性に関連付けられたメニュー項目に基づいて、ワークスペースに基づく表示をコントロールします。

### <a name="methods"></a>メソッド

| メソッド名 | 返品 | 説明 |
|---|---|---|
| 新規 | 無効 | 属性の新しいインスタンスの作成 |
| WorkspaceMenuItemName | MenuItemName | ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定 |
| WorkspaceMenuItemType | MenuItemType | ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定 |

### <a name="method-new"></a>メソッド new

属性の新しいインスタンスの作成

```xpp
public void new (MenuItemName _workspaceMenuItemName, [MenuItemType _workspaceMenuItemType])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _workspaceMenuItemName | MenuItemName | False | ワークスペースを関連付ける必要のあるメニュー項目名
| _workspaceMenuItemType | MenuItemType | はい | メニュー項目タイプ

### <a name="method-workspacemenuitemname"></a>メソッド WorkspaceMenuItemName

ワークスペース セキュリティ属性のワークスペース menuItem の取得または設定

```xpp
public MenuItemName WorkspaceMenuItemName ([MenuItemName _workspaceMenuItemName])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _workspaceMenuItemName | MenuItemName | はい | ワークスペース セキュリティ属性のワークスペース メニュー項目

#### <a name="return-value"></a>戻り値

ワークスペース セキュリティ属性のワークスペース メニュー項目

### <a name="method-workspacemenuitemtype"></a>メソッド WorkspaceMenuItemType

ワークスペース セキュリティ属性のワークスペース メニュー項目タイプの取得または設定

```xpp
public MenuItemType WorkspaceMenuItemType ([MenuItemType _workspaceMenuItemType])
```

#### <a name="parameters"></a>パラメーター

| パラメーター名 |  パラメーター タイプ | オプション | 説明 |
|---|---|---|---|
| _workspaceMenuItemType | MenuItemType | True | `workspacesecurity` 属性のワークスペース メニュー項目タイプ

#### <a name="return-value"></a>戻り値

ワークスペース セキュリティ属性のワークスペース メニュー項目タイプ


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
