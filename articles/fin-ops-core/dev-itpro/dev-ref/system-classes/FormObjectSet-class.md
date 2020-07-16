---
title: FormObjectSet クラス
description: このトピックでは、FormObjectSet クラスについて説明します。
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
ms.openlocfilehash: 53f2d72d571a27176c02b2cd365ad6222104cb32
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502926"
---
# <a name="class-formobjectset"></a>クラス FormObjectSet

[!include [banner](../../includes/banner.md)]

```xpp
class FormObjectSet extends Object
```

FormObjectSet クラスは、フォームのデータ ソースを操作するための基本機能を提供する基本クラスです。

## <a name="remarks"></a>備考

FormObjectSet クラスのメソッドのほとんどは空です。 これらは、FormDataSource 派生クラスで実装されています。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                             | 説明                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int active()                                                | FormObjectSet クラスでの機能はありませんが、ユーザーが新しいレコードに移動するときに、結合されたデータ ソースからデータを取得する FormDataSource.active メソッドにより上書きされます。                                 |
| public Common cursor()                                             | FormObjectSet クラスでの機能はありませんが、データソースによって参照されるテーブル内の現在アクティブなレコードを返す FormDataSource.cursor メソッドによって上書きされます。                        |
| public boolean findRecord(Common record)                           | FormObjectSet クラスでの機能はありませんが、現在データソースで指定されるレコードを検索して現在のレコードにする FormDataSource.findRecord メソッドによって上書きされます。                                  |
| public boolean positionToRecord(Common record)                     |                                                                                                                                                                                                                             |
| public int first()                                                 | データ ソースの最初のレコードにフォーカスを移動します。                                                                                                                                                                           |
| public xFormRun formRun()                                          |                                                                                                                                                                                                                             |
| public int getPosition()                                           |                                                                                                                                                                                                                             |
| public int id()                                                    |                                                                                                                                                                                                                             |
| public int last()                                                  | データ ソースの最後のレコードにフォーカスを移動します。                                                                                                                                                                          |
| public boolean leaveRecord(\[boolean forceUpdate\])                | FormObjectSet クラスでの機能はありませんが、ユーザーが別のレコードに移動するときに通知を提供する FormDataSource.leaveRecord メソッドによって上書きされます。                                            |
| public FormObjectSet masterObjectSet()                             | 現在のオブジェクト セットのマスター オブジェクト セットを取得します。                                                                                                                                                                 |
| public str name(\[str value\])                                     | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                                                                                     |
| public int next()                                                  | データ ソースの次のレコードにフォーカスを移動します。                                                                                                                                                                          |
| public int nextPage(int pageSize)                                  | データ ソースで指定した数のレコード (位置変更) を進めます。                                                                                                                                                             |
| public FormDataObject object(int objectId)                         |                                                                                                                                                                                                                             |
| public int prev()                                                  | データ ソースの前のレコードにフォーカスを移動します。                                                                                                                                                                      |
| public int prevPage(int pageSize)                                  | データ ソースで指定した数のレコード (位置変更) を戻します。                                                                                                                                          |
| public boolean setPosition(int position)                           |                                                                                                                                                                                                                             |
| public boolean validateDelete()                                    | FormObjectSet クラスでの機能はありませんが、データソースからのレコードの削除をユーザーが確認するよう求める FormDataSource.validateDelete メソッドによって上書きされます。                             |
| public boolean validateWrite()                                     | FormObjectSet クラスでの機能はありませんが、データが有効であるかおよび書き込まれる準備ができているかどうかを判断する FormDataSource.validateWrite メソッドによって上書きされます。                                               |
| public void refresh()                                              | FormObjectSet クラスでの機能はありませんが、データ ソースにすべてのレコードの表示を更新する FormDataSource.refresh メソッドにより上書きされます。                                                           |
| public void addNotifyHandler(FormObjectSetNotify notifyHandler)    |                                                                                                                                                                                                                             |
| public void reread()                                               | FormObjectSet クラスでの機能はありませんが、データベースから現在のレコードを再読み込みする FormDataSource.reread メソッドにより上書きされます。                                                                  |
| public void init()                                                 | FormObjectSet クラスでの機能はありませんが、データ ソース プロパティに基づいてデータ ソース クエリを作成する FormDataSource.init メソッドにより上書きされます。                                                |
| public void deleteMarked()                                         | FormObjectSet クラスでの機能はありませんが、データソースからマークされたレコードをすべて削除する FormDataSource.deleteMarked メソッドによって上書きされます。                                                           |
| public void delete()                                               | FormObjectSet クラスでの機能はありませんが、現在データソースから選択されるレコードを削除する FormDataSource.delete メソッドによって上書きされます。                                            |
| public void write()                                                | FormObjectSet クラスでの機能はありませんが、データベースの書き込み操作を管理する FormDataSource.write メソッドにより上書きされます。                                                                           |
| public void create(\[boolean append\])                             | FormObjectSet クラスでの機能はありませんが、データ ソースに新しいレコードを作成する FormDataSource.create メソッドにより上書きされます。                                                                       |
| public void removeNotifyHandler(FormObjectSetNotify notifyHandler) |                                                                                                                                                                                                                             |
| public void prompt()                                               | FormObjectSet クラスでの機能はありませんが、クエリの範囲を制限するために使用される SysQueryForm クラスを有効にするFormDataSource.prompt メソッドによって上書きされます。                                          |
| public void research(\[boolean retainPosition\])                   | FormObjectSet クラスでの機能はありませんが、現在フォームに適用されているフィルターおよびソートで定義されているデータベースの検索を更新する FormDataSource.research メソッドによってオーバーライドされます。 |
| public void refreshEx(\[AnyType pos\])                             | FormObjectSet クラスでの機能はありませんが、特定のレコードの表示を更新する FormDataSource.refreshEx メソッドにより上書きされます。                                                                   |
| public void initValue()                                            | FormObjectSet クラスでの機能はありませんが、新しいレコードでフィールド値を初期化する FormDataSource.initValue メソッドにより上書きされます。                                                                   |
| public void removeFilter()                                         | FormObjectSet クラスでの機能はありませんが、データ ソースのクエリをリセットする FormDataSource.removeFilter メソッドにより上書きされます。                                                                    |

## <a name="method-active"></a>メソッド active

FormObjectSet クラスでの機能はありませんが、ユーザーが新しいレコードに移動するときに、結合されたデータ ソースからデータを取得する FormDataSource.active メソッドにより上書きされます。

```xpp
public int active()
```

### <a name="return-value---active"></a>戻り値 - active

常に 1 を返します。

## <a name="method-cursor"></a>メソッド cursor

FormObjectSet クラスでの機能はありませんが、データソースによって参照されるテーブル内の現在アクティブなレコードを返す FormDataSource.cursor メソッドによって上書きされます。

```xpp
public Common cursor()
```

### <a name="return-value---cursor"></a>戻り値 - cursor

## <a name="method-findrecord"></a>メソッド findRecord

FormObjectSet クラスでの機能はありませんが、現在データソースで指定されるレコードを検索して現在のレコードにする FormDataSource.findRecord メソッドによって上書きされます。

```xpp
public boolean findRecord(Common record)
```

### <a name="parameters---findrecord"></a>パラメーター - findRecord

記録  
FormObjectSet 基本クラスで使用されていないパラメーター。

### <a name="return-value---findrecord"></a>戻り値 - findRecord

レコードが見つかった場合は true。それ以外の場合は、false。

## <a name="method-positiontorecord"></a>メソッド positionToRecord

```xpp
public boolean positionToRecord(Common record)
```

### <a name="parameters---positiontorecord"></a>パラメーター - positionToRecord

記録  

### <a name="return-value---positiontorecord"></a>戻り値 - positionToRecord

## <a name="method-first"></a>メソッド first

データ ソースの最初のレコードにフォーカスを移動します。

```xpp
public int first()
```

### <a name="return-value---first"></a>戻り値 - first

操作が成功した場合はゼロ以外の整数。

### <a name="remarks---first"></a>備考 - first

このメソッドは、ユーザーが CTRL+HOME キーを押してフォームの最初のレコードを選択するときに呼び出されるメソッドによって上書きされます。

## <a name="method-formrun"></a>メソッド formRun

```xpp
public xFormRun formRun()
```

### <a name="return-value---formrun"></a>戻り値 - formRun

## <a name="method-getposition"></a>メソッド getPosition

```xpp
public int getPosition()
```

### <a name="return-value---getposition"></a>戻り値 - getPosition

## <a name="method-id"></a>メソッド id

```xpp
public int id()
```

### <a name="return-value---id"></a>戻り値 - id

## <a name="method-last"></a>メソッド last

データ ソースの最後のレコードにフォーカスを移動します。

```xpp
public int last()
```

### <a name="return-value---last"></a>戻り値 - last

操作が成功した場合はゼロ以外の整数。

### <a name="remarks---last"></a>備考 - last

このメソッドは、ユーザーが CTRL+END キーを押してフォームの最後のレコードを選択するときに呼び出されるメソッドによって上書きされます。

## <a name="method-leaverecord"></a>メソッド leaveRecord

FormObjectSet クラスでの機能はありませんが、ユーザーが別のレコードに移動するときに通知を提供する FormDataSource.leaveRecord メソッドによって上書きされます。

```xpp
public boolean leaveRecord([boolean forceUpdate])
```

### <a name="parameters---leaverecord"></a>パラメーター - leaveRecord

forceUpdate  

### <a name="return-value---leaverecord"></a>戻り値 - leaveRecord

## <a name="method-masterobjectset"></a>メソッド masterObjectSet

現在のオブジェクト セットのマスター オブジェクト セットを取得します。

```xpp
public FormObjectSet masterObjectSet()
```

### <a name="return-value---masterobjectset"></a>戻り値 - masterObjectSet

マスター オブジェクト セット。

### <a name="remarks---masterobjectset"></a>備考 - masterObjectSet

フォームには、多くの場合、1 つ以上のオブジェクトのセット (データ ソース) があります。 これらは、ツリー階層を使用して結合されます。ここでは、1 つのデータ ソースがマスターまたは親データソースです。 masterObjectSet メソッドは、特定のデータソースのマスター データソースの ID を返します。

### <a name="examples---masterobjectset"></a>例 - masterObjectSet

次の例は、FormRun オブジェクトのマスター データ ソースの名前を返します。

```xpp
private static client Name formDataSourceName(FormRun _formRun) 
{ 
    return _formRun.objectSet().masterObjectSet().name(); 
}
```

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  
コントロールに割り当てる名前。

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-next"></a>メソッド next

データ ソースの次のレコードにフォーカスを移動します。

```xpp
public int next()
```

### <a name="return-value---next"></a>戻り値 - next

操作が成功した場合はゼロ以外の整数。

### <a name="remarks---next"></a>備考 - next

このメソッドは、ユーザーが DOWN ARROW キーを押してフォームの次のレコードを選択するときに呼び出されます。

## <a name="method-nextpage"></a>メソッド nextPage

データ ソースで指定した数のレコード (位置変更) を進めます。

```xpp
public int nextPage(int pageSize)
```

### <a name="parameters---nextpage"></a>パラメーター - nextPage

pageSize  
スキップするレコードの数。

### <a name="return-value---nextpage"></a>戻り値 - nextPage

操作が成功した場合はゼロ以外の整数。

### <a name="remarks---nextpage"></a>備考 - nextPage

このメソッドは、ユーザーがフォーム内にあるときに PAGE DOWN キーを押すと呼び出されます。 これにより、ページ サイズは自動的に計算されて、pageSize パラメーターに使用されます。 このメソッドは、FormDataSource クラスで上書きされます。

## <a name="method-object"></a>メソッド object

```xpp
public FormDataObject object(int objectId)
```

### <a name="parameters---object"></a>パラメーター - object

objectId  

### <a name="return-value---object"></a>戻り値 - object

## <a name="method-prev"></a>メソッド prev

データ ソースの前のレコードにフォーカスを移動します。

```xpp
public int prev()
```

### <a name="return-value---prev"></a>戻り値 - prev

操作が成功した場合はゼロ以外の整数。

### <a name="remarks---prev"></a>備考 - prev

このメソッドは、ユーザーがフォーム内の前のレコードを選択したときに呼び出されます。

## <a name="method-prevpage"></a>メソッド prevPage

データ ソースで指定した数のレコード (位置変更) を戻します。

```xpp
public int prevPage(int pageSize)
```

### <a name="parameters---prevpage"></a>パラメーター - prevPage

pageSize  
戻すレコードの数 (位置の変更)。

### <a name="return-value---prevpage"></a>戻り値 - prevPage

操作が成功した場合はゼロ以外の整数。

### <a name="remarks---prevpage"></a>備考 - prevPage

このメソッドは、ユーザーがフォーム内にあるときに PAGE UP キーを押すと呼び出されます。 これにより、ページ サイズは自動的に計算されて、pageSize パラメーターに使用されます。

## <a name="method-setposition"></a>メソッド setPosition

```xpp
public boolean setPosition(int position)
```

### <a name="parameters---setposition"></a>パラメーター - setPosition

職位  

### <a name="return-value---setposition"></a>戻り値 - setPosition

## <a name="method-validatedelete"></a>メソッド validateDelete

FormObjectSet クラスでの機能はありませんが、データソースからのレコードの削除をユーザーが確認するよう求める FormDataSource.validateDelete メソッドによって上書きされます。

```xpp
public boolean validateDelete()
```

### <a name="return-value---validatedelete"></a>戻り値 - validateDelete

## <a name="method-validatewrite"></a>メソッド validateWrite

FormObjectSet クラスでの機能はありませんが、データが有効であるかおよび書き込まれる準備ができているかどうかを判断する FormDataSource.validateWrite メソッドによって上書きされます。

```xpp
public boolean validateWrite()
```

### <a name="return-value---validatewrite"></a>戻り値 - validateWrite

## <a name="method-refresh"></a>メソッド refresh

FormObjectSet クラスでの機能はありませんが、データ ソースにすべてのレコードの表示を更新する FormDataSource.refresh メソッドにより上書きされます。

```xpp
public void refresh()
```

## <a name="method-addnotifyhandler"></a>メソッド addNotifyHandler

```xpp
public void addNotifyHandler(FormObjectSetNotify notifyHandler)
```

### <a name="parameters---addnotifyhandler"></a>パラメーター - addNotifyHandler

notifyHandler  

## <a name="method-reread"></a>メソッド reread

FormObjectSet クラスでの機能はありませんが、データベースから現在のレコードを再読み込みする FormDataSource.reread メソッドにより上書きされます。

```xpp
public void reread()
```

## <a name="method-init"></a>メソッド init

FormObjectSet クラスでの機能はありませんが、データ ソース プロパティに基づいてデータ ソース クエリを作成する FormDataSource.init メソッドにより上書きされます。

```xpp
public void init()
```

## <a name="method-deletemarked"></a>メソッド deleteMarked

FormObjectSet クラスでの機能はありませんが、データソースからマークされたレコードをすべて削除する FormDataSource.deleteMarked メソッドによって上書きされます。

```xpp
public void deleteMarked()
```

## <a name="method-delete"></a>メソッド delete

FormObjectSet クラスでの機能はありませんが、現在データソースから選択されるレコードを削除する FormDataSource.delete メソッドによって上書きされます。

```xpp
public void delete()
```

## <a name="method-write"></a>メソッド write

FormObjectSet クラスでの機能はありませんが、データベースの書き込み操作を管理する FormDataSource.write メソッドにより上書きされます。

```xpp
public void write()
```

## <a name="method-create"></a>メソッド create

FormObjectSet クラスでの機能はありませんが、データ ソースに新しいレコードを作成する FormDataSource.create メソッドにより上書きされます。

```xpp
public void create([boolean append])
```

### <a name="parameters---create"></a>パラメーター - create

append  
現在のカーソル位置の前後にレコードを挿入するかどうかを示すブール値フラグ。 値が true に設定されている場合、現在のレコードの後に新しいレコードが挿入されます。

## <a name="method-removenotifyhandler"></a>メソッド removeNotifyHandler

```xpp
public void removeNotifyHandler(FormObjectSetNotify notifyHandler)
```

### <a name="parameters---removenotifyhandler"></a>パラメーター - removeNotifyHandler

notifyHandler  

## <a name="method-prompt"></a>メソッド prompt

FormObjectSet クラスでの機能はありませんが、クエリの範囲を制限するために使用される SysQueryForm クラスを有効にするFormDataSource.prompt メソッドによって上書きされます。

```xpp
public void prompt()
```

## <a name="method-research"></a>メソッド research

FormObjectSet クラスでの機能はありませんが、現在フォームに適用されているフィルターおよびソートで定義されているデータベースの検索を更新する FormDataSource.research メソッドによってオーバーライドされます。

```xpp
public void research([boolean retainPosition])
```

### <a name="parameters---research"></a>パラメーター - research

retainPosition  

## <a name="method-refreshex"></a>メソッド refreshEx

FormObjectSet クラスでの機能はありませんが、特定のレコードの表示を更新する FormDataSource.refreshEx メソッドにより上書きされます。

```xpp
public void refreshEx([AnyType pos])
```

### <a name="parameters---refreshex"></a>パラメーター - refreshEx

pos  
FormObjectSet.refreshEx メソッドで使用されていないパラメーター (オプション)。

## <a name="method-initvalue"></a>メソッド initValue

FormObjectSet クラスでの機能はありませんが、新しいレコードでフィールド値を初期化する FormDataSource.initValue メソッドにより上書きされます。

```xpp
public void initValue()
```

## <a name="method-removefilter"></a>メソッド removeFilter

FormObjectSet クラスでの機能はありませんが、データ ソースのクエリをリセットする FormDataSource.removeFilter メソッドにより上書きされます。

```xpp
public void removeFilter()
```

