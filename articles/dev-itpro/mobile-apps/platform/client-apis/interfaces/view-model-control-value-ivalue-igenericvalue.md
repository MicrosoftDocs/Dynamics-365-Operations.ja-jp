---
title: GenericValue タイプ
description: コントロール タイプの一般的な値。
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e5c36f11113a51ff82a8b84e828b3c4468eeabe4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506215"
---
# <a name="genericvalue-type"></a>GenericValue タイプ

[!include [banner](../../../../includes/banner.md)]

コントロール タイプの一般的な値。

### <a name="hierarchy"></a>階層

[値](view-model-control-value-ivalue-ivalue.md) <br>&nbsp;&nbsp;&nbsp;└─ GenericValue <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コンテナー](view-model-control-value-ivalue-igenericvalue.md#container)
* [ジェネリック](view-model-control-value-ivalue-igenericvalue.md#generic)
* [getDataSource](view-model-control-value-ivalue-igenericvalue.md#getdatasource)
* [非表示](view-model-control-value-ivalue-igenericvalue.md#hidden)

### <a name="methods"></a>メソッド

* [applyDesign](view-model-control-value-ivalue-igenericvalue.md#applydesign)
* [dataContext](view-model-control-value-ivalue-igenericvalue.md#datacontext)
* [getDesign](view-model-control-value-ivalue-igenericvalue.md#getdesign)
* [getValue](view-model-control-value-ivalue-igenericvalue.md#getvalue)
* [isEditable](view-model-control-value-ivalue-igenericvalue.md#iseditable)
* [メタデータ](view-model-control-value-ivalue-igenericvalue.md#metadata)
* [親](view-model-control-value-ivalue-igenericvalue.md#parent)
* [ルート](view-model-control-value-ivalue-igenericvalue.md#root)
* [setValue](view-model-control-value-ivalue-igenericvalue.md#setvalue)

### <a name="events"></a>イベント

* [onDataChanged](view-model-control-value-ivalue-igenericvalue.md#ondatachanged)

## <a name="properties"></a>プロパティ

### <a name="container"></a>コンテナー

container: ブール値 (省略可) 

コントロールがコンテナーの場合は true です。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承


### <a name="generic"></a>generic

generic: boolean

コントロールがジェネリックの場合は true です。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) をオーバーライドします。


### <a name="getdatasource"></a>getDataSource

getDataSource: function(): any



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承


### <a name="hidden"></a>hidden

hidden: boolean

コントロールが非常時の場合は true です。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承


## <a name="methods"></a>メソッド

### <a name="applydesign"></a>applyDesign


applyDesign(design: [Design](view-model-ipage-idesign.md)): void

付与されたデザインをコントロールのデザインに適用します。
デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| design|[Design](view-model-ipage-idesign.md)|デザイン プロパティをキーとして含むオブジェクト|

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



### <a name="getvalue"></a>getValue


getValue(): string

コントロールの値を返します。

> [Value](view-model-control-value-ivalue-ivalue.md).[getValue](view-model-control-value-ivalue-ivalue.md#getvalue) から継承

#### <a name="returns-string"></a>文字列を返します



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


metadata(): [ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md)

このコントロールのメタデータ オブジェクトを返します。

> [Value](view-model-control-value-ivalue-ivalue.md).[metadata](view-model-control-value-ivalue-ivalue.md#metadata) から継承
> 
> [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。

#### <a name="returns-valuemetadataview-model-control-value-ivalue-ivaluemetadatamd"></a>[ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md) を返します



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



### <a name="setvalue"></a>setValue


setValue(value: string): void

コントロールの値を設定します。

> [Value](view-model-control-value-ivalue-ivalue.md).[setValue](view-model-control-value-ivalue-ivalue.md#setvalue) から継承


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| 値|string||

#### <a name="returns-void"></a>void を返します

## <a name="events"></a>イベント

### <a name="ondatachanged"></a>onDataChanged

onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;

入力コントロールのデータが変更されたときに発生するイベントです。

> [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承


