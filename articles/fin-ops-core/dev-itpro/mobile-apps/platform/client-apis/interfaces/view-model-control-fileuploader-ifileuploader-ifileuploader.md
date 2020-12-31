---
title: FileUploader タイプ
description: ファイル アップローダーコントロール タイプ。 イメージなどのファイルをアップロードするためのコントロールです。
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 04dbd84de9c42dc2e80a04d1bf7518a1b0ac65b8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679236"
---
# <a name="fileuploader-type"></a>FileUploader タイプ

[!include [banner](../../../../includes/banner.md)]

ファイル アップローダーコントロール タイプ。
イメージなどのファイルをアップロードするためのコントロールです。

### <a name="hierarchy"></a>階層

[値](view-model-control-value-ivalue-ivalue.md) <br>&nbsp;&nbsp;&nbsp;└─ FileUploader <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コンテナー](view-model-control-fileuploader-ifileuploader-ifileuploader.md#container)
* [ジェネリック](view-model-control-fileuploader-ifileuploader-ifileuploader.md#generic)
* [getDataSource](view-model-control-fileuploader-ifileuploader-ifileuploader.md#getdatasource)
* [非表示](view-model-control-fileuploader-ifileuploader-ifileuploader.md#hidden)
* [画像](view-model-control-fileuploader-ifileuploader-ifileuploader.md#image)

### <a name="methods"></a>メソッド

* [applyDesign](view-model-control-fileuploader-ifileuploader-ifileuploader.md#applydesign)
* [canLoadFromDevice](view-model-control-fileuploader-ifileuploader-ifileuploader.md#canloadfromdevice)
* [dataContext](view-model-control-fileuploader-ifileuploader-ifileuploader.md#datacontext)
* [getDesign](view-model-control-fileuploader-ifileuploader-ifileuploader.md#getdesign)
* [getImage](view-model-control-fileuploader-ifileuploader-ifileuploader.md#getimage)
* [getValue](view-model-control-fileuploader-ifileuploader-ifileuploader.md#getvalue)
* [isEditable](view-model-control-fileuploader-ifileuploader-ifileuploader.md#iseditable)
* [loadFromFileSystem](view-model-control-fileuploader-ifileuploader-ifileuploader.md#loadfromfilesystem)
* [メタデータ](view-model-control-fileuploader-ifileuploader-ifileuploader.md#metadata)
* [親](view-model-control-fileuploader-ifileuploader-ifileuploader.md#parent)
* [ルート](view-model-control-fileuploader-ifileuploader-ifileuploader.md#root)
* [setCamera](view-model-control-fileuploader-ifileuploader-ifileuploader.md#setcamera)
* [setValue](view-model-control-fileuploader-ifileuploader-ifileuploader.md#setvalue)

### <a name="events"></a>イベント

* [onDataChanged](view-model-control-fileuploader-ifileuploader-ifileuploader.md#ondatachanged)

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


### <a name="image"></a>image

image: [Image](view-model-control-image-iimage-iimage.md)




## <a name="methods"></a>メソッド

### <a name="applydesign"></a>applyDesign


applyDesign(IDesign: [FileUploaderDesign](view-model-control-fileuploader-ifileuploader-ifileuploaderdesign.md)): void

付与されたデザインをコントロールのデザインに適用します。
デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| IDesign|[FileUploaderDesign](view-model-control-fileuploader-ifileuploader-ifileuploaderdesign.md)|デザイン プロパティをキーとして含むオブジェクト|

#### <a name="returns-void"></a>void を返します

### <a name="canloadfromdevice"></a>canLoadFromDevice


canLoadFromDevice(): boolean

携帯電話にカメラ プラグインがある場合は、true を返します。

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="datacontext"></a>dataContext


dataContext(): any



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承

#### <a name="returns-any"></a>any を返します

### <a name="getdesign"></a>getDesign


getDesign(): [Design](view-model-ipage-idesign.md)

このコントロールのデザイン オブジェクトを返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承

#### <a name="returns-design"></a>[Design](view-model-ipage-idesign.md) を返します



### <a name="getimage"></a>getImage


getImage(options: any): Promise &lt;string&gt;

画像データを持つオブジェクトの約定を返します。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| オプション|any|[カメラのオプション](https://github.com/apache/cordova-plugin-camera#module_camera.CameraOptions) を参照してください|

#### <a name="returns-promise-ltstringgt"></a>Promise &lt;string&gt; を返します



### <a name="getvalue"></a>getValue


getValue(): any

コントロールにバインドされているエンティティの値を取得します。

> [Value](view-model-control-value-ivalue-ivalue.md).[getValue](view-model-control-value-ivalue-ivalue.md#getvalue) をオーバーライドします。

#### <a name="returns-any"></a>any を返します



### <a name="iseditable"></a>isEditable


isEditable(): boolean

コントロールが編集可能かどうかを示すブール値。
コントロールまたはその親が編集可能でない場合は、false を返します。
コントロールとその親の両方が編集可能な場合、true を返します。
コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。
コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="loadfromfilesystem"></a>loadFromFileSystem


loadFromFileSystem(file: Blob): Promise &lt;any&gt;




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| ファイル|BLOB||

#### <a name="returns-promise-ltanygt"></a>Promise &lt;any&gt; を返します

### <a name="metadata"></a>metadata


metadata(): [FileUploaderMetadata](view-model-control-fileuploader-ifileuploader-ifileuploadermetadata.md)

このコントロールのメタデータ オブジェクトを返します。

> [Value](view-model-control-value-ivalue-ivalue.md).[metadata](view-model-control-value-ivalue-ivalue.md#metadata) をオーバーライドします。

#### <a name="returns-fileuploadermetadata"></a>[FileUploaderMetadata](view-model-control-fileuploader-ifileuploader-ifileuploadermetadata.md) を返します



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



### <a name="setcamera"></a>setCamera


setCamera(camera: any): void

コントロールでカメラ オブジェクトを設定します。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| カメラ|any||

#### <a name="returns-void"></a>void を返します

### <a name="setvalue"></a>setValue


setValue(value: string): void

コントロールの値を設定します。

> [Value](view-model-control-value-ivalue-ivalue.md).[setValue](view-model-control-value-ivalue-ivalue.md#setvalue) から継承


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| 値|string||

#### <a name="returns-void"></a>void を返します

## <a name="events"></a>イベント

### <a name="ondatachanged"></a>onDataChanged

onDataChanged: [EventHook](event-ievent-ieventhook.md) &lt;null&gt;

入力コントロールのデータが変更されたときに発生するイベントです。

> [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md).[onDataChanged](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md#ondatachanged) から継承


