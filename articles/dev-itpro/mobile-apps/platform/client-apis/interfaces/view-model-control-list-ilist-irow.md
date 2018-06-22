---
title: "行"
description: "行コントロールは、一覧を構成しています。 リストには、任意の数の行のコントロールが含まれています。"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 6a0f05d99857e365ede167a731720d98ff71164b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="row-type"></a>Row タイプ

[!include [banner](../../../../includes/banner.md)]

行コントロールは、一覧を構成しています。 リストには、任意の数の行のコントロールが含まれています。

### <a name="hierarchy"></a>階層

行 <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [fieldList](view-model-control-list-ilist-irow.md#fieldlist)
* [headerField](view-model-control-list-ilist-irow.md#headerfield)
* [非表示](view-model-control-list-ilist-irow.md#hidden)
* [imageFields](view-model-control-list-ilist-irow.md#imagefields)
* [isSelected](view-model-control-list-ilist-irow.md#isselected)
* [品目](view-model-control-list-ilist-irow.md#item)
* [テンプレート](view-model-control-list-ilist-irow.md#template)

### <a name="methods"></a>メソッド

* [getControl](view-model-control-list-ilist-irow.md#getcontrol)
* [getControlById](view-model-control-list-ilist-irow.md#getcontrolbyid)
* [getControlValueById](view-model-control-list-ilist-irow.md#getcontrolvaluebyid)
* [getRowHeader](view-model-control-list-ilist-irow.md#getrowheader)
* [getRowId](view-model-control-list-ilist-irow.md#getrowid)
* [hasImageField](view-model-control-list-ilist-irow.md#hasimagefield)
* [isEntityCreatedNew](view-model-control-list-ilist-irow.md#isentitycreatednew)
* [isEntityDeleted](view-model-control-list-ilist-irow.md#isentitydeleted)
* [isEntityModified](view-model-control-list-ilist-irow.md#isentitymodified)
* [isEntitySyncPending](view-model-control-list-ilist-irow.md#isentitysyncpending)
* [選択](view-model-control-list-ilist-irow.md#select)

## <a name="properties"></a>プロパティ

### <a name="fieldlist"></a>fieldList

fieldList: [Control](view-model-control-basecontrol-icontrol-icontrol.md) [ ]




### <a name="headerfield"></a>headerField

headerField: [Control](view-model-control-basecontrol-icontrol-icontrol.md)




### <a name="hidden"></a>hidden

hidden: boolean

True の場合、行が表示されません。


### <a name="imagefields"></a>imageFields

imageFields: [Control](view-model-control-basecontrol-icontrol-icontrol.md) [ ]




### <a name="isselected"></a>isSelected

isSelected: boolean




### <a name="item"></a>項目

item: any

表示されるデータのコンテナーです。


### <a name="template"></a>テンプレート

template: [Group](view-model-control-group-igroup-igroup.md)

行のテンプレートを表すグループ コントロール。


## <a name="methods"></a>メソッド

### <a name="getcontrol"></a>getControl


getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| controlName|string||

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します

### <a name="getcontrolbyid"></a>getControlById


getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| id|string|id は valueKey か、またはリスト コントロール メタデータの displayKey になります|

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します

### <a name="getcontrolvaluebyid"></a>getControlValueById


getControlValueById(id: string): string




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| id|string|id は valueKey か、またはリスト コントロール メタデータの displayKey になります|

#### <a name="returns-string"></a>文字列を返します

### <a name="getrowheader"></a>getRowHeader


getRowHeader(): [Control](view-model-control-basecontrol-icontrol-icontrol.md)



#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a>[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します

### <a name="getrowid"></a>getRowId


getRowId(): string



#### <a name="returns-string"></a>文字列を返します

### <a name="hasimagefield"></a>hasImageField


hasImageField(): boolean

行に画像フィールドが含まれている場合は、true を返します。

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="isentitycreatednew"></a>isEntityCreatedNew


isEntityCreatedNew(): boolean



#### <a name="returns-boolean"></a>ブール値を返します

### <a name="isentitydeleted"></a>isEntityDeleted


isEntityDeleted(): boolean



#### <a name="returns-boolean"></a>ブール値を返します

### <a name="isentitymodified"></a>isEntityModified


isEntityModified(): boolean



#### <a name="returns-boolean"></a>ブール値を返します

### <a name="isentitysyncpending"></a>isEntitySyncPending


isEntitySyncPending(): boolean



#### <a name="returns-boolean"></a>ブール値を返します

### <a name="select"></a>select


select(): any



#### <a name="returns-any"></a>any を返します

