---
title: コントロール タイプ
description: すべてのコントロールの基準メソッドと属性を持つコントロール インターフェイス。 これは、コントロールのランタイムのインスタンスを表します。
author: jasongre
ms.date: 05/24/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: 038522e6d5362299db6fcf09d5768d60fcbe7a06
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284048"
---
# <a name="control-type"></a>コントロール タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

すべてのコントロールの基準メソッドと属性を持つコントロール インターフェイス。
これは、コントロールのランタイムのインスタンスを表します。 プロパティの変更は、UI にすぐに反映されます。

### <a name="hierarchy"></a>階層

状態 <br>&nbsp;&nbsp;&nbsp;└─ [PageLink](view-model-control-pagelink-ipagelink-ipagelink.md) <br>&nbsp;&nbsp;&nbsp;└─ [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ [InputControl](view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ [画像](view-model-control-image-iimage-iimage.md) <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コンテナー](view-model-control-basecontrol-icontrol-icontrol.md#container)
* [ジェネリック](view-model-control-basecontrol-icontrol-icontrol.md#generic)
* [getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)
* [非表示](view-model-control-basecontrol-icontrol-icontrol.md#hidden)

### <a name="methods"></a>メソッド

* [applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)
* [dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)
* [getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)
* [isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)
* [メタデータ](view-model-control-basecontrol-icontrol-icontrol.md#metadata)
* [親](view-model-control-basecontrol-icontrol-icontrol.md#parent)
* [ルート](view-model-control-basecontrol-icontrol-icontrol.md#root)

## <a name="properties"></a>プロパティ

### <a name="container"></a>コンテナー

container: ブール値 (省略可) 

コントロールがコンテナーの場合は true です。


### <a name="generic"></a>generic

generic: boolean (省略可) 




### <a name="getdatasource"></a>getDataSource

getDataSource: function(): any




### <a name="hidden"></a>hidden

hidden: boolean

コントロールが非常時の場合は true です。


## <a name="methods"></a>メソッド

### <a name="applydesign"></a>applyDesign


applyDesign(design: [Design](view-model-ipage-idesign.md)): void

付与されたデザインをコントロールのデザインに適用します。
デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| design|[Design](view-model-ipage-idesign.md)|デザイン プロパティをキーとして含むオブジェクト|

#### <a name="returns-void"></a>void を返します

### <a name="datacontext"></a>dataContext


dataContext(): any



#### <a name="returns-any"></a>any を返します

### <a name="getdesign"></a>getDesign


getDesign(): [Design](view-model-ipage-idesign.md)

このコントロールのデザイン オブジェクトを返します。

#### <a name="returns-design"></a>[Design](view-model-ipage-idesign.md) を返します



### <a name="iseditable"></a>isEditable


isEditable(): boolean

コントロールが編集可能かどうかを示すブール値。
コントロールまたはその親が編集可能でない場合は、false を返します。
コントロールとその親の両方が編集可能な場合、true を返します。
コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。
コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="metadata"></a>metadata


metadata(): [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)

このコントロールのメタデータ オブジェクトを返します。

#### <a name="returns-controlmetadata"></a>[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) を返します



### <a name="parent"></a>parent


parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)

このコントロールの親 (コントロールまたはページ) を返します。

#### <a name="returns-control-124-page"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します



### <a name="root"></a>root


root(): [Page](view-model-ipage-ipage.md)

このコントロールのルート フォーム インスタンス (ページ) を返します。

#### <a name="returns-page"></a>[Page](view-model-ipage-ipage.md) を返します





[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
