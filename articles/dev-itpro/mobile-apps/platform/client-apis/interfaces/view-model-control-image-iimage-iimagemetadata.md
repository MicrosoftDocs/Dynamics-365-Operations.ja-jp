---
title: ImageMetadata タイプ
description: イメージ メタデータの種類。
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
ms.openlocfilehash: 1130185c5e1071ea8d902353792bf272de5c914c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369684"
---
# <a name="imagemetadata-type"></a>ImageMetadata タイプ

[!include [banner](../../../../includes/banner.md)]

イメージ メタデータの種類。

### <a name="hierarchy"></a>階層

[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ ImageMetadata <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [BaseUrl](view-model-control-image-iimage-iimagemetadata.md#baseurl)
* [BoundEntity](view-model-control-image-iimage-iimagemetadata.md#boundentity)
* [BoundField](view-model-control-image-iimage-iimagemetadata.md#boundfield)
* [説明](view-model-control-image-iimage-iimagemetadata.md#description)
* [編集可能](view-model-control-image-iimage-iimagemetadata.md#editable)
* [ExtType](view-model-control-image-iimage-iimagemetadata.md#exttype)
* [高さ](view-model-control-image-iimage-iimagemetadata.md#height)
* [HelpText](view-model-control-image-iimage-iimagemetadata.md#helptext)
* [非表示](view-model-control-image-iimage-iimagemetadata.md#hidden)
* [ID](view-model-control-image-iimage-iimagemetadata.md#id)
* [ImageStyle](view-model-control-image-iimage-iimagemetadata.md#imagestyle)
* [ラベル](view-model-control-image-iimage-iimagemetadata.md#label)
* [名前](view-model-control-image-iimage-iimagemetadata.md#name)
* [注文](view-model-control-image-iimage-iimagemetadata.md#order)
* [[タイプ](view-model-control-image-iimage-iimagemetadata.md#type)]
* [幅](view-model-control-image-iimage-iimagemetadata.md#width)

## <a name="properties"></a>プロパティ

### <a name="baseurl"></a>BaseUrl

BaseUrl: 文字列 (省略可) 

AOTResource タイプ イメージの基準 URL。


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


### <a name="exttype"></a>ExtType

ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

拡張されたコントロール タイプです。 E.g. コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承


### <a name="height"></a>高さ

高さ: 番号 (オプション) 

画像の相対垂直方向。
サイズは CSS 空白サイズとほぼ同じです。


### <a name="helptext"></a>HelpText

HelpText: 文字列 (オプション) 

コマンドのキーボード ショートカットです。 E.g. 「(Shift + F5)」

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承


### <a name="hidden"></a>非表示

非表示: ブール値 (オプション) 

コントロールを非表示にするかどうかを示すブール値。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承


### <a name="id"></a>ID

Id: string (オプション) 

コントロールの ID 文字列です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承


### <a name="imagestyle"></a>ImageStyle

ImageStyle: [ImageStyleType](../modules/view-model-control-image-iimage.md#imagestyletype) (オプション) 

画像のスタイル。


### <a name="label"></a>ラベル

ラベル: 文字列 (省略可) 

コントロールのラベル。 E.g. 個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承


### <a name="name"></a>氏名

Name: 文字列 (省略可) 

コントロールの名前です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承


### <a name="order"></a>注文

注文: 番号 (オプション) 

コントロールがページに表示される順序を示す番号。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承


### <a name="type"></a>種類

Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

コントロール タイプを示す文字列。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承


### <a name="width"></a>幅

幅: 番号 (オプション) 

画像の相対水平方向。
サイズは CSS 空白サイズとほぼ同じです。


