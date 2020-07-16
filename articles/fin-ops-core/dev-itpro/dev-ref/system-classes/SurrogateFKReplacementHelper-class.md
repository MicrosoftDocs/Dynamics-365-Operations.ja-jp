---
title: SurrogateFKReplacementHelper クラス
description: このトピックでは、SurrogateFKReplacementHelper クラスについて説明します。
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
ms.openlocfilehash: 4b6c3536299786bdc55177ed68e2ccd92332eb13
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502794"
---
# <a name="class-surrogatefkreplacementhelper"></a><span data-ttu-id="01d48-103">クラス SurrogateFKReplacementHelper</span><span class="sxs-lookup"><span data-stu-id="01d48-103">Class SurrogateFKReplacementHelper</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SurrogateFKReplacementHelper extends Object
```

## <a name="remarks"></a><span data-ttu-id="01d48-104">備考</span><span class="sxs-lookup"><span data-stu-id="01d48-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="01d48-105">例</span><span class="sxs-lookup"><span data-stu-id="01d48-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="01d48-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="01d48-106">Methods</span></span>

| <span data-ttu-id="01d48-107">方法</span><span class="sxs-lookup"><span data-stu-id="01d48-107">Method</span></span>                                                                                                                                                                                                             | <span data-ttu-id="01d48-108">説明</span><span class="sxs-lookup"><span data-stu-id="01d48-108">Description</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="01d48-109">public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)</span><span class="sxs-lookup"><span data-stu-id="01d48-109">public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)</span></span>                                                                                             |                                                 |
| <span data-ttu-id="01d48-110">public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)</span><span class="sxs-lookup"><span data-stu-id="01d48-110">public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)</span></span>                                                              |                                                 |
| <span data-ttu-id="01d48-111">public List displayBindings(str replacementFieldGroupName, \[boolean distinctBindingsOnly\])</span><span class="sxs-lookup"><span data-stu-id="01d48-111">public List displayBindings(str replacementFieldGroupName, \[boolean distinctBindingsOnly\])</span></span>                                                                                                                       |                                                 |
| <span data-ttu-id="01d48-112">public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\], \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span><span class="sxs-lookup"><span data-stu-id="01d48-112">public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\], \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span></span>                   |                                                 |
| <span data-ttu-id="01d48-113">public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span><span class="sxs-lookup"><span data-stu-id="01d48-113">public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span></span>                                                               |                                                 |
| <span data-ttu-id="01d48-114">public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span><span class="sxs-lookup"><span data-stu-id="01d48-114">public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span></span> |                                                 |
| <span data-ttu-id="01d48-115">public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, \[boolean isRootPrimaryKeyDataSource\])</span><span class="sxs-lookup"><span data-stu-id="01d48-115">public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, \[boolean isRootPrimaryKeyDataSource\])</span></span>                                                                                        |                                                 |
| <span data-ttu-id="01d48-116">public str extendedDataType()</span><span class="sxs-lookup"><span data-stu-id="01d48-116">public str extendedDataType()</span></span>                                                                                                                                                                                      |                                                 |
| <span data-ttu-id="01d48-117">public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)</span><span class="sxs-lookup"><span data-stu-id="01d48-117">public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)</span></span>                                                                                               |                                                 |
| <span data-ttu-id="01d48-118">public boolean isResolvedReferenceAmbiguous(Query query)</span><span class="sxs-lookup"><span data-stu-id="01d48-118">public boolean isResolvedReferenceAmbiguous(Query query)</span></span>                                                                                                                                                           |                                                 |
| <span data-ttu-id="01d48-119">public str primaryKeyTableName()</span><span class="sxs-lookup"><span data-stu-id="01d48-119">public str primaryKeyTableName()</span></span>                                                                                                                                                                                   |                                                 |
| <span data-ttu-id="01d48-120">public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\])</span><span class="sxs-lookup"><span data-stu-id="01d48-120">public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\])</span></span>                                                                                |                                                 |
| <span data-ttu-id="01d48-121">public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)</span><span class="sxs-lookup"><span data-stu-id="01d48-121">public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)</span></span>                                                     |                                                 |
| <span data-ttu-id="01d48-122">public Common resolveReference(Query query, \[boolean ignoreAmbiguousReference\])</span><span class="sxs-lookup"><span data-stu-id="01d48-122">public Common resolveReference(Query query, \[boolean ignoreAmbiguousReference\])</span></span>                                                                                                                                  |                                                 |
| <span data-ttu-id="01d48-123">public FieldBinding surrogateForeignKeyFieldBinding()</span><span class="sxs-lookup"><span data-stu-id="01d48-123">public FieldBinding surrogateForeignKeyFieldBinding()</span></span>                                                                                                                                                              |                                                 |
| <span data-ttu-id="01d48-124">::public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)</span><span class="sxs-lookup"><span data-stu-id="01d48-124">::public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)</span></span>                                                                                                                    |                                                 |
| <span data-ttu-id="01d48-125">::public static SurrogateFKReplacementHelper constructForEDT(str edtName)</span><span class="sxs-lookup"><span data-stu-id="01d48-125">::public static SurrogateFKReplacementHelper constructForEDT(str edtName)</span></span>                                                                                                                                          |                                                 |
| <span data-ttu-id="01d48-126">::public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)</span><span class="sxs-lookup"><span data-stu-id="01d48-126">::public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)</span></span>                                                                                                                                  |                                                 |
| <span data-ttu-id="01d48-127">::public static str defaultPrimaryKeyQueryDataSourceName()</span><span class="sxs-lookup"><span data-stu-id="01d48-127">::public static str defaultPrimaryKeyQueryDataSourceName()</span></span>                                                                                                                                                         |                                                 |
| <span data-ttu-id="01d48-128">::public static str DEPRECATED\_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)</span><span class="sxs-lookup"><span data-stu-id="01d48-128">::public static str DEPRECATED\_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)</span></span>                                                                                                                    |                                                 |
| <span data-ttu-id="01d48-129">::public static str implicitReplacementFieldGroupName()</span><span class="sxs-lookup"><span data-stu-id="01d48-129">::public static str implicitReplacementFieldGroupName()</span></span>                                                                                                                                                            |                                                 |
| <span data-ttu-id="01d48-130">private void new(FieldBinding surrogateForeignKeyBinding)</span><span class="sxs-lookup"><span data-stu-id="01d48-130">private void new(FieldBinding surrogateForeignKeyBinding)</span></span>                                                                                                                                                          | <span data-ttu-id="01d48-131">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="01d48-131">Initializes a new instance of the Object class.</span></span> |

## <a name="method-adddefaultrequiredjoins"></a><span data-ttu-id="01d48-132">メソッド addDefaultRequiredJoins</span><span class="sxs-lookup"><span data-stu-id="01d48-132">Method addDefaultRequiredJoins</span></span>

```xpp
public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)
```

### <a name="parameters---adddefaultrequiredjoins"></a><span data-ttu-id="01d48-133">パラメーター - addDefaultRequiredJoins</span><span class="sxs-lookup"><span data-stu-id="01d48-133">Parameters - addDefaultRequiredJoins</span></span>

<span data-ttu-id="01d48-134">foreignKeyQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="01d48-134">foreignKeyQueryBuildDataSource</span></span>  

<!-- -->

<span data-ttu-id="01d48-135">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-135">replacementFieldGroupName</span></span>  

### <a name="return-value---adddefaultrequiredjoins"></a><span data-ttu-id="01d48-136">戻り値 - addDefaultRequiredJoins</span><span class="sxs-lookup"><span data-stu-id="01d48-136">Return Value - addDefaultRequiredJoins</span></span>

## <a name="method-addrequiredjoins"></a><span data-ttu-id="01d48-137">メソッド addRequiredJoins</span><span class="sxs-lookup"><span data-stu-id="01d48-137">Method addRequiredJoins</span></span>

```xpp
public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)
```

### <a name="parameters---addrequiredjoins"></a><span data-ttu-id="01d48-138">パラメーター - addRequiredJoins</span><span class="sxs-lookup"><span data-stu-id="01d48-138">Parameters - addRequiredJoins</span></span>

<span data-ttu-id="01d48-139">requiredJoinsAsRelationPathList</span><span class="sxs-lookup"><span data-stu-id="01d48-139">requiredJoinsAsRelationPathList</span></span>  

<!-- -->

<span data-ttu-id="01d48-140">foreignKeyQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="01d48-140">foreignKeyQueryBuildDataSource</span></span>  

<!-- -->

<span data-ttu-id="01d48-141">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-141">replacementFieldGroupName</span></span>  

### <a name="return-value---addrequiredjoins"></a><span data-ttu-id="01d48-142">戻り値 - addRequiredJoins</span><span class="sxs-lookup"><span data-stu-id="01d48-142">Return Value - addRequiredJoins</span></span>

## <a name="method-displaybindings"></a><span data-ttu-id="01d48-143">メソッド displayBindings</span><span class="sxs-lookup"><span data-stu-id="01d48-143">Method displayBindings</span></span>

```xpp
public List displayBindings(str replacementFieldGroupName, [boolean distinctBindingsOnly])
```

### <a name="parameters---displaybindings"></a><span data-ttu-id="01d48-144">パラメーター - displayBindings</span><span class="sxs-lookup"><span data-stu-id="01d48-144">Parameters - displayBindings</span></span>

<span data-ttu-id="01d48-145">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-145">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="01d48-146">distinctBindingsOnly</span><span class="sxs-lookup"><span data-stu-id="01d48-146">distinctBindingsOnly</span></span>  

### <a name="return-value---displaybindings"></a><span data-ttu-id="01d48-147">戻り値 - displayBindings</span><span class="sxs-lookup"><span data-stu-id="01d48-147">Return Value - displayBindings</span></span>

## <a name="method-displayvaluesfromqueryrun"></a><span data-ttu-id="01d48-148">メソッド displayValuesFromQueryRun</span><span class="sxs-lookup"><span data-stu-id="01d48-148">Method displayValuesFromQueryRun</span></span>

```xpp
public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, [boolean isRootPrimaryKeyDataSource], [boolean trimSecuredValues], [boolean distinctBindingsOnly])
```

### <a name="parameters---displayvaluesfromqueryrun"></a><span data-ttu-id="01d48-149">パラメーター - displayValuesFromQueryRun</span><span class="sxs-lookup"><span data-stu-id="01d48-149">Parameters - displayValuesFromQueryRun</span></span>

<span data-ttu-id="01d48-150">queryRun</span><span class="sxs-lookup"><span data-stu-id="01d48-150">queryRun</span></span>  

<!-- -->

<span data-ttu-id="01d48-151">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-151">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="01d48-152">isRootPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="01d48-152">isRootPrimaryKeyDataSource</span></span>  

<!-- -->

<span data-ttu-id="01d48-153">trimSecuredValues</span><span class="sxs-lookup"><span data-stu-id="01d48-153">trimSecuredValues</span></span>  

<!-- -->

<span data-ttu-id="01d48-154">distinctBindingsOnly</span><span class="sxs-lookup"><span data-stu-id="01d48-154">distinctBindingsOnly</span></span>  

### <a name="return-value---displayvaluesfromqueryrun"></a><span data-ttu-id="01d48-155">戻り値 - displayValuesFromQueryRun</span><span class="sxs-lookup"><span data-stu-id="01d48-155">Return Value - displayValuesFromQueryRun</span></span>

## <a name="method-displayvaluesfromrecid"></a><span data-ttu-id="01d48-156">メソッド displayValuesFromRecID</span><span class="sxs-lookup"><span data-stu-id="01d48-156">Method displayValuesFromRecID</span></span>

```xpp
public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, [boolean trimSecuredValues], [boolean distinctBindingsOnly])
```

### <a name="parameters---displayvaluesfromrecid"></a><span data-ttu-id="01d48-157">パラメーター - displayValuesFromRecID</span><span class="sxs-lookup"><span data-stu-id="01d48-157">Parameters - displayValuesFromRecID</span></span>

<span data-ttu-id="01d48-158">recIDValue</span><span class="sxs-lookup"><span data-stu-id="01d48-158">recIDValue</span></span>  

<!-- -->

<span data-ttu-id="01d48-159">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-159">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="01d48-160">trimSecuredValues</span><span class="sxs-lookup"><span data-stu-id="01d48-160">trimSecuredValues</span></span>  

<!-- -->

<span data-ttu-id="01d48-161">distinctBindingsOnly</span><span class="sxs-lookup"><span data-stu-id="01d48-161">distinctBindingsOnly</span></span>  

### <a name="return-value---displayvaluesfromrecid"></a><span data-ttu-id="01d48-162">戻り値 - displayValuesFromRecID</span><span class="sxs-lookup"><span data-stu-id="01d48-162">Return Value - displayValuesFromRecID</span></span>

## <a name="method-displayvaluesfromrootds"></a><span data-ttu-id="01d48-163">メソッド displayValuesFromRootDS</span><span class="sxs-lookup"><span data-stu-id="01d48-163">Method displayValuesFromRootDS</span></span>

```xpp
public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, [boolean trimSecuredValues], [boolean distinctBindingsOnly])
```

### <a name="parameters---displayvaluesfromrootds"></a><span data-ttu-id="01d48-164">パラメーター - displayValuesFromRootDS</span><span class="sxs-lookup"><span data-stu-id="01d48-164">Parameters - displayValuesFromRootDS</span></span>

<span data-ttu-id="01d48-165">rootQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="01d48-165">rootQueryBuildDataSource</span></span>  

<!-- -->

<span data-ttu-id="01d48-166">isPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="01d48-166">isPrimaryKeyDataSource</span></span>  

<!-- -->

<span data-ttu-id="01d48-167">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-167">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="01d48-168">trimSecuredValues</span><span class="sxs-lookup"><span data-stu-id="01d48-168">trimSecuredValues</span></span>  

<!-- -->

<span data-ttu-id="01d48-169">distinctBindingsOnly</span><span class="sxs-lookup"><span data-stu-id="01d48-169">distinctBindingsOnly</span></span>  

### <a name="return-value---displayvaluesfromrootds"></a><span data-ttu-id="01d48-170">戻り値 - displayValuesFromRootDS</span><span class="sxs-lookup"><span data-stu-id="01d48-170">Return Value - displayValuesFromRootDS</span></span>

## <a name="method-displayvalue"></a><span data-ttu-id="01d48-171">メソッド displayValue</span><span class="sxs-lookup"><span data-stu-id="01d48-171">Method displayValue</span></span>

```xpp
public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, [boolean isRootPrimaryKeyDataSource])
```

### <a name="parameters---displayvalue"></a><span data-ttu-id="01d48-172">パラメーター - displayValue</span><span class="sxs-lookup"><span data-stu-id="01d48-172">Parameters - displayValue</span></span>

<span data-ttu-id="01d48-173">resolvedCursor</span><span class="sxs-lookup"><span data-stu-id="01d48-173">resolvedCursor</span></span>  

<!-- -->

<span data-ttu-id="01d48-174">displayBinding</span><span class="sxs-lookup"><span data-stu-id="01d48-174">displayBinding</span></span>  

<!-- -->

<span data-ttu-id="01d48-175">isRootPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="01d48-175">isRootPrimaryKeyDataSource</span></span>  

### <a name="return-value---displayvalue"></a><span data-ttu-id="01d48-176">戻り値 - displayValue</span><span class="sxs-lookup"><span data-stu-id="01d48-176">Return Value - displayValue</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="01d48-177">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="01d48-177">Method extendedDataType</span></span>

```xpp
public str extendedDataType()
```

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="01d48-178">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="01d48-178">Return Value - extendedDataType</span></span>

## <a name="method-generateresolvereferencequery"></a><span data-ttu-id="01d48-179">メソッド generateResolveReferenceQuery</span><span class="sxs-lookup"><span data-stu-id="01d48-179">Method generateResolveReferenceQuery</span></span>

```xpp
public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)
```

### <a name="parameters---generateresolvereferencequery"></a><span data-ttu-id="01d48-180">パラメーター - generateResolveReferenceQuery</span><span class="sxs-lookup"><span data-stu-id="01d48-180">Parameters - generateResolveReferenceQuery</span></span>

<span data-ttu-id="01d48-181">requiredJoinsAsRelationPathList</span><span class="sxs-lookup"><span data-stu-id="01d48-181">requiredJoinsAsRelationPathList</span></span>  

<!-- -->

<span data-ttu-id="01d48-182">filterValuesAsFilterValueList</span><span class="sxs-lookup"><span data-stu-id="01d48-182">filterValuesAsFilterValueList</span></span>  

### <a name="return-value---generateresolvereferencequery"></a><span data-ttu-id="01d48-183">戻り値 - generateResolveReferenceQuery</span><span class="sxs-lookup"><span data-stu-id="01d48-183">Return Value - generateResolveReferenceQuery</span></span>

## <a name="method-isresolvedreferenceambiguous"></a><span data-ttu-id="01d48-184">メソッド isResolvedReferenceAmbiguous</span><span class="sxs-lookup"><span data-stu-id="01d48-184">Method isResolvedReferenceAmbiguous</span></span>

```xpp
public boolean isResolvedReferenceAmbiguous(Query query)
```

### <a name="parameters---isresolvedreferenceambiguous"></a><span data-ttu-id="01d48-185">パラメーター - isResolvedReferenceAmbiguous</span><span class="sxs-lookup"><span data-stu-id="01d48-185">Parameters - isResolvedReferenceAmbiguous</span></span>

<span data-ttu-id="01d48-186">クエリ</span><span class="sxs-lookup"><span data-stu-id="01d48-186">query</span></span>  

### <a name="return-value---isresolvedreferenceambiguous"></a><span data-ttu-id="01d48-187">戻り値 - isResolvedReferenceAmbiguous</span><span class="sxs-lookup"><span data-stu-id="01d48-187">Return Value - isResolvedReferenceAmbiguous</span></span>

## <a name="method-primarykeytablename"></a><span data-ttu-id="01d48-188">メソッド primaryKeyTableName</span><span class="sxs-lookup"><span data-stu-id="01d48-188">Method primaryKeyTableName</span></span>

```xpp
public str primaryKeyTableName()
```

### <a name="return-value---primarykeytablename"></a><span data-ttu-id="01d48-189">戻り値 - primaryKeyTableName</span><span class="sxs-lookup"><span data-stu-id="01d48-189">Return Value - primaryKeyTableName</span></span>

## <a name="method-querybuilddatasourcebindingsforquery"></a><span data-ttu-id="01d48-190">メソッド queryBuildDataSourceBindingsForQuery</span><span class="sxs-lookup"><span data-stu-id="01d48-190">Method queryBuildDataSourceBindingsForQuery</span></span>

```xpp
public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, [boolean isRootPrimaryKeyDataSource])
```

### <a name="parameters---querybuilddatasourcebindingsforquery"></a><span data-ttu-id="01d48-191">パラメーター - queryBuildDataSourceBindingsForQuery</span><span class="sxs-lookup"><span data-stu-id="01d48-191">Parameters - queryBuildDataSourceBindingsForQuery</span></span>

<span data-ttu-id="01d48-192">クエリ</span><span class="sxs-lookup"><span data-stu-id="01d48-192">query</span></span>  

<!-- -->

<span data-ttu-id="01d48-193">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-193">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="01d48-194">isRootPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="01d48-194">isRootPrimaryKeyDataSource</span></span>  

### <a name="return-value---querybuilddatasourcebindingsforquery"></a><span data-ttu-id="01d48-195">戻り値 - queryBuildDataSourceBindingsForQuery</span><span class="sxs-lookup"><span data-stu-id="01d48-195">Return Value - queryBuildDataSourceBindingsForQuery</span></span>

## <a name="method-querybuilddatasourcebindingsforrootds"></a><span data-ttu-id="01d48-196">メソッド queryBuildDataSourceBindingsForRootDS</span><span class="sxs-lookup"><span data-stu-id="01d48-196">Method queryBuildDataSourceBindingsForRootDS</span></span>

```xpp
public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)
```

### <a name="parameters---querybuilddatasourcebindingsforrootds"></a><span data-ttu-id="01d48-197">パラメーター - queryBuildDataSourceBindingsForRootDS</span><span class="sxs-lookup"><span data-stu-id="01d48-197">Parameters - queryBuildDataSourceBindingsForRootDS</span></span>

<span data-ttu-id="01d48-198">rootQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="01d48-198">rootQueryBuildDataSource</span></span>  

<!-- -->

<span data-ttu-id="01d48-199">isPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="01d48-199">isPrimaryKeyDataSource</span></span>  

<!-- -->

<span data-ttu-id="01d48-200">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-200">replacementFieldGroupName</span></span>  

### <a name="return-value---querybuilddatasourcebindingsforrootds"></a><span data-ttu-id="01d48-201">戻り値 - queryBuildDataSourceBindingsForRootDS</span><span class="sxs-lookup"><span data-stu-id="01d48-201">Return Value - queryBuildDataSourceBindingsForRootDS</span></span>

## <a name="method-resolvereference"></a><span data-ttu-id="01d48-202">メソッド resolveReference</span><span class="sxs-lookup"><span data-stu-id="01d48-202">Method resolveReference</span></span>

```xpp
public Common resolveReference(Query query, [boolean ignoreAmbiguousReference])
```

### <a name="parameters---resolvereference"></a><span data-ttu-id="01d48-203">パラメーター - resolveReference</span><span class="sxs-lookup"><span data-stu-id="01d48-203">Parameters - resolveReference</span></span>

<span data-ttu-id="01d48-204">クエリ</span><span class="sxs-lookup"><span data-stu-id="01d48-204">query</span></span>  

<!-- -->

<span data-ttu-id="01d48-205">ignoreAmbiguousReference</span><span class="sxs-lookup"><span data-stu-id="01d48-205">ignoreAmbiguousReference</span></span>  

### <a name="return-value---resolvereference"></a><span data-ttu-id="01d48-206">戻り値 - resolveReference</span><span class="sxs-lookup"><span data-stu-id="01d48-206">Return Value - resolveReference</span></span>

## <a name="method-surrogateforeignkeyfieldbinding"></a><span data-ttu-id="01d48-207">メソッド surrogateForeignKeyFieldBinding</span><span class="sxs-lookup"><span data-stu-id="01d48-207">Method surrogateForeignKeyFieldBinding</span></span>

```xpp
public FieldBinding surrogateForeignKeyFieldBinding()
```

### <a name="return-value---surrogateforeignkeyfieldbinding"></a><span data-ttu-id="01d48-208">戻り値 - surrogateForeignKeyFieldBinding</span><span class="sxs-lookup"><span data-stu-id="01d48-208">Return Value - surrogateForeignKeyFieldBinding</span></span>

## <a name="method-construct"></a><span data-ttu-id="01d48-209">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="01d48-209">Method construct</span></span>

```xpp
public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)
```

### <a name="parameters---construct"></a><span data-ttu-id="01d48-210">パラメーター - construct</span><span class="sxs-lookup"><span data-stu-id="01d48-210">Parameters - construct</span></span>

<span data-ttu-id="01d48-211">surrogateForeignKeyBinding</span><span class="sxs-lookup"><span data-stu-id="01d48-211">surrogateForeignKeyBinding</span></span>  

### <a name="return-value---construct"></a><span data-ttu-id="01d48-212">戻り値 - construct</span><span class="sxs-lookup"><span data-stu-id="01d48-212">Return Value - construct</span></span>

## <a name="method-constructforedt"></a><span data-ttu-id="01d48-213">メソッド constructForEDT</span><span class="sxs-lookup"><span data-stu-id="01d48-213">Method constructForEDT</span></span>

```xpp
public static SurrogateFKReplacementHelper constructForEDT(str edtName)
```

### <a name="parameters---constructforedt"></a><span data-ttu-id="01d48-214">パラメーター - constructForEDT</span><span class="sxs-lookup"><span data-stu-id="01d48-214">Parameters - constructForEDT</span></span>

<span data-ttu-id="01d48-215">edtName</span><span class="sxs-lookup"><span data-stu-id="01d48-215">edtName</span></span>  

### <a name="return-value---constructforedt"></a><span data-ttu-id="01d48-216">戻り値 - constructForEDT</span><span class="sxs-lookup"><span data-stu-id="01d48-216">Return Value - constructForEDT</span></span>

## <a name="method-constructforpktable"></a><span data-ttu-id="01d48-217">メソッド constructForPKTable</span><span class="sxs-lookup"><span data-stu-id="01d48-217">Method constructForPKTable</span></span>

```xpp
public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)
```

### <a name="parameters---constructforpktable"></a><span data-ttu-id="01d48-218">パラメーター - constructForPKTable</span><span class="sxs-lookup"><span data-stu-id="01d48-218">Parameters - constructForPKTable</span></span>

<span data-ttu-id="01d48-219">pkTableName</span><span class="sxs-lookup"><span data-stu-id="01d48-219">pkTableName</span></span>  

### <a name="return-value---constructforpktable"></a><span data-ttu-id="01d48-220">戻り値 - constructForPKTable</span><span class="sxs-lookup"><span data-stu-id="01d48-220">Return Value - constructForPKTable</span></span>

## <a name="method-defaultprimarykeyquerydatasourcename"></a><span data-ttu-id="01d48-221">メソッド defaultPrimaryKeyQueryDataSourceName</span><span class="sxs-lookup"><span data-stu-id="01d48-221">Method defaultPrimaryKeyQueryDataSourceName</span></span>

```xpp
public static str defaultPrimaryKeyQueryDataSourceName()
```

### <a name="return-value---defaultprimarykeyquerydatasourcename"></a><span data-ttu-id="01d48-222">戻り値 - defaultPrimaryKeyQueryDataSourceName</span><span class="sxs-lookup"><span data-stu-id="01d48-222">Return Value - defaultPrimaryKeyQueryDataSourceName</span></span>

## <a name="method-deprecated_workflowcaption"></a><span data-ttu-id="01d48-223">メソッド DEPRECATED\_WorkflowCaption</span><span class="sxs-lookup"><span data-stu-id="01d48-223">Method DEPRECATED\_WorkflowCaption</span></span>

```xpp
public static str DEPRECATED_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)
```

### <a name="parameters---deprecated_workflowcaption"></a><span data-ttu-id="01d48-224">パラメーター - DEPRECATED\_WorkflowCaption</span><span class="sxs-lookup"><span data-stu-id="01d48-224">Parameters - DEPRECATED\_WorkflowCaption</span></span>

<span data-ttu-id="01d48-225">tableName</span><span class="sxs-lookup"><span data-stu-id="01d48-225">tableName</span></span>  

<!-- -->

<span data-ttu-id="01d48-226">fieldName</span><span class="sxs-lookup"><span data-stu-id="01d48-226">fieldName</span></span>  

<!-- -->

<span data-ttu-id="01d48-227">recIDValue</span><span class="sxs-lookup"><span data-stu-id="01d48-227">recIDValue</span></span>  

### <a name="return-value---deprecated_workflowcaption"></a><span data-ttu-id="01d48-228">戻り値 - DEPRECATED\_WorkflowCaption</span><span class="sxs-lookup"><span data-stu-id="01d48-228">Return Value - DEPRECATED\_WorkflowCaption</span></span>

## <a name="method-implicitreplacementfieldgroupname"></a><span data-ttu-id="01d48-229">メソッド implicitReplacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-229">Method implicitReplacementFieldGroupName</span></span>

```xpp
public static str implicitReplacementFieldGroupName()
```

### <a name="return-value---implicitreplacementfieldgroupname"></a><span data-ttu-id="01d48-230">戻り値 - implicitReplacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="01d48-230">Return Value - implicitReplacementFieldGroupName</span></span>

## <a name="method-new"></a><span data-ttu-id="01d48-231">メソッド new</span><span class="sxs-lookup"><span data-stu-id="01d48-231">Method new</span></span>

<span data-ttu-id="01d48-232">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="01d48-232">Initializes a new instance of the Object class.</span></span>

```xpp
private void new(FieldBinding surrogateForeignKeyBinding)
```

### <a name="parameters---new"></a><span data-ttu-id="01d48-233">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="01d48-233">Parameters - new</span></span>

<span data-ttu-id="01d48-234">surrogateForeignKeyBinding</span><span class="sxs-lookup"><span data-stu-id="01d48-234">surrogateForeignKeyBinding</span></span>  

