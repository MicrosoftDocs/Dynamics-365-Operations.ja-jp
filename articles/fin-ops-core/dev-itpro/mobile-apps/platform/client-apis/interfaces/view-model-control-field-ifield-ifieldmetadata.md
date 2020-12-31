---
title: FieldMetadata タイプ
description: フィールド メタデータのインターフェイス。
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2f5f18b9da77f42a1da60440c04e82f3267aa724
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679238"
---
# <a name="fieldmetadata-type"></a>FieldMetadata タイプ

[!include [banner](../../../../includes/banner.md)]

フィールド メタデータのインターフェイス。

### <a name="hierarchy"></a>階層

[InputControlMetadata](view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ FieldMetadata <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [BoundEntity](view-model-control-field-ifield-ifieldmetadata.md#boundentity)
* [BoundField](view-model-control-field-ifield-ifieldmetadata.md#boundfield)
* [DecimalPlaces](view-model-control-field-ifield-ifieldmetadata.md#decimalplaces)
* [説明](view-model-control-field-ifield-ifieldmetadata.md#description)
* [編集可能](view-model-control-field-ifield-ifieldmetadata.md#editable)
* [ExtType](view-model-control-field-ifield-ifieldmetadata.md#exttype)
* [書式設定](view-model-control-field-ifield-ifieldmetadata.md#formatting)
* [HelpText](view-model-control-field-ifield-ifieldmetadata.md#helptext)
* [非表示](view-model-control-field-ifield-ifieldmetadata.md#hidden)
* [ID](view-model-control-field-ifield-ifieldmetadata.md#id)
* [ラベル](view-model-control-field-ifield-ifieldmetadata.md#label)
* [LinkType](view-model-control-field-ifield-ifieldmetadata.md#linktype)
* [必須](view-model-control-field-ifield-ifieldmetadata.md#mandatory)
* [名前](view-model-control-field-ifield-ifieldmetadata.md#name)
* [NumSequence](view-model-control-field-ifield-ifieldmetadata.md#numsequence)
* [注文](view-model-control-field-ifield-ifieldmetadata.md#order)
* [ReferenceAppId](view-model-control-field-ifield-ifieldmetadata.md#referenceappid)
* [ReferencePageId](view-model-control-field-ifield-ifieldmetadata.md#referencepageid)
* [スタイル](view-model-control-field-ifield-ifieldmetadata.md#style)
* [[タイプ](view-model-control-field-ifield-ifieldmetadata.md#type)]
* [UnWrapText](view-model-control-field-ifield-ifieldmetadata.md#unwraptext)
* [WrapText](view-model-control-field-ifield-ifieldmetadata.md#wraptext)

## <a name="properties"></a>プロパティ

### <a name="boundentity"></a>BoundEntity

BoundEntity: 文字列 (オプション) 

コントロールがバインドされるエンティティ。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承


### <a name="boundfield"></a>BoundField

BoundField: 文字列 (オプション) 



> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承


### <a name="decimalplaces"></a>DecimalPlaces

DecimalPlaces: 番号 (オプション) 

タイプ「実数」のフィールドに表示される小数点以下の桁数。
既定 = 2 です。番号は [0:20] の範囲内になければなりません。


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


### <a name="formatting"></a>書式設定

書式設定: 任意 (オプション) 

タイプ「日時」または「日付」のフィールドを書式設定します。
**注記:** ブラウザーがオプション付きの `toLocaleString` をサポートしていない場合、値全体を表示します。
<br>書式設定のオプションは、選択されているスタイルによって異なります。[スタイル: "DateOnly" オプション](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString)、[スタイル: "TimeOnly" オプション](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleTimeString)、および [スタイルなしのオプション](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString)。

<br>例 1: `{ Style: "TimeOnly", Formatting: { timeZone: "UTC", timeZoneName: "short" } }`

<br>例 2: `{ Style: "DateOnly", Formatting: { month: "long", day: "numeric" } }` 結果: 3 月 2 日


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


### <a name="linktype"></a>LinkType

LinkType: 「電話」 &#124; 「電子メール」 &#124; 「URL」 (省略可) 

フィールドのリンク タイプを割り当てることで、リンクが選択されたときに適切なモバイル アプリケーションを開くことができます。


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


### <a name="referenceappid"></a>ReferenceAppId

ReferenceAppId: 文字列 (オプション) 

フィールド コントロールが存在するアプリの ID。


### <a name="referencepageid"></a>ReferencePageId

ReferencePageId: 文字列 (オプション) 

フィールド コントロールが存在するページの ID。


### <a name="style"></a>スタイル

スタイル: 文字列 (省略可) 

タイプ「日時」または「日付」のフィールドをスタイル設定します。
例: `{ Style: TimeOnly }` 結果: 12:00:00 AM


### <a name="type"></a>種類

Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

コントロール タイプを示す文字列。

> [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承


### <a name="unwraptext"></a>UnWrapText

UnWrapText: ブール値 (オプション) 

既定で False -- ページのテキストが折り返されます。


### <a name="wraptext"></a>WrapText

WrapText: ブール値 (オプション) 

True の場合、フィールド コントロールのテキストは、次の行に折り返されます。


