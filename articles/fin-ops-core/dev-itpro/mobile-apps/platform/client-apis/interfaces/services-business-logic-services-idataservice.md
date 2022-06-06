---
title: DataService タイプ
description: アプリケーション ワークスペースの下でデータ アクセス機能を提供します。
author: tonyafehr
ms.date: 05/24/2022
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: a4c24511ace4c678d81bb4993a0a1337cc8ef95e
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811224"
---
# <a name="dataservice-type"></a>DataService タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

アプリケーション ワークスペースの下でデータ アクセス機能を提供します。

### <a name="hierarchy"></a>階層

DataService <br>

## <a name="index"></a>指数

### <a name="methods"></a>メソッド

* [findEntityData](services-business-logic-services-idataservice.md#findentitydata)
* [getEntityData](services-business-logic-services-idataservice.md#getentitydata)
* [getPageData](services-business-logic-services-idataservice.md#getpagedata)

## <a name="methods"></a>メソッド

### <a name="findentitydata"></a>findEntityData


findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| entityType|any||
| propertyName|string||
| propertyValue|any||
| includeChanges?|ブール値||

#### <a name="returns-any"></a>any を返します

### <a name="getentitydata"></a>getEntityData


getEntityData(entityType: any, entityId: string): any




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| entityType|any||
| entityId|string||

#### <a name="returns-any"></a>any を返します

### <a name="getpagedata"></a>getPageData


getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt;




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| pageId|string||
| context|any||
| フィルタ|any||
| allowedStaleness|数値||

#### <a name="returns-promise-ltpagedatagt"></a>Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt; を返します



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
