---
title: RunAsPermission クラス
description: このトピックでは、RunAsPermission クラスについて説明します。
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
ms.openlocfilehash: 1272adb7eafda535d1b60fc54cdcb673703d58c7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502821"
---
# <a name="class-runaspermission"></a>クラス RunAsPermission

[!include [banner](../../includes/banner.md)]

```xpp
class RunAsPermission extends CodeAccessPermission
```

RunAsPermssion クラスは、別のユーザーのセキュリティ コンテキストでコードの実行を制御します。

## <a name="remarks"></a>備考

保護された API が実行される前に、対応する CodeAccessPermission.demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します。RunAsPermission クラスは、runAs 関数のアクセス許可をチェックするように設計されています。 アクセス許可によって保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。

-   サーバー静的メソッド �または�
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド

## <a name="examples"></a>例

次のコード例は、RunAsPermission クラスの新しいインスタンスを示しています。 assert メソッドが呼び出され、コードが runAs 関数を呼び出して、別のユーザーのセキュリティ コンテキストで EventJobDueDate.:runDueDateEventsForUser メソッドを実行できることが宣言されます。

```xpp
server static void main(Args args) 
{ 
    RunAsPermission _perm; 
    UserId          _runAsUser; 
    SysUserInfo     _userInfo; 
    _userInfo = SysUserInfo::find(); 
    _runAsUser = _userInfo.Id; 
    _perm = new RunAsPermission(_runAsUser); 
    _perm.assert(); 
    // Invoke the protected API. 
    RunAs(_runAsUser, classnum(EventJobDueDate), "runDueDateEventsForUser"); 
    // Optionally, call revertAssert() to limit the scope of assert. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | アクセス許可クラス オブジェクトのコピーを作成し、返します。                                                            |
| public boolean isSubsetOf(CodeAccessPermission target) | 派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。 |
| public void new(UserId userId)                         | CodeAccessPermission クラスの新しいインスタンスを初期化します。                                                       |

## <a name="method-copy"></a>メソッド copy

アクセス許可クラス オブジェクトのコピーを作成し、返します。

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

現在の派生クラスオブジェクトのコピーです。

### <a name="remarks---copy"></a>備考 - copy

API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。

## <a name="method-issubsetof"></a>メソッド isSubsetOf

派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。

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

## <a name="method-new"></a>メソッド new

CodeAccessPermission クラスの新しいインスタンスを初期化します。

```xpp
public void new(UserId userId)
```

### <a name="parameters---new"></a>パラメーター - new

userId  
ユーザーを指定する userId システム データ型。

### <a name="examples---new"></a>例 - new

次の例は、RunAsPermission クラスの新しいインスタンスを示しています。 SysUserInfo テーブルは、userId パラメーターの初期化に使用されます。

```xpp
server static void main(Args args) 
{ 
    RunAsPermission _perm; 
    UserId          _userId; 
    SysUserInfo     _userInfo; 
    _userInfo = SysUserInfo::find(); 
    _userId = _userInfo.Id; 
    _perm = new RunAsPermission(_userId); 
```

```xpp
}
```

### <a name="remarks---new"></a>備考 - new

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

## <a name="method-rightmargin"></a>メソッド rightMargin

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a>パラメーター - rightMargin

値  

<!-- -->

単位  

## <a name="method-left"></a>メソッド left

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a>パラメーター - left

値  

<!-- -->

単位  

## <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a>パラメーター - width

値  

<!-- -->

単位  

### <a name="remarks---width"></a>備考 - width

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

## <a name="method-extrasumwidth"></a>メソッド extraSumWidth

```xpp
public void extraSumWidth(Real value, Units unit)
```

### <a name="parameters---extrasumwidth"></a>パラメーター - extraSumWidth

値  

<!-- -->

単位  

## <a name="method-topmargin"></a>メソッド topMargin

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a>パラメーター - topMargin

値  

<!-- -->

単位  

## <a name="method-leftmargin"></a>メソッド leftMargin

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a>パラメーター - leftMargin

値  

<!-- -->

単位  

## <a name="method-labelwidth"></a>メソッド labelWidth

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a>パラメーター - labelWidth

値  

<!-- -->

単位  

## <a name="method-top"></a>メソッド top

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a>パラメーター - top

値  

<!-- -->

単位  

## <a name="method-bottommargin"></a>メソッド bottomMargin

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a>パラメーター - bottomMargin

値  

<!-- -->

単位  

