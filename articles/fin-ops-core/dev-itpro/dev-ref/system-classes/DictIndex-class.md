---
title: DictIndex クラス
description: このトピックでは、DictIndex クラスについて説明します。
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
ms.openlocfilehash: 90968356a9543452338e76bc18b3b2ec27977a09
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502986"
---
# <a name="class-dictindex"></a><span data-ttu-id="b62df-103">クラス DictIndex</span><span class="sxs-lookup"><span data-stu-id="b62df-103">Class DictIndex</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictIndex extends Object
```

<span data-ttu-id="b62df-104">DictIndex クラスは、テーブル インデックスに関するメタデータを返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-104">The DictIndex class returns metadata about a table index.</span></span>

## <a name="remarks"></a><span data-ttu-id="b62df-105">備考</span><span class="sxs-lookup"><span data-stu-id="b62df-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b62df-106">例</span><span class="sxs-lookup"><span data-stu-id="b62df-106">Examples</span></span>

<span data-ttu-id="b62df-107">次の例では、DictIndex クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b62df-107">The following example creates an instance of the DictIndex class.</span></span>

```xpp
Dictionary dict; 
DictTable  table; 
DictIndex  idx; 
dict = new Dictionary(); 
table = new DictTable(dict.tableName2Id("Address")); 
idx = new DictIndex(table.id(), table.indexName2Id("AddrIdx"));
```

## <a name="methods"></a><span data-ttu-id="b62df-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="b62df-108">Methods</span></span>

| <span data-ttu-id="b62df-109">方法</span><span class="sxs-lookup"><span data-stu-id="b62df-109">Method</span></span>                                                                                                                          | <span data-ttu-id="b62df-110">説明</span><span class="sxs-lookup"><span data-stu-id="b62df-110">Description</span></span>                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="b62df-111">public boolean allowDuplicates()</span><span class="sxs-lookup"><span data-stu-id="b62df-111">public boolean allowDuplicates()</span></span>                                                                                                | <span data-ttu-id="b62df-112">インデックスの allowDuplicates プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-112">Returns the value of the allowDuplicates property for the index.</span></span>      |
| <span data-ttu-id="b62df-113">public ConfigurationKeyId configurationKeyId()</span><span class="sxs-lookup"><span data-stu-id="b62df-113">public ConfigurationKeyId configurationKeyId()</span></span>                                                                                  | <span data-ttu-id="b62df-114">インデックスのコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-114">Returns the ID of the configuration key for the index.</span></span>                |
| <span data-ttu-id="b62df-115">public boolean enabled()</span><span class="sxs-lookup"><span data-stu-id="b62df-115">public boolean enabled()</span></span>                                                                                                        | <span data-ttu-id="b62df-116">インデックスが有効かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-116">Returns a value that indicates whether the index is enabled.</span></span>          |
| <span data-ttu-id="b62df-117">public FieldId field(int fieldNumber)</span><span class="sxs-lookup"><span data-stu-id="b62df-117">public FieldId field(int fieldNumber)</span></span>                                                                                           | <span data-ttu-id="b62df-118">インデックス内の指定したフィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-118">Returns the ID of the specified field in the index.</span></span>                   |
| <span data-ttu-id="b62df-119">public ValidTimeStateMode getValidTimeStateMode()</span><span class="sxs-lookup"><span data-stu-id="b62df-119">public ValidTimeStateMode getValidTimeStateMode()</span></span>                                                                               |                                                                       |
| <span data-ttu-id="b62df-120">public IndexId id()</span><span class="sxs-lookup"><span data-stu-id="b62df-120">public IndexId id()</span></span>                                                                                                             | <span data-ttu-id="b62df-121">インデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-121">Returns the ID of the index.</span></span>                                          |
| <span data-ttu-id="b62df-122">public FieldId includedColumn(int fieldNumber)</span><span class="sxs-lookup"><span data-stu-id="b62df-122">public FieldId includedColumn(int fieldNumber)</span></span>                                                                                  |                                                                       |
| <span data-ttu-id="b62df-123">public boolean isAlternateKey()</span><span class="sxs-lookup"><span data-stu-id="b62df-123">public boolean isAlternateKey()</span></span>                                                                                                 |                                                                       |
| <span data-ttu-id="b62df-124">public boolean isSql()</span><span class="sxs-lookup"><span data-stu-id="b62df-124">public boolean isSql()</span></span>                                                                                                          | <span data-ttu-id="b62df-125">インデックスが SQL データベースにあるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b62df-125">Gets a value that indicates whether the index is in the SQL database.</span></span> |
| <span data-ttu-id="b62df-126">public boolean isValidTimeStateKey()</span><span class="sxs-lookup"><span data-stu-id="b62df-126">public boolean isValidTimeStateKey()</span></span>                                                                                            |                                                                       |
| <span data-ttu-id="b62df-127">public boolean modify(boolean enabled, boolean allowDuplicates, boolean saveInLoadedLayer)</span><span class="sxs-lookup"><span data-stu-id="b62df-127">public boolean modify(boolean enabled, boolean allowDuplicates, boolean saveInLoadedLayer)</span></span>                                      | <span data-ttu-id="b62df-128">インデックスを変更します。</span><span class="sxs-lookup"><span data-stu-id="b62df-128">Modifies the index.</span></span>                                                   |
| <span data-ttu-id="b62df-129">public str name(\[DbBackend db\])</span><span class="sxs-lookup"><span data-stu-id="b62df-129">public str name(\[DbBackend db\])</span></span>                                                                                               | <span data-ttu-id="b62df-130">インデックスの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-130">Returns the name of the index.</span></span>                                        |
| <span data-ttu-id="b62df-131">public int numberOfFields()</span><span class="sxs-lookup"><span data-stu-id="b62df-131">public int numberOfFields()</span></span>                                                                                                     | <span data-ttu-id="b62df-132">インデックス定義のフィールドの数を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-132">Returns the number of fields in the index definition.</span></span>                 |
| <span data-ttu-id="b62df-133">public int numberOfIncludedColumns()</span><span class="sxs-lookup"><span data-stu-id="b62df-133">public int numberOfIncludedColumns()</span></span>                                                                                            |                                                                       |
| <span data-ttu-id="b62df-134">public boolean setAlternateKey(boolean alternateKey, boolean saveInLoadedLayer)</span><span class="sxs-lookup"><span data-stu-id="b62df-134">public boolean setAlternateKey(boolean alternateKey, boolean saveInLoadedLayer)</span></span>                                                 |                                                                       |
| <span data-ttu-id="b62df-135">public boolean setValidTimeStateKey(boolean setValidTimeStateKey, ValidTimeStateMode validTimeState, boolean saveInLoadedLayer)</span><span class="sxs-lookup"><span data-stu-id="b62df-135">public boolean setValidTimeStateKey(boolean setValidTimeStateKey, ValidTimeStateMode validTimeState, boolean saveInLoadedLayer)</span></span> |                                                                       |
| <span data-ttu-id="b62df-136">public TableId tableid()</span><span class="sxs-lookup"><span data-stu-id="b62df-136">public TableId tableid()</span></span>                                                                                                        | <span data-ttu-id="b62df-137">インデックスを含むテーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-137">Returns the ID of the table that contains the index.</span></span>                  |
| <span data-ttu-id="b62df-138">public void new(TableId tableId, IndexId indexId)</span><span class="sxs-lookup"><span data-stu-id="b62df-138">public void new(TableId tableId, IndexId indexId)</span></span>                                                                               | <span data-ttu-id="b62df-139">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b62df-139">Initializes a new instance of the Object class.</span></span>                       |

## <a name="method-allowduplicates"></a><span data-ttu-id="b62df-140">メソッド allowDuplicates</span><span class="sxs-lookup"><span data-stu-id="b62df-140">Method allowDuplicates</span></span>

<span data-ttu-id="b62df-141">インデックスの allowDuplicates プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-141">Returns the value of the allowDuplicates property for the index.</span></span>

```xpp
public boolean allowDuplicates()
```

### <a name="return-value---allowduplicates"></a><span data-ttu-id="b62df-142">戻り値 - allowDuplicates</span><span class="sxs-lookup"><span data-stu-id="b62df-142">Return Value - allowDuplicates</span></span>

<span data-ttu-id="b62df-143">インデックスが重複を許容する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b62df-143">true if the index allows duplicates; otherwise, false.</span></span>

## <a name="method-configurationkeyid"></a><span data-ttu-id="b62df-144">メソッド configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="b62df-144">Method configurationKeyId</span></span>

<span data-ttu-id="b62df-145">インデックスのコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-145">Returns the ID of the configuration key for the index.</span></span>

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a><span data-ttu-id="b62df-146">戻り値 - configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="b62df-146">Return Value - configurationKeyId</span></span>

<span data-ttu-id="b62df-147">インデックスのコンフィギュレーション キーの ID。インデックスにコンフィギュレーション キーがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="b62df-147">The ID of the configuration key for the index; 0 (zero) if the index does not have a configuration key.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="b62df-148">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="b62df-148">Method enabled</span></span>

<span data-ttu-id="b62df-149">インデックスが有効かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-149">Returns a value that indicates whether the index is enabled.</span></span>

```xpp
public boolean enabled()
```

### <a name="return-value---enabled"></a><span data-ttu-id="b62df-150">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="b62df-150">Return Value - enabled</span></span>

<span data-ttu-id="b62df-151">インデックスが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b62df-151">true if the index is enabled; otherwise, false.</span></span>

## <a name="method-field"></a><span data-ttu-id="b62df-152">メソッド field</span><span class="sxs-lookup"><span data-stu-id="b62df-152">Method field</span></span>

<span data-ttu-id="b62df-153">インデックス内の指定したフィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-153">Returns the ID of the specified field in the index.</span></span>

```xpp
public FieldId field(int fieldNumber)
```

### <a name="parameters---field"></a><span data-ttu-id="b62df-154">パラメーター - field</span><span class="sxs-lookup"><span data-stu-id="b62df-154">Parameters - field</span></span>

<span data-ttu-id="b62df-155">fieldNumber</span><span class="sxs-lookup"><span data-stu-id="b62df-155">fieldNumber</span></span>  
<span data-ttu-id="b62df-156">インデックス内のフィールドの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="b62df-156">The one-based index of the field in the index.</span></span>

### <a name="return-value---field"></a><span data-ttu-id="b62df-157">戻り値 - field</span><span class="sxs-lookup"><span data-stu-id="b62df-157">Return Value - field</span></span>

<span data-ttu-id="b62df-158">fieldNumber により指定されているフィールドの ID。fieldNumber が有効なフィールドを表していない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="b62df-158">The ID of the field that is specified by fieldNumber; 0 (zero) if fieldNumber does not represent a valid field.</span></span>

### <a name="examples---field"></a><span data-ttu-id="b62df-159">例 - field</span><span class="sxs-lookup"><span data-stu-id="b62df-159">Examples - field</span></span>

<span data-ttu-id="b62df-160">次の例は、インデックス内の各フィールドの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="b62df-160">The following example shows the retrieval of each field in an index.</span></span> <span data-ttu-id="b62df-161">各フィールドの名前は、ループを使用して表示されます。</span><span class="sxs-lookup"><span data-stu-id="b62df-161">The name of each field is displayed by using a loop.</span></span>

```xpp
Dictionary dict; 
DictTable  table; 
DictIndex  idx; 
DictField  field; 
int i; 
dict = new Dictionary(); 
table = new DictTable(dict.tableName2Id("Address")); 
idx = new DictIndex(table.id(), table.indexName2Id("AddrIdx")); 
for (i=1; i <= idx.numberOfFields(); i++) 
{ 
    field = new DictField(table.id(), idx.field(i)); 
    print field.name(); 
}
```

## <a name="method-getvalidtimestatemode"></a><span data-ttu-id="b62df-162">メソッド getValidTimeStateMode</span><span class="sxs-lookup"><span data-stu-id="b62df-162">Method getValidTimeStateMode</span></span>

```xpp
public ValidTimeStateMode getValidTimeStateMode()
```

### <a name="return-value---getvalidtimestatemode"></a><span data-ttu-id="b62df-163">戻り値 - getValidTimeStateMode</span><span class="sxs-lookup"><span data-stu-id="b62df-163">Return Value - getValidTimeStateMode</span></span>

## <a name="method-id"></a><span data-ttu-id="b62df-164">メソッド id</span><span class="sxs-lookup"><span data-stu-id="b62df-164">Method id</span></span>

<span data-ttu-id="b62df-165">インデックスの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-165">Returns the ID of the index.</span></span>

```xpp
public IndexId id()
```

### <a name="return-value---id"></a><span data-ttu-id="b62df-166">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="b62df-166">Return Value - id</span></span>

<span data-ttu-id="b62df-167">インデックスの ID です。</span><span class="sxs-lookup"><span data-stu-id="b62df-167">The ID of the index.</span></span>

## <a name="method-includedcolumn"></a><span data-ttu-id="b62df-168">メソッド includedColumn</span><span class="sxs-lookup"><span data-stu-id="b62df-168">Method includedColumn</span></span>

```xpp
public FieldId includedColumn(int fieldNumber)
```

### <a name="parameters---includedcolumn"></a><span data-ttu-id="b62df-169">パラメーター - includedColumn</span><span class="sxs-lookup"><span data-stu-id="b62df-169">Parameters - includedColumn</span></span>

<span data-ttu-id="b62df-170">fieldNumber</span><span class="sxs-lookup"><span data-stu-id="b62df-170">fieldNumber</span></span>  

### <a name="return-value---includedcolumn"></a><span data-ttu-id="b62df-171">戻り値 - includedColumn</span><span class="sxs-lookup"><span data-stu-id="b62df-171">Return Value - includedColumn</span></span>

## <a name="method-isalternatekey"></a><span data-ttu-id="b62df-172">メソッド isAlternateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-172">Method isAlternateKey</span></span>

```xpp
public boolean isAlternateKey()
```

### <a name="return-value---isalternatekey"></a><span data-ttu-id="b62df-173">戻り値 - isAlternateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-173">Return Value - isAlternateKey</span></span>

## <a name="method-issql"></a><span data-ttu-id="b62df-174">メソッド isSql</span><span class="sxs-lookup"><span data-stu-id="b62df-174">Method isSql</span></span>

<span data-ttu-id="b62df-175">インデックスが SQL データベースにあるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="b62df-175">Gets a value that indicates whether the index is in the SQL database.</span></span>

```xpp
public boolean isSql()
```

### <a name="return-value---issql"></a><span data-ttu-id="b62df-176">戻り値 - isSql</span><span class="sxs-lookup"><span data-stu-id="b62df-176">Return Value - isSql</span></span>

<span data-ttu-id="b62df-177">インデックスが SQL データベースである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b62df-177">true if the index is in the SQL database; otherwise, false.</span></span>

## <a name="method-isvalidtimestatekey"></a><span data-ttu-id="b62df-178">メソッド isValidTimeStateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-178">Method isValidTimeStateKey</span></span>

```xpp
public boolean isValidTimeStateKey()
```

### <a name="return-value---isvalidtimestatekey"></a><span data-ttu-id="b62df-179">戻り値 - isValidTimeStateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-179">Return Value - isValidTimeStateKey</span></span>

## <a name="method-modify"></a><span data-ttu-id="b62df-180">メソッド modify</span><span class="sxs-lookup"><span data-stu-id="b62df-180">Method modify</span></span>

<span data-ttu-id="b62df-181">インデックスを変更します。</span><span class="sxs-lookup"><span data-stu-id="b62df-181">Modifies the index.</span></span>

```xpp
public boolean modify(boolean enabled, boolean allowDuplicates, boolean saveInLoadedLayer)
```

### <a name="parameters---modify"></a><span data-ttu-id="b62df-182">パラメーター - modify</span><span class="sxs-lookup"><span data-stu-id="b62df-182">Parameters - modify</span></span>

<span data-ttu-id="b62df-183">有効</span><span class="sxs-lookup"><span data-stu-id="b62df-183">enabled</span></span>  
<span data-ttu-id="b62df-184">読み込まれたレイヤーに変更が保存されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b62df-184">A Boolean value that indicates whether the modification is saved in the layer that is loaded.</span></span>

<!-- -->

<span data-ttu-id="b62df-185">allowDuplicates</span><span class="sxs-lookup"><span data-stu-id="b62df-185">allowDuplicates</span></span>  
<span data-ttu-id="b62df-186">読み込まれたレイヤーに変更が保存されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b62df-186">A Boolean value that indicates whether the modification is saved in the layer that is loaded.</span></span>

<!-- -->

<span data-ttu-id="b62df-187">saveInLoadedLayer</span><span class="sxs-lookup"><span data-stu-id="b62df-187">saveInLoadedLayer</span></span>  
<span data-ttu-id="b62df-188">読み込まれたレイヤーに変更が保存されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="b62df-188">A Boolean value that indicates whether the modification is saved in the layer that is loaded.</span></span>

### <a name="return-value---modify"></a><span data-ttu-id="b62df-189">戻り値 - modify</span><span class="sxs-lookup"><span data-stu-id="b62df-189">Return Value - modify</span></span>

<span data-ttu-id="b62df-190">インデックスが正常に修正された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b62df-190">true if the index was successfully modified; otherwise, false.</span></span>

### <a name="remarks---modify"></a><span data-ttu-id="b62df-191">備考 - modify</span><span class="sxs-lookup"><span data-stu-id="b62df-191">Remarks - modify</span></span>

<span data-ttu-id="b62df-192">このメソッドを使用すると、X++ コードとメタデータを作成、読み込み、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="b62df-192">This method lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="b62df-193">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b62df-193">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="method-name"></a><span data-ttu-id="b62df-194">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b62df-194">Method name</span></span>

<span data-ttu-id="b62df-195">インデックスの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-195">Returns the name of the index.</span></span>

```xpp
public str name([DbBackend db])
```

### <a name="parameters---name"></a><span data-ttu-id="b62df-196">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="b62df-196">Parameters - name</span></span>

<span data-ttu-id="b62df-197">db</span><span class="sxs-lookup"><span data-stu-id="b62df-197">db</span></span>  
<span data-ttu-id="b62df-198">返される名前のタイプを指定する DbBackend 値。</span><span class="sxs-lookup"><span data-stu-id="b62df-198">A DbBackend value that specifies the type of name to return.</span></span> <span data-ttu-id="b62df-199">これは、インデックスのネイティブ名の場合は DbBackend::Native、インデックスの SQL 名の場合は DbBackend::Sql になります。</span><span class="sxs-lookup"><span data-stu-id="b62df-199">This can be DbBackend::Native for the native name of the index or DbBackend::Sql for the SQL name of the index.</span></span> <span data-ttu-id="b62df-200">db が指定されていない場合は、DbBackend::Native が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b62df-200">If db is not specified, DbBackend::Native is used.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="b62df-201">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="b62df-201">Return Value - name</span></span>

<span data-ttu-id="b62df-202">データベースで指定された形式のインデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="b62df-202">The name of the index in the format that is specified by db.</span></span>

## <a name="method-numberoffields"></a><span data-ttu-id="b62df-203">メソッド numberOfFields</span><span class="sxs-lookup"><span data-stu-id="b62df-203">Method numberOfFields</span></span>

<span data-ttu-id="b62df-204">インデックス定義のフィールドの数を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-204">Returns the number of fields in the index definition.</span></span>

```xpp
public int numberOfFields()
```

### <a name="return-value---numberoffields"></a><span data-ttu-id="b62df-205">戻り値 - numberOfFields</span><span class="sxs-lookup"><span data-stu-id="b62df-205">Return Value - numberOfFields</span></span>

<span data-ttu-id="b62df-206">インデックス内のフィールドの数。</span><span class="sxs-lookup"><span data-stu-id="b62df-206">The number of fields in the index.</span></span>

### <a name="examples---numberoffields"></a><span data-ttu-id="b62df-207">例 - numberOfFields</span><span class="sxs-lookup"><span data-stu-id="b62df-207">Examples - numberOfFields</span></span>

<span data-ttu-id="b62df-208">次の例は、インデックス内のフィールド数の取得を示し、インデックス内のフィールドの名前をリストしています。</span><span class="sxs-lookup"><span data-stu-id="b62df-208">The following example shows the retrieval of the number of fields in the index and lists the names of the fields in the index.</span></span>

```xpp
Dictionary dict; 
DictTable  table; 
DictIndex  idx; 
DictField  field; 
int i; 
dict = new Dictionary(); 
table = new DictTable(dict.tableName2Id("Address")); 
idx = new DictIndex(table.id(), table.indexName2Id("AddrIdx")); 
for (i=1; i <= idx.numberOfFields(); i++) 
{ 
    field = new DictField(table.id(), idx.field(i)); 
    print field.name(); 
}
```

## <a name="method-numberofincludedcolumns"></a><span data-ttu-id="b62df-209">メソッド numberOfIncludedColumns</span><span class="sxs-lookup"><span data-stu-id="b62df-209">Method numberOfIncludedColumns</span></span>

```xpp
public int numberOfIncludedColumns()
```

### <a name="return-value---numberofincludedcolumns"></a><span data-ttu-id="b62df-210">戻り値 - numberOfIncludedColumns</span><span class="sxs-lookup"><span data-stu-id="b62df-210">Return Value - numberOfIncludedColumns</span></span>

## <a name="method-setalternatekey"></a><span data-ttu-id="b62df-211">メソッド setAlternateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-211">Method setAlternateKey</span></span>

```xpp
public boolean setAlternateKey(boolean alternateKey, boolean saveInLoadedLayer)
```

### <a name="parameters---setalternatekey"></a><span data-ttu-id="b62df-212">パラメーター - setAlternateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-212">Parameters - setAlternateKey</span></span>

<span data-ttu-id="b62df-213">alternateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-213">alternateKey</span></span>  

<!-- -->

<span data-ttu-id="b62df-214">saveInLoadedLayer</span><span class="sxs-lookup"><span data-stu-id="b62df-214">saveInLoadedLayer</span></span>  

### <a name="return-value---setalternatekey"></a><span data-ttu-id="b62df-215">戻り値 - setAlternateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-215">Return Value - setAlternateKey</span></span>

## <a name="method-setvalidtimestatekey"></a><span data-ttu-id="b62df-216">メソッド setValidTimeStateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-216">Method setValidTimeStateKey</span></span>

```xpp
public boolean setValidTimeStateKey(boolean setValidTimeStateKey, ValidTimeStateMode validTimeState, boolean saveInLoadedLayer)
```

### <a name="parameters---setvalidtimestatekey"></a><span data-ttu-id="b62df-217">パラメーター - setValidTimeStateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-217">Parameters - setValidTimeStateKey</span></span>

<span data-ttu-id="b62df-218">setValidTimeStateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-218">setValidTimeStateKey</span></span>  

<!-- -->

<span data-ttu-id="b62df-219">validTimeState</span><span class="sxs-lookup"><span data-stu-id="b62df-219">validTimeState</span></span>  

<!-- -->

<span data-ttu-id="b62df-220">saveInLoadedLayer</span><span class="sxs-lookup"><span data-stu-id="b62df-220">saveInLoadedLayer</span></span>  

### <a name="return-value---setvalidtimestatekey"></a><span data-ttu-id="b62df-221">戻り値 - setValidTimeStateKey</span><span class="sxs-lookup"><span data-stu-id="b62df-221">Return Value - setValidTimeStateKey</span></span>

## <a name="method-tableid"></a><span data-ttu-id="b62df-222">メソッド tableid</span><span class="sxs-lookup"><span data-stu-id="b62df-222">Method tableid</span></span>

<span data-ttu-id="b62df-223">インデックスを含むテーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b62df-223">Returns the ID of the table that contains the index.</span></span>

```xpp
public TableId tableid()
```

### <a name="return-value---tableid"></a><span data-ttu-id="b62df-224">戻り値 - tableid</span><span class="sxs-lookup"><span data-stu-id="b62df-224">Return Value - tableid</span></span>

<span data-ttu-id="b62df-225">インデックスを含むテーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="b62df-225">The ID of the table that contains the index.</span></span>

## <a name="method-new"></a><span data-ttu-id="b62df-226">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b62df-226">Method new</span></span>

<span data-ttu-id="b62df-227">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b62df-227">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(TableId tableId, IndexId indexId)
```

### <a name="parameters---new"></a><span data-ttu-id="b62df-228">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="b62df-228">Parameters - new</span></span>

<span data-ttu-id="b62df-229">tableId</span><span class="sxs-lookup"><span data-stu-id="b62df-229">tableId</span></span>  
<span data-ttu-id="b62df-230">DictIndex クラスのこのインスタンスを作成するために使用されるインデックスの ID。</span><span class="sxs-lookup"><span data-stu-id="b62df-230">The ID of the index that is used to create this instance of the DictIndex class.</span></span>

<!-- -->

<span data-ttu-id="b62df-231">indexId</span><span class="sxs-lookup"><span data-stu-id="b62df-231">indexId</span></span>  
<span data-ttu-id="b62df-232">DictIndex クラスのこのインスタンスを作成するために使用されるインデックスの ID。</span><span class="sxs-lookup"><span data-stu-id="b62df-232">The ID of the index that is used to create this instance of the DictIndex class.</span></span>

