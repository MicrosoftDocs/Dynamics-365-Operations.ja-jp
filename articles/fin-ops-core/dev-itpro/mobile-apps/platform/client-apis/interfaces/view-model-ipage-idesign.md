---
title: Design タイプ
description: デザイン オブジェクトの種類。
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
ms.openlocfilehash: f289e7559e7b12590ecdfb3ad9ebeeeb1fe72001
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658882"
---
# <a name="design-type"></a>Design タイプ

[!include [banner](../../../../includes/banner.md)]

デザイン オブジェクトの種類。
デザインの詳細については、[デザインの概要](../../scenarios/client-api-design-overview.md) を参照してください。

### <a name="hierarchy"></a>階層

デザイン <br>&nbsp;&nbsp;&nbsp;└─ [PageLinkDesign](view-model-control-pagelink-ipagelink-ipagelinkdesign.md) <br>&nbsp;&nbsp;&nbsp;└─ [ContainerControlDesign](view-model-control-container-icontainercontrol-icontainercontroldesign.md) <br>&nbsp;&nbsp;&nbsp;└─ [InputControlDesign](view-model-control-basecontrol-iinputcontrol-iinputcontroldesign.md) <br>&nbsp;&nbsp;&nbsp;└─ [ImageDesign](view-model-control-image-iimage-iimagedesign.md) <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [alignItems](view-model-ipage-idesign.md#alignitems)
* [alignSelf](view-model-ipage-idesign.md#alignself)
* [バインディング](view-model-ipage-idesign.md#bindings)
* [枠線](view-model-ipage-idesign.md#border)
* [色](view-model-ipage-idesign.md#color)
* [flexFlow](view-model-ipage-idesign.md#flexflow)
* [flexSize](view-model-ipage-idesign.md#flexsize)
* [fontSize](view-model-ipage-idesign.md#fontsize)
* [fontWeight](view-model-ipage-idesign.md#fontweight)
* [justifyItems](view-model-ipage-idesign.md#justifyitems)
* [ラベル](view-model-ipage-idesign.md#label)
* [labelPosition](view-model-ipage-idesign.md#labelposition)
* [名前](view-model-ipage-idesign.md#name)
* [スペース](view-model-ipage-idesign.md#padding)
* [タイプ](view-model-ipage-idesign.md#type)

## <a name="properties"></a>プロパティ

### <a name="alignitems"></a>alignItems

alignItems: string (optional) 

このプロパティは、CSS プロパティ「align-items」のエイリアスです。
"align-items" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。


### <a name="alignself"></a>alignSelf

alignSelf: string (optional) 




### <a name="bindings"></a>bindings

bindings: any (optional) 




### <a name="border"></a>border

border: "none" &#124; "solid" &#124; "left" &#124; "right" &#124; "top" &#124; "bottom" (省略可) 

コントロールの境界動作。 このプロパティは、子によって継承されません。


### <a name="color"></a>色

color: string (optional) 

コンテナーの前景色。
これにより、コンテナ内のすべてのヘッダー、アイテム、ラベル、アイコンの色が変更されます。<br>
この属性を設定するときは、必要に応じて背景色を同時に設定することを検討してください。<br>
注記: 色が「テーマ」に設定されている場合、アプリケーションのテーマ色が使用されます。<br>
使用可能な色は次のとおりです。 <br>
![使用可能な色の画像](../../../media/colors.PNG)


### <a name="flexflow"></a>flexFlow

flexFlow: string (省略可) 

このプロパティを指定すると、コンポーネントがフレックス コンテナー コンポーネントになります。
このプロパティは、CSS プロパティ「flex-flow」のエイリアスです。
"flex-flow" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。


### <a name="flexsize"></a>flexSize

flexSize: string (省略可) 

1 つの番号または 2 つの番号が文字列として書き込まれています。 E.g. 「(サイズを拡大) [(サイズの縮小)]」して、即時フレックス コンテナの使用可能領域に対応します。
このプロパティは、CSS プロパティ「flex」のエイリアスです。 "flex" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。


### <a name="fontsize"></a>fontSize

fontSize: "medium" &#124; "xx-small" &#124; "x-small" &#124; "small" &#124; "large" &#124; "x-large" &#124; "xx-large" (省略可) 

比例テキスト サイズ


### <a name="fontweight"></a>fontWeight

fontWeight: "normal" &#124; "bold" (省略可) 

標準または太字のテキスト。


### <a name="justifyitems"></a>justifyItems

justifyItems: "flex-start" &#124; "flex-end" &#124; "center" &#124; "space-between" (省略可) 

このプロパティは CSS プロパティ「justify-content」のエイリアスです。
"justify-content" プロパティに関するドキュメントは、[この Web ページ](https://css-tricks.com/snippets/css/a-guide-to-flexbox)をご覧ください。


### <a name="label"></a>ラベル

label: string (省略可) 




### <a name="labelposition"></a>labelPosition

labelPosition: "stacked" &#124; "hidden" &#124; "inline" (省略可) 

ラベルの配置方法を決定します (行われる場合)。 既定では、labelPosition が stacked に設定されています。


### <a name="name"></a>名前

name: string (省略可) 




### <a name="padding"></a>padding

padding: "none" &#124; "small" &#124; "std" (省略可) 

コンポーネントのスペース動作を指定できるように許可します。
コンポーネントは、親コンテナー コンポーネントによって指定されたスペース動作を継承します。


### <a name="type"></a>タイプ

type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可) 

文字列としてのコントロールのタイプ。


