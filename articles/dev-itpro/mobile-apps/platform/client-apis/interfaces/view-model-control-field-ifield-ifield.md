---
title: フィールド タイプ
description: フィールド コントロール タイプ。
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5bcf852d59a1d83cbb12c5a88d06e9c69b51fdac
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851599"
---
# <a name="field-type"></a>フィールド タイプ

[!include [banner](../../../../includes/banner.md)]

フィールド コントロール タイプ。

### <a name="hierarchy"></a>階層

[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ フィールド <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コンテナー](view-model-control-field-ifield-ifield.md#container)
* [ジェネリック](view-model-control-field-ifield-ifield.md#generic)
* [getDataSource](view-model-control-field-ifield-ifield.md#getdatasource)
* [非表示](view-model-control-field-ifield-ifield.md#hidden)

### <a name="methods"></a>メソッド

* [applyDesign](view-model-control-field-ifield-ifield.md#applydesign)
* [dataContext](view-model-control-field-ifield-ifield.md#datacontext)
* [getDesign](view-model-control-field-ifield-ifield.md#getdesign)
* [getEditableFormattedValue](view-model-control-field-ifield-ifield.md#geteditableformattedvalue)
* [getEditableValue](view-model-control-field-ifield-ifield.md#geteditablevalue)
* [getEntityRef](view-model-control-field-ifield-ifield.md#getentityref)
* [getFormattedValue](view-model-control-field-ifield-ifield.md#getformattedvalue)
* [getRefLink](view-model-control-field-ifield-ifield.md#getreflink)
* [getValue](view-model-control-field-ifield-ifield.md#getvalue)
* [hasRefLink](view-model-control-field-ifield-ifield.md#hasreflink)
* [hasUnWrapText](view-model-control-field-ifield-ifield.md#hasunwraptext)
* [isEditable](view-model-control-field-ifield-ifield.md#iseditable)
* [メタデータ](view-model-control-field-ifield-ifield.md#metadata)
* [親](view-model-control-field-ifield-ifield.md#parent)
* [ルート](view-model-control-field-ifield-ifield.md#root)
* [setEditableValue](view-model-control-field-ifield-ifield.md#seteditablevalue)

### <a name="events"></a>イベント

* [onDataChanged](view-model-control-field-ifield-ifield.md#ondatachanged)

## <a name="properties"></a>プロパティ

### <a name="container"></a>コンテナー

container: ブール値 (省略可) 

コントロールがコンテナーの場合は true です。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承


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


## <a name="methods"></a>メソッド

### <a name="applydesign"></a>applyDesign


applyDesign(IDesign: [FieldDesign](view-model-control-field-ifield-ifielddesign.md)): void

付与されたデザインをコントロールのデザインに適用します。
デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| IDesign|[FieldDesign](view-model-control-field-ifield-ifielddesign.md)|デザイン プロパティをキーとして含むオブジェクト|

#### <a name="returns-void"></a>void を返します

### <a name="datacontext"></a>dataContext


dataContext(): any



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承

#### <a name="returns-any"></a>any を返します

### <a name="getdesign"></a>getDesign


getDesign(): [Design](view-model-ipage-idesign.md)

このコントロールのデザイン オブジェクトを返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承

#### <a name="returns-designview-model-ipage-idesignmd"></a>[Design](view-model-ipage-idesign.md) を返します



### <a name="geteditableformattedvalue"></a>getEditableFormattedValue


getEditableFormattedValue(): string &#124; number &#124; Date

編集可能なフィールド コントロールの書式設定された10 進法の文字列値を取得します。

#### <a name="returns-string-124-number-124-date"></a>string &#124; number &#124; Date を返します



### <a name="geteditablevalue"></a>getEditableValue


getEditableValue(): string &#124; number &#124; Date

編集可能なフィールド コントロールの値を取得します。

#### <a name="returns-string-124-number-124-date"></a>string &#124; number &#124; Date を返します



### <a name="getentityref"></a>getEntityRef


getEntityRef(): any

コントロールにバインドする entityRef の値を取得します。

#### <a name="returns-any"></a>any を返します
コントロールにバインドする entityRef の値


### <a name="getformattedvalue"></a>getFormattedValue


getFormattedValue(): string

書式設定された 10 進法の文字列値を取得します。

#### <a name="returns-string"></a>文字列を返します



### <a name="getreflink"></a>getRefLink


getRefLink(): [NavigationArgs](view-model-ipage-inavigationargs.md)

参照リンクのナビゲーション オブジェクトを取得します。

#### <a name="returns-navigationargsview-model-ipage-inavigationargsmd"></a>[NavigationArgs](view-model-ipage-inavigationargs.md) を返します



### <a name="getvalue"></a>getValue


getValue(): any

フィールド コントロールの値を取得します。

#### <a name="returns-any"></a>any を返します



### <a name="hasreflink"></a>hasRefLink


hasRefLink(): boolean

フィールドに refLink がある場合は true を返します。それ以外の場合は、false を返します。

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="hasunwraptext"></a>hasUnWrapText


hasUnWrapText(): boolean

コントロールのラップ テキスト プロパティを取得します。

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



### <a name="metadata"></a>metadata


metadata(): [FieldMetadata](view-model-control-field-ifield-ifieldmetadata.md)

このコントロールのメタデータ オブジェクトを返します。

> [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。

#### <a name="returns-fieldmetadataview-model-control-field-ifield-ifieldmetadatamd"></a>[FieldMetadata](view-model-control-field-ifield-ifieldmetadata.md) を返します



### <a name="parent"></a>parent


parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)

このコントロールの親 (コントロールまたはページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd-124-pageview-model-ipage-ipagemd"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します



### <a name="root"></a>root


root(): [Page](view-model-ipage-ipage.md)

このコントロールのルート フォーム インスタンス (ページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承

#### <a name="returns-pageview-model-ipage-ipagemd"></a>[Page](view-model-ipage-ipage.md) を返します



### <a name="seteditablevalue"></a>setEditableValue


setEditableValue(value: string &#124; number &#124; Date): void

編集可能なフィールド コントロールの値を設定します。


#### <a name="parameters"></a>パラメーター

| 氏名 | 型 | 説明 |
| ---- | ---- | ----------- |
| 値|string &#124; number &#124; Date|値|

#### <a name="returns-void"></a>void を返します

## <a name="events"></a>イベント

### <a name="ondatachanged"></a>onDataChanged

onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;

入力コントロールのデータが変更されたときに発生するイベントです。

> [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承


