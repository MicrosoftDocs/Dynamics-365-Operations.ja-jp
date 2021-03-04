---
title: DataService タイプ
description: アプリケーション ワークスペースの下でデータ アクセス機能を提供します。
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
ms.openlocfilehash: 10ef31bcff5eee93b3f0925ce3d8b34a999e275a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687853"
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