---
title: 管理モジュール
description: コントロールは、ページのコンテンツを構成するものです。
author: jasongre
ms.date: 05/26/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: 864b59bffe17d1859854a87c3e0d539be3105928
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279378"
---
# <a name="control-module"></a>管理モジュール

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

コントロールは、ページのコンテンツを構成するものです。

## <a name="index"></a>指数

### <a name="types"></a>種類

* [コントロール](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md)
* [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)

### <a name="type-aliases"></a>型のエイリアス

* [ControlType](view-model-control-basecontrol-icontrol.md#controltype)

## <a name="types"></a>種類


### <a name="control"></a>状態

#### <a name="hierarchy"></a>階層

状態 <br>&nbsp;&nbsp;&nbsp;└─ [PageLink](../interfaces/view-model-control-pagelink-ipagelink-ipagelink.md) <br>&nbsp;&nbsp;&nbsp;└─ [ContainerControl](../interfaces/view-model-control-container-icontainercontrol-icontainercontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ [InputControl](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrol.md) <br>&nbsp;&nbsp;&nbsp;└─ [画像](../interfaces/view-model-control-image-iimage-iimage.md) <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [コンテナー](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#container) |container: ブール値 (省略可)  <br>|コントロールがコンテナーの場合は true です。<br>  |
| [ジェネリック](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#generic) |generic: boolean (省略可)  <br>|  |
| [getDataSource](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) |getDataSource: function(): any <br>|  |
| [非表示](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#hidden) |hidden: boolean <br>|コントロールが非常時の場合は true です。<br>  |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [applyDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#applydesign) |applyDesign(design: [Design](../interfaces/view-model-ipage-idesign.md)): void|付与されたデザインをコントロールのデザインに適用します。<br>  |
| [dataContext](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#datacontext) |dataContext(): any|  |
| [getDesign](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#getdesign) |getDesign(): [Design](../interfaces/view-model-ipage-idesign.md)|このコントロールのデザイン オブジェクトを返します。<br>  |
| [isEditable](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#iseditable) |isEditable(): boolean|コントロールが編集可能かどうかを示すブール値。<br>  |
| [メタデータ](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#metadata) |metadata(): [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)|このコントロールのメタデータ オブジェクトを返します。<br>  |
| [親](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#parent) |parent(): [Control](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールの親 (コントロールまたはページ) を返します。<br>  |
| [ルート](../interfaces/view-model-control-basecontrol-icontrol-icontrol.md#root) |root(): [Page](../interfaces/view-model-ipage-ipage.md)|このコントロールのルート フォーム インスタンス (ページ) を返します。<br>  |


### <a name="controlmetadata"></a>ControlMetadata

#### <a name="hierarchy"></a>階層

ControlMetadata <br>&nbsp;&nbsp;&nbsp;└─ [PageLinkMetadata](../interfaces/view-model-control-pagelink-ipagelink-ipagelinkmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ [ContainerControlMetadata](../interfaces/view-model-control-container-icontainercontrol-icontainercontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ [InputControlMetadata](../interfaces/view-model-control-basecontrol-iinputcontrol-iinputcontrolmetadata.md) <br>&nbsp;&nbsp;&nbsp;└─ [ImageMetadata](../interfaces/view-model-control-image-iimage-iimagemetadata.md) <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [BoundEntity](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) |BoundEntity: 文字列 (オプション)  <br>|コントロールがバインドされるエンティティ。<br>  |
| [BoundField](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) |BoundField: 文字列 (オプション)  <br>|  |
| [説明](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) |説明:文字列 (オプション)  <br>|コントロールの説明。<br>  |
| [編集可能](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) |編集可能: プール値 (省略可)  <br>|コントロールが編集可能かどうかを示すブール値。<br>  |
| [ExtType](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) |ExtType: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|拡張されたコントロール タイプです。 たとえば、コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。<br>  |
| [HelpText](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) |HelpText: 文字列 (オプション)  <br>|コマンドのキーボード ショートカットです。 たとえば、「(Shift + F5)」<br>  |
| [非表示](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) |非表示: ブール値 (オプション)  <br>|コントロールを非表示にするかどうかを示すブール値。<br>  |
| [ID](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) |Id: string (オプション)  <br>|コントロールの ID 文字列です。<br>  |
| [ラベル](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) |ラベル: 文字列 (省略可)  <br>|コントロールのラベル。 たとえば、個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。<br>  |
| [名前](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) |Name: 文字列 (省略可)  <br>|コントロールの名前です。<br>  |
| [注文](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) |注文: 番号 (オプション)  <br>|コントロールがページに表示される順序を示す番号。<br>  |
| [タイプ](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) |Type: [ControlType](view-model-control-basecontrol-icontrol.md#controltype) (省略可)  <br>|コントロール タイプを示す文字列。<br>  |

## <a name="type-aliases"></a>型のエイリアス


### <a name="controltype"></a>ControlType
ControlType: 「FileUpload」 &#124; 「バーコード」 &#124; 「入力」 &#124; 「MultilineInput」 &#124; 「ナビゲーション」 &#124; 「整数」 &#124; 「Int64」 &#124; 「日付」 &#124; 「日時」 &#124; 「ComboBox」 &#124; 「実数」 &#124; 「リスト」 &#124; 「ルックアップ」 &#124; 「MultiLookup」 &#124; 「ナビゲーション」 &#124; 「画像」 &#124; 「グループ」 &#124; 「パート」 &#124; 「カレンダー」 &#124; 「ハイパーリンク」 &#124; 「タイマー」


コントロールには、ControlType にリストされているタイプのいずれかを割り当てる必要があります。



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
