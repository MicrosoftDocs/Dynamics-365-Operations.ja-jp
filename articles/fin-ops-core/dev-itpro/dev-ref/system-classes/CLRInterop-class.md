---
title: CLRInterop クラス
description: このトピックでは、CLRInterop クラスについて説明します。
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
ms.openlocfilehash: b7dc64a05508c77e202ef69b63b99d78e694b5d8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502718"
---
# <a name="class-clrinterop"></a><span data-ttu-id="2584e-103">クラス CLRInterop</span><span class="sxs-lookup"><span data-stu-id="2584e-103">Class CLRInterop</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class CLRInterop extends Object
```

<span data-ttu-id="2584e-104">ClrInterop クラスは、タイプ マーシャ リングおよび例外処理の機能を提供するユーティリティ クラスです。</span><span class="sxs-lookup"><span data-stu-id="2584e-104">The ClrInterop class is a utility class that provides functionality for type marshaling and exception handling.</span></span> <span data-ttu-id="2584e-105">すべてのメソッドは静的であるため、クラスのインスタンス化をする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2584e-105">Because all the methods are static, no instantiation of the class is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="2584e-106">備考</span><span class="sxs-lookup"><span data-stu-id="2584e-106">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="2584e-107">例</span><span class="sxs-lookup"><span data-stu-id="2584e-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="2584e-108">方法</span><span class="sxs-lookup"><span data-stu-id="2584e-108">Methods</span></span>

| <span data-ttu-id="2584e-109">方法</span><span class="sxs-lookup"><span data-stu-id="2584e-109">Method</span></span>                                                                               | <span data-ttu-id="2584e-110">説明</span><span class="sxs-lookup"><span data-stu-id="2584e-110">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2584e-111">::public static AnyType getAnyTypeForObject(CLRObject clrObject)</span><span class="sxs-lookup"><span data-stu-id="2584e-111">::public static AnyType getAnyTypeForObject(CLRObject clrObject)</span></span>                     | <span data-ttu-id="2584e-112">共通言語ランタイム (CLR) オブジェクトを X++ anytype データ型の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2584e-112">Converts a common language runtime (CLR) object to a value of the X++ anytype data type.</span></span>                                                 |
| <span data-ttu-id="2584e-113">::public static CLRObject getLastException()</span><span class="sxs-lookup"><span data-stu-id="2584e-113">::public static CLRObject getLastException()</span></span>                                         | <span data-ttu-id="2584e-114">最新の CLR 例外を取得します。</span><span class="sxs-lookup"><span data-stu-id="2584e-114">Retrieves the most recent CLR exception.</span></span>                                                                                                 |
| <span data-ttu-id="2584e-115">::public static CLRObject getObjectForAnyType(AnyType anyType)</span><span class="sxs-lookup"><span data-stu-id="2584e-115">::public static CLRObject getObjectForAnyType(AnyType anyType)</span></span>                       | <span data-ttu-id="2584e-116">X++ anytype データ型の値を CLRObject データ型の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2584e-116">Converts a value of the X++ anytype data type to a value of the CLRObject data type.</span></span>                                                     |
| <span data-ttu-id="2584e-117">::public static CLRObject getType(str clrTypeName)</span><span class="sxs-lookup"><span data-stu-id="2584e-117">::public static CLRObject getType(str clrTypeName)</span></span>                                   |                                                                                                                                          |
| <span data-ttu-id="2584e-118">::public static boolean isNull(CLRObject clrObject)</span><span class="sxs-lookup"><span data-stu-id="2584e-118">::public static boolean isNull(CLRObject clrObject)</span></span>                                  | <span data-ttu-id="2584e-119">指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にセットされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2584e-119">Confirms whether the specified CLRObject instance is set to nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>            |
| <span data-ttu-id="2584e-120">::public static CLRObject Null(str clrTypeName)</span><span class="sxs-lookup"><span data-stu-id="2584e-120">::public static CLRObject Null(str clrTypeName)</span></span>                                      | <span data-ttu-id="2584e-121">nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の値を持つ CLR データ型を返します。</span><span class="sxs-lookup"><span data-stu-id="2584e-121">Returns a CLR data type that has a value of nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>                            |
| <span data-ttu-id="2584e-122">::public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)</span><span class="sxs-lookup"><span data-stu-id="2584e-122">::public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)</span></span>          | <span data-ttu-id="2584e-123">1 つ以上の列挙定数の名前または数値の文字列で表したものを、等価の CLRObject インスタンスに変換します。</span><span class="sxs-lookup"><span data-stu-id="2584e-123">Converts the string representation of the name or numeric value of one or more enumerated constants to an equivalent CLRObject instance.</span></span> |
| <span data-ttu-id="2584e-124">::public static CLRObject staticInvoke(str className, str methodName, VarArg params)</span><span class="sxs-lookup"><span data-stu-id="2584e-124">::public static CLRObject staticInvoke(str className, str methodName, VarArg params)</span></span> | <span data-ttu-id="2584e-125">CLR データ型の静的メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2584e-125">Calls a static method on a CLR data type.</span></span>                                                                                                |
| <span data-ttu-id="2584e-126">::public static void loadAssembly(str clrAssemblyName)</span><span class="sxs-lookup"><span data-stu-id="2584e-126">::public static void loadAssembly(str clrAssemblyName)</span></span>                               |                                                                                                                                          |
| <span data-ttu-id="2584e-127">public void new()</span><span class="sxs-lookup"><span data-stu-id="2584e-127">public void new()</span></span>                                                                    | <span data-ttu-id="2584e-128">CLRInterop クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="2584e-128">Initializes a new instance of the CLRInterop class.</span></span>                                                                                      |

## <a name="method-getanytypeforobject"></a><span data-ttu-id="2584e-129">メソッド getAnyTypeForObject</span><span class="sxs-lookup"><span data-stu-id="2584e-129">Method getAnyTypeForObject</span></span>

<span data-ttu-id="2584e-130">共通言語ランタイム (CLR) オブジェクトを X++ anytype データ型の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2584e-130">Converts a common language runtime (CLR) object to a value of the X++ anytype data type.</span></span>

```xpp
public static AnyType getAnyTypeForObject(CLRObject clrObject)
```

### <a name="parameters---getanytypeforobject"></a><span data-ttu-id="2584e-131">パラメーター - getAnyTypeForObject</span><span class="sxs-lookup"><span data-stu-id="2584e-131">Parameters - getAnyTypeForObject</span></span>

<span data-ttu-id="2584e-132">clrObject</span><span class="sxs-lookup"><span data-stu-id="2584e-132">clrObject</span></span>  
<span data-ttu-id="2584e-133">X++ データ型に変換する CLR オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="2584e-133">The CLR object to convert to an X++ data type.</span></span>

### <a name="return-value---getanytypeforobject"></a><span data-ttu-id="2584e-134">戻り値 - getAnyTypeForObject</span><span class="sxs-lookup"><span data-stu-id="2584e-134">Return Value - getAnyTypeForObject</span></span>

<span data-ttu-id="2584e-135">\_オブジェクトの引数値を持つ X++ anytype データ型です。</span><span class="sxs-lookup"><span data-stu-id="2584e-135">An X++ anytype date type that has the value of the \_object argument.</span></span>

### <a name="remarks---getanytypeforobject"></a><span data-ttu-id="2584e-136">備考 - getAnyTypeForObject</span><span class="sxs-lookup"><span data-stu-id="2584e-136">Remarks - getAnyTypeForObject</span></span>

<span data-ttu-id="2584e-137">攻撃者が getAnyTypeForObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="2584e-137">If an attacker can control input to the getAnyTypeForObject method, a security risk exists.</span></span> <span data-ttu-id="2584e-138">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="2584e-138">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="2584e-139">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="2584e-139">Calls to this method on the server require permission.</span></span> <span data-ttu-id="2584e-140">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2584e-140">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span> <span data-ttu-id="2584e-141">引数 X++ のデータ型に変換することができない場合、Exception::ClrError タイプの例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="2584e-141">If the argument cannot be converted to an X++ data type, an exception of the Exception::ClrError type is thrown.</span></span>

### <a name="examples---getanytypeforobject"></a><span data-ttu-id="2584e-142">例 - getAnyTypeForObject</span><span class="sxs-lookup"><span data-stu-id="2584e-142">Examples - getAnyTypeForObject</span></span>

<span data-ttu-id="2584e-143">次の例では、CLR 文字列の値を X++ str データ型に設定します。</span><span class="sxs-lookup"><span data-stu-id="2584e-143">The following example sets the value of a CLR string to an X++ str data type.</span></span>

```xpp
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
    System.String   clrStr = "Calculate total"; 
    str             s; 
```

```xpp
    perm = new InteropPermission(InteropKind::ClrInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
```

```xpp
    s = ClrInterop::getAnyTypeForObject(clrStr); 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-getlastexception"></a><span data-ttu-id="2584e-144">メソッド getLastException</span><span class="sxs-lookup"><span data-stu-id="2584e-144">Method getLastException</span></span>

<span data-ttu-id="2584e-145">最新の CLR 例外を取得します。</span><span class="sxs-lookup"><span data-stu-id="2584e-145">Retrieves the most recent CLR exception.</span></span>

```xpp
public static CLRObject getLastException()
```

### <a name="return-value---getlastexception"></a><span data-ttu-id="2584e-146">戻り値 - getLastException</span><span class="sxs-lookup"><span data-stu-id="2584e-146">Return Value - getLastException</span></span>

<span data-ttu-id="2584e-147">Exception::ClrError 型の最新の例外。それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="2584e-147">The most recent exception of the Exception::ClrError type; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---getlastexception"></a><span data-ttu-id="2584e-148">備考 - getLastException</span><span class="sxs-lookup"><span data-stu-id="2584e-148">Remarks - getLastException</span></span>

<span data-ttu-id="2584e-149">攻撃者が getLastException メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="2584e-149">If an attacker can control input to the getLastException method, a security risk exists.</span></span> <span data-ttu-id="2584e-150">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="2584e-150">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="2584e-151">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="2584e-151">Calls to this method on the server require permission.</span></span> <span data-ttu-id="2584e-152">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2584e-152">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---getlastexception"></a><span data-ttu-id="2584e-153">例 - getLastException</span><span class="sxs-lookup"><span data-stu-id="2584e-153">Examples - getLastException</span></span>

<span data-ttu-id="2584e-154">次の例では、無効な形式の日付を渡します。</span><span class="sxs-lookup"><span data-stu-id="2584e-154">The following example tries to pass in a date that has an invalid format.</span></span> <span data-ttu-id="2584e-155">スローされた CLR 例外は、X++ 例外に変換された後、情報ログに出力されます。</span><span class="sxs-lookup"><span data-stu-id="2584e-155">The CLR exception that is thrown is converted to an X++ exception and then printed to the Infolog.</span></span> <span data-ttu-id="2584e-156">入れ子になった例外は情報ログにも出力されます。</span><span class="sxs-lookup"><span data-stu-id="2584e-156">Any nested exceptions are also printed to the Infolog.</span></span>

```xpp
static void Job2(Args _args) 
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
```

```xpp
    try 
    { 
        System.DateTime::Parse( "-1/-1/-1"); 
    } 
    catch( Exception::CLRError ) 
    { 
        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 
```

```xpp
        e = ClrInterop::getLastException(); 
```

```xpp
        CodeAccessPermission::revertAssert(); 
```

```xpp
        while( e ) 
        { 
            info( e.get_Message() ); 
            e = e.get_InnerException(); 
        } 
    } 
```

```xpp
}
```

## <a name="method-getobjectforanytype"></a><span data-ttu-id="2584e-157">メソッド getObjectForAnyType</span><span class="sxs-lookup"><span data-stu-id="2584e-157">Method getObjectForAnyType</span></span>

<span data-ttu-id="2584e-158">X++ anytype データ型の値を CLRObject データ型の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2584e-158">Converts a value of the X++ anytype data type to a value of the CLRObject data type.</span></span>

```xpp
public static CLRObject getObjectForAnyType(AnyType anyType)
```

### <a name="parameters---getobjectforanytype"></a><span data-ttu-id="2584e-159">パラメーター - getObjectForAnyType</span><span class="sxs-lookup"><span data-stu-id="2584e-159">Parameters - getObjectForAnyType</span></span>

<span data-ttu-id="2584e-160">anyType</span><span class="sxs-lookup"><span data-stu-id="2584e-160">anyType</span></span>  
<span data-ttu-id="2584e-161">CLRObject データ型の値に変換する X++ 値。</span><span class="sxs-lookup"><span data-stu-id="2584e-161">The X++ value to convert to a value of the CLRObject data type.</span></span>

### <a name="return-value---getobjectforanytype"></a><span data-ttu-id="2584e-162">戻り値 - getObjectForAnyType</span><span class="sxs-lookup"><span data-stu-id="2584e-162">Return Value - getObjectForAnyType</span></span>

<span data-ttu-id="2584e-163">値 \_anytype 引数を持つ CLR オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="2584e-163">The CLR object that has the value of the \_anytype argument.</span></span>

### <a name="remarks---getobjectforanytype"></a><span data-ttu-id="2584e-164">備考 - getObjectForAnyType</span><span class="sxs-lookup"><span data-stu-id="2584e-164">Remarks - getObjectForAnyType</span></span>

<span data-ttu-id="2584e-165">攻撃者が getObjectForAnyType メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="2584e-165">If an attacker can control input to the getObjectForAnyType method, a security risk exists.</span></span> <span data-ttu-id="2584e-166">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="2584e-166">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="2584e-167">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="2584e-167">Calls to this method on the server require permission.</span></span> <span data-ttu-id="2584e-168">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2584e-168">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span> <span data-ttu-id="2584e-169">引数を CLRObject 型に変換することができない場合、Exception::CLRError 型の例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="2584e-169">If the argument cannot be converted to the CLRObject type, an exception of the Exception::CLRError type is thrown.</span></span>

### <a name="examples---getobjectforanytype"></a><span data-ttu-id="2584e-170">例 - getObjectForAnyType</span><span class="sxs-lookup"><span data-stu-id="2584e-170">Examples - getObjectForAnyType</span></span>

<span data-ttu-id="2584e-171">次の例では、文字列値を CLR 文字列オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="2584e-171">The following example converts a string value to a CLR string object.</span></span>

```xpp
static void Job3(Args _args) 
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
    System.String s; 
```

```xpp
    perm = new InteropPermission(InteropKind::ClrInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
```

```xpp
    s = CLRInterop::getObjectForAnyType("Calculate total"); 
```

```xpp
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-gettype"></a><span data-ttu-id="2584e-172">メソッド getType</span><span class="sxs-lookup"><span data-stu-id="2584e-172">Method getType</span></span>

```xpp
public static CLRObject getType(str clrTypeName)
```

### <a name="parameters---gettype"></a><span data-ttu-id="2584e-173">パラメーター - getType</span><span class="sxs-lookup"><span data-stu-id="2584e-173">Parameters - getType</span></span>

<span data-ttu-id="2584e-174">clrTypeName</span><span class="sxs-lookup"><span data-stu-id="2584e-174">clrTypeName</span></span>  

### <a name="return-value---gettype"></a><span data-ttu-id="2584e-175">戻り値 - getType</span><span class="sxs-lookup"><span data-stu-id="2584e-175">Return Value - getType</span></span>

## <a name="method-isnull"></a><span data-ttu-id="2584e-176">メソッド isNull</span><span class="sxs-lookup"><span data-stu-id="2584e-176">Method isNull</span></span>

<span data-ttu-id="2584e-177">指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にセットされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2584e-177">Confirms whether the specified CLRObject instance is set to nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

```xpp
public static boolean isNull(CLRObject clrObject)
```

### <a name="parameters---isnull"></a><span data-ttu-id="2584e-178">パラメーター - isNull</span><span class="sxs-lookup"><span data-stu-id="2584e-178">Parameters - isNull</span></span>

<span data-ttu-id="2584e-179">clrObject</span><span class="sxs-lookup"><span data-stu-id="2584e-179">clrObject</span></span>  
<span data-ttu-id="2584e-180">評価する CLRObject インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="2584e-180">The CLRObject instance to evaluate.</span></span>

### <a name="return-value---isnull"></a><span data-ttu-id="2584e-181">戻り値 - isNull</span><span class="sxs-lookup"><span data-stu-id="2584e-181">Return Value - isNull</span></span>

<span data-ttu-id="2584e-182">指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にセットされた場合または初期化されていない場合は true。</span><span class="sxs-lookup"><span data-stu-id="2584e-182">true if the specified CLRObject instance is set to nullNothingnullptrunita null reference (Nothing in Visual Basic) or has not been initialized.</span></span>

### <a name="remarks---isnull"></a><span data-ttu-id="2584e-183">備考 - isNull</span><span class="sxs-lookup"><span data-stu-id="2584e-183">Remarks - isNull</span></span>

<span data-ttu-id="2584e-184">CLR データ型が nullNothingnullptrunita null 参照 (Visual Basic では Nothing) であるかどうかを評価する条件ステートメントでは、X++ nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の代わりに isNull メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2584e-184">The isNull method should be used instead of the X++ nullNothingnullptrunita null reference (Nothing in Visual Basic) in conditional statements that evaluate whether a CLR data type is nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="examples---isnull"></a><span data-ttu-id="2584e-185">例 - isNull</span><span class="sxs-lookup"><span data-stu-id="2584e-185">Examples - isNull</span></span>

<span data-ttu-id="2584e-186">次の例では、CLR 文字列データ型を nullNothingnullptrunita null 参照 (Visual Basic では Nothing) に設定し、タイプ値を CLR オブジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2584e-186">The following example sets the CLR string data type to nullNothingnullptrunita null reference (Nothing in Visual Basic) and assigns the type value to the CLR object.</span></span> <span data-ttu-id="2584e-187">isNull メソッドを呼び出し、情報ログに結果を出力します。</span><span class="sxs-lookup"><span data-stu-id="2584e-187">It then calls the isNull method and prints the result in the Infolog.</span></span>

```xpp
static void Job5(Args _args) 
{ 
    System.String nullStr; 
```

```xpp
    nullStr = CLRInterop::Null("System.String"); 
```

```xpp
    print CLRInterop::isNull(nullStr); 
}
```

## <a name="method-null"></a><span data-ttu-id="2584e-188">メソッド Null</span><span class="sxs-lookup"><span data-stu-id="2584e-188">Method Null</span></span>

<span data-ttu-id="2584e-189">nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の値を持つ CLR データ型を返します。</span><span class="sxs-lookup"><span data-stu-id="2584e-189">Returns a CLR data type that has a value of nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

```xpp
public static CLRObject Null(str clrTypeName)
```

### <a name="parameters---null"></a><span data-ttu-id="2584e-190">パラメーター - Null</span><span class="sxs-lookup"><span data-stu-id="2584e-190">Parameters - Null</span></span>

<span data-ttu-id="2584e-191">clrTypeName</span><span class="sxs-lookup"><span data-stu-id="2584e-191">clrTypeName</span></span>  
<span data-ttu-id="2584e-192">nullNothingnullptrunita null参照 (Visual Basic では Nothing) に設定する必要がある CLR データ型。</span><span class="sxs-lookup"><span data-stu-id="2584e-192">The CLR data type to set to nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="return-value---null"></a><span data-ttu-id="2584e-193">戻り値 - Null</span><span class="sxs-lookup"><span data-stu-id="2584e-193">Return Value - Null</span></span>

<span data-ttu-id="2584e-194">指定された CLR データ型の CLRObject インスタンス。</span><span class="sxs-lookup"><span data-stu-id="2584e-194">A CLRObject instance of the specified CLR data type.</span></span>

### <a name="remarks---null"></a><span data-ttu-id="2584e-195">備考 - Null</span><span class="sxs-lookup"><span data-stu-id="2584e-195">Remarks - Null</span></span>

<span data-ttu-id="2584e-196">X++ で CLR データ型を NullNothingnullptrunita null 参照 (Visual Basic では Nothing) に直接設定する場合は、カーネル参照を nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にのみ設定します。</span><span class="sxs-lookup"><span data-stu-id="2584e-196">If you directly set CLR data types to nullNothingnullptrunita null reference (Nothing in Visual Basic) in X++, you only set the kernel reference to nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span> <span data-ttu-id="2584e-197">これにより、CLR データ型として型を使用することができなくなります。</span><span class="sxs-lookup"><span data-stu-id="2584e-197">This will make it impossible to use the type as a CLR data type.</span></span> <span data-ttu-id="2584e-198">CLRInterop:null("yourType") に CLR データ型を割り当てると、静的メソッド呼び出しのパラメーターとして、実行時にタイプを解析できます。</span><span class="sxs-lookup"><span data-stu-id="2584e-198">If you assign the CLR data type to CLRInterop:null("yourType"),, the type can be parsed at run time as a parameter of a static method invocation.</span></span>

### <a name="examples---null"></a><span data-ttu-id="2584e-199">例 - Null</span><span class="sxs-lookup"><span data-stu-id="2584e-199">Examples - Null</span></span>

<span data-ttu-id="2584e-200">次の例では、CLR 文字列型を nullNothingnullptrunita null 参照 (Visual Basic では Nothing) に設定し、タイプ値を CLR オブジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2584e-200">The following example sets the CLR string type to nullNothingnullptrunita null reference (Nothing in Visual Basic) and assigns the type value to a CLR object.</span></span>

```xpp
static void Job5(Args _args) 
{ 
    System.String nullStr; 
```

```xpp
    nullStr = CLRInterop::Null("System.String"); 
```

```xpp
    print CLRInterop::isInitialized(nullStr); 
    print CLRInterop::isNull(nullStr); 
}
```

## <a name="method-parseclrenum"></a><span data-ttu-id="2584e-201">メソッド parseClrEnum</span><span class="sxs-lookup"><span data-stu-id="2584e-201">Method parseClrEnum</span></span>

<span data-ttu-id="2584e-202">1 つ以上の列挙定数の名前または数値の文字列で表したものを、等価の CLRObject インスタンスに変換します。</span><span class="sxs-lookup"><span data-stu-id="2584e-202">Converts the string representation of the name or numeric value of one or more enumerated constants to an equivalent CLRObject instance.</span></span>

```xpp
public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)
```

### <a name="parameters---parseclrenum"></a><span data-ttu-id="2584e-203">パラメーター - parseClrEnum</span><span class="sxs-lookup"><span data-stu-id="2584e-203">Parameters - parseClrEnum</span></span>

<span data-ttu-id="2584e-204">clrEnumTypeName</span><span class="sxs-lookup"><span data-stu-id="2584e-204">clrEnumTypeName</span></span>  
<span data-ttu-id="2584e-205">変換する名前または値を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="2584e-205">A string that contains the name or value to convert.</span></span>

<!-- -->

<span data-ttu-id="2584e-206">enumValues</span><span class="sxs-lookup"><span data-stu-id="2584e-206">enumValues</span></span>  
<span data-ttu-id="2584e-207">変換する名前または値を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="2584e-207">A string that contains the name or value to convert.</span></span>

### <a name="return-value---parseclrenum"></a><span data-ttu-id="2584e-208">戻り値 - parseClrEnum</span><span class="sxs-lookup"><span data-stu-id="2584e-208">Return Value - parseClrEnum</span></span>

<span data-ttu-id="2584e-209">指定した CLR 列挙値を含む CLRObject インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="2584e-209">The CLRObject instance that contains the specified CLR enumerator values.</span></span>

### <a name="remarks---parseclrenum"></a><span data-ttu-id="2584e-210">備考 - parseClrEnum</span><span class="sxs-lookup"><span data-stu-id="2584e-210">Remarks - parseClrEnum</span></span>

<span data-ttu-id="2584e-211">\_enumValues パラメーターには、値、名前付き定数、またはコンマ (,) で区切られた名前付き定数の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2584e-211">The \_enumValues parameter contains a value, a named constant, or a list of named constants that are delimited by commas (,).</span></span> <span data-ttu-id="2584e-212">1 つ以上の空白スペースは、\_enumValues の各値、名前、またはコンマの前か後に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="2584e-212">One or more blanks spaces can precede or follow each value, name, or comma in \_enumValues.</span></span> <span data-ttu-id="2584e-213">\_enumValues が一覧の場合、戻り値は、ビット単位の OR 演算と組み合わされた指定された名前の値です。</span><span class="sxs-lookup"><span data-stu-id="2584e-213">If \_enumValues is a list, the return value is the value of the specified names combined with a bitwise OR operation.</span></span>

### <a name="examples---parseclrenum"></a><span data-ttu-id="2584e-214">例 - parseClrEnum</span><span class="sxs-lookup"><span data-stu-id="2584e-214">Examples - parseClrEnum</span></span>

<span data-ttu-id="2584e-215">次の例では、列挙子の値を月曜日の文字列値に変換し、Infolog の値を出力します。</span><span class="sxs-lookup"><span data-stu-id="2584e-215">The following example converts the enumerator value to the string value of Monday and prints the value in the Infolog.</span></span>

```xpp
static void Job6(Args _args) 
{ 
    System.DayOfWeek    dayOfWeek; 
    System.Type         dayOfWeekType; 
```

```xpp
    dayOfWeek = CLRInterop::parseClrEnum( "System.DayOfWeek", "Monday"); 
```

```xpp
    dayOfWeekType = dayOfWeek.GetType(); 
```

```xpp
    info( dayOfWeek.ToString() ); 
}
```

## <a name="method-staticinvoke"></a><span data-ttu-id="2584e-216">メソッド staticInvoke</span><span class="sxs-lookup"><span data-stu-id="2584e-216">Method staticInvoke</span></span>

<span data-ttu-id="2584e-217">CLR データ型の静的メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2584e-217">Calls a static method on a CLR data type.</span></span>

```xpp
public static CLRObject staticInvoke(str className, str methodName, VarArg params)
```

### <a name="parameters---staticinvoke"></a><span data-ttu-id="2584e-218">パラメーター - staticInvoke</span><span class="sxs-lookup"><span data-stu-id="2584e-218">Parameters - staticInvoke</span></span>

<span data-ttu-id="2584e-219">className</span><span class="sxs-lookup"><span data-stu-id="2584e-219">className</span></span>  
<span data-ttu-id="2584e-220">\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。</span><span class="sxs-lookup"><span data-stu-id="2584e-220">The arguments, if there are any, to the method that is specified in the \_methodName parameter.</span></span>

<!-- -->

<span data-ttu-id="2584e-221">methodName</span><span class="sxs-lookup"><span data-stu-id="2584e-221">methodName</span></span>  
<span data-ttu-id="2584e-222">\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。</span><span class="sxs-lookup"><span data-stu-id="2584e-222">The arguments, if there are any, to the method that is specified in the \_methodName parameter.</span></span>

<!-- -->

<span data-ttu-id="2584e-223">params</span><span class="sxs-lookup"><span data-stu-id="2584e-223">params</span></span>  
<span data-ttu-id="2584e-224">\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。</span><span class="sxs-lookup"><span data-stu-id="2584e-224">The arguments, if there are any, to the method that is specified in the \_methodName parameter.</span></span>

### <a name="return-value---staticinvoke"></a><span data-ttu-id="2584e-225">戻り値 - staticInvoke</span><span class="sxs-lookup"><span data-stu-id="2584e-225">Return Value - staticInvoke</span></span>

<span data-ttu-id="2584e-226">静的 CLR メソッドによって返される値を含む CLRObject。それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="2584e-226">The CLRObject that contains the value that is returned by the static CLR method; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---staticinvoke"></a><span data-ttu-id="2584e-227">備考 - staticInvoke</span><span class="sxs-lookup"><span data-stu-id="2584e-227">Remarks - staticInvoke</span></span>

<span data-ttu-id="2584e-228">攻撃者が staticInvoke メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="2584e-228">If an attacker can control input to the staticInvoke method, a security risk exists.</span></span> <span data-ttu-id="2584e-229">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="2584e-229">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="2584e-230">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="2584e-230">Calls to this method on the server require permission.</span></span> <span data-ttu-id="2584e-231">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2584e-231">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span> <span data-ttu-id="2584e-232">get\_Now メソッドを呼び出すときにエラーが発生した場合は、Exception::ClrError 例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="2584e-232">If an error occurs when you call the get\_Now method, the Exception::ClrError exception is thrown.</span></span>

### <a name="examples---staticinvoke"></a><span data-ttu-id="2584e-233">例 - staticInvoke</span><span class="sxs-lookup"><span data-stu-id="2584e-233">Examples - staticInvoke</span></span>

<span data-ttu-id="2584e-234">次の例では、System.DateTime CLR クラスの get\_Now メソッドを呼び出し、結果を Infolog に出力します。</span><span class="sxs-lookup"><span data-stu-id="2584e-234">The following example calls the get\_Now method on the System.DateTime CLR class and prints the results in the Infolog.</span></span>

```xpp
static void Job7(Args _args) 
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
    System.DateTime dateTime; 
```

```xpp
    perm = new InteropPermission(InteropKind::ClrInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
```

```xpp
    dateTime = CLRInterop::staticInvoke( 
                   "System.DateTime", 
                   "get_Now" ); 
    info(dateTime.ToString()); 
    CodeAccessPermission::revertAssert(); 
```

```xpp
    pause; 
```

```xpp
    // This is the same code using CLR syntax. 
    // dateTime = System.DateTime::get_Now(); 
    // info(dateTime.ToString()); 
}
```

## <a name="method-loadassembly"></a><span data-ttu-id="2584e-235">メソッド loadAssembly</span><span class="sxs-lookup"><span data-stu-id="2584e-235">Method loadAssembly</span></span>

```xpp
public static void loadAssembly(str clrAssemblyName)
```

### <a name="parameters---loadassembly"></a><span data-ttu-id="2584e-236">パラメーター - loadAssembly</span><span class="sxs-lookup"><span data-stu-id="2584e-236">Parameters - loadAssembly</span></span>

<span data-ttu-id="2584e-237">clrAssemblyName</span><span class="sxs-lookup"><span data-stu-id="2584e-237">clrAssemblyName</span></span>  

## <a name="method-new"></a><span data-ttu-id="2584e-238">メソッド new</span><span class="sxs-lookup"><span data-stu-id="2584e-238">Method new</span></span>

<span data-ttu-id="2584e-239">CLRInterop クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="2584e-239">Initializes a new instance of the CLRInterop class.</span></span>

```xpp
public void new()
```

### <a name="remarks---new"></a><span data-ttu-id="2584e-240">備考 - new</span><span class="sxs-lookup"><span data-stu-id="2584e-240">Remarks - new</span></span>

<span data-ttu-id="2584e-241">CLRInterop クラスのすべてのメンバーは静的です。</span><span class="sxs-lookup"><span data-stu-id="2584e-241">All members of the CLRInterop class are static.</span></span> <span data-ttu-id="2584e-242">このクラスをインスタンス化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2584e-242">There is no requirement to instantiate this class.</span></span> <span data-ttu-id="2584e-243">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="2584e-243">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="2584e-244">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="2584e-244">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="2584e-245">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="2584e-245">Calls to this method on the server require permission from the InteropPermission class.</span></span>

