---
title: "X++ 変換ランタイム関数"
description: "このトピックでは、変換ランタイム関数について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 31321
ms.assetid: cf3e4f05-5ef0-49b1-b76e-8269913ee29d
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f44bea249f70a862d5430833110638f436d548e4
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="x-conversion-run-time-functions"></a><span data-ttu-id="7a075-103">X++ 変換ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="7a075-103">X++ conversion run-time functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a075-104">このトピックでは、変換ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a075-104">This topic describes the conversion run-time functions.</span></span>

<a name="any2date"></a><span data-ttu-id="7a075-105">any2Date</span><span class="sxs-lookup"><span data-stu-id="7a075-105">any2Date</span></span>
--------

<span data-ttu-id="7a075-106">**anytype** 値を**日付**値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-106">Converts an **anytype** value to a **date** value.</span></span>

    date any2Date(anytype object)

### <a name="parameters"></a><span data-ttu-id="7a075-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-107">Parameters</span></span>

| <span data-ttu-id="7a075-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-108">Parameter</span></span> | <span data-ttu-id="7a075-109">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-109">Description</span></span>                     |
|-----------|---------------------------------|
| <span data-ttu-id="7a075-110">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7a075-110">object</span></span>    | <span data-ttu-id="7a075-111">日付に変換する値。</span><span class="sxs-lookup"><span data-stu-id="7a075-111">The value to convert to a date.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-112">Return value</span></span>

<span data-ttu-id="7a075-113">**日付**値。</span><span class="sxs-lookup"><span data-stu-id="7a075-113">A **date** value.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-114">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-114">Remarks</span></span>

<span data-ttu-id="7a075-115">*object* パラメーターはほとんどのデータ型にすることができますが、**str** または **int** 型である場合に役に立つ出力が取得されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-115">The *object* parameter can be of most data types, but useful output is obtained when it's of the **str** or **int** type.</span></span> <span data-ttu-id="7a075-116">不適切なコンテンツでは、ランタイム エラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-116">Inappropriate content generates a run-time error.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-117">例</span><span class="sxs-lookup"><span data-stu-id="7a075-117">Example</span></span>

    static void any2DateExample(Args _args)
    {
            date myDate;
            str s;
            int i;
            s = "2010 6 17"; // A string object, of yyyy mm dd.
            myDate = any2Date(s);
            Global::info(strFmt("%1  is output, from input of "2010 6 17"", myDate));
            i = 40361; // An int object, which represents the number of days from 1900/01/01.
            myDate = any2Date(i);
            Global::info(strFmt("%1  is output, from input of 40361", myDate));
    }
    /**** Infolog display.
    Message (04:44:15 pm)
    6/17/2010 is output, from input of "2010 6 17"
    7/4/2010 is output, from input of 40361
    ****/

## <a name="any2enum"></a><span data-ttu-id="7a075-118">any2Enum</span><span class="sxs-lookup"><span data-stu-id="7a075-118">any2Enum</span></span>
<span data-ttu-id="7a075-119">**anytype** 値を、ターゲット列挙の要素の**名前**プロパティ値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-119">Converts an **anytype** value to the **Name** property value of an element in the target enum.</span></span>

    enum any2Enum(anytype object)

### <a name="parameters"></a><span data-ttu-id="7a075-120">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-120">Parameters</span></span>

| <span data-ttu-id="7a075-121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-121">Parameter</span></span> | <span data-ttu-id="7a075-122">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-122">Description</span></span>                                                                 |
|-----------|-----------------------------------------------------------------------------|
| <span data-ttu-id="7a075-123">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7a075-123">object</span></span>    | <span data-ttu-id="7a075-124">ターゲット列挙の要素の **Value** プロパティに一致する値。</span><span class="sxs-lookup"><span data-stu-id="7a075-124">The value to match the **Value** property of an element in the target enum.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-125">Return value</span></span>

<span data-ttu-id="7a075-126">ターゲット列挙に、入力パラメーターに一致する **Value** がある方の、**Name** プロパティの値</span><span class="sxs-lookup"><span data-stu-id="7a075-126">The value of the **Name** property for whichever element in the target enum has a **Value** property that matches the input parameter.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-127">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-127">Remarks</span></span>

<span data-ttu-id="7a075-128">*object* パラメーターはほとんどのデータ型にすることができますが、**str** または **int** 型のパラメーターを使用した場合のみ役に立つデータが取得されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-128">The *object* parameter can be of most data types, but useful data is obtained only when you use a parameter of the **str** or **int** type.</span></span> <span data-ttu-id="7a075-129">この入力*オブジェクト*パラメーターは、ターゲット列挙型の個々の要素の**値**プロパティを参照します。</span><span class="sxs-lookup"><span data-stu-id="7a075-129">This input *object* parameter refers to the **Value** property of an individual element in the target enum.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-130">例</span><span class="sxs-lookup"><span data-stu-id="7a075-130">Example</span></span>

    static void any2EnumExample(Args _args)
    {
            NoYes myNoYes;  // NoYes is an enum.
            int i;
            str s;
            i = 0;  // An int that will be converted.
            myNoYes = any2Enum(i);
            Global::info(strfmt("'%1' - is the output, from input of the %2 as int.", myNoYes, i));
            s = "1";  // A str that will be converted.
            myNoYes = any2Enum(s);
            Global::info(strfmt("'%1' - is the output, from input of the %2 as str.", myNoYes, s));
            /**** Infolog display.
            Message (01:05:32 pm)
            'No' - is the output, from input of the 0 as int.
            'Yes' - is the output, from input of the 1 as str.
            ****/
    }

## <a name="any2guid"></a><span data-ttu-id="7a075-131">any2Guid</span><span class="sxs-lookup"><span data-stu-id="7a075-131">any2Guid</span></span>
<span data-ttu-id="7a075-132">指定された **anytype** オブジェクトを GUID オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-132">Converts the specified **anytype** object to a GUID object.</span></span>

    guid any2Guid(anytype object)

### <a name="parameters"></a><span data-ttu-id="7a075-133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-133">Parameters</span></span>

| <span data-ttu-id="7a075-134">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-134">Parameter</span></span> | <span data-ttu-id="7a075-135">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-135">Description</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="7a075-136">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7a075-136">object</span></span>    | <span data-ttu-id="7a075-137">GUID オブジェクトに変換する値。</span><span class="sxs-lookup"><span data-stu-id="7a075-137">The value to convert to a GUID object.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-138">Return value</span></span>

<span data-ttu-id="7a075-139">GUID オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7a075-139">A GUID object.</span></span>

## <a name="any2int"></a><span data-ttu-id="7a075-140">any2Int</span><span class="sxs-lookup"><span data-stu-id="7a075-140">any2Int</span></span>
<span data-ttu-id="7a075-141">**anytype** 値を **int** 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-141">Converts an **anytype** value to an **int** value.</span></span>

    int any2Int(anytype object)

### <a name="parameters"></a><span data-ttu-id="7a075-142">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-142">Parameters</span></span>

| <span data-ttu-id="7a075-143">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-143">Parameter</span></span> | <span data-ttu-id="7a075-144">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-144">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="7a075-145">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7a075-145">object</span></span>    | <span data-ttu-id="7a075-146">変換する値。</span><span class="sxs-lookup"><span data-stu-id="7a075-146">The value to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-147">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-147">Return value</span></span>

<span data-ttu-id="7a075-148">**int** 値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-148">An **int** value.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-149">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-149">Remarks</span></span>

<span data-ttu-id="7a075-150">*object* パラメーターはほとんどのデータ型にすることができますが、**enum**、**real**、または **str** 型のパラメーターを使用した場合のみ役に立つデータが取得されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-150">The *object* parameter can be of most data types, but useful data is obtained only when you use parameters of the **enum**, **real**, or **str** type.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-151">例</span><span class="sxs-lookup"><span data-stu-id="7a075-151">Example</span></span>

    static void any2IntExample(Args _args)
    {
            int myInt;
            str s;
            NoYes a;
            real r;
            s = "31";
            myInt = any2Int(s);
            Global::info(strfmt("%1 is the output, from input of 31 as a str value.", myInt));
            a = NoYes::No;
            myInt = any2Int(a);
            Global::info(strfmt("%1 is the output, from input of NoYes::No as an enum value.", myInt));
            r = 5.34e2;
            myInt = any2Int(r);
            Global::info(strfmt("%1 is the output, from the input of 5.34e2 as a real value.", myInt));
    }
    /**** Infolog display.
    Message (02:23:59 pm)
    31 is the output, from input of 31 as a str value.
    0 is the output, from input of NoYes::No as an enum value.
    534 is the output, from the input of 5.34e2 as a real value.
    ****/

## <a name="any2int64"></a><span data-ttu-id="7a075-152">any2Int64</span><span class="sxs-lookup"><span data-stu-id="7a075-152">any2Int64</span></span>
<span data-ttu-id="7a075-153">**anytype** オブジェクトを **int64** オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-153">Converts an **anytype** object to an **int64** object.</span></span>

    int64 any2Int64(anytype object)

### <a name="parameters"></a><span data-ttu-id="7a075-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-154">Parameters</span></span>

| <span data-ttu-id="7a075-155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-155">Parameter</span></span> | <span data-ttu-id="7a075-156">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-156">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="7a075-157">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7a075-157">object</span></span>    | <span data-ttu-id="7a075-158">変換する **anytype** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7a075-158">The **anytype** object to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-159">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-159">Return value</span></span>

<span data-ttu-id="7a075-160">**int64** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="7a075-160">An **int64** object.</span></span>

## <a name="any2real"></a><span data-ttu-id="7a075-161">any2Real</span><span class="sxs-lookup"><span data-stu-id="7a075-161">any2Real</span></span>
<span data-ttu-id="7a075-162">**anytype** 値を**実際の**値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-162">Converts an **anytype** value to a **real** value.</span></span>

    real any2Real(anytype object)

### <a name="parameters"></a><span data-ttu-id="7a075-163">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-163">Parameters</span></span>

| <span data-ttu-id="7a075-164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-164">Parameter</span></span> | <span data-ttu-id="7a075-165">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-165">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="7a075-166">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7a075-166">object</span></span>    | <span data-ttu-id="7a075-167">変換する値。</span><span class="sxs-lookup"><span data-stu-id="7a075-167">The value to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-168">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-168">Return value</span></span>

<span data-ttu-id="7a075-169">**実数**値。</span><span class="sxs-lookup"><span data-stu-id="7a075-169">A **real** value.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-170">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-170">Remarks</span></span>

<span data-ttu-id="7a075-171">*object* パラメーターはほとんどのデータ型にすることができますが、**date**、**int**、**enum**、および **str** 型の入力要素で役に立つ出力が取得されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-171">The *object* parameter can be of most data types, but useful output is obtained for input elements of the **date**, **int**, **enum**, and **str** types.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-172">例</span><span class="sxs-lookup"><span data-stu-id="7a075-172">Example</span></span>

    static void any2RealExample(Args _args)
    {
            real myReal;
            str s;
            int i;
            NoYes a;
            s = "5.12";
            myReal = any2Real(s);
            Global::info(strfmt("%1 is the output from the input of 5.12 as a str object", myReal));
            i = 64;
            myReal = any2Real(i);
            Global::info(strfmt("%1 is the output from the input of 64 as an int object", myReal));
            a = NoYes::Yes;
            myReal = any2Real(a);
            Global::info(strfmt("%1 is the output from the input of NoYes::Yes as an enum object", myReal));
    }
    /****Infolog display.
    Message (02:43:57 pm)
    5.12 is the output from the input of 5.12 as a str object
    64.00 is the output from the input of 64 as an int object
    1.00 is the output from the input of NoYes::Yes as an enum object
    ****/

## <a name="any2str"></a><span data-ttu-id="7a075-173">any2Str</span><span class="sxs-lookup"><span data-stu-id="7a075-173">any2Str</span></span>
<span data-ttu-id="7a075-174">**anytype** 値を **str** 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-174">Converts an **anytype** value to a **str** value.</span></span>

    str any2Str(anytype object)

### <a name="parameters"></a><span data-ttu-id="7a075-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-175">Parameters</span></span>

| <span data-ttu-id="7a075-176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-176">Parameter</span></span> | <span data-ttu-id="7a075-177">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-177">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="7a075-178">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7a075-178">object</span></span>    | <span data-ttu-id="7a075-179">変換する値。</span><span class="sxs-lookup"><span data-stu-id="7a075-179">The value to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-180">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-180">Return value</span></span>

<span data-ttu-id="7a075-181">**str**値。</span><span class="sxs-lookup"><span data-stu-id="7a075-181">A **str** value.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-182">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-182">Remarks</span></span>

<span data-ttu-id="7a075-183">*object* パラメーターはほとんどのデータ型にすることができますが、**date**、**int**、および **enum** 型の入力要素から役に立つ出力が取得されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-183">The *object* parameter can be of most data types, but useful output is obtained from input elements of the **date**, **int**, and **enum** types.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-184">例</span><span class="sxs-lookup"><span data-stu-id="7a075-184">Example</span></span>

    static void any2StrExample(Args _args)
    {
            str myStr;
            anytype a;
            a = "Any to string";
            myStr = any2Str(a);
            Global::info(strFmt("%1 is output, from input of Any to string as a str value", myStr));
            a = NoYes::Yes;
            myStr = any2Str(a);
            Global::info(strFmt("%1 is output, from input of NoYes::Yes as an enumeration", myStr));
    }
    /****Infolog Display
    Message (09:08:46 am)
    Any to string is output, from input of Any to string as a str value
    1 is output, from input of NoYes::Yes as an enumeration
    ****/

## <a name="anytodate"></a><span data-ttu-id="7a075-185">anytodate</span><span class="sxs-lookup"><span data-stu-id="7a075-185">anytodate</span></span>
<span data-ttu-id="7a075-186">[any2Date](#any2date) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a075-186">See [any2Date](#any2date).</span></span>

## <a name="anytoenum"></a><span data-ttu-id="7a075-187">anytoenum</span><span class="sxs-lookup"><span data-stu-id="7a075-187">anytoenum</span></span>
<span data-ttu-id="7a075-188">[any2Enum](#any2enum) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a075-188">See [any2Enum](#any2enum).</span></span>

## <a name="anytoguid"></a><span data-ttu-id="7a075-189">anytoguid</span><span class="sxs-lookup"><span data-stu-id="7a075-189">anytoguid</span></span>
<span data-ttu-id="7a075-190">[any2Guid](#any2guid) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a075-190">See [any2Guid](#any2guid).</span></span>

## <a name="anytoint"></a><span data-ttu-id="7a075-191">anytoint</span><span class="sxs-lookup"><span data-stu-id="7a075-191">anytoint</span></span>
<span data-ttu-id="7a075-192">[any2Int](#any2int) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a075-192">See [any2Int](#any2int).</span></span>

## <a name="anytoint64"></a><span data-ttu-id="7a075-193">anytoint64</span><span class="sxs-lookup"><span data-stu-id="7a075-193">anytoint64</span></span>
<span data-ttu-id="7a075-194">[any2Int64](#any2int64) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a075-194">See [any2Int64](#any2int64).</span></span>

## <a name="anytoreal"></a><span data-ttu-id="7a075-195">anytoreal</span><span class="sxs-lookup"><span data-stu-id="7a075-195">anytoreal</span></span>
<span data-ttu-id="7a075-196">[any2Real](#any2real) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a075-196">See [any2Real](#any2real).</span></span>

## <a name="anytostr"></a><span data-ttu-id="7a075-197">anytostr</span><span class="sxs-lookup"><span data-stu-id="7a075-197">anytostr</span></span>
<span data-ttu-id="7a075-198">[any2Str](#any2str) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a075-198">See [any2Str](#any2str).</span></span>

## <a name="char2num"></a><span data-ttu-id="7a075-199">char2Num</span><span class="sxs-lookup"><span data-stu-id="7a075-199">char2Num</span></span>

<span data-ttu-id="7a075-200">文字列内の文字を、その文字の ASCII 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-200">Converts a character in a string to the ASCII value of the character.</span></span>

    int char2Num(str text, int position)

### <a name="parameters"></a><span data-ttu-id="7a075-201">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-201">Parameters</span></span>

| <span data-ttu-id="7a075-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-202">Parameter</span></span> | <span data-ttu-id="7a075-203">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-203">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="7a075-204">テキスト</span><span class="sxs-lookup"><span data-stu-id="7a075-204">text</span></span>      | <span data-ttu-id="7a075-205">文字を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-205">The string that contains the character.</span></span>      |
| <span data-ttu-id="7a075-206">職位</span><span class="sxs-lookup"><span data-stu-id="7a075-206">position</span></span>  | <span data-ttu-id="7a075-207">文字列内の文字の位置。</span><span class="sxs-lookup"><span data-stu-id="7a075-207">The position of the character in the string.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-208">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-208">Return value</span></span>

<span data-ttu-id="7a075-209">**int** オブジェクトとしての文字の ASCII 値。</span><span class="sxs-lookup"><span data-stu-id="7a075-209">The ASCII value of the character as an **int** object.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-210">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-210">Remarks</span></span>

    char2Num("ABCDEFG",3); //Returns the numeric value of C, which is 67.
    char2Num("ABCDEFG",1); //Returns the numeric value of A, which is 65.

## <a name="date2num"></a><span data-ttu-id="7a075-211">date2Num</span><span class="sxs-lookup"><span data-stu-id="7a075-211">date2Num</span></span>
<span data-ttu-id="7a075-212">日付を、1900 年1 月 1 日以降の日数に対応する整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-212">Converts a date to an integer that corresponds to the number of days since January 1, 1900.</span></span>

    int date2Num(date _date)

### <a name="parameters"></a><span data-ttu-id="7a075-213">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-213">Parameters</span></span>

| <span data-ttu-id="7a075-214">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-214">Parameter</span></span> | <span data-ttu-id="7a075-215">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-215">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="7a075-216">\_ 日付</span><span class="sxs-lookup"><span data-stu-id="7a075-216">\_date</span></span>    | <span data-ttu-id="7a075-217">変換する日付。</span><span class="sxs-lookup"><span data-stu-id="7a075-217">The date to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-218">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-218">Return value</span></span>

<span data-ttu-id="7a075-219">1900 年 1 月 1 日から指定された日付までの日数。</span><span class="sxs-lookup"><span data-stu-id="7a075-219">The number of days between January 1, 1900, and the specified date.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-220">例</span><span class="sxs-lookup"><span data-stu-id="7a075-220">Example</span></span>

    //Returns the value377.
    date2Num(1311901);
    static void date2NumExample(Args _arg)
    {
            date d = today();
            int i;
            i = date2Num(d);
            print i;
    }

## <a name="date2str"></a><span data-ttu-id="7a075-221">date2Str</span><span class="sxs-lookup"><span data-stu-id="7a075-221">date2Str</span></span>
<span data-ttu-id="7a075-222">指定されたデータを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-222">Converts the specified date to a string.</span></span>

    str date2Str(date date, int sequence, int day, int separator1, int month, int separator2, int year [, int flags = DateFlags::None])

### <a name="parameters"></a><span data-ttu-id="7a075-223">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-223">Parameters</span></span>

| <span data-ttu-id="7a075-224">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-224">Parameter</span></span>  | <span data-ttu-id="7a075-225">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-225">Description</span></span>                                                                                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a075-226">日付</span><span class="sxs-lookup"><span data-stu-id="7a075-226">date</span></span>       | <span data-ttu-id="7a075-227">変換する日付。</span><span class="sxs-lookup"><span data-stu-id="7a075-227">The date to convert.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="7a075-228">順序</span><span class="sxs-lookup"><span data-stu-id="7a075-228">sequence</span></span>   | <span data-ttu-id="7a075-229">日付のコンポーネントの順序を示す 3 桁の番号: 日は **1**、月は **2**、年は **3**。</span><span class="sxs-lookup"><span data-stu-id="7a075-229">A three-digit number that indicates the sequence for the components of the date: **1** for day, **2** for month, and **3** for year.</span></span>                                                                        |
| <span data-ttu-id="7a075-230">日</span><span class="sxs-lookup"><span data-stu-id="7a075-230">day</span></span>        | <span data-ttu-id="7a075-231">日付に関する、日付コンポーネントの形式を示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-231">An enumeration value that indicates the format for the day component of the date.</span></span>                                                                                                                            |
| <span data-ttu-id="7a075-232">separator1</span><span class="sxs-lookup"><span data-stu-id="7a075-232">separator1</span></span> | <span data-ttu-id="7a075-233">日付の最初の 2 つのコンポーネント間で使用する区切り記号を示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-233">An enumeration value that indicates the separator to use between the first two components of the date.</span></span>                                                                                                       |
| <span data-ttu-id="7a075-234">月</span><span class="sxs-lookup"><span data-stu-id="7a075-234">month</span></span>      | <span data-ttu-id="7a075-235">日付に関する月のコンポーネントの形式を示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-235">An enumeration value that indicates the format for the month component of the date.</span></span>                                                                                                                          |
| <span data-ttu-id="7a075-236">separator2</span><span class="sxs-lookup"><span data-stu-id="7a075-236">separator2</span></span> | <span data-ttu-id="7a075-237">日付の最後の 2 つのコンポーネント間で使用する区切り記号を示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-237">An enumeration value that indicates the separator to use between the last two components of the date.</span></span>                                                                                                        |
| <span data-ttu-id="7a075-238">年</span><span class="sxs-lookup"><span data-stu-id="7a075-238">year</span></span>       | <span data-ttu-id="7a075-239">日付に関する、年のコンポーネントの形式を示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-239">An enumeration value that indicates the format for the year component of the date.</span></span>                                                                                                                           |
| <span data-ttu-id="7a075-240">flags</span><span class="sxs-lookup"><span data-stu-id="7a075-240">flags</span></span>      | <span data-ttu-id="7a075-241">**DateFlags** は、ローカル コンピューター上の言語設定を使用して、返された文字列内の、左から右または右から左の順序が適切か計算する必要があるかどうかを示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-241">A **DateFlags** enumeration value that indicates whether the language settings on the local computer should be used to calculate the proper left-to-right or right-to-left sequence in the returned string.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-242">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-242">Return value</span></span>

<span data-ttu-id="7a075-243">指定日を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-243">A string that represents the specified date.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-244">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-244">Remarks</span></span>

<span data-ttu-id="7a075-245">MorphX は、指定された値が有効でない場合、書式設定パラメーターに有効な値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a075-245">MorphX allocates valid values to the formatting parameters if the specified values aren't valid.</span></span> <span data-ttu-id="7a075-246">地域設定で指定した日付形式を使用するには、**strFmt** または **date2Str** 関数を使用し、すべての書式設定パラメーターで **-1** を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a075-246">To use the date format that the user specified in Regional Settings, use the **strFmt** or **date2Str** function and specify **-1** in all the formatting parameters.</span></span> <span data-ttu-id="7a075-247">地域の設定が日付形式を制御するときは、その設定はユーザーごとに変更できます。</span><span class="sxs-lookup"><span data-stu-id="7a075-247">When the regional settings control the date format, the settings can change from user to user.</span></span> <span data-ttu-id="7a075-248">**-1** がいずれかの*区切り*パラメーターに使用されている場合、両方の区切りはデフォルトで地域設定になります。</span><span class="sxs-lookup"><span data-stu-id="7a075-248">If **-1** is used for either *separator* parameter, both separators default to Regional Settings.</span></span> <span data-ttu-id="7a075-249">*sequence* パラメーターの値は、桁 1、2、および 3 をそれぞれちょうど 1 回含む任意の 3 桁の数値にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a075-249">The *sequence* parameter values must be any three-digit number that contains exactly one occurrence of each the digits 1, 2 and 3.</span></span> <span data-ttu-id="7a075-250">数字 1、2、および 3 は、日、月、および年をそれぞれ表します。</span><span class="sxs-lookup"><span data-stu-id="7a075-250">The digits 1, 2, and 3 represent day, month, and year, respectively.</span></span> <span data-ttu-id="7a075-251">たとえば、**321** は連続する年、月、および日を生成します。</span><span class="sxs-lookup"><span data-stu-id="7a075-251">For example, **321** produces the sequence year, month, and day.</span></span> <span data-ttu-id="7a075-252">または、値は地域の設定を使う **-1** にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7a075-252">Or the value can be **-1** to use Regional Settings.</span></span> <span data-ttu-id="7a075-253">321 などの数字は、0 ～ 250 を含む列挙値の有効な値の範囲を超えているため、このパラメーターに使用する必要がある列挙型はありません。</span><span class="sxs-lookup"><span data-stu-id="7a075-253">No enumeration type should be used for this parameter, because numbers such as 321 exceed the range of valid values for enumeration values, which is 0 through 250, inclusive.</span></span> <span data-ttu-id="7a075-254">*フラグ* パラメーターの既定値は、**DateFlags::None** 列挙値で、左から右または右から左へのシーケンス処理は行われないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="7a075-254">The default value of the *flags* parameter is the **DateFlags::None** enumeration value, which means no left-to-right or right-to-left sequence processing is done.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-255">例</span><span class="sxs-lookup"><span data-stu-id="7a075-255">Example</span></span>

<span data-ttu-id="7a075-256">次の例では、現在の日付を年、月、日の順に表示します。</span><span class="sxs-lookup"><span data-stu-id="7a075-256">The following example displays the current date in the sequence of year, month, and day.</span></span>

    static void Job2(Args _args)
    {
            date currentDate = today();
            str s;
            int iEnum;
            s = date2Str
            (currentDate, 
                    321,
                    DateDay::Digits2,
                    DateSeparator::Hyphen, // separator1
                    DateMonth::Digits2,
                    DateSeparator::Hyphen, // separator2
                    DateYear::Digits4
            );
            info("Today is:  " + s);
    }
    /** Example Infolog output
    Message (12:36:21 pm)
    Today is:  2009-01-13
    **/

## <a name="datetime2str"></a><span data-ttu-id="7a075-257">datetime2Str</span><span class="sxs-lookup"><span data-stu-id="7a075-257">datetime2Str</span></span>
<span data-ttu-id="7a075-258">**utcdatetime** 値を文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-258">Converts a **utcdatetime** value into a string.</span></span>

    str datetime2Str(utcdatetime datetime [, int flags = DateFlags::None])

### <a name="parameters"></a><span data-ttu-id="7a075-259">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-259">Parameters</span></span>

| <span data-ttu-id="7a075-260">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-260">Parameter</span></span> | <span data-ttu-id="7a075-261">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-261">Description</span></span>                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a075-262">datetime</span><span class="sxs-lookup"><span data-stu-id="7a075-262">datetime</span></span>  | <span data-ttu-id="7a075-263">変換する **utcdatetime** 値。</span><span class="sxs-lookup"><span data-stu-id="7a075-263">The **utcdatetime** value to convert.</span></span>                                                                    |
| <span data-ttu-id="7a075-264">flags</span><span class="sxs-lookup"><span data-stu-id="7a075-264">flags</span></span>     | <span data-ttu-id="7a075-265">**DateFlags** は、右から左への出力にローカル設定を使用するかどうかを示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-265">A **DateFlags** enumeration value that indicates whether to use local settings for right-to-left output.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-266">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-266">Return value</span></span>

<span data-ttu-id="7a075-267">*datetime* パラメーターとして指定された **utcdatetime** 値を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-267">A string that represents the **utcdatetime** value that was specified as the *datetime* parameter.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-268">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-268">Remarks</span></span>

#### <a name="null-date-time-input"></a><span data-ttu-id="7a075-269">null の日付と時刻の入力</span><span class="sxs-lookup"><span data-stu-id="7a075-269">Null date-time input</span></span>

<span data-ttu-id="7a075-270">**utcdatetime** 値の最小値が *datetime* パラメーターに対して指定されている場合、**datetime2Str** 関数は null 入力値として扱われます。</span><span class="sxs-lookup"><span data-stu-id="7a075-270">If the minimum **utcdatetime** value is specified for the *datetime* parameter, the **datetime2Str** function treats it as a null input value.</span></span> <span data-ttu-id="7a075-271">これにより、関数は空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="7a075-271">This causes the function to return an empty string.</span></span> <span data-ttu-id="7a075-272">日時 **1900-01-01T00:00:00** は、**DateTimeUtil::minValue** メソッドによって返されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-272">The date-time **1900-01-01T00:00:00** is returned by the **DateTimeUtil::minValue** method.</span></span> <span data-ttu-id="7a075-273">この最小値は null として扱われます。</span><span class="sxs-lookup"><span data-stu-id="7a075-273">This minimum value is treated as null.</span></span>

#### <a name="right-to-left-local-settings"></a><span data-ttu-id="7a075-274">右から左 (ローカル設定)</span><span class="sxs-lookup"><span data-stu-id="7a075-274">Right-to-left local settings</span></span>

<span data-ttu-id="7a075-275">この関数の規定の動作では、左から右への順序で文字列を生成します。年の部分が一番左になります。</span><span class="sxs-lookup"><span data-stu-id="7a075-275">The default behavior of this function is to generate the string in left-to-right sequence, where the year portion is leftmost.</span></span> <span data-ttu-id="7a075-276">ただし、**DateFlags::FormatAll** 列挙値の*フラグ*パラメーター値は、ローカル設定が右から左に構成されている場合は、右から左の順序で文字列を生成するよう機能に指示します。</span><span class="sxs-lookup"><span data-stu-id="7a075-276">However, the *flags* parameter value of the **DateFlags::FormatAll** enumeration value directs the function to generate the string in right-to-left sequence if the local settings are configured for right-to-left.</span></span> <span data-ttu-id="7a075-277">**DateTimeUtil** クラスの **toStr** メソッドの形式は、地域設定の影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="7a075-277">The format of the **toStr** method of the **DateTimeUtil** class is unaffected by regional settings.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-278">例</span><span class="sxs-lookup"><span data-stu-id="7a075-278">Example</span></span>

    static void jobTestDatetime2str( Args _args )
    {
            utcdatetime utc2 = 1959-06-17T15:44:33;
            str s3;
            s3 = datetime2Str( utc2 );
            info( s3 );
    }

## <a name="enum2str"></a><span data-ttu-id="7a075-279">enum2Str</span><span class="sxs-lookup"><span data-stu-id="7a075-279">enum2Str</span></span>
<span data-ttu-id="7a075-280">指定された、列挙されたテキストを文字表現に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-280">Converts the specified enumerated text to a character representation.</span></span>

    str enum2Str(enum enum)

### <a name="parameters"></a><span data-ttu-id="7a075-281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-281">Parameters</span></span>

| <span data-ttu-id="7a075-282">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-282">Parameter</span></span> | <span data-ttu-id="7a075-283">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-283">Description</span></span>                     |
|-----------|---------------------------------|
| <span data-ttu-id="7a075-284">列挙型</span><span class="sxs-lookup"><span data-stu-id="7a075-284">enum</span></span>      | <span data-ttu-id="7a075-285">変換する列挙されたテキスト。</span><span class="sxs-lookup"><span data-stu-id="7a075-285">The enumerated text to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-286">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-286">Return value</span></span>

<span data-ttu-id="7a075-287">文字列形式での列挙値。</span><span class="sxs-lookup"><span data-stu-id="7a075-287">The value of the enumeration as a string.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-288">例</span><span class="sxs-lookup"><span data-stu-id="7a075-288">Example</span></span>

<span data-ttu-id="7a075-289">次の例では、文字列 "含まない" を返します。</span><span class="sxs-lookup"><span data-stu-id="7a075-289">The following example returns the string "Not included."</span></span> <span data-ttu-id="7a075-290">これは、**ListCode** 列挙型の **IncludeNot** 値のラベルです。</span><span class="sxs-lookup"><span data-stu-id="7a075-290">This is the label for the **IncludeNot** value of the **ListCode** enumeration type.</span></span>

    static void enum2StrExample(Args _arg)
    {
            ListCode l;
            l =  ListCode::IncludeNot;
            print enum2Str(l);
    }

## <a name="guid2str"></a><span data-ttu-id="7a075-291">guid2Str</span><span class="sxs-lookup"><span data-stu-id="7a075-291">guid2Str</span></span>
<span data-ttu-id="7a075-292">指定した GUID オブジェクトを等価の文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-292">Converts the specified GUID object to the equivalent string.</span></span>

    str guid2String(guid _uuid)

### <a name="parameters"></a><span data-ttu-id="7a075-293">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-293">Parameters</span></span>

| <span data-ttu-id="7a075-294">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-294">Parameter</span></span> | <span data-ttu-id="7a075-295">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-295">Description</span></span>                 |
|-----------|-----------------------------|
| <span data-ttu-id="7a075-296">\_uuid</span><span class="sxs-lookup"><span data-stu-id="7a075-296">\_uuid</span></span>    | <span data-ttu-id="7a075-297">変換する GUID オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7a075-297">The GUID object to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-298">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-298">Return value</span></span>

<span data-ttu-id="7a075-299">指定された GUID オブジェクトに等価の文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-299">The string equivalent of the specified GUID object.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-300">例</span><span class="sxs-lookup"><span data-stu-id="7a075-300">Example</span></span>

    static void guid2StrExample()
    {
            guid _guid;
            str stringGuid;
            _guid = Global::guidFromString("{12345678-1234-1234-1234-123456789abc}");
            print strfmt("GUID is %1", _guid);
            stringGuid = guid2str(_guid);
            info("String GUID is " + stringGuid);
    }
    /**** Output to Infolog
    String GUID is {12345678-1234-1234-1234-123456789ABC}
    ****/

## <a name="int2str"></a><span data-ttu-id="7a075-301">int2Str</span><span class="sxs-lookup"><span data-stu-id="7a075-301">int2Str</span></span>
<span data-ttu-id="7a075-302">整数を等価の文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-302">Converts an integer to the equivalent string.</span></span>

    str int2Str(int integer)

### <a name="parameters"></a><span data-ttu-id="7a075-303">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-303">Parameters</span></span>

| <span data-ttu-id="7a075-304">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-304">Parameter</span></span> | <span data-ttu-id="7a075-305">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-305">Description</span></span>             |
|-----------|-------------------------|
| <span data-ttu-id="7a075-306">integer</span><span class="sxs-lookup"><span data-stu-id="7a075-306">integer</span></span>   | <span data-ttu-id="7a075-307">変換する整数。</span><span class="sxs-lookup"><span data-stu-id="7a075-307">The integer to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-308">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-308">Return value</span></span>

<span data-ttu-id="7a075-309">整数の文字列表現。</span><span class="sxs-lookup"><span data-stu-id="7a075-309">A string representation of the integer.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-310">例</span><span class="sxs-lookup"><span data-stu-id="7a075-310">Example</span></span>

    static void int2StrExample(Args _arg)
    {
            print "This is int2Str, value is " + int2Str(intMax());
            print "This is int642Str, value is " + int642Str(int64Max());
    }

## <a name="int642str"></a><span data-ttu-id="7a075-311">int642Str</span><span class="sxs-lookup"><span data-stu-id="7a075-311">int642Str</span></span>
<span data-ttu-id="7a075-312">指定された*整数*パラメーターを等価のテキスト文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-312">Converts the specified *integer* parameter to the equivalent text string.</span></span>

    str int642Str(int64 integer)

### <a name="parameters"></a><span data-ttu-id="7a075-313">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-313">Parameters</span></span>

| <span data-ttu-id="7a075-314">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-314">Parameter</span></span> | <span data-ttu-id="7a075-315">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-315">Description</span></span>                       |
|-----------|-----------------------------------|
| <span data-ttu-id="7a075-316">integer</span><span class="sxs-lookup"><span data-stu-id="7a075-316">integer</span></span>   | <span data-ttu-id="7a075-317">文字列に変換する int64。</span><span class="sxs-lookup"><span data-stu-id="7a075-317">The int64 to convert to a string.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-318">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-318">Return value</span></span>

<span data-ttu-id="7a075-319">*整数* パラメーターの等価テキスト文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-319">The equivalent text string of the *integer* parameter.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-320">例</span><span class="sxs-lookup"><span data-stu-id="7a075-320">Example</span></span>

    static void example()
    {
            print "This is int2Str, value is " + int2Str(intMax());
            print "This is int642Str, value is " + int642Str(int64Max());
    }

## <a name="num2char"></a><span data-ttu-id="7a075-321">num2Char</span><span class="sxs-lookup"><span data-stu-id="7a075-321">num2Char</span></span>
<span data-ttu-id="7a075-322">整数を対応する ASCII 文字に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-322">Converts an integer to the corresponding ASCII character.</span></span>

    str num2Char(int figure)

### <a name="parameters"></a><span data-ttu-id="7a075-323">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-323">Parameters</span></span>

| <span data-ttu-id="7a075-324">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-324">Parameter</span></span> | <span data-ttu-id="7a075-325">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-325">Description</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="7a075-326">figure</span><span class="sxs-lookup"><span data-stu-id="7a075-326">figure</span></span>    | <span data-ttu-id="7a075-327">文字に変換する整数。</span><span class="sxs-lookup"><span data-stu-id="7a075-327">The integer to convert to a character.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-328">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-328">Return value</span></span>

<span data-ttu-id="7a075-329">指定した整数で表される文字。</span><span class="sxs-lookup"><span data-stu-id="7a075-329">The character that is represented by the specified integer.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-330">例</span><span class="sxs-lookup"><span data-stu-id="7a075-330">Example</span></span>

    static void num2CharExample(Args _arg)
    {
            str s;
            s = num2Char(42);
            // Prints an asterisk * -the character represented by 42.
            print s;
    }

## <a name="num2date"></a><span data-ttu-id="7a075-331">num2Date</span><span class="sxs-lookup"><span data-stu-id="7a075-331">num2Date</span></span>
<span data-ttu-id="7a075-332">1900 年 1 月 1 日から指定した日数に対応する日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="7a075-332">Retrieves the date that corresponds to the specified number of days after January 1, 1900.</span></span>

    date num2Date(int _days)

### <a name="parameters"></a><span data-ttu-id="7a075-333">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-333">Parameters</span></span>

| <span data-ttu-id="7a075-334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-334">Parameter</span></span> | <span data-ttu-id="7a075-335">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-335">Description</span></span>                                                                                                                                                                                                                |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a075-336">\_日</span><span class="sxs-lookup"><span data-stu-id="7a075-336">\_days</span></span>    | <span data-ttu-id="7a075-337">1900 年 1 月 1 日以降の日数を返します。</span><span class="sxs-lookup"><span data-stu-id="7a075-337">The number of days after January 1, 1900 to return the date for.</span></span> <span data-ttu-id="7a075-338">**注記:** 最初の有効日は 1901 年 1 月 1 日です。</span><span class="sxs-lookup"><span data-stu-id="7a075-338">**Note:** The first valid date is January 1, 1901.</span></span> <span data-ttu-id="7a075-339">したがって、**num2Date** 関数は、*\_days* が **365** を超えない限り、有効な日付を返しません。</span><span class="sxs-lookup"><span data-stu-id="7a075-339">Therefore, the **num2Date** function doesn't return a valid date unless *\_days* is more than **365**.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-340">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-340">Return value</span></span>

<span data-ttu-id="7a075-341">1900年1月1日以降に、*\_days* パラメーターで指定された日数の日付。</span><span class="sxs-lookup"><span data-stu-id="7a075-341">The date that is the number of days that is specified by the *\_days* parameter after January 1, 1900.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-342">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-342">Remarks</span></span>

    num2Date(366); //Returns the date 01/01/1901 (1 January 1901).

## <a name="num2str"></a><span data-ttu-id="7a075-343">num2Str</span><span class="sxs-lookup"><span data-stu-id="7a075-343">num2Str</span></span>
<span data-ttu-id="7a075-344">実数を文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-344">Converts a real number to a string.</span></span>

    str num2Str(real number, int character, int decimals, int separator1, int separator2)

### <a name="parameters"></a><span data-ttu-id="7a075-345">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-345">Parameters</span></span>

| <span data-ttu-id="7a075-346">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-346">Parameter</span></span>  | <span data-ttu-id="7a075-347">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-347">Description</span></span>                                                     |
|------------|-----------------------------------------------------------------|
| <span data-ttu-id="7a075-348">数値</span><span class="sxs-lookup"><span data-stu-id="7a075-348">number</span></span>     | <span data-ttu-id="7a075-349">文字列に変換する実数。</span><span class="sxs-lookup"><span data-stu-id="7a075-349">The real number to convert to a string.</span></span>                         |
| <span data-ttu-id="7a075-350">文字</span><span class="sxs-lookup"><span data-stu-id="7a075-350">character</span></span>  | <span data-ttu-id="7a075-351">テキストに必要な最小文字数。</span><span class="sxs-lookup"><span data-stu-id="7a075-351">The minimum number of characters that are required in the text.</span></span> |
| <span data-ttu-id="7a075-352">decimals</span><span class="sxs-lookup"><span data-stu-id="7a075-352">decimals</span></span>   | <span data-ttu-id="7a075-353">小数点以下の必要な桁数。</span><span class="sxs-lookup"><span data-stu-id="7a075-353">The required number of decimal places.</span></span>                          |
| <span data-ttu-id="7a075-354">separator1</span><span class="sxs-lookup"><span data-stu-id="7a075-354">separator1</span></span> | <span data-ttu-id="7a075-355">**DecimalSeparator** 列挙値。</span><span class="sxs-lookup"><span data-stu-id="7a075-355">A **DecimalSeparator** enumeration value.</span></span>                       |
| <span data-ttu-id="7a075-356">separator2</span><span class="sxs-lookup"><span data-stu-id="7a075-356">separator2</span></span> | <span data-ttu-id="7a075-357">**ThousandSeparator** 列挙値。</span><span class="sxs-lookup"><span data-stu-id="7a075-357">A **ThousandSeparator** enumeration value.</span></span>                      |

### <a name="return-value"></a><span data-ttu-id="7a075-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-358">Return value</span></span>

<span data-ttu-id="7a075-359">番号を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-359">A string that represents the number.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-360">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-360">Remarks</span></span>

<span data-ttu-id="7a075-361">*小数点以下*パラメーターについては、最大値は **16** です。</span><span class="sxs-lookup"><span data-stu-id="7a075-361">For the *decimals* parameter, the maximum value is **16**.</span></span> <span data-ttu-id="7a075-362">より大きい数値が使用された場合、このメソッドは*小数点以下*のパラメーターの値をローカル コンピューターから取得します。</span><span class="sxs-lookup"><span data-stu-id="7a075-362">If a larger number is used, this method obtains a value for the *decimals* parameter from the local computer instead.</span></span> <span data-ttu-id="7a075-363">どちらの場合も、丸めが発生します。</span><span class="sxs-lookup"><span data-stu-id="7a075-363">In both cases, rounding occurs.</span></span> <span data-ttu-id="7a075-364">*separator1* パラメータの使用可能な列挙値を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7a075-364">Here are the possible enumeration values for the *separator1* parameter:</span></span>

-   <span data-ttu-id="7a075-365">**1** - ポイント (.)</span><span class="sxs-lookup"><span data-stu-id="7a075-365">**1** – Point (.)</span></span>
-   <span data-ttu-id="7a075-366">**2** - コンマ (,)</span><span class="sxs-lookup"><span data-stu-id="7a075-366">**2** – Comma (,)</span></span>

<span data-ttu-id="7a075-367">*separator2* パラメータの使用可能な値を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7a075-367">Here are the possible values for the *separator2* parameter:</span></span>

-   <span data-ttu-id="7a075-368">**0**– 3 桁の区切り文字なし</span><span class="sxs-lookup"><span data-stu-id="7a075-368">**0 **– No thousands separator</span></span>
-   <span data-ttu-id="7a075-369">**1**– ポイント (.)</span><span class="sxs-lookup"><span data-stu-id="7a075-369">**1 **– Point (.)</span></span>
-   <span data-ttu-id="7a075-370">**2**– コンマ (,)</span><span class="sxs-lookup"><span data-stu-id="7a075-370">**2 **– Comma (,)</span></span>
-   <span data-ttu-id="7a075-371">**3**– スペース ( )</span><span class="sxs-lookup"><span data-stu-id="7a075-371">**3 **– Space ( )</span></span>

### <a name="example"></a><span data-ttu-id="7a075-372">例</span><span class="sxs-lookup"><span data-stu-id="7a075-372">Example</span></span>

<span data-ttu-id="7a075-373">次のコード例では、**num2str** メソッドの最初の呼び出しでは **16** が*小数点以下*のパラメーターに渡され、2 番目の呼び出しでは **17** が渡されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-373">In the following code example, the first call to the **num2str** method provides **16** for the *decimals* parameter, and the second call provides **17**.</span></span>

    static void Job_Num2Str(Args _args)
    {
            real realNum = 0.1294567890123456777; // 19 decimals places.
            info(Num2Str(realNum,0,16,1,3)); // 16 decimal places
            info(Num2Str(realNum,0,17,1,3)); // 17 decimal places
    }

### <a name="output"></a><span data-ttu-id="7a075-374">出力</span><span class="sxs-lookup"><span data-stu-id="7a075-374">Output</span></span>

<span data-ttu-id="7a075-375">メッセージは次の Infolog 出力にあります。</span><span class="sxs-lookup"><span data-stu-id="7a075-375">The messages are in the following Infolog output.</span></span> <span data-ttu-id="7a075-376">出力の最初の数字には 16 桁の小数が含まれ、2 番目の数字には小数点以下 2 桁の小数のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7a075-376">The first number in the output contains 16 decimal place digits, whereas the second number contains only two decimal place digits.</span></span>

    Message (10:18:12)
    0.1294567890123457
    0.13

## <a name="str2date"></a><span data-ttu-id="7a075-377">str2Date</span><span class="sxs-lookup"><span data-stu-id="7a075-377">str2Date</span></span>
<span data-ttu-id="7a075-378">指定された文字列を**データ**値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-378">Converts the specified string to a **date** value.</span></span>

    date str2Date(str _text, str _sequence)

### <a name="parameters"></a><span data-ttu-id="7a075-379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-379">Parameters</span></span>

| <span data-ttu-id="7a075-380">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-380">Parameter</span></span>  | <span data-ttu-id="7a075-381">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-381">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a075-382">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="7a075-382">\_text</span></span>     | <span data-ttu-id="7a075-383">**date** 値に変換する文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-383">The string to convert to a **date** value.</span></span>                                                               |
| <span data-ttu-id="7a075-384">\_順序</span><span class="sxs-lookup"><span data-stu-id="7a075-384">\_sequence</span></span> | <span data-ttu-id="7a075-385">変換する文字列の日、月、年の位置を表す 3 桁の整数。</span><span class="sxs-lookup"><span data-stu-id="7a075-385">A three-digit integer that describes the positions of the day, month, and year in the string to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-386">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-386">Return value</span></span>

<span data-ttu-id="7a075-387">**日付**値。</span><span class="sxs-lookup"><span data-stu-id="7a075-387">A **date** value.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-388">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-388">Remarks</span></span>

<span data-ttu-id="7a075-389">*\_sequence* パラメーターで日、月、年の位置を指定するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7a075-389">Use the following values to specify the positions of the day, month, and year in the *\_sequence* parameter:</span></span>

-   <span data-ttu-id="7a075-390">**日付:** 1</span><span class="sxs-lookup"><span data-stu-id="7a075-390">**Day:** 1</span></span>
-   <span data-ttu-id="7a075-391">**月:** 2</span><span class="sxs-lookup"><span data-stu-id="7a075-391">**Month:** 2</span></span>
-   <span data-ttu-id="7a075-392">**年:** 3</span><span class="sxs-lookup"><span data-stu-id="7a075-392">**Year:** 3</span></span>

<span data-ttu-id="7a075-393">たとえば、文字列の順序が月、年、さらに日である場合、*\_順序*パラメーターは **231** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a075-393">For example, if the sequence in the string is month, year, and then day, the *\_sequence* parameter must be **231**.</span></span> <span data-ttu-id="7a075-394">入力パラメーターが無効な日付を指定した場合、日付 **0**(ゼロ) が返されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-394">A **0** (zero) date is returned if the input parameters specify an invalid date.</span></span> <span data-ttu-id="7a075-395">次の 2 つの例では無効な日付を指定しています。</span><span class="sxs-lookup"><span data-stu-id="7a075-395">The following two examples specify an invalid date.</span></span>

    str2Date("31/12/44", 123) // Year must be four digits to reach the minimum of January 1 1901.
    str2Date("31/12/2044", 213) // 213 means the month occurs first in the string, but 31 cannot be a month.

### <a name="example"></a><span data-ttu-id="7a075-396">例</span><span class="sxs-lookup"><span data-stu-id="7a075-396">Example</span></span>

    static void str2DateExample(Args _arg)
    {
            date d;
            d = str2Date("22/11/2007", 123);
            print d;
    }

## <a name="str2datetime"></a><span data-ttu-id="7a075-397">str2Datetime</span><span class="sxs-lookup"><span data-stu-id="7a075-397">str2Datetime</span></span>
<span data-ttu-id="7a075-398">日付と時刻情報の指定した文字列から **utcdatetime** 値を生成します。</span><span class="sxs-lookup"><span data-stu-id="7a075-398">Generates a **utcdatetime** value from the specified string of date and time information.</span></span>

    utcdatetime str2datetime( str text, int sequence )

### <a name="parameters"></a><span data-ttu-id="7a075-399">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-399">Parameters</span></span>

| <span data-ttu-id="7a075-400">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-400">Parameter</span></span> | <span data-ttu-id="7a075-401">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-401">Description</span></span>                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a075-402">テキスト</span><span class="sxs-lookup"><span data-stu-id="7a075-402">text</span></span>      | <span data-ttu-id="7a075-403">**utcdatetime** 値に変換する文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-403">The string to convert to a **utcdatetime** value.</span></span>                                                |
| <span data-ttu-id="7a075-404">順序</span><span class="sxs-lookup"><span data-stu-id="7a075-404">sequence</span></span>  | <span data-ttu-id="7a075-405">*テキスト* パラメーターの日付コンポーネントの順序を示す 3 桁の番号。</span><span class="sxs-lookup"><span data-stu-id="7a075-405">A three-digit number that describes the sequence of the date components in the *text* parameter.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-406">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-406">Return value</span></span>

<span data-ttu-id="7a075-407">**utcdatetime** 値は、指定された日付と時刻を表します。</span><span class="sxs-lookup"><span data-stu-id="7a075-407">A **utcdatetime** value that represents the specified date and time.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-408">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-408">Remarks</span></span>

<span data-ttu-id="7a075-409">*text* パラメーターの日付部分の構文要件は柔軟性があります。</span><span class="sxs-lookup"><span data-stu-id="7a075-409">The syntax requirements for the date portion of the *text* parameter are flexible.</span></span> <span data-ttu-id="7a075-410">有効な形式のバリエーションは、**date2str** 関数と同じです。</span><span class="sxs-lookup"><span data-stu-id="7a075-410">The variety of valid formats is the same as in the **date2str** function.</span></span> <span data-ttu-id="7a075-411">**str2datetime** への以下の呼び出しはそれぞれ有効です。またそれらすべての出力は同じです。</span><span class="sxs-lookup"><span data-stu-id="7a075-411">Each of the following calls to **str2datetime** is valid, and all of them produce the same output.</span></span>

    utc3 = str2datetime( "1985/02/25 23:04:59" ,321 );
    utc3 = str2datetime( "Feb-1985-25 11:04:59 pm" ,231 );
    utc3 = str2datetime( "2 25 1985 11:04:59 pm" ,123 );

<span data-ttu-id="7a075-412">各コンポーネントの日時は、*シーケンス*パラメーター内の数字で表されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-412">Each component of the date time is represented by a digit in the *sequence* parameter:</span></span>

-   <span data-ttu-id="7a075-413">**1** - 日</span><span class="sxs-lookup"><span data-stu-id="7a075-413">**1** – Day</span></span>
-   <span data-ttu-id="7a075-414">**2** - 月</span><span class="sxs-lookup"><span data-stu-id="7a075-414">**2** – Month</span></span>
-   <span data-ttu-id="7a075-415">**3** - 年</span><span class="sxs-lookup"><span data-stu-id="7a075-415">**3** – Year</span></span>

<span data-ttu-id="7a075-416">たとえば、年、月、日の順序は **321** です。</span><span class="sxs-lookup"><span data-stu-id="7a075-416">For example, year, month, day order is **321**.</span></span> <span data-ttu-id="7a075-417">すべての有効な値には、これらの 3 桁の数字がそれぞれ正確に 1 回含まれます。</span><span class="sxs-lookup"><span data-stu-id="7a075-417">All valid values contain each of these three digits exactly one time.</span></span> <span data-ttu-id="7a075-418">*順序*パラメーターの値が無効である場合、入力*テキスト* パラメーターを解釈するために地域の設定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-418">If the value of the *sequence* parameter isn't valid, the regional settings are used to interpret the input *text* parameter.</span></span> <span data-ttu-id="7a075-419">入力パラメーターに無効な日付と時刻が表示されている場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="7a075-419">If the input parameters describe an invalid date and time, an empty string is returned.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-420">例</span><span class="sxs-lookup"><span data-stu-id="7a075-420">Example</span></span>

    static void JobTestStr2datetime( Args _args )
    {
            utcdatetime utc3;
            str sTemp;
            utc3 = str2datetime( "1985/02/25 23:04:59" ,321 );
            sTemp = datetime2str( utc3 );
            print( "sTemp == " + sTemp );
    }

## <a name="str2enum"></a><span data-ttu-id="7a075-421">str2Enum</span><span class="sxs-lookup"><span data-stu-id="7a075-421">str2Enum</span></span>
<span data-ttu-id="7a075-422">ローカライズされた **Label** プロパティ値が入力文字列に一致する列挙要素を取得します。</span><span class="sxs-lookup"><span data-stu-id="7a075-422">Retrieves the enum element for which the localized **Label** property value matches the input string.</span></span>

    enum str2Enum(enum _type, str _text)

### <a name="parameters"></a><span data-ttu-id="7a075-423">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-423">Parameters</span></span>

| <span data-ttu-id="7a075-424">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-424">Parameter</span></span> | <span data-ttu-id="7a075-425">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-425">Description</span></span>                                                              |
|-----------|--------------------------------------------------------------------------|
| <span data-ttu-id="7a075-426">\_タイプ</span><span class="sxs-lookup"><span data-stu-id="7a075-426">\_type</span></span>    | <span data-ttu-id="7a075-427">**列挙**型の宣言された変数。</span><span class="sxs-lookup"><span data-stu-id="7a075-427">A variable that is declared of the **enum** type.</span></span>                        |
| <span data-ttu-id="7a075-428">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="7a075-428">\_text</span></span>    | <span data-ttu-id="7a075-429">列挙型内のターゲット要素のローカライズ **ラベル** プロパティのテキスト。</span><span class="sxs-lookup"><span data-stu-id="7a075-429">The localized **Label** property text of the target element in the enum.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-430">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-430">Return value</span></span>

<span data-ttu-id="7a075-431">ターゲット列挙の要素で、int も表します。</span><span class="sxs-lookup"><span data-stu-id="7a075-431">An element of the target enum, which also represents an int.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-432">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-432">Remarks</span></span>

<span data-ttu-id="7a075-433">関連関数 **enum2str** は列挙型の 1 要素から **Label** プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="7a075-433">The related function **enum2str** returns the value of a **Label** property from one element in the enum.</span></span> <span data-ttu-id="7a075-434">**enum2str** 関数により返された値は、**str2enum** 関数の *\_type* パラメーターの入力となります。</span><span class="sxs-lookup"><span data-stu-id="7a075-434">The value that is returned by **enum2str** function can be the input for the *\_type* parameter of the **str2enum** function.</span></span> <span data-ttu-id="7a075-435">*\_テキスト*パラメータは **enum2Str(BankAccountType::SavingsAccount)** の適切な値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-435">An appropriate value for the *\_text* parameter is **enum2Str(BankAccountType::SavingsAccount)**.</span></span> <span data-ttu-id="7a075-436">各列挙型要素には、**名前**プロパティおよび**ラベル**プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7a075-436">Each element of an enum has a **Name** property and a **Label** property.</span></span> <span data-ttu-id="7a075-437">新規インストールでは、**名前**の値はほぼ必ず英語です。</span><span class="sxs-lookup"><span data-stu-id="7a075-437">In a fresh install, the **Name** values are almost always English words.</span></span> <span data-ttu-id="7a075-438">英語版では、**ラベル**のプロパティ値がほとんどの場合、**名前**の値と同じです。</span><span class="sxs-lookup"><span data-stu-id="7a075-438">In the English edition, the **Label** property value is almost always the same as the **Name** value.</span></span> <span data-ttu-id="7a075-439">ただし、英語以外のエディションでは、**ラベル**値はローカライズされるため**名前**値とは一致しません。</span><span class="sxs-lookup"><span data-stu-id="7a075-439">However, in non-English editions, the **Label** values are localized and therefore don't match the **Name** values.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-440">例</span><span class="sxs-lookup"><span data-stu-id="7a075-440">Example</span></span>

<span data-ttu-id="7a075-441">他の言語にローカライズされたために発生する文字列の不一致を避けるために、**str2enum** 関数への入力を生成するには **enum2str** 関数を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7a075-441">To avoid string mismatches that are caused by localization to other spoken languages, we recommend that you use the **enum2str** function to generate the input into the **str2enum** function.</span></span> <span data-ttu-id="7a075-442">次の例は、**str2enum** 関数と **enum2str** 関数を併用する適切な方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7a075-442">The following example shows the appropriate way to use the **str2enum** function together with the **enum2str** function.</span></span>

    static void str2Enum_AcrossLangs(Args _arg)
    {
            BankAccountType bat;
            str sEnumValueLabelLocalized;
            int nInt;
            // enum2str.
            sEnumValueLabelLocalized = enum2str(BankAccountType::SavingsAccount);
            info("Localized friendly string: "
                    + sEnumValueLabelLocalized);
            // str2enum.
            bat = str2Enum(bat, sEnumValueLabelLocalized);
            nInt = bat;
            info("nInt = " + int2str(nInt));
            /********** Actual output:
            Message (04:32:12 pm)
            Localized friendly string: Savings account
            nInt = 1
            **********/
    }

## <a name="str2guid"></a><span data-ttu-id="7a075-443">str2Guid</span><span class="sxs-lookup"><span data-stu-id="7a075-443">str2Guid</span></span>
<span data-ttu-id="7a075-444">文字列を GUID オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-444">Converts a string to a GUID object.</span></span>

    Guid str2Guid(str text)

### <a name="parameters"></a><span data-ttu-id="7a075-445">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-445">Parameters</span></span>

| <span data-ttu-id="7a075-446">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-446">Parameter</span></span> | <span data-ttu-id="7a075-447">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-447">Description</span></span>                      |
|-----------|----------------------------------|
| <span data-ttu-id="7a075-448">guid</span><span class="sxs-lookup"><span data-stu-id="7a075-448">guid</span></span>      | <span data-ttu-id="7a075-449">GUID を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-449">A string that represents a GUID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-450">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-450">Return value</span></span>

<span data-ttu-id="7a075-451">入力文字列で表される GUID。</span><span class="sxs-lookup"><span data-stu-id="7a075-451">A GUID that is represented by the input string.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-452">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-452">Remarks</span></span>

<span data-ttu-id="7a075-453">たとえば、*GUID* パラメータの有効な値は **{12345678-1234-abCD-3456-123456789012}** で、かっこ付きまたはかっこなしのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="7a075-453">For example, a valid value for the *guid* parameter is **{12345678-1234-abCD-3456-123456789012}**, either with or without the braces.</span></span>

## <a name="str2int"></a><span data-ttu-id="7a075-454">str2Int</span><span class="sxs-lookup"><span data-stu-id="7a075-454">str2Int</span></span>
<span data-ttu-id="7a075-455">文字列を等価の整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-455">Converts a string to the equivalent integer.</span></span>

    int str2Int(str _text)

### <a name="parameters"></a><span data-ttu-id="7a075-456">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-456">Parameters</span></span>

| <span data-ttu-id="7a075-457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-457">Parameter</span></span> | <span data-ttu-id="7a075-458">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-458">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="7a075-459">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="7a075-459">\_text</span></span>    | <span data-ttu-id="7a075-460">整数に変換する文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-460">The string to convert to an integer.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-461">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-461">Return value</span></span>

<span data-ttu-id="7a075-462">指定された文字列の等価整数。</span><span class="sxs-lookup"><span data-stu-id="7a075-462">The integer equivalent of the specified string.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-463">例</span><span class="sxs-lookup"><span data-stu-id="7a075-463">Example</span></span>

    static void str2IntExample(Args _arg)
    {
            int i;
            i = str2Int("1234567890");
            print "i = " + int2Str(i);
    }

## <a name="str2int64"></a><span data-ttu-id="7a075-464">str2Int64</span><span class="sxs-lookup"><span data-stu-id="7a075-464">str2Int64</span></span>
<span data-ttu-id="7a075-465">文字列を **Int64** 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-465">Converts a string into an **Int64** value.</span></span>

    int str2Int64(str text)

### <a name="parameters"></a><span data-ttu-id="7a075-466">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-466">Parameters</span></span>

| <span data-ttu-id="7a075-467">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-467">Parameter</span></span> | <span data-ttu-id="7a075-468">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-468">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="7a075-469">テキスト</span><span class="sxs-lookup"><span data-stu-id="7a075-469">text</span></span>      | <span data-ttu-id="7a075-470">変換する文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-470">The string to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-471">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-471">Return value</span></span>

<span data-ttu-id="7a075-472">指定された文字列の **Int64** 値。</span><span class="sxs-lookup"><span data-stu-id="7a075-472">The **Int64** value of the specified string.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-473">例</span><span class="sxs-lookup"><span data-stu-id="7a075-473">Example</span></span>

    static void str2Int64Example(Args _args)
    {
            str myStr;
            str tooBig;
            Int64 myInt64;
            myStr = "1234567890";
            tooBig = int642str(int64Max()+1);
            myInt64 = str2Int64(mystr);
            print strfmt ("int64: %1",myInt64);
            myInt64 = str2Int64(tooBig);
            print strfmt ("Too big int64: %1",myInt64);
    }

## <a name="str2num"></a><span data-ttu-id="7a075-474">str2Num</span><span class="sxs-lookup"><span data-stu-id="7a075-474">str2Num</span></span>
<span data-ttu-id="7a075-475">文字列を実数に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-475">Converts a string to a real number.</span></span>

    real str2Num(str _text)

### <a name="parameters"></a><span data-ttu-id="7a075-476">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-476">Parameters</span></span>

| <span data-ttu-id="7a075-477">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-477">Parameter</span></span> | <span data-ttu-id="7a075-478">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-478">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="7a075-479">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="7a075-479">\_text</span></span>    | <span data-ttu-id="7a075-480">実数に変換する文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-480">The string to convert to a real number.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-481">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-481">Return value</span></span>

<span data-ttu-id="7a075-482">指定された文字列に有効な数値が含まれている場合の実数。それ以外の場合は **0** (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7a075-482">The real number if the specified string contains a valid number; otherwise, **0** (zero).</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-483">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-483">Remarks</span></span>

<span data-ttu-id="7a075-484">次の例では、この関数の使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7a075-484">The following examples show how this function is used.</span></span>

    str2Num("123.45") returns the value 123.45.
    str2Num("a123") returns the value 0.0.
    str2Num("123a") returns the value 123.00.

<span data-ttu-id="7a075-485">スキャンは左から右に行われ、文字を実数の一部に変換できなくなると終了します。</span><span class="sxs-lookup"><span data-stu-id="7a075-485">Scanning occurs from left to right and ends when a character can't be converted to part of a real number.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-486">例</span><span class="sxs-lookup"><span data-stu-id="7a075-486">Example</span></span>

    static void str2NumToReal(Args _arg)
    {
            real r;
            str s;
            r = str2Num("3.15");
            s = strFmt("r = %1", r);
            info(s);
    }
    /*** Infolog output.
    Message_@SYS14327 (02:36:12 pm)
    r = 3.15
    ***/

    static void str2NumExponentialSyntax(Args _args)
    {
            Qty qty1, qty2, qty3;
            qty1 = str2num('1e-3'); // Bad syntax by the user.
            qty2 = str2num('1.e-3');
            qty3 = str2num('1.0e-3');
            info(strfmt('Result: %1; Expected: %2', num2str(qty1, 0,3,2,0), '0.001'));
            info(strfmt('Result: %1; Expected: %2', num2str(qty2, 0,3,2,0), '0.001'));
            info(strfmt('Result: %1; Expected: %2', num2str(qty3, 0,3,2,0), '0.001'));
    }
    /*** Infolog output. The first result differs from expectations.
    Message_@SYS14327 (02:20:55 pm)
    Result: 1,000; Expected: 0.001
    Result: 0,001; Expected: 0.001
    Result: 0,001; Expected: 0.001
    ***/

## <a name="str2time"></a><span data-ttu-id="7a075-487">str2Time</span><span class="sxs-lookup"><span data-stu-id="7a075-487">str2Time</span></span>
<span data-ttu-id="7a075-488">文字列を **timeOfDay** 値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-488">Converts a string to a **timeOfDay** value.</span></span>

    int str2Time(str _text)

### <a name="parameters"></a><span data-ttu-id="7a075-489">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-489">Parameters</span></span>

| <span data-ttu-id="7a075-490">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-490">Parameter</span></span> | <span data-ttu-id="7a075-491">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-491">Description</span></span>                                                        |
|-----------|--------------------------------------------------------------------|
| <span data-ttu-id="7a075-492">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="7a075-492">\_text</span></span>    | <span data-ttu-id="7a075-493">深夜からの秒数を計算するために使用する時間。</span><span class="sxs-lookup"><span data-stu-id="7a075-493">The time to use to calculate the number of seconds since midnight.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-494">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-494">Return value</span></span>

<span data-ttu-id="7a075-495">真夜中と *\_text* パラメーターの間の秒数。 そうでなければ、**-1**。</span><span class="sxs-lookup"><span data-stu-id="7a075-495">The number of seconds between midnight and the *\_text* parameter; otherwise, **-1**.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-496">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-496">Remarks</span></span>

    str2Time("05:01:37") //Returns the value 18097.
    str2Time("7 o'clock") //Returns the value -1.

### <a name="example"></a><span data-ttu-id="7a075-497">例</span><span class="sxs-lookup"><span data-stu-id="7a075-497">Example</span></span>

    static void str2TimeExample(Args _arg)
    {
            int i;
            i = str2Time("11:30");
            print i;
    }

## <a name="time2str"></a><span data-ttu-id="7a075-498">time2Str</span><span class="sxs-lookup"><span data-stu-id="7a075-498">time2Str</span></span>
<span data-ttu-id="7a075-499">**timeOfDay** 値を時、分、秒を含む文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-499">Converts a **timeOfDay** value to a string that includes hours, minutes, and seconds.</span></span>

    str time2Str(int _time, int _separator, int _timeFormat)

### <a name="parameters"></a><span data-ttu-id="7a075-500">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-500">Parameters</span></span>

| <span data-ttu-id="7a075-501">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-501">Parameter</span></span>    | <span data-ttu-id="7a075-502">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-502">Description</span></span>                                                                                                                       |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a075-503">\_タイム</span><span class="sxs-lookup"><span data-stu-id="7a075-503">\_time</span></span>       | <span data-ttu-id="7a075-504">**timeOfDay** 値。</span><span class="sxs-lookup"><span data-stu-id="7a075-504">A **timeOfDay** value.</span></span>                                                                                                            |
| <span data-ttu-id="7a075-505">\_区切り記号</span><span class="sxs-lookup"><span data-stu-id="7a075-505">\_separator</span></span>  | <span data-ttu-id="7a075-506">**TimeSeparator** は、出力文字列の時、分、秒の間の文字を示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-506">A **TimeSeparator** enumeration value that indicates the characters between the hours, minutes, and seconds in the output string.</span></span> |
| <span data-ttu-id="7a075-507">\_timeFormat</span><span class="sxs-lookup"><span data-stu-id="7a075-507">\_timeFormat</span></span> | <span data-ttu-id="7a075-508">**TimeFormat** は、12時間制または24時間制のどちらを使用するかを示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="7a075-508">A **TimeFormat** enumeration value that indicates whether a 12-hour clock or a 24-hour clock is used.</span></span>                             |

### <a name="return-value"></a><span data-ttu-id="7a075-509">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-509">Return value</span></span>

<span data-ttu-id="7a075-510">指定された時間を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-510">A string that represents the specified time.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-511">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-511">Remarks</span></span>

<span data-ttu-id="7a075-512">*\_time* パラメーターの値は、深夜 0 時からの秒数です。</span><span class="sxs-lookup"><span data-stu-id="7a075-512">The value of the *\_time* parameter is the number of seconds since midnight.</span></span>

### <a name="example"></a><span data-ttu-id="7a075-513">例</span><span class="sxs-lookup"><span data-stu-id="7a075-513">Example</span></span>

    static void TimeJob4(Args _args)
    {
            timeOfDay theTime = timeNow();
            info( time2Str(theTime, TimeSeparator::Colon, TimeFormat::AMPM) );
    }
    /**
    Message (04:33:56 pm)
    04:33:56 pm
    **/

## <a name="uint2str"></a><span data-ttu-id="7a075-514">uint2Str</span><span class="sxs-lookup"><span data-stu-id="7a075-514">uint2Str</span></span>
<span data-ttu-id="7a075-515">整数を文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7a075-515">Converts an integer to a string.</span></span> <span data-ttu-id="7a075-516">整数が符号なしであることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="7a075-516">The assumption is that the integer is unsigned.</span></span>

    str uint2Str(int integer)

### <a name="parameters"></a><span data-ttu-id="7a075-517">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-517">Parameters</span></span>

| <span data-ttu-id="7a075-518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a075-518">Parameter</span></span> | <span data-ttu-id="7a075-519">説明</span><span class="sxs-lookup"><span data-stu-id="7a075-519">Description</span></span>             |
|-----------|-------------------------|
| <span data-ttu-id="7a075-520">integer</span><span class="sxs-lookup"><span data-stu-id="7a075-520">integer</span></span>   | <span data-ttu-id="7a075-521">変換する整数。</span><span class="sxs-lookup"><span data-stu-id="7a075-521">The integer to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="7a075-522">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a075-522">Return value</span></span>

<span data-ttu-id="7a075-523">指定された符号なし整数に同等の文字列。</span><span class="sxs-lookup"><span data-stu-id="7a075-523">The string equivalent to the specified unsigned integer.</span></span>

### <a name="remarks"></a><span data-ttu-id="7a075-524">備考</span><span class="sxs-lookup"><span data-stu-id="7a075-524">Remarks</span></span>

<span data-ttu-id="7a075-525">レコード ID などの非常に大きな整数の場合は、**int2str** 関数の代わりにこの関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="7a075-525">Use this function instead of the **int2str** function for very large integers, such as record IDs.</span></span>

    info(int2str(3123456789)); //returns -1171510507 as a string.
    info(uint2str(3123456789)); //returns 3123456789 as a string.



