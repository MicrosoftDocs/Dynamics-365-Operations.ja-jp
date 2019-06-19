---
title: フィールド モジュール
description: フィールドのランタイムのインスタンスを表します。
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
ms.openlocfilehash: ae40dd2ce627e90a5c36729fa8135c3d7b9e4105
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550411"
---
# <a name="field-module"></a>フィールド モジュール

[!include [banner](../../../../includes/banner.md)]

フィールドのランタイムのインスタンスを表します。

## <a name="index"></a>指数

### <a name="types"></a>種類

* [フィールド](../interfaces/view-model-control-field-ifield-ifield.md)
* [FieldDesign](../interfaces/view-model-control-field-ifield-ifielddesign.md)
* [FieldMetadata](../interfaces/view-model-control-field-ifield-ifieldmetadata.md)

## <a name="types"></a>種類


### <a name="field"></a>フィールド

#### <a name="hierarchy"></a>階層

[InputControl](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ フィールド <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [コンテナー](../interfaces/view-model-control-field-ifield-ifield.md#container) |container: ブール値 (省略可)  <br>|コントロールがコンテナーの場合は true です。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[container](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#container) から継承 <br> |
| [ジェネリック](../interfaces/view-model-control-field-ifield-ifield.md#generic) |generic: boolean (省略可)  <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[generic](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承 <br> |
| [getDataSource](../interfaces/view-model-control-field-ifield-ifield.md#getdatasource) |getDataSource: function(): any <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承 <br> |
| [非表示](../interfaces/view-model-control-field-ifield-ifield.md#hidden) |hidden: boolean <br>|コントロールが非常時の場合は true です。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承 <br> |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [applyDesign](../interfaces/view-model-control-field-ifield-ifield.md#applydesign) |applyDesign(IDesign: [FieldDesign](../interfaces/view-model-control-field-ifield-ifielddesign.md)): void|付与されたデザインをコントロールのデザインに適用します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。 <br> |
| [dataContext](../interfaces/view-model-control-field-ifield-ifield.md#datacontext) |dataContext(): any|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承 <br> |
| [getDesign](../interfaces/view-model-control-field-ifield-ifield.md#getdesign) |getDesign(): [Design](../interfaces/view-model-ipage-idesign.md)|このコントロールのデザイン オブジェクトを返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承 <br> |
| [getEditableFormattedValue](../interfaces/view-model-control-field-ifield-ifield.md#geteditableformattedvalue) |getEditableFormattedValue(): string &#124; number &#124; Date|編集可能なフィールド コントロールの書式設定された10 進法の文字列値を取得します。<br>  |
| [getEditableValue](../interfaces/view-model-control-field-ifield-ifield.md#geteditablevalue) |getEditableValue(): string &#124; number &#124; Date|編集可能なフィールド コントロールの値を取得します。<br>  |
| [getEntityRef](../interfaces/view-model-control-field-ifield-ifield.md#getentityref) |getEntityRef(): any|コントロールにバインドする entityRef の値を取得します。<br>  |
| [getFormattedValue](../interfaces/view-model-control-field-ifield-ifield.md#getformattedvalue) |getFormattedValue(): string|書式設定された 10 進法の文字列値を取得します。<br>  |
| [getRefLink](../interfaces/view-model-control-field-ifield-ifield.md#getreflink) |getRefLink(): [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md)|参照リンクのナビゲーション オブジェクトを取得します。<br>  |
| [getValue](../interfaces/view-model-control-field-ifield-ifield.md#getvalue) |getValue(): any|フィールド コントロールの値を取得します。<br>  |
| [hasRefLink](../interfaces/view-model-control-field-ifield-ifield.md#hasreflink) |hasRefLink(): boolean|フィールドに refLink がある場合は true を返します。それ以外の場合は、false を返します。<br>  |
| [hasUnWrapText](../interfaces/view-model-control-field-ifield-ifield.md#hasunwraptext) |hasUnWrapText(): boolean|コントロールのラップ テキスト プロパティを取得します。<br>  |
| [isEditable](../interfaces/view-model-control-field-ifield-ifield.md#iseditable) |isEditable(): boolean|コントロールが編集可能かどうかを示すブール値。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承 <br> |
| [メタデータ](../interfaces/view-model-control-field-ifield-ifield.md#metadata) |metadata(): [FieldMetadata](../interfaces/view-model-control-field-ifield-ifieldmetadata.md)|このコントロールのメタデータ オブジェクトを返します。<br>  [InputControl](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。 <br> |
| [親](../interfaces/view-model-control-field-ifield-ifield.md#parent) |parent(): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールの親 (コントロールまたはページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[parent](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承 <br> |
| [ルート](../interfaces/view-model-control-field-ifield-ifield.md#root) |root(): [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールのルート フォーム インスタンス (ページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[root](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#root) から継承 <br> |
| [setEditableValue](../interfaces/view-model-control-field-ifield-ifield.md#seteditablevalue) |setEditableValue(value: string &#124; number &#124; Date): void|編集可能なフィールド コントロールの値を設定します。<br>  |

#### <a name="events"></a>イベント

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [onDataChanged](../interfaces/view-model-control-field-ifield-ifield.md#ondatachanged) |onDataChanged: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;null&gt; <br>|入力コントロールのデータが変更されたときに発生するイベントです。<br>  [InputControl](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承 <br> |


### <a name="fielddesign"></a>FieldDesign

#### <a name="hierarchy"></a>階層

[InputControlDesign](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md) <br>&nbsp;&nbsp;&nbsp;└─ FieldDesign <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [alignItems](../interfaces/view-model-control-field-ifield-ifielddesign.md#alignitems) |alignItems: string (optional)  <br>|このプロパティは、CSS プロパティ「align-items」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[alignItems](../interfaces/view-model-ipage-idesign.md#alignitems) から継承 <br> |
| [alignSelf](../interfaces/view-model-control-field-ifield-ifielddesign.md#alignself) |alignSelf: string (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[alignSelf](../interfaces/view-model-ipage-idesign.md#alignself) から継承 <br> |
| [バインディング](../interfaces/view-model-control-field-ifield-ifielddesign.md#bindings) |bindings: any (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[bindings](../interfaces/view-model-ipage-idesign.md#bindings) から継承 <br> |
| [枠線](../interfaces/view-model-control-field-ifield-ifielddesign.md#border) |border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (省略可)  <br>|コントロールの境界動作。 このプロパティは、子によって継承されません。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[border](../interfaces/view-model-ipage-idesign.md#border) から継承 <br> |
| [色](../interfaces/view-model-control-field-ifield-ifielddesign.md#color) |color: string (optional)  <br>|コンテナーの前景色。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[color](../interfaces/view-model-ipage-idesign.md#color) から継承 <br> |
| [flexFlow](../interfaces/view-model-control-field-ifield-ifielddesign.md#flexflow) |flexFlow: string (省略可)  <br>|このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexFlow](../interfaces/view-model-ipage-idesign.md#flexflow) から継承 <br> |
| [flexSize](../interfaces/view-model-control-field-ifield-ifielddesign.md#flexsize) |flexSize: string (省略可)  <br>|1 つの番号または 2 つの番号が文字列として書き込まれています。 E.g. 「(サイズを拡大) [(サイズの縮小)]」して、即時フレックス コンテナの使用可能領域に対応します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexSize](../interfaces/view-model-ipage-idesign.md#flexsize) から継承 <br> |
| [fontSize](../interfaces/view-model-control-field-ifield-ifielddesign.md#fontsize) |fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (省略可)  <br>|比例テキスト サイズ<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontSize](../interfaces/view-model-ipage-idesign.md#fontsize) から継承 <br> |
| [fontWeight](../interfaces/view-model-control-field-ifield-ifielddesign.md#fontweight) |fontWeight: "normal" &#124; "bold" (省略可)  <br>|標準または太字のテキスト。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontWeight](../interfaces/view-model-ipage-idesign.md#fontweight) から継承 <br> |
| [justifyItems](../interfaces/view-model-control-field-ifield-ifielddesign.md#justifyitems) |justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (省略可)  <br>|このプロパティは CSS プロパティ「justify-content」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[justifyItems](../interfaces/view-model-ipage-idesign.md#justifyitems) から継承 <br> |
| [ラベル](../interfaces/view-model-control-field-ifield-ifielddesign.md#label) |label: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[label](../interfaces/view-model-ipage-idesign.md#label) から継承 <br> |
| [labelPosition](../interfaces/view-model-control-field-ifield-ifielddesign.md#labelposition) |labelPosition: "stacked" &#124; "hidden" &#124; "inline" (省略可)  <br>|ラベルの配置方法を決定します (行われる場合)。 既定では、labelPosition が stacked に設定されています。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[labelPosition](../interfaces/view-model-ipage-idesign.md#labelposition) から継承 <br> |
| [名前](../interfaces/view-model-control-field-ifield-ifielddesign.md#name) |name: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[name](../interfaces/view-model-ipage-idesign.md#name) から継承 <br> |
| [スペース](../interfaces/view-model-control-field-ifield-ifielddesign.md#padding) |padding: "none" &#124; "small" &#124; "std" (省略可)  <br>|コンポーネントのスペース動作を指定できるように許可します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[padding](../interfaces/view-model-ipage-idesign.md#padding) から継承 <br> |
| [タイプ](../interfaces/view-model-control-field-ifield-ifielddesign.md#type) |type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|文字列としてのコントロールのタイプ。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[type](../interfaces/view-model-ipage-idesign.md#type) から継承 <br> |


### <a name="fieldmetadata"></a>FieldMetadata

#### <a name="hierarchy"></a>階層

[InputControlMetadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ FieldMetadata <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [BoundEntity](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#boundentity) |BoundEntity: 文字列 (オプション)  <br>|コントロールがバインドされるエンティティ。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承 <br> |
| [BoundField](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#boundfield) |BoundField: 文字列 (オプション)  <br>|  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承 <br> |
| [DecimalPlaces](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#decimalplaces) |DecimalPlaces: 番号 (オプション)  <br>|タイプ「実数」のフィールドに表示される小数点以下の桁数。<br>  |
| [説明](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#description) |説明:文字列 (オプション)  <br>|コントロールの説明。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承 <br> |
| [編集可能](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#editable) |編集可能: プール値 (省略可)  <br>|コントロールが編集可能かどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承 <br> |
| [ExtType](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#exttype) |ExtType: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|拡張されたコントロール タイプです。 E.g. コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承 <br> |
| [書式設定](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#formatting) |書式設定: 任意 (オプション)  <br>|タイプ「日時」または「日付」のフィールドを書式設定します。<br>  |
| [HelpText](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#helptext) |HelpText: 文字列 (オプション)  <br>|コマンドのキーボード ショートカットです。 E.g. 「(Shift + F5)」<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承 <br> |
| [非表示](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#hidden) |非表示: ブール値 (オプション)  <br>|コントロールを非表示にするかどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承 <br> |
| [ID](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#id) |Id: string (オプション)  <br>|コントロールの ID 文字列です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承 <br> |
| [ラベル](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#label) |ラベル: 文字列 (省略可)  <br>|コントロールのラベル。 E.g. 個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承 <br> |
| [LinkType](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#linktype) |LinkType: 「電話」 &#124; 「電子メール」 &#124; 「URL」 (省略可)  <br>|フィールドのリンク タイプを割り当てることで、リンクが選択されたときに適切なモバイル アプリケーションを開くことができます。<br>  |
| [必須](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#mandatory) |必須: ブール値 (省略可)  <br>|true と設定されている場合は、コントロールのインプットがタスクを完了するために必要です。 必須のコントロールには、赤いアウトラインがあります。<br>  [InputControlMetadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md).[Mandatory](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#mandatory) から継承 <br> |
| [名前](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#name) |Name: 文字列 (省略可)  <br>|コントロールの名前です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承 <br> |
| [NumSequence](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#numsequence) |NumSequence: [NumberSequenceConfig](../interfaces/view-model-control-basecontrol-iinputcontrol-inumbersequenceconfig.md) (省略可)  <br>|拡張ビジネス ロジックを使用し、AX 番号シーケンス構成に基づいて、タスクまたはページ内の番号シーケンス コントロールの可視性を自動的に検出および変更するために使用されます。<br>  [InputControlMetadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md).[NumSequence](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#numsequence) から継承 <br> |
| [注文](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#order) |注文: 番号 (オプション)  <br>|コントロールがページに表示される順序を示す番号。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承 <br> |
| [ReferenceAppId](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#referenceappid) |ReferenceAppId: 文字列 (オプション)  <br>|フィールド コントロールが存在するアプリの ID。<br>  |
| [ReferencePageId](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#referencepageid) |ReferencePageId: 文字列 (オプション)  <br>|フィールド コントロールが存在するページの ID。<br>  |
| [スタイル](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#style) |スタイル: 文字列 (省略可)  <br>|タイプ「日時」または「日付」のフィールドをスタイル設定します。<br>  |
| [[タイプ](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#type)] |Type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|コントロール タイプを示す文字列。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承 <br> |
| [UnWrapText](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#unwraptext) |UnWrapText: ブール値 (オプション)  <br>|既定で False -- ページのテキストが折り返されます。<br>  |
| [WrapText](../interfaces/view-model-control-field-ifield-ifieldmetadata.md#wraptext) |WrapText: ブール値 (オプション)  <br>|True の場合、フィールド コントロールのテキストは、次の行に折り返されます。<br>  |

