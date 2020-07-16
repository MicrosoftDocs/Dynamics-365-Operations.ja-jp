---
title: DictRelation クラス
description: このトピックでは、DictRelation クラスについて説明します。
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
ms.openlocfilehash: 2d79651b7998c203d088cd8da5964d2e8ef5b3f1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502983"
---
# <a name="class-dictrelation"></a><span data-ttu-id="c19e7-103">クラス DictRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-103">Class DictRelation</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictRelation extends Object
```

<span data-ttu-id="c19e7-104">DictRelation クラスは、テーブルのディクショナリ関係の管理に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c19e7-104">The DictRelation class can be used to manage dictionary relations for the tables.</span></span>

## <a name="remarks"></a><span data-ttu-id="c19e7-105">備考</span><span class="sxs-lookup"><span data-stu-id="c19e7-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="c19e7-106">例</span><span class="sxs-lookup"><span data-stu-id="c19e7-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c19e7-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="c19e7-107">Methods</span></span>

| <span data-ttu-id="c19e7-108">方法</span><span class="sxs-lookup"><span data-stu-id="c19e7-108">Method</span></span>                                                                                                                | <span data-ttu-id="c19e7-109">説明</span><span class="sxs-lookup"><span data-stu-id="c19e7-109">Description</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="c19e7-110">public Cardinality Cardinality()</span><span class="sxs-lookup"><span data-stu-id="c19e7-110">public Cardinality Cardinality()</span></span>                                                                                      | <span data-ttu-id="c19e7-111">基数値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-111">Retrieves the cardinality value.</span></span>                                     |
| <span data-ttu-id="c19e7-112">public boolean createNavigationPropertyMethods()</span><span class="sxs-lookup"><span data-stu-id="c19e7-112">public boolean createNavigationPropertyMethods()</span></span>                                                                      |                                                                      |
| <span data-ttu-id="c19e7-113">public boolean EDTRelation()</span><span class="sxs-lookup"><span data-stu-id="c19e7-113">public boolean EDTRelation()</span></span>                                                                                          | <span data-ttu-id="c19e7-114">拡張データ型 (EDT) の関係の状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-114">Retrieves the extended data type (EDT) relation state.</span></span>               |
| <span data-ttu-id="c19e7-115">public str entityRelationshipRole()</span><span class="sxs-lookup"><span data-stu-id="c19e7-115">public str entityRelationshipRole()</span></span>                                                                                   | <span data-ttu-id="c19e7-116">エンティティ リレーションシップ ロールの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-116">Retrieves the name of the entity relationship role.</span></span>                  |
| <span data-ttu-id="c19e7-117">public str entityRelationshipRoleLabelId()</span><span class="sxs-lookup"><span data-stu-id="c19e7-117">public str entityRelationshipRoleLabelId()</span></span>                                                                            | <span data-ttu-id="c19e7-118">エンティティ関係ロールの名前のラベル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-118">Retrieves the label ID for the name of the entity relationship role.</span></span> |
| <span data-ttu-id="c19e7-119">public TableId externTable()</span><span class="sxs-lookup"><span data-stu-id="c19e7-119">public TableId externTable()</span></span>                                                                                          | <span data-ttu-id="c19e7-120">関係のために使用する外部テーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-120">Returns the ID of the external table that is used for the relation.</span></span>  |
| <span data-ttu-id="c19e7-121">public boolean isSelfLink()</span><span class="sxs-lookup"><span data-stu-id="c19e7-121">public boolean isSelfLink()</span></span>                                                                                           | <span data-ttu-id="c19e7-122">リレーションが自己リンクされているかどうかを検証します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-122">Verifies whether the relation is self-linked.</span></span>                        |
| <span data-ttu-id="c19e7-123">public int lineExternTableValue(int lineNumber)</span><span class="sxs-lookup"><span data-stu-id="c19e7-123">public int lineExternTableValue(int lineNumber)</span></span>                                                                       | <span data-ttu-id="c19e7-124">特定の行の外部テーブル値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-124">Retrieves the external table value for the given line.</span></span>               |
| <span data-ttu-id="c19e7-125">public int lines()</span><span class="sxs-lookup"><span data-stu-id="c19e7-125">public int lines()</span></span>                                                                                                    | <span data-ttu-id="c19e7-126">リレーションの明細行の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-126">Retrieves the number of the lines in the relation.</span></span>                   |
| <span data-ttu-id="c19e7-127">public int lineSourceEDT(int lineNumber)</span><span class="sxs-lookup"><span data-stu-id="c19e7-127">public int lineSourceEDT(int lineNumber)</span></span>                                                                              | <span data-ttu-id="c19e7-128">特定のテーブル行のソース EDT 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-128">Retrieves the source EDT value for the given table line.</span></span>             |
| <span data-ttu-id="c19e7-129">public RelationshipSubType lineSubType(int lineNumber)</span><span class="sxs-lookup"><span data-stu-id="c19e7-129">public RelationshipSubType lineSubType(int lineNumber)</span></span>                                                                | <span data-ttu-id="c19e7-130">指定されたテーブル行のサブタイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-130">Retrieves the sub-type for the given table line.</span></span>                     |
| <span data-ttu-id="c19e7-131">public int lineTableValue(int lineNumber)</span><span class="sxs-lookup"><span data-stu-id="c19e7-131">public int lineTableValue(int lineNumber)</span></span>                                                                             | <span data-ttu-id="c19e7-132">特定のテーブル行の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-132">Retrieves the value for the given table line.</span></span>                        |
| <span data-ttu-id="c19e7-133">public TableRelation lineType(int lineNumber)</span><span class="sxs-lookup"><span data-stu-id="c19e7-133">public TableRelation lineType(int lineNumber)</span></span>                                                                         | <span data-ttu-id="c19e7-134">指定されたテーブル行のリレーション タイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-134">Retrieves the relation type for the given table line.</span></span>                |
| <span data-ttu-id="c19e7-135">public TableId loadFieldRelation(FieldId fieldId, \[TableScope tableScope\], \[Common record\], \[boolean isLookup\])</span><span class="sxs-lookup"><span data-stu-id="c19e7-135">public TableId loadFieldRelation(FieldId fieldId, \[TableScope tableScope\], \[Common record\], \[boolean isLookup\])</span></span> | <span data-ttu-id="c19e7-136">フィールド ID で指定されている関係を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="c19e7-136">Loads a relation that is specified by a field ID.</span></span>                    |
| <span data-ttu-id="c19e7-137">public TableId loadNameRelation(str name)</span><span class="sxs-lookup"><span data-stu-id="c19e7-137">public TableId loadNameRelation(str name)</span></span>                                                                             | <span data-ttu-id="c19e7-138">指定された名前の関係を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="c19e7-138">Loads the relation for the given name.</span></span>                               |
| <span data-ttu-id="c19e7-139">public TableId loadTableRelation(TableId tableId, \[TableScope tableScope\], \[Common record\])</span><span class="sxs-lookup"><span data-stu-id="c19e7-139">public TableId loadTableRelation(TableId tableId, \[TableScope tableScope\], \[Common record\])</span></span>                       | <span data-ttu-id="c19e7-140">テーブル リレーションを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="c19e7-140">Loads a table relation.</span></span>                                              |
| <span data-ttu-id="c19e7-141">public str navigationPropertyNameOverride()</span><span class="sxs-lookup"><span data-stu-id="c19e7-141">public str navigationPropertyNameOverride()</span></span>                                                                           |                                                                      |
| <span data-ttu-id="c19e7-142">public RelatedTableCardinality RelatedTableCardinality()</span><span class="sxs-lookup"><span data-stu-id="c19e7-142">public RelatedTableCardinality RelatedTableCardinality()</span></span>                                                              | <span data-ttu-id="c19e7-143">関連テーブルの基数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-143">Retrieves the cardinality for the related table.</span></span>                     |
| <span data-ttu-id="c19e7-144">public str RelatedTableRole()</span><span class="sxs-lookup"><span data-stu-id="c19e7-144">public str RelatedTableRole()</span></span>                                                                                         | <span data-ttu-id="c19e7-145">関連テーブルのロール名を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-145">Retrieves the role name for the related table.</span></span>                       |
| <span data-ttu-id="c19e7-146">public RelationshipType relationshipType()</span><span class="sxs-lookup"><span data-stu-id="c19e7-146">public RelationshipType relationshipType()</span></span>                                                                            | <span data-ttu-id="c19e7-147">関係タイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-147">Retrieves the relationship type.</span></span>                                     |
| <span data-ttu-id="c19e7-148">public str Role()</span><span class="sxs-lookup"><span data-stu-id="c19e7-148">public str Role()</span></span>                                                                                                     | <span data-ttu-id="c19e7-149">ロール名を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-149">Retrieves the role name.</span></span>                                             |
| <span data-ttu-id="c19e7-150">public TableId table()</span><span class="sxs-lookup"><span data-stu-id="c19e7-150">public TableId table()</span></span>                                                                                                | <span data-ttu-id="c19e7-151">リレーションのテーブル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-151">Returns the table ID of the relation.</span></span>                                |
| <span data-ttu-id="c19e7-152">public boolean useDefaultRoleNames()</span><span class="sxs-lookup"><span data-stu-id="c19e7-152">public boolean useDefaultRoleNames()</span></span>                                                                                  |                                                                      |
| <span data-ttu-id="c19e7-153">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="c19e7-153">public boolean validate()</span></span>                                                                                             | <span data-ttu-id="c19e7-154">リレーションを検証します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-154">Validates a relation.</span></span>                                                |
| <span data-ttu-id="c19e7-155">::public static boolean isSurrogateForeignKeyRelation(TableId tableId, str relationName)</span><span class="sxs-lookup"><span data-stu-id="c19e7-155">::public static boolean isSurrogateForeignKeyRelation(TableId tableId, str relationName)</span></span>                              | <span data-ttu-id="c19e7-156">代理外部キーのリレーションがあるかどうかを検証します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-156">Verifies whether there is surrogate foreign key relation.</span></span>            |
| <span data-ttu-id="c19e7-157">public void new(int id, \[UtilElementType Util\_Element\_Type\], \[int index\])</span><span class="sxs-lookup"><span data-stu-id="c19e7-157">public void new(int id, \[UtilElementType Util\_Element\_Type\], \[int index\])</span></span>                                       | <span data-ttu-id="c19e7-158">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-158">Initializes a new instance of the Object class.</span></span>                      |

## <a name="method-cardinality"></a><span data-ttu-id="c19e7-159">メソッド Cardinality</span><span class="sxs-lookup"><span data-stu-id="c19e7-159">Method Cardinality</span></span>

<span data-ttu-id="c19e7-160">基数値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-160">Retrieves the cardinality value.</span></span>

```xpp
public Cardinality Cardinality()
```

### <a name="return-value---cardinality"></a><span data-ttu-id="c19e7-161">戻り値 - Cardinality</span><span class="sxs-lookup"><span data-stu-id="c19e7-161">Return Value - Cardinality</span></span>

<span data-ttu-id="c19e7-162">基数値。</span><span class="sxs-lookup"><span data-stu-id="c19e7-162">The cardinality value.</span></span>

## <a name="method-createnavigationpropertymethods"></a><span data-ttu-id="c19e7-163">メソッド createNavigationPropertyMethods</span><span class="sxs-lookup"><span data-stu-id="c19e7-163">Method createNavigationPropertyMethods</span></span>

```xpp
public boolean createNavigationPropertyMethods()
```

### <a name="return-value---createnavigationpropertymethods"></a><span data-ttu-id="c19e7-164">戻り値 - createNavigationPropertyMethods</span><span class="sxs-lookup"><span data-stu-id="c19e7-164">Return Value - createNavigationPropertyMethods</span></span>

## <a name="method-edtrelation"></a><span data-ttu-id="c19e7-165">メソッド EDTRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-165">Method EDTRelation</span></span>

<span data-ttu-id="c19e7-166">拡張データ型 (EDT) の関係の状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-166">Retrieves the extended data type (EDT) relation state.</span></span>

```xpp
public boolean EDTRelation()
```

### <a name="return-value---edtrelation"></a><span data-ttu-id="c19e7-167">戻り値 - EDTRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-167">Return Value - EDTRelation</span></span>

<span data-ttu-id="c19e7-168">EDT 関係が使用可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="c19e7-168">A Boolean value that indicates whether the EDT relation is available.</span></span>

## <a name="method-entityrelationshiprole"></a><span data-ttu-id="c19e7-169">メソッド entityRelationshipRole</span><span class="sxs-lookup"><span data-stu-id="c19e7-169">Method entityRelationshipRole</span></span>

<span data-ttu-id="c19e7-170">エンティティ リレーションシップ ロールの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-170">Retrieves the name of the entity relationship role.</span></span>

```xpp
public str entityRelationshipRole()
```

### <a name="return-value---entityrelationshiprole"></a><span data-ttu-id="c19e7-171">戻り値 - entityRelationshipRole</span><span class="sxs-lookup"><span data-stu-id="c19e7-171">Return Value - entityRelationshipRole</span></span>

<span data-ttu-id="c19e7-172">エンティティ リレーションシップ ロールの名前。</span><span class="sxs-lookup"><span data-stu-id="c19e7-172">The name of the entity relationship role.</span></span>

## <a name="method-entityrelationshiprolelabelid"></a><span data-ttu-id="c19e7-173">メソッド entityRelationshipRoleLabelId</span><span class="sxs-lookup"><span data-stu-id="c19e7-173">Method entityRelationshipRoleLabelId</span></span>

<span data-ttu-id="c19e7-174">エンティティ関係ロールの名前のラベル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-174">Retrieves the label ID for the name of the entity relationship role.</span></span>

```xpp
public str entityRelationshipRoleLabelId()
```

### <a name="return-value---entityrelationshiprolelabelid"></a><span data-ttu-id="c19e7-175">戻り値 - entityRelationshipRoleLabelId</span><span class="sxs-lookup"><span data-stu-id="c19e7-175">Return Value - entityRelationshipRoleLabelId</span></span>

<span data-ttu-id="c19e7-176">エンティティ リレーションシップ ロールのラベル ID。</span><span class="sxs-lookup"><span data-stu-id="c19e7-176">The label ID for the entity relationship role.</span></span>

## <a name="method-externtable"></a><span data-ttu-id="c19e7-177">メソッド externTable</span><span class="sxs-lookup"><span data-stu-id="c19e7-177">Method externTable</span></span>

<span data-ttu-id="c19e7-178">関係のために使用する外部テーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-178">Returns the ID of the external table that is used for the relation.</span></span>

```xpp
public TableId externTable()
```

### <a name="return-value---externtable"></a><span data-ttu-id="c19e7-179">戻り値 - externTable</span><span class="sxs-lookup"><span data-stu-id="c19e7-179">Return Value - externTable</span></span>

<span data-ttu-id="c19e7-180">関係に使用される外部テーブルの ID。関係がまだ読み込まれていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="c19e7-180">The ID of the external table that is used for the relation; 0 (zero) if the relation has not yet been loaded.</span></span>

### <a name="examples---externtable"></a><span data-ttu-id="c19e7-181">例 - externTable</span><span class="sxs-lookup"><span data-stu-id="c19e7-181">Examples - externTable</span></span>

<span data-ttu-id="c19e7-182">次の例は、外部テーブルの ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="c19e7-182">The following example shows the retrieval of the external table ID.</span></span>

```xpp
Dictionary dict; 
DictRelation dr; 
int i;  
dict = new Dictionary(); 
dr = new DictRelation(dict.tableName2Id("CustTable")); 
// Load a relation by name 
dr.loadNameRelation("CompanyData");  // Also returns the external table ID. 
print "The external table ID is: " + int2str(dr.externTable());
```

## <a name="method-isselflink"></a><span data-ttu-id="c19e7-183">メソッド isSelfLink</span><span class="sxs-lookup"><span data-stu-id="c19e7-183">Method isSelfLink</span></span>

<span data-ttu-id="c19e7-184">リレーションが自己リンクされているかどうかを検証します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-184">Verifies whether the relation is self-linked.</span></span>

```xpp
public boolean isSelfLink()
```

### <a name="return-value---isselflink"></a><span data-ttu-id="c19e7-185">戻り値 - isSelfLink</span><span class="sxs-lookup"><span data-stu-id="c19e7-185">Return Value - isSelfLink</span></span>

<span data-ttu-id="c19e7-186">リレーションが自己リンクである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c19e7-186">true if the relation is self-linked; otherwise, false.</span></span>

## <a name="method-lineexterntablevalue"></a><span data-ttu-id="c19e7-187">メソッド lineExternTableValue</span><span class="sxs-lookup"><span data-stu-id="c19e7-187">Method lineExternTableValue</span></span>

<span data-ttu-id="c19e7-188">特定の行の外部テーブル値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-188">Retrieves the external table value for the given line.</span></span>

```xpp
public int lineExternTableValue(int lineNumber)
```

### <a name="parameters---lineexterntablevalue"></a><span data-ttu-id="c19e7-189">パラメーター - lineExternTableValue</span><span class="sxs-lookup"><span data-stu-id="c19e7-189">Parameters - lineExternTableValue</span></span>

<span data-ttu-id="c19e7-190">lineNumber</span><span class="sxs-lookup"><span data-stu-id="c19e7-190">lineNumber</span></span>  

### <a name="return-value---lineexterntablevalue"></a><span data-ttu-id="c19e7-191">戻り値 - lineExternTableValue</span><span class="sxs-lookup"><span data-stu-id="c19e7-191">Return Value - lineExternTableValue</span></span>

<span data-ttu-id="c19e7-192">外部テーブル値。</span><span class="sxs-lookup"><span data-stu-id="c19e7-192">The external table value.</span></span>

## <a name="method-lines"></a><span data-ttu-id="c19e7-193">メソッド lines</span><span class="sxs-lookup"><span data-stu-id="c19e7-193">Method lines</span></span>

<span data-ttu-id="c19e7-194">リレーションの明細行の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-194">Retrieves the number of the lines in the relation.</span></span>

```xpp
public int lines()
```

### <a name="return-value---lines"></a><span data-ttu-id="c19e7-195">戻り値 - lines</span><span class="sxs-lookup"><span data-stu-id="c19e7-195">Return Value - lines</span></span>

<span data-ttu-id="c19e7-196">ラインの数。</span><span class="sxs-lookup"><span data-stu-id="c19e7-196">The number of the lines.</span></span>

## <a name="method-linesourceedt"></a><span data-ttu-id="c19e7-197">メソッド lineSourceEDT</span><span class="sxs-lookup"><span data-stu-id="c19e7-197">Method lineSourceEDT</span></span>

<span data-ttu-id="c19e7-198">特定のテーブル行のソース EDT 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-198">Retrieves the source EDT value for the given table line.</span></span>

```xpp
public int lineSourceEDT(int lineNumber)
```

### <a name="parameters---linesourceedt"></a><span data-ttu-id="c19e7-199">パラメーター - lineSourceEDT</span><span class="sxs-lookup"><span data-stu-id="c19e7-199">Parameters - lineSourceEDT</span></span>

<span data-ttu-id="c19e7-200">lineNumber</span><span class="sxs-lookup"><span data-stu-id="c19e7-200">lineNumber</span></span>  

### <a name="return-value---linesourceedt"></a><span data-ttu-id="c19e7-201">戻り値 - lineSourceEDT</span><span class="sxs-lookup"><span data-stu-id="c19e7-201">Return Value - lineSourceEDT</span></span>

<span data-ttu-id="c19e7-202">ソース EDT 値。</span><span class="sxs-lookup"><span data-stu-id="c19e7-202">The source EDT value.</span></span>

## <a name="method-linesubtype"></a><span data-ttu-id="c19e7-203">メソッド lineSubType</span><span class="sxs-lookup"><span data-stu-id="c19e7-203">Method lineSubType</span></span>

<span data-ttu-id="c19e7-204">指定されたテーブル行のサブタイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-204">Retrieves the sub-type for the given table line.</span></span>

```xpp
public RelationshipSubType lineSubType(int lineNumber)
```

### <a name="parameters---linesubtype"></a><span data-ttu-id="c19e7-205">パラメーター - lineSubType</span><span class="sxs-lookup"><span data-stu-id="c19e7-205">Parameters - lineSubType</span></span>

<span data-ttu-id="c19e7-206">lineNumber</span><span class="sxs-lookup"><span data-stu-id="c19e7-206">lineNumber</span></span>  

### <a name="return-value---linesubtype"></a><span data-ttu-id="c19e7-207">戻り値 - lineSubType</span><span class="sxs-lookup"><span data-stu-id="c19e7-207">Return Value - lineSubType</span></span>

<span data-ttu-id="c19e7-208">指定されたテーブル行のサブタイプ。</span><span class="sxs-lookup"><span data-stu-id="c19e7-208">The sub-type for the given table line.</span></span>

## <a name="method-linetablevalue"></a><span data-ttu-id="c19e7-209">メソッド lineTableValue</span><span class="sxs-lookup"><span data-stu-id="c19e7-209">Method lineTableValue</span></span>

<span data-ttu-id="c19e7-210">特定のテーブル行の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-210">Retrieves the value for the given table line.</span></span>

```xpp
public int lineTableValue(int lineNumber)
```

### <a name="parameters---linetablevalue"></a><span data-ttu-id="c19e7-211">パラメーター - lineTableValue</span><span class="sxs-lookup"><span data-stu-id="c19e7-211">Parameters - lineTableValue</span></span>

<span data-ttu-id="c19e7-212">lineNumber</span><span class="sxs-lookup"><span data-stu-id="c19e7-212">lineNumber</span></span>  

### <a name="return-value---linetablevalue"></a><span data-ttu-id="c19e7-213">戻り値 - lineTableValue</span><span class="sxs-lookup"><span data-stu-id="c19e7-213">Return Value - lineTableValue</span></span>

<span data-ttu-id="c19e7-214">テーブル行の値。</span><span class="sxs-lookup"><span data-stu-id="c19e7-214">The value for the table line.</span></span>

## <a name="method-linetype"></a><span data-ttu-id="c19e7-215">メソッド lineType</span><span class="sxs-lookup"><span data-stu-id="c19e7-215">Method lineType</span></span>

<span data-ttu-id="c19e7-216">指定されたテーブル行のリレーション タイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-216">Retrieves the relation type for the given table line.</span></span>

```xpp
public TableRelation lineType(int lineNumber)
```

### <a name="parameters---linetype"></a><span data-ttu-id="c19e7-217">パラメーター - lineType</span><span class="sxs-lookup"><span data-stu-id="c19e7-217">Parameters - lineType</span></span>

<span data-ttu-id="c19e7-218">lineNumber</span><span class="sxs-lookup"><span data-stu-id="c19e7-218">lineNumber</span></span>  

### <a name="return-value---linetype"></a><span data-ttu-id="c19e7-219">戻り値 - lineType</span><span class="sxs-lookup"><span data-stu-id="c19e7-219">Return Value - lineType</span></span>

<span data-ttu-id="c19e7-220">指定された行のテーブルのリレーション タイプ。</span><span class="sxs-lookup"><span data-stu-id="c19e7-220">The table relation type for the given line.</span></span>

## <a name="method-loadfieldrelation"></a><span data-ttu-id="c19e7-221">メソッド loadFieldRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-221">Method loadFieldRelation</span></span>

<span data-ttu-id="c19e7-222">フィールド ID で指定されている関係を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="c19e7-222">Loads a relation that is specified by a field ID.</span></span>

```xpp
public TableId loadFieldRelation(FieldId fieldId, [TableScope tableScope], [Common record], [boolean isLookup])
```

### <a name="parameters---loadfieldrelation"></a><span data-ttu-id="c19e7-223">パラメーター - loadFieldRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-223">Parameters - loadFieldRelation</span></span>

<span data-ttu-id="c19e7-224">fieldId</span><span class="sxs-lookup"><span data-stu-id="c19e7-224">fieldId</span></span>  

<!-- -->

<span data-ttu-id="c19e7-225">tableScope</span><span class="sxs-lookup"><span data-stu-id="c19e7-225">tableScope</span></span>  

<!-- -->

<span data-ttu-id="c19e7-226">記録</span><span class="sxs-lookup"><span data-stu-id="c19e7-226">record</span></span>  

<!-- -->

<span data-ttu-id="c19e7-227">isLookup</span><span class="sxs-lookup"><span data-stu-id="c19e7-227">isLookup</span></span>  

### <a name="return-value---loadfieldrelation"></a><span data-ttu-id="c19e7-228">戻り値 - loadFieldRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-228">Return Value - loadFieldRelation</span></span>

<span data-ttu-id="c19e7-229">関係のテーブルの ID。メソッドが失敗した場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="c19e7-229">The ID of the table for the relation; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if the method failed.</span></span>

## <a name="method-loadnamerelation"></a><span data-ttu-id="c19e7-230">メソッド loadNameRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-230">Method loadNameRelation</span></span>

<span data-ttu-id="c19e7-231">指定された名前の関係を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="c19e7-231">Loads the relation for the given name.</span></span>

```xpp
public TableId loadNameRelation(str name)
```

### <a name="parameters---loadnamerelation"></a><span data-ttu-id="c19e7-232">パラメーター - loadNameRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-232">Parameters - loadNameRelation</span></span>

<span data-ttu-id="c19e7-233">名前</span><span class="sxs-lookup"><span data-stu-id="c19e7-233">name</span></span>  

### <a name="return-value---loadnamerelation"></a><span data-ttu-id="c19e7-234">戻り値 - loadNameRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-234">Return Value - loadNameRelation</span></span>

<span data-ttu-id="c19e7-235">テーブル リレーションのテーブル ID。</span><span class="sxs-lookup"><span data-stu-id="c19e7-235">The table ID for the table relation.</span></span>

## <a name="method-loadtablerelation"></a><span data-ttu-id="c19e7-236">メソッド loadTableRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-236">Method loadTableRelation</span></span>

<span data-ttu-id="c19e7-237">テーブル リレーションを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="c19e7-237">Loads a table relation.</span></span>

```xpp
public TableId loadTableRelation(TableId tableId, [TableScope tableScope], [Common record])
```

### <a name="parameters---loadtablerelation"></a><span data-ttu-id="c19e7-238">パラメーター - loadTableRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-238">Parameters - loadTableRelation</span></span>

<span data-ttu-id="c19e7-239">tableId</span><span class="sxs-lookup"><span data-stu-id="c19e7-239">tableId</span></span>  

<!-- -->

<span data-ttu-id="c19e7-240">tableScope</span><span class="sxs-lookup"><span data-stu-id="c19e7-240">tableScope</span></span>  

<!-- -->

<span data-ttu-id="c19e7-241">記録</span><span class="sxs-lookup"><span data-stu-id="c19e7-241">record</span></span>  

### <a name="return-value---loadtablerelation"></a><span data-ttu-id="c19e7-242">戻り値 - loadTableRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-242">Return Value - loadTableRelation</span></span>

<span data-ttu-id="c19e7-243">テーブル リレーションのテーブル ID。</span><span class="sxs-lookup"><span data-stu-id="c19e7-243">The table ID for the table relation.</span></span>

## <a name="method-navigationpropertynameoverride"></a><span data-ttu-id="c19e7-244">メソッド navigationPropertyNameOverride</span><span class="sxs-lookup"><span data-stu-id="c19e7-244">Method navigationPropertyNameOverride</span></span>

```xpp
public str navigationPropertyNameOverride()
```

### <a name="return-value---navigationpropertynameoverride"></a><span data-ttu-id="c19e7-245">戻り値 - navigationPropertyNameOverride</span><span class="sxs-lookup"><span data-stu-id="c19e7-245">Return Value - navigationPropertyNameOverride</span></span>

## <a name="method-relatedtablecardinality"></a><span data-ttu-id="c19e7-246">メソッド RelatedTableCardinality</span><span class="sxs-lookup"><span data-stu-id="c19e7-246">Method RelatedTableCardinality</span></span>

<span data-ttu-id="c19e7-247">関連テーブルの基数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-247">Retrieves the cardinality for the related table.</span></span>

```xpp
public RelatedTableCardinality RelatedTableCardinality()
```

### <a name="return-value---relatedtablecardinality"></a><span data-ttu-id="c19e7-248">戻り値 - RelatedTableCardinality</span><span class="sxs-lookup"><span data-stu-id="c19e7-248">Return Value - RelatedTableCardinality</span></span>

<span data-ttu-id="c19e7-249">関連テーブルの基数。</span><span class="sxs-lookup"><span data-stu-id="c19e7-249">The cardinality for the related table.</span></span>

## <a name="method-relatedtablerole"></a><span data-ttu-id="c19e7-250">メソッド RelatedTableRole</span><span class="sxs-lookup"><span data-stu-id="c19e7-250">Method RelatedTableRole</span></span>

<span data-ttu-id="c19e7-251">関連テーブルのロール名を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-251">Retrieves the role name for the related table.</span></span>

```xpp
public str RelatedTableRole()
```

### <a name="return-value---relatedtablerole"></a><span data-ttu-id="c19e7-252">戻り値 - RelatedTableRole</span><span class="sxs-lookup"><span data-stu-id="c19e7-252">Return Value - RelatedTableRole</span></span>

<span data-ttu-id="c19e7-253">関連テーブルのロール名。</span><span class="sxs-lookup"><span data-stu-id="c19e7-253">The role name for the related table.</span></span>

## <a name="method-relationshiptype"></a><span data-ttu-id="c19e7-254">メソッド relationshipType</span><span class="sxs-lookup"><span data-stu-id="c19e7-254">Method relationshipType</span></span>

<span data-ttu-id="c19e7-255">関係タイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-255">Retrieves the relationship type.</span></span>

```xpp
public RelationshipType relationshipType()
```

### <a name="return-value---relationshiptype"></a><span data-ttu-id="c19e7-256">戻り値 - relationshipType</span><span class="sxs-lookup"><span data-stu-id="c19e7-256">Return Value - relationshipType</span></span>

<span data-ttu-id="c19e7-257">リレーションシップ タイプ。</span><span class="sxs-lookup"><span data-stu-id="c19e7-257">The relationship type.</span></span>

## <a name="method-role"></a><span data-ttu-id="c19e7-258">メソッド Role</span><span class="sxs-lookup"><span data-stu-id="c19e7-258">Method Role</span></span>

<span data-ttu-id="c19e7-259">ロール名を取得します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-259">Retrieves the role name.</span></span>

```xpp
public str Role()
```

### <a name="return-value---role"></a><span data-ttu-id="c19e7-260">戻り値 - Role</span><span class="sxs-lookup"><span data-stu-id="c19e7-260">Return Value - Role</span></span>

<span data-ttu-id="c19e7-261">ロール名。</span><span class="sxs-lookup"><span data-stu-id="c19e7-261">The role name.</span></span>

## <a name="method-table"></a><span data-ttu-id="c19e7-262">メソッド table</span><span class="sxs-lookup"><span data-stu-id="c19e7-262">Method table</span></span>

<span data-ttu-id="c19e7-263">リレーションのテーブル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-263">Returns the table ID of the relation.</span></span>

```xpp
public TableId table()
```

### <a name="return-value---table"></a><span data-ttu-id="c19e7-264">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="c19e7-264">Return Value - table</span></span>

<span data-ttu-id="c19e7-265">リレーションのテーブル ID</span><span class="sxs-lookup"><span data-stu-id="c19e7-265">The table ID of the relation.</span></span>

### <a name="examples---table"></a><span data-ttu-id="c19e7-266">例 - table</span><span class="sxs-lookup"><span data-stu-id="c19e7-266">Examples - table</span></span>

<span data-ttu-id="c19e7-267">次の例は、リレーションのテーブル ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="c19e7-267">The following example shows the retrieval of the table ID for a relation.</span></span>

```xpp
Dictionary dict; 
DictRelation dr; 
dict = new Dictionary(); 
dr = new DictRelation(dict.tableName2Id("CustTable")); 
print dr.table();
```

## <a name="method-usedefaultrolenames"></a><span data-ttu-id="c19e7-268">メソッド useDefaultRoleNames</span><span class="sxs-lookup"><span data-stu-id="c19e7-268">Method useDefaultRoleNames</span></span>

```xpp
public boolean useDefaultRoleNames()
```

### <a name="return-value---usedefaultrolenames"></a><span data-ttu-id="c19e7-269">戻り値 - useDefaultRoleNames</span><span class="sxs-lookup"><span data-stu-id="c19e7-269">Return Value - useDefaultRoleNames</span></span>

## <a name="method-validate"></a><span data-ttu-id="c19e7-270">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="c19e7-270">Method validate</span></span>

<span data-ttu-id="c19e7-271">リレーションを検証します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-271">Validates a relation.</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="c19e7-272">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="c19e7-272">Return Value - validate</span></span>

<span data-ttu-id="c19e7-273">リレーションが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c19e7-273">true if the relation is valid; otherwise, false.</span></span>

## <a name="method-issurrogateforeignkeyrelation"></a><span data-ttu-id="c19e7-274">メソッド isSurrogateForeignKeyRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-274">Method isSurrogateForeignKeyRelation</span></span>

<span data-ttu-id="c19e7-275">代理外部キーのリレーションがあるかどうかを検証します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-275">Verifies whether there is surrogate foreign key relation.</span></span>

```xpp
public static boolean isSurrogateForeignKeyRelation(TableId tableId, str relationName)
```

### <a name="parameters---issurrogateforeignkeyrelation"></a><span data-ttu-id="c19e7-276">パラメーター - isSurrogateForeignKeyRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-276">Parameters - isSurrogateForeignKeyRelation</span></span>

<span data-ttu-id="c19e7-277">tableId</span><span class="sxs-lookup"><span data-stu-id="c19e7-277">tableId</span></span>  

<!-- -->

<span data-ttu-id="c19e7-278">relationName</span><span class="sxs-lookup"><span data-stu-id="c19e7-278">relationName</span></span>  

### <a name="return-value---issurrogateforeignkeyrelation"></a><span data-ttu-id="c19e7-279">戻り値 - isSurrogateForeignKeyRelation</span><span class="sxs-lookup"><span data-stu-id="c19e7-279">Return Value - isSurrogateForeignKeyRelation</span></span>

<span data-ttu-id="c19e7-280">代理外部キー リレーションがある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c19e7-280">true if there is a surrogate foreign key relation; otherwise, false.</span></span>

## <a name="method-new"></a><span data-ttu-id="c19e7-281">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c19e7-281">Method new</span></span>

<span data-ttu-id="c19e7-282">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c19e7-282">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(int id, [UtilElementType Util_Element_Type], [int index])
```

### <a name="parameters---new"></a><span data-ttu-id="c19e7-283">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="c19e7-283">Parameters - new</span></span>

<span data-ttu-id="c19e7-284">id</span><span class="sxs-lookup"><span data-stu-id="c19e7-284">id</span></span>  
<span data-ttu-id="c19e7-285">リレーション インデックス (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c19e7-285">The relation index; optional.</span></span> <span data-ttu-id="c19e7-286">既定値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="c19e7-286">The default value is 1.</span></span>

<!-- -->

<span data-ttu-id="c19e7-287">Util\_Element\_Type</span><span class="sxs-lookup"><span data-stu-id="c19e7-287">Util\_Element\_Type</span></span>  
<span data-ttu-id="c19e7-288">リレーション インデックス (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c19e7-288">The relation index; optional.</span></span> <span data-ttu-id="c19e7-289">既定値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="c19e7-289">The default value is 1.</span></span>

<!-- -->

<span data-ttu-id="c19e7-290">指数</span><span class="sxs-lookup"><span data-stu-id="c19e7-290">index</span></span>  
<span data-ttu-id="c19e7-291">リレーション インデックス (オプション)。</span><span class="sxs-lookup"><span data-stu-id="c19e7-291">The relation index; optional.</span></span> <span data-ttu-id="c19e7-292">既定値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="c19e7-292">The default value is 1.</span></span>

