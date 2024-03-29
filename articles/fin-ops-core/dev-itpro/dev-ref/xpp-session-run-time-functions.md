---
title: X++ セッション ランタイム関数
description: この記事では、セッション ランタイム関数について説明します。
author: josaw1
ms.date: 06/20/2017
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b92154d170155231bbbf4c80334a5f6ee802eca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271267"
---
# <a name="x-session-runtime-functions"></a>X++ セッション ランタイム関数

[!include [banner](../includes/banner.md)]

この記事では、セッション ランタイム関数について説明します。

## <a name="curext"></a>curExt

現在の会社に使用できる拡張を取得します。

```xpp
str curExt()
```

### <a name="return-value"></a>戻り値

現在の会社の内線電話番号。

### <a name="example"></a>例

```xpp
static void curExtExample(Args _arg)
{
    str s;
    // Sets s to the extension of the current company.
    s = curExt();
    print "Current extension is " + s;
}
```

## <a name="curuserid"></a>curUserId
現在のユーザーを表す数値以外の ID を取得します。

```xpp
str curUserId()
```

### <a name="return-value"></a>戻り値

現在のユーザーを表す数値以外の ID を取得します。

### <a name="example"></a>例

```xpp
static void curUserIdExample(Args _arg)
{
    str s;
    s = curUserId();
    print "Current user ID is " + s;
}
```

## <a name="funcname"></a>funcName
現在の関数コンテキストを含む文字列を取得します。

```xpp
str funcName()
```

### <a name="return-value"></a>戻り値

このメソッドを実行しているメソッドの名前。

### <a name="remarks"></a>備考

実行がテーブルまたはクラス メンバー内に現在ある場合は、メソッドの名前に、そのテーブルまたはクラスの名前が付けられます。

### <a name="example"></a>例

```xpp
static void funcNameExample(Args _arg)
{
    print "Current function context is " + funcName();
}
```

## <a name="getcurrentpartition"></a>getCurrentPartition
現在のパーティションの短い名前を取得します。

```xpp
str getCurrentPartition()
```

### <a name="return-value"></a>戻り値

現在のパーティションの短い名前。

### <a name="remarks"></a>備考

返されるデータ パーティション名の最大の長さは 8 文字です。

### <a name="example"></a>例

次のコード例は、X++ 言語の **getCurrentPartition** 関数、および関連する関数またはメソッドへの呼び出しおよび出力を示しています。

```xpp
static public void Main(Args _args)  // X++ method.
{
    int64 iPartition;
    str sPartition;
    SelectableDataArea oSelectableDataArea;  // System ExDT.
    iPartition = getCurrentPartitionRecId();
    sPartition = getcurrentpartition();
    oSelectableDataArea = Global::getCompany( tableNum(BankAccountTable) );
    Global::info( strFmt(
            "getCurrentPartitionRecId =%1 , getCurrentPartition =%2 , getCompany =%3",
            iPartition, sPartition, oSelectableDataArea) );
}
/**** Pasted from Infolog window:
Message_@SYS14327 (03:42:38 pm)
getCurrentPartitionRecId =5637144576 , getCurrentPartition =initial , getCompany =ceu
****/
```

## <a name="getcurrentpartitionrecid"></a>getCurrentPartitionRecId
現在のパーティションの **RecId** フィールドを取得します。

```xpp
int64 getCurrentPartitionRecId()
```

### <a name="return-value"></a>戻り値

現在のデータ パーティションの **RecId** フィールド。

### <a name="remarks"></a>備考

**getCurrentPartitionRecId** 関数に依存するコード例を参照するには、[[パーティションのフィルターを直接 Transact-SQL に含める方法](/dynamicsax-2012/developer/how-to-include-a-filter-for-partition-in-direct-transact-sql)] を参照してください。

### <a name="example"></a>例

次のコード例は、X++ 言語の **getCurrentPartitionRecId** 関数、および関連する関数またはメソッドへの呼び出しおよび出力を示しています。

```xpp
static public void Main(Args _args)  // X++ method.
{
    int64 iPartition;
    str sPartition;
    SelectableDataArea oSelectableDataArea;  // System ExDT.
    iPartition = getCurrentPartitionRecId();
    sPartition = getcurrentpartition();
    oSelectableDataArea = Global::getCompany( tableNum(BankAccountTable) );
    Global::info( strFmt(
            "getCurrentPartitionRecId =%1 , getCurrentPartition =%2 , getCompany =%3",
            iPartition, sPartition, oSelectableDataArea) );
}
/**** Pasted from Infolog window:
Message_@SYS14327 (03:42:38 pm)
getCurrentPartitionRecId =5637144576 , getCurrentPartition =initial , getCompany =ceu
****/
```

## <a name="getprefix"></a>getPrefix
**setPrefix** 関数が連続して呼び出された後、現在の実行接頭辞を取得します。

```xpp
str getPrefix()
```

### <a name="return-value"></a>戻り値

現在の実行接頭語。

### <a name="remarks"></a>備考

接頭語メカニズムを使用すると、アプリケーションが実行したトランザクションについての正確なエラー メッセージの書き込みがより簡単になります。 情報ログでは階層表示が作成されるため、各エラーの原因を特定するのが容易になります。

### <a name="example"></a>例

```xpp
static void getPrefixExample(Args _arg)
{
    setPrefix("Prefix");
    setPrefix("Another prefix");
    print getPrefix();
}
```

## <a name="sessionid"></a>sessionId
現在のセッションのセッション番号を取得します。

```xpp
int sessionId()
```

### <a name="return-value"></a>戻り値

現在のセッションの数値 ID。

### <a name="remarks"></a>備考

セッション番号は、クライアントの起動時に割り当てられ、Application Object Server (AOS) に接続します。 クライアントの存続中にこの関数を呼び出すたびに、同じ整数値が戻されます。 返された値は、**SessionID** 拡張データ型と互換性があります。 **contains** メソッドは、個々のユーザー セッションに関する情報を返します。

### <a name="example"></a>例

```xpp
static void sessionIdExample(Args _arg)
{
    int session;
    session = sessionId();
    print "This session ID is number " + int2Str(session);
}
```

## <a name="prmisdefault"></a>prmIsDefault
現在のメソッドの指定されたパラメータに既定値があるかどうかを判定します。

```xpp
int prmIsDefault(anytype argument)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明            |
|-----------|------------------------|
| 引数  | テストするパラメータ。 |

### <a name="return-value"></a>戻り値

パラメータの既定値が使用された場合 **1**、それ以外の場合は、**0** (ゼロ)。

### <a name="example"></a>例

```xpp
static void prmIsDefaultExample(Args _arg)
{
    void fn(boolean b = true, int j = 42)
    {
        if (prmIsDefault(b) == 1)
        {
            print "First parameter is using the default value.";
        }
        else
        {
            print "First parameter is not using the default value.";
        }
    }
    fn();
    fn(false);
}
```

## <a name="runas"></a>runAs
別のユーザーのセキュリティ コンテキストで、X++ メソッドを実行する呼び出し元を有効にします。 この関数は、バッチ処理で最もよく使用されます。

```xpp
container runAs(
    str userId,
    int classId,
    str staticMethodName
    [,
    container params,
    str company,
    str language,
    str partition
    ])
```

### <a name="parameters"></a>パラメーター

| パラメーター        | 説明                                                                                       |
|------------------|---------------------------------------------------------------------------------------------------|
| userId           | 偽装するユーザー。                                                                          |
| classId          | 偽装セッションで呼び出すクラス。                                                  |
| staticMethodName | 新しいユーザー コンテキストで呼び出すクラス メソッド。                                               |
| params           | メソッドに渡すパラメーター (省略可能)。                                                   |
| 会社          | 偽装セッション用に選択された会社 (オプション)。                              |
| 言語         | 偽装セッション用に選択された言語 (オプション)。                             |
| パーティション        | **getCurrentPartition** 関数によって返されるタイプのパーティション キー。省略可能です。 |

### <a name="return-value"></a>戻り値

任意の値が返された場合に、**runAs** 関数によって呼び出されるメソッドの戻り値または値を保持するコンテナーです。

### <a name="remarks"></a>備考

この関数を使用すると、別のユーザーとしてコードを実行できます。 この機能はセキュリティ上の脅威です。 したがって、この関数は、[コード アクセス セキュリティ](/dynamicsax-2012/developer/code-access-security)で実行されます。 サーバー上でこの関数を呼び出すには、**RunAsPermission** クラスからのアクセス許可が必要です。 このアプリケーション プログラミング インターフェイス (API) を使用するたびに、脅威なモデル化とする必要があります。 セキュリティの脆弱性が見つかった場合は、この API への入力を検証します。 デバッガーは、**runAs** 関数を使用して呼び出されるメソッドにあるブレークポイントを無視することがあります。 **runAs** 関数として実行される X++ コードは、Microsoft .NET Framework の共通中間言語 (CIL) として実行する必要があります。 CIL が対象となる静的メソッドに対して生成されていない場合、メソッドが見つからないことを示すエラーメッセージが表示されます。 **PartitionKey** システムの型は、*partition* パラメーターの正確な型です。 **PartitionKey** は最大長が 8 文字の文字列です。

### <a name="example"></a>例

次の例では、**EventJobDueDate** クラスの **runDueDateEventsForUser** メソッドを呼び出します。 このコードは、ユーザーのセキュリティ コンテキストで実行されます。 新しいクラスのメソッドに適用することによって、このコードを実行します。

```xpp
server static public void Main(Args _args)
{
    RunAsPermission perm;
    UserId runAsUser;
    SysUserInfo userInfo;
    userInfo = SysUserInfo::find();
    runAsUser = userInfo.Id;
    perm = new RunAsPermission(runAsUser);
    perm.assert();
    runAs(runAsUser, classnum(EventJobDueDate), "runDueDateEventsForUser");
    CodeAccessPermission::revertAssert();
}
```

## <a name="setprefix"></a>setPrefix
現在の実行スコープの接頭語を設定します。

```xpp
int setPrefix(str _prefix)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                 |
|-----------|---------------------------------------------|
| \_接頭語  | 現在の実行スコープの接頭語。 |

### <a name="return-value"></a>戻り値

**0** 接頭語が正常に設定された場合。

### <a name="remarks"></a>備考

**getPrefix** 関数を使用すると、実行の完全な接頭辞を取得できます。 スコープが残っているときは、接頭語が前のレベルに自動的にリセットされます。 接頭語メカニズムを使用すると、アプリケーションが実行したトランザクションについての正確なエラー メッセージの書き込みがより簡単になります。 たとえば、**AA** メソッドは **BB** メソッドを呼び出し、各メソッドは **setPrefix** 機能を呼び出します。 **BB** メソッドが情報ログに書き込んだメッセージは、階層内で入れ子になって表示されます。 **BB** メソッドが終了し、コントロールが **AA** メソッドに戻ると、**BB** メソッドによって設定された接頭語は後続のメッセージには関連付けられません。

### <a name="example"></a>例

```xpp
static void setPrefixExample(Args _arg)
{
    int i;
    i = setPrefix("Prefix");
    print i;
}
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
