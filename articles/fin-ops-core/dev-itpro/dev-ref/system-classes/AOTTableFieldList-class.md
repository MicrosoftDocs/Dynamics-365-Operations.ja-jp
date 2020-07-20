---
title: AOTTableFieldList クラス
description: このトピックでは、AOTTableFieldList クラスについて説明します。
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
ms.openlocfilehash: efb1cdc1d5f5a3afe1e95314657f0525361d6dd8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502752"
---
# <a name="class-aottablefieldlist"></a>クラス AOTTableFieldList

[!include [banner](../../includes/banner.md)]

```xpp
class AOTTableFieldList extends TreeNode
```

AOTTableFieldList クラスは、テーブルのフィールド ノードを表し、フィールドをテーブルに追加するためにも使用されます。

## <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 開発者は、他の方法を使用してノードに関する一般的な情報を取得できます。

## <a name="examples"></a>例

次の例では、列挙型のフィールドを TutorialJournalName テーブルに追加します。

```xpp
{ 
    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
```

```xpp
     if (!tfl.AOTFindChild('NewEnum')) 
     { 
         tfl.addEnum('NewEnum');  // Adds the field NewEnum. 
     } 
}
```

## <a name="methods"></a>メソッド

| 方法                             | 説明                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| public void addInteger(str name)   | 現在のテーブルのフィールドのリストに整数型の新しいフィールドを追加します。   |
| public void addGuid(str name)      |                                                                                     |
| public void addContainer(str name) | 現在のテーブルのフィールドのリストにコンテナー型の新しいフィールドを追加します。 |
| public void addInt64(str name)     |                                                                                     |
| public void addDateTime(str name)  |                                                                                     |
| public void addDate(str name)      | 現在のテーブルのフィールドのリストに日付型の新しいフィールドを追加します。      |
| public void addString(str name)    | 現在のテーブルのフィールドのリストに文字列型の新しいフィールドを追加します。    |
| public void addReal(str name)      | 現在のテーブルのフィールドのリストに実数型の新しいフィールドを追加します。      |
| public void addTime(str name)      | 現在のテーブルのフィールドのリストに時刻タイプの新しいフィールドを追加します。      |
| public void addEnum(str name)      | 現在のテーブルのフィールドのリストに列挙型の新しいフィールドを追加します。      |

## <a name="method-addinteger"></a>メソッド addInteger

現在のテーブルのフィールドのリストに整数型の新しいフィールドを追加します。

```xpp
public void addInteger(str name)
```

### <a name="parameters---addinteger"></a>パラメーター - addInteger

名前  
追加するフィールドの名前。

### <a name="remarks---addinteger"></a>備考 - addInteger

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

### <a name="examples---addinteger"></a>例 - addInteger

次のコード例は、整数型である、NewInteger フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
if (!tfl.AOTFindChild('NewInteger')) 
{ 
    tfl.addInteger('NewInteger'); 
}
```

## <a name="method-addguid"></a>メソッド addGuid

```xpp
public void addGuid(str name)
```

### <a name="parameters---addguid"></a>パラメーター - addGuid

名前  

## <a name="method-addcontainer"></a>メソッド addContainer

現在のテーブルのフィールドのリストにコンテナー型の新しいフィールドを追加します。

```xpp
public void addContainer(str name)
```

### <a name="parameters---addcontainer"></a>パラメーター -addContainer

名前  
追加するフィールドの名前。

### <a name="remarks---addcontainer"></a>備考 - addContainer

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

### <a name="examples---addcontainer"></a>例 - addContainer

次のコード例は、NewContainer フィールドと NewContainer1 フィールド (両方ともコンテナー タイプ) を TutorialJournalName テーブルのフィールドのリストに追加します。

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
```

```xpp
// Add a NewContainer field. 
tfl.addContainer('NewContainer'); 
```

```xpp
// Add a NewContainer1 field. 
tfl.addContainer('NewContainer');
```

## <a name="method-addint64"></a>メソッド addInt64

```xpp
public void addInt64(str name)
```

### <a name="parameters---addint64"></a>パラメーター - addInt64

名前  

## <a name="method-adddatetime"></a>メソッド addDateTime

```xpp
public void addDateTime(str name)
```

### <a name="parameters---adddatetime"></a>パラメーター - addDateTime

名前  

## <a name="method-adddate"></a>メソッド addDate

現在のテーブルのフィールドのリストに日付型の新しいフィールドを追加します。

```xpp
public void addDate(str name)
```

### <a name="parameters---adddate"></a>パラメーター - addDate

名前  
追加するフィールドの名前。

### <a name="remarks---adddate"></a>備考 - addDate

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

### <a name="examples---adddate"></a>例 - addDate

次のコード例は、日付タイプである、NewDate フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
if (!tfl.AOTFindChild('NewDate')) 
{ 
    tfl.addDate('NewDate'); 
}
```

## <a name="method-addstring"></a>メソッド addString

現在のテーブルのフィールドのリストに文字列型の新しいフィールドを追加します。

```xpp
public void addString(str name)
```

### <a name="parameters---addstring"></a>パラメーター - addString

名前  
追加するフィールドの名前。

### <a name="remarks---addstring"></a>備考 - addString

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

### <a name="examples---addstring"></a>例 - addString

次の例では、文字列型の NewString フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

```xpp
{ 
    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewString')) 
    { 
        tfl.addString('NewString'); 
    } 
}
```

## <a name="method-addreal"></a>メソッド addReal

現在のテーブルのフィールドのリストに実数型の新しいフィールドを追加します。

```xpp
public void addReal(str name)
```

### <a name="parameters---addreal"></a>パラメーター - addReal

名前  
追加するフィールドの名前。

### <a name="remarks---addreal"></a>備考 - addReal

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

### <a name="examples---addreal"></a>例 - addReal

次の例では、実際の型の NewReal フィールドと NewReal1 フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
// Add the field NewReal. 
tfl.addReal('NewReal'); 
// Add the field NewReal1. 
tfl.addReal('NewReal');
```

## <a name="method-addtime"></a>メソッド addTime

現在のテーブルのフィールドのリストに時刻タイプの新しいフィールドを追加します。

```xpp
public void addTime(str name)
```

### <a name="parameters---addtime"></a>パラメーター - addTime

名前  
追加するフィールドの名前。

### <a name="remarks---addtime"></a>備考 - addTime

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

### <a name="examples---addtime"></a>例 - addTime

次のコード例は、時間タイプである、NewTime フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
if (!tfl.AOTFindChild('NewTime')) 
{ 
    tfl.addTime('NewTime'); 
}
```

## <a name="method-addenum"></a>メソッド addEnum

現在のテーブルのフィールドのリストに列挙型の新しいフィールドを追加します。

```xpp
public void addEnum(str name)
```

### <a name="parameters---addenum"></a>パラメーター - addEnum

名前  
追加するフィールドの名前。

### <a name="remarks---addenum"></a>備考 - addEnum

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

### <a name="examples---addenum"></a>例 - addEnum

次の例では、列挙型の NewEnum フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
if (!tfl.AOTFindChild('NewEnum')) 
{ 
    tfl.addEnum('NewEnum');  // adds the field NewEnum 
}
```

