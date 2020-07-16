---
title: AOTTableFieldList クラス
description: このトピックでは、AOTTableFieldList クラスについて説明します。
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
ms.openlocfilehash: efb1cdc1d5f5a3afe1e95314657f0525361d6dd8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502752"
---
# <a name="class-aottablefieldlist"></a><span data-ttu-id="0aaad-103">クラス AOTTableFieldList</span><span class="sxs-lookup"><span data-stu-id="0aaad-103">Class AOTTableFieldList</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class AOTTableFieldList extends TreeNode
```

<span data-ttu-id="0aaad-104">AOTTableFieldList クラスは、テーブルのフィールド ノードを表し、フィールドをテーブルに追加するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-104">The AOTTableFieldList class represents the Fields node of a table and is also used to add fields to a table.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aaad-105">備考</span><span class="sxs-lookup"><span data-stu-id="0aaad-105">Remarks</span></span>

<span data-ttu-id="0aaad-106">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-106">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="0aaad-107">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-107">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="0aaad-108">開発者は、他の方法を使用してノードに関する一般的な情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-108">The developer can obtain general information on the node by using other methods.</span></span>

## <a name="examples"></a><span data-ttu-id="0aaad-109">例</span><span class="sxs-lookup"><span data-stu-id="0aaad-109">Examples</span></span>

<span data-ttu-id="0aaad-110">次の例では、列挙型のフィールドを TutorialJournalName テーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-110">The following example adds a field of the enum type to the TutorialJournalName table.</span></span>

```xpp
{ 
    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
```

```xpp
     if (!tfl.AOTFindChild('NewEnum')) 
     { 
         tfl.addEnum('NewEnum');  // Adds the field NewEnum. 
     } 
}
```

## <a name="methods"></a><span data-ttu-id="0aaad-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="0aaad-111">Methods</span></span>

| <span data-ttu-id="0aaad-112">方法</span><span class="sxs-lookup"><span data-stu-id="0aaad-112">Method</span></span>                             | <span data-ttu-id="0aaad-113">説明</span><span class="sxs-lookup"><span data-stu-id="0aaad-113">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0aaad-114">public void addInteger(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-114">public void addInteger(str name)</span></span>   | <span data-ttu-id="0aaad-115">現在のテーブルのフィールドのリストに整数型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-115">Adds a new field of the integer type to the list of fields for the current table.</span></span>   |
| <span data-ttu-id="0aaad-116">public void addGuid(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-116">public void addGuid(str name)</span></span>      |                                                                                     |
| <span data-ttu-id="0aaad-117">public void addContainer(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-117">public void addContainer(str name)</span></span> | <span data-ttu-id="0aaad-118">現在のテーブルのフィールドのリストにコンテナー型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-118">Adds a new field of the container type to the list of fields for the current table.</span></span> |
| <span data-ttu-id="0aaad-119">public void addInt64(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-119">public void addInt64(str name)</span></span>     |                                                                                     |
| <span data-ttu-id="0aaad-120">public void addDateTime(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-120">public void addDateTime(str name)</span></span>  |                                                                                     |
| <span data-ttu-id="0aaad-121">public void addDate(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-121">public void addDate(str name)</span></span>      | <span data-ttu-id="0aaad-122">現在のテーブルのフィールドのリストに日付型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-122">Adds a new field of the date type to the list of fields for the current table.</span></span>      |
| <span data-ttu-id="0aaad-123">public void addString(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-123">public void addString(str name)</span></span>    | <span data-ttu-id="0aaad-124">現在のテーブルのフィールドのリストに文字列型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-124">Adds a new field of the string type to the list of fields for the current table.</span></span>    |
| <span data-ttu-id="0aaad-125">public void addReal(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-125">public void addReal(str name)</span></span>      | <span data-ttu-id="0aaad-126">現在のテーブルのフィールドのリストに実数型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-126">Adds a new field of the real type to the list of fields for the current table.</span></span>      |
| <span data-ttu-id="0aaad-127">public void addTime(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-127">public void addTime(str name)</span></span>      | <span data-ttu-id="0aaad-128">現在のテーブルのフィールドのリストに時刻タイプの新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-128">Adds a new field of the time type to the list of fields for the current table.</span></span>      |
| <span data-ttu-id="0aaad-129">public void addEnum(str name)</span><span class="sxs-lookup"><span data-stu-id="0aaad-129">public void addEnum(str name)</span></span>      | <span data-ttu-id="0aaad-130">現在のテーブルのフィールドのリストに列挙型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-130">Adds a new field of the enum type to the list of fields for the current table.</span></span>      |

## <a name="method-addinteger"></a><span data-ttu-id="0aaad-131">メソッド addInteger</span><span class="sxs-lookup"><span data-stu-id="0aaad-131">Method addInteger</span></span>

<span data-ttu-id="0aaad-132">現在のテーブルのフィールドのリストに整数型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-132">Adds a new field of the integer type to the list of fields for the current table.</span></span>

```xpp
public void addInteger(str name)
```

### <a name="parameters---addinteger"></a><span data-ttu-id="0aaad-133">パラメーター - addInteger</span><span class="sxs-lookup"><span data-stu-id="0aaad-133">Parameters - addInteger</span></span>

<span data-ttu-id="0aaad-134">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-134">name</span></span>  
<span data-ttu-id="0aaad-135">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="0aaad-135">The name of the field to add.</span></span>

### <a name="remarks---addinteger"></a><span data-ttu-id="0aaad-136">備考 - addInteger</span><span class="sxs-lookup"><span data-stu-id="0aaad-136">Remarks - addInteger</span></span>

<span data-ttu-id="0aaad-137">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-137">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="0aaad-138">開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="0aaad-138">The developer must make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="0aaad-139">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-139">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

### <a name="examples---addinteger"></a><span data-ttu-id="0aaad-140">例 - addInteger</span><span class="sxs-lookup"><span data-stu-id="0aaad-140">Examples - addInteger</span></span>

<span data-ttu-id="0aaad-141">次のコード例は、整数型である、NewInteger フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-141">The following code example adds the NewInteger field, which is of the integer type, to the list of fields for the TutorialJournalName table.</span></span>

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
if (!tfl.AOTFindChild('NewInteger')) 
{ 
    tfl.addInteger('NewInteger'); 
}
```

## <a name="method-addguid"></a><span data-ttu-id="0aaad-142">メソッド addGuid</span><span class="sxs-lookup"><span data-stu-id="0aaad-142">Method addGuid</span></span>

```xpp
public void addGuid(str name)
```

### <a name="parameters---addguid"></a><span data-ttu-id="0aaad-143">パラメーター - addGuid</span><span class="sxs-lookup"><span data-stu-id="0aaad-143">Parameters - addGuid</span></span>

<span data-ttu-id="0aaad-144">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-144">name</span></span>  

## <a name="method-addcontainer"></a><span data-ttu-id="0aaad-145">メソッド addContainer</span><span class="sxs-lookup"><span data-stu-id="0aaad-145">Method addContainer</span></span>

<span data-ttu-id="0aaad-146">現在のテーブルのフィールドのリストにコンテナー型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-146">Adds a new field of the container type to the list of fields for the current table.</span></span>

```xpp
public void addContainer(str name)
```

### <a name="parameters---addcontainer"></a><span data-ttu-id="0aaad-147">パラメーター -addContainer</span><span class="sxs-lookup"><span data-stu-id="0aaad-147">Parameters - addContainer</span></span>

<span data-ttu-id="0aaad-148">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-148">name</span></span>  
<span data-ttu-id="0aaad-149">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="0aaad-149">The name of the field to add.</span></span>

### <a name="remarks---addcontainer"></a><span data-ttu-id="0aaad-150">備考 - addContainer</span><span class="sxs-lookup"><span data-stu-id="0aaad-150">Remarks - addContainer</span></span>

<span data-ttu-id="0aaad-151">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-151">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="0aaad-152">開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="0aaad-152">The developer must make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="0aaad-153">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-153">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

### <a name="examples---addcontainer"></a><span data-ttu-id="0aaad-154">例 - addContainer</span><span class="sxs-lookup"><span data-stu-id="0aaad-154">Examples - addContainer</span></span>

<span data-ttu-id="0aaad-155">次のコード例は、NewContainer フィールドと NewContainer1 フィールド (両方ともコンテナー タイプ) を TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-155">The following code example adds the NewContainer and NewContainer1 fields, which are both of the container type, to the list of fields of the TutorialJournalName table.</span></span>

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
```

```xpp
// Add a NewContainer field. 
tfl.addContainer('NewContainer'); 
```

```xpp
// Add a NewContainer1 field. 
tfl.addContainer('NewContainer');
```

## <a name="method-addint64"></a><span data-ttu-id="0aaad-156">メソッド addInt64</span><span class="sxs-lookup"><span data-stu-id="0aaad-156">Method addInt64</span></span>

```xpp
public void addInt64(str name)
```

### <a name="parameters---addint64"></a><span data-ttu-id="0aaad-157">パラメーター - addInt64</span><span class="sxs-lookup"><span data-stu-id="0aaad-157">Parameters - addInt64</span></span>

<span data-ttu-id="0aaad-158">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-158">name</span></span>  

## <a name="method-adddatetime"></a><span data-ttu-id="0aaad-159">メソッド addDateTime</span><span class="sxs-lookup"><span data-stu-id="0aaad-159">Method addDateTime</span></span>

```xpp
public void addDateTime(str name)
```

### <a name="parameters---adddatetime"></a><span data-ttu-id="0aaad-160">パラメーター - addDateTime</span><span class="sxs-lookup"><span data-stu-id="0aaad-160">Parameters - addDateTime</span></span>

<span data-ttu-id="0aaad-161">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-161">name</span></span>  

## <a name="method-adddate"></a><span data-ttu-id="0aaad-162">メソッド addDate</span><span class="sxs-lookup"><span data-stu-id="0aaad-162">Method addDate</span></span>

<span data-ttu-id="0aaad-163">現在のテーブルのフィールドのリストに日付型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-163">Adds a new field of the date type to the list of fields for the current table.</span></span>

```xpp
public void addDate(str name)
```

### <a name="parameters---adddate"></a><span data-ttu-id="0aaad-164">パラメーター - addDate</span><span class="sxs-lookup"><span data-stu-id="0aaad-164">Parameters - addDate</span></span>

<span data-ttu-id="0aaad-165">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-165">name</span></span>  
<span data-ttu-id="0aaad-166">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="0aaad-166">The name of the field to add.</span></span>

### <a name="remarks---adddate"></a><span data-ttu-id="0aaad-167">備考 - addDate</span><span class="sxs-lookup"><span data-stu-id="0aaad-167">Remarks - addDate</span></span>

<span data-ttu-id="0aaad-168">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-168">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="0aaad-169">開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="0aaad-169">The developer must make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="0aaad-170">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-170">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

### <a name="examples---adddate"></a><span data-ttu-id="0aaad-171">例 - addDate</span><span class="sxs-lookup"><span data-stu-id="0aaad-171">Examples - addDate</span></span>

<span data-ttu-id="0aaad-172">次のコード例は、日付タイプである、NewDate フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-172">The following code example adds the NewDate field, which is of the date type, to the list of fields for the TutorialJournalName table.</span></span>

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
if (!tfl.AOTFindChild('NewDate')) 
{ 
    tfl.addDate('NewDate'); 
}
```

## <a name="method-addstring"></a><span data-ttu-id="0aaad-173">メソッド addString</span><span class="sxs-lookup"><span data-stu-id="0aaad-173">Method addString</span></span>

<span data-ttu-id="0aaad-174">現在のテーブルのフィールドのリストに文字列型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-174">Adds a new field of the string type to the list of fields for the current table.</span></span>

```xpp
public void addString(str name)
```

### <a name="parameters---addstring"></a><span data-ttu-id="0aaad-175">パラメーター - addString</span><span class="sxs-lookup"><span data-stu-id="0aaad-175">Parameters - addString</span></span>

<span data-ttu-id="0aaad-176">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-176">name</span></span>  
<span data-ttu-id="0aaad-177">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="0aaad-177">The name of the field to add.</span></span>

### <a name="remarks---addstring"></a><span data-ttu-id="0aaad-178">備考 - addString</span><span class="sxs-lookup"><span data-stu-id="0aaad-178">Remarks - addString</span></span>

<span data-ttu-id="0aaad-179">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-179">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="0aaad-180">名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="0aaad-180">It is up to the developer to make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="0aaad-181">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-181">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

### <a name="examples---addstring"></a><span data-ttu-id="0aaad-182">例 - addString</span><span class="sxs-lookup"><span data-stu-id="0aaad-182">Examples - addString</span></span>

<span data-ttu-id="0aaad-183">次の例では、文字列型の NewString フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-183">The following example adds the NewString field, which is of the string type, to the list of fields for the TutorialJournalName table.</span></span>

```xpp
{ 
    AOTTableFieldList tfl = infolog.findNode( 
        '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
    if (!tfl.AOTFindChild('NewString')) 
    { 
        tfl.addString('NewString'); 
    } 
}
```

## <a name="method-addreal"></a><span data-ttu-id="0aaad-184">メソッド addReal</span><span class="sxs-lookup"><span data-stu-id="0aaad-184">Method addReal</span></span>

<span data-ttu-id="0aaad-185">現在のテーブルのフィールドのリストに実数型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-185">Adds a new field of the real type to the list of fields for the current table.</span></span>

```xpp
public void addReal(str name)
```

### <a name="parameters---addreal"></a><span data-ttu-id="0aaad-186">パラメーター - addReal</span><span class="sxs-lookup"><span data-stu-id="0aaad-186">Parameters - addReal</span></span>

<span data-ttu-id="0aaad-187">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-187">name</span></span>  
<span data-ttu-id="0aaad-188">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="0aaad-188">The name of the field to add.</span></span>

### <a name="remarks---addreal"></a><span data-ttu-id="0aaad-189">備考 - addReal</span><span class="sxs-lookup"><span data-stu-id="0aaad-189">Remarks - addReal</span></span>

<span data-ttu-id="0aaad-190">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-190">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="0aaad-191">名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="0aaad-191">It is up to the developer to make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="0aaad-192">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-192">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

### <a name="examples---addreal"></a><span data-ttu-id="0aaad-193">例 - addReal</span><span class="sxs-lookup"><span data-stu-id="0aaad-193">Examples - addReal</span></span>

<span data-ttu-id="0aaad-194">次の例では、実際の型の NewReal フィールドと NewReal1 フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-194">The following example adds the NewReal and NewReal1 fields, which is of the real type, to the list of fields for the TutorialJournalName table.</span></span>

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
// Add the field NewReal. 
tfl.addReal('NewReal'); 
// Add the field NewReal1. 
tfl.addReal('NewReal');
```

## <a name="method-addtime"></a><span data-ttu-id="0aaad-195">メソッド addTime</span><span class="sxs-lookup"><span data-stu-id="0aaad-195">Method addTime</span></span>

<span data-ttu-id="0aaad-196">現在のテーブルのフィールドのリストに時刻タイプの新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-196">Adds a new field of the time type to the list of fields for the current table.</span></span>

```xpp
public void addTime(str name)
```

### <a name="parameters---addtime"></a><span data-ttu-id="0aaad-197">パラメーター - addTime</span><span class="sxs-lookup"><span data-stu-id="0aaad-197">Parameters - addTime</span></span>

<span data-ttu-id="0aaad-198">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-198">name</span></span>  
<span data-ttu-id="0aaad-199">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="0aaad-199">The name of the field to add.</span></span>

### <a name="remarks---addtime"></a><span data-ttu-id="0aaad-200">備考 - addTime</span><span class="sxs-lookup"><span data-stu-id="0aaad-200">Remarks - addTime</span></span>

<span data-ttu-id="0aaad-201">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-201">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="0aaad-202">開発者は名前が予約語ではないことを確認する必要があります。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="0aaad-202">The developer must make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="0aaad-203">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-203">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

### <a name="examples---addtime"></a><span data-ttu-id="0aaad-204">例 - addTime</span><span class="sxs-lookup"><span data-stu-id="0aaad-204">Examples - addTime</span></span>

<span data-ttu-id="0aaad-205">次のコード例は、時間タイプである、NewTime フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-205">The following code example adds the NewTime field, which is of the time type, to the list of fields of the TutorialJournalName table.</span></span>

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
if (!tfl.AOTFindChild('NewTime')) 
{ 
    tfl.addTime('NewTime'); 
}
```

## <a name="method-addenum"></a><span data-ttu-id="0aaad-206">メソッド addEnum</span><span class="sxs-lookup"><span data-stu-id="0aaad-206">Method addEnum</span></span>

<span data-ttu-id="0aaad-207">現在のテーブルのフィールドのリストに列挙型の新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-207">Adds a new field of the enum type to the list of fields for the current table.</span></span>

```xpp
public void addEnum(str name)
```

### <a name="parameters---addenum"></a><span data-ttu-id="0aaad-208">パラメーター - addEnum</span><span class="sxs-lookup"><span data-stu-id="0aaad-208">Parameters - addEnum</span></span>

<span data-ttu-id="0aaad-209">名前</span><span class="sxs-lookup"><span data-stu-id="0aaad-209">name</span></span>  
<span data-ttu-id="0aaad-210">追加するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="0aaad-210">The name of the field to add.</span></span>

### <a name="remarks---addenum"></a><span data-ttu-id="0aaad-211">備考 - addEnum</span><span class="sxs-lookup"><span data-stu-id="0aaad-211">Remarks - addEnum</span></span>

<span data-ttu-id="0aaad-212">指定された名前がフィールド リスト内の既存のフィールドと一致する場合、新しいフィールドの名前に整数が追加され、固有のフィールド名が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-212">If the supplied name coincides with an existing field in the field list, an integer is appended to the name of the new field to make the field name unique.</span></span> <span data-ttu-id="0aaad-213">名前が予約語ではないことを確認するのは開発者次第です。予約語が指定されている場合、メソッドはエラーをスローしません。</span><span class="sxs-lookup"><span data-stu-id="0aaad-213">It is up to the developer to make sure that the name is not a reserved word; the method will not throw an error if a reserved word is specified.</span></span> <span data-ttu-id="0aaad-214">AOTfindChild メソッドを使用すると、フィールド名がすでに使用されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="0aaad-214">You can use the AOTfindChild method to determine whether a field name is already being used.</span></span>

### <a name="examples---addenum"></a><span data-ttu-id="0aaad-215">例 - addEnum</span><span class="sxs-lookup"><span data-stu-id="0aaad-215">Examples - addEnum</span></span>

<span data-ttu-id="0aaad-216">次の例では、列挙型の NewEnum フィールドを TutorialJournalName テーブルのフィールドのリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="0aaad-216">The following example adds the NewEnum field, which is of the enum type, to the list of fields of the TutorialJournalName table.</span></span>

```xpp
AOTTableFieldList tfl = infolog.findNode( 
    '\\Data Dictionary\\Tables\\TutorialJournalName\\Fields'); 
if (!tfl.AOTFindChild('NewEnum')) 
{ 
    tfl.addEnum('NewEnum');  // adds the field NewEnum 
}
```

