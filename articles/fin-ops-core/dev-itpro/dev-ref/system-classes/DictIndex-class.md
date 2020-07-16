---
title: DictIndex クラス
description: このトピックでは、DictIndex クラスについて説明します。
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
ms.openlocfilehash: 90968356a9543452338e76bc18b3b2ec27977a09
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502986"
---
# <a name="class-dictindex"></a>クラス DictIndex

[!include [banner](../../includes/banner.md)]

```xpp
class DictIndex extends Object
```

DictIndex クラスは、テーブル インデックスに関するメタデータを返します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

次の例では、DictIndex クラスのインスタンスを作成します。

```xpp
Dictionary dict; 
DictTable  table; 
DictIndex  idx; 
dict = new Dictionary(); 
table = new DictTable(dict.tableName2Id("Address")); 
idx = new DictIndex(table.id(), table.indexName2Id("AddrIdx"));
```

## <a name="methods"></a>メソッド

| 方法                                                                                                                          | 説明                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| public boolean allowDuplicates()                                                                                                | インデックスの allowDuplicates プロパティの値を返します。      |
| public ConfigurationKeyId configurationKeyId()                                                                                  | インデックスのコンフィギュレーション キーの ID を返します。                |
| public boolean enabled()                                                                                                        | インデックスが有効かどうかを示す値を返します。          |
| public FieldId field(int fieldNumber)                                                                                           | インデックス内の指定したフィールドの ID を返します。                   |
| public ValidTimeStateMode getValidTimeStateMode()                                                                               |                                                                       |
| public IndexId id()                                                                                                             | インデックスの ID を返します。                                          |
| public FieldId includedColumn(int fieldNumber)                                                                                  |                                                                       |
| public boolean isAlternateKey()                                                                                                 |                                                                       |
| public boolean isSql()                                                                                                          | インデックスが SQL データベースにあるかどうかを示す値を取得します。 |
| public boolean isValidTimeStateKey()                                                                                            |                                                                       |
| public boolean modify(boolean enabled, boolean allowDuplicates, boolean saveInLoadedLayer)                                      | インデックスを変更します。                                                   |
| public str name(\[DbBackend db\])                                                                                               | インデックスの名前を返します。                                        |
| public int numberOfFields()                                                                                                     | インデックス定義のフィールドの数を返します。                 |
| public int numberOfIncludedColumns()                                                                                            |                                                                       |
| public boolean setAlternateKey(boolean alternateKey, boolean saveInLoadedLayer)                                                 |                                                                       |
| public boolean setValidTimeStateKey(boolean setValidTimeStateKey, ValidTimeStateMode validTimeState, boolean saveInLoadedLayer) |                                                                       |
| public TableId tableid()                                                                                                        | インデックスを含むテーブルの ID を返します。                  |
| public void new(TableId tableId, IndexId indexId)                                                                               | Object クラスの新しいインスタンスを初期化します。                       |

## <a name="method-allowduplicates"></a>メソッド allowDuplicates

インデックスの allowDuplicates プロパティの値を返します。

```xpp
public boolean allowDuplicates()
```

### <a name="return-value---allowduplicates"></a>戻り値 - allowDuplicates

インデックスが重複を許容する場合は true。それ以外の場合は、false。

## <a name="method-configurationkeyid"></a>メソッド configurationKeyId

インデックスのコンフィギュレーション キーの ID を返します。

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a>戻り値 - configurationKeyId

インデックスのコンフィギュレーション キーの ID。インデックスにコンフィギュレーション キーがない場合は 0 (ゼロ)。

## <a name="method-enabled"></a>メソッド enabled

インデックスが有効かどうかを示す値を返します。

```xpp
public boolean enabled()
```

### <a name="return-value---enabled"></a>戻り値 - enabled

インデックスが有効である場合は true。それ以外の場合は、false。

## <a name="method-field"></a>メソッド field

インデックス内の指定したフィールドの ID を返します。

```xpp
public FieldId field(int fieldNumber)
```

### <a name="parameters---field"></a>パラメーター - field

fieldNumber  
インデックス内のフィールドの 1 から始まるインデックス。

### <a name="return-value---field"></a>戻り値 - field

fieldNumber により指定されているフィールドの ID。fieldNumber が有効なフィールドを表していない場合は 0 (ゼロ)。

### <a name="examples---field"></a>例 - field

次の例は、インデックス内の各フィールドの取得を示しています。 各フィールドの名前は、ループを使用して表示されます。

```xpp
Dictionary dict; 
DictTable  table; 
DictIndex  idx; 
DictField  field; 
int i; 
dict = new Dictionary(); 
table = new DictTable(dict.tableName2Id("Address")); 
idx = new DictIndex(table.id(), table.indexName2Id("AddrIdx")); 
for (i=1; i <= idx.numberOfFields(); i++) 
{ 
    field = new DictField(table.id(), idx.field(i)); 
    print field.name(); 
}
```

## <a name="method-getvalidtimestatemode"></a>メソッド getValidTimeStateMode

```xpp
public ValidTimeStateMode getValidTimeStateMode()
```

### <a name="return-value---getvalidtimestatemode"></a>戻り値 - getValidTimeStateMode

## <a name="method-id"></a>メソッド id

インデックスの ID を返します。

```xpp
public IndexId id()
```

### <a name="return-value---id"></a>戻り値 - id

インデックスの ID です。

## <a name="method-includedcolumn"></a>メソッド includedColumn

```xpp
public FieldId includedColumn(int fieldNumber)
```

### <a name="parameters---includedcolumn"></a>パラメーター - includedColumn

fieldNumber  

### <a name="return-value---includedcolumn"></a>戻り値 - includedColumn

## <a name="method-isalternatekey"></a>メソッド isAlternateKey

```xpp
public boolean isAlternateKey()
```

### <a name="return-value---isalternatekey"></a>戻り値 - isAlternateKey

## <a name="method-issql"></a>メソッド isSql

インデックスが SQL データベースにあるかどうかを示す値を取得します。

```xpp
public boolean isSql()
```

### <a name="return-value---issql"></a>戻り値 - isSql

インデックスが SQL データベースである場合は true。それ以外の場合は、false。

## <a name="method-isvalidtimestatekey"></a>メソッド isValidTimeStateKey

```xpp
public boolean isValidTimeStateKey()
```

### <a name="return-value---isvalidtimestatekey"></a>戻り値 - isValidTimeStateKey

## <a name="method-modify"></a>メソッド modify

インデックスを変更します。

```xpp
public boolean modify(boolean enabled, boolean allowDuplicates, boolean saveInLoadedLayer)
```

### <a name="parameters---modify"></a>パラメーター - modify

有効  
読み込まれたレイヤーに変更が保存されるかどうかを示すブール値。

<!-- -->

allowDuplicates  
読み込まれたレイヤーに変更が保存されるかどうかを示すブール値。

<!-- -->

saveInLoadedLayer  
読み込まれたレイヤーに変更が保存されるかどうかを示すブール値。

### <a name="return-value---modify"></a>戻り値 - modify

インデックスが正常に修正された場合は true。それ以外の場合は、false。

### <a name="remarks---modify"></a>備考 - modify

このメソッドを使用すると、X++ コードとメタデータを作成、読み込み、更新、および削除ができます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="method-name"></a>メソッド名

インデックスの名前を返します。

```xpp
public str name([DbBackend db])
```

### <a name="parameters---name"></a>パラメーター - 名前

db  
返される名前のタイプを指定する DbBackend 値。 これは、インデックスのネイティブ名の場合は DbBackend::Native、インデックスの SQL 名の場合は DbBackend::Sql になります。 db が指定されていない場合は、DbBackend::Native が使用されます。

### <a name="return-value---name"></a>戻り値 - name

データベースで指定された形式のインデックスの名前。

## <a name="method-numberoffields"></a>メソッド numberOfFields

インデックス定義のフィールドの数を返します。

```xpp
public int numberOfFields()
```

### <a name="return-value---numberoffields"></a>戻り値 - numberOfFields

インデックス内のフィールドの数。

### <a name="examples---numberoffields"></a>例 - numberOfFields

次の例は、インデックス内のフィールド数の取得を示し、インデックス内のフィールドの名前をリストしています。

```xpp
Dictionary dict; 
DictTable  table; 
DictIndex  idx; 
DictField  field; 
int i; 
dict = new Dictionary(); 
table = new DictTable(dict.tableName2Id("Address")); 
idx = new DictIndex(table.id(), table.indexName2Id("AddrIdx")); 
for (i=1; i <= idx.numberOfFields(); i++) 
{ 
    field = new DictField(table.id(), idx.field(i)); 
    print field.name(); 
}
```

## <a name="method-numberofincludedcolumns"></a>メソッド numberOfIncludedColumns

```xpp
public int numberOfIncludedColumns()
```

### <a name="return-value---numberofincludedcolumns"></a>戻り値 - numberOfIncludedColumns

## <a name="method-setalternatekey"></a>メソッド setAlternateKey

```xpp
public boolean setAlternateKey(boolean alternateKey, boolean saveInLoadedLayer)
```

### <a name="parameters---setalternatekey"></a>パラメーター - setAlternateKey

alternateKey  

<!-- -->

saveInLoadedLayer  

### <a name="return-value---setalternatekey"></a>戻り値 - setAlternateKey

## <a name="method-setvalidtimestatekey"></a>メソッド setValidTimeStateKey

```xpp
public boolean setValidTimeStateKey(boolean setValidTimeStateKey, ValidTimeStateMode validTimeState, boolean saveInLoadedLayer)
```

### <a name="parameters---setvalidtimestatekey"></a>パラメーター - setValidTimeStateKey

setValidTimeStateKey  

<!-- -->

validTimeState  

<!-- -->

saveInLoadedLayer  

### <a name="return-value---setvalidtimestatekey"></a>戻り値 - setValidTimeStateKey

## <a name="method-tableid"></a>メソッド tableid

インデックスを含むテーブルの ID を返します。

```xpp
public TableId tableid()
```

### <a name="return-value---tableid"></a>戻り値 - tableid

インデックスを含むテーブルの ID。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(TableId tableId, IndexId indexId)
```

### <a name="parameters---new"></a>パラメーター - new

tableId  
DictIndex クラスのこのインスタンスを作成するために使用されるインデックスの ID。

<!-- -->

indexId  
DictIndex クラスのこのインスタンスを作成するために使用されるインデックスの ID。

