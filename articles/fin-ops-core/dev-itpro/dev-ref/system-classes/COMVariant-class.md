---
title: COMVariant クラス
description: このトピックでは、COMVariant クラスについて説明します。
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
ms.openlocfilehash: 261fae114d6b6cf1159cb1687d7722f6d52a4173
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502716"
---
# <a name="class-comvariant"></a>クラス COMVariant

[!include [banner](../../includes/banner.md)]

```xpp
class COMVariant extends Object
```

COMVariant クラスは、さまざまな種類のデータを格納できる一般的なクラスとして使用されます。 このクラスは、COM (コンポーネント オブジェクト モデル) 自動オブジェクトのメソッドまたはプロパティに引数を渡すために使用され、COM および COMDispFunction クラスとともに使用されます。

## <a name="remarks"></a>備考

COMVariant オブジェクトのデータ型は次によって設定できます。

-   新しいメソッド
-   variantType メソッド
-   CreateFrom� メソッド。 たとえば、createFromBoolean メソッドは、VT\_BOOL (= ブール値) のタイプの COMVariant オブジェクトを作成します。
-   プロパティ メソッド。 たとえば、boolean プロパティを使用して新しい値を設定すると、オブジェクトは VT\_BOOL (= Boolean) のタイプではなく、このタイプに変更されます。

データ型の値は、いずれかのプロパティ メソッドによって設定されます。 たとえば、タイプ VT\_BOOL の COMVariant オブジェクトの値は、boolean メソッドにより設定されます。 その値を設定する可能なデータ型とメソッドは、「備考」セクションに表示されます。 COMVariant クラスがサポートするデータ型は、X++ データ型ではなく、COMオートメーション標準によって定義されたデータ型です。 COMVariant クラスは、Win32 SDK にある VARIANT 構造に基づいています。 詳細については、Win32 SDK ドキュメントを参照してください。 COMVariant クラスのプロパティ メソッドは、次のように COMVariantType 値にマップされます。

|             |               |                                                                                           |
|-------------|---------------|-------------------------------------------------------------------------------------------|
| ブール値     | VT\_BOOL      |                                                                                           |
| bStr        | VT\_BSTR      | 文字列データ型                                                                          |
| byte        | VT\_UI1       |                                                                                           |
| char        | VT\_I1        |                                                                                           |
| 通貨    | VT\_CY        |                                                                                           |
| 日付、時刻  | VT\_DATE      | 日付/時刻データ型。両方のプロパティを設定する必要があります。                                         |
| decimal     | VT\_DECIMAL   |                                                                                           |
| double      | VT\_R8        |                                                                                           |
| float       | VT\_R4        |                                                                                           |
| iDispatch   | VT\_DISPATCH  |                                                                                           |
| int, long   | VT\_I4        | VT\_I4 は、int データ型と Long データ型の両方で使用されます                                   |
| iUnknown    | VT\_UNKNOWN   |                                                                                           |
| sCode       | VT\_ERROR     | scode データ型は、Win32 HRESULT データ型と同等の COM データ型です。 |
| short       | VT\_I2        |                                                                                           |
| uInt、uLong | VT\_UI4       | VT\_UI4 は、uInt データ型と uLong データ型の両方で使用されます                                |
| uShort      | VT\_UI2       |                                                                                           |
| バリアント     | VT\_VARIANT   |                                                                                           |
| safeArray   | VT\_SAFEARRAY | 配列データ タイプ                                                                           |

## <a name="examples"></a>例

次の例では、COMVariant パラメーターとして渡された 2 つの浮動小数点数を乗算する multiply というメソッドを公開する COM オブジェクトをインスタンス化します。

```xpp
{ 
    COM com; 
    COMVariant varArg1 = new COMVariant(); 
    COMVariant varArg2 = new COMVariant(); 
    COMVariant varRet; 
    real ret; 
    InteropPermission perm; 
```

```xpp
    // Set code access permission to help protect the use  
    // of the COM object. 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    // Permission scope starts here 
    perm.assert(); 
```

```xpp
        com = new COM("MyCOM.Object"); 
```

```xpp
    // Specify arguments for the 'multiply' method 
    varArg1.float(123); 
    varArg2.float(456); 
    varRet = com.multiply(varArg1, varArg2); 
```

```xpp
    ret = varRet.double(); 
    // 'ret' is now 56088 (123*456) 
```

```xpp
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                    | 説明                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean boolean(\[boolean newValue\])                                                              | VT\_BOOL データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                    |
| public str bStr(\[str newValue\])                                                                         | VT\_BSTR データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                    |
| public int byte(\[int newValue\])                                                                         | VT\_UI1 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                     |
| public int char(\[int newValue\])                                                                         | VT\_I1 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public container container(\[container newValue\], \[COMVariantType newType\])                            | コンテナ データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                   |
| public Real currency(\[Real newValue\])                                                                   | VT\_CY データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public Date date(\[Date newValue\])                                                                       | VT\_DATE データ タイプの COMVariant オブジェクトの値の日付部分を取得または設定します。                                                                                   |
| public Real decimal(\[Real newValue\])                                                                    | VT\_DECIMAL データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                 |
| public Real double(\[Real newValue\])                                                                     | VT\_R8 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public Real float(\[Real newValue\])                                                                      | VT\_R4 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public ComInterface iDispatch(\[ComInterface newValue\])                                                  | VT\_DISPATCH データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                |
| public int int(\[int newValue\])                                                                          | VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public ComInterface iUnknown(\[ComInterface newValue\])                                                   | VT\_UNKNOWN (IUnknown) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                      |
| public int long(\[int newValue\])                                                                         | VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public Int64 longLong(\[Int64 newValue\])                                                                 | VT\_I8 (longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                           |
| public Array safeArray(\[Array newValue\], \[COMVariantType newType\])                                    | VT\_SAFEARRAY データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                               |
| public int sCode(\[int newValue\])                                                                        | VT\_ERROR データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                   |
| public int short(\[int newValue\])                                                                        | VT\_I2 (短い) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                              |
| public int time(\[int newValue\])                                                                         | VT\_DATE データ タイプの COMVariant オブジェクトの値の時刻部分を取得または設定します。                                                                                   |
| public str toString()                                                                                     | COMVariant オブジェクトの文字列形式を作成します。 この文字列形式には、オブジェクトの値と型が含まれます。                                               |
| public int uInt(\[int newValue\])                                                                         | VT\_UI4 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                     |
| public int uLong(\[int newValue\])                                                                        | VT\_UI4 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                     |
| public Int64 uLongLong(\[Int64 newValue\])                                                                | VT\_UI8 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                 |
| public int uShort(\[int newValue\])                                                                       | VT\_UI2 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                     |
| public COMVariant variant(\[COMVariant newValue\])                                                        | VT\_VARIANT (バリアント) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                       |
| public COMVariantInOut variantInOutFlag(\[COMVariantInOut newValue\])                                     | COMVariant オブジェクトに対する InOutFlag 設定を設定する返します。                                                                                                              |
| public COMVariantType variantType(\[COMVariantType newValue\])                                            | COMVariant オブジェクトにそのバリアント データ型を照会するか、データ型を変更します。                                                                                             |
| ::public static COMVariant createDateFromYMD(int year, int month, int day, \[COMVariantInOut inOutFlag\]) | 新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。                                                                                      |
| ::public static COMVariant createFromArray(Array value, \[COMVariantInOut inOutFlag\])                    | 新しい COMVariant オブジェクトを作成し、1 回の操作で配列で初期化します。                                                                                          |
| ::public static COMVariant createFromBoolean(boolean value, \[COMVariantInOut inOutFlag\])                | 新しい COMVariant オブジェクトを作成し、1 回の操作でブール値で初期化します。                                                                                   |
| ::public static COMVariant createFromCOM(COM value, \[COMVariantInOut inOutFlag\])                        | 新しい COMVariant オブジェクトを作成し、1 回の操作で COM クラスで初期化します。                                                                                       |
| ::public static COMVariant createFromDate(Date value, \[COMVariantInOut inOutFlag\])                      | 新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。                                                                                      |
| ::public static COMVariant createFromDateAndTime(Date date, int time, \[COMVariantInOut inOutFlag\])      | 新しい COMVariant オブジェクトを作成し、1 回の操作で日時で初期化します。                                                                                   |
| ::public static COMVariant createFromInt(int value, \[COMVariantInOut inOutFlag\])                        | 新しい COMVariant オブジェクトを作成し、1 回の操作で整数値で初期化します。                                                                                  |
| ::public static COMVariant createFromInt64(Int64 value, \[COMVariantInOut inOutFlag\])                    | 新しい COMVariant オブジェクトを作成し、1 回の操作でint64 値 (longLong や uLongLong) で初期化します。                                                            |
| ::public static COMVariant createFromReal(Real value, \[COMVariantInOut inOutFlag\])                      | 新しい COMVariant オブジェクトを作成し、1 回の操作で実際の値で初期化します。                                                                                      |
| ::public static COMVariant createFromStr(str value, \[COMVariantInOut inOutFlag\])                        | 新しい COMVariant オブジェクトを作成し、1 回の操作で文字列で初期化します。                                                                                          |
| ::public static COMVariant createFromTime(int value, \[COMVariantInOut inOutFlag\])                       | 新しい COMVariant オブジェクトを作成し、1 回の操作で時刻値で初期化します。                                                                                      |
| ::public static COMVariant createFromUtcDateTime(DateTime value, \[COMVariantInOut inOutFlag\])           |                                                                                                                                                                             |
| ::public static COMVariant createNoValue()                                                                | 値を持たない VT\_エラー バリアント タイプの COMVariant オブジェクトを作成します。                                                                                                    |
| public void new(\[COMVariantInOut inOutFlag\], \[COMVariantType type\])                                   | COM オートメーション オブジェクトのメソッドまたはプロパティに引数を渡すために使用できる COMVariant オブジェクトを作成します。                                                     |
| public void noValue()                                                                                     | 既存の COMVariant オブジェクトの内容を削除し、COMDispFunction.call メソッドまたは COM クラスで使用されている場合は、未指定の引数として機能させることができます。 |
| public void finalize()                                                                                    | 実装されていません。 明示的にオブジェクトを破棄する必要がある場合は、このメソッドをオーバーライドすることができます。                                                                                 |

## <a name="method-boolean"></a>メソッド boolean

VT\_BOOL データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public boolean boolean([boolean newValue])
```

### <a name="parameters---boolean"></a>パラメーター - boolean

newValue  
新しい値 (オプション)。

### <a name="return-value---boolean"></a>戻り値 - boolean

現在の値。

### <a name="remarks---boolean"></a>備考 - boolean

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_BOOL に設定されている場合、その COMVariant オブジェクトはブール型です。 COM ブール値のデータ型は、"VARIANT\_BOOL" とも呼ばれることがあります。

### <a name="examples---boolean"></a>例 - boolean

次の例では、VT\_BOOL 型の新しい COMVariant オブジェクトを作成し、値を true に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_BOOL); 
```

```xpp
    // Set value of the object 
    var.boolean(true); 
}
```

## <a name="method-bstr"></a>メソッド bStr

VT\_BSTR データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public str bStr([str newValue])
```

### <a name="parameters---bstr"></a>パラメーター - bStr

newValue  
新しい値 (オプション)。

### <a name="return-value---bstr"></a>戻り値 - bStr

現在の文字列の価値。

### <a name="remarks---bstr"></a>備考 - bStr

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_BSTR に設定されている場合、その COMVariant オブジェクトは文字列データ型です。 BStr データ型は、文字列の処理に使用される COM データ型です。

### <a name="examples---bstr"></a>例 - bStr

次の例では、VT\_BSTR 型の新しい COMVariant オブジェクトを作成し、値を "Hello World" に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_BSTR); 
```

```xpp
    // Set string value of the object 
    var.bStr("Hello World"); 
}
```

## <a name="method-byte"></a>メソッド byte

VT\_UI1 データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public int byte([int newValue])
```

### <a name="parameters---byte"></a>パラメーター - byte

newValue  
新しい値 (オプション)。

### <a name="return-value---byte"></a>戻り値 - byte

現在の値。

### <a name="remarks---byte"></a>備考 - byte

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_UI1 に設定されている場合、その COMVariant オブジェクトは byte データ型です。 また、「符号なし文字型」を使用して COM バイト データ型を参照することができます。

### <a name="examples---byte"></a>例 - byte

次の例では、VT\_UI1 型の新しい COMVariant オブジェクトを作成し、値を 123 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UI1); 
```

```xpp
    // Set value of the object 
    var.byte(123); 
}
```

## <a name="method-char"></a>メソッド char

VT\_I1 データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public int char([int newValue])
```

### <a name="parameters---char"></a>パラメーター - char

newValue  
新しい値 (オプション)。

### <a name="return-value---char"></a>戻り値 - char

現在の値。

### <a name="remarks---char"></a>備考 - char

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_I1 に設定されている場合、その COMVariant オブジェクトは char データ型です。

### <a name="examples---char"></a>例 - char

次の例では、VT\_I1 型の 新しい COMVariant オブジェクトを作成し、値を 65 の、A の数値に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I1); 
```

```xpp
    // Set value of the object 
    var.char(Char2Num("A", 1)); 
}
```

## <a name="method-container"></a>メソッド container

コンテナ データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public container container([container newValue], [COMVariantType newType])
```

### <a name="parameters---container"></a>パラメーター - container

newValue  
新しいコンテナーのタイプ (オプション)。 既定では、コンテナーが整数を格納します。

<!-- -->

newType  
新しいコンテナーのタイプ (オプション)。 既定では、コンテナーが整数を格納します。

### <a name="return-value---container"></a>戻り値 - container

現在のコンテナー。

### <a name="remarks---container"></a>備考 - container

newType パラメーターの使用可能な値は、COMVariantType システム列挙によって提供される値のサブセットです。

-   VT\_I2
-   VT\_I4
-   VT\_R4
-   VT\_R8
-   VT\_CY
-   VT\_DATE
-   VT\_BSTR
-   VT\_ERROR
-   VT\_BOOL
-   VT\_DECIMAL
-   VT\_I1
-   VT\_UI1
-   VT\_UI2
-   VT\_UI4
-   VT\_I8
-   VT\_UI8
-   VT\_INT
-   VT\_UINT

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 コンテナーが COMVariant オブジェクトに保存されると、コンテナーのバイナリ表現がバイナリ配列に保存されます (COMVariant.safeArray メソッドを参照してください)。 コンテナーのプロパティは、データベース COM オブジェクトにデータを格納し、後でデータを処理する COM オブジェクトを使用せずに Finance and Operations アプリケーションにデータを読み戻す必要がある場合に便利です。 コンテナーのプロパティは、COMVariant クラスの高度なプロパティです。 COMVariant オブジェクト内で、コンテナーが格納されるバイナリ配列の内容は、どの COM オブジェクトによっても変更されないようにしなければならないため、注意して使用する必要があります。

### <a name="examples---container"></a>例 - container

次の例では、コンテナー 型の新しい COMVariant オブジェクトを作成します。 コンテナー内のデータは、データベース COM オブジェクトに渡され、データベース COM オブジェクトによって使用されます。 注記: 次のセクションのコードには仮想 COM オブジェクト (MyDatabaseCOM.Object) が含まれており、Finance and Operations アプリケーションの外部でオブジェクトが作成されていない限り実行されません。

```xpp
{ 
    COM com; 
    COMVariant var = new COMVariant(); 
    container con; 
    InteropPermission perm; 
```

```xpp
    // Set code access permission to help protect use of COM object 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    // Permission scope starts here 
    perm.assert(); 
```

```xpp
    // Put some data in the container 
    con = conins(con, 1, "Element 1"); 
    con = conins(con, 2, "Element 2"); 
    // Set value of the object and ensure the data 
    // is stored in a binary array of bytes 
    var.container(con, COMVariantType::VT_UI1); 
```

```xpp
    // Create a database object to store the data in 
    com = new COM("MyDatabaseCOM.Object"); 
    com.writeData(var); 
    // ... 
```

```xpp
    // Close code access permission 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-currency"></a>メソッド currency

VT\_CY データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public Real currency([Real newValue])
```

### <a name="parameters---currency"></a>パラメーター - currency

newValue  
新しい値 (オプション)。

### <a name="return-value---currency"></a>戻り値 - currency

現在の値。

### <a name="remarks---currency"></a>備考 - currency

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_CY に設定されている場合、その COMVariant オブジェクトは通貨データ型です。 通貨データ型は、通貨値に最適化された COM データ型です。 小数点以下 4 桁のある実数です。 場合によっては、COM 通貨データ型を参照するために "CY" も使用されます。

### <a name="examples---currency"></a>例 - currency

次の例では、VT\_CY 型の新しい COMVariant オブジェクトを作成し、値を 123.4567 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_CY); 
```

```xpp
    // Set value of the object 
    var.currency(123.4567); 
}
```

## <a name="method-date"></a>メソッド date

VT\_DATE データ タイプの COMVariant オブジェクトの値の日付部分を取得または設定します。

```xpp
public Date date([Date newValue])
```

### <a name="parameters---date"></a>パラメーター - date

newValue  
新しい値 (オプション)。

### <a name="return-value---date"></a>戻り値 - date

現在の値。

### <a name="remarks---date"></a>備考 - date

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_DATE に設定されている場合、その COMVariant オブジェクトは日時データ型です。 オブジェクトの値を設定するとき、日付に加えて、値の時刻の部分を設定する必要があります。 値の時間部分を設定するには、time プロパティを使用します。

### <a name="examples---date"></a>例 - date

次の例では、VT\_DATE 型の COMVariant オブジェクトを作成し、値の日付部分を 1998 年 12 月 24 日に設定し、時刻の部分を 13.24 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_DATE); 
```

```xpp
    // Set value of the object 
    var.date(Str2Date("12.24.1998", 213)); 
    var.time(Str2Time("13:24:00")); 
}
```

## <a name="method-decimal"></a>メソッド decimal

VT\_DECIMAL データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public Real decimal([Real newValue])
```

### <a name="parameters---decimal"></a>パラメーター - decimal

newValue  
新しい値 (オプション)。

### <a name="return-value---decimal"></a>戻り値 - decimal

現在の値。

### <a name="remarks---decimal"></a>備考 - decimal

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_DECIMAL に設定されている場合、その COMVariant オブジェクトは 10 進型です。 10進データ型は、数値のサイズとスケールを提供する COM データ型です。 X++ には 10 進データ型と並行するものはありません。

### <a name="examples---decimal"></a>例 - decimal

次の例では、VT\_DECIMAL 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_DECIMAL); 
```

```xpp
    // Set value of the object 
    var.decimal(123.456); 
}
```

## <a name="method-double"></a>メソッド double

VT\_R8 データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public Real double([Real newValue])
```

### <a name="parameters---double"></a>パラメーター - double

newValue  
新しい値 (オプション)。

### <a name="return-value---double"></a>戻り値 - double

現在の値。

### <a name="remarks---double"></a>備考 - double

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_R8 に設定されている場合、その COMVariant オブジェクトは double データ型です。

### <a name="examples---double"></a>例 - double

次の例では、VT\_R8 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_R8); 
```

```xpp
    // Set value of the object 
    var.double(123.456); 
}
```

## <a name="method-float"></a>メソッド float

VT\_R4 データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public Real float([Real newValue])
```

### <a name="parameters---float"></a>パラメーター - float

newValue  
新しい値 (オプション)。

### <a name="return-value---float"></a>戻り値 - float

現在の値。

### <a name="remarks---float"></a>備考 - float

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_R4 に設定されている場合、COMVariant オブジェクトは float 型です。 場合によっては、COM 浮動小数点データ型を参照するために "single" も使用されます。

### <a name="examples---float"></a>例 - float

次の例では、VT\_R4 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_R4); 
```

```xpp
    // Set value of the object 
    var.float(123.456); 
}
```

## <a name="method-idispatch"></a>メソッド iDispatch

VT\_DISPATCH データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public ComInterface iDispatch([ComInterface newValue])
```

### <a name="parameters---idispatch"></a>パラメーター - iDispatch

newValue  
新しい値 (オプション)。

### <a name="return-value---idispatch"></a>戻り値 - iDispatch

現在の値。

### <a name="remarks---idispatch"></a>備考 - iDispatch

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_DISPATCH に設定されている場合、その COMVariant オブジェクトは IDispatch データ型です。 IDispatch データ型は、COM IDispatch インターフェイスへのハンドルを提供する COM データ型です。

### <a name="examples---idispatch"></a>例 - iDispatch

次の例では、VT\_DISPATCH 型の新しい COMVariant オブジェクトを作成します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_DISPATCH); 
    COMInterface comInterface; 
```

```xpp
    // Here, the comInterface variable must be assigned 
    // a COM IDispatch interface 
    //� 
```

```xpp
    // Set value of the object 
    var.iDispatch(comInterface); 
}
```

## <a name="method-int"></a>メソッド int

VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public int int([int newValue])
```

### <a name="parameters---int"></a>パラメーター - int

newValue  
新しい値 (オプション)。

### <a name="return-value---int"></a>戻り値 - int

現在の値。

### <a name="remarks---int"></a>備考 - int

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 COMVariantType::VT\_I4 データ型は long バリアント型にも使用されます。 COMVariant.long メソッドは、このメソッドと同じです。2 つのメソッドは、完全性のために存在します。

### <a name="examples---int"></a>例 - int

次の例では、VT\_I4 型の COMVariant オブジェクトを作成し、値を 123456 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I4); 
```

```xpp
    // Set value of the object 
    var.int(123456); 
}
```

## <a name="method-iunknown"></a>メソッド iUnknown

VT\_UNKNOWN (IUnknown) データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public ComInterface iUnknown([ComInterface newValue])
```

### <a name="parameters---iunknown"></a>パラメーター - iUnknown

newValue  
新しい値 (オプション)。

### <a name="return-value---iunknown"></a>戻り値 - iUnknown

現在の値。

### <a name="remarks---iunknown"></a>備考 - iUnknown

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、データ型の値に合わせて変更されます。 データ型が COMVariantType::VT\_UNKNOWN に設定されている場合、COMVariant オブジェクトは IUnknown データ型です。 IUnknown データ型は、COM IUnknown インターフェイスへのハンドルを提供する COM データ型です。

### <a name="examples---iunknown"></a>例 - iUnknown

次の例では、VT\_UNKNOWN 型の新しい COMVariant オブジェクトを作成します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UNKNOWN); 
    COMInterface comInterface; 
```

```xpp
    // comInterface variable is assigned 
    // a COM IUnknown interface 
    // ... 
```

```xpp
    // Set value of the object 
    var.iUnknown(comInterface); 
}
```

## <a name="method-long"></a>メソッド long

VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public int long([int newValue])
```

### <a name="parameters---long"></a>パラメーター - long

newValue  
新しい値 (オプション)。

### <a name="return-value---long"></a>戻り値 - long

現在の値。

### <a name="remarks---long"></a>備考 - long

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 COMVariantType::VT\_I4 データ型は int バリアント型にも使用されます。 COMVariant.int メソッドは、このメソッドと同じです。2 つのメソッドは、完全性のために存在します。

### <a name="examples---long"></a>例 - long

次の例では、VT\_I4 型の COMVariant オブジェクトを作成し、値を 123456 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I4); 
```

```xpp
    // Set value of the object 
    var.long(123456); 
}
```

## <a name="method-longlong"></a>メソッド longLong

VT\_I8 (longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public Int64 longLong([Int64 newValue])
```

### <a name="parameters---longlong"></a>パラメーター - longLong

newValue  
新しい値 (オプション)。

### <a name="return-value---longlong"></a>戻り値 - longLong

現在の値。

### <a name="remarks---longlong"></a>備考 - longLong

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_I8 に設定されている場合、その COMVariant オブジェクトは longlong バリアント型です。

### <a name="examples---longlong"></a>例 - longLong

次の例では、VT\_I8 型の新しい COMVariant オブジェクトを作成し、値を 2,305,843,009,213,693,952 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_BOOL); 
```

```xpp
    // Set value of the object 
    var.longLong(2305843009213693952); 
}
```

## <a name="method-safearray"></a>メソッド safeArray

VT\_SAFEARRAY データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public Array safeArray([Array newValue], [COMVariantType newType])
```

### <a name="parameters---safearray"></a>パラメーター - safeArray

newValue  
新しい配列のタイプ (オプション)。

<!-- -->

newType  
新しい配列のタイプ (オプション)。

### <a name="return-value---safearray"></a>戻り値 - safeArray

現在の配列。

### <a name="remarks---safearray"></a>備考 - safeArray

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_SAFEARRAY に設定されている場合、その COMVariant オブジェクトは配列ブール型です。 セーフ配列は、COM の配列に相当します。 現在、1 次元セーフ配列のみがサポートされています。

### <a name="examples---safearray"></a>例 - safeArray

次の例では、VT\_SAFEARRAY 型の新しい COMVariant オブジェクトを作成し、short 配列で初期化します。

```xpp
{ 
    int i, result; 
    COM com; 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_SAFEARRAY); 
    Array arr = new Array(Types::INTEGER); 
```

```xpp
    // Insert 10 values in the array 
    for (i = 1; i <= 10; i++) 
    { 
        arr.value(i, i); 
    } 
```

```xpp
    // Set value of the object and ensure the integer values 
    // are treated as short data types 
    var.safeArray(arr, COMVariantType::VT_I2); 
}
```

## <a name="method-scode"></a>メソッド sCode

VT\_ERROR データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public int sCode([int newValue])
```

### <a name="parameters---scode"></a>パラメーター - sCode

newValue  
新しい値 (オプション)。

### <a name="return-value---scode"></a>戻り値 - sCode

現在の値。

### <a name="remarks---scode"></a>備考 - sCode

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_ERROR に設定されている場合、その COMVariant オブジェクトは scode データ型です。 scode データ型は、COM 関数の戻り値として最もよく使用される Win32 HRESULT データ型と同等の COM データ型です。

### <a name="examples---scode"></a>例 - sCode

次の例では、VT\_ERROR 型の新しい COMVariant オブジェクトを作成し、値を 0x80001004 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_ERROR); 
```

```xpp
    // Set value of the object 
    var.sCode(0x80001004); 
}
```

## <a name="method-short"></a>メソッド short

VT\_I2 (短い) データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public int short([int newValue])
```

### <a name="parameters---short"></a>パラメーター - short

newValue  
新しい値 (オプション)。

### <a name="return-value---short"></a>戻り値 - short

現在の値。

### <a name="remarks---short"></a>備考 - short

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_I2 に設定されている場合、その COMVariant オブジェクトは short データ型です。

### <a name="examples---short"></a>例 - short

次の例では、VT\_I2 型の新しい COMVariant オブジェクトを作成し、値を 123 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I2); 
```

```xpp
    // Set value of the object 
    var.short(123); 
}
```

## <a name="method-time"></a>メソッド time

VT\_DATE データ タイプの COMVariant オブジェクトの値の時刻部分を取得または設定します。

```xpp
public int time([int newValue])
```

### <a name="parameters---time"></a>パラメーター - time

newValue  
新しい値 (オプション)。

### <a name="return-value---time"></a>戻り値 - time

現在の値。

### <a name="remarks---time"></a>備考 - time

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_DATE に設定されている場合、その COMVariant オブジェクトは日時データ型です。 オブジェクトの値を設定するとき、時刻に加えて、値の日付の部分を設定する必要があります。 値の日付部分を設定するには、date プロパティを使用します。

### <a name="examples---time"></a>例 - time

次の例では、VT\_DATE 型の COMVariant オブジェクトを作成し、値の日付部分を 1998 年 12 月 24 日に設定し、時刻の部分を 13.24 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_DATE); 
```

```xpp
    // Set value of the object 
    var.date(Str2Date("12.24.1998", 213)); 
    var.time(Str2Time("13:24:00")); 
}
```

## <a name="method-tostring"></a>メソッド toString

COMVariant オブジェクトの文字列形式を作成します。 この文字列形式には、オブジェクトの値と型が含まれます。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

COMVariant オブジェクトの文字列表現。

### <a name="remarks---tostring"></a>備考 - toString

このメソッドから返される実際の文字列は、COMVariant オブジェクトのバリアント データ型によって異なります。

### <a name="examples---tostring"></a>例 - toString

次の例では、COMVariant オブジェクトを作成し、現在の日付を割り当てます。 情報ログにオブジェクトの説明を出力します。

```xpp
COMVariant theDay; 
```

```xpp
theDay = COMVariant::createFromDate(today()); 
info(theDay.toString());
```

## <a name="method-uint"></a>メソッド uInt

VT\_UI4 データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public int uInt([int newValue])
```

### <a name="parameters---uint"></a>パラメーター - ulnt

newValue  
新しい値 (オプション)。

### <a name="return-value---uint"></a>戻り値 - ulnt

現在の値。

### <a name="remarks---uint"></a>備考 - ulnt

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 COMVariantType::VT\_UI4 データ型は uLong データ型にも使用されます。

### <a name="examples---uint"></a>例 - ulnt

次の例では、VT\_UI4 型の新しい COMVariant オブジェクトを作成し、値を 123456 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UI4); 
```

```xpp
    // Set value of the object 
    var.uInt(123456); 
}
```

## <a name="method-ulong"></a>メソッド uLong

VT\_UI4 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public int uLong([int newValue])
```

### <a name="parameters---ulong"></a>パラメーター - uLong

newValue  
新しい値 (オプション)。

### <a name="return-value---ulong"></a>戻り値 - uLong

現在の値。

### <a name="remarks---ulong"></a>備考 - uLong

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 COMVariantType::VT\_UI4 データ型は uInt データ型にも使用されます。

### <a name="examples---ulong"></a>例 - uLong

次の例では、VT\_UI4 型の新しい COMVariant オブジェクトを作成し、値を 123456 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UI4); 
```

```xpp
    // set value of the object 
    var.uLong(123456); 
}
```

## <a name="method-ulonglong"></a>メソッド uLongLong

VT\_UI8 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public Int64 uLongLong([Int64 newValue])
```

### <a name="parameters---ulonglong"></a>パラメーター - uLongLong

newValue  
新しい値 (オプション)。

### <a name="return-value---ulonglong"></a>戻り値 - uLongLong

現在の値。

### <a name="remarks---ulonglong"></a>備考 - uLongLong

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_I8 に設定されている場合、その COMVariant オブジェクトは unsigned longlong バリアント型です。

### <a name="examples---ulonglong"></a>例 - uLongLong

次の例では、VT\_I8 型の新しい COMVariant オブジェクトを作成し、値を 9,223,372,036,854,775,808 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_BOOL); 
```

```xpp
    // Set value of the object 
    var.longLong(9223372036854775808); 
}
```

## <a name="method-ushort"></a>メソッド uShort

VT\_UI2 データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public int uShort([int newValue])
```

### <a name="parameters---ushort"></a>パラメーター - uShort

newValue  
新しい値 (オプション)。

### <a name="return-value---ushort"></a>戻り値 - uShort

現在の値。

### <a name="remarks---ushort"></a>備考 - uShort

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_UI2 に設定されている場合、その COMVariant オブジェクトは unsigned short データ型です。

### <a name="examples---ushort"></a>例 - uShort

次の例では、VT\_UI2 型の新しい COMVariant オブジェクトを作成し、値を 12345 に設定します。

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UI2); 
```

```xpp
    // Set value of the object 
    var.uShort(12345); 
}
```

## <a name="method-variant"></a>メソッド variant

VT\_VARIANT (バリアント) データ タイプの COMVariant オブジェクトの値を取得または設定します。

```xpp
public COMVariant variant([COMVariant newValue])
```

### <a name="parameters---variant"></a>パラメーター - variant

newValue  
新しい値 (オプション)。

### <a name="return-value---variant"></a>戻り値 - variant

現在の値。

### <a name="remarks---variant"></a>備考 - variant

variant プロパティは、ある COMVariant オブジェクトを別の COMVariant オブジェクトにネストするために使用されます。 親オブジェクトを COMDispFunction.call への呼び出しまたは COM クラスへの呼び出しの引数として使用する場合、呼び出されたメソッドは自動的に入れ子になったオブジェクトのデータを抽出します。 このネスト機能は、COM オブジェクトのメソッドが複数のデータ型で動作できる場合に便利です。 バリアントの入れ子は 1 つのレベルのみ許可されます。 オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 データ型が COMVariantType::VT\_VARIANT に設定されている場合、その COMVariant オブジェクトはバリアント型です。

### <a name="examples---variant"></a>例 - variant

次の例では、VT\_I4 (long) 型の COMVariant オブジェクトと VT\_VARIANT 型の COMVariant オブジェクトを作成します. VT\_VARIANT タイプのオブジェクトには、VT\_I4 タイプのオブジェクトの値が割り当てられます。 以下のコードには仮想 COM オブジェクト (「MyCOM.Object」) が含まれており、Finance and Operations アプリケーションの外部でオブジェクトが作成されていない限り実行されません。

```xpp
{ 
    COM com; 
    COMDispFunction funcShow; 
```

```xpp
    COMVariant var1 = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I4); 
```

```xpp
    COMVariant var2 = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_VARIANT); 
```

```xpp
    InteropPermission perm1; 
    InteropPermission perm2; 
```

```xpp
    // Set code access permission to help protect use of COM object 
    perm1 = new InteropPermission(InteropKind::ComInterop); 
    perm1.assert(); 
```

```xpp
    com = new COM("MyCOM.Object"); 
```

```xpp
    // Close code access permission for COM 
    CodeAccessPermission::revertAssert(); 
```

```xpp
    // Set value of 'var1' 
    var1.Long(123456); 
    // Set value of 'var2' to 'var1' 
    var2.Variant(var1); 
```

```xpp
    // Set code access permission to protect use of 
    // COMDispFunction object 
    perm2 = new InteropPermission(InteropKind::ComInterop); 
    perm2.assert(); 
```

```xpp
    funcShow = new COMDispFunction( 
        com,  
        "Show",  
        COMDispContext::METHOD); 
```

```xpp
    // Call funcShow with a long 
    funcShow.Call(var2); 
    // Change value of 'var1' 
     var1.BStr("Hello World"); 
    // Call funcShow with a string 
    funcShow.Call(var2); 
```

```xpp
    // Close code access permission for COMDispFunction 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-variantinoutflag"></a>メソッド variantInOutFlag

COMVariant オブジェクトに対する InOutFlag 設定を設定する返します。

```xpp
public COMVariantInOut variantInOutFlag([COMVariantInOut newValue])
```

### <a name="parameters---variantinoutflag"></a>パラメーター - variantInOutFlag

newValue  
新しい InOutFlag 設定 (オプション)。

### <a name="return-value---variantinoutflag"></a>戻り値 - variantInOutFlag

現在の InOutFlag 設定。

### <a name="remarks---variantinoutflag"></a>備考 - variantInOutFlag

次に、newValue パラメーターで使用可能な値のリストを示します。

-   COMVariantInOut::IN
-   COMVariantInOut::IN\_OUT
-   COMVariantInOut::OUT
-   COMVariantInOut::OUT\_RETVAL.

InOutFlag 設定は、オブジェクトが COMDispFunction.call メソッドで引数として使用されたときに、オブジェクトに格納されているデータがどのように扱われるかを記述します。 InOutFlag 設定の使用可能な値は、Win32 SDK に記述されている COM オートメーション オブジェクトの値に対応します。 COMVariant オブジェクトに格納されたデータは、InOutFlag 設定が変更されても影響を受けません。

### <a name="examples---variantinoutflag"></a>例 - variantInOutFlag

次の例では、InOutFlag 設定が IN に設定されている COMVariant オブジェクトを作成し、variantInOutFlag メソッドを使用して設定を OUT に変更します。

```xpp
{ 
    COMVariant var = new COMVariant(COMVariantInOut::IN); 
```

```xpp
    // Change the 'var' object to be used as an out argument 
    var.variantInOutFlag(COMVariantInOut::OUT); 
}
```

## <a name="method-varianttype"></a>メソッド variantType

COMVariant オブジェクトにそのバリアント データ型を照会するか、データ型を変更します。

```xpp
public COMVariantType variantType([COMVariantType newValue])
```

### <a name="parameters---varianttype"></a>パラメーター - variantType

newValue  
新しいバリアント データ型 (オプション)。

### <a name="return-value---varianttype"></a>戻り値 - variantType

現在のバリアント データ型。

### <a name="remarks---varianttype"></a>備考 - variantType

newValue パラメーターの使用可能な値は次のとおりです。

-   COMVariantType::VT\_I2
-   COMVariantType::VT\_I4
-   COMVariantType::VT\_R4
-   COMVariantType::VT\_R8
-   COMVariantType::VT\_CY
-   COMVariantType::VT\_DATE
-   COMVariantType::VT\_BSTR
-   COMVariantType::VT\_DISPATCH
-   COMVariantType::VT\_ERROR
-   COMVariantType::VT\_BOOL
-   COMVariantType::VT\_VARIANT
-   COMVariantType::VT\_UNKNOWN
-   COMVariantType::VT\_DECIMAL
-   COMVariantType::VT\_I1
-   COMVariantType::VT\_UI1
-   COMVariantType::VT\_UI2
-   COMVariantType::VT\_UI4

バリアント データ型は、オブジェクトが COMDispFunction.call メソッドの呼び出しまたは COM クラスの呼び出しで引数として使用されたときに、オブジェクトに格納されているデータがどのように扱われるかを記述します。 データ型を変更すると、オブジェクトに保持されているデータは削除されます。 使用可能なバリアント データ型については、\[COMVariant.new\] を参照してください。

### <a name="examples---varianttype"></a>例 - variantType

次の例では、新しい COMVariant オブジェクトを作成し、それを long (VT\_I4) データ型に設定します。 その後、variantType メソッドを使用して、データ型を VT\_DATE (日付) に変更します。 オブジェクトが保持するデータは破棄されます。

```xpp
{ 
    COMVariant var = new COMVariant(); 
```

```xpp
    // Set the 'var' object to be a long 
    var.long(123); 
```

```xpp
    // Change var so that it can store a date 
    var.variantType(COMVariantType::VT_DATE); 
}
```

## <a name="method-createdatefromymd"></a>メソッド createDateFromYMD

新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。

```xpp
public static COMVariant createDateFromYMD(int year, int month, int day, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createdatefromymd"></a>パラメーター - createDateFromYMD

年  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値: COMVariantInOut::OUT\_RETVAL

<!-- -->

月  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値: COMVariantInOut::OUT\_RETVAL

<!-- -->

日  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値: COMVariantInOut::OUT\_RETVAL

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値: COMVariantInOut::OUT\_RETVAL

### <a name="return-value---createdatefromymd"></a>戻り値 - createDateFromYMD

新しい COMVariant オブジェクト。

### <a name="remarks---createdatefromymd"></a>備考 - createDateFromYMD

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。 このメソッドを使用すると、日付データ型 (0111901〜31122154) の範囲外の日付を使用できます。 日付範囲内の日付で、COMVariant.createFromDate メソッドを使用することができます。

### <a name="examples---createdatefromymd"></a>例 - createDateFromYMD

次の例では、COMVariant オブジェクトを作成し、4015 年 1 月 1 日の日付で初期化します。

```xpp
COMVariant myDate; 
```

```xpp
myDate = COMVariant::createDateFromYMD(4015,1,1);
```

## <a name="method-createfromarray"></a>メソッド createFromArray

新しい COMVariant オブジェクトを作成し、1 回の操作で配列で初期化します。

```xpp
public static COMVariant createFromArray(Array value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromarray"></a>パラメーター - createFromArray

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromarray"></a>戻り値 - createFromArray

新しい COMVariant オブジェクト。

### <a name="remarks---createfromarray"></a>備考 - createFromArray

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_SAFEARRAY (配列) を持っています。 variantType メソッドの使用により、または safeArray プロパティ メソッドを使用して配列値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_SAFEARRAY に変更することができます。

### <a name="examples---createfromarray"></a>例 - createFromArray

次の例では、新しい COMVariant オブジェクトを作成し、整数の配列で初期化します。

```xpp
{ 
    int i; 
    COMVariant var; 
    Array arr = new Array(Types::INTEGER); 
```

```xpp
    for (i = 1; i <= 10; i++) 
        // Insert 10 values in the array 
        arr.value(i, i); 
```

```xpp
    // Create and initialize a COMVariant object  
    var = COMVariant::createFromArray(arr); 
}
```

## <a name="method-createfromboolean"></a>メソッド createFromBoolean

新しい COMVariant オブジェクトを作成し、1 回の操作でブール値で初期化します。

```xpp
public static COMVariant createFromBoolean(boolean value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromboolean"></a>パラメーター - createFromBoolean

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromboolean"></a>戻り値 - createFromBoolean

新しい COMVariant オブジェクト。

### <a name="remarks---createfromboolean"></a>備考 - createFromBoolean

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_BOOL (ブール値) を持っています。 variantType メソッドの使用により、または boolean プロパティ メソッドを使用してブール値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_BOOL に変更することができます。

### <a name="examples---createfromboolean"></a>例 - createFromBoolean

次の例では、VT\_BOOL バリアント データ型 (ブール値) の COMVariant オブジェクトを作成し、その値を true に設定します。

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromBoolean(TRUE); 
}
```

## <a name="method-createfromcom"></a>メソッド createFromCOM

新しい COMVariant オブジェクトを作成し、1 回の操作で COM クラスで初期化します。

```xpp
public static COMVariant createFromCOM(COM value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromcom"></a>パラメーター - createFromCOM

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromcom"></a>戻り値 - createFromCOM

新しい COMVariant オブジェクト。

### <a name="remarks---createfromcom"></a>備考 - createFromCOM

inOutFlag パラメーターの使用可能な値は次のとおりです。

-   COMVariantInOut::IN
-   COMVariantInOut::IN\_OUT
-   COMVariantInOut::OUT
-   COMVariantInOut::OUT\_RETVAL

### <a name="examples---createfromcom"></a>例 - createFromCOM

次の例では、新しい COMVariant オブジェクトを作成し、COM オブジェクトで初期化します。

```xpp
{ 
    COMVariant var; 
    COM com = new COM("MyCOM.Object"); 
```

```xpp
    var = COMVariant::createFromCOM(com); 
}
```

## <a name="method-createfromdate"></a>メソッド createFromDate

新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。

```xpp
public static COMVariant createFromDate(Date value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromdate"></a>パラメーター - createFromDate

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromdate"></a>戻り値 - createFromDate

新しい COMVariant オブジェクト。

### <a name="remarks---createfromdate"></a>備考 - createFromDate

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。 variantType メソッドの使用により、または date プロパティ メソッドを使用して時刻値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_DATE に変更することができます。 Axapta の日付タイプ (0111901〜31122154) の範囲外の日付を使用する場合は、COMVariant.createDateFromYMD メソッドを使用します。

### <a name="examples---createfromdate"></a>例 - createFromDate

次の例では、COMVariant オブジェクトを作成し、現在の日付で初期化します。

```xpp
COMVariant theDay; 
```

```xpp
theDay = COMVariant::createFromDate(today()); 
info(theDay.toString());
```

## <a name="method-createfromdateandtime"></a>メソッド createFromDateAndTime

新しい COMVariant オブジェクトを作成し、1 回の操作で日時で初期化します。

```xpp
public static COMVariant createFromDateAndTime(Date date, int time, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromdateandtime"></a>パラメーター - createFromDateAndTime

日付  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

タイム  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromdateandtime"></a>戻り値 - createFromDateAndTime

新しい COMVariant オブジェクト。

### <a name="remarks---createfromdateandtime"></a>備考 - createFromDateAndTime

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。 variantType メソッドを使用することにより、既存の COMVariant オブジェクトを VT\_DATE に変更することができます。

### <a name="examples---createfromdateandtime"></a>例 - createFromDateAndTime

次の例では、COMVariant オブジェクトを作成し、現在の日付と深夜 0 時から 10 秒の間隔の時刻を割り当てます。

```xpp
date theDay; 
COMVariant theDayAndTime; 
```

```xpp
theDay = today(); 
theDayAndTime = COMVariant::createFromDateAndTime(theDay, 10); 
info(theDayAndTime.toString());
```

## <a name="method-createfromint"></a>メソッド createFromInt

新しい COMVariant オブジェクトを作成し、1 回の操作で整数値で初期化します。

```xpp
public static COMVariant createFromInt(int value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromint"></a>パラメーター - createFromInt

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromint"></a>戻り値 - createFromInt

新しい COMVariant オブジェクト。

### <a name="remarks---createfromint"></a>備考 - createFromInt

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_I4 (整数) を持っています。 variantType メソッドの使用により、または int プロパティ メソッドを使用して整数値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_I4 に変更することができます。

### <a name="examples---createfromint"></a>例 - createFromInt

次の例では、VT\_I4 バリアント データ型 (整数) の COMVariant オブジェクトを作成し、値を 123 に設定します。

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromInt(123); 
}
```

## <a name="method-createfromint64"></a>メソッド createFromInt64

新しい COMVariant オブジェクトを作成し、1 回の操作でint64 値 (longLong や uLongLong) で初期化します。

```xpp
public static COMVariant createFromInt64(Int64 value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromint64"></a>パラメーター - createFromInt64

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromint64"></a>戻り値 - createFromInt64

新しい COMVariant オブジェクト。

### <a name="remarks---createfromint64"></a>備考 - createFromInt64

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_I8 (int64) を持っています。 variantType メソッドの使用により、または longLong や uLongLong プロパティ メソッドを使用して int64 値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_I8 に変更することができます。

### <a name="examples---createfromint64"></a>例 - createFromInt64

次の例では、VT\_I8 バリアント データ型 (整数) の COMVariant オブジェクトを作成し、値を 123456 に設定します。

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromInt64(123456); 
}
```

## <a name="method-createfromreal"></a>メソッド createFromReal

新しい COMVariant オブジェクトを作成し、1 回の操作で実際の値で初期化します。

```xpp
public static COMVariant createFromReal(Real value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromreal"></a>パラメーター - createFromReal

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromreal"></a>戻り値 - createFromReal

新しい COMVariant オブジェクト。

### <a name="remarks---createfromreal"></a>備考 - createFromReal

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_R8 (実数) を持っています。 variantType メソッドの使用により、または double プロパティ メソッドを使用してブール値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_R8 に変更することができます。

### <a name="examples---createfromreal"></a>例 - createFromReal

次の例では、VT\_R8 バリアント データ型 (実数) の COMVariant オブジェクトを作成し、値を 123.456 に設定します。

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromReal(123.456); 
}
```

## <a name="method-createfromstr"></a>メソッド createFromStr

新しい COMVariant オブジェクトを作成し、1 回の操作で文字列で初期化します。

```xpp
public static COMVariant createFromStr(str value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromstr"></a>パラメーター - createFromStr

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromstr"></a>戻り値 - createFromStr

新しい COMVariant オブジェクト。

### <a name="remarks---createfromstr"></a>備考 - createFromStr

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_BSTR (文字列) を持っています。 variantType メソッドの使用により、または bStr プロパティ メソッドを使用して文字列値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_BSTR に変更することができます。

### <a name="examples---createfromstr"></a>例 - createFromStr

次の例では、VT\_BSTR バリアント データ型の COMVariant オブジェクトを作成し、値を "Hello World" に設定します。

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromStr("Hello World"); 
}
```

## <a name="method-createfromtime"></a>メソッド createFromTime

新しい COMVariant オブジェクトを作成し、1 回の操作で時刻値で初期化します。

```xpp
public static COMVariant createFromTime(int value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromtime"></a>パラメーター - createFromTime

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

### <a name="return-value---createfromtime"></a>戻り値 - createFromTime

新しい COMVariant オブジェクト。

### <a name="remarks---createfromtime"></a>備考 - createFromTime

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。 variantType メソッドの使用により、または time プロパティ メソッドを使用して時刻値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_DATE に変更することができます。

### <a name="examples---createfromtime"></a>例 - createFromTime

次の例では、COMVariant オブジェクトを作成し、時刻の部分を深夜 0 時から 10 秒の間隔に設定します。

```xpp
COMVariant theTime; 
```

```xpp
theTime = COMVariant::createFromTime(10); 
info(theTime.toString());
```

## <a name="method-createfromutcdatetime"></a>メソッド createFromUtcDateTime

```xpp
public static COMVariant createFromUtcDateTime(DateTime value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromutcdatetime"></a>パラメーター - createFromUtcDateTime

値  

<!-- -->

inOutFlag  

### <a name="return-value---createfromutcdatetime"></a>戻り値 - createFromUtcDateTime

## <a name="method-createnovalue"></a>メソッド createNoValue

値を持たない VT\_エラー バリアント タイプの COMVariant オブジェクトを作成します。

```xpp
public static COMVariant createNoValue()
```

### <a name="return-value---createnovalue"></a>戻り値 - createNoValue

新しい COMVariant オブジェクト。

### <a name="remarks---createnovalue"></a>備考 - createNoValue

オプションの COM パラメーターには、値を持たない COMVariant オブジェクトを使用できます。

### <a name="examples---createnovalue"></a>例 - createNoValue

次の例では、空の COMVariant オブジェクトを作成します。

```xpp
COMVariant noValue; 
```

```xpp
noValue = COMVariant::createNoValue(); 
info(noValue.toString());
```

## <a name="method-new"></a>メソッド new

COM オートメーション オブジェクトのメソッドまたはプロパティに引数を渡すために使用できる COMVariant オブジェクトを作成します。

```xpp
public void new([COMVariantInOut inOutFlag], [COMVariantType type])
```

### <a name="parameters---new"></a>パラメーター - new

inOutFlag  
格納するデータのタイプ、オプション。 これらは、COMVariantType システム列挙型によって提供される可能性のある値です。

<!-- -->

タイプ  
格納するデータのタイプ、オプション。 これらは、COMVariantType システム列挙型によって提供される可能性のある値です。

### <a name="remarks---new"></a>備考 - new

型パラメーターが省略されると、COMVariant オブジェクトのプロパティのいずれかによって必要とされるまで、内部メモリは割り当てられません。 プロパティ メソッドの一覧については、\[COMVariant クラス\] を参照してください。 異なるタイプの新しい値を指定することにより (いずれかのプロパティ メソッドを使用して)、バリアント データ型を設定後に変更することができます。 COMVariantType 列挙によって定義されるデータ型は、Win32 SDK によって定義されるバリアントデータ型と同じです。

### <a name="examples---new"></a>例 - new

次の例では、3 つの COMVariant オブジェクトを作成します。

-   varIn は COM メソッドにデータを渡すためのものです。内部には文字列および短整数が格納されています。
-   varOut は VT\_I4 (long) タイプのデータを受け取るためのものです。
-   varOutRetval はデータをパスまたは受け取ることができます。そのデータ タイプは COMDispFunction.call メソッドでセットすることができます。

<!-- -->

```xpp
{ 
    COMVariant varIn  = new COMVariant(); 
    COMVariant varOut = new COMVariant( 
        COMVariantInOut::OUT,  
        COMVariantType::VT_I4); 
    COMVariant varOutRetval = new COMVariant( 
        COMVariantInOut::OUT_RETVAL); ; 
```

```xpp
    // Store a text string in the varIn object 
    varIn.bStr("Hello World"); 
```

```xpp
    // Change varIn to a short. 
    // Text string stored in varIn is automatically released 
    varIn.short(123);  
}
```

## <a name="method-novalue"></a>メソッド noValue

既存の COMVariant オブジェクトの内容を削除し、COMDispFunction.call メソッドまたは COM クラスで使用されている場合は、未指定の引数として機能させることができます。

```xpp
public void noValue()
```

### <a name="remarks---novalue"></a>備考 - noValue

値を持たないバリアントは、null にできるパラメーターが COM メソッドにあるときに使用できます。 引数が指定されていない COM オブジェクトと、独自の既定値を使用する必要がある COM オブジェクトを示します。 COM オブジェクトに対するメソッドを呼び出すときは、COMArgument::NoValue 列挙型を使用して、未指定の引数を指定することもできます。 COMDispFunction クラスを通じて呼び出すときに、この列挙型は使用できないことに注意してください。

### <a name="examples---novalue"></a>例 - noValue

次の例は、3 番目の引数 unspecified を使用して COM.multiply メソッドを呼び出す方法を示しています。 以下のコードには仮想 COM オブジェクト (「MyCOM.Object」) が含まれており、Finance and Operations アプリケーションの外部でオブジェクトが作成されていない限り実行されません。

```xpp
{ 
    COM        com; 
    COMVariant varArg1 = new COMVariant(); 
    COMVariant varArg2 = new COMVariant(); 
    COMVariant varArg3 = new COMVariant(); 
    COMVariant varRet  = new COMVariant(COMVariantInOut::OUT_RETVAL); 
    real       ret; 
    InteropPermission perm; 
```

```xpp
    // Set code access permission to help protect use of COM object 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    // Permission scope starts here 
    perm.assert(); 
```

```xpp
    com = new COM("MyCOM.Object"); 
```

```xpp
    // Specify arguments for the multiply method 
    varArg1.float(123); 
    varArg2.float(456); 
    varArg3.noValue(); 
    varRet = com.multiply(varArg1, varArg2, varArg3); 
    // �or� 
    varRet = com.multiply(varArg1, varArg2, COMArgument::NoValue); 
     ret = varRet.double(); 
    // ret is now 56088 (123*456) 
```

```xpp
    // Close code access permission 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-finalize"></a>メソッド finalize

実装されていません。 明示的にオブジェクトを破棄する必要がある場合は、このメソッドをオーバーライドすることができます。

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a>備考 - finalize

メソッドのすべてのステートメントを実行する確定メソッドを呼び出す必要があります。メソッドを確定する暗黙的な呼び出しはありません。

