---
title: PageLinkMetadata
description: "Pagelink メタデータ タイプ。"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 4963e65fd1b8e1f42f2f21b7eb8d9ce01de12d08
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="pagelinkmetadata-type"></a>PageLinkMetadata タイプ

[!include [banner](../../../../includes/banner.md)]

Pagelink メタデータ タイプ。

### <a name="hierarchy"></a>階層

[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ PageLinkMetadata <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [BoundEntity](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#boundentity)
* [BoundField](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#boundfield)
* [説明](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#description)
* [編集可能](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#editable)
* [ExcludeContext](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#excludecontext)
* [ExtType](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#exttype)
* [HelpText](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#helptext)
* [非表示](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#hidden)
* [アイコン](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#icon)
* [IconSize](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#iconsize)
* [ID](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#id)
* [ラベル](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#label)
* [名前](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#name)
* [ナビゲーション](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#navigation)
* [注文](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#order)
* [ShowCount](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#showcount)
* [スタイル](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#style)
* [ターゲット](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#target)
* [[タイプ](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#type)]
* [UseDataContext](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#usedatacontext)

### <a name="events"></a>イベント

* [OnNavigate](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#onnavigate)

## <a name="properties"></a>プロパティ

### <a name="boundentity"></a>BoundEntity

BoundEntity: 文字列 (オプション) 

コントロールがバインドされるエンティティ。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承


### <a name="boundfield"></a>BoundField

BoundField: 文字列 (オプション) 



> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承


### <a name="description"></a>説明

説明:文字列 (オプション) 

コントロールの説明。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承


### <a name="editable"></a>編集可能

編集可能: プール値 (省略可) 

コントロールが編集可能かどうかを示すブール値。
コントロールまたはその親が編集可能でない場合は、False です。
コントロールとその親の両方が編集可能な場合、true です。
コントロールまたはその親が編集可能で、もう一方が未定義の場合は true です。
コントロールの編集機能と親の編集機能の両方が未定義の場合は未定義です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承


### <a name="excludecontext"></a>ExcludeContext

ExcludeContext: boolean (オプション) 




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


### <a name="icon"></a>アイコン

アイコン: string (オプション) 

ページリンク コントロールに表示されるアイコンの名前。
次に [利用可能なアイコンの一覧](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/AXSymbolFont) を示します。


### <a name="iconsize"></a>IconSize

IconSize: 番号 (オプション) 

ページリンク コントロールに表示されるアイコンのサイズを決定します。


### <a name="id"></a>ID

Id: string (オプション) 

コントロールの ID 文字列です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承


### <a name="label"></a>ラベル

ラベル: 文字列 (省略可) 

コントロールのラベル。 E.g. 個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承


### <a name="name"></a>氏名

Name: 文字列 (省略可) 

コントロールの名前です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承


### <a name="navigation"></a>ナビゲーション

ナビゲーション: [NavigationArgs](view-model-ipage-inavigationargs.md) (省略可) 

ページリンクのナビゲーション オブジェクト。


### <a name="order"></a>注文

注文: 番号 (オプション) 

コントロールがページに表示される順序を示す番号。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承


### <a name="showcount"></a>ShowCount

ShowCount: ブール値 (省略可) 

True の場合、ターゲット ページのリストに存在するレコードの数を表示します。
このプロパティは、ナビゲーション ターゲットがリスト コントロールに含まれるページである場合にのみ適しています。


### <a name="style"></a>スタイル

スタイル: 文字列 (省略可) 

ページリンク コントロールのビジュアル スタイルを指定します。
オプション:
* 「インライン」: は、アイコン、ラベル インラインと共にコンテナー全体の幅を占めます
* 「ボタン」: は、アイコンの下のラベルと共に、ラベルの必要な幅だけを占めます


### <a name="target"></a>ターゲット

ターゲット: string (省略可) 

ページリンクが選択されたときに移動するターゲット アクションまたはページの名前。


### <a name="type"></a>種類

Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

コントロール タイプを示す文字列。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承


### <a name="usedatacontext"></a>UseDataContext

UseDataContext: boolean (オプション) 




## <a name="events"></a>イベント

### <a name="onnavigate"></a>OnNavigate

OnNavigate: 機能 (ナビゲーション:[NavigationArgs](view-model-ipage-inavigationargs.md) & #124; 文字列): すべて (オプション) 

ナビゲーションがトリガーされたときに発生するイベントです。



