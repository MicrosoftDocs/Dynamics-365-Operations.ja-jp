---
title: MetadataService タイプ
description: アプリケーション ワークスペースでさまざまなメタデータ要素にアクセスして構成する機能を提供します。
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
ms.openlocfilehash: 7b9a2318b1d2b873c6eb8f4cc0924e581b83ec00
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537156"
---
# <a name="metadataservice-type"></a><span data-ttu-id="0083c-103">MetadataService タイプ</span><span class="sxs-lookup"><span data-stu-id="0083c-103">MetadataService type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="0083c-104">アプリケーション ワークスペースでさまざまなメタデータ要素にアクセスして構成する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="0083c-104">Provides ability to access and configure various metadata elements under the application workspace.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="0083c-105">階層</span><span class="sxs-lookup"><span data-stu-id="0083c-105">Hierarchy</span></span>

<span data-ttu-id="0083c-106">MetadataService</span><span class="sxs-lookup"><span data-stu-id="0083c-106">MetadataService</span></span> <br>

## <a name="index"></a><span data-ttu-id="0083c-107">指数</span><span class="sxs-lookup"><span data-stu-id="0083c-107">Index</span></span>

### <a name="properties"></a><span data-ttu-id="0083c-108">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0083c-108">Properties</span></span>

* [<span data-ttu-id="0083c-109">バージョン</span><span class="sxs-lookup"><span data-stu-id="0083c-109">version</span></span>](services-business-logic-services-imetadataservice.md#version)

### <a name="methods"></a><span data-ttu-id="0083c-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="0083c-110">Methods</span></span>

* [<span data-ttu-id="0083c-111">addControl</span><span class="sxs-lookup"><span data-stu-id="0083c-111">addControl</span></span>](services-business-logic-services-imetadataservice.md#addcontrol)
* [<span data-ttu-id="0083c-112">compareVersion</span><span class="sxs-lookup"><span data-stu-id="0083c-112">compareVersion</span></span>](services-business-logic-services-imetadataservice.md#compareversion)
* [<span data-ttu-id="0083c-113">configureAction</span><span class="sxs-lookup"><span data-stu-id="0083c-113">configureAction</span></span>](services-business-logic-services-imetadataservice.md#configureaction)
* [<span data-ttu-id="0083c-114">configureControl</span><span class="sxs-lookup"><span data-stu-id="0083c-114">configureControl</span></span>](services-business-logic-services-imetadataservice.md#configurecontrol)
* [<span data-ttu-id="0083c-115">configureEntity</span><span class="sxs-lookup"><span data-stu-id="0083c-115">configureEntity</span></span>](services-business-logic-services-imetadataservice.md#configureentity)
* [<span data-ttu-id="0083c-116">configureLookup</span><span class="sxs-lookup"><span data-stu-id="0083c-116">configureLookup</span></span>](services-business-logic-services-imetadataservice.md#configurelookup)
* [<span data-ttu-id="0083c-117">configurePage</span><span class="sxs-lookup"><span data-stu-id="0083c-117">configurePage</span></span>](services-business-logic-services-imetadataservice.md#configurepage)
* [<span data-ttu-id="0083c-118">configureWorkspace</span><span class="sxs-lookup"><span data-stu-id="0083c-118">configureWorkspace</span></span>](services-business-logic-services-imetadataservice.md#configureworkspace)
* [<span data-ttu-id="0083c-119">findAction</span><span class="sxs-lookup"><span data-stu-id="0083c-119">findAction</span></span>](services-business-logic-services-imetadataservice.md#findaction)
* [<span data-ttu-id="0083c-120">findControl</span><span class="sxs-lookup"><span data-stu-id="0083c-120">findControl</span></span>](services-business-logic-services-imetadataservice.md#findcontrol)
* [<span data-ttu-id="0083c-121">findPage</span><span class="sxs-lookup"><span data-stu-id="0083c-121">findPage</span></span>](services-business-logic-services-imetadataservice.md#findpage)
* [<span data-ttu-id="0083c-122">getFilterExpression</span><span class="sxs-lookup"><span data-stu-id="0083c-122">getFilterExpression</span></span>](services-business-logic-services-imetadataservice.md#getfilterexpression)
* [<span data-ttu-id="0083c-123">getFormReference</span><span class="sxs-lookup"><span data-stu-id="0083c-123">getFormReference</span></span>](services-business-logic-services-imetadataservice.md#getformreference)
* [<span data-ttu-id="0083c-124">hideNavigation</span><span class="sxs-lookup"><span data-stu-id="0083c-124">hideNavigation</span></span>](services-business-logic-services-imetadataservice.md#hidenavigation)

## <a name="properties"></a><span data-ttu-id="0083c-125">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0083c-125">Properties</span></span>

### <a name="version"></a><span data-ttu-id="0083c-126">のバージョン</span><span class="sxs-lookup"><span data-stu-id="0083c-126">version</span></span>

<span data-ttu-id="0083c-127">version: string</span><span class="sxs-lookup"><span data-stu-id="0083c-127">version: string</span></span>

<span data-ttu-id="0083c-128">(読み取り専用) 現在実行中のプラットフォームのバージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="0083c-128">(Read-only) Gets the version of the platform currently running.</span></span>


## <a name="methods"></a><span data-ttu-id="0083c-129">メソッド</span><span class="sxs-lookup"><span data-stu-id="0083c-129">Methods</span></span>

### <a name="addcontrol"></a><span data-ttu-id="0083c-130">addControl</span><span class="sxs-lookup"><span data-stu-id="0083c-130">addControl</span></span>


<span data-ttu-id="0083c-131">addControl(componentName: string, controlName: string, controlType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype), parentContainerName?: string, options?: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="0083c-131">addControl(componentName: string, controlName: string, controlType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype), parentContainerName?: string, options?: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any</span></span>




#### <a name="parameters"></a><span data-ttu-id="0083c-132">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-132">Parameters</span></span>

| <span data-ttu-id="0083c-133">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-133">Name</span></span> | <span data-ttu-id="0083c-134">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-134">Type</span></span> | <span data-ttu-id="0083c-135">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-135">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-136">componentName</span><span class="sxs-lookup"><span data-stu-id="0083c-136">componentName</span></span>|<span data-ttu-id="0083c-137">string</span><span class="sxs-lookup"><span data-stu-id="0083c-137">string</span></span>||
| <span data-ttu-id="0083c-138">controlName</span><span class="sxs-lookup"><span data-stu-id="0083c-138">controlName</span></span>|<span data-ttu-id="0083c-139">string</span><span class="sxs-lookup"><span data-stu-id="0083c-139">string</span></span>||
| <span data-ttu-id="0083c-140">controlType</span><span class="sxs-lookup"><span data-stu-id="0083c-140">controlType</span></span>|[<span data-ttu-id="0083c-141">ControlType</span><span class="sxs-lookup"><span data-stu-id="0083c-141">ControlType</span></span>](../modules/view-model-control-basecontrol-icontrol.md#controltype)||
| <span data-ttu-id="0083c-142">parentContainerName?</span><span class="sxs-lookup"><span data-stu-id="0083c-142">parentContainerName?</span></span>|<span data-ttu-id="0083c-143">string</span><span class="sxs-lookup"><span data-stu-id="0083c-143">string</span></span>||
| <span data-ttu-id="0083c-144">options?</span><span class="sxs-lookup"><span data-stu-id="0083c-144">options?</span></span>|[<span data-ttu-id="0083c-145">ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="0083c-145">ControlMetadata</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md)||

#### <a name="returns-any"></a><span data-ttu-id="0083c-146">any を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-146">Returns any</span></span>

### <a name="compareversion"></a><span data-ttu-id="0083c-147">compareVersion</span><span class="sxs-lookup"><span data-stu-id="0083c-147">compareVersion</span></span>


<span data-ttu-id="0083c-148">compareVersion(versionToCompare: string): 1 &#124; -1</span><span class="sxs-lookup"><span data-stu-id="0083c-148">compareVersion(versionToCompare: string): 1 &#124; -1</span></span>

<span data-ttu-id="0083c-149">現在のプラットフォームのバージョンと参照バージョンを比較します。</span><span class="sxs-lookup"><span data-stu-id="0083c-149">Compares the current platform version with a reference version.</span></span>


#### <a name="parameters"></a><span data-ttu-id="0083c-150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-150">Parameters</span></span>

| <span data-ttu-id="0083c-151">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-151">Name</span></span> | <span data-ttu-id="0083c-152">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-152">Type</span></span> | <span data-ttu-id="0083c-153">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-153">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-154">versionToCompare</span><span class="sxs-lookup"><span data-stu-id="0083c-154">versionToCompare</span></span>|<span data-ttu-id="0083c-155">string</span><span class="sxs-lookup"><span data-stu-id="0083c-155">string</span></span>|<span data-ttu-id="0083c-156">比較する参照バージョン</span><span class="sxs-lookup"><span data-stu-id="0083c-156">The reference version to compare with</span></span>|

#### <a name="returns-1-124--1"></a><span data-ttu-id="0083c-157">1 &#124; -1 を返す</span><span class="sxs-lookup"><span data-stu-id="0083c-157">Returns 1 &#124; -1</span></span>
<span data-ttu-id="0083c-158">1 はプラットフォーム バージョンが参照バージョンより古いことを示し、-1 はプラットフォーム バージョンが参照バージョンより新しいか、または同じであることを示す</span><span class="sxs-lookup"><span data-stu-id="0083c-158">1 to indicate the platform version is older than the reference version, -1 to indicate that the platform version is newer or same as the reference version</span></span>

### <a name="configureaction"></a><span data-ttu-id="0083c-159">configureAction</span><span class="sxs-lookup"><span data-stu-id="0083c-159">configureAction</span></span>


<span data-ttu-id="0083c-160">configureAction(actionName: string, options: [PageMetadata](view-model-ipage-ipagemetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="0083c-160">configureAction(actionName: string, options: [PageMetadata](view-model-ipage-ipagemetadata.md)): any</span></span>

<span data-ttu-id="0083c-161">アクションをコンフィギュレーションすると、そのアクションに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="0083c-161">Configuring an action allows specifying or overriding certain behaviors specific to actions.</span></span>
<span data-ttu-id="0083c-162">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-162">Example:</span></span>

```javascript
metadataService.configureAction('Edit-Reservation', { properties-to-set });
```


#### <a name="parameters"></a><span data-ttu-id="0083c-163">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-163">Parameters</span></span>

| <span data-ttu-id="0083c-164">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-164">Name</span></span> | <span data-ttu-id="0083c-165">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-165">Type</span></span> | <span data-ttu-id="0083c-166">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-166">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-167">actionName</span><span class="sxs-lookup"><span data-stu-id="0083c-167">actionName</span></span>|<span data-ttu-id="0083c-168">string</span><span class="sxs-lookup"><span data-stu-id="0083c-168">string</span></span>|<span data-ttu-id="0083c-169">動作が変更されるアクション</span><span class="sxs-lookup"><span data-stu-id="0083c-169">The action whose behavior is to be changed</span></span>|
| <span data-ttu-id="0083c-170">オプション</span><span class="sxs-lookup"><span data-stu-id="0083c-170">options</span></span>|[<span data-ttu-id="0083c-171">PageMetadata</span><span class="sxs-lookup"><span data-stu-id="0083c-171">PageMetadata</span></span>](view-model-ipage-ipagemetadata.md)|<span data-ttu-id="0083c-172">アクションに設定するプロパティを含むプロパティ バッグ</span><span class="sxs-lookup"><span data-stu-id="0083c-172">The property bag containing the properties to set on the action</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="0083c-173">any を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-173">Returns any</span></span>

### <a name="configurecontrol"></a><span data-ttu-id="0083c-174">configureControl</span><span class="sxs-lookup"><span data-stu-id="0083c-174">configureControl</span></span>


<span data-ttu-id="0083c-175">configureControl(componentName: string, controlName: string, options: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="0083c-175">configureControl(componentName: string, controlName: string, options: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any</span></span>

<span data-ttu-id="0083c-176">コントロールをコンフィギュレーションすると、そのコントロールに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="0083c-176">Configuring a control allows specifying or overriding certain behaviors specific to the control.</span></span> <span data-ttu-id="0083c-177">使用可能な動作はコントロール タイプで異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0083c-177">Note that the available behaviors vary by control type.</span></span>
<span data-ttu-id="0083c-178">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-178">Example:</span></span>

```javascript
metadataService.configureControl('All-Customers', 'FMCustomer_RecId', { properties-to-set });
```


#### <a name="parameters"></a><span data-ttu-id="0083c-179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-179">Parameters</span></span>

| <span data-ttu-id="0083c-180">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-180">Name</span></span> | <span data-ttu-id="0083c-181">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-181">Type</span></span> | <span data-ttu-id="0083c-182">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-182">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-183">componentName</span><span class="sxs-lookup"><span data-stu-id="0083c-183">componentName</span></span>|<span data-ttu-id="0083c-184">string</span><span class="sxs-lookup"><span data-stu-id="0083c-184">string</span></span>|<span data-ttu-id="0083c-185">コントロールを含むページまたはアクション</span><span class="sxs-lookup"><span data-stu-id="0083c-185">A page or action that contains the control</span></span>|
| <span data-ttu-id="0083c-186">controlName</span><span class="sxs-lookup"><span data-stu-id="0083c-186">controlName</span></span>|<span data-ttu-id="0083c-187">string</span><span class="sxs-lookup"><span data-stu-id="0083c-187">string</span></span>|<span data-ttu-id="0083c-188">動作を変更するコントロール</span><span class="sxs-lookup"><span data-stu-id="0083c-188">The control whose behavior is to be changed</span></span>|
| <span data-ttu-id="0083c-189">オプション</span><span class="sxs-lookup"><span data-stu-id="0083c-189">options</span></span>|[<span data-ttu-id="0083c-190">ControlMetadata</span><span class="sxs-lookup"><span data-stu-id="0083c-190">ControlMetadata</span></span>](view-model-control-basecontrol-icontrol-icontrolmetadata.md)|<span data-ttu-id="0083c-191">コントロールに設定するプロパティを含むプロパティ バッグ</span><span class="sxs-lookup"><span data-stu-id="0083c-191">The property bag containing the properties to set on the control</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="0083c-192">any を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-192">Returns any</span></span>

### <a name="configureentity"></a><span data-ttu-id="0083c-193">configureEntity</span><span class="sxs-lookup"><span data-stu-id="0083c-193">configureEntity</span></span>


<span data-ttu-id="0083c-194">configureEntity(entityName: string, options: any): any</span><span class="sxs-lookup"><span data-stu-id="0083c-194">configureEntity(entityName: string, options: any): any</span></span>

<span data-ttu-id="0083c-195">エンティティをコンフィギュレーションすると、そのエンティティに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="0083c-195">Configuring an entity allows specifying or overriding certain behaviors specific to the entity.</span></span>
<span data-ttu-id="0083c-196">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-196">Example:</span></span>

```javascript
metadataService.configureEntity("FMCustomer", { properties-to-set });
```


#### <a name="parameters"></a><span data-ttu-id="0083c-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-197">Parameters</span></span>

| <span data-ttu-id="0083c-198">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-198">Name</span></span> | <span data-ttu-id="0083c-199">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-199">Type</span></span> | <span data-ttu-id="0083c-200">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-200">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-201">entityName</span><span class="sxs-lookup"><span data-stu-id="0083c-201">entityName</span></span>|<span data-ttu-id="0083c-202">string</span><span class="sxs-lookup"><span data-stu-id="0083c-202">string</span></span>|<span data-ttu-id="0083c-203">エンティティ名</span><span class="sxs-lookup"><span data-stu-id="0083c-203">An entity name</span></span>|
| <span data-ttu-id="0083c-204">オプション</span><span class="sxs-lookup"><span data-stu-id="0083c-204">options</span></span>|<span data-ttu-id="0083c-205">any</span><span class="sxs-lookup"><span data-stu-id="0083c-205">any</span></span>|<span data-ttu-id="0083c-206">エンティティに設定するプロパティを含むプロパティ バッグ</span><span class="sxs-lookup"><span data-stu-id="0083c-206">The property bag containing the properties to set on the entity</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="0083c-207">any を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-207">Returns any</span></span>

### <a name="configurelookup"></a><span data-ttu-id="0083c-208">configureLookup</span><span class="sxs-lookup"><span data-stu-id="0083c-208">configureLookup</span></span>


<span data-ttu-id="0083c-209">configureLookup(taskName: string, lookupControlName: string, options: [LookupMetadata](view-model-control-lookup-ilookup-ilookupmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="0083c-209">configureLookup(taskName: string, lookupControlName: string, options: [LookupMetadata](view-model-control-lookup-ilookup-ilookupmetadata.md)): any</span></span>

<span data-ttu-id="0083c-210">アクションのフィールドをルックアップとして動作するようにコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="0083c-210">Configures a field on an action to behave as a lookup.</span></span> <span data-ttu-id="0083c-211">リスト コントロールを含む既存のページを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0083c-211">Requires using an existing page which contains a list control.</span></span>
<span data-ttu-id="0083c-212">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-212">Example:</span></span>

```javascript
metadataService.configureLookup('Add-Reservation', 'FMRental_Customer', { lookupPage: 'All-Customers', valueField: 'FMCustomer_RecId', displayField: 'FMCustomer_FullName'});
```


#### <a name="parameters"></a><span data-ttu-id="0083c-213">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-213">Parameters</span></span>

| <span data-ttu-id="0083c-214">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-214">Name</span></span> | <span data-ttu-id="0083c-215">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-215">Type</span></span> | <span data-ttu-id="0083c-216">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-216">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-217">taskName</span><span class="sxs-lookup"><span data-stu-id="0083c-217">taskName</span></span>|<span data-ttu-id="0083c-218">string</span><span class="sxs-lookup"><span data-stu-id="0083c-218">string</span></span>|<span data-ttu-id="0083c-219">アクション名</span><span class="sxs-lookup"><span data-stu-id="0083c-219">Action name</span></span>|
| <span data-ttu-id="0083c-220">lookupControlName</span><span class="sxs-lookup"><span data-stu-id="0083c-220">lookupControlName</span></span>|<span data-ttu-id="0083c-221">string</span><span class="sxs-lookup"><span data-stu-id="0083c-221">string</span></span>|<span data-ttu-id="0083c-222">ルックアップの動作を指定するフィールドのコントロール名</span><span class="sxs-lookup"><span data-stu-id="0083c-222">The control name of the field to be given lookup behavior</span></span>|
| <span data-ttu-id="0083c-223">オプション</span><span class="sxs-lookup"><span data-stu-id="0083c-223">options</span></span>|[<span data-ttu-id="0083c-224">LookupMetadata</span><span class="sxs-lookup"><span data-stu-id="0083c-224">LookupMetadata</span></span>](view-model-control-lookup-ilookup-ilookupmetadata.md)|<span data-ttu-id="0083c-225">ルックアップ コンフィギュレーション オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0083c-225">Lookup configuration object</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="0083c-226">any を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-226">Returns any</span></span>

### <a name="configurepage"></a><span data-ttu-id="0083c-227">configurePage</span><span class="sxs-lookup"><span data-stu-id="0083c-227">configurePage</span></span>


<span data-ttu-id="0083c-228">configurePage(pageName: string, options: [PageMetadata](view-model-ipage-ipagemetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="0083c-228">configurePage(pageName: string, options: [PageMetadata](view-model-ipage-ipagemetadata.md)): any</span></span>

<span data-ttu-id="0083c-229">ページをコンフィギュレーションすると、そのページに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="0083c-229">Configuring a Page allows specifying or overriding certain behaviors specific to the Page.</span></span>
<span data-ttu-id="0083c-230">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-230">Example:</span></span>

```javascript
metadataService.configurePage('Reservation-details', { properties-to-set });
```


#### <a name="parameters"></a><span data-ttu-id="0083c-231">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-231">Parameters</span></span>

| <span data-ttu-id="0083c-232">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-232">Name</span></span> | <span data-ttu-id="0083c-233">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-233">Type</span></span> | <span data-ttu-id="0083c-234">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-234">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-235">pageName</span><span class="sxs-lookup"><span data-stu-id="0083c-235">pageName</span></span>|<span data-ttu-id="0083c-236">string</span><span class="sxs-lookup"><span data-stu-id="0083c-236">string</span></span>|<span data-ttu-id="0083c-237">コントロールを含むページ</span><span class="sxs-lookup"><span data-stu-id="0083c-237">The page that contains the control</span></span>|
| <span data-ttu-id="0083c-238">オプション</span><span class="sxs-lookup"><span data-stu-id="0083c-238">options</span></span>|[<span data-ttu-id="0083c-239">PageMetadata</span><span class="sxs-lookup"><span data-stu-id="0083c-239">PageMetadata</span></span>](view-model-ipage-ipagemetadata.md)|<span data-ttu-id="0083c-240">ページに設定するプロパティを含むプロパティ バッグ</span><span class="sxs-lookup"><span data-stu-id="0083c-240">The property bag containing the properties to set on the page</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="0083c-241">any を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-241">Returns any</span></span>

### <a name="configureworkspace"></a><span data-ttu-id="0083c-242">configureWorkspace</span><span class="sxs-lookup"><span data-stu-id="0083c-242">configureWorkspace</span></span>


<span data-ttu-id="0083c-243">configureWorkspace(options: [PageMetadata](view-model-ipage-ipagemetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="0083c-243">configureWorkspace(options: [PageMetadata](view-model-ipage-ipagemetadata.md)): any</span></span>

<span data-ttu-id="0083c-244">ワークスペースをコンフィギュレーションすると、そのワークスペースに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="0083c-244">Configuring a workspace allows specifying or overriding certain behaviors specific to the workspace.</span></span>
<span data-ttu-id="0083c-245">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-245">Example:</span></span>

```javascript
metadataService.configureWorkspace({ properties-to-set });
```


#### <a name="parameters"></a><span data-ttu-id="0083c-246">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-246">Parameters</span></span>

| <span data-ttu-id="0083c-247">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-247">Name</span></span> | <span data-ttu-id="0083c-248">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-248">Type</span></span> | <span data-ttu-id="0083c-249">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-249">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-250">オプション</span><span class="sxs-lookup"><span data-stu-id="0083c-250">options</span></span>|[<span data-ttu-id="0083c-251">PageMetadata</span><span class="sxs-lookup"><span data-stu-id="0083c-251">PageMetadata</span></span>](view-model-ipage-ipagemetadata.md)|<span data-ttu-id="0083c-252">ワークスペースに設定するプロパティを含むプロパティ バッグ</span><span class="sxs-lookup"><span data-stu-id="0083c-252">The property bag containing the properties to set on the workspace</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="0083c-253">any を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-253">Returns any</span></span>

### <a name="findaction"></a><span data-ttu-id="0083c-254">findAction</span><span class="sxs-lookup"><span data-stu-id="0083c-254">findAction</span></span>


<span data-ttu-id="0083c-255">findAction(actionName: string): [PageMetadata](view-model-ipage-ipagemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="0083c-255">findAction(actionName: string): [PageMetadata](view-model-ipage-ipagemetadata.md)</span></span>

<span data-ttu-id="0083c-256">メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたアクションの現在のメタデータ インスタンスのコピーを取得します。</span><span class="sxs-lookup"><span data-stu-id="0083c-256">Gets a copy of the current metadata instance of a specified Action, for the purpose of inspecting the metadata (not to be used for changing the metadata).</span></span>
<span data-ttu-id="0083c-257">注記: メタデータはビジネス ロジックによっていつでも変更でき、呼び出された時点でメタデータの状態を反映するため、この API を使用してコピーを取得するタイミングに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0083c-257">Note: Since metadata can be changed at any time by business logic, you must be mindful of when you use this API to get a copy as it will reflect the state of the metadata at the time the call is made.</span></span>

<span data-ttu-id="0083c-258">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-258">Example:</span></span>

```javascript
var newCustomerTaskMetadata = metadataService.findTask("New-customer");
```


#### <a name="parameters"></a><span data-ttu-id="0083c-259">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-259">Parameters</span></span>

| <span data-ttu-id="0083c-260">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-260">Name</span></span> | <span data-ttu-id="0083c-261">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-261">Type</span></span> | <span data-ttu-id="0083c-262">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-262">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-263">actionName</span><span class="sxs-lookup"><span data-stu-id="0083c-263">actionName</span></span>|<span data-ttu-id="0083c-264">string</span><span class="sxs-lookup"><span data-stu-id="0083c-264">string</span></span>|<span data-ttu-id="0083c-265">アクション名</span><span class="sxs-lookup"><span data-stu-id="0083c-265">An action name</span></span>|

#### <a name="returns-pagemetadataview-model-ipage-ipagemetadatamd"></a><span data-ttu-id="0083c-266">[PageMetadata](view-model-ipage-ipagemetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-266">Returns [PageMetadata](view-model-ipage-ipagemetadata.md)</span></span>



### <a name="findcontrol"></a><span data-ttu-id="0083c-267">findControl</span><span class="sxs-lookup"><span data-stu-id="0083c-267">findControl</span></span>


<span data-ttu-id="0083c-268">findControl(componentMetadata: any, controlName: string): [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="0083c-268">findControl(componentMetadata: any, controlName: string): [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)</span></span>

<span data-ttu-id="0083c-269">メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたコントロールの現在のメタデータ インスタンスのコピーを取得します。</span><span class="sxs-lookup"><span data-stu-id="0083c-269">Gets a copy of the current metadata instance of a specified control, for the purpose of inspecting the metadata (not to be used for changing the metadata).</span></span>
<span data-ttu-id="0083c-270">注記: メタデータはビジネス ロジックによっていつでも変更でき、呼び出された時点でメタデータの状態を反映するため、この API を使用してコピーを取得するタイミングに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0083c-270">Note: Since metadata can be changed at any time by business logic, you must be mindful of when you use this API to get a copy as it will reflect the state of the metadata at the time the call is made.</span></span>

<span data-ttu-id="0083c-271">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-271">Example:</span></span>

```javascript
var firstNameControl = metadataService.findControl(newCustomerTaskMetadata, 'FMCustomer_FirstName');
```


#### <a name="parameters"></a><span data-ttu-id="0083c-272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-272">Parameters</span></span>

| <span data-ttu-id="0083c-273">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-273">Name</span></span> | <span data-ttu-id="0083c-274">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-274">Type</span></span> | <span data-ttu-id="0083c-275">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-275">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-276">componentMetadata</span><span class="sxs-lookup"><span data-stu-id="0083c-276">componentMetadata</span></span>|<span data-ttu-id="0083c-277">any</span><span class="sxs-lookup"><span data-stu-id="0083c-277">any</span></span>|<span data-ttu-id="0083c-278">ページまたはアクションのメタデータ インスタンス</span><span class="sxs-lookup"><span data-stu-id="0083c-278">A metadata instance of the page or action</span></span>|
| <span data-ttu-id="0083c-279">controlName</span><span class="sxs-lookup"><span data-stu-id="0083c-279">controlName</span></span>|<span data-ttu-id="0083c-280">string</span><span class="sxs-lookup"><span data-stu-id="0083c-280">string</span></span>|<span data-ttu-id="0083c-281">コントロール名</span><span class="sxs-lookup"><span data-stu-id="0083c-281">A control name</span></span>|

#### <a name="returns-controlmetadataview-model-control-basecontrol-icontrol-icontrolmetadatamd"></a><span data-ttu-id="0083c-282">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-282">Returns [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md)</span></span>



### <a name="findpage"></a><span data-ttu-id="0083c-283">findPage</span><span class="sxs-lookup"><span data-stu-id="0083c-283">findPage</span></span>


<span data-ttu-id="0083c-284">findPage(pageName: string): [PageMetadata](view-model-ipage-ipagemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="0083c-284">findPage(pageName: string): [PageMetadata](view-model-ipage-ipagemetadata.md)</span></span>

<span data-ttu-id="0083c-285">メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたページの現在のメタデータ インスタンスのコピーを取得します。</span><span class="sxs-lookup"><span data-stu-id="0083c-285">Gets a copy of the current metadata instance of a specified page, for the purpose of inspecting the metadata (not to be used for changing the metadata).</span></span>
<span data-ttu-id="0083c-286">注記: メタデータはビジネス ロジックによっていつでも変更でき、呼び出された時点でメタデータの状態を反映するため、この API を使用してコピーを取得するタイミングに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0083c-286">Note: Since metadata can be changed at any time by business logic, you must be mindful of when you use this API to get a copy as it will reflect the state of the metadata at the time the call is made.</span></span>

<span data-ttu-id="0083c-287">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-287">Example:</span></span>

```javascript
var reservationDetailsMetadata = metadataService.findPage("Reservation-details");
```


#### <a name="parameters"></a><span data-ttu-id="0083c-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-288">Parameters</span></span>

| <span data-ttu-id="0083c-289">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-289">Name</span></span> | <span data-ttu-id="0083c-290">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-290">Type</span></span> | <span data-ttu-id="0083c-291">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-291">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-292">pageName</span><span class="sxs-lookup"><span data-stu-id="0083c-292">pageName</span></span>|<span data-ttu-id="0083c-293">string</span><span class="sxs-lookup"><span data-stu-id="0083c-293">string</span></span>|<span data-ttu-id="0083c-294">ページ名</span><span class="sxs-lookup"><span data-stu-id="0083c-294">A page name</span></span>|

#### <a name="returns-pagemetadataview-model-ipage-ipagemetadatamd"></a><span data-ttu-id="0083c-295">[PageMetadata](view-model-ipage-ipagemetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-295">Returns [PageMetadata](view-model-ipage-ipagemetadata.md)</span></span>



### <a name="getfilterexpression"></a><span data-ttu-id="0083c-296">getFilterExpression</span><span class="sxs-lookup"><span data-stu-id="0083c-296">getFilterExpression</span></span>


<span data-ttu-id="0083c-297">getFilterExpression(pageName: string, listControlName: string, controlName: string, operator: [ExpressionOperator](../modules/services-business-logic-services.md#expressionoperator), value: string): DataFilter</span><span class="sxs-lookup"><span data-stu-id="0083c-297">getFilterExpression(pageName: string, listControlName: string, controlName: string, operator: [ExpressionOperator](../modules/services-business-logic-services.md#expressionoperator), value: string): DataFilter</span></span>

<span data-ttu-id="0083c-298">指定されたオプションに基づいてリスト コントロール用の DataFilter オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0083c-298">Create a DataFilter object for a list control based on the provided options.</span></span>
<span data-ttu-id="0083c-299">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-299">Example:</span></span>
```javascript
var filter = metadataService.getFilterExpression(
 pageNames.AllCustomers, controlNames.CustomerList, controlNames.CustomerFullName, "Is", firstCustomerName),
```


#### <a name="parameters"></a><span data-ttu-id="0083c-300">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-300">Parameters</span></span>

| <span data-ttu-id="0083c-301">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-301">Name</span></span> | <span data-ttu-id="0083c-302">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-302">Type</span></span> | <span data-ttu-id="0083c-303">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-303">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-304">pageName</span><span class="sxs-lookup"><span data-stu-id="0083c-304">pageName</span></span>|<span data-ttu-id="0083c-305">string</span><span class="sxs-lookup"><span data-stu-id="0083c-305">string</span></span>||
| <span data-ttu-id="0083c-306">listControlName</span><span class="sxs-lookup"><span data-stu-id="0083c-306">listControlName</span></span>|<span data-ttu-id="0083c-307">string</span><span class="sxs-lookup"><span data-stu-id="0083c-307">string</span></span>||
| <span data-ttu-id="0083c-308">controlName</span><span class="sxs-lookup"><span data-stu-id="0083c-308">controlName</span></span>|<span data-ttu-id="0083c-309">string</span><span class="sxs-lookup"><span data-stu-id="0083c-309">string</span></span>||
| <span data-ttu-id="0083c-310">演算子</span><span class="sxs-lookup"><span data-stu-id="0083c-310">operator</span></span>|[<span data-ttu-id="0083c-311">ExpressionOperator</span><span class="sxs-lookup"><span data-stu-id="0083c-311">ExpressionOperator</span></span>](../modules/services-business-logic-services.md#expressionoperator)||
| <span data-ttu-id="0083c-312">値</span><span class="sxs-lookup"><span data-stu-id="0083c-312">value</span></span>|<span data-ttu-id="0083c-313">string</span><span class="sxs-lookup"><span data-stu-id="0083c-313">string</span></span>||

#### <a name="returns-datafilter"></a><span data-ttu-id="0083c-314">DataFilter を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-314">Returns DataFilter</span></span>



### <a name="getformreference"></a><span data-ttu-id="0083c-315">getFormReference</span><span class="sxs-lookup"><span data-stu-id="0083c-315">getFormReference</span></span>


<span data-ttu-id="0083c-316">getFormReference(componentName: string, filterContext: DataFilter, excludeContext: boolean, filterLocalOnly?: boolean): [NavigationArgs](view-model-ipage-inavigationargs.md)</span><span class="sxs-lookup"><span data-stu-id="0083c-316">getFormReference(componentName: string, filterContext: DataFilter, excludeContext: boolean, filterLocalOnly?: boolean): [NavigationArgs](view-model-ipage-inavigationargs.md)</span></span>

<span data-ttu-id="0083c-317">ナビゲーション コントロールで使用する特定のページ/アクションに対し INavigationArgs オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0083c-317">Create an INavigationArgs object for a specific page/action to be used with a navigation control.</span></span>


#### <a name="parameters"></a><span data-ttu-id="0083c-318">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-318">Parameters</span></span>

| <span data-ttu-id="0083c-319">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-319">Name</span></span> | <span data-ttu-id="0083c-320">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-320">Type</span></span> | <span data-ttu-id="0083c-321">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-321">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-322">componentName</span><span class="sxs-lookup"><span data-stu-id="0083c-322">componentName</span></span>|<span data-ttu-id="0083c-323">string</span><span class="sxs-lookup"><span data-stu-id="0083c-323">string</span></span>|<span data-ttu-id="0083c-324">アクション/ページの名前</span><span class="sxs-lookup"><span data-stu-id="0083c-324">Name of the action/page</span></span>|
| <span data-ttu-id="0083c-325">filterContext</span><span class="sxs-lookup"><span data-stu-id="0083c-325">filterContext</span></span>|<span data-ttu-id="0083c-326">DataFilter</span><span class="sxs-lookup"><span data-stu-id="0083c-326">DataFilter</span></span>||
| <span data-ttu-id="0083c-327">excludeContext</span><span class="sxs-lookup"><span data-stu-id="0083c-327">excludeContext</span></span>|<span data-ttu-id="0083c-328">ブール値</span><span class="sxs-lookup"><span data-stu-id="0083c-328">boolean</span></span>||
| <span data-ttu-id="0083c-329">filterLocalOnly?</span><span class="sxs-lookup"><span data-stu-id="0083c-329">filterLocalOnly?</span></span>|<span data-ttu-id="0083c-330">ブール値</span><span class="sxs-lookup"><span data-stu-id="0083c-330">boolean</span></span>||

#### <a name="returns-navigationargsview-model-ipage-inavigationargsmd"></a><span data-ttu-id="0083c-331">[NavigationArgs](view-model-ipage-inavigationargs.md) を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-331">Returns [NavigationArgs](view-model-ipage-inavigationargs.md)</span></span>



### <a name="hidenavigation"></a><span data-ttu-id="0083c-332">hideNavigation</span><span class="sxs-lookup"><span data-stu-id="0083c-332">hideNavigation</span></span>


<span data-ttu-id="0083c-333">hideNavigation(pageNamesToHide: string [ ]): any</span><span class="sxs-lookup"><span data-stu-id="0083c-333">hideNavigation(pageNamesToHide: string [ ]): any</span></span>

<span data-ttu-id="0083c-334">既定のランディング ページから指定されたページを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="0083c-334">Hides the specified page(s) from the default landing page.</span></span>
<span data-ttu-id="0083c-335">例 :</span><span class="sxs-lookup"><span data-stu-id="0083c-335">Example:</span></span>

```javascript
metadataService.hideNavigation('Select-a-customer', 'Select-a-vehicle');
```


#### <a name="parameters"></a><span data-ttu-id="0083c-336">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0083c-336">Parameters</span></span>

| <span data-ttu-id="0083c-337">氏名</span><span class="sxs-lookup"><span data-stu-id="0083c-337">Name</span></span> | <span data-ttu-id="0083c-338">種類</span><span class="sxs-lookup"><span data-stu-id="0083c-338">Type</span></span> | <span data-ttu-id="0083c-339">説明</span><span class="sxs-lookup"><span data-stu-id="0083c-339">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0083c-340">pageNamesToHide</span><span class="sxs-lookup"><span data-stu-id="0083c-340">pageNamesToHide</span></span>|<span data-ttu-id="0083c-341">string [ ]</span><span class="sxs-lookup"><span data-stu-id="0083c-341">string [ ]</span></span>|<span data-ttu-id="0083c-342">ページ名</span><span class="sxs-lookup"><span data-stu-id="0083c-342">Page name(s)</span></span>|

#### <a name="returns-any"></a><span data-ttu-id="0083c-343">any を返します</span><span class="sxs-lookup"><span data-stu-id="0083c-343">Returns any</span></span>

