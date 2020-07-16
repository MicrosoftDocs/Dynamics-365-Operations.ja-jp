---
title: 'Label クラス '
description: このトピックでは、Label クラスについて説明します。
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
ms.openlocfilehash: bd2d63127d839ec1cde16650d0b50707f9e10319
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502592"
---
# <a name="class-label"></a>クラス ラベル

[!include [banner](../../includes/banner.md)]


```xpp
class Label extends Object
```

Label クラスは、ラベル ID およびラベル ファイルを管理します。

## <a name="remarks"></a>備考

SysLabel クラスは、Label クラスを拡張します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-bulkeditor"></a>メソッド bulkEditor

LabelBulkEditor クラスのインスタンスを作成します。

```xpp
public LabelBulkEditor bulkEditor(str module)
```

### <a name="parameters---bulkeditor"></a>パラメータ - bulkEditor

モジュール  
3 文字のラベル ファイル ID を指定する文字列データ型。

### <a name="return-value---bulkeditor"></a>戻り値 - bulkEditor

LabelBulkEditor クラスのインスタンス。

### <a name="remarks---bulkeditor"></a>備考 - bulkEditor

LabelBulkEditor クラスを使用すると、ラベル ファイルが簡単に変更されます。 このメソッドは、クライアント層から呼び出されたときに nullNothingnullptrunita null 参照 (Visual Basic ではNothing) を返します。

## <a name="method-createlabelfile"></a>メソッド createLabelFile

指定されたラベル ID のラベル ファイルを作成します。

```xpp
public boolean createLabelFile(str module, str language)
```

### <a name="parameters---createlabelfile"></a>パラメーター - createLabelFile

モジュール  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

### <a name="return-value---createlabelfile"></a>戻り値 - createLabelFile

ファイルが作成された場合は true。それ以外の場合は false。

### <a name="remarks---createlabelfile"></a>備考 - createLabelFile

ラベル ファイルは、ファイル バッファがディスクにフラッシュされた後に作成されます。これは、サーバーが閉じるときに発生します。

## <a name="method-delete"></a>メソッド delete

指定したラベルを削除します。

```xpp
public boolean delete(str label)
```

### <a name="parameters---delete"></a>パラメーター - delete

ラベル  
ラベル ID を指定する文字列。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

### <a name="return-value---delete"></a>戻り値 - delete

ラベル ID が削除された場合は true。それ以外の場合は false。

## <a name="method-exists"></a>メソッド exists

指定したラベル ID が存在するかどうかを示します。

```xpp
public boolean exists(str label)
```

### <a name="parameters---exists"></a>パラメーター - exists

ラベル  
アット マーク (@) を含むラベル ID 文字列からの literalStr 関数の出力。

### <a name="return-value---exists"></a>戻り値 - exists

ラベル ID が存在する場合は true。それ以外の場合は、false。

### <a name="remarks---exists"></a>備考 - exists

ラベル パラメーターの値の形式は、literalStr と同様でなければいけません ("@SYS24359")。

## <a name="method-extractcomment"></a>メソッド extractComment

指定されたラベル ID に関連付けられているコメントを返します。

```xpp
public str extractComment(str label)
```

### <a name="parameters---extractcomment"></a>パラメーター - extractComment

ラベル  
ラベル ID を指定する文字列。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

### <a name="return-value---extractcomment"></a>戻り値 - extractComment

指定されたラベル ID に関連付けられているコメントを示す文字列値。

### <a name="remarks---extractcomment"></a>備考 - extractComment

存在しないラベル ID を指定する場合、このメソッドは文字列として指定した ID を返します。 ラベル パラメーターの値に @ を含めない場合は、メソッドはラベル ID を返します。

## <a name="method-extractstring"></a>メソッド extractString

指定されたラベル ID に関連付けられているテキストを返します。

```xpp
public str extractString(str label)
```

### <a name="parameters---extractstring"></a>パラメーター - extractString

ラベル  
ラベル ID を指定する文字列データ型。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

### <a name="return-value---extractstring"></a>戻り値 - extractString

指定されたラベル ID に関連付けられているテキストを示す文字列データ型の値。

### <a name="remarks---extractstring"></a>備考 - extractString

存在しないラベル ID を指定する場合、メソッドは文字列として指定した ID を返します。 ラベル パラメーターの値に @ を含めない場合は、メソッドはラベル ID を返します。

## <a name="method-getfirstlabelfile"></a>メソッド getFirstLabelFile

最初のラベル ファイル ID レコードを返します。

```xpp
public str getFirstLabelFile()
```

### <a name="return-value---getfirstlabelfile"></a>戻り値 - getFirstLabelFile

ラベル ファイル ID を示す文字列データ型の値。

### <a name="remarks---getfirstlabelfile"></a>備考 - getFirstLabelFile

ラベル ファイル ID は、ラベル ファイルの 3 文字の識別子です。

## <a name="method-getlabelfilecreateddate"></a>メソッド getLabelFileCreatedDate

指定したラベル ファイルが作成された日付を返します。

```xpp
public Date getLabelFileCreatedDate(str labelFile, str language)
```

### <a name="parameters---getlabelfilecreateddate"></a>パラメーター - getLabelFileCreatedDate

labelFile  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

### <a name="return-value---getlabelfilecreateddate"></a>戻り値 - getLabelFileCreatedDate

ラベル ファイルの作成日時を示す Date データ タイプ値。

### <a name="remarks---getlabelfilecreateddate"></a>備考 - getLabelFileCreatedDate

date2str 関数を使用すると日付をテキスト文字列に変換することができます。

## <a name="method-getlabelfilecreatedtime"></a>メソッド getLabelFileCreatedTime

指定したラベル ファイルが作成された時刻を返します。

```xpp
public int getLabelFileCreatedTime(str labelFile, str language)
```

### <a name="parameters---getlabelfilecreatedtime"></a>パラメーター - getLabelFileCreatedTime

labelFile  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

### <a name="return-value---getlabelfilecreatedtime"></a>戻り値 - getLabelFileCreatedTime

ラベル ファイルが作成された時間を示す整数データ型値。

### <a name="remarks---getlabelfilecreatedtime"></a>備考 - getLabelFileCreatedTime

詳細については、「方法: ラベル ファイルの作成」を参照してください。 time2str 関数を使用すると整数をテキスト文字列に変換することができます。

## <a name="method-getlabelfilemodificationdate"></a>メソッド getLabelFileModificationDate

変更したラベル ファイルが作成された日付を返します。

```xpp
public Date getLabelFileModificationDate(str labelFile, str language)
```

### <a name="parameters---getlabelfilemodificationdate"></a>パラメーター - getLabelFileModificationDate

labelFile  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

### <a name="return-value---getlabelfilemodificationdate"></a>戻り値 - getLabelFileModificationDate

ラベル ファイルの変更日時を示す Date データ タイプ値。

### <a name="remarks---getlabelfilemodificationdate"></a>戻り値 - getLabelFileModificationDate

date2str 関数を使用すると日付をテキスト文字列に変換することができます。

## <a name="method-getlabelfilemodificationtime"></a>メソッド getLabelFileModificationTime

変更したラベル ファイルが作成された時刻を返します。

```xpp
public int getLabelFileModificationTime(str labelFile, str language)
```

### <a name="parameters---getlabelfilemodificationtime"></a>パラメーター - getLabelFileModificationTime

labelFile  
言語の接頭語を使用して、言語を指定する文字列データ型。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列データ型。

### <a name="return-value---getlabelfilemodificationtime"></a>戻り値 - getLabelFileModificationTime

ラベル ファイルが変更された時間を示す整数データ型値。

### <a name="remarks---getlabelfilemodificationtime"></a>備考 - getLabelFileModificationTime

time2str 関数を使用すると整数をテキスト文字列に変換することができます。

## <a name="method-getnextlabelfile"></a>メソッド getNextLabelFile

次のラベル ファイル ID レコードを返します。

```xpp
public str getNextLabelFile()
```

### <a name="return-value---getnextlabelfile"></a>戻り値 - getNextLabelFile

ラベル ファイル ID を示す文字列データ型の値。

### <a name="remarks---getnextlabelfile"></a>備考 - getNextLabelFile

ラベル ファイル ID は、ラベル ファイルの 3 文字の識別子です。

## <a name="method-insert"></a>メソッド insert

指定されたテキスト文字列のラベル ID を作成します。

```xpp
public str insert(str text, str comment, str module)
```

### <a name="parameters---insert"></a>パラメーター - insert

テキスト  
3 文字のラベル ファイル ID を指定する文字列データ型。

<!-- -->

comment  
3 文字のラベル ファイル ID を指定する文字列データ型。

<!-- -->

モジュール  
3 文字のラベル ファイル ID を指定する文字列データ型。

### <a name="return-value---insert"></a>戻り値 - insert

作成されるラベル ID の文字列データ型の値。

### <a name="remarks---insert"></a>備考 - insert

この操作では、すべての言語に新しいラベル ID が割り当てられます。

## <a name="method-labelid"></a>メソッド labelId

指定したラベル ID に含まれる番号を返します。

```xpp
public int labelId(str label)
```

### <a name="parameters---labelid"></a>パラメーター - labelId

ラベル  
ラベル ID を指定する文字列データ型。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

### <a name="return-value---labelid"></a>戻り値 - LabelId

ラベル ID に含まれる番号を示す整数データ型値。

### <a name="remarks---labelid"></a>戻り値 - labelId

searchFirst または searchNext メソッドを呼び出してから、パラメーターとして戻り値をこのメソッドに渡す必要があります。

## <a name="method-maxlabelid"></a>メソッド maxLabelId

指定したラベル ファイル内の最後のラベルの ID を返します。

```xpp
public int maxLabelId(str module)
```

### <a name="parameters---maxlabelid"></a>パラメーター - maxLabelId

モジュール  
3 文字のラベル ファイル ID を指定する文字列。

### <a name="return-value---maxlabelid"></a>戻り値 - maxLabelId

指定したラベル ファイルの最大ラベル ID を示す整数。

## <a name="method-modify"></a>メソッド modify

指定されたラベルに関連付けられているテキストおよびコメントを変更します。

```xpp
public boolean modify(str label, str text, [str comment])
```

### <a name="parameters---modify"></a>パラメーター - modify

ラベル  
ラベル ID に関連付けられているコメントを指定する文字列。

<!-- -->

テキスト  
ラベル ID に関連付けられているコメントを指定する文字列。

<!-- -->

comment  
ラベル ID に関連付けられているコメントを指定する文字列。

### <a name="return-value---modify"></a>戻り値 - modify

ラベル ID が修正された場合は true。それ以外の場合は false。

## <a name="method-moduleid"></a>メソッド moduleId

指定したラベル ID のラベル ファイルを返します。

```xpp
public str moduleId(str label)
```

### <a name="parameters---moduleid"></a>パラメーター - moduleId

ラベル  
ラベル ID を指定する文字列。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

### <a name="return-value---moduleid"></a>戻り値 - moduleId

指定したラベル ID のラベル ファイル ID を示す文字列。

### <a name="remarks---moduleid"></a>備考 - moduleId

SearchFirst または searchNext のメソッドを呼び出すパラメーターとして戻り値を labelId メソッドに渡す必要があります。

## <a name="method-morelabelfiles"></a>メソッド moreLabelFiles

追加のラベル ファイルがあるかどうかを示します。

```xpp
public boolean moreLabelFiles()
```

### <a name="return-value---morelabelfiles"></a>戻り値 - moreLabelFiles

追加のラベル ファイルがある場合は true。それ以外の場合は、false。

## <a name="method-name"></a>メソッド名

指定したラベル ファイル ID およびラベル ID 番号に基づいて、ラベル ID を返します。

```xpp
public str name(str module, int labelId)
```

### <a name="parameters---name"></a>パラメーター - name

モジュール  
ラベル ID の数値部分を指定する整数。

<!-- -->

labelId  
ラベル ID の数値部分を指定する整数。

### <a name="return-value---name"></a>戻り値 - name

ラベル ID を示す文字列値。

## <a name="method-searchfirst"></a>メソッド searchFirst

指定した検索用語で検出された最初のラベル ID を返します。

```xpp
public str searchFirst(str searchString)
```

### <a name="parameters---searchfirst"></a>パラメーター - searchFirst

searchString  
検索用語を指定する文字列。

### <a name="return-value---searchfirst"></a>戻り値 - searchFirst

ラベル ID を示す文字列値。

## <a name="method-searchnext"></a>メソッド searchNext

searchFirst メソッドに渡される検索用語のある次のラベル ID を返します。

```xpp
public str searchNext()
```

### <a name="return-value---searchnext"></a>戻り値 - searchNext

ラベル ID を示す文字列値。

### <a name="remarks---searchnext"></a>備考 - searchNext

このメソッドを呼び出す前に、searchFirst メソッドを呼び出す必要があります。 それ以外の場合、このメソッドは、ランダムなラベル ID を返します。

## <a name="method-flush"></a>メソッド flush

ディスクにラベル ファイル バッファーをフラッシュします。

```xpp
public static boolean flush(str labelFileId, str language)
```

### <a name="parameters---flush"></a>パラメーター - flush

labelFileId  
言語の接頭語を使用して、言語を指定する文字列。

<!-- -->

言語  
言語の接頭語を使用して、言語を指定する文字列。

### <a name="return-value---flush"></a>戻り値 - flush

## <a name="method-new"></a>メソッド new

ラベル クラスの新しいインスタンスを作成します。

```xpp
public void new([str language])
```

### <a name="parameters---new"></a>パラメーター - new

言語  
言語の接頭語を使用して、言語を指定する文字列。

## <a name="method-finalize"></a>メソッド finalize

現在のラベル ファイルを閉じます。

```xpp
public void finalize()
```

