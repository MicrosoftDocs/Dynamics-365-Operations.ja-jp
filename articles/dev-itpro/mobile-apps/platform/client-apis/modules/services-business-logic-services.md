---
title: "サービス モジュール"
description: "クライアントの実行時に、アプリケーションで使用できるさまざまなサービス。"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8a19ede998e8e4b30faef73ff401855dc5ae0e44
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="services-module"></a><span data-ttu-id="609bb-103">サービス モジュール</span><span class="sxs-lookup"><span data-stu-id="609bb-103">Services module</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="609bb-104">クライアントの実行時に、アプリケーションで使用できるさまざまなサービス。</span><span class="sxs-lookup"><span data-stu-id="609bb-104">Various services that are available to the application in client runtime.</span></span>

## <a name="index"></a><span data-ttu-id="609bb-105">指数</span><span class="sxs-lookup"><span data-stu-id="609bb-105">Index</span></span>

### <a name="types"></a><span data-ttu-id="609bb-106">種類</span><span class="sxs-lookup"><span data-stu-id="609bb-106">Types</span></span>

* [<span data-ttu-id="609bb-107">AsyncService</span><span class="sxs-lookup"><span data-stu-id="609bb-107">AsyncService</span></span>](../interfaces/services-business-logic-services-iasyncservice.md)
* [<span data-ttu-id="609bb-108">CacheService</span><span class="sxs-lookup"><span data-stu-id="609bb-108">CacheService</span></span>](../interfaces/services-business-logic-services-icacheservice.md)
* [<span data-ttu-id="609bb-109">DataService</span><span class="sxs-lookup"><span data-stu-id="609bb-109">DataService</span></span>](../interfaces/services-business-logic-services-idataservice.md)
* [<span data-ttu-id="609bb-110">MetadataService</span><span class="sxs-lookup"><span data-stu-id="609bb-110">MetadataService</span></span>](../interfaces/services-business-logic-services-imetadataservice.md)
* [<span data-ttu-id="609bb-111">PageData</span><span class="sxs-lookup"><span data-stu-id="609bb-111">PageData</span></span>](../interfaces/services-business-logic-services-ipagedata.md)

### <a name="type-aliases"></a><span data-ttu-id="609bb-112">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="609bb-112">Type aliases</span></span>

* [<span data-ttu-id="609bb-113">ExpressionOperator</span><span class="sxs-lookup"><span data-stu-id="609bb-113">ExpressionOperator</span></span>](services-business-logic-services.md#expressionoperator)

## <a name="types"></a><span data-ttu-id="609bb-114">種類</span><span class="sxs-lookup"><span data-stu-id="609bb-114">Types</span></span>


### <a name="asyncservice"></a><span data-ttu-id="609bb-115">AsyncService</span><span class="sxs-lookup"><span data-stu-id="609bb-115">AsyncService</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="609bb-116">階層</span><span class="sxs-lookup"><span data-stu-id="609bb-116">Hierarchy</span></span>

<span data-ttu-id="609bb-117">AsyncService</span><span class="sxs-lookup"><span data-stu-id="609bb-117">AsyncService</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="609bb-118">メソッド</span><span class="sxs-lookup"><span data-stu-id="609bb-118">Methods</span></span>

| <span data-ttu-id="609bb-119">氏名</span><span class="sxs-lookup"><span data-stu-id="609bb-119">Name</span></span> | <span data-ttu-id="609bb-120">署名</span><span class="sxs-lookup"><span data-stu-id="609bb-120">Signature</span></span> | <span data-ttu-id="609bb-121">説明</span><span class="sxs-lookup"><span data-stu-id="609bb-121">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="609bb-122">すべて</span><span class="sxs-lookup"><span data-stu-id="609bb-122">all</span></span>](../interfaces/services-business-logic-services-iasyncservice.md#all) |<span data-ttu-id="609bb-123">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span><span class="sxs-lookup"><span data-stu-id="609bb-123">all(...args: any [ ]): Promise &lt;any [ ]&gt;</span></span>|  |
| [<span data-ttu-id="609bb-124">延期</span><span class="sxs-lookup"><span data-stu-id="609bb-124">defer</span></span>](../interfaces/services-business-logic-services-iasyncservice.md#defer) |<span data-ttu-id="609bb-125">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span><span class="sxs-lookup"><span data-stu-id="609bb-125">defer &lt;T&gt;(): [Deferred](../interfaces/defer-ideferred.md) &lt;T&gt;</span></span>|<span data-ttu-id="609bb-126">イベント ハンドラー (該当する場合) から回答を返し、非同期でそれらを拒否または解決するために使用できる遅延オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="609bb-126">Creates a deferred object which can be used to return a promise from event handlers (where applicable) and resolve reject them asynchronously.</span></span><br>  |


### <a name="cacheservice"></a><span data-ttu-id="609bb-127">CacheService</span><span class="sxs-lookup"><span data-stu-id="609bb-127">CacheService</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="609bb-128">階層</span><span class="sxs-lookup"><span data-stu-id="609bb-128">Hierarchy</span></span>

<span data-ttu-id="609bb-129">CacheService</span><span class="sxs-lookup"><span data-stu-id="609bb-129">CacheService</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="609bb-130">メソッド</span><span class="sxs-lookup"><span data-stu-id="609bb-130">Methods</span></span>

| <span data-ttu-id="609bb-131">氏名</span><span class="sxs-lookup"><span data-stu-id="609bb-131">Name</span></span> | <span data-ttu-id="609bb-132">署名</span><span class="sxs-lookup"><span data-stu-id="609bb-132">Signature</span></span> | <span data-ttu-id="609bb-133">説明</span><span class="sxs-lookup"><span data-stu-id="609bb-133">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="609bb-134">getData</span><span class="sxs-lookup"><span data-stu-id="609bb-134">getData</span></span>](../interfaces/services-business-logic-services-icacheservice.md#getdata) |<span data-ttu-id="609bb-135">getData(cacheKey: string): any</span><span class="sxs-lookup"><span data-stu-id="609bb-135">getData(cacheKey: string): any</span></span>|  |
| [<span data-ttu-id="609bb-136">setData</span><span class="sxs-lookup"><span data-stu-id="609bb-136">setData</span></span>](../interfaces/services-business-logic-services-icacheservice.md#setdata) |<span data-ttu-id="609bb-137">setData(cacheKey: string, data: any): any</span><span class="sxs-lookup"><span data-stu-id="609bb-137">setData(cacheKey: string, data: any): any</span></span>|  |


### <a name="dataservice"></a><span data-ttu-id="609bb-138">DataService</span><span class="sxs-lookup"><span data-stu-id="609bb-138">DataService</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="609bb-139">階層</span><span class="sxs-lookup"><span data-stu-id="609bb-139">Hierarchy</span></span>

<span data-ttu-id="609bb-140">DataService</span><span class="sxs-lookup"><span data-stu-id="609bb-140">DataService</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="609bb-141">メソッド</span><span class="sxs-lookup"><span data-stu-id="609bb-141">Methods</span></span>

| <span data-ttu-id="609bb-142">氏名</span><span class="sxs-lookup"><span data-stu-id="609bb-142">Name</span></span> | <span data-ttu-id="609bb-143">署名</span><span class="sxs-lookup"><span data-stu-id="609bb-143">Signature</span></span> | <span data-ttu-id="609bb-144">説明</span><span class="sxs-lookup"><span data-stu-id="609bb-144">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="609bb-145">findEntityData</span><span class="sxs-lookup"><span data-stu-id="609bb-145">findEntityData</span></span>](../interfaces/services-business-logic-services-idataservice.md#findentitydata) |<span data-ttu-id="609bb-146">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span><span class="sxs-lookup"><span data-stu-id="609bb-146">findEntityData(entityType: any, propertyName: string, propertyValue: any, includeChanges?: boolean): any</span></span>|  |
| [<span data-ttu-id="609bb-147">getEntityData</span><span class="sxs-lookup"><span data-stu-id="609bb-147">getEntityData</span></span>](../interfaces/services-business-logic-services-idataservice.md#getentitydata) |<span data-ttu-id="609bb-148">getEntityData(entityType: any, entityId: string): any</span><span class="sxs-lookup"><span data-stu-id="609bb-148">getEntityData(entityType: any, entityId: string): any</span></span>|  |
| [<span data-ttu-id="609bb-149">getPageData</span><span class="sxs-lookup"><span data-stu-id="609bb-149">getPageData</span></span>](../interfaces/services-business-logic-services-idataservice.md#getpagedata) |<span data-ttu-id="609bb-150">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](../interfaces/services-business-logic-services-ipagedata.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="609bb-150">getPageData(pageId: string, context: any, filter: any, allowedStaleness: number): Promise &lt;[PageData](../interfaces/services-business-logic-services-ipagedata.md)&gt;</span></span>|  |


### <a name="metadataservice"></a><span data-ttu-id="609bb-151">MetadataService</span><span class="sxs-lookup"><span data-stu-id="609bb-151">MetadataService</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="609bb-152">階層</span><span class="sxs-lookup"><span data-stu-id="609bb-152">Hierarchy</span></span>

<span data-ttu-id="609bb-153">MetadataService</span><span class="sxs-lookup"><span data-stu-id="609bb-153">MetadataService</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="609bb-154">プロパティ</span><span class="sxs-lookup"><span data-stu-id="609bb-154">Properties</span></span>

| <span data-ttu-id="609bb-155">氏名</span><span class="sxs-lookup"><span data-stu-id="609bb-155">Name</span></span> | <span data-ttu-id="609bb-156">署名</span><span class="sxs-lookup"><span data-stu-id="609bb-156">Signature</span></span> | <span data-ttu-id="609bb-157">説明</span><span class="sxs-lookup"><span data-stu-id="609bb-157">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="609bb-158">バージョン</span><span class="sxs-lookup"><span data-stu-id="609bb-158">version</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#version) |<span data-ttu-id="609bb-159">version: string</span><span class="sxs-lookup"><span data-stu-id="609bb-159">version: string</span></span> <br>|<span data-ttu-id="609bb-160">現在実行中のプラットフォームのバージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="609bb-160">Gets the version of the platform currently running.</span></span><br>  |

#### <a name="methods"></a><span data-ttu-id="609bb-161">メソッド</span><span class="sxs-lookup"><span data-stu-id="609bb-161">Methods</span></span>

| <span data-ttu-id="609bb-162">氏名</span><span class="sxs-lookup"><span data-stu-id="609bb-162">Name</span></span> | <span data-ttu-id="609bb-163">署名</span><span class="sxs-lookup"><span data-stu-id="609bb-163">Signature</span></span> | <span data-ttu-id="609bb-164">説明</span><span class="sxs-lookup"><span data-stu-id="609bb-164">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="609bb-165">addControl</span><span class="sxs-lookup"><span data-stu-id="609bb-165">addControl</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#addcontrol) |<span data-ttu-id="609bb-166">addControl(componentName: string, controlName: string, controlType: [ControlType](view-model-control-basecontrol-icontrol.md#controltype), parentContainerName?: string, options?: [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="609bb-166">addControl(componentName: string, controlName: string, controlType: [ControlType](view-model-control-basecontrol-icontrol.md#controltype), parentContainerName?: string, options?: [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any</span></span>|  |
| [<span data-ttu-id="609bb-167">compareVersion</span><span class="sxs-lookup"><span data-stu-id="609bb-167">compareVersion</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#compareversion) |<span data-ttu-id="609bb-168">compareVersion(versionToCompare: string): 1 &#124; -1</span><span class="sxs-lookup"><span data-stu-id="609bb-168">compareVersion(versionToCompare: string): 1 &#124; -1</span></span>|<span data-ttu-id="609bb-169">現在のプラットフォームのバージョンと参照バージョンを比較します。</span><span class="sxs-lookup"><span data-stu-id="609bb-169">Compares the current platform version with a reference version.</span></span><br>  |
| [<span data-ttu-id="609bb-170">configureAction</span><span class="sxs-lookup"><span data-stu-id="609bb-170">configureAction</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#configureaction) |<span data-ttu-id="609bb-171">configureAction(actionName: string, options: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="609bb-171">configureAction(actionName: string, options: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)): any</span></span>|<span data-ttu-id="609bb-172">アクションをコンフィギュレーションすると、そのアクションに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="609bb-172">Configuring an action allows specifying or overriding certain behaviors specific to actions.</span></span><br>  |
| [<span data-ttu-id="609bb-173">configureControl</span><span class="sxs-lookup"><span data-stu-id="609bb-173">configureControl</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#configurecontrol) |<span data-ttu-id="609bb-174">configureControl(componentName: string, controlName: string, options: [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="609bb-174">configureControl(componentName: string, controlName: string, options: [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)): any</span></span>|<span data-ttu-id="609bb-175">コントロールをコンフィギュレーションすると、そのコントロールに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="609bb-175">Configuring a control allows specifying or overriding certain behaviors specific to the control.</span></span> <span data-ttu-id="609bb-176">使用可能な動作はコントロール タイプで異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="609bb-176">Note that the available behaviors vary by control type.</span></span><br>  |
| [<span data-ttu-id="609bb-177">configureEntity</span><span class="sxs-lookup"><span data-stu-id="609bb-177">configureEntity</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#configureentity) |<span data-ttu-id="609bb-178">configureEntity(entityName: string, options: any): any</span><span class="sxs-lookup"><span data-stu-id="609bb-178">configureEntity(entityName: string, options: any): any</span></span>|<span data-ttu-id="609bb-179">エンティティをコンフィギュレーションすると、そのエンティティに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="609bb-179">Configuring an entity allows specifying or overriding certain behaviors specific to the entity.</span></span><br>  |
| [<span data-ttu-id="609bb-180">configureLookup</span><span class="sxs-lookup"><span data-stu-id="609bb-180">configureLookup</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#configurelookup) |<span data-ttu-id="609bb-181">configureLookup(taskName: string, lookupControlName: string, options: [LookupMetadata](../interfaces/view-model-control-lookup-ilookup-ilookupmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="609bb-181">configureLookup(taskName: string, lookupControlName: string, options: [LookupMetadata](../interfaces/view-model-control-lookup-ilookup-ilookupmetadata.md)): any</span></span>|<span data-ttu-id="609bb-182">アクションのフィールドをルックアップとして動作するようにコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="609bb-182">Configures a field on an action to behave as a lookup.</span></span> <span data-ttu-id="609bb-183">リスト コントロールを含む既存のページを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="609bb-183">Requires using an existing page which contains a list control.</span></span><br>  |
| [<span data-ttu-id="609bb-184">configurePage</span><span class="sxs-lookup"><span data-stu-id="609bb-184">configurePage</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#configurepage) |<span data-ttu-id="609bb-185">configurePage(pageName: string, options: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="609bb-185">configurePage(pageName: string, options: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)): any</span></span>|<span data-ttu-id="609bb-186">ページをコンフィギュレーションすると、そのページに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="609bb-186">Configuring a Page allows specifying or overriding certain behaviors specific to the Page.</span></span><br>  |
| [<span data-ttu-id="609bb-187">configureWorkspace</span><span class="sxs-lookup"><span data-stu-id="609bb-187">configureWorkspace</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#configureworkspace) |<span data-ttu-id="609bb-188">configureWorkspace(options: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="609bb-188">configureWorkspace(options: [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)): any</span></span>|<span data-ttu-id="609bb-189">ワークスペースをコンフィギュレーションすると、そのワークスペースに固有の特定の動作を指定または上書きできます。</span><span class="sxs-lookup"><span data-stu-id="609bb-189">Configuring a workspace allows specifying or overriding certain behaviors specific to the workspace.</span></span><br>  |
| [<span data-ttu-id="609bb-190">findAction</span><span class="sxs-lookup"><span data-stu-id="609bb-190">findAction</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#findaction) |<span data-ttu-id="609bb-191">findAction(actionName: string): [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="609bb-191">findAction(actionName: string): [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)</span></span>|<span data-ttu-id="609bb-192">メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたアクションの現在のメタデータ インスタンスのコピーを取得します。</span><span class="sxs-lookup"><span data-stu-id="609bb-192">Gets a copy of the current metadata instance of a specified Action, for the purpose of inspecting the metadata (not to be used for changing the metadata).</span></span><br>  |
| [<span data-ttu-id="609bb-193">findControl</span><span class="sxs-lookup"><span data-stu-id="609bb-193">findControl</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#findcontrol) |<span data-ttu-id="609bb-194">findControl(componentMetadata: any, controlName: string): [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="609bb-194">findControl(componentMetadata: any, controlName: string): [ControlMetadata](../interfaces/view-model-control-basecontrol-icontrol-icontrolmetadata.md)</span></span>|<span data-ttu-id="609bb-195">メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたコントロールの現在のメタデータ インスタンスのコピーを取得します。</span><span class="sxs-lookup"><span data-stu-id="609bb-195">Gets a copy of the current metadata instance of a specified control, for the purpose of inspecting the metadata (not to be used for changing the metadata).</span></span><br>  |
| [<span data-ttu-id="609bb-196">findPage</span><span class="sxs-lookup"><span data-stu-id="609bb-196">findPage</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#findpage) |<span data-ttu-id="609bb-197">findPage(pageName: string): [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)</span><span class="sxs-lookup"><span data-stu-id="609bb-197">findPage(pageName: string): [PageMetadata](../interfaces/view-model-ipage-ipagemetadata.md)</span></span>|<span data-ttu-id="609bb-198">メタデータ (メタデータを変更するために使用されない) を検査するため、指定されたページの現在のメタデータ インスタンスのコピーを取得します。</span><span class="sxs-lookup"><span data-stu-id="609bb-198">Gets a copy of the current metadata instance of a specified page, for the purpose of inspecting the metadata (not to be used for changing the metadata).</span></span><br>  |
| [<span data-ttu-id="609bb-199">getFilterExpression</span><span class="sxs-lookup"><span data-stu-id="609bb-199">getFilterExpression</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#getfilterexpression) |<span data-ttu-id="609bb-200">getFilterExpression(pageName: string, listControlName: string, controlName: string, operator: [ExpressionOperator](services-business-logic-services.md#expressionoperator), value: string): DataFilter</span><span class="sxs-lookup"><span data-stu-id="609bb-200">getFilterExpression(pageName: string, listControlName: string, controlName: string, operator: [ExpressionOperator](services-business-logic-services.md#expressionoperator), value: string): DataFilter</span></span>|<span data-ttu-id="609bb-201">指定されたオプションに基づいてリスト コントロール用の DataFilter オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="609bb-201">Create a DataFilter object for a list control based on the provided options.</span></span><br>  |
| [<span data-ttu-id="609bb-202">getFormReference</span><span class="sxs-lookup"><span data-stu-id="609bb-202">getFormReference</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#getformreference) |<span data-ttu-id="609bb-203">getFormReference(componentName: string, filterContext: DataFilter, excludeContext: boolean, filterLocalOnly?: boolean): [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md)</span><span class="sxs-lookup"><span data-stu-id="609bb-203">getFormReference(componentName: string, filterContext: DataFilter, excludeContext: boolean, filterLocalOnly?: boolean): [NavigationArgs](../interfaces/view-model-ipage-inavigationargs.md)</span></span>|<span data-ttu-id="609bb-204">ナビゲーション コントロールで使用する特定のページ アクションに対し INavigationArgs オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="609bb-204">Create an INavigationArgs object for a specific page action to be used with a navigation control.</span></span><br>  |
| [<span data-ttu-id="609bb-205">hideNavigation</span><span class="sxs-lookup"><span data-stu-id="609bb-205">hideNavigation</span></span>](../interfaces/services-business-logic-services-imetadataservice.md#hidenavigation) |<span data-ttu-id="609bb-206">hideNavigation(pageNamesToHide: string [ ]): any</span><span class="sxs-lookup"><span data-stu-id="609bb-206">hideNavigation(pageNamesToHide: string [ ]): any</span></span>|<span data-ttu-id="609bb-207">既定のランディング ページから指定されたページを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="609bb-207">Hides the specified page(s) from the default landing page.</span></span><br>  |


### <a name="pagedata"></a><span data-ttu-id="609bb-208">PageData</span><span class="sxs-lookup"><span data-stu-id="609bb-208">PageData</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="609bb-209">階層</span><span class="sxs-lookup"><span data-stu-id="609bb-209">Hierarchy</span></span>

<span data-ttu-id="609bb-210">PageData</span><span class="sxs-lookup"><span data-stu-id="609bb-210">PageData</span></span> <br>

#### <a name="methods"></a><span data-ttu-id="609bb-211">メソッド</span><span class="sxs-lookup"><span data-stu-id="609bb-211">Methods</span></span>

| <span data-ttu-id="609bb-212">氏名</span><span class="sxs-lookup"><span data-stu-id="609bb-212">Name</span></span> | <span data-ttu-id="609bb-213">署名</span><span class="sxs-lookup"><span data-stu-id="609bb-213">Signature</span></span> | <span data-ttu-id="609bb-214">説明</span><span class="sxs-lookup"><span data-stu-id="609bb-214">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="609bb-215">getControlValue</span><span class="sxs-lookup"><span data-stu-id="609bb-215">getControlValue</span></span>](../interfaces/services-business-logic-services-ipagedata.md#getcontrolvalue) |<span data-ttu-id="609bb-216">getControlValue(controlName: string): any</span><span class="sxs-lookup"><span data-stu-id="609bb-216">getControlValue(controlName: string): any</span></span>|<span data-ttu-id="609bb-217">ページでデータ セットから直接読み込まれるコントロールの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="609bb-217">Gets the value of a control directly from the data set loaded in the page.</span></span><br>  |
| [<span data-ttu-id="609bb-218">setControlValue</span><span class="sxs-lookup"><span data-stu-id="609bb-218">setControlValue</span></span>](../interfaces/services-business-logic-services-ipagedata.md#setcontrolvalue) |<span data-ttu-id="609bb-219">setControlValue(controlName: string, value: any): any</span><span class="sxs-lookup"><span data-stu-id="609bb-219">setControlValue(controlName: string, value: any): any</span></span>|<span data-ttu-id="609bb-220">ページでデータ セットに直接読み込まれるコントロールの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="609bb-220">Sets the value of a control directly into the data set loaded in the page.</span></span><br>  |

## <a name="type-aliases"></a><span data-ttu-id="609bb-221">型のエイリアス</span><span class="sxs-lookup"><span data-stu-id="609bb-221">Type aliases</span></span>


### <a name="expressionoperator"></a><span data-ttu-id="609bb-222">ExpressionOperator</span><span class="sxs-lookup"><span data-stu-id="609bb-222">ExpressionOperator</span></span>
<span data-ttu-id="609bb-223">ExpressionOperator: 「Is」 &#124; 「IsNot」 &#124; 「Contains」 &#124; 「BeginsWith」 &#124; 「EndsWith」 &#124; 「GreaterThan」 &#124; 「LessThan」 &#124; 「GreaterThanOrEqual」 &#124; 「LessThanOrEqual」</span><span class="sxs-lookup"><span data-stu-id="609bb-223">ExpressionOperator: "Is" &#124; "IsNot" &#124; "Contains" &#124; "BeginsWith" &#124; "EndsWith" &#124; "GreaterThan" &#124; "LessThan" &#124; "GreaterThanOrEqual" &#124; "LessThanOrEqual"</span></span>


<span data-ttu-id="609bb-224">フィルターの定義およびその他の場所で使用される式演算子の使用可能な値を表します</span><span class="sxs-lookup"><span data-stu-id="609bb-224">Represents possible values for the expression operator used in defining filters and in other places</span></span>


