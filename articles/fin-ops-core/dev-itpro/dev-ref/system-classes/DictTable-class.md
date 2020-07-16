---
title: DictTable クラス
description: このトピックでは、DictTable クラスについて説明します。
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
ms.openlocfilehash: ea1491b083d21dd2b41970e049f0b2c11d0df063
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502982"
---
# <a name="class-dicttable"></a><span data-ttu-id="8e3a3-103">クラス DictTable</span><span class="sxs-lookup"><span data-stu-id="8e3a3-103">Class DictTable</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictTable extends Object
```

<span data-ttu-id="8e3a3-104">DictTable クラスは、テーブルに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-104">The DictTable class provides information about a table.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e3a3-105">備考</span><span class="sxs-lookup"><span data-stu-id="8e3a3-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="8e3a3-106">例</span><span class="sxs-lookup"><span data-stu-id="8e3a3-106">Examples</span></span>

<span data-ttu-id="8e3a3-107">次の例は、DictTable クラスのインスタンスを作成して、テーブル内のデータが会社ごとに格納されているかどうかを判断する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-107">The following example shows how to create an instance of the DictTable class to determine whether the data in the table is stored on a per-company basis.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table is saved on a %1 basis.", dt.dataPrCompany() ? 
                      "per company" : "global")); 
}
```

## <a name="methods"></a><span data-ttu-id="8e3a3-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="8e3a3-108">Methods</span></span>

| <span data-ttu-id="8e3a3-109">方法</span><span class="sxs-lookup"><span data-stu-id="8e3a3-109">Method</span></span>                                                                                                                                      | <span data-ttu-id="8e3a3-110">説明</span><span class="sxs-lookup"><span data-stu-id="8e3a3-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3a3-111">public boolean doesMethodExist(str name)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-111">public boolean doesMethodExist(str name)</span></span>                                                                                                    | <span data-ttu-id="8e3a3-112">指定されたメソッドがテーブルに存在するかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-112">Checks whether a given method exists on the table.</span></span>                                                                                                                        |
| <span data-ttu-id="8e3a3-113">public AOSAuthorization AOSAuthSetting()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-113">public AOSAuthorization AOSAuthSetting()</span></span>                                                                                                    | <span data-ttu-id="8e3a3-114">ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定する AOSAuthorization システム列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-114">Retrieves an AOSAuthorization system enumeration value that specifies the type of operation that a user can perform on a table, depending on the permissions of the user.</span></span> |
| <span data-ttu-id="8e3a3-115">public RecordCacheLevel cacheLookup()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-115">public RecordCacheLevel cacheLookup()</span></span>                                                                                                       | <span data-ttu-id="8e3a3-116">テーブルのレコード キャッシュ レベルを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-116">Returns the record cache level for the table.</span></span>                                                                                                                             |
| <span data-ttu-id="8e3a3-117">public int cacheSize()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-117">public int cacheSize()</span></span>                                                                                                                      | <span data-ttu-id="8e3a3-118">テーブルのキャッシュ サイズをレコードの数で返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-118">Returns the cache size for the table, in the number of records.</span></span>                                                                                                           |
| <span data-ttu-id="8e3a3-119">public AnyType callObject(str methodName, Common Called, VarArg )</span><span class="sxs-lookup"><span data-stu-id="8e3a3-119">public AnyType callObject(str methodName, Common Called, VarArg )</span></span>                                                                           | <span data-ttu-id="8e3a3-120">テーブルの指定されたオブジェクトのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-120">Calls the specified object method for a table.</span></span>                                                                                                                            |
| <span data-ttu-id="8e3a3-121">public AnyType callStatic(str methodName, VarArg )</span><span class="sxs-lookup"><span data-stu-id="8e3a3-121">public AnyType callStatic(str methodName, VarArg )</span></span>                                                                                          | <span data-ttu-id="8e3a3-122">テーブルの指定された静的メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-122">Calls the specified static method for a table.</span></span>                                                                                                                            |
| <span data-ttu-id="8e3a3-123">public IndexId clusterIndex(\[boolean asDefinedInAOT\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-123">public IndexId clusterIndex(\[boolean asDefinedInAOT\])</span></span>                                                                                     | <span data-ttu-id="8e3a3-124">テーブルのクラスター化されたインデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-124">Returns the ID of the clustered index for the table.</span></span>                                                                                                                      |
| <span data-ttu-id="8e3a3-125">public ConfigurationKeyId configurationKeyId()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-125">public ConfigurationKeyId configurationKeyId()</span></span>                                                                                              | <span data-ttu-id="8e3a3-126">テーブルのコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-126">Returns the ID of the configuration key for the table.</span></span>                                                                                                                    |
| <span data-ttu-id="8e3a3-127">public boolean dataPerPartition()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-127">public boolean dataPerPartition()</span></span>                                                                                                           | <span data-ttu-id="8e3a3-128">テーブルのデータがパーティション単位で保存されるかどうかと、テーブルの SaveDataPerPartition プロパティに対応するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-128">Returns a value that indicates whether the data of the table is saved on a per-partition basis, and corresponds to the SaveDataPerPartition property of the table.</span></span>        |
| <span data-ttu-id="8e3a3-129">public boolean dataPrCompany()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-129">public boolean dataPrCompany()</span></span>                                                                                                              | <span data-ttu-id="8e3a3-130">テーブルのデータが会社単位で保存されるかどうかと、テーブルの SaveDataPerCompany プロパティに対応するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-130">Returns a value that indicates whether the data of the table is saved on a per-company basis, and corresponds to the SaveDataPerCompany property of the table.</span></span>            |
| <span data-ttu-id="8e3a3-131">public int deleteActionCnt()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-131">public int deleteActionCnt()</span></span>                                                                                                                | <span data-ttu-id="8e3a3-132">テーブルの削除アクションの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-132">Retrieves the number of delete actions for the table.</span></span>                                                                                                                     |
| <span data-ttu-id="8e3a3-133">public str deleteActionRelation(int cnt)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-133">public str deleteActionRelation(int cnt)</span></span>                                                                                                    |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-134">public TableId deleteActionTableId(int cnt)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-134">public TableId deleteActionTableId(int cnt)</span></span>                                                                                                 | <span data-ttu-id="8e3a3-135">インデックスで指定されているテーブルの削除アクションのテーブル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-135">Returns the table ID of a table's delete action that is specified by an index.</span></span>                                                                                            |
| <span data-ttu-id="8e3a3-136">public int deleteActionType(int cnt)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-136">public int deleteActionType(int cnt)</span></span>                                                                                                        | <span data-ttu-id="8e3a3-137">テーブルの削除アクションの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-137">Retrieves the type of a delete action for a table.</span></span>                                                                                                                        |
| <span data-ttu-id="8e3a3-138">public str developerDocumentation()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-138">public str developerDocumentation()</span></span>                                                                                                         |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-139">public str developerDocumentationLabelId()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-139">public str developerDocumentationLabelId()</span></span>                                                                                                  |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-140">public boolean enabled()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-140">public boolean enabled()</span></span>                                                                                                                    | <span data-ttu-id="8e3a3-141">テーブルが有効かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-141">Returns a value that indicates whether the table is enabled.</span></span>                                                                                                              |
| <span data-ttu-id="8e3a3-142">public boolean enforceRelationRules()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-142">public boolean enforceRelationRules()</span></span>                                                                                                       |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-143">public EntityRelationshipType entityRelationshipType()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-143">public EntityRelationshipType entityRelationshipType()</span></span>                                                                                      |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-144">public List extendedBy(\[boolean allLevels\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-144">public List extendedBy(\[boolean allLevels\])</span></span>                                                                                               |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-145">public TableId extends()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-145">public TableId extends()</span></span>                                                                                                                    | <span data-ttu-id="8e3a3-146">基本テーブルのテーブル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-146">Returns the table ID of a base table.</span></span>                                                                                                                                     |
| <span data-ttu-id="8e3a3-147">public int fieldCnt(\[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-147">public int fieldCnt(\[TableScope tableScope\])</span></span>                                                                                              | <span data-ttu-id="8e3a3-148">テーブルのフィールドの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-148">Returns the number of fields for a table.</span></span>                                                                                                                                 |
| <span data-ttu-id="8e3a3-149">public FieldId fieldCnt2Id(int cnt, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-149">public FieldId fieldCnt2Id(int cnt, \[TableScope tableScope\])</span></span>                                                                              | <span data-ttu-id="8e3a3-150">インデックスで指定されるフィールドのフィールド ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-150">Returns the field ID of the field that is specified by an index.</span></span>                                                                                                          |
| <span data-ttu-id="8e3a3-151">public str fieldGroup(int FieldGroupNumber, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-151">public str fieldGroup(int FieldGroupNumber, \[TableScope tableScope\])</span></span>                                                                      | <span data-ttu-id="8e3a3-152">インデックスで指定されるフィールド グループの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-152">Returns the name of a field group that is specified by index.</span></span>                                                                                                             |
| <span data-ttu-id="8e3a3-153">public int fieldGroupCnt(\[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-153">public int fieldGroupCnt(\[TableScope tableScope\])</span></span>                                                                                         | <span data-ttu-id="8e3a3-154">テーブルのフィールド グループの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-154">Returns the number of field groups for the table.</span></span>                                                                                                                         |
| <span data-ttu-id="8e3a3-155">public str fieldName(FieldId fieldId, \[DbBackend db\], \[int arrayindex\], \[FieldNameGenerationMode generationMode\], \[str tableAlias\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-155">public str fieldName(FieldId fieldId, \[DbBackend db\], \[int arrayindex\], \[FieldNameGenerationMode generationMode\], \[str tableAlias\])</span></span> | <span data-ttu-id="8e3a3-156">フィールド ID で指定されるフィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-156">Returns the name of the field that is specified by field ID.</span></span>                                                                                                              |
| <span data-ttu-id="8e3a3-157">public FieldId fieldName2Id(str name)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-157">public FieldId fieldName2Id(str name)</span></span>                                                                                                       | <span data-ttu-id="8e3a3-158">名前で指定されるフィールドのフィールド ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-158">Returns the field ID of a field that is specified by name.</span></span>                                                                                                                |
| <span data-ttu-id="8e3a3-159">public FieldId fieldNext(FieldId fieldId, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-159">public FieldId fieldNext(FieldId fieldId, \[TableScope tableScope\])</span></span>                                                                        | <span data-ttu-id="8e3a3-160">テーブルのフィールド反復処理中に、次のフィールド ID の値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-160">Returns the value of the next field ID during a field iteration of the table.</span></span>                                                                                             |
| <span data-ttu-id="8e3a3-161">public DictField fieldObject(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-161">public DictField fieldObject(FieldId fieldId)</span></span>                                                                                               | <span data-ttu-id="8e3a3-162">フィールド ID で指定されているフィールドの DictField クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-162">Creates an instance of the DictField class for the field that is specified by field ID.</span></span>                                                                                   |
| <span data-ttu-id="8e3a3-163">public IndexId fieldOrigin2Id(Guid fieldOrigin, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-163">public IndexId fieldOrigin2Id(Guid fieldOrigin, \[TableScope tableScope\])</span></span>                                                                  |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-164">public str fieldSqlDefault(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-164">public str fieldSqlDefault(FieldId fieldId)</span></span>                                                                                                 | <span data-ttu-id="8e3a3-165">フィールド ID で指定されているフィールドの SQL 既定値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-165">Returns the SQL default value for the field that is specified by field ID.</span></span>                                                                                                |
| <span data-ttu-id="8e3a3-166">public str formRef(\[boolean searchBaseTables\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-166">public str formRef(\[boolean searchBaseTables\])</span></span>                                                                                            | <span data-ttu-id="8e3a3-167">テーブルの既定のフォームの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-167">Returns the name of the default form for the table.</span></span>                                                                                                                       |
| <span data-ttu-id="8e3a3-168">public container getCountryRegionCodes()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-168">public container getCountryRegionCodes()</span></span>                                                                                                    |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-169">public FieldId getCountryRegionContextField()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-169">public FieldId getCountryRegionContextField()</span></span>                                                                                               |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-170">public FieldId getValidTimeStateValidFromFieldId()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-170">public FieldId getValidTimeStateValidFromFieldId()</span></span>                                                                                          |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-171">public FieldId getValidTimeStateValidToFieldId()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-171">public FieldId getValidTimeStateValidToFieldId()</span></span>                                                                                            |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-172">public boolean hasRecidIdx()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-172">public boolean hasRecidIdx()</span></span>                                                                                                                | <span data-ttu-id="8e3a3-173">テーブルのレコード ID インデックスが有効かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-173">Returns a value that indicates whether a record ID index for the table is in effect.</span></span>                                                                                      |
| <span data-ttu-id="8e3a3-174">public boolean hasSurrogateKey()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-174">public boolean hasSurrogateKey()</span></span>                                                                                                            |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-175">public TableId id()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-175">public TableId id()</span></span>                                                                                                                         | <span data-ttu-id="8e3a3-176">テーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-176">Returns the ID of the table.</span></span>                                                                                                                                              |
| <span data-ttu-id="8e3a3-177">public int indexCnt()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-177">public int indexCnt()</span></span>                                                                                                                       | <span data-ttu-id="8e3a3-178">テーブルのインデックスの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-178">Returns the number of indexes for the table.</span></span>                                                                                                                              |
| <span data-ttu-id="8e3a3-179">public IndexId indexCnt2Id(int cnt)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-179">public IndexId indexCnt2Id(int cnt)</span></span>                                                                                                         |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-180">public str indexName(IndexId indexId, \[DbBackend db\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-180">public str indexName(IndexId indexId, \[DbBackend db\])</span></span>                                                                                     | <span data-ttu-id="8e3a3-181">indexId パラメーターで指定された形式のインデックスの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-181">Returns the name of an index that is specified by the indexId parameter.</span></span>                                                                                                  |
| <span data-ttu-id="8e3a3-182">public IndexId indexName2Id(str name)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-182">public IndexId indexName2Id(str name)</span></span>                                                                                                       | <span data-ttu-id="8e3a3-183">名前で指定されているインデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-183">Returns the ID of an index that is specified by name.</span></span>                                                                                                                     |
| <span data-ttu-id="8e3a3-184">public IndexId indexNext(IndexId id)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-184">public IndexId indexNext(IndexId id)</span></span>                                                                                                        | <span data-ttu-id="8e3a3-185">テーブルのインデックス反復処理中に、次のインデックス ID の値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-185">Returns the value of the next index ID during an index iteration of the table.</span></span>                                                                                            |
| <span data-ttu-id="8e3a3-186">public DictIndex indexObject(IndexId indexId)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-186">public DictIndex indexObject(IndexId indexId)</span></span>                                                                                               | <span data-ttu-id="8e3a3-187">ID で指定されているインデックスの DictTable クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-187">Creates an instance of the DictTable class for the index that is specified by ID.</span></span>                                                                                         |
| <span data-ttu-id="8e3a3-188">public IndexId indexUnique()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-188">public IndexId indexUnique()</span></span>                                                                                                                | <span data-ttu-id="8e3a3-189">テーブルの一意のインデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-189">Returns the ID of the unique index for the table.</span></span>                                                                                                                         |
| <span data-ttu-id="8e3a3-190">public FieldId instanceRelationType()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-190">public FieldId instanceRelationType()</span></span>                                                                                                       |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-191">public boolean isAbstract()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-191">public boolean isAbstract()</span></span>                                                                                                                 | <span data-ttu-id="8e3a3-192">このテーブルが抽象かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-192">Indicates whether this table is abstract.</span></span>                                                                                                                                 |
| <span data-ttu-id="8e3a3-193">public boolean isBaseData()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-193">public boolean isBaseData()</span></span>                                                                                                                 | <span data-ttu-id="8e3a3-194">テーブル コンテンツが基本データであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-194">Indicates whether the table content is base data.</span></span>                                                                                                                         |
| <span data-ttu-id="8e3a3-195">public boolean isDefaultData()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-195">public boolean isDefaultData()</span></span>                                                                                                              | <span data-ttu-id="8e3a3-196">テーブルが既定のデータを含むかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-196">Indicates whether the table contains default data.</span></span>                                                                                                                        |
| <span data-ttu-id="8e3a3-197">public boolean isDerivedFrom(TableName baseTableName)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-197">public boolean isDerivedFrom(TableName baseTableName)</span></span>                                                                                       | <span data-ttu-id="8e3a3-198">1 つのテーブル タイプが別から派生しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-198">Indicates whether one table type derives from another.</span></span>                                                                                                                    |
| <span data-ttu-id="8e3a3-199">public boolean isMap()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-199">public boolean isMap()</span></span>                                                                                                                      | <span data-ttu-id="8e3a3-200">テーブルがマップであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-200">Indicates whether the table is a map.</span></span>                                                                                                                                     |
| <span data-ttu-id="8e3a3-201">public boolean isSql()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-201">public boolean isSql()</span></span>                                                                                                                      | <span data-ttu-id="8e3a3-202">テーブルが SQL テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-202">Indicates whether the table is an SQL table.</span></span>                                                                                                                              |
| <span data-ttu-id="8e3a3-203">public boolean isSystemTable()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-203">public boolean isSystemTable()</span></span>                                                                                                              | <span data-ttu-id="8e3a3-204">テーブルがシステム テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-204">Indicates whether the table is a system table.</span></span>                                                                                                                            |
| <span data-ttu-id="8e3a3-205">public boolean isTempDb()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-205">public boolean isTempDb()</span></span>                                                                                                                   |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-206">public boolean isTmp()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-206">public boolean isTmp()</span></span>                                                                                                                      | <span data-ttu-id="8e3a3-207">テーブルが一時テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-207">Indicates whether the table is a temporary table.</span></span>                                                                                                                         |
| <span data-ttu-id="8e3a3-208">public boolean isUnionAllView()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-208">public boolean isUnionAllView()</span></span>                                                                                                             |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-209">public boolean isValidTimeStateTable()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-209">public boolean isValidTimeStateTable()</span></span>                                                                                                      |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-210">public boolean isView()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-210">public boolean isView()</span></span>                                                                                                                     | <span data-ttu-id="8e3a3-211">テーブルがビューであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-211">Indicates whether the table is a view.</span></span>                                                                                                                                    |
| <span data-ttu-id="8e3a3-212">public str label()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-212">public str label()</span></span>                                                                                                                          | <span data-ttu-id="8e3a3-213">テーブルのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-213">Returns the label text for the table.</span></span>                                                                                                                                     |
| <span data-ttu-id="8e3a3-214">public str labelDefined()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-214">public str labelDefined()</span></span>                                                                                                                   | <span data-ttu-id="8e3a3-215">テーブルの label プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-215">Returns the value of the label property for the table.</span></span>                                                                                                                    |
| <span data-ttu-id="8e3a3-216">public str listPageRef(\[boolean searchBaseTables\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-216">public str listPageRef(\[boolean searchBaseTables\])</span></span>                                                                                        |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-217">public Common makeRecord()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-217">public Common makeRecord()</span></span>                                                                                                                  | <span data-ttu-id="8e3a3-218">テーブルの空白のレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-218">Creates a blank record for the table.</span></span>                                                                                                                                     |
| <span data-ttu-id="8e3a3-219">public AccessType maxAccessMode()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-219">public AccessType maxAccessMode()</span></span>                                                                                                           | <span data-ttu-id="8e3a3-220">AOT 内で設定されているとおり、テーブルの MaxAccessMode プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-220">Returns the value of the MaxAccessMode property for a table, as set in the AOT.</span></span>                                                                                           |
| <span data-ttu-id="8e3a3-221">public str name(\[DbBackend db\], \[boolean pseudoname\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-221">public str name(\[DbBackend db\], \[boolean pseudoname\])</span></span>                                                                                   | <span data-ttu-id="8e3a3-222">テーブル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-222">Retrieves the name of the table.</span></span>                                                                                                                                          |
| <span data-ttu-id="8e3a3-223">public str objectMethod(int methodNumber, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-223">public str objectMethod(int methodNumber, \[TableScope tableScope\])</span></span>                                                                        | <span data-ttu-id="8e3a3-224">インデックスで指定されるインスタンス メソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-224">Returns the name of an instance method that is specified by index.</span></span>                                                                                                        |
| <span data-ttu-id="8e3a3-225">public int objectMethodCnt(\[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-225">public int objectMethodCnt(\[TableScope tableScope\])</span></span>                                                                                       | <span data-ttu-id="8e3a3-226">テーブルのインスタンス メソッドの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-226">Returns the number of instance methods for the table.</span></span>                                                                                                                     |
| <span data-ttu-id="8e3a3-227">public DictMethod objectMethodObject(int methodNumber, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-227">public DictMethod objectMethodObject(int methodNumber, \[TableScope tableScope\])</span></span>                                                           | <span data-ttu-id="8e3a3-228">インデックスにより指定されているオブジェクト メソッドの MethodInfo クラスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-228">Returns an instance of the MethodInfo class for an object method that is specified by index.</span></span>                                                                              |
| <span data-ttu-id="8e3a3-229">public DictTableMap mapObject(int methodNumber)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-229">public DictTableMap mapObject(int methodNumber)</span></span>                                                                                             | <span data-ttu-id="8e3a3-230">インデックスで指定されているマッピングに対する \[t: DictTableMap\] クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-230">Creates an instance of the \[T: DictTableMap\] class for a mapping that is specified by index.</span></span>                                                                            |
| <span data-ttu-id="8e3a3-231">public int mapCnt()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-231">public int mapCnt()</span></span>                                                                                                                         | <span data-ttu-id="8e3a3-232">この DictTable インスタンスにより指定されているマップの使用可能なテーブル マッピングの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-232">Returns the count of available table mappings for the map that is specified by this DictTable instance.</span></span>                                                                   |
| <span data-ttu-id="8e3a3-233">public boolean occEnabled()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-233">public boolean occEnabled()</span></span>                                                                                                                 | <span data-ttu-id="8e3a3-234">テーブルに対してオプティミスティック同時実行モードが有効になっているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-234">Indicates whether the optimistic concurrency mode has been enabled for a table.</span></span>                                                                                           |
| <span data-ttu-id="8e3a3-235">public IndexId primaryIndex(\[boolean asDefinedInAOT\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-235">public IndexId primaryIndex(\[boolean asDefinedInAOT\])</span></span>                                                                                     | <span data-ttu-id="8e3a3-236">テーブルのプライマリ インデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-236">Returns the ID of the primary index for the table.</span></span>                                                                                                                        |
| <span data-ttu-id="8e3a3-237">public FieldId primaryKeyField()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-237">public FieldId primaryKeyField()</span></span>                                                                                                            | <span data-ttu-id="8e3a3-238">テーブルの主キーに使用されているフィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-238">Returns the ID of the field that is used for the primary key of the table.</span></span>                                                                                                |
| <span data-ttu-id="8e3a3-239">public str relation(int RelationNumber, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-239">public str relation(int RelationNumber, \[TableScope tableScope\])</span></span>                                                                          | <span data-ttu-id="8e3a3-240">インデックスで指定される関係の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-240">Returns the name of a relation that is specified by index.</span></span>                                                                                                                |
| <span data-ttu-id="8e3a3-241">public int relationCnt(\[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-241">public int relationCnt(\[TableScope tableScope\])</span></span>                                                                                           | <span data-ttu-id="8e3a3-242">テーブルの関係の数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-242">Returns the number of relations for the table.</span></span>                                                                                                                            |
| <span data-ttu-id="8e3a3-243">public IndexId replacementKey()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-243">public IndexId replacementKey()</span></span>                                                                                                             |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-244">public str reportRef()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-244">public str reportRef()</span></span>                                                                                                                      | <span data-ttu-id="8e3a3-245">テーブルの既定のレポートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-245">Returns the name of the default report for the table.</span></span>                                                                                                                     |
| <span data-ttu-id="8e3a3-246">public AccessType rights(\[boolean ignoreContext\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-246">public AccessType rights(\[boolean ignoreContext\])</span></span>                                                                                         | <span data-ttu-id="8e3a3-247">テーブルに指定されている、現在のユーザーのアクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-247">Returns the access rights of the current user that is specified for the table.</span></span>                                                                                            |
| <span data-ttu-id="8e3a3-248">public SecurityKeyId securityKeyId()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-248">public SecurityKeyId securityKeyId()</span></span>                                                                                                        | <span data-ttu-id="8e3a3-249">テーブルのセキュリティ キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-249">Returns the ID of the security key for the table.</span></span>                                                                                                                         |
| <span data-ttu-id="8e3a3-250">public str singularLabel(\[boolean labelTranslation\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-250">public str singularLabel(\[boolean labelTranslation\])</span></span>                                                                                      |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-251">public str staticMethod(int methodNumber)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-251">public str staticMethod(int methodNumber)</span></span>                                                                                                   | <span data-ttu-id="8e3a3-252">インデックスで指定される静的メソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-252">Returns the name of a static method that is specified by index.</span></span>                                                                                                           |
| <span data-ttu-id="8e3a3-253">public int staticMethodCnt()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-253">public int staticMethodCnt()</span></span>                                                                                                                | <span data-ttu-id="8e3a3-254">テーブルの静的メソッドの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-254">Returns the number of static methods for the table.</span></span>                                                                                                                       |
| <span data-ttu-id="8e3a3-255">public DictMethod staticMethodObject(int methodNumber)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-255">public DictMethod staticMethodObject(int methodNumber)</span></span>                                                                                      | <span data-ttu-id="8e3a3-256">インデックスにより指定されている静的メソッドの MethodInfo クラスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-256">Returns an instance of the MethodInfo class for a static method that is specified by index.</span></span>                                                                               |
| <span data-ttu-id="8e3a3-257">public boolean supportInheritance()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-257">public boolean supportInheritance()</span></span>                                                                                                         |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-258">public TableGroup tableGroup()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-258">public TableGroup tableGroup()</span></span>                                                                                                              | <span data-ttu-id="8e3a3-259">テーブルのテーブル グループを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-259">Returns the table group for a table.</span></span>                                                                                                                                      |
| <span data-ttu-id="8e3a3-260">public TableType tableType()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-260">public TableType tableType()</span></span>                                                                                                                | <span data-ttu-id="8e3a3-261">テーブルのタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-261">Indicates the type of the table.</span></span>                                                                                                                                          |
| <span data-ttu-id="8e3a3-262">public FieldId titleField1(\[boolean includeBaseTables\], \[boolean extendedFieldId\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-262">public FieldId titleField1(\[boolean includeBaseTables\], \[boolean extendedFieldId\])</span></span>                                                      | <span data-ttu-id="8e3a3-263">テーブルの titleField1 プロパティを表すフィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-263">Returns the ID of the field that represents the titleField1 property of the table.</span></span>                                                                                        |
| <span data-ttu-id="8e3a3-264">public FieldId titleField2(\[boolean includeBaseTables\], \[boolean extendedFieldId\])</span><span class="sxs-lookup"><span data-stu-id="8e3a3-264">public FieldId titleField2(\[boolean includeBaseTables\], \[boolean extendedFieldId\])</span></span>                                                      | <span data-ttu-id="8e3a3-265">テーブルの titleField2 プロパティを表すフィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-265">Returns the ID of the field that represents the titleField2 property of the table.</span></span>                                                                                        |
| <span data-ttu-id="8e3a3-266">public boolean validRelationship()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-266">public boolean validRelationship()</span></span>                                                                                                          |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-267">public boolean visible()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-267">public boolean visible()</span></span>                                                                                                                    | <span data-ttu-id="8e3a3-268">テーブルが表示できるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-268">Determines whether the table is visible.</span></span>                                                                                                                                  |
| <span data-ttu-id="8e3a3-269">::public static DictTable construct(str tableName)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-269">::public static DictTable construct(str tableName)</span></span>                                                                                          |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-270">::public static RecId getRelationTypeFromTableName(TableName tableName)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-270">::public static RecId getRelationTypeFromTableName(TableName tableName)</span></span>                                                                     |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-271">::public static TableName getTableNameFromRelationType(RecId relationType)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-271">::public static TableName getTableNameFromRelationType(RecId relationType)</span></span>                                                                  |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-272">::public static Common createRecord(str tableName)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-272">::public static Common createRecord(str tableName)</span></span>                                                                                          |                                                                                                                                                                           |
| <span data-ttu-id="8e3a3-273">public void reloadSecurity()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-273">public void reloadSecurity()</span></span>                                                                                                                | <span data-ttu-id="8e3a3-274">テーブルの機能キー システムを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-274">Reloads the feature key system for the table.</span></span>                                                                                                                             |
| <span data-ttu-id="8e3a3-275">public void new(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="8e3a3-275">public void new(TableId tableId)</span></span>                                                                                                            | <span data-ttu-id="8e3a3-276">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-276">Initializes a new instance of the Object class.</span></span>                                                                                                                           |
| <span data-ttu-id="8e3a3-277">public void reindex()</span><span class="sxs-lookup"><span data-stu-id="8e3a3-277">public void reindex()</span></span>                                                                                                                       | <span data-ttu-id="8e3a3-278">テーブルのインデックスの再作成を実行します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-278">Performs a reindex of the table.</span></span>                                                                                                                                          |

## <a name="method-doesmethodexist"></a><span data-ttu-id="8e3a3-279">メソッド doesMethodExist</span><span class="sxs-lookup"><span data-stu-id="8e3a3-279">Method doesMethodExist</span></span>

<span data-ttu-id="8e3a3-280">指定されたメソッドがテーブルに存在するかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-280">Checks whether a given method exists on the table.</span></span>

```xpp
public boolean doesMethodExist(str name)
```

### <a name="parameters---doesmethodexist"></a><span data-ttu-id="8e3a3-281">パラメーター - doesMethodExist</span><span class="sxs-lookup"><span data-stu-id="8e3a3-281">Parameters - doesMethodExist</span></span>

<span data-ttu-id="8e3a3-282">名前</span><span class="sxs-lookup"><span data-stu-id="8e3a3-282">name</span></span>  

### <a name="return-value---doesmethodexist"></a><span data-ttu-id="8e3a3-283">戻り値 - doesMethodExist</span><span class="sxs-lookup"><span data-stu-id="8e3a3-283">Return Value - doesMethodExist</span></span>

<span data-ttu-id="8e3a3-284">指定メソッドがテーブル上に存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-284">true if the given method exists on the table; otherwise, false.</span></span>

### <a name="remarks---doesmethodexist"></a><span data-ttu-id="8e3a3-285">備考 - doesMethodExist</span><span class="sxs-lookup"><span data-stu-id="8e3a3-285">Remarks - doesMethodExist</span></span>

<span data-ttu-id="8e3a3-286">この API は、メソッドが正常にコンパイルされているかどうかを確認せずに、メソッドがテーブルに存在するかどうかを確認するために推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-286">This API is the preferred way to check whether a method exists on the table without checking whether the method compiled successfully.</span></span>

## <a name="method-aosauthsetting"></a><span data-ttu-id="8e3a3-287">メソッド AOSAuthSetting</span><span class="sxs-lookup"><span data-stu-id="8e3a3-287">Method AOSAuthSetting</span></span>

<span data-ttu-id="8e3a3-288">ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定する AOSAuthorization システム列挙値を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-288">Retrieves an AOSAuthorization system enumeration value that specifies the type of operation that a user can perform on a table, depending on the permissions of the user.</span></span>

```xpp
public AOSAuthorization AOSAuthSetting()
```

### <a name="return-value---aosauthsetting"></a><span data-ttu-id="8e3a3-289">戻り値 - AOSAuthSetting</span><span class="sxs-lookup"><span data-stu-id="8e3a3-289">Return Value - AOSAuthSetting</span></span>

<span data-ttu-id="8e3a3-290">AOSAuthorization システム列挙値です。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-290">An AOSAuthorization system enumeration value.</span></span>

### <a name="remarks---aosauthsetting"></a><span data-ttu-id="8e3a3-291">備考 - AOSAuthSetting</span><span class="sxs-lookup"><span data-stu-id="8e3a3-291">Remarks - AOSAuthSetting</span></span>

<span data-ttu-id="8e3a3-292">AOSAuthorization::None 値は、承認チェックが実行されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-292">The AOSAuthorization::None value indicates that an authorization check is not performed.</span></span> <span data-ttu-id="8e3a3-293">テーブルの AOSAuthorization プロパティを設定するには、テーブルのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-293">Use table properties to set the AOSAuthorization property for a table.</span></span> <span data-ttu-id="8e3a3-294">アプリケーション オブジェクト ツリー (AOT) で、テーブルを右クリックしてからプロパティをクリックしてテーブルのプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-294">In the Application Object Tree (AOT), right-click the table, and then click Properties to access the table properties.</span></span>

### <a name="examples---aosauthsetting"></a><span data-ttu-id="8e3a3-295">例 - AOSAuthSetting</span><span class="sxs-lookup"><span data-stu-id="8e3a3-295">Examples - AOSAuthSetting</span></span>

<span data-ttu-id="8e3a3-296">次の例は、AOSAuthSetting メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-296">This following example shows a call to the AOSAuthSetting method.</span></span>

```xpp
static public void Main(Args _args) 
{ 
    DictTable dt; 
    AOSAuthorization a; 
    dt = new DictTable(tablenum(CustTable)); 
    a = dt.AOSAuthSetting(); 
}
```

## <a name="method-cachelookup"></a><span data-ttu-id="8e3a3-297">メソッド cacheLookup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-297">Method cacheLookup</span></span>

<span data-ttu-id="8e3a3-298">テーブルのレコード キャッシュ レベルを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-298">Returns the record cache level for the table.</span></span>

```xpp
public RecordCacheLevel cacheLookup()
```

### <a name="return-value---cachelookup"></a><span data-ttu-id="8e3a3-299">戻り値 - cacheLookup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-299">Return Value - cacheLookup</span></span>

<span data-ttu-id="8e3a3-300">テーブルのレコード キャッシュ レベルを示す RecordCacheLevel 値。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-300">A RecordCacheLevel value that indicates the record cache level for the table.</span></span>

### <a name="examples---cachelookup"></a><span data-ttu-id="8e3a3-301">例 - cacheLookup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-301">Examples - cacheLookup</span></span>

<span data-ttu-id="8e3a3-302">次の例は、テーブルのキャッシュ レベルの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-302">The following example shows the retrieval of the cache level for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print dt.cacheLookup(); 
}
```

## <a name="method-cachesize"></a><span data-ttu-id="8e3a3-303">メソッド cacheSize</span><span class="sxs-lookup"><span data-stu-id="8e3a3-303">Method cacheSize</span></span>

<span data-ttu-id="8e3a3-304">テーブルのキャッシュ サイズをレコードの数で返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-304">Returns the cache size for the table, in the number of records.</span></span>

```xpp
public int cacheSize()
```

### <a name="return-value---cachesize"></a><span data-ttu-id="8e3a3-305">戻り値 - cacheSize</span><span class="sxs-lookup"><span data-stu-id="8e3a3-305">Return Value - cacheSize</span></span>

<span data-ttu-id="8e3a3-306">テーブルのキャッシュ サイズです。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-306">The cache size for the table.</span></span>

### <a name="examples---cachesize"></a><span data-ttu-id="8e3a3-307">例 - cacheSize</span><span class="sxs-lookup"><span data-stu-id="8e3a3-307">Examples - cacheSize</span></span>

<span data-ttu-id="8e3a3-308">次の例では、テーブルのキャッシュ サイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-308">The following example retrieves the cache size for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(SysUserInfo)); 
if (dt) 
{ 
     print strfmt("Cache size: %1", dt.cacheSize()); 
}
```

## <a name="method-callobject"></a><span data-ttu-id="8e3a3-309">メソッド callObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-309">Method callObject</span></span>

<span data-ttu-id="8e3a3-310">テーブルの指定されたオブジェクトのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-310">Calls the specified object method for a table.</span></span>

```xpp
public AnyType callObject(str methodName, Common Called, VarArg )
```

### <a name="parameters---callobject"></a><span data-ttu-id="8e3a3-311">パラメータ - callObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-311">Parameters - callObject</span></span>

<span data-ttu-id="8e3a3-312">methodName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-312">methodName</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-313">呼び出された</span><span class="sxs-lookup"><span data-stu-id="8e3a3-313">Called</span></span>  

<!-- -->


### <a name="return-value---callobject"></a><span data-ttu-id="8e3a3-314">戻り値 - callObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-314">Return Value - callObject</span></span>

<span data-ttu-id="8e3a3-315">methodName パラメーターへの呼び出しの結果。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-315">The results of the call to the methodName parameter.</span></span>

### <a name="remarks---callobject"></a><span data-ttu-id="8e3a3-316">備考 - callObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-316">Remarks - callObject</span></span>

<span data-ttu-id="8e3a3-317">攻撃者が callObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-317">If an attacker can control input to the callObject method, a security risk exists.</span></span> <span data-ttu-id="8e3a3-318">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-318">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="8e3a3-319">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-319">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="8e3a3-320">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-320">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---callobject"></a><span data-ttu-id="8e3a3-321">例 - callObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-321">Examples - callObject</span></span>

<span data-ttu-id="8e3a3-322">この例では、SysUserLog テーブルの SysUserLog.onlineTime 静的メソッドを呼び出し、呼び出しから返された値を出力します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-322">This example calls the SysUserLog.onlineTime static method in the SysUserLog table and then prints the value that is returned from the call.</span></span>

```xpp
{ 
    Dicttable         dictTable; 
    int               onlineTime; 
    Common            common; 
    str               resultOutput; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    dictTable= new DictTable(tablenum(SysUserLog)); 
    if (dictTable != null) 
    { 
        common = dictTable.makeRecord(); 
        // Grants permission to execute the 
        // DictTable.callObject method. DictTable.callObject runs 
        // under code access security. 
        perm.assert(); 
        onlineTime   = dictTable.callObject("onlineTime", common); 
        resultOutput = strfmt("User online time is %1", onlineTime); 
        print resultOutput; 
        pause; 
    } 
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-callstatic"></a><span data-ttu-id="8e3a3-323">メソッド callStatic</span><span class="sxs-lookup"><span data-stu-id="8e3a3-323">Method callStatic</span></span>

<span data-ttu-id="8e3a3-324">テーブルの指定された静的メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-324">Calls the specified static method for a table.</span></span>

```xpp
public AnyType callStatic(str methodName, VarArg )
```

### <a name="parameters---callstatic"></a><span data-ttu-id="8e3a3-325">パラメーター - callStatic</span><span class="sxs-lookup"><span data-stu-id="8e3a3-325">Parameters - callStatic</span></span>

<span data-ttu-id="8e3a3-326">methodName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-326">methodName</span></span>  

<!-- -->


### <a name="return-value---callstatic"></a><span data-ttu-id="8e3a3-327">戻り値 - callStatic</span><span class="sxs-lookup"><span data-stu-id="8e3a3-327">Return Value - callStatic</span></span>

<span data-ttu-id="8e3a3-328">methodName パラメーターへの呼び出しの結果。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-328">The results of the call to the methodName parameter.</span></span>

### <a name="remarks---callstatic"></a><span data-ttu-id="8e3a3-329">備考 - callStatic</span><span class="sxs-lookup"><span data-stu-id="8e3a3-329">Remarks - callStatic</span></span>

<span data-ttu-id="8e3a3-330">攻撃者がこの機能への入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-330">If an attacker can control input to this function, a security risk exists.</span></span> <span data-ttu-id="8e3a3-331">したがって、callStatic メソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-331">Therefore, the callStatic method runs under Code Access Security.</span></span> <span data-ttu-id="8e3a3-332">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-332">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="8e3a3-333">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-333">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---callstatic"></a><span data-ttu-id="8e3a3-334">例 - callStatic</span><span class="sxs-lookup"><span data-stu-id="8e3a3-334">Examples - callStatic</span></span>

<span data-ttu-id="8e3a3-335">この例では、SysUserInfo テーブル内の SysUserInfo:find static method メソッドを呼び出し、呼び出しから返された値を callStatic メソッドに出力します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-335">This example calls the SysUserInfo:find static method in the SysUserInfo table and then prints the value that is returned from the call to the callStatic method.</span></span>

```xpp
 { 
    Dicttable   dictTable; 
    SysUserInfo userInfo; 
    str         resultOutput; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    // Grants permission to execute the DictTable.callStatic method. 
    // DictTable.callStatic runs under code access security. 
    perm.assert(); 
    dictTable= new DictTable(tablenum(SysUserInfo)); 
    if (dictTable != null) 
    { 
        userInfo     = dictTable.callStatic("find"); 
        resultOutput = strfmt("Current user ID is %1", userInfo.Id); 
        print resultOutput; 
        pause; 
    } 
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-clusterindex"></a><span data-ttu-id="8e3a3-336">メソッド clusterIndex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-336">Method clusterIndex</span></span>

<span data-ttu-id="8e3a3-337">テーブルのクラスター化されたインデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-337">Returns the ID of the clustered index for the table.</span></span>

```xpp
public IndexId clusterIndex([boolean asDefinedInAOT])
```

### <a name="parameters---clusterindex"></a><span data-ttu-id="8e3a3-338">パラメーター - clusterIndex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-338">Parameters - clusterIndex</span></span>

<span data-ttu-id="8e3a3-339">asDefinedInAOT</span><span class="sxs-lookup"><span data-stu-id="8e3a3-339">asDefinedInAOT</span></span>  
<span data-ttu-id="8e3a3-340">取得するクラスター インデックスが AOT で定義されているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-340">A value that indicates whether the clustered index to retrieve is defined in the AOT.</span></span> <span data-ttu-id="8e3a3-341">true の値は、AOT で定義されたクラスター インデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-341">A value of true returns the clustered index as defined in the AOT.</span></span> <span data-ttu-id="8e3a3-342">false の値は、SQL テーブルで定義されたクラスター インデックスを返します、オプション。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-342">A value of false returns the clustered index as defined in the SQL table; optional.</span></span>

### <a name="return-value---clusterindex"></a><span data-ttu-id="8e3a3-343">戻り値 - clusterIndex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-343">Return Value - clusterIndex</span></span>

<span data-ttu-id="8e3a3-344">テーブルのクラスター化されたインデックスの ID。テーブルのクラスター化されたインデックスがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-344">The ID of the clustered index for the table; 0 (zero) if there is no clustered index for the table.</span></span>

### <a name="examples---clusterindex"></a><span data-ttu-id="8e3a3-345">例 - clusterIndex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-345">Examples - clusterIndex</span></span>

<span data-ttu-id="8e3a3-346">次の例は、テーブルのクラスター インデックスの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-346">The following example shows the retrieval of the clustered index for a table.</span></span>

```xpp
DictTable dt; 
DictIndex di; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    i = dt.clusterIndex(); 
    if (0 != i) 
    { 
        di = new DictIndex(tablenum(CustTable), i); 
        print di.name(); 
    } 
}
```

## <a name="method-configurationkeyid"></a><span data-ttu-id="8e3a3-347">メソッド configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-347">Method configurationKeyId</span></span>

<span data-ttu-id="8e3a3-348">テーブルのコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-348">Returns the ID of the configuration key for the table.</span></span>

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a><span data-ttu-id="8e3a3-349">戻り値 - configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-349">Return Value - configurationKeyId</span></span>

<span data-ttu-id="8e3a3-350">テーブルのコンフィギュレーション キーの ID。テーブルのコンフィギュレーション キーがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-350">The ID of the configuration key for the table; 0 (zero) if there is no configuration key for the table.</span></span>

### <a name="examples---configurationkeyid"></a><span data-ttu-id="8e3a3-351">例 - configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-351">Examples - configurationKeyId</span></span>

<span data-ttu-id="8e3a3-352">次の例は、テーブルのコンフィギュレーション キー ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-352">The following example shows the retrieval of the configuration key ID for a table.</span></span>

```xpp
DictTable dt; 
DictConfigurationKey dck; 
dt = new DictTable(tablenum(AddressCountryRegionBLWI)); 
if (dt) 
{ 
    if (0 != dt.configurationKeyId()) 
    dck = new DictConfigurationKey(dt.configurationKeyId()); 
    if (dck) 
    { 
        print (strfmt("The table's configuration key is %1.", dck.name())); 
    } 
}
```

## <a name="method-dataperpartition"></a><span data-ttu-id="8e3a3-353">メソッド dataPerPartition</span><span class="sxs-lookup"><span data-stu-id="8e3a3-353">Method dataPerPartition</span></span>

<span data-ttu-id="8e3a3-354">テーブルのデータがパーティション単位で保存されるかどうかと、テーブルの SaveDataPerPartition プロパティに対応するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-354">Returns a value that indicates whether the data of the table is saved on a per-partition basis, and corresponds to the SaveDataPerPartition property of the table.</span></span>

```xpp
public boolean dataPerPartition()
```

### <a name="return-value---dataperpartition"></a><span data-ttu-id="8e3a3-355">戻り値 - dataPerPartition</span><span class="sxs-lookup"><span data-stu-id="8e3a3-355">Return Value - dataPerPartition</span></span>

<span data-ttu-id="8e3a3-356">データがパーティション単位で保存される場合は true。それ以外の場合は false で、データはすべてのパーティションに対してグローバルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-356">true if the data is saved on a per-partition basis; otherwise, false, and the data is saved globally for all partitions.</span></span>

## <a name="method-dataprcompany"></a><span data-ttu-id="8e3a3-357">メソッド dataPrCompany</span><span class="sxs-lookup"><span data-stu-id="8e3a3-357">Method dataPrCompany</span></span>

<span data-ttu-id="8e3a3-358">テーブルのデータが会社単位で保存されるかどうかと、テーブルの SaveDataPerCompany プロパティに対応するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-358">Returns a value that indicates whether the data of the table is saved on a per-company basis, and corresponds to the SaveDataPerCompany property of the table.</span></span>

```xpp
public boolean dataPrCompany()
```

### <a name="return-value---dataprcompany"></a><span data-ttu-id="8e3a3-359">戻り値 - dataPrCompany</span><span class="sxs-lookup"><span data-stu-id="8e3a3-359">Return Value - dataPrCompany</span></span>

<span data-ttu-id="8e3a3-360">データが会社単位で保存される場合は true。それ以外の場合は false で、データはすべての会社に対してグローバルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-360">true if the data is saved on a per-company basis; otherwise, false, and the data is saved globally for all companies.</span></span>

### <a name="examples---dataprcompany"></a><span data-ttu-id="8e3a3-361">例 - dataPrCompany</span><span class="sxs-lookup"><span data-stu-id="8e3a3-361">Examples - dataPrCompany</span></span>

<span data-ttu-id="8e3a3-362">次の例は、データが会社ごとに保存されるかどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-362">The following example shows the retrieval of the value that indicates whether the data is saved on a per-company basis.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table is saved on a %1 basis.", dt.dataPrCompany() ? "per company" : "global")); 
}
```

## <a name="method-deleteactioncnt"></a><span data-ttu-id="8e3a3-363">メソッド deleteActionCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-363">Method deleteActionCnt</span></span>

<span data-ttu-id="8e3a3-364">テーブルの削除アクションの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-364">Retrieves the number of delete actions for the table.</span></span>

```xpp
public int deleteActionCnt()
```

### <a name="return-value---deleteactioncnt"></a><span data-ttu-id="8e3a3-365">戻り値 - deleteActionCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-365">Return Value - deleteActionCnt</span></span>

<span data-ttu-id="8e3a3-366">テーブルの削除アクションの数。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-366">The number of delete actions for the table.</span></span>

### <a name="examples---deleteactioncnt"></a><span data-ttu-id="8e3a3-367">例 - deleteActionCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-367">Examples - deleteActionCnt</span></span>

<span data-ttu-id="8e3a3-368">次の例は、テーブルの削除アクション数の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-368">The following example shows the retrieval of the number of delete actions for the table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 delete actions.", dt.deleteActionCnt())); 
}
```

## <a name="method-deleteactionrelation"></a><span data-ttu-id="8e3a3-369">メソッド deleteActionRelation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-369">Method deleteActionRelation</span></span>

```xpp
public str deleteActionRelation(int cnt)
```

### <a name="parameters---deleteactionrelation"></a><span data-ttu-id="8e3a3-370">パラメーター - deleteActionRelation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-370">Parameters - deleteActionRelation</span></span>

<span data-ttu-id="8e3a3-371">cnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-371">cnt</span></span>  

### <a name="return-value---deleteactionrelation"></a><span data-ttu-id="8e3a3-372">戻り値 - deleteActionRelation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-372">Return Value - deleteActionRelation</span></span>

## <a name="method-deleteactiontableid"></a><span data-ttu-id="8e3a3-373">メソッド deleteActionTableId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-373">Method deleteActionTableId</span></span>

<span data-ttu-id="8e3a3-374">インデックスで指定されているテーブルの削除アクションのテーブル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-374">Returns the table ID of a table's delete action that is specified by an index.</span></span>

```xpp
public TableId deleteActionTableId(int cnt)
```

### <a name="parameters---deleteactiontableid"></a><span data-ttu-id="8e3a3-375">パラメーター - deleteActionTableId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-375">Parameters - deleteActionTableId</span></span>

<span data-ttu-id="8e3a3-376">cnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-376">cnt</span></span>  
<span data-ttu-id="8e3a3-377">テーブルの削除アクションのリストへの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-377">A one-based index to the list of the delete actions for the table.</span></span> <span data-ttu-id="8e3a3-378">リストは AOT の順です。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-378">The list is in AOT order.</span></span>

### <a name="return-value---deleteactiontableid"></a><span data-ttu-id="8e3a3-379">戻り値 - deleteActionTableId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-379">Return Value - deleteActionTableId</span></span>

<span data-ttu-id="8e3a3-380">cnt によって指定されたテーブルの削除アクションのテーブル ID。cnt 値が有効な削除アクション索引を表していない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-380">The table ID of the table's delete action that is specified by cnt; 0 (zero) if the cnt value does not represent a valid delete action index.</span></span>

### <a name="examples---deleteactiontableid"></a><span data-ttu-id="8e3a3-381">例 - deleteActionTableId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-381">Examples - deleteActionTableId</span></span>

<span data-ttu-id="8e3a3-382">次の例は、deleteActionTableId メソッドを使用して CustTable テーブルの削除アクションを持つテーブルの名前を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-382">The following example shows the use of the deleteActionTableId method to retrieve the names of tables that have delete actions for the CustTable table.</span></span>

```xpp
DictTable dt, dt2; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.deleteActionCnt(); i++) 
    { 
        dt2 = new DictTable(dt.deleteActionTableId(i)); 
        if (dt2) 
        { 
            print dt2.name(); 
        } 
    } 
}
```

## <a name="method-deleteactiontype"></a><span data-ttu-id="8e3a3-383">メソッド deleteActionType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-383">Method deleteActionType</span></span>

<span data-ttu-id="8e3a3-384">テーブルの削除アクションの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-384">Retrieves the type of a delete action for a table.</span></span>

```xpp
public int deleteActionType(int cnt)
```

### <a name="parameters---deleteactiontype"></a><span data-ttu-id="8e3a3-385">パラメーター - deleteActionType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-385">Parameters - deleteActionType</span></span>

<span data-ttu-id="8e3a3-386">cnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-386">cnt</span></span>  
<span data-ttu-id="8e3a3-387">テーブルの削除アクションのリストへの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-387">The one-based index to the list of the delete actions for the table.</span></span> <span data-ttu-id="8e3a3-388">リストは AOT の順です。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-388">The list is in AOT order.</span></span>

### <a name="return-value---deleteactiontype"></a><span data-ttu-id="8e3a3-389">戻り値 - deleteActionType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-389">Return Value - deleteActionType</span></span>

<span data-ttu-id="8e3a3-390">cnt パラメーターで指定されているテーブルの削除アクションのタイプを表す整数。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-390">An integer that represents the type of the delete action of the table that is specified by the cnt parameter.</span></span> <span data-ttu-id="8e3a3-391">これは、次のテーブルの値の 1 つになります。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-391">It can be one of the values in the following table.</span></span>

|     |                      |
|-----|----------------------|
| <span data-ttu-id="8e3a3-392">0</span><span class="sxs-lookup"><span data-stu-id="8e3a3-392">0</span></span>   | <span data-ttu-id="8e3a3-393">None</span><span class="sxs-lookup"><span data-stu-id="8e3a3-393">None</span></span>                 |
| <span data-ttu-id="8e3a3-394">1</span><span class="sxs-lookup"><span data-stu-id="8e3a3-394">1</span></span>   | <span data-ttu-id="8e3a3-395">重ねて表示</span><span class="sxs-lookup"><span data-stu-id="8e3a3-395">Cascade</span></span>              |
| <span data-ttu-id="8e3a3-396">2</span><span class="sxs-lookup"><span data-stu-id="8e3a3-396">2</span></span>   | <span data-ttu-id="8e3a3-397">制限</span><span class="sxs-lookup"><span data-stu-id="8e3a3-397">Restricted</span></span>           |
| <span data-ttu-id="8e3a3-398">3</span><span class="sxs-lookup"><span data-stu-id="8e3a3-398">3</span></span>   | <span data-ttu-id="8e3a3-399">重ねて表示 + 制限</span><span class="sxs-lookup"><span data-stu-id="8e3a3-399">Cascade + Restricted</span></span> |

### <a name="examples---deleteactiontype"></a><span data-ttu-id="8e3a3-400">例 - deleteActionType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-400">Examples - deleteActionType</span></span>

<span data-ttu-id="8e3a3-401">次の例は、テーブルの削除アクションのタイプの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-401">The following example shows the retrieval of the type of delete actions for a table.</span></span>

```xpp
DictTable dt, dt2; 
str       strDelActType; 
int       i, nDelActType; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.deleteActionCnt(); i++) 
    { 
        dt2 = new DictTable(dt.deleteActionTableId(i)); 
        if (dt2) 
        { 
            nDelActType = dt.deleteActionType(i); 
            switch (nDelActType) 
            { 
               case 0: 
                strDelActType = "None"; 
                break; 
               case 1: 
                strDelActType = "Cascade"; 
                break; 
               case 2: 
                strDelActType = "Restricted"; 
                break; 
               case 3: 
                strDelActType = "Cascade + Restricted"; 
                break; 
            } 
            print strfmt("Delete action table: %1 Type: %2", 
                         dt2.name(), 
                         strDelActType); 
        } 
    } 
}
```

## <a name="method-developerdocumentation"></a><span data-ttu-id="8e3a3-402">メソッド developerDocumentation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-402">Method developerDocumentation</span></span>

```xpp
public str developerDocumentation()
```

### <a name="return-value---developerdocumentation"></a><span data-ttu-id="8e3a3-403">戻り値 - developerDocumentation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-403">Return Value - developerDocumentation</span></span>

## <a name="method-developerdocumentationlabelid"></a><span data-ttu-id="8e3a3-404">メソッド developerDocumentationLabelId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-404">Method developerDocumentationLabelId</span></span>

```xpp
public str developerDocumentationLabelId()
```

### <a name="return-value---developerdocumentationlabelid"></a><span data-ttu-id="8e3a3-405">戻り値 - developerDocumentationLabelId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-405">Return Value - developerDocumentationLabelId</span></span>

## <a name="method-enabled"></a><span data-ttu-id="8e3a3-406">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="8e3a3-406">Method enabled</span></span>

<span data-ttu-id="8e3a3-407">テーブルが有効かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-407">Returns a value that indicates whether the table is enabled.</span></span>

```xpp
public boolean enabled()
```

### <a name="return-value---enabled"></a><span data-ttu-id="8e3a3-408">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="8e3a3-408">Return Value - enabled</span></span>

<span data-ttu-id="8e3a3-409">テーブルが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-409">true if the table is enabled; otherwise, false.</span></span>

### <a name="examples---enabled"></a><span data-ttu-id="8e3a3-410">例 - enabled</span><span class="sxs-lookup"><span data-stu-id="8e3a3-410">Examples - enabled</span></span>

<span data-ttu-id="8e3a3-411">次の例は、テーブルが有効化されているかどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-411">The following example shows the retrieval of the value that indicates whether the table is enabled.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table is %1.", dt.enabled() ? "enabled" : "not enabled")); 
}
```

## <a name="method-enforcerelationrules"></a><span data-ttu-id="8e3a3-412">メソッド enforceRelationRules</span><span class="sxs-lookup"><span data-stu-id="8e3a3-412">Method enforceRelationRules</span></span>

```xpp
public boolean enforceRelationRules()
```

### <a name="return-value---enforcerelationrules"></a><span data-ttu-id="8e3a3-413">戻り値 - enforceRelationRules</span><span class="sxs-lookup"><span data-stu-id="8e3a3-413">Return Value - enforceRelationRules</span></span>

## <a name="method-entityrelationshiptype"></a><span data-ttu-id="8e3a3-414">メソッド entityRelationshipType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-414">Method entityRelationshipType</span></span>

```xpp
public EntityRelationshipType entityRelationshipType()
```

### <a name="return-value---entityrelationshiptype"></a><span data-ttu-id="8e3a3-415">戻り値 - entityRelationshipType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-415">Return Value - entityRelationshipType</span></span>

## <a name="method-extendedby"></a><span data-ttu-id="8e3a3-416">メソッド extendedBy</span><span class="sxs-lookup"><span data-stu-id="8e3a3-416">Method extendedBy</span></span>

```xpp
public List extendedBy([boolean allLevels])
```

### <a name="parameters---extendedby"></a><span data-ttu-id="8e3a3-417">パラメーター - extendedBy</span><span class="sxs-lookup"><span data-stu-id="8e3a3-417">Parameters - extendedBy</span></span>

<span data-ttu-id="8e3a3-418">allLevels</span><span class="sxs-lookup"><span data-stu-id="8e3a3-418">allLevels</span></span>  

### <a name="return-value---extendedby"></a><span data-ttu-id="8e3a3-419">戻り値 - extendedBy</span><span class="sxs-lookup"><span data-stu-id="8e3a3-419">Return Value - extendedBy</span></span>

## <a name="method-extends"></a><span data-ttu-id="8e3a3-420">メソッド extends</span><span class="sxs-lookup"><span data-stu-id="8e3a3-420">Method extends</span></span>

<span data-ttu-id="8e3a3-421">基本テーブルのテーブル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-421">Returns the table ID of a base table.</span></span>

```xpp
public TableId extends()
```

### <a name="return-value---extends"></a><span data-ttu-id="8e3a3-422">戻り値 - extends</span><span class="sxs-lookup"><span data-stu-id="8e3a3-422">Return Value - extends</span></span>

<span data-ttu-id="8e3a3-423">ベース テーブルのテーブル ID</span><span class="sxs-lookup"><span data-stu-id="8e3a3-423">The table ID of the base table.</span></span>

## <a name="method-fieldcnt"></a><span data-ttu-id="8e3a3-424">メソッド fieldCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-424">Method fieldCnt</span></span>

<span data-ttu-id="8e3a3-425">テーブルのフィールドの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-425">Returns the number of fields for a table.</span></span>

```xpp
public int fieldCnt([TableScope tableScope])
```

### <a name="parameters---fieldcnt"></a><span data-ttu-id="8e3a3-426">パラメーター - fieldCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-426">Parameters - fieldCnt</span></span>

<span data-ttu-id="8e3a3-427">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-427">tableScope</span></span>  

### <a name="return-value---fieldcnt"></a><span data-ttu-id="8e3a3-428">戻り値 - fieldCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-428">Return Value - fieldCnt</span></span>

<span data-ttu-id="8e3a3-429">テーブルのフィールドの数。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-429">The number of fields for the table.</span></span>

### <a name="examples---fieldcnt"></a><span data-ttu-id="8e3a3-430">例 - fieldCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-430">Examples - fieldCnt</span></span>

<span data-ttu-id="8e3a3-431">次の例は、テーブルのフィールド数の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-431">The following example shows the retrieval of the number of fields for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 fields.", dt.fieldCnt())); 
}
```

## <a name="method-fieldcnt2id"></a><span data-ttu-id="8e3a3-432">メソッド fieldCnt2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-432">Method fieldCnt2Id</span></span>

<span data-ttu-id="8e3a3-433">インデックスで指定されるフィールドのフィールド ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-433">Returns the field ID of the field that is specified by an index.</span></span>

```xpp
public FieldId fieldCnt2Id(int cnt, [TableScope tableScope])
```

### <a name="parameters---fieldcnt2id"></a><span data-ttu-id="8e3a3-434">パラメーター - fieldCnt2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-434">Parameters - fieldCnt2Id</span></span>

<span data-ttu-id="8e3a3-435">cnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-435">cnt</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-436">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-436">tableScope</span></span>  

### <a name="return-value---fieldcnt2id"></a><span data-ttu-id="8e3a3-437">戻り値 - fieldCnt2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-437">Return Value - fieldCnt2Id</span></span>

<span data-ttu-id="8e3a3-438">インデックスで指定されたフィールドのフィールド ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-438">The field ID of the field that is specified by an index.</span></span>

### <a name="examples---fieldcnt2id"></a><span data-ttu-id="8e3a3-439">例 - fieldCnt2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-439">Examples - fieldCnt2Id</span></span>

<span data-ttu-id="8e3a3-440">次の例は、インデックスによるテーブルのフィールドの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-440">The following example shows the retrieval of the fields of a table by index.</span></span>

```xpp
DictTable dt; 
int       i, fId, tId; 
DictField df; 
str       strFieldName; 
tId = tablenum(CustTable); 
dt = new DictTable(tId); 
if (dt) 
{ 
    for (i=1; i <= dt.fieldCnt(); i++) 
    { 
        fId = dt.fieldCnt2Id(i); 
        df = new DictField(tId, fId); 
        strFieldName = (df ? df.name() : ""); 
        print(strfmt("%1) %2 %3", i, fId, strFieldName)); 
    } 
}
```

## <a name="method-fieldgroup"></a><span data-ttu-id="8e3a3-441">メソッド fieldGroup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-441">Method fieldGroup</span></span>

<span data-ttu-id="8e3a3-442">インデックスで指定されるフィールド グループの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-442">Returns the name of a field group that is specified by index.</span></span>

```xpp
public str fieldGroup(int FieldGroupNumber, [TableScope tableScope])
```

### <a name="parameters---fieldgroup"></a><span data-ttu-id="8e3a3-443">パラメーター - fieldGroup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-443">Parameters - fieldGroup</span></span>

<span data-ttu-id="8e3a3-444">FieldGroupNumber</span><span class="sxs-lookup"><span data-stu-id="8e3a3-444">FieldGroupNumber</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-445">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-445">tableScope</span></span>  

### <a name="return-value---fieldgroup"></a><span data-ttu-id="8e3a3-446">戻り値 - fieldGroup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-446">Return Value - fieldGroup</span></span>

<span data-ttu-id="8e3a3-447">FieldGroupNumber パラメーターで指定されるフィールド グループの名前。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-447">The name of the field group that is specified by the FieldGroupNumber parameter.</span></span>

### <a name="examples---fieldgroup"></a><span data-ttu-id="8e3a3-448">例 - fieldGroup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-448">Examples - fieldGroup</span></span>

<span data-ttu-id="8e3a3-449">次の例は、テーブルのフィールド グループの名前の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-449">The following example shows the retrieval of the names of the field groups for a table.</span></span>

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i =1; i <= dt.fieldGroupCnt(); i++) 
    { 
        print (dt.fieldGroup(i)); 
    } 
}
```

## <a name="method-fieldgroupcnt"></a><span data-ttu-id="8e3a3-450">メソッド fieldGroupCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-450">Method fieldGroupCnt</span></span>

<span data-ttu-id="8e3a3-451">テーブルのフィールド グループの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-451">Returns the number of field groups for the table.</span></span>

```xpp
public int fieldGroupCnt([TableScope tableScope])
```

### <a name="parameters---fieldgroupcnt"></a><span data-ttu-id="8e3a3-452">パラメーター - fieldGroupCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-452">Parameters - fieldGroupCnt</span></span>

<span data-ttu-id="8e3a3-453">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-453">tableScope</span></span>  

### <a name="return-value---fieldgroupcnt"></a><span data-ttu-id="8e3a3-454">戻り値 - fieldGroupCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-454">Return Value - fieldGroupCnt</span></span>

<span data-ttu-id="8e3a3-455">テーブルのフィールド グループの数。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-455">The number of field groups for the table.</span></span>

### <a name="examples---fieldgroupcnt"></a><span data-ttu-id="8e3a3-456">例 - fieldGroupCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-456">Examples - fieldGroupCnt</span></span>

<span data-ttu-id="8e3a3-457">次の例は、テーブルのフィールド グループ数の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-457">The following example shows the retrieval of the number of field groups for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 field groups.", dt.fieldGroupCnt())); 
}
```

## <a name="method-fieldname"></a><span data-ttu-id="8e3a3-458">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-458">Method fieldName</span></span>

<span data-ttu-id="8e3a3-459">フィールド ID で指定されるフィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-459">Returns the name of the field that is specified by field ID.</span></span>

```xpp
public str fieldName(FieldId fieldId, [DbBackend db], [int arrayindex], [FieldNameGenerationMode generationMode], [str tableAlias])
```

### <a name="parameters---fieldname"></a><span data-ttu-id="8e3a3-460">パラメーター - fieldName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-460">Parameters - fieldName</span></span>

<span data-ttu-id="8e3a3-461">fieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-461">fieldId</span></span>  
<span data-ttu-id="8e3a3-462">テーブルのエイリアスの名前 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-462">The alias name for the table; optional.</span></span>

<!-- -->

<span data-ttu-id="8e3a3-463">db</span><span class="sxs-lookup"><span data-stu-id="8e3a3-463">db</span></span>  
<span data-ttu-id="8e3a3-464">テーブルのエイリアスの名前 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-464">The alias name for the table; optional.</span></span>

<!-- -->

<span data-ttu-id="8e3a3-465">arrayindex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-465">arrayindex</span></span>  
<span data-ttu-id="8e3a3-466">テーブルのエイリアスの名前 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-466">The alias name for the table; optional.</span></span>

<!-- -->

<span data-ttu-id="8e3a3-467">generationMode</span><span class="sxs-lookup"><span data-stu-id="8e3a3-467">generationMode</span></span>  
<span data-ttu-id="8e3a3-468">テーブルのエイリアスの名前 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-468">The alias name for the table; optional.</span></span>

<!-- -->

<span data-ttu-id="8e3a3-469">tableAlias</span><span class="sxs-lookup"><span data-stu-id="8e3a3-469">tableAlias</span></span>  
<span data-ttu-id="8e3a3-470">テーブルのエイリアスの名前 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-470">The alias name for the table; optional.</span></span>

### <a name="return-value---fieldname"></a><span data-ttu-id="8e3a3-471">戻り値 - fieldName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-471">Return Value - fieldName</span></span>

<span data-ttu-id="8e3a3-472">フィールド ID で指定されるフィールド グループの名前。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-472">The name of the field that is specified by its field ID.</span></span>

### <a name="remarks---fieldname"></a><span data-ttu-id="8e3a3-473">備考 - fieldName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-473">Remarks - fieldName</span></span>

<span data-ttu-id="8e3a3-474">db が指定されていない場合は、DbBackend::Native オブジェクトが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-474">If db is not specified, the DbBackend::Native object is used.</span></span>

### <a name="examples---fieldname"></a><span data-ttu-id="8e3a3-475">例 - fieldName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-475">Examples - fieldName</span></span>

<span data-ttu-id="8e3a3-476">次の例は、フィールド ID で指定されたテーブルのフィールド名の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-476">The following example shows the retrieval of field names of a table as specified by the field IDs.</span></span>

```xpp
DictTable dt; 
int       i, tId, fId; 
tId = tablenum(CustTable); 
dt = new DictTable(tId); 
if (dt) 
{ 
    for (i=1; i <= dt.fieldCnt(); i++) 
    { 
        fId = dt.fieldCnt2Id(i); 
        print(strfmt("%1) %2 %3", i, fId, dt.fieldName(fId))); 
    } 
}
```

## <a name="method-fieldname2id"></a><span data-ttu-id="8e3a3-477">メソッド fieldName2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-477">Method fieldName2Id</span></span>

<span data-ttu-id="8e3a3-478">名前で指定されるフィールドのフィールド ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-478">Returns the field ID of a field that is specified by name.</span></span>

```xpp
public FieldId fieldName2Id(str name)
```

### <a name="parameters---fieldname2id"></a><span data-ttu-id="8e3a3-479">パラメーター - fieldName2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-479">Parameters - fieldName2Id</span></span>

<span data-ttu-id="8e3a3-480">名前</span><span class="sxs-lookup"><span data-stu-id="8e3a3-480">name</span></span>  
<span data-ttu-id="8e3a3-481">フィールド ID が取得されているフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-481">The name of the field for which the field ID is being retrieved.</span></span>

### <a name="return-value---fieldname2id"></a><span data-ttu-id="8e3a3-482">戻り値 - fieldName2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-482">Return Value - fieldName2Id</span></span>

<span data-ttu-id="8e3a3-483">name パラメーターで指定されたフィールドのフィールド ID。name がテーブルの有効なフィールド名を表していない場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-483">The field ID of the field that is specified by the name parameter; 0 (zero) if name does not represent a valid field name for the table.</span></span>

### <a name="examples---fieldname2id"></a><span data-ttu-id="8e3a3-484">例 - fieldName2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-484">Examples - fieldName2Id</span></span>

<span data-ttu-id="8e3a3-485">次の例は、フィールド名によるフィールド ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-485">The following example shows the retrieval of a field ID by its field name.</span></span>

```xpp
DictTable dt; 
fieldId   fId; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    fId = dt.fieldName2Id("Pager"); 
    // Use the field ID as needed. 
    // This example merely prints out the field ID. 
    print (strfmt("fId: %1", fId)); 
}
```

## <a name="method-fieldnext"></a><span data-ttu-id="8e3a3-486">メソッド fieldNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-486">Method fieldNext</span></span>

<span data-ttu-id="8e3a3-487">テーブルのフィールド反復処理中に、次のフィールド ID の値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-487">Returns the value of the next field ID during a field iteration of the table.</span></span>

```xpp
public FieldId fieldNext(FieldId fieldId, [TableScope tableScope])
```

### <a name="parameters---fieldnext"></a><span data-ttu-id="8e3a3-488">パラメーター - fieldNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-488">Parameters - fieldNext</span></span>

<span data-ttu-id="8e3a3-489">fieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-489">fieldId</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-490">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-490">tableScope</span></span>  

### <a name="return-value---fieldnext"></a><span data-ttu-id="8e3a3-491">戻り値 - fieldNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-491">Return Value - fieldNext</span></span>

<span data-ttu-id="8e3a3-492">テーブルのフィールド反復における次のフィールドの ID。反復処理するフィールドがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-492">The ID of the next field in the field iteration for the table; 0 (zero) if there are no more fields to iterate.</span></span>

### <a name="remarks---fieldnext"></a><span data-ttu-id="8e3a3-493">備考 - fieldNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-493">Remarks - fieldNext</span></span>

<span data-ttu-id="8e3a3-494">フィールドの反復を開始するには、fieldId パラメーターの値を 0 (ゼロ) に評価し、その反復の後続の呼び出しには戻り値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-494">The value of the fieldId parameter should evaluate to 0 (zero) to start the field iteration, and the return value should be used for subsequent calls to the iteration.</span></span>

### <a name="examples---fieldnext"></a><span data-ttu-id="8e3a3-495">例 - fieldNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-495">Examples - fieldNext</span></span>

<span data-ttu-id="8e3a3-496">次の例では、テーブルのフィールドを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-496">The following example iterates through the fields of a table.</span></span>

```xpp
DictTable   dt; 
DictField   df; 
int         counter; 
counter = 0; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    counter = dt.fieldNext(counter); 
    while (counter) 
    { 
        df = dt.fieldObject(counter); 
        if (df) 
        { 
            print strfmt("ID: %1 Name: %2", 
                         df.id(), 
                         df.name() ); 
        } 
        counter = dt.fieldNext(counter); 
    } 
}
```

## <a name="method-fieldobject"></a><span data-ttu-id="8e3a3-497">メソッド fieldObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-497">Method fieldObject</span></span>

<span data-ttu-id="8e3a3-498">フィールド ID で指定されているフィールドの DictField クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-498">Creates an instance of the DictField class for the field that is specified by field ID.</span></span>

```xpp
public DictField fieldObject(FieldId fieldId)
```

### <a name="parameters---fieldobject"></a><span data-ttu-id="8e3a3-499">パラメーター - fieldObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-499">Parameters - fieldObject</span></span>

<span data-ttu-id="8e3a3-500">fieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-500">fieldId</span></span>  
<span data-ttu-id="8e3a3-501">作成するフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-501">The ID of the field to create.</span></span>

### <a name="return-value---fieldobject"></a><span data-ttu-id="8e3a3-502">戻り値 - fieldObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-502">Return Value - fieldObject</span></span>

<span data-ttu-id="8e3a3-503">fieldId パラメーターで指定されたフィールドの DictField オブジェクト。オブジェクトを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-503">A DictField object for the field that is specified by the fieldId parameter; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if the object could not be created.</span></span>

### <a name="examples---fieldobject"></a><span data-ttu-id="8e3a3-504">例 - fieldObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-504">Examples - fieldObject</span></span>

<span data-ttu-id="8e3a3-505">次の例は、テーブル内のフィールドの DictField オブジェクトを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-505">The following example shows how to create a DictField object for the fields in a table.</span></span>

```xpp
DictTable dt; 
DictField df; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.fieldCnt(); i++) 
    { 
      df = dt.fieldObject(dt.fieldCnt2Id(i)); 
      if (df) 
      { 
          print df.name(); 
      } 
    } 
}
```

## <a name="method-fieldorigin2id"></a><span data-ttu-id="8e3a3-506">メソッド fieldOrigin2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-506">Method fieldOrigin2Id</span></span>

```xpp
public IndexId fieldOrigin2Id(Guid fieldOrigin, [TableScope tableScope])
```

### <a name="parameters---fieldorigin2id"></a><span data-ttu-id="8e3a3-507">パラメーター - fieldOrigin2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-507">Parameters - fieldOrigin2Id</span></span>

<span data-ttu-id="8e3a3-508">fieldOrigin</span><span class="sxs-lookup"><span data-stu-id="8e3a3-508">fieldOrigin</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-509">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-509">tableScope</span></span>  

### <a name="return-value---fieldorigin2id"></a><span data-ttu-id="8e3a3-510">戻り値 - fieldOrigin2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-510">Return Value - fieldOrigin2Id</span></span>

## <a name="method-fieldsqldefault"></a><span data-ttu-id="8e3a3-511">メソッド fieldSqlDefault</span><span class="sxs-lookup"><span data-stu-id="8e3a3-511">Method fieldSqlDefault</span></span>

<span data-ttu-id="8e3a3-512">フィールド ID で指定されているフィールドの SQL 既定値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-512">Returns the SQL default value for the field that is specified by field ID.</span></span>

```xpp
public str fieldSqlDefault(FieldId fieldId)
```

### <a name="parameters---fieldsqldefault"></a><span data-ttu-id="8e3a3-513">パラメーター - fieldSqlDefault</span><span class="sxs-lookup"><span data-stu-id="8e3a3-513">Parameters - fieldSqlDefault</span></span>

<span data-ttu-id="8e3a3-514">fieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-514">fieldId</span></span>  
<span data-ttu-id="8e3a3-515">SQL の既定のデータが取得されるフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-515">The ID of the field for which the SQL default data is being retrieved.</span></span>

### <a name="return-value---fieldsqldefault"></a><span data-ttu-id="8e3a3-516">戻り値 - fieldSqlDefault</span><span class="sxs-lookup"><span data-stu-id="8e3a3-516">Return Value - fieldSqlDefault</span></span>

<span data-ttu-id="8e3a3-517">fieldId パラメーターで指定されたフィールドの SQL 既定値を表す文字列、フィールドに SQL のデフォルト値がない場合、またはテーブルが SQL テーブルではない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-517">A string that represents the SQL default value for the field that is specified by the fieldId parameter; an empty string if the field has no SQL default value or the table is not an SQL table.</span></span>

## <a name="method-formref"></a><span data-ttu-id="8e3a3-518">メソッド formRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-518">Method formRef</span></span>

<span data-ttu-id="8e3a3-519">テーブルの既定のフォームの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-519">Returns the name of the default form for the table.</span></span>

```xpp
public str formRef([boolean searchBaseTables])
```

### <a name="parameters---formref"></a><span data-ttu-id="8e3a3-520">パラメーター - formRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-520">Parameters - formRef</span></span>

<span data-ttu-id="8e3a3-521">searchBaseTables</span><span class="sxs-lookup"><span data-stu-id="8e3a3-521">searchBaseTables</span></span>  

### <a name="return-value---formref"></a><span data-ttu-id="8e3a3-522">戻り値 - formRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-522">Return Value - formRef</span></span>

<span data-ttu-id="8e3a3-523">テーブルの既定のフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-523">The name of the default form for the table.</span></span>

### <a name="remarks---formref"></a><span data-ttu-id="8e3a3-524">備考 - formRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-524">Remarks - formRef</span></span>

<span data-ttu-id="8e3a3-525">AOT に、テーブルの FormRef プロパティの値が表示されない場合、テーブルの既定のフォームの名前は、テーブルの名前と同じであると見なされます。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-525">If the AOT shows no value for the FormRef property of a table, the name of the default form for the table is considered to be the same as the name of the table.</span></span> <span data-ttu-id="8e3a3-526">この場合、このメソッドは空の文字列を返しません。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-526">In this case, this method does not return an empty string.</span></span>

### <a name="examples---formref"></a><span data-ttu-id="8e3a3-527">例 - formRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-527">Examples - formRef</span></span>

<span data-ttu-id="8e3a3-528">次の例は、テーブルの既定のフォームの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-528">The following example shows the retrieval of the default form for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print strfmt("Default form: %1", dt.formRef()); 
}
```

## <a name="method-getcountryregioncodes"></a><span data-ttu-id="8e3a3-529">メソッド getCountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="8e3a3-529">Method getCountryRegionCodes</span></span>

```xpp
public container getCountryRegionCodes()
```

### <a name="return-value---getcountryregioncodes"></a><span data-ttu-id="8e3a3-530">戻り値 - getCountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="8e3a3-530">Return Value - getCountryRegionCodes</span></span>

## <a name="method-getcountryregioncontextfield"></a><span data-ttu-id="8e3a3-531">メソッド getCountryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="8e3a3-531">Method getCountryRegionContextField</span></span>

```xpp
public FieldId getCountryRegionContextField()
```

### <a name="return-value---getcountryregioncontextfield"></a><span data-ttu-id="8e3a3-532">戻り値 - getCountryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="8e3a3-532">Return Value - getCountryRegionContextField</span></span>

## <a name="method-getvalidtimestatevalidfromfieldid"></a><span data-ttu-id="8e3a3-533">メソッド getValidTimeStateValidFromFieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-533">Method getValidTimeStateValidFromFieldId</span></span>

```xpp
public FieldId getValidTimeStateValidFromFieldId()
```

### <a name="return-value---getvalidtimestatevalidfromfieldid"></a><span data-ttu-id="8e3a3-534">戻り値 - getValidTimeStateValidFromFieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-534">Return Value - getValidTimeStateValidFromFieldId</span></span>

## <a name="method-getvalidtimestatevalidtofieldid"></a><span data-ttu-id="8e3a3-535">メソッド getValidTimeStateValidToFieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-535">Method getValidTimeStateValidToFieldId</span></span>

```xpp
public FieldId getValidTimeStateValidToFieldId()
```

### <a name="return-value---getvalidtimestatevalidtofieldid"></a><span data-ttu-id="8e3a3-536">戻り値 - getValidTimeStateValidToFieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-536">Return Value - getValidTimeStateValidToFieldId</span></span>

## <a name="method-hasrecididx"></a><span data-ttu-id="8e3a3-537">メソッド hasRecidIdx</span><span class="sxs-lookup"><span data-stu-id="8e3a3-537">Method hasRecidIdx</span></span>

<span data-ttu-id="8e3a3-538">テーブルのレコード ID インデックスが有効かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-538">Returns a value that indicates whether a record ID index for the table is in effect.</span></span>

```xpp
public boolean hasRecidIdx()
```

### <a name="return-value---hasrecididx"></a><span data-ttu-id="8e3a3-539">戻り値 - hasRecidIdx</span><span class="sxs-lookup"><span data-stu-id="8e3a3-539">Return Value - hasRecidIdx</span></span>

<span data-ttu-id="8e3a3-540">レコード ID インデックスがテーブルで有効な場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-540">true if a record ID index is in effect for the table; otherwise, false.</span></span>

### <a name="remarks---hasrecididx"></a><span data-ttu-id="8e3a3-541">備考 - hasRecidIdx</span><span class="sxs-lookup"><span data-stu-id="8e3a3-541">Remarks - hasRecidIdx</span></span>

<span data-ttu-id="8e3a3-542">戻り値は、テーブルの CreateRecIdIndex プロパティが Yes に設定されているかどうかに対応します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-542">The return value corresponds to whether the CreateRecIdIndex property of the table is set to Yes.</span></span>

### <a name="examples---hasrecididx"></a><span data-ttu-id="8e3a3-543">例 - hasRecidIdx</span><span class="sxs-lookup"><span data-stu-id="8e3a3-543">Examples - hasRecidIdx</span></span>

<span data-ttu-id="8e3a3-544">次の例は、テーブルのレコード ID インデックスが有効かどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-544">The following example shows the retrieval of a value that indicates whether the record ID index of the table is in effect.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("A record ID index for the table %1 in effect.", 
           dt.hasRecidIdx() ? "is" : "is not") ); 
}
```

## <a name="method-hassurrogatekey"></a><span data-ttu-id="8e3a3-545">メソッド hasSurrogateKey</span><span class="sxs-lookup"><span data-stu-id="8e3a3-545">Method hasSurrogateKey</span></span>

```xpp
public boolean hasSurrogateKey()
```

### <a name="return-value---hassurrogatekey"></a><span data-ttu-id="8e3a3-546">戻り値 - hasSurrogateKey</span><span class="sxs-lookup"><span data-stu-id="8e3a3-546">Return Value - hasSurrogateKey</span></span>

## <a name="method-id"></a><span data-ttu-id="8e3a3-547">メソッド id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-547">Method id</span></span>

<span data-ttu-id="8e3a3-548">テーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-548">Returns the ID of the table.</span></span>

```xpp
public TableId id()
```

### <a name="return-value---id"></a><span data-ttu-id="8e3a3-549">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-549">Return Value - id</span></span>

<span data-ttu-id="8e3a3-550">テーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-550">The ID of the table.</span></span>

### <a name="examples---id"></a><span data-ttu-id="8e3a3-551">例 - id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-551">Examples - id</span></span>

<span data-ttu-id="8e3a3-552">次の例は、テーブルの ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-552">The following example shows the retrieval of the ID of a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table ID is: %1", dt.id())); 
}
```

## <a name="method-indexcnt"></a><span data-ttu-id="8e3a3-553">メソッド indexCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-553">Method indexCnt</span></span>

<span data-ttu-id="8e3a3-554">テーブルのインデックスの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-554">Returns the number of indexes for the table.</span></span>

```xpp
public int indexCnt()
```

### <a name="return-value---indexcnt"></a><span data-ttu-id="8e3a3-555">戻り値 - indexCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-555">Return Value - indexCnt</span></span>

<span data-ttu-id="8e3a3-556">テーブルのインデックスの数。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-556">The number of indexes for the table.</span></span>

### <a name="examples---indexcnt"></a><span data-ttu-id="8e3a3-557">例 - indexCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-557">Examples - indexCnt</span></span>

<span data-ttu-id="8e3a3-558">次の例は、テーブルのインデックス数の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-558">The following example shows the retrieval of the number of indexes for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 indexes.", dt.indexCnt())); 
}
```

## <a name="method-indexcnt2id"></a><span data-ttu-id="8e3a3-559">メソッド indexCnt2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-559">Method indexCnt2Id</span></span>

```xpp
public IndexId indexCnt2Id(int cnt)
```

### <a name="parameters---indexcnt2id"></a><span data-ttu-id="8e3a3-560">パラメーター - indexCnt2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-560">Parameters - indexCnt2Id</span></span>

<span data-ttu-id="8e3a3-561">cnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-561">cnt</span></span>  

### <a name="return-value---indexcnt2id"></a><span data-ttu-id="8e3a3-562">戻り値 - indexCnt2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-562">Return Value - indexCnt2Id</span></span>

## <a name="method-indexname"></a><span data-ttu-id="8e3a3-563">メソッド indexName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-563">Method indexName</span></span>

<span data-ttu-id="8e3a3-564">indexId パラメーターで指定された形式のインデックスの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-564">Returns the name of an index that is specified by the indexId parameter.</span></span>

```xpp
public str indexName(IndexId indexId, [DbBackend db])
```

### <a name="parameters---indexname"></a><span data-ttu-id="8e3a3-565">パラメーター - indexName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-565">Parameters - indexName</span></span>

<span data-ttu-id="8e3a3-566">indexId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-566">indexId</span></span>  
<span data-ttu-id="8e3a3-567">データベース バックエンドのタイプを指定する DbBackend 値; オプション。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-567">A DbBackend value that specifies the type of database back end; optional.</span></span>

<!-- -->

<span data-ttu-id="8e3a3-568">db</span><span class="sxs-lookup"><span data-stu-id="8e3a3-568">db</span></span>  
<span data-ttu-id="8e3a3-569">データベース バックエンドのタイプを指定する DbBackend 値; オプション。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-569">A DbBackend value that specifies the type of database back end; optional.</span></span>

### <a name="return-value---indexname"></a><span data-ttu-id="8e3a3-570">戻り値 - indexName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-570">Return Value - indexName</span></span>

<span data-ttu-id="8e3a3-571">indexId パラメーターで指定された形式のインデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-571">The name of the index that is specified by the indexId parameter.</span></span>

### <a name="examples---indexname"></a><span data-ttu-id="8e3a3-572">例 - indexName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-572">Examples - indexName</span></span>

<span data-ttu-id="8e3a3-573">次の例は、テーブルのインデックスの名前の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-573">The following example shows the retrieval of the names of the indexes for a table.</span></span>

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.indexCnt(); i++) 
    { 
        print (dt.indexName(i)); 
    } 
}
```

## <a name="method-indexname2id"></a><span data-ttu-id="8e3a3-574">メソッド indexName2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-574">Method indexName2Id</span></span>

<span data-ttu-id="8e3a3-575">名前で指定されているインデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-575">Returns the ID of an index that is specified by name.</span></span>

```xpp
public IndexId indexName2Id(str name)
```

### <a name="parameters---indexname2id"></a><span data-ttu-id="8e3a3-576">パラメーター - indexName2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-576">Parameters - indexName2Id</span></span>

<span data-ttu-id="8e3a3-577">名前</span><span class="sxs-lookup"><span data-stu-id="8e3a3-577">name</span></span>  
<span data-ttu-id="8e3a3-578">インデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-578">The name of the index.</span></span>

### <a name="return-value---indexname2id"></a><span data-ttu-id="8e3a3-579">戻り値 - indexName2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-579">Return Value - indexName2Id</span></span>

<span data-ttu-id="8e3a3-580">名前パラメーターで指定されているインデックスの ID。名前値と同じ名前が付けられたインデックスがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-580">The ID of the index that is specified by the name parameter; 0 (zero) if there is no index that has a name that equals the name value.</span></span>

### <a name="examples---indexname2id"></a><span data-ttu-id="8e3a3-581">例 - indexName2Id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-581">Examples - indexName2Id</span></span>

<span data-ttu-id="8e3a3-582">次の例は、名前で指定されたインデックスの ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-582">The following example shows the retrieval of the ID of an index that is specified by name.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print(strfmt("Index ID: %1", dt.indexName2Id("TypeIdx"))); 
}
```

## <a name="method-indexnext"></a><span data-ttu-id="8e3a3-583">メソッド indexNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-583">Method indexNext</span></span>

<span data-ttu-id="8e3a3-584">テーブルのインデックス反復処理中に、次のインデックス ID の値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-584">Returns the value of the next index ID during an index iteration of the table.</span></span>

```xpp
public IndexId indexNext(IndexId id)
```

### <a name="parameters---indexnext"></a><span data-ttu-id="8e3a3-585">パラメーター - indexNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-585">Parameters - indexNext</span></span>

<span data-ttu-id="8e3a3-586">id</span><span class="sxs-lookup"><span data-stu-id="8e3a3-586">id</span></span>  
<span data-ttu-id="8e3a3-587">次のインデックス ID が照会されるインデックスの ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-587">The ID of the index for which the next index ID is being queried.</span></span>

### <a name="return-value---indexnext"></a><span data-ttu-id="8e3a3-588">戻り値 - indexNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-588">Return Value - indexNext</span></span>

<span data-ttu-id="8e3a3-589">テーブルのインデックス反復における次のインデックスの ID。反復処理するインデックスがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-589">The ID of the next index in the index iteration for the table; 0 (zero) if there are no more indexes to iterate.</span></span>

### <a name="remarks---indexnext"></a><span data-ttu-id="8e3a3-590">備考 - indexNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-590">Remarks - indexNext</span></span>

<span data-ttu-id="8e3a3-591">インデックスの反復を開始するには、id パラメーターの値を 0 (ゼロ) に評価し、その反復の後続の呼び出しには戻り値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-591">The value of the id parameter should evaluate to 0 (zero) to start the index iteration, and the return value should be used for subsequent calls to the iteration.</span></span>

### <a name="examples---indexnext"></a><span data-ttu-id="8e3a3-592">例 - indexNext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-592">Examples - indexNext</span></span>

<span data-ttu-id="8e3a3-593">次の例では、テーブルのインデックスを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-593">The following example iterates through the indexes of a table.</span></span>

```xpp
DictTable   dt; 
DictIndex   di; 
int         counter; 
counter = 0; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    counter = dt.indexNext(counter); 
    while (counter) 
    { 
        di = dt.indexObject(counter); 
        if (di) 
        { 
            print strfmt("ID: %1 Name: %2", 
                         di.id(), 
                         di.name() ); 
        } 
        counter = dt.indexNext(counter); 
    } 
}
```

## <a name="method-indexobject"></a><span data-ttu-id="8e3a3-594">メソッド indexObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-594">Method indexObject</span></span>

<span data-ttu-id="8e3a3-595">ID で指定されているインデックスの DictTable クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-595">Creates an instance of the DictTable class for the index that is specified by ID.</span></span>

```xpp
public DictIndex indexObject(IndexId indexId)
```

### <a name="parameters---indexobject"></a><span data-ttu-id="8e3a3-596">パラメーター - indexObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-596">Parameters - indexObject</span></span>

<span data-ttu-id="8e3a3-597">indexId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-597">indexId</span></span>  
<span data-ttu-id="8e3a3-598">作成するインデックスの ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-598">The ID of the index to create.</span></span>

### <a name="return-value---indexobject"></a><span data-ttu-id="8e3a3-599">戻り値 - indexObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-599">Return Value - indexObject</span></span>

<span data-ttu-id="8e3a3-600">indexId パラメーターで指定されたインデックスの DictIndex オブジェクト。オブジェクトを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-600">A DictIndex object for the index that is specified by the indexId parameter; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if the object could not be created.</span></span>

### <a name="examples---indexobject"></a><span data-ttu-id="8e3a3-601">例 - indexObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-601">Examples - indexObject</span></span>

<span data-ttu-id="8e3a3-602">次の例は、テーブルの固有インデックスの DictIndex オブジェクトを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-602">The following example shows how to create a DictIndex object for the unique index of a table.</span></span>

```xpp
DictTable dt; 
DictIndex di; 
dt = new DictTable(tablenum(SysUserInfo)); 
if (dt) 
{ 
     di = dt.indexObject(dt.indexUnique()); 
     if (di) 
     { 
        print di.name(); 
     } 
}
```

## <a name="method-indexunique"></a><span data-ttu-id="8e3a3-603">メソッド indexUnique</span><span class="sxs-lookup"><span data-stu-id="8e3a3-603">Method indexUnique</span></span>

<span data-ttu-id="8e3a3-604">テーブルの一意のインデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-604">Returns the ID of the unique index for the table.</span></span>

```xpp
public IndexId indexUnique()
```

### <a name="return-value---indexunique"></a><span data-ttu-id="8e3a3-605">戻り値 - indexUnique</span><span class="sxs-lookup"><span data-stu-id="8e3a3-605">Return Value - indexUnique</span></span>

<span data-ttu-id="8e3a3-606">テーブルの一意のインデックスの ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-606">The ID of the unique index for the table.</span></span>

### <a name="remarks---indexunique"></a><span data-ttu-id="8e3a3-607">備考 - indexUnique</span><span class="sxs-lookup"><span data-stu-id="8e3a3-607">Remarks - indexUnique</span></span>

<span data-ttu-id="8e3a3-608">テーブルに複数の一意のインデックスが存在するとき、戻り値は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-608">When there is more than one unique index on the table, the return value is one of the following:</span></span>

-   <span data-ttu-id="8e3a3-609">RecID 列を持つインデックス。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-609">The index that has the RecID column.</span></span>
-   <span data-ttu-id="8e3a3-610">インデックスにレコードの ID がない場合、最短サイズを持つインデックスは、列のサイズの合計に基づきます。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-610">If no index has a record ID, the index that has the shortest size, based on the total size of columns.</span></span>
-   <span data-ttu-id="8e3a3-611">最短サイズに関して複数のインデックスが一致する場合、インデックスが最初に追加されました。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-611">If multiple indexes match with regard to the shortest size, the index that was added first.</span></span>

### <a name="examples---indexunique"></a><span data-ttu-id="8e3a3-612">例 - indexUnique</span><span class="sxs-lookup"><span data-stu-id="8e3a3-612">Examples - indexUnique</span></span>

<span data-ttu-id="8e3a3-613">次の例は、テーブルの固有インデックスの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-613">The following example shows the retrieval of the unique index for a table.</span></span>

```xpp
DictTable dt; 
DictIndex di; 
dt = new DictTable(tablenum(SysUserInfo)); 
if (dt) 
{ 
     di = dt.indexObject(dt.indexUnique()); 
     if (di) 
     { 
        print di.name(); 
     } 
}
```

## <a name="method-instancerelationtype"></a><span data-ttu-id="8e3a3-614">メソッド instanceRelationType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-614">Method instanceRelationType</span></span>

```xpp
public FieldId instanceRelationType()
```

### <a name="return-value---instancerelationtype"></a><span data-ttu-id="8e3a3-615">戻り値 - instanceRelationType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-615">Return Value - instanceRelationType</span></span>

## <a name="method-isabstract"></a><span data-ttu-id="8e3a3-616">メソッド isAbstract</span><span class="sxs-lookup"><span data-stu-id="8e3a3-616">Method isAbstract</span></span>

<span data-ttu-id="8e3a3-617">このテーブルが抽象かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-617">Indicates whether this table is abstract.</span></span>

```xpp
public boolean isAbstract()
```

### <a name="return-value---isabstract"></a><span data-ttu-id="8e3a3-618">戻り値 - isAbstract</span><span class="sxs-lookup"><span data-stu-id="8e3a3-618">Return Value - isAbstract</span></span>

<span data-ttu-id="8e3a3-619">このテーブルが抽象である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-619">true if this table is abstract; otherwise, false.</span></span>

## <a name="method-isbasedata"></a><span data-ttu-id="8e3a3-620">メソッド isBaseData</span><span class="sxs-lookup"><span data-stu-id="8e3a3-620">Method isBaseData</span></span>

<span data-ttu-id="8e3a3-621">テーブル コンテンツが基本データであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-621">Indicates whether the table content is base data.</span></span>

```xpp
public boolean isBaseData()
```

### <a name="return-value---isbasedata"></a><span data-ttu-id="8e3a3-622">戻り値 - isBaseData</span><span class="sxs-lookup"><span data-stu-id="8e3a3-622">Return Value - isBaseData</span></span>

<span data-ttu-id="8e3a3-623">テーブル コンテンツがベース データであることを AOT 内の TableContents プロパティが示す場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-623">true if the TableContents property in the AOT indicates that the table content is base data; otherwise, false.</span></span>

### <a name="examples---isbasedata"></a><span data-ttu-id="8e3a3-624">例 - isBaseData</span><span class="sxs-lookup"><span data-stu-id="8e3a3-624">Examples - isBaseData</span></span>

<span data-ttu-id="8e3a3-625">次の例は、テーブルの内容が基本データかどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-625">The following example shows the retrieval of a value that indicates whether the table content is base data.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print strfmt("isBaseData: %1", dt.isBaseData()); 
    print strfmt("isDefaultData: %1", dt.isDefaultData()); 
}
```

## <a name="method-isdefaultdata"></a><span data-ttu-id="8e3a3-626">メソッド isDefaultData</span><span class="sxs-lookup"><span data-stu-id="8e3a3-626">Method isDefaultData</span></span>

<span data-ttu-id="8e3a3-627">テーブルが既定のデータを含むかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-627">Indicates whether the table contains default data.</span></span>

```xpp
public boolean isDefaultData()
```

### <a name="return-value---isdefaultdata"></a><span data-ttu-id="8e3a3-628">戻り値 - isDefaultData</span><span class="sxs-lookup"><span data-stu-id="8e3a3-628">Return Value - isDefaultData</span></span>

<span data-ttu-id="8e3a3-629">テーブルに既定のデータが含まれている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-629">true if the table contains default data; otherwise, false.</span></span>

### <a name="examples---isdefaultdata"></a><span data-ttu-id="8e3a3-630">例 - isDefaultData</span><span class="sxs-lookup"><span data-stu-id="8e3a3-630">Examples - isDefaultData</span></span>

<span data-ttu-id="8e3a3-631">次の例は、テーブルに既定のデータが含まれているかどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-631">The following example shows the retrieval of a value that indicates whether the table contains default data.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print strfmt("isDefaultData: %1", dt.isDefaultData()); 
}
```

## <a name="method-isderivedfrom"></a><span data-ttu-id="8e3a3-632">メソッド isDerivedFrom</span><span class="sxs-lookup"><span data-stu-id="8e3a3-632">Method isDerivedFrom</span></span>

<span data-ttu-id="8e3a3-633">1 つのテーブル タイプが別から派生しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-633">Indicates whether one table type derives from another.</span></span>

```xpp
public boolean isDerivedFrom(TableName baseTableName)
```

### <a name="parameters---isderivedfrom"></a><span data-ttu-id="8e3a3-634">パラメータ - isDerivedFrom</span><span class="sxs-lookup"><span data-stu-id="8e3a3-634">Parameters - isDerivedFrom</span></span>

<span data-ttu-id="8e3a3-635">baseTableName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-635">baseTableName</span></span>  

### <a name="return-value---isderivedfrom"></a><span data-ttu-id="8e3a3-636">戻り値 - isDerivedFrom</span><span class="sxs-lookup"><span data-stu-id="8e3a3-636">Return Value - isDerivedFrom</span></span>

<span data-ttu-id="8e3a3-637">このテーブルが baseTableName パラメーターで指定されたテーブルに由来する場合は true。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-637">true if this table is derived from the table that is specified by the baseTableName parameter.</span></span>

## <a name="method-ismap"></a><span data-ttu-id="8e3a3-638">メソッド isMap</span><span class="sxs-lookup"><span data-stu-id="8e3a3-638">Method isMap</span></span>

<span data-ttu-id="8e3a3-639">テーブルがマップであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-639">Indicates whether the table is a map.</span></span>

```xpp
public boolean isMap()
```

### <a name="return-value---ismap"></a><span data-ttu-id="8e3a3-640">戻り値 - isMap</span><span class="sxs-lookup"><span data-stu-id="8e3a3-640">Return Value - isMap</span></span>

<span data-ttu-id="8e3a3-641">テーブルがマップである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-641">true if the table is a map; otherwise, false.</span></span>

### <a name="examples---ismap"></a><span data-ttu-id="8e3a3-642">例 - isMap</span><span class="sxs-lookup"><span data-stu-id="8e3a3-642">Examples - isMap</span></span>

<span data-ttu-id="8e3a3-643">次の例は、テーブルがマップかどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-643">The following example shows the retrieval of a value that indicates whether the table is a map.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(AddressMap)); 
if (dt) 
{ 
    print(strfmt("Map: %1", dt.isMap())); 
}
```

## <a name="method-issql"></a><span data-ttu-id="8e3a3-644">メソッド isSql</span><span class="sxs-lookup"><span data-stu-id="8e3a3-644">Method isSql</span></span>

<span data-ttu-id="8e3a3-645">テーブルが SQL テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-645">Indicates whether the table is an SQL table.</span></span>

```xpp
public boolean isSql()
```

### <a name="return-value---issql"></a><span data-ttu-id="8e3a3-646">戻り値 - isSql</span><span class="sxs-lookup"><span data-stu-id="8e3a3-646">Return Value - isSql</span></span>

<span data-ttu-id="8e3a3-647">テーブルが SQL テーブルである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-647">true if the table is an SQL table; otherwise, false.</span></span>

### <a name="examples---issql"></a><span data-ttu-id="8e3a3-648">例 - isSql</span><span class="sxs-lookup"><span data-stu-id="8e3a3-648">Examples - isSql</span></span>

<span data-ttu-id="8e3a3-649">次の例は、テーブルが SQL テーブルかどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-649">The following example shows the retrieval of a value that indicates whether the table is an SQL table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print(strfmt("SQL table: %1", dt.isSql())); 
}
```

## <a name="method-issystemtable"></a><span data-ttu-id="8e3a3-650">メソッド isSystemTable</span><span class="sxs-lookup"><span data-stu-id="8e3a3-650">Method isSystemTable</span></span>

<span data-ttu-id="8e3a3-651">テーブルがシステム テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-651">Indicates whether the table is a system table.</span></span>

```xpp
public boolean isSystemTable()
```

### <a name="return-value---issystemtable"></a><span data-ttu-id="8e3a3-652">戻り値 - isSystemTable</span><span class="sxs-lookup"><span data-stu-id="8e3a3-652">Return Value - isSystemTable</span></span>

<span data-ttu-id="8e3a3-653">テーブルがシステム テーブルである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-653">true if the table is a system table; otherwise, false.</span></span>

### <a name="examples---issystemtable"></a><span data-ttu-id="8e3a3-654">例 - isSystemTable</span><span class="sxs-lookup"><span data-stu-id="8e3a3-654">Examples - isSystemTable</span></span>

<span data-ttu-id="8e3a3-655">次の例は、テーブルがシステム テーブルかどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-655">The following example shows the retrieval of a value that indicates whether the table is a system table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print(strfmt("System table: %1", dt.isSystemTable())); 
}
```

## <a name="method-istempdb"></a><span data-ttu-id="8e3a3-656">メソッド isTempDb</span><span class="sxs-lookup"><span data-stu-id="8e3a3-656">Method isTempDb</span></span>

```xpp
public boolean isTempDb()
```

### <a name="return-value---istempdb"></a><span data-ttu-id="8e3a3-657">戻り値 - isTempDb</span><span class="sxs-lookup"><span data-stu-id="8e3a3-657">Return Value - isTempDb</span></span>

## <a name="method-istmp"></a><span data-ttu-id="8e3a3-658">メソッド isTmp</span><span class="sxs-lookup"><span data-stu-id="8e3a3-658">Method isTmp</span></span>

<span data-ttu-id="8e3a3-659">テーブルが一時テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-659">Indicates whether the table is a temporary table.</span></span>

```xpp
public boolean isTmp()
```

### <a name="return-value---istmp"></a><span data-ttu-id="8e3a3-660">戻り値 - isTmp</span><span class="sxs-lookup"><span data-stu-id="8e3a3-660">Return Value - isTmp</span></span>

<span data-ttu-id="8e3a3-661">テーブルが一時テーブルである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-661">true if the table is a temporary table; otherwise, false.</span></span>

### <a name="examples---istmp"></a><span data-ttu-id="8e3a3-662">例 - isTmp</span><span class="sxs-lookup"><span data-stu-id="8e3a3-662">Examples - isTmp</span></span>

<span data-ttu-id="8e3a3-663">次の例は、テーブルが一時テーブルかどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-663">The following example shows the retrieval of a value that indicates whether the table is a temporary table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(TmpWMSOrder)); 
if (dt) 
{ 
    print(strfmt("Temporary table: %1", dt.isTmp())); 
}
```

## <a name="method-isunionallview"></a><span data-ttu-id="8e3a3-664">メソッド isUnionAllView</span><span class="sxs-lookup"><span data-stu-id="8e3a3-664">Method isUnionAllView</span></span>

```xpp
public boolean isUnionAllView()
```

### <a name="return-value---isunionallview"></a><span data-ttu-id="8e3a3-665">戻り値 - isUnionAllView</span><span class="sxs-lookup"><span data-stu-id="8e3a3-665">Return Value - isUnionAllView</span></span>

## <a name="method-isvalidtimestatetable"></a><span data-ttu-id="8e3a3-666">メソッド isValidTimeStateTable</span><span class="sxs-lookup"><span data-stu-id="8e3a3-666">Method isValidTimeStateTable</span></span>

```xpp
public boolean isValidTimeStateTable()
```

### <a name="return-value---isvalidtimestatetable"></a><span data-ttu-id="8e3a3-667">戻り値 - isValidTimeStateTable</span><span class="sxs-lookup"><span data-stu-id="8e3a3-667">Return Value - isValidTimeStateTable</span></span>

## <a name="method-isview"></a><span data-ttu-id="8e3a3-668">メソッド isView</span><span class="sxs-lookup"><span data-stu-id="8e3a3-668">Method isView</span></span>

<span data-ttu-id="8e3a3-669">テーブルがビューであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-669">Indicates whether the table is a view.</span></span>

```xpp
public boolean isView()
```

### <a name="return-value---isview"></a><span data-ttu-id="8e3a3-670">戻り値 - isView</span><span class="sxs-lookup"><span data-stu-id="8e3a3-670">Return Value - isView</span></span>

<span data-ttu-id="8e3a3-671">テーブルがビューである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-671">true if the table is a view; otherwise, false.</span></span>

### <a name="examples---isview"></a><span data-ttu-id="8e3a3-672">例 - isView</span><span class="sxs-lookup"><span data-stu-id="8e3a3-672">Examples - isView</span></span>

<span data-ttu-id="8e3a3-673">次の例は、テーブルがビューかどうかを示す値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-673">The following example shows the retrieval of a value that indicates whether the table is a view.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print(strfmt("View: %1", dt.isView())); 
}
```

## <a name="method-label"></a><span data-ttu-id="8e3a3-674">メソッド label</span><span class="sxs-lookup"><span data-stu-id="8e3a3-674">Method label</span></span>

<span data-ttu-id="8e3a3-675">テーブルのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-675">Returns the label text for the table.</span></span>

```xpp
public str label()
```

### <a name="return-value---label"></a><span data-ttu-id="8e3a3-676">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="8e3a3-676">Return Value - label</span></span>

<span data-ttu-id="8e3a3-677">テーブルのラベル テキスト。テーブルにラベル テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-677">The label text for the table; an empty string if there is no label text for the table.</span></span>

### <a name="examples---label"></a><span data-ttu-id="8e3a3-678">例 - label</span><span class="sxs-lookup"><span data-stu-id="8e3a3-678">Examples - label</span></span>

<span data-ttu-id="8e3a3-679">次の例は、テーブルのラベル テキストの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-679">The following example shows the retrieval of the label text for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
     print(strfmt("Label: %1", dt.label())); 
}
```

## <a name="method-labeldefined"></a><span data-ttu-id="8e3a3-680">メソッド labelDefined</span><span class="sxs-lookup"><span data-stu-id="8e3a3-680">Method labelDefined</span></span>

<span data-ttu-id="8e3a3-681">テーブルの label プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-681">Returns the value of the label property for the table.</span></span>

```xpp
public str labelDefined()
```

### <a name="return-value---labeldefined"></a><span data-ttu-id="8e3a3-682">戻り値 - labelDefined</span><span class="sxs-lookup"><span data-stu-id="8e3a3-682">Return Value - labelDefined</span></span>

<span data-ttu-id="8e3a3-683">テーブルの label プロパティの値。テーブルのラベル テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-683">The value of the label property for the table; an empty string if there is no label text for the table.</span></span>

## <a name="method-listpageref"></a><span data-ttu-id="8e3a3-684">メソッド listPageRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-684">Method listPageRef</span></span>

```xpp
public str listPageRef([boolean searchBaseTables])
```

### <a name="parameters---listpageref"></a><span data-ttu-id="8e3a3-685">パラメーター - listPageRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-685">Parameters - listPageRef</span></span>

<span data-ttu-id="8e3a3-686">searchBaseTables</span><span class="sxs-lookup"><span data-stu-id="8e3a3-686">searchBaseTables</span></span>  

### <a name="return-value---listpageref"></a><span data-ttu-id="8e3a3-687">戻り値 - listPageRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-687">Return Value - listPageRef</span></span>

## <a name="method-makerecord"></a><span data-ttu-id="8e3a3-688">メソッド makeRecord</span><span class="sxs-lookup"><span data-stu-id="8e3a3-688">Method makeRecord</span></span>

<span data-ttu-id="8e3a3-689">テーブルの空白のレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-689">Creates a blank record for the table.</span></span>

```xpp
public Common makeRecord()
```

### <a name="return-value---makerecord"></a><span data-ttu-id="8e3a3-690">戻り値 - makeRecord</span><span class="sxs-lookup"><span data-stu-id="8e3a3-690">Return Value - makeRecord</span></span>

<span data-ttu-id="8e3a3-691">レコードが正常に作成された場合の共通の値。レコードを作成できなかった場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-691">A Common value if the record was successfully created; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if the record could not be created.</span></span>

### <a name="remarks---makerecord"></a><span data-ttu-id="8e3a3-692">備考 - makeRecord</span><span class="sxs-lookup"><span data-stu-id="8e3a3-692">Remarks - makeRecord</span></span>

<span data-ttu-id="8e3a3-693">返される共通値は、DictTable.callObject メソッドの呼び出しで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-693">The Common value that is returned can be used in a call to the DictTable.callObject Method method.</span></span>

## <a name="method-maxaccessmode"></a><span data-ttu-id="8e3a3-694">メソッド maxAccessMode</span><span class="sxs-lookup"><span data-stu-id="8e3a3-694">Method maxAccessMode</span></span>

<span data-ttu-id="8e3a3-695">AOT 内で設定されているとおり、テーブルの MaxAccessMode プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-695">Returns the value of the MaxAccessMode property for a table, as set in the AOT.</span></span>

```xpp
public AccessType maxAccessMode()
```

### <a name="return-value---maxaccessmode"></a><span data-ttu-id="8e3a3-696">戻り値 - maxAccessMode</span><span class="sxs-lookup"><span data-stu-id="8e3a3-696">Return Value - maxAccessMode</span></span>

<span data-ttu-id="8e3a3-697">テーブルの最大アクセス モードを表す AccessType 値。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-697">A AccessType value that represents the maximum access mode for the table.</span></span>

### <a name="examples---maxaccessmode"></a><span data-ttu-id="8e3a3-698">例 - maxAccessMode</span><span class="sxs-lookup"><span data-stu-id="8e3a3-698">Examples - maxAccessMode</span></span>

<span data-ttu-id="8e3a3-699">次の例は、テーブルの最大アクセス モードの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-699">The following example shows the retrieval of the maximum access mode for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print strfmt("Maximum Access Mode: %1",dt.maxAccessMode()); 
}
```

## <a name="method-name"></a><span data-ttu-id="8e3a3-700">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8e3a3-700">Method name</span></span>

<span data-ttu-id="8e3a3-701">テーブル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-701">Retrieves the name of the table.</span></span>

```xpp
public str name([DbBackend db], [boolean pseudoname])
```

### <a name="parameters---name"></a><span data-ttu-id="8e3a3-702">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="8e3a3-702">Parameters - name</span></span>

<span data-ttu-id="8e3a3-703">db</span><span class="sxs-lookup"><span data-stu-id="8e3a3-703">db</span></span>  
<span data-ttu-id="8e3a3-704">疑似名が返されるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-704">A Boolean value that indicates whether a pseudo name is returned; optional.</span></span>

<!-- -->

<span data-ttu-id="8e3a3-705">pseudoname</span><span class="sxs-lookup"><span data-stu-id="8e3a3-705">pseudoname</span></span>  
<span data-ttu-id="8e3a3-706">疑似名が返されるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-706">A Boolean value that indicates whether a pseudo name is returned; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="8e3a3-707">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="8e3a3-707">Return Value - name</span></span>

<span data-ttu-id="8e3a3-708">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-708">The name of the table.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="8e3a3-709">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="8e3a3-709">Remarks - name</span></span>

<span data-ttu-id="8e3a3-710">テーブル名が 30 文字よりも長い場合は、ネイティブ名およびテーブルの SQL 名は一致しません。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-710">If the table name is longer than 30 characters, the native name and SQL name of the table do not match.</span></span>

### <a name="examples---name"></a><span data-ttu-id="8e3a3-711">例 - 名前</span><span class="sxs-lookup"><span data-stu-id="8e3a3-711">Examples - name</span></span>

<span data-ttu-id="8e3a3-712">次の例は、テーブルの名前の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-712">The following example shows the retrieval of the name of a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(1);  // 1 == tablenum(CustTable) 
if (dt) 
{ 
    print(strfmt("The table name is %1.", dt.name())); 
}
```

## <a name="method-objectmethod"></a><span data-ttu-id="8e3a3-713">メソッド objectMethod</span><span class="sxs-lookup"><span data-stu-id="8e3a3-713">Method objectMethod</span></span>

<span data-ttu-id="8e3a3-714">インデックスで指定されるインスタンス メソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-714">Returns the name of an instance method that is specified by index.</span></span>

```xpp
public str objectMethod(int methodNumber, [TableScope tableScope])
```

### <a name="parameters---objectmethod"></a><span data-ttu-id="8e3a3-715">パラメーター - objectMethod</span><span class="sxs-lookup"><span data-stu-id="8e3a3-715">Parameters - objectMethod</span></span>

<span data-ttu-id="8e3a3-716">methodNumber</span><span class="sxs-lookup"><span data-stu-id="8e3a3-716">methodNumber</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-717">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-717">tableScope</span></span>  

### <a name="return-value---objectmethod"></a><span data-ttu-id="8e3a3-718">戻り値 - objectMethod</span><span class="sxs-lookup"><span data-stu-id="8e3a3-718">Return Value - objectMethod</span></span>

<span data-ttu-id="8e3a3-719">methodNumber パラメーターで指定されているインスタンス メソッドの名前。methodNumber 値が有効なインスタンス メソッド インデックスでない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-719">The name of the instance method that is specified by the methodNumber parameter; an empty string if the methodNumber value is not a valid instance method index.</span></span>

### <a name="examples---objectmethod"></a><span data-ttu-id="8e3a3-720">例 - objectMethod</span><span class="sxs-lookup"><span data-stu-id="8e3a3-720">Examples - objectMethod</span></span>

<span data-ttu-id="8e3a3-721">次の例は、テーブル内の各インスタンス メソッドの名前の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-721">The following example shows the retrieval of the name of each instance method in a table.</span></span>

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.objectMethodCnt() ; i++) 
    { 
        print dt.objectMethod(i); 
    } 
}
```

## <a name="method-objectmethodcnt"></a><span data-ttu-id="8e3a3-722">メソッド objectMethodCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-722">Method objectMethodCnt</span></span>

<span data-ttu-id="8e3a3-723">テーブルのインスタンス メソッドの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-723">Returns the number of instance methods for the table.</span></span>

```xpp
public int objectMethodCnt([TableScope tableScope])
```

### <a name="parameters---objectmethodcnt"></a><span data-ttu-id="8e3a3-724">パラメーター - objectMethodCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-724">Parameters - objectMethodCnt</span></span>

<span data-ttu-id="8e3a3-725">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-725">tableScope</span></span>  

### <a name="return-value---objectmethodcnt"></a><span data-ttu-id="8e3a3-726">戻り値 - objectMethodCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-726">Return Value - objectMethodCnt</span></span>

<span data-ttu-id="8e3a3-727">テーブルのインスタンス メソッドの数。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-727">The number of instance methods for the table.</span></span>

### <a name="examples---objectmethodcnt"></a><span data-ttu-id="8e3a3-728">例 - objectMethodCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-728">Examples - objectMethodCnt</span></span>

<span data-ttu-id="8e3a3-729">次の例は、テーブルのインスタンス メソッド数の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-729">The following example shows the retrieval of the number of instance methods for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 instance methods.", dt.objectMethodCnt())); 
}
```

## <a name="method-objectmethodobject"></a><span data-ttu-id="8e3a3-730">メソッド objectMethodObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-730">Method objectMethodObject</span></span>

<span data-ttu-id="8e3a3-731">インデックスにより指定されているオブジェクト メソッドの MethodInfo クラスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-731">Returns an instance of the MethodInfo class for an object method that is specified by index.</span></span>

```xpp
public DictMethod objectMethodObject(int methodNumber, [TableScope tableScope])
```

### <a name="parameters---objectmethodobject"></a><span data-ttu-id="8e3a3-732">パラメーター - objectMethodObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-732">Parameters - objectMethodObject</span></span>

<span data-ttu-id="8e3a3-733">methodNumber</span><span class="sxs-lookup"><span data-stu-id="8e3a3-733">methodNumber</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-734">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-734">tableScope</span></span>  

### <a name="return-value---objectmethodobject"></a><span data-ttu-id="8e3a3-735">戻り値 - objectMethodObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-735">Return Value - objectMethodObject</span></span>

<span data-ttu-id="8e3a3-736">methodNumber パラメーターで指定されているオブジェクト メソッドの MethodInfo クラスのインスタンス。インスタンスを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-736">An instance of the MethodInfo class for the object method that is specified by the methodNumber parameter; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if the instance could not be created.</span></span>

### <a name="examples---objectmethodobject"></a><span data-ttu-id="8e3a3-737">例 - objectMethodObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-737">Examples - objectMethodObject</span></span>

<span data-ttu-id="8e3a3-738">次の例は、テーブルのオブジェクト メソッドの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-738">The following example shows the retrieval of the object methods for a table.</span></span>

```xpp
DictTable dt; 
int       i; 
MethodInfo mi; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.objectMethodCnt(); i++) 
    { 
        mi = dt.objectMethodObject(i); 
        if (mi) 
        { 
            print mi.name(); 
        } 
    } 
}
```

## <a name="method-mapobject"></a><span data-ttu-id="8e3a3-739">メソッド mapObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-739">Method mapObject</span></span>

<span data-ttu-id="8e3a3-740">インデックスで指定されているマッピングに対する \[t: DictTableMap\] クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-740">Creates an instance of the \[T: DictTableMap\] class for a mapping that is specified by index.</span></span>

```xpp
public DictTableMap mapObject(int methodNumber)
```

### <a name="parameters---mapobject"></a><span data-ttu-id="8e3a3-741">パラメーター - mapObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-741">Parameters - mapObject</span></span>

<span data-ttu-id="8e3a3-742">methodNumber</span><span class="sxs-lookup"><span data-stu-id="8e3a3-742">methodNumber</span></span>  

### <a name="return-value---mapobject"></a><span data-ttu-id="8e3a3-743">戻り値 - mapObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-743">Return Value - mapObject</span></span>

<span data-ttu-id="8e3a3-744">\_cnt パラメーターで指定されたフィールドの DictTableMap オブジェクト。オブジェクトを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-744">A DictTableMap object for the field that is specified by the \_cnt parameter; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if the object could not be created.</span></span>

## <a name="method-mapcnt"></a><span data-ttu-id="8e3a3-745">メソッド mapCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-745">Method mapCnt</span></span>

<span data-ttu-id="8e3a3-746">この DictTable インスタンスにより指定されているマップの使用可能なテーブル マッピングの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-746">Returns the count of available table mappings for the map that is specified by this DictTable instance.</span></span>

```xpp
public int mapCnt()
```

### <a name="return-value---mapcnt"></a><span data-ttu-id="8e3a3-747">戻り値 - mapCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-747">Return Value - mapCnt</span></span>

<span data-ttu-id="8e3a3-748">カウント。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-748">The count.</span></span>

## <a name="method-occenabled"></a><span data-ttu-id="8e3a3-749">メソッド occEnabled</span><span class="sxs-lookup"><span data-stu-id="8e3a3-749">Method occEnabled</span></span>

<span data-ttu-id="8e3a3-750">テーブルに対してオプティミスティック同時実行モードが有効になっているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-750">Indicates whether the optimistic concurrency mode has been enabled for a table.</span></span>

```xpp
public boolean occEnabled()
```

### <a name="return-value---occenabled"></a><span data-ttu-id="8e3a3-751">戻り値 - occEnabled</span><span class="sxs-lookup"><span data-stu-id="8e3a3-751">Return Value - occEnabled</span></span>

<span data-ttu-id="8e3a3-752">オプティミスティック同時モードが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-752">true if the optimistic concurrency mode is enabled; otherwise, false.</span></span>

### <a name="remarks---occenabled"></a><span data-ttu-id="8e3a3-753">備考 - occEnabled</span><span class="sxs-lookup"><span data-stu-id="8e3a3-753">Remarks - occEnabled</span></span>

<span data-ttu-id="8e3a3-754">このモードを有効にすると、データがデータベースからフェッチされるときに、データは今後の変更からロックされません。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-754">When this mode is enabled, data is not locked from future modification when it is fetched from the database.</span></span> <span data-ttu-id="8e3a3-755">データは、実際の更新の実行時にのみロックされます。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-755">Data is locked only when the actual update is performed.</span></span>

### <a name="examples---occenabled"></a><span data-ttu-id="8e3a3-756">例 - occEnabled</span><span class="sxs-lookup"><span data-stu-id="8e3a3-756">Examples - occEnabled</span></span>

<span data-ttu-id="8e3a3-757">次の例は、occEnabled メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-757">The following example shows a call to the occEnabled method.</span></span>

```xpp
static public void Main(Args _args) 
{ 
    DictTable dt; 
    boolean enabled; 
    dt = new DictTable(tablenum(CustTable)); 
    enabled = dt.occEnabled(); 
}
```

## <a name="method-primaryindex"></a><span data-ttu-id="8e3a3-758">メソッド primaryIndex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-758">Method primaryIndex</span></span>

<span data-ttu-id="8e3a3-759">テーブルのプライマリ インデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-759">Returns the ID of the primary index for the table.</span></span>

```xpp
public IndexId primaryIndex([boolean asDefinedInAOT])
```

### <a name="parameters---primaryindex"></a><span data-ttu-id="8e3a3-760">パラメーター - primaryIndex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-760">Parameters - primaryIndex</span></span>

<span data-ttu-id="8e3a3-761">asDefinedInAOT</span><span class="sxs-lookup"><span data-stu-id="8e3a3-761">asDefinedInAOT</span></span>  
<span data-ttu-id="8e3a3-762">取得するプライマリ インデックスが、AOT で定義されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-762">A Boolean value that indicates whether the primary index to retrieve is defined in the AOT.</span></span> <span data-ttu-id="8e3a3-763">true の値は、AOT で定義されたプライマリ インデックスを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-763">A value of true returns the primary index as defined in the AOT.</span></span> <span data-ttu-id="8e3a3-764">false の値は、SQL テーブルで定義されたプライマリ インデックスを返します、オプション。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-764">A value of false returns the primary index as defined in the SQL table; optional.</span></span>

### <a name="return-value---primaryindex"></a><span data-ttu-id="8e3a3-765">戻り値 - primaryIndex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-765">Return Value - primaryIndex</span></span>

<span data-ttu-id="8e3a3-766">テーブルの主インデックスの ID。テーブルの主インデックスがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-766">The ID of the primary index for the table; 0 (zero) if there is no primary index for the table.</span></span>

### <a name="examples---primaryindex"></a><span data-ttu-id="8e3a3-767">例 - primaryIndex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-767">Examples - primaryIndex</span></span>

<span data-ttu-id="8e3a3-768">次の例は、テーブルのプライマリ インデックスの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-768">The following example shows the retrieval of the primary index for a table.</span></span>

```xpp
DictTable dt; 
DictIndex di; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    i = dt.primaryIndex(); 
    if (0 != i) 
    { 
        di = new DictIndex(tablenum(CustTable), i); 
        print di.name(); 
    } 
}
```

## <a name="method-primarykeyfield"></a><span data-ttu-id="8e3a3-769">メソッド primaryKeyField</span><span class="sxs-lookup"><span data-stu-id="8e3a3-769">Method primaryKeyField</span></span>

<span data-ttu-id="8e3a3-770">テーブルの主キーに使用されているフィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-770">Returns the ID of the field that is used for the primary key of the table.</span></span>

```xpp
public FieldId primaryKeyField()
```

### <a name="return-value---primarykeyfield"></a><span data-ttu-id="8e3a3-771">戻り値 - primaryKeyField</span><span class="sxs-lookup"><span data-stu-id="8e3a3-771">Return Value - primaryKeyField</span></span>

<span data-ttu-id="8e3a3-772">テーブルの主キーで使用されるフィールドの ID。テーブルの主キーとして機能する単一のフィールドがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-772">The ID of the field that is used for the primary key of the table; 0 (zero) if no single field serves as the primary key of the table.</span></span>

### <a name="examples---primarykeyfield"></a><span data-ttu-id="8e3a3-773">例 - primaryKeyField</span><span class="sxs-lookup"><span data-stu-id="8e3a3-773">Examples - primaryKeyField</span></span>

<span data-ttu-id="8e3a3-774">次の例は、テーブルの主キーのフィールド ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-774">The following example shows the retrieval of the field ID of the primary key for the table.</span></span>

```xpp
DictTable dt; 
DictField df; 
tableId   tID; 
fieldId   fID; 
tID = tablenum(CustTable); 
dt = new DictTable(tID); 
if (dt) 
{ 
   fID = dt.primaryKeyField(); 
   if (0 != fID) 
   { 
       df = new DictField(tID, fID); 
       if (df) 
       { 
            print strfmt("Primary key field name: %1", df.name()); 
       } 
   } 
}
```

## <a name="method-relation"></a><span data-ttu-id="8e3a3-775">メソッド relation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-775">Method relation</span></span>

<span data-ttu-id="8e3a3-776">インデックスで指定される関係の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-776">Returns the name of a relation that is specified by index.</span></span>

```xpp
public str relation(int RelationNumber, [TableScope tableScope])
```

### <a name="parameters---relation"></a><span data-ttu-id="8e3a3-777">パラメーター - relation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-777">Parameters - relation</span></span>

<span data-ttu-id="8e3a3-778">RelationNumber</span><span class="sxs-lookup"><span data-stu-id="8e3a3-778">RelationNumber</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-779">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-779">tableScope</span></span>  

### <a name="return-value---relation"></a><span data-ttu-id="8e3a3-780">戻り値 - relation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-780">Return Value - relation</span></span>

<span data-ttu-id="8e3a3-781">RelationNumber パラメーターで指定されているリレーションの名前。RelationNumber 値が有効なリレーション インデックスでない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-781">The name of the relation that is specified by the RelationNumber parameter; an empty string if the RelationNumber value is not a valid relation index.</span></span>

### <a name="examples---relation"></a><span data-ttu-id="8e3a3-782">例 - relation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-782">Examples - relation</span></span>

<span data-ttu-id="8e3a3-783">次の例は、テーブル内の各リレーションの名前の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-783">The following example shows the retrieval of the name for each relation in a table.</span></span>

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.relationCnt() ; i++) 
    { 
        print dt.relation(i); 
    } 
}
```

## <a name="method-relationcnt"></a><span data-ttu-id="8e3a3-784">メソッド relationCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-784">Method relationCnt</span></span>

<span data-ttu-id="8e3a3-785">テーブルの関係の数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-785">Returns the number of relations for the table.</span></span>

```xpp
public int relationCnt([TableScope tableScope])
```

### <a name="parameters---relationcnt"></a><span data-ttu-id="8e3a3-786">パラメーター - relationCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-786">Parameters - relationCnt</span></span>

<span data-ttu-id="8e3a3-787">tableScope</span><span class="sxs-lookup"><span data-stu-id="8e3a3-787">tableScope</span></span>  

### <a name="return-value---relationcnt"></a><span data-ttu-id="8e3a3-788">戻り値 - relationCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-788">Return Value - relationCnt</span></span>

<span data-ttu-id="8e3a3-789">テーブルのリレーションの番号。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-789">The number of relations for the table.</span></span>

### <a name="examples---relationcnt"></a><span data-ttu-id="8e3a3-790">例 - relationCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-790">Examples - relationCnt</span></span>

<span data-ttu-id="8e3a3-791">次の例は、テーブルのリレーション数の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-791">The following example shows the retrieval of the number of relations for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 relations.", dt.relationCnt())); 
}
```

## <a name="method-replacementkey"></a><span data-ttu-id="8e3a3-792">メソッド replacementKey</span><span class="sxs-lookup"><span data-stu-id="8e3a3-792">Method replacementKey</span></span>

```xpp
public IndexId replacementKey()
```

### <a name="return-value---replacementkey"></a><span data-ttu-id="8e3a3-793">戻り値 - replacementKey</span><span class="sxs-lookup"><span data-stu-id="8e3a3-793">Return Value - replacementKey</span></span>

## <a name="method-reportref"></a><span data-ttu-id="8e3a3-794">メソッド reportRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-794">Method reportRef</span></span>

<span data-ttu-id="8e3a3-795">テーブルの既定のレポートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-795">Returns the name of the default report for the table.</span></span>

```xpp
public str reportRef()
```

### <a name="return-value---reportref"></a><span data-ttu-id="8e3a3-796">戻り値 - reportRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-796">Return Value - reportRef</span></span>

<span data-ttu-id="8e3a3-797">テーブルの既定のレポートの名前。テーブルの既定のレポートがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-797">The name of the default report for the table; an empty string if there is no default report for the table.</span></span>

### <a name="examples---reportref"></a><span data-ttu-id="8e3a3-798">例 - reportRef</span><span class="sxs-lookup"><span data-stu-id="8e3a3-798">Examples - reportRef</span></span>

<span data-ttu-id="8e3a3-799">以下は、テーブルの既定のレポートの名前の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-799">The following shows the retrieval of the name of the default report for a table.</span></span>

```xpp
DictTable dt; 
str       strReport; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    strReport = dt.reportRef(); 
    print strfmt("Default report: %1", strReport != "" ? strReport : "None specified"); 
}
```

## <a name="method-rights"></a><span data-ttu-id="8e3a3-800">メソッド rights</span><span class="sxs-lookup"><span data-stu-id="8e3a3-800">Method rights</span></span>

<span data-ttu-id="8e3a3-801">テーブルに指定されている、現在のユーザーのアクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-801">Returns the access rights of the current user that is specified for the table.</span></span>

```xpp
public AccessType rights([boolean ignoreContext])
```

### <a name="parameters---rights"></a><span data-ttu-id="8e3a3-802">パラメーター - rights</span><span class="sxs-lookup"><span data-stu-id="8e3a3-802">Parameters - rights</span></span>

<span data-ttu-id="8e3a3-803">ignoreContext</span><span class="sxs-lookup"><span data-stu-id="8e3a3-803">ignoreContext</span></span>  

### <a name="return-value---rights"></a><span data-ttu-id="8e3a3-804">戻り値 - rights</span><span class="sxs-lookup"><span data-stu-id="8e3a3-804">Return Value - rights</span></span>

<span data-ttu-id="8e3a3-805">テーブルに指定されている、現在のユーザーのアクセス権。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-805">The access rights of the current user that is specified for the table.</span></span> <span data-ttu-id="8e3a3-806">戻り値は、AccessType システム列挙値の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-806">The return value can be one of the values in the AccessType system enumeration.</span></span>

## <a name="method-securitykeyid"></a><span data-ttu-id="8e3a3-807">メソッド securityKeyId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-807">Method securityKeyId</span></span>

<span data-ttu-id="8e3a3-808">テーブルのセキュリティ キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-808">Returns the ID of the security key for the table.</span></span>

```xpp
public SecurityKeyId securityKeyId()
```

### <a name="return-value---securitykeyid"></a><span data-ttu-id="8e3a3-809">戻り値 - securityKeyId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-809">Return Value - securityKeyId</span></span>

<span data-ttu-id="8e3a3-810">テーブルのセキュリティ キーの ID。テーブルのセキュリティ キーがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-810">The ID of the security key for the table; 0 (zero) if there is no security key for the table.</span></span>

## <a name="method-singularlabel"></a><span data-ttu-id="8e3a3-811">メソッド singularLabel</span><span class="sxs-lookup"><span data-stu-id="8e3a3-811">Method singularLabel</span></span>

```xpp
public str singularLabel([boolean labelTranslation])
```

### <a name="parameters---singularlabel"></a><span data-ttu-id="8e3a3-812">パラメーター - singularLabel</span><span class="sxs-lookup"><span data-stu-id="8e3a3-812">Parameters - singularLabel</span></span>

<span data-ttu-id="8e3a3-813">labelTranslation</span><span class="sxs-lookup"><span data-stu-id="8e3a3-813">labelTranslation</span></span>  

### <a name="return-value---singularlabel"></a><span data-ttu-id="8e3a3-814">戻り値 - singularLabel</span><span class="sxs-lookup"><span data-stu-id="8e3a3-814">Return Value - singularLabel</span></span>

## <a name="method-staticmethod"></a><span data-ttu-id="8e3a3-815">メソッド staticMethod</span><span class="sxs-lookup"><span data-stu-id="8e3a3-815">Method staticMethod</span></span>

<span data-ttu-id="8e3a3-816">インデックスで指定される静的メソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-816">Returns the name of a static method that is specified by index.</span></span>

```xpp
public str staticMethod(int methodNumber)
```

### <a name="parameters---staticmethod"></a><span data-ttu-id="8e3a3-817">パラメーター - staticMethod</span><span class="sxs-lookup"><span data-stu-id="8e3a3-817">Parameters - staticMethod</span></span>

<span data-ttu-id="8e3a3-818">methodNumber</span><span class="sxs-lookup"><span data-stu-id="8e3a3-818">methodNumber</span></span>  
<span data-ttu-id="8e3a3-819">テーブルの静的メソッドのリストへの AOT の順で、1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-819">The one-based index to the list of static methods for the table, in AOT order.</span></span>

### <a name="return-value---staticmethod"></a><span data-ttu-id="8e3a3-820">戻り値 - staticMethod</span><span class="sxs-lookup"><span data-stu-id="8e3a3-820">Return Value - staticMethod</span></span>

<span data-ttu-id="8e3a3-821">methodNumber パラメーターで指定されている静的メソッドの名前。methodNumber 値が有効な静的メソッド インデックスでない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-821">The name of the static method that is specified by the methodNumber parameter; an empty string if the methodNumber value is not a valid static method index.</span></span>

### <a name="examples---staticmethod"></a><span data-ttu-id="8e3a3-822">例 - staticMethod</span><span class="sxs-lookup"><span data-stu-id="8e3a3-822">Examples - staticMethod</span></span>

<span data-ttu-id="8e3a3-823">次の例は、テーブル内の各静的メソッドの名前の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-823">The following example shows the retrieval of the name of each static method in a table.</span></span>

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.staticMethodCnt() ; i++) 
    { 
        print dt.staticMethod(i); 
    } 
}
```

## <a name="method-staticmethodcnt"></a><span data-ttu-id="8e3a3-824">メソッド staticMethodCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-824">Method staticMethodCnt</span></span>

<span data-ttu-id="8e3a3-825">テーブルの静的メソッドの数を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-825">Returns the number of static methods for the table.</span></span>

```xpp
public int staticMethodCnt()
```

### <a name="return-value---staticmethodcnt"></a><span data-ttu-id="8e3a3-826">戻り値 - staticMethodCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-826">Return Value - staticMethodCnt</span></span>

<span data-ttu-id="8e3a3-827">テーブルの静的メソッドの数。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-827">The number of static methods for the table.</span></span>

### <a name="examples---staticmethodcnt"></a><span data-ttu-id="8e3a3-828">例 - staticMethodCnt</span><span class="sxs-lookup"><span data-stu-id="8e3a3-828">Examples - staticMethodCnt</span></span>

<span data-ttu-id="8e3a3-829">次の例は、テーブルの静的メソッド数の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-829">The following example shows the retrieval of the number of static methods for a table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 static methods.", dt. staticMethodCnt())); 
}
```

## <a name="method-staticmethodobject"></a><span data-ttu-id="8e3a3-830">メソッド staticMethodObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-830">Method staticMethodObject</span></span>

<span data-ttu-id="8e3a3-831">インデックスにより指定されている静的メソッドの MethodInfo クラスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-831">Returns an instance of the MethodInfo class for a static method that is specified by index.</span></span>

```xpp
public DictMethod staticMethodObject(int methodNumber)
```

### <a name="parameters---staticmethodobject"></a><span data-ttu-id="8e3a3-832">パラメーター - staticMethodObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-832">Parameters - staticMethodObject</span></span>

<span data-ttu-id="8e3a3-833">methodNumber</span><span class="sxs-lookup"><span data-stu-id="8e3a3-833">methodNumber</span></span>  
<span data-ttu-id="8e3a3-834">テーブルの静的メソッドへの AOT の順で、1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-834">The one-based index to the static methods for the table, in AOT order.</span></span>

### <a name="return-value---staticmethodobject"></a><span data-ttu-id="8e3a3-835">戻り値 - staticMethodObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-835">Return Value - staticMethodObject</span></span>

<span data-ttu-id="8e3a3-836">methodNumber パラメーターで指定されている静的メソッドの MethodInfo クラスのインスタンス。インスタンスを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-836">An instance of the MethodInfo class for the static method that is specified by the methodNumber parameter; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if the instance could not be created.</span></span>

### <a name="examples---staticmethodobject"></a><span data-ttu-id="8e3a3-837">例 - staticMethodObject</span><span class="sxs-lookup"><span data-stu-id="8e3a3-837">Examples - staticMethodObject</span></span>

<span data-ttu-id="8e3a3-838">次の例は、テーブルの静的メソッドの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-838">The following example shows the retrieval of the static methods for a table.</span></span>

```xpp
DictTable dt; 
int       i; 
MethodInfo mi; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.staticMethodCnt(); i++) 
    { 
        mi = dt.staticMethodObject(i); 
        if (mi) 
        { 
            print mi.name(); 
        } 
    } 
}
```

## <a name="method-supportinheritance"></a><span data-ttu-id="8e3a3-839">メソッド supportInheritance</span><span class="sxs-lookup"><span data-stu-id="8e3a3-839">Method supportInheritance</span></span>

```xpp
public boolean supportInheritance()
```

### <a name="return-value---supportinheritance"></a><span data-ttu-id="8e3a3-840">戻り値 - supportInheritance</span><span class="sxs-lookup"><span data-stu-id="8e3a3-840">Return Value - supportInheritance</span></span>

## <a name="method-tablegroup"></a><span data-ttu-id="8e3a3-841">メソッド tableGroup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-841">Method tableGroup</span></span>

<span data-ttu-id="8e3a3-842">テーブルのテーブル グループを返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-842">Returns the table group for a table.</span></span>

```xpp
public TableGroup tableGroup()
```

### <a name="return-value---tablegroup"></a><span data-ttu-id="8e3a3-843">戻り値 - tableGroup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-843">Return Value - tableGroup</span></span>

<span data-ttu-id="8e3a3-844">テーブルのテーブル グループを表す TableGroup 値。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-844">A TableGroup value that represents the table group of the table.</span></span>

### <a name="remarks---tablegroup"></a><span data-ttu-id="8e3a3-845">備考 - tableGroup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-845">Remarks - tableGroup</span></span>

<span data-ttu-id="8e3a3-846">戻り値は、AOT テーブルの TableGroup プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-846">The return value corresponds to the TableGroup property of the table in the AOT.</span></span>

### <a name="examples---tablegroup"></a><span data-ttu-id="8e3a3-847">例 - tableGroup</span><span class="sxs-lookup"><span data-stu-id="8e3a3-847">Examples - tableGroup</span></span>

<span data-ttu-id="8e3a3-848">次の例は、テーブルのテーブル グループの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-848">The following example shows the retrieval of the table group of the table.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
   print strfmt("Table Group: %1", dt.tableGroup()); 
}
```

## <a name="method-tabletype"></a><span data-ttu-id="8e3a3-849">メソッド tableType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-849">Method tableType</span></span>

<span data-ttu-id="8e3a3-850">テーブルのタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-850">Indicates the type of the table.</span></span>

```xpp
public TableType tableType()
```

### <a name="return-value---tabletype"></a><span data-ttu-id="8e3a3-851">戻り値 - tableType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-851">Return Value - tableType</span></span>

<span data-ttu-id="8e3a3-852">エラー状態がある場合は、エラー状態です。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-852">The error state, if there is any error state.</span></span>

## <a name="method-titlefield1"></a><span data-ttu-id="8e3a3-853">メソッド titleField1</span><span class="sxs-lookup"><span data-stu-id="8e3a3-853">Method titleField1</span></span>

<span data-ttu-id="8e3a3-854">テーブルの titleField1 プロパティを表すフィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-854">Returns the ID of the field that represents the titleField1 property of the table.</span></span>

```xpp
public FieldId titleField1([boolean includeBaseTables], [boolean extendedFieldId])
```

### <a name="parameters---titlefield1"></a><span data-ttu-id="8e3a3-855">パラメーター - titleField1</span><span class="sxs-lookup"><span data-stu-id="8e3a3-855">Parameters - titleField1</span></span>

<span data-ttu-id="8e3a3-856">includeBaseTables</span><span class="sxs-lookup"><span data-stu-id="8e3a3-856">includeBaseTables</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-857">extendedFieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-857">extendedFieldId</span></span>  

### <a name="return-value---titlefield1"></a><span data-ttu-id="8e3a3-858">戻り値 - titleField1</span><span class="sxs-lookup"><span data-stu-id="8e3a3-858">Return Value - titleField1</span></span>

<span data-ttu-id="8e3a3-859">テーブルの titleField1 プロパティを表すフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-859">The ID of the field that represents the titleField1 property of the table.</span></span>

### <a name="remarks---titlefield1"></a><span data-ttu-id="8e3a3-860">備考 - titleField1</span><span class="sxs-lookup"><span data-stu-id="8e3a3-860">Remarks - titleField1</span></span>

<span data-ttu-id="8e3a3-861">ベスト プラクティスのガイドラインに従うと、titleField1 プロパティは、テーブルのレコードのキー フィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-861">According to best practice guidelines, the titleField1 property represents the key field for the records in the table.</span></span>

### <a name="examples---titlefield1"></a><span data-ttu-id="8e3a3-862">例 - titleField1</span><span class="sxs-lookup"><span data-stu-id="8e3a3-862">Examples - titleField1</span></span>

<span data-ttu-id="8e3a3-863">次の例は、テーブルの titleField1 プロパティに使用されるフィールドの ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-863">The following example shows the retrieval of the ID of the field that is used for the titleField1 property of the table.</span></span>

```xpp
DictTable dt; 
DictField df; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    df = new DictField(tablenum(CustTable),dt.titleField1()); 
    if (df) 
    { 
        print df.name(); 
    } 
} 
pause;
```

## <a name="method-titlefield2"></a><span data-ttu-id="8e3a3-864">メソッド titleField2</span><span class="sxs-lookup"><span data-stu-id="8e3a3-864">Method titleField2</span></span>

<span data-ttu-id="8e3a3-865">テーブルの titleField2 プロパティを表すフィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-865">Returns the ID of the field that represents the titleField2 property of the table.</span></span>

```xpp
public FieldId titleField2([boolean includeBaseTables], [boolean extendedFieldId])
```

### <a name="parameters---titlefield2"></a><span data-ttu-id="8e3a3-866">パラメーター - titleField2</span><span class="sxs-lookup"><span data-stu-id="8e3a3-866">Parameters - titleField2</span></span>

<span data-ttu-id="8e3a3-867">includeBaseTables</span><span class="sxs-lookup"><span data-stu-id="8e3a3-867">includeBaseTables</span></span>  

<!-- -->

<span data-ttu-id="8e3a3-868">extendedFieldId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-868">extendedFieldId</span></span>  

### <a name="return-value---titlefield2"></a><span data-ttu-id="8e3a3-869">戻り値 - titleField2</span><span class="sxs-lookup"><span data-stu-id="8e3a3-869">Return Value - titleField2</span></span>

<span data-ttu-id="8e3a3-870">テーブルの titleField2 プロパティを表すフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-870">The ID of the field that represents the titleField2 property of the table.</span></span>

### <a name="remarks---titlefield2"></a><span data-ttu-id="8e3a3-871">備考 - titleField2</span><span class="sxs-lookup"><span data-stu-id="8e3a3-871">Remarks - titleField2</span></span>

<span data-ttu-id="8e3a3-872">ベスト プラクティスのガイドラインに従うと、titleField2 プロパティは、テーブルのレコードの説明を表します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-872">According to best practice guidelines, the titleField2 property represents the description of the records of the table.</span></span>

### <a name="examples---titlefield2"></a><span data-ttu-id="8e3a3-873">例 - titleField2</span><span class="sxs-lookup"><span data-stu-id="8e3a3-873">Examples - titleField2</span></span>

<span data-ttu-id="8e3a3-874">次の例は、テーブルの titleField2 プロパティに使用されるフィールドの ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-874">The following example shows the retrieval of the ID of the field that is used for the titleField2 property of the table.</span></span>

```xpp
DictTable dt; 
DictField df; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    df = new DictField(tablenum(CustTable),dt.titleField2()); 
    if (df) 
    { 
        print df.name(); 
    } 
}
```

## <a name="method-validrelationship"></a><span data-ttu-id="8e3a3-875">メソッド validRelationship</span><span class="sxs-lookup"><span data-stu-id="8e3a3-875">Method validRelationship</span></span>

```xpp
public boolean validRelationship()
```

### <a name="return-value---validrelationship"></a><span data-ttu-id="8e3a3-876">戻り値 - validRelationship</span><span class="sxs-lookup"><span data-stu-id="8e3a3-876">Return Value - validRelationship</span></span>

## <a name="method-visible"></a><span data-ttu-id="8e3a3-877">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="8e3a3-877">Method visible</span></span>

<span data-ttu-id="8e3a3-878">テーブルが表示できるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-878">Determines whether the table is visible.</span></span>

```xpp
public boolean visible()
```

### <a name="return-value---visible"></a><span data-ttu-id="8e3a3-879">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="8e3a3-879">Return Value - visible</span></span>

<span data-ttu-id="8e3a3-880">テーブルが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-880">true if the table is visible; otherwise, false.</span></span>

## <a name="method-construct"></a><span data-ttu-id="8e3a3-881">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="8e3a3-881">Method construct</span></span>

```xpp
public static DictTable construct(str tableName)
```

### <a name="parameters---construct"></a><span data-ttu-id="8e3a3-882">パラメーター - construct</span><span class="sxs-lookup"><span data-stu-id="8e3a3-882">Parameters - construct</span></span>

<span data-ttu-id="8e3a3-883">tableName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-883">tableName</span></span>  

### <a name="return-value---construct"></a><span data-ttu-id="8e3a3-884">戻り値 - construct</span><span class="sxs-lookup"><span data-stu-id="8e3a3-884">Return Value - construct</span></span>

## <a name="method-getrelationtypefromtablename"></a><span data-ttu-id="8e3a3-885">メソッド getRelationTypeFromTableName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-885">Method getRelationTypeFromTableName</span></span>

```xpp
public static RecId getRelationTypeFromTableName(TableName tableName)
```

### <a name="parameters---getrelationtypefromtablename"></a><span data-ttu-id="8e3a3-886">パラメーター - getRelationTypeFromTableName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-886">Parameters - getRelationTypeFromTableName</span></span>

<span data-ttu-id="8e3a3-887">tableName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-887">tableName</span></span>  

### <a name="return-value---getrelationtypefromtablename"></a><span data-ttu-id="8e3a3-888">戻り値 - getRelationTypeFromTableName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-888">Return Value - getRelationTypeFromTableName</span></span>

## <a name="method-gettablenamefromrelationtype"></a><span data-ttu-id="8e3a3-889">メソッド getTableNameFromRelationType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-889">Method getTableNameFromRelationType</span></span>

```xpp
public static TableName getTableNameFromRelationType(RecId relationType)
```

### <a name="parameters---gettablenamefromrelationtype"></a><span data-ttu-id="8e3a3-890">パラメーター - getTableNameFromRelationType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-890">Parameters - getTableNameFromRelationType</span></span>

<span data-ttu-id="8e3a3-891">relationType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-891">relationType</span></span>  

### <a name="return-value---gettablenamefromrelationtype"></a><span data-ttu-id="8e3a3-892">戻り値 - getTableNameFromRelationType</span><span class="sxs-lookup"><span data-stu-id="8e3a3-892">Return Value - getTableNameFromRelationType</span></span>

## <a name="method-createrecord"></a><span data-ttu-id="8e3a3-893">メソッド createRecord</span><span class="sxs-lookup"><span data-stu-id="8e3a3-893">Method createRecord</span></span>

```xpp
public static Common createRecord(str tableName)
```

### <a name="parameters---createrecord"></a><span data-ttu-id="8e3a3-894">パラメーター - createRecord</span><span class="sxs-lookup"><span data-stu-id="8e3a3-894">Parameters - createRecord</span></span>

<span data-ttu-id="8e3a3-895">tableName</span><span class="sxs-lookup"><span data-stu-id="8e3a3-895">tableName</span></span>  

### <a name="return-value---createrecord"></a><span data-ttu-id="8e3a3-896">戻り値 - createRecord</span><span class="sxs-lookup"><span data-stu-id="8e3a3-896">Return Value - createRecord</span></span>

## <a name="method-reloadsecurity"></a><span data-ttu-id="8e3a3-897">メソッド reloadSecurity</span><span class="sxs-lookup"><span data-stu-id="8e3a3-897">Method reloadSecurity</span></span>

<span data-ttu-id="8e3a3-898">テーブルの機能キー システムを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-898">Reloads the feature key system for the table.</span></span>

```xpp
public void reloadSecurity()
```

### <a name="examples---reloadsecurity"></a><span data-ttu-id="8e3a3-899">例 - reloadSecurity</span><span class="sxs-lookup"><span data-stu-id="8e3a3-899">Examples - reloadSecurity</span></span>

<span data-ttu-id="8e3a3-900">次の例では、テーブルの機能キー システムを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-900">The following example reloads the feature key system for a table.</span></span>

```xpp
dt.reloadSecurity()
```

## <a name="method-new"></a><span data-ttu-id="8e3a3-901">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8e3a3-901">Method new</span></span>

<span data-ttu-id="8e3a3-902">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-902">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(TableId tableId)
```

### <a name="parameters---new"></a><span data-ttu-id="8e3a3-903">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="8e3a3-903">Parameters - new</span></span>

<span data-ttu-id="8e3a3-904">tableId</span><span class="sxs-lookup"><span data-stu-id="8e3a3-904">tableId</span></span>  
<span data-ttu-id="8e3a3-905">DictTable クラスのインスタンスを作成するために使用されるテーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-905">The ID of the table that is used to create the instance of the DictTable class.</span></span>

### <a name="examples---new"></a><span data-ttu-id="8e3a3-906">例 - new</span><span class="sxs-lookup"><span data-stu-id="8e3a3-906">Examples - new</span></span>

<span data-ttu-id="8e3a3-907">次の例は、DictTable クラスのインスタンスを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-907">The following example shows how to create an instance of the DictTable class.</span></span>

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (!dt) 
{ 
    // Take error action. 
}
```

## <a name="method-reindex"></a><span data-ttu-id="8e3a3-908">メソッド reindex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-908">Method reindex</span></span>

<span data-ttu-id="8e3a3-909">テーブルのインデックスの再作成を実行します。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-909">Performs a reindex of the table.</span></span>

```xpp
public void reindex()
```

### <a name="remarks---reindex"></a><span data-ttu-id="8e3a3-910">備考 - reindex</span><span class="sxs-lookup"><span data-stu-id="8e3a3-910">Remarks - reindex</span></span>

<span data-ttu-id="8e3a3-911">SQL テーブルのインデックスの再作成にこのメソッドを使用しないでください。代わりに、SqlDataDictionary::tableReindex メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-911">Do not use this method to reindex SQL tables; instead, use the SqlDataDictionary::tableReindex method.</span></span> <span data-ttu-id="8e3a3-912">また、クライアントで実行時に DictTable::reindex メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="8e3a3-912">Additionally, the DictTable::reindex method is not supported when it is run on the client.</span></span>

