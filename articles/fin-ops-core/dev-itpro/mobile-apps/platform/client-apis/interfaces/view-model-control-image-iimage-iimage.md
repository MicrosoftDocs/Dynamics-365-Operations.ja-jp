---
title: 画像タイプ
description: モバイル アプリ内のイメージを表すためのイメージ コントロール インターフェイス。
author: jasongre
ms.date: 05/24/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: eb0f9ed153fbfbab7a3291c795dd6d8f737e8722
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274643"
---
# <a name="image-type"></a>画像タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

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

#### <a name="returns-design"></a>[Design](view-model-ipage-idesign.md) を返します



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

#### <a name="returns-imagemetadata"></a>[ImageMetadata](view-model-control-image-iimage-iimagemetadata.md) を返します



### <a name="parent"></a>parent


parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)

このコントロールの親 (コントロールまたはページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承

#### <a name="returns-control-124-page"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します



### <a name="root"></a>root


root(): [Page](view-model-ipage-ipage.md)

このコントロールのルート フォーム インスタンス (ページ) を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承

#### <a name="returns-page"></a>[Page](view-model-ipage-ipage.md) を返します





[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
