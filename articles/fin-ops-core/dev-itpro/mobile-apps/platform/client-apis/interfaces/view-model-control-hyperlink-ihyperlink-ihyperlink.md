---
title: HyperLink タイプ
description: Hyperlink コントロール タイプ。 ハイパーリンク コントロールは、ハイパーリンクを示すコントロールです。 ほとんどの場合、Pagelinks も使用できます。
author: jasongre
ms.date: 05/24/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: 0a704fec6bdc92518ad69ab2a6379f424b4576d9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267260"
---
# <a name="hyperlink-type"></a>HyperLink タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

Hyperlink コントロール タイプ。 ハイパーリンク コントロールは、ハイパーリンクを示すコントロールです。 ほとんどの場合、Pagelinks も使用できます。

### <a name="hierarchy"></a>階層

[値](view-model-control-value-ivalue-ivalue.md) <br>&nbsp;&nbsp;&nbsp;└─ ハイパーリンク <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コンテナー](view-model-control-hyperlink-ihyperlink-ihyperlink.md#container)
* [ジェネリック](view-model-control-hyperlink-ihyperlink-ihyperlink.md#generic)
* [getDataSource](view-model-control-hyperlink-ihyperlink-ihyperlink.md#getdatasource)
* [非表示](view-model-control-hyperlink-ihyperlink-ihyperlink.md#hidden)

### <a name="methods"></a>メソッド

* [applyDesign](view-model-control-hyperlink-ihyperlink-ihyperlink.md#applydesign)
* [dataContext](view-model-control-hyperlink-ihyperlink-ihyperlink.md#datacontext)
* [getDesign](view-model-control-hyperlink-ihyperlink-ihyperlink.md#getdesign)
* [getHyperLinkValue](view-model-control-hyperlink-ihyperlink-ihyperlink.md#gethyperlinkvalue)
* [getValue](view-model-control-hyperlink-ihyperlink-ihyperlink.md#getvalue)
* [isEditable](view-model-control-hyperlink-ihyperlink-ihyperlink.md#iseditable)
* [isHyperLinkURLPresent](view-model-control-hyperlink-ihyperlink-ihyperlink.md#ishyperlinkurlpresent)
* [メタデータ](view-model-control-hyperlink-ihyperlink-ihyperlink.md#metadata)
* [親](view-model-control-hyperlink-ihyperlink-ihyperlink.md#parent)
* [ルート](view-model-control-hyperlink-ihyperlink-ihyperlink.md#root)
* [setBaseURL](view-model-control-hyperlink-ihyperlink-ihyperlink.md#setbaseurl)
* [setValue](view-model-control-hyperlink-ihyperlink-ihyperlink.md#setvalue)

### <a name="events"></a>イベント

* [onDataChanged](view-model-control-hyperlink-ihyperlink-ihyperlink.md#ondatachanged)

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


applyDesign(IDesign: [HyperLinkDesign](view-model-control-hyperlink-ihyperlink-ihyperlinkdesign.md)): void

付与されたデザインをコントロールのデザインに適用します。
デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| IDesign|[HyperLinkDesign](view-model-control-hyperlink-ihyperlink-ihyperlinkdesign.md)|デザイン プロパティをキーとして含むオブジェクト|

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



### <a name="gethyperlinkvalue"></a>getHyperLinkValue


getHyperLinkValue(): string



#### <a name="returns-string"></a>文字列を返します

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



### <a name="ishyperlinkurlpresent"></a>isHyperLinkURLPresent


isHyperLinkURLPresent(): boolean



#### <a name="returns-boolean"></a>ブール値を返します

### <a name="metadata"></a>metadata


metadata(): [HyperLinkMetadata](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md)

このコントロールのメタデータ オブジェクトを返します。

> [Value](view-model-control-value-ivalue-ivalue.md).[metadata](view-model-control-value-ivalue-ivalue.md#metadata) をオーバーライドします。

#### <a name="returns-hyperlinkmetadata"></a>[HyperLinkMetadata](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md) を返します



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



### <a name="setbaseurl"></a>setBaseURL


setBaseURL(url: string): any




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| URL|string||

#### <a name="returns-any"></a>any を返します

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




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
