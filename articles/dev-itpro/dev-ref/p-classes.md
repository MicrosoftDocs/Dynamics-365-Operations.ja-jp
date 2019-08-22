---
title: P クラス
description: 文字 P で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 52231
ms.assetid: 50842cd5-c27f-43aa-8a6d-bc9d3b02fd60
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be43a30edca6f94e7c0f406c8095a6670ae6900b
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833672"
---
# <a name="p-classes"></a>P クラス

[!include [banner](../includes/banner.md)]

文字 P で始まるシステム API クラス。

<a name="class-page"></a>クラス ページ
----------

    class Page extends Object

このページ クラスでは、作成、読み取り、更新、および X++ コードおよびメタデータを削除できます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                        | 説明                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| public boolean actionPaneControlEnabled(str controlName, \[boolean enabled\]) | アクション ウィンドウ上のコントロールの有効なプロパティの値を設定または取得します。 |
| public boolean actionPaneControlVisible(str controlName, \[boolean visible\]) | アクション ウィンドウ上のコントロールの表示されるプロパティの値を設定または取得します。 |
| public Array activeActionPaneTabNames()                                       |                                                                          |
| public Common activeRecord(str dataSourceName)                                | 特定のデータ ソース名の有効なレコードを取得します。                   |
| public str name()                                                             | ページの名前を取得します。                                               |
| public PageArgs pageArgs()                                                    | page 引数を取得します。                                                 |
| public xFormRun formRun()                                                     |                                                                          |

### <a name="method-actionpanecontrolenabled"></a>メソッド actionPaneControlEnabled

アクション ウィンドウ上のコントロールの有効なプロパティの値を設定または取得します。

    public boolean actionPaneControlEnabled(str controlName, [boolean enabled])

#### <a name="parameters"></a>パラメーター

controlName  
アクション ウィンドウ コントロールが有効かどうかを指定する値、オプション。

<!-- -->

有効  
アクション ウィンドウ コントロールが有効かどうかを指定する値、オプション。

#### <a name="return-value"></a>戻り値

アクション ペイン コントロールが有効かどうかを指定するブール値。

### <a name="method-actionpanecontrolvisible"></a>メソッド actionPaneControlVisible

アクション ウィンドウ上のコントロールの表示されるプロパティの値を設定または取得します。

    public boolean actionPaneControlVisible(str controlName, [boolean visible])

#### <a name="parameters"></a>パラメーター

controlName  
アクション ウィンドウ コントロールが表示されるかどうかを指定する値、オプション。

<!-- -->

表示  
アクション ウィンドウ コントロールが表示されるかどうかを指定する値、オプション。

#### <a name="return-value"></a>戻り値

アクション ペイン コントロールが表示されるかどうかを指定するブール値。

### <a name="method-activeactionpanetabnames"></a>メソッド activeActionPaneTabNames

    public Array activeActionPaneTabNames()

#### <a name="return-value"></a>戻り値

### <a name="method-activerecord"></a>メソッド activeRecord

特定のデータ ソース名の有効なレコードを取得します。

    public Common activeRecord(str dataSourceName)

#### <a name="parameters"></a>パラメーター

dataSourceName  
検索するデータ ソースの名前。

#### <a name="return-value"></a>戻り値

特定のデータ ソース用の有効なレコード。

### <a name="method-name"></a>メソッド名

ページの名前を取得します。

    public str name()

#### <a name="return-value"></a>戻り値

ページ名。

### <a name="method-pageargs"></a>メソッド pageArgs

page 引数を取得します。

    public PageArgs pageArgs()

#### <a name="return-value"></a>戻り値

page 引数。

### <a name="method-formrun"></a>メソッド formRun

    public xFormRun formRun()

#### <a name="return-value"></a>戻り値

## <a name="class-pageargs"></a>クラス PageArgs
    class PageArgs extends Object

PageArgs クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                         | 説明                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| public int enumParameter(\[int value\])        | MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。 |
| public int enumTypeParameter(\[int value\])    | MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。                                     |
| public Common externalRecord(\[Common value\]) |                                                                                                             |
| public str menuItemName(\[str value\])         |                                                                                                             |
| public str parameters(\[str value\])           | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。      |
| public void new()                              | PageArgs クラスの新しいインスタンスを初期化します。                                                           |

### <a name="method-enumparameter"></a>メソッド enumParameter

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。

    public int enumParameter([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。

### <a name="method-enumtypeparameter"></a>メソッド enumTypeParameter

MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。

    public int enumTypeParameter([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスの enumTypeParameter プロパティ。

### <a name="method-externalrecord"></a>メソッド externalRecord

    public Common externalRecord([Common value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-new"></a>メソッド new

PageArgs クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-pageinteraction"></a>クラス PageInteraction
    class PageInteraction extends Object

PageInteraction クラスは、リスト ページとやり取りするための機能を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                           | 説明                                                        |
|--------------------------------------------------|--------------------------------------------------------------------|
| public Page page()                               | ListPage インスタンスを取得します。                                        |
| public void tabChanged(container activeTabNames) |                                                                    |
| public void new(Page page)                       | リスト ページ上で動作する新しい PageInteraction オブジェクトを作成します。 |

### <a name="method-page"></a>メソッド page

ListPage インスタンスを取得します。

    public Page page()

#### <a name="return-value"></a>戻り値

この PageInteraction インスタンスの ListPage インスタンスを返します。

### <a name="method-tabchanged"></a>メソッド tabChanged

    public void tabChanged(container activeTabNames)

#### <a name="parameters"></a>パラメーター

activeTabNames  

### <a name="method-new"></a>メソッド new

リスト ページ上で動作する新しい PageInteraction オブジェクトを作成します。

    public void new(Page page)

#### <a name="parameters"></a>パラメーター

ページ  

## <a name="class-partlist"></a>クラス PartList
    class PartList extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                        | 説明                                     |
|-----------------------------------------------|-------------------------------------------------|
| public xFormRun getPartById(int id)           |                                                 |
| public FormControl getPartControlById(int id) |                                                 |
| public int partCount()                        |                                                 |
| public void new(xFormRun form)                | Object クラスの新しいインスタンスを初期化します。 |
| public void finalize()                        |                                                 |

### <a name="method-getpartbyid"></a>メソッド getPartById

    public xFormRun getPartById(int id)

#### <a name="parameters"></a>パラメーター

id  

#### <a name="return-value"></a>戻り値

### <a name="method-getpartcontrolbyid"></a>メソッド getPartControlById

    public FormControl getPartControlById(int id)

#### <a name="parameters"></a>パラメーター

id  

#### <a name="return-value"></a>戻り値

### <a name="method-partcount"></a>メソッド partCount

    public int partCount()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(xFormRun form)

#### <a name="parameters"></a>パラメーター

フォーム  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-percentbar"></a>クラス Percentbar
    class Percentbar extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                   | 説明                                         |
|------------------------------------------|-----------------------------------------------------|
| public void new(int maxCount, str title) | Percentbar クラスの新しいインスタンスを初期化します。 |
| public void set(int count)               |                                                     |
| public void finalize()                   |                                                     |

### <a name="method-new"></a>メソッド new

Percentbar クラスの新しいインスタンスを初期化します。

    public void new(int maxCount, str title)

#### <a name="parameters"></a>パラメーター

maxCount  

<!-- -->

title  

### <a name="method-set"></a>メソッド set

    public void set(int count)

#### <a name="parameters"></a>パラメーター

カウント  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-performancemonitor"></a>クラス PerformanceMonitor
    class PerformanceMonitor extends Object

PerformanceMonitor クラスは、システムで実行されているプロセスのデータをフェッチします。

### <a name="remarks"></a>備考

いつでもシステムのスナップショットを取得して、システムで実行されている任意のプロセスのカウンター上で移動することができます。

### <a name="examples"></a>例

次の例は、現在実行中のすべてのプロセスの processId および workingset 値を出力します。

    static void pvPerformanceMonitorTest(args a) 
    { 
        int i, j;  
        PerformanceMonitorInstance instance;  
        PerformanceMonitorCounter counter1, counter2;  
        PerformanceMonitor pm = new PerformanceMonitor();  
        // Take a current snapshot of the system. 
        pm.takeSnapshot ();  
        // Traverse all the running processes. 
        for (i= 1; i <= pm.instanceCount(); i++)  
        {  
            instance = pm.instance(i);  
            counter1 = instance.getCounter("ID Process");  
            counter2 = instance.getCounter("Working Set");  
            print instance.name(), " ",  
            counter1.intData(), " ",  
            counter2.intData();  
        } 
        pause;  
    }

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                    |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| public PerformanceMonitorInstance instance(int instanceNo) |                                                                                                |
| public int instanceCount()                                 | インスタンス数 (現在のスナップショットのプロセスの数) を返します。          |
| public int processId()                                     | このメソッドを実行しているプロセスの processId 値を返します。                        |
| public str systemName()                                    |                                                                                                |
| public boolean takeSnapshot(\[str processName\])           |                                                                                                |
| public str toString()                                      | クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。 |
| public void new()                                          | PerformanceMonitor クラスの新しいインスタンスを初期化します。                                    |

### <a name="method-instance"></a>メソッド instance

    public PerformanceMonitorInstance instance(int instanceNo)

#### <a name="parameters"></a>パラメーター

instanceNo  

#### <a name="return-value"></a>戻り値

### <a name="method-instancecount"></a>メソッド instanceCount

インスタンス数 (現在のスナップショットのプロセスの数) を返します。

    public int instanceCount()

#### <a name="return-value"></a>戻り値

現在のスナップショット内のプロセス数。

#### <a name="remarks"></a>備考

現在実行中のプロセスのスナップショットを取得するには、takeSnapshot メソッドを使用します。

#### <a name="examples"></a>例

    static void pvPerformanceMonitorTest(args a) 
    { 
        int i, j; 
        PerformanceMonitorInstance instance; 
        PerformanceMonitorCounter counter1, counter2; 
        PerformanceMonitor pm = new PerformanceMonitor(); 
        // Take a current snapshot of the system. 
        pm.takeSnapshot (); 
        // Traverse all the running processes. 
        for (i= 1; i <= pm.instanceCount(); i++) 
        { 
            instance = pm.instance(i); 
            counter1 = instance.getCounter("ID Process"); 
            counter2 = instance.getCounter("Working Set"); 
            print instance.name(), " ",  
                counter1.intData(), " ",  
                counter2.intData(); 
        } 
        pause; 
    }

### <a name="method-processid"></a>メソッド processId

このメソッドを実行しているプロセスの processId 値を返します。

    public int processId()

#### <a name="return-value"></a>戻り値

このメソッドを実行している、Finance and Operations プロセスの processId 値。

#### <a name="examples"></a>例

    static void processIdDemo(args a) 
    { 
        PerformanceMonitor pm = new PerformanceMonitor(); 
        print pm.processId(); 
        pause; 
    }

### <a name="method-systemname"></a>メソッド systemName

    public str systemName()

#### <a name="return-value"></a>戻り値

### <a name="method-takesnapshot"></a>メソッド takeSnapshot

    public boolean takeSnapshot([str processName])

#### <a name="parameters"></a>パラメーター

processName  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

クラスのテキストの説明。

#### <a name="remarks"></a>備考

既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。 ただし、一部のクラスでは、追加情報が文字列で返されます。

### <a name="method-new"></a>メソッド new

PerformanceMonitor クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-performancemonitorcounter"></a>クラス PerformanceMonitorCounter
    class PerformanceMonitorCounter extends Object

PerformanceMonitorCounter クラスでは、特定のスナップショットの特定のインスタンスに割り当てられているカウンターを識別します。

### <a name="remarks"></a>備考

get メソッドを使用してデータを取得できます。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                 | 説明                                                                                    |
|------------------------|------------------------------------------------------------------------------------------------|
| public int intData()   |                                                                                                |
| public str name()      |                                                                                                |
| public Time timeData() |                                                                                                |
| public str toString()  | クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。 |

### <a name="method-intdata"></a>メソッド intData

    public int intData()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-timedata"></a>メソッド timeData

    public Time timeData()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

クラスのテキストの説明。

#### <a name="remarks"></a>備考

既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。 ただし、一部のクラスでは、追加情報が文字列で返されます。

## <a name="class-performancemonitorinstance"></a>クラス PerformanceMonitorInstance
    class PerformanceMonitorInstance extends Object

PerformanceMonitorInstance クラスは、プロセス モニターが実行されるコンピューターで実行されているプロセスを表します。

### <a name="remarks"></a>備考

このクラスは、プロセス カウンターのクエリを可能にします。 このクラスのオブジェクトを使用してプロセス カウンターをクエリすることができます。 各カウンターは、プロセス パラメーターを表します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                       | 説明                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| public PerformanceMonitorCounter getCounter(str counterName) |                                                                                                |
| public str name()                                            |                                                                                                |
| public str toString()                                        | クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。 |

### <a name="method-getcounter"></a>メソッド getCounter

    public PerformanceMonitorCounter getCounter(str counterName)

#### <a name="parameters"></a>パラメーター

counterName  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

クラスのテキストの説明を返します。

#### <a name="remarks"></a>備考

既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。 ただし、一部のクラスでは、追加情報が文字列で返されます。

## <a name="class-pipeclient"></a>クラス PipeClient
    class PipeClient extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                              | 説明                                         |
|---------------------------------------------------------------------|-----------------------------------------------------|
| public boolean blockingMode(\[boolean block\])                      |                                                     |
| public int errorCode()                                              |                                                     |
| public str read()                                                   |                                                     |
| public boolean write(str buffer)                                    |                                                     |
| public void new(str servername, str pipename, \[boolean blocking\]) | PipeClient クラスの新しいインスタンスを初期化します。 |

### <a name="method-blockingmode"></a>メソッド blockingMode

    public boolean blockingMode([boolean block])

#### <a name="parameters"></a>パラメーター

block  

#### <a name="return-value"></a>戻り値

### <a name="method-errorcode"></a>メソッド errorCode

    public int errorCode()

#### <a name="return-value"></a>戻り値

### <a name="method-read"></a>メソッド read

    public str read()

#### <a name="return-value"></a>戻り値

### <a name="method-write"></a>メソッド write

    public boolean write(str buffer)

#### <a name="parameters"></a>パラメーター

バッファ  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

PipeClient クラスの新しいインスタンスを初期化します。

    public void new(str servername, str pipename, [boolean blocking])

#### <a name="parameters"></a>パラメーター

servername  

<!-- -->

pipename  

<!-- -->

ブロック  

## <a name="class-pipeserver"></a>クラス PipeServer
    class PipeServer extends Object

PipeServer クラスでは、名前付きパイプのサーバー側がサポートされます。

### <a name="remarks"></a>備考

PipeServer オブジェクトが PipeServer.new メソッドを使用して作成されたときに、名前付きパイプが作成されます。 作成されるパイプは、読み取りアクセス権を保有し、メッセージ モードの状態にあります。 パイプの名前には自動的に接頭語 \\\\.\\pipe\\Dynamics が付けられます。 現在のセッション SID は名前の接尾辞になります。 サーバーのパイプ接続に提供されるサポートは、以下のセキュリティ上の理由により制限されています。

-   パイプは、セッションが作成されたコンピュータ上の現在のログオン セッションのみに対してサポートされます。
-   パイプを作成するユーザーは、そのパイプと通信できる唯一のユーザーです。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                              | 説明                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| public boolean blockingMode(\[boolean block\])      |                                                                              |
| public boolean connect()                            | クライアントが名前付きパイプに接続するまで待機します。                             |
| public boolean disconnect()                         | 名前付きパイプ インスタンスのサーバー側をクライアント プロセスから切断します。 |
| public int errorCode()                              |                                                                              |
| public str read()                                   | パイプ クライアントによって書き込まれたとおりに、名前付きパイプからデータを読み取ります。                 |
| public void new(str pipename, \[boolean blocking\]) | PipeServer クラスの新しいインスタンスを作成します。                              |

### <a name="method-blockingmode"></a>メソッド blockingMode

    public boolean blockingMode([boolean block])

#### <a name="parameters"></a>パラメーター

block  

#### <a name="return-value"></a>戻り値

### <a name="method-connect"></a>メソッド connect

クライアントが名前付きパイプに接続するまで待機します。

    public boolean connect()

#### <a name="return-value"></a>戻り値

メソッドが成功する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

クライアントが接続するのを待機している場合は、現在のスレッドをブロックしない場合、PipeServer.connect メソッドを使用しないようにし、代わりに PipeServer.read メソッドを使用してポーリングします。

### <a name="method-disconnect"></a>メソッド disconnect

名前付きパイプ インスタンスのサーバー側をクライアント プロセスから切断します。

    public boolean disconnect()

#### <a name="return-value"></a>戻り値

メソッドが成功する場合は true。それ以外の場合は、false。

### <a name="method-errorcode"></a>メソッド errorCode

    public int errorCode()

#### <a name="return-value"></a>戻り値

### <a name="method-read"></a>メソッド read

パイプ クライアントによって書き込まれたとおりに、名前付きパイプからデータを読み取ります。

    public str read()

#### <a name="return-value"></a>戻り値

データが読み取られた場合に、パイプから読み取られるデータ。

#### <a name="remarks"></a>備考

クライアントが名前付きパイプに接続されていないために、このメソッドが呼び出されたときにデータを使用できないことがあります。 クライアントへの接続を待機する場合は、接続方法を使用します。 ただし、クライアントの接続を待機している現在のスレッドをブロックしない場合、読み取りメソッドを使用してポーリングします。

### <a name="method-new"></a>メソッド new

PipeServer クラスの新しいインスタンスを作成します。

    public void new(str pipename, [boolean blocking])

#### <a name="parameters"></a>パラメーター

pipename  
ブロック動作を使用するかどうかを示すブール値フラグ。 非ブロック モードは、Microsoft LAN Manager バージョン 2.0 との互換性をサポートしており、名前付きパイプで非同期入出力を達成するために使用しないでください。 代わりに、ポーリング技術を使用する必要があります。 読み取りメソッドを参照してください。

<!-- -->

ブロック  
ブロック動作を使用するかどうかを示すブール値フラグ。 非ブロック モードは、Microsoft LAN Manager バージョン 2.0 との互換性をサポートしており、名前付きパイプで非同期入出力を達成するために使用しないでください。 代わりに、ポーリング技術を使用する必要があります。 読み取りメソッドを参照してください。

#### <a name="remarks"></a>備考

いくつかの制限が適用されます。 PipeServer クラスの一般的な説明の例を参照してください。

## <a name="class-presenceinfo"></a>クラス PresenceInfo
    class PresenceInfo extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                | 説明                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------|
| public str contactName(\[str contactName\])                           |                                                       |
| public str emailAddress(int index)                                    |                                                       |
| public str emailAlias(int index)                                      |                                                       |
| public int emailCount()                                               |                                                       |
| public str phoneAlias(int index)                                      |                                                       |
| public int phoneCount()                                               |                                                       |
| public str phoneNumber(int index)                                     |                                                       |
| public str sipAddress(\[str sipAddress\])                             |                                                       |
| public void finalize()                                                |                                                       |
| public void new()                                                     | PresenceInfo クラスの新しいインスタンスを初期化します。 |
| public void addEmailAddress(\[str emailAlias\], \[str emailAddress\]) |                                                       |
| public void addPhoneNumber(\[str phoneAlias\], \[str phoneNumber\])   |                                                       |

### <a name="method-contactname"></a>メソッド contactName

    public str contactName([str contactName])

#### <a name="parameters"></a>パラメーター

contactName  

#### <a name="return-value"></a>戻り値

### <a name="method-emailaddress"></a>メソッド emailAddress

    public str emailAddress(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-emailalias"></a>メソッド emailAlias

    public str emailAlias(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-emailcount"></a>メソッド emailCount

    public int emailCount()

#### <a name="return-value"></a>戻り値

### <a name="method-phonealias"></a>メソッド phoneAlias

    public str phoneAlias(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-phonecount"></a>メソッド phoneCount

    public int phoneCount()

#### <a name="return-value"></a>戻り値

### <a name="method-phonenumber"></a>メソッド phoneNumber

    public str phoneNumber(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-sipaddress"></a>メソッド sipAddress

    public str sipAddress([str sipAddress])

#### <a name="parameters"></a>パラメーター

sipAddress  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

PresenceInfo クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-addemailaddress"></a>メソッド addEmailAddress

    public void addEmailAddress([str emailAlias], [str emailAddress])

#### <a name="parameters"></a>パラメーター

emailAlias  

<!-- -->

emailAddress  

### <a name="method-addphonenumber"></a>メソッド addPhoneNumber

    public void addPhoneNumber([str phoneAlias], [str phoneNumber])

#### <a name="parameters"></a>パラメーター

phoneAlias  

<!-- -->

phoneNumber  

## <a name="class-printjobsettings"></a>クラス PrintJobSettings
    class PrintJobSettings extends Object

PrintJobSettings クラスを使用すると、ユーザーがプリンターおよびそのデバイス設定にアクセスできます。

### <a name="remarks"></a>備考

PrintJobSettings は、SysPrintForm フォームにより使用されます。

### <a name="examples"></a>例

次の例では、既定のプリンターの名前を書き込み、使用可能なプリンターを一覧表示します。

    void printerInfo() 
    {    
        printJobSettings pjs; 
        int i; 
        pjs = new PrintJobSettings(); 
        print "The default printer is ", pjs.DeviceName(); 
        print "There are ", pjs.GetNumberOfPrinters(), " printers"; 
        i = 1; 
        while (i<=pjs.GetNumberOfPrinters())  
        { 
            print "Printer No. ", i, " is ", pjs.GetPrinter(i);  
            i++; 
        } 
        pause; 
    }

### <a name="methods"></a>メソッド

| 方法                                                                                                  | 説明                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| public boolean allPages(\[boolean all\])                                                                | sysPrintForm を実行するときに、すべてまたはページのオプション ボタンを選択するかどうかをコントロールします。 |
| public boolean appendToTextFile(\[boolean append\])                                                     |                                                                                                   |
| public boolean banding()                                                                                |                                                                                                   |
| public PrintJobSettings clientPrintJobSettings()                                                        |                                                                                                   |
| public boolean collate(\[boolean collate\])                                                             |                                                                                                   |
| public int copies(\[int numberOfCopies\])                                                               |                                                                                                   |
| public str copyDescription(int number, \[str description\])                                             |                                                                                                   |
| public str deviceName(\[str device\], \[ClassRunMode runOn\])                                           | プリンターを選択するか、選択されているプリンター デバイス名を取得します。                            |
| public boolean doNotOverwrite(\[boolean warn\])                                                         |                                                                                                   |
| public boolean enableCopies(\[boolean enable\])                                                         |                                                                                                   |
| public boolean enableDevice(\[boolean enable\])                                                         |                                                                                                   |
| public boolean enablePages(\[boolean enable\])                                                          |                                                                                                   |
| public boolean enableProperties(\[boolean enable\])                                                     |                                                                                                   |
| public boolean enableStoreInPrintArchive(\[boolean enable\])                                            |                                                                                                   |
| public boolean enableTarget(\[boolean enable\])                                                         |                                                                                                   |
| public int facename2number(\[str facename\])                                                            |                                                                                                   |
| public str fileName(\[str FileName\])                                                                   |                                                                                                   |
| public boolean fitToPage(\[boolean fit\])                                                               |                                                                                                   |
| public PrintFormat format(\[PrintFormat format\])                                                       |                                                                                                   |
| public int from(\[int fromPage\])                                                                       |                                                                                                   |
| public str getFacename(int number)                                                                      |                                                                                                   |
| public str getFacenameInfo(int number)                                                                  |                                                                                                   |
| public Struct getFontInfo(str fontName)                                                                 |                                                                                                   |
| public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)                             |                                                                                                   |
| public int getNumberOfClientPrinters()                                                                  |                                                                                                   |
| public int getNumberOfFacenames()                                                                       |                                                                                                   |
| public int getNumberOfPrinters()                                                                        | コンピューターに設定されているプリンターの数を返します。                                   |
| public int getNumberOfServerPrinters()                                                                  |                                                                                                   |
| public int getNumberOfTrays()                                                                           |                                                                                                   |
| public str getPrinter(int number)                                                                       | プリンターの deviceName を取得します。                                                                 |
| public ClassRunMode getRunOn(int number)                                                                |                                                                                                   |
| public PrintMedium getTarget()                                                                          |                                                                                                   |
| public int getTray(int number)                                                                          |                                                                                                   |
| public str getTrayName(int number)                                                                      |                                                                                                   |
| public Int64 hDC()                                                                                      |                                                                                                   |
| public boolean lockDestinationProperties(\[boolean warn\])                                              |                                                                                                   |
| public str mailCc(\[str MailCc\])                                                                       |                                                                                                   |
| public str mailSubject(\[str MailSubject\])                                                             |                                                                                                   |
| public str mailTo(\[str MailTo\])                                                                       |                                                                                                   |
| public int numberOfCopyDescriptions(int number)                                                         |                                                                                                   |
| public boolean outputToClient(\[boolean toClient\])                                                     |                                                                                                   |
| public boolean outputToPrnFile(\[boolean writePrnFile\])                                                |                                                                                                   |
| public container packNamesAndPrinterData()                                                              |                                                                                                   |
| public container packPageSettings()                                                                     | ページの書式設定時に選択されているデータをコンテナーに格納します。                           |
| public container packPrinterSettings()                                                                  |                                                                                                   |
| public container packPrintJobSettings()                                                                 |                                                                                                   |
| public container packSubtotalSettings()                                                                 |                                                                                                   |
| public int pageCopy2Tray(int pageNumber, \[int copyNumber\])                                            |                                                                                                   |
| public boolean pageFormatting()                                                                         |                                                                                                   |
| public PrinterOrientation paperOrientation(\[PrinterOrientation orientation\])                          |                                                                                                   |
| public int paperTray(\[int tray\])                                                                      |                                                                                                   |
| public int paperTrayRaw(\[int tray\])                                                                   |                                                                                                   |
| public int performanceTest(\[int loops\])                                                               |                                                                                                   |
| public PrintFormat preferredFileFormat(\[PrintFormat format\])                                          |                                                                                                   |
| public PrintFormat preferredMailFormat(\[PrintFormat format\])                                          |                                                                                                   |
| public PrinterOrientation preferredOrientation(\[PrinterOrientation orientation\])                      |                                                                                                   |
| public PrintMedium preferredTarget(\[PrintMedium target\])                                              |                                                                                                   |
| public int printerAttributes()                                                                          |                                                                                                   |
| public int printerAveragePPM()                                                                          |                                                                                                   |
| public str printerComment()                                                                             |                                                                                                   |
| public str printerDatatype()                                                                            |                                                                                                   |
| public int printerDefaultPriority()                                                                     |                                                                                                   |
| public str printerDriverName()                                                                          |                                                                                                   |
| public str printerLocation()                                                                            |                                                                                                   |
| public int printerPageHeight()                                                                          |                                                                                                   |
| public int printerPageWidth()                                                                           |                                                                                                   |
| public int printerPaper()                                                                               |                                                                                                   |
| public str printerParameters()                                                                          |                                                                                                   |
| public str printerPortName()                                                                            |                                                                                                   |
| public str printerPrinterName()                                                                         |                                                                                                   |
| public str printerPrintProcessor()                                                                      |                                                                                                   |
| public int printerPriority()                                                                            |                                                                                                   |
| public int printerQueuedJobs()                                                                          |                                                                                                   |
| public ClassRunMode printerRunOn()                                                                      |                                                                                                   |
| public str printerSepFile()                                                                             |                                                                                                   |
| public str printerServerName()                                                                          |                                                                                                   |
| public boolean printerSettings(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\]) |                                                                                                   |
| public str printerShareName()                                                                           |                                                                                                   |
| public TimeOfDay printerStartTime()                                                                     |                                                                                                   |
| public int printerStatus()                                                                              |                                                                                                   |
| public TimeOfDay printerUntilTime()                                                                     |                                                                                                   |
| public ReportRun reportRun()                                                                            |                                                                                                   |
| public str requestedDeviceName()                                                                        |                                                                                                   |
| public ClassRunMode requestedRunOn()                                                                    |                                                                                                   |
| public boolean runClient()                                                                              |                                                                                                   |
| public boolean runServer()                                                                              |                                                                                                   |
| public int sectionsPerPage(\[int sectionsPerPage\])                                                     |                                                                                                   |
| public PrintMedium setTarget(PrintMedium target)                                                        | 印刷メディアを設定します。                                                                            |
| public boolean singleLargePage(\[boolean singleLargePage\])                                             |                                                                                                   |
| public boolean skipBitmapsInRTF(\[boolean skipBitmaps\])                                                | .rtf ファイルにレポートを印刷するときにビットマップを含めるかどうかをコントロールします。                   |
| public boolean storeInPrintArchive(\[boolean store\])                                                   |                                                                                                   |
| public boolean suppressScalingMessage(\[boolean suppress\])                                             |                                                                                                   |
| public int to(\[int toPage\])                                                                           |                                                                                                   |
| public str toString()                                                                                   | 現在のオブジェクトを表す文字列を返します。                                              |
| public boolean unpackPageSettings(container settings)                                                   | 用紙サイズと向きなど、ページ設定を設定します。                                       |
| public boolean unpackPrinterSettings(container settings)                                                |                                                                                                   |
| public boolean unpackPrintJobSettings(container settings)                                               |                                                                                                   |
| public boolean unpackSubtotalSettings(container settings)                                               |                                                                                                   |
| public int unprintableBottom()                                                                          |                                                                                                   |
| public int unprintableLeft()                                                                            |                                                                                                   |
| public int unprintableRight()                                                                           |                                                                                                   |
| public int unprintableTop()                                                                             | 用紙の最上部から用紙の印刷可能な範囲までの距離を示します。              |
| public ReportOutputUserType viewerType(\[ReportOutputUserType type\])                                   |                                                                                                   |
| public int virtualPageHeight(\[int height\])                                                            |                                                                                                   |
| public boolean warnIfFileExists(\[boolean warn\])                                                       |                                                                                                   |
| public void enableBody(\[TableId tableId\])                                                             |                                                                                                   |
| public void new(\[container Settings\], \[boolean infoOnly\])                                           | Object クラスの新しいインスタンスを初期化します。                                                   |
| public void addTrayPageCopy(int tray, int pageNumber, \[int copyNumber\])                               |                                                                                                   |
| public void disableBody(\[TableId tableId\])                                                            |                                                                                                   |
| public void clearTrayPageCopy()                                                                         |                                                                                                   |
| public void rulerInch()                                                                                 |                                                                                                   |
| public void finalize()                                                                                  |                                                                                                   |
| public void rulerOff()                                                                                  |                                                                                                   |
| public void rulerMetric()                                                                               |                                                                                                   |

### <a name="method-allpages"></a>メソッド allPages

sysPrintForm を実行するときに、すべてまたはページのオプション ボタンを選択するかどうかをコントロールします。

    public boolean allPages([boolean all])

#### <a name="parameters"></a>パラメーター

すべて  
true の場合、すべてのオプション ボタンが選択されるブール値; それ以外の場合は、ページ オプション ボタンが選択されます。

#### <a name="return-value"></a>戻り値

すべてのオプション ボタンを選択する必要がある場合は true。それ以外の場合は false で、ページのオプション ボタンが選択されます。

#### <a name="remarks"></a>備考

このメソッドは、sysPrintForm によって内部的に使用されます。

#### <a name="examples"></a>例

次の例では、2 〜 4 のページを印刷し、[すべてのオプション] ボタンではなく [ページのオプション] ボタンを選択します。

    static void PrintingToPDF(Args _args) 
    { 
        Args                args; 
        ReportRun           rr; 
        str reportName = 'Cust'; 
        int i; 
        int numReports = 10; 
        args = new Args(reportName); 
        rr = new ReportRun(args,''); 
        rr.setTarget(Printmedium::File); 
        rr.printJobSettings().format(PrintFormat::RTF); 
        rr.printJobSettings().fileName("C:\\tmp\\Cust_ReportRange2.rtf"); 
        // Select the Pages option button rather than the All option button. 
        rr.printJobSettings().allPages(false); 
        rr.printJobSettings().from(2); 
        rr.printJobSettings().to(4); 
        rr.query().interactive(false); 
        rr.report().interactive(false); 
        rr.run(); 
    }

### <a name="method-appendtotextfile"></a>メソッド appendToTextFile

    public boolean appendToTextFile([boolean append])

#### <a name="parameters"></a>パラメーター

append  

#### <a name="return-value"></a>戻り値

### <a name="method-banding"></a>メソッド banding

    public boolean banding()

#### <a name="return-value"></a>戻り値

### <a name="method-clientprintjobsettings"></a>メソッド clientPrintJobSettings

    public PrintJobSettings clientPrintJobSettings()

#### <a name="return-value"></a>戻り値

### <a name="method-collate"></a>メソッド collate

    public boolean collate([boolean collate])

#### <a name="parameters"></a>パラメーター

collate  

#### <a name="return-value"></a>戻り値

### <a name="method-copies"></a>メソッド copies

    public int copies([int numberOfCopies])

#### <a name="parameters"></a>パラメーター

numberOfCopies  

#### <a name="return-value"></a>戻り値

### <a name="method-copydescription"></a>メソッド copyDescription

    public str copyDescription(int number, [str description])

#### <a name="parameters"></a>パラメーター

数値  

<!-- -->

description  

#### <a name="return-value"></a>戻り値

### <a name="method-devicename"></a>メソッド deviceName

プリンターを選択するか、選択されているプリンター デバイス名を取得します。

    public str deviceName([str device], [ClassRunMode runOn])

#### <a name="parameters"></a>パラメーター

デバイス  

<!-- -->

runOn  

#### <a name="return-value"></a>戻り値

選択したプリンターの deviceName。

#### <a name="remarks"></a>備考

選択されるプリンターの deviceName は、getPrinter メソッドを使用して検出できます。

#### <a name="examples"></a>例

このジョブは、利用可能なプリンターと印刷できない領域を一覧表示します。

    static void aaaKJ(args a) 
    { 
        printJobSettings pjs; 
        str printer; 
        int i; 
        pjs = new printJobSettings(); 
        for (i=1; i<=pjs.GetNumberOfPrinters(); i++) 
        { 
            printer = pjs.GetPrinter(i); 
            pjs.DeviceName(printer); 
            print "printer No. ",i, " has name ",  printer; 
            print "   left:  ", pjs.UnprintableLeft(),   "/100 mm"; 
            print "   right: ", pjs.UnprintableRight(),  "/100 mm"; 
            print "   top:   ", pjs.UnprintableTop(),    "/100 mm"; 
            print "   bottom:", pjs.UnprintableBottom(), "/100 mm"; 
        } 
        pause; 
    }

### <a name="method-donotoverwrite"></a>メソッド doNotOverwrite

    public boolean doNotOverwrite([boolean warn])

#### <a name="parameters"></a>パラメーター

警告  

#### <a name="return-value"></a>戻り値

### <a name="method-enablecopies"></a>メソッド enableCopies

    public boolean enableCopies([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  

#### <a name="return-value"></a>戻り値

### <a name="method-enabledevice"></a>メソッド enableDevice

    public boolean enableDevice([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  

#### <a name="return-value"></a>戻り値

### <a name="method-enablepages"></a>メソッド enablePages

    public boolean enablePages([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  

#### <a name="return-value"></a>戻り値

### <a name="method-enableproperties"></a>メソッド enableProperties

    public boolean enableProperties([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  

#### <a name="return-value"></a>戻り値

### <a name="method-enablestoreinprintarchive"></a>メソッド enableStoreInPrintArchive

    public boolean enableStoreInPrintArchive([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  

#### <a name="return-value"></a>戻り値

### <a name="method-enabletarget"></a>メソッド enableTarget

    public boolean enableTarget([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  

#### <a name="return-value"></a>戻り値

### <a name="method-facename2number"></a>メソッド facename2number

    public int facename2number([str facename])

#### <a name="parameters"></a>パラメーター

facename  

#### <a name="return-value"></a>戻り値

### <a name="method-filename"></a>メソッド fileName

    public str fileName([str FileName])

#### <a name="parameters"></a>パラメーター

FileName  

#### <a name="return-value"></a>戻り値

### <a name="method-fittopage"></a>メソッド fitToPage

    public boolean fitToPage([boolean fit])

#### <a name="parameters"></a>パラメーター

fit  

#### <a name="return-value"></a>戻り値

### <a name="method-format"></a>メソッド format

    public PrintFormat format([PrintFormat format])

#### <a name="parameters"></a>パラメーター

形式  

#### <a name="return-value"></a>戻り値

### <a name="method-from"></a>メソッド from

    public int from([int fromPage])

#### <a name="parameters"></a>パラメーター

fromPage  

#### <a name="return-value"></a>戻り値

### <a name="method-getfacename"></a>メソッド getFacename

    public str getFacename(int number)

#### <a name="parameters"></a>パラメーター

数値  

#### <a name="return-value"></a>戻り値

### <a name="method-getfacenameinfo"></a>メソッド getFacenameInfo

    public str getFacenameInfo(int number)

#### <a name="parameters"></a>パラメーター

数値  

#### <a name="return-value"></a>戻り値

### <a name="method-getfontinfo"></a>メソッド getFontInfo

    public Struct getFontInfo(str fontName)

#### <a name="parameters"></a>パラメーター

fontName  

#### <a name="return-value"></a>戻り値

### <a name="method-getglyphwidthsarray"></a>メソッド getGlyphWidthsArray

    public Array getGlyphWidthsArray(str fontName, int firstChar, int lastChar)

#### <a name="parameters"></a>パラメーター

fontName  

<!-- -->

firstChar  

<!-- -->

lastChar  

#### <a name="return-value"></a>戻り値

### <a name="method-getnumberofclientprinters"></a>メソッド getNumberOfClientPrinters

    public int getNumberOfClientPrinters()

#### <a name="return-value"></a>戻り値

### <a name="method-getnumberoffacenames"></a>メソッド getNumberOfFacenames

    public int getNumberOfFacenames()

#### <a name="return-value"></a>戻り値

### <a name="method-getnumberofprinters"></a>メソッド getNumberOfPrinters

コンピューターに設定されているプリンターの数を返します。

    public int getNumberOfPrinters()

#### <a name="return-value"></a>戻り値

コンピューターに設定されているプリンターの数。

### <a name="method-getnumberofserverprinters"></a>メソッド getNumberOfServerPrinters

    public int getNumberOfServerPrinters()

#### <a name="return-value"></a>戻り値

### <a name="method-getnumberoftrays"></a>メソッド getNumberOfTrays

    public int getNumberOfTrays()

#### <a name="return-value"></a>戻り値

### <a name="method-getprinter"></a>メソッド getPrinter

プリンターの deviceName を取得します。

    public str getPrinter(int number)

#### <a name="parameters"></a>パラメーター

数値  
1 から使用可能なプリンターの数までの値。

#### <a name="return-value"></a>戻り値

指定されたプリンター番号の deviceName。

#### <a name="examples"></a>例

    printJobSettings pjs; 
    int i; 
    pjs = new printJobSettings(); 
    i = 1; 
    while (i<=pjs.GetNumberOfPrinters()) 
    { 
        print "Printer No. ", i, " is ", pjs.GetPrinter(i); 
        i++; 
    }

### <a name="method-getrunon"></a>メソッド getRunOn

    public ClassRunMode getRunOn(int number)

#### <a name="parameters"></a>パラメーター

数値  

#### <a name="return-value"></a>戻り値

### <a name="method-gettarget"></a>メソッド getTarget

    public PrintMedium getTarget()

#### <a name="return-value"></a>戻り値

### <a name="method-gettray"></a>メソッド getTray

    public int getTray(int number)

#### <a name="parameters"></a>パラメーター

数値  

#### <a name="return-value"></a>戻り値

### <a name="method-gettrayname"></a>メソッド getTrayName

    public str getTrayName(int number)

#### <a name="parameters"></a>パラメーター

数値  

#### <a name="return-value"></a>戻り値

### <a name="method-hdc"></a>メソッド hDC

    public Int64 hDC()

#### <a name="return-value"></a>戻り値

### <a name="method-lockdestinationproperties"></a>メソッド lockDestinationProperties

    public boolean lockDestinationProperties([boolean warn])

#### <a name="parameters"></a>パラメーター

警告  

#### <a name="return-value"></a>戻り値

### <a name="method-mailcc"></a>メソッド mailCc

    public str mailCc([str MailCc])

#### <a name="parameters"></a>パラメーター

MailCc  

#### <a name="return-value"></a>戻り値

### <a name="method-mailsubject"></a>メソッド mailSubject

    public str mailSubject([str MailSubject])

#### <a name="parameters"></a>パラメーター

MailSubject  

#### <a name="return-value"></a>戻り値

### <a name="method-mailto"></a>メソッド mailTo

    public str mailTo([str MailTo])

#### <a name="parameters"></a>パラメーター

MailTo  

#### <a name="return-value"></a>戻り値

### <a name="method-numberofcopydescriptions"></a>メソッド numberOfCopyDescriptions

    public int numberOfCopyDescriptions(int number)

#### <a name="parameters"></a>パラメーター

数値  

#### <a name="return-value"></a>戻り値

### <a name="method-outputtoclient"></a>メソッド outputToClient

    public boolean outputToClient([boolean toClient])

#### <a name="parameters"></a>パラメーター

toClient  

#### <a name="return-value"></a>戻り値

### <a name="method-outputtoprnfile"></a>メソッド outputToPrnFile

    public boolean outputToPrnFile([boolean writePrnFile])

#### <a name="parameters"></a>パラメーター

writePrnFile  

#### <a name="return-value"></a>戻り値

### <a name="method-packnamesandprinterdata"></a>メソッド packNamesAndPrinterData

    public container packNamesAndPrinterData()

#### <a name="return-value"></a>戻り値

### <a name="method-packpagesettings"></a>メソッド packPageSettings

ページの書式設定時に選択されているデータをコンテナーに格納します。

    public container packPageSettings()

#### <a name="return-value"></a>戻り値

ページの書式設定時に選択されているデータを保持するコンテナーです。

#### <a name="remarks"></a>備考

返されたコンテナーは、unpackPageSettings メソッドへの入力として使用できます。

### <a name="method-packprintersettings"></a>メソッド packPrinterSettings

    public container packPrinterSettings()

#### <a name="return-value"></a>戻り値

### <a name="method-packprintjobsettings"></a>メソッド packPrintJobSettings

    public container packPrintJobSettings()

#### <a name="return-value"></a>戻り値

### <a name="method-packsubtotalsettings"></a>メソッド packSubtotalSettings

    public container packSubtotalSettings()

#### <a name="return-value"></a>戻り値

### <a name="method-pagecopy2tray"></a>メソッド pageCopy2Tray

    public int pageCopy2Tray(int pageNumber, [int copyNumber])

#### <a name="parameters"></a>パラメーター

pageNumber  

<!-- -->

copyNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-pageformatting"></a>メソッド pageFormatting

    public boolean pageFormatting()

#### <a name="return-value"></a>戻り値

### <a name="method-paperorientation"></a>メソッド paperOrientation

    public PrinterOrientation paperOrientation([PrinterOrientation orientation])

#### <a name="parameters"></a>パラメーター

orientation  

#### <a name="return-value"></a>戻り値

### <a name="method-papertray"></a>メソッド paperTray

    public int paperTray([int tray])

#### <a name="parameters"></a>パラメーター

トレイ  

#### <a name="return-value"></a>戻り値

### <a name="method-papertrayraw"></a>メソッド paperTrayRaw

    public int paperTrayRaw([int tray])

#### <a name="parameters"></a>パラメーター

トレイ  

#### <a name="return-value"></a>戻り値

### <a name="method-performancetest"></a>メソッド performanceTest

    public int performanceTest([int loops])

#### <a name="parameters"></a>パラメーター

loops  

#### <a name="return-value"></a>戻り値

### <a name="method-preferredfileformat"></a>メソッド preferredFileFormat

    public PrintFormat preferredFileFormat([PrintFormat format])

#### <a name="parameters"></a>パラメーター

形式  

#### <a name="return-value"></a>戻り値

### <a name="method-preferredmailformat"></a>メソッド preferredMailFormat

    public PrintFormat preferredMailFormat([PrintFormat format])

#### <a name="parameters"></a>パラメーター

形式  

#### <a name="return-value"></a>戻り値

### <a name="method-preferredorientation"></a>メソッド preferredOrientation

    public PrinterOrientation preferredOrientation([PrinterOrientation orientation])

#### <a name="parameters"></a>パラメーター

orientation  

#### <a name="return-value"></a>戻り値

### <a name="method-preferredtarget"></a>メソッド preferredTarget

    public PrintMedium preferredTarget([PrintMedium target])

#### <a name="parameters"></a>パラメーター

target  

#### <a name="return-value"></a>戻り値

### <a name="method-printerattributes"></a>メソッド printerAttributes

    public int printerAttributes()

#### <a name="return-value"></a>戻り値

### <a name="method-printeraverageppm"></a>メソッド printerAveragePPM

    public int printerAveragePPM()

#### <a name="return-value"></a>戻り値

### <a name="method-printercomment"></a>メソッド printerComment

    public str printerComment()

#### <a name="return-value"></a>戻り値

### <a name="method-printerdatatype"></a>メソッド printerDatatype

    public str printerDatatype()

#### <a name="return-value"></a>戻り値

### <a name="method-printerdefaultpriority"></a>メソッド printerDefaultPriority

    public int printerDefaultPriority()

#### <a name="return-value"></a>戻り値

### <a name="method-printerdrivername"></a>メソッド printerDriverName

    public str printerDriverName()

#### <a name="return-value"></a>戻り値

### <a name="method-printerlocation"></a>メソッド printerLocation

    public str printerLocation()

#### <a name="return-value"></a>戻り値

### <a name="method-printerpageheight"></a>メソッド printerPageHeight

    public int printerPageHeight()

#### <a name="return-value"></a>戻り値

### <a name="method-printerpagewidth"></a>メソッド printerPageWidth

    public int printerPageWidth()

#### <a name="return-value"></a>戻り値

### <a name="method-printerpaper"></a>メソッド printerPaper

    public int printerPaper()

#### <a name="return-value"></a>戻り値

### <a name="method-printerparameters"></a>メソッド printerParameters

    public str printerParameters()

#### <a name="return-value"></a>戻り値

### <a name="method-printerportname"></a>メソッド printerPortName

    public str printerPortName()

#### <a name="return-value"></a>戻り値

### <a name="method-printerprintername"></a>メソッド printerPrinterName

    public str printerPrinterName()

#### <a name="return-value"></a>戻り値

### <a name="method-printerprintprocessor"></a>メソッド printerPrintProcessor

    public str printerPrintProcessor()

#### <a name="return-value"></a>戻り値

### <a name="method-printerpriority"></a>メソッド printerPriority

    public int printerPriority()

#### <a name="return-value"></a>戻り値

### <a name="method-printerqueuedjobs"></a>メソッド printerQueuedJobs

    public int printerQueuedJobs()

#### <a name="return-value"></a>戻り値

### <a name="method-printerrunon"></a>メソッド printerRunOn

    public ClassRunMode printerRunOn()

#### <a name="return-value"></a>戻り値

### <a name="method-printersepfile"></a>メソッド printerSepFile

    public str printerSepFile()

#### <a name="return-value"></a>戻り値

### <a name="method-printerservername"></a>メソッド printerServerName

    public str printerServerName()

#### <a name="return-value"></a>戻り値

### <a name="method-printersettings"></a>メソッド printerSettings

    public boolean printerSettings(str formName, [xArgs args], [ReportRun reportRun], [int showWhat])

#### <a name="parameters"></a>パラメーター

formName  

<!-- -->

args  

<!-- -->

reportRun  

<!-- -->

showWhat  

#### <a name="return-value"></a>戻り値

### <a name="method-printersharename"></a>メソッド printerShareName

    public str printerShareName()

#### <a name="return-value"></a>戻り値

### <a name="method-printerstarttime"></a>メソッド printerStartTime

    public TimeOfDay printerStartTime()

#### <a name="return-value"></a>戻り値

### <a name="method-printerstatus"></a>メソッド printerStatus

    public int printerStatus()

#### <a name="return-value"></a>戻り値

### <a name="method-printeruntiltime"></a>メソッド printerUntilTime

    public TimeOfDay printerUntilTime()

#### <a name="return-value"></a>戻り値

### <a name="method-reportrun"></a>メソッド reportRun

    public ReportRun reportRun()

#### <a name="return-value"></a>戻り値

### <a name="method-requesteddevicename"></a>メソッド requestedDeviceName

    public str requestedDeviceName()

#### <a name="return-value"></a>戻り値

### <a name="method-requestedrunon"></a>メソッド requestedRunOn

    public ClassRunMode requestedRunOn()

#### <a name="return-value"></a>戻り値

### <a name="method-runclient"></a>メソッド runClient

    public boolean runClient()

#### <a name="return-value"></a>戻り値

### <a name="method-runserver"></a>メソッド runServer

    public boolean runServer()

#### <a name="return-value"></a>戻り値

### <a name="method-sectionsperpage"></a>メソッド sectionsPerPage

    public int sectionsPerPage([int sectionsPerPage])

#### <a name="parameters"></a>パラメーター

sectionsPerPage  

#### <a name="return-value"></a>戻り値

### <a name="method-settarget"></a>メソッド setTarget

印刷メディアを設定します。

    public PrintMedium setTarget(PrintMedium target)

#### <a name="parameters"></a>パラメーター

target  
印刷メディア。

#### <a name="return-value"></a>戻り値

印刷メディア。

### <a name="method-singlelargepage"></a>メソッド singleLargePage

    public boolean singleLargePage([boolean singleLargePage])

#### <a name="parameters"></a>パラメーター

singleLargePage  

#### <a name="return-value"></a>戻り値

### <a name="method-skipbitmapsinrtf"></a>メソッド skipBitmapsInRTF

.rtf ファイルにレポートを印刷するときにビットマップを含めるかどうかをコントロールします。

    public boolean skipBitmapsInRTF([boolean skipBitmaps])

#### <a name="parameters"></a>パラメーター

skipBitmaps  
ビットマップが含まれるかどうかを判断するブール フラグ; オプション。

#### <a name="return-value"></a>戻り値

ビットマップが含まれる場合は true。それ以外の場合は、false。

### <a name="method-storeinprintarchive"></a>メソッド storeInPrintArchive

    public boolean storeInPrintArchive([boolean store])

#### <a name="parameters"></a>パラメーター

店舗  

#### <a name="return-value"></a>戻り値

### <a name="method-suppressscalingmessage"></a>メソッド suppressScalingMessage

    public boolean suppressScalingMessage([boolean suppress])

#### <a name="parameters"></a>パラメーター

suppress  

#### <a name="return-value"></a>戻り値

### <a name="method-to"></a>メソッド to

    public int to([int toPage])

#### <a name="parameters"></a>パラメーター

toPage  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。

### <a name="method-unpackpagesettings"></a>メソッド unpackPageSettings

用紙サイズと向きなど、ページ設定を設定します。

    public boolean unpackPageSettings(container settings)

#### <a name="parameters"></a>パラメーター

設定  
packPageSettings メソッドを呼び出して取得されるコンテナーです。

#### <a name="return-value"></a>戻り値

pageSettings が正常に変更された場合は true。pageSettings が既定値に設定された場合は false。

#### <a name="remarks"></a>備考

reportDesign クラスと report クラスには、同じ名前のメソッドがあります。

### <a name="method-unpackprintersettings"></a>メソッド unpackPrinterSettings

    public boolean unpackPrinterSettings(container settings)

#### <a name="parameters"></a>パラメーター

設定  

#### <a name="return-value"></a>戻り値

### <a name="method-unpackprintjobsettings"></a>メソッド unpackPrintJobSettings

    public boolean unpackPrintJobSettings(container settings)

#### <a name="parameters"></a>パラメーター

設定  

#### <a name="return-value"></a>戻り値

### <a name="method-unpacksubtotalsettings"></a>メソッド unpackSubtotalSettings

    public boolean unpackSubtotalSettings(container settings)

#### <a name="parameters"></a>パラメーター

設定  

#### <a name="return-value"></a>戻り値

### <a name="method-unprintablebottom"></a>メソッド unprintableBottom

    public int unprintableBottom()

#### <a name="return-value"></a>戻り値

### <a name="method-unprintableleft"></a>メソッド unprintableLeft

    public int unprintableLeft()

#### <a name="return-value"></a>戻り値

### <a name="method-unprintableright"></a>メソッド unprintableRight

    public int unprintableRight()

#### <a name="return-value"></a>戻り値

### <a name="method-unprintabletop"></a>メソッド unprintableTop

用紙の最上部から用紙の印刷可能な範囲までの距離を示します。

    public int unprintableTop()

#### <a name="return-value"></a>戻り値

印刷できない領域のサイズ。単位は 100 分の 1 ミリメートルです。

#### <a name="remarks"></a>備考

レポートでは、reportDesign の topMargin を unprintableTop よりも小さくしてはなりません。

#### <a name="examples"></a>例

    static void printerInfo(args a) 
    { 
        printJobSettings pjs; 
        str printer; 
        int i; 
        pjs = new printJobSettings(); 
        for (i=1; i<=pjs.GetNumberOfPrinters(); i++) 
        { 
            printer = pjs.GetPrinter(i); 
            pjs.DeviceName(printer); 
            print "printer No. ",i, " has name ",  printer; 
            print "   left:   ", pjs.UnprintableLeft(),   "/100 mm"; 
            print "   right:  ", pjs.UnprintableRight(),  "/100 mm"; 
            print "   totalWidth: ", pjs.UnprintableLeft() +  
                pjs.PrinterPageWidth() + pjs.UnprintableRight(); 
            print "   top:    ", pjs.UnprintableTop(),    "/100 mm"; 
            print "   bottom: ", pjs.UnprintableBottom(), "/100 mm"; 
            print "   totalHeight: ", pjs.UnprintableTop() +  
                pjs.PrinterPageHeight() + pjs.UnprintableBottom(); 
        } 
        pause; 
    }

### <a name="method-viewertype"></a>メソッド viewerType

    public ReportOutputUserType viewerType([ReportOutputUserType type])

#### <a name="parameters"></a>パラメーター

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-virtualpageheight"></a>メソッド virtualPageHeight

    public int virtualPageHeight([int height])

#### <a name="parameters"></a>パラメーター

height  

#### <a name="return-value"></a>戻り値

### <a name="method-warniffileexists"></a>メソッド warnIfFileExists

    public boolean warnIfFileExists([boolean warn])

#### <a name="parameters"></a>パラメーター

警告  

#### <a name="return-value"></a>戻り値

### <a name="method-enablebody"></a>メソッド enableBody

    public void enableBody([TableId tableId])

#### <a name="parameters"></a>パラメーター

tableId  

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new([container Settings], [boolean infoOnly])

#### <a name="parameters"></a>パラメーター

設定  

<!-- -->

infoOnly  

### <a name="method-addtraypagecopy"></a>メソッド addTrayPageCopy

    public void addTrayPageCopy(int tray, int pageNumber, [int copyNumber])

#### <a name="parameters"></a>パラメーター

トレイ  

<!-- -->

pageNumber  

<!-- -->

copyNumber  

### <a name="method-disablebody"></a>メソッド disableBody

    public void disableBody([TableId tableId])

#### <a name="parameters"></a>パラメーター

tableId  

### <a name="method-cleartraypagecopy"></a>メソッド clearTrayPageCopy

    public void clearTrayPageCopy()

### <a name="method-rulerinch"></a>メソッド rulerInch

    public void rulerInch()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-ruleroff"></a>メソッド rulerOff

    public void rulerOff()

### <a name="method-rulermetric"></a>メソッド rulerMetric

    public void rulerMetric()

## <a name="class-profiler"></a>クラス プロファイラー
    class profiler extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 説明                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| public int collected()                                                                                                                                                                                                                                                                                                                                                                                                                                          |                                                      |
| public int flushInterval(\[int interval\])                                                                                                                                                                                                                                                                                                                                                                                                                      |                                                      |
| public AnyType profileOff()                                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                      |
| public AnyType profileOn(str runId, \[int traceDepth\])                                                                                                                                                                                                                                                                                                                                                                                                         |                                                      |
| public str tempPath()                                                                                                                                                                                                                                                                                                                                                                                                                                           |                                                      |
| public str toString()                                                                                                                                                                                                                                                                                                                                                                                                                                           | 現在のオブジェクトを表す文字列を返します。 |
| ::public static AnyType profilerAlreadyOn()                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                      |
| public void flush()                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                      |
| public void new()                                                                                                                                                                                                                                                                                                                                                                                                                                               | profiler クラスの新しいインスタンスを初期化します。    |
| public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, \[int sqlInsertBytes\], \[int sqlInsertRows\], \[int sqlUpdateBytes\], \[int sqlUpdateRows\], \[int sqlDeleteBytes\], \[int sqlDeleteRows\]) |                                                      |

### <a name="method-collected"></a>メソッド collected

    public int collected()

#### <a name="return-value"></a>戻り値

### <a name="method-flushinterval"></a>メソッド flushInterval

    public int flushInterval([int interval])

#### <a name="parameters"></a>パラメーター

interval  

#### <a name="return-value"></a>戻り値

### <a name="method-profileoff"></a>メソッド profileOff

    public AnyType profileOff()

#### <a name="return-value"></a>戻り値

### <a name="method-profileon"></a>メソッド profileOn

    public AnyType profileOn(str runId, [int traceDepth])

#### <a name="parameters"></a>パラメーター

runId  

<!-- -->

traceDepth  

#### <a name="return-value"></a>戻り値

### <a name="method-temppath"></a>メソッド tempPath

    public str tempPath()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。

### <a name="method-profileralreadyon"></a>メソッド profilerAlreadyOn

    public static AnyType profilerAlreadyOn()

#### <a name="return-value"></a>戻り値

### <a name="method-flush"></a>メソッド flush

    public void flush()

### <a name="method-new"></a>メソッド new

profiler クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-flushdata"></a>メソッド flushData

    public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, [int sqlInsertBytes], [int sqlInsertRows], [int sqlUpdateBytes], [int sqlUpdateRows], [int sqlDeleteBytes], [int sqlDeleteRows])

#### <a name="parameters"></a>パラメーター

lineNumber  

<!-- -->

path  

<!-- -->

microSecs  

<!-- -->

sequenceNumber  

<!-- -->

parentSequenceNumber  

<!-- -->

selectCalls  

<!-- -->

selectBytes  

<!-- -->

selectRows  

<!-- -->

sqlWaitTime  

<!-- -->

aosWaitTime  

<!-- -->

sqlInserts  

<!-- -->

sqlUpdates  

<!-- -->

sqlDeletes  

<!-- -->

aosInCalls  

<!-- -->

aosOutCalls  

<!-- -->

aosInBytes  

<!-- -->

aosOutBytes  

<!-- -->

sqlInsertBytes  

<!-- -->

sqlInsertRows  

<!-- -->

sqlUpdateBytes  

<!-- -->

sqlUpdateRows  

<!-- -->

sqlDeleteBytes  

<!-- -->

sqlDeleteRows  

## <a name="class-progresswindow"></a>クラス ProgressWindow
    class ProgressWindow extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                      | 説明                                             |
|-------------------------------------------------------------|---------------------------------------------------------|
| public int addProgressControl(\[int progressControlCount\]) |                                                         |
| public void ProgressBarVisible(int index, int visible)      |                                                         |
| public void ProgressValue(int index, int progressValue)     |                                                         |
| public void ControlMinMax(int index, int min, int max)      |                                                         |
| public void ProgressTextVisible(int index, int visible)     |                                                         |
| public void Animation(str animation)                        |                                                         |
| public void ControlText(int index, str text)                |                                                         |
| public void FormCaption(str text)                           |                                                         |
| public void ControlTime(str text)                           |                                                         |
| public void finalize()                                      |                                                         |
| public void new()                                           | ProgressWindow クラスの新しいインスタンスを初期化します。 |

### <a name="method-addprogresscontrol"></a>メソッド addProgressControl

    public int addProgressControl([int progressControlCount])

#### <a name="parameters"></a>パラメーター

progressControlCount  

#### <a name="return-value"></a>戻り値

### <a name="method-progressbarvisible"></a>メソッド ProgressBarVisible

    public void ProgressBarVisible(int index, int visible)

#### <a name="parameters"></a>パラメーター

指数  

<!-- -->

表示  

### <a name="method-progressvalue"></a>メソッド ProgressValue

    public void ProgressValue(int index, int progressValue)

#### <a name="parameters"></a>パラメーター

指数  

<!-- -->

progressValue  

### <a name="method-controlminmax"></a>メソッド ControlMinMax

    public void ControlMinMax(int index, int min, int max)

#### <a name="parameters"></a>パラメーター

指数  

<!-- -->

最小  

<!-- -->

最大  

### <a name="method-progresstextvisible"></a>メソッド ProgressTextVisible

    public void ProgressTextVisible(int index, int visible)

#### <a name="parameters"></a>パラメーター

指数  

<!-- -->

表示  

### <a name="method-animation"></a>メソッド アニメーション

    public void Animation(str animation)

#### <a name="parameters"></a>パラメーター

animation  

### <a name="method-controltext"></a>メソッド ControlText

    public void ControlText(int index, str text)

#### <a name="parameters"></a>パラメーター

指数  

<!-- -->

テキスト  

### <a name="method-formcaption"></a>メソッド FormCaption

    public void FormCaption(str text)

#### <a name="parameters"></a>パラメーター

テキスト  

### <a name="method-controltime"></a>メソッド ControlTime

    public void ControlTime(str text)

#### <a name="parameters"></a>パラメーター

テキスト  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

ProgressWindow クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-projectgroupnode"></a>クラス ProjectGroupNode
    class ProjectGroupNode extends TreeNode

ProjectGroupNode クラスは、プロジェクト内のグループ ノードを表します。

### <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\]) | 特定の要素の projectGroup を検索します。 特定のグループまたはプロジェクト全体を検索するために使用できます。                             |
| public str groupMask(\[str value\])                                                          |                                                                                                                                               |
| public str name(\[str value\])                                                               | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public boolean preventEditProperties(\[boolean value\])                                      |                                                                                                                                               |
| public GroupNodeType projectGroupType(\[GroupNodeType value\])                               |                                                                                                                                               |
| public void addUtilNode(UtilElementType type, str name)                                      | projectGroup にノードを追加します。                                                                                                              |
| public void addNode(TreeNode node)                                                           | ProjectGroup に既存のノードを追加します。                                                                                                    |

### <a name="method-findgroupmember"></a>メソッド findGroupMember

特定の要素の projectGroup を検索します。 特定のグループまたはプロジェクト全体を検索するために使用できます。

    public TreeNode findGroupMember(str name, UtilElementType type, [boolean searchSubgroups])

#### <a name="parameters"></a>パラメーター

名前  
検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。

<!-- -->

タイプ  
検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。

<!-- -->

searchSubgroups  
検索が再帰的 (サブプロジェクトを検索するか) どうかを決定するブール フラグ; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが見つからない場合は、条件を満たす最初のオブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic にはなし) を返します。

#### <a name="remarks"></a>備考

このメソッドは ProjectNode にもあります。

### <a name="method-groupmask"></a>メソッド groupMask

    public str groupMask([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-preventeditproperties"></a>メソッド preventEditProperties

    public boolean preventEditProperties([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-projectgrouptype"></a>メソッド projectGroupType

    public GroupNodeType projectGroupType([GroupNodeType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-addutilnode"></a>メソッド addUtilNode

projectGroup にノードを追加します。

    public void addUtilNode(UtilElementType type, str name)

#### <a name="parameters"></a>パラメーター

タイプ  
ノードの名前。

<!-- -->

名前  
ノードの名前。

#### <a name="remarks"></a>備考

このメソッドは、ProjectNode クラスにもあります。

### <a name="method-addnode"></a>メソッド addNode

ProjectGroup に既存のノードを追加します。

    public void addNode(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  
追加するノード。

## <a name="class-projectlistnode"></a>クラス ProjectListNode
    class ProjectListNode extends TreeNode

ProjectListNode クラスは、プロジェクトの概要ウィンドウ内のプロジェクトのプライベートと共有のリストに対応します。 X++ コードから新しいプロジェクトを追加するのにには、ProjectListNode.addProject メソッドを使用します。

### <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                               | 説明                     |
|----------------------------------------------------------------------|---------------------------------|
| public ProjectNode addProject(str projectName, \[str projectClass\]) | リストに新しいプロジェクトを追加します。 |

### <a name="method-addproject"></a>メソッド addProject

リストに新しいプロジェクトを追加します。

    public ProjectNode addProject(str projectName, [str projectClass])

#### <a name="parameters"></a>パラメーター

projectName  
projecttype の名前 (オプション)。 これは、プロジェクトに関連付けられたクラスの名前でなければなりません (setProjectClass メソッドを参照)。 値が指定されていない場合は、標準のプロジェクトがプロジェクトになります。

<!-- -->

projectClass  
projecttype の名前 (オプション)。 これは、プロジェクトに関連付けられたクラスの名前でなければなりません (setProjectClass メソッドを参照)。 値が指定されていない場合は、標準のプロジェクトがプロジェクトになります。

#### <a name="return-value"></a>戻り値

新たに追加された projectNode。

## <a name="class-projectnode"></a>クラス ProjectNode
    class ProjectNode extends TreeNode

ProjectNode クラスは、AOT プロジェクトの動作を制御します。

### <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 このクラスから拡張して、新しいユーザー定義の AOT プロジェクトを作成します。 このクラスのメソッドを上書きすることによって、プロジェクトの動作を制御します。 Web プロジェクトとヘルプ プロジェクトの両方を作成するには、ProjectNode クラスを拡張するクラスを作成します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str addContextMenuItems()                                                             | プロジェクト ノードのショートカット メニューに品目のリストを追加します。                                                                                |
| public str changedBy(\[str value\])                                                          | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])                                                      | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                 |
| public str changedTime(\[str value\])                                                        | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                 |
| public str createdBy(\[str value\])                                                          | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])                                                     | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                      |
| public str creationTime(\[str value\])                                                       |                                                                                                                                               |
| public str export(str buffer)                                                                |                                                                                                                                               |
| public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\]) | 特定の要素のプロジェクトまたはグループを検索します。                                                                                         |
| public str getProjectClassName()                                                             | プロジェクトの classid に対応するクラスの名前を返します。                                                                    |
| public ProjectNode getRunNode()                                                              | プロジェクト ウィンドウを開いて、プロジェクトの概要ウィンドウで見つかった特定の projectNode のためにそのウィンドウのルート projectNode を返します。  |
| public str import(str buffer)                                                                |                                                                                                                                               |
| public boolean isRunNode()                                                                   |                                                                                                                                               |
| public ProjectNode loadForInspection()                                                       | プロジェクトの概要ウィンドウにある projectNode の読み込まれたバージョンを返します。                                                               |
| public str name(\[str value\])                                                               | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                                                           |                                                                                                                                               |
| public boolean removeFromProject(TreeNode node)                                              |                                                                                                                                               |
| public str tooltipText(TreeNode node)                                                        |                                                                                                                                               |
| ::public static str projectType()                                                            |                                                                                                                                               |
| public void lockUpdate()                                                                     | 一連のアクションを実行中に、視覚的な更新を禁止します。                                                                         |
| public void addSpecialOverlayIcon(str path, int resId, \[int xOffset\], \[int yOffset\])     |                                                                                                                                               |
| public void created(str name)                                                                | プロジェクトの新しいインスタンスが作成された際、プロジェクトでカスタム アクションを実行を有効にします。                                     |
| public void setSpecialIcon(int type, str name, int resId)                                    | プロジェクト内の特定のノードに別のアイコンを割り当てます。                                                                                   |
| public void loadProject(str buffer)                                                          | プロジェクトが読み込まれた際、プロジェクト定義にカスタムデータの格納と取得を有効にします。                                                |
| public void saveProject(str buffer)                                                          | アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データの保存を有効にします。                                                      |
| public void unlockUpdate()                                                                   | lockUpdate で一連のアクションを開始した後にビジュアル更新プログラムを有効にします。                                                                    |
| public void handleContextMenuItem(int id)                                                    | ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するのを処理します。                  |
| public void addNode(TreeNode node)                                                           | プロジェクトに既存のノードを追加します。                                                                                                         |
| public void addUtilNode(UtilElementType type, str name)                                      | プロジェクトにノードを追加します。                                                                                                                   |
| public void clear()                                                                          | プロジェクトの内容を削除します。                                                                                                            |
| public void setProjectClass(int classid)                                                     | クラスをプロジェクトに割り当てますが、クラスに定義されているタイプをプロジェクトに与えます。                                                      |
| public void removeSpecialOverlayIcons(str path)                                              |                                                                                                                                               |
| public void new()                                                                            | ProjectNode クラスの新しいインスタンスを初期化します。                                                                                          |

### <a name="method-addcontextmenuitems"></a>メソッド addContextMenuItems

プロジェクト ノードのショートカット メニューに品目のリストを追加します。

    public str addContextMenuItems()

#### <a name="return-value"></a>戻り値

追加するメニュー項目のコンマ区切りリスト。

#### <a name="remarks"></a>備考

プロジェクト ノードのショートカット メニューに品目のリストを追加するには、このメソッドを上書きします。 追加されたメニュー項目の 1 つがユーザーによって選択されると、handleContextMenuItem メソッドが呼び出されます。 適切なアクションを実行するには、このメソッドを上書きします。

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-export"></a>メソッド export

    public str export(str buffer)

#### <a name="parameters"></a>パラメーター

バッファ  

#### <a name="return-value"></a>戻り値

### <a name="method-findgroupmember"></a>メソッド findGroupMember

特定の要素のプロジェクトまたはグループを検索します。

    public TreeNode findGroupMember(str name, UtilElementType type, [boolean searchSubgroups])

#### <a name="parameters"></a>パラメーター

名前  
検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。

<!-- -->

タイプ  
検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。

<!-- -->

searchSubgroups  
検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。

#### <a name="return-value"></a>戻り値

オブジェクトが見つからない場合は、条件を満たす最初のオブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

このメソッドは ProjectGroupNode にもあります。

### <a name="method-getprojectclassname"></a>メソッド getProjectClassName

プロジェクトの classid に対応するクラスの名前を返します。

    public str getProjectClassName()

#### <a name="return-value"></a>戻り値

プロジェクトの classid に対応するクラスの名前。

#### <a name="remarks"></a>備考

setClassId メソッドは、クラス ID をプロジェクトに割り当てます。

### <a name="method-getrunnode"></a>メソッド getRunNode

プロジェクト ウィンドウを開いて、プロジェクトの概要ウィンドウで見つかった特定の projectNode のためにそのウィンドウのルート projectNode を返します。

    public ProjectNode getRunNode()

#### <a name="return-value"></a>戻り値

実行中の projectNode。

#### <a name="remarks"></a>備考

[プロジェクト] ウィンドウを開くことがなく実行中の projectNode を取得するには、ProjectNode.loadForInspection メソッドを使用します。

### <a name="method-import"></a>メソッド import

    public str import(str buffer)

#### <a name="parameters"></a>パラメーター

バッファ  

#### <a name="return-value"></a>戻り値

### <a name="method-isrunnode"></a>メソッド isRunNode

    public boolean isRunNode()

#### <a name="return-value"></a>戻り値

### <a name="method-loadforinspection"></a>メソッド loadForInspection

プロジェクトの概要ウィンドウにある projectNode の読み込まれたバージョンを返します。

    public ProjectNode loadForInspection()

#### <a name="return-value"></a>戻り値

読み込まれた projectNode。

#### <a name="remarks"></a>備考

[プロジェクト] ウィンドウを開いたときに projectNode を読み込むには、getRunNode メソッドを使用します。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-removefromproject"></a>メソッド removeFromProject

    public boolean removeFromProject(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltiptext"></a>メソッド tooltipText

    public str tooltipText(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-projecttype"></a>メソッド projectType

    public static str projectType()

#### <a name="return-value"></a>戻り値

### <a name="method-lockupdate"></a>メソッド lockUpdate

一連のアクションを実行中に、視覚的な更新を禁止します。

    public void lockUpdate()

#### <a name="remarks"></a>備考

一連のアクションの後にビジュアル アップデートを実行するには、unlockUpdate を呼び出します。

### <a name="method-addspecialoverlayicon"></a>メソッド addSpecialOverlayIcon

    public void addSpecialOverlayIcon(str path, int resId, [int xOffset], [int yOffset])

#### <a name="parameters"></a>パラメーター

path  

<!-- -->

resId  

<!-- -->

xOffset  

<!-- -->

yOffset  

### <a name="method-created"></a>メソッド created

プロジェクトの新しいインスタンスが作成された際、プロジェクトでカスタム アクションを実行を有効にします。

    public void created(str name)

#### <a name="parameters"></a>パラメーター

名前  
プロジェクト インスタンスの名前。

#### <a name="remarks"></a>備考

このメソッドは、プロジェクトの新しいインスタンスが作成されるときに呼び出されます。 プロジェクトでカスタム アクションを実行するには、このメソッドを上書きします。

### <a name="method-setspecialicon"></a>メソッド setSpecialIcon

プロジェクト内の特定のノードに別のアイコンを割り当てます。

    public void setSpecialIcon(int type, str name, int resId)

#### <a name="parameters"></a>パラメーター

タイプ  
指定されたノードに使用する必要があるアイコンの ID。

<!-- -->

名前  
指定されたノードに使用する必要があるアイコンの ID。

<!-- -->

resId  
指定されたノードに使用する必要があるアイコンの ID。

### <a name="method-loadproject"></a>メソッド loadProject

プロジェクトが読み込まれた際、プロジェクト定義にカスタムデータの格納と取得を有効にします。

    public void loadProject(str buffer)

#### <a name="parameters"></a>パラメーター

バッファ  
saveProject によってプロジェクトに保存されたカスタム データを含む文字列。

#### <a name="remarks"></a>備考

このメソッドは、プロジェクトが読み込まれたときに呼び出されます。 saveProject および loadProject を上書きすることにより、ユーザーはカスタム データをプロジェクト定義に保存して取得できます。 読み込みを続行するには、プロジェクトの super() を呼び出す必要があります。

### <a name="method-saveproject"></a>メソッド saveProject

アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データの保存を有効にします。

    public void saveProject(str buffer)

#### <a name="parameters"></a>パラメーター

バッファ  
データをパッキングするために使用する必要がある文字列バッファ。 その後、バッファ はsuper() に渡されなければなりません。

#### <a name="remarks"></a>備考

このメソッドを上書きすることにより、アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データを保存できます。 データは「&lt;APPDATA&gt; ... &lt;/APPDATA&gt;」の形式で XML 文字列として形成することをお勧めします。このデータは loadProject メソッドをオーバーライドして取得できます。

### <a name="method-unlockupdate"></a>メソッド unlockUpdate

lockUpdate で一連のアクションを開始した後にビジュアル更新プログラムを有効にします。

    public void unlockUpdate()

### <a name="method-handlecontextmenuitem"></a>メソッド handleContextMenuItem

ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するのを処理します。

    public void handleContextMenuItem(int id)

#### <a name="parameters"></a>パラメーター

id  
メニュー項目の ID。 これは、addContextMenuItems メソッドによって設定されたリスト内の 0 から始まる数値です。 accContextMenuItems が文字列である "item1,item2" を返し、ユーザーがショートカット メニューの品目である "item2" を選択した場合、この方法では値 1 を使用します。

#### <a name="remarks"></a>備考

このメソッドは、ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するときに呼び出されます。

### <a name="method-addnode"></a>メソッド addNode

プロジェクトに既存のノードを追加します。

    public void addNode(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  
追加するノード。

### <a name="method-addutilnode"></a>メソッド addUtilNode

プロジェクトにノードを追加します。

    public void addUtilNode(UtilElementType type, str name)

#### <a name="parameters"></a>パラメーター

タイプ  
ノードの名前。

<!-- -->

名前  
ノードの名前。

#### <a name="remarks"></a>備考

この関数は ProjectGroupNode にもあります。

### <a name="method-clear"></a>メソッド clear

プロジェクトの内容を削除します。

    public void clear()

#### <a name="remarks"></a>備考

このメソッドは、アプリケーション オブジェクト ツリー (AOT) からプロジェクトの内容を削除しません。プロジェクト自体からのみです。 このメソッドはプロジェクトの内容を削除しますが、プロジェクト フォルダーは削除しません。 1 回のメソッド呼び出しでプロジェクトとその内容を削除するには、AOTdelete メソッドを使用します。 オブジェクトを AOT から削除するには、AOTdelete メソッドを使用します。

#### <a name="examples"></a>例

次の例では、Project1 プロジェクト内のプライベート フォルダー内のオブジェクトをすべて削除します。

    static void clearProjectObjects(Args _args) 
        { 
            ProjectNode privatePn; 
            ProjectNode pn; 
            // Navigate to the Private projects folder. 
            privatePn = infolog.projectRootNode().AOTfindChild("Private"); 
            // Get a reference to the project. 
            pn = privatePn.AOTfindChild("Project1"); 
            // Clear the project. 
            pn.clear(); 
        }

### <a name="method-setprojectclass"></a>メソッド setProjectClass

クラスをプロジェクトに割り当てますが、クラスに定義されているタイプをプロジェクトに与えます。

    public void setProjectClass(int classid)

#### <a name="parameters"></a>パラメーター

classid  
プロジェクトに割り当てるクラスの ID。

#### <a name="remarks"></a>備考

指定されたクラスは、projectNode クラスを拡張する必要があります。

### <a name="method-removespecialoverlayicons"></a>メソッド removeSpecialOverlayIcons

    public void removeSpecialOverlayIcons(str path)

#### <a name="parameters"></a>パラメーター

path  

### <a name="method-new"></a>メソッド new

ProjectNode クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-propertieswindow"></a>クラス PropertiesWindow
    class PropertiesWindow extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                   | 説明 |
|----------------------------------------------------------|-------------|
| public int Activate(PropWindowDisplayState displaystate) |             |
| public boolean DockFrame(PropWindowDockState dockstate)  |             |
| public str GetSelectedPropertyName()                     |             |
| public boolean IsVisible()                               |             |
| public boolean SelectPropertyByName(str propname)        |             |
| public boolean SelectTab(PropWindowSelectTab selecttab)  |             |

### <a name="method-activate"></a>メソッド Activate

    public int Activate(PropWindowDisplayState displaystate)

#### <a name="parameters"></a>パラメーター

displaystate  

#### <a name="return-value"></a>戻り値

### <a name="method-dockframe"></a>メソッド DockFrame

    public boolean DockFrame(PropWindowDockState dockstate)

#### <a name="parameters"></a>パラメーター

dockstate  

#### <a name="return-value"></a>戻り値

### <a name="method-getselectedpropertyname"></a>メソッド GetSelectedPropertyName

    public str GetSelectedPropertyName()

#### <a name="return-value"></a>戻り値

### <a name="method-isvisible"></a>メソッド IsVisible

    public boolean IsVisible()

#### <a name="return-value"></a>戻り値

### <a name="method-selectpropertybyname"></a>メソッド SelectPropertyByName

    public boolean SelectPropertyByName(str propname)

#### <a name="parameters"></a>パラメーター

propname  

#### <a name="return-value"></a>戻り値

### <a name="method-selecttab"></a>メソッド SelectTab

    public boolean SelectTab(PropWindowSelectTab selecttab)

#### <a name="parameters"></a>パラメーター

selecttab  

#### <a name="return-value"></a>戻り値



