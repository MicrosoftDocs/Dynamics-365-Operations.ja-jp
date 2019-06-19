---
title: X++ コンパイル時関数
description: このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29581
ms.assetid: fa6613a4-7d0b-40d3-be29-9d14c22c7d5b
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e9438ef0764399ac9de3444330d05a47e72e5f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544182"
---
# <a name="x-compile-time-functions"></a><span data-ttu-id="6babe-103">X++ コンパイル時関数</span><span class="sxs-lookup"><span data-stu-id="6babe-103">X++ compile-time functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6babe-104">このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。</span><span class="sxs-lookup"><span data-stu-id="6babe-104">This topic lists the compile-time functions and describes their syntax, parameters, and return values.</span></span>

<a name="overview"></a><span data-ttu-id="6babe-105">概要</span><span class="sxs-lookup"><span data-stu-id="6babe-105">Overview</span></span>
--------

<span data-ttu-id="6babe-106">コンパイル時関数は、X++ コードのコンパイル時に早期実行されます。</span><span class="sxs-lookup"><span data-stu-id="6babe-106">Compile-time functions are executed early during compilation of X++ code.</span></span> <span data-ttu-id="6babe-107">アプリケーション エクスプローラーに保存されているメタデータの変更に対してコードを復元するためには、可能な限り X++ で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6babe-107">They should be used wherever possible in X++ code to make the code resilient to changes to the metadata stored in the Application Explorer.</span></span> <span data-ttu-id="6babe-108">コンパイル時関数は、コンパイラによって入力値が検証されます。</span><span class="sxs-lookup"><span data-stu-id="6babe-108">Compile-time functions have their input value verified by the compiler.</span></span> <span data-ttu-id="6babe-109">入力された値が見つからず、アプリケーション エクスプローラーの既存のオブジェクトが一致しない場合は、コンパイラーはエラーを発行します。</span><span class="sxs-lookup"><span data-stu-id="6babe-109">If the input value is not found to match any existing object in the Application Explorer, the compiler issues an error.</span></span> <span data-ttu-id="6babe-110">コンパイラは実行時に変数に含まれる値を判別できないため、これらの関数への入力はリテラルでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6babe-110">The inputs to these functions must be literals, because the compiler cannot determine the value that a variable contains at run time.</span></span> <span data-ttu-id="6babe-111">コンパイル時関数は、メタデータ アサーション関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-111">A compile-time function is a metadata assertion function.</span></span> <span data-ttu-id="6babe-112">アプリケーション エクスプローラーでエンティティを表す引数を取得し、コンパイル時にその引数を検証します。</span><span class="sxs-lookup"><span data-stu-id="6babe-112">It takes arguments that represents an entity in the Application Explorer and validates the arguments at compile time.</span></span> <span data-ttu-id="6babe-113">実行時に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="6babe-113">It has no effect at run time.</span></span> <span data-ttu-id="6babe-114">属性は **SysAttribute** クラスから継承するクラスです。</span><span class="sxs-lookup"><span data-stu-id="6babe-114">Attributes are classes that inherit from the **SysAttribute** class.</span></span> <span data-ttu-id="6babe-115">フォーム、レポート、クエリ、メニュー のメタデータの検証をサポートするには、コントロールの **AutoDeclaration** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6babe-115">To support the validation of form, report, query, and menu metadata, use the **AutoDeclaration** property on controls.</span></span> <span data-ttu-id="6babe-116">これらの機能のほとんどは、アプリケーション エクスプローラーにある項目に関するメタデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-116">Most of these functions retrieve metadata about items that are in the Application Explorer.</span></span> <span data-ttu-id="6babe-117">いくつかの一般的なコンパイル時機能は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6babe-117">Some common compile time functions are as follows:</span></span>

-   <span data-ttu-id="6babe-118">`classNum` – クラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-118">`classNum` – Retrieves the ID of a class.</span></span>
-   <span data-ttu-id="6babe-119">`classStr` – コンパイル時に、その名前のクラスが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="6babe-119">`classStr` – During compile time, verifies that a class of that name exists.</span></span> <span data-ttu-id="6babe-120">この方法は、実行時にエラーを後で発見するよりも優れています。</span><span class="sxs-lookup"><span data-stu-id="6babe-120">This approach is better than discovering the error later during run time.</span></span>
-   <span data-ttu-id="6babe-121">`evalBuf`– X++ コードの入力文字列を評価し、結果を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-121">`evalBuf`– Evaluates the input string of X++ code, and then returns the results as a string.</span></span>
-   <span data-ttu-id="6babe-122">`literalStr` – は、文字列 `"@SYS12345"` などのラベルの文字列表示が与えられたときにラベル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-122">`literalStr` – retrieves a label ID when given the string representation of a label, such as the string `"@SYS12345"`.</span></span> <span data-ttu-id="6babe-123">たとえば、`myLabel.exists(literalStr("@SYS12345"));`。</span><span class="sxs-lookup"><span data-stu-id="6babe-123">For example, `myLabel.exists(literalStr("@SYS12345"));`.</span></span>

| <span data-ttu-id="6babe-124">**メモ**</span><span class="sxs-lookup"><span data-stu-id="6babe-124">**Note**</span></span>                                                         |
|------------------------------------------------------------------|
| <span data-ttu-id="6babe-125">X++ コンパイル時関数は .NET プログラムから呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="6babe-125">X++ compile time functions cannot be called from a .NET program.</span></span> |

### <a name="functions"></a><span data-ttu-id="6babe-126">関数</span><span class="sxs-lookup"><span data-stu-id="6babe-126">Functions</span></span>

## <a name="attributestr"></a><span data-ttu-id="6babe-127">attributeStr</span><span class="sxs-lookup"><span data-stu-id="6babe-127">attributeStr</span></span>
<span data-ttu-id="6babe-128">指定した属性クラスがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-128">Validates that the specified attribute class exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-129">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-129">Syntax</span></span>

    str classStr(class class)

### <a name="parameters"></a><span data-ttu-id="6babe-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-130">Parameters</span></span>

| <span data-ttu-id="6babe-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-131">Parameter</span></span> | <span data-ttu-id="6babe-132">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-132">Description</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="6babe-133">クラス</span><span class="sxs-lookup"><span data-stu-id="6babe-133">class</span></span>     | <span data-ttu-id="6babe-134">検証する属性の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-134">The name of the attribute to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-135">Return Value</span></span>

<span data-ttu-id="6babe-136">属性の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-136">The name of the attribute.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-137">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-137">Remarks</span></span>

<span data-ttu-id="6babe-138">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-138">This is a compile-time function.</span></span> <span data-ttu-id="6babe-139">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-139">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-140">例</span><span class="sxs-lookup"><span data-stu-id="6babe-140">Example</span></span>

    static void attributeStrExample(Args _args)
    {
        str s;
        ;
        s = attributeStr(AifDocumentOperationAttribute);
        print s;
        pause;
    }

## <a name="classnum"></a><span data-ttu-id="6babe-141">classNum</span><span class="sxs-lookup"><span data-stu-id="6babe-141">classNum</span></span>
<span data-ttu-id="6babe-142">指定されたクラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-142">Retrieves the ID of the specified class.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-143">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-143">Syntax</span></span>

    int classNum(class class)

### <a name="parameters"></a><span data-ttu-id="6babe-144">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-144">Parameters</span></span>

| <span data-ttu-id="6babe-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-145">Parameter</span></span> | <span data-ttu-id="6babe-146">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-146">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="6babe-147">クラス</span><span class="sxs-lookup"><span data-stu-id="6babe-147">class</span></span>     | <span data-ttu-id="6babe-148">ID を取得するクラス。</span><span class="sxs-lookup"><span data-stu-id="6babe-148">The class for which to retrieve the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-149">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-149">Return Value</span></span>

<span data-ttu-id="6babe-150">指定されたクラスの ID。</span><span class="sxs-lookup"><span data-stu-id="6babe-150">The ID of the specified class.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-151">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-151">Remarks</span></span>

<span data-ttu-id="6babe-152">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-152">This is a compile-time function.</span></span> <span data-ttu-id="6babe-153">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-153">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-154">例</span><span class="sxs-lookup"><span data-stu-id="6babe-154">Example</span></span>

    static void classNumExample(Args _args)
    {
        int i;
        ;
        i = classNum(Global);
        print i;
        pause;
    }

## <a name="classstr"></a><span data-ttu-id="6babe-155">classStr</span><span class="sxs-lookup"><span data-stu-id="6babe-155">classStr</span></span>
<span data-ttu-id="6babe-156">文字列としてクラスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-156">Retrieves the name of a class as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-157">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-157">Syntax</span></span>

    str classStr(class class)

### <a name="parameters"></a><span data-ttu-id="6babe-158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-158">Parameters</span></span>

| <span data-ttu-id="6babe-159">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-159">Parameter</span></span> | <span data-ttu-id="6babe-160">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-160">Description</span></span>                      |
|-----------|----------------------------------|
| <span data-ttu-id="6babe-161">クラス</span><span class="sxs-lookup"><span data-stu-id="6babe-161">class</span></span>     | <span data-ttu-id="6babe-162">返すクラスの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-162">The name of the class to return.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-163">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-163">Return Value</span></span>

<span data-ttu-id="6babe-164">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-164">The name of the class.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-165">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-165">Remarks</span></span>

<span data-ttu-id="6babe-166">リテラル テキストの代わりにこの関数を使用して、クラス名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-166">Use this function instead of literal text to retrieve a string that contains the class name.</span></span> <span data-ttu-id="6babe-167">クラスが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="6babe-167">If the class does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="6babe-168">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-168">This is a compile-time function.</span></span> <span data-ttu-id="6babe-169">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-169">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-170">例</span><span class="sxs-lookup"><span data-stu-id="6babe-170">Example</span></span>

    static void clStrExample(Args _args)
    {
        str s;
        ;
        s = classStr(Global);
        print s;
        pause;
    }

## <a name="configurationkeynum"></a><span data-ttu-id="6babe-171">configurationKeyNum</span><span class="sxs-lookup"><span data-stu-id="6babe-171">configurationKeyNum</span></span>
<span data-ttu-id="6babe-172">指定されたコンフィギュレーション キーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-172">Retrieves the ID of the specified configuration key.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-173">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-173">Syntax</span></span>

    int configurationKeyNum(str keyname)

### <a name="parameters"></a><span data-ttu-id="6babe-174">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-174">Parameters</span></span>

| <span data-ttu-id="6babe-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-175">Parameter</span></span> | <span data-ttu-id="6babe-176">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-176">Description</span></span>                                       |
|-----------|---------------------------------------------------|
| <span data-ttu-id="6babe-177">keyname</span><span class="sxs-lookup"><span data-stu-id="6babe-177">keyname</span></span>   | <span data-ttu-id="6babe-178">ID を返すコンフィギュレーション キー。</span><span class="sxs-lookup"><span data-stu-id="6babe-178">The configuration key for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-179">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-179">Return Value</span></span>

<span data-ttu-id="6babe-180">指定されたコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="6babe-180">The ID of the specified configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-181">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-181">Remarks</span></span>

<span data-ttu-id="6babe-182">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-182">This is a compile-time function.</span></span> <span data-ttu-id="6babe-183">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-183">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-184">例</span><span class="sxs-lookup"><span data-stu-id="6babe-184">Example</span></span>

    static void configurationKeyNum(Args _args)
    {
        int i;
        ;
        i = configurationKeyNum(AIF);
        print i;
        pause;
    }

## <a name="configurationkeystr"></a><span data-ttu-id="6babe-185">configurationKeyStr</span><span class="sxs-lookup"><span data-stu-id="6babe-185">configurationKeyStr</span></span>
<span data-ttu-id="6babe-186">文字列としてコンフィギュレーション キーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-186">Retrieves the name of a configuration key as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-187">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-187">Syntax</span></span>

    str configurationKeyStr(str keyname)

### <a name="parameters"></a><span data-ttu-id="6babe-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-188">Parameters</span></span>

| <span data-ttu-id="6babe-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-189">Parameter</span></span> | <span data-ttu-id="6babe-190">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-190">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="6babe-191">keyname</span><span class="sxs-lookup"><span data-stu-id="6babe-191">keyname</span></span>   | <span data-ttu-id="6babe-192">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-192">The name of the configuration key.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-193">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-193">Return Value</span></span>

<span data-ttu-id="6babe-194">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-194">The name of the configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-195">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-195">Remarks</span></span>

<span data-ttu-id="6babe-196">リテラル テキストの代わりにこの関数を使用して、構成キー名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-196">Use this function instead of literal text to retrieve a string that contains the configuration key name.</span></span> <span data-ttu-id="6babe-197">キーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="6babe-197">If the key does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="6babe-198">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-198">This is a compile-time function.</span></span> <span data-ttu-id="6babe-199">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-199">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-200">例</span><span class="sxs-lookup"><span data-stu-id="6babe-200">Example</span></span>

    static void configurationKeyStrExample(Args _args)
    {
        str s;
        ;
        s = configurationKeyStr(AIF);
        print s;
        pause;
    }

## <a name="dataentitydatasourcestr"></a><span data-ttu-id="6babe-201">dataEntityDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="6babe-201">dataEntityDataSourceStr</span></span>
<span data-ttu-id="6babe-202">データ エンティティのデータ ソースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-202">Retrieves the name of a data source of a data entity.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-203">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-203">Syntax</span></span>

    str dataEntityDataSourceStr(str dataEntity, str dataSource)

### <a name="parameters"></a><span data-ttu-id="6babe-204">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-204">Parameters</span></span>

| <span data-ttu-id="6babe-205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-205">Parameter</span></span>  | <span data-ttu-id="6babe-206">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-206">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="6babe-207">dataEntity</span><span class="sxs-lookup"><span data-stu-id="6babe-207">dataEntity</span></span> | <span data-ttu-id="6babe-208">データ エンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-208">The name of the data entity.</span></span> |
| <span data-ttu-id="6babe-209">dataSource</span><span class="sxs-lookup"><span data-stu-id="6babe-209">dataSource</span></span> | <span data-ttu-id="6babe-210">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-210">The name of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-211">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-211">Return Value</span></span>

<span data-ttu-id="6babe-212">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-212">The name of the data source.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-213">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-213">Remarks</span></span>

<span data-ttu-id="6babe-214">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-214">This is a compile-time function.</span></span> <span data-ttu-id="6babe-215">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-215">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-216">例</span><span class="sxs-lookup"><span data-stu-id="6babe-216">Example</span></span>

    No example.

## <a name="delegatestr"></a><span data-ttu-id="6babe-217">delegateStr</span><span class="sxs-lookup"><span data-stu-id="6babe-217">delegateStr</span></span>
<span data-ttu-id="6babe-218">委任の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-218">Returns the name of the delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-219">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-219">Syntax</span></span>

    str delegateStr(str class, str instanceDelegate)

### <a name="parameters"></a><span data-ttu-id="6babe-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-220">Parameters</span></span>

| <span data-ttu-id="6babe-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-221">Parameter</span></span>        | <span data-ttu-id="6babe-222">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-222">Description</span></span>                            |
|------------------|----------------------------------------|
| <span data-ttu-id="6babe-223">クラス</span><span class="sxs-lookup"><span data-stu-id="6babe-223">class</span></span>            | <span data-ttu-id="6babe-224">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-224">The name of the class, table, or form.</span></span> |
| <span data-ttu-id="6babe-225">instanceDelegate</span><span class="sxs-lookup"><span data-stu-id="6babe-225">instanceDelegate</span></span> | <span data-ttu-id="6babe-226">インスタンス デリゲートの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-226">The name of the instance delegate.</span></span>     |

### <a name="return-value"></a><span data-ttu-id="6babe-227">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-227">Return Value</span></span>

<span data-ttu-id="6babe-228">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="6babe-228">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-229">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-229">Remarks</span></span>

<span data-ttu-id="6babe-230">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-230">This is a compile-time function.</span></span> <span data-ttu-id="6babe-231">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-231">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-232">例</span><span class="sxs-lookup"><span data-stu-id="6babe-232">Example</span></span>

    No example.

## <a name="dimensionhierarchylevelstr"></a><span data-ttu-id="6babe-233">dimensionHierarchyLevelStr</span><span class="sxs-lookup"><span data-stu-id="6babe-233">dimensionHierarchyLevelStr</span></span>
<span data-ttu-id="6babe-234">分析コード階層レベルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-234">Returns the name of the dimension hierarchy level.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-235">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-235">Syntax</span></span>

    str dimensionHierarchyLevelStr(str dimensionHierarchyLevel)

### <a name="parameters"></a><span data-ttu-id="6babe-236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-236">Parameters</span></span>

| <span data-ttu-id="6babe-237">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-237">Parameter</span></span>               | <span data-ttu-id="6babe-238">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-238">Description</span></span>                                |
|-------------------------|--------------------------------------------|
| <span data-ttu-id="6babe-239">dimensionHierarchyLevel</span><span class="sxs-lookup"><span data-stu-id="6babe-239">dimensionHierarchyLevel</span></span> | <span data-ttu-id="6babe-240">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-240">The name of the dimension hierarchy level.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-241">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-241">Return Value</span></span>

<span data-ttu-id="6babe-242">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-242">The name of the dimension hierarchy level.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-243">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-243">Remarks</span></span>

<span data-ttu-id="6babe-244">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-244">This is a compile-time function.</span></span> <span data-ttu-id="6babe-245">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-245">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-246">例</span><span class="sxs-lookup"><span data-stu-id="6babe-246">Example</span></span>

    No example.

## <a name="dimensionhierarchystr"></a><span data-ttu-id="6babe-247">dimensionHierarchyStr</span><span class="sxs-lookup"><span data-stu-id="6babe-247">dimensionHierarchyStr</span></span>
<span data-ttu-id="6babe-248">分析コード階層の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-248">Returns the name of the dimension hierarchy.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-249">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-249">Syntax</span></span>

    str dimensionHierarchyStr(str dimensionHierarchy)

### <a name="parameters"></a><span data-ttu-id="6babe-250">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-250">Parameters</span></span>

| <span data-ttu-id="6babe-251">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-251">Parameter</span></span>          | <span data-ttu-id="6babe-252">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-252">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="6babe-253">dimensionHierarchy</span><span class="sxs-lookup"><span data-stu-id="6babe-253">dimensionHierarchy</span></span> | <span data-ttu-id="6babe-254">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-254">The name of the dimension hierarchy.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-255">Return Value</span></span>

<span data-ttu-id="6babe-256">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-256">The name of the dimension hierarchy.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-257">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-257">Remarks</span></span>

<span data-ttu-id="6babe-258">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-258">This is a compile-time function.</span></span> <span data-ttu-id="6babe-259">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-259">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-260">例</span><span class="sxs-lookup"><span data-stu-id="6babe-260">Example</span></span>

    No example.

## <a name="dimensionreferencestr"></a><span data-ttu-id="6babe-261">dimensionReferenceStr</span><span class="sxs-lookup"><span data-stu-id="6babe-261">dimensionReferenceStr</span></span>
<span data-ttu-id="6babe-262">分析コード参照の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-262">Returns the name of the dimension reference.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-263">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-263">Syntax</span></span>

    str dimensionReferenceStr(str dimensionReference)

### <a name="parameters"></a><span data-ttu-id="6babe-264">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-264">Parameters</span></span>

| <span data-ttu-id="6babe-265">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-265">Parameter</span></span>          | <span data-ttu-id="6babe-266">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-266">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="6babe-267">dimensionReference</span><span class="sxs-lookup"><span data-stu-id="6babe-267">dimensionReference</span></span> | <span data-ttu-id="6babe-268">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-268">The name of the dimension reference.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-269">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-269">Return Value</span></span>

<span data-ttu-id="6babe-270">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-270">The name of the dimension reference.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-271">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-271">Remarks</span></span>

<span data-ttu-id="6babe-272">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-272">This is a compile-time function.</span></span> <span data-ttu-id="6babe-273">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-273">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-274">例</span><span class="sxs-lookup"><span data-stu-id="6babe-274">Example</span></span>

    No example.

## <a name="dutystr"></a><span data-ttu-id="6babe-275">dutyStr</span><span class="sxs-lookup"><span data-stu-id="6babe-275">dutyStr</span></span>
<span data-ttu-id="6babe-276">指定したセキュリティ職務権限の名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-276">Retrieves a string that represents the name of the specified security duty.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-277">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-277">Syntax</span></span>

    str dutyStr(str securityDuty)

### <a name="parameters"></a><span data-ttu-id="6babe-278">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-278">Parameters</span></span>

| <span data-ttu-id="6babe-279">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-279">Parameter</span></span>    | <span data-ttu-id="6babe-280">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-280">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="6babe-281">securityDuty</span><span class="sxs-lookup"><span data-stu-id="6babe-281">securityDuty</span></span> | <span data-ttu-id="6babe-282">セキュリティ職務権限の名前です。</span><span class="sxs-lookup"><span data-stu-id="6babe-282">The name of the security duty.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-283">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-283">Return Value</span></span>

<span data-ttu-id="6babe-284">文字列のセキュリティ職務の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-284">The name of the security duty in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-285">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-285">Remarks</span></span>

<span data-ttu-id="6babe-286">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-286">This is a compile-time function.</span></span> <span data-ttu-id="6babe-287">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-287">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-288">例</span><span class="sxs-lookup"><span data-stu-id="6babe-288">Example</span></span>

    No example.

## <a name="enumcnt"></a><span data-ttu-id="6babe-289">enumCnt</span><span class="sxs-lookup"><span data-stu-id="6babe-289">enumCnt</span></span>
<span data-ttu-id="6babe-290">指定された列挙型の要素数を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-290">Retrieves the number of elements in the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-291">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-291">Syntax</span></span>

    int enumCnt(enum enumtype)

### <a name="parameters"></a><span data-ttu-id="6babe-292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-292">Parameters</span></span>

| <span data-ttu-id="6babe-293">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-293">Parameter</span></span> | <span data-ttu-id="6babe-294">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-294">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="6babe-295">enumtype</span><span class="sxs-lookup"><span data-stu-id="6babe-295">enumtype</span></span>  | <span data-ttu-id="6babe-296">列挙型タイプ。</span><span class="sxs-lookup"><span data-stu-id="6babe-296">The enumeration type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-297">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-297">Return Value</span></span>

<span data-ttu-id="6babe-298">指定された列挙型の要素数。</span><span class="sxs-lookup"><span data-stu-id="6babe-298">The number of elements in the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-299">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-299">Remarks</span></span>

<span data-ttu-id="6babe-300">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-300">This is a compile-time function.</span></span> <span data-ttu-id="6babe-301">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-301">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-302">例</span><span class="sxs-lookup"><span data-stu-id="6babe-302">Example</span></span>

    enumCnt(NoYes); //Returns 2, as the two elements are Yes and No.

## <a name="enumliteralstr"></a><span data-ttu-id="6babe-303">enumLiteralStr</span><span class="sxs-lookup"><span data-stu-id="6babe-303">enumLiteralStr</span></span>
<span data-ttu-id="6babe-304">指定した文字列が指定した列挙型の要素であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6babe-304">Indicates whether the specified string is an element of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-305">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-305">Syntax</span></span>

    enumLiteralStr(enum enum, string str)

### <a name="parameters"></a><span data-ttu-id="6babe-306">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-306">Parameters</span></span>

| <span data-ttu-id="6babe-307">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-307">Parameter</span></span> | <span data-ttu-id="6babe-308">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-308">Description</span></span>                                                      |
|-----------|------------------------------------------------------------------|
| <span data-ttu-id="6babe-309">列挙型</span><span class="sxs-lookup"><span data-stu-id="6babe-309">enum</span></span>      | <span data-ttu-id="6babe-310">指定された値を取得する列挙型。</span><span class="sxs-lookup"><span data-stu-id="6babe-310">The enumeration type from which to retrieve the specified value.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-311">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-311">Return Value</span></span>

<span data-ttu-id="6babe-312">指定された文字列が見つかった場合の *str* パラメーターの値。それ以外の場合は、コンパイル エラーです。</span><span class="sxs-lookup"><span data-stu-id="6babe-312">The value of the *str* parameter if the specified string was found; otherwise, a compilation error.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-313">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-313">Remarks</span></span>

<span data-ttu-id="6babe-314">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-314">This is a compile-time function.</span></span> <span data-ttu-id="6babe-315">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-315">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-316">例</span><span class="sxs-lookup"><span data-stu-id="6babe-316">Example</span></span>

    static void getEnumValueAsString()
    {
        str i;
        i = enumLiteralStr(ABCEnum, "valueInABCEnum");
        print i;
        pause;
    }

## <a name="enumnum"></a><span data-ttu-id="6babe-317">enumNum</span><span class="sxs-lookup"><span data-stu-id="6babe-317">enumNum</span></span>
<span data-ttu-id="6babe-318">指定された列挙型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-318">Retrieves the ID of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-319">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-319">Syntax</span></span>

    int enumNum(enum enum)

### <a name="parameters"></a><span data-ttu-id="6babe-320">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-320">Parameters</span></span>

| <span data-ttu-id="6babe-321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-321">Parameter</span></span> | <span data-ttu-id="6babe-322">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-322">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="6babe-323">列挙型</span><span class="sxs-lookup"><span data-stu-id="6babe-323">enum</span></span>      | <span data-ttu-id="6babe-324">ID を返す列挙。</span><span class="sxs-lookup"><span data-stu-id="6babe-324">The enumeration for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-325">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-325">Return Value</span></span>

<span data-ttu-id="6babe-326">指定された列挙型の ID。</span><span class="sxs-lookup"><span data-stu-id="6babe-326">The ID of the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-327">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-327">Remarks</span></span>

<span data-ttu-id="6babe-328">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-328">This is a compile-time function.</span></span> <span data-ttu-id="6babe-329">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-329">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-330">例</span><span class="sxs-lookup"><span data-stu-id="6babe-330">Example</span></span>

    static void enumNum(Args _args)
    {
        int i;
        ;
        i = enumNum(ABC);
        print i;
        pause;
    }

## <a name="enumstr"></a><span data-ttu-id="6babe-331">enumStr</span><span class="sxs-lookup"><span data-stu-id="6babe-331">enumStr</span></span>
<span data-ttu-id="6babe-332">文字列として列挙型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-332">Retrieves the name of an enumeration as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-333">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-333">Syntax</span></span>

    str enumStr(enum enum)

### <a name="parameters"></a><span data-ttu-id="6babe-334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-334">Parameters</span></span>

| <span data-ttu-id="6babe-335">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-335">Parameter</span></span> | <span data-ttu-id="6babe-336">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-336">Description</span></span>                  |
|-----------|------------------------------|
| <span data-ttu-id="6babe-337">列挙型</span><span class="sxs-lookup"><span data-stu-id="6babe-337">enum</span></span>      | <span data-ttu-id="6babe-338">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-338">The name of the enumeration.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-339">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-339">Return Value</span></span>

<span data-ttu-id="6babe-340">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-340">The name of the enumeration.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-341">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-341">Remarks</span></span>

<span data-ttu-id="6babe-342">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-342">This is a compile-time function.</span></span> <span data-ttu-id="6babe-343">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-343">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-344">例</span><span class="sxs-lookup"><span data-stu-id="6babe-344">Example</span></span>

    static void enumStrExample(Args _args)
    {
        str s;
        ;
        s = enumStr(ABC);
        print s;
        pause;
    }

## <a name="extendedtypenum"></a><span data-ttu-id="6babe-345">extendedTypeNum</span><span class="sxs-lookup"><span data-stu-id="6babe-345">extendedTypeNum</span></span>
<span data-ttu-id="6babe-346">指定された拡張データ型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-346">Retrieves the ID of the specified extended data type.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-347">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-347">Syntax</span></span>

    int extendedTypeNum(int str)

### <a name="parameters"></a><span data-ttu-id="6babe-348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-348">Parameters</span></span>

| <span data-ttu-id="6babe-349">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-349">Parameter</span></span> | <span data-ttu-id="6babe-350">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-350">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="6babe-351">str</span><span class="sxs-lookup"><span data-stu-id="6babe-351">str</span></span>       | <span data-ttu-id="6babe-352">ID を返す拡張データ型。</span><span class="sxs-lookup"><span data-stu-id="6babe-352">The extended data type for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-353">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-353">Return Value</span></span>

<span data-ttu-id="6babe-354">指定された拡張データ型の ID。</span><span class="sxs-lookup"><span data-stu-id="6babe-354">The ID of the specified extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-355">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-355">Remarks</span></span>

<span data-ttu-id="6babe-356">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-356">This is a compile-time function.</span></span> <span data-ttu-id="6babe-357">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-357">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-358">例</span><span class="sxs-lookup"><span data-stu-id="6babe-358">Example</span></span>

    static void EDTNum(Args _args)
    {
        int i;
        str s;
        ;

        i = extendedTypeNum(AccountName);
        s = extendedTypeStr(AccountName);
        print  int2Str(i);
        print  s;
        pause;
    }

## <a name="extendedtypestr"></a><span data-ttu-id="6babe-359">extendedTypeStr</span><span class="sxs-lookup"><span data-stu-id="6babe-359">extendedTypeStr</span></span>
<span data-ttu-id="6babe-360">文字列として拡張データ型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-360">Retrieves the name of an extended data type as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-361">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-361">Syntax</span></span>

    str extendedTypeStr(int str)

### <a name="parameters"></a><span data-ttu-id="6babe-362">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-362">Parameters</span></span>

| <span data-ttu-id="6babe-363">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-363">Parameter</span></span> | <span data-ttu-id="6babe-364">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-364">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="6babe-365">str</span><span class="sxs-lookup"><span data-stu-id="6babe-365">str</span></span>       | <span data-ttu-id="6babe-366">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-366">The name of the extended data type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-367">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-367">Return Value</span></span>

<span data-ttu-id="6babe-368">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-368">The name of the extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-369">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-369">Remarks</span></span>

<span data-ttu-id="6babe-370">リテラル テキストの代わりにこの関数を使用すると、拡張データ型名を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-370">Use this function instead of literal text to return a string that contains the extended data type name.</span></span> <span data-ttu-id="6babe-371">データ タイプが存在しない場合、**extendedTypeStr** 関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="6babe-371">If the data type does not exist, the **extendedTypeStr** function generates a syntax error at compile time.</span></span> <span data-ttu-id="6babe-372">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-372">This is a compile-time function.</span></span> <span data-ttu-id="6babe-373">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-373">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-374">例</span><span class="sxs-lookup"><span data-stu-id="6babe-374">Example</span></span>

    static void EDTStr(Args _args)
    {
        int i;
        str s;
        ;

        i = extendedTypeNum(AccountName);
        s = extendedTypeStr(AccountName);
        print  int2Str(i);
        print  s;
        pause;
    }

## <a name="fieldnum"></a><span data-ttu-id="6babe-375">fieldNum</span><span class="sxs-lookup"><span data-stu-id="6babe-375">fieldNum</span></span>
<span data-ttu-id="6babe-376">指定したフィールドの ID 番号を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-376">Returns the ID number of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-377">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-377">Syntax</span></span>

    int fieldNum(str tableName, str fieldName)

### <a name="parameters"></a><span data-ttu-id="6babe-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-378">Parameters</span></span>

| <span data-ttu-id="6babe-379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-379">Parameter</span></span> | <span data-ttu-id="6babe-380">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-380">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="6babe-381">tableName</span><span class="sxs-lookup"><span data-stu-id="6babe-381">tableName</span></span> | <span data-ttu-id="6babe-382">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-382">The name of the table.</span></span> |
| <span data-ttu-id="6babe-383">fieldName</span><span class="sxs-lookup"><span data-stu-id="6babe-383">fieldName</span></span> | <span data-ttu-id="6babe-384">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-384">The name of the field.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-385">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-385">Return Value</span></span>

<span data-ttu-id="6babe-386">指定されたフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="6babe-386">The ID of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-387">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-387">Remarks</span></span>

<span data-ttu-id="6babe-388">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-388">This is a compile-time function.</span></span> <span data-ttu-id="6babe-389">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-389">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-390">例</span><span class="sxs-lookup"><span data-stu-id="6babe-390">Example</span></span>

<span data-ttu-id="6babe-391">次の例では、**CashDisc** フィールドの番号を **CustTable** テーブルに出力します。</span><span class="sxs-lookup"><span data-stu-id="6babe-391">The following example prints the number of the **CashDisc** field in the **CustTable** table.</span></span>

    static void fieldNumExample(Args _args)
    {
        int myInt;
        ;

        myInt = fieldNum(CustTable, CashDisc);
        Global::info(strfmt("CashDisc has a field ID of %1 in the CustTable table.", myInt));
    }
    /****Infolog Display
    Message (10:40:00 am)
    CashDisc has a field ID of 10 in the CustTable table.
    ****/

## <a name="fieldpname"></a><span data-ttu-id="6babe-392">fieldPName</span><span class="sxs-lookup"><span data-stu-id="6babe-392">fieldPName</span></span>
<span data-ttu-id="6babe-393">指定されたフィールドのラベルを取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-393">Retrieves the label of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-394">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-394">Syntax</span></span>

    str fieldPName(str tableid, str fieldid)

### <a name="parameters"></a><span data-ttu-id="6babe-395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-395">Parameters</span></span>

| <span data-ttu-id="6babe-396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-396">Parameter</span></span> | <span data-ttu-id="6babe-397">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-397">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="6babe-398">tableid</span><span class="sxs-lookup"><span data-stu-id="6babe-398">tableid</span></span>   | <span data-ttu-id="6babe-399">指定されたフィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="6babe-399">The table that contains the specified field.</span></span> |
| <span data-ttu-id="6babe-400">fieldid</span><span class="sxs-lookup"><span data-stu-id="6babe-400">fieldid</span></span>   | <span data-ttu-id="6babe-401">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="6babe-401">The field to convert.</span></span>                        |

### <a name="return-value"></a><span data-ttu-id="6babe-402">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-402">Return Value</span></span>

<span data-ttu-id="6babe-403">フィールドのラベル。</span><span class="sxs-lookup"><span data-stu-id="6babe-403">The label of the field.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-404">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-404">Remarks</span></span>

<span data-ttu-id="6babe-405">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-405">This is a compile-time function.</span></span> <span data-ttu-id="6babe-406">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-406">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-407">例</span><span class="sxs-lookup"><span data-stu-id="6babe-407">Example</span></span>

<span data-ttu-id="6babe-408">次の例では、**CashDisc** フィールドのラベルを出力します。</span><span class="sxs-lookup"><span data-stu-id="6babe-408">The following example prints the label of the **CashDisc** field.</span></span>

    static void fieldPNameExample(Args _arg)
    {
        str myText;
        ;

        myText = fieldPName(CustTable, CashDisc);
        Global::info(strfmt("%1 is the label of the CashDisc field.", myText));
    }
    /****Infolog Display
    Message (02:00:57 pm)
    Cash discount is the label of the CashDisc field.
    ****/

## <a name="fieldstr"></a><span data-ttu-id="6babe-409">fieldStr</span><span class="sxs-lookup"><span data-stu-id="6babe-409">fieldStr</span></span>
<span data-ttu-id="6babe-410">指定したフィールドのフィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-410">Retrieves the field name of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-411">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-411">Syntax</span></span>

    str fieldStr(str tableid, str fieldid)

### <a name="parameters"></a><span data-ttu-id="6babe-412">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-412">Parameters</span></span>

| <span data-ttu-id="6babe-413">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-413">Parameter</span></span> | <span data-ttu-id="6babe-414">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-414">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="6babe-415">tableid</span><span class="sxs-lookup"><span data-stu-id="6babe-415">tableid</span></span>   | <span data-ttu-id="6babe-416">フィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="6babe-416">The table that contains the field.</span></span> |
| <span data-ttu-id="6babe-417">fieldid</span><span class="sxs-lookup"><span data-stu-id="6babe-417">fieldid</span></span>   | <span data-ttu-id="6babe-418">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="6babe-418">The field to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="6babe-419">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-419">Return Value</span></span>

<span data-ttu-id="6babe-420">指定したフィールドのフィールド名。</span><span class="sxs-lookup"><span data-stu-id="6babe-420">The field name of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-421">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-421">Remarks</span></span>

<span data-ttu-id="6babe-422">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-422">This is a compile-time function.</span></span> <span data-ttu-id="6babe-423">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-423">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-424">例</span><span class="sxs-lookup"><span data-stu-id="6babe-424">Example</span></span>

<span data-ttu-id="6babe-425">次の例では、**CashDisc** フィールドの名前を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6babe-425">The following example assigns the name of the **CashDisc** field to the *myText* variable.</span></span>

    static void fieldStrExample(Args _arg)
    {
        str myText;
        ;

        myText = fieldStr(CustTable, CashDisc);
        Global::info(strfmt("%1 is the specified field.", myText));
    }
    /****Infolog Display
    Message (09:11:52 am)
    CashDisc is the specified field.
    ****/

## <a name="formcontrolstr"></a><span data-ttu-id="6babe-426">formControlStr</span><span class="sxs-lookup"><span data-stu-id="6babe-426">formControlStr</span></span>
<span data-ttu-id="6babe-427">X++ コンパイラは、コントロールがフォームに存在するかどうかをチェックし、関数呼び出しを有効なコントロール名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6babe-427">Causes the X++ compiler to check whether the control exists on the form, and to replace the function call with a string of the valid control name.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-428">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-428">Syntax</span></span>

    str formControlStr(formName, controlName)

### <a name="parameters"></a><span data-ttu-id="6babe-429">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-429">Parameters</span></span>

| <span data-ttu-id="6babe-430">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-430">Parameter</span></span>   | <span data-ttu-id="6babe-431">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-431">Description</span></span>                                                          |
|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="6babe-432">formName</span><span class="sxs-lookup"><span data-stu-id="6babe-432">formName</span></span>    | <span data-ttu-id="6babe-433">引用符ではなく、フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-433">The name of the form, not in quotation marks.</span></span>                        |
| <span data-ttu-id="6babe-434">controlName</span><span class="sxs-lookup"><span data-stu-id="6babe-434">controlName</span></span> | <span data-ttu-id="6babe-435">フォーム上のコントロールの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="6babe-435">The name of the control that is on the form, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-436">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-436">Return Value</span></span>

<span data-ttu-id="6babe-437">アプリケーション エクスプローラーで表示されるコントロールの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-437">A string that contains the name of the control as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-438">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-438">Remarks</span></span>

<span data-ttu-id="6babe-439">コントロールがフォームに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6babe-439">A compile error is issued if the compiler determines that the control does not exist on the form.</span></span> <span data-ttu-id="6babe-440">X++ コードが引用符が含まれる文字列を使用してコントロールの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="6babe-440">If your X++ code uses a string that contains quotation marks to supply the control name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="6babe-441">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="6babe-441">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="6babe-442">コンパイラにより実行される **formControlStr** などの X++ 関数は、コンパイル時関数と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6babe-442">X++ functions such as **formControlStr** that are executed by the compiler are called compile-time functions or compile-time functions.</span></span> <span data-ttu-id="6babe-443">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="6babe-443">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="6babe-444">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="6babe-444">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="6babe-445">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-445">This is a compile-time function.</span></span> <span data-ttu-id="6babe-446">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-446">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-447">例</span><span class="sxs-lookup"><span data-stu-id="6babe-447">Example</span></span>

    No example.

## <a name="formdatafieldstr"></a><span data-ttu-id="6babe-448">formDataFieldStr</span><span class="sxs-lookup"><span data-stu-id="6babe-448">formDataFieldStr</span></span>
<span data-ttu-id="6babe-449">フォームのデータ フィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-449">Returns the name of a data field in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-450">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-450">Syntax</span></span>

    str formDataFieldStr(str formName, str dataSource, str dataField)

### <a name="parameters"></a><span data-ttu-id="6babe-451">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-451">Parameters</span></span>

| <span data-ttu-id="6babe-452">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-452">Parameter</span></span>  | <span data-ttu-id="6babe-453">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-453">Description</span></span>                        |
|------------|------------------------------------|
| <span data-ttu-id="6babe-454">formName</span><span class="sxs-lookup"><span data-stu-id="6babe-454">formName</span></span>   | <span data-ttu-id="6babe-455">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-455">The name of the form.</span></span>              |
| <span data-ttu-id="6babe-456">dataSource</span><span class="sxs-lookup"><span data-stu-id="6babe-456">dataSource</span></span> | <span data-ttu-id="6babe-457">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="6babe-457">The data source of the form.</span></span>       |
| <span data-ttu-id="6babe-458">dataField</span><span class="sxs-lookup"><span data-stu-id="6babe-458">dataField</span></span>  | <span data-ttu-id="6babe-459">データ ソースのデータ フィールド。</span><span class="sxs-lookup"><span data-stu-id="6babe-459">The data field of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-460">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-460">Return Value</span></span>

<span data-ttu-id="6babe-461">フォームのデータ フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-461">The name of a data field in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-462">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-462">Remarks</span></span>

<span data-ttu-id="6babe-463">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-463">This is a compile-time function.</span></span> <span data-ttu-id="6babe-464">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-464">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-465">例</span><span class="sxs-lookup"><span data-stu-id="6babe-465">Example</span></span>

    str a = formDataFieldStr(FMVehicle, FMModelRate, RatePerDay);

## <a name="formdatasourcestr"></a><span data-ttu-id="6babe-466">formDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="6babe-466">formDataSourceStr</span></span>
<span data-ttu-id="6babe-467">フォームのデータ ソースの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-467">Returns the name of a data source in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-468">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-468">Syntax</span></span>

    str formDataSourceStr(str formName, str dataSource)

### <a name="parameters"></a><span data-ttu-id="6babe-469">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-469">Parameters</span></span>

| <span data-ttu-id="6babe-470">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-470">Parameter</span></span>  | <span data-ttu-id="6babe-471">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-471">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="6babe-472">formName</span><span class="sxs-lookup"><span data-stu-id="6babe-472">formName</span></span>   | <span data-ttu-id="6babe-473">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-473">The name of the form.</span></span>        |
| <span data-ttu-id="6babe-474">dataSource</span><span class="sxs-lookup"><span data-stu-id="6babe-474">dataSource</span></span> | <span data-ttu-id="6babe-475">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="6babe-475">The data source of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-476">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-476">Return Value</span></span>

<span data-ttu-id="6babe-477">フォームのデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-477">The name of a data source in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-478">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-478">Remarks</span></span>

<span data-ttu-id="6babe-479">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-479">This is a compile-time function.</span></span> <span data-ttu-id="6babe-480">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-480">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-481">例</span><span class="sxs-lookup"><span data-stu-id="6babe-481">Example</span></span>

    str b = formDataSourceStr(FMVehicle, FMModelRate);

## <a name="formmethodstr"></a><span data-ttu-id="6babe-482">formMethodStr</span><span class="sxs-lookup"><span data-stu-id="6babe-482">formMethodStr</span></span>
<span data-ttu-id="6babe-483">フォームのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-483">Returns the name of a method of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-484">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-484">Syntax</span></span>

    str formMethodStr(str formName, str methodName)

### <a name="parameters"></a><span data-ttu-id="6babe-485">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-485">Parameters</span></span>

| <span data-ttu-id="6babe-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-486">Parameter</span></span>  | <span data-ttu-id="6babe-487">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-487">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="6babe-488">formName</span><span class="sxs-lookup"><span data-stu-id="6babe-488">formName</span></span>   | <span data-ttu-id="6babe-489">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-489">The name of the form.</span></span>   |
| <span data-ttu-id="6babe-490">methodName</span><span class="sxs-lookup"><span data-stu-id="6babe-490">methodName</span></span> | <span data-ttu-id="6babe-491">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="6babe-491">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-492">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-492">Return Value</span></span>

<span data-ttu-id="6babe-493">フォームのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-493">The name of a method in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-494">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-494">Remarks</span></span>

<span data-ttu-id="6babe-495">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-495">This is a compile-time function.</span></span> <span data-ttu-id="6babe-496">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-496">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-497">例</span><span class="sxs-lookup"><span data-stu-id="6babe-497">Example</span></span>

<span data-ttu-id="6babe-498">次の例では、**showDialog** メソッドの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="6babe-498">The following example prints the name of the **showDialog** method.</span></span>

    str c = formMethodStr(Batch,showDialog);

## <a name="formstr"></a><span data-ttu-id="6babe-499">formStr</span><span class="sxs-lookup"><span data-stu-id="6babe-499">formStr</span></span>
<span data-ttu-id="6babe-500">フォームの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-500">Retrieves the name of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-501">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-501">Syntax</span></span>

    str formStr(str form)

### <a name="parameters"></a><span data-ttu-id="6babe-502">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-502">Parameters</span></span>

| <span data-ttu-id="6babe-503">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-503">Parameter</span></span> | <span data-ttu-id="6babe-504">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-504">Description</span></span>         |
|-----------|---------------------|
| <span data-ttu-id="6babe-505">フォーム</span><span class="sxs-lookup"><span data-stu-id="6babe-505">form</span></span>      | <span data-ttu-id="6babe-506">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-506">The name of a form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-507">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-507">Return Value</span></span>

<span data-ttu-id="6babe-508">フォームの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-508">A string that represents the name of the form.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-509">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-509">Remarks</span></span>

<span data-ttu-id="6babe-510">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-510">This is a compile-time function.</span></span> <span data-ttu-id="6babe-511">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-511">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-512">例</span><span class="sxs-lookup"><span data-stu-id="6babe-512">Example</span></span>

<span data-ttu-id="6babe-513">次の例では、InventDim フォームの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="6babe-513">The following example prints the name of the InventDim form.</span></span>

    static void formStrExample(Args _arg)
    {
        ;

        Global::info(formStr(InventDim));
    }
    /****Infolog Display
    Message (11:04:39 am)
    InventDim
    ****/

## <a name="identifierstr"></a><span data-ttu-id="6babe-514">identifierStr</span><span class="sxs-lookup"><span data-stu-id="6babe-514">identifierStr</span></span>
<span data-ttu-id="6babe-515">指定された識別子を文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="6babe-515">Converts the specified identifier to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-516">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-516">Syntax</span></span>

    str identifierStr(str ident)

### <a name="parameters"></a><span data-ttu-id="6babe-517">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-517">Parameters</span></span>

| <span data-ttu-id="6babe-518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-518">Parameter</span></span> | <span data-ttu-id="6babe-519">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-519">Description</span></span>                |
|-----------|----------------------------|
| <span data-ttu-id="6babe-520">ident</span><span class="sxs-lookup"><span data-stu-id="6babe-520">ident</span></span>     | <span data-ttu-id="6babe-521">変換する ID。</span><span class="sxs-lookup"><span data-stu-id="6babe-521">The identifier to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-522">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-522">Return Value</span></span>

<span data-ttu-id="6babe-523">指定した ID を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-523">A string that represents the specified identifier.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-524">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-524">Remarks</span></span>

<span data-ttu-id="6babe-525">**identifierStr** 関数使用する場合、ベスト プラクティス警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6babe-525">You will receive a best practice warning if you use the **identifierStr** function.</span></span> <span data-ttu-id="6babe-526">これは、**identifierStr** に対して存在チェックが実行されたために発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-526">This occurs because existence checking is performed for **identifierStr**.</span></span> <span data-ttu-id="6babe-527">使用可能な場合は、より具体的なコンパイル時の関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-527">Try to use a more specific compile-time function if one is available.</span></span> <span data-ttu-id="6babe-528">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-528">This is a compile-time function.</span></span> <span data-ttu-id="6babe-529">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-529">For more information, [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-530">例</span><span class="sxs-lookup"><span data-stu-id="6babe-530">Example</span></span>

<span data-ttu-id="6babe-531">次のコード例では、*myvar* 変数名を *thevar* 変数に割り当てています。</span><span class="sxs-lookup"><span data-stu-id="6babe-531">The following code example assigns the *myvar* variable name to the *thevar* variable.</span></span>

    static void indentifierStrExample(Args _args)
    {
        str myvar;
        str thevar
        ;

        thevar = "[" + identifierStr(myvar) + "]";
        Global::info(strfmt(thevar));
    }
    /****Infolog Display
    Message (09:19:49 am)
    [myvar]
    ****/

## <a name="indexnum"></a><span data-ttu-id="6babe-532">indexNum</span><span class="sxs-lookup"><span data-stu-id="6babe-532">indexNum</span></span>
<span data-ttu-id="6babe-533">指定されたインデックスを数字に変換します。</span><span class="sxs-lookup"><span data-stu-id="6babe-533">Converts the specified index to a number.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-534">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-534">Syntax</span></span>

    int indexNum(str tableid, str indexid)

### <a name="parameters"></a><span data-ttu-id="6babe-535">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-535">Parameters</span></span>

| <span data-ttu-id="6babe-536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-536">Parameter</span></span> | <span data-ttu-id="6babe-537">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-537">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="6babe-538">tableid</span><span class="sxs-lookup"><span data-stu-id="6babe-538">tableid</span></span>   | <span data-ttu-id="6babe-539">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="6babe-539">The table that contains the index.</span></span> |
| <span data-ttu-id="6babe-540">indexid</span><span class="sxs-lookup"><span data-stu-id="6babe-540">indexid</span></span>   | <span data-ttu-id="6babe-541">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="6babe-541">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="6babe-542">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-542">Return Value</span></span>

<span data-ttu-id="6babe-543">指定されたインデックスを表すインデックス番号。</span><span class="sxs-lookup"><span data-stu-id="6babe-543">The index number that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-544">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-544">Remarks</span></span>

<span data-ttu-id="6babe-545">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-545">This is a compile-time function.</span></span> <span data-ttu-id="6babe-546">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-546">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-547">例</span><span class="sxs-lookup"><span data-stu-id="6babe-547">Example</span></span>

<span data-ttu-id="6babe-548">次の例では、当事者インデックスのインデックス値を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-548">The following example returns the index value of the Party index.</span></span>

    static void indexNumExample(Args _arg)
    {
        ;

        Global::info(strfmt("%1 is the index number of Party.", indexNum(CustTable, Party)));
    }
    /****Infolog Display
    Message (11:28:03 am)
    3 is the index number of Party.
    ****/

## <a name="indexstr"></a><span data-ttu-id="6babe-549">indexStr</span><span class="sxs-lookup"><span data-stu-id="6babe-549">indexStr</span></span>
<span data-ttu-id="6babe-550">指定されたインデックスを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="6babe-550">Converts the specified index to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-551">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-551">Syntax</span></span>

    str indexStr(str tableid, str indexid)

### <a name="parameters"></a><span data-ttu-id="6babe-552">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-552">Parameters</span></span>

| <span data-ttu-id="6babe-553">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-553">Parameter</span></span> | <span data-ttu-id="6babe-554">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-554">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="6babe-555">tableid</span><span class="sxs-lookup"><span data-stu-id="6babe-555">tableid</span></span>   | <span data-ttu-id="6babe-556">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="6babe-556">The table that contains the index.</span></span> |
| <span data-ttu-id="6babe-557">indexid</span><span class="sxs-lookup"><span data-stu-id="6babe-557">indexid</span></span>   | <span data-ttu-id="6babe-558">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="6babe-558">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="6babe-559">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-559">Return Value</span></span>

<span data-ttu-id="6babe-560">指定インデックスを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-560">A string that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-561">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-561">Remarks</span></span>

<span data-ttu-id="6babe-562">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-562">This is a compile-time function.</span></span> <span data-ttu-id="6babe-563">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-563">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-564">例</span><span class="sxs-lookup"><span data-stu-id="6babe-564">Example</span></span>

<span data-ttu-id="6babe-565">次の例では、**CashDisc** インデックス値を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6babe-565">The following example assigns the **CashDisc** index value to the *myText* variable.</span></span>

    static void fieldStrExample(Args _arg)
    {
        str myText;
        ;

        myText = fieldStr(CustTable, CashDisc);
        Global::info(strfmt("%1 is the specified index.", myText));
    }
    /****Infolog Display
    Message (09:11:52 am)
    CashDisc is the specified index.
    ****/

## <a name="licensecodenum"></a><span data-ttu-id="6babe-566">licenseCodeNum</span><span class="sxs-lookup"><span data-stu-id="6babe-566">licenseCodeNum</span></span>
<span data-ttu-id="6babe-567">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-567">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-568">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-568">Syntax</span></span>

    int licenseCodeNum(str codename)

### <a name="parameters"></a><span data-ttu-id="6babe-569">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-569">Parameters</span></span>

| <span data-ttu-id="6babe-570">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-570">Parameter</span></span> | <span data-ttu-id="6babe-571">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-571">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="6babe-572">codename</span><span class="sxs-lookup"><span data-stu-id="6babe-572">codename</span></span>  | <span data-ttu-id="6babe-573">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-573">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-574">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-574">Return Value</span></span>

<span data-ttu-id="6babe-575">指定されたライセンス コードの数。</span><span class="sxs-lookup"><span data-stu-id="6babe-575">The number of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-576">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-576">Remarks</span></span>

<span data-ttu-id="6babe-577">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-577">This is a compile-time function.</span></span> <span data-ttu-id="6babe-578">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-578">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-579">例</span><span class="sxs-lookup"><span data-stu-id="6babe-579">Example</span></span>

    static void licenseCodeNumExample(Args args)
    {
        int i;
        ;

        i = licenseCodeNum(SysMorphX);
        Global::info(strfmt("%1 is the license code number for SysMorphX.", i));
    }
    /****Infolog Display
    Message (01:52:35 pm)
    24 is the license code number for SysMorphX.
    ****/

## <a name="licensecodestr"></a><span data-ttu-id="6babe-580">licenseCodeStr</span><span class="sxs-lookup"><span data-stu-id="6babe-580">licenseCodeStr</span></span>
<span data-ttu-id="6babe-581">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-581">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-582">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-582">Syntax</span></span>

    str licenseCodeStr(str codename)

### <a name="parameters"></a><span data-ttu-id="6babe-583">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-583">Parameters</span></span>

| <span data-ttu-id="6babe-584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-584">Parameter</span></span> | <span data-ttu-id="6babe-585">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-585">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="6babe-586">codename</span><span class="sxs-lookup"><span data-stu-id="6babe-586">codename</span></span>  | <span data-ttu-id="6babe-587">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-587">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-588">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-588">Return Value</span></span>

<span data-ttu-id="6babe-589">指定されたライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-589">The name of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-590">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-590">Remarks</span></span>

<span data-ttu-id="6babe-591">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-591">This is a compile-time function.</span></span> <span data-ttu-id="6babe-592">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-592">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-593">例</span><span class="sxs-lookup"><span data-stu-id="6babe-593">Example</span></span>

    static void licenseCodeStrExample(Args _arg)
    {
        str s;
        ;

        s = licenseCodeStr(SysMorphX);
        Global::info(strfmt("%1 is the license code string for SysMorphX.", s));
    }
    /****Infolog Display
    Message (02:33:56 pm)
    SysMorphX is the license code string for SysMorphX.
    ****/

## <a name="literalstr"></a><span data-ttu-id="6babe-594">literalStr</span><span class="sxs-lookup"><span data-stu-id="6babe-594">literalStr</span></span>
<span data-ttu-id="6babe-595">指定した文字列がリテラル文字列であることを検証します。そうでない場合は、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-595">Validates that the specified string can be a literal string; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-596">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-596">Syntax</span></span>

    str literalStr(int str)

### <a name="parameters"></a><span data-ttu-id="6babe-597">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-597">Parameters</span></span>

| <span data-ttu-id="6babe-598">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-598">Parameter</span></span> | <span data-ttu-id="6babe-599">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-599">Description</span></span>             |
|-----------|-------------------------|
| <span data-ttu-id="6babe-600">codename</span><span class="sxs-lookup"><span data-stu-id="6babe-600">codename</span></span>  | <span data-ttu-id="6babe-601">検証する文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-601">The string to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-602">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-602">Return Value</span></span>

<span data-ttu-id="6babe-603">有効な場合は、リテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-603">The literal string if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-604">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-604">Remarks</span></span>

<span data-ttu-id="6babe-605">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-605">This is a compile-time function.</span></span> <span data-ttu-id="6babe-606">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-606">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-607">例</span><span class="sxs-lookup"><span data-stu-id="6babe-607">Example</span></span>

    {
        str s;
        ;

        s = literalStr("This is a literal str");
        print s;
        pause;
    }

## <a name="maxdate"></a><span data-ttu-id="6babe-608">maxDate</span><span class="sxs-lookup"><span data-stu-id="6babe-608">maxDate</span></span>
<span data-ttu-id="6babe-609">日付型の変数に使用できる最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-609">Retrieves the maximum value allowed for a variable of type date.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-610">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-610">Syntax</span></span>

    date maxDate()

### <a name="return-value"></a><span data-ttu-id="6babe-611">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-611">Return Value</span></span>

<span data-ttu-id="6babe-612">**日付** の変数に使用できる最大値は、**2154-12-31**です。</span><span class="sxs-lookup"><span data-stu-id="6babe-612">The maximum value allowed for a variable of type **date**, which is **2154-12-31**.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-613">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-613">Remarks</span></span>

<span data-ttu-id="6babe-614">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-614">This is a compile-time function.</span></span> <span data-ttu-id="6babe-615">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-615">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-616">例</span><span class="sxs-lookup"><span data-stu-id="6babe-616">Example</span></span>

    static void maxDateExample(Args _arg)
    {
        date maximumDate;
        ;
        maximumDate = maxDate();
        print maximumDate;
        pause;
    }

## <a name="maxint"></a><span data-ttu-id="6babe-617">maxInt</span><span class="sxs-lookup"><span data-stu-id="6babe-617">maxInt</span></span>
<span data-ttu-id="6babe-618">**int** 型に格納可能な最大符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-618">Retrieves the maximum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-619">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-619">Syntax</span></span>

    int maxInt()

### <a name="return-value"></a><span data-ttu-id="6babe-620">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-620">Return Value</span></span>

<span data-ttu-id="6babe-621">整数の許容値の最大値。</span><span class="sxs-lookup"><span data-stu-id="6babe-621">The maximum value allowed value of an integer.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-622">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-622">Remarks</span></span>

<span data-ttu-id="6babe-623">その他の整数値は、戻り値以下になります。</span><span class="sxs-lookup"><span data-stu-id="6babe-623">Any other integer will be less than or equal to the returned value.</span></span> <span data-ttu-id="6babe-624">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-624">This is a compile-time function.</span></span> <span data-ttu-id="6babe-625">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-625">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-626">例</span><span class="sxs-lookup"><span data-stu-id="6babe-626">Example</span></span>

    static void maxIntExample(Args _arg)
    {
        int i;
        ;
        print "The maximum value for type int is " + int2Str(maxInt());
        pause;
    }

## <a name="measurementstr"></a><span data-ttu-id="6babe-627">measurementStr</span><span class="sxs-lookup"><span data-stu-id="6babe-627">measurementStr</span></span>
<span data-ttu-id="6babe-628">測定の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-628">Returns the name of a measurement.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-629">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-629">Syntax</span></span>

    str measurementStr(str measurement)

### <a name="parameters"></a><span data-ttu-id="6babe-630">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-630">Parameters</span></span>

| <span data-ttu-id="6babe-631">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-631">Parameter</span></span>   | <span data-ttu-id="6babe-632">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-632">Description</span></span>                  |
|-------------|------------------------------|
| <span data-ttu-id="6babe-633">測定値</span><span class="sxs-lookup"><span data-stu-id="6babe-633">measurement</span></span> | <span data-ttu-id="6babe-634">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-634">The name of the measurement.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-635">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-635">Return Value</span></span>

<span data-ttu-id="6babe-636">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-636">The name of the measurement.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-637">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-637">Remarks</span></span>

<span data-ttu-id="6babe-638">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-638">This is a compile-time function.</span></span> <span data-ttu-id="6babe-639">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-639">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-640">例</span><span class="sxs-lookup"><span data-stu-id="6babe-640">Example</span></span>

    No example.

## <a name="measurestr"></a><span data-ttu-id="6babe-641">measureStr</span><span class="sxs-lookup"><span data-stu-id="6babe-641">measureStr</span></span>
<span data-ttu-id="6babe-642">メジャーの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-642">Returns the name of a measure.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-643">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-643">Syntax</span></span>

    str measureStr(str measure)

### <a name="parameters"></a><span data-ttu-id="6babe-644">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-644">Parameters</span></span>

| <span data-ttu-id="6babe-645">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-645">Parameter</span></span> | <span data-ttu-id="6babe-646">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-646">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="6babe-647">測定</span><span class="sxs-lookup"><span data-stu-id="6babe-647">measure</span></span>   | <span data-ttu-id="6babe-648">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-648">The name of the measure.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-649">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-649">Return Value</span></span>

<span data-ttu-id="6babe-650">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-650">The name of the measure.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-651">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-651">Remarks</span></span>

<span data-ttu-id="6babe-652">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-652">This is a compile-time function.</span></span> <span data-ttu-id="6babe-653">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-653">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-654">例</span><span class="sxs-lookup"><span data-stu-id="6babe-654">Example</span></span>

    No example.

## <a name="menuitemactionstr"></a><span data-ttu-id="6babe-655">menuItemActionStr</span><span class="sxs-lookup"><span data-stu-id="6babe-655">menuItemActionStr</span></span>
<span data-ttu-id="6babe-656">指定したメニュー項目のアクションがアプリケーション オブジェクト ツリー (Application Explorer) に存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-656">Validates that the specified menu item action exists in the Application Object Tree (Application Explorer); if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-657">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-657">Syntax</span></span>

    str menuItemActionStr(class menuitem)

### <a name="parameters"></a><span data-ttu-id="6babe-658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-658">Parameters</span></span>

| <span data-ttu-id="6babe-659">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-659">Parameter</span></span> | <span data-ttu-id="6babe-660">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-660">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="6babe-661">codename</span><span class="sxs-lookup"><span data-stu-id="6babe-661">codename</span></span>  | <span data-ttu-id="6babe-662">検証するメニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-662">The name of the menu item action to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-663">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-663">Return Value</span></span>

<span data-ttu-id="6babe-664">有効な場合の、メニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-664">The name of the menu item action, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-665">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-665">Remarks</span></span>

<span data-ttu-id="6babe-666">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-666">This is a compile-time function.</span></span> <span data-ttu-id="6babe-667">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-667">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-668">例</span><span class="sxs-lookup"><span data-stu-id="6babe-668">Example</span></span>

    {
        str s1, s2, s3, s4;
        ;

        s1 = menuItemActionStr(AssetCopy);
        s2 = menuItemDisplayStr(Address);
        s3 = menuItemOutputStr(AssetBarcode);
        s4 = menuStr(Administration);

        print "menuItemActionStr for AssetCopy is " + s1;
        print "menuItemDisplayStr for Address is " + s2;
        print "menuItemOutputStr for AssetBarcode is " + s3;
        print "menuStr for Administration is " + s4;

        pause;
    }

## <a name="menuitemdisplaystr"></a><span data-ttu-id="6babe-669">menuItemDisplayStr</span><span class="sxs-lookup"><span data-stu-id="6babe-669">menuItemDisplayStr</span></span>
<span data-ttu-id="6babe-670">指定したメニュー項目の表示がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-670">Validates that the specified menu item display exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-671">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-671">Syntax</span></span>

    str menuitemdisplaystr(class menuItem)

### <a name="parameters"></a><span data-ttu-id="6babe-672">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-672">Parameters</span></span>

| <span data-ttu-id="6babe-673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-673">Parameter</span></span> | <span data-ttu-id="6babe-674">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-674">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="6babe-675">codename</span><span class="sxs-lookup"><span data-stu-id="6babe-675">codename</span></span>  | <span data-ttu-id="6babe-676">検証するメニュー項目nの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-676">The name of the menu item display to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-677">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-677">Return Value</span></span>

<span data-ttu-id="6babe-678">有効な場合の、指定されたメニューの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-678">The name of the specified menu item display, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-679">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-679">Remarks</span></span>

<span data-ttu-id="6babe-680">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-680">This is a compile-time function.</span></span> <span data-ttu-id="6babe-681">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-681">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-682">例</span><span class="sxs-lookup"><span data-stu-id="6babe-682">Example</span></span>

    {
        str s1, s2, s3, s4;
        ;

        s1 = menuItemActionStr(AssetCopy);
        s2 = menuItemDisplayStr(Address);
        s3 = menuItemOutputStr(AssetBarcode);
        s4 = menuStr(Administration);

        print "menuItemActionStr for AssetCopy is " + s1;
        print "menuItemDisplayStr for Address is " + s2;
        print "menuItemOutputStr for AssetBarcode is " + s3;
        print "menuStr for Administration is " + s4;

        pause;
    }

## <a name="menuitemoutputstr"></a><span data-ttu-id="6babe-683">menuItemOutputStr</span><span class="sxs-lookup"><span data-stu-id="6babe-683">menuItemOutputStr</span></span>
<span data-ttu-id="6babe-684">指定したメニュー項目の出力がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-684">Validates that the specified menu item output exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-685">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-685">Syntax</span></span>

    str menuItemOutputStr(class menuitem)

### <a name="parameters"></a><span data-ttu-id="6babe-686">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-686">Parameters</span></span>

| <span data-ttu-id="6babe-687">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-687">Parameter</span></span> | <span data-ttu-id="6babe-688">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-688">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="6babe-689">codename</span><span class="sxs-lookup"><span data-stu-id="6babe-689">codename</span></span>  | <span data-ttu-id="6babe-690">検証するメニュー項目出力の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-690">The name of the menu item output to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-691">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-691">Return Value</span></span>

<span data-ttu-id="6babe-692">有効な場合、指定されたメニュー項目が出力されます。</span><span class="sxs-lookup"><span data-stu-id="6babe-692">The specified menu item output if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-693">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-693">Remarks</span></span>

<span data-ttu-id="6babe-694">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-694">This is a compile-time function.</span></span> <span data-ttu-id="6babe-695">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-695">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-696">例</span><span class="sxs-lookup"><span data-stu-id="6babe-696">Example</span></span>

    {
        str s1, s2, s3, s4;
        ;

        s1 = menuItemActionStr(AssetCopy);
        s2 = menuItemDisplayStr(Address);
        s3 = menuItemOutputStr(AssetBarcode);
        s4 = menuStr(Administration);

        print "menuItemActionStr for AssetCopy is " + s1;
        print "menuItemDisplayStr for Address is " + s2;
        print "menuItemOutputStr for AssetBarcode is " + s3;
        print "menuStr for Administration is " + s4;

        pause;
    }

## <a name="menustr"></a><span data-ttu-id="6babe-697">menuStr</span><span class="sxs-lookup"><span data-stu-id="6babe-697">menuStr</span></span>
<span data-ttu-id="6babe-698">指定したメニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-698">Validates that the specified menu exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-699">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-699">Syntax</span></span>

    str menuStr(class menu)

### <a name="parameters"></a><span data-ttu-id="6babe-700">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-700">Parameters</span></span>

| <span data-ttu-id="6babe-701">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-701">Parameter</span></span> | <span data-ttu-id="6babe-702">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-702">Description</span></span>                       |
|-----------|-----------------------------------|
| <span data-ttu-id="6babe-703">メニュー</span><span class="sxs-lookup"><span data-stu-id="6babe-703">menu</span></span>      | <span data-ttu-id="6babe-704">検証するメニューの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-704">The name of the menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-705">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-705">Return Value</span></span>

<span data-ttu-id="6babe-706">有効な場合の指定されたメニュー項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-706">The name of the specified menu item if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-707">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-707">Remarks</span></span>

<span data-ttu-id="6babe-708">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-708">This is a compile-time function.</span></span> <span data-ttu-id="6babe-709">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-709">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-710">例</span><span class="sxs-lookup"><span data-stu-id="6babe-710">Example</span></span>

    {
        str s1, s2, s3, s4;
        ;

        s1 = menuItemActionStr(AssetCopy);
        s2 = menuItemDisplayStr(Address);
        s3 = menuItemOutputStr(AssetBarcode);
        s4 = menuStr(Administration);

        print "menuItemActionStr for AssetCopy is " + s1;
        print "menuItemDisplayStr for Address is " + s2;
        print "menuItemOutputStr for AssetBarcode is " + s3;
        print "menuStr for Administration is " + s4;

        pause;
    }

## <a name="methodstr"></a><span data-ttu-id="6babe-711">methodStr</span><span class="sxs-lookup"><span data-stu-id="6babe-711">methodStr</span></span>
<span data-ttu-id="6babe-712">指定したメソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-712">Validates that the specified method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-713">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-713">Syntax</span></span>

    str methodStr(class class, int method)

### <a name="parameters"></a><span data-ttu-id="6babe-714">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-714">Parameters</span></span>

| <span data-ttu-id="6babe-715">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-715">Parameter</span></span> | <span data-ttu-id="6babe-716">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-716">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="6babe-717">クラス</span><span class="sxs-lookup"><span data-stu-id="6babe-717">class</span></span>     | <span data-ttu-id="6babe-718">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-718">The name of the class.</span></span>              |
| <span data-ttu-id="6babe-719">メソッド</span><span class="sxs-lookup"><span data-stu-id="6babe-719">method</span></span>    | <span data-ttu-id="6babe-720">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-720">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-721">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-721">Return Value</span></span>

<span data-ttu-id="6babe-722">有効な場合の、指定されたメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-722">The name of the specified method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-723">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-723">Remarks</span></span>

<span data-ttu-id="6babe-724">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-724">This is a compile-time function.</span></span> <span data-ttu-id="6babe-725">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-725">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-726">例</span><span class="sxs-lookup"><span data-stu-id="6babe-726">Example</span></span>

    {
        #define.timeout(50)
        str s;
        SysHelpInitTimeOut SysHelpInitTimeOut;
        ;

        s = methodStr(SysHelpInitTimeOut, timeout);
        print s;
        pause;
    }

## <a name="minint"></a><span data-ttu-id="6babe-727">minInt</span><span class="sxs-lookup"><span data-stu-id="6babe-727">minInt</span></span>
<span data-ttu-id="6babe-728">**int** 型に格納可能な最小符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-728">Retrieves the minimum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-729">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-729">Syntax</span></span>

    int minInt()

### <a name="return-value"></a><span data-ttu-id="6babe-730">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-730">Return Value</span></span>

<span data-ttu-id="6babe-731">**int** 型の最小値です。</span><span class="sxs-lookup"><span data-stu-id="6babe-731">The minimum value of an **int** type.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-732">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-732">Remarks</span></span>

<span data-ttu-id="6babe-733">その他の整数値は、戻り値以上になります。</span><span class="sxs-lookup"><span data-stu-id="6babe-733">Any other integer value will be greater than or equal to the returned value.</span></span> <span data-ttu-id="6babe-734">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-734">This is a compile-time function.</span></span> <span data-ttu-id="6babe-735">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-735">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-736">例</span><span class="sxs-lookup"><span data-stu-id="6babe-736">Example</span></span>

    static void minIntExample(Args _arg)
    {
        int i;
        ;
        i = minInt();
        print "minInt() is " + int2Str(i);    
        pause;
    }

## <a name="privilegestr"></a><span data-ttu-id="6babe-737">privilegeStr</span><span class="sxs-lookup"><span data-stu-id="6babe-737">privilegeStr</span></span>
<span data-ttu-id="6babe-738">権限の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-738">Returns the name of the privilege.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-739">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-739">Syntax</span></span>

    str privilegeStr(str privilege)

### <a name="parameters"></a><span data-ttu-id="6babe-740">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-740">Parameters</span></span>

| <span data-ttu-id="6babe-741">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-741">Parameter</span></span> | <span data-ttu-id="6babe-742">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-742">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="6babe-743">権限</span><span class="sxs-lookup"><span data-stu-id="6babe-743">privilege</span></span> | <span data-ttu-id="6babe-744">名前を返す対象の特権。</span><span class="sxs-lookup"><span data-stu-id="6babe-744">The privilege for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-745">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-745">Return Value</span></span>

<span data-ttu-id="6babe-746">権限の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-746">The name of the privilege.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-747">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-747">Remarks</span></span>

<span data-ttu-id="6babe-748">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-748">This is a compile-time function.</span></span> <span data-ttu-id="6babe-749">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-749">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-750">例</span><span class="sxs-lookup"><span data-stu-id="6babe-750">Example</span></span>

    No example.

## <a name="querydatasourcestr"></a><span data-ttu-id="6babe-751">queryDatasourceStr</span><span class="sxs-lookup"><span data-stu-id="6babe-751">queryDatasourceStr</span></span>
<span data-ttu-id="6babe-752">X++ コンパイラは、データ ソースがクエリに存在するかどうかをチェックし、関数呼び出しを有効なデータ ソース名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6babe-752">Causes the X++ compiler to check whether the data source exists on the query, and to replace the function call with a string of the valid data source name.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-753">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-753">Syntax</span></span>

    str queryDataSourceStr(queryName, dataSourceName)

### <a name="parameters"></a><span data-ttu-id="6babe-754">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-754">Parameters</span></span>

| <span data-ttu-id="6babe-755">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-755">Parameter</span></span>      | <span data-ttu-id="6babe-756">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-756">Description</span></span>                                                               |
|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="6babe-757">queryName</span><span class="sxs-lookup"><span data-stu-id="6babe-757">queryName</span></span>      | <span data-ttu-id="6babe-758">引用符ではなく、クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-758">The name of the query, not in quotation marks.</span></span>                            |
| <span data-ttu-id="6babe-759">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="6babe-759">dataSourceName</span></span> | <span data-ttu-id="6babe-760">クエリ上のデータ ソースの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="6babe-760">The name of the data source that is on the query, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-761">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-761">Return Value</span></span>

<span data-ttu-id="6babe-762">アプリケーション エクスプローラーで表示されるデータ ソースの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-762">A string that contains the name of the data source as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-763">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-763">Remarks</span></span>

<span data-ttu-id="6babe-764">データ ソースがクエリに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6babe-764">A compile error is issued if the compiler determines that the data source does not exist on the query.</span></span> <span data-ttu-id="6babe-765">X++ コードが引用符が含まれる文字列を使用してデータ ソースの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="6babe-765">If your X++ code uses a string that contains quotation marks to supply the data source name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="6babe-766">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="6babe-766">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="6babe-767">コンパイラにより実行される **queryDataSourceStr** などの X++ 関数は、コンパイル時関数とみなされます。</span><span class="sxs-lookup"><span data-stu-id="6babe-767">X++ functions such as **queryDataSourceStr** that are executed by the compiler are referred to as compile-time functions or compile-time functions.</span></span> <span data-ttu-id="6babe-768">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="6babe-768">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="6babe-769">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="6babe-769">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="6babe-770">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-770">This is a compile-time function.</span></span> <span data-ttu-id="6babe-771">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-771">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-772">例</span><span class="sxs-lookup"><span data-stu-id="6babe-772">Example</span></span>

    No example.

## <a name="querymethodstr"></a><span data-ttu-id="6babe-773">queryMethodStr</span><span class="sxs-lookup"><span data-stu-id="6babe-773">queryMethodStr</span></span>
<span data-ttu-id="6babe-774">クエリのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-774">Returns the name of a method of a query.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-775">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-775">Syntax</span></span>

    str queryMethodStr(str queryName, str methodName)

### <a name="parameters"></a><span data-ttu-id="6babe-776">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-776">Parameters</span></span>

| <span data-ttu-id="6babe-777">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-777">Parameter</span></span>  | <span data-ttu-id="6babe-778">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-778">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="6babe-779">queryName</span><span class="sxs-lookup"><span data-stu-id="6babe-779">queryName</span></span>  | <span data-ttu-id="6babe-780">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-780">The name of the query.</span></span>  |
| <span data-ttu-id="6babe-781">methodName</span><span class="sxs-lookup"><span data-stu-id="6babe-781">methodName</span></span> | <span data-ttu-id="6babe-782">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="6babe-782">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-783">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-783">Return Value</span></span>

<span data-ttu-id="6babe-784">クエリのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-784">The name of a method in a query.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-785">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-785">Remarks</span></span>

<span data-ttu-id="6babe-786">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-786">This is a compile-time function.</span></span> <span data-ttu-id="6babe-787">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-787">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-788">例</span><span class="sxs-lookup"><span data-stu-id="6babe-788">Example</span></span>

    No example.

## <a name="querystr"></a><span data-ttu-id="6babe-789">queryStr</span><span class="sxs-lookup"><span data-stu-id="6babe-789">queryStr</span></span>
<span data-ttu-id="6babe-790">既存のクエリを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-790">Retrieves a string that represents an existing query.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-791">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-791">Syntax</span></span>

    str queryStr(str query)

### <a name="parameters"></a><span data-ttu-id="6babe-792">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-792">Parameters</span></span>

| <span data-ttu-id="6babe-793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-793">Parameter</span></span> | <span data-ttu-id="6babe-794">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-794">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="6babe-795">クエリ</span><span class="sxs-lookup"><span data-stu-id="6babe-795">query</span></span>     | <span data-ttu-id="6babe-796">取得するクエリ。</span><span class="sxs-lookup"><span data-stu-id="6babe-796">The query to retrieve.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-797">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-797">Return Value</span></span>

<span data-ttu-id="6babe-798">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-798">The name of the query.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-799">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-799">Remarks</span></span>

<span data-ttu-id="6babe-800">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-800">This is a compile-time function.</span></span> <span data-ttu-id="6babe-801">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-801">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-802">例</span><span class="sxs-lookup"><span data-stu-id="6babe-802">Example</span></span>

    static void queryStrExample(Args _arg)
    {
        str myText;
        ;

        myText = queryStr(AssetTable);
        Global::info(strfmt("%1 is the name of the query.",myText));
    }
    /****Infolog Display
    Message (09:45:16 am)
    AssetTable is the name of the query.
    ****/

## <a name="reportstr"></a><span data-ttu-id="6babe-803">reportStr</span><span class="sxs-lookup"><span data-stu-id="6babe-803">reportStr</span></span>
<span data-ttu-id="6babe-804">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-804">Retrieves a string that represents the name of the specified report.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-805">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-805">Syntax</span></span>

    str reportStr(str report)

### <a name="parameters"></a><span data-ttu-id="6babe-806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-806">Parameters</span></span>

| <span data-ttu-id="6babe-807">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-807">Parameter</span></span> | <span data-ttu-id="6babe-808">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-808">Description</span></span>                              |
|-----------|------------------------------------------|
| <span data-ttu-id="6babe-809">レポート</span><span class="sxs-lookup"><span data-stu-id="6babe-809">report</span></span>    | <span data-ttu-id="6babe-810">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="6babe-810">The report for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-811">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-811">Return Value</span></span>

<span data-ttu-id="6babe-812">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-812">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-813">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-813">Remarks</span></span>

<span data-ttu-id="6babe-814">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-814">This is a compile-time function.</span></span> <span data-ttu-id="6babe-815">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-815">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-816">例</span><span class="sxs-lookup"><span data-stu-id="6babe-816">Example</span></span>

<span data-ttu-id="6babe-817">次の例では、**AssetAddition** レポートの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6babe-817">The following example assigns the name of the **AssetAddition** report to the *MyTxt* variable.</span></span>

    static void reportStrExample(Args _args)
    {
        str MyTxt;
        ;

        MyTxt = reportStr(AssetAddition);
        Global::info(strfmt("%1 is the name of the report.", MyTxt));
    }
    /****Infolog Display.
    Message (10:46:36 am)
    AssetAddition is the name of the report.
    ****/

## <a name="resourcestr"></a><span data-ttu-id="6babe-818">resourceStr</span><span class="sxs-lookup"><span data-stu-id="6babe-818">resourceStr</span></span>
<span data-ttu-id="6babe-819">指定したリソースがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-819">Validates that the specified resource exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-820">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-820">Syntax</span></span>

    str resourceStr(str resourcename)

### <a name="parameters"></a><span data-ttu-id="6babe-821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-821">Parameters</span></span>

| <span data-ttu-id="6babe-822">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-822">Parameter</span></span>    | <span data-ttu-id="6babe-823">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-823">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="6babe-824">resourcename</span><span class="sxs-lookup"><span data-stu-id="6babe-824">resourcename</span></span> | <span data-ttu-id="6babe-825">検証するリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-825">The name of the resource to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-826">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-826">Return Value</span></span>

<span data-ttu-id="6babe-827">有効な場合の、指定されたリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-827">The name of the specified resource, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-828">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-828">Remarks</span></span>

<span data-ttu-id="6babe-829">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-829">This is a compile-time function.</span></span> <span data-ttu-id="6babe-830">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-830">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-831">例</span><span class="sxs-lookup"><span data-stu-id="6babe-831">Example</span></span>

    {
        print "Str for resource StyleSheet_Help_Axapta is " 
            + resourceStr(StyleSheet_Help_Axapta);
        pause;
    }

## <a name="rolestr"></a><span data-ttu-id="6babe-832">roleStr</span><span class="sxs-lookup"><span data-stu-id="6babe-832">roleStr</span></span>
<span data-ttu-id="6babe-833">指定したセキュリティ ロールの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-833">Retrieves a string that represents the name of the specified security role.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-834">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-834">Syntax</span></span>

    str roleStr(str securityRole)

### <a name="parameters"></a><span data-ttu-id="6babe-835">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-835">Parameters</span></span>

| <span data-ttu-id="6babe-836">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-836">Parameter</span></span>    | <span data-ttu-id="6babe-837">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-837">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="6babe-838">securityRole</span><span class="sxs-lookup"><span data-stu-id="6babe-838">securityRole</span></span> | <span data-ttu-id="6babe-839">セキュリティ ロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="6babe-839">The name of the security role.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-840">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-840">Return Value</span></span>

<span data-ttu-id="6babe-841">文字列のセキュリティ ロールの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-841">The name of the security role in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-842">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-842">Remarks</span></span>

<span data-ttu-id="6babe-843">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-843">This is a compile-time function.</span></span> <span data-ttu-id="6babe-844">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-844">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-845">例</span><span class="sxs-lookup"><span data-stu-id="6babe-845">Example</span></span>

    No example.

## <a name="ssrsreportstr"></a><span data-ttu-id="6babe-846">ssrsReportStr</span><span class="sxs-lookup"><span data-stu-id="6babe-846">ssrsReportStr</span></span>
<span data-ttu-id="6babe-847">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-847">Retrieves a string that represents the name of the specified report.</span></span> <span data-ttu-id="6babe-848">レポート コントローラー クラスで実行されるレポートを指定する場合は、この関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6babe-848">Use this function when you want to specify the report that should be run by a report controller class.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-849">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-849">Syntax</span></span>

    str ssrsReportStr(str report, str design)

### <a name="parameters"></a><span data-ttu-id="6babe-850">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-850">Parameters</span></span>

| <span data-ttu-id="6babe-851">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-851">Parameter</span></span> | <span data-ttu-id="6babe-852">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-852">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| <span data-ttu-id="6babe-853">レポート</span><span class="sxs-lookup"><span data-stu-id="6babe-853">report</span></span>    | <span data-ttu-id="6babe-854">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="6babe-854">The report to return the name for.</span></span>                         |
| <span data-ttu-id="6babe-855">design</span><span class="sxs-lookup"><span data-stu-id="6babe-855">design</span></span>    | <span data-ttu-id="6babe-856">レポートに関連付けられているデザインの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-856">The name of the design that is associated with the report.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-857">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-857">Return Value</span></span>

<span data-ttu-id="6babe-858">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-858">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-859">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-859">Remarks</span></span>

<span data-ttu-id="6babe-860">**ssrsReportStr** 関数は、有効なレポートに属しているかどうかを検証するために、渡された 2 つの値を解析します。</span><span class="sxs-lookup"><span data-stu-id="6babe-860">The **ssrsReportStr** function parses the two values that are passed to it, to validate whether they belong to a valid report.</span></span> <span data-ttu-id="6babe-861">コントローラーが、どのレポート デザインの組み合わせを呼び出す必要があるかを判断できるように、メニュー項目が controller() を指しているときは、レポート名を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6babe-861">The report name must be set when a menu item points to a controller(), so that the controller can determine which report-design combination must be invoked.</span></span> <span data-ttu-id="6babe-862">**ssrsReportStr** 関数を使用すると、レポートおよびデザイン名のコンパイル時の検証で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6babe-862">Use of the **ssrsReportStr** function provides the benefit of compile-time validation for the report and design name.</span></span> <span data-ttu-id="6babe-863">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-863">This is a compile-time function.</span></span> <span data-ttu-id="6babe-864">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-864">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-865">例</span><span class="sxs-lookup"><span data-stu-id="6babe-865">Example</span></span>

    public static void main(Args _args)
    {
        // Initializing the object for a controller class, in this case, the class named AssetListingController.
        SrsReportRunController controller = new AssetListingController();

        // Getting the properties of the called object (in this case AssetListing MenuItem)
        controller.parmArgs(_args);
        // Setting the Report name for the controller.
        controller.parmReportName(ssrsReportStr(AssetListing, Report));

        // Initiate the report execution.
        controller.startOperation();
    }

## <a name="staticdelegatestr"></a><span data-ttu-id="6babe-866">staticDelegateStr</span><span class="sxs-lookup"><span data-stu-id="6babe-866">staticDelegateStr</span></span>
<span data-ttu-id="6babe-867">静的デリゲートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="6babe-867">Returns the name of a static delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-868">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-868">Syntax</span></span>

    str staticDelegateStr(str class, str delegate)

### <a name="parameters"></a><span data-ttu-id="6babe-869">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-869">Parameters</span></span>

| <span data-ttu-id="6babe-870">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-870">Parameter</span></span> | <span data-ttu-id="6babe-871">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-871">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="6babe-872">クラス</span><span class="sxs-lookup"><span data-stu-id="6babe-872">class</span></span>     | <span data-ttu-id="6babe-873">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-873">The name of a class, table, or form.</span></span> |
| <span data-ttu-id="6babe-874">デリゲート</span><span class="sxs-lookup"><span data-stu-id="6babe-874">delegate</span></span>  | <span data-ttu-id="6babe-875">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="6babe-875">The name of the delegate.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="6babe-876">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-876">Return Value</span></span>

<span data-ttu-id="6babe-877">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="6babe-877">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-878">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-878">Remarks</span></span>

<span data-ttu-id="6babe-879">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-879">This is a compile-time function.</span></span> <span data-ttu-id="6babe-880">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-880">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-881">例</span><span class="sxs-lookup"><span data-stu-id="6babe-881">Example</span></span>

    No example.

## <a name="staticmethodstr"></a><span data-ttu-id="6babe-882">staticMethodStr</span><span class="sxs-lookup"><span data-stu-id="6babe-882">staticMethodStr</span></span>
<span data-ttu-id="6babe-883">指定した静的メソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-883">Validates that the specified static method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-884">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-884">Syntax</span></span>

    str staticMethodStr(class class, int method)

### <a name="parameters"></a><span data-ttu-id="6babe-885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-885">Parameters</span></span>

| <span data-ttu-id="6babe-886">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-886">Parameter</span></span> | <span data-ttu-id="6babe-887">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-887">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="6babe-888">クラス</span><span class="sxs-lookup"><span data-stu-id="6babe-888">class</span></span>     | <span data-ttu-id="6babe-889">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-889">The name of the class.</span></span>                     |
| <span data-ttu-id="6babe-890">メソッド</span><span class="sxs-lookup"><span data-stu-id="6babe-890">method</span></span>    | <span data-ttu-id="6babe-891">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-891">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-892">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-892">Return Value</span></span>

<span data-ttu-id="6babe-893">有効な場合の、指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-893">The name of the static method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-894">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-894">Remarks</span></span>

<span data-ttu-id="6babe-895">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-895">This is a compile-time function.</span></span> <span data-ttu-id="6babe-896">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-896">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-897">例</span><span class="sxs-lookup"><span data-stu-id="6babe-897">Example</span></span>

    No example.

## <a name="tablecollectionstr"></a><span data-ttu-id="6babe-898">tableCollectionStr</span><span class="sxs-lookup"><span data-stu-id="6babe-898">tableCollectionStr</span></span>
<span data-ttu-id="6babe-899">指定したテーブル コレクションがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-899">Validates that the specified table collection exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-900">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-900">Syntax</span></span>

    str tableCollectionStr(class tablecollection)

### <a name="parameters"></a><span data-ttu-id="6babe-901">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-901">Parameters</span></span>

| <span data-ttu-id="6babe-902">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-902">Parameter</span></span>       | <span data-ttu-id="6babe-903">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-903">Description</span></span>                                   |
|-----------------|-----------------------------------------------|
| <span data-ttu-id="6babe-904">tablecollection</span><span class="sxs-lookup"><span data-stu-id="6babe-904">tablecollection</span></span> | <span data-ttu-id="6babe-905">検証するテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-905">The name of the table collection to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-906">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-906">Return Value</span></span>

<span data-ttu-id="6babe-907">有効な場合の、指定されたテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-907">The name of the specified table collection, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-908">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-908">Remarks</span></span>

<span data-ttu-id="6babe-909">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-909">This is a compile-time function.</span></span> <span data-ttu-id="6babe-910">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-910">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-911">例</span><span class="sxs-lookup"><span data-stu-id="6babe-911">Example</span></span>

    No example.

## <a name="tablefieldgroupstr"></a><span data-ttu-id="6babe-912">tableFieldGroupStr</span><span class="sxs-lookup"><span data-stu-id="6babe-912">tableFieldGroupStr</span></span>
<span data-ttu-id="6babe-913">文字列としてフィールド グループの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-913">Retrieves the name of a field group as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-914">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-914">Syntax</span></span>

    str tableFieldGroupStr(str tableName, str fieldGroupName)

### <a name="parameters"></a><span data-ttu-id="6babe-915">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-915">Parameters</span></span>

| <span data-ttu-id="6babe-916">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-916">Parameter</span></span>      | <span data-ttu-id="6babe-917">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-917">Description</span></span>                              |
|----------------|------------------------------------------|
| <span data-ttu-id="6babe-918">tableName</span><span class="sxs-lookup"><span data-stu-id="6babe-918">tableName</span></span>      | <span data-ttu-id="6babe-919">フィールド グループを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="6babe-919">The table that contains the field group.</span></span> |
| <span data-ttu-id="6babe-920">fieldGroupName</span><span class="sxs-lookup"><span data-stu-id="6babe-920">fieldGroupName</span></span> | <span data-ttu-id="6babe-921">テーブル内のフィールド グループ。</span><span class="sxs-lookup"><span data-stu-id="6babe-921">The field group in the table.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="6babe-922">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-922">Return Value</span></span>

<span data-ttu-id="6babe-923">文字列としてのフィールド グループの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-923">The name of the field group as a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-924">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-924">Remarks</span></span>

<span data-ttu-id="6babe-925">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-925">This is a compile-time function.</span></span> <span data-ttu-id="6babe-926">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-926">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-927">例</span><span class="sxs-lookup"><span data-stu-id="6babe-927">Example</span></span>

<span data-ttu-id="6babe-928">次の例では、**編集** フィールド グループの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-928">The following example retrieves the name of the **Editing** field group as a string.</span></span>

    static void tableFieldGroupStrExample(Args _arg)
    {
        ;

        Global::info(tableFieldGroupStr(AccountingDistribution, Editing));
    }
    /****Infolog Display
    Message (03:14:54 pm)
    Editing
    ****/

## <a name="tablemethodstr"></a><span data-ttu-id="6babe-929">tableMethodStr</span><span class="sxs-lookup"><span data-stu-id="6babe-929">tableMethodStr</span></span>
<span data-ttu-id="6babe-930">指定したメソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-930">Validates that the specified method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-931">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-931">Syntax</span></span>

    str tableMethodStr(int table, int method)

### <a name="parameters"></a><span data-ttu-id="6babe-932">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-932">Parameters</span></span>

| <span data-ttu-id="6babe-933">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-933">Parameter</span></span> | <span data-ttu-id="6babe-934">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-934">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="6babe-935">テーブル</span><span class="sxs-lookup"><span data-stu-id="6babe-935">table</span></span>     | <span data-ttu-id="6babe-936">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-936">The name of the table.</span></span>              |
| <span data-ttu-id="6babe-937">メソッド</span><span class="sxs-lookup"><span data-stu-id="6babe-937">method</span></span>    | <span data-ttu-id="6babe-938">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-938">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-939">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-939">Return Value</span></span>

<span data-ttu-id="6babe-940">有効な場合の、メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-940">The name of the method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-941">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-941">Remarks</span></span>

<span data-ttu-id="6babe-942">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-942">This is a compile-time function.</span></span> <span data-ttu-id="6babe-943">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-943">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-944">例</span><span class="sxs-lookup"><span data-stu-id="6babe-944">Example</span></span>

    No example.

## <a name="tablenum"></a><span data-ttu-id="6babe-945">tableNum</span><span class="sxs-lookup"><span data-stu-id="6babe-945">tableNum</span></span>
<span data-ttu-id="6babe-946">特定のテーブルのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-946">Retrieves the table ID of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-947">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-947">Syntax</span></span>

    int tableNum(str table)

### <a name="parameters"></a><span data-ttu-id="6babe-948">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-948">Parameters</span></span>

| <span data-ttu-id="6babe-949">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-949">Parameter</span></span> | <span data-ttu-id="6babe-950">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-950">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="6babe-951">テーブル</span><span class="sxs-lookup"><span data-stu-id="6babe-951">table</span></span>     | <span data-ttu-id="6babe-952">テーブル ID を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="6babe-952">The table to retrieve the table ID for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-953">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-953">Return Value</span></span>

<span data-ttu-id="6babe-954">特定のテーブルのテーブル ID</span><span class="sxs-lookup"><span data-stu-id="6babe-954">The table ID of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-955">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-955">Remarks</span></span>

<span data-ttu-id="6babe-956">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-956">This is a compile-time function.</span></span> <span data-ttu-id="6babe-957">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-957">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-958">例</span><span class="sxs-lookup"><span data-stu-id="6babe-958">Example</span></span>

<span data-ttu-id="6babe-959">次の例では、**tableID** 変数を 77 に設定します。これは、**CustTable** テーブルの **ID** です。</span><span class="sxs-lookup"><span data-stu-id="6babe-959">The following example sets the **tableID** variable to 77, which is the **ID** of the **CustTable** table.</span></span>

    static void tableNumExample(Args _args)
    {
        int tableID;
        ;

        tableID = tableNum(CustTable);
        Global::info(strfmt("%1 is the table ID for the CustTable table.", tableID));

    }
    /****Infolog Display
    Message (11:15:54 am)
    77 is the table ID for the CustTable table.
    ****/

## <a name="tablepname"></a><span data-ttu-id="6babe-960">tablePName</span><span class="sxs-lookup"><span data-stu-id="6babe-960">tablePName</span></span>
<span data-ttu-id="6babe-961">指定されたテーブルの出力可能な名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-961">Retrieves a string that contains the printable name of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-962">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-962">Syntax</span></span>

    str tablePName(str table)

### <a name="parameters"></a><span data-ttu-id="6babe-963">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-963">Parameters</span></span>

| <span data-ttu-id="6babe-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-964">Parameter</span></span> | <span data-ttu-id="6babe-965">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-965">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="6babe-966">テーブル</span><span class="sxs-lookup"><span data-stu-id="6babe-966">table</span></span>     | <span data-ttu-id="6babe-967">印刷可能な名前を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="6babe-967">The table to retrieve the printable name for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-968">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-968">Return Value</span></span>

<span data-ttu-id="6babe-969">指定されたテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-969">The name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-970">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-970">Remarks</span></span>

<span data-ttu-id="6babe-971">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-971">This is a compile-time function.</span></span> <span data-ttu-id="6babe-972">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-972">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-973">例</span><span class="sxs-lookup"><span data-stu-id="6babe-973">Example</span></span>

<span data-ttu-id="6babe-974">次の例では、**CustTable** テーブルのラベルを *MyText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6babe-974">The following example assigns the label of the **CustTable** table to the *MyText* variable.</span></span>

    static void tablePNameExample(Args _args)
    {
        str MyText;
        ;

        MyText = tablePname(CustTable);
        Global::info(strfmt("%1 is the label of the CustTable table.", MyText));
    }
    /**** Infolog Display.
    Message (12:13:53 pm)
    Customers is the label of the CustTable table.
    ****/

## <a name="tablestaticmethodstr"></a><span data-ttu-id="6babe-975">tableStaticMethodStr</span><span class="sxs-lookup"><span data-stu-id="6babe-975">tableStaticMethodStr</span></span>
<span data-ttu-id="6babe-976">指定した静的メソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-976">Validates that the specified static method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-977">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-977">Syntax</span></span>

    str tableStaticMethodStr(int table, int method)

### <a name="parameters"></a><span data-ttu-id="6babe-978">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-978">Parameters</span></span>

| <span data-ttu-id="6babe-979">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-979">Parameter</span></span> | <span data-ttu-id="6babe-980">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-980">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="6babe-981">テーブル</span><span class="sxs-lookup"><span data-stu-id="6babe-981">table</span></span>     | <span data-ttu-id="6babe-982">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-982">The name of the table.</span></span>                     |
| <span data-ttu-id="6babe-983">メソッド</span><span class="sxs-lookup"><span data-stu-id="6babe-983">method</span></span>    | <span data-ttu-id="6babe-984">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-984">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-985">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-985">Return Value</span></span>

<span data-ttu-id="6babe-986">指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-986">The name of the specified static method.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-987">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-987">Remarks</span></span>

<span data-ttu-id="6babe-988">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-988">This is a compile-time function.</span></span> <span data-ttu-id="6babe-989">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-989">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-990">例</span><span class="sxs-lookup"><span data-stu-id="6babe-990">Example</span></span>

    No example.

## <a name="tablestr"></a><span data-ttu-id="6babe-991">tableStr</span><span class="sxs-lookup"><span data-stu-id="6babe-991">tableStr</span></span>
<span data-ttu-id="6babe-992">指定したテーブルの名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-992">Retrieves a string that contains the name the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-993">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-993">Syntax</span></span>

    str tableStr(str table)

### <a name="parameters"></a><span data-ttu-id="6babe-994">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-994">Parameters</span></span>

| <span data-ttu-id="6babe-995">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-995">Parameter</span></span> | <span data-ttu-id="6babe-996">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-996">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="6babe-997">テーブル</span><span class="sxs-lookup"><span data-stu-id="6babe-997">table</span></span>     | <span data-ttu-id="6babe-998">文字列を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="6babe-998">The table to retrieve a string for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-999">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-999">Return Value</span></span>

<span data-ttu-id="6babe-1000">指定したテーブルの名前を含む文字列値。</span><span class="sxs-lookup"><span data-stu-id="6babe-1000">A string value that contains the name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1001">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1001">Remarks</span></span>

<span data-ttu-id="6babe-1002">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1002">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1003">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1003">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1004">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1004">Example</span></span>

<span data-ttu-id="6babe-1005">次の例では、**CustTable** テーブルの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6babe-1005">The following example assigns the name of the **CustTable** table to the *MyTxt* variable.</span></span>

    static void tableStrExample(Args _args)
    {
        str MyTxt;
        ;

        MyTxt = tableStr(CustTable);
        Global::info(strfmt("%1 is the str output of the input of CustTable.", MyTxt));
    }
    /**** Infolog Display. 
    Message (01:21:49 pm)
    CustTable is the str output of the input of CustTable.
    ****/

## <a name="tilestr"></a><span data-ttu-id="6babe-1006">tileStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1006">tileStr</span></span>
<span data-ttu-id="6babe-1007">指定したタイルの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1007">Retrieves a string that represents the name of the specified tile.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1008">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1008">Syntax</span></span>

    str tileStr(str tile)

### <a name="parameters"></a><span data-ttu-id="6babe-1009">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1009">Parameters</span></span>

| <span data-ttu-id="6babe-1010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1010">Parameter</span></span> | <span data-ttu-id="6babe-1011">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1011">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="6babe-1012">tile</span><span class="sxs-lookup"><span data-stu-id="6babe-1012">tile</span></span>      | <span data-ttu-id="6babe-1013">タイルの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1013">The name of the tile.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1014">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1014">Return Value</span></span>

<span data-ttu-id="6babe-1015">文字列のタイルの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1015">The name of the tile in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1016">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1016">Remarks</span></span>

<span data-ttu-id="6babe-1017">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1017">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1018">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1018">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1019">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1019">Example</span></span>

    No example.

## <a name="varstr"></a><span data-ttu-id="6babe-1020">varStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1020">varStr</span></span>
<span data-ttu-id="6babe-1021">指定した変数の名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1021">Retrieves a string that contains the name of the specified variable.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1022">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1022">Syntax</span></span>

    str varStr(str var)

### <a name="parameters"></a><span data-ttu-id="6babe-1023">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1023">Parameters</span></span>

| <span data-ttu-id="6babe-1024">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1024">Parameter</span></span> | <span data-ttu-id="6babe-1025">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1025">Description</span></span>               |
|-----------|---------------------------|
| <span data-ttu-id="6babe-1026">var</span><span class="sxs-lookup"><span data-stu-id="6babe-1026">var</span></span>       | <span data-ttu-id="6babe-1027">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1027">The name of the variable.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1028">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1028">Return Value</span></span>

<span data-ttu-id="6babe-1029">指定した変数の名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-1029">A string that contains the name of the specified variable.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1030">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1030">Remarks</span></span>

<span data-ttu-id="6babe-1031">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1031">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1032">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1032">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1033">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1033">Example</span></span>

    static void varStrExample(Args _arg)
    {
        str myString;
        anytype myVariable;
        ;

        myString = varStr(myVariable);
        Global::info(strfmt("%1 is the variable name.", myString));
    }
    /****Infolog Display.
    Message (02:26:56 pm)
    myVariable is the variable name.
    ****/

## <a name="webactionitemstr"></a><span data-ttu-id="6babe-1034">webActionItemStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1034">webActionItemStr</span></span>
<span data-ttu-id="6babe-1035">指定した Web アクション項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1035">Validates that the specified web action item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1036">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1036">Syntax</span></span>

    str webActionItemStr(class webactionitem)

### <a name="parameters"></a><span data-ttu-id="6babe-1037">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1037">Parameters</span></span>

| <span data-ttu-id="6babe-1038">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1038">Parameter</span></span>     | <span data-ttu-id="6babe-1039">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1039">Description</span></span>                                  |
|---------------|----------------------------------------------|
| <span data-ttu-id="6babe-1040">webactionitem</span><span class="sxs-lookup"><span data-stu-id="6babe-1040">webactionitem</span></span> | <span data-ttu-id="6babe-1041">検証する Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1041">The name of the web action item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1042">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1042">Return Value</span></span>

<span data-ttu-id="6babe-1043">有効な場合の、指定された Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1043">The name of the specified web action item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1044">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1044">Remarks</span></span>

<span data-ttu-id="6babe-1045">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1045">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1046">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1046">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1047">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1047">Example</span></span>

    {
        str s;
        ;
        s = webActionItemStr(EPFlushData);
        print "webactionitem str is " + s;
        pause;
    }

## <a name="webdisplaycontentitemstr"></a><span data-ttu-id="6babe-1048">webDisplayContentItemStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1048">webDisplayContentItemStr</span></span>
<span data-ttu-id="6babe-1049">指定したWeb 表示のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1049">Validates that the specified web display content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1050">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1050">Syntax</span></span>

    str webDisplayContentItemStr(class webdisplaycontentitem)

### <a name="parameters"></a><span data-ttu-id="6babe-1051">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1051">Parameters</span></span>

| <span data-ttu-id="6babe-1052">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1052">Parameter</span></span>             | <span data-ttu-id="6babe-1053">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1053">Description</span></span>                                           |
|-----------------------|-------------------------------------------------------|
| <span data-ttu-id="6babe-1054">webdisplaycontentitem</span><span class="sxs-lookup"><span data-stu-id="6babe-1054">webdisplaycontentitem</span></span> | <span data-ttu-id="6babe-1055">検証する Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1055">The name of the web display content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1056">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1056">Return Value</span></span>

<span data-ttu-id="6babe-1057">有効な場合の、指定された Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1057">The name of the specified web display content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1058">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1058">Remarks</span></span>

<span data-ttu-id="6babe-1059">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1059">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1060">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1060">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1061">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1061">Example</span></span>

    {
        str s;
        ;

        s = webDisplayContentItemStr(EPAdmin);
        print "string for webcontent display item EPAdmin is " + s;
        pause;
    }

## <a name="webformstr"></a><span data-ttu-id="6babe-1062">webFormStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1062">webFormStr</span></span>
<span data-ttu-id="6babe-1063">指定した Web フォームがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1063">Validates that the specified web form exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1064">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1064">Syntax</span></span>

    str webFormStr(str name)

### <a name="parameters"></a><span data-ttu-id="6babe-1065">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1065">Parameters</span></span>

| <span data-ttu-id="6babe-1066">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1066">Parameter</span></span> | <span data-ttu-id="6babe-1067">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1067">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="6babe-1068">名前</span><span class="sxs-lookup"><span data-stu-id="6babe-1068">name</span></span>      | <span data-ttu-id="6babe-1069">検証する Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1069">The name of the web form to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1070">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1070">Return Value</span></span>

<span data-ttu-id="6babe-1071">有効な場合の、指定された Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1071">The name of the specified web form, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1072">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1072">Remarks</span></span>

<span data-ttu-id="6babe-1073">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1073">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1074">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1074">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1075">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1075">Example</span></span>

    {
        str s;
        ;
        s = webFormStr(EPAdmin);
        print "String for web form EPAdmin is " + s;
        pause;
    }

## <a name="webletitemstr"></a><span data-ttu-id="6babe-1076">webletItemStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1076">webletItemStr</span></span>
<span data-ttu-id="6babe-1077">指定した Weblet 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1077">Validates that the specified weblet item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1078">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1078">Syntax</span></span>

    str webletItemStr(class webletitem)

### <a name="parameters"></a><span data-ttu-id="6babe-1079">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1079">Parameters</span></span>

| <span data-ttu-id="6babe-1080">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1080">Parameter</span></span>  | <span data-ttu-id="6babe-1081">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1081">Description</span></span>                              |
|------------|------------------------------------------|
| <span data-ttu-id="6babe-1082">webletitem</span><span class="sxs-lookup"><span data-stu-id="6babe-1082">webletitem</span></span> | <span data-ttu-id="6babe-1083">検証する Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1083">The name of the weblet item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1084">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1084">Return Value</span></span>

<span data-ttu-id="6babe-1085">有効な場合の、指定された Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1085">The name of the specified weblet item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1086">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1086">Remarks</span></span>

<span data-ttu-id="6babe-1087">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1087">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1088">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1088">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1089">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1089">Example</span></span>

    {
        str s;
        ;
        s = webletItemStr(WebFormWeblet);
        print "String for WebFormWeblet is " + s;
        pause;
    }

## <a name="webmenustr"></a><span data-ttu-id="6babe-1090">webMenuStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1090">webMenuStr</span></span>
<span data-ttu-id="6babe-1091">指定した Web メニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1091">Validates that the specified web menu exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1092">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1092">Syntax</span></span>

    str webMenuStr(str name)

### <a name="parameters"></a><span data-ttu-id="6babe-1093">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1093">Parameters</span></span>

| <span data-ttu-id="6babe-1094">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1094">Parameter</span></span> | <span data-ttu-id="6babe-1095">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1095">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="6babe-1096">名前</span><span class="sxs-lookup"><span data-stu-id="6babe-1096">name</span></span>      | <span data-ttu-id="6babe-1097">検証する Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1097">The name of the web menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1098">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1098">Return Value</span></span>

<span data-ttu-id="6babe-1099">有効な場合の、指定された Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1099">The name of the specified web menu, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1100">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1100">Remarks</span></span>

<span data-ttu-id="6babe-1101">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1101">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1102">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1102">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1103">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1103">Example</span></span>

    {
        str s;
        ;
        s = webMenuStr(ECPAdmin);
        print "String for web menu ECPAdmin is " + s;
        pause;
    }

## <a name="weboutputcontentitemstr"></a><span data-ttu-id="6babe-1104">webOutputContentItemStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1104">webOutputContentItemStr</span></span>
<span data-ttu-id="6babe-1105">指定したWeb 出力のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1105">Validates that the specified web output content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1106">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1106">Syntax</span></span>

    str webOutputContentItemStr(class weboutputcontentitem)

### <a name="parameters"></a><span data-ttu-id="6babe-1107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1107">Parameters</span></span>

| <span data-ttu-id="6babe-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1108">Parameter</span></span>            | <span data-ttu-id="6babe-1109">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1109">Description</span></span>                                          |
|----------------------|------------------------------------------------------|
| <span data-ttu-id="6babe-1110">weboutputcontentitem</span><span class="sxs-lookup"><span data-stu-id="6babe-1110">weboutputcontentitem</span></span> | <span data-ttu-id="6babe-1111">検証する Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1111">The name of the web output content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1112">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1112">Return Value</span></span>

<span data-ttu-id="6babe-1113">有効な場合の、指定された Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1113">The name of the specified web output content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1114">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1114">Remarks</span></span>

<span data-ttu-id="6babe-1115">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1115">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1116">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1116">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1117">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1117">Example</span></span>

    {
        str s;
        ;
        s = webOutputContentItemStr(EPPriceList);
        print "string for weboutput content item EPPriceList is " + s;
        pause;
    }

## <a name="webpagedefstr"></a><span data-ttu-id="6babe-1118">webpageDefStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1118">webpageDefStr</span></span>
<span data-ttu-id="6babe-1119">指定した Web ページ定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1119">Validates that the specified Web page definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1120">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1120">Syntax</span></span>

    str webpageDefStr(str pagename)

### <a name="parameters"></a><span data-ttu-id="6babe-1121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1121">Parameters</span></span>

| <span data-ttu-id="6babe-1122">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1122">Parameter</span></span> | <span data-ttu-id="6babe-1123">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1123">Description</span></span>                                      |
|-----------|--------------------------------------------------|
| <span data-ttu-id="6babe-1124">pagename</span><span class="sxs-lookup"><span data-stu-id="6babe-1124">pagename</span></span>  | <span data-ttu-id="6babe-1125">検証する Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1125">The name of the Web page definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1126">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1126">Return Value</span></span>

<span data-ttu-id="6babe-1127">有効な場合の、指定された Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1127">The name of the specified web-page definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1128">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1128">Remarks</span></span>

<span data-ttu-id="6babe-1129">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1129">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1130">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1130">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1131">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1131">Example</span></span>

    No example.

## <a name="webreportstr"></a><span data-ttu-id="6babe-1132">webReportStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1132">webReportStr</span></span>
<span data-ttu-id="6babe-1133">指定した Web レポートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1133">Validates that the specified web report exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1134">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1134">Syntax</span></span>

    str webReportStr(str name)

### <a name="parameters"></a><span data-ttu-id="6babe-1135">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1135">Parameters</span></span>

| <span data-ttu-id="6babe-1136">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1136">Parameter</span></span> | <span data-ttu-id="6babe-1137">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1137">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="6babe-1138">名前</span><span class="sxs-lookup"><span data-stu-id="6babe-1138">name</span></span>      | <span data-ttu-id="6babe-1139">検証する Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1139">The name of the web report to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1140">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1140">Return Value</span></span>

<span data-ttu-id="6babe-1141">有効な場合の、指定された Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1141">The name of the specified web report, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1142">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1142">Remarks</span></span>

<span data-ttu-id="6babe-1143">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1143">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1144">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1144">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1145">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1145">Example</span></span>

    {
        str s;
        ;
        s = webReportStr(EPCSSSalesConfirm);
        print "String for web report EPCSSalesConfirm is " + s;
        pause;
    }

## <a name="websitedefstr"></a><span data-ttu-id="6babe-1146">websiteDefStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1146">websiteDefStr</span></span>
<span data-ttu-id="6babe-1147">指定した Web サイトの定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1147">Validates that the specified web-site definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1148">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1148">Syntax</span></span>

    str websiteDefStr(str resourcename)

### <a name="parameters"></a><span data-ttu-id="6babe-1149">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1149">Parameters</span></span>

| <span data-ttu-id="6babe-1150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1150">Parameter</span></span>    | <span data-ttu-id="6babe-1151">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1151">Description</span></span>                                      |
|--------------|--------------------------------------------------|
| <span data-ttu-id="6babe-1152">resourcename</span><span class="sxs-lookup"><span data-stu-id="6babe-1152">resourcename</span></span> | <span data-ttu-id="6babe-1153">検証する Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1153">The name of the Web site definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1154">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1154">Return Value</span></span>

<span data-ttu-id="6babe-1155">有効な場合の、指定された Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1155">The name of the specified web-site definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1156">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1156">Remarks</span></span>

<span data-ttu-id="6babe-1157">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1157">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1158">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1158">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1159">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1159">Example</span></span>

    {
        str s;
        ;

        s = websiteDefStr(AxSiteDef_1033_xip);
        print "string for web site definition AxSiteDef_1033_xip is " + s;
        pause;
    }

## <a name="websitetempstr"></a><span data-ttu-id="6babe-1160">webSiteTempStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1160">webSiteTempStr</span></span>
<span data-ttu-id="6babe-1161">指定した Web サイトのテンプレートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1161">Validates that the specified web-site template exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1162">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1162">Syntax</span></span>

    str websiteTempStr(str resourcename)

### <a name="parameters"></a><span data-ttu-id="6babe-1163">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1163">Parameters</span></span>

| <span data-ttu-id="6babe-1164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1164">Parameter</span></span>    | <span data-ttu-id="6babe-1165">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1165">Description</span></span>                                    |
|--------------|------------------------------------------------|
| <span data-ttu-id="6babe-1166">resourcename</span><span class="sxs-lookup"><span data-stu-id="6babe-1166">resourcename</span></span> | <span data-ttu-id="6babe-1167">検証する Web サイト テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1167">The name of the Web site template to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1168">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1168">Return Value</span></span>

<span data-ttu-id="6babe-1169">有効な場合の、指定された Web テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1169">The name of the specified web-site template, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1170">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1170">Remarks</span></span>

<span data-ttu-id="6babe-1171">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1171">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1172">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1172">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1173">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1173">Example</span></span>

    No example.

## <a name="webstaticfilestr"></a><span data-ttu-id="6babe-1174">webStaticFileStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1174">webStaticFileStr</span></span>
<span data-ttu-id="6babe-1175">指定した Web 静的ファイルがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1175">Validates that the specified web static file exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1176">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1176">Syntax</span></span>

    str webStaticFileStr(str pagename)

### <a name="parameters"></a><span data-ttu-id="6babe-1177">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1177">Parameters</span></span>

| <span data-ttu-id="6babe-1178">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1178">Parameter</span></span> | <span data-ttu-id="6babe-1179">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1179">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="6babe-1180">pagename</span><span class="sxs-lookup"><span data-stu-id="6babe-1180">pagename</span></span>  | <span data-ttu-id="6babe-1181">検証する Web 静的ファイル テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1181">The name of the web static file to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1182">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1182">Return Value</span></span>

<span data-ttu-id="6babe-1183">有効な場合の、指定された Web 静的ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1183">The name of the specified web static file, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1184">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1184">Remarks</span></span>

<span data-ttu-id="6babe-1185">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1185">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1186">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1186">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1187">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1187">Example</span></span>

    {
        str s;
        ;

        s = webStaticFileStr(AXEP);
        print "string for web static file AXEP is " + s;
        pause;
    }

## <a name="weburlitemstr"></a><span data-ttu-id="6babe-1188">webUrlItemStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1188">webUrlItemStr</span></span>
<span data-ttu-id="6babe-1189">指定した Web URL 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1189">Validates that the specified web URL item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1190">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1190">Syntax</span></span>

    str webUrlItemStr(class weburlitem)

### <a name="parameters"></a><span data-ttu-id="6babe-1191">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1191">Parameters</span></span>

| <span data-ttu-id="6babe-1192">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1192">Parameter</span></span>  | <span data-ttu-id="6babe-1193">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1193">Description</span></span>                               |
|------------|-------------------------------------------|
| <span data-ttu-id="6babe-1194">weburlitem</span><span class="sxs-lookup"><span data-stu-id="6babe-1194">weburlitem</span></span> | <span data-ttu-id="6babe-1195">検証する Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1195">The name of the web URL item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1196">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1196">Return Value</span></span>

<span data-ttu-id="6babe-1197">有効な場合の、指定された Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1197">The name of the specified web URL item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1198">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1198">Remarks</span></span>

<span data-ttu-id="6babe-1199">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1199">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1200">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1200">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1201">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1201">Example</span></span>

    {
        str s;
        ;

        s = webUrlItemStr(EPAdmin);
        print "string for web url item EPAdmin is " + s;
        pause;
    }

## <a name="webwebpartstr"></a><span data-ttu-id="6babe-1202">webWebPartStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1202">webWebPartStr</span></span>
<span data-ttu-id="6babe-1203">指定した Web パーツがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1203">Validates that the specified web part exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1204">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1204">Syntax</span></span>

    str webWebpartStr(str resourcename)

### <a name="parameters"></a><span data-ttu-id="6babe-1205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1205">Parameters</span></span>

| <span data-ttu-id="6babe-1206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1206">Parameter</span></span>    | <span data-ttu-id="6babe-1207">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1207">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="6babe-1208">resourcename</span><span class="sxs-lookup"><span data-stu-id="6babe-1208">resourcename</span></span> | <span data-ttu-id="6babe-1209">検証する Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1209">The name of the web part to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1210">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1210">Return Value</span></span>

<span data-ttu-id="6babe-1211">有効な場合の、指定された Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1211">The name of the specified web part, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1212">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1212">Remarks</span></span>

<span data-ttu-id="6babe-1213">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1213">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1214">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1214">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1215">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1215">Example</span></span>

    {
        str s;
        ;

        s = webWebpartStr(AxWebParts_cab);
        print "string for web part AxWebParts_cab is " + s;
        pause;
    }

## <a name="workflowapprovalstr"></a><span data-ttu-id="6babe-1216">workflowApprovalStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1216">workflowApprovalStr</span></span>
<span data-ttu-id="6babe-1217">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー承認の名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1217">Retrieves the name of a workflow approval in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1218">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1218">Syntax</span></span>

    str workflowapprovalstr(approval approval)

### <a name="parameters"></a><span data-ttu-id="6babe-1219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1219">Parameters</span></span>

| <span data-ttu-id="6babe-1220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1220">Parameter</span></span> | <span data-ttu-id="6babe-1221">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1221">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="6babe-1222">承認</span><span class="sxs-lookup"><span data-stu-id="6babe-1222">approval</span></span>  | <span data-ttu-id="6babe-1223">ワークフローの承認のアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1223">The Application Explorer name of the workflow approval.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1224">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1224">Return Value</span></span>

<span data-ttu-id="6babe-1225">ワークフローの承認のアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-1225">A string that represents the Application Explorer name of the workflow approval.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1226">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1226">Remarks</span></span>

<span data-ttu-id="6babe-1227">リテラル テキストの代わりにこの関数を使用して、ワークフロー承認名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1227">Use this function instead of literal text to retrieve a string that contains the workflow approval name.</span></span> <span data-ttu-id="6babe-1228">ワークフローの承認が存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1228">If the workflow approval does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="6babe-1229">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1229">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1230">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1230">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1231">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1231">Example</span></span>

<span data-ttu-id="6babe-1232">次のコード例では、変数 *str s* を **MyWorkflowApproval** に設定します。これは、アプリケーション エクスプローラーでのワークフロー承認の名前です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1232">The following code example sets the variable *str s* to **MyWorkflowApproval** which is the name of the workflow approval in the Application Explorer.</span></span>

    static void MyWorkflowApprovalStrExample(Args _args)
    {
        str s;
        ;
        s = workflowapprovalstr(MyWorkflowApproval);
        print s;
        pause;
    }

## <a name="workflowcategorystr"></a><span data-ttu-id="6babe-1233">workflowCategoryStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1233">workflowCategoryStr</span></span>
<span data-ttu-id="6babe-1234">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー カテゴリの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1234">Retrieves the name of a workflow category in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1235">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1235">Syntax</span></span>

    str workflowcategorystr(category category)

### <a name="parameters"></a><span data-ttu-id="6babe-1236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1236">Parameters</span></span>

| <span data-ttu-id="6babe-1237">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1237">Parameter</span></span> | <span data-ttu-id="6babe-1238">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1238">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="6babe-1239">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="6babe-1239">category</span></span>  | <span data-ttu-id="6babe-1240">ワークフロー カテゴリーのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1240">The Application Explorer name of the workflow category.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1241">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1241">Return Value</span></span>

<span data-ttu-id="6babe-1242">ワークフロー カテゴリのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-1242">A string that represents the Application Explorer name of the workflow category.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1243">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1243">Remarks</span></span>

<span data-ttu-id="6babe-1244">リテラル テキストの代わりにこの関数を使用して、ワークフロー カテゴリ名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1244">Use this function instead of literal text to retrieve a string that contains the workflow category name.</span></span> <span data-ttu-id="6babe-1245">ワークフローのカテゴリーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1245">If the workflow category does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="6babe-1246">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1246">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1247">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1247">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1248">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1248">Example</span></span>

<span data-ttu-id="6babe-1249">次のコード例では、変数 *str s* を **MyWorkflowCategory** に設定します。これは、アプリケーション エクスプローラーでのワークフロー カテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1249">The following code example sets the variable *str s* to **MyWorkflowCategory** which is the name of the workflow category in the Application Explorer.</span></span>

    static void MyWorkflowCategoryStrExample(Args _args)
    {
        str s;
        ;
        s = workflowcategorystr(MyWorkflowCategory);
        print s;
        pause;
    }

## <a name="workflowtaskstr"></a><span data-ttu-id="6babe-1250">workflowTaskStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1250">workflowTaskStr</span></span>
<span data-ttu-id="6babe-1251">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー タスクの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1251">Retrieves the name of a workflow task in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1252">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1252">Syntax</span></span>

    str workflowtaskstr(task task)

### <a name="parameters"></a><span data-ttu-id="6babe-1253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1253">Parameters</span></span>

| <span data-ttu-id="6babe-1254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1254">Parameter</span></span> | <span data-ttu-id="6babe-1255">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1255">Description</span></span>                                         |
|-----------|-----------------------------------------------------|
| <span data-ttu-id="6babe-1256">タスク</span><span class="sxs-lookup"><span data-stu-id="6babe-1256">task</span></span>      | <span data-ttu-id="6babe-1257">ワークフロー タスクのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1257">The Application Explorer name of the workflow task.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1258">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1258">Return Value</span></span>

<span data-ttu-id="6babe-1259">ワークフロー タスクのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="6babe-1259">A string that represents the Application Explorer name of the workflow task.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1260">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1260">Remarks</span></span>

<span data-ttu-id="6babe-1261">リテラル テキストの代わりにこの関数を使用して、ワークフロー タスク名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1261">Use this function instead of literal text to retrieve a string that contains the workflow task name.</span></span> <span data-ttu-id="6babe-1262">ワークフローのタスクーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1262">If the workflow task does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="6babe-1263">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1263">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1264">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1264">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1265">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1265">Example</span></span>

<span data-ttu-id="6babe-1266">次のコード例では、変数 *str s* を **MyWorkflowTask** に設定します。これは、アプリケーション エクスプローラーでのワークフロー タスクの名前です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1266">The following code example sets the variable *str s* to **MyWorkflowTask** which is the name of the workflow task in the Application Explorer.</span></span>

    static void MyWorkflowTaskStrExample(Args _args)
    {
        str s;
        ;
        s = workflowtaskstr(MyWorkflowTask);
        print s;
        pause;
    }

## <a name="workflowtypestr"></a><span data-ttu-id="6babe-1267">workflowTypeStr</span><span class="sxs-lookup"><span data-stu-id="6babe-1267">workflowTypeStr</span></span>
<span data-ttu-id="6babe-1268">指定したワークフロー タイプがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6babe-1268">Validates that the specified workflow type exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="6babe-1269">構文</span><span class="sxs-lookup"><span data-stu-id="6babe-1269">Syntax</span></span>

    str workflowTypeStr(str workflow)

### <a name="parameters"></a><span data-ttu-id="6babe-1270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1270">Parameters</span></span>

| <span data-ttu-id="6babe-1271">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6babe-1271">Parameter</span></span> | <span data-ttu-id="6babe-1272">説明</span><span class="sxs-lookup"><span data-stu-id="6babe-1272">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="6babe-1273">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="6babe-1273">workflow</span></span>  | <span data-ttu-id="6babe-1274">検証するワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1274">The name of the workflow type to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6babe-1275">戻り値</span><span class="sxs-lookup"><span data-stu-id="6babe-1275">Return Value</span></span>

<span data-ttu-id="6babe-1276">ワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="6babe-1276">The name of the workflow type.</span></span>

### <a name="remarks"></a><span data-ttu-id="6babe-1277">備考</span><span class="sxs-lookup"><span data-stu-id="6babe-1277">Remarks</span></span>

<span data-ttu-id="6babe-1278">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="6babe-1278">This is a compile-time function.</span></span> <span data-ttu-id="6babe-1279">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6babe-1279">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="6babe-1280">例</span><span class="sxs-lookup"><span data-stu-id="6babe-1280">Example</span></span>

    static void workFlowTypeStrExample(Args _args)
    {
        str s;
        ;
        s = workFlowTypeStr(BudgetAccountEntryType);
        print s;
        pause;
    }



