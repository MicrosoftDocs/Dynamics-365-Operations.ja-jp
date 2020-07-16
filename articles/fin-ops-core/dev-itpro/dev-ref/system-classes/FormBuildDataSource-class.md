---
title: FormBuildDataSource クラス
description: このトピックでは、FormBuildDataSource クラスについて説明します。
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
ms.openlocfilehash: c90d337d4b017e616e25893a1de3d7ceb542bcb7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502969"
---
# <a name="class-formbuilddatasource"></a><span data-ttu-id="ac2c7-103">クラス FormBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-103">Class FormBuildDataSource</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildDataSource extends FormBuildObjectSet
```

<span data-ttu-id="ac2c7-104">FormBuildDataSource クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-104">The FormBuildDataSource class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac2c7-105">備考</span><span class="sxs-lookup"><span data-stu-id="ac2c7-105">Remarks</span></span>

<span data-ttu-id="ac2c7-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="ac2c7-107">例</span><span class="sxs-lookup"><span data-stu-id="ac2c7-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ac2c7-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="ac2c7-108">Methods</span></span>

| <span data-ttu-id="ac2c7-109">方法</span><span class="sxs-lookup"><span data-stu-id="ac2c7-109">Method</span></span>                                                                            | <span data-ttu-id="ac2c7-110">説明</span><span class="sxs-lookup"><span data-stu-id="ac2c7-110">Description</span></span>                                                                                                               |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2c7-111">public FormBuildDataSource addReferenceDataSource(str name, \[str joinRelation\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-111">public FormBuildDataSource addReferenceDataSource(str name, \[str joinRelation\])</span></span> |                                                                                                                           |
| <span data-ttu-id="ac2c7-112">public boolean allowCheck(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-112">public boolean allowCheck(\[boolean value\])</span></span>                                      |                                                                                                                           |
| <span data-ttu-id="ac2c7-113">public boolean allowCreate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-113">public boolean allowCreate(\[boolean value\])</span></span>                                     |                                                                                                                           |
| <span data-ttu-id="ac2c7-114">public boolean allowDeferredLoad(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-114">public boolean allowDeferredLoad(\[boolean value\])</span></span>                               |                                                                                                                           |
| <span data-ttu-id="ac2c7-115">public boolean allowDelete(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-115">public boolean allowDelete(\[boolean value\])</span></span>                                     |                                                                                                                           |
| <span data-ttu-id="ac2c7-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-116">public boolean allowEdit(\[boolean value\])</span></span>                                       | <span data-ttu-id="ac2c7-117">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-117">Determines whether the user can change the contents of the control.</span></span>                                                       |
| <span data-ttu-id="ac2c7-118">public boolean autoNotify(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-118">public boolean autoNotify(\[boolean value\])</span></span>                                      |                                                                                                                           |
| <span data-ttu-id="ac2c7-119">public boolean autoQuery(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-119">public boolean autoQuery(\[boolean value\])</span></span>                                       |                                                                                                                           |
| <span data-ttu-id="ac2c7-120">public boolean autoSearch(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-120">public boolean autoSearch(\[boolean value\])</span></span>                                      |                                                                                                                           |
| <span data-ttu-id="ac2c7-121">public FormBuildDataSource baseDataSource()</span><span class="sxs-lookup"><span data-stu-id="ac2c7-121">public FormBuildDataSource baseDataSource()</span></span>                                       |                                                                                                                           |
| <span data-ttu-id="ac2c7-122">public str company(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-122">public str company(\[str value\])</span></span>                                                 |                                                                                                                           |
| <span data-ttu-id="ac2c7-123">public FieldId counterField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-123">public FieldId counterField(\[FieldId value\])</span></span>                                    |                                                                                                                           |
| <span data-ttu-id="ac2c7-124">public boolean crossCompanyAutoQuery(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-124">public boolean crossCompanyAutoQuery(\[boolean value\])</span></span>                           |                                                                                                                           |
| <span data-ttu-id="ac2c7-125">public boolean delayActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-125">public boolean delayActive(\[boolean value\])</span></span>                                     |                                                                                                                           |
| <span data-ttu-id="ac2c7-126">public int extends(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-126">public int extends(\[AnyType value\])</span></span>                                             |                                                                                                                           |
| <span data-ttu-id="ac2c7-127">public str GetXppILImplementation()</span><span class="sxs-lookup"><span data-stu-id="ac2c7-127">public str GetXppILImplementation()</span></span>                                               |                                                                                                                           |
| <span data-ttu-id="ac2c7-128">public IndexId index(\[IndexId value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-128">public IndexId index(\[IndexId value\])</span></span>                                           |                                                                                                                           |
| <span data-ttu-id="ac2c7-129">public boolean insertAtEnd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-129">public boolean insertAtEnd(\[boolean value\])</span></span>                                     |                                                                                                                           |
| <span data-ttu-id="ac2c7-130">public boolean insertIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-130">public boolean insertIfEmpty(\[boolean value\])</span></span>                                   |                                                                                                                           |
| <span data-ttu-id="ac2c7-131">public boolean isBaseDataSource()</span><span class="sxs-lookup"><span data-stu-id="ac2c7-131">public boolean isBaseDataSource()</span></span>                                                 |                                                                                                                           |
| <span data-ttu-id="ac2c7-132">public boolean isInheritanceDataSource()</span><span class="sxs-lookup"><span data-stu-id="ac2c7-132">public boolean isInheritanceDataSource()</span></span>                                          |                                                                                                                           |
| <span data-ttu-id="ac2c7-133">public boolean isMasterDataSource()</span><span class="sxs-lookup"><span data-stu-id="ac2c7-133">public boolean isMasterDataSource()</span></span>                                               |                                                                                                                           |
| <span data-ttu-id="ac2c7-134">public str joinRelation(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-134">public str joinRelation(\[str value\])</span></span>                                            |                                                                                                                           |
| <span data-ttu-id="ac2c7-135">public int joinSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-135">public int joinSource(\[AnyType value\])</span></span>                                          |                                                                                                                           |
| <span data-ttu-id="ac2c7-136">public int linkType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-136">public int linkType(\[int value\])</span></span>                                                |                                                                                                                           |
| <span data-ttu-id="ac2c7-137">public FormBuildDataSource masterDataSource()</span><span class="sxs-lookup"><span data-stu-id="ac2c7-137">public FormBuildDataSource masterDataSource()</span></span>                                     |                                                                                                                           |
| <span data-ttu-id="ac2c7-138">public int maxAccessRight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-138">public int maxAccessRight(\[int value\])</span></span>                                          |                                                                                                                           |
| <span data-ttu-id="ac2c7-139">public int maxRecordsToLoad(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-139">public int maxRecordsToLoad(\[int value\])</span></span>                                        |                                                                                                                           |
| <span data-ttu-id="ac2c7-140">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-140">public str name(\[str value\])</span></span>                                                    | <span data-ttu-id="ac2c7-141">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-141">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span> |
| <span data-ttu-id="ac2c7-142">public boolean onlyFetchActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-142">public boolean onlyFetchActive(\[boolean value\])</span></span>                                 |                                                                                                                           |
| <span data-ttu-id="ac2c7-143">public int optionalRecordMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-143">public int optionalRecordMode(\[int value\])</span></span>                                      |                                                                                                                           |
| <span data-ttu-id="ac2c7-144">public int startPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-144">public int startPosition(\[int value\])</span></span>                                           |                                                                                                                           |
| <span data-ttu-id="ac2c7-145">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-145">public TableId table(\[TableId value\])</span></span>                                           | <span data-ttu-id="ac2c7-146">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-146">Gets or sets the table ID associated with the object.</span></span>                                                                     |
| <span data-ttu-id="ac2c7-147">public int validTimeStateAutoQuery(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-147">public int validTimeStateAutoQuery(\[int value\])</span></span>                                 |                                                                                                                           |
| <span data-ttu-id="ac2c7-148">public int validTimeStateUpdate(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ac2c7-148">public int validTimeStateUpdate(\[int value\])</span></span>                                    |                                                                                                                           |
| <span data-ttu-id="ac2c7-149">public void RegisterXppDataFieldILImplementation(str fieldName, str className)</span><span class="sxs-lookup"><span data-stu-id="ac2c7-149">public void RegisterXppDataFieldILImplementation(str fieldName, str className)</span></span>    |                                                                                                                           |
| <span data-ttu-id="ac2c7-150">public void RegisterXppILImplementation(str className)</span><span class="sxs-lookup"><span data-stu-id="ac2c7-150">public void RegisterXppILImplementation(str className)</span></span>                            |                                                                                                                           |
| <span data-ttu-id="ac2c7-151">public void SetDataLinkType(QueryDataLinkType linkType, str parentDataSource)</span><span class="sxs-lookup"><span data-stu-id="ac2c7-151">public void SetDataLinkType(QueryDataLinkType linkType, str parentDataSource)</span></span>     |                                                                                                                           |

## <a name="method-addreferencedatasource"></a><span data-ttu-id="ac2c7-152">メソッド addReferenceDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-152">Method addReferenceDataSource</span></span>

```xpp
public FormBuildDataSource addReferenceDataSource(str name, [str joinRelation])
```

### <a name="parameters---addreferencedatasource"></a><span data-ttu-id="ac2c7-153">パラメーター - addReferenceDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-153">Parameters - addReferenceDataSource</span></span>

<span data-ttu-id="ac2c7-154">名前</span><span class="sxs-lookup"><span data-stu-id="ac2c7-154">name</span></span>  

<!-- -->

<span data-ttu-id="ac2c7-155">joinRelation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-155">joinRelation</span></span>  

### <a name="return-value---addreferencedatasource"></a><span data-ttu-id="ac2c7-156">戻り値 - addReferenceDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-156">Return Value - addReferenceDataSource</span></span>

## <a name="method-allowcheck"></a><span data-ttu-id="ac2c7-157">メソッド allowCheck</span><span class="sxs-lookup"><span data-stu-id="ac2c7-157">Method allowCheck</span></span>

```xpp
public boolean allowCheck([boolean value])
```

### <a name="parameters---allowcheck"></a><span data-ttu-id="ac2c7-158">パラメーター - allowCheck</span><span class="sxs-lookup"><span data-stu-id="ac2c7-158">Parameters - allowCheck</span></span>

<span data-ttu-id="ac2c7-159">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-159">value</span></span>  

### <a name="return-value---allowcheck"></a><span data-ttu-id="ac2c7-160">戻り値 - allowCheck</span><span class="sxs-lookup"><span data-stu-id="ac2c7-160">Return Value - allowCheck</span></span>

## <a name="method-allowcreate"></a><span data-ttu-id="ac2c7-161">メソッド allowCreate</span><span class="sxs-lookup"><span data-stu-id="ac2c7-161">Method allowCreate</span></span>

```xpp
public boolean allowCreate([boolean value])
```

### <a name="parameters---allowcreate"></a><span data-ttu-id="ac2c7-162">パラメーター - allowCreate</span><span class="sxs-lookup"><span data-stu-id="ac2c7-162">Parameters - allowCreate</span></span>

<span data-ttu-id="ac2c7-163">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-163">value</span></span>  

### <a name="return-value---allowcreate"></a><span data-ttu-id="ac2c7-164">戻り値 - allowCreate</span><span class="sxs-lookup"><span data-stu-id="ac2c7-164">Return Value - allowCreate</span></span>

## <a name="method-allowdeferredload"></a><span data-ttu-id="ac2c7-165">メソッド allowDeferredLoad</span><span class="sxs-lookup"><span data-stu-id="ac2c7-165">Method allowDeferredLoad</span></span>

```xpp
public boolean allowDeferredLoad([boolean value])
```

### <a name="parameters---allowdeferredload"></a><span data-ttu-id="ac2c7-166">パラメーター - allowDeferredLoad</span><span class="sxs-lookup"><span data-stu-id="ac2c7-166">Parameters - allowDeferredLoad</span></span>

<span data-ttu-id="ac2c7-167">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-167">value</span></span>  

### <a name="return-value---allowdeferredload"></a><span data-ttu-id="ac2c7-168">戻り値 - allowDeferredLoad</span><span class="sxs-lookup"><span data-stu-id="ac2c7-168">Return Value - allowDeferredLoad</span></span>

## <a name="method-allowdelete"></a><span data-ttu-id="ac2c7-169">メソッド allowDelete</span><span class="sxs-lookup"><span data-stu-id="ac2c7-169">Method allowDelete</span></span>

```xpp
public boolean allowDelete([boolean value])
```

### <a name="parameters---allowdelete"></a><span data-ttu-id="ac2c7-170">パラメーター - allowDelete</span><span class="sxs-lookup"><span data-stu-id="ac2c7-170">Parameters - allowDelete</span></span>

<span data-ttu-id="ac2c7-171">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-171">value</span></span>  

### <a name="return-value---allowdelete"></a><span data-ttu-id="ac2c7-172">戻り値 - allowDelete</span><span class="sxs-lookup"><span data-stu-id="ac2c7-172">Return Value - allowDelete</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="ac2c7-173">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="ac2c7-173">Method allowEdit</span></span>

<span data-ttu-id="ac2c7-174">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-174">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="ac2c7-175">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ac2c7-175">Parameters - allowEdit</span></span>

<span data-ttu-id="ac2c7-176">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-176">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="ac2c7-177">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ac2c7-177">Return Value - allowEdit</span></span>

<span data-ttu-id="ac2c7-178">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-178">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="ac2c7-179">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="ac2c7-179">Remarks - allowEdit</span></span>

<span data-ttu-id="ac2c7-180">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-180">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autonotify"></a><span data-ttu-id="ac2c7-181">メソッド autoNotify</span><span class="sxs-lookup"><span data-stu-id="ac2c7-181">Method autoNotify</span></span>

```xpp
public boolean autoNotify([boolean value])
```

### <a name="parameters---autonotify"></a><span data-ttu-id="ac2c7-182">パラメーター - autoNotify</span><span class="sxs-lookup"><span data-stu-id="ac2c7-182">Parameters - autoNotify</span></span>

<span data-ttu-id="ac2c7-183">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-183">value</span></span>  

### <a name="return-value---autonotify"></a><span data-ttu-id="ac2c7-184">戻り値 - autoNotify</span><span class="sxs-lookup"><span data-stu-id="ac2c7-184">Return Value - autoNotify</span></span>

## <a name="method-autoquery"></a><span data-ttu-id="ac2c7-185">メソッド autoQuery</span><span class="sxs-lookup"><span data-stu-id="ac2c7-185">Method autoQuery</span></span>

```xpp
public boolean autoQuery([boolean value])
```

### <a name="parameters---autoquery"></a><span data-ttu-id="ac2c7-186">パラメーター - autoQuery</span><span class="sxs-lookup"><span data-stu-id="ac2c7-186">Parameters - autoQuery</span></span>

<span data-ttu-id="ac2c7-187">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-187">value</span></span>  

### <a name="return-value---autoquery"></a><span data-ttu-id="ac2c7-188">戻り値 - autoQuery</span><span class="sxs-lookup"><span data-stu-id="ac2c7-188">Return Value - autoQuery</span></span>

## <a name="method-autosearch"></a><span data-ttu-id="ac2c7-189">メソッド autoSearch</span><span class="sxs-lookup"><span data-stu-id="ac2c7-189">Method autoSearch</span></span>

```xpp
public boolean autoSearch([boolean value])
```

### <a name="parameters---autosearch"></a><span data-ttu-id="ac2c7-190">パラメーター - autoSearch</span><span class="sxs-lookup"><span data-stu-id="ac2c7-190">Parameters - autoSearch</span></span>

<span data-ttu-id="ac2c7-191">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-191">value</span></span>  

### <a name="return-value---autosearch"></a><span data-ttu-id="ac2c7-192">戻り値 - autoSearch</span><span class="sxs-lookup"><span data-stu-id="ac2c7-192">Return Value - autoSearch</span></span>

## <a name="method-basedatasource"></a><span data-ttu-id="ac2c7-193">メソッド baseDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-193">Method baseDataSource</span></span>

```xpp
public FormBuildDataSource baseDataSource()
```

### <a name="return-value---basedatasource"></a><span data-ttu-id="ac2c7-194">戻り値 - baseDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-194">Return Value - baseDataSource</span></span>

## <a name="method-company"></a><span data-ttu-id="ac2c7-195">メソッド company</span><span class="sxs-lookup"><span data-stu-id="ac2c7-195">Method company</span></span>

```xpp
public str company([str value])
```

### <a name="parameters---company"></a><span data-ttu-id="ac2c7-196">パラメーター - company</span><span class="sxs-lookup"><span data-stu-id="ac2c7-196">Parameters - company</span></span>

<span data-ttu-id="ac2c7-197">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-197">value</span></span>  

### <a name="return-value---company"></a><span data-ttu-id="ac2c7-198">戻り値 - company</span><span class="sxs-lookup"><span data-stu-id="ac2c7-198">Return Value - company</span></span>

## <a name="method-counterfield"></a><span data-ttu-id="ac2c7-199">メソッド counterField</span><span class="sxs-lookup"><span data-stu-id="ac2c7-199">Method counterField</span></span>

```xpp
public FieldId counterField([FieldId value])
```

### <a name="parameters---counterfield"></a><span data-ttu-id="ac2c7-200">パラメーター - counterField</span><span class="sxs-lookup"><span data-stu-id="ac2c7-200">Parameters - counterField</span></span>

<span data-ttu-id="ac2c7-201">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-201">value</span></span>  

### <a name="return-value---counterfield"></a><span data-ttu-id="ac2c7-202">戻り値 - counterField</span><span class="sxs-lookup"><span data-stu-id="ac2c7-202">Return Value - counterField</span></span>

## <a name="method-crosscompanyautoquery"></a><span data-ttu-id="ac2c7-203">メソッド crossCompanyAutoQuery</span><span class="sxs-lookup"><span data-stu-id="ac2c7-203">Method crossCompanyAutoQuery</span></span>

```xpp
public boolean crossCompanyAutoQuery([boolean value])
```

### <a name="parameters---crosscompanyautoquery"></a><span data-ttu-id="ac2c7-204">パラメーター - crossCompanyAutoQuery</span><span class="sxs-lookup"><span data-stu-id="ac2c7-204">Parameters - crossCompanyAutoQuery</span></span>

<span data-ttu-id="ac2c7-205">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-205">value</span></span>  

### <a name="return-value---crosscompanyautoquery"></a><span data-ttu-id="ac2c7-206">戻り値 - crossCompanyAutoQuery</span><span class="sxs-lookup"><span data-stu-id="ac2c7-206">Return Value - crossCompanyAutoQuery</span></span>

## <a name="method-delayactive"></a><span data-ttu-id="ac2c7-207">メソッド delayActive</span><span class="sxs-lookup"><span data-stu-id="ac2c7-207">Method delayActive</span></span>

```xpp
public boolean delayActive([boolean value])
```

### <a name="parameters---delayactive"></a><span data-ttu-id="ac2c7-208">パラメーター - delayActive</span><span class="sxs-lookup"><span data-stu-id="ac2c7-208">Parameters - delayActive</span></span>

<span data-ttu-id="ac2c7-209">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-209">value</span></span>  

### <a name="return-value---delayactive"></a><span data-ttu-id="ac2c7-210">戻り値 - delayActive</span><span class="sxs-lookup"><span data-stu-id="ac2c7-210">Return Value - delayActive</span></span>

## <a name="method-extends"></a><span data-ttu-id="ac2c7-211">メソッド extends</span><span class="sxs-lookup"><span data-stu-id="ac2c7-211">Method extends</span></span>

```xpp
public int extends([AnyType value])
```

### <a name="parameters---extends"></a><span data-ttu-id="ac2c7-212">パラメーター - extends</span><span class="sxs-lookup"><span data-stu-id="ac2c7-212">Parameters - extends</span></span>

<span data-ttu-id="ac2c7-213">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-213">value</span></span>  

### <a name="return-value---extends"></a><span data-ttu-id="ac2c7-214">戻り値 - extends</span><span class="sxs-lookup"><span data-stu-id="ac2c7-214">Return Value - extends</span></span>

## <a name="method-getxppilimplementation"></a><span data-ttu-id="ac2c7-215">メソッド GetXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-215">Method GetXppILImplementation</span></span>

```xpp
public str GetXppILImplementation()
```

### <a name="return-value---getxppilimplementation"></a><span data-ttu-id="ac2c7-216">戻り値 - GetXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-216">Return Value - GetXppILImplementation</span></span>

## <a name="method-index"></a><span data-ttu-id="ac2c7-217">メソッド index</span><span class="sxs-lookup"><span data-stu-id="ac2c7-217">Method index</span></span>

```xpp
public IndexId index([IndexId value])
```

### <a name="parameters---index"></a><span data-ttu-id="ac2c7-218">パラメーター - index</span><span class="sxs-lookup"><span data-stu-id="ac2c7-218">Parameters - index</span></span>

<span data-ttu-id="ac2c7-219">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-219">value</span></span>  

### <a name="return-value---index"></a><span data-ttu-id="ac2c7-220">戻り値 - index</span><span class="sxs-lookup"><span data-stu-id="ac2c7-220">Return Value - index</span></span>

## <a name="method-insertatend"></a><span data-ttu-id="ac2c7-221">メソッド insertAtEnd</span><span class="sxs-lookup"><span data-stu-id="ac2c7-221">Method insertAtEnd</span></span>

```xpp
public boolean insertAtEnd([boolean value])
```

### <a name="parameters---insertatend"></a><span data-ttu-id="ac2c7-222">パラメーター - insertAtEnd</span><span class="sxs-lookup"><span data-stu-id="ac2c7-222">Parameters - insertAtEnd</span></span>

<span data-ttu-id="ac2c7-223">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-223">value</span></span>  

### <a name="return-value---insertatend"></a><span data-ttu-id="ac2c7-224">戻り値 - insertAtEnd</span><span class="sxs-lookup"><span data-stu-id="ac2c7-224">Return Value - insertAtEnd</span></span>

## <a name="method-insertifempty"></a><span data-ttu-id="ac2c7-225">メソッド insertIfEmpty</span><span class="sxs-lookup"><span data-stu-id="ac2c7-225">Method insertIfEmpty</span></span>

```xpp
public boolean insertIfEmpty([boolean value])
```

### <a name="parameters---insertifempty"></a><span data-ttu-id="ac2c7-226">パラメーター - insertIfEmpty</span><span class="sxs-lookup"><span data-stu-id="ac2c7-226">Parameters - insertIfEmpty</span></span>

<span data-ttu-id="ac2c7-227">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-227">value</span></span>  

### <a name="return-value---insertifempty"></a><span data-ttu-id="ac2c7-228">戻り値 - insertIfEmpty</span><span class="sxs-lookup"><span data-stu-id="ac2c7-228">Return Value - insertIfEmpty</span></span>

## <a name="method-isbasedatasource"></a><span data-ttu-id="ac2c7-229">メソッド isBaseDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-229">Method isBaseDataSource</span></span>

```xpp
public boolean isBaseDataSource()
```

### <a name="return-value---isbasedatasource"></a><span data-ttu-id="ac2c7-230">戻り値 - isBaseDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-230">Return Value - isBaseDataSource</span></span>

## <a name="method-isinheritancedatasource"></a><span data-ttu-id="ac2c7-231">メソッド isInheritanceDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-231">Method isInheritanceDataSource</span></span>

```xpp
public boolean isInheritanceDataSource()
```

### <a name="return-value---isinheritancedatasource"></a><span data-ttu-id="ac2c7-232">戻り値 - isInheritanceDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-232">Return Value - isInheritanceDataSource</span></span>

## <a name="method-ismasterdatasource"></a><span data-ttu-id="ac2c7-233">メソッド isMasterDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-233">Method isMasterDataSource</span></span>

```xpp
public boolean isMasterDataSource()
```

### <a name="return-value---ismasterdatasource"></a><span data-ttu-id="ac2c7-234">戻り値 - isMasterDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-234">Return Value - isMasterDataSource</span></span>

## <a name="method-joinrelation"></a><span data-ttu-id="ac2c7-235">メソッド joinRelation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-235">Method joinRelation</span></span>

```xpp
public str joinRelation([str value])
```

### <a name="parameters---joinrelation"></a><span data-ttu-id="ac2c7-236">パラメーター - joinRelation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-236">Parameters - joinRelation</span></span>

<span data-ttu-id="ac2c7-237">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-237">value</span></span>  

### <a name="return-value---joinrelation"></a><span data-ttu-id="ac2c7-238">戻り値 - joinRelation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-238">Return Value - joinRelation</span></span>

## <a name="method-joinsource"></a><span data-ttu-id="ac2c7-239">メソッド joinSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-239">Method joinSource</span></span>

```xpp
public int joinSource([AnyType value])
```

### <a name="parameters---joinsource"></a><span data-ttu-id="ac2c7-240">パラメーター - joinSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-240">Parameters - joinSource</span></span>

<span data-ttu-id="ac2c7-241">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-241">value</span></span>  

### <a name="return-value---joinsource"></a><span data-ttu-id="ac2c7-242">戻り値 - joinSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-242">Return Value - joinSource</span></span>

## <a name="method-linktype"></a><span data-ttu-id="ac2c7-243">メソッド linkType</span><span class="sxs-lookup"><span data-stu-id="ac2c7-243">Method linkType</span></span>

```xpp
public int linkType([int value])
```

### <a name="parameters---linktype"></a><span data-ttu-id="ac2c7-244">パラメーター - linkType</span><span class="sxs-lookup"><span data-stu-id="ac2c7-244">Parameters - linkType</span></span>

<span data-ttu-id="ac2c7-245">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-245">value</span></span>  

### <a name="return-value---linktype"></a><span data-ttu-id="ac2c7-246">戻り値 - linkType</span><span class="sxs-lookup"><span data-stu-id="ac2c7-246">Return Value - linkType</span></span>

## <a name="method-masterdatasource"></a><span data-ttu-id="ac2c7-247">メソッド masterDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-247">Method masterDataSource</span></span>

```xpp
public FormBuildDataSource masterDataSource()
```

### <a name="return-value---masterdatasource"></a><span data-ttu-id="ac2c7-248">戻り値 - masterDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-248">Return Value - masterDataSource</span></span>

## <a name="method-maxaccessright"></a><span data-ttu-id="ac2c7-249">メソッド maxAccessRight</span><span class="sxs-lookup"><span data-stu-id="ac2c7-249">Method maxAccessRight</span></span>

```xpp
public int maxAccessRight([int value])
```

### <a name="parameters---maxaccessright"></a><span data-ttu-id="ac2c7-250">パラメーター - maxAccessRight</span><span class="sxs-lookup"><span data-stu-id="ac2c7-250">Parameters - maxAccessRight</span></span>

<span data-ttu-id="ac2c7-251">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-251">value</span></span>  

### <a name="return-value---maxaccessright"></a><span data-ttu-id="ac2c7-252">戻り値 - maxAccessRight</span><span class="sxs-lookup"><span data-stu-id="ac2c7-252">Return Value - maxAccessRight</span></span>

## <a name="method-maxrecordstoload"></a><span data-ttu-id="ac2c7-253">メソッド maxRecordsToLoad</span><span class="sxs-lookup"><span data-stu-id="ac2c7-253">Method maxRecordsToLoad</span></span>

```xpp
public int maxRecordsToLoad([int value])
```

### <a name="parameters---maxrecordstoload"></a><span data-ttu-id="ac2c7-254">パラメーター - maxRecordsToLoad</span><span class="sxs-lookup"><span data-stu-id="ac2c7-254">Parameters - maxRecordsToLoad</span></span>

<span data-ttu-id="ac2c7-255">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-255">value</span></span>  

### <a name="return-value---maxrecordstoload"></a><span data-ttu-id="ac2c7-256">戻り値 - maxRecordsToLoad</span><span class="sxs-lookup"><span data-stu-id="ac2c7-256">Return Value - maxRecordsToLoad</span></span>

## <a name="method-name"></a><span data-ttu-id="ac2c7-257">メソッド名</span><span class="sxs-lookup"><span data-stu-id="ac2c7-257">Method name</span></span>

<span data-ttu-id="ac2c7-258">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-258">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="ac2c7-259">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="ac2c7-259">Parameters - name</span></span>

<span data-ttu-id="ac2c7-260">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-260">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="ac2c7-261">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="ac2c7-261">Return Value - name</span></span>

<span data-ttu-id="ac2c7-262">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-262">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="ac2c7-263">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="ac2c7-263">Remarks - name</span></span>

<span data-ttu-id="ac2c7-264">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-264">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="ac2c7-265">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-265">Begins with a letter.</span></span>
-   <span data-ttu-id="ac2c7-266">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-266">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="ac2c7-267">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-267">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="ac2c7-268">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-268">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="ac2c7-269">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-269">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-onlyfetchactive"></a><span data-ttu-id="ac2c7-270">メソッド onlyFetchActive</span><span class="sxs-lookup"><span data-stu-id="ac2c7-270">Method onlyFetchActive</span></span>

```xpp
public boolean onlyFetchActive([boolean value])
```

### <a name="parameters---onlyfetchactive"></a><span data-ttu-id="ac2c7-271">パラメーター - onlyFetchActive</span><span class="sxs-lookup"><span data-stu-id="ac2c7-271">Parameters - onlyFetchActive</span></span>

<span data-ttu-id="ac2c7-272">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-272">value</span></span>  

### <a name="return-value---onlyfetchactive"></a><span data-ttu-id="ac2c7-273">戻り値 - onlyFetchActive</span><span class="sxs-lookup"><span data-stu-id="ac2c7-273">Return Value - onlyFetchActive</span></span>

## <a name="method-optionalrecordmode"></a><span data-ttu-id="ac2c7-274">メソッド optionalRecordMode</span><span class="sxs-lookup"><span data-stu-id="ac2c7-274">Method optionalRecordMode</span></span>

```xpp
public int optionalRecordMode([int value])
```

### <a name="parameters---optionalrecordmode"></a><span data-ttu-id="ac2c7-275">パラメーター - optionalRecordMode</span><span class="sxs-lookup"><span data-stu-id="ac2c7-275">Parameters - optionalRecordMode</span></span>

<span data-ttu-id="ac2c7-276">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-276">value</span></span>  

### <a name="return-value---optionalrecordmode"></a><span data-ttu-id="ac2c7-277">戻り値 - optionalRecordMode</span><span class="sxs-lookup"><span data-stu-id="ac2c7-277">Return Value - optionalRecordMode</span></span>

## <a name="method-startposition"></a><span data-ttu-id="ac2c7-278">メソッド startPosition</span><span class="sxs-lookup"><span data-stu-id="ac2c7-278">Method startPosition</span></span>

```xpp
public int startPosition([int value])
```

### <a name="parameters---startposition"></a><span data-ttu-id="ac2c7-279">パラメーター - startPosition</span><span class="sxs-lookup"><span data-stu-id="ac2c7-279">Parameters - startPosition</span></span>

<span data-ttu-id="ac2c7-280">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-280">value</span></span>  

### <a name="return-value---startposition"></a><span data-ttu-id="ac2c7-281">戻り値 - startPosition</span><span class="sxs-lookup"><span data-stu-id="ac2c7-281">Return Value - startPosition</span></span>

## <a name="method-table"></a><span data-ttu-id="ac2c7-282">メソッド table</span><span class="sxs-lookup"><span data-stu-id="ac2c7-282">Method table</span></span>

<span data-ttu-id="ac2c7-283">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-283">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="ac2c7-284">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="ac2c7-284">Parameters - table</span></span>

<span data-ttu-id="ac2c7-285">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-285">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="ac2c7-286">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="ac2c7-286">Return Value - table</span></span>

<span data-ttu-id="ac2c7-287">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="ac2c7-287">The current value of the table ID associated with the object.</span></span>

## <a name="method-validtimestateautoquery"></a><span data-ttu-id="ac2c7-288">メソッド validTimeStateAutoQuery</span><span class="sxs-lookup"><span data-stu-id="ac2c7-288">Method validTimeStateAutoQuery</span></span>

```xpp
public int validTimeStateAutoQuery([int value])
```

### <a name="parameters---validtimestateautoquery"></a><span data-ttu-id="ac2c7-289">パラメーター - validTimeStateAutoQuery</span><span class="sxs-lookup"><span data-stu-id="ac2c7-289">Parameters - validTimeStateAutoQuery</span></span>

<span data-ttu-id="ac2c7-290">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-290">value</span></span>  

### <a name="return-value---validtimestateautoquery"></a><span data-ttu-id="ac2c7-291">戻り値 - validTimeStateAutoQuery</span><span class="sxs-lookup"><span data-stu-id="ac2c7-291">Return Value - validTimeStateAutoQuery</span></span>

## <a name="method-validtimestateupdate"></a><span data-ttu-id="ac2c7-292">メソッド validTimeStateUpdate</span><span class="sxs-lookup"><span data-stu-id="ac2c7-292">Method validTimeStateUpdate</span></span>

```xpp
public int validTimeStateUpdate([int value])
```

### <a name="parameters---validtimestateupdate"></a><span data-ttu-id="ac2c7-293">パラメーター - validTimeStateUpdate</span><span class="sxs-lookup"><span data-stu-id="ac2c7-293">Parameters - validTimeStateUpdate</span></span>

<span data-ttu-id="ac2c7-294">値</span><span class="sxs-lookup"><span data-stu-id="ac2c7-294">value</span></span>  

### <a name="return-value---validtimestateupdate"></a><span data-ttu-id="ac2c7-295">戻り値 - validTimeStateUpdate</span><span class="sxs-lookup"><span data-stu-id="ac2c7-295">Return Value - validTimeStateUpdate</span></span>

## <a name="method-registerxppdatafieldilimplementation"></a><span data-ttu-id="ac2c7-296">メソッド RegisterXppDataFieldILImplementation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-296">Method RegisterXppDataFieldILImplementation</span></span>

```xpp
public void RegisterXppDataFieldILImplementation(str fieldName, str className)
```

### <a name="parameters---registerxppdatafieldilimplementation"></a><span data-ttu-id="ac2c7-297">パラメーター - RegisterXppDataFieldILImplementation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-297">Parameters - RegisterXppDataFieldILImplementation</span></span>

<span data-ttu-id="ac2c7-298">fieldName</span><span class="sxs-lookup"><span data-stu-id="ac2c7-298">fieldName</span></span>  

<!-- -->

<span data-ttu-id="ac2c7-299">className</span><span class="sxs-lookup"><span data-stu-id="ac2c7-299">className</span></span>  

## <a name="method-registerxppilimplementation"></a><span data-ttu-id="ac2c7-300">メソッド RegisterXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-300">Method RegisterXppILImplementation</span></span>

```xpp
public void RegisterXppILImplementation(str className)
```

### <a name="parameters---registerxppilimplementation"></a><span data-ttu-id="ac2c7-301">パラメーター - RegisterXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="ac2c7-301">Parameters - RegisterXppILImplementation</span></span>

<span data-ttu-id="ac2c7-302">className</span><span class="sxs-lookup"><span data-stu-id="ac2c7-302">className</span></span>  

## <a name="method-setdatalinktype"></a><span data-ttu-id="ac2c7-303">メソッド SetDataLinkType</span><span class="sxs-lookup"><span data-stu-id="ac2c7-303">Method SetDataLinkType</span></span>

```xpp
public void SetDataLinkType(QueryDataLinkType linkType, str parentDataSource)
```

### <a name="parameters---setdatalinktype"></a><span data-ttu-id="ac2c7-304">パラメーター - SetDataLinkType</span><span class="sxs-lookup"><span data-stu-id="ac2c7-304">Parameters - SetDataLinkType</span></span>

<span data-ttu-id="ac2c7-305">linkType</span><span class="sxs-lookup"><span data-stu-id="ac2c7-305">linkType</span></span>  

<!-- -->

<span data-ttu-id="ac2c7-306">parentDataSource</span><span class="sxs-lookup"><span data-stu-id="ac2c7-306">parentDataSource</span></span>  

