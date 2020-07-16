---
title: XppPrePostArgs クラス
description: このトピックでは、XppPrePostArgs クラスについて説明します。
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
ms.openlocfilehash: c374813b5c3e1d9890e3751c048f90398572f5d8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502774"
---
# <a name="class-xppprepostargs"></a><span data-ttu-id="6bb7a-103">クラス XppPrePostArgs</span><span class="sxs-lookup"><span data-stu-id="6bb7a-103">Class XppPrePostArgs</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class XppPrePostArgs extends XppEventArgs
```

<span data-ttu-id="6bb7a-104">XppPrePostArgs クラスは、プリハンドラーとポストハンドラーのためのパブリッシャーの引数と戻り値に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-104">The XppPrePostArgs class provides information about a publisher's arguments and return values for pre-handlers and post-handlers.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb7a-105">備考</span><span class="sxs-lookup"><span data-stu-id="6bb7a-105">Remarks</span></span>

<span data-ttu-id="6bb7a-106">パブリッシャーは、プリイベントとポストイベントを公開するメソッドです。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-106">A publisher is a method that exposes pre-events and post-events.</span></span>

## <a name="examples"></a><span data-ttu-id="6bb7a-107">例</span><span class="sxs-lookup"><span data-stu-id="6bb7a-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6bb7a-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="6bb7a-108">Methods</span></span>

| <span data-ttu-id="6bb7a-109">方法</span><span class="sxs-lookup"><span data-stu-id="6bb7a-109">Method</span></span>                                                                                       | <span data-ttu-id="6bb7a-110">説明</span><span class="sxs-lookup"><span data-stu-id="6bb7a-110">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb7a-111">public boolean wrapper(str fieldName, AnyType value)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-111">public boolean wrapper(str fieldName, AnyType value)</span></span>                                         |                                                                                                             |
| <span data-ttu-id="6bb7a-112">public struct args()</span><span class="sxs-lookup"><span data-stu-id="6bb7a-112">public struct args()</span></span>                                                                         |                                                                                                             |
| <span data-ttu-id="6bb7a-113">public boolean existsArg(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-113">public boolean existsArg(str fieldName)</span></span>                                                      | <span data-ttu-id="6bb7a-114">出版社の引数の存在を名前でチェックします。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-114">Checks the existence of the publisher's argument by name.</span></span>                                                   |
| <span data-ttu-id="6bb7a-115">public AnyType getArgNum(int argIndex)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-115">public AnyType getArgNum(int argIndex)</span></span>                                                       | <span data-ttu-id="6bb7a-116">パブリッシャーの引数をインデックスごとに取得します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-116">Retrieves the ;publisher's argument by index.</span></span>                                                               |
| <span data-ttu-id="6bb7a-117">public int setArgNum(int argIndex, AnyType value)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-117">public int setArgNum(int argIndex, AnyType value)</span></span>                                            | <span data-ttu-id="6bb7a-118">パブリッシャーの引数をインデックスごとに設定します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-118">Sets the publisher's argument by index.</span></span>                                                                     |
| <span data-ttu-id="6bb7a-119">public AnyType value(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-119">public AnyType value(str fieldName)</span></span>                                                          |                                                                                                             |
| <span data-ttu-id="6bb7a-120">public XppEventHandlerCalledWhen getCalledWhen()</span><span class="sxs-lookup"><span data-stu-id="6bb7a-120">public XppEventHandlerCalledWhen getCalledWhen()</span></span>                                             | <span data-ttu-id="6bb7a-121">プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-121">Retrieves a value that indicates whether the instance is currently serving a pre-handler or a post-handler.</span></span> |
| <span data-ttu-id="6bb7a-122">public AnyType getReturnValue()</span><span class="sxs-lookup"><span data-stu-id="6bb7a-122">public AnyType getReturnValue()</span></span>                                                              | <span data-ttu-id="6bb7a-123">発行元の戻り値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-123">Gets the publisher's return value.</span></span>                                                                          |
| <span data-ttu-id="6bb7a-124">public AnyType getThis()</span><span class="sxs-lookup"><span data-stu-id="6bb7a-124">public AnyType getThis()</span></span>                                                                     | <span data-ttu-id="6bb7a-125">発行元の「this」参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-125">Gets the publisher's "this" reference.</span></span>                                                                      |
| <span data-ttu-id="6bb7a-126">public boolean removeArg(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-126">public boolean removeArg(str fieldName)</span></span>                                                      |                                                                                                             |
| <span data-ttu-id="6bb7a-127">public int wrapper(str fieldName, AnyType value)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-127">public int wrapper(str fieldName, AnyType value)</span></span>                                             |                                                                                                             |
| <span data-ttu-id="6bb7a-128">public int setReturnValue(AnyType retval)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-128">public int setReturnValue(AnyType retval)</span></span>                                                    | <span data-ttu-id="6bb7a-129">発行元の戻り値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-129">Sets the publisher's return value.</span></span>                                                                          |
| <span data-ttu-id="6bb7a-130">public str isFirst()</span><span class="sxs-lookup"><span data-stu-id="6bb7a-130">public str isFirst()</span></span>                                                                         |                                                                                                             |
| <span data-ttu-id="6bb7a-131">public void setCalledWhen(XppEventHandlerCalledWhen calledWhen)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-131">public void setCalledWhen(XppEventHandlerCalledWhen calledWhen)</span></span>                              | <span data-ttu-id="6bb7a-132">プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-132">Sets whether the instance is currently serving a pre-handler or a post-handler.</span></span>                             |
| <span data-ttu-id="6bb7a-133">::public static void setReturnValueEx(AnyType retval, XppPrePostArgs args)</span><span class="sxs-lookup"><span data-stu-id="6bb7a-133">::public static void setReturnValueEx(AnyType retval, XppPrePostArgs args)</span></span>                   |                                                                                                             |
| <span data-ttu-id="6bb7a-134">public void new(\[AnyType thisPtr\], \[str args\], \[XppEventHandlerCalledWhen calledWhen\])</span><span class="sxs-lookup"><span data-stu-id="6bb7a-134">public void new(\[AnyType thisPtr\], \[str args\], \[XppEventHandlerCalledWhen calledWhen\])</span></span> | <span data-ttu-id="6bb7a-135">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-135">Initializes a new instance of the Object class.</span></span>                                                             |

## <a name="method-wrapper"></a><span data-ttu-id="6bb7a-136">メソッド wrapper</span><span class="sxs-lookup"><span data-stu-id="6bb7a-136">Method wrapper</span></span>

```xpp
public boolean wrapper(str fieldName, AnyType value)
```

### <a name="parameters---wrapper"></a><span data-ttu-id="6bb7a-137">パラメーター - wrapper</span><span class="sxs-lookup"><span data-stu-id="6bb7a-137">Parameters - wrapper</span></span>

<span data-ttu-id="6bb7a-138">fieldName</span><span class="sxs-lookup"><span data-stu-id="6bb7a-138">fieldName</span></span>  

<!-- -->

<span data-ttu-id="6bb7a-139">値</span><span class="sxs-lookup"><span data-stu-id="6bb7a-139">value</span></span>  

### <a name="return-value---wrapper"></a><span data-ttu-id="6bb7a-140">戻り値 - wrapper</span><span class="sxs-lookup"><span data-stu-id="6bb7a-140">Return Value - wrapper</span></span>

## <a name="method-args"></a><span data-ttu-id="6bb7a-141">メソッド args</span><span class="sxs-lookup"><span data-stu-id="6bb7a-141">Method args</span></span>

```xpp
public struct args()
```

### <a name="return-value---args"></a><span data-ttu-id="6bb7a-142">戻り値 - args</span><span class="sxs-lookup"><span data-stu-id="6bb7a-142">Return Value - args</span></span>

## <a name="method-existsarg"></a><span data-ttu-id="6bb7a-143">メソッド existsArg</span><span class="sxs-lookup"><span data-stu-id="6bb7a-143">Method existsArg</span></span>

<span data-ttu-id="6bb7a-144">出版社の引数の存在を名前でチェックします。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-144">Checks the existence of the publisher's argument by name.</span></span>

```xpp
public boolean existsArg(str fieldName)
```

### <a name="parameters---existsarg"></a><span data-ttu-id="6bb7a-145">パラメーター - existsArg</span><span class="sxs-lookup"><span data-stu-id="6bb7a-145">Parameters - existsArg</span></span>

<span data-ttu-id="6bb7a-146">fieldName</span><span class="sxs-lookup"><span data-stu-id="6bb7a-146">fieldName</span></span>  

### <a name="return-value---existsarg"></a><span data-ttu-id="6bb7a-147">戻り値 - existsArg</span><span class="sxs-lookup"><span data-stu-id="6bb7a-147">Return Value - existsArg</span></span>

<span data-ttu-id="6bb7a-148">指定された引数が存在するかどうかを示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-148">A Boolean data type value that indicates whether the specified argument exists.</span></span>

### <a name="remarks---existsarg"></a><span data-ttu-id="6bb7a-149">備考 - existsArg</span><span class="sxs-lookup"><span data-stu-id="6bb7a-149">Remarks - existsArg</span></span>

<span data-ttu-id="6bb7a-150">引数名は大文字と小文字を区別しません。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-150">Argument names are case insensitive.</span></span>

## <a name="method-getargnum"></a><span data-ttu-id="6bb7a-151">メソッド getArgNum</span><span class="sxs-lookup"><span data-stu-id="6bb7a-151">Method getArgNum</span></span>

<span data-ttu-id="6bb7a-152">パブリッシャーの引数をインデックスごとに取得します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-152">Retrieves the ;publisher's argument by index.</span></span>

```xpp
public AnyType getArgNum(int argIndex)
```

### <a name="parameters---getargnum"></a><span data-ttu-id="6bb7a-153">パラメーター - getArgNum</span><span class="sxs-lookup"><span data-stu-id="6bb7a-153">Parameters - getArgNum</span></span>

<span data-ttu-id="6bb7a-154">argIndex</span><span class="sxs-lookup"><span data-stu-id="6bb7a-154">argIndex</span></span>  
<span data-ttu-id="6bb7a-155">ターゲット引数の int インデックス。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-155">An int index of the target argument.</span></span>

### <a name="return-value---getargnum"></a><span data-ttu-id="6bb7a-156">戻り値 - getArgNum</span><span class="sxs-lookup"><span data-stu-id="6bb7a-156">Return Value - getArgNum</span></span>

<span data-ttu-id="6bb7a-157">指定された引数の anytype 値です。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-157">An anytype value of the specified argument.</span></span>

### <a name="remarks---getargnum"></a><span data-ttu-id="6bb7a-158">備考 - getArgNum</span><span class="sxs-lookup"><span data-stu-id="6bb7a-158">Remarks - getArgNum</span></span>

<span data-ttu-id="6bb7a-159">インデックスの範囲は、静的パブリッシャーの場合は 0 ベース、インスタンス パブリッシャーの場合は 1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-159">The index range is 0-based for static publishers but 1-based for instance publishers.</span></span>

## <a name="method-setargnum"></a><span data-ttu-id="6bb7a-160">メソッド setArgNum</span><span class="sxs-lookup"><span data-stu-id="6bb7a-160">Method setArgNum</span></span>

<span data-ttu-id="6bb7a-161">パブリッシャーの引数をインデックスごとに設定します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-161">Sets the publisher's argument by index.</span></span>

```xpp
public int setArgNum(int argIndex, AnyType value)
```

### <a name="parameters---setargnum"></a><span data-ttu-id="6bb7a-162">パラメーター - setArgNum</span><span class="sxs-lookup"><span data-stu-id="6bb7a-162">Parameters - setArgNum</span></span>

<span data-ttu-id="6bb7a-163">argIndex</span><span class="sxs-lookup"><span data-stu-id="6bb7a-163">argIndex</span></span>  
<span data-ttu-id="6bb7a-164">指定された引数に割り当てる anytype 値です。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-164">An anytype value to assign to the specified argument.</span></span>

<!-- -->

<span data-ttu-id="6bb7a-165">値</span><span class="sxs-lookup"><span data-stu-id="6bb7a-165">value</span></span>  
<span data-ttu-id="6bb7a-166">指定された引数に割り当てる anytype 値です。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-166">An anytype value to assign to the specified argument.</span></span>

### <a name="return-value---setargnum"></a><span data-ttu-id="6bb7a-167">戻り値 - setArgNum</span><span class="sxs-lookup"><span data-stu-id="6bb7a-167">Return Value - setArgNum</span></span>

<span data-ttu-id="6bb7a-168">int データ型値 1 。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-168">An int data type value of 1.</span></span>

### <a name="remarks---setargnum"></a><span data-ttu-id="6bb7a-169">備考 - setArgNum</span><span class="sxs-lookup"><span data-stu-id="6bb7a-169">Remarks - setArgNum</span></span>

<span data-ttu-id="6bb7a-170">インデックスの範囲は、静的パブリッシャーの場合は 0 ベース、インスタンス パブリッシャーの場合は 1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-170">The index range is 0-based for static publishers but 1-based for instance publishers.</span></span>

## <a name="method-value"></a><span data-ttu-id="6bb7a-171">メソッド value</span><span class="sxs-lookup"><span data-stu-id="6bb7a-171">Method value</span></span>

```xpp
public AnyType value(str fieldName)
```

### <a name="parameters---value"></a><span data-ttu-id="6bb7a-172">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="6bb7a-172">Parameters - value</span></span>

<span data-ttu-id="6bb7a-173">fieldName</span><span class="sxs-lookup"><span data-stu-id="6bb7a-173">fieldName</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="6bb7a-174">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="6bb7a-174">Return Value - value</span></span>

## <a name="method-getcalledwhen"></a><span data-ttu-id="6bb7a-175">メソッド getCalledWhen</span><span class="sxs-lookup"><span data-stu-id="6bb7a-175">Method getCalledWhen</span></span>

<span data-ttu-id="6bb7a-176">プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-176">Retrieves a value that indicates whether the instance is currently serving a pre-handler or a post-handler.</span></span>

```xpp
public XppEventHandlerCalledWhen getCalledWhen()
```

### <a name="return-value---getcalledwhen"></a><span data-ttu-id="6bb7a-177">戻り値 - getCalledWhen</span><span class="sxs-lookup"><span data-stu-id="6bb7a-177">Return Value - getCalledWhen</span></span>

<span data-ttu-id="6bb7a-178">XppPrePostArgs インスタンスはプリハンドラーまたはポストハンドラーかどうかを示す XppEventHandlerCalledWhen データ型値です。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-178">An XppEventHandlerCalledWhen data type value that indicates whether the XppPrePostArgs instance is serving the pre-handlers or the post-handlers.</span></span>

## <a name="method-getreturnvalue"></a><span data-ttu-id="6bb7a-179">メソッド getReturnValue</span><span class="sxs-lookup"><span data-stu-id="6bb7a-179">Method getReturnValue</span></span>

<span data-ttu-id="6bb7a-180">発行元の戻り値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-180">Gets the publisher's return value.</span></span>

```xpp
public AnyType getReturnValue()
```

### <a name="return-value---getreturnvalue"></a><span data-ttu-id="6bb7a-181">戻り値 - getReturnValue</span><span class="sxs-lookup"><span data-stu-id="6bb7a-181">Return Value - getReturnValue</span></span>

<span data-ttu-id="6bb7a-182">anytype データ型値は、発行元の戻り値を表します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-182">An anytype data type value that represents the publisher's return value.</span></span>

### <a name="remarks---getreturnvalue"></a><span data-ttu-id="6bb7a-183">備考 - getReturnValue</span><span class="sxs-lookup"><span data-stu-id="6bb7a-183">Remarks - getReturnValue</span></span>

<span data-ttu-id="6bb7a-184">このメソッドは、プリハンドラー用ではありません。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-184">This method is not intended for pre-handlers.</span></span>

## <a name="method-getthis"></a><span data-ttu-id="6bb7a-185">メソッド getThis</span><span class="sxs-lookup"><span data-stu-id="6bb7a-185">Method getThis</span></span>

<span data-ttu-id="6bb7a-186">発行元の「this」参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-186">Gets the publisher's "this" reference.</span></span>

```xpp
public AnyType getThis()
```

### <a name="return-value---getthis"></a><span data-ttu-id="6bb7a-187">戻り値 - getThis</span><span class="sxs-lookup"><span data-stu-id="6bb7a-187">Return Value - getThis</span></span>

<span data-ttu-id="6bb7a-188">anytype データ型値は、発行元の「this」参照を表します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-188">An anytype data type value that represents the publisher's "this" reference.</span></span>

### <a name="remarks---getthis"></a><span data-ttu-id="6bb7a-189">備考 - getThis</span><span class="sxs-lookup"><span data-stu-id="6bb7a-189">Remarks - getThis</span></span>

<span data-ttu-id="6bb7a-190">パブリッシャーが静的な場合は、nullNothingnullptrunita null 参照 (Visual Basic ではなしになる) を返します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-190">Returns a nullNothingnullptrunita null reference (Nothing in Visual Basic) reference if the publisher is static.</span></span>

## <a name="method-removearg"></a><span data-ttu-id="6bb7a-191">メソッド removeArg</span><span class="sxs-lookup"><span data-stu-id="6bb7a-191">Method removeArg</span></span>

```xpp
public boolean removeArg(str fieldName)
```

### <a name="parameters---removearg"></a><span data-ttu-id="6bb7a-192">パラメーター - removeArg</span><span class="sxs-lookup"><span data-stu-id="6bb7a-192">Parameters - removeArg</span></span>

<span data-ttu-id="6bb7a-193">fieldName</span><span class="sxs-lookup"><span data-stu-id="6bb7a-193">fieldName</span></span>  

### <a name="return-value---removearg"></a><span data-ttu-id="6bb7a-194">戻り値 - removeArg</span><span class="sxs-lookup"><span data-stu-id="6bb7a-194">Return Value - removeArg</span></span>

## <a name="method-wrapper"></a><span data-ttu-id="6bb7a-195">メソッド wrapper</span><span class="sxs-lookup"><span data-stu-id="6bb7a-195">Method wrapper</span></span>

```xpp
public int wrapper(str fieldName, AnyType value)
```

### <a name="parameters---wrapper"></a><span data-ttu-id="6bb7a-196">パラメーター - wrapper</span><span class="sxs-lookup"><span data-stu-id="6bb7a-196">Parameters - wrapper</span></span>

<span data-ttu-id="6bb7a-197">fieldName</span><span class="sxs-lookup"><span data-stu-id="6bb7a-197">fieldName</span></span>  

<!-- -->

<span data-ttu-id="6bb7a-198">値</span><span class="sxs-lookup"><span data-stu-id="6bb7a-198">value</span></span>  

### <a name="return-value---wrapper"></a><span data-ttu-id="6bb7a-199">戻り値 - wrapper</span><span class="sxs-lookup"><span data-stu-id="6bb7a-199">Return Value - wrapper</span></span>

## <a name="method-setreturnvalue"></a><span data-ttu-id="6bb7a-200">メソッド setReturnValue</span><span class="sxs-lookup"><span data-stu-id="6bb7a-200">Method setReturnValue</span></span>

<span data-ttu-id="6bb7a-201">発行元の戻り値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-201">Sets the publisher's return value.</span></span>

```xpp
public int setReturnValue(AnyType retval)
```

### <a name="parameters---setreturnvalue"></a><span data-ttu-id="6bb7a-202">パラメーター - setReturnValue</span><span class="sxs-lookup"><span data-stu-id="6bb7a-202">Parameters - setReturnValue</span></span>

<span data-ttu-id="6bb7a-203">retval</span><span class="sxs-lookup"><span data-stu-id="6bb7a-203">retval</span></span>  

### <a name="return-value---setreturnvalue"></a><span data-ttu-id="6bb7a-204">戻り値 - setReturnValue</span><span class="sxs-lookup"><span data-stu-id="6bb7a-204">Return Value - setReturnValue</span></span>

<span data-ttu-id="6bb7a-205">int データ型値 1 。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-205">An int data type value of 1.</span></span>

### <a name="remarks---setreturnvalue"></a><span data-ttu-id="6bb7a-206">備考 - setReturnValue</span><span class="sxs-lookup"><span data-stu-id="6bb7a-206">Remarks - setReturnValue</span></span>

<span data-ttu-id="6bb7a-207">このメソッドは、プリハンドラーまたは無効を返すパブリッシャーのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-207">This method is not intended for pre-handlers or for publishers that return void.</span></span>

## <a name="method-isfirst"></a><span data-ttu-id="6bb7a-208">メソッド isFirst</span><span class="sxs-lookup"><span data-stu-id="6bb7a-208">Method isFirst</span></span>

```xpp
public str isFirst()
```

### <a name="return-value---isfirst"></a><span data-ttu-id="6bb7a-209">戻り値 - isFirst</span><span class="sxs-lookup"><span data-stu-id="6bb7a-209">Return Value - isFirst</span></span>

## <a name="method-setcalledwhen"></a><span data-ttu-id="6bb7a-210">メソッド setCalledWhen</span><span class="sxs-lookup"><span data-stu-id="6bb7a-210">Method setCalledWhen</span></span>

<span data-ttu-id="6bb7a-211">プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを設定します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-211">Sets whether the instance is currently serving a pre-handler or a post-handler.</span></span>

```xpp
public void setCalledWhen(XppEventHandlerCalledWhen calledWhen)
```

### <a name="parameters---setcalledwhen"></a><span data-ttu-id="6bb7a-212">パラメーター - setCalledWhen</span><span class="sxs-lookup"><span data-stu-id="6bb7a-212">Parameters - setCalledWhen</span></span>

<span data-ttu-id="6bb7a-213">calledWhen</span><span class="sxs-lookup"><span data-stu-id="6bb7a-213">calledWhen</span></span>  

### <a name="remarks---setcalledwhen"></a><span data-ttu-id="6bb7a-214">備考 - setCalledWhen</span><span class="sxs-lookup"><span data-stu-id="6bb7a-214">Remarks - setCalledWhen</span></span>

<span data-ttu-id="6bb7a-215">このメソッドは、プリハンドラーまたはポストハンドラーのコードから明示的に呼び出されてはなりません。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-215">This method must never be called explicitly from the pre-handler or post-handler code.</span></span> <span data-ttu-id="6bb7a-216">このメソッドは、単体テストおよび自動生成コード用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-216">This method is reserved for unit testing and auto-generated code only.</span></span>

## <a name="method-setreturnvalueex"></a><span data-ttu-id="6bb7a-217">メソッド setReturnValueEx</span><span class="sxs-lookup"><span data-stu-id="6bb7a-217">Method setReturnValueEx</span></span>

```xpp
public static void setReturnValueEx(AnyType retval, XppPrePostArgs args)
```

### <a name="parameters---setreturnvalueex"></a><span data-ttu-id="6bb7a-218">パラメーター - setReturnValueEx</span><span class="sxs-lookup"><span data-stu-id="6bb7a-218">Parameters - setReturnValueEx</span></span>

<span data-ttu-id="6bb7a-219">retval</span><span class="sxs-lookup"><span data-stu-id="6bb7a-219">retval</span></span>  

<!-- -->

<span data-ttu-id="6bb7a-220">args</span><span class="sxs-lookup"><span data-stu-id="6bb7a-220">args</span></span>  

## <a name="method-new"></a><span data-ttu-id="6bb7a-221">メソッド new</span><span class="sxs-lookup"><span data-stu-id="6bb7a-221">Method new</span></span>

<span data-ttu-id="6bb7a-222">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6bb7a-222">Initializes a new instance of the Object class.</span></span>

```xpp
public void new([AnyType thisPtr], [str args], [XppEventHandlerCalledWhen calledWhen])
```

### <a name="parameters---new"></a><span data-ttu-id="6bb7a-223">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="6bb7a-223">Parameters - new</span></span>

<span data-ttu-id="6bb7a-224">thisPtr</span><span class="sxs-lookup"><span data-stu-id="6bb7a-224">thisPtr</span></span>  

<!-- -->

<span data-ttu-id="6bb7a-225">args</span><span class="sxs-lookup"><span data-stu-id="6bb7a-225">args</span></span>  

<!-- -->

<span data-ttu-id="6bb7a-226">calledWhen</span><span class="sxs-lookup"><span data-stu-id="6bb7a-226">calledWhen</span></span>  

