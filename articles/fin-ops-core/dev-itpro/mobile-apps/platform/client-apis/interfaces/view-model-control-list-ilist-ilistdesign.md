---
title: ListDesign タイプ
description: リスト デザイン オブジェクトの種類。
author: tonyafehr
ms.date: 08/01/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 610bfb7662813a8c645240f7f0c1e369bc67ac23
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781867"
---
# <a name="listdesign-type"></a>ListDesign タイプ

[!include [banner](../../../../includes/banner.md)]

リスト デザイン オブジェクトの種類。

### <a name="hierarchy"></a>階層

[ContainerControlDesign](view-model-control-container-icontainercontrol-icontainercontroldesign.md) <br>&nbsp;&nbsp;&nbsp;└─ ListDesign <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [alignItems](view-model-control-list-ilist-ilistdesign.md#alignitems)
* [alignSelf](view-model-control-list-ilist-ilistdesign.md#alignself)
* [allowScroll](view-model-control-list-ilist-ilistdesign.md#allowscroll)
* [バックグラウンド](view-model-control-list-ilist-ilistdesign.md#background)
* [バインディング](view-model-control-list-ilist-ilistdesign.md#bindings)
* [枠線](view-model-control-list-ilist-ilistdesign.md#border)
* [色](view-model-control-list-ilist-ilistdesign.md#color)
* [デザイン](view-model-control-list-ilist-ilistdesign.md#design)
* [flexFlow](view-model-control-list-ilist-ilistdesign.md#flexflow)
* [flexSize](view-model-control-list-ilist-ilistdesign.md#flexsize)
* [fontSize](view-model-control-list-ilist-ilistdesign.md#fontsize)
* [fontWeight](view-model-control-list-ilist-ilistdesign.md#fontweight)
* [hideArrow](view-model-control-list-ilist-ilistdesign.md#hidearrow)
* [hideSearchBar](view-model-control-list-ilist-ilistdesign.md#hidesearchbar)
* [itemBorder](view-model-control-list-ilist-ilistdesign.md#itemborder)
* [品目](view-model-control-list-ilist-ilistdesign.md#items)
* [justifyItems](view-model-control-list-ilist-ilistdesign.md#justifyitems)
* [ラベル](view-model-control-list-ilist-ilistdesign.md#label)
* [labelPosition](view-model-control-list-ilist-ilistdesign.md#labelposition)
* [名前](view-model-control-list-ilist-ilistdesign.md#name)
* [スペース](view-model-control-list-ilist-ilistdesign.md#padding)
* [タイプ](view-model-control-list-ilist-ilistdesign.md#type)

## <a name="properties"></a>プロパティ

### <a name="alignitems"></a>alignItems

alignItems: string (optional) 

このプロパティは、CSS プロパティ「align-items」のエイリアスです。
"align-items" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。

> [Design](view-model-ipage-idesign.md).[alignItems](view-model-ipage-idesign.md#alignitems) から継承


### <a name="alignself"></a>alignSelf

alignSelf: string (optional) 



> [Design](view-model-ipage-idesign.md).[alignSelf](view-model-ipage-idesign.md#alignself) から継承


### <a name="allowscroll"></a>allowScroll

allowScroll: string (optional) 

アイテムがコンテナーの空き領域に収まらないときにコンテナーがスクロールできる場合は true です。
コンテナーにスクロール可能なアイテムがある場合、スクロール領域が入れ子にならないように、このプロパティを false に設定します。

> [ContainerControlDesign](view-model-control-container-icontainercontrol-icontainercontroldesign.md).[allowScroll](view-model-control-container-icontainercontrol-icontainercontroldesign.md#allowscroll) から継承


### <a name="background"></a>background

background: string (optional) 

コンテナーの背景色。
背景色をオーバーレイするフォントが適切に表示されるように、同じコンテナ内の色属性を変更することを検討してください。
注記: 背景が「テーマ」に設定されている場合、アプリケーションのテーマ色が使用されます。
使用可能な色は次のとおりです。 <br>
![使用可能な色の画像。](../../../media/colors.PNG)

> [ContainerControlDesign](view-model-control-container-icontainercontrol-icontainercontroldesign.md).[background](view-model-control-container-icontainercontrol-icontainercontroldesign.md#background) から継承


### <a name="bindings"></a>bindings

bindings: any (optional) 



> [Design](view-model-ipage-idesign.md).[bindings](view-model-ipage-idesign.md#bindings) から継承


### <a name="border"></a>border

border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (省略可) 

コントロールの境界動作。 このプロパティは、子によって継承されません。

> [Design](view-model-ipage-idesign.md).[border](view-model-ipage-idesign.md#border) から継承


### <a name="color"></a>色

color: string (optional) 

コンテナーの前景色。
これにより、コンテナ内のすべてのヘッダー、アイテム、ラベル、アイコンの色が変更されます。<br>
この属性を設定するときは、必要に応じて背景色を同時に設定することを検討してください。<br>
注記: 色が「テーマ」に設定されている場合、アプリケーションのテーマ色が使用されます。<br>
使用可能な色は次のとおりです。 <br>
![使用可能な色の画像。](../../../media/colors.PNG)

> [Design](view-model-ipage-idesign.md).[color](view-model-ipage-idesign.md#color) から継承


### <a name="design"></a>design

design: [GroupDesign](view-model-control-group-igroup-igroupdesign.md) (optional) 

各行に適用されるデザイン オブジェクト。


### <a name="flexflow"></a>flexFlow

flexFlow: string (省略可) 

このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。
このプロパティは、CSS プロパティ「flex-flow」のエイリアスです。
"flex-flow" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。

> [Design](view-model-ipage-idesign.md).[flexFlow](view-model-ipage-idesign.md#flexflow) から継承


### <a name="flexsize"></a>flexSize

flexSize: string (省略可) 

1 つの番号または 2 つの番号が文字列として書き込まれています。 たとえば、「(サイズを拡大) [(サイズを縮小)]」して、即時フレックス コンテナーの使用可能領域に対応します。
このプロパティは、CSS プロパティ「flex」のエイリアスです。 "flex" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。

> [Design](view-model-ipage-idesign.md).[flexSize](view-model-ipage-idesign.md#flexsize) から継承


### <a name="fontsize"></a>fontSize

fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (省略可) 

比例テキスト サイズ

> [Design](view-model-ipage-idesign.md).[fontSize](view-model-ipage-idesign.md#fontsize) から継承


### <a name="fontweight"></a>fontWeight

fontWeight: "normal" &#124; "bold" (省略可) 

標準または太字のテキスト。

> [Design](view-model-ipage-idesign.md).[fontWeight](view-model-ipage-idesign.md#fontweight) から継承


### <a name="hidearrow"></a>hideArrow

hideArrow: boolean (省略可) 

既定のスタイル ナビゲーション コントロールの矢印 ( > ) を非表示にするように許可します。
リストで、メタデータに DetailsPageId、navigationHandler、または OnNavigate がある場合、既定では行がクリック可能であることを示すための矢印が存在することに注意してください。

<br>このプロパティは、デザイン オブジェクトを通じてのみ追加できます。


### <a name="hidesearchbar"></a>hideSearchBar

hideSearchBar: boolean (省略可) 

True の場合、検索バーが表示されません。


### <a name="itemborder"></a>itemBorder

itemBorder: "solid" &#124; "none" (省略可) 

True の場合、リストの各行の周りに境界線が表示されます。
このプロパティは、border プロパティをコンテナ内のすべてのアイテムに個別に適用するのと同じです。

> [ContainerControlDesign](view-model-control-container-icontainercontrol-icontainercontroldesign.md).[itemBorder](view-model-control-container-icontainercontrol-icontainercontroldesign.md#itemborder) から継承


### <a name="items"></a>品目

items: string &#124; [Design](view-model-ipage-idesign.md) \[ \] (省略可) 

コンテナーの内部で配置するコンポーネントを含む配列です。

> [ContainerControlDesign](view-model-control-container-icontainercontrol-icontainercontroldesign.md).[items](view-model-control-container-icontainercontrol-icontainercontroldesign.md#items) から継承


### <a name="justifyitems"></a>justifyItems

justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (省略可) 

このプロパティは CSS プロパティ「justify-content」のエイリアスです。
"justify-content" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。

> [Design](view-model-ipage-idesign.md).[justifyItems](view-model-ipage-idesign.md#justifyitems) から継承


### <a name="label"></a>ラベル

label: string (省略可) 



> [Design](view-model-ipage-idesign.md).[label](view-model-ipage-idesign.md#label) から継承


### <a name="labelposition"></a>labelPosition

labelPosition: "stacked" &#124; "hidden" &#124; "inline" (省略可) 

ラベルの配置方法を決定します (行われる場合)。 既定では、labelPosition が stacked に設定されています。

> [Design](view-model-ipage-idesign.md).[labelPosition](view-model-ipage-idesign.md#labelposition) から継承


### <a name="name"></a>名前

name: string (省略可) 



> [Design](view-model-ipage-idesign.md).[name](view-model-ipage-idesign.md#name) から継承


### <a name="padding"></a>padding

padding: "none" &#124; "small" &#124; "std" (省略可) 

コンポーネントのスペース動作を指定できるように許可します。
コンポーネントは、親コンテナー コンポーネントによって指定されたスペース動作を継承します。

> [Design](view-model-ipage-idesign.md).[padding](view-model-ipage-idesign.md#padding) から継承


### <a name="type"></a>タイプ

type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

文字列としてのコントロールのタイプ。

> [Design](view-model-ipage-idesign.md).[type](view-model-ipage-idesign.md#type) から継承




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]