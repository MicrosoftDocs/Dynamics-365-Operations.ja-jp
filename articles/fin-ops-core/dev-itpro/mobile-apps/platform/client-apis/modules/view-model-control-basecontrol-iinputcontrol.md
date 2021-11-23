---
title: 入力モジュール
description: 入力コントロールは、たとえば新しいコントロールに対するユーザー入力を収集するために通常はタスク ページで使用されます。
author: tonyafehr
ms.date: 08/01/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 27e71fd52e430d42c451992a65d9f1585f140d35
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782170"
---
# <a name="input-module"></a>入力モジュール

[!include [banner](../../../../includes/banner.md)]

入力コントロールは、たとえば新しいコントロールに対するユーザー入力を収集するために通常はタスク ページで使用されます。

## <a name="index"></a>指数

### <a name="types"></a>種類

* [InputControl](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md)
* [InputControlDesign](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md)
* [InputControlMetadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)
* [NumberSequenceConfig](../interfaces/view-model-control-basecontrol-iinputcontrol-inumbersequenceconfig.md)

## <a name="types"></a>種類


### <a name="inputcontrol"></a>InputControl

#### <a name="hierarchy"></a>階層

[コントロール](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ InputControl <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [Field](../interfaces/view-model-control-field-ifield-ifield.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ルックアップ](../interfaces/view-model-control-lookup-ilookup-ilookup.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [MultiLookup](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [値](../interfaces/view-model-control-value-ivalue-ivalue.md) <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [コンテナー](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#container) |container: ブール値 (省略可)  <br>|コントロールがコンテナーの場合は true です。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[container](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#container) から継承 <br> |
| [ジェネリック](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#generic) |generic: boolean (省略可)  <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[generic](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承 <br> |
| [getDataSource](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#getdatasource) |getDataSource: function(): any <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承 <br> |
| [非表示](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#hidden) |hidden: boolean <br>|コントロールが非常時の場合は true です。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承 <br> |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [applyDesign](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#applydesign) |applyDesign(design: [Design](../interfaces/view-model-ipage-idesign.md)): void|付与されたデザインをコントロールのデザインに適用します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#applydesign) から継承 <br> |
| [dataContext](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#datacontext) |dataContext(): any|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承 <br> |
| [getDesign](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#getdesign) |getDesign(): [Design](../interfaces/view-model-ipage-idesign.md)|このコントロールのデザイン オブジェクトを返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承 <br> |
| [isEditable](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#iseditable) |isEditable(): boolean|コントロールが編集可能かどうかを示すブール値。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承 <br> |
| [メタデータ](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) |metadata(): [InputControlMetadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md)|このコントロールのメタデータ オブジェクトを返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[metadata](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#metadata) をオーバーライドします。 <br> |
| [親](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#parent) |parent(): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールの親 (コントロールまたはページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[parent](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承 <br> |
| [ルート](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#root) |root(): [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールのルート フォーム インスタンス (ページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[root](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#root) から継承 <br> |

#### <a name="events"></a>イベント

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [onDataChanged](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) |onDataChanged: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;null&gt; <br>|入力コントロールのデータが変更されたときに発生するイベントです。<br>  |


### <a name="inputcontroldesign"></a>InputControlDesign

#### <a name="hierarchy"></a>階層

[Design](../interfaces/view-model-ipage-idesign.md) <br>&nbsp;&nbsp;&nbsp;└─ InputControlDesign <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FieldDesign](../interfaces/view-model-control-field-ifield-ifielddesign.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [LookupDesign](../interfaces/view-model-control-lookup-ilookup-ilookupdesign.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [MultiLookupDesign](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ValueDesign](../interfaces/view-model-control-value-ivalue-ivaluedesign.md) <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [alignItems](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#alignitems) |alignItems: string (optional)  <br>|このプロパティは、CSS プロパティ「align-items」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[alignItems](../interfaces/view-model-ipage-idesign.md#alignitems) から継承 <br> |
| [alignSelf](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#alignself) |alignSelf: string (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[alignSelf](../interfaces/view-model-ipage-idesign.md#alignself) から継承 <br> |
| [バインディング](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#bindings) |bindings: any (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[bindings](../interfaces/view-model-ipage-idesign.md#bindings) から継承 <br> |
| [枠線](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#border) |border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (省略可)  <br>|コントロールの境界動作。 このプロパティは、子によって継承されません。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[border](../interfaces/view-model-ipage-idesign.md#border) から継承 <br> |
| [色](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#color) |color: string (optional)  <br>|コンテナーの前景色。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[color](../interfaces/view-model-ipage-idesign.md#color) から継承 <br> |
| [flexFlow](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#flexflow) |flexFlow: string (省略可)  <br>|このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexFlow](../interfaces/view-model-ipage-idesign.md#flexflow) から継承 <br> |
| [flexSize](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#flexsize) |flexSize: string (省略可)  <br>|1 つの番号または 2 つの番号が文字列として書き込まれています。 たとえば、「(サイズを拡大) [(サイズを縮小)]」して、即時フレックス コンテナーの使用可能領域に対応します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexSize](../interfaces/view-model-ipage-idesign.md#flexsize) から継承 <br> |
| [fontSize](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#fontsize) |fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (省略可)  <br>|比例テキスト サイズ<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontSize](../interfaces/view-model-ipage-idesign.md#fontsize) から継承 <br> |
| [fontWeight](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#fontweight) |fontWeight: "normal" &#124; "bold" (省略可)  <br>|標準または太字のテキスト。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontWeight](../interfaces/view-model-ipage-idesign.md#fontweight) から継承 <br> |
| [justifyItems](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#justifyitems) |justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (省略可)  <br>|このプロパティは CSS プロパティ「justify-content」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[justifyItems](../interfaces/view-model-ipage-idesign.md#justifyitems) から継承 <br> |
| [ラベル](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#label) |label: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[label](../interfaces/view-model-ipage-idesign.md#label) から継承 <br> |
| [labelPosition](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#labelposition) |labelPosition: "stacked" &#124; "hidden" &#124; "inline" (省略可)  <br>|ラベルの配置方法を決定します (行われる場合)。 既定では、labelPosition が stacked に設定されています。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[labelPosition](../interfaces/view-model-ipage-idesign.md#labelposition) から継承 <br> |
| [名前](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#name) |name: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[name](../interfaces/view-model-ipage-idesign.md#name) から継承 <br> |
| [スペース](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#padding) |padding: "none" &#124; "small" &#124; "std" (省略可)  <br>|コンポーネントのスペース動作を指定できるように許可します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[padding](../interfaces/view-model-ipage-idesign.md#padding) から継承 <br> |
| [タイプ](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md#type) |type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|文字列としてのコントロールのタイプ。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[type](../interfaces/view-model-ipage-idesign.md#type) から継承 <br> |


### <a name="inputcontrolmetadata"></a>InputControlMetadata

#### <a name="hierarchy"></a>階層

[ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ InputControlMetadata <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [FieldMetadata](../interfaces/view-model-control-field-ifield-ifieldmetadata.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [LookupMetadata](../interfaces/view-model-control-lookup-ilookup-ilookupmetadata.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [MultiLookupMetadata](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md) <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ [ValueMetadata](../interfaces/view-model-control-value-ivalue-ivaluemetadata.md) <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [BoundEntity](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#boundentity) |BoundEntity: 文字列 (オプション)  <br>|コントロールがバインドされるエンティティ。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承 <br> |
| [BoundField](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#boundfield) |BoundField: 文字列 (オプション)  <br>|  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承 <br> |
| [説明](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#description) |説明:文字列 (オプション)  <br>|コントロールの説明。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承 <br> |
| [編集可能](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#editable) |編集可能: プール値 (省略可)  <br>|コントロールが編集可能かどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承 <br> |
| [ExtType](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#exttype) |ExtType: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|拡張されたコントロール タイプです。 たとえば、コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承 <br> |
| [HelpText](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#helptext) |HelpText: 文字列 (オプション)  <br>|コマンドのキーボード ショートカットです。 たとえば、「(Shift + F5)」<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承 <br> |
| [非表示](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#hidden) |非表示: ブール値 (オプション)  <br>|コントロールを非表示にするかどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承 <br> |
| [ID](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#id) |Id: string (オプション)  <br>|コントロールの ID 文字列です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承 <br> |
| [ラベル](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#label) |ラベル: 文字列 (省略可)  <br>|コントロールのラベル。 たとえば、個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承 <br> |
| [必須](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#mandatory) |必須: ブール値 (省略可)  <br>|true と設定されている場合は、コントロールのインプットがタスクを完了するために必要です。 必須のコントロールには、赤いアウトラインがあります。<br>  |
| [名前](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#name) |Name: 文字列 (省略可)  <br>|コントロールの名前です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承 <br> |
| [NumSequence](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#numsequence) |NumSequence: [NumberSequenceConfig](../interfaces/view-model-control-basecontrol-iinputcontrol-inumbersequenceconfig.md) (省略可)  <br>|拡張ビジネス ロジックを使用し、AX 番号シーケンス構成に基づいて、タスクまたはページ内の番号シーケンス コントロールの可視性を自動的に検出および変更するために使用されます。<br>  |
| [注文](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#order) |注文: 番号 (オプション)  <br>|コントロールがページに表示される順序を示す番号。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承 <br> |
| [タイプ](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#type) |Type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|コントロール タイプを示す文字列。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承 <br> |


### <a name="numbersequenceconfig"></a>NumberSequenceConfig

#### <a name="hierarchy"></a>階層

NumberSequenceConfig <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [データ型](../interfaces/view-model-control-basecontrol-iinputcontrol-inumbersequenceconfig.md#datatype) |dataType: string <br>|データ型は、参照ページで番号順序が編集可能かどうかを検索するために使用されます。<br>  |
| [referencePageName](../interfaces/view-model-control-basecontrol-iinputcontrol-inumbersequenceconfig.md#referencepagename) |referencePageName: string <br>|番号順序が編集可能かどうかを定義するページのページ名。<br>  |



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]