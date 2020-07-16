---
title: FileIOPermission クラス
description: このトピックでは、FileIOPermission クラスについて説明します。
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
ms.openlocfilehash: 4fea939d775183fc3948bbe4cbc9ef4487006f17
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502979"
---
# <a name="class-fileiopermission"></a>クラス FileIOPermission

[!include [banner](../../includes/banner.md)]

```xpp
class FileIOPermission extends CodeAccessPermission
```

FileIOPermission クラスは、ファイルおよびフォルダーへのアクセス機能を制御します。

## <a name="remarks"></a>備考

FileIoPermission クラスは、特定の API のアクセス許可をチェックするように設計されています。 アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。 保護された API を実行する前に、対応する CodeAccessPermission:: demand メソッドが呼び出されている同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド

## <a name="examples"></a>例

次のコード例は、File.txt ファイルの読み取りアクセス許可を指定する FileIoPermission クラスの新しいインスタンスを示しています。 assert メソッドが呼び出され、コードが AsciiIo.new メソッドを呼び出すことができることが宣言されます。

```xpp
server static void main(Args args) 
{ 
    FileIoPermission _perm; 
    AsciiIo a; 
    _perm = new FileIoPermission("c:\\File.txt",'r'); 
    _perm.assert(); 
    // Invoke the protected API. 
    a = new AsciiIo("c:\\File.txt",'r'); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | 現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。               |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が指定されたアクセス許可のサブセットかどうかを決定します。 |
| public void new(str filename, str mode)                | CodeAccessPermission クラスの新しいインスタンスを初期化します。                    |

## <a name="method-copy"></a>メソッド copy

現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

現在のアクセス許可オブジェクトのコピーです。

### <a name="remarks---copy"></a>備考 - copy

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「コピー」を参照してください。

## <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が指定されたアクセス許可のサブセットかどうかを決定します。

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a>パラメーター - isSubsetOf

target  
CodeAccessPermission クラス オブジェクト。

### <a name="return-value---issubsetof"></a>戻り値 - isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

### <a name="remarks---issubsetof"></a>備考 - isSubsetOf

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「M: CodeAccessPermission.isSubsetOf」を参照してください。

## <a name="method-new"></a>メソッド new

CodeAccessPermission クラスの新しいインスタンスを初期化します。

```xpp
public void new(str filename, str mode)
```

### <a name="parameters---new"></a>パラメーター - new

filename  
アクセスのタイプを指定する文字列データ型。

<!-- -->

モード  
アクセスのタイプを指定する文字列データ型。

### <a name="remarks---new"></a>備考 - new

次のテーブルに、\_mode パラメーターの使用可能な値を示します。

|     |                |
|-----|----------------|
| R   | 既読           |
| W   | 書き込み          |
| RW  | 読み取りと書き込み |

### <a name="examples---new"></a>例 - new

次のコード例は、File.txt ファイルの読み取りアクセス許可を指定する FileIoPermission クラスの新しいインスタンスを示しています。

```xpp
server static void main(Args args) 
{ 
    FileIoPermission _perm; 
    _perm = new FileIoPermission("c:\\File.txt",'r'); 
}
```

