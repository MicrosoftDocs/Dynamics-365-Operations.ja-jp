---
title: COM クラス
description: このトピックでは、COM クラスについて説明します。
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
ms.openlocfilehash: 361cdc27fcc0da6dd605381b45a14500760bee13
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502715"
---
# <a name="class-com"></a>クラス COM

[!include [banner](../../includes/banner.md)]

```xpp
class COM
```

COM クラスは、コンポーネント オブジェクト モデル (COM) オブジェクトを作成するためにも使用されます。

## <a name="remarks"></a>備考

COM クラスは、分散コンポーネント オブジェクト モデル (DCOM) もサポートしています。 DCOM は、DCOM をサポートするオブジェクトをリモート コンピュータで実行できるようにします。 COM クラスを使用して COM オブジェクトがインスタンス化されると、そのメソッドおよびプロパティに、COMDispFunction クラスかまたは COM クラスの 拡張構文を使用してアクセスできます。 拡張構文を使用すると、Lookup リストに表示されていなくても 、メソッドとプロパティを COM オブジェクトで直接呼び出すことができます (例: com.comMethod("Hello World");)。 拡張構文は、任意の数の引数を取るメソッドとプロパティへの呼び出しをサポートしています。 一部の COM オブジェクトは、省略可能な引数の概念をサポートします。 オプションのバリアント引数のみ省略できます。 オプションの引数を省略すると、COM オブジェクトは、既定値を使用します。 COM オブジェクトの引数を省略し、強制的に既定値を使用するには、次の例に示すように、COMArgument::NoValue 列挙型を指定します。

```xpp
com.comMethod(COMArgument::NoValue, "Hello Another World");
```


COM オブジェクトから省略する引数が引数リストの最後に表示される場合は、コードから省略します。 COM クラスの引数型と戻り値型の拡張構文では、次の型がサポートされています。

-   array
-   COM
-   COMVariant
-   日付
-   列挙型
-   int
-   real
-   str

COM オブジェクトが日付を返し、拡張構文が使用されている場合は、COM メソッドの戻り値を COM Variant クラス変数に割り当てる必要があります。 そして、日付と時刻のプロパティを使用して、COMVariant クラスから実際の日時 (形式) を抽出することができます。 日付の戻り値に COMVariant クラスではなく日付変数が割り当てられている場合、日付の時間の部分は失われます。 拡張構文を使用するときは、オブジェクトに対して COM クラス メソッド (ルックアップ リストに表示されるメソッド) をまだ呼び出すことができます。 COM クラス メソッドは、実際の COM オブジェクトでのメソッドよりも優先順位が高くなります。 COM オブジェクトのメソッドが COM クラスのメソッドと同じ名前 (たとえば、attach) である場合、そのメソッドを COM オブジェクトで呼び出すことはできません。 COM クラスで同じ名前を持つメソッドを呼び出すのではなく、COM オブジェクトのメソッドを呼び出せるようにするには、重複するメソッド名の先頭にアンダースコアを付けます (たとえば、com.\_detach();)。 COM クラスの拡張構文は、コンパイル時ではなく実行時に評価され、パフォーマンスがわずかに低下します。 パフォーマンスの高いコードが必要な場合は、COMDispFunction クラスを使用することを検討します。 このクラスは、COM クラスの拡張構文よりもパフォーマンスが向上しています。

## <a name="examples"></a>例

この例では、Scripting.FileSystemObject COM オブジェクトから GetFileName メソッドを呼び出します。

```xpp
void COMExample() 
{ 
    COM               com; 
    str               result; 
    InteropPermission perm; 
    ; 
```

```xpp
    // Set code access permission to help protect the use of the 
    // COM object. 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    // Permission scope starts here. 
    perm.assert(); 
```

```xpp
    com = new COM("Scripting.FileSystemObject"); 
    if (com != null) 
    { 
        result = com.GetFileName(@"c:\boot.ini"); 
    } 
```

```xpp
    // Close code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| public AnyType dispatch(VarArg )                                                                            | 予約済み。 メソッドを明示的に呼び出さないでください。                                                                                                |
| public str documentationName()                                                                              | COM クラスのインスタンスに関連付けられている COM オブジェクトの名前を表すテキストを返します。                                            |
| public COMError error()                                                                                     | COM クラスのインスタンスに関連付けられている COMError オブジェクトを返します。                                                             |
| public ComInterface interface()                                                                             | COM オブジェクトに関連付けられているインターフェイスを返します。                                                                                |
| public int lcid(\[int lcid\])                                                                               |                                                                                                                                              |
| public str toString()                                                                                       | COM クラスのインスタンスを表す文字列を返します。                                                                              |
| ::public static COM createFromInterface(ComInterface interface)                                             | 指定された COM インターフェイスを使用して COM クラスのインスタンスを作成します。                                                                   |
| ::public static COM createFromObject(COM object)                                                            | 指定された COM オブジェクトを使用して COM クラスのインスタンスを作成します。                                                                      |
| ::public static COM createFromVariant(COMVariant variant)                                                   | COMVariant クラスの指定されたインスタンスを使用して、COM クラスのインスタンスを作成します。                                                |
| ::public static COM getObject(str className)                                                                | 実行している COM オブジェクトのインスタンスを返します。                                                                                         |
| ::public static COM getObjectEx(str fileName)                                                               | ファイル名で指定されている COM オブジェクトのインスタンスを返します。                                                                      |
| ::public static AnyType unsupported(int action, \[AnyType param1\], \[AnyType param2\], \[AnyType param3\]) | 予約済み。                                                                                                                                    |
| public void finalize()                                                                                      | COM クラスのインスタンスに関連付けられているリソースを解放します。                                                                      |
| public void new(\[str className\], \[str computerName\])                                                    | COM クラスに接続できる COM クラスのインスタンスを作成し、オプションで、指定されたコンピュータ上で COM オブジェクトをインスタンス化することができます。 |
| public void attach(ComInterface interface)                                                                  | COM クラスのインスタンスを COM インターフェイスに関連付けます。                                                                                    |
| public void detach()                                                                                        | 関連付けられているクラスから COM オブジェクトを解除します。                                                                            |

## <a name="method-dispatch"></a>メソッド dispatch

予約済み。 メソッドを明示的に呼び出さないでください。

```xpp
public AnyType dispatch(VarArg )
```

### <a name="parameters---dispatch"></a>パラメーター - dispatch


### <a name="return-value---dispatch"></a>戻り値 - dispatch

## <a name="method-documentationname"></a>メソッド documentationName

COM クラスのインスタンスに関連付けられている COM オブジェクトの名前を表すテキストを返します。

```xpp
public str documentationName()
```

### <a name="return-value---documentationname"></a>戻り値 - documentationName

COM クラスのインスタンスに関連付けられている COM オブジェクトのテキスト名。COM オブジェクトのドキュメント名がない場合は空の文字列です。

### <a name="remarks---documentationname"></a>備考 - documentationName

クラスのテキスト名は、そのクラスを記述するためにクラスによって使用されます。 テキスト名は、クラスをインスタンス化するために使用されるクラス名とは異なります。

### <a name="examples---documentationname"></a>例 - documentationName

次の例は、COM オブジェクトのドキュメント名を取得する方法を示しています。

```xpp
str docName; 
; 
// The obj that was previously instantiated. 
docName = obj.documentationName(); 
info(strfmt("documentationName: %1", docName));
```

## <a name="method-error"></a>メソッド error

COM クラスのインスタンスに関連付けられている COMError オブジェクトを返します。

```xpp
public COMError error()
```

### <a name="return-value---error"></a>戻り値 - error

COM クラスのインスタンスに関連付けられているエラーを表す COMError 値。

### <a name="examples---error"></a>例 - error

次の例は、COM クラスのインスタンスに関連付けられているエラー オブジェクトを取得する方法を示しています。

```xpp
COMError err; 
```

```xpp
// The obj variable was previously instantiated. 
err = obj.error(); 
```

```xpp
// Output the error number. 
info(strfmt("Error: %1", err.number()))
```

## <a name="method-interface"></a>メソッド interface

COM オブジェクトに関連付けられているインターフェイスを返します。

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a>戻り値 - interface

COM オブジェクトに関連付けられているインターフェイス。インターフェイスが COM オブジェクトに関連付けられていない場合は 0 (ゼロ)。

### <a name="examples---interface"></a>例 - interface

次の例は、COM オブジェクトに関連付けられているインターフェイスを取得する方法を示しています。

```xpp
// The obj variable was previously instantiated. 
info(strfmt("Interface: %1", obj.interface()));
```

## <a name="method-lcid"></a>メソッド lcid

```xpp
public int lcid([int lcid])
```

### <a name="parameters---lcid"></a>パラメーター - lcid

lcid  

### <a name="return-value---lcid"></a>戻り値 - lcid

## <a name="method-tostring"></a>メソッド toString

COM クラスのインスタンスを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

COM クラスのインスタンスの説明を含む文字列。

### <a name="examples---tostring"></a>例 - toString

次の例は、toString メソッドの使用方法を示しています。

```xpp
print objCOM.toString();
```

## <a name="method-createfrominterface"></a>メソッド createFromInterface

指定された COM インターフェイスを使用して COM クラスのインスタンスを作成します。

```xpp
public static COM createFromInterface(ComInterface interface)
```

### <a name="parameters---createfrominterface"></a>パラメーター - createFromInterface

インターフェイス  
COM クラスの新しいインスタンスを作成するために使用するインターフェイス。

### <a name="return-value---createfrominterface"></a>戻り値 - createFromInterface

インターフェイス パラメーターで指定される COM インターフェイスの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。

### <a name="remarks---createfrominterface"></a>備考 - createFromInterface

アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。

## <a name="method-createfromobject"></a>メソッド createFromObject

指定された COM オブジェクトを使用して COM クラスのインスタンスを作成します。

```xpp
public static COM createFromObject(COM object)
```

### <a name="parameters---createfromobject"></a>パラメーター - createFromObject

オブジェクト  
COM クラスの新しいインスタンスを作成するために使用する COM クラスのインスタンス。

### <a name="return-value---createfromobject"></a>戻り値 - createFromObject

オブジェクト パラメーターで指定される COM オブジェクトの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。

### <a name="remarks---createfromobject"></a>備考 - createFromObject

アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。

## <a name="method-createfromvariant"></a>メソッド createFromVariant

COMVariant クラスの指定されたインスタンスを使用して、COM クラスのインスタンスを作成します。

```xpp
public static COM createFromVariant(COMVariant variant)
```

### <a name="parameters---createfromvariant"></a>パラメーター - createFromVariant

バリアント  
COM クラスの新しいインスタンスを作成するために使用する COMVariant クラスのインスタンス。

### <a name="return-value---createfromvariant"></a>戻り値 - createFromVariant

バリアント パラメーターで指定される COM オブジェクトの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。

### <a name="remarks---createfromvariant"></a>備考 - createFromVariant

アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。

## <a name="method-getobject"></a>メソッド getObject

実行している COM オブジェクトのインスタンスを返します。

```xpp
public static COM getObject(str className)
```

### <a name="parameters---getobject"></a>パラメーター - getObject

className  
COM クラスのインスタンスを作成するために使用される COM オブジェクトの ProgID 値またはクラス名。

### <a name="return-value---getobject"></a>戻り値 - getObject

className パラメーターで指定されるクラスの COM クラスのインスタンス。インスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。

### <a name="remarks---getobject"></a>備考 - getObject

指定した COM オブジェクトの複数インスタンスが実行している場合は、getObject メソッドによってどのインスタンスが返されるかを保証できません。 一部の COM オブジェクトは、このメソッドの呼び出しを可能にする拡張機能をサポートしていません。

### <a name="examples---getobject"></a>例 - getObject

次の例は、実行中の COM オブジェクトのインスタンスを取得する方法を示しています。

```xpp
COM objExcel, objWorkBook, objWorkBooks; 
InteropPermission perm; 
```

```xpp
// Set code access permission to help protect the use of COM.new. 
perm = new InteropPermission(InteropKind::ComInterop); 
perm.assert(); 
```

```xpp
objExcel = COM::getObject("Excel.Application"); 
```

```xpp
if (!objExcel) 
{ 
    // Unable to connect to a running instance of Microsoft Excel. 
    // Try starting it. 
    objExcel = new COM("Excel.Application"); 
    if (!objExcel) 
    { 
        Info ("Unable to find or create an instance of Excel"); 
        return;  // Or other error action. 
    }  
} 
// Close code access permission scope. 
CodeAccessPermission::revertAssert(); 
```

```xpp
objExcel.visible(true); 
objWorkBooks = objExcel.workbooks(); 
if (objWorkBooks) 
{ 
    objWorkBook = objWorkBooks.open("d:\mydata\book1.xls"); 
}
```

## <a name="method-getobjectex"></a>メソッド getObjectEx

ファイル名で指定されている COM オブジェクトのインスタンスを返します。

```xpp
public static COM getObjectEx(str fileName)
```

### <a name="parameters---getobjectex"></a>パラメーター - getObjectEx

fileName  
COM クラスのインスタンスを作成するために使用される COM オブジェクトの機能を提供するファイルの名前。

### <a name="return-value---getobjectex"></a>戻り値 - getObjectEx

filename パラメーターで指定される COM クラスのインスタンス。インスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。

### <a name="remarks---getobjectex"></a>備考 - getObjectEx

アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。

## <a name="method-unsupported"></a>メソッド unsupported

予約済み。

```xpp
public static AnyType unsupported(int action, [AnyType param1], [AnyType param2], [AnyType param3])
```

### <a name="parameters---unsupported"></a>パラメーター - unsupported

アクション  

<!-- -->

param1  

<!-- -->

param2  

<!-- -->

param3  

### <a name="return-value---unsupported"></a>戻り値 - unsupported

## <a name="method-finalize"></a>メソッド finalize

COM クラスのインスタンスに関連付けられているリソースを解放します。

```xpp
public void finalize()
```

### <a name="examples---finalize"></a>例 - finalize

次の例では、finalize メソッドの使用方法を示しています。

```xpp
objCOM.finalize();
```

## <a name="method-new"></a>メソッド new

COM クラスに接続できる COM クラスのインスタンスを作成し、オプションで、指定されたコンピュータ上で COM オブジェクトをインスタンス化することができます。

```xpp
public void new([str className], [str computerName])
```

### <a name="parameters---new"></a>パラメーター - new

className  
COM オブジェクトをインスタンス化するリモート コンピューターの名前 (オプション)。 このパラメータを省略すると、COM オブジェクトはローカル コンピューターでインスタンス化されます。 コンピューター名が指定されている場合は、ローカル コンピューターとリモート コンピューターの両方に DCOM システムのコンポーネントをインストールする必要があります。 特定の COM オブジェクトは DCOM をサポートする必要があり、ローカル コンピューターとリモート コンピューターの両方で正しく構成されている必要があります。 システム コンポーネントは、Microsoft Windows 98、Windows NT、およびそれ以降のバージョンの標準コンポーネントです。 Windows 95 では、DCOM システム コンポーネントをインストールする必要があります。

<!-- -->

computerName  
COM オブジェクトをインスタンス化するリモート コンピューターの名前 (オプション)。 このパラメータを省略すると、COM オブジェクトはローカル コンピューターでインスタンス化されます。 コンピューター名が指定されている場合は、ローカル コンピューターとリモート コンピューターの両方に DCOM システムのコンポーネントをインストールする必要があります。 特定の COM オブジェクトは DCOM をサポートする必要があり、ローカル コンピューターとリモート コンピューターの両方で正しく構成されている必要があります。 システム コンポーネントは、Microsoft Windows 98、Windows NT、およびそれ以降のバージョンの標準コンポーネントです。 Windows 95 では、DCOM システム コンポーネントをインストールする必要があります。

### <a name="remarks---new"></a>備考 - new

COM オブジェクトのクラス名は、そのプログラム識別子 (ProgID) またはそのクラス識別子 (CLSID) です。

-   ProgID の形式: program.component.version
-   ClSID は 128 ビット値であり、その形式は {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} です。

攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---new"></a>例 - new

この例では、Scripting.FileSystemObject COM オブジェクトから GetFileName メソッドを呼び出します。

```xpp
void COMExample() 
{ 
    COM               com; 
    str               result; 
    InteropPermission perm; 
```

```xpp
    // Set the code access permission to help protect the use of the 
    // COM object. 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    // Permission scope starts here. 
    perm.assert(); 
```

```xpp
    com = new COM("Scripting.FileSystemObject"); 
    if (com != null) 
    { 
        result = com.GetFileName(@"c:\boot.ini"); 
    } 
```

```xpp
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-attach"></a>メソッド attach

COM クラスのインスタンスを COM インターフェイスに関連付けます。

```xpp
public void attach(ComInterface interface)
```

### <a name="parameters---attach"></a>パラメーター - attach

インターフェイス  
COM クラスのインスタンスに関連付けるインターフェイス。

### <a name="remarks---attach"></a>備考 - attach

このメソッドは、一部の COM オブジェクトは他の COM オブジェクトによってのみインスタンス化されるが、COM クラスによって直接インスタンス化することができないため、用意されています。

## <a name="method-detach"></a>メソッド detach

関連付けられているクラスから COM オブジェクトを解除します。

```xpp
public void detach()
```

### <a name="remarks---detach"></a>備考 - detach

たとえば、このメソッドは、接続または新しいメソッドの呼び出しから COM オブジェクトを切り離すために呼び出されます。

