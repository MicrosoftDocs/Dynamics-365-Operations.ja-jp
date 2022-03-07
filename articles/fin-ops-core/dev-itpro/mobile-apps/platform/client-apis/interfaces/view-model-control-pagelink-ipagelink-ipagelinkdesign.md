---
title: PageLinkDesign タイプ
description: Pagelink デザイン オブジェクトの種類。
author: tonyafehr
ms.date: 08/01/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 7494faf0841109c38da2301dcc850249d28ea783
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782865"
---
# <a name="pagelinkdesign-type"></a>PageLinkDesign タイプ

[!include [banner](../../../../includes/banner.md)]

Pagelink デザイン オブジェクトの種類。

### <a name="hierarchy"></a>階層

[Design](view-model-ipage-idesign.md) <br>&nbsp;&nbsp;&nbsp;└─ PageLinkDesign <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [alignItems](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#alignitems)
* [alignSelf](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#alignself)
* [バックグラウンド](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#background)
* [バインディング](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#bindings)
* [枠線](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#border)
* [色](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#color)
* [excludeContext](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#excludecontext)
* [flexFlow](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#flexflow)
* [flexSize](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#flexsize)
* [fontSize](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#fontsize)
* [fontWeight](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#fontweight)
* [hideArrow](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#hidearrow)
* [アイコン](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#icon)
* [justifyItems](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#justifyitems)
* [ラベル](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#label)
* [labelPosition](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#labelposition)
* [名前](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#name)
* [ナビゲーション](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#navigation)
* [スペース](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#padding)
* [showCount](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#showcount)
* [スタイル](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#style)
* [タイプ](view-model-control-pagelink-ipagelink-ipagelinkdesign.md#type)

## <a name="properties"></a>プロパティ

### <a name="alignitems"></a>alignItems

alignItems: string (optional) 

このプロパティは、CSS プロパティ「align-items」のエイリアスです。
"align-items" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。

> [Design](view-model-ipage-idesign.md).[alignItems](view-model-ipage-idesign.md#alignitems) から継承


### <a name="alignself"></a>alignSelf

alignSelf: string (optional) 



> [Design](view-model-ipage-idesign.md).[alignSelf](view-model-ipage-idesign.md#alignself) から継承


### <a name="background"></a>background

background: string (optional) 

背景色を設定します。
「テーマ」を使用している場合、色はアプリケーションのテーマの色と一致します。 <br>
![使用可能な背景色の画像。](../../../platform/media/colors_pagelink.PNG)


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
![使用可能な前景色の画像。](../../../media/colors.PNG)

> [Design](view-model-ipage-idesign.md).[color](view-model-ipage-idesign.md#color) から継承


### <a name="excludecontext"></a>excludeContext

excludeContext: boolean (省略可) 




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
既定では、矢印はナビゲーション コントロール内に存在します。<br>
このプロパティは、デザイン オブジェクトを通じてのみ追加できます。


### <a name="icon"></a>[] アイコン

icon: string (省略可) 

ページリンク コントロールに表示されるアイコンの名前。
次に [利用可能なアイコンの一覧](/dynamics/s-e/) を示します。


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


### <a name="navigation"></a>navigation

navigation: [NavigationArgs](view-model-ipage-inavigationargs.md) (省略可) 

ページリンクのナビゲーション オブジェクト。


### <a name="padding"></a>padding

padding: "none" &#124; "small" &#124; "std" (省略可) 

コンポーネントのスペース動作を指定できるように許可します。
コンポーネントは、親コンテナー コンポーネントによって指定されたスペース動作を継承します。

> [Design](view-model-ipage-idesign.md).[padding](view-model-ipage-idesign.md#padding) から継承


### <a name="showcount"></a>showCount

showCount: boolean (省略可) 

True の場合、ターゲット ページのリストに存在するレコードの数を表示します。
このプロパティは、ナビゲーション ターゲットがリスト コントロールに含まれるページである場合にのみ適しています。


### <a name="style"></a>style

style: string (省略可) 

ページリンク コントロールのビジュアル スタイルを指定します。
オプション:
* 「インライン」: は、アイコン、ラベル インラインと共にコンテナー全体の幅を占めます
* 「ボタン」: は、アイコンの下のラベルと共に、ラベルの必要な幅だけを占めます


### <a name="type"></a>タイプ

type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

文字列としてのコントロールのタイプ。

> [Design](view-model-ipage-idesign.md).[type](view-model-ipage-idesign.md#type) から継承




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]