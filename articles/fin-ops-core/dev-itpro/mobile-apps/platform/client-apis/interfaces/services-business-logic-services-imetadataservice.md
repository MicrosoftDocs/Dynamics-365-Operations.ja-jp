---
title: MetadataService タイプ
description: アプリケーション ワークスペースでさまざまなメタデータ要素にアクセスして構成する機能を提供します。
author: tonyafehr
ms.date: 05/24/2022
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: f6aad7c726b77e14c17dba99cec443558f364d7a
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811340"
---
# <a name="metadataservice-type"></a>MetadataService タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

アプリケーション ワークスペースでさまざまなメタデータ要素にアクセスして構成する機能を提供します。

### <a name="hierarchy"></a>階層

MetadataService <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [バージョン](services-business-logic-services-imetadataservice.md#version)

### <a name="methods"></a>メソッド

* [addControl](services-business-logic-services-imetadataservice.md#addcontrol)
* [compareVersion](services-business-logic-services-imetadataservice.md#compareversion)
* [configureAction](services-business-logic-services-imetadataservice.md#configureaction)
* [configureControl](services-business-logic-services-imetadataservice.md#configurecontrol)
* [configureEntity](services-business-logic-services-imetadataservice.md#configureentity)
* [configureLookup](services-business-logic-services-imetadataservice.md#configurelookup)
* [configurePage](services-business-logic-services-imetadataservice.md#configurepage)
* [configureWorkspace](services-business-logic-services-imetadataservice.md#configureworkspace)
* [findAction](services-business-logic-services-imetadataservice.md#findaction)
* [findControl](services-business-logic-services-imetadataservice.md#findcontrol)
* [findPage](services-business-logic-services-imetadataservice.md#findpage)
* [getFilterExpression](services-business-logic-services-imetadataservice.md#getfilterexpression)
* [getFormReference](services-business-logic-services-imetadataservice.md#getformreference)
* [hideNavigation](services-business-logic-services-imetadataservice.md#hidenavigation)

## <a name="properties"></a>プロパティ

### <a name="version"></a>のバージョン

version: string

(読み取り専用) 現在実行中のプラットフォームのバージョンを取得します。


## <a name="methods"></a>メソッド

### <a name="addcontrol"></a>addControl


addControl(componentName: string, controlName: string, controlType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype), parentContainerName?: string, options?: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| componentName|string||
| controlName|string||
| controlType|[ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype)||
| parentContainerName?|string||
| options?|[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)||

#### <a name="returns-any"></a>any を返します

### <a name="compareversion"></a>compareVersion


compareVersion(versionToCompare: string): 1 &#124; -1

現在のプラットフォームのバージョンと参照バージョンを比較します。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| versionToCompare|string|比較する参照バージョン|

#### <a name="returns-1-124--1"></a>1 &#124; -1 を返す
1 はプラットフォーム バージョンが参照バージョンより古いことを示し、-1 はプラットフォーム バージョンが参照バージョンより新しいか、または同じであることを示す

### <a name="configureaction"></a>configureAction


configureAction(actionName: string, options: [PageMetadata](view-model-ipage-ipagemetadata.md)): any

アクションをコンフィギュレーションすると、そのアクションに固有の特定の動作を指定または上書きできます。
例 :

```javascript
metadataService.configureAction('Edit-Reservation', { properties-to-set });
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| actionName|string|動作が変更されるアクション|
| オプション|[PageMetadata](view-model-ipage-ipagemetadata.md)|アクションに設定するプロパティを含むプロパティ バッグ|

#### <a name="returns-any"></a>any を返します

### <a name="configurecontrol"></a>configureControl


configureControl(componentName: string, controlName: string, options: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any

コントロールをコンフィギュレーションすると、そのコントロールに固有の特定の動作を指定または上書きできます。 使用可能な動作はコントロール タイプで異なることに注意してください。
例 :

```javascript
metadataService.configureControl('All-Customers', 'FMCustomer_RecId', { properties-to-set });
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| componentName|string|コントロールを含むページまたはアクション|
| controlName|string|動作を変更するコントロール|
| オプション|[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)|コントロールに設定するプロパティを含むプロパティ バッグ|

#### <a name="returns-any"></a>any を返します

### <a name="configureentity"></a>configureEntity


configureEntity(entityName: string, options: any): any

エンティティをコンフィギュレーションすると、そのエンティティに固有の特定の動作を指定または上書きできます。
例 :

```javascript
metadataService.configureEntity("FMCustomer", { properties-to-set });
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| entityName|string|エンティティ名|
| オプション|any|エンティティに設定するプロパティを含むプロパティ バッグ|

#### <a name="returns-any"></a>any を返します

### <a name="configurelookup"></a>configureLookup


configureLookup(taskName: string, lookupControlName: string, options: [LookupMetadata](view-model-control-lookup-ilookup-ilookupmetadata.md)): any

アクションのフィールドをルックアップとして動作するようにコンフィギュレーションします。 リスト コントロールを含む既存のページを使用する必要があります。
例 :

```javascript
metadataService.configureLookup('Add-Reservation', 'FMRental_Customer', { lookupPage: 'All-Customers', valueField: 'FMCustomer_RecId', displayField: 'FMCustomer_FullName'});
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| taskName|string|アクション名|
| lookupControlName|string|ルックアップの動作を指定するフィールドのコントロール名|
| オプション|[LookupMetadata](view-model-control-lookup-ilookup-ilookupmetadata.md)|ルックアップ コンフィギュレーション オブジェクト|

#### <a name="returns-any"></a>any を返します

### <a name="configurepage"></a>configurePage


configurePage(pageName: string, options: [PageMetadata](view-model-ipage-ipagemetadata.md)): any

ページをコンフィギュレーションすると、そのページに固有の特定の動作を指定または上書きできます。
例 :

```javascript
metadataService.configurePage('Reservation-details', { properties-to-set });
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| pageName|string|コントロールを含むページ|
| オプション|[PageMetadata](view-model-ipage-ipagemetadata.md)|ページに設定するプロパティを含むプロパティ バッグ|

#### <a name="returns-any"></a>any を返します

### <a name="configureworkspace"></a>configureWorkspace


configureWorkspace(options: [PageMetadata](view-model-ipage-ipagemetadata.md)): any

ワークスペースをコンフィギュレーションすると、そのワークスペースに固有の特定の動作を指定または上書きできます。
例 :

```javascript
metadataService.configureWorkspace({ properties-to-set });
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| オプション|[PageMetadata](view-model-ipage-ipagemetadata.md)|ワークスペースに設定するプロパティを含むプロパティ バッグ|

#### <a name="returns-any"></a>any を返します

### <a name="findaction"></a>findAction


findAction(actionName: string): [PageMetadata](view-model-ipage-ipagemetadata.md)

メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたアクションの現在のメタデータ インスタンスのコピーを取得します。
注記: メタデータはビジネス ロジックによっていつでも変更でき、呼び出された時点でメタデータの状態を反映するため、この API を使用してコピーを取得するタイミングに注意する必要があります。

例 :

```javascript
var newCustomerTaskMetadata = metadataService.findTask("New-customer");
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| actionName|string|アクション名|

#### <a name="returns-pagemetadata"></a>[PageMetadata](view-model-ipage-ipagemetadata.md) を返します



### <a name="findcontrol"></a>findControl


findControl(componentMetadata: any, controlName: string): [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)

メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたコントロールの現在のメタデータ インスタンスのコピーを取得します。
注記: メタデータはビジネス ロジックによっていつでも変更でき、呼び出された時点でメタデータの状態を反映するため、この API を使用してコピーを取得するタイミングに注意する必要があります。

例 :

```javascript
var firstNameControl = metadataService.findControl(newCustomerTaskMetadata, 'FMCustomer_FirstName');
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| componentMetadata|any|ページまたはアクションのメタデータ インスタンス|
| controlName|string|コントロール名|

#### <a name="returns-controlmetadata"></a>[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) を返します



### <a name="findpage"></a>findPage


findPage(pageName: string): [PageMetadata](view-model-ipage-ipagemetadata.md)

メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたページの現在のメタデータ インスタンスのコピーを取得します。
注記: メタデータはビジネス ロジックによっていつでも変更でき、呼び出された時点でメタデータの状態を反映するため、この API を使用してコピーを取得するタイミングに注意する必要があります。

例 :

```javascript
var reservationDetailsMetadata = metadataService.findPage("Reservation-details");
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| pageName|string|ページ名|

#### <a name="returns-pagemetadata"></a>[PageMetadata](view-model-ipage-ipagemetadata.md) を返します



### <a name="getfilterexpression"></a>getFilterExpression


getFilterExpression(pageName: string, listControlName: string, controlName: string, operator: [ExpressionOperator](../modules/services-business-logic-services.md#expressionoperator), value: string): DataFilter

指定されたオプションに基づいてリスト コントロール用の DataFilter オブジェクトを作成します。
例 :
```javascript
var filter = metadataService.getFilterExpression(
 pageNames.AllCustomers, controlNames.CustomerList, controlNames.CustomerFullName, "Is", firstCustomerName),
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| pageName|string||
| listControlName|string||
| controlName|string||
| 演算子|[ExpressionOperator](../modules/services-business-logic-services.md#expressionoperator)||
| 値|string||

#### <a name="returns-datafilter"></a>DataFilter を返します



### <a name="getformreference"></a>getFormReference


getFormReference(componentName: string, filterContext: DataFilter, excludeContext: boolean, filterLocalOnly?: boolean): [NavigationArgs](view-model-ipage-inavigationargs.md)

ナビゲーション コントロールで使用する特定のページ/アクションに対し INavigationArgs オブジェクトを作成します。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| componentName|string|アクション/ページの名前|
| filterContext|DataFilter||
| excludeContext|ブール値||
| filterLocalOnly?|ブール値||

#### <a name="returns-navigationargs"></a>[NavigationArgs](view-model-ipage-inavigationargs.md) を返します



### <a name="hidenavigation"></a>hideNavigation


hideNavigation(pageNamesToHide: string [ ]): any

既定のランディング ページから指定されたページを非表示にします。
例 :

```javascript
metadataService.hideNavigation('Select-a-customer', 'Select-a-vehicle');
```


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| pageNamesToHide|string [ ]|ページ名|

#### <a name="returns-any"></a>any を返します



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
