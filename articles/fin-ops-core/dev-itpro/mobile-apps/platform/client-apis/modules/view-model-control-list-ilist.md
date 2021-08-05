---
title: リスト モジュール
description: リストは、任意の数の行を含むコントロールです。
author: robinarh
ms.date: 08/01/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.openlocfilehash: 83ef44408903b139dcee27ba94583c82e9fa25c6
ms.sourcegitcommit: ff5e892a91a1585472af2191ae45d6291cceb7f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2021
ms.locfileid: "6661574"
---
# <a name="list-module"></a>リスト モジュール

[!include [banner](../../../../includes/banner.md)]

リストは、任意の数の行を含むコントロールです。
各行は、任意の数のコントロールに対するレイアウト用テンプレートに従います。
リストには簡易とカードの 2 つのスタイルがあります。

## <a name="index"></a>指数

### <a name="types"></a>種類

* [リスト](../interfaces/view-model-control-list-ilist-ilist.md)
* [ListDesign](../interfaces/view-model-control-list-ilist-ilistdesign.md)
* [ListMetadata](../interfaces/view-model-control-list-ilist-ilistmetadata.md)
* [Row](../interfaces/view-model-control-list-ilist-irow.md)

## <a name="types"></a>種類


### <a name="list"></a>リスト

#### <a name="hierarchy"></a>階層

[ContainerControl](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ リスト <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [$accessibility](../interfaces/view-model-control-list-ilist-ilist.md#accessibility) |$accessibility: すべて <br>|  |
| [DefaultSearchColumn](../interfaces/view-model-control-list-ilist-ilist.md#defaultsearchcolumn) |DefaultSearchColumn: 文字列 <br>|  |
| [コンテナー](../interfaces/view-model-control-list-ilist-ilist.md#container) |container: ブール値 <br>|コントロールがコンテナーの場合は true です。<br>  [ContainerControl](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md).[container](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md#container) から継承 <br> [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[container](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#container) をオーバーライドします。 <br> |
| [emptyListMessage](../interfaces/view-model-control-list-ilist-ilist.md#emptylistmessage) |emptyListMessage: string <br>|既定の空のリスト メッセージを上書きする設定可能なプロパティ。<br>  |
| [enableMultiSelect](../interfaces/view-model-control-list-ilist-ilist.md#enablemultiselect) |enableMultiSelect: boolean <br>|  |
| [ジェネリック](../interfaces/view-model-control-list-ilist-ilist.md#generic) |generic: boolean (省略可)  <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[generic](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承 <br> |
| [getDataSource](../interfaces/view-model-control-list-ilist-ilist.md#getdatasource) |getDataSource: function(): any <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承 <br> |
| [非表示](../interfaces/view-model-control-list-ilist-ilist.md#hidden) |hidden: boolean <br>|コントロールが非常時の場合は true です。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承 <br> |
| [hideEmptyListMessage](../interfaces/view-model-control-list-ilist-ilist.md#hideemptylistmessage) |hideEmptyListMessage: boolean <br>|True で一覧が空である場合、メッセージが表示されません。 このプロパティを設定するには、対応するメタデータ プロパティを configureControl で更新します。<br>  |
| [imageFields](../interfaces/view-model-control-list-ilist-ilist.md#imagefields) |imageFields: any [ ] <br>|  |
| [performingRemoteSearch](../interfaces/view-model-control-list-ilist-ilist.md#performingremotesearch) |performingRemoteSearch: boolean <br>|  |
| [searchQuery](../interfaces/view-model-control-list-ilist-ilist.md#searchquery) |searchQuery: [value: string]: any <br>|  |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [allowsNavigation](../interfaces/view-model-control-list-ilist-ilist.md#allowsnavigation) |allowsNavigation(): boolean|  |
| [applyDesign](../interfaces/view-model-control-list-ilist-ilist.md#applydesign) |applyDesign(IDesign: [ListDesign](../interfaces/view-model-control-list-ilist-ilistdesign.md)): void|付与されたデザインをコントロールのデザインに適用します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。 <br> |
| [applySearch](../interfaces/view-model-control-list-ilist-ilist.md#applysearch) |applySearch(): void|  |
| [canPerformRemoteSearch](../interfaces/view-model-control-list-ilist-ilist.md#canperformremotesearch) |canPerformRemoteSearch(): boolean|  |
| [clearSearch](../interfaces/view-model-control-list-ilist-ilist.md#clearsearch) |clearSearch(): void|  |
| [dataContext](../interfaces/view-model-control-list-ilist-ilist.md#datacontext) |dataContext(): any|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承 <br> |
| [getColumnLabel](../interfaces/view-model-control-list-ilist-ilist.md#getcolumnlabel) |getColumnLabel(id: string): string|  |
| [getControl](../interfaces/view-model-control-list-ilist-ilist.md#getcontrol) |getControl(controlName: string): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)|コントロールの名前の場合、コントロール インスタンスを返します。<br>  [ContainerControl](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md).[getControl](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol) から継承 <br> |
| [getControlById](../interfaces/view-model-control-list-ilist-ilist.md#getcontrolbyid) |getControlById(id: string): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)|コントロールの ID の場合、コントロール インスタンスを返します。<br>  [ContainerControl](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md).[getControlById](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid) から継承 <br> |
| [getControlMetadata](../interfaces/view-model-control-list-ilist-ilist.md#getcontrolmetadata) |getControlMetadata(controlName: string): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)|  |
| [getControlMetadataById](../interfaces/view-model-control-list-ilist-ilist.md#getcontrolmetadatabyid) |getControlMetadataById(id: string): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)|  |
| [getData](../interfaces/view-model-control-list-ilist-ilist.md#getdata) |getData(): any [ ]|  |
| [getDesign](../interfaces/view-model-control-list-ilist-ilist.md#getdesign) |getDesign(): [Design](../interfaces/view-model-ipage-idesign.md)|このコントロールのデザイン オブジェクトを返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承 <br> |
| [getListData](../interfaces/view-model-control-list-ilist-ilist.md#getlistdata) |getListData(): any|  |
| [getRenderedRows](../interfaces/view-model-control-list-ilist-ilist.md#getrenderedrows) |getRenderedRows(): [Row](../interfaces/view-model-control-list-ilist-irow.md) [ ]|  |
| [getRowNavigation](../interfaces/view-model-control-list-ilist-ilist.md#getrownavigation) |getRowNavigation(row: [Row](../interfaces/view-model-control-list-ilist-irow.md)): Promise &lt;any&gt; &#124; any|  |
| [getRowSelectionCount](../interfaces/view-model-control-list-ilist-ilist.md#getrowselectioncount) |getRowSelectionCount(): number|  |
| [getRowSelections](../interfaces/view-model-control-list-ilist-ilist.md#getrowselections) |getRowSelections(): string [ ]|  |
| [getRowTracking](../interfaces/view-model-control-list-ilist-ilist.md#getrowtracking) |getRowTracking(row: any, index: string): string|  |
| [getSearchColumn](../interfaces/view-model-control-list-ilist-ilist.md#getsearchcolumn) |getSearchColumn(): string|  |
| [getSearchColumnLabel](../interfaces/view-model-control-list-ilist-ilist.md#getsearchcolumnlabel) |getSearchColumnLabel(): string|  |
| [getSearchableColumns](../interfaces/view-model-control-list-ilist-ilist.md#getsearchablecolumns) |getSearchableColumns(): any [ ]|  |
| [hideSearchBar](../interfaces/view-model-control-list-ilist-ilist.md#hidesearchbar) |hideSearchBar(): boolean|  |
| [isEditable](../interfaces/view-model-control-list-ilist-ilist.md#iseditable) |isEditable(): boolean|コントロールが編集可能かどうかを示すブール値。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承 <br> |
| [loadMetaData](../interfaces/view-model-control-list-ilist-ilist.md#loadmetadata) |loadMetaData(): void|  |
| [loadMore](../interfaces/view-model-control-list-ilist-ilist.md#loadmore) |loadMore(): void|  |
| [メタデータ](../interfaces/view-model-control-list-ilist-ilist.md#metadata) |metadata(): [ListMetadata](../interfaces/view-model-control-list-ilist-ilistmetadata.md)|このコントロールのメタデータ オブジェクトを返します。<br>  [ContainerControl](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md).[metadata](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md#metadata) をオーバーライドします。 <br> |
| [親](../interfaces/view-model-control-list-ilist-ilist.md#parent) |parent(): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールの親 (コントロールまたはページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[parent](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承 <br> |
| [performRemoteSearch](../interfaces/view-model-control-list-ilist-ilist.md#performremotesearch) |performRemoteSearch(): void|  |
| [ルート](../interfaces/view-model-control-list-ilist-ilist.md#root) |root(): [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールのルート フォーム インスタンス (ページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[root](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#root) から継承 <br> |
| [selectSearchColumn](../interfaces/view-model-control-list-ilist-ilist.md#selectsearchcolumn) |selectSearchColumn(column: string): void|  |
| [setRowSections](../interfaces/view-model-control-list-ilist-ilist.md#setrowsections) |setRowSections(selections: string [ ]): void|  |

#### <a name="events"></a>イベント

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [onRowCreate](../interfaces/view-model-control-list-ilist-ilist.md#onrowcreate) |onRowCreate: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;[Row](../interfaces/view-model-control-list-ilist-irow.md)&gt; <br>|  |
| [onRowSelect](../interfaces/view-model-control-list-ilist-ilist.md#onrowselect) |onRowSelect: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;[Row](../interfaces/view-model-control-list-ilist-irow.md)&gt; <br>|  |


### <a name="listdesign"></a>ListDesign

#### <a name="hierarchy"></a>階層

[ContainerControlDesign](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md) <br>&nbsp;&nbsp;&nbsp;└─ ListDesign <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [alignItems](../interfaces/view-model-control-list-ilist-ilistdesign.md#alignitems) |alignItems: string (optional)  <br>|このプロパティは、CSS プロパティ「align-items」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[alignItems](../interfaces/view-model-ipage-idesign.md#alignitems) から継承 <br> |
| [alignSelf](../interfaces/view-model-control-list-ilist-ilistdesign.md#alignself) |alignSelf: string (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[alignSelf](../interfaces/view-model-ipage-idesign.md#alignself) から継承 <br> |
| [allowScroll](../interfaces/view-model-control-list-ilist-ilistdesign.md#allowscroll) |allowScroll: string (optional)  <br>|アイテムがコンテナーの空き領域に収まらないときにコンテナーがスクロールできる場合は true です。 コンテナーにスクロール可能なアイテムがある場合、スクロール領域が入れ子にならないように、このプロパティを false に設定します。<br>  [ContainerControlDesign](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md).[allowScroll](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md#allowscroll) から継承 <br> |
| [バックグラウンド](../interfaces/view-model-control-list-ilist-ilistdesign.md#background) |background: string (optional)  <br>|コンテナーの背景色。<br>  [ContainerControlDesign](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md).[background](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md#background) から継承 <br> |
| [バインディング](../interfaces/view-model-control-list-ilist-ilistdesign.md#bindings) |bindings: any (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[bindings](../interfaces/view-model-ipage-idesign.md#bindings) から継承 <br> |
| [枠線](../interfaces/view-model-control-list-ilist-ilistdesign.md#border) |border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (省略可)  <br>|コントロールの境界動作。 このプロパティは、子によって継承されません。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[border](../interfaces/view-model-ipage-idesign.md#border) から継承 <br> |
| [色](../interfaces/view-model-control-list-ilist-ilistdesign.md#color) |color: string (optional)  <br>|コンテナーの前景色。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[color](../interfaces/view-model-ipage-idesign.md#color) から継承 <br> |
| [デザイン](../interfaces/view-model-control-list-ilist-ilistdesign.md#design) |design: [GroupDesign](../interfaces/view-model-control-group-igroup-igroupdesign.md) (optional)  <br>|各行に適用されるデザイン オブジェクト。<br>  |
| [flexFlow](../interfaces/view-model-control-list-ilist-ilistdesign.md#flexflow) |flexFlow: string (省略可)  <br>|このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexFlow](../interfaces/view-model-ipage-idesign.md#flexflow) から継承 <br> |
| [flexSize](../interfaces/view-model-control-list-ilist-ilistdesign.md#flexsize) |flexSize: string (省略可)  <br>|1 つの番号または 2 つの番号が文字列として書き込まれています。 たとえば、「(サイズを拡大) [(サイズを縮小)]」して、即時フレックス コンテナーの使用可能領域に対応します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexSize](../interfaces/view-model-ipage-idesign.md#flexsize) から継承 <br> |
| [fontSize](../interfaces/view-model-control-list-ilist-ilistdesign.md#fontsize) |fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (省略可)  <br>|比例テキスト サイズ<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontSize](../interfaces/view-model-ipage-idesign.md#fontsize) から継承 <br> |
| [fontWeight](../interfaces/view-model-control-list-ilist-ilistdesign.md#fontweight) |fontWeight: "normal" &#124; "bold" (省略可)  <br>|標準または太字のテキスト。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontWeight](../interfaces/view-model-ipage-idesign.md#fontweight) から継承 <br> |
| [hideArrow](../interfaces/view-model-control-list-ilist-ilistdesign.md#hidearrow) |hideArrow: boolean (省略可)  <br>|既定のスタイル ナビゲーション コントロールの矢印 ( > ) を非表示にするように許可します。<br>  |
| [hideSearchBar](../interfaces/view-model-control-list-ilist-ilistdesign.md#hidesearchbar) |hideSearchBar: boolean (省略可)  <br>|True の場合、検索バーが表示されません。<br>  |
| [itemBorder](../interfaces/view-model-control-list-ilist-ilistdesign.md#itemborder) |itemBorder: "solid" &#124; "none" (省略可)  <br>|True の場合、リストの各行の周りに境界線が表示されます。<br>  [ContainerControlDesign](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md).[itemBorder](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md#itemborder) から継承 <br> |
| [品目](../interfaces/view-model-control-list-ilist-ilistdesign.md#items) |items: string &#124; [Design](../interfaces/view-model-ipage-idesign.md) \[ \] (省略可)  <br>|コンテナーの内部で配置するコンポーネントを含む配列です。<br>  [ContainerControlDesign](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md).[items](../interfaces/view-model-control-container-icontainercontrol-icontainercontroldesign.md#items) から継承 <br> |
| [justifyItems](../interfaces/view-model-control-list-ilist-ilistdesign.md#justifyitems) |justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (省略可)  <br>|このプロパティは CSS プロパティ「justify-content」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[justifyItems](../interfaces/view-model-ipage-idesign.md#justifyitems) から継承 <br> |
| [ラベル](../interfaces/view-model-control-list-ilist-ilistdesign.md#label) |label: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[label](../interfaces/view-model-ipage-idesign.md#label) から継承 <br> |
| [labelPosition](../interfaces/view-model-control-list-ilist-ilistdesign.md#labelposition) |labelPosition: "stacked" &#124; "hidden" &#124; "inline" (省略可)  <br>|ラベルの配置方法を決定します (行われる場合)。 既定では、labelPosition が stacked に設定されています。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[labelPosition](../interfaces/view-model-ipage-idesign.md#labelposition) から継承 <br> |
| [名前](../interfaces/view-model-control-list-ilist-ilistdesign.md#name) |name: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[name](../interfaces/view-model-ipage-idesign.md#name) から継承 <br> |
| [スペース](../interfaces/view-model-control-list-ilist-ilistdesign.md#padding) |padding: "none" &#124; "small" &#124; "std" (省略可)  <br>|コンポーネントのスペース動作を指定できるように許可します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[padding](../interfaces/view-model-ipage-idesign.md#padding) から継承 <br> |
| [タイプ](../interfaces/view-model-control-list-ilist-ilistdesign.md#type) |type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|文字列としてのコントロールのタイプ。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[type](../interfaces/view-model-ipage-idesign.md#type) から継承 <br> |


### <a name="listmetadata"></a>ListMetadata

#### <a name="hierarchy"></a>階層

[ContainerControlMetadata](../interfaces/view-model-control-container-icontainercontrol-icontainercontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ ListMetadata <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [BoundEntity](../interfaces/view-model-control-list-ilist-ilistmetadata.md#boundentity) |BoundEntity: 文字列 (オプション)  <br>|コントロールがバインドされるエンティティ。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承 <br> |
| [BoundField](../interfaces/view-model-control-list-ilist-ilistmetadata.md#boundfield) |BoundField: 文字列 (オプション)  <br>|  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承 <br> |
| [子](../interfaces/view-model-control-list-ilist-ilistmetadata.md#children) |子: [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md) \[ \] (オプション)  <br>|リストの各行に表示されるコントロールのメタデータのリスト。<br>  |
| [説明](../interfaces/view-model-control-list-ilist-ilistmetadata.md#description) |説明:文字列 (オプション)  <br>|コントロールの説明。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承 <br> |
| [DetailsPageAppId](../interfaces/view-model-control-list-ilist-ilistmetadata.md#detailspageappid) |DetailsPageAppId: 文字列 (省略可)  <br>|リストの各行が移動するページのアプリ ID。<br>  |
| [DetailsPageId](../interfaces/view-model-control-list-ilist-ilistmetadata.md#detailspageid) |DetailsPageId: 文字列 (省略可)  <br>|各行が移動するページの ID。<br>  |
| [編集可能](../interfaces/view-model-control-list-ilist-ilistmetadata.md#editable) |編集可能: プール値 (省略可)  <br>|コントロールが編集可能かどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承 <br> |
| [EmptyListMessage](../interfaces/view-model-control-list-ilist-ilistmetadata.md#emptylistmessage) |EmptyListMessage: 文字列 (省略可)  <br>|設定されている場合、空のリストの既定のメッセージを上書きします。<br>  |
| [ExtType](../interfaces/view-model-control-list-ilist-ilistmetadata.md#exttype) |ExtType: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|拡張されたコントロール タイプです。 たとえば、コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承 <br> |
| [HelpText](../interfaces/view-model-control-list-ilist-ilistmetadata.md#helptext) |HelpText: 文字列 (オプション)  <br>|コマンドのキーボード ショートカットです。 たとえば、「(Shift + F5)」<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承 <br> |
| [非表示](../interfaces/view-model-control-list-ilist-ilistmetadata.md#hidden) |非表示: ブール値 (オプション)  <br>|コントロールを非表示にするかどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承 <br> |
| [HideEmptyListMessage](../interfaces/view-model-control-list-ilist-ilistmetadata.md#hideemptylistmessage) |HideEmptyListMessage: ブール値 (オプション)  <br>|True の場合、空のリストのメッセージは表示されません。<br>  |
| [HideSearchBar](../interfaces/view-model-control-list-ilist-ilistmetadata.md#hidesearchbar) |HideSearchBar: ブール値 (オプション)  <br>|True の場合、検索バーが表示されません。<br>  |
| [ID](../interfaces/view-model-control-list-ilist-ilistmetadata.md#id) |Id: string (オプション)  <br>|コントロールの ID 文字列です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承 <br> |
| [InfiniteScroll](../interfaces/view-model-control-list-ilist-ilistmetadata.md#infinitescroll) |InfiniteScroll: ブール値 (オプション)  <br>|true と設定されている場合は、リストにより無限のスクロールが可能になります。<br>  |
| [InfiniteScrollPageSize](../interfaces/view-model-control-list-ilist-ilistmetadata.md#infinitescrollpagesize) |InfiniteScrollPageSize: 番号 (オプション)  <br>|最初に読み込む行の数と、ユーザーが現在表示されている行の終わりに達した後に読み込む行の数。<br>  |
| [ラベル](../interfaces/view-model-control-list-ilist-ilistmetadata.md#label) |ラベル: 文字列 (省略可)  <br>|コントロールのラベル。 たとえば、個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承 <br> |
| [ListStyle](../interfaces/view-model-control-list-ilist-ilistmetadata.md#liststyle) |ListStyle: 文字列 (省略可)  <br>|リスト テンプレートの種類を決定します。<br>  |
| [MultiSelect](../interfaces/view-model-control-list-ilist-ilistmetadata.md#multiselect) |MultiSelect: ブール値 (省略可)  <br>|True の場合、リストは複数選択リストになります。<br>  |
| [名前](../interfaces/view-model-control-list-ilist-ilistmetadata.md#name) |Name: 文字列 (省略可)  <br>|コントロールの名前です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承 <br> |
| [NonEntityProjection](../interfaces/view-model-control-list-ilist-ilistmetadata.md#nonentityprojection) |NonEntityProjection: ブール値 (省略可)  <br>|  |
| [注文](../interfaces/view-model-control-list-ilist-ilistmetadata.md#order) |注文: 番号 (オプション)  <br>|コントロールがページに表示される順序を示す番号。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承 <br> |
| [タイプ](../interfaces/view-model-control-list-ilist-ilistmetadata.md#type) |Type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|コントロール タイプを示す文字列。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承 <br> |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [navigationHandler](../interfaces/view-model-control-list-ilist-ilistmetadata.md#navigationhandler) |オプション navigationHandler(row: [Row](../interfaces/view-model-control-list-ilist-irow.md)): Promise &lt;any&gt; &#124; [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md)|特定の行のナビゲーションを決定する機能。<br>  |

#### <a name="events"></a>イベント

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [OnNavigate](../interfaces/view-model-control-list-ilist-ilistmetadata.md#onnavigate) |OnNavigate: 機能 (ナビゲーション:[NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md)): すべて (オプション)  <br>|ページリンク コントロールが選択されているときに発生するイベントです。<br>  |
| [OnRowSelect](../interfaces/view-model-control-list-ilist-ilistmetadata.md#onrowselect) |OnRowSelect: 機能 (行: [行](../interfaces/view-model-control-list-ilist-irow.md)): 無効 (オプション)  <br>|行が選択されたときに発生するイベントです。<br>  |


### <a name="row"></a>行

#### <a name="hierarchy"></a>階層

行 <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [fieldList](../interfaces/view-model-control-list-ilist-irow.md#fieldlist) |fieldList: [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) [ ] <br>|  |
| [headerField](../interfaces/view-model-control-list-ilist-irow.md#headerfield) |headerField: [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) <br>|  |
| [非表示](../interfaces/view-model-control-list-ilist-irow.md#hidden) |hidden: boolean <br>|True の場合、行が表示されません。<br>  |
| [imageFields](../interfaces/view-model-control-list-ilist-irow.md#imagefields) |imageFields: [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) [ ] <br>|  |
| [isSelected](../interfaces/view-model-control-list-ilist-irow.md#isselected) |isSelected: boolean <br>|  |
| [品目](../interfaces/view-model-control-list-ilist-irow.md#item) |item: any <br>|表示されるデータのコンテナーです。<br>  |
| [テンプレート](../interfaces/view-model-control-list-ilist-irow.md#template) |template: [Group](../interfaces/view-model-control-group-igroup-igroup.md) <br>|行のテンプレートを表すグループ コントロール。<br>  |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [getControl](../interfaces/view-model-control-list-ilist-irow.md#getcontrol) |getControl(controlName: string): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)|  |
| [getControlById](../interfaces/view-model-control-list-ilist-irow.md#getcontrolbyid) |getControlById(id: string): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)|  |
| [getControlValueById](../interfaces/view-model-control-list-ilist-irow.md#getcontrolvaluebyid) |getControlValueById(id: string): string|  |
| [getRowHeader](../interfaces/view-model-control-list-ilist-irow.md#getrowheader) |getRowHeader(): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)|  |
| [getRowId](../interfaces/view-model-control-list-ilist-irow.md#getrowid) |getRowId(): string|  |
| [hasImageField](../interfaces/view-model-control-list-ilist-irow.md#hasimagefield) |hasImageField(): boolean|行に画像フィールドが含まれている場合は、true を返します。<br>  |
| [isEntityCreatedNew](../interfaces/view-model-control-list-ilist-irow.md#isentitycreatednew) |isEntityCreatedNew(): boolean|  |
| [isEntityDeleted](../interfaces/view-model-control-list-ilist-irow.md#isentitydeleted) |isEntityDeleted(): boolean|  |
| [isEntityModified](../interfaces/view-model-control-list-ilist-irow.md#isentitymodified) |isEntityModified(): boolean|  |
| [isEntitySyncPending](../interfaces/view-model-control-list-ilist-irow.md#isentitysyncpending) |isEntitySyncPending(): boolean|  |
| [選択](../interfaces/view-model-control-list-ilist-irow.md#select) |select(): any|  |



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]