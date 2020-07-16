---
title: FormDataSource クラス
description: このトピックでは、FormDataSource クラスについて説明します。
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
ms.openlocfilehash: 2e0077269d1c575f3f7bca2b580cd9e51ffe76bd
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502625"
---
# <a name="class-formdatasource"></a><span data-ttu-id="a12fc-103">クラス FormDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-103">Class FormDataSource</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormDataSource extends FormObjectSet
```

<span data-ttu-id="a12fc-104">FormDataSource クラスには、フォーム内のデータ ソースの動作を定義するプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a12fc-104">The FormDataSource class contains properties that define the behavior of data sources in forms.</span></span>

## <a name="remarks"></a><span data-ttu-id="a12fc-105">備考</span><span class="sxs-lookup"><span data-stu-id="a12fc-105">Remarks</span></span>

<span data-ttu-id="a12fc-106">クラスのメソッドを上書きすることにより、特定のフォームの挿入または検証などのメソッド アクションの動作をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-106">By overriding the methods on the class, you can customize the behavior for the method actions, such as insertion or validation, for a specific form.</span></span> <span data-ttu-id="a12fc-107">FormDataSource クラスは、データ ソース テーブルが、フォームに表示される他のデータ ソース (テーブル) にどのように関連するかを決定するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-107">The FormDataSource class is also used to determine how the data source table is related to other data sources (tables) that are displayed in the form.</span></span> <span data-ttu-id="a12fc-108">FormDataSource クラスの一部のメソッドをオーバーライドするには、フォーム データソースのメソッド ノードを右クリックし、[メソッドをオーバーライド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-108">To override some of the methods in the FormDataSource class, right-click the Methods node for a form data source, and then click Override Method.</span></span> <span data-ttu-id="a12fc-109">フォームに対してメソッドを作成するときは、特定のクラスの FormDataSource オブジェクトを参照するために、\_ds 識別子を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-109">When you create methods on a form, you should use a \_ds identifier to reference the FormDataSource object for a particular class.</span></span> <span data-ttu-id="a12fc-110">たとえば、CustTrans\_ds は、フォームの CustTrans データ ソースに対する FormDataSource オブジェクトを参照し、CustTrans\_ds.executeQuery() は CustTrans データ ソースの FormDataSource.executeQuery メソッドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-110">For example, CustTrans\_ds references the FormDataSource object for the CustTrans data source on the form, and CustTrans\_ds.executeQuery() executes the FormDataSource.executeQuery method on the CustTrans data source.</span></span> <span data-ttu-id="a12fc-111">いくつかの FormDataSource メソッドは、FormObjectSet オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-111">Several FormDataSource methods return a FormObjectSet object.</span></span> <span data-ttu-id="a12fc-112">このオブジェクトの FormDataSource メソッドで定義されているメソッドを使用するには、FormDataSource オブジェクトに型キャストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-112">To use the methods that are defined on the FormDataSource method on this object, you must typecast it to a FormDataSource object.</span></span>

## <a name="examples"></a><span data-ttu-id="a12fc-113">例</span><span class="sxs-lookup"><span data-stu-id="a12fc-113">Examples</span></span>

<span data-ttu-id="a12fc-114">次の例は、自動的に生成されたクエリではなく、フィールドのカスタム クエリを提供します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-114">The following example supplies a custom query for a field instead of the automatically generated query.</span></span> <span data-ttu-id="a12fc-115">これは、フィールドの performFormLookup メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-115">It overrides the performFormLookup method on the field.</span></span>

```xpp
public void performFormLookup(FormRun _p1, FormControl _formControl)  
{ 
    FormDataSource formDataSource; 
    QueryRun queryRunGenerated; 
    // The FormDataSource object retrieved from the FormRun parameter. 
    formDataSource = _p1.dataSource(1); 
    // Get the generated query. 
    queryRunGenerated = formDataSource.queryRun(); 
    // Modify the query. 
    // ... 
    // Call the standard implementation of performFormLookup 
    // with the parameters supplied in this method. 
    super(_p1, _formControl); 
}
```

## <a name="methods"></a><span data-ttu-id="a12fc-116">メソッド</span><span class="sxs-lookup"><span data-stu-id="a12fc-116">Methods</span></span>

| <span data-ttu-id="a12fc-117">方法</span><span class="sxs-lookup"><span data-stu-id="a12fc-117">Method</span></span>                                                                                                                         | <span data-ttu-id="a12fc-118">説明</span><span class="sxs-lookup"><span data-stu-id="a12fc-118">Description</span></span>                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12fc-119">public int active()</span><span class="sxs-lookup"><span data-stu-id="a12fc-119">public int active()</span></span>                                                                                                            | <span data-ttu-id="a12fc-120">ユーザーが新しいレコードに移動し、現在のレコードとして新しいレコードを設定するときに、結合されたデータ ソースからデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-120">Retrieves data from joined data sources when a user navigates to a new record and then sets the new record as the current record.</span></span>                        |
| <span data-ttu-id="a12fc-121">public boolean allowCheck(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-121">public boolean allowCheck(\[boolean value\])</span></span>                                                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-122">public boolean allowCreate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-122">public boolean allowCreate(\[boolean value\])</span></span>                                                                                  |                                                                                                                                                          |
| <span data-ttu-id="a12fc-123">public boolean allowDeferredLoad(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-123">public boolean allowDeferredLoad(\[boolean value\])</span></span>                                                                            |                                                                                                                                                          |
| <span data-ttu-id="a12fc-124">public boolean allowDelete(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-124">public boolean allowDelete(\[boolean value\])</span></span>                                                                                  |                                                                                                                                                          |
| <span data-ttu-id="a12fc-125">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-125">public boolean allowEdit(\[boolean value\])</span></span>                                                                                    | <span data-ttu-id="a12fc-126">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-126">Determines whether the user can change the contents of the control.</span></span>                                                                                      |
| <span data-ttu-id="a12fc-127">public boolean allRowsLoaded()</span><span class="sxs-lookup"><span data-stu-id="a12fc-127">public boolean allRowsLoaded()</span></span>                                                                                                 |                                                                                                                                                          |
| <span data-ttu-id="a12fc-128">public boolean anyMarked()</span><span class="sxs-lookup"><span data-stu-id="a12fc-128">public boolean anyMarked()</span></span>                                                                                                     | <span data-ttu-id="a12fc-129">基になるキャッシュ内のレコードがマークされているかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-129">Checks whether any records in the underlying cache are marked.</span></span>                                                                                           |
| <span data-ttu-id="a12fc-130">public boolean autoNotify(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-130">public boolean autoNotify(\[boolean value\])</span></span>                                                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-131">public boolean autoQuery(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-131">public boolean autoQuery(\[boolean value\])</span></span>                                                                                    |                                                                                                                                                          |
| <span data-ttu-id="a12fc-132">public boolean autoSearch(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-132">public boolean autoSearch(\[boolean value\])</span></span>                                                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-133">public str bindField(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="a12fc-133">public str bindField(FieldId fieldId)</span></span>                                                                                          |                                                                                                                                                          |
| <span data-ttu-id="a12fc-134">public str bindDataMethod(str dataMethodName)</span><span class="sxs-lookup"><span data-stu-id="a12fc-134">public str bindDataMethod(str dataMethodName)</span></span>                                                                                  |                                                                                                                                                          |
| <span data-ttu-id="a12fc-135">public boolean cacheAddMethod(str methodName, \[boolean updateOnWrite\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-135">public boolean cacheAddMethod(str methodName, \[boolean updateOnWrite\])</span></span>                                                       | <span data-ttu-id="a12fc-136">キャッシュの指定された表示または編集方法を登録します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-136">Registers the specified display or edit method for caching.</span></span>                                                                                              |
| <span data-ttu-id="a12fc-137">public boolean cacheCalculateMethod(str methodName)</span><span class="sxs-lookup"><span data-stu-id="a12fc-137">public boolean cacheCalculateMethod(str methodName)</span></span>                                                                            | <span data-ttu-id="a12fc-138">指定されたキャッシュされたメソッドを呼び出し、現在のレコードのキャッシュ内の値を更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-138">Calls the specified cached method and updates the value in the cache for the current record.</span></span>                                                             |
| <span data-ttu-id="a12fc-139">public boolean cacheOnlyMode(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-139">public boolean cacheOnlyMode(\[boolean value\])</span></span>                                                                                |                                                                                                                                                          |
| <span data-ttu-id="a12fc-140">public boolean canCreate()</span><span class="sxs-lookup"><span data-stu-id="a12fc-140">public boolean canCreate()</span></span>                                                                                                     |                                                                                                                                                          |
| <span data-ttu-id="a12fc-141">public boolean canDelete()</span><span class="sxs-lookup"><span data-stu-id="a12fc-141">public boolean canDelete()</span></span>                                                                                                     |                                                                                                                                                          |
| <span data-ttu-id="a12fc-142">public boolean canEdit()</span><span class="sxs-lookup"><span data-stu-id="a12fc-142">public boolean canEdit()</span></span>                                                                                                       |                                                                                                                                                          |
| <span data-ttu-id="a12fc-143">public int clientPageSize(\[int pageSize\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-143">public int clientPageSize(\[int pageSize\])</span></span>                                                                                    |                                                                                                                                                          |
| <span data-ttu-id="a12fc-144">public str company(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-144">public str company(\[str value\])</span></span>                                                                                              |                                                                                                                                                          |
| <span data-ttu-id="a12fc-145">public FieldId counterField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-145">public FieldId counterField(\[FieldId value\])</span></span>                                                                                 |                                                                                                                                                          |
| <span data-ttu-id="a12fc-146">public boolean crossCompanyAutoQuery(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-146">public boolean crossCompanyAutoQuery(\[boolean value\])</span></span>                                                                        |                                                                                                                                                          |
| <span data-ttu-id="a12fc-147">public Common cursor(\[int rowIndex\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-147">public Common cursor(\[int rowIndex\])</span></span>                                                                                         | <span data-ttu-id="a12fc-148">FormObjectSet クラスには機能がありません。</span><span class="sxs-lookup"><span data-stu-id="a12fc-148">Has no functionality in the FormObjectSet class.</span></span>                                                                                                         |
| <span data-ttu-id="a12fc-149">public int defaultMark(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-149">public int defaultMark(\[int value\])</span></span>                                                                                          | <span data-ttu-id="a12fc-150">グリッドで選択されたときにレコードがマークされるかどうかを決定する、フォーム内のレコードの既定のマーク値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-150">Sets the default mark value for records in a form, which determines whether records are marked when they have been selected in a grid.</span></span>                   |
| <span data-ttu-id="a12fc-151">public boolean delayActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-151">public boolean delayActive(\[boolean value\])</span></span>                                                                                  |                                                                                                                                                          |
| <span data-ttu-id="a12fc-152">public int extends(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-152">public int extends(\[AnyType value\])</span></span>                                                                                          |                                                                                                                                                          |
| <span data-ttu-id="a12fc-153">public boolean findRecord(Common record)</span><span class="sxs-lookup"><span data-stu-id="a12fc-153">public boolean findRecord(Common record)</span></span>                                                                                       | <span data-ttu-id="a12fc-154">データ ソースで指定されたレコードを検索し、それが現在のレコードになります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-154">Finds the specified record in the data source and makes it the current record.</span></span>                                                                           |
| <span data-ttu-id="a12fc-155">public boolean findValue(FieldId field, str value)</span><span class="sxs-lookup"><span data-stu-id="a12fc-155">public boolean findValue(FieldId field, str value)</span></span>                                                                             | <span data-ttu-id="a12fc-156">データ ソースで指定された値を検索し、そのレコードが FormDataSource.findRecord メソッドを使用する現在のレコードの値を持つようにします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-156">Finds the specified value in the data source and makes the record that has that value the current record that uses the FormDataSource.findRecord method.</span></span> |
| <span data-ttu-id="a12fc-157">public boolean positionToRecord(Common record)</span><span class="sxs-lookup"><span data-stu-id="a12fc-157">public boolean positionToRecord(Common record)</span></span>                                                                                 |                                                                                                                                                          |
| <span data-ttu-id="a12fc-158">public boolean positionToRecordByValue(FieldId field, str value)</span><span class="sxs-lookup"><span data-stu-id="a12fc-158">public boolean positionToRecordByValue(FieldId field, str value)</span></span>                                                               |                                                                                                                                                          |
| <span data-ttu-id="a12fc-159">public int first()</span><span class="sxs-lookup"><span data-stu-id="a12fc-159">public int first()</span></span>                                                                                                             | <span data-ttu-id="a12fc-160">データ ソースの最初のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-160">Moves focus to the first record in the data source.</span></span>                                                                                                      |
| <span data-ttu-id="a12fc-161">public boolean forceWrite(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-161">public boolean forceWrite(\[boolean value\])</span></span>                                                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-162">public FormObject functionObject(str name)</span><span class="sxs-lookup"><span data-stu-id="a12fc-162">public FormObject functionObject(str name)</span></span>                                                                                     |                                                                                                                                                          |
| <span data-ttu-id="a12fc-163">public FormDataRow getDataRow(\[int rowIndex\], \[boolean allowFetchAhead\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-163">public FormDataRow getDataRow(\[int rowIndex\], \[boolean allowFetchAhead\])</span></span>                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-164">public Common getFirst(\[int mark\], \[boolean fetchAhead\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-164">public Common getFirst(\[int mark\], \[boolean fetchAhead\])</span></span>                                                                   | <span data-ttu-id="a12fc-165">データ セットの最初のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-165">Retrieves the first record in a data set.</span></span>                                                                                                                |
| <span data-ttu-id="a12fc-166">public Common getNext()</span><span class="sxs-lookup"><span data-stu-id="a12fc-166">public Common getNext()</span></span>                                                                                                        | <span data-ttu-id="a12fc-167">FormDataSource.getFirst メソッドへの以前の呼び出しで設定されている条件に合う次のレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-167">Returns the next record that meets the criteria that are set up in an earlier call to the FormDataSource.getFirst method.</span></span>                                |
| <span data-ttu-id="a12fc-168">public int id()</span><span class="sxs-lookup"><span data-stu-id="a12fc-168">public int id()</span></span>                                                                                                                | <span data-ttu-id="a12fc-169">データ ソースの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-169">Retrieves the ID of the data source.</span></span>                                                                                                                     |
| <span data-ttu-id="a12fc-170">public IndexId index(\[IndexId value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-170">public IndexId index(\[IndexId value\])</span></span>                                                                                        |                                                                                                                                                          |
| <span data-ttu-id="a12fc-171">public boolean insertAtEnd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-171">public boolean insertAtEnd(\[boolean value\])</span></span>                                                                                  |                                                                                                                                                          |
| <span data-ttu-id="a12fc-172">public boolean insertIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-172">public boolean insertIfEmpty(\[boolean value\])</span></span>                                                                                |                                                                                                                                                          |
| <span data-ttu-id="a12fc-173">public boolean isBaseDataSource()</span><span class="sxs-lookup"><span data-stu-id="a12fc-173">public boolean isBaseDataSource()</span></span>                                                                                              |                                                                                                                                                          |
| <span data-ttu-id="a12fc-174">public boolean isInheritanceDataSource()</span><span class="sxs-lookup"><span data-stu-id="a12fc-174">public boolean isInheritanceDataSource()</span></span>                                                                                       |                                                                                                                                                          |
| <span data-ttu-id="a12fc-175">private boolean isOptionalRecordCreated(\[boolean set\], Common record, \[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-175">private boolean isOptionalRecordCreated(\[boolean set\], Common record, \[boolean value\])</span></span>                                     |                                                                                                                                                          |
| <span data-ttu-id="a12fc-176">public boolean isReferenceDataSource()</span><span class="sxs-lookup"><span data-stu-id="a12fc-176">public boolean isReferenceDataSource()</span></span>                                                                                         |                                                                                                                                                          |
| <span data-ttu-id="a12fc-177">public str joinRelation(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-177">public str joinRelation(\[str value\])</span></span>                                                                                         |                                                                                                                                                          |
| <span data-ttu-id="a12fc-178">public DictRelation joinRelationAsDictRelation()</span><span class="sxs-lookup"><span data-stu-id="a12fc-178">public DictRelation joinRelationAsDictRelation()</span></span>                                                                               |                                                                                                                                                          |
| <span data-ttu-id="a12fc-179">public int joinSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-179">public int joinSource(\[AnyType value\])</span></span>                                                                                       |                                                                                                                                                          |
| <span data-ttu-id="a12fc-180">public FormDataSource joinSourceDataSource()</span><span class="sxs-lookup"><span data-stu-id="a12fc-180">public FormDataSource joinSourceDataSource()</span></span>                                                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-181">public int last()</span><span class="sxs-lookup"><span data-stu-id="a12fc-181">public int last()</span></span>                                                                                                              | <span data-ttu-id="a12fc-182">データ ソースの最後のレコードにマウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-182">Moves the mouse pointer to the last record in the data source.</span></span>                                                                                           |
| <span data-ttu-id="a12fc-183">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="a12fc-183">public boolean leave()</span></span>                                                                                                         | <span data-ttu-id="a12fc-184">マウス ポインターが次のレコードまたは別のデータ ソースに移動すると、通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-184">Provides notification when the mouse pointer is moved to the next record or to another data source.</span></span>                                                      |
| <span data-ttu-id="a12fc-185">public boolean leaveRecord(\[boolean forceUpdate\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-185">public boolean leaveRecord(\[boolean forceUpdate\])</span></span>                                                                            | <span data-ttu-id="a12fc-186">別のレコードまたはフォームの品目にフォーカスが移動したときに通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-186">Provides notification when the focus moves to another record or item in the form.</span></span>                                                                        |
| <span data-ttu-id="a12fc-187">public container resolvePartLinks(\[str relationName\], \[int partTableId\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-187">public container resolvePartLinks(\[str relationName\], \[int partTableId\])</span></span>                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-188">public int linkType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-188">public int linkType(\[int value\])</span></span>                                                                                             |                                                                                                                                                          |
| <span data-ttu-id="a12fc-189">public int mark(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-189">public int mark(\[int value\])</span></span>                                                                                                 |                                                                                                                                                          |
| <span data-ttu-id="a12fc-190">public boolean markAllLoadedRecords(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-190">public boolean markAllLoadedRecords(\[int value\])</span></span>                                                                             |                                                                                                                                                          |
| <span data-ttu-id="a12fc-191">public int markRecord(AnyType record, \[int mark\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-191">public int markRecord(AnyType record, \[int mark\])</span></span>                                                                            | <span data-ttu-id="a12fc-192">指定されたマーク値を使用して、指定されたレコードをマークします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-192">Marks the specified record by using the specified mark value.</span></span>                                                                                            |
| <span data-ttu-id="a12fc-193">public boolean markRecords(Array markedRecordIds)</span><span class="sxs-lookup"><span data-stu-id="a12fc-193">public boolean markRecords(Array markedRecordIds)</span></span>                                                                              |                                                                                                                                                          |
| <span data-ttu-id="a12fc-194">public FormDataSource masterInheritanceDataSource()</span><span class="sxs-lookup"><span data-stu-id="a12fc-194">public FormDataSource masterInheritanceDataSource()</span></span>                                                                            |                                                                                                                                                          |
| <span data-ttu-id="a12fc-195">public int maxAccessRight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-195">public int maxAccessRight(\[int value\])</span></span>                                                                                       |                                                                                                                                                          |
| <span data-ttu-id="a12fc-196">public int maxRecordsToLoad(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-196">public int maxRecordsToLoad(\[int value\])</span></span>                                                                                     |                                                                                                                                                          |
| <span data-ttu-id="a12fc-197">public Int64 maxPagingRowCountValue(\[Int64 newValue\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-197">public Int64 maxPagingRowCountValue(\[Int64 newValue\])</span></span>                                                                        |                                                                                                                                                          |
| <span data-ttu-id="a12fc-198">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-198">public str name(\[str value\])</span></span>                                                                                                 | <span data-ttu-id="a12fc-199">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-199">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                  |
| <span data-ttu-id="a12fc-200">public int next()</span><span class="sxs-lookup"><span data-stu-id="a12fc-200">public int next()</span></span>                                                                                                              | <span data-ttu-id="a12fc-201">データ ソースの次のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-201">Moves the focus to the next record in the data source.</span></span>                                                                                                   |
| <span data-ttu-id="a12fc-202">public int nextPage(int pageSize)</span><span class="sxs-lookup"><span data-stu-id="a12fc-202">public int nextPage(int pageSize)</span></span>                                                                                              | <span data-ttu-id="a12fc-203">データ ソースで指定した数のレコード (位置変更) を進めます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-203">Moves a specified number of records forward in the data source.</span></span>                                                                                          |
| <span data-ttu-id="a12fc-204">public int numberOfRowsLoaded(\[boolean redirectToMasterDS\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-204">public int numberOfRowsLoaded(\[boolean redirectToMasterDS\])</span></span>                                                                  |                                                                                                                                                          |
| <span data-ttu-id="a12fc-205">public FormDataObject object(FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-205">public FormDataObject object(FieldId fieldId, \[int arrayIndex\])</span></span>                                                              | <span data-ttu-id="a12fc-206">指定した ID を持つ FormDataObject クラスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-206">Returns an instance of the FormDataObject class that has the specified ID.</span></span>                                                                               |
| <span data-ttu-id="a12fc-207">public boolean onlyFetchActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-207">public boolean onlyFetchActive(\[boolean value\])</span></span>                                                                              |                                                                                                                                                          |
| <span data-ttu-id="a12fc-208">public int optionalRecordMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-208">public int optionalRecordMode(\[int value\])</span></span>                                                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-209">public int pageSize()</span><span class="sxs-lookup"><span data-stu-id="a12fc-209">public int pageSize()</span></span>                                                                                                          |                                                                                                                                                          |
| <span data-ttu-id="a12fc-210">public boolean pagingEnabled()</span><span class="sxs-lookup"><span data-stu-id="a12fc-210">public boolean pagingEnabled()</span></span>                                                                                                 |                                                                                                                                                          |
| <span data-ttu-id="a12fc-211">public TitleFields parentTitleFields(Common record)</span><span class="sxs-lookup"><span data-stu-id="a12fc-211">public TitleFields parentTitleFields(Common record)</span></span>                                                                            |                                                                                                                                                          |
| <span data-ttu-id="a12fc-212">public int prev()</span><span class="sxs-lookup"><span data-stu-id="a12fc-212">public int prev()</span></span>                                                                                                              | <span data-ttu-id="a12fc-213">データ ソースの前のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-213">Moves the focus to the previous record in the data source.</span></span>                                                                                               |
| <span data-ttu-id="a12fc-214">public int prevPage(int pageSize)</span><span class="sxs-lookup"><span data-stu-id="a12fc-214">public int prevPage(int pageSize)</span></span>                                                                                              | <span data-ttu-id="a12fc-215">データ ソースで指定した数のレコード分フォーカスを戻します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-215">Moves the focus back by a specified number of records in the data source.</span></span>                                                                                |
| <span data-ttu-id="a12fc-216">public Query query(\[Query value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-216">public Query query(\[Query value\])</span></span>                                                                                            |                                                                                                                                                          |
| <span data-ttu-id="a12fc-217">public QueryBuildDataSource queryBuildDataSource()</span><span class="sxs-lookup"><span data-stu-id="a12fc-217">public QueryBuildDataSource queryBuildDataSource()</span></span>                                                                             |                                                                                                                                                          |
| <span data-ttu-id="a12fc-218">public QueryRun queryRun(\[QueryRun value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-218">public QueryRun queryRun(\[QueryRun value\])</span></span>                                                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-219">public QueryBuildDataSource queryRunQueryBuildDataSource()</span><span class="sxs-lookup"><span data-stu-id="a12fc-219">public QueryBuildDataSource queryRunQueryBuildDataSource()</span></span>                                                                     |                                                                                                                                                          |
| <span data-ttu-id="a12fc-220">public Array recordsMarked()</span><span class="sxs-lookup"><span data-stu-id="a12fc-220">public Array recordsMarked()</span></span>                                                                                                   |                                                                                                                                                          |
| <span data-ttu-id="a12fc-221">public int startPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-221">public int startPosition(\[int value\])</span></span>                                                                                        |                                                                                                                                                          |
| <span data-ttu-id="a12fc-222">public int startRowIndex()</span><span class="sxs-lookup"><span data-stu-id="a12fc-222">public int startRowIndex()</span></span>                                                                                                     |                                                                                                                                                          |
| <span data-ttu-id="a12fc-223">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-223">public TableId table(\[TableId value\])</span></span>                                                                                        | <span data-ttu-id="a12fc-224">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-224">Gets or sets the table ID associated with the object.</span></span>                                                                                                    |
| <span data-ttu-id="a12fc-225">public TitleFields titleFields(Common record)</span><span class="sxs-lookup"><span data-stu-id="a12fc-225">public TitleFields titleFields(Common record)</span></span>                                                                                  |                                                                                                                                                          |
| <span data-ttu-id="a12fc-226">public int totalNumberOfRows()</span><span class="sxs-lookup"><span data-stu-id="a12fc-226">public int totalNumberOfRows()</span></span>                                                                                                 |                                                                                                                                                          |
| <span data-ttu-id="a12fc-227">public boolean validateDelete()</span><span class="sxs-lookup"><span data-stu-id="a12fc-227">public boolean validateDelete()</span></span>                                                                                                | <span data-ttu-id="a12fc-228">ユーザーがデータ ソースからのレコードの削除を確認することを要求します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-228">Requests that the user confirm the deletion of a record from the data source.</span></span>                                                                            |
| <span data-ttu-id="a12fc-229">public boolean validateWrite()</span><span class="sxs-lookup"><span data-stu-id="a12fc-229">public boolean validateWrite()</span></span>                                                                                                 | <span data-ttu-id="a12fc-230">データが有効で書き込み可能な状態かどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-230">Determines whether data is valid and ready to be written.</span></span>                                                                                                |
| <span data-ttu-id="a12fc-231">public int validTimeStateAutoQuery(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-231">public int validTimeStateAutoQuery(\[int value\])</span></span>                                                                              |                                                                                                                                                          |
| <span data-ttu-id="a12fc-232">public int validTimeStateUpdate(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-232">public int validTimeStateUpdate(\[int value\])</span></span>                                                                                 |                                                                                                                                                          |
| <span data-ttu-id="a12fc-233">public void delete()</span><span class="sxs-lookup"><span data-stu-id="a12fc-233">public void delete()</span></span>                                                                                                           | <span data-ttu-id="a12fc-234">データ ソースから現在のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-234">Deletes the current record from the data source.</span></span>                                                                                                         |
| <span data-ttu-id="a12fc-235">public void addFieldToSelectionList(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="a12fc-235">public void addFieldToSelectionList(FieldId fieldId)</span></span>                                                                           |                                                                                                                                                          |
| <span data-ttu-id="a12fc-236">public void cacheRemoveRecord(\[Common record\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-236">public void cacheRemoveRecord(\[Common record\])</span></span>                                                                               | <span data-ttu-id="a12fc-237">データ ソースの基になるキャッシュから指定されたレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-237">Removes the specified record from the underlying cache of the data source.</span></span>                                                                               |
| <span data-ttu-id="a12fc-238">private void OnValidatedWrite(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-238">private void OnValidatedWrite(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                        |                                                                                                                                                          |
| <span data-ttu-id="a12fc-239">public void reread()</span><span class="sxs-lookup"><span data-stu-id="a12fc-239">public void reread()</span></span>                                                                                                           | <span data-ttu-id="a12fc-240">データベースから現在のレコードを再読み取りします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-240">Rereads the current record from the database.</span></span>                                                                                                            |
| <span data-ttu-id="a12fc-241">public void rereadJoinHierarchy()</span><span class="sxs-lookup"><span data-stu-id="a12fc-241">public void rereadJoinHierarchy()</span></span>                                                                                              |                                                                                                                                                          |
| <span data-ttu-id="a12fc-242">private void OnRefreshed(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-242">private void OnRefreshed(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                             |                                                                                                                                                          |
| <span data-ttu-id="a12fc-243">private void OnValidatedDelete(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-243">private void OnValidatedDelete(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                       |                                                                                                                                                          |
| <span data-ttu-id="a12fc-244">public void markChanged()</span><span class="sxs-lookup"><span data-stu-id="a12fc-244">public void markChanged()</span></span>                                                                                                      |                                                                                                                                                          |
| <span data-ttu-id="a12fc-245">public void setPagingParameters(boolean pagingEnabled, int startRowIndex, int pageSize)</span><span class="sxs-lookup"><span data-stu-id="a12fc-245">public void setPagingParameters(boolean pagingEnabled, int startRowIndex, int pageSize)</span></span>                                        |                                                                                                                                                          |
| <span data-ttu-id="a12fc-246">public void deleted()</span><span class="sxs-lookup"><span data-stu-id="a12fc-246">public void deleted()</span></span>                                                                                                          |                                                                                                                                                          |
| <span data-ttu-id="a12fc-247">public void print(PrintMedium target)</span><span class="sxs-lookup"><span data-stu-id="a12fc-247">public void print(PrintMedium target)</span></span>                                                                                          | <span data-ttu-id="a12fc-248">現在のレコードを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-248">Prints the current record.</span></span>                                                                                                                               |
| <span data-ttu-id="a12fc-249">private void OnReread(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-249">private void OnReread(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                                |                                                                                                                                                          |
| <span data-ttu-id="a12fc-250">public void research(\[boolean retainPosition\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-250">public void research(\[boolean retainPosition\])</span></span>                                                                               | <span data-ttu-id="a12fc-251">FormDataSource.research メソッドでオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-251">Is overridden by the FormDataSource.research method.</span></span>                                                                                                     |
| <span data-ttu-id="a12fc-252">public void createTypes(Map concreteTypesToCreate, \[boolean append\], \[boolean implicitCreate\], \[boolean explicitCreate\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-252">public void createTypes(Map concreteTypesToCreate, \[boolean append\], \[boolean implicitCreate\], \[boolean explicitCreate\])</span></span> |                                                                                                                                                          |
| <span data-ttu-id="a12fc-253">private void OnCreated(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-253">private void OnCreated(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                               |                                                                                                                                                          |
| <span data-ttu-id="a12fc-254">private void OnQueryExecuted(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-254">private void OnQueryExecuted(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                         |                                                                                                                                                          |
| <span data-ttu-id="a12fc-255">public void written()</span><span class="sxs-lookup"><span data-stu-id="a12fc-255">public void written()</span></span>                                                                                                          |                                                                                                                                                          |
| <span data-ttu-id="a12fc-256">public void filter(FieldId field, str value)</span><span class="sxs-lookup"><span data-stu-id="a12fc-256">public void filter(FieldId field, str value)</span></span>                                                                                   | <span data-ttu-id="a12fc-257">フィルターはデータ ソースで記録します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-257">Filters records in the data source.</span></span>                                                                                                                      |
| <span data-ttu-id="a12fc-258">public void refresh()</span><span class="sxs-lookup"><span data-stu-id="a12fc-258">public void refresh()</span></span>                                                                                                          | <span data-ttu-id="a12fc-259">データ ソース内のすべてのレコードのビューを更新してフォームを更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-259">Updates the form by updating the view of all the records in the data source.</span></span>                                                                             |
| <span data-ttu-id="a12fc-260">public void write()</span><span class="sxs-lookup"><span data-stu-id="a12fc-260">public void write()</span></span>                                                                                                            | <span data-ttu-id="a12fc-261">FormDataSource.validateWrite メソッドを呼び出し、データベースの書き込み操作を管理します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-261">Calls the FormDataSource.validateWrite method and manages the database write operation.</span></span>                                                                  |
| <span data-ttu-id="a12fc-262">public void executeQuery()</span><span class="sxs-lookup"><span data-stu-id="a12fc-262">public void executeQuery()</span></span>                                                                                                     | <span data-ttu-id="a12fc-263">データ ソース クエリを実行し、取得されたレコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-263">Executes the data source query and displays the records that are retrieved.</span></span>                                                                              |
| <span data-ttu-id="a12fc-264">public void setRecord(Common record)</span><span class="sxs-lookup"><span data-stu-id="a12fc-264">public void setRecord(Common record)</span></span>                                                                                           |                                                                                                                                                          |
| <span data-ttu-id="a12fc-265">public void refreshEx(\[AnyType pos\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-265">public void refreshEx(\[AnyType pos\])</span></span>                                                                                         | <span data-ttu-id="a12fc-266">指定されたレコードのビューを更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-266">Updates the view of the specified records.</span></span>                                                                                                               |
| <span data-ttu-id="a12fc-267">public void setCurrent()</span><span class="sxs-lookup"><span data-stu-id="a12fc-267">public void setCurrent()</span></span>                                                                                                       |                                                                                                                                                          |
| <span data-ttu-id="a12fc-268">private void OnValidatingDelete(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-268">private void OnValidatingDelete(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                      |                                                                                                                                                          |
| <span data-ttu-id="a12fc-269">public void writing()</span><span class="sxs-lookup"><span data-stu-id="a12fc-269">public void writing()</span></span>                                                                                                          |                                                                                                                                                          |
| <span data-ttu-id="a12fc-270">private void OnWritten(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-270">private void OnWritten(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                               |                                                                                                                                                          |
| <span data-ttu-id="a12fc-271">public void clearDisplayOption(Common record)</span><span class="sxs-lookup"><span data-stu-id="a12fc-271">public void clearDisplayOption(Common record)</span></span>                                                                                  | <span data-ttu-id="a12fc-272">レコードに対して以前に指定された表示オプションをクリアして、レコードを再描画します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-272">Clears display options that were previously specified for a record and then redraws the record.</span></span>                                                          |
| <span data-ttu-id="a12fc-273">private void OnMarkChanged(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-273">private void OnMarkChanged(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                           |                                                                                                                                                          |
| <span data-ttu-id="a12fc-274">private void OnLeftRecord(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-274">private void OnLeftRecord(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                            |                                                                                                                                                          |
| <span data-ttu-id="a12fc-275">private void OnDeleted(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-275">private void OnDeleted(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                               |                                                                                                                                                          |
| <span data-ttu-id="a12fc-276">public void removeFilter()</span><span class="sxs-lookup"><span data-stu-id="a12fc-276">public void removeFilter()</span></span>                                                                                                     | <span data-ttu-id="a12fc-277">データ ソースのクエリをリセットします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-277">Resets the query for the data source.</span></span>                                                                                                                    |
| <span data-ttu-id="a12fc-278">private void OnInitialized(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-278">private void OnInitialized(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                           |                                                                                                                                                          |
| <span data-ttu-id="a12fc-279">private void OnPostLinkActive(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-279">private void OnPostLinkActive(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                        |                                                                                                                                                          |
| <span data-ttu-id="a12fc-280">private void OnSelectionChanged(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-280">private void OnSelectionChanged(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                      |                                                                                                                                                          |
| <span data-ttu-id="a12fc-281">public void deleting()</span><span class="sxs-lookup"><span data-stu-id="a12fc-281">public void deleting()</span></span>                                                                                                         |                                                                                                                                                          |
| <span data-ttu-id="a12fc-282">public void observe()</span><span class="sxs-lookup"><span data-stu-id="a12fc-282">public void observe()</span></span>                                                                                                          |                                                                                                                                                          |
| <span data-ttu-id="a12fc-283">private void OnWriting(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-283">private void OnWriting(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                               |                                                                                                                                                          |
| <span data-ttu-id="a12fc-284">private void OnActivated(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-284">private void OnActivated(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                             |                                                                                                                                                          |
| <span data-ttu-id="a12fc-285">public void removeFieldFromSelectionList(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="a12fc-285">public void removeFieldFromSelectionList(FieldId fieldId)</span></span>                                                                      |                                                                                                                                                          |
| <span data-ttu-id="a12fc-286">private void OnCreating(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-286">private void OnCreating(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                              |                                                                                                                                                          |
| <span data-ttu-id="a12fc-287">public void rereadReferenceDataSources()</span><span class="sxs-lookup"><span data-stu-id="a12fc-287">public void rereadReferenceDataSources()</span></span>                                                                                       |                                                                                                                                                          |
| <span data-ttu-id="a12fc-288">private void OnValidatingWrite(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-288">private void OnValidatingWrite(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                       |                                                                                                                                                          |
| <span data-ttu-id="a12fc-289">public void prompt()</span><span class="sxs-lookup"><span data-stu-id="a12fc-289">public void prompt()</span></span>                                                                                                           | <span data-ttu-id="a12fc-290">クエリの範囲を制限するために使用される、標準フォーム、SysQueryForm を有効化します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-290">Activates the standard form, SysQueryForm, that is used to limit a query range.</span></span>                                                                          |
| <span data-ttu-id="a12fc-291">private void OnQueryExecuting(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-291">private void OnQueryExecuting(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                        |                                                                                                                                                          |
| <span data-ttu-id="a12fc-292">private void OnInitValue(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-292">private void OnInitValue(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                             |                                                                                                                                                          |
| <span data-ttu-id="a12fc-293">public void clearReferenceData(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="a12fc-293">public void clearReferenceData(FieldId fieldId)</span></span>                                                                                |                                                                                                                                                          |
| <span data-ttu-id="a12fc-294">public void cursorNotify(int event)</span><span class="sxs-lookup"><span data-stu-id="a12fc-294">public void cursorNotify(int event)</span></span>                                                                                            | <span data-ttu-id="a12fc-295">カーソルのイベントに関してアプリケーションに通知します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-295">Notifies the application about a cursor event.</span></span>                                                                                                           |
| <span data-ttu-id="a12fc-296">public void displayOption(Common record, FormRowDisplayOption options)</span><span class="sxs-lookup"><span data-stu-id="a12fc-296">public void displayOption(Common record, FormRowDisplayOption options)</span></span>                                                         | <span data-ttu-id="a12fc-297">データ ソース内のレコードのテキストの色および背景色を設定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-297">Sets the text color and the background color for a record in the data source.</span></span>                                                                            |
| <span data-ttu-id="a12fc-298">public void create(\[boolean append\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-298">public void create(\[boolean append\])</span></span>                                                                                         | <span data-ttu-id="a12fc-299">データ ソースに新しいレコードを作成します</span><span class="sxs-lookup"><span data-stu-id="a12fc-299">Creates a new record in the data source.</span></span>                                                                                                                 |
| <span data-ttu-id="a12fc-300">public void init()</span><span class="sxs-lookup"><span data-stu-id="a12fc-300">public void init()</span></span>                                                                                                             | <span data-ttu-id="a12fc-301">データソース プロパティに基づくデータソース クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-301">Creates a data source query that is based on the data source properties.</span></span>                                                                                 |
| <span data-ttu-id="a12fc-302">public void linkActive()</span><span class="sxs-lookup"><span data-stu-id="a12fc-302">public void linkActive()</span></span>                                                                                                       | <span data-ttu-id="a12fc-303">現在のデータソースにリンクされているデータソースの FormDataSource.exeuteQuery メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-303">Calls the FormDataSource.exeuteQuery method on data sources that are linked to the current data source.</span></span>                                                  |
| <span data-ttu-id="a12fc-304">public void selectionChanged()</span><span class="sxs-lookup"><span data-stu-id="a12fc-304">public void selectionChanged()</span></span>                                                                                                 |                                                                                                                                                          |
| <span data-ttu-id="a12fc-305">private void OnDeleting(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-305">private void OnDeleting(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                              |                                                                                                                                                          |
| <span data-ttu-id="a12fc-306">public void addReferenceFieldToSelectionList(FieldId fieldId, str referenceFieldGroupName)</span><span class="sxs-lookup"><span data-stu-id="a12fc-306">public void addReferenceFieldToSelectionList(FieldId fieldId, str referenceFieldGroupName)</span></span>                                     |                                                                                                                                                          |
| <span data-ttu-id="a12fc-307">public void initValue()</span><span class="sxs-lookup"><span data-stu-id="a12fc-307">public void initValue()</span></span>                                                                                                        | <span data-ttu-id="a12fc-308">新しいレコードでフィールド値を初期化します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-308">Initializes field values in a new record.</span></span>                                                                                                                |
| <span data-ttu-id="a12fc-309">public void deleteMarked()</span><span class="sxs-lookup"><span data-stu-id="a12fc-309">public void deleteMarked()</span></span>                                                                                                     | <span data-ttu-id="a12fc-310">マークされた (選択された) すべてのレコードをデータソースから削除します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-310">Deletes all marked (selected) records from a data source.</span></span>                                                                                                |
| <span data-ttu-id="a12fc-311">private void OnLeavingRecord(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="a12fc-311">private void OnLeavingRecord(\[FormDataSource sender\], \[FormDataSourceEventArgs e\])</span></span>                                         |                                                                                                                                                          |

## <a name="method-active"></a><span data-ttu-id="a12fc-312">メソッド active</span><span class="sxs-lookup"><span data-stu-id="a12fc-312">Method active</span></span>

<span data-ttu-id="a12fc-313">ユーザーが新しいレコードに移動し、現在のレコードとして新しいレコードを設定するときに、結合されたデータ ソースからデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-313">Retrieves data from joined data sources when a user navigates to a new record and then sets the new record as the current record.</span></span>

```xpp
public int active()
```

### <a name="return-value---active"></a><span data-ttu-id="a12fc-314">戻り値 - active</span><span class="sxs-lookup"><span data-stu-id="a12fc-314">Return Value - active</span></span>

<span data-ttu-id="a12fc-315">常に 1 を返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-315">Always returns 1.</span></span>

### <a name="remarks---active"></a><span data-ttu-id="a12fc-316">備考 - active</span><span class="sxs-lookup"><span data-stu-id="a12fc-316">Remarks - active</span></span>

<span data-ttu-id="a12fc-317">データ ソースの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントしてから [有効] をクリックすると、有効なメソッドをフォーム データ ソースでオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-317">The active method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking active.</span></span>

## <a name="method-allowcheck"></a><span data-ttu-id="a12fc-318">メソッド allowCheck</span><span class="sxs-lookup"><span data-stu-id="a12fc-318">Method allowCheck</span></span>

```xpp
public boolean allowCheck([boolean value])
```

### <a name="parameters---allowcheck"></a><span data-ttu-id="a12fc-319">パラメーター - allowCheck</span><span class="sxs-lookup"><span data-stu-id="a12fc-319">Parameters - allowCheck</span></span>

<span data-ttu-id="a12fc-320">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-320">value</span></span>  

### <a name="return-value---allowcheck"></a><span data-ttu-id="a12fc-321">戻り値 - allowCheck</span><span class="sxs-lookup"><span data-stu-id="a12fc-321">Return Value - allowCheck</span></span>

## <a name="method-allowcreate"></a><span data-ttu-id="a12fc-322">メソッド allowCreate</span><span class="sxs-lookup"><span data-stu-id="a12fc-322">Method allowCreate</span></span>

```xpp
public boolean allowCreate([boolean value])
```

### <a name="parameters---allowcreate"></a><span data-ttu-id="a12fc-323">パラメーター - allowCreate</span><span class="sxs-lookup"><span data-stu-id="a12fc-323">Parameters - allowCreate</span></span>

<span data-ttu-id="a12fc-324">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-324">value</span></span>  

### <a name="return-value---allowcreate"></a><span data-ttu-id="a12fc-325">戻り値 - allowCreate</span><span class="sxs-lookup"><span data-stu-id="a12fc-325">Return Value - allowCreate</span></span>

## <a name="method-allowdeferredload"></a><span data-ttu-id="a12fc-326">メソッド allowDeferredLoad</span><span class="sxs-lookup"><span data-stu-id="a12fc-326">Method allowDeferredLoad</span></span>

```xpp
public boolean allowDeferredLoad([boolean value])
```

### <a name="parameters---allowdeferredload"></a><span data-ttu-id="a12fc-327">パラメーター - allowDeferredLoad</span><span class="sxs-lookup"><span data-stu-id="a12fc-327">Parameters - allowDeferredLoad</span></span>

<span data-ttu-id="a12fc-328">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-328">value</span></span>  

### <a name="return-value---allowdeferredload"></a><span data-ttu-id="a12fc-329">戻り値 - allowDeferredLoad</span><span class="sxs-lookup"><span data-stu-id="a12fc-329">Return Value - allowDeferredLoad</span></span>

## <a name="method-allowdelete"></a><span data-ttu-id="a12fc-330">メソッド allowDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-330">Method allowDelete</span></span>

```xpp
public boolean allowDelete([boolean value])
```

### <a name="parameters---allowdelete"></a><span data-ttu-id="a12fc-331">パラメーター - allowDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-331">Parameters - allowDelete</span></span>

<span data-ttu-id="a12fc-332">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-332">value</span></span>  

### <a name="return-value---allowdelete"></a><span data-ttu-id="a12fc-333">戻り値 - allowDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-333">Return Value - allowDelete</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="a12fc-334">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="a12fc-334">Method allowEdit</span></span>

<span data-ttu-id="a12fc-335">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-335">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="a12fc-336">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a12fc-336">Parameters - allowEdit</span></span>

<span data-ttu-id="a12fc-337">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-337">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="a12fc-338">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a12fc-338">Return Value - allowEdit</span></span>

<span data-ttu-id="a12fc-339">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a12fc-339">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="a12fc-340">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a12fc-340">Remarks - allowEdit</span></span>

<span data-ttu-id="a12fc-341">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-341">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allrowsloaded"></a><span data-ttu-id="a12fc-342">メソッド allRowsLoaded</span><span class="sxs-lookup"><span data-stu-id="a12fc-342">Method allRowsLoaded</span></span>

```xpp
public boolean allRowsLoaded()
```

### <a name="return-value---allrowsloaded"></a><span data-ttu-id="a12fc-343">戻り値 - allRowsLoaded</span><span class="sxs-lookup"><span data-stu-id="a12fc-343">Return Value - allRowsLoaded</span></span>

## <a name="method-anymarked"></a><span data-ttu-id="a12fc-344">メソッド anyMarked</span><span class="sxs-lookup"><span data-stu-id="a12fc-344">Method anyMarked</span></span>

<span data-ttu-id="a12fc-345">基になるキャッシュ内のレコードがマークされているかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-345">Checks whether any records in the underlying cache are marked.</span></span>

```xpp
public boolean anyMarked()
```

### <a name="return-value---anymarked"></a><span data-ttu-id="a12fc-346">戻り値 - anyMarked</span><span class="sxs-lookup"><span data-stu-id="a12fc-346">Return Value - anyMarked</span></span>

<span data-ttu-id="a12fc-347">いずれかのレコードがマークされた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a12fc-347">true if any records are marked; otherwise, false.</span></span>

### <a name="remarks---anymarked"></a><span data-ttu-id="a12fc-348">備考 - anyMarked</span><span class="sxs-lookup"><span data-stu-id="a12fc-348">Remarks - anyMarked</span></span>

<span data-ttu-id="a12fc-349">データ ソース内のレコードは、削除などのアクションとしてマーク (選択) したり、FormDataSource.markedRecord メソッドを使用してコピーできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-349">Records in a data source can be marked (selected) for actions such as deletion or copying by using the FormDataSource.markedRecord method.</span></span>

## <a name="method-autonotify"></a><span data-ttu-id="a12fc-350">メソッド autoNotify</span><span class="sxs-lookup"><span data-stu-id="a12fc-350">Method autoNotify</span></span>

```xpp
public boolean autoNotify([boolean value])
```

### <a name="parameters---autonotify"></a><span data-ttu-id="a12fc-351">パラメーター - autoNotify</span><span class="sxs-lookup"><span data-stu-id="a12fc-351">Parameters - autoNotify</span></span>

<span data-ttu-id="a12fc-352">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-352">value</span></span>  

### <a name="return-value---autonotify"></a><span data-ttu-id="a12fc-353">戻り値 - autoNotify</span><span class="sxs-lookup"><span data-stu-id="a12fc-353">Return Value - autoNotify</span></span>

## <a name="method-autoquery"></a><span data-ttu-id="a12fc-354">メソッド autoQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-354">Method autoQuery</span></span>

```xpp
public boolean autoQuery([boolean value])
```

### <a name="parameters---autoquery"></a><span data-ttu-id="a12fc-355">パラメーター - autoQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-355">Parameters - autoQuery</span></span>

<span data-ttu-id="a12fc-356">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-356">value</span></span>  

### <a name="return-value---autoquery"></a><span data-ttu-id="a12fc-357">戻り値 - autoQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-357">Return Value - autoQuery</span></span>

## <a name="method-autosearch"></a><span data-ttu-id="a12fc-358">メソッド autoSearch</span><span class="sxs-lookup"><span data-stu-id="a12fc-358">Method autoSearch</span></span>

```xpp
public boolean autoSearch([boolean value])
```

### <a name="parameters---autosearch"></a><span data-ttu-id="a12fc-359">パラメーター - autoSearch</span><span class="sxs-lookup"><span data-stu-id="a12fc-359">Parameters - autoSearch</span></span>

<span data-ttu-id="a12fc-360">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-360">value</span></span>  

### <a name="return-value---autosearch"></a><span data-ttu-id="a12fc-361">戻り値 - autoSearch</span><span class="sxs-lookup"><span data-stu-id="a12fc-361">Return Value - autoSearch</span></span>

## <a name="method-bindfield"></a><span data-ttu-id="a12fc-362">メソッド bindField</span><span class="sxs-lookup"><span data-stu-id="a12fc-362">Method bindField</span></span>

```xpp
public str bindField(FieldId fieldId)
```

### <a name="parameters---bindfield"></a><span data-ttu-id="a12fc-363">パラメーター - bindField</span><span class="sxs-lookup"><span data-stu-id="a12fc-363">Parameters - bindField</span></span>

<span data-ttu-id="a12fc-364">fieldId</span><span class="sxs-lookup"><span data-stu-id="a12fc-364">fieldId</span></span>  

### <a name="return-value---bindfield"></a><span data-ttu-id="a12fc-365">戻り値 - bindField</span><span class="sxs-lookup"><span data-stu-id="a12fc-365">Return Value - bindField</span></span>

## <a name="method-binddatamethod"></a><span data-ttu-id="a12fc-366">メソッド bindDataMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-366">Method bindDataMethod</span></span>

```xpp
public str bindDataMethod(str dataMethodName)
```

### <a name="parameters---binddatamethod"></a><span data-ttu-id="a12fc-367">パラメーター - bindDataMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-367">Parameters - bindDataMethod</span></span>

<span data-ttu-id="a12fc-368">dataMethodName</span><span class="sxs-lookup"><span data-stu-id="a12fc-368">dataMethodName</span></span>  

### <a name="return-value---binddatamethod"></a><span data-ttu-id="a12fc-369">戻り値 - bindDataMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-369">Return Value - bindDataMethod</span></span>

## <a name="method-cacheaddmethod"></a><span data-ttu-id="a12fc-370">メソッド cacheAddMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-370">Method cacheAddMethod</span></span>

<span data-ttu-id="a12fc-371">キャッシュの指定された表示または編集方法を登録します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-371">Registers the specified display or edit method for caching.</span></span>

```xpp
public boolean cacheAddMethod(str methodName, [boolean updateOnWrite])
```

### <a name="parameters---cacheaddmethod"></a><span data-ttu-id="a12fc-372">パラメーター - cacheAddMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-372">Parameters - cacheAddMethod</span></span>

<span data-ttu-id="a12fc-373">methodName</span><span class="sxs-lookup"><span data-stu-id="a12fc-373">methodName</span></span>  
<span data-ttu-id="a12fc-374">レコードが書き込まれたときにキャッシュされた値が自動的に更新されるかどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a12fc-374">A Boolean value that determines whether the cached value is updated automatically when the record is written; optional.</span></span>

<!-- -->

<span data-ttu-id="a12fc-375">updateOnWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-375">updateOnWrite</span></span>  
<span data-ttu-id="a12fc-376">レコードが書き込まれたときにキャッシュされた値が自動的に更新されるかどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a12fc-376">A Boolean value that determines whether the cached value is updated automatically when the record is written; optional.</span></span>

### <a name="return-value---cacheaddmethod"></a><span data-ttu-id="a12fc-377">戻り値 - cacheAddMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-377">Return Value - cacheAddMethod</span></span>

<span data-ttu-id="a12fc-378">メソッドが正常に登録された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a12fc-378">true if the method was registered successfully; otherwise, false.</span></span>

### <a name="remarks---cacheaddmethod"></a><span data-ttu-id="a12fc-379">備考 - cacheAddMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-379">Remarks - cacheAddMethod</span></span>

<span data-ttu-id="a12fc-380">キャッシュされたメソッドはフェッチされたデータの計算を実行し、計算された値はデータと共にクライアントに渡されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-380">Cached methods perform calculations on fetched data, and then the calculated values are passed to the client together with the data.</span></span> <span data-ttu-id="a12fc-381">計算された値は再読み込み時に更新されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-381">The calculated values are updated on reread.</span></span> <span data-ttu-id="a12fc-382">既定では、値は書き込みおよび作成時にも更新されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-382">By default, the values are also update on write and create.</span></span> <span data-ttu-id="a12fc-383">このメソッドは、データ ソースの初期化後に、ただし、データがフェッチされる前に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-383">This method should be called after initialization of the data source, but before any data is fetched.</span></span> <span data-ttu-id="a12fc-384">したがって、このメソッドの呼び出しは、init メソッドの super メソッドを呼び出した後に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-384">Therefore, the call to this method should be put after the call to the super method in the init method.</span></span> <span data-ttu-id="a12fc-385">また、updateOnWrite パラメーターは、新しいレコードが作成されたときに表示メソッド値または編集メソッド値を計算してキャッシュするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-385">The updateOnWrite parameter also determines whether the display or edit method value should be calculated and cached when a new record is created.</span></span> <span data-ttu-id="a12fc-386">表示メソッドまたは編集メソッドのキャッシュされた値を手動で更新するには、FormDataSource.cacheCalculateMethod メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-386">To manually update the cached value for the display or edit method, call the FormDataSource.cacheCalculateMethod method.</span></span> <span data-ttu-id="a12fc-387">表示または編集キーワードを持つテーブル メソッドのみキャッシュされます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-387">Only table methods that have the display or edit keyword can be cached.</span></span> <span data-ttu-id="a12fc-388">フォームまたはフォーム データ ソースに記述されているメソッドをキャッシュすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a12fc-388">Methods that are written on the form or the form data source cannot be cached.</span></span> <span data-ttu-id="a12fc-389">表示を登録したり、フォームで使用されていないメソッドを編集しないでください。</span><span class="sxs-lookup"><span data-stu-id="a12fc-389">Do not register display or edit methods that are not used on the form.</span></span> <span data-ttu-id="a12fc-390">これらのメソッドは、値が表示されない場合でも、各レコードに対して計算が行われます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-390">Those methods are calculated for each record, even though the values are never shown.</span></span>

### <a name="examples---cacheaddmethod"></a><span data-ttu-id="a12fc-391">例 - cacheAddMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-391">Examples - cacheAddMethod</span></span>

<span data-ttu-id="a12fc-392">次の例では、VendTransOpen テーブルにキャッシュする 2 つのメソッドを登録します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-392">The following example registers two methods for caching on the VendTransOpen table.</span></span>

```xpp
public void init() 
{ 
    super(); 
    this.cacheAddMethod(tablemethodstr(VendTransOpen, 
        nextCashDiscDate)); 
    this.cacheAddMethod(tablemethodstr(VendTransOpen, 
        nextCashDiscAmount)); 
}
```

## <a name="method-cachecalculatemethod"></a><span data-ttu-id="a12fc-393">メソッド cacheCalculateMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-393">Method cacheCalculateMethod</span></span>

<span data-ttu-id="a12fc-394">指定されたキャッシュされたメソッドを呼び出し、現在のレコードのキャッシュ内の値を更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-394">Calls the specified cached method and updates the value in the cache for the current record.</span></span>

```xpp
public boolean cacheCalculateMethod(str methodName)
```

### <a name="parameters---cachecalculatemethod"></a><span data-ttu-id="a12fc-395">パラメーター - cacheCalculateMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-395">Parameters - cacheCalculateMethod</span></span>

<span data-ttu-id="a12fc-396">methodName</span><span class="sxs-lookup"><span data-stu-id="a12fc-396">methodName</span></span>  
<span data-ttu-id="a12fc-397">呼び出すテーブル メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="a12fc-397">The name of the table method to call.</span></span>

### <a name="return-value---cachecalculatemethod"></a><span data-ttu-id="a12fc-398">戻り値 - cacheCalculateMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-398">Return Value - cacheCalculateMethod</span></span>

<span data-ttu-id="a12fc-399">値が更新された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a12fc-399">true if the value has been updated; otherwise, false.</span></span>

### <a name="remarks---cachecalculatemethod"></a><span data-ttu-id="a12fc-400">備考 - cacheCalculateMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-400">Remarks - cacheCalculateMethod</span></span>

<span data-ttu-id="a12fc-401">キャッシュされた値は、指定されたメソッド名が FormDataSource.cacheAddMethod method メソッドを使用してキャッシュされたメソッドとして以前に登録されている場合にのみ更新されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-401">The cached value is updated only if the method name that was supplied was previously registered as a cached method by using the FormDataSource.cacheAddMethod method.</span></span> <span data-ttu-id="a12fc-402">cacheCalculate メソッドは、特定の条件が満たされたときにのみキャッシュされた値を更新する場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="a12fc-402">The cacheCalculate method is particularly useful if you want to update cached values only when certain conditions are met.</span></span> <span data-ttu-id="a12fc-403">この場合、FormDataSource.cacheAddMethod メソッドの呼び出しで updateOnWrite パラメーターを false に設定し、データ ソースで書き込みメソッドを使用するなど手動でキャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-403">In this case, set the updateOnWrite parameter in the call to the FormDataSource.cacheAddMethod method to false, and then manually update the cache, such as by using the write method on the data source.</span></span>

### <a name="examples---cachecalculatemethod"></a><span data-ttu-id="a12fc-404">例 - cacheCalculateMethod</span><span class="sxs-lookup"><span data-stu-id="a12fc-404">Examples - cacheCalculateMethod</span></span>

<span data-ttu-id="a12fc-405">次の例では、VendTransOpen テーブルの nextCashDiscDate メソッドと nextCashDiscAmount メソッドを使用して、キャッシュされた値を再計算します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-405">The following example recalculates cached values by using the nextCashDiscDate method and the nextCashDiscAmount method, both in the VendTransOpen table.</span></span>

```xpp
public void write() 
{ 
    super(); 
    vendTransOpen_ds.cacheCalculateMethod(tablemethodstr( 
        VendTransOpen, nextCashDiscDate)); 
    vendTransOpen_ds.cacheCalculateMethod(tablemethodstr( 
        VendTransOpen, nextCashDiscAmount)); 
}
```

## <a name="method-cacheonlymode"></a><span data-ttu-id="a12fc-406">メソッド cacheOnlyMode</span><span class="sxs-lookup"><span data-stu-id="a12fc-406">Method cacheOnlyMode</span></span>

```xpp
public boolean cacheOnlyMode([boolean value])
```

### <a name="parameters---cacheonlymode"></a><span data-ttu-id="a12fc-407">パラメーター - cacheOnlyMode</span><span class="sxs-lookup"><span data-stu-id="a12fc-407">Parameters - cacheOnlyMode</span></span>

<span data-ttu-id="a12fc-408">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-408">value</span></span>  

### <a name="return-value---cacheonlymode"></a><span data-ttu-id="a12fc-409">戻り値 - cacheOnlyMode</span><span class="sxs-lookup"><span data-stu-id="a12fc-409">Return Value - cacheOnlyMode</span></span>

## <a name="method-cancreate"></a><span data-ttu-id="a12fc-410">メソッド canCreate</span><span class="sxs-lookup"><span data-stu-id="a12fc-410">Method canCreate</span></span>

```xpp
public boolean canCreate()
```

### <a name="return-value---cancreate"></a><span data-ttu-id="a12fc-411">戻り値 - canCreate</span><span class="sxs-lookup"><span data-stu-id="a12fc-411">Return Value - canCreate</span></span>

## <a name="method-candelete"></a><span data-ttu-id="a12fc-412">メソッド canDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-412">Method canDelete</span></span>

```xpp
public boolean canDelete()
```

### <a name="return-value---candelete"></a><span data-ttu-id="a12fc-413">戻り値 - canDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-413">Return Value - canDelete</span></span>

## <a name="method-canedit"></a><span data-ttu-id="a12fc-414">メソッド canEdit</span><span class="sxs-lookup"><span data-stu-id="a12fc-414">Method canEdit</span></span>

```xpp
public boolean canEdit()
```

### <a name="return-value---canedit"></a><span data-ttu-id="a12fc-415">戻り値 - canEdit</span><span class="sxs-lookup"><span data-stu-id="a12fc-415">Return Value - canEdit</span></span>

## <a name="method-clientpagesize"></a><span data-ttu-id="a12fc-416">メソッド clientPageSize</span><span class="sxs-lookup"><span data-stu-id="a12fc-416">Method clientPageSize</span></span>

```xpp
public int clientPageSize([int pageSize])
```

### <a name="parameters---clientpagesize"></a><span data-ttu-id="a12fc-417">パラメーター - clientPageSize</span><span class="sxs-lookup"><span data-stu-id="a12fc-417">Parameters - clientPageSize</span></span>

<span data-ttu-id="a12fc-418">pageSize</span><span class="sxs-lookup"><span data-stu-id="a12fc-418">pageSize</span></span>  

### <a name="return-value---clientpagesize"></a><span data-ttu-id="a12fc-419">戻り値 - clientPageSize</span><span class="sxs-lookup"><span data-stu-id="a12fc-419">Return Value - clientPageSize</span></span>

## <a name="method-company"></a><span data-ttu-id="a12fc-420">メソッド company</span><span class="sxs-lookup"><span data-stu-id="a12fc-420">Method company</span></span>

```xpp
public str company([str value])
```

### <a name="parameters---company"></a><span data-ttu-id="a12fc-421">パラメーター - company</span><span class="sxs-lookup"><span data-stu-id="a12fc-421">Parameters - company</span></span>

<span data-ttu-id="a12fc-422">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-422">value</span></span>  

### <a name="return-value---company"></a><span data-ttu-id="a12fc-423">戻り値 - company</span><span class="sxs-lookup"><span data-stu-id="a12fc-423">Return Value - company</span></span>

## <a name="method-counterfield"></a><span data-ttu-id="a12fc-424">メソッド counterField</span><span class="sxs-lookup"><span data-stu-id="a12fc-424">Method counterField</span></span>

```xpp
public FieldId counterField([FieldId value])
```

### <a name="parameters---counterfield"></a><span data-ttu-id="a12fc-425">パラメーター - counterField</span><span class="sxs-lookup"><span data-stu-id="a12fc-425">Parameters - counterField</span></span>

<span data-ttu-id="a12fc-426">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-426">value</span></span>  

### <a name="return-value---counterfield"></a><span data-ttu-id="a12fc-427">戻り値 - counterField</span><span class="sxs-lookup"><span data-stu-id="a12fc-427">Return Value - counterField</span></span>

## <a name="method-crosscompanyautoquery"></a><span data-ttu-id="a12fc-428">メソッド crossCompanyAutoQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-428">Method crossCompanyAutoQuery</span></span>

```xpp
public boolean crossCompanyAutoQuery([boolean value])
```

### <a name="parameters---crosscompanyautoquery"></a><span data-ttu-id="a12fc-429">パラメーター - crossCompanyAutoQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-429">Parameters - crossCompanyAutoQuery</span></span>

<span data-ttu-id="a12fc-430">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-430">value</span></span>  

### <a name="return-value---crosscompanyautoquery"></a><span data-ttu-id="a12fc-431">戻り値 - crossCompanyAutoQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-431">Return Value - crossCompanyAutoQuery</span></span>

## <a name="method-cursor"></a><span data-ttu-id="a12fc-432">メソッド cursor</span><span class="sxs-lookup"><span data-stu-id="a12fc-432">Method cursor</span></span>

<span data-ttu-id="a12fc-433">FormObjectSet クラスには機能がありません。</span><span class="sxs-lookup"><span data-stu-id="a12fc-433">Has no functionality in the FormObjectSet class.</span></span>

```xpp
public Common cursor([int rowIndex])
```

### <a name="parameters---cursor"></a><span data-ttu-id="a12fc-434">パラメーター - cursor</span><span class="sxs-lookup"><span data-stu-id="a12fc-434">Parameters - cursor</span></span>

<span data-ttu-id="a12fc-435">rowIndex</span><span class="sxs-lookup"><span data-stu-id="a12fc-435">rowIndex</span></span>  

### <a name="return-value---cursor"></a><span data-ttu-id="a12fc-436">戻り値 - cursor</span><span class="sxs-lookup"><span data-stu-id="a12fc-436">Return Value - cursor</span></span>

### <a name="remarks---cursor"></a><span data-ttu-id="a12fc-437">備考 - cursor</span><span class="sxs-lookup"><span data-stu-id="a12fc-437">Remarks - cursor</span></span>

<span data-ttu-id="a12fc-438">このメソッドは、データソースによって参照されるテーブル内の現在アクティブなレコードを返す FormDataSource.cursor メソッドによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-438">This method is overridden by the FormDataSource.cursor method, which returns the currently active record in the table that is referenced by the data source.</span></span>

## <a name="method-defaultmark"></a><span data-ttu-id="a12fc-439">メソッド defaultMark</span><span class="sxs-lookup"><span data-stu-id="a12fc-439">Method defaultMark</span></span>

<span data-ttu-id="a12fc-440">グリッドで選択されたときにレコードがマークされるかどうかを決定する、フォーム内のレコードの既定のマーク値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-440">Sets the default mark value for records in a form, which determines whether records are marked when they have been selected in a grid.</span></span>

```xpp
public int defaultMark([int value])
```

### <a name="parameters---defaultmark"></a><span data-ttu-id="a12fc-441">パラメーター - defaultMark</span><span class="sxs-lookup"><span data-stu-id="a12fc-441">Parameters - defaultMark</span></span>

<span data-ttu-id="a12fc-442">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-442">value</span></span>  
<span data-ttu-id="a12fc-443">フォーム内のレコードの既定のマーク値。</span><span class="sxs-lookup"><span data-stu-id="a12fc-443">The default mark value for records in the form.</span></span> <span data-ttu-id="a12fc-444">レコードの標準デフォルト マーク値は 1 ですが、この値は value パラメーターを設定することで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-444">The standard default mark value for records is 1, but this value can be overridden by setting the value parameter.</span></span> <span data-ttu-id="a12fc-445">0 (ゼロ) 以外の値は、選択されたときにフォームのグリッドでマークされてレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-445">A value other than 0 (zero) causes the record to be displayed as marked in grids in the form when they have been selected.</span></span>

### <a name="return-value---defaultmark"></a><span data-ttu-id="a12fc-446">戻り値 - defaultMark</span><span class="sxs-lookup"><span data-stu-id="a12fc-446">Return Value - defaultMark</span></span>

<span data-ttu-id="a12fc-447">フォーム内のレコードの既定のマーク値。</span><span class="sxs-lookup"><span data-stu-id="a12fc-447">The default mark value for records in the form.</span></span>

### <a name="remarks---defaultmark"></a><span data-ttu-id="a12fc-448">備考 - defaultMark</span><span class="sxs-lookup"><span data-stu-id="a12fc-448">Remarks - defaultMark</span></span>

<span data-ttu-id="a12fc-449">このメソッドは、グリッド内のすべてのレコードを選択するためにグリッド コントロールの左上隅をクリックすると実行されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-449">This method is executed when a user clicks the top-left corner in a grid control to select all the records in the grid.</span></span> <span data-ttu-id="a12fc-450">defaultMark メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-450">The defaultMark method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-451">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] &gt; [defaultMark] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-451">Right-click the Methods node under the data source, and then select Override Method &gt; defaultMark.</span></span>

## <a name="method-delayactive"></a><span data-ttu-id="a12fc-452">メソッド delayActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-452">Method delayActive</span></span>

```xpp
public boolean delayActive([boolean value])
```

### <a name="parameters---delayactive"></a><span data-ttu-id="a12fc-453">パラメーター - delayActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-453">Parameters - delayActive</span></span>

<span data-ttu-id="a12fc-454">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-454">value</span></span>  

### <a name="return-value---delayactive"></a><span data-ttu-id="a12fc-455">戻り値 - delayActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-455">Return Value - delayActive</span></span>

## <a name="method-extends"></a><span data-ttu-id="a12fc-456">メソッド extends</span><span class="sxs-lookup"><span data-stu-id="a12fc-456">Method extends</span></span>

```xpp
public int extends([AnyType value])
```

### <a name="parameters---extends"></a><span data-ttu-id="a12fc-457">パラメーター - extends</span><span class="sxs-lookup"><span data-stu-id="a12fc-457">Parameters - extends</span></span>

<span data-ttu-id="a12fc-458">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-458">value</span></span>  

### <a name="return-value---extends"></a><span data-ttu-id="a12fc-459">戻り値 - extends</span><span class="sxs-lookup"><span data-stu-id="a12fc-459">Return Value - extends</span></span>

## <a name="method-findrecord"></a><span data-ttu-id="a12fc-460">メソッド findRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-460">Method findRecord</span></span>

<span data-ttu-id="a12fc-461">データ ソースで指定されたレコードを検索し、それが現在のレコードになります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-461">Finds the specified record in the data source and makes it the current record.</span></span>

```xpp
public boolean findRecord(Common record)
```

### <a name="parameters---findrecord"></a><span data-ttu-id="a12fc-462">パラメーター - findRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-462">Parameters - findRecord</span></span>

<span data-ttu-id="a12fc-463">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-463">record</span></span>  
<span data-ttu-id="a12fc-464">検索するレコード。</span><span class="sxs-lookup"><span data-stu-id="a12fc-464">The record to find.</span></span>

### <a name="return-value---findrecord"></a><span data-ttu-id="a12fc-465">戻り値 - findRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-465">Return Value - findRecord</span></span>

<span data-ttu-id="a12fc-466">レコードが見つかった場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a12fc-466">true if the record was found; otherwise, false.</span></span>

### <a name="remarks---findrecord"></a><span data-ttu-id="a12fc-467">備考 - findRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-467">Remarks - findRecord</span></span>

<span data-ttu-id="a12fc-468">このメソッドは、FormDataSource.findValue メソッド が呼び出されたときにアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-468">This method is activated when the FormDataSource.findValue method is called.</span></span> <span data-ttu-id="a12fc-469">findRecord メソッドは、データソースの下にある [メソッド ノード] を右クリックし、[メソッドの上書き] をポイントしてから、[findRecord] をクリックして、フォーム データ ソース上で上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-469">The findRecord method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking findRecord.</span></span>

## <a name="method-findvalue"></a><span data-ttu-id="a12fc-470">メソッド findValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-470">Method findValue</span></span>

<span data-ttu-id="a12fc-471">データ ソースで指定された値を検索し、そのレコードが FormDataSource.findRecord メソッドを使用する現在のレコードの値を持つようにします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-471">Finds the specified value in the data source and makes the record that has that value the current record that uses the FormDataSource.findRecord method.</span></span>

```xpp
public boolean findValue(FieldId field, str value)
```

### <a name="parameters---findvalue"></a><span data-ttu-id="a12fc-472">パラメーター - findValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-472">Parameters - findValue</span></span>

<span data-ttu-id="a12fc-473"> フィールド</span><span class="sxs-lookup"><span data-stu-id="a12fc-473">field</span></span>  
<span data-ttu-id="a12fc-474">検索する値。</span><span class="sxs-lookup"><span data-stu-id="a12fc-474">The value to find.</span></span>

<!-- -->

<span data-ttu-id="a12fc-475">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-475">value</span></span>  
<span data-ttu-id="a12fc-476">検索する値。</span><span class="sxs-lookup"><span data-stu-id="a12fc-476">The value to find.</span></span>

### <a name="return-value---findvalue"></a><span data-ttu-id="a12fc-477">戻り値 - findValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-477">Return Value - findValue</span></span>

<span data-ttu-id="a12fc-478">値が見つかった場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a12fc-478">true if the value is found; otherwise, false.</span></span>

### <a name="remarks---findvalue"></a><span data-ttu-id="a12fc-479">備考 - findValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-479">Remarks - findValue</span></span>

<span data-ttu-id="a12fc-480">このメソッドは、ユーザーがフォーム コントロールのショートカット メニューで FindValue をクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-480">This method is called when a user clicks FindValue in the shortcut menu on a form control.</span></span> <span data-ttu-id="a12fc-481">findValue メソッドは、データソースの下にある [メソッド ノード] を右クリックし、[メソッドの上書き] をポイントしてから、[findValue] をクリックして、フォーム データ ソース上で上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-481">The findValue method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking findValue.</span></span>

### <a name="examples---findvalue"></a><span data-ttu-id="a12fc-482">例 - findValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-482">Examples - findValue</span></span>

<span data-ttu-id="a12fc-483">次の例では、データを変更する前に現在のレコードの ID を格納しています。</span><span class="sxs-lookup"><span data-stu-id="a12fc-483">The following example stores the ID of the current record before it tries to modify data.</span></span> <span data-ttu-id="a12fc-484">更新に失敗した場合、データ ソースは、元のレコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-484">If the update fails, the data source is positioned on the original record.</span></span>

```xpp
void clicked() 
{ 
    DocuTypeId  docuTypeId; 
    RecId       activeRecId; 
    ; 
     // Store current RecID 
    activeRecId = docuRef.RecId;  
    // Open the Document Type dialog. 
    docuTypeId = smmDocuments::getDocuTypeId(element.args().record()); 
    try 
    { 
        ttsbegin; 
        if (docuTypeId) 
        { 
            // Create a new document record 
            docuRef_ds.create(); 
            docuRef.RefTableId      = tableReference; 
            docuRef.RefRecId        = recReference; 
            docuRef_ds.write(); 
            super(); 
        } 
        ttscommit; 
    } 
    catch 
    { 
        // Focus moved back to original record if there is an error 
        docuRef_ds.executeQuery(); 
        docuRef_ds.findValue(fieldnum(DocuRef,RecId), 
            int642str(activeRecId)); 
    } 
}
```

## <a name="method-positiontorecord"></a><span data-ttu-id="a12fc-485">メソッド positionToRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-485">Method positionToRecord</span></span>

```xpp
public boolean positionToRecord(Common record)
```

### <a name="parameters---positiontorecord"></a><span data-ttu-id="a12fc-486">パラメーター - positionToRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-486">Parameters - positionToRecord</span></span>

<span data-ttu-id="a12fc-487">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-487">record</span></span>  

### <a name="return-value---positiontorecord"></a><span data-ttu-id="a12fc-488">戻り値 - positionToRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-488">Return Value - positionToRecord</span></span>

## <a name="method-positiontorecordbyvalue"></a><span data-ttu-id="a12fc-489">メソッド positionToRecordByValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-489">Method positionToRecordByValue</span></span>

```xpp
public boolean positionToRecordByValue(FieldId field, str value)
```

### <a name="parameters---positiontorecordbyvalue"></a><span data-ttu-id="a12fc-490">パラメーター - positionToRecordByValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-490">Parameters - positionToRecordByValue</span></span>

<span data-ttu-id="a12fc-491"> フィールド</span><span class="sxs-lookup"><span data-stu-id="a12fc-491">field</span></span>  

<!-- -->

<span data-ttu-id="a12fc-492">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-492">value</span></span>  

### <a name="return-value---positiontorecordbyvalue"></a><span data-ttu-id="a12fc-493">戻り値 - positionToRecordByValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-493">Return Value - positionToRecordByValue</span></span>

## <a name="method-first"></a><span data-ttu-id="a12fc-494">メソッド first</span><span class="sxs-lookup"><span data-stu-id="a12fc-494">Method first</span></span>

<span data-ttu-id="a12fc-495">データ ソースの最初のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-495">Moves focus to the first record in the data source.</span></span>

```xpp
public int first()
```

### <a name="return-value---first"></a><span data-ttu-id="a12fc-496">戻り値 - first</span><span class="sxs-lookup"><span data-stu-id="a12fc-496">Return Value - first</span></span>

<span data-ttu-id="a12fc-497">フォーカスが最初のレコードに正常に移動した場合は、ゼロ以外の値。</span><span class="sxs-lookup"><span data-stu-id="a12fc-497">A non-zero value if focus is successfully moved to the first record.</span></span>

### <a name="remarks---first"></a><span data-ttu-id="a12fc-498">備考 - first</span><span class="sxs-lookup"><span data-stu-id="a12fc-498">Remarks - first</span></span>

<span data-ttu-id="a12fc-499">このメソッドは、ユーザーが CTRL+HOME キーを押してフォームの最初のレコードを選択するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-499">This method is called when a user selects the first record in a form by pressing CTRL+HOME.</span></span> <span data-ttu-id="a12fc-500">最初のメソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-500">The first method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-501">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [first] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-501">Right-click the Methods node under the data source, point to Override Method, and then click first.</span></span>

### <a name="examples---first"></a><span data-ttu-id="a12fc-502">例 - first</span><span class="sxs-lookup"><span data-stu-id="a12fc-502">Examples - first</span></span>

<span data-ttu-id="a12fc-503">次の例では、InventTrans フォームの InventTransPostingFinancial データソースの最初のメソッドを上書きし、そのフォームで使用されている別のデータ ソースの最後のレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-503">The following example overrides the first method for the InventTransPostingFinancial data source on the InventTrans form and returns the last record in another data source that is used on the form.</span></span>

```xpp
int first() 
{ 
    return inventTrans_ds.first(); 
}
```

## <a name="method-forcewrite"></a><span data-ttu-id="a12fc-504">メソッド forceWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-504">Method forceWrite</span></span>

```xpp
public boolean forceWrite([boolean value])
```

### <a name="parameters---forcewrite"></a><span data-ttu-id="a12fc-505">パラメーター - forceWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-505">Parameters - forceWrite</span></span>

<span data-ttu-id="a12fc-506">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-506">value</span></span>  

### <a name="return-value---forcewrite"></a><span data-ttu-id="a12fc-507">戻り値 - forceWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-507">Return Value - forceWrite</span></span>

## <a name="method-functionobject"></a><span data-ttu-id="a12fc-508">メソッド functionObject</span><span class="sxs-lookup"><span data-stu-id="a12fc-508">Method functionObject</span></span>

```xpp
public FormObject functionObject(str name)
```

### <a name="parameters---functionobject"></a><span data-ttu-id="a12fc-509">パラメーター - functionObject</span><span class="sxs-lookup"><span data-stu-id="a12fc-509">Parameters - functionObject</span></span>

<span data-ttu-id="a12fc-510">名前</span><span class="sxs-lookup"><span data-stu-id="a12fc-510">name</span></span>  

### <a name="return-value---functionobject"></a><span data-ttu-id="a12fc-511">戻り値 - functionObject</span><span class="sxs-lookup"><span data-stu-id="a12fc-511">Return Value - functionObject</span></span>

## <a name="method-getdatarow"></a><span data-ttu-id="a12fc-512">メソッド getDataRow</span><span class="sxs-lookup"><span data-stu-id="a12fc-512">Method getDataRow</span></span>

```xpp
public FormDataRow getDataRow([int rowIndex], [boolean allowFetchAhead])
```

### <a name="parameters---getdatarow"></a><span data-ttu-id="a12fc-513">パラメーター - getDataRow</span><span class="sxs-lookup"><span data-stu-id="a12fc-513">Parameters - getDataRow</span></span>

<span data-ttu-id="a12fc-514">rowIndex</span><span class="sxs-lookup"><span data-stu-id="a12fc-514">rowIndex</span></span>  

<!-- -->

<span data-ttu-id="a12fc-515">allowFetchAhead</span><span class="sxs-lookup"><span data-stu-id="a12fc-515">allowFetchAhead</span></span>  

### <a name="return-value---getdatarow"></a><span data-ttu-id="a12fc-516">戻り値 - getDataRow</span><span class="sxs-lookup"><span data-stu-id="a12fc-516">Return Value - getDataRow</span></span>

## <a name="method-getfirst"></a><span data-ttu-id="a12fc-517">メソッド getFirst</span><span class="sxs-lookup"><span data-stu-id="a12fc-517">Method getFirst</span></span>

<span data-ttu-id="a12fc-518">データ セットの最初のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-518">Retrieves the first record in a data set.</span></span>

```xpp
public Common getFirst([int mark], [boolean fetchAhead])
```

### <a name="parameters---getfirst"></a><span data-ttu-id="a12fc-519">パラメーター - getFirst</span><span class="sxs-lookup"><span data-stu-id="a12fc-519">Parameters - getFirst</span></span>

<span data-ttu-id="a12fc-520">mark</span><span class="sxs-lookup"><span data-stu-id="a12fc-520">mark</span></span>  
<span data-ttu-id="a12fc-521">ブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a12fc-521">A Boolean value; optional.</span></span> <span data-ttu-id="a12fc-522">既定値は true です。</span><span class="sxs-lookup"><span data-stu-id="a12fc-522">The default value is true.</span></span>

<!-- -->

<span data-ttu-id="a12fc-523">fetchAhead</span><span class="sxs-lookup"><span data-stu-id="a12fc-523">fetchAhead</span></span>  
<span data-ttu-id="a12fc-524">ブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="a12fc-524">A Boolean value; optional.</span></span> <span data-ttu-id="a12fc-525">既定値は true です。</span><span class="sxs-lookup"><span data-stu-id="a12fc-525">The default value is true.</span></span>

### <a name="return-value---getfirst"></a><span data-ttu-id="a12fc-526">戻り値 - getFirst</span><span class="sxs-lookup"><span data-stu-id="a12fc-526">Return Value - getFirst</span></span>

<span data-ttu-id="a12fc-527">データ セットの最初のレコード。</span><span class="sxs-lookup"><span data-stu-id="a12fc-527">The first record in the data set.</span></span>

### <a name="remarks---getfirst"></a><span data-ttu-id="a12fc-528">備考 - getFirst</span><span class="sxs-lookup"><span data-stu-id="a12fc-528">Remarks - getFirst</span></span>

<span data-ttu-id="a12fc-529">マーク パラメーターがない 0 (ゼロ) の場合、指定した値がマークされている最初のレコードが返され、その後 FormDataSource.getNext メソッドを呼び出すと、マークされたレコードが返されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-529">If the mark parameter is not 0 (zero), the first record that is marked with the specified value is returned, and subsequent calls to the FormDataSource.getNext method return marked records.</span></span> <span data-ttu-id="a12fc-530">FetchAhead パラメーターが false に設定されている場合は、キャッシュされているレコードだけが返されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-530">If the fetchAhead parameter is set to false, only cached records are returned.</span></span> <span data-ttu-id="a12fc-531">true に設定され、追加のレコードが検出され、それがキャッシュに追加される場合は、大量のレコード セットで実行される時に、工程に非常に時間がかかる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-531">If it is set to true, additional records are found and added to the cache, but the operation can become very time-consuming when it is performed on a large record set.</span></span> <span data-ttu-id="a12fc-532">1 つのグリッド内のレコードが複数選択されると、それらのレコードに値 1 がマークされます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-532">When records in a grid are multiselected, the records are marked with the value 1.</span></span> <span data-ttu-id="a12fc-533">次の例は、マーク付きレコードまたはマークなしレコードを取得する方法を示しています。 // 最初に取得する recordformDataSource.getFirst();// 2formDataSource.getFirst(2); とマークされた最初に取得するレコード // 1formDataSource.getFirst(1, false); とマークされた最初にキャッシュされたレコード</span><span class="sxs-lookup"><span data-stu-id="a12fc-533">The following examples illustrate how to retrieve a marked or unmarked record: // Get first recordformDataSource.getFirst();// Get first record marked with 2formDataSource.getFirst(2); // Get first cached record marked with 1formDataSource.getFirst(1, false);</span></span>

### <a name="examples---getfirst"></a><span data-ttu-id="a12fc-534">例 - getFirst</span><span class="sxs-lookup"><span data-stu-id="a12fc-534">Examples - getFirst</span></span>

<span data-ttu-id="a12fc-535">次の例では、フォーム内で 2 つのレコードが選択されているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-535">The following example determines whether two records are selected in a form.</span></span>

```xpp
boolean twoMarked() 
{ 
    SysVersionControlTmpItem tmpitem  = this.getFirst(1); 
    if (!tmpitem) 
    { 
        return false; 
    } 
    tmpitem = this.getNext(); 
    if (!tmpitem) 
    { 
        return false; 
    } 
    tmpitem = this.getNext(); 
    if (!tmpitem) 
    { 
        return true; 
    } 
    return false; 
}
```

## <a name="method-getnext"></a><span data-ttu-id="a12fc-536">メソッド getNext</span><span class="sxs-lookup"><span data-stu-id="a12fc-536">Method getNext</span></span>

<span data-ttu-id="a12fc-537">FormDataSource.getFirst メソッドへの以前の呼び出しで設定されている条件に合う次のレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-537">Returns the next record that meets the criteria that are set up in an earlier call to the FormDataSource.getFirst method.</span></span>

```xpp
public Common getNext()
```

### <a name="return-value---getnext"></a><span data-ttu-id="a12fc-538">戻り値 - getNext</span><span class="sxs-lookup"><span data-stu-id="a12fc-538">Return Value - getNext</span></span>

<span data-ttu-id="a12fc-539">データセットの次のレコード。</span><span class="sxs-lookup"><span data-stu-id="a12fc-539">The next record in the dataset.</span></span>

### <a name="remarks---getnext"></a><span data-ttu-id="a12fc-540">備考 - getNext</span><span class="sxs-lookup"><span data-stu-id="a12fc-540">Remarks - getNext</span></span>

<span data-ttu-id="a12fc-541">FormDataSource.getFirst メソッドの呼び出しで実行される初期化によって、getNext メソッドは特定のマーク値を持つレコードのみを返し、キャッシュからレコードを返すことがあります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-541">Depending on the initialization that is performed in the call to the FormDataSource.getFirst method, the getNext method might return only records that have a particular mark value, and it might return records from the cache.</span></span>

### <a name="examples---getnext"></a><span data-ttu-id="a12fc-542">例 - getNext</span><span class="sxs-lookup"><span data-stu-id="a12fc-542">Examples - getNext</span></span>

<span data-ttu-id="a12fc-543">次の例では、フォーム内で 2 つのレコードが選択されているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-543">The following example determines whether two records are selected in a form.</span></span>

```xpp
boolean twoMarked() 
{ 
    SysVersionControlTmpItem tmpitem  = this.getFirst(1); 
    if (!tmpitem) 
    { 
        return false; 
    } 
    tmpitem = this.getNext(); 
    if (!tmpitem) 
    { 
        return false; 
    } 
    tmpitem = this.getNext(); 
    if (!tmpitem) 
    { 
        return true; 
    } 
    return false; 
}
```

## <a name="method-id"></a><span data-ttu-id="a12fc-544">メソッド id</span><span class="sxs-lookup"><span data-stu-id="a12fc-544">Method id</span></span>

<span data-ttu-id="a12fc-545">データ ソースの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-545">Retrieves the ID of the data source.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="a12fc-546">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="a12fc-546">Return Value - id</span></span>

<span data-ttu-id="a12fc-547">データ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="a12fc-547">The ID of the data source.</span></span>

### <a name="examples---id"></a><span data-ttu-id="a12fc-548">例 - id</span><span class="sxs-lookup"><span data-stu-id="a12fc-548">Examples - id</span></span>

<span data-ttu-id="a12fc-549">次の例では、フォーム データ ソースをデータ ソース ID に変換します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-549">The following example converts form data sources to their data source IDs.</span></span>

```xpp
static client DataSourceNumber fds2fdsNo(FormDataSource _fds) 
{ 
    Form  form = _fds.formRun().form(); 
    int   i; 
    for (i=1;i<=form.dataSourceCount();i++) 
    { 
        if (_fds.formRun().dataSource(i).id() == _fds.id()) 
        { 
            return i; 
        } 
    } 
    return 0; 
}
```

## <a name="method-index"></a><span data-ttu-id="a12fc-550">メソッド index</span><span class="sxs-lookup"><span data-stu-id="a12fc-550">Method index</span></span>

```xpp
public IndexId index([IndexId value])
```

### <a name="parameters---index"></a><span data-ttu-id="a12fc-551">パラメーター - index</span><span class="sxs-lookup"><span data-stu-id="a12fc-551">Parameters - index</span></span>

<span data-ttu-id="a12fc-552">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-552">value</span></span>  

### <a name="return-value---index"></a><span data-ttu-id="a12fc-553">戻り値 - index</span><span class="sxs-lookup"><span data-stu-id="a12fc-553">Return Value - index</span></span>

## <a name="method-insertatend"></a><span data-ttu-id="a12fc-554">メソッド insertAtEnd</span><span class="sxs-lookup"><span data-stu-id="a12fc-554">Method insertAtEnd</span></span>

```xpp
public boolean insertAtEnd([boolean value])
```

### <a name="parameters---insertatend"></a><span data-ttu-id="a12fc-555">パラメーター - insertAtEnd</span><span class="sxs-lookup"><span data-stu-id="a12fc-555">Parameters - insertAtEnd</span></span>

<span data-ttu-id="a12fc-556">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-556">value</span></span>  

### <a name="return-value---insertatend"></a><span data-ttu-id="a12fc-557">戻り値 - insertAtEnd</span><span class="sxs-lookup"><span data-stu-id="a12fc-557">Return Value - insertAtEnd</span></span>

## <a name="method-insertifempty"></a><span data-ttu-id="a12fc-558">メソッド insertIfEmpty</span><span class="sxs-lookup"><span data-stu-id="a12fc-558">Method insertIfEmpty</span></span>

```xpp
public boolean insertIfEmpty([boolean value])
```

### <a name="parameters---insertifempty"></a><span data-ttu-id="a12fc-559">パラメーター - insertIfEmpty</span><span class="sxs-lookup"><span data-stu-id="a12fc-559">Parameters - insertIfEmpty</span></span>

<span data-ttu-id="a12fc-560">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-560">value</span></span>  

### <a name="return-value---insertifempty"></a><span data-ttu-id="a12fc-561">戻り値 - insertIfEmpty</span><span class="sxs-lookup"><span data-stu-id="a12fc-561">Return Value - insertIfEmpty</span></span>

## <a name="method-isbasedatasource"></a><span data-ttu-id="a12fc-562">メソッド isBaseDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-562">Method isBaseDataSource</span></span>

```xpp
public boolean isBaseDataSource()
```

### <a name="return-value---isbasedatasource"></a><span data-ttu-id="a12fc-563">戻り値 - isBaseDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-563">Return Value - isBaseDataSource</span></span>

## <a name="method-isinheritancedatasource"></a><span data-ttu-id="a12fc-564">メソッド isInheritanceDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-564">Method isInheritanceDataSource</span></span>

```xpp
public boolean isInheritanceDataSource()
```

### <a name="return-value---isinheritancedatasource"></a><span data-ttu-id="a12fc-565">戻り値 - isInheritanceDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-565">Return Value - isInheritanceDataSource</span></span>

## <a name="method-isoptionalrecordcreated"></a><span data-ttu-id="a12fc-566">メソッド isOptionalRecordCreated</span><span class="sxs-lookup"><span data-stu-id="a12fc-566">Method isOptionalRecordCreated</span></span>

```xpp
private boolean isOptionalRecordCreated([boolean set], Common record, [boolean value])
```

### <a name="parameters---isoptionalrecordcreated"></a><span data-ttu-id="a12fc-567">パラメーター - isOptionalRecordCreated</span><span class="sxs-lookup"><span data-stu-id="a12fc-567">Parameters - isOptionalRecordCreated</span></span>

<span data-ttu-id="a12fc-568">set</span><span class="sxs-lookup"><span data-stu-id="a12fc-568">set</span></span>  

<!-- -->

<span data-ttu-id="a12fc-569">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-569">record</span></span>  

<!-- -->

<span data-ttu-id="a12fc-570">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-570">value</span></span>  

### <a name="return-value---isoptionalrecordcreated"></a><span data-ttu-id="a12fc-571">戻り値 - isOptionalRecordCreated</span><span class="sxs-lookup"><span data-stu-id="a12fc-571">Return Value - isOptionalRecordCreated</span></span>

## <a name="method-isreferencedatasource"></a><span data-ttu-id="a12fc-572">メソッド isReferenceDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-572">Method isReferenceDataSource</span></span>

```xpp
public boolean isReferenceDataSource()
```

### <a name="return-value---isreferencedatasource"></a><span data-ttu-id="a12fc-573">戻り値 - isReferenceDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-573">Return Value - isReferenceDataSource</span></span>

## <a name="method-joinrelation"></a><span data-ttu-id="a12fc-574">メソッド joinRelation</span><span class="sxs-lookup"><span data-stu-id="a12fc-574">Method joinRelation</span></span>

```xpp
public str joinRelation([str value])
```

### <a name="parameters---joinrelation"></a><span data-ttu-id="a12fc-575">パラメーター - joinRelation</span><span class="sxs-lookup"><span data-stu-id="a12fc-575">Parameters - joinRelation</span></span>

<span data-ttu-id="a12fc-576">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-576">value</span></span>  

### <a name="return-value---joinrelation"></a><span data-ttu-id="a12fc-577">戻り値 - joinRelation</span><span class="sxs-lookup"><span data-stu-id="a12fc-577">Return Value - joinRelation</span></span>

## <a name="method-joinrelationasdictrelation"></a><span data-ttu-id="a12fc-578">メソッド joinRelationAsDictRelation</span><span class="sxs-lookup"><span data-stu-id="a12fc-578">Method joinRelationAsDictRelation</span></span>

```xpp
public DictRelation joinRelationAsDictRelation()
```

### <a name="return-value---joinrelationasdictrelation"></a><span data-ttu-id="a12fc-579">パラメーター - joinRelationAsDictRelation</span><span class="sxs-lookup"><span data-stu-id="a12fc-579">Return Value - joinRelationAsDictRelation</span></span>

## <a name="method-joinsource"></a><span data-ttu-id="a12fc-580">メソッド joinSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-580">Method joinSource</span></span>

```xpp
public int joinSource([AnyType value])
```

### <a name="parameters---joinsource"></a><span data-ttu-id="a12fc-581">パラメーター - joinSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-581">Parameters - joinSource</span></span>

<span data-ttu-id="a12fc-582">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-582">value</span></span>  

### <a name="return-value---joinsource"></a><span data-ttu-id="a12fc-583">戻り値 - joinSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-583">Return Value - joinSource</span></span>

## <a name="method-joinsourcedatasource"></a><span data-ttu-id="a12fc-584">メソッド joinSourceDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-584">Method joinSourceDataSource</span></span>

```xpp
public FormDataSource joinSourceDataSource()
```

### <a name="return-value---joinsourcedatasource"></a><span data-ttu-id="a12fc-585">戻り値 - joinSourceDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-585">Return Value - joinSourceDataSource</span></span>

## <a name="method-last"></a><span data-ttu-id="a12fc-586">メソッド last</span><span class="sxs-lookup"><span data-stu-id="a12fc-586">Method last</span></span>

<span data-ttu-id="a12fc-587">データ ソースの最後のレコードにマウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-587">Moves the mouse pointer to the last record in the data source.</span></span>

```xpp
public int last()
```

### <a name="return-value---last"></a><span data-ttu-id="a12fc-588">戻り値 - last</span><span class="sxs-lookup"><span data-stu-id="a12fc-588">Return Value - last</span></span>

<span data-ttu-id="a12fc-589">マウス ポインターが最後のレコードに正常に移動した場合は、ゼロ以外の値。</span><span class="sxs-lookup"><span data-stu-id="a12fc-589">A non-zero value if the mouse pointer is successfully moved to the last record.</span></span>

### <a name="remarks---last"></a><span data-ttu-id="a12fc-590">備考 - last</span><span class="sxs-lookup"><span data-stu-id="a12fc-590">Remarks - last</span></span>

<span data-ttu-id="a12fc-591">データ ソースの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントしてから [最後] をクリックすると、最後のメソッドをフォーム データ ソースでオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-591">The last method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking last.</span></span>

### <a name="examples---last"></a><span data-ttu-id="a12fc-592">例 - last</span><span class="sxs-lookup"><span data-stu-id="a12fc-592">Examples - last</span></span>

<span data-ttu-id="a12fc-593">次の例では、WMSOrderTransport フォームの InventDim データ ソースの最後のメソッドを上書きし、フォームで使用されている他のデータ ソースの最後のレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-593">The following example overrides the last method for the InventDim data source on the WMSOrderTransport form and returns the last record in the other data source that is used on the form.</span></span>

```xpp
int last() 
{ 
    return WMSOrder_ds.last(); 
}
```

## <a name="method-leave"></a><span data-ttu-id="a12fc-594">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="a12fc-594">Method leave</span></span>

<span data-ttu-id="a12fc-595">マウス ポインターが次のレコードまたは別のデータ ソースに移動すると、通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-595">Provides notification when the mouse pointer is moved to the next record or to another data source.</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="a12fc-596">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="a12fc-596">Return Value - leave</span></span>

<span data-ttu-id="a12fc-597">メソッドが上書きされない限り、常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-597">Always returns true, unless the method is overridden.</span></span>

### <a name="remarks---leave"></a><span data-ttu-id="a12fc-598">備考 - leave</span><span class="sxs-lookup"><span data-stu-id="a12fc-598">Remarks - leave</span></span>

<span data-ttu-id="a12fc-599">このメソッドは、レコードレベルの入力検証を実装するために上書きされることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-599">This method is often overridden to implement record-level input validation.</span></span> <span data-ttu-id="a12fc-600">データ ソースの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントしてから [leave] をクリックすると、leave メソッドをフォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-600">The leave method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking leave.</span></span>

### <a name="examples---leave"></a><span data-ttu-id="a12fc-601">例 - leave</span><span class="sxs-lookup"><span data-stu-id="a12fc-601">Examples - leave</span></span>

<span data-ttu-id="a12fc-602">次の例では、現在のレコードが残される前にデータ検証を実行する leave メソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-602">The following example overrides the leave method to perform data validation before the current record is left.</span></span> <span data-ttu-id="a12fc-603">データが無効な場合、このメソッドは false を返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-603">The method returns false if the data is invalid.</span></span>

```xpp
public boolean leave() 
{ 
    boolean ret; 
    ret = super(); 
    if(! salesLine.PBAItemLine::checkMandatory()) 
    { 
        return false; 
    } 
    return ret; 
}
```

## <a name="method-leaverecord"></a><span data-ttu-id="a12fc-604">メソッド leaveRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-604">Method leaveRecord</span></span>

<span data-ttu-id="a12fc-605">別のレコードまたはフォームの品目にフォーカスが移動したときに通知を提供します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-605">Provides notification when the focus moves to another record or item in the form.</span></span>

```xpp
public boolean leaveRecord([boolean forceUpdate])
```

### <a name="parameters---leaverecord"></a><span data-ttu-id="a12fc-606">パラメーター - leaveRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-606">Parameters - leaveRecord</span></span>

<span data-ttu-id="a12fc-607">forceUpdate</span><span class="sxs-lookup"><span data-stu-id="a12fc-607">forceUpdate</span></span>  

### <a name="return-value---leaverecord"></a><span data-ttu-id="a12fc-608">戻り値 - leaveRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-608">Return Value - leaveRecord</span></span>

<span data-ttu-id="a12fc-609">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a12fc-609">true if the operation succeeds; otherwise, false.</span></span>

### <a name="remarks---leaverecord"></a><span data-ttu-id="a12fc-610">備考 - leaveRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-610">Remarks - leaveRecord</span></span>

<span data-ttu-id="a12fc-611">メソッドが失敗する可能性があり、変更の検証や書き込みができない場合は false を返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-611">The method might fail and return false if changes could not be validated or written.</span></span> <span data-ttu-id="a12fc-612">このメソッドをオーバーライドすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-612">It is recommended that you not override this method.</span></span> <span data-ttu-id="a12fc-613">代わりに、FormDataSource.leave メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-613">Instead, override the FormDataSource.leave method.</span></span> <span data-ttu-id="a12fc-614">LeaveRecord メソッドをオーバーライドする場合は、スーパー メソッドを呼び出し、メソッドのカーネル実装が実行されるかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-614">If you do override the leaveRecord method, you must call the super method to make sure that the kernel implementation of the method is executed.</span></span>

## <a name="method-resolvepartlinks"></a><span data-ttu-id="a12fc-615">メソッド resolvePartLinks</span><span class="sxs-lookup"><span data-stu-id="a12fc-615">Method resolvePartLinks</span></span>

```xpp
public container resolvePartLinks([str relationName], [int partTableId])
```

### <a name="parameters---resolvepartlinks"></a><span data-ttu-id="a12fc-616">パラメーター - resolvePartLinks</span><span class="sxs-lookup"><span data-stu-id="a12fc-616">Parameters - resolvePartLinks</span></span>

<span data-ttu-id="a12fc-617">relationName</span><span class="sxs-lookup"><span data-stu-id="a12fc-617">relationName</span></span>  

<!-- -->

<span data-ttu-id="a12fc-618">partTableId</span><span class="sxs-lookup"><span data-stu-id="a12fc-618">partTableId</span></span>  

### <a name="return-value---resolvepartlinks"></a><span data-ttu-id="a12fc-619">戻り値 - resolvePartLinks</span><span class="sxs-lookup"><span data-stu-id="a12fc-619">Return Value - resolvePartLinks</span></span>

## <a name="method-linktype"></a><span data-ttu-id="a12fc-620">メソッド linkType</span><span class="sxs-lookup"><span data-stu-id="a12fc-620">Method linkType</span></span>

```xpp
public int linkType([int value])
```

### <a name="parameters---linktype"></a><span data-ttu-id="a12fc-621">パラメーター - linkType</span><span class="sxs-lookup"><span data-stu-id="a12fc-621">Parameters - linkType</span></span>

<span data-ttu-id="a12fc-622">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-622">value</span></span>  

### <a name="return-value---linktype"></a><span data-ttu-id="a12fc-623">戻り値 - linkType</span><span class="sxs-lookup"><span data-stu-id="a12fc-623">Return Value - linkType</span></span>

## <a name="method-mark"></a><span data-ttu-id="a12fc-624">メソッド mark</span><span class="sxs-lookup"><span data-stu-id="a12fc-624">Method mark</span></span>

```xpp
public int mark([int value])
```

### <a name="parameters---mark"></a><span data-ttu-id="a12fc-625">パラメーター - mark</span><span class="sxs-lookup"><span data-stu-id="a12fc-625">Parameters - mark</span></span>

<span data-ttu-id="a12fc-626">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-626">value</span></span>  

### <a name="return-value---mark"></a><span data-ttu-id="a12fc-627">戻り値 - mark</span><span class="sxs-lookup"><span data-stu-id="a12fc-627">Return Value - mark</span></span>

## <a name="method-markallloadedrecords"></a><span data-ttu-id="a12fc-628">メソッド markAllLoadedRecords</span><span class="sxs-lookup"><span data-stu-id="a12fc-628">Method markAllLoadedRecords</span></span>

```xpp
public boolean markAllLoadedRecords([int value])
```

### <a name="parameters---markallloadedrecords"></a><span data-ttu-id="a12fc-629">パラメーター - markAllLoadedRecords</span><span class="sxs-lookup"><span data-stu-id="a12fc-629">Parameters - markAllLoadedRecords</span></span>

<span data-ttu-id="a12fc-630">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-630">value</span></span>  

### <a name="return-value---markallloadedrecords"></a><span data-ttu-id="a12fc-631">戻り値 - markAllLoadedRecords</span><span class="sxs-lookup"><span data-stu-id="a12fc-631">Return Value - markAllLoadedRecords</span></span>

## <a name="method-markrecord"></a><span data-ttu-id="a12fc-632">メソッド markRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-632">Method markRecord</span></span>

<span data-ttu-id="a12fc-633">指定されたマーク値を使用して、指定されたレコードをマークします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-633">Marks the specified record by using the specified mark value.</span></span>

```xpp
public int markRecord(AnyType record, [int mark])
```

### <a name="parameters---markrecord"></a><span data-ttu-id="a12fc-634">パラメーター - markRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-634">Parameters - markRecord</span></span>

<span data-ttu-id="a12fc-635">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-635">record</span></span>  
<span data-ttu-id="a12fc-636">マークされたレコードに関連付けられた値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a12fc-636">The value that is associated with a marked record; optional.</span></span> <span data-ttu-id="a12fc-637">0 (ゼロ) 以外の値は、フォームのグリッドでマークされてレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-637">A value other than 0 (zero) causes the record to be displayed as marked in grids in the form.</span></span>

<!-- -->

<span data-ttu-id="a12fc-638">mark</span><span class="sxs-lookup"><span data-stu-id="a12fc-638">mark</span></span>  
<span data-ttu-id="a12fc-639">マークされたレコードに関連付けられた値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a12fc-639">The value that is associated with a marked record; optional.</span></span> <span data-ttu-id="a12fc-640">0 (ゼロ) 以外の値は、フォームのグリッドでマークされてレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-640">A value other than 0 (zero) causes the record to be displayed as marked in grids in the form.</span></span>

### <a name="return-value---markrecord"></a><span data-ttu-id="a12fc-641">戻り値 - markRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-641">Return Value - markRecord</span></span>

<span data-ttu-id="a12fc-642">レコードがマークされている場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="a12fc-642">A non-zero integer if the record has been marked.</span></span>

### <a name="remarks---markrecord"></a><span data-ttu-id="a12fc-643">備考 - markRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-643">Remarks - markRecord</span></span>

<span data-ttu-id="a12fc-644">フォーム外の select 文またはメソッド呼び出しを使用してレコードが見つかった場合は、FormDataSource.mark メソッドの代わりにこのメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-644">Use this method instead of the FormDataSource.mark method if the record has been found by using a select statement or a method call outside the form.</span></span>

## <a name="method-markrecords"></a><span data-ttu-id="a12fc-645">メソッド markRecords</span><span class="sxs-lookup"><span data-stu-id="a12fc-645">Method markRecords</span></span>

```xpp
public boolean markRecords(Array markedRecordIds)
```

### <a name="parameters---markrecords"></a><span data-ttu-id="a12fc-646">パラメーター - markRecords</span><span class="sxs-lookup"><span data-stu-id="a12fc-646">Parameters - markRecords</span></span>

<span data-ttu-id="a12fc-647">markedRecordIds</span><span class="sxs-lookup"><span data-stu-id="a12fc-647">markedRecordIds</span></span>  

### <a name="return-value---markrecords"></a><span data-ttu-id="a12fc-648">戻り値 - markRecords</span><span class="sxs-lookup"><span data-stu-id="a12fc-648">Return Value - markRecords</span></span>

## <a name="method-masterinheritancedatasource"></a><span data-ttu-id="a12fc-649">メソッド masterInheritanceDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-649">Method masterInheritanceDataSource</span></span>

```xpp
public FormDataSource masterInheritanceDataSource()
```

### <a name="return-value---masterinheritancedatasource"></a><span data-ttu-id="a12fc-650">戻り値 - masterInheritanceDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-650">Return Value - masterInheritanceDataSource</span></span>

## <a name="method-maxaccessright"></a><span data-ttu-id="a12fc-651">メソッド maxAccessRight</span><span class="sxs-lookup"><span data-stu-id="a12fc-651">Method maxAccessRight</span></span>

```xpp
public int maxAccessRight([int value])
```

### <a name="parameters---maxaccessright"></a><span data-ttu-id="a12fc-652">パラメーター - maxAccessRight</span><span class="sxs-lookup"><span data-stu-id="a12fc-652">Parameters - maxAccessRight</span></span>

<span data-ttu-id="a12fc-653">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-653">value</span></span>  

### <a name="return-value---maxaccessright"></a><span data-ttu-id="a12fc-654">戻り値 - maxAccessRight</span><span class="sxs-lookup"><span data-stu-id="a12fc-654">Return Value - maxAccessRight</span></span>

## <a name="method-maxrecordstoload"></a><span data-ttu-id="a12fc-655">メソッド maxRecordsToLoad</span><span class="sxs-lookup"><span data-stu-id="a12fc-655">Method maxRecordsToLoad</span></span>

```xpp
public int maxRecordsToLoad([int value])
```

### <a name="parameters---maxrecordstoload"></a><span data-ttu-id="a12fc-656">パラメーター - maxRecordsToLoad</span><span class="sxs-lookup"><span data-stu-id="a12fc-656">Parameters - maxRecordsToLoad</span></span>

<span data-ttu-id="a12fc-657">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-657">value</span></span>  

### <a name="return-value---maxrecordstoload"></a><span data-ttu-id="a12fc-658">戻り値 - maxRecordsToLoad</span><span class="sxs-lookup"><span data-stu-id="a12fc-658">Return Value - maxRecordsToLoad</span></span>

## <a name="method-maxpagingrowcountvalue"></a><span data-ttu-id="a12fc-659">メソッド maxPagingRowCountValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-659">Method maxPagingRowCountValue</span></span>

```xpp
public Int64 maxPagingRowCountValue([Int64 newValue])
```

### <a name="parameters---maxpagingrowcountvalue"></a><span data-ttu-id="a12fc-660">パラメーター - maxPagingRowCountValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-660">Parameters - maxPagingRowCountValue</span></span>

<span data-ttu-id="a12fc-661">newValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-661">newValue</span></span>  

### <a name="return-value---maxpagingrowcountvalue"></a><span data-ttu-id="a12fc-662">戻り値 - maxPagingRowCountValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-662">Return Value - maxPagingRowCountValue</span></span>

## <a name="method-name"></a><span data-ttu-id="a12fc-663">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a12fc-663">Method name</span></span>

<span data-ttu-id="a12fc-664">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-664">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="a12fc-665">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="a12fc-665">Parameters - name</span></span>

<span data-ttu-id="a12fc-666">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-666">value</span></span>  
<span data-ttu-id="a12fc-667">データ ソースの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a12fc-667">The name for the data source; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="a12fc-668">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="a12fc-668">Return Value - name</span></span>

<span data-ttu-id="a12fc-669">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="a12fc-669">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="a12fc-670">備考 - name</span><span class="sxs-lookup"><span data-stu-id="a12fc-670">Remarks - name</span></span>

<span data-ttu-id="a12fc-671">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-671">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="a12fc-672">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-672">It must start with a letter.</span></span>
-   <span data-ttu-id="a12fc-673">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="a12fc-673">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="a12fc-674">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-674">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="a12fc-675">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="a12fc-675">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="a12fc-676">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="a12fc-676">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="examples---name"></a><span data-ttu-id="a12fc-677">例 - name</span><span class="sxs-lookup"><span data-stu-id="a12fc-677">Examples - name</span></span>

<span data-ttu-id="a12fc-678">次の例では、フォーム データ ソースの QueryBuildDataSource オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-678">The following example creates a QueryBuildDataSource object for a form data source.</span></span> <span data-ttu-id="a12fc-679">FormDataSource.name メソッドは、QueryBuildDataSource オブジェクトの名前を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-679">The FormDataSource.name method is used to specify the name of the QueryBuildDataSource object.</span></span>

```xpp
static client QueryBuildDataSource fds2Qbds(FormDataSource _fds) 
{ 
    Form     form = _fds.formRun().form(); 
    if (_fds.query()  
        && _fds.name()  
        && _fds.query().dataSourceName(_fds.name())) 
    { 
        return _fds.query().dataSourceName(_fds.name()); 
    } 
    // Use the first data source if not found by name. 
    if (_fds.query() && _fds.query().dataSourceNo(1)) 
    { 
        return _fds.query().dataSourceNo(1); 
    } 
    return null; 
}
```

## <a name="method-next"></a><span data-ttu-id="a12fc-680">メソッド next</span><span class="sxs-lookup"><span data-stu-id="a12fc-680">Method next</span></span>

<span data-ttu-id="a12fc-681">データ ソースの次のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-681">Moves the focus to the next record in the data source.</span></span>

```xpp
public int next()
```

### <a name="return-value---next"></a><span data-ttu-id="a12fc-682">戻り値 - next</span><span class="sxs-lookup"><span data-stu-id="a12fc-682">Return Value - next</span></span>

<span data-ttu-id="a12fc-683">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="a12fc-683">A non-zero integer if the operation succeeds.</span></span>

### <a name="remarks---next"></a><span data-ttu-id="a12fc-684">備考 - next</span><span class="sxs-lookup"><span data-stu-id="a12fc-684">Remarks - next</span></span>

<span data-ttu-id="a12fc-685">フォーム データ ソース上では、次のメソッドは上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-685">The next method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-686">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [next] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-686">Right-click the Methods node under the data source, point to Override Method, and then click next.</span></span>

### <a name="examples---next"></a><span data-ttu-id="a12fc-687">例 - next</span><span class="sxs-lookup"><span data-stu-id="a12fc-687">Examples - next</span></span>

<span data-ttu-id="a12fc-688">次の例では、別のデータ ソースから次のレコードを返すために、データ ソースの next メソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-688">The following example overrides the next method on a data source to return the next record from a different data source.</span></span>

```xpp
int next() 
{ 
    return inventTrans_ds.next(); 
}
```

## <a name="method-nextpage"></a><span data-ttu-id="a12fc-689">メソッド nextPage</span><span class="sxs-lookup"><span data-stu-id="a12fc-689">Method nextPage</span></span>

<span data-ttu-id="a12fc-690">データ ソースで指定した数のレコード (位置変更) を進めます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-690">Moves a specified number of records forward in the data source.</span></span>

```xpp
public int nextPage(int pageSize)
```

### <a name="parameters---nextpage"></a><span data-ttu-id="a12fc-691">パラメーター - nextPage</span><span class="sxs-lookup"><span data-stu-id="a12fc-691">Parameters - nextPage</span></span>

<span data-ttu-id="a12fc-692">pageSize</span><span class="sxs-lookup"><span data-stu-id="a12fc-692">pageSize</span></span>  
<span data-ttu-id="a12fc-693">スキップするレコードの数。</span><span class="sxs-lookup"><span data-stu-id="a12fc-693">The number of records to skip.</span></span>

### <a name="return-value---nextpage"></a><span data-ttu-id="a12fc-694">戻り値 - nextPage</span><span class="sxs-lookup"><span data-stu-id="a12fc-694">Return Value - nextPage</span></span>

<span data-ttu-id="a12fc-695">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="a12fc-695">A non-zero integer if the operation succeeds.</span></span>

## <a name="method-numberofrowsloaded"></a><span data-ttu-id="a12fc-696">メソッド numberOfRowsLoaded</span><span class="sxs-lookup"><span data-stu-id="a12fc-696">Method numberOfRowsLoaded</span></span>

```xpp
public int numberOfRowsLoaded([boolean redirectToMasterDS])
```

### <a name="parameters---numberofrowsloaded"></a><span data-ttu-id="a12fc-697">パラメーター - numberOfRowsLoaded</span><span class="sxs-lookup"><span data-stu-id="a12fc-697">Parameters - numberOfRowsLoaded</span></span>

<span data-ttu-id="a12fc-698">redirectToMasterDS</span><span class="sxs-lookup"><span data-stu-id="a12fc-698">redirectToMasterDS</span></span>  

### <a name="return-value---numberofrowsloaded"></a><span data-ttu-id="a12fc-699">戻り値 - numberOfRowsLoaded</span><span class="sxs-lookup"><span data-stu-id="a12fc-699">Return Value - numberOfRowsLoaded</span></span>

## <a name="method-object"></a><span data-ttu-id="a12fc-700">メソッド object</span><span class="sxs-lookup"><span data-stu-id="a12fc-700">Method object</span></span>

<span data-ttu-id="a12fc-701">指定した ID を持つ FormDataObject クラスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-701">Returns an instance of the FormDataObject class that has the specified ID.</span></span>

```xpp
public FormDataObject object(FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---object"></a><span data-ttu-id="a12fc-702">パラメーター - object</span><span class="sxs-lookup"><span data-stu-id="a12fc-702">Parameters - object</span></span>

<span data-ttu-id="a12fc-703">fieldId</span><span class="sxs-lookup"><span data-stu-id="a12fc-703">fieldId</span></span>  

<!-- -->

<span data-ttu-id="a12fc-704">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="a12fc-704">arrayIndex</span></span>  

### <a name="return-value---object"></a><span data-ttu-id="a12fc-705">戻り値 - object</span><span class="sxs-lookup"><span data-stu-id="a12fc-705">Return Value - object</span></span>

<span data-ttu-id="a12fc-706">objectId パラメーターで指定されている ID を持つ FormDataObject クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="a12fc-706">An instance of the FormDataObject class that has the ID that is specified in the objectId parameter.</span></span>

### <a name="examples---object"></a><span data-ttu-id="a12fc-707">例 - object</span><span class="sxs-lookup"><span data-stu-id="a12fc-707">Examples - object</span></span>

<span data-ttu-id="a12fc-708">次の例では、RepositoryFolder フィールドの FormDataObject オブジェクトを SysVersionControlParameters テーブルに作成し、フィールドの AllowEdit プロパティを true に設定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-708">The following example creates a FormDataObject object for the RepositoryFolder field in the SysVersionControlParameters table, and then sets the AllowEdit property for the field to true.</span></span>

```xpp
public void initFormDatasource(FormDataSource _formDataSource) 
{ 
    FormDataObject dataObject = _formDataSource.object( 
        fieldnum(SysVersionControlParameters, RepositoryFolder)); 
    if (dataObject) 
    { 
        dataObject.allowEdit(true); 
    } 
}
```

## <a name="method-onlyfetchactive"></a><span data-ttu-id="a12fc-709">メソッド onlyFetchActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-709">Method onlyFetchActive</span></span>

```xpp
public boolean onlyFetchActive([boolean value])
```

### <a name="parameters---onlyfetchactive"></a><span data-ttu-id="a12fc-710">パラメーター - onlyFetchActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-710">Parameters - onlyFetchActive</span></span>

<span data-ttu-id="a12fc-711">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-711">value</span></span>  

### <a name="return-value---onlyfetchactive"></a><span data-ttu-id="a12fc-712">戻り値 - onlyFetchActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-712">Return Value - onlyFetchActive</span></span>

## <a name="method-optionalrecordmode"></a><span data-ttu-id="a12fc-713">メソッド optionalRecordMode</span><span class="sxs-lookup"><span data-stu-id="a12fc-713">Method optionalRecordMode</span></span>

```xpp
public int optionalRecordMode([int value])
```

### <a name="parameters---optionalrecordmode"></a><span data-ttu-id="a12fc-714">パラメーター - optionalRecordMode</span><span class="sxs-lookup"><span data-stu-id="a12fc-714">Parameters - optionalRecordMode</span></span>

<span data-ttu-id="a12fc-715">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-715">value</span></span>  

### <a name="return-value---optionalrecordmode"></a><span data-ttu-id="a12fc-716">戻り値 - optionalRecordMode</span><span class="sxs-lookup"><span data-stu-id="a12fc-716">Return Value - optionalRecordMode</span></span>

## <a name="method-pagesize"></a><span data-ttu-id="a12fc-717">メソッド pageSize</span><span class="sxs-lookup"><span data-stu-id="a12fc-717">Method pageSize</span></span>

```xpp
public int pageSize()
```

### <a name="return-value---pagesize"></a><span data-ttu-id="a12fc-718">戻り値 - pageSize</span><span class="sxs-lookup"><span data-stu-id="a12fc-718">Return Value - pageSize</span></span>

## <a name="method-pagingenabled"></a><span data-ttu-id="a12fc-719">メソッド pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="a12fc-719">Method pagingEnabled</span></span>

```xpp
public boolean pagingEnabled()
```

### <a name="return-value---pagingenabled"></a><span data-ttu-id="a12fc-720">戻り値 - pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="a12fc-720">Return Value - pagingEnabled</span></span>

## <a name="method-parenttitlefields"></a><span data-ttu-id="a12fc-721">メソッド parentTitleFields</span><span class="sxs-lookup"><span data-stu-id="a12fc-721">Method parentTitleFields</span></span>

```xpp
public TitleFields parentTitleFields(Common record)
```

### <a name="parameters---parenttitlefields"></a><span data-ttu-id="a12fc-722">パラメーター - parentTitleFields</span><span class="sxs-lookup"><span data-stu-id="a12fc-722">Parameters - parentTitleFields</span></span>

<span data-ttu-id="a12fc-723">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-723">record</span></span>  

### <a name="return-value---parenttitlefields"></a><span data-ttu-id="a12fc-724">戻り値 - parentTitleFields</span><span class="sxs-lookup"><span data-stu-id="a12fc-724">Return Value - parentTitleFields</span></span>

## <a name="method-prev"></a><span data-ttu-id="a12fc-725">メソッド prev</span><span class="sxs-lookup"><span data-stu-id="a12fc-725">Method prev</span></span>

<span data-ttu-id="a12fc-726">データ ソースの前のレコードにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-726">Moves the focus to the previous record in the data source.</span></span>

```xpp
public int prev()
```

### <a name="return-value---prev"></a><span data-ttu-id="a12fc-727">戻り値 - prev</span><span class="sxs-lookup"><span data-stu-id="a12fc-727">Return Value - prev</span></span>

<span data-ttu-id="a12fc-728">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="a12fc-728">A non-zero integer if the operation succeeds.</span></span>

### <a name="remarks---prev"></a><span data-ttu-id="a12fc-729">備考 - prev</span><span class="sxs-lookup"><span data-stu-id="a12fc-729">Remarks - prev</span></span>

<span data-ttu-id="a12fc-730">このメソッドを使用すると、データ ソースのレコードを逆順に反復処理できます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-730">This method can be used to iterate through the records of a data source in reverse order.</span></span> <span data-ttu-id="a12fc-731">フォーム データ ソース上では、prev メソッドは上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-731">The prev method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-732">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [prev] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-732">Right-click the Methods node under the data source, point to Override Method, and then click prev.</span></span>

### <a name="examples---prev"></a><span data-ttu-id="a12fc-733">例 - prev</span><span class="sxs-lookup"><span data-stu-id="a12fc-733">Examples - prev</span></span>

<span data-ttu-id="a12fc-734">次の例では、別のデータ ソースから前のレコードを返すために、データ ソースの prev メソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-734">The following example overrides the prev method on a data source to return the previous record from a different data source.</span></span>

```xpp
int prev() 
{ 
    return inventTrans_ds.prev(); 
}
```

## <a name="method-prevpage"></a><span data-ttu-id="a12fc-735">メソッド prevPage</span><span class="sxs-lookup"><span data-stu-id="a12fc-735">Method prevPage</span></span>

<span data-ttu-id="a12fc-736">データ ソースで指定した数のレコード分フォーカスを戻します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-736">Moves the focus back by a specified number of records in the data source.</span></span>

```xpp
public int prevPage(int pageSize)
```

### <a name="parameters---prevpage"></a><span data-ttu-id="a12fc-737">パラメーター - prevPage</span><span class="sxs-lookup"><span data-stu-id="a12fc-737">Parameters - prevPage</span></span>

<span data-ttu-id="a12fc-738">pageSize</span><span class="sxs-lookup"><span data-stu-id="a12fc-738">pageSize</span></span>  
<span data-ttu-id="a12fc-739">戻されるレコードの数。</span><span class="sxs-lookup"><span data-stu-id="a12fc-739">The number of records to move back by.</span></span>

### <a name="return-value---prevpage"></a><span data-ttu-id="a12fc-740">戻り値 - prevPage</span><span class="sxs-lookup"><span data-stu-id="a12fc-740">Return Value - prevPage</span></span>

<span data-ttu-id="a12fc-741">操作が成功した場合はゼロ以外の整数。</span><span class="sxs-lookup"><span data-stu-id="a12fc-741">A non-zero integer if the operation succeeds.</span></span>

## <a name="method-query"></a><span data-ttu-id="a12fc-742">メソッド query</span><span class="sxs-lookup"><span data-stu-id="a12fc-742">Method query</span></span>

```xpp
public Query query([Query value])
```

### <a name="parameters---query"></a><span data-ttu-id="a12fc-743">パラメーター - query</span><span class="sxs-lookup"><span data-stu-id="a12fc-743">Parameters - query</span></span>

<span data-ttu-id="a12fc-744">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-744">value</span></span>  

### <a name="return-value---query"></a><span data-ttu-id="a12fc-745">戻り値 - query</span><span class="sxs-lookup"><span data-stu-id="a12fc-745">Return Value - query</span></span>

## <a name="method-querybuilddatasource"></a><span data-ttu-id="a12fc-746">メソッド queryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-746">Method queryBuildDataSource</span></span>

```xpp
public QueryBuildDataSource queryBuildDataSource()
```

### <a name="return-value---querybuilddatasource"></a><span data-ttu-id="a12fc-747">戻り値 - queryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-747">Return Value - queryBuildDataSource</span></span>

## <a name="method-queryrun"></a><span data-ttu-id="a12fc-748">メソッド queryRun</span><span class="sxs-lookup"><span data-stu-id="a12fc-748">Method queryRun</span></span>

```xpp
public QueryRun queryRun([QueryRun value])
```

### <a name="parameters---queryrun"></a><span data-ttu-id="a12fc-749">パラメーター - queryRun</span><span class="sxs-lookup"><span data-stu-id="a12fc-749">Parameters - queryRun</span></span>

<span data-ttu-id="a12fc-750">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-750">value</span></span>  

### <a name="return-value---queryrun"></a><span data-ttu-id="a12fc-751">戻り値 - queryRun</span><span class="sxs-lookup"><span data-stu-id="a12fc-751">Return Value - queryRun</span></span>

## <a name="method-queryrunquerybuilddatasource"></a><span data-ttu-id="a12fc-752">メソッド queryRunQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-752">Method queryRunQueryBuildDataSource</span></span>

```xpp
public QueryBuildDataSource queryRunQueryBuildDataSource()
```

### <a name="return-value---queryrunquerybuilddatasource"></a><span data-ttu-id="a12fc-753">戻り値 - queryRunQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="a12fc-753">Return Value - queryRunQueryBuildDataSource</span></span>

## <a name="method-recordsmarked"></a><span data-ttu-id="a12fc-754">メソッド recordsMarked</span><span class="sxs-lookup"><span data-stu-id="a12fc-754">Method recordsMarked</span></span>

```xpp
public Array recordsMarked()
```

### <a name="return-value---recordsmarked"></a><span data-ttu-id="a12fc-755">戻り値 - recordsMarked</span><span class="sxs-lookup"><span data-stu-id="a12fc-755">Return Value - recordsMarked</span></span>

## <a name="method-startposition"></a><span data-ttu-id="a12fc-756">メソッド startPosition</span><span class="sxs-lookup"><span data-stu-id="a12fc-756">Method startPosition</span></span>

```xpp
public int startPosition([int value])
```

### <a name="parameters---startposition"></a><span data-ttu-id="a12fc-757">パラメーター - startPosition</span><span class="sxs-lookup"><span data-stu-id="a12fc-757">Parameters - startPosition</span></span>

<span data-ttu-id="a12fc-758">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-758">value</span></span>  

### <a name="return-value---startposition"></a><span data-ttu-id="a12fc-759">戻り値 - startPosition</span><span class="sxs-lookup"><span data-stu-id="a12fc-759">Return Value - startPosition</span></span>

## <a name="method-startrowindex"></a><span data-ttu-id="a12fc-760">メソッド startRowIndex</span><span class="sxs-lookup"><span data-stu-id="a12fc-760">Method startRowIndex</span></span>

```xpp
public int startRowIndex()
```

### <a name="return-value---startrowindex"></a><span data-ttu-id="a12fc-761">戻り値 - startRowIndex</span><span class="sxs-lookup"><span data-stu-id="a12fc-761">Return Value - startRowIndex</span></span>

## <a name="method-table"></a><span data-ttu-id="a12fc-762">メソッド table</span><span class="sxs-lookup"><span data-stu-id="a12fc-762">Method table</span></span>

<span data-ttu-id="a12fc-763">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-763">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="a12fc-764">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="a12fc-764">Parameters - table</span></span>

<span data-ttu-id="a12fc-765">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-765">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="a12fc-766">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="a12fc-766">Return Value - table</span></span>

<span data-ttu-id="a12fc-767">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="a12fc-767">The current value of the table ID associated with the object.</span></span>

## <a name="method-titlefields"></a><span data-ttu-id="a12fc-768">メソッド titleFields</span><span class="sxs-lookup"><span data-stu-id="a12fc-768">Method titleFields</span></span>

```xpp
public TitleFields titleFields(Common record)
```

### <a name="parameters---titlefields"></a><span data-ttu-id="a12fc-769">パラメーター - titleFields</span><span class="sxs-lookup"><span data-stu-id="a12fc-769">Parameters - titleFields</span></span>

<span data-ttu-id="a12fc-770">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-770">record</span></span>  

### <a name="return-value---titlefields"></a><span data-ttu-id="a12fc-771">戻り値 - titleFields</span><span class="sxs-lookup"><span data-stu-id="a12fc-771">Return Value - titleFields</span></span>

## <a name="method-totalnumberofrows"></a><span data-ttu-id="a12fc-772">メソッド totalNumberOfRows</span><span class="sxs-lookup"><span data-stu-id="a12fc-772">Method totalNumberOfRows</span></span>

```xpp
public int totalNumberOfRows()
```

### <a name="return-value---totalnumberofrows"></a><span data-ttu-id="a12fc-773">戻り値 - totalNumberOfRows</span><span class="sxs-lookup"><span data-stu-id="a12fc-773">Return Value - totalNumberOfRows</span></span>

## <a name="method-validatedelete"></a><span data-ttu-id="a12fc-774">メソッド validateDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-774">Method validateDelete</span></span>

<span data-ttu-id="a12fc-775">ユーザーがデータ ソースからのレコードの削除を確認することを要求します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-775">Requests that the user confirm the deletion of a record from the data source.</span></span>

```xpp
public boolean validateDelete()
```

### <a name="return-value---validatedelete"></a><span data-ttu-id="a12fc-776">戻り値 - validateDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-776">Return Value - validateDelete</span></span>

<span data-ttu-id="a12fc-777">削除が正常に実行される場合 true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a12fc-777">true if the deletion is performed successfully; otherwise, false.</span></span>

### <a name="remarks---validatedelete"></a><span data-ttu-id="a12fc-778">備考 - validateDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-778">Remarks - validateDelete</span></span>

<span data-ttu-id="a12fc-779">このメソッドは、データ ソース テーブルの validateDelete メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-779">This method calls the validateDelete method on the data source table.</span></span> <span data-ttu-id="a12fc-780">FormDataSource.validateDelete メソッドは、FormDataSource.delete メソッドにより呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-780">The FormDataSource.validateDelete method is called by the FormDataSource.delete method.</span></span> <span data-ttu-id="a12fc-781">必要に応じてカスタムのデータ入力規則のチェックを追加するには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-781">Use this method to add custom data validation checks whenever they are required.</span></span> <span data-ttu-id="a12fc-782">データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[validateDelete] をクリックして、validateDelete メソッドを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-782">The validateDelete method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking validateDelete.</span></span>

### <a name="examples---validatedelete"></a><span data-ttu-id="a12fc-783">例 - validateDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-783">Examples - validateDelete</span></span>

<span data-ttu-id="a12fc-784">次の例では、super() メソッドを呼び出さずに true を返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-784">The following example does not call the super() method and returns true.</span></span> <span data-ttu-id="a12fc-785">これは、削除確認メッセージ ボックスの表示を抑制します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-785">This suppresses the display of the delete confirmation message box.</span></span>

```xpp
public boolean validateDelete() 
{ 
    // Do not display warning dialog. 
    return true; 
}
```

## <a name="method-validatewrite"></a><span data-ttu-id="a12fc-786">メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-786">Method validateWrite</span></span>

<span data-ttu-id="a12fc-787">データが有効で書き込み可能な状態かどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-787">Determines whether data is valid and ready to be written.</span></span>

```xpp
public boolean validateWrite()
```

### <a name="return-value---validatewrite"></a><span data-ttu-id="a12fc-788">戻り値 - validateWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-788">Return Value - validateWrite</span></span>

<span data-ttu-id="a12fc-789">データが有効である場合は true を返します。それ以外の場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-789">Returns true if data is valid; otherwise, false.</span></span>

### <a name="remarks---validatewrite"></a><span data-ttu-id="a12fc-790">備考 - validateWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-790">Remarks - validateWrite</span></span>

<span data-ttu-id="a12fc-791">このメソッドは、FormDataSource.write メソッドから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-791">This method is called from the FormDataSource.write method.</span></span> <span data-ttu-id="a12fc-792">False が返される場合は、書き込み操作が中止され、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-792">If false is returned, the write operation is aborted and an error message is displayed.</span></span> <span data-ttu-id="a12fc-793">データ ソースにカスタム検証ルーチンを追加するには、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-793">Override this method to add custom validation routines to your data source.</span></span> <span data-ttu-id="a12fc-794">データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[validateWrite] をクリックして、validateWrite メソッドを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-794">The validateWrite method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking validateWrite.</span></span> <span data-ttu-id="a12fc-795">このメソッドで super() メソッドを呼び出すと、データ ソースとして使用されるテーブルの validateWrite メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-795">The call to the super() method in this method calls the validateWrite method on the table that is used as a data source.</span></span> <span data-ttu-id="a12fc-796">したがって、super() メソッドの戻り値を調べる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-796">Therefore, the return value of the super() method should be examined.</span></span> <span data-ttu-id="a12fc-797">このメソッドをオーバーライドする場合は、super() メソッドも true を返す場合に true のみを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-797">If you override the method, it should return true only if the super() method also returns true.</span></span>

## <a name="method-validtimestateautoquery"></a><span data-ttu-id="a12fc-798">メソッド validTimeStateAutoQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-798">Method validTimeStateAutoQuery</span></span>

```xpp
public int validTimeStateAutoQuery([int value])
```

### <a name="parameters---validtimestateautoquery"></a><span data-ttu-id="a12fc-799">パラメーター - validTimeStateAutoQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-799">Parameters - validTimeStateAutoQuery</span></span>

<span data-ttu-id="a12fc-800">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-800">value</span></span>  

### <a name="return-value---validtimestateautoquery"></a><span data-ttu-id="a12fc-801">戻り値 - validTimeStateAutoQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-801">Return Value - validTimeStateAutoQuery</span></span>

## <a name="method-validtimestateupdate"></a><span data-ttu-id="a12fc-802">メソッド validTimeStateUpdate</span><span class="sxs-lookup"><span data-stu-id="a12fc-802">Method validTimeStateUpdate</span></span>

```xpp
public int validTimeStateUpdate([int value])
```

### <a name="parameters---validtimestateupdate"></a><span data-ttu-id="a12fc-803">パラメーター - validTimeStateUpdate</span><span class="sxs-lookup"><span data-stu-id="a12fc-803">Parameters - validTimeStateUpdate</span></span>

<span data-ttu-id="a12fc-804">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-804">value</span></span>  

### <a name="return-value---validtimestateupdate"></a><span data-ttu-id="a12fc-805">戻り値 - validTimeStateUpdate</span><span class="sxs-lookup"><span data-stu-id="a12fc-805">Return Value - validTimeStateUpdate</span></span>

## <a name="method-delete"></a><span data-ttu-id="a12fc-806">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="a12fc-806">Method delete</span></span>

<span data-ttu-id="a12fc-807">データ ソースから現在のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-807">Deletes the current record from the data source.</span></span>

```xpp
public void delete()
```

### <a name="remarks---delete"></a><span data-ttu-id="a12fc-808">備考 - delete</span><span class="sxs-lookup"><span data-stu-id="a12fc-808">Remarks - delete</span></span>

<span data-ttu-id="a12fc-809">このメソッドは、ユーザーがフォーム内のレコードを削除するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-809">This method is called when a user deletes a record in a form.</span></span> <span data-ttu-id="a12fc-810">この削除メソッドは、FormDataSource.validateDelete メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-810">The delete method calls the FormDataSource.validateDelete method.</span></span> <span data-ttu-id="a12fc-811">validateDelete メソッドが true を返す場合は、レコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-811">If the validateDelete method returns true, the record is deleted.</span></span> <span data-ttu-id="a12fc-812">削除した後、カーソルは、次のレコードに配置されます (存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="a12fc-812">After the deletion, the cursor is positioned on the next record (if there is one).</span></span> <span data-ttu-id="a12fc-813">データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[削除] をクリックして、フォーム データ ソースで削除メソッドを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-813">The delete method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking delete.</span></span>

### <a name="examples---delete"></a><span data-ttu-id="a12fc-814">例 - delete</span><span class="sxs-lookup"><span data-stu-id="a12fc-814">Examples - delete</span></span>

<span data-ttu-id="a12fc-815">次の例では、SysCompilerOutput フォームの Errors データ ソースの delete メソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-815">The following example overrides the delete method on the Errors data source for the SysCompilerOutput form.</span></span> <span data-ttu-id="a12fc-816">このメソッドは、エラーを削除した後、コンパイラ出力フォームに表示されるエラーの数を更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-816">The method updates the number of errors that are displayed in the Compiler output form after an error has been removed.</span></span>

```xpp
public void delete() 
{ 
    super(); 
    sysCompilerOutput.updateCounters(); 
}
```

## <a name="method-addfieldtoselectionlist"></a><span data-ttu-id="a12fc-817">メソッド addFieldToSelectionList</span><span class="sxs-lookup"><span data-stu-id="a12fc-817">Method addFieldToSelectionList</span></span>

```xpp
public void addFieldToSelectionList(FieldId fieldId)
```

### <a name="parameters---addfieldtoselectionlist"></a><span data-ttu-id="a12fc-818">パラメーター - addFieldToSelectionList</span><span class="sxs-lookup"><span data-stu-id="a12fc-818">Parameters - addFieldToSelectionList</span></span>

<span data-ttu-id="a12fc-819">fieldId</span><span class="sxs-lookup"><span data-stu-id="a12fc-819">fieldId</span></span>  

## <a name="method-cacheremoverecord"></a><span data-ttu-id="a12fc-820">メソッド cacheRemoveRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-820">Method cacheRemoveRecord</span></span>

<span data-ttu-id="a12fc-821">データ ソースの基になるキャッシュから指定されたレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-821">Removes the specified record from the underlying cache of the data source.</span></span>

```xpp
public void cacheRemoveRecord([Common record])
```

### <a name="parameters---cacheremoverecord"></a><span data-ttu-id="a12fc-822">パラメーター - cacheRemoveRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-822">Parameters - cacheRemoveRecord</span></span>

<span data-ttu-id="a12fc-823">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-823">record</span></span>  
<span data-ttu-id="a12fc-824">キャッシュから削除するレコード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a12fc-824">The record to remove from the cache; optional.</span></span>

### <a name="remarks---cacheremoverecord"></a><span data-ttu-id="a12fc-825">備考 - cacheRemoveRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-825">Remarks - cacheRemoveRecord</span></span>

<span data-ttu-id="a12fc-826">Ttsbegin/ttscommit ブロック内のデータ変更ステートメントを囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-826">You must enclose data modification statements in a ttsbegin/ttscommit block.</span></span>

### <a name="examples---cacheremoverecord"></a><span data-ttu-id="a12fc-827">例 - cacheRemoveRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-827">Examples - cacheRemoveRecord</span></span>

<span data-ttu-id="a12fc-828">次の例では、データ ソースのキャッシュから inventTable レコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-828">The following example deletes the inventTable record from the cache of the data source.</span></span>

```xpp
void updateCache(container _conItemId) 
{ 
    SetIterator itSetItemId; 
    InventTable inventTable; 
    Set setItemId = new Set(Types::String); 
    setItemId = Set::create(_conItemId); 
    itSetItemId = new SetIterator(setItemId); 
    ttsBegin; 
    while (itSetItemId.more()) 
    { 
        inventTable = InventTable::find(itSetItemId.value()); 
        if(inventTableWithOutReqItem_ds. 
            findRecord(inventTable)) 
            inventTableWithOutReqItem_ds. 
                cacheRemoveRecord(inventTable); 
        itSetItemId.next(); 
    } 
    ttsCommit; 
}
```

## <a name="method-onvalidatedwrite"></a><span data-ttu-id="a12fc-829">メソッド OnValidatedWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-829">Method OnValidatedWrite</span></span>

```xpp
private void OnValidatedWrite([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onvalidatedwrite"></a><span data-ttu-id="a12fc-830">パラメーター - OnValidatedWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-830">Parameters - OnValidatedWrite</span></span>

<span data-ttu-id="a12fc-831">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-831">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-832">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-832">e</span></span>  

## <a name="method-reread"></a><span data-ttu-id="a12fc-833">メソッド reread</span><span class="sxs-lookup"><span data-stu-id="a12fc-833">Method reread</span></span>

<span data-ttu-id="a12fc-834">データベースから現在のレコードを再読み取りします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-834">Rereads the current record from the database.</span></span>

```xpp
public void reread()
```

### <a name="remarks---reread"></a><span data-ttu-id="a12fc-835">備考 - reread</span><span class="sxs-lookup"><span data-stu-id="a12fc-835">Remarks - reread</span></span>

<span data-ttu-id="a12fc-836">このメソッドを呼び出して、データベースからの最新の変更でレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-836">Call this method to update the record with the latest changes from the database.</span></span> <span data-ttu-id="a12fc-837">reread メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-837">The reread method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-838">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [reread] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-838">Right-click the Methods node under the data source, point to Override Method, and then click reread.</span></span>

### <a name="examples---reread"></a><span data-ttu-id="a12fc-839">例 - reread</span><span class="sxs-lookup"><span data-stu-id="a12fc-839">Examples - reread</span></span>

<span data-ttu-id="a12fc-840">次の例では、テーブルの更新に使用されるメソッドの一部として reread メソッドを使用しています。</span><span class="sxs-lookup"><span data-stu-id="a12fc-840">The following example uses the reread method as part of a method that is used to update a table.</span></span>

```xpp
void doRefresh() 
{ 
    salesTable_ds.reread(); 
    salesTable_ds.refresh(); 
    salesLine_ds.reread(); 
    salesLine_ds.refresh(); 
    interCompanyPurchSalesReference_ds.executeQuery(); 
}
```

## <a name="method-rereadjoinhierarchy"></a><span data-ttu-id="a12fc-841">メソッド rereadJoinHierarchy</span><span class="sxs-lookup"><span data-stu-id="a12fc-841">Method rereadJoinHierarchy</span></span>

```xpp
public void rereadJoinHierarchy()
```

## <a name="method-onrefreshed"></a><span data-ttu-id="a12fc-842">メソッド OnRefreshed</span><span class="sxs-lookup"><span data-stu-id="a12fc-842">Method OnRefreshed</span></span>

```xpp
private void OnRefreshed([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onrefreshed"></a><span data-ttu-id="a12fc-843">パラメーター - OnRefreshed</span><span class="sxs-lookup"><span data-stu-id="a12fc-843">Parameters - OnRefreshed</span></span>

<span data-ttu-id="a12fc-844">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-844">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-845">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-845">e</span></span>  

## <a name="method-onvalidateddelete"></a><span data-ttu-id="a12fc-846">メソッド OnValidatedDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-846">Method OnValidatedDelete</span></span>

```xpp
private void OnValidatedDelete([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onvalidateddelete"></a><span data-ttu-id="a12fc-847">パラメーター - OnValidatedDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-847">Parameters - OnValidatedDelete</span></span>

<span data-ttu-id="a12fc-848">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-848">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-849">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-849">e</span></span>  

## <a name="method-markchanged"></a><span data-ttu-id="a12fc-850">メソッド markChanged</span><span class="sxs-lookup"><span data-stu-id="a12fc-850">Method markChanged</span></span>

```xpp
public void markChanged()
```

## <a name="method-setpagingparameters"></a><span data-ttu-id="a12fc-851">メソッド setPagingParameters</span><span class="sxs-lookup"><span data-stu-id="a12fc-851">Method setPagingParameters</span></span>

```xpp
public void setPagingParameters(boolean pagingEnabled, int startRowIndex, int pageSize)
```

### <a name="parameters---setpagingparameters"></a><span data-ttu-id="a12fc-852">パラメーター - setPagingParameters</span><span class="sxs-lookup"><span data-stu-id="a12fc-852">Parameters - setPagingParameters</span></span>

<span data-ttu-id="a12fc-853">pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="a12fc-853">pagingEnabled</span></span>  

<!-- -->

<span data-ttu-id="a12fc-854">startRowIndex</span><span class="sxs-lookup"><span data-stu-id="a12fc-854">startRowIndex</span></span>  

<!-- -->

<span data-ttu-id="a12fc-855">pageSize</span><span class="sxs-lookup"><span data-stu-id="a12fc-855">pageSize</span></span>  

## <a name="method-deleted"></a><span data-ttu-id="a12fc-856">メソッド deleted</span><span class="sxs-lookup"><span data-stu-id="a12fc-856">Method deleted</span></span>

```xpp
public void deleted()
```

## <a name="method-print"></a><span data-ttu-id="a12fc-857">メソッド print</span><span class="sxs-lookup"><span data-stu-id="a12fc-857">Method print</span></span>

<span data-ttu-id="a12fc-858">現在のレコードを印刷します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-858">Prints the current record.</span></span>

```xpp
public void print(PrintMedium target)
```

### <a name="parameters---print"></a><span data-ttu-id="a12fc-859">パラメーター - print</span><span class="sxs-lookup"><span data-stu-id="a12fc-859">Parameters - print</span></span>

<span data-ttu-id="a12fc-860">target</span><span class="sxs-lookup"><span data-stu-id="a12fc-860">target</span></span>  
<span data-ttu-id="a12fc-861">レコードの印刷に使用する印刷メディア。</span><span class="sxs-lookup"><span data-stu-id="a12fc-861">The print medium to use to print the record.</span></span>

### <a name="remarks---print"></a><span data-ttu-id="a12fc-862">備考 - print</span><span class="sxs-lookup"><span data-stu-id="a12fc-862">Remarks - print</span></span>

<span data-ttu-id="a12fc-863">現在のレコードは、システムの自動レポート機能 (レポート ノードにある SysTableReport レポート) を使用して印刷されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-863">The current record is printed by using the system's auto report facilities (the SysTableReport report, which is located in the Reports node).</span></span> <span data-ttu-id="a12fc-864">フォーム データ ソース上では、print メソッドは上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-864">The print method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-865">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [print] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-865">Right-click the Methods node under the data source, point to Override Method, and then click print.</span></span>

## <a name="method-onreread"></a><span data-ttu-id="a12fc-866">メソッド OnReread</span><span class="sxs-lookup"><span data-stu-id="a12fc-866">Method OnReread</span></span>

```xpp
private void OnReread([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onreread"></a><span data-ttu-id="a12fc-867">パラメーター - OnReread</span><span class="sxs-lookup"><span data-stu-id="a12fc-867">Parameters - OnReread</span></span>

<span data-ttu-id="a12fc-868">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-868">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-869">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-869">e</span></span>  

## <a name="method-research"></a><span data-ttu-id="a12fc-870">メソッド research</span><span class="sxs-lookup"><span data-stu-id="a12fc-870">Method research</span></span>

<span data-ttu-id="a12fc-871">FormDataSource.research メソッドでオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-871">Is overridden by the FormDataSource.research method.</span></span>

```xpp
public void research([boolean retainPosition])
```

### <a name="parameters---research"></a><span data-ttu-id="a12fc-872">パラメーター - research</span><span class="sxs-lookup"><span data-stu-id="a12fc-872">Parameters - research</span></span>

<span data-ttu-id="a12fc-873">retainPosition</span><span class="sxs-lookup"><span data-stu-id="a12fc-873">retainPosition</span></span>  
<span data-ttu-id="a12fc-874">メソッドの完了後に、グリッド内の位置を維持するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a12fc-874">A Boolean value that indicates whether to maintain the position in the grid after the method is completed.</span></span>

### <a name="remarks---research"></a><span data-ttu-id="a12fc-875">備考 - research</span><span class="sxs-lookup"><span data-stu-id="a12fc-875">Remarks - research</span></span>

<span data-ttu-id="a12fc-876">このメソッドには、FormObjectSet クラスには機能がありません。</span><span class="sxs-lookup"><span data-stu-id="a12fc-876">This method has no functionality in the FormObjectSet class.</span></span> <span data-ttu-id="a12fc-877">現在適用されているフィルターおよびソートで定義されているデータベースの検索を更新する FormDataSource.research メソッドによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-877">It is overridden by the FormDataSource.research method, which updates the database search that is defined by the filters and sorts that are currently applied to the form.</span></span>

## <a name="method-createtypes"></a><span data-ttu-id="a12fc-878">メソッド createTypes</span><span class="sxs-lookup"><span data-stu-id="a12fc-878">Method createTypes</span></span>

```xpp
public void createTypes(Map concreteTypesToCreate, [boolean append], [boolean implicitCreate], [boolean explicitCreate])
```

### <a name="parameters---createtypes"></a><span data-ttu-id="a12fc-879">パラメーター - createTypes</span><span class="sxs-lookup"><span data-stu-id="a12fc-879">Parameters - createTypes</span></span>

<span data-ttu-id="a12fc-880">concreteTypesToCreate</span><span class="sxs-lookup"><span data-stu-id="a12fc-880">concreteTypesToCreate</span></span>  

<!-- -->

<span data-ttu-id="a12fc-881">append</span><span class="sxs-lookup"><span data-stu-id="a12fc-881">append</span></span>  

<!-- -->

<span data-ttu-id="a12fc-882">implicitCreate</span><span class="sxs-lookup"><span data-stu-id="a12fc-882">implicitCreate</span></span>  

<!-- -->

<span data-ttu-id="a12fc-883">explicitCreate</span><span class="sxs-lookup"><span data-stu-id="a12fc-883">explicitCreate</span></span>  

## <a name="method-oncreated"></a><span data-ttu-id="a12fc-884">メソッド OnCreated</span><span class="sxs-lookup"><span data-stu-id="a12fc-884">Method OnCreated</span></span>

```xpp
private void OnCreated([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---oncreated"></a><span data-ttu-id="a12fc-885">パラメーター - OnCreated</span><span class="sxs-lookup"><span data-stu-id="a12fc-885">Parameters - OnCreated</span></span>

<span data-ttu-id="a12fc-886">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-886">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-887">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-887">e</span></span>  

## <a name="method-onqueryexecuted"></a><span data-ttu-id="a12fc-888">メソッド OnQueryExecuted</span><span class="sxs-lookup"><span data-stu-id="a12fc-888">Method OnQueryExecuted</span></span>

```xpp
private void OnQueryExecuted([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onqueryexecuted"></a><span data-ttu-id="a12fc-889">パラメーター - OnQueryExecuted</span><span class="sxs-lookup"><span data-stu-id="a12fc-889">Parameters - OnQueryExecuted</span></span>

<span data-ttu-id="a12fc-890">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-890">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-891">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-891">e</span></span>  

## <a name="method-written"></a><span data-ttu-id="a12fc-892">メソッド written</span><span class="sxs-lookup"><span data-stu-id="a12fc-892">Method written</span></span>

```xpp
public void written()
```

## <a name="method-filter"></a><span data-ttu-id="a12fc-893">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="a12fc-893">Method filter</span></span>

<span data-ttu-id="a12fc-894">フィルターはデータ ソースで記録します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-894">Filters records in the data source.</span></span>

```xpp
public void filter(FieldId field, str value)
```

### <a name="parameters---filter"></a><span data-ttu-id="a12fc-895">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="a12fc-895">Parameters - filter</span></span>

<span data-ttu-id="a12fc-896"> フィールド</span><span class="sxs-lookup"><span data-stu-id="a12fc-896">field</span></span>  
<span data-ttu-id="a12fc-897">フィルター処理の条件。</span><span class="sxs-lookup"><span data-stu-id="a12fc-897">The filtering condition.</span></span>

<!-- -->

<span data-ttu-id="a12fc-898">値</span><span class="sxs-lookup"><span data-stu-id="a12fc-898">value</span></span>  
<span data-ttu-id="a12fc-899">フィルター処理の条件。</span><span class="sxs-lookup"><span data-stu-id="a12fc-899">The filtering condition.</span></span>

### <a name="remarks---filter"></a><span data-ttu-id="a12fc-900">備考 - filter</span><span class="sxs-lookup"><span data-stu-id="a12fc-900">Remarks - filter</span></span>

<span data-ttu-id="a12fc-901">標準フィルター機能を拡張するために、フィルター メソッドをフォーム・データ ソース上で上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-901">The filter method can be overridden on a form data source to extend the standard filtering functionality.</span></span> <span data-ttu-id="a12fc-902">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [filter] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-902">Right-click the Methods node under the data source, point to Override Method, and then click filter.</span></span>

## <a name="method-refresh"></a><span data-ttu-id="a12fc-903">メソッド refresh</span><span class="sxs-lookup"><span data-stu-id="a12fc-903">Method refresh</span></span>

<span data-ttu-id="a12fc-904">データ ソース内のすべてのレコードのビューを更新してフォームを更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-904">Updates the form by updating the view of all the records in the data source.</span></span>

```xpp
public void refresh()
```

### <a name="remarks---refresh"></a><span data-ttu-id="a12fc-905">備考 - refresh</span><span class="sxs-lookup"><span data-stu-id="a12fc-905">Remarks - refresh</span></span>

<span data-ttu-id="a12fc-906">レコードのコンテンツは、ディスクから読み込まずに再描画されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-906">The contents of the records are redrawn without loading from disk.</span></span> <span data-ttu-id="a12fc-907">たとえば、時間がかかる処理の実行中に更新する必要がある場合は、最新の情報に更新を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-907">You can, for example, use refresh if you have to update while a lengthy operation is running.</span></span> <span data-ttu-id="a12fc-908">すべてのレコードを最新の情報に更新しない場合は、FormDataSource.refreshEx メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-908">Use the FormDataSource.refreshEx method if you do not want to refresh all the records.</span></span> <span data-ttu-id="a12fc-909">refresh メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-909">The refresh method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-910">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [refresh] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-910">Right-click the Methods node under the data source, point to Override Method, and then click refresh.</span></span>

### <a name="examples---refresh"></a><span data-ttu-id="a12fc-911">例 - refresh</span><span class="sxs-lookup"><span data-stu-id="a12fc-911">Examples - refresh</span></span>

<span data-ttu-id="a12fc-912">次の例では、データ ソースの write メソッドを上書きして、書き込み操作後に別のデータ ソースのレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-912">The following example overrides the write method on a data source so that it updates records in a different data source after a write operation.</span></span>

```xpp
public void write() 
{ 
    super(); 
    EPParameters_ds.research(); 
    EPParameters_ds.refresh(); 
}
```

## <a name="method-write"></a><span data-ttu-id="a12fc-913">メソッド write</span><span class="sxs-lookup"><span data-stu-id="a12fc-913">Method write</span></span>

<span data-ttu-id="a12fc-914">FormDataSource.validateWrite メソッドを呼び出し、データベースの書き込み操作を管理します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-914">Calls the FormDataSource.validateWrite method and manages the database write operation.</span></span>

```xpp
public void write()
```

### <a name="remarks---write"></a><span data-ttu-id="a12fc-915">備考 - write</span><span class="sxs-lookup"><span data-stu-id="a12fc-915">Remarks - write</span></span>

<span data-ttu-id="a12fc-916">このメソッドは、ユーザーが新しいレコードを挿入するか、既存のレコードを更新するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-916">This method is invoked when a user inserts a new record or updates an existing one.</span></span> <span data-ttu-id="a12fc-917">refreshEx メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-917">The refreshEx method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-918">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [refreshEx] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-918">Right-click the Methods node under the data source, point to Override Method, and then click refreshEx.</span></span>

## <a name="method-executequery"></a><span data-ttu-id="a12fc-919">メソッド executeQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-919">Method executeQuery</span></span>

<span data-ttu-id="a12fc-920">データ ソース クエリを実行し、取得されたレコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-920">Executes the data source query and displays the records that are retrieved.</span></span>

```xpp
public void executeQuery()
```

### <a name="remarks---executequery"></a><span data-ttu-id="a12fc-921">備考 - executeQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-921">Remarks - executeQuery</span></span>

<span data-ttu-id="a12fc-922">このメソッドは、フォームがデータ表示用に開かれたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-922">This method is executed when a form is opened for data display.</span></span> <span data-ttu-id="a12fc-923">データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[executeQuery] をクリックして、executeQuery メソッドを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-923">The executeQuery method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking executeQuery.</span></span>

### <a name="examples---executequery"></a><span data-ttu-id="a12fc-924">例 - executeQuery</span><span class="sxs-lookup"><span data-stu-id="a12fc-924">Examples - executeQuery</span></span>

<span data-ttu-id="a12fc-925">次の例では、タブ ページの有効化イベントに応答してデータ ソース クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-925">The following example executes a data source query in response to a tab page activation event.</span></span>

```xpp
public void pageActivated() 
{ 
    monday_ds.executeQuery(); 
    super(); 
}
```

## <a name="method-setrecord"></a><span data-ttu-id="a12fc-926">メソッド setRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-926">Method setRecord</span></span>

```xpp
public void setRecord(Common record)
```

### <a name="parameters---setrecord"></a><span data-ttu-id="a12fc-927">パラメーター - setRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-927">Parameters - setRecord</span></span>

<span data-ttu-id="a12fc-928">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-928">record</span></span>  

## <a name="method-refreshex"></a><span data-ttu-id="a12fc-929">メソッド refreshEx</span><span class="sxs-lookup"><span data-stu-id="a12fc-929">Method refreshEx</span></span>

<span data-ttu-id="a12fc-930">指定されたレコードのビューを更新します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-930">Updates the view of the specified records.</span></span>

```xpp
public void refreshEx([AnyType pos])
```

### <a name="parameters---refreshex"></a><span data-ttu-id="a12fc-931">パラメーター - refreshEx</span><span class="sxs-lookup"><span data-stu-id="a12fc-931">Parameters - refreshEx</span></span>

<span data-ttu-id="a12fc-932">pos</span><span class="sxs-lookup"><span data-stu-id="a12fc-932">pos</span></span>  
<span data-ttu-id="a12fc-933">更新するレコードの番号 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a12fc-933">The number of the record to refresh; optional.</span></span> <span data-ttu-id="a12fc-934">-1 の値が指定されている場合は、すべてのレコードが更新されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-934">If a value of -1 is specified, all records are updated.</span></span> <span data-ttu-id="a12fc-935">-2 の値が指定されている場合、マークされているすべてのレコードと指定された表示オプションを持つすべてのレコードが更新されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-935">If a value of -2 is specified, all marked records and all records that have display options specified are updated.</span></span> <span data-ttu-id="a12fc-936">既定値は -2 です。</span><span class="sxs-lookup"><span data-stu-id="a12fc-936">The default value is -2.</span></span>

### <a name="remarks---refreshex"></a><span data-ttu-id="a12fc-937">備考 - refreshEx</span><span class="sxs-lookup"><span data-stu-id="a12fc-937">Remarks - refreshEx</span></span>

<span data-ttu-id="a12fc-938">データ ソースの Methods ノードを右クリックして [Override Method] をポイントし、[refreshEx] をクリックして、refreshEx メソッドを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-938">The refreshEx method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking refreshEx.</span></span>

## <a name="method-setcurrent"></a><span data-ttu-id="a12fc-939">メソッド setCurrent</span><span class="sxs-lookup"><span data-stu-id="a12fc-939">Method setCurrent</span></span>

```xpp
public void setCurrent()
```

## <a name="method-onvalidatingdelete"></a><span data-ttu-id="a12fc-940">メソッド OnValidatingDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-940">Method OnValidatingDelete</span></span>

```xpp
private void OnValidatingDelete([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onvalidatingdelete"></a><span data-ttu-id="a12fc-941">パラメーター - OnValidatingDelete</span><span class="sxs-lookup"><span data-stu-id="a12fc-941">Parameters - OnValidatingDelete</span></span>

<span data-ttu-id="a12fc-942">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-942">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-943">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-943">e</span></span>  

## <a name="method-writing"></a><span data-ttu-id="a12fc-944">メソッド writing</span><span class="sxs-lookup"><span data-stu-id="a12fc-944">Method writing</span></span>

```xpp
public void writing()
```

## <a name="method-onwritten"></a><span data-ttu-id="a12fc-945">メソッド OnWritten</span><span class="sxs-lookup"><span data-stu-id="a12fc-945">Method OnWritten</span></span>

```xpp
private void OnWritten([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onwritten"></a><span data-ttu-id="a12fc-946">パラメーター - OnWritten</span><span class="sxs-lookup"><span data-stu-id="a12fc-946">Parameters - OnWritten</span></span>

<span data-ttu-id="a12fc-947">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-947">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-948">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-948">e</span></span>  

## <a name="method-cleardisplayoption"></a><span data-ttu-id="a12fc-949">メソッド clearDisplayOption</span><span class="sxs-lookup"><span data-stu-id="a12fc-949">Method clearDisplayOption</span></span>

<span data-ttu-id="a12fc-950">レコードに対して以前に指定された表示オプションをクリアして、レコードを再描画します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-950">Clears display options that were previously specified for a record and then redraws the record.</span></span>

```xpp
public void clearDisplayOption(Common record)
```

### <a name="parameters---cleardisplayoption"></a><span data-ttu-id="a12fc-951">パラメーター - clearDisplayOption</span><span class="sxs-lookup"><span data-stu-id="a12fc-951">Parameters - clearDisplayOption</span></span>

<span data-ttu-id="a12fc-952">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-952">record</span></span>  
<span data-ttu-id="a12fc-953">再振出するレコード。</span><span class="sxs-lookup"><span data-stu-id="a12fc-953">The record to redraw.</span></span>

### <a name="remarks---cleardisplayoption"></a><span data-ttu-id="a12fc-954">備考 - clearDisplayOption</span><span class="sxs-lookup"><span data-stu-id="a12fc-954">Remarks - clearDisplayOption</span></span>

<span data-ttu-id="a12fc-955">表示オプションは、FormDataSource.displayOption メソッドを使用して設定されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-955">Display options are set by using the FormDataSource.displayOption method.</span></span>

### <a name="examples---cleardisplayoption"></a><span data-ttu-id="a12fc-956">例 - clearDisplayOption</span><span class="sxs-lookup"><span data-stu-id="a12fc-956">Examples - clearDisplayOption</span></span>

<span data-ttu-id="a12fc-957">次の例では、データ ソースの最初のレコードを再描画します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-957">The following example redraws the first record in a data source.</span></span>

```xpp
public void run() 
{ 
    super(); 
    sysRecordTmpTemplate_ds.clearDisplayOption( 
        sysRecordTmpTemplate_ds.getFirst()); 
}
```

## <a name="method-onmarkchanged"></a><span data-ttu-id="a12fc-958">メソッド OnMarkChanged</span><span class="sxs-lookup"><span data-stu-id="a12fc-958">Method OnMarkChanged</span></span>

```xpp
private void OnMarkChanged([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onmarkchanged"></a><span data-ttu-id="a12fc-959">パラメーター - OnMarkChanged</span><span class="sxs-lookup"><span data-stu-id="a12fc-959">Parameters - OnMarkChanged</span></span>

<span data-ttu-id="a12fc-960">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-960">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-961">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-961">e</span></span>  

## <a name="method-onleftrecord"></a><span data-ttu-id="a12fc-962">メソッド OnLeftRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-962">Method OnLeftRecord</span></span>

```xpp
private void OnLeftRecord([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onleftrecord"></a><span data-ttu-id="a12fc-963">パラメーター - OnLeftRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-963">Parameters - OnLeftRecord</span></span>

<span data-ttu-id="a12fc-964">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-964">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-965">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-965">e</span></span>  

## <a name="method-ondeleted"></a><span data-ttu-id="a12fc-966">メソッド OnDeleted</span><span class="sxs-lookup"><span data-stu-id="a12fc-966">Method OnDeleted</span></span>

```xpp
private void OnDeleted([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---ondeleted"></a><span data-ttu-id="a12fc-967">パラメーター - OnDeleted</span><span class="sxs-lookup"><span data-stu-id="a12fc-967">Parameters - OnDeleted</span></span>

<span data-ttu-id="a12fc-968">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-968">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-969">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-969">e</span></span>  

## <a name="method-removefilter"></a><span data-ttu-id="a12fc-970">メソッド removeFilter</span><span class="sxs-lookup"><span data-stu-id="a12fc-970">Method removeFilter</span></span>

<span data-ttu-id="a12fc-971">データ ソースのクエリをリセットします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-971">Resets the query for the data source.</span></span>

```xpp
public void removeFilter()
```

### <a name="remarks---removefilter"></a><span data-ttu-id="a12fc-972">備考 - removeFilter</span><span class="sxs-lookup"><span data-stu-id="a12fc-972">Remarks - removeFilter</span></span>

<span data-ttu-id="a12fc-973">このメソッドは、ユーザーがフォーム コントロールのショートカット メニューでフィルターのキャンセル コマンドをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-973">This method is called when a user clicks the Cancel Filter command in the shortcut menu on a form control.</span></span> <span data-ttu-id="a12fc-974">removeFilter メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-974">The removeFilter method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-975">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [removeFilter] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-975">Right-click the Methods node under the data source, point to Override Method, and then click removeFilter.</span></span> <span data-ttu-id="a12fc-976">たとえば、removeFilter は FormDataSource.init メソッドによって生成された元のクエリに対するすべての変更を削除します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-976">For example, removeFilter removes all modifications to the original query that is generated by the FormDataSource.init method.</span></span>

## <a name="method-oninitialized"></a><span data-ttu-id="a12fc-977">メソッド OnInitialized</span><span class="sxs-lookup"><span data-stu-id="a12fc-977">Method OnInitialized</span></span>

```xpp
private void OnInitialized([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---oninitialized"></a><span data-ttu-id="a12fc-978">パラメーター - OnInitialized</span><span class="sxs-lookup"><span data-stu-id="a12fc-978">Parameters - OnInitialized</span></span>

<span data-ttu-id="a12fc-979">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-979">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-980">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-980">e</span></span>  

## <a name="method-onpostlinkactive"></a><span data-ttu-id="a12fc-981">メソッド OnPostLinkActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-981">Method OnPostLinkActive</span></span>

```xpp
private void OnPostLinkActive([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onpostlinkactive"></a><span data-ttu-id="a12fc-982">パラメーター - OnPostLinkActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-982">Parameters - OnPostLinkActive</span></span>

<span data-ttu-id="a12fc-983">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-983">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-984">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-984">e</span></span>  

## <a name="method-onselectionchanged"></a><span data-ttu-id="a12fc-985">メソッド OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="a12fc-985">Method OnSelectionChanged</span></span>

```xpp
private void OnSelectionChanged([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onselectionchanged"></a><span data-ttu-id="a12fc-986">パラメーター - OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="a12fc-986">Parameters - OnSelectionChanged</span></span>

<span data-ttu-id="a12fc-987">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-987">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-988">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-988">e</span></span>  

## <a name="method-deleting"></a><span data-ttu-id="a12fc-989">メソッド deleting</span><span class="sxs-lookup"><span data-stu-id="a12fc-989">Method deleting</span></span>

```xpp
public void deleting()
```

## <a name="method-observe"></a><span data-ttu-id="a12fc-990">メソッド observe</span><span class="sxs-lookup"><span data-stu-id="a12fc-990">Method observe</span></span>

```xpp
public void observe()
```

## <a name="method-onwriting"></a><span data-ttu-id="a12fc-991">メソッド OnWriting</span><span class="sxs-lookup"><span data-stu-id="a12fc-991">Method OnWriting</span></span>

```xpp
private void OnWriting([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onwriting"></a><span data-ttu-id="a12fc-992">パラメーター - OnWriting</span><span class="sxs-lookup"><span data-stu-id="a12fc-992">Parameters - OnWriting</span></span>

<span data-ttu-id="a12fc-993">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-993">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-994">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-994">e</span></span>  

## <a name="method-onactivated"></a><span data-ttu-id="a12fc-995">メソッド OnActivated</span><span class="sxs-lookup"><span data-stu-id="a12fc-995">Method OnActivated</span></span>

```xpp
private void OnActivated([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onactivated"></a><span data-ttu-id="a12fc-996">パラメーター - OnActivated</span><span class="sxs-lookup"><span data-stu-id="a12fc-996">Parameters - OnActivated</span></span>

<span data-ttu-id="a12fc-997">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-997">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-998">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-998">e</span></span>  

## <a name="method-removefieldfromselectionlist"></a><span data-ttu-id="a12fc-999">メソッド removeFieldFromSelectionList</span><span class="sxs-lookup"><span data-stu-id="a12fc-999">Method removeFieldFromSelectionList</span></span>

```xpp
public void removeFieldFromSelectionList(FieldId fieldId)
```

### <a name="parameters---removefieldfromselectionlist"></a><span data-ttu-id="a12fc-1000">パラメーター - removeFieldFromSelectionList</span><span class="sxs-lookup"><span data-stu-id="a12fc-1000">Parameters - removeFieldFromSelectionList</span></span>

<span data-ttu-id="a12fc-1001">fieldId</span><span class="sxs-lookup"><span data-stu-id="a12fc-1001">fieldId</span></span>  

## <a name="method-oncreating"></a><span data-ttu-id="a12fc-1002">メソッド OnCreating</span><span class="sxs-lookup"><span data-stu-id="a12fc-1002">Method OnCreating</span></span>

```xpp
private void OnCreating([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---oncreating"></a><span data-ttu-id="a12fc-1003">パラメーター - OnCreating</span><span class="sxs-lookup"><span data-stu-id="a12fc-1003">Parameters - OnCreating</span></span>

<span data-ttu-id="a12fc-1004">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-1004">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-1005">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-1005">e</span></span>  

## <a name="method-rereadreferencedatasources"></a><span data-ttu-id="a12fc-1006">メソッド rereadReferenceDataSources</span><span class="sxs-lookup"><span data-stu-id="a12fc-1006">Method rereadReferenceDataSources</span></span>

```xpp
public void rereadReferenceDataSources()
```

## <a name="method-onvalidatingwrite"></a><span data-ttu-id="a12fc-1007">メソッド OnValidatingWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-1007">Method OnValidatingWrite</span></span>

```xpp
private void OnValidatingWrite([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onvalidatingwrite"></a><span data-ttu-id="a12fc-1008">パラメーター - OnValidatingWrite</span><span class="sxs-lookup"><span data-stu-id="a12fc-1008">Parameters - OnValidatingWrite</span></span>

<span data-ttu-id="a12fc-1009">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-1009">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-1010">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-1010">e</span></span>  

## <a name="method-prompt"></a><span data-ttu-id="a12fc-1011">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="a12fc-1011">Method prompt</span></span>

<span data-ttu-id="a12fc-1012">クエリの範囲を制限するために使用される、標準フォーム、SysQueryForm を有効化します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1012">Activates the standard form, SysQueryForm, that is used to limit a query range.</span></span>

```xpp
public void prompt()
```

### <a name="remarks---prompt"></a><span data-ttu-id="a12fc-1013">備考 - prompt</span><span class="sxs-lookup"><span data-stu-id="a12fc-1013">Remarks - prompt</span></span>

<span data-ttu-id="a12fc-1014">このメソッドは、ユーザーが [コマンド] メニューの [レコードのフィルター] コマンドをクリックするか、CTRL+F3 を押すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1014">This method is called when a user clicks the Filter records command on the Command menu or presses CTRL+F3.</span></span> <span data-ttu-id="a12fc-1015">prompt メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1015">The prompt method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-1016">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [prompt] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1016">Right-click the Methods node under the data source, point to Override Method, and then click prompt.</span></span>

## <a name="method-onqueryexecuting"></a><span data-ttu-id="a12fc-1017">メソッド OnQueryExecuting</span><span class="sxs-lookup"><span data-stu-id="a12fc-1017">Method OnQueryExecuting</span></span>

```xpp
private void OnQueryExecuting([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onqueryexecuting"></a><span data-ttu-id="a12fc-1018">パラメーター - OnQueryExecuting</span><span class="sxs-lookup"><span data-stu-id="a12fc-1018">Parameters - OnQueryExecuting</span></span>

<span data-ttu-id="a12fc-1019">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-1019">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-1020">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-1020">e</span></span>  

## <a name="method-oninitvalue"></a><span data-ttu-id="a12fc-1021">メソッド OnInitValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-1021">Method OnInitValue</span></span>

```xpp
private void OnInitValue([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---oninitvalue"></a><span data-ttu-id="a12fc-1022">パラメーター - OnInitValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-1022">Parameters - OnInitValue</span></span>

<span data-ttu-id="a12fc-1023">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-1023">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-1024">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-1024">e</span></span>  

## <a name="method-clearreferencedata"></a><span data-ttu-id="a12fc-1025">メソッド clearReferenceData</span><span class="sxs-lookup"><span data-stu-id="a12fc-1025">Method clearReferenceData</span></span>

```xpp
public void clearReferenceData(FieldId fieldId)
```

### <a name="parameters---clearreferencedata"></a><span data-ttu-id="a12fc-1026">パラメーター - clearReferenceData</span><span class="sxs-lookup"><span data-stu-id="a12fc-1026">Parameters - clearReferenceData</span></span>

<span data-ttu-id="a12fc-1027">fieldId</span><span class="sxs-lookup"><span data-stu-id="a12fc-1027">fieldId</span></span>  

## <a name="method-cursornotify"></a><span data-ttu-id="a12fc-1028">メソッド cursorNotify</span><span class="sxs-lookup"><span data-stu-id="a12fc-1028">Method cursorNotify</span></span>

<span data-ttu-id="a12fc-1029">カーソルのイベントに関してアプリケーションに通知します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1029">Notifies the application about a cursor event.</span></span>

```xpp
public void cursorNotify(int event)
```

### <a name="parameters---cursornotify"></a><span data-ttu-id="a12fc-1030">パラメーター - cursorNotify</span><span class="sxs-lookup"><span data-stu-id="a12fc-1030">Parameters - cursorNotify</span></span>

<span data-ttu-id="a12fc-1031">イベント</span><span class="sxs-lookup"><span data-stu-id="a12fc-1031">event</span></span>  
<span data-ttu-id="a12fc-1032">カーソルのイベント識別子。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1032">The cursor event identifier.</span></span> <span data-ttu-id="a12fc-1033">次のテーブルに、利用可能なカーソル イベントを示します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1033">The following table shows the available cursor events.</span></span>

### <a name="remarks---cursornotify"></a><span data-ttu-id="a12fc-1034">備考 - cursorNotify</span><span class="sxs-lookup"><span data-stu-id="a12fc-1034">Remarks - cursorNotify</span></span>

<span data-ttu-id="a12fc-1035">このメソッドは、カーソル イベントのカスタム処理を実装するためにオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1035">This method can be overridden to implement custom handling of cursor events.</span></span> <span data-ttu-id="a12fc-1036">ただし、必要に応じてイベントを処理するカーネルを有効にするため、super() メソッドが最初に呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1036">However, the super() method has to be called first to enable the kernel to handle the event as appropriate.</span></span>

## <a name="method-displayoption"></a><span data-ttu-id="a12fc-1037">メソッド displayOption</span><span class="sxs-lookup"><span data-stu-id="a12fc-1037">Method displayOption</span></span>

<span data-ttu-id="a12fc-1038">データ ソース内のレコードのテキストの色および背景色を設定します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1038">Sets the text color and the background color for a record in the data source.</span></span>

```xpp
public void displayOption(Common record, FormRowDisplayOption options)
```

### <a name="parameters---displayoption"></a><span data-ttu-id="a12fc-1039">パラメーター - displayOption</span><span class="sxs-lookup"><span data-stu-id="a12fc-1039">Parameters - displayOption</span></span>

<span data-ttu-id="a12fc-1040">記録</span><span class="sxs-lookup"><span data-stu-id="a12fc-1040">record</span></span>  
<span data-ttu-id="a12fc-1041">目的のレコード表示プロパティをカプセル化する FormRowDisplayOption オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1041">The FormRowDisplayOption object that encapsulates the desired record display properties.</span></span>

<!-- -->

<span data-ttu-id="a12fc-1042">オプション</span><span class="sxs-lookup"><span data-stu-id="a12fc-1042">options</span></span>  
<span data-ttu-id="a12fc-1043">目的のレコード表示プロパティをカプセル化する FormRowDisplayOption オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1043">The FormRowDisplayOption object that encapsulates the desired record display properties.</span></span>

### <a name="remarks---displayoption"></a><span data-ttu-id="a12fc-1044">備考 - displayOption</span><span class="sxs-lookup"><span data-stu-id="a12fc-1044">Remarks - displayOption</span></span>

<span data-ttu-id="a12fc-1045">このメソッドは、レコードがフォームで表示される前にレコードごとに 1 回実行されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1045">This method is executed one time for each record before the record is displayed in a form.</span></span> <span data-ttu-id="a12fc-1046">displayOption メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1046">The displayOption method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-1047">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [displayOption] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1047">Right-click the Methods node under the data source, point to Override Method, and then click displayOption.</span></span>

### <a name="examples---displayoption"></a><span data-ttu-id="a12fc-1048">例 - displayOption</span><span class="sxs-lookup"><span data-stu-id="a12fc-1048">Examples - displayOption</span></span>

<span data-ttu-id="a12fc-1049">次の例では、displayOption メソッドを上書きして、格納されているプロファイルから表示オプションを設定し、特定のレコードの設定に基づいて背景色を上書きします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1049">The following example overrides the displayOption method to set display options from a stored profile and to override the background color that is based on the settings for the particular record.</span></span>

```xpp
public void displayOption(Common _record, FormRowDisplayOption 
    _options) 
{ 
    JmgProfileTable profile; 
    profile = _record; 
    _options.backColor(profile.Color); 
    super(_record, _options); 
}
```

## <a name="method-create"></a><span data-ttu-id="a12fc-1050">メソッド create</span><span class="sxs-lookup"><span data-stu-id="a12fc-1050">Method create</span></span>

<span data-ttu-id="a12fc-1051">データ ソースに新しいレコードを作成します</span><span class="sxs-lookup"><span data-stu-id="a12fc-1051">Creates a new record in the data source.</span></span>

```xpp
public void create([boolean append])
```

### <a name="parameters---create"></a><span data-ttu-id="a12fc-1052">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="a12fc-1052">Parameters - create</span></span>

<span data-ttu-id="a12fc-1053">append</span><span class="sxs-lookup"><span data-stu-id="a12fc-1053">append</span></span>  
<span data-ttu-id="a12fc-1054">現在のカーソル位置の前後にレコードを挿入するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1054">A Boolean value that indicates whether to insert the record after or before the current cursor position.</span></span> <span data-ttu-id="a12fc-1055">true に設定されている場合、現在のレコードの後に新しいレコードが挿入されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1055">If it is set to true, the new record is inserted after the current record.</span></span>

### <a name="remarks---create"></a><span data-ttu-id="a12fc-1056">備考 - create</span><span class="sxs-lookup"><span data-stu-id="a12fc-1056">Remarks - create</span></span>

<span data-ttu-id="a12fc-1057">このメソッドは、挿入 (CTRL+N) の既定のショートカット キーを使用するなど、ユーザーがデータ ソースに新しいレコードを作成するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1057">This method is called when a user creates a new record in a data source, such as by using the default shortcut key for insertion (CTRL+N).</span></span> <span data-ttu-id="a12fc-1058">create メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1058">The create method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-1059">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] &gt; [create] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1059">Right-click the Methods node under the data source, and then select Override Method &gt; create.</span></span>

## <a name="method-init"></a><span data-ttu-id="a12fc-1060">メソッド init</span><span class="sxs-lookup"><span data-stu-id="a12fc-1060">Method init</span></span>

<span data-ttu-id="a12fc-1061">データソース プロパティに基づくデータソース クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1061">Creates a data source query that is based on the data source properties.</span></span>

```xpp
public void init()
```

### <a name="remarks---init"></a><span data-ttu-id="a12fc-1062">備考 - init</span><span class="sxs-lookup"><span data-stu-id="a12fc-1062">Remarks - init</span></span>

<span data-ttu-id="a12fc-1063">このメソッドは、フォームが開かれたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1063">This method is called when the form is opened.</span></span> <span data-ttu-id="a12fc-1064">メソッドによって生成されたクエリは、フォームに表示するデータをロードするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1064">The query that is generated by the method is used to the load data so that it can be displayed in the form.</span></span> <span data-ttu-id="a12fc-1065">フォーム データ ソース上では、init メソッドは上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1065">The init method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-1066">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [init] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1066">Right-click the Methods node under the data source, point to Override Method, and then click init.</span></span>

### <a name="examples---init"></a><span data-ttu-id="a12fc-1067">例 - init</span><span class="sxs-lookup"><span data-stu-id="a12fc-1067">Examples - init</span></span>

<span data-ttu-id="a12fc-1068">次の例では、データ ソースのソート順を指定するために、データ ソースの init メソッドを上書きしています。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1068">The following example overrides the init method on a data source to specify the sorting order for the data source.</span></span>

```xpp
public void init() 
{ 
    super(); 
    this.query().dataSourceTable( 
        tablenum(SysVersionControlTmpItem)).addSortField( 
            fieldnum(SysVersionControlTmpItem, VCSDate), 
        SortOrder::Descending); 
    this.query().dataSourceTable( 
        tablenum(SysVersionControlTmpItem)).addSortField( 
            fieldnum(SysVersionControlTmpItem, VCSTime), 
        SortOrder::Descending); 
    this.query().dataSourceTable( 
        tablenum(SysVersionControlTmpItem)).addSortField( 
            fieldnum(SysVersionControlTmpItem, ChangeNumber), 
        SortOrder::Ascending); 
}
```

## <a name="method-linkactive"></a><span data-ttu-id="a12fc-1069">メソッド linkActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-1069">Method linkActive</span></span>

<span data-ttu-id="a12fc-1070">現在のデータソースにリンクされているデータソースの FormDataSource.exeuteQuery メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1070">Calls the FormDataSource.exeuteQuery method on data sources that are linked to the current data source.</span></span>

```xpp
public void linkActive()
```

### <a name="remarks---linkactive"></a><span data-ttu-id="a12fc-1071">備考 - linkActive</span><span class="sxs-lookup"><span data-stu-id="a12fc-1071">Remarks - linkActive</span></span>

<span data-ttu-id="a12fc-1072">このメソッドは、ユーザーがマスター データ ソースの別のレコードに移動したときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1072">This method is executed when a user moves to another record in the master data source.</span></span> <span data-ttu-id="a12fc-1073">これにより、リンクされたすべてのデータ ソースが更新されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1073">This causes an update to all linked data sources.</span></span> <span data-ttu-id="a12fc-1074">親データ ソースの LinkType プロパティが Passive、Delayed、Active に設定されている場合、FormDataSource.active メソッドの super() 呼び出しは、リンクされたすべての子データ ソースで FormDataSource.linkActive メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1074">The super() call in the FormDataSource.active method calls the FormDataSource.linkActive method on all linked child data sources if the LinkType property on the parent data source is set to Passive, Delayed, or Active.</span></span> <span data-ttu-id="a12fc-1075">linkActive メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1075">The linkActive method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-1076">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] にポイントして [linkActive] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1076">Right-click the Methods node under the data source, point to Override Method, and then click linkActive.</span></span>

## <a name="method-selectionchanged"></a><span data-ttu-id="a12fc-1077">メソッド selectionChanged</span><span class="sxs-lookup"><span data-stu-id="a12fc-1077">Method selectionChanged</span></span>

```xpp
public void selectionChanged()
```

## <a name="method-ondeleting"></a><span data-ttu-id="a12fc-1078">メソッド OnDeleting</span><span class="sxs-lookup"><span data-stu-id="a12fc-1078">Method OnDeleting</span></span>

```xpp
private void OnDeleting([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---ondeleting"></a><span data-ttu-id="a12fc-1079">パラメーター - OnDeleting</span><span class="sxs-lookup"><span data-stu-id="a12fc-1079">Parameters - OnDeleting</span></span>

<span data-ttu-id="a12fc-1080">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-1080">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-1081">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-1081">e</span></span>  

## <a name="method-addreferencefieldtoselectionlist"></a><span data-ttu-id="a12fc-1082">メソッド addReferenceFieldToSelectionList</span><span class="sxs-lookup"><span data-stu-id="a12fc-1082">Method addReferenceFieldToSelectionList</span></span>

```xpp
public void addReferenceFieldToSelectionList(FieldId fieldId, str referenceFieldGroupName)
```

### <a name="parameters---addreferencefieldtoselectionlist"></a><span data-ttu-id="a12fc-1083">パラメーター - addReferenceFieldToSelectionList</span><span class="sxs-lookup"><span data-stu-id="a12fc-1083">Parameters - addReferenceFieldToSelectionList</span></span>

<span data-ttu-id="a12fc-1084">fieldId</span><span class="sxs-lookup"><span data-stu-id="a12fc-1084">fieldId</span></span>  

<!-- -->

<span data-ttu-id="a12fc-1085">referenceFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="a12fc-1085">referenceFieldGroupName</span></span>  

## <a name="method-initvalue"></a><span data-ttu-id="a12fc-1086">メソッド initValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-1086">Method initValue</span></span>

<span data-ttu-id="a12fc-1087">新しいレコードでフィールド値を初期化します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1087">Initializes field values in a new record.</span></span>

```xpp
public void initValue()
```

### <a name="remarks---initvalue"></a><span data-ttu-id="a12fc-1088">備考 - initValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-1088">Remarks - initValue</span></span>

<span data-ttu-id="a12fc-1089">このメソッドは、新しいレコードが作成されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1089">This method is called when a new record is created.</span></span> <span data-ttu-id="a12fc-1090">これはフィールドの初期値をレコードに入力します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1090">It populates the record with initial values for the fields.</span></span> <span data-ttu-id="a12fc-1091">initValue メソッドは、データソースの下にある [メソッド ノード] を右クリックし、[メソッドの上書き] をポイントしてから、[initValue] をクリックして、フォーム データ ソース上で上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1091">The initValue method can be overridden on a form data source by right-clicking the Methods node under the data source, pointing to Override Method, and then clicking initValue.</span></span>

### <a name="examples---initvalue"></a><span data-ttu-id="a12fc-1092">例 - initValue</span><span class="sxs-lookup"><span data-stu-id="a12fc-1092">Examples - initValue</span></span>

<span data-ttu-id="a12fc-1093">次の例では、TaxLimitBase フィールドが特定の値で初期化されるように FormDataSource.initValue を上書きします。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1093">The following example overrides FormDataSource.initValue so that the TaxLimitBase field is initialized with a particular value.</span></span>

```xpp
public void initValue() 
{ 
    super(); 
    taxTable.TaxLimitBase = TaxLimitBase::InvoiceWithoutVAT; 
}
```

## <a name="method-deletemarked"></a><span data-ttu-id="a12fc-1094">メソッド deleteMarked</span><span class="sxs-lookup"><span data-stu-id="a12fc-1094">Method deleteMarked</span></span>

<span data-ttu-id="a12fc-1095">マークされた (選択された) すべてのレコードをデータソースから削除します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1095">Deletes all marked (selected) records from a data source.</span></span>

```xpp
public void deleteMarked()
```

### <a name="remarks---deletemarked"></a><span data-ttu-id="a12fc-1096">備考 - deleteMarked</span><span class="sxs-lookup"><span data-stu-id="a12fc-1096">Remarks - deleteMarked</span></span>

<span data-ttu-id="a12fc-1097">レコードが選択されていない場合は、FormDataSource.delete メソッドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1097">If no records have been selected, the FormDataSource.delete method is executed.</span></span> <span data-ttu-id="a12fc-1098">Ctrl + Break キーを押すと、操作が中断されます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1098">The operation can be interrupted by pressing CTRL+BREAK.</span></span> <span data-ttu-id="a12fc-1099">deleteMarked メソッドは、フォーム データ ソースで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1099">The deleteMarked method can be overridden on a form data source.</span></span> <span data-ttu-id="a12fc-1100">データのソースの下のメソッド ノードを右クリックし、[オーバーライド メソッド] &gt; [deleteMarked] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1100">Right-click the Methods node under the data source, and then select Override Method &gt; deleteMarked.</span></span>

### <a name="examples---deletemarked"></a><span data-ttu-id="a12fc-1101">例 - deleteMarked</span><span class="sxs-lookup"><span data-stu-id="a12fc-1101">Examples - deleteMarked</span></span>

<span data-ttu-id="a12fc-1102">次の例では、deleteMarked メソッドを上書きして、マークされたレコードを削除するかどうかをユーザーに確認させます。</span><span class="sxs-lookup"><span data-stu-id="a12fc-1102">The following example overrides the deleteMarked method to let users confirm whether they want to delete the marked records.</span></span>

```xpp
public void deleteMarked() 
{ 
    if (Box::yesNo("@SYS79428", DialogButton::Yes, "@SYS79319")) 
        super(); 
}
```

## <a name="method-onleavingrecord"></a><span data-ttu-id="a12fc-1103">メソッド OnLeavingRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-1103">Method OnLeavingRecord</span></span>

```xpp
private void OnLeavingRecord([FormDataSource sender], [FormDataSourceEventArgs e])
```

### <a name="parameters---onleavingrecord"></a><span data-ttu-id="a12fc-1104">パラメーター - OnLeavingRecord</span><span class="sxs-lookup"><span data-stu-id="a12fc-1104">Parameters - OnLeavingRecord</span></span>

<span data-ttu-id="a12fc-1105">sender</span><span class="sxs-lookup"><span data-stu-id="a12fc-1105">sender</span></span>  

<!-- -->

<span data-ttu-id="a12fc-1106">e</span><span class="sxs-lookup"><span data-stu-id="a12fc-1106">e</span></span>  

