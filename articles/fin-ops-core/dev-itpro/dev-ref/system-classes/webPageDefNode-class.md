---
title: webPageDefNode クラス
description: このトピックでは、webPageDefNode クラスについて説明します。
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
ms.openlocfilehash: e914cd2b4640e9c6cbc333499053b73fc8a28087
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502685"
---
# <a name="class-webpagedefnode"></a>クラス webPageDefNode

[!include [banner](../../includes/banner.md)]

```xpp
class webPageDefNode extends TreeNode
```

webPageDefNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | ノードのソースを取得します。                                                                                                              |
| public str changedBy(\[str value\])                        | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])                    | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])                      | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])                        | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])                   | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])                     |                                                                                                                                           |
| public str helpText(\[str value\])                         | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public str imageResource(\[str value\])                    |                                                                                                                                           |
| public boolean mOSSOnly(\[boolean value\])                 |                                                                                                                                           |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                         |                                                                                                                                           |
| public str pageTitle(\[str value\])                        |                                                                                                                                           |
| public str parentPage(\[str value\])                       |                                                                                                                                           |
| public boolean publicPage(\[boolean value\])               |                                                                                                                                           |
| public str uRL(\[str value\])                              |                                                                                                                                           |
| public boolean useContext(\[boolean value\])               |                                                                                                                                           |
| public str webModule(\[str value\])                        |                                                                                                                                           |
| public str wSSHelpTopic(\[str value\])                     |                                                                                                                                           |
| public void new(str name)                                  | 新しい webPageDefNode の作成。                                                                                                             |
| public void AOTsetSource(str source, \[boolean isStatic\]) | 指定した文字列に webPageDefNode のソースを設定します。                                                                                 |

## <a name="method-aotgetsource"></a>メソッド AOTgetSource

ノードのソースを取得します。

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a>戻り値 - AOTgetSource

ノードのソース。

### <a name="remarks---aotgetsource"></a>備考 - AOTgetSource

このメソッドは、ソース コードを持つノードによって上書きされます。

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  

### <a name="return-value---creationdate"></a>戻り値 - creationDate

アプリケーション オブジェクトが作成された日付。

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  

### <a name="return-value---helptext"></a>戻り値 - helpText

画面の下部に表示される文字列。

### <a name="remarks---helptext"></a>備考 - helpText

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

## <a name="method-imageresource"></a>メソッド imageResource

```xpp
public str imageResource([str value])
```

### <a name="parameters---imageresource"></a>パラメーター - imageResource

値  

### <a name="return-value---imageresource"></a>戻り値 - imageResource

## <a name="method-mossonly"></a>メソッド mOSSOnly

```xpp
public boolean mOSSOnly([boolean value])
```

### <a name="parameters---mossonly"></a>パラメーター - mOSSOnly

値  

### <a name="return-value---mossonly"></a>戻り値 - mOSSOnly

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-pagetitle"></a>メソッド pageTitle

```xpp
public str pageTitle([str value])
```

### <a name="parameters---pagetitle"></a>パラメーター - pageTitle

値  

### <a name="return-value---pagetitle"></a>戻り値 - pageTitle

## <a name="method-parentpage"></a>メソッド parentPage

```xpp
public str parentPage([str value])
```

### <a name="parameters---parentpage"></a>パラメーター - parentPage

値  

### <a name="return-value---parentpage"></a>戻り値 - parentPage

## <a name="method-publicpage"></a>メソッド publicPage

```xpp
public boolean publicPage([boolean value])
```

### <a name="parameters---publicpage"></a>パラメーター - publicPage

値  

### <a name="return-value---publicpage"></a>戻り値 - publicPage

## <a name="method-url"></a>メソッド uRL

```xpp
public str uRL([str value])
```

### <a name="parameters---url"></a>パラメーター - uRL

値  

### <a name="return-value---url"></a>戻り値 - uRL

## <a name="method-usecontext"></a>メソッド useContext

```xpp
public boolean useContext([boolean value])
```

### <a name="parameters---usecontext"></a>パラメーター - useContext

値  

### <a name="return-value---usecontext"></a>戻り値 - useContext

## <a name="method-webmodule"></a>メソッド webModule

```xpp
public str webModule([str value])
```

### <a name="parameters---webmodule"></a>パラメーター - webModule

値  

### <a name="return-value---webmodule"></a>戻り値 - webModule

## <a name="method-wsshelptopic"></a>メソッド wSSHelpTopic

```xpp
public str wSSHelpTopic([str value])
```

### <a name="parameters---wsshelptopic"></a>パラメーター - wSSHelpTopic

値  

### <a name="return-value---wsshelptopic"></a>戻り値 - wSSHelpTopic

## <a name="method-new"></a>メソッド new

新しい webPageDefNode の作成。

```xpp
public void new(str name)
```

### <a name="parameters---new"></a>パラメーター - new

名前  

## <a name="method-aotsetsource"></a>メソッド AOTsetSource

指定した文字列に webPageDefNode のソースを設定します。

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a>パラメーター - AOTsetSource

ソース  
ソースが静的であるかどうかのマークを付けるオプションのパラメーター。

<!-- -->

isStatic  
ソースが静的であるかどうかのマークを付けるオプションのパラメーター。

### <a name="remarks---aotsetsource"></a>備考 - AOTgetSource

このメソッドは、ソース コードを持つノードによって上書きされます。

