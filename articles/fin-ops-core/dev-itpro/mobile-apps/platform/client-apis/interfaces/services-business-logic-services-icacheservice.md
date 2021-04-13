---
title: CacheService タイプ
description: デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。
author: robinarh
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82a7e62936a15d9cc482f3c84935ed6560aacce8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744207"
---
# <a name="cacheservice-type"></a>CacheService タイプ

[!include [banner](../../../../includes/banner.md)]

デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。

### <a name="hierarchy"></a>階層

CacheService <br>

## <a name="index"></a>指数

### <a name="methods"></a>メソッド

* [getData](services-business-logic-services-icacheservice.md#getdata)
* [setData](services-business-logic-services-icacheservice.md#setdata)

## <a name="methods"></a>メソッド

### <a name="getdata"></a>getData


getData(cacheKey: string): any




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| cacheKey|string||

#### <a name="returns-any"></a>any を返します

### <a name="setdata"></a>setData


setData(cacheKey: string, data: any): any




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| cacheKey|string||
| データ|any||

#### <a name="returns-any"></a>any を返します



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]