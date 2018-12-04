---
title: "マルチ参照モジュール"
description: "複数ルックアップ コントロールは、一度に複数選択できる点を除いて通常のルックアップに似ています。"
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
ms.openlocfilehash: 4b476037b3634de6bcc273e1be05386b084c2f3a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="multi-lookup-module"></a>マルチ参照モジュール

[!include [banner](../../../../includes/banner.md)]

複数ルックアップ コントロールは、一度に複数選択できる点を除いて通常のルックアップに似ています。

## <a name="index"></a>指数

### <a name="types"></a>種類

* [MultiLookup](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md)
* [MultiLookupDesign](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md)
* [MultiLookupMetadata](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md)

## <a name="types"></a>種類


### <a name="multilookup"></a>MultiLookup

#### <a name="hierarchy"></a>階層

[InputControl](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ MultiLookup <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [コンテナー](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#container) |container: ブール値 (省略可)  <br>|コントロールがコンテナーの場合は true です。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[container](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#container) から継承 <br> |
| [ジェネリック](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#generic) |generic: boolean (省略可)  <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[generic](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承 <br> |
| [getDataSource](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#getdatasource) |getDataSource: function(): any <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承 <br> |
| [getEntityRefs](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#getentityrefs) |getEntityRefs: function(): string [ ] &#124; number [ ] <br>|  |
| [非表示](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#hidden) |hidden: boolean <br>|コントロールが非常時の場合は true です。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承 <br> |
| [setEntityRefs](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#setentityrefs) |setEntityRefs: function(ids: string [ ] &#124; number [ ]): Promise &lt;any&gt; <br>|  |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [applyDesign](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#applydesign) |applyDesign(IDesign: [MultiLookupDesign](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md)): void|付与されたデザインをコントロールのデザインに適用します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。 <br> |
| [dataContext](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#datacontext) |dataContext(): any|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承 <br> |
| [getDesign](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#getdesign) |getDesign(): [Design](../interfaces/view-model-ipage-idesign.md)|このコントロールのデザイン オブジェクトを返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承 <br> |
| [getLookupPage](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#getlookuppage) |getLookupPage(): [Page](../interfaces/view-model-ipage-ipage.md)|  |
| [isEditable](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#iseditable) |isEditable(): boolean|コントロールが編集可能かどうかを示すブール値。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承 <br> |
| [メタデータ](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#metadata) |metadata(): [MultiLookupMetadata](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md)|このコントロールのメタデータ オブジェクトを返します。<br>  [InputControl](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[metadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#metadata) をオーバーライドします。 <br> |
| [親](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#parent) |parent(): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールの親 (コントロールまたはページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[parent](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承 <br> |
| [ルート](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#root) |root(): [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールのルート フォーム インスタンス (ページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[root](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#root) から継承 <br> |

#### <a name="events"></a>イベント

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [onDataChanged](../interfaces/view-model-control-lookup-imultilookup-imultilookup.md#ondatachanged) |onDataChanged: [EventHook](../interfaces/event-ievent-ieventhook.md) &lt;null&gt; <br>|入力コントロールのデータが変更されたときに発生するイベントです。<br>  [InputControl](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承 <br> |


### <a name="multilookupdesign"></a>MultiLookupDesign

#### <a name="hierarchy"></a>階層

[InputControlDesign](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md) <br>&nbsp;&nbsp;&nbsp;└─ MultiLookupDesign <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [alignItems](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#alignitems) |alignItems: string (optional)  <br>|このプロパティは、CSS プロパティ「align-items」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[alignItems](../interfaces/view-model-ipage-idesign.md#alignitems) から継承 <br> |
| [alignSelf](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#alignself) |alignSelf: string (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[alignSelf](../interfaces/view-model-ipage-idesign.md#alignself) から継承 <br> |
| [バインディング](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#bindings) |bindings: any (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[bindings](../interfaces/view-model-ipage-idesign.md#bindings) から継承 <br> |
| [枠線](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#border) |border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (optional)  <br>|コントロールの境界動作。 このプロパティは、子によって継承されません。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[border](../interfaces/view-model-ipage-idesign.md#border) から継承 <br> |
| [色](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#color) |color: string (optional)  <br>|コンテナーの前景色。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[color](../interfaces/view-model-ipage-idesign.md#color) から継承 <br> |
| [flexFlow](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#flexflow) |flexFlow: string (省略可)  <br>|このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexFlow](../interfaces/view-model-ipage-idesign.md#flexflow) から継承 <br> |
| [flexSize](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#flexsize) |flexSize: string (省略可)  <br>|1 つの番号または 2 つの番号が文字列として書き込まれています。 E.g. 「(サイズを拡大) [(サイズの縮小)]」して、即時フレックス コンテナの使用可能領域に対応します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexSize](../interfaces/view-model-ipage-idesign.md#flexsize) から継承 <br> |
| [fontSize](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#fontsize) |fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (省略可)  <br>|比例テキスト サイズ<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontSize](../interfaces/view-model-ipage-idesign.md#fontsize) から継承 <br> |
| [fontWeight](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#fontweight) |fontWeight: "normal" &#124; "bold" (省略可)  <br>|標準または太字のテキスト。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontWeight](../interfaces/view-model-ipage-idesign.md#fontweight) から継承 <br> |
| [justifyItems](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#justifyitems) |justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (省略可)  <br>|このプロパティは CSS プロパティ「justify-content」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[justifyItems](../interfaces/view-model-ipage-idesign.md#justifyitems) から継承 <br> |
| [ラベル](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#label) |label: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[label](../interfaces/view-model-ipage-idesign.md#label) から継承 <br> |
| [labelPosition](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#labelposition) |labelPosition: "stacked" &#124; "hidden" &#124; "inline" (省略可)  <br>|ラベルの配置方法を決定します (行われる場合)。 既定では、labelPosition が stacked に設定されています。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[labelPosition](../interfaces/view-model-ipage-idesign.md#labelposition) から継承 <br> |
| [名前](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#name) |name: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[name](../interfaces/view-model-ipage-idesign.md#name) から継承 <br> |
| [スペース](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#padding) |padding: "none" &#124; "small" &#124; "std" (省略可)  <br>|コンポーネントのスペース動作を指定できるように許可します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[padding](../interfaces/view-model-ipage-idesign.md#padding) から継承 <br> |
| [タイプ](../interfaces/view-model-control-lookup-imultilookup-imultilookupdesign.md#type) |type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|文字列としてのコントロールのタイプ。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[type](../interfaces/view-model-ipage-idesign.md#type) から継承 <br> |


### <a name="multilookupmetadata"></a>MultiLookupMetadata

#### <a name="hierarchy"></a>階層

[InputControlMetadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ MultiLookupMetadata <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [BoundEntity](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#boundentity) |BoundEntity: 文字列 (オプション)  <br>|コントロールがバインドされるエンティティ。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承 <br> |
| [BoundField](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#boundfield) |BoundField: 文字列 (オプション)  <br>|  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承 <br> |
| [説明](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#description) |説明:文字列 (オプション)  <br>|コントロールの説明。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承 <br> |
| [Design](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#design) |デザイン: [デザイン](../interfaces/view-model-ipage-idesign.md) (オプション)  <br>|LookupPageId によって参照されるルックアップ ページのデザイン オブジェクト。<br>  |
| [編集可能](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#editable) |編集可能: プール値 (省略可)  <br>|コントロールが編集可能かどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承 <br> |
| [ExtType](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#exttype) |ExtType: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|拡張されたコントロール タイプです。 E.g. コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承 <br> |
| [FilterContext](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#filtercontext) |FilterContext: DataFilter (オプション)  <br>|  |
| [FilterLocalOnly](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#filterlocalonly) |FilterLocalOnly: ブール値 (オプション)  <br>|  |
| [HelpText](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#helptext) |HelpText: 文字列 (オプション)  <br>|コマンドのキーボード ショートカットです。 E.g. 「(Shift + F5)」<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承 <br> |
| [非表示](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#hidden) |非表示: ブール値 (オプション)  <br>|コントロールを非表示にするかどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承 <br> |
| [ID](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#id) |Id: string (オプション)  <br>|コントロールの ID 文字列です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承 <br> |
| [ラベル](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#label) |ラベル: 文字列 (省略可)  <br>|コントロールのラベル。 E.g. 個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承 <br> |
| [LookupPageId](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#lookuppageid) |LookupPageId: 文字列 (省略可)  <br>|複数のルックアップ内でホストされているページ。<br>  |
| [必須](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#mandatory) |必須: ブール値 (省略可)  <br>|true と設定されている場合は、コントロールのインプットがタスクを完了するために必要です。 必須のコントロールには、赤いアウトラインがあります。<br>  [InputControlMetadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md).[Mandatory](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#mandatory) から継承 <br> |
| [名前](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#name) |Name: 文字列 (省略可)  <br>|コントロールの名前です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承 <br> |
| [NumSequence](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#numsequence) |NumSequence: [NumberSequenceConfig](../interfaces/view-model-control-basecontrol-iinputcontrol-inumbersequenceconfig.md) (省略可)  <br>|拡張ビジネス ロジックを使用し、AX 番号シーケンス構成に基づいて、タスクまたはページ内の番号シーケンス コントロールの可視性を自動的に検出および変更するために使用されます。<br>  [InputControlMetadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md).[NumSequence](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md#numsequence) から継承 <br> |
| [注文](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#order) |注文: 番号 (オプション)  <br>|コントロールがページに表示される順序を示す番号。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承 <br> |
| [ReferenceAppId](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#referenceappid) |ReferenceAppId: 文字列 (オプション)  <br>|  |
| [ReverseLookupRelation](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#reverselookuprelation) |ReverseLookupRelation: ブール値 (省略可)  <br>|  |
| [ShowPending](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#showpending) |ShowPending: ブール値 (省略可)  <br>|  |
| [[タイプ](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#type)] |Type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|コントロール タイプを示す文字列。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承 <br> |

#### <a name="events"></a>イベント

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [OnLookupPageCreate](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#onlookuppagecreate) |OnLookupPageCreate: 機能 (args: すべて、multiLookup: すべて): (無効) オプション  <br>|  |
| [OnLookupPageCreated](../interfaces/view-model-control-lookup-imultilookup-imultilookupmetadata.md#onlookuppagecreated) |OnLookupPageCreate: 機能 (args: すべて、multiLookup: すべて): 無効 (オプション)  <br>|  |


