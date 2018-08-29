---
title: "X++ 数学ランタイム関数"
description: "このトピックでは、数学ランタイム関数について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 31361
ms.assetid: 8982f158-f638-46d7-b3f7-ba8cfd356d57
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 4343059f8a8051fb98904cb716610a02b18f80d6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="x-math-runtime-functions"></a><span data-ttu-id="bcaf9-103">X++ 数学ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="bcaf9-103">X++ math runtime functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcaf9-104">このトピックでは、数学ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-104">This topic describes the math run-time functions.</span></span>

<span data-ttu-id="bcaf9-105">これらの関数は数学的な計算を実行します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-105">These functions perform mathematical calculations.</span></span>

<a name="abs"></a><span data-ttu-id="bcaf9-106">abs</span><span class="sxs-lookup"><span data-stu-id="bcaf9-106">abs</span></span>
---

<span data-ttu-id="bcaf9-107">実数の絶対値を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-107">Retrieves the absolute value of a real number.</span></span> <span data-ttu-id="bcaf9-108">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-108">Examples:</span></span>

-   <span data-ttu-id="bcaf9-109">**abs(-100.0)** は、値 **100.0** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-109">**abs(-100.0)** returns the value **100.0**.</span></span>
-   <span data-ttu-id="bcaf9-110">**abs(30.56)** は、値 **30.56** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-110">**abs(30.56)** returns the value **30.56**.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-111">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-111">Syntax</span></span>

    real abs(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-112">Parameters</span></span>

| <span data-ttu-id="bcaf9-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-113">Parameter</span></span> | <span data-ttu-id="bcaf9-114">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-114">Description</span></span>                              |
|-----------|------------------------------------------|
| <span data-ttu-id="bcaf9-115">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-115">arg</span></span>       | <span data-ttu-id="bcaf9-116">絶対値を取得する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-116">The number to get the absolute value of.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-117">Return value</span></span>

<span data-ttu-id="bcaf9-118">*arg* の絶対値。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-118">The absolute value of *arg*.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-119">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-119">Example</span></span>

    static void absExample(Args _args)
    {
        real r1;
        real r2;
        ;
        r1 = abs(-3.14);
        r2 = abs(3.14);
        if (r1 == r2)
        {
            print "abs of values are the same";
            pause;
        }
    }

## <a name="acos"></a><span data-ttu-id="bcaf9-120">acos</span><span class="sxs-lookup"><span data-stu-id="bcaf9-120">acos</span></span>
<span data-ttu-id="bcaf9-121">実数の逆余弦を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-121">Retrieves the arc cosine of a real number.</span></span> <span data-ttu-id="bcaf9-122">**注記:** 引数が -1 から 1 の範囲外の場合、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-122">**Note:** Argument values that are outside the -1 to 1 range cause the following run-time error: "Argument for trigonometric function out of range."</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-123">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-123">Syntax</span></span>

    real acos(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-124">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-124">Parameters</span></span>

| <span data-ttu-id="bcaf9-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-125">Parameter</span></span> | <span data-ttu-id="bcaf9-126">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-126">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="bcaf9-127">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-127">arg</span></span>       | <span data-ttu-id="bcaf9-128">逆余弦を取得するための数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-128">The number to retrieve the arc cosine of.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-129">Return value</span></span>

<span data-ttu-id="bcaf9-130">*arg* の逆余弦。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-130">The arc cosine of *arg*.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-131">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-131">Example</span></span>

    static void acosExample(Args _args)
    {
        real r;
        str  s;
        ;
        r = acos(0.0);
        s = strFmt("The arc cosine of 0.0 is %1 ", r);
        print s;
        pause;
    }

## <a name="asin"></a><span data-ttu-id="bcaf9-132">asin</span><span class="sxs-lookup"><span data-stu-id="bcaf9-132">asin</span></span>
<span data-ttu-id="bcaf9-133">実数の逆正弦を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-133">Retrieves the arc sine of a real number.</span></span> <span data-ttu-id="bcaf9-134">**注記:** 引数が -1 から 1 の範囲外の場合、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-134">**Note:** Argument values that are outside the -1 to 1 range cause the following run-time error: "Argument for trigonometric function out of range."</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-135">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-135">Syntax</span></span>

    real asin(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-136">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-136">Parameters</span></span>

| <span data-ttu-id="bcaf9-137">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-137">Parameter</span></span> | <span data-ttu-id="bcaf9-138">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-138">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="bcaf9-139">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-139">arg</span></span>       | <span data-ttu-id="bcaf9-140">逆正弦を計算する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-140">The number to calculate the arc sine for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-141">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-141">Return value</span></span>

<span data-ttu-id="bcaf9-142">指定した数の逆正弦。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-142">The arc sine of the specified number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-143">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-143">Remarks</span></span>

<span data-ttu-id="bcaf9-144">**aSin(0.36)** は **0.37** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-144">**aSin(0.36)** returns **0.37**.</span></span>

## <a name="atan"></a><span data-ttu-id="bcaf9-145">atan</span><span class="sxs-lookup"><span data-stu-id="bcaf9-145">atan</span></span>
<span data-ttu-id="bcaf9-146">実数の逆正接を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-146">Retrieves the arc tangent of a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-147">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-147">Syntax</span></span>

    real atan(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-148">Parameters</span></span>

| <span data-ttu-id="bcaf9-149">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-149">Parameter</span></span> | <span data-ttu-id="bcaf9-150">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-150">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="bcaf9-151">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-151">arg</span></span>       | <span data-ttu-id="bcaf9-152">逆正接を計算する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-152">The number to calculate the arc tangent for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-153">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-153">Return value</span></span>

<span data-ttu-id="bcaf9-154">指定した数の逆正接。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-154">The arc tangent of the specified number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-155">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-155">Remarks</span></span>

<span data-ttu-id="bcaf9-156">**aTan(0.36)** は **0.35** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-156">**aTan(0.36)** returns **0.35**.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-157">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-157">Example</span></span>

    static void atanExample(Args _args)
    {
        real r;
        ;
        r = atan(1.0);
        print strFmt("The Arc Tangent of 1.0 is %1", r);
        pause;
    }

## <a name="corrflagget"></a><span data-ttu-id="bcaf9-158">corrFlagGet</span><span class="sxs-lookup"><span data-stu-id="bcaf9-158">corrFlagGet</span></span>
<span data-ttu-id="bcaf9-159">実数の修正フラグの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-159">Retrieves the state of the correction flag for a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-160">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-160">Syntax</span></span>

    int corrFlagGet(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-161">Parameters</span></span>

| <span data-ttu-id="bcaf9-162">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-162">Parameter</span></span> | <span data-ttu-id="bcaf9-163">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-163">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="bcaf9-164">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-164">arg</span></span>       | <span data-ttu-id="bcaf9-165">状態を取得するためのフラグ。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-165">The flag to retrieve the state for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-166">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-166">Return value</span></span>

<span data-ttu-id="bcaf9-167">フラグが **0** (ゼロ) に設定された場合、フラグがクリアされた場合はゼロ以外の値。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-167">A non-zero value if the flag is set; **0** (zero) if the flag is cleared.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-168">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-168">Example</span></span>

<span data-ttu-id="bcaf9-169">次の例は、**1** を表示します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-169">The following example displays **1**.</span></span>

    static void corrFlagGetExample(Args _args)
    {
        real rr;
        rr = corrFlagSet(0.36,2);
        print(corrFlagGet(rr));
    }

## <a name="corrflagset"></a><span data-ttu-id="bcaf9-170">corrFlagSet</span><span class="sxs-lookup"><span data-stu-id="bcaf9-170">corrFlagSet</span></span>
<span data-ttu-id="bcaf9-171">実数の補正フラグをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-171">Controls the correction flag for a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-172">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-172">Syntax</span></span>

    real corrFlagSet(real real, int arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-173">Parameters</span></span>

| <span data-ttu-id="bcaf9-174">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-174">Parameter</span></span> | <span data-ttu-id="bcaf9-175">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-175">Description</span></span>                                                       |
|-----------|-------------------------------------------------------------------|
| <span data-ttu-id="bcaf9-176">real</span><span class="sxs-lookup"><span data-stu-id="bcaf9-176">real</span></span>      | <span data-ttu-id="bcaf9-177">補正フラグをオンまたはオフにする番号。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-177">The number in which to turn the correction flag on or off.</span></span>        |
| <span data-ttu-id="bcaf9-178">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-178">arg</span></span>       | <span data-ttu-id="bcaf9-179">フラグを無効にするには **0**、フラグを有効にする場合は、0 以外の値。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-179">**0** to turn the flag off; a non-zero value to turn the flag on.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-180">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-180">Return value</span></span>

<span data-ttu-id="bcaf9-181">**0** フラグが現在オフの場合。フラグがオンの場合はゼロ以外の値。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-181">**0** if the flag is now off; a non-zero value if the flag is now on.</span></span>

<a name="cos"></a><span data-ttu-id="bcaf9-182">cos</span><span class="sxs-lookup"><span data-stu-id="bcaf9-182">cos</span></span>
---

<span data-ttu-id="bcaf9-183">実数の余弦を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-183">Retrieves the cosine of a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-184">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-184">Syntax</span></span>

    real cos(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-185">Parameters</span></span>

| <span data-ttu-id="bcaf9-186">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-186">Parameter</span></span> | <span data-ttu-id="bcaf9-187">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-187">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="bcaf9-188">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-188">arg</span></span>       | <span data-ttu-id="bcaf9-189">余弦を計算する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-189">The number to find the cosine for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-190">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-190">Return value</span></span>

<span data-ttu-id="bcaf9-191">指定した数のコサイン。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-191">The cosine of the specified number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-192">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-192">Remarks</span></span>

<span data-ttu-id="bcaf9-193">パラメーター *arg* の値はラジアンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-193">The value of the *arg* parameter must be in radians.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-194">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-194">Example</span></span>

<span data-ttu-id="bcaf9-195">次のコード例は、**0.76** を表示します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-195">The following code example displays **0.76**.</span></span>

    static void cosExample(Args _arg)
    {
        real r;
        ;
        r = cos(15);
        print strFmt("Cos of 15 is %1", r);
        pause;
    }

## <a name="cosh"></a><span data-ttu-id="bcaf9-196">cosh</span><span class="sxs-lookup"><span data-stu-id="bcaf9-196">cosh</span></span>
<span data-ttu-id="bcaf9-197">実数の双曲線余弦を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-197">Retrieves the hyperbolic cosine of a real number.</span></span> <span data-ttu-id="bcaf9-198">**注記:** 引数が -250 から 250 の範囲外の場合、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-198">**Note:** Argument values that are outside the -250 to 250 range cause the following run-time error: "Argument for trigonometric function out of range."</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-199">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-199">Syntax</span></span>

    real cosh(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-200">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-200">Parameters</span></span>

| <span data-ttu-id="bcaf9-201">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-201">Parameter</span></span> | <span data-ttu-id="bcaf9-202">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-202">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="bcaf9-203">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-203">arg</span></span>       | <span data-ttu-id="bcaf9-204">余弦を計算する双曲線余弦。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-204">The hyperbolic number to calculate the cosine for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-205">Return value</span></span>

<span data-ttu-id="bcaf9-206">指定した数の双曲線余弦。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-206">The hyperbolic cosine of the specified number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-207">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-207">Remarks</span></span>

<span data-ttu-id="bcaf9-208">パラメーター *arg* の値はラジアンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-208">The value of the *arg* parameter must be in radians.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-209">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-209">Example</span></span>

    static void coshExample(Args _arg)
    {
        real r;
        ;
        r = cosh(0.1);
        print "The hyperbolic cosine of 0.1 is " + num2Str(r, 2, 2, 1, 1);
        pause;
    }

## <a name="decround"></a><span data-ttu-id="bcaf9-210">decRound</span><span class="sxs-lookup"><span data-stu-id="bcaf9-210">decRound</span></span>
<span data-ttu-id="bcaf9-211">指定された小数点以下の桁数となるように数値の端数を丸めます。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-211">Rounds a number to the specified number of decimal places.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-212">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-212">Syntax</span></span>

    real decRound(real figure, int decimals)

### <a name="parameters"></a><span data-ttu-id="bcaf9-213">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-213">Parameters</span></span>

| <span data-ttu-id="bcaf9-214">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-214">Parameter</span></span> | <span data-ttu-id="bcaf9-215">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-215">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="bcaf9-216">figure</span><span class="sxs-lookup"><span data-stu-id="bcaf9-216">figure</span></span>    | <span data-ttu-id="bcaf9-217">切り上げ後の数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-217">The number to round.</span></span>                      |
| <span data-ttu-id="bcaf9-218">decimals</span><span class="sxs-lookup"><span data-stu-id="bcaf9-218">decimals</span></span>  | <span data-ttu-id="bcaf9-219">丸められる小数点以下の桁数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-219">The number of decimal places to round to.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-220">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-220">Return value</span></span>

<span data-ttu-id="bcaf9-221">指定された数値の小数点以下の桁数を丸めた値。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-221">The value of the specified number, rounded to the specified number of decimal places.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-222">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-222">Remarks</span></span>

<span data-ttu-id="bcaf9-223">*decimals* パラメーターの値は、正の値、0 (ゼロ)、負の値のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-223">The value of the *decimals* parameter can be positive, 0 (zero), or negative.</span></span>

-   <span data-ttu-id="bcaf9-224">**decRound(1234.6574,2)** は、値 **1234.66** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-224">**decRound(1234.6574,2)** returns the value **1234.66**.</span></span>
-   <span data-ttu-id="bcaf9-225">**decRound(1234.6574,0)** は、値 **1235** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-225">**decRound(1234.6574,0)** returns the value **1235**.</span></span>
-   <span data-ttu-id="bcaf9-226">**decRound(1234.6574,-2)** は、値 **1200** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-226">**decRound(1234.6574,-2)** returns the value **1200**.</span></span>
-   <span data-ttu-id="bcaf9-227">**decRound(12345.6789,1)** は、値 **12345.70** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-227">**decRound(12345.6789,1)** returns the value **12345.70**.</span></span>
-   <span data-ttu-id="bcaf9-228">**decRound(12345.6789,-1)** は、値 **12350.00** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-228">**decRound(12345.6789,-1)** returns the value **12350.00**.</span></span>

<a name="exp"></a><span data-ttu-id="bcaf9-229">exp</span><span class="sxs-lookup"><span data-stu-id="bcaf9-229">exp</span></span>
---

<span data-ttu-id="bcaf9-230">指定した実数の値の自然逆対数を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-230">Retrieves the natural antilogarithm of the specified real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-231">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-231">Syntax</span></span>

    real exp(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-232">Parameters</span></span>

| <span data-ttu-id="bcaf9-233">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-233">Parameter</span></span> | <span data-ttu-id="bcaf9-234">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-234">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="bcaf9-235">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-235">arg</span></span>       | <span data-ttu-id="bcaf9-236">ナチュラル逆対数を計算する実数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-236">The real number to calculate the natural antilogarithm for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-237">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-237">Return value</span></span>

<span data-ttu-id="bcaf9-238">指定した実数の値の自然逆対数を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-238">The natural antilogarithm of the specified real number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-239">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-239">Remarks</span></span>

<span data-ttu-id="bcaf9-240">計算されたナチュラル逆対数は、*引数* パラメーターによって示されるべき乗した自然対数 e です。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-240">The calculated natural antilogarithm is the natural logarithm e raised to the power that is indicated by the *arg* parameter.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-241">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-241">Example</span></span>

    static void expExample(Args _arg)
    {
        real r1;
        real r2;
        ;
        r1 = exp(2.302585093);
        r2 = exp10(2.302585093);
        print strFmt("exp of 2.302585093 is %1", r1);
        print strFmt("exp10 of 230258 is %1", r2);
        pause;
    }

## <a name="exp10"></a><span data-ttu-id="bcaf9-242">exp10</span><span class="sxs-lookup"><span data-stu-id="bcaf9-242">exp10</span></span>
<span data-ttu-id="bcaf9-243">指定した実数の値の常用逆対数を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-243">Retrieves the base-10 antilogarithm of the specified real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-244">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-244">Syntax</span></span>

    real exp10(real decimal)

### <a name="parameters"></a><span data-ttu-id="bcaf9-245">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-245">Parameters</span></span>

| <span data-ttu-id="bcaf9-246">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-246">Parameter</span></span> | <span data-ttu-id="bcaf9-247">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-247">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="bcaf9-248">decimal</span><span class="sxs-lookup"><span data-stu-id="bcaf9-248">decimal</span></span>   | <span data-ttu-id="bcaf9-249">10 進数の逆数を計算する実数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-249">The real number to calculate the base-10 antilogarithm for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-250">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-250">Return value</span></span>

<span data-ttu-id="bcaf9-251">*decimal* パラメーターの値の 10 から始まる逆対数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-251">The 10-based antilogarithm of the value of the *decimal* parameter.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-252">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-252">Example</span></span>

    static void exp10Example(Args _arg)
    {
        real r1;
        real r2;
        ;
        r1 = exp(2.302585093);
        r2 = exp10(2.302585093);
        print strFmt("exp of 2.302585093 is %1", r1);
        print strFmt("exp10 of 230258 is %1", r2);
        pause;
    }

## <a name="frac"></a><span data-ttu-id="bcaf9-253">frac</span><span class="sxs-lookup"><span data-stu-id="bcaf9-253">frac</span></span>
<span data-ttu-id="bcaf9-254">実数の小数部を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-254">Retrieves the decimal part of a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-255">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-255">Syntax</span></span>

    real frac(real decimal)

### <a name="parameters"></a><span data-ttu-id="bcaf9-256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-256">Parameters</span></span>

| <span data-ttu-id="bcaf9-257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-257">Parameter</span></span> | <span data-ttu-id="bcaf9-258">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-258">Description</span></span>                                       |
|-----------|---------------------------------------------------|
| <span data-ttu-id="bcaf9-259">decimal</span><span class="sxs-lookup"><span data-stu-id="bcaf9-259">decimal</span></span>   | <span data-ttu-id="bcaf9-260">小数部を取得する実数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-260">The real number to retrieve the decimal part for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-261">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-261">Return value</span></span>

<span data-ttu-id="bcaf9-262">指定した数の小数部分。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-262">The decimal part of the specified number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-263">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-263">Remarks</span></span>

<span data-ttu-id="bcaf9-264">**frac(12.345)** は、値 **0.345** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-264">**frac(12.345)** returns the value **0.345**.</span></span>

## <a name="log10"></a><span data-ttu-id="bcaf9-265">log10</span><span class="sxs-lookup"><span data-stu-id="bcaf9-265">log10</span></span>
<span data-ttu-id="bcaf9-266">実数の 10 桁の対数を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-266">Retrieves the 10-digit logarithm of a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-267">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-267">Syntax</span></span>

    real log10(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-268">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-268">Parameters</span></span>

| <span data-ttu-id="bcaf9-269">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-269">Parameter</span></span> | <span data-ttu-id="bcaf9-270">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-270">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="bcaf9-271">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-271">arg</span></span>       | <span data-ttu-id="bcaf9-272">対数を計算する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-272">The number to calculate the logarithm for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-273">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-273">Return value</span></span>

<span data-ttu-id="bcaf9-274">指定した数の常用対数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-274">The base-10 logarithm of the specified number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-275">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-275">Remarks</span></span>

<span data-ttu-id="bcaf9-276">**log10(200)** は、値 **2.30** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-276">**log10(200)** returns the value **2.30**.</span></span>

## <a name="logn"></a><span data-ttu-id="bcaf9-277">logN</span><span class="sxs-lookup"><span data-stu-id="bcaf9-277">logN</span></span>
<span data-ttu-id="bcaf9-278">指定した実数の値の自然対数を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-278">Retrieves the natural logarithm of the specified real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-279">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-279">Syntax</span></span>

    real logN(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-280">Parameters</span></span>

| <span data-ttu-id="bcaf9-281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-281">Parameter</span></span> | <span data-ttu-id="bcaf9-282">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-282">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="bcaf9-283">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-283">arg</span></span>       | <span data-ttu-id="bcaf9-284">自然対数を計算する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-284">The number to calculate the natural logarithm for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-285">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-285">Return value</span></span>

<span data-ttu-id="bcaf9-286">指定した数の自然対数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-286">The natural logarithm of the specified number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-287">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-287">Remarks</span></span>

<span data-ttu-id="bcaf9-288">**logN(45)** は、値 **3.81** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-288">**logN(45)** returns the value **3.81**.</span></span>

<a name="max"></a><span data-ttu-id="bcaf9-289">最大</span><span class="sxs-lookup"><span data-stu-id="bcaf9-289">max</span></span>
---

<span data-ttu-id="bcaf9-290">2 つの指定した値の大きい方を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-290">Retrieves the larger of two specified values.</span></span>

    anytype max(anytype object1, anytype object2)

### <a name="parameters"></a><span data-ttu-id="bcaf9-291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-291">Parameters</span></span>

| <span data-ttu-id="bcaf9-292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-292">Parameter</span></span> | <span data-ttu-id="bcaf9-293">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-293">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="bcaf9-294">object1</span><span class="sxs-lookup"><span data-stu-id="bcaf9-294">object1</span></span>   | <span data-ttu-id="bcaf9-295">最初の値。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-295">The first value.</span></span>  |
| <span data-ttu-id="bcaf9-296">object2</span><span class="sxs-lookup"><span data-stu-id="bcaf9-296">object2</span></span>   | <span data-ttu-id="bcaf9-297">2 番目の値。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-297">The second value.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-298">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-298">Return value</span></span>

<span data-ttu-id="bcaf9-299">*object1* および *object2* パラメーターで指定される 2 つの値のうちの大きい方。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-299">The larger of the two values that are specified by the *object1* and *object2* parameters.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-300">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-300">Remarks</span></span>

-   <span data-ttu-id="bcaf9-301">**最大 (12.0,12.1)** は、値 **12.1** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-301">**max(12.0,12.1)** returns the value **12.1**.</span></span>
-   <span data-ttu-id="bcaf9-302">**最大 (2,33)** は、値 **33** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-302">**max(2,33)** returns the value **33**.</span></span>

<a name="min"></a><span data-ttu-id="bcaf9-303">最小</span><span class="sxs-lookup"><span data-stu-id="bcaf9-303">min</span></span>
---

<span data-ttu-id="bcaf9-304">2 つの指定した値の小さい方を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-304">Retrieves the smaller of two specified values.</span></span>

    anytype min(anytype object1, anytype object2)

### <a name="parameters"></a><span data-ttu-id="bcaf9-305">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-305">Parameters</span></span>

| <span data-ttu-id="bcaf9-306">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-306">Parameter</span></span> | <span data-ttu-id="bcaf9-307">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-307">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="bcaf9-308">object1</span><span class="sxs-lookup"><span data-stu-id="bcaf9-308">object1</span></span>   | <span data-ttu-id="bcaf9-309">最初の値。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-309">The first value.</span></span>  |
| <span data-ttu-id="bcaf9-310">object2</span><span class="sxs-lookup"><span data-stu-id="bcaf9-310">object2</span></span>   | <span data-ttu-id="bcaf9-311">2 番目の値。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-311">The second value.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-312">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-312">Return value</span></span>

<span data-ttu-id="bcaf9-313">*object1* パラメーターおよび *object2* パラメーターで指定される 2 つの値のうちの小さい方。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-313">The smaller of the two values that are specified by the *object1* and *object2* parameters.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-314">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-314">Remarks</span></span>

<span data-ttu-id="bcaf9-315">**最小 (2,33**) は、値 **2** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-315">**min(2,33**) returns the value **2**.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-316">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-316">Example</span></span>

    static void minExample(Args _arg)
    {
            anytype a;
            real r = 3.0;
            real s = 2.0;

            a = min(r, s);
            print num2Str(a, 1, 2, 1, 1) + " is less than the other number.";
    }

## <a name="power"></a><span data-ttu-id="bcaf9-317">power</span><span class="sxs-lookup"><span data-stu-id="bcaf9-317">power</span></span>
<span data-ttu-id="bcaf9-318">実数を別の実数でべき乗します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-318">Raises a real number to the power of another real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-319">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-319">Syntax</span></span>

    real power(real arg, real exponent)

### <a name="parameters"></a><span data-ttu-id="bcaf9-320">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-320">Parameters</span></span>

| <span data-ttu-id="bcaf9-321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-321">Parameter</span></span> | <span data-ttu-id="bcaf9-322">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-322">Description</span></span>                                                                 |
|-----------|-----------------------------------------------------------------------------|
| <span data-ttu-id="bcaf9-323">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-323">arg</span></span>       | <span data-ttu-id="bcaf9-324">力を計算する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-324">The number to calculate the power of.</span></span>                                       |
| <span data-ttu-id="bcaf9-325">exponent</span><span class="sxs-lookup"><span data-stu-id="bcaf9-325">exponent</span></span>  | <span data-ttu-id="bcaf9-326">*arg* パラメーターで指定された数値を増やすための数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-326">The number to raise the number that is specified by the *arg* parameter to.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-327">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-327">Return value</span></span>

<span data-ttu-id="bcaf9-328">*arg* パラメーターで指定された数の実数は、*exponent* パラメーターで指定された数の累乗になります。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-328">The real number that is the number specified by the *arg* parameter to the power of the number specified by the *exponent* parameter.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-329">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-329">Remarks</span></span>

-   <span data-ttu-id="bcaf9-330">**パワー (5.0,2.0)** は、値 **25.0** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-330">**power(5.0,2.0)** returns the value **25.0**.</span></span>
-   <span data-ttu-id="bcaf9-331">**パワー (4.0,0.5)** は、値 **2.0** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-331">**power(4.0,0.5)** returns the value **2.0**.</span></span>

## <a name="round"></a><span data-ttu-id="bcaf9-332">round</span><span class="sxs-lookup"><span data-stu-id="bcaf9-332">round</span></span>
<span data-ttu-id="bcaf9-333">実数は別の実数の最も近い倍数に切り上げられます。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-333">Rounds a real number to the nearest multiple of another real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-334">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-334">Syntax</span></span>

    real round(real _arg, real _decimals)

### <a name="parameters"></a><span data-ttu-id="bcaf9-335">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-335">Parameters</span></span>

| <span data-ttu-id="bcaf9-336">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-336">Parameter</span></span>  | <span data-ttu-id="bcaf9-337">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-337">Description</span></span>                                                                          |
|------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bcaf9-338">\_arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-338">\_arg</span></span>      | <span data-ttu-id="bcaf9-339">元の番号。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-339">The original number.</span></span>                                                                 |
| <span data-ttu-id="bcaf9-340">\_小数点以下</span><span class="sxs-lookup"><span data-stu-id="bcaf9-340">\_decimals</span></span> | <span data-ttu-id="bcaf9-341">*\_arg* パラメーターの値を倍数に丸める必要がある数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-341">The number that the value of the *\_arg* parameter must be rounded to a multiple of.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-342">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-342">Return value</span></span>

<span data-ttu-id="bcaf9-343">*\_decimals* パラメーターで指定された値の倍数で *\_arg* パラメーターで指定された値に最も近い数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-343">The number that is a multiple of the value specified by the *\_decimals* parameter and is closest to the value specified by the *\_arg* parameter.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-344">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-344">Remarks</span></span>

<span data-ttu-id="bcaf9-345">指定した小数点以下の桁数に実数を丸めるには、[decround 関数](http://msdn.microsoft.com/library/03bd2ea2-414e-43e0-ba05-f5db1a943b91(AX.60).aspx)を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-345">To round a real number to a specified number of decimal places, use the [decround function](http://msdn.microsoft.com/library/03bd2ea2-414e-43e0-ba05-f5db1a943b91(AX.60).aspx).</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-346">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-346">Remarks</span></span>

-   <span data-ttu-id="bcaf9-347">**丸め (123.45,5.00)** は、値 **125.00** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-347">**round(123.45,5.00)** returns the value **125.00**.</span></span>
-   <span data-ttu-id="bcaf9-348">**丸め (7.45,1.05)** は、値 **7.35** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-348">**round(7.45,1.05)** returns the value **7.35**.</span></span>
-   <span data-ttu-id="bcaf9-349">**丸め (23.9,5.0)** は、値 **25.00** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-349">**round(23.9,5.0)** returns the value **25.00**.</span></span>
-   <span data-ttu-id="bcaf9-350">**丸め (26.1,5.0)** は、値 **25.00** を返します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-350">**round(26.1,5.0)** returns the value **25.00**.</span></span>

<a name="sin"></a><span data-ttu-id="bcaf9-351">sin</span><span class="sxs-lookup"><span data-stu-id="bcaf9-351">sin</span></span>
---

<span data-ttu-id="bcaf9-352">実数の正弦を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-352">Retrieves the sine of a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-353">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-353">Syntax</span></span>

    real sin(real _arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-354">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-354">Parameters</span></span>

| <span data-ttu-id="bcaf9-355">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-355">Parameter</span></span> | <span data-ttu-id="bcaf9-356">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-356">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="bcaf9-357">\_arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-357">\_arg</span></span>     | <span data-ttu-id="bcaf9-358">正弦を計算する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-358">The number to calculate the sine for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-359">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-359">Return value</span></span>

<span data-ttu-id="bcaf9-360">指定した実数のサイン。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-360">The sine of the specified real number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-361">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-361">Remarks</span></span>

<span data-ttu-id="bcaf9-362">パラメーター *\_arg* の値はラジアンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-362">The value of the *\_arg* parameter must be in radians.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-363">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-363">Example</span></span>

    static void sinExample(Args _arg)
    {
        real angleDegrees = 15.0;
        real angleRadians;
        real pi = 3.14;
        real r;
        ;
        angleRadians = pi * angleDegrees / 180;
        r = sin(angleRadians);
        print "sin of a "
            + num2Str(angleDegrees, 2, 2, 1, 1)
            + " degree angle is "
            + num2Str(r, 2, 10, 1, 1);
        pause;
    }

## <a name="sinh"></a><span data-ttu-id="bcaf9-364">sinh</span><span class="sxs-lookup"><span data-stu-id="bcaf9-364">sinh</span></span>
<span data-ttu-id="bcaf9-365">実数の双曲線正弦を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-365">Retrieves the hyperbolic sine of a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-366">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-366">Syntax</span></span>

    real sinh(real _arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-367">Parameters</span></span>

| <span data-ttu-id="bcaf9-368">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-368">Parameter</span></span> | <span data-ttu-id="bcaf9-369">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-369">Description</span></span>                                      |
|-----------|--------------------------------------------------|
| <span data-ttu-id="bcaf9-370">\_arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-370">\_arg</span></span>     | <span data-ttu-id="bcaf9-371">双曲線正弦を計算する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-371">The number to calculate the hyperbolic sine for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-372">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-372">Return value</span></span>

<span data-ttu-id="bcaf9-373">指定された実数の双曲線正弦。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-373">The hyperbolic sine of the specified real number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-374">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-374">Remarks</span></span>

<span data-ttu-id="bcaf9-375">-250 から 250 の範囲外の *\_arg* パラメーターの値では、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-375">Values for the *\_arg* parameter that are outside the -250 to 250 range cause the following run-time error: "Argument for trigonometric function out of range."</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-376">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-376">Example</span></span>

<span data-ttu-id="bcaf9-377">次の例は、**sinh** 関数を示しています。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-377">The following example illustrates the **sinh** function.</span></span>

    static void sinhExample(Args _arg)
    {
        real angleDegrees = 45.0;
        real angleRadians;
        real pi = 3.14;
        real r;
        ;
        angleRadians = pi * angleDegrees / 180;
        r = sinh(angleRadians);
        print "sinh of a "
        + num2Str(angleDegrees, 2, 2, 1, 1)
        + " degree angle is "
        + num2Str(r, 2, 15, 1, 1);
        pause;
    }

<a name="tan"></a><span data-ttu-id="bcaf9-378">tan</span><span class="sxs-lookup"><span data-stu-id="bcaf9-378">tan</span></span>
---

<span data-ttu-id="bcaf9-379">実数の正接を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-379">Retrieves the tangent of a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-380">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-380">Syntax</span></span>

    real tan(real arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-381">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-381">Parameters</span></span>

| <span data-ttu-id="bcaf9-382">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-382">Parameter</span></span> | <span data-ttu-id="bcaf9-383">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-383">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="bcaf9-384">arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-384">arg</span></span>       | <span data-ttu-id="bcaf9-385">正接を計算する実数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-385">The real number to calculate the tangent for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-386">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-386">Return value</span></span>

<span data-ttu-id="bcaf9-387">指定した実数の正接。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-387">The tangent of the specified real number.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-388">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-388">Remarks</span></span>

<span data-ttu-id="bcaf9-389">-250 から 250 の範囲外の *arg* パラメーターの値では、次のランタイム エラーが発生します。「引数が三角関数の範囲外です」。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-389">Values for the *arg* parameter that are outside the -250 to 250 range cause the following run-time error: "Argument for trigonometric function out of range."</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-390">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-390">Example</span></span>

<span data-ttu-id="bcaf9-391">次の例は、**tan** 関数を示しています。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-391">The following example illustrates the **tan** function.</span></span>

    static void tanExample(Args _arg)
    {
        real r;
        ;
        r = tan(250);
        print strFmt("Tan of 250 is %1", r);
        pause;
    }

## <a name="tanh"></a><span data-ttu-id="bcaf9-392">tanh</span><span class="sxs-lookup"><span data-stu-id="bcaf9-392">tanh</span></span>
<span data-ttu-id="bcaf9-393">実数の双曲線正接を取得します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-393">Retrieves the hyperbolic tangent of a real number.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-394">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-394">Syntax</span></span>

    real tanh(real _arg)

### <a name="parameters"></a><span data-ttu-id="bcaf9-395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-395">Parameters</span></span>

| <span data-ttu-id="bcaf9-396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-396">Parameter</span></span> | <span data-ttu-id="bcaf9-397">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-397">Description</span></span>                                         |
|-----------|-----------------------------------------------------|
| <span data-ttu-id="bcaf9-398">\_arg</span><span class="sxs-lookup"><span data-stu-id="bcaf9-398">\_arg</span></span>     | <span data-ttu-id="bcaf9-399">双曲線正接を計算する数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-399">The number to calculate the hyperbolic tangent for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-400">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-400">Return value</span></span>

<span data-ttu-id="bcaf9-401">指定された実数の双曲線正接。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-401">The hyperbolic tangent of the specified real number.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-402">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-402">Example</span></span>

<span data-ttu-id="bcaf9-403">次の例は、**tanh** 関数を示しています。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-403">The following example illustrates the **tanh** function.</span></span>

    static void tanhExample(Args _arg)
    {
        real r;
        ;
        r = tanh(0.1);
        print "The hyperbolic tangent of angle 0.1 is "
        + num2Str(r, 2, 10, 1, 1);
        pause;
    }

## <a name="trunc"></a><span data-ttu-id="bcaf9-404">trunc</span><span class="sxs-lookup"><span data-stu-id="bcaf9-404">trunc</span></span>
<span data-ttu-id="bcaf9-405">小数点以下を削除して実数を切り捨てます。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-405">Truncates a real number by removing any decimal places.</span></span>

### <a name="syntax"></a><span data-ttu-id="bcaf9-406">構文</span><span class="sxs-lookup"><span data-stu-id="bcaf9-406">Syntax</span></span>

    real trunc(real _decimal)

### <a name="parameters"></a><span data-ttu-id="bcaf9-407">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-407">Parameters</span></span>

| <span data-ttu-id="bcaf9-408">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcaf9-408">Parameter</span></span> | <span data-ttu-id="bcaf9-409">説明</span><span class="sxs-lookup"><span data-stu-id="bcaf9-409">Description</span></span>             |
|-----------|-------------------------|
| <span data-ttu-id="bcaf9-410">\_小数点以下</span><span class="sxs-lookup"><span data-stu-id="bcaf9-410">\_decimal</span></span> | <span data-ttu-id="bcaf9-411">切り捨て後の数。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-411">The number to truncate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="bcaf9-412">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcaf9-412">Return value</span></span>

<span data-ttu-id="bcaf9-413">小数点以下桁数が削除された後の *\_decimal* パラメーターの値に等しい番号。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-413">A number that is equivalent to the value of the *\_decimal* parameter after the decimal places have been removed.</span></span>

### <a name="remarks"></a><span data-ttu-id="bcaf9-414">備考</span><span class="sxs-lookup"><span data-stu-id="bcaf9-414">Remarks</span></span>

<span data-ttu-id="bcaf9-415">この関数は、常に数値を完全な整数に四捨五入します。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-415">This function always rounds numbers down to a complete integer.</span></span>

### <a name="example"></a><span data-ttu-id="bcaf9-416">例</span><span class="sxs-lookup"><span data-stu-id="bcaf9-416">Example</span></span>

<span data-ttu-id="bcaf9-417">次の例では、2.7147 を 2.00 に切り捨てます。</span><span class="sxs-lookup"><span data-stu-id="bcaf9-417">The following example truncates 2.7147 to 2.00.</span></span>

    static void truncExample(Args _arg)
    {
        real r;
        ;
        r = trunc(2.7147);
        print strFmt("r = %1",  r);
        pause;
    }




