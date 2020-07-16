---
title: FormDataSource クラス
description: このトピックでは、FormDataSource クラスについて説明します。
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
ms.openlocfilehash: 2e0077269d1c575f3f7bca2b580cd9e51ffe76bd
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502625"
---
# <a name="class-formdatasource"></a>クラス FormDataSource

[!include [banner](../../includes/banner.md)]

```xpp
class FormDataSource extends FormObjectSet
```

FormDataSource クラスには、フォーム内のデータ ソースの動作を定義するプロパティが含まれています。

## <a name="remarks"></a>備考

クラスのメソッドを上書きすることにより、特定のフォームの挿入または検証などのメソッド アクションの動作をカスタマイズできます。 FormDataSource クラスは、データ ソース テーブルが、フォームに表示される他のデータ ソース (テーブル) にどのように関連するかを決定するためにも使用されます。 FormDataSource クラスの一部のメソッドをオーバーライドするには、フォーム データソースのメソッド ノードを右クリックし、[メソッドをオーバーライド] をクリックします。 フォームに対してメソッドを作成するときは、特定のクラスの FormDataSource オブジェクトを参照するために、\_ds 識別子を使用する必要があります。 たとえば、CustTrans\_ds は、フォームの CustTrans データ ソースに対する FormDataSource オブジェクトを参照し、CustTrans\_ds.executeQuery() は CustTrans データ ソースの FormDataSource.executeQuery メソッドを実行します。 いくつかの FormDataSource メソッドは、FormObjectSet オブジェクトを返します。 このオブジェクトの FormDataSource メソッドで定義されているメソッドを使用するには、FormDataSource オブジェクトに型キャストする必要があります。

## <a name="examples"></a>例

次の例は、自動的に生成されたクエリではなく、フィールドのカスタム クエリを提供します。 これは、フィールドの performFormLookup メソッドをオーバーライドします。

```xpp
public void performFormLookup(FormRun _p1, FormControl _formControl)  
{ 
    FormDataSource formDataSource; 
    QueryRun queryRunGenerated; 
    // The FormDataSource object retrieved from the FormRun parameter. 
    formDataSource = _p1.dataSource(1); 
    // Get the generated query. 
    queryRunGenerated = formDataSource.queryRun(); 
    // Modify the query. 
    // ... 
    // Call the standard implementation of performFormLookup 
    // with the parameters supplied in this method. 
    super(_p1, _formControl); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                                         | 説明                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int active()                                                                                                            | ユーザーが新しいレコードに移動し、現在のレコードとして新しいレコードを設定するときに、結合されたデータ ソースからデータを取得します。                        |
| public boolean allowCheck(\[boolean value\])                                                                                   |                                                                                                                                                          |
| public boolean allowCreate(\[boolean value\])                                                                                  |                                                                                                                                                          |
| public boolean allowDeferredLoad(\[boolean value\])                                                                            |                                                                                                                                                          |
| public boolean allowDelete(\[boolean value\])                                                                                  |                                                                                                                                                          |
| public boolean allowEdit(\[boolean value\])                                                                                    | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                                      |
| public boolean allRowsLoaded()                                                                                                 |                                                                                                                                                          |
| public boolean anyMarked()                                                                                                     | 基になるキャッシュ内のレコードがマークされているかどうかをチェックします。                                                                                           |
| public boolean autoNotify(\[boolean value\])                                                                                   |                                                                                                                                                          |
| public boolean autoQuery(\[boolean value\])                                                                                    |                                                                                                                                                          |
| public boolean autoSearch(\[boolean value\])                                                                                   |                                                                                                                                                          |
| public str bindField(FieldId fieldId)                                                                                          |                                                                                                                                                          |
| public str bindDataMethod(str dataMethodName)                                                                                  |                                                                                                                                                          |
| public boolean cacheAddMethod(str methodName, \[boolean updateOnWrite\])                                                       | キャッシュの指定された表示または編集方法を登録します。                                                                                              |
| public boolean cacheCalculateMethod(str methodName)                                                                            | 指定されたキャッシュされたメソッドを呼び出し、現在のレコードのキャッシュ内の値を更新します。                                                             |
| public boolean cacheOnlyMode(\[boolean value\])                                                                                |                                                                                                                                                          |
| public boolean canCreate()                                                                                                     |                                                                                                                                                          |
| public boolean canDelete()                                                                                                     |                                                                                                                                                          |
| public boolean canEdit()                                                                                                       |                                                                                                                                                          |
| public int clientPageSize(\[int pageSize\])                                                                                    |                                                                                                                                                          |
| public str company(\[str value\])                                                                                              |                                                                                                                                                          |
| public FieldId counterField(\[FieldId value\])                                                                                 |                                                                                                                                                          |
| public boolean crossCompanyAutoQuery(\[boolean value\])                                                                        |                                                                                                                                                          |
| public Common cursor(\[int rowIndex\])                                                                                         | FormObjectSet クラスには機能がありません。                                                                                                         |
| public int defaultMark(\[int value\])                                                                                          | グリッドで選択されたときにレコードがマークされるかどうかを決定する、フォーム内のレコードの既定のマーク値を設定します。                   |
| public boolean delayActive(\[boolean value\])                                                                                  |                                                                                                                                                          |
| public int extends(\[AnyType value\])                                                                                          |                                                                                                                                                          |
| public boolean findRecord(Common record)                                                                                       | データ ソースで指定されたレコードを検索し、それが現在のレコードになります。                                                                           |
| public boolean findValue(FieldId field, str value)                                                                             | データ ソースで指定された値を検索し、そのレコードが FormDataSource.findRecord メソッドを使用する現在のレコードの値を持つようにします。 |
| public boolean positionToRecord(Common record)                                                                                 |                                                                                                                                                          |
| public boolean positionToRecordByValue(FieldId field, str value)                                                               |                                                                                                                                                          |
| public int first()                                                                                                             | データ ソースの最初のレコードにフォーカスを移動します。                                                                                                      |
| public boolean forceWrite(\[boolean value\])                                                                                   |                                                                                                                                                          |
| public FormObject functionObject(str name)                                                                                     |                                                                                                                                                          |
| public FormDataRow getDataRow(\[int rowIndex\], \[boolean allowFetchAhead\])                                                   |                                                                                                                                                          |
| public Common getFirst(\[int mark\], \[boolean fetchAhead\])                                                                   | データ セットの最初のレコードを取得します。                                                                                                                |
| public Common getNext()                                                                                                        | FormDataSource.getFirst メソッドへの以前の呼び出しで設定されている条件に合う次のレコードを返します。                                |
| public int id()                                                                                                                | データ ソースの ID を取得します。                                                                                                                     |
| public IndexId index(\[IndexId value\])                                                                                        |                                                                                                                                                          |
| public boolean insertAtEnd(\[boolean value\])                                                                                  |                                                                                                                                                          |
| public boolean insertIfEmpty(\[boolean value\])                                                                                |                                                                                                                                                          |
| public boolean isBaseDataSource()                                                                                              |                                                                                                                                                          |
| public boolean isInheritanceDataSource()                                                                                       |                                                                                                                                                          |
| private boolean isOptionalRecordCreated(\[boolean set\], Common record, \[boolean value\])                                     |                                                                                                                                                          |
| public boolean isReferenceDataSource()                                                                                         |                                                                                                                                                          |
| public str joinRelation(\[str value\])                                                                                         |                                                                                                                                                          |
| public DictRelation joinRelationAsDictRelation()                                                                               |                                                                                                                                                          |
| public int joinSource(\[AnyType value\])                                                                                       |                                                                                                                                                          |
| public FormDataSource joinSourceDataSource()                                                                                   |                                                                                                                                                          |
| public int last()                                                                                                              | データ ソースの最後のレコードにマウス ポインターを移動します。                                                                                           |
| public boolean leave()                                                                                                         | マウス ポインターが次のレコードまたは別のデータ ソースに移動すると、通知を提供します。                                                      |
| public boolean leaveRecord(\[boolean forceUpdate\])                                                                            | 別のレコードまたはフォームの品目にフォーカスが移動したときに通知を提供します。                                                                        |
| public container resolvePartLinks(\[str relationName\], \[int partTableId\])                                                   |                                                                                                                                                          |
| public int linkType(\[int value\])                                                                                             |                                                                                                                                                          |
| public int mark(\[int value\])                                                                                                 |                                                                                                                                                          |
| public boolean markAllLoadedRecords(\[int value\])                                                                             |                                                                                                                                                          |
| public int markRecord(AnyType record, \[int mark\])                                                                            | 指定されたマーク値を使用して、指定されたレコードをマークします。                                                                                            |
| public boolean markRecords(Array markedRecordIds)                                                                              |                                                                                                                                                          |
| public FormDataSource masterInheritanceDataSource()                                                                            |                                                                                                                                                          |
| public int maxAccessRight(\[int value\])                                                                                       |                                                                                                                                                          |
| public int maxRecordsToLoad(\[int value\])                                                                                     |                                                                                                                                                          |
| public Int64 maxPagingRowCountValue(\[Int64 newValue\])                                                                        |                                                                                                                                                          |
| public str name(\[str value\])                                                                                                 | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。                  |
| public int next()                                                                                                              | データ ソースの次のレコードにフォーカスを移動します。                                                                                                   |
| public int nextPage(int pageSize)                                                                                              | データ ソースで指定した数のレコード (位置変更) を進めます。                                                                                          |
| public int numberOfRowsLoaded(\[boolean redirectToMasterDS\])                                                                  |                                                                                                                                                          |
| public FormDataObject object(FieldId fieldId, \[int arrayIndex\])                                                              | 指定した ID を持つ FormDataObject クラスのインスタンスを返します。                                                                               |
| public boolean onlyFetchActive(\[boolean value\])                                                                              |                                                                                                                                                          |
| public int optionalRecordMode(\[int value\])                                                                                   |                                                                                                                                                          |
| public int pageSize()                                                                                                          |                                                                                                                                                          |
| public boolean pagingEnabled()                                                                                                 |                                                                                                                                                          |
| public TitleFields parentTitleFields(Common record)                                                                            |                                                                                                                                                          |
| public int prev()                                                                                                              | データ ソースの前のレコードにフォーカスを移動します。                                                                                               |
| public int prevPage(int pageSize)                                                                                              | データ ソースで指定した数のレコード分フォーカスを戻します。                                                                                |
| public Query query(\[Query value\])                                                                                            |                                                                                                                                                          |
| public QueryBuildDataSource queryBuildDataSource()                                                                             |                                                                                                                                                          |
| public QueryRun queryRun(\[QueryRun value\])                                                                                   |                                                                                                                                                          |
| public QueryBuildDataSource queryRunQueryBuildDataSource()                                                                     |                                                                                                                                                          |
| public Array recordsMarked()                                                                                                   |                                                                                                                                                          |
| public int startPosition(\[int value\])                                                                                        |                                                                                                                                                          |
| public int startRowIndex()                                                                                                     |                                                                                                                                                          |
| public TableId table(\[TableId value\])                                                                                        | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                                                    |
| public TitleFields titleFields(Common record)                                                                                  |                                                                                                                                                          |
| public int totalNumberOfRows()                                                                                                 |                                                                                                                                                          |
| public boolean validateDelete()                                                                                                | ユーザーがデータ ソースからのレコードの削除を確認することを要求します。                                                                            |
| public boolean validateWrite()                                                                                                 | データが有効で書き込み可能な状態かどうかを判断します。                                                                                                |
| public int validTimeStateAutoQuery(\[int value\])                                                                              |                                                                                                                                                          |
| public int validTimeStateUpdate(\[int value\])                                                                                 |                                                                                                                                                          |
| public void delete()                                                                                                           | データ ソースから現在のレコードを削除します。                                                                                                         |
| public void addFieldToSelectionList(FieldId fieldId)                                                                           |                                                                                                                                                          |
| public void cacheRemoveRecord(\[Common record\])                                                                               | データ ソースの基になるキャッシュから指定されたレコードを削除します。                                                                               |
| private void OnValidatedWrite(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                        |                                                                                                                                                          |
| public void reread()                                                                                                           | データベースから現在のレコードを再読み取りします。                                                                                                            |
| public void rereadJoinHierarchy()                                                                                              |                                                                                                                                                          |
| private void OnRefreshed(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                             |                                                                                                                                                          |
| private void OnValidatedDelete(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                       |                                                                                                                                                          |
| public void markChanged()                                                                                                      |                                                                                                                                                          |
| public void setPagingParameters(boolean pagingEnabled, int startRowIndex, int pageSize)                                        |                                                                                                                                                          |
| public void deleted()                                                                                                          |                                                                                                                                                          |
| public void print(PrintMedium target)                                                                                          | 現在のレコードを印刷します。                                                                                                                               |
| private void OnReread(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                                |                                                                                                                                                          |
| public void research(\[boolean retainPosition\])                                                                               | FormDataSource.research メソッドでオーバーライドされます。                                                                                                     |
| public void createTypes(Map concreteTypesToCreate, \[boolean append\], \[boolean implicitCreate\], \[boolean explicitCreate\]) |                                                                                                                                                          |
| private void OnCreated(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                               |                                                                                                                                                          |
| private void OnQueryExecuted(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                         |                                                                                                                                                          |
| public void written()                                                                                                          |                                                                                                                                                          |
| public void filter(FieldId field, str value)                                                                                   | フィルターはデータ ソースで記録します。                                                                                                                      |
| public void refresh()                                                                                                          | データ ソース内のすべてのレコードのビューを更新してフォームを更新します。                                                                             |
| public void write()                                                                                                            | FormDataSource.validateWrite メソッドを呼び出し、データベースの書き込み操作を管理します。                                                                  |
| public void executeQuery()                                                                                                     | データ ソース クエリを実行し、取得されたレコードを表示します。                                                                              |
| public void setRecord(Common record)                                                                                           |                                                                                                                                                          |
| public void refreshEx(\[AnyType pos\])                                                                                         | 指定されたレコードのビューを更新します。                                                                                                               |
| public void setCurrent()                                                                                                       |                                                                                                                                                          |
| private void OnValidatingDelete(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                      |                                                                                                                                                          |
| public void writing()                                                                                                          |                                                                                                                                                          |
| private void OnWritten(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                               |                                                                                                                                                          |
| public void clearDisplayOption(Common record)                                                                                  | レコードに対して以前に指定された表示オプションをクリアして、レコードを再描画します。                                                          |
| private void OnMarkChanged(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                           |                                                                                                                                                          |
| private void OnLeftRecord(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                            |                                                                                                                                                          |
| private void OnDeleted(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                               |                                                                                                                                                          |
| public void removeFilter()                                                                                                     | データ ソースのクエリをリセットします。                                                                                                                    |
| private void OnInitialized(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                           |                                                                                                                                                          |
| private void OnPostLinkActive(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                        |                                                                                                                                                          |
| private void OnSelectionChanged(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                      |                                                                                                                                                          |
| public void deleting()                                                                                                         |                                                                                                                                                          |
| public void observe()                                                                                                          |                                                                                                                                                          |
| private void OnWriting(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                               |                                                                                                                                                          |
| private void OnActivated(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                             |                                                                                                                                                          |
| public void removeFieldFromSelectionList(FieldId fieldId)                                                                      |                                                                                                                                                          |
| private void OnCreating(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                              |                                                                                                                                                          |
| public void rereadReferenceDataSources()                                                                                       |                                                                                                                                                          |
| private void OnValidatingWrite(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                       |                                                                                                                                                          |
| public void prompt()                                                                                                           | クエリの範囲を制限するために使用される、標準フォーム、SysQueryForm を有効化します。                                                                          |
| private void OnQueryExecuting(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                        |                                                                                                                                                          |
| private void OnInitValue(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                             |                                                                                                                                                          |
| public void clearReferenceData(FieldId fieldId)                                                                                |                                                                                                                                                          |
| public void cursorNotify(int event)                                                                                            | カーソルのイベントに関してアプリケーションに通知します。                                                                                                           |
| public void displayOption(Common record, FormRowDisplayOption options)                                                         | データ ソース内のレコードのテキストの色および背景色を設定します。                                                                            |
| public void create(\[boolean append\])                                                                                         | データ ソースに新しいレコードを作成します                                                                                                                 |
| public void init()                                                                                                             | データソース プロパティに基づくデータソース クエリを作成します。                                                                                 |
| public void linkActive()                                                                                                       | 現在のデータソースにリンクされているデータソースの FormDataSource.exeuteQuery メソッドを呼び出します。                                                  |
| public void selectionChanged()                                                                                                 |                                                                                                                                                          |
| private void OnDeleting(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                              |                                                                                                                                                          |
| public void addReferenceFieldToSelectionList(FieldId fieldId, str referenceFieldGroupName)                                     |                                                                                                                                                          |
| public void initValue()                                                                                                        | 新しいレコードでフィールド値を初期化します。                                                                                                                |
| public void deleteMarked()                                                                                                     | マークされた (選択された) すべてのレコードをデータソースから削除します。                                                                                                |
| private void OnLeavingRecord(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])                                         |                                                                                                                                                          |

## <a name="method-active"></a>メソッド active

ユーザーが新しいレコードに移動し、現在のレコードとして新しいレコードを設定するときに、結合されたデータ ソースからデータを取得します。

```xpp
public int active()
```

### <a name="return-value---active"></a>戻り値 - active

常に 1 を返します。

### <a name="remarks---active"></a>備考 - active

データ ソースの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントしてから [有効] をクリックすると、有効なメソッドをフォーム データ ソースでオーバーライドできます。

## <a name="method-allowcheck"></a>メソッド allowCheck

```xpp
public boolean allowCheck([boolean value])
```

### <a name="parameters---allowcheck"></a>パラメーター - allowCheck

値  

### <a name="return-value---allowcheck"></a>戻り値 - allowCheck

## <a name="method-allowcreate"></a>メソッド allowCreate

```xpp
public boolean allowCreate([boolean value])
```

### <a name="parameters---allowcreate"></a>パラメーター - allowCreate

値  

### <a name="return-value---allowcreate"></a>戻り値 - allowCreate

## <a name="method-allowdeferredload"></a>メソッド allowDeferredLoad

```xpp
public boolean allowDeferredLoad([boolean value])
```

### <a name="parameters---allowdeferredload"></a>パラメーター - allowDeferredLoad

値  

### <a name="return-value---allowdeferredload"></a>戻り値 - allowDeferredLoad

## <a name="method-allowdelete"></a>メソッド allowDelete

```xpp
public boolean allowDelete([boolean value])
```

### <a name="parameters---allowdelete"></a>パラメーター - allowDelete

値  

### <a name="return-value---allowdelete"></a>戻り値 - allowDelete

## <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

コントロールを編集することができる場合は true。それ以外の場合は、false。

### <a name="remarks---allowedit"></a>備考 - allowEdit

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

## <a name="method-allrowsloaded"></a>メソッド allRowsLoaded

```xpp
public boolean allRowsLoaded()
```

### <a name="return-value---allrowsloaded"></a>戻り値 - allRowsLoaded

## <a name="method-anymarked"></a>メソッド anyMarked

基になるキャッシュ内のレコードがマークされているかどうかをチェックします。

```xpp
public boolean anyMarked()
```

### <a name="return-value---anymarked"></a>戻り値 - anyMarked

いずれかのレコードがマークされた場合は true。それ以外の場合は、false。

### <a name="remarks---anymarked"></a>備考 - anyMarked

データ ソース内のレコードは、削除などのアクションとしてマーク (選択) したり、FormDataSource.markedRecord メソッドを使用してコピーできます。

## <a name="method-autonotify"></a>メソッド autoNotify

```xpp
public boolean autoNotify([boolean value])
```

### <a name="parameters---autonotify"></a>パラメーター - autoNotify

値  

### <a name="return-value---autonotify"></a>戻り値 - autoNotify

## <a name="method-autoquery"></a>メソッド autoQuery

```xpp
public boolean autoQuery([boolean value])
```

### <a name="parameters---autoquery"></a>パラメーター - autoQuery

値  

### <a name="return-value---autoquery"></a>戻り値 - autoQuery

## <a name="method-autosearch"></a>メソッド autoSearch

```xpp
public boolean autoSearch([boolean value])
```

### <a name="parameters---autosearch"></a>パラメーター - autoSearch

値  

### <a name="return-value---autosearch"></a>戻り値 - autoSearch

## <a name="method-bindfield"></a>メソッド bindField

```xpp
public str bindField(FieldId fieldId)
```

### <a name="parameters---bindfield"></a>パラメーター - bindField

fieldId  

### <a name="return-value---bindfield"></a>戻り値 - bindField

## <a name="method-binddatamethod"></a>メソッド bindDataMethod

```xpp
public str bindDataMethod(str dataMethodName)
```

### <a name="parameters---binddatamethod"></a>パラメーター - bindDataMethod

dataMethodName  

### <a name="return-value---binddatamethod"></a>戻り値 - bindDataMethod

## <a name="method-cacheaddmethod"></a>メソッド cacheAddMethod

キャッシュの指定された表示または編集方法を登録します。

```xpp
public boolean cacheAddMethod(str methodName, [boolean updateOnWrite])
```

### <a name="parameters---cacheaddmethod"></a>パラメーター - cacheAddMethod

methodName  
レコードが書き込まれたときにキャッシュされた値が自動的に更新されるかどうかを指定するブール値; オプション。

<!-- -->

updateOnWrite  
レコードが書き込まれたときにキャッシュされた値が自動的に更新されるかどうかを指定するブール値; オプション。

### <a name="return-value---cacheaddmethod"></a>戻り値 - cacheAddMethod

メソッドが正常に登録された場合は true。それ以外の場合は、false。

### <a name="remarks---cacheaddmethod"></a>備考 - cacheAddMethod

キャッシュされたメソッドはフェッチされたデータの計算を実行し、計算された値はデータと共にクライアントに渡されます。 計算された値は再読み込み時に更新されます。 既定では、値は書き込みおよび作成時にも更新されます。 このメソッドは、データ ソースの初期化後に、ただし、データがフェッチされる前に呼び出す必要があります。 したがって、このメソッドの呼び出しは、init メソッドの super メソッドを呼び出した後に行う必要があります。 また、updateOnWrite パラメーターは、新しいレコードが作成されたときに表示メソッド値または編集メソッド値を計算してキャッシュするかどうかを決定します。 表示メソッドまたは編集メソッドのキャッシュされた値を手動で更新するには、FormDataSource.cacheCalculateMethod メソッドを呼び出します。 表示または編集キーワードを持つテーブル メソッドのみキャッシュされます。 フォームまたはフォーム データ ソースに記述されているメソッドをキャッシュすることはできません。 表示を登録したり、フォームで使用されていないメソッドを編集しないでください。 これらのメソッドは、値が表示されない場合でも、各レコードに対して計算が行われます。

### <a name="examples---cacheaddmethod"></a>例 - cacheAddMethod

次の例では、VendTransOpen テーブルにキャッシュする 2 つのメソッドを登録します。

```xpp
public void init() 
{ 
    super(); 
    this.cacheAddMethod(tablemethodstr(VendTransOpen, 
        nextCashDiscDate)); 
    this.cacheAddMethod(tablemethodstr(VendTransOpen, 
        nextCashDiscAmount)); 
}
```

## <a name="method-cachecalculatemethod"></a>メソッド cacheCalculateMethod

指定されたキャッシュされたメソッドを呼び出し、現在のレコードのキャッシュ内の値を更新します。

```xpp
public boolean cacheCalculateMethod(str methodName)
```

### <a name="parameters---cachecalculatemethod"></a>パラメーター - cacheCalculateMethod

methodName  
呼び出すテーブル メソッドの名前。

### <a name="return-value---cachecalculatemethod"></a>戻り値 - cacheCalculateMethod

値が更新された場合は true。それ以外の場合は、false。

### <a name="remarks---cachecalculatemethod"></a>備考 - cacheCalculateMethod

キャッシュされた値は、指定されたメソッド名が FormDataSource.cacheAddMethod method メソッドを使用してキャッシュされたメソッドとして以前に登録されている場合にのみ更新されます。 cacheCalculate メソッドは、特定の条件が満たされたときにのみキャッシュされた値を更新する場合に特に便利です。 この場合、FormDataSource.cacheAddMethod メソッドの呼び出しで updateOnWrite パラメーターを false に設定し、データ ソースで書き込みメソッドを使用するなど手動でキャッシュを更新します。

### <a name="examples---cachecalculatemethod"></a>例 - cacheCalculateMethod

次の例では、VendTransOpen テーブルの nextCashDiscDate メソッドと nextCashDiscAmount メソッドを使用して、キャッシュされた値を再計算します。

```xpp
public void write() 
{ 
    super(); 
    vendTransOpen_ds.cacheCalculateMethod(tablemethodstr( 
        VendTransOpen, nextCashDiscDate)); 
    vendTransOpen_ds.cacheCalculateMethod(tablemethodstr( 
        VendTransOpen, nextCashDiscAmount)); 
}
```

## <a name="method-cacheonlymode"></a>メソッド cacheOnlyMode

```xpp
public boolean cacheOnlyMode([boolean value])
```

### <a name="parameters---cacheonlymode"></a>パラメーター - cacheOnlyMode

値  

### <a name="return-value---cacheonlymode"></a>戻り値 - cacheOnlyMode

## <a name="method-cancreate"></a>メソッド canCreate

```xpp
public boolean canCreate()
```

### <a name="return-value---cancreate"></a>戻り値 - canCreate

## <a name="method-candelete"></a>メソッド canDelete

```xpp
public boolean canDelete()
```

### <a name="return-value---candelete"></a>戻り値 - canDelete

## <a name="method-canedit"></a>メソッド canEdit

```xpp
public boolean canEdit()
```

### <a name="return-value---canedit"></a>戻り値 - canEdit

## <a name="method-clientpagesize"></a>メソッド clientPageSize

```xpp
public int clientPageSize([int pageSize])
```

### <a name="parameters---clientpagesize"></a>パラメーター - clientPageSize

pageSize  

### <a name="return-value---clientpagesize"></a>戻り値 - clientPageSize

## <a name="method-company"></a>メソッド company

```xpp
public str company([str value])
```

### <a name="parameters---company"></a>パラメーター - company

値  

### <a name="return-value---company"></a>戻り値 - company

## <a name="method-counterfield"></a>メソッド counterField

```xpp
public FieldId counterField([FieldId value])
```

### <a name="parameters---counterfield"></a>パラメーター - counterField

値  

### <a name="return-value---counterfield"></a>戻り値 - counterField

## <a name="method-crosscompanyautoquery"></a>メソッド crossCompanyAutoQuery

```xpp
public boolean crossCompanyAutoQuery([boolean value])
```

### <a name="parameters---crosscompanyautoquery"></a>パラメーター - crossCompanyAutoQuery

値  

### <a name="return-value---crosscompanyautoquery"></a>戻り値 - crossCompanyAutoQuery

## <a name="method-cursor"></a>メソッド cursor

FormObjectSet クラスには機能がありません。

```xpp
public Common cursor([int rowIndex])
```

### <a name="parameters---cursor"></a>パラメーター - cursor

rowIndex  

### <a name="return-value---cursor"></a>戻り値 - cursor

### <a name="remarks---cursor"></a>備考 - cursor

このメソッドは、データソースによって参照されるテーブル内の現在アクティブなレコードを返す FormDataSource.cursor メソッドによって上書きされます。

## <a name="method-defaultmark"></a>メソッド defaultMark

グリッドで選択されたときにレコードがマークされるかどうかを決定する、フォーム内のレコードの既定のマーク値を設定します。

```xpp
public int defaultMark([int value])
```

### <a name="parameters---defaultmark"></a>パラメーター - defaultMark

値  
フォーム内のレコードの既定のマーク値。 レコードの標準デフォルト マーク値は 1 ですが、この値は value パラメーターを設定することで上書きできます。 0 (ゼロ) 以外の値は、選択されたときにフォームのグリッドでマークされてレコードが表示されます。

### <a name="return-value---defaultmark"></a>戻り値 - defaultMark

フォーム内のレコードの既定のマーク値。

### <a name="remarks---defaultmark"></a>備考 - defaultMark

このメソッドは、グリッド内のすべてのレコードを選択するためにグリッド コントロールの左上隅をクリックすると実行されます。 defaultMark メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] &gt; [defaultMark] を選択します。

## <a name="method-delayactive"></a>メソッド delayActive

```xpp
public boolean delayActive([boolean value])
```

### <a name="parameters---delayactive"></a>パラメーター - delayActive

値  

### <a name="return-value---delayactive"></a>戻り値 - delayActive

## <a name="method-extends"></a>メソッド extends

```xpp
public int extends([AnyType value])
```

### <a name="parameters---extends"></a>パラメーター - extends

値  

### <a name="return-value---extends"></a>戻り値 - extends

## <a name="method-findrecord"></a>メソッド findRecord

データ ソースで指定されたレコードを検索し、それが現在のレコードになります。

```xpp
public boolean findRecord(Common record)
```

### <a name="parameters---findrecord"></a>パラメーター - findRecord

記録  
検索するレコード。

### <a name="return-value---findrecord"></a>戻り値 - findRecord

レコードが見つかった場合は true。それ以外の場合は、false。

### <a name="remarks---findrecord"></a>備考 - findRecord

このメソッドは、FormDataSource.findValue メソッド が呼び出されたときにアクティブになります。 findRecord メソッドは、データソースの下にある [メソッド ノード] を右クリックし、[メソッドの上書き] をポイントしてから、[findRecord] をクリックして、フォーム データ ソース上で上書きできます。

## <a name="method-findvalue"></a>メソッド findValue

データ ソースで指定された値を検索し、そのレコードが FormDataSource.findRecord メソッドを使用する現在のレコードの値を持つようにします。

```xpp
public boolean findValue(FieldId field, str value)
```

### <a name="parameters---findvalue"></a>パラメーター - findValue

 フィールド  
検索する値。

<!-- -->

値  
検索する値。

### <a name="return-value---findvalue"></a>戻り値 - findValue

値が見つかった場合は true。それ以外の場合は、false。

### <a name="remarks---findvalue"></a>備考 - findValue

このメソッドは、ユーザーがフォーム コントロールのショートカット メニューで FindValue をクリックすると呼び出されます。 findValue メソッドは、データソースの下にある [メソッド ノード] を右クリックし、[メソッドの上書き] をポイントしてから、[findValue] をクリックして、フォーム データ ソース上で上書きできます。

### <a name="examples---findvalue"></a>例 - findValue

次の例では、データを変更する前に現在のレコードの ID を格納しています。 更新に失敗した場合、データ ソースは、元のレコードに配置されます。

```xpp
void clicked() 
{ 
    DocuTypeId  docuTypeId; 
    RecId       activeRecId; 
    ; 
     // Store current RecID 
    activeRecId = docuRef.RecId;  
    // Open the Document Type dialog. 
    docuTypeId = smmDocuments::getDocuTypeId(element.args().record()); 
    try 
    { 
        ttsbegin; 
        if (docuTypeId) 
        { 
            // Create a new document record 
            docuRef_ds.create(); 
            docuRef.RefTableId      = tableReference; 
            docuRef.RefRecId        = recReference; 
            docuRef_ds.write(); 
            super(); 
        } 
        ttscommit; 
    } 
    catch 
    { 
        // Focus moved back to original record if there is an error 
        docuRef_ds.executeQuery(); 
        docuRef_ds.findValue(fieldnum(DocuRef,RecId), 
            int642str(activeRecId)); 
    } 
}
```

## <a name="method-positiontorecord"></a>メソッド positionToRecord

```xpp
public boolean positionToRecord(Common record)
```

### <a name="parameters---positiontorecord"></a>パラメーター - positionToRecord

記録  

### <a name="return-value---positiontorecord"></a>戻り値 - positionToRecord

## <a name="method-positiontorecordbyvalue"></a>メソッド positionToRecordByValue

```xpp
public boolean positionToRecordByValue(FieldId field, str value)
```

### <a name="parameters---positiontorecordbyvalue"></a>パラメーター - positionToRecordByValue

 フィールド  

<!-- -->

値  

### <a name="return-value---positiontorecordbyvalue"></a>戻り値 - positionToRecordByValue

## <a name="method-first"></a>メソッド first

データ ソースの最初のレコードにフォーカスを移動します。

```xpp
public int first()
```

### <a name="return-value---first"></a>戻り値 - first

フォーカスが最初のレコードに正常に移動した場合は、ゼロ以外の値。

### <a name="remarks---first"></a>備考 - first

このメソッドは、ユーザーが CTRL+HOME キーを押してフォームの最初のレコードを選択するときに呼び出されます。 最初のメソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [first] をクリックします。

### <a name="examples---first"></a>例 - first

次の例では、InventTrans フォームの InventTransPostingFinancial データソースの最初のメソッドを上書きし、そのフォームで使用されている別のデータ ソースの最後のレコードを返します。

```xpp
int first() 
{ 
    return inventTrans_ds.first(); 
}
```

## <a name="method-forcewrite"></a>メソッド forceWrite

```xpp
public boolean forceWrite([boolean value])
```

### <a name="parameters---forcewrite"></a>パラメーター - forceWrite

値  

### <a name="return-value---forcewrite"></a>戻り値 - forceWrite

## <a name="method-functionobject"></a>メソッド functionObject

```xpp
public FormObject functionObject(str name)
```

### <a name="parameters---functionobject"></a>パラメーター - functionObject

名前  

### <a name="return-value---functionobject"></a>戻り値 - functionObject

## <a name="method-getdatarow"></a>メソッド getDataRow

```xpp
public FormDataRow getDataRow([int rowIndex], [boolean allowFetchAhead])
```

### <a name="parameters---getdatarow"></a>パラメーター - getDataRow

rowIndex  

<!-- -->

allowFetchAhead  

### <a name="return-value---getdatarow"></a>戻り値 - getDataRow

## <a name="method-getfirst"></a>メソッド getFirst

データ セットの最初のレコードを取得します。

```xpp
public Common getFirst([int mark], [boolean fetchAhead])
```

### <a name="parameters---getfirst"></a>パラメーター - getFirst

mark  
ブール値; オプション。 既定値は true です。

<!-- -->

fetchAhead  
ブール値; オプション。 既定値は true です。

### <a name="return-value---getfirst"></a>戻り値 - getFirst

データ セットの最初のレコード。

### <a name="remarks---getfirst"></a>備考 - getFirst

マーク パラメーターがない 0 (ゼロ) の場合、指定した値がマークされている最初のレコードが返され、その後 FormDataSource.getNext メソッドを呼び出すと、マークされたレコードが返されます。 FetchAhead パラメーターが false に設定されている場合は、キャッシュされているレコードだけが返されます。 true に設定され、追加のレコードが検出され、それがキャッシュに追加される場合は、大量のレコード セットで実行される時に、工程に非常に時間がかかる可能性があります。 1 つのグリッド内のレコードが複数選択されると、それらのレコードに値 1 がマークされます。 次の例は、マーク付きレコードまたはマークなしレコードを取得する方法を示しています。 // 最初に取得する recordformDataSource.getFirst();// 2formDataSource.getFirst(2); とマークされた最初に取得するレコード // 1formDataSource.getFirst(1, false); とマークされた最初にキャッシュされたレコード

### <a name="examples---getfirst"></a>例 - getFirst

次の例では、フォーム内で 2 つのレコードが選択されているかどうかを判断します。

```xpp
boolean twoMarked() 
{ 
    SysVersionControlTmpItem tmpitem  = this.getFirst(1); 
    if (!tmpitem) 
    { 
        return false; 
    } 
    tmpitem = this.getNext(); 
    if (!tmpitem) 
    { 
        return false; 
    } 
    tmpitem = this.getNext(); 
    if (!tmpitem) 
    { 
        return true; 
    } 
    return false; 
}
```

## <a name="method-getnext"></a>メソッド getNext

FormDataSource.getFirst メソッドへの以前の呼び出しで設定されている条件に合う次のレコードを返します。

```xpp
public Common getNext()
```

### <a name="return-value---getnext"></a>戻り値 - getNext

データセットの次のレコード。

### <a name="remarks---getnext"></a>備考 - getNext

FormDataSource.getFirst メソッドの呼び出しで実行される初期化によって、getNext メソッドは特定のマーク値を持つレコードのみを返し、キャッシュからレコードを返すことがあります。

### <a name="examples---getnext"></a>例 - getNext

次の例では、フォーム内で 2 つのレコードが選択されているかどうかを判断します。

```xpp
boolean twoMarked() 
{ 
    SysVersionControlTmpItem tmpitem  = this.getFirst(1); 
    if (!tmpitem) 
    { 
        return false; 
    } 
    tmpitem = this.getNext(); 
    if (!tmpitem) 
    { 
        return false; 
    } 
    tmpitem = this.getNext(); 
    if (!tmpitem) 
    { 
        return true; 
    } 
    return false; 
}
```

## <a name="method-id"></a>メソッド id

データ ソースの ID を取得します。

```xpp
public int id()
```

### <a name="return-value---id"></a>戻り値 - id

データ ソースの ID。

### <a name="examples---id"></a>例 - id

次の例では、フォーム データ ソースをデータ ソース ID に変換します。

```xpp
static client DataSourceNumber fds2fdsNo(FormDataSource _fds) 
{ 
    Form  form = _fds.formRun().form(); 
    int   i; 
    for (i=1;i<=form.dataSourceCount();i++) 
    { 
        if (_fds.formRun().dataSource(i).id() == _fds.id()) 
        { 
            return i; 
        } 
    } 
    return 0; 
}
```

## <a name="method-index"></a>メソッド index

```xpp
public IndexId index([IndexId value])
```

### <a name="parameters---index"></a>パラメーター - index

値  

### <a name="return-value---index"></a>戻り値 - index

## <a name="method-insertatend"></a>メソッド insertAtEnd

```xpp
public boolean insertAtEnd([boolean value])
```

### <a name="parameters---insertatend"></a>パラメーター - insertAtEnd

値  

### <a name="return-value---insertatend"></a>戻り値 - insertAtEnd

## <a name="method-insertifempty"></a>メソッド insertIfEmpty

```xpp
public boolean insertIfEmpty([boolean value])
```

### <a name="parameters---insertifempty"></a>パラメーター - insertIfEmpty

値  

### <a name="return-value---insertifempty"></a>戻り値 - insertIfEmpty

## <a name="method-isbasedatasource"></a>メソッド isBaseDataSource

```xpp
public boolean isBaseDataSource()
```

### <a name="return-value---isbasedatasource"></a>戻り値 - isBaseDataSource

## <a name="method-isinheritancedatasource"></a>メソッド isInheritanceDataSource

```xpp
public boolean isInheritanceDataSource()
```

### <a name="return-value---isinheritancedatasource"></a>戻り値 - isInheritanceDataSource

## <a name="method-isoptionalrecordcreated"></a>メソッド isOptionalRecordCreated

```xpp
private boolean isOptionalRecordCreated([boolean set], Common record, [boolean value])
```

### <a name="parameters---isoptionalrecordcreated"></a>パラメーター - isOptionalRecordCreated

set  

<!-- -->

記録  

<!-- -->

値  

### <a name="return-value---isoptionalrecordcreated"></a>戻り値 - isOptionalRecordCreated

## <a name="method-isreferencedatasource"></a>メソッド isReferenceDataSource

```xpp
public boolean isReferenceDataSource()
```

### <a name="return-value---isreferencedatasource"></a>戻り値 - isReferenceDataSource

## <a name="method-joinrelation"></a>メソッド joinRelation

```xpp
public str joinRelation([str value])
```

### <a name="parameters---joinrelation"></a>パラメーター - joinRelation

値  

### <a name="return-value---joinrelation"></a>戻り値 - joinRelation

## <a name="method-joinrelationasdictrelation"></a>メソッド joinRelationAsDictRelation

```xpp
public DictRelation joinRelationAsDictRelation()
```

### <a name="return-value---joinrelationasdictrelation"></a>パラメーター - joinRelationAsDictRelation

## <a name="method-joinsource"></a>メソッド joinSource

```xpp
public int joinSource([AnyType value])
```

### <a name="parameters---joinsource"></a>パラメーター - joinSource

値  

### <a name="return-value---joinsource"></a>戻り値 - joinSource

## <a name="method-joinsourcedatasource"></a>メソッド joinSourceDataSource

```xpp
public FormDataSource joinSourceDataSource()
```

### <a name="return-value---joinsourcedatasource"></a>戻り値 - joinSourceDataSource

## <a name="method-last"></a>メソッド last

データ ソースの最後のレコードにマウス ポインターを移動します。

```xpp
public int last()
```

### <a name="return-value---last"></a>戻り値 - last

マウス ポインターが最後のレコードに正常に移動した場合は、ゼロ以外の値。

### <a name="remarks---last"></a>備考 - last

データ ソースの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントしてから [最後] をクリックすると、最後のメソッドをフォーム データ ソースでオーバーライドできます。

### <a name="examples---last"></a>例 - last

次の例では、WMSOrderTransport フォームの InventDim データ ソースの最後のメソッドを上書きし、フォームで使用されている他のデータ ソースの最後のレコードを返します。

```xpp
int last() 
{ 
    return WMSOrder_ds.last(); 
}
```

## <a name="method-leave"></a>メソッド leave

マウス ポインターが次のレコードまたは別のデータ ソースに移動すると、通知を提供します。

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a>戻り値 - leave

メソッドが上書きされない限り、常に true を返します。

### <a name="remarks---leave"></a>備考 - leave

このメソッドは、レコードレベルの入力検証を実装するために上書きされることがよくあります。 データ ソースの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントしてから [leave] をクリックすると、leave メソッドをフォーム データ ソースで上書きできます。

### <a name="examples---leave"></a>例 - leave

次の例では、現在のレコードが残される前にデータ検証を実行する leave メソッドを上書きします。 データが無効な場合、このメソッドは false を返します。

```xpp
public boolean leave() 
{ 
    boolean ret; 
    ret = super(); 
    if(! salesLine.PBAItemLine::checkMandatory()) 
    { 
        return false; 
    } 
    return ret; 
}
```

## <a name="method-leaverecord"></a>メソッド leaveRecord

別のレコードまたはフォームの品目にフォーカスが移動したときに通知を提供します。

```xpp
public boolean leaveRecord([boolean forceUpdate])
```

### <a name="parameters---leaverecord"></a>パラメーター - leaveRecord

forceUpdate  

### <a name="return-value---leaverecord"></a>戻り値 - leaveRecord

操作が成功する場合は true。それ以外の場合は、false。

### <a name="remarks---leaverecord"></a>備考 - leaveRecord

メソッドが失敗する可能性があり、変更の検証や書き込みができない場合は false を返します。 このメソッドをオーバーライドすることをお勧めします。 代わりに、FormDataSource.leave メソッドをオーバーライドします。 LeaveRecord メソッドをオーバーライドする場合は、スーパー メソッドを呼び出し、メソッドのカーネル実装が実行されるかどうかを確認する必要があります。

## <a name="method-resolvepartlinks"></a>メソッド resolvePartLinks

```xpp
public container resolvePartLinks([str relationName], [int partTableId])
```

### <a name="parameters---resolvepartlinks"></a>パラメーター - resolvePartLinks

relationName  

<!-- -->

partTableId  

### <a name="return-value---resolvepartlinks"></a>戻り値 - resolvePartLinks

## <a name="method-linktype"></a>メソッド linkType

```xpp
public int linkType([int value])
```

### <a name="parameters---linktype"></a>パラメーター - linkType

値  

### <a name="return-value---linktype"></a>戻り値 - linkType

## <a name="method-mark"></a>メソッド mark

```xpp
public int mark([int value])
```

### <a name="parameters---mark"></a>パラメーター - mark

値  

### <a name="return-value---mark"></a>戻り値 - mark

## <a name="method-markallloadedrecords"></a>メソッド markAllLoadedRecords

```xpp
public boolean markAllLoadedRecords([int value])
```

### <a name="parameters---markallloadedrecords"></a>パラメーター - markAllLoadedRecords

値  

### <a name="return-value---markallloadedrecords"></a>戻り値 - markAllLoadedRecords

## <a name="method-markrecord"></a>メソッド markRecord

指定されたマーク値を使用して、指定されたレコードをマークします。

```xpp
public int markRecord(AnyType record, [int mark])
```

### <a name="parameters---markrecord"></a>パラメーター - markRecord

記録  
マークされたレコードに関連付けられた値 (オプション)。 0 (ゼロ) 以外の値は、フォームのグリッドでマークされてレコードが表示されます。

<!-- -->

mark  
マークされたレコードに関連付けられた値 (オプション)。 0 (ゼロ) 以外の値は、フォームのグリッドでマークされてレコードが表示されます。

### <a name="return-value---markrecord"></a>戻り値 - markRecord

レコードがマークされている場合はゼロ以外の整数。

### <a name="remarks---markrecord"></a>備考 - markRecord

フォーム外の select 文またはメソッド呼び出しを使用してレコードが見つかった場合は、FormDataSource.mark メソッドの代わりにこのメソッドを使用します。

## <a name="method-markrecords"></a>メソッド markRecords

```xpp
public boolean markRecords(Array markedRecordIds)
```

### <a name="parameters---markrecords"></a>パラメーター - markRecords

markedRecordIds  

### <a name="return-value---markrecords"></a>戻り値 - markRecords

## <a name="method-masterinheritancedatasource"></a>メソッド masterInheritanceDataSource

```xpp
public FormDataSource masterInheritanceDataSource()
```

### <a name="return-value---masterinheritancedatasource"></a>戻り値 - masterInheritanceDataSource

## <a name="method-maxaccessright"></a>メソッド maxAccessRight

```xpp
public int maxAccessRight([int value])
```

### <a name="parameters---maxaccessright"></a>パラメーター - maxAccessRight

値  

### <a name="return-value---maxaccessright"></a>戻り値 - maxAccessRight

## <a name="method-maxrecordstoload"></a>メソッド maxRecordsToLoad

```xpp
public int maxRecordsToLoad([int value])
```

### <a name="parameters---maxrecordstoload"></a>パラメーター - maxRecordsToLoad

値  

### <a name="return-value---maxrecordstoload"></a>戻り値 - maxRecordsToLoad

## <a name="method-maxpagingrowcountvalue"></a>メソッド maxPagingRowCountValue

```xpp
public Int64 maxPagingRowCountValue([Int64 newValue])
```

### <a name="parameters---maxpagingrowcountvalue"></a>パラメーター - maxPagingRowCountValue

newValue  

### <a name="return-value---maxpagingrowcountvalue"></a>戻り値 - maxPagingRowCountValue

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  
データ ソースの名前 (オプション)。

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="examples---name"></a>例 - name

次の例では、フォーム データ ソースの QueryBuildDataSource オブジェクトを作成します。 FormDataSource.name メソッドは、QueryBuildDataSource オブジェクトの名前を指定するために使用されます。

```xpp
static client QueryBuildDataSource fds2Qbds(FormDataSource _fds) 
{ 
    Form     form = _fds.formRun().form(); 
    if (_fds.query()  
        && _fds.name()  
        && _fds.query().dataSourceName(_fds.name())) 
    { 
        return _fds.query().dataSourceName(_fds.name()); 
    } 
    // Use the first data source if not found by name. 
    if (_fds.query() && _fds.query().dataSourceNo(1)) 
    { 
        return _fds.query().dataSourceNo(1); 
    } 
    return null; 
}
```

## <a name="method-next"></a>メソッド next

データ ソースの次のレコードにフォーカスを移動します。

```xpp
public int next()
```

### <a name="return-value---next"></a>戻り値 - next

操作が成功した場合はゼロ以外の整数。

### <a name="remarks---next"></a>備考 - next

フォーム データ ソース上では、次のメソッドは上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [next] をクリックします。

### <a name="examples---next"></a>例 - next

次の例では、別のデータ ソースから次のレコードを返すために、データ ソースの next メソッドを上書きします。

```xpp
int next() 
{ 
    return inventTrans_ds.next(); 
}
```

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

## <a name="method-numberofrowsloaded"></a>メソッド numberOfRowsLoaded

```xpp
public int numberOfRowsLoaded([boolean redirectToMasterDS])
```

### <a name="parameters---numberofrowsloaded"></a>パラメーター - numberOfRowsLoaded

redirectToMasterDS  

### <a name="return-value---numberofrowsloaded"></a>戻り値 - numberOfRowsLoaded

## <a name="method-object"></a>メソッド object

指定した ID を持つ FormDataObject クラスのインスタンスを返します。

```xpp
public FormDataObject object(FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---object"></a>パラメーター - object

fieldId  

<!-- -->

arrayIndex  

### <a name="return-value---object"></a>戻り値 - object

objectId パラメーターで指定されている ID を持つ FormDataObject クラスのインスタンス。

### <a name="examples---object"></a>例 - object

次の例では、RepositoryFolder フィールドの FormDataObject オブジェクトを SysVersionControlParameters テーブルに作成し、フィールドの AllowEdit プロパティを true に設定します。

```xpp
public void initFormDatasource(FormDataSource _formDataSource) 
{ 
    FormDataObject dataObject = _formDataSource.object( 
        fieldnum(SysVersionControlParameters, RepositoryFolder)); 
    if (dataObject) 
    { 
        dataObject.allowEdit(true); 
    } 
}
```

## <a name="method-onlyfetchactive"></a>メソッド onlyFetchActive

```xpp
public boolean onlyFetchActive([boolean value])
```

### <a name="parameters---onlyfetchactive"></a>パラメーター - onlyFetchActive

値  

### <a name="return-value---onlyfetchactive"></a>戻り値 - onlyFetchActive

## <a name="method-optionalrecordmode"></a>メソッド optionalRecordMode

```xpp
public int optionalRecordMode([int value])
```

### <a name="parameters---optionalrecordmode"></a>パラメーター - optionalRecordMode

値  

### <a name="return-value---optionalrecordmode"></a>戻り値 - optionalRecordMode

## <a name="method-pagesize"></a>メソッド pageSize

```xpp
public int pageSize()
```

### <a name="return-value---pagesize"></a>戻り値 - pageSize

## <a name="method-pagingenabled"></a>メソッド pagingEnabled

```xpp
public boolean pagingEnabled()
```

### <a name="return-value---pagingenabled"></a>戻り値 - pagingEnabled

## <a name="method-parenttitlefields"></a>メソッド parentTitleFields

```xpp
public TitleFields parentTitleFields(Common record)
```

### <a name="parameters---parenttitlefields"></a>パラメーター - parentTitleFields

記録  

### <a name="return-value---parenttitlefields"></a>戻り値 - parentTitleFields

## <a name="method-prev"></a>メソッド prev

データ ソースの前のレコードにフォーカスを移動します。

```xpp
public int prev()
```

### <a name="return-value---prev"></a>戻り値 - prev

操作が成功した場合はゼロ以外の整数。

### <a name="remarks---prev"></a>備考 - prev

このメソッドを使用すると、データ ソースのレコードを逆順に反復処理できます。 フォーム データ ソース上では、prev メソッドは上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [prev] をクリックします。

### <a name="examples---prev"></a>例 - prev

次の例では、別のデータ ソースから前のレコードを返すために、データ ソースの prev メソッドを上書きします。

```xpp
int prev() 
{ 
    return inventTrans_ds.prev(); 
}
```

## <a name="method-prevpage"></a>メソッド prevPage

データ ソースで指定した数のレコード分フォーカスを戻します。

```xpp
public int prevPage(int pageSize)
```

### <a name="parameters---prevpage"></a>パラメーター - prevPage

pageSize  
戻されるレコードの数。

### <a name="return-value---prevpage"></a>戻り値 - prevPage

操作が成功した場合はゼロ以外の整数。

## <a name="method-query"></a>メソッド query

```xpp
public Query query([Query value])
```

### <a name="parameters---query"></a>パラメーター - query

値  

### <a name="return-value---query"></a>戻り値 - query

## <a name="method-querybuilddatasource"></a>メソッド queryBuildDataSource

```xpp
public QueryBuildDataSource queryBuildDataSource()
```

### <a name="return-value---querybuilddatasource"></a>戻り値 - queryBuildDataSource

## <a name="method-queryrun"></a>メソッド queryRun

```xpp
public QueryRun queryRun([QueryRun value])
```

### <a name="parameters---queryrun"></a>パラメーター - queryRun

値  

### <a name="return-value---queryrun"></a>戻り値 - queryRun

## <a name="method-queryrunquerybuilddatasource"></a>メソッド queryRunQueryBuildDataSource

```xpp
public QueryBuildDataSource queryRunQueryBuildDataSource()
```

### <a name="return-value---queryrunquerybuilddatasource"></a>戻り値 - queryRunQueryBuildDataSource

## <a name="method-recordsmarked"></a>メソッド recordsMarked

```xpp
public Array recordsMarked()
```

### <a name="return-value---recordsmarked"></a>戻り値 - recordsMarked

## <a name="method-startposition"></a>メソッド startPosition

```xpp
public int startPosition([int value])
```

### <a name="parameters---startposition"></a>パラメーター - startPosition

値  

### <a name="return-value---startposition"></a>戻り値 - startPosition

## <a name="method-startrowindex"></a>メソッド startRowIndex

```xpp
public int startRowIndex()
```

### <a name="return-value---startrowindex"></a>戻り値 - startRowIndex

## <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a>パラメーター - table

値  

### <a name="return-value---table"></a>戻り値 - toBlob

オブジェクトに関連付けられたテーブル ID の現在の値。

## <a name="method-titlefields"></a>メソッド titleFields

```xpp
public TitleFields titleFields(Common record)
```

### <a name="parameters---titlefields"></a>パラメーター - titleFields

記録  

### <a name="return-value---titlefields"></a>戻り値 - titleFields

## <a name="method-totalnumberofrows"></a>メソッド totalNumberOfRows

```xpp
public int totalNumberOfRows()
```

### <a name="return-value---totalnumberofrows"></a>戻り値 - totalNumberOfRows

## <a name="method-validatedelete"></a>メソッド validateDelete

ユーザーがデータ ソースからのレコードの削除を確認することを要求します。

```xpp
public boolean validateDelete()
```

### <a name="return-value---validatedelete"></a>戻り値 - validateDelete

削除が正常に実行される場合 true。それ以外の場合は、false。

### <a name="remarks---validatedelete"></a>備考 - validateDelete

このメソッドは、データ ソース テーブルの validateDelete メソッドを呼び出します。 FormDataSource.validateDelete メソッドは、FormDataSource.delete メソッドにより呼び出されます。 必要に応じてカスタムのデータ入力規則のチェックを追加するには、このメソッドを使用します。 データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[validateDelete] をクリックして、validateDelete メソッドを上書きできます。

### <a name="examples---validatedelete"></a>例 - validateDelete

次の例では、super() メソッドを呼び出さずに true を返します。 これは、削除確認メッセージ ボックスの表示を抑制します。

```xpp
public boolean validateDelete() 
{ 
    // Do not display warning dialog. 
    return true; 
}
```

## <a name="method-validatewrite"></a>メソッド validateWrite

データが有効で書き込み可能な状態かどうかを判断します。

```xpp
public boolean validateWrite()
```

### <a name="return-value---validatewrite"></a>戻り値 - validateWrite

データが有効である場合は true を返します。それ以外の場合は、false を返します。

### <a name="remarks---validatewrite"></a>備考 - validateWrite

このメソッドは、FormDataSource.write メソッドから呼び出されます。 False が返される場合は、書き込み操作が中止され、エラー メッセージが表示されます。 データ ソースにカスタム検証ルーチンを追加するには、このメソッドを上書きします。 データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[validateWrite] をクリックして、validateWrite メソッドを上書きできます。 このメソッドで super() メソッドを呼び出すと、データ ソースとして使用されるテーブルの validateWrite メソッドが呼び出されます。 したがって、super() メソッドの戻り値を調べる必要があります。 このメソッドをオーバーライドする場合は、super() メソッドも true を返す場合に true のみを返す必要があります。

## <a name="method-validtimestateautoquery"></a>メソッド validTimeStateAutoQuery

```xpp
public int validTimeStateAutoQuery([int value])
```

### <a name="parameters---validtimestateautoquery"></a>パラメーター - validTimeStateAutoQuery

値  

### <a name="return-value---validtimestateautoquery"></a>戻り値 - validTimeStateAutoQuery

## <a name="method-validtimestateupdate"></a>メソッド validTimeStateUpdate

```xpp
public int validTimeStateUpdate([int value])
```

### <a name="parameters---validtimestateupdate"></a>パラメーター - validTimeStateUpdate

値  

### <a name="return-value---validtimestateupdate"></a>戻り値 - validTimeStateUpdate

## <a name="method-delete"></a>メソッド delete

データ ソースから現在のレコードを削除します。

```xpp
public void delete()
```

### <a name="remarks---delete"></a>備考 - delete

このメソッドは、ユーザーがフォーム内のレコードを削除するときに呼び出されます。 この削除メソッドは、FormDataSource.validateDelete メソッドを呼び出します。 validateDelete メソッドが true を返す場合は、レコードが削除されます。 削除した後、カーソルは、次のレコードに配置されます (存在する場合)。 データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[削除] をクリックして、フォーム データ ソースで削除メソッドを上書きできます。

### <a name="examples---delete"></a>例 - delete

次の例では、SysCompilerOutput フォームの Errors データ ソースの delete メソッドを上書きします。 このメソッドは、エラーを削除した後、コンパイラ出力フォームに表示されるエラーの数を更新します。

```xpp
public void delete() 
{ 
    super(); 
    sysCompilerOutput.updateCounters(); 
}
```

## <a name="method-addfieldtoselectionlist"></a>メソッド addFieldToSelectionList

```xpp
public void addFieldToSelectionList(FieldId fieldId)
```

### <a name="parameters---addfieldtoselectionlist"></a>パラメーター - addFieldToSelectionList

fieldId  

## <a name="method-cacheremoverecord"></a>メソッド cacheRemoveRecord

データ ソースの基になるキャッシュから指定されたレコードを削除します。

```xpp
public void cacheRemoveRecord([Common record])
```

### <a name="parameters---cacheremoverecord"></a>パラメーター - cacheRemoveRecord

記録  
キャッシュから削除するレコード (オプション)。

### <a name="remarks---cacheremoverecord"></a>備考 - cacheRemoveRecord

Ttsbegin/ttscommit ブロック内のデータ変更ステートメントを囲む必要があります。

### <a name="examples---cacheremoverecord"></a>例 - cacheRemoveRecord

次の例では、データ ソースのキャッシュから inventTable レコードを削除します。

```xpp
void updateCache(container _conItemId) 
{ 
    SetIterator itSetItemId; 
    InventTable inventTable; 
    Set setItemId = new Set(Types::String); 
    setItemId = Set::create(_conItemId); 
    itSetItemId = new SetIterator(setItemId); 
    ttsBegin; 
    while (itSetItemId.more()) 
    { 
        inventTable = InventTable::find(itSetItemId.value()); 
        if(inventTableWithOutReqItem_ds. 
            findRecord(inventTable)) 
            inventTableWithOutReqItem_ds. 
                cacheRemoveRecord(inventTable); 
        itSetItemId.next(); 
    } 
    ttsCommit; 
}
```

## <a name="method-onvalidatedwrite"></a>メソッド OnValidatedWrite

```xpp
private void OnValidatedWrite([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onvalidatedwrite"></a>パラメーター - OnValidatedWrite

sender  

<!-- -->

e  

## <a name="method-reread"></a>メソッド reread

データベースから現在のレコードを再読み取りします。

```xpp
public void reread()
```

### <a name="remarks---reread"></a>備考 - reread

このメソッドを呼び出して、データベースからの最新の変更でレコードを更新します。 reread メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [reread] をクリックします。

### <a name="examples---reread"></a>例 - reread

次の例では、テーブルの更新に使用されるメソッドの一部として reread メソッドを使用しています。

```xpp
void doRefresh() 
{ 
    salesTable_ds.reread(); 
    salesTable_ds.refresh(); 
    salesLine_ds.reread(); 
    salesLine_ds.refresh(); 
    interCompanyPurchSalesReference_ds.executeQuery(); 
}
```

## <a name="method-rereadjoinhierarchy"></a>メソッド rereadJoinHierarchy

```xpp
public void rereadJoinHierarchy()
```

## <a name="method-onrefreshed"></a>メソッド OnRefreshed

```xpp
private void OnRefreshed([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onrefreshed"></a>パラメーター - OnRefreshed

sender  

<!-- -->

e  

## <a name="method-onvalidateddelete"></a>メソッド OnValidatedDelete

```xpp
private void OnValidatedDelete([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onvalidateddelete"></a>パラメーター - OnValidatedDelete

sender  

<!-- -->

e  

## <a name="method-markchanged"></a>メソッド markChanged

```xpp
public void markChanged()
```

## <a name="method-setpagingparameters"></a>メソッド setPagingParameters

```xpp
public void setPagingParameters(boolean pagingEnabled, int startRowIndex, int pageSize)
```

### <a name="parameters---setpagingparameters"></a>パラメーター - setPagingParameters

pagingEnabled  

<!-- -->

startRowIndex  

<!-- -->

pageSize  

## <a name="method-deleted"></a>メソッド deleted

```xpp
public void deleted()
```

## <a name="method-print"></a>メソッド print

現在のレコードを印刷します。

```xpp
public void print(PrintMedium target)
```

### <a name="parameters---print"></a>パラメーター - print

target  
レコードの印刷に使用する印刷メディア。

### <a name="remarks---print"></a>備考 - print

現在のレコードは、システムの自動レポート機能 (レポート ノードにある SysTableReport レポート) を使用して印刷されます。 フォーム データ ソース上では、print メソッドは上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [print] をクリックします。

## <a name="method-onreread"></a>メソッド OnReread

```xpp
private void OnReread([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onreread"></a>パラメーター - OnReread

sender  

<!-- -->

e  

## <a name="method-research"></a>メソッド research

FormDataSource.research メソッドでオーバーライドされます。

```xpp
public void research([boolean retainPosition])
```

### <a name="parameters---research"></a>パラメーター - research

retainPosition  
メソッドの完了後に、グリッド内の位置を維持するかどうかを示すブール値。

### <a name="remarks---research"></a>備考 - research

このメソッドには、FormObjectSet クラスには機能がありません。 現在適用されているフィルターおよびソートで定義されているデータベースの検索を更新する FormDataSource.research メソッドによってオーバーライドされます。

## <a name="method-createtypes"></a>メソッド createTypes

```xpp
public void createTypes(Map concreteTypesToCreate, [boolean append], [boolean implicitCreate], [boolean explicitCreate])
```

### <a name="parameters---createtypes"></a>パラメーター - createTypes

concreteTypesToCreate  

<!-- -->

append  

<!-- -->

implicitCreate  

<!-- -->

explicitCreate  

## <a name="method-oncreated"></a>メソッド OnCreated

```xpp
private void OnCreated([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---oncreated"></a>パラメーター - OnCreated

sender  

<!-- -->

e  

## <a name="method-onqueryexecuted"></a>メソッド OnQueryExecuted

```xpp
private void OnQueryExecuted([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onqueryexecuted"></a>パラメーター - OnQueryExecuted

sender  

<!-- -->

e  

## <a name="method-written"></a>メソッド written

```xpp
public void written()
```

## <a name="method-filter"></a>メソッド filter

フィルターはデータ ソースで記録します。

```xpp
public void filter(FieldId field, str value)
```

### <a name="parameters---filter"></a>パラメーター - filter

 フィールド  
フィルター処理の条件。

<!-- -->

値  
フィルター処理の条件。

### <a name="remarks---filter"></a>備考 - filter

標準フィルター機能を拡張するために、フィルター メソッドをフォーム・データ ソース上で上書きすることができます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [filter] をクリックします。

## <a name="method-refresh"></a>メソッド refresh

データ ソース内のすべてのレコードのビューを更新してフォームを更新します。

```xpp
public void refresh()
```

### <a name="remarks---refresh"></a>備考 - refresh

レコードのコンテンツは、ディスクから読み込まずに再描画されます。 たとえば、時間がかかる処理の実行中に更新する必要がある場合は、最新の情報に更新を使用することができます。 すべてのレコードを最新の情報に更新しない場合は、FormDataSource.refreshEx メソッドを使用します。 refresh メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [refresh] をクリックします。

### <a name="examples---refresh"></a>例 - refresh

次の例では、データ ソースの write メソッドを上書きして、書き込み操作後に別のデータ ソースのレコードを更新します。

```xpp
public void write() 
{ 
    super(); 
    EPParameters_ds.research(); 
    EPParameters_ds.refresh(); 
}
```

## <a name="method-write"></a>メソッド write

FormDataSource.validateWrite メソッドを呼び出し、データベースの書き込み操作を管理します。

```xpp
public void write()
```

### <a name="remarks---write"></a>備考 - write

このメソッドは、ユーザーが新しいレコードを挿入するか、既存のレコードを更新するときに呼び出されます。 refreshEx メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [refreshEx] をクリックします。

## <a name="method-executequery"></a>メソッド executeQuery

データ ソース クエリを実行し、取得されたレコードを表示します。

```xpp
public void executeQuery()
```

### <a name="remarks---executequery"></a>備考 - executeQuery

このメソッドは、フォームがデータ表示用に開かれたときに実行されます。 データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[executeQuery] をクリックして、executeQuery メソッドを上書きできます。

### <a name="examples---executequery"></a>例 - executeQuery

次の例では、タブ ページの有効化イベントに応答してデータ ソース クエリを実行します。

```xpp
public void pageActivated() 
{ 
    monday_ds.executeQuery(); 
    super(); 
}
```

## <a name="method-setrecord"></a>メソッド setRecord

```xpp
public void setRecord(Common record)
```

### <a name="parameters---setrecord"></a>パラメーター - setRecord

記録  

## <a name="method-refreshex"></a>メソッド refreshEx

指定されたレコードのビューを更新します。

```xpp
public void refreshEx([AnyType pos])
```

### <a name="parameters---refreshex"></a>パラメーター - refreshEx

pos  
更新するレコードの番号 (オプション)。 -1 の値が指定されている場合は、すべてのレコードが更新されます。 -2 の値が指定されている場合、マークされているすべてのレコードと指定された表示オプションを持つすべてのレコードが更新されます。 既定値は -2 です。

### <a name="remarks---refreshex"></a>備考 - refreshEx

データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[refreshEx] をクリックして、refreshEx メソッドを上書きできます。

## <a name="method-setcurrent"></a>メソッド setCurrent

```xpp
public void setCurrent()
```

## <a name="method-onvalidatingdelete"></a>メソッド OnValidatingDelete

```xpp
private void OnValidatingDelete([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onvalidatingdelete"></a>パラメーター - OnValidatingDelete

sender  

<!-- -->

e  

## <a name="method-writing"></a>メソッド writing

```xpp
public void writing()
```

## <a name="method-onwritten"></a>メソッド OnWritten

```xpp
private void OnWritten([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onwritten"></a>パラメーター - OnWritten

sender  

<!-- -->

e  

## <a name="method-cleardisplayoption"></a>メソッド clearDisplayOption

レコードに対して以前に指定された表示オプションをクリアして、レコードを再描画します。

```xpp
public void clearDisplayOption(Common record)
```

### <a name="parameters---cleardisplayoption"></a>パラメーター - clearDisplayOption

記録  
再振出するレコード。

### <a name="remarks---cleardisplayoption"></a>備考 - clearDisplayOption

表示オプションは、FormDataSource.displayOption メソッドを使用して設定されます。

### <a name="examples---cleardisplayoption"></a>例 - clearDisplayOption

次の例では、データ ソースの最初のレコードを再描画します。

```xpp
public void run() 
{ 
    super(); 
    sysRecordTmpTemplate_ds.clearDisplayOption( 
        sysRecordTmpTemplate_ds.getFirst()); 
}
```

## <a name="method-onmarkchanged"></a>メソッド OnMarkChanged

```xpp
private void OnMarkChanged([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onmarkchanged"></a>パラメーター - OnMarkChanged

sender  

<!-- -->

e  

## <a name="method-onleftrecord"></a>メソッド OnLeftRecord

```xpp
private void OnLeftRecord([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onleftrecord"></a>パラメーター - OnLeftRecord

sender  

<!-- -->

e  

## <a name="method-ondeleted"></a>メソッド OnDeleted

```xpp
private void OnDeleted([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---ondeleted"></a>パラメーター - OnDeleted

sender  

<!-- -->

e  

## <a name="method-removefilter"></a>メソッド removeFilter

データ ソースのクエリをリセットします。

```xpp
public void removeFilter()
```

### <a name="remarks---removefilter"></a>備考 - removeFilter

このメソッドは、ユーザーがフォーム コントロールのショートカット メニューでフィルターのキャンセル コマンドをクリックすると呼び出されます。 removeFilter メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [removeFilter] をクリックします。 たとえば、removeFilter は FormDataSource.init メソッドによって生成された元のクエリに対するすべての変更を削除します。

## <a name="method-oninitialized"></a>メソッド OnInitialized

```xpp
private void OnInitialized([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---oninitialized"></a>パラメーター - OnInitialized

sender  

<!-- -->

e  

## <a name="method-onpostlinkactive"></a>メソッド OnPostLinkActive

```xpp
private void OnPostLinkActive([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onpostlinkactive"></a>パラメーター - OnPostLinkActive

sender  

<!-- -->

e  

## <a name="method-onselectionchanged"></a>メソッド OnSelectionChanged

```xpp
private void OnSelectionChanged([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onselectionchanged"></a>パラメーター - OnSelectionChanged

sender  

<!-- -->

e  

## <a name="method-deleting"></a>メソッド deleting

```xpp
public void deleting()
```

## <a name="method-observe"></a>メソッド observe

```xpp
public void observe()
```

## <a name="method-onwriting"></a>メソッド OnWriting

```xpp
private void OnWriting([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onwriting"></a>パラメーター - OnWriting

sender  

<!-- -->

e  

## <a name="method-onactivated"></a>メソッド OnActivated

```xpp
private void OnActivated([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onactivated"></a>パラメーター - OnActivated

sender  

<!-- -->

e  

## <a name="method-removefieldfromselectionlist"></a>メソッド removeFieldFromSelectionList

```xpp
public void removeFieldFromSelectionList(FieldId fieldId)
```

### <a name="parameters---removefieldfromselectionlist"></a>パラメーター - removeFieldFromSelectionList

fieldId  

## <a name="method-oncreating"></a>メソッド OnCreating

```xpp
private void OnCreating([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---oncreating"></a>パラメーター - OnCreating

sender  

<!-- -->

e  

## <a name="method-rereadreferencedatasources"></a>メソッド rereadReferenceDataSources

```xpp
public void rereadReferenceDataSources()
```

## <a name="method-onvalidatingwrite"></a>メソッド OnValidatingWrite

```xpp
private void OnValidatingWrite([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onvalidatingwrite"></a>パラメーター - OnValidatingWrite

sender  

<!-- -->

e  

## <a name="method-prompt"></a>メソッド prompt

クエリの範囲を制限するために使用される、標準フォーム、SysQueryForm を有効化します。

```xpp
public void prompt()
```

### <a name="remarks---prompt"></a>備考 - prompt

このメソッドは、ユーザーが [コマンド] メニューの [レコードのフィルター] コマンドをクリックするか、CTRL+F3 を押すと呼び出されます。 prompt メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [prompt] をクリックします。

## <a name="method-onqueryexecuting"></a>メソッド OnQueryExecuting

```xpp
private void OnQueryExecuting([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onqueryexecuting"></a>パラメーター - OnQueryExecuting

sender  

<!-- -->

e  

## <a name="method-oninitvalue"></a>メソッド OnInitValue

```xpp
private void OnInitValue([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---oninitvalue"></a>パラメーター - OnInitValue

sender  

<!-- -->

e  

## <a name="method-clearreferencedata"></a>メソッド clearReferenceData

```xpp
public void clearReferenceData(FieldId fieldId)
```

### <a name="parameters---clearreferencedata"></a>パラメーター - clearReferenceData

fieldId  

## <a name="method-cursornotify"></a>メソッド cursorNotify

カーソルのイベントに関してアプリケーションに通知します。

```xpp
public void cursorNotify(int event)
```

### <a name="parameters---cursornotify"></a>パラメーター - cursorNotify

イベント  
カーソルのイベント識別子。 次のテーブルに、利用可能なカーソル イベントを示します。

### <a name="remarks---cursornotify"></a>備考 - cursorNotify

このメソッドは、カーソル イベントのカスタム処理を実装するためにオーバーライドできます。 ただし、必要に応じてイベントを処理するカーネルを有効にするため、super() メソッドが最初に呼び出される必要があります。

## <a name="method-displayoption"></a>メソッド displayOption

データ ソース内のレコードのテキストの色および背景色を設定します。

```xpp
public void displayOption(Common record, FormRowDisplayOption options)
```

### <a name="parameters---displayoption"></a>パラメーター - displayOption

記録  
目的のレコード表示プロパティをカプセル化する FormRowDisplayOption オブジェクト。

<!-- -->

オプション  
目的のレコード表示プロパティをカプセル化する FormRowDisplayOption オブジェクト。

### <a name="remarks---displayoption"></a>備考 - displayOption

このメソッドは、レコードがフォームで表示される前にレコードごとに 1 回実行されます。 displayOption メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [displayOption] をクリックします。

### <a name="examples---displayoption"></a>例 - displayOption

次の例では、displayOption メソッドを上書きして、格納されているプロファイルから表示オプションを設定し、特定のレコードの設定に基づいて背景色を上書きします。

```xpp
public void displayOption(Common _record, FormRowDisplayOption 
    _options) 
{ 
    JmgProfileTable profile; 
    profile = _record; 
    _options.backColor(profile.Color); 
    super(_record, _options); 
}
```

## <a name="method-create"></a>メソッド create

データ ソースに新しいレコードを作成します

```xpp
public void create([boolean append])
```

### <a name="parameters---create"></a>パラメーター - create

append  
現在のカーソル位置の前後にレコードを挿入するかどうかを示すブール値。 true に設定されている場合、現在のレコードの後に新しいレコードが挿入されます。

### <a name="remarks---create"></a>備考 - create

このメソッドは、挿入 (CTRL+N) の既定のショートカット キーを使用するなど、ユーザーがデータ ソースに新しいレコードを作成するときに呼び出されます。 create メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] &gt; [create] を選択します。

## <a name="method-init"></a>メソッド init

データソース プロパティに基づくデータソース クエリを作成します。

```xpp
public void init()
```

### <a name="remarks---init"></a>備考 - init

このメソッドは、フォームが開かれたときに呼び出されます。 メソッドによって生成されたクエリは、フォームに表示するデータをロードするために使用されます。 フォーム データ ソース上では、init メソッドは上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [init] をクリックします。

### <a name="examples---init"></a>例 - init

次の例では、データ ソースのソート順を指定するために、データ ソースの init メソッドを上書きしています。

```xpp
public void init() 
{ 
    super(); 
    this.query().dataSourceTable( 
        tablenum(SysVersionControlTmpItem)).addSortField( 
            fieldnum(SysVersionControlTmpItem, VCSDate), 
        SortOrder::Descending); 
    this.query().dataSourceTable( 
        tablenum(SysVersionControlTmpItem)).addSortField( 
            fieldnum(SysVersionControlTmpItem, VCSTime), 
        SortOrder::Descending); 
    this.query().dataSourceTable( 
        tablenum(SysVersionControlTmpItem)).addSortField( 
            fieldnum(SysVersionControlTmpItem, ChangeNumber), 
        SortOrder::Ascending); 
}
```

## <a name="method-linkactive"></a>メソッド linkActive

現在のデータソースにリンクされているデータソースの FormDataSource.exeuteQuery メソッドを呼び出します。

```xpp
public void linkActive()
```

### <a name="remarks---linkactive"></a>備考 - linkActive

このメソッドは、ユーザーがマスター データ ソースの別のレコードに移動したときに実行されます。 これにより、リンクされたすべてのデータ ソースが更新されます。 親データ ソースの LinkType プロパティが Passive、Delayed、Active に設定されている場合、FormDataSource.active メソッドの super() 呼び出しは、リンクされたすべての子データ ソースで FormDataSource.linkActive メソッドを呼び出します。 linkActive メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [linkActive] をクリックします。

## <a name="method-selectionchanged"></a>メソッド selectionChanged

```xpp
public void selectionChanged()
```

## <a name="method-ondeleting"></a>メソッド OnDeleting

```xpp
private void OnDeleting([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---ondeleting"></a>パラメーター - OnDeleting

sender  

<!-- -->

e  

## <a name="method-addreferencefieldtoselectionlist"></a>メソッド addReferenceFieldToSelectionList

```xpp
public void addReferenceFieldToSelectionList(FieldId fieldId, str referenceFieldGroupName)
```

### <a name="parameters---addreferencefieldtoselectionlist"></a>パラメーター - addReferenceFieldToSelectionList

fieldId  

<!-- -->

referenceFieldGroupName  

## <a name="method-initvalue"></a>メソッド initValue

新しいレコードでフィールド値を初期化します。

```xpp
public void initValue()
```

### <a name="remarks---initvalue"></a>備考 - initValue

このメソッドは、新しいレコードが作成されるときに呼び出されます。 これはフィールドの初期値をレコードに入力します。 initValue メソッドは、データソースの下にある [メソッド ノード] を右クリックし、[メソッドの上書き] をポイントしてから、[initValue] をクリックして、フォーム データ ソース上で上書きできます。

### <a name="examples---initvalue"></a>例 - initValue

次の例では、TaxLimitBase フィールドが特定の値で初期化されるように FormDataSource.initValue を上書きします。

```xpp
public void initValue() 
{ 
    super(); 
    taxTable.TaxLimitBase = TaxLimitBase::InvoiceWithoutVAT; 
}
```

## <a name="method-deletemarked"></a>メソッド deleteMarked

マークされた (選択された) すべてのレコードをデータソースから削除します。

```xpp
public void deleteMarked()
```

### <a name="remarks---deletemarked"></a>備考 - deleteMarked

レコードが選択されていない場合は、FormDataSource.delete メソッドを実行します。 Ctrl + Break キーを押すと、操作が中断されます。 deleteMarked メソッドは、フォーム データ ソースで上書きできます。 データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] &gt; [deleteMarked] を選択します。

### <a name="examples---deletemarked"></a>例 - deleteMarked

次の例では、deleteMarked メソッドを上書きして、マークされたレコードを削除するかどうかをユーザーに確認させます。

```xpp
public void deleteMarked() 
{ 
    if (Box::yesNo("@SYS79428", DialogButton::Yes, "@SYS79319")) 
        super(); 
}
```

## <a name="method-onleavingrecord"></a>メソッド OnLeavingRecord

```xpp
private void OnLeavingRecord([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onleavingrecord"></a>パラメーター - OnLeavingRecord

sender  

<!-- -->

e  

