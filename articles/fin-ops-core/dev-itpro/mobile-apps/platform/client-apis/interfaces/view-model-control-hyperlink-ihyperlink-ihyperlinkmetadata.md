---
title: HyperLinkMetadata タイプ
description: HyperLink メタデータ タイプ。
author: jasongre
ms.date: 05/24/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: bbcac7637f3b6cbd32d3964ad289666b0224f99d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276534"
---
# <a name="hyperlinkmetadata-type"></a>HyperLinkMetadata タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

HyperLink メタデータ タイプ。

### <a name="hierarchy"></a>階層

[ValueMetadata](view-model-control-value-ivalue-ivaluemetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ HyperLinkMetadata <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [BoundEntity](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#boundentity)
* [BoundField](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#boundfield)
* [説明](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#description)
* [編集可能](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#editable)
* [ExtType](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#exttype)
* [HelpText](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#helptext)
* [非表示](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#hidden)
* [ID](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#id)
* [ラベル](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#label)
* [必須](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#mandatory)
* [名前](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#name)
* [NumSequence](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#numsequence)
* [注文](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#order)
* [タイプ](view-model-control-hyperlink-ihyperlink-ihyperlinkmetadata.md#type)

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


### <a name="exttype"></a>ExtType

ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

拡張されたコントロール タイプです。 たとえば、コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承


### <a name="helptext"></a>HelpText

HelpText: 文字列 (オプション) 

コマンドのキーボード ショートカットです。 たとえば、「(Shift + F5)」

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承


### <a name="hidden"></a>非表示

非表示: ブール値 (オプション) 

コントロールを非表示にするかどうかを示すブール値。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承


### <a name="id"></a>ID

Id: string (オプション) 

コントロールの ID 文字列です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承


### <a name="label"></a>ラベル

ラベル: 文字列 (省略可) 

コントロールのラベル。 たとえば、個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承


### <a name="mandatory"></a>必須

必須: ブール値 (省略可) 

true と設定されている場合は、コントロールのインプットがタスクを完了するために必要です。
必須のコントロールには、赤いアウトラインがあります。

> [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md).[Mandatory](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#mandatory) から継承


### <a name="name"></a>氏名

Name: 文字列 (省略可) 

コントロールの名前です。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承


### <a name="numsequence"></a>NumSequence

NumSequence: [NumberSequenceConfig](view-model-control-basecontrol-iinputcontrol-inumbersequenceconfig.md) (省略可) 

拡張ビジネス ロジックを使用し、AX 番号シーケンス構成に基づいて、タスクまたはページ内の番号シーケンス コントロールの可視性を自動的に検出および変更するために使用されます。
例 :
```javascript
// hide number sequence reference page from users
metadataService.hideNavigation('numSeqReferencePage');

// parameters to be passed to 'numSequence' flag in configureControl
var configParam = {
     referencePageName: 'numSeqReferencePage',
     dataType: 'HcmPersonnelNumberId'
};

// setup 'PersonnelNumber' control as number sequence in the task 'add-worker'
metadataService.configureControl('add-worker', 'PersonnelNumber', { numSequence: configParam });
```

> [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md).[NumSequence](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#numsequence) から継承


### <a name="order"></a>注文

注文: 番号 (オプション) 

コントロールがページに表示される順序を示す番号。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承


### <a name="type"></a>種類

Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

コントロール タイプを示す文字列。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
