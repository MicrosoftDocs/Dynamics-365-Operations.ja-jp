---
title: COMVariant クラス
description: このトピックでは、COMVariant クラスについて説明します。
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
ms.openlocfilehash: 261fae114d6b6cf1159cb1687d7722f6d52a4173
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502716"
---
# <a name="class-comvariant"></a><span data-ttu-id="015df-103">クラス COMVariant</span><span class="sxs-lookup"><span data-stu-id="015df-103">Class COMVariant</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class COMVariant extends Object
```

<span data-ttu-id="015df-104">COMVariant クラスは、さまざまな種類のデータを格納できる一般的なクラスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-104">The COMVariant class is used as a generic class that can store different types of data.</span></span> <span data-ttu-id="015df-105">このクラスは、COM (コンポーネント オブジェクト モデル) 自動オブジェクトのメソッドまたはプロパティに引数を渡すために使用され、COM および COMDispFunction クラスとともに使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-105">The class is used to pass arguments to the methods or properties of a COM (Component Object Model) Automation object and is used with the COM and COMDispFunction classes.</span></span>

## <a name="remarks"></a><span data-ttu-id="015df-106">備考</span><span class="sxs-lookup"><span data-stu-id="015df-106">Remarks</span></span>

<span data-ttu-id="015df-107">COMVariant オブジェクトのデータ型は次によって設定できます。</span><span class="sxs-lookup"><span data-stu-id="015df-107">The data type of the COMVariant object can be set by:</span></span>

-   <span data-ttu-id="015df-108">新しいメソッド</span><span class="sxs-lookup"><span data-stu-id="015df-108">The new method</span></span>
-   <span data-ttu-id="015df-109">variantType メソッド</span><span class="sxs-lookup"><span data-stu-id="015df-109">The variantType method</span></span>
-   <span data-ttu-id="015df-110">CreateFrom� メソッド。</span><span class="sxs-lookup"><span data-stu-id="015df-110">The createFrom� methods.</span></span> <span data-ttu-id="015df-111">たとえば、createFromBoolean メソッドは、VT\_BOOL (= ブール値) のタイプの COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-111">For example, the createFromBoolean method creates a COMVariant object of type VT\_BOOL (= Boolean).</span></span>
-   <span data-ttu-id="015df-112">プロパティ メソッド。</span><span class="sxs-lookup"><span data-stu-id="015df-112">The property methods.</span></span> <span data-ttu-id="015df-113">たとえば、boolean プロパティを使用して新しい値を設定すると、オブジェクトは VT\_BOOL (= Boolean) のタイプではなく、このタイプに変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-113">For example, if you set a new value by using the boolean property, and the object is not of type VT\_BOOL (= Boolean), it will be changed to this type.</span></span>

<span data-ttu-id="015df-114">データ型の値は、いずれかのプロパティ メソッドによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="015df-114">The value of the data type is set by one of the property methods.</span></span> <span data-ttu-id="015df-115">たとえば、タイプ VT\_BOOL の COMVariant オブジェクトの値は、boolean メソッドにより設定されます。</span><span class="sxs-lookup"><span data-stu-id="015df-115">For example, the value of a COMVariant object of type VT\_BOOL is set by the boolean method.</span></span> <span data-ttu-id="015df-116">その値を設定する可能なデータ型とメソッドは、「備考」セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="015df-116">The possible data types and the methods that set their values are listed in the Remarks section.</span></span> <span data-ttu-id="015df-117">COMVariant クラスがサポートするデータ型は、X++ データ型ではなく、COMオートメーション標準によって定義されたデータ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-117">The data types that the COMVariant class supports are not X++ data types, but data types defined by the COM Automation standard.</span></span> <span data-ttu-id="015df-118">COMVariant クラスは、Win32 SDK にある VARIANT 構造に基づいています。</span><span class="sxs-lookup"><span data-stu-id="015df-118">The COMVariant class is based on the VARIANT structure found in the Win32 SDK.</span></span> <span data-ttu-id="015df-119">詳細については、Win32 SDK ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="015df-119">For more information see the Win32 SDK documentation.</span></span> <span data-ttu-id="015df-120">COMVariant クラスのプロパティ メソッドは、次のように COMVariantType 値にマップされます。</span><span class="sxs-lookup"><span data-stu-id="015df-120">The property methods of the COMVariant class map to the COMVariantType values in the following way:</span></span>

|             |               |                                                                                           |
|-------------|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="015df-121">ブール値</span><span class="sxs-lookup"><span data-stu-id="015df-121">boolean</span></span>     | <span data-ttu-id="015df-122">VT\_BOOL</span><span class="sxs-lookup"><span data-stu-id="015df-122">VT\_BOOL</span></span>      |                                                                                           |
| <span data-ttu-id="015df-123">bStr</span><span class="sxs-lookup"><span data-stu-id="015df-123">bStr</span></span>        | <span data-ttu-id="015df-124">VT\_BSTR</span><span class="sxs-lookup"><span data-stu-id="015df-124">VT\_BSTR</span></span>      | <span data-ttu-id="015df-125">文字列データ型</span><span class="sxs-lookup"><span data-stu-id="015df-125">String data type</span></span>                                                                          |
| <span data-ttu-id="015df-126">byte</span><span class="sxs-lookup"><span data-stu-id="015df-126">byte</span></span>        | <span data-ttu-id="015df-127">VT\_UI1</span><span class="sxs-lookup"><span data-stu-id="015df-127">VT\_UI1</span></span>       |                                                                                           |
| <span data-ttu-id="015df-128">char</span><span class="sxs-lookup"><span data-stu-id="015df-128">char</span></span>        | <span data-ttu-id="015df-129">VT\_I1</span><span class="sxs-lookup"><span data-stu-id="015df-129">VT\_I1</span></span>        |                                                                                           |
| <span data-ttu-id="015df-130">通貨</span><span class="sxs-lookup"><span data-stu-id="015df-130">currency</span></span>    | <span data-ttu-id="015df-131">VT\_CY</span><span class="sxs-lookup"><span data-stu-id="015df-131">VT\_CY</span></span>        |                                                                                           |
| <span data-ttu-id="015df-132">日付、時刻</span><span class="sxs-lookup"><span data-stu-id="015df-132">date, time</span></span>  | <span data-ttu-id="015df-133">VT\_DATE</span><span class="sxs-lookup"><span data-stu-id="015df-133">VT\_DATE</span></span>      | <span data-ttu-id="015df-134">日付/時刻データ型。両方のプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="015df-134">Date/time data type; both properties must be set.</span></span>                                         |
| <span data-ttu-id="015df-135">decimal</span><span class="sxs-lookup"><span data-stu-id="015df-135">decimal</span></span>     | <span data-ttu-id="015df-136">VT\_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="015df-136">VT\_DECIMAL</span></span>   |                                                                                           |
| <span data-ttu-id="015df-137">double</span><span class="sxs-lookup"><span data-stu-id="015df-137">double</span></span>      | <span data-ttu-id="015df-138">VT\_R8</span><span class="sxs-lookup"><span data-stu-id="015df-138">VT\_R8</span></span>        |                                                                                           |
| <span data-ttu-id="015df-139">float</span><span class="sxs-lookup"><span data-stu-id="015df-139">float</span></span>       | <span data-ttu-id="015df-140">VT\_R4</span><span class="sxs-lookup"><span data-stu-id="015df-140">VT\_R4</span></span>        |                                                                                           |
| <span data-ttu-id="015df-141">iDispatch</span><span class="sxs-lookup"><span data-stu-id="015df-141">iDispatch</span></span>   | <span data-ttu-id="015df-142">VT\_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="015df-142">VT\_DISPATCH</span></span>  |                                                                                           |
| <span data-ttu-id="015df-143">int, long</span><span class="sxs-lookup"><span data-stu-id="015df-143">int, long</span></span>   | <span data-ttu-id="015df-144">VT\_I4</span><span class="sxs-lookup"><span data-stu-id="015df-144">VT\_I4</span></span>        | <span data-ttu-id="015df-145">VT\_I4 は、int データ型と Long データ型の両方で使用されます</span><span class="sxs-lookup"><span data-stu-id="015df-145">VT\_I4 is used for both the int and the long data types</span></span>                                   |
| <span data-ttu-id="015df-146">iUnknown</span><span class="sxs-lookup"><span data-stu-id="015df-146">iUnknown</span></span>    | <span data-ttu-id="015df-147">VT\_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="015df-147">VT\_UNKNOWN</span></span>   |                                                                                           |
| <span data-ttu-id="015df-148">sCode</span><span class="sxs-lookup"><span data-stu-id="015df-148">sCode</span></span>       | <span data-ttu-id="015df-149">VT\_ERROR</span><span class="sxs-lookup"><span data-stu-id="015df-149">VT\_ERROR</span></span>     | <span data-ttu-id="015df-150">scode データ型は、Win32 HRESULT データ型と同等の COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-150">The scode data type is a COM data type that is equivalent to the Win32 HRESULT data type.</span></span> |
| <span data-ttu-id="015df-151">short</span><span class="sxs-lookup"><span data-stu-id="015df-151">short</span></span>       | <span data-ttu-id="015df-152">VT\_I2</span><span class="sxs-lookup"><span data-stu-id="015df-152">VT\_I2</span></span>        |                                                                                           |
| <span data-ttu-id="015df-153">uInt、uLong</span><span class="sxs-lookup"><span data-stu-id="015df-153">uInt, uLong</span></span> | <span data-ttu-id="015df-154">VT\_UI4</span><span class="sxs-lookup"><span data-stu-id="015df-154">VT\_UI4</span></span>       | <span data-ttu-id="015df-155">VT\_UI4 は、uInt データ型と uLong データ型の両方で使用されます</span><span class="sxs-lookup"><span data-stu-id="015df-155">VT\_UI4 is used for both the uInt and the uLong data types</span></span>                                |
| <span data-ttu-id="015df-156">uShort</span><span class="sxs-lookup"><span data-stu-id="015df-156">uShort</span></span>      | <span data-ttu-id="015df-157">VT\_UI2</span><span class="sxs-lookup"><span data-stu-id="015df-157">VT\_UI2</span></span>       |                                                                                           |
| <span data-ttu-id="015df-158">バリアント</span><span class="sxs-lookup"><span data-stu-id="015df-158">variant</span></span>     | <span data-ttu-id="015df-159">VT\_VARIANT</span><span class="sxs-lookup"><span data-stu-id="015df-159">VT\_VARIANT</span></span>   |                                                                                           |
| <span data-ttu-id="015df-160">safeArray</span><span class="sxs-lookup"><span data-stu-id="015df-160">safeArray</span></span>   | <span data-ttu-id="015df-161">VT\_SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="015df-161">VT\_SAFEARRAY</span></span> | <span data-ttu-id="015df-162">配列データ タイプ</span><span class="sxs-lookup"><span data-stu-id="015df-162">Array data type</span></span>                                                                           |

## <a name="examples"></a><span data-ttu-id="015df-163">例</span><span class="sxs-lookup"><span data-stu-id="015df-163">Examples</span></span>

<span data-ttu-id="015df-164">次の例では、COMVariant パラメーターとして渡された 2 つの浮動小数点数を乗算する multiply というメソッドを公開する COM オブジェクトをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="015df-164">The following example instantiates a COM object that exposes a method called multiply which multiplies two floating point numbers passed in as COMVariant parameters.</span></span>

```xpp
{ 
    COM com; 
    COMVariant varArg1 = new COMVariant(); 
    COMVariant varArg2 = new COMVariant(); 
    COMVariant varRet; 
    real ret; 
    InteropPermission perm; 
```

```xpp
    // Set code access permission to help protect the use  
    // of the COM object. 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    // Permission scope starts here 
    perm.assert(); 
```

```xpp
        com = new COM("MyCOM.Object"); 
```

```xpp
    // Specify arguments for the 'multiply' method 
    varArg1.float(123); 
    varArg2.float(456); 
    varRet = com.multiply(varArg1, varArg2); 
```

```xpp
    ret = varRet.double(); 
    // 'ret' is now 56088 (123*456) 
```

```xpp
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a><span data-ttu-id="015df-165">メソッド</span><span class="sxs-lookup"><span data-stu-id="015df-165">Methods</span></span>

| <span data-ttu-id="015df-166">方法</span><span class="sxs-lookup"><span data-stu-id="015df-166">Method</span></span>                                                                                                    | <span data-ttu-id="015df-167">説明</span><span class="sxs-lookup"><span data-stu-id="015df-167">Description</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="015df-168">public boolean boolean(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-168">public boolean boolean(\[boolean newValue\])</span></span>                                                              | <span data-ttu-id="015df-169">VT\_BOOL データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-169">Gets or sets the value of a COMVariant object of the VT\_BOOL data type.</span></span>                                                                                                    |
| <span data-ttu-id="015df-170">public str bStr(\[str newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-170">public str bStr(\[str newValue\])</span></span>                                                                         | <span data-ttu-id="015df-171">VT\_BSTR データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-171">Gets or sets the value of a COMVariant object of the VT\_BSTR data type.</span></span>                                                                                                    |
| <span data-ttu-id="015df-172">public int byte(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-172">public int byte(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="015df-173">VT\_UI1 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-173">Gets or sets the value of a COMVariant object of the VT\_UI1 data type.</span></span>                                                                                                     |
| <span data-ttu-id="015df-174">public int char(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-174">public int char(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="015df-175">VT\_I1 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-175">Gets or sets the value of a COMVariant object of the VT\_I1 data type.</span></span>                                                                                                      |
| <span data-ttu-id="015df-176">public container container(\[container newValue\], \[COMVariantType newType\])</span><span class="sxs-lookup"><span data-stu-id="015df-176">public container container(\[container newValue\], \[COMVariantType newType\])</span></span>                            | <span data-ttu-id="015df-177">コンテナ データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-177">Gets or sets the value of a COMVariant object of the container data type.</span></span>                                                                                                   |
| <span data-ttu-id="015df-178">public Real currency(\[Real newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-178">public Real currency(\[Real newValue\])</span></span>                                                                   | <span data-ttu-id="015df-179">VT\_CY データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-179">Gets or sets the value of a COMVariant object of the VT\_CY data type.</span></span>                                                                                                      |
| <span data-ttu-id="015df-180">public Date date(\[Date newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-180">public Date date(\[Date newValue\])</span></span>                                                                       | <span data-ttu-id="015df-181">VT\_DATE データ タイプの COMVariant オブジェクトの値の日付部分を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-181">Gets or sets the date part of the value of a COMVariant object of the VT\_DATE data type.</span></span>                                                                                   |
| <span data-ttu-id="015df-182">public Real decimal(\[Real newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-182">public Real decimal(\[Real newValue\])</span></span>                                                                    | <span data-ttu-id="015df-183">VT\_DECIMAL データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-183">Gets or sets the value of a COMVariant object of the VT\_DECIMAL data type.</span></span>                                                                                                 |
| <span data-ttu-id="015df-184">public Real double(\[Real newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-184">public Real double(\[Real newValue\])</span></span>                                                                     | <span data-ttu-id="015df-185">VT\_R8 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-185">Gets or sets the value of a COMVariant object of the VT\_R8 data type.</span></span>                                                                                                      |
| <span data-ttu-id="015df-186">public Real float(\[Real newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-186">public Real float(\[Real newValue\])</span></span>                                                                      | <span data-ttu-id="015df-187">VT\_R4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-187">Gets or sets the value of a COMVariant object of the VT\_R4 data type.</span></span>                                                                                                      |
| <span data-ttu-id="015df-188">public ComInterface iDispatch(\[ComInterface newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-188">public ComInterface iDispatch(\[ComInterface newValue\])</span></span>                                                  | <span data-ttu-id="015df-189">VT\_DISPATCH データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-189">Gets or sets the value of a COMVariant object of the VT\_DISPATCH data type.</span></span>                                                                                                |
| <span data-ttu-id="015df-190">public int int(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-190">public int int(\[int newValue\])</span></span>                                                                          | <span data-ttu-id="015df-191">VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-191">Gets or sets the value of a COMVariant object of the VT\_I4 data type.</span></span>                                                                                                      |
| <span data-ttu-id="015df-192">public ComInterface iUnknown(\[ComInterface newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-192">public ComInterface iUnknown(\[ComInterface newValue\])</span></span>                                                   | <span data-ttu-id="015df-193">VT\_UNKNOWN (IUnknown) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-193">Gets or sets the value of a COMVariant object of the VT\_UNKNOWN (IUnknown) data type.</span></span>                                                                                      |
| <span data-ttu-id="015df-194">public int long(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-194">public int long(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="015df-195">VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-195">Gets or sets the value of a COMVariant object of the VT\_I4 data type.</span></span>                                                                                                      |
| <span data-ttu-id="015df-196">public Int64 longLong(\[Int64 newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-196">public Int64 longLong(\[Int64 newValue\])</span></span>                                                                 | <span data-ttu-id="015df-197">VT\_I8 (longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-197">Gets or sets the value of a COMVariant object of the VT\_I8 (longlong) data type.</span></span>                                                                                           |
| <span data-ttu-id="015df-198">public Array safeArray(\[Array newValue\], \[COMVariantType newType\])</span><span class="sxs-lookup"><span data-stu-id="015df-198">public Array safeArray(\[Array newValue\], \[COMVariantType newType\])</span></span>                                    | <span data-ttu-id="015df-199">VT\_SAFEARRAY データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-199">Gets or sets the value of a COMVariant object of the VT\_SAFEARRAY data type.</span></span>                                                                                               |
| <span data-ttu-id="015df-200">public int sCode(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-200">public int sCode(\[int newValue\])</span></span>                                                                        | <span data-ttu-id="015df-201">VT\_ERROR データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-201">Gets or sets the value of a COMVariant object of the VT\_ERROR data type.</span></span>                                                                                                   |
| <span data-ttu-id="015df-202">public int short(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-202">public int short(\[int newValue\])</span></span>                                                                        | <span data-ttu-id="015df-203">VT\_I2 (短い) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-203">Gets or sets the value of a COMVariant object of the VT\_I2 (short) data type.</span></span>                                                                                              |
| <span data-ttu-id="015df-204">public int time(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-204">public int time(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="015df-205">VT\_DATE データ タイプの COMVariant オブジェクトの値の時刻部分を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-205">Gets or sets the time part of the value of a COMVariant object of the VT\_DATE data type.</span></span>                                                                                   |
| <span data-ttu-id="015df-206">public str toString()</span><span class="sxs-lookup"><span data-stu-id="015df-206">public str toString()</span></span>                                                                                     | <span data-ttu-id="015df-207">COMVariant オブジェクトの文字列形式を作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-207">Creates a string representation of a COMVariant object.</span></span> <span data-ttu-id="015df-208">この文字列形式には、オブジェクトの値と型が含まれます。</span><span class="sxs-lookup"><span data-stu-id="015df-208">This string representation includes the value and type of the object.</span></span>                                               |
| <span data-ttu-id="015df-209">public int uInt(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-209">public int uInt(\[int newValue\])</span></span>                                                                         | <span data-ttu-id="015df-210">VT\_UI4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-210">Gets or sets the value of a COMVariant object of the VT\_UI4 data type.</span></span>                                                                                                     |
| <span data-ttu-id="015df-211">public int uLong(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-211">public int uLong(\[int newValue\])</span></span>                                                                        | <span data-ttu-id="015df-212">VT\_UI4 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-212">Gets or sets the value of a COMVariant object of the VT\_UI4 (unsigned long) data type.</span></span>                                                                                     |
| <span data-ttu-id="015df-213">public Int64 uLongLong(\[Int64 newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-213">public Int64 uLongLong(\[Int64 newValue\])</span></span>                                                                | <span data-ttu-id="015df-214">VT\_UI8 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-214">Gets or sets the value of a COMVariant object of the VT\_UI8 (unsigned longlong) data type.</span></span>                                                                                 |
| <span data-ttu-id="015df-215">public int uShort(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-215">public int uShort(\[int newValue\])</span></span>                                                                       | <span data-ttu-id="015df-216">VT\_UI2 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-216">Gets or sets the value of a COMVariant object of the VT\_UI2 data type.</span></span>                                                                                                     |
| <span data-ttu-id="015df-217">public COMVariant variant(\[COMVariant newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-217">public COMVariant variant(\[COMVariant newValue\])</span></span>                                                        | <span data-ttu-id="015df-218">VT\_VARIANT (バリアント) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-218">Gets or sets the value of a COMVariant object of the VT\_VARIANT (variant) data type.</span></span>                                                                                       |
| <span data-ttu-id="015df-219">public COMVariantInOut variantInOutFlag(\[COMVariantInOut newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-219">public COMVariantInOut variantInOutFlag(\[COMVariantInOut newValue\])</span></span>                                     | <span data-ttu-id="015df-220">COMVariant オブジェクトに対する InOutFlag 設定を設定する返します。</span><span class="sxs-lookup"><span data-stu-id="015df-220">Sets or returns the InOutFlag setting for a COMVariant object.</span></span>                                                                                                              |
| <span data-ttu-id="015df-221">public COMVariantType variantType(\[COMVariantType newValue\])</span><span class="sxs-lookup"><span data-stu-id="015df-221">public COMVariantType variantType(\[COMVariantType newValue\])</span></span>                                            | <span data-ttu-id="015df-222">COMVariant オブジェクトにそのバリアント データ型を照会するか、データ型を変更します。</span><span class="sxs-lookup"><span data-stu-id="015df-222">Queries a COMVariant object for its variant data type or changes the data type.</span></span>                                                                                             |
| <span data-ttu-id="015df-223">::public static COMVariant createDateFromYMD(int year, int month, int day, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-223">::public static COMVariant createDateFromYMD(int year, int month, int day, \[COMVariantInOut inOutFlag\])</span></span> | <span data-ttu-id="015df-224">新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-224">Creates a new COMVariant object and initializes it with a date value in one operation.</span></span>                                                                                      |
| <span data-ttu-id="015df-225">::public static COMVariant createFromArray(Array value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-225">::public static COMVariant createFromArray(Array value, \[COMVariantInOut inOutFlag\])</span></span>                    | <span data-ttu-id="015df-226">新しい COMVariant オブジェクトを作成し、1 回の操作で配列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-226">Creates a new COMVariant object and initializes it with an array in one operation.</span></span>                                                                                          |
| <span data-ttu-id="015df-227">::public static COMVariant createFromBoolean(boolean value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-227">::public static COMVariant createFromBoolean(boolean value, \[COMVariantInOut inOutFlag\])</span></span>                | <span data-ttu-id="015df-228">新しい COMVariant オブジェクトを作成し、1 回の操作でブール値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-228">Creates a new COMVariant object and initializes it with a Boolean value in one operation.</span></span>                                                                                   |
| <span data-ttu-id="015df-229">::public static COMVariant createFromCOM(COM value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-229">::public static COMVariant createFromCOM(COM value, \[COMVariantInOut inOutFlag\])</span></span>                        | <span data-ttu-id="015df-230">新しい COMVariant オブジェクトを作成し、1 回の操作で COM クラスで初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-230">Creates a new COMVariant object and initializes it with a COM class in one operation.</span></span>                                                                                       |
| <span data-ttu-id="015df-231">::public static COMVariant createFromDate(Date value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-231">::public static COMVariant createFromDate(Date value, \[COMVariantInOut inOutFlag\])</span></span>                      | <span data-ttu-id="015df-232">新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-232">Creates a new COMVariant object and initializes it with a date value in one operation.</span></span>                                                                                      |
| <span data-ttu-id="015df-233">::public static COMVariant createFromDateAndTime(Date date, int time, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-233">::public static COMVariant createFromDateAndTime(Date date, int time, \[COMVariantInOut inOutFlag\])</span></span>      | <span data-ttu-id="015df-234">新しい COMVariant オブジェクトを作成し、1 回の操作で日時で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-234">Creates a new COMVariant object and initializes it with a date and time in one operation.</span></span>                                                                                   |
| <span data-ttu-id="015df-235">::public static COMVariant createFromInt(int value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-235">::public static COMVariant createFromInt(int value, \[COMVariantInOut inOutFlag\])</span></span>                        | <span data-ttu-id="015df-236">新しい COMVariant オブジェクトを作成し、1 回の操作で整数値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-236">Creates a new COMVariant object and initializes it with an integer value in one operation.</span></span>                                                                                  |
| <span data-ttu-id="015df-237">::public static COMVariant createFromInt64(Int64 value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-237">::public static COMVariant createFromInt64(Int64 value, \[COMVariantInOut inOutFlag\])</span></span>                    | <span data-ttu-id="015df-238">新しい COMVariant オブジェクトを作成し、1 回の操作でint64 値 (longLong や uLongLong) で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-238">Creates a new COMVariant object and initializes it with an int64 value (longLong or uLongLong) in one operation.</span></span>                                                            |
| <span data-ttu-id="015df-239">::public static COMVariant createFromReal(Real value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-239">::public static COMVariant createFromReal(Real value, \[COMVariantInOut inOutFlag\])</span></span>                      | <span data-ttu-id="015df-240">新しい COMVariant オブジェクトを作成し、1 回の操作で実際の値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-240">Creates a new COMVariant object and initializes it with a real value in one operation.</span></span>                                                                                      |
| <span data-ttu-id="015df-241">::public static COMVariant createFromStr(str value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-241">::public static COMVariant createFromStr(str value, \[COMVariantInOut inOutFlag\])</span></span>                        | <span data-ttu-id="015df-242">新しい COMVariant オブジェクトを作成し、1 回の操作で文字列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-242">Creates a new COMVariant object and initializes it with a string in one operation.</span></span>                                                                                          |
| <span data-ttu-id="015df-243">::public static COMVariant createFromTime(int value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-243">::public static COMVariant createFromTime(int value, \[COMVariantInOut inOutFlag\])</span></span>                       | <span data-ttu-id="015df-244">新しい COMVariant オブジェクトを作成し、1 回の操作で時刻値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-244">Creates a new COMVariant object and initializes it with a time value in one operation.</span></span>                                                                                      |
| <span data-ttu-id="015df-245">::public static COMVariant createFromUtcDateTime(DateTime value, \[COMVariantInOut inOutFlag\])</span><span class="sxs-lookup"><span data-stu-id="015df-245">::public static COMVariant createFromUtcDateTime(DateTime value, \[COMVariantInOut inOutFlag\])</span></span>           |                                                                                                                                                                             |
| <span data-ttu-id="015df-246">::public static COMVariant createNoValue()</span><span class="sxs-lookup"><span data-stu-id="015df-246">::public static COMVariant createNoValue()</span></span>                                                                | <span data-ttu-id="015df-247">値を持たない VT\_エラー バリアント タイプの COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-247">Creates a COMVariant object of the VT\_ERROR variant type with no value.</span></span>                                                                                                    |
| <span data-ttu-id="015df-248">public void new(\[COMVariantInOut inOutFlag\], \[COMVariantType type\])</span><span class="sxs-lookup"><span data-stu-id="015df-248">public void new(\[COMVariantInOut inOutFlag\], \[COMVariantType type\])</span></span>                                   | <span data-ttu-id="015df-249">COM オートメーション オブジェクトのメソッドまたはプロパティに引数を渡すために使用できる COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-249">Creates a COMVariant object that can be used to pass arguments to the methods or properties of a COM Automation object.</span></span>                                                     |
| <span data-ttu-id="015df-250">public void noValue()</span><span class="sxs-lookup"><span data-stu-id="015df-250">public void noValue()</span></span>                                                                                     | <span data-ttu-id="015df-251">既存の COMVariant オブジェクトの内容を削除し、COMDispFunction.call メソッドまたは COM クラスで使用されている場合は、未指定の引数として機能させることができます。</span><span class="sxs-lookup"><span data-stu-id="015df-251">Deletes the contents of an existing COMVariant object and enables it to act as an unspecified argument when it is used in the COMDispFunction.call method or the COM class.</span></span> |
| <span data-ttu-id="015df-252">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="015df-252">public void finalize()</span></span>                                                                                    | <span data-ttu-id="015df-253">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="015df-253">Not implemented.</span></span> <span data-ttu-id="015df-254">明示的にオブジェクトを破棄する必要がある場合は、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="015df-254">You can override this method if you need to explicitly destruct an object.</span></span>                                                                                 |

## <a name="method-boolean"></a><span data-ttu-id="015df-255">メソッド boolean</span><span class="sxs-lookup"><span data-stu-id="015df-255">Method boolean</span></span>

<span data-ttu-id="015df-256">VT\_BOOL データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-256">Gets or sets the value of a COMVariant object of the VT\_BOOL data type.</span></span>

```xpp
public boolean boolean([boolean newValue])
```

### <a name="parameters---boolean"></a><span data-ttu-id="015df-257">パラメーター - boolean</span><span class="sxs-lookup"><span data-stu-id="015df-257">Parameters - boolean</span></span>

<span data-ttu-id="015df-258">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-258">newValue</span></span>  
<span data-ttu-id="015df-259">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-259">The new value; optional.</span></span>

### <a name="return-value---boolean"></a><span data-ttu-id="015df-260">戻り値 - boolean</span><span class="sxs-lookup"><span data-stu-id="015df-260">Return Value - boolean</span></span>

<span data-ttu-id="015df-261">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-261">The current value.</span></span>

### <a name="remarks---boolean"></a><span data-ttu-id="015df-262">備考 - boolean</span><span class="sxs-lookup"><span data-stu-id="015df-262">Remarks - boolean</span></span>

<span data-ttu-id="015df-263">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-263">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-264">データ型が COMVariantType::VT\_BOOL に設定されている場合、その COMVariant オブジェクトはブール型です。</span><span class="sxs-lookup"><span data-stu-id="015df-264">A COMVariant object has a Boolean type if its data type is set to COMVariantType::VT\_BOOL.</span></span> <span data-ttu-id="015df-265">COM ブール値のデータ型は、"VARIANT\_BOOL" とも呼ばれることがあります。</span><span class="sxs-lookup"><span data-stu-id="015df-265">The COM Boolean data type may also be referred to as "VARIANT\_BOOL".</span></span>

### <a name="examples---boolean"></a><span data-ttu-id="015df-266">例 - boolean</span><span class="sxs-lookup"><span data-stu-id="015df-266">Examples - boolean</span></span>

<span data-ttu-id="015df-267">次の例では、VT\_BOOL 型の新しい COMVariant オブジェクトを作成し、値を true に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-267">The following example creates a new COMVariant object of type VT\_BOOL and sets the value to true.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_BOOL); 
```

```xpp
    // Set value of the object 
    var.boolean(true); 
}
```

## <a name="method-bstr"></a><span data-ttu-id="015df-268">メソッド bStr</span><span class="sxs-lookup"><span data-stu-id="015df-268">Method bStr</span></span>

<span data-ttu-id="015df-269">VT\_BSTR データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-269">Gets or sets the value of a COMVariant object of the VT\_BSTR data type.</span></span>

```xpp
public str bStr([str newValue])
```

### <a name="parameters---bstr"></a><span data-ttu-id="015df-270">パラメーター - bStr</span><span class="sxs-lookup"><span data-stu-id="015df-270">Parameters - bStr</span></span>

<span data-ttu-id="015df-271">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-271">newValue</span></span>  
<span data-ttu-id="015df-272">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-272">The new value; optional.</span></span>

### <a name="return-value---bstr"></a><span data-ttu-id="015df-273">戻り値 - bStr</span><span class="sxs-lookup"><span data-stu-id="015df-273">Return Value - bStr</span></span>

<span data-ttu-id="015df-274">現在の文字列の価値。</span><span class="sxs-lookup"><span data-stu-id="015df-274">The current string value.</span></span>

### <a name="remarks---bstr"></a><span data-ttu-id="015df-275">備考 - bStr</span><span class="sxs-lookup"><span data-stu-id="015df-275">Remarks - bStr</span></span>

<span data-ttu-id="015df-276">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-276">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-277">データ型が COMVariantType::VT\_BSTR に設定されている場合、その COMVariant オブジェクトは文字列データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-277">A COMVariant object has a string data type if its data type is set to COMVariantType::VT\_BSTR.</span></span> <span data-ttu-id="015df-278">BStr データ型は、文字列の処理に使用される COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-278">The BStr data type is a COM data type that is used for handling strings.</span></span>

### <a name="examples---bstr"></a><span data-ttu-id="015df-279">例 - bStr</span><span class="sxs-lookup"><span data-stu-id="015df-279">Examples - bStr</span></span>

<span data-ttu-id="015df-280">次の例では、VT\_BSTR 型の新しい COMVariant オブジェクトを作成し、値を "Hello World" に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-280">The following example creates a new COMVariant object of type VT\_BSTR, and sets the value to "Hello World."</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_BSTR); 
```

```xpp
    // Set string value of the object 
    var.bStr("Hello World"); 
}
```

## <a name="method-byte"></a><span data-ttu-id="015df-281">メソッド byte</span><span class="sxs-lookup"><span data-stu-id="015df-281">Method byte</span></span>

<span data-ttu-id="015df-282">VT\_UI1 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-282">Gets or sets the value of a COMVariant object of the VT\_UI1 data type.</span></span>

```xpp
public int byte([int newValue])
```

### <a name="parameters---byte"></a><span data-ttu-id="015df-283">パラメーター - byte</span><span class="sxs-lookup"><span data-stu-id="015df-283">Parameters - byte</span></span>

<span data-ttu-id="015df-284">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-284">newValue</span></span>  
<span data-ttu-id="015df-285">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-285">The new value; optional.</span></span>

### <a name="return-value---byte"></a><span data-ttu-id="015df-286">戻り値 - byte</span><span class="sxs-lookup"><span data-stu-id="015df-286">Return Value - byte</span></span>

<span data-ttu-id="015df-287">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-287">The current value.</span></span>

### <a name="remarks---byte"></a><span data-ttu-id="015df-288">備考 - byte</span><span class="sxs-lookup"><span data-stu-id="015df-288">Remarks - byte</span></span>

<span data-ttu-id="015df-289">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-289">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-290">データ型が COMVariantType::VT\_UI1 に設定されている場合、その COMVariant オブジェクトは byte データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-290">A COMVariant object has a byte data type if its data type is set to COMVariantType::VT\_UI1.</span></span> <span data-ttu-id="015df-291">また、「符号なし文字型」を使用して COM バイト データ型を参照することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-291">You can also use "unsigned char" to refer to the COM byte data type.</span></span>

### <a name="examples---byte"></a><span data-ttu-id="015df-292">例 - byte</span><span class="sxs-lookup"><span data-stu-id="015df-292">Examples - byte</span></span>

<span data-ttu-id="015df-293">次の例では、VT\_UI1 型の新しい COMVariant オブジェクトを作成し、値を 123 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-293">The following example creates a new COMVariant object of the VT\_UI1 type and sets the value to 123.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UI1); 
```

```xpp
    // Set value of the object 
    var.byte(123); 
}
```

## <a name="method-char"></a><span data-ttu-id="015df-294">メソッド char</span><span class="sxs-lookup"><span data-stu-id="015df-294">Method char</span></span>

<span data-ttu-id="015df-295">VT\_I1 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-295">Gets or sets the value of a COMVariant object of the VT\_I1 data type.</span></span>

```xpp
public int char([int newValue])
```

### <a name="parameters---char"></a><span data-ttu-id="015df-296">パラメーター - char</span><span class="sxs-lookup"><span data-stu-id="015df-296">Parameters - char</span></span>

<span data-ttu-id="015df-297">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-297">newValue</span></span>  
<span data-ttu-id="015df-298">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-298">The new value; optional.</span></span>

### <a name="return-value---char"></a><span data-ttu-id="015df-299">戻り値 - char</span><span class="sxs-lookup"><span data-stu-id="015df-299">Return Value - char</span></span>

<span data-ttu-id="015df-300">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-300">The current value.</span></span>

### <a name="remarks---char"></a><span data-ttu-id="015df-301">備考 - char</span><span class="sxs-lookup"><span data-stu-id="015df-301">Remarks - char</span></span>

<span data-ttu-id="015df-302">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-302">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-303">データ型が COMVariantType::VT\_I1 に設定されている場合、その COMVariant オブジェクトは char データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-303">A COMVariant object has a char data type if its data type is set to COMVariantType::VT\_I1.</span></span>

### <a name="examples---char"></a><span data-ttu-id="015df-304">例 - char</span><span class="sxs-lookup"><span data-stu-id="015df-304">Examples - char</span></span>

<span data-ttu-id="015df-305">次の例では、VT\_I1 型の 新しい COMVariant オブジェクトを作成し、値を 65 の、A の数値に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-305">The following example creates a new COMVariant object of type VT\_I1 and sets the value to the numeric value of A, which is 65.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I1); 
```

```xpp
    // Set value of the object 
    var.char(Char2Num("A", 1)); 
}
```

## <a name="method-container"></a><span data-ttu-id="015df-306">メソッド container</span><span class="sxs-lookup"><span data-stu-id="015df-306">Method container</span></span>

<span data-ttu-id="015df-307">コンテナ データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-307">Gets or sets the value of a COMVariant object of the container data type.</span></span>

```xpp
public container container([container newValue], [COMVariantType newType])
```

### <a name="parameters---container"></a><span data-ttu-id="015df-308">パラメーター - container</span><span class="sxs-lookup"><span data-stu-id="015df-308">Parameters - container</span></span>

<span data-ttu-id="015df-309">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-309">newValue</span></span>  
<span data-ttu-id="015df-310">新しいコンテナーのタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-310">The type of the new container; optional.</span></span> <span data-ttu-id="015df-311">既定では、コンテナーが整数を格納します。</span><span class="sxs-lookup"><span data-stu-id="015df-311">The default is for the container to store integers.</span></span>

<!-- -->

<span data-ttu-id="015df-312">newType</span><span class="sxs-lookup"><span data-stu-id="015df-312">newType</span></span>  
<span data-ttu-id="015df-313">新しいコンテナーのタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-313">The type of the new container; optional.</span></span> <span data-ttu-id="015df-314">既定では、コンテナーが整数を格納します。</span><span class="sxs-lookup"><span data-stu-id="015df-314">The default is for the container to store integers.</span></span>

### <a name="return-value---container"></a><span data-ttu-id="015df-315">戻り値 - container</span><span class="sxs-lookup"><span data-stu-id="015df-315">Return Value - container</span></span>

<span data-ttu-id="015df-316">現在のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="015df-316">The current container.</span></span>

### <a name="remarks---container"></a><span data-ttu-id="015df-317">備考 - container</span><span class="sxs-lookup"><span data-stu-id="015df-317">Remarks - container</span></span>

<span data-ttu-id="015df-318">newType パラメーターの使用可能な値は、COMVariantType システム列挙によって提供される値のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="015df-318">The possible values for the newType parameter are a subset of the values that are supplied by the COMVariantType system enum:</span></span>

-   <span data-ttu-id="015df-319">VT\_I2</span><span class="sxs-lookup"><span data-stu-id="015df-319">VT\_I2</span></span>
-   <span data-ttu-id="015df-320">VT\_I4</span><span class="sxs-lookup"><span data-stu-id="015df-320">VT\_I4</span></span>
-   <span data-ttu-id="015df-321">VT\_R4</span><span class="sxs-lookup"><span data-stu-id="015df-321">VT\_R4</span></span>
-   <span data-ttu-id="015df-322">VT\_R8</span><span class="sxs-lookup"><span data-stu-id="015df-322">VT\_R8</span></span>
-   <span data-ttu-id="015df-323">VT\_CY</span><span class="sxs-lookup"><span data-stu-id="015df-323">VT\_CY</span></span>
-   <span data-ttu-id="015df-324">VT\_DATE</span><span class="sxs-lookup"><span data-stu-id="015df-324">VT\_DATE</span></span>
-   <span data-ttu-id="015df-325">VT\_BSTR</span><span class="sxs-lookup"><span data-stu-id="015df-325">VT\_BSTR</span></span>
-   <span data-ttu-id="015df-326">VT\_ERROR</span><span class="sxs-lookup"><span data-stu-id="015df-326">VT\_ERROR</span></span>
-   <span data-ttu-id="015df-327">VT\_BOOL</span><span class="sxs-lookup"><span data-stu-id="015df-327">VT\_BOOL</span></span>
-   <span data-ttu-id="015df-328">VT\_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="015df-328">VT\_DECIMAL</span></span>
-   <span data-ttu-id="015df-329">VT\_I1</span><span class="sxs-lookup"><span data-stu-id="015df-329">VT\_I1</span></span>
-   <span data-ttu-id="015df-330">VT\_UI1</span><span class="sxs-lookup"><span data-stu-id="015df-330">VT\_UI1</span></span>
-   <span data-ttu-id="015df-331">VT\_UI2</span><span class="sxs-lookup"><span data-stu-id="015df-331">VT\_UI2</span></span>
-   <span data-ttu-id="015df-332">VT\_UI4</span><span class="sxs-lookup"><span data-stu-id="015df-332">VT\_UI4</span></span>
-   <span data-ttu-id="015df-333">VT\_I8</span><span class="sxs-lookup"><span data-stu-id="015df-333">VT\_I8</span></span>
-   <span data-ttu-id="015df-334">VT\_UI8</span><span class="sxs-lookup"><span data-stu-id="015df-334">VT\_UI8</span></span>
-   <span data-ttu-id="015df-335">VT\_INT</span><span class="sxs-lookup"><span data-stu-id="015df-335">VT\_INT</span></span>
-   <span data-ttu-id="015df-336">VT\_UINT</span><span class="sxs-lookup"><span data-stu-id="015df-336">VT\_UINT</span></span>

<span data-ttu-id="015df-337">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-337">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-338">コンテナーが COMVariant オブジェクトに保存されると、コンテナーのバイナリ表現がバイナリ配列に保存されます (COMVariant.safeArray メソッドを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="015df-338">When a container is stored in a COMVariant object, the binary representation of the container is stored in a binary array (see the COMVariant.safeArray method).</span></span> <span data-ttu-id="015df-339">コンテナーのプロパティは、データベース COM オブジェクトにデータを格納し、後でデータを処理する COM オブジェクトを使用せずに Finance and Operations アプリケーションにデータを読み戻す必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="015df-339">The container property is useful when you need to store data in a database COM object and then later read the data back into a Finance and Operations application without the COM object processing the data.</span></span> <span data-ttu-id="015df-340">コンテナーのプロパティは、COMVariant クラスの高度なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="015df-340">The container property is an advanced property of the COMVariant class.</span></span> <span data-ttu-id="015df-341">COMVariant オブジェクト内で、コンテナーが格納されるバイナリ配列の内容は、どの COM オブジェクトによっても変更されないようにしなければならないため、注意して使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="015df-341">It should be used with caution because the content of the binary array that the container is stored in, inside the COMVariant object, must not be changed by any COM object.</span></span>

### <a name="examples---container"></a><span data-ttu-id="015df-342">例 - container</span><span class="sxs-lookup"><span data-stu-id="015df-342">Examples - container</span></span>

<span data-ttu-id="015df-343">次の例では、コンテナー 型の新しい COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-343">The following example creates a new COMVariant object of type container.</span></span> <span data-ttu-id="015df-344">コンテナー内のデータは、データベース COM オブジェクトに渡され、データベース COM オブジェクトによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-344">The data in the container is passed to, and used by, a database COM object.</span></span> <span data-ttu-id="015df-345">注記: 次のセクションのコードには仮想 COM オブジェクト (MyDatabaseCOM.Object) が含まれており、Finance and Operations アプリケーションの外部でオブジェクトが作成されていない限り実行されません。</span><span class="sxs-lookup"><span data-stu-id="015df-345">Note The code in the following section contains a hypothetical COM object MyDatabaseCOM.Object" and will therefore not run, unless such an object is created outside a Finance and Operations application.</span></span>

```xpp
{ 
    COM com; 
    COMVariant var = new COMVariant(); 
    container con; 
    InteropPermission perm; 
```

```xpp
    // Set code access permission to help protect use of COM object 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    // Permission scope starts here 
    perm.assert(); 
```

```xpp
    // Put some data in the container 
    con = conins(con, 1, "Element 1"); 
    con = conins(con, 2, "Element 2"); 
    // Set value of the object and ensure the data 
    // is stored in a binary array of bytes 
    var.container(con, COMVariantType::VT_UI1); 
```

```xpp
    // Create a database object to store the data in 
    com = new COM("MyDatabaseCOM.Object"); 
    com.writeData(var); 
    // ... 
```

```xpp
    // Close code access permission 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-currency"></a><span data-ttu-id="015df-346">メソッド currency</span><span class="sxs-lookup"><span data-stu-id="015df-346">Method currency</span></span>

<span data-ttu-id="015df-347">VT\_CY データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-347">Gets or sets the value of a COMVariant object of the VT\_CY data type.</span></span>

```xpp
public Real currency([Real newValue])
```

### <a name="parameters---currency"></a><span data-ttu-id="015df-348">パラメーター - currency</span><span class="sxs-lookup"><span data-stu-id="015df-348">Parameters - currency</span></span>

<span data-ttu-id="015df-349">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-349">newValue</span></span>  
<span data-ttu-id="015df-350">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-350">The new value; optional.</span></span>

### <a name="return-value---currency"></a><span data-ttu-id="015df-351">戻り値 - currency</span><span class="sxs-lookup"><span data-stu-id="015df-351">Return Value - currency</span></span>

<span data-ttu-id="015df-352">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-352">The current value.</span></span>

### <a name="remarks---currency"></a><span data-ttu-id="015df-353">備考 - currency</span><span class="sxs-lookup"><span data-stu-id="015df-353">Remarks - currency</span></span>

<span data-ttu-id="015df-354">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-354">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-355">データ型が COMVariantType::VT\_CY に設定されている場合、その COMVariant オブジェクトは通貨データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-355">A COMVariant object has a currency data type if its data type is set to COMVariantType::VT\_CY.</span></span> <span data-ttu-id="015df-356">通貨データ型は、通貨値に最適化された COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-356">The currency data type is a COM data type that is optimized for currency values.</span></span> <span data-ttu-id="015df-357">小数点以下 4 桁のある実数です。</span><span class="sxs-lookup"><span data-stu-id="015df-357">It is a real number with four decimal places.</span></span> <span data-ttu-id="015df-358">場合によっては、COM 通貨データ型を参照するために "CY" も使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-358">Sometimes "CY" is also used to refer to the COM currency data type.</span></span>

### <a name="examples---currency"></a><span data-ttu-id="015df-359">例 - currency</span><span class="sxs-lookup"><span data-stu-id="015df-359">Examples - currency</span></span>

<span data-ttu-id="015df-360">次の例では、VT\_CY 型の新しい COMVariant オブジェクトを作成し、値を 123.4567 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-360">The following example creates a new COMVariant object of type VT\_CY and sets the value to 123.4567.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_CY); 
```

```xpp
    // Set value of the object 
    var.currency(123.4567); 
}
```

## <a name="method-date"></a><span data-ttu-id="015df-361">メソッド date</span><span class="sxs-lookup"><span data-stu-id="015df-361">Method date</span></span>

<span data-ttu-id="015df-362">VT\_DATE データ タイプの COMVariant オブジェクトの値の日付部分を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-362">Gets or sets the date part of the value of a COMVariant object of the VT\_DATE data type.</span></span>

```xpp
public Date date([Date newValue])
```

### <a name="parameters---date"></a><span data-ttu-id="015df-363">パラメーター - date</span><span class="sxs-lookup"><span data-stu-id="015df-363">Parameters - date</span></span>

<span data-ttu-id="015df-364">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-364">newValue</span></span>  
<span data-ttu-id="015df-365">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-365">The new value; optional.</span></span>

### <a name="return-value---date"></a><span data-ttu-id="015df-366">戻り値 - date</span><span class="sxs-lookup"><span data-stu-id="015df-366">Return Value - date</span></span>

<span data-ttu-id="015df-367">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-367">The current value.</span></span>

### <a name="remarks---date"></a><span data-ttu-id="015df-368">備考 - date</span><span class="sxs-lookup"><span data-stu-id="015df-368">Remarks - date</span></span>

<span data-ttu-id="015df-369">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-369">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-370">データ型が COMVariantType::VT\_DATE に設定されている場合、その COMVariant オブジェクトは日時データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-370">A COMVariant object has a date and time data type if its data type is set to COMVariantType::VT\_DATE.</span></span> <span data-ttu-id="015df-371">オブジェクトの値を設定するとき、日付に加えて、値の時刻の部分を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="015df-371">When you set the value of the object, you must set the time part of the value in addition to the date.</span></span> <span data-ttu-id="015df-372">値の時間部分を設定するには、time プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="015df-372">To set the time part of the value, use the time property.</span></span>

### <a name="examples---date"></a><span data-ttu-id="015df-373">例 - date</span><span class="sxs-lookup"><span data-stu-id="015df-373">Examples - date</span></span>

<span data-ttu-id="015df-374">次の例では、VT\_DATE 型の COMVariant オブジェクトを作成し、値の日付部分を 1998 年 12 月 24 日に設定し、時刻の部分を 13.24 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-374">The following example creates a COMVariant object of type VT\_DATE and sets the date part of the value to 24 December 1998, and the time part of the value to 13.24.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_DATE); 
```

```xpp
    // Set value of the object 
    var.date(Str2Date("12.24.1998", 213)); 
    var.time(Str2Time("13:24:00")); 
}
```

## <a name="method-decimal"></a><span data-ttu-id="015df-375">メソッド decimal</span><span class="sxs-lookup"><span data-stu-id="015df-375">Method decimal</span></span>

<span data-ttu-id="015df-376">VT\_DECIMAL データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-376">Gets or sets the value of a COMVariant object of the VT\_DECIMAL data type.</span></span>

```xpp
public Real decimal([Real newValue])
```

### <a name="parameters---decimal"></a><span data-ttu-id="015df-377">パラメーター - decimal</span><span class="sxs-lookup"><span data-stu-id="015df-377">Parameters - decimal</span></span>

<span data-ttu-id="015df-378">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-378">newValue</span></span>  
<span data-ttu-id="015df-379">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-379">The new value; optional.</span></span>

### <a name="return-value---decimal"></a><span data-ttu-id="015df-380">戻り値 - decimal</span><span class="sxs-lookup"><span data-stu-id="015df-380">Return Value - decimal</span></span>

<span data-ttu-id="015df-381">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-381">The current value.</span></span>

### <a name="remarks---decimal"></a><span data-ttu-id="015df-382">備考 - decimal</span><span class="sxs-lookup"><span data-stu-id="015df-382">Remarks - decimal</span></span>

<span data-ttu-id="015df-383">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-383">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-384">データ型が COMVariantType::VT\_DECIMAL に設定されている場合、その COMVariant オブジェクトは 10 進型です。</span><span class="sxs-lookup"><span data-stu-id="015df-384">A COMVariant object has a decimal type if its data type is set to COMVariantType::VT\_DECIMAL.</span></span> <span data-ttu-id="015df-385">10進データ型は、数値のサイズとスケールを提供する COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-385">The decimal data type is a COM data type that provides size and scale for a number.</span></span> <span data-ttu-id="015df-386">X++ には 10 進データ型と並行するものはありません。</span><span class="sxs-lookup"><span data-stu-id="015df-386">There is no parallel to the decimal data type in X++.</span></span>

### <a name="examples---decimal"></a><span data-ttu-id="015df-387">例 - decimal</span><span class="sxs-lookup"><span data-stu-id="015df-387">Examples - decimal</span></span>

<span data-ttu-id="015df-388">次の例では、VT\_DECIMAL 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-388">The following example creates a new COMVariant object of type VT\_DECIMAL and sets the value to 123.456.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_DECIMAL); 
```

```xpp
    // Set value of the object 
    var.decimal(123.456); 
}
```

## <a name="method-double"></a><span data-ttu-id="015df-389">メソッド double</span><span class="sxs-lookup"><span data-stu-id="015df-389">Method double</span></span>

<span data-ttu-id="015df-390">VT\_R8 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-390">Gets or sets the value of a COMVariant object of the VT\_R8 data type.</span></span>

```xpp
public Real double([Real newValue])
```

### <a name="parameters---double"></a><span data-ttu-id="015df-391">パラメーター - double</span><span class="sxs-lookup"><span data-stu-id="015df-391">Parameters - double</span></span>

<span data-ttu-id="015df-392">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-392">newValue</span></span>  
<span data-ttu-id="015df-393">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-393">The new value; optional.</span></span>

### <a name="return-value---double"></a><span data-ttu-id="015df-394">戻り値 - double</span><span class="sxs-lookup"><span data-stu-id="015df-394">Return Value - double</span></span>

<span data-ttu-id="015df-395">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-395">The current value.</span></span>

### <a name="remarks---double"></a><span data-ttu-id="015df-396">備考 - double</span><span class="sxs-lookup"><span data-stu-id="015df-396">Remarks - double</span></span>

<span data-ttu-id="015df-397">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-397">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-398">データ型が COMVariantType::VT\_R8 に設定されている場合、その COMVariant オブジェクトは double データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-398">A COMVariant object has a double data type if its data type is set to COMVariantType::VT\_R8.</span></span>

### <a name="examples---double"></a><span data-ttu-id="015df-399">例 - double</span><span class="sxs-lookup"><span data-stu-id="015df-399">Examples - double</span></span>

<span data-ttu-id="015df-400">次の例では、VT\_R8 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-400">The following example creates a new COMVariant object of type VT\_R8 and sets the value to 123.456.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_R8); 
```

```xpp
    // Set value of the object 
    var.double(123.456); 
}
```

## <a name="method-float"></a><span data-ttu-id="015df-401">メソッド float</span><span class="sxs-lookup"><span data-stu-id="015df-401">Method float</span></span>

<span data-ttu-id="015df-402">VT\_R4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-402">Gets or sets the value of a COMVariant object of the VT\_R4 data type.</span></span>

```xpp
public Real float([Real newValue])
```

### <a name="parameters---float"></a><span data-ttu-id="015df-403">パラメーター - float</span><span class="sxs-lookup"><span data-stu-id="015df-403">Parameters - float</span></span>

<span data-ttu-id="015df-404">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-404">newValue</span></span>  
<span data-ttu-id="015df-405">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-405">The new value; optional.</span></span>

### <a name="return-value---float"></a><span data-ttu-id="015df-406">戻り値 - float</span><span class="sxs-lookup"><span data-stu-id="015df-406">Return Value - float</span></span>

<span data-ttu-id="015df-407">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-407">The current value.</span></span>

### <a name="remarks---float"></a><span data-ttu-id="015df-408">備考 - float</span><span class="sxs-lookup"><span data-stu-id="015df-408">Remarks - float</span></span>

<span data-ttu-id="015df-409">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-409">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-410">データ型が COMVariantType::VT\_R4 に設定されている場合、COMVariant オブジェクトは float 型です。</span><span class="sxs-lookup"><span data-stu-id="015df-410">A COMVariant object has a float type if its data type is set to COMVariantType::VT\_R4.</span></span> <span data-ttu-id="015df-411">場合によっては、COM 浮動小数点データ型を参照するために "single" も使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-411">Sometimes "single" is also used to refer to the COM float data type.</span></span>

### <a name="examples---float"></a><span data-ttu-id="015df-412">例 - float</span><span class="sxs-lookup"><span data-stu-id="015df-412">Examples - float</span></span>

<span data-ttu-id="015df-413">次の例では、VT\_R4 型の新しい COMVariant オブジェクトを作成し、値を 123.456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-413">The following example creates a new COMVariant object of type VT\_R4 and sets the value to 123.456.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_R4); 
```

```xpp
    // Set value of the object 
    var.float(123.456); 
}
```

## <a name="method-idispatch"></a><span data-ttu-id="015df-414">メソッド iDispatch</span><span class="sxs-lookup"><span data-stu-id="015df-414">Method iDispatch</span></span>

<span data-ttu-id="015df-415">VT\_DISPATCH データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-415">Gets or sets the value of a COMVariant object of the VT\_DISPATCH data type.</span></span>

```xpp
public ComInterface iDispatch([ComInterface newValue])
```

### <a name="parameters---idispatch"></a><span data-ttu-id="015df-416">パラメーター - iDispatch</span><span class="sxs-lookup"><span data-stu-id="015df-416">Parameters - iDispatch</span></span>

<span data-ttu-id="015df-417">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-417">newValue</span></span>  
<span data-ttu-id="015df-418">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-418">The new value; optional.</span></span>

### <a name="return-value---idispatch"></a><span data-ttu-id="015df-419">戻り値 - iDispatch</span><span class="sxs-lookup"><span data-stu-id="015df-419">Return Value - iDispatch</span></span>

<span data-ttu-id="015df-420">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-420">The current value.</span></span>

### <a name="remarks---idispatch"></a><span data-ttu-id="015df-421">備考 - iDispatch</span><span class="sxs-lookup"><span data-stu-id="015df-421">Remarks - iDispatch</span></span>

<span data-ttu-id="015df-422">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-422">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-423">データ型が COMVariantType::VT\_DISPATCH に設定されている場合、その COMVariant オブジェクトは IDispatch データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-423">A COMVariant object has an IDispatch data type if its data type is set to COMVariantType::VT\_DISPATCH.</span></span> <span data-ttu-id="015df-424">IDispatch データ型は、COM IDispatch インターフェイスへのハンドルを提供する COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-424">The IDispatch data type is a COM data type that provides a handle to a COM IDispatch interface.</span></span>

### <a name="examples---idispatch"></a><span data-ttu-id="015df-425">例 - iDispatch</span><span class="sxs-lookup"><span data-stu-id="015df-425">Examples - iDispatch</span></span>

<span data-ttu-id="015df-426">次の例では、VT\_DISPATCH 型の新しい COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-426">The following example creates a new COMVariant object of type VT\_DISPATCH.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_DISPATCH); 
    COMInterface comInterface; 
```

```xpp
    // Here, the comInterface variable must be assigned 
    // a COM IDispatch interface 
    //� 
```

```xpp
    // Set value of the object 
    var.iDispatch(comInterface); 
}
```

## <a name="method-int"></a><span data-ttu-id="015df-427">メソッド int</span><span class="sxs-lookup"><span data-stu-id="015df-427">Method int</span></span>

<span data-ttu-id="015df-428">VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-428">Gets or sets the value of a COMVariant object of the VT\_I4 data type.</span></span>

```xpp
public int int([int newValue])
```

### <a name="parameters---int"></a><span data-ttu-id="015df-429">パラメーター - int</span><span class="sxs-lookup"><span data-stu-id="015df-429">Parameters - int</span></span>

<span data-ttu-id="015df-430">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-430">newValue</span></span>  
<span data-ttu-id="015df-431">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-431">The new value; optional.</span></span>

### <a name="return-value---int"></a><span data-ttu-id="015df-432">戻り値 - int</span><span class="sxs-lookup"><span data-stu-id="015df-432">Return Value - int</span></span>

<span data-ttu-id="015df-433">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-433">The current value.</span></span>

### <a name="remarks---int"></a><span data-ttu-id="015df-434">備考 - int</span><span class="sxs-lookup"><span data-stu-id="015df-434">Remarks - int</span></span>

<span data-ttu-id="015df-435">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-435">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-436">COMVariantType::VT\_I4 データ型は long バリアント型にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-436">The COMVariantType::VT\_I4 data type is also used for the long variant type.</span></span> <span data-ttu-id="015df-437">COMVariant.long メソッドは、このメソッドと同じです。2 つのメソッドは、完全性のために存在します。</span><span class="sxs-lookup"><span data-stu-id="015df-437">The COMVariant.long method is identical to this method; the two methods exist for completeness.</span></span>

### <a name="examples---int"></a><span data-ttu-id="015df-438">例 - int</span><span class="sxs-lookup"><span data-stu-id="015df-438">Examples - int</span></span>

<span data-ttu-id="015df-439">次の例では、VT\_I4 型の COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-439">The following example creates a COMVariant object of type VT\_I4 and sets the value to 123456.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I4); 
```

```xpp
    // Set value of the object 
    var.int(123456); 
}
```

## <a name="method-iunknown"></a><span data-ttu-id="015df-440">メソッド iUnknown</span><span class="sxs-lookup"><span data-stu-id="015df-440">Method iUnknown</span></span>

<span data-ttu-id="015df-441">VT\_UNKNOWN (IUnknown) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-441">Gets or sets the value of a COMVariant object of the VT\_UNKNOWN (IUnknown) data type.</span></span>

```xpp
public ComInterface iUnknown([ComInterface newValue])
```

### <a name="parameters---iunknown"></a><span data-ttu-id="015df-442">パラメーター - iUnknown</span><span class="sxs-lookup"><span data-stu-id="015df-442">Parameters - iUnknown</span></span>

<span data-ttu-id="015df-443">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-443">newValue</span></span>  
<span data-ttu-id="015df-444">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-444">The new value; optional.</span></span>

### <a name="return-value---iunknown"></a><span data-ttu-id="015df-445">戻り値 - iUnknown</span><span class="sxs-lookup"><span data-stu-id="015df-445">Return Value - iUnknown</span></span>

<span data-ttu-id="015df-446">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-446">The current value.</span></span>

### <a name="remarks---iunknown"></a><span data-ttu-id="015df-447">備考 - iUnknown</span><span class="sxs-lookup"><span data-stu-id="015df-447">Remarks - iUnknown</span></span>

<span data-ttu-id="015df-448">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、データ型の値に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-448">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type value.</span></span> <span data-ttu-id="015df-449">データ型が COMVariantType::VT\_UNKNOWN に設定されている場合、COMVariant オブジェクトは IUnknown データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-449">A COMVariant object has an IUnknown data type if its data type is set to COMVariantType::VT\_UNKNOWN.</span></span> <span data-ttu-id="015df-450">IUnknown データ型は、COM IUnknown インターフェイスへのハンドルを提供する COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-450">The IUnknown data type is a COM data type that provides a handle to a COM IUnknown interface.</span></span>

### <a name="examples---iunknown"></a><span data-ttu-id="015df-451">例 - iUnknown</span><span class="sxs-lookup"><span data-stu-id="015df-451">Examples - iUnknown</span></span>

<span data-ttu-id="015df-452">次の例では、VT\_UNKNOWN 型の新しい COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-452">The following example creates a new COMVariant object of type VT\_UNKNOWN.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UNKNOWN); 
    COMInterface comInterface; 
```

```xpp
    // comInterface variable is assigned 
    // a COM IUnknown interface 
    // ... 
```

```xpp
    // Set value of the object 
    var.iUnknown(comInterface); 
}
```

## <a name="method-long"></a><span data-ttu-id="015df-453">メソッド long</span><span class="sxs-lookup"><span data-stu-id="015df-453">Method long</span></span>

<span data-ttu-id="015df-454">VT\_I4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-454">Gets or sets the value of a COMVariant object of the VT\_I4 data type.</span></span>

```xpp
public int long([int newValue])
```

### <a name="parameters---long"></a><span data-ttu-id="015df-455">パラメーター - long</span><span class="sxs-lookup"><span data-stu-id="015df-455">Parameters - long</span></span>

<span data-ttu-id="015df-456">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-456">newValue</span></span>  
<span data-ttu-id="015df-457">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-457">The new value; optional.</span></span>

### <a name="return-value---long"></a><span data-ttu-id="015df-458">戻り値 - long</span><span class="sxs-lookup"><span data-stu-id="015df-458">Return Value - long</span></span>

<span data-ttu-id="015df-459">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-459">The current value.</span></span>

### <a name="remarks---long"></a><span data-ttu-id="015df-460">備考 - long</span><span class="sxs-lookup"><span data-stu-id="015df-460">Remarks - long</span></span>

<span data-ttu-id="015df-461">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-461">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-462">COMVariantType::VT\_I4 データ型は int バリアント型にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-462">The COMVariantType::VT\_I4 data type is also used for the int variant type.</span></span> <span data-ttu-id="015df-463">COMVariant.int メソッドは、このメソッドと同じです。2 つのメソッドは、完全性のために存在します。</span><span class="sxs-lookup"><span data-stu-id="015df-463">The COMVariant.int method is identical to this method; the two methods exist for completeness.</span></span>

### <a name="examples---long"></a><span data-ttu-id="015df-464">例 - long</span><span class="sxs-lookup"><span data-stu-id="015df-464">Examples - long</span></span>

<span data-ttu-id="015df-465">次の例では、VT\_I4 型の COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-465">The following example creates a COMVariant object of type VT\_I4 and sets the value to 123456.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I4); 
```

```xpp
    // Set value of the object 
    var.long(123456); 
}
```

## <a name="method-longlong"></a><span data-ttu-id="015df-466">メソッド longLong</span><span class="sxs-lookup"><span data-stu-id="015df-466">Method longLong</span></span>

<span data-ttu-id="015df-467">VT\_I8 (longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-467">Gets or sets the value of a COMVariant object of the VT\_I8 (longlong) data type.</span></span>

```xpp
public Int64 longLong([Int64 newValue])
```

### <a name="parameters---longlong"></a><span data-ttu-id="015df-468">パラメーター - longLong</span><span class="sxs-lookup"><span data-stu-id="015df-468">Parameters - longLong</span></span>

<span data-ttu-id="015df-469">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-469">newValue</span></span>  
<span data-ttu-id="015df-470">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-470">The new value; optional.</span></span>

### <a name="return-value---longlong"></a><span data-ttu-id="015df-471">戻り値 - longLong</span><span class="sxs-lookup"><span data-stu-id="015df-471">Return Value - longLong</span></span>

<span data-ttu-id="015df-472">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-472">The current value.</span></span>

### <a name="remarks---longlong"></a><span data-ttu-id="015df-473">備考 - longLong</span><span class="sxs-lookup"><span data-stu-id="015df-473">Remarks - longLong</span></span>

<span data-ttu-id="015df-474">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-474">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the value�s data type.</span></span> <span data-ttu-id="015df-475">データ型が COMVariantType::VT\_I8 に設定されている場合、その COMVariant オブジェクトは longlong バリアント型です。</span><span class="sxs-lookup"><span data-stu-id="015df-475">A COMVariant object has a longlong variant type if its data type is set to COMVariantType::VT\_I8.</span></span>

### <a name="examples---longlong"></a><span data-ttu-id="015df-476">例 - longLong</span><span class="sxs-lookup"><span data-stu-id="015df-476">Examples - longLong</span></span>

<span data-ttu-id="015df-477">次の例では、VT\_I8 型の新しい COMVariant オブジェクトを作成し、値を 2,305,843,009,213,693,952 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-477">The following example creates a new COMVariant object of type VT\_I8 and sets the value to 2,305,843,009,213,693,952.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_BOOL); 
```

```xpp
    // Set value of the object 
    var.longLong(2305843009213693952); 
}
```

## <a name="method-safearray"></a><span data-ttu-id="015df-478">メソッド safeArray</span><span class="sxs-lookup"><span data-stu-id="015df-478">Method safeArray</span></span>

<span data-ttu-id="015df-479">VT\_SAFEARRAY データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-479">Gets or sets the value of a COMVariant object of the VT\_SAFEARRAY data type.</span></span>

```xpp
public Array safeArray([Array newValue], [COMVariantType newType])
```

### <a name="parameters---safearray"></a><span data-ttu-id="015df-480">パラメーター - safeArray</span><span class="sxs-lookup"><span data-stu-id="015df-480">Parameters - safeArray</span></span>

<span data-ttu-id="015df-481">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-481">newValue</span></span>  
<span data-ttu-id="015df-482">新しい配列のタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-482">The type of the new array; optional.</span></span>

<!-- -->

<span data-ttu-id="015df-483">newType</span><span class="sxs-lookup"><span data-stu-id="015df-483">newType</span></span>  
<span data-ttu-id="015df-484">新しい配列のタイプ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-484">The type of the new array; optional.</span></span>

### <a name="return-value---safearray"></a><span data-ttu-id="015df-485">戻り値 - safeArray</span><span class="sxs-lookup"><span data-stu-id="015df-485">Return Value - safeArray</span></span>

<span data-ttu-id="015df-486">現在の配列。</span><span class="sxs-lookup"><span data-stu-id="015df-486">The current array.</span></span>

### <a name="remarks---safearray"></a><span data-ttu-id="015df-487">備考 - safeArray</span><span class="sxs-lookup"><span data-stu-id="015df-487">Remarks - safeArray</span></span>

<span data-ttu-id="015df-488">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-488">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-489">データ型が COMVariantType::VT\_SAFEARRAY に設定されている場合、その COMVariant オブジェクトは配列ブール型です。</span><span class="sxs-lookup"><span data-stu-id="015df-489">A COMVariant object has an array Boolean type if its data type is set to COMVariantType::VT\_SAFEARRAY.</span></span> <span data-ttu-id="015df-490">セーフ配列は、COM の配列に相当します。</span><span class="sxs-lookup"><span data-stu-id="015df-490">A safe array is COM's equivalent to an array.</span></span> <span data-ttu-id="015df-491">現在、1 次元セーフ配列のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="015df-491">Currently only one-dimensional safe arrays are supported.</span></span>

### <a name="examples---safearray"></a><span data-ttu-id="015df-492">例 - safeArray</span><span class="sxs-lookup"><span data-stu-id="015df-492">Examples - safeArray</span></span>

<span data-ttu-id="015df-493">次の例では、VT\_SAFEARRAY 型の新しい COMVariant オブジェクトを作成し、short 配列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-493">The following example creates a new COMVariant object of type VT\_SAFEARRAY and initializes it with an array of shorts.</span></span>

```xpp
{ 
    int i, result; 
    COM com; 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_SAFEARRAY); 
    Array arr = new Array(Types::INTEGER); 
```

```xpp
    // Insert 10 values in the array 
    for (i = 1; i <= 10; i++) 
    { 
        arr.value(i, i); 
    } 
```

```xpp
    // Set value of the object and ensure the integer values 
    // are treated as short data types 
    var.safeArray(arr, COMVariantType::VT_I2); 
}
```

## <a name="method-scode"></a><span data-ttu-id="015df-494">メソッド sCode</span><span class="sxs-lookup"><span data-stu-id="015df-494">Method sCode</span></span>

<span data-ttu-id="015df-495">VT\_ERROR データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-495">Gets or sets the value of a COMVariant object of the VT\_ERROR data type.</span></span>

```xpp
public int sCode([int newValue])
```

### <a name="parameters---scode"></a><span data-ttu-id="015df-496">パラメーター - sCode</span><span class="sxs-lookup"><span data-stu-id="015df-496">Parameters - sCode</span></span>

<span data-ttu-id="015df-497">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-497">newValue</span></span>  
<span data-ttu-id="015df-498">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-498">The new value; optional.</span></span>

### <a name="return-value---scode"></a><span data-ttu-id="015df-499">戻り値 - sCode</span><span class="sxs-lookup"><span data-stu-id="015df-499">Return Value - sCode</span></span>

<span data-ttu-id="015df-500">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-500">The current value.</span></span>

### <a name="remarks---scode"></a><span data-ttu-id="015df-501">備考 - sCode</span><span class="sxs-lookup"><span data-stu-id="015df-501">Remarks - sCode</span></span>

<span data-ttu-id="015df-502">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-502">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-503">データ型が COMVariantType::VT\_ERROR に設定されている場合、その COMVariant オブジェクトは scode データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-503">A COMVariant object has an scode data type if its data type is set to COMVariantType::VT\_ERROR.</span></span> <span data-ttu-id="015df-504">scode データ型は、COM 関数の戻り値として最もよく使用される Win32 HRESULT データ型と同等の COM データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-504">The scode data type is a COM data type that is equivalent to the Win32 HRESULT data type, which is most used as return values for COM functions.</span></span>

### <a name="examples---scode"></a><span data-ttu-id="015df-505">例 - sCode</span><span class="sxs-lookup"><span data-stu-id="015df-505">Examples - sCode</span></span>

<span data-ttu-id="015df-506">次の例では、VT\_ERROR 型の新しい COMVariant オブジェクトを作成し、値を 0x80001004 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-506">The following example creates a new COMVariant object of type VT\_ERROR and sets the value to 0x80001004.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_ERROR); 
```

```xpp
    // Set value of the object 
    var.sCode(0x80001004); 
}
```

## <a name="method-short"></a><span data-ttu-id="015df-507">メソッド short</span><span class="sxs-lookup"><span data-stu-id="015df-507">Method short</span></span>

<span data-ttu-id="015df-508">VT\_I2 (短い) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-508">Gets or sets the value of a COMVariant object of the VT\_I2 (short) data type.</span></span>

```xpp
public int short([int newValue])
```

### <a name="parameters---short"></a><span data-ttu-id="015df-509">パラメーター - short</span><span class="sxs-lookup"><span data-stu-id="015df-509">Parameters - short</span></span>

<span data-ttu-id="015df-510">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-510">newValue</span></span>  
<span data-ttu-id="015df-511">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-511">The new value; optional.</span></span>

### <a name="return-value---short"></a><span data-ttu-id="015df-512">戻り値 - short</span><span class="sxs-lookup"><span data-stu-id="015df-512">Return Value - short</span></span>

<span data-ttu-id="015df-513">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-513">The current value.</span></span>

### <a name="remarks---short"></a><span data-ttu-id="015df-514">備考 - short</span><span class="sxs-lookup"><span data-stu-id="015df-514">Remarks - short</span></span>

<span data-ttu-id="015df-515">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-515">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-516">データ型が COMVariantType::VT\_I2 に設定されている場合、その COMVariant オブジェクトは short データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-516">A COMVariant object has a short data type if its data type is set to COMVariantType::VT\_I2.</span></span>

### <a name="examples---short"></a><span data-ttu-id="015df-517">例 - short</span><span class="sxs-lookup"><span data-stu-id="015df-517">Examples - short</span></span>

<span data-ttu-id="015df-518">次の例では、VT\_I2 型の新しい COMVariant オブジェクトを作成し、値を 123 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-518">The following example creates a new COMVariant object of the VT\_I2 type and sets the value to 123.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I2); 
```

```xpp
    // Set value of the object 
    var.short(123); 
}
```

## <a name="method-time"></a><span data-ttu-id="015df-519">メソッド time</span><span class="sxs-lookup"><span data-stu-id="015df-519">Method time</span></span>

<span data-ttu-id="015df-520">VT\_DATE データ タイプの COMVariant オブジェクトの値の時刻部分を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-520">Gets or sets the time part of the value of a COMVariant object of the VT\_DATE data type.</span></span>

```xpp
public int time([int newValue])
```

### <a name="parameters---time"></a><span data-ttu-id="015df-521">パラメーター - time</span><span class="sxs-lookup"><span data-stu-id="015df-521">Parameters - time</span></span>

<span data-ttu-id="015df-522">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-522">newValue</span></span>  
<span data-ttu-id="015df-523">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-523">The new value; optional.</span></span>

### <a name="return-value---time"></a><span data-ttu-id="015df-524">戻り値 - time</span><span class="sxs-lookup"><span data-stu-id="015df-524">Return Value - time</span></span>

<span data-ttu-id="015df-525">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-525">The current value.</span></span>

### <a name="remarks---time"></a><span data-ttu-id="015df-526">備考 - time</span><span class="sxs-lookup"><span data-stu-id="015df-526">Remarks - time</span></span>

<span data-ttu-id="015df-527">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-527">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-528">データ型が COMVariantType::VT\_DATE に設定されている場合、その COMVariant オブジェクトは日時データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-528">A COMVariant object has a date and time data type if its data type is set to COMVariantType::VT\_DATE.</span></span> <span data-ttu-id="015df-529">オブジェクトの値を設定するとき、時刻に加えて、値の日付の部分を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="015df-529">When you set the value of the object, you must set the date part of the value in addition to the time.</span></span> <span data-ttu-id="015df-530">値の日付部分を設定するには、date プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="015df-530">To set the date part of the value, use the date property.</span></span>

### <a name="examples---time"></a><span data-ttu-id="015df-531">例 - time</span><span class="sxs-lookup"><span data-stu-id="015df-531">Examples - time</span></span>

<span data-ttu-id="015df-532">次の例では、VT\_DATE 型の COMVariant オブジェクトを作成し、値の日付部分を 1998 年 12 月 24 日に設定し、時刻の部分を 13.24 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-532">The following example creates a COMVariant object of type VT\_DATE and sets the date part of the value to 24 December 1998, and the time part of the value to 13.24.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_DATE); 
```

```xpp
    // Set value of the object 
    var.date(Str2Date("12.24.1998", 213)); 
    var.time(Str2Time("13:24:00")); 
}
```

## <a name="method-tostring"></a><span data-ttu-id="015df-533">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="015df-533">Method toString</span></span>

<span data-ttu-id="015df-534">COMVariant オブジェクトの文字列形式を作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-534">Creates a string representation of a COMVariant object.</span></span> <span data-ttu-id="015df-535">この文字列形式には、オブジェクトの値と型が含まれます。</span><span class="sxs-lookup"><span data-stu-id="015df-535">This string representation includes the value and type of the object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="015df-536">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="015df-536">Return Value - toString</span></span>

<span data-ttu-id="015df-537">COMVariant オブジェクトの文字列表現。</span><span class="sxs-lookup"><span data-stu-id="015df-537">The string representation of the COMVariant object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="015df-538">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="015df-538">Remarks - toString</span></span>

<span data-ttu-id="015df-539">このメソッドから返される実際の文字列は、COMVariant オブジェクトのバリアント データ型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="015df-539">The actual string returned from this method depends on the variant data type of the COMVariant object.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="015df-540">例 - toString</span><span class="sxs-lookup"><span data-stu-id="015df-540">Examples - toString</span></span>

<span data-ttu-id="015df-541">次の例では、COMVariant オブジェクトを作成し、現在の日付を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="015df-541">The following example creates a COMVariant object and assigns the current date to it.</span></span> <span data-ttu-id="015df-542">情報ログにオブジェクトの説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="015df-542">It then prints a description of the object to the Infolog.</span></span>

```xpp
COMVariant theDay; 
```

```xpp
theDay = COMVariant::createFromDate(today()); 
info(theDay.toString());
```

## <a name="method-uint"></a><span data-ttu-id="015df-543">メソッド uInt</span><span class="sxs-lookup"><span data-stu-id="015df-543">Method uInt</span></span>

<span data-ttu-id="015df-544">VT\_UI4 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-544">Gets or sets the value of a COMVariant object of the VT\_UI4 data type.</span></span>

```xpp
public int uInt([int newValue])
```

### <a name="parameters---uint"></a><span data-ttu-id="015df-545">パラメーター - ulnt</span><span class="sxs-lookup"><span data-stu-id="015df-545">Parameters - uInt</span></span>

<span data-ttu-id="015df-546">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-546">newValue</span></span>  
<span data-ttu-id="015df-547">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-547">The new value; optional.</span></span>

### <a name="return-value---uint"></a><span data-ttu-id="015df-548">戻り値 - ulnt</span><span class="sxs-lookup"><span data-stu-id="015df-548">Return Value - uInt</span></span>

<span data-ttu-id="015df-549">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-549">The current value.</span></span>

### <a name="remarks---uint"></a><span data-ttu-id="015df-550">備考 - ulnt</span><span class="sxs-lookup"><span data-stu-id="015df-550">Remarks - uInt</span></span>

<span data-ttu-id="015df-551">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-551">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-552">COMVariantType::VT\_UI4 データ型は uLong データ型にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-552">The COMVariantType::VT\_UI4 data type is also used for the uLong data type.</span></span>

### <a name="examples---uint"></a><span data-ttu-id="015df-553">例 - ulnt</span><span class="sxs-lookup"><span data-stu-id="015df-553">Examples - uInt</span></span>

<span data-ttu-id="015df-554">次の例では、VT\_UI4 型の新しい COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-554">The following example creates a new COMVariant object of the VT\_UI4 type and sets the value to 123456.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UI4); 
```

```xpp
    // Set value of the object 
    var.uInt(123456); 
}
```

## <a name="method-ulong"></a><span data-ttu-id="015df-555">メソッド uLong</span><span class="sxs-lookup"><span data-stu-id="015df-555">Method uLong</span></span>

<span data-ttu-id="015df-556">VT\_UI4 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-556">Gets or sets the value of a COMVariant object of the VT\_UI4 (unsigned long) data type.</span></span>

```xpp
public int uLong([int newValue])
```

### <a name="parameters---ulong"></a><span data-ttu-id="015df-557">パラメーター - uLong</span><span class="sxs-lookup"><span data-stu-id="015df-557">Parameters - uLong</span></span>

<span data-ttu-id="015df-558">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-558">newValue</span></span>  
<span data-ttu-id="015df-559">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-559">The new value; optional.</span></span>

### <a name="return-value---ulong"></a><span data-ttu-id="015df-560">戻り値 - uLong</span><span class="sxs-lookup"><span data-stu-id="015df-560">Return Value - uLong</span></span>

<span data-ttu-id="015df-561">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-561">The current value.</span></span>

### <a name="remarks---ulong"></a><span data-ttu-id="015df-562">備考 - uLong</span><span class="sxs-lookup"><span data-stu-id="015df-562">Remarks - uLong</span></span>

<span data-ttu-id="015df-563">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-563">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-564">COMVariantType::VT\_UI4 データ型は uInt データ型にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-564">The COMVariantType::VT\_UI4 data type is also used for the uInt data type.</span></span>

### <a name="examples---ulong"></a><span data-ttu-id="015df-565">例 - uLong</span><span class="sxs-lookup"><span data-stu-id="015df-565">Examples - uLong</span></span>

<span data-ttu-id="015df-566">次の例では、VT\_UI4 型の新しい COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-566">The following example creates a new COMVariant object of type VT\_UI4 and sets the value to 123456.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UI4); 
```

```xpp
    // set value of the object 
    var.uLong(123456); 
}
```

## <a name="method-ulonglong"></a><span data-ttu-id="015df-567">メソッド uLongLong</span><span class="sxs-lookup"><span data-stu-id="015df-567">Method uLongLong</span></span>

<span data-ttu-id="015df-568">VT\_UI8 (未署名の longlong) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-568">Gets or sets the value of a COMVariant object of the VT\_UI8 (unsigned longlong) data type.</span></span>

```xpp
public Int64 uLongLong([Int64 newValue])
```

### <a name="parameters---ulonglong"></a><span data-ttu-id="015df-569">パラメーター - uLongLong</span><span class="sxs-lookup"><span data-stu-id="015df-569">Parameters - uLongLong</span></span>

<span data-ttu-id="015df-570">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-570">newValue</span></span>  
<span data-ttu-id="015df-571">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-571">The new value; optional.</span></span>

### <a name="return-value---ulonglong"></a><span data-ttu-id="015df-572">戻り値 - uLongLong</span><span class="sxs-lookup"><span data-stu-id="015df-572">Return Value - uLongLong</span></span>

<span data-ttu-id="015df-573">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-573">The current value.</span></span>

### <a name="remarks---ulonglong"></a><span data-ttu-id="015df-574">備考 - uLongLong</span><span class="sxs-lookup"><span data-stu-id="015df-574">Remarks - uLongLong</span></span>

<span data-ttu-id="015df-575">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-575">If you pass in a value that has a different data type than the object, the object�s data type will be changed to match the value�s data type.</span></span> <span data-ttu-id="015df-576">データ型が COMVariantType::VT\_I8 に設定されている場合、その COMVariant オブジェクトは unsigned longlong バリアント型です。</span><span class="sxs-lookup"><span data-stu-id="015df-576">A COMVariant object has an unsigned longlong variant type if its data type is set to COMVariantType::VT\_I8.</span></span>

### <a name="examples---ulonglong"></a><span data-ttu-id="015df-577">例 - uLongLong</span><span class="sxs-lookup"><span data-stu-id="015df-577">Examples - uLongLong</span></span>

<span data-ttu-id="015df-578">次の例では、VT\_I8 型の新しい COMVariant オブジェクトを作成し、値を 9,223,372,036,854,775,808 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-578">The following example creates a new COMVariant object of type VT\_I8 and sets the value to 9,223,372,036,854,775,808.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_BOOL); 
```

```xpp
    // Set value of the object 
    var.longLong(9223372036854775808); 
}
```

## <a name="method-ushort"></a><span data-ttu-id="015df-579">メソッド uShort</span><span class="sxs-lookup"><span data-stu-id="015df-579">Method uShort</span></span>

<span data-ttu-id="015df-580">VT\_UI2 データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-580">Gets or sets the value of a COMVariant object of the VT\_UI2 data type.</span></span>

```xpp
public int uShort([int newValue])
```

### <a name="parameters---ushort"></a><span data-ttu-id="015df-581">パラメーター - uShort</span><span class="sxs-lookup"><span data-stu-id="015df-581">Parameters - uShort</span></span>

<span data-ttu-id="015df-582">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-582">newValue</span></span>  
<span data-ttu-id="015df-583">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-583">The new value; optional.</span></span>

### <a name="return-value---ushort"></a><span data-ttu-id="015df-584">戻り値 - uShort</span><span class="sxs-lookup"><span data-stu-id="015df-584">Return Value - uShort</span></span>

<span data-ttu-id="015df-585">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-585">The current value.</span></span>

### <a name="remarks---ushort"></a><span data-ttu-id="015df-586">備考 - uShort</span><span class="sxs-lookup"><span data-stu-id="015df-586">Remarks - uShort</span></span>

<span data-ttu-id="015df-587">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-587">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-588">データ型が COMVariantType::VT\_UI2 に設定されている場合、その COMVariant オブジェクトは unsigned short データ型です。</span><span class="sxs-lookup"><span data-stu-id="015df-588">A COMVariant object has an unsigned short data type if its data type is set to COMVariantType::VT\_UI2.</span></span>

### <a name="examples---ushort"></a><span data-ttu-id="015df-589">例 - uShort</span><span class="sxs-lookup"><span data-stu-id="015df-589">Examples - uShort</span></span>

<span data-ttu-id="015df-590">次の例では、VT\_UI2 型の新しい COMVariant オブジェクトを作成し、値を 12345 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-590">The following example creates a new COMVariant object of type VT\_UI2 and sets the value to 12345.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_UI2); 
```

```xpp
    // Set value of the object 
    var.uShort(12345); 
}
```

## <a name="method-variant"></a><span data-ttu-id="015df-591">メソッド variant</span><span class="sxs-lookup"><span data-stu-id="015df-591">Method variant</span></span>

<span data-ttu-id="015df-592">VT\_VARIANT (バリアント) データ タイプの COMVariant オブジェクトの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-592">Gets or sets the value of a COMVariant object of the VT\_VARIANT (variant) data type.</span></span>

```xpp
public COMVariant variant([COMVariant newValue])
```

### <a name="parameters---variant"></a><span data-ttu-id="015df-593">パラメーター - variant</span><span class="sxs-lookup"><span data-stu-id="015df-593">Parameters - variant</span></span>

<span data-ttu-id="015df-594">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-594">newValue</span></span>  
<span data-ttu-id="015df-595">新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-595">The new value; optional.</span></span>

### <a name="return-value---variant"></a><span data-ttu-id="015df-596">戻り値 - variant</span><span class="sxs-lookup"><span data-stu-id="015df-596">Return Value - variant</span></span>

<span data-ttu-id="015df-597">現在の値。</span><span class="sxs-lookup"><span data-stu-id="015df-597">The current value.</span></span>

### <a name="remarks---variant"></a><span data-ttu-id="015df-598">備考 - variant</span><span class="sxs-lookup"><span data-stu-id="015df-598">Remarks - variant</span></span>

<span data-ttu-id="015df-599">variant プロパティは、ある COMVariant オブジェクトを別の COMVariant オブジェクトにネストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="015df-599">The variant property is used to nest one COMVariant object in another COMVariant object.</span></span> <span data-ttu-id="015df-600">親オブジェクトを COMDispFunction.call への呼び出しまたは COM クラスへの呼び出しの引数として使用する場合、呼び出されたメソッドは自動的に入れ子になったオブジェクトのデータを抽出します。</span><span class="sxs-lookup"><span data-stu-id="015df-600">When using the parent object as the argument in a call to COMDispFunction.call or in a call to the COM class, the called method will automatically extract the data of the nested object.</span></span> <span data-ttu-id="015df-601">このネスト機能は、COM オブジェクトのメソッドが複数のデータ型で動作できる場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="015df-601">This nesting facility is useful when a method on a COM object can work with multiple data types.</span></span> <span data-ttu-id="015df-602">バリアントの入れ子は 1 つのレベルのみ許可されます。</span><span class="sxs-lookup"><span data-stu-id="015df-602">Only one level of variant nesting is allowed.</span></span> <span data-ttu-id="015df-603">オブジェクトと異なるデータ型の値を渡す場合は、オブジェクトのデータ型は、値のデータ型に合わせて変更されます。</span><span class="sxs-lookup"><span data-stu-id="015df-603">If you pass in a value that has a different data type than the object, the data type of the object will be changed to match the data type of the value.</span></span> <span data-ttu-id="015df-604">データ型が COMVariantType::VT\_VARIANT に設定されている場合、その COMVariant オブジェクトはバリアント型です。</span><span class="sxs-lookup"><span data-stu-id="015df-604">A COMVariant object has a variant type if its data type is set to COMVariantType::VT\_VARIANT.</span></span>

### <a name="examples---variant"></a><span data-ttu-id="015df-605">例 - variant</span><span class="sxs-lookup"><span data-stu-id="015df-605">Examples - variant</span></span>

<span data-ttu-id="015df-606">次の例では、VT\_I4 (long) 型の COMVariant オブジェクトと VT\_VARIANT 型の COMVariant オブジェクトを作成します.</span><span class="sxs-lookup"><span data-stu-id="015df-606">The following example creates a COMVariant object of type VT\_I4 (long), and a COMVariant object of type VT\_VARIANT.</span></span> <span data-ttu-id="015df-607">VT\_VARIANT タイプのオブジェクトには、VT\_I4 タイプのオブジェクトの値が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="015df-607">The object of type VT\_VARIANT is assigned the value of the object of type VT\_I4.</span></span> <span data-ttu-id="015df-608">以下のコードには仮想 COM オブジェクト (「MyCOM.Object」) が含まれており、Finance and Operations アプリケーションの外部でオブジェクトが作成されていない限り実行されません。</span><span class="sxs-lookup"><span data-stu-id="015df-608">The code below contains a hypothetical COM object ("MyCOM.Object"), and will therefore not run, unless such an object is created outside a Finance and Operations application.</span></span>

```xpp
{ 
    COM com; 
    COMDispFunction funcShow; 
```

```xpp
    COMVariant var1 = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_I4); 
```

```xpp
    COMVariant var2 = new COMVariant( 
        COMVariantInOut::IN_OUT,  
        COMVariantType::VT_VARIANT); 
```

```xpp
    InteropPermission perm1; 
    InteropPermission perm2; 
```

```xpp
    // Set code access permission to help protect use of COM object 
    perm1 = new InteropPermission(InteropKind::ComInterop); 
    perm1.assert(); 
```

```xpp
    com = new COM("MyCOM.Object"); 
```

```xpp
    // Close code access permission for COM 
    CodeAccessPermission::revertAssert(); 
```

```xpp
    // Set value of 'var1' 
    var1.Long(123456); 
    // Set value of 'var2' to 'var1' 
    var2.Variant(var1); 
```

```xpp
    // Set code access permission to protect use of 
    // COMDispFunction object 
    perm2 = new InteropPermission(InteropKind::ComInterop); 
    perm2.assert(); 
```

```xpp
    funcShow = new COMDispFunction( 
        com,  
        "Show",  
        COMDispContext::METHOD); 
```

```xpp
    // Call funcShow with a long 
    funcShow.Call(var2); 
    // Change value of 'var1' 
     var1.BStr("Hello World"); 
    // Call funcShow with a string 
    funcShow.Call(var2); 
```

```xpp
    // Close code access permission for COMDispFunction 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-variantinoutflag"></a><span data-ttu-id="015df-609">メソッド variantInOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-609">Method variantInOutFlag</span></span>

<span data-ttu-id="015df-610">COMVariant オブジェクトに対する InOutFlag 設定を設定する返します。</span><span class="sxs-lookup"><span data-stu-id="015df-610">Sets or returns the InOutFlag setting for a COMVariant object.</span></span>

```xpp
public COMVariantInOut variantInOutFlag([COMVariantInOut newValue])
```

### <a name="parameters---variantinoutflag"></a><span data-ttu-id="015df-611">パラメーター - variantInOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-611">Parameters - variantInOutFlag</span></span>

<span data-ttu-id="015df-612">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-612">newValue</span></span>  
<span data-ttu-id="015df-613">新しい InOutFlag 設定 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-613">The new InOutFlag setting; optional.</span></span>

### <a name="return-value---variantinoutflag"></a><span data-ttu-id="015df-614">戻り値 - variantInOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-614">Return Value - variantInOutFlag</span></span>

<span data-ttu-id="015df-615">現在の InOutFlag 設定。</span><span class="sxs-lookup"><span data-stu-id="015df-615">The current InOutFlag setting.</span></span>

### <a name="remarks---variantinoutflag"></a><span data-ttu-id="015df-616">備考 - variantInOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-616">Remarks - variantInOutFlag</span></span>

<span data-ttu-id="015df-617">次に、newValue パラメーターで使用可能な値のリストを示します。</span><span class="sxs-lookup"><span data-stu-id="015df-617">The following is a list of possible values for the newValue parameter.</span></span>

-   <span data-ttu-id="015df-618">COMVariantInOut::IN</span><span class="sxs-lookup"><span data-stu-id="015df-618">COMVariantInOut::IN</span></span>
-   <span data-ttu-id="015df-619">COMVariantInOut::IN\_OUT</span><span class="sxs-lookup"><span data-stu-id="015df-619">COMVariantInOut::IN\_OUT</span></span>
-   <span data-ttu-id="015df-620">COMVariantInOut::OUT</span><span class="sxs-lookup"><span data-stu-id="015df-620">COMVariantInOut::OUT</span></span>
-   <span data-ttu-id="015df-621">COMVariantInOut::OUT\_RETVAL.</span><span class="sxs-lookup"><span data-stu-id="015df-621">COMVariantInOut::OUT\_RETVAL.</span></span>

<span data-ttu-id="015df-622">InOutFlag 設定は、オブジェクトが COMDispFunction.call メソッドで引数として使用されたときに、オブジェクトに格納されているデータがどのように扱われるかを記述します。</span><span class="sxs-lookup"><span data-stu-id="015df-622">The InOutFlag setting describes how the data that is stored in the object is treated when the object is used as an argument in the COMDispFunction.call method.</span></span> <span data-ttu-id="015df-623">InOutFlag 設定の使用可能な値は、Win32 SDK に記述されている COM オートメーション オブジェクトの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="015df-623">The possible values of the InOutFlag setting correspond to the values for COM Automation objects described in the Win32 SDK.</span></span> <span data-ttu-id="015df-624">COMVariant オブジェクトに格納されたデータは、InOutFlag 設定が変更されても影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="015df-624">The data stored in the COMVariant object is unaffected when the InOutFlag setting is changed.</span></span>

### <a name="examples---variantinoutflag"></a><span data-ttu-id="015df-625">例 - variantInOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-625">Examples - variantInOutFlag</span></span>

<span data-ttu-id="015df-626">次の例では、InOutFlag 設定が IN に設定されている COMVariant オブジェクトを作成し、variantInOutFlag メソッドを使用して設定を OUT に変更します。</span><span class="sxs-lookup"><span data-stu-id="015df-626">The following example creates a COMVariant object that has the InOutFlag setting set to IN, and then uses the variantInOutFlag method to change the setting to OUT.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant(COMVariantInOut::IN); 
```

```xpp
    // Change the 'var' object to be used as an out argument 
    var.variantInOutFlag(COMVariantInOut::OUT); 
}
```

## <a name="method-varianttype"></a><span data-ttu-id="015df-627">メソッド variantType</span><span class="sxs-lookup"><span data-stu-id="015df-627">Method variantType</span></span>

<span data-ttu-id="015df-628">COMVariant オブジェクトにそのバリアント データ型を照会するか、データ型を変更します。</span><span class="sxs-lookup"><span data-stu-id="015df-628">Queries a COMVariant object for its variant data type or changes the data type.</span></span>

```xpp
public COMVariantType variantType([COMVariantType newValue])
```

### <a name="parameters---varianttype"></a><span data-ttu-id="015df-629">パラメーター - variantType</span><span class="sxs-lookup"><span data-stu-id="015df-629">Parameters - variantType</span></span>

<span data-ttu-id="015df-630">newValue</span><span class="sxs-lookup"><span data-stu-id="015df-630">newValue</span></span>  
<span data-ttu-id="015df-631">新しいバリアント データ型 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="015df-631">The new variant data type; optional.</span></span>

### <a name="return-value---varianttype"></a><span data-ttu-id="015df-632">戻り値 - variantType</span><span class="sxs-lookup"><span data-stu-id="015df-632">Return Value - variantType</span></span>

<span data-ttu-id="015df-633">現在のバリアント データ型。</span><span class="sxs-lookup"><span data-stu-id="015df-633">The current variant data type.</span></span>

### <a name="remarks---varianttype"></a><span data-ttu-id="015df-634">備考 - variantType</span><span class="sxs-lookup"><span data-stu-id="015df-634">Remarks - variantType</span></span>

<span data-ttu-id="015df-635">newValue パラメーターの使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="015df-635">The possible values for the newValue parameter are:</span></span>

-   <span data-ttu-id="015df-636">COMVariantType::VT\_I2</span><span class="sxs-lookup"><span data-stu-id="015df-636">COMVariantType::VT\_I2</span></span>
-   <span data-ttu-id="015df-637">COMVariantType::VT\_I4</span><span class="sxs-lookup"><span data-stu-id="015df-637">COMVariantType::VT\_I4</span></span>
-   <span data-ttu-id="015df-638">COMVariantType::VT\_R4</span><span class="sxs-lookup"><span data-stu-id="015df-638">COMVariantType::VT\_R4</span></span>
-   <span data-ttu-id="015df-639">COMVariantType::VT\_R8</span><span class="sxs-lookup"><span data-stu-id="015df-639">COMVariantType::VT\_R8</span></span>
-   <span data-ttu-id="015df-640">COMVariantType::VT\_CY</span><span class="sxs-lookup"><span data-stu-id="015df-640">COMVariantType::VT\_CY</span></span>
-   <span data-ttu-id="015df-641">COMVariantType::VT\_DATE</span><span class="sxs-lookup"><span data-stu-id="015df-641">COMVariantType::VT\_DATE</span></span>
-   <span data-ttu-id="015df-642">COMVariantType::VT\_BSTR</span><span class="sxs-lookup"><span data-stu-id="015df-642">COMVariantType::VT\_BSTR</span></span>
-   <span data-ttu-id="015df-643">COMVariantType::VT\_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="015df-643">COMVariantType::VT\_DISPATCH</span></span>
-   <span data-ttu-id="015df-644">COMVariantType::VT\_ERROR</span><span class="sxs-lookup"><span data-stu-id="015df-644">COMVariantType::VT\_ERROR</span></span>
-   <span data-ttu-id="015df-645">COMVariantType::VT\_BOOL</span><span class="sxs-lookup"><span data-stu-id="015df-645">COMVariantType::VT\_BOOL</span></span>
-   <span data-ttu-id="015df-646">COMVariantType::VT\_VARIANT</span><span class="sxs-lookup"><span data-stu-id="015df-646">COMVariantType::VT\_VARIANT</span></span>
-   <span data-ttu-id="015df-647">COMVariantType::VT\_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="015df-647">COMVariantType::VT\_UNKNOWN</span></span>
-   <span data-ttu-id="015df-648">COMVariantType::VT\_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="015df-648">COMVariantType::VT\_DECIMAL</span></span>
-   <span data-ttu-id="015df-649">COMVariantType::VT\_I1</span><span class="sxs-lookup"><span data-stu-id="015df-649">COMVariantType::VT\_I1</span></span>
-   <span data-ttu-id="015df-650">COMVariantType::VT\_UI1</span><span class="sxs-lookup"><span data-stu-id="015df-650">COMVariantType::VT\_UI1</span></span>
-   <span data-ttu-id="015df-651">COMVariantType::VT\_UI2</span><span class="sxs-lookup"><span data-stu-id="015df-651">COMVariantType::VT\_UI2</span></span>
-   <span data-ttu-id="015df-652">COMVariantType::VT\_UI4</span><span class="sxs-lookup"><span data-stu-id="015df-652">COMVariantType::VT\_UI4</span></span>

<span data-ttu-id="015df-653">バリアント データ型は、オブジェクトが COMDispFunction.call メソッドの呼び出しまたは COM クラスの呼び出しで引数として使用されたときに、オブジェクトに格納されているデータがどのように扱われるかを記述します。</span><span class="sxs-lookup"><span data-stu-id="015df-653">The variant data type describes how the data that is stored in the object is treated when the object is used as an argument in a call to the COMDispFunction.call method or a call to the COM class.</span></span> <span data-ttu-id="015df-654">データ型を変更すると、オブジェクトに保持されているデータは削除されます。</span><span class="sxs-lookup"><span data-stu-id="015df-654">If you change the data type, the data that is held in the object is deleted.</span></span> <span data-ttu-id="015df-655">使用可能なバリアント データ型については、\[COMVariant.new\] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="015df-655">See the \[COMVariant.new\] for information about the available variant data types.</span></span>

### <a name="examples---varianttype"></a><span data-ttu-id="015df-656">例 - variantType</span><span class="sxs-lookup"><span data-stu-id="015df-656">Examples - variantType</span></span>

<span data-ttu-id="015df-657">次の例では、新しい COMVariant オブジェクトを作成し、それを long (VT\_I4) データ型に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-657">The following example creates a new COMVariant object and sets it to be of long (VT\_I4) data type.</span></span> <span data-ttu-id="015df-658">その後、variantType メソッドを使用して、データ型を VT\_DATE (日付) に変更します。</span><span class="sxs-lookup"><span data-stu-id="015df-658">The variantType method is then used to change the data type to VT\_DATE (date).</span></span> <span data-ttu-id="015df-659">オブジェクトが保持するデータは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="015df-659">The data that is held by the object is discarded.</span></span>

```xpp
{ 
    COMVariant var = new COMVariant(); 
```

```xpp
    // Set the 'var' object to be a long 
    var.long(123); 
```

```xpp
    // Change var so that it can store a date 
    var.variantType(COMVariantType::VT_DATE); 
}
```

## <a name="method-createdatefromymd"></a><span data-ttu-id="015df-660">メソッド createDateFromYMD</span><span class="sxs-lookup"><span data-stu-id="015df-660">Method createDateFromYMD</span></span>

<span data-ttu-id="015df-661">新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-661">Creates a new COMVariant object and initializes it with a date value in one operation.</span></span>

```xpp
public static COMVariant createDateFromYMD(int year, int month, int day, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createdatefromymd"></a><span data-ttu-id="015df-662">パラメーター - createDateFromYMD</span><span class="sxs-lookup"><span data-stu-id="015df-662">Parameters - createDateFromYMD</span></span>

<span data-ttu-id="015df-663">年</span><span class="sxs-lookup"><span data-stu-id="015df-663">year</span></span>  
<span data-ttu-id="015df-664">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-664">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-665">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-665">This parameter is optional.</span></span> <span data-ttu-id="015df-666">有効値: COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="015df-666">Possible values are: COMVariantInOut::OUT\_RETVAL</span></span>

<!-- -->

<span data-ttu-id="015df-667">月</span><span class="sxs-lookup"><span data-stu-id="015df-667">month</span></span>  
<span data-ttu-id="015df-668">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-668">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-669">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-669">This parameter is optional.</span></span> <span data-ttu-id="015df-670">有効値: COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="015df-670">Possible values are: COMVariantInOut::OUT\_RETVAL</span></span>

<!-- -->

<span data-ttu-id="015df-671">日</span><span class="sxs-lookup"><span data-stu-id="015df-671">day</span></span>  
<span data-ttu-id="015df-672">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-672">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-673">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-673">This parameter is optional.</span></span> <span data-ttu-id="015df-674">有効値: COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="015df-674">Possible values are: COMVariantInOut::OUT\_RETVAL</span></span>

<!-- -->

<span data-ttu-id="015df-675">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-675">inOutFlag</span></span>  
<span data-ttu-id="015df-676">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-676">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-677">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-677">This parameter is optional.</span></span> <span data-ttu-id="015df-678">有効値: COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="015df-678">Possible values are: COMVariantInOut::OUT\_RETVAL</span></span>

### <a name="return-value---createdatefromymd"></a><span data-ttu-id="015df-679">戻り値 - createDateFromYMD</span><span class="sxs-lookup"><span data-stu-id="015df-679">Return Value - createDateFromYMD</span></span>

<span data-ttu-id="015df-680">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-680">The new COMVariant object.</span></span>

### <a name="remarks---createdatefromymd"></a><span data-ttu-id="015df-681">備考 - createDateFromYMD</span><span class="sxs-lookup"><span data-stu-id="015df-681">Remarks - createDateFromYMD</span></span>

<span data-ttu-id="015df-682">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-682">The COMVariant object that is created by this method has the data type VT\_DATE (date/time).</span></span> <span data-ttu-id="015df-683">このメソッドを使用すると、日付データ型 (0111901〜31122154) の範囲外の日付を使用できます。</span><span class="sxs-lookup"><span data-stu-id="015df-683">This method allows you to use dates that are outside the range for the date data type (0111901 to 31122154).</span></span> <span data-ttu-id="015df-684">日付範囲内の日付で、COMVariant.createFromDate メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-684">For dates within the date range, you can use the COMVariant.createFromDate method.</span></span>

### <a name="examples---createdatefromymd"></a><span data-ttu-id="015df-685">例 - createDateFromYMD</span><span class="sxs-lookup"><span data-stu-id="015df-685">Examples - createDateFromYMD</span></span>

<span data-ttu-id="015df-686">次の例では、COMVariant オブジェクトを作成し、4015 年 1 月 1 日の日付で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-686">The following example creates a COMVariant object and initializes it with the date 01 January 4015.</span></span>

```xpp
COMVariant myDate; 
```

```xpp
myDate = COMVariant::createDateFromYMD(4015,1,1);
```

## <a name="method-createfromarray"></a><span data-ttu-id="015df-687">メソッド createFromArray</span><span class="sxs-lookup"><span data-stu-id="015df-687">Method createFromArray</span></span>

<span data-ttu-id="015df-688">新しい COMVariant オブジェクトを作成し、1 回の操作で配列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-688">Creates a new COMVariant object and initializes it with an array in one operation.</span></span>

```xpp
public static COMVariant createFromArray(Array value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromarray"></a><span data-ttu-id="015df-689">パラメーター - createFromArray</span><span class="sxs-lookup"><span data-stu-id="015df-689">Parameters - createFromArray</span></span>

<span data-ttu-id="015df-690">値</span><span class="sxs-lookup"><span data-stu-id="015df-690">value</span></span>  
<span data-ttu-id="015df-691">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-691">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-692">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-692">This parameter is optional.</span></span> <span data-ttu-id="015df-693">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-693">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-694">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-694">inOutFlag</span></span>  
<span data-ttu-id="015df-695">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-695">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-696">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-696">This parameter is optional.</span></span> <span data-ttu-id="015df-697">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-697">Possible values are:</span></span>

### <a name="return-value---createfromarray"></a><span data-ttu-id="015df-698">戻り値 - createFromArray</span><span class="sxs-lookup"><span data-stu-id="015df-698">Return Value - createFromArray</span></span>

<span data-ttu-id="015df-699">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-699">The new COMVariant object.</span></span>

### <a name="remarks---createfromarray"></a><span data-ttu-id="015df-700">備考 - createFromArray</span><span class="sxs-lookup"><span data-stu-id="015df-700">Remarks - createFromArray</span></span>

<span data-ttu-id="015df-701">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_SAFEARRAY (配列) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-701">The COMVariant object that is created by this method has the data type VT\_SAFEARRAY (array).</span></span> <span data-ttu-id="015df-702">variantType メソッドの使用により、または safeArray プロパティ メソッドを使用して配列値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_SAFEARRAY に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-702">You can change the data type of an existing COMVariant object to VT\_SAFEARRAY by using the variantType method or by passing in an array value by using the safeArray property method.</span></span>

### <a name="examples---createfromarray"></a><span data-ttu-id="015df-703">例 - createFromArray</span><span class="sxs-lookup"><span data-stu-id="015df-703">Examples - createFromArray</span></span>

<span data-ttu-id="015df-704">次の例では、新しい COMVariant オブジェクトを作成し、整数の配列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-704">The following example creates a new COMVariant object and initializes it with an array of integers.</span></span>

```xpp
{ 
    int i; 
    COMVariant var; 
    Array arr = new Array(Types::INTEGER); 
```

```xpp
    for (i = 1; i <= 10; i++) 
        // Insert 10 values in the array 
        arr.value(i, i); 
```

```xpp
    // Create and initialize a COMVariant object  
    var = COMVariant::createFromArray(arr); 
}
```

## <a name="method-createfromboolean"></a><span data-ttu-id="015df-705">メソッド createFromBoolean</span><span class="sxs-lookup"><span data-stu-id="015df-705">Method createFromBoolean</span></span>

<span data-ttu-id="015df-706">新しい COMVariant オブジェクトを作成し、1 回の操作でブール値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-706">Creates a new COMVariant object and initializes it with a Boolean value in one operation.</span></span>

```xpp
public static COMVariant createFromBoolean(boolean value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromboolean"></a><span data-ttu-id="015df-707">パラメーター - createFromBoolean</span><span class="sxs-lookup"><span data-stu-id="015df-707">Parameters - createFromBoolean</span></span>

<span data-ttu-id="015df-708">値</span><span class="sxs-lookup"><span data-stu-id="015df-708">value</span></span>  
<span data-ttu-id="015df-709">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-709">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-710">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-710">This parameter is optional.</span></span> <span data-ttu-id="015df-711">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-711">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-712">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-712">inOutFlag</span></span>  
<span data-ttu-id="015df-713">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-713">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-714">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-714">This parameter is optional.</span></span> <span data-ttu-id="015df-715">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-715">Possible values are:</span></span>

### <a name="return-value---createfromboolean"></a><span data-ttu-id="015df-716">戻り値 - createFromBoolean</span><span class="sxs-lookup"><span data-stu-id="015df-716">Return Value - createFromBoolean</span></span>

<span data-ttu-id="015df-717">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-717">The new COMVariant object.</span></span>

### <a name="remarks---createfromboolean"></a><span data-ttu-id="015df-718">備考 - createFromBoolean</span><span class="sxs-lookup"><span data-stu-id="015df-718">Remarks - createFromBoolean</span></span>

<span data-ttu-id="015df-719">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_BOOL (ブール値) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-719">The COMVariant object that is created by this method has the data type VT\_BOOL (Boolean).</span></span> <span data-ttu-id="015df-720">variantType メソッドの使用により、または boolean プロパティ メソッドを使用してブール値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_BOOL に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-720">You can change the data type of an existing COMVariant object to VT\_BOOL by using the variantType method or by passing in a Boolean value by using the boolean property method.</span></span>

### <a name="examples---createfromboolean"></a><span data-ttu-id="015df-721">例 - createFromBoolean</span><span class="sxs-lookup"><span data-stu-id="015df-721">Examples - createFromBoolean</span></span>

<span data-ttu-id="015df-722">次の例では、VT\_BOOL バリアント データ型 (ブール値) の COMVariant オブジェクトを作成し、その値を true に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-722">The following example creates a COMVariant object of the VT\_BOOL variant data type (Boolean), and sets the value to true.</span></span>

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromBoolean(TRUE); 
}
```

## <a name="method-createfromcom"></a><span data-ttu-id="015df-723">メソッド createFromCOM</span><span class="sxs-lookup"><span data-stu-id="015df-723">Method createFromCOM</span></span>

<span data-ttu-id="015df-724">新しい COMVariant オブジェクトを作成し、1 回の操作で COM クラスで初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-724">Creates a new COMVariant object and initializes it with a COM class in one operation.</span></span>

```xpp
public static COMVariant createFromCOM(COM value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromcom"></a><span data-ttu-id="015df-725">パラメーター - createFromCOM</span><span class="sxs-lookup"><span data-stu-id="015df-725">Parameters - createFromCOM</span></span>

<span data-ttu-id="015df-726">値</span><span class="sxs-lookup"><span data-stu-id="015df-726">value</span></span>  
<span data-ttu-id="015df-727">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-727">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-728">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-728">This parameter is optional.</span></span> <span data-ttu-id="015df-729">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-729">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-730">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-730">inOutFlag</span></span>  
<span data-ttu-id="015df-731">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-731">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-732">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-732">This parameter is optional.</span></span> <span data-ttu-id="015df-733">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-733">Possible values are:</span></span>

### <a name="return-value---createfromcom"></a><span data-ttu-id="015df-734">戻り値 - createFromCOM</span><span class="sxs-lookup"><span data-stu-id="015df-734">Return Value - createFromCOM</span></span>

<span data-ttu-id="015df-735">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-735">The new COMVariant object.</span></span>

### <a name="remarks---createfromcom"></a><span data-ttu-id="015df-736">備考 - createFromCOM</span><span class="sxs-lookup"><span data-stu-id="015df-736">Remarks - createFromCOM</span></span>

<span data-ttu-id="015df-737">inOutFlag パラメーターの使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="015df-737">Possible values of the inOutFlag parameter are as follows:</span></span>

-   <span data-ttu-id="015df-738">COMVariantInOut::IN</span><span class="sxs-lookup"><span data-stu-id="015df-738">COMVariantInOut::IN</span></span>
-   <span data-ttu-id="015df-739">COMVariantInOut::IN\_OUT</span><span class="sxs-lookup"><span data-stu-id="015df-739">COMVariantInOut::IN\_OUT</span></span>
-   <span data-ttu-id="015df-740">COMVariantInOut::OUT</span><span class="sxs-lookup"><span data-stu-id="015df-740">COMVariantInOut::OUT</span></span>
-   <span data-ttu-id="015df-741">COMVariantInOut::OUT\_RETVAL</span><span class="sxs-lookup"><span data-stu-id="015df-741">COMVariantInOut::OUT\_RETVAL</span></span>

### <a name="examples---createfromcom"></a><span data-ttu-id="015df-742">例 - createFromCOM</span><span class="sxs-lookup"><span data-stu-id="015df-742">Examples - createFromCOM</span></span>

<span data-ttu-id="015df-743">次の例では、新しい COMVariant オブジェクトを作成し、COM オブジェクトで初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-743">The following example creates a new COMVariant object and initializes it with a COM object.</span></span>

```xpp
{ 
    COMVariant var; 
    COM com = new COM("MyCOM.Object"); 
```

```xpp
    var = COMVariant::createFromCOM(com); 
}
```

## <a name="method-createfromdate"></a><span data-ttu-id="015df-744">メソッド createFromDate</span><span class="sxs-lookup"><span data-stu-id="015df-744">Method createFromDate</span></span>

<span data-ttu-id="015df-745">新しい COMVariant オブジェクトを作成し、1 回の操作で日付値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-745">Creates a new COMVariant object and initializes it with a date value in one operation.</span></span>

```xpp
public static COMVariant createFromDate(Date value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromdate"></a><span data-ttu-id="015df-746">パラメーター - createFromDate</span><span class="sxs-lookup"><span data-stu-id="015df-746">Parameters - createFromDate</span></span>

<span data-ttu-id="015df-747">値</span><span class="sxs-lookup"><span data-stu-id="015df-747">value</span></span>  
<span data-ttu-id="015df-748">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-748">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-749">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-749">This parameter is optional.</span></span> <span data-ttu-id="015df-750">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-750">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-751">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-751">inOutFlag</span></span>  
<span data-ttu-id="015df-752">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-752">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-753">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-753">This parameter is optional.</span></span> <span data-ttu-id="015df-754">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-754">Possible values are:</span></span>

### <a name="return-value---createfromdate"></a><span data-ttu-id="015df-755">戻り値 - createFromDate</span><span class="sxs-lookup"><span data-stu-id="015df-755">Return Value - createFromDate</span></span>

<span data-ttu-id="015df-756">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-756">The new COMVariant object.</span></span>

### <a name="remarks---createfromdate"></a><span data-ttu-id="015df-757">備考 - createFromDate</span><span class="sxs-lookup"><span data-stu-id="015df-757">Remarks - createFromDate</span></span>

<span data-ttu-id="015df-758">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-758">The COMVariant object that is created by this method has the data type VT\_DATE (date/time).</span></span> <span data-ttu-id="015df-759">variantType メソッドの使用により、または date プロパティ メソッドを使用して時刻値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_DATE に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-759">You can change the data type of an existing COMVariant object to VT\_DATE by using the variantType method or by passing in a time value by using the date property method.</span></span> <span data-ttu-id="015df-760">Axapta の日付タイプ (0111901〜31122154) の範囲外の日付を使用する場合は、COMVariant.createDateFromYMD メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="015df-760">If you want to use a date that is outside the range for the Axapta date type (0111901 to 31122154), use the COMVariant.createDateFromYMD method.</span></span>

### <a name="examples---createfromdate"></a><span data-ttu-id="015df-761">例 - createFromDate</span><span class="sxs-lookup"><span data-stu-id="015df-761">Examples - createFromDate</span></span>

<span data-ttu-id="015df-762">次の例では、COMVariant オブジェクトを作成し、現在の日付で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-762">The following example creates a COMVariant object and initializes it with the current date.</span></span>

```xpp
COMVariant theDay; 
```

```xpp
theDay = COMVariant::createFromDate(today()); 
info(theDay.toString());
```

## <a name="method-createfromdateandtime"></a><span data-ttu-id="015df-763">メソッド createFromDateAndTime</span><span class="sxs-lookup"><span data-stu-id="015df-763">Method createFromDateAndTime</span></span>

<span data-ttu-id="015df-764">新しい COMVariant オブジェクトを作成し、1 回の操作で日時で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-764">Creates a new COMVariant object and initializes it with a date and time in one operation.</span></span>

```xpp
public static COMVariant createFromDateAndTime(Date date, int time, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromdateandtime"></a><span data-ttu-id="015df-765">パラメーター - createFromDateAndTime</span><span class="sxs-lookup"><span data-stu-id="015df-765">Parameters - createFromDateAndTime</span></span>

<span data-ttu-id="015df-766">日付</span><span class="sxs-lookup"><span data-stu-id="015df-766">date</span></span>  
<span data-ttu-id="015df-767">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-767">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-768">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-768">This parameter is optional.</span></span> <span data-ttu-id="015df-769">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-769">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-770">タイム</span><span class="sxs-lookup"><span data-stu-id="015df-770">time</span></span>  
<span data-ttu-id="015df-771">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-771">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-772">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-772">This parameter is optional.</span></span> <span data-ttu-id="015df-773">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-773">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-774">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-774">inOutFlag</span></span>  
<span data-ttu-id="015df-775">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-775">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-776">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-776">This parameter is optional.</span></span> <span data-ttu-id="015df-777">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-777">Possible values are:</span></span>

### <a name="return-value---createfromdateandtime"></a><span data-ttu-id="015df-778">戻り値 - createFromDateAndTime</span><span class="sxs-lookup"><span data-stu-id="015df-778">Return Value - createFromDateAndTime</span></span>

<span data-ttu-id="015df-779">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-779">The new COMVariant object.</span></span>

### <a name="remarks---createfromdateandtime"></a><span data-ttu-id="015df-780">備考 - createFromDateAndTime</span><span class="sxs-lookup"><span data-stu-id="015df-780">Remarks - createFromDateAndTime</span></span>

<span data-ttu-id="015df-781">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-781">The COMVariant object that is created by this method has the data type VT\_DATE (date/time).</span></span> <span data-ttu-id="015df-782">variantType メソッドを使用することにより、既存の COMVariant オブジェクトを VT\_DATE に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-782">You can change the data type of an existing COMVariant object to VT\_DATE by using the variantType method.</span></span>

### <a name="examples---createfromdateandtime"></a><span data-ttu-id="015df-783">例 - createFromDateAndTime</span><span class="sxs-lookup"><span data-stu-id="015df-783">Examples - createFromDateAndTime</span></span>

<span data-ttu-id="015df-784">次の例では、COMVariant オブジェクトを作成し、現在の日付と深夜 0 時から 10 秒の間隔の時刻を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="015df-784">The following example creates a COMVariant object and assigns it the current date, and a time of 10 seconds past midnight.</span></span>

```xpp
date theDay; 
COMVariant theDayAndTime; 
```

```xpp
theDay = today(); 
theDayAndTime = COMVariant::createFromDateAndTime(theDay, 10); 
info(theDayAndTime.toString());
```

## <a name="method-createfromint"></a><span data-ttu-id="015df-785">メソッド createFromInt</span><span class="sxs-lookup"><span data-stu-id="015df-785">Method createFromInt</span></span>

<span data-ttu-id="015df-786">新しい COMVariant オブジェクトを作成し、1 回の操作で整数値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-786">Creates a new COMVariant object and initializes it with an integer value in one operation.</span></span>

```xpp
public static COMVariant createFromInt(int value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromint"></a><span data-ttu-id="015df-787">パラメーター - createFromInt</span><span class="sxs-lookup"><span data-stu-id="015df-787">Parameters - createFromInt</span></span>

<span data-ttu-id="015df-788">値</span><span class="sxs-lookup"><span data-stu-id="015df-788">value</span></span>  
<span data-ttu-id="015df-789">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-789">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-790">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-790">This parameter is optional.</span></span> <span data-ttu-id="015df-791">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-791">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-792">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-792">inOutFlag</span></span>  
<span data-ttu-id="015df-793">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-793">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-794">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-794">This parameter is optional.</span></span> <span data-ttu-id="015df-795">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-795">Possible values are:</span></span>

### <a name="return-value---createfromint"></a><span data-ttu-id="015df-796">戻り値 - createFromInt</span><span class="sxs-lookup"><span data-stu-id="015df-796">Return Value - createFromInt</span></span>

<span data-ttu-id="015df-797">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-797">The new COMVariant object.</span></span>

### <a name="remarks---createfromint"></a><span data-ttu-id="015df-798">備考 - createFromInt</span><span class="sxs-lookup"><span data-stu-id="015df-798">Remarks - createFromInt</span></span>

<span data-ttu-id="015df-799">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_I4 (整数) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-799">The COMVariant object that is created by this method has the data type VT\_I4 (integer).</span></span> <span data-ttu-id="015df-800">variantType メソッドの使用により、または int プロパティ メソッドを使用して整数値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_I4 に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-800">You can change the data type of an existing COMVariant object to VT\_I4 by using the variantType method or by passing in an integer value by using the int property method.</span></span>

### <a name="examples---createfromint"></a><span data-ttu-id="015df-801">例 - createFromInt</span><span class="sxs-lookup"><span data-stu-id="015df-801">Examples - createFromInt</span></span>

<span data-ttu-id="015df-802">次の例では、VT\_I4 バリアント データ型 (整数) の COMVariant オブジェクトを作成し、値を 123 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-802">The following example creates a COMVariant object of the VT\_I4 variant data type (integer), and sets the value to 123.</span></span>

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromInt(123); 
}
```

## <a name="method-createfromint64"></a><span data-ttu-id="015df-803">メソッド createFromInt64</span><span class="sxs-lookup"><span data-stu-id="015df-803">Method createFromInt64</span></span>

<span data-ttu-id="015df-804">新しい COMVariant オブジェクトを作成し、1 回の操作でint64 値 (longLong や uLongLong) で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-804">Creates a new COMVariant object and initializes it with an int64 value (longLong or uLongLong) in one operation.</span></span>

```xpp
public static COMVariant createFromInt64(Int64 value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromint64"></a><span data-ttu-id="015df-805">パラメーター - createFromInt64</span><span class="sxs-lookup"><span data-stu-id="015df-805">Parameters - createFromInt64</span></span>

<span data-ttu-id="015df-806">値</span><span class="sxs-lookup"><span data-stu-id="015df-806">value</span></span>  
<span data-ttu-id="015df-807">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-807">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-808">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-808">This parameter is optional.</span></span> <span data-ttu-id="015df-809">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-809">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-810">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-810">inOutFlag</span></span>  
<span data-ttu-id="015df-811">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-811">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-812">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-812">This parameter is optional.</span></span> <span data-ttu-id="015df-813">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-813">Possible values are:</span></span>

### <a name="return-value---createfromint64"></a><span data-ttu-id="015df-814">戻り値 - createFromInt64</span><span class="sxs-lookup"><span data-stu-id="015df-814">Return Value - createFromInt64</span></span>

<span data-ttu-id="015df-815">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-815">The new COMVariant object.</span></span>

### <a name="remarks---createfromint64"></a><span data-ttu-id="015df-816">備考 - createFromInt64</span><span class="sxs-lookup"><span data-stu-id="015df-816">Remarks - createFromInt64</span></span>

<span data-ttu-id="015df-817">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_I8 (int64) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-817">The COMVariant object that is created by this method has the data type VT\_I8 (int64).</span></span> <span data-ttu-id="015df-818">variantType メソッドの使用により、または longLong や uLongLong プロパティ メソッドを使用して int64 値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_I8 に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-818">You can change the data type of an existing COMVariant object to VT\_I8 by using the variantType method or by passing in an int64 value by using the longLong or uLongLong property method.</span></span>

### <a name="examples---createfromint64"></a><span data-ttu-id="015df-819">例 - createFromInt64</span><span class="sxs-lookup"><span data-stu-id="015df-819">Examples - createFromInt64</span></span>

<span data-ttu-id="015df-820">次の例では、VT\_I8 バリアント データ型 (整数) の COMVariant オブジェクトを作成し、値を 123456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-820">The following example creates a COMVariant object of the VT\_I8 variant data type (integer), and sets the value to 123456.</span></span>

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromInt64(123456); 
}
```

## <a name="method-createfromreal"></a><span data-ttu-id="015df-821">メソッド createFromReal</span><span class="sxs-lookup"><span data-stu-id="015df-821">Method createFromReal</span></span>

<span data-ttu-id="015df-822">新しい COMVariant オブジェクトを作成し、1 回の操作で実際の値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-822">Creates a new COMVariant object and initializes it with a real value in one operation.</span></span>

```xpp
public static COMVariant createFromReal(Real value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromreal"></a><span data-ttu-id="015df-823">パラメーター - createFromReal</span><span class="sxs-lookup"><span data-stu-id="015df-823">Parameters - createFromReal</span></span>

<span data-ttu-id="015df-824">値</span><span class="sxs-lookup"><span data-stu-id="015df-824">value</span></span>  
<span data-ttu-id="015df-825">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-825">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-826">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-826">This parameter is optional.</span></span> <span data-ttu-id="015df-827">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-827">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-828">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-828">inOutFlag</span></span>  
<span data-ttu-id="015df-829">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-829">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-830">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-830">This parameter is optional.</span></span> <span data-ttu-id="015df-831">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-831">Possible values are:</span></span>

### <a name="return-value---createfromreal"></a><span data-ttu-id="015df-832">戻り値 - createFromReal</span><span class="sxs-lookup"><span data-stu-id="015df-832">Return Value - createFromReal</span></span>

<span data-ttu-id="015df-833">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-833">The new COMVariant object.</span></span>

### <a name="remarks---createfromreal"></a><span data-ttu-id="015df-834">備考 - createFromReal</span><span class="sxs-lookup"><span data-stu-id="015df-834">Remarks - createFromReal</span></span>

<span data-ttu-id="015df-835">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_R8 (実数) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-835">The COMVariant object that is created by this method has the data type VT\_R8 (real).</span></span> <span data-ttu-id="015df-836">variantType メソッドの使用により、または double プロパティ メソッドを使用してブール値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_R8 に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-836">You can change the data type of an existing COMVariant object to VT\_R8 by using the variantType method or by passing in a Boolean value by using the double property method.</span></span>

### <a name="examples---createfromreal"></a><span data-ttu-id="015df-837">例 - createFromReal</span><span class="sxs-lookup"><span data-stu-id="015df-837">Examples - createFromReal</span></span>

<span data-ttu-id="015df-838">次の例では、VT\_R8 バリアント データ型 (実数) の COMVariant オブジェクトを作成し、値を 123.456 に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-838">The following example creates a COMVariant object of the VT\_R8 variant data type (real) and sets the value to 123.456.</span></span>

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromReal(123.456); 
}
```

## <a name="method-createfromstr"></a><span data-ttu-id="015df-839">メソッド createFromStr</span><span class="sxs-lookup"><span data-stu-id="015df-839">Method createFromStr</span></span>

<span data-ttu-id="015df-840">新しい COMVariant オブジェクトを作成し、1 回の操作で文字列で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-840">Creates a new COMVariant object and initializes it with a string in one operation.</span></span>

```xpp
public static COMVariant createFromStr(str value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromstr"></a><span data-ttu-id="015df-841">パラメーター - createFromStr</span><span class="sxs-lookup"><span data-stu-id="015df-841">Parameters - createFromStr</span></span>

<span data-ttu-id="015df-842">値</span><span class="sxs-lookup"><span data-stu-id="015df-842">value</span></span>  
<span data-ttu-id="015df-843">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-843">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-844">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-844">This parameter is optional.</span></span> <span data-ttu-id="015df-845">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-845">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-846">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-846">inOutFlag</span></span>  
<span data-ttu-id="015df-847">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-847">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-848">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-848">This parameter is optional.</span></span> <span data-ttu-id="015df-849">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-849">Possible values are:</span></span>

### <a name="return-value---createfromstr"></a><span data-ttu-id="015df-850">戻り値 - createFromStr</span><span class="sxs-lookup"><span data-stu-id="015df-850">Return Value - createFromStr</span></span>

<span data-ttu-id="015df-851">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-851">The new COMVariant object.</span></span>

### <a name="remarks---createfromstr"></a><span data-ttu-id="015df-852">備考 - createFromStr</span><span class="sxs-lookup"><span data-stu-id="015df-852">Remarks - createFromStr</span></span>

<span data-ttu-id="015df-853">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_BSTR (文字列) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-853">The COMVariant object that is created by this method has the data type VT\_BSTR (string).</span></span> <span data-ttu-id="015df-854">variantType メソッドの使用により、または bStr プロパティ メソッドを使用して文字列値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_BSTR に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-854">You can change the data type of an existing COMVariant object to VT\_BSTR by using the variantType method or by passing in a string value by using the bStr property method.</span></span>

### <a name="examples---createfromstr"></a><span data-ttu-id="015df-855">例 - createFromStr</span><span class="sxs-lookup"><span data-stu-id="015df-855">Examples - createFromStr</span></span>

<span data-ttu-id="015df-856">次の例では、VT\_BSTR バリアント データ型の COMVariant オブジェクトを作成し、値を "Hello World" に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-856">The following example creates a COMVariant object of the VT\_BSTR variant data type and sets the value to "Hello World."</span></span>

```xpp
{ 
    COMVariant var; 
```

```xpp
    var = COMVariant::createFromStr("Hello World"); 
}
```

## <a name="method-createfromtime"></a><span data-ttu-id="015df-857">メソッド createFromTime</span><span class="sxs-lookup"><span data-stu-id="015df-857">Method createFromTime</span></span>

<span data-ttu-id="015df-858">新しい COMVariant オブジェクトを作成し、1 回の操作で時刻値で初期化します。</span><span class="sxs-lookup"><span data-stu-id="015df-858">Creates a new COMVariant object and initializes it with a time value in one operation.</span></span>

```xpp
public static COMVariant createFromTime(int value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromtime"></a><span data-ttu-id="015df-859">パラメーター - createFromTime</span><span class="sxs-lookup"><span data-stu-id="015df-859">Parameters - createFromTime</span></span>

<span data-ttu-id="015df-860">値</span><span class="sxs-lookup"><span data-stu-id="015df-860">value</span></span>  
<span data-ttu-id="015df-861">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-861">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-862">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-862">This parameter is optional.</span></span> <span data-ttu-id="015df-863">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-863">Possible values are:</span></span>

<!-- -->

<span data-ttu-id="015df-864">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-864">inOutFlag</span></span>  
<span data-ttu-id="015df-865">オブジェクトを COM メソッドまたは COM プロパティにデータを渡すか、データを受信するか、またはその両方かどうかを決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="015df-865">A flag that determines whether the object can be used to pass data to a COM method or COM property, to receive data, or both.</span></span> <span data-ttu-id="015df-866">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="015df-866">This parameter is optional.</span></span> <span data-ttu-id="015df-867">有効値:</span><span class="sxs-lookup"><span data-stu-id="015df-867">Possible values are:</span></span>

### <a name="return-value---createfromtime"></a><span data-ttu-id="015df-868">戻り値 - createFromTime</span><span class="sxs-lookup"><span data-stu-id="015df-868">Return Value - createFromTime</span></span>

<span data-ttu-id="015df-869">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-869">The new COMVariant object.</span></span>

### <a name="remarks---createfromtime"></a><span data-ttu-id="015df-870">備考 - createFromTime</span><span class="sxs-lookup"><span data-stu-id="015df-870">Remarks - createFromTime</span></span>

<span data-ttu-id="015df-871">このメソッドによって作成される COMVariant オブジェクトは、データ型 VT\_DATE (日時) を持っています。</span><span class="sxs-lookup"><span data-stu-id="015df-871">The COMVariant object that is created by this method has the data type VT\_DATE (date/time).</span></span> <span data-ttu-id="015df-872">variantType メソッドの使用により、または time プロパティ メソッドを使用して時刻値を指定することにより、既存の COMVariant オブジェクトのデータ型を VT\_DATE に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-872">You can change the data type of an existing COMVariant object to VT\_DATE by using the variantType method or by passing in a time value by using the time property method.</span></span>

### <a name="examples---createfromtime"></a><span data-ttu-id="015df-873">例 - createFromTime</span><span class="sxs-lookup"><span data-stu-id="015df-873">Examples - createFromTime</span></span>

<span data-ttu-id="015df-874">次の例では、COMVariant オブジェクトを作成し、時刻の部分を深夜 0 時から 10 秒の間隔に設定します。</span><span class="sxs-lookup"><span data-stu-id="015df-874">The following example will create a COMVariant object and set the time part to 10 seconds past midnight.</span></span>

```xpp
COMVariant theTime; 
```

```xpp
theTime = COMVariant::createFromTime(10); 
info(theTime.toString());
```

## <a name="method-createfromutcdatetime"></a><span data-ttu-id="015df-875">メソッド createFromUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="015df-875">Method createFromUtcDateTime</span></span>

```xpp
public static COMVariant createFromUtcDateTime(DateTime value, [COMVariantInOut inOutFlag])
```

### <a name="parameters---createfromutcdatetime"></a><span data-ttu-id="015df-876">パラメーター - createFromUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="015df-876">Parameters - createFromUtcDateTime</span></span>

<span data-ttu-id="015df-877">値</span><span class="sxs-lookup"><span data-stu-id="015df-877">value</span></span>  

<!-- -->

<span data-ttu-id="015df-878">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-878">inOutFlag</span></span>  

### <a name="return-value---createfromutcdatetime"></a><span data-ttu-id="015df-879">戻り値 - createFromUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="015df-879">Return Value - createFromUtcDateTime</span></span>

## <a name="method-createnovalue"></a><span data-ttu-id="015df-880">メソッド createNoValue</span><span class="sxs-lookup"><span data-stu-id="015df-880">Method createNoValue</span></span>

<span data-ttu-id="015df-881">値を持たない VT\_エラー バリアント タイプの COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-881">Creates a COMVariant object of the VT\_ERROR variant type with no value.</span></span>

```xpp
public static COMVariant createNoValue()
```

### <a name="return-value---createnovalue"></a><span data-ttu-id="015df-882">戻り値 - createNoValue</span><span class="sxs-lookup"><span data-stu-id="015df-882">Return Value - createNoValue</span></span>

<span data-ttu-id="015df-883">新しい COMVariant オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="015df-883">The new COMVariant object.</span></span>

### <a name="remarks---createnovalue"></a><span data-ttu-id="015df-884">備考 - createNoValue</span><span class="sxs-lookup"><span data-stu-id="015df-884">Remarks - createNoValue</span></span>

<span data-ttu-id="015df-885">オプションの COM パラメーターには、値を持たない COMVariant オブジェクトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="015df-885">A COMVariant object with no value can be used for COM parameters which are optional.</span></span>

### <a name="examples---createnovalue"></a><span data-ttu-id="015df-886">例 - createNoValue</span><span class="sxs-lookup"><span data-stu-id="015df-886">Examples - createNoValue</span></span>

<span data-ttu-id="015df-887">次の例では、空の COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-887">The following example creates an empty COMVariant object.</span></span>

```xpp
COMVariant noValue; 
```

```xpp
noValue = COMVariant::createNoValue(); 
info(noValue.toString());
```

## <a name="method-new"></a><span data-ttu-id="015df-888">メソッド new</span><span class="sxs-lookup"><span data-stu-id="015df-888">Method new</span></span>

<span data-ttu-id="015df-889">COM オートメーション オブジェクトのメソッドまたはプロパティに引数を渡すために使用できる COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-889">Creates a COMVariant object that can be used to pass arguments to the methods or properties of a COM Automation object.</span></span>

```xpp
public void new([COMVariantInOut inOutFlag], [COMVariantType type])
```

### <a name="parameters---new"></a><span data-ttu-id="015df-890">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="015df-890">Parameters - new</span></span>

<span data-ttu-id="015df-891">inOutFlag</span><span class="sxs-lookup"><span data-stu-id="015df-891">inOutFlag</span></span>  
<span data-ttu-id="015df-892">格納するデータのタイプ、オプション。</span><span class="sxs-lookup"><span data-stu-id="015df-892">A type of data to store; optional.</span></span> <span data-ttu-id="015df-893">これらは、COMVariantType システム列挙型によって提供される可能性のある値です。</span><span class="sxs-lookup"><span data-stu-id="015df-893">These are the possible values that are supplied by the COMVariantType system enum:</span></span>

<!-- -->

<span data-ttu-id="015df-894">タイプ</span><span class="sxs-lookup"><span data-stu-id="015df-894">type</span></span>  
<span data-ttu-id="015df-895">格納するデータのタイプ、オプション。</span><span class="sxs-lookup"><span data-stu-id="015df-895">A type of data to store; optional.</span></span> <span data-ttu-id="015df-896">これらは、COMVariantType システム列挙型によって提供される可能性のある値です。</span><span class="sxs-lookup"><span data-stu-id="015df-896">These are the possible values that are supplied by the COMVariantType system enum:</span></span>

### <a name="remarks---new"></a><span data-ttu-id="015df-897">備考 - new</span><span class="sxs-lookup"><span data-stu-id="015df-897">Remarks - new</span></span>

<span data-ttu-id="015df-898">型パラメーターが省略されると、COMVariant オブジェクトのプロパティのいずれかによって必要とされるまで、内部メモリは割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="015df-898">If the type parameter is omitted, no internal memory will be allocated until it is needed by one of the property methods of the COMVariant object.</span></span> <span data-ttu-id="015df-899">プロパティ メソッドの一覧については、\[COMVariant クラス\] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="015df-899">For a list of the property methods, see \[COMVariant Class\].</span></span> <span data-ttu-id="015df-900">異なるタイプの新しい値を指定することにより (いずれかのプロパティ メソッドを使用して)、バリアント データ型を設定後に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="015df-900">You can change the variant data type after it has been set by passing in a new value of a different type (by using one of the property methods).</span></span> <span data-ttu-id="015df-901">COMVariantType 列挙によって定義されるデータ型は、Win32 SDK によって定義されるバリアントデータ型と同じです。</span><span class="sxs-lookup"><span data-stu-id="015df-901">The data types that are defined by the COMVariantType enum are equivalent to the variant data types that are defined by the Win32 SDK.</span></span>

### <a name="examples---new"></a><span data-ttu-id="015df-902">例 - new</span><span class="sxs-lookup"><span data-stu-id="015df-902">Examples - new</span></span>

<span data-ttu-id="015df-903">次の例では、3 つの COMVariant オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="015df-903">The following example creates three COMVariant objects:</span></span>

-   <span data-ttu-id="015df-904">varIn は COM メソッドにデータを渡すためのものです。内部には文字列および短整数が格納されています。</span><span class="sxs-lookup"><span data-stu-id="015df-904">varIn is for passing data to a COM method; it has a string stored in it and then a short (integer).</span></span>
-   <span data-ttu-id="015df-905">varOut は VT\_I4 (long) タイプのデータを受け取るためのものです。</span><span class="sxs-lookup"><span data-stu-id="015df-905">varOut is to receive data of type VT\_I4 (long).</span></span>
-   <span data-ttu-id="015df-906">varOutRetval はデータをパスまたは受け取ることができます。そのデータ タイプは COMDispFunction.call メソッドでセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="015df-906">varOutRetval can pass in or receive data; its data type can be set by the COMDispFunction.call method.</span></span>

<!-- -->

```xpp
{ 
    COMVariant varIn  = new COMVariant(); 
    COMVariant varOut = new COMVariant( 
        COMVariantInOut::OUT,  
        COMVariantType::VT_I4); 
    COMVariant varOutRetval = new COMVariant( 
        COMVariantInOut::OUT_RETVAL); ; 
```

```xpp
    // Store a text string in the varIn object 
    varIn.bStr("Hello World"); 
```

```xpp
    // Change varIn to a short. 
    // Text string stored in varIn is automatically released 
    varIn.short(123);  
}
```

## <a name="method-novalue"></a><span data-ttu-id="015df-907">メソッド noValue</span><span class="sxs-lookup"><span data-stu-id="015df-907">Method noValue</span></span>

<span data-ttu-id="015df-908">既存の COMVariant オブジェクトの内容を削除し、COMDispFunction.call メソッドまたは COM クラスで使用されている場合は、未指定の引数として機能させることができます。</span><span class="sxs-lookup"><span data-stu-id="015df-908">Deletes the contents of an existing COMVariant object and enables it to act as an unspecified argument when it is used in the COMDispFunction.call method or the COM class.</span></span>

```xpp
public void noValue()
```

### <a name="remarks---novalue"></a><span data-ttu-id="015df-909">備考 - noValue</span><span class="sxs-lookup"><span data-stu-id="015df-909">Remarks - noValue</span></span>

<span data-ttu-id="015df-910">値を持たないバリアントは、null にできるパラメーターが COM メソッドにあるときに使用できます。</span><span class="sxs-lookup"><span data-stu-id="015df-910">A no-value variant can be used when a COM method has parameters that can be null.</span></span> <span data-ttu-id="015df-911">引数が指定されていない COM オブジェクトと、独自の既定値を使用する必要がある COM オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="015df-911">It indicates to the COM object that the argument has not been specified and that it must use its own default value.</span></span> <span data-ttu-id="015df-912">COM オブジェクトに対するメソッドを呼び出すときは、COMArgument::NoValue 列挙型を使用して、未指定の引数を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="015df-912">When you are calling methods on a COM object, the unspecified argument can also be specified by using the COMArgument::NoValue enum.</span></span> <span data-ttu-id="015df-913">COMDispFunction クラスを通じて呼び出すときに、この列挙型は使用できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="015df-913">Note that this enum cannot be used when calling through the COMDispFunction class.</span></span>

### <a name="examples---novalue"></a><span data-ttu-id="015df-914">例 - noValue</span><span class="sxs-lookup"><span data-stu-id="015df-914">Examples - noValue</span></span>

<span data-ttu-id="015df-915">次の例は、3 番目の引数 unspecified を使用して COM.multiply メソッドを呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="015df-915">The following example shows how to call the COM.multiply method with the third argument unspecified.</span></span> <span data-ttu-id="015df-916">以下のコードには仮想 COM オブジェクト (「MyCOM.Object」) が含まれており、Finance and Operations アプリケーションの外部でオブジェクトが作成されていない限り実行されません。</span><span class="sxs-lookup"><span data-stu-id="015df-916">The code below contains a hypothetical COM object ("MyCOM.Object"), and will therefore not run, unless such an object is created outside a Finance and Operations application.</span></span>

```xpp
{ 
    COM        com; 
    COMVariant varArg1 = new COMVariant(); 
    COMVariant varArg2 = new COMVariant(); 
    COMVariant varArg3 = new COMVariant(); 
    COMVariant varRet  = new COMVariant(COMVariantInOut::OUT_RETVAL); 
    real       ret; 
    InteropPermission perm; 
```

```xpp
    // Set code access permission to help protect use of COM object 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    // Permission scope starts here 
    perm.assert(); 
```

```xpp
    com = new COM("MyCOM.Object"); 
```

```xpp
    // Specify arguments for the multiply method 
    varArg1.float(123); 
    varArg2.float(456); 
    varArg3.noValue(); 
    varRet = com.multiply(varArg1, varArg2, varArg3); 
    // �or� 
    varRet = com.multiply(varArg1, varArg2, COMArgument::NoValue); 
     ret = varRet.double(); 
    // ret is now 56088 (123*456) 
```

```xpp
    // Close code access permission 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-finalize"></a><span data-ttu-id="015df-917">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="015df-917">Method finalize</span></span>

<span data-ttu-id="015df-918">実装されていません。</span><span class="sxs-lookup"><span data-stu-id="015df-918">Not implemented.</span></span> <span data-ttu-id="015df-919">明示的にオブジェクトを破棄する必要がある場合は、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="015df-919">You can override this method if you need to explicitly destruct an object.</span></span>

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a><span data-ttu-id="015df-920">備考 - finalize</span><span class="sxs-lookup"><span data-stu-id="015df-920">Remarks - finalize</span></span>

<span data-ttu-id="015df-921">メソッドのすべてのステートメントを実行する確定メソッドを呼び出す必要があります。メソッドを確定する暗黙的な呼び出しはありません。</span><span class="sxs-lookup"><span data-stu-id="015df-921">You must call finalize methods to execute any statements in them; there are no implicit calls to finalize methods.</span></span>

