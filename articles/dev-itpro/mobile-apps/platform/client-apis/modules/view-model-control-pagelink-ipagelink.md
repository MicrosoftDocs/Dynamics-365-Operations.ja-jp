---
title: "ページリンク"
description: "ページリンクは、別のページに移動するコントロールです。"
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
ms.openlocfilehash: 43fbafcaa6bd1411534894499acdab1012cb844b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="pagelink"></a>ページリンク 

[!include [banner](../../../../includes/banner.md)]

ページリンクは、別のページに移動するコントロールです。

## <a name="index"></a>指数

### <a name="types"></a>種類

* [PageLink](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md)
* [PageLinkDesign](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md)
* [PageLinkMetadata](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md)

## <a name="types"></a>種類


### <a name="pagelink"></a>PageLink

#### <a name="hierarchy"></a>階層

[コントロール](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ PageLink <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [コンテナー](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#container) |container: ブール値 (省略可)  <br>|コントロールがコンテナーの場合は true です。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[container](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#container) から継承 <br> |
| [ジェネリック](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#generic) |generic: boolean (省略可)  <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[generic](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承 <br> |
| [getDataSource](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#getdatasource) |getDataSource: function(): any <br>|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承 <br> |
| [非表示](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#hidden) |hidden: boolean <br>|コントロールが非常時の場合は true です。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承 <br> |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [allowsNavigation](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#allowsnavigation) |allowsNavigation(): boolean|  |
| [applyDesign](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#applydesign) |applyDesign(design: [PageLinkDesign](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md)): void|付与されたデザインをコントロールのデザインに適用します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。 <br> |
| [dataContext](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#datacontext) |dataContext(): any|  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承 <br> |
| [getCount](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#getcount) |getCount(): number &#124; string|  |
| [getDesign](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#getdesign) |getDesign(): [Design](../interfaces/view-model-ipage-idesign.md)|このコントロールのデザイン オブジェクトを返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承 <br> |
| [getNavigationHandler](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#getnavigationhandler) |getNavigationHandler(): [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md)|  |
| [isEditable](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#iseditable) |isEditable(): boolean|コントロールが編集可能かどうかを示すブール値。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承 <br> |
| [メタデータ](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#metadata) |metadata(): [PageLinkMetadata](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md)|このコントロールのメタデータ オブジェクトを返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[metadata](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#metadata) をオーバーライドします。 <br> |
| [親](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#parent) |parent(): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールの親 (コントロールまたはページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[parent](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承 <br> |
| [ルート](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#root) |root(): [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールのルート フォーム インスタンス (ページ) を返します。<br>  [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md).[root](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#root) から継承 <br> |
| [showCount](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md#showcount) |showCount(): boolean|  |


### <a name="pagelinkdesign"></a>PageLinkDesign

#### <a name="hierarchy"></a>階層

[Design](../interfaces/view-model-ipage-idesign.md) <br>&nbsp;&nbsp;&nbsp;└─ PageLinkDesign <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [alignItems](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#alignitems) |alignItems: string (optional)  <br>|このプロパティは、CSS プロパティ「align-items」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[alignItems](../interfaces/view-model-ipage-idesign.md#alignitems) から継承 <br> |
| [alignSelf](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#alignself) |alignSelf: string (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[alignSelf](../interfaces/view-model-ipage-idesign.md#alignself) から継承 <br> |
| [バックグラウンド](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#background) |background: string (optional)  <br>|背景色を設定します。<br>  |
| [バインディング](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#bindings) |bindings: any (optional)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[bindings](../interfaces/view-model-ipage-idesign.md#bindings) から継承 <br> |
| [枠線](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#border) |border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (optional)  <br>|コントロールの境界動作。 このプロパティは、子によって継承されません。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[border](../interfaces/view-model-ipage-idesign.md#border) から継承 <br> |
| [色](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#color) |color: string (optional)  <br>|コンテナーの前景色。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[color](../interfaces/view-model-ipage-idesign.md#color) から継承 <br> |
| [excludeContext](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#excludecontext) |excludeContext: boolean (省略可)  <br>|  |
| [flexFlow](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#flexflow) |flexFlow: string (省略可)  <br>|このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexFlow](../interfaces/view-model-ipage-idesign.md#flexflow) から継承 <br> |
| [flexSize](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#flexsize) |flexSize: string (省略可)  <br>|1 つの番号または 2 つの番号が文字列として書き込まれています。 E.g. 「(サイズを拡大) [(サイズの縮小)]」して、即時フレックス コンテナの使用可能領域に対応します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[flexSize](../interfaces/view-model-ipage-idesign.md#flexsize) から継承 <br> |
| [fontSize](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#fontsize) |fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (省略可)  <br>|比例テキスト サイズ<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontSize](../interfaces/view-model-ipage-idesign.md#fontsize) から継承 <br> |
| [fontWeight](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#fontweight) |fontWeight: "normal" &#124; "bold" (省略可)  <br>|標準または太字のテキスト。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[fontWeight](../interfaces/view-model-ipage-idesign.md#fontweight) から継承 <br> |
| [hideArrow](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#hidearrow) |hideArrow: boolean (省略可)  <br>|既定のスタイル ナビゲーション コントロールの矢印 ( > ) を非表示にするように許可します。<br>  |
| [アイコン](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#icon) |icon: string (省略可)  <br>|ページリンク コントロールに表示されるアイコンの名前。<br>  |
| [justifyItems](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#justifyitems) |justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (省略可)  <br>|このプロパティは CSS プロパティ「justify-content」のエイリアスです。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[justifyItems](../interfaces/view-model-ipage-idesign.md#justifyitems) から継承 <br> |
| [ラベル](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#label) |label: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[label](../interfaces/view-model-ipage-idesign.md#label) から継承 <br> |
| [labelPosition](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#labelposition) |labelPosition: "stacked" &#124; "hidden" &#124; "inline" (省略可)  <br>|ラベルの配置方法を決定します (行われる場合)。 既定では、labelPosition が stacked に設定されています。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[labelPosition](../interfaces/view-model-ipage-idesign.md#labelposition) から継承 <br> |
| [名前](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#name) |name: string (省略可)  <br>|  [Design](../interfaces/view-model-ipage-idesign.md).[name](../interfaces/view-model-ipage-idesign.md#name) から継承 <br> |
| [ナビゲーション](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#navigation) |navigation: [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md) (省略可)  <br>|ページリンクのナビゲーション オブジェクト。<br>  |
| [スペース](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#padding) |padding: "none" &#124; "small" &#124; "std" (省略可)  <br>|コンポーネントのスペース動作を指定できるように許可します。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[padding](../interfaces/view-model-ipage-idesign.md#padding) から継承 <br> |
| [showCount](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#showcount) |showCount: boolean (省略可)  <br>|True の場合、ターゲット ページのリストに存在するレコードの数を表示します。<br>  |
| [スタイル](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#style) |style: string (省略可)  <br>|ページリンク コントロールのビジュアル スタイルを指定します。 オプション: * "inline": は、アイコンをインラインに含むラベルによってそのコンテナーの幅全体を示します。* "button": は、アイコンの下のラベルによって、ラベル必要な幅だけを示します。<br>  |
| [タイプ](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkdesign.md#type) |type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|文字列としてのコントロールのタイプ。<br>  [Design](../interfaces/view-model-ipage-idesign.md).[type](../interfaces/view-model-ipage-idesign.md#type) から継承 <br> |


### <a name="pagelinkmetadata"></a>PageLinkMetadata

#### <a name="hierarchy"></a>階層

[ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ PageLinkMetadata <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [BoundEntity](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#boundentity) |BoundEntity: 文字列 (オプション)  <br>|コントロールがバインドされるエンティティ。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承 <br> |
| [BoundField](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#boundfield) |BoundField: 文字列 (オプション)  <br>|  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承 <br> |
| [説明](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#description) |説明:文字列 (オプション)  <br>|コントロールの説明。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承 <br> |
| [編集可能](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#editable) |編集可能: プール値 (省略可)  <br>|コントロールが編集可能かどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承 <br> |
| [ExcludeContext](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#excludecontext) |ExcludeContext: boolean (オプション)  <br>|  |
| [ExtType](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#exttype) |ExtType: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|拡張されたコントロール タイプです。 E.g. コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承 <br> |
| [HelpText](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#helptext) |HelpText: 文字列 (オプション)  <br>|コマンドのキーボード ショートカットです。 E.g. 「(Shift + F5)」<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承 <br> |
| [非表示](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#hidden) |非表示: ブール値 (オプション)  <br>|コントロールを非表示にするかどうかを示すブール値。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承 <br> |
| [アイコン](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#icon) |アイコン: string (オプション)  <br>|ページリンク コントロールに表示されるアイコンの名前。<br>  |
| [IconSize](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#iconsize) |IconSize: 番号 (オプション)  <br>|ページリンク コントロールに表示されるアイコンのサイズを決定します。<br>  |
| [ID](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#id) |Id: string (オプション)  <br>|コントロールの ID 文字列です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承 <br> |
| [ラベル](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#label) |ラベル: 文字列 (省略可)  <br>|コントロールのラベル。 E.g. 個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承 <br> |
| [名前](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#name) |Name: 文字列 (省略可)  <br>|コントロールの名前です。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承 <br> |
| [ナビゲーション](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#navigation) |ナビゲーション: [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md) (省略可)  <br>|ページリンクのナビゲーション オブジェクト。<br>  |
| [注文](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#order) |注文: 番号 (オプション)  <br>|コントロールがページに表示される順序を示す番号。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承 <br> |
| [ShowCount](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#showcount) |ShowCount: ブール値 (省略可)  <br>|True の場合、ターゲット ページのリストに存在するレコードの数を表示します。<br>  |
| [スタイル](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#style) |スタイル: 文字列 (省略可)  <br>|ページリンク コントロールのビジュアル スタイルを指定します。<br>  |
| [ターゲット](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#target) |ターゲット: string (省略可)  <br>|ページリンクが選択されたときに移動するターゲット アクションまたはページの名前。<br>  |
| [[タイプ](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#type)] |Type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|コントロール タイプを示す文字列。<br>  [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承 <br> |
| [UseDataContext](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#usedatacontext) |UseDataContext: boolean (オプション)  <br>|  |

#### <a name="events"></a>イベント

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [OnNavigate](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md#onnavigate) |OnNavigate: 機能 (ナビゲーション:[NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md) & #124; 文字列): すべて (オプション)  <br>|ナビゲーションがトリガーされたときに発生するイベントです。<br>  |


