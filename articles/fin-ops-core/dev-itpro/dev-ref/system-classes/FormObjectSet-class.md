---
title: FormObjectSet クラス
description: このトピックでは、FormObjectSet クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53f2d72d571a27176c02b2cd365ad6222104cb32
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502926"
---
# <a name="class-formobjectset"></a><span data-ttu-id="28cae-103">クラス FormObjectSet</span><span class="sxs-lookup"><span data-stu-id="28cae-103">Class FormObjectSet</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormObjectSet extends Object
```

<span data-ttu-id="28cae-104">FormObjectSet クラスは、フォームのデータ ソースを操作するための基本機能を提供する基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="28cae-104">The FormObjectSet class is a base class that provides basic functionality for working with the data sources for a form.</span></span>

## <a name="remarks"></a><span data-ttu-id="28cae-105">備考</span><span class="sxs-lookup"><span data-stu-id="28cae-105">Remarks</span></span>

<span data-ttu-id="28cae-106">FormObjectSet クラスのメソッドのほとんどは空です。</span><span class="sxs-lookup"><span data-stu-id="28cae-106">Most of the methods on the FormObjectSet class are empty.</span></span> <span data-ttu-id="28cae-107">これらは、FormDataSource 派生クラスで実装されています。</span><span class="sxs-lookup"><span data-stu-id="28cae-107">They are implemented in the FormDataSource derived class.</span></span>

## <a name="examples"></a><span data-ttu-id="28cae-108">例</span><span class="sxs-lookup"><span data-stu-id="28cae-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="28cae-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="28cae-109">Methods</span></span>

| <span data-ttu-id="28cae-110">方法</span><span class="sxs-lookup"><span data-stu-id="28cae-110">Method</span></span>                                                             | <span data-ttu-id="28cae-111">説明</span><span class="sxs-lookup"><span data-stu-id="28cae-111">Description</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28cae-112">public int active()</span><span class="sxs-lookup"><span data-stu-id="28cae-112">public int active()</span></span>                                                | <span data-ttu-id="28cae-113">FormObjectSet クラスでの機能はありませんが、ユーザーが新しいレコードに移動するときに、結合されたデータ ソースからデータを取得する FormDataSource.active メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-113">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.active method, which retrieves data from joined data sources when a user navigates to a new record.</span></span>                                 |
| <span data-ttu-id="28cae-114">public Common cursor()</span><span class="sxs-lookup"><span data-stu-id="28cae-114">public Common cursor()</span></span>                                             | <span data-ttu-id="28cae-115">FormObjectSet クラスでの機能はありませんが、データソースによって参照されるテーブル内の現在アクティブなレコードを返す FormDataSource.cursor メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-115">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.cursor method, which returns the currently active record in the table that is referenced by the data source.</span></span>                        |
| <span data-ttu-id="28cae-116">public boolean findRecord(Common record)</span><span class="sxs-lookup"><span data-stu-id="28cae-116">public boolean findRecord(Common record)</span></span>                           | <span data-ttu-id="28cae-117">FormObjectSet クラスでの機能はありませんが、現在データソースで指定されるレコードを検索して現在のレコードにする FormDataSource.findRecord メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-117">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.findRecord method, which finds a specified record in the data source and makes it the current one.</span></span>                                  |
| <span data-ttu-id="28cae-118">public boolean positionToRecord(Common record)</span><span class="sxs-lookup"><span data-stu-id="28cae-118">public boolean positionToRecord(Common record)</span></span>                     |                                                                                                                                                                                                                             |
| <span data-ttu-id="28cae-119">public int first()</span><span class="sxs-lookup"><span data-stu-id="28cae-119">public int first()</span></span>                                                 | <span data-ttu-id="28cae-120">データ ソースの最初のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="28cae-120">Moves focus to the first record in a data source.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="28cae-121">public xFormRun formRun()</span><span class="sxs-lookup"><span data-stu-id="28cae-121">public xFormRun formRun()</span></span>                                          |                                                                                                                                                                                                                             |
| <span data-ttu-id="28cae-122">public int getPosition()</span><span class="sxs-lookup"><span data-stu-id="28cae-122">public int getPosition()</span></span>                                           |                                                                                                                                                                                                                             |
| <span data-ttu-id="28cae-123">public int id()</span><span class="sxs-lookup"><span data-stu-id="28cae-123">public int id()</span></span>                                                    |                                                                                                                                                                                                                             |
| <span data-ttu-id="28cae-124">public int last()</span><span class="sxs-lookup"><span data-stu-id="28cae-124">public int last()</span></span>                                                  | <span data-ttu-id="28cae-125">データ ソースの最後のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="28cae-125">Moves focus to the last record in the data source.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="28cae-126">public boolean leaveRecord(\[boolean forceUpdate\])</span><span class="sxs-lookup"><span data-stu-id="28cae-126">public boolean leaveRecord(\[boolean forceUpdate\])</span></span>                | <span data-ttu-id="28cae-127">FormObjectSet クラスでの機能はありませんが、ユーザーが別のレコードに移動するときに通知を提供する FormDataSource.leaveRecord メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-127">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.leaveRecord method, which provides a notification when the user moves to another record.</span></span>                                            |
| <span data-ttu-id="28cae-128">public FormObjectSet masterObjectSet()</span><span class="sxs-lookup"><span data-stu-id="28cae-128">public FormObjectSet masterObjectSet()</span></span>                             | <span data-ttu-id="28cae-129">現在のオブジェクト セットのマスター オブジェクト セットを取得します。</span><span class="sxs-lookup"><span data-stu-id="28cae-129">Retrieves the master object set for the current object set.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="28cae-130">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="28cae-130">public str name(\[str value\])</span></span>                                     | <span data-ttu-id="28cae-131">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="28cae-131">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                                                                     |
| <span data-ttu-id="28cae-132">public int next()</span><span class="sxs-lookup"><span data-stu-id="28cae-132">public int next()</span></span>                                                  | <span data-ttu-id="28cae-133">データ ソースの次のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="28cae-133">Moves focus to the next record in the data source.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="28cae-134">public int nextPage(int pageSize)</span><span class="sxs-lookup"><span data-stu-id="28cae-134">public int nextPage(int pageSize)</span></span>                                  | <span data-ttu-id="28cae-135">データ ソースで指定した数のレコード (位置変更) を進めます。</span><span class="sxs-lookup"><span data-stu-id="28cae-135">Moves a specified number of records forward in the data source.</span></span>                                                                                                                                                             |
| <span data-ttu-id="28cae-136">public FormDataObject object(int objectId)</span><span class="sxs-lookup"><span data-stu-id="28cae-136">public FormDataObject object(int objectId)</span></span>                         |                                                                                                                                                                                                                             |
| <span data-ttu-id="28cae-137">public int prev()</span><span class="sxs-lookup"><span data-stu-id="28cae-137">public int prev()</span></span>                                                  | <span data-ttu-id="28cae-138">データ ソースの前のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="28cae-138">Moves focus to the previous record in the data source.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="28cae-139">public int prevPage(int pageSize)</span><span class="sxs-lookup"><span data-stu-id="28cae-139">public int prevPage(int pageSize)</span></span>                                  | <span data-ttu-id="28cae-140">データ ソースで指定した数のレコード (位置変更) を戻します。</span><span class="sxs-lookup"><span data-stu-id="28cae-140">Moves a specified number of records back (a positional change) in the data source.</span></span>                                                                                                                                          |
| <span data-ttu-id="28cae-141">public boolean setPosition(int position)</span><span class="sxs-lookup"><span data-stu-id="28cae-141">public boolean setPosition(int position)</span></span>                           |                                                                                                                                                                                                                             |
| <span data-ttu-id="28cae-142">public boolean validateDelete()</span><span class="sxs-lookup"><span data-stu-id="28cae-142">public boolean validateDelete()</span></span>                                    | <span data-ttu-id="28cae-143">FormObjectSet クラスでの機能はありませんが、データソースからのレコードの削除をユーザーが確認するよう求める FormDataSource.validateDelete メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-143">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.validateDelete method, which prompts the user to confirm the deletion of a record from the data source.</span></span>                             |
| <span data-ttu-id="28cae-144">public boolean validateWrite()</span><span class="sxs-lookup"><span data-stu-id="28cae-144">public boolean validateWrite()</span></span>                                     | <span data-ttu-id="28cae-145">FormObjectSet クラスでの機能はありませんが、データが有効であるかおよび書き込まれる準備ができているかどうかを判断する FormDataSource.validateWrite メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-145">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.validateWrite method, which determines whether data is valid and ready to be written.</span></span>                                               |
| <span data-ttu-id="28cae-146">public void refresh()</span><span class="sxs-lookup"><span data-stu-id="28cae-146">public void refresh()</span></span>                                              | <span data-ttu-id="28cae-147">FormObjectSet クラスでの機能はありませんが、データ ソースにすべてのレコードの表示を更新する FormDataSource.refresh メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-147">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.refresh method, which updates the view of all records in the data source.</span></span>                                                           |
| <span data-ttu-id="28cae-148">public void addNotifyHandler(FormObjectSetNotify notifyHandler)</span><span class="sxs-lookup"><span data-stu-id="28cae-148">public void addNotifyHandler(FormObjectSetNotify notifyHandler)</span></span>    |                                                                                                                                                                                                                             |
| <span data-ttu-id="28cae-149">public void reread()</span><span class="sxs-lookup"><span data-stu-id="28cae-149">public void reread()</span></span>                                               | <span data-ttu-id="28cae-150">FormObjectSet クラスでの機能はありませんが、データベースから現在のレコードを再読み込みする FormDataSource.reread メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-150">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.reread method, which rereads the current record from the database.</span></span>                                                                  |
| <span data-ttu-id="28cae-151">public void init()</span><span class="sxs-lookup"><span data-stu-id="28cae-151">public void init()</span></span>                                                 | <span data-ttu-id="28cae-152">FormObjectSet クラスでの機能はありませんが、データ ソース プロパティに基づいてデータ ソース クエリを作成する FormDataSource.init メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-152">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.init method, which creates a data source query, based on the data source properties.</span></span>                                                |
| <span data-ttu-id="28cae-153">public void deleteMarked()</span><span class="sxs-lookup"><span data-stu-id="28cae-153">public void deleteMarked()</span></span>                                         | <span data-ttu-id="28cae-154">FormObjectSet クラスでの機能はありませんが、データソースからマークされたレコードをすべて削除する FormDataSource.deleteMarked メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-154">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.deleteMarked method, which deletes all marked records from a data source.</span></span>                                                           |
| <span data-ttu-id="28cae-155">public void delete()</span><span class="sxs-lookup"><span data-stu-id="28cae-155">public void delete()</span></span>                                               | <span data-ttu-id="28cae-156">FormObjectSet クラスでの機能はありませんが、現在データソースから選択されるレコードを削除する FormDataSource.delete メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-156">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.delete method, which deletes the record that is currently selected from the data source.</span></span>                                            |
| <span data-ttu-id="28cae-157">public void write()</span><span class="sxs-lookup"><span data-stu-id="28cae-157">public void write()</span></span>                                                | <span data-ttu-id="28cae-158">FormObjectSet クラスでの機能はありませんが、データベースの書き込み操作を管理する FormDataSource.write メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-158">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.write method, which manages the database write operation.</span></span>                                                                           |
| <span data-ttu-id="28cae-159">public void create(\[boolean append\])</span><span class="sxs-lookup"><span data-stu-id="28cae-159">public void create(\[boolean append\])</span></span>                             | <span data-ttu-id="28cae-160">FormObjectSet クラスでの機能はありませんが、データ ソースに新しいレコードを作成する FormDataSource.create メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-160">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.create method, which creates a new record in the data source.</span></span>                                                                       |
| <span data-ttu-id="28cae-161">public void removeNotifyHandler(FormObjectSetNotify notifyHandler)</span><span class="sxs-lookup"><span data-stu-id="28cae-161">public void removeNotifyHandler(FormObjectSetNotify notifyHandler)</span></span> |                                                                                                                                                                                                                             |
| <span data-ttu-id="28cae-162">public void prompt()</span><span class="sxs-lookup"><span data-stu-id="28cae-162">public void prompt()</span></span>                                               | <span data-ttu-id="28cae-163">FormObjectSet クラスでの機能はありませんが、クエリの範囲を制限するために使用される SysQueryForm クラスを有効にするFormDataSource.prompt メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-163">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.prompt method, which activates the SysQueryForm class that is used to limit a query range.</span></span>                                          |
| <span data-ttu-id="28cae-164">public void research(\[boolean retainPosition\])</span><span class="sxs-lookup"><span data-stu-id="28cae-164">public void research(\[boolean retainPosition\])</span></span>                   | <span data-ttu-id="28cae-165">FormObjectSet クラスでの機能はありませんが、現在フォームに適用されているフィルターおよびソートで定義されているデータベースの検索を更新する FormDataSource.research メソッドによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-165">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.research method, which updates the database search that is defined by the filters and sorts that are currently applied to the form.</span></span> |
| <span data-ttu-id="28cae-166">public void refreshEx(\[AnyType pos\])</span><span class="sxs-lookup"><span data-stu-id="28cae-166">public void refreshEx(\[AnyType pos\])</span></span>                             | <span data-ttu-id="28cae-167">FormObjectSet クラスでの機能はありませんが、特定のレコードの表示を更新する FormDataSource.refreshEx メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-167">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.refreshEx method, which updates the view of the specified record.</span></span>                                                                   |
| <span data-ttu-id="28cae-168">public void initValue()</span><span class="sxs-lookup"><span data-stu-id="28cae-168">public void initValue()</span></span>                                            | <span data-ttu-id="28cae-169">FormObjectSet クラスでの機能はありませんが、新しいレコードでフィールド値を初期化する FormDataSource.initValue メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-169">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.initValue method, which initializes field values in a new record.</span></span>                                                                   |
| <span data-ttu-id="28cae-170">public void removeFilter()</span><span class="sxs-lookup"><span data-stu-id="28cae-170">public void removeFilter()</span></span>                                         | <span data-ttu-id="28cae-171">FormObjectSet クラスでの機能はありませんが、データ ソースのクエリをリセットする FormDataSource.removeFilter メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-171">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.removeFilter method, which resets the query for the data source.</span></span>                                                                    |

## <a name="method-active"></a><span data-ttu-id="28cae-172">メソッド active</span><span class="sxs-lookup"><span data-stu-id="28cae-172">Method active</span></span>

<span data-ttu-id="28cae-173">FormObjectSet クラスでの機能はありませんが、ユーザーが新しいレコードに移動するときに、結合されたデータ ソースからデータを取得する FormDataSource.active メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-173">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.active method, which retrieves data from joined data sources when a user navigates to a new record.</span></span>

```xpp
public int active()
```

### <a name="return-value---active"></a><span data-ttu-id="28cae-174">戻り値 - active</span><span class="sxs-lookup"><span data-stu-id="28cae-174">Return Value - active</span></span>

<span data-ttu-id="28cae-175">常に 1 を返します。</span><span class="sxs-lookup"><span data-stu-id="28cae-175">Always returns 1.</span></span>

## <a name="method-cursor"></a><span data-ttu-id="28cae-176">メソッド cursor</span><span class="sxs-lookup"><span data-stu-id="28cae-176">Method cursor</span></span>

<span data-ttu-id="28cae-177">FormObjectSet クラスでの機能はありませんが、データソースによって参照されるテーブル内の現在アクティブなレコードを返す FormDataSource.cursor メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-177">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.cursor method, which returns the currently active record in the table that is referenced by the data source.</span></span>

```xpp
public Common cursor()
```

### <a name="return-value---cursor"></a><span data-ttu-id="28cae-178">戻り値 - cursor</span><span class="sxs-lookup"><span data-stu-id="28cae-178">Return Value - cursor</span></span>

## <a name="method-findrecord"></a><span data-ttu-id="28cae-179">メソッド findRecord</span><span class="sxs-lookup"><span data-stu-id="28cae-179">Method findRecord</span></span>

<span data-ttu-id="28cae-180">FormObjectSet クラスでの機能はありませんが、現在データソースで指定されるレコードを検索して現在のレコードにする FormDataSource.findRecord メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-180">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.findRecord method, which finds a specified record in the data source and makes it the current one.</span></span>

```xpp
public boolean findRecord(Common record)
```

### <a name="parameters---findrecord"></a><span data-ttu-id="28cae-181">パラメーター - findRecord</span><span class="sxs-lookup"><span data-stu-id="28cae-181">Parameters - findRecord</span></span>

<span data-ttu-id="28cae-182">記録</span><span class="sxs-lookup"><span data-stu-id="28cae-182">record</span></span>  
<span data-ttu-id="28cae-183">FormObjectSet 基本クラスで使用されていないパラメーター。</span><span class="sxs-lookup"><span data-stu-id="28cae-183">A parameter that is not used in the FormObjectSet base class.</span></span>

### <a name="return-value---findrecord"></a><span data-ttu-id="28cae-184">戻り値 - findRecord</span><span class="sxs-lookup"><span data-stu-id="28cae-184">Return Value - findRecord</span></span>

<span data-ttu-id="28cae-185">レコードが見つかった場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="28cae-185">true if the record was found; otherwise, false.</span></span>

## <a name="method-positiontorecord"></a><span data-ttu-id="28cae-186">メソッド positionToRecord</span><span class="sxs-lookup"><span data-stu-id="28cae-186">Method positionToRecord</span></span>

```xpp
public boolean positionToRecord(Common record)
```

### <a name="parameters---positiontorecord"></a><span data-ttu-id="28cae-187">パラメーター - positionToRecord</span><span class="sxs-lookup"><span data-stu-id="28cae-187">Parameters - positionToRecord</span></span>

<span data-ttu-id="28cae-188">記録</span><span class="sxs-lookup"><span data-stu-id="28cae-188">record</span></span>  

### <a name="return-value---positiontorecord"></a><span data-ttu-id="28cae-189">戻り値 - positionToRecord</span><span class="sxs-lookup"><span data-stu-id="28cae-189">Return Value - positionToRecord</span></span>

## <a name="method-first"></a><span data-ttu-id="28cae-190">メソッド first</span><span class="sxs-lookup"><span data-stu-id="28cae-190">Method first</span></span>

<span data-ttu-id="28cae-191">データ ソースの最初のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="28cae-191">Moves focus to the first record in a data source.</span></span>

```xpp
public int first()
```

### <a name="return-value---first"></a><span data-ttu-id="28cae-192">戻り値 - first</span><span class="sxs-lookup"><span data-stu-id="28cae-192">Return Value - first</span></span>

<span data-ttu-id="28cae-193">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="28cae-193">A non-zero integer if the operation succeeds.</span></span>

### <a name="remarks---first"></a><span data-ttu-id="28cae-194">備考 - first</span><span class="sxs-lookup"><span data-stu-id="28cae-194">Remarks - first</span></span>

<span data-ttu-id="28cae-195">このメソッドは、ユーザーが CTRL+HOME キーを押してフォームの最初のレコードを選択するときに呼び出されるメソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-195">This method is overridden by the method that is called when a user presses CTRL+HOME to select the first record in a form.</span></span>

## <a name="method-formrun"></a><span data-ttu-id="28cae-196">メソッド formRun</span><span class="sxs-lookup"><span data-stu-id="28cae-196">Method formRun</span></span>

```xpp
public xFormRun formRun()
```

### <a name="return-value---formrun"></a><span data-ttu-id="28cae-197">戻り値 - formRun</span><span class="sxs-lookup"><span data-stu-id="28cae-197">Return Value - formRun</span></span>

## <a name="method-getposition"></a><span data-ttu-id="28cae-198">メソッド getPosition</span><span class="sxs-lookup"><span data-stu-id="28cae-198">Method getPosition</span></span>

```xpp
public int getPosition()
```

### <a name="return-value---getposition"></a><span data-ttu-id="28cae-199">戻り値 - getPosition</span><span class="sxs-lookup"><span data-stu-id="28cae-199">Return Value - getPosition</span></span>

## <a name="method-id"></a><span data-ttu-id="28cae-200">メソッド id</span><span class="sxs-lookup"><span data-stu-id="28cae-200">Method id</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="28cae-201">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="28cae-201">Return Value - id</span></span>

## <a name="method-last"></a><span data-ttu-id="28cae-202">メソッド last</span><span class="sxs-lookup"><span data-stu-id="28cae-202">Method last</span></span>

<span data-ttu-id="28cae-203">データ ソースの最後のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="28cae-203">Moves focus to the last record in the data source.</span></span>

```xpp
public int last()
```

### <a name="return-value---last"></a><span data-ttu-id="28cae-204">戻り値 - last</span><span class="sxs-lookup"><span data-stu-id="28cae-204">Return Value - last</span></span>

<span data-ttu-id="28cae-205">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="28cae-205">A non-zero integer if the operation succeeds.</span></span>

### <a name="remarks---last"></a><span data-ttu-id="28cae-206">備考 - last</span><span class="sxs-lookup"><span data-stu-id="28cae-206">Remarks - last</span></span>

<span data-ttu-id="28cae-207">このメソッドは、ユーザーが CTRL+END キーを押してフォームの最後のレコードを選択するときに呼び出されるメソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-207">This method is overridden by the method that is called when a user presses CTRL+END to select the last record in a form.</span></span>

## <a name="method-leaverecord"></a><span data-ttu-id="28cae-208">メソッド leaveRecord</span><span class="sxs-lookup"><span data-stu-id="28cae-208">Method leaveRecord</span></span>

<span data-ttu-id="28cae-209">FormObjectSet クラスでの機能はありませんが、ユーザーが別のレコードに移動するときに通知を提供する FormDataSource.leaveRecord メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-209">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.leaveRecord method, which provides a notification when the user moves to another record.</span></span>

```xpp
public boolean leaveRecord([boolean forceUpdate])
```

### <a name="parameters---leaverecord"></a><span data-ttu-id="28cae-210">パラメーター - leaveRecord</span><span class="sxs-lookup"><span data-stu-id="28cae-210">Parameters - leaveRecord</span></span>

<span data-ttu-id="28cae-211">forceUpdate</span><span class="sxs-lookup"><span data-stu-id="28cae-211">forceUpdate</span></span>  

### <a name="return-value---leaverecord"></a><span data-ttu-id="28cae-212">戻り値 - leaveRecord</span><span class="sxs-lookup"><span data-stu-id="28cae-212">Return Value - leaveRecord</span></span>

## <a name="method-masterobjectset"></a><span data-ttu-id="28cae-213">メソッド masterObjectSet</span><span class="sxs-lookup"><span data-stu-id="28cae-213">Method masterObjectSet</span></span>

<span data-ttu-id="28cae-214">現在のオブジェクト セットのマスター オブジェクト セットを取得します。</span><span class="sxs-lookup"><span data-stu-id="28cae-214">Retrieves the master object set for the current object set.</span></span>

```xpp
public FormObjectSet masterObjectSet()
```

### <a name="return-value---masterobjectset"></a><span data-ttu-id="28cae-215">戻り値 - masterObjectSet</span><span class="sxs-lookup"><span data-stu-id="28cae-215">Return Value - masterObjectSet</span></span>

<span data-ttu-id="28cae-216">マスター オブジェクト セット。</span><span class="sxs-lookup"><span data-stu-id="28cae-216">The master object set.</span></span>

### <a name="remarks---masterobjectset"></a><span data-ttu-id="28cae-217">備考 - masterObjectSet</span><span class="sxs-lookup"><span data-stu-id="28cae-217">Remarks - masterObjectSet</span></span>

<span data-ttu-id="28cae-218">フォームには、多くの場合、1 つ以上のオブジェクトのセット (データ ソース) があります。</span><span class="sxs-lookup"><span data-stu-id="28cae-218">A form often has more than one object set (data source).</span></span> <span data-ttu-id="28cae-219">これらは、ツリー階層を使用して結合されます。ここでは、1 つのデータ ソースがマスターまたは親データソースです。</span><span class="sxs-lookup"><span data-stu-id="28cae-219">These are joined together by using a tree hierarchy, where one data source is the master or parent data source.</span></span> <span data-ttu-id="28cae-220">masterObjectSet メソッドは、特定のデータソースのマスター データソースの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="28cae-220">The masterObjectSet method returns the ID of the master data source for a specific data source.</span></span>

### <a name="examples---masterobjectset"></a><span data-ttu-id="28cae-221">例 - masterObjectSet</span><span class="sxs-lookup"><span data-stu-id="28cae-221">Examples - masterObjectSet</span></span>

<span data-ttu-id="28cae-222">次の例は、FormRun オブジェクトのマスター データ ソースの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="28cae-222">The following example returns the name of the master data source for a FormRun object.</span></span>

```xpp
private static client Name formDataSourceName(FormRun _formRun) 
{ 
    return _formRun.objectSet().masterObjectSet().name(); 
}
```

## <a name="method-name"></a><span data-ttu-id="28cae-223">メソッド名</span><span class="sxs-lookup"><span data-stu-id="28cae-223">Method name</span></span>

<span data-ttu-id="28cae-224">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="28cae-224">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="28cae-225">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="28cae-225">Parameters - name</span></span>

<span data-ttu-id="28cae-226">値</span><span class="sxs-lookup"><span data-stu-id="28cae-226">value</span></span>  
<span data-ttu-id="28cae-227">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="28cae-227">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="28cae-228">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="28cae-228">Return Value - name</span></span>

<span data-ttu-id="28cae-229">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="28cae-229">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="28cae-230">備考 - name</span><span class="sxs-lookup"><span data-stu-id="28cae-230">Remarks - name</span></span>

<span data-ttu-id="28cae-231">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="28cae-231">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="28cae-232">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="28cae-232">It must start with a letter.</span></span>
-   <span data-ttu-id="28cae-233">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="28cae-233">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="28cae-234">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="28cae-234">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="28cae-235">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="28cae-235">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="28cae-236">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="28cae-236">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-next"></a><span data-ttu-id="28cae-237">メソッド next</span><span class="sxs-lookup"><span data-stu-id="28cae-237">Method next</span></span>

<span data-ttu-id="28cae-238">データ ソースの次のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="28cae-238">Moves focus to the next record in the data source.</span></span>

```xpp
public int next()
```

### <a name="return-value---next"></a><span data-ttu-id="28cae-239">戻り値 - next</span><span class="sxs-lookup"><span data-stu-id="28cae-239">Return Value - next</span></span>

<span data-ttu-id="28cae-240">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="28cae-240">A non-zero integer if the operation succeeds.</span></span>

### <a name="remarks---next"></a><span data-ttu-id="28cae-241">備考 - next</span><span class="sxs-lookup"><span data-stu-id="28cae-241">Remarks - next</span></span>

<span data-ttu-id="28cae-242">このメソッドは、ユーザーが DOWN ARROW キーを押してフォームの次のレコードを選択するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28cae-242">This method is called when a user selects the next record in a form by pressing the DOWN ARROW key.</span></span>

## <a name="method-nextpage"></a><span data-ttu-id="28cae-243">メソッド nextPage</span><span class="sxs-lookup"><span data-stu-id="28cae-243">Method nextPage</span></span>

<span data-ttu-id="28cae-244">データ ソースで指定した数のレコード (位置変更) を進めます。</span><span class="sxs-lookup"><span data-stu-id="28cae-244">Moves a specified number of records forward in the data source.</span></span>

```xpp
public int nextPage(int pageSize)
```

### <a name="parameters---nextpage"></a><span data-ttu-id="28cae-245">パラメーター - nextPage</span><span class="sxs-lookup"><span data-stu-id="28cae-245">Parameters - nextPage</span></span>

<span data-ttu-id="28cae-246">pageSize</span><span class="sxs-lookup"><span data-stu-id="28cae-246">pageSize</span></span>  
<span data-ttu-id="28cae-247">スキップするレコードの数。</span><span class="sxs-lookup"><span data-stu-id="28cae-247">The number of records to skip.</span></span>

### <a name="return-value---nextpage"></a><span data-ttu-id="28cae-248">戻り値 - nextPage</span><span class="sxs-lookup"><span data-stu-id="28cae-248">Return Value - nextPage</span></span>

<span data-ttu-id="28cae-249">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="28cae-249">A non-zero integer if the operation succeeds.</span></span>

### <a name="remarks---nextpage"></a><span data-ttu-id="28cae-250">備考 - nextPage</span><span class="sxs-lookup"><span data-stu-id="28cae-250">Remarks - nextPage</span></span>

<span data-ttu-id="28cae-251">このメソッドは、ユーザーがフォーム内にあるときに PAGE DOWN キーを押すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28cae-251">This method is called when a user presses the PAGE DOWN key while he or she is in a form.</span></span> <span data-ttu-id="28cae-252">これにより、ページ サイズは自動的に計算されて、pageSize パラメーターに使用されます。</span><span class="sxs-lookup"><span data-stu-id="28cae-252">The page size is then automatically calculated and used for the pageSize parameter.</span></span> <span data-ttu-id="28cae-253">このメソッドは、FormDataSource クラスで上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-253">This method is overridden on the FormDataSource class.</span></span>

## <a name="method-object"></a><span data-ttu-id="28cae-254">メソッド object</span><span class="sxs-lookup"><span data-stu-id="28cae-254">Method object</span></span>

```xpp
public FormDataObject object(int objectId)
```

### <a name="parameters---object"></a><span data-ttu-id="28cae-255">パラメーター - object</span><span class="sxs-lookup"><span data-stu-id="28cae-255">Parameters - object</span></span>

<span data-ttu-id="28cae-256">objectId</span><span class="sxs-lookup"><span data-stu-id="28cae-256">objectId</span></span>  

### <a name="return-value---object"></a><span data-ttu-id="28cae-257">戻り値 - object</span><span class="sxs-lookup"><span data-stu-id="28cae-257">Return Value - object</span></span>

## <a name="method-prev"></a><span data-ttu-id="28cae-258">メソッド prev</span><span class="sxs-lookup"><span data-stu-id="28cae-258">Method prev</span></span>

<span data-ttu-id="28cae-259">データ ソースの前のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="28cae-259">Moves focus to the previous record in the data source.</span></span>

```xpp
public int prev()
```

### <a name="return-value---prev"></a><span data-ttu-id="28cae-260">戻り値 - prev</span><span class="sxs-lookup"><span data-stu-id="28cae-260">Return Value - prev</span></span>

<span data-ttu-id="28cae-261">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="28cae-261">A non-zero integer if the operation succeeds.</span></span>

### <a name="remarks---prev"></a><span data-ttu-id="28cae-262">備考 - prev</span><span class="sxs-lookup"><span data-stu-id="28cae-262">Remarks - prev</span></span>

<span data-ttu-id="28cae-263">このメソッドは、ユーザーがフォーム内の前のレコードを選択したときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28cae-263">This method is called when a user selects the previous record in the form.</span></span>

## <a name="method-prevpage"></a><span data-ttu-id="28cae-264">メソッド prevPage</span><span class="sxs-lookup"><span data-stu-id="28cae-264">Method prevPage</span></span>

<span data-ttu-id="28cae-265">データ ソースで指定した数のレコード (位置変更) を戻します。</span><span class="sxs-lookup"><span data-stu-id="28cae-265">Moves a specified number of records back (a positional change) in the data source.</span></span>

```xpp
public int prevPage(int pageSize)
```

### <a name="parameters---prevpage"></a><span data-ttu-id="28cae-266">パラメーター - prevPage</span><span class="sxs-lookup"><span data-stu-id="28cae-266">Parameters - prevPage</span></span>

<span data-ttu-id="28cae-267">pageSize</span><span class="sxs-lookup"><span data-stu-id="28cae-267">pageSize</span></span>  
<span data-ttu-id="28cae-268">戻すレコードの数 (位置の変更)。</span><span class="sxs-lookup"><span data-stu-id="28cae-268">The number of records to move back (a positional change).</span></span>

### <a name="return-value---prevpage"></a><span data-ttu-id="28cae-269">戻り値 - prevPage</span><span class="sxs-lookup"><span data-stu-id="28cae-269">Return Value - prevPage</span></span>

<span data-ttu-id="28cae-270">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="28cae-270">A non-zero integer if the operation succeeds.</span></span>

### <a name="remarks---prevpage"></a><span data-ttu-id="28cae-271">備考 - prevPage</span><span class="sxs-lookup"><span data-stu-id="28cae-271">Remarks - prevPage</span></span>

<span data-ttu-id="28cae-272">このメソッドは、ユーザーがフォーム内にあるときに PAGE UP キーを押すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="28cae-272">This method is called when a user presses the PAGE UP key while he or she is in a form.</span></span> <span data-ttu-id="28cae-273">これにより、ページ サイズは自動的に計算されて、pageSize パラメーターに使用されます。</span><span class="sxs-lookup"><span data-stu-id="28cae-273">The page size is then calculated automatically and used for the pageSize parameter.</span></span>

## <a name="method-setposition"></a><span data-ttu-id="28cae-274">メソッド setPosition</span><span class="sxs-lookup"><span data-stu-id="28cae-274">Method setPosition</span></span>

```xpp
public boolean setPosition(int position)
```

### <a name="parameters---setposition"></a><span data-ttu-id="28cae-275">パラメーター - setPosition</span><span class="sxs-lookup"><span data-stu-id="28cae-275">Parameters - setPosition</span></span>

<span data-ttu-id="28cae-276">職位</span><span class="sxs-lookup"><span data-stu-id="28cae-276">position</span></span>  

### <a name="return-value---setposition"></a><span data-ttu-id="28cae-277">戻り値 - setPosition</span><span class="sxs-lookup"><span data-stu-id="28cae-277">Return Value - setPosition</span></span>

## <a name="method-validatedelete"></a><span data-ttu-id="28cae-278">メソッド validateDelete</span><span class="sxs-lookup"><span data-stu-id="28cae-278">Method validateDelete</span></span>

<span data-ttu-id="28cae-279">FormObjectSet クラスでの機能はありませんが、データソースからのレコードの削除をユーザーが確認するよう求める FormDataSource.validateDelete メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-279">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.validateDelete method, which prompts the user to confirm the deletion of a record from the data source.</span></span>

```xpp
public boolean validateDelete()
```

### <a name="return-value---validatedelete"></a><span data-ttu-id="28cae-280">戻り値 - validateDelete</span><span class="sxs-lookup"><span data-stu-id="28cae-280">Return Value - validateDelete</span></span>

## <a name="method-validatewrite"></a><span data-ttu-id="28cae-281">メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="28cae-281">Method validateWrite</span></span>

<span data-ttu-id="28cae-282">FormObjectSet クラスでの機能はありませんが、データが有効であるかおよび書き込まれる準備ができているかどうかを判断する FormDataSource.validateWrite メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-282">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.validateWrite method, which determines whether data is valid and ready to be written.</span></span>

```xpp
public boolean validateWrite()
```

### <a name="return-value---validatewrite"></a><span data-ttu-id="28cae-283">戻り値 - validateWrite</span><span class="sxs-lookup"><span data-stu-id="28cae-283">Return Value - validateWrite</span></span>

## <a name="method-refresh"></a><span data-ttu-id="28cae-284">メソッド refresh</span><span class="sxs-lookup"><span data-stu-id="28cae-284">Method refresh</span></span>

<span data-ttu-id="28cae-285">FormObjectSet クラスでの機能はありませんが、データ ソースにすべてのレコードの表示を更新する FormDataSource.refresh メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-285">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.refresh method, which updates the view of all records in the data source.</span></span>

```xpp
public void refresh()
```

## <a name="method-addnotifyhandler"></a><span data-ttu-id="28cae-286">メソッド addNotifyHandler</span><span class="sxs-lookup"><span data-stu-id="28cae-286">Method addNotifyHandler</span></span>

```xpp
public void addNotifyHandler(FormObjectSetNotify notifyHandler)
```

### <a name="parameters---addnotifyhandler"></a><span data-ttu-id="28cae-287">パラメーター - addNotifyHandler</span><span class="sxs-lookup"><span data-stu-id="28cae-287">Parameters - addNotifyHandler</span></span>

<span data-ttu-id="28cae-288">notifyHandler</span><span class="sxs-lookup"><span data-stu-id="28cae-288">notifyHandler</span></span>  

## <a name="method-reread"></a><span data-ttu-id="28cae-289">メソッド reread</span><span class="sxs-lookup"><span data-stu-id="28cae-289">Method reread</span></span>

<span data-ttu-id="28cae-290">FormObjectSet クラスでの機能はありませんが、データベースから現在のレコードを再読み込みする FormDataSource.reread メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-290">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.reread method, which rereads the current record from the database.</span></span>

```xpp
public void reread()
```

## <a name="method-init"></a><span data-ttu-id="28cae-291">メソッド init</span><span class="sxs-lookup"><span data-stu-id="28cae-291">Method init</span></span>

<span data-ttu-id="28cae-292">FormObjectSet クラスでの機能はありませんが、データ ソース プロパティに基づいてデータ ソース クエリを作成する FormDataSource.init メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-292">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.init method, which creates a data source query, based on the data source properties.</span></span>

```xpp
public void init()
```

## <a name="method-deletemarked"></a><span data-ttu-id="28cae-293">メソッド deleteMarked</span><span class="sxs-lookup"><span data-stu-id="28cae-293">Method deleteMarked</span></span>

<span data-ttu-id="28cae-294">FormObjectSet クラスでの機能はありませんが、データソースからマークされたレコードをすべて削除する FormDataSource.deleteMarked メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-294">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.deleteMarked method, which deletes all marked records from a data source.</span></span>

```xpp
public void deleteMarked()
```

## <a name="method-delete"></a><span data-ttu-id="28cae-295">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="28cae-295">Method delete</span></span>

<span data-ttu-id="28cae-296">FormObjectSet クラスでの機能はありませんが、現在データソースから選択されるレコードを削除する FormDataSource.delete メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-296">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.delete method, which deletes the record that is currently selected from the data source.</span></span>

```xpp
public void delete()
```

## <a name="method-write"></a><span data-ttu-id="28cae-297">メソッド write</span><span class="sxs-lookup"><span data-stu-id="28cae-297">Method write</span></span>

<span data-ttu-id="28cae-298">FormObjectSet クラスでの機能はありませんが、データベースの書き込み操作を管理する FormDataSource.write メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-298">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.write method, which manages the database write operation.</span></span>

```xpp
public void write()
```

## <a name="method-create"></a><span data-ttu-id="28cae-299">メソッド create</span><span class="sxs-lookup"><span data-stu-id="28cae-299">Method create</span></span>

<span data-ttu-id="28cae-300">FormObjectSet クラスでの機能はありませんが、データ ソースに新しいレコードを作成する FormDataSource.create メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-300">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.create method, which creates a new record in the data source.</span></span>

```xpp
public void create([boolean append])
```

### <a name="parameters---create"></a><span data-ttu-id="28cae-301">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="28cae-301">Parameters - create</span></span>

<span data-ttu-id="28cae-302">append</span><span class="sxs-lookup"><span data-stu-id="28cae-302">append</span></span>  
<span data-ttu-id="28cae-303">現在のカーソル位置の前後にレコードを挿入するかどうかを示すブール値フラグ。</span><span class="sxs-lookup"><span data-stu-id="28cae-303">A Boolean flag that indicates whether to insert the record after or before the current cursor position; optional.</span></span> <span data-ttu-id="28cae-304">値が true に設定されている場合、現在のレコードの後に新しいレコードが挿入されます。</span><span class="sxs-lookup"><span data-stu-id="28cae-304">If the value is true, the new record is inserted after the current one.</span></span>

## <a name="method-removenotifyhandler"></a><span data-ttu-id="28cae-305">メソッド removeNotifyHandler</span><span class="sxs-lookup"><span data-stu-id="28cae-305">Method removeNotifyHandler</span></span>

```xpp
public void removeNotifyHandler(FormObjectSetNotify notifyHandler)
```

### <a name="parameters---removenotifyhandler"></a><span data-ttu-id="28cae-306">パラメーター - removeNotifyHandler</span><span class="sxs-lookup"><span data-stu-id="28cae-306">Parameters - removeNotifyHandler</span></span>

<span data-ttu-id="28cae-307">notifyHandler</span><span class="sxs-lookup"><span data-stu-id="28cae-307">notifyHandler</span></span>  

## <a name="method-prompt"></a><span data-ttu-id="28cae-308">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="28cae-308">Method prompt</span></span>

<span data-ttu-id="28cae-309">FormObjectSet クラスでの機能はありませんが、クエリの範囲を制限するために使用される SysQueryForm クラスを有効にするFormDataSource.prompt メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-309">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.prompt method, which activates the SysQueryForm class that is used to limit a query range.</span></span>

```xpp
public void prompt()
```

## <a name="method-research"></a><span data-ttu-id="28cae-310">メソッド research</span><span class="sxs-lookup"><span data-stu-id="28cae-310">Method research</span></span>

<span data-ttu-id="28cae-311">FormObjectSet クラスでの機能はありませんが、現在フォームに適用されているフィルターおよびソートで定義されているデータベースの検索を更新する FormDataSource.research メソッドによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-311">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.research method, which updates the database search that is defined by the filters and sorts that are currently applied to the form.</span></span>

```xpp
public void research([boolean retainPosition])
```

### <a name="parameters---research"></a><span data-ttu-id="28cae-312">パラメーター - research</span><span class="sxs-lookup"><span data-stu-id="28cae-312">Parameters - research</span></span>

<span data-ttu-id="28cae-313">retainPosition</span><span class="sxs-lookup"><span data-stu-id="28cae-313">retainPosition</span></span>  

## <a name="method-refreshex"></a><span data-ttu-id="28cae-314">メソッド refreshEx</span><span class="sxs-lookup"><span data-stu-id="28cae-314">Method refreshEx</span></span>

<span data-ttu-id="28cae-315">FormObjectSet クラスでの機能はありませんが、特定のレコードの表示を更新する FormDataSource.refreshEx メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-315">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.refreshEx method, which updates the view of the specified record.</span></span>

```xpp
public void refreshEx([AnyType pos])
```

### <a name="parameters---refreshex"></a><span data-ttu-id="28cae-316">パラメーター - refreshEx</span><span class="sxs-lookup"><span data-stu-id="28cae-316">Parameters - refreshEx</span></span>

<span data-ttu-id="28cae-317">pos</span><span class="sxs-lookup"><span data-stu-id="28cae-317">pos</span></span>  
<span data-ttu-id="28cae-318">FormObjectSet.refreshEx メソッドで使用されていないパラメーター (オプション)。</span><span class="sxs-lookup"><span data-stu-id="28cae-318">A parameter that is not used in the FormObjectSet.refreshEx method; optional.</span></span>

## <a name="method-initvalue"></a><span data-ttu-id="28cae-319">メソッド initValue</span><span class="sxs-lookup"><span data-stu-id="28cae-319">Method initValue</span></span>

<span data-ttu-id="28cae-320">FormObjectSet クラスでの機能はありませんが、新しいレコードでフィールド値を初期化する FormDataSource.initValue メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-320">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.initValue method, which initializes field values in a new record.</span></span>

```xpp
public void initValue()
```

## <a name="method-removefilter"></a><span data-ttu-id="28cae-321">メソッド removeFilter</span><span class="sxs-lookup"><span data-stu-id="28cae-321">Method removeFilter</span></span>

<span data-ttu-id="28cae-322">FormObjectSet クラスでの機能はありませんが、データ ソースのクエリをリセットする FormDataSource.removeFilter メソッドにより上書きされます。</span><span class="sxs-lookup"><span data-stu-id="28cae-322">Has no functionality in the FormObjectSet class but is overridden by the FormDataSource.removeFilter method, which resets the query for the data source.</span></span>

```xpp
public void removeFilter()
```

