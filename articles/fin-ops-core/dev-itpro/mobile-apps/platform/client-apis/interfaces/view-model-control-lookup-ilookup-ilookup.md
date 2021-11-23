---
title: 参照タイプ
description: ルックアップ コントロールの種類。 ルックアップは、オプションの一覧からの入力を選択するために使用する入力コントロールです。
author: tonyafehr
ms.date: 08/01/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 9247c26916e5d48bf0d49840d4891fe6d4c31d8a
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781536"
---
# <a name="lookup-type"></a>参照タイプ

[!include [banner](../../../../includes/banner.md)]

ルックアップ コントロールの種類。 ルックアップは、オプションの一覧からの入力を選択するために使用する入力コントロールです。
たとえば、ルックアップは、新しい販売注文に顧客をリンクするときに、顧客を調べるために使用できます。

### <a name="hierarchy"></a>階層

[InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ ルックアップ <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コンテナー](view-model-control-lookup-ilookup-ilookup.md#container)
* [ジェネリック](view-model-control-lookup-ilookup-ilookup.md#generic)
* [getDataSource](view-model-control-lookup-ilookup-ilookup.md#getdatasource)
* [非表示](view-model-control-lookup-ilookup-ilookup.md#hidden)

### <a name="methods"></a>メソッド

* [applyDesign](view-model-control-lookup-ilookup-ilookup.md#applydesign)
* [dataContext](view-model-control-lookup-ilookup-ilookup.md#datacontext)
* [getDesign](view-model-control-lookup-ilookup-ilookup.md#getdesign)
* [getDisplayValue](view-model-control-lookup-ilookup-ilookup.md#getdisplayvalue)
* [getLookupPage](view-model-control-lookup-ilookup-ilookup.md#getlookuppage)
* [getValue](view-model-control-lookup-ilookup-ilookup.md#getvalue)
* [isEditable](view-model-control-lookup-ilookup-ilookup.md#iseditable)
* [メタデータ](view-model-control-lookup-ilookup-ilookup.md#metadata)
* [親](view-model-control-lookup-ilookup-ilookup.md#parent)
* [ルート](view-model-control-lookup-ilookup-ilookup.md#root)
* [setEntityRef](view-model-control-lookup-ilookup-ilookup.md#setentityref)

### <a name="events"></a>イベント

* [onDataChanged](view-model-control-lookup-ilookup-ilookup.md#ondatachanged)

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


applyDesign(IDesign: [LookupDesign](view-model-control-lookup-ilookup-ilookupdesign.md)): void

付与されたデザインをコントロールのデザインに適用します。
デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| IDesign|[LookupDesign](view-model-control-lookup-ilookup-ilookupdesign.md)|デザイン プロパティをキーとして含むオブジェクト|

#### <a name="returns-void"></a>void を返します

### <a name="datacontext"></a>dataContext


dataContext(): any



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承

#### <a name="returns-any"></a>any を返します

### <a name="getdesign"></a>getDesign


getDesign(): [Design](view-model-ipage-idesign.md)

このコントロールのデザイン オブジェクトを返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承

#### <a name="returns-design"></a>[Design](view-model-ipage-idesign.md) を返します



### <a name="getdisplayvalue"></a>getDisplayValue


getDisplayValue(): string



#### <a name="returns-string"></a>文字列を返します

### <a name="getlookuppage"></a>getLookupPage


getLookupPage(): [Page](view-model-ipage-ipage.md)



#### <a name="returns-page"></a>[Page](view-model-ipage-ipage.md) を返します

### <a name="getvalue"></a>getValue


getValue(): string &#124; number



#### <a name="returns-string-124-number"></a>Returns string &#124; number

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


metadata(): [LookupMetadata](view-model-control-lookup-ilookup-ilookupmetadata.md)

このコントロールのメタデータ オブジェクトを返します。

> [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。

#### <a name="returns-lookupmetadata"></a>[LookupMetadata](view-model-control-lookup-ilookup-ilookupmetadata.md) を返します



### <a name="parent"></a>parent


parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)

このコントロールの親 (コントロールまたはページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承

#### <a name="returns-control-124-page"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します



### <a name="root"></a>root


root(): [Page](view-model-ipage-ipage.md)

このコントロールのルート フォーム インスタンス (ページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承

#### <a name="returns-page"></a>[Page](view-model-ipage-ipage.md) を返します



### <a name="setentityref"></a>setEntityRef


setEntityRef(newValue: string &#124; number): Promise &lt;any&gt;




#### <a name="parameters"></a>パラメーター

| 氏名 | 型 | 説明 |
| ---- | ---- | ----------- |
| newValue|string &#124; number||

#### <a name="returns-promise-ltanygt"></a>Promise &lt;any&gt; を返します

## <a name="events"></a>イベント

### <a name="ondatachanged"></a>onDataChanged

onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;

入力コントロールのデータが変更されたときに発生するイベントです。

> [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]