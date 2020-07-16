---
title: MethodInfo クラス
description: このトピックでは､MethodInfo クラスについて説明します。
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
ms.openlocfilehash: 0de113c74623d6f57bebb19ee713c7619706b32c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502572"
---
# <a name="class-methodinfo"></a><span data-ttu-id="c2387-103">クラス MethodInfo</span><span class="sxs-lookup"><span data-stu-id="c2387-103">Class MethodInfo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MethodInfo extends Object
```

<span data-ttu-id="c2387-104">指定したメソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c2387-104">Provides information about a specified method.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2387-105">備考</span><span class="sxs-lookup"><span data-stu-id="c2387-105">Remarks</span></span>

<span data-ttu-id="c2387-106">SysDictTable クラスを使用してテーブル メソッドを MethodInfo に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c2387-106">Assign a table method to MethodInfo by using the SysDictTable class.</span></span> <span data-ttu-id="c2387-107">SysDictClass クラスを使用してクラス メソッドを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c2387-107">Assign a class method by using the SysDictClass class.</span></span> <span data-ttu-id="c2387-108">次のクラスは MethodInfo を拡張しています。</span><span class="sxs-lookup"><span data-stu-id="c2387-108">The following classes extend MethodInfo:</span></span>

-   <span data-ttu-id="c2387-109">SysMethodInfo</span><span class="sxs-lookup"><span data-stu-id="c2387-109">SysMethodInfo</span></span>
-   <span data-ttu-id="c2387-110">DictMethod</span><span class="sxs-lookup"><span data-stu-id="c2387-110">DictMethod</span></span>

## <a name="examples"></a><span data-ttu-id="c2387-111">例</span><span class="sxs-lookup"><span data-stu-id="c2387-111">Examples</span></span>

<span data-ttu-id="c2387-112">次の例では、SysDictClass::ObjectMethodObject メソッドを使用して、FormBuildDataSource クラス オブジェクトのメソッドをMethodInfo クラスのインスタンスに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c2387-112">The following example uses the SysDictClass::ObjectMethodObject method to assign a method of a FormBuildDataSource Class object to an instance of the MethodInfo class.</span></span> <span data-ttu-id="c2387-113">整数値はメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-113">An integer value specifies the method.</span></span> <span data-ttu-id="c2387-114">MethodInfo.name メソッドは、メソッド名を返します。</span><span class="sxs-lookup"><span data-stu-id="c2387-114">The MethodInfo.name Method method returns the method name.</span></span>

```xpp
void getMethodInfo() 
{ 
    MethodInfo methodInfo; 
    SysDictClass sysDictClass; 
    str name; 
    try 
    { 
        sysDictClass = new SysDictClass(classnum(FormBuildDataSource)); 
        methodInfo = sysDictClass.objectMethodObject(1); 
        if(!methodInfo) 
        { 
            throw exception::Error; 
        } 
        name = methodInfo.name(); 
        print name; 
        pause; 
     } 
     catch (exception::Error) 
     { 
        print "The specified method does not exist"; 
        pause; 
     } 
}
```

## <a name="methods"></a><span data-ttu-id="c2387-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="c2387-115">Methods</span></span>

| <span data-ttu-id="c2387-116">方法</span><span class="sxs-lookup"><span data-stu-id="c2387-116">Method</span></span>                                                      | <span data-ttu-id="c2387-117">説明</span><span class="sxs-lookup"><span data-stu-id="c2387-117">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2387-118">public AccessSpecifier accessSpecifier()</span><span class="sxs-lookup"><span data-stu-id="c2387-118">public AccessSpecifier accessSpecifier()</span></span>                    | <span data-ttu-id="c2387-119">メソッドがパブリック、保護、またはプライベートかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-119">Specifies whether the method is public, protected, or private.</span></span>                                                                                |
| <span data-ttu-id="c2387-120">public boolean compiledOk()</span><span class="sxs-lookup"><span data-stu-id="c2387-120">public boolean compiledOk()</span></span>                                 | <span data-ttu-id="c2387-121">メソッドがコンパイルされているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-121">Specifies whether the method has compiled.</span></span>                                                                                                    |
| <span data-ttu-id="c2387-122">public TableId displayTableId()</span><span class="sxs-lookup"><span data-stu-id="c2387-122">public TableId displayTableId()</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="c2387-123">public DisplayFunctionType displayType()</span><span class="sxs-lookup"><span data-stu-id="c2387-123">public DisplayFunctionType displayType()</span></span>                    | <span data-ttu-id="c2387-124">メソッドの表示機能のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-124">Specifies the display function type of a method.</span></span>                                                                                              |
| <span data-ttu-id="c2387-125">public Array getAllAttributes()</span><span class="sxs-lookup"><span data-stu-id="c2387-125">public Array getAllAttributes()</span></span>                             | <span data-ttu-id="c2387-126">メソッドの属性の完全なセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="c2387-126">Gets the full set of attributes for the method.</span></span>                                                                                               |
| <span data-ttu-id="c2387-127">public Object getAttribute(str attribute)</span><span class="sxs-lookup"><span data-stu-id="c2387-127">public Object getAttribute(str attribute)</span></span>                   | <span data-ttu-id="c2387-128">クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="c2387-128">Gets the first matching attribute from the class header metadata, creates an instance of the Object class that represents it, and returns it.</span></span> |
| <span data-ttu-id="c2387-129">public Array getAttributes(str attribute)</span><span class="sxs-lookup"><span data-stu-id="c2387-129">public Array getAttributes(str attribute)</span></span>                   |                                                                                                                                               |
| <span data-ttu-id="c2387-130">public boolean isAbstract()</span><span class="sxs-lookup"><span data-stu-id="c2387-130">public boolean isAbstract()</span></span>                                 | <span data-ttu-id="c2387-131">メソッドが抽象かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c2387-131">Indicates whether the method is abstract.</span></span>                                                                                                     |
| <span data-ttu-id="c2387-132">public boolean isStatic()</span><span class="sxs-lookup"><span data-stu-id="c2387-132">public boolean isStatic()</span></span>                                   | <span data-ttu-id="c2387-133">メソッドが静的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-133">Specifies whether the method is static.</span></span>                                                                                                       |
| <span data-ttu-id="c2387-134">public str name()</span><span class="sxs-lookup"><span data-stu-id="c2387-134">public str name()</span></span>                                           | <span data-ttu-id="c2387-135">メソッドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-135">Specifies the name of a method.</span></span>                                                                                                               |
| <span data-ttu-id="c2387-136">public int noParms()</span><span class="sxs-lookup"><span data-stu-id="c2387-136">public int noParms()</span></span>                                        | <span data-ttu-id="c2387-137">メソッド内のパラメーターの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-137">Specifies the number of parameters in a method.</span></span>                                                                                               |
| <span data-ttu-id="c2387-138">public int noVars()</span><span class="sxs-lookup"><span data-stu-id="c2387-138">public int noVars()</span></span>                                         | <span data-ttu-id="c2387-139">メソッド内の変数の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-139">Specifies the number of variables in a method.</span></span>                                                                                                |
| <span data-ttu-id="c2387-140">public int parentId()</span><span class="sxs-lookup"><span data-stu-id="c2387-140">public int parentId()</span></span>                                       | <span data-ttu-id="c2387-141">テーブル メソッドのテーブル ID またはクラス メソッドのクラス ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-141">Specifies the table ID for a table method or the class ID for a class method.</span></span>                                                                 |
| <span data-ttu-id="c2387-142">public str propertyHelp()</span><span class="sxs-lookup"><span data-stu-id="c2387-142">public str propertyHelp()</span></span>                                   | <span data-ttu-id="c2387-143">メソッドがコントロールに設定または返すヘルプ テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-143">Specifies the Help text that a method sets or returns for a control.</span></span>                                                                          |
| <span data-ttu-id="c2387-144">public NoYes PropertyMethod()</span><span class="sxs-lookup"><span data-stu-id="c2387-144">public NoYes PropertyMethod()</span></span>                               | <span data-ttu-id="c2387-145">メソッドがプロパティ メソッドかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-145">Specifies whether a method is a property method.</span></span>                                                                                              |
| <span data-ttu-id="c2387-146">public int returnId()</span><span class="sxs-lookup"><span data-stu-id="c2387-146">public int returnId()</span></span>                                       | <span data-ttu-id="c2387-147">値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-147">Specifies the ID for certain return data types, such as extended data types and classes, for a method that returns a value.</span></span>                   |
| <span data-ttu-id="c2387-148">public Types returnType()</span><span class="sxs-lookup"><span data-stu-id="c2387-148">public Types returnType()</span></span>                                   | <span data-ttu-id="c2387-149">メソッドの戻り値の型を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-149">Specifies a method return type.</span></span>                                                                                                               |
| <span data-ttu-id="c2387-150">public ClassRunMode runMode()</span><span class="sxs-lookup"><span data-stu-id="c2387-150">public ClassRunMode runMode()</span></span>                               | <span data-ttu-id="c2387-151">メソッドが実行される場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-151">Specifies where a method is executed.</span></span>                                                                                                         |
| <span data-ttu-id="c2387-152">public int varId(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="c2387-152">public int varId(int variableNumber)</span></span>                        | <span data-ttu-id="c2387-153">変数を含むメソッドについて、拡張データ型や列挙値などの特定の変数のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-153">Specifies the ID for certain variable data types, such as extended data types and enums, for a method that contains variables.</span></span>                |
| <span data-ttu-id="c2387-154">public int varIdOld(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="c2387-154">public int varIdOld(int variableNumber)</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="c2387-155">public Types varType(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="c2387-155">public Types varType(int variableNumber)</span></span>                    | <span data-ttu-id="c2387-156">Types 列挙の値を使用して変数のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-156">Specifies a variable data type by using values from the Types enumeration.</span></span>                                                                    |
| <span data-ttu-id="c2387-157">public void new(UtilElementType utilType, int Id, str Name)</span><span class="sxs-lookup"><span data-stu-id="c2387-157">public void new(UtilElementType utilType, int Id, str Name)</span></span> | <span data-ttu-id="c2387-158">MethodInfo クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="c2387-158">Creates a new instance of the MethodInfo class.</span></span>                                                                                               |
| <span data-ttu-id="c2387-159">public void setMethod(MemberFunction method)</span><span class="sxs-lookup"><span data-stu-id="c2387-159">public void setMethod(MemberFunction method)</span></span>                | <span data-ttu-id="c2387-160">インスタンスを使用してアプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-160">Specifies the application object type of a node in the Application Object Tree (AOT) by using an instance of the .</span></span>                            |

## <a name="method-accessspecifier"></a><span data-ttu-id="c2387-161">メソッド accessSpecifier</span><span class="sxs-lookup"><span data-stu-id="c2387-161">Method accessSpecifier</span></span>

<span data-ttu-id="c2387-162">メソッドがパブリック、保護、またはプライベートかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-162">Specifies whether the method is public, protected, or private.</span></span>

```xpp
public AccessSpecifier accessSpecifier()
```

### <a name="return-value---accessspecifier"></a><span data-ttu-id="c2387-163">戻り値 - accessSpecifier</span><span class="sxs-lookup"><span data-stu-id="c2387-163">Return Value - accessSpecifier</span></span>

<span data-ttu-id="c2387-164">メソッドがパブリック、保護、またはプライベートのいずれかを指定する AccessSpecifier 列挙型値です。</span><span class="sxs-lookup"><span data-stu-id="c2387-164">An AccessSpecifier enum value that specifies whether the method is public, protected, or private.</span></span>

## <a name="method-compiledok"></a><span data-ttu-id="c2387-165">メソッド compiledOk</span><span class="sxs-lookup"><span data-stu-id="c2387-165">Method compiledOk</span></span>

<span data-ttu-id="c2387-166">メソッドがコンパイルされているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-166">Specifies whether the method has compiled.</span></span>

```xpp
public boolean compiledOk()
```

### <a name="return-value---compiledok"></a><span data-ttu-id="c2387-167">戻り値 - compiledOk</span><span class="sxs-lookup"><span data-stu-id="c2387-167">Return Value - compiledOk</span></span>

<span data-ttu-id="c2387-168">メソッドがコンパイル済みの場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c2387-168">true if the method has compiled; otherwise, false.</span></span>

## <a name="method-displaytableid"></a><span data-ttu-id="c2387-169">メソッド displayTableId</span><span class="sxs-lookup"><span data-stu-id="c2387-169">Method displayTableId</span></span>

```xpp
public TableId displayTableId()
```

### <a name="return-value---displaytableid"></a><span data-ttu-id="c2387-170">戻り値 - displayTableId</span><span class="sxs-lookup"><span data-stu-id="c2387-170">Return Value - displayTableId</span></span>

## <a name="method-displaytype"></a><span data-ttu-id="c2387-171">メソッド displayType</span><span class="sxs-lookup"><span data-stu-id="c2387-171">Method displayType</span></span>

<span data-ttu-id="c2387-172">メソッドの表示機能のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-172">Specifies the display function type of a method.</span></span>

```xpp
public DisplayFunctionType displayType()
```

### <a name="return-value---displaytype"></a><span data-ttu-id="c2387-173">戻り値 - displayType</span><span class="sxs-lookup"><span data-stu-id="c2387-173">Return Value - displayType</span></span>

<span data-ttu-id="c2387-174">メソッドの表示機能のタイプを示す DisplayFunctionType 列挙値。</span><span class="sxs-lookup"><span data-stu-id="c2387-174">A DisplayFunctionType enumeration value that indicates the display function type of a method.</span></span>

### <a name="remarks---displaytype"></a><span data-ttu-id="c2387-175">備考 - displayType</span><span class="sxs-lookup"><span data-stu-id="c2387-175">Remarks - displayType</span></span>

<span data-ttu-id="c2387-176">次のテーブルに、displayType メソッドによって返される可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="c2387-176">The following table lists the possible values returned by the displayType method.</span></span>

|           |                                             |
|-----------|---------------------------------------------|
| <span data-ttu-id="c2387-177">取得</span><span class="sxs-lookup"><span data-stu-id="c2387-177">Get</span></span>       | <span data-ttu-id="c2387-178">このメソッドは表示メソッドです。</span><span class="sxs-lookup"><span data-stu-id="c2387-178">The method is a display method.</span></span>             |
| <span data-ttu-id="c2387-179">None</span><span class="sxs-lookup"><span data-stu-id="c2387-179">None</span></span>      | <span data-ttu-id="c2387-180">このメソッドは、表示メソッドまたは編集メソッドではありません。</span><span class="sxs-lookup"><span data-stu-id="c2387-180">The method is not a display or edit method.</span></span> |
| <span data-ttu-id="c2387-181">RecordGet</span><span class="sxs-lookup"><span data-stu-id="c2387-181">RecordGet</span></span> | <span data-ttu-id="c2387-182">このメソッドは、レコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="c2387-182">The method gets a record.</span></span>                   |
| <span data-ttu-id="c2387-183">RecordSet</span><span class="sxs-lookup"><span data-stu-id="c2387-183">RecordSet</span></span> | <span data-ttu-id="c2387-184">このメソッドは、レコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-184">The method sets a record.</span></span>                   |
| <span data-ttu-id="c2387-185">セット</span><span class="sxs-lookup"><span data-stu-id="c2387-185">Set</span></span>       | <span data-ttu-id="c2387-186">このメソッドは、編集メソッドです。</span><span class="sxs-lookup"><span data-stu-id="c2387-186">The method is an edit method.</span></span>               |

## <a name="method-getallattributes"></a><span data-ttu-id="c2387-187">メソッド getAllAttributes</span><span class="sxs-lookup"><span data-stu-id="c2387-187">Method getAllAttributes</span></span>

<span data-ttu-id="c2387-188">メソッドの属性の完全なセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="c2387-188">Gets the full set of attributes for the method.</span></span>

```xpp
public Array getAllAttributes()
```

### <a name="return-value---getallattributes"></a><span data-ttu-id="c2387-189">戻り値 - getAllAttributes</span><span class="sxs-lookup"><span data-stu-id="c2387-189">Return Value - getAllAttributes</span></span>

<span data-ttu-id="c2387-190">メソッドの SysAttribute オブジェクトの配列。</span><span class="sxs-lookup"><span data-stu-id="c2387-190">The Array of SysAttribute objects for the method.</span></span>

## <a name="method-getattribute"></a><span data-ttu-id="c2387-191">メソッド getAttribute</span><span class="sxs-lookup"><span data-stu-id="c2387-191">Method getAttribute</span></span>

<span data-ttu-id="c2387-192">クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="c2387-192">Gets the first matching attribute from the class header metadata, creates an instance of the Object class that represents it, and returns it.</span></span>

```xpp
public Object getAttribute(str attribute)
```

### <a name="parameters---getattribute"></a><span data-ttu-id="c2387-193">パラメーター - getAttribute</span><span class="sxs-lookup"><span data-stu-id="c2387-193">Parameters - getAttribute</span></span>

<span data-ttu-id="c2387-194">属性</span><span class="sxs-lookup"><span data-stu-id="c2387-194">attribute</span></span>  
<span data-ttu-id="c2387-195">検索の対象である属性。</span><span class="sxs-lookup"><span data-stu-id="c2387-195">The attribute for which to search.</span></span>

### <a name="return-value---getattribute"></a><span data-ttu-id="c2387-196">戻り値 - getAttribute</span><span class="sxs-lookup"><span data-stu-id="c2387-196">Return Value - getAttribute</span></span>

<span data-ttu-id="c2387-197">オブジェクト クラスのインスタンスとしての属性。</span><span class="sxs-lookup"><span data-stu-id="c2387-197">The attribute as an instance of the Object class.</span></span>

## <a name="method-getattributes"></a><span data-ttu-id="c2387-198">メソッド getAttributes</span><span class="sxs-lookup"><span data-stu-id="c2387-198">Method getAttributes</span></span>

```xpp
public Array getAttributes(str attribute)
```

### <a name="parameters---getattributes"></a><span data-ttu-id="c2387-199">パラメーター - getAttributes</span><span class="sxs-lookup"><span data-stu-id="c2387-199">Parameters - getAttributes</span></span>

<span data-ttu-id="c2387-200">属性</span><span class="sxs-lookup"><span data-stu-id="c2387-200">attribute</span></span>  

### <a name="return-value---getattributes"></a><span data-ttu-id="c2387-201">戻り値 - getAttributes</span><span class="sxs-lookup"><span data-stu-id="c2387-201">Return Value - getAttributes</span></span>

## <a name="method-isabstract"></a><span data-ttu-id="c2387-202">メソッド isAbstract</span><span class="sxs-lookup"><span data-stu-id="c2387-202">Method isAbstract</span></span>

<span data-ttu-id="c2387-203">メソッドが抽象かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c2387-203">Indicates whether the method is abstract.</span></span>

```xpp
public boolean isAbstract()
```

### <a name="return-value---isabstract"></a><span data-ttu-id="c2387-204">戻り値 - isAbstract</span><span class="sxs-lookup"><span data-stu-id="c2387-204">Return Value - isAbstract</span></span>

<span data-ttu-id="c2387-205">メソッドが抽象である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c2387-205">true if the method is abstract; otherwise, false.</span></span>

### <a name="remarks---isabstract"></a><span data-ttu-id="c2387-206">備考 - isAbstract</span><span class="sxs-lookup"><span data-stu-id="c2387-206">Remarks - isAbstract</span></span>

<span data-ttu-id="c2387-207">抽象メソッドは宣言されていますが、親クラスで実装されていません。</span><span class="sxs-lookup"><span data-stu-id="c2387-207">An abstract method is declared but not implemented in a parent class.</span></span> <span data-ttu-id="c2387-208">詳細については、「メソッド モディファイア」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2387-208">For more information, see Method Modifiers.</span></span>

## <a name="method-isstatic"></a><span data-ttu-id="c2387-209">メソッド isStatic</span><span class="sxs-lookup"><span data-stu-id="c2387-209">Method isStatic</span></span>

<span data-ttu-id="c2387-210">メソッドが静的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-210">Specifies whether the method is static.</span></span>

```xpp
public boolean isStatic()
```

### <a name="return-value---isstatic"></a><span data-ttu-id="c2387-211">戻り値 - isStatic</span><span class="sxs-lookup"><span data-stu-id="c2387-211">Return Value - isStatic</span></span>

<span data-ttu-id="c2387-212">メソッドが静的である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c2387-212">true if the method is static; otherwise, false.</span></span>

### <a name="remarks---isstatic"></a><span data-ttu-id="c2387-213">備考 - isStatic</span><span class="sxs-lookup"><span data-stu-id="c2387-213">Remarks - isStatic</span></span>

<span data-ttu-id="c2387-214">詳細については、「静的メソッド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2387-214">For more information, see Static Methods.</span></span>

## <a name="method-name"></a><span data-ttu-id="c2387-215">メソッド名</span><span class="sxs-lookup"><span data-stu-id="c2387-215">Method name</span></span>

<span data-ttu-id="c2387-216">メソッドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-216">Specifies the name of a method.</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="c2387-217">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="c2387-217">Return Value - name</span></span>

<span data-ttu-id="c2387-218">メソッド名を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="c2387-218">A string that indicates the method name.</span></span>

## <a name="method-noparms"></a><span data-ttu-id="c2387-219">メソッド noParms</span><span class="sxs-lookup"><span data-stu-id="c2387-219">Method noParms</span></span>

<span data-ttu-id="c2387-220">メソッド内のパラメーターの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-220">Specifies the number of parameters in a method.</span></span>

```xpp
public int noParms()
```

### <a name="return-value---noparms"></a><span data-ttu-id="c2387-221">戻り値 - noParms</span><span class="sxs-lookup"><span data-stu-id="c2387-221">Return Value - noParms</span></span>

<span data-ttu-id="c2387-222">メソッド内のパラメータの数を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c2387-222">An integer value that indicates the number of parameters in a method.</span></span>

## <a name="method-novars"></a><span data-ttu-id="c2387-223">メソッド noVars</span><span class="sxs-lookup"><span data-stu-id="c2387-223">Method noVars</span></span>

<span data-ttu-id="c2387-224">メソッド内の変数の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-224">Specifies the number of variables in a method.</span></span>

```xpp
public int noVars()
```

### <a name="return-value---novars"></a><span data-ttu-id="c2387-225">戻り値 - noVars</span><span class="sxs-lookup"><span data-stu-id="c2387-225">Return Value - noVars</span></span>

<span data-ttu-id="c2387-226">メソッド内の変数の数を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c2387-226">An integer value that indicates the number of variables in a method.</span></span>

## <a name="method-parentid"></a><span data-ttu-id="c2387-227">メソッド parentId</span><span class="sxs-lookup"><span data-stu-id="c2387-227">Method parentId</span></span>

<span data-ttu-id="c2387-228">テーブル メソッドのテーブル ID またはクラス メソッドのクラス ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-228">Specifies the table ID for a table method or the class ID for a class method.</span></span>

```xpp
public int parentId()
```

### <a name="return-value---parentid"></a><span data-ttu-id="c2387-229">戻り値 - parentId</span><span class="sxs-lookup"><span data-stu-id="c2387-229">Return Value - parentId</span></span>

<span data-ttu-id="c2387-230">テーブル ID またはクラス ID を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c2387-230">An integer value that indicates a table ID or a class ID.</span></span>

## <a name="method-propertyhelp"></a><span data-ttu-id="c2387-231">メソッド propertyHelp</span><span class="sxs-lookup"><span data-stu-id="c2387-231">Method propertyHelp</span></span>

<span data-ttu-id="c2387-232">メソッドがコントロールに設定または返すヘルプ テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-232">Specifies the Help text that a method sets or returns for a control.</span></span>

```xpp
public str propertyHelp()
```

### <a name="return-value---propertyhelp"></a><span data-ttu-id="c2387-233">戻り値 - propertyHelp</span><span class="sxs-lookup"><span data-stu-id="c2387-233">Return Value - propertyHelp</span></span>

<span data-ttu-id="c2387-234">ヘルプ テキストを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="c2387-234">A string that contains the Help text.</span></span>

## <a name="method-propertymethod"></a><span data-ttu-id="c2387-235">メソッド PropertyMethod</span><span class="sxs-lookup"><span data-stu-id="c2387-235">Method PropertyMethod</span></span>

<span data-ttu-id="c2387-236">メソッドがプロパティ メソッドかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-236">Specifies whether a method is a property method.</span></span>

```xpp
public NoYes PropertyMethod()
```

### <a name="return-value---propertymethod"></a><span data-ttu-id="c2387-237">戻り値 - PropertyMethod</span><span class="sxs-lookup"><span data-stu-id="c2387-237">Return Value - PropertyMethod</span></span>

<span data-ttu-id="c2387-238">メソッドがプロパティ メソッドの場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="c2387-238">1 if the method is a property method; otherwise, 0.</span></span>

### <a name="remarks---propertymethod"></a><span data-ttu-id="c2387-239">備考 - PropertyMethod</span><span class="sxs-lookup"><span data-stu-id="c2387-239">Remarks - PropertyMethod</span></span>

<span data-ttu-id="c2387-240">プロパティ メソッドは、プロパティを設定または返します。</span><span class="sxs-lookup"><span data-stu-id="c2387-240">A property method sets or returns a property.</span></span>

## <a name="method-returnid"></a><span data-ttu-id="c2387-241">メソッド returnId</span><span class="sxs-lookup"><span data-stu-id="c2387-241">Method returnId</span></span>

<span data-ttu-id="c2387-242">値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-242">Specifies the ID for certain return data types, such as extended data types and classes, for a method that returns a value.</span></span>

```xpp
public int returnId()
```

### <a name="return-value---returnid"></a><span data-ttu-id="c2387-243">戻り値 - returnId</span><span class="sxs-lookup"><span data-stu-id="c2387-243">Return Value - returnId</span></span>

<span data-ttu-id="c2387-244">戻り値のデータ型の ID を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c2387-244">An integer value that indicates the ID for the return data type.</span></span>

### <a name="remarks---returnid"></a><span data-ttu-id="c2387-245">備考 - returnId</span><span class="sxs-lookup"><span data-stu-id="c2387-245">Remarks - returnId</span></span>

<span data-ttu-id="c2387-246">データ型に ID がない場合またはメソッドが値を返さない場合、戻り値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="c2387-246">The return value is 0 if the data type does not have an ID or if a method does not return a value.</span></span>

## <a name="method-returntype"></a><span data-ttu-id="c2387-247">メソッド returnType</span><span class="sxs-lookup"><span data-stu-id="c2387-247">Method returnType</span></span>

<span data-ttu-id="c2387-248">メソッドの戻り値の型を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-248">Specifies a method return type.</span></span>

```xpp
public Types returnType()
```

### <a name="return-value---returntype"></a><span data-ttu-id="c2387-249">戻り値 - returnType</span><span class="sxs-lookup"><span data-stu-id="c2387-249">Return Value - returnType</span></span>

<span data-ttu-id="c2387-250">メソッドの戻り値を示すタイプ列挙値。</span><span class="sxs-lookup"><span data-stu-id="c2387-250">A Types enumeration value that indicates a method return type.</span></span>

### <a name="remarks---returntype"></a><span data-ttu-id="c2387-251">備考 - returnType</span><span class="sxs-lookup"><span data-stu-id="c2387-251">Remarks - returnType</span></span>

<span data-ttu-id="c2387-252">表示される値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c2387-252">The following list indicates the possible values.</span></span> <span data-ttu-id="c2387-253">:</span><span class="sxs-lookup"><span data-stu-id="c2387-253">:</span></span>

-   <span data-ttu-id="c2387-254">AnyType</span><span class="sxs-lookup"><span data-stu-id="c2387-254">AnyType</span></span>
-   <span data-ttu-id="c2387-255">BLOB</span><span class="sxs-lookup"><span data-stu-id="c2387-255">BLOB</span></span>
-   <span data-ttu-id="c2387-256">クラス</span><span class="sxs-lookup"><span data-stu-id="c2387-256">Class</span></span>
-   <span data-ttu-id="c2387-257">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c2387-257">Container</span></span>
-   <span data-ttu-id="c2387-258">日</span><span class="sxs-lookup"><span data-stu-id="c2387-258">Date</span></span>
-   <span data-ttu-id="c2387-259">日時</span><span class="sxs-lookup"><span data-stu-id="c2387-259">DateTime</span></span>
-   <span data-ttu-id="c2387-260">列挙</span><span class="sxs-lookup"><span data-stu-id="c2387-260">Enum</span></span>
-   <span data-ttu-id="c2387-261">グリッド</span><span class="sxs-lookup"><span data-stu-id="c2387-261">Grid</span></span>
-   <span data-ttu-id="c2387-262">Int64</span><span class="sxs-lookup"><span data-stu-id="c2387-262">Int64</span></span>
-   <span data-ttu-id="c2387-263">整数</span><span class="sxs-lookup"><span data-stu-id="c2387-263">Integer</span></span>
-   <span data-ttu-id="c2387-264">実数</span><span class="sxs-lookup"><span data-stu-id="c2387-264">Real</span></span>
-   <span data-ttu-id="c2387-265">レコード</span><span class="sxs-lookup"><span data-stu-id="c2387-265">Record</span></span>
-   <span data-ttu-id="c2387-266">RString</span><span class="sxs-lookup"><span data-stu-id="c2387-266">RString</span></span>
-   <span data-ttu-id="c2387-267">文字列</span><span class="sxs-lookup"><span data-stu-id="c2387-267">String</span></span>
-   <span data-ttu-id="c2387-268">UserType</span><span class="sxs-lookup"><span data-stu-id="c2387-268">UserType</span></span>
-   <span data-ttu-id="c2387-269">VarString</span><span class="sxs-lookup"><span data-stu-id="c2387-269">VarString</span></span>
-   <span data-ttu-id="c2387-270">無効</span><span class="sxs-lookup"><span data-stu-id="c2387-270">void</span></span>

## <a name="method-runmode"></a><span data-ttu-id="c2387-271">メソッド runMode</span><span class="sxs-lookup"><span data-stu-id="c2387-271">Method runMode</span></span>

<span data-ttu-id="c2387-272">メソッドが実行される場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-272">Specifies where a method is executed.</span></span>

```xpp
public ClassRunMode runMode()
```

### <a name="return-value---runmode"></a><span data-ttu-id="c2387-273">戻り値 - runMode</span><span class="sxs-lookup"><span data-stu-id="c2387-273">Return Value - runMode</span></span>

<span data-ttu-id="c2387-274">メソッドが実行される場所を示す ClassRunMode 列挙値。</span><span class="sxs-lookup"><span data-stu-id="c2387-274">A ClassRunMode enumeration value that indicates where a method is executed.</span></span>

### <a name="remarks---runmode"></a><span data-ttu-id="c2387-275">備考 - runMode</span><span class="sxs-lookup"><span data-stu-id="c2387-275">Remarks - runMode</span></span>

<span data-ttu-id="c2387-276">表示される値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c2387-276">The following list indicates the possible values.</span></span>

-   <span data-ttu-id="c2387-277">呼び出された</span><span class="sxs-lookup"><span data-stu-id="c2387-277">Called</span></span>
-   <span data-ttu-id="c2387-278">クライアント</span><span class="sxs-lookup"><span data-stu-id="c2387-278">Client</span></span>
-   <span data-ttu-id="c2387-279">ClientorServer</span><span class="sxs-lookup"><span data-stu-id="c2387-279">ClientorServer</span></span>
-   <span data-ttu-id="c2387-280">サーバー</span><span class="sxs-lookup"><span data-stu-id="c2387-280">Server</span></span>

## <a name="method-varid"></a><span data-ttu-id="c2387-281">メソッド varId</span><span class="sxs-lookup"><span data-stu-id="c2387-281">Method varId</span></span>

<span data-ttu-id="c2387-282">変数を含むメソッドについて、拡張データ型や列挙値などの特定の変数のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-282">Specifies the ID for certain variable data types, such as extended data types and enums, for a method that contains variables.</span></span>

```xpp
public int varId(int variableNumber)
```

### <a name="parameters---varid"></a><span data-ttu-id="c2387-283">パラメーター - varId</span><span class="sxs-lookup"><span data-stu-id="c2387-283">Parameters - varId</span></span>

<span data-ttu-id="c2387-284">variableNumber</span><span class="sxs-lookup"><span data-stu-id="c2387-284">variableNumber</span></span>  
<span data-ttu-id="c2387-285">メソッドに一覧表示されている変数の順序に基づいてメソッド変数を指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="c2387-285">An integer value that specifies a method variable based on the order of the variables listed in the method.</span></span>

### <a name="return-value---varid"></a><span data-ttu-id="c2387-286">戻り値 - varid</span><span class="sxs-lookup"><span data-stu-id="c2387-286">Return Value - varId</span></span>

<span data-ttu-id="c2387-287">変数のデータ型 ID を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="c2387-287">An integer value that indicates the variable data type ID.</span></span>

### <a name="remarks---varid"></a><span data-ttu-id="c2387-288">備考 - varid</span><span class="sxs-lookup"><span data-stu-id="c2387-288">Remarks - varId</span></span>

<span data-ttu-id="c2387-289">データ型に ID がない場合またはメソッドに変数がない場合、戻り値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="c2387-289">The return value is 0 if the data type does not have an ID or if a method does not have variables.</span></span>

## <a name="method-varidold"></a><span data-ttu-id="c2387-290">メソッド varIdOld</span><span class="sxs-lookup"><span data-stu-id="c2387-290">Method varIdOld</span></span>

```xpp
public int varIdOld(int variableNumber)
```

### <a name="parameters---varidold"></a><span data-ttu-id="c2387-291">パラメーター - varIdOld</span><span class="sxs-lookup"><span data-stu-id="c2387-291">Parameters - varIdOld</span></span>

<span data-ttu-id="c2387-292">variableNumber</span><span class="sxs-lookup"><span data-stu-id="c2387-292">variableNumber</span></span>  

### <a name="return-value---varidold"></a><span data-ttu-id="c2387-293">戻り値 - varldOld</span><span class="sxs-lookup"><span data-stu-id="c2387-293">Return Value - varIdOld</span></span>

## <a name="method-vartype"></a><span data-ttu-id="c2387-294">メソッド varType</span><span class="sxs-lookup"><span data-stu-id="c2387-294">Method varType</span></span>

<span data-ttu-id="c2387-295">Types 列挙の値を使用して変数のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-295">Specifies a variable data type by using values from the Types enumeration.</span></span>

```xpp
public Types varType(int variableNumber)
```

### <a name="parameters---vartype"></a><span data-ttu-id="c2387-296">パラメーター - varType</span><span class="sxs-lookup"><span data-stu-id="c2387-296">Parameters - varType</span></span>

<span data-ttu-id="c2387-297">variableNumber</span><span class="sxs-lookup"><span data-stu-id="c2387-297">variableNumber</span></span>  
<span data-ttu-id="c2387-298">メソッドに一覧表示されている変数の順序に基づいてメソッド変数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="c2387-298">An integer that specifies a method variable based on the order of the variables listed in the method.</span></span>

### <a name="return-value---vartype"></a><span data-ttu-id="c2387-299">戻り値 - varType</span><span class="sxs-lookup"><span data-stu-id="c2387-299">Return Value - varType</span></span>

<span data-ttu-id="c2387-300">変数のデータ型を示すタイプ列挙値。</span><span class="sxs-lookup"><span data-stu-id="c2387-300">A Types enumeration value that indicates the variable data type.</span></span>

### <a name="remarks---vartype"></a><span data-ttu-id="c2387-301">備考 - varType</span><span class="sxs-lookup"><span data-stu-id="c2387-301">Remarks - varType</span></span>

<span data-ttu-id="c2387-302">以下は使用可能な値です。</span><span class="sxs-lookup"><span data-stu-id="c2387-302">Following are the possible values:</span></span>

-   <span data-ttu-id="c2387-303">AnyType</span><span class="sxs-lookup"><span data-stu-id="c2387-303">AnyType</span></span>
-   <span data-ttu-id="c2387-304">BLOB</span><span class="sxs-lookup"><span data-stu-id="c2387-304">BLOB</span></span>
-   <span data-ttu-id="c2387-305">クラス</span><span class="sxs-lookup"><span data-stu-id="c2387-305">Class</span></span>
-   <span data-ttu-id="c2387-306">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c2387-306">Container</span></span>
-   <span data-ttu-id="c2387-307">日</span><span class="sxs-lookup"><span data-stu-id="c2387-307">Date</span></span>
-   <span data-ttu-id="c2387-308">日時</span><span class="sxs-lookup"><span data-stu-id="c2387-308">DateTime</span></span>
-   <span data-ttu-id="c2387-309">列挙</span><span class="sxs-lookup"><span data-stu-id="c2387-309">Enum</span></span>
-   <span data-ttu-id="c2387-310">グリッド</span><span class="sxs-lookup"><span data-stu-id="c2387-310">Grid</span></span>
-   <span data-ttu-id="c2387-311">Int64</span><span class="sxs-lookup"><span data-stu-id="c2387-311">Int64</span></span>
-   <span data-ttu-id="c2387-312">整数</span><span class="sxs-lookup"><span data-stu-id="c2387-312">Integer</span></span>
-   <span data-ttu-id="c2387-313">実数</span><span class="sxs-lookup"><span data-stu-id="c2387-313">Real</span></span>
-   <span data-ttu-id="c2387-314">レコード</span><span class="sxs-lookup"><span data-stu-id="c2387-314">Record</span></span>
-   <span data-ttu-id="c2387-315">RString</span><span class="sxs-lookup"><span data-stu-id="c2387-315">RString</span></span>
-   <span data-ttu-id="c2387-316">文字列</span><span class="sxs-lookup"><span data-stu-id="c2387-316">String</span></span>
-   <span data-ttu-id="c2387-317">UserType</span><span class="sxs-lookup"><span data-stu-id="c2387-317">UserType</span></span>
-   <span data-ttu-id="c2387-318">VarString</span><span class="sxs-lookup"><span data-stu-id="c2387-318">VarString</span></span>
-   <span data-ttu-id="c2387-319">無効</span><span class="sxs-lookup"><span data-stu-id="c2387-319">void</span></span>

## <a name="method-new"></a><span data-ttu-id="c2387-320">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c2387-320">Method new</span></span>

<span data-ttu-id="c2387-321">MethodInfo クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="c2387-321">Creates a new instance of the MethodInfo class.</span></span>

```xpp
public void new(UtilElementType utilType, int Id, str Name)
```

### <a name="parameters---new"></a><span data-ttu-id="c2387-322">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="c2387-322">Parameters - new</span></span>

<span data-ttu-id="c2387-323">utilType</span><span class="sxs-lookup"><span data-stu-id="c2387-323">utilType</span></span>  
<span data-ttu-id="c2387-324">要素の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="c2387-324">A string that specifies the name of the element.</span></span>

<!-- -->

<span data-ttu-id="c2387-325">ID</span><span class="sxs-lookup"><span data-stu-id="c2387-325">Id</span></span>  
<span data-ttu-id="c2387-326">要素の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="c2387-326">A string that specifies the name of the element.</span></span>

<!-- -->

<span data-ttu-id="c2387-327">氏名</span><span class="sxs-lookup"><span data-stu-id="c2387-327">Name</span></span>  
<span data-ttu-id="c2387-328">要素の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="c2387-328">A string that specifies the name of the element.</span></span>

## <a name="method-setmethod"></a><span data-ttu-id="c2387-329">メソッド setMethod</span><span class="sxs-lookup"><span data-stu-id="c2387-329">Method setMethod</span></span>

<span data-ttu-id="c2387-330">アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2387-330">Specifies the application object type of a node in the Application Object Tree (AOT).</span></span>

```xpp
public void setMethod(MemberFunction method)
```

### <a name="parameters---setmethod"></a><span data-ttu-id="c2387-331">パラメーター - setMethod</span><span class="sxs-lookup"><span data-stu-id="c2387-331">Parameters - setMethod</span></span>

<span data-ttu-id="c2387-332">メソッド</span><span class="sxs-lookup"><span data-stu-id="c2387-332">method</span></span>  
<span data-ttu-id="c2387-333">AOT 内のノードを表す MemberFunction クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="c2387-333">An instance of the MemberFunction class that represents a node in the AOT.</span></span>

