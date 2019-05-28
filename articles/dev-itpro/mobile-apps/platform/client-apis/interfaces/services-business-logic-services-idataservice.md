---
title: DataService タイプ
description: アプリケーション ワークスペースの下でデータ アクセス機能を提供します。
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
ms.openlocfilehash: 0e44e8ff9df7d65398bf87a7b7027e1696515164
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537157"
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

#### <a name="returns-promise-ltpagedataservices-business-logic-services-ipagedatamdgt"></a>Promise &lt;[PageData](services-business-logic-services-ipagedata.md)&gt; を返します

