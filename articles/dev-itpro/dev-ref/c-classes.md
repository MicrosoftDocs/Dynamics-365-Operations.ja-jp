---
title: "C クラス"
description: "文字 C で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 11/06/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 50962
ms.assetid: 53eb660c-9a11-4f59-9870-a24502588ebf
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 1cd1de091da9e1c95da7471cd8e181cffc676899
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="c-classes"></a>C クラス

[!include [banner](../includes/banner.md)]

文字 C で始まるシステム API クラス。

<a name="class-classnode"></a>クラス ClassNode
---------------

    class ClassNode extends TreeNode

ClassNode クラスは、Finance and Operations のアプリケーション オブジェクト ツリー (AOT) 内のクラスを表す TreeNode クラスの特殊な形式です。

### <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                            | 説明                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public TreeNode AOToverrideMethod(str methodName) |                                                                                                                                               |
| public str changedBy(\[str value\])               | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])           | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                 |
| public str changedTime(\[str value\])             | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                 |
| public str createdBy(\[str value\])               | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\])          | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                      |
| public str creationTime(\[str value\])            |                                                                                                                                               |
| public str extends(\[str value\])                 |                                                                                                                                               |
| public int iD(\[int value\])                      |                                                                                                                                               |
| public boolean isDetached()                       |                                                                                                                                               |
| public int legacyId(\[int value\])                |                                                                                                                                               |
| public str name(\[str value\])                    | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                |                                                                                                                                               |
| public int runOn(\[int value\])                   |                                                                                                                                               |
| public void AOTedit(\[int Line\], \[int Column\]) | クラスを開き、エディターで変更することもできるようにします。                                                                                     |

### <a name="method-aotoverridemethod"></a>メソッド AOToverrideMethod

    public TreeNode AOToverrideMethod(str methodName)

#### <a name="parameters"></a>パラメーター

methodName  

#### <a name="return-value"></a>戻り値

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

### <a name="method-extends"></a>メソッド extends

    public str extends([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド iD

    public int iD([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-isdetached"></a>メソッド isDetached

    public boolean isDetached()

#### <a name="return-value"></a>戻り値

### <a name="method-legacyid"></a>メソッド legacyId

    public int legacyId([int value])

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

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-runon"></a>メソッド runOn

    public int runOn([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aotedit"></a>メソッド AOTedit

クラスを開き、エディターで変更することもできるようにします。

    public void AOTedit([int Line], [int Column])

#### <a name="parameters"></a>パラメーター

明細行  
無視される値、オプション。

<!-- -->

円柱  
無視される値、オプション。

#### <a name="remarks"></a>備考

すべてのメソッドはエディターに読み込まれます。 引数は、下位互換性のためにのみ署名に含まれているため、無視されます。

#### <a name="examples"></a>例

    static void example() 
    { 
        ClassNode classNode; 

        classNode = infolog.findNode('\Classes\SysClassWizard'); 
        classNode.AOTedit(); 
    }

## <a name="class-clientprintjobsettings"></a>クラス ClientPrintJobSettings
    class ClientPrintJobSettings extends PrintJobSettings

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                  | 説明                                     |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public container getFontDimension(container container)                                                                  |                                                 |
| public container getInfoStrings()                                                                                       |                                                 |
| public int getNextLineOffset(container container)                                                                       |                                                 |
| public container getPageInfo()                                                                                          |                                                 |
| public container getPrinterNames()                                                                                      |                                                 |
| public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)                     |                                                 |
| public container getTextWidthExt(container container)                                                                   |                                                 |
| public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight) |                                                 |
| public container getWordWrapInfoExt(container container)                                                                |                                                 |
| public container printerSettingsExt(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])            |                                                 |
| public container setOrientationGetPageInfo(PrinterOrientation orientation)                                              |                                                 |
| public void new(\[container Settings\], \[boolean infoOnly\])                                                           | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-getfontdimension"></a>メソッド getFontDimension

    public container getFontDimension(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  

#### <a name="return-value"></a>戻り値

### <a name="method-getinfostrings"></a>メソッド getInfoStrings

    public container getInfoStrings()

#### <a name="return-value"></a>戻り値

### <a name="method-getnextlineoffset"></a>メソッド getNextLineOffset

    public int getNextLineOffset(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  

#### <a name="return-value"></a>戻り値

### <a name="method-getpageinfo"></a>メソッド getPageInfo

    public container getPageInfo()

#### <a name="return-value"></a>戻り値

### <a name="method-getprinternames"></a>メソッド getPrinterNames

    public container getPrinterNames()

#### <a name="return-value"></a>戻り値

### <a name="method-gettextwidth"></a>メソッド getTextWidth

    public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

fontName  

<!-- -->

charSet  

<!-- -->

fontHeight  

<!-- -->

style  

<!-- -->

重量  

#### <a name="return-value"></a>戻り値

### <a name="method-gettextwidthext"></a>メソッド getTextWidthExt

    public container getTextWidthExt(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  

#### <a name="return-value"></a>戻り値

### <a name="method-getwordwrapinfo"></a>メソッド getWordWrapInfo

    public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight)

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

width  

<!-- -->

fontName  

<!-- -->

charSet  

<!-- -->

fontHeight  

<!-- -->

style  

<!-- -->

重量  

#### <a name="return-value"></a>戻り値

### <a name="method-getwordwrapinfoext"></a>メソッド getWordWrapInfoExt

    public container getWordWrapInfoExt(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  

#### <a name="return-value"></a>戻り値

### <a name="method-printersettingsext"></a>メソッド printerSettingsExt

    public container printerSettingsExt(str formName, [xArgs args], [ReportRun reportRun], [int showWhat])

#### <a name="parameters"></a>パラメーター

formName  

<!-- -->

args  

<!-- -->

reportRun  

<!-- -->

showWhat  

#### <a name="return-value"></a>戻り値

### <a name="method-setorientationgetpageinfo"></a>メソッド setOrientationGetPageInfo

    public container setOrientationGetPageInfo(PrinterOrientation orientation)

#### <a name="parameters"></a>パラメーター

orientation  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new([container Settings], [boolean infoOnly])

#### <a name="parameters"></a>パラメーター

設定  

<!-- -->

infoOnly  

## <a name="class-clrinterop"></a>クラス CLRInterop
    class CLRInterop extends Object

ClrInterop クラスは、タイプ マーシャ リングおよび例外処理の機能を提供するユーティリティ クラスです。 すべてのメソッドは静的であるため、クラスのインスタンス化をする必要はありません。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                               | 説明                                                                                                                              |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ::public static AnyType getAnyTypeForObject(CLRObject clrObject)                     | 共通言語ランタイム (CLR) オブジェクトを X++ anytype データ型の値に変換します。                                                 |
| ::public static CLRObject getLastException()                                         | 最新の CLR 例外を取得します。                                                                                                 |
| ::public static CLRObject getObjectForAnyType(AnyType anyType)                       | X++ anytype データ型の値を CLRObject データ型の値に変換します。                                                     |
| ::public static CLRObject getType(str clrTypeName)                                   |                                                                                                                                          |
| ::public static boolean isNull(CLRObject clrObject)                                  | 指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic にはない) にセットされたかどうかを確認します。            |
| ::public static CLRObject Null(str clrTypeName)                                      | nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の値を持つ CLR データ型を返します。                            |
| ::public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)          | 1 つ以上の列挙定数の名前または数値の文字列で表したものを、等価の CLRObject インスタンスに変換します。 |
| ::public static CLRObject staticInvoke(str className, str methodName, VarArg params) | CLR データ型の静的メソッドを呼び出します。                                                                                                |
| ::public static void loadAssembly(str clrAssemblyName)                               |                                                                                                                                          |
| public void new()                                                                    | CLRInterop クラスの新しいインスタンスを初期化します。                                                                                      |

### <a name="method-getanytypeforobject"></a>メソッド getAnyTypeForObject

共通言語ランタイム (CLR) オブジェクトを X++ anytype データ型の値に変換します。

    public static AnyType getAnyTypeForObject(CLRObject clrObject)

#### <a name="parameters"></a>パラメーター

clrObject  
X++ データ型に変換する CLR オブジェクト。

#### <a name="return-value"></a>戻り値

\_オブジェクトの引数値を持つ X++ anytype データ型です。

#### <a name="remarks"></a>備考

攻撃者が getAnyTypeForObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。 引数が、X++ のデータ型に変換することができない場合、Exception::ClrError タイプの例外がスローされます。

#### <a name="examples"></a>例

次の例では、CLR 文字列の値を X++ str データ型に設定します。

    { 
        CLRObject clrObj; 
        InteropPermission perm; 
        System.String   clrStr = "Calculate total"; 
        str             s; 

        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 

        s = ClrInterop::getAnyTypeForObject(clrStr); 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-getlastexception"></a>メソッド getLastException

最新の CLR 例外を取得します。

    public static CLRObject getLastException()

#### <a name="return-value"></a>戻り値

Exception::ClrError type 型の最新の例外。それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic ではなし)。

#### <a name="remarks"></a>備考

攻撃者が getLastException メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

次の例では、無効な形式の日付を渡します。 スローされた CLR 例外は、X++ 例外に変換された後、情報ログに出力されます。 入れ子になった例外は情報ログにも出力されます。

    static void Job2(Args _args) 
    { 
        CLRObject clrObj; 
        InteropPermission perm; 

        try 
        { 
            System.DateTime::Parse( "-1/-1/-1"); 
        } 
        catch( Exception::CLRError ) 
        { 
            perm = new InteropPermission(InteropKind::ClrInterop); 
            if (perm == null) 
            { 
                return; 
            } 
            perm.assert(); 

            e = ClrInterop::getLastException(); 

            CodeAccessPermission::revertAssert(); 

            while( e ) 
            { 
                info( e.get_Message() ); 
                e = e.get_InnerException(); 
            } 
        } 

    }

### <a name="method-getobjectforanytype"></a>メソッド getObjectForAnyType

X++ anytype データ型の値を CLRObject データ型の値に変換します。

    public static CLRObject getObjectForAnyType(AnyType anyType)

#### <a name="parameters"></a>パラメーター

anyType  
CLRObject データ型の値に変換する X++ 値。

#### <a name="return-value"></a>戻り値

値 \_anytype 引数を持つ CLR オブジェクト。

#### <a name="remarks"></a>備考

攻撃者が getObjectForAnyType メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。 引数が CLRObject 型に変換することができない場合、Exception::CLRError タイプの例外がスローされます。

#### <a name="examples"></a>例

次の例では、文字列値を CLR 文字列オブジェクトに変換します。

    static void Job3(Args _args) 
    { 
        CLRObject clrObj; 
        InteropPermission perm; 
        System.String s; 

        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 

        s = CLRInterop::getObjectForAnyType("Calculate total"); 

        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-gettype"></a>メソッド getType

    public static CLRObject getType(str clrTypeName)

#### <a name="parameters"></a>パラメーター

clrTypeName  

#### <a name="return-value"></a>戻り値

### <a name="method-isnull"></a>メソッド isNull

指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic にはない) にセットされたかどうかを確認します。

    public static boolean isNull(CLRObject clrObject)

#### <a name="parameters"></a>パラメーター

clrObject  
評価する CLRObject インスタンスです。

#### <a name="return-value"></a>戻り値

指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic にはない) にセットされた場合または初期化されていない場合は true。

#### <a name="remarks"></a>備考

CLN データ型が nullNothingnullptrunita null 参照 (Visual Basic にはない) であるかどうかを評価する条件ステートメントでは、X++ nullNothingnullptrunita null参照 (Visual Basic にはない) の代わりに isNull メソッドを使用する必要があります。

#### <a name="examples"></a>例

次の例では、CLR 文字列データ型を nullNothingnullptrunita null 参照 (Visual Basic にはない) に設定し、タイプ値を CLR オブジェクトに割り当てます。 isNull メソッドを呼び出し、情報ログに結果を出力します。

    static void Job5(Args _args) 
    { 
        System.String nullStr; 

        nullStr = CLRInterop::Null("System.String"); 

        print CLRInterop::isNull(nullStr); 
    }

### <a name="method-null"></a>メソッド Null

nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の値を持つ CLR データ型を返します。

    public static CLRObject Null(str clrTypeName)

#### <a name="parameters"></a>パラメーター

clrTypeName  
nullNothingnullptrunita null参照 (Visual Basic にはない) に設定する必要がある CLR データ型。

#### <a name="return-value"></a>戻り値

指定された CLR データ型の CLRObject インスタンス。

#### <a name="remarks"></a>備考

X++ で CLR データ型を NullNothingnullptrunita null 参照 (Visual Basic ではなし) に直接設定する場合は、カーネル参照を nullNothingnullptrunita null 参照 (Visual Basic ではなし) にのみ設定します。 これにより、CLR データ型として型を使用することができなくなります。 CLRInterop:null("yourType") に CLR データ型を割り当てると、静的メソッド呼び出しのパラメーターとして、実行時にタイプを解析できます。

#### <a name="examples"></a>例

次の例では、CLR 文字列型を nullNothingnullptrunita nul l参照 (Visual Basic にはない) に設定し、型値を CLR オブジェクトに割り当てます。

    static void Job5(Args _args) 
    { 
        System.String nullStr; 

        nullStr = CLRInterop::Null("System.String"); 

        print CLRInterop::isInitialized(nullStr); 
        print CLRInterop::isNull(nullStr); 
    }

### <a name="method-parseclrenum"></a>メソッド parseClrEnum

1 つ以上の列挙定数の名前または数値の文字列で表したものを、等価の CLRObject インスタンスに変換します。

    public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)

#### <a name="parameters"></a>パラメーター

clrEnumTypeName  
変換する名前または値を含む文字列。

<!-- -->

enumValues  
変換する名前または値を含む文字列。

#### <a name="return-value"></a>戻り値

指定した CLR 列挙値を含む CLRObject インスタンスです。

#### <a name="remarks"></a>備考

\_enumValues パラメーターには、値、名前付き定数、またはコンマ (,) で区切られた名前付き定数の一覧が含まれています。 1 つ以上の空白スペースは、\_enumValues の各値、名前、またはコンマの前か後に置くことができます。 \_enumValues が一覧の場合、戻り値は、ビット単位の OR 演算と組み合わされた指定された名前の値です。

#### <a name="examples"></a>例

次の例では、列挙子の値を月曜日の文字列値に変換し、Infolog の値を出力します。

    static void Job6(Args _args) 
    { 
        System.DayOfWeek    dayOfWeek; 
        System.Type         dayOfWeekType; 

        dayOfWeek = CLRInterop::parseClrEnum( "System.DayOfWeek", "Monday"); 

        dayOfWeekType = dayOfWeek.GetType(); 

        info( dayOfWeek.ToString() ); 
    }

### <a name="method-staticinvoke"></a>メソッド staticInvoke

CLR データ型の静的メソッドを呼び出します。

    public static CLRObject staticInvoke(str className, str methodName, VarArg params)

#### <a name="parameters"></a>パラメーター

className  
\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。

<!-- -->

methodName  
\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。

<!-- -->

params  
\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。

#### <a name="return-value"></a>戻り値

静的 CLR メソッドによって返される値を含む CLRObject。それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic ではなし)。

#### <a name="remarks"></a>備考

攻撃者が staticInvoke メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。 get\_Now メソッドを呼び出すときにエラーが発生した場合は、Exception::ClrError 例外がスローされます。

#### <a name="examples"></a>例

次の例では、System.DateTime CLR クラスの get\_Now メソッドを呼び出し、結果を Infolog に出力します。

    static void Job7(Args _args) 
    { 
        CLRObject clrObj; 
        InteropPermission perm; 
        System.DateTime dateTime; 

        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 

        dateTime = CLRInterop::staticInvoke( 
                       "System.DateTime", 
                       "get_Now" ); 
        info(dateTime.ToString()); 
        CodeAccessPermission::revertAssert(); 

        pause; 

        // This is the same code using CLR syntax. 
        // dateTime = System.DateTime::get_Now(); 
        // info(dateTime.ToString()); 
    }

### <a name="method-loadassembly"></a>メソッド loadAssembly

    public static void loadAssembly(str clrAssemblyName)

#### <a name="parameters"></a>パラメーター

clrAssemblyName  

### <a name="method-new"></a>メソッド new

CLRInterop クラスの新しいインスタンスを初期化します。

    public void new()

#### <a name="remarks"></a>備考

CLRInterop クラスのすべてのメンバーは静的です。 このクラスをインスタンス化する必要はありません。 攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。

## <a name="class-clrobject"></a>クラス CLRObject
    class CLRObject extends Object

CLRObject クラスは、共通言語ランタイム (CLR) オブジェクトのインスタンスへの参照を保持し、X++ からの呼び出しを対応するラップされたマネージド インスタンスにディスパッチします。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                            | 説明                                   |
|---------------------------------------------------|-----------------------------------------------|
| private CLRObject dispatch(VarArg )               | 予約済み: メソッドを明示的に呼び出さないでください。 |
| public void new(str className, \[VarArg params\]) | CLRObject クラスのインスタンスを作成します。   |

### <a name="method-dispatch"></a>メソッド dispatch

予約済み: メソッドを明示的に呼び出さないでください。

    private CLRObject dispatch(VarArg )

#### <a name="parameters"></a>パラメーター



#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

攻撃者が出荷メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。

### <a name="method-new"></a>メソッド new

CLRObject クラスのインスタンスを作成します。

    public void new(str className, [VarArg params])

#### <a name="parameters"></a>パラメーター

className  
インスタンスを作成する CLR クラスのコンストラクターの引数。

<!-- -->

params  
インスタンスを作成する CLR クラスのコンストラクターの引数。

#### <a name="remarks"></a>備考

CLRObject クラスのインスタンスは、CLR メソッドの呼び出しから返される値をラップするために使用されます。 攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーが新しいメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。 新しい ClrObject オブジェクトをインスタンス化できない場合、例外: 例外内部はスローします。 元の CLR 例外を取得するには、CLRInterop :: getLastException メソッドを呼び出します。

#### <a name="examples"></a>例

この例では、新しい System.Int32 CLR オブジェクトを作成します。

    void ClrObjectExample() 
    { 
        CLRObject clrObj; 
        InteropPermission perm; 
        anytype retVal; 

        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 

        perm.assert(); 

        clrObj = new CLRObject("System.Int32"); 

        CodeAccessPermission::revertAssert(); 
    }

## <a name="class-codeaccesspermission"></a>クラス CodeAccessPermission
    class CodeAccessPermission extends Object

CodeAccessPermission クラスは、コード アクセス許可の基になる構造を定義します。

### <a name="remarks"></a>備考

次のクラスは、CodeAccessPermission クラスを拡張します: ExecutePermission、FileIOPermission、InteropPermission、RunAsPermission、SkipAOSValidationPermission、SqlDataDictionaryPermission、SqlStatementExecutePermission、および SysDatabaseLogPermission。

### <a name="examples"></a>例

次のコード例は、CodeAccessPermission クラスから派生したクラスを示しています。

    final class SysTestCodeAccessPermission extends CodeAccessPermission 
    { 
        str data; 
    }

このコード例は、API を保護するプロセスのステップを示しています。

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                                                                                       |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | アクセス許可クラス オブジェクトのコピーを作成し、返します。                                                                                          |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。                         |
| public void new()                                      | CodeAccessPermission クラスの新しいインスタンスを初期化します。                                                                                     |
| public void assert()                                   | 呼び出しコードがアクセス許可によって保護されている API を呼び出すことができることを宣言します。                                                               |
| public void demand()                                   | コール スタックをチェックして、API を呼び出すために必要なアクセス許可が呼び出しコードに与えられているかどうかを判断します。                 |
| ::public static void revertAssert()                    | CodeAccessPermission.assert および CodeAccessPermission::assertMultiple メソッドへの以前の呼び出しを削除し、無効にします。 |
| ::public static void assertMultiple(Set permissionSet) | 呼び出しコードが指定されたコレクションでのアクセス許可によって保護されている API を呼び出すことができることを宣言します。                           |

### <a name="method-copy"></a>メソッド copy

アクセス許可クラス オブジェクトのコピーを作成し、返します。

    public CodeAccessPermission copy()

#### <a name="return-value"></a>戻り値

現在の派生クラスオブジェクトのコピーです。

#### <a name="remarks"></a>備考

API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。

#### <a name="examples"></a>例

次のコード例は、copy メソッドを上書きして、CodeAccessPermission クラスから派生したクラスのコピーを作成して返す方法を示しています。

    public CodeAccessPermission copy() 
    { 
        return new SysTestCodeAccessPermission(_data); 
    }

### <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a>パラメーター

target  
CodeAccessPermission クラス オブジェクト。

#### <a name="return-value"></a>戻り値

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。

#### <a name="examples"></a>例

次の例は、isSubsetOf メソッドを上書きして、現在のオブジェクトに格納されているアクセス権が \_target にあるかどうかを判断する方法を示しています。.

    public boolean isSubsetOf(CodeAccessPermission _target) 
    { 
        SysTestCodeAccessPermission sysTarget = _target; 
        return this.handle() == _target.handle(); 
    }

### <a name="method-new"></a>メソッド new

CodeAccessPermission クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-assert"></a>メソッド assert

呼び出しコードがアクセス許可によって保護されている API を呼び出すことができることを宣言します。

    public void assert()

#### <a name="remarks"></a>備考

API を起動する前に、保護された API の派生クラスで assert メソッドを呼び出す必要があります。 アクセス許可によって保護されている API の詳細については、「セキュリティで保護された API」を参照してください。 保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド

Finance and Operations は、同じ呼び出しコードで、Assert メソッドに対する複数の連続する呼び出しをサポートしません。 Assert メソッドへの各呼び出し間の CodeAccessPermission::revertAssert メソッドを呼び出すか、または CodeAccessPermission::assertMultiple メソッドを呼び出すかです。 assertmethod を複数にわたり連続して呼び出すと、コードを実行するときに Infolog によってエラーが表示されます。

#### <a name="examples"></a>例

次のコード例は、アクセス許可で保護されている AsciiIo クラスが呼び出される前に assert メソッドを呼び出す方法を示しています。 assert メソッドは、CodeAccessPermission クラスから派生した FileIOPermission クラスのメンバーです。

    server static void main(Args args) 
    { 
        FileIoPermission _perm; 
        AsciiIo a; 


        _perm = new FileIoPermission("c:\File.txt",'r'); 
        _perm.assert(); 

        // Invoke the protected API. 
        a = new AsciiIo("c:\File.txt",'r'); 
    }

### <a name="method-demand"></a>メソッド demand

コール スタックをチェックして、API を呼び出すために必要なアクセス許可が呼び出しコードに与えられているかどうかを判断します。

    public void demand()

#### <a name="examples"></a>例

次のコード例は、API 機能を実行する前に、API を呼び出すコードに data 変数で指定されたリソースへのアクセス許可が与えられているかどうかを判断するための、demand メソッドの呼び出しを示しています。

    public static void main(str data) 
    { 
        SysTestCodeAccessPermission p = new SysTestCodeAccessPermission(data); 
        p.demand(); 

        //Add functionality 
    }

このコード例は、API を保護するプロセスのステップを示しています。

### <a name="method-revertassert"></a>メソッド revertAssert

CodeAccessPermission.assert および CodeAccessPermission::assertMultiple メソッドへの以前の呼び出しを削除し、無効にします。

    public static void revertAssert()

#### <a name="remarks"></a>備考

同じ呼び出しコードで assert メソッドに複数の呼び出しをするときは、それぞれの呼び出しの間に revertAssert メソッドを呼び出す必要があります。 それ以外の場合、情報ログには、コードを実行するときにエラーが表示されます。 assert メソッドを1回だけ呼び出すとき、または CodeAccessPermission::assertMultiple メソッドを呼び出すときは、アサートの範囲を制限する保護された API の起動後にも、revertAssert メソッドを呼び出すことをお勧めします。

#### <a name="examples"></a>例

次のコード例は、ユーザーが CodeAccessPermission.assert メソッドを呼び出した後の CodeAccessPermission :: revertAssert メソッドと、アクセス許可で保護されている AsciiIo クラスの呼び出しを示しています

    server static void main(Args args) 
    { 
        FileIoPermission _perm; 
        AsciiIo a; 


        _perm = new FileIoPermission("c:\File.txt",'r'); 
        _perm.assert(); 

        //invoke protected API 
        a = new AsciiIo("c:\File.txt",'r'); 

        // Optionally call revertAssert() to limit scope of assert. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-assertmultiple"></a>メソッド assertMultiple

呼び出しコードが指定されたコレクションでのアクセス許可によって保護されている API を呼び出すことができることを宣言します。

    public static void assertMultiple(Set permissionSet)

#### <a name="parameters"></a>パラメーター

permissionSet  
アクセス許可のコレクションを含むセット クラス オブジェクト。

#### <a name="remarks"></a>備考

同じ呼び出しコードで CodeAccessPermission.assert および CodeAccessPermission::revertAssert メソッドに対する複数の連続する呼び出しをする代わりに、assertMultple メソッドを呼び出します。

#### <a name="examples"></a>例

次のコード例は、CodeAccessPermission :: assertMultple メソッドを呼び出します。 コードのサンプルは WinAPIServer::createFile メソッドを呼び出します。これは、CodeAccessPermission::assertMultple メソッドへの前回の呼び出しがなく失敗します。 このコード例は、作成する新しいクラスに追加できる静的メソッドです。 MyClass::RunOnServerPermissionTest のようなコード行を使用して、X++ ジョブから静的メソッドを呼び出すことができます。 コードの例では、WinAPIServer クラスに、セキュリティで保護されたメソッドがいくつかあります。 WinAPIServer クラスは、クライアント層ではなく、サーバー層で実行されます。 したがって、コード例のメソッドはサーバー層でも実行する必要があります。 それ以外の場合、クライアント層で実行されたすべてのアクセス許可アサートは、サーバー層で実行されるメソッドにより無視されます。 このため、サーバー キーワードはコード例のメソッド宣言に含まれています。 メソッドのサーバー キーワードは、クラスで指定された RunOn プロパティ値よりも優先されます。

    server
        static public void RunOnServerPermissionTest()
    {
        Set permissionSet;
        str fileName = @"C:\TestFile75a.txt";
        boolean boolFileDeleted;

        permissionSet =  new Set(Types::Class);
        permissionSet.add(new FileIoPermission(fileName,'rw'));

        CodeAccessPermission::assertMultiple(permissionSet);
        //--- Permissions are set, now perform file operations.

        WinAPIServer::createFile(fileName);
        boolFileDeleted = WinAPI::deleteFile(fileName);

        if (boolFileDeleted)
        {
            info("The file was deleted. Good.");
        }
        else
        {
            error("The file was not deleted. Error.");
        }
    }

## <a name="class-com"></a>クラス COM
    class COM

COM クラスは、コンポーネント オブジェクト モデル (COM) オブジェクトを作成するためにも使用されます。

### <a name="remarks"></a>備考

COM クラスは、分散コンポーネント オブジェクト モデル (DCOM) もサポートしています。 DCOM は、DCOM をサポートするオブジェクトをリモート コンピュータで実行できるようにします。 COM クラスを使用して COM オブジェクトがインスタンス化されると、そのメソッドおよびプロパティに、COMDispFunction クラスかまたは COM クラスの 拡張構文を使用してアクセスできます。 拡張構文を使用すると、Lookup リストに表示されていなくても 、メソッドとプロパティを COM オブジェクトで直接呼び出すことができます (例: com.comMethod("Hello World");)。 拡張構文は、任意の数の引数を取るメソッドとプロパティへの呼び出しをサポートしています。 一部の COM オブジェクトは、省略可能な引数の概念をサポートします。 オプションのバリアント引数のみ省略できます。 オプションの引数を省略すると、COM オブジェクトは、既定値を使用します。 COM オブジェクトの引数を省略し、強制的に既定値を使用するには、次の例に示すように COMArgument :: NoValue 列挙型を指定します。

    com.comMethod(COMArgument::NoValue, "Hello Another World");



COM オブジェクトから省略する引数が引数リストの最後に表示される場合は、コードから省略します。 COM クラスの引数型と戻り値型の拡張構文では、次の型がサポートされています。

-   array
-   COM
-   COMVariant
-   日付
-   列挙型
-   int
-   real
-   str

COM オブジェクトが日付を返し、拡張構文が使用されている場合は、COM メソッドの戻り値を COM Variant クラス変数に割り当てる必要があります。 そして、日付と時刻のプロパティを使用して、COMVariant クラスから実際の日時 (形式) を抽出することができます。 日付の戻り値に COMVariant クラスではなく日付変数が割り当てられている場合、日付の時間の部分は失われます。 拡張構文を使用するときは、オブジェクトに対して COM クラス メソッド (ルックアップ リストに表示されるメソッド) をまだ呼び出すことができます。 COM クラス メソッドは、実際の COM オブジェクトでのメソッドよりも優先順位が高くなります。 COM オブジェクトのメソッドが COM クラスのメソッドと同じ名前 (たとえば、attach) である場合、そのメソッドを COM オブジェクトで呼び出すことはできません。 Finance and Operations で、COM クラスで同じ名前を持つメソッドを呼び出すのではなく、COM オブジェクトのメソッドを呼び出せるようにするには、重複するメソッド名の先頭にアンダースコアを付けます (たとえば、com.\_detach();)。 COM クラスの拡張構文は、コンパイル時ではなく実行時に評価され、パフォーマンスがわずかに低下します。 パフォーマンスの高いコードが必要な場合は、COMDispFunction クラスを使用することを検討します。 このクラスは、COM クラスの拡張構文よりもパフォーマンスが向上しています。

### <a name="examples"></a>例

この例では、Scripting.FileSystemObject COM オブジェクトから GetFileName メソッドを呼び出します。

    void COMExample() 
    { 
        COM               com; 
        str               result; 
        InteropPermission perm; 
        ; 

        // Set code access permission to help protect the use of the 
        // COM object. 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        // Permission scope starts here. 
        perm.assert(); 

        com = new COM("Scripting.FileSystemObject"); 
        if (com != null) 
        { 
            result = com.GetFileName(@"c:\boot.ini"); 
        } 

        // Close code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a>メソッド

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

### <a name="method-dispatch"></a>メソッド dispatch

予約済み。 メソッドを明示的に呼び出さないでください。

    public AnyType dispatch(VarArg )

#### <a name="parameters"></a>パラメーター



#### <a name="return-value"></a>戻り値

### <a name="method-documentationname"></a>メソッド documentationName

COM クラスのインスタンスに関連付けられている COM オブジェクトの名前を表すテキストを返します。

    public str documentationName()

#### <a name="return-value"></a>戻り値

COM クラスのインスタンスに関連付けられている COM オブジェクトのテキスト名。COM オブジェクトのドキュメント名がない場合は空の文字列です。

#### <a name="remarks"></a>備考

クラスのテキスト名は、そのクラスを記述するためにクラスによって使用されます。 テキスト名は、クラスをインスタンス化するために使用されるクラス名とは異なります。

#### <a name="examples"></a>例

次の例は、COM オブジェクトのドキュメント名を取得する方法を示しています。

    str docName; 
    ; 
    // The obj that was previously instantiated. 
    docName = obj.documentationName(); 
    info(strfmt("documentationName: %1", docName));

### <a name="method-error"></a>メソッド error

COM クラスのインスタンスに関連付けられている COMError オブジェクトを返します。

    public COMError error()

#### <a name="return-value"></a>戻り値

COM クラスのインスタンスに関連付けられているエラーを表す COMError 値。

#### <a name="examples"></a>例

次の例は、COM クラスのインスタンスに関連付けられているエラー オブジェクトを取得する方法を示しています。

    COMError err; 

    // The obj variable was previously instantiated. 
    err = obj.error(); 

    // Output the error number. 
    info(strfmt("Error: %1", err.number()))

### <a name="method-interface"></a>メソッド interface

COM オブジェクトに関連付けられているインターフェイスを返します。

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

COM オブジェクトに関連付けられているインターフェイス。インターフェイスが COM オブジェクトに関連付けられていない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、COM オブジェクトに関連付けられているインターフェイスを取得する方法を示しています。

    // The obj variable was previously instantiated. 
    info(strfmt("Interface: %1", obj.interface()));

### <a name="method-lcid"></a>メソッド lcid

    public int lcid([int lcid])

#### <a name="parameters"></a>パラメーター

lcid  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

COM クラスのインスタンスを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

COM クラスのインスタンスの説明を含む文字列。

#### <a name="examples"></a>例

次の例は、toString メソッドの使用方法を示しています。

    print objCOM.toString();

### <a name="method-createfrominterface"></a>メソッド createFromInterface

指定された COM インターフェイスを使用して COM クラスのインスタンスを作成します。

    public static COM createFromInterface(ComInterface interface)

#### <a name="parameters"></a>パラメーター

インターフェイス  
COM クラスの新しいインスタンスを作成するために使用するインターフェイス。

#### <a name="return-value"></a>戻り値

インターフェイス パラメーターで指定されている COM インターフェイスの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし) 。

#### <a name="remarks"></a>備考

アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。

### <a name="method-createfromobject"></a>メソッド createFromObject

指定された COM オブジェクトを使用して COM クラスのインスタンスを作成します。

    public static COM createFromObject(COM object)

#### <a name="parameters"></a>パラメーター

オブジェクト  
COM クラスの新しいインスタンスを作成するために使用する COM クラスのインスタンス。

#### <a name="return-value"></a>戻り値

オブジェクト パラメーターで指定されている COM オブジェクトの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし) 。

#### <a name="remarks"></a>備考

アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。

### <a name="method-createfromvariant"></a>メソッド createFromVariant

COMVariant クラスの指定されたインスタンスを使用して、COM クラスのインスタンスを作成します。

    public static COM createFromVariant(COMVariant variant)

#### <a name="parameters"></a>パラメーター

バリアント  
COM クラスの新しいインスタンスを作成するために使用する COMVariant クラスのインスタンス。

#### <a name="return-value"></a>戻り値

バリアント パラメーターで指定されている COM オブジェクトの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし) 。

#### <a name="remarks"></a>備考

アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。

### <a name="method-getobject"></a>メソッド getObject

実行している COM オブジェクトのインスタンスを返します。

    public static COM getObject(str className)

#### <a name="parameters"></a>パラメーター

className  
COM クラスのインスタンスを作成するために使用される COM オブジェクトの ProgID 値またはクラス名。

#### <a name="return-value"></a>戻り値

className パラメーターで指定されているクラスの COM クラスのインスタンス。インスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし) 。

#### <a name="remarks"></a>備考

指定した COM オブジェクトの複数インスタンスが実行している場合は、getObject メソッドによってどのインスタンスが返されるかを保証できません。 一部の COM オブジェクトは、このメソッドの呼び出しを可能にする拡張機能をサポートしていません。

#### <a name="examples"></a>例

次の例は、実行中の COM オブジェクトのインスタンスを取得する方法を示しています。

    COM objExcel, objWorkBook, objWorkBooks; 
    InteropPermission perm; 

    // Set code access permission to help protect the use of COM.new. 
    perm = new InteropPermission(InteropKind::ComInterop); 
    perm.assert(); 

    objExcel = COM::getObject("Excel.Application"); 

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

    objExcel.visible(true); 
    objWorkBooks = objExcel.workbooks(); 
    if (objWorkBooks) 
    { 
        objWorkBook = objWorkBooks.open("d:\mydata\book1.xls"); 
    }

### <a name="method-getobjectex"></a>メソッド getObjectEx

ファイル名で指定されている COM オブジェクトのインスタンスを返します。

    public static COM getObjectEx(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  
COM クラスのインスタンスを作成するために使用される COM オブジェクトの機能を提供するファイルの名前。

#### <a name="return-value"></a>戻り値

filename パラメーターで指定されている COM クラスのインスタンス。インスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし) 。

#### <a name="remarks"></a>備考

アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。

### <a name="method-unsupported"></a>メソッド unsupported

予約済み。

    public static AnyType unsupported(int action, [AnyType param1], [AnyType param2], [AnyType param3])

#### <a name="parameters"></a>パラメーター

アクション  

<!-- -->

param1  

<!-- -->

param2  

<!-- -->

param3  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

COM クラスのインスタンスに関連付けられているリソースを解放します。

    public void finalize()

#### <a name="examples"></a>例

次の例では、finalize メソッドの使用方法を示しています。

    objCOM.finalize();

### <a name="method-new"></a>メソッド new

COM クラスに接続できる COM クラスのインスタンスを作成し、オプションで、指定されたコンピュータ上で COM オブジェクトをインスタンス化することができます。

    public void new([str className], [str computerName])

#### <a name="parameters"></a>パラメーター

className  
COM オブジェクトをインスタンス化するリモート コンピューターの名前 (オプション)。 このパラメータを省略すると、COM オブジェクトはローカル コンピューターでインスタンス化されます。 コンピューター名が指定されている場合は、ローカル コンピューターとリモート コンピューターの両方に DCOM システムのコンポーネントをインストールする必要があります。 特定の COM オブジェクトは DCOM をサポートする必要があり、ローカル コンピューターとリモート コンピューターの両方で正しく構成されている必要があります。 システム コンポーネントは、Microsoft Windows 98、Windows NT、およびそれ以降のバージョンの標準コンポーネントです。 Windows 95 では、DCOM システム コンポーネントをインストールする必要があります。

<!-- -->

computerName  
COM オブジェクトをインスタンス化するリモート コンピューターの名前 (オプション)。 このパラメータを省略すると、COM オブジェクトはローカル コンピューターでインスタンス化されます。 コンピューター名が指定されている場合は、ローカル コンピューターとリモート コンピューターの両方に DCOM システムのコンポーネントをインストールする必要があります。 特定の COM オブジェクトは DCOM をサポートする必要があり、ローカル コンピューターとリモート コンピューターの両方で正しく構成されている必要があります。 システム コンポーネントは、Microsoft Windows 98、Windows NT、およびそれ以降のバージョンの標準コンポーネントです。 Windows 95 では、DCOM システム コンポーネントをインストールする必要があります。

#### <a name="remarks"></a>備考

COM オブジェクトのクラス名は、そのプログラム識別子 (ProgID) またはそのクラス識別子 (CLSID) です。

-   ProgID の形式: program.component.version
-   CLSIDs は 128 ビット値で、次の形式を持ちます: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}

攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

この例では、Scripting.FileSystemObject COM オブジェクトから GetFileName メソッドを呼び出します。

    void COMExample() 
    { 
        COM               com; 
        str               result; 
        InteropPermission perm; 

        // Set the code access permission to help protect the use of the 
        // COM object. 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        // Permission scope starts here. 
        perm.assert(); 

        com = new COM("Scripting.FileSystemObject"); 
        if (com != null) 
        { 
            result = com.GetFileName(@"c:\boot.ini"); 
        } 

        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-attach"></a>メソッド attach

COM クラスのインスタンスを COM インターフェイスに関連付けます。

    public void attach(ComInterface interface)

#### <a name="parameters"></a>パラメーター

インターフェイス  
COM クラスのインスタンスに関連付けるインターフェイス。

#### <a name="remarks"></a>備考

このメソッドは、一部の COM オブジェクトは他の COM オブジェクトによってのみインスタンス化されるが、COM クラスによって直接インスタンス化することができないため、用意されています。

### <a name="method-detach"></a>メソッド detach

関連付けられているクラスから COM オブジェクトを解除します。

    public void detach()

#### <a name="remarks"></a>備考

たとえば、このメソッドは、接続または新しいメソッドの呼び出しから COM オブジェクトを切り離すために呼び出されます。

## <a name="class-comdispfunction"></a>クラス COMDispFunction
    class COMDispFunction extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                   | 説明                                                                                          |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| public int call(VarArg )                                                 |                                                                                                      |
| public AnyType callContainerOfParms(container parms)                     |                                                                                                      |
| public str toString()                                                    | 現在のオブジェクトを表す文字列を返します。                                                 |
| public void finalize()                                                   |                                                                                                      |
| public void new(COM comObject, str functionName, COMDispContext context) | オートメーション オブジェクトの機能にアクセスするために使用される COMDispFunction オブジェクトを作成します。 |

### <a name="method-call"></a>メソッド call

    public int call(VarArg )

#### <a name="parameters"></a>パラメーター



#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

攻撃者が呼び出しメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="method-callcontainerofparms"></a>メソッド callContainerOfParms

    public AnyType callContainerOfParms(container parms)

#### <a name="parameters"></a>パラメーター

parms  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

オートメーション オブジェクトの機能にアクセスするために使用される COMDispFunction オブジェクトを作成します。

    public void new(COM comObject, str functionName, COMDispContext context)

#### <a name="parameters"></a>パラメーター

comObject  
アクセスする機能のコンテキスト。 次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF

<!-- -->

functionName  
アクセスする機能のコンテキスト。 次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF

<!-- -->

context  
アクセスする機能のコンテキスト。 次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF

#### <a name="remarks"></a>備考

COM オブジェクトは、同じ名前を使用する最大 4 つの機能を指定できるので、アクセスする COM オブジェクトで機能の正しいコンテキストを指定することが重要です。 使用可能な名前の衝突のため、コンテキストはメソッドまたはプロパティを区別するために使用されます。 正しいコンテキストを指定するには、アクセスする COM オブジェクトのドキュメントを参照してください。

#### <a name="examples"></a>例



    { 
        InteropPermission perm; 
        COM com; 
        COMDispFunction funcShow; 
        COMDispFunction getValue; 
        COMDispFunction putValue; 
        ; 

        perm = new InteropPermission(InteropKind::ComInterop); 
        perm.assert(); 
        com = new COM("MyCOM.Object"); 
        funcShow = 
            new COMDispFunction(com, "show",  COMDispContext::METHOD); 
        getValue = 
            new COMDispFunction(com, "value", COMDispContext::PROPERTYGET); 
        putValue = 
            new COMDispFunction(com, "value", COMDispContext::PROPERTYPUT); 
    }

## <a name="class-comerror"></a>クラス COMError
    class COMError extends Object

COMError クラスは、COM メソッド呼び出し時に発生するすべての COM エラーをラップします。

### <a name="remarks"></a>備考

COM メソッド呼び出し中にエラーが発生すると、エラー コードとエラーの説明が COMError オブジェクトに格納されます。 COM クラスに関連付けられている COMError オブジェクトは、COM.error メソッドを使用して COM クラスから取得されます。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                   | 説明                                                                                                               |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public str description() | COM オブジェクトが呼び出されたときに発生したエラーの説明を返します。                                          |
| public int helpContext() | COM オブジェクトが呼び出されたときに発生したエラーのヘルプ コンテキスト ID を返します。                                   |
| public str helpFile()    | COM オブジェクトが呼び出されたときに発生したエラーに関する情報が含まれるヘルプ ファイルの名前を返します。 |
| public int number()      | COM オブジェクトが呼び出されたときに発生したエラーのエラー コードを返します。                                         |
| public str source()      | COM オブジェクトが呼び出されたときに発生したエラーを引き起こしたコンポーネントの名前を返します。                     |
| public str toString()    | クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。                           |
| public void clear()      | COMError オブジェクトのプロパティをクリアします。                                                                             |
| public void new()        | COMError クラスのインスタンスを初期化します。                                                                            |
| public void finalize()   |                                                                                                                           |

### <a name="method-description"></a>メソッドの説明

COM オブジェクトが呼び出されたときに発生したエラーの説明を返します。

    public str description()

#### <a name="return-value"></a>戻り値

エラーの説明です。

#### <a name="remarks"></a>備考

COM オブジェクトがテキストのエラー メッセージの手渡しをサポートしていない場合は、説明が空白になることがあります。 説明のプロパティは読み取り専用です。

### <a name="method-helpcontext"></a>メソッド helpContext

COM オブジェクトが呼び出されたときに発生したエラーのヘルプ コンテキスト ID を返します。

    public int helpContext()

#### <a name="return-value"></a>戻り値

ヘルプ コンテキスト ID。

#### <a name="remarks"></a>備考

ヘルプ コンテキスト ID は、COM オブジェクトがエラーのヘルプをサポートしていない場合、0 (ゼロ) にすることができます。 helpContext プロパティは読み取り専用です。

### <a name="method-helpfile"></a>メソッド helpFile

COM オブジェクトが呼び出されたときに発生したエラーに関する情報が含まれるヘルプ ファイルの名前を返します。

    public str helpFile()

#### <a name="return-value"></a>戻り値

ヘルプ ファイルの名前。

#### <a name="remarks"></a>備考

ヘルプ ファイルは、COM オブジェクトがエラーのヘルプをサポートしていない場合、空にすることができます。 helpFile プロパティは読み取り専用です。

### <a name="method-number"></a>メソッド number

COM オブジェクトが呼び出されたときに発生したエラーのエラー コードを返します。

    public int number()

#### <a name="return-value"></a>戻り値

エラーコード。COM オブジェクトが呼び出されたときにエラーが発生しなかった場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

数プロパティは読み取り専用です。

### <a name="method-source"></a>メソッド source

COM オブジェクトが呼び出されたときに発生したエラーを引き起こしたコンポーネントの名前を返します。

    public str source()

#### <a name="return-value"></a>戻り値

エラーのソース。

#### <a name="remarks"></a>備考

COM オブジェクトがエラーのソースの手渡しをサポートしていない場合は、ソースが空白になることがあります。 ソースのプロパティは読み取り専用です。

### <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

クラスのテキストの説明。

#### <a name="remarks"></a>備考

ほとんどのクラスでは、返される文字列には、クラス ハンドルと名前が含まれています。 ただし、一部のクラスでは、文字列に追加情報が追加されます。

### <a name="method-clear"></a>メソッド clear

COMError オブジェクトのプロパティをクリアします。

    public void clear()

#### <a name="remarks"></a>備考

通常、COMError オブジェクトのプロパティは読み取り専用ですが、このメソッドを使用して解除できます。

### <a name="method-new"></a>メソッド new

COMError クラスのインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-commaio"></a>クラス CommaIo
    class CommaIo extends Io

CommaIo クラスには、コンマ区切りファイルの読み取りと書き込みを行う機能があります。

### <a name="remarks"></a>備考

このクラスは、CommaTextIo クラスに置き換えられました。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                       | 説明                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| public int filePosition()                    |                                                                                                                              |
| public str inFieldDelimiter(\[str value\])   | \*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。                                    |
| public str inRecordDelimiter(\[str value\])  | 完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。  |
| public int inRecordLength(\[int value\])     | ファイル内の各レコードを読み取る文字数を取得または設定します。                                                     |
| public str outFieldDelimiter(\[str value\])  | レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。          |
| public str outRecordDelimiter(\[str value\]) | 出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。 |
| public container read()                      | Io オブジェクトから次の完全なレコードを読み取ります。                                                                               |
| public IO\_Status status()                   | Io オブジェクトで実行された最後の操作のステータスを取得します。                                              |
| public boolean write(VarArg values)          | 単純型の値を記述します。                                                                                              |
| public boolean writeExp(container data)      | コンテナのコンテンツをファイルに記述します。                                                                                 |
| public void new(str filename, str mode)      | CommaIo クラスの新しいオブジェクトを作成します。                                                                                   |
| public void finalize()                       | ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。                                                  |

### <a name="method-fileposition"></a>メソッド filePosition

    public int filePosition()

#### <a name="return-value"></a>戻り値

### <a name="method-infielddelimiter"></a>メソッド inFieldDelimiter

\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。

### <a name="method-inrecorddelimiter"></a>メソッド inRecordDelimiter

完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

完全なレコードが読み込まれたかどうかを示す文字。

#### <a name="remarks"></a>備考

標準的なテキストについては、区切り記号は改行文字です。

### <a name="method-inrecordlength"></a>メソッド inRecordLength

ファイル内の各レコードを読み取る文字数を取得または設定します。

    public int inRecordLength([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ファイル内の各レコードを読み取る文字数。

#### <a name="remarks"></a>備考

固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。 レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。 固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。 inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。 レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。

### <a name="method-outfielddelimiter"></a>メソッド outFieldDelimiter

レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。

### <a name="method-outrecorddelimiter"></a>メソッド outRecordDelimiter

出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

出力ファイルに書き込まれる文字のシーケンス。

#### <a name="remarks"></a>備考

標準的なテキスト ファイルについては、区切り記号は改行文字です。

### <a name="method-read"></a>メソッド read

Io オブジェクトから次の完全なレコードを読み取ります。

    public container read()

#### <a name="return-value"></a>戻り値

Io オブジェクトからの次の完全なレコード。

#### <a name="remarks"></a>備考

次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength プロパティによって制御されます。 レコードはコンテナーとして返されます。 コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。 それぞれの特殊な Io クラスでは、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定を使用し、最も一般的な形式の入出力を有効にします。 ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。

### <a name="method-status"></a>メソッド status

Io オブジェクトで実行された最後の操作のステータスを取得します。

    public IO_Status status()

#### <a name="return-value"></a>戻り値

最後の操作の状態。システム列挙形式。

#### <a name="remarks"></a>備考

戻り値は、IO\_ステータス システムの列挙によって表されます。 可能性のある IO\_Status 値の範囲はクラスによって異なります。

#### <a name="examples"></a>例

この例は、状態メソッドを使用する方法を示しています。 ただし、この例は、クラス、フォーム、またはその他のオブジェクトのコンテキストで実行される必要があるため、ジョブはコンパイルされません。

    { 
        // Create an Io object and perform some operations. 
        if (myIo.status() == IO_Status::OK) 
        { 
            // Go ahead - the last operation was successful. 
        } 
    }

### <a name="method-write"></a>メソッド write

単純型の値を記述します。

    public boolean write(VarArg values)

#### <a name="parameters"></a>パラメーター

値  
1 つ以上の値の、各単純型は、フィールドの区切り記号で区切られています。 単純型は、文字列、整数、実数、列挙型、日付です。

#### <a name="return-value"></a>戻り値

書き込み操作が成功する場合は true。それ以外の場合は、false。 工程が失敗すると、ステータスをチェックし障害について確認できます。

#### <a name="remarks"></a>備考

このメソッドは、可変数の引数を受け入れます。 指定された各値は、フィールドとして出力レコードに配置されます。 最初の引数は最初のフィールドになり、2 番目の引数は 2 番目のフィールドなどになります。 フィールドは、outFieldDelimiter メソッドで指定されるフィールド区切り記号で区切られます。 レコードは、outRecordDelimiter メソッドを使用して指定される区切り記号で区切られます。 完全なコンテナーを書き込むには、writeExp メソッドを使用します。

### <a name="method-writeexp"></a>メソッド writeExp

コンテナのコンテンツをファイルに記述します。

    public boolean writeExp(container data)

#### <a name="parameters"></a>パラメーター

データ  
レコードのデータを保持するコンテナー。

#### <a name="return-value"></a>戻り値

操作が成功する場合は true。それ以外の場合は、false。 工程が失敗すると、ステータスをチェックし障害について確認できます。

#### <a name="remarks"></a>備考

コンテナー内のエントリはフィールドとして扱われます。 コンテナー自体は、完全なレコードとして扱われます。 フィールドは、outFieldDelimiter メソッドを使用して指定される区切り記号で区切られます。 レコードは、outRecordDelimiter メソッドを使用して指定される区切り記号で区切られます。

#### <a name="examples"></a>例

この例では、CommaIO オブジェクトを使用してサンプル ファイルから読み取ります。

    { 
        container c; 
        CommaIo myfile; 
        FileIoPermission perm; 

        #define.ExampleFile(@"c:\myfile.txt") 
        #define.ExampleOpenMode("w") 

        // Set code access permission to help protect the use 
        // of CommaIO.new 
        perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
        perm.assert(); 

        myfile = new CommaIo(#ExampleFile, #ExampleOpenMode); 

        // Assign the entries in the container according to record layout. 
        c = [1,"MyText",1.324,"Last field"]; 
        // Write this record according to file format  
        // (record/field delimiters). 
        myfile.writeExp(c); 

        // Close the code access permission. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-new"></a>メソッド new

CommaIo クラスの新しいオブジェクトを作成します。

    public void new(str filename, str mode)

#### <a name="parameters"></a>パラメーター

filename  
ファイルを開く必要があるモード。 次のようにモードを指定します。

<!-- -->

モード  
ファイルを開く必要があるモード。 次のようにモードを指定します。

#### <a name="remarks"></a>備考

ランタイム エラーは、現在のモードに対応していないメソッドを使用してファイルにアクセスした場合に発生します。 たとえば、ユーザーが読み取りモードで開いているファイルへの書き込みしようとすると、エラーが発生します。 攻撃者がこのメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

次の例では、CommaIO オブジェクトを使用して ExampleFile ファイルから読み取ります。

    { 
        CommaIo         io; 
        container       con; 
        FileIoPermission perm; 

        #define.ExampleFile(@"c:\test.txt") 
        #define.ExampleOpenMode("r") 

        perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
        if (perm == null) 
        { 
            return; 
        } 
        // Grants permission to execute the CommaIo.new method. 
        // CommaIo.new runs under code access security. 
        perm.assert(); 

        io = new CommaIo(#ExampleFile, #ExampleOpenMode); 
        if (io != null) 
        { 
            con = io.read(); 
        } 

        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。

    public void finalize()

#### <a name="remarks"></a>備考

このメソッドは通常は直接呼び出されません。代わりに、オブジェクトはスコープを離れることによって確定されます。 記述された出力はオブジェクトが終了するまで無効です。

## <a name="class-commatextio"></a>クラス CommaTextIo
    class CommaTextIo extends Io

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                    | 説明                                                                                                                  |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| public int filePosition()                                 |                                                                                                                              |
| public str inFieldDelimiter(\[str value\])                | \*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。                                    |
| public str inRecordDelimiter(\[str value\])               | 完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。  |
| public int inRecordLength(\[int value\])                  | ファイル内の各レコードを読み取る文字数を取得または設定します。                                                     |
| public str outFieldDelimiter(\[str value\])               | レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。          |
| public str outRecordDelimiter(\[str value\])              | 出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。 |
| public container read()                                   | Io オブジェクトから次の完全なレコードを読み取ります。                                                                               |
| public IO\_Status status()                                | Io オブジェクトで実行された最後の操作のステータスを取得します。                                              |
| public boolean write(VarArg values)                       | 単純型の値を記述します。                                                                                              |
| public boolean writeExp(container data)                   | コンテナのコンテンツをファイルに記述します。                                                                                 |
| public void finalize()                                    | ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。                                                  |
| public void new(str filename, str mode, \[int codepage\]) | Object クラスの新しいインスタンスを初期化します。                                                                              |

### <a name="method-fileposition"></a>メソッド filePosition

    public int filePosition()

#### <a name="return-value"></a>戻り値

### <a name="method-infielddelimiter"></a>メソッド inFieldDelimiter

\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。

### <a name="method-inrecorddelimiter"></a>メソッド inRecordDelimiter

完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

完全なレコードが読み込まれたかどうかを示す文字。

#### <a name="remarks"></a>備考

標準的なテキストについては、区切り記号は改行文字です。

### <a name="method-inrecordlength"></a>メソッド inRecordLength

ファイル内の各レコードを読み取る文字数を取得または設定します。

    public int inRecordLength([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ファイル内の各レコードを読み取る文字数。

#### <a name="remarks"></a>備考

固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。 レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。 固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。 inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。 レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。

### <a name="method-outfielddelimiter"></a>メソッド outFieldDelimiter

レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。

### <a name="method-outrecorddelimiter"></a>メソッド outRecordDelimiter

出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

出力ファイルに書き込まれる文字のシーケンス。

#### <a name="remarks"></a>備考

標準的なテキスト ファイルについては、区切り記号は改行文字です。

### <a name="method-read"></a>メソッド read

Io オブジェクトから次の完全なレコードを読み取ります。

    public container read()

#### <a name="return-value"></a>戻り値

入出力オブジェクトから次の完全なレコードを保持するコンテナーです。

#### <a name="remarks"></a>備考

次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。 レコードはコンテナーとして返されます。 コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。 それぞれの特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定があります。 これらの既定の設定では、最も一般的な形式の入力と出力が可能です。 ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。

### <a name="method-status"></a>メソッド status

Io オブジェクトで実行された最後の操作のステータスを取得します。

    public IO_Status status()

#### <a name="return-value"></a>戻り値

IO\_Status システム列挙値としての最後の操作の状態。

#### <a name="remarks"></a>備考

返される IO\_Status の値の範囲は、Io クラスによって異なります。

### <a name="method-write"></a>メソッド write

単純型の値を記述します。

    public boolean write(VarArg values)

#### <a name="parameters"></a>パラメーター

値  
単純型の値。 単純型は、文字列、整数、実数、列挙型、日付です。

#### <a name="return-value"></a>戻り値

書き込み操作が成功する場合は true。それ以外の場合は、false。 書き込み操作が失敗すると、ステータス メソッドを使用して、原因について確認できます。

#### <a name="remarks"></a>備考

このメソッドは、可変数の引数を受け入れます。 指定された各値は、フィールドとして出力レコードに配置されます。 最初の引数は最初のフィールドであり、2 番目の引数は 2 番目のフィールドなどになります。 フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。 レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。 完全なコンテナーを書き込むには、writeExp メソッドを使用します。

### <a name="method-writeexp"></a>メソッド writeExp

コンテナのコンテンツをファイルに記述します。

    public boolean writeExp(container data)

#### <a name="parameters"></a>パラメーター

データ  
レコードのデータを保持するコンテナー。

#### <a name="return-value"></a>戻り値

操作が成功する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドが false を返す場合、ステータス メソッドで原因を確認します。 コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。 フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。 レコード区切りは outRecordDelimiter メソッドで定義されます。

### <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。

    public void finalize()

#### <a name="remarks"></a>備考

このメソッドは、通常は直接呼び出されません。 代わりに、オブジェクトは通常、スコープを離れることによって確定されます。 記述された出力はオブジェクトが終了するまで無効です。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(str filename, str mode, [int codepage])

#### <a name="parameters"></a>パラメーター

filename  

<!-- -->

モード  

<!-- -->

codepage  

#### <a name="remarks"></a>備考

攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

## <a name="class-compileoutputinfos"></a>クラス CompileOutputInfos
    class CompileOutputInfos extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                               | 説明 |
|--------------------------------------|-------------|
| ::public static void NotifyChanges() |             |

### <a name="method-notifychanges"></a>メソッド NotifyChanges

    public static void NotifyChanges()

## <a name="class-comvariant"></a>クラス COMVariant
    class COMVariant extends Object

COMVariant クラスは、さまざまな種類のデータを格納できる一般的なクラスとして使用されます。 このクラスは、COM (コンポーネント オブジェクト モデル) 自動オブジェクトのメソッドまたはプロパティに引数を渡すために使用され、COM および COMDispFunction クラスとともに使用されます。

### <a name="remarks"></a>備考

COMVariant オブジェクトのデータ型は次によって設定できます。

-   新しいメソッド
-   variantType メソッド
-   createFrom… メソッド。 たとえば、createFromBoolean メソッドは、VT\_BOOL (= ブール値) のタイプの COMVariant オブジェクトを作成します。
-   プロパティ メソッド。 たとえば、boolean プロパティを使用して新しい値を設定すると、オブジェクトは VT\_BOOL (= Boolean) のタイプではなく、このタイプに変更されます。

データ型の値は、いずれかのプロパティ メソッドによって設定されます。 たとえば、タイプ VT\_BOOL の COMVariant オブジェクトの値は、boolean メソッドにより設定されます。 その値を設定する可能なデータ型とメソッドは、「備考」セクションに表示されます。 COMVariant クラスがサポートするデータ型は、X++ データ型ではなく、COMオートメーション標準によって定義されたデータ型です。 COMVariant クラスは、Win32 SDK にある VARIANT 構造に基づいています。 詳細については、Win32 SDK ドキュメントを参照してください。 COMVariant クラスのプロパティ メソッドは、次のように COMVariantType 値にマップされます。

|             |               |                                                                                           |
|-------------|---------------|-------------------------------------------------------------------------------------------|
| ブール値     | VT\_BOOL      |                                                                                           |
| bStr        | VT\_BSTR      | 文字列データ型                                                                          |
| byte        | VT\_UI1       |                                                                                           |
| char        | VT\_I1        |                                                                                           |
| 通貨    | VT\_CY        |                                                                                           |
| 日付、時刻  | VT\_DATE      | 日付/時刻データ型。両方のプロパティを設定する必要があります。                                         |
| decimal     | VT\_DECIMAL   |                                                                                           |
| double      | VT\_R8        |                                                                                           |
| float       | VT\_R4        |                                                                                           |
| iDispatch   | VT\_DISPATCH  |                                                                                           |
| int, long   | VT\_I4        | VT\_I4 は、int データ型と Long データ型の両方で使用されます                                   |
| iUnknown    | VT\_UNKNOWN   |                                                                                           |
| sCode       | VT\_ERROR     | scode データ型は、Win32 HRESULT データ型と同等の COM データ型です。 |
| short       | VT\_I2        |                                                                                           |
| uInt、uLong | VT\_UI4       | VT\_UI4 は、uInt データ型と uLong データ型の両方で使用されます                                |
| uShort      | VT\_UI2       |                                                                                           |
| バリアント     | VT\_VARIANT   |                                                                                           |
| safeArray   | VT\_SAFEARRAY | 配列データ タイプ                                                                           |

### <a name="examples"></a>例

次の例では、COMVariant パラメーターとして渡された 2 つの浮動小数点数を乗算する multiply というメソッドを公開する COM オブジェクトをインスタンス化します。

    { 
        COM com; 
        COMVariant varArg1 = new COMVariant(); 
        COMVariant varArg2 = new COMVariant(); 
        COMVariant varRet; 
        real ret; 
        InteropPermission perm; 

        // Set code access permission to help protect the use  
        // of the COM object. 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 

        // Permission scope starts here 
        perm.assert(); 

            com = new COM("MyCOM.Object"); 

        // Specify arguments for the 'multiply' method 
        varArg1.float(123); 
        varArg2.float(456); 
        varRet = com.multiply(varArg1, varArg2); 

        ret = varRet.double(); 
        // 'ret' is now 56088 (123*456) 

        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a>メソッド

| 方法                                                                                                    | 説明                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean boolean(\[boolean newValue\])                                                              | VT\_BOOL データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                    |
| public str bStr(\[str newValue\])                                                                         | VT\_BSTR データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                    |
| public int byte(\[int newValue\])                                                                         | VT\_UI1 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                     |
| public int char(\[int newValue\])                                                                         | VT\_I1 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public container container(\[container newValue\], \[COMVariantType newType\])                            | コンテナ データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                   |
| public Real currency(\[Real newValue\])                                                                   | VT\_CY データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public Date date(\[Date newValue\])                                                                       | VT\_DATE データ タイプの COMVariant オブジェクトの値の日付部分を取得または設定します。                                                                                   |
| public Real decimal(\[Real newValue\])                                                                    | VT\_DECIMAL データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                 |
| public Real double(\[Real newValue\])                                                                     | VT\_R8 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public Real float(\[Real newValue\])                                                                      | VT\_R4 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public ComInterface iDispatch(\[ComInterface newValue\])                                                  | VT\_DISPATCH データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                |
| public int int(\[int newValue\])                                                                          | VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public ComInterface iUnknown(\[ComInterface newValue\])                                                   | VT\_UNKNOWN (IUnknown) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                      |
| public int long(\[int newValue\])                                                                         | VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                      |
| public Int64 longLong(\[Int64 newValue\])                                                                 | VT\_I8 (longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                           |
| public Array safeArray(\[Array newValue\], \[COMVariantType newType\])                                    | VT\_SAFEARRAY データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                               |
| public int sCode(\[int newValue\])                                                                        | VT\_ERROR データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                   |
| public int short(\[int newValue\])                                                                        | VT\_I2 (短い) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                              |
| public int time(\[int newValue\])                                                                         | VT\_DATE データ タイプの COMVariant オブジェクトの値の時刻部分を取得または設定します。                                                                                   |
| public str toString()                                                                                     | COMVariant オブジェクトの文字列形式を作成します。 この文字列形式には、オブジェクトの値と型が含まれます。                                               |
| public int uInt(\[int newValue\])                                                                         | VT\_UI4 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                     |
| public int uLong(\[int newValue\])                                                                        | VT\_UI4 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                     |
| public Int64 uLongLong(\[Int64 newValue\])                                                                | VT\_UI8 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                 |
| public int uShort(\[int newValue\])                                                                       | VT\_UI2 データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                                     |
| public COMVariant variant(\[COMVariant newValue\])                                                        | VT\_VARIANT (バリアント) データ タイプの COMVariant オブジェクトの値を取得または設定します。                                                                                       |
| public COMVariantInOut variantInOutFlag(\[COMVariantInOut newValue\])                                     | COMVariant オブジェクトに対する InOutFlag 設定を設定する返します。                                                                                                              |
| public COMVariantType variantType(\[COMVariantType newValue\])                                            | COMVariant オブジェクトにそのバリアント データ型を照会するか、データ型を変更します。                                                                                             |
| ::public static COMVariant createDateFromYMD(int year, int month, int day, \[COMVariantInOut inOutFlag\]) | 新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。                                                                                      |
| ::public static COMVariant createFromArray(Array value, \[COMVariantInOut inOutFlag\])                    | 新しい COMVariant オブジェクトを作成し、1 回の操作で配列で初期化します。                                                                                          |
| ::public static COMVariant createFromBoolean(boolean value, \[COMVariantInOut inOutFlag\])                | 新しい COMVariant オブジェクトを作成し、1 回の操作でブール値で初期化します。                                                                                   |
| ::public static COMVariant createFromCOM(COM value, \[COMVariantInOut inOutFlag\])                        | 新しい COMVariant オブジェクトを作成し、1 回の操作で COM クラスで初期化します。                                                                                       |
| ::public static COMVariant createFromDate(Date value, \[COMVariantInOut inOutFlag\])                      | 新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。                                                                                      |
| ::public static COMVariant createFromDateAndTime(Date date, int time, \[COMVariantInOut inOutFlag\])      | 新しい COMVariant オブジェクトを作成し、1 回の操作で日時で初期化します。                                                                                   |
| ::public static COMVariant createFromInt(int value, \[COMVariantInOut inOutFlag\])                        | 新しい COMVariant オブジェクトを作成し、1 回の操作で整数値で初期化します。                                                                                  |
| ::public static COMVariant createFromInt64(Int64 value, \[COMVariantInOut inOutFlag\])                    | 新しい COMVariant オブジェクトを作成し、1 回の操作でint64 値 (longLong や uLongLong) で初期化します。                                                            |
| ::public static COMVariant createFromReal(Real value, \[COMVariantInOut inOutFlag\])                      | 新しい COMVariant オブジェクトを作成し、1 回の操作で実際の値で初期化します。                                                                                      |
| ::public static COMVariant createFromStr(str value, \[COMVariantInOut inOutFlag\])                        | 新しい COMVariant オブジェクトを作成し、1 回の操作で文字列で初期化します。                                                                                          |
| ::public static COMVariant createFromTime(int value, \[COMVariantInOut inOutFlag\])                       | 新しい COMVariant オブジェクトを作成し、1 回の操作で時刻値で初期化します。                                                                                      |
| ::public static COMVariant createFromUtcDateTime(DateTime value, \[COMVariantInOut inOutFlag\])           |                                                                                                                                                                             |
| ::public static COMVariant createNoValue()                                                                | 値を持たない VT\_エラー バリアント タイプの COMVariant オブジェクトを作成します。                                                                                                    |
| public void new(\[COMVariantInOut inOutFlag\], \[COMVariantType type\])                                   | COM オートメーション オブジェクトのメソッドまたはプロパティに引数を渡すために使用できる COMVariant オブジェクトを作成します。                                                     |
| public void noValue()                                                                                     | 既存の COMVariant オブジェクトの内容を削除し、COMDispFunction.call メソッドまたは COM クラスで使用されている場合は、未指定の引数として機能させることができます。 |
| public void finalize()                                                                                    | 実装されていません。 明示的にオブジェクトを破棄する必要がある場合は、このメソッドをオーバーライドすることができます。                                                                                 |

### <a name="method-boolean"></a>メソッド boolean

VT\_BOOL データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public boolean boolean([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_BOOL に設定されている場合、COMVariant オブジェクトはブール型です。 COM ブール値のデータ型は、"VARIANT\_BOOL" とも呼ばれることがあります。

#### <a name="examples"></a>例

次の例では、VT\_BOOL 型の新しい COMVariant オブジェクトを作成し、値を true に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_BOOL); 

        // Set value of the object 
        var.boolean(true); 
    }

### <a name="method-bstr"></a>メソッド bStr

VT\_BSTR データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public str bStr([str newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の文字列の価値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_BSTR に設定されている場合、COMVariant オブジェクトは文字列データ型です。 BStr データ型は、文字列の処理に使用される COM データ型です。

#### <a name="examples"></a>例

次の例では、VT\_BSTR 型の新しい COMVariant オブジェクトを作成し、値を "Hello World" に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_BSTR); 

        // Set string value of the object 
        var.bStr("Hello World"); 
    }

### <a name="method-byte"></a>メソッド byte

VT\_UI1 データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public int byte([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_UI1 に設定されている場合、COMVariant オブジェクトはバイト データ型です。 また、「符号なし文字型」を使用して COM バイト データ型を参照することができます。

#### <a name="examples"></a>例

次の例では、VT\_UI1 型の新しい COMVariant オブジェクトを作成し、値を 123 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UI1); 

        // Set value of the object 
        var.byte(123); 
    }

### <a name="method-char"></a>メソッド char

VT\_I1 データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public int char([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_I1 に設定されている場合、COMVariant オブジェクトは char データ型です。

#### <a name="examples"></a>例

次の例では、VT\_I1 型の 新しい COMVariant オブジェクトを作成し、値を 65 の、A の数値に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I1); 

        // Set value of the object 
        var.char(Char2Num("A", 1)); 
    }

### <a name="method-container"></a>メソッド container

コンテナ データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public container container([container newValue], [COMVariantType newType])

#### <a name="parameters"></a>パラメーター

newValue  
新しいコンテナーのタイプ (オプション)。 既定では、コンテナーが整数を格納します。

<!-- -->

newType  
新しいコンテナーのタイプ (オプション)。 既定では、コンテナーが整数を格納します。

#### <a name="return-value"></a>戻り値

現在のコンテナー。

#### <a name="remarks"></a>備考

newType パラメーターの使用可能な値は、COMVariantType システム列挙によって提供される値のサブセットです。

-   VT\_I2
-   VT\_I4
-   VT\_R4
-   VT\_R8
-   VT\_CY
-   VT\_DATE
-   VT\_BSTR
-   VT\_ERROR
-   VT\_BOOL
-   VT\_DECIMAL
-   VT\_I1
-   VT\_UI1
-   VT\_UI2
-   VT\_UI4
-   VT\_I8
-   VT\_UI8
-   VT\_INT
-   VT\_UINT

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 コンテナーが COMVariant オブジェクトに保存されると、コンテナーのバイナリ表現がバイナリ配列に保存されます (COMVariant.safeArray メソッドを参照してください)。 コンテナーのプロパティは、データベース COM オブジェクトにデータを格納し、後でデータを処理する COM オブジェクトを使用せずに Finance and Operations にデータを読み戻す必要がある場合に便利です。 コンテナーのプロパティは、COMVariant クラスの高度なプロパティです。 COMVariant オブジェクト内で、コンテナーが格納されるバイナリ配列の内容は、どの COM オブジェクトによっても変更されないようにしなければならないため、注意して使用する必要があります。

#### <a name="examples"></a>例

次の例では、コンテナー 型の新しい COMVariant オブジェクトを作成します。 コンテナー内のデータは、データベース COM オブジェクトに渡され、データベース COM オブジェクトによって使用されます。 注記: 次のセクションのコードには仮想 COM オブジェクト (「MyDatabaseCOM.Object」) が含まれており、Finance and Operations の外部でオブジェクトが作成されていない限り、Finance and Operations では実行されません。

    { 
        COM com; 
        COMVariant var = new COMVariant(); 
        container con; 
        InteropPermission perm; 

        // Set code access permission to help protect use of COM object 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 

        // Permission scope starts here 
        perm.assert(); 

        // Put some data in the container 
        con = conins(con, 1, "Element 1"); 
        con = conins(con, 2, "Element 2"); 
        // Set value of the object and ensure the data 
        // is stored in a binary array of bytes 
        var.container(con, COMVariantType::VT_UI1); 

        // Create a database object to store the data in 
        com = new COM("MyDatabaseCOM.Object"); 
        com.writeData(var); 
        // ... 

        // Close code access permission 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-currency"></a>メソッド currency

VT\_CY データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public Real currency([Real newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_CY に設定されている場合、COMVariant オブジェクトは 通貨データ型です。 通貨データ型は、通貨値に最適化された COM データ型です。 小数点以下 4 桁のある実数です。 場合によっては、COM 通貨データ型を参照するために "CY" も使用されます。

#### <a name="examples"></a>例

次の例では、VT\_CY 型の新しい COMVariant オブジェクトを作成し、値を 123.4567 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_CY); 

        // Set value of the object 
        var.currency(123.4567); 
    }

### <a name="method-date"></a>メソッド date

VT\_DATE データ タイプの COMVariant オブジェクトの値の日付部分を取得または設定します。

    public Date date([Date newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_DATE に設定されている場合、COMVariant オブジェクトは 日時データ型です。 オブジェクトの値を設定するとき、日付に加えて、値の時刻の部分を設定する必要があります。 値の時間部分を設定するには、time プロパティを使用します。

#### <a name="examples"></a>例

次の例では、VT\_DATE 型の COMVariant オブジェクトを作成し、値の日付部分を 1998 年 12 月 24 日に設定し、時刻の部分を 13.24 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_DATE); 

        // Set value of the object 
        var.date(Str2Date("12.24.1998", 213)); 
        var.time(Str2Time("13:24:00")); 
    }

### <a name="method-decimal"></a>メソッド decimal

VT\_DECIMAL データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public Real decimal([Real newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_DECIMAL に設定されている場合、COMVariant オブジェクトは 10 進型です。 10進データ型は、数値のサイズとスケールを提供する COM データ型です。 X++ には 10 進データ型と並行するものはありません。

#### <a name="examples"></a>例

次の例では、VT\_DECIMAL 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_DECIMAL); 

        // Set value of the object 
        var.decimal(123.456); 
    }

### <a name="method-double"></a>メソッド double

VT\_R8 データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public Real double([Real newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_R8 に設定されている場合、COMVariant オブジェクトはダブル データ型です。

#### <a name="examples"></a>例

次の例では、VT\_R8 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_R8); 

        // Set value of the object 
        var.double(123.456); 
    }

### <a name="method-float"></a>メソッド float

VT\_R4 データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public Real float([Real newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_R4 に設定されている場合、COMVariant オブジェクトは float 型です。 場合によっては、COM 浮動小数点データ型を参照するために "single" も使用されます。

#### <a name="examples"></a>例

次の例では、VT\_R4 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_R4); 

        // Set value of the object 
        var.float(123.456); 
    }

### <a name="method-idispatch"></a>メソッド iDispatch

VT\_DISPATCH データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public ComInterface iDispatch([ComInterface newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_DISPATCH に設定されている場合、COMVariant オブジェクトは IDispatch データ型です。 IDispatch データ型は、COM IDispatch インターフェイスへのハンドルを提供する COM データ型です。

#### <a name="examples"></a>例

次の例では、VT\_DISPATCH 型の新しい COMVariant オブジェクトを作成します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_DISPATCH); 
        COMInterface comInterface; 

        // Here, the comInterface variable must be assigned 
        // a COM IDispatch interface 
        //… 

        // Set value of the object 
        var.iDispatch(comInterface); 
    }

### <a name="method-int"></a>メソッド int

VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public int int([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 COMVariantType::VT\_I4 データ型は long バリアント型にも使用されます。 COMVariant.long メソッドは、このメソッドと同じです。2 つのメソッドは、完全性のために存在します。

#### <a name="examples"></a>例

次の例では、VT\_I4 型の COMVariant オブジェクトを作成し、値を 123456 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I4); 

        // Set value of the object 
        var.int(123456); 
    }

### <a name="method-iunknown"></a>メソッド iUnknown

VT\_UNKNOWN (IUnknown) データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public ComInterface iUnknown([ComInterface newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、データ型の値に合わせて変更されます。 そのデータ型が COMVariantType::VT\_UNKNOWN に設定されている場合、COMVariant オブジェクトは IUnknown データ型です。 IUnknown データ型は、COM IUnknown インターフェイスへのハンドルを提供する COM データ型です。

#### <a name="examples"></a>例

次の例では、VT\_UNKNOWN 型の新しい COMVariant オブジェクトを作成します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UNKNOWN); 
        COMInterface comInterface; 

        // comInterface variable is assigned 
        // a COM IUnknown interface 
        // ... 

        // Set value of the object 
        var.iUnknown(comInterface); 
    }

### <a name="method-long"></a>メソッド long

VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public int long([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 COMVariantType::VT\_I4 データ型は int バリアント型にも使用されます。 COMVariant.int メソッドは、このメソッドと同じです。2 つのメソッドは、完全性のために存在します。

#### <a name="examples"></a>例

次の例では、VT\_I4 型の COMVariant オブジェクトを作成し、値を 123456 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I4); 

        // Set value of the object 
        var.long(123456); 
    }

### <a name="method-longlong"></a>メソッド longLong

VT\_I8 (longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public Int64 longLong([Int64 newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_I8 に設定されている場合、COMVariant オブジェクトは longlong バリアント型です。

#### <a name="examples"></a>例

次の例では、VT\_I8 型の新しい COMVariant オブジェクトを作成し、値を 2,305,843,009,213,693,952 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_BOOL); 

        // Set value of the object 
        var.longLong(2305843009213693952); 
    }

### <a name="method-safearray"></a>メソッド safeArray

VT\_SAFEARRAY データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public Array safeArray([Array newValue], [COMVariantType newType])

#### <a name="parameters"></a>パラメーター

newValue  
新しい配列のタイプ (オプション)。

<!-- -->

newType  
新しい配列のタイプ (オプション)。

#### <a name="return-value"></a>戻り値

現在の配列。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_SAFEARRAY に設定されている場合、COMVariant オブジェクトは配列ブール型です。 セーフ配列は、COM の配列に相当します。 現在、1 次元セーフ配列のみがサポートされています。

#### <a name="examples"></a>例

次の例では、VT\_SAFEARRAY 型の新しい COMVariant オブジェクトを作成し、short 配列で初期化します。

    { 
        int i, result; 
        COM com; 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_SAFEARRAY); 
        Array arr = new Array(Types::INTEGER); 

        // Insert 10 values in the array 
        for (i = 1; i <= 10; i++) 
        { 
            arr.value(i, i); 
        } 

        // Set value of the object and ensure the integer values 
        // are treated as short data types 
        var.safeArray(arr, COMVariantType::VT_I2); 
    }

### <a name="method-scode"></a>メソッド sCode

VT\_ERROR データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public int sCode([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_ERROR に設定されている場合、COMVariant オブジェクトは scode データ型です。 scode データ型は、COM 関数の戻り値として最もよく使用される Win32 HRESULT データ型と同等の COM データ型です。

#### <a name="examples"></a>例

次の例では、VT\_ERROR 型の新しい COMVariant オブジェクトを作成し、値を 0x80001004 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_ERROR); 

        // Set value of the object 
        var.sCode(0x80001004); 
    }

### <a name="method-short"></a>メソッド short

VT\_I2 (短い) データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public int short([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_I2 に設定されている場合、COMVariant オブジェクトはショート データ型です。

#### <a name="examples"></a>例

次の例では、VT\_I2 型の新しい COMVariant オブジェクトを作成し、値を 123 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I2); 

        // Set value of the object 
        var.short(123); 
    }

### <a name="method-time"></a>メソッド time

VT\_DATE データ タイプの COMVariant オブジェクトの値の時刻部分を取得または設定します。

    public int time([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_DATE に設定されている場合、COMVariant オブジェクトは 日時データ型です。 オブジェクトの値を設定するとき、時刻に加えて、値の日付の部分を設定する必要があります。 値の日付部分を設定するには、date プロパティを使用します。

#### <a name="examples"></a>例

次の例では、VT\_DATE 型の COMVariant オブジェクトを作成し、値の日付部分を 1998 年 12 月 24 日に設定し、時刻の部分を 13.24 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_DATE); 

        // Set value of the object 
        var.date(Str2Date("12.24.1998", 213)); 
        var.time(Str2Time("13:24:00")); 
    }

### <a name="method-tostring"></a>メソッド toString

COMVariant オブジェクトの文字列形式を作成します。 この文字列形式には、オブジェクトの値と型が含まれます。

    public str toString()

#### <a name="return-value"></a>戻り値

COMVariant オブジェクトの文字列表現。

#### <a name="remarks"></a>備考

このメソッドから返される実際の文字列は、COMVariant オブジェクトのバリアント データ型によって異なります。

#### <a name="examples"></a>例

次の例では、COMVariant オブジェクトを作成し、現在の日付を割り当てます。 情報ログにオブジェクトの説明を出力します。

    COMVariant theDay; 

    theDay = COMVariant::createFromDate(today()); 
    info(theDay.toString());

### <a name="method-uint"></a>メソッド uInt

VT\_UI4 データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public int uInt([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 COMVariantType::VT\_UI4 データ型は uLong データ型にも使用されます。

#### <a name="examples"></a>例

次の例では、VT\_UI4 型の新しい COMVariant オブジェクトを作成し、値を 123456 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UI4); 

        // Set value of the object 
        var.uInt(123456); 
    }

### <a name="method-ulong"></a>メソッド uLong

VT\_UI4 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public int uLong([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 COMVariantType::VT\_UI4 データ型は uInt データ型にも使用されます。

#### <a name="examples"></a>例

次の例では、VT\_UI4 型の新しい COMVariant オブジェクトを作成し、値を 123456 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UI4); 

        // set value of the object 
        var.uLong(123456); 
    }

### <a name="method-ulonglong"></a>メソッド uLongLong

VT\_UI8 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public Int64 uLongLong([Int64 newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_I8 に設定されている場合、COMVariant オブジェクトは未署名の longlong バリアント型です。

#### <a name="examples"></a>例

次の例では、VT\_I8 型の新しい COMVariant オブジェクトを作成し、値を 9,223,372,036,854,775,808 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_BOOL); 

        // Set value of the object 
        var.longLong(9223372036854775808); 
    }

### <a name="method-ushort"></a>メソッド uShort

VT\_UI2 データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public int uShort([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_UI2 に設定されている場合、COMVariant オブジェクトは未署名の ショート データ型です。

#### <a name="examples"></a>例

次の例では、VT\_UI2 型の新しい COMVariant オブジェクトを作成し、値を 12345 に設定します。

    { 
        COMVariant var = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_UI2); 

        // Set value of the object 
        var.uShort(12345); 
    }

### <a name="method-variant"></a>メソッド variant

VT\_VARIANT (バリアント) データ タイプの COMVariant オブジェクトの値を取得または設定します。

    public COMVariant variant([COMVariant newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

現在の値。

#### <a name="remarks"></a>備考

variant プロパティは、ある COMVariant オブジェクトを別の COMVariant オブジェクトにネストするために使用されます。 親オブジェクトを COMDispFunction.call への呼び出しまたは COM クラスへの呼び出しの引数として使用する場合、呼び出されたメソッドは自動的に入れ子になったオブジェクトのデータを抽出します。 このネスト機能は、COM オブジェクトのメソッドが複数のデータ型で動作できる場合に便利です。 バリアントの入れ子は 1 つのレベルのみ許可されます。 オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。 そのデータ型が COMVariantType::VT\_VARIANT に設定されている場合、COMVariant オブジェクトはバリアント型です。

#### <a name="examples"></a>例

次の例では、VT\_I4 (long) 型の COMVariant オブジェクトと VT\_VARIANT 型の COMVariant オブジェクトを作成します. VT\_VARIANT タイプのオブジェクトには、VT\_I4 タイプのオブジェクトの値が割り当てられます。 以下のコードには仮想 COM オブジェクト (「MyCOM.Object」) が含まれており、Finance and Operations の外部でオブジェクトが作成されていない限り、Finance and Operations では実行されません。

    { 
        COM com; 
        COMDispFunction funcShow; 

        COMVariant var1 = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_I4); 

        COMVariant var2 = new COMVariant( 
            COMVariantInOut::IN_OUT,  
            COMVariantType::VT_VARIANT); 

        InteropPermission perm1; 
        InteropPermission perm2; 

        // Set code access permission to help protect use of COM object 
        perm1 = new InteropPermission(InteropKind::ComInterop); 
        perm1.assert(); 

        com = new COM("MyCOM.Object"); 

        // Close code access permission for COM 
        CodeAccessPermission::revertAssert(); 

        // Set value of 'var1' 
        var1.Long(123456); 
        // Set value of 'var2' to 'var1' 
        var2.Variant(var1); 

        // Set code access permission to protect use of 
        // COMDispFunction object 
        perm2 = new InteropPermission(InteropKind::ComInterop); 
        perm2.assert(); 

        funcShow = new COMDispFunction( 
            com,  
            "Show",  
            COMDispContext::METHOD); 

        // Call funcShow with a long 
        funcShow.Call(var2); 
        // Change value of 'var1' 
         var1.BStr("Hello World"); 
        // Call funcShow with a string 
        funcShow.Call(var2); 

        // Close code access permission for COMDispFunction 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-variantinoutflag"></a>メソッド variantInOutFlag

COMVariant オブジェクトに対する InOutFlag 設定を設定する返します。

    public COMVariantInOut variantInOutFlag([COMVariantInOut newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しい InOutFlag 設定 (オプション)。

#### <a name="return-value"></a>戻り値

現在の InOutFlag 設定。

#### <a name="remarks"></a>備考

次に、newValue パラメーターで使用可能な値のリストを示します。

-   COMVariantInOut::IN
-   COMVariantInOut::IN\_OUT
-   COMVariantInOut::OUT
-   COMVariantInOut::OUT\_戻り値。

InOutFlag 設定は、オブジェクトが COMDispFunction.call メソッドで引数として使用されたときに、オブジェクトに格納されているデータがどのように扱われるかを記述します。 InOutFlag 設定の使用可能な値は、Win32 SDK に記述されている COM オートメーション オブジェクトの値に対応します。 COMVariant オブジェクトに格納されたデータは、InOutFlag 設定が変更されても影響を受けません。

#### <a name="examples"></a>例

次の例では、InOutFlag 設定が IN に設定されている COMVariant オブジェクトを作成し、variantInOutFlag メソッドを使用して設定を OUT に変更します。

    { 
        COMVariant var = new COMVariant(COMVariantInOut::IN); 

        // Change the 'var' object to be used as an out argument 
        var.variantInOutFlag(COMVariantInOut::OUT); 
    }

### <a name="method-varianttype"></a>メソッド variantType

COMVariant オブジェクトにそのバリアント データ型を照会するか、データ型を変更します。

    public COMVariantType variantType([COMVariantType newValue])

#### <a name="parameters"></a>パラメーター

newValue  
新しいバリアント データ型 (オプション)。

#### <a name="return-value"></a>戻り値

現在のバリアント データ型。

#### <a name="remarks"></a>備考

newValue パラメーターの使用可能な値は次のとおりです。

-   COMVariantType::VT\_I2
-   COMVariantType::VT\_I4
-   COMVariantType::VT\_R4
-   COMVariantType::VT\_R8
-   COMVariantType::VT\_CY
-   COMVariantType::VT\_日付
-   COMVariantType::VT\_BSTR
-   COMVariantType::VT\_出荷
-   COMVariantType::VT\_エラー
-   COMVariantType::VT\_ブール値
-   COMVariantType::VT\_バリアント
-   COMVariantType::VT\_不明
-   COMVariantType::VT\_10 進値
-   COMVariantType::VT\_I1
-   COMVariantType::VT\_UI1
-   COMVariantType::VT\_UI2
-   COMVariantType::VT\_UI4

バリアント データ型は、オブジェクトが COMDispFunction.call メソッドの呼び出しまたは COM クラスの呼び出しで引数として使用されたときに、オブジェクトに格納されているデータがどのように扱われるかを記述します。 データ型を変更すると、オブジェクトに保持されているデータは削除されます。 使用可能なバリアント データ型については、\[COMVariant.new\] を参照してください。

#### <a name="examples"></a>例

次の例では、新しい COMVariant オブジェクトを作成し、それを long (VT\_I4) データ型に設定します。 その後、variantType メソッドを使用して、データ型を VT\_DATE (日付) に変更します。 オブジェクトが保持するデータは破棄されます。

    { 
        COMVariant var = new COMVariant(); 

        // Set the 'var' object to be a long 
        var.long(123); 

        // Change var so that it can store a date 
        var.variantType(COMVariantType::VT_DATE); 
    }

### <a name="method-createdatefromymd"></a>メソッド createDateFromYMD

新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。

    public static COMVariant createDateFromYMD(int year, int month, int day, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

年  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値: COMVariantInOut::OUT\_RETVAL

<!-- -->

月  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値: COMVariantInOut::OUT\_RETVAL

<!-- -->

日  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値: COMVariantInOut::OUT\_RETVAL

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値: COMVariantInOut::OUT\_RETVAL

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。 このメソッドを使用すると、Finance and Operationsdate データ型 (0111901〜31122154) の範囲外の日付を使用できます。 日付範囲内の日付で、COMVariant.createFromDate メソッドを使用することができます。

#### <a name="examples"></a>例

次の例では、COMVariant オブジェクトを作成し、4015 年 1 月 1 日の日付で初期化します。

    COMVariant myDate; 

    myDate = COMVariant::createDateFromYMD(4015,1,1);

### <a name="method-createfromarray"></a>メソッド createFromArray

新しい COMVariant オブジェクトを作成し、1 回の操作で配列で初期化します。

    public static COMVariant createFromArray(Array value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_SAFEARRAY (配列) を持っています。 variantType メソッドの使用により、または safeArray プロパティ メソッドを使用して配列値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_SAFEARRAY に変更することができます。

#### <a name="examples"></a>例

次の例では、新しい COMVariant オブジェクトを作成し、整数の配列で初期化します。

    { 
        int i; 
        COMVariant var; 
        Array arr = new Array(Types::INTEGER); 

        for (i = 1; i <= 10; i++) 
            // Insert 10 values in the array 
            arr.value(i, i); 

        // Create and initialize a COMVariant object  
        var = COMVariant::createFromArray(arr); 
    }

### <a name="method-createfromboolean"></a>メソッド createFromBoolean

新しい COMVariant オブジェクトを作成し、1 回の操作でブール値で初期化します。

    public static COMVariant createFromBoolean(boolean value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_BOOL (ブール値) を持っています。 variantType メソッドの使用により、または boolean プロパティ メソッドを使用してブール値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_BOOL に変更することができます。

#### <a name="examples"></a>例

次の例では、VT\_BOOL バリアント データ型 (ブール値) の COMVariant オブジェクトを作成し、その値を true に設定します。

    { 
        COMVariant var; 

        var = COMVariant::createFromBoolean(TRUE); 
    }

### <a name="method-createfromcom"></a>メソッド createFromCOM

新しい COMVariant オブジェクトを作成し、1 回の操作で COM クラスで初期化します。

    public static COMVariant createFromCOM(COM value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

inOutFlag パラメーターの使用可能な値は次のとおりです。

-   COMVariantInOut::IN
-   COMVariantInOut::IN\_OUT
-   COMVariantInOut::OUT
-   COMVariantInOut::OUT\_戻り値

#### <a name="examples"></a>例

次の例では、新しい COMVariant オブジェクトを作成し、COM オブジェクトで初期化します。

    { 
        COMVariant var; 
        COM com = new COM("MyCOM.Object"); 

        var = COMVariant::createFromCOM(com); 
    }

### <a name="method-createfromdate"></a>メソッド createFromDate

新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。

    public static COMVariant createFromDate(Date value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。 variantType メソッドの使用により、または date プロパティ メソッドを使用して時刻値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_DATE に変更することができます。 Axapta の日付タイプ (0111901〜31122154) の範囲外の日付を使用する場合は、COMVariant.createDateFromYMD メソッドを使用します。

#### <a name="examples"></a>例

次の例では、COMVariant オブジェクトを作成し、現在の日付で初期化します。

    COMVariant theDay; 

    theDay = COMVariant::createFromDate(today()); 
    info(theDay.toString());

### <a name="method-createfromdateandtime"></a>メソッド createFromDateAndTime

新しい COMVariant オブジェクトを作成し、1 回の操作で日時で初期化します。

    public static COMVariant createFromDateAndTime(Date date, int time, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

日付  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

タイム  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。 variantType メソッドを使用することにより、既存の COMVariant オブジェクトを VT\_DATE に変更することができます。

#### <a name="examples"></a>例

次の例では、COMVariant オブジェクトを作成し、現在の日付と深夜 0 時から 10 秒の間隔の時刻を割り当てます。

    date theDay; 
    COMVariant theDayAndTime; 

    theDay = today(); 
    theDayAndTime = COMVariant::createFromDateAndTime(theDay, 10); 
    info(theDayAndTime.toString());

### <a name="method-createfromint"></a>メソッド createFromInt

新しい COMVariant オブジェクトを作成し、1 回の操作で整数値で初期化します。

    public static COMVariant createFromInt(int value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_I4 (整数) を持っています。 variantType メソッドの使用により、または int プロパティ メソッドを使用して整数値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_I4 に変更することができます。

#### <a name="examples"></a>例

次の例では、VT\_I4 バリアント データ型 (整数) の COMVariant オブジェクトを作成し、値を 123 に設定します。

    { 
        COMVariant var; 

        var = COMVariant::createFromInt(123); 
    }

### <a name="method-createfromint64"></a>メソッド createFromInt64

新しい COMVariant オブジェクトを作成し、1 回の操作でint64 値 (longLong や uLongLong) で初期化します。

    public static COMVariant createFromInt64(Int64 value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_I8 (int64) を持っています。 variantType メソッドの使用により、または longLong や uLongLong プロパティ メソッドを使用して int64 値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_I8 に変更することができます。

#### <a name="examples"></a>例

次の例では、VT\_I8 バリアント データ型 (整数) の COMVariant オブジェクトを作成し、値を 123456 に設定します。

    { 
        COMVariant var; 

        var = COMVariant::createFromInt64(123456); 
    }

### <a name="method-createfromreal"></a>メソッド createFromReal

新しい COMVariant オブジェクトを作成し、1 回の操作で実際の値で初期化します。

    public static COMVariant createFromReal(Real value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_R8 (実数) を持っています。 variantType メソッドの使用により、または double プロパティ メソッドを使用してブール値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_R8 に変更することができます。

#### <a name="examples"></a>例

次の例では、VT\_R8 バリアント データ型 (実数) の COMVariant オブジェクトを作成し、値を 123.456 に設定します。

    { 
        COMVariant var; 

        var = COMVariant::createFromReal(123.456); 
    }

### <a name="method-createfromstr"></a>メソッド createFromStr

新しい COMVariant オブジェクトを作成し、1 回の操作で文字列で初期化します。

    public static COMVariant createFromStr(str value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_BSTR (文字列) を持っています。 variantType メソッドの使用により、または bStr プロパティ メソッドを使用して文字列値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_BSTR に変更することができます。

#### <a name="examples"></a>例

次の例では、VT\_BSTR バリアント データ型の COMVariant オブジェクトを作成し、値を "Hello World" に設定します。

    { 
        COMVariant var; 

        var = COMVariant::createFromStr("Hello World"); 
    }

### <a name="method-createfromtime"></a>メソッド createFromTime

新しい COMVariant オブジェクトを作成し、1 回の操作で時刻値で初期化します。

    public static COMVariant createFromTime(int value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

<!-- -->

inOutFlag  
オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。 このパラメーターはオプションです。 有効値:

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。 variantType メソッドの使用により、または time プロパティ メソッドを使用して時刻値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_DATE に変更することができます。

#### <a name="examples"></a>例

次の例では、COMVariant オブジェクトを作成し、時刻の部分を深夜 0 時から 10 秒の間隔に設定します。

    COMVariant theTime; 

    theTime = COMVariant::createFromTime(10); 
    info(theTime.toString());

### <a name="method-createfromutcdatetime"></a>メソッド createFromUtcDateTime

    public static COMVariant createFromUtcDateTime(DateTime value, [COMVariantInOut inOutFlag])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

inOutFlag  

#### <a name="return-value"></a>戻り値

### <a name="method-createnovalue"></a>メソッド createNoValue

値を持たない VT\_エラー バリアント タイプの COMVariant オブジェクトを作成します。

    public static COMVariant createNoValue()

#### <a name="return-value"></a>戻り値

新しい COMVariant オブジェクト。

#### <a name="remarks"></a>備考

オプションの COM パラメーターには、値を持たない COMVariant オブジェクトを使用できます。

#### <a name="examples"></a>例

次の例では、空の COMVariant オブジェクトを作成します。

    COMVariant noValue; 

    noValue = COMVariant::createNoValue(); 
    info(noValue.toString());

### <a name="method-new"></a>メソッド new

COM オートメーション オブジェクトのメソッドまたはプロパティに引数を渡すために使用できる COMVariant オブジェクトを作成します。

    public void new([COMVariantInOut inOutFlag], [COMVariantType type])

#### <a name="parameters"></a>パラメーター

inOutFlag  
格納するデータのタイプ、オプション。 これらは、COMVariantType システム列挙型によって提供される可能性のある値です。

<!-- -->

タイプ  
格納するデータのタイプ、オプション。 これらは、COMVariantType システム列挙型によって提供される可能性のある値です。

#### <a name="remarks"></a>備考

型パラメーターが省略されると、COMVariant オブジェクトのプロパティのいずれかによって必要とされるまで、内部メモリは割り当てられません。 プロパティ メソッドの一覧については、\[COMVariant クラス\] を参照してください。 異なるタイプの新しい値を指定することにより (いずれかのプロパティ メソッドを使用して)、バリアント データ型を設定後に変更することができます。 COMVariantType 列挙によって定義されるデータ型は、Win32 SDK によって定義されるバリアントデータ型と同じです。

#### <a name="examples"></a>例

次の例では、3 つの COMVariant オブジェクトを作成します。

-   varIn は COM メソッドにデータを渡すためのものです。内部には文字列および短整数が格納されています。
-   varOut は VT\_I4 (long) タイプのデータを受け取るためのものです。
-   varOutRetval はデータをパスまたは受け取ることができます。そのデータ タイプは COMDispFunction.call メソッドでセットすることができます。

<!-- -->

    { 
        COMVariant varIn  = new COMVariant(); 
        COMVariant varOut = new COMVariant( 
            COMVariantInOut::OUT,  
            COMVariantType::VT_I4); 
        COMVariant varOutRetval = new COMVariant( 
            COMVariantInOut::OUT_RETVAL); ; 

        // Store a text string in the varIn object 
        varIn.bStr("Hello World"); 

        // Change varIn to a short. 
        // Text string stored in varIn is automatically released 
        varIn.short(123);  
    }

### <a name="method-novalue"></a>メソッド noValue

既存の COMVariant オブジェクトの内容を削除し、COMDispFunction.call メソッドまたは COM クラスで使用されている場合は、未指定の引数として機能させることができます。

    public void noValue()

#### <a name="remarks"></a>備考

値を持たないバリアントは、null にできるパラメーターが COM メソッドにあるときに使用できます。 引数が指定されていない COM オブジェクトと、独自の既定値を使用する必要がある COM オブジェクトを示します。 COM オブジェクトに対するメソッドを呼び出すときは、COMArgument::NoValue 列挙型を使用して、未指定の引数を指定することもできます。 COMDispFunction クラスを通じて呼び出すときに、この列挙型は使用できないことに注意してください。

#### <a name="examples"></a>例

次の例は、3 番目の引数 unspecified を使用して COM.multiply メソッドを呼び出す方法を示しています。 以下のコードには仮想 COM オブジェクト (「MyCOM.Object」) が含まれており、Finance and Operations の外部でオブジェクトが作成されていない限り、Finance and Operations では実行されません。

    { 
        COM        com; 
        COMVariant varArg1 = new COMVariant(); 
        COMVariant varArg2 = new COMVariant(); 
        COMVariant varArg3 = new COMVariant(); 
        COMVariant varRet  = new COMVariant(COMVariantInOut::OUT_RETVAL); 
        real       ret; 
        InteropPermission perm; 

        // Set code access permission to help protect use of COM object 
        perm = new InteropPermission(InteropKind::ComInterop); 
        if (perm == null) 
        { 
            return; 
        } 

        // Permission scope starts here 
        perm.assert(); 

        com = new COM("MyCOM.Object"); 

        // Specify arguments for the multiply method 
        varArg1.float(123); 
        varArg2.float(456); 
        varArg3.noValue(); 
        varRet = com.multiply(varArg1, varArg2, varArg3); 
        // …or… 
        varRet = com.multiply(varArg1, varArg2, COMArgument::NoValue); 
         ret = varRet.double(); 
        // ret is now 56088 (123*456) 

        // Close code access permission 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-finalize"></a>メソッド finalize

実装されていません。 明示的にオブジェクトを破棄する必要がある場合は、このメソッドをオーバーライドすることができます。

    public void finalize()

#### <a name="remarks"></a>備考

メソッドのすべてのステートメントを実行する確定メソッドを呼び出す必要があります。メソッドを確定する暗黙的な呼び出しはありません。

## <a name="class-configurationkeyset"></a>クラス ConfigurationKeySet
    class ConfigurationKeySet extends Object

ConfigurationKeySet クラスでは、コンフィギュレーション キーのツリーを操作できます。

### <a name="remarks"></a>備考

新しい ConfigurationKeySet が作成されるとき、コンフィギュレーション キーのツリーが作成されます。この場合、すべてのキーは既定では「有効」に設定されます。 cnt メソッドは、すべての設定キーをループしてカウントするために使用されます。 cntID メソッドは、設定キーの ID を取得するために使用されます。 コンフィギュレーション キーが削除され、キー ID が ID1、ID2、ID5 などである場合、このメソッドはそれらの ID と比較してコンフィギュレーション キーの数を区別します。 新しい ConfigurationKeySet が作成されるとき、すべてのコンフィギュレーション キーが有効になります。 システムは loadSystemSetup メソッドを呼び出し、構成タイプが格納されている SysConfig テーブルをスキャンします。 コンフィギュレーション キーの設定をループし、有効になっているものを識別します。 次に、有効なメソッドが呼び出されます。 構成キーが無効になるたびに、すべてのサブ構成キーも自動的に無効になります。 トップ ノードが有効でサブノードの 1 つが無効になっている場合、カーネルはトップ ノードが無効になったときに必ずどのコンフィギュレーション キー サブ ノードが以前に無効にされたかを記録します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                            | 説明                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| public int cnt()                                                                  | Finance and Operations アプリケーション オブジェクト ツリー (AOT) で定義されているコンフィギュレーション キーの数を取得します。 |
| public ConfigurationKeyId cnt2Id(int cnt)                                         | *n* 番目のコンフィギュレーション キーの ID を取得します。                                                                        |
| public boolean enabled(ConfigurationKeyId configurationKeyId, \[boolean enable\]) | オブジェクトを有効または無効にするかどうかを決定します。                                                                     |
| public container pack()                                                           | ConfigurationKeySet クラスの現在のインスタンスをシリアル化します。                                                       |
| public boolean touchedByUser(ConfigurationKeyId configurationKeyId)               |                                                                                                                         |
| public void new(\[container container\])                                          | Object クラスの新しいインスタンスを初期化します。                                                                         |
| public void loadSystemSetup()                                                     |                                                                                                                         |

### <a name="method-cnt"></a>メソッド cnt

Finance and Operations アプリケーション オブジェクト ツリー (AOT) で定義されているコンフィギュレーション キーの数を取得します。

    public int cnt()

#### <a name="return-value"></a>戻り値

AOT で定義されているコンフィギュレーション キーの数。

### <a name="method-cnt2id"></a>メソッド cnt2Id

*n* 番目のコンフィギュレーション キーの ID を取得します。

    public ConfigurationKeyId cnt2Id(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  
コンフィギュレーション キーのインデックス。1 とコンフィギュレーション キーの間でなければなりません。

#### <a name="return-value"></a>戻り値

指定されたコンフィギュレーション キーの ID。

#### <a name="remarks"></a>備考

構成キーの数を調べるには、cnt メソッドを使用します。 一般に、すべての ID が使用されているわけではないため、インデックスおよび ID は異なります。

#### <a name="examples"></a>例

    ConfigurationKeySet configKeySet = new ConfigurationKeySet(); 
    DictConfigurationKey dictConfigurationKey; 
    int i; 

    configKeySet.loadSystemSetup(); 
    for (i=1; i<= configKeySet.cnt(); i++) 
    { 
        setPrefix('Disabled configurationkeys'); 
        if (!configKeySet.enabled( configKeySet.cnt2Id(i) )) 
        { 
            dictConfigurationKey =  
                new DictConfigurationKey(configKeySet.cnt2id(i)); 
            info (dictConfigurationKey.name()); 
        } 
    }

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled(ConfigurationKeyId configurationKeyId, [boolean enable])

#### <a name="parameters"></a>パラメーター

configurationKeyId  
構成キーの状態を設定する値 (オプション)。

<!-- -->

enable  
構成キーの状態を設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

#### <a name="examples"></a>例

この例では、ConfigurationKeySet.enabled メソッドの使用方法を示します。

    static void testConfigKey(Args _args) 
    { 
        ConfigurationKeySet configKey = new ConfigurationKeySet(); 

        configKey.loadSystemSetup(); 

        // Set the enable value to false. 
        configKey.enabled(configurationkeynum(RouteApprove), false); 
        SysDictConfigurationKey::save(configKey.pack()); 
        SysSecurity::reload(true); 
        print isConfigurationkeyEnabled(configurationkeynum(RouteApprove)); 

        // Set the enable value to true. 
        configKey.enabled(configurationkeynum(RouteApprove), true); 
        //Save the configuration key setup. 
        SysDictConfigurationKey::save(configKey.pack()); 
        SysSecurity::reload(true); 

        print isConfigurationkeyEnabled(configurationkeynum(RouteApprove)); 

        pause; 
    }

### <a name="method-pack"></a>メソッド pack

ConfigurationKeySet クラスの現在のインスタンスをシリアル化します。

    public container pack()

#### <a name="return-value"></a>戻り値

ConfigurationKeySet クラスの現在のインスタンスを含むコンテナーです。

### <a name="method-touchedbyuser"></a>メソッド touchedByUser

    public boolean touchedByUser(ConfigurationKeyId configurationKeyId)

#### <a name="parameters"></a>パラメーター

configurationKeyId  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new([container container])

#### <a name="parameters"></a>パラメーター

コンテナー  

### <a name="method-loadsystemsetup"></a>メソッド loadSystemSetup

    public void loadSystemSetup()

## <a name="class-connection"></a>クラス接続
    class Connection extends Object

接続クラスは、SQL ステートメントを実行して結果を返す現在のデータベース セッションを確立します。

### <a name="remarks"></a>備考

次のクラスは Connection クラスを拡張しています。

-   OdbcConnection
-   OciConnection
-   UserConnection

### <a name="examples"></a>例

次の例では、createStatement メソッドはステートメント オブジェクトを初期化します。 Statement.executeQuery メソッドは、SQL ステートメントを実行し、ResultSet オブジェクトに取得したデータを格納します。

    server static void main(Args args) 
    { 
        Connection con = new Connection(); 
        Statement stmt = con.createStatement(); 
        ResultSet r; 
        str sql; 
        SqlStatementExecutePermission perm; 

        sql = strfmt('SELECT VALUE FROM SQLSYSTEMVARIABLES'); 

        // Set code access permission to help protect the use of 
        // Statement.executeUpdate. 
        perm = new SqlStatementExecutePermission(sql); 
        perm.assert(); 

        try 
        { 
            r = stmt.executeQuery(sql); 
            while (r.next()) 
            { 
                print r.getString(1); 
                pause; 
            } 
        } 
        catch (exception::Error) 
        { 
            print "An error occurred in the query."; 
            pause; 
        } 
        // Code access permission scope ends here. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a>メソッド

| 方法                                                                                                           | 説明                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public Statement createStatement(\[ResultSetType resultSetType\], \[ResultSetConcurrency resultSetConcurrency\]) | SQL ステートメントの実行に使用されるステートメント オブジェクトを作成します。                                                                                                                    |
| public int odbcGetInfoInt(int InfoId)                                                                            | ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo Open Database Connectivity (ODBC) 関数へのインターフェイスを提供します。 |
| public int odbcGetInfoLong(int InfoId)                                                                           | ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。                              |
| public str odbcGetInfoStr(int InfoId)                                                                            | ODBC ドライバに関する情報と接続に関連付けられているデータのソースを文字列形式で取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。           |
| public str toString()                                                                                            | 接続オブジェクトを文字列に変換します。                                                                                                                                             |
| public int ttsLevel()                                                                                            | トランザクションを開始するために使用する ttsbegin メソッドの最後の呼び出しの数を返します。                                                                                        |
| public boolean isInTransactionScope()                                                                            |                                                                                                                                                                                         |
| public void finalize()                                                                                           |                                                                                                                                                                                         |
| public void transactionScopeAbort()                                                                              |                                                                                                                                                                                         |
| public void ttsNotifyCommit()                                                                                    | ttscommit メソッドが呼び出されると呼び出されます。                                                                                                                                          |
| public void transactionScopeBegin()                                                                              |                                                                                                                                                                                         |
| public void transactionScopeCommit()                                                                             |                                                                                                                                                                                         |
| public void ttsNotifyBegin()                                                                                     |                                                                                                                                                                                         |
| public void ttsbegin()                                                                                           | トランザクションを開始します。                                                                                                                                                                   |
| public void ttsabort()                                                                                           | トランザクションに関連する変更を破棄し、データベースを元の状態にロールバックします。                                                                              |
| public void new()                                                                                                | Connection クラスの新しいインスタンスを初期化します。                                                                                                                                     |
| public void ttsNotifyAbort()                                                                                     | 例外がスローされると呼び出されます。                                                                                                                                                  |
| public void ttscommit()                                                                                          | トランザクションに関連付けられている変更をデータベースにコミットします。                                                                                                             |

### <a name="method-createstatement"></a>メソッド createStatement

SQL ステートメントの実行に使用されるステートメント オブジェクトを作成します。

    public Statement createStatement([ResultSetType resultSetType], [ResultSetConcurrency resultSetConcurrency])

#### <a name="parameters"></a>パラメーター

resultSetType  
既定で読み取り専用を指定する ResultSetConcurrency 列挙。

<!-- -->

resultSetConcurrency  
既定で読み取り専用を指定する ResultSetConcurrency 列挙。

#### <a name="return-value"></a>戻り値

新しいステートメント オブジェクトであるデータ型の値です。

#### <a name="remarks"></a>備考

createStatement メソッドを使用して SQL ステートメントを作成し、ユーザーがステートメントへの入力を制御できるようにすると、SQL インジェクション脅威の危険性があります。 SQL インジェクションの詳細については、「http://go.microsoft.com/fwlink/?LinkId=114986」を参照してください。 AOT、ビュー、および X++ Select ステートメントでは、SQL ステートメントを実行するための安全な代替手段として、クエリ要素を使用することができます。

### <a name="method-odbcgetinfoint"></a>メソッド odbcGetInfoInt

ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo Open Database Connectivity (ODBC) 関数へのインターフェイスを提供します。

    public int odbcGetInfoInt(int InfoId)

#### <a name="parameters"></a>パラメーター

InfoId  
ODBC 標準に従って要求された情報の ID を指定する整数。

#### <a name="return-value"></a>戻り値

取得される情報の整数値。

#### <a name="examples"></a>例

次の例では、odbcGetInfoInt メソッドは列名の最大の長さの整数値を返します。

    void getConnection() 
    { 
        Connection con; 
        Statement stmt; 
        int info; 

        #define.SQL_MAX_COLUMN_NAME_LEN(30) 
        con = new Connection(); 

        try 
        { 
            info = con.odbcGetInfoInt(#SQL_MAX_COLUMN_NAME_LEN); 

            print info; 
            pause; 
         } 

        catch(exception::Error) 
        { 
            print "An error occurred."; 

        } 

    }

### <a name="method-odbcgetinfolong"></a>メソッド odbcGetInfoLong

ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。

    public int odbcGetInfoLong(int InfoId)

#### <a name="parameters"></a>パラメーター

InfoId  
ODBC 標準による要求された情報の ID を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

取得される情報の整数データ型値です。

#### <a name="remarks"></a>備考

このメソッドは 32 ビット整数を取得し、整数として返します。

#### <a name="examples"></a>例

次の例では、odbcGetInfoLong メソッドは行の最大サイズの整数を返します。

    void getConnection() 
    { 
        Connection con; 
        Statement stmt; 
        int info; 

        #define.SQL_MAX_ROW_SIZE(104) 
        con = new Connection(); 

        try 
        { 
            info = con.odbcGetInfoLong(#SQL_MAX_ROW_SIZE); 

            print info; 
            pause; 
         } 

        catch(exception::Error) 
        { 
            print "An error occurred."; 

        } 

    }

### <a name="method-odbcgetinfostr"></a>メソッド odbcGetInfoStr

ODBC ドライバに関する情報と接続に関連付けられているデータのソースを文字列形式で取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。

    public str odbcGetInfoStr(int InfoId)

#### <a name="parameters"></a>パラメーター

InfoId  
ODBC 標準による要求された情報の ID を指定する整数データ型です。

#### <a name="return-value"></a>戻り値

取得される情報の文字列データ型値。

#### <a name="examples"></a>例

次の例では、odbcGetInfoStr メソッドはデータベース管理システムの名前を返します。

    void getConnection() 
    { 
        Connection con; 
        str info; 

        #define.SQL_DBMS_NAME(17) 
        con = new Connection(); 

        try 
        { 
            info = con.odbcGetInfoStr(#SQL_DBMS_NAME); 

            print info; 
            pause; 
         } 

        catch(exception::Error) 
        { 
            print "An error occurred."; 
        } 
    }

### <a name="method-tostring"></a>メソッド toString

接続オブジェクトを文字列に変換します。

    public str toString()

#### <a name="return-value"></a>戻り値

接続オブジェクトの文字列値。

### <a name="method-ttslevel"></a>メソッド ttsLevel

トランザクションを開始するために使用する ttsbegin メソッドの最後の呼び出しの数を返します。

    public int ttsLevel()

#### <a name="return-value"></a>戻り値

ttsbegin メソッドに最後の呼び出しの番号を示す整数値。 たとえば、ttsLevel メソッドが ttsbegin メソッドへの 3 回目の呼び出し後に呼び出されると、戻り値は 3 になります。

### <a name="method-isintransactionscope"></a>メソッド isInTransactionScope

    public boolean isInTransactionScope()

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-transactionscopeabort"></a>メソッド transactionScopeAbort

    public void transactionScopeAbort()

### <a name="method-ttsnotifycommit"></a>メソッド ttsNotifyCommit

ttscommit メソッドが呼び出されると呼び出されます。

    public void ttsNotifyCommit()

### <a name="method-transactionscopebegin"></a>メソッド transactionScopeBegin

    public void transactionScopeBegin()

### <a name="method-transactionscopecommit"></a>メソッド transactionScopeCommit

    public void transactionScopeCommit()

### <a name="method-ttsnotifybegin"></a>メソッド ttsNotifyBegin

    public void ttsNotifyBegin()

### <a name="method-ttsbegin"></a>メソッド ttsbegin

トランザクションを開始します。

    public void ttsbegin()

### <a name="method-ttsabort"></a>メソッド ttsabort

トランザクションに関連する変更を破棄し、データベースを元の状態にロールバックします。

    public void ttsabort()

### <a name="method-new"></a>メソッド new

Connection クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-ttsnotifyabort"></a>メソッド ttsNotifyAbort

例外がスローされると呼び出されます。

    public void ttsNotifyAbort()

### <a name="method-ttscommit"></a>メソッド ttscommit

トランザクションに関連付けられている変更をデータベースにコミットします。

    public void ttscommit()

## <a name="class-containerclass"></a>クラス ContainerClass
    class ContainerClass extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                              | 説明                                          |
|---------------------------------------------------------------------|------------------------------------------------------|
| public int length()                                                 |                                                      |
| public container toBlob()                                           |                                                      |
| public str toString()                                               | 現在のオブジェクトを表す文字列を返します。 |
| public container value()                                            |                                                      |
| ::public static container blob2Container(container blob\_container) |                                                      |
| ::public static int containerLength(container container)            |                                                      |
| public void new(container container)                                | Object クラスの新しいインスタンスを初期化します。      |

### <a name="method-length"></a>メソッド length

    public int length()

#### <a name="return-value"></a>戻り値

### <a name="method-toblob"></a>メソッド toBlob

    public container toBlob()

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

### <a name="method-blob2container"></a>メソッド blob2Container

    public static container blob2Container(container blob_container)

#### <a name="parameters"></a>パラメーター

blob\_container  

#### <a name="return-value"></a>戻り値

### <a name="method-containerlength"></a>メソッド containerLength

    public static int containerLength(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  

## <a name="class-controlfiltervalue"></a>クラス ControlFilterValue
    class ControlFilterValue extends FilterValue

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                | 説明                                     |
|-------------------------------------------------------|-------------------------------------------------|
| public FormControl control()                          |                                                 |
| public void new(FormControl control, str filterValue) | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-control"></a>メソッド control

    public FormControl control()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(FormControl control, str filterValue)

#### <a name="parameters"></a>パラメーター

control  

<!-- -->

filterValue  

## <a name="class-controlnode"></a>クラス ControlNode
    class ControlNode extends TreeNode

ControlNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                         | 説明                                       |
|------------------------------------------------|---------------------------------------------------|
| public void new(str name, \[TreeNode parent\]) | TreeNode クラスの新しいインスタンスを初期化します。 |

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str name, [TreeNode parent])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

parent  

## <a name="class-cryptoapi"></a>クラス CryptoAPI
    class CryptoAPI extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                   | 説明                                     |
|------------------------------------------|-------------------------------------------------|
| public container decrypt(container blob) |                                                 |
| public container encrypt(container blob) |                                                 |
| public container getKey()                |                                                 |
| public Int64 salt()                      |                                                 |
| public void new(Int64 salt)              | Object クラスの新しいインスタンスを初期化します。 |
| ::public static void resetKey()          |                                                 |

### <a name="method-decrypt"></a>メソッド decrypt

    public container decrypt(container blob)

#### <a name="parameters"></a>パラメーター

blob  

#### <a name="return-value"></a>戻り値

### <a name="method-encrypt"></a>メソッド encrypt

    public container encrypt(container blob)

#### <a name="parameters"></a>パラメーター

blob  

#### <a name="return-value"></a>戻り値

### <a name="method-getkey"></a>メソッド getKey

    public container getKey()

#### <a name="return-value"></a>戻り値

### <a name="method-salt"></a>メソッド salt

    public Int64 salt()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(Int64 salt)

#### <a name="parameters"></a>パラメーター

salt  

### <a name="method-resetkey"></a>メソッド resetKey

    public static void resetKey()

## <a name="class-cue"></a>クラス キュー
    class Cue extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                         | 説明                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])            | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])        | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])          | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])            | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])       | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])         |                                                                                                                                           |
| public int cueMax(\[int value\])               |                                                                                                                                           |
| public str dataField(\[str value\])            |                                                                                                                                           |
| public str label(\[str value\])                | コントロールのラベルを取得または設定します。                                                                                                     |
| public str LabelId()                           |                                                                                                                                           |
| public str menuItemName(\[str value\])         |                                                                                                                                           |
| public str name(\[str value\])                 | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])             |                                                                                                                                           |
| public str previewPartReference(\[str value\]) |                                                                                                                                           |
| public boolean showAlert(\[boolean value\])    |                                                                                                                                           |
| public int showAlertValue(\[int value\])       |                                                                                                                                           |
| public int showAlertWhen(\[int value\])        |                                                                                                                                           |
| public boolean showSum(\[boolean value\])      |                                                                                                                                           |
| public str table(\[str value\])                | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                                     |
| public void new(str cueName)                   | TreeNode クラスの新しいインスタンスを初期化します。                                                                                         |

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

### <a name="method-cuemax"></a>メソッド cueMax

    public int cueMax([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public str dataField([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelid"></a>メソッド LabelId

    public str LabelId()

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

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
-   テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-previewpartreference"></a>メソッド previewPartReference

    public str previewPartReference([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showalert"></a>メソッド showAlert

    public boolean showAlert([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showalertvalue"></a>メソッド showAlertValue

    public int showAlertValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showalertwhen"></a>メソッド showAlertWhen

    public int showAlertWhen([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showsum"></a>メソッド showSum

    public boolean showSum([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

    public str table([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに関連付けられたテーブル ID の現在の値。

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str cueName)

#### <a name="parameters"></a>パラメーター

cueName  

## <a name="class-cuegroup"></a>クラス CueGroup
    class CueGroup extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                   | 説明                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])      | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                    |
| public Date changedDate(\[Date value\])  | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                                 |
| public str changedTime(\[str value\])    | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                                 |
| public str createdBy(\[str value\])      | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                         |
| public Date creationDate(\[Date value\]) | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                      |
| public str creationTime(\[str value\])   |                                                                                                                                               |
| public str label(\[str value\])          | コントロールのラベルを取得または設定します。                                                                                                         |
| public str LabelId()                     |                                                                                                                                               |
| public str name(\[str value\])           | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])       |                                                                                                                                               |
| public void new(str cueGroupName)        | TreeNode クラスの新しいインスタンスを初期化します。                                                                                             |

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

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelid"></a>メソッド LabelId

    public str LabelId()

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
-   テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str cueGroupName)

#### <a name="parameters"></a>パラメーター

cueGroupName  

## <a name="class-cuereference"></a>クラス CueReference
    class CueReference extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                | 説明                                                                                                                       |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| public str cue(\[str value\])         |                                                                                                                                   |
| public str name(\[str value\])        | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public void new(str cueReferenceName) | TreeNode クラスの新しいインスタンスを初期化します。                                                                                 |

### <a name="method-cue"></a>メソッド cue

    public str cue([str value])

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
-   句読点やスペースを含めないでください。
-   テーブルは、拡張データ型、基本列挙型、クラス、他のパブリックオブジェクトなど、他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str cueReferenceName)

#### <a name="parameters"></a>パラメーター

cueReferenceName  
このフォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前。






