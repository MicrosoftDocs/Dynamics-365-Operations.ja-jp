---
title: リスト タイプ
description: リスト コントロール タイプ。
author: robinarh
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dd55cea676065165f55ea3cda24a42aee98896ee
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749253"
---
# <a name="list-type"></a>リスト タイプ

[!include [banner](../../../../includes/banner.md)]

リスト コントロール タイプ。
リストは、任意の数の行を含むコントロールです。
各行は、任意の数のコントロールに対するレイアウト用テンプレートに従います。
リストには簡易とカードの 2 つのスタイルがあります。

### <a name="hierarchy"></a>階層

[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ リスト <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [$accessibility](view-model-control-list-ilist-ilist.md#accessibility)
* [DefaultSearchColumn](view-model-control-list-ilist-ilist.md#defaultsearchcolumn)
* [コンテナー](view-model-control-list-ilist-ilist.md#container)
* [emptyListMessage](view-model-control-list-ilist-ilist.md#emptylistmessage)
* [enableMultiSelect](view-model-control-list-ilist-ilist.md#enablemultiselect)
* [ジェネリック](view-model-control-list-ilist-ilist.md#generic)
* [getDataSource](view-model-control-list-ilist-ilist.md#getdatasource)
* [非表示](view-model-control-list-ilist-ilist.md#hidden)
* [hideEmptyListMessage](view-model-control-list-ilist-ilist.md#hideemptylistmessage)
* [imageFields](view-model-control-list-ilist-ilist.md#imagefields)
* [performingRemoteSearch](view-model-control-list-ilist-ilist.md#performingremotesearch)
* [searchQuery](view-model-control-list-ilist-ilist.md#searchquery)

### <a name="methods"></a>メソッド

* [allowsNavigation](view-model-control-list-ilist-ilist.md#allowsnavigation)
* [applyDesign](view-model-control-list-ilist-ilist.md#applydesign)
* [applySearch](view-model-control-list-ilist-ilist.md#applysearch)
* [canPerformRemoteSearch](view-model-control-list-ilist-ilist.md#canperformremotesearch)
* [clearSearch](view-model-control-list-ilist-ilist.md#clearsearch)
* [dataContext](view-model-control-list-ilist-ilist.md#datacontext)
* [getColumnLabel](view-model-control-list-ilist-ilist.md#getcolumnlabel)
* [getControl](view-model-control-list-ilist-ilist.md#getcontrol)
* [getControlById](view-model-control-list-ilist-ilist.md#getcontrolbyid)
* [getControlMetadata](view-model-control-list-ilist-ilist.md#getcontrolmetadata)
* [getControlMetadataById](view-model-control-list-ilist-ilist.md#getcontrolmetadatabyid)
* [getData](view-model-control-list-ilist-ilist.md#getdata)
* [getDesign](view-model-control-list-ilist-ilist.md#getdesign)
* [getListData](view-model-control-list-ilist-ilist.md#getlistdata)
* [getRenderedRows](view-model-control-list-ilist-ilist.md#getrenderedrows)
* [getRowNavigation](view-model-control-list-ilist-ilist.md#getrownavigation)
* [getRowSelectionCount](view-model-control-list-ilist-ilist.md#getrowselectioncount)
* [getRowSelections](view-model-control-list-ilist-ilist.md#getrowselections)
* [getRowTracking](view-model-control-list-ilist-ilist.md#getrowtracking)
* [getSearchColumn](view-model-control-list-ilist-ilist.md#getsearchcolumn)
* [getSearchColumnLabel](view-model-control-list-ilist-ilist.md#getsearchcolumnlabel)
* [getSearchableColumns](view-model-control-list-ilist-ilist.md#getsearchablecolumns)
* [hideSearchBar](view-model-control-list-ilist-ilist.md#hidesearchbar)
* [isEditable](view-model-control-list-ilist-ilist.md#iseditable)
* [loadMetaData](view-model-control-list-ilist-ilist.md#loadmetadata)
* [loadMore](view-model-control-list-ilist-ilist.md#loadmore)
* [メタデータ](view-model-control-list-ilist-ilist.md#metadata)
* [親](view-model-control-list-ilist-ilist.md#parent)
* [performRemoteSearch](view-model-control-list-ilist-ilist.md#performremotesearch)
* [ルート](view-model-control-list-ilist-ilist.md#root)
* [selectSearchColumn](view-model-control-list-ilist-ilist.md#selectsearchcolumn)
* [setRowSections](view-model-control-list-ilist-ilist.md#setrowsections)

### <a name="events"></a>イベント

* [onRowCreate](view-model-control-list-ilist-ilist.md#onrowcreate)
* [onRowSelect](view-model-control-list-ilist-ilist.md#onrowselect)

## <a name="properties"></a>プロパティ

### <a name="accessibility"></a>$accessibility

$accessibility: すべて




### <a name="defaultsearchcolumn"></a>DefaultSearchColumn

DefaultSearchColumn: 文字列




### <a name="container"></a>コンテナー

container: ブール値

コントロールがコンテナーの場合は true です。

> [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[container](view-model-control-container-icontainercontrol-icontainercontrol.md#container) から継承
> 
> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) をオーバーライドします。


### <a name="emptylistmessage"></a>emptyListMessage

emptyListMessage: string

既定の空のリスト メッセージを上書きする設定可能なプロパティ。


### <a name="enablemultiselect"></a>enableMultiSelect

enableMultiSelect: boolean




### <a name="generic"></a>generic

generic: boolean (省略可) 



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承


### <a name="getdatasource"></a>getDataSource

getDataSource: function(): any



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承


### <a name="hidden"></a>hidden

hidden: boolean

コントロールが非常時の場合は true です。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承


### <a name="hideemptylistmessage"></a>hideEmptyListMessage

hideEmptyListMessage: boolean

True で一覧が空である場合、メッセージが表示されません。
このプロパティを設定するには、対応するメタデータ プロパティを configureControl で更新します。


### <a name="imagefields"></a>imageFields

imageFields: any [ ]




### <a name="performingremotesearch"></a>performingRemoteSearch

performingRemoteSearch: boolean




### <a name="searchquery"></a>searchQuery

searchQuery: [value: string]: any




## <a name="methods"></a>メソッド

### <a name="allowsnavigation"></a>allowsNavigation


allowsNavigation(): boolean



#### <a name="returns-boolean"></a>ブール値を返します

### <a name="applydesign"></a>applyDesign


applyDesign(IDesign: [ListDesign](view-model-control-list-ilist-ilistdesign.md)): void

付与されたデザインをコントロールのデザインに適用します。
デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| IDesign|[ListDesign](view-model-control-list-ilist-ilistdesign.md)|デザイン プロパティをキーとして含むオブジェクト|

#### <a name="returns-void"></a>void を返します

### <a name="applysearch"></a>applySearch


applySearch(): void



#### <a name="returns-void"></a>void を返します

### <a name="canperformremotesearch"></a>canPerformRemoteSearch


canPerformRemoteSearch(): boolean



#### <a name="returns-boolean"></a>ブール値を返します

### <a name="clearsearch"></a>clearSearch


clearSearch(): void



#### <a name="returns-void"></a>void を返します

### <a name="datacontext"></a>dataContext


dataContext(): any



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承

#### <a name="returns-any"></a>any を返します

### <a name="getcolumnlabel"></a>getColumnLabel


getColumnLabel(id: string): string




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| id|string||

#### <a name="returns-string"></a>文字列を返します

### <a name="getcontrol"></a>getControl


getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)

コントロールの名前の場合、コントロール インスタンスを返します。

> [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControl](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol) から継承


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| controlName|string|コントロール名|

#### <a name="returns-control"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します



### <a name="getcontrolbyid"></a>getControlById


getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)

コントロールの ID の場合、コントロール インスタンスを返します。

> [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControlById](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid) から継承


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| id|string|コントロール ID|

#### <a name="returns-control"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します



### <a name="getcontrolmetadata"></a>getControlMetadata


getControlMetadata(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| controlName|string||

#### <a name="returns-control"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します

### <a name="getcontrolmetadatabyid"></a>getControlMetadataById


getControlMetadataById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| id|string||

#### <a name="returns-control"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します

### <a name="getdata"></a>getData


getData(): any [ ]



#### <a name="returns-any--"></a>any [ ] を返します

### <a name="getdesign"></a>getDesign


getDesign(): [Design](view-model-ipage-idesign.md)

このコントロールのデザイン オブジェクトを返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承

#### <a name="returns-design"></a>[Design](view-model-ipage-idesign.md) を返します



### <a name="getlistdata"></a>getListData


getListData(): any



#### <a name="returns-any"></a>any を返します

### <a name="getrenderedrows"></a>getRenderedRows


getRenderedRows(): [Row](view-model-control-list-ilist-irow.md) [ ]



#### <a name="returns-row--"></a>[Row](view-model-control-list-ilist-irow.md) [ ] を返します

### <a name="getrownavigation"></a>getRowNavigation


getRowNavigation(row: [Row](view-model-control-list-ilist-irow.md)): Promise &lt;any&gt; &#124; any




#### <a name="parameters"></a>パラメーター

| 氏名 | 型 | 説明 |
| ---- | ---- | ----------- |
|  行 |[Row](view-model-control-list-ilist-irow.md)||

#### <a name="returns-promise-ltanygt-124-any"></a>Promise &lt;any&gt; &#124; any を返します

### <a name="getrowselectioncount"></a>getRowSelectionCount


getRowSelectionCount(): number



#### <a name="returns-number"></a>number を返します

### <a name="getrowselections"></a>getRowSelections


getRowSelections(): string [ ]



#### <a name="returns-string--"></a>string [ ] を返します

### <a name="getrowtracking"></a>getRowTracking


getRowTracking(row: any, index: string): string




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| 行|any||
| 指数|string||

#### <a name="returns-string"></a>文字列を返します

### <a name="getsearchcolumn"></a>getSearchColumn


getSearchColumn(): string



#### <a name="returns-string"></a>文字列を返します

### <a name="getsearchcolumnlabel"></a>getSearchColumnLabel


getSearchColumnLabel(): string



#### <a name="returns-string"></a>文字列を返します

### <a name="getsearchablecolumns"></a>getSearchableColumns


getSearchableColumns(): any [ ]



#### <a name="returns-any--"></a>any [ ] を返します

### <a name="hidesearchbar"></a>hideSearchBar


hideSearchBar(): boolean



#### <a name="returns-boolean"></a>ブール値を返します

### <a name="iseditable"></a>isEditable


isEditable(): boolean

コントロールが編集可能かどうかを示すブール値。
コントロールまたはその親が編集可能でない場合は、false を返します。
コントロールとその親の両方が編集可能な場合、true を返します。
コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。
コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="loadmetadata"></a>loadMetaData


loadMetaData(): void



#### <a name="returns-void"></a>void を返します

### <a name="loadmore"></a>loadMore


loadMore(): void



#### <a name="returns-void"></a>void を返します

### <a name="metadata"></a>metadata


metadata(): [ListMetadata](view-model-control-list-ilist-ilistmetadata.md)

このコントロールのメタデータ オブジェクトを返します。

> [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[metadata](view-model-control-container-icontainercontrol-icontainercontrol.md#metadata) をオーバーライドします。

#### <a name="returns-listmetadata"></a>[ListMetadata](view-model-control-list-ilist-ilistmetadata.md) を返します



### <a name="parent"></a>parent


parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)

このコントロールの親 (コントロールまたはページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承

#### <a name="returns-control-124-page"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します



### <a name="performremotesearch"></a>performRemoteSearch


performRemoteSearch(): void



#### <a name="returns-void"></a>void を返します

### <a name="root"></a>root


root(): [Page](view-model-ipage-ipage.md)

このコントロールのルート フォーム インスタンス (ページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承

#### <a name="returns-page"></a>[Page](view-model-ipage-ipage.md) を返します



### <a name="selectsearchcolumn"></a>selectSearchColumn


selectSearchColumn(column: string): void




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| column|string||

#### <a name="returns-void"></a>void を返します

### <a name="setrowsections"></a>setRowSections


setRowSections(selections: string [ ]): void




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| 選択内容|string [ ]||

#### <a name="returns-void"></a>void を返します

## <a name="events"></a>イベント

### <a name="onrowcreate"></a>onRowCreate

onRowCreate: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;




### <a name="onrowselect"></a>onRowSelect

onRowSelect: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;






[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]