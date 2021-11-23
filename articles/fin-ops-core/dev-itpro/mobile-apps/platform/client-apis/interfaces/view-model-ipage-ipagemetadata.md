---
title: PageMetadata タイプ
description: PageMetadata タイプ
author: tonyafehr
ms.date: 08/01/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 098aece41e87e277f9401101f4ffef15c3cf4f6d
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782172"
---
# <a name="pagemetadata-type"></a>PageMetadata タイプ

[!include [banner](../../../../includes/banner.md)]

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