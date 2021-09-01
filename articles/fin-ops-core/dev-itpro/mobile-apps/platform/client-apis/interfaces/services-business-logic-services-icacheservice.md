---
title: CacheService タイプ
description: デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。
author: robinarh
ms.date: 08/01/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.openlocfilehash: cb9c1566a1e7d784c7a5cd1574b39b19da6bb9945276922f35d17df52bc77904
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769177"
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