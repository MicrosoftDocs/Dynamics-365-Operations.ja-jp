---
title: F クラス (FormObject から FormRealControl)
description: FormObject から FormRealControl までのクラスの API 参照。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 63603
ms.assetid: 170eb939-154e-488e-84a8-f67dd9d9a8f6
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c02845b6c05663e35e1c7860938f163cb0ff9e3c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191617"
---
# <a name="f-classes-formobject-to-formrealcontrol"></a><span data-ttu-id="622ca-103">F クラス (FormObject から FormRealControl)</span><span class="sxs-lookup"><span data-stu-id="622ca-103">F classes (FormObject to FormRealControl)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="622ca-104">FormObject から FormRealControl までのクラスの API 参照。</span><span class="sxs-lookup"><span data-stu-id="622ca-104">API reference for classes from FormObject to FormRealControl.</span></span>

<a name="class-formobject"></a><span data-ttu-id="622ca-105">クラス FormObject</span><span class="sxs-lookup"><span data-stu-id="622ca-105">Class FormObject</span></span>
----------------

    class FormObject extends Object

### <a name="remarks"></a><span data-ttu-id="622ca-106">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-107">例</span><span class="sxs-lookup"><span data-stu-id="622ca-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-108">Methods</span></span>

| <span data-ttu-id="622ca-109">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-109">Method</span></span>                                        | <span data-ttu-id="622ca-110">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-110">Description</span></span>                             |
|-----------------------------------------------|-----------------------------------------|
| <span data-ttu-id="622ca-111">public boolean getAllowEdit(\[int rowIndex\])</span><span class="sxs-lookup"><span data-stu-id="622ca-111">public boolean getAllowEdit(\[int rowIndex\])</span></span> |                                         |
| <span data-ttu-id="622ca-112">public AnyType getValue(\[int rowIndex\])</span><span class="sxs-lookup"><span data-stu-id="622ca-112">public AnyType getValue(\[int rowIndex\])</span></span>     |                                         |
| <span data-ttu-id="622ca-113">public boolean getVisible()</span><span class="sxs-lookup"><span data-stu-id="622ca-113">public boolean getVisible()</span></span>                   |                                         |
| <span data-ttu-id="622ca-114">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="622ca-114">public str helpField()</span></span>                        | <span data-ttu-id="622ca-115">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-115">Returns the Help text for the control.</span></span>  |
| <span data-ttu-id="622ca-116">public str labelText()</span><span class="sxs-lookup"><span data-stu-id="622ca-116">public str labelText()</span></span>                        | <span data-ttu-id="622ca-117">コントロールのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-117">Returns the label text for the control.</span></span> |
| <span data-ttu-id="622ca-118">public boolean setValue(AnyType value)</span><span class="sxs-lookup"><span data-stu-id="622ca-118">public boolean setValue(AnyType value)</span></span>        |                                         |
| <span data-ttu-id="622ca-119">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="622ca-119">public str toolTip()</span></span>                          |                                         |
| <span data-ttu-id="622ca-120">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="622ca-120">public boolean validate()</span></span>                     |                                         |
| <span data-ttu-id="622ca-121">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="622ca-121">public void jumpRef()</span></span>                         |                                         |
| <span data-ttu-id="622ca-122">public void modified()</span><span class="sxs-lookup"><span data-stu-id="622ca-122">public void modified()</span></span>                        |                                         |
| <span data-ttu-id="622ca-123">public void restore()</span><span class="sxs-lookup"><span data-stu-id="622ca-123">public void restore()</span></span>                         |                                         |
| <span data-ttu-id="622ca-124">public void find()</span><span class="sxs-lookup"><span data-stu-id="622ca-124">public void find()</span></span>                            |                                         |
| <span data-ttu-id="622ca-125">public void context()</span><span class="sxs-lookup"><span data-stu-id="622ca-125">public void context()</span></span>                         |                                         |

### <a name="method-getallowedit"></a><span data-ttu-id="622ca-126">メソッド getAllowEdit</span><span class="sxs-lookup"><span data-stu-id="622ca-126">Method getAllowEdit</span></span>

    public boolean getAllowEdit([int rowIndex])

#### <a name="parameters"></a><span data-ttu-id="622ca-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-127">Parameters</span></span>

<span data-ttu-id="622ca-128">rowIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-128">rowIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-129">Return Value</span></span>

### <a name="method-getvalue"></a><span data-ttu-id="622ca-130">メソッド getValue</span><span class="sxs-lookup"><span data-stu-id="622ca-130">Method getValue</span></span>

    public AnyType getValue([int rowIndex])

#### <a name="parameters"></a><span data-ttu-id="622ca-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-131">Parameters</span></span>

<span data-ttu-id="622ca-132">rowIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-132">rowIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-133">Return Value</span></span>

### <a name="method-getvisible"></a><span data-ttu-id="622ca-134">メソッド getVisible</span><span class="sxs-lookup"><span data-stu-id="622ca-134">Method getVisible</span></span>

    public boolean getVisible()

#### <a name="return-value"></a><span data-ttu-id="622ca-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-135">Return Value</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="622ca-136">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="622ca-136">Method helpField</span></span>

<span data-ttu-id="622ca-137">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-137">Returns the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="622ca-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-138">Return Value</span></span>

<span data-ttu-id="622ca-139">コントロールのヘルプ テキスト。ヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-139">The Help text for the control; an empty string if there is no Help text.</span></span>

#### <a name="examples"></a><span data-ttu-id="622ca-140">例</span><span class="sxs-lookup"><span data-stu-id="622ca-140">Examples</span></span>

<span data-ttu-id="622ca-141">次の例は、helpField メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="622ca-141">The following example shows how to use the helpField method.</span></span>

    str strHelp;
    strHelp = this.helpField();

### <a name="method-labeltext"></a><span data-ttu-id="622ca-142">メソッド labelText</span><span class="sxs-lookup"><span data-stu-id="622ca-142">Method labelText</span></span>

<span data-ttu-id="622ca-143">コントロールのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-143">Returns the label text for the control.</span></span>

    public str labelText()

#### <a name="return-value"></a><span data-ttu-id="622ca-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-144">Return Value</span></span>

<span data-ttu-id="622ca-145">コントロールのラベル テキスト。コントロールにラベル テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-145">The label text for the control; an empty string if there is no label text for the control.</span></span>

### <a name="method-setvalue"></a><span data-ttu-id="622ca-146">メソッド setValue</span><span class="sxs-lookup"><span data-stu-id="622ca-146">Method setValue</span></span>

    public boolean setValue(AnyType value)

#### <a name="parameters"></a><span data-ttu-id="622ca-147">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-147">Parameters</span></span>

<span data-ttu-id="622ca-148">値</span><span class="sxs-lookup"><span data-stu-id="622ca-148">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-149">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-149">Return Value</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="622ca-150">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="622ca-150">Method toolTip</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="622ca-151">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-151">Return Value</span></span>

### <a name="method-validate"></a><span data-ttu-id="622ca-152">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="622ca-152">Method validate</span></span>

    public boolean validate()

#### <a name="return-value"></a><span data-ttu-id="622ca-153">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-153">Return Value</span></span>

### <a name="method-jumpref"></a><span data-ttu-id="622ca-154">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="622ca-154">Method jumpRef</span></span>

    public void jumpRef()

### <a name="method-modified"></a><span data-ttu-id="622ca-155">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="622ca-155">Method modified</span></span>

    public void modified()

### <a name="method-restore"></a><span data-ttu-id="622ca-156">メソッド restore</span><span class="sxs-lookup"><span data-stu-id="622ca-156">Method restore</span></span>

    public void restore()

### <a name="method-find"></a><span data-ttu-id="622ca-157">メソッド find</span><span class="sxs-lookup"><span data-stu-id="622ca-157">Method find</span></span>

    public void find()

### <a name="method-context"></a><span data-ttu-id="622ca-158">メソッド context</span><span class="sxs-lookup"><span data-stu-id="622ca-158">Method context</span></span>

    public void context()

## <a name="class-formobjectset"></a><span data-ttu-id="622ca-159">クラス FormObjectSet</span><span class="sxs-lookup"><span data-stu-id="622ca-159">Class FormObjectSet</span></span>
    class FormObjectSet extends Object

<span data-ttu-id="622ca-160">FormObjectSet クラスは、フォームのデータ ソースを操作するための基本機能を提供する基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="622ca-160">The FormObjectSet class is a base class that provides basic functionality for working with the data sources for a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="622ca-161">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-161">Remarks</span></span>

<span data-ttu-id="622ca-162">FormObjectSet クラスのメソッドのほとんどは空です。</span><span class="sxs-lookup"><span data-stu-id="622ca-162">Most of the methods on the FormObjectSet class are empty.</span></span> <span data-ttu-id="622ca-163">これらは、FormDataSource 派生クラスで実装されています。</span><span class="sxs-lookup"><span data-stu-id="622ca-163">They are implemented in the FormDataSource derived class.</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-164">例</span><span class="sxs-lookup"><span data-stu-id="622ca-164">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-165">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-165">Methods</span></span>

| <span data-ttu-id="622ca-166">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-166">Method</span></span>                                                             | <span data-ttu-id="622ca-167">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-167">Description</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-168">public int active()</span><span class="sxs-lookup"><span data-stu-id="622ca-168">public int active()</span></span>                                                | <span data-ttu-id="622ca-169">FormObjectSet クラスでの機能はありませんが、ユーザーが新しいレコードに移動するときに、結合されたデータ ソースからデータを取得する FormDataSource.active メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-169">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.active method, which retrieves data from joined data sources when a user navigates to a new record.</span></span>                                 |
| <span data-ttu-id="622ca-170">public Common cursor()</span><span class="sxs-lookup"><span data-stu-id="622ca-170">public Common cursor()</span></span>                                             | <span data-ttu-id="622ca-171">FormObjectSet クラスでの機能はありませんが、データソースによって参照されるテーブル内の現在アクティブなレコードを返す FormDataSource.cursor メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-171">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.cursor method, which returns the currently active record in the table that is referenced by the data source.</span></span>                        |
| <span data-ttu-id="622ca-172">public boolean findRecord(Common record)</span><span class="sxs-lookup"><span data-stu-id="622ca-172">public boolean findRecord(Common record)</span></span>                           | <span data-ttu-id="622ca-173">FormObjectSet クラスでの機能はありませんが、現在データソースで指定されるレコードを検索して現在のレコードにする FormDataSource.findRecord メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-173">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.findRecord method, which finds a specified record in the data source and makes it the current one.</span></span>                                  |
| <span data-ttu-id="622ca-174">public boolean positionToRecord(Common record)</span><span class="sxs-lookup"><span data-stu-id="622ca-174">public boolean positionToRecord(Common record)</span></span>                     |                                                                                                                                                                                                                             |
| <span data-ttu-id="622ca-175">public int first()</span><span class="sxs-lookup"><span data-stu-id="622ca-175">public int first()</span></span>                                                 | <span data-ttu-id="622ca-176">データ ソースの最初のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-176">Moves focus to the first record in a data source.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="622ca-177">public xFormRun formRun()</span><span class="sxs-lookup"><span data-stu-id="622ca-177">public xFormRun formRun()</span></span>                                          |                                                                                                                                                                                                                             |
| <span data-ttu-id="622ca-178">public int getPosition()</span><span class="sxs-lookup"><span data-stu-id="622ca-178">public int getPosition()</span></span>                                           |                                                                                                                                                                                                                             |
| <span data-ttu-id="622ca-179">public int id()</span><span class="sxs-lookup"><span data-stu-id="622ca-179">public int id()</span></span>                                                    |                                                                                                                                                                                                                             |
| <span data-ttu-id="622ca-180">public int last()</span><span class="sxs-lookup"><span data-stu-id="622ca-180">public int last()</span></span>                                                  | <span data-ttu-id="622ca-181">データ ソースの最後のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-181">Moves focus to the last record in the data source.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="622ca-182">public boolean leaveRecord(\[boolean forceUpdate\])</span><span class="sxs-lookup"><span data-stu-id="622ca-182">public boolean leaveRecord(\[boolean forceUpdate\])</span></span>                | <span data-ttu-id="622ca-183">FormObjectSet クラスでの機能はありませんが、ユーザーが別のレコードに移動するときに通知を提供する FormDataSource.leaveRecord メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-183">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.leaveRecord method, which provides a notification when the user moves to another record.</span></span>                                            |
| <span data-ttu-id="622ca-184">public FormObjectSet masterObjectSet()</span><span class="sxs-lookup"><span data-stu-id="622ca-184">public FormObjectSet masterObjectSet()</span></span>                             | <span data-ttu-id="622ca-185">現在のオブジェクト セットのマスター オブジェクト セットを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-185">Retrieves the master object set for the current object set.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="622ca-186">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-186">public str name(\[str value\])</span></span>                                     | <span data-ttu-id="622ca-187">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-187">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                                                                     |
| <span data-ttu-id="622ca-188">public int next()</span><span class="sxs-lookup"><span data-stu-id="622ca-188">public int next()</span></span>                                                  | <span data-ttu-id="622ca-189">データ ソースの次のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-189">Moves focus to the next record in the data source.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="622ca-190">public int nextPage(int pageSize)</span><span class="sxs-lookup"><span data-stu-id="622ca-190">public int nextPage(int pageSize)</span></span>                                  | <span data-ttu-id="622ca-191">データ ソースで指定した数のレコード (位置変更) を進めます。</span><span class="sxs-lookup"><span data-stu-id="622ca-191">Moves a specified number of records forward in the data source.</span></span>                                                                                                                                                             |
| <span data-ttu-id="622ca-192">public FormDataObject object(int objectId)</span><span class="sxs-lookup"><span data-stu-id="622ca-192">public FormDataObject object(int objectId)</span></span>                         |                                                                                                                                                                                                                             |
| <span data-ttu-id="622ca-193">public int prev()</span><span class="sxs-lookup"><span data-stu-id="622ca-193">public int prev()</span></span>                                                  | <span data-ttu-id="622ca-194">データ ソースの前のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-194">Moves focus to the previous record in the data source.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="622ca-195">public int prevPage(int pageSize)</span><span class="sxs-lookup"><span data-stu-id="622ca-195">public int prevPage(int pageSize)</span></span>                                  | <span data-ttu-id="622ca-196">データ ソースで指定した数のレコード (位置変更) を戻します。</span><span class="sxs-lookup"><span data-stu-id="622ca-196">Moves a specified number of records back (a positional change) in the data source.</span></span>                                                                                                                                          |
| <span data-ttu-id="622ca-197">public boolean setPosition(int position)</span><span class="sxs-lookup"><span data-stu-id="622ca-197">public boolean setPosition(int position)</span></span>                           |                                                                                                                                                                                                                             |
| <span data-ttu-id="622ca-198">public boolean validateDelete()</span><span class="sxs-lookup"><span data-stu-id="622ca-198">public boolean validateDelete()</span></span>                                    | <span data-ttu-id="622ca-199">FormObjectSet クラスでの機能はありませんが、データソースからのレコードの削除をユーザーが確認するよう求める FormDataSource.validateDelete メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-199">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.validateDelete method, which prompts the user to confirm the deletion of a record from the data source.</span></span>                             |
| <span data-ttu-id="622ca-200">public boolean validateWrite()</span><span class="sxs-lookup"><span data-stu-id="622ca-200">public boolean validateWrite()</span></span>                                     | <span data-ttu-id="622ca-201">FormObjectSet クラスでの機能はありませんが、データが有効であるかおよび書き込まれる準備ができているかどうかを判断する FormDataSource.validateWrite メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-201">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.validateWrite method, which determines whether data is valid and ready to be written.</span></span>                                               |
| <span data-ttu-id="622ca-202">public void refresh()</span><span class="sxs-lookup"><span data-stu-id="622ca-202">public void refresh()</span></span>                                              | <span data-ttu-id="622ca-203">FormObjectSet クラスでの機能はありませんが、データ ソースにすべてのレコードの表示を更新する FormDataSource.refresh メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-203">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.refresh method, which updates the view of all records in the data source.</span></span>                                                           |
| <span data-ttu-id="622ca-204">public void addNotifyHandler(FormObjectSetNotify notifyHandler)</span><span class="sxs-lookup"><span data-stu-id="622ca-204">public void addNotifyHandler(FormObjectSetNotify notifyHandler)</span></span>    |                                                                                                                                                                                                                             |
| <span data-ttu-id="622ca-205">public void reread()</span><span class="sxs-lookup"><span data-stu-id="622ca-205">public void reread()</span></span>                                               | <span data-ttu-id="622ca-206">FormObjectSet クラスでの機能はありませんが、データベースから現在のレコードを再読み込みする FormDataSource.reread メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-206">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.reread method, which rereads the current record from the database.</span></span>                                                                  |
| <span data-ttu-id="622ca-207">public void init()</span><span class="sxs-lookup"><span data-stu-id="622ca-207">public void init()</span></span>                                                 | <span data-ttu-id="622ca-208">FormObjectSet クラスでの機能はありませんが、データ ソース プロパティに基づいてデータ ソース クエリを作成する FormDataSource.init メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-208">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.init method, which creates a data source query, based on the data source properties.</span></span>                                                |
| <span data-ttu-id="622ca-209">public void deleteMarked()</span><span class="sxs-lookup"><span data-stu-id="622ca-209">public void deleteMarked()</span></span>                                         | <span data-ttu-id="622ca-210">FormObjectSet クラスでの機能はありませんが、データソースからマークされたレコードをすべて削除する FormDataSource.deleteMarked メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-210">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.deleteMarked method, which deletes all marked records from a data source.</span></span>                                                           |
| <span data-ttu-id="622ca-211">public void delete()</span><span class="sxs-lookup"><span data-stu-id="622ca-211">public void delete()</span></span>                                               | <span data-ttu-id="622ca-212">FormObjectSet クラスでの機能はありませんが、現在データソースから選択されるレコードを削除する FormDataSource.delete メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-212">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.delete method, which deletes the record that is currently selected from the data source.</span></span>                                            |
| <span data-ttu-id="622ca-213">public void write()</span><span class="sxs-lookup"><span data-stu-id="622ca-213">public void write()</span></span>                                                | <span data-ttu-id="622ca-214">FormObjectSet クラスでの機能はありませんが、データベースの書き込み操作を管理する FormDataSource.write メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-214">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.write method, which manages the database write operation.</span></span>                                                                           |
| <span data-ttu-id="622ca-215">public void create(\[boolean append\])</span><span class="sxs-lookup"><span data-stu-id="622ca-215">public void create(\[boolean append\])</span></span>                             | <span data-ttu-id="622ca-216">FormObjectSet クラスでの機能はありませんが、データ ソースに新しいレコードを作成する FormDataSource.create メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-216">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.create method, which creates a new record in the data source.</span></span>                                                                       |
| <span data-ttu-id="622ca-217">public void removeNotifyHandler(FormObjectSetNotify notifyHandler)</span><span class="sxs-lookup"><span data-stu-id="622ca-217">public void removeNotifyHandler(FormObjectSetNotify notifyHandler)</span></span> |                                                                                                                                                                                                                             |
| <span data-ttu-id="622ca-218">public void prompt()</span><span class="sxs-lookup"><span data-stu-id="622ca-218">public void prompt()</span></span>                                               | <span data-ttu-id="622ca-219">FormObjectSet クラスでの機能はありませんが、クエリの範囲を制限するために使用される SysQueryForm クラスを有効にするFormDataSource.prompt メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-219">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.prompt method, which activates the SysQueryForm class that is used to limit a query range.</span></span>                                          |
| <span data-ttu-id="622ca-220">public void research(\[boolean retainPosition\])</span><span class="sxs-lookup"><span data-stu-id="622ca-220">public void research(\[boolean retainPosition\])</span></span>                   | <span data-ttu-id="622ca-221">FormObjectSet クラスでの機能はありませんが、現在フォームに適用されているフィルターおよびソートで定義されているデータベースの検索を更新する FormDataSource.research メソッドによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-221">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.research method, which updates the database search that is defined by the filters and sorts that are currently applied to the form.</span></span> |
| <span data-ttu-id="622ca-222">public void refreshEx(\[AnyType pos\])</span><span class="sxs-lookup"><span data-stu-id="622ca-222">public void refreshEx(\[AnyType pos\])</span></span>                             | <span data-ttu-id="622ca-223">FormObjectSet クラスでの機能はありませんが、特定のレコードの表示を更新する FormDataSource.refreshEx メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-223">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.refreshEx method, which updates the view of the specified record.</span></span>                                                                   |
| <span data-ttu-id="622ca-224">public void initValue()</span><span class="sxs-lookup"><span data-stu-id="622ca-224">public void initValue()</span></span>                                            | <span data-ttu-id="622ca-225">FormObjectSet クラスでの機能はありませんが、新しいレコードでフィールド値を初期化する FormDataSource.initValue メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-225">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.initValue method, which initializes field values in a new record.</span></span>                                                                   |
| <span data-ttu-id="622ca-226">public void removeFilter()</span><span class="sxs-lookup"><span data-stu-id="622ca-226">public void removeFilter()</span></span>                                         | <span data-ttu-id="622ca-227">FormObjectSet クラスでの機能はありませんが、データ ソースのクエリをリセットする FormDataSource.removeFilter メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-227">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.removeFilter method, which resets the query for the data source.</span></span>                                                                    |

### <a name="method-active"></a><span data-ttu-id="622ca-228">メソッド active</span><span class="sxs-lookup"><span data-stu-id="622ca-228">Method active</span></span>

<span data-ttu-id="622ca-229">FormObjectSet クラスでの機能はありませんが、ユーザーが新しいレコードに移動するときに、結合されたデータ ソースからデータを取得する FormDataSource.active メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-229">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.active method, which retrieves data from joined data sources when a user navigates to a new record.</span></span>

    public int active()

#### <a name="return-value"></a><span data-ttu-id="622ca-230">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-230">Return Value</span></span>

<span data-ttu-id="622ca-231">常に 1 を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-231">Always returns 1.</span></span>

### <a name="method-cursor"></a><span data-ttu-id="622ca-232">メソッド cursor</span><span class="sxs-lookup"><span data-stu-id="622ca-232">Method cursor</span></span>

<span data-ttu-id="622ca-233">FormObjectSet クラスでの機能はありませんが、データソースによって参照されるテーブル内の現在アクティブなレコードを返す FormDataSource.cursor メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-233">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.cursor method, which returns the currently active record in the table that is referenced by the data source.</span></span>

    public Common cursor()

#### <a name="return-value"></a><span data-ttu-id="622ca-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-234">Return Value</span></span>

### <a name="method-findrecord"></a><span data-ttu-id="622ca-235">メソッド findRecord</span><span class="sxs-lookup"><span data-stu-id="622ca-235">Method findRecord</span></span>

<span data-ttu-id="622ca-236">FormObjectSet クラスでの機能はありませんが、現在データソースで指定されるレコードを検索して現在のレコードにする FormDataSource.findRecord メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-236">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.findRecord method, which finds a specified record in the data source and makes it the current one.</span></span>

    public boolean findRecord(Common record)

#### <a name="parameters"></a><span data-ttu-id="622ca-237">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-237">Parameters</span></span>

<span data-ttu-id="622ca-238">記録</span><span class="sxs-lookup"><span data-stu-id="622ca-238">record</span></span>  
<span data-ttu-id="622ca-239">FormObjectSet 基本クラスで使用されていないパラメーター。</span><span class="sxs-lookup"><span data-stu-id="622ca-239">A parameter that is not used in the FormObjectSet base class.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-240">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-240">Return Value</span></span>

<span data-ttu-id="622ca-241">レコードが見つかった場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-241">true if the record was found; otherwise, false.</span></span>

### <a name="method-positiontorecord"></a><span data-ttu-id="622ca-242">メソッド positionToRecord</span><span class="sxs-lookup"><span data-stu-id="622ca-242">Method positionToRecord</span></span>

    public boolean positionToRecord(Common record)

#### <a name="parameters"></a><span data-ttu-id="622ca-243">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-243">Parameters</span></span>

<span data-ttu-id="622ca-244">記録</span><span class="sxs-lookup"><span data-stu-id="622ca-244">record</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-245">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-245">Return Value</span></span>

### <a name="method-first"></a><span data-ttu-id="622ca-246">メソッド first</span><span class="sxs-lookup"><span data-stu-id="622ca-246">Method first</span></span>

<span data-ttu-id="622ca-247">データ ソースの最初のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-247">Moves focus to the first record in a data source.</span></span>

    public int first()

#### <a name="return-value"></a><span data-ttu-id="622ca-248">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-248">Return Value</span></span>

<span data-ttu-id="622ca-249">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-249">A non-zero integer if the operation succeeds.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-250">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-250">Remarks</span></span>

<span data-ttu-id="622ca-251">このメソッドは、ユーザーが CTRL+HOME キーを押してフォームの最初のレコードを選択するときに呼び出されるメソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-251">This method is overridden by the method that is called when a user presses CTRL+HOME to select the first record in a form.</span></span>

### <a name="method-formrun"></a><span data-ttu-id="622ca-252">メソッド formRun</span><span class="sxs-lookup"><span data-stu-id="622ca-252">Method formRun</span></span>

    public xFormRun formRun()

#### <a name="return-value"></a><span data-ttu-id="622ca-253">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-253">Return Value</span></span>

### <a name="method-getposition"></a><span data-ttu-id="622ca-254">メソッド getPosition</span><span class="sxs-lookup"><span data-stu-id="622ca-254">Method getPosition</span></span>

    public int getPosition()

#### <a name="return-value"></a><span data-ttu-id="622ca-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-255">Return Value</span></span>

### <a name="method-id"></a><span data-ttu-id="622ca-256">メソッド id</span><span class="sxs-lookup"><span data-stu-id="622ca-256">Method id</span></span>

    public int id()

#### <a name="return-value"></a><span data-ttu-id="622ca-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-257">Return Value</span></span>

### <a name="method-last"></a><span data-ttu-id="622ca-258">メソッド last</span><span class="sxs-lookup"><span data-stu-id="622ca-258">Method last</span></span>

<span data-ttu-id="622ca-259">データ ソースの最後のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-259">Moves focus to the last record in the data source.</span></span>

    public int last()

#### <a name="return-value"></a><span data-ttu-id="622ca-260">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-260">Return Value</span></span>

<span data-ttu-id="622ca-261">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-261">A non-zero integer if the operation succeeds.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-262">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-262">Remarks</span></span>

<span data-ttu-id="622ca-263">このメソッドは、ユーザーが CTRL+END キーを押してフォームの最後のレコードを選択するときに呼び出されるメソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-263">This method is overridden by the method that is called when a user presses CTRL+END to select the last record in a form.</span></span>

### <a name="method-leaverecord"></a><span data-ttu-id="622ca-264">メソッド leaveRecord</span><span class="sxs-lookup"><span data-stu-id="622ca-264">Method leaveRecord</span></span>

<span data-ttu-id="622ca-265">FormObjectSet クラスでの機能はありませんが、ユーザーが別のレコードに移動するときに通知を提供する FormDataSource.leaveRecord メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-265">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.leaveRecord method, which provides a notification when the user moves to another record.</span></span>

    public boolean leaveRecord([boolean forceUpdate])

#### <a name="parameters"></a><span data-ttu-id="622ca-266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-266">Parameters</span></span>

<span data-ttu-id="622ca-267">forceUpdate</span><span class="sxs-lookup"><span data-stu-id="622ca-267">forceUpdate</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-268">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-268">Return Value</span></span>

### <a name="method-masterobjectset"></a><span data-ttu-id="622ca-269">メソッド masterObjectSet</span><span class="sxs-lookup"><span data-stu-id="622ca-269">Method masterObjectSet</span></span>

<span data-ttu-id="622ca-270">現在のオブジェクト セットのマスター オブジェクト セットを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-270">Retrieves the master object set for the current object set.</span></span>

    public FormObjectSet masterObjectSet()

#### <a name="return-value"></a><span data-ttu-id="622ca-271">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-271">Return Value</span></span>

<span data-ttu-id="622ca-272">マスター オブジェクト セット。</span><span class="sxs-lookup"><span data-stu-id="622ca-272">The master object set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-273">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-273">Remarks</span></span>

<span data-ttu-id="622ca-274">フォームには、多くの場合、1 つ以上のオブジェクトのセット (データ ソース) があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-274">A form often has more than one object set (data source).</span></span> <span data-ttu-id="622ca-275">これらは、ツリー階層を使用して結合されます。ここでは、1 つのデータ ソースがマスターまたは親データソースです。</span><span class="sxs-lookup"><span data-stu-id="622ca-275">These are joined together by using a tree hierarchy, where one data source is the master or parent data source.</span></span> <span data-ttu-id="622ca-276">masterObjectSet メソッドは、特定のデータソースのマスター データソースの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-276">The masterObjectSet method returns the ID of the master data source for a specific data source.</span></span>

#### <a name="examples"></a><span data-ttu-id="622ca-277">例</span><span class="sxs-lookup"><span data-stu-id="622ca-277">Examples</span></span>

<span data-ttu-id="622ca-278">次の例は、FormRun オブジェクトのマスター データ ソースの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-278">The following example returns the name of the master data source for a FormRun object.</span></span>

    private static client Name formDataSourceName(FormRun _formRun) 
    { 
        return _formRun.objectSet().masterObjectSet().name(); 
    }

### <a name="method-name"></a><span data-ttu-id="622ca-279">メソッド名</span><span class="sxs-lookup"><span data-stu-id="622ca-279">Method name</span></span>

<span data-ttu-id="622ca-280">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-280">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-281">Parameters</span></span>

<span data-ttu-id="622ca-282">値</span><span class="sxs-lookup"><span data-stu-id="622ca-282">value</span></span>  
<span data-ttu-id="622ca-283">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-283">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-284">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-284">Return Value</span></span>

<span data-ttu-id="622ca-285">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-285">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-286">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-286">Remarks</span></span>

<span data-ttu-id="622ca-287">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-287">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="622ca-288">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-288">It must start with a letter.</span></span>
-   <span data-ttu-id="622ca-289">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-289">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="622ca-290">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-290">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="622ca-291">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-291">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="622ca-292">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-292">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-next"></a><span data-ttu-id="622ca-293">メソッド next</span><span class="sxs-lookup"><span data-stu-id="622ca-293">Method next</span></span>

<span data-ttu-id="622ca-294">データ ソースの次のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-294">Moves focus to the next record in the data source.</span></span>

    public int next()

#### <a name="return-value"></a><span data-ttu-id="622ca-295">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-295">Return Value</span></span>

<span data-ttu-id="622ca-296">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-296">A non-zero integer if the operation succeeds.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-297">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-297">Remarks</span></span>

<span data-ttu-id="622ca-298">このメソッドは、ユーザーが DOWN ARROW キーを押してフォームの次のレコードを選択するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-298">This method is called when a user selects the next record in a form by pressing the DOWN ARROW key.</span></span>

### <a name="method-nextpage"></a><span data-ttu-id="622ca-299">メソッド nextPage</span><span class="sxs-lookup"><span data-stu-id="622ca-299">Method nextPage</span></span>

<span data-ttu-id="622ca-300">データ ソースで指定した数のレコード (位置変更) を進めます。</span><span class="sxs-lookup"><span data-stu-id="622ca-300">Moves a specified number of records forward in the data source.</span></span>

    public int nextPage(int pageSize)

#### <a name="parameters"></a><span data-ttu-id="622ca-301">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-301">Parameters</span></span>

<span data-ttu-id="622ca-302">pageSize</span><span class="sxs-lookup"><span data-stu-id="622ca-302">pageSize</span></span>  
<span data-ttu-id="622ca-303">スキップするレコードの数。</span><span class="sxs-lookup"><span data-stu-id="622ca-303">The number of records to skip.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-304">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-304">Return Value</span></span>

<span data-ttu-id="622ca-305">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-305">A non-zero integer if the operation succeeds.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-306">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-306">Remarks</span></span>

<span data-ttu-id="622ca-307">このメソッドは、ユーザーがフォーム内にあるときに PAGE DOWN キーを押すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-307">This method is called when a user presses the PAGE DOWN key while he or she is in a form.</span></span> <span data-ttu-id="622ca-308">これにより、ページ サイズは自動的に計算されて、pageSize パラメーターに使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-308">The page size is then automatically calculated and used for the pageSize parameter.</span></span> <span data-ttu-id="622ca-309">このメソッドは、FormDataSource クラスで上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-309">This method is overridden on the FormDataSource class.</span></span>

### <a name="method-object"></a><span data-ttu-id="622ca-310">メソッド object</span><span class="sxs-lookup"><span data-stu-id="622ca-310">Method object</span></span>

    public FormDataObject object(int objectId)

#### <a name="parameters"></a><span data-ttu-id="622ca-311">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-311">Parameters</span></span>

<span data-ttu-id="622ca-312">objectId</span><span class="sxs-lookup"><span data-stu-id="622ca-312">objectId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-313">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-313">Return Value</span></span>

### <a name="method-prev"></a><span data-ttu-id="622ca-314">メソッド prev</span><span class="sxs-lookup"><span data-stu-id="622ca-314">Method prev</span></span>

<span data-ttu-id="622ca-315">データ ソースの前のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-315">Moves focus to the previous record in the data source.</span></span>

    public int prev()

#### <a name="return-value"></a><span data-ttu-id="622ca-316">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-316">Return Value</span></span>

<span data-ttu-id="622ca-317">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-317">A non-zero integer if the operation succeeds.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-318">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-318">Remarks</span></span>

<span data-ttu-id="622ca-319">このメソッドは、ユーザーがフォーム内の前のレコードを選択したときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-319">This method is called when a user selects the previous record in the form.</span></span>

### <a name="method-prevpage"></a><span data-ttu-id="622ca-320">メソッド prevPage</span><span class="sxs-lookup"><span data-stu-id="622ca-320">Method prevPage</span></span>

<span data-ttu-id="622ca-321">データ ソースで指定した数のレコード (位置変更) を戻します。</span><span class="sxs-lookup"><span data-stu-id="622ca-321">Moves a specified number of records back (a positional change) in the data source.</span></span>

    public int prevPage(int pageSize)

#### <a name="parameters"></a><span data-ttu-id="622ca-322">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-322">Parameters</span></span>

<span data-ttu-id="622ca-323">pageSize</span><span class="sxs-lookup"><span data-stu-id="622ca-323">pageSize</span></span>  
<span data-ttu-id="622ca-324">戻すレコードの数 (位置の変更)。</span><span class="sxs-lookup"><span data-stu-id="622ca-324">The number of records to move back (a positional change).</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-325">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-325">Return Value</span></span>

<span data-ttu-id="622ca-326">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-326">A non-zero integer if the operation succeeds.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-327">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-327">Remarks</span></span>

<span data-ttu-id="622ca-328">このメソッドは、ユーザーがフォーム内にあるときに PAGE UP キーを押すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-328">This method is called when a user presses the PAGE UP key while he or she is in a form.</span></span> <span data-ttu-id="622ca-329">これにより、ページ サイズは自動的に計算されて、pageSize パラメーターに使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-329">The page size is then calculated automatically and used for the pageSize parameter.</span></span>

### <a name="method-setposition"></a><span data-ttu-id="622ca-330">メソッド setPosition</span><span class="sxs-lookup"><span data-stu-id="622ca-330">Method setPosition</span></span>

    public boolean setPosition(int position)

#### <a name="parameters"></a><span data-ttu-id="622ca-331">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-331">Parameters</span></span>

<span data-ttu-id="622ca-332">職位</span><span class="sxs-lookup"><span data-stu-id="622ca-332">position</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-333">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-333">Return Value</span></span>

### <a name="method-validatedelete"></a><span data-ttu-id="622ca-334">メソッド validateDelete</span><span class="sxs-lookup"><span data-stu-id="622ca-334">Method validateDelete</span></span>

<span data-ttu-id="622ca-335">FormObjectSet クラスでの機能はありませんが、データソースからのレコードの削除をユーザーが確認するよう求める FormDataSource.validateDelete メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-335">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.validateDelete method, which prompts the user to confirm the deletion of a record from the data source.</span></span>

    public boolean validateDelete()

#### <a name="return-value"></a><span data-ttu-id="622ca-336">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-336">Return Value</span></span>

### <a name="method-validatewrite"></a><span data-ttu-id="622ca-337">メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="622ca-337">Method validateWrite</span></span>

<span data-ttu-id="622ca-338">FormObjectSet クラスでの機能はありませんが、データが有効であるかおよび書き込まれる準備ができているかどうかを判断する FormDataSource.validateWrite メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-338">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.validateWrite method, which determines whether data is valid and ready to be written.</span></span>

    public boolean validateWrite()

#### <a name="return-value"></a><span data-ttu-id="622ca-339">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-339">Return Value</span></span>

### <a name="method-refresh"></a><span data-ttu-id="622ca-340">メソッド refresh</span><span class="sxs-lookup"><span data-stu-id="622ca-340">Method refresh</span></span>

<span data-ttu-id="622ca-341">FormObjectSet クラスでの機能はありませんが、データ ソースにすべてのレコードの表示を更新する FormDataSource.refresh メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-341">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.refresh method, which updates the view of all records in the data source.</span></span>

    public void refresh()

### <a name="method-addnotifyhandler"></a><span data-ttu-id="622ca-342">メソッド addNotifyHandler</span><span class="sxs-lookup"><span data-stu-id="622ca-342">Method addNotifyHandler</span></span>

    public void addNotifyHandler(FormObjectSetNotify notifyHandler)

#### <a name="parameters"></a><span data-ttu-id="622ca-343">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-343">Parameters</span></span>

<span data-ttu-id="622ca-344">notifyHandler</span><span class="sxs-lookup"><span data-stu-id="622ca-344">notifyHandler</span></span>  

### <a name="method-reread"></a><span data-ttu-id="622ca-345">メソッド reread</span><span class="sxs-lookup"><span data-stu-id="622ca-345">Method reread</span></span>

<span data-ttu-id="622ca-346">FormObjectSet クラスでの機能はありませんが、データベースから現在のレコードを再読み込みする FormDataSource.reread メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-346">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.reread method, which rereads the current record from the database.</span></span>

    public void reread()

### <a name="method-init"></a><span data-ttu-id="622ca-347">メソッド init</span><span class="sxs-lookup"><span data-stu-id="622ca-347">Method init</span></span>

<span data-ttu-id="622ca-348">FormObjectSet クラスでの機能はありませんが、データ ソース プロパティに基づいてデータ ソース クエリを作成する FormDataSource.init メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-348">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.init method, which creates a data source query, based on the data source properties.</span></span>

    public void init()

### <a name="method-deletemarked"></a><span data-ttu-id="622ca-349">メソッド deleteMarked</span><span class="sxs-lookup"><span data-stu-id="622ca-349">Method deleteMarked</span></span>

<span data-ttu-id="622ca-350">FormObjectSet クラスでの機能はありませんが、データソースからマークされたレコードをすべて削除する FormDataSource.deleteMarked メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-350">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.deleteMarked method, which deletes all marked records from a data source.</span></span>

    public void deleteMarked()

### <a name="method-delete"></a><span data-ttu-id="622ca-351">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="622ca-351">Method delete</span></span>

<span data-ttu-id="622ca-352">FormObjectSet クラスでの機能はありませんが、現在データソースから選択されるレコードを削除する FormDataSource.delete メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-352">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.delete method, which deletes the record that is currently selected from the data source.</span></span>

    public void delete()

### <a name="method-write"></a><span data-ttu-id="622ca-353">メソッド write</span><span class="sxs-lookup"><span data-stu-id="622ca-353">Method write</span></span>

<span data-ttu-id="622ca-354">FormObjectSet クラスでの機能はありませんが、データベースの書き込み操作を管理する FormDataSource.write メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-354">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.write method, which manages the database write operation.</span></span>

    public void write()

### <a name="method-create"></a><span data-ttu-id="622ca-355">メソッド create</span><span class="sxs-lookup"><span data-stu-id="622ca-355">Method create</span></span>

<span data-ttu-id="622ca-356">FormObjectSet クラスでの機能はありませんが、データ ソースに新しいレコードを作成する FormDataSource.create メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-356">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.create method, which creates a new record in the data source.</span></span>

    public void create([boolean append])

#### <a name="parameters"></a><span data-ttu-id="622ca-357">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-357">Parameters</span></span>

<span data-ttu-id="622ca-358">append</span><span class="sxs-lookup"><span data-stu-id="622ca-358">append</span></span>  
<span data-ttu-id="622ca-359">現在のカーソル位置の前後にレコードを挿入するかどうかを示すブール値フラグ。</span><span class="sxs-lookup"><span data-stu-id="622ca-359">A Boolean flag that indicates whether to insert the record after or before the current cursor position; optional.</span></span> <span data-ttu-id="622ca-360">値が true に設定されている場合、現在のレコードの後に新しいレコードが挿入されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-360">If the value is true, the new record is inserted after the current one.</span></span>

### <a name="method-removenotifyhandler"></a><span data-ttu-id="622ca-361">メソッド removeNotifyHandler</span><span class="sxs-lookup"><span data-stu-id="622ca-361">Method removeNotifyHandler</span></span>

    public void removeNotifyHandler(FormObjectSetNotify notifyHandler)

#### <a name="parameters"></a><span data-ttu-id="622ca-362">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-362">Parameters</span></span>

<span data-ttu-id="622ca-363">notifyHandler</span><span class="sxs-lookup"><span data-stu-id="622ca-363">notifyHandler</span></span>  

### <a name="method-prompt"></a><span data-ttu-id="622ca-364">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="622ca-364">Method prompt</span></span>

<span data-ttu-id="622ca-365">FormObjectSet クラスでの機能はありませんが、クエリの範囲を制限するために使用される SysQueryForm クラスを有効にするFormDataSource.prompt メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-365">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.prompt method, which activates the SysQueryForm class that is used to limit a query range.</span></span>

    public void prompt()

### <a name="method-research"></a><span data-ttu-id="622ca-366">メソッド research</span><span class="sxs-lookup"><span data-stu-id="622ca-366">Method research</span></span>

<span data-ttu-id="622ca-367">FormObjectSet クラスでの機能はありませんが、現在フォームに適用されているフィルターおよびソートで定義されているデータベースの検索を更新する FormDataSource.research メソッドによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-367">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.research method, which updates the database search that is defined by the filters and sorts that are currently applied to the form.</span></span>

    public void research([boolean retainPosition])

#### <a name="parameters"></a><span data-ttu-id="622ca-368">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-368">Parameters</span></span>

<span data-ttu-id="622ca-369">retainPosition</span><span class="sxs-lookup"><span data-stu-id="622ca-369">retainPosition</span></span>  

### <a name="method-refreshex"></a><span data-ttu-id="622ca-370">メソッド refreshEx</span><span class="sxs-lookup"><span data-stu-id="622ca-370">Method refreshEx</span></span>

<span data-ttu-id="622ca-371">FormObjectSet クラスでの機能はありませんが、特定のレコードの表示を更新する FormDataSource.refreshEx メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-371">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.refreshEx method, which updates the view of the specified record.</span></span>

    public void refreshEx([AnyType pos])

#### <a name="parameters"></a><span data-ttu-id="622ca-372">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-372">Parameters</span></span>

<span data-ttu-id="622ca-373">pos</span><span class="sxs-lookup"><span data-stu-id="622ca-373">pos</span></span>  
<span data-ttu-id="622ca-374">FormObjectSet.refreshEx メソッドで使用されていないパラメーター (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-374">A parameter that is not used in the FormObjectSet.refreshEx method; optional.</span></span>

### <a name="method-initvalue"></a><span data-ttu-id="622ca-375">メソッド initValue</span><span class="sxs-lookup"><span data-stu-id="622ca-375">Method initValue</span></span>

<span data-ttu-id="622ca-376">FormObjectSet クラスでの機能はありませんが、新しいレコードでフィールド値を初期化する FormDataSource.initValue メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-376">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.initValue method, which initializes field values in a new record.</span></span>

    public void initValue()

### <a name="method-removefilter"></a><span data-ttu-id="622ca-377">メソッド removeFilter</span><span class="sxs-lookup"><span data-stu-id="622ca-377">Method removeFilter</span></span>

<span data-ttu-id="622ca-378">FormObjectSet クラスでの機能はありませんが、データ ソースのクエリをリセットする FormDataSource.removeFilter メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="622ca-378">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.removeFilter method, which resets the query for the data source.</span></span>

    public void removeFilter()

## <a name="class-formobjectsetcachechangedeventargs"></a><span data-ttu-id="622ca-379">クラス FormObjectSetCacheChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="622ca-379">Class FormObjectSetCacheChangedEventArgs</span></span>
    class FormObjectSetCacheChangedEventArgs extends ManagedEventArgs

### <a name="remarks"></a><span data-ttu-id="622ca-380">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-380">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-381">例</span><span class="sxs-lookup"><span data-stu-id="622ca-381">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-382">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-382">Methods</span></span>

| <span data-ttu-id="622ca-383">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-383">Method</span></span>                                                 | <span data-ttu-id="622ca-384">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-384">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="622ca-385">public NotifyCacheChangeType cacheChangeType()</span><span class="sxs-lookup"><span data-stu-id="622ca-385">public NotifyCacheChangeType cacheChangeType()</span></span>         |                                                           |
| <span data-ttu-id="622ca-386">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="622ca-386">public void finalize()</span></span>                                 |                                                           |
| <span data-ttu-id="622ca-387">public void new(NotifyCacheChangeType cacheChangeType)</span><span class="sxs-lookup"><span data-stu-id="622ca-387">public void new(NotifyCacheChangeType cacheChangeType)</span></span> | <span data-ttu-id="622ca-388">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-388">Initializes a new instance of the ManagedEventArgs class.</span></span> |

### <a name="method-cachechangetype"></a><span data-ttu-id="622ca-389">メソッド cacheChangeType</span><span class="sxs-lookup"><span data-stu-id="622ca-389">Method cacheChangeType</span></span>

    public NotifyCacheChangeType cacheChangeType()

#### <a name="return-value"></a><span data-ttu-id="622ca-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-390">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="622ca-391">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="622ca-391">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="622ca-392">メソッド new</span><span class="sxs-lookup"><span data-stu-id="622ca-392">Method new</span></span>

<span data-ttu-id="622ca-393">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-393">Initializes a new instance of the ManagedEventArgs class.</span></span>

    public void new(NotifyCacheChangeType cacheChangeType)

#### <a name="parameters"></a><span data-ttu-id="622ca-394">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-394">Parameters</span></span>

<span data-ttu-id="622ca-395">cacheChangeType</span><span class="sxs-lookup"><span data-stu-id="622ca-395">cacheChangeType</span></span>  

## <a name="class-formobjectsetcurrentchangedeventargs"></a><span data-ttu-id="622ca-396">クラス FormObjectSetCurrentChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="622ca-396">Class FormObjectSetCurrentChangedEventArgs</span></span>
    class FormObjectSetCurrentChangedEventArgs extends ManagedEventArgs

### <a name="remarks"></a><span data-ttu-id="622ca-397">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-397">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-398">例</span><span class="sxs-lookup"><span data-stu-id="622ca-398">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-399">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-399">Methods</span></span>

| <span data-ttu-id="622ca-400">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-400">Method</span></span>                        | <span data-ttu-id="622ca-401">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-401">Description</span></span>                                               |
|-------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="622ca-402">public int position()</span><span class="sxs-lookup"><span data-stu-id="622ca-402">public int position()</span></span>         |                                                           |
| <span data-ttu-id="622ca-403">public void new(int position)</span><span class="sxs-lookup"><span data-stu-id="622ca-403">public void new(int position)</span></span> | <span data-ttu-id="622ca-404">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-404">Initializes a new instance of the ManagedEventArgs class.</span></span> |
| <span data-ttu-id="622ca-405">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="622ca-405">public void finalize()</span></span>        |                                                           |

### <a name="method-position"></a><span data-ttu-id="622ca-406">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="622ca-406">Method position</span></span>

    public int position()

#### <a name="return-value"></a><span data-ttu-id="622ca-407">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-407">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="622ca-408">メソッド new</span><span class="sxs-lookup"><span data-stu-id="622ca-408">Method new</span></span>

<span data-ttu-id="622ca-409">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-409">Initializes a new instance of the ManagedEventArgs class.</span></span>

    public void new(int position)

#### <a name="parameters"></a><span data-ttu-id="622ca-410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-410">Parameters</span></span>

<span data-ttu-id="622ca-411">職位</span><span class="sxs-lookup"><span data-stu-id="622ca-411">position</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="622ca-412">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="622ca-412">Method finalize</span></span>

    public void finalize()

## <a name="class-formobjectsetleaveeventargs"></a><span data-ttu-id="622ca-413">クラス FormObjectSetLeaveEventArgs</span><span class="sxs-lookup"><span data-stu-id="622ca-413">Class FormObjectSetLeaveEventArgs</span></span>
    class FormObjectSetLeaveEventArgs extends ManagedEventArgs

### <a name="remarks"></a><span data-ttu-id="622ca-414">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-414">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-415">例</span><span class="sxs-lookup"><span data-stu-id="622ca-415">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-416">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-416">Methods</span></span>

| <span data-ttu-id="622ca-417">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-417">Method</span></span>                    | <span data-ttu-id="622ca-418">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-418">Description</span></span>                                                          |
|---------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="622ca-419">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="622ca-419">public void finalize()</span></span>    |                                                                      |
| <span data-ttu-id="622ca-420">public void new()</span><span class="sxs-lookup"><span data-stu-id="622ca-420">public void new()</span></span>         | <span data-ttu-id="622ca-421">FormObjectSetLeaveEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-421">Initializes a new instance of the FormObjectSetLeaveEventArgs class.</span></span> |
| <span data-ttu-id="622ca-422">public void cancelLeave()</span><span class="sxs-lookup"><span data-stu-id="622ca-422">public void cancelLeave()</span></span> |                                                                      |

### <a name="method-finalize"></a><span data-ttu-id="622ca-423">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="622ca-423">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="622ca-424">メソッド new</span><span class="sxs-lookup"><span data-stu-id="622ca-424">Method new</span></span>

<span data-ttu-id="622ca-425">FormObjectSetLeaveEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-425">Initializes a new instance of the FormObjectSetLeaveEventArgs class.</span></span>

    public void new()

### <a name="method-cancelleave"></a><span data-ttu-id="622ca-426">メソッド cancelLeave</span><span class="sxs-lookup"><span data-stu-id="622ca-426">Method cancelLeave</span></span>

    public void cancelLeave()

## <a name="class-formobjectsetmarkingchangedeventargs"></a><span data-ttu-id="622ca-427">クラス FormObjectSetMarkingChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="622ca-427">Class FormObjectSetMarkingChangedEventArgs</span></span>
    class FormObjectSetMarkingChangedEventArgs extends ManagedEventArgs

### <a name="remarks"></a><span data-ttu-id="622ca-428">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-428">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-429">例</span><span class="sxs-lookup"><span data-stu-id="622ca-429">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-430">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-430">Methods</span></span>

| <span data-ttu-id="622ca-431">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-431">Method</span></span>                     | <span data-ttu-id="622ca-432">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-432">Description</span></span>                                               |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="622ca-433">public Array ids()</span><span class="sxs-lookup"><span data-stu-id="622ca-433">public Array ids()</span></span>         |                                                           |
| <span data-ttu-id="622ca-434">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="622ca-434">public void finalize()</span></span>     |                                                           |
| <span data-ttu-id="622ca-435">public void new(Array ids)</span><span class="sxs-lookup"><span data-stu-id="622ca-435">public void new(Array ids)</span></span> | <span data-ttu-id="622ca-436">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-436">Initializes a new instance of the ManagedEventArgs class.</span></span> |

### <a name="method-ids"></a><span data-ttu-id="622ca-437">メソッド ids</span><span class="sxs-lookup"><span data-stu-id="622ca-437">Method ids</span></span>

    public Array ids()

#### <a name="return-value"></a><span data-ttu-id="622ca-438">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-438">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="622ca-439">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="622ca-439">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="622ca-440">メソッド new</span><span class="sxs-lookup"><span data-stu-id="622ca-440">Method new</span></span>

<span data-ttu-id="622ca-441">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-441">Initializes a new instance of the ManagedEventArgs class.</span></span>

    public void new(Array ids)

#### <a name="parameters"></a><span data-ttu-id="622ca-442">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-442">Parameters</span></span>

<span data-ttu-id="622ca-443">ids</span><span class="sxs-lookup"><span data-stu-id="622ca-443">ids</span></span>  

## <a name="class-formobjectsetnotify"></a><span data-ttu-id="622ca-444">クラス FormObjectSetNotify</span><span class="sxs-lookup"><span data-stu-id="622ca-444">Class FormObjectSetNotify</span></span>
    class FormObjectSetNotify extends Object

### <a name="remarks"></a><span data-ttu-id="622ca-445">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-445">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-446">例</span><span class="sxs-lookup"><span data-stu-id="622ca-446">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-447">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-447">Methods</span></span>

| <span data-ttu-id="622ca-448">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-448">Method</span></span>                                                                                                                                                                               | <span data-ttu-id="622ca-449">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-449">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="622ca-450">public boolean onLeave(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="622ca-450">public boolean onLeave(FormObjectSet sender)</span></span>                                                                                                                                         |                                                              |
| <span data-ttu-id="622ca-451">public int onRequestCacheSize(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="622ca-451">public int onRequestCacheSize(FormObjectSet sender)</span></span>                                                                                                                                  |                                                              |
| <span data-ttu-id="622ca-452">public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)</span><span class="sxs-lookup"><span data-stu-id="622ca-452">public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)</span></span>                                                                                              |                                                              |
| <span data-ttu-id="622ca-453">public void new()</span><span class="sxs-lookup"><span data-stu-id="622ca-453">public void new()</span></span>                                                                                                                                                                    | <span data-ttu-id="622ca-454">FormObjectSetNotify クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-454">Initializes a new instance of the FormObjectSetNotify class.</span></span> |
| <span data-ttu-id="622ca-455">public void onCurrentChanged(FormObjectSet sender, int position)</span><span class="sxs-lookup"><span data-stu-id="622ca-455">public void onCurrentChanged(FormObjectSet sender, int position)</span></span>                                                                                                                     |                                                              |
| <span data-ttu-id="622ca-456">public void onActive(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="622ca-456">public void onActive(FormObjectSet sender)</span></span>                                                                                                                                           |                                                              |
| <span data-ttu-id="622ca-457">public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)</span><span class="sxs-lookup"><span data-stu-id="622ca-457">public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)</span></span>                                                                  |                                                              |
| <span data-ttu-id="622ca-458">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="622ca-458">public void finalize()</span></span>                                                                                                                                                               |                                                              |
| <span data-ttu-id="622ca-459">public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span><span class="sxs-lookup"><span data-stu-id="622ca-459">public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span></span> |                                                              |
| <span data-ttu-id="622ca-460">public void onRefresh(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="622ca-460">public void onRefresh(FormObjectSet sender)</span></span>                                                                                                                                          |                                                              |
| <span data-ttu-id="622ca-461">public void onMarkingChanged(FormObjectSet sender, Array ids)</span><span class="sxs-lookup"><span data-stu-id="622ca-461">public void onMarkingChanged(FormObjectSet sender, Array ids)</span></span>                                                                                                                        |                                                              |

### <a name="method-onleave"></a><span data-ttu-id="622ca-462">メソッド onLeave</span><span class="sxs-lookup"><span data-stu-id="622ca-462">Method onLeave</span></span>

    public boolean onLeave(FormObjectSet sender)

#### <a name="parameters"></a><span data-ttu-id="622ca-463">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-463">Parameters</span></span>

<span data-ttu-id="622ca-464">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-464">sender</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-465">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-465">Return Value</span></span>

### <a name="method-onrequestcachesize"></a><span data-ttu-id="622ca-466">メソッド onRequestCacheSize</span><span class="sxs-lookup"><span data-stu-id="622ca-466">Method onRequestCacheSize</span></span>

    public int onRequestCacheSize(FormObjectSet sender)

#### <a name="parameters"></a><span data-ttu-id="622ca-467">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-467">Parameters</span></span>

<span data-ttu-id="622ca-468">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-468">sender</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-469">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-469">Return Value</span></span>

### <a name="method-oncachechanged"></a><span data-ttu-id="622ca-470">メソッド onCacheChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-470">Method onCacheChanged</span></span>

    public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)

#### <a name="parameters"></a><span data-ttu-id="622ca-471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-471">Parameters</span></span>

<span data-ttu-id="622ca-472">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-472">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-473">cacheChangeType</span><span class="sxs-lookup"><span data-stu-id="622ca-473">cacheChangeType</span></span>  

### <a name="method-new"></a><span data-ttu-id="622ca-474">メソッド new</span><span class="sxs-lookup"><span data-stu-id="622ca-474">Method new</span></span>

<span data-ttu-id="622ca-475">FormObjectSetNotify クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-475">Initializes a new instance of the FormObjectSetNotify class.</span></span>

    public void new()

### <a name="method-oncurrentchanged"></a><span data-ttu-id="622ca-476">メソッド onCurrentChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-476">Method onCurrentChanged</span></span>

    public void onCurrentChanged(FormObjectSet sender, int position)

#### <a name="parameters"></a><span data-ttu-id="622ca-477">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-477">Parameters</span></span>

<span data-ttu-id="622ca-478">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-478">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-479">職位</span><span class="sxs-lookup"><span data-stu-id="622ca-479">position</span></span>  

### <a name="method-onactive"></a><span data-ttu-id="622ca-480">メソッド onActive</span><span class="sxs-lookup"><span data-stu-id="622ca-480">Method onActive</span></span>

    public void onActive(FormObjectSet sender)

#### <a name="parameters"></a><span data-ttu-id="622ca-481">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-481">Parameters</span></span>

<span data-ttu-id="622ca-482">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-482">sender</span></span>  

### <a name="method-onpagingparameterschanged"></a><span data-ttu-id="622ca-483">メソッド onPagingParametersChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-483">Method onPagingParametersChanged</span></span>

    public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)

#### <a name="parameters"></a><span data-ttu-id="622ca-484">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-484">Parameters</span></span>

<span data-ttu-id="622ca-485">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-485">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-486">pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="622ca-486">pagingEnabled</span></span>  

<!-- -->

<span data-ttu-id="622ca-487">startRowIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-487">startRowIndex</span></span>  

<!-- -->

<span data-ttu-id="622ca-488">pageSize</span><span class="sxs-lookup"><span data-stu-id="622ca-488">pageSize</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="622ca-489">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="622ca-489">Method finalize</span></span>

    public void finalize()

### <a name="method-onruntimemetadatachanged"></a><span data-ttu-id="622ca-490">メソッド onRuntimeMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-490">Method onRuntimeMetadataChanged</span></span>

    public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)

#### <a name="parameters"></a><span data-ttu-id="622ca-491">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-491">Parameters</span></span>

<span data-ttu-id="622ca-492">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-492">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-493">changedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="622ca-493">changedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="622ca-494">referencedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="622ca-494">referencedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="622ca-495">changedFieldId</span><span class="sxs-lookup"><span data-stu-id="622ca-495">changedFieldId</span></span>  

<!-- -->

<span data-ttu-id="622ca-496">changeType</span><span class="sxs-lookup"><span data-stu-id="622ca-496">changeType</span></span>  

### <a name="method-onrefresh"></a><span data-ttu-id="622ca-497">メソッド onRefresh</span><span class="sxs-lookup"><span data-stu-id="622ca-497">Method onRefresh</span></span>

    public void onRefresh(FormObjectSet sender)

#### <a name="parameters"></a><span data-ttu-id="622ca-498">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-498">Parameters</span></span>

<span data-ttu-id="622ca-499">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-499">sender</span></span>  

### <a name="method-onmarkingchanged"></a><span data-ttu-id="622ca-500">メソッド onMarkingChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-500">Method onMarkingChanged</span></span>

    public void onMarkingChanged(FormObjectSet sender, Array ids)

#### <a name="parameters"></a><span data-ttu-id="622ca-501">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-501">Parameters</span></span>

<span data-ttu-id="622ca-502">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-502">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-503">ids</span><span class="sxs-lookup"><span data-stu-id="622ca-503">ids</span></span>  

## <a name="class-formobjectsetnotifyevents"></a><span data-ttu-id="622ca-504">クラス FormObjectSetNotifyEvents</span><span class="sxs-lookup"><span data-stu-id="622ca-504">Class FormObjectSetNotifyEvents</span></span>
    class FormObjectSetNotifyEvents extends FormObjectSetNotify

### <a name="remarks"></a><span data-ttu-id="622ca-505">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-505">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-506">例</span><span class="sxs-lookup"><span data-stu-id="622ca-506">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-507">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-507">Methods</span></span>

| <span data-ttu-id="622ca-508">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-508">Method</span></span>                                                                                                                                                                               | <span data-ttu-id="622ca-509">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-509">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="622ca-510">public boolean onLeave(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="622ca-510">public boolean onLeave(FormObjectSet sender)</span></span>                                                                                                                                         |                                                                    |
| <span data-ttu-id="622ca-511">public int onRequestCacheSize(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="622ca-511">public int onRequestCacheSize(FormObjectSet sender)</span></span>                                                                                                                                  |                                                                    |
| <span data-ttu-id="622ca-512">public void new()</span><span class="sxs-lookup"><span data-stu-id="622ca-512">public void new()</span></span>                                                                                                                                                                    | <span data-ttu-id="622ca-513">FormObjectSetNotifyEvents クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-513">Initializes a new instance of the FormObjectSetNotifyEvents class.</span></span> |
| <span data-ttu-id="622ca-514">public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span><span class="sxs-lookup"><span data-stu-id="622ca-514">public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span></span> |                                                                    |
| <span data-ttu-id="622ca-515">public void onRefresh(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="622ca-515">public void onRefresh(FormObjectSet sender)</span></span>                                                                                                                                          |                                                                    |
| <span data-ttu-id="622ca-516">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="622ca-516">public void finalize()</span></span>                                                                                                                                                               |                                                                    |
| <span data-ttu-id="622ca-517">public void addEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)</span><span class="sxs-lookup"><span data-stu-id="622ca-517">public void addEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)</span></span>                                                                                   |                                                                    |
| <span data-ttu-id="622ca-518">public void onCurrentChanged(FormObjectSet sender, int position)</span><span class="sxs-lookup"><span data-stu-id="622ca-518">public void onCurrentChanged(FormObjectSet sender, int position)</span></span>                                                                                                                     |                                                                    |
| <span data-ttu-id="622ca-519">public void removeEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)</span><span class="sxs-lookup"><span data-stu-id="622ca-519">public void removeEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)</span></span>                                                                                |                                                                    |
| <span data-ttu-id="622ca-520">public void onMarkingChanged(FormObjectSet sender, Array ids)</span><span class="sxs-lookup"><span data-stu-id="622ca-520">public void onMarkingChanged(FormObjectSet sender, Array ids)</span></span>                                                                                                                        |                                                                    |
| <span data-ttu-id="622ca-521">public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)</span><span class="sxs-lookup"><span data-stu-id="622ca-521">public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)</span></span>                                                                  |                                                                    |
| <span data-ttu-id="622ca-522">public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)</span><span class="sxs-lookup"><span data-stu-id="622ca-522">public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)</span></span>                                                                                              |                                                                    |
| <span data-ttu-id="622ca-523">public void onActive(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="622ca-523">public void onActive(FormObjectSet sender)</span></span>                                                                                                                                           |                                                                    |

### <a name="method-onleave"></a><span data-ttu-id="622ca-524">メソッド onLeave</span><span class="sxs-lookup"><span data-stu-id="622ca-524">Method onLeave</span></span>

    public boolean onLeave(FormObjectSet sender)

#### <a name="parameters"></a><span data-ttu-id="622ca-525">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-525">Parameters</span></span>

<span data-ttu-id="622ca-526">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-526">sender</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-527">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-527">Return Value</span></span>

### <a name="method-onrequestcachesize"></a><span data-ttu-id="622ca-528">メソッド onRequestCacheSize</span><span class="sxs-lookup"><span data-stu-id="622ca-528">Method onRequestCacheSize</span></span>

    public int onRequestCacheSize(FormObjectSet sender)

#### <a name="parameters"></a><span data-ttu-id="622ca-529">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-529">Parameters</span></span>

<span data-ttu-id="622ca-530">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-530">sender</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-531">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-531">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="622ca-532">メソッド new</span><span class="sxs-lookup"><span data-stu-id="622ca-532">Method new</span></span>

<span data-ttu-id="622ca-533">FormObjectSetNotifyEvents クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-533">Initializes a new instance of the FormObjectSetNotifyEvents class.</span></span>

    public void new()

### <a name="method-onruntimemetadatachanged"></a><span data-ttu-id="622ca-534">メソッド onRuntimeMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-534">Method onRuntimeMetadataChanged</span></span>

    public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)

#### <a name="parameters"></a><span data-ttu-id="622ca-535">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-535">Parameters</span></span>

<span data-ttu-id="622ca-536">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-536">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-537">changedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="622ca-537">changedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="622ca-538">referencedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="622ca-538">referencedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="622ca-539">changedFieldId</span><span class="sxs-lookup"><span data-stu-id="622ca-539">changedFieldId</span></span>  

<!-- -->

<span data-ttu-id="622ca-540">changeType</span><span class="sxs-lookup"><span data-stu-id="622ca-540">changeType</span></span>  

### <a name="method-onrefresh"></a><span data-ttu-id="622ca-541">メソッド onRefresh</span><span class="sxs-lookup"><span data-stu-id="622ca-541">Method onRefresh</span></span>

    public void onRefresh(FormObjectSet sender)

#### <a name="parameters"></a><span data-ttu-id="622ca-542">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-542">Parameters</span></span>

<span data-ttu-id="622ca-543">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-543">sender</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="622ca-544">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="622ca-544">Method finalize</span></span>

    public void finalize()

### <a name="method-addeventdelegate"></a><span data-ttu-id="622ca-545">メソッド addEventDelegate</span><span class="sxs-lookup"><span data-stu-id="622ca-545">Method addEventDelegate</span></span>

    public void addEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)

#### <a name="parameters"></a><span data-ttu-id="622ca-546">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-546">Parameters</span></span>

<span data-ttu-id="622ca-547">eventType</span><span class="sxs-lookup"><span data-stu-id="622ca-547">eventType</span></span>  

<!-- -->

<span data-ttu-id="622ca-548">eventDelegate</span><span class="sxs-lookup"><span data-stu-id="622ca-548">eventDelegate</span></span>  

### <a name="method-oncurrentchanged"></a><span data-ttu-id="622ca-549">メソッド onCurrentChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-549">Method onCurrentChanged</span></span>

    public void onCurrentChanged(FormObjectSet sender, int position)

#### <a name="parameters"></a><span data-ttu-id="622ca-550">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-550">Parameters</span></span>

<span data-ttu-id="622ca-551">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-551">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-552">職位</span><span class="sxs-lookup"><span data-stu-id="622ca-552">position</span></span>  

### <a name="method-removeeventdelegate"></a><span data-ttu-id="622ca-553">メソッド removeEventDelegate</span><span class="sxs-lookup"><span data-stu-id="622ca-553">Method removeEventDelegate</span></span>

    public void removeEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)

#### <a name="parameters"></a><span data-ttu-id="622ca-554">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-554">Parameters</span></span>

<span data-ttu-id="622ca-555">eventType</span><span class="sxs-lookup"><span data-stu-id="622ca-555">eventType</span></span>  

<!-- -->

<span data-ttu-id="622ca-556">eventDelegate</span><span class="sxs-lookup"><span data-stu-id="622ca-556">eventDelegate</span></span>  

### <a name="method-onmarkingchanged"></a><span data-ttu-id="622ca-557">メソッド onMarkingChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-557">Method onMarkingChanged</span></span>

    public void onMarkingChanged(FormObjectSet sender, Array ids)

#### <a name="parameters"></a><span data-ttu-id="622ca-558">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-558">Parameters</span></span>

<span data-ttu-id="622ca-559">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-559">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-560">ids</span><span class="sxs-lookup"><span data-stu-id="622ca-560">ids</span></span>  

### <a name="method-onpagingparameterschanged"></a><span data-ttu-id="622ca-561">メソッド onPagingParametersChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-561">Method onPagingParametersChanged</span></span>

    public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)

#### <a name="parameters"></a><span data-ttu-id="622ca-562">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-562">Parameters</span></span>

<span data-ttu-id="622ca-563">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-563">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-564">pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="622ca-564">pagingEnabled</span></span>  

<!-- -->

<span data-ttu-id="622ca-565">startRowIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-565">startRowIndex</span></span>  

<!-- -->

<span data-ttu-id="622ca-566">pageSize</span><span class="sxs-lookup"><span data-stu-id="622ca-566">pageSize</span></span>  

### <a name="method-oncachechanged"></a><span data-ttu-id="622ca-567">メソッド onCacheChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-567">Method onCacheChanged</span></span>

    public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)

#### <a name="parameters"></a><span data-ttu-id="622ca-568">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-568">Parameters</span></span>

<span data-ttu-id="622ca-569">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-569">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-570">cacheChangeType</span><span class="sxs-lookup"><span data-stu-id="622ca-570">cacheChangeType</span></span>  

### <a name="method-onactive"></a><span data-ttu-id="622ca-571">メソッド onActive</span><span class="sxs-lookup"><span data-stu-id="622ca-571">Method onActive</span></span>

    public void onActive(FormObjectSet sender)

#### <a name="parameters"></a><span data-ttu-id="622ca-572">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-572">Parameters</span></span>

<span data-ttu-id="622ca-573">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-573">sender</span></span>  

## <a name="class-formobjectsetpagingparamschangedevtargs"></a><span data-ttu-id="622ca-574">クラス FormObjectSetPagingParamsChangedEvtArgs</span><span class="sxs-lookup"><span data-stu-id="622ca-574">Class FormObjectSetPagingParamsChangedEvtArgs</span></span>
    class FormObjectSetPagingParamsChangedEvtArgs extends ManagedEventArgs

### <a name="remarks"></a><span data-ttu-id="622ca-575">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-575">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-576">例</span><span class="sxs-lookup"><span data-stu-id="622ca-576">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-577">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-577">Methods</span></span>

| <span data-ttu-id="622ca-578">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-578">Method</span></span>                                                                  | <span data-ttu-id="622ca-579">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-579">Description</span></span>                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="622ca-580">public int pageSize()</span><span class="sxs-lookup"><span data-stu-id="622ca-580">public int pageSize()</span></span>                                                   |                                                           |
| <span data-ttu-id="622ca-581">public boolean pagingEnabled()</span><span class="sxs-lookup"><span data-stu-id="622ca-581">public boolean pagingEnabled()</span></span>                                          |                                                           |
| <span data-ttu-id="622ca-582">public int startRowIndex()</span><span class="sxs-lookup"><span data-stu-id="622ca-582">public int startRowIndex()</span></span>                                              |                                                           |
| <span data-ttu-id="622ca-583">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="622ca-583">public void finalize()</span></span>                                                  |                                                           |
| <span data-ttu-id="622ca-584">public void new(boolean pagingEnabled, int startRowIndex, int pageSize)</span><span class="sxs-lookup"><span data-stu-id="622ca-584">public void new(boolean pagingEnabled, int startRowIndex, int pageSize)</span></span> | <span data-ttu-id="622ca-585">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-585">Initializes a new instance of the ManagedEventArgs class.</span></span> |

### <a name="method-pagesize"></a><span data-ttu-id="622ca-586">メソッド pageSize</span><span class="sxs-lookup"><span data-stu-id="622ca-586">Method pageSize</span></span>

    public int pageSize()

#### <a name="return-value"></a><span data-ttu-id="622ca-587">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-587">Return Value</span></span>

### <a name="method-pagingenabled"></a><span data-ttu-id="622ca-588">メソッド pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="622ca-588">Method pagingEnabled</span></span>

    public boolean pagingEnabled()

#### <a name="return-value"></a><span data-ttu-id="622ca-589">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-589">Return Value</span></span>

### <a name="method-startrowindex"></a><span data-ttu-id="622ca-590">メソッド startRowIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-590">Method startRowIndex</span></span>

    public int startRowIndex()

#### <a name="return-value"></a><span data-ttu-id="622ca-591">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-591">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="622ca-592">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="622ca-592">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="622ca-593">メソッド new</span><span class="sxs-lookup"><span data-stu-id="622ca-593">Method new</span></span>

<span data-ttu-id="622ca-594">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-594">Initializes a new instance of the ManagedEventArgs class.</span></span>

    public void new(boolean pagingEnabled, int startRowIndex, int pageSize)

#### <a name="parameters"></a><span data-ttu-id="622ca-595">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-595">Parameters</span></span>

<span data-ttu-id="622ca-596">pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="622ca-596">pagingEnabled</span></span>  

<!-- -->

<span data-ttu-id="622ca-597">startRowIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-597">startRowIndex</span></span>  

<!-- -->

<span data-ttu-id="622ca-598">pageSize</span><span class="sxs-lookup"><span data-stu-id="622ca-598">pageSize</span></span>  

## <a name="class-formobjectsetrequestcachesizeeventargs"></a><span data-ttu-id="622ca-599">クラス FormObjectSetRequestCacheSizeEventArgs</span><span class="sxs-lookup"><span data-stu-id="622ca-599">Class FormObjectSetRequestCacheSizeEventArgs</span></span>
    class FormObjectSetRequestCacheSizeEventArgs extends ManagedEventArgs

### <a name="remarks"></a><span data-ttu-id="622ca-600">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-600">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-601">例</span><span class="sxs-lookup"><span data-stu-id="622ca-601">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-602">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-602">Methods</span></span>

| <span data-ttu-id="622ca-603">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-603">Method</span></span>                                  | <span data-ttu-id="622ca-604">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-604">Description</span></span>                                                                     |
|-----------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-605">public void setCacheSize(int cacheSize)</span><span class="sxs-lookup"><span data-stu-id="622ca-605">public void setCacheSize(int cacheSize)</span></span> |                                                                                 |
| <span data-ttu-id="622ca-606">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="622ca-606">public void finalize()</span></span>                  |                                                                                 |
| <span data-ttu-id="622ca-607">public void new()</span><span class="sxs-lookup"><span data-stu-id="622ca-607">public void new()</span></span>                       | <span data-ttu-id="622ca-608">FormObjectSetRequestCacheSizeEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-608">Initializes a new instance of the FormObjectSetRequestCacheSizeEventArgs class.</span></span> |

### <a name="method-setcachesize"></a><span data-ttu-id="622ca-609">メソッド setCacheSize</span><span class="sxs-lookup"><span data-stu-id="622ca-609">Method setCacheSize</span></span>

    public void setCacheSize(int cacheSize)

#### <a name="parameters"></a><span data-ttu-id="622ca-610">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-610">Parameters</span></span>

<span data-ttu-id="622ca-611">cacheSize</span><span class="sxs-lookup"><span data-stu-id="622ca-611">cacheSize</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="622ca-612">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="622ca-612">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="622ca-613">メソッド new</span><span class="sxs-lookup"><span data-stu-id="622ca-613">Method new</span></span>

<span data-ttu-id="622ca-614">FormObjectSetRequestCacheSizeEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-614">Initializes a new instance of the FormObjectSetRequestCacheSizeEventArgs class.</span></span>

    public void new()

## <a name="class-formpart"></a><span data-ttu-id="622ca-615">クラス FormPart</span><span class="sxs-lookup"><span data-stu-id="622ca-615">Class FormPart</span></span>
    class FormPart extends TreeNode

### <a name="remarks"></a><span data-ttu-id="622ca-616">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-616">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-617">例</span><span class="sxs-lookup"><span data-stu-id="622ca-617">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-618">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-618">Methods</span></span>

| <span data-ttu-id="622ca-619">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-619">Method</span></span>                                       | <span data-ttu-id="622ca-620">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-620">Description</span></span>                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-621">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-621">public str caption(\[str value\])</span></span>            | <span data-ttu-id="622ca-622">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-622">Gets or set the caption of the control.</span></span>                                                                                                   |
| <span data-ttu-id="622ca-623">public str form(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-623">public str form(\[str value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="622ca-624">public str managedContentItem(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-624">public str managedContentItem(\[str value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="622ca-625">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-625">public str name(\[str value\])</span></span>               | <span data-ttu-id="622ca-626">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-626">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="622ca-627">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-627">public Guid origin(\[Guid value\])</span></span>           |                                                                                                                                           |
| <span data-ttu-id="622ca-628">public void new()</span><span class="sxs-lookup"><span data-stu-id="622ca-628">public void new()</span></span>                            | <span data-ttu-id="622ca-629">FormPart クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-629">Initializes a new instance of the FormPart class.</span></span>                                                                                         |

### <a name="method-caption"></a><span data-ttu-id="622ca-630">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="622ca-630">Method caption</span></span>

<span data-ttu-id="622ca-631">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-631">Gets or set the caption of the control.</span></span>

    public str caption([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-632">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-632">Parameters</span></span>

<span data-ttu-id="622ca-633">値</span><span class="sxs-lookup"><span data-stu-id="622ca-633">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-634">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-634">Return Value</span></span>

<span data-ttu-id="622ca-635">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-635">The string that is used as the caption of the control.</span></span>

### <a name="method-form"></a><span data-ttu-id="622ca-636">メソッド form</span><span class="sxs-lookup"><span data-stu-id="622ca-636">Method form</span></span>

    public str form([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-637">Parameters</span></span>

<span data-ttu-id="622ca-638">値</span><span class="sxs-lookup"><span data-stu-id="622ca-638">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-639">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-639">Return Value</span></span>

### <a name="method-managedcontentitem"></a><span data-ttu-id="622ca-640">メソッド managedContentItem</span><span class="sxs-lookup"><span data-stu-id="622ca-640">Method managedContentItem</span></span>

    public str managedContentItem([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-641">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-641">Parameters</span></span>

<span data-ttu-id="622ca-642">値</span><span class="sxs-lookup"><span data-stu-id="622ca-642">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-643">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-643">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="622ca-644">メソッド名</span><span class="sxs-lookup"><span data-stu-id="622ca-644">Method name</span></span>

<span data-ttu-id="622ca-645">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-645">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-646">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-646">Parameters</span></span>

<span data-ttu-id="622ca-647">値</span><span class="sxs-lookup"><span data-stu-id="622ca-647">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-648">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-648">Return Value</span></span>

<span data-ttu-id="622ca-649">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-649">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-650">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-650">Remarks</span></span>

<span data-ttu-id="622ca-651">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-651">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="622ca-652">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="622ca-652">Begins with a letter.</span></span>
-   <span data-ttu-id="622ca-653">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="622ca-653">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="622ca-654">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-654">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="622ca-655">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-655">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="622ca-656">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-656">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-origin"></a><span data-ttu-id="622ca-657">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="622ca-657">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="622ca-658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-658">Parameters</span></span>

<span data-ttu-id="622ca-659">値</span><span class="sxs-lookup"><span data-stu-id="622ca-659">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-660">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-660">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="622ca-661">メソッド new</span><span class="sxs-lookup"><span data-stu-id="622ca-661">Method new</span></span>

<span data-ttu-id="622ca-662">FormPart クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="622ca-662">Initializes a new instance of the FormPart class.</span></span>

    public void new()

## <a name="class-formprogresscontrol"></a><span data-ttu-id="622ca-663">クラス FormProgressControl</span><span class="sxs-lookup"><span data-stu-id="622ca-663">Class FormProgressControl</span></span>
    class FormProgressControl extends FormControl

### <a name="remarks"></a><span data-ttu-id="622ca-664">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-664">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-665">例</span><span class="sxs-lookup"><span data-stu-id="622ca-665">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-666">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-666">Methods</span></span>

| <span data-ttu-id="622ca-667">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-667">Method</span></span>                                                                                                      | <span data-ttu-id="622ca-668">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-668">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-669">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-669">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="622ca-670">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-670">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-671">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-671">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="622ca-672">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-672">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="622ca-673">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="622ca-673">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="622ca-674">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-674">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="622ca-675">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-675">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="622ca-676">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-676">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="622ca-677">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-677">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="622ca-678">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-678">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-679">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="622ca-679">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="622ca-680">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-680">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="622ca-681">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-681">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="622ca-682">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-682">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="622ca-683">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="622ca-683">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="622ca-684">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-684">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="622ca-685">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-685">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="622ca-686">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-686">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="622ca-687">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-687">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="622ca-688">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-688">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="622ca-689">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-689">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-690">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-690">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="622ca-691">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-691">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="622ca-692">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-692">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-693">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-693">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="622ca-694">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-694">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="622ca-695">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-695">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="622ca-696">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-696">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="622ca-697">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-697">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="622ca-698">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="622ca-698">public str dragText()</span></span>                                                                                       | <span data-ttu-id="622ca-699">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-699">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="622ca-700">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-700">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="622ca-701">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-701">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="622ca-702">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="622ca-702">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="622ca-703">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-703">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="622ca-704">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="622ca-704">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="622ca-705">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-705">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="622ca-706">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-706">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="622ca-707">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-707">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="622ca-708">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-708">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="622ca-709">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-709">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-710">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-710">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="622ca-711">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-711">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="622ca-712">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="622ca-712">public str helpField()</span></span>                                                                                      | <span data-ttu-id="622ca-713">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-713">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-714">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-714">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="622ca-715">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-715">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="622ca-716">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-716">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="622ca-717">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-717">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="622ca-718">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="622ca-718">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="622ca-719">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-719">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="622ca-720">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="622ca-720">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-721">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="622ca-721">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="622ca-722">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-722">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="622ca-723">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="622ca-723">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="622ca-724">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-724">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="622ca-725">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="622ca-725">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="622ca-726">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-726">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="622ca-727">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="622ca-727">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-728">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-728">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="622ca-729">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-729">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="622ca-730">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-730">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-731">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-731">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-732">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-732">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-733">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-733">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="622ca-734">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-734">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="622ca-735">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="622ca-735">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="622ca-736">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-736">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="622ca-737">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-737">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="622ca-738">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-738">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="622ca-739">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-739">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="622ca-740">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-740">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="622ca-741">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-741">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="622ca-742">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-742">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="622ca-743">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-743">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="622ca-744">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-744">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="622ca-745">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-745">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="622ca-746">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-746">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-747">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="622ca-747">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-748">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="622ca-748">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="622ca-749">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-749">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="622ca-750">public int pos(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-750">public int pos(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="622ca-751">public int progressType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-751">public int progressType(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-752">public int rangeHi(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-752">public int rangeHi(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="622ca-753">public int rangeLo(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-753">public int rangeLo(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="622ca-754">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-754">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="622ca-755">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-755">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-756">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="622ca-756">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="622ca-757">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-757">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-758">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-758">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="622ca-759">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-759">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="622ca-760">public int step(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-760">public int step(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-761">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-761">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="622ca-762">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="622ca-762">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="622ca-763">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-763">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="622ca-764">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-764">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="622ca-765">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-765">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-766">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-766">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="622ca-767">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-767">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-768">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-768">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-769">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-769">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-770">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-770">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-771">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="622ca-771">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-772">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-772">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-773">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-773">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="622ca-774">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-774">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="622ca-775">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-775">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="622ca-776">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-776">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="622ca-777">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-777">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-778">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-778">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="622ca-779">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-779">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="622ca-780">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-780">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="622ca-781">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-781">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="622ca-782">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-782">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-783">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-783">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="622ca-784">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-784">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="622ca-785">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-785">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="622ca-786">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-786">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="622ca-787">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-787">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-788">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-788">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="622ca-789">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-789">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="622ca-790">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-790">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="622ca-791">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-791">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="622ca-792">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-792">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-793">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-793">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="622ca-794">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-794">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-795">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-795">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="622ca-796">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-796">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="622ca-797">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-797">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-798">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-798">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="622ca-799">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-799">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-800">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-800">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="622ca-801">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-801">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-802">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-802">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="622ca-803">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-803">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="622ca-804">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-804">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="622ca-805">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-805">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="622ca-806">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-806">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-807">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-807">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-808">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-808">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="622ca-809">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-809">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="622ca-810">public void context()</span><span class="sxs-lookup"><span data-stu-id="622ca-810">public void context()</span></span>                                                                                       | <span data-ttu-id="622ca-811">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-811">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-812">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="622ca-812">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="622ca-813">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-813">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-814">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="622ca-814">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="622ca-815">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="622ca-815">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="622ca-816">public void paste()</span><span class="sxs-lookup"><span data-stu-id="622ca-816">public void paste()</span></span>                                                                                         | <span data-ttu-id="622ca-817">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="622ca-817">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-818">public void enter()</span><span class="sxs-lookup"><span data-stu-id="622ca-818">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-819">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-819">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="622ca-820">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-820">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="622ca-821">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-821">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-822">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-822">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="622ca-823">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-823">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="622ca-824">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-824">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-825">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-825">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-826">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="622ca-826">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="622ca-827">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-827">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-828">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-828">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="622ca-829">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-829">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="622ca-830">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="622ca-830">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="622ca-831">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="622ca-831">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="622ca-832">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-832">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="622ca-833">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="622ca-833">public void displayControl()</span></span>                                                                                | <span data-ttu-id="622ca-834">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-834">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="622ca-835">public void cut()</span><span class="sxs-lookup"><span data-stu-id="622ca-835">public void cut()</span></span>                                                                                           | <span data-ttu-id="622ca-836">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="622ca-836">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="622ca-837">public void stepIt()</span><span class="sxs-lookup"><span data-stu-id="622ca-837">public void stepIt()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-838">public void deltaPos(int inc)</span><span class="sxs-lookup"><span data-stu-id="622ca-838">public void deltaPos(int inc)</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="622ca-839">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="622ca-839">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="622ca-840">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-840">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="622ca-841">public void copy()</span><span class="sxs-lookup"><span data-stu-id="622ca-841">public void copy()</span></span>                                                                                          | <span data-ttu-id="622ca-842">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="622ca-842">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="622ca-843">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="622ca-843">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="622ca-844">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-844">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="622ca-845">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-845">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-846">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="622ca-846">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="622ca-847">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-847">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="622ca-848">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="622ca-848">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="622ca-849">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="622ca-849">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="622ca-850">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="622ca-850">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="622ca-851">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-851">Indicates that the control has received focus.</span></span>                                                                                                                          |

### <a name="method-aligncontrol"></a><span data-ttu-id="622ca-852">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="622ca-852">Method alignControl</span></span>

<span data-ttu-id="622ca-853">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-853">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-854">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-854">Parameters</span></span>

<span data-ttu-id="622ca-855">値</span><span class="sxs-lookup"><span data-stu-id="622ca-855">value</span></span>  
<span data-ttu-id="622ca-856">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-856">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-857">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-857">Return Value</span></span>

<span data-ttu-id="622ca-858">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-858">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-859">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-859">Remarks</span></span>

<span data-ttu-id="622ca-860">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-860">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="622ca-861">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="622ca-861">Method allowEdit</span></span>

<span data-ttu-id="622ca-862">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-862">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-863">Parameters</span></span>

<span data-ttu-id="622ca-864">値</span><span class="sxs-lookup"><span data-stu-id="622ca-864">value</span></span>  
<span data-ttu-id="622ca-865">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="622ca-865">The value to assign to the allowEdit property.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-866">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-866">Return Value</span></span>

<span data-ttu-id="622ca-867">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-867">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-868">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-868">Remarks</span></span>

<span data-ttu-id="622ca-869">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="622ca-869">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="622ca-870">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="622ca-870">Method allowSysSetup</span></span>

<span data-ttu-id="622ca-871">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-871">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="622ca-872">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-872">Return Value</span></span>

<span data-ttu-id="622ca-873">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-873">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="622ca-874">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="622ca-874">Method autoDeclaration</span></span>

<span data-ttu-id="622ca-875">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-875">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-876">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-876">Parameters</span></span>

<span data-ttu-id="622ca-877">値</span><span class="sxs-lookup"><span data-stu-id="622ca-877">value</span></span>  
<span data-ttu-id="622ca-878">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-878">The new value for the property; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-879">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-879">Return Value</span></span>

<span data-ttu-id="622ca-880">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-880">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-881">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-881">Remarks</span></span>

<span data-ttu-id="622ca-882">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-882">Controls cannot have identical names.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="622ca-883">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="622ca-883">Method beginDrag</span></span>

<span data-ttu-id="622ca-884">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-884">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-885">Parameters</span></span>

<span data-ttu-id="622ca-886">x</span><span class="sxs-lookup"><span data-stu-id="622ca-886">x</span></span>  
<span data-ttu-id="622ca-887">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-887">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="622ca-888">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="622ca-888">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="622ca-889">y</span><span class="sxs-lookup"><span data-stu-id="622ca-889">y</span></span>  
<span data-ttu-id="622ca-890">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-890">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="622ca-891">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="622ca-891">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-892">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-892">Return Value</span></span>

<span data-ttu-id="622ca-893">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-893">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-894">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-894">Remarks</span></span>

<span data-ttu-id="622ca-895">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="622ca-895">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="622ca-896">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-896">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-calccontrolsize"></a><span data-ttu-id="622ca-897">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="622ca-897">Method calcControlSize</span></span>

<span data-ttu-id="622ca-898">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-898">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="622ca-899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-899">Parameters</span></span>

<span data-ttu-id="622ca-900">chars</span><span class="sxs-lookup"><span data-stu-id="622ca-900">chars</span></span>  
<span data-ttu-id="622ca-901">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="622ca-901">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="622ca-902">明細行</span><span class="sxs-lookup"><span data-stu-id="622ca-902">lines</span></span>  
<span data-ttu-id="622ca-903">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="622ca-903">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-904">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-904">Return Value</span></span>

<span data-ttu-id="622ca-905">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="622ca-905">The container that holds the width and height.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="622ca-906">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="622ca-906">Method configurationKey</span></span>

<span data-ttu-id="622ca-907">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-907">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-908">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-908">Parameters</span></span>

<span data-ttu-id="622ca-909">値</span><span class="sxs-lookup"><span data-stu-id="622ca-909">value</span></span>  
<span data-ttu-id="622ca-910">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-910">The ID of the configuration key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-911">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-911">Return Value</span></span>

<span data-ttu-id="622ca-912">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="622ca-912">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-913">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-913">Remarks</span></span>

<span data-ttu-id="622ca-914">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-914">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="622ca-915">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="622ca-915">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="622ca-916">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="622ca-916">Method configurationKeyEx</span></span>

<span data-ttu-id="622ca-917">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-917">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="622ca-918">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-918">Return Value</span></span>

<span data-ttu-id="622ca-919">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="622ca-919">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-920">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-920">Remarks</span></span>

<span data-ttu-id="622ca-921">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="622ca-921">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="622ca-922">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-922">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="622ca-923">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-923">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="622ca-924">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="622ca-924">Method countryRegionCodes</span></span>

<span data-ttu-id="622ca-925">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-925">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-926">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-926">Parameters</span></span>

<span data-ttu-id="622ca-927">値</span><span class="sxs-lookup"><span data-stu-id="622ca-927">value</span></span>  
<span data-ttu-id="622ca-928">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-928">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-929">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-929">Return Value</span></span>

<span data-ttu-id="622ca-930">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="622ca-930">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="622ca-931">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="622ca-931">Method dataRelationPath</span></span>

<span data-ttu-id="622ca-932">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-932">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-933">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-933">Parameters</span></span>

<span data-ttu-id="622ca-934">値</span><span class="sxs-lookup"><span data-stu-id="622ca-934">value</span></span>  
<span data-ttu-id="622ca-935">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-935">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-936">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-936">Return Value</span></span>

<span data-ttu-id="622ca-937">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="622ca-937">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-938">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-938">Remarks</span></span>

<span data-ttu-id="622ca-939">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="622ca-939">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="622ca-940">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="622ca-940">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-direction"></a><span data-ttu-id="622ca-941">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="622ca-941">Method direction</span></span>

    public int direction([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-942">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-942">Parameters</span></span>

<span data-ttu-id="622ca-943">値</span><span class="sxs-lookup"><span data-stu-id="622ca-943">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-944">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-944">Return Value</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="622ca-945">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="622ca-945">Method displayTarget</span></span>

<span data-ttu-id="622ca-946">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-946">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-947">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-947">Parameters</span></span>

<span data-ttu-id="622ca-948">値</span><span class="sxs-lookup"><span data-stu-id="622ca-948">value</span></span>  
<span data-ttu-id="622ca-949">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-949">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-950">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-950">Return Value</span></span>

<span data-ttu-id="622ca-951">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="622ca-951">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="622ca-952">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="622ca-952">Method dragDrop</span></span>

<span data-ttu-id="622ca-953">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-953">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-954">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-954">Parameters</span></span>

<span data-ttu-id="622ca-955">値</span><span class="sxs-lookup"><span data-stu-id="622ca-955">value</span></span>  
<span data-ttu-id="622ca-956">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-956">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-957">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-957">Return Value</span></span>

<span data-ttu-id="622ca-958">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="622ca-958">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-959">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-959">Remarks</span></span>

<span data-ttu-id="622ca-960">dragLeave、dragOver、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-960">Use the dragLeave, the dragOver, and dragOverEx methods to specify the behavior.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="622ca-961">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="622ca-961">Method dragOver</span></span>

<span data-ttu-id="622ca-962">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-962">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-963">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-963">Parameters</span></span>

<span data-ttu-id="622ca-964">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-964">dragSource</span></span>  
<span data-ttu-id="622ca-965">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-965">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-966">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-966">dragMode</span></span>  
<span data-ttu-id="622ca-967">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-967">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-968">x</span><span class="sxs-lookup"><span data-stu-id="622ca-968">x</span></span>  
<span data-ttu-id="622ca-969">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-969">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-970">y</span><span class="sxs-lookup"><span data-stu-id="622ca-970">y</span></span>  
<span data-ttu-id="622ca-971">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-971">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-972">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-972">Return Value</span></span>

<span data-ttu-id="622ca-973">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="622ca-973">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="622ca-974">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="622ca-974">Method dragOverEx</span></span>

<span data-ttu-id="622ca-975">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-975">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-976">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-976">Parameters</span></span>

<span data-ttu-id="622ca-977">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-977">dragSource</span></span>  
<span data-ttu-id="622ca-978">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-978">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-979">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-979">dragMode</span></span>  
<span data-ttu-id="622ca-980">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-980">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-981">x</span><span class="sxs-lookup"><span data-stu-id="622ca-981">x</span></span>  
<span data-ttu-id="622ca-982">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-982">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-983">y</span><span class="sxs-lookup"><span data-stu-id="622ca-983">y</span></span>  
<span data-ttu-id="622ca-984">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-984">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-985">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-985">Return Value</span></span>

<span data-ttu-id="622ca-986">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="622ca-986">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="622ca-987">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="622ca-987">Method dragText</span></span>

<span data-ttu-id="622ca-988">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-988">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="622ca-989">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-989">Return Value</span></span>

<span data-ttu-id="622ca-990">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-990">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="622ca-991">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="622ca-991">Method enabled</span></span>

<span data-ttu-id="622ca-992">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-992">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-993">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-993">Parameters</span></span>

<span data-ttu-id="622ca-994">値</span><span class="sxs-lookup"><span data-stu-id="622ca-994">value</span></span>  
<span data-ttu-id="622ca-995">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-995">A Boolean value that specifies whether the control is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-996">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-996">Return Value</span></span>

<span data-ttu-id="622ca-997">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-997">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-998">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-998">Remarks</span></span>

<span data-ttu-id="622ca-999">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-999">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="622ca-1000">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1000">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="622ca-1001">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1001">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="622ca-1002">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-1002">Method hasChanged</span></span>

<span data-ttu-id="622ca-1003">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1003">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="622ca-1004">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1004">Parameters</span></span>

<span data-ttu-id="622ca-1005">val</span><span class="sxs-lookup"><span data-stu-id="622ca-1005">val</span></span>  
<span data-ttu-id="622ca-1006">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1006">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1007">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1007">Return Value</span></span>

<span data-ttu-id="622ca-1008">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1008">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="622ca-1009">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="622ca-1009">Method hasUserSetting</span></span>

<span data-ttu-id="622ca-1010">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1010">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="622ca-1011">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1011">Return Value</span></span>

<span data-ttu-id="622ca-1012">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1012">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="622ca-1013">メソッド height</span><span class="sxs-lookup"><span data-stu-id="622ca-1013">Method height</span></span>

<span data-ttu-id="622ca-1014">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1014">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-1015">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1015">Parameters</span></span>

<span data-ttu-id="622ca-1016">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1016">value</span></span>  
<span data-ttu-id="622ca-1017">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1017">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-1018">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1018">mode</span></span>  
<span data-ttu-id="622ca-1019">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1019">An integer that indicates how the height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1020">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1020">Return Value</span></span>

<span data-ttu-id="622ca-1021">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-1021">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1022">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1022">Remarks</span></span>

<span data-ttu-id="622ca-1023">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1023">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="622ca-1024">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="622ca-1024">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="622ca-1025">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1025">Mode</span></span>            | <span data-ttu-id="622ca-1026">高さの計算</span><span class="sxs-lookup"><span data-stu-id="622ca-1026">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-1027">-1 正確</span><span class="sxs-lookup"><span data-stu-id="622ca-1027">-1 Exact</span></span>        | <span data-ttu-id="622ca-1028">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1028">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-1029">0 自動</span><span class="sxs-lookup"><span data-stu-id="622ca-1029">0 Auto</span></span>          | <span data-ttu-id="622ca-1030">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1030">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-1031">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="622ca-1031">1 Column height</span></span> | <span data-ttu-id="622ca-1032">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1032">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="622ca-1033">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1033">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="622ca-1034">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="622ca-1034">Method heightMode</span></span>

<span data-ttu-id="622ca-1035">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1035">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1036">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1036">Parameters</span></span>

<span data-ttu-id="622ca-1037">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1037">value</span></span>  
<span data-ttu-id="622ca-1038">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1038">An integer value that indicates how control height is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1039">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1039">Return Value</span></span>

<span data-ttu-id="622ca-1040">計算モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-1040">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1041">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1041">Remarks</span></span>

<span data-ttu-id="622ca-1042">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="622ca-1042">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="622ca-1043">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1043">Mode</span></span>          | <span data-ttu-id="622ca-1044">高さの計算</span><span class="sxs-lookup"><span data-stu-id="622ca-1044">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-1045">正確</span><span class="sxs-lookup"><span data-stu-id="622ca-1045">Exact</span></span>         | <span data-ttu-id="622ca-1046">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1046">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-1047">自動</span><span class="sxs-lookup"><span data-stu-id="622ca-1047">Auto</span></span>          | <span data-ttu-id="622ca-1048">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1048">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-1049">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="622ca-1049">Column height</span></span> | <span data-ttu-id="622ca-1050">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1050">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="622ca-1051">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1051">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="622ca-1052">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="622ca-1052">Method heightValue</span></span>

<span data-ttu-id="622ca-1053">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1053">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1054">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1054">Parameters</span></span>

<span data-ttu-id="622ca-1055">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1055">value</span></span>  
<span data-ttu-id="622ca-1056">高さをピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1056">An integer that specifies the height in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1057">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1057">Return Value</span></span>

<span data-ttu-id="622ca-1058">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-1058">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1059">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1059">Remarks</span></span>

<span data-ttu-id="622ca-1060">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1060">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="622ca-1061">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="622ca-1061">Method helpField</span></span>

<span data-ttu-id="622ca-1062">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1062">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="622ca-1063">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1063">Return Value</span></span>

<span data-ttu-id="622ca-1064">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-1064">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1065">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1065">Remarks</span></span>

<span data-ttu-id="622ca-1066">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1066">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="622ca-1067">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1067">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="622ca-1068">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="622ca-1068">Method helpText</span></span>

<span data-ttu-id="622ca-1069">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1069">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1070">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1070">Parameters</span></span>

<span data-ttu-id="622ca-1071">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1071">value</span></span>  
<span data-ttu-id="622ca-1072">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1072">The value to assign as the Help text for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1073">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1073">Return Value</span></span>

<span data-ttu-id="622ca-1074">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-1074">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1075">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1075">Remarks</span></span>

<span data-ttu-id="622ca-1076">このメソッドは、プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1076">This method sets the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="622ca-1077">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1077">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="622ca-1078">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="622ca-1078">Method hierarchyParent</span></span>

<span data-ttu-id="622ca-1079">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1079">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1080">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1080">Parameters</span></span>

<span data-ttu-id="622ca-1081">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1081">value</span></span>  
<span data-ttu-id="622ca-1082">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1082">The value to assign to the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1083">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1083">Return Value</span></span>

<span data-ttu-id="622ca-1084">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1084">The HierarchyParent property value of the control.</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="622ca-1085">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="622ca-1085">Method hWnd</span></span>

<span data-ttu-id="622ca-1086">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1086">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="622ca-1087">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1087">Return Value</span></span>

<span data-ttu-id="622ca-1088">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="622ca-1088">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1089">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1089">Remarks</span></span>

<span data-ttu-id="622ca-1090">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1090">The handle can be used with the Windows API.</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="622ca-1091">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="622ca-1091">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="622ca-1092">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1092">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="622ca-1093">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="622ca-1093">Method isDisplayed</span></span>

<span data-ttu-id="622ca-1094">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1094">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="622ca-1095">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1095">Return Value</span></span>

<span data-ttu-id="622ca-1096">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1096">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1097">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1097">Remarks</span></span>

<span data-ttu-id="622ca-1098">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1098">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="622ca-1099">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="622ca-1099">Method isRestricted</span></span>

<span data-ttu-id="622ca-1100">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1100">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="622ca-1101">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1101">Return Value</span></span>

<span data-ttu-id="622ca-1102">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1102">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="622ca-1103">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="622ca-1103">Method isUserSetupEnabled</span></span>

<span data-ttu-id="622ca-1104">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1104">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="622ca-1105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1105">Parameters</span></span>

<span data-ttu-id="622ca-1106">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="622ca-1106">neededSetupRights</span></span>  
<span data-ttu-id="622ca-1107">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1107">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1108">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1108">Return Value</span></span>

<span data-ttu-id="622ca-1109">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1109">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="622ca-1110">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1110">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1111">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1111">Remarks</span></span>

<span data-ttu-id="622ca-1112">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1112">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-1113">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="622ca-1113">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="622ca-1114">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1114">No changes can be made to the control.</span></span> <span data-ttu-id="622ca-1115">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1115">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="622ca-1116">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="622ca-1116">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="622ca-1117">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1117">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="622ca-1118">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1118">The user cannot move the control.</span></span>   |
| <span data-ttu-id="622ca-1119">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="622ca-1119">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="622ca-1120">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1120">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="622ca-1121">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1121">The user can also move the control.</span></span> |

### <a name="method-leave"></a><span data-ttu-id="622ca-1122">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="622ca-1122">Method leave</span></span>

    public boolean leave()

#### <a name="return-value"></a><span data-ttu-id="622ca-1123">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1123">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="622ca-1124">メソッド left</span><span class="sxs-lookup"><span data-stu-id="622ca-1124">Method left</span></span>

<span data-ttu-id="622ca-1125">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1125">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-1126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1126">Parameters</span></span>

<span data-ttu-id="622ca-1127">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1127">value</span></span>  
<span data-ttu-id="622ca-1128">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1128">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-1129">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1129">mode</span></span>  
<span data-ttu-id="622ca-1130">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1130">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1131">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1131">Return Value</span></span>

<span data-ttu-id="622ca-1132">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-1132">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="622ca-1133">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="622ca-1133">Method leftMode</span></span>

<span data-ttu-id="622ca-1134">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1134">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1135">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1135">Parameters</span></span>

<span data-ttu-id="622ca-1136">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1136">value</span></span>  
<span data-ttu-id="622ca-1137">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1137">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1138">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1138">Return Value</span></span>

<span data-ttu-id="622ca-1139">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-1139">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="622ca-1140">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="622ca-1140">Method leftValue</span></span>

<span data-ttu-id="622ca-1141">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1141">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1142">Parameters</span></span>

<span data-ttu-id="622ca-1143">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1143">value</span></span>  
<span data-ttu-id="622ca-1144">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1144">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1145">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1145">Return Value</span></span>

<span data-ttu-id="622ca-1146">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-1146">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="622ca-1147">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="622ca-1147">Method markAsUserAdd</span></span>

<span data-ttu-id="622ca-1148">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="622ca-1148">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1149">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1149">Parameters</span></span>

<span data-ttu-id="622ca-1150">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1150">value</span></span>  
<span data-ttu-id="622ca-1151">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1151">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1152">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1152">Return Value</span></span>

<span data-ttu-id="622ca-1153">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1153">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="622ca-1154">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="622ca-1154">Method mouseDblClick</span></span>

<span data-ttu-id="622ca-1155">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1155">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-1156">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1156">Parameters</span></span>

<span data-ttu-id="622ca-1157">x</span><span class="sxs-lookup"><span data-stu-id="622ca-1157">x</span></span>  
<span data-ttu-id="622ca-1158">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1158">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1159">y</span><span class="sxs-lookup"><span data-stu-id="622ca-1159">y</span></span>  
<span data-ttu-id="622ca-1160">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1160">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1161">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-1161">button</span></span>  
<span data-ttu-id="622ca-1162">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1162">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1163">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-1163">Ctrl</span></span>  
<span data-ttu-id="622ca-1164">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1164">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1165">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-1165">Shift</span></span>  
<span data-ttu-id="622ca-1166">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1166">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1167">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1167">Return Value</span></span>

<span data-ttu-id="622ca-1168">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1168">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1169">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1169">Remarks</span></span>

<span data-ttu-id="622ca-1170">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1170">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="622ca-1171">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="622ca-1171">Method mouseDown</span></span>

<span data-ttu-id="622ca-1172">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1172">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-1173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1173">Parameters</span></span>

<span data-ttu-id="622ca-1174">x</span><span class="sxs-lookup"><span data-stu-id="622ca-1174">x</span></span>  
<span data-ttu-id="622ca-1175">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1175">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1176">y</span><span class="sxs-lookup"><span data-stu-id="622ca-1176">y</span></span>  
<span data-ttu-id="622ca-1177">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1177">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1178">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-1178">button</span></span>  
<span data-ttu-id="622ca-1179">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1179">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1180">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-1180">Ctrl</span></span>  
<span data-ttu-id="622ca-1181">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1181">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1182">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-1182">Shift</span></span>  
<span data-ttu-id="622ca-1183">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1183">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1184">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1184">Return Value</span></span>

<span data-ttu-id="622ca-1185">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1185">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1186">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1186">Remarks</span></span>

<span data-ttu-id="622ca-1187">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1187">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="622ca-1188">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1188">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="622ca-1189">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="622ca-1189">Method mouseMove</span></span>

<span data-ttu-id="622ca-1190">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1190">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-1191">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1191">Parameters</span></span>

<span data-ttu-id="622ca-1192">x</span><span class="sxs-lookup"><span data-stu-id="622ca-1192">x</span></span>  
<span data-ttu-id="622ca-1193">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1193">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1194">y</span><span class="sxs-lookup"><span data-stu-id="622ca-1194">y</span></span>  
<span data-ttu-id="622ca-1195">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1195">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1196">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-1196">button</span></span>  
<span data-ttu-id="622ca-1197">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1197">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1198">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-1198">Ctrl</span></span>  
<span data-ttu-id="622ca-1199">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1199">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1200">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-1200">Shift</span></span>  
<span data-ttu-id="622ca-1201">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1201">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1202">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1202">Return Value</span></span>

<span data-ttu-id="622ca-1203">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1203">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1204">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1204">Remarks</span></span>

<span data-ttu-id="622ca-1205">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1205">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="622ca-1206">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="622ca-1206">Method mouseUp</span></span>

<span data-ttu-id="622ca-1207">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1207">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-1208">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1208">Parameters</span></span>

<span data-ttu-id="622ca-1209">x</span><span class="sxs-lookup"><span data-stu-id="622ca-1209">x</span></span>  
<span data-ttu-id="622ca-1210">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1210">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1211">y</span><span class="sxs-lookup"><span data-stu-id="622ca-1211">y</span></span>  
<span data-ttu-id="622ca-1212">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1212">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1213">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-1213">button</span></span>  
<span data-ttu-id="622ca-1214">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1214">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1215">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-1215">Ctrl</span></span>  
<span data-ttu-id="622ca-1216">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1216">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1217">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-1217">Shift</span></span>  
<span data-ttu-id="622ca-1218">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1218">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1219">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1219">Return Value</span></span>

<span data-ttu-id="622ca-1220">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1220">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1221">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1221">Remarks</span></span>

<span data-ttu-id="622ca-1222">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1222">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="622ca-1223">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1223">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-name"></a><span data-ttu-id="622ca-1224">メソッド名</span><span class="sxs-lookup"><span data-stu-id="622ca-1224">Method name</span></span>

<span data-ttu-id="622ca-1225">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1225">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1226">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1226">Parameters</span></span>

<span data-ttu-id="622ca-1227">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1227">value</span></span>  
<span data-ttu-id="622ca-1228">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-1228">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1229">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1229">Return Value</span></span>

<span data-ttu-id="622ca-1230">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-1230">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1231">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1231">Remarks</span></span>

<span data-ttu-id="622ca-1232">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1232">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="622ca-1233">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1233">It must start with a letter.</span></span>
-   <span data-ttu-id="622ca-1234">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1234">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="622ca-1235">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1235">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="622ca-1236">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1236">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="622ca-1237">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1237">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="622ca-1238">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="622ca-1238">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1239">Parameters</span></span>

<span data-ttu-id="622ca-1240">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1240">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1241">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1241">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="622ca-1242">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="622ca-1242">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="622ca-1243">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1243">Return Value</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="622ca-1244">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="622ca-1244">Method parentControl</span></span>

<span data-ttu-id="622ca-1245">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1245">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="622ca-1246">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1246">Return Value</span></span>

<span data-ttu-id="622ca-1247">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="622ca-1247">The parent control for the control.</span></span>

### <a name="method-pos"></a><span data-ttu-id="622ca-1248">メソッド pos</span><span class="sxs-lookup"><span data-stu-id="622ca-1248">Method pos</span></span>

    public int pos([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1249">Parameters</span></span>

<span data-ttu-id="622ca-1250">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1250">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1251">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1251">Return Value</span></span>

### <a name="method-progresstype"></a><span data-ttu-id="622ca-1252">メソッド progressType</span><span class="sxs-lookup"><span data-stu-id="622ca-1252">Method progressType</span></span>

    public int progressType([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1253">Parameters</span></span>

<span data-ttu-id="622ca-1254">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1254">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1255">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1255">Return Value</span></span>

### <a name="method-rangehi"></a><span data-ttu-id="622ca-1256">メソッド rangeHi</span><span class="sxs-lookup"><span data-stu-id="622ca-1256">Method rangeHi</span></span>

    public int rangeHi([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1257">Parameters</span></span>

<span data-ttu-id="622ca-1258">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1258">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1259">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1259">Return Value</span></span>

### <a name="method-rangelo"></a><span data-ttu-id="622ca-1260">メソッド rangeLo</span><span class="sxs-lookup"><span data-stu-id="622ca-1260">Method rangeLo</span></span>

    public int rangeLo([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1261">Parameters</span></span>

<span data-ttu-id="622ca-1262">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1262">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1263">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1263">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="622ca-1264">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="622ca-1264">Method securityKey</span></span>

<span data-ttu-id="622ca-1265">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1265">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1266">Parameters</span></span>

<span data-ttu-id="622ca-1267">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1267">value</span></span>  
<span data-ttu-id="622ca-1268">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1268">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1269">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1269">Return Value</span></span>

<span data-ttu-id="622ca-1270">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1270">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="622ca-1271">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="622ca-1271">Method showContextMenu</span></span>

<span data-ttu-id="622ca-1272">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1272">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="622ca-1273">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1273">Parameters</span></span>

<span data-ttu-id="622ca-1274">menuHandle</span><span class="sxs-lookup"><span data-stu-id="622ca-1274">menuHandle</span></span>  
<span data-ttu-id="622ca-1275">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="622ca-1275">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1276">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1276">Return Value</span></span>

<span data-ttu-id="622ca-1277">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1277">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-skip"></a><span data-ttu-id="622ca-1278">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="622ca-1278">Method skip</span></span>

<span data-ttu-id="622ca-1279">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1279">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1280">Parameters</span></span>

<span data-ttu-id="622ca-1281">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1281">value</span></span>  
<span data-ttu-id="622ca-1282">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1282">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1283">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1283">Return Value</span></span>

<span data-ttu-id="622ca-1284">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1284">true if the control is skipped when the user presses the TAB key to move to the control; otherwise false.</span></span>

### <a name="method-step"></a><span data-ttu-id="622ca-1285">メソッド step</span><span class="sxs-lookup"><span data-stu-id="622ca-1285">Method step</span></span>

    public int step([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1286">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1286">Parameters</span></span>

<span data-ttu-id="622ca-1287">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1287">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1288">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1288">Return Value</span></span>

### <a name="method-style"></a><span data-ttu-id="622ca-1289">メソッド style</span><span class="sxs-lookup"><span data-stu-id="622ca-1289">Method style</span></span>

    public int style([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1290">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1290">Parameters</span></span>

<span data-ttu-id="622ca-1291">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1291">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1292">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1292">Return Value</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="622ca-1293">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="622ca-1293">Method toolTip</span></span>

<span data-ttu-id="622ca-1294">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1294">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="622ca-1295">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1295">Return Value</span></span>

<span data-ttu-id="622ca-1296">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-1296">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1297">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1297">Remarks</span></span>

<span data-ttu-id="622ca-1298">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1298">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="622ca-1299">メソッド top</span><span class="sxs-lookup"><span data-stu-id="622ca-1299">Method top</span></span>

<span data-ttu-id="622ca-1300">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1300">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-1301">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1301">Parameters</span></span>

<span data-ttu-id="622ca-1302">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1302">value</span></span>  
<span data-ttu-id="622ca-1303">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1303">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-1304">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1304">mode</span></span>  
<span data-ttu-id="622ca-1305">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1305">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1306">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1306">Return Value</span></span>

<span data-ttu-id="622ca-1307">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-1307">The vertical position of the control in the form.</span></span>

### <a name="method-topmode"></a><span data-ttu-id="622ca-1308">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="622ca-1308">Method topMode</span></span>

<span data-ttu-id="622ca-1309">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1309">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1310">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1310">Parameters</span></span>

<span data-ttu-id="622ca-1311">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1311">value</span></span>  
<span data-ttu-id="622ca-1312">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1312">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1313">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1313">Return Value</span></span>

<span data-ttu-id="622ca-1314">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-1314">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="622ca-1315">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="622ca-1315">Method topValue</span></span>

<span data-ttu-id="622ca-1316">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1316">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1317">Parameters</span></span>

<span data-ttu-id="622ca-1318">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1318">value</span></span>  
<span data-ttu-id="622ca-1319">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1319">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1320">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1320">Return Value</span></span>

<span data-ttu-id="622ca-1321">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-1321">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="622ca-1322">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="622ca-1322">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1323">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1323">Parameters</span></span>

<span data-ttu-id="622ca-1324">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1324">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1325">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1325">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="622ca-1326">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="622ca-1326">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="622ca-1327">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1327">Parameters</span></span>

<span data-ttu-id="622ca-1328">データ</span><span class="sxs-lookup"><span data-stu-id="622ca-1328">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1329">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1329">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="622ca-1330">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="622ca-1330">Method userData</span></span>

<span data-ttu-id="622ca-1331">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1331">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1332">Parameters</span></span>

<span data-ttu-id="622ca-1333">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1333">value</span></span>  
<span data-ttu-id="622ca-1334">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1334">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1335">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1335">Return Value</span></span>

<span data-ttu-id="622ca-1336">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="622ca-1336">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="622ca-1337">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="622ca-1337">Method userDataItem</span></span>

<span data-ttu-id="622ca-1338">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1338">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1339">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1339">Parameters</span></span>

<span data-ttu-id="622ca-1340">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1340">value</span></span>  
<span data-ttu-id="622ca-1341">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1341">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1342">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1342">Return Value</span></span>

<span data-ttu-id="622ca-1343">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="622ca-1343">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="622ca-1344">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="622ca-1344">Method userDataItems</span></span>

<span data-ttu-id="622ca-1345">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1345">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1346">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1346">Parameters</span></span>

<span data-ttu-id="622ca-1347">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1347">value</span></span>  
<span data-ttu-id="622ca-1348">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1348">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1349">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1349">Return Value</span></span>

<span data-ttu-id="622ca-1350">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="622ca-1350">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="622ca-1351">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="622ca-1351">Method userDisable</span></span>

<span data-ttu-id="622ca-1352">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1352">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1353">Parameters</span></span>

<span data-ttu-id="622ca-1354">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1354">value</span></span>  
<span data-ttu-id="622ca-1355">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1355">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1356">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1356">Return Value</span></span>

<span data-ttu-id="622ca-1357">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1357">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="622ca-1358">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="622ca-1358">Method userHeight</span></span>

<span data-ttu-id="622ca-1359">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1359">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1360">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1360">Parameters</span></span>

<span data-ttu-id="622ca-1361">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1361">value</span></span>  
<span data-ttu-id="622ca-1362">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1362">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1363">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1363">Return Value</span></span>

<span data-ttu-id="622ca-1364">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-1364">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="622ca-1365">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="622ca-1365">Method userHide</span></span>

<span data-ttu-id="622ca-1366">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1366">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1367">Parameters</span></span>

<span data-ttu-id="622ca-1368">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1368">value</span></span>  
<span data-ttu-id="622ca-1369">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1369">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1370">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1370">Return Value</span></span>

<span data-ttu-id="622ca-1371">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1371">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1372">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1372">Remarks</span></span>

<span data-ttu-id="622ca-1373">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1373">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="622ca-1374">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1374">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="622ca-1375">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1375">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="622ca-1376">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="622ca-1376">Method userOrgContainer</span></span>

<span data-ttu-id="622ca-1377">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1377">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1378">Parameters</span></span>

<span data-ttu-id="622ca-1379">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1379">value</span></span>  
<span data-ttu-id="622ca-1380">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1380">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1381">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1381">Return Value</span></span>

<span data-ttu-id="622ca-1382">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="622ca-1382">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="622ca-1383">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="622ca-1383">Method userOrgSibling</span></span>

<span data-ttu-id="622ca-1384">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1384">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1385">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1385">Parameters</span></span>

<span data-ttu-id="622ca-1386">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1386">value</span></span>  
<span data-ttu-id="622ca-1387">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1387">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1388">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1388">Return Value</span></span>

<span data-ttu-id="622ca-1389">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="622ca-1389">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="622ca-1390">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="622ca-1390">Method userPromptText</span></span>

<span data-ttu-id="622ca-1391">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1391">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1392">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1392">Parameters</span></span>

<span data-ttu-id="622ca-1393">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1393">value</span></span>  
<span data-ttu-id="622ca-1394">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1394">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1395">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1395">Return Value</span></span>

<span data-ttu-id="622ca-1396">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="622ca-1396">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="622ca-1397">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="622ca-1397">Method userSecurityLevel</span></span>

<span data-ttu-id="622ca-1398">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1398">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1399">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1399">Parameters</span></span>

<span data-ttu-id="622ca-1400">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1400">value</span></span>  
<span data-ttu-id="622ca-1401">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1401">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1402">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1402">Return Value</span></span>

<span data-ttu-id="622ca-1403">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="622ca-1403">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="622ca-1404">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="622ca-1404">Method userSkip</span></span>

<span data-ttu-id="622ca-1405">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1405">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1406">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1406">Parameters</span></span>

<span data-ttu-id="622ca-1407">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1407">value</span></span>  
<span data-ttu-id="622ca-1408">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1408">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="622ca-1409">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1409">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1410">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1410">Return Value</span></span>

<span data-ttu-id="622ca-1411">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1411">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="622ca-1412">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="622ca-1412">Method userWidth</span></span>

<span data-ttu-id="622ca-1413">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1413">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1414">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1414">Parameters</span></span>

<span data-ttu-id="622ca-1415">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1415">value</span></span>  
<span data-ttu-id="622ca-1416">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1416">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1417">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1417">Return Value</span></span>

<span data-ttu-id="622ca-1418">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1418">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1419">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1419">Remarks</span></span>

<span data-ttu-id="622ca-1420">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1420">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="622ca-1421">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1421">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="622ca-1422">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1422">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="622ca-1423">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="622ca-1423">Method verticalSpacing</span></span>

<span data-ttu-id="622ca-1424">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1424">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-1425">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1425">Parameters</span></span>

<span data-ttu-id="622ca-1426">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1426">value</span></span>  
<span data-ttu-id="622ca-1427">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1427">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-1428">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1428">mode</span></span>  
<span data-ttu-id="622ca-1429">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1429">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1430">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1430">Return Value</span></span>

<span data-ttu-id="622ca-1431">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="622ca-1431">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="622ca-1432">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="622ca-1432">Method verticalSpacingMode</span></span>

<span data-ttu-id="622ca-1433">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1433">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-1434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1434">Parameters</span></span>

<span data-ttu-id="622ca-1435">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1435">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1436">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1436">Return Value</span></span>

<span data-ttu-id="622ca-1437">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-1437">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="622ca-1438">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="622ca-1438">Method verticalSpacingValue</span></span>

<span data-ttu-id="622ca-1439">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1439">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1440">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1440">Parameters</span></span>

<span data-ttu-id="622ca-1441">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1441">value</span></span>  
<span data-ttu-id="622ca-1442">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1442">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1443">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1443">Return Value</span></span>

<span data-ttu-id="622ca-1444">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="622ca-1444">The vertical spacing of the control in the form.</span></span>

### <a name="method-visible"></a><span data-ttu-id="622ca-1445">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="622ca-1445">Method visible</span></span>

<span data-ttu-id="622ca-1446">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1446">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1447">Parameters</span></span>

<span data-ttu-id="622ca-1448">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1448">value</span></span>  
<span data-ttu-id="622ca-1449">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1449">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1450">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1450">Return Value</span></span>

<span data-ttu-id="622ca-1451">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1451">true if the control is visible; otherwise, false.</span></span>

### <a name="method-width"></a><span data-ttu-id="622ca-1452">メソッド width</span><span class="sxs-lookup"><span data-stu-id="622ca-1452">Method width</span></span>

<span data-ttu-id="622ca-1453">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1453">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-1454">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1454">Parameters</span></span>

<span data-ttu-id="622ca-1455">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1455">value</span></span>  
<span data-ttu-id="622ca-1456">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1456">An integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-1457">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1457">mode</span></span>  
<span data-ttu-id="622ca-1458">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1458">An integer that indicates how the width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1459">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1459">Return Value</span></span>

<span data-ttu-id="622ca-1460">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="622ca-1460">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1461">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1461">Remarks</span></span>

<span data-ttu-id="622ca-1462">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1462">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="622ca-1463">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="622ca-1463">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="622ca-1464">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1464">Mode</span></span>           | <span data-ttu-id="622ca-1465">幅計算</span><span class="sxs-lookup"><span data-stu-id="622ca-1465">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-1466">-1 正確</span><span class="sxs-lookup"><span data-stu-id="622ca-1466">-1 Exact</span></span>       | <span data-ttu-id="622ca-1467">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1467">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-1468">0 自動</span><span class="sxs-lookup"><span data-stu-id="622ca-1468">0 Auto</span></span>         | <span data-ttu-id="622ca-1469">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1469">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-1470">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="622ca-1470">1 Column width</span></span> | <span data-ttu-id="622ca-1471">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1471">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="622ca-1472">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1472">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="622ca-1473">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="622ca-1473">Method widthMode</span></span>

<span data-ttu-id="622ca-1474">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1474">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1475">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1475">Parameters</span></span>

<span data-ttu-id="622ca-1476">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1476">value</span></span>  
<span data-ttu-id="622ca-1477">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1477">An integer value that indicates how control width is calculated; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1478">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1478">Return Value</span></span>

<span data-ttu-id="622ca-1479">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1479">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1480">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1480">Remarks</span></span>

<span data-ttu-id="622ca-1481">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="622ca-1481">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="622ca-1482">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1482">Mode</span></span>         | <span data-ttu-id="622ca-1483">幅計算</span><span class="sxs-lookup"><span data-stu-id="622ca-1483">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-1484">正確</span><span class="sxs-lookup"><span data-stu-id="622ca-1484">Exact</span></span>        | <span data-ttu-id="622ca-1485">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1485">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-1486">自動</span><span class="sxs-lookup"><span data-stu-id="622ca-1486">Auto</span></span>         | <span data-ttu-id="622ca-1487">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1487">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-1488">列の幅</span><span class="sxs-lookup"><span data-stu-id="622ca-1488">Column width</span></span> | <span data-ttu-id="622ca-1489">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1489">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="622ca-1490">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1490">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="622ca-1491">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="622ca-1491">Method widthValue</span></span>

<span data-ttu-id="622ca-1492">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1492">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1493">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1493">Parameters</span></span>

<span data-ttu-id="622ca-1494">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1494">value</span></span>  
<span data-ttu-id="622ca-1495">幅をピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1495">An integer that specifies the width in pixels; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1496">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1496">Return Value</span></span>

<span data-ttu-id="622ca-1497">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="622ca-1497">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1498">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1498">Remarks</span></span>

<span data-ttu-id="622ca-1499">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1499">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-context"></a><span data-ttu-id="622ca-1500">メソッド context</span><span class="sxs-lookup"><span data-stu-id="622ca-1500">Method context</span></span>

<span data-ttu-id="622ca-1501">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1501">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-enddrag"></a><span data-ttu-id="622ca-1502">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="622ca-1502">Method endDrag</span></span>

<span data-ttu-id="622ca-1503">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1503">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="622ca-1504">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1504">Remarks</span></span>

<span data-ttu-id="622ca-1505">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1505">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="622ca-1506">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1506">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-inputsearch"></a><span data-ttu-id="622ca-1507">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="622ca-1507">Method inputSearch</span></span>

<span data-ttu-id="622ca-1508">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1508">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="622ca-1509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1509">Parameters</span></span>

<span data-ttu-id="622ca-1510">searchStr</span><span class="sxs-lookup"><span data-stu-id="622ca-1510">searchStr</span></span>  
<span data-ttu-id="622ca-1511">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1511">The string value to use to filter data; optional.</span></span>

### <a name="method-paste"></a><span data-ttu-id="622ca-1512">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="622ca-1512">Method paste</span></span>

<span data-ttu-id="622ca-1513">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1513">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-enter"></a><span data-ttu-id="622ca-1514">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="622ca-1514">Method enter</span></span>

    public void enter()

### <a name="method-mouseenter"></a><span data-ttu-id="622ca-1515">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="622ca-1515">Method mouseEnter</span></span>

<span data-ttu-id="622ca-1516">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1516">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-1517">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1517">Parameters</span></span>

<span data-ttu-id="622ca-1518">x</span><span class="sxs-lookup"><span data-stu-id="622ca-1518">x</span></span>  
<span data-ttu-id="622ca-1519">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1519">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1520">y</span><span class="sxs-lookup"><span data-stu-id="622ca-1520">y</span></span>  
<span data-ttu-id="622ca-1521">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1521">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1522">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-1522">button</span></span>  
<span data-ttu-id="622ca-1523">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1523">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1524">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-1524">Ctrl</span></span>  
<span data-ttu-id="622ca-1525">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1525">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-1526">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-1526">Shift</span></span>  
<span data-ttu-id="622ca-1527">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1527">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-onlostfocus"></a><span data-ttu-id="622ca-1528">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-1528">Method OnLostFocus</span></span>

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-1529">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1529">Parameters</span></span>

<span data-ttu-id="622ca-1530">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-1530">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-1531">e</span><span class="sxs-lookup"><span data-stu-id="622ca-1531">e</span></span>  

### <a name="method-drop"></a><span data-ttu-id="622ca-1532">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="622ca-1532">Method drop</span></span>

<span data-ttu-id="622ca-1533">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1533">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-1534">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1534">Parameters</span></span>

<span data-ttu-id="622ca-1535">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-1535">dragSource</span></span>  
<span data-ttu-id="622ca-1536">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1536">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-1537">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-1537">dragMode</span></span>  
<span data-ttu-id="622ca-1538">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1538">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-1539">x</span><span class="sxs-lookup"><span data-stu-id="622ca-1539">x</span></span>  
<span data-ttu-id="622ca-1540">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1540">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-1541">y</span><span class="sxs-lookup"><span data-stu-id="622ca-1541">y</span></span>  
<span data-ttu-id="622ca-1542">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1542">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-onleaving"></a><span data-ttu-id="622ca-1543">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="622ca-1543">Method OnLeaving</span></span>

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-1544">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1544">Parameters</span></span>

<span data-ttu-id="622ca-1545">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-1545">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-1546">e</span><span class="sxs-lookup"><span data-stu-id="622ca-1546">e</span></span>  

### <a name="method-ongotfocus"></a><span data-ttu-id="622ca-1547">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-1547">Method OnGotFocus</span></span>

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-1548">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1548">Parameters</span></span>

<span data-ttu-id="622ca-1549">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-1549">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-1550">e</span><span class="sxs-lookup"><span data-stu-id="622ca-1550">e</span></span>  

### <a name="method-mouseleave"></a><span data-ttu-id="622ca-1551">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="622ca-1551">Method mouseLeave</span></span>

<span data-ttu-id="622ca-1552">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1552">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-dropex"></a><span data-ttu-id="622ca-1553">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="622ca-1553">Method dropEx</span></span>

<span data-ttu-id="622ca-1554">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1554">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-1555">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1555">Parameters</span></span>

<span data-ttu-id="622ca-1556">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-1556">dragSource</span></span>  
<span data-ttu-id="622ca-1557">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1557">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-1558">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-1558">dragMode</span></span>  
<span data-ttu-id="622ca-1559">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1559">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-1560">x</span><span class="sxs-lookup"><span data-stu-id="622ca-1560">x</span></span>  
<span data-ttu-id="622ca-1561">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1561">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-1562">y</span><span class="sxs-lookup"><span data-stu-id="622ca-1562">y</span></span>  
<span data-ttu-id="622ca-1563">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1563">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-registeroverridemethod"></a><span data-ttu-id="622ca-1564">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="622ca-1564">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="622ca-1565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1565">Parameters</span></span>

<span data-ttu-id="622ca-1566">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="622ca-1566">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="622ca-1567">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="622ca-1567">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="622ca-1568">overrideObject</span><span class="sxs-lookup"><span data-stu-id="622ca-1568">overrideObject</span></span>  

### <a name="method-dragleave"></a><span data-ttu-id="622ca-1569">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="622ca-1569">Method dragLeave</span></span>

<span data-ttu-id="622ca-1570">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1570">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

### <a name="method-displaycontrol"></a><span data-ttu-id="622ca-1571">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="622ca-1571">Method displayControl</span></span>

<span data-ttu-id="622ca-1572">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1572">Displays the control.</span></span>

    public void displayControl()

### <a name="method-cut"></a><span data-ttu-id="622ca-1573">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="622ca-1573">Method cut</span></span>

<span data-ttu-id="622ca-1574">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="622ca-1574">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-stepit"></a><span data-ttu-id="622ca-1575">メソッド stepIt</span><span class="sxs-lookup"><span data-stu-id="622ca-1575">Method stepIt</span></span>

    public void stepIt()

### <a name="method-deltapos"></a><span data-ttu-id="622ca-1576">メソッド deltaPos</span><span class="sxs-lookup"><span data-stu-id="622ca-1576">Method deltaPos</span></span>

    public void deltaPos(int inc)

#### <a name="parameters"></a><span data-ttu-id="622ca-1577">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1577">Parameters</span></span>

<span data-ttu-id="622ca-1578">inc</span><span class="sxs-lookup"><span data-stu-id="622ca-1578">inc</span></span>  

### <a name="method-lostfocus"></a><span data-ttu-id="622ca-1579">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-1579">Method lostFocus</span></span>

<span data-ttu-id="622ca-1580">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1580">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-copy"></a><span data-ttu-id="622ca-1581">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="622ca-1581">Method copy</span></span>

<span data-ttu-id="622ca-1582">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="622ca-1582">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-prefcolumnsize"></a><span data-ttu-id="622ca-1583">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="622ca-1583">Method prefColumnSize</span></span>

<span data-ttu-id="622ca-1584">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1584">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="622ca-1585">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1585">Parameters</span></span>

<span data-ttu-id="622ca-1586">width</span><span class="sxs-lookup"><span data-stu-id="622ca-1586">width</span></span>  
<span data-ttu-id="622ca-1587">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="622ca-1587">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="622ca-1588">height</span><span class="sxs-lookup"><span data-stu-id="622ca-1588">height</span></span>  
<span data-ttu-id="622ca-1589">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="622ca-1589">The preferred height of the control.</span></span>

### <a name="method-onenter"></a><span data-ttu-id="622ca-1590">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="622ca-1590">Method OnEnter</span></span>

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-1591">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1591">Parameters</span></span>

<span data-ttu-id="622ca-1592">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-1592">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-1593">e</span><span class="sxs-lookup"><span data-stu-id="622ca-1593">e</span></span>  

### <a name="method-setfocus"></a><span data-ttu-id="622ca-1594">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-1594">Method setFocus</span></span>

<span data-ttu-id="622ca-1595">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1595">Sets the focus on the control.</span></span>

    public void setFocus()

### <a name="method-resetusersetting"></a><span data-ttu-id="622ca-1596">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="622ca-1596">Method resetUserSetting</span></span>

<span data-ttu-id="622ca-1597">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="622ca-1597">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-gotfocus"></a><span data-ttu-id="622ca-1598">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-1598">Method gotFocus</span></span>

<span data-ttu-id="622ca-1599">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1599">Indicates that the control has received focus.</span></span>

    public void gotFocus()

## <a name="class-formqueryminer"></a><span data-ttu-id="622ca-1600">クラス FormQueryMiner</span><span class="sxs-lookup"><span data-stu-id="622ca-1600">Class FormQueryMiner</span></span>
    class FormQueryMiner extends Object

### <a name="remarks"></a><span data-ttu-id="622ca-1601">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1601">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-1602">例</span><span class="sxs-lookup"><span data-stu-id="622ca-1602">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-1603">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-1603">Methods</span></span>

| <span data-ttu-id="622ca-1604">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-1604">Method</span></span> | <span data-ttu-id="622ca-1605">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-1605">Description</span></span> |
|--------|-------------|
|        |             |

## <a name="class-formradiocontrol"></a><span data-ttu-id="622ca-1606">クラス FormRadioControl</span><span class="sxs-lookup"><span data-stu-id="622ca-1606">Class FormRadioControl</span></span>
    class FormRadioControl extends FormControl

### <a name="remarks"></a><span data-ttu-id="622ca-1607">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1607">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-1608">例</span><span class="sxs-lookup"><span data-stu-id="622ca-1608">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-1609">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-1609">Methods</span></span>

| <span data-ttu-id="622ca-1610">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-1610">Method</span></span>                                                                                                      | <span data-ttu-id="622ca-1611">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-1611">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-1612">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1612">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="622ca-1613">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1613">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-1614">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1614">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="622ca-1615">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1615">Determines whether the user can modify the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="622ca-1616">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="622ca-1616">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="622ca-1617">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1617">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="622ca-1618">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1618">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1619">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1619">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="622ca-1620">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1620">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="622ca-1621">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1621">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="622ca-1622">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1622">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="622ca-1623">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1623">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-1624">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1624">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-1625">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-1625">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="622ca-1626">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1626">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-1627">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1627">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="622ca-1628">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1628">Gets or sets the font weight that is used to display text in the control.</span></span>                                                                                               |
| <span data-ttu-id="622ca-1629">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1629">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1630">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1630">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1631">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1631">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1632">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1632">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1633">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="622ca-1633">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="622ca-1634">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1634">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="622ca-1635">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1635">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="622ca-1636">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1636">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="622ca-1637">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1637">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="622ca-1638">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1638">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="622ca-1639">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1639">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="622ca-1640">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1640">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="622ca-1641">public int columns(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1641">public int columns(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1642">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1642">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="622ca-1643">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1643">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="622ca-1644">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="622ca-1644">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="622ca-1645">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1645">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="622ca-1646">public int count()</span><span class="sxs-lookup"><span data-stu-id="622ca-1646">public int count()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1647">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1647">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="622ca-1648">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1648">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="622ca-1649">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1649">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1650">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1650">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1651">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1651">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1652">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1652">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="622ca-1653">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1653">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="622ca-1654">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1654">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="622ca-1655">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1655">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                |
| <span data-ttu-id="622ca-1656">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1656">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1657">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1657">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1658">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1658">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1659">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1659">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="622ca-1660">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1660">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="622ca-1661">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1661">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-1662">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1662">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="622ca-1663">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-1663">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="622ca-1664">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1664">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="622ca-1665">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-1665">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="622ca-1666">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1666">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="622ca-1667">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="622ca-1667">public str dragText()</span></span>                                                                                       | <span data-ttu-id="622ca-1668">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1668">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="622ca-1669">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1669">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="622ca-1670">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1670">Determines whether the object is enabled or disabled.</span></span>                                                                                                                   |
| <span data-ttu-id="622ca-1671">public EnumId enumType(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1671">public EnumId enumType(\[EnumId value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1672">public EnumId enumTypeValue()</span><span class="sxs-lookup"><span data-stu-id="622ca-1672">public EnumId enumTypeValue()</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1673">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1673">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1674">public int find(str string)</span><span class="sxs-lookup"><span data-stu-id="622ca-1674">public int find(str string)</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1675">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1675">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="622ca-1676">コントロールに使用されるフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1676">Gets or sets the name of the font that is used for the control.</span></span>                                                                                                         |
| <span data-ttu-id="622ca-1677">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1677">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-1678">コントロール内のテキストに使用されるフォント サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1678">Gets or sets the font size that is used for the control.</span></span>                                                                                                                |
| <span data-ttu-id="622ca-1679">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1679">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="622ca-1680">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1680">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="622ca-1681">public int framePosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1681">public int framePosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1682">public int frameType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1682">public int frameType(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1683">public str getText(int index)</span><span class="sxs-lookup"><span data-stu-id="622ca-1683">public str getText(int index)</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1684">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1684">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="622ca-1685">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1685">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="622ca-1686">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="622ca-1686">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="622ca-1687">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1687">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="622ca-1688">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1688">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="622ca-1689">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1689">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="622ca-1690">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1690">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="622ca-1691">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1691">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-1692">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1692">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="622ca-1693">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1693">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="622ca-1694">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="622ca-1694">public str helpField()</span></span>                                                                                      | <span data-ttu-id="622ca-1695">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1695">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-1696">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1696">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="622ca-1697">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1697">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>                                                         |
| <span data-ttu-id="622ca-1698">public boolean hideFirstEntry(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1698">public boolean hideFirstEntry(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1699">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1699">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="622ca-1700">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1700">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="622ca-1701">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="622ca-1701">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="622ca-1702">コントロールに関連付けられているウィンドウのハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1702">Returns the handle to the window that is associated with the control.</span></span>                                                                                                   |
| <span data-ttu-id="622ca-1703">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="622ca-1703">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="622ca-1704">コントロールがコンテナーかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1704">Gets a value that indicates whether the control is a container.</span></span>                                                                                                         |
| <span data-ttu-id="622ca-1705">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="622ca-1705">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="622ca-1706">コントロールが表示されるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1706">Returns a value that indicates whether the control is displayed.</span></span>                                                                                                        |
| <span data-ttu-id="622ca-1707">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="622ca-1707">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="622ca-1708">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1708">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="622ca-1709">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="622ca-1709">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="622ca-1710">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1710">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="622ca-1711">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="622ca-1711">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1712">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1712">public boolean italic(\[boolean value\])</span></span>                                                                    | <span data-ttu-id="622ca-1713">コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1713">Sets or returns a value that indicates whether the text in the control is italic.</span></span>                                                                                       |
| <span data-ttu-id="622ca-1714">public int item(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1714">public int item(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1715">public int items(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1715">public int items(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1716">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="622ca-1716">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1717">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1717">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="622ca-1718">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1718">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="622ca-1719">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1719">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1720">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1720">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1721">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1721">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1722">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1722">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-1723">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1723">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-1724">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1724">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-1725">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1725">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="622ca-1726">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1726">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="622ca-1727">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="622ca-1727">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="622ca-1728">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="622ca-1728">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1729">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-1729">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="622ca-1730">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1730">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="622ca-1731">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-1731">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="622ca-1732">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1732">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="622ca-1733">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-1733">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="622ca-1734">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1734">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="622ca-1735">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-1735">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="622ca-1736">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1736">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="622ca-1737">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1737">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="622ca-1738">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1738">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="622ca-1739">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1739">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1740">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="622ca-1740">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1741">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="622ca-1741">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="622ca-1742">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1742">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="622ca-1743">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1743">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1744">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1744">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1745">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1745">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1746">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1746">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1747">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1747">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="622ca-1748">コントロールに関連付けられているセキュリティ キーを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1748">Sets or returns the security key that is associated with the control.</span></span>                                                                                                   |
| <span data-ttu-id="622ca-1749">public int selection(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1749">public int selection(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1750">public int selectionChange()</span><span class="sxs-lookup"><span data-stu-id="622ca-1750">public int selectionChange()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1751">public int selectText(str string)</span><span class="sxs-lookup"><span data-stu-id="622ca-1751">public int selectText(str string)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1752">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="622ca-1752">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="622ca-1753">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1753">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-1754">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1754">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="622ca-1755">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1755">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="622ca-1756">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1756">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1757">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1757">public str text(\[str value\])</span></span>                                                                              | <span data-ttu-id="622ca-1758">コントロールのテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1758">Sets or returns the text for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="622ca-1759">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="622ca-1759">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="622ca-1760">コントロールのツールヒント テキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1760">Sets or returns the tooltip text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="622ca-1761">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1761">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="622ca-1762">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1762">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-1763">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1763">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1764">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1764">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1765">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1765">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1766">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1766">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="622ca-1767">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1767">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-1768">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1768">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-1769">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1769">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-1770">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1770">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1771">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1771">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="622ca-1772">コントロール内のテキストの下線プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1772">Sets or returns the value of the underline property for the text in the control.</span></span>                                                                                        |
| <span data-ttu-id="622ca-1773">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="622ca-1773">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1774">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1774">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-1775">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1775">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="622ca-1776">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1776">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="622ca-1777">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1777">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="622ca-1778">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1778">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="622ca-1779">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1779">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-1780">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1780">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="622ca-1781">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1781">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="622ca-1782">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1782">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="622ca-1783">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1783">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="622ca-1784">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1784">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-1785">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1785">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="622ca-1786">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1786">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="622ca-1787">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1787">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="622ca-1788">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1788">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="622ca-1789">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1789">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-1790">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1790">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="622ca-1791">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1791">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="622ca-1792">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1792">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="622ca-1793">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1793">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="622ca-1794">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1794">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-1795">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1795">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="622ca-1796">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1796">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-1797">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1797">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="622ca-1798">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="622ca-1798">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1799">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1799">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="622ca-1800">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1800">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-1801">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1801">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="622ca-1802">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1802">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-1803">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1803">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="622ca-1804">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1804">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-1805">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1805">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1806">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1806">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="622ca-1807">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1807">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="622ca-1808">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1808">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="622ca-1809">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1809">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="622ca-1810">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1810">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-1811">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1811">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-1812">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1812">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="622ca-1813">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1813">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="622ca-1814">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1814">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1815">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1815">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1816">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-1816">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="622ca-1817">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1817">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="622ca-1818">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="622ca-1818">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="622ca-1819">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1819">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="622ca-1820">public void insert(str string, int index)</span><span class="sxs-lookup"><span data-stu-id="622ca-1820">public void insert(str string, int index)</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1821">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1821">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1822">public void delete(str string)</span><span class="sxs-lookup"><span data-stu-id="622ca-1822">public void delete(str string)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1823">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="622ca-1823">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="622ca-1824">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1824">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="622ca-1825">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1825">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1826">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="622ca-1826">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1827">public void endUpdate()</span><span class="sxs-lookup"><span data-stu-id="622ca-1827">public void endUpdate()</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1828">public void cut()</span><span class="sxs-lookup"><span data-stu-id="622ca-1828">public void cut()</span></span>                                                                                           | <span data-ttu-id="622ca-1829">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="622ca-1829">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="622ca-1830">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="622ca-1830">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="622ca-1831">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="622ca-1831">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="622ca-1832">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-1832">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="622ca-1833">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1833">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="622ca-1834">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="622ca-1834">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="622ca-1835">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1835">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="622ca-1836">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1836">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1837">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1837">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1838">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="622ca-1838">public void displayControl()</span></span>                                                                                | <span data-ttu-id="622ca-1839">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1839">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="622ca-1840">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1840">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1841">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="622ca-1841">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="622ca-1842">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1842">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-1843">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="622ca-1843">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="622ca-1844">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1844">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="622ca-1845">public void add(str string)</span><span class="sxs-lookup"><span data-stu-id="622ca-1845">public void add(str string)</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1846">public void context()</span><span class="sxs-lookup"><span data-stu-id="622ca-1846">public void context()</span></span>                                                                                       | <span data-ttu-id="622ca-1847">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1847">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-1848">private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1848">private void OnSelectionChanging(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1849">public void beginUpdate()</span><span class="sxs-lookup"><span data-stu-id="622ca-1849">public void beginUpdate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1850">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1850">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1851">public void enter()</span><span class="sxs-lookup"><span data-stu-id="622ca-1851">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1852">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="622ca-1852">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="622ca-1853">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1853">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="622ca-1854">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1854">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1855">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="622ca-1855">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="622ca-1856">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1856">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="622ca-1857">public void clear()</span><span class="sxs-lookup"><span data-stu-id="622ca-1857">public void clear()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1858">public void paste()</span><span class="sxs-lookup"><span data-stu-id="622ca-1858">public void paste()</span></span>                                                                                         | <span data-ttu-id="622ca-1859">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1859">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-1860">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="622ca-1860">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1861">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1861">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1862">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-1862">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="622ca-1863">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1863">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="622ca-1864">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-1864">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1865">public void undo()</span><span class="sxs-lookup"><span data-stu-id="622ca-1865">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="622ca-1866">public void copy()</span><span class="sxs-lookup"><span data-stu-id="622ca-1866">public void copy()</span></span>                                                                                          | <span data-ttu-id="622ca-1867">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="622ca-1867">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="622ca-1868">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="622ca-1868">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="622ca-1869">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1869">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |

### <a name="method-aligncontrol"></a><span data-ttu-id="622ca-1870">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="622ca-1870">Method alignControl</span></span>

<span data-ttu-id="622ca-1871">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1871">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1872">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1872">Parameters</span></span>

<span data-ttu-id="622ca-1873">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1873">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1874">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1874">Return Value</span></span>

<span data-ttu-id="622ca-1875">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1875">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1876">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1876">Remarks</span></span>

<span data-ttu-id="622ca-1877">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1877">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="622ca-1878">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="622ca-1878">Method allowEdit</span></span>

<span data-ttu-id="622ca-1879">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1879">Determines whether the user can modify the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1880">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1880">Parameters</span></span>

<span data-ttu-id="622ca-1881">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1881">value</span></span>  
<span data-ttu-id="622ca-1882">コントロールの allowEdit プロパティに割り当てるブール値: オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-1882">The Boolean value to assign as the allowEdit property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1883">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1883">Return Value</span></span>

<span data-ttu-id="622ca-1884">コントロールを変更することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1884">true if the control can be modified; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1885">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1885">Remarks</span></span>

<span data-ttu-id="622ca-1886">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="622ca-1886">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="622ca-1887">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="622ca-1887">Method allowSysSetup</span></span>

<span data-ttu-id="622ca-1888">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1888">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="622ca-1889">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1889">Return Value</span></span>

<span data-ttu-id="622ca-1890">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1890">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-arrayindex"></a><span data-ttu-id="622ca-1891">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-1891">Method arrayIndex</span></span>

    public int arrayIndex([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1892">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1892">Parameters</span></span>

<span data-ttu-id="622ca-1893">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1893">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1894">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1894">Return Value</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="622ca-1895">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="622ca-1895">Method autoDeclaration</span></span>

<span data-ttu-id="622ca-1896">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1896">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1897">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1897">Parameters</span></span>

<span data-ttu-id="622ca-1898">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1898">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1899">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1899">Return Value</span></span>

<span data-ttu-id="622ca-1900">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-1900">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1901">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1901">Remarks</span></span>

<span data-ttu-id="622ca-1902">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1902">Controls cannot have identical names.</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="622ca-1903">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="622ca-1903">Method backgroundColor</span></span>

<span data-ttu-id="622ca-1904">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1904">Gets or sets the background color of the control.</span></span>

    public int backgroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1905">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1905">Parameters</span></span>

<span data-ttu-id="622ca-1906">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1906">value</span></span>  
<span data-ttu-id="622ca-1907">コントロールの背景色に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1907">The value to assign for the background color of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1908">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1908">Return Value</span></span>

<span data-ttu-id="622ca-1909">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-1909">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1910">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1910">Remarks</span></span>

<span data-ttu-id="622ca-1911">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1911">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="622ca-1912">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="622ca-1912">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="622ca-1913">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="622ca-1913">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="622ca-1914">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="622ca-1914">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="622ca-1915">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1915">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="622ca-1916">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1916">The maximum value for a single byte is 255.</span></span>

### <a name="method-backstyle"></a><span data-ttu-id="622ca-1917">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="622ca-1917">Method backStyle</span></span>

<span data-ttu-id="622ca-1918">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1918">Determines whether the control background can be transparent.</span></span>

    public int backStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1919">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1919">Parameters</span></span>

<span data-ttu-id="622ca-1920">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1920">value</span></span>  
<span data-ttu-id="622ca-1921">コントロールの背景スタイルに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1921">The value to assign for the background style of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1922">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1922">Return Value</span></span>

<span data-ttu-id="622ca-1923">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1923">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="622ca-1924">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="622ca-1924">Method beginDrag</span></span>

<span data-ttu-id="622ca-1925">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1925">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-1926">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1926">Parameters</span></span>

<span data-ttu-id="622ca-1927">x</span><span class="sxs-lookup"><span data-stu-id="622ca-1927">x</span></span>  
<span data-ttu-id="622ca-1928">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1928">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="622ca-1929">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="622ca-1929">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="622ca-1930">y</span><span class="sxs-lookup"><span data-stu-id="622ca-1930">y</span></span>  
<span data-ttu-id="622ca-1931">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1931">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="622ca-1932">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="622ca-1932">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1933">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1933">Return Value</span></span>

<span data-ttu-id="622ca-1934">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-1934">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1935">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1935">Remarks</span></span>

<span data-ttu-id="622ca-1936">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="622ca-1936">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="622ca-1937">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1937">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-bold"></a><span data-ttu-id="622ca-1938">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="622ca-1938">Method bold</span></span>

<span data-ttu-id="622ca-1939">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1939">Gets or sets the font weight that is used to display text in the control.</span></span>

    public int bold([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1940">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1940">Parameters</span></span>

<span data-ttu-id="622ca-1941">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1941">value</span></span>  
<span data-ttu-id="622ca-1942">コントロールのボールド設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-1942">The value to assign to the bold setting of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1943">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1943">Return Value</span></span>

<span data-ttu-id="622ca-1944">0 (ゼロ) から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1944">An integer value between 0 (zero) and 9, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1945">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1945">Remarks</span></span>

<span data-ttu-id="622ca-1946">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-1946">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="622ca-1947">0 - 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1947">0 – Use the default font weight.</span></span>
-   <span data-ttu-id="622ca-1948">1 - シン。</span><span class="sxs-lookup"><span data-stu-id="622ca-1948">1 – Thin.</span></span>
-   <span data-ttu-id="622ca-1949">2 - エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="622ca-1949">2 – Extra-light.</span></span>
-   <span data-ttu-id="622ca-1950">3 - ライト。</span><span class="sxs-lookup"><span data-stu-id="622ca-1950">3 – Light.</span></span>
-   <span data-ttu-id="622ca-1951">4 - 標準。</span><span class="sxs-lookup"><span data-stu-id="622ca-1951">4 – Normal.</span></span>
-   <span data-ttu-id="622ca-1952">5 - 中。</span><span class="sxs-lookup"><span data-stu-id="622ca-1952">5 – Medium.</span></span>
-   <span data-ttu-id="622ca-1953">6 - セミボールド。</span><span class="sxs-lookup"><span data-stu-id="622ca-1953">6 – Semibold.</span></span>
-   <span data-ttu-id="622ca-1954">7 - 太字。</span><span class="sxs-lookup"><span data-stu-id="622ca-1954">7 – Bold.</span></span>
-   <span data-ttu-id="622ca-1955">8 - 極太。</span><span class="sxs-lookup"><span data-stu-id="622ca-1955">8 – Extra-bold.</span></span>
-   <span data-ttu-id="622ca-1956">9 - ヘビー。</span><span class="sxs-lookup"><span data-stu-id="622ca-1956">9 – Heavy.</span></span>

### <a name="method-bottommargin"></a><span data-ttu-id="622ca-1957">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="622ca-1957">Method bottomMargin</span></span>

    public int bottomMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-1958">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1958">Parameters</span></span>

<span data-ttu-id="622ca-1959">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1959">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-1960">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1960">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1961">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1961">Return Value</span></span>

### <a name="method-bottommarginmode"></a><span data-ttu-id="622ca-1962">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="622ca-1962">Method bottomMarginMode</span></span>

    public AutoMode bottomMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-1963">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1963">Parameters</span></span>

<span data-ttu-id="622ca-1964">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-1964">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1965">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1965">Return Value</span></span>

### <a name="method-bottommarginvalue"></a><span data-ttu-id="622ca-1966">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="622ca-1966">Method bottomMarginValue</span></span>

    public int bottomMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1967">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1967">Parameters</span></span>

<span data-ttu-id="622ca-1968">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1968">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1969">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1969">Return Value</span></span>

### <a name="method-cachedatamethod"></a><span data-ttu-id="622ca-1970">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="622ca-1970">Method cacheDataMethod</span></span>

    public int cacheDataMethod([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1971">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1971">Parameters</span></span>

<span data-ttu-id="622ca-1972">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1972">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1973">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1973">Return Value</span></span>

### <a name="method-calccontrolsize"></a><span data-ttu-id="622ca-1974">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="622ca-1974">Method calcControlSize</span></span>

<span data-ttu-id="622ca-1975">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1975">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="622ca-1976">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1976">Parameters</span></span>

<span data-ttu-id="622ca-1977">chars</span><span class="sxs-lookup"><span data-stu-id="622ca-1977">chars</span></span>  
<span data-ttu-id="622ca-1978">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="622ca-1978">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="622ca-1979">明細行</span><span class="sxs-lookup"><span data-stu-id="622ca-1979">lines</span></span>  
<span data-ttu-id="622ca-1980">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="622ca-1980">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-1981">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1981">Return Value</span></span>

<span data-ttu-id="622ca-1982">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="622ca-1982">The container that holds the width and height.</span></span>

### <a name="method-caption"></a><span data-ttu-id="622ca-1983">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="622ca-1983">Method caption</span></span>

<span data-ttu-id="622ca-1984">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1984">Gets or set the caption of the control.</span></span>

    public str caption([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1985">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1985">Parameters</span></span>

<span data-ttu-id="622ca-1986">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1986">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1987">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1987">Return Value</span></span>

<span data-ttu-id="622ca-1988">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-1988">The string that is used as the caption of the control.</span></span>

### <a name="method-characterset"></a><span data-ttu-id="622ca-1989">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="622ca-1989">Method characterSet</span></span>

<span data-ttu-id="622ca-1990">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1990">Gets or sets the character set of the font.</span></span>

    public int characterSet([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-1991">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-1991">Parameters</span></span>

<span data-ttu-id="622ca-1992">値</span><span class="sxs-lookup"><span data-stu-id="622ca-1992">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-1993">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-1993">Return Value</span></span>

<span data-ttu-id="622ca-1994">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-1994">An integer value that indicates the character set of the font.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-1995">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-1995">Remarks</span></span>

<span data-ttu-id="622ca-1996">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-1996">The values for the integer that is returned indicate the character set according to the following table.</span></span>

| <span data-ttu-id="622ca-1997">先頭値</span><span class="sxs-lookup"><span data-stu-id="622ca-1997">Value</span></span> | <span data-ttu-id="622ca-1998">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-1998">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="622ca-1999">0</span><span class="sxs-lookup"><span data-stu-id="622ca-1999">0</span></span>     | <span data-ttu-id="622ca-2000">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2000">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="622ca-2001">1</span><span class="sxs-lookup"><span data-stu-id="622ca-2001">1</span></span>     | <span data-ttu-id="622ca-2002">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2002">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="622ca-2003">2</span><span class="sxs-lookup"><span data-stu-id="622ca-2003">2</span></span>     | <span data-ttu-id="622ca-2004">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2004">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="622ca-2005">77</span><span class="sxs-lookup"><span data-stu-id="622ca-2005">77</span></span>    | <span data-ttu-id="622ca-2006">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2006">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="622ca-2007">128</span><span class="sxs-lookup"><span data-stu-id="622ca-2007">128</span></span>   | <span data-ttu-id="622ca-2008">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2008">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="622ca-2009">129</span><span class="sxs-lookup"><span data-stu-id="622ca-2009">129</span></span>   | <span data-ttu-id="622ca-2010">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2010">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="622ca-2011">134</span><span class="sxs-lookup"><span data-stu-id="622ca-2011">134</span></span>   | <span data-ttu-id="622ca-2012">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2012">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="622ca-2013">136</span><span class="sxs-lookup"><span data-stu-id="622ca-2013">136</span></span>   | <span data-ttu-id="622ca-2014">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2014">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="622ca-2015">161</span><span class="sxs-lookup"><span data-stu-id="622ca-2015">161</span></span>   | <span data-ttu-id="622ca-2016">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2016">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="622ca-2017">162</span><span class="sxs-lookup"><span data-stu-id="622ca-2017">162</span></span>   | <span data-ttu-id="622ca-2018">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2018">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="622ca-2019">163</span><span class="sxs-lookup"><span data-stu-id="622ca-2019">163</span></span>   | <span data-ttu-id="622ca-2020">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2020">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="622ca-2021">186</span><span class="sxs-lookup"><span data-stu-id="622ca-2021">186</span></span>   | <span data-ttu-id="622ca-2022">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2022">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="622ca-2023">204</span><span class="sxs-lookup"><span data-stu-id="622ca-2023">204</span></span>   | <span data-ttu-id="622ca-2024">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2024">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="622ca-2025">238</span><span class="sxs-lookup"><span data-stu-id="622ca-2025">238</span></span>   | <span data-ttu-id="622ca-2026">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2026">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="622ca-2027">255</span><span class="sxs-lookup"><span data-stu-id="622ca-2027">255</span></span>   | <span data-ttu-id="622ca-2028">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2028">OEM\_CHARSET</span></span>         |

<span data-ttu-id="622ca-2029">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2029">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="622ca-2030">金額</span><span class="sxs-lookup"><span data-stu-id="622ca-2030">Value</span></span> | <span data-ttu-id="622ca-2031">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-2031">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="622ca-2032">130</span><span class="sxs-lookup"><span data-stu-id="622ca-2032">130</span></span>   | <span data-ttu-id="622ca-2033">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2033">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="622ca-2034">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2034">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="622ca-2035">先頭値</span><span class="sxs-lookup"><span data-stu-id="622ca-2035">Value</span></span> | <span data-ttu-id="622ca-2036">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-2036">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="622ca-2037">177</span><span class="sxs-lookup"><span data-stu-id="622ca-2037">177</span></span>   | <span data-ttu-id="622ca-2038">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2038">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="622ca-2039">178</span><span class="sxs-lookup"><span data-stu-id="622ca-2039">178</span></span>   | <span data-ttu-id="622ca-2040">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2040">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="622ca-2041">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2041">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="622ca-2042">先頭値</span><span class="sxs-lookup"><span data-stu-id="622ca-2042">Value</span></span> | <span data-ttu-id="622ca-2043">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-2043">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="622ca-2044">222</span><span class="sxs-lookup"><span data-stu-id="622ca-2044">222</span></span>   | <span data-ttu-id="622ca-2045">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-2045">THAI\_CHARSET</span></span> |

<span data-ttu-id="622ca-2046">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2046">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="622ca-2047">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2047">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="622ca-2048">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="622ca-2048">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

### <a name="method-colorscheme"></a><span data-ttu-id="622ca-2049">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="622ca-2049">Method colorScheme</span></span>

<span data-ttu-id="622ca-2050">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2050">Gets or sets the color scheme of the control.</span></span>

    public int colorScheme([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2051">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2051">Parameters</span></span>

<span data-ttu-id="622ca-2052">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2052">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2053">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2053">Return Value</span></span>

<span data-ttu-id="622ca-2054">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-2054">An integer between zero and two, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2055">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2055">Remarks</span></span>

<span data-ttu-id="622ca-2056">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2056">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="622ca-2057">先頭値</span><span class="sxs-lookup"><span data-stu-id="622ca-2057">Value</span></span> | <span data-ttu-id="622ca-2058">スタイル</span><span class="sxs-lookup"><span data-stu-id="622ca-2058">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="622ca-2059">0</span><span class="sxs-lookup"><span data-stu-id="622ca-2059">0</span></span>     | <span data-ttu-id="622ca-2060">既定</span><span class="sxs-lookup"><span data-stu-id="622ca-2060">Default</span></span>               |
| <span data-ttu-id="622ca-2061">1</span><span class="sxs-lookup"><span data-stu-id="622ca-2061">1</span></span>     | <span data-ttu-id="622ca-2062">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="622ca-2062">The Windows palette</span></span>   |
| <span data-ttu-id="622ca-2063">2</span><span class="sxs-lookup"><span data-stu-id="622ca-2063">2</span></span>     | <span data-ttu-id="622ca-2064">真の配色</span><span class="sxs-lookup"><span data-stu-id="622ca-2064">The true-color scheme</span></span> |

### <a name="method-columns"></a><span data-ttu-id="622ca-2065">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="622ca-2065">Method columns</span></span>

    public int columns([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2066">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2066">Parameters</span></span>

<span data-ttu-id="622ca-2067">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2067">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2068">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2068">Return Value</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="622ca-2069">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="622ca-2069">Method configurationKey</span></span>

<span data-ttu-id="622ca-2070">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2070">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2071">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2071">Parameters</span></span>

<span data-ttu-id="622ca-2072">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2072">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2073">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2073">Return Value</span></span>

<span data-ttu-id="622ca-2074">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="622ca-2074">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2075">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2075">Remarks</span></span>

<span data-ttu-id="622ca-2076">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2076">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="622ca-2077">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2077">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="622ca-2078">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="622ca-2078">Method configurationKeyEx</span></span>

<span data-ttu-id="622ca-2079">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2079">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="622ca-2080">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2080">Return Value</span></span>

<span data-ttu-id="622ca-2081">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="622ca-2081">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2082">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2082">Remarks</span></span>

<span data-ttu-id="622ca-2083">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2083">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="622ca-2084">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2084">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="622ca-2085">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2085">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-count"></a><span data-ttu-id="622ca-2086">メソッド count</span><span class="sxs-lookup"><span data-stu-id="622ca-2086">Method count</span></span>

    public int count()

#### <a name="return-value"></a><span data-ttu-id="622ca-2087">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2087">Return Value</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="622ca-2088">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="622ca-2088">Method countryRegionCodes</span></span>

<span data-ttu-id="622ca-2089">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2089">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2090">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2090">Parameters</span></span>

<span data-ttu-id="622ca-2091">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2091">value</span></span>  
<span data-ttu-id="622ca-2092">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2092">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2093">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2093">Return Value</span></span>

<span data-ttu-id="622ca-2094">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="622ca-2094">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-countryregioncontextfield"></a><span data-ttu-id="622ca-2095">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="622ca-2095">Method countryRegionContextField</span></span>

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2096">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2096">Parameters</span></span>

<span data-ttu-id="622ca-2097">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2097">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2098">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2098">Return Value</span></span>

### <a name="method-datafield"></a><span data-ttu-id="622ca-2099">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="622ca-2099">Method dataField</span></span>

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2100">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2100">Parameters</span></span>

<span data-ttu-id="622ca-2101">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2101">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2102">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2102">Return Value</span></span>

### <a name="method-datamethod"></a><span data-ttu-id="622ca-2103">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="622ca-2103">Method dataMethod</span></span>

    public str dataMethod([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2104">Parameters</span></span>

<span data-ttu-id="622ca-2105">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2105">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2106">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2106">Return Value</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="622ca-2107">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="622ca-2107">Method dataRelationPath</span></span>

<span data-ttu-id="622ca-2108">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2108">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2109">Parameters</span></span>

<span data-ttu-id="622ca-2110">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2110">value</span></span>  
<span data-ttu-id="622ca-2111">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2111">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2112">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2112">Return Value</span></span>

<span data-ttu-id="622ca-2113">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="622ca-2113">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2114">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2114">Remarks</span></span>

<span data-ttu-id="622ca-2115">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2115">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="622ca-2116">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="622ca-2116">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-datasource"></a><span data-ttu-id="622ca-2117">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="622ca-2117">Method dataSource</span></span>

<span data-ttu-id="622ca-2118">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2118">Gets or sets a data source that will be used by the control or the form.</span></span>

    public int dataSource([AnyType value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2119">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2119">Parameters</span></span>

<span data-ttu-id="622ca-2120">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2120">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2121">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2121">Return Value</span></span>

<span data-ttu-id="622ca-2122">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="622ca-2122">The identifier of the data source that will be used.</span></span>

### <a name="method-displaylength"></a><span data-ttu-id="622ca-2123">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="622ca-2123">Method displayLength</span></span>

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2124">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2124">Parameters</span></span>

<span data-ttu-id="622ca-2125">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2125">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-2126">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2126">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2127">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2127">Return Value</span></span>

### <a name="method-displaylengthmode"></a><span data-ttu-id="622ca-2128">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2128">Method displayLengthMode</span></span>

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2129">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2129">Parameters</span></span>

<span data-ttu-id="622ca-2130">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2130">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2131">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2131">Return Value</span></span>

### <a name="method-displaylengthvalue"></a><span data-ttu-id="622ca-2132">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2132">Method displayLengthValue</span></span>

    public int displayLengthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2133">Parameters</span></span>

<span data-ttu-id="622ca-2134">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2134">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2135">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2135">Return Value</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="622ca-2136">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="622ca-2136">Method displayTarget</span></span>

<span data-ttu-id="622ca-2137">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2137">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2138">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2138">Parameters</span></span>

<span data-ttu-id="622ca-2139">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2139">value</span></span>  
<span data-ttu-id="622ca-2140">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2140">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2141">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2141">Return Value</span></span>

<span data-ttu-id="622ca-2142">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2142">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="622ca-2143">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="622ca-2143">Method dragDrop</span></span>

<span data-ttu-id="622ca-2144">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2144">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2145">Parameters</span></span>

<span data-ttu-id="622ca-2146">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2146">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2147">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2147">Return Value</span></span>

<span data-ttu-id="622ca-2148">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2148">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="622ca-2149">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="622ca-2149">Method dragOver</span></span>

<span data-ttu-id="622ca-2150">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2150">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-2151">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2151">Parameters</span></span>

<span data-ttu-id="622ca-2152">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-2152">dragSource</span></span>  
<span data-ttu-id="622ca-2153">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2153">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2154">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2154">dragMode</span></span>  
<span data-ttu-id="622ca-2155">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2155">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2156">x</span><span class="sxs-lookup"><span data-stu-id="622ca-2156">x</span></span>  
<span data-ttu-id="622ca-2157">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2157">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2158">y</span><span class="sxs-lookup"><span data-stu-id="622ca-2158">y</span></span>  
<span data-ttu-id="622ca-2159">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2159">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2160">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2160">Return Value</span></span>

<span data-ttu-id="622ca-2161">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2161">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="622ca-2162">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="622ca-2162">Method dragOverEx</span></span>

<span data-ttu-id="622ca-2163">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2163">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-2164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2164">Parameters</span></span>

<span data-ttu-id="622ca-2165">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-2165">dragSource</span></span>  
<span data-ttu-id="622ca-2166">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2166">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2167">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2167">dragMode</span></span>  
<span data-ttu-id="622ca-2168">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2168">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2169">x</span><span class="sxs-lookup"><span data-stu-id="622ca-2169">x</span></span>  
<span data-ttu-id="622ca-2170">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2170">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2171">y</span><span class="sxs-lookup"><span data-stu-id="622ca-2171">y</span></span>  
<span data-ttu-id="622ca-2172">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2172">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2173">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2173">Return Value</span></span>

<span data-ttu-id="622ca-2174">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2174">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="622ca-2175">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="622ca-2175">Method dragText</span></span>

<span data-ttu-id="622ca-2176">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2176">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="622ca-2177">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2177">Return Value</span></span>

<span data-ttu-id="622ca-2178">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-2178">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="622ca-2179">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="622ca-2179">Method enabled</span></span>

<span data-ttu-id="622ca-2180">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2180">Determines whether the object is enabled or disabled.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2181">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2181">Parameters</span></span>

<span data-ttu-id="622ca-2182">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2182">value</span></span>  
<span data-ttu-id="622ca-2183">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2183">A Boolean value that determines whether the control is enabled; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2184">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2184">Return Value</span></span>

<span data-ttu-id="622ca-2185">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2185">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2186">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2186">Remarks</span></span>

<span data-ttu-id="622ca-2187">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2187">The enabled property lets you enable or disable controls at run time.</span></span> <span data-ttu-id="622ca-2188">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2188">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="622ca-2189">また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2189">You can also disable a control that is used only for display purposes, such as an error message that provides read-only information.</span></span>

### <a name="method-enumtype"></a><span data-ttu-id="622ca-2190">メソッド enumType</span><span class="sxs-lookup"><span data-stu-id="622ca-2190">Method enumType</span></span>

    public EnumId enumType([EnumId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2191">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2191">Parameters</span></span>

<span data-ttu-id="622ca-2192">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2192">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2193">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2193">Return Value</span></span>

### <a name="method-enumtypevalue"></a><span data-ttu-id="622ca-2194">メソッド enumTypeValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2194">Method enumTypeValue</span></span>

    public EnumId enumTypeValue()

#### <a name="return-value"></a><span data-ttu-id="622ca-2195">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2195">Return Value</span></span>

### <a name="method-extendeddatatype"></a><span data-ttu-id="622ca-2196">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="622ca-2196">Method extendedDataType</span></span>

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2197">Parameters</span></span>

<span data-ttu-id="622ca-2198">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2198">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2199">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2199">Return Value</span></span>

### <a name="method-find"></a><span data-ttu-id="622ca-2200">メソッド find</span><span class="sxs-lookup"><span data-stu-id="622ca-2200">Method find</span></span>

    public int find(str string)

#### <a name="parameters"></a><span data-ttu-id="622ca-2201">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2201">Parameters</span></span>

<span data-ttu-id="622ca-2202">string</span><span class="sxs-lookup"><span data-stu-id="622ca-2202">string</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2203">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2203">Return Value</span></span>

### <a name="method-font"></a><span data-ttu-id="622ca-2204">メソッド font</span><span class="sxs-lookup"><span data-stu-id="622ca-2204">Method font</span></span>

<span data-ttu-id="622ca-2205">コントロールに使用されるフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2205">Gets or sets the name of the font that is used for the control.</span></span>

    public str font([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2206">Parameters</span></span>

<span data-ttu-id="622ca-2207">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2207">value</span></span>  
<span data-ttu-id="622ca-2208">コントロールのフォントとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2208">The value to assign as the font for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2209">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2209">Return Value</span></span>

<span data-ttu-id="622ca-2210">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-2210">The name of the font, such as Tahoma or Verdana.</span></span>

### <a name="method-fontsize"></a><span data-ttu-id="622ca-2211">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="622ca-2211">Method fontSize</span></span>

<span data-ttu-id="622ca-2212">コントロール内のテキストに使用されるフォント サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2212">Gets or sets the font size that is used for the control.</span></span>

    public int fontSize([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2213">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2213">Parameters</span></span>

<span data-ttu-id="622ca-2214">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2214">value</span></span>  
<span data-ttu-id="622ca-2215">コントロールのフォント サイズとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2215">The value to assign as the font size for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2216">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2216">Return Value</span></span>

<span data-ttu-id="622ca-2217">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-2217">The height of the font in points.</span></span>

### <a name="method-foregroundcolor"></a><span data-ttu-id="622ca-2218">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="622ca-2218">Method foregroundColor</span></span>

<span data-ttu-id="622ca-2219">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2219">Gets or sets the text color for the control to use.</span></span>

    public int foregroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2220">Parameters</span></span>

<span data-ttu-id="622ca-2221">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2221">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2222">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2222">Return Value</span></span>

<span data-ttu-id="622ca-2223">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-2223">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2224">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2224">Remarks</span></span>

<span data-ttu-id="622ca-2225">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2225">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="622ca-2226">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="622ca-2226">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="622ca-2227">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="622ca-2227">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="622ca-2228">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="622ca-2228">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="622ca-2229">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2229">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="622ca-2230">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2230">The maximum value for a single byte is 255.</span></span>

### <a name="method-frameposition"></a><span data-ttu-id="622ca-2231">メソッド framePosition</span><span class="sxs-lookup"><span data-stu-id="622ca-2231">Method framePosition</span></span>

    public int framePosition([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2232">Parameters</span></span>

<span data-ttu-id="622ca-2233">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2233">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2234">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2234">Return Value</span></span>

### <a name="method-frametype"></a><span data-ttu-id="622ca-2235">メソッド frameType</span><span class="sxs-lookup"><span data-stu-id="622ca-2235">Method frameType</span></span>

    public int frameType([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2236">Parameters</span></span>

<span data-ttu-id="622ca-2237">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2237">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2238">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2238">Return Value</span></span>

### <a name="method-gettext"></a><span data-ttu-id="622ca-2239">メソッド getText</span><span class="sxs-lookup"><span data-stu-id="622ca-2239">Method getText</span></span>

    public str getText(int index)

#### <a name="parameters"></a><span data-ttu-id="622ca-2240">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2240">Parameters</span></span>

<span data-ttu-id="622ca-2241">指数</span><span class="sxs-lookup"><span data-stu-id="622ca-2241">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2242">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2242">Return Value</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="622ca-2243">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-2243">Method hasChanged</span></span>

<span data-ttu-id="622ca-2244">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2244">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="622ca-2245">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2245">Parameters</span></span>

<span data-ttu-id="622ca-2246">val</span><span class="sxs-lookup"><span data-stu-id="622ca-2246">val</span></span>  
<span data-ttu-id="622ca-2247">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2247">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2248">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2248">Return Value</span></span>

<span data-ttu-id="622ca-2249">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2249">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="622ca-2250">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="622ca-2250">Method hasUserSetting</span></span>

<span data-ttu-id="622ca-2251">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2251">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="622ca-2252">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2252">Return Value</span></span>

<span data-ttu-id="622ca-2253">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2253">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="622ca-2254">メソッド height</span><span class="sxs-lookup"><span data-stu-id="622ca-2254">Method height</span></span>

<span data-ttu-id="622ca-2255">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2255">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2256">Parameters</span></span>

<span data-ttu-id="622ca-2257">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2257">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-2258">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2258">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2259">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2259">Return Value</span></span>

<span data-ttu-id="622ca-2260">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-2260">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2261">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2261">Remarks</span></span>

<span data-ttu-id="622ca-2262">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2262">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="622ca-2263">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2263">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="622ca-2264">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2264">Mode</span></span>            | <span data-ttu-id="622ca-2265">高さの計算</span><span class="sxs-lookup"><span data-stu-id="622ca-2265">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-2266">-1 正確</span><span class="sxs-lookup"><span data-stu-id="622ca-2266">-1 Exact</span></span>        | <span data-ttu-id="622ca-2267">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2267">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-2268">0 自動</span><span class="sxs-lookup"><span data-stu-id="622ca-2268">0 Auto</span></span>          | <span data-ttu-id="622ca-2269">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2269">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-2270">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="622ca-2270">1 Column height</span></span> | <span data-ttu-id="622ca-2271">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2271">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="622ca-2272">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2272">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="622ca-2273">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2273">Method heightMode</span></span>

<span data-ttu-id="622ca-2274">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2274">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2275">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2275">Parameters</span></span>

<span data-ttu-id="622ca-2276">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2276">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2277">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2277">Return Value</span></span>

<span data-ttu-id="622ca-2278">計算モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-2278">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2279">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2279">Remarks</span></span>

<span data-ttu-id="622ca-2280">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2280">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="622ca-2281">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2281">Mode</span></span>          | <span data-ttu-id="622ca-2282">高さの計算</span><span class="sxs-lookup"><span data-stu-id="622ca-2282">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-2283">正確</span><span class="sxs-lookup"><span data-stu-id="622ca-2283">Exact</span></span>         | <span data-ttu-id="622ca-2284">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2284">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-2285">自動</span><span class="sxs-lookup"><span data-stu-id="622ca-2285">Auto</span></span>          | <span data-ttu-id="622ca-2286">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2286">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-2287">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="622ca-2287">Column height</span></span> | <span data-ttu-id="622ca-2288">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2288">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="622ca-2289">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2289">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="622ca-2290">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2290">Method heightValue</span></span>

<span data-ttu-id="622ca-2291">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2291">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2292">Parameters</span></span>

<span data-ttu-id="622ca-2293">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2293">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2294">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2294">Return Value</span></span>

<span data-ttu-id="622ca-2295">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-2295">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2296">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2296">Remarks</span></span>

<span data-ttu-id="622ca-2297">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2297">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="622ca-2298">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="622ca-2298">Method helpField</span></span>

<span data-ttu-id="622ca-2299">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2299">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="622ca-2300">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2300">Return Value</span></span>

<span data-ttu-id="622ca-2301">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-2301">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2302">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2302">Remarks</span></span>

<span data-ttu-id="622ca-2303">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2303">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="622ca-2304">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2304">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="622ca-2305">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="622ca-2305">Method helpText</span></span>

<span data-ttu-id="622ca-2306">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2306">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2307">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2307">Parameters</span></span>

<span data-ttu-id="622ca-2308">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2308">value</span></span>  
<span data-ttu-id="622ca-2309">コントロールのヘルプ テキストとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2309">The value to assign as the Help text for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2310">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2310">Return Value</span></span>

<span data-ttu-id="622ca-2311">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-2311">The string that should be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2312">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2312">Remarks</span></span>

<span data-ttu-id="622ca-2313">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2313">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="622ca-2314">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2314">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hidefirstentry"></a><span data-ttu-id="622ca-2315">メソッド hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="622ca-2315">Method hideFirstEntry</span></span>

    public boolean hideFirstEntry([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2316">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2316">Parameters</span></span>

<span data-ttu-id="622ca-2317">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2317">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2318">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2318">Return Value</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="622ca-2319">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="622ca-2319">Method hierarchyParent</span></span>

<span data-ttu-id="622ca-2320">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2320">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2321">Parameters</span></span>

<span data-ttu-id="622ca-2322">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2322">value</span></span>  
<span data-ttu-id="622ca-2323">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2323">The value to assign to the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2324">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2324">Return Value</span></span>

<span data-ttu-id="622ca-2325">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2325">The HierarchyParent property value of the control.</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="622ca-2326">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="622ca-2326">Method hWnd</span></span>

<span data-ttu-id="622ca-2327">コントロールに関連付けられているウィンドウのハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2327">Returns the handle to the window that is associated with the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="622ca-2328">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2328">Return Value</span></span>

<span data-ttu-id="622ca-2329">コントロールに関連付けられているウィンドウのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="622ca-2329">The handle to the window that is associated with the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2330">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2330">Remarks</span></span>

<span data-ttu-id="622ca-2331">ウィンドウのハンドルは、Windows API 関数で使用できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2331">The handle to the window can be used with Windows API functions.</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="622ca-2332">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="622ca-2332">Method isContainer</span></span>

<span data-ttu-id="622ca-2333">コントロールがコンテナーかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2333">Gets a value that indicates whether the control is a container.</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="622ca-2334">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2334">Return Value</span></span>

<span data-ttu-id="622ca-2335">コントロールがコンテナーである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2335">true if the control is a container; otherwise, false.</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="622ca-2336">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="622ca-2336">Method isDisplayed</span></span>

<span data-ttu-id="622ca-2337">コントロールが表示されるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2337">Returns a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="622ca-2338">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2338">Return Value</span></span>

<span data-ttu-id="622ca-2339">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2339">true if the control is displayed; otherwise, false.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="622ca-2340">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="622ca-2340">Method isRestricted</span></span>

<span data-ttu-id="622ca-2341">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2341">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="622ca-2342">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2342">Return Value</span></span>

<span data-ttu-id="622ca-2343">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2343">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="622ca-2344">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="622ca-2344">Method isUserSetupEnabled</span></span>

<span data-ttu-id="622ca-2345">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2345">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="622ca-2346">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2346">Parameters</span></span>

<span data-ttu-id="622ca-2347">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="622ca-2347">neededSetupRights</span></span>  
<span data-ttu-id="622ca-2348">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2348">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2349">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2349">Return Value</span></span>

<span data-ttu-id="622ca-2350">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2350">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2351">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2351">Remarks</span></span>

<span data-ttu-id="622ca-2352">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2352">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span> <span data-ttu-id="622ca-2353">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2353">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-2354">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="622ca-2354">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="622ca-2355">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2355">No changes can be made to the control.</span></span> <span data-ttu-id="622ca-2356">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2356">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="622ca-2357">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="622ca-2357">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="622ca-2358">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2358">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="622ca-2359">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2359">The user cannot move the control.</span></span>   |
| <span data-ttu-id="622ca-2360">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="622ca-2360">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="622ca-2361">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2361">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="622ca-2362">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2362">The user can also move the control.</span></span> |

### <a name="method-isvalid"></a><span data-ttu-id="622ca-2363">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="622ca-2363">Method isValid</span></span>

    public boolean isValid()

#### <a name="return-value"></a><span data-ttu-id="622ca-2364">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2364">Return Value</span></span>

### <a name="method-italic"></a><span data-ttu-id="622ca-2365">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="622ca-2365">Method italic</span></span>

<span data-ttu-id="622ca-2366">コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2366">Sets or returns a value that indicates whether the text in the control is italic.</span></span>

    public boolean italic([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2367">Parameters</span></span>

<span data-ttu-id="622ca-2368">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2368">value</span></span>  
<span data-ttu-id="622ca-2369">コントロールの斜体設定の値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2369">The value for the control's italic setting; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2370">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2370">Return Value</span></span>

<span data-ttu-id="622ca-2371">コントロール内のテキストが斜体である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2371">true if the text in the control is italic; otherwise, false.</span></span>

### <a name="method-item"></a><span data-ttu-id="622ca-2372">メソッド item</span><span class="sxs-lookup"><span data-stu-id="622ca-2372">Method item</span></span>

    public int item([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2373">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2373">Parameters</span></span>

<span data-ttu-id="622ca-2374">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2374">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2375">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2375">Return Value</span></span>

### <a name="method-items"></a><span data-ttu-id="622ca-2376">メソッド items</span><span class="sxs-lookup"><span data-stu-id="622ca-2376">Method items</span></span>

    public int items([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2377">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2377">Parameters</span></span>

<span data-ttu-id="622ca-2378">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2378">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2379">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2379">Return Value</span></span>

### <a name="method-leave"></a><span data-ttu-id="622ca-2380">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="622ca-2380">Method leave</span></span>

    public boolean leave()

#### <a name="return-value"></a><span data-ttu-id="622ca-2381">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2381">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="622ca-2382">メソッド left</span><span class="sxs-lookup"><span data-stu-id="622ca-2382">Method left</span></span>

<span data-ttu-id="622ca-2383">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2383">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2384">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2384">Parameters</span></span>

<span data-ttu-id="622ca-2385">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2385">value</span></span>  
<span data-ttu-id="622ca-2386">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2386">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-2387">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2387">mode</span></span>  
<span data-ttu-id="622ca-2388">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2388">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2389">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2389">Return Value</span></span>

<span data-ttu-id="622ca-2390">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-2390">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmargin"></a><span data-ttu-id="622ca-2391">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="622ca-2391">Method leftMargin</span></span>

    public int leftMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2392">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2392">Parameters</span></span>

<span data-ttu-id="622ca-2393">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2393">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-2394">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2394">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2395">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2395">Return Value</span></span>

### <a name="method-leftmarginmode"></a><span data-ttu-id="622ca-2396">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2396">Method leftMarginMode</span></span>

    public AutoMode leftMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2397">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2397">Parameters</span></span>

<span data-ttu-id="622ca-2398">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2398">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2399">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2399">Return Value</span></span>

### <a name="method-leftmarginvalue"></a><span data-ttu-id="622ca-2400">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2400">Method leftMarginValue</span></span>

    public int leftMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2401">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2401">Parameters</span></span>

<span data-ttu-id="622ca-2402">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2402">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2403">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2403">Return Value</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="622ca-2404">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2404">Method leftMode</span></span>

<span data-ttu-id="622ca-2405">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2405">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2406">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2406">Parameters</span></span>

<span data-ttu-id="622ca-2407">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2407">value</span></span>  
<span data-ttu-id="622ca-2408">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2408">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2409">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2409">Return Value</span></span>

<span data-ttu-id="622ca-2410">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-2410">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="622ca-2411">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2411">Method leftValue</span></span>

<span data-ttu-id="622ca-2412">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2412">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2413">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2413">Parameters</span></span>

<span data-ttu-id="622ca-2414">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2414">value</span></span>  
<span data-ttu-id="622ca-2415">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2415">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2416">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2416">Return Value</span></span>

<span data-ttu-id="622ca-2417">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-2417">The horizontal position of the control in the form.</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="622ca-2418">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="622ca-2418">Method markAsUserAdd</span></span>

<span data-ttu-id="622ca-2419">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="622ca-2419">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2420">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2420">Parameters</span></span>

<span data-ttu-id="622ca-2421">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2421">value</span></span>  
<span data-ttu-id="622ca-2422">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2422">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2423">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2423">Return Value</span></span>

<span data-ttu-id="622ca-2424">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2424">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-modified"></a><span data-ttu-id="622ca-2425">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="622ca-2425">Method modified</span></span>

    public boolean modified()

#### <a name="return-value"></a><span data-ttu-id="622ca-2426">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2426">Return Value</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="622ca-2427">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="622ca-2427">Method mouseDblClick</span></span>

<span data-ttu-id="622ca-2428">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2428">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-2429">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2429">Parameters</span></span>

<span data-ttu-id="622ca-2430">x</span><span class="sxs-lookup"><span data-stu-id="622ca-2430">x</span></span>  
<span data-ttu-id="622ca-2431">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2431">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2432">y</span><span class="sxs-lookup"><span data-stu-id="622ca-2432">y</span></span>  
<span data-ttu-id="622ca-2433">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2433">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2434">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-2434">button</span></span>  
<span data-ttu-id="622ca-2435">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2435">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2436">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-2436">Ctrl</span></span>  
<span data-ttu-id="622ca-2437">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2437">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2438">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-2438">Shift</span></span>  
<span data-ttu-id="622ca-2439">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2439">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2440">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2440">Return Value</span></span>

<span data-ttu-id="622ca-2441">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2441">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2442">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2442">Remarks</span></span>

<span data-ttu-id="622ca-2443">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2443">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="622ca-2444">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="622ca-2444">Method mouseDown</span></span>

<span data-ttu-id="622ca-2445">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2445">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-2446">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2446">Parameters</span></span>

<span data-ttu-id="622ca-2447">x</span><span class="sxs-lookup"><span data-stu-id="622ca-2447">x</span></span>  
<span data-ttu-id="622ca-2448">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2448">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2449">y</span><span class="sxs-lookup"><span data-stu-id="622ca-2449">y</span></span>  
<span data-ttu-id="622ca-2450">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2450">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2451">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-2451">button</span></span>  
<span data-ttu-id="622ca-2452">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2452">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2453">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-2453">Ctrl</span></span>  
<span data-ttu-id="622ca-2454">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2454">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2455">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-2455">Shift</span></span>  
<span data-ttu-id="622ca-2456">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2456">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2457">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2457">Return Value</span></span>

<span data-ttu-id="622ca-2458">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2458">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2459">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2459">Remarks</span></span>

<span data-ttu-id="622ca-2460">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2460">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="622ca-2461">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2461">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="622ca-2462">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="622ca-2462">Method mouseMove</span></span>

<span data-ttu-id="622ca-2463">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2463">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-2464">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2464">Parameters</span></span>

<span data-ttu-id="622ca-2465">x</span><span class="sxs-lookup"><span data-stu-id="622ca-2465">x</span></span>  
<span data-ttu-id="622ca-2466">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2466">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2467">y</span><span class="sxs-lookup"><span data-stu-id="622ca-2467">y</span></span>  
<span data-ttu-id="622ca-2468">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2468">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2469">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-2469">button</span></span>  
<span data-ttu-id="622ca-2470">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2470">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2471">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-2471">Ctrl</span></span>  
<span data-ttu-id="622ca-2472">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2472">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2473">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-2473">Shift</span></span>  
<span data-ttu-id="622ca-2474">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2474">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2475">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2475">Return Value</span></span>

<span data-ttu-id="622ca-2476">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2476">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2477">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2477">Remarks</span></span>

<span data-ttu-id="622ca-2478">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2478">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="622ca-2479">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="622ca-2479">Method mouseUp</span></span>

<span data-ttu-id="622ca-2480">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2480">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-2481">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2481">Parameters</span></span>

<span data-ttu-id="622ca-2482">x</span><span class="sxs-lookup"><span data-stu-id="622ca-2482">x</span></span>  
<span data-ttu-id="622ca-2483">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2483">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2484">y</span><span class="sxs-lookup"><span data-stu-id="622ca-2484">y</span></span>  
<span data-ttu-id="622ca-2485">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2485">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2486">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-2486">button</span></span>  
<span data-ttu-id="622ca-2487">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2487">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2488">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-2488">Ctrl</span></span>  
<span data-ttu-id="622ca-2489">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2489">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2490">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-2490">Shift</span></span>  
<span data-ttu-id="622ca-2491">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2491">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2492">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2492">Return Value</span></span>

<span data-ttu-id="622ca-2493">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2493">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2494">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2494">Remarks</span></span>

<span data-ttu-id="622ca-2495">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2495">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="622ca-2496">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2496">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-name"></a><span data-ttu-id="622ca-2497">メソッド名</span><span class="sxs-lookup"><span data-stu-id="622ca-2497">Method name</span></span>

<span data-ttu-id="622ca-2498">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2498">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2499">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2499">Parameters</span></span>

<span data-ttu-id="622ca-2500">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2500">value</span></span>  
<span data-ttu-id="622ca-2501">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-2501">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2502">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2502">Return Value</span></span>

<span data-ttu-id="622ca-2503">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-2503">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2504">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2504">Remarks</span></span>

<span data-ttu-id="622ca-2505">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2505">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="622ca-2506">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2506">It must start with a letter.</span></span>
-   <span data-ttu-id="622ca-2507">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2507">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="622ca-2508">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2508">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="622ca-2509">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2509">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="622ca-2510">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2510">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="622ca-2511">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="622ca-2511">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2512">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2512">Parameters</span></span>

<span data-ttu-id="622ca-2513">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2513">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2514">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2514">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="622ca-2515">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="622ca-2515">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="622ca-2516">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2516">Return Value</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="622ca-2517">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="622ca-2517">Method parentControl</span></span>

<span data-ttu-id="622ca-2518">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2518">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="622ca-2519">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2519">Return Value</span></span>

<span data-ttu-id="622ca-2520">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="622ca-2520">The parent control for the control.</span></span>

### <a name="method-previewpartref"></a><span data-ttu-id="622ca-2521">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="622ca-2521">Method previewPartRef</span></span>

    public str previewPartRef([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2522">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2522">Parameters</span></span>

<span data-ttu-id="622ca-2523">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2523">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2524">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2524">Return Value</span></span>

### <a name="method-rightmargin"></a><span data-ttu-id="622ca-2525">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="622ca-2525">Method rightMargin</span></span>

    public int rightMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2526">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2526">Parameters</span></span>

<span data-ttu-id="622ca-2527">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2527">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-2528">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2528">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2529">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2529">Return Value</span></span>

### <a name="method-rightmarginmode"></a><span data-ttu-id="622ca-2530">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2530">Method rightMarginMode</span></span>

    public AutoMode rightMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2531">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2531">Parameters</span></span>

<span data-ttu-id="622ca-2532">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2532">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2533">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2533">Return Value</span></span>

### <a name="method-rightmarginvalue"></a><span data-ttu-id="622ca-2534">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2534">Method rightMarginValue</span></span>

    public int rightMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2535">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2535">Parameters</span></span>

<span data-ttu-id="622ca-2536">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2536">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2537">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2537">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="622ca-2538">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="622ca-2538">Method securityKey</span></span>

<span data-ttu-id="622ca-2539">コントロールに関連付けられているセキュリティ キーを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2539">Sets or returns the security key that is associated with the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2540">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2540">Parameters</span></span>

<span data-ttu-id="622ca-2541">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2541">value</span></span>  
<span data-ttu-id="622ca-2542">コントロールに関連付けられているセキュリティ キー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2542">The security key that is associated with the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2543">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2543">Return Value</span></span>

<span data-ttu-id="622ca-2544">コントロールに関連付けられているセキュリティ キー。</span><span class="sxs-lookup"><span data-stu-id="622ca-2544">The security key that is associated with the control.</span></span>

### <a name="method-selection"></a><span data-ttu-id="622ca-2545">メソッド selection</span><span class="sxs-lookup"><span data-stu-id="622ca-2545">Method selection</span></span>

    public int selection([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2546">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2546">Parameters</span></span>

<span data-ttu-id="622ca-2547">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2547">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2548">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2548">Return Value</span></span>

### <a name="method-selectionchange"></a><span data-ttu-id="622ca-2549">メソッド selectionChange</span><span class="sxs-lookup"><span data-stu-id="622ca-2549">Method selectionChange</span></span>

    public int selectionChange()

#### <a name="return-value"></a><span data-ttu-id="622ca-2550">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2550">Return Value</span></span>

### <a name="method-selecttext"></a><span data-ttu-id="622ca-2551">メソッド selectText</span><span class="sxs-lookup"><span data-stu-id="622ca-2551">Method selectText</span></span>

    public int selectText(str string)

#### <a name="parameters"></a><span data-ttu-id="622ca-2552">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2552">Parameters</span></span>

<span data-ttu-id="622ca-2553">string</span><span class="sxs-lookup"><span data-stu-id="622ca-2553">string</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2554">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2554">Return Value</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="622ca-2555">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="622ca-2555">Method showContextMenu</span></span>

<span data-ttu-id="622ca-2556">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2556">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="622ca-2557">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2557">Parameters</span></span>

<span data-ttu-id="622ca-2558">menuHandle</span><span class="sxs-lookup"><span data-stu-id="622ca-2558">menuHandle</span></span>  
<span data-ttu-id="622ca-2559">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="622ca-2559">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2560">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2560">Return Value</span></span>

<span data-ttu-id="622ca-2561">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2561">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-skip"></a><span data-ttu-id="622ca-2562">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="622ca-2562">Method skip</span></span>

<span data-ttu-id="622ca-2563">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2563">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2564">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2564">Parameters</span></span>

<span data-ttu-id="622ca-2565">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2565">value</span></span>  
<span data-ttu-id="622ca-2566">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2566">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2567">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2567">Return Value</span></span>

<span data-ttu-id="622ca-2568">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2568">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="method-sort"></a><span data-ttu-id="622ca-2569">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="622ca-2569">Method sort</span></span>

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a><span data-ttu-id="622ca-2570">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2570">Parameters</span></span>

<span data-ttu-id="622ca-2571">sortDirection</span><span class="sxs-lookup"><span data-stu-id="622ca-2571">sortDirection</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2572">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2572">Return Value</span></span>

### <a name="method-text"></a><span data-ttu-id="622ca-2573">メソッド text</span><span class="sxs-lookup"><span data-stu-id="622ca-2573">Method text</span></span>

<span data-ttu-id="622ca-2574">コントロールのテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2574">Sets or returns the text for the control.</span></span>

    public str text([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2575">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2575">Parameters</span></span>

<span data-ttu-id="622ca-2576">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2576">value</span></span>  
<span data-ttu-id="622ca-2577">コントロールに割り当てるテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2577">The text to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2578">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2578">Return Value</span></span>

<span data-ttu-id="622ca-2579">コントロールのテキスト。コントロールにテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-2579">The text for the control; an empty string if there is no text for the control.</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="622ca-2580">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="622ca-2580">Method toolTip</span></span>

<span data-ttu-id="622ca-2581">コントロールのツールヒント テキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2581">Sets or returns the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="622ca-2582">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2582">Return Value</span></span>

<span data-ttu-id="622ca-2583">コントロールのツールヒント テキスト。コントロールにツールヒント テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-2583">The tooltip text for the control; an empty string if there is no tooltip text for the control.</span></span>

### <a name="method-top"></a><span data-ttu-id="622ca-2584">メソッド top</span><span class="sxs-lookup"><span data-stu-id="622ca-2584">Method top</span></span>

<span data-ttu-id="622ca-2585">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2585">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2586">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2586">Parameters</span></span>

<span data-ttu-id="622ca-2587">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2587">value</span></span>  
<span data-ttu-id="622ca-2588">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2588">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-2589">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2589">mode</span></span>  
<span data-ttu-id="622ca-2590">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2590">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2591">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2591">Return Value</span></span>

<span data-ttu-id="622ca-2592">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-2592">The vertical position of the control in the form.</span></span>

### <a name="method-topmargin"></a><span data-ttu-id="622ca-2593">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="622ca-2593">Method topMargin</span></span>

    public int topMargin([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2594">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2594">Parameters</span></span>

<span data-ttu-id="622ca-2595">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2595">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-2596">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2596">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2597">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2597">Return Value</span></span>

### <a name="method-topmarginmode"></a><span data-ttu-id="622ca-2598">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2598">Method topMarginMode</span></span>

    public AutoMode topMarginMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2599">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2599">Parameters</span></span>

<span data-ttu-id="622ca-2600">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2600">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2601">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2601">Return Value</span></span>

### <a name="method-topmarginvalue"></a><span data-ttu-id="622ca-2602">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2602">Method topMarginValue</span></span>

    public int topMarginValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2603">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2603">Parameters</span></span>

<span data-ttu-id="622ca-2604">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2604">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2605">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2605">Return Value</span></span>

### <a name="method-topmode"></a><span data-ttu-id="622ca-2606">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2606">Method topMode</span></span>

<span data-ttu-id="622ca-2607">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2607">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2608">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2608">Parameters</span></span>

<span data-ttu-id="622ca-2609">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2609">value</span></span>  
<span data-ttu-id="622ca-2610">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2610">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2611">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2611">Return Value</span></span>

<span data-ttu-id="622ca-2612">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-2612">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="622ca-2613">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2613">Method topValue</span></span>

<span data-ttu-id="622ca-2614">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2614">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2615">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2615">Parameters</span></span>

<span data-ttu-id="622ca-2616">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2616">value</span></span>  
<span data-ttu-id="622ca-2617">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2617">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2618">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2618">Return Value</span></span>

<span data-ttu-id="622ca-2619">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-2619">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="622ca-2620">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="622ca-2620">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2621">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2621">Parameters</span></span>

<span data-ttu-id="622ca-2622">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2622">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2623">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2623">Return Value</span></span>

### <a name="method-underline"></a><span data-ttu-id="622ca-2624">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="622ca-2624">Method underline</span></span>

<span data-ttu-id="622ca-2625">コントロール内のテキストの下線プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2625">Sets or returns the value of the underline property for the text in the control.</span></span>

    public boolean underline([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2626">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2626">Parameters</span></span>

<span data-ttu-id="622ca-2627">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2627">value</span></span>  
<span data-ttu-id="622ca-2628">コントロールに対する underline プロパティの値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2628">The value of the underline property for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2629">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2629">Return Value</span></span>

<span data-ttu-id="622ca-2630">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2630">true if the text in the control is underlined; otherwise, false.</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="622ca-2631">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="622ca-2631">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="622ca-2632">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2632">Parameters</span></span>

<span data-ttu-id="622ca-2633">データ</span><span class="sxs-lookup"><span data-stu-id="622ca-2633">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2634">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2634">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="622ca-2635">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="622ca-2635">Method userData</span></span>

<span data-ttu-id="622ca-2636">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2636">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2637">Parameters</span></span>

<span data-ttu-id="622ca-2638">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2638">value</span></span>  
<span data-ttu-id="622ca-2639">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2639">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2640">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2640">Return Value</span></span>

<span data-ttu-id="622ca-2641">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="622ca-2641">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="622ca-2642">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="622ca-2642">Method userDataItem</span></span>

<span data-ttu-id="622ca-2643">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2643">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2644">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2644">Parameters</span></span>

<span data-ttu-id="622ca-2645">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2645">value</span></span>  
<span data-ttu-id="622ca-2646">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2646">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2647">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2647">Return Value</span></span>

<span data-ttu-id="622ca-2648">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="622ca-2648">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="622ca-2649">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="622ca-2649">Method userDataItems</span></span>

<span data-ttu-id="622ca-2650">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2650">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2651">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2651">Parameters</span></span>

<span data-ttu-id="622ca-2652">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2652">value</span></span>  
<span data-ttu-id="622ca-2653">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2653">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2654">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2654">Return Value</span></span>

<span data-ttu-id="622ca-2655">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="622ca-2655">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="622ca-2656">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="622ca-2656">Method userDisable</span></span>

<span data-ttu-id="622ca-2657">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2657">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2658">Parameters</span></span>

<span data-ttu-id="622ca-2659">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2659">value</span></span>  
<span data-ttu-id="622ca-2660">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2660">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2661">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2661">Return Value</span></span>

<span data-ttu-id="622ca-2662">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2662">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userheight"></a><span data-ttu-id="622ca-2663">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="622ca-2663">Method userHeight</span></span>

<span data-ttu-id="622ca-2664">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2664">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2665">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2665">Parameters</span></span>

<span data-ttu-id="622ca-2666">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2666">value</span></span>  
<span data-ttu-id="622ca-2667">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2667">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2668">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2668">Return Value</span></span>

<span data-ttu-id="622ca-2669">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-2669">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="622ca-2670">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="622ca-2670">Method userHide</span></span>

<span data-ttu-id="622ca-2671">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2671">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2672">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2672">Parameters</span></span>

<span data-ttu-id="622ca-2673">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2673">value</span></span>  
<span data-ttu-id="622ca-2674">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2674">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2675">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2675">Return Value</span></span>

<span data-ttu-id="622ca-2676">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2676">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2677">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2677">Remarks</span></span>

<span data-ttu-id="622ca-2678">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2678">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="622ca-2679">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2679">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="622ca-2680">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2680">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="622ca-2681">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="622ca-2681">Method userOrgContainer</span></span>

<span data-ttu-id="622ca-2682">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2682">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2683">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2683">Parameters</span></span>

<span data-ttu-id="622ca-2684">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2684">value</span></span>  
<span data-ttu-id="622ca-2685">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2685">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2686">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2686">Return Value</span></span>

<span data-ttu-id="622ca-2687">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="622ca-2687">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="622ca-2688">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="622ca-2688">Method userOrgSibling</span></span>

<span data-ttu-id="622ca-2689">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2689">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2690">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2690">Parameters</span></span>

<span data-ttu-id="622ca-2691">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2691">value</span></span>  
<span data-ttu-id="622ca-2692">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2692">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2693">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2693">Return Value</span></span>

<span data-ttu-id="622ca-2694">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="622ca-2694">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="622ca-2695">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="622ca-2695">Method userPromptText</span></span>

<span data-ttu-id="622ca-2696">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2696">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2697">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2697">Parameters</span></span>

<span data-ttu-id="622ca-2698">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2698">value</span></span>  
<span data-ttu-id="622ca-2699">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2699">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2700">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2700">Return Value</span></span>

<span data-ttu-id="622ca-2701">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="622ca-2701">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="622ca-2702">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="622ca-2702">Method userSecurityLevel</span></span>

<span data-ttu-id="622ca-2703">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2703">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2704">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2704">Parameters</span></span>

<span data-ttu-id="622ca-2705">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2705">value</span></span>  
<span data-ttu-id="622ca-2706">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2706">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2707">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2707">Return Value</span></span>

<span data-ttu-id="622ca-2708">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="622ca-2708">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="622ca-2709">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="622ca-2709">Method userSkip</span></span>

<span data-ttu-id="622ca-2710">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2710">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2711">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2711">Parameters</span></span>

<span data-ttu-id="622ca-2712">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2712">value</span></span>  
<span data-ttu-id="622ca-2713">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2713">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="622ca-2714">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2714">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2715">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2715">Return Value</span></span>

<span data-ttu-id="622ca-2716">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-2716">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="622ca-2717">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="622ca-2717">Method userWidth</span></span>

<span data-ttu-id="622ca-2718">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2718">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2719">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2719">Parameters</span></span>

<span data-ttu-id="622ca-2720">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2720">value</span></span>  
<span data-ttu-id="622ca-2721">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2721">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2722">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2722">Return Value</span></span>

<span data-ttu-id="622ca-2723">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2723">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2724">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2724">Remarks</span></span>

<span data-ttu-id="622ca-2725">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2725">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="622ca-2726">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2726">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="622ca-2727">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2727">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-validate"></a><span data-ttu-id="622ca-2728">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="622ca-2728">Method validate</span></span>

    public boolean validate()

#### <a name="return-value"></a><span data-ttu-id="622ca-2729">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2729">Return Value</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="622ca-2730">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="622ca-2730">Method verticalSpacing</span></span>

<span data-ttu-id="622ca-2731">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2731">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2732">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2732">Parameters</span></span>

<span data-ttu-id="622ca-2733">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2733">value</span></span>  
<span data-ttu-id="622ca-2734">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2734">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-2735">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2735">mode</span></span>  
<span data-ttu-id="622ca-2736">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2736">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2737">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2737">Return Value</span></span>

<span data-ttu-id="622ca-2738">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="622ca-2738">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="622ca-2739">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2739">Method verticalSpacingMode</span></span>

<span data-ttu-id="622ca-2740">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2740">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2741">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2741">Parameters</span></span>

<span data-ttu-id="622ca-2742">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2742">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2743">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2743">Return Value</span></span>

<span data-ttu-id="622ca-2744">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-2744">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="622ca-2745">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2745">Method verticalSpacingValue</span></span>

<span data-ttu-id="622ca-2746">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2746">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2747">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2747">Parameters</span></span>

<span data-ttu-id="622ca-2748">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2748">value</span></span>  
<span data-ttu-id="622ca-2749">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-2749">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2750">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2750">Return Value</span></span>

<span data-ttu-id="622ca-2751">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="622ca-2751">The vertical spacing of the control in the form.</span></span>

### <a name="method-vieweditmode"></a><span data-ttu-id="622ca-2752">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2752">Method viewEditMode</span></span>

    public int viewEditMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2753">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2753">Parameters</span></span>

<span data-ttu-id="622ca-2754">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2754">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2755">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2755">Return Value</span></span>

### <a name="method-visible"></a><span data-ttu-id="622ca-2756">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="622ca-2756">Method visible</span></span>

<span data-ttu-id="622ca-2757">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2757">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2758">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2758">Parameters</span></span>

<span data-ttu-id="622ca-2759">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2759">value</span></span>  
<span data-ttu-id="622ca-2760">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2760">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-2761">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2761">Return Value</span></span>

<span data-ttu-id="622ca-2762">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-2762">true if the control is visible; otherwise, false.</span></span>

### <a name="method-width"></a><span data-ttu-id="622ca-2763">メソッド width</span><span class="sxs-lookup"><span data-stu-id="622ca-2763">Method width</span></span>

<span data-ttu-id="622ca-2764">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2764">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-2765">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2765">Parameters</span></span>

<span data-ttu-id="622ca-2766">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2766">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-2767">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2767">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2768">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2768">Return Value</span></span>

<span data-ttu-id="622ca-2769">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="622ca-2769">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2770">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2770">Remarks</span></span>

<span data-ttu-id="622ca-2771">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2771">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="622ca-2772">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2772">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="622ca-2773">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2773">Mode</span></span>           | <span data-ttu-id="622ca-2774">幅計算</span><span class="sxs-lookup"><span data-stu-id="622ca-2774">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-2775">-1 正確</span><span class="sxs-lookup"><span data-stu-id="622ca-2775">-1 Exact</span></span>       | <span data-ttu-id="622ca-2776">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2776">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-2777">0 自動</span><span class="sxs-lookup"><span data-stu-id="622ca-2777">0 Auto</span></span>         | <span data-ttu-id="622ca-2778">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2778">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-2779">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="622ca-2779">1 Column width</span></span> | <span data-ttu-id="622ca-2780">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2780">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="622ca-2781">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2781">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="622ca-2782">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2782">Method widthMode</span></span>

<span data-ttu-id="622ca-2783">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2783">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2784">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2784">Parameters</span></span>

<span data-ttu-id="622ca-2785">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2785">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2786">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2786">Return Value</span></span>

<span data-ttu-id="622ca-2787">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2787">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2788">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2788">Remarks</span></span>

<span data-ttu-id="622ca-2789">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="622ca-2789">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="622ca-2790">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-2790">Mode</span></span>         | <span data-ttu-id="622ca-2791">幅計算</span><span class="sxs-lookup"><span data-stu-id="622ca-2791">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-2792">正確</span><span class="sxs-lookup"><span data-stu-id="622ca-2792">Exact</span></span>        | <span data-ttu-id="622ca-2793">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2793">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-2794">自動</span><span class="sxs-lookup"><span data-stu-id="622ca-2794">Auto</span></span>         | <span data-ttu-id="622ca-2795">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2795">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-2796">列の幅</span><span class="sxs-lookup"><span data-stu-id="622ca-2796">Column width</span></span> | <span data-ttu-id="622ca-2797">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2797">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="622ca-2798">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="622ca-2798">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="622ca-2799">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="622ca-2799">Method widthValue</span></span>

<span data-ttu-id="622ca-2800">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2800">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-2801">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2801">Parameters</span></span>

<span data-ttu-id="622ca-2802">値</span><span class="sxs-lookup"><span data-stu-id="622ca-2802">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-2803">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-2803">Return Value</span></span>

<span data-ttu-id="622ca-2804">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="622ca-2804">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-2805">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2805">Remarks</span></span>

<span data-ttu-id="622ca-2806">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2806">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-onleaving"></a><span data-ttu-id="622ca-2807">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="622ca-2807">Method OnLeaving</span></span>

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2808">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2808">Parameters</span></span>

<span data-ttu-id="622ca-2809">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2809">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2810">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2810">e</span></span>  

### <a name="method-filter"></a><span data-ttu-id="622ca-2811">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="622ca-2811">Method filter</span></span>

    public void filter([str filterStr])

#### <a name="parameters"></a><span data-ttu-id="622ca-2812">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2812">Parameters</span></span>

<span data-ttu-id="622ca-2813">filterStr</span><span class="sxs-lookup"><span data-stu-id="622ca-2813">filterStr</span></span>  

### <a name="method-mouseenter"></a><span data-ttu-id="622ca-2814">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="622ca-2814">Method mouseEnter</span></span>

<span data-ttu-id="622ca-2815">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2815">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-2816">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2816">Parameters</span></span>

<span data-ttu-id="622ca-2817">x</span><span class="sxs-lookup"><span data-stu-id="622ca-2817">x</span></span>  
<span data-ttu-id="622ca-2818">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2818">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2819">y</span><span class="sxs-lookup"><span data-stu-id="622ca-2819">y</span></span>  
<span data-ttu-id="622ca-2820">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2820">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2821">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-2821">button</span></span>  
<span data-ttu-id="622ca-2822">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2822">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2823">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-2823">Ctrl</span></span>  
<span data-ttu-id="622ca-2824">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2824">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-2825">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-2825">Shift</span></span>  
<span data-ttu-id="622ca-2826">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2826">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-setfocus"></a><span data-ttu-id="622ca-2827">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-2827">Method setFocus</span></span>

<span data-ttu-id="622ca-2828">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2828">Sets the focus on the control.</span></span>

    public void setFocus()

### <a name="method-insert"></a><span data-ttu-id="622ca-2829">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="622ca-2829">Method insert</span></span>

    public void insert(str string, int index)

#### <a name="parameters"></a><span data-ttu-id="622ca-2830">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2830">Parameters</span></span>

<span data-ttu-id="622ca-2831">string</span><span class="sxs-lookup"><span data-stu-id="622ca-2831">string</span></span>  

<!-- -->

<span data-ttu-id="622ca-2832">指数</span><span class="sxs-lookup"><span data-stu-id="622ca-2832">index</span></span>  

### <a name="method-onselectionchanged"></a><span data-ttu-id="622ca-2833">メソッド OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-2833">Method OnSelectionChanged</span></span>

    private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2834">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2834">Parameters</span></span>

<span data-ttu-id="622ca-2835">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2835">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2836">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2836">e</span></span>  

### <a name="method-delete"></a><span data-ttu-id="622ca-2837">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="622ca-2837">Method delete</span></span>

    public void delete(str string)

#### <a name="parameters"></a><span data-ttu-id="622ca-2838">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2838">Parameters</span></span>

<span data-ttu-id="622ca-2839">string</span><span class="sxs-lookup"><span data-stu-id="622ca-2839">string</span></span>  

### <a name="method-prefcolumnsize"></a><span data-ttu-id="622ca-2840">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="622ca-2840">Method prefColumnSize</span></span>

<span data-ttu-id="622ca-2841">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2841">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="622ca-2842">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2842">Parameters</span></span>

<span data-ttu-id="622ca-2843">width</span><span class="sxs-lookup"><span data-stu-id="622ca-2843">width</span></span>  
<span data-ttu-id="622ca-2844">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="622ca-2844">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="622ca-2845">height</span><span class="sxs-lookup"><span data-stu-id="622ca-2845">height</span></span>  
<span data-ttu-id="622ca-2846">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="622ca-2846">The preferred height of the control.</span></span>

### <a name="method-onlookup"></a><span data-ttu-id="622ca-2847">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="622ca-2847">Method OnLookup</span></span>

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2848">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2848">Parameters</span></span>

<span data-ttu-id="622ca-2849">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2849">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2850">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2850">e</span></span>  

### <a name="method-jumpref"></a><span data-ttu-id="622ca-2851">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="622ca-2851">Method jumpRef</span></span>

    public void jumpRef()

### <a name="method-endupdate"></a><span data-ttu-id="622ca-2852">メソッド endUpdate</span><span class="sxs-lookup"><span data-stu-id="622ca-2852">Method endUpdate</span></span>

    public void endUpdate()

### <a name="method-cut"></a><span data-ttu-id="622ca-2853">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="622ca-2853">Method cut</span></span>

<span data-ttu-id="622ca-2854">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="622ca-2854">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-resetusersetting"></a><span data-ttu-id="622ca-2855">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="622ca-2855">Method resetUserSetting</span></span>

<span data-ttu-id="622ca-2856">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="622ca-2856">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-dropex"></a><span data-ttu-id="622ca-2857">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="622ca-2857">Method dropEx</span></span>

<span data-ttu-id="622ca-2858">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2858">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-2859">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2859">Parameters</span></span>

<span data-ttu-id="622ca-2860">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-2860">dragSource</span></span>  
<span data-ttu-id="622ca-2861">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2861">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2862">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2862">dragMode</span></span>  
<span data-ttu-id="622ca-2863">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2863">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2864">x</span><span class="sxs-lookup"><span data-stu-id="622ca-2864">x</span></span>  
<span data-ttu-id="622ca-2865">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2865">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2866">y</span><span class="sxs-lookup"><span data-stu-id="622ca-2866">y</span></span>  
<span data-ttu-id="622ca-2867">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2867">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-lostfocus"></a><span data-ttu-id="622ca-2868">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-2868">Method lostFocus</span></span>

<span data-ttu-id="622ca-2869">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2869">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-onvalidated"></a><span data-ttu-id="622ca-2870">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="622ca-2870">Method OnValidated</span></span>

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2871">Parameters</span></span>

<span data-ttu-id="622ca-2872">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2872">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2873">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2873">e</span></span>  

### <a name="method-onmodified"></a><span data-ttu-id="622ca-2874">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="622ca-2874">Method OnModified</span></span>

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2875">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2875">Parameters</span></span>

<span data-ttu-id="622ca-2876">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2876">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2877">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2877">e</span></span>  

### <a name="method-displaycontrol"></a><span data-ttu-id="622ca-2878">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="622ca-2878">Method displayControl</span></span>

<span data-ttu-id="622ca-2879">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2879">Displays the control.</span></span>

    public void displayControl()

### <a name="method-ongotfocus"></a><span data-ttu-id="622ca-2880">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-2880">Method OnGotFocus</span></span>

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2881">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2881">Parameters</span></span>

<span data-ttu-id="622ca-2882">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2882">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2883">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2883">e</span></span>  

### <a name="method-mouseleave"></a><span data-ttu-id="622ca-2884">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="622ca-2884">Method mouseLeave</span></span>

<span data-ttu-id="622ca-2885">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2885">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-dragleave"></a><span data-ttu-id="622ca-2886">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="622ca-2886">Method dragLeave</span></span>

<span data-ttu-id="622ca-2887">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2887">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

### <a name="method-add"></a><span data-ttu-id="622ca-2888">メソッド add</span><span class="sxs-lookup"><span data-stu-id="622ca-2888">Method add</span></span>

    public void add(str string)

#### <a name="parameters"></a><span data-ttu-id="622ca-2889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2889">Parameters</span></span>

<span data-ttu-id="622ca-2890">string</span><span class="sxs-lookup"><span data-stu-id="622ca-2890">string</span></span>  

### <a name="method-context"></a><span data-ttu-id="622ca-2891">メソッド context</span><span class="sxs-lookup"><span data-stu-id="622ca-2891">Method context</span></span>

<span data-ttu-id="622ca-2892">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2892">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-onselectionchanging"></a><span data-ttu-id="622ca-2893">メソッド OnSelectionChanging</span><span class="sxs-lookup"><span data-stu-id="622ca-2893">Method OnSelectionChanging</span></span>

    private void OnSelectionChanging([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2894">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2894">Parameters</span></span>

<span data-ttu-id="622ca-2895">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2895">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2896">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2896">e</span></span>  

### <a name="method-beginupdate"></a><span data-ttu-id="622ca-2897">メソッド beginUpdate</span><span class="sxs-lookup"><span data-stu-id="622ca-2897">Method beginUpdate</span></span>

    public void beginUpdate()

### <a name="method-onlostfocus"></a><span data-ttu-id="622ca-2898">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-2898">Method OnLostFocus</span></span>

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2899">Parameters</span></span>

<span data-ttu-id="622ca-2900">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2900">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2901">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2901">e</span></span>  

### <a name="method-enter"></a><span data-ttu-id="622ca-2902">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="622ca-2902">Method enter</span></span>

    public void enter()

### <a name="method-inputsearch"></a><span data-ttu-id="622ca-2903">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="622ca-2903">Method inputSearch</span></span>

<span data-ttu-id="622ca-2904">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2904">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="622ca-2905">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2905">Parameters</span></span>

<span data-ttu-id="622ca-2906">searchStr</span><span class="sxs-lookup"><span data-stu-id="622ca-2906">searchStr</span></span>  
<span data-ttu-id="622ca-2907">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-2907">The string value to use to filter data; optional.</span></span>

### <a name="method-onenter"></a><span data-ttu-id="622ca-2908">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="622ca-2908">Method OnEnter</span></span>

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2909">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2909">Parameters</span></span>

<span data-ttu-id="622ca-2910">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2910">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2911">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2911">e</span></span>  

### <a name="method-gotfocus"></a><span data-ttu-id="622ca-2912">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-2912">Method gotFocus</span></span>

<span data-ttu-id="622ca-2913">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2913">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-clear"></a><span data-ttu-id="622ca-2914">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="622ca-2914">Method clear</span></span>

    public void clear()

### <a name="method-paste"></a><span data-ttu-id="622ca-2915">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="622ca-2915">Method paste</span></span>

<span data-ttu-id="622ca-2916">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2916">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-lookup"></a><span data-ttu-id="622ca-2917">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="622ca-2917">Method lookup</span></span>

    public void lookup()

### <a name="method-registeroverridemethod"></a><span data-ttu-id="622ca-2918">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="622ca-2918">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="622ca-2919">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2919">Parameters</span></span>

<span data-ttu-id="622ca-2920">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="622ca-2920">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="622ca-2921">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="622ca-2921">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="622ca-2922">overrideObject</span><span class="sxs-lookup"><span data-stu-id="622ca-2922">overrideObject</span></span>  

### <a name="method-drop"></a><span data-ttu-id="622ca-2923">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="622ca-2923">Method drop</span></span>

<span data-ttu-id="622ca-2924">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2924">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-2925">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2925">Parameters</span></span>

<span data-ttu-id="622ca-2926">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-2926">dragSource</span></span>  
<span data-ttu-id="622ca-2927">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2927">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2928">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-2928">dragMode</span></span>  
<span data-ttu-id="622ca-2929">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2929">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2930">x</span><span class="sxs-lookup"><span data-stu-id="622ca-2930">x</span></span>  
<span data-ttu-id="622ca-2931">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2931">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-2932">y</span><span class="sxs-lookup"><span data-stu-id="622ca-2932">y</span></span>  
<span data-ttu-id="622ca-2933">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-2933">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-onvalidating"></a><span data-ttu-id="622ca-2934">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="622ca-2934">Method OnValidating</span></span>

    private void OnValidating([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-2935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-2935">Parameters</span></span>

<span data-ttu-id="622ca-2936">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-2936">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-2937">e</span><span class="sxs-lookup"><span data-stu-id="622ca-2937">e</span></span>  

### <a name="method-undo"></a><span data-ttu-id="622ca-2938">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="622ca-2938">Method undo</span></span>

    public void undo()

### <a name="method-copy"></a><span data-ttu-id="622ca-2939">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="622ca-2939">Method copy</span></span>

<span data-ttu-id="622ca-2940">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="622ca-2940">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-enddrag"></a><span data-ttu-id="622ca-2941">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="622ca-2941">Method endDrag</span></span>

<span data-ttu-id="622ca-2942">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2942">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="622ca-2943">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2943">Remarks</span></span>

<span data-ttu-id="622ca-2944">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="622ca-2944">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="622ca-2945">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2945">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="class-formrealcontrol"></a><span data-ttu-id="622ca-2946">クラス FormRealControl</span><span class="sxs-lookup"><span data-stu-id="622ca-2946">Class FormRealControl</span></span>
    class FormRealControl extends FormControl

### <a name="remarks"></a><span data-ttu-id="622ca-2947">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-2947">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="622ca-2948">例</span><span class="sxs-lookup"><span data-stu-id="622ca-2948">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="622ca-2949">メソッド</span><span class="sxs-lookup"><span data-stu-id="622ca-2949">Methods</span></span>

| <span data-ttu-id="622ca-2950">方法</span><span class="sxs-lookup"><span data-stu-id="622ca-2950">Method</span></span>                                                                                                      | <span data-ttu-id="622ca-2951">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-2951">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-2952">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2952">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="622ca-2953">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2953">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-2954">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2954">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2955">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2955">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="622ca-2956">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2956">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="622ca-2957">public int allowNegative(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2957">public int allowNegative(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2958">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="622ca-2958">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="622ca-2959">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2959">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="622ca-2960">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2960">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2961">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2961">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="622ca-2962">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2962">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="622ca-2963">public int autoInsSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2963">public int autoInsSeparator(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2964">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2964">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="622ca-2965">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2965">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="622ca-2966">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2966">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-2967">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2967">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-2968">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-2968">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="622ca-2969">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-2969">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-2970">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2970">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="622ca-2971">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2971">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                                             |
| <span data-ttu-id="622ca-2972">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2972">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="622ca-2973">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2973">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="622ca-2974">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2974">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2975">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="622ca-2975">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="622ca-2976">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2976">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="622ca-2977">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2977">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="622ca-2978">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2978">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="622ca-2979">public int charFromPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-2979">public int charFromPos(int x, int y)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2980">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2980">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="622ca-2981">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2981">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="622ca-2982">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2982">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="622ca-2983">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2983">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="622ca-2984">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="622ca-2984">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="622ca-2985">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2985">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="622ca-2986">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2986">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="622ca-2987">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2987">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="622ca-2988">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2988">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2989">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2989">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2990">public int dataFieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="622ca-2990">public int dataFieldArrayIndex()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2991">public FieldName dataFieldName()</span><span class="sxs-lookup"><span data-stu-id="622ca-2991">public FieldName dataFieldName()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2992">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2992">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2993">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2993">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="622ca-2994">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2994">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="622ca-2995">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2995">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="622ca-2996">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-2996">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                |
| <span data-ttu-id="622ca-2997">public int decimalSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2997">public int decimalSeparator(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2998">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2998">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-2999">public int displaceNegative(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-2999">public int displaceNegative(\[int value\], \[AutoMode mode\])</span></span>                                               |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3000">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3000">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3001">public int displaceNegativeValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3001">public int displaceNegativeValue(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3002">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3002">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3003">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3003">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3004">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3004">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3005">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3005">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3006">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3006">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3007">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3007">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3008">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3008">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="622ca-3009">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3009">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="622ca-3010">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3010">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-3011">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3011">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                        |
| <span data-ttu-id="622ca-3012">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-3012">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="622ca-3013">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3013">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="622ca-3014">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-3014">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="622ca-3015">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3015">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="622ca-3016">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="622ca-3016">public str dragText()</span></span>                                                                                       | <span data-ttu-id="622ca-3017">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3017">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="622ca-3018">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3018">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="622ca-3019">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3019">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="622ca-3020">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3020">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3021">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3021">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3022">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3022">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="622ca-3023">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3023">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="622ca-3024">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3024">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-3025">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3025">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="622ca-3026">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3026">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="622ca-3027">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3027">Gets or sets the text color for the control to use.</span></span>                                                                                                                     |
| <span data-ttu-id="622ca-3028">public int formatMST(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3028">public int formatMST(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3029">public container getCursorPos()</span><span class="sxs-lookup"><span data-stu-id="622ca-3029">public container getCursorPos()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3030">public int getFirstVisibleLine()</span><span class="sxs-lookup"><span data-stu-id="622ca-3030">public int getFirstVisibleLine()</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3031">public str getLine(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="622ca-3031">public str getLine(int lineNo)</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3032">public int getLineCount()</span><span class="sxs-lookup"><span data-stu-id="622ca-3032">public int getLineCount()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3033">public container getSelection()</span><span class="sxs-lookup"><span data-stu-id="622ca-3033">public container getSelection()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3034">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3034">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="622ca-3035">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3035">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="622ca-3036">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="622ca-3036">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="622ca-3037">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3037">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="622ca-3038">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3038">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="622ca-3039">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3039">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="622ca-3040">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3040">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="622ca-3041">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3041">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-3042">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3042">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="622ca-3043">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3043">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="622ca-3044">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="622ca-3044">public str helpField()</span></span>                                                                                      | <span data-ttu-id="622ca-3045">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3045">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-3046">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3046">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="622ca-3047">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3047">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="622ca-3048">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3048">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="622ca-3049">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3049">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="622ca-3050">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="622ca-3050">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="622ca-3051">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3051">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="622ca-3052">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3052">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3053">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="622ca-3053">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3054">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="622ca-3054">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="622ca-3055">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3055">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="622ca-3056">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="622ca-3056">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="622ca-3057">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3057">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="622ca-3058">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="622ca-3058">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="622ca-3059">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3059">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                     |
| <span data-ttu-id="622ca-3060">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="622ca-3060">public boolean isValid()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3061">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3061">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3062">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3062">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="622ca-3063">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3063">Gets or sets the label for a control.</span></span>                                                                                                                                   |
| <span data-ttu-id="622ca-3064">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3064">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3065">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3065">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3066">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3066">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3067">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3067">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3068">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3068">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3069">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3069">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3070">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3070">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3071">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3071">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3072">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3072">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3073">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3073">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3074">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3074">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3075">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-3075">public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3076">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-3076">public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3077">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-3077">public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3078">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3078">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3079">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3079">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3080">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3080">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3081">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3081">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3082">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3082">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3083">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="622ca-3083">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3084">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3084">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="622ca-3085">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3085">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="622ca-3086">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3086">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-3087">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3087">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-3088">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3088">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-3089">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3089">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="622ca-3090">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3090">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3091">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3091">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3092">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3092">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3093">public int lineFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="622ca-3093">public int lineFromChar(int charIndex)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3094">public int lineIndex(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="622ca-3094">public int lineIndex(int lineNo)</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3095">public int lineLength(int lineNo)</span><span class="sxs-lookup"><span data-stu-id="622ca-3095">public int lineLength(int lineNo)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3096">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3096">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3097">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3097">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3098">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3098">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="622ca-3099">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="622ca-3099">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="622ca-3100">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3100">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3101">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3101">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3102">public int minNoOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3102">public int minNoOfDecimalsValue(\[int value\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3103">public boolean modified()</span><span class="sxs-lookup"><span data-stu-id="622ca-3103">public boolean modified()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3104">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-3104">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="622ca-3105">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3105">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="622ca-3106">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-3106">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="622ca-3107">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3107">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="622ca-3108">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-3108">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="622ca-3109">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3109">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="622ca-3110">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-3110">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="622ca-3111">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3111">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="622ca-3112">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3112">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="622ca-3113">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3113">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="622ca-3114">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3114">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3115">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3115">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3116">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3116">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3117">public int noOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3117">public int noOfDecimalsValue(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3118">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="622ca-3118">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3119">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="622ca-3119">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="622ca-3120">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3120">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="622ca-3121">public container posFromChar(int charIndex)</span><span class="sxs-lookup"><span data-stu-id="622ca-3121">public container posFromChar(int charIndex)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3122">public str previewPartRef(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3122">public str previewPartRef(\[str value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3123">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3123">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3124">public Real realValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3124">public Real realValue(\[Real value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3125">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3125">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3126">public int rotateSign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3126">public int rotateSign(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3127">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3127">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3128">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3128">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3129">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3129">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="622ca-3130">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3130">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-3131">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="622ca-3131">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="622ca-3132">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3132">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-3133">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3133">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3134">public int showZero(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3134">public int showZero(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3135">public int signDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3135">public int signDisplay(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3136">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3136">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="622ca-3137">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3137">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="622ca-3138">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3138">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3139">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3139">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3140">public int thousandSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3140">public int thousandSeparator(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3141">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="622ca-3141">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="622ca-3142">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3142">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="622ca-3143">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3143">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="622ca-3144">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3144">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-3145">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3145">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="622ca-3146">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3146">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-3147">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3147">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-3148">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3148">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-3149">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3149">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3150">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3150">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3151">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="622ca-3151">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3152">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3152">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-3153">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3153">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="622ca-3154">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3154">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="622ca-3155">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3155">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="622ca-3156">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3156">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="622ca-3157">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3157">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-3158">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3158">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="622ca-3159">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3159">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="622ca-3160">public int userFastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3160">public int userFastTabSummary(\[int value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3161">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3161">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="622ca-3162">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3162">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="622ca-3163">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3163">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-3164">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3164">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="622ca-3165">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3165">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="622ca-3166">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3166">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="622ca-3167">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3167">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="622ca-3168">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3168">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-3169">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3169">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="622ca-3170">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3170">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="622ca-3171">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3171">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="622ca-3172">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3172">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="622ca-3173">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3173">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="622ca-3174">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3174">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="622ca-3175">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3175">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-3176">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3176">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="622ca-3177">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="622ca-3177">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3178">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3178">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="622ca-3179">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3179">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-3180">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3180">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="622ca-3181">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3181">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="622ca-3182">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3182">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="622ca-3183">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3183">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-3184">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3184">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3185">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3185">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="622ca-3186">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3186">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="622ca-3187">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3187">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="622ca-3188">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3188">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="622ca-3189">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3189">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="622ca-3190">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3190">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="622ca-3191">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3191">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="622ca-3192">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3192">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="622ca-3193">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="622ca-3193">public void displayControl()</span></span>                                                                                | <span data-ttu-id="622ca-3194">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3194">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="622ca-3195">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3195">public void performTypeLookup(\[int userType\], \[int arrayIndex\], \[SelectableDataArea company\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3196">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3196">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3197">public void pasteText(str pasteStr, \[boolean InsertSel\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3197">public void pasteText(str pasteStr, \[boolean InsertSel\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3198">public void lookup()</span><span class="sxs-lookup"><span data-stu-id="622ca-3198">public void lookup()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3199">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3199">private void OnValidated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3200">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3200">private void OnLookup(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                   |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3201">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3201">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3202">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="622ca-3202">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="622ca-3203">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3203">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-3204">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="622ca-3204">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="622ca-3205">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3205">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="622ca-3206">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3206">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3207">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3207">private void OnModified(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3208">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="622ca-3208">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="622ca-3209">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3209">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="622ca-3210">public void undo()</span><span class="sxs-lookup"><span data-stu-id="622ca-3210">public void undo()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3211">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3211">public void performDBLookup(\[FieldId fieldId\], \[TableId tableId\], \[SelectableDataArea company\])</span></span>       |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3212">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="622ca-3212">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="622ca-3213">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3213">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="622ca-3214">public void context()</span><span class="sxs-lookup"><span data-stu-id="622ca-3214">public void context()</span></span>                                                                                       | <span data-ttu-id="622ca-3215">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3215">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="622ca-3216">public void textChange()</span><span class="sxs-lookup"><span data-stu-id="622ca-3216">public void textChange()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3217">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3217">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3218">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-3218">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="622ca-3219">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3219">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="622ca-3220">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="622ca-3220">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="622ca-3221">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3221">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="622ca-3222">public void scrollCursor()</span><span class="sxs-lookup"><span data-stu-id="622ca-3222">public void scrollCursor()</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3223">public void lineScroll(int dx, int dy)</span><span class="sxs-lookup"><span data-stu-id="622ca-3223">public void lineScroll(int dx, int dy)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3224">public void paste()</span><span class="sxs-lookup"><span data-stu-id="622ca-3224">public void paste()</span></span>                                                                                         | <span data-ttu-id="622ca-3225">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3225">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="622ca-3226">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3226">private void OnValidating(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3227">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3227">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3228">public void performFormLookup(xFormRun form)</span><span class="sxs-lookup"><span data-stu-id="622ca-3228">public void performFormLookup(xFormRun form)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3229">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="622ca-3229">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="622ca-3230">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3230">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="622ca-3231">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="622ca-3231">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="622ca-3232">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3232">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="622ca-3233">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="622ca-3233">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3234">public void setSelection(int charIndexFrom, int charIndexTo)</span><span class="sxs-lookup"><span data-stu-id="622ca-3234">public void setSelection(int charIndexFrom, int charIndexTo)</span></span>                                                |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3235">public void copy()</span><span class="sxs-lookup"><span data-stu-id="622ca-3235">public void copy()</span></span>                                                                                          | <span data-ttu-id="622ca-3236">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="622ca-3236">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="622ca-3237">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="622ca-3237">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3238">public void cut()</span><span class="sxs-lookup"><span data-stu-id="622ca-3238">public void cut()</span></span>                                                                                           | <span data-ttu-id="622ca-3239">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="622ca-3239">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="622ca-3240">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="622ca-3240">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="622ca-3241">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3241">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="622ca-3242">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="622ca-3242">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="622ca-3243">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3243">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="622ca-3244">public void enter()</span><span class="sxs-lookup"><span data-stu-id="622ca-3244">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="622ca-3245">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="622ca-3245">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="622ca-3246">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="622ca-3246">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="622ca-3247">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-3247">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="622ca-3248">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3248">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="622ca-3249">public void setCursorPos(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="622ca-3249">public void setCursorPos(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |

### <a name="method-aligncontrol"></a><span data-ttu-id="622ca-3250">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="622ca-3250">Method alignControl</span></span>

<span data-ttu-id="622ca-3251">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3251">Determines whether to align the control.</span></span>

    public boolean alignControl([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3252">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3252">Parameters</span></span>

<span data-ttu-id="622ca-3253">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3253">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3254">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3254">Return Value</span></span>

<span data-ttu-id="622ca-3255">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3255">true if the control should be aligned; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3256">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3256">Remarks</span></span>

<span data-ttu-id="622ca-3257">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3257">The upper-left corner of the control is aligned according to the longest label.</span></span>

### <a name="method-alignment"></a><span data-ttu-id="622ca-3258">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="622ca-3258">Method alignment</span></span>

    public int alignment([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3259">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3259">Parameters</span></span>

<span data-ttu-id="622ca-3260">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3260">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3261">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3261">Return Value</span></span>

### <a name="method-allowedit"></a><span data-ttu-id="622ca-3262">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="622ca-3262">Method allowEdit</span></span>

<span data-ttu-id="622ca-3263">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3263">Determines whether the user can change the contents of the control.</span></span>

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3264">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3264">Parameters</span></span>

<span data-ttu-id="622ca-3265">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3265">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3266">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3266">Return Value</span></span>

<span data-ttu-id="622ca-3267">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3267">true if the control can be edited; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3268">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3268">Remarks</span></span>

<span data-ttu-id="622ca-3269">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="622ca-3269">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

### <a name="method-allownegative"></a><span data-ttu-id="622ca-3270">メソッド allowNegative</span><span class="sxs-lookup"><span data-stu-id="622ca-3270">Method allowNegative</span></span>

    public int allowNegative([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3271">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3271">Parameters</span></span>

<span data-ttu-id="622ca-3272">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3272">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3273">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3273">Return Value</span></span>

### <a name="method-allowsyssetup"></a><span data-ttu-id="622ca-3274">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="622ca-3274">Method allowSysSetup</span></span>

<span data-ttu-id="622ca-3275">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3275">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

    public boolean allowSysSetup()

#### <a name="return-value"></a><span data-ttu-id="622ca-3276">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3276">Return Value</span></span>

<span data-ttu-id="622ca-3277">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3277">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

### <a name="method-arrayindex"></a><span data-ttu-id="622ca-3278">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-3278">Method arrayIndex</span></span>

    public int arrayIndex([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3279">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3279">Parameters</span></span>

<span data-ttu-id="622ca-3280">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3280">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3281">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3281">Return Value</span></span>

### <a name="method-autodeclaration"></a><span data-ttu-id="622ca-3282">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="622ca-3282">Method autoDeclaration</span></span>

<span data-ttu-id="622ca-3283">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3283">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3284">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3284">Parameters</span></span>

<span data-ttu-id="622ca-3285">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3285">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3286">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3286">Return Value</span></span>

<span data-ttu-id="622ca-3287">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3287">true if the member variable can be declared for this control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3288">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3288">Remarks</span></span>

<span data-ttu-id="622ca-3289">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3289">Controls cannot have identical names.</span></span>

### <a name="method-autoinsseparator"></a><span data-ttu-id="622ca-3290">メソッド autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="622ca-3290">Method autoInsSeparator</span></span>

    public int autoInsSeparator([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3291">Parameters</span></span>

<span data-ttu-id="622ca-3292">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3292">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3293">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3293">Return Value</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="622ca-3294">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="622ca-3294">Method backgroundColor</span></span>

<span data-ttu-id="622ca-3295">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3295">Gets or sets the background color of the control.</span></span>

    public int backgroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3296">Parameters</span></span>

<span data-ttu-id="622ca-3297">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3297">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3298">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3298">Return Value</span></span>

<span data-ttu-id="622ca-3299">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-3299">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3300">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3300">Remarks</span></span>

<span data-ttu-id="622ca-3301">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3301">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="622ca-3302">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="622ca-3302">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="622ca-3303">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="622ca-3303">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="622ca-3304">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="622ca-3304">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="622ca-3305">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3305">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="622ca-3306">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3306">The maximum value for a single byte is 255.</span></span>

### <a name="method-backstyle"></a><span data-ttu-id="622ca-3307">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="622ca-3307">Method backStyle</span></span>

<span data-ttu-id="622ca-3308">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3308">Determines whether the control background can be transparent.</span></span>

    public int backStyle([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3309">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3309">Parameters</span></span>

<span data-ttu-id="622ca-3310">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3310">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3311">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3311">Return Value</span></span>

<span data-ttu-id="622ca-3312">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3312">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="method-begindrag"></a><span data-ttu-id="622ca-3313">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="622ca-3313">Method beginDrag</span></span>

<span data-ttu-id="622ca-3314">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3314">Is called when the user starts to drag a form control.</span></span>

    public int beginDrag(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-3315">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3315">Parameters</span></span>

<span data-ttu-id="622ca-3316">x</span><span class="sxs-lookup"><span data-stu-id="622ca-3316">x</span></span>  
<span data-ttu-id="622ca-3317">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3317">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="622ca-3318">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="622ca-3318">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="622ca-3319">y</span><span class="sxs-lookup"><span data-stu-id="622ca-3319">y</span></span>  
<span data-ttu-id="622ca-3320">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3320">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="622ca-3321">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="622ca-3321">The coordinate is relative to the upper-left corner of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3322">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3322">Return Value</span></span>

<span data-ttu-id="622ca-3323">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3323">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3324">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3324">Remarks</span></span>

<span data-ttu-id="622ca-3325">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3325">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="622ca-3326">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3326">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-bold"></a><span data-ttu-id="622ca-3327">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="622ca-3327">Method bold</span></span>

<span data-ttu-id="622ca-3328">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3328">Gets or sets the weight of font that is used to output text in the control.</span></span>

    public int bold([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3329">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3329">Parameters</span></span>

<span data-ttu-id="622ca-3330">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3330">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3331">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3331">Return Value</span></span>

<span data-ttu-id="622ca-3332">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3332">An integer value between zero and nine, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3333">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3333">Remarks</span></span>

<span data-ttu-id="622ca-3334">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3334">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="622ca-3335">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3335">0 Use the default font weight.</span></span>
-   <span data-ttu-id="622ca-3336">1 シン。</span><span class="sxs-lookup"><span data-stu-id="622ca-3336">1 Thin.</span></span>
-   <span data-ttu-id="622ca-3337">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="622ca-3337">2 Extra-light.</span></span>
-   <span data-ttu-id="622ca-3338">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="622ca-3338">3 Light.</span></span>
-   <span data-ttu-id="622ca-3339">4 標準。</span><span class="sxs-lookup"><span data-stu-id="622ca-3339">4 Normal.</span></span>
-   <span data-ttu-id="622ca-3340">5 中。</span><span class="sxs-lookup"><span data-stu-id="622ca-3340">5 Medium.</span></span>
-   <span data-ttu-id="622ca-3341">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="622ca-3341">6 Semibold.</span></span>
-   <span data-ttu-id="622ca-3342">7 太字。</span><span class="sxs-lookup"><span data-stu-id="622ca-3342">7 Bold.</span></span>
-   <span data-ttu-id="622ca-3343">8 極太。</span><span class="sxs-lookup"><span data-stu-id="622ca-3343">8 Extra-bold.</span></span>
-   <span data-ttu-id="622ca-3344">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="622ca-3344">9 Heavy.</span></span>

### <a name="method-border"></a><span data-ttu-id="622ca-3345">メソッド border</span><span class="sxs-lookup"><span data-stu-id="622ca-3345">Method border</span></span>

<span data-ttu-id="622ca-3346">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3346">Gets or sets the style of the borderline of the control.</span></span>

    public int border([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3347">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3347">Parameters</span></span>

<span data-ttu-id="622ca-3348">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3348">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3349">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3349">Return Value</span></span>

<span data-ttu-id="622ca-3350">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-3350">An integer between zero and four, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3351">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3351">Remarks</span></span>

<span data-ttu-id="622ca-3352">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3352">The integer that is returned contains the style of the borderline of the control as follows.</span></span>

| <span data-ttu-id="622ca-3353">先頭値</span><span class="sxs-lookup"><span data-stu-id="622ca-3353">Value</span></span> | <span data-ttu-id="622ca-3354">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-3354">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="622ca-3355">0</span><span class="sxs-lookup"><span data-stu-id="622ca-3355">0</span></span>     | <span data-ttu-id="622ca-3356">自動</span><span class="sxs-lookup"><span data-stu-id="622ca-3356">Auto</span></span>        |
| <span data-ttu-id="622ca-3357">1</span><span class="sxs-lookup"><span data-stu-id="622ca-3357">1</span></span>     | <span data-ttu-id="622ca-3358">3D</span><span class="sxs-lookup"><span data-stu-id="622ca-3358">3D</span></span>          |
| <span data-ttu-id="622ca-3359">2</span><span class="sxs-lookup"><span data-stu-id="622ca-3359">2</span></span>     | <span data-ttu-id="622ca-3360">単一明細行</span><span class="sxs-lookup"><span data-stu-id="622ca-3360">Single line</span></span> |
| <span data-ttu-id="622ca-3361">3</span><span class="sxs-lookup"><span data-stu-id="622ca-3361">3</span></span>     | <span data-ttu-id="622ca-3362">均一</span><span class="sxs-lookup"><span data-stu-id="622ca-3362">Flat</span></span>        |
| <span data-ttu-id="622ca-3363">4</span><span class="sxs-lookup"><span data-stu-id="622ca-3363">4</span></span>     | <span data-ttu-id="622ca-3364">None</span><span class="sxs-lookup"><span data-stu-id="622ca-3364">None</span></span>        |

### <a name="method-cachedatamethod"></a><span data-ttu-id="622ca-3365">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="622ca-3365">Method cacheDataMethod</span></span>

    public int cacheDataMethod([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3366">Parameters</span></span>

<span data-ttu-id="622ca-3367">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3367">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3368">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3368">Return Value</span></span>

### <a name="method-calccontrolsize"></a><span data-ttu-id="622ca-3369">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="622ca-3369">Method calcControlSize</span></span>

<span data-ttu-id="622ca-3370">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3370">Retrieves the size of the control.</span></span>

    public container calcControlSize(int chars, int lines)

#### <a name="parameters"></a><span data-ttu-id="622ca-3371">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3371">Parameters</span></span>

<span data-ttu-id="622ca-3372">chars</span><span class="sxs-lookup"><span data-stu-id="622ca-3372">chars</span></span>  
<span data-ttu-id="622ca-3373">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="622ca-3373">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="622ca-3374">明細行</span><span class="sxs-lookup"><span data-stu-id="622ca-3374">lines</span></span>  
<span data-ttu-id="622ca-3375">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="622ca-3375">The number of lines to use to determine the height.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3376">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3376">Return Value</span></span>

<span data-ttu-id="622ca-3377">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="622ca-3377">The container that holds the width and height.</span></span>

### <a name="method-characterset"></a><span data-ttu-id="622ca-3378">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="622ca-3378">Method characterSet</span></span>

<span data-ttu-id="622ca-3379">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3379">Gets or sets the character set of the font.</span></span>

    public int characterSet([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3380">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3380">Parameters</span></span>

<span data-ttu-id="622ca-3381">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3381">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3382">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3382">Return Value</span></span>

<span data-ttu-id="622ca-3383">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3383">An integer value that indicates the character set of the font.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3384">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3384">Remarks</span></span>

<span data-ttu-id="622ca-3385">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3385">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="622ca-3386">先頭値</span><span class="sxs-lookup"><span data-stu-id="622ca-3386">Value</span></span> | <span data-ttu-id="622ca-3387">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-3387">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="622ca-3388">0</span><span class="sxs-lookup"><span data-stu-id="622ca-3388">0</span></span>     | <span data-ttu-id="622ca-3389">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3389">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="622ca-3390">1</span><span class="sxs-lookup"><span data-stu-id="622ca-3390">1</span></span>     | <span data-ttu-id="622ca-3391">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3391">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="622ca-3392">2</span><span class="sxs-lookup"><span data-stu-id="622ca-3392">2</span></span>     | <span data-ttu-id="622ca-3393">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3393">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="622ca-3394">77</span><span class="sxs-lookup"><span data-stu-id="622ca-3394">77</span></span>    | <span data-ttu-id="622ca-3395">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3395">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="622ca-3396">128</span><span class="sxs-lookup"><span data-stu-id="622ca-3396">128</span></span>   | <span data-ttu-id="622ca-3397">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3397">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="622ca-3398">129</span><span class="sxs-lookup"><span data-stu-id="622ca-3398">129</span></span>   | <span data-ttu-id="622ca-3399">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3399">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="622ca-3400">134</span><span class="sxs-lookup"><span data-stu-id="622ca-3400">134</span></span>   | <span data-ttu-id="622ca-3401">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3401">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="622ca-3402">136</span><span class="sxs-lookup"><span data-stu-id="622ca-3402">136</span></span>   | <span data-ttu-id="622ca-3403">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3403">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="622ca-3404">161</span><span class="sxs-lookup"><span data-stu-id="622ca-3404">161</span></span>   | <span data-ttu-id="622ca-3405">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3405">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="622ca-3406">162</span><span class="sxs-lookup"><span data-stu-id="622ca-3406">162</span></span>   | <span data-ttu-id="622ca-3407">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3407">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="622ca-3408">163</span><span class="sxs-lookup"><span data-stu-id="622ca-3408">163</span></span>   | <span data-ttu-id="622ca-3409">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3409">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="622ca-3410">186</span><span class="sxs-lookup"><span data-stu-id="622ca-3410">186</span></span>   | <span data-ttu-id="622ca-3411">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3411">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="622ca-3412">204</span><span class="sxs-lookup"><span data-stu-id="622ca-3412">204</span></span>   | <span data-ttu-id="622ca-3413">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3413">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="622ca-3414">238</span><span class="sxs-lookup"><span data-stu-id="622ca-3414">238</span></span>   | <span data-ttu-id="622ca-3415">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3415">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="622ca-3416">255</span><span class="sxs-lookup"><span data-stu-id="622ca-3416">255</span></span>   | <span data-ttu-id="622ca-3417">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3417">OEM\_CHARSET</span></span>         |

<span data-ttu-id="622ca-3418">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3418">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="622ca-3419">金額</span><span class="sxs-lookup"><span data-stu-id="622ca-3419">Value</span></span> | <span data-ttu-id="622ca-3420">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-3420">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="622ca-3421">130</span><span class="sxs-lookup"><span data-stu-id="622ca-3421">130</span></span>   | <span data-ttu-id="622ca-3422">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3422">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="622ca-3423">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3423">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="622ca-3424">先頭値</span><span class="sxs-lookup"><span data-stu-id="622ca-3424">Value</span></span> | <span data-ttu-id="622ca-3425">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-3425">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="622ca-3426">177</span><span class="sxs-lookup"><span data-stu-id="622ca-3426">177</span></span>   | <span data-ttu-id="622ca-3427">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3427">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="622ca-3428">178</span><span class="sxs-lookup"><span data-stu-id="622ca-3428">178</span></span>   | <span data-ttu-id="622ca-3429">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3429">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="622ca-3430">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3430">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="622ca-3431">先頭値</span><span class="sxs-lookup"><span data-stu-id="622ca-3431">Value</span></span> | <span data-ttu-id="622ca-3432">説明</span><span class="sxs-lookup"><span data-stu-id="622ca-3432">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="622ca-3433">222</span><span class="sxs-lookup"><span data-stu-id="622ca-3433">222</span></span>   | <span data-ttu-id="622ca-3434">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="622ca-3434">THAI\_CHARSET</span></span> |

<span data-ttu-id="622ca-3435">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3435">The default character set is set to values that are based on the current system locale.</span></span> <span data-ttu-id="622ca-3436">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3436">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="622ca-3437">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="622ca-3437">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

### <a name="method-charfrompos"></a><span data-ttu-id="622ca-3438">メソッド charFromPos</span><span class="sxs-lookup"><span data-stu-id="622ca-3438">Method charFromPos</span></span>

    public int charFromPos(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-3439">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3439">Parameters</span></span>

<span data-ttu-id="622ca-3440">x</span><span class="sxs-lookup"><span data-stu-id="622ca-3440">x</span></span>  

<!-- -->

<span data-ttu-id="622ca-3441">y</span><span class="sxs-lookup"><span data-stu-id="622ca-3441">y</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3442">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3442">Return Value</span></span>

### <a name="method-colorscheme"></a><span data-ttu-id="622ca-3443">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="622ca-3443">Method colorScheme</span></span>

<span data-ttu-id="622ca-3444">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3444">Gets or sets the color scheme of the control.</span></span>

    public int colorScheme([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3445">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3445">Parameters</span></span>

<span data-ttu-id="622ca-3446">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3446">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3447">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3447">Return Value</span></span>

<span data-ttu-id="622ca-3448">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-3448">An integer between zero and two, inclusive.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3449">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3449">Remarks</span></span>

<span data-ttu-id="622ca-3450">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3450">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="622ca-3451">先頭値</span><span class="sxs-lookup"><span data-stu-id="622ca-3451">Value</span></span> | <span data-ttu-id="622ca-3452">スタイル</span><span class="sxs-lookup"><span data-stu-id="622ca-3452">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="622ca-3453">0</span><span class="sxs-lookup"><span data-stu-id="622ca-3453">0</span></span>     | <span data-ttu-id="622ca-3454">既定</span><span class="sxs-lookup"><span data-stu-id="622ca-3454">Default</span></span>               |
| <span data-ttu-id="622ca-3455">1</span><span class="sxs-lookup"><span data-stu-id="622ca-3455">1</span></span>     | <span data-ttu-id="622ca-3456">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="622ca-3456">The Windows palette</span></span>   |
| <span data-ttu-id="622ca-3457">2</span><span class="sxs-lookup"><span data-stu-id="622ca-3457">2</span></span>     | <span data-ttu-id="622ca-3458">真の配色</span><span class="sxs-lookup"><span data-stu-id="622ca-3458">The true-color scheme</span></span> |

### <a name="method-configurationkey"></a><span data-ttu-id="622ca-3459">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="622ca-3459">Method configurationKey</span></span>

<span data-ttu-id="622ca-3460">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3460">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3461">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3461">Parameters</span></span>

<span data-ttu-id="622ca-3462">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3462">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3463">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3463">Return Value</span></span>

<span data-ttu-id="622ca-3464">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="622ca-3464">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3465">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3465">Remarks</span></span>

<span data-ttu-id="622ca-3466">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3466">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="622ca-3467">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3467">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-configurationkeyex"></a><span data-ttu-id="622ca-3468">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="622ca-3468">Method configurationKeyEx</span></span>

<span data-ttu-id="622ca-3469">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3469">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

    public List configurationKeyEx()

#### <a name="return-value"></a><span data-ttu-id="622ca-3470">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3470">Return Value</span></span>

<span data-ttu-id="622ca-3471">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="622ca-3471">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3472">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3472">Remarks</span></span>

<span data-ttu-id="622ca-3473">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3473">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="622ca-3474">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3474">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="622ca-3475">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3475">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="622ca-3476">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="622ca-3476">Method countryRegionCodes</span></span>

<span data-ttu-id="622ca-3477">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3477">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3478">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3478">Parameters</span></span>

<span data-ttu-id="622ca-3479">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3479">value</span></span>  
<span data-ttu-id="622ca-3480">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-3480">The string that contains the country/region codes to set; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3481">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3481">Return Value</span></span>

<span data-ttu-id="622ca-3482">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="622ca-3482">The comma-separated list of country/region codes for the control.</span></span>

### <a name="method-countryregioncontextfield"></a><span data-ttu-id="622ca-3483">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="622ca-3483">Method countryRegionContextField</span></span>

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3484">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3484">Parameters</span></span>

<span data-ttu-id="622ca-3485">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3485">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3486">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3486">Return Value</span></span>

### <a name="method-datafield"></a><span data-ttu-id="622ca-3487">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="622ca-3487">Method dataField</span></span>

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3488">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3488">Parameters</span></span>

<span data-ttu-id="622ca-3489">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3489">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3490">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3490">Return Value</span></span>

### <a name="method-datafieldarrayindex"></a><span data-ttu-id="622ca-3491">メソッド dataFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-3491">Method dataFieldArrayIndex</span></span>

    public int dataFieldArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="622ca-3492">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3492">Return Value</span></span>

### <a name="method-datafieldname"></a><span data-ttu-id="622ca-3493">メソッド dataFieldName</span><span class="sxs-lookup"><span data-stu-id="622ca-3493">Method dataFieldName</span></span>

    public FieldName dataFieldName()

#### <a name="return-value"></a><span data-ttu-id="622ca-3494">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3494">Return Value</span></span>

### <a name="method-datamethod"></a><span data-ttu-id="622ca-3495">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="622ca-3495">Method dataMethod</span></span>

    public str dataMethod([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3496">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3496">Parameters</span></span>

<span data-ttu-id="622ca-3497">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3497">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3498">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3498">Return Value</span></span>

### <a name="method-datarelationpath"></a><span data-ttu-id="622ca-3499">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="622ca-3499">Method dataRelationPath</span></span>

<span data-ttu-id="622ca-3500">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3500">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

    public str dataRelationPath([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3501">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3501">Parameters</span></span>

<span data-ttu-id="622ca-3502">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3502">value</span></span>  
<span data-ttu-id="622ca-3503">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-3503">The string that contains the period-delimited list of relations; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3504">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3504">Return Value</span></span>

<span data-ttu-id="622ca-3505">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="622ca-3505">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3506">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3506">Remarks</span></span>

<span data-ttu-id="622ca-3507">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3507">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="622ca-3508">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="622ca-3508">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

### <a name="method-datasource"></a><span data-ttu-id="622ca-3509">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="622ca-3509">Method dataSource</span></span>

<span data-ttu-id="622ca-3510">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3510">Gets or sets a data source that will be used by the control or the form.</span></span>

    public int dataSource([AnyType value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3511">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3511">Parameters</span></span>

<span data-ttu-id="622ca-3512">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3512">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3513">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3513">Return Value</span></span>

<span data-ttu-id="622ca-3514">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="622ca-3514">The identifier of the data source that will be used.</span></span>

### <a name="method-decimalseparator"></a><span data-ttu-id="622ca-3515">メソッド decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="622ca-3515">Method decimalSeparator</span></span>

    public int decimalSeparator([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3516">Parameters</span></span>

<span data-ttu-id="622ca-3517">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3517">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3518">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3518">Return Value</span></span>

### <a name="method-direction"></a><span data-ttu-id="622ca-3519">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="622ca-3519">Method direction</span></span>

    public int direction([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3520">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3520">Parameters</span></span>

<span data-ttu-id="622ca-3521">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3521">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3522">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3522">Return Value</span></span>

### <a name="method-displacenegative"></a><span data-ttu-id="622ca-3523">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="622ca-3523">Method displaceNegative</span></span>

    public int displaceNegative([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3524">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3524">Parameters</span></span>

<span data-ttu-id="622ca-3525">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3525">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-3526">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3526">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3527">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3527">Return Value</span></span>

### <a name="method-displacenegativemode"></a><span data-ttu-id="622ca-3528">メソッド displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3528">Method displaceNegativeMode</span></span>

    public AutoMode displaceNegativeMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3529">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3529">Parameters</span></span>

<span data-ttu-id="622ca-3530">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3530">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3531">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3531">Return Value</span></span>

### <a name="method-displacenegativevalue"></a><span data-ttu-id="622ca-3532">メソッド displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="622ca-3532">Method displaceNegativeValue</span></span>

    public int displaceNegativeValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3533">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3533">Parameters</span></span>

<span data-ttu-id="622ca-3534">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3534">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3535">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3535">Return Value</span></span>

### <a name="method-displayheight"></a><span data-ttu-id="622ca-3536">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="622ca-3536">Method displayHeight</span></span>

    public int displayHeight([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3537">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3537">Parameters</span></span>

<span data-ttu-id="622ca-3538">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3538">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-3539">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3539">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3540">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3540">Return Value</span></span>

### <a name="method-displayheightmode"></a><span data-ttu-id="622ca-3541">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3541">Method displayHeightMode</span></span>

    public AutoMode displayHeightMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3542">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3542">Parameters</span></span>

<span data-ttu-id="622ca-3543">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3543">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3544">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3544">Return Value</span></span>

### <a name="method-displayheightvalue"></a><span data-ttu-id="622ca-3545">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="622ca-3545">Method displayHeightValue</span></span>

    public int displayHeightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3546">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3546">Parameters</span></span>

<span data-ttu-id="622ca-3547">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3547">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3548">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3548">Return Value</span></span>

### <a name="method-displaylength"></a><span data-ttu-id="622ca-3549">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="622ca-3549">Method displayLength</span></span>

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3550">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3550">Parameters</span></span>

<span data-ttu-id="622ca-3551">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3551">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-3552">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3552">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3553">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3553">Return Value</span></span>

### <a name="method-displaylengthmode"></a><span data-ttu-id="622ca-3554">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3554">Method displayLengthMode</span></span>

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3555">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3555">Parameters</span></span>

<span data-ttu-id="622ca-3556">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3556">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3557">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3557">Return Value</span></span>

### <a name="method-displaylengthvalue"></a><span data-ttu-id="622ca-3558">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="622ca-3558">Method displayLengthValue</span></span>

    public int displayLengthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3559">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3559">Parameters</span></span>

<span data-ttu-id="622ca-3560">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3560">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3561">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3561">Return Value</span></span>

### <a name="method-displaytarget"></a><span data-ttu-id="622ca-3562">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="622ca-3562">Method displayTarget</span></span>

<span data-ttu-id="622ca-3563">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3563">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

    public int displayTarget([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3564">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3564">Parameters</span></span>

<span data-ttu-id="622ca-3565">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3565">value</span></span>  
<span data-ttu-id="622ca-3566">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-3566">The integer value that indicates where the control is displayed; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3567">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3567">Return Value</span></span>

<span data-ttu-id="622ca-3568">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3568">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

### <a name="method-dragdrop"></a><span data-ttu-id="622ca-3569">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="622ca-3569">Method dragDrop</span></span>

<span data-ttu-id="622ca-3570">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3570">Indicates whether to enable or disable drag-and-drop operations for the control.</span></span>

    public int dragDrop([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3571">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3571">Parameters</span></span>

<span data-ttu-id="622ca-3572">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3572">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3573">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3573">Return Value</span></span>

<span data-ttu-id="622ca-3574">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3574">1 if drag-and-drop operations are enabled; otherwise, 0.</span></span>

### <a name="method-dragover"></a><span data-ttu-id="622ca-3575">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="622ca-3575">Method dragOver</span></span>

<span data-ttu-id="622ca-3576">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3576">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-3577">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3577">Parameters</span></span>

<span data-ttu-id="622ca-3578">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-3578">dragSource</span></span>  
<span data-ttu-id="622ca-3579">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3579">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-3580">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3580">dragMode</span></span>  
<span data-ttu-id="622ca-3581">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3581">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-3582">x</span><span class="sxs-lookup"><span data-stu-id="622ca-3582">x</span></span>  
<span data-ttu-id="622ca-3583">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3583">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-3584">y</span><span class="sxs-lookup"><span data-stu-id="622ca-3584">y</span></span>  
<span data-ttu-id="622ca-3585">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3585">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3586">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3586">Return Value</span></span>

<span data-ttu-id="622ca-3587">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3587">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragoverex"></a><span data-ttu-id="622ca-3588">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="622ca-3588">Method dragOverEx</span></span>

<span data-ttu-id="622ca-3589">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3589">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

    public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-3590">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3590">Parameters</span></span>

<span data-ttu-id="622ca-3591">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-3591">dragSource</span></span>  
<span data-ttu-id="622ca-3592">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3592">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-3593">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3593">dragMode</span></span>  
<span data-ttu-id="622ca-3594">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3594">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-3595">x</span><span class="sxs-lookup"><span data-stu-id="622ca-3595">x</span></span>  
<span data-ttu-id="622ca-3596">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3596">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-3597">y</span><span class="sxs-lookup"><span data-stu-id="622ca-3597">y</span></span>  
<span data-ttu-id="622ca-3598">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3598">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3599">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3599">Return Value</span></span>

<span data-ttu-id="622ca-3600">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3600">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

### <a name="method-dragtext"></a><span data-ttu-id="622ca-3601">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="622ca-3601">Method dragText</span></span>

<span data-ttu-id="622ca-3602">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3602">Retrieves the text that is displayed when the form control is dragged.</span></span>

    public str dragText()

#### <a name="return-value"></a><span data-ttu-id="622ca-3603">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3603">Return Value</span></span>

<span data-ttu-id="622ca-3604">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-3604">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

### <a name="method-enabled"></a><span data-ttu-id="622ca-3605">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="622ca-3605">Method enabled</span></span>

<span data-ttu-id="622ca-3606">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3606">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3607">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3607">Parameters</span></span>

<span data-ttu-id="622ca-3608">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3608">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3609">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3609">Return Value</span></span>

<span data-ttu-id="622ca-3610">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3610">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3611">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3611">Remarks</span></span>

<span data-ttu-id="622ca-3612">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3612">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="622ca-3613">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3613">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="622ca-3614">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3614">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-extendeddatatype"></a><span data-ttu-id="622ca-3615">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="622ca-3615">Method extendedDataType</span></span>

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3616">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3616">Parameters</span></span>

<span data-ttu-id="622ca-3617">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3617">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3618">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3618">Return Value</span></span>

### <a name="method-fasttabsummary"></a><span data-ttu-id="622ca-3619">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="622ca-3619">Method fastTabSummary</span></span>

    public int fastTabSummary([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3620">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3620">Parameters</span></span>

<span data-ttu-id="622ca-3621">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3621">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3622">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3622">Return Value</span></span>

### <a name="method-font"></a><span data-ttu-id="622ca-3623">メソッド font</span><span class="sxs-lookup"><span data-stu-id="622ca-3623">Method font</span></span>

<span data-ttu-id="622ca-3624">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3624">Gets or sets the name of the font for the control to use.</span></span>

    public str font([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3625">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3625">Parameters</span></span>

<span data-ttu-id="622ca-3626">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3626">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3627">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3627">Return Value</span></span>

<span data-ttu-id="622ca-3628">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-3628">The name of the font to use, such as Tahoma or Verdana.</span></span>

### <a name="method-fontsize"></a><span data-ttu-id="622ca-3629">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="622ca-3629">Method fontSize</span></span>

<span data-ttu-id="622ca-3630">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3630">Gets or sets the size of the font for the control to use.</span></span>

    public int fontSize([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3631">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3631">Parameters</span></span>

<span data-ttu-id="622ca-3632">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3632">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3633">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3633">Return Value</span></span>

<span data-ttu-id="622ca-3634">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-3634">The height of the font in points.</span></span>

### <a name="method-foregroundcolor"></a><span data-ttu-id="622ca-3635">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="622ca-3635">Method foregroundColor</span></span>

<span data-ttu-id="622ca-3636">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3636">Gets or sets the text color for the control to use.</span></span>

    public int foregroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3637">Parameters</span></span>

<span data-ttu-id="622ca-3638">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3638">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3639">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3639">Return Value</span></span>

<span data-ttu-id="622ca-3640">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="622ca-3640">An integer that contains a packed RGB color.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3641">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3641">Remarks</span></span>

<span data-ttu-id="622ca-3642">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3642">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="622ca-3643">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="622ca-3643">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="622ca-3644">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="622ca-3644">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="622ca-3645">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="622ca-3645">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="622ca-3646">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3646">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="622ca-3647">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3647">The maximum value for a single byte is 255.</span></span>

### <a name="method-formatmst"></a><span data-ttu-id="622ca-3648">メソッド formatMST</span><span class="sxs-lookup"><span data-stu-id="622ca-3648">Method formatMST</span></span>

    public int formatMST([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3649">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3649">Parameters</span></span>

<span data-ttu-id="622ca-3650">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3650">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3651">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3651">Return Value</span></span>

### <a name="method-getcursorpos"></a><span data-ttu-id="622ca-3652">メソッド getCursorPos</span><span class="sxs-lookup"><span data-stu-id="622ca-3652">Method getCursorPos</span></span>

    public container getCursorPos()

#### <a name="return-value"></a><span data-ttu-id="622ca-3653">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3653">Return Value</span></span>

### <a name="method-getfirstvisibleline"></a><span data-ttu-id="622ca-3654">メソッド getFirstVisibleLine</span><span class="sxs-lookup"><span data-stu-id="622ca-3654">Method getFirstVisibleLine</span></span>

    public int getFirstVisibleLine()

#### <a name="return-value"></a><span data-ttu-id="622ca-3655">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3655">Return Value</span></span>

### <a name="method-getline"></a><span data-ttu-id="622ca-3656">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="622ca-3656">Method getLine</span></span>

    public str getLine(int lineNo)

#### <a name="parameters"></a><span data-ttu-id="622ca-3657">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3657">Parameters</span></span>

<span data-ttu-id="622ca-3658">lineNo</span><span class="sxs-lookup"><span data-stu-id="622ca-3658">lineNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3659">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3659">Return Value</span></span>

### <a name="method-getlinecount"></a><span data-ttu-id="622ca-3660">メソッド getLineCount</span><span class="sxs-lookup"><span data-stu-id="622ca-3660">Method getLineCount</span></span>

    public int getLineCount()

#### <a name="return-value"></a><span data-ttu-id="622ca-3661">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3661">Return Value</span></span>

### <a name="method-getselection"></a><span data-ttu-id="622ca-3662">メソッド getSelection</span><span class="sxs-lookup"><span data-stu-id="622ca-3662">Method getSelection</span></span>

    public container getSelection()

#### <a name="return-value"></a><span data-ttu-id="622ca-3663">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3663">Return Value</span></span>

### <a name="method-haschanged"></a><span data-ttu-id="622ca-3664">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="622ca-3664">Method hasChanged</span></span>

<span data-ttu-id="622ca-3665">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3665">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

    public boolean hasChanged([boolean val])

#### <a name="parameters"></a><span data-ttu-id="622ca-3666">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3666">Parameters</span></span>

<span data-ttu-id="622ca-3667">val</span><span class="sxs-lookup"><span data-stu-id="622ca-3667">val</span></span>  
<span data-ttu-id="622ca-3668">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-3668">The value to assign as the hasChanged value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3669">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3669">Return Value</span></span>

<span data-ttu-id="622ca-3670">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3670">true if the contents of the control have changed; otherwise, false.</span></span>

### <a name="method-hasusersetting"></a><span data-ttu-id="622ca-3671">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="622ca-3671">Method hasUserSetting</span></span>

<span data-ttu-id="622ca-3672">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3672">Indicates whether the control has custom user settings.</span></span>

    public boolean hasUserSetting()

#### <a name="return-value"></a><span data-ttu-id="622ca-3673">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3673">Return Value</span></span>

<span data-ttu-id="622ca-3674">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3674">true if the control has custom user settings; otherwise, false.</span></span>

### <a name="method-height"></a><span data-ttu-id="622ca-3675">メソッド height</span><span class="sxs-lookup"><span data-stu-id="622ca-3675">Method height</span></span>

<span data-ttu-id="622ca-3676">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3676">Gets or sets the height of the control.</span></span>

    public int height(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3677">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3677">Parameters</span></span>

<span data-ttu-id="622ca-3678">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3678">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-3679">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3679">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3680">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3680">Return Value</span></span>

<span data-ttu-id="622ca-3681">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-3681">The height of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3682">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3682">Remarks</span></span>

<span data-ttu-id="622ca-3683">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3683">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="622ca-3684">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="622ca-3684">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="622ca-3685">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3685">Mode</span></span>            | <span data-ttu-id="622ca-3686">高さの計算</span><span class="sxs-lookup"><span data-stu-id="622ca-3686">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-3687">-1 正確</span><span class="sxs-lookup"><span data-stu-id="622ca-3687">-1 Exact</span></span>        | <span data-ttu-id="622ca-3688">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3688">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-3689">0 自動</span><span class="sxs-lookup"><span data-stu-id="622ca-3689">0 Auto</span></span>          | <span data-ttu-id="622ca-3690">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3690">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-3691">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="622ca-3691">1 Column height</span></span> | <span data-ttu-id="622ca-3692">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-3692">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="622ca-3693">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3693">The height and height calculation mode can be set separately.</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="622ca-3694">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3694">Method heightMode</span></span>

<span data-ttu-id="622ca-3695">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3695">Gets or sets a calculation mode for the height of the control.</span></span>

    public int heightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3696">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3696">Parameters</span></span>

<span data-ttu-id="622ca-3697">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3697">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3698">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3698">Return Value</span></span>

<span data-ttu-id="622ca-3699">計算モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-3699">The calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3700">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3700">Remarks</span></span>

<span data-ttu-id="622ca-3701">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="622ca-3701">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="622ca-3702">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3702">Mode</span></span>          | <span data-ttu-id="622ca-3703">高さの計算</span><span class="sxs-lookup"><span data-stu-id="622ca-3703">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-3704">正確</span><span class="sxs-lookup"><span data-stu-id="622ca-3704">Exact</span></span>         | <span data-ttu-id="622ca-3705">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3705">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-3706">自動</span><span class="sxs-lookup"><span data-stu-id="622ca-3706">Auto</span></span>          | <span data-ttu-id="622ca-3707">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3707">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-3708">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="622ca-3708">Column height</span></span> | <span data-ttu-id="622ca-3709">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-3709">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="622ca-3710">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="622ca-3710">The height of the control might change when the mode is set to auto or column height.</span></span>

### <a name="method-heightvalue"></a><span data-ttu-id="622ca-3711">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="622ca-3711">Method heightValue</span></span>

<span data-ttu-id="622ca-3712">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3712">Gets or sets the height of the control.</span></span>

    public int heightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3713">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3713">Parameters</span></span>

<span data-ttu-id="622ca-3714">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3714">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3715">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3715">Return Value</span></span>

<span data-ttu-id="622ca-3716">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-3716">The height in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3717">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3717">Remarks</span></span>

<span data-ttu-id="622ca-3718">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3718">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

### <a name="method-helpfield"></a><span data-ttu-id="622ca-3719">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="622ca-3719">Method helpField</span></span>

<span data-ttu-id="622ca-3720">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3720">Retrieves the Help text for the control.</span></span>

    public str helpField()

#### <a name="return-value"></a><span data-ttu-id="622ca-3721">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3721">Return Value</span></span>

<span data-ttu-id="622ca-3722">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-3722">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3723">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3723">Remarks</span></span>

<span data-ttu-id="622ca-3724">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3724">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="622ca-3725">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3725">Use the helpText method to set the value of the Help text.</span></span>

### <a name="method-helptext"></a><span data-ttu-id="622ca-3726">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="622ca-3726">Method helpText</span></span>

<span data-ttu-id="622ca-3727">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3727">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

    public str helpText([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3728">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3728">Parameters</span></span>

<span data-ttu-id="622ca-3729">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3729">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3730">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3730">Return Value</span></span>

<span data-ttu-id="622ca-3731">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-3731">The string to be displayed at the bottom of the screen.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3732">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3732">Remarks</span></span>

<span data-ttu-id="622ca-3733">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3733">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="622ca-3734">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3734">The Help text must not exceed 250 characters.</span></span>

### <a name="method-hierarchyparent"></a><span data-ttu-id="622ca-3735">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="622ca-3735">Method hierarchyParent</span></span>

<span data-ttu-id="622ca-3736">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3736">Gets or sets the HierarchyParent property value of the control.</span></span>

    public str hierarchyParent([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3737">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3737">Parameters</span></span>

<span data-ttu-id="622ca-3738">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3738">value</span></span>  
<span data-ttu-id="622ca-3739">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3739">The value to assign to the HierarchyParent property of the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3740">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3740">Return Value</span></span>

<span data-ttu-id="622ca-3741">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3741">The HierarchyParent property value of the control.</span></span>

### <a name="method-hwnd"></a><span data-ttu-id="622ca-3742">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="622ca-3742">Method hWnd</span></span>

<span data-ttu-id="622ca-3743">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3743">Retrieves the Windows handle for the control.</span></span>

    public int hWnd()

#### <a name="return-value"></a><span data-ttu-id="622ca-3744">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3744">Return Value</span></span>

<span data-ttu-id="622ca-3745">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="622ca-3745">The handle for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3746">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3746">Remarks</span></span>

<span data-ttu-id="622ca-3747">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3747">The handle can be used with the Windows API.</span></span>

### <a name="method-imemode"></a><span data-ttu-id="622ca-3748">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3748">Method iMEMode</span></span>

    public int iMEMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3749">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3749">Parameters</span></span>

<span data-ttu-id="622ca-3750">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3750">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3751">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3751">Return Value</span></span>

### <a name="method-iscontainer"></a><span data-ttu-id="622ca-3752">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="622ca-3752">Method isContainer</span></span>

    public boolean isContainer()

#### <a name="return-value"></a><span data-ttu-id="622ca-3753">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3753">Return Value</span></span>

### <a name="method-isdisplayed"></a><span data-ttu-id="622ca-3754">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="622ca-3754">Method isDisplayed</span></span>

<span data-ttu-id="622ca-3755">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3755">Retrieves a value that indicates whether the control is displayed.</span></span>

    public boolean isDisplayed()

#### <a name="return-value"></a><span data-ttu-id="622ca-3756">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3756">Return Value</span></span>

<span data-ttu-id="622ca-3757">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3757">true if the control is displayed; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3758">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3758">Remarks</span></span>

<span data-ttu-id="622ca-3759">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3759">To modify the visible state of the control, call the visible method.</span></span>

### <a name="method-isrestricted"></a><span data-ttu-id="622ca-3760">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="622ca-3760">Method isRestricted</span></span>

<span data-ttu-id="622ca-3761">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3761">Retrieves a value that indicates whether the control is restricted.</span></span>

    public boolean isRestricted()

#### <a name="return-value"></a><span data-ttu-id="622ca-3762">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3762">Return Value</span></span>

<span data-ttu-id="622ca-3763">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3763">true if the control is restricted; otherwise, false.</span></span>

### <a name="method-isusersetupenabled"></a><span data-ttu-id="622ca-3764">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="622ca-3764">Method isUserSetupEnabled</span></span>

<span data-ttu-id="622ca-3765">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3765">Returns a value that indicates whether the control allows for the specified level of customization.</span></span>

    public boolean isUserSetupEnabled(int neededSetupRights)

#### <a name="parameters"></a><span data-ttu-id="622ca-3766">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3766">Parameters</span></span>

<span data-ttu-id="622ca-3767">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="622ca-3767">neededSetupRights</span></span>  
<span data-ttu-id="622ca-3768">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3768">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3769">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3769">Return Value</span></span>

<span data-ttu-id="622ca-3770">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3770">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3771">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3771">Remarks</span></span>

<span data-ttu-id="622ca-3772">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3772">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-3773">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="622ca-3773">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="622ca-3774">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3774">No changes can be made to the control.</span></span> <span data-ttu-id="622ca-3775">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3775">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="622ca-3776">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="622ca-3776">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="622ca-3777">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3777">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="622ca-3778">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3778">The user cannot move the control.</span></span>   |
| <span data-ttu-id="622ca-3779">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="622ca-3779">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="622ca-3780">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3780">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="622ca-3781">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3781">The user can also move the control.</span></span> |

<span data-ttu-id="622ca-3782">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-3782">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="method-isvalid"></a><span data-ttu-id="622ca-3783">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="622ca-3783">Method isValid</span></span>

    public boolean isValid()

#### <a name="return-value"></a><span data-ttu-id="622ca-3784">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3784">Return Value</span></span>

### <a name="method-italic"></a><span data-ttu-id="622ca-3785">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="622ca-3785">Method italic</span></span>

    public boolean italic([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3786">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3786">Parameters</span></span>

<span data-ttu-id="622ca-3787">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3787">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3788">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3788">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="622ca-3789">メソッド label</span><span class="sxs-lookup"><span data-stu-id="622ca-3789">Method label</span></span>

<span data-ttu-id="622ca-3790">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3790">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3791">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3791">Parameters</span></span>

<span data-ttu-id="622ca-3792">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3792">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3793">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3793">Return Value</span></span>

<span data-ttu-id="622ca-3794">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3794">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3795">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3795">Remarks</span></span>

<span data-ttu-id="622ca-3796">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3796">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="622ca-3797">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-3797">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-labelalignment"></a><span data-ttu-id="622ca-3798">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="622ca-3798">Method labelAlignment</span></span>

    public int labelAlignment([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3799">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3799">Parameters</span></span>

<span data-ttu-id="622ca-3800">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3800">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3801">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3801">Return Value</span></span>

### <a name="method-labelbold"></a><span data-ttu-id="622ca-3802">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="622ca-3802">Method labelBold</span></span>

    public int labelBold([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3803">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3803">Parameters</span></span>

<span data-ttu-id="622ca-3804">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3804">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3805">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3805">Return Value</span></span>

### <a name="method-labelcharacterset"></a><span data-ttu-id="622ca-3806">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="622ca-3806">Method labelCharacterSet</span></span>

    public int labelCharacterSet([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3807">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3807">Parameters</span></span>

<span data-ttu-id="622ca-3808">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3808">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3809">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3809">Return Value</span></span>

### <a name="method-labelfont"></a><span data-ttu-id="622ca-3810">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="622ca-3810">Method labelFont</span></span>

    public str labelFont([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3811">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3811">Parameters</span></span>

<span data-ttu-id="622ca-3812">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3812">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3813">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3813">Return Value</span></span>

### <a name="method-labelfontsize"></a><span data-ttu-id="622ca-3814">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="622ca-3814">Method labelFontSize</span></span>

    public int labelFontSize([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3815">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3815">Parameters</span></span>

<span data-ttu-id="622ca-3816">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3816">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3817">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3817">Return Value</span></span>

### <a name="method-labelforegroundcolor"></a><span data-ttu-id="622ca-3818">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="622ca-3818">Method labelForegroundColor</span></span>

    public int labelForegroundColor([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3819">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3819">Parameters</span></span>

<span data-ttu-id="622ca-3820">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3820">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3821">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3821">Return Value</span></span>

### <a name="method-labelguide"></a><span data-ttu-id="622ca-3822">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="622ca-3822">Method labelGuide</span></span>

    public int labelGuide([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3823">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3823">Parameters</span></span>

<span data-ttu-id="622ca-3824">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3824">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3825">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3825">Return Value</span></span>

### <a name="method-labelheight"></a><span data-ttu-id="622ca-3826">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="622ca-3826">Method labelHeight</span></span>

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3827">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3827">Parameters</span></span>

<span data-ttu-id="622ca-3828">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3828">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-3829">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3829">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3830">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3830">Return Value</span></span>

### <a name="method-labelheightmode"></a><span data-ttu-id="622ca-3831">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3831">Method labelHeightMode</span></span>

    public int labelHeightMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3832">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3832">Parameters</span></span>

<span data-ttu-id="622ca-3833">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3833">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3834">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3834">Return Value</span></span>

### <a name="method-labelheightvalue"></a><span data-ttu-id="622ca-3835">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="622ca-3835">Method labelHeightValue</span></span>

    public int labelHeightValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3836">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3836">Parameters</span></span>

<span data-ttu-id="622ca-3837">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3837">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3838">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3838">Return Value</span></span>

### <a name="method-labelitalic"></a><span data-ttu-id="622ca-3839">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="622ca-3839">Method labelItalic</span></span>

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3840">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3840">Parameters</span></span>

<span data-ttu-id="622ca-3841">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3841">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3842">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3842">Return Value</span></span>

### <a name="method-labelmousedblclick"></a><span data-ttu-id="622ca-3843">メソッド labelMouseDblClick</span><span class="sxs-lookup"><span data-stu-id="622ca-3843">Method labelMouseDblClick</span></span>

    public int labelMouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-3844">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3844">Parameters</span></span>

<span data-ttu-id="622ca-3845">x</span><span class="sxs-lookup"><span data-stu-id="622ca-3845">x</span></span>  

<!-- -->

<span data-ttu-id="622ca-3846">y</span><span class="sxs-lookup"><span data-stu-id="622ca-3846">y</span></span>  

<!-- -->

<span data-ttu-id="622ca-3847">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-3847">button</span></span>  

<!-- -->

<span data-ttu-id="622ca-3848">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-3848">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="622ca-3849">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-3849">Shift</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3850">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3850">Return Value</span></span>

### <a name="method-labelmousedown"></a><span data-ttu-id="622ca-3851">メソッド labelMouseDown</span><span class="sxs-lookup"><span data-stu-id="622ca-3851">Method labelMouseDown</span></span>

    public int labelMouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-3852">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3852">Parameters</span></span>

<span data-ttu-id="622ca-3853">x</span><span class="sxs-lookup"><span data-stu-id="622ca-3853">x</span></span>  

<!-- -->

<span data-ttu-id="622ca-3854">y</span><span class="sxs-lookup"><span data-stu-id="622ca-3854">y</span></span>  

<!-- -->

<span data-ttu-id="622ca-3855">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-3855">button</span></span>  

<!-- -->

<span data-ttu-id="622ca-3856">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-3856">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="622ca-3857">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-3857">Shift</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3858">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3858">Return Value</span></span>

### <a name="method-labelmouseup"></a><span data-ttu-id="622ca-3859">メソッド labelMouseUp</span><span class="sxs-lookup"><span data-stu-id="622ca-3859">Method labelMouseUp</span></span>

    public int labelMouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-3860">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3860">Parameters</span></span>

<span data-ttu-id="622ca-3861">x</span><span class="sxs-lookup"><span data-stu-id="622ca-3861">x</span></span>  

<!-- -->

<span data-ttu-id="622ca-3862">y</span><span class="sxs-lookup"><span data-stu-id="622ca-3862">y</span></span>  

<!-- -->

<span data-ttu-id="622ca-3863">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-3863">button</span></span>  

<!-- -->

<span data-ttu-id="622ca-3864">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-3864">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="622ca-3865">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-3865">Shift</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3866">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3866">Return Value</span></span>

### <a name="method-labelposition"></a><span data-ttu-id="622ca-3867">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="622ca-3867">Method labelPosition</span></span>

    public int labelPosition([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3868">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3868">Parameters</span></span>

<span data-ttu-id="622ca-3869">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3869">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3870">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3870">Return Value</span></span>

### <a name="method-labelunderline"></a><span data-ttu-id="622ca-3871">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="622ca-3871">Method labelUnderline</span></span>

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3872">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3872">Parameters</span></span>

<span data-ttu-id="622ca-3873">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3873">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3874">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3874">Return Value</span></span>

### <a name="method-labelwidth"></a><span data-ttu-id="622ca-3875">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="622ca-3875">Method labelWidth</span></span>

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3876">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3876">Parameters</span></span>

<span data-ttu-id="622ca-3877">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3877">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-3878">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3878">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3879">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3879">Return Value</span></span>

### <a name="method-labelwidthmode"></a><span data-ttu-id="622ca-3880">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3880">Method labelWidthMode</span></span>

    public int labelWidthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3881">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3881">Parameters</span></span>

<span data-ttu-id="622ca-3882">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3882">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3883">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3883">Return Value</span></span>

### <a name="method-labelwidthvalue"></a><span data-ttu-id="622ca-3884">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="622ca-3884">Method labelWidthValue</span></span>

    public int labelWidthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3885">Parameters</span></span>

<span data-ttu-id="622ca-3886">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3886">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3887">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3887">Return Value</span></span>

### <a name="method-leave"></a><span data-ttu-id="622ca-3888">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="622ca-3888">Method leave</span></span>

    public boolean leave()

#### <a name="return-value"></a><span data-ttu-id="622ca-3889">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3889">Return Value</span></span>

### <a name="method-left"></a><span data-ttu-id="622ca-3890">メソッド left</span><span class="sxs-lookup"><span data-stu-id="622ca-3890">Method left</span></span>

<span data-ttu-id="622ca-3891">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3891">Gets or sets the horizontal position of the control in the form.</span></span>

    public int left(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3892">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3892">Parameters</span></span>

<span data-ttu-id="622ca-3893">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3893">value</span></span>  
<span data-ttu-id="622ca-3894">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-3894">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-3895">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3895">mode</span></span>  
<span data-ttu-id="622ca-3896">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-3896">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3897">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3897">Return Value</span></span>

<span data-ttu-id="622ca-3898">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-3898">The horizontal position of the control in the form.</span></span>

### <a name="method-leftmode"></a><span data-ttu-id="622ca-3899">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3899">Method leftMode</span></span>

<span data-ttu-id="622ca-3900">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3900">Sets the horizontal arrange mode for the control in the form.</span></span>

    public int leftMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3901">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3901">Parameters</span></span>

<span data-ttu-id="622ca-3902">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3902">value</span></span>  
<span data-ttu-id="622ca-3903">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-3903">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3904">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3904">Return Value</span></span>

<span data-ttu-id="622ca-3905">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-3905">The horizontal arrange mode for the control in the form.</span></span>

### <a name="method-leftvalue"></a><span data-ttu-id="622ca-3906">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="622ca-3906">Method leftValue</span></span>

<span data-ttu-id="622ca-3907">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-3907">Gets or sets the horizontal position of the control in the form.</span></span>

    public int leftValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3908">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3908">Parameters</span></span>

<span data-ttu-id="622ca-3909">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3909">value</span></span>  
<span data-ttu-id="622ca-3910">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-3910">An integer value that indicates the horizontal position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3911">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3911">Return Value</span></span>

<span data-ttu-id="622ca-3912">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-3912">The horizontal position of the control in the form.</span></span>

### <a name="method-limittext"></a><span data-ttu-id="622ca-3913">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="622ca-3913">Method limitText</span></span>

    public int limitText([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3914">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3914">Parameters</span></span>

<span data-ttu-id="622ca-3915">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3915">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-3916">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3916">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3917">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3917">Return Value</span></span>

### <a name="method-limittextmode"></a><span data-ttu-id="622ca-3918">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3918">Method limitTextMode</span></span>

    public AutoMode limitTextMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3919">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3919">Parameters</span></span>

<span data-ttu-id="622ca-3920">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3920">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3921">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3921">Return Value</span></span>

### <a name="method-limittextvalue"></a><span data-ttu-id="622ca-3922">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="622ca-3922">Method limitTextValue</span></span>

    public int limitTextValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3923">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3923">Parameters</span></span>

<span data-ttu-id="622ca-3924">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3924">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3925">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3925">Return Value</span></span>

### <a name="method-linefromchar"></a><span data-ttu-id="622ca-3926">メソッド lineFromChar</span><span class="sxs-lookup"><span data-stu-id="622ca-3926">Method lineFromChar</span></span>

    public int lineFromChar(int charIndex)

#### <a name="parameters"></a><span data-ttu-id="622ca-3927">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3927">Parameters</span></span>

<span data-ttu-id="622ca-3928">charIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-3928">charIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3929">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3929">Return Value</span></span>

### <a name="method-lineindex"></a><span data-ttu-id="622ca-3930">メソッド lineIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-3930">Method lineIndex</span></span>

    public int lineIndex(int lineNo)

#### <a name="parameters"></a><span data-ttu-id="622ca-3931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3931">Parameters</span></span>

<span data-ttu-id="622ca-3932">lineNo</span><span class="sxs-lookup"><span data-stu-id="622ca-3932">lineNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3933">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3933">Return Value</span></span>

### <a name="method-linelength"></a><span data-ttu-id="622ca-3934">メソッド lineLength</span><span class="sxs-lookup"><span data-stu-id="622ca-3934">Method lineLength</span></span>

    public int lineLength(int lineNo)

#### <a name="parameters"></a><span data-ttu-id="622ca-3935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3935">Parameters</span></span>

<span data-ttu-id="622ca-3936">lineNo</span><span class="sxs-lookup"><span data-stu-id="622ca-3936">lineNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3937">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3937">Return Value</span></span>

### <a name="method-lookupbutton"></a><span data-ttu-id="622ca-3938">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="622ca-3938">Method lookupButton</span></span>

    public int lookupButton([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3939">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3939">Parameters</span></span>

<span data-ttu-id="622ca-3940">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3940">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3941">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3941">Return Value</span></span>

### <a name="method-mandatory"></a><span data-ttu-id="622ca-3942">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="622ca-3942">Method mandatory</span></span>

    public boolean mandatory([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3943">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3943">Parameters</span></span>

<span data-ttu-id="622ca-3944">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3944">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3945">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3945">Return Value</span></span>

### <a name="method-markasuseradd"></a><span data-ttu-id="622ca-3946">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="622ca-3946">Method markAsUserAdd</span></span>

<span data-ttu-id="622ca-3947">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="622ca-3947">Marks or unmarks the control as a user-added control.</span></span>

    public boolean markAsUserAdd([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3948">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3948">Parameters</span></span>

<span data-ttu-id="622ca-3949">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3949">value</span></span>  
<span data-ttu-id="622ca-3950">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3950">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3951">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3951">Return Value</span></span>

<span data-ttu-id="622ca-3952">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-3952">true if the control was marked as a user-added control; otherwise, false.</span></span>

### <a name="method-minnoofdecimals"></a><span data-ttu-id="622ca-3953">メソッド minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="622ca-3953">Method minNoOfDecimals</span></span>

    public int minNoOfDecimals([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3954">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3954">Parameters</span></span>

<span data-ttu-id="622ca-3955">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3955">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-3956">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3956">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3957">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3957">Return Value</span></span>

### <a name="method-minnoofdecimalsmode"></a><span data-ttu-id="622ca-3958">メソッド minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="622ca-3958">Method minNoOfDecimalsMode</span></span>

    public AutoMode minNoOfDecimalsMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-3959">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3959">Parameters</span></span>

<span data-ttu-id="622ca-3960">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-3960">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3961">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3961">Return Value</span></span>

### <a name="method-minnoofdecimalsvalue"></a><span data-ttu-id="622ca-3962">メソッド minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="622ca-3962">Method minNoOfDecimalsValue</span></span>

    public int minNoOfDecimalsValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-3963">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3963">Parameters</span></span>

<span data-ttu-id="622ca-3964">値</span><span class="sxs-lookup"><span data-stu-id="622ca-3964">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-3965">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3965">Return Value</span></span>

### <a name="method-modified"></a><span data-ttu-id="622ca-3966">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="622ca-3966">Method modified</span></span>

    public boolean modified()

#### <a name="return-value"></a><span data-ttu-id="622ca-3967">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3967">Return Value</span></span>

### <a name="method-mousedblclick"></a><span data-ttu-id="622ca-3968">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="622ca-3968">Method mouseDblClick</span></span>

<span data-ttu-id="622ca-3969">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3969">Is called when the control is double-clicked by the user.</span></span>

    public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-3970">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3970">Parameters</span></span>

<span data-ttu-id="622ca-3971">x</span><span class="sxs-lookup"><span data-stu-id="622ca-3971">x</span></span>  
<span data-ttu-id="622ca-3972">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3972">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-3973">y</span><span class="sxs-lookup"><span data-stu-id="622ca-3973">y</span></span>  
<span data-ttu-id="622ca-3974">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3974">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-3975">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-3975">button</span></span>  
<span data-ttu-id="622ca-3976">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3976">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-3977">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-3977">Ctrl</span></span>  
<span data-ttu-id="622ca-3978">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3978">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-3979">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-3979">Shift</span></span>  
<span data-ttu-id="622ca-3980">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3980">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3981">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3981">Return Value</span></span>

<span data-ttu-id="622ca-3982">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3982">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-3983">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-3983">Remarks</span></span>

<span data-ttu-id="622ca-3984">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3984">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mousedown"></a><span data-ttu-id="622ca-3985">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="622ca-3985">Method mouseDown</span></span>

<span data-ttu-id="622ca-3986">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-3986">Is called when the user clicks the mouse button over the control.</span></span>

    public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-3987">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-3987">Parameters</span></span>

<span data-ttu-id="622ca-3988">x</span><span class="sxs-lookup"><span data-stu-id="622ca-3988">x</span></span>  
<span data-ttu-id="622ca-3989">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3989">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-3990">y</span><span class="sxs-lookup"><span data-stu-id="622ca-3990">y</span></span>  
<span data-ttu-id="622ca-3991">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3991">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-3992">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-3992">button</span></span>  
<span data-ttu-id="622ca-3993">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3993">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-3994">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-3994">Ctrl</span></span>  
<span data-ttu-id="622ca-3995">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3995">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-3996">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-3996">Shift</span></span>  
<span data-ttu-id="622ca-3997">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-3997">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-3998">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-3998">Return Value</span></span>

<span data-ttu-id="622ca-3999">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-3999">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4000">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4000">Remarks</span></span>

<span data-ttu-id="622ca-4001">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4001">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="622ca-4002">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4002">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-mousemove"></a><span data-ttu-id="622ca-4003">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="622ca-4003">Method mouseMove</span></span>

<span data-ttu-id="622ca-4004">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4004">Is called when the user moves the mouse pointer over the control.</span></span>

    public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-4005">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4005">Parameters</span></span>

<span data-ttu-id="622ca-4006">x</span><span class="sxs-lookup"><span data-stu-id="622ca-4006">x</span></span>  
<span data-ttu-id="622ca-4007">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4007">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4008">y</span><span class="sxs-lookup"><span data-stu-id="622ca-4008">y</span></span>  
<span data-ttu-id="622ca-4009">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4009">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4010">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-4010">button</span></span>  
<span data-ttu-id="622ca-4011">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4011">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4012">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-4012">Ctrl</span></span>  
<span data-ttu-id="622ca-4013">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4013">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4014">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-4014">Shift</span></span>  
<span data-ttu-id="622ca-4015">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4015">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4016">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4016">Return Value</span></span>

<span data-ttu-id="622ca-4017">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-4017">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4018">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4018">Remarks</span></span>

<span data-ttu-id="622ca-4019">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4019">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="method-mouseup"></a><span data-ttu-id="622ca-4020">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="622ca-4020">Method mouseUp</span></span>

<span data-ttu-id="622ca-4021">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4021">Is called when the user releases the mouse button over the control area.</span></span>

    public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-4022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4022">Parameters</span></span>

<span data-ttu-id="622ca-4023">x</span><span class="sxs-lookup"><span data-stu-id="622ca-4023">x</span></span>  
<span data-ttu-id="622ca-4024">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4024">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4025">y</span><span class="sxs-lookup"><span data-stu-id="622ca-4025">y</span></span>  
<span data-ttu-id="622ca-4026">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4026">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4027">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-4027">button</span></span>  
<span data-ttu-id="622ca-4028">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4028">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4029">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-4029">Ctrl</span></span>  
<span data-ttu-id="622ca-4030">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4030">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4031">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-4031">Shift</span></span>  
<span data-ttu-id="622ca-4032">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4032">A Boolean value that indicates whether the SHIFT key is down.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4033">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4033">Return Value</span></span>

<span data-ttu-id="622ca-4034">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="622ca-4034">0 (zero) if the event has been handled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4035">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4035">Remarks</span></span>

<span data-ttu-id="622ca-4036">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4036">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="622ca-4037">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4037">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="method-name"></a><span data-ttu-id="622ca-4038">メソッド名</span><span class="sxs-lookup"><span data-stu-id="622ca-4038">Method name</span></span>

<span data-ttu-id="622ca-4039">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4039">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4040">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4040">Parameters</span></span>

<span data-ttu-id="622ca-4041">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4041">value</span></span>  
<span data-ttu-id="622ca-4042">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-4042">The name to assign to the control.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4043">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4043">Return Value</span></span>

<span data-ttu-id="622ca-4044">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="622ca-4044">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4045">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4045">Remarks</span></span>

<span data-ttu-id="622ca-4046">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-4046">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="622ca-4047">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="622ca-4047">It must start with a letter.</span></span>
-   <span data-ttu-id="622ca-4048">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-4048">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="622ca-4049">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4049">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="622ca-4050">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-4050">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="622ca-4051">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="622ca-4051">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-neededpermission"></a><span data-ttu-id="622ca-4052">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="622ca-4052">Method neededPermission</span></span>

    public int neededPermission([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4053">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4053">Parameters</span></span>

<span data-ttu-id="622ca-4054">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4054">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4055">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4055">Return Value</span></span>

### <a name="method-noofdecimals"></a><span data-ttu-id="622ca-4056">メソッド noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="622ca-4056">Method noOfDecimals</span></span>

    public int noOfDecimals([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-4057">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4057">Parameters</span></span>

<span data-ttu-id="622ca-4058">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4058">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-4059">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-4059">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4060">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4060">Return Value</span></span>

### <a name="method-noofdecimalsmode"></a><span data-ttu-id="622ca-4061">メソッド noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="622ca-4061">Method noOfDecimalsMode</span></span>

    public AutoMode noOfDecimalsMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-4062">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4062">Parameters</span></span>

<span data-ttu-id="622ca-4063">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-4063">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4064">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4064">Return Value</span></span>

### <a name="method-noofdecimalsvalue"></a><span data-ttu-id="622ca-4065">メソッド noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="622ca-4065">Method noOfDecimalsValue</span></span>

    public int noOfDecimalsValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4066">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4066">Parameters</span></span>

<span data-ttu-id="622ca-4067">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4067">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4068">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4068">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="622ca-4069">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="622ca-4069">Method SysObsoleteAttribute</span></span>

    public container SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="622ca-4070">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4070">Return Value</span></span>

### <a name="method-parentcontrol"></a><span data-ttu-id="622ca-4071">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="622ca-4071">Method parentControl</span></span>

<span data-ttu-id="622ca-4072">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4072">Retrieves the parent control for the control.</span></span>

    public FormControl parentControl()

#### <a name="return-value"></a><span data-ttu-id="622ca-4073">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4073">Return Value</span></span>

<span data-ttu-id="622ca-4074">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="622ca-4074">The parent control for the control.</span></span>

### <a name="method-posfromchar"></a><span data-ttu-id="622ca-4075">メソッド posFromChar</span><span class="sxs-lookup"><span data-stu-id="622ca-4075">Method posFromChar</span></span>

    public container posFromChar(int charIndex)

#### <a name="parameters"></a><span data-ttu-id="622ca-4076">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4076">Parameters</span></span>

<span data-ttu-id="622ca-4077">charIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-4077">charIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4078">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4078">Return Value</span></span>

### <a name="method-previewpartref"></a><span data-ttu-id="622ca-4079">メソッド previewPartRef</span><span class="sxs-lookup"><span data-stu-id="622ca-4079">Method previewPartRef</span></span>

    public str previewPartRef([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4080">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4080">Parameters</span></span>

<span data-ttu-id="622ca-4081">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4081">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4082">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4082">Return Value</span></span>

### <a name="method-promptrect"></a><span data-ttu-id="622ca-4083">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="622ca-4083">Method promptrect</span></span>

    public int promptrect([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4084">Parameters</span></span>

<span data-ttu-id="622ca-4085">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4085">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4086">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4086">Return Value</span></span>

### <a name="method-realvalue"></a><span data-ttu-id="622ca-4087">メソッド realValue</span><span class="sxs-lookup"><span data-stu-id="622ca-4087">Method realValue</span></span>

    public Real realValue([Real value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4088">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4088">Parameters</span></span>

<span data-ttu-id="622ca-4089">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4089">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4090">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4090">Return Value</span></span>

### <a name="method-replaceonlookup"></a><span data-ttu-id="622ca-4091">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="622ca-4091">Method replaceOnLookup</span></span>

    public boolean replaceOnLookup([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4092">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4092">Parameters</span></span>

<span data-ttu-id="622ca-4093">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4093">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4094">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4094">Return Value</span></span>

### <a name="method-rotatesign"></a><span data-ttu-id="622ca-4095">メソッド rotateSign</span><span class="sxs-lookup"><span data-stu-id="622ca-4095">Method rotateSign</span></span>

    public int rotateSign([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4096">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4096">Parameters</span></span>

<span data-ttu-id="622ca-4097">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4097">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4098">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4098">Return Value</span></span>

### <a name="method-searchafterinput"></a><span data-ttu-id="622ca-4099">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="622ca-4099">Method searchAfterInput</span></span>

    public int searchAfterInput([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4100">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4100">Parameters</span></span>

<span data-ttu-id="622ca-4101">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4101">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4102">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4102">Return Value</span></span>

### <a name="method-searchmode"></a><span data-ttu-id="622ca-4103">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="622ca-4103">Method searchMode</span></span>

    public int searchMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4104">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4104">Parameters</span></span>

<span data-ttu-id="622ca-4105">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4105">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4106">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4106">Return Value</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="622ca-4107">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="622ca-4107">Method securityKey</span></span>

<span data-ttu-id="622ca-4108">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4108">Sets or returns the ID of the security key for the control.</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4109">Parameters</span></span>

<span data-ttu-id="622ca-4110">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4110">value</span></span>  
<span data-ttu-id="622ca-4111">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4111">The ID of the security key to assign to the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4112">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4112">Return Value</span></span>

<span data-ttu-id="622ca-4113">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4113">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="method-showcontextmenu"></a><span data-ttu-id="622ca-4114">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="622ca-4114">Method showContextMenu</span></span>

<span data-ttu-id="622ca-4115">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4115">Shows the shortcut menu for the control.</span></span>

    public int showContextMenu(int menuHandle)

#### <a name="parameters"></a><span data-ttu-id="622ca-4116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4116">Parameters</span></span>

<span data-ttu-id="622ca-4117">menuHandle</span><span class="sxs-lookup"><span data-stu-id="622ca-4117">menuHandle</span></span>  
<span data-ttu-id="622ca-4118">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="622ca-4118">The ID of the menu to show.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4119">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4119">Return Value</span></span>

<span data-ttu-id="622ca-4120">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4120">An integer value that indicates whether the call succeeded.</span></span>

### <a name="method-showlabel"></a><span data-ttu-id="622ca-4121">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="622ca-4121">Method showLabel</span></span>

    public boolean showLabel([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4122">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4122">Parameters</span></span>

<span data-ttu-id="622ca-4123">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4123">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4124">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4124">Return Value</span></span>

### <a name="method-showzero"></a><span data-ttu-id="622ca-4125">メソッド showZero</span><span class="sxs-lookup"><span data-stu-id="622ca-4125">Method showZero</span></span>

    public int showZero([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4126">Parameters</span></span>

<span data-ttu-id="622ca-4127">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4127">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4128">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4128">Return Value</span></span>

### <a name="method-signdisplay"></a><span data-ttu-id="622ca-4129">メソッド signDisplay</span><span class="sxs-lookup"><span data-stu-id="622ca-4129">Method signDisplay</span></span>

    public int signDisplay([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4130">Parameters</span></span>

<span data-ttu-id="622ca-4131">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4131">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4132">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4132">Return Value</span></span>

### <a name="method-skip"></a><span data-ttu-id="622ca-4133">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="622ca-4133">Method skip</span></span>

<span data-ttu-id="622ca-4134">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4134">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

    public boolean skip([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4135">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4135">Parameters</span></span>

<span data-ttu-id="622ca-4136">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4136">value</span></span>  
<span data-ttu-id="622ca-4137">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4137">The value to assign to the skip property of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4138">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4138">Return Value</span></span>

<span data-ttu-id="622ca-4139">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="622ca-4139">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4140">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4140">Remarks</span></span>

<span data-ttu-id="622ca-4141">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4141">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

### <a name="method-sort"></a><span data-ttu-id="622ca-4142">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="622ca-4142">Method sort</span></span>

    public int sort([SortOrder sortDirection])

#### <a name="parameters"></a><span data-ttu-id="622ca-4143">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4143">Parameters</span></span>

<span data-ttu-id="622ca-4144">sortDirection</span><span class="sxs-lookup"><span data-stu-id="622ca-4144">sortDirection</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4145">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4145">Return Value</span></span>

### <a name="method-style"></a><span data-ttu-id="622ca-4146">メソッド style</span><span class="sxs-lookup"><span data-stu-id="622ca-4146">Method style</span></span>

    public int style([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4147">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4147">Parameters</span></span>

<span data-ttu-id="622ca-4148">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4148">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4149">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4149">Return Value</span></span>

### <a name="method-thousandseparator"></a><span data-ttu-id="622ca-4150">メソッド thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="622ca-4150">Method thousandSeparator</span></span>

    public int thousandSeparator([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4151">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4151">Parameters</span></span>

<span data-ttu-id="622ca-4152">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4152">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4153">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4153">Return Value</span></span>

### <a name="method-tooltip"></a><span data-ttu-id="622ca-4154">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="622ca-4154">Method toolTip</span></span>

<span data-ttu-id="622ca-4155">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4155">Retrieves the tooltip text for the control.</span></span>

    public str toolTip()

#### <a name="return-value"></a><span data-ttu-id="622ca-4156">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4156">Return Value</span></span>

<span data-ttu-id="622ca-4157">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="622ca-4157">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4158">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4158">Remarks</span></span>

<span data-ttu-id="622ca-4159">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4159">The method might be overridden to provide a value to the toolTip method.</span></span>

### <a name="method-top"></a><span data-ttu-id="622ca-4160">メソッド top</span><span class="sxs-lookup"><span data-stu-id="622ca-4160">Method top</span></span>

<span data-ttu-id="622ca-4161">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4161">Gets or sets the vertical position of the control in the form.</span></span>

    public int top(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-4162">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4162">Parameters</span></span>

<span data-ttu-id="622ca-4163">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4163">value</span></span>  
<span data-ttu-id="622ca-4164">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4164">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-4165">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-4165">mode</span></span>  
<span data-ttu-id="622ca-4166">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4166">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4167">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4167">Return Value</span></span>

<span data-ttu-id="622ca-4168">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-4168">The vertical position of the control in the form.</span></span>

### <a name="method-topmode"></a><span data-ttu-id="622ca-4169">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="622ca-4169">Method topMode</span></span>

<span data-ttu-id="622ca-4170">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4170">Sets the vertical arrange mode for the control in the form.</span></span>

    public int topMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4171">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4171">Parameters</span></span>

<span data-ttu-id="622ca-4172">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4172">value</span></span>  
<span data-ttu-id="622ca-4173">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4173">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4174">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4174">Return Value</span></span>

<span data-ttu-id="622ca-4175">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-4175">The vertical arrange mode for the control in the form.</span></span>

### <a name="method-topvalue"></a><span data-ttu-id="622ca-4176">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="622ca-4176">Method topValue</span></span>

<span data-ttu-id="622ca-4177">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4177">Gets or sets the vertical position of the control in the form.</span></span>

    public int topValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4178">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4178">Parameters</span></span>

<span data-ttu-id="622ca-4179">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4179">value</span></span>  
<span data-ttu-id="622ca-4180">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4180">An integer value that indicates the vertical position of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4181">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4181">Return Value</span></span>

<span data-ttu-id="622ca-4182">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="622ca-4182">The vertical position of the control in the form.</span></span>

### <a name="method-type"></a><span data-ttu-id="622ca-4183">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="622ca-4183">Method type</span></span>

    public int type([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4184">Parameters</span></span>

<span data-ttu-id="622ca-4185">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4185">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4186">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4186">Return Value</span></span>

### <a name="method-underline"></a><span data-ttu-id="622ca-4187">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="622ca-4187">Method underline</span></span>

    public boolean underline([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4188">Parameters</span></span>

<span data-ttu-id="622ca-4189">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4189">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4190">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4190">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="622ca-4191">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="622ca-4191">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(container data)

#### <a name="parameters"></a><span data-ttu-id="622ca-4192">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4192">Parameters</span></span>

<span data-ttu-id="622ca-4193">データ</span><span class="sxs-lookup"><span data-stu-id="622ca-4193">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4194">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4194">Return Value</span></span>

### <a name="method-userdata"></a><span data-ttu-id="622ca-4195">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="622ca-4195">Method userData</span></span>

<span data-ttu-id="622ca-4196">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4196">Gets or sets the user data for the control.</span></span>

    public int userData([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4197">Parameters</span></span>

<span data-ttu-id="622ca-4198">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4198">value</span></span>  
<span data-ttu-id="622ca-4199">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4199">An integer value that indicates the user data for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4200">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4200">Return Value</span></span>

<span data-ttu-id="622ca-4201">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="622ca-4201">The user data for the control.</span></span>

### <a name="method-userdataitem"></a><span data-ttu-id="622ca-4202">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="622ca-4202">Method userDataItem</span></span>

<span data-ttu-id="622ca-4203">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4203">Gets or sets the user data item for the control.</span></span>

    public int userDataItem([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4204">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4204">Parameters</span></span>

<span data-ttu-id="622ca-4205">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4205">value</span></span>  
<span data-ttu-id="622ca-4206">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4206">An integer value that indicates the user data item for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4207">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4207">Return Value</span></span>

<span data-ttu-id="622ca-4208">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="622ca-4208">The user data item for the control.</span></span>

### <a name="method-userdataitems"></a><span data-ttu-id="622ca-4209">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="622ca-4209">Method userDataItems</span></span>

<span data-ttu-id="622ca-4210">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4210">Gets or sets the number of user data items for the control.</span></span>

    public int userDataItems([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4211">Parameters</span></span>

<span data-ttu-id="622ca-4212">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4212">value</span></span>  
<span data-ttu-id="622ca-4213">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4213">An integer value that indicates the number of user data items for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4214">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4214">Return Value</span></span>

<span data-ttu-id="622ca-4215">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="622ca-4215">The number of user data items for the control.</span></span>

### <a name="method-userdisable"></a><span data-ttu-id="622ca-4216">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="622ca-4216">Method userDisable</span></span>

<span data-ttu-id="622ca-4217">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4217">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

    public int userDisable([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4218">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4218">Parameters</span></span>

<span data-ttu-id="622ca-4219">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4219">value</span></span>  
<span data-ttu-id="622ca-4220">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4220">The value that indicates whether the control is disabled for the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4221">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4221">Return Value</span></span>

<span data-ttu-id="622ca-4222">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-4222">1 if the control is disabled for the user; otherwise, 0.</span></span>

### <a name="method-userfasttabsummary"></a><span data-ttu-id="622ca-4223">メソッド userFastTabSummary</span><span class="sxs-lookup"><span data-stu-id="622ca-4223">Method userFastTabSummary</span></span>

    public int userFastTabSummary([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4224">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4224">Parameters</span></span>

<span data-ttu-id="622ca-4225">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4225">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4226">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4226">Return Value</span></span>

### <a name="method-userheight"></a><span data-ttu-id="622ca-4227">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="622ca-4227">Method userHeight</span></span>

<span data-ttu-id="622ca-4228">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4228">Gets or sets the custom user height for the control.</span></span>

    public int userHeight([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4229">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4229">Parameters</span></span>

<span data-ttu-id="622ca-4230">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4230">value</span></span>  
<span data-ttu-id="622ca-4231">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4231">The user height for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4232">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4232">Return Value</span></span>

<span data-ttu-id="622ca-4233">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="622ca-4233">The custom user height for the control.</span></span>

### <a name="method-userhide"></a><span data-ttu-id="622ca-4234">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="622ca-4234">Method userHide</span></span>

<span data-ttu-id="622ca-4235">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4235">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

    public int userHide([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4236">Parameters</span></span>

<span data-ttu-id="622ca-4237">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4237">value</span></span>  
<span data-ttu-id="622ca-4238">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4238">The value that indicates whether the control is hidden from the user; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4239">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4239">Return Value</span></span>

<span data-ttu-id="622ca-4240">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-4240">1 if the control is hidden from the user; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4241">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4241">Remarks</span></span>

<span data-ttu-id="622ca-4242">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4242">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="622ca-4243">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4243">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="622ca-4244">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4244">This method lets you programmatically determine and set the value.</span></span>

### <a name="method-userorgcontainer"></a><span data-ttu-id="622ca-4245">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="622ca-4245">Method userOrgContainer</span></span>

<span data-ttu-id="622ca-4246">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4246">Gets or sets the organization container for the control.</span></span>

    public int userOrgContainer([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4247">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4247">Parameters</span></span>

<span data-ttu-id="622ca-4248">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4248">value</span></span>  
<span data-ttu-id="622ca-4249">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4249">The organization container to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4250">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4250">Return Value</span></span>

<span data-ttu-id="622ca-4251">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="622ca-4251">The organization container for the control.</span></span>

### <a name="method-userorgsibling"></a><span data-ttu-id="622ca-4252">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="622ca-4252">Method userOrgSibling</span></span>

<span data-ttu-id="622ca-4253">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4253">Gets or sets the organization sibling for the control.</span></span>

    public int userOrgSibling([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4254">Parameters</span></span>

<span data-ttu-id="622ca-4255">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4255">value</span></span>  
<span data-ttu-id="622ca-4256">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4256">The organization sibling to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4257">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4257">Return Value</span></span>

<span data-ttu-id="622ca-4258">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="622ca-4258">The organization sibling for the control.</span></span>

### <a name="method-userprompttext"></a><span data-ttu-id="622ca-4259">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="622ca-4259">Method userPromptText</span></span>

<span data-ttu-id="622ca-4260">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4260">Gets or sets the user label text for the control.</span></span>

    public str userPromptText([str value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4261">Parameters</span></span>

<span data-ttu-id="622ca-4262">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4262">value</span></span>  
<span data-ttu-id="622ca-4263">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4263">The user label text to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4264">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4264">Return Value</span></span>

<span data-ttu-id="622ca-4265">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="622ca-4265">The user label text for the control.</span></span>

### <a name="method-usersecuritylevel"></a><span data-ttu-id="622ca-4266">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="622ca-4266">Method userSecurityLevel</span></span>

<span data-ttu-id="622ca-4267">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4267">Gets or sets the user security level for the control.</span></span>

    public int userSecurityLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4268">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4268">Parameters</span></span>

<span data-ttu-id="622ca-4269">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4269">value</span></span>  
<span data-ttu-id="622ca-4270">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4270">The user security level to set for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4271">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4271">Return Value</span></span>

<span data-ttu-id="622ca-4272">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="622ca-4272">The user security level for the control.</span></span>

### <a name="method-userskip"></a><span data-ttu-id="622ca-4273">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="622ca-4273">Method userSkip</span></span>

<span data-ttu-id="622ca-4274">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4274">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

    public int userSkip([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4275">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4275">Parameters</span></span>

<span data-ttu-id="622ca-4276">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4276">value</span></span>  
<span data-ttu-id="622ca-4277">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4277">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="622ca-4278">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-4278">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4279">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4279">Return Value</span></span>

<span data-ttu-id="622ca-4280">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="622ca-4280">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="method-userwidth"></a><span data-ttu-id="622ca-4281">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="622ca-4281">Method userWidth</span></span>

<span data-ttu-id="622ca-4282">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4282">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

    public int userWidth([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4283">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4283">Parameters</span></span>

<span data-ttu-id="622ca-4284">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4284">value</span></span>  
<span data-ttu-id="622ca-4285">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4285">The number of pixels to use as the width of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4286">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4286">Return Value</span></span>

<span data-ttu-id="622ca-4287">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4287">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4288">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4288">Remarks</span></span>

<span data-ttu-id="622ca-4289">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4289">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="622ca-4290">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="622ca-4290">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="622ca-4291">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4291">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="method-validate"></a><span data-ttu-id="622ca-4292">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="622ca-4292">Method validate</span></span>

    public boolean validate()

#### <a name="return-value"></a><span data-ttu-id="622ca-4293">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4293">Return Value</span></span>

### <a name="method-verticalspacing"></a><span data-ttu-id="622ca-4294">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="622ca-4294">Method verticalSpacing</span></span>

<span data-ttu-id="622ca-4295">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4295">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-4296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4296">Parameters</span></span>

<span data-ttu-id="622ca-4297">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4297">value</span></span>  
<span data-ttu-id="622ca-4298">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4298">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="622ca-4299">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-4299">mode</span></span>  
<span data-ttu-id="622ca-4300">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4300">An integer value that indicates the AutoMode value for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4301">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4301">Return Value</span></span>

<span data-ttu-id="622ca-4302">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="622ca-4302">The vertical spacing of the control in the form.</span></span>

### <a name="method-verticalspacingmode"></a><span data-ttu-id="622ca-4303">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="622ca-4303">Method verticalSpacingMode</span></span>

<span data-ttu-id="622ca-4304">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4304">Sets the vertical spacing mode for the control in the form.</span></span>

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-4305">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4305">Parameters</span></span>

<span data-ttu-id="622ca-4306">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-4306">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4307">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4307">Return Value</span></span>

<span data-ttu-id="622ca-4308">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="622ca-4308">The vertical spacing mode for the control in the form.</span></span>

### <a name="method-verticalspacingvalue"></a><span data-ttu-id="622ca-4309">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="622ca-4309">Method verticalSpacingValue</span></span>

<span data-ttu-id="622ca-4310">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4310">Gets or sets the vertical spacing of the control in the form.</span></span>

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4311">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4311">Parameters</span></span>

<span data-ttu-id="622ca-4312">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4312">value</span></span>  
<span data-ttu-id="622ca-4313">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="622ca-4313">An integer value that indicates the vertical spacing of the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4314">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4314">Return Value</span></span>

<span data-ttu-id="622ca-4315">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="622ca-4315">The vertical spacing of the control in the form.</span></span>

### <a name="method-vieweditmode"></a><span data-ttu-id="622ca-4316">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="622ca-4316">Method viewEditMode</span></span>

    public int viewEditMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4317">Parameters</span></span>

<span data-ttu-id="622ca-4318">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4318">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4319">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4319">Return Value</span></span>

### <a name="method-visible"></a><span data-ttu-id="622ca-4320">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="622ca-4320">Method visible</span></span>

<span data-ttu-id="622ca-4321">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4321">Sets or returns a value that indicates whether the control is visible.</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4322">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4322">Parameters</span></span>

<span data-ttu-id="622ca-4323">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4323">value</span></span>  
<span data-ttu-id="622ca-4324">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4324">The value to assign to the visibility setting for the control; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="622ca-4325">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4325">Return Value</span></span>

<span data-ttu-id="622ca-4326">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="622ca-4326">true if the control is visible; otherwise, false.</span></span>

### <a name="method-width"></a><span data-ttu-id="622ca-4327">メソッド width</span><span class="sxs-lookup"><span data-stu-id="622ca-4327">Method width</span></span>

<span data-ttu-id="622ca-4328">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4328">Gets or sets the width of the control.</span></span>

    public int width(int value, [int mode])

#### <a name="parameters"></a><span data-ttu-id="622ca-4329">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4329">Parameters</span></span>

<span data-ttu-id="622ca-4330">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4330">value</span></span>  

<!-- -->

<span data-ttu-id="622ca-4331">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-4331">mode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4332">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4332">Return Value</span></span>

<span data-ttu-id="622ca-4333">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="622ca-4333">The width of the control in pixels.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4334">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4334">Remarks</span></span>

<span data-ttu-id="622ca-4335">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4335">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="622ca-4336">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4336">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="622ca-4337">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-4337">Mode</span></span>           | <span data-ttu-id="622ca-4338">幅計算</span><span class="sxs-lookup"><span data-stu-id="622ca-4338">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-4339">-1 正確</span><span class="sxs-lookup"><span data-stu-id="622ca-4339">-1 Exact</span></span>       | <span data-ttu-id="622ca-4340">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4340">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-4341">0 自動</span><span class="sxs-lookup"><span data-stu-id="622ca-4341">0 Auto</span></span>         | <span data-ttu-id="622ca-4342">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4342">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-4343">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="622ca-4343">1 Column width</span></span> | <span data-ttu-id="622ca-4344">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-4344">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="622ca-4345">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4345">The width and width calculation mode can be set separately.</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="622ca-4346">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="622ca-4346">Method widthMode</span></span>

<span data-ttu-id="622ca-4347">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4347">Gets or sets the calculation mode of the width of the control.</span></span>

    public int widthMode([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4348">Parameters</span></span>

<span data-ttu-id="622ca-4349">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4349">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4350">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4350">Return Value</span></span>

<span data-ttu-id="622ca-4351">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4351">An integer value that indicates the current calculation mode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4352">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4352">Remarks</span></span>

<span data-ttu-id="622ca-4353">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4353">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="622ca-4354">モード</span><span class="sxs-lookup"><span data-stu-id="622ca-4354">Mode</span></span>         | <span data-ttu-id="622ca-4355">幅計算</span><span class="sxs-lookup"><span data-stu-id="622ca-4355">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="622ca-4356">正確</span><span class="sxs-lookup"><span data-stu-id="622ca-4356">Exact</span></span>        | <span data-ttu-id="622ca-4357">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4357">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="622ca-4358">自動</span><span class="sxs-lookup"><span data-stu-id="622ca-4358">Auto</span></span>         | <span data-ttu-id="622ca-4359">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4359">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="622ca-4360">列の幅</span><span class="sxs-lookup"><span data-stu-id="622ca-4360">Column width</span></span> | <span data-ttu-id="622ca-4361">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="622ca-4361">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="622ca-4362">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="622ca-4362">The width of the control might change when the mode is set to auto or column width.</span></span>

### <a name="method-widthvalue"></a><span data-ttu-id="622ca-4363">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="622ca-4363">Method widthValue</span></span>

<span data-ttu-id="622ca-4364">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4364">Gets or sets the width of the control.</span></span>

    public int widthValue([int value])

#### <a name="parameters"></a><span data-ttu-id="622ca-4365">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4365">Parameters</span></span>

<span data-ttu-id="622ca-4366">値</span><span class="sxs-lookup"><span data-stu-id="622ca-4366">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="622ca-4367">戻り値</span><span class="sxs-lookup"><span data-stu-id="622ca-4367">Return Value</span></span>

<span data-ttu-id="622ca-4368">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="622ca-4368">The width in pixels of the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="622ca-4369">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4369">Remarks</span></span>

<span data-ttu-id="622ca-4370">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4370">To change the width of the control, use the exact width calculation mode.</span></span>

### <a name="method-displaycontrol"></a><span data-ttu-id="622ca-4371">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="622ca-4371">Method displayControl</span></span>

<span data-ttu-id="622ca-4372">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4372">Displays the control.</span></span>

    public void displayControl()

### <a name="method-performtypelookup"></a><span data-ttu-id="622ca-4373">メソッド performTypeLookup</span><span class="sxs-lookup"><span data-stu-id="622ca-4373">Method performTypeLookup</span></span>

    public void performTypeLookup([int userType], [int arrayIndex], [SelectableDataArea company])

#### <a name="parameters"></a><span data-ttu-id="622ca-4374">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4374">Parameters</span></span>

<span data-ttu-id="622ca-4375">userType</span><span class="sxs-lookup"><span data-stu-id="622ca-4375">userType</span></span>  

<!-- -->

<span data-ttu-id="622ca-4376">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="622ca-4376">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="622ca-4377">会社</span><span class="sxs-lookup"><span data-stu-id="622ca-4377">company</span></span>  

### <a name="method-onleaving"></a><span data-ttu-id="622ca-4378">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="622ca-4378">Method OnLeaving</span></span>

    private void OnLeaving([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-4379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4379">Parameters</span></span>

<span data-ttu-id="622ca-4380">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-4380">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-4381">e</span><span class="sxs-lookup"><span data-stu-id="622ca-4381">e</span></span>  

### <a name="method-pastetext"></a><span data-ttu-id="622ca-4382">メソッド pasteText</span><span class="sxs-lookup"><span data-stu-id="622ca-4382">Method pasteText</span></span>

    public void pasteText(str pasteStr, [boolean InsertSel])

#### <a name="parameters"></a><span data-ttu-id="622ca-4383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4383">Parameters</span></span>

<span data-ttu-id="622ca-4384">pasteStr</span><span class="sxs-lookup"><span data-stu-id="622ca-4384">pasteStr</span></span>  

<!-- -->

<span data-ttu-id="622ca-4385">InsertSel</span><span class="sxs-lookup"><span data-stu-id="622ca-4385">InsertSel</span></span>  

### <a name="method-lookup"></a><span data-ttu-id="622ca-4386">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="622ca-4386">Method lookup</span></span>

    public void lookup()

### <a name="method-onvalidated"></a><span data-ttu-id="622ca-4387">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="622ca-4387">Method OnValidated</span></span>

    private void OnValidated([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-4388">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4388">Parameters</span></span>

<span data-ttu-id="622ca-4389">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-4389">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-4390">e</span><span class="sxs-lookup"><span data-stu-id="622ca-4390">e</span></span>  

### <a name="method-onlookup"></a><span data-ttu-id="622ca-4391">メソッド OnLookup</span><span class="sxs-lookup"><span data-stu-id="622ca-4391">Method OnLookup</span></span>

    private void OnLookup([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-4392">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4392">Parameters</span></span>

<span data-ttu-id="622ca-4393">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-4393">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-4394">e</span><span class="sxs-lookup"><span data-stu-id="622ca-4394">e</span></span>  

### <a name="method-filter"></a><span data-ttu-id="622ca-4395">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="622ca-4395">Method filter</span></span>

    public void filter([str filterStr])

#### <a name="parameters"></a><span data-ttu-id="622ca-4396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4396">Parameters</span></span>

<span data-ttu-id="622ca-4397">filterStr</span><span class="sxs-lookup"><span data-stu-id="622ca-4397">filterStr</span></span>  

### <a name="method-mouseleave"></a><span data-ttu-id="622ca-4398">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="622ca-4398">Method mouseLeave</span></span>

<span data-ttu-id="622ca-4399">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4399">Indicates that the mouse pointer has left the control.</span></span>

    public void mouseLeave()

### <a name="method-dragleave"></a><span data-ttu-id="622ca-4400">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="622ca-4400">Method dragLeave</span></span>

<span data-ttu-id="622ca-4401">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4401">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

    public void dragLeave()

### <a name="method-registeroverridemethod"></a><span data-ttu-id="622ca-4402">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="622ca-4402">Method registerOverrideMethod</span></span>

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a><span data-ttu-id="622ca-4403">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4403">Parameters</span></span>

<span data-ttu-id="622ca-4404">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="622ca-4404">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="622ca-4405">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="622ca-4405">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="622ca-4406">overrideObject</span><span class="sxs-lookup"><span data-stu-id="622ca-4406">overrideObject</span></span>  

### <a name="method-onmodified"></a><span data-ttu-id="622ca-4407">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="622ca-4407">Method OnModified</span></span>

    private void OnModified([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-4408">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4408">Parameters</span></span>

<span data-ttu-id="622ca-4409">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-4409">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-4410">e</span><span class="sxs-lookup"><span data-stu-id="622ca-4410">e</span></span>  

### <a name="method-setfocus"></a><span data-ttu-id="622ca-4411">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-4411">Method setFocus</span></span>

<span data-ttu-id="622ca-4412">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4412">Sets the focus on the control.</span></span>

    public void setFocus()

### <a name="method-undo"></a><span data-ttu-id="622ca-4413">メソッド undo</span><span class="sxs-lookup"><span data-stu-id="622ca-4413">Method undo</span></span>

    public void undo()

### <a name="method-performdblookup"></a><span data-ttu-id="622ca-4414">メソッド performDBLookup</span><span class="sxs-lookup"><span data-stu-id="622ca-4414">Method performDBLookup</span></span>

    public void performDBLookup([FieldId fieldId], [TableId tableId], [SelectableDataArea company])

#### <a name="parameters"></a><span data-ttu-id="622ca-4415">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4415">Parameters</span></span>

<span data-ttu-id="622ca-4416">fieldId</span><span class="sxs-lookup"><span data-stu-id="622ca-4416">fieldId</span></span>  

<!-- -->

<span data-ttu-id="622ca-4417">tableId</span><span class="sxs-lookup"><span data-stu-id="622ca-4417">tableId</span></span>  

<!-- -->

<span data-ttu-id="622ca-4418">会社</span><span class="sxs-lookup"><span data-stu-id="622ca-4418">company</span></span>  

### <a name="method-inputsearch"></a><span data-ttu-id="622ca-4419">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="622ca-4419">Method inputSearch</span></span>

<span data-ttu-id="622ca-4420">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4420">Performs data filtering for the control, based on the specified string.</span></span>

    public void inputSearch(str searchStr)

#### <a name="parameters"></a><span data-ttu-id="622ca-4421">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4421">Parameters</span></span>

<span data-ttu-id="622ca-4422">searchStr</span><span class="sxs-lookup"><span data-stu-id="622ca-4422">searchStr</span></span>  
<span data-ttu-id="622ca-4423">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="622ca-4423">The string value to use to filter data; optional.</span></span>

### <a name="method-context"></a><span data-ttu-id="622ca-4424">メソッド context</span><span class="sxs-lookup"><span data-stu-id="622ca-4424">Method context</span></span>

<span data-ttu-id="622ca-4425">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4425">Shows the shortcut menu for the control.</span></span>

    public void context()

### <a name="method-textchange"></a><span data-ttu-id="622ca-4426">メソッド textChange</span><span class="sxs-lookup"><span data-stu-id="622ca-4426">Method textChange</span></span>

    public void textChange()

### <a name="method-ongotfocus"></a><span data-ttu-id="622ca-4427">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-4427">Method OnGotFocus</span></span>

    private void OnGotFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-4428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4428">Parameters</span></span>

<span data-ttu-id="622ca-4429">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-4429">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-4430">e</span><span class="sxs-lookup"><span data-stu-id="622ca-4430">e</span></span>  

### <a name="method-drop"></a><span data-ttu-id="622ca-4431">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="622ca-4431">Method drop</span></span>

<span data-ttu-id="622ca-4432">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4432">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

    public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-4433">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4433">Parameters</span></span>

<span data-ttu-id="622ca-4434">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-4434">dragSource</span></span>  
<span data-ttu-id="622ca-4435">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4435">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-4436">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-4436">dragMode</span></span>  
<span data-ttu-id="622ca-4437">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4437">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-4438">x</span><span class="sxs-lookup"><span data-stu-id="622ca-4438">x</span></span>  
<span data-ttu-id="622ca-4439">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4439">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-4440">y</span><span class="sxs-lookup"><span data-stu-id="622ca-4440">y</span></span>  
<span data-ttu-id="622ca-4441">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4441">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-gotfocus"></a><span data-ttu-id="622ca-4442">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-4442">Method gotFocus</span></span>

<span data-ttu-id="622ca-4443">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4443">Indicates that the control has received focus.</span></span>

    public void gotFocus()

### <a name="method-scrollcursor"></a><span data-ttu-id="622ca-4444">メソッド scrollCursor</span><span class="sxs-lookup"><span data-stu-id="622ca-4444">Method scrollCursor</span></span>

    public void scrollCursor()

### <a name="method-linescroll"></a><span data-ttu-id="622ca-4445">メソッド lineScroll</span><span class="sxs-lookup"><span data-stu-id="622ca-4445">Method lineScroll</span></span>

    public void lineScroll(int dx, int dy)

#### <a name="parameters"></a><span data-ttu-id="622ca-4446">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4446">Parameters</span></span>

<span data-ttu-id="622ca-4447">dx</span><span class="sxs-lookup"><span data-stu-id="622ca-4447">dx</span></span>  

<!-- -->

<span data-ttu-id="622ca-4448">dy</span><span class="sxs-lookup"><span data-stu-id="622ca-4448">dy</span></span>  

### <a name="method-paste"></a><span data-ttu-id="622ca-4449">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="622ca-4449">Method paste</span></span>

<span data-ttu-id="622ca-4450">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4450">Pastes the contents of the clipboard into the control.</span></span>

    public void paste()

### <a name="method-onvalidating"></a><span data-ttu-id="622ca-4451">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="622ca-4451">Method OnValidating</span></span>

    private void OnValidating([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-4452">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4452">Parameters</span></span>

<span data-ttu-id="622ca-4453">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-4453">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-4454">e</span><span class="sxs-lookup"><span data-stu-id="622ca-4454">e</span></span>  

### <a name="method-onenter"></a><span data-ttu-id="622ca-4455">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="622ca-4455">Method OnEnter</span></span>

    private void OnEnter([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-4456">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4456">Parameters</span></span>

<span data-ttu-id="622ca-4457">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-4457">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-4458">e</span><span class="sxs-lookup"><span data-stu-id="622ca-4458">e</span></span>  

### <a name="method-performformlookup"></a><span data-ttu-id="622ca-4459">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="622ca-4459">Method performFormLookup</span></span>

    public void performFormLookup(xFormRun form)

#### <a name="parameters"></a><span data-ttu-id="622ca-4460">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4460">Parameters</span></span>

<span data-ttu-id="622ca-4461">フォーム</span><span class="sxs-lookup"><span data-stu-id="622ca-4461">form</span></span>  

### <a name="method-lostfocus"></a><span data-ttu-id="622ca-4462">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-4462">Method lostFocus</span></span>

<span data-ttu-id="622ca-4463">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4463">Indicates that the control has lost focus.</span></span>

    public void lostFocus()

### <a name="method-enddrag"></a><span data-ttu-id="622ca-4464">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="622ca-4464">Method endDrag</span></span>

<span data-ttu-id="622ca-4465">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4465">Is called when the user has finished dragging a form control.</span></span>

    public void endDrag()

#### <a name="remarks"></a><span data-ttu-id="622ca-4466">備考</span><span class="sxs-lookup"><span data-stu-id="622ca-4466">Remarks</span></span>

<span data-ttu-id="622ca-4467">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="622ca-4467">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="622ca-4468">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4468">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="method-onlostfocus"></a><span data-ttu-id="622ca-4469">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="622ca-4469">Method OnLostFocus</span></span>

    private void OnLostFocus([FormControl sender], [FormControlEventArgs e])

#### <a name="parameters"></a><span data-ttu-id="622ca-4470">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4470">Parameters</span></span>

<span data-ttu-id="622ca-4471">sender</span><span class="sxs-lookup"><span data-stu-id="622ca-4471">sender</span></span>  

<!-- -->

<span data-ttu-id="622ca-4472">e</span><span class="sxs-lookup"><span data-stu-id="622ca-4472">e</span></span>  

### <a name="method-setselection"></a><span data-ttu-id="622ca-4473">メソッド setSelection</span><span class="sxs-lookup"><span data-stu-id="622ca-4473">Method setSelection</span></span>

    public void setSelection(int charIndexFrom, int charIndexTo)

#### <a name="parameters"></a><span data-ttu-id="622ca-4474">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4474">Parameters</span></span>

<span data-ttu-id="622ca-4475">charIndexFrom</span><span class="sxs-lookup"><span data-stu-id="622ca-4475">charIndexFrom</span></span>  

<!-- -->

<span data-ttu-id="622ca-4476">charIndexTo</span><span class="sxs-lookup"><span data-stu-id="622ca-4476">charIndexTo</span></span>  

### <a name="method-copy"></a><span data-ttu-id="622ca-4477">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="622ca-4477">Method copy</span></span>

<span data-ttu-id="622ca-4478">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="622ca-4478">Copies the contents of the control to the clipboard.</span></span>

    public void copy()

### <a name="method-jumpref"></a><span data-ttu-id="622ca-4479">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="622ca-4479">Method jumpRef</span></span>

    public void jumpRef()

### <a name="method-cut"></a><span data-ttu-id="622ca-4480">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="622ca-4480">Method cut</span></span>

<span data-ttu-id="622ca-4481">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="622ca-4481">Cuts the contents of the control.</span></span>

    public void cut()

### <a name="method-mouseenter"></a><span data-ttu-id="622ca-4482">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="622ca-4482">Method mouseEnter</span></span>

<span data-ttu-id="622ca-4483">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4483">Is called when the user moves the mouse pointer into the control area.</span></span>

    public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)

#### <a name="parameters"></a><span data-ttu-id="622ca-4484">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4484">Parameters</span></span>

<span data-ttu-id="622ca-4485">x</span><span class="sxs-lookup"><span data-stu-id="622ca-4485">x</span></span>  
<span data-ttu-id="622ca-4486">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4486">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4487">y</span><span class="sxs-lookup"><span data-stu-id="622ca-4487">y</span></span>  
<span data-ttu-id="622ca-4488">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4488">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4489">ボタン</span><span class="sxs-lookup"><span data-stu-id="622ca-4489">button</span></span>  
<span data-ttu-id="622ca-4490">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4490">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4491">Ctrl</span><span class="sxs-lookup"><span data-stu-id="622ca-4491">Ctrl</span></span>  
<span data-ttu-id="622ca-4492">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4492">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="622ca-4493">シフト</span><span class="sxs-lookup"><span data-stu-id="622ca-4493">Shift</span></span>  
<span data-ttu-id="622ca-4494">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4494">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="method-prefcolumnsize"></a><span data-ttu-id="622ca-4495">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="622ca-4495">Method prefColumnSize</span></span>

<span data-ttu-id="622ca-4496">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="622ca-4496">Specifies the preferred column width and height for the form control.</span></span>

    public void prefColumnSize(int width, int height)

#### <a name="parameters"></a><span data-ttu-id="622ca-4497">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4497">Parameters</span></span>

<span data-ttu-id="622ca-4498">width</span><span class="sxs-lookup"><span data-stu-id="622ca-4498">width</span></span>  
<span data-ttu-id="622ca-4499">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="622ca-4499">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="622ca-4500">height</span><span class="sxs-lookup"><span data-stu-id="622ca-4500">height</span></span>  
<span data-ttu-id="622ca-4501">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="622ca-4501">The preferred height of the control.</span></span>

### <a name="method-enter"></a><span data-ttu-id="622ca-4502">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="622ca-4502">Method enter</span></span>

    public void enter()

### <a name="method-resetusersetting"></a><span data-ttu-id="622ca-4503">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="622ca-4503">Method resetUserSetting</span></span>

<span data-ttu-id="622ca-4504">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="622ca-4504">Resets the user settings for the control.</span></span>

    public void resetUserSetting()

### <a name="method-dropex"></a><span data-ttu-id="622ca-4505">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="622ca-4505">Method dropEx</span></span>

<span data-ttu-id="622ca-4506">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="622ca-4506">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

    public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-4507">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4507">Parameters</span></span>

<span data-ttu-id="622ca-4508">dragSource</span><span class="sxs-lookup"><span data-stu-id="622ca-4508">dragSource</span></span>  
<span data-ttu-id="622ca-4509">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4509">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-4510">dragMode</span><span class="sxs-lookup"><span data-stu-id="622ca-4510">dragMode</span></span>  
<span data-ttu-id="622ca-4511">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4511">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-4512">x</span><span class="sxs-lookup"><span data-stu-id="622ca-4512">x</span></span>  
<span data-ttu-id="622ca-4513">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4513">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="622ca-4514">y</span><span class="sxs-lookup"><span data-stu-id="622ca-4514">y</span></span>  
<span data-ttu-id="622ca-4515">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="622ca-4515">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="method-setcursorpos"></a><span data-ttu-id="622ca-4516">メソッド setCursorPos</span><span class="sxs-lookup"><span data-stu-id="622ca-4516">Method setCursorPos</span></span>

    public void setCursorPos(int x, int y)

#### <a name="parameters"></a><span data-ttu-id="622ca-4517">パラメーター</span><span class="sxs-lookup"><span data-stu-id="622ca-4517">Parameters</span></span>

<span data-ttu-id="622ca-4518">x</span><span class="sxs-lookup"><span data-stu-id="622ca-4518">x</span></span>  

<!-- -->

<span data-ttu-id="622ca-4519">y</span><span class="sxs-lookup"><span data-stu-id="622ca-4519">y</span></span>  





