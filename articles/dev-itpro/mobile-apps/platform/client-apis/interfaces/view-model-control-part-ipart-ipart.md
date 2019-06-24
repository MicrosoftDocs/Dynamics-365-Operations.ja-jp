---
title: Part タイプ
description: パーツ コントロール タイプ。 パーツは、ページのみを含むコンテナー コントロールで、ページがページ内に埋め込まれるのを許可します。
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
ms.openlocfilehash: 67bd5662259f11a5f148c4ac2f815172bf721813
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547356"
---
# <a name="part-type"></a>Part タイプ

[!include [banner](../../../../includes/banner.md)]

パーツ コントロール タイプ。 パーツは、ページのみを含むコンテナー コントロールで、ページがページ内に埋め込まれるのを許可します。

### <a name="hierarchy"></a>階層

[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ パート <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コンテナー](view-model-control-part-ipart-ipart.md#container)
* [ジェネリック](view-model-control-part-ipart-ipart.md#generic)
* [getDataSource](view-model-control-part-ipart-ipart.md#getdatasource)
* [非表示](view-model-control-part-ipart-ipart.md#hidden)

### <a name="methods"></a>メソッド

* [applyDesign](view-model-control-part-ipart-ipart.md#applydesign)
* [dataContext](view-model-control-part-ipart-ipart.md#datacontext)
* [getControl](view-model-control-part-ipart-ipart.md#getcontrol)
* [getControlById](view-model-control-part-ipart-ipart.md#getcontrolbyid)
* [getDesign](view-model-control-part-ipart-ipart.md#getdesign)
* [getEntityRef](view-model-control-part-ipart-ipart.md#getentityref)
* [getPartPage](view-model-control-part-ipart-ipart.md#getpartpage)
* [hasTarget](view-model-control-part-ipart-ipart.md#hastarget)
* [isEditable](view-model-control-part-ipart-ipart.md#iseditable)
* [メタデータ](view-model-control-part-ipart-ipart.md#metadata)
* [親](view-model-control-part-ipart-ipart.md#parent)
* [ルート](view-model-control-part-ipart-ipart.md#root)

## <a name="properties"></a>プロパティ

### <a name="container"></a>コンテナー

container: ブール値

コントロールがコンテナーの場合は true です。

> [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[container](view-model-control-container-icontainercontrol-icontainercontrol.md#container) から継承
> 
> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) をオーバーライドします。


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


## <a name="methods"></a>メソッド

### <a name="applydesign"></a>applyDesign


applyDesign(IDesign: [PartDesign](view-model-control-part-ipart-ipartdesign.md)): void

付与されたデザインをコントロールのデザインに適用します。
デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| IDesign|[PartDesign](view-model-control-part-ipart-ipartdesign.md)|デザイン プロパティをキーとして含むオブジェクト|

#### <a name="returns-void"></a>void を返します

### <a name="datacontext"></a>dataContext


dataContext(): any



> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承

#### <a name="returns-any"></a>any を返します

### <a name="getcontrol"></a>getControl


getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)

コントロールの名前の場合、コントロール インスタンスを返します。

> [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControl](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol) から継承


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| controlName|string|コントロール名|

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します



### <a name="getcontrolbyid"></a>getControlById


getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)

コントロールの ID の場合、コントロール インスタンスを返します。

> [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControlById](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid) から継承


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| id|string|コントロール ID|

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します



### <a name="getdesign"></a>getDesign


getDesign(): [Design](view-model-ipage-idesign.md)

このコントロールのデザイン オブジェクトを返します。

> [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承

#### <a name="returns-designview-model-ipage-idesignmd"></a>[Design](view-model-ipage-idesign.md) を返します



### <a name="getentityref"></a>getEntityRef


getEntityRef(): string

コントロールにバインドする entityRef の値を取得します。

#### <a name="returns-string"></a>文字列を返します



### <a name="getpartpage"></a>getPartPage


getPartPage(): [Page](view-model-ipage-ipage.md)

パーツのページを取得します。

#### <a name="returns-pageview-model-ipage-ipagemd"></a>[Page](view-model-ipage-ipage.md) を返します



### <a name="hastarget"></a>hasTarget


hasTarget(): boolean

部品にターゲット ページがある場合は、true を返します。

#### <a name="returns-boolean"></a>ブール値を返します



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


metadata(): [PartMetadata](view-model-control-part-ipart-ipartmetadata.md)

このコントロールのメタデータ オブジェクトを返します。

> [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[metadata](view-model-control-container-icontainercontrol-icontainercontrol.md#metadata) をオーバーライドします。

#### <a name="returns-partmetadataview-model-control-part-ipart-ipartmetadatamd"></a>[PartMetadata](view-model-control-part-ipart-ipartmetadata.md) を返します



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



