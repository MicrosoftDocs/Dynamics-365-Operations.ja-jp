---
title: MapEnumerator クラス
description: このトピックでは、MapEnumerator クラスについて説明します。
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
ms.openlocfilehash: 874905fd9ddadadbbe46ce244495744271101280
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502884"
---
# <a name="class-mapenumerator"></a>クラス MapEnumerator

[!include [banner](../../includes/banner.md)]

```xpp
class MapEnumerator extends Object
```

MapEnumerator クラスを使用すると、マップ内の要素上を移動できます。

## <a name="remarks"></a>備考

マップ列挙子は、リストの最初の要素の前に開始します。 リストの最初の要素を指すようにするために MapEnumerator.moveNext メソッドを呼び出す必要があります。 Map.getEnumerator メソッドが呼び出されたときに、マップと同じ層で列挙子が自動的に作成されるため、MapIterator クラスではなく、MapEnumerator クラスを使用することがベスト プラクティスです。 MapEnumerator クラスを使用すると、Called from としてマークされたコードの潜在的な問題が回避されます。反復子とマップは別々の層に置くことができます。 さらに、マップ列挙子はマップ反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。 マップ反復子を使用する必要がある唯一の状況は、MapIterator.delete メソッドを使用してリストから項目を削除する場合です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                        | 説明                                                                                                                                       |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| public AnyType current()      | このメソッドは廃止されました。代わりに MapEnumerator.currentKey を使用してください。                                                                                    |
| public AnyType currentKey()   | 現在列挙子によってポイントされている (キー、値) ペアからキーを返します。                                                        |
| public AnyType currentValue() | 現在列挙子によってポイントされている (キー、値) ペアから値を返します。                                                      |
| public str definitionString() | 列挙子の説明を返します。 たとえば、文字列への整数のマップの列挙子は、「\[int -&gt; str\] 列挙子」を返します。 |
| public boolean moveNext()     | 列挙子が有効なマップ要素を指すかどうかを決定します。                                                                                  |
| public str toString()         | 現在のオブジェクトを表す文字列を返します。                                                                                              |
| public void new(Map map)      | Object クラスの新しいインスタンスを初期化します。                                                                                                   |
| public void reset()           | 列挙子を移動して、マップ内の最初の要素の直前をポイントします。                                                                        |

## <a name="method-current"></a>メソッド current

このメソッドは廃止されました。代わりに MapEnumerator.currentKey を使用してください。

```xpp
public AnyType current()
```

### <a name="return-value---current"></a>戻り値 - current

## <a name="method-currentkey"></a>メソッド currentKey

現在列挙子によってポイントされている (キー、値) ペアからキーを返します。

```xpp
public AnyType currentKey()
```

### <a name="return-value---currentkey"></a>戻り値 - currentKey

現在列挙子によってポイントされているマップ要素のキー。

### <a name="remarks---currentkey"></a>備考 - currentKey

CurrentKey メソッドを呼び出す前に、MapEnumerator.moveNext メソッドを呼び出す必要があります。

### <a name="examples---currentkey"></a>例 - currentKey

次の例では、マップ内の特定のテーブル ID を検索し、そのマップ要素のキー値を返します。

```xpp
private LabelType tableLabel(tableId _tableId) 
{ 
    LabelType     labelType; 
    MapEnumerator mapEnum; 
    mapEnum = tableAllMap.getEnumerator(); 
    while (mapEnum.moveNext()) 
    { 
        if (_tableId == mapEnum.currentValue()) 
        { 
            labelType = mapEnum.currentKey(); 
            break; 
        } 
    } 
    return labelType; 
}
```

## <a name="method-currentvalue"></a>メソッド currentValue

現在列挙子によってポイントされている (キー、値) ペアから値を返します。

```xpp
public AnyType currentValue()
```

### <a name="return-value---currentvalue"></a>戻り値 - currentValue

現在列挙子によってポイントされているマップ要素の値。

### <a name="remarks---currentvalue"></a>備考 - currentValue

このメソッドを呼び出す前に、MapEnumerator.moveNext メソッドを呼び出す必要があります。

### <a name="examples---currentvalue"></a>例 - currentValue

次の例では、マップを検索して、パラメーターとして渡された値と等しい値を持つ要素を検索します。 MapEnumerator.moveNext メソッドは、マップを反復処理するために使用され、currentValue メソッドは各値をテストしてパラメーターと一致するかどうかを確認するために使用されます。

```xpp
private LabelType tableLabel(tableId _tableId) 
{ 
    LabelType     labelType; 
    MapEnumerator mapEnum; 
    mapEnum = tableAllMap.getEnumerator(); 
    while (mapEnum.moveNext()) 
    { 
        if (_tableId == mapEnum.currentValue()) 
        { 
            labelType = mapEnum.currentKey(); 
            break; 
        } 
    } 
    return labelType; 
}
```

## <a name="method-definitionstring"></a>メソッド definitionString

列挙子の説明を返します。 たとえば、文字列への整数のマップの列挙子は、「\[int -&gt; str\] 列挙子」を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

列挙子の説明を含む文字列。

### <a name="examples---definitionstring"></a>例 - definitionString

次の例では、マップとその列挙子を作成し、列挙子の定義を出力します。

```xpp
{ 
    Map myMap = new Map(Types::Integer, Types::String); 
    MapEnumerator  enumerator; 
    int i; 
    // Add some elements to the map 
    myMap.insert(1, "Element one"); 
    myMap.insert(2, "Element two"); 
    myMap.insert(3, "Element three"); 
    myMap.insert(4, "Element Four"); 
    // Set the enumerator 
    enumerator = myMap.getEnumerator(); 
    print enumerator.definitionString(); 
    pause; 
}
```

## <a name="method-movenext"></a>メソッド moveNext

列挙子が有効なマップ要素を指すかどうかを決定します。

```xpp
public boolean moveNext()
```

### <a name="return-value---movenext"></a>戻り値 - moveNext

マップ内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は false。

### <a name="remarks---movenext"></a>備考 - moveNext

マップ列挙子は、マップの最初の要素の前に開始します。 マップの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。

### <a name="examples---movenext"></a>例 - moveNext

次の例では、moveNext メソッドを使用してプロジェクトに含まれるテーブルを反復処理し、テーブルの DictTable オブジェクトを含む新しいマップに追加します。 (DictTable を使用すると、テーブルに関する情報にアクセスできます。)

```xpp
{ 
    Map map = Map::create( 
        SysUmlDataModel::getProjectTablesClient(projectNode)); 
    MapEnumerator enum = map.getEnumerator(); 
    TableName tableName; 
    while (enum.moveNext()) 
    { 
        tableName = enum.currentKey(); 
        map.insert(tableName, new DictTable(tablename2id(tableName))); 
    } 
    return map; 
}
```

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="examples---tostring"></a>例 - toString

次の例では、マップを作成し、最初の要素と 2 番目の要素の内容をマップに出力します。

```xpp
{ 
    Map myMap = new Map(Types::Integer, Types::String); 
    MapEnumerator  enumerator; 
    int i; 
     // Add some elements to the map 
    myMap.insert(1, "Element one"); 
    myMap.insert(2, "Element two"); 
    myMap.insert(3, "Element three"); 
    myMap.insert(4, "Element Four"); 
    // Set the enumerator 
    enumerator = myMap.getEnumerator(); 
    // Go to beginning of enumerator 
    enumerator.reset(); 
    // Go to the first element in the map 
    enumerator.moveNext(); 
    // Print first item in the map 
    print enumerator.toString(); 
    // go to second element 
     enumerator.moveNext(); 
    // Print second element in map 
    print enumerator.toString(); 
    pause; 
}
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(Map map)
```

### <a name="parameters---new"></a>パラメーター - new

マップ  
列挙子を作成するマップ。

### <a name="remarks---new"></a>備考 - new

 メソッドは廃止されています。 代わりに Map.getEnumerator メソッドを使用します。

## <a name="method-reset"></a>メソッド reset

列挙子を移動して、マップ内の最初の要素の直前をポイントします。

```xpp
public void reset()
```

### <a name="remarks---reset"></a>備考 - reset

reset メソッドは、列挙子をセットの先頭、セットの最初の要素の前に移動します。 セットの最初の要素を指すようにするために MapEnumerator.moveNext メソッドを呼び出す必要があります。

