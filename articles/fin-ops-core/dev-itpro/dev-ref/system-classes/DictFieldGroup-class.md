---
title: DictFieldGroup クラス
description: このトピックでは、DictFieldGroup クラスについて説明します。
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
ms.openlocfilehash: b8e6dcecbcdc4299c77fafe4f638ce4097822a09
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502988"
---
# <a name="class-dictfieldgroup"></a>クラス DictFieldGroup

[!include [banner](../../includes/banner.md)]

```xpp
class DictFieldGroup extends Object
```

DictFieldGroup クラスは、テーブル内の固有のフィールド グループに関する情報を提供します。

## <a name="remarks"></a>備考

このクラスを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                             | 説明                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| public FieldId field(int fieldNumber)                                              | フィールド グループから指定したフィールドを返します。                                   |
| public str label()                                                                 | フィールド グループのラベル テキストを返します。                                          |
| public str labelId()                                                               | フィールド グループのラベル ID を返します。                                            |
| public str methodName(FieldId fieldId)                                             | フィールド グループから指定したメソッドの名前を返します。                      |
| public str name()                                                                  | フィールド グループの名前を返します。                                                |
| public int numberOfFields()                                                        | フィールド グループのテーブル フィールドの数と編集メソッドと表示メソッドを返します。 |
| public TableId tableid()                                                           | フィールド グループに関連付けられたテーブル ID を返します。                |
| public void new(TableId tableId, str FieldGroupName, \[TableId includeBaseTable\]) | Object クラスの新しいインスタンスを初期化します。                                     |

## <a name="method-field"></a>メソッド field

フィールド グループから指定したフィールドを返します。

```xpp
public FieldId field(int fieldNumber)
```

### <a name="parameters---field"></a>パラメーター - field

fieldNumber  
フィールド グループのフィールド内のフィールドへの 1 から始まるインデックス。 インデックスは、アプリケーション オブジェクト ツリー (AOT) と同じ順序です。

### <a name="return-value---field"></a>戻り値 - field

フィールドのフィールド ID。 品目が表示メソッドの場合は、ID は、フォーム 65280 + 0 から始まるメソッドのインデックスになります。

### <a name="remarks---field"></a>備考 - field

フィールド メソッドを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。

## <a name="method-label"></a>メソッド label

フィールド グループのラベル テキストを返します。

```xpp
public str label()
```

### <a name="return-value---label"></a>戻り値 - label

フィールド グループのラベル テキスト。

## <a name="method-labelid"></a>メソッド labelId

フィールド グループのラベル ID を返します。

```xpp
public str labelId()
```

### <a name="return-value---labelid"></a>戻り値 - LabelId

フィールド グループのラベル ID。

## <a name="method-methodname"></a>メソッド methodName

フィールド グループから指定したメソッドの名前を返します。

```xpp
public str methodName(FieldId fieldId)
```

### <a name="parameters---methodname"></a>パラメーター - methodName

fieldId  
返されるメソッド名のフィールド メソッドへの呼び出しから返されるフィールド ID。 有効なフィールド ID が使用されていることを確認するのは開発者の責任です。

### <a name="return-value---methodname"></a>戻り値 - methodName

フィールド グループから指定されたメソッドの名前。fieldId の値が 65280 より小さい場合は空の文字列。

### <a name="remarks---methodname"></a>備考 - methodName

メソッドは、メソッド インデックス + 65280 によって指定されます。 このメソッドを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。

## <a name="method-name"></a>メソッド名

フィールド グループの名前を返します。

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

フィールド グループの名前。

## <a name="method-numberoffields"></a>メソッド numberOfFields

フィールド グループのテーブル フィールドの数と編集メソッドと表示メソッドを返します。

```xpp
public int numberOfFields()
```

### <a name="return-value---numberoffields"></a>戻り値 - numberOfFields

フィールド グループのテーブル フィールドの数と編集メソッドと表示メソッド。

### <a name="examples---numberoffields"></a>例 - numberOfFields

次の例は、フィールド グループのテーブル フィールド数と編集メソッドおよび表示メソッドの数の取得を示しています。

```xpp
    DictFieldGroup  fldGrp; 
    DictField       fld; 
    fieldId         fldId; 
    tableId         tblId; 
    int             i; 
    tblId = tablenum("CustTable"); 
    fldGrp = new DictFieldGroup(tblId,"AutoReport"); 
    if (fldGrp) 
    {     for (i=1; i <= fldGrp.numberOfFields(); i++) 
         { 
             fldId = fldGrp.field(i); 
             fld  = new DictField(tblId, fldId); 
             if (fld) 
             { 
                print 'Field: ' + fld.name() 
       + ' (' + int2str(fldId) + ')'; 
             } 
             else 
             { 
                print 'MethodName: ' + fldGrp.methodName(fldId)  
                + ' (' + int2str(fldId) + ')'; 
             } 
         } 
    }
```

## <a name="method-tableid"></a>メソッド tableid

フィールド グループに関連付けられたテーブル ID を返します。

```xpp
public TableId tableid()
```

### <a name="return-value---tableid"></a>戻り値 - tableid

フィールド グループに関連付けられたテーブル ID。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(TableId tableId, str FieldGroupName, [TableId includeBaseTable])
```

### <a name="parameters---new"></a>パラメーター - new

tableId  

<!-- -->

FieldGroupName  

<!-- -->

includeBaseTable  

### <a name="remarks---new"></a>備考 - new

このメソッドを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。

