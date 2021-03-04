---
title: NavigationArgs タイプ
description: NavigationArgs タイプ
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
ms.openlocfilehash: 0e49d8fbbed1c70ffe6754512bc1d81c125ee21e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688493"
---
# <a name="navigationargs-type"></a>NavigationArgs タイプ

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a>階層

[PageTarget](view-model-ipage-ipagetarget.md) <br>&nbsp;&nbsp;&nbsp;└─ NavigationArgs <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [ラベル](view-model-ipage-inavigationargs.md#label)
* [オプション](view-model-ipage-inavigationargs.md#options)
* [パラメーター](view-model-ipage-inavigationargs.md#params)
* [置換](view-model-ipage-inavigationargs.md#replace)
* [to](view-model-ipage-inavigationargs.md#to)
* [url](view-model-ipage-inavigationargs.md#url)

## <a name="properties"></a>プロパティ

### <a name="label"></a>ラベル

label: string (省略可) 




### <a name="options"></a>オプション

options: any (省略可) 




### <a name="params"></a>params

params: [PageOptions](view-model-ipage-ipageoptions.md) (省略可) 



> [PageTarget](view-model-ipage-ipagetarget.md).[params](view-model-ipage-ipagetarget.md#params) から継承


### <a name="replace"></a>置換

replace: boolean (省略可) 

true と設定されている場合は、ナビゲーション履歴スタックから現在のビューの起動ナビゲーションを削除します。


### <a name="to"></a>終了

to: string (省略可) 



> [PageTarget](view-model-ipage-ipagetarget.md).[to](view-model-ipage-ipagetarget.md#to) から継承


### <a name="url"></a>URL

url: string (省略可) 

指定した場合、このリンクは直接開かれます。




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]