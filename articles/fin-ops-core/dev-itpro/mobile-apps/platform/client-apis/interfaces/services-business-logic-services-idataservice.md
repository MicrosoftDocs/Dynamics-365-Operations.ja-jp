---
title: DataService タイプ
description: アプリケーション ワークスペースの下でデータ アクセス機能を提供します。
author: robinarh
ms.date: 08/01/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.openlocfilehash: 4254ed9fa59d7f07e191b880226caf64d2f6a2847c2e14c3e5bb12c292e3e3a9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714571"
---
# <a name="dataservice-type"></a>DataService タイプ

[!include [banner](../../../../includes/banner.md)]

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