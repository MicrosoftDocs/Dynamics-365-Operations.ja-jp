---
title: PageMetadata タイプ
description: PageMetadata タイプ
author: jasongre
ms.date: 05/26/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: 4db855f9a23839a047f65aad5ed6a5d224d5e182
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283480"
---
# <a name="pagemetadata-type"></a>PageMetadata タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

### <a name="hierarchy"></a>階層

PageMetadata

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [コントロール](view-model-ipage-ipagemetadata.md#controls)
* [デザイン](view-model-ipage-ipagemetadata.md#design)
* [ID](view-model-ipage-ipagemetadata.md#id)
* [QuickSubmit](view-model-ipage-ipagemetadata.md#quicksubmit)
* [SourcePageId](view-model-ipage-ipagemetadata.md#sourcepageid)
* [SubmitButtonDesign](view-model-ipage-ipagemetadata.md#submitbuttondesign)
* [仕事](view-model-ipage-ipagemetadata.md#tasks)
* [肩書き](view-model-ipage-ipagemetadata.md#title)

### <a name="events"></a>イベント

* [OnDataLoaded](view-model-ipage-ipagemetadata.md#ondataloaded)
* [OnInit](view-model-ipage-ipagemetadata.md#oninit)
* [OnPreInit](view-model-ipage-ipagemetadata.md#onpreinit)
* [OnSubmit](view-model-ipage-ipagemetadata.md#onsubmit)
* [OnTaskSubmitted](view-model-ipage-ipagemetadata.md#ontasksubmitted)
* [OnTaskSubmitting](view-model-ipage-ipagemetadata.md#ontasksubmitting)

## <a name="properties"></a>プロパティ

### <a name="controls"></a>コントロール

コントロール: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)\[\] (オプション) 

### <a name="design"></a>デザイン

デザイン: [デザイン](view-model-ipage-idesign.md) (オプション) 




### <a name="id"></a>ID

ID: string (オプション) 




### <a name="quicksubmit"></a>QuickSubmit

QuickSubmit: ブール値 (省略可) 




### <a name="sourcepageid"></a>SourcePageId

SourcePageId: 文字列 (省略可) 




### <a name="submitbuttondesign"></a>SubmitButtonDesign

SubmitButtonDesign: [デザイン](view-model-ipage-idesign.md) (省略可) 




### <a name="tasks"></a>仕事

仕事: [PageMetadata](view-model-ipage-ipagemetadata.md)\[\] (オプション) 




### <a name="title"></a>肩書き

タイトル: 文字列 (省略可) 




## <a name="events"></a>イベント

### <a name="ondataloaded"></a>OnDataLoaded

OnDataLoaded: 機能 (送信者: [ページ](view-model-ipage-ipage.md)、dataWrapper: すべて): 無効 (オプション) 




### <a name="oninit"></a>OnInit

OnInit: 機能 (送信者: [ページ](view-model-ipage-ipage.md)): 無効 (オプション) 




### <a name="onpreinit"></a>OnPreInit

OnPreInit: 機能 (送信者: [ページ](view-model-ipage-ipage.md)): 無効 (オプション) 




### <a name="onsubmit"></a>OnSubmit

OnSubmit: 機能 (dataValues: すべて、args: すべて): 無効 (オプション) 




### <a name="ontasksubmitted"></a>OnTaskSubmitted

OnTaskSubmitted: 機能 (taskHandle: すべて、taskOptions: すべて): すべて (オプション) 




### <a name="ontasksubmitting"></a>OnTaskSubmitting

OnTaskSubmitted: 機能 (taskOptions: すべて): すべて (オプション) 






[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
