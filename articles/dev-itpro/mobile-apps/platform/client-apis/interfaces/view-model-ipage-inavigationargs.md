---
title: "NavigationArgs タイプ"
description: "NavigationArgs タイプ"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b1e38920b7a3d529eebfd5b5039591aaaf88a79d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

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



