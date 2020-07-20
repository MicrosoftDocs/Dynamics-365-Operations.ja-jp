---
title: xInfo クラス
description: このトピックでは、xInfo クラスについて説明します。
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
ms.openlocfilehash: 245a4d3cd0c6faa4cf9090114748d3ce112155cc
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502763"
---
# <a name="class-xinfo"></a>クラス xInfo

[!include [banner](../../includes/banner.md)]

```xpp
class xInfo extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                       | 説明                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int removeMessage(Int64 messageId)                                                                                                                                                                    |                                                                                                                                                                                         |
| public Int64 insertMessage(MessageSeverity type, str message)                                                                                                                                                |                                                                                                                                                                                         |
| public Exception add(Exception exceptionType, str string, \[str helpURL\], \[Object obj\], \[boolean buildprefix\])                                                                                          | 情報ログ バッファに文字列を追加します。                                                                                                                                                    |
| public Exception addException(str string, str stackTrace)                                                                                                                                                    |                                                                                                                                                                                         |
| public container breakpoint(\[container breakpoint\])                                                                                                                                                        | ブレークポイントに関する情報を取得または設定します。                                                                                                                                             |
| public boolean canShowCreateRuleMenuItem(xFormRun caller)                                                                                                                                                    | フォームの警告ルール作成フォームのメニュー項目を表示するかどうかを決定します。                                                                                         |
| public boolean canShutdown(boolean silent)                                                                                                                                                                   | システムをシャットダウンできるかどうかをテストします。 このメソッドを使用しないでください。 代わりに、Info クラスでオーバーライドされたバージョンを使用します。                                                        |
| public boolean canViewAlertInbox()                                                                                                                                                                           | 現在のユーザーに警告の表示フォームを表示するアクセス許可があるかどうかを判断します。                                                                                                        |
| public xCompilerOutput compilerOutput(\[Object compilerOut\])                                                                                                                                                | コンパイラ出力オブジェクトを取得または設定します。 コンパイラ出力オブジェクトは、デフォルトでコンパイラ出力ウィンドウです。                                                                           |
| public container copy(int from, int to)                                                                                                                                                                      | 情報ログ バッファーから行をコピーします。                                                                                                                                                   |
| public int createDevelopmentWorkspaceWindow()                                                                                                                                                                |                                                                                                                                                                                         |
| public int createWorkspaceWindow()                                                                                                                                                                           | 新しいワークスペース ウィンドウを開きます。 たとえば、これにより、異なるウィンドウでアプリケーション オブジェクトの異なるセットを開く、または会社コードの 2 つの異なるセットを使用することができます。 |
| public UtilEntryLevel currentAOLayer()                                                                                                                                                                       | SYS または USR などで実行している現在の階層を取得します。                                                                                                                     |
| public container cut(int from, int to)                                                                                                                                                                       | 情報ログ バッファーから行を切り取りします。                                                                                                                                                     |
| public str documentationLanguage(\[str languageCode\])                                                                                                                                                       | ドキュメントに使用される言語を取得または設定します。                                                                                                     |
| public container export()                                                                                                                                                                                    |                                                                                                                                                                                         |
| public TreeNode findNode(str nodePath)                                                                                                                                                                       | 指定されたツリー ノードを取得します。                                                                                                                                                    |
| public TreeNode getDocNode(UtilFileType helpType, int UtilType, str Name, \[UtilElementId ParentId\], \[int Type\], \[UtilEntryLevel UtilLevel\], \[boolean ForceLevel\], \[int Mode\], \[boolean OldUtil\]) | AOT から指定したドキュメント ノードを取得します。                                                                                                                               |
| public TreeNode getImportedNode(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)                                                                                    | XPO ファイルからツリー ノードのインスタンスを作成しますが、AOT にインポートしません。 たとえば、これにより、同じツリー ノードの別のバージョンと比較できます。         |
| public TreeNode getNode(UtilElementType UtilType, str Name, \[UtilElementId ParentId\], \[int Type\], \[UtilEntryLevel Utillevel\], \[boolean Forcelevel\], \[int Mode\], \[boolean OldUtil\])               | AOT 内のノードに対応するツリー ノードを取得します。                                                                                                                            |
| public int getNodeResid(UtilElementType nodeType)                                                                                                                                                            | 指定したタイプのノードを表示するために使用されるアイコンのリソース ID を取得します。                                                                                             |
| public Struct getTaskInfo(int taskNumber)                                                                                                                                                                    |                                                                                                                                                                                         |
| public UserSetup getUserSetup()                                                                                                                                                                              | ユーザー パラメーターを設定するために使用する UserSetup オブジェクトを取得します。                                                                                                                       |
| public container getWorkspaceList()                                                                                                                                                                          |                                                                                                                                                                                         |
| public int hWnd(\[int workspaceNum\])                                                                                                                                                                        | ナビゲーション ペイン ウィンドウのハンドルを取得します。                                                                                                                  |
| public boolean import(container infologContainer, \[boolean clearExistingInfolog\])                                                                                                                          |                                                                                                                                                                                         |
| public int importElement(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)                                                                                           | インポートする対象を指定します。                                                                                                                                                    |
| public int importString(str source, UtilElementType kind, str name)                                                                                                                                          | ファイルからオブジェクトをインポートします。                                                                                                                                                          |
| public int instance()                                                                                                                                                                                        | アプリケーションの現在のインスタンスへのハンドルを取得します。                                                                                                                          |
| public str isoCurrencyCode(\[str code\])                                                                                                                                                                     | 通貨コードを取得または設定します。                                                                                                                                                         |
| public boolean IsVisible()                                                                                                                                                                                   | クライアントのウィンドウが最小化されていないかどうかを決定します。                                                                                                                                  |
| public str language(\[str languageCode\])                                                                                                                                                                    | GUI の言語を取得または設定します。                                                                                                                                                  |
| public Exception level(int line)                                                                                                                                                                             | 情報ログ バッファー内の行の例外レベルを取得します。                                                                                                                          |
| public int line()                                                                                                                                                                                            | 情報ログ バッファの明細行の数を取得します。                                                                                                                                    |
| public MessageWin messageWin()                                                                                                                                                                               | Infolog から Message ウィンドウに出力を送信できます。                                                                                                                      |
| public Real nationalCurrencyFactor(\[Real factor\])                                                                                                                                                          |                                                                                                                                                                                         |
| public str nationalCurrencyPostfix(\[str string\])                                                                                                                                                           |                                                                                                                                                                                         |
| public str nationalCurrencyPrefix(\[str string\])                                                                                                                                                            |                                                                                                                                                                                         |
| public xNavPane navPane()                                                                                                                                                                                    | プライマリ ナビゲーション コントロール クラスの xNavPane オブジェクトを取得します。                                                                                                                     |
| public int num(\[Exception exceptionType\])                                                                                                                                                                  | 情報ログ バッファにおける指定した型の例外の数を取得します。                                                                                                         |
| public int prevInstance()                                                                                                                                                                                    | アプリケーションの前のインスタンスへのハンドルを取得します。                                                                                                                         |
| public int processId()                                                                                                                                                                                       | プロセスの ID を取得します。                                                                                                                                 |
| public TreeNode projectRootNode()                                                                                                                                                                            | X++ プロジェクト ノードを返します。                                                                                                                                                          |
| public TreeNode rootNode()                                                                                                                                                                                   | アプリケーション オブジェクト ツリーのルートを取得します。                                                                                                                                      |
| public int startImport(str file, int flag, \[str labelSubstitutes\])                                                                                                                                         | インポート コンテキストを作成します。                                                                                                                                                              |
| public str text(\[int line\])                                                                                                                                                                                | 情報ログからテキストの行を取得します。                                                                                                                                              |
| public TreeNode userNode()                                                                                                                                                                                   |                                                                                                                                                                                         |
| public AnyType webSession(\[AnyType value\])                                                                                                                                                                 |                                                                                                                                                                                         |
| ::public static container activeXControls()                                                                                                                                                                  | ActiveX コントロールの一覧を取得します。                                                                                                             |
| ::public static str AOTLogDirectory()                                                                                                                                                                        | 現在のインストールのログ ディレクトリへのパスを取得します。                                                                                                                        |
| ::public static container automationObjects()                                                                                                                                                                | 使用可能な COM オブジェクトの一覧を取得します。                                                                                                          |
| ::public static str buildNo()                                                                                                                                                                                | 現在の実行可能ファイルのカーネル ビルド番号を取得します。                                                                                                      |
| ::public static str compilationDate()                                                                                                                                                                        | 現在のバージョンが最後にコンパイルされた日付を取得します。                                                                                             |
| ::public static str compilationTime()                                                                                                                                                                        | 現在のバージョンが最後にコンパイルされた時刻を取得します。                                                                                             |
| ::public static str componentName()                                                                                                                                                                          | コンポーネントへのパスを取得します。                                                                                                                                                    |
| ::public static str configuration()                                                                                                                                                                          | 現在のクライアント構成を取得します。                                                                                                                                             |
| ::public static int currentWorkspaceNum()                                                                                                                                                                    | 現在のワークスペースのアプリケーション ウィンドウ ID を取得します。                                                                                                                           |
| ::public static str directory(DirectoryType type)                                                                                                                                                            | クライアントがインストールされているディレクトリへのパスを取得します。                                                                                          |
| ::public static Date expireDate()                                                                                                                                                                            | 現在のインストールのライセンスの有効期限が切れる日付を取得します。                                                                                                           |
| ::public static ApplicationObjectTreeWindow getApplicationObjectTreeWindow()                                                                                                                                 |                                                                                                                                                                                         |
| ::public static int getCurrentModelId()                                                                                                                                                                      |                                                                                                                                                                                         |
| ::public static int getNumberOfDecimals(Real number)                                                                                                                                                         | 指定された数値の小数点以下の桁数を取得します。                                                                                                                         |
| ::public static PropertiesWindow getPropertiesWindow()                                                                                                                                                       |                                                                                                                                                                                         |
| ::public static int getSystemGeneratedModelId(UtilEntryLevel layer)                                                                                                                                          |                                                                                                                                                                                         |
| ::public static str licenseName()                                                                                                                                                                            | 現在のライセンスの名前を取得します。                                                                                                                        |
| ::public static str productName()                                                                                                                                                                            | 製品の名前を取得します。                                                                                                                                                      |
| ::public static str productRegisteredName()                                                                                                                                                                  |                                                                                                                                                                                         |
| ::public static str releaseVersion()                                                                                                                                                                         | 現在の実行可能ファイルのバージョン番号を取得します。例: 3.0、4.0。                                                                                 |
| ::public static str releaseYear()                                                                                                                                                                            |                                                                                                                                                                                         |
| ::public static str serialNo()                                                                                                                                                                               | 現在のライセンスのシリアル番号を取得します。                                                                                                               |
| public void new()                                                                                                                                                                                            | 新しい xInfo オブジェクトを初期化します。                                                                                                                                                         |
| public void workspaceWindowDestroyed(int hWnd)                                                                                                                                                               | 新しいワークスペースが終了した時に実行します。                                                                                                                                                    |
| public void writeCustomStatlineItem(str text)                                                                                                                                                                | テキストの行をステータス バーに記述します。                                                                                                                                                |
| public void reloadRunningMode()                                                                                                                                                                              |                                                                                                                                                                                         |
| public void setWindowOrder(int window, \[int afterWindow\])                                                                                                                                                  | Windows の表示順序を設定します。                                                                                                                                    |
| public void shutDown(boolean force)                                                                                                                                                                          | クライアントをシャットダウンします。                                                                                                                                                                  |
| public void xref(str path, xRef x)                                                                                                                                                                           | 相互参照システムが使用される時に実行します。                                                                                                                                       |
| public void updateCurrentCompany()                                                                                                                                                                           |                                                                                                                                                                                         |
| public void redrawAllWindows()                                                                                                                                                                               | すべてのウィンドウを再描画します。                                                                                                                                                                    |
| public void formNotify(xFormRun form, FormNotify notification, \[FormNotifyEventArgs formNotifyEventArgs\])                                                                                                  | 特定フォームへの変更特定タイプに基づいて実行し、カスタムコードの実行を許可します。                                                                                          |
| public void mayReloadMenu(boolean value)                                                                                                                                                                     | UI を更新できないようにする                                                                                                                                                        |
| public void startLengthyOperation()                                                                                                                                                                          | マウス カーソルをアイドルに設定します。                                                                                                                                                          |
| public void breakpointNotify(BreakpointNotify notification)                                                                                                                                                  | ブレークポイントが変更されたときの通知システムを実装します。                                                                                                                          |
| public void initializeInfolog(int window)                                                                                                                                                                    |                                                                                                                                                                                         |
| public void startup(str startupCmd)                                                                                                                                                                          | クライアントの起動時に実行します。                                                                                                                                                        |
| public void endImport(int id, int elements)                                                                                                                                                                  | インポート プロセスを完了します。                                                                                                                                                            |
| public void yield()                                                                                                                                                                                          |                                                                                                                                                                                         |
| public void viewAlertInbox(\[int selectedTab\])                                                                                                                                                              | 警告の表示フォームを起動します。                                                                                                                                                          |
| public void reportSendMailServer(PrintJobSettings settings)                                                                                                                                                  |                                                                                                                                                                                         |
| public void endLengthyOperation(\[boolean endAll\])                                                                                                                                                          | startLengthyOperation の呼び出し後にマウス カーソルが標準に戻るように設定します。                                                                                                             |
| public void setNumUnreadAlerts(\[int n\])                                                                                                                                                                    | 未読の警告メールの数が変わると、ステータス バーのテキストを更新します。                                                                                                          |
| public void truncate(str prefix)                                                                                                                                                                             | 情報ログから指定した接頭語の付いた品目を削除します。                                                                                                                           |
| public void formNoteButton(boolean enable, boolean value)                                                                                                                                                    | ツールバーのドキュメント処理ボタンをコントロールします。                                                                                                                                   |
| public void viewCreateRuleDialog(xFormRun caller)                                                                                                                                                            | 警告ルールの作成フォームを起動します。                                                                                                                                                    |
| public void view(\[container container\])                                                                                                                                                                    |                                                                                                                                                                                         |
| public void clear(\[int linesLeft\])                                                                                                                                                                         | 情報ログ バッファーから行を削除します。                                                                                                                                                  |
| public void workspaceWindowCreated(int hWnd)                                                                                                                                                                 | 新しいワークスペースが作成された時に実行します。                                                                                                                                               |
| ::public static void setCurrentModelId(int currentModelId)                                                                                                                                                   |                                                                                                                                                                                         |
| public void activateMenubarTask(int command)                                                                                                                                                                 |                                                                                                                                                                                         |
| public void finalize()                                                                                                                                                                                       |                                                                                                                                                                                         |
| public void insertXReferences()                                                                                                                                                                              |                                                                                                                                                                                         |
| public void activateButton(int command)                                                                                                                                                                      |                                                                                                                                                                                         |
| public void activateWindow(int window)                                                                                                                                                                       | フォームまたはウィンドウにフォーカスを設定します。                                                                                                                                                     |
| public void reportSendMail(PrintJobSettings settings)                                                                                                                                                        | レポートを電子メールで送信するための設定を生成します。                                                                                                                                   |

## <a name="method-removemessage"></a>メソッド removeMessage

```xpp
public int removeMessage(Int64 messageId)
```

### <a name="parameters---removemessage"></a>パラメーター - removeMessage

messageId  

### <a name="return-value---removemessage"></a>戻り値 - removeMessage

## <a name="method-insertmessage"></a>メソッド insertMessage

```xpp
public Int64 insertMessage(MessageSeverity type, str message)
```

### <a name="parameters---insertmessage"></a>パラメーター - insertMessage

タイプ  

<!-- -->

メッセージ  

### <a name="return-value---insertmessage"></a>戻り値 - insertMessage

## <a name="method-add"></a>メソッド add

情報ログ バッファに文字列を追加します。

```xpp
public Exception add(Exception exceptionType, str string, [str helpURL], [Object obj], [boolean buildprefix])
```

### <a name="parameters---add"></a>パラメーター - add

exceptionType  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

<!-- -->

string  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

<!-- -->

helpURL  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

<!-- -->

obj  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

<!-- -->

buildprefix  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

### <a name="return-value---add"></a>戻り値 - add

例外システム列挙値です。 詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。

### <a name="remarks---add"></a>備考 - add

helpURL パラメーターの値の例は、「KernDoc:\\\\\\\\ 機能 \\\\substr」です。 このメソッドは直接使用しないでください。 代わりに、infolog.info、infolog.warning、infolog.error、または infolog.checkFailed メソッドを使用します。 ExceptionType パラメーターの詳細については、トライおよびキャッチ キーワードで例外処理を参照してください。

## <a name="method-addexception"></a>メソッド addException

```xpp
public Exception addException(str string, str stackTrace)
```

### <a name="parameters---addexception"></a>パラメーター - addException

文字列  

<!-- -->

stackTrace  

### <a name="return-value---addexception"></a>戻り値 - addException

## <a name="method-breakpoint"></a>メソッド breakpoint

ブレークポイントに関する情報を取得または設定します。

```xpp
public container breakpoint([container breakpoint])
```

### <a name="parameters---breakpoint"></a>パラメーター - breakpoint

ブレークポイント  
現在のブレークポイントに関する情報を保持するコンテナーです。

### <a name="return-value---breakpoint"></a>戻り値 - breakpoint

現在のブレークポイントに関する情報を保持するコンテナーです。

### <a name="remarks---breakpoint"></a>備考 - breakpoint

ブレークポイントに関する情報を保持するコンテナーの形式は次のとおりです。

-   項目 1: バージョン番号
-   項目 2 - 4、5-7、n - n+2: 以下で構成される各ブレークポイントに関する情報:

```xpp
-   the AOT path
-   the line number on which the breakpoint is set
-   whether the breakpoint is enabled or disabled
```

アプリケーションで、このメソッドはブレークポイント フォームで使用されます。 このフォームは、開いているときに、フォームに対して getBreakpoints メソッドを呼び出します。 これは、xInfo.breakpoint メソッドを呼び出し、ブレークポイント情報を持つコンテナーをパラメーターとして使用します。 ブレークポイントを無効にするとき、有効にするとき、またはフォームから削除するとき、setBreakpoints メソッドが呼び出されます。 これにより、ブレークポイントに関する情報が更新され、ブレークポイント パラメーターを使用せずに xInfo.breakpoint メソッドを使用してコンテナーとして返されます。 コンテナーは、コード エディター ウィンドウのブレークポイント情報を更新するために使用されます。

## <a name="method-canshowcreaterulemenuitem"></a>メソッド canShowCreateRuleMenuItem

フォームの警告ルール作成フォームのメニュー項目を表示するかどうかを決定します。

```xpp
public boolean canShowCreateRuleMenuItem(xFormRun caller)
```

### <a name="parameters---canshowcreaterulemenuitem"></a>パラメーター - canShowCreateRuleMenuItem

caller  
現在のフォーム: 警告ルールの作成メニュー項目が表示されるフォーム。

### <a name="return-value---canshowcreaterulemenuitem"></a>戻り値 - canShowCreateRuleMenuItem

現在のフォームが警告の作成をサポートする場合は true。それ以外の場合は false。

## <a name="method-canshutdown"></a>メソッド canShutdown

システムをシャットダウンできるかどうかをテストします。 このメソッドを使用しないでください。 代わりに、Info クラスでオーバーライドされたバージョンを使用します。

```xpp
public boolean canShutdown(boolean silent)
```

### <a name="parameters---canshutdown"></a>パラメーター - canShutdown

silent  
ユーザーがシステムを終了したいか尋ねるかどうかを決定するブール値。

### <a name="return-value---canshutdown"></a>戻り値 - canShutdown

システムをシャットダウンすることができる場合は true。それ以外の場合は、false。

## <a name="method-canviewalertinbox"></a>メソッド canViewAlertInbox

現在のユーザーに警告の表示フォームを表示するアクセス許可があるかどうかを判断します。

```xpp
public boolean canViewAlertInbox()
```

### <a name="return-value---canviewalertinbox"></a>戻り値 - canViewAlertInbox

ユーザーがフォームを表示するためのアクセス許可を持つ場合は true。それ以外の場合は、false。

### <a name="remarks---canviewalertinbox"></a>備考 - canViewAlertInbox

xInfo.viewAlertInbox を呼び出す前に、このメソッドを呼び出します。

## <a name="method-compileroutput"></a>メソッド compilerOutput

コンパイラ出力オブジェクトを取得または設定します。 コンパイラ出力オブジェクトは、デフォルトでコンパイラ出力ウィンドウです。

```xpp
public xCompilerOutput compilerOutput([Object compilerOut])
```

### <a name="parameters---compileroutput"></a>パラメーター - compilerOutput

compilerOut  
コンパイラ出力オブジェクト; オプション。 オプションのパラメーター。

### <a name="return-value---compileroutput"></a>戻り値 - compilerOutput

xCompilerOutput オブジェクト。

### <a name="remarks---compileroutput"></a>備考 - compilerOutput

compilerOut パラメーターの既定値は、コンパイラ出力ウィンドウですが、メッセージ ウィンドウでもあります。

## <a name="method-copy"></a>メソッド copy

情報ログ バッファーから行をコピーします。

```xpp
public container copy(int from, int to)
```

### <a name="parameters---copy"></a>パラメーター - copy

投稿者  
コピーする最後の行。

<!-- -->

終了日  
コピーする最後の行。

### <a name="return-value---copy"></a>戻り値 - copy

開始日と終了の間の情報ログ行を含むコンテナー。

### <a name="examples---copy"></a>例 - copy

次の例では、copy メソッドを使用して、情報ログの内容をログにコピーします。

```xpp
boolean validateRecord() 
{ 
    boolean     ok = true; 
    ok = intrastat.validateRecord(); 
    if (ok) 
        intrastat.log = ''; 
    else 
    { 
        intrastat.log = Info::infoCon2Str( 
            infolog.copy(infoLogCounter+1,infolog.num())); 
        infoLogCounter = infolog.num(); 
        errorFound = true; 
    } 
    intrastat.update(); 
    return ok; 
}
```

## <a name="method-createdevelopmentworkspacewindow"></a>メソッド createDevelopmentWorkspaceWindow

```xpp
public int createDevelopmentWorkspaceWindow()
```

### <a name="return-value---createdevelopmentworkspacewindow"></a>戻り値 - createDevelopmentWorkspaceWindow

## <a name="method-createworkspacewindow"></a>メソッド createWorkspaceWindow

新しいワークスペース ウィンドウを開きます。 たとえば、これにより、異なるウィンドウでアプリケーション オブジェクトの異なるセットを開く、または会社コードの 2 つの異なるセットを使用することができます。

```xpp
public int createWorkspaceWindow()
```

### <a name="return-value---createworkspacewindow"></a>戻り値 - createWorkspaceWindow

新規のウィンドウにハンドルを返します。

## <a name="method-currentaolayer"></a>メソッド currentAOLayer

SYS または USR などで実行している現在の階層を取得します。

```xpp
public UtilEntryLevel currentAOLayer()
```

### <a name="return-value---currentaolayer"></a>戻り値 - currentAOLayer

作業中の現在のレイヤーを示す UtilEntryLevel システム列挙値。

### <a name="remarks---currentaolayer"></a>備考 - currentAOLayer

詳細については、「レイヤー」を参照してください。

## <a name="method-cut"></a>メソッド cut

情報ログ バッファーから行を切り取りします。

```xpp
public container cut(int from, int to)
```

### <a name="parameters---cut"></a>パラメーター - cut

投稿者  
カットする最後の行。

<!-- -->

終了日  
カットする最後の行。

### <a name="return-value---cut"></a>戻り値 - cut

「～から」と「～へ」のパラメーターで指定された行の間の情報ログ行を保持するコンテナーです。

### <a name="examples---cut"></a>例 - cut

次の例では、fromLine 値で指定された行から最後の行まで Infolog の行を切り取ります。

```xpp
private void cutInfolog(int fromLine) 
{ 
    infolog.cut(fromLine+1, Global::infologLine()); 
}
```

## <a name="method-documentationlanguage"></a>メソッド documentationLanguage

ドキュメントに使用される言語を取得または設定します。

```xpp
public str documentationLanguage([str languageCode])
```

### <a name="parameters---documentationlanguage"></a>パラメーター - documentationLanguage

languageCode  
設定する言語の ID。オプション。

### <a name="return-value---documentationlanguage"></a>戻り値 - documentationLanguage

ドキュメントに現在使用されている言語の ID。

### <a name="remarks---documentationlanguage"></a>備考 - documentationLanguage

GUI の言語を設定するには、xInfo.language メソッドを使用します。 特定のセッションのドキュメント言語を設定するには、xSession.documentationLanguage メソッドを使用します。 languageCode パラメーターの値の例は「en-us」で、英語 (US) の言語に設定されます。

## <a name="method-export"></a>メソッド export

```xpp
public container export()
```

### <a name="return-value---export"></a>戻り値 - export

## <a name="method-findnode"></a>メソッド findNode

指定されたツリー ノードを取得します。

```xpp
public TreeNode findNode(str nodePath)
```

### <a name="parameters---findnode"></a>パラメーター - findNode

nodePath  
ノードへのパスを含む文字列。

### <a name="return-value---findnode"></a>戻り値 - findNode

nodePath パラメーターで指定されるツリー ノードを返します。

### <a name="remarks---findnode"></a>備考 - findNode

 メソッドは廃止されています。 代わりに TreeNode::findNode メソッドを使用してください。

## <a name="method-getdocnode"></a>メソッド getDocNode

AOT から指定したドキュメント ノードを取得します。

```xpp
public TreeNode getDocNode(UtilFileType helpType, int UtilType, str Name, [UtilElementId ParentId], [int Type], [UtilEntryLevel UtilLevel], [boolean ForceLevel], [int Mode], [boolean OldUtil])
```

### <a name="parameters---getdocnode"></a>パラメーター - getDocNode

helpType  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

UtilType  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

氏名  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

ParentId  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

種類  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

UtilLevel  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

ForceLevel  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

モード  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

OldUtil  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

### <a name="return-value---getdocnode"></a>戻り値 - getDocNode

AOT からのドキュメント ノードです。

### <a name="remarks---getdocnode"></a>備考 - getDocNode

helpType パラメーターの使用可能な値は、UtilFileType システム列挙の値です。

-   KernelHelp: システム ドキュメント ノード
-   ApplicationHelp: アプリケーション ドキュメント ノード
-   ApplicationCodeDocumentation: アプリケーション開発者ドキュメント ノード。

utilType パラメーターの値の例は、システム ドキュメント ノード内の機能ノードです。 ForceLevel パラメーターの既定値は false です。 False に設定され、指定されたレイヤーでコンテンツがない場合は、ノードはコンテンツを持つ次のレイヤーから取得されます。 true に設定され、レイヤーにコンテンツがない場合、メソッドは nullNothingnullptrunita null 参照 (Visual Basic 上ではなし) を返します。

## <a name="method-getimportednode"></a>メソッド getImportedNode

XPO ファイルからツリー ノードのインスタンスを作成しますが、AOT にインポートしません。 たとえば、これにより、同じツリー ノードの別のバージョンと比較できます。

```xpp
public TreeNode getImportedNode(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)
```

### <a name="parameters---getimportednode"></a>パラメーター - getImportedNode

id  

<!-- -->

utilfiletype  

<!-- -->

utiltype  

<!-- -->

名前  

<!-- -->

fileposition  

<!-- -->

フラグ  

### <a name="return-value---getimportednode"></a>戻り値 - getImportedNode

ツリー ノード。

### <a name="remarks---getimportednode"></a>備考 - getImportedNode

tilfiletype パラメーターの使用可能な値は UtilFileType 列挙で使用可能な値です。 utiltype パラメーターの使用可能な値は UtilElementType 列挙で使用可能な値です。 フラグ パラメーターの可能な値の一覧については、AOTExport マクロを参照してください。 値は、システム インポート フラグ コメントの下に一覧で表示されています。

### <a name="examples---getimportednode"></a>例 - getImportedNode

次の例では、getImportedNode メソッドを使用して仮想ツリー ノードを作成します。

```xpp
public TreeNode getVirtualTreenode( 
    Filename _filename = this.fileName()) 
{ 
    #AOT 
    #AotExport 
    TmpAotImport      tmpImportAot; 
    SysImportElements sysImportElements = new SysImportElements(); 
    TreeNode treeNodeImport  = null; 
    int      exportId; 
    int      flag = (#impGetCompareNode + #impKeepIds); 
    str      name; 
    ; 
    // Set the filename. 
    sysImportElements.newFile(_filename); 
    // Get info from the file 
    tmpImportAot = sysImportElements.getTmpImportAot(); 
    // Create an import context 
    exportId     = infolog.startImport(_filename, flag); 
    // Get the right name 
    // for doc nodes it is the path excl. the first part 
    switch (tmpImportAot.UtilFileType) 
    { 
        case UtilFileType::Application: 
            name = tmpImportAot.TreeNodeName; 
            break; 
        case UtilFileType::ApplicationCodeDocumentation: 
            name = strdel(tmpImportAot.TreeNodePath, 1, strlen(#ApplicationDeveloperDocPath)); 
            break; 
        case UtilFileType::ApplicationHelp: 
            name = strdel(tmpImportAot.TreeNodePath, 1, strlen(#ApplicationDocPath)); 
            break; 
        case UtilFileType::KernelHelp: 
            name = strdel(tmpImportAot.TreeNodePath, 1, strlen(#SystemDocPath)); 
            break; 
        default: 
            name = tmpImportAot.TreeNodeName; 
            break; 
    } 
    // Import the node in memory 
    treeNodeImport  = infolog.getImportedNode( 
        exportId, 
        tmpImportAot.UtilFileType, 
        tmpImportAot.UtilElementType, 
        name, 
        tmpImportAot.FilePos, 
        flag); 
    // Close the import context 
    infolog.endImport(exportId, 1); 
    return treeNodeImport; 
}
```

## <a name="method-getnode"></a>メソッド getNode

AOT 内のノードに対応するツリー ノードを取得します。

```xpp
public TreeNode getNode(UtilElementType UtilType, str Name, [UtilElementId ParentId], [int Type], [UtilEntryLevel Utillevel], [boolean Forcelevel], [int Mode], [boolean OldUtil])
```

### <a name="parameters---getnode"></a>パラメーター - getNode

UtilType  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

氏名  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

ParentId  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

種類  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

Utillevel  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

Forcelevel  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

モード  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

OldUtil  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

### <a name="return-value---getnode"></a>戻り値 - getNode

UtilType パラメーターおよび Name パラメーターで指定されるツリー ノード。

### <a name="remarks---getnode"></a>備考 - getNode

戻されたノードは AOT にリンクされていないため、ノードで操作を実行することはできません。 ノードの操作を行うには、代わりに findNode メソッドまたは rootNode メソッドを使用します。 UtilLevel trueparameter パラメーターの既定値は現在のレイヤーです。 Mode パラメーターの使用可能な値は次のとおりです。

-   0x001: 実行用の読み込み
-   0x002: 編集用の読み込み

ForceLevel パラメーターの既定値は false です。 False に設定され、指定されたレイヤーでコンテンツがない場合は、ノードはコンテンツを持つ次のレイヤーから取得されます。 true に設定され、レイヤーにコンテンツがない場合、メソッドは nullNothingnullptrunita null 参照 (Visual Basic 上ではなし) を返します。

## <a name="method-getnoderesid"></a>メソッド getNodeResid

指定したタイプのノードを表示するために使用されるアイコンのリソース ID を取得します。

```xpp
public int getNodeResid(UtilElementType nodeType)
```

### <a name="parameters---getnoderesid"></a>パラメーター - getNodeResid

nodeType  
取得するノードのタイプを示す UtilElementType システム列挙値。

### <a name="return-value---getnoderesid"></a>戻り値 - getNodeResid

ノードのリソース ID を表す整数。

## <a name="method-gettaskinfo"></a>メソッド getTaskInfo

```xpp
public Struct getTaskInfo(int taskNumber)
```

### <a name="parameters---gettaskinfo"></a>パラメーター - getTaskInfo

taskNumber  

### <a name="return-value---gettaskinfo"></a>戻り値 - getTaskInfo

## <a name="method-getusersetup"></a>メソッド getUserSetup

ユーザー パラメーターを設定するために使用する UserSetup オブジェクトを取得します。

```xpp
public UserSetup getUserSetup()
```

### <a name="return-value---getusersetup"></a>戻り値 - getUserSetup

UserSetup オブジェクト。

### <a name="remarks---getusersetup"></a>備考 - getUserSetup

UserSetup システム クラスは、ユーザー パラメーターを設定するためのインターフェイスを提供します。

## <a name="method-getworkspacelist"></a>メソッド getWorkspaceList

```xpp
public container getWorkspaceList()
```

### <a name="return-value---getworkspacelist"></a>戻り値 - getWorkspaceList

## <a name="method-hwnd"></a>メソッド hWnd

ナビゲーション ペイン ウィンドウのハンドルを取得します。

```xpp
public int hWnd([int workspaceNum])
```

### <a name="parameters---hwnd"></a>パラメーター - hWnd

workspaceNum  
ナビゲーション ウィンドウ ハンドルを取得するワークスペースのハンドルです。

### <a name="return-value---hwnd"></a>戻り値 - hWnd

ナビゲーション ペイン ウィンドウにハンドルを表示する整数。

## <a name="method-import"></a>メソッド import

```xpp
public boolean import(container infologContainer, [boolean clearExistingInfolog])
```

### <a name="parameters---import"></a>パラメーター - import

infologContainer  

<!-- -->

clearExistingInfolog  

### <a name="return-value---import"></a>戻り値 - import

## <a name="method-importelement"></a>メソッド importElement

インポートする対象を指定します。

```xpp
public int importElement(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)
```

### <a name="parameters---importelement"></a>パラメーター - importElement

id  

<!-- -->

utilfiletype  

<!-- -->

utiltype  

<!-- -->

名前  

<!-- -->

fileposition  

<!-- -->

フラグ  

### <a name="return-value---importelement"></a>戻り値 - importElement

 メソッドは廃止されています。 代わりに SysImportElements クラスを使用します。

## <a name="method-importstring"></a>メソッド importString

ファイルからオブジェクトをインポートします。

```xpp
public int importString(str source, UtilElementType kind, str name)
```

### <a name="parameters---importstring"></a>パラメーター - importString

ソース  
オブジェクトの名前です。

<!-- -->

kind  
オブジェクトの名前です。

<!-- -->

名前  
オブジェクトの名前です。

### <a name="return-value---importstring"></a>戻り値 - importString

## <a name="method-instance"></a>メソッド instance

アプリケーションの現在のインスタンスへのハンドルを取得します。

```xpp
public int instance()
```

### <a name="return-value---instance"></a>戻り値 - instance

アプリケーションの現在のインスタンスのハンドルです。

## <a name="method-isocurrencycode"></a>メソッド isoCurrencyCode

通貨コードを取得または設定します。

```xpp
public str isoCurrencyCode([str code])
```

### <a name="parameters---isocurrencycode"></a>パラメーター - isoCurrencyCode

コード  
設定する ISO 通貨コードを含む文字列。

### <a name="return-value---isocurrencycode"></a>戻り値 - isoCurrencyCode

現在のアプリケーションの通貨コードを含む文字列。

## <a name="method-isvisible"></a>メソッド IsVisible

クライアントのウィンドウが最小化されていないかどうかを決定します。

```xpp
public boolean IsVisible()
```

### <a name="return-value---isvisible"></a>戻り値 - IsVisible

クライアント ウィンドウが最小化されている場合は false; それ以外の場合は true。

## <a name="method-language"></a>メソッド language

GUI の言語を取得または設定します。

```xpp
public str language([str languageCode])
```

### <a name="parameters---language"></a>パラメーター - language

languageCode  
設定の言語コードを含む文字列。

### <a name="return-value---language"></a>戻り値 - language

現在の言語コードを含む文字列。

### <a name="remarks---language"></a>備考 - language

ドキュメントの言語を設定するには、xInfo.documentationLanguage メソッドを使用します。 特定のセッションの GUI 言語を設定するには、xSession.interfaceLanguage メソッドを使用します。

### <a name="examples---language"></a>例 - language

次の例では、現在設定されている言語のコードを出力します。 たとえば、インターフェイスが英語 (US) であった場合、「en-us」を印刷します。

```xpp
{ 
    print infolog.language(); 
    pause; 
}
```

## <a name="method-level"></a>メソッド level

情報ログ バッファー内の行の例外レベルを取得します。

```xpp
public Exception level(int line)
```

### <a name="parameters---level"></a>パラメーター - level

明細行  
例外レベルを取得する情報ログの行。

### <a name="return-value---level"></a>戻り値 - level

例外システム列挙値。

### <a name="remarks---level"></a>備考 - level

詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。

## <a name="method-line"></a>メソッド line

情報ログ バッファの明細行の数を取得します。

```xpp
public int line()
```

### <a name="return-value---line"></a>戻り値 - line

情報ログ バッファー内の行数を表す整数。

### <a name="remarks---line"></a>備考 - line

サーバーでコードを実行している場合は、代わりに xGlobal::infologLine メソッドを使用します。 サーバーとクライアントの間の呼び出しを除外します。 Infolog 内の特定タイプの例外の数を取得するには、xInfo.num メソッドを使用します。

## <a name="method-messagewin"></a>メソッド messageWin

Infolog から Message ウィンドウに出力を送信できます。

```xpp
public MessageWin messageWin()
```

### <a name="return-value---messagewin"></a>戻り値 - messageWin

MessageWin オブジェクト。

### <a name="remarks---messagewin"></a>備考 - messageWin

時間がかかるプロセスがある場合は、メッセージ ウィンドウに出力を送信することが必要な場合があります。 情報ログに出力を送信する場合、プロセスが完了するまで何も表示されません。 メッセージ ウィンドウに出力を送信する場合は、工程の進行中のコンテンツが表示されます。

## <a name="method-nationalcurrencyfactor"></a>メソッド nationalCurrencyFactor

```xpp
public Real nationalCurrencyFactor([Real factor])
```

### <a name="parameters---nationalcurrencyfactor"></a>パラメーター - nationalCurrencyFactor

係数  

### <a name="return-value---nationalcurrencyfactor"></a>戻り値 - nationalCurrencyFactor

## <a name="method-nationalcurrencypostfix"></a>メソッド nationalCurrencyPostfix

```xpp
public str nationalCurrencyPostfix([str string])
```

### <a name="parameters---nationalcurrencypostfix"></a>パラメーター - nationalCurrencyPostfix

文字列  

### <a name="return-value---nationalcurrencypostfix"></a>戻り値 - nationalCurrencyPostfix

## <a name="method-nationalcurrencyprefix"></a>メソッド nationalCurrencyPrefix

```xpp
public str nationalCurrencyPrefix([str string])
```

### <a name="parameters---nationalcurrencyprefix"></a>パラメーター - nationalCurrencyPrefix

文字列  

### <a name="return-value---nationalcurrencyprefix"></a>戻り値 - nationalCurrencyPrefix

## <a name="method-navpane"></a>メソッド navPane

プライマリ ナビゲーション コントロール クラスの xNavPane オブジェクトを取得します。

```xpp
public xNavPane navPane()
```

### <a name="return-value---navpane"></a>戻り値 - navPane

xNavPane クラスのインスタンス。

### <a name="remarks---navpane"></a>備考 - navPane

このクラスのインスタンスはワークスペースごとに 1 つのみ持つことができます。

## <a name="method-num"></a>メソッド num

情報ログ バッファにおける指定した型の例外の数を取得します。

```xpp
public int num([Exception exceptionType])
```

### <a name="parameters---num"></a>パラメーター - num

exceptionType  
カウントする例外のタイプを示す例外システム列挙値; オプション。

### <a name="return-value---num"></a>戻り値 - num

exceptionType パラメーターで指定されたタイプの例外の数または、パラメーターが指定されていない場合の情報ログ内の行の合計数を表す整数。

### <a name="remarks---num"></a>備考 - num

詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。

### <a name="examples---num"></a>例 - num

次の例は、Infolog 内の警告の数を返します。

```xpp
{ 
    print infolog.num(Exception::Warning); 
    pause; 
}
```

## <a name="method-previnstance"></a>メソッド prevInstance

アプリケーションの前のインスタンスへのハンドルを取得します。

```xpp
public int prevInstance()
```

### <a name="return-value---previnstance"></a>戻り値 - prevInstance

アプリケーションの以前のインスタンスのハンドルです。

### <a name="remarks---previnstance"></a>備考 - prevInstance

このメソッドは使用しないでください。

## <a name="method-processid"></a>メソッド processId

プロセスの ID を取得します。

```xpp
public int processId()
```

### <a name="return-value---processid"></a>戻り値 - processId

プロセスの ID。

## <a name="method-projectrootnode"></a>メソッド projectRootNode

X++ プロジェクト ノードを返します。

```xpp
public TreeNode projectRootNode()
```

### <a name="return-value---projectrootnode"></a>戻り値 - projectRootNode

X++ プロジェクトを含むツリー ノード。

### <a name="examples---projectrootnode"></a>例 - projectRootNode

次の例では、共有プロジェクト フォルダー内のすべてのプロジェクトの名前を出力します。

```xpp
void ProjectNames() 
{ 
    Treenode treenode; 
    TreenodeIterator it; 
    treenode = infolog.projectRootNode(); 
    treenode = treenode.AOTfindChild("Shared"); 
    it = treenode.AOTiterator(); 
    while (treenode) 
    { 
       print treenode.treeNodeName(); 
       treenode = it.next(); 
    } 
    pause; 
}
```

## <a name="method-rootnode"></a>メソッド rootNode

アプリケーション オブジェクト ツリーのルートを取得します。

```xpp
public TreeNode rootNode()
```

### <a name="return-value---rootnode"></a>戻り値 - rootNode

アプリケーション オブジェクト ツリーのルート。

### <a name="examples---rootnode"></a>例 - rootNode

次の例では、AddressSelectForm クラスのメソッドのすべての名前を出力します。 rootnode メソッドは、子ノードを選択する前に、treenode オブジェクトを AOT ルートに設定するために使用されます。

```xpp
{ 
    Treenode treenode; 
    TreenodeIterator it; 
    treenode = infolog.rootNode(); 
    treenode = treenode.AOTfindChild("Classes"); 
    treenode = treenode.AOTfindChild("AddressSelectForm"); 
    it = treenode.AOTiterator(); 
    while (treenode) 
    { 
       print treenode.treeNodeName(); 
       treenode = it.next(); 
    } 
    pause; 
}
```

## <a name="method-startimport"></a>メソッド startImport

インポート コンテキストを作成します。

```xpp
public int startImport(str file, int flag, [str labelSubstitutes])
```

### <a name="parameters---startimport"></a>パラメーター - startImport

ファイル  

<!-- -->

flag  

<!-- -->

labelSubstitutes  

### <a name="return-value---startimport"></a>戻り値 - startImport

### <a name="remarks---startimport"></a>備考 - startImport

 メソッドは廃止されています。 代わりに SysImportElements クラスを使用します。

## <a name="method-text"></a>メソッド text

情報ログからテキストの行を取得します。

```xpp
public str text([int line])
```

### <a name="parameters---text"></a>パラメーター - text

明細行  
取得するテキストを含む情報ログ内の行。

### <a name="return-value---text"></a>戻り値 - text

情報ログのテキストを含む文字列。

## <a name="method-usernode"></a>メソッド userNode

```xpp
public TreeNode userNode()
```

### <a name="return-value---usernode"></a>戻り値 - userNode

## <a name="method-websession"></a>メソッド webSession

```xpp
public AnyType webSession([AnyType value])
```

### <a name="parameters---websession"></a>パラメーター - webSession

値  

### <a name="return-value---websession"></a>戻り値 - webSession

## <a name="method-activexcontrols"></a>メソッド activeXControls

ActiveX コントロールの一覧を取得します。

```xpp
public static container activeXControls()
```

### <a name="return-value---activexcontrols"></a>戻り値 - activeXControls

各 ActiveX コントロールに関する情報を保持する入れ子になったコンテナー。

### <a name="remarks---activexcontrols"></a>備考 - activeXControls

返されるコンテナーには 4 つのコンテナーがあります。 最初の内部コンテナーには、すべてのコントロールの名前が含まれます。 2 番目の内部コンテナーには、各コントロールの ID (GUID) が格納されます。 3 番目の内部コンテナーには、各コントロールのセキュリティ設定が格納されます。 4 番目の内部コンテナーには、各コントロールの説明が含まれています。

### <a name="examples---activexcontrols"></a>例 - activeXControls

次の例は、各 ActiveX コントロールの説明を出力します。

```xpp
static void activeXcontents(Args _args) 
{ 
    int       i; 
    str       strClsName, strTypeLibHelp, strClsId, strSafeForBits; 
    container c; 
    container clsName, clsId, safeForBits, typeLibHelp; 
    c = xinfo::activeXControls(); 
    clsName = conpeek(c, 1); 
    clsId = conpeek(c, 2); 
    safeForBits = conpeek(c, 3); 
    typeLibHelp = conpeek(c, 4); 
    for (i=1; i<conlen(clsName); i++) 
    { 
        strClsName = conpeek(clsName, i); 
        strClsId = conpeek(clsId, i); 
        strSafeForBits = conpeek(safeForBits, i); 
        strTypeLibHelp = conpeek(typeLibHelp, i); 
        print strClsName, " ", strClsId, " ", strSafeForBits, 
            " ", strTypeLibHelp; 
    } 
    pause; 
}
```

## <a name="method-aotlogdirectory"></a>メソッド AOTLogDirectory

現在のインストールのログ ディレクトリへのパスを取得します。

```xpp
public static str AOTLogDirectory()
```

### <a name="return-value---aotlogdirectory"></a>戻り値 - AOTLogDirectory

現在のインストールのログ ディレクトリへのパスを含む文字列。

### <a name="remarks---aotlogdirectory"></a>備考 - AOTLogDirectory

AOT ログ オプションを有効にする場合は、コンパイルするたびにときに、ログ ディレクトリに情報が保存されます。 このオプションをオンにするには、次のようにします。

1.  開発者ワークスペースを開きます。
2.  [ツール] &gt; [オプション] &gt; [開発]&gt; [コンパイラ] を選択します。
3.  AOT ログ チェック ボックスをオンにします。

## <a name="method-automationobjects"></a>メソッド automationObjects

使用可能な COM オブジェクトの一覧を取得します。

```xpp
public static container automationObjects()
```

### <a name="return-value---automationobjects"></a>戻り値 - automationObjects

各 COM オブジェクトの説明を保持する入れ子になったコンテナー。

### <a name="examples---automationobjects"></a>例 - automationObjects

次の例では、automationObject から返される入れ子になったコンテナーを展開して、COM オブジェクトのリストを取得します。

```xpp
void getAutomationObjects() 
{ 
    int idx; 
    FormListItem listItem; 
    int itemPos; 
    container clsGUID,clsDesc,clsVersion,clsPath; 
    [clsGUID,clsDesc,clsVersion,clsPath] = xInfo::automationObjects(); 
    for (idx = 1; idx < conlen(clsGUID); idx++) 
    { 
        itemPos = formListControl.add(conpeek(clsDesc,idx)); 
        listItem = formListControl.getItem(itemPos); 
        listItem.data(conpeek(clsPath,idx)); 
        formListControl.setItem(listItem); 
    } 
}
```

## <a name="method-buildno"></a>メソッド buildNo

現在の実行可能ファイルのカーネル ビルド番号を取得します。

```xpp
public static str buildNo()
```

### <a name="return-value---buildno"></a>戻り値 - buildNo

カーネル ビルド番号を含む文字列。

### <a name="examples---buildno"></a>例 - buildNo

次の例では、このメソッドを使用して、バージョン情報を含む文字列の一部としてカーネル ビルド番号を返します。

```xpp
static client str axaptaReleaseID() 
{ 
    #define.versionPrefix('v') 
    #define.versionNumber('#') 
    #define.versionPartition('/') 
    return    #versionprefix+xInfo::releaseVersion()+ 
              #versionNumber+xInfo::buildNo()+ 
              #versionPartition+ApplicationVersion::buildNo(); 
}
```

## <a name="method-compilationdate"></a>メソッド compilationDate

現在のバージョンが最後にコンパイルされた日付を取得します。

```xpp
public static str compilationDate()
```

### <a name="return-value---compilationdate"></a>戻り値 - compilationDate

現在のバージョンが最後にコンパイルされた日付を含む文字列。

### <a name="examples---compilationdate"></a>例 - compilationDate

次の例では、アプリケーションが最後にコンパイルされた日付を含むシステム情報を返します。

```xpp
str environment() 
{ 
    return xInfo::buildNo() + ' - '  
        + xInfo::compilationDate() + ' - '  
        + xInfo::dbName() + ' - '  
        + xInfo::osName() + ' - '  
        + xInfo::productName() + ' - '  
        + xInfo::releaseVersion(); 
}
```

## <a name="method-compilationtime"></a>メソッド compilationTime

現在のバージョンが最後にコンパイルされた時刻を取得します。

```xpp
public static str compilationTime()
```

### <a name="return-value---compilationtime"></a>戻り値 - compilationTime

現在のバージョンが最後にコンパイルされた時刻を含む文字列。

## <a name="method-componentname"></a>メソッド componentName

コンポーネントへのパスを取得します。

```xpp
public static str componentName()
```

### <a name="return-value---componentname"></a>戻り値 - componentName

実行可能ファイルへのパスを含む文字列。

### <a name="remarks---componentname"></a>備考 - componentName

このメソッドがクライアントで実行される場合、クライアントの .exe ファイルへのパスを返します。 サーバーで実行する場合、AOS の .exe ファイルへのパスを返します。

## <a name="method-configuration"></a>メソッド configuration

現在のクライアント構成を取得します。

```xpp
public static str configuration()
```

### <a name="return-value---configuration"></a>戻り値 - configuration

現在のクライアント コンフィギュレーションを表す文字列。

### <a name="remarks---configuration"></a>備考 - configuration

これは、クライアント構成ユーティリティー プログラムの「構成」ボックスで選択されている構成です。 返される文字列の例としては「オリジナル (インストール済コンフィギュレーション)」です。

## <a name="method-currentworkspacenum"></a>メソッド currentWorkspaceNum

現在のワークスペースのアプリケーション ウィンドウ ID を取得します。

```xpp
public static int currentWorkspaceNum()
```

### <a name="return-value---currentworkspacenum"></a>戻り値 - currentWorkspaceNum

現在のワークスペースのアプリケーション ウィンドウ ID。

### <a name="remarks---currentworkspacenum"></a>備考 - currentWorkspaceNum

createWorkspaceWindow メソッドを使用すると、アプリケーション内で追加のワークスペースを開くことができます。

## <a name="method-directory"></a>メソッド directory

クライアントがインストールされているディレクトリへのパスを取得します。

```xpp
public static str directory(DirectoryType type)
```

### <a name="parameters---directory"></a>パラメーター - directory

タイプ  
クライアント インストールのサブフォルダーのいずれかを示す DirectoryType 列挙値。

### <a name="return-value---directory"></a>戻り値 - directory

DirectoryType パラメーターで指定されているディレクトリへのパスを含む文字列。

### <a name="examples---directory"></a>例 - directory

次の例は、現在のクライアント インストールの Bin ディレクトリへのパスを出力します。

```xpp
{ 
    print xInfo::directory(DirectoryType::Bin); 
    pause; 
}
```

## <a name="method-expiredate"></a>メソッド expireDate

現在のインストールのライセンスの有効期限が切れる日付を取得します。

```xpp
public static Date expireDate()
```

### <a name="return-value---expiredate"></a>戻り値 - expireDate

ライセンスの有効期限が切れる日を表す日付です。

## <a name="method-getapplicationobjecttreewindow"></a>メソッド getApplicationObjectTreeWindow

```xpp
public static ApplicationObjectTreeWindow getApplicationObjectTreeWindow()
```

### <a name="return-value---getapplicationobjecttreewindow"></a>戻り値 - getApplicationObjectTreeWindow

## <a name="method-getcurrentmodelid"></a>メソッド getCurrentModelId

```xpp
public static int getCurrentModelId()
```

### <a name="return-value---getcurrentmodelid"></a>戻り値 - getCurrentModelId

## <a name="method-getnumberofdecimals"></a>メソッド getNumberOfDecimals

指定された数値の小数点以下の桁数を取得します。

```xpp
public static int getNumberOfDecimals(Real number)
```

### <a name="parameters---getnumberofdecimals"></a>パラメーター - getNumberOfDecimals

番号  
実数。

### <a name="return-value---getnumberofdecimals"></a>戻り値 - getNumberOfDecimals

数値パラメーターの小数点以下の桁数。

## <a name="method-getpropertieswindow"></a>メソッド getPropertiesWindow

```xpp
public static PropertiesWindow getPropertiesWindow()
```

### <a name="return-value---getpropertieswindow"></a>戻り値 - getPropertiesWindow

## <a name="method-getsystemgeneratedmodelid"></a>メソッド getSystemGeneratedModelId

```xpp
public static int getSystemGeneratedModelId(UtilEntryLevel layer)
```

### <a name="parameters---getsystemgeneratedmodelid"></a>パラメーター - getSystemGeneratedModelId

 レイヤー  

### <a name="return-value---getsystemgeneratedmodelid"></a>戻り値 - getSystemGeneratedModelId

## <a name="method-licensename"></a>メソッド licenseName

現在のライセンスの名前を取得します。

```xpp
public static str licenseName()
```

### <a name="return-value---licensename"></a>戻り値 - licenseName

ライセンスの名前を含む文字列。

### <a name="remarks---licensename"></a>備考 - licenseName

xInfo::expireDate メソッドは、ライセンスが失効する日付を返します。 xInfo::serialNo メソッドは、ライセンスのシリアル番号を返します。

## <a name="method-productname"></a>メソッド productName

製品の名前を取得します。

```xpp
public static str productName()
```

### <a name="return-value---productname"></a>戻り値 - productName

製品の名前を含む文字列。

### <a name="examples---productname"></a>例 - productName

次の例では、製品の名前を含むシステム情報を戻します。

```xpp
str environment() 
{ 
    return xInfo::buildNo() + ' - '  
        + xInfo::compilationDate() + ' - '  
        + xInfo::dbName() + ' - '  
        + xInfo::osName() + ' - '  
        + xInfo::productName() + ' - '  
        + xInfo::releaseVersion(); 
}
```

## <a name="method-productregisteredname"></a>メソッド productRegisteredName

```xpp
public static str productRegisteredName()
```

### <a name="return-value---productregisteredname"></a>戻り値 - productRegisteredName

## <a name="method-releaseversion"></a>メソッド releaseVersion

現在の実行可能ファイルのバージョン番号を取得します。例: 3.0、4.0。

```xpp
public static str releaseVersion()
```

### <a name="return-value---releaseversion"></a>戻り値 - releaseVersion

バージョン番号を含む文字列。

### <a name="remarks---releaseversion"></a>備考 - releaseVersion

有効なバージョン番号は、3.0 および 4.0 などです。

### <a name="examples---releaseversion"></a>例 - releaseVersion

次の例では、これを使用して、バージョン情報を含む文字列の一部としてバージョン番号を返します。

```xpp
static client str axaptaReleaseID() 
{ 
    #define.versionPrefix('v') 
    #define.versionNumber('#') 
    #define.versionPartition('/') 
    return    #versionprefix+xInfo::releaseVersion()+ 
              #versionNumber+xInfo::buildNo()+ 
              #versionPartition+ApplicationVersion::buildNo(); 
}
```

## <a name="method-releaseyear"></a>メソッド releaseYear

```xpp
public static str releaseYear()
```

### <a name="return-value---releaseyear"></a>戻り値 - releaseYear

## <a name="method-serialno"></a>メソッド serialNo

現在のライセンスのシリアル番号を取得します。

```xpp
public static str serialNo()
```

### <a name="return-value---serialno"></a>戻り値 - serialNo

ライセンスのシリアル番号を含む文字列。

## <a name="method-new"></a>メソッド new

新しい xInfo オブジェクトを初期化します。

```xpp
public void new()
```

### <a name="remarks---new"></a>備考 - new

注記: このメソッドを使用しないでください。 代わりに、xInfo クラスのグローバル インスタンス infolog を使用する必要があります。 詳細については、「xInfo クラス」を参照してください。

## <a name="method-workspacewindowdestroyed"></a>メソッド workspaceWindowDestroyed

新しいワークスペースが終了した時に実行します。

```xpp
public void workspaceWindowDestroyed(int hWnd)
```

### <a name="parameters---workspacewindowdestroyed"></a>パラメーター - workspaceWindowDestroyed

hWnd  
ワークスペースのハンドルです。

### <a name="remarks---workspacewindowdestroyed"></a>備考 - workspaceWindowDestroyed

このメソッドは、新しいワークスペースが閉じられるときに呼び出されます。 これにより、発生したときにアクションを実行できます。

## <a name="method-writecustomstatlineitem"></a>メソッド writeCustomStatlineItem

テキストの行をステータス バーに記述します。

```xpp
public void writeCustomStatlineItem(str text)
```

### <a name="parameters---writecustomstatlineitem"></a>パラメーター - writeCustomStatlineItem

テキスト  
ステータス バーに入れるテキストの行。

## <a name="method-reloadrunningmode"></a>メソッド reloadRunningMode

```xpp
public void reloadRunningMode()
```

## <a name="method-setwindoworder"></a>メソッド setWindowOrder

Windows の表示順序を設定します。

```xpp
public void setWindowOrder(int window, [int afterWindow])
```

### <a name="parameters---setwindoworder"></a>パラメーター - setWindowOrder

window  
ウィンドウ パラメーターで指定されたウィンドウの後に配置するウィンドウのハンドルです (オプション)。

<!-- -->

afterWindow  
ウィンドウ パラメーターで指定されたウィンドウの後に配置するウィンドウのハンドルです (オプション)。

### <a name="examples---setwindoworder"></a>例 - setWindowOrder

次の例では、ウィンドウにフォーカスを設定し、ウィンドウを前面に移動します。

```xpp
void setFocus() 
{ 
    infolog.activateWindow(element.hWnd()); 
    infolog.setWindowOrder(element.hWnd()); 
}
```

## <a name="method-shutdown"></a>メソッド shutDown

クライアントをシャットダウンします。

```xpp
public void shutDown(boolean force)
```

### <a name="parameters---shutdown"></a>パラメーター - shutDown

force  
シャット ダウンを防止するオプションが、ユーザーに与えられたかどうかを示すブール値。

## <a name="method-xref"></a>メソッド xref

相互参照システムが使用される時に実行します。

```xpp
public void xref(str path, xRef x)
```

### <a name="parameters---xref"></a>パラメーター - xref

path  

<!-- -->

x  

### <a name="remarks---xref"></a>備考 - xref

このメソッドを使用しないでください。

## <a name="method-updatecurrentcompany"></a>メソッド updateCurrentCompany

```xpp
public void updateCurrentCompany()
```

## <a name="method-redrawallwindows"></a>メソッド redrawAllWindows

すべてのウィンドウを再描画します。

```xpp
public void redrawAllWindows()
```

### <a name="remarks---redrawallwindows"></a>備考 - redrawAllWindows

このメソッドは、長いプロセス中に表示を更新するために使用できます。

## <a name="method-formnotify"></a>メソッド formNotify

特定フォームへの変更特定タイプに基づいて実行し、カスタムコードの実行を許可します。

```xpp
public void formNotify(xFormRun form, FormNotify notification, [FormNotifyEventArgs formNotifyEventArgs])
```

### <a name="parameters---formnotify"></a>パラメーター - formNotify

フォーム  

<!-- -->

通知  

<!-- -->

formNotifyEventArgs  

### <a name="remarks---formnotify"></a>備考 - formNotify

通知パラメーターの使用可能な値は次のとおりです。

-   アクティブ化
-   DeActivate
-   求人開始
-   終了
-   RecordChange
-   NoteClicked

このメソッドの使用例については、このメソッドが上書きされた情報クラスの formNotify メソッドを参照してください。

## <a name="method-mayreloadmenu"></a>メソッド mayReloadMenu

UI を更新できないようにする

```xpp
public void mayReloadMenu(boolean value)
```

### <a name="parameters---mayreloadmenu"></a>パラメーター - mayReloadMenu

値  
UI が更新されないようにするかどうかを示すブール値。

### <a name="remarks---mayreloadmenu"></a>備考 - mayReloadMenu

プロセスが実行されたときに UI が更新されないように値を false に設定し、プロセスが終了した後は true に設定します。 mayReloadMenu メソッドは、AOT 内の多くのノードが読み取られているなど、UI がちらつくのを防ぐのに便利です。

## <a name="method-startlengthyoperation"></a>メソッド startLengthyOperation

マウス カーソルをアイドルに設定します。

```xpp
public void startLengthyOperation()
```

### <a name="remarks---startlengthyoperation"></a>備考 - startLengthyOperation

時間のかかる操作の開始時に、プロセスが進行中であることを示すために使用します。 工程が完了したら、システムは endLengthyOperation メソッドを自動的に呼び出します。

## <a name="method-breakpointnotify"></a>メソッド breakpointNotify

ブレークポイントが変更されたときの通知システムを実装します。

```xpp
public void breakpointNotify(BreakpointNotify notification)
```

### <a name="parameters---breakpointnotify"></a>パラメーター - breakpointNotify

通知  
ブレークポイントに発生した変更のタイプを指定する BreakpointNotify システム列挙値。

### <a name="remarks---breakpointnotify"></a>備考 - breakpointNotify

アプリケーションで、このメソッドはコード エディター ウィンドウでのブレークポイントの変更時に、ブレークポイント フォームを更新するために使用されます。 通知パラメーターには、次の BreakpointNotify 列挙型の値が有効です。

-   BreakpointForm: ブレークポイント リストを再読み込みする必要があることをクライアントに通知します。
-   BreakpointChange: クライアントとサーバーにブレークポイントの状態が変更 (有効、無効、または削除) されたことを通知します。

## <a name="method-initializeinfolog"></a>メソッド initializeInfolog

```xpp
public void initializeInfolog(int window)
```

### <a name="parameters---initializeinfolog"></a>パラメーター - initializeInfolog

window  

## <a name="method-startup"></a>メソッド startup

クライアントの起動時に実行します。

```xpp
public void startup(str startupCmd)
```

### <a name="parameters---startup"></a>パラメーター - startup

startupCmd  

### <a name="remarks---startup"></a>備考 - startup

このメソッドを使用しないでください。 代わりに次の方法のいずれかを使用します。 起動コマンドをクライアントに渡すには Info.startupPost メソッドを使用します。 起動コマンドをサーバーに渡すには Application.startupPost メソッドを使用します。 Application.startup または Info.startup メソッドを使用しないでください。 これは新しいバージョンのコードに影響する可能性があり、クライアントまたはサーバーの起動を妨げる可能性があります。

## <a name="method-endimport"></a>メソッド endImport

インポート プロセスを完了します。

```xpp
public void endImport(int id, int elements)
```

### <a name="parameters---endimport"></a>パラメーター - endImport

id  

<!-- -->

elements  

### <a name="remarks---endimport"></a>備考 - endImport

 メソッドは廃止されています。 代わりに SysImportElements クラスを使用します。

## <a name="method-yield"></a>メソッド yield

```xpp
public void yield()
```

## <a name="method-viewalertinbox"></a>メソッド viewAlertInbox

警告の表示フォームを起動します。

```xpp
public void viewAlertInbox([int selectedTab])
```

### <a name="parameters---viewalertinbox"></a>パラメーター - viewAlertInbox

selectedTab  
警告の表示フォームが表示されるタブを決定します。オプション。

### <a name="remarks---viewalertinbox"></a>備考 - viewAlertInbox

selectedTab パラメーターの既定値は、最初のタブである概要です。xInfo.canViewAlertInbox メソッドを呼び出して、ユーザーがこのフォームを表示する権限を持っているかどうかを確認します。

## <a name="method-reportsendmailserver"></a>メソッド reportSendMailServer

```xpp
public void reportSendMailServer(PrintJobSettings settings)
```

### <a name="parameters---reportsendmailserver"></a>パラメーター - reportSendMailServer

設定  

## <a name="method-endlengthyoperation"></a>メソッド endLengthyOperation

startLengthyOperation の呼び出し後にマウス カーソルが標準に戻るように設定します。

```xpp
public void endLengthyOperation([boolean endAll])
```

### <a name="parameters---endlengthyoperation"></a>パラメータ－ - endLengthyOperation

endAll  
予約済み。

### <a name="remarks---endlengthyoperation"></a>備考 - endLengthyOperation

このメソッドを呼び出さないことをお勧めします。 操作が終了すると、システムによって自動的に呼び出されます。 明示的にこのメソッドを呼び出し、その他のプロセスまたはループのコードがある場合は、このメソッドを使用すると、マウス ポインターが点滅する可能性があります。

## <a name="method-setnumunreadalerts"></a>メソッド setNumUnreadAlerts

未読の警告メールの数が変わると、ステータス バーのテキストを更新します。

```xpp
public void setNumUnreadAlerts([int n])
```

### <a name="parameters---setnumunreadalerts"></a>パラメーター - setNumUnreadAlerts

n  
未読メールの数を特定の番号に設定できます。

## <a name="method-truncate"></a>メソッド truncate

情報ログから指定した接頭語の付いた品目を削除します。

```xpp
public void truncate(str prefix)
```

### <a name="parameters---truncate"></a>パラメーター - truncate

prefix  
情報ログから削除する必要のある項目の接頭語。

## <a name="method-formnotebutton"></a>メソッド formNoteButton

ツールバーのドキュメント処理ボタンをコントロールします。

```xpp
public void formNoteButton(boolean enable, boolean value)
```

### <a name="parameters---formnotebutton"></a>パラメーター - formNoteButton

enable  
アイコンの表示が示すブール値データ型。

<!-- -->

値  
アイコンの表示が示すブール値データ型。

### <a name="examples---formnotebutton"></a>例 - formNoteButton

次の例は、ドキュメント処理ボタンを無効にする方法を示しています。

```xpp
void disableNoteButton() 
    { 
        infolog.formNoteButton(false, false); 
    }
```

## <a name="method-viewcreateruledialog"></a>メソッド viewCreateRuleDialog

警告ルールの作成フォームを起動します。

```xpp
public void viewCreateRuleDialog(xFormRun caller)
```

### <a name="parameters---viewcreateruledialog"></a>パラメーター - viewCreateRuleDialog

caller  
現在のフォーム。

### <a name="remarks---viewcreateruledialog"></a>備考 - viewCreateRuleDialog

作成警告ルール フォームは、呼び出し元のパラメーターで指定された現在のフォームから起動されます。

## <a name="method-view"></a>メソッド view

```xpp
public void view([container container])
```

### <a name="parameters---view"></a>パラメーター - view

コンテナー  

## <a name="method-clear"></a>メソッド clear

情報ログ バッファーから行を削除します。

```xpp
public void clear([int linesLeft])
```

### <a name="parameters---clear"></a>パラメーター - clear

linesLeft  
バッファに残す行の数、省略可能です。

### <a name="remarks---clear"></a>備考 - clear

他のプロセスが情報を Infolog に入れていない限り、既定値がゼロのメソッドで呼び出さないでください。

### <a name="examples---clear"></a>例 - clear

Infolog キャッシュを消去するには、このパターンを使用します。

```xpp
int line = Global::infologLine();
try 
{ 
    // 
} 
catch 
{ 
    infolog.clear(line); 
}
```

## <a name="method-workspacewindowcreated"></a>メソッド workspaceWindowCreated

新しいワークスペースが作成された時に実行します。

```xpp
public void workspaceWindowCreated(int hWnd)
```

### <a name="parameters---workspacewindowcreated"></a>パラメーター - workspaceWindowCreated

hWnd  
新しいワークスペースのハンドルです。

### <a name="remarks---workspacewindowcreated"></a>備考 - workspaceWindowCreated

このメソッドは、新しいワークスペースが作成されるときに呼び出されます。 これにより、発生したときにアクションを実行できます。

## <a name="method-setcurrentmodelid"></a>メソッド setCurrentModelId

```xpp
public static void setCurrentModelId(int currentModelId)
```

### <a name="parameters---setcurrentmodelid"></a>パラメーター - setCurrentModelId

currentModelId  

## <a name="method-activatemenubartask"></a>メソッド activateMenubarTask

```xpp
public void activateMenubarTask(int command)
```

### <a name="parameters---activatemenubartask"></a>パラメーター - activateMenubarTask

command  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-insertxreferences"></a>メソッド insertXReferences

```xpp
public void insertXReferences()
```

## <a name="method-activatebutton"></a>メソッド activateButton

```xpp
public void activateButton(int command)
```

### <a name="parameters---activatebutton"></a>パラメーター - activateButton

command  

## <a name="method-activatewindow"></a>メソッド activateWindow

フォームまたはウィンドウにフォーカスを設定します。

```xpp
public void activateWindow(int window)
```

### <a name="parameters---activatewindow"></a>パラメーター - activateWindow

window  
詳しく説明するフォームまたはウィンドウのハンドルです。

## <a name="method-reportsendmail"></a>メソッド reportSendMail

レポートを電子メールで送信するための設定を生成します。

```xpp
public void reportSendMail(PrintJobSettings settings)
```

### <a name="parameters---reportsendmail"></a>パラメーター - reportSendMail

設定  
ユーザーの電子メール設定。

