---
title: ListMetadata タイプ
description: リスト コントロールのメタデータ。
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
ms.openlocfilehash: aefa6cb362a5eae9f52e3b83cab806261ae655ac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183130"
---
# <a name="listmetadata-type"></a>ListMetadata タイプ

[!include [banner](../../../../includes/banner.md)]

リスト コントロールのメタデータ。

### <a name="hierarchy"></a>階層

[ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ ListMetadata <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [BoundEntity](view-model-control-list-ilist-ilistmetadata.md#boundentity)
* [BoundField](view-model-control-list-ilist-ilistmetadata.md#boundfield)
* [子](view-model-control-list-ilist-ilistmetadata.md#children)
* [説明](view-model-control-list-ilist-ilistmetadata.md#description)
* [DetailsPageAppId](view-model-control-list-ilist-ilistmetadata.md#detailspageappid)
* [DetailsPageId](view-model-control-list-ilist-ilistmetadata.md#detailspageid)
* [編集可能](view-model-control-list-ilist-ilistmetadata.md#editable)
* [EmptyListMessage](view-model-control-list-ilist-ilistmetadata.md#emptylistmessage)
* [ExtType](view-model-control-list-ilist-ilistmetadata.md#exttype)
* [HelpText](view-model-control-list-ilist-ilistmetadata.md#helptext)
* [非表示](view-model-control-list-ilist-ilistmetadata.md#hidden)
* [HideEmptyListMessage](view-model-control-list-ilist-ilistmetadata.md#hideemptylistmessage)
* [HideSearchBar](view-model-control-list-ilist-ilistmetadata.md#hidesearchbar)
* [ID](view-model-control-list-ilist-ilistmetadata.md#id)
* [InfiniteScroll](view-model-control-list-ilist-ilistmetadata.md#infinitescroll)
* [InfiniteScrollPageSize](view-model-control-list-ilist-ilistmetadata.md#infinitescrollpagesize)
* [ラベル](view-model-control-list-ilist-ilistmetadata.md#label)
* [ListStyle](view-model-control-list-ilist-ilistmetadata.md#liststyle)
* [MultiSelect](view-model-control-list-ilist-ilistmetadata.md#multiselect)
* [名前](view-model-control-list-ilist-ilistmetadata.md#name)
* [NonEntityProjection](view-model-control-list-ilist-ilistmetadata.md#nonentityprojection)
* [注文](view-model-control-list-ilist-ilistmetadata.md#order)
* [[タイプ](view-model-control-list-ilist-ilistmetadata.md#type)]

### <a name="methods"></a>メソッド

* [navigationHandler](view-model-control-list-ilist-ilistmetadata.md#navigationhandler)

### <a name="events"></a>イベント

* [OnNavigate](view-model-control-list-ilist-ilistmetadata.md#onnavigate)
* [OnRowSelect](view-model-control-list-ilist-ilistmetadata.md#onrowselect)

## <a name="properties"></a>プロパティ

### <a name="boundentity"></a>BoundEntity

BoundEntity: 文字列 (オプション) 

コントロールがバインドされるエンティティ。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承


### <a name="boundfield"></a>BoundField

BoundField: 文字列 (オプション) 



> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承


### <a name="children"></a>子

子: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) \[ \] (オプション) 

リストの各行に表示されるコントロールのメタデータのリスト。


### <a name="description"></a>説明

説明:文字列 (オプション) 

コントロールの説明。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承


### <a name="detailspageappid"></a>DetailsPageAppId

DetailsPageAppId: 文字列 (省略可) 

リストの各行が移動するページのアプリ ID。


### <a name="detailspageid"></a>DetailsPageId

DetailsPageId: 文字列 (省略可) 

各行が移動するページの ID。


### <a name="editable"></a>編集可能

編集可能: プール値 (省略可) 

コントロールが編集可能かどうかを示すブール値。
コントロールまたはその親が編集可能でない場合は、False です。
コントロールとその親の両方が編集可能な場合、true です。
コントロールまたはその親が編集可能で、もう一方が未定義の場合は true です。
コントロールの編集機能と親の編集機能の両方が未定義の場合は未定義です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承


### <a name="emptylistmessage"></a>EmptyListMessage

EmptyListMessage: 文字列 (省略可) 

設定されている場合、空のリストの既定のメッセージを上書きします。


### <a name="exttype"></a>ExtType

ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

拡張されたコントロール タイプです。 E.g. コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承


### <a name="helptext"></a>HelpText

HelpText: 文字列 (オプション) 

コマンドのキーボード ショートカットです。 E.g. 「(Shift + F5)」

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承


### <a name="hidden"></a>非表示

非表示: ブール値 (オプション) 

コントロールを非表示にするかどうかを示すブール値。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承


### <a name="hideemptylistmessage"></a>HideEmptyListMessage

HideEmptyListMessage: ブール値 (オプション) 

True の場合、空のリストのメッセージは表示されません。


### <a name="hidesearchbar"></a>HideSearchBar

HideSearchBar: ブール値 (オプション) 

True の場合、検索バーが表示されません。


### <a name="id"></a>ID

Id: string (オプション) 

コントロールの ID 文字列です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承


### <a name="infinitescroll"></a>InfiniteScroll

InfiniteScroll: ブール値 (オプション) 

true と設定されている場合は、リストにより無限のスクロールが可能になります。


### <a name="infinitescrollpagesize"></a>InfiniteScrollPageSize

InfiniteScrollPageSize: 番号 (オプション) 

最初に読み込む行の数と、ユーザーが現在表示されている行の終わりに達した後に読み込む行の数。


### <a name="label"></a>ラベル

ラベル: 文字列 (省略可) 

コントロールのラベル。 E.g. 個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承


### <a name="liststyle"></a>ListStyle

ListStyle: 文字列 (省略可) 

リスト テンプレートの種類を決定します。
オプション:
* 「簡易」: 簡易スタイル<br>
* 「カード」: カードのスタイル


### <a name="multiselect"></a>MultiSelect

MultiSelect: ブール値 (省略可) 

True の場合、リストは複数選択リストになります。


### <a name="name"></a>氏名

Name: 文字列 (省略可) 

コントロールの名前です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承


### <a name="nonentityprojection"></a>NonEntityProjection

NonEntityProjection: ブール値 (省略可) 




### <a name="order"></a>注文

注文: 番号 (オプション) 

コントロールがページに表示される順序を示す番号。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承


### <a name="type"></a>種類

Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

コントロール タイプを示す文字列。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承


## <a name="methods"></a>メソッド

### <a name="navigationhandler"></a>navigationHandler
オプション 

navigationHandler(row: [Row](view-model-control-list-ilist-irow.md)): Promise &lt;any&gt; &#124; [NavigationArgs](view-model-ipage-inavigationargs.md)

特定の行のナビゲーションを決定する機能。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
|  行 |[Row](view-model-control-list-ilist-irow.md)|ナビゲーション ハンドラーを取得する行。|

#### <a name="returns-promise-ltanygt-124-navigationargsview-model-ipage-inavigationargsmd"></a>Promise &lt;any&gt; &#124; [NavigationArgs](view-model-ipage-inavigationargs.md) を返します



## <a name="events"></a>イベント

### <a name="onnavigate"></a>OnNavigate

OnNavigate: 機能 (ナビゲーション:[NavigationArgs](view-model-ipage-inavigationargs.md)): すべて (オプション) 

ページリンク コントロールが選択されているときに発生するイベントです。


### <a name="onrowselect"></a>OnRowSelect

OnRowSelect: 機能 (行: [行](view-model-control-list-ilist-irow.md)): 無効 (オプション) 

行が選択されたときに発生するイベントです。


