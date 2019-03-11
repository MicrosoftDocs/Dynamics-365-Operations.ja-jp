---
title: InputControl タイプ
description: すべてのコントロールのメソッドと属性を持つ入力コントロール インターフェイス。 入力コントロールは、たとえば新しいコントロールに対するユーザー入力を収集するために通常はタスク ページで使用されます。
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
ms.openlocfilehash: 24965ad43137c2c158db45051fd9561b2393d40e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369542"
---
# <a name="inputcontrol-type"></a>InputControl タイプ

[!include [banner](../../../../includes/banner.md)]

すべてのコントロールのメソッドと属性を持つ入力コントロール インターフェイス。
入力コントロールは、たとえば新しいコントロールに対するユーザー入力を収集するために通常はタスク ページで使用されます。

### <a name="hierarchy"></a>階層

[コントロール](view-model-control-basecontrol-icontrol-icontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ InputControl <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Field](view-model-control-field-ifield-ifield.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ルックアップ](view-model-control-lookup-ilookup-ilookup.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [MultiLookup](view-model-control-lookup-imultilookup-imultilookup.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [値](view-model-control-value-ivalue-ivalue.md) <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コンテナー](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#container)
* [ジェネリック](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#generic)
* [getDataSource](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#getdatasource)
* [非表示](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#hidden)

### <a name="methods"></a>メソッド

* [applyDesign](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#applydesign)
* [dataContext](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#datacontext)
* [getDesign](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#getdesign)
* [isEditable](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#iseditable)
* [メタデータ](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata)
* [親](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#parent)
* [ルート](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#root)

### <a name="events"></a>イベント

* [onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged)

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


metadata(): [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)

このコントロールのメタデータ オブジェクトを返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata) をオーバーライドします。

#### <a name="returns-inputcontrolmetadataview-model-control-basecontrol-iinputcontrol-iinputcontrolmetadatamd"></a>[InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md) を返します



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



## <a name="events"></a>イベント

### <a name="ondatachanged"></a>onDataChanged

onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;

入力コントロールのデータが変更されたときに発生するイベントです。


