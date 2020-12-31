---
title: サービス モジュール
description: クライアントの実行時に、アプリケーションで使用できるさまざまなサービス。
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
ms.openlocfilehash: dc46ff863d03275f4311cc0e547ab34611675d12
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687858"
---
# <a name="services-module"></a>サービス モジュール

[!include [banner](../../../../includes/banner.md)]

クライアントの実行時に、アプリケーションで使用できるさまざまなサービス。

## <a name="index"></a>指数

### <a name="types"></a>種類

* [AsyncService](../interfaces/services-business-logic-services-iasyncservice.md)
* [CacheService](../interfaces/services-business-logic-services-icacheservice.md)
* [DataService](../interfaces/services-business-logic-services-idataservice.md)
* [MetadataService](../interfaces/services-business-logic-services-imetadataservice.md)
* [PageData](../interfaces/services-business-logic-services-ipagedata.md)

### <a name="type-aliases"></a>型のエイリアス

* [ExpressionOperator](services-business-logic-services.md#expressionoperator)

## <a name="types"></a>種類


### <a name="asyncservice"></a>AsyncService

#### <a name="hierarchy"></a>階層

AsyncService <br>

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [すべて](../interfaces/services-business-logic-services-iasyncservice.md#all) |all(...args: any [ ]): Promise &lt;any [ ]&gt;|  |
| [延期](../interfaces/services-business-logic-services-iasyncservice.md#defer) |defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;|イベント ハンドラー (該当する場合) から回答を返し、非同期でそれらを拒否または解決するために使用できる遅延オブジェクトを作成します。<br>  |


### <a name="cacheservice"></a>CacheService

#### <a name="hierarchy"></a>階層

CacheService <br>

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [getData](../interfaces/services-business-logic-services-icacheservice.md#getdata) |getData(cacheKey: string): any|  |
| [setData](../interfaces/services-business-logic-services-icacheservice.md#setdata) |setData(cacheKey: string, data: any): any|  |


### <a name="dataservice"></a>DataService

#### <a name="hierarchy"></a>階層

DataService <br>

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [findEntityData](../interfaces/services-business-logic-services-idataservice.md#findentitydata) |findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any|  |
| [getEntityData](../interfaces/services-business-logic-services-idataservice.md#getentitydata) |getEntityData(entityType: any, entityId: string): any|  |
| [getPageData](../interfaces/services-business-logic-services-idataservice.md#getpagedata) |getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](../interfaces/services-business-logic-services-ipagedata.md)&gt;|  |


### <a name="metadataservice"></a>MetadataService

#### <a name="hierarchy"></a>階層

MetadataService <br>

#### <a name="properties"></a>プロパティ

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [バージョン](../interfaces/services-business-logic-services-imetadataservice.md#version) |version: string <br>|現在実行中のプラットフォームのバージョンを取得します。<br>  |

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [addControl](../interfaces/services-business-logic-services-imetadataservice.md#addcontrol) |addControl(componentName: string, controlName: string, controlType: [ControlType](view-model-control-basecontrol-icontrol.md#controltype), parentContainerName?: string, options?: [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any|  |
| [compareVersion](../interfaces/services-business-logic-services-imetadataservice.md#compareversion) |compareVersion(versionToCompare: string): 1 &#124; -1|現在のプラットフォームのバージョンと参照バージョンを比較します。<br>  |
| [configureAction](../interfaces/services-business-logic-services-imetadataservice.md#configureaction) |configureAction(actionName: string, options: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)): any|アクションをコンフィギュレーションすると、そのアクションに固有の特定の動作を指定または上書きできます。<br>  |
| [configureControl](../interfaces/services-business-logic-services-imetadataservice.md#configurecontrol) |configureControl(componentName: string, controlName: string, options: [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any|コントロールをコンフィギュレーションすると、そのコントロールに固有の特定の動作を指定または上書きできます。 使用可能な動作はコントロール タイプで異なることに注意してください。<br>  |
| [configureEntity](../interfaces/services-business-logic-services-imetadataservice.md#configureentity) |configureEntity(entityName: string, options: any): any|エンティティをコンフィギュレーションすると、そのエンティティに固有の特定の動作を指定または上書きできます。<br>  |
| [configureLookup](../interfaces/services-business-logic-services-imetadataservice.md#configurelookup) |configureLookup(taskName: string, lookupControlName: string, options: [LookupMetadata](../interfaces/view-model-control-lookup-ilookup-ilookupmetadata.md)): any|アクションのフィールドをルックアップとして動作するようにコンフィギュレーションします。 リスト コントロールを含む既存のページを使用する必要があります。<br>  |
| [configurePage](../interfaces/services-business-logic-services-imetadataservice.md#configurepage) |configurePage(pageName: string, options: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)): any|ページをコンフィギュレーションすると、そのページに固有の特定の動作を指定または上書きできます。<br>  |
| [configureWorkspace](../interfaces/services-business-logic-services-imetadataservice.md#configureworkspace) |configureWorkspace(options: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)): any|ワークスペースをコンフィギュレーションすると、そのワークスペースに固有の特定の動作を指定または上書きできます。<br>  |
| [findAction](../interfaces/services-business-logic-services-imetadataservice.md#findaction) |findAction(actionName: string): [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)|メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたアクションの現在のメタデータ インスタンスのコピーを取得します。<br>  |
| [findControl](../interfaces/services-business-logic-services-imetadataservice.md#findcontrol) |findControl(componentMetadata: any, controlName: string): [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)|メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたコントロールの現在のメタデータ インスタンスのコピーを取得します。<br>  |
| [findPage](../interfaces/services-business-logic-services-imetadataservice.md#findpage) |findPage(pageName: string): [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)|メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたページの現在のメタデータ インスタンスのコピーを取得します。<br>  |
| [getFilterExpression](../interfaces/services-business-logic-services-imetadataservice.md#getfilterexpression) |getFilterExpression(pageName: string, listControlName: string, controlName: string, operator: [ExpressionOperator](services-business-logic-services.md#expressionoperator), value: string): DataFilter|指定されたオプションに基づいてリスト コントロール用の DataFilter オブジェクトを作成します。<br>  |
| [getFormReference](../interfaces/services-business-logic-services-imetadataservice.md#getformreference) |getFormReference(componentName: string, filterContext: DataFilter, excludeContext: boolean, filterLocalOnly?: boolean): [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md)|ナビゲーション コントロールで使用する特定のページ アクションに対し INavigationArgs オブジェクトを作成します。<br>  |
| [hideNavigation](../interfaces/services-business-logic-services-imetadataservice.md#hidenavigation) |hideNavigation(pageNamesToHide: string [ ]): any|既定のランディング ページから指定されたページを非表示にします。<br>  |


### <a name="pagedata"></a>PageData

#### <a name="hierarchy"></a>階層

PageData <br>

#### <a name="methods"></a>メソッド

| 氏名 | 署名 | 説明 |
| ---- | --------- | ----------- |
| [getControlValue](../interfaces/services-business-logic-services-ipagedata.md#getcontrolvalue) |getControlValue(controlName: string): any|ページでデータ セットから直接読み込まれるコントロールの値を取得します。<br>  |
| [setControlValue](../interfaces/services-business-logic-services-ipagedata.md#setcontrolvalue) |setControlValue(controlName: string, value: any): any|ページでデータ セットに直接読み込まれるコントロールの値を設定します。<br>  |

## <a name="type-aliases"></a>型のエイリアス


### <a name="expressionoperator"></a>ExpressionOperator
ExpressionOperator: 「Is」 &#124; 「IsNot」 &#124; 「Contains」 &#124; 「BeginsWith」 &#124; 「EndsWith」 &#124; 「GreaterThan」 &#124; 「LessThan」 &#124; 「GreaterThanOrEqual」 &#124; 「LessThanOrEqual」


フィルターの定義およびその他の場所で使用される式演算子の使用可能な値を表します

