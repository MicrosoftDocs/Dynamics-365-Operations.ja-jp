---
title: "L クラス"
description: "文字 L で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52291
ms.assetid: 60d8c71b-6df4-4776-9642-ed89ab5ad46a
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 0f6ba5193e0c2fb14ce5e28379b5e1d92eb79839
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="l-classes"></a>L クラス

[!include [banner](../includes/banner.md)]

文字 L で始まるシステム API クラス。

<a name="class-label"></a>クラス ラベル
-----------

    class Label extends Object

Label クラスは、ラベル ID およびラベル ファイルを管理します。

### <a name="remarks"></a>備考

SysLabel クラスは、Label クラスを拡張します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                | 説明                                                                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| public LabelBulkEditor bulkEditor(str module)                         | LabelBulkEditor クラスのインスタンスを作成します。                                                   |
| public boolean createLabelFile(str module, str language)              | 指定されたラベル ID のラベル ファイルを作成します。                                                      |
| public boolean delete(str label)                                      | 指定したラベルを削除します。                                                                          |
| public boolean exists(str label)                                      | 指定したラベル ID が存在するかどうかを示します。                                                      |
| public str extractComment(str label)                                  | 指定されたラベル ID に関連付けられているコメントを返します。                                     |
| public str extractString(str label)                                   | 指定されたラベル ID に関連付けられているテキストを返します。                                      |
| public str getFirstLabelFile()                                        | 最初のラベル ファイル ID レコードを返します。                                                             |
| public Date getLabelFileCreatedDate(str labelFile, str language)      | 指定したラベル ファイルが作成された日付を返します。                                           |
| public int getLabelFileCreatedTime(str labelFile, str language)       | 指定したラベル ファイルが作成された時刻を返します。                                           |
| public Date getLabelFileModificationDate(str labelFile, str language) | 変更したラベル ファイルが作成された日付を返します。                                          |
| public int getLabelFileModificationTime(str labelFile, str language)  | 変更したラベル ファイルが作成された時刻を返します。                                          |
| public str getNextLabelFile()                                         | 次のラベル ファイル ID レコードを返します。                                                              |
| public str insert(str text, str comment, str module)                  | 指定されたテキスト文字列のラベル ID を作成します。                                                     |
| public int labelId(str label)                                         | 指定したラベル ID に含まれる番号を返します。                                        |
| public int maxLabelId(str module)                                     | 指定したラベル ファイル内の最後のラベルの ID を返します。                                      |
| public boolean modify(str label, str text, \[str comment\])           | 指定されたラベルに関連付けられているテキストおよびコメントを変更します。                           |
| public str moduleId(str label)                                        | 指定したラベル ID のラベル ファイルを返します。                                                 |
| public boolean moreLabelFiles()                                       | 追加のラベル ファイルがあるかどうかを示します。                                                 |
| public str name(str module, int labelId)                              | 指定したラベル ファイル ID およびラベル ID 番号に基づいて、ラベル ID を返します。                         |
| public str searchFirst(str searchString)                              | 指定した検索用語で検出された最初のラベル ID を返します。                               |
| public str searchNext()                                               | searchFirst メソッドに渡される検索用語のある次のラベル ID を返します。 |
| ::public static boolean flush(str labelFileId, str language)          | ディスクにラベル ファイル バッファーをフラッシュします。                                                             |
| public void new(\[str language\])                                     | ラベル クラスの新しいインスタンスを作成します。                                                          |
| public void finalize()                                                | 現在のラベル ファイルを閉じます。                                                                      |

### <a name="method-bulkeditor"></a>メソッド bulkEditor

LabelBulkEditor クラスのインスタンスを作成します。

    public LabelBulkEditor bulkEditor(str module)

#### <a name="parameters"></a>パラメーター

モジュール  
3 文字のラベル ファイル ID を指定する文字列データ型。

#### <a name="return-value"></a>戻り値

LabelBulkEditor クラスのインスタンス。

#### <a name="remarks"></a>備考

LabelBulkEditor クラスを使用すると、ラベル ファイルが簡単に変更されます。 このメソッドは、クライアント層から呼び出されたときに nullNothingnullptrunita null 参照 (Visual BasicではNothing) を返します。

### <a name="method-createlabelfile"></a>メソッド createLabelFile

指定されたラベル ID のラベル ファイルを作成します。

    public boolean createLabelFile(str module, str language)

#### <a name="parameters"></a>パラメーター

モジュール  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

#### <a name="return-value"></a>戻り値

ファイルが作成された場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

ラベル ファイルは、ファイル バッファがディスクにフラッシュされた後に作成されます。これは、サーバーが閉じるときに発生します。

### <a name="method-delete"></a>メソッド delete

指定したラベルを削除します。

    public boolean delete(str label)

#### <a name="parameters"></a>パラメーター

ラベル  
ラベル ID を指定する文字列。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

#### <a name="return-value"></a>戻り値

ラベル ID が削除された場合は true。それ以外の場合は false。

### <a name="method-exists"></a>メソッド exists

指定したラベル ID が存在するかどうかを示します。

    public boolean exists(str label)

#### <a name="parameters"></a>パラメーター

ラベル  
アット マーク (@) を含むラベル ID 文字列からの literalStr 関数の出力。

#### <a name="return-value"></a>戻り値

ラベル ID が存在する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

ラベル パラメーターの値の形式は、literalStr と同様でなければいけません ("@SYS24359")。

### <a name="method-extractcomment"></a>メソッド extractComment

指定されたラベル ID に関連付けられているコメントを返します。

    public str extractComment(str label)

#### <a name="parameters"></a>パラメーター

ラベル  
ラベル ID を指定する文字列。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

#### <a name="return-value"></a>戻り値

指定されたラベル ID に関連付けられているコメントを示す文字列値。

#### <a name="remarks"></a>備考

存在しないラベル ID を指定する場合、このメソッドは文字列として指定した ID を返します。 ラベル パラメーターの値に @ を含めない場合は、メソッドはラベル ID を返します。

### <a name="method-extractstring"></a>メソッド extractString

指定されたラベル ID に関連付けられているテキストを返します。

    public str extractString(str label)

#### <a name="parameters"></a>パラメーター

ラベル  
ラベル ID を指定する文字列データ型。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

#### <a name="return-value"></a>戻り値

指定されたラベル ID に関連付けられているテキストを示す文字列データ型の値。

#### <a name="remarks"></a>備考

存在しないラベル ID を指定する場合、メソッドは文字列として指定した ID を返します。 ラベル パラメーターの値に @ を含めない場合は、メソッドはラベル ID を返します。

### <a name="method-getfirstlabelfile"></a>メソッド getFirstLabelFile

最初のラベル ファイル ID レコードを返します。

    public str getFirstLabelFile()

#### <a name="return-value"></a>戻り値

ラベル ファイル ID を示す文字列データ型の値。

#### <a name="remarks"></a>備考

ラベル ファイル ID は、ラベル ファイルの 3 文字の識別子です。

### <a name="method-getlabelfilecreateddate"></a>メソッド getLabelFileCreatedDate

指定したラベル ファイルが作成された日付を返します。

    public Date getLabelFileCreatedDate(str labelFile, str language)

#### <a name="parameters"></a>パラメーター

labelFile  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

#### <a name="return-value"></a>戻り値

ラベル ファイルの作成日時を示す Date データ タイプ値。

#### <a name="remarks"></a>備考

date2str 関数を使用すると日付をテキスト文字列に変換することができます。

### <a name="method-getlabelfilecreatedtime"></a>メソッド getLabelFileCreatedTime

指定したラベル ファイルが作成された時刻を返します。

    public int getLabelFileCreatedTime(str labelFile, str language)

#### <a name="parameters"></a>パラメーター

labelFile  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

#### <a name="return-value"></a>戻り値

ラベル ファイルが作成された時間を示す整数データ型値。

#### <a name="remarks"></a>備考

詳細については、「方法: ラベル ファイルの作成」を参照してください。 time2str 関数を使用すると整数をテキスト文字列に変換することができます。

### <a name="method-getlabelfilemodificationdate"></a>メソッド getLabelFileModificationDate

変更したラベル ファイルが作成された日付を返します。

    public Date getLabelFileModificationDate(str labelFile, str language)

#### <a name="parameters"></a>パラメーター

labelFile  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

#### <a name="return-value"></a>戻り値

ラベル ファイルの変更日時を示す Date データ タイプ値。

#### <a name="remarks"></a>備考

date2str 関数を使用すると日付をテキスト文字列に変換することができます。

### <a name="method-getlabelfilemodificationtime"></a>メソッド getLabelFileModificationTime

変更したラベル ファイルが作成された時刻を返します。

    public int getLabelFileModificationTime(str labelFile, str language)

#### <a name="parameters"></a>パラメーター

labelFile  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

#### <a name="return-value"></a>戻り値

ラベル ファイルが変更された時間を示す整数データ型値。

#### <a name="remarks"></a>備考

time2str 関数を使用すると整数をテキスト文字列に変換することができます。

### <a name="method-getnextlabelfile"></a>メソッド getNextLabelFile

次のラベル ファイル ID レコードを返します。

    public str getNextLabelFile()

#### <a name="return-value"></a>戻り値

ラベル ファイル ID を示す文字列データ型の値。

#### <a name="remarks"></a>備考

ラベル ファイル ID は、ラベル ファイルの 3 文字の識別子です。

### <a name="method-insert"></a>メソッド insert

指定されたテキスト文字列のラベル ID を作成します。

    public str insert(str text, str comment, str module)

#### <a name="parameters"></a>パラメーター

テキスト  
3 文字のラベル ファイル ID を指定する文字列データ型。

<!-- -->

comment  
3 文字のラベル ファイル ID を指定する文字列データ型。

<!-- -->

モジュール  
3 文字のラベル ファイル ID を指定する文字列データ型。

#### <a name="return-value"></a>戻り値

作成されるラベル ID の文字列データ型の値。

#### <a name="remarks"></a>備考

この操作では、すべての言語に新しいラベル ID が割り当てられます。

### <a name="method-labelid"></a>メソッド labelId

指定したラベル ID に含まれる番号を返します。

    public int labelId(str label)

#### <a name="parameters"></a>パラメーター

ラベル  
ラベル ID を指定する文字列データ型。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

#### <a name="return-value"></a>戻り値

ラベル ID に含まれる番号を示す整数データ型値。

#### <a name="remarks"></a>備考

searchFirst または searchNext メソッドを呼び出してから、パラメーターとして戻り値をこのメソッドに渡す必要があります。

### <a name="method-maxlabelid"></a>メソッド maxLabelId

指定したラベル ファイル内の最後のラベルの ID を返します。

    public int maxLabelId(str module)

#### <a name="parameters"></a>パラメーター

モジュール  
3 文字のラベル ファイル ID を指定する文字列。

#### <a name="return-value"></a>戻り値

指定したラベル ファイルの最大ラベル ID を示す整数。

### <a name="method-modify"></a>メソッド modify

指定されたラベルに関連付けられているテキストおよびコメントを変更します。

    public boolean modify(str label, str text, [str comment])

#### <a name="parameters"></a>パラメーター

ラベル  
ラベル ID に関連付けられているコメントを指定する文字列。

<!-- -->

テキスト  
ラベル ID に関連付けられているコメントを指定する文字列。

<!-- -->

comment  
ラベル ID に関連付けられているコメントを指定する文字列。

#### <a name="return-value"></a>戻り値

ラベル ID が修正された場合は true。それ以外の場合は false。

### <a name="method-moduleid"></a>メソッド moduleId

指定したラベル ID のラベル ファイルを返します。

    public str moduleId(str label)

#### <a name="parameters"></a>パラメーター

ラベル  
ラベル ID を指定する文字列。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

#### <a name="return-value"></a>戻り値

指定したラベル ID のラベル ファイル ID を示す文字列。

#### <a name="remarks"></a>備考

SearchFirst または searchNext のメソッドを呼び出すパラメーターとして戻り値を labelId メソッドに渡す必要があります。

### <a name="method-morelabelfiles"></a>メソッド moreLabelFiles

追加のラベル ファイルがあるかどうかを示します。

    public boolean moreLabelFiles()

#### <a name="return-value"></a>戻り値

追加のラベル ファイルがある場合は true。それ以外の場合は、false。

### <a name="method-name"></a>メソッド名

指定したラベル ファイル ID およびラベル ID 番号に基づいて、ラベル ID を返します。

    public str name(str module, int labelId)

#### <a name="parameters"></a>パラメーター

モジュール  
ラベル ID の数値部分を指定する整数。

<!-- -->

labelId  
ラベル ID の数値部分を指定する整数。

#### <a name="return-value"></a>戻り値

ラベル ID を示す文字列値。

### <a name="method-searchfirst"></a>メソッド searchFirst

指定した検索用語で検出された最初のラベル ID を返します。

    public str searchFirst(str searchString)

#### <a name="parameters"></a>パラメーター

searchString  
検索用語を指定する文字列。

#### <a name="return-value"></a>戻り値

ラベル ID を示す文字列値。

### <a name="method-searchnext"></a>メソッド searchNext

searchFirst メソッドに渡される検索用語のある次のラベル ID を返します。

    public str searchNext()

#### <a name="return-value"></a>戻り値

ラベル ID を示す文字列値。

#### <a name="remarks"></a>備考

このメソッドを呼び出す前に、searchFirst メソッドを呼び出す必要があります。 それ以外の場合、このメソッドは、ランダムなラベル ID を返します。

### <a name="method-flush"></a>メソッド flush

ディスクにラベル ファイル バッファーをフラッシュします。

    public static boolean flush(str labelFileId, str language)

#### <a name="parameters"></a>パラメーター

labelFileId  
言語の接頭語を使用して、言語を指定する文字列。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列。

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

ラベル クラスの新しいインスタンスを作成します。

    public void new([str language])

#### <a name="parameters"></a>パラメーター

言語  
言語の接頭語を使用して、言語を指定する文字列。

### <a name="method-finalize"></a>メソッド finalize

現在のラベル ファイルを閉じます。

    public void finalize()

## <a name="class-labelbulkeditor"></a>クラス LabelBulkEditor
    class LabelBulkEditor extends Object

LabelBulkEditor クラスを使用すると、ラベル ファイルが簡単に変更されます。

### <a name="remarks"></a>備考

LabelBulkEditor クラスは、Label.bulkEditor() メソッドを通じてインスタンス化されます。 ラベル ファイルは、クラスのインスタンスが作成されたときに変更用に開かれ、インスタンスがガベージ コレクションされたときにラベル ファイルは閉じられます。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                      | 説明                                                                  |
|-------------------------------------------------------------|------------------------------------------------------------------------------|
| public boolean delete(str label)                            | 指定したラベルを削除します。                                                   |
| public boolean modify(str label, str text, \[str comment\]) | 指定されたラベル ID に関連付けられているテキストおよびコメントを変更します。 |
| public void new()                                           | LabelBulkEditor クラスのインスタンスを初期化します。                        |

### <a name="method-delete"></a>メソッド delete

指定したラベルを削除します。

    public boolean delete(str label)

#### <a name="parameters"></a>パラメーター

ラベル  
ラベル ID を指定する文字列。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

#### <a name="return-value"></a>戻り値

ラベルが削除された場合は true。それ以外の場合は false。

### <a name="method-modify"></a>メソッド modify

指定されたラベル ID に関連付けられているテキストおよびコメントを変更します。

    public boolean modify(str label, str text, [str comment])

#### <a name="parameters"></a>パラメーター

ラベル  
ラベル ID に関連付けられているコメントを指定する文字列。

<!-- -->

テキスト  
ラベル ID に関連付けられているコメントを指定する文字列。

<!-- -->

comment  
ラベル ID に関連付けられているコメントを指定する文字列。

#### <a name="return-value"></a>戻り値

ラベルが修正された場合は true。それ以外の場合は false。

### <a name="method-new"></a>メソッド new

LabelBulkEditor クラスのインスタンスを初期化します。

    public void new()

## <a name="class-lastaotselection"></a>クラス LastAotSelection
    class LastAotSelection extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                           | 説明                                               |
|----------------------------------|-----------------------------------------------------------|
| public TreeNode first()          |                                                           |
| public TreeNode next()           |                                                           |
| public ProjectNode projectRoot() |                                                           |
| public int selectionCount()      |                                                           |
| public void new()                | LastAotSelection クラスの新しいインスタンスを初期化します。 |
| public void finalize()           |                                                           |

### <a name="method-first"></a>メソッド first

    public TreeNode first()

#### <a name="return-value"></a>戻り値

### <a name="method-next"></a>メソッド next

    public TreeNode next()

#### <a name="return-value"></a>戻り値

### <a name="method-projectroot"></a>メソッド projectRoot

    public ProjectNode projectRoot()

#### <a name="return-value"></a>戻り値

### <a name="method-selectioncount"></a>メソッド selectionCount

    public int selectionCount()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

LastAotSelection クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-list"></a>クラス リスト
    class List extends Object

順にアクセスされる任意の数の要素を含みます。 リストは、あらゆる X++ 型の値を含めることができる構造です。 リスト内のすべての値は同じタイプである必要があります。

### <a name="remarks"></a>備考

リスト内の値のタイプは、リストが作成されたときに指定され、後で変更することはできません。 リストの実装は、リスト要素のトラバーサルを非常に高速にします。 リストを移動するには、ListEnumerator クラスを使用します。 ListEnumerator オブジェクトを作成するには、List.getEnumerator を使用します。

### <a name="examples"></a>例

次の例では、整数のリストを作成し、リストの説明とそれに含まれる値を出力します。

    { 
        // Create a list of integers 
        List il = new List(Types::Integer); 
        // Add some elements to the list 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addStart(3); 
        // Print a description of the list 
        print il.definitionString(); 
        print il.toString(); 
        pause; 
    }

### <a name="methods"></a>メソッド

| 方法                                                | 説明                                                                           |
|-------------------------------------------------------|---------------------------------------------------------------------------------------|
| public AnyType addEnd(AnyType element)                | リストの末尾に値を追加します。                                                  |
| public AnyType addStart(AnyType element)              | リストの冒頭に値を追加します。                                                |
| public str definitionString()                         | リスト内のすべての要素のタイプの説明を返します。                        |
| public int elements()                                 | リスト内の要素の数を指定します。                                           |
| public boolean empty()                                | 一覧が空であるかどうかを判定します。                                                   |
| public boolean equalTo(List l)                        | 一覧が現在の一覧と同じかどうかを判定します。                            |
| public ListEnumerator getEnumerator()                 | リストのスキャンを可能にするリストの列挙子を作成します。               |
| public container pack()                               | List クラスの現在のインスタンスをシリアル化します。                                    |
| public str toString()                                 | リスト内の値の説明を返します。                                      |
| public Types typeId()                                 | リスト内の値のタイプを返します。                                             |
| public str xml(\[int indent\])                        | 現在のオブジェクトを表す XML 文字列を返します。                             |
| ::public static List create(container container)      | 以前の List.pack メソッドの呼び出しで取得したコンテナーからリストを作成します。 |
| ::public static List createFromXML(Object xmlnode)    |                                                                                       |
| ::public static boolean equal(List list1, List list2) | 2 つのリストが同じかどうかを判定します。                                           |
| ::public static List merge(List list1, List list2)    | 2 つのリストを組み合わせ、新しいリストを作成します。                                              |
| public void appendList(List list)                     |                                                                                       |
| public void new(Types Type)                           | リストを作成します。                                                                       |

### <a name="method-addend"></a>メソッド addEnd

リストの末尾に値を追加します。

    public AnyType addEnd(AnyType element)

#### <a name="parameters"></a>パラメーター

要素  
リストの末尾に追加する値。

#### <a name="return-value"></a>戻り値

リストに追加される値。

### <a name="method-addstart"></a>メソッド addStart

リストの冒頭に値を追加します。

    public AnyType addStart(AnyType element)

#### <a name="parameters"></a>パラメーター

要素  
リストの冒頭に追加する値。

#### <a name="return-value"></a>戻り値

このリストに追加される値。

#### <a name="remarks"></a>備考

要素は、List.addEnd メソッドを使用して、リストの最後に追加できます。

#### <a name="examples"></a>例

次の例では、整数のリストを作成し、値の 1 と 2 をリストの末尾に追加し、値 3 をリストの先頭に追加します。 List.toString メソッドによって返される値は{3,1,2}です。

    { 
        // Create a list of integers 
        list il = new List(Types::Integer); 
        // Add some elements to the list 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addStart(3); 
        // Print a description of the list. 
        print il.definitionString(); 
        print il.toString(); 
        pause; 
    }

### <a name="method-definitionstring"></a>メソッド definitionString

リスト内のすべての要素のタイプの説明を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

リストの定義を含む文字列。

#### <a name="remarks"></a>備考

たとえば、このメソッドは、「int の一覧」を返すことができます。 リスト内の値の一覧を印刷するには、List.toString メソッドを使用します。

#### <a name="examples"></a>例

次の例では、整数のリストを作成します。 definitionString メソッドを使用して、リストの説明を出力します。

    { 
        // Create a list of integers 
        List il = new List(Types::Integer); 
        // Add some elements to the list 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addStart(3); 
        // Print a description ofvthe list 
        print il.definitionString(); 
        print il.toString(); 
        pause; 
    }

### <a name="method-elements"></a>メソッド elements

リスト内の要素の数を指定します。

    public int elements()

#### <a name="return-value"></a>戻り値

リスト内の要素の数。

#### <a name="examples"></a>例

次の例では、整数のリストを作成し、いくつかの要素を追加します。 要素メソッドは、リストに 3 つの要素があるかどうかをテストするために使用されます。

    { 
        List il = new List(Types::Integer); 
        il.addStart(1); 
        il.addStart(2); 
        il.addStart(3); 
        if (il.elements() != 3) 
        { 
            print "Something is wrong..."; 
        } 
    }

### <a name="method-empty"></a>メソッド empty

一覧が空であるかどうかを判定します。

    public boolean empty()

#### <a name="return-value"></a>戻り値

リストが空の場合は true。それ以外の場合は、false。

### <a name="method-equalto"></a>メソッド equalTo

一覧が現在の一覧と同じかどうかを判定します。

    public boolean equalTo(List l)

#### <a name="parameters"></a>パラメーター

l  
現在のリストと比較されるリスト。

#### <a name="return-value"></a>戻り値

指定したリストが、メソッドが呼び出されたリストと同一である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

2 つのリストが同じ型の場合、リストは別のリストと等しくなり、要素の同じ番号を含み、同じ順序で要素が発生します。 equalTo メソッドは、List.equal メソッドを使用するためのショートカットです。(this、l) と等しい。

### <a name="method-getenumerator"></a>メソッド getEnumerator

リストのスキャンを可能にするリストの列挙子を作成します。

    public ListEnumerator getEnumerator()

#### <a name="return-value"></a>戻り値

現在のリストの listEnumerator オブジェクト。

### <a name="method-pack"></a>メソッド pack

List クラスの現在のインスタンスをシリアル化します。

    public container pack()

#### <a name="return-value"></a>戻り値

List クラスの現在のインスタンスを含むコンテナーです。

#### <a name="remarks"></a>備考

このメソッドで作成されたコンテナーには、リストの最初の要素の前に 3 つの要素が含まれます。

-   コンテナのバージョン番号
-   リスト要素のデータ型を識別する整数
-   リスト内の要素の数。

リスト内の要素がオブジェクトとなっている場合は、梱包は、各オブジェクトに対して pack メソッドを連続して呼び出し、サブコンテナーを取得することによって行われます。 List.create メソッドを使用して、パックされたコンテナーからリストを取得できます。

#### <a name="examples"></a>例

次の例では、レコードのリストを作成し、新しい projReverseMarking オブジェクトを作成するためのパラメーターとしてパックされたリストに渡します。

    public boolean canClose() 
    { 
        ProjReverseMarking      projReverseMarking; 
        boolean                 canClose; 
        List                    list; 
        canClose = super(); 
        if (element.closedOk() && canClose) 
        { 
            List = new List(Types::Record); 
            while select tmpFrmVirtualLines 
            { 
                list.addEnd(tmpFrmVirtualLines); 
            } 
            projReverseMarking = new ProjReverseMarking(list.pack()); 
            projReverseMarking.run(); 
        } 
        return canClose; 
    }

### <a name="method-tostring"></a>メソッド toString

リスト内の値の説明を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

リストの要素の値を説明する文字列。

#### <a name="remarks"></a>備考

リスト内の要素のタイプの説明を印刷するには、List.definitionString メソッドを使用します。

#### <a name="examples"></a>例

次の例では、整数のリストを作成します。 toString メソッドを使用して、リストにある値の説明を出力します。

    { 
        // Create a list of integers 
        List il = new List(Types::Integer); 
        // Add some elements to the list 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addStart(3); 
        // Print a description of the list 
        print il.definitionString(); 
        print il.toString(); 
        pause; 
    }

### <a name="method-typeid"></a>メソッド typeId

リスト内の値のタイプを返します。

    public Types typeId()

#### <a name="return-value"></a>戻り値

リスト要素のタイプ。

#### <a name="remarks"></a>備考

リストのタイプは、リストが作成されるときに指定され、リストの存続期間中は同じままです。

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

### <a name="method-create"></a>メソッド create

以前の List.pack メソッドの呼び出しで取得したコンテナーからリストを作成します。

    public static List create(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  
パックされたリストを保持するコンテナー。

#### <a name="return-value"></a>戻り値

コンテナーに梱包されたものと同一のリスト。

#### <a name="examples"></a>例

次の例では、リストを作成し、それをコンテナーにパックします。 次に、create メソッドを使用してコンテナーを展開し、元のリストと同じリストを作成します。

    { 
        List il = new List(Types::Integer); 
        List newList; 
        container packedList; 
        // Add some elements 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addEnd(3); 
        // Pack the list into a container 
        packedList = il.pack(); 
        newList = list::create(packedList); 
        // Prints <1, 2, 3> 
        print newList.toString(); 
        pause; 
    }

### <a name="method-createfromxml"></a>メソッド createFromXML

    public static List createFromXML(Object xmlnode)

#### <a name="parameters"></a>パラメーター

xmlnode  

#### <a name="return-value"></a>戻り値

### <a name="method-equal"></a>メソッド equal

2 つのリストが同じかどうかを判定します。

    public static boolean equal(List list1, List list2)

#### <a name="parameters"></a>パラメーター

list1  
比較する 2 番目のリスト。

<!-- -->

list2  
比較する 2 番目のリスト。

#### <a name="return-value"></a>戻り値

2 つのリストが同一である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

2 つのリストが同じ型の場合、リストは別のリストと等しくなり、要素の同じ番号を含み、同じ順序で要素が発生します。

### <a name="method-merge"></a>メソッド merge

2 つのリストを組み合わせ、新しいリストを作成します。

    public static List merge(List list1, List list2)

#### <a name="parameters"></a>パラメーター

list1  
新しいリストを作成するために最初のリストの最後に追加されるリスト。

<!-- -->

list2  
新しいリストを作成するために最初のリストの最後に追加されるリスト。

#### <a name="return-value"></a>戻り値

新しいリスト。

#### <a name="remarks"></a>備考

リストのタイプは同じにする必要があります。

#### <a name="examples"></a>例

次の例では、2 つの整数値のリストを作成し、それらをマージして新しいリストを作成し、新しい組み合わせリストに値を出力します。

    { 
        List list1  = new List(Types::Integer); 
        List list2  = new List(Types::Integer); 
        List combinedList  = new List(Types::Integer); 
        int  i; 
        for(i=1; i<6; i++) 
        { 
            List1.addEnd(i); 
        } 
         for(i=6; i<11; i++) 
        { 
            List2.addEnd(i); 
        } 
        combinedList = List::merge(list1, list2); 
        print combinedList.toString(); 
        pause; 
    }

### <a name="method-appendlist"></a>メソッド appendList

    public void appendList(List list)

#### <a name="parameters"></a>パラメーター

リスト  

### <a name="method-new"></a>メソッド new

リストを作成します。

    public void new(Types Type)

#### <a name="parameters"></a>パラメーター

種類  
リスト内の要素が持つべきタイプ。

#### <a name="remarks"></a>備考

Type パラメーターの使用可能な値は、Type システム列挙によって提供されます。 リストを作成した後、そのリストに含まれている要素のタイプを変更することはできません。

#### <a name="examples"></a>例

次の例では、文字列のリストを作成します。

    { 
        // Creates a list of integers. 
        List il = new List(Types::String); 
    }

## <a name="class-listenumerator"></a>クラス ListEnumerator
    class ListEnumerator extends Object

ListEnumerator クラスを使用すると、一覧内の要素上を移動できます。

### <a name="remarks"></a>備考

リストの列挙子は、リストの最初の要素の前に開始します。 リストの最初の要素を指すようにするために ListEnumerator.moveNext メソッドを呼び出す必要があります。 list.getEnumerator メソッドが呼び出されたときに、リストと同じ層で列挙子が自動的に作成されるため、ListIterator クラスではなく、ListEnumerator クラスを使用することがベスト プラクティスです。 これにより、Caller from としてマークされたコードの潜在的な問題を回避します。反復子とリストは別々の層に置くことができます。 さらに、リスト列挙子はリスト反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。 リスト反復子を使用する必要がある唯一の状況は、リストから項目を削除する場合です (ListIterator.delete メソッドを使用します)。

### <a name="examples"></a>例

次の例では、整数のリストを作成し、いくつかの値をその中に入れます。 その後、列挙子を作成し、一覧の最初の要素、一覧の 2 番目の要素に列挙子を設定します。

    { 
        List list = new List(Types::Integer); 
        ListEnumerator enumerator; 
        // Add some elements to the list 
        list.addEnd(1); 
        list.addEnd(2); 
        list.addStart(3); 
        // Set the enumerator 
        enumerator = list.getEnumerator(); 
        // Print a description of the list 
        print enumerator.definitionString(); 
        // Go to beginning of enumerator 
        enumerator.reset(); 
        //Go to the first element in the List 
        enumerator.moveNext(); 
        // Print contents of first and second elements 
        // First element is 3 as this was added to start of list 
        print enumerator.toString(); 
        enumerator.moveNext(); 
        print enumerator.toString(); 
        pause; 
    }

### <a name="methods"></a>メソッド

| 方法                        | 説明                                                                                                   |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| public AnyType current()      | 列挙子によりポイントされている値を取得します。                                                     |
| public str definitionString() | 列挙子の説明を返します。                                                                      |
| public boolean moveNext()     | 列挙子が有効なリスト要素を示すかどうかを決定します。                                               |
| public str toString()         | 列挙子が現在ポイントしているリスト内の要素の内容の説明を返します。 |
| public void reset()           | 列挙子をリストの先頭に移動します。                                                                |

### <a name="method-current"></a>メソッド current

列挙子によりポイントされている値を取得します。

    public AnyType current()

#### <a name="return-value"></a>戻り値

リスト内で現在指定されている値。 戻り値のタイプは、リスト内の項目のタイプによって決まります。

#### <a name="examples"></a>例

次の例では、リストを反復処理し、dimensionTopic 変数を現在のリスト要素の値に設定します。

    public DimensionTopic firstDimensionTopic() 
    { 
        DimensionTopic  dimensionTopic; 
        ListEnumerator  enumerator; 
        enumerator = this.getTopicsEnumerator(); 
        if (enumerator.moveNext()) 
        { 
            dimensionTopic = enumerator.current(); 
        } 
        return dimensionTopic; 
    }

### <a name="method-definitionstring"></a>メソッド definitionString

列挙子の説明を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

列挙子の説明を含む文字列。

#### <a name="remarks"></a>備考

たとえば、整数のリストの列挙子は、int リスト列挙子を返します。

#### <a name="examples"></a>例

次の例では、リストとそのリストの列挙子を作成します。 definitionString メソッドを使用して、列挙子の説明を出力します。

    { 
        List list = new List(Types::Integer); 
        ListEnumerator  enumerator; 
        ; 
        // Add some elements to the list 
        list.addEnd(1); 
        list.addEnd(2); 
        list.addStart(3); 
        // Set the enumerator 
        enumerator = list.getEnumerator(); 
        print enumerator.definitionString(); 
        pause; 
    }

### <a name="method-movenext"></a>メソッド moveNext

列挙子が有効なリスト要素を示すかどうかを決定します。

    public boolean moveNext()

#### <a name="return-value"></a>戻り値

リスト内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

リストの列挙子は、リストの最初の要素の前に開始します。 リストの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。

#### <a name="examples"></a>例

次の例では、moveNext メソッドを使用してリスト内に別の要素があるかどうかを確認し、dimensionTopic 変数を現在のリスト要素の値に設定します。

    public DimensionTopic firstDimensionTopic() 
    { 
        DimensionTopic  dimensionTopic; 
        ListEnumerator  enumerator; 
        enumerator = this.getTopicsEnumerator(); 
        if (enumerator.moveNext()) 
        { 
            dimensionTopic = enumerator.current(); 
        } 
        return dimensionTopic; 
    }

### <a name="method-tostring"></a>メソッド toString

列挙子が現在ポイントしているリスト内の要素の内容の説明を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のリスト要素の説明を含む文字列。

#### <a name="examples"></a>例

次の例では、リストを作成し、最初の要素と 2 番目の要素の内容をリストに出力します。

    { 
        List list = new List(Types::Integer); 
        ListEnumerator  enumerator; 
        // Add some elements to the list 
        list.addEnd(1); 
        list.addEnd(2); 
        list.addStart(3); 
        // Set the enumerator 
        enumerator = list.getEnumerator(); 
        // Go to beginning of enumerator 
        enumerator.reset(); 
        //Go to the first element in the List 
        enumerator.moveNext(); 
        // First element is 3 as this was added to start of list 
        print enumerator.toString(); 
        pause; 
        enumerator.moveNext(); 
        //Print second element in list (1) 
        print enumerator.toString(); 
        pause; 
    }

### <a name="method-reset"></a>メソッド reset

列挙子をリストの先頭に移動します。

    public void reset()

#### <a name="remarks"></a>備考

reset メソッドは、列挙子をリストの先頭、リストの最初の要素の前に移動します。 リストの最初の要素を指すようにするために ListEnumerator.moveNext メソッドを呼び出す必要があります。

#### <a name="examples"></a>例

次の例では、リストを作成し、そのリストの列挙子を作成します。 reset メソッドを使用して一覧の先頭に移動し、moveNext メソッドを使用して一覧の最初の要素に移動します。

    { 
        List list = new List(Types::Integer); 
        ListEnumerator  enumerator; 
        // Add some elements to the list 
        list.addEnd(1); 
        list.addEnd(2); 
        list.addStart(3); 
        // Set the enumerator 
        enumerator = list.getEnumerator(); 
        // Go to beginning of enumerator 
        enumerator.reset(); 
        //Go to the first element in the List 
        enumerator.moveNext(); 
        // First element is 3 as this was added to start of list 
        print enumerator.toString(); 
        pause; 
    }

## <a name="class-listiterator"></a>クラス ListIterator
    class ListIterator extends Object

ListIterator クラスは、一覧内の要素を反復処理するために使用されます。

### <a name="remarks"></a>備考

リストの反復子は、反復処理する対象となるリストにポインターとして表示することができます。 繰り返しを開始する機能は利用可能であり、より多くの要素が利用可能であるかどうかを決定し、繰り返しによりポイントされる要素をフェッチします。 繰り返し中に要素が発生する順序は、要素が挿入される順序によって定義されます。 要素を挿入するには、List.addStart、List.addEnd、または ListIterator.insert メソッドを使用します。 ListIterator クラスよりも ListEnumerator クラスを使用することをお勧めします。 反復処理するリストの反復子およびマップは、同じクライアント/サーバー側にある必要があります。 ListIterator クラスを使用し、コードが Called from としてマークされている場合、リストと反復子が別の層で終了する可能性があります。 この場合、コードは失敗します。 ListEnumerator クラスを使用する場合、列挙子はリストと同じ層に自動的に作成されます。 また、リスト内の次のアイテムに移動するには、反復子リストを使用している場合は、より多くのメソッドと次のメソッドを明示的に呼び出す必要があります。 ListEnumerator クラスを使用する場合、moveNext メソッドを呼び出すだけです。 リスト列挙子を使用できない唯一の状況は、リストから要素を削除する必要がある場合です。 詳細については、「メソッドの削除」を参照してください。

### <a name="examples"></a>例

次の例では、リストとそれを指す反復子を作成します。 ListIterator クラスのさまざまなメソッドを使用して、一覧の説明と一覧内の項目を出力します。

    { 
        List il = new List(types::Integer); 
        ListIterator it; 
        // Add some elements into the list. 
        il.addStart(1); 
        il.addStart(2); 
        il.addStart(4);  
        // Create a list iterator to traverse the values. 
        it = new ListIterator (il);  
        // Prints "int list iterator". 
        print it.definitionString();  
        // Prints "(begin)[4]". 
        print it.toString();  
        // Go on for as long as elements are found in the list. 
        // Prints 4, 2, 1. 
        while (it.more()) 
        { 
            print it.value(); 
            it.next(); 
        } 
        // Prints (end). 
        print it.toString(); 
        pause; 
    }

### <a name="methods"></a>メソッド

| 方法                               | 説明                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------------------|
| public str definitionString()        | 反復子のタイプのテキスト表現を返します。                                  |
| public AnyType insert(AnyType value) | 反復子が現在ポイントしているリスト内の位置に新しい値を挿入します。         |
| public boolean more()                | リスト反復子が有効な要素を指しているかどうかを判定します。                                |
| public str toString()                | 反復子によりポイントされている現在のリスト値のテキスト形式を返します。 |
| public AnyType value()               | 反復子によりポイントされている値を取得します。                                        |
| public void begin()                  | 反復子をリストの先頭に移動します。                                                   |
| public void next()                   | リストで次の要素に反復子を移動します。                                            |
| public void end()                    | リストで最後の要素の後に反復子を移動します。                                          |
| public void delete()                 | 反復子によってポイントされている要素を一覧から削除します。                          |
| public void new(List list)           | 特定のリストに対する新しい反復子を作成します。                                                  |

### <a name="method-definitionstring"></a>メソッド definitionString

反復子のタイプのテキスト表現を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

反復子のタイプを含む文字列。

#### <a name="remarks"></a>備考

例: int リスト反復子。

### <a name="method-insert"></a>メソッド insert

反復子が現在ポイントしているリスト内の位置に新しい値を挿入します。

    public AnyType insert(AnyType value)

#### <a name="parameters"></a>パラメーター

値  
リストに挿入する項目の値。

#### <a name="return-value"></a>戻り値

リストに挿入された値。

#### <a name="remarks"></a>備考

value パラメーターは、リストと同じタイプである必要があります。

#### <a name="examples"></a>例

次の例では、10 個のアイテムを持つリストを作成し、ListIterator.insert メソッドを使用してリスト内の 3 番目のアイテムとして新しい値を挿入します。

    { 
        List il = new List(Types::Integer); 
        ListIterator it; 
        int i; 
        int j = 25; 
        // Insert values 1 to 10 into the list 
        for (i = 1; i <= 10; i++) 
        { 
            il.addEnd(i); 
        } 
        // Go to the 3rd element in the list 
        it = new ListIterator(il); 
        it.begin(); 
        it.next(); 
        it.next(); 
        // Insert a new value (25) 
        it.insert(j); 
      it.begin(); 
        // Print all values in the list. 
        // 25 is the third value in the list 
        while (it.more()) 
        { 
            print it.value(); 
            it.next();  
        } 
        pause; 
    }

### <a name="method-more"></a>メソッド more

リスト反復子が有効な要素を指しているかどうかを判定します。

    public boolean more()

#### <a name="return-value"></a>戻り値

リスト反復子が有効な要素を指定する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドが false を返すときに要素にアクセスしようとするとエラーが発生します。

#### <a name="examples"></a>例

次の例では、ListIterator.more メソッドを使用してリストに要素があるかどうかを確認し、リスト内のすべての要素の値を出力する while ループを実行します。

    { 
        List il = new List(Types::Integer); 
        ListIterator it; 
        int i; 
        // Add some elements 
        for (i = 1; i <= 10; i++) 
        { 
            il.addEnd(i); 
        } 
        // Traverse the list 
        it = new ListIterator(il); 
        while (it.more()) 
        { 
            print it.value(); 
            it.next(); // Skip to the next element 
        } 
        pause; 
    }

### <a name="method-tostring"></a>メソッド toString

反復子によりポイントされている現在のリスト値のテキスト形式を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在の値の説明を含む文字列。

#### <a name="remarks"></a>備考

反復子がリスト内の最初の要素を指している場合、文字列には "(開始)\[値\]" という形式の文字列が含まれます。反復子が要素を指していない場合 (つまり、more() メソッドが false を返す場合)、返される次の文字列は: (終了) になります。 反復子が値をポイントしている場合、文字列は "\[値\]" で、値が要素値の文字列表現です。

#### <a name="examples"></a>例

次の例では、リスト内の 2 つの値の値の説明を表示します。

1.  (開始) \[2\]
2.  \[1\]

<!-- -->

    { 
        List li = new List(Types::Integer); 
        ListIterator it = new ListIterator(li); 
        li.addStart(1); 
        li.addStart(2); // This is now the first value 
        it.begin(); 
        print it.toString(); 
        it.next(); 
        print it.toString(); 
        pause; 
    }

### <a name="method-value"></a>メソッド value

反復子によりポイントされている値を取得します。

    public AnyType value()

#### <a name="return-value"></a>戻り値

反復子によりポイントされている値。

#### <a name="remarks"></a>備考

リスト要素の値を取得する前に、ListIterator.more メソッドを使用して要素が存在するかどうかをテストします。

### <a name="method-begin"></a>メソッド begin

反復子をリストの先頭に移動します。

    public void begin()

### <a name="method-next"></a>メソッド next

リストで次の要素に反復子を移動します。

    public void next()

#### <a name="remarks"></a>備考

ListIterator.more メソッドを使用して、反復子が有効な要素を指しているかどうかを判断します。

#### <a name="examples"></a>例

次の例では、ListIterator.next メソッドを使用して、各要素の値が出力されるときにリストをスキャンします。

    { 
        List il = new List(Types::Integer); 
        ListIterator it; 
        int i; 
        // Add some elements 
        for (i = 1; i <= 10; i++) 
        { 
            il.addEnd(i); 
        } 
        // Traverse the list 
        it = new ListIterator(il); 
        while (it.more()) 
        { 
            print it.value(); 
            // Move to the next element 
            it.next();  
        } 
        pause; 
    }

### <a name="method-end"></a>メソッド end

リストで最後の要素の後に反復子を移動します。

    public void end()

#### <a name="remarks"></a>備考

このメソッドが実行すると、ListIterator.more メソッドが false に戻ります。

### <a name="method-delete"></a>メソッド delete

反復子によってポイントされている要素を一覧から削除します。

    public void delete()

#### <a name="remarks"></a>備考

反復子は、この削除の後に次の要素を指します。

#### <a name="examples"></a>例

次の例では、3 つの要素を含むリストを作成し、リスト内の要素の説明を出力します。 一覧の最初の要素を削除し、残りの要素の説明を印刷します。

    { 
        List li = new List(Types::Integer); 
        ListIterator it; 
        li.addStart(1); 
        li.addStart(2); 
        li.addStart(3); 
        print li.toString(); 
        it = new ListIterator(li); 
        it.delete(); 
        print li.toString(); 
        pause; 
    }

### <a name="method-new"></a>メソッド new

特定のリストに対する新しい反復子を作成します。

    public void new(List list)

#### <a name="parameters"></a>パラメーター

リスト  
反復子を作成するリスト。

#### <a name="remarks"></a>備考

反復子は、リストが空でない場合、リストの最初の値に配置されます。 反復子および繰り返すリストは、同じクライアント/サーバー側にする必要があります。

#### <a name="examples"></a>例

次の例では、整数リストの反復子を作成します。

    List il = new List(types::Integer); 
    ListIterator it; 
    it = new ListIterator (il);

## <a name="class-listpage"></a>クラス ListPage
    class ListPage extends Page

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                      | 説明                                       |
|-----------------------------------------------------------------------------|---------------------------------------------------|
| public str actionPaneControlParameters(str controlName, \[str parameters\]) |                                                   |
| public Array activeActionPaneTabNames()                                     | 指定された有効なタブの名前を取得します。        |
| public str caption(\[str value\])                                           |                                                   |
| public ListPageArgs listPageArgs()                                          |                                                   |
| public int listPageFieldDataField(str fieldName)                            |                                                   |
| public Array listPageFieldNames()                                           |                                                   |
| public int listPageFieldTableId(str fieldName)                              |                                                   |
| public boolean listPageFieldVisible(str fieldName, \[boolean visible\])     |                                                   |
| public str modeledQueryName(\[str value\])                                  |                                                   |
| public void new()                                                           | ListPage クラスの新しいインスタンスを初期化します。 |

### <a name="method-actionpanecontrolparameters"></a>メソッド actionPaneControlParameters

    public str actionPaneControlParameters(str controlName, [str parameters])

#### <a name="parameters"></a>パラメーター

controlName  

<!-- -->

パラメータ  

#### <a name="return-value"></a>戻り値

### <a name="method-activeactionpanetabnames"></a>メソッド activeActionPaneTabNames

指定された有効なタブの名前を取得します。

    public Array activeActionPaneTabNames()

#### <a name="return-value"></a>戻り値

アクティブなタブの名前を含む配列です。

### <a name="method-caption"></a>メソッド caption

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-listpageargs"></a>メソッド listPageArgs

    public ListPageArgs listPageArgs()

#### <a name="return-value"></a>戻り値

### <a name="method-listpagefielddatafield"></a>メソッド listPageFieldDataField

    public int listPageFieldDataField(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  

#### <a name="return-value"></a>戻り値

### <a name="method-listpagefieldnames"></a>メソッド listPageFieldNames

    public Array listPageFieldNames()

#### <a name="return-value"></a>戻り値

### <a name="method-listpagefieldtableid"></a>メソッド listPageFieldTableId

    public int listPageFieldTableId(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  

#### <a name="return-value"></a>戻り値

### <a name="method-listpagefieldvisible"></a>メソッド listPageFieldVisible

    public boolean listPageFieldVisible(str fieldName, [boolean visible])

#### <a name="parameters"></a>パラメーター

fieldName  

<!-- -->

表示  

#### <a name="return-value"></a>戻り値

### <a name="method-modeledqueryname"></a>メソッド modeledQueryName

    public str modeledQueryName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

ListPage クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-listpageargs"></a>クラス ListPageArgs
    class ListPageArgs extends PageArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法 | 説明 |
|--------|-------------|
|        |             |

## <a name="class-listpageinteraction"></a>クラス ListPageInteraction
    class ListPageInteraction extends PageInteraction

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                           | 説明                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| public ListPage listPage()                       |                                                               |
| public void tabChanged(container activeTabNames) | アクティブなタブが変更されたときに呼び出されます。                        |
| public void initializing()                       |                                                               |
| public void initialized()                        |                                                               |
| public void selectionChanged()                   |                                                               |
| public void initializeQuery(Query query)         |                                                               |
| public void new(ListPage listPage)               | listPage 上で動作する新しい PageInteraction オブジェクトを作成します。 |

### <a name="method-listpage"></a>メソッド listPage

    public ListPage listPage()

#### <a name="return-value"></a>戻り値

### <a name="method-tabchanged"></a>メソッド tabChanged

アクティブなタブが変更されたときに呼び出されます。

    public void tabChanged(container activeTabNames)

#### <a name="parameters"></a>パラメーター

activeTabNames  
アクティブなタブの名前を含むコンテナーです。

### <a name="method-initializing"></a>メソッド initializing

    public void initializing()

### <a name="method-initialized"></a>メソッド initialized

    public void initialized()

### <a name="method-selectionchanged"></a>メソッド selectionChanged

    public void selectionChanged()

### <a name="method-initializequery"></a>メソッド initializeQuery

    public void initializeQuery(Query query)

#### <a name="parameters"></a>パラメーター

クエリ  

### <a name="method-new"></a>メソッド new

listPage 上で動作する新しい PageInteraction オブジェクトを作成します。

    public void new(ListPage listPage)

#### <a name="parameters"></a>パラメーター

listPage  
指定した ListPage オブジェクト。

## <a name="class-loadautocompletedataeventargs"></a>クラス LoadAutoCompleteDataEventArgs
    class LoadAutoCompleteDataEventArgs extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                          | 説明 |
|-------------------------------------------------------------------------------------------------|-------------|
| public AutoCompleteDataMode autoCompleteDataMode(\[AutoCompleteDataMode autoCompleteDataMode\]) |             |
| public boolean canPage(\[boolean canPage\])                                                     |             |
| public str filterValue()                                                                        |             |
| public AnyType lastPagedTag()                                                                   |             |
| public FormSegment segment()                                                                    |             |
| public void addAutoCompleteData(str value, str description, AnyType tag)                        |             |

### <a name="method-autocompletedatamode"></a>メソッド autoCompleteDataMode

    public AutoCompleteDataMode autoCompleteDataMode([AutoCompleteDataMode autoCompleteDataMode])

#### <a name="parameters"></a>パラメーター

autoCompleteDataMode  

#### <a name="return-value"></a>戻り値

### <a name="method-canpage"></a>メソッド canPage

    public boolean canPage([boolean canPage])

#### <a name="parameters"></a>パラメーター

canPage  

#### <a name="return-value"></a>戻り値

### <a name="method-filtervalue"></a>メソッド filterValue

    public str filterValue()

#### <a name="return-value"></a>戻り値

### <a name="method-lastpagedtag"></a>メソッド lastPagedTag

    public AnyType lastPagedTag()

#### <a name="return-value"></a>戻り値

### <a name="method-segment"></a>メソッド segment

    public FormSegment segment()

#### <a name="return-value"></a>戻り値

### <a name="method-addautocompletedata"></a>メソッド addAutoCompleteData

    public void addAutoCompleteData(str value, str description, AnyType tag)

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

description  

<!-- -->

タグ  

## <a name="class-loginproperty"></a>クラス LoginProperty
    class LoginProperty extends Object

LoginProperty クラスでは、OdbcConnection クラスのインスタンスにログオン情報を渡すことができます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                | 説明                                                                                                                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public str getDatabase()                              | LoginProperty クラスに格納されている、データベースの名前を取得します。                                                                                                                              |
| public str getDSN()                                   | LoginProperty クラスに格納されているデータ ソース名 (DSN) を取得します。                                                                                                                        |
| public str getOciServiceName()                        | LoginProperty クラスに格納されている Oracle サービス名を取得します。                                                                                                                           |
| public str getOther()                                 | LoginProperty クラスに格納されているその他のログオン パラメーターを取得します。                                                                                                                  |
| public str getServer()                                | LoginProperty クラスに格納されているサーバー名を取得します。                                                                                                                                   |
| public str getTcpIpPort()                             | LoginProperty クラスに格納されている TCP/IP ポートを取得します。                                                                                                                                   |
| public boolean getUsePredefinedService()              | loginProperty クラスが、loginProperty クラスでサーバーおよびデータベース情報を指定する代わりに、事前定義された Oracle サービスを使用するように設定されているかどうかを返します。                                |
| public void setTcpIpPort(str tcpipPort)               | Oracle に接続するために使用される TCP/IP ポートを指定します。                                                                                                                                              |
| public void setDatabase(str database)                 | ログイン先のデータベースの名前を設定します。                                                                                                                                                            |
| public void setDSN(str datasourceName)                | データ ソースへのアクセスに使用される DSN を設定します。                                                                                                                                                   |
| public void new()                                     | LoginProperty クラスの新しいインスタンスを初期化します。                                                                                                                                                 |
| public void setOciServiceName(str ociServiceName)     | Oracle サービス名を指定します。                                                                                                                                                                      |
| public void setOther(str otherOdbcParameters)         | LoginProperty クラスに格納されているその他の非標準ログオン パラメーターを設定します。                                                                                                               |
| public void setServer(str serverName)                 | データベースが置かれているサーバーの名前を設定します。                                                                                                                                             |
| public void setUsePredefinedService(boolean newValue) | 接続情報に事前に定義された Oracle サービス (Oracle ネットワーク コンフィギュレーション ツールを使用して作成) を使用するかどうか、または loginProperty クラスで指定するかどうかを指定します。 |

### <a name="method-getdatabase"></a>メソッド getDatabase

LoginProperty クラスに格納されている、データベースの名前を取得します。

    public str getDatabase()

#### <a name="return-value"></a>戻り値

データベースの名前です。

### <a name="method-getdsn"></a>メソッド getDSN

LoginProperty クラスに格納されているデータ ソース名 (DSN) を取得します。

    public str getDSN()

#### <a name="return-value"></a>戻り値

DSN。

### <a name="method-getociservicename"></a>メソッド getOciServiceName

LoginProperty クラスに格納されている Oracle サービス名を取得します。

    public str getOciServiceName()

#### <a name="return-value"></a>戻り値

Oracle サービス名。

### <a name="method-getother"></a>メソッド getOther

LoginProperty クラスに格納されているその他のログオン パラメーターを取得します。

    public str getOther()

#### <a name="return-value"></a>戻り値

文字列としての追加ログオン パラメーター。

### <a name="method-getserver"></a>メソッド getServer

LoginProperty クラスに格納されているサーバー名を取得します。

    public str getServer()

#### <a name="return-value"></a>戻り値

サーバーの名前。

### <a name="method-gettcpipport"></a>メソッド getTcpIpPort

LoginProperty クラスに格納されている TCP/IP ポートを取得します。

    public str getTcpIpPort()

#### <a name="return-value"></a>戻り値

TCP/IP ポート。

### <a name="method-getusepredefinedservice"></a>メソッド getUsePredefinedService

loginProperty クラスが、loginProperty クラスでサーバーおよびデータベース情報を指定する代わりに、事前定義された Oracle サービスを使用するように設定されているかどうかを返します。

    public boolean getUsePredefinedService()

#### <a name="return-value"></a>戻り値

定義済みの Oracle サービスが接続に使用される場合は true。それ以外の場合は、false。

### <a name="method-settcpipport"></a>メソッド setTcpIpPort

Oracle に接続するために使用される TCP/IP ポートを指定します。

    public void setTcpIpPort(str tcpipPort)

#### <a name="parameters"></a>パラメーター

tcpipPort  
使用する TCP/IP ポート。

#### <a name="remarks"></a>備考

既定のポートは 1521 です。

### <a name="method-setdatabase"></a>メソッド setDatabase

ログイン先のデータベースの名前を設定します。

    public void setDatabase(str database)

#### <a name="parameters"></a>パラメーター

データベース  
データベースの名前です。

### <a name="method-setdsn"></a>メソッド setDSN

データ ソースへのアクセスに使用される DSN を設定します。

    public void setDSN(str datasourceName)

#### <a name="parameters"></a>パラメーター

datasourceName  
データ ソースの名前。

### <a name="method-new"></a>メソッド new

LoginProperty クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-setociservicename"></a>メソッド setOciServiceName

Oracle サービス名を指定します。

    public void setOciServiceName(str ociServiceName)

#### <a name="parameters"></a>パラメーター

ociServiceName  
サービスの名前。

#### <a name="remarks"></a>備考

このメソッドは、loginProperty クラスが事前定義済みの Oracle サービスを使用するように設定されていない場合に使用されます。

### <a name="method-setother"></a>メソッド setOther

LoginProperty クラスに格納されているその他の非標準ログオン パラメーターを設定します。

    public void setOther(str otherOdbcParameters)

#### <a name="parameters"></a>パラメーター

otherOdbcParameters  
ODBC 書式に設定された追加のパラメータ。

#### <a name="remarks"></a>備考

このメソッドは、使用するデータソースに追加の非標準のパラメーターが必要な場合にのみ使用してください。 パラメーターは、標準の ODBC 形式の &lt;parm1&gt;=&lt;value1&gt;;&lt;parm2&gt;=&lt;value2&gt; で、たとえば、MODE=1;PATCH=32 で適用する必要があります。

### <a name="method-setserver"></a>メソッド setServer

データベースが置かれているサーバーの名前を設定します。

    public void setServer(str serverName)

#### <a name="parameters"></a>パラメーター

serverName  
データベースがあるサーバーの名前。

### <a name="method-setusepredefinedservice"></a>メソッド setUsePredefinedService

接続情報に事前に定義された Oracle サービス (Oracle ネットワーク コンフィギュレーション ツールを使用して作成) を使用するかどうか、または loginProperty クラスで指定するかどうかを指定します。

    public void setUsePredefinedService(boolean newValue)

#### <a name="parameters"></a>パラメーター

newValue  
事前定義された Oracle サービスを使用するかどうかを示すブール値。

#### <a name="remarks"></a>備考

既定では、事前に定義されたサービスは使用されません。




