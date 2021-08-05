---
title: CacheService タイプ
description: デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。
author: robinarh
ms.date: 08/01/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.openlocfilehash: d75c3455f3640b3890761e4b29817028b35ea955
ms.sourcegitcommit: ff5e892a91a1585472af2191ae45d6291cceb7f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2021
ms.locfileid: "6661508"
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