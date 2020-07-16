---
title: BinData クラス
description: このトピックでは、BinData クラスについて説明します。
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
ms.openlocfilehash: 693f2179ce7344cfa565456b8ee539d4708a6142
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502721"
---
# <a name="class-bindata"></a><span data-ttu-id="b34da-103">クラス BinData</span><span class="sxs-lookup"><span data-stu-id="b34da-103">Class BinData</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class BinData extends Object
```

## <a name="remarks"></a><span data-ttu-id="b34da-104">備考</span><span class="sxs-lookup"><span data-stu-id="b34da-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b34da-105">例</span><span class="sxs-lookup"><span data-stu-id="b34da-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b34da-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b34da-106">Methods</span></span>

| <span data-ttu-id="b34da-107">方法</span><span class="sxs-lookup"><span data-stu-id="b34da-107">Method</span></span>                                                                | <span data-ttu-id="b34da-108">説明</span><span class="sxs-lookup"><span data-stu-id="b34da-108">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="b34da-109">public boolean appendToFile(str filename)</span><span class="sxs-lookup"><span data-stu-id="b34da-109">public boolean appendToFile(str filename)</span></span>                             |                                               |
| <span data-ttu-id="b34da-110">public str ascii85Encode()</span><span class="sxs-lookup"><span data-stu-id="b34da-110">public str ascii85Encode()</span></span>                                            |                                               |
| <span data-ttu-id="b34da-111">public str base64Encode()</span><span class="sxs-lookup"><span data-stu-id="b34da-111">public str base64Encode()</span></span>                                             |                                               |
| <span data-ttu-id="b34da-112">public int compressLZ77(int windowBits)</span><span class="sxs-lookup"><span data-stu-id="b34da-112">public int compressLZ77(int windowBits)</span></span>                               |                                               |
| <span data-ttu-id="b34da-113">public boolean copyData(BinData data, \[int offset\], \[int length\])</span><span class="sxs-lookup"><span data-stu-id="b34da-113">public boolean copyData(BinData data, \[int offset\], \[int length\])</span></span> |                                               |
| <span data-ttu-id="b34da-114">public int decompressLZ77()</span><span class="sxs-lookup"><span data-stu-id="b34da-114">public int decompressLZ77()</span></span>                                           |                                               |
| <span data-ttu-id="b34da-115">public str getAsciiData()</span><span class="sxs-lookup"><span data-stu-id="b34da-115">public str getAsciiData()</span></span>                                             |                                               |
| <span data-ttu-id="b34da-116">public container getData()</span><span class="sxs-lookup"><span data-stu-id="b34da-116">public container getData()</span></span>                                            |                                               |
| <span data-ttu-id="b34da-117">public str getStrData()</span><span class="sxs-lookup"><span data-stu-id="b34da-117">public str getStrData()</span></span>                                               |                                               |
| <span data-ttu-id="b34da-118">public COMVariant getVariant()</span><span class="sxs-lookup"><span data-stu-id="b34da-118">public COMVariant getVariant()</span></span>                                        |                                               |
| <span data-ttu-id="b34da-119">public boolean loadFile(str filename, \[int offset\], \[int length\])</span><span class="sxs-lookup"><span data-stu-id="b34da-119">public boolean loadFile(str filename, \[int offset\], \[int length\])</span></span> |                                               |
| <span data-ttu-id="b34da-120">public boolean saveFile(str filename)</span><span class="sxs-lookup"><span data-stu-id="b34da-120">public boolean saveFile(str filename)</span></span>                                 |                                               |
| <span data-ttu-id="b34da-121">public int size()</span><span class="sxs-lookup"><span data-stu-id="b34da-121">public int size()</span></span>                                                     |                                               |
| <span data-ttu-id="b34da-122">::public static str dataToString(container data)</span><span class="sxs-lookup"><span data-stu-id="b34da-122">::public static str dataToString(container data)</span></span>                      |                                               |
| <span data-ttu-id="b34da-123">::public static container loadFromAscii85(str ascii85EncodedString)</span><span class="sxs-lookup"><span data-stu-id="b34da-123">::public static container loadFromAscii85(str ascii85EncodedString)</span></span>   |                                               |
| <span data-ttu-id="b34da-124">::public static container loadFromBase64(str base64EncodedString)</span><span class="sxs-lookup"><span data-stu-id="b34da-124">::public static container loadFromBase64(str base64EncodedString)</span></span>     |                                               |
| <span data-ttu-id="b34da-125">::public static container stringToData(str string)</span><span class="sxs-lookup"><span data-stu-id="b34da-125">::public static container stringToData(str string)</span></span>                    |                                               |
| <span data-ttu-id="b34da-126">public void setStrData(str data)</span><span class="sxs-lookup"><span data-stu-id="b34da-126">public void setStrData(str data)</span></span>                                      |                                               |
| <span data-ttu-id="b34da-127">public void setVariant(COMVariant data)</span><span class="sxs-lookup"><span data-stu-id="b34da-127">public void setVariant(COMVariant data)</span></span>                               |                                               |
| <span data-ttu-id="b34da-128">public void appendData(BinData binData)</span><span class="sxs-lookup"><span data-stu-id="b34da-128">public void appendData(BinData binData)</span></span>                               |                                               |
| <span data-ttu-id="b34da-129">public void new()</span><span class="sxs-lookup"><span data-stu-id="b34da-129">public void new()</span></span>                                                     | <span data-ttu-id="b34da-130">BinData クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b34da-130">Initializes an instance of the BinData class.</span></span> |
| <span data-ttu-id="b34da-131">public void setBinaryData(Binary binary)</span><span class="sxs-lookup"><span data-stu-id="b34da-131">public void setBinaryData(Binary binary)</span></span>                              |                                               |
| <span data-ttu-id="b34da-132">public void setAsciiData(str data, \[int codePage\])</span><span class="sxs-lookup"><span data-stu-id="b34da-132">public void setAsciiData(str data, \[int codePage\])</span></span>                  |                                               |
| <span data-ttu-id="b34da-133">public void setData(container data)</span><span class="sxs-lookup"><span data-stu-id="b34da-133">public void setData(container data)</span></span>                                   |                                               |
| <span data-ttu-id="b34da-134">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="b34da-134">public void finalize()</span></span>                                                |                                               |

## <a name="method-appendtofile"></a><span data-ttu-id="b34da-135">メソッド appendToFile</span><span class="sxs-lookup"><span data-stu-id="b34da-135">Method appendToFile</span></span>

```xpp
public boolean appendToFile(str filename)
```

### <a name="parameters---appendtofile"></a><span data-ttu-id="b34da-136">パラメーター - appendToFile</span><span class="sxs-lookup"><span data-stu-id="b34da-136">Parameters - appendToFile</span></span>

<span data-ttu-id="b34da-137">filename</span><span class="sxs-lookup"><span data-stu-id="b34da-137">filename</span></span>  

### <a name="return-value---appendtofile"></a><span data-ttu-id="b34da-138">戻り値 - appendToFile</span><span class="sxs-lookup"><span data-stu-id="b34da-138">Return Value - appendToFile</span></span>

## <a name="method-ascii85encode"></a><span data-ttu-id="b34da-139">メソッド ascii85Encode</span><span class="sxs-lookup"><span data-stu-id="b34da-139">Method ascii85Encode</span></span>

```xpp
public str ascii85Encode()
```

### <a name="return-value---ascii85encode"></a><span data-ttu-id="b34da-140">戻り値 - ascii85Encode</span><span class="sxs-lookup"><span data-stu-id="b34da-140">Return Value - ascii85Encode</span></span>

## <a name="method-base64encode"></a><span data-ttu-id="b34da-141">メソッド base64Encode</span><span class="sxs-lookup"><span data-stu-id="b34da-141">Method base64Encode</span></span>

```xpp
public str base64Encode()
```

### <a name="return-value---base64encode"></a><span data-ttu-id="b34da-142">戻り値 - base64Encode</span><span class="sxs-lookup"><span data-stu-id="b34da-142">Return Value - base64Encode</span></span>

## <a name="method-compresslz77"></a><span data-ttu-id="b34da-143">メソッド compressLZ77</span><span class="sxs-lookup"><span data-stu-id="b34da-143">Method compressLZ77</span></span>

```xpp
public int compressLZ77(int windowBits)
```

### <a name="parameters---compresslz77"></a><span data-ttu-id="b34da-144">パラメーター - compressLZ77</span><span class="sxs-lookup"><span data-stu-id="b34da-144">Parameters - compressLZ77</span></span>

<span data-ttu-id="b34da-145">windowBits</span><span class="sxs-lookup"><span data-stu-id="b34da-145">windowBits</span></span>  

### <a name="return-value---compresslz77"></a><span data-ttu-id="b34da-146">戻り値 - compressLZ77</span><span class="sxs-lookup"><span data-stu-id="b34da-146">Return Value - compressLZ77</span></span>

## <a name="method-copydata"></a><span data-ttu-id="b34da-147">メソッド copyData</span><span class="sxs-lookup"><span data-stu-id="b34da-147">Method copyData</span></span>

```xpp
public boolean copyData(BinData data, [int offset], [int length])
```

### <a name="parameters---copydata"></a><span data-ttu-id="b34da-148">パラメーター - copyData</span><span class="sxs-lookup"><span data-stu-id="b34da-148">Parameters - copyData</span></span>

<span data-ttu-id="b34da-149">データ</span><span class="sxs-lookup"><span data-stu-id="b34da-149">data</span></span>  

<!-- -->

<span data-ttu-id="b34da-150">相殺</span><span class="sxs-lookup"><span data-stu-id="b34da-150">offset</span></span>  

<!-- -->

<span data-ttu-id="b34da-151">length</span><span class="sxs-lookup"><span data-stu-id="b34da-151">length</span></span>  

### <a name="return-value---copydata"></a><span data-ttu-id="b34da-152">戻り値 - copyData</span><span class="sxs-lookup"><span data-stu-id="b34da-152">Return Value - copyData</span></span>

## <a name="method-decompresslz77"></a><span data-ttu-id="b34da-153">メソッド decompressLZ77</span><span class="sxs-lookup"><span data-stu-id="b34da-153">Method decompressLZ77</span></span>

```xpp
public int decompressLZ77()
```

### <a name="return-value---decompresslz77"></a><span data-ttu-id="b34da-154">戻り値 - decompressLZ77</span><span class="sxs-lookup"><span data-stu-id="b34da-154">Return Value - decompressLZ77</span></span>

## <a name="method-getasciidata"></a><span data-ttu-id="b34da-155">メソッド getAsciiData</span><span class="sxs-lookup"><span data-stu-id="b34da-155">Method getAsciiData</span></span>

```xpp
public str getAsciiData()
```

### <a name="return-value---getasciidata"></a><span data-ttu-id="b34da-156">戻り値 - getAsciiData</span><span class="sxs-lookup"><span data-stu-id="b34da-156">Return Value - getAsciiData</span></span>

## <a name="method-getdata"></a><span data-ttu-id="b34da-157">メソッド getData</span><span class="sxs-lookup"><span data-stu-id="b34da-157">Method getData</span></span>

```xpp
public container getData()
```

### <a name="return-value---getdata"></a><span data-ttu-id="b34da-158">戻り値 - getData</span><span class="sxs-lookup"><span data-stu-id="b34da-158">Return Value - getData</span></span>

## <a name="method-getstrdata"></a><span data-ttu-id="b34da-159">メソッド getStrData</span><span class="sxs-lookup"><span data-stu-id="b34da-159">Method getStrData</span></span>

```xpp
public str getStrData()
```

### <a name="return-value---getstrdata"></a><span data-ttu-id="b34da-160">戻り値 - getStrData</span><span class="sxs-lookup"><span data-stu-id="b34da-160">Return Value - getStrData</span></span>

## <a name="method-getvariant"></a><span data-ttu-id="b34da-161">メソッド getVariant</span><span class="sxs-lookup"><span data-stu-id="b34da-161">Method getVariant</span></span>

```xpp
public COMVariant getVariant()
```

### <a name="return-value---getvariant"></a><span data-ttu-id="b34da-162">戻り値 - getVariant</span><span class="sxs-lookup"><span data-stu-id="b34da-162">Return Value - getVariant</span></span>

## <a name="method-loadfile"></a><span data-ttu-id="b34da-163">メソッド loadFile</span><span class="sxs-lookup"><span data-stu-id="b34da-163">Method loadFile</span></span>

```xpp
public boolean loadFile(str filename, [int offset], [int length])
```

### <a name="parameters---loadfile"></a><span data-ttu-id="b34da-164">パラメーター - loadFile</span><span class="sxs-lookup"><span data-stu-id="b34da-164">Parameters - loadFile</span></span>

<span data-ttu-id="b34da-165">filename</span><span class="sxs-lookup"><span data-stu-id="b34da-165">filename</span></span>  

<!-- -->

<span data-ttu-id="b34da-166">相殺</span><span class="sxs-lookup"><span data-stu-id="b34da-166">offset</span></span>  

<!-- -->

<span data-ttu-id="b34da-167">length</span><span class="sxs-lookup"><span data-stu-id="b34da-167">length</span></span>  

### <a name="return-value---loadfile"></a><span data-ttu-id="b34da-168">戻り値 - loadFile</span><span class="sxs-lookup"><span data-stu-id="b34da-168">Return Value - loadFile</span></span>

### <a name="remarks---loadfile"></a><span data-ttu-id="b34da-169">備考 - loadFile</span><span class="sxs-lookup"><span data-stu-id="b34da-169">Remarks - loadFile</span></span>

<span data-ttu-id="b34da-170">攻撃者が loadFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="b34da-170">If an attacker can control input to the loadFile method, a security risk exists.</span></span> <span data-ttu-id="b34da-171">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="b34da-171">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="b34da-172">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="b34da-172">Calls to this method on the server require permission.</span></span> <span data-ttu-id="b34da-173">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b34da-173">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

## <a name="method-savefile"></a><span data-ttu-id="b34da-174">メソッド saveFile</span><span class="sxs-lookup"><span data-stu-id="b34da-174">Method saveFile</span></span>

```xpp
public boolean saveFile(str filename)
```

### <a name="parameters---savefile"></a><span data-ttu-id="b34da-175">パラメーター - saveFile</span><span class="sxs-lookup"><span data-stu-id="b34da-175">Parameters - saveFile</span></span>

<span data-ttu-id="b34da-176">filename</span><span class="sxs-lookup"><span data-stu-id="b34da-176">filename</span></span>  

### <a name="return-value---savefile"></a><span data-ttu-id="b34da-177">戻り値 - saveFile</span><span class="sxs-lookup"><span data-stu-id="b34da-177">Return Value - saveFile</span></span>

### <a name="remarks---savefile"></a><span data-ttu-id="b34da-178">備考 - saveFile</span><span class="sxs-lookup"><span data-stu-id="b34da-178">Remarks - saveFile</span></span>

<span data-ttu-id="b34da-179">攻撃者が saveFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="b34da-179">If an attacker can control input to the saveFile method, a security risk exists.</span></span> <span data-ttu-id="b34da-180">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="b34da-180">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="b34da-181">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="b34da-181">Calls to this method on the server require permission.</span></span> <span data-ttu-id="b34da-182">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b34da-182">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

## <a name="method-size"></a><span data-ttu-id="b34da-183">メソッド size</span><span class="sxs-lookup"><span data-stu-id="b34da-183">Method size</span></span>

```xpp
public int size()
```

### <a name="return-value---size"></a><span data-ttu-id="b34da-184">戻り値 - size</span><span class="sxs-lookup"><span data-stu-id="b34da-184">Return Value - size</span></span>

## <a name="method-datatostring"></a><span data-ttu-id="b34da-185">メソッド dataToString</span><span class="sxs-lookup"><span data-stu-id="b34da-185">Method dataToString</span></span>

```xpp
public static str dataToString(container data)
```

### <a name="parameters---datatostring"></a><span data-ttu-id="b34da-186">パラメーター - dataToString</span><span class="sxs-lookup"><span data-stu-id="b34da-186">Parameters - dataToString</span></span>

<span data-ttu-id="b34da-187">データ</span><span class="sxs-lookup"><span data-stu-id="b34da-187">data</span></span>  

### <a name="return-value---datatostring"></a><span data-ttu-id="b34da-188">戻り値 - dataToString</span><span class="sxs-lookup"><span data-stu-id="b34da-188">Return Value - dataToString</span></span>

## <a name="method-loadfromascii85"></a><span data-ttu-id="b34da-189">メソッド loadFromAscii85</span><span class="sxs-lookup"><span data-stu-id="b34da-189">Method loadFromAscii85</span></span>

```xpp
public static container loadFromAscii85(str ascii85EncodedString)
```

### <a name="parameters---loadfromascii85"></a><span data-ttu-id="b34da-190">パラメーター - loadFromAscii85</span><span class="sxs-lookup"><span data-stu-id="b34da-190">Parameters - loadFromAscii85</span></span>

<span data-ttu-id="b34da-191">ascii85EncodedString</span><span class="sxs-lookup"><span data-stu-id="b34da-191">ascii85EncodedString</span></span>  

### <a name="return-value---loadfromascii85"></a><span data-ttu-id="b34da-192">戻り値 - loadFromAscii85</span><span class="sxs-lookup"><span data-stu-id="b34da-192">Return Value - loadFromAscii85</span></span>

## <a name="method-loadfrombase64"></a><span data-ttu-id="b34da-193">メソッド loadFromBase64</span><span class="sxs-lookup"><span data-stu-id="b34da-193">Method loadFromBase64</span></span>

```xpp
public static container loadFromBase64(str base64EncodedString)
```

### <a name="parameters---loadfrombase64"></a><span data-ttu-id="b34da-194">パラメーター - loadFromBase64</span><span class="sxs-lookup"><span data-stu-id="b34da-194">Parameters - loadFromBase64</span></span>

<span data-ttu-id="b34da-195">base64EncodedString</span><span class="sxs-lookup"><span data-stu-id="b34da-195">base64EncodedString</span></span>  

### <a name="return-value---loadfrombase64"></a><span data-ttu-id="b34da-196">戻り値 - loadFromBase64</span><span class="sxs-lookup"><span data-stu-id="b34da-196">Return Value - loadFromBase64</span></span>

## <a name="method-stringtodata"></a><span data-ttu-id="b34da-197">メソッド stringToData</span><span class="sxs-lookup"><span data-stu-id="b34da-197">Method stringToData</span></span>

```xpp
public static container stringToData(str string)
```

### <a name="parameters---stringtodata"></a><span data-ttu-id="b34da-198">パラメーター - stringToData</span><span class="sxs-lookup"><span data-stu-id="b34da-198">Parameters - stringToData</span></span>

<span data-ttu-id="b34da-199">文字列</span><span class="sxs-lookup"><span data-stu-id="b34da-199">string</span></span>  

### <a name="return-value---stringtodata"></a><span data-ttu-id="b34da-200">戻り値 - stringToData</span><span class="sxs-lookup"><span data-stu-id="b34da-200">Return Value - stringToData</span></span>

## <a name="method-setstrdata"></a><span data-ttu-id="b34da-201">メソッド setStrData</span><span class="sxs-lookup"><span data-stu-id="b34da-201">Method setStrData</span></span>

```xpp
public void setStrData(str data)
```

### <a name="parameters---setstrdata"></a><span data-ttu-id="b34da-202">パラメーター - setStrData</span><span class="sxs-lookup"><span data-stu-id="b34da-202">Parameters - setStrData</span></span>

<span data-ttu-id="b34da-203">データ</span><span class="sxs-lookup"><span data-stu-id="b34da-203">data</span></span>  

## <a name="method-setvariant"></a><span data-ttu-id="b34da-204">メソッド setVariant</span><span class="sxs-lookup"><span data-stu-id="b34da-204">Method setVariant</span></span>

```xpp
public void setVariant(COMVariant data)
```

### <a name="parameters---setvariant"></a><span data-ttu-id="b34da-205">パラメーター - setVariant</span><span class="sxs-lookup"><span data-stu-id="b34da-205">Parameters - setVariant</span></span>

<span data-ttu-id="b34da-206">データ</span><span class="sxs-lookup"><span data-stu-id="b34da-206">data</span></span>  

## <a name="method-appenddata"></a><span data-ttu-id="b34da-207">メソッド appendData</span><span class="sxs-lookup"><span data-stu-id="b34da-207">Method appendData</span></span>

```xpp
public void appendData(BinData binData)
```

### <a name="parameters---appenddata"></a><span data-ttu-id="b34da-208">パラメーター - appendData</span><span class="sxs-lookup"><span data-stu-id="b34da-208">Parameters - appendData</span></span>

<span data-ttu-id="b34da-209">binData</span><span class="sxs-lookup"><span data-stu-id="b34da-209">binData</span></span>  

## <a name="method-new"></a><span data-ttu-id="b34da-210">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b34da-210">Method new</span></span>

<span data-ttu-id="b34da-211">BinData クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b34da-211">Initializes an instance of the BinData class.</span></span>

```xpp
public void new()
```

## <a name="method-setbinarydata"></a><span data-ttu-id="b34da-212">メソッド setBinaryData</span><span class="sxs-lookup"><span data-stu-id="b34da-212">Method setBinaryData</span></span>

```xpp
public void setBinaryData(Binary binary)
```

### <a name="parameters---setbinarydata"></a><span data-ttu-id="b34da-213">パラメーター - setBinaryData</span><span class="sxs-lookup"><span data-stu-id="b34da-213">Parameters - setBinaryData</span></span>

<span data-ttu-id="b34da-214">binary</span><span class="sxs-lookup"><span data-stu-id="b34da-214">binary</span></span>  

## <a name="method-setasciidata"></a><span data-ttu-id="b34da-215">メソッド setAsciiData</span><span class="sxs-lookup"><span data-stu-id="b34da-215">Method setAsciiData</span></span>

```xpp
public void setAsciiData(str data, [int codePage])
```

### <a name="parameters---setasciidata"></a><span data-ttu-id="b34da-216">パラメーター - setAsciiData</span><span class="sxs-lookup"><span data-stu-id="b34da-216">Parameters - setAsciiData</span></span>

<span data-ttu-id="b34da-217">データ</span><span class="sxs-lookup"><span data-stu-id="b34da-217">data</span></span>  

<!-- -->

<span data-ttu-id="b34da-218">codePage</span><span class="sxs-lookup"><span data-stu-id="b34da-218">codePage</span></span>  

## <a name="method-setdata"></a><span data-ttu-id="b34da-219">メソッド setData</span><span class="sxs-lookup"><span data-stu-id="b34da-219">Method setData</span></span>

```xpp
public void setData(container data)
```

### <a name="parameters---setdata"></a><span data-ttu-id="b34da-220">パラメーター - setData</span><span class="sxs-lookup"><span data-stu-id="b34da-220">Parameters - setData</span></span>

<span data-ttu-id="b34da-221">データ</span><span class="sxs-lookup"><span data-stu-id="b34da-221">data</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="b34da-222">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="b34da-222">Method finalize</span></span>

```xpp
public void finalize()
```


