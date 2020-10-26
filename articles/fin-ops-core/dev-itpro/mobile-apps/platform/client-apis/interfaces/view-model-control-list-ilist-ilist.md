---
title: リスト タイプ
description: リスト コントロール タイプ。
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 18ab57c706418758ded8ab164025e235a0f31510
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982765"
---
# <a name="list-type"></a><span data-ttu-id="b3535-103">リスト タイプ</span><span class="sxs-lookup"><span data-stu-id="b3535-103">List type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="b3535-104">リスト コントロール タイプ。</span><span class="sxs-lookup"><span data-stu-id="b3535-104">List control type.</span></span>
<span data-ttu-id="b3535-105">リストは、任意の数の行を含むコントロールです。</span><span class="sxs-lookup"><span data-stu-id="b3535-105">A list is a control that contains any numbers of rows.</span></span>
<span data-ttu-id="b3535-106">各行は、任意の数のコントロールに対するレイアウト用テンプレートに従います。</span><span class="sxs-lookup"><span data-stu-id="b3535-106">Each row follows a template for the layout of any number of controls.</span></span>
<span data-ttu-id="b3535-107">リストには簡易とカードの 2 つのスタイルがあります。</span><span class="sxs-lookup"><span data-stu-id="b3535-107">Lists come in two styles: simple and card.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="b3535-108">階層</span><span class="sxs-lookup"><span data-stu-id="b3535-108">Hierarchy</span></span>

[<span data-ttu-id="b3535-109">ContainerControl</span><span class="sxs-lookup"><span data-stu-id="b3535-109">ContainerControl</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md) <br><span data-ttu-id="b3535-110">&nbsp;&nbsp;&nbsp;└─ リスト</span><span class="sxs-lookup"><span data-stu-id="b3535-110">&nbsp;&nbsp;&nbsp;└─ List</span></span> <br>

## <a name="index"></a><span data-ttu-id="b3535-111">指数</span><span class="sxs-lookup"><span data-stu-id="b3535-111">Index</span></span>

### <a name="properties"></a><span data-ttu-id="b3535-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b3535-112">Properties</span></span>

* [<span data-ttu-id="b3535-113">$accessibility</span><span class="sxs-lookup"><span data-stu-id="b3535-113">$accessibility</span></span>](view-model-control-list-ilist-ilist.md#accessibility)
* [<span data-ttu-id="b3535-114">DefaultSearchColumn</span><span class="sxs-lookup"><span data-stu-id="b3535-114">DefaultSearchColumn</span></span>](view-model-control-list-ilist-ilist.md#defaultsearchcolumn)
* [<span data-ttu-id="b3535-115">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b3535-115">container</span></span>](view-model-control-list-ilist-ilist.md#container)
* [<span data-ttu-id="b3535-116">emptyListMessage</span><span class="sxs-lookup"><span data-stu-id="b3535-116">emptyListMessage</span></span>](view-model-control-list-ilist-ilist.md#emptylistmessage)
* [<span data-ttu-id="b3535-117">enableMultiSelect</span><span class="sxs-lookup"><span data-stu-id="b3535-117">enableMultiSelect</span></span>](view-model-control-list-ilist-ilist.md#enablemultiselect)
* [<span data-ttu-id="b3535-118">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="b3535-118">generic</span></span>](view-model-control-list-ilist-ilist.md#generic)
* [<span data-ttu-id="b3535-119">getDataSource</span><span class="sxs-lookup"><span data-stu-id="b3535-119">getDataSource</span></span>](view-model-control-list-ilist-ilist.md#getdatasource)
* [<span data-ttu-id="b3535-120">非表示</span><span class="sxs-lookup"><span data-stu-id="b3535-120">hidden</span></span>](view-model-control-list-ilist-ilist.md#hidden)
* [<span data-ttu-id="b3535-121">hideEmptyListMessage</span><span class="sxs-lookup"><span data-stu-id="b3535-121">hideEmptyListMessage</span></span>](view-model-control-list-ilist-ilist.md#hideemptylistmessage)
* [<span data-ttu-id="b3535-122">imageFields</span><span class="sxs-lookup"><span data-stu-id="b3535-122">imageFields</span></span>](view-model-control-list-ilist-ilist.md#imagefields)
* [<span data-ttu-id="b3535-123">performingRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="b3535-123">performingRemoteSearch</span></span>](view-model-control-list-ilist-ilist.md#performingremotesearch)
* [<span data-ttu-id="b3535-124">searchQuery</span><span class="sxs-lookup"><span data-stu-id="b3535-124">searchQuery</span></span>](view-model-control-list-ilist-ilist.md#searchquery)

### <a name="methods"></a><span data-ttu-id="b3535-125">メソッド</span><span class="sxs-lookup"><span data-stu-id="b3535-125">Methods</span></span>

* [<span data-ttu-id="b3535-126">allowsNavigation</span><span class="sxs-lookup"><span data-stu-id="b3535-126">allowsNavigation</span></span>](view-model-control-list-ilist-ilist.md#allowsnavigation)
* [<span data-ttu-id="b3535-127">applyDesign</span><span class="sxs-lookup"><span data-stu-id="b3535-127">applyDesign</span></span>](view-model-control-list-ilist-ilist.md#applydesign)
* [<span data-ttu-id="b3535-128">applySearch</span><span class="sxs-lookup"><span data-stu-id="b3535-128">applySearch</span></span>](view-model-control-list-ilist-ilist.md#applysearch)
* [<span data-ttu-id="b3535-129">canPerformRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="b3535-129">canPerformRemoteSearch</span></span>](view-model-control-list-ilist-ilist.md#canperformremotesearch)
* [<span data-ttu-id="b3535-130">clearSearch</span><span class="sxs-lookup"><span data-stu-id="b3535-130">clearSearch</span></span>](view-model-control-list-ilist-ilist.md#clearsearch)
* [<span data-ttu-id="b3535-131">dataContext</span><span class="sxs-lookup"><span data-stu-id="b3535-131">dataContext</span></span>](view-model-control-list-ilist-ilist.md#datacontext)
* [<span data-ttu-id="b3535-132">getColumnLabel</span><span class="sxs-lookup"><span data-stu-id="b3535-132">getColumnLabel</span></span>](view-model-control-list-ilist-ilist.md#getcolumnlabel)
* [<span data-ttu-id="b3535-133">getControl</span><span class="sxs-lookup"><span data-stu-id="b3535-133">getControl</span></span>](view-model-control-list-ilist-ilist.md#getcontrol)
* [<span data-ttu-id="b3535-134">getControlById</span><span class="sxs-lookup"><span data-stu-id="b3535-134">getControlById</span></span>](view-model-control-list-ilist-ilist.md#getcontrolbyid)
* [<span data-ttu-id="b3535-135">getControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b3535-135">getControlMetadata</span></span>](view-model-control-list-ilist-ilist.md#getcontrolmetadata)
* [<span data-ttu-id="b3535-136">getControlMetadataById</span><span class="sxs-lookup"><span data-stu-id="b3535-136">getControlMetadataById</span></span>](view-model-control-list-ilist-ilist.md#getcontrolmetadatabyid)
* [<span data-ttu-id="b3535-137">getData</span><span class="sxs-lookup"><span data-stu-id="b3535-137">getData</span></span>](view-model-control-list-ilist-ilist.md#getdata)
* [<span data-ttu-id="b3535-138">getDesign</span><span class="sxs-lookup"><span data-stu-id="b3535-138">getDesign</span></span>](view-model-control-list-ilist-ilist.md#getdesign)
* [<span data-ttu-id="b3535-139">getListData</span><span class="sxs-lookup"><span data-stu-id="b3535-139">getListData</span></span>](view-model-control-list-ilist-ilist.md#getlistdata)
* [<span data-ttu-id="b3535-140">getRenderedRows</span><span class="sxs-lookup"><span data-stu-id="b3535-140">getRenderedRows</span></span>](view-model-control-list-ilist-ilist.md#getrenderedrows)
* [<span data-ttu-id="b3535-141">getRowNavigation</span><span class="sxs-lookup"><span data-stu-id="b3535-141">getRowNavigation</span></span>](view-model-control-list-ilist-ilist.md#getrownavigation)
* [<span data-ttu-id="b3535-142">getRowSelectionCount</span><span class="sxs-lookup"><span data-stu-id="b3535-142">getRowSelectionCount</span></span>](view-model-control-list-ilist-ilist.md#getrowselectioncount)
* [<span data-ttu-id="b3535-143">getRowSelections</span><span class="sxs-lookup"><span data-stu-id="b3535-143">getRowSelections</span></span>](view-model-control-list-ilist-ilist.md#getrowselections)
* [<span data-ttu-id="b3535-144">getRowTracking</span><span class="sxs-lookup"><span data-stu-id="b3535-144">getRowTracking</span></span>](view-model-control-list-ilist-ilist.md#getrowtracking)
* [<span data-ttu-id="b3535-145">getSearchColumn</span><span class="sxs-lookup"><span data-stu-id="b3535-145">getSearchColumn</span></span>](view-model-control-list-ilist-ilist.md#getsearchcolumn)
* [<span data-ttu-id="b3535-146">getSearchColumnLabel</span><span class="sxs-lookup"><span data-stu-id="b3535-146">getSearchColumnLabel</span></span>](view-model-control-list-ilist-ilist.md#getsearchcolumnlabel)
* [<span data-ttu-id="b3535-147">getSearchableColumns</span><span class="sxs-lookup"><span data-stu-id="b3535-147">getSearchableColumns</span></span>](view-model-control-list-ilist-ilist.md#getsearchablecolumns)
* [<span data-ttu-id="b3535-148">hideSearchBar</span><span class="sxs-lookup"><span data-stu-id="b3535-148">hideSearchBar</span></span>](view-model-control-list-ilist-ilist.md#hidesearchbar)
* [<span data-ttu-id="b3535-149">isEditable</span><span class="sxs-lookup"><span data-stu-id="b3535-149">isEditable</span></span>](view-model-control-list-ilist-ilist.md#iseditable)
* [<span data-ttu-id="b3535-150">loadMetaData</span><span class="sxs-lookup"><span data-stu-id="b3535-150">loadMetaData</span></span>](view-model-control-list-ilist-ilist.md#loadmetadata)
* [<span data-ttu-id="b3535-151">loadMore</span><span class="sxs-lookup"><span data-stu-id="b3535-151">loadMore</span></span>](view-model-control-list-ilist-ilist.md#loadmore)
* [<span data-ttu-id="b3535-152">メタデータ</span><span class="sxs-lookup"><span data-stu-id="b3535-152">metadata</span></span>](view-model-control-list-ilist-ilist.md#metadata)
* [<span data-ttu-id="b3535-153">親</span><span class="sxs-lookup"><span data-stu-id="b3535-153">parent</span></span>](view-model-control-list-ilist-ilist.md#parent)
* [<span data-ttu-id="b3535-154">performRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="b3535-154">performRemoteSearch</span></span>](view-model-control-list-ilist-ilist.md#performremotesearch)
* [<span data-ttu-id="b3535-155">ルート</span><span class="sxs-lookup"><span data-stu-id="b3535-155">root</span></span>](view-model-control-list-ilist-ilist.md#root)
* [<span data-ttu-id="b3535-156">selectSearchColumn</span><span class="sxs-lookup"><span data-stu-id="b3535-156">selectSearchColumn</span></span>](view-model-control-list-ilist-ilist.md#selectsearchcolumn)
* [<span data-ttu-id="b3535-157">setRowSections</span><span class="sxs-lookup"><span data-stu-id="b3535-157">setRowSections</span></span>](view-model-control-list-ilist-ilist.md#setrowsections)

### <a name="events"></a><span data-ttu-id="b3535-158">イベント</span><span class="sxs-lookup"><span data-stu-id="b3535-158">Events</span></span>

* [<span data-ttu-id="b3535-159">onRowCreate</span><span class="sxs-lookup"><span data-stu-id="b3535-159">onRowCreate</span></span>](view-model-control-list-ilist-ilist.md#onrowcreate)
* [<span data-ttu-id="b3535-160">onRowSelect</span><span class="sxs-lookup"><span data-stu-id="b3535-160">onRowSelect</span></span>](view-model-control-list-ilist-ilist.md#onrowselect)

## <a name="properties"></a><span data-ttu-id="b3535-161">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b3535-161">Properties</span></span>

### <a name="accessibility"></a><span data-ttu-id="b3535-162">$accessibility</span><span class="sxs-lookup"><span data-stu-id="b3535-162">$accessibility</span></span>

<span data-ttu-id="b3535-163">$accessibility: すべて</span><span class="sxs-lookup"><span data-stu-id="b3535-163">$accessibility: any</span></span>




### <a name="defaultsearchcolumn"></a><span data-ttu-id="b3535-164">DefaultSearchColumn</span><span class="sxs-lookup"><span data-stu-id="b3535-164">DefaultSearchColumn</span></span>

<span data-ttu-id="b3535-165">DefaultSearchColumn: 文字列</span><span class="sxs-lookup"><span data-stu-id="b3535-165">DefaultSearchColumn: string</span></span>




### <a name="container"></a><span data-ttu-id="b3535-166">コンテナー</span><span class="sxs-lookup"><span data-stu-id="b3535-166">container</span></span>

<span data-ttu-id="b3535-167">container: ブール値</span><span class="sxs-lookup"><span data-stu-id="b3535-167">container: boolean</span></span>

<span data-ttu-id="b3535-168">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="b3535-168">True if the control is a container.</span></span>

> <span data-ttu-id="b3535-169">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[container](view-model-control-container-icontainercontrol-icontainercontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-169">Inherited from [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[container](view-model-control-container-icontainercontrol-icontainercontrol.md#container)</span></span>
> 
> <span data-ttu-id="b3535-170">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="b3535-170">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="emptylistmessage"></a><span data-ttu-id="b3535-171">emptyListMessage</span><span class="sxs-lookup"><span data-stu-id="b3535-171">emptyListMessage</span></span>

<span data-ttu-id="b3535-172">emptyListMessage: string</span><span class="sxs-lookup"><span data-stu-id="b3535-172">emptyListMessage: string</span></span>

<span data-ttu-id="b3535-173">既定の空のリスト メッセージを上書きする設定可能なプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b3535-173">Settable property to override default empty list message.</span></span>


### <a name="enablemultiselect"></a><span data-ttu-id="b3535-174">enableMultiSelect</span><span class="sxs-lookup"><span data-stu-id="b3535-174">enableMultiSelect</span></span>

<span data-ttu-id="b3535-175">enableMultiSelect: boolean</span><span class="sxs-lookup"><span data-stu-id="b3535-175">enableMultiSelect: boolean</span></span>




### <a name="generic"></a><span data-ttu-id="b3535-176">generic</span><span class="sxs-lookup"><span data-stu-id="b3535-176">generic</span></span>

<span data-ttu-id="b3535-177">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="b3535-177">generic: boolean (optional)</span></span> 



> <span data-ttu-id="b3535-178">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-178">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="b3535-179">getDataSource</span><span class="sxs-lookup"><span data-stu-id="b3535-179">getDataSource</span></span>

<span data-ttu-id="b3535-180">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="b3535-180">getDataSource: function(): any</span></span>



> <span data-ttu-id="b3535-181">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-181">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="b3535-182">hidden</span><span class="sxs-lookup"><span data-stu-id="b3535-182">hidden</span></span>

<span data-ttu-id="b3535-183">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="b3535-183">hidden: boolean</span></span>

<span data-ttu-id="b3535-184">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="b3535-184">True if the control is hidden.</span></span>

> <span data-ttu-id="b3535-185">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-185">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


### <a name="hideemptylistmessage"></a><span data-ttu-id="b3535-186">hideEmptyListMessage</span><span class="sxs-lookup"><span data-stu-id="b3535-186">hideEmptyListMessage</span></span>

<span data-ttu-id="b3535-187">hideEmptyListMessage: boolean</span><span class="sxs-lookup"><span data-stu-id="b3535-187">hideEmptyListMessage: boolean</span></span>

<span data-ttu-id="b3535-188">True で一覧が空である場合、メッセージが表示されません。</span><span class="sxs-lookup"><span data-stu-id="b3535-188">If true, no message is shown if the list is empty.</span></span>
<span data-ttu-id="b3535-189">このプロパティを設定するには、対応するメタデータ プロパティを configureControl で更新します。</span><span class="sxs-lookup"><span data-stu-id="b3535-189">To set this property, update the corresponding metadata property via configureControl.</span></span>


### <a name="imagefields"></a><span data-ttu-id="b3535-190">imageFields</span><span class="sxs-lookup"><span data-stu-id="b3535-190">imageFields</span></span>

<span data-ttu-id="b3535-191">imageFields: any [ ]</span><span class="sxs-lookup"><span data-stu-id="b3535-191">imageFields: any [ ]</span></span>




### <a name="performingremotesearch"></a><span data-ttu-id="b3535-192">performingRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="b3535-192">performingRemoteSearch</span></span>

<span data-ttu-id="b3535-193">performingRemoteSearch: boolean</span><span class="sxs-lookup"><span data-stu-id="b3535-193">performingRemoteSearch: boolean</span></span>




### <a name="searchquery"></a><span data-ttu-id="b3535-194">searchQuery</span><span class="sxs-lookup"><span data-stu-id="b3535-194">searchQuery</span></span>

<span data-ttu-id="b3535-195">searchQuery: [value: string]: any</span><span class="sxs-lookup"><span data-stu-id="b3535-195">searchQuery: [value: string]: any</span></span>




## <a name="methods"></a><span data-ttu-id="b3535-196">メソッド</span><span class="sxs-lookup"><span data-stu-id="b3535-196">Methods</span></span>

### <a name="allowsnavigation"></a><span data-ttu-id="b3535-197">allowsNavigation</span><span class="sxs-lookup"><span data-stu-id="b3535-197">allowsNavigation</span></span>


<span data-ttu-id="b3535-198">allowsNavigation(): boolean</span><span class="sxs-lookup"><span data-stu-id="b3535-198">allowsNavigation(): boolean</span></span>



#### <a name="returns-boolean"></a><span data-ttu-id="b3535-199">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-199">Returns boolean</span></span>

### <a name="applydesign"></a><span data-ttu-id="b3535-200">applyDesign</span><span class="sxs-lookup"><span data-stu-id="b3535-200">applyDesign</span></span>


<span data-ttu-id="b3535-201">applyDesign(IDesign: [ListDesign](view-model-control-list-ilist-ilistdesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="b3535-201">applyDesign(IDesign: [ListDesign](view-model-control-list-ilist-ilistdesign.md)): void</span></span>

<span data-ttu-id="b3535-202">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="b3535-202">Applies given design to the design on the control.</span></span>
<span data-ttu-id="b3535-203">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="b3535-203">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="b3535-204">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="b3535-204">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="b3535-205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-205">Parameters</span></span>

| <span data-ttu-id="b3535-206">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-206">Name</span></span> | <span data-ttu-id="b3535-207">種類</span><span class="sxs-lookup"><span data-stu-id="b3535-207">Type</span></span> | <span data-ttu-id="b3535-208">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-208">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-209">IDesign</span><span class="sxs-lookup"><span data-stu-id="b3535-209">IDesign</span></span>|[<span data-ttu-id="b3535-210">ListDesign</span><span class="sxs-lookup"><span data-stu-id="b3535-210">ListDesign</span></span>](view-model-control-list-ilist-ilistdesign.md)|<span data-ttu-id="b3535-211">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="b3535-211">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="b3535-212">void を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-212">Returns void</span></span>

### <a name="applysearch"></a><span data-ttu-id="b3535-213">applySearch</span><span class="sxs-lookup"><span data-stu-id="b3535-213">applySearch</span></span>


<span data-ttu-id="b3535-214">applySearch(): void</span><span class="sxs-lookup"><span data-stu-id="b3535-214">applySearch(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="b3535-215">void を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-215">Returns void</span></span>

### <a name="canperformremotesearch"></a><span data-ttu-id="b3535-216">canPerformRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="b3535-216">canPerformRemoteSearch</span></span>


<span data-ttu-id="b3535-217">canPerformRemoteSearch(): boolean</span><span class="sxs-lookup"><span data-stu-id="b3535-217">canPerformRemoteSearch(): boolean</span></span>



#### <a name="returns-boolean"></a><span data-ttu-id="b3535-218">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-218">Returns boolean</span></span>

### <a name="clearsearch"></a><span data-ttu-id="b3535-219">clearSearch</span><span class="sxs-lookup"><span data-stu-id="b3535-219">clearSearch</span></span>


<span data-ttu-id="b3535-220">clearSearch(): void</span><span class="sxs-lookup"><span data-stu-id="b3535-220">clearSearch(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="b3535-221">void を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-221">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="b3535-222">dataContext</span><span class="sxs-lookup"><span data-stu-id="b3535-222">dataContext</span></span>


<span data-ttu-id="b3535-223">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="b3535-223">dataContext(): any</span></span>



> <span data-ttu-id="b3535-224">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-224">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="b3535-225">any を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-225">Returns any</span></span>

### <a name="getcolumnlabel"></a><span data-ttu-id="b3535-226">getColumnLabel</span><span class="sxs-lookup"><span data-stu-id="b3535-226">getColumnLabel</span></span>


<span data-ttu-id="b3535-227">getColumnLabel(id: string): string</span><span class="sxs-lookup"><span data-stu-id="b3535-227">getColumnLabel(id: string): string</span></span>




#### <a name="parameters"></a><span data-ttu-id="b3535-228">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-228">Parameters</span></span>

| <span data-ttu-id="b3535-229">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-229">Name</span></span> | <span data-ttu-id="b3535-230">種類</span><span class="sxs-lookup"><span data-stu-id="b3535-230">Type</span></span> | <span data-ttu-id="b3535-231">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-231">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-232">id</span><span class="sxs-lookup"><span data-stu-id="b3535-232">id</span></span>|<span data-ttu-id="b3535-233">string</span><span class="sxs-lookup"><span data-stu-id="b3535-233">string</span></span>||

#### <a name="returns-string"></a><span data-ttu-id="b3535-234">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-234">Returns string</span></span>

### <a name="getcontrol"></a><span data-ttu-id="b3535-235">getControl</span><span class="sxs-lookup"><span data-stu-id="b3535-235">getControl</span></span>


<span data-ttu-id="b3535-236">getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="b3535-236">getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

<span data-ttu-id="b3535-237">コントロールの名前の場合、コントロール インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-237">Given the name of a control, returns the control instance.</span></span>

> <span data-ttu-id="b3535-238">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControl](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-238">Inherited from [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControl](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol)</span></span>


#### <a name="parameters"></a><span data-ttu-id="b3535-239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-239">Parameters</span></span>

| <span data-ttu-id="b3535-240">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-240">Name</span></span> | <span data-ttu-id="b3535-241">種類</span><span class="sxs-lookup"><span data-stu-id="b3535-241">Type</span></span> | <span data-ttu-id="b3535-242">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-242">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-243">controlName</span><span class="sxs-lookup"><span data-stu-id="b3535-243">controlName</span></span>|<span data-ttu-id="b3535-244">string</span><span class="sxs-lookup"><span data-stu-id="b3535-244">string</span></span>|<span data-ttu-id="b3535-245">コントロール名</span><span class="sxs-lookup"><span data-stu-id="b3535-245">control name</span></span>|

#### <a name="returns-control"></a><span data-ttu-id="b3535-246">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-246">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>



### <a name="getcontrolbyid"></a><span data-ttu-id="b3535-247">getControlById</span><span class="sxs-lookup"><span data-stu-id="b3535-247">getControlById</span></span>


<span data-ttu-id="b3535-248">getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="b3535-248">getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

<span data-ttu-id="b3535-249">コントロールの ID の場合、コントロール インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-249">Given the ID of a control, returns the control instance.</span></span>

> <span data-ttu-id="b3535-250">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControlById](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-250">Inherited from [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControlById](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid)</span></span>


#### <a name="parameters"></a><span data-ttu-id="b3535-251">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-251">Parameters</span></span>

| <span data-ttu-id="b3535-252">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-252">Name</span></span> | <span data-ttu-id="b3535-253">種類</span><span class="sxs-lookup"><span data-stu-id="b3535-253">Type</span></span> | <span data-ttu-id="b3535-254">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-254">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-255">id</span><span class="sxs-lookup"><span data-stu-id="b3535-255">id</span></span>|<span data-ttu-id="b3535-256">string</span><span class="sxs-lookup"><span data-stu-id="b3535-256">string</span></span>|<span data-ttu-id="b3535-257">コントロール ID</span><span class="sxs-lookup"><span data-stu-id="b3535-257">control ID</span></span>|

#### <a name="returns-control"></a><span data-ttu-id="b3535-258">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-258">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>



### <a name="getcontrolmetadata"></a><span data-ttu-id="b3535-259">getControlMetadata</span><span class="sxs-lookup"><span data-stu-id="b3535-259">getControlMetadata</span></span>


<span data-ttu-id="b3535-260">getControlMetadata(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="b3535-260">getControlMetadata(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>




#### <a name="parameters"></a><span data-ttu-id="b3535-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-261">Parameters</span></span>

| <span data-ttu-id="b3535-262">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-262">Name</span></span> | <span data-ttu-id="b3535-263">種類</span><span class="sxs-lookup"><span data-stu-id="b3535-263">Type</span></span> | <span data-ttu-id="b3535-264">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-264">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-265">controlName</span><span class="sxs-lookup"><span data-stu-id="b3535-265">controlName</span></span>|<span data-ttu-id="b3535-266">string</span><span class="sxs-lookup"><span data-stu-id="b3535-266">string</span></span>||

#### <a name="returns-control"></a><span data-ttu-id="b3535-267">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-267">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

### <a name="getcontrolmetadatabyid"></a><span data-ttu-id="b3535-268">getControlMetadataById</span><span class="sxs-lookup"><span data-stu-id="b3535-268">getControlMetadataById</span></span>


<span data-ttu-id="b3535-269">getControlMetadataById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="b3535-269">getControlMetadataById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>




#### <a name="parameters"></a><span data-ttu-id="b3535-270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-270">Parameters</span></span>

| <span data-ttu-id="b3535-271">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-271">Name</span></span> | <span data-ttu-id="b3535-272">種類</span><span class="sxs-lookup"><span data-stu-id="b3535-272">Type</span></span> | <span data-ttu-id="b3535-273">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-273">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-274">id</span><span class="sxs-lookup"><span data-stu-id="b3535-274">id</span></span>|<span data-ttu-id="b3535-275">string</span><span class="sxs-lookup"><span data-stu-id="b3535-275">string</span></span>||

#### <a name="returns-control"></a><span data-ttu-id="b3535-276">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-276">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

### <a name="getdata"></a><span data-ttu-id="b3535-277">getData</span><span class="sxs-lookup"><span data-stu-id="b3535-277">getData</span></span>


<span data-ttu-id="b3535-278">getData(): any [ ]</span><span class="sxs-lookup"><span data-stu-id="b3535-278">getData(): any [ ]</span></span>



#### <a name="returns-any--"></a><span data-ttu-id="b3535-279">any [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-279">Returns any [ ]</span></span>

### <a name="getdesign"></a><span data-ttu-id="b3535-280">getDesign</span><span class="sxs-lookup"><span data-stu-id="b3535-280">getDesign</span></span>


<span data-ttu-id="b3535-281">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="b3535-281">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="b3535-282">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-282">Returns the design object of this control.</span></span>

> <span data-ttu-id="b3535-283">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-283">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-design"></a><span data-ttu-id="b3535-284">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-284">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="getlistdata"></a><span data-ttu-id="b3535-285">getListData</span><span class="sxs-lookup"><span data-stu-id="b3535-285">getListData</span></span>


<span data-ttu-id="b3535-286">getListData(): any</span><span class="sxs-lookup"><span data-stu-id="b3535-286">getListData(): any</span></span>



#### <a name="returns-any"></a><span data-ttu-id="b3535-287">any を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-287">Returns any</span></span>

### <a name="getrenderedrows"></a><span data-ttu-id="b3535-288">getRenderedRows</span><span class="sxs-lookup"><span data-stu-id="b3535-288">getRenderedRows</span></span>


<span data-ttu-id="b3535-289">getRenderedRows(): [Row](view-model-control-list-ilist-irow.md) [ ]</span><span class="sxs-lookup"><span data-stu-id="b3535-289">getRenderedRows(): [Row](view-model-control-list-ilist-irow.md) [ ]</span></span>



#### <a name="returns-row--"></a><span data-ttu-id="b3535-290">[Row](view-model-control-list-ilist-irow.md) [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-290">Returns [Row](view-model-control-list-ilist-irow.md) [ ]</span></span>

### <a name="getrownavigation"></a><span data-ttu-id="b3535-291">getRowNavigation</span><span class="sxs-lookup"><span data-stu-id="b3535-291">getRowNavigation</span></span>


<span data-ttu-id="b3535-292">getRowNavigation(row: [Row](view-model-control-list-ilist-irow.md)): Promise &lt;any&gt; &#124; any</span><span class="sxs-lookup"><span data-stu-id="b3535-292">getRowNavigation(row: [Row](view-model-control-list-ilist-irow.md)): Promise &lt;any&gt; &#124; any</span></span>




#### <a name="parameters"></a><span data-ttu-id="b3535-293">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-293">Parameters</span></span>

| <span data-ttu-id="b3535-294">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-294">Name</span></span> | <span data-ttu-id="b3535-295">型</span><span class="sxs-lookup"><span data-stu-id="b3535-295">Type</span></span> | <span data-ttu-id="b3535-296">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-296">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-297"> 行 </span><span class="sxs-lookup"><span data-stu-id="b3535-297">row</span></span>|[<span data-ttu-id="b3535-298">Row</span><span class="sxs-lookup"><span data-stu-id="b3535-298">Row</span></span>](view-model-control-list-ilist-irow.md)||

#### <a name="returns-promise-ltanygt-124-any"></a><span data-ttu-id="b3535-299">Promise &lt;any&gt; &#124; any を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-299">Returns Promise &lt;any&gt; &#124; any</span></span>

### <a name="getrowselectioncount"></a><span data-ttu-id="b3535-300">getRowSelectionCount</span><span class="sxs-lookup"><span data-stu-id="b3535-300">getRowSelectionCount</span></span>


<span data-ttu-id="b3535-301">getRowSelectionCount(): number</span><span class="sxs-lookup"><span data-stu-id="b3535-301">getRowSelectionCount(): number</span></span>



#### <a name="returns-number"></a><span data-ttu-id="b3535-302">number を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-302">Returns number</span></span>

### <a name="getrowselections"></a><span data-ttu-id="b3535-303">getRowSelections</span><span class="sxs-lookup"><span data-stu-id="b3535-303">getRowSelections</span></span>


<span data-ttu-id="b3535-304">getRowSelections(): string [ ]</span><span class="sxs-lookup"><span data-stu-id="b3535-304">getRowSelections(): string [ ]</span></span>



#### <a name="returns-string--"></a><span data-ttu-id="b3535-305">string [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-305">Returns string [ ]</span></span>

### <a name="getrowtracking"></a><span data-ttu-id="b3535-306">getRowTracking</span><span class="sxs-lookup"><span data-stu-id="b3535-306">getRowTracking</span></span>


<span data-ttu-id="b3535-307">getRowTracking(row: any, index: string): string</span><span class="sxs-lookup"><span data-stu-id="b3535-307">getRowTracking(row: any, index: string): string</span></span>




#### <a name="parameters"></a><span data-ttu-id="b3535-308">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-308">Parameters</span></span>

| <span data-ttu-id="b3535-309">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-309">Name</span></span> | <span data-ttu-id="b3535-310">種類</span><span class="sxs-lookup"><span data-stu-id="b3535-310">Type</span></span> | <span data-ttu-id="b3535-311">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-311">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-312">行</span><span class="sxs-lookup"><span data-stu-id="b3535-312">row</span></span>|<span data-ttu-id="b3535-313">any</span><span class="sxs-lookup"><span data-stu-id="b3535-313">any</span></span>||
| <span data-ttu-id="b3535-314">指数</span><span class="sxs-lookup"><span data-stu-id="b3535-314">index</span></span>|<span data-ttu-id="b3535-315">string</span><span class="sxs-lookup"><span data-stu-id="b3535-315">string</span></span>||

#### <a name="returns-string"></a><span data-ttu-id="b3535-316">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-316">Returns string</span></span>

### <a name="getsearchcolumn"></a><span data-ttu-id="b3535-317">getSearchColumn</span><span class="sxs-lookup"><span data-stu-id="b3535-317">getSearchColumn</span></span>


<span data-ttu-id="b3535-318">getSearchColumn(): string</span><span class="sxs-lookup"><span data-stu-id="b3535-318">getSearchColumn(): string</span></span>



#### <a name="returns-string"></a><span data-ttu-id="b3535-319">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-319">Returns string</span></span>

### <a name="getsearchcolumnlabel"></a><span data-ttu-id="b3535-320">getSearchColumnLabel</span><span class="sxs-lookup"><span data-stu-id="b3535-320">getSearchColumnLabel</span></span>


<span data-ttu-id="b3535-321">getSearchColumnLabel(): string</span><span class="sxs-lookup"><span data-stu-id="b3535-321">getSearchColumnLabel(): string</span></span>



#### <a name="returns-string"></a><span data-ttu-id="b3535-322">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-322">Returns string</span></span>

### <a name="getsearchablecolumns"></a><span data-ttu-id="b3535-323">getSearchableColumns</span><span class="sxs-lookup"><span data-stu-id="b3535-323">getSearchableColumns</span></span>


<span data-ttu-id="b3535-324">getSearchableColumns(): any [ ]</span><span class="sxs-lookup"><span data-stu-id="b3535-324">getSearchableColumns(): any [ ]</span></span>



#### <a name="returns-any--"></a><span data-ttu-id="b3535-325">any [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-325">Returns any [ ]</span></span>

### <a name="hidesearchbar"></a><span data-ttu-id="b3535-326">hideSearchBar</span><span class="sxs-lookup"><span data-stu-id="b3535-326">hideSearchBar</span></span>


<span data-ttu-id="b3535-327">hideSearchBar(): boolean</span><span class="sxs-lookup"><span data-stu-id="b3535-327">hideSearchBar(): boolean</span></span>



#### <a name="returns-boolean"></a><span data-ttu-id="b3535-328">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-328">Returns boolean</span></span>

### <a name="iseditable"></a><span data-ttu-id="b3535-329">isEditable</span><span class="sxs-lookup"><span data-stu-id="b3535-329">isEditable</span></span>


<span data-ttu-id="b3535-330">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="b3535-330">isEditable(): boolean</span></span>

<span data-ttu-id="b3535-331">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b3535-331">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="b3535-332">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-332">Returns false when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="b3535-333">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-333">Returns true when both the control and it's parent are editable.</span></span>
<span data-ttu-id="b3535-334">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-334">Returns true when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="b3535-335">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-335">Returns undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="b3535-336">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-336">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="b3535-337">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-337">Returns boolean</span></span>



### <a name="loadmetadata"></a><span data-ttu-id="b3535-338">loadMetaData</span><span class="sxs-lookup"><span data-stu-id="b3535-338">loadMetaData</span></span>


<span data-ttu-id="b3535-339">loadMetaData(): void</span><span class="sxs-lookup"><span data-stu-id="b3535-339">loadMetaData(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="b3535-340">void を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-340">Returns void</span></span>

### <a name="loadmore"></a><span data-ttu-id="b3535-341">loadMore</span><span class="sxs-lookup"><span data-stu-id="b3535-341">loadMore</span></span>


<span data-ttu-id="b3535-342">loadMore(): void</span><span class="sxs-lookup"><span data-stu-id="b3535-342">loadMore(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="b3535-343">void を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-343">Returns void</span></span>

### <a name="metadata"></a><span data-ttu-id="b3535-344">metadata</span><span class="sxs-lookup"><span data-stu-id="b3535-344">metadata</span></span>


<span data-ttu-id="b3535-345">metadata(): [ListMetadata](view-model-control-list-ilist-ilistmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="b3535-345">metadata(): [ListMetadata](view-model-control-list-ilist-ilistmetadata.md)</span></span>

<span data-ttu-id="b3535-346">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-346">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="b3535-347">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[metadata](view-model-control-container-icontainercontrol-icontainercontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="b3535-347">Overrides [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[metadata](view-model-control-container-icontainercontrol-icontainercontrol.md#metadata)</span></span>

#### <a name="returns-listmetadata"></a><span data-ttu-id="b3535-348">[ListMetadata](view-model-control-list-ilist-ilistmetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-348">Returns [ListMetadata](view-model-control-list-ilist-ilistmetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="b3535-349">parent</span><span class="sxs-lookup"><span data-stu-id="b3535-349">parent</span></span>


<span data-ttu-id="b3535-350">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="b3535-350">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="b3535-351">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-351">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="b3535-352">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-352">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-control-124-page"></a><span data-ttu-id="b3535-353">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-353">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="performremotesearch"></a><span data-ttu-id="b3535-354">performRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="b3535-354">performRemoteSearch</span></span>


<span data-ttu-id="b3535-355">performRemoteSearch(): void</span><span class="sxs-lookup"><span data-stu-id="b3535-355">performRemoteSearch(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="b3535-356">void を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-356">Returns void</span></span>

### <a name="root"></a><span data-ttu-id="b3535-357">root</span><span class="sxs-lookup"><span data-stu-id="b3535-357">root</span></span>


<span data-ttu-id="b3535-358">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="b3535-358">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="b3535-359">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="b3535-359">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="b3535-360">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="b3535-360">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-page"></a><span data-ttu-id="b3535-361">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-361">Returns [Page](view-model-ipage-ipage.md)</span></span>



### <a name="selectsearchcolumn"></a><span data-ttu-id="b3535-362">selectSearchColumn</span><span class="sxs-lookup"><span data-stu-id="b3535-362">selectSearchColumn</span></span>


<span data-ttu-id="b3535-363">selectSearchColumn(column: string): void</span><span class="sxs-lookup"><span data-stu-id="b3535-363">selectSearchColumn(column: string): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="b3535-364">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-364">Parameters</span></span>

| <span data-ttu-id="b3535-365">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-365">Name</span></span> | <span data-ttu-id="b3535-366">種類</span><span class="sxs-lookup"><span data-stu-id="b3535-366">Type</span></span> | <span data-ttu-id="b3535-367">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-367">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-368">column</span><span class="sxs-lookup"><span data-stu-id="b3535-368">column</span></span>|<span data-ttu-id="b3535-369">string</span><span class="sxs-lookup"><span data-stu-id="b3535-369">string</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="b3535-370">void を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-370">Returns void</span></span>

### <a name="setrowsections"></a><span data-ttu-id="b3535-371">setRowSections</span><span class="sxs-lookup"><span data-stu-id="b3535-371">setRowSections</span></span>


<span data-ttu-id="b3535-372">setRowSections(selections: string [ ]): void</span><span class="sxs-lookup"><span data-stu-id="b3535-372">setRowSections(selections: string [ ]): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="b3535-373">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3535-373">Parameters</span></span>

| <span data-ttu-id="b3535-374">氏名</span><span class="sxs-lookup"><span data-stu-id="b3535-374">Name</span></span> | <span data-ttu-id="b3535-375">種類</span><span class="sxs-lookup"><span data-stu-id="b3535-375">Type</span></span> | <span data-ttu-id="b3535-376">説明</span><span class="sxs-lookup"><span data-stu-id="b3535-376">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="b3535-377">選択内容</span><span class="sxs-lookup"><span data-stu-id="b3535-377">selections</span></span>|<span data-ttu-id="b3535-378">string [ ]</span><span class="sxs-lookup"><span data-stu-id="b3535-378">string [ ]</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="b3535-379">void を返します</span><span class="sxs-lookup"><span data-stu-id="b3535-379">Returns void</span></span>

## <a name="events"></a><span data-ttu-id="b3535-380">イベント</span><span class="sxs-lookup"><span data-stu-id="b3535-380">Events</span></span>

### <a name="onrowcreate"></a><span data-ttu-id="b3535-381">onRowCreate</span><span class="sxs-lookup"><span data-stu-id="b3535-381">onRowCreate</span></span>

<span data-ttu-id="b3535-382">onRowCreate: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="b3535-382">onRowCreate: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;</span></span>




### <a name="onrowselect"></a><span data-ttu-id="b3535-383">onRowSelect</span><span class="sxs-lookup"><span data-stu-id="b3535-383">onRowSelect</span></span>

<span data-ttu-id="b3535-384">onRowSelect: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="b3535-384">onRowSelect: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;</span></span>




