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
# <a name="class-xsession"></a><span data-ttu-id="0e511-103">クラス xSession</span><span class="sxs-lookup"><span data-stu-id="0e511-103">Class xSession</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xSession extends Object
```

<span data-ttu-id="0e511-104">セッションに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-104">Gets information about sessions.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e511-105">備考</span><span class="sxs-lookup"><span data-stu-id="0e511-105">Remarks</span></span>

<span data-ttu-id="0e511-106">現在のセッションに関する情報を取得するには、パラメーターを指定せずに新しい xSession セッションを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e511-106">To get information about the current session, create a new xSession session without parameters.</span></span> <span data-ttu-id="0e511-107">すべてのアクティブなセッション (AOS のみ) に関する情報を取得する唯一の方法は、セッション ID 1 から xSession.maxSessionId に移動することです。</span><span class="sxs-lookup"><span data-stu-id="0e511-107">The only way to get information about all active sessions (AOS only) is to traverse from session ID 1 to xSession.maxSessionId.</span></span> <span data-ttu-id="0e511-108">ID は、永続的な一覧ではなく、maxSessionId メソッドで指定したセッションの最大数を超えることはありません。</span><span class="sxs-lookup"><span data-stu-id="0e511-108">The IDs are not an unbroken list, but will never exceed the maximum number of sessions as specified in the maxSessionId method.</span></span>

## <a name="examples"></a><span data-ttu-id="0e511-109">例</span><span class="sxs-lookup"><span data-stu-id="0e511-109">Examples</span></span>

<span data-ttu-id="0e511-110">次の例では、新しい xSession オブジェクトを作成し、それを使用して現在のセッションのサーバー名を検索します。</span><span class="sxs-lookup"><span data-stu-id="0e511-110">The following example creates a new xSession object, and then uses it to find the name of the server for the current session.</span></span>

```xpp
xSession xSession; 
xSession = new xSession();   
// Prints the name of server for the current session. 
print xSession.AOSName();
```

## <a name="methods"></a><span data-ttu-id="0e511-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="0e511-111">Methods</span></span>

| <span data-ttu-id="0e511-112">方法</span><span class="sxs-lookup"><span data-stu-id="0e511-112">Method</span></span>                                                                            | <span data-ttu-id="0e511-113">説明</span><span class="sxs-lookup"><span data-stu-id="0e511-113">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e511-114">public str AOSName()</span><span class="sxs-lookup"><span data-stu-id="0e511-114">public str AOSName()</span></span>                                                              | <span data-ttu-id="0e511-115">セッションの処理を担当する Application Object Server (AOS) の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-115">Retrieves the name of the Application Object Server (AOS) that is responsible for servicing the session.</span></span>                       |
| <span data-ttu-id="0e511-116">public str clientComputerName()</span><span class="sxs-lookup"><span data-stu-id="0e511-116">public str clientComputerName()</span></span>                                                   | <span data-ttu-id="0e511-117">セッションの処理を担当するクライアント コンピューターのネットワーク名を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-117">Retrieves the network name of the client computer that is responsible for servicing the session.</span></span>                               |
| <span data-ttu-id="0e511-118">public ClientType clientKind()</span><span class="sxs-lookup"><span data-stu-id="0e511-118">public ClientType clientKind()</span></span>                                                    | <span data-ttu-id="0e511-119">セッションの処理を担当するクライアントの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-119">Retrieves the type of the client that is responsible for servicing the session.</span></span>                                                |
| <span data-ttu-id="0e511-120">public str databaseSpid()</span><span class="sxs-lookup"><span data-stu-id="0e511-120">public str databaseSpid()</span></span>                                                         | <span data-ttu-id="0e511-121">有効な接続 ID のコンマ区切りのリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-121">Retrieves a comma-separated list of active connection IDs.</span></span>                                                                     |
| <span data-ttu-id="0e511-122">public str documentationLanguage()</span><span class="sxs-lookup"><span data-stu-id="0e511-122">public str documentationLanguage()</span></span>                                                | <span data-ttu-id="0e511-123">セッションに表示されるドキュメントの言語 ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-123">Retrieves the language ID of the documentation that is shown for the session.</span></span>                                                  |
| <span data-ttu-id="0e511-124">public str interfaceLanguage()</span><span class="sxs-lookup"><span data-stu-id="0e511-124">public str interfaceLanguage()</span></span>                                                    | <span data-ttu-id="0e511-125">セッションのメニューとダイアログで使用される言語の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-125">Retrieves the ID for the language that is used on menus and dialogs for the session.</span></span>                                           |
| <span data-ttu-id="0e511-126">public boolean isWorkerThread()</span><span class="sxs-lookup"><span data-stu-id="0e511-126">public boolean isWorkerThread()</span></span>                                                   | <span data-ttu-id="0e511-127">セッションがワーカー スレッドかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="0e511-127">Determines whether the session is a worker thread.</span></span>                                                                             |
| <span data-ttu-id="0e511-128">public Date loginDate()</span><span class="sxs-lookup"><span data-stu-id="0e511-128">public Date loginDate()</span></span>                                                           | <span data-ttu-id="0e511-129">セッションのユーザーがログオンした日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-129">Retrieves the date on which the user of the session logged on.</span></span>                                                                 |
| <span data-ttu-id="0e511-130">public DateTime loginDateTime()</span><span class="sxs-lookup"><span data-stu-id="0e511-130">public DateTime loginDateTime()</span></span>                                                   |                                                                                                                                |
| <span data-ttu-id="0e511-131">public TimeOfDay loginTime()</span><span class="sxs-lookup"><span data-stu-id="0e511-131">public TimeOfDay loginTime()</span></span>                                                      | <span data-ttu-id="0e511-132">セッションのユーザーがログオンした時刻を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-132">Retrieves the time at which the user of the session logged on.</span></span>                                                                 |
| <span data-ttu-id="0e511-133">public int masterSessionId()</span><span class="sxs-lookup"><span data-stu-id="0e511-133">public int masterSessionId()</span></span>                                                      | <span data-ttu-id="0e511-134">xSession オブジェクトの対象となるセッションのマスター セッション ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-134">Retrieves the master session ID for the session that the xSession object covers.</span></span>                                               |
| <span data-ttu-id="0e511-135">public int serverId()</span><span class="sxs-lookup"><span data-stu-id="0e511-135">public int serverId()</span></span>                                                             |                                                                                                                                |
| <span data-ttu-id="0e511-136">public int sessionId()</span><span class="sxs-lookup"><span data-stu-id="0e511-136">public int sessionId()</span></span>                                                            | <span data-ttu-id="0e511-137">xSession オブジェクトの対象となるセッションのセッション ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-137">Retrieves the session ID of the session that the xSession object covers.</span></span>                                                       |
| <span data-ttu-id="0e511-138">public boolean terminate(\[Date loginDate\], \[TimeOfDay loginTime\])</span><span class="sxs-lookup"><span data-stu-id="0e511-138">public boolean terminate(\[Date loginDate\], \[TimeOfDay loginTime\])</span></span>             | <span data-ttu-id="0e511-139">オブジェクトのインスタンス化に使用されたセッション ID を終了します。</span><span class="sxs-lookup"><span data-stu-id="0e511-139">Terminates the session ID that the object was instantiated with.</span></span>                                                               |
| <span data-ttu-id="0e511-140">public UserId userId()</span><span class="sxs-lookup"><span data-stu-id="0e511-140">public UserId userId()</span></span>                                                            | <span data-ttu-id="0e511-141">このセッションがログオンしているユーザー ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-141">Retrieves the user ID that this session is logged on with.</span></span>                                                                     |
| <span data-ttu-id="0e511-142">::public static int currentRetryCount()</span><span class="sxs-lookup"><span data-stu-id="0e511-142">::public static int currentRetryCount()</span></span>                                           | <span data-ttu-id="0e511-143">デッドロック、更新の競合、または別の例外の後に try ブロックが再試行された回数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="0e511-143">Counts the number of times a try block has been retried after a deadlock, an update conflict, or another exception.</span></span>            |
| <span data-ttu-id="0e511-144">::public static Uncheck currentUnCheck()</span><span class="sxs-lookup"><span data-stu-id="0e511-144">::public static Uncheck currentUnCheck()</span></span>                                          |                                                                                                                                |
| <span data-ttu-id="0e511-145">::public static str getDbSchema()</span><span class="sxs-lookup"><span data-stu-id="0e511-145">::public static str getDbSchema()</span></span>                                                 | <span data-ttu-id="0e511-146">セッションのデータベース オブジェクト名のスキーマ部分を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-146">Retrieves the schema part of the database object name for the session.</span></span>                                                         |
| <span data-ttu-id="0e511-147">::public static COM getIISObject(IISObject object)</span><span class="sxs-lookup"><span data-stu-id="0e511-147">::public static COM getIISObject(IISObject object)</span></span>                                | <span data-ttu-id="0e511-148">IIS オブジェクトの COM オブジェクトのインスタンスを作成して返します。</span><span class="sxs-lookup"><span data-stu-id="0e511-148">Instantiates and returns a COM object for an IIS object.</span></span>                                                                       |
| <span data-ttu-id="0e511-149">::public static boolean getSysTraceActive()</span><span class="sxs-lookup"><span data-stu-id="0e511-149">::public static boolean getSysTraceActive()</span></span>                                       | <span data-ttu-id="0e511-150">セッションでシステム トレースを有効にするかどうかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="0e511-150">Enables you to determine whether system tracing is turned on for the session.</span></span>                                                  |
| <span data-ttu-id="0e511-151">::public static str getXRefAssembyTempFolder()</span><span class="sxs-lookup"><span data-stu-id="0e511-151">::public static str getXRefAssembyTempFolder()</span></span>                                    |                                                                                                                                |
| <span data-ttu-id="0e511-152">::public static boolean isCLRSession()</span><span class="sxs-lookup"><span data-stu-id="0e511-152">::public static boolean isCLRSession()</span></span>                                            |                                                                                                                                |
| <span data-ttu-id="0e511-153">::public static boolean isUserPreferredTzSameAsLocalMachine()</span><span class="sxs-lookup"><span data-stu-id="0e511-153">::public static boolean isUserPreferredTzSameAsLocalMachine()</span></span>                     |                                                                                                                                |
| <span data-ttu-id="0e511-154">::public static int lastDuplicateKeyViolatingTable()</span><span class="sxs-lookup"><span data-stu-id="0e511-154">::public static int lastDuplicateKeyViolatingTable()</span></span>                              |                                                                                                                                |
| <span data-ttu-id="0e511-155">::public static int lastUpdateConflictingTable()</span><span class="sxs-lookup"><span data-stu-id="0e511-155">::public static int lastUpdateConflictingTable()</span></span>                                  | <span data-ttu-id="0e511-156">最後に更新の競合をしたテーブルのインスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-156">Retrieves an instance of the table that most recently had an update conflict.</span></span>                                                  |
| <span data-ttu-id="0e511-157">::public static int maxSessionId()</span><span class="sxs-lookup"><span data-stu-id="0e511-157">::public static int maxSessionId()</span></span>                                                | <span data-ttu-id="0e511-158">現在のライセンス コードで許可されているセッションの最大数を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-158">Retrieves the maximum number of sessions that are permitted by the current license codes.</span></span>                                      |
| <span data-ttu-id="0e511-159">::public static int numSession()</span><span class="sxs-lookup"><span data-stu-id="0e511-159">::public static int numSession()</span></span>                                                  | <span data-ttu-id="0e511-160">登録されているセッションの現在の番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-160">Retrieves the current number of registered sessions.</span></span>                                                                           |
| <span data-ttu-id="0e511-161">public PreferredLocale preferredLocale()</span><span class="sxs-lookup"><span data-stu-id="0e511-161">public PreferredLocale preferredLocale()</span></span>                                          |                                                                                                                                |
| <span data-ttu-id="0e511-162">::public static int pseudoBandwidth(\[int bandwidth\])</span><span class="sxs-lookup"><span data-stu-id="0e511-162">::public static int pseudoBandwidth(\[int bandwidth\])</span></span>                            | <span data-ttu-id="0e511-163">セッションの帯域幅シミュレーションをオンにするかどうかを決定し、帯域幅シミュレーションをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="0e511-163">Determines whether bandwidth simulation is turned on for the session, and enables bandwidth simulation to be turned on or off.</span></span> |
| <span data-ttu-id="0e511-164">::public static int pseudoLatency(\[int latency\])</span><span class="sxs-lookup"><span data-stu-id="0e511-164">::public static int pseudoLatency(\[int latency\])</span></span>                                | <span data-ttu-id="0e511-165">セッションの待機シミュレーションをオンにするかどうかを決定し、待機シミュレーションをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="0e511-165">Determines whether latency simulation is turned on for the session, and enables latency simulation to be turned on or off.</span></span>     |
| <span data-ttu-id="0e511-166">::public static int pseudoSimMode(\[int simMode\])</span><span class="sxs-lookup"><span data-stu-id="0e511-166">::public static int pseudoSimMode(\[int simMode\])</span></span>                                | <span data-ttu-id="0e511-167">セッションの遅延シミュレーションをオンにするかどうかを決定し、遅延シミュレーションをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="0e511-167">Determines whether delay simulation is turned on for the session, and enables delay simulation to be turned on or off.</span></span>         |
| <span data-ttu-id="0e511-168">::public static int systemSessionId()</span><span class="sxs-lookup"><span data-stu-id="0e511-168">::public static int systemSessionId()</span></span>                                             | <span data-ttu-id="0e511-169">xSession オブジェクトの対象となるセッションのシステム セッション ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-169">Retrieves the system session ID for the session that the xSession object covers.</span></span>                                               |
| <span data-ttu-id="0e511-170">::public static container xppCallStack()</span><span class="sxs-lookup"><span data-stu-id="0e511-170">::public static container xppCallStack()</span></span>                                          | <span data-ttu-id="0e511-171">現在の呼び出し履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-171">Retrieves the current call stack.</span></span>                                                                                              |
| <span data-ttu-id="0e511-172">::public static void removeAOC()</span><span class="sxs-lookup"><span data-stu-id="0e511-172">::public static void removeAOC()</span></span>                                                  | <span data-ttu-id="0e511-173">現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を削除します。</span><span class="sxs-lookup"><span data-stu-id="0e511-173">Removes the Application Object Server client-side cache (AOC) for the current session.</span></span>                                         |
| <span data-ttu-id="0e511-174">::public static void updateAOC()</span><span class="sxs-lookup"><span data-stu-id="0e511-174">::public static void updateAOC()</span></span>                                                  | <span data-ttu-id="0e511-175">現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を更新します。</span><span class="sxs-lookup"><span data-stu-id="0e511-175">Updates the Application Object Server client-side cache (AOC) for the current session.</span></span>                                         |
| <span data-ttu-id="0e511-176">::public static void setAutoUpdateRecVersion(boolean autoUpdateRecVersion)</span><span class="sxs-lookup"><span data-stu-id="0e511-176">::public static void setAutoUpdateRecVersion(boolean autoUpdateRecVersion)</span></span>        |                                                                                                                                |
| <span data-ttu-id="0e511-177">::public static void setSysTraceActive(boolean nValue)</span><span class="sxs-lookup"><span data-stu-id="0e511-177">::public static void setSysTraceActive(boolean nValue)</span></span>                            | <span data-ttu-id="0e511-178">システム追跡のオンまたはオフを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0e511-178">Switches system tracing on or off.</span></span>                                                                                             |
| <span data-ttu-id="0e511-179">::private static void clientSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)</span><span class="sxs-lookup"><span data-stu-id="0e511-179">::private static void clientSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)</span></span> |                                                                                                                                |
| <span data-ttu-id="0e511-180">::private static void serverSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)</span><span class="sxs-lookup"><span data-stu-id="0e511-180">::private static void serverSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)</span></span> |                                                                                                                                |
| <span data-ttu-id="0e511-181">public void new(\[int sessionId\], \[boolean checkSession\])</span><span class="sxs-lookup"><span data-stu-id="0e511-181">public void new(\[int sessionId\], \[boolean checkSession\])</span></span>                      | <span data-ttu-id="0e511-182">現在のセッションまたはパラメーターとして渡されたセッション ID のいずれかに対して xSession オブジェクトのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e511-182">Instantiates the xSession object, either for current session or for the session ID passed in as a parameter.</span></span>                   |
| <span data-ttu-id="0e511-183">::public static void reloadTableCollectionOnClient()</span><span class="sxs-lookup"><span data-stu-id="0e511-183">::public static void reloadTableCollectionOnClient()</span></span>                              |                                                                                                                                |

## <a name="method-aosname"></a><span data-ttu-id="0e511-184">メソッド AOSName</span><span class="sxs-lookup"><span data-stu-id="0e511-184">Method AOSName</span></span>

<span data-ttu-id="0e511-185">セッションの処理を担当する Application Object Server (AOS) の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-185">Retrieves the name of the Application Object Server (AOS) that is responsible for servicing the session.</span></span>

```xpp
public str AOSName()
```

### <a name="return-value---aosname"></a><span data-ttu-id="0e511-186">戻り値 - AOSName</span><span class="sxs-lookup"><span data-stu-id="0e511-186">Return Value - AOSName</span></span>

<span data-ttu-id="0e511-187">AOS の名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="0e511-187">A string that indicates the name of the AOS.</span></span>

### <a name="remarks---aosname"></a><span data-ttu-id="0e511-188">備考 - AOSName</span><span class="sxs-lookup"><span data-stu-id="0e511-188">Remarks - AOSName</span></span>

<span data-ttu-id="0e511-189">AOS 以外の接続されているクライアントについては、このメソッドは空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="0e511-189">For non�AOS connected clients, this method returns an empty string.</span></span>

### <a name="examples---aosname"></a><span data-ttu-id="0e511-190">例 - AOSName</span><span class="sxs-lookup"><span data-stu-id="0e511-190">Examples - AOSName</span></span>

<span data-ttu-id="0e511-191">次の例は、現在のセッションを実行している AOS の名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="0e511-191">The following example prints the name of the AOS that is running the current session.</span></span>

```xpp
xSession xSession; 
xSession = new xSession(); 
// Prints the name of server for the current session. 
print xSession.AOSName();
```

## <a name="method-clientcomputername"></a><span data-ttu-id="0e511-192">メソッド clientComputerName</span><span class="sxs-lookup"><span data-stu-id="0e511-192">Method clientComputerName</span></span>

<span data-ttu-id="0e511-193">セッションの処理を担当するクライアント コンピューターのネットワーク名を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-193">Retrieves the network name of the client computer that is responsible for servicing the session.</span></span>

```xpp
public str clientComputerName()
```

### <a name="return-value---clientcomputername"></a><span data-ttu-id="0e511-194">戻り値 - clientComputerName</span><span class="sxs-lookup"><span data-stu-id="0e511-194">Return Value - clientComputerName</span></span>

<span data-ttu-id="0e511-195">クライアント コンピューターの名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="0e511-195">A string that indicates the name of the client computer.</span></span>

### <a name="examples---clientcomputername"></a><span data-ttu-id="0e511-196">例 - clientComputerName</span><span class="sxs-lookup"><span data-stu-id="0e511-196">Examples - clientComputerName</span></span>

<span data-ttu-id="0e511-197">次の例は、現在のセッションを実行しているクライアントの名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="0e511-197">The following example prints the name of the client that is running the current session.</span></span>

```xpp
{ 
    xSession xSession; 
    xSession = new xSession(); 
    print xSession.clientComputerName(); 
    pause; 
}
```

## <a name="method-clientkind"></a><span data-ttu-id="0e511-198">メソッド clientKind</span><span class="sxs-lookup"><span data-stu-id="0e511-198">Method clientKind</span></span>

<span data-ttu-id="0e511-199">セッションの処理を担当するクライアントの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-199">Retrieves the type of the client that is responsible for servicing the session.</span></span>

```xpp
public ClientType clientKind()
```

### <a name="return-value---clientkind"></a><span data-ttu-id="0e511-200">戻り値 - clientKind</span><span class="sxs-lookup"><span data-stu-id="0e511-200">Return Value - clientKind</span></span>

<span data-ttu-id="0e511-201">クライアントのタイプ。</span><span class="sxs-lookup"><span data-stu-id="0e511-201">The type of the client.</span></span>

### <a name="remarks---clientkind"></a><span data-ttu-id="0e511-202">備考 - clientKind</span><span class="sxs-lookup"><span data-stu-id="0e511-202">Remarks - clientKind</span></span>

<span data-ttu-id="0e511-203">可能な値は、ClientType システム列挙の値です。</span><span class="sxs-lookup"><span data-stu-id="0e511-203">The possible values are those in the ClientType system enumeration:</span></span>

-   <span data-ttu-id="0e511-204">COMObject</span><span class="sxs-lookup"><span data-stu-id="0e511-204">COMObject</span></span>
-   <span data-ttu-id="0e511-205">クライアント</span><span class="sxs-lookup"><span data-stu-id="0e511-205">Client</span></span>
-   <span data-ttu-id="0e511-206">サーバー</span><span class="sxs-lookup"><span data-stu-id="0e511-206">Server</span></span>
-   <span data-ttu-id="0e511-207">WorkerThread</span><span class="sxs-lookup"><span data-stu-id="0e511-207">WorkerThread</span></span>

### <a name="examples---clientkind"></a><span data-ttu-id="0e511-208">例 - clientKind</span><span class="sxs-lookup"><span data-stu-id="0e511-208">Examples - clientKind</span></span>

<span data-ttu-id="0e511-209">次の例は、現在のセッションを実行しているクライアントのタイプを表示します。</span><span class="sxs-lookup"><span data-stu-id="0e511-209">The following example prints the type of the client that is running the current session.</span></span>

```xpp
{ 
    xSession xSession; 
    xSession = new xSession(); 
    print xSession.clientKind(); 
    pause; 
}
```

## <a name="method-databasespid"></a><span data-ttu-id="0e511-210">メソッド databaseSpid</span><span class="sxs-lookup"><span data-stu-id="0e511-210">Method databaseSpid</span></span>

<span data-ttu-id="0e511-211">有効な接続 ID のコンマ区切りのリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-211">Retrieves a comma-separated list of active connection IDs.</span></span>

```xpp
public str databaseSpid()
```

### <a name="return-value---databasespid"></a><span data-ttu-id="0e511-212">戻り値 - databaseSpid</span><span class="sxs-lookup"><span data-stu-id="0e511-212">Return Value - databaseSpid</span></span>

<span data-ttu-id="0e511-213">有効な接続 ID のコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="0e511-213">A comma-separated list of active connection IDs.</span></span>

### <a name="remarks---databasespid"></a><span data-ttu-id="0e511-214">備考 - databaseSpid</span><span class="sxs-lookup"><span data-stu-id="0e511-214">Remarks - databaseSpid</span></span>

<span data-ttu-id="0e511-215">このメソッドは、オンライン ユーザー フォーム (SysUsersOnline) を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e511-215">This method is used to populate the Online users form (SysUsersOnline).</span></span> <span data-ttu-id="0e511-216">有効な接続の数を取得するには、xSession::numSession を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e511-216">To retrieve the number of active connections, use xSession::numSession.</span></span>

## <a name="method-documentationlanguage"></a><span data-ttu-id="0e511-217">メソッド documentationLanguage</span><span class="sxs-lookup"><span data-stu-id="0e511-217">Method documentationLanguage</span></span>

<span data-ttu-id="0e511-218">セッションに表示されるドキュメントの言語 ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-218">Retrieves the language ID of the documentation that is shown for the session.</span></span>

```xpp
public str documentationLanguage()
```

### <a name="return-value---documentationlanguage"></a><span data-ttu-id="0e511-219">戻り値 - documentationLanguage</span><span class="sxs-lookup"><span data-stu-id="0e511-219">Return Value - documentationLanguage</span></span>

<span data-ttu-id="0e511-220">セッションのドキュメントに使用される言語の ID を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="0e511-220">A string that contains the ID of the language that is used for the documentation in the session.</span></span>

### <a name="remarks---documentationlanguage"></a><span data-ttu-id="0e511-221">備考 - documentationLanguage</span><span class="sxs-lookup"><span data-stu-id="0e511-221">Remarks - documentationLanguage</span></span>

<span data-ttu-id="0e511-222">たとえば、このメソッドは、言語が英語 (US) に設定されている場合「en-us」を返します。</span><span class="sxs-lookup"><span data-stu-id="0e511-222">For example, this method returns "en-us" if the language is set to US English.</span></span> <span data-ttu-id="0e511-223">ドキュメントの言語は個別に選択することができ、メニューやダイアログで使用される言語と必ずしも同一ではありません。</span><span class="sxs-lookup"><span data-stu-id="0e511-223">The documentation language can be selected separately and is not necessarily identical to the language used in menus and dialogs.</span></span> <span data-ttu-id="0e511-224">メニューやダイアログ ボックスの言語 ID を取得するには、xSession.interfaceLanguage を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e511-224">To retrieve the language ID for menus and dialogs, use xSession.interfaceLanguage.</span></span> <span data-ttu-id="0e511-225">xInfo.documentationLanguage を使用すると、ドキュメントの言語を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0e511-225">xInfo.documentationLanguage enables you to set the documentation language.</span></span>

## <a name="method-interfacelanguage"></a><span data-ttu-id="0e511-226">メソッド interfaceLanguage</span><span class="sxs-lookup"><span data-stu-id="0e511-226">Method interfaceLanguage</span></span>

<span data-ttu-id="0e511-227">セッションのメニューとダイアログで使用される言語の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-227">Retrieves the ID for the language that is used on menus and dialogs for the session.</span></span>

```xpp
public str interfaceLanguage()
```

### <a name="return-value---interfacelanguage"></a><span data-ttu-id="0e511-228">戻り値 - interfaceLanguage</span><span class="sxs-lookup"><span data-stu-id="0e511-228">Return Value - interfaceLanguage</span></span>

<span data-ttu-id="0e511-229">セッションのメニューとダイアログで使用される言語の ID を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="0e511-229">A string that contains the ID of the language used on menus and dialogs in the session.</span></span>

### <a name="remarks---interfacelanguage"></a><span data-ttu-id="0e511-230">備考 - interfaceLanguage</span><span class="sxs-lookup"><span data-stu-id="0e511-230">Remarks - interfaceLanguage</span></span>

<span data-ttu-id="0e511-231">たとえば、このメソッドは、言語が英語 (US) に設定されている場合「en-us」を返します。</span><span class="sxs-lookup"><span data-stu-id="0e511-231">For example, this method returns "en-us" if the language is set to US English.</span></span> <span data-ttu-id="0e511-232">ドキュメントの言語は個別に選択することができ、メニューやダイアログで使用される言語と必ずしも同一ではありません。</span><span class="sxs-lookup"><span data-stu-id="0e511-232">The documentation language can be selected separately and is not necessarily identical to the language used in menus and dialogs.</span></span> <span data-ttu-id="0e511-233">ドキュメントの言語 ID を取得するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e511-233">To retrieve the language ID for documentation, use .</span></span>

## <a name="method-isworkerthread"></a><span data-ttu-id="0e511-234">メソッド isWorkerThread</span><span class="sxs-lookup"><span data-stu-id="0e511-234">Method isWorkerThread</span></span>

<span data-ttu-id="0e511-235">セッションがワーカー スレッドかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="0e511-235">Determines whether the session is a worker thread.</span></span>

```xpp
public boolean isWorkerThread()
```

### <a name="return-value---isworkerthread"></a><span data-ttu-id="0e511-236">戻り値 - isWorkerThread</span><span class="sxs-lookup"><span data-stu-id="0e511-236">Return Value - isWorkerThread</span></span>

<span data-ttu-id="0e511-237">セッションがワーカー スレッドである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0e511-237">true if the session is a worker thread; otherwise, false.</span></span>

### <a name="remarks---isworkerthread"></a><span data-ttu-id="0e511-238">備考 - isWorkerThread</span><span class="sxs-lookup"><span data-stu-id="0e511-238">Remarks - isWorkerThread</span></span>

<span data-ttu-id="0e511-239">ワーカー スレッドは、Thread クラスのインスタンスで、UI がない新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e511-239">A worker thread is an instance of the Thread class, which creates a new instance without UI.</span></span> <span data-ttu-id="0e511-240">このメソッドがこのようなセッション内で呼び出される場合は true が返されます。</span><span class="sxs-lookup"><span data-stu-id="0e511-240">If this method is called inside such a session, it will return true.</span></span>

## <a name="method-logindate"></a><span data-ttu-id="0e511-241">メソッド loginDate</span><span class="sxs-lookup"><span data-stu-id="0e511-241">Method loginDate</span></span>

<span data-ttu-id="0e511-242">セッションのユーザーがログオンした日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-242">Retrieves the date on which the user of the session logged on.</span></span>

```xpp
public Date loginDate()
```

### <a name="return-value---logindate"></a><span data-ttu-id="0e511-243">戻り値 - loginDate</span><span class="sxs-lookup"><span data-stu-id="0e511-243">Return Value - loginDate</span></span>

<span data-ttu-id="0e511-244">セッションのユーザーがログオンした日付。</span><span class="sxs-lookup"><span data-stu-id="0e511-244">The date that the user of the session logged on.</span></span>

## <a name="method-logindatetime"></a><span data-ttu-id="0e511-245">メソッド loginDateTime</span><span class="sxs-lookup"><span data-stu-id="0e511-245">Method loginDateTime</span></span>

```xpp
public DateTime loginDateTime()
```

### <a name="return-value---logindatetime"></a><span data-ttu-id="0e511-246">戻り値 - loginDateTime</span><span class="sxs-lookup"><span data-stu-id="0e511-246">Return Value - loginDateTime</span></span>

## <a name="method-logintime"></a><span data-ttu-id="0e511-247">メソッド loginTime</span><span class="sxs-lookup"><span data-stu-id="0e511-247">Method loginTime</span></span>

<span data-ttu-id="0e511-248">セッションのユーザーがログオンした時刻を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-248">Retrieves the time at which the user of the session logged on.</span></span>

```xpp
public TimeOfDay loginTime()
```

### <a name="return-value---logintime"></a><span data-ttu-id="0e511-249">戻り値 - loginTime</span><span class="sxs-lookup"><span data-stu-id="0e511-249">Return Value - loginTime</span></span>

<span data-ttu-id="0e511-250">セッションのユーザーがログオンした時間。</span><span class="sxs-lookup"><span data-stu-id="0e511-250">The time that the user of the session logged on.</span></span>

## <a name="method-mastersessionid"></a><span data-ttu-id="0e511-251">メソッド masterSessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-251">Method masterSessionId</span></span>

<span data-ttu-id="0e511-252">xSession オブジェクトの対象となるセッションのマスター セッション ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-252">Retrieves the master session ID for the session that the xSession object covers.</span></span>

```xpp
public int masterSessionId()
```

### <a name="return-value---mastersessionid"></a><span data-ttu-id="0e511-253">戻り値 - masterSessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-253">Return Value - masterSessionId</span></span>

<span data-ttu-id="0e511-254">セッション ID を表す整数。</span><span class="sxs-lookup"><span data-stu-id="0e511-254">An integer that represents the session ID.</span></span>

### <a name="remarks---mastersessionid"></a><span data-ttu-id="0e511-255">備考 - masterSessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-255">Remarks - masterSessionId</span></span>

<span data-ttu-id="0e511-256">一部のセッションには、COM セッションまたはワーカー スレッド セッションなどのマスター セッション ID があります。</span><span class="sxs-lookup"><span data-stu-id="0e511-256">Some sessions have a master session ID, such as a COM session or a worker thread session.</span></span>

### <a name="examples---mastersessionid"></a><span data-ttu-id="0e511-257">例 - masterSessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-257">Examples - masterSessionId</span></span>

<span data-ttu-id="0e511-258">次の例では、通常のセッション ID (または存在する場合は､マスター セッション ID) を使用して xSession オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e511-258">The following example creates an xSession object by using the normal session ID (or the master session ID, if there is one).</span></span>

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

## <a name="method-serverid"></a><span data-ttu-id="0e511-259">メソッド serverId</span><span class="sxs-lookup"><span data-stu-id="0e511-259">Method serverId</span></span>

```xpp
public int serverId()
```

### <a name="return-value---serverid"></a><span data-ttu-id="0e511-260">戻り値 - serverId</span><span class="sxs-lookup"><span data-stu-id="0e511-260">Return Value - serverId</span></span>

## <a name="method-sessionid"></a><span data-ttu-id="0e511-261">メソッド sessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-261">Method sessionId</span></span>

<span data-ttu-id="0e511-262">xSession オブジェクトの対象となるセッションのセッション ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-262">Retrieves the session ID of the session that the xSession object covers.</span></span>

```xpp
public int sessionId()
```

### <a name="return-value---sessionid"></a><span data-ttu-id="0e511-263">戻り値 - sessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-263">Return Value - sessionId</span></span>

<span data-ttu-id="0e511-264">セッション ID を表す整数。</span><span class="sxs-lookup"><span data-stu-id="0e511-264">An integer that represents the session ID.</span></span>

## <a name="method-terminate"></a><span data-ttu-id="0e511-265">メソッド terminate</span><span class="sxs-lookup"><span data-stu-id="0e511-265">Method terminate</span></span>

<span data-ttu-id="0e511-266">オブジェクトのインスタンス化に使用されたセッション ID を終了します。</span><span class="sxs-lookup"><span data-stu-id="0e511-266">Terminates the session ID that the object was instantiated with.</span></span>

```xpp
public boolean terminate([Date loginDate], [TimeOfDay loginTime])
```

### <a name="parameters---terminate"></a><span data-ttu-id="0e511-267">パラメーター - terminate</span><span class="sxs-lookup"><span data-stu-id="0e511-267">Parameters - terminate</span></span>

<span data-ttu-id="0e511-268">loginDate</span><span class="sxs-lookup"><span data-stu-id="0e511-268">loginDate</span></span>  
<span data-ttu-id="0e511-269">セッションのユーザーがログオンした時間 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0e511-269">The time that the user of the session logged on; optional.</span></span>

<!-- -->

<span data-ttu-id="0e511-270">loginTime</span><span class="sxs-lookup"><span data-stu-id="0e511-270">loginTime</span></span>  
<span data-ttu-id="0e511-271">セッションのユーザーがログオンした時間 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0e511-271">The time that the user of the session logged on; optional.</span></span>

### <a name="return-value---terminate"></a><span data-ttu-id="0e511-272">戻り値 - terminate</span><span class="sxs-lookup"><span data-stu-id="0e511-272">Return Value - terminate</span></span>

<span data-ttu-id="0e511-273">ユーザーにこの関数を実行する権限がない場合は false; それ以外の場合は true。</span><span class="sxs-lookup"><span data-stu-id="0e511-273">false if the user is not authorized to perform this function; otherwise, true.</span></span>

### <a name="remarks---terminate"></a><span data-ttu-id="0e511-274">備考 - terminate</span><span class="sxs-lookup"><span data-stu-id="0e511-274">Remarks - terminate</span></span>

<span data-ttu-id="0e511-275">この API には、実行時に呼び出される組み込み認証チェックがあります。</span><span class="sxs-lookup"><span data-stu-id="0e511-275">This API has a built-in authorization check that is invoked at run time.</span></span> <span data-ttu-id="0e511-276">終了メソッドの呼び出しが開発セキュリティ キー (SysDevelopment) のアクセス権のないユーザーによって行われた場合はスローされます。</span><span class="sxs-lookup"><span data-stu-id="0e511-276">An exception is thrown if calls to the terminate method are made by users who do not have access to the development security key (SysDevelopment).</span></span> <span data-ttu-id="0e511-277">オプションのパラメーターを使用すると、セッションにタイムスタンプを設定して、終了する予定のセッションであることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="0e511-277">The optional parameters allow you to put a timestamp on the session to ensure that it is the session you intend to terminate.</span></span> <span data-ttu-id="0e511-278">同じセッション ID を 2 つの異なる時間に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0e511-278">The same session ID could be used at two different times.</span></span> <span data-ttu-id="0e511-279">terminate メソッドは、オンライン ユーザー フォームで管理者がセッションを終了できるようにするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e511-279">The terminate method is used in the Online users form to allow administrators to terminate sessions.</span></span> <span data-ttu-id="0e511-280">管理者はセッションが応答を停止した場合や、多くのリソースを消費した場合、または別のユーザーのためにライセンスを解放する必要がある場合にセッションを終了させることがあります。</span><span class="sxs-lookup"><span data-stu-id="0e511-280">An administrator might decide to terminate a session because it has stopped responding, is consuming a lot of resources, or its license needs to be freed for another user.</span></span>

### <a name="examples---terminate"></a><span data-ttu-id="0e511-281">例 - terminate</span><span class="sxs-lookup"><span data-stu-id="0e511-281">Examples - terminate</span></span>

<span data-ttu-id="0e511-282">次の例では、ユーザーにセッションを終了する権限があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e511-282">The following example confirms whether the user has permission to terminate the session.</span></span> <span data-ttu-id="0e511-283">その場合は、セッションが終了します。</span><span class="sxs-lookup"><span data-stu-id="0e511-283">If so, the session is terminated.</span></span>

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

## <a name="method-userid"></a><span data-ttu-id="0e511-284">メソッド userId</span><span class="sxs-lookup"><span data-stu-id="0e511-284">Method userId</span></span>

<span data-ttu-id="0e511-285">このセッションがログオンしているユーザー ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-285">Retrieves the user ID that this session is logged on with.</span></span>

```xpp
public UserId userId()
```

### <a name="return-value---userid"></a><span data-ttu-id="0e511-286">戻り値 - userId</span><span class="sxs-lookup"><span data-stu-id="0e511-286">Return Value - userId</span></span>

<span data-ttu-id="0e511-287">セッションのユーザーの ID です。</span><span class="sxs-lookup"><span data-stu-id="0e511-287">The ID for the user of the session.</span></span>

### <a name="examples---userid"></a><span data-ttu-id="0e511-288">例 - userId</span><span class="sxs-lookup"><span data-stu-id="0e511-288">Examples - userId</span></span>

<span data-ttu-id="0e511-289">次の例では、特定のユーザーがオンラインかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="0e511-289">The following example determines whether a particular user is online.</span></span>

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

## <a name="method-currentretrycount"></a><span data-ttu-id="0e511-290">メソッド currentRetryCount</span><span class="sxs-lookup"><span data-stu-id="0e511-290">Method currentRetryCount</span></span>

<span data-ttu-id="0e511-291">デッドロック、更新の競合、または別の例外の後に try ブロックが再試行された回数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="0e511-291">Counts the number of times a try block has been retried after a deadlock, an update conflict, or another exception.</span></span>

```xpp
public static int currentRetryCount()
```

### <a name="return-value---currentretrycount"></a><span data-ttu-id="0e511-292">戻り値 - currentRetryCount</span><span class="sxs-lookup"><span data-stu-id="0e511-292">Return Value - currentRetryCount</span></span>

<span data-ttu-id="0e511-293">try ブロックが再試行された回数。</span><span class="sxs-lookup"><span data-stu-id="0e511-293">The number of times that the try block has been retried.</span></span>

### <a name="examples---currentretrycount"></a><span data-ttu-id="0e511-294">例 - currentRetryCount</span><span class="sxs-lookup"><span data-stu-id="0e511-294">Examples - currentRetryCount</span></span>

<span data-ttu-id="0e511-295">次の例では、currentRetryCount メソッドを使用して、トランザクションが CUD トランザクションの例外処理を判断するために再試行された回数をテストします。</span><span class="sxs-lookup"><span data-stu-id="0e511-295">The following example uses the currentRetryCount method to test how many times that a transaction has been retried to determine the exception handling for a CUD transaction.</span></span>

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

## <a name="method-currentuncheck"></a><span data-ttu-id="0e511-296">メソッド currentUnCheck</span><span class="sxs-lookup"><span data-stu-id="0e511-296">Method currentUnCheck</span></span>

```xpp
public static Uncheck currentUnCheck()
```

### <a name="return-value---currentuncheck"></a><span data-ttu-id="0e511-297">戻り値 - currentUnCheck</span><span class="sxs-lookup"><span data-stu-id="0e511-297">Return Value - currentUnCheck</span></span>

## <a name="method-getdbschema"></a><span data-ttu-id="0e511-298">メソッド getDbSchema</span><span class="sxs-lookup"><span data-stu-id="0e511-298">Method getDbSchema</span></span>

<span data-ttu-id="0e511-299">セッションのデータベース オブジェクト名のスキーマ部分を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-299">Retrieves the schema part of the database object name for the session.</span></span>

```xpp
public static str getDbSchema()
```

### <a name="return-value---getdbschema"></a><span data-ttu-id="0e511-300">戻り値 - getDbSchema</span><span class="sxs-lookup"><span data-stu-id="0e511-300">Return Value - getDbSchema</span></span>

<span data-ttu-id="0e511-301">データベース オブジェクト名のスキーマ部分を返します。</span><span class="sxs-lookup"><span data-stu-id="0e511-301">Returns the schema part of the database object name.</span></span>

## <a name="method-getiisobject"></a><span data-ttu-id="0e511-302">メソッド getIISObject</span><span class="sxs-lookup"><span data-stu-id="0e511-302">Method getIISObject</span></span>

<span data-ttu-id="0e511-303">IIS オブジェクトの COM オブジェクトのインスタンスを作成して返します。</span><span class="sxs-lookup"><span data-stu-id="0e511-303">Instantiates and returns a COM object for an IIS object.</span></span>

```xpp
public static COM getIISObject(IISObject object)
```

### <a name="parameters---getiisobject"></a><span data-ttu-id="0e511-304">パラメーター - getIISObject</span><span class="sxs-lookup"><span data-stu-id="0e511-304">Parameters - getIISObject</span></span>

<span data-ttu-id="0e511-305">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0e511-305">object</span></span>  
<span data-ttu-id="0e511-306">COM オブジェクトを作成する IIS オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0e511-306">The IIS object that you want to create a COM object for.</span></span>

### <a name="return-value---getiisobject"></a><span data-ttu-id="0e511-307">戻り値 - getIISObject</span><span class="sxs-lookup"><span data-stu-id="0e511-307">Return Value - getIISObject</span></span>

<span data-ttu-id="0e511-308">COM オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0e511-308">A COM object.</span></span>

### <a name="remarks---getiisobject"></a><span data-ttu-id="0e511-309">備考 - getIISObject</span><span class="sxs-lookup"><span data-stu-id="0e511-309">Remarks - getIISObject</span></span>

<span data-ttu-id="0e511-310">IIS オブジェクトは、IISObject システム列挙によって提供される使用可能な値のいずれかにすることができます。</span><span class="sxs-lookup"><span data-stu-id="0e511-310">The IIS object can be one of the possible values supplied by the IISObject system enumeration:</span></span>

-   <span data-ttu-id="0e511-311">ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="0e511-311">ApplicationObject</span></span>
-   <span data-ttu-id="0e511-312">要求</span><span class="sxs-lookup"><span data-stu-id="0e511-312">Request</span></span>
-   <span data-ttu-id="0e511-313">応答</span><span class="sxs-lookup"><span data-stu-id="0e511-313">Response</span></span>
-   <span data-ttu-id="0e511-314">サーバー</span><span class="sxs-lookup"><span data-stu-id="0e511-314">Server</span></span>
-   <span data-ttu-id="0e511-315">SessionObject</span><span class="sxs-lookup"><span data-stu-id="0e511-315">SessionObject</span></span>

## <a name="method-getsystraceactive"></a><span data-ttu-id="0e511-316">メソッド getSysTraceActive</span><span class="sxs-lookup"><span data-stu-id="0e511-316">Method getSysTraceActive</span></span>

<span data-ttu-id="0e511-317">セッションでシステム トレースを有効にするかどうかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="0e511-317">Enables you to determine whether system tracing is turned on for the session.</span></span>

```xpp
public static boolean getSysTraceActive()
```

### <a name="return-value---getsystraceactive"></a><span data-ttu-id="0e511-318">戻り値 - getSysTraceActive</span><span class="sxs-lookup"><span data-stu-id="0e511-318">Return Value - getSysTraceActive</span></span>

<span data-ttu-id="0e511-319">システム トレースが有効な場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0e511-319">true if system tracing is active; otherwise, false.</span></span>

### <a name="remarks---getsystraceactive"></a><span data-ttu-id="0e511-320">備考 - getSysTraceActive</span><span class="sxs-lookup"><span data-stu-id="0e511-320">Remarks - getSysTraceActive</span></span>

<span data-ttu-id="0e511-321">システム トレースを有効にするには、xSession::setSysTraceActive を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e511-321">To turn on system tracing, use xSession::setSysTraceActive.</span></span>

### <a name="examples---getsystraceactive"></a><span data-ttu-id="0e511-322">例 - getSysTraceActive</span><span class="sxs-lookup"><span data-stu-id="0e511-322">Examples - getSysTraceActive</span></span>

<span data-ttu-id="0e511-323">次の例では、getSysTraceActive メソッドを使用してシステム トレースの元の設定を判断し、トレースを一時的に false に設定した後に設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="0e511-323">The following example uses the getSysTraceActive method to determine the original setting for system tracing and to reset the setting after tracing is temporarily set to false.</span></span>

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

## <a name="method-getxrefassembytempfolder"></a><span data-ttu-id="0e511-324">メソッド getXRefAssembyTempFolder</span><span class="sxs-lookup"><span data-stu-id="0e511-324">Method getXRefAssembyTempFolder</span></span>

```xpp
public static str getXRefAssembyTempFolder()
```

### <a name="return-value---getxrefassembytempfolder"></a><span data-ttu-id="0e511-325">戻り値 - getXRefAssembyTempFolder</span><span class="sxs-lookup"><span data-stu-id="0e511-325">Return Value - getXRefAssembyTempFolder</span></span>

## <a name="method-isclrsession"></a><span data-ttu-id="0e511-326">メソッド isCLRSession</span><span class="sxs-lookup"><span data-stu-id="0e511-326">Method isCLRSession</span></span>

```xpp
public static boolean isCLRSession()
```

### <a name="return-value---isclrsession"></a><span data-ttu-id="0e511-327">戻り値 - isCLRSession</span><span class="sxs-lookup"><span data-stu-id="0e511-327">Return Value - isCLRSession</span></span>

## <a name="method-isuserpreferredtzsameaslocalmachine"></a><span data-ttu-id="0e511-328">メソッド isUserPreferredTzSameAsLocalMachine</span><span class="sxs-lookup"><span data-stu-id="0e511-328">Method isUserPreferredTzSameAsLocalMachine</span></span>

```xpp
public static boolean isUserPreferredTzSameAsLocalMachine()
```

### <a name="return-value---isuserpreferredtzsameaslocalmachine"></a><span data-ttu-id="0e511-329">戻り値 - isUserPreferredTzSameAsLocalMachine</span><span class="sxs-lookup"><span data-stu-id="0e511-329">Return Value - isUserPreferredTzSameAsLocalMachine</span></span>

## <a name="method-lastduplicatekeyviolatingtable"></a><span data-ttu-id="0e511-330">メソッド lastDuplicateKeyViolatingTable</span><span class="sxs-lookup"><span data-stu-id="0e511-330">Method lastDuplicateKeyViolatingTable</span></span>

```xpp
public static int lastDuplicateKeyViolatingTable()
```

### <a name="return-value---lastduplicatekeyviolatingtable"></a><span data-ttu-id="0e511-331">戻り値 - lastDuplicateKeyViolatingTable</span><span class="sxs-lookup"><span data-stu-id="0e511-331">Return Value - lastDuplicateKeyViolatingTable</span></span>

## <a name="method-lastupdateconflictingtable"></a><span data-ttu-id="0e511-332">メソッド lastUpdateConflictingTable</span><span class="sxs-lookup"><span data-stu-id="0e511-332">Method lastUpdateConflictingTable</span></span>

<span data-ttu-id="0e511-333">最後に更新の競合をしたテーブルのインスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-333">Retrieves an instance of the table that most recently had an update conflict.</span></span>

```xpp
public static int lastUpdateConflictingTable()
```

### <a name="return-value---lastupdateconflictingtable"></a><span data-ttu-id="0e511-334">戻り値 - lastUpdateConflictingTable</span><span class="sxs-lookup"><span data-stu-id="0e511-334">Return Value - lastUpdateConflictingTable</span></span>

<span data-ttu-id="0e511-335">最後に、更新の競合をしたテーブルのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="0e511-335">An instance of the table that most recently had an update conflict.</span></span>

### <a name="examples---lastupdateconflictingtable"></a><span data-ttu-id="0e511-336">例 - lastUpdateConflictingTable</span><span class="sxs-lookup"><span data-stu-id="0e511-336">Examples - lastUpdateConflictingTable</span></span>

<span data-ttu-id="0e511-337">次の例では、lastUpdateConflictingTable メソッドの一般的な使用方法を示しています。これにより、更新の競合が発生しているテーブルに従ってトランザクションを中断または再試行できます。</span><span class="sxs-lookup"><span data-stu-id="0e511-337">The following example demonstrates the general use of the lastUpdateConflictingTable method�it enables you to abort or retry transactions according to which table has an update conflict.</span></span>

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

## <a name="method-maxsessionid"></a><span data-ttu-id="0e511-338">メソッド maxSessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-338">Method maxSessionId</span></span>

<span data-ttu-id="0e511-339">現在のライセンス コードで許可されているセッションの最大数を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-339">Retrieves the maximum number of sessions that are permitted by the current license codes.</span></span>

```xpp
public static int maxSessionId()
```

### <a name="return-value---maxsessionid"></a><span data-ttu-id="0e511-340">戻り値 - maxSessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-340">Return Value - maxSessionId</span></span>

<span data-ttu-id="0e511-341">現在のライセンス コードで許可されているセッションの最大数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="0e511-341">An integer that indicates the maximum number of sessions that are permitted by the current license code.</span></span>

## <a name="method-numsession"></a><span data-ttu-id="0e511-342">メソッド numSession</span><span class="sxs-lookup"><span data-stu-id="0e511-342">Method numSession</span></span>

<span data-ttu-id="0e511-343">登録されているセッションの現在の番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-343">Retrieves the current number of registered sessions.</span></span>

```xpp
public static int numSession()
```

### <a name="return-value---numsession"></a><span data-ttu-id="0e511-344">戻り値 - numSession</span><span class="sxs-lookup"><span data-stu-id="0e511-344">Return Value - numSession</span></span>

<span data-ttu-id="0e511-345">現在登録されているセッションの数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="0e511-345">An integer that indicates the number of currently registered sessions.</span></span>

## <a name="method-preferredlocale"></a><span data-ttu-id="0e511-346">メソッド preferredLocale</span><span class="sxs-lookup"><span data-stu-id="0e511-346">Method preferredLocale</span></span>

```xpp
public PreferredLocale preferredLocale()
```

### <a name="return-value---preferredlocale"></a><span data-ttu-id="0e511-347">戻り値 - preferredLocale</span><span class="sxs-lookup"><span data-stu-id="0e511-347">Return Value - preferredLocale</span></span>

## <a name="method-pseudobandwidth"></a><span data-ttu-id="0e511-348">メソッド pseudoBandwidth</span><span class="sxs-lookup"><span data-stu-id="0e511-348">Method pseudoBandwidth</span></span>

<span data-ttu-id="0e511-349">セッションの帯域幅シミュレーションをオンにするかどうかを決定し、帯域幅シミュレーションをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="0e511-349">Determines whether bandwidth simulation is turned on for the session, and enables bandwidth simulation to be turned on or off.</span></span>

```xpp
public static int pseudoBandwidth([int bandwidth])
```

### <a name="parameters---pseudobandwidth"></a><span data-ttu-id="0e511-350">パラメーター - pseudoBandwidth</span><span class="sxs-lookup"><span data-stu-id="0e511-350">Parameters - pseudoBandwidth</span></span>

<span data-ttu-id="0e511-351">bandwidth</span><span class="sxs-lookup"><span data-stu-id="0e511-351">bandwidth</span></span>  
<span data-ttu-id="0e511-352">帯域幅のシミュレーションのオン/オフを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0e511-352">Turns bandwidth simulation on or off.</span></span> <span data-ttu-id="0e511-353">シミュレーションをオフにするには 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e511-353">Set to zero to turn simulation off.</span></span> <span data-ttu-id="0e511-354">その他の値は、シミュレーションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="0e511-354">Other values turn simulation on.</span></span>

### <a name="return-value---pseudobandwidth"></a><span data-ttu-id="0e511-355">戻り値 - pseudoBandwidth</span><span class="sxs-lookup"><span data-stu-id="0e511-355">Return Value - pseudoBandwidth</span></span>

<span data-ttu-id="0e511-356">帯域幅のシミュレーションを有効にするかどうかを示す整数。</span><span class="sxs-lookup"><span data-stu-id="0e511-356">An integer that indicates whether bandwidth simulation is turned on.</span></span> <span data-ttu-id="0e511-357">戻り値が 0 の場合、帯域幅シミュレーションはありません。</span><span class="sxs-lookup"><span data-stu-id="0e511-357">If the return value is zero, there is no bandwidth simulation.</span></span>

### <a name="remarks---pseudobandwidth"></a><span data-ttu-id="0e511-358">備考 - pseudoBandwidth</span><span class="sxs-lookup"><span data-stu-id="0e511-358">Remarks - pseudoBandwidth</span></span>

<span data-ttu-id="0e511-359">システム監視ツールからリモート接続の疑似シミュレーションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="0e511-359">You can run pseudo simulations of remote connections from the System monitoring tool:</span></span>

-   <span data-ttu-id="0e511-360">ツール バーで、ツールを選択し、開発ツールをポイントし、システム監視をポイントして、リモート接続タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e511-360">On the toolbar, select Tools, point to Development tools, point to System monitoring, and then click the Remote connection tab.</span></span>

## <a name="method-pseudolatency"></a><span data-ttu-id="0e511-361">メソッド pseudoLatency</span><span class="sxs-lookup"><span data-stu-id="0e511-361">Method pseudoLatency</span></span>

<span data-ttu-id="0e511-362">セッションの待機シミュレーションをオンにするかどうかを決定し、待機シミュレーションをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="0e511-362">Determines whether latency simulation is turned on for the session, and enables latency simulation to be turned on or off.</span></span>

```xpp
public static int pseudoLatency([int latency])
```

### <a name="parameters---pseudolatency"></a><span data-ttu-id="0e511-363">パラメーター - pseudoLatency</span><span class="sxs-lookup"><span data-stu-id="0e511-363">Parameters - pseudoLatency</span></span>

<span data-ttu-id="0e511-364">latency</span><span class="sxs-lookup"><span data-stu-id="0e511-364">latency</span></span>  
<span data-ttu-id="0e511-365">待機シミュレーションのオン/オフを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0e511-365">Turns latency simulation on or off.</span></span> <span data-ttu-id="0e511-366">シミュレーションをオフにするには 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e511-366">Set to zero to turn simulation off.</span></span> <span data-ttu-id="0e511-367">その他の値は、シミュレーションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="0e511-367">Other values turn simulation on.</span></span>

### <a name="return-value---pseudolatency"></a><span data-ttu-id="0e511-368">戻り値 - pseudoLatency</span><span class="sxs-lookup"><span data-stu-id="0e511-368">Return Value - pseudoLatency</span></span>

<span data-ttu-id="0e511-369">待機シミュレーションを有効にするかどうかを示す整数。</span><span class="sxs-lookup"><span data-stu-id="0e511-369">An integer that indicates whether latency simulation is turned on.</span></span> <span data-ttu-id="0e511-370">戻り値が 0 の場合、遅延シミュレーションはありません。</span><span class="sxs-lookup"><span data-stu-id="0e511-370">If the return value is zero, there is no latency simulation.</span></span>

### <a name="remarks---pseudolatency"></a><span data-ttu-id="0e511-371">備考 - pseudoLatency</span><span class="sxs-lookup"><span data-stu-id="0e511-371">Remarks - pseudoLatency</span></span>

<span data-ttu-id="0e511-372">システム監視ツールからリモート接続の疑似シミュレーションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="0e511-372">You can run pseudo simulations of remote connections from the System monitoring tool:</span></span>

-   <span data-ttu-id="0e511-373">ツール バーで、ツールを選択し、開発ツールをポイントし、システム監視をポイントして、リモート接続タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e511-373">On the toolbar, select Tools, point to Development tools, point to System monitoring, and then click the Remote connection tab</span></span>

## <a name="method-pseudosimmode"></a><span data-ttu-id="0e511-374">メソッド pseudoSimMode</span><span class="sxs-lookup"><span data-stu-id="0e511-374">Method pseudoSimMode</span></span>

<span data-ttu-id="0e511-375">セッションの遅延シミュレーションをオンにするかどうかを決定し、遅延シミュレーションをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="0e511-375">Determines whether delay simulation is turned on for the session, and enables delay simulation to be turned on or off.</span></span>

```xpp
public static int pseudoSimMode([int simMode])
```

### <a name="parameters---pseudosimmode"></a><span data-ttu-id="0e511-376">パラメーター - pseudoSimMode</span><span class="sxs-lookup"><span data-stu-id="0e511-376">Parameters - pseudoSimMode</span></span>

<span data-ttu-id="0e511-377">simMode</span><span class="sxs-lookup"><span data-stu-id="0e511-377">simMode</span></span>  
<span data-ttu-id="0e511-378">遅延シミュレーションのオン/オフを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0e511-378">Turns delay simulation on or off.</span></span> <span data-ttu-id="0e511-379">シミュレーションをオフにするには 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e511-379">Set to zero to turn simulation off.</span></span> <span data-ttu-id="0e511-380">アプリケーションの呼び出しで遅延をシミュレートするには 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="0e511-380">Set to 1 to simulate delays for application calls.</span></span> <span data-ttu-id="0e511-381">すべての呼び出しで遅延をシミュレートするには 2 に設定します。</span><span class="sxs-lookup"><span data-stu-id="0e511-381">Set to 2 to simulate delays for all calls.</span></span>

### <a name="return-value---pseudosimmode"></a><span data-ttu-id="0e511-382">戻り値 - pseudoSimMode</span><span class="sxs-lookup"><span data-stu-id="0e511-382">Return Value - pseudoSimMode</span></span>

<span data-ttu-id="0e511-383">遅延シミュレーションを有効にするかどうかを示す整数。</span><span class="sxs-lookup"><span data-stu-id="0e511-383">An integer that indicates whether delay simulation is turned on.</span></span> <span data-ttu-id="0e511-384">戻り値が 0 の場合、遅延シミュレーションはありません。</span><span class="sxs-lookup"><span data-stu-id="0e511-384">If the return value is zero, there is no delay simulation.</span></span> <span data-ttu-id="0e511-385">戻り値が 1 の場合は、遅延はアプリケーション制御の呼び出しに対してのみシミュレートされます。</span><span class="sxs-lookup"><span data-stu-id="0e511-385">If the return value is 1, delays are simulated only for application-controlled calls.</span></span> <span data-ttu-id="0e511-386">戻り値が 2 の場合は、遅延はすべての呼び出しに対してシミュレートされます。</span><span class="sxs-lookup"><span data-stu-id="0e511-386">If the return value is 2, delays are simulated for all calls.</span></span>

### <a name="remarks---pseudosimmode"></a><span data-ttu-id="0e511-387">備考 - pseudoSimMode</span><span class="sxs-lookup"><span data-stu-id="0e511-387">Remarks - pseudoSimMode</span></span>

<span data-ttu-id="0e511-388">システム監視ツールからリモート接続の疑似シミュレーションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="0e511-388">You can run pseudo simulations of remote connections from the System monitoring tool:</span></span>

-   <span data-ttu-id="0e511-389">ツール バーで、ツールを選択し、開発ツールをポイントし、システム監視をポイントして、リモート接続タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e511-389">On the toolbar, select Tools, point to Development tools, point to System monitoring, and then click the Remote connection tab</span></span>

## <a name="method-systemsessionid"></a><span data-ttu-id="0e511-390">メソッド systemSessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-390">Method systemSessionId</span></span>

<span data-ttu-id="0e511-391">xSession オブジェクトの対象となるセッションのシステム セッション ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-391">Retrieves the system session ID for the session that the xSession object covers.</span></span>

```xpp
public static int systemSessionId()
```

### <a name="return-value---systemsessionid"></a><span data-ttu-id="0e511-392">戻り値 - systemSessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-392">Return Value - systemSessionId</span></span>

<span data-ttu-id="0e511-393">セッション ID を表す整数。</span><span class="sxs-lookup"><span data-stu-id="0e511-393">An integer that represents the session ID.</span></span>

### <a name="remarks---systemsessionid"></a><span data-ttu-id="0e511-394">備考 - systemSessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-394">Remarks - systemSessionId</span></span>

<span data-ttu-id="0e511-395">COM セッションまたはワーカー スレッド セッションなどの一部のセッションには、親システム セッションがあります。</span><span class="sxs-lookup"><span data-stu-id="0e511-395">Some sessions, such as a COM session or a worker thread session, have a parent system session.</span></span>

## <a name="method-xppcallstack"></a><span data-ttu-id="0e511-396">メソッド xppCallStack</span><span class="sxs-lookup"><span data-stu-id="0e511-396">Method xppCallStack</span></span>

<span data-ttu-id="0e511-397">現在の呼び出し履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e511-397">Retrieves the current call stack.</span></span>

```xpp
public static container xppCallStack()
```

### <a name="return-value---xppcallstack"></a><span data-ttu-id="0e511-398">戻り値 - xppCallStack</span><span class="sxs-lookup"><span data-stu-id="0e511-398">Return Value - xppCallStack</span></span>

<span data-ttu-id="0e511-399">現在のコール スタックの内容を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="0e511-399">A container that holds the contents of the current call stack.</span></span>

## <a name="method-removeaoc"></a><span data-ttu-id="0e511-400">メソッド removeAOC</span><span class="sxs-lookup"><span data-stu-id="0e511-400">Method removeAOC</span></span>

<span data-ttu-id="0e511-401">現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を削除します。</span><span class="sxs-lookup"><span data-stu-id="0e511-401">Removes the Application Object Server client-side cache (AOC) for the current session.</span></span>

```xpp
public static void removeAOC()
```

## <a name="method-updateaoc"></a><span data-ttu-id="0e511-402">メソッド updateAOC</span><span class="sxs-lookup"><span data-stu-id="0e511-402">Method updateAOC</span></span>

<span data-ttu-id="0e511-403">現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を更新します。</span><span class="sxs-lookup"><span data-stu-id="0e511-403">Updates the Application Object Server client-side cache (AOC) for the current session.</span></span>

```xpp
public static void updateAOC()
```

### <a name="remarks---updateaoc"></a><span data-ttu-id="0e511-404">備考 - updateAOC</span><span class="sxs-lookup"><span data-stu-id="0e511-404">Remarks - updateAOC</span></span>

<span data-ttu-id="0e511-405">AOC は、クライアントによってロードされるメタデータで構成されるクライアント側のキャッシュであり、クライアントを閉じると、ディスクに保存されます。</span><span class="sxs-lookup"><span data-stu-id="0e511-405">AOC is a client-side cache that consists of metadata that is loaded by the client, and then saved to disk when the client is closed.</span></span> <span data-ttu-id="0e511-406">これはユーザーのローカル設定フォルダーで保存されます。</span><span class="sxs-lookup"><span data-stu-id="0e511-406">It is saved under the user�s local settings folder.</span></span> <span data-ttu-id="0e511-407">このファイルの拡張子は .auc で、ユーザーのローカル設定フォルダーに保存されます。</span><span class="sxs-lookup"><span data-stu-id="0e511-407">The file has an .auc filename extension and is saved in a user's Local Settings folder.</span></span> <span data-ttu-id="0e511-408">クライアントは、起動されると、キャッシュからの読み取りの後、ディスクからそのキャッシュを削除します。</span><span class="sxs-lookup"><span data-stu-id="0e511-408">When the client is started, it reads from the cache, and then deletes the cache from the disk.</span></span>

## <a name="method-setautoupdaterecversion"></a><span data-ttu-id="0e511-409">メソッド setAutoUpdateRecVersion</span><span class="sxs-lookup"><span data-stu-id="0e511-409">Method setAutoUpdateRecVersion</span></span>

```xpp
public static void setAutoUpdateRecVersion(boolean autoUpdateRecVersion)
```

### <a name="parameters---setautoupdaterecversion"></a><span data-ttu-id="0e511-410">パラメーター - setAutoUpdateRecVersion</span><span class="sxs-lookup"><span data-stu-id="0e511-410">Parameters - setAutoUpdateRecVersion</span></span>

<span data-ttu-id="0e511-411">autoUpdateRecVersion</span><span class="sxs-lookup"><span data-stu-id="0e511-411">autoUpdateRecVersion</span></span>  

## <a name="method-setsystraceactive"></a><span data-ttu-id="0e511-412">メソッド setSysTraceActive</span><span class="sxs-lookup"><span data-stu-id="0e511-412">Method setSysTraceActive</span></span>

<span data-ttu-id="0e511-413">システム追跡のオンまたはオフを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0e511-413">Switches system tracing on or off.</span></span>

```xpp
public static void setSysTraceActive(boolean nValue)
```

### <a name="parameters---setsystraceactive"></a><span data-ttu-id="0e511-414">パラメーター - setSysTraceActive</span><span class="sxs-lookup"><span data-stu-id="0e511-414">Parameters - setSysTraceActive</span></span>

<span data-ttu-id="0e511-415">nValue</span><span class="sxs-lookup"><span data-stu-id="0e511-415">nValue</span></span>  
<span data-ttu-id="0e511-416">追跡をオンまたはオフに切り替える必要があるかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="0e511-416">A Boolean value that determines whether tracing should be switched on or off.</span></span> <span data-ttu-id="0e511-417">追跡をオンにするには、true に設定します。</span><span class="sxs-lookup"><span data-stu-id="0e511-417">Set to true to switch tracing on.</span></span>

### <a name="examples---setsystraceactive"></a><span data-ttu-id="0e511-418">例 - setSysTraceActive</span><span class="sxs-lookup"><span data-stu-id="0e511-418">Examples - setSysTraceActive</span></span>

<span data-ttu-id="0e511-419">次の例では、データのインポート時に setSysTraceActive メソッドを使用してシステム トレースをオフにします。</span><span class="sxs-lookup"><span data-stu-id="0e511-419">The following example uses the setSysTraceActive method to turn system tracing off when data is imported.</span></span>

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

## <a name="method-clientsetautoupdaterecversion"></a><span data-ttu-id="0e511-420">メソッド clientSetAutoUpdateRecVersion</span><span class="sxs-lookup"><span data-stu-id="0e511-420">Method clientSetAutoUpdateRecVersion</span></span>

```xpp
private static void clientSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)
```

### <a name="parameters---clientsetautoupdaterecversion"></a><span data-ttu-id="0e511-421">パラメーター - clientSetAutoUpdateRecVersion</span><span class="sxs-lookup"><span data-stu-id="0e511-421">Parameters - clientSetAutoUpdateRecVersion</span></span>

<span data-ttu-id="0e511-422">autoUpdateRecVersion</span><span class="sxs-lookup"><span data-stu-id="0e511-422">autoUpdateRecVersion</span></span>  

## <a name="method-serversetautoupdaterecversion"></a><span data-ttu-id="0e511-423">メソッド serverSetAutoUpdateRecVersion</span><span class="sxs-lookup"><span data-stu-id="0e511-423">Method serverSetAutoUpdateRecVersion</span></span>

```xpp
private static void serverSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)
```

### <a name="parameters---serversetautoupdaterecversion"></a><span data-ttu-id="0e511-424">パラメーター - serverSetAutoUpdateRecVersion</span><span class="sxs-lookup"><span data-stu-id="0e511-424">Parameters - serverSetAutoUpdateRecVersion</span></span>

<span data-ttu-id="0e511-425">autoUpdateRecVersion</span><span class="sxs-lookup"><span data-stu-id="0e511-425">autoUpdateRecVersion</span></span>  

## <a name="method-new"></a><span data-ttu-id="0e511-426">メソッド new</span><span class="sxs-lookup"><span data-stu-id="0e511-426">Method new</span></span>

<span data-ttu-id="0e511-427">現在のセッションまたはパラメーターとして渡されたセッション ID のいずれかに対して xSession オブジェクトのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e511-427">Instantiates the xSession object, either for current session or for the session ID passed in as a parameter.</span></span>

```xpp
public void new([int sessionId], [boolean checkSession])
```

### <a name="parameters---new"></a><span data-ttu-id="0e511-428">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="0e511-428">Parameters - new</span></span>

<span data-ttu-id="0e511-429">sessionId</span><span class="sxs-lookup"><span data-stu-id="0e511-429">sessionId</span></span>  
<span data-ttu-id="0e511-430">true に設定すると\_SessionId パラメーターで指定されたセッションが存在するかどうかを確認するブール フラグ。</span><span class="sxs-lookup"><span data-stu-id="0e511-430">A boolean flag that, if set to true, checks to determine whether the session specified by the \_SessionId parameter exists.</span></span> <span data-ttu-id="0e511-431">セッションが存在するかどうかを確認する操作は、多くのシステムリソースを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0e511-431">The operation that checks whether a session exists might use a lot of system resources.</span></span> <span data-ttu-id="0e511-432">したがって、このパラメーターは既定で false に設定されています。</span><span class="sxs-lookup"><span data-stu-id="0e511-432">This parameter is therefore set to false by default.</span></span>

<!-- -->

<span data-ttu-id="0e511-433">checkSession</span><span class="sxs-lookup"><span data-stu-id="0e511-433">checkSession</span></span>  
<span data-ttu-id="0e511-434">true に設定すると\_SessionId パラメーターで指定されたセッションが存在するかどうかを確認するブール フラグ。</span><span class="sxs-lookup"><span data-stu-id="0e511-434">A boolean flag that, if set to true, checks to determine whether the session specified by the \_SessionId parameter exists.</span></span> <span data-ttu-id="0e511-435">セッションが存在するかどうかを確認する操作は、多くのシステムリソースを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0e511-435">The operation that checks whether a session exists might use a lot of system resources.</span></span> <span data-ttu-id="0e511-436">したがって、このパラメーターは既定で false に設定されています。</span><span class="sxs-lookup"><span data-stu-id="0e511-436">This parameter is therefore set to false by default.</span></span>

### <a name="examples---new"></a><span data-ttu-id="0e511-437">例 - new</span><span class="sxs-lookup"><span data-stu-id="0e511-437">Examples - new</span></span>

<span data-ttu-id="0e511-438">次の例は、すべての有効なセッションの数を返します。</span><span class="sxs-lookup"><span data-stu-id="0e511-438">The following example returns a count of all the active sessions.</span></span>

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

## <a name="method-reloadtablecollectiononclient"></a><span data-ttu-id="0e511-439">メソッド reloadTableCollectionOnClient</span><span class="sxs-lookup"><span data-stu-id="0e511-439">Method reloadTableCollectionOnClient</span></span>

```xpp
public static void reloadTableCollectionOnClient()
```

