---
title: xSession クラス
description: このトピックでは、xSession クラスについて説明します。
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
ms.openlocfilehash: ffdd600d428b7bf29d436b6af16ada461816b288
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502760"
---
# <a name="class-xsession"></a>クラス xSession

[!include [banner](../../includes/banner.md)]

```xpp
class xSession extends Object
```

セッションに関する情報を取得します。

## <a name="remarks"></a>備考

現在のセッションに関する情報を取得するには、パラメーターを指定せずに新しい xSession セッションを作成します。 すべてのアクティブなセッション (AOS のみ) に関する情報を取得する唯一の方法は、セッション ID 1 から xSession.maxSessionId に移動することです。 ID は、永続的な一覧ではなく、maxSessionId メソッドで指定したセッションの最大数を超えることはありません。

## <a name="examples"></a>例

次の例では、新しい xSession オブジェクトを作成し、それを使用して現在のセッションのサーバー名を検索します。

```xpp
xSession xSession; 
xSession = new xSession();   
// Prints the name of server for the current session. 
print xSession.AOSName();
```

## <a name="methods"></a>メソッド

| 方法                                                                            | 説明                                                                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| public str AOSName()                                                              | セッションの処理を担当する Application Object Server (AOS) の名前を取得します。                       |
| public str clientComputerName()                                                   | セッションの処理を担当するクライアント コンピューターのネットワーク名を取得します。                               |
| public ClientType clientKind()                                                    | セッションの処理を担当するクライアントの種類を取得します。                                                |
| public str databaseSpid()                                                         | 有効な接続 ID のコンマ区切りのリストを取得します。                                                                     |
| public str documentationLanguage()                                                | セッションに表示されるドキュメントの言語 ID を取得します。                                                  |
| public str interfaceLanguage()                                                    | セッションのメニューとダイアログで使用される言語の ID を取得します。                                           |
| public boolean isWorkerThread()                                                   | セッションがワーカー スレッドかどうかを判定します。                                                                             |
| public Date loginDate()                                                           | セッションのユーザーがログオンした日付を取得します。                                                                 |
| public DateTime loginDateTime()                                                   |                                                                                                                                |
| public TimeOfDay loginTime()                                                      | セッションのユーザーがログオンした時刻を取得します。                                                                 |
| public int masterSessionId()                                                      | xSession オブジェクトの対象となるセッションのマスター セッション ID を取得します。                                               |
| public int serverId()                                                             |                                                                                                                                |
| public int sessionId()                                                            | xSession オブジェクトの対象となるセッションのセッション ID を取得します。                                                       |
| public boolean terminate(\[Date loginDate\], \[TimeOfDay loginTime\])             | オブジェクトのインスタンス化に使用されたセッション ID を終了します。                                                               |
| public UserId userId()                                                            | このセッションがログオンしているユーザー ID を取得します。                                                                     |
| ::public static int currentRetryCount()                                           | デッドロック、更新の競合、または別の例外の後に try ブロックが再試行された回数をカウントします。            |
| ::public static Uncheck currentUnCheck()                                          |                                                                                                                                |
| ::public static str getDbSchema()                                                 | セッションのデータベース オブジェクト名のスキーマ部分を取得します。                                                         |
| ::public static COM getIISObject(IISObject object)                                | IIS オブジェクトの COM オブジェクトのインスタンスを作成して返します。                                                                       |
| ::public static boolean getSysTraceActive()                                       | セッションでシステム トレースを有効にするかどうかを決定できます。                                                  |
| ::public static str getXRefAssembyTempFolder()                                    |                                                                                                                                |
| ::public static boolean isCLRSession()                                            |                                                                                                                                |
| ::public static boolean isUserPreferredTzSameAsLocalMachine()                     |                                                                                                                                |
| ::public static int lastDuplicateKeyViolatingTable()                              |                                                                                                                                |
| ::public static int lastUpdateConflictingTable()                                  | 最後に更新の競合をしたテーブルのインスタンスを取得します。                                                  |
| ::public static int maxSessionId()                                                | 現在のライセンス コードで許可されているセッションの最大数を取得します。                                      |
| ::public static int numSession()                                                  | 登録されているセッションの現在の番号を取得します。                                                                           |
| public PreferredLocale preferredLocale()                                          |                                                                                                                                |
| ::public static int pseudoBandwidth(\[int bandwidth\])                            | セッションの帯域幅シミュレーションをオンにするかどうかを決定し、帯域幅シミュレーションをオンまたはオフにします。 |
| ::public static int pseudoLatency(\[int latency\])                                | セッションの待機シミュレーションをオンにするかどうかを決定し、待機シミュレーションをオンまたはオフにします。     |
| ::public static int pseudoSimMode(\[int simMode\])                                | セッションの遅延シミュレーションをオンにするかどうかを決定し、遅延シミュレーションをオンまたはオフにします。         |
| ::public static int systemSessionId()                                             | xSession オブジェクトの対象となるセッションのシステム セッション ID を取得します。                                               |
| ::public static container xppCallStack()                                          | 現在の呼び出し履歴を取得します。                                                                                              |
| ::public static void removeAOC()                                                  | 現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を削除します。                                         |
| ::public static void updateAOC()                                                  | 現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を更新します。                                         |
| ::public static void setAutoUpdateRecVersion(boolean autoUpdateRecVersion)        |                                                                                                                                |
| ::public static void setSysTraceActive(boolean nValue)                            | システム追跡のオンまたはオフを切り替えます。                                                                                             |
| ::private static void clientSetAutoUpdateRecVersion(boolean autoUpdateRecVersion) |                                                                                                                                |
| ::private static void serverSetAutoUpdateRecVersion(boolean autoUpdateRecVersion) |                                                                                                                                |
| public void new(\[int sessionId\], \[boolean checkSession\])                      | 現在のセッションまたはパラメーターとして渡されたセッション ID のいずれかに対して xSession オブジェクトのインスタンスを作成します。                   |
| ::public static void reloadTableCollectionOnClient()                              |                                                                                                                                |

## <a name="method-aosname"></a>メソッド AOSName

セッションの処理を担当する Application Object Server (AOS) の名前を取得します。

```xpp
public str AOSName()
```

### <a name="return-value---aosname"></a>戻り値 - AOSName

AOS の名前を示す文字列。

### <a name="remarks---aosname"></a>備考 - AOSName

AOS 以外の接続されているクライアントについては、このメソッドは空の文字列を返します。

### <a name="examples---aosname"></a>例 - AOSName

次の例は、現在のセッションを実行している AOS の名前を表示します。

```xpp
xSession xSession; 
xSession = new xSession(); 
// Prints the name of server for the current session. 
print xSession.AOSName();
```

## <a name="method-clientcomputername"></a>メソッド clientComputerName

セッションの処理を担当するクライアント コンピューターのネットワーク名を取得します。

```xpp
public str clientComputerName()
```

### <a name="return-value---clientcomputername"></a>戻り値 - clientComputerName

クライアント コンピューターの名前を示す文字列。

### <a name="examples---clientcomputername"></a>例 - clientComputerName

次の例は、現在のセッションを実行しているクライアントの名前を表示します。

```xpp
{ 
    xSession xSession; 
    xSession = new xSession(); 
    print xSession.clientComputerName(); 
    pause; 
}
```

## <a name="method-clientkind"></a>メソッド clientKind

セッションの処理を担当するクライアントの種類を取得します。

```xpp
public ClientType clientKind()
```

### <a name="return-value---clientkind"></a>戻り値 - clientKind

クライアントのタイプ。

### <a name="remarks---clientkind"></a>備考 - clientKind

可能な値は、ClientType システム列挙の値です。

-   COMObject
-   クライアント
-   サーバー
-   WorkerThread

### <a name="examples---clientkind"></a>例 - clientKind

次の例は、現在のセッションを実行しているクライアントのタイプを表示します。

```xpp
{ 
    xSession xSession; 
    xSession = new xSession(); 
    print xSession.clientKind(); 
    pause; 
}
```

## <a name="method-databasespid"></a>メソッド databaseSpid

有効な接続 ID のコンマ区切りのリストを取得します。

```xpp
public str databaseSpid()
```

### <a name="return-value---databasespid"></a>戻り値 - databaseSpid

有効な接続 ID のコンマ区切りのリスト。

### <a name="remarks---databasespid"></a>備考 - databaseSpid

このメソッドは、オンライン ユーザー フォーム (SysUsersOnline) を作成するために使用されます。 有効な接続の数を取得するには、xSession::numSession を使用します。

## <a name="method-documentationlanguage"></a>メソッド documentationLanguage

セッションに表示されるドキュメントの言語 ID を取得します。

```xpp
public str documentationLanguage()
```

### <a name="return-value---documentationlanguage"></a>戻り値 - documentationLanguage

セッションのドキュメントに使用される言語の ID を含む文字列。

### <a name="remarks---documentationlanguage"></a>備考 - documentationLanguage

たとえば、このメソッドは、言語が英語 (US) に設定されている場合「en-us」を返します。 ドキュメントの言語は個別に選択することができ、メニューやダイアログで使用される言語と必ずしも同一ではありません。 メニューやダイアログ ボックスの言語 ID を取得するには、xSession.interfaceLanguage を使用します。 xInfo.documentationLanguage を使用すると、ドキュメントの言語を設定することができます。

## <a name="method-interfacelanguage"></a>メソッド interfaceLanguage

セッションのメニューとダイアログで使用される言語の ID を取得します。

```xpp
public str interfaceLanguage()
```

### <a name="return-value---interfacelanguage"></a>戻り値 - interfaceLanguage

セッションのメニューとダイアログで使用される言語の ID を含む文字列。

### <a name="remarks---interfacelanguage"></a>備考 - interfaceLanguage

たとえば、このメソッドは、言語が英語 (US) に設定されている場合「en-us」を返します。 ドキュメントの言語は個別に選択することができ、メニューやダイアログで使用される言語と必ずしも同一ではありません。 ドキュメントの言語 ID を取得するには、次を使用します。

## <a name="method-isworkerthread"></a>メソッド isWorkerThread

セッションがワーカー スレッドかどうかを判定します。

```xpp
public boolean isWorkerThread()
```

### <a name="return-value---isworkerthread"></a>戻り値 - isWorkerThread

セッションがワーカー スレッドである場合は true。それ以外の場合は、false。

### <a name="remarks---isworkerthread"></a>備考 - isWorkerThread

ワーカー スレッドは、Thread クラスのインスタンスで、UI がない新しいインスタンスを作成します。 このメソッドがこのようなセッション内で呼び出される場合は true が返されます。

## <a name="method-logindate"></a>メソッド loginDate

セッションのユーザーがログオンした日付を取得します。

```xpp
public Date loginDate()
```

### <a name="return-value---logindate"></a>戻り値 - loginDate

セッションのユーザーがログオンした日付。

## <a name="method-logindatetime"></a>メソッド loginDateTime

```xpp
public DateTime loginDateTime()
```

### <a name="return-value---logindatetime"></a>戻り値 - loginDateTime

## <a name="method-logintime"></a>メソッド loginTime

セッションのユーザーがログオンした時刻を取得します。

```xpp
public TimeOfDay loginTime()
```

### <a name="return-value---logintime"></a>戻り値 - loginTime

セッションのユーザーがログオンした時間。

## <a name="method-mastersessionid"></a>メソッド masterSessionId

xSession オブジェクトの対象となるセッションのマスター セッション ID を取得します。

```xpp
public int masterSessionId()
```

### <a name="return-value---mastersessionid"></a>戻り値 - masterSessionId

セッション ID を表す整数。

### <a name="remarks---mastersessionid"></a>備考 - masterSessionId

一部のセッションには、COM セッションまたはワーカー スレッド セッションなどのマスター セッション ID があります。

### <a name="examples---mastersessionid"></a>例 - masterSessionId

次の例では、通常のセッション ID (または存在する場合は､マスター セッション ID) を使用して xSession オブジェクトを作成します。

```xpp
static xSession getThisSession() 
{ 
    xSession xSession = new xSession(sessionid()); 
    if (xSession.masterSessionId()) 
    { 
        xSession = new xSession(xSession.masterSessionId()); 
    } 
    return xSession; 
}
```

## <a name="method-serverid"></a>メソッド serverId

```xpp
public int serverId()
```

### <a name="return-value---serverid"></a>戻り値 - serverId

## <a name="method-sessionid"></a>メソッド sessionId

xSession オブジェクトの対象となるセッションのセッション ID を取得します。

```xpp
public int sessionId()
```

### <a name="return-value---sessionid"></a>戻り値 - sessionId

セッション ID を表す整数。

## <a name="method-terminate"></a>メソッド terminate

オブジェクトのインスタンス化に使用されたセッション ID を終了します。

```xpp
public boolean terminate([Date loginDate], [TimeOfDay loginTime])
```

### <a name="parameters---terminate"></a>パラメーター - terminate

loginDate  
セッションのユーザーがログオンした時間 (オプション)。

<!-- -->

loginTime  
セッションのユーザーがログオンした時間 (オプション)。

### <a name="return-value---terminate"></a>戻り値 - terminate

ユーザーにこの関数を実行する権限がない場合は false; それ以外の場合は true。

### <a name="remarks---terminate"></a>備考 - terminate

この API には、実行時に呼び出される組み込み認証チェックがあります。 終了メソッドの呼び出しが開発セキュリティ キー (SysDevelopment) のアクセス権のないユーザーによって行われた場合はスローされます。 オプションのパラメーターを使用すると、セッションにタイムスタンプを設定して、終了する予定のセッションであることを確認できます。 同じセッション ID を 2 つの異なる時間に使用することができます。 terminate メソッドは、オンライン ユーザー フォームで管理者がセッションを終了できるようにするために使用されます。 管理者はセッションが応答を停止した場合や、多くのリソースを消費した場合、または別のユーザーのためにライセンスを解放する必要がある場合にセッションを終了させることがあります。

### <a name="examples---terminate"></a>例 - terminate

次の例では、ユーザーにセッションを終了する権限があるかどうかを確認します。 その場合は、セッションが終了します。

```xpp
server static public void Main(Args _args) 
{ 
    Session session; 
    session = new Session(); 
    if (session) 
    { 
        session.terminate(); 
    } 
}
```

## <a name="method-userid"></a>メソッド userId

このセッションがログオンしているユーザー ID を取得します。

```xpp
public UserId userId()
```

### <a name="return-value---userid"></a>戻り値 - userId

セッションのユーザーの ID です。

### <a name="examples---userid"></a>例 - userId

次の例では、特定のユーザーがオンラインかどうかを判断します。

```xpp
server static boolean isUserOnline(userId userId) 
{ 
    xSession    session; 
    int counter; 
    int maxSessions = Info::licensedUsersTotal(); 
    if (!userId) 
    { 
        return false; 
    } 
    for(counter = 1; counter < maxSessions;counter++) 
    { 
        session = new xSession(counter, true); 
        if(session && session.userId() == userId) 
        { 
            return true; 
        } 
    } 
    return false; 
}
```

## <a name="method-currentretrycount"></a>メソッド currentRetryCount

デッドロック、更新の競合、または別の例外の後に try ブロックが再試行された回数をカウントします。

```xpp
public static int currentRetryCount()
```

### <a name="return-value---currentretrycount"></a>戻り値 - currentRetryCount

try ブロックが再試行された回数。

### <a name="examples---currentretrycount"></a>例 - currentRetryCount

次の例では、currentRetryCount メソッドを使用して、トランザクションが CUD トランザクションの例外処理を判断するために再試行された回数をテストします。

```xpp
catch (Exception::UpdateConflict) 
    { 
        if (appl.ttsLevel() == 0) 
        { 
            if (xSession::currentRetryCount() >= #RetryNum) 
            { 
                throw Exception::UpdateConflictNotRecovered; 
            } 
            else 
            { 
                retry; 
            } 
        } 
        else 
        { 
            throw Exception::UpdateConflict; 
        } 
    }
```

## <a name="method-currentuncheck"></a>メソッド currentUnCheck

```xpp
public static Uncheck currentUnCheck()
```

### <a name="return-value---currentuncheck"></a>戻り値 - currentUnCheck

## <a name="method-getdbschema"></a>メソッド getDbSchema

セッションのデータベース オブジェクト名のスキーマ部分を取得します。

```xpp
public static str getDbSchema()
```

### <a name="return-value---getdbschema"></a>戻り値 - getDbSchema

データベース オブジェクト名のスキーマ部分を返します。

## <a name="method-getiisobject"></a>メソッド getIISObject

IIS オブジェクトの COM オブジェクトのインスタンスを作成して返します。

```xpp
public static COM getIISObject(IISObject object)
```

### <a name="parameters---getiisobject"></a>パラメーター - getIISObject

オブジェクト  
COM オブジェクトを作成する IIS オブジェクト。

### <a name="return-value---getiisobject"></a>戻り値 - getIISObject

COM オブジェクト。

### <a name="remarks---getiisobject"></a>備考 - getIISObject

IIS オブジェクトは、IISObject システム列挙によって提供される使用可能な値のいずれかにすることができます。

-   ApplicationObject
-   要求
-   応答
-   サーバー
-   SessionObject

## <a name="method-getsystraceactive"></a>メソッド getSysTraceActive

セッションでシステム トレースを有効にするかどうかを決定できます。

```xpp
public static boolean getSysTraceActive()
```

### <a name="return-value---getsystraceactive"></a>戻り値 - getSysTraceActive

システム トレースが有効な場合は true。それ以外の場合は、false。

### <a name="remarks---getsystraceactive"></a>備考 - getSysTraceActive

システム トレースを有効にするには、xSession::setSysTraceActive を使用します。

### <a name="examples---getsystraceactive"></a>例 - getSysTraceActive

次の例では、getSysTraceActive メソッドを使用してシステム トレースの元の設定を判断し、トレースを一時的に false に設定した後に設定をリセットします。

```xpp
server static void main(Args a) 
{ 
    SysDataImport sysDataImport; 
    boolean       sysTraceActive = xSession::getSysTraceActive(); 
    sysDataImport = SysDataImport::newTmpFilename(''); 
    sysDataImport.addTmpExpImpTable( 
        tablenum(SysTraceTableSQL), 
        false); 
    sysDataImport.addTmpExpImpTable( 
        tablenum(SysTraceTableSQLExecPlan), 
        false); 
    sysDataImport.addTmpExpImpTable( 
        tablenum(SysTraceTableSQLTabRef), 
        false); 
    xSession::setSysTraceActive(FALSE); 
    if (sysDataImport.prompt()) 
        sysDataImport.run(); 
    xSession::setSysTraceActive(sysTraceActive); 
}
```

## <a name="method-getxrefassembytempfolder"></a>メソッド getXRefAssembyTempFolder

```xpp
public static str getXRefAssembyTempFolder()
```

### <a name="return-value---getxrefassembytempfolder"></a>戻り値 - getXRefAssembyTempFolder

## <a name="method-isclrsession"></a>メソッド isCLRSession

```xpp
public static boolean isCLRSession()
```

### <a name="return-value---isclrsession"></a>戻り値 - isCLRSession

## <a name="method-isuserpreferredtzsameaslocalmachine"></a>メソッド isUserPreferredTzSameAsLocalMachine

```xpp
public static boolean isUserPreferredTzSameAsLocalMachine()
```

### <a name="return-value---isuserpreferredtzsameaslocalmachine"></a>戻り値 - isUserPreferredTzSameAsLocalMachine

## <a name="method-lastduplicatekeyviolatingtable"></a>メソッド lastDuplicateKeyViolatingTable

```xpp
public static int lastDuplicateKeyViolatingTable()
```

### <a name="return-value---lastduplicatekeyviolatingtable"></a>戻り値 - lastDuplicateKeyViolatingTable

## <a name="method-lastupdateconflictingtable"></a>メソッド lastUpdateConflictingTable

最後に更新の競合をしたテーブルのインスタンスを取得します。

```xpp
public static int lastUpdateConflictingTable()
```

### <a name="return-value---lastupdateconflictingtable"></a>戻り値 - lastUpdateConflictingTable

最後に、更新の競合をしたテーブルのインスタンス。

### <a name="examples---lastupdateconflictingtable"></a>例 - lastUpdateConflictingTable

次の例では、lastUpdateConflictingTable メソッドの一般的な使用方法を示しています。これにより、更新の競合が発生しているテーブルに従ってトランザクションを中断または再試行できます。

```xpp
try 
{ 
    // ... 
    table1.update(); 
    // ... 
    table2.update(); 
} 
catch(Exception::UpdateConflict) 
{ 
    if(xSession::lastUpdateConflictingTable() == table1) 
    { 
        ttsabort; 
    } 
    else if(xSession::lastUpdateConflictingTable() == table2) 
    { 
        // Compensate here. 
        // ... 
        retry; 
    } 
}
```

## <a name="method-maxsessionid"></a>メソッド maxSessionId

現在のライセンス コードで許可されているセッションの最大数を取得します。

```xpp
public static int maxSessionId()
```

### <a name="return-value---maxsessionid"></a>戻り値 - maxSessionId

現在のライセンス コードで許可されているセッションの最大数を示す整数。

## <a name="method-numsession"></a>メソッド numSession

登録されているセッションの現在の番号を取得します。

```xpp
public static int numSession()
```

### <a name="return-value---numsession"></a>戻り値 - numSession

現在登録されているセッションの数を示す整数。

## <a name="method-preferredlocale"></a>メソッド preferredLocale

```xpp
public PreferredLocale preferredLocale()
```

### <a name="return-value---preferredlocale"></a>戻り値 - preferredLocale

## <a name="method-pseudobandwidth"></a>メソッド pseudoBandwidth

セッションの帯域幅シミュレーションをオンにするかどうかを決定し、帯域幅シミュレーションをオンまたはオフにします。

```xpp
public static int pseudoBandwidth([int bandwidth])
```

### <a name="parameters---pseudobandwidth"></a>パラメーター - pseudoBandwidth

bandwidth  
帯域幅のシミュレーションのオン/オフを切り替えます。 シミュレーションをオフにするには 0 に設定されます。 その他の値は、シミュレーションをオンにします。

### <a name="return-value---pseudobandwidth"></a>戻り値 - pseudoBandwidth

帯域幅のシミュレーションを有効にするかどうかを示す整数。 戻り値が 0 の場合、帯域幅シミュレーションはありません。

### <a name="remarks---pseudobandwidth"></a>備考 - pseudoBandwidth

システム監視ツールからリモート接続の疑似シミュレーションを実行することができます。

-   ツール バーで、ツールを選択し、開発ツールをポイントし、システム監視をポイントして、リモート接続タブをクリックします。

## <a name="method-pseudolatency"></a>メソッド pseudoLatency

セッションの待機シミュレーションをオンにするかどうかを決定し、待機シミュレーションをオンまたはオフにします。

```xpp
public static int pseudoLatency([int latency])
```

### <a name="parameters---pseudolatency"></a>パラメーター - pseudoLatency

latency  
待機シミュレーションのオン/オフを切り替えます。 シミュレーションをオフにするには 0 に設定されます。 その他の値は、シミュレーションをオンにします。

### <a name="return-value---pseudolatency"></a>戻り値 - pseudoLatency

待機シミュレーションを有効にするかどうかを示す整数。 戻り値が 0 の場合、遅延シミュレーションはありません。

### <a name="remarks---pseudolatency"></a>備考 - pseudoLatency

システム監視ツールからリモート接続の疑似シミュレーションを実行することができます。

-   ツール バーで、ツールを選択し、開発ツールをポイントし、システム監視をポイントして、リモート接続タブをクリックします。

## <a name="method-pseudosimmode"></a>メソッド pseudoSimMode

セッションの遅延シミュレーションをオンにするかどうかを決定し、遅延シミュレーションをオンまたはオフにします。

```xpp
public static int pseudoSimMode([int simMode])
```

### <a name="parameters---pseudosimmode"></a>パラメーター - pseudoSimMode

simMode  
遅延シミュレーションのオン/オフを切り替えます。 シミュレーションをオフにするには 0 に設定されます。 アプリケーションの呼び出しで遅延をシミュレートするには 1 に設定します。 すべての呼び出しで遅延をシミュレートするには 2 に設定します。

### <a name="return-value---pseudosimmode"></a>戻り値 - pseudoSimMode

遅延シミュレーションを有効にするかどうかを示す整数。 戻り値が 0 の場合、遅延シミュレーションはありません。 戻り値が 1 の場合は、遅延はアプリケーション制御の呼び出しに対してのみシミュレートされます。 戻り値が 2 の場合は、遅延はすべての呼び出しに対してシミュレートされます。

### <a name="remarks---pseudosimmode"></a>備考 - pseudoSimMode

システム監視ツールからリモート接続の疑似シミュレーションを実行することができます。

-   ツール バーで、ツールを選択し、開発ツールをポイントし、システム監視をポイントして、リモート接続タブをクリックします。

## <a name="method-systemsessionid"></a>メソッド systemSessionId

xSession オブジェクトの対象となるセッションのシステム セッション ID を取得します。

```xpp
public static int systemSessionId()
```

### <a name="return-value---systemsessionid"></a>戻り値 - systemSessionId

セッション ID を表す整数。

### <a name="remarks---systemsessionid"></a>備考 - systemSessionId

COM セッションまたはワーカー スレッド セッションなどの一部のセッションには、親システム セッションがあります。

## <a name="method-xppcallstack"></a>メソッド xppCallStack

現在の呼び出し履歴を取得します。

```xpp
public static container xppCallStack()
```

### <a name="return-value---xppcallstack"></a>戻り値 - xppCallStack

現在のコール スタックの内容を保持するコンテナーです。

## <a name="method-removeaoc"></a>メソッド removeAOC

現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を削除します。

```xpp
public static void removeAOC()
```

## <a name="method-updateaoc"></a>メソッド updateAOC

現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を更新します。

```xpp
public static void updateAOC()
```

### <a name="remarks---updateaoc"></a>備考 - updateAOC

AOC は、クライアントによってロードされるメタデータで構成されるクライアント側のキャッシュであり、クライアントを閉じると、ディスクに保存されます。 これはユーザーのローカル設定フォルダーで保存されます。 このファイルの拡張子は .auc で、ユーザーのローカル設定フォルダーに保存されます。 クライアントは、起動されると、キャッシュからの読み取りの後、ディスクからそのキャッシュを削除します。

## <a name="method-setautoupdaterecversion"></a>メソッド setAutoUpdateRecVersion

```xpp
public static void setAutoUpdateRecVersion(boolean autoUpdateRecVersion)
```

### <a name="parameters---setautoupdaterecversion"></a>パラメーター - setAutoUpdateRecVersion

autoUpdateRecVersion  

## <a name="method-setsystraceactive"></a>メソッド setSysTraceActive

システム追跡のオンまたはオフを切り替えます。

```xpp
public static void setSysTraceActive(boolean nValue)
```

### <a name="parameters---setsystraceactive"></a>パラメーター - setSysTraceActive

nValue  
追跡をオンまたはオフに切り替える必要があるかどうかを指定するブール値。 追跡をオンにするには、true に設定します。

### <a name="examples---setsystraceactive"></a>例 - setSysTraceActive

次の例では、データのインポート時に setSysTraceActive メソッドを使用してシステム トレースをオフにします。

```xpp
server static void main(Args a) 
{ 
    SysDataImport sysDataImport; 
    boolean       sysTraceActive = xSession::getSysTraceActive(); 
    sysDataImport = SysDataImport::newTmpFilename(''); 
    sysDataImport.addTmpExpImpTable( 
        tablenum(SysTraceTableSQL), 
        false); 
    sysDataImport.addTmpExpImpTable( 
        tablenum(SysTraceTableSQLExecPlan), 
        false); 
    sysDataImport.addTmpExpImpTable( 
        tablenum(SysTraceTableSQLTabRef), 
        false); 
    xSession::setSysTraceActive(FALSE); 
    if (sysDataImport.prompt()) 
        sysDataImport.run(); 
    xSession::setSysTraceActive(sysTraceActive); 
}
```

## <a name="method-clientsetautoupdaterecversion"></a>メソッド clientSetAutoUpdateRecVersion

```xpp
private static void clientSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)
```

### <a name="parameters---clientsetautoupdaterecversion"></a>パラメーター - clientSetAutoUpdateRecVersion

autoUpdateRecVersion  

## <a name="method-serversetautoupdaterecversion"></a>メソッド serverSetAutoUpdateRecVersion

```xpp
private static void serverSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)
```

### <a name="parameters---serversetautoupdaterecversion"></a>パラメーター - serverSetAutoUpdateRecVersion

autoUpdateRecVersion  

## <a name="method-new"></a>メソッド new

現在のセッションまたはパラメーターとして渡されたセッション ID のいずれかに対して xSession オブジェクトのインスタンスを作成します。

```xpp
public void new([int sessionId], [boolean checkSession])
```

### <a name="parameters---new"></a>パラメーター - new

sessionId  
true に設定すると\_SessionId パラメーターで指定されたセッションが存在するかどうかを確認するブール フラグ。 セッションが存在するかどうかを確認する操作は、多くのシステムリソースを使用する可能性があります。 したがって、このパラメーターは既定で false に設定されています。

<!-- -->

checkSession  
true に設定すると\_SessionId パラメーターで指定されたセッションが存在するかどうかを確認するブール フラグ。 セッションが存在するかどうかを確認する操作は、多くのシステムリソースを使用する可能性があります。 したがって、このパラメーターは既定で false に設定されています。

### <a name="examples---new"></a>例 - new

次の例は、すべての有効なセッションの数を返します。

```xpp
server static Integer getAllOnlineUserCount() 
{ 
    int      counter; 
    int      num = 0; 
    int      maxSessions = Info::licensedUsersTotal(); 
    xSession session; 
    UserInfo userInfo; 
    for(counter = 1; counter < maxSessions;counter++) 
    { 
        session = new xSession(counter, true); 
        if(session && session.userId()) 
        { 
            select firstonly userInfo 
                where userInfo.Id == session.userId(); 
            if (userInfo) 
                num++; 
        } 
    } 
    return num; 
}
```

## <a name="method-reloadtablecollectiononclient"></a>メソッド reloadTableCollectionOnClient

```xpp
public static void reloadTableCollectionOnClient()
```

