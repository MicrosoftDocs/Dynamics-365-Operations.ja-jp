---
title: COMError クラス
description: このトピックでは、COMError クラスについて説明します。
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
ms.openlocfilehash: 79fc9e6ed9ae32546964a1b22b664d631a4b7c91
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502713"
---
# <a name="class-comerror"></a><span data-ttu-id="32504-103">クラス COMError</span><span class="sxs-lookup"><span data-stu-id="32504-103">Class COMError</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class COMError extends Object
```

<span data-ttu-id="32504-104">COMError クラスは、COM メソッド呼び出し時に発生するすべての COM エラーをラップします。</span><span class="sxs-lookup"><span data-stu-id="32504-104">The COMError class wraps any COM errors that occur during a COM method call.</span></span>

## <a name="remarks"></a><span data-ttu-id="32504-105">備考</span><span class="sxs-lookup"><span data-stu-id="32504-105">Remarks</span></span>

<span data-ttu-id="32504-106">COM メソッド呼び出し中にエラーが発生すると、エラー コードとエラーの説明が COMError オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="32504-106">When an error occurs during a COM method call, the error code and the error description are stored in the COMError object.</span></span> <span data-ttu-id="32504-107">COM クラスに関連付けられている COMError オブジェクトは、COM.error メソッドを使用して COM クラスから取得されます。</span><span class="sxs-lookup"><span data-stu-id="32504-107">The COMError object that is associated with a COM class is retrieved from the COM class by using the COM.error method.</span></span>

## <a name="examples"></a><span data-ttu-id="32504-108">例</span><span class="sxs-lookup"><span data-stu-id="32504-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="32504-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="32504-109">Methods</span></span>

| <span data-ttu-id="32504-110">方法</span><span class="sxs-lookup"><span data-stu-id="32504-110">Method</span></span>                   | <span data-ttu-id="32504-111">説明</span><span class="sxs-lookup"><span data-stu-id="32504-111">Description</span></span>                                                                                                               |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32504-112">public str description()</span><span class="sxs-lookup"><span data-stu-id="32504-112">public str description()</span></span> | <span data-ttu-id="32504-113">COM オブジェクトが呼び出されたときに発生したエラーの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-113">Returns a description of the error that occurred when the COM object was called.</span></span>                                          |
| <span data-ttu-id="32504-114">public int helpContext()</span><span class="sxs-lookup"><span data-stu-id="32504-114">public int helpContext()</span></span> | <span data-ttu-id="32504-115">COM オブジェクトが呼び出されたときに発生したエラーのヘルプ コンテキスト ID を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-115">Returns the Help context ID for the error that occurred when the COM object was called.</span></span>                                   |
| <span data-ttu-id="32504-116">public str helpFile()</span><span class="sxs-lookup"><span data-stu-id="32504-116">public str helpFile()</span></span>    | <span data-ttu-id="32504-117">COM オブジェクトが呼び出されたときに発生したエラーに関する情報が含まれるヘルプ ファイルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-117">Returns the name of the Help file that contains information about the error that occurred when the COM object was called.</span></span> |
| <span data-ttu-id="32504-118">public int number()</span><span class="sxs-lookup"><span data-stu-id="32504-118">public int number()</span></span>      | <span data-ttu-id="32504-119">COM オブジェクトが呼び出されたときに発生したエラーのエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="32504-119">Returns the error code of the error that occurred when the COM object was called.</span></span>                                         |
| <span data-ttu-id="32504-120">public str source()</span><span class="sxs-lookup"><span data-stu-id="32504-120">public str source()</span></span>      | <span data-ttu-id="32504-121">COM オブジェクトが呼び出されたときに発生したエラーを引き起こしたコンポーネントの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-121">Returns the name of the component that caused the error that occurred when the COM object was called.</span></span>                     |
| <span data-ttu-id="32504-122">public str toString()</span><span class="sxs-lookup"><span data-stu-id="32504-122">public str toString()</span></span>    | <span data-ttu-id="32504-123">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-123">Returns a string that contains the class handle and name, and sometimes additional information.</span></span>                           |
| <span data-ttu-id="32504-124">public void clear()</span><span class="sxs-lookup"><span data-stu-id="32504-124">public void clear()</span></span>      | <span data-ttu-id="32504-125">COMError オブジェクトのプロパティをクリアします。</span><span class="sxs-lookup"><span data-stu-id="32504-125">Clears the properties of the COMError object.</span></span>                                                                             |
| <span data-ttu-id="32504-126">public void new()</span><span class="sxs-lookup"><span data-stu-id="32504-126">public void new()</span></span>        | <span data-ttu-id="32504-127">COMError クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="32504-127">Initializes an instance of the COMError class.</span></span>                                                                            |
| <span data-ttu-id="32504-128">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="32504-128">public void finalize()</span></span>   |                                                                                                                           |

## <a name="method-description"></a><span data-ttu-id="32504-129">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="32504-129">Method description</span></span>

<span data-ttu-id="32504-130">COM オブジェクトが呼び出されたときに発生したエラーの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-130">Returns a description of the error that occurred when the COM object was called.</span></span>

```xpp
public str description()
```

### <a name="return-value---description"></a><span data-ttu-id="32504-131">戻り値 - description</span><span class="sxs-lookup"><span data-stu-id="32504-131">Return Value - description</span></span>

<span data-ttu-id="32504-132">エラーの説明です。</span><span class="sxs-lookup"><span data-stu-id="32504-132">The error description.</span></span>

### <a name="remarks---description"></a><span data-ttu-id="32504-133">備考 - description</span><span class="sxs-lookup"><span data-stu-id="32504-133">Remarks - description</span></span>

<span data-ttu-id="32504-134">COM オブジェクトがテキストのエラー メッセージの手渡しをサポートしていない場合は、説明が空白になることがあります。</span><span class="sxs-lookup"><span data-stu-id="32504-134">The description might be empty if the COM object does not support handing out textual error messages.</span></span> <span data-ttu-id="32504-135">説明のプロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="32504-135">The description property is read-only.</span></span>

## <a name="method-helpcontext"></a><span data-ttu-id="32504-136">メソッド helpContext</span><span class="sxs-lookup"><span data-stu-id="32504-136">Method helpContext</span></span>

<span data-ttu-id="32504-137">COM オブジェクトが呼び出されたときに発生したエラーのヘルプ コンテキスト ID を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-137">Returns the Help context ID for the error that occurred when the COM object was called.</span></span>

```xpp
public int helpContext()
```

### <a name="return-value---helpcontext"></a><span data-ttu-id="32504-138">戻り値 - helpContext</span><span class="sxs-lookup"><span data-stu-id="32504-138">Return Value - helpContext</span></span>

<span data-ttu-id="32504-139">ヘルプ コンテキスト ID。</span><span class="sxs-lookup"><span data-stu-id="32504-139">The Help context ID.</span></span>

### <a name="remarks---helpcontext"></a><span data-ttu-id="32504-140">備考 - helpContext</span><span class="sxs-lookup"><span data-stu-id="32504-140">Remarks - helpContext</span></span>

<span data-ttu-id="32504-141">ヘルプ コンテキスト ID は、COM オブジェクトがエラーのヘルプをサポートしていない場合、0 (ゼロ) にすることができます。</span><span class="sxs-lookup"><span data-stu-id="32504-141">The Help context ID might be 0 (zero) if the COM object does not support Help for its errors.</span></span> <span data-ttu-id="32504-142">helpContext プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="32504-142">The helpContext property is read-only.</span></span>

## <a name="method-helpfile"></a><span data-ttu-id="32504-143">メソッド helpFile</span><span class="sxs-lookup"><span data-stu-id="32504-143">Method helpFile</span></span>

<span data-ttu-id="32504-144">COM オブジェクトが呼び出されたときに発生したエラーに関する情報が含まれるヘルプ ファイルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-144">Returns the name of the Help file that contains information about the error that occurred when the COM object was called.</span></span>

```xpp
public str helpFile()
```

### <a name="return-value---helpfile"></a><span data-ttu-id="32504-145">戻り値 - helpFile</span><span class="sxs-lookup"><span data-stu-id="32504-145">Return Value - helpFile</span></span>

<span data-ttu-id="32504-146">ヘルプ ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="32504-146">The name of the Help file.</span></span>

### <a name="remarks---helpfile"></a><span data-ttu-id="32504-147">備考 - helpFile</span><span class="sxs-lookup"><span data-stu-id="32504-147">Remarks - helpFile</span></span>

<span data-ttu-id="32504-148">ヘルプ ファイルは、COM オブジェクトがエラーのヘルプをサポートしていない場合、空にすることができます。</span><span class="sxs-lookup"><span data-stu-id="32504-148">The Help file might be empty if the COM object does not support Help for its errors.</span></span> <span data-ttu-id="32504-149">helpFile プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="32504-149">The helpFile property is read-only.</span></span>

## <a name="method-number"></a><span data-ttu-id="32504-150">メソッド number</span><span class="sxs-lookup"><span data-stu-id="32504-150">Method number</span></span>

<span data-ttu-id="32504-151">COM オブジェクトが呼び出されたときに発生したエラーのエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="32504-151">Returns the error code of the error that occurred when the COM object was called.</span></span>

```xpp
public int number()
```

### <a name="return-value---number"></a><span data-ttu-id="32504-152">戻り値 - number</span><span class="sxs-lookup"><span data-stu-id="32504-152">Return Value - number</span></span>

<span data-ttu-id="32504-153">エラーコード。COM オブジェクトが呼び出されたときにエラーが発生しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="32504-153">The error code; 0 (zero) if no error occurred when the COM object was called.</span></span>

### <a name="remarks---number"></a><span data-ttu-id="32504-154">備考 - number</span><span class="sxs-lookup"><span data-stu-id="32504-154">Remarks - number</span></span>

<span data-ttu-id="32504-155">数プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="32504-155">The number property is read-only.</span></span>

## <a name="method-source"></a><span data-ttu-id="32504-156">メソッド source</span><span class="sxs-lookup"><span data-stu-id="32504-156">Method source</span></span>

<span data-ttu-id="32504-157">COM オブジェクトが呼び出されたときに発生したエラーを引き起こしたコンポーネントの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-157">Returns the name of the component that caused the error that occurred when the COM object was called.</span></span>

```xpp
public str source()
```

### <a name="return-value---source"></a><span data-ttu-id="32504-158">戻り値 - source</span><span class="sxs-lookup"><span data-stu-id="32504-158">Return Value - source</span></span>

<span data-ttu-id="32504-159">エラーのソース。</span><span class="sxs-lookup"><span data-stu-id="32504-159">The source of the error.</span></span>

### <a name="remarks---source"></a><span data-ttu-id="32504-160">備考 - source</span><span class="sxs-lookup"><span data-stu-id="32504-160">Remarks - source</span></span>

<span data-ttu-id="32504-161">COM オブジェクトがエラーのソースの手渡しをサポートしていない場合は、ソースが空白になることがあります。</span><span class="sxs-lookup"><span data-stu-id="32504-161">The source might be empty if the COM object does not support handing out the source of the error.</span></span> <span data-ttu-id="32504-162">ソースのプロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="32504-162">The source property is read-only.</span></span>

## <a name="method-tostring"></a><span data-ttu-id="32504-163">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="32504-163">Method toString</span></span>

<span data-ttu-id="32504-164">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="32504-164">Returns a string that contains the class handle and name, and sometimes additional information.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="32504-165">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="32504-165">Return Value - toString</span></span>

<span data-ttu-id="32504-166">クラスのテキストの説明。</span><span class="sxs-lookup"><span data-stu-id="32504-166">A textual description of the class.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="32504-167">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="32504-167">Remarks - toString</span></span>

<span data-ttu-id="32504-168">ほとんどのクラスでは、返される文字列には、クラス ハンドルと名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="32504-168">For most classes, the string that is returned contains the class handle and name.</span></span> <span data-ttu-id="32504-169">ただし、一部のクラスでは、文字列に追加情報が追加されます。</span><span class="sxs-lookup"><span data-stu-id="32504-169">However, for some classes, additional information is included in the string.</span></span>

## <a name="method-clear"></a><span data-ttu-id="32504-170">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="32504-170">Method clear</span></span>

<span data-ttu-id="32504-171">COMError オブジェクトのプロパティをクリアします。</span><span class="sxs-lookup"><span data-stu-id="32504-171">Clears the properties of the COMError object.</span></span>

```xpp
public void clear()
```

### <a name="remarks---clear"></a><span data-ttu-id="32504-172">備考 - clear</span><span class="sxs-lookup"><span data-stu-id="32504-172">Remarks - clear</span></span>

<span data-ttu-id="32504-173">通常、COMError オブジェクトのプロパティは読み取り専用ですが、このメソッドを使用して解除できます。</span><span class="sxs-lookup"><span data-stu-id="32504-173">The properties of the COMError object are usually read-only, but they can be cleared by using this method.</span></span>

## <a name="method-new"></a><span data-ttu-id="32504-174">メソッド new</span><span class="sxs-lookup"><span data-stu-id="32504-174">Method new</span></span>

<span data-ttu-id="32504-175">COMError クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="32504-175">Initializes an instance of the COMError class.</span></span>

```xpp
public void new()
```

## <a name="method-finalize"></a><span data-ttu-id="32504-176">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="32504-176">Method finalize</span></span>

```xpp
public void finalize()
```

