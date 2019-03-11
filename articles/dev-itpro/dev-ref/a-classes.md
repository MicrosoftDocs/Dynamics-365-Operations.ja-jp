---
title: A クラス
description: 文字 A で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 47561
ms.assetid: 03d9d906-d683-47b4-8488-795173db2125
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9efb519a03ca5604db541f042dd7ddc1c2b87ef6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368796"
---
# <a name="a-classes"></a>A クラス

[!include [banner](../includes/banner.md)]

文字 A で始まるシステム API クラス。

<a name="class-absolutefieldbinding"></a>クラス AbsoluteFieldBinding
--------------------------

    class AbsoluteFieldBinding extends FieldBinding

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法                                                                            | 説明                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------|
| ::public static AbsoluteFieldBinding construct(str fieldName, str tableName)      |                                                               |
| ::public static AbsoluteFieldBinding create(container packedAbsoluteFieldBinding) |                                                               |
| private void new()                                                                | AbsoluteFieldBinding クラスの新しいインスタンスを初期化します。 |

### <a name="method-construct"></a>メソッド construct

    public static AbsoluteFieldBinding construct(str fieldName, str tableName)

#### <a name="parameters"></a>パラメーター

fieldName  

<!-- -->

tableName  

#### <a name="return-value"></a>戻り値

### <a name="method-create"></a>メソッド create

    public static AbsoluteFieldBinding create(container packedAbsoluteFieldBinding)

#### <a name="parameters"></a>パラメーター

packedAbsoluteFieldBinding  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

AbsoluteFieldBinding クラスの新しいインスタンスを初期化します。

    private void new()

## <a name="class-adobject"></a>クラス AdObject
    class AdObject extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                             | 説明                                     |
|------------------------------------|-------------------------------------------------|
| public boolean found()             |                                                 |
| public str getValue(str attribute) |                                                 |
| public void new(str osUserName)    | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-found"></a>メソッド found

    public boolean found()

#### <a name="return-value"></a>戻り値

### <a name="method-getvalue"></a>メソッド getValue

    public str getValue(str attribute)

#### <a name="parameters"></a>パラメーター

属性  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(str osUserName)

#### <a name="parameters"></a>パラメーター

osUserName  

## <a name="class-allowencryptionkeyretrievalpermission"></a>クラス AllowEncryptionKeyRetrievalPermission
    class AllowEncryptionKeyRetrievalPermission extends CodeAccessPermission

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | アクセス許可クラス オブジェクトのコピーを作成し、返します。                                                                  |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。 |
| public void new()                                      | AllowEncryptionKeyRetrievalPermission クラスの新しいインスタンスを初期化します。                                            |

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

AllowEncryptionKeyRetrievalPermission クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-aosloadgen"></a>クラス AOSLoadGen
    class AOSLoadGen extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                  |
|------------------------------------------------------------|----------------------------------------------|
| public boolean spawnClass(ClassId classId, str parm)       |                                              |
| public boolean spawnJob(UtilElementName jobName, str parm) |                                              |
| public void new(\[UserId user\], \[ClassId infoClass\])    | AOSLoadGen クラスのインスタンスを作成します。 |

### <a name="method-spawnclass"></a>メソッド spawnClass

    public boolean spawnClass(ClassId classId, str parm)

#### <a name="parameters"></a>パラメーター

classId  

<!-- -->

parm  

#### <a name="return-value"></a>戻り値

### <a name="method-spawnjob"></a>メソッド spawnJob

    public boolean spawnJob(UtilElementName jobName, str parm)

#### <a name="parameters"></a>パラメーター

jobName  

<!-- -->

parm  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

AOSLoadGen クラスのインスタンスを作成します。

    public void new([UserId user], [ClassId infoClass])

#### <a name="parameters"></a>パラメーター

ユーザー  
AOSLoadGen クラスのインスタンスを作成するために使用される情報クラス。 既定値は情報です。

<!-- -->

infoClass  
AOSLoadGen クラスのインスタンスを作成するために使用される情報クラス。 既定値は情報です。

#### <a name="remarks"></a>備考

新しいメソッドへの入力を制御することは、セキュリティ上のリスクとなる可能性があります。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

## <a name="class-aossessioninfo"></a>クラス AOSSessionInfo
    class AOSSessionInfo extends Object

AOSSessionInfo クラスは、Finance and Operations Application Object Server (AOS) のセッションに関する情報を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                             | 説明                                                               |
|------------------------------------|---------------------------------------------------------------------------|
| public AOSClientMode clientMode()  | AOS セッションのクライアント モードを返します。                              |
| public int cpuTime()               | CPU が AOS セッションに使用するミリ秒数を返します。 |
| public int idleTicks()             | AOS との最後の通信以降のミリ秒数を返します。 |
| public int sessionId()             | AOS セッションの ID を返します。                                        |
| public void new(\[int sessionId\]) | AOSSessionInfo クラスのインスタンスを作成します。                          |

### <a name="method-clientmode"></a>メソッド clientMode

AOS セッションのクライアント モードを返します。

    public AOSClientMode clientMode()

#### <a name="return-value"></a>戻り値

AOS セッションのクライアント モード。

### <a name="method-cputime"></a>メソッド cpuTime

CPU が AOS セッションに使用するミリ秒数を返します。

    public int cpuTime()

#### <a name="return-value"></a>戻り値

CPU が AOS セッションに使用するミリ秒数。

### <a name="method-idleticks"></a>メソッド idleTicks

AOS との最後の通信以降のミリ秒数を返します。

    public int idleTicks()

#### <a name="return-value"></a>戻り値

AOS との最後の通信以降のミリ秒数。

### <a name="method-sessionid"></a>メソッド sessionId

AOS セッションの ID を返します。

    public int sessionId()

#### <a name="return-value"></a>戻り値

AOS セッションの ID。

### <a name="method-new"></a>メソッド new

AOSSessionInfo クラスのインスタンスを作成します。

    public void new([int sessionId])

#### <a name="parameters"></a>パラメーター

sessionId  
AOSSessionInfo クラスのインスタンスを作成するために使用されるセッション ID。 セッション ID が指定されていない場合、現在のセッションが使用されます; 省略。

## <a name="class-aottablefieldlist"></a>クラス AOTTableFieldList
    class AOTTableFieldList extends TreeNode

AOTTableFieldList クラスは、テーブルのフィールド ノードを表し、フィールドをテーブルに追加するためにも使用されます。

### <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 開発者は、他の方法を使用してノードに関する一般的な情報を取得できます。

### <a name="examples"></a>例

次の例では、列挙型のフィールドを TutorialJournalName テーブルに追加します。

    { 
        AOTTableFieldList tfl = infolog.findNode( 
            '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 

         if (!tfl.AOTFindChild('NewEnum')) 
         { 
             tfl.addEnum('NewEnum');  // Adds the field NewEnum. 
         } 
    }

### <a name="methods"></a>メソッド

| 方法                             | 説明                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| public void addInteger(str name)   | 現在のテーブルのフィールドのリストに整数型の新しいフィールドを追加します。   |
| public void addGuid(str name)      |                                                                                     |
| public void addContainer(str name) | 現在のテーブルのフィールドのリストにコンテナー型の新しいフィールドを追加します。 |
| public void addInt64(str name)     |                                                                                     |
| public void addDateTime(str name)  |                                                                                     |
| public void addDate(str name)      | 現在のテーブルのフィールドのリストに日付型の新しいフィールドを追加します。      |
| public void addString(str name)    | 現在のテーブルのフィールドのリストに文字列型の新しいフィールドを追加します。    |
| public void addReal(str name)      | 現在のテーブルのフィールドのリストに実数型の新しいフィールドを追加します。      |
| public void addTime(str name)      | 現在のテーブルのフィールドのリストに時刻タイプの新しいフィールドを追加します。      |
| public void addEnum(str name)      | 現在のテーブルのフィールドのリストに列挙型の新しいフィールドを追加します。      |

### <a name="method-addinteger"></a>メソッド addInteger

現在のテーブルのフィールドのリストに整数型の新しいフィールドを追加します。

    public void addInteger(str name)

#### <a name="parameters"></a>パラメーター

名前  
追加するフィールドの名前。

#### <a name="remarks"></a>備考

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

#### <a name="examples"></a>例

次のコード例は、整数型である、NewInteger フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewInteger')) 
    { 
        tfl.addInteger('NewInteger'); 
    }

### <a name="method-addguid"></a>メソッド addGuid

    public void addGuid(str name)

#### <a name="parameters"></a>パラメーター

名前  

### <a name="method-addcontainer"></a>メソッド addContainer

現在のテーブルのフィールドのリストにコンテナー型の新しいフィールドを追加します。

    public void addContainer(str name)

#### <a name="parameters"></a>パラメーター

名前  
追加するフィールドの名前。

#### <a name="remarks"></a>備考

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

#### <a name="examples"></a>例

次のコード例は、NewContainer フィールドと NewContainer1 フィールド (両方ともコンテナー タイプ) を TutorialJournalName テーブルのフィールドのリストに追加します。

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 

    // Add a NewContainer field. 
    tfl.addContainer('NewContainer'); 

    // Add a NewContainer1 field. 
    tfl.addContainer('NewContainer');

### <a name="method-addint64"></a>メソッド addInt64

    public void addInt64(str name)

#### <a name="parameters"></a>パラメーター

名前  

### <a name="method-adddatetime"></a>メソッド addDateTime

    public void addDateTime(str name)

#### <a name="parameters"></a>パラメーター

名前  

### <a name="method-adddate"></a>メソッド addDate

現在のテーブルのフィールドのリストに日付型の新しいフィールドを追加します。

    public void addDate(str name)

#### <a name="parameters"></a>パラメーター

名前  
追加するフィールドの名前。

#### <a name="remarks"></a>備考

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

#### <a name="examples"></a>例

次のコード例は、日付タイプである、NewDate フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewDate')) 
    { 
        tfl.addDate('NewDate'); 
    }

### <a name="method-addstring"></a>メソッド addString

現在のテーブルのフィールドのリストに文字列型の新しいフィールドを追加します。

    public void addString(str name)

#### <a name="parameters"></a>パラメーター

名前  
追加するフィールドの名前。

#### <a name="remarks"></a>備考

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

#### <a name="examples"></a>例

次の例では、文字列型の NewString フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

    { 
        AOTTableFieldList tfl = infolog.findNode( 
            '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
        if (!tfl.AOTFindChild('NewString')) 
        { 
            tfl.addString('NewString'); 
        } 
    }

### <a name="method-addreal"></a>メソッド addReal

現在のテーブルのフィールドのリストに実数型の新しいフィールドを追加します。

    public void addReal(str name)

#### <a name="parameters"></a>パラメーター

名前  
追加するフィールドの名前。

#### <a name="remarks"></a>備考

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

#### <a name="examples"></a>例

次の例では、実際の型の NewReal フィールドと NewReal1 フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    // Add the field NewReal. 
    tfl.addReal('NewReal'); 
    // Add the field NewReal1. 
    tfl.addReal('NewReal');

### <a name="method-addtime"></a>メソッド addTime

現在のテーブルのフィールドのリストに時刻タイプの新しいフィールドを追加します。

    public void addTime(str name)

#### <a name="parameters"></a>パラメーター

名前  
追加するフィールドの名前。

#### <a name="remarks"></a>備考

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

#### <a name="examples"></a>例

次のコード例は、時間タイプである、NewTime フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewTime')) 
    { 
        tfl.addTime('NewTime'); 
    }

### <a name="method-addenum"></a>メソッド addEnum

現在のテーブルのフィールドのリストに列挙型の新しいフィールドを追加します。

    public void addEnum(str name)

#### <a name="parameters"></a>パラメーター

名前  
追加するフィールドの名前。

#### <a name="remarks"></a>備考

指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。 名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。 AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。

#### <a name="examples"></a>例

次の例では、列挙型の NewEnum フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。

    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewEnum')) 
    { 
        tfl.addEnum('NewEnum');  // adds the field NewEnum 
    }

## <a name="class-applicationobjecttreewindow"></a>クラス ApplicationObjectTreeWindow
    class ApplicationObjectTreeWindow extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                  | 説明                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| public str getSelectedNodeModelName()   |                                                                      |
| public Set getSelectedNodes()           |                                                                      |
| public Set getSelectedNodesPaths()      |                                                                      |
| public boolean isSelectedNodeExpanded() |                                                                      |
| private void new()                      | ApplicationObjectTreeWindow クラスの新しいインスタンスを初期化します。 |

### <a name="method-getselectednodemodelname"></a>メソッド getSelectedNodeModelName

    public str getSelectedNodeModelName()

#### <a name="return-value"></a>戻り値

### <a name="method-getselectednodes"></a>メソッド getSelectedNodes

    public Set getSelectedNodes()

#### <a name="return-value"></a>戻り値

### <a name="method-getselectednodespaths"></a>メソッド getSelectedNodesPaths

    public Set getSelectedNodesPaths()

#### <a name="return-value"></a>戻り値

### <a name="method-isselectednodeexpanded"></a>メソッド isSelectedNodeExpanded

    public boolean isSelectedNodeExpanded()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

ApplicationObjectTreeWindow クラスの新しいインスタンスを初期化します。

    private void new()

## <a name="class-array"></a>クラス配列
    class Array extends Object

### <a name="remarks"></a>備考

配列では、オブジェクトやレコードなど単一タイプの値を保持できます (X++ 言語に組み込まれている配列のデータ タイプとは異なります) 。 このタイプのオブジェクトは、関数やメソッドに転送することができます。 値は、順番に格納されます。 配列は、必要に応じて展開されます。 したがって、配列の特定の分析コードは提供されません。

### <a name="examples"></a>例

次の例では、クラスの配列を作成し、3 つのクエリ オブジェクトを配列に追加します。

    { 
        Array oarray = new Array (Types::Class); 

        oarray.value(1, new query()); 
        oarray.value(2, new query()); 
        oarray.value(4, new query());  
        print oarray.toString(); 
        print oarray.definitionString(); 
        pause; 
    }

### <a name="methods"></a>メソッド

| 方法                                              | 説明                                                                                         |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| public str definitionString()                       | 配列の定義を含む文字列を返します。                                         |
| public boolean exists(int index)                    | 特定の配列要素が有効かどうかを判定します。                                             |
| public int lastIndex()                              | 配列に値を格納するために使用する最上位のインデックスを取得します。                             |
| public container pack()                             | Array クラスの現在のインスタンスをシリアル化します。                                                 |
| public str toString()                               | 配列の内容を説明する文字列を返します。                                          |
| public Types typeId()                               | 配列の値のデータ型を返します。                                                   |
| public AnyType value(int index, \[AnyType arg\])    | 指定したインデックスに格納される配列要素の値を取得または設定します。                  |
| public str xml(\[int indent\])                      | 現在のオブジェクトを表す XML 文字列を返します。                                           |
| ::public static Array create(container container)   | 以前の Array.pack メソッドの呼び出しで取得されるコンテナーから配列を作成します。 |
| ::public static Array createFromXML(Object xmlnode) |                                                                                                     |
| public void new(Types Type)                         | 各要素が指定されたタイプを持つ配列を作成します。                                      |

### <a name="method-definitionstring"></a>メソッド definitionString

配列の定義を含む文字列を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

配列の定義を含む文字列。

#### <a name="examples"></a>例

次の例では、クラスの配列を作成し、3 つのクエリ オブジェクトを配列に追加します。 definitionString メソッドを使用して、配列の定義を出力します。

    { 
        Array oarray = new Array (Types::Class); 

        oarray.value(1, new query()); 
        oarray.value(2, new query()); 
        oarray.value(4, new query());  
        print oarray.definitionString(); 
        pause; 
    }

### <a name="method-exists"></a>メソッド exists

特定の配列要素が有効かどうかを判定します。

    public boolean exists(int index)

#### <a name="parameters"></a>パラメーター

指数  
テスト対象の配列要素。

#### <a name="return-value"></a>戻り値

インデックスにより指定される配列要素が有効な場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例では、exists メソッドを使用して、配列内のさまざまな要素が有効かどうかをテストします。

    { 
        array a = new array(types::Integer); 

        a.value(1, 23); 

        print a.value(1); 
        pause; 
        if (a.exists(7)) // No, only element 1 is initialized 
        { 
            print a.value(7); 

        } 
        else  
        { 
            print "Value does not exist"; 
        } 
        pause; 

        //Array positions 2 to 9 padded with default values 
        a.value(10, 55); 

        if (a.exists(7)) // Yes, elements 1..10 now initialized 
        { 
            print a.value(7); 
        } 
        else  
        { 
            print "Value does not exist"; 
        } 
        pause; 
    }

### <a name="method-lastindex"></a>メソッド lastIndex

配列に値を格納するために使用する最上位のインデックスを取得します。

    public int lastIndex()

#### <a name="return-value"></a>戻り値

値を格納するために使用する最上位のインデックスを表す整数。

#### <a name="examples"></a>例

次の例では、lastIndex メソッドを使用して配列の最後の要素を見つけ、この要素の後に新しい値を追加します。

    { 
        Array myArray = new Array(Types::Integer); 
        int newValue; 

        // Other code - values are added to myArray 
        // and a value is assigned to newValue 

        myArray.value(myArray.lastIndex()+1, newValue); 
    }

### <a name="method-pack"></a>メソッド pack

Array クラスの現在のインスタンスをシリアル化します。

    public container pack()

#### <a name="return-value"></a>戻り値

Array クラスの現在のインスタンスを含むコンテナーです。

#### <a name="remarks"></a>備考

このメソッドで作成されたコンテナーには、配列の最初の要素の前に 3 つの要素が含まれます。

-   コンテナのバージョン番号。
-   配列要素のデータ型を識別する整数。
-   この配列の要素の数。

配列の値がオブジェクトになっている場合は、各オブジェクトに対して pack メソッドが呼び出され、サブコンテナーを取得します。

#### <a name="examples"></a>例

次の例では、整数の配列を作成し、それにいくつかの値を追加します。 pack メソッドを使用して配列をコンテナーにパックし、コンテナーを使用して新しい配列を作成します。

    { 
        int i; 
        container packedArray; 
        // Create an integer array 
        Array ia = new Array (Types::Integer); 
        Array iacopy; 

        // Write some elements in it 
        for (i = 1; i< 10; i++) 
        { 
            ia.value(i, i*2); 
        } 

        // Pack the array 
        packedArray = ia.pack(); 

        // Unpack the array  
        iacopy = Array::create(packedArray); 

        // Check the values 
        for (i = 1; i< 10; i++) 
        { 
            if (iacopy.value(i) != 2*i) 
            { 
                print "Error!"; 
            } 
        } 
        pause; 
    }

### <a name="method-tostring"></a>メソッド toString

配列の内容を説明する文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

配列の内容を説明する文字列。

#### <a name="examples"></a>例

次の例では、整数の配列を作成し、それにいくつかの値を追加します。 toString メソッドは、配列が保持する値を出力するために使用されます。

    { 
        Array     myArray; 

        Set set1 = new Set(Types::Integer); 
        Set set2 = new Set(Types::Integer); 
        int i; 


        myArray = new Array(Types::Integer); 

        // Add some values to the array. 
        for (i = 1; i< 10; i++) 
        { 
            myArray.value(i, i*2); 
        } 

        // Print out the values in the array. 
        print myArray.toString(); 
        pause; 
    }

### <a name="method-typeid"></a>メソッド typeId

配列の値のデータ型を返します。

    public Types typeId()

#### <a name="return-value"></a>戻り値

配列の要素のデータ型。

#### <a name="remarks"></a>備考

タイプは配列の寿命を通して同じままです。 タイプは、配列の作成時に指定されます。

#### <a name="examples"></a>例

次の例では、特定の配列要素が存在するかどうかをテストします。 存在しない場合、配列に追加する必要がある新しい値のタイプを指定するために typeId メソッドが使用されます。

    public anytype getArrayValue(Array a, int _index) 
    { 
        if (! a.exists(_index)) 
        { 
            a.value(_index,nullValueFromType(a.typeId())); 
        } 

        return a.value(_index); 
    }

### <a name="method-value"></a>メソッド value

指定したインデックスに格納される配列要素の値を取得または設定します。

    public AnyType value(int index, [AnyType arg])

#### <a name="parameters"></a>パラメーター

指数  
指定されたオフセットで配列要素に割り当てる値 (オプション)。

<!-- -->

arg  
指定されたオフセットで配列要素に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

指定したオフセットに格納されている値。

#### <a name="remarks"></a>備考

戻り値のタイプは、配列のタイプと同じです。 値を持つ最後のインデックスを超えるインデックスで値を読み取ろうとすると、例外がスローされます。 値が実在しない位置に書き込まれる場合、前の要素とその実在しない位置との間にあるすべての位置に既定値が入力され、配列が展開されます。

#### <a name="examples"></a>例

次の例では、整数の配列を作成し、value メソッドを使用して値を配列に追加します。 値のメソッドを使用して配列内で格納されている値を取得し、それらをテストします。

    { 
         int i; 
        // Create an integer array 
        Array ia = new Array (Types::Integer); 

        // Write some elements in it 
        for (i = 1; i< 10; i++) 
        { 
            ia.value(i, i*2); 
        } 

        // Check the values 
        for (i = 1; i< 10; i++) 
        { 
            if (ia.value(i) != 2*i) 
            { 
                print "Error!"; 
            } 
        } 
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

このメソッドをオーバーライドして、特定の型に対して意味のある値を返すことができます。

### <a name="method-create"></a>メソッド create

以前の Array.pack メソッドの呼び出しで取得されるコンテナーから配列を作成します。

    public static Array create(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  
Array.pack メソッドを使用して作成されるコンテナーです。 コンテナーを展開して配列を作成します。

#### <a name="return-value"></a>戻り値

指定したコンテナーの内容を保持する配列です。

#### <a name="remarks"></a>備考

配列の値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出される Array.unpack メソッドが必要です。

#### <a name="examples"></a>例

次の例では、配列を作成し、2 つのセットを追加します。 配列がパックされ、それを使用して、新しい配列が作成されます。

    { 
        Array     myArray; 
        Array     newArray; 
        container packedArray; 

        Set set1 = new Set(Types::Integer); 
        Set set2 = new Set(Types::Integer); 
        int i; 
        int j; 

        myArray = new Array(Types::Class); 

        // Add some values to the set1 and set2 
        for (i = 0; i < 10; i++) 
        { 
            set1.add(i); 
            j = i+3; 
            set2.add(j); 
        } 

        // Add set1 and set2 to myArray 
        myArray.value(1, set1); 
        myArray.value(2, set2); 

        // Pack the myArray into a container 
        packedArray = myArray.pack(); 

        // Create a new array from the container 
        if(packedArray != connull()) 
        { 
            newArray = Array::create(packedArray); 
        } 

        // Test that newArray has same contents as myArray 
        print newArray.definitionString(); 
        print newArray.toString(); 
        pause; 
    }

### <a name="method-createfromxml"></a>メソッド createFromXML

    public static Array createFromXML(Object xmlnode)

#### <a name="parameters"></a>パラメーター

xmlnode  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

各要素が指定されたタイプを持つ配列を作成します。

    public void new(Types Type)

#### <a name="parameters"></a>パラメーター

種類  
配列要素のデータ型。

#### <a name="remarks"></a>備考

可能な値は、Types システム列挙に使用可能な値です。

-   AnyType
-   BLOB
-   クラス
-   コンテナー
-   日
-   日時
-   列挙
-   Guid
-   Int64
-   整数

#### <a name="examples"></a>例

次の例では、整数の配列を作成します。

    Array intArray = new Array(Types::Integer);

## <a name="class-asciiio"></a>クラス AsciiIo
    class AsciiIo extends CommaIo

AsciiIo クラスには、ASCII ファイルの読み取りと書き込みを行う機能があります。

### <a name="remarks"></a>備考

TextIo クラスには、さまざまなコード ページを使用するファイルの読み取りと書き込みを行う機能があります。 AsciiIO クラスは、ANSI コード ページ (ACP) 文字のみサポートします。 AsciiIO クラスを使用する既存のコードは、ファイルに ACP 以外の文字が含まれている場合や、.xpo ファイルなどの Finance and Operations でのみ使用されるファイルの場合に TextIO クラスを使用するように変換する必要があります。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                       | 説明                                                                                                                      |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| public str inFieldDelimiter(\[str value\])   | AsciiIO オブジェクトによって表される入力ファイルのフィールド区切り記号として使用される文字を設定または取得します。   |
| public str inRecordDelimiter(\[str value\])  | AsciiIO オブジェクトによって表される入力ファイルのレコード区切り記号として使用される文字を設定または取得します。  |
| public int inRecordLength(\[int value\])     | 入力ファイルのレコードの長さを設定または取得します。                                                                           |
| public str outFieldDelimiter(\[str value\])  | AsciiIO オブジェクトによって表される出力ファイルのフィールド区切り記号として使用される文字を設定または取得します。  |
| public str outRecordDelimiter(\[str value\]) | AsciiIO オブジェクトによって表される出力ファイルのレコード区切り記号として使用される文字を設定または取得します。 |
| public container read()                      | Io オブジェクトから次の完全なレコードを読み取ります。                                                                                   |
| public IO\_Status status()                   | ファイルでの最後の操作のステータスを返します。                                                                            |
| public boolean write(VarArg values)          | 単純型の値を記述します。                                                                                                  |
| public boolean writeChar(int int)            |                                                                                                                                  |
| public boolean writeExp(container data)      | コンテナのコンテンツをファイルに記述します。                                                                                     |
| public boolean writeRaw(str data)            |                                                                                                                                  |
| public void finalize()                       | ファイルを閉じ、ファイル バッファーをディスクにフラッシュします。                                                                       |
| public void new(str filename, str mode)      | AsciiIo クラスのインスタンスを作成します。                                                                                        |

### <a name="method-infielddelimiter"></a>メソッド inFieldDelimiter

AsciiIO オブジェクトによって表される入力ファイルのフィールド区切り記号として使用される文字を設定または取得します。

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  
フィールドの区切り記号として割り当てられる文字。

#### <a name="return-value"></a>戻り値

フィールドの区切り記号として使用される文字。

### <a name="method-inrecorddelimiter"></a>メソッド inRecordDelimiter

AsciiIO オブジェクトによって表される入力ファイルのレコード区切り記号として使用される文字を設定または取得します。

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  
レコードの区切り記号として割り当てられる文字。

#### <a name="return-value"></a>戻り値

レコードの区切り記号として使用される文字。

#### <a name="remarks"></a>備考

標準的なテキストについては、区切り記号は改行文字です。

### <a name="method-inrecordlength"></a>メソッド inRecordLength

入力ファイルのレコードの長さを設定または取得します。

    public int inRecordLength([int value])

#### <a name="parameters"></a>パラメーター

値  
入力ファイルのレコード長として割り当てる値。

#### <a name="return-value"></a>戻り値

入力ファイルのレコードの長さ。

#### <a name="remarks"></a>備考

固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。 レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合 (つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、それ以上のデータは読み込まれません。 固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。 inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。 レコードの長さのチェックを無効にするには、inRecordDelimiter プロパティ値を 0 (ゼロ) に設定します。

### <a name="method-outfielddelimiter"></a>メソッド outFieldDelimiter

AsciiIO オブジェクトによって表される出力ファイルのフィールド区切り記号として使用される文字を設定または取得します。

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  
フィールドの区切り記号として割り当てられる文字。

#### <a name="return-value"></a>戻り値

フィールドの区切り記号として使用される文字。

### <a name="method-outrecorddelimiter"></a>メソッド outRecordDelimiter

AsciiIO オブジェクトによって表される出力ファイルのレコード区切り記号として使用される文字を設定または取得します。

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  
レコードの区切り記号として割り当てられる文字。

#### <a name="return-value"></a>戻り値

レコードの区切り記号として使用される文字。

#### <a name="remarks"></a>備考

標準的なテキスト ファイルについては、区切り記号は改行文字です。

### <a name="method-read"></a>メソッド read

Io オブジェクトから次の完全なレコードを読み取ります。

    public container read()

#### <a name="return-value"></a>戻り値

Io オブジェクトからの次の完全なレコード。

#### <a name="remarks"></a>備考

次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength によって制御されます。 レコードはコンテナーとして返されます。 コンテナー内の各エントリは、レコードの 1 つのフィールドを表します。 それぞれの特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のデフォルト設定があります。 これらの設定では、最も一般的な形式の入力と出力が可能です。 ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。

### <a name="method-status"></a>メソッド status

ファイルでの最後の操作のステータスを返します。

    public IO_Status status()

#### <a name="return-value"></a>戻り値

最後のファイル操作の状態。

### <a name="method-write"></a>メソッド write

単純型の値を記述します。

    public boolean write(VarArg values)

#### <a name="parameters"></a>パラメーター

値  
1 つ以上の値の、各単純型は、フィールドの区切り記号で区切られています。 単純型は、文字列、整数、実数、列挙型、日付です。

#### <a name="return-value"></a>戻り値

書き込み操作が成功する場合は true。それ以外の場合は、false。 書き込み操作が失敗すると、ステータスをチェックし、原因について確認できます。

#### <a name="remarks"></a>備考

このメソッドは、可変数の引数を受け入れます。 指定された各値は、フィールドとして出力レコードに配置されます: 最初のフィールドとしての最初の引数、2 番目のフィールドとしての 2 番目の引数など。 フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。 レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。 完全なコンテナーを書き込むには、writeExp メソッドを使用します。

### <a name="method-writechar"></a>メソッド writeChar

    public boolean writeChar(int int)

#### <a name="parameters"></a>パラメーター

int  

#### <a name="return-value"></a>戻り値

### <a name="method-writeexp"></a>メソッド writeExp

コンテナのコンテンツをファイルに記述します。

    public boolean writeExp(container data)

#### <a name="parameters"></a>パラメーター

データ  
レコードのデータを保持するコンテナー。

#### <a name="return-value"></a>戻り値

操作が成功する場合は true。それ以外の場合は、false。 工程が失敗すると、ステータスをチェックし原因について確認します。

#### <a name="remarks"></a>備考

コンテナー内のエントリはフィールドとして扱われます。 コンテナーは、完全なレコードとして扱われます。 フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。 レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。

### <a name="method-writeraw"></a>メソッド writeRaw

    public boolean writeRaw(str data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、ファイル バッファーをディスクにフラッシュします。

    public void finalize()

#### <a name="remarks"></a>備考

AsciiIo オブジェクトは通常そのスコープの終了後に確定されます。 このメソッドは、通常は直接呼び出されません。 AsciiIo オブジェクトが確定済みになるまで、ファイルに書き込まれる出力は無効です。

### <a name="method-new"></a>メソッド new

AsciiIo クラスのインスタンスを作成します。

    public void new(str filename, str mode)

#### <a name="parameters"></a>パラメーター

filename  
AsciiIo クラスのこのインスタンスを作成するために使用するモード。

<!-- -->

モード  
AsciiIo クラスのこのインスタンスを作成するために使用するモード。

#### <a name="remarks"></a>備考

攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

次の例では、AsciiIo クラスを使用してテキスト ファイルから読み込みます。

    void AsciiIoExample() 
    { 
        AsciiIo asciiIo; 
        container con; 
        FileIoPermission perm; 

        #define.ExampleFile(@"c:\test.txt") 
        #define.ExampleOpenMode("r") 

        // The AsciiIo.new method runs under code access permission. 
        perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
        if (perm == null) 
        { 
            return; 
        } 

        // Code access permission scope starts here. 
         perm.assert(); 

         asciiIo = new AsciiIo(#ExampleFile, #ExampleOpenMode); 
        if (asciiIo != null) 
        { 
              con = asciiIo.read(); 
        } 
        // Closes the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

## <a name="class-assemblydeploymanager"></a>クラス AssemblyDeployManager
    class AssemblyDeployManager extends Object

AssemblyDeployManager クラスを使用すると、.NET 呼び出し時に X++ ランタイムによって使用できる AOS VSAssemblies フォルダーに、AOT Visual Studio プロジェクトに格納されているアセンブリを展開することができます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法                                                        | 説明                                                                                             |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| ::public static boolean isHotswappingEnabled()                | ホット スワップが有効かどうかを示すブール値を返します。                                 |
| ::public static void deployAssemblyFromPath(str assemblyPath) |                                                                                                         |
| ::public static void removeAssemblyFromPath(str assemblyPath) | サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーから削除します。 |
| ::public static void deployAssemblies()                       | サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーに展開します。       |

### <a name="method-ishotswappingenabled"></a>メソッド isHotswappingEnabled

ホット スワップが有効かどうかを示すブール値を返します。

    public static boolean isHotswappingEnabled()

#### <a name="return-value"></a>戻り値

ホット スワップが有効かどうかを示すブール値。

### <a name="method-deployassemblyfrompath"></a>メソッド deployAssemblyFromPath

    public static void deployAssemblyFromPath(str assemblyPath)

#### <a name="parameters"></a>パラメーター

assemblyPath  

### <a name="method-removeassemblyfrompath"></a>メソッド removeAssemblyFromPath

サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーから削除します。

    public static void removeAssemblyFromPath(str assemblyPath)

#### <a name="parameters"></a>パラメーター

assemblyPath  
アセンブリが格納されている Visual Studio プロジェクト パス。

### <a name="method-deployassemblies"></a>メソッド deployAssemblies

サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーに展開します。

    public static void deployAssemblies()

## <a name="class-asynctaskresult"></a>クラス AsyncTaskResult
    class AsyncTaskResult extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                               | 説明 |
|--------------------------------------------------------------------------------------|-------------|
| public container getResult()                                                         |             |
| public System.Exception getException()                                               |             |
| public container getInfologData()                                                    |             |
| public container getAsyncState()                                                     |             |
| ::public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task) |             |

### <a name="method-getresult"></a>メソッド getResult

    public container getResult()

#### <a name="return-value"></a>戻り値

### <a name="method-getexception"></a>メソッド getException

    public System.Exception getException()

#### <a name="return-value"></a>戻り値

### <a name="method-getinfologdata"></a>メソッド getInfologData

    public container getInfologData()

#### <a name="return-value"></a>戻り値

### <a name="method-getasyncstate"></a>メソッド getAsyncState

    public container getAsyncState()

#### <a name="return-value"></a>戻り値

### <a name="method-getasynctaskresult"></a>メソッド getAsyncTaskResult

    public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task)

#### <a name="parameters"></a>パラメーター

タスク  

#### <a name="return-value"></a>戻り値

## <a name="class-axaptacomconnectormonitor"></a>クラス AxaptaCOMConnectorMonitor
    class AxaptaCOMConnectorMonitor extends Object

Microsoft 社内のみで使用。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                     | 説明                                                        |
|--------------------------------------------|--------------------------------------------------------------------|
| public int getBufferCount()                |                                                                    |
| public str getCOMRegistration()            |                                                                    |
| public int getContainerCount()             |                                                                    |
| public int getLoggedOnAxaptaObjectCount()  |                                                                    |
| public int getObjectCount()                |                                                                    |
| public int getRecordCount()                |                                                                    |
| public int getReferenceCount()             |                                                                    |
| public boolean isAxaptaCOMConnector()      |                                                                    |
| public boolean isAxaptaInternetConnector() |                                                                    |
| public void finalize()                     | Microsoft 社内のみで使用。                                        |
| public void new()                          | AxaptaCOMConnectorMonitor クラスの新しいインスタンスを初期化します。 |

### <a name="method-getbuffercount"></a>メソッド getBufferCount

    public int getBufferCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getcomregistration"></a>メソッド getCOMRegistration

    public str getCOMRegistration()

#### <a name="return-value"></a>戻り値

### <a name="method-getcontainercount"></a>メソッド getContainerCount

    public int getContainerCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getloggedonaxaptaobjectcount"></a>メソッド getLoggedOnAxaptaObjectCount

    public int getLoggedOnAxaptaObjectCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getobjectcount"></a>メソッド getObjectCount

    public int getObjectCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecordcount"></a>メソッド getRecordCount

    public int getRecordCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getreferencecount"></a>メソッド getReferenceCount

    public int getReferenceCount()

#### <a name="return-value"></a>戻り値

### <a name="method-isaxaptacomconnector"></a>メソッド isAxaptaCOMConnector

    public boolean isAxaptaCOMConnector()

#### <a name="return-value"></a>戻り値

### <a name="method-isaxaptainternetconnector"></a>メソッド isAxaptaInternetConnector

    public boolean isAxaptaInternetConnector()

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

Microsoft 社内のみで使用。

    public void finalize()

### <a name="method-new"></a>メソッド new

AxaptaCOMConnectorMonitor クラスの新しいインスタンスを初期化します。

    public void new()



