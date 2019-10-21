---
title: ControlMetadata タイプ
description: コントロールのメタデータのインターフェイス。 コントロール メタデータをオーバーライドすると、コントロール&#x27;の外観と動作を変更できます。
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
ms.openlocfilehash: f9c6bafd19b44141a169422155ee765492cd22a6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191863"
---
# <a name="controlmetadata-type"></a>ControlMetadata タイプ

[!include [banner](../../../../includes/banner.md)]

コントロールのメタデータのインターフェイス。 コントロール メタデータをオーバーライドすると、コントロールの外観と動作を変更できます。
変更できるプロパティはコントロールによって異なりますが、すべてのコントロールにここに表示される基準のプロパティがあります。

### <a name="hierarchy"></a>階層

ControlMetadata <br>&nbsp;&nbsp;&nbsp;└─ [PageLinkMetadata](view-model-control-pagelink-ipagelink-ipagelinkmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ [ContainerControlMetadata](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ [ImageMetadata](view-model-control-image-iimage-iimagemetadata.md) <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity)
* [BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield)
* [説明](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description)
* [編集可能](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable)
* [ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype)
* [HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext)
* [非表示](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden)
* [ID](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id)
* [ラベル](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label)
* [名前](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name)
* [注文](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order)
* [[タイプ](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type)]

## <a name="properties"></a>プロパティ

### <a name="boundentity"></a>BoundEntity

BoundEntity: 文字列 (オプション) 

コントロールがバインドされるエンティティ。


### <a name="boundfield"></a>BoundField

BoundField: 文字列 (オプション) 




### <a name="description"></a>説明

説明:文字列 (オプション) 

コントロールの説明。


### <a name="editable"></a>編集可能

編集可能: プール値 (省略可) 

コントロールが編集可能かどうかを示すブール値。
コントロールまたはその親が編集可能でない場合は、False です。
コントロールとその親の両方が編集可能な場合、true です。
コントロールまたはその親が編集可能で、もう一方が未定義の場合は true です。
コントロールの編集機能と親の編集機能の両方が未定義の場合は未定義です。


### <a name="exttype"></a>ExtType

ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

拡張されたコントロール タイプです。 E.g. コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。


### <a name="helptext"></a>HelpText

HelpText: 文字列 (オプション) 

コマンドのキーボード ショートカットです。 E.g. 「(Shift + F5)」


### <a name="hidden"></a>非表示

非表示: ブール値 (オプション) 

コントロールを非表示にするかどうかを示すブール値。


### <a name="id"></a>ID

Id: string (オプション) 

コントロールの ID 文字列です。


### <a name="label"></a>ラベル

ラベル: 文字列 (省略可) 

コントロールのラベル。 E.g. 個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。


### <a name="name"></a>氏名

Name: 文字列 (省略可) 

コントロールの名前です。


### <a name="order"></a>注文

注文: 番号 (オプション) 

コントロールがページに表示される順序を示す番号。


### <a name="type"></a>種類

Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

コントロール タイプを示す文字列。


