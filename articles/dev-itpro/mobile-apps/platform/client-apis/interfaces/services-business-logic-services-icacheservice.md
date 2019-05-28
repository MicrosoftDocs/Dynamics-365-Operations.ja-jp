---
title: CacheService タイプ
description: デバイス キャッシュからデータにアクセスし、デバイス キャッシュにデータを更新する機能を提供します。
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
ms.openlocfilehash: 97c09131d964a7a9d1affc5cd03696e4581b0e0d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506049"
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

