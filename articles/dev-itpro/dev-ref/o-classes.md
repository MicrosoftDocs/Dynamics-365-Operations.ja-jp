---
title: O クラス
description: 文字 O で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 52201
ms.assetid: 63f93d3d-54a5-46c2-b356-fe5863b6f927
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 915cbcc14ec6709f45a28db0810b8edc6910b5e7
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833668"
---
# <a name="o-classes"></a>O クラス

[!include [banner](../includes/banner.md)]

文字 O で始まるシステム API クラス。

<a name="class-object"></a>クラス オブジェクト
------------

    class Object

Object クラスは、その他のすべてのクラスの派生元となる基本クラスです。

### <a name="remarks"></a>備考

オブジェクト クラスのメソッドは、任意のオブジェクトに対して呼び出すことができます。 Object クラスは、開発者がオブジェクトの実際のタイプを知らなくても、割り当ておよび等価チェックを実行できるようにするために使用されます。 メソッドは 3 つのグループにグループ化できます。

-   タイム アウト メソッド - 指定した時間が経過した後にメソッドをアクティブにするために使用できます。
-   プロセス フローを制御したり、別のオブジェクトがそのタスクを終了するを待機するために使用される、Wait、Notify、NotifyAll メソッドなどのメソッドを処理します。
-   クラス メソッド - オブジェクトに関する基本情報を返します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                      | 説明                                                                                                 |
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| public boolean equal(Object object)                                         | 指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。                                        |
| public int getTimeOutTimerHandle()                                          | オブジェクトのタイマー ハンドルを返します。                                                                    |
| public ClassId handle()                                                     | オブジェクトのクラスのハンドルを取得します。                                                            |
| public boolean SysObsoleteAttribute()                                       |                                                                                                             |
| public int SysObsoleteAttribute(str Method, int WaitTime, \[boolean idle\]) |                                                                                                             |
| public str toString()                                                       | 現在のオブジェクトを表す文字列を返します。                                                        |
| public int usageCount()                                                     | オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。 |
| public str xml(\[int indent\])                                              | 現在のオブジェクトを表す XML 文字列を返します。                                                   |
| public boolean Equals(System.Object obj)                                    |                                                                                                             |
| public int GetHashCode()                                                    |                                                                                                             |
| public void finalize()                                                      |                                                                                                             |
| public void wait()                                                          | プロセスを一時停止します。                                                                                           |
| public void cancelTimeOut(int timerHandle)                                  | setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。                                                    |
| public void new()                                                           | Object クラスの新しいインスタンスを初期化します。                                                             |
| public void notify()                                                        | このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。                              |
| public void notifyAll()                                                     | このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。                            |

### <a name="method-equal"></a>メソッド equal

指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。

    public boolean equal(Object object)

#### <a name="parameters"></a>パラメーター

オブジェクト  
現在のオブジェクトと比較するオブジェクト。

#### <a name="return-value"></a>戻り値

指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。 ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドをオーバーライドできます。

#### <a name="examples"></a>例

次の例では、現在のインスタンスと別のオブジェクトを比較します。

    static void Object_Equal(Args _args) 
    { 
        Object objA = new Object(); 
        Object objB = new Object(); 
        print objA.equal(objA);  // true. 
        print objA.equal(objB);  // false. 
        objA = objB; 
        print objA.equal(objB);  // true. 
     }

### <a name="method-gettimeouttimerhandle"></a>メソッド getTimeOutTimerHandle

オブジェクトのタイマー ハンドルを返します。

    public int getTimeOutTimerHandle()

#### <a name="return-value"></a>戻り値

オブジェクトのタイマー ハンドル。

#### <a name="remarks"></a>備考

オブジェクトのタイマー ハンドルは、setTimeOut メソッドを呼び出すことによって設定されます。

#### <a name="examples"></a>例

次の例では、タイムアウトを設定してから、タイムアウトをキャンセルします。

    public void myJob() 
    { 
        int timerHandle = 0; 
        this.setTimeOut(identifierstr(workerFunction), 0); 
        //Perform some operations. 
        timerHandle = this.getTimeOutTimerHandle(); 
        this.cancelTimeOut( timerHandle ); 
    }

### <a name="method-handle"></a>メソッド handle

オブジェクトのクラスのハンドルを取得します。

    public ClassId handle()

#### <a name="return-value"></a>戻り値

現在のオブジェクトのクラスのハンドル、つまり classId プロパティです。

#### <a name="remarks"></a>備考

クラスの処理が後のリリースで変更されない、またはユーザー定義クラスのエクスポートまたはインポートの後に変更されないという保証はありません。 このメソッドによって返される値を、クラスを参照する永続的な定数として使用しないことを強くお勧めします。

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public int SysObsoleteAttribute(str Method, int WaitTime, [boolean idle])

#### <a name="parameters"></a>パラメーター

方法  

<!-- -->

WaitTime  

<!-- -->

idle  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

#### <a name="examples"></a>例

次の例では、o のクラス名を出力します。

    static void Object_ToString_Job(Args _args) 
    { 
        Object o = new Object(); 
        print o.toString();  // Prints out: "Class Object" 
        pause; 
    }

### <a name="method-usagecount"></a>メソッド usageCount

オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。

    public int usageCount()

#### <a name="return-value"></a>戻り値

オブジェクトが持つ参照の現在の数。

#### <a name="remarks"></a>備考

オブジェクトが作成されると、その参照カウンターが 1 になります。 新しい参照が作成されると、その値が増加します。 スコープ外の参照は、値が減少します。

#### <a name="examples"></a>例

次の例では、objA の参照の数を出力ウィンドウに出力します。

    static void Object_UsageCount(Args _args) 
    { 
        Object objA = new Object(); 
        Object objB; 
        print objA.usageCount();    // Prints 1. 
        objB = objA;                // objB is a reference to objA. 
        print objA.usageCount();    // prints 2 
        pause; 
    }

### <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

    public str xml([int indent])

#### <a name="parameters"></a>パラメーター

インデント  
返された XML 文字列のインデントの量 (省略可能)。

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す XML 文字列です。

#### <a name="remarks"></a>備考

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

### <a name="method-equals"></a>メソッド Equals

    public boolean Equals(System.Object obj)

#### <a name="parameters"></a>パラメーター

obj  

#### <a name="return-value"></a>戻り値

### <a name="method-gethashcode"></a>メソッド GetHashCode

    public int GetHashCode()

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-wait"></a>メソッド wait

プロセスを一時停止します。

    public void wait()

#### <a name="remarks"></a>備考

このメソッドの最も一般的な使い方は、ユーザーに何らかの入力を求めるオブジェクトを開始し、そのオブジェクト (フォームなど) の wait メソッドを呼び出すことです。 次のコード行は、オブジェクトが notify メソッド または notifyAll メソッドを呼び出すまで実行されません。 フォームから wait メソッドが呼び出されるとき、ユーザーは通知メソッドを手動で呼び出す必要はありません。それは、ユーザーがフォームを閉じるか、または [適用] ボタンを押すと、フォームが Object.notifyAll メソッドを呼び出すためです。 このメソッドはスレッドの同期のためのものではありません。 代わりに waitUntilSignaled メソッドを使用します。

#### <a name="examples"></a>例

次の例では、GetUserInput ダイアログを開き、ブロックし、ユーザーがフォームを閉じるまで待機します。

    { 
        Args a = new Args("GetUserInput"); 
        formRun fr = new formRun(a); 
        fr.init(); 
        fr.run(); 
        fr.wait(); 
        // Execution will resume at this point, only after 
        // the user has closed the form. 
    }

### <a name="method-canceltimeout"></a>メソッド cancelTimeOut

setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。

    public void cancelTimeOut(int timerHandle)

#### <a name="parameters"></a>パラメーター

timerHandle  
削除する予定イベントのハンドル。 ハンドルは、Object.setTimeOut メソッドによって返される値です。

#### <a name="remarks"></a>備考

まだ処理されていないスケジュールされたタイムアウト呼び出しは、オブジェクト自体が削除されると自動的に削除されます。

#### <a name="examples"></a>例

次の例では、Object.setTimeOut メソッドを呼び出した後、タイムアウトをキャンセルします。

    void Object_cancelTimeOut(Args _args) 
    { 
        int th; // timerHandle. 
        // timedMethod is a worker method. 
        th = this.setTimeOut( "timedMethod", 2000 ); 
        //.... 
        // Remove timeOut later. 
        CancelTimeOut(th); 
    }

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-notify"></a>メソッド notify

このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。

    public void notify()

#### <a name="examples"></a>例

次の例では、オブジェクトをロックしてから解放します。

    public void doWork() 
    { 
        // Perform some actions. 
        this.setTimeOut(identifierstr(workerFunction), 0); 
        this.wait(); // Lock and wait for notify to be called. 
    } 
    public void workerFunction() 
    { 
        // Perform some actions. 
        // Work is done; unlock the doWork method. 
        this.notify(); 
    }

### <a name="method-notifyall"></a>メソッド notifyAll

このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。

    public void notifyAll()

#### <a name="remarks"></a>備考

このメソッドの現在の実装では、notify メソッドと notifyAll メソッドの呼び出しに違いはありません。 フォームは、ユーザーがフォームを閉じるまたは「適用」ボタンを押す際に、notifyAll メソッドを自動で呼び出します。

#### <a name="examples"></a>例

次の例では、notifyAll メソッドの使用方法を示しています。

    public void doWork() 
    { 
          //Do some work. 
          this.setTimeOut(identifierstr(workerFunction), 0); 
          this.wait(); // block and wait for notify. 
    } 
    public void workerFunction() 
    { 
    // Do some work. 
    //... 
    // Work is done. Notify an unblock. 
    this.notify(); 
    } 

## <a name="class-objectident"></a>クラス ObjectIdent
    class ObjectIdent extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                         | 説明                                     |
|--------------------------------|-------------------------------------------------|
| public Object object()         |                                                 |
| public void new(Object object) | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-object"></a>メソッド object

    public Object object()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(Object object)

#### <a name="parameters"></a>パラメーター

オブジェクト  

## <a name="class-objectrun"></a>クラス ObjectRun
    class ObjectRun extends Object

FormRun クラスおよび ReportRun クラスの基本クラスとして使用されます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                      | 説明                                                                                                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public xArgs args()         | オブジェクトが作成された引数を返します。                                                                                                             |
| public boolean isDetached() | このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。                                                                                      |
| public void attach()        | メソッドの呼び出しが取り消されます。 これは、ObjectRun.detach メソッドの呼び出しの逆です。 呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。 |
| public void detach()        | フォーカスをウィンドウ間で切り替えられるように許可します。                                                                                                                            |

### <a name="method-args"></a>メソッド args

オブジェクトが作成された引数を返します。

    public xArgs args()

#### <a name="return-value"></a>戻り値

オブジェクトの引数を含む Args クラス オブジェクトです。

### <a name="method-isdetached"></a>メソッド isDetached

このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。

    public boolean isDetached()

#### <a name="return-value"></a>戻り値

デタッチが呼び出された場合は true。それ以外の場合は、false。

### <a name="method-attach"></a>メソッド attach

メソッドの呼び出しが取り消されます。 これは、ObjectRun.detach メソッドの呼び出しの逆です。 呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。

    public void attach()

### <a name="method-detach"></a>メソッド detach

フォーカスをウィンドウ間で切り替えられるように許可します。

    public void detach()

#### <a name="remarks"></a>備考

たとえば、新しいフォームの実行方法を呼び出すことにより、新しいフォームが既存のフォームから作成されます。 実行メソッドを呼び出すと、フォーカスが新しいフォームに変更されます。 解除メソッドを呼び出すと、ユーザーは 2 番目のフォームを閉じることなく最初のフォームに戻ることができます。 ObjectRun.attach Method メソッドの呼び出しは、解除メソッドの影響を取り消します。

## <a name="class-ociconnection"></a>クラス OciConnection
    class OciConnection extends Connection

OciConnection クラスは、Oci (Oracle 呼び出しインターフェイス) を使用するデータベース接続を確立します。

### <a name="remarks"></a>備考

OciConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。 LoginProperty インスタンスに対して指定されている情報を基に、接続を確立できない場合、例外および理由は、情報ログに転記されます。 このクラスは、Oracle クライアント ソフトウェアがインストールされている場合にのみ使用できます。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                               | 説明                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------|
| public void new(LoginProperty Login) | ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。 |

### <a name="method-new"></a>メソッド new

ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。

    public void new(LoginProperty Login)

#### <a name="parameters"></a>パラメーター

ログイン  
ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。

## <a name="class-odbcconnection"></a>クラス OdbcConnection
    class OdbcConnection extends Connection

OdbcConnection クラスは、ODBC (Open Database Connectivity) を使用してデータベース接続を確立します。

### <a name="remarks"></a>備考

OdbcConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。 ODBC データ ソースへの接続を確立できない場合、例外がスローされ、その原因が Infolog に転記されます。 このクラスは、正しい ODBC ドライバーがインストールされ、コントロール パネルの ODBC マネージャーで構成されている場合にのみ機能します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                               | 説明                                                                                              |
|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| public void new(LoginProperty Login) | ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。 |

### <a name="method-new"></a>メソッド new

ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。

    public void new(LoginProperty Login)

#### <a name="parameters"></a>パラメーター

ログイン  
ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。

## <a name="class-olecommand"></a>クラス OleCommand
    class OleCommand extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                              | 説明                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm) |                                                 |
| public void finalize()                                                              |                                                 |
| public void new(ComInterface comObject)                                             | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-exec"></a>メソッド exec

    public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)

#### <a name="parameters"></a>パラメーター

cmdGroup  

<!-- -->

cmdId  

<!-- -->

cmdExecOption  

<!-- -->

parm  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(ComInterface comObject)

#### <a name="parameters"></a>パラメーター

comObject  

## <a name="class-ouputsection"></a>クラス OuputSection
    class OuputSection extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                           | 説明                                           |
|--------------------------------------------------|-------------------------------------------------------|
| public int arrangeMethod()                       |                                                       |
| public int backgroundColor()                     |                                                       |
| public LineThickness borderWidth()               |                                                       |
| public int bottomMargin()                        |                                                       |
| public HeadingsStrategy columnHeadingsStrategy() |                                                       |
| public str fontName()                            |                                                       |
| public int leftMargin()                          |                                                       |
| public LineType lineBottom()                     |                                                       |
| public LineType lineLeft()                       |                                                       |
| public LineType lineRight()                      |                                                       |
| public LineType lineTop()                        |                                                       |
| public int nextVerticalPos()                     |                                                       |
| public int rightMargin()                         |                                                       |
| public ReportBlockType sectionType()             |                                                       |
| public int topMargin()                           |                                                       |
| public int type()                                |                                                       |
| public int verticalPos()                         |                                                       |
| public void new()                                | OuputSection クラスの新しいインスタンスを初期化します。 |

### <a name="method-arrangemethod"></a>メソッド arrangeMethod

    public int arrangeMethod()

#### <a name="return-value"></a>戻り値

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

    public int backgroundColor()

#### <a name="return-value"></a>戻り値

### <a name="method-borderwidth"></a>メソッド borderWidth

    public LineThickness borderWidth()

#### <a name="return-value"></a>戻り値

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin()

#### <a name="return-value"></a>戻り値

### <a name="method-columnheadingsstrategy"></a>メソッド columnHeadingsStrategy

    public HeadingsStrategy columnHeadingsStrategy()

#### <a name="return-value"></a>戻り値

### <a name="method-fontname"></a>メソッド fontName

    public str fontName()

#### <a name="return-value"></a>戻り値

### <a name="method-leftmargin"></a>メソッド leftMargin

    public int leftMargin()

#### <a name="return-value"></a>戻り値

### <a name="method-linebottom"></a>メソッド lineBottom

    public LineType lineBottom()

#### <a name="return-value"></a>戻り値

### <a name="method-lineleft"></a>メソッド lineLeft

    public LineType lineLeft()

#### <a name="return-value"></a>戻り値

### <a name="method-lineright"></a>メソッド lineRight

    public LineType lineRight()

#### <a name="return-value"></a>戻り値

### <a name="method-linetop"></a>メソッド lineTop

    public LineType lineTop()

#### <a name="return-value"></a>戻り値

### <a name="method-nextverticalpos"></a>メソッド nextVerticalPos

    public int nextVerticalPos()

#### <a name="return-value"></a>戻り値

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin()

#### <a name="return-value"></a>戻り値

### <a name="method-sectiontype"></a>メソッド sectionType

    public ReportBlockType sectionType()

#### <a name="return-value"></a>戻り値

### <a name="method-topmargin"></a>メソッド topMargin

    public int topMargin()

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type()

#### <a name="return-value"></a>戻り値

### <a name="method-verticalpos"></a>メソッド verticalPos

    public int verticalPos()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OuputSection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputautolabelfield"></a>クラス OutputAutoLabelField
    class OutputAutoLabelField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                  | 説明                                                   |
|-------------------------|---------------------------------------------------------------|
| public boolean leadIn() |                                                               |
| public str toString()   | 現在のオブジェクトを表す文字列を返します。          |
| public str value()      |                                                               |
| public void new()       | OutputAutoLabelField クラスの新しいインスタンスを初期化します。 |

### <a name="method-leadin"></a>メソッド leadIn

    public boolean leadIn()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public str value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputAutoLabelField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputbitmapfield"></a>クラス OutputBitmapField
    class OutputBitmapField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                     | 説明                                                |
|----------------------------|------------------------------------------------------------|
| public str imageFileName() |                                                            |
| public boolean resize()    |                                                            |
| public int resourceId()    |                                                            |
| public str toString()      | 現在のオブジェクトを表す文字列を返します。       |
| public container value()   |                                                            |
| public void new()          | OutputBitmapField クラスの新しいインスタンスを初期化します。 |

### <a name="method-imagefilename"></a>メソッド imageFileName

    public str imageFileName()

#### <a name="return-value"></a>戻り値

### <a name="method-resize"></a>メソッド resize

    public boolean resize()

#### <a name="return-value"></a>戻り値

### <a name="method-resourceid"></a>メソッド resourceId

    public int resourceId()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public container value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputBitmapField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputbodysection"></a>クラス OutputBodySection
    class OutputBodySection extends OuputSection

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法             | 説明                                                |
|--------------------|------------------------------------------------------------|
| public int recId() |                                                            |
| public int table() |                                                            |
| public void new()  | OutputBodySection クラスの新しいインスタンスを初期化します。 |

### <a name="method-recid"></a>メソッド recId

    public int recId()

#### <a name="return-value"></a>戻り値

### <a name="method-table"></a>メソッド table

    public int table()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputBodySection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputcolumnheadingssection"></a>クラス OutputColumnHeadingsSection
    class OutputColumnHeadingsSection extends OuputSection

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法             | 説明                                                          |
|--------------------|----------------------------------------------------------------------|
| public str table() |                                                                      |
| public void new()  | OutputColumnHeadingsSection クラスの新しいインスタンスを初期化します。 |

### <a name="method-table"></a>メソッド table

    public str table()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputColumnHeadingsSection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputdatefield"></a>クラス OutputDateField
    class OutputDateField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                | 説明                                              |
|-----------------------|----------------------------------------------------------|
| public str toString() | 現在のオブジェクトを表す文字列を返します。     |
| public Date value()   |                                                          |
| public void new()     | OutputDateField クラスの新しいインスタンスを初期化します。 |

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public Date value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputDateField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputdatetimefield"></a>クラス OutputDateTimeField
    class OutputDateTimeField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                  | 説明                                                  |
|-------------------------|--------------------------------------------------------------|
| public str toString()   | 現在のオブジェクトを表す文字列を返します。         |
| public DateTime value() |                                                              |
| public void new()       | OutputDateTimeField クラスの新しいインスタンスを初期化します。 |

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public DateTime value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputDateTimeField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputenumfield"></a>クラス OutputEnumField
    class OutputEnumField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                 | 説明                                              |
|------------------------|----------------------------------------------------------|
| public str getString() |                                                          |
| public void new()      | OutputEnumField クラスの新しいインスタンスを初期化します。 |

### <a name="method-getstring"></a>メソッド getString

    public str getString()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputEnumField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputepilogsection"></a>クラス OutputEpilogSection
    class OutputEpilogSection extends OuputSection

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法            | 説明                                                  |
|-------------------|--------------------------------------------------------------|
| public void new() | OutputEpilogSection クラスの新しいインスタンスを初期化します。 |

### <a name="method-new"></a>メソッド new

OutputEpilogSection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputfield"></a>クラス OutputField
    class OutputField extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                         | 説明                                          |
|--------------------------------|------------------------------------------------------|
| public Alignment alignment()   |                                                      |
| public int backgroundColor()   |                                                      |
| public int borderWidth()       |                                                      |
| public str CSSClass()          |                                                      |
| public int dateFormat()        |                                                      |
| public int decimals()          |                                                      |
| public int extendedDataType()  |                                                      |
| public FieldId fieldHandle()   |                                                      |
| public str fieldName()         |                                                      |
| public int fontHeight()        |                                                      |
| public str fontName()          |                                                      |
| public int foregroundColor()   |                                                      |
| public str formatValue()       |                                                      |
| public int height()            |                                                      |
| public int heightMode()        |                                                      |
| public boolean hideZeros()     |                                                      |
| public boolean isOneline()     |                                                      |
| public boolean isOverlapping() |                                                      |
| public boolean italic()        |                                                      |
| public LateEvalMode lateEval() |                                                      |
| public LineType lineBottom()   |                                                      |
| public LineType lineLeft()     |                                                      |
| public LineType lineRight()    |                                                      |
| public LineType lineTop()      |                                                      |
| public str menuFunctionHelp()  |                                                      |
| public str menuFunctionName()  |                                                      |
| public int menuFunctionType()  |                                                      |
| public str menuFunctionWeb()   |                                                      |
| public str name()              |                                                      |
| public int recId()             |                                                      |
| public boolean showPrompt()    |                                                      |
| public boolean strikeThrough() |                                                      |
| public TableId tableHandle()   |                                                      |
| public str tableName()         |                                                      |
| public boolean turnSign()      |                                                      |
| public int type()              |                                                      |
| public boolean underline()     |                                                      |
| public str webMenuItemName()   |                                                      |
| public int webMenuItemType()   |                                                      |
| public str webTarget()         |                                                      |
| public int weight()            |                                                      |
| public int width()             |                                                      |
| public int widthMode()         |                                                      |
| public int xPos()              |                                                      |
| public int yPos()              |                                                      |
| public void new()              | OutputField クラスの新しいインスタンスを初期化します。 |

### <a name="method-alignment"></a>メソッド alignment

    public Alignment alignment()

#### <a name="return-value"></a>戻り値

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

    public int backgroundColor()

#### <a name="return-value"></a>戻り値

### <a name="method-borderwidth"></a>メソッド borderWidth

    public int borderWidth()

#### <a name="return-value"></a>戻り値

### <a name="method-cssclass"></a>メソッド CSSClass

    public str CSSClass()

#### <a name="return-value"></a>戻り値

### <a name="method-dateformat"></a>メソッド dateFormat

    public int dateFormat()

#### <a name="return-value"></a>戻り値

### <a name="method-decimals"></a>メソッド decimals

    public int decimals()

#### <a name="return-value"></a>戻り値

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public int extendedDataType()

#### <a name="return-value"></a>戻り値

### <a name="method-fieldhandle"></a>メソッド fieldHandle

    public FieldId fieldHandle()

#### <a name="return-value"></a>戻り値

### <a name="method-fieldname"></a>メソッド fieldName

    public str fieldName()

#### <a name="return-value"></a>戻り値

### <a name="method-fontheight"></a>メソッド fontHeight

    public int fontHeight()

#### <a name="return-value"></a>戻り値

### <a name="method-fontname"></a>メソッド fontName

    public str fontName()

#### <a name="return-value"></a>戻り値

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

    public int foregroundColor()

#### <a name="return-value"></a>戻り値

### <a name="method-formatvalue"></a>メソッド formatValue

    public str formatValue()

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

    public int height()

#### <a name="return-value"></a>戻り値

### <a name="method-heightmode"></a>メソッド heightMode

    public int heightMode()

#### <a name="return-value"></a>戻り値

### <a name="method-hidezeros"></a>メソッド hideZeros

    public boolean hideZeros()

#### <a name="return-value"></a>戻り値

### <a name="method-isoneline"></a>メソッド isOneline

    public boolean isOneline()

#### <a name="return-value"></a>戻り値

### <a name="method-isoverlapping"></a>メソッド isOverlapping

    public boolean isOverlapping()

#### <a name="return-value"></a>戻り値

### <a name="method-italic"></a>メソッド italic

    public boolean italic()

#### <a name="return-value"></a>戻り値

### <a name="method-lateeval"></a>メソッド lateEval

    public LateEvalMode lateEval()

#### <a name="return-value"></a>戻り値

### <a name="method-linebottom"></a>メソッド lineBottom

    public LineType lineBottom()

#### <a name="return-value"></a>戻り値

### <a name="method-lineleft"></a>メソッド lineLeft

    public LineType lineLeft()

#### <a name="return-value"></a>戻り値

### <a name="method-lineright"></a>メソッド lineRight

    public LineType lineRight()

#### <a name="return-value"></a>戻り値

### <a name="method-linetop"></a>メソッド lineTop

    public LineType lineTop()

#### <a name="return-value"></a>戻り値

### <a name="method-menufunctionhelp"></a>メソッド menuFunctionHelp

    public str menuFunctionHelp()

#### <a name="return-value"></a>戻り値

### <a name="method-menufunctionname"></a>メソッド menuFunctionName

    public str menuFunctionName()

#### <a name="return-value"></a>戻り値

### <a name="method-menufunctiontype"></a>メソッド menuFunctionType

    public int menuFunctionType()

#### <a name="return-value"></a>戻り値

### <a name="method-menufunctionweb"></a>メソッド menuFunctionWeb

    public str menuFunctionWeb()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-recid"></a>メソッド recId

    public int recId()

#### <a name="return-value"></a>戻り値

### <a name="method-showprompt"></a>メソッド showPrompt

    public boolean showPrompt()

#### <a name="return-value"></a>戻り値

### <a name="method-strikethrough"></a>メソッド strikeThrough

    public boolean strikeThrough()

#### <a name="return-value"></a>戻り値

### <a name="method-tablehandle"></a>メソッド tableHandle

    public TableId tableHandle()

#### <a name="return-value"></a>戻り値

### <a name="method-tablename"></a>メソッド tableName

    public str tableName()

#### <a name="return-value"></a>戻り値

### <a name="method-turnsign"></a>メソッド turnSign

    public boolean turnSign()

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type()

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

    public boolean underline()

#### <a name="return-value"></a>戻り値

### <a name="method-webmenuitemname"></a>メソッド webMenuItemName

    public str webMenuItemName()

#### <a name="return-value"></a>戻り値

### <a name="method-webmenuitemtype"></a>メソッド webMenuItemType

    public int webMenuItemType()

#### <a name="return-value"></a>戻り値

### <a name="method-webtarget"></a>メソッド webTarget

    public str webTarget()

#### <a name="return-value"></a>戻り値

### <a name="method-weight"></a>メソッド weight

    public int weight()

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

    public int width()

#### <a name="return-value"></a>戻り値

### <a name="method-widthmode"></a>メソッド widthMode

    public int widthMode()

#### <a name="return-value"></a>戻り値

### <a name="method-xpos"></a>メソッド xPos

    public int xPos()

#### <a name="return-value"></a>戻り値

### <a name="method-ypos"></a>メソッド yPos

    public int yPos()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputfootersection"></a>クラス OutputFooterSection
    class OutputFooterSection extends OuputSection

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                | 説明                                                  |
|---------------------------------------|--------------------------------------------------------------|
| public int level()                    |                                                              |
| public int level2field(\[int level\]) |                                                              |
| public int niveau()                   |                                                              |
| public int table()                    |                                                              |
| public void new()                     | OutputFooterSection クラスの新しいインスタンスを初期化します。 |

### <a name="method-level"></a>メソッド level

    public int level()

#### <a name="return-value"></a>戻り値

### <a name="method-level2field"></a>メソッド level2field

    public int level2field([int level])

#### <a name="parameters"></a>パラメーター

level  

#### <a name="return-value"></a>戻り値

### <a name="method-niveau"></a>メソッド niveau

    public int niveau()

#### <a name="return-value"></a>戻り値

### <a name="method-table"></a>メソッド table

    public int table()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputFooterSection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputheadersection"></a>クラス OutputHeaderSection
    class OutputHeaderSection extends OuputSection

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法             | 説明                                                  |
|--------------------|--------------------------------------------------------------|
| public int table() |                                                              |
| public void new()  | OutputHeaderSection クラスの新しいインスタンスを初期化します。 |

### <a name="method-table"></a>メソッド table

    public int table()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputHeaderSection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputintegerfield"></a>クラス OutputIntegerField
    class OutputIntegerField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                        | 説明                                                 |
|-------------------------------|-------------------------------------------------------------|
| public int displaceNegative() |                                                             |
| public boolean negative()     |                                                             |
| public str toString()         | 現在のオブジェクトを表す文字列を返します。        |
| public int value()            |                                                             |
| public void new()             | OutputIntegerField クラスの新しいインスタンスを初期化します。 |

### <a name="method-displacenegative"></a>メソッド displaceNegative

    public int displaceNegative()

#### <a name="return-value"></a>戻り値

### <a name="method-negative"></a>メソッド negative

    public boolean negative()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public int value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputIntegerField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputlabelfield"></a>クラス OutputLabelField
    class OutputLabelField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                | 説明                                               |
|-----------------------|-----------------------------------------------------------|
| public str toString() | 現在のオブジェクトを表す文字列を返します。      |
| public str value()    |                                                           |
| public void new()     | OutputLabelField クラスの新しいインスタンスを初期化します。 |

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public str value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputLabelField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputpage"></a>クラス OutputPage
    class OutputPage extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                        | 説明                                         |
|-------------------------------|-----------------------------------------------------|
| public int bottomMargin()     |                                                     |
| public str fontName()         |                                                     |
| public int height()           |                                                     |
| public boolean layoutRTL()    |                                                     |
| public int leftMargin()       |                                                     |
| public str pageNumber()       |                                                     |
| public int rightMargin()      |                                                     |
| public int sectionNo()        |                                                     |
| public int topMargin()        |                                                     |
| public int unusedBottom()     |                                                     |
| public int unusedLeft()       |                                                     |
| public int unusedRight()      |                                                     |
| public int unusedTop()        |                                                     |
| public int virtualPageWidth() |                                                     |
| public int width()            |                                                     |
| public void new()             | OutputPage クラスの新しいインスタンスを初期化します。 |

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin()

#### <a name="return-value"></a>戻り値

### <a name="method-fontname"></a>メソッド fontName

    public str fontName()

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

    public int height()

#### <a name="return-value"></a>戻り値

### <a name="method-layoutrtl"></a>メソッド layoutRTL

    public boolean layoutRTL()

#### <a name="return-value"></a>戻り値

### <a name="method-leftmargin"></a>メソッド leftMargin

    public int leftMargin()

#### <a name="return-value"></a>戻り値

### <a name="method-pagenumber"></a>メソッド pageNumber

    public str pageNumber()

#### <a name="return-value"></a>戻り値

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin()

#### <a name="return-value"></a>戻り値

### <a name="method-sectionno"></a>メソッド sectionNo

    public int sectionNo()

#### <a name="return-value"></a>戻り値

### <a name="method-topmargin"></a>メソッド topMargin

    public int topMargin()

#### <a name="return-value"></a>戻り値

### <a name="method-unusedbottom"></a>メソッド unusedBottom

    public int unusedBottom()

#### <a name="return-value"></a>戻り値

### <a name="method-unusedleft"></a>メソッド unusedLeft

    public int unusedLeft()

#### <a name="return-value"></a>戻り値

### <a name="method-unusedright"></a>メソッド unusedRight

    public int unusedRight()

#### <a name="return-value"></a>戻り値

### <a name="method-unusedtop"></a>メソッド unusedTop

    public int unusedTop()

#### <a name="return-value"></a>戻り値

### <a name="method-virtualpagewidth"></a>メソッド virtualPageWidth

    public int virtualPageWidth()

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

    public int width()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputPage クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputpagefootersection"></a>クラス OutputPageFooterSection
    class OutputPageFooterSection extends OuputSection

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法            | 説明                                                      |
|-------------------|------------------------------------------------------------------|
| public void new() | OutputPageFooterSection クラスの新しいインスタンスを初期化します。 |

### <a name="method-new"></a>メソッド new

OutputPageFooterSection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputpageheadersection"></a>クラス OutputPageHeaderSection
    class OutputPageHeaderSection extends OuputSection

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法            | 説明                                                      |
|-------------------|------------------------------------------------------------------|
| public void new() | OutputPageHeaderSection クラスの新しいインスタンスを初期化します。 |

### <a name="method-new"></a>メソッド new

OutputPageHeaderSection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputprogrammablesection"></a>クラス OutputProgrammableSection
    class OutputProgrammableSection extends OuputSection

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法              | 説明                                                        |
|---------------------|--------------------------------------------------------------------|
| public str number() |                                                                    |
| public void new()   | OutputProgrammableSection クラスの新しいインスタンスを初期化します。 |

### <a name="method-number"></a>メソッド number

    public str number()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputProgrammableSection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputprologsection"></a>クラス OutputPrologSection
    class OutputPrologSection extends OuputSection

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法            | 説明                                                  |
|-------------------|--------------------------------------------------------------|
| public void new() | OutputPrologSection クラスの新しいインスタンスを初期化します。 |

### <a name="method-new"></a>メソッド new

OutputPrologSection クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputrealfield"></a>クラス OutputRealField
    class OutputRealField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                        | 説明                                              |
|-------------------------------|----------------------------------------------------------|
| public int displaceNegative() |                                                          |
| public boolean negative()     |                                                          |
| public str toString()         | 現在のオブジェクトを表す文字列を返します。     |
| public Real value()           |                                                          |
| public void new()             | OutputRealField クラスの新しいインスタンスを初期化します。 |

### <a name="method-displacenegative"></a>メソッド displaceNegative

    public int displaceNegative()

#### <a name="return-value"></a>戻り値

### <a name="method-negative"></a>メソッド negative

    public boolean negative()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public Real value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputRealField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputshapefield"></a>クラス OutputShapeField
    class OutputShapeField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                       | 説明                                               |
|------------------------------|-----------------------------------------------------------|
| public int borderWidth()     |                                                           |
| public LineType lineType()   |                                                           |
| public ShapeType shapeType() |                                                           |
| public str toString()        | 現在のオブジェクトを表す文字列を返します。      |
| public int value()           |                                                           |
| public void new()            | OutputShapeField クラスの新しいインスタンスを初期化します。 |

### <a name="method-borderwidth"></a>メソッド borderWidth

    public int borderWidth()

#### <a name="return-value"></a>戻り値

### <a name="method-linetype"></a>メソッド lineType

    public LineType lineType()

#### <a name="return-value"></a>戻り値

### <a name="method-shapetype"></a>メソッド shapeType

    public ShapeType shapeType()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public int value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputShapeField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputstatictextfield"></a>クラス OutputStaticTextField
    class OutputStaticTextField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                | 説明                                                    |
|-----------------------|----------------------------------------------------------------|
| public str toString() | 現在のオブジェクトを表す文字列を返します。           |
| public str value()    |                                                                |
| public void new()     | OutputStaticTextField クラスの新しいインスタンスを初期化します。 |

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public str value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputStaticTextField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputstringfield"></a>クラス OutputStringField
    class OutputStringField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                | 説明                                                |
|-----------------------|------------------------------------------------------------|
| public str toString() | 現在のオブジェクトを表す文字列を返します。       |
| public str value()    |                                                            |
| public void new()     | OutputStringField クラスの新しいインスタンスを初期化します。 |

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public str value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputStringField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputsumfield"></a>クラス OutputSumField
    class OutputSumField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                | 説明                                             |
|-----------------------|---------------------------------------------------------|
| public str toString() | 現在のオブジェクトを表す文字列を返します。    |
| public Real value()   |                                                         |
| public void new()     | OutputSumField クラスの新しいインスタンスを初期化します。 |

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public Real value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputSumField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-outputtimefield"></a>クラス OutputTimeField
    class OutputTimeField extends OutputField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                | 説明                                              |
|-----------------------|----------------------------------------------------------|
| public str toString() | 現在のオブジェクトを表す文字列を返します。     |
| public int value()    |                                                          |
| public void new()     | OutputTimeField クラスの新しいインスタンスを初期化します。 |

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public int value()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

OutputTimeField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-overwritesystemfieldspermission"></a>クラス OverwriteSystemfieldsPermission
    class OverwriteSystemfieldsPermission extends CodeAccessPermission

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | アクセス許可クラス オブジェクトのコピーを作成し、返します。                                                                  |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。 |
| public void new()                                      | OverwriteSystemfieldsPermission クラスの新しいインスタンスを初期化します。                                                  |

### <a name="method-copy"></a>メソッド copy

アクセス許可クラス オブジェクトのコピーを作成し、返します。

    public CodeAccessPermission copy()

#### <a name="return-value"></a>戻り値

現在の派生クラスオブジェクトのコピーです。

#### <a name="remarks"></a>備考

API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。 詳細については、「サーバー層で実行する API の保護」を参照してください。

### <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a>パラメーター

target  
CodeAccessPermission クラス オブジェクト。

#### <a name="return-value"></a>戻り値

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。 詳細については、「サーバー層で実行する API の保護」を参照してください。

### <a name="method-new"></a>メソッド new

OverwriteSystemfieldsPermission クラスの新しいインスタンスを初期化します。

    public void new()



