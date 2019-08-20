---
title: 画像タイプ
description: モバイル アプリ内のイメージを表すためのイメージ コントロール インターフェイス。 イメージは、次のいずれかの種類が使用できます&amp;58 DataUri、Base64、URL、AOTResource、または Symbol。
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
ms.openlocfilehash: ba2c10ad3bf87058793034b2979759cb042b5a63
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851603"
---
# <a name="image-type"></a>画像タイプ

[!include [banner](../../../../includes/banner.md)]

モバイル アプリ内のイメージを表すためのイメージ コントロール インターフェイス。
イメージは、次のいずれかの種類を使用できます。DataUri、Base64、URL、AOTResource、または Symbol。

### <a name="hierarchy"></a>階層

[コントロール](view-model-control-basecontrol-icontrol-icontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ 画像 <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コンテナー](view-model-control-image-iimage-iimage.md#container)
* [ジェネリック](view-model-control-image-iimage-iimage.md#generic)
* [getDataSource](view-model-control-image-iimage-iimage.md#getdatasource)
* [非表示](view-model-control-image-iimage-iimage.md#hidden)
* [imageSource](view-model-control-image-iimage-iimage.md#imagesource)
* [imageView](view-model-control-image-iimage-iimage.md#imageview)
* [placeholderClass](view-model-control-image-iimage-iimage.md#placeholderclass)
* [記号](view-model-control-image-iimage-iimage.md#symbol)

### <a name="methods"></a>メソッド

* [applyDesign](view-model-control-image-iimage-iimage.md#applydesign)
* [dataContext](view-model-control-image-iimage-iimage.md#datacontext)
* [getDesign](view-model-control-image-iimage-iimage.md#getdesign)
* [isEditable](view-model-control-image-iimage-iimage.md#iseditable)
* [メタデータ](view-model-control-image-iimage-iimage.md#metadata)
* [親](view-model-control-image-iimage-iimage.md#parent)
* [ルート](view-model-control-image-iimage-iimage.md#root)

## <a name="properties"></a>プロパティ

### <a name="container"></a>コンテナー

container: ブール値 (省略可) 

コントロールがコンテナーの場合は true です。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) から継承


### <a name="generic"></a>generic

generic: boolean (省略可) 



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承


### <a name="getdatasource"></a>getDataSource

getDataSource: function(): any



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承


### <a name="hidden"></a>hidden

hidden: boolean

コントロールが非常時の場合は true です。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承


### <a name="imagesource"></a>imageSource

imageSource: string

ImageSource を定義します。


### <a name="imageview"></a>imageView

imageView: string

画像のスタイルを決定します。


### <a name="placeholderclass"></a>placeholderClass

placeholderClass: string




### <a name="symbol"></a>symbol

symbol: string

イメージがシンボル型である場合、シンボルを定義します。


## <a name="methods"></a>メソッド

### <a name="applydesign"></a>applyDesign


applyDesign(design: [ImageDesign](view-model-control-image-iimage-iimagedesign.md)): void

付与されたデザインをコントロールのデザインに適用します。
デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| design|[ImageDesign](view-model-control-image-iimage-iimagedesign.md)|デザイン プロパティをキーとして含むオブジェクト|

#### <a name="returns-void"></a>void を返します

### <a name="datacontext"></a>dataContext


dataContext(): any



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承

#### <a name="returns-any"></a>any を返します

### <a name="getdesign"></a>getDesign


getDesign(): [Design](view-model-ipage-idesign.md)

このコントロールのデザイン オブジェクトを返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承

#### <a name="returns-designview-model-ipage-idesignmd"></a>[Design](view-model-ipage-idesign.md) を返します



### <a name="iseditable"></a>isEditable


isEditable(): boolean

コントロールが編集可能かどうかを示すブール値。
コントロールまたはその親が編集可能でない場合は、false を返します。
コントロールとその親の両方が編集可能な場合、true を返します。
コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。
コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="metadata"></a>metadata


metadata(): [ImageMetadata](view-model-control-image-iimage-iimagemetadata.md)

このコントロールのメタデータ オブジェクトを返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[metadata](view-model-control-basecontrol-icontrol-icontrol.md#metadata) をオーバーライドします。

#### <a name="returns-imagemetadataview-model-control-image-iimage-iimagemetadatamd"></a>[ImageMetadata](view-model-control-image-iimage-iimagemetadata.md) を返します



### <a name="parent"></a>parent


parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)

このコントロールの親 (コントロールまたはページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd-124-pageview-model-ipage-ipagemd"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します



### <a name="root"></a>root


root(): [Page](view-model-ipage-ipage.md)

このコントロールのルート フォーム インスタンス (ページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承

#### <a name="returns-pageview-model-ipage-ipagemd"></a>[Page](view-model-ipage-ipage.md) を返します



