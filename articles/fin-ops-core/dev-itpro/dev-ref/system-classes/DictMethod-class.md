---
title: DictMethod クラス
description: このトピックでは､DictMethod クラスについて説明します。
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
ms.openlocfilehash: 51fee7fa2fd68550cf37e60d63f722954ad04a5d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502984"
---
# <a name="class-dictmethod"></a><span data-ttu-id="3335c-103">クラス DictMethod</span><span class="sxs-lookup"><span data-stu-id="3335c-103">Class DictMethod</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictMethod extends MethodInfo
```

## <a name="remarks"></a><span data-ttu-id="3335c-104">備考</span><span class="sxs-lookup"><span data-stu-id="3335c-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3335c-105">例</span><span class="sxs-lookup"><span data-stu-id="3335c-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3335c-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3335c-106">Methods</span></span>

| <span data-ttu-id="3335c-107">方法</span><span class="sxs-lookup"><span data-stu-id="3335c-107">Method</span></span>                                                      | <span data-ttu-id="3335c-108">説明</span><span class="sxs-lookup"><span data-stu-id="3335c-108">Description</span></span>                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3335c-109">public AccessSpecifier accessSpecifier()</span><span class="sxs-lookup"><span data-stu-id="3335c-109">public AccessSpecifier accessSpecifier()</span></span>                    | <span data-ttu-id="3335c-110">メソッドがパブリック、保護、またはプライベートかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-110">Specifies whether the method is public, protected, or private.</span></span>                                                                                               |
| <span data-ttu-id="3335c-111">public str clrParameterType(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="3335c-111">public str clrParameterType(int variableNumber)</span></span>             |                                                                                                                                                              |
| <span data-ttu-id="3335c-112">public str clrReturnType()</span><span class="sxs-lookup"><span data-stu-id="3335c-112">public str clrReturnType()</span></span>                                  |                                                                                                                                                              |
| <span data-ttu-id="3335c-113">public str clrVarType(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="3335c-113">public str clrVarType(int variableNumber)</span></span>                   |                                                                                                                                                              |
| <span data-ttu-id="3335c-114">public boolean compiledOk()</span><span class="sxs-lookup"><span data-stu-id="3335c-114">public boolean compiledOk()</span></span>                                 | <span data-ttu-id="3335c-115">メソッドが正常にコンパイルしたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-115">Indicates whether the method compiled successfully.</span></span>                                                                                                          |
| <span data-ttu-id="3335c-116">public TableId displayId()</span><span class="sxs-lookup"><span data-stu-id="3335c-116">public TableId displayId()</span></span>                                  |                                                                                                                                                              |
| <span data-ttu-id="3335c-117">public DisplayFunctionType displayType()</span><span class="sxs-lookup"><span data-stu-id="3335c-117">public DisplayFunctionType displayType()</span></span>                    | <span data-ttu-id="3335c-118">メソッドの表示機能のタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-118">Indicates the type of display function of a method.</span></span>                                                                                                          |
| <span data-ttu-id="3335c-119">public boolean hasImplementation()</span><span class="sxs-lookup"><span data-stu-id="3335c-119">public boolean hasImplementation()</span></span>                          | <span data-ttu-id="3335c-120">実際のメソッドの実装がクラスにあるのか、基本クラスから派生したのかを判断します。</span><span class="sxs-lookup"><span data-stu-id="3335c-120">Determines whether the actual method implementation is on the class or derived from the base class.</span></span>                                                          |
| <span data-ttu-id="3335c-121">public boolean isAbstract()</span><span class="sxs-lookup"><span data-stu-id="3335c-121">public boolean isAbstract()</span></span>                                 | <span data-ttu-id="3335c-122">メソッドが抽象かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-122">Indicates whether the method is abstract.</span></span>                                                                                                                    |
| <span data-ttu-id="3335c-123">public boolean isDelegate()</span><span class="sxs-lookup"><span data-stu-id="3335c-123">public boolean isDelegate()</span></span>                                 | <span data-ttu-id="3335c-124">メソッドがデリゲートかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-124">Indicates whether the method is a delegate.</span></span>                                                                                                                  |
| <span data-ttu-id="3335c-125">public boolean isStatic()</span><span class="sxs-lookup"><span data-stu-id="3335c-125">public boolean isStatic()</span></span>                                   | <span data-ttu-id="3335c-126">メソッドが静的かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-126">Indicates whether the method is static.</span></span>                                                                                                                      |
| <span data-ttu-id="3335c-127">public str name()</span><span class="sxs-lookup"><span data-stu-id="3335c-127">public str name()</span></span>                                           | <span data-ttu-id="3335c-128">メソッドの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-128">Gets the name of the method.</span></span>                                                                                                                                 |
| <span data-ttu-id="3335c-129">public int parameterCnt()</span><span class="sxs-lookup"><span data-stu-id="3335c-129">public int parameterCnt()</span></span>                                   | <span data-ttu-id="3335c-130">メソッドのパラメーター数を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-130">Gets the number of parameters for the method.</span></span>                                                                                                                |
| <span data-ttu-id="3335c-131">public int parameterId(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="3335c-131">public int parameterId(int variableNumber)</span></span>                  | <span data-ttu-id="3335c-132">指定されたパラメータの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-132">Gets the ID of the specified parameter.</span></span>                                                                                                                      |
| <span data-ttu-id="3335c-133">public str parameterName(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="3335c-133">public str parameterName(int variableNumber)</span></span>                | <span data-ttu-id="3335c-134">指定されたパラメータの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-134">Gets the name of the specified parameter.</span></span>                                                                                                                    |
| <span data-ttu-id="3335c-135">public boolean parameterOptional(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="3335c-135">public boolean parameterOptional(int variableNumber)</span></span>        | <span data-ttu-id="3335c-136">メソッドの指定されたパラメーターが省略可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-136">Indicates whether the specified parameter of the method is optional.</span></span>                                                                                         |
| <span data-ttu-id="3335c-137">public Types parameterType(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="3335c-137">public Types parameterType(int variableNumber)</span></span>              |                                                                                                                                                              |
| <span data-ttu-id="3335c-138">public int parentId()</span><span class="sxs-lookup"><span data-stu-id="3335c-138">public int parentId()</span></span>                                       | <span data-ttu-id="3335c-139">メソッドを所有する親の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-139">Gets the ID of the parent that owns the method.</span></span>                                                                                                              |
| <span data-ttu-id="3335c-140">public str propertyHelp()</span><span class="sxs-lookup"><span data-stu-id="3335c-140">public str propertyHelp()</span></span>                                   | <span data-ttu-id="3335c-141">メソッドに関連付けられているプロパティのヘルプ文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-141">Gets the Help string for the property that is associated with the method.</span></span>                                                                                    |
| <span data-ttu-id="3335c-142">public NoYes propertyMethod()</span><span class="sxs-lookup"><span data-stu-id="3335c-142">public NoYes propertyMethod()</span></span>                               | <span data-ttu-id="3335c-143">メソッドがプロパティ メソッドかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-143">Indicates whether the method is a property method.</span></span>                                                                                                           |
| <span data-ttu-id="3335c-144">public int returnId()</span><span class="sxs-lookup"><span data-stu-id="3335c-144">public int returnId()</span></span>                                       | <span data-ttu-id="3335c-145">値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-145">Specifies the ID for certain return data types, such as extended data types and classes, for a method that returns a value.</span></span>                                  |
| <span data-ttu-id="3335c-146">public Types returnType()</span><span class="sxs-lookup"><span data-stu-id="3335c-146">public Types returnType()</span></span>                                   | <span data-ttu-id="3335c-147">メソッドの戻り値の型を指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-147">Specifies a method return type.</span></span>                                                                                                                              |
| <span data-ttu-id="3335c-148">public ClassRunMode runMode()</span><span class="sxs-lookup"><span data-stu-id="3335c-148">public ClassRunMode runMode()</span></span>                               | <span data-ttu-id="3335c-149">メソッドが実行される場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-149">Specifies where a method is run.</span></span>                                                                                                                             |
| <span data-ttu-id="3335c-150">public int varCnt()</span><span class="sxs-lookup"><span data-stu-id="3335c-150">public int varCnt()</span></span>                                         | <span data-ttu-id="3335c-151">メソッドの変数の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-151">Gets the number of variables for the method.</span></span>                                                                                                                 |
| <span data-ttu-id="3335c-152">public str varName(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="3335c-152">public str varName(int variableNumber)</span></span>                      | <span data-ttu-id="3335c-153">指定された変数の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-153">Gets the name of the specified variable.</span></span>                                                                                                                     |
| <span data-ttu-id="3335c-154">public void setMethod(MemberFunction method)</span><span class="sxs-lookup"><span data-stu-id="3335c-154">public void setMethod(MemberFunction method)</span></span>                | <span data-ttu-id="3335c-155">MemberFunction クラスのインスタンスを使用して、アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-155">Specifies the application object type of a node in the Application Object Tree (AOT) by using an instance of the MemberFunction class.</span></span> |
| <span data-ttu-id="3335c-156">public void new(UtilElementType utilType, int id, str name)</span><span class="sxs-lookup"><span data-stu-id="3335c-156">public void new(UtilElementType utilType, int id, str name)</span></span> | <span data-ttu-id="3335c-157">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3335c-157">Initializes a new instance of the Object class.</span></span>                                                                                                              |

## <a name="method-accessspecifier"></a><span data-ttu-id="3335c-158">メソッド accessSpecifier</span><span class="sxs-lookup"><span data-stu-id="3335c-158">Method accessSpecifier</span></span>

<span data-ttu-id="3335c-159">メソッドがパブリック、保護、またはプライベートかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-159">Specifies whether the method is public, protected, or private.</span></span>

```xpp
public AccessSpecifier accessSpecifier()
```

### <a name="return-value---accessspecifier"></a><span data-ttu-id="3335c-160">戻り値 - accessSpecifier</span><span class="sxs-lookup"><span data-stu-id="3335c-160">Return Value - accessSpecifier</span></span>

<span data-ttu-id="3335c-161">メソッドがパブリック、保護、またはプライベートのいずれかを指定する AccessSpecifier 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="3335c-161">An AccessSpecifier enumeration value that specifies whether the method is public, protected, or private.</span></span>

## <a name="method-clrparametertype"></a><span data-ttu-id="3335c-162">メソッド clrParameterType</span><span class="sxs-lookup"><span data-stu-id="3335c-162">Method clrParameterType</span></span>

```xpp
public str clrParameterType(int variableNumber)
```

### <a name="parameters---clrparametertype"></a><span data-ttu-id="3335c-163">パラメーター - clrParameterType</span><span class="sxs-lookup"><span data-stu-id="3335c-163">Parameters - clrParameterType</span></span>

<span data-ttu-id="3335c-164">variableNumber</span><span class="sxs-lookup"><span data-stu-id="3335c-164">variableNumber</span></span>  

### <a name="return-value---clrparametertype"></a><span data-ttu-id="3335c-165">戻り値 - clrParameterType</span><span class="sxs-lookup"><span data-stu-id="3335c-165">Return Value - clrParameterType</span></span>

## <a name="method-clrreturntype"></a><span data-ttu-id="3335c-166">メソッド clrReturnType</span><span class="sxs-lookup"><span data-stu-id="3335c-166">Method clrReturnType</span></span>

```xpp
public str clrReturnType()
```

### <a name="return-value---clrreturntype"></a><span data-ttu-id="3335c-167">戻り値 - clrReturnType</span><span class="sxs-lookup"><span data-stu-id="3335c-167">Return Value - clrReturnType</span></span>

## <a name="method-clrvartype"></a><span data-ttu-id="3335c-168">メソッド clrVarType</span><span class="sxs-lookup"><span data-stu-id="3335c-168">Method clrVarType</span></span>

```xpp
public str clrVarType(int variableNumber)
```

### <a name="parameters---clrvartype"></a><span data-ttu-id="3335c-169">パラメーター - clrVarType</span><span class="sxs-lookup"><span data-stu-id="3335c-169">Parameters - clrVarType</span></span>

<span data-ttu-id="3335c-170">variableNumber</span><span class="sxs-lookup"><span data-stu-id="3335c-170">variableNumber</span></span>  

### <a name="return-value---clrvartype"></a><span data-ttu-id="3335c-171">戻り値 - clrVarType</span><span class="sxs-lookup"><span data-stu-id="3335c-171">Return Value - clrVarType</span></span>

## <a name="method-compiledok"></a><span data-ttu-id="3335c-172">メソッド compiledOk</span><span class="sxs-lookup"><span data-stu-id="3335c-172">Method compiledOk</span></span>

<span data-ttu-id="3335c-173">メソッドが正常にコンパイルしたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-173">Indicates whether the method compiled successfully.</span></span>

```xpp
public boolean compiledOk()
```

### <a name="return-value---compiledok"></a><span data-ttu-id="3335c-174">戻り値 - compiledOk</span><span class="sxs-lookup"><span data-stu-id="3335c-174">Return Value - compiledOk</span></span>

<span data-ttu-id="3335c-175">メソッドが正常にコンパイルされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3335c-175">true if the method compiled successfully; otherwise, false.</span></span>

## <a name="method-displayid"></a><span data-ttu-id="3335c-176">メソッド displayId</span><span class="sxs-lookup"><span data-stu-id="3335c-176">Method displayId</span></span>

```xpp
public TableId displayId()
```

### <a name="return-value---displayid"></a><span data-ttu-id="3335c-177">戻り値 - displayId</span><span class="sxs-lookup"><span data-stu-id="3335c-177">Return Value - displayId</span></span>

## <a name="method-displaytype"></a><span data-ttu-id="3335c-178">メソッド displayType</span><span class="sxs-lookup"><span data-stu-id="3335c-178">Method displayType</span></span>

<span data-ttu-id="3335c-179">メソッドの表示機能のタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-179">Indicates the type of display function of a method.</span></span>

```xpp
public DisplayFunctionType displayType()
```

### <a name="return-value---displaytype"></a><span data-ttu-id="3335c-180">戻り値 - displayType</span><span class="sxs-lookup"><span data-stu-id="3335c-180">Return Value - displayType</span></span>

<span data-ttu-id="3335c-181">メソッドの表示機能のタイプを示す DisplayFunctionType 列挙値。</span><span class="sxs-lookup"><span data-stu-id="3335c-181">A DisplayFunctionType enumeration value that indicates the display function type of a method.</span></span>

### <a name="remarks---displaytype"></a><span data-ttu-id="3335c-182">備考 - displayType</span><span class="sxs-lookup"><span data-stu-id="3335c-182">Remarks - displayType</span></span>

<span data-ttu-id="3335c-183">次のテーブルに、displayType メソッドによって返される可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-183">The following table lists the possible values that are returned by the displayType method.</span></span>

|           |                                             |
|-----------|---------------------------------------------|
| <span data-ttu-id="3335c-184">取得</span><span class="sxs-lookup"><span data-stu-id="3335c-184">Get</span></span>       | <span data-ttu-id="3335c-185">このメソッドは表示メソッドです。</span><span class="sxs-lookup"><span data-stu-id="3335c-185">The method is a display method.</span></span>             |
| <span data-ttu-id="3335c-186">None</span><span class="sxs-lookup"><span data-stu-id="3335c-186">None</span></span>      | <span data-ttu-id="3335c-187">このメソッドは、表示メソッドまたは編集メソッドではありません。</span><span class="sxs-lookup"><span data-stu-id="3335c-187">The method is not a display or edit method.</span></span> |
| <span data-ttu-id="3335c-188">RecordGet</span><span class="sxs-lookup"><span data-stu-id="3335c-188">RecordGet</span></span> | <span data-ttu-id="3335c-189">このメソッドは、レコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-189">The method retrieves a record.</span></span>              |
| <span data-ttu-id="3335c-190">RecordSet</span><span class="sxs-lookup"><span data-stu-id="3335c-190">RecordSet</span></span> | <span data-ttu-id="3335c-191">このメソッドは、レコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-191">The method sets a record.</span></span>                   |
| <span data-ttu-id="3335c-192">セット</span><span class="sxs-lookup"><span data-stu-id="3335c-192">Set</span></span>       | <span data-ttu-id="3335c-193">このメソッドは、編集メソッドです。</span><span class="sxs-lookup"><span data-stu-id="3335c-193">The method is an edit method.</span></span>               |

## <a name="method-hasimplementation"></a><span data-ttu-id="3335c-194">メソッド hasImplementation</span><span class="sxs-lookup"><span data-stu-id="3335c-194">Method hasImplementation</span></span>

<span data-ttu-id="3335c-195">実際のメソッドの実装がクラスにあるのか、基本クラスから派生したのかを判断します。</span><span class="sxs-lookup"><span data-stu-id="3335c-195">Determines whether the actual method implementation is on the class or derived from the base class.</span></span>

```xpp
public boolean hasImplementation()
```

### <a name="return-value---hasimplementation"></a><span data-ttu-id="3335c-196">戻り値 - hasImplementation</span><span class="sxs-lookup"><span data-stu-id="3335c-196">Return Value - hasImplementation</span></span>

<span data-ttu-id="3335c-197">メソッドがクラス上に実装される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3335c-197">true if the method is implemented on the class; otherwise, false.</span></span>

## <a name="method-isabstract"></a><span data-ttu-id="3335c-198">メソッド isAbstract</span><span class="sxs-lookup"><span data-stu-id="3335c-198">Method isAbstract</span></span>

<span data-ttu-id="3335c-199">メソッドが抽象かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-199">Indicates whether the method is abstract.</span></span>

```xpp
public boolean isAbstract()
```

### <a name="return-value---isabstract"></a><span data-ttu-id="3335c-200">戻り値 - isAbstract</span><span class="sxs-lookup"><span data-stu-id="3335c-200">Return Value - isAbstract</span></span>

<span data-ttu-id="3335c-201">メソッドが抽象である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3335c-201">true if the method is abstract; otherwise, false.</span></span>

## <a name="method-isdelegate"></a><span data-ttu-id="3335c-202">メソッド isDelegate</span><span class="sxs-lookup"><span data-stu-id="3335c-202">Method isDelegate</span></span>

<span data-ttu-id="3335c-203">メソッドがデリゲートかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-203">Indicates whether the method is a delegate.</span></span>

```xpp
public boolean isDelegate()
```

### <a name="return-value---isdelegate"></a><span data-ttu-id="3335c-204">戻り値 - isDelegate</span><span class="sxs-lookup"><span data-stu-id="3335c-204">Return Value - isDelegate</span></span>

<span data-ttu-id="3335c-205">メソッドがデリゲートされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3335c-205">true if the method is a delegate; otherwise, false.</span></span>

## <a name="method-isstatic"></a><span data-ttu-id="3335c-206">メソッド isStatic</span><span class="sxs-lookup"><span data-stu-id="3335c-206">Method isStatic</span></span>

<span data-ttu-id="3335c-207">メソッドが静的かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-207">Indicates whether the method is static.</span></span>

```xpp
public boolean isStatic()
```

### <a name="return-value---isstatic"></a><span data-ttu-id="3335c-208">戻り値 - isStatic</span><span class="sxs-lookup"><span data-stu-id="3335c-208">Return Value - isStatic</span></span>

<span data-ttu-id="3335c-209">メソッドが静的である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3335c-209">true if the method is a static; otherwise, false.</span></span>

## <a name="method-name"></a><span data-ttu-id="3335c-210">メソッド名</span><span class="sxs-lookup"><span data-stu-id="3335c-210">Method name</span></span>

<span data-ttu-id="3335c-211">メソッドの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-211">Gets the name of the method.</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="3335c-212">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="3335c-212">Return Value - name</span></span>

<span data-ttu-id="3335c-213">メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="3335c-213">The name of the method.</span></span>

## <a name="method-parametercnt"></a><span data-ttu-id="3335c-214">メソッド parameterCnt</span><span class="sxs-lookup"><span data-stu-id="3335c-214">Method parameterCnt</span></span>

<span data-ttu-id="3335c-215">メソッドのパラメーター数を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-215">Gets the number of parameters for the method.</span></span>

```xpp
public int parameterCnt()
```

### <a name="return-value---parametercnt"></a><span data-ttu-id="3335c-216">戻り値 - parameterCnt</span><span class="sxs-lookup"><span data-stu-id="3335c-216">Return Value - parameterCnt</span></span>

<span data-ttu-id="3335c-217">メソッドのパラメーター数を取得。</span><span class="sxs-lookup"><span data-stu-id="3335c-217">The number of parameters for the method.</span></span>

## <a name="method-parameterid"></a><span data-ttu-id="3335c-218">メソッド parameterId</span><span class="sxs-lookup"><span data-stu-id="3335c-218">Method parameterId</span></span>

<span data-ttu-id="3335c-219">指定されたパラメータの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-219">Gets the ID of the specified parameter.</span></span>

```xpp
public int parameterId(int variableNumber)
```

### <a name="parameters---parameterid"></a><span data-ttu-id="3335c-220">パラメーター - parameterId</span><span class="sxs-lookup"><span data-stu-id="3335c-220">Parameters - parameterId</span></span>

<span data-ttu-id="3335c-221">variableNumber</span><span class="sxs-lookup"><span data-stu-id="3335c-221">variableNumber</span></span>  
<span data-ttu-id="3335c-222">メソッドのパラメーター リストへの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="3335c-222">The one-based index to the parameter list for the method.</span></span>

### <a name="return-value---parameterid"></a><span data-ttu-id="3335c-223">戻り値 - parameterId</span><span class="sxs-lookup"><span data-stu-id="3335c-223">Return Value - parameterId</span></span>

<span data-ttu-id="3335c-224">指定されたパラメーターの ID。</span><span class="sxs-lookup"><span data-stu-id="3335c-224">The ID of the specified parameter.</span></span>

## <a name="method-parametername"></a><span data-ttu-id="3335c-225">メソッド parameterName</span><span class="sxs-lookup"><span data-stu-id="3335c-225">Method parameterName</span></span>

<span data-ttu-id="3335c-226">指定されたパラメータの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-226">Gets the name of the specified parameter.</span></span>

```xpp
public str parameterName(int variableNumber)
```

### <a name="parameters---parametername"></a><span data-ttu-id="3335c-227">パラメーター - parameterName</span><span class="sxs-lookup"><span data-stu-id="3335c-227">Parameters - parameterName</span></span>

<span data-ttu-id="3335c-228">variableNumber</span><span class="sxs-lookup"><span data-stu-id="3335c-228">variableNumber</span></span>  
<span data-ttu-id="3335c-229">メソッドのパラメーター リストへの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="3335c-229">The one-based index to the parameter list for the method.</span></span>

### <a name="return-value---parametername"></a><span data-ttu-id="3335c-230">戻り値 - parameterName</span><span class="sxs-lookup"><span data-stu-id="3335c-230">Return Value - parameterName</span></span>

<span data-ttu-id="3335c-231">指定されたパラメーターの名前。</span><span class="sxs-lookup"><span data-stu-id="3335c-231">The name of the specified parameter.</span></span>

## <a name="method-parameteroptional"></a><span data-ttu-id="3335c-232">メソッド parameterOptional</span><span class="sxs-lookup"><span data-stu-id="3335c-232">Method parameterOptional</span></span>

<span data-ttu-id="3335c-233">メソッドの指定されたパラメーターが省略可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-233">Indicates whether the specified parameter of the method is optional.</span></span>

```xpp
public boolean parameterOptional(int variableNumber)
```

### <a name="parameters---parameteroptional"></a><span data-ttu-id="3335c-234">パラメーター - parameterOptional</span><span class="sxs-lookup"><span data-stu-id="3335c-234">Parameters - parameterOptional</span></span>

<span data-ttu-id="3335c-235">variableNumber</span><span class="sxs-lookup"><span data-stu-id="3335c-235">variableNumber</span></span>  
<span data-ttu-id="3335c-236">メソッドのパラメーター リストへの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="3335c-236">The one-based index to the parameter list for the method.</span></span>

### <a name="return-value---parameteroptional"></a><span data-ttu-id="3335c-237">戻り値 - parameterOptional</span><span class="sxs-lookup"><span data-stu-id="3335c-237">Return Value - parameterOptional</span></span>

<span data-ttu-id="3335c-238">パラメーターがオプションである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3335c-238">true if the parameter is optional; otherwise, false.</span></span>

## <a name="method-parametertype"></a><span data-ttu-id="3335c-239">メソッド parameterType</span><span class="sxs-lookup"><span data-stu-id="3335c-239">Method parameterType</span></span>

```xpp
public Types parameterType(int variableNumber)
```

### <a name="parameters---parametertype"></a><span data-ttu-id="3335c-240">パラメーター - parameterType</span><span class="sxs-lookup"><span data-stu-id="3335c-240">Parameters - parameterType</span></span>

<span data-ttu-id="3335c-241">variableNumber</span><span class="sxs-lookup"><span data-stu-id="3335c-241">variableNumber</span></span>  

### <a name="return-value---parametertype"></a><span data-ttu-id="3335c-242">戻り値 - parameterType</span><span class="sxs-lookup"><span data-stu-id="3335c-242">Return Value - parameterType</span></span>

## <a name="method-parentid"></a><span data-ttu-id="3335c-243">メソッド parentId</span><span class="sxs-lookup"><span data-stu-id="3335c-243">Method parentId</span></span>

<span data-ttu-id="3335c-244">メソッドを所有する親の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-244">Gets the ID of the parent that owns the method.</span></span>

```xpp
public int parentId()
```

### <a name="return-value---parentid"></a><span data-ttu-id="3335c-245">戻り値 - parentId</span><span class="sxs-lookup"><span data-stu-id="3335c-245">Return Value - parentId</span></span>

<span data-ttu-id="3335c-246">メソッドを所有する親の ID。</span><span class="sxs-lookup"><span data-stu-id="3335c-246">The ID of the parent that owns the method.</span></span>

## <a name="method-propertyhelp"></a><span data-ttu-id="3335c-247">メソッド propertyHelp</span><span class="sxs-lookup"><span data-stu-id="3335c-247">Method propertyHelp</span></span>

<span data-ttu-id="3335c-248">メソッドに関連付けられているプロパティのヘルプ文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-248">Gets the Help string for the property that is associated with the method.</span></span>

```xpp
public str propertyHelp()
```

### <a name="return-value---propertyhelp"></a><span data-ttu-id="3335c-249">戻り値 - propertyHelp</span><span class="sxs-lookup"><span data-stu-id="3335c-249">Return Value - propertyHelp</span></span>

<span data-ttu-id="3335c-250">メソッドに関連付けられているプロパティのヘルプ文字列。ヘルプ文字列がない場合は、空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3335c-250">The Help string for the property that is associated with the method; an empty string if there is no Help string.</span></span>

### <a name="remarks---propertyhelp"></a><span data-ttu-id="3335c-251">備考 - propertyHelp</span><span class="sxs-lookup"><span data-stu-id="3335c-251">Remarks - propertyHelp</span></span>

<span data-ttu-id="3335c-252">このメソッドは、DictMethod::propertyMethod メソッドを呼び出して、メソッドがプロパティ メソッドかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-252">This method calls the DictMethod::propertyMethod method to determine whether the method is a property method.</span></span>

## <a name="method-propertymethod"></a><span data-ttu-id="3335c-253">メソッド propertyMethod</span><span class="sxs-lookup"><span data-stu-id="3335c-253">Method propertyMethod</span></span>

<span data-ttu-id="3335c-254">メソッドがプロパティ メソッドかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3335c-254">Indicates whether the method is a property method.</span></span>

```xpp
public NoYes propertyMethod()
```

### <a name="return-value---propertymethod"></a><span data-ttu-id="3335c-255">戻り値 - propertyMethod</span><span class="sxs-lookup"><span data-stu-id="3335c-255">Return Value - propertyMethod</span></span>

<span data-ttu-id="3335c-256">メソッドがプロパティ メソッドである場合は NoYes::No 列挙値、それ以外の場合は NoYes::Yes 列挙値。</span><span class="sxs-lookup"><span data-stu-id="3335c-256">A NoYes::No enumeration value if the method is a property method; otherwise, a NoYes::Yes enumeration value.</span></span>

## <a name="method-returnid"></a><span data-ttu-id="3335c-257">メソッド returnId</span><span class="sxs-lookup"><span data-stu-id="3335c-257">Method returnId</span></span>

<span data-ttu-id="3335c-258">値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-258">Specifies the ID for certain return data types, such as extended data types and classes, for a method that returns a value.</span></span>

```xpp
public int returnId()
```

### <a name="return-value---returnid"></a><span data-ttu-id="3335c-259">戻り値 - returnId</span><span class="sxs-lookup"><span data-stu-id="3335c-259">Return Value - returnId</span></span>

<span data-ttu-id="3335c-260">戻り値のデータ型の ID。データ型に ID がない場合またはメソッドが値を返さない場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3335c-260">The ID for the return data type; 0 (zero) if the data type does not have an ID or a method does not return a value..</span></span>

## <a name="method-returntype"></a><span data-ttu-id="3335c-261">メソッド returnType</span><span class="sxs-lookup"><span data-stu-id="3335c-261">Method returnType</span></span>

<span data-ttu-id="3335c-262">メソッドの戻り値の型を指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-262">Specifies a method return type.</span></span>

```xpp
public Types returnType()
```

### <a name="return-value---returntype"></a><span data-ttu-id="3335c-263">戻り値 - returnType</span><span class="sxs-lookup"><span data-stu-id="3335c-263">Return Value - returnType</span></span>

<span data-ttu-id="3335c-264">メソッドの戻り値を示すタイプ列挙値。</span><span class="sxs-lookup"><span data-stu-id="3335c-264">A Types enumeration value that indicates the method return type.</span></span>

### <a name="remarks---returntype"></a><span data-ttu-id="3335c-265">備考 - returnType</span><span class="sxs-lookup"><span data-stu-id="3335c-265">Remarks - returnType</span></span>

<span data-ttu-id="3335c-266">表示される値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3335c-266">The following list shows the possible values:</span></span>

-   <span data-ttu-id="3335c-267">AnyType</span><span class="sxs-lookup"><span data-stu-id="3335c-267">AnyType</span></span>
-   <span data-ttu-id="3335c-268">BLOB</span><span class="sxs-lookup"><span data-stu-id="3335c-268">BLOB</span></span>
-   <span data-ttu-id="3335c-269">クラス</span><span class="sxs-lookup"><span data-stu-id="3335c-269">Class</span></span>
-   <span data-ttu-id="3335c-270">コンテナー</span><span class="sxs-lookup"><span data-stu-id="3335c-270">Container</span></span>
-   <span data-ttu-id="3335c-271">日</span><span class="sxs-lookup"><span data-stu-id="3335c-271">Date</span></span>
-   <span data-ttu-id="3335c-272">日時</span><span class="sxs-lookup"><span data-stu-id="3335c-272">DateTime</span></span>
-   <span data-ttu-id="3335c-273">列挙</span><span class="sxs-lookup"><span data-stu-id="3335c-273">Enum</span></span>
-   <span data-ttu-id="3335c-274">グリッド</span><span class="sxs-lookup"><span data-stu-id="3335c-274">Grid</span></span>
-   <span data-ttu-id="3335c-275">Int64</span><span class="sxs-lookup"><span data-stu-id="3335c-275">Int64</span></span>
-   <span data-ttu-id="3335c-276">整数</span><span class="sxs-lookup"><span data-stu-id="3335c-276">Integer</span></span>
-   <span data-ttu-id="3335c-277">実数</span><span class="sxs-lookup"><span data-stu-id="3335c-277">Real</span></span>
-   <span data-ttu-id="3335c-278">レコード</span><span class="sxs-lookup"><span data-stu-id="3335c-278">Record</span></span>
-   <span data-ttu-id="3335c-279">RString</span><span class="sxs-lookup"><span data-stu-id="3335c-279">RString</span></span>
-   <span data-ttu-id="3335c-280">文字列</span><span class="sxs-lookup"><span data-stu-id="3335c-280">String</span></span>
-   <span data-ttu-id="3335c-281">UserType</span><span class="sxs-lookup"><span data-stu-id="3335c-281">UserType</span></span>
-   <span data-ttu-id="3335c-282">VarString</span><span class="sxs-lookup"><span data-stu-id="3335c-282">VarString</span></span>
-   <span data-ttu-id="3335c-283">無効</span><span class="sxs-lookup"><span data-stu-id="3335c-283">void</span></span>

## <a name="method-runmode"></a><span data-ttu-id="3335c-284">メソッド runMode</span><span class="sxs-lookup"><span data-stu-id="3335c-284">Method runMode</span></span>

<span data-ttu-id="3335c-285">メソッドが実行される場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-285">Specifies where a method is run.</span></span>

```xpp
public ClassRunMode runMode()
```

### <a name="return-value---runmode"></a><span data-ttu-id="3335c-286">戻り値 - runMode</span><span class="sxs-lookup"><span data-stu-id="3335c-286">Return Value - runMode</span></span>

<span data-ttu-id="3335c-287">メソッドが実行される場所を示す ClassRunMode 列挙値。</span><span class="sxs-lookup"><span data-stu-id="3335c-287">A ClassRunMode enumeration value that indicates where a method is run.</span></span>

### <a name="remarks---runmode"></a><span data-ttu-id="3335c-288">備考 - runMode</span><span class="sxs-lookup"><span data-stu-id="3335c-288">Remarks - runMode</span></span>

<span data-ttu-id="3335c-289">表示される値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3335c-289">The following list shows the possible values:</span></span>

-   <span data-ttu-id="3335c-290">呼び出された</span><span class="sxs-lookup"><span data-stu-id="3335c-290">Called</span></span>
-   <span data-ttu-id="3335c-291">クライアント</span><span class="sxs-lookup"><span data-stu-id="3335c-291">Client</span></span>
-   <span data-ttu-id="3335c-292">ClientorServer</span><span class="sxs-lookup"><span data-stu-id="3335c-292">ClientorServer</span></span>
-   <span data-ttu-id="3335c-293">サーバー</span><span class="sxs-lookup"><span data-stu-id="3335c-293">Server</span></span>

## <a name="method-varcnt"></a><span data-ttu-id="3335c-294">メソッド varCnt</span><span class="sxs-lookup"><span data-stu-id="3335c-294">Method varCnt</span></span>

<span data-ttu-id="3335c-295">メソッドの変数の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-295">Gets the number of variables for the method.</span></span>

```xpp
public int varCnt()
```

### <a name="return-value---varcnt"></a><span data-ttu-id="3335c-296">戻り値 - varCnt</span><span class="sxs-lookup"><span data-stu-id="3335c-296">Return Value - varCnt</span></span>

<span data-ttu-id="3335c-297">メソッドのローカル変数と継承変数の数。</span><span class="sxs-lookup"><span data-stu-id="3335c-297">The number of local and inherited variables for the method.</span></span>

## <a name="method-varname"></a><span data-ttu-id="3335c-298">メソッド varName</span><span class="sxs-lookup"><span data-stu-id="3335c-298">Method varName</span></span>

<span data-ttu-id="3335c-299">指定された変数の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="3335c-299">Gets the name of the specified variable.</span></span>

```xpp
public str varName(int variableNumber)
```

### <a name="parameters---varname"></a><span data-ttu-id="3335c-300">パラメーター - varName</span><span class="sxs-lookup"><span data-stu-id="3335c-300">Parameters - varName</span></span>

<span data-ttu-id="3335c-301">variableNumber</span><span class="sxs-lookup"><span data-stu-id="3335c-301">variableNumber</span></span>  
<span data-ttu-id="3335c-302">メソッドの変数リストへの 1 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="3335c-302">The one-based index to the variable list for the method.</span></span>

### <a name="return-value---varname"></a><span data-ttu-id="3335c-303">戻り値 - varName</span><span class="sxs-lookup"><span data-stu-id="3335c-303">Return Value - varName</span></span>

<span data-ttu-id="3335c-304">指定された変数の名前。</span><span class="sxs-lookup"><span data-stu-id="3335c-304">The name of the specified variable.</span></span>

## <a name="method-setmethod"></a><span data-ttu-id="3335c-305">メソッド setMethod</span><span class="sxs-lookup"><span data-stu-id="3335c-305">Method setMethod</span></span>

<span data-ttu-id="3335c-306">MemberFunction クラスのインスタンスを使用して、アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="3335c-306">Specifies the application object type of a node in the Application Object Tree (AOT) by using an instance of the MemberFunction class.</span></span>

```xpp
public void setMethod(MemberFunction method)
```

### <a name="parameters---setmethod"></a><span data-ttu-id="3335c-307">パラメーター - setMethod</span><span class="sxs-lookup"><span data-stu-id="3335c-307">Parameters - setMethod</span></span>

<span data-ttu-id="3335c-308">メソッド</span><span class="sxs-lookup"><span data-stu-id="3335c-308">method</span></span>  
<span data-ttu-id="3335c-309">AOT 内のノードを表す MemberFunction クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="3335c-309">An instance of the MemberFunction class that represents a node in the AOT.</span></span>

## <a name="method-new"></a><span data-ttu-id="3335c-310">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3335c-310">Method new</span></span>

<span data-ttu-id="3335c-311">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3335c-311">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(UtilElementType utilType, int id, str name)
```

### <a name="parameters---new"></a><span data-ttu-id="3335c-312">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="3335c-312">Parameters - new</span></span>

<span data-ttu-id="3335c-313">utilType</span><span class="sxs-lookup"><span data-stu-id="3335c-313">utilType</span></span>  

<!-- -->

<span data-ttu-id="3335c-314">id</span><span class="sxs-lookup"><span data-stu-id="3335c-314">id</span></span>  

<!-- -->

<span data-ttu-id="3335c-315">名前</span><span class="sxs-lookup"><span data-stu-id="3335c-315">name</span></span>  

