---
title: ImageDesign タイプ
description: イメージ デザイン オブジェクトの種類。
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
ms.openlocfilehash: fcd54b7f1f6dc3b01cb1effaaf90abae8458f498
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851575"
---
# <a name="imagedesign-type"></a>ImageDesign タイプ

[!include [banner](../../../../includes/banner.md)]

イメージ デザイン オブジェクトの種類。

### <a name="hierarchy"></a>階層

[Design](view-model-ipage-idesign.md) <br>&nbsp;&nbsp;&nbsp;└─ ImageDesign <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [alignItems](view-model-control-image-iimage-iimagedesign.md#alignitems)
* [alignSelf](view-model-control-image-iimage-iimagedesign.md#alignself)
* [バインディング](view-model-control-image-iimage-iimagedesign.md#bindings)
* [枠線](view-model-control-image-iimage-iimagedesign.md#border)
* [色](view-model-control-image-iimage-iimagedesign.md#color)
* [flexFlow](view-model-control-image-iimage-iimagedesign.md#flexflow)
* [flexSize](view-model-control-image-iimage-iimagedesign.md#flexsize)
* [fontSize](view-model-control-image-iimage-iimagedesign.md#fontsize)
* [fontWeight](view-model-control-image-iimage-iimagedesign.md#fontweight)
* [高さ](view-model-control-image-iimage-iimagedesign.md#height)
* [imageStyle](view-model-control-image-iimage-iimagedesign.md#imagestyle)
* [justifyItems](view-model-control-image-iimage-iimagedesign.md#justifyitems)
* [ラベル](view-model-control-image-iimage-iimagedesign.md#label)
* [labelPosition](view-model-control-image-iimage-iimagedesign.md#labelposition)
* [名前](view-model-control-image-iimage-iimagedesign.md#name)
* [スペース](view-model-control-image-iimage-iimagedesign.md#padding)
* [タイプ](view-model-control-image-iimage-iimagedesign.md#type)
* [幅](view-model-control-image-iimage-iimagedesign.md#width)

## <a name="properties"></a>プロパティ

### <a name="alignitems"></a>alignItems

alignItems: string (optional) 

このプロパティは、CSS プロパティ「align-items」のエイリアスです。
"align-items" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。

> [Design](view-model-ipage-idesign.md).[alignItems](view-model-ipage-idesign.md#alignitems) から継承


### <a name="alignself"></a>alignSelf

alignSelf: string (optional) 



> [Design](view-model-ipage-idesign.md).[alignSelf](view-model-ipage-idesign.md#alignself) から継承


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
![サンプル画像](../../../media/colors.PNG)

> [Design](view-model-ipage-idesign.md).[color](view-model-ipage-idesign.md#color) から継承


### <a name="flexflow"></a>flexFlow

flexFlow: string (省略可) 

このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。
このプロパティは、CSS プロパティ「flex-flow」のエイリアスです。
"flex-flow" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。

> [Design](view-model-ipage-idesign.md).[flexFlow](view-model-ipage-idesign.md#flexflow) から継承


### <a name="flexsize"></a>flexSize

flexSize: string (省略可) 

1 つの番号または 2 つの番号が文字列として書き込まれています。 E.g. 「(サイズを拡大) [(サイズの縮小)]」して、即時フレックス コンテナの使用可能領域に対応します。
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


### <a name="height"></a>height

height: string (省略可) 

画像の相対垂直方向。
サイズは CSS 空白サイズとほぼ同じです。


### <a name="imagestyle"></a>imageStyle

imageStyle: [ImageStyleType](../modules/view-model-control-image-iimage.md#imagestyletype) (optional) 

画像のスタイル。


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


### <a name="width"></a>width

width: string (省略可) 

画像の相対水平方向。
サイズは CSS 空白サイズとほぼ同じです。


