---
title: CodeAccessPermission クラス
description: このトピックでは、CodeAccessPermission クラスについて説明します。
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
ms.openlocfilehash: e3f7f6d30d76a85d4c1120e22c46c1917e0d37b9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502745"
---
# <a name="class-codeaccesspermission"></a>クラス CodeAccessPermission

[!include [banner](../../includes/banner.md)]

```xpp
class CodeAccessPermission extends Object
```

CodeAccessPermission クラスは、コード アクセス許可の基になる構造を定義します。

## <a name="remarks"></a>備考

次のクラスは、CodeAccessPermission クラスを拡張します: ExecutePermission、FileIOPermission、InteropPermission、RunAsPermission、SkipAOSValidationPermission、SqlDataDictionaryPermission、SqlStatementExecutePermission、および SysDatabaseLogPermission。

## <a name="examples"></a>例

次のコード例は、CodeAccessPermission クラスから派生したクラスを示しています。

```xpp
final class SysTestCodeAccessPermission extends CodeAccessPermission 
{ 
    str data; 
}
```

このコード例は、API を保護するプロセスのステップを示しています。

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                                                                                       |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | アクセス許可クラス オブジェクトのコピーを作成し、返します。                                                                                          |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。                         |
| public void new()                                      | CodeAccessPermission クラスの新しいインスタンスを初期化します。                                                                                     |
| public void assert()                                   | 呼び出しコードがアクセス許可によって保護されている API を呼び出すことができることを宣言します。                                                               |
| public void demand()                                   | コール スタックをチェックして、API を呼び出すために必要なアクセス許可が呼び出しコードに与えられているかどうかを判断します。                 |
| ::public static void revertAssert()                    | CodeAccessPermission.assert および CodeAccessPermission::assertMultiple メソッドへの以前の呼び出しを削除し、無効にします。 |
| ::public static void assertMultiple(Set permissionSet) | 呼び出しコードが指定されたコレクションでのアクセス許可によって保護されている API を呼び出すことができることを宣言します。                           |

## <a name="method-copy"></a>メソッド copy

アクセス許可クラス オブジェクトのコピーを作成し、返します。

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

現在の派生クラスオブジェクトのコピーです。

### <a name="remarks---copy"></a>備考 - copy

API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。

### <a name="examples---copy"></a>例 - copy

次のコード例は、copy メソッドを上書きして、CodeAccessPermission クラスから派生したクラスのコピーを作成して返す方法を示しています。

```xpp
public CodeAccessPermission copy() 
{ 
    return new SysTestCodeAccessPermission(_data); 
}
```

## <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a>パラメーター - isSubsetOf

target  
CodeAccessPermission クラス オブジェクト。

### <a name="return-value---issubsetof"></a>戻り値 - isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

### <a name="remarks---issubsetof"></a>備考 - isSubsetOf

API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。

### <a name="examples---issubsetof"></a>例 - isSubsetOf

次の例は、isSubsetOf メソッドを上書きして、現在のオブジェクトに格納されているアクセス権が \_target にあるかどうかを判断する方法を示しています。.

```xpp
public boolean isSubsetOf(CodeAccessPermission _target) 
{ 
    SysTestCodeAccessPermission sysTarget = _target; 
    return this.handle() == _target.handle(); 
}
```

## <a name="method-new"></a>メソッド new

CodeAccessPermission クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-assert"></a>メソッド assert

呼び出しコードがアクセス許可によって保護されている API を呼び出すことができることを宣言します。

```xpp
public void assert()
```

### <a name="remarks---assert"></a>備考 - assert

API を起動する前に、保護された API の派生クラスで assert メソッドを呼び出す必要があります。 アクセス許可によって保護されている API の詳細については、「セキュリティで保護された API」を参照してください。 保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド

同じ呼び出しコードにおいて Assert メソッドに対する複数の連続した呼び出しはサポートされません。 assert メソッドへの各呼び出し間で CodeAccessPermission::revertAssert メソッドを呼び出すか、または CodeAccessPermission::assertMultiple メソッドを呼び出すかのいずれかを行います。 assertmethod を複数にわたり連続して呼び出すと、コードを実行するときに Infolog によってエラーが表示されます。

### <a name="examples---assert"></a>例 - assert

次のコード例は、アクセス許可で保護されている AsciiIo クラスが呼び出される前に assert メソッドを呼び出す方法を示しています。 assert メソッドは、CodeAccessPermission クラスから派生した FileIOPermission クラスのメンバーです。

```xpp
server static void main(Args args) 
{ 
    FileIoPermission _perm; 
    AsciiIo a; 
```


```xpp
    _perm = new FileIoPermission("c:\File.txt",'r'); 
    _perm.assert(); 
```

```xpp
    // Invoke the protected API. 
    a = new AsciiIo("c:\File.txt",'r'); 
}
```

## <a name="method-demand"></a>メソッド demand

コール スタックをチェックして、API を呼び出すために必要なアクセス許可が呼び出しコードに与えられているかどうかを判断します。

```xpp
public void demand()
```

### <a name="examples---demand"></a>例 - demand

次のコード例は、API 機能を実行する前に、API を呼び出すコードに data 変数で指定されたリソースへのアクセス許可が与えられているかどうかを判断するための、demand メソッドの呼び出しを示しています。

```xpp
public static void main(str data) 
{ 
    SysTestCodeAccessPermission p = new SysTestCodeAccessPermission(data); 
    p.demand(); 
```

```xpp
    //Add functionality 
}
```

このコード例は、API を保護するプロセスのステップを示しています。

## <a name="method-revertassert"></a>メソッド revertAssert

CodeAccessPermission.assert および CodeAccessPermission::assertMultiple メソッドへの以前の呼び出しを削除し、無効にします。

```xpp
public static void revertAssert()
```

### <a name="remarks---revertassert"></a>備考 - revertAssert

同じ呼び出しコードで assert メソッドに複数の呼び出しをするときは、それぞれの呼び出しの間に revertAssert メソッドを呼び出す必要があります。 それ以外の場合、情報ログには、コードを実行するときにエラーが表示されます。 assert メソッドを1回だけ呼び出すとき、または CodeAccessPermission::assertMultiple メソッドを呼び出すときは、保護された API の起動後にも revertAssert メソッドを呼び出して、アサートの範囲を制限することをお勧めします。

### <a name="examples---revertassert"></a>例 - revertAssert

次のコード例は、ユーザーが CodeAccessPermission.assert メソッドとアクセス許可で保護されている AsciiIo クラスの呼び出しを呼び出した後の、 CodeAccessPermission::revertAssert メソッドへの呼び出しを示しています。

```xpp
server static void main(Args args) 
{ 
    FileIoPermission _perm; 
    AsciiIo a; 
```


```xpp
    _perm = new FileIoPermission("c:\File.txt",'r'); 
    _perm.assert(); 
```

```xpp
    //invoke protected API 
    a = new AsciiIo("c:\File.txt",'r'); 
```

```xpp
    // Optionally call revertAssert() to limit scope of assert. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-assertmultiple"></a>メソッド assertMultiple

呼び出しコードが指定されたコレクションでのアクセス許可によって保護されている API を呼び出すことができることを宣言します。

```xpp
public static void assertMultiple(Set permissionSet)
```

### <a name="parameters---assertmultiple"></a>パラメーター - assertMultiple

permissionSet  
アクセス許可のコレクションを含むセット クラス オブジェクト。

### <a name="remarks---assertmultiple"></a>備考 - assertMultiple

同じ呼び出しコードで CodeAccessPermission.assert および CodeAccessPermission::revertAssert メソッドに対する複数の連続する呼び出しをする代わりに、assertMultple メソッドを呼び出します。

### <a name="examples---assertmultiple"></a>例 - assertMultiple

次のコード例は、CodeAccessPermission::assertMultple メソッドを呼び出します。 このコード例は WinAPIServer::createFile メソッドを呼び出します。このメソッド、CodeAccessPermission::assertMultple メソッドへの事前の呼び出しがない場合は失敗します。 このコード例は、作成する新しいクラスに追加できる静的メソッドです。 MyClass::RunOnServerPermissionTest のようなコード行を使用して、X++ ジョブから静的メソッドを呼び出すことができます。 コードの例では、WinAPIServer クラスに、セキュリティで保護されたメソッドがいくつかあります。 WinAPIServer クラスは、クライアント層ではなく、サーバー層で実行されます。 したがって、コード例のメソッドはサーバー層でも実行する必要があります。 それ以外の場合、クライアント層で実行されたすべてのアクセス許可アサートは、サーバー層で実行されるメソッドにより無視されます。 このため、サーバー キーワードはコード例のメソッド宣言に含まれています。 メソッドのサーバー キーワードは、クラスで指定された RunOn プロパティ値よりも優先されます。

```xpp
server
    static public void RunOnServerPermissionTest()
{
    Set permissionSet;
    str fileName = @"C:\TestFile75a.txt";
    boolean boolFileDeleted;
```

```xpp
    permissionSet =  new Set(Types::Class);
    permissionSet.add(new FileIoPermission(fileName,'rw'));
```

```xpp
    CodeAccessPermission::assertMultiple(permissionSet);
    //--- Permissions are set, now perform file operations.
```

```xpp
    WinAPIServer::createFile(fileName);
    boolFileDeleted = WinAPI::deleteFile(fileName);
```

```xpp
    if (boolFileDeleted)
    {
        info("The file was deleted. Good.");
    }
    else
    {
        error("The file was not deleted. Error.");
    }
}
```

