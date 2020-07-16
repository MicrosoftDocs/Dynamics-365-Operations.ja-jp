---
title: DictFieldGroup クラス
description: このトピックでは、DictFieldGroup クラスについて説明します。
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
ms.openlocfilehash: b8e6dcecbcdc4299c77fafe4f638ce4097822a09
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502988"
---
# <a name="class-dictfieldgroup"></a><span data-ttu-id="14f13-103">クラス DictFieldGroup</span><span class="sxs-lookup"><span data-stu-id="14f13-103">Class DictFieldGroup</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictFieldGroup extends Object
```

<span data-ttu-id="14f13-104">DictFieldGroup クラスは、テーブル内の固有のフィールド グループに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="14f13-104">The DictFieldGroup class provides information about a specific field group in a table.</span></span>

## <a name="remarks"></a><span data-ttu-id="14f13-105">備考</span><span class="sxs-lookup"><span data-stu-id="14f13-105">Remarks</span></span>

<span data-ttu-id="14f13-106">このクラスを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="14f13-106">For a code example that uses this class, see the DictFieldGroup.numberOfFields Method method.</span></span>

## <a name="examples"></a><span data-ttu-id="14f13-107">例</span><span class="sxs-lookup"><span data-stu-id="14f13-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="14f13-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="14f13-108">Methods</span></span>

| <span data-ttu-id="14f13-109">方法</span><span class="sxs-lookup"><span data-stu-id="14f13-109">Method</span></span>                                                                             | <span data-ttu-id="14f13-110">説明</span><span class="sxs-lookup"><span data-stu-id="14f13-110">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="14f13-111">public FieldId field(int fieldNumber)</span><span class="sxs-lookup"><span data-stu-id="14f13-111">public FieldId field(int fieldNumber)</span></span>                                              | <span data-ttu-id="14f13-112">フィールド グループから指定したフィールドを返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-112">Returns the specified field from the field group.</span></span>                                   |
| <span data-ttu-id="14f13-113">public str label()</span><span class="sxs-lookup"><span data-stu-id="14f13-113">public str label()</span></span>                                                                 | <span data-ttu-id="14f13-114">フィールド グループのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-114">Returns the label text of the field group.</span></span>                                          |
| <span data-ttu-id="14f13-115">public str labelId()</span><span class="sxs-lookup"><span data-stu-id="14f13-115">public str labelId()</span></span>                                                               | <span data-ttu-id="14f13-116">フィールド グループのラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-116">Returns the label ID of the field group.</span></span>                                            |
| <span data-ttu-id="14f13-117">public str methodName(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="14f13-117">public str methodName(FieldId fieldId)</span></span>                                             | <span data-ttu-id="14f13-118">フィールド グループから指定したメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-118">Returns the name of the specified method from the field group.</span></span>                      |
| <span data-ttu-id="14f13-119">public str name()</span><span class="sxs-lookup"><span data-stu-id="14f13-119">public str name()</span></span>                                                                  | <span data-ttu-id="14f13-120">フィールド グループの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-120">Returns the name of the field group.</span></span>                                                |
| <span data-ttu-id="14f13-121">public int numberOfFields()</span><span class="sxs-lookup"><span data-stu-id="14f13-121">public int numberOfFields()</span></span>                                                        | <span data-ttu-id="14f13-122">フィールド グループのテーブル フィールドの数と編集メソッドと表示メソッドを返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-122">Returns the number of table fields and edit and display methods in the field group.</span></span> |
| <span data-ttu-id="14f13-123">public TableId tableid()</span><span class="sxs-lookup"><span data-stu-id="14f13-123">public TableId tableid()</span></span>                                                           | <span data-ttu-id="14f13-124">フィールド グループに関連付けられたテーブル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-124">Returns the ID of the table that is associated with the field group.</span></span>                |
| <span data-ttu-id="14f13-125">public void new(TableId tableId, str FieldGroupName, \[TableId includeBaseTable\])</span><span class="sxs-lookup"><span data-stu-id="14f13-125">public void new(TableId tableId, str FieldGroupName, \[TableId includeBaseTable\])</span></span> | <span data-ttu-id="14f13-126">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14f13-126">Initializes a new instance of the Object class.</span></span>                                     |

## <a name="method-field"></a><span data-ttu-id="14f13-127">メソッド field</span><span class="sxs-lookup"><span data-stu-id="14f13-127">Method field</span></span>

<span data-ttu-id="14f13-128">フィールド グループから指定したフィールドを返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-128">Returns the specified field from the field group.</span></span>

```xpp
public FieldId field(int fieldNumber)
```

### <a name="parameters---field"></a><span data-ttu-id="14f13-129">パラメーター - field</span><span class="sxs-lookup"><span data-stu-id="14f13-129">Parameters - field</span></span>

<span data-ttu-id="14f13-130">fieldNumber</span><span class="sxs-lookup"><span data-stu-id="14f13-130">fieldNumber</span></span>  
<span data-ttu-id="14f13-131">フィールド グループのフィールド内のフィールドへの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="14f13-131">The one-based index to the list of fields in the field group.</span></span> <span data-ttu-id="14f13-132">インデックスは、アプリケーション オブジェクト ツリー (AOT) と同じ順序です。</span><span class="sxs-lookup"><span data-stu-id="14f13-132">The index is in the same order as the Application Object Tree (AOT).</span></span>

### <a name="return-value---field"></a><span data-ttu-id="14f13-133">戻り値 - field</span><span class="sxs-lookup"><span data-stu-id="14f13-133">Return Value - field</span></span>

<span data-ttu-id="14f13-134">フィールドのフィールド ID。</span><span class="sxs-lookup"><span data-stu-id="14f13-134">The field ID of the field.</span></span> <span data-ttu-id="14f13-135">品目が表示メソッドの場合は、ID は、フォーム 65280 + 0 から始まるメソッドのインデックスになります。</span><span class="sxs-lookup"><span data-stu-id="14f13-135">If the item is a display method, the ID is in the form 65280 + 0-based method index.</span></span>

### <a name="remarks---field"></a><span data-ttu-id="14f13-136">備考 - field</span><span class="sxs-lookup"><span data-stu-id="14f13-136">Remarks - field</span></span>

<span data-ttu-id="14f13-137">フィールド メソッドを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="14f13-137">For a code example that uses the Field method, see the DictFieldGroup.numberOfFields Method method.</span></span>

## <a name="method-label"></a><span data-ttu-id="14f13-138">メソッド label</span><span class="sxs-lookup"><span data-stu-id="14f13-138">Method label</span></span>

<span data-ttu-id="14f13-139">フィールド グループのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-139">Returns the label text of the field group.</span></span>

```xpp
public str label()
```

### <a name="return-value---label"></a><span data-ttu-id="14f13-140">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="14f13-140">Return Value - label</span></span>

<span data-ttu-id="14f13-141">フィールド グループのラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="14f13-141">The label text of the field group.</span></span>

## <a name="method-labelid"></a><span data-ttu-id="14f13-142">メソッド labelId</span><span class="sxs-lookup"><span data-stu-id="14f13-142">Method labelId</span></span>

<span data-ttu-id="14f13-143">フィールド グループのラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-143">Returns the label ID of the field group.</span></span>

```xpp
public str labelId()
```

### <a name="return-value---labelid"></a><span data-ttu-id="14f13-144">戻り値 - LabelId</span><span class="sxs-lookup"><span data-stu-id="14f13-144">Return Value - labelId</span></span>

<span data-ttu-id="14f13-145">フィールド グループのラベル ID。</span><span class="sxs-lookup"><span data-stu-id="14f13-145">The label ID of the field group.</span></span>

## <a name="method-methodname"></a><span data-ttu-id="14f13-146">メソッド methodName</span><span class="sxs-lookup"><span data-stu-id="14f13-146">Method methodName</span></span>

<span data-ttu-id="14f13-147">フィールド グループから指定したメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-147">Returns the name of the specified method from the field group.</span></span>

```xpp
public str methodName(FieldId fieldId)
```

### <a name="parameters---methodname"></a><span data-ttu-id="14f13-148">パラメーター - methodName</span><span class="sxs-lookup"><span data-stu-id="14f13-148">Parameters - methodName</span></span>

<span data-ttu-id="14f13-149">fieldId</span><span class="sxs-lookup"><span data-stu-id="14f13-149">fieldId</span></span>  
<span data-ttu-id="14f13-150">返されるメソッド名のフィールド メソッドへの呼び出しから返されるフィールド ID。</span><span class="sxs-lookup"><span data-stu-id="14f13-150">The field ID that is returned from a call to the field method for the method name to return.</span></span> <span data-ttu-id="14f13-151">有効なフィールド ID が使用されていることを確認するのは開発者の責任です。</span><span class="sxs-lookup"><span data-stu-id="14f13-151">It is the responsibility of the developer to make sure that a valid field ID is used.</span></span>

### <a name="return-value---methodname"></a><span data-ttu-id="14f13-152">戻り値 - methodName</span><span class="sxs-lookup"><span data-stu-id="14f13-152">Return Value - methodName</span></span>

<span data-ttu-id="14f13-153">フィールド グループから指定されたメソッドの名前。fieldId の値が 65280 より小さい場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="14f13-153">The name of the specified method from the field group; an empty string if the fieldId value is less than 65280.</span></span>

### <a name="remarks---methodname"></a><span data-ttu-id="14f13-154">備考 - methodName</span><span class="sxs-lookup"><span data-stu-id="14f13-154">Remarks - methodName</span></span>

<span data-ttu-id="14f13-155">メソッドは、メソッド インデックス + 65280 によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="14f13-155">Methods are specified by method index + 65280.</span></span> <span data-ttu-id="14f13-156">このメソッドを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="14f13-156">For a code example that uses this method, see the DictFieldGroup.numberOfFields Method method.</span></span>

## <a name="method-name"></a><span data-ttu-id="14f13-157">メソッド名</span><span class="sxs-lookup"><span data-stu-id="14f13-157">Method name</span></span>

<span data-ttu-id="14f13-158">フィールド グループの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-158">Returns the name of the field group.</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="14f13-159">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="14f13-159">Return Value - name</span></span>

<span data-ttu-id="14f13-160">フィールド グループの名前。</span><span class="sxs-lookup"><span data-stu-id="14f13-160">The name of the field group.</span></span>

## <a name="method-numberoffields"></a><span data-ttu-id="14f13-161">メソッド numberOfFields</span><span class="sxs-lookup"><span data-stu-id="14f13-161">Method numberOfFields</span></span>

<span data-ttu-id="14f13-162">フィールド グループのテーブル フィールドの数と編集メソッドと表示メソッドを返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-162">Returns the number of table fields and edit and display methods in the field group.</span></span>

```xpp
public int numberOfFields()
```

### <a name="return-value---numberoffields"></a><span data-ttu-id="14f13-163">戻り値 - numberOfFields</span><span class="sxs-lookup"><span data-stu-id="14f13-163">Return Value - numberOfFields</span></span>

<span data-ttu-id="14f13-164">フィールド グループのテーブル フィールドの数と編集メソッドと表示メソッド。</span><span class="sxs-lookup"><span data-stu-id="14f13-164">The number of table fields and edit and display methods in the field group.</span></span>

### <a name="examples---numberoffields"></a><span data-ttu-id="14f13-165">例 - numberOfFields</span><span class="sxs-lookup"><span data-stu-id="14f13-165">Examples - numberOfFields</span></span>

<span data-ttu-id="14f13-166">次の例は、フィールド グループのテーブル フィールド数と編集メソッドおよび表示メソッドの数の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="14f13-166">The following example shows the retrieval of the number of table fields and edit and display methods in a field group.</span></span>

```xpp
    DictFieldGroup  fldGrp; 
    DictField       fld; 
    fieldId         fldId; 
    tableId         tblId; 
    int             i; 
    tblId = tablenum("CustTable"); 
    fldGrp = new DictFieldGroup(tblId,"AutoReport"); 
    if (fldGrp) 
    {     for (i=1; i <= fldGrp.numberOfFields(); i++) 
         { 
             fldId = fldGrp.field(i); 
             fld  = new DictField(tblId, fldId); 
             if (fld) 
             { 
                print 'Field: ' + fld.name() 
       + ' (' + int2str(fldId) + ')'; 
             } 
             else 
             { 
                print 'MethodName: ' + fldGrp.methodName(fldId)  
                + ' (' + int2str(fldId) + ')'; 
             } 
         } 
    }
```

## <a name="method-tableid"></a><span data-ttu-id="14f13-167">メソッド tableid</span><span class="sxs-lookup"><span data-stu-id="14f13-167">Method tableid</span></span>

<span data-ttu-id="14f13-168">フィールド グループに関連付けられたテーブル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="14f13-168">Returns the ID of the table that is associated with the field group.</span></span>

```xpp
public TableId tableid()
```

### <a name="return-value---tableid"></a><span data-ttu-id="14f13-169">戻り値 - tableid</span><span class="sxs-lookup"><span data-stu-id="14f13-169">Return Value - tableid</span></span>

<span data-ttu-id="14f13-170">フィールド グループに関連付けられたテーブル ID。</span><span class="sxs-lookup"><span data-stu-id="14f13-170">The ID of the table that is associated with the field group.</span></span>

## <a name="method-new"></a><span data-ttu-id="14f13-171">メソッド new</span><span class="sxs-lookup"><span data-stu-id="14f13-171">Method new</span></span>

<span data-ttu-id="14f13-172">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="14f13-172">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(TableId tableId, str FieldGroupName, [TableId includeBaseTable])
```

### <a name="parameters---new"></a><span data-ttu-id="14f13-173">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="14f13-173">Parameters - new</span></span>

<span data-ttu-id="14f13-174">tableId</span><span class="sxs-lookup"><span data-stu-id="14f13-174">tableId</span></span>  

<!-- -->

<span data-ttu-id="14f13-175">FieldGroupName</span><span class="sxs-lookup"><span data-stu-id="14f13-175">FieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="14f13-176">includeBaseTable</span><span class="sxs-lookup"><span data-stu-id="14f13-176">includeBaseTable</span></span>  

### <a name="remarks---new"></a><span data-ttu-id="14f13-177">備考 - new</span><span class="sxs-lookup"><span data-stu-id="14f13-177">Remarks - new</span></span>

<span data-ttu-id="14f13-178">このメソッドを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="14f13-178">For a code example that uses this method, see the DictFieldGroup.numberOfFields Method method.</span></span>

