---
title: "LookupMetadata タイプ"
description: "ルックアップ メタデータの種類。"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 265e3bada5090aa2689115332bca6366c3ca31ba
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="lookupmetadata-type"></a>LookupMetadata タイプ

[!include [banner](../../../../includes/banner.md)]

ルックアップ メタデータの種類。

### <a name="hierarchy"></a>階層

[InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ LookupMetadata <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [BoundEntity](view-model-control-lookup-ilookup-ilookupmetadata.md#boundentity)
* [BoundField](view-model-control-lookup-ilookup-ilookupmetadata.md#boundfield)
* [説明](view-model-control-lookup-ilookup-ilookupmetadata.md#description)
* [DisplayField](view-model-control-lookup-ilookup-ilookupmetadata.md#displayfield)
* [DisplayKey](view-model-control-lookup-ilookup-ilookupmetadata.md#displaykey)
* [編集可能](view-model-control-lookup-ilookup-ilookupmetadata.md#editable)
* [ExtType](view-model-control-lookup-ilookup-ilookupmetadata.md#exttype)
* [FilterContext](view-model-control-lookup-ilookup-ilookupmetadata.md#filtercontext)
* [HelpText](view-model-control-lookup-ilookup-ilookupmetadata.md#helptext)
* [非表示](view-model-control-lookup-ilookup-ilookupmetadata.md#hidden)
* [ID](view-model-control-lookup-ilookup-ilookupmetadata.md#id)
* [ラベル](view-model-control-lookup-ilookup-ilookupmetadata.md#label)
* [LookupEntity](view-model-control-lookup-ilookup-ilookupmetadata.md#lookupentity)
* [LookupPage](view-model-control-lookup-ilookup-ilookupmetadata.md#lookuppage)
* [LookupPageId](view-model-control-lookup-ilookup-ilookupmetadata.md#lookuppageid)
* [必須](view-model-control-lookup-ilookup-ilookupmetadata.md#mandatory)
* [MultiSelect](view-model-control-lookup-ilookup-ilookupmetadata.md#multiselect)
* [名前](view-model-control-lookup-ilookup-ilookupmetadata.md#name)
* [NumSequence](view-model-control-lookup-ilookup-ilookupmetadata.md#numsequence)
* [注文](view-model-control-lookup-ilookup-ilookupmetadata.md#order)
* [ReferenceAppId](view-model-control-lookup-ilookup-ilookupmetadata.md#referenceappid)
* [ShowLookupPage](view-model-control-lookup-ilookup-ilookupmetadata.md#showlookuppage)
* [[タイプ](view-model-control-lookup-ilookup-ilookupmetadata.md#type)]
* [ValueField](view-model-control-lookup-ilookup-ilookupmetadata.md#valuefield)
* [ValueKey](view-model-control-lookup-ilookup-ilookupmetadata.md#valuekey)

### <a name="events"></a>イベント

* [OnOptionSelected](view-model-control-lookup-ilookup-ilookupmetadata.md#onoptionselected)
* [OnValueChanged](view-model-control-lookup-ilookup-ilookupmetadata.md#onvaluechanged)

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


### <a name="displayfield"></a>DisplayField

DisplayField: 文字列 (オプション) 

ページ上のコントロールの名前。その値はユーザーに表示する必要があります。 通常、この値は、ユーザーが読み取り可能なわかりやすい値です。


### <a name="displaykey"></a>DisplayKey

DisplayKey: 文字列 (オプション) 




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


### <a name="filtercontext"></a>FilterContext

FilterContext: DataFilter (オプション) 




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


### <a name="label"></a>ラベル

ラベル: 文字列 (省略可) 

コントロールのラベル。 E.g. 個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承


### <a name="lookupentity"></a>LookupEntity

LookupEntity: 任意 (省略可) 

ルックアップで検索されているエンティティ。


### <a name="lookuppage"></a>LookupPage

LookupPage: 文字列 (省略可) 




### <a name="lookuppageid"></a>LookupPageId

LookupPageId: 文字列 (省略可) 




### <a name="mandatory"></a>必須

必須: ブール値 (省略可) 

true と設定されている場合は、コントロールのインプットがタスクを完了するために必要です。
必須のコントロールには、赤いアウトラインがあります。

> [InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md).[Mandatory](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#mandatory) から継承


### <a name="multiselect"></a>MultiSelect

MultiSelect: ブール値 (省略可) 

True の場合、ルックアップは複数選択として構成されます。


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


### <a name="referenceappid"></a>ReferenceAppId

ReferenceAppId: 文字列 (オプション) 




### <a name="showlookuppage"></a>ShowLookupPage

ShowLookupPage: ブール値 (省略可) 




### <a name="type"></a>種類

Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

コントロール タイプを示す文字列。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承


### <a name="valuefield"></a>ValueField

ValueField: 文字列 (オプション) 

ページ上のコントロールの名前。その値はデータをコミットする際に使用する必要があります。 通常、この値は固有キーです。


### <a name="valuekey"></a>ValueKey

ValueKey: 文字列 (オプション) 




## <a name="events"></a>イベント

### <a name="onoptionselected"></a>OnOptionSelected

OnOptionSelected: 機能 (ルックアップ: すべて、lookupEntityData: すべて): 無効 (オプション) 

オプションが選択されることによって発生するイベントです。


### <a name="onvaluechanged"></a>OnValueChanged

OnValueChanged: 機能 (値 : すべて): 無効 (オプション) 

値が変更されることによって発生するイベントです。



