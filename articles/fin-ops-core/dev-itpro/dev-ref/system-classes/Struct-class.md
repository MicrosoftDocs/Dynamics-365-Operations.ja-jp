---
title: Struct クラス
description: このトピックでは、Struct クラスについて説明します。
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
ms.openlocfilehash: a0bd9b1be951ca89c4e7321869aea256ec6e2e70
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502795"
---
# <a name="class-struct"></a>クラス構造体

[!include [banner](../../includes/banner.md)]

```xpp
class Struct extends Object
```

構造体は、特定のエンティティに関する情報をグループ化するために、任意の X++ 型の複数値を保持します。

## <a name="remarks"></a>備考

構造体 (略構造) は、すべての X++ 型の複数値を保持できるエンティティです。 構造体は、特定のエンティティに関する情報をグループ化するために使用されます。 たとえば、顧客の名前、年齢、および住所に関する情報を格納し、それからこの複合情報を 1つの項目として扱う場合があります。 構造体内の項目は、データ型と名前で指定されます。 項目は、new メソッドを使用して構造体が作成される場合に追加されるか、add メソッドを使用して構造体が作成された後に作成されます。 Add メソッドを使用して品目を追加する場合は、同時に品目の値を指定し、この値からデータ型が推測されます。 構造体のインスタンス化中に品目を追加する場合は、値または valueIndex メソッドを使用して、値を割り当てる必要があります。 構造体内の項目は、文字列型、整数型、実数型、日付型、コンテナー型、レコード型、クラス型など、型システムの列挙型にあるデータ型のいずれでもかまいません。 構造体内の項目は、項目名のアルファベット順に並べられます。 構造体のフィールドは、fields、fieldName、および fieldType メソッドを使用してスキャンできます。 構造体は、コンテナーに梱包し、後で Struct::create メソッドを使用して復元できます。 構造体には、X++ コンテナーとのいくつかの類似点があります。 ただし、コンテナーは値の型であり、X++ 言語に組み込まれています。 入れ子になったコンテナを作成することができますが、入れ子になった構造体は作成することができません。 X++ クラスは、構造とほぼ同じ方法で情報を保管することができます。 クラスはデータを操作する方法を供給することができますが、構造体のための該当する機能は提供されておらず、上書きまたは拡張の概念はありません。 クラスは AOT でのみ作成できますが、構造体は作成されたコードのコンテキスト内にのみ存在します。 クラス メンバーの変数はクラス専用なので、アクセサー関数はクラスの外部から使用される値のためにコード化されている必要があります。 構造体内の項目は一般にアクセス可能です。

## <a name="examples"></a>例

次の例では、2 つの項目を含む構造体を作成し、その項目に値を割り当てます。 Struct.add メソッドを使用して新しい項目が追加されます。項目のデータ型は割り当てられた値から推測されます。 次に、構造体はコンテナーに梱包され、元の構造体のコピーである新しい構造体を作成するために使用されます。

```xpp
{ 
    Struct s = new struct ("int age; str name"); 
    Struct copy; 
    container c; 
    int i; 
    // Add values to the items 
    s.value("age", 25); 
    s.value("name", "Jane Dow"); 
  // Add a new item; data type is inferred from value 
    s.add("Shoesize", 45); 
    // Print the definition of the struct 
    print s.definitionString(); 
    // Prints the type and name of all items in the struct 
    for (i =  1;   i <= s.fields();i++) 
    { 
         print s.fieldType(i), " ", s.fieldName(i); 
    }  
    // Pack the struct into a container and restore it into copy 
    c = s.pack(); 
    copy = Struct::create(c); 
    print copy.definitionString(); 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                                                        | 説明                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| public boolean add(str fieldName, AnyType value)              | 構造体に新しい項目を追加し、指定した値を割り当てます。                          |
| public str definitionString()                                 | 構造体の要素の名前およびタイプの説明を返します。                   |
| public boolean exists(str fieldName)                          | 特定の項目が構造体に存在するかどうかを判定します。                                      |
| public str fieldName(int index)                               | 指定された位置にある構造体内の項目の名前を返します。                         |
| public int fields()                                           | 構造体内の項目の数を返します。                                                    |
| public Types fieldType(int index)                             | 指定された位置にある構造体内の項目のデータ型を返します。                    |
| public int index(str fieldName)                               | 名前に基づいて構造体の項目の位置を計算します。                           |
| public container pack()                                       | Struct クラスの現在のインスタンスをシリアル化します。                                          |
| public boolean remove(str fieldName)                          | 構造体から品目を削除します。                                                                |
| public str toString()                                         | 構造体の内容を説明する文字列を返します。                                   |
| public AnyType value(str fieldName, \[AnyType value\])        | 構造体で指定される品目の値を取得または設定します。                                      |
| public str valueImage(int index)                              | 構造体内の特定の位置にある品目の値を説明する文字列を返します。 |
| public AnyType valueIndex(int index, \[AnyType value\])       | 構造体で指定される位置での品目の値を取得または設定します。                       |
| public str xml(\[int indent\])                                | 現在のオブジェクトを表す XML 文字列を返します。                                     |
| ::public static Struct create(container container)            | 以前の Struct.pack の呼び出しで取得されたコンテナーから構造体を作成します。          |
| ::public static Struct createFromXML(Object xmlnode)          |                                                                                               |
| ::public static boolean equal(Struct struct1, Struct struct2) | 2 つの構造体が等しいかどうかを判断します。                                                     |
| ::public static Struct merge(Struct struct1, Struct struct2)  | 2 つの構造体を組み合わせ、新しい構造体を作成します。                                                  |
| public void new(VarArg specifier)                             | 構造体を作成します。                                                                             |

## <a name="method-add"></a>メソッド add

構造体に新しい項目を追加し、指定した値を割り当てます。

```xpp
public boolean add(str fieldName, AnyType value)
```

### <a name="parameters---add"></a>パラメーター - add

fieldName  
新しい項目に割り当てる値 (オプション)。 この値は、アイテムのタイプを定義します。

<!-- -->

値  
新しい項目に割り当てる値 (オプション)。 この値は、アイテムのタイプを定義します。

### <a name="return-value---add"></a>戻り値 - add

値が構造体に追加された場合は true。値を追加することができなかった場合は (既に構造体に存在していた場合は) false。

### <a name="remarks---add"></a>備考 - add

値のタイプは値の内容から推測されます。 構造体内の項目は、項目名に従ってアルファベット順に並べられます。 構造体の項目の値は、Struct.value メソッドまたは Struct.valueIndex メソッドを使用して変更できます。

### <a name="examples---add"></a>例 - add

次の例では、名前および年齢フィールドの 2 つの項目を持つ構造体を作成し、それらの項目に値を割り当てます。 その後、add メソッドを使用して、43 という値の shoeSize 変数が追加項目として作成されます。 値のタイプによって、新しい項目のタイプ int が決まります。

```xpp
{ 
    Struct s = new Struct ("str name; int age"); 
    // Prints number of items (2) 
    print s.fields(); 
    // Values are assigned to the two items 
    s.value("name", "John"); 
    s.value("age", 34); 
    //Another item is added to the struct 
    s.add("shoeSize", 43); 
    // Prints number of item (3) 
    print s.fields(); 
    // Prints a description of the items in the struct 
    print s.definitionString(); 
    pause; 
}
```

## <a name="method-definitionstring"></a>メソッド definitionString

構造体の要素の名前およびタイプの説明を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

構造体の定義を含む文字列。

### <a name="remarks---definitionstring"></a>備考 - definitionString

definitionString メソッドを使用すると、構文 newStruct = new struct(oldStruct.definitionString()); を用いて構造体のコピーを作成することができます。

## <a name="method-exists"></a>メソッド exists

特定の項目が構造体に存在するかどうかを判定します。

```xpp
public boolean exists(str fieldName)
```

### <a name="parameters---exists"></a>パラメーター - exists

fieldName  
チェックするアイテムの名前。

### <a name="return-value---exists"></a>戻り値 - exists

項目が構造体内に存在する場合は true。それ以外の場合は、false。

### <a name="examples---exists"></a>例 - exists

次の例では、特定の項目が構造体に存在するかどうかを検査し、存在しない場合は、項目を追加し、Struct.add メソッドを使用して項目に値を割り当てます。

```xpp
client server static void setProp( 
    Struct     properties, 
    str        name, 
    anytype   value 
    ) 
{ 
    if (! properties.exists(name)) 
    { 
        properties.add(name,nullValue(value)); 
    } 
    properties.value(name,value); 
}
```

## <a name="method-fieldname"></a>メソッド fieldName

指定された位置にある構造体内の項目の名前を返します。

```xpp
public str fieldName(int index)
```

### <a name="parameters---fieldname"></a>パラメーター - fieldName

指数  
項目名を取得する構造体内の位置。

### <a name="return-value---fieldname"></a>戻り値 - fieldName

インデックスで指定された位置にある項目の名前。

### <a name="remarks---fieldname"></a>備考 - fieldName

インデックスが見つからない場合は、空の文字列が返されます。

### <a name="examples---fieldname"></a>例 - fieldName

次の例では、コンテナーから構造体を作成し、Struct.fields メソッドを使用してコンテナーの内容を反復処理します。 fieldName メソッドは、構造体の各項目の名前をテストするために使用され、この名前の値に応じて特定のアクションが実行されます。

```xpp
boolean unpack(container packed) 
{ 
    Struct      unpackedProperties; 
    container   structCon; 
    Counter     i; 
    [#currentList,structCon] = packed; 
    unpackedProperties = Struct::create(structCon); 
    for (i=1;i<=unpackedProperties.fields();i++) 
    { 
        switch (unpackedProperties.fieldName(i)) 
        { 
            case #closedOk: 
                break; 
            case #PropertyCaption: 
                if (! dialogForm  
                    || dialogForm  
                    && ! dialogForm.form().design().caption()) 
                    this.caption(unpackedProperties.valueIndex(i)); 
                break; 
            case #dialogFormname: 
                // Do nothing 
                break; 
            case #PropertyAlwaysOnTop: 
                this.alwaysOnTop(unpackedProperties.valueIndex(i)); 
                break; 
            case #PropertyWindowType: 
                this.windowType(unpackedProperties.valueIndex(i)); 
                break; 
            case #defaultButton: 
                this.defaultButton(unpackedProperties.valueIndex(i)); 
                break; 
            default: 
                throw error(strfmt( 
                    "@SYS67326",unpackedProperties.fieldName(i), 
                     classId2Name(classidget(this)))); 
        } 
    } 
    return true; 
}
```

## <a name="method-fields"></a>メソッド fields

構造体内の項目の数を返します。

```xpp
public int fields()
```

### <a name="return-value---fields"></a>戻り値 - fields

構造体内の項目の数。

### <a name="remarks---fields"></a>備考 - fields

構造体内の項目の位置を見つけるには、Struct.index メソッドを使用します。

### <a name="examples---fields"></a>例 - fields

次の例では、コンテナーから構造体を作成し、フィールド メソッドを使用してコンテナーの内容を反復処理します。

```xpp
boolean unpack(container packed) 
{ 
    Struct      unpackedProperties; 
    container   structCon; 
    Counter     i; 
    [#currentList,structCon] = packed; 
    unpackedProperties = Struct::create(structCon); 
    for (i=1;i<=unpackedProperties.fields();i++) 
    { 
        switch (unpackedProperties.fieldName(i)) 
        { 
            case #closedOk: 
                break; 
            case #PropertyCaption: 
                if (! dialogForm  
                    || dialogForm  
                    && ! dialogForm.form().design().caption()) 
                    this.caption(unpackedProperties.valueIndex(i)); 
                break; 
            case #dialogFormname: 
                // Do nothing 
                break; 
            case #PropertyAlwaysOnTop: 
                this.alwaysOnTop(unpackedProperties.valueIndex(i)); 
                break; 
            case #PropertyWindowType: 
                this.windowType(unpackedProperties.valueIndex(i)); 
                break; 
            case #defaultButton: 
                this.defaultButton(unpackedProperties.valueIndex(i)); 
                break; 
            default: 
                throw error(strfmt( 
                    "@SYS67326",unpackedProperties.fieldName(i), 
                     classId2Name(classidget(this)))); 
        } 
    } 
    return true; 
}
```

## <a name="method-fieldtype"></a>メソッド fieldType

指定された位置にある構造体内の項目のデータ型を返します。

```xpp
public Types fieldType(int index)
```

### <a name="parameters---fieldtype"></a>パラメーター - fieldType

指数  
データ型を取得する構造体内の位置。

### <a name="return-value---fieldtype"></a>戻り値 - fieldType

インデックスで指定された位置にある項目のデータ型。

### <a name="remarks---fieldtype"></a>備考 - fieldType

可能な値は、システム列挙で提供されます。 インデックスが見つからない場合は、返す値は Types::void です。 Struct.index メソッドを使用することにより、構造体内の特定の品目の位置を決定することができます。

## <a name="method-index"></a>メソッド index

名前に基づいて構造体の項目の位置を計算します。

```xpp
public int index(str fieldName)
```

### <a name="parameters---index"></a>パラメーター - index

fieldName  
位置を返す項目の名前。

### <a name="return-value---index"></a>戻り値 - index

項目の位置。

### <a name="remarks---index"></a>備考 - index

構造体内の項目は、項目名に従ってアルファベット順に並べられます。 fieldName という名前の項目がない場合は、0 が返されます。

## <a name="method-pack"></a>メソッド pack

Struct クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

Struct クラスの現在のインスタンスを含むコンテナーです。

### <a name="remarks---pack"></a>備考 - pack

pack メソッドは、オブジェクトを保持する各フィールドで呼び出され、(サブ) コンテナーを生成します。 構造体は、Struct.create メソッドを使用してコンテナーから再作成できます。

### <a name="examples---pack"></a>例 - pack

次の例では、2 つの項目 (名前と年齢) を持つ構造体を作成し、項目に値を追加します。 構造体はコンテナーに梱包され、このコンテナーが使用されて新しい構造体が作成されます。

```xpp
{  
    container packedStruct;  
    Struct s1, s = new Struct ("str name; int age"); 
    s.value ("name", "Jane Dow");  
    s.value ("age", 34); 
    // Struct is packed into a container 
    packedStruct = s.pack();  
    // A new struct is created from the container 
    s1 = Struct::create(packedStruct); 
    // Both structs have the same contents 
    print s.toString();  
    print s1.toString();  
    pause;  
}
```

## <a name="method-remove"></a>メソッド remove

構造体から品目を削除します。

```xpp
public boolean remove(str fieldName)
```

### <a name="parameters---remove"></a>パラメーター - remove

fieldName  
削除する項目の名前。

### <a name="return-value---remove"></a>戻り値 - remove

項目が見つかった (そして削除された) 場合は true。それ以外の場合は、false。

### <a name="remarks---remove"></a>備考 - remove

fieldName パラメーターに指定する名前は、構造体のインスタンス化で指定されたアイテムの名前または Struct.add メソッドを使用して追加されたアイテムの名前でなければなりません。 名前は引用符 (" ") で囲む必要があります。

### <a name="examples---remove"></a>例 - remove

次の例では、2 つの項目を含む構造体を作成し、これらの項目の説明を出力します。 品目のいずれかは、メソッドの削除を使用して削除されます。

```xpp
{ 
    Struct s = new Struct ("str name; int age"); 
    // Values are assigned to the two items 
    s.value("name", "John"); 
    s.value("age", 34); 
    // Prints a description of the items in the struct 
    print s.definitionString(); 
    pause; 
    // Removes the name field 
    s.remove("name"); 
    // Describes remaining items in the struct 
    print s.definitionString(); 
    pause; 
}
```

## <a name="method-tostring"></a>メソッド toString

構造体の内容を説明する文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

構造体の内容を説明する文字列。

## <a name="method-value"></a>メソッド value

構造体で指定される品目の値を取得または設定します。

```xpp
public AnyType value(str fieldName, [AnyType value])
```

### <a name="parameters---value"></a>パラメーター - value

fieldName  
項目に割り当てる値 (オプション)。

<!-- -->

値  
項目に割り当てる値 (オプション)。

### <a name="return-value---value"></a>戻り値 - value

指定項目の値。

### <a name="remarks---value"></a>備考 - value

構造体内で指定された名前に項目がない場合は例外が発生します。 構造体内の項目名は、Struct.fieldName メソッドを使用して取得できます。 Struct.add メソッドを使用することにより、新しい品目を構造体に追加すると同時に値を割り当てることができます。 構造体内の位置に基づいてアイテムに新しい値を割り当てるには、Struct.valueIndex メソッドを使用します。

### <a name="examples---value"></a>例 - value

次の例では、2 つの項目を含む構造体を作成し、value メソッドを使用してこれらの 2 つの項目に値を割り当てます。

```xpp
{ 
    Struct s = new Struct ("str name; int age"); 
    // Set the values 
    s.value("name", "Jane Dow"); 
    s.value("age", 34); 
    // Print the values 
    print s.value("name"); 
    print s.value("age"); 
    pause; 
}
```

## <a name="method-valueimage"></a>メソッド valueImage

構造体内の特定の位置にある品目の値を説明する文字列を返します。

```xpp
public str valueImage(int index)
```

### <a name="parameters---valueimage"></a>パラメーター - valueImage

指数  
説明を返す項目の位置。

### <a name="return-value---valueimage"></a>戻り値 - valueImage

品目の価値を説明する文字列。

### <a name="remarks---valueimage"></a>備考 - valueImage

構造体内の項目は、項目の名前に従ってアルファベット順に表示されます。 インデックスで指定された位置に項目がない場合は例外が発生します。

## <a name="method-valueindex"></a>メソッド valueIndex

構造体で指定される位置での品目の値を取得または設定します。

```xpp
public AnyType valueIndex(int index, [AnyType value])
```

### <a name="parameters---valueindex"></a>パラメーター - valueIndex

指数  
インデックスで指定された位置のアイテムに割り当てる値 (オプション)。

<!-- -->

値  
インデックスで指定された位置のアイテムに割り当てる値 (オプション)。

### <a name="return-value---valueindex"></a>戻り値 - valueIndex

インデックスで指定された位置にある項目の値。

### <a name="remarks---valueindex"></a>備考 - valueIndex

インデックスで指定された位置に項目がない場合は例外が発生します。 構造体内の項目の位置は、Struct.index メソッドを使用して取得できます。

## <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a>パラメーター - xml

インデント  
返された XML 文字列のインデントの量 (省略可能)。

### <a name="return-value---xml"></a>戻り値 - xml

現在のオブジェクトを表す XML 文字列です。

### <a name="remarks---xml"></a>備考 - xml

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

## <a name="method-create"></a>メソッド create

以前の Struct.pack の呼び出しで取得されたコンテナーから構造体を作成します。

```xpp
public static Struct create(container container)
```

### <a name="parameters---create"></a>パラメーター - create

コンテナー  
梱包済みの構造体を含むコンテナーです。

### <a name="return-value---create"></a>戻り値 - create

特定のコンテナーに梱包されたものと同じ構造体。

### <a name="remarks---create"></a>備考 - create

構造体にオブジェクトが含まれている場合、これらのオブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。

### <a name="examples---create"></a>例 - create

次の例では、2 つの項目 (名前と年齢) を持つ構造体を作成し、項目に値を追加します。 構造体はコンテナーに梱包され、このコンテナーは開梱されて新しい構造体が作成されます。

```xpp
{  
    container packedStruct;  
    Struct s1, s = new Struct ("str name; int age"); 
    s.value ("name", "Jane Dow");  
    s.value ("age", 34); 
    // Struct is packed into a container 
    packedStruct = s.pack();  
    // A new struct is created from the container 
    s1 = Struct::create(packedStruct); 
    // Both structs have the same contents 
    print s.toString();  
    print s1.toString();  
    pause;  
}
```

## <a name="method-createfromxml"></a>メソッド createFromXML

```xpp
public static Struct createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a>パラメータ - createFromXML

xmlnode  

### <a name="return-value---createfromxml"></a>戻り値 - createFromXML

## <a name="method-equal"></a>メソッド equal

2 つの構造体が等しいかどうかを判断します。

```xpp
public static boolean equal(Struct struct1, Struct struct2)
```

### <a name="parameters---equal"></a>パラメーター - equal

struct1  
比較される 2 つの構造体のうちの 2 番目の構造体。

<!-- -->

struct2  
比較される 2 つの構造体のうちの 2 番目の構造体。

### <a name="return-value---equal"></a>戻り値 - equal

構造体が等しい場合は true。それ以外の場合は、false。

### <a name="remarks---equal"></a>備考 - equal

同じ数のフィールドを持ち、フィールド名が同じで、各フィールドが同じ型で同じ値を持つ場合、2 つの構造体は同等です。

## <a name="method-merge"></a>メソッド merge

2 つの構造体を組み合わせ、新しい構造体を作成します。

```xpp
public static Struct merge(Struct struct1, Struct struct2)
```

### <a name="parameters---merge"></a>パラメーター - merge

struct1  
新しい構造体を作成するために最初の構造体の最後に追加される構造体。

<!-- -->

struct2  
新しい構造体を作成するために最初の構造体の最後に追加される構造体。

### <a name="return-value---merge"></a>戻り値 - merge

新しい構造体。

### <a name="remarks---merge"></a>備考 - merge

struct2 は struct1 の最後に追加されます。 つまり、新しい構造体の項目の順序は、項目名のアルファベット順に並べられた struct1 のすべての項目と、項目名のアルファベット順に並べられた struct2 のすべての項目です。 両方の構造体に同じ名前を持つ品目が含まれている場合は、最初の構造体からの品目のみが含まれるようになります。

### <a name="examples---merge"></a>例 - merge

次の例では、person と address という 2 つの構造体を作成し、それらを allInfo という新しい構造体にマージします。

```xpp
{ 
    container packedStruct; 
    Struct person = new Struct ("str name; int age"); 
    Struct address = new Struct ("str street; str city; str country"); 
    Struct allInfo; 
    person.value ("name", "Jane Dow"); 
    person.value ("age", 34); 
    address.value ("street", "Downing street 10"); 
    address.value ("country", "Great Britain"); 
    address.value ("city", " London"); 
    allInfo = Struct::merge(person, address); 
    print allInfo.toString(); 
    pause; 
}
```

## <a name="method-new"></a>メソッド new

構造体を作成します。

```xpp
public void new(VarArg specifier)
```

### <a name="parameters---new"></a>パラメーター - new

指定子  
文字列として品目の名前の後には、品目のデータ型を指定した 1 つ以上の組み合わせ。

### <a name="remarks---new"></a>備考 - new

項目のデータ型は、プリミティブ データ型の名前を使用するか、システム列挙を使用して指定できます。 構造体内の項目は、文字列型、整数型、実数型、日付型、コンテナー型、レコード型、クラス型など、型システムの列挙型にあるデータ型のいずれでもかまいません。 以下の例に説明されているように、Struct.definitionString メソッドを使用して新しい構造体を作成し、構造体のコピーを作成することができます。 構造体を作成した後は、Struct.add メソッドを使用して新しい項目を追加し、Struct.value または Struct.valueIndex メソッドを使用して構造体に項目の値を設定することができます。

### <a name="examples---new"></a>例 - new

次の例では、同じ定義を持つ 2 つの構造体を作成し、2 つの値と追加の項目および値をその 1 つ (s1) に追加します。 この構造体をコピーして、Struct.definitionString メソッドを使用することにより新しい構造体を作成します。

```xpp
{ 
    Struct s1, s2, s3; 
    // The two constructors below create the same struct 
    s1 = new Struct(Types::Integer, "age", Types::String, "name"); 
    s2 = new Struct ("int age; str name"); 
    // Print the definitions 
    print s1.definitionString(); 
    print s2.definitionString(); 
    s1.value("age", 25); 
    s1.value("name", "Jane Dow"); 
    // Add a field at runtime 
    s1.add("Shoesize", 45); 
    print s1.definitionString(); 
    print s1.toString(); 
    // Create a container with age, name and shoesize, 
    // using definitionString 
    s3 = new struct(s1.definitionString()); 
    print s3.definitionString(); 
    pause; 
}
```

