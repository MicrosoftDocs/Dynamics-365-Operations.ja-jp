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
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 29581
ms.assetid: fa6613a4-7d0b-40d3-be29-9d14c22c7d5b
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e6d7c50c39d166f4b69843dea110d12e3a3b870
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191603"
---
# <a name="x-compile-time-functions"></a><span data-ttu-id="20efa-103">X++ コンパイル時関数</span><span class="sxs-lookup"><span data-stu-id="20efa-103">X++ compile-time functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20efa-104">このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。</span><span class="sxs-lookup"><span data-stu-id="20efa-104">This topic lists the compile-time functions and describes their syntax, parameters, and return values.</span></span>

<a name="overview"></a><span data-ttu-id="20efa-105">概要</span><span class="sxs-lookup"><span data-stu-id="20efa-105">Overview</span></span>
--------

<span data-ttu-id="20efa-106">コンパイル時関数は、X++ コードのコンパイル時に早期実行されます。</span><span class="sxs-lookup"><span data-stu-id="20efa-106">Compile-time functions are executed early during compilation of X++ code.</span></span> <span data-ttu-id="20efa-107">アプリケーション エクスプローラーに保存されているメタデータの変更に対してコードを復元するためには、可能な限り X++ で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20efa-107">They should be used wherever possible in X++ code to make the code resilient to changes to the metadata stored in the Application Explorer.</span></span> <span data-ttu-id="20efa-108">コンパイル時関数は、コンパイラによって入力値が検証されます。</span><span class="sxs-lookup"><span data-stu-id="20efa-108">Compile-time functions have their input value verified by the compiler.</span></span> <span data-ttu-id="20efa-109">入力された値が見つからず、アプリケーション エクスプローラーの既存のオブジェクトが一致しない場合は、コンパイラーはエラーを発行します。</span><span class="sxs-lookup"><span data-stu-id="20efa-109">If the input value is not found to match any existing object in the Application Explorer, the compiler issues an error.</span></span> <span data-ttu-id="20efa-110">コンパイラは実行時に変数に含まれる値を判別できないため、これらの関数への入力はリテラルでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="20efa-110">The inputs to these functions must be literals, because the compiler cannot determine the value that a variable contains at run time.</span></span> <span data-ttu-id="20efa-111">コンパイル時関数は、メタデータ アサーション関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-111">A compile-time function is a metadata assertion function.</span></span> <span data-ttu-id="20efa-112">アプリケーション エクスプローラーでエンティティを表す引数を取得し、コンパイル時にその引数を検証します。</span><span class="sxs-lookup"><span data-stu-id="20efa-112">It takes arguments that represents an entity in the Application Explorer and validates the arguments at compile time.</span></span> <span data-ttu-id="20efa-113">実行時に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="20efa-113">It has no effect at run time.</span></span> <span data-ttu-id="20efa-114">属性は **SysAttribute** クラスから継承するクラスです。</span><span class="sxs-lookup"><span data-stu-id="20efa-114">Attributes are classes that inherit from the **SysAttribute** class.</span></span> <span data-ttu-id="20efa-115">フォーム、レポート、クエリ、メニュー のメタデータの検証をサポートするには、コントロールの **AutoDeclaration** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="20efa-115">To support the validation of form, report, query, and menu metadata, use the **AutoDeclaration** property on controls.</span></span> <span data-ttu-id="20efa-116">これらの機能のほとんどは、アプリケーション エクスプローラーにある項目に関するメタデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-116">Most of these functions retrieve metadata about items that are in the Application Explorer.</span></span> <span data-ttu-id="20efa-117">いくつかの一般的なコンパイル時機能は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="20efa-117">Some common compile time functions are as follows:</span></span>

-   <span data-ttu-id="20efa-118">`classNum` – クラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-118">`classNum` – Retrieves the ID of a class.</span></span>
-   <span data-ttu-id="20efa-119">`classStr` – コンパイル時に、その名前のクラスが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="20efa-119">`classStr` – During compile time, verifies that a class of that name exists.</span></span> <span data-ttu-id="20efa-120">この方法は、実行時にエラーを後で発見するよりも優れています。</span><span class="sxs-lookup"><span data-stu-id="20efa-120">This approach is better than discovering the error later during run time.</span></span>
-   <span data-ttu-id="20efa-121">`evalBuf`– X++ コードの入力文字列を評価し、結果を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-121">`evalBuf`– Evaluates the input string of X++ code, and then returns the results as a string.</span></span>
-   <span data-ttu-id="20efa-122">`literalStr` – は、文字列 `"@SYS12345"` などのラベルの文字列表示が与えられたときにラベル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-122">`literalStr` – retrieves a label ID when given the string representation of a label, such as the string `"@SYS12345"`.</span></span> <span data-ttu-id="20efa-123">たとえば、`myLabel.exists(literalStr("@SYS12345"));`。</span><span class="sxs-lookup"><span data-stu-id="20efa-123">For example, `myLabel.exists(literalStr("@SYS12345"));`.</span></span>

| <span data-ttu-id="20efa-124">**メモ**</span><span class="sxs-lookup"><span data-stu-id="20efa-124">**Note**</span></span>                                                         |
|------------------------------------------------------------------|
| <span data-ttu-id="20efa-125">X++ コンパイル時関数は .NET プログラムから呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="20efa-125">X++ compile time functions cannot be called from a .NET program.</span></span> |

### <a name="functions"></a><span data-ttu-id="20efa-126">関数</span><span class="sxs-lookup"><span data-stu-id="20efa-126">Functions</span></span>

## <a name="attributestr"></a><span data-ttu-id="20efa-127">attributeStr</span><span class="sxs-lookup"><span data-stu-id="20efa-127">attributeStr</span></span>
<span data-ttu-id="20efa-128">指定した属性クラスがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-128">Validates that the specified attribute class exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-129">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-129">Syntax</span></span>

    str classStr(class class)

### <a name="parameters"></a><span data-ttu-id="20efa-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-130">Parameters</span></span>

| <span data-ttu-id="20efa-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-131">Parameter</span></span> | <span data-ttu-id="20efa-132">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-132">Description</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="20efa-133">クラス</span><span class="sxs-lookup"><span data-stu-id="20efa-133">class</span></span>     | <span data-ttu-id="20efa-134">検証する属性の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-134">The name of the attribute to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-135">Return Value</span></span>

<span data-ttu-id="20efa-136">属性の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-136">The name of the attribute.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-137">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-137">Remarks</span></span>

<span data-ttu-id="20efa-138">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-138">This is a compile-time function.</span></span> <span data-ttu-id="20efa-139">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-139">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-140">例</span><span class="sxs-lookup"><span data-stu-id="20efa-140">Example</span></span>

    static void attributeStrExample(Args _args)
    {
        str s;
        ;
        s = attributeStr(AifDocumentOperationAttribute);
        print s;
        pause;
    }

## <a name="classnum"></a><span data-ttu-id="20efa-141">classNum</span><span class="sxs-lookup"><span data-stu-id="20efa-141">classNum</span></span>
<span data-ttu-id="20efa-142">指定されたクラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-142">Retrieves the ID of the specified class.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-143">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-143">Syntax</span></span>

    int classNum(class class)

### <a name="parameters"></a><span data-ttu-id="20efa-144">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-144">Parameters</span></span>

| <span data-ttu-id="20efa-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-145">Parameter</span></span> | <span data-ttu-id="20efa-146">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-146">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="20efa-147">クラス</span><span class="sxs-lookup"><span data-stu-id="20efa-147">class</span></span>     | <span data-ttu-id="20efa-148">ID を取得するクラス。</span><span class="sxs-lookup"><span data-stu-id="20efa-148">The class for which to retrieve the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-149">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-149">Return Value</span></span>

<span data-ttu-id="20efa-150">指定されたクラスの ID。</span><span class="sxs-lookup"><span data-stu-id="20efa-150">The ID of the specified class.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-151">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-151">Remarks</span></span>

<span data-ttu-id="20efa-152">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-152">This is a compile-time function.</span></span> <span data-ttu-id="20efa-153">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-153">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-154">例</span><span class="sxs-lookup"><span data-stu-id="20efa-154">Example</span></span>

    static void classNumExample(Args _args)
    {
        int i;
        ;
        i = classNum(Global);
        print i;
        pause;
    }

## <a name="classstr"></a><span data-ttu-id="20efa-155">classStr</span><span class="sxs-lookup"><span data-stu-id="20efa-155">classStr</span></span>
<span data-ttu-id="20efa-156">文字列としてクラスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-156">Retrieves the name of a class as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-157">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-157">Syntax</span></span>

    str classStr(class class)

### <a name="parameters"></a><span data-ttu-id="20efa-158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-158">Parameters</span></span>

| <span data-ttu-id="20efa-159">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-159">Parameter</span></span> | <span data-ttu-id="20efa-160">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-160">Description</span></span>                      |
|-----------|----------------------------------|
| <span data-ttu-id="20efa-161">クラス</span><span class="sxs-lookup"><span data-stu-id="20efa-161">class</span></span>     | <span data-ttu-id="20efa-162">返すクラスの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-162">The name of the class to return.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-163">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-163">Return Value</span></span>

<span data-ttu-id="20efa-164">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-164">The name of the class.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-165">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-165">Remarks</span></span>

<span data-ttu-id="20efa-166">リテラル テキストの代わりにこの関数を使用して、クラス名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-166">Use this function instead of literal text to retrieve a string that contains the class name.</span></span> <span data-ttu-id="20efa-167">クラスが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="20efa-167">If the class does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="20efa-168">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-168">This is a compile-time function.</span></span> <span data-ttu-id="20efa-169">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-169">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-170">例</span><span class="sxs-lookup"><span data-stu-id="20efa-170">Example</span></span>

    static void clStrExample(Args _args)
    {
        str s;
        ;
        s = classStr(Global);
        print s;
        pause;
    }

## <a name="configurationkeynum"></a><span data-ttu-id="20efa-171">configurationKeyNum</span><span class="sxs-lookup"><span data-stu-id="20efa-171">configurationKeyNum</span></span>
<span data-ttu-id="20efa-172">指定されたコンフィギュレーション キーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-172">Retrieves the ID of the specified configuration key.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-173">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-173">Syntax</span></span>

    int configurationKeyNum(str keyname)

### <a name="parameters"></a><span data-ttu-id="20efa-174">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-174">Parameters</span></span>

| <span data-ttu-id="20efa-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-175">Parameter</span></span> | <span data-ttu-id="20efa-176">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-176">Description</span></span>                                       |
|-----------|---------------------------------------------------|
| <span data-ttu-id="20efa-177">keyname</span><span class="sxs-lookup"><span data-stu-id="20efa-177">keyname</span></span>   | <span data-ttu-id="20efa-178">ID を返すコンフィギュレーション キー。</span><span class="sxs-lookup"><span data-stu-id="20efa-178">The configuration key for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-179">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-179">Return Value</span></span>

<span data-ttu-id="20efa-180">指定されたコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="20efa-180">The ID of the specified configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-181">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-181">Remarks</span></span>

<span data-ttu-id="20efa-182">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-182">This is a compile-time function.</span></span> <span data-ttu-id="20efa-183">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-183">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-184">例</span><span class="sxs-lookup"><span data-stu-id="20efa-184">Example</span></span>

    static void configurationKeyNum(Args _args)
    {
        int i;
        ;
        i = configurationKeyNum(AIF);
        print i;
        pause;
    }

## <a name="configurationkeystr"></a><span data-ttu-id="20efa-185">configurationKeyStr</span><span class="sxs-lookup"><span data-stu-id="20efa-185">configurationKeyStr</span></span>
<span data-ttu-id="20efa-186">文字列としてコンフィギュレーション キーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-186">Retrieves the name of a configuration key as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-187">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-187">Syntax</span></span>

    str configurationKeyStr(str keyname)

### <a name="parameters"></a><span data-ttu-id="20efa-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-188">Parameters</span></span>

| <span data-ttu-id="20efa-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-189">Parameter</span></span> | <span data-ttu-id="20efa-190">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-190">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="20efa-191">keyname</span><span class="sxs-lookup"><span data-stu-id="20efa-191">keyname</span></span>   | <span data-ttu-id="20efa-192">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-192">The name of the configuration key.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-193">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-193">Return Value</span></span>

<span data-ttu-id="20efa-194">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-194">The name of the configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-195">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-195">Remarks</span></span>

<span data-ttu-id="20efa-196">リテラル テキストの代わりにこの関数を使用して、構成キー名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-196">Use this function instead of literal text to retrieve a string that contains the configuration key name.</span></span> <span data-ttu-id="20efa-197">キーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="20efa-197">If the key does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="20efa-198">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-198">This is a compile-time function.</span></span> <span data-ttu-id="20efa-199">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-199">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-200">例</span><span class="sxs-lookup"><span data-stu-id="20efa-200">Example</span></span>

    static void configurationKeyStrExample(Args _args)
    {
        str s;
        ;
        s = configurationKeyStr(AIF);
        print s;
        pause;
    }

## <a name="dataentitydatasourcestr"></a><span data-ttu-id="20efa-201">dataEntityDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="20efa-201">dataEntityDataSourceStr</span></span>
<span data-ttu-id="20efa-202">データ エンティティのデータ ソースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-202">Retrieves the name of a data source of a data entity.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-203">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-203">Syntax</span></span>

    str dataEntityDataSourceStr(str dataEntity, str dataSource)

### <a name="parameters"></a><span data-ttu-id="20efa-204">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-204">Parameters</span></span>

| <span data-ttu-id="20efa-205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-205">Parameter</span></span>  | <span data-ttu-id="20efa-206">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-206">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="20efa-207">dataEntity</span><span class="sxs-lookup"><span data-stu-id="20efa-207">dataEntity</span></span> | <span data-ttu-id="20efa-208">データ エンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-208">The name of the data entity.</span></span> |
| <span data-ttu-id="20efa-209">dataSource</span><span class="sxs-lookup"><span data-stu-id="20efa-209">dataSource</span></span> | <span data-ttu-id="20efa-210">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-210">The name of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-211">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-211">Return Value</span></span>

<span data-ttu-id="20efa-212">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-212">The name of the data source.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-213">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-213">Remarks</span></span>

<span data-ttu-id="20efa-214">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-214">This is a compile-time function.</span></span> <span data-ttu-id="20efa-215">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-215">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-216">例</span><span class="sxs-lookup"><span data-stu-id="20efa-216">Example</span></span>

    No example.

## <a name="delegatestr"></a><span data-ttu-id="20efa-217">delegateStr</span><span class="sxs-lookup"><span data-stu-id="20efa-217">delegateStr</span></span>
<span data-ttu-id="20efa-218">委任の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-218">Returns the name of the delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-219">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-219">Syntax</span></span>

    str delegateStr(str class, str instanceDelegate)

### <a name="parameters"></a><span data-ttu-id="20efa-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-220">Parameters</span></span>

| <span data-ttu-id="20efa-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-221">Parameter</span></span>        | <span data-ttu-id="20efa-222">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-222">Description</span></span>                            |
|------------------|----------------------------------------|
| <span data-ttu-id="20efa-223">クラス</span><span class="sxs-lookup"><span data-stu-id="20efa-223">class</span></span>            | <span data-ttu-id="20efa-224">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-224">The name of the class, table, or form.</span></span> |
| <span data-ttu-id="20efa-225">instanceDelegate</span><span class="sxs-lookup"><span data-stu-id="20efa-225">instanceDelegate</span></span> | <span data-ttu-id="20efa-226">インスタンス デリゲートの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-226">The name of the instance delegate.</span></span>     |

### <a name="return-value"></a><span data-ttu-id="20efa-227">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-227">Return Value</span></span>

<span data-ttu-id="20efa-228">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="20efa-228">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-229">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-229">Remarks</span></span>

<span data-ttu-id="20efa-230">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-230">This is a compile-time function.</span></span> <span data-ttu-id="20efa-231">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-231">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-232">例</span><span class="sxs-lookup"><span data-stu-id="20efa-232">Example</span></span>

    No example.

## <a name="dimensionhierarchylevelstr"></a><span data-ttu-id="20efa-233">dimensionHierarchyLevelStr</span><span class="sxs-lookup"><span data-stu-id="20efa-233">dimensionHierarchyLevelStr</span></span>
<span data-ttu-id="20efa-234">分析コード階層レベルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-234">Returns the name of the dimension hierarchy level.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-235">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-235">Syntax</span></span>

    str dimensionHierarchyLevelStr(str dimensionHierarchyLevel)

### <a name="parameters"></a><span data-ttu-id="20efa-236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-236">Parameters</span></span>

| <span data-ttu-id="20efa-237">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-237">Parameter</span></span>               | <span data-ttu-id="20efa-238">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-238">Description</span></span>                                |
|-------------------------|--------------------------------------------|
| <span data-ttu-id="20efa-239">dimensionHierarchyLevel</span><span class="sxs-lookup"><span data-stu-id="20efa-239">dimensionHierarchyLevel</span></span> | <span data-ttu-id="20efa-240">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-240">The name of the dimension hierarchy level.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-241">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-241">Return Value</span></span>

<span data-ttu-id="20efa-242">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-242">The name of the dimension hierarchy level.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-243">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-243">Remarks</span></span>

<span data-ttu-id="20efa-244">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-244">This is a compile-time function.</span></span> <span data-ttu-id="20efa-245">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-245">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-246">例</span><span class="sxs-lookup"><span data-stu-id="20efa-246">Example</span></span>

    No example.

## <a name="dimensionhierarchystr"></a><span data-ttu-id="20efa-247">dimensionHierarchyStr</span><span class="sxs-lookup"><span data-stu-id="20efa-247">dimensionHierarchyStr</span></span>
<span data-ttu-id="20efa-248">分析コード階層の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-248">Returns the name of the dimension hierarchy.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-249">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-249">Syntax</span></span>

    str dimensionHierarchyStr(str dimensionHierarchy)

### <a name="parameters"></a><span data-ttu-id="20efa-250">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-250">Parameters</span></span>

| <span data-ttu-id="20efa-251">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-251">Parameter</span></span>          | <span data-ttu-id="20efa-252">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-252">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="20efa-253">dimensionHierarchy</span><span class="sxs-lookup"><span data-stu-id="20efa-253">dimensionHierarchy</span></span> | <span data-ttu-id="20efa-254">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-254">The name of the dimension hierarchy.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-255">Return Value</span></span>

<span data-ttu-id="20efa-256">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-256">The name of the dimension hierarchy.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-257">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-257">Remarks</span></span>

<span data-ttu-id="20efa-258">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-258">This is a compile-time function.</span></span> <span data-ttu-id="20efa-259">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-259">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-260">例</span><span class="sxs-lookup"><span data-stu-id="20efa-260">Example</span></span>

    No example.

## <a name="dimensionreferencestr"></a><span data-ttu-id="20efa-261">dimensionReferenceStr</span><span class="sxs-lookup"><span data-stu-id="20efa-261">dimensionReferenceStr</span></span>
<span data-ttu-id="20efa-262">分析コード参照の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-262">Returns the name of the dimension reference.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-263">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-263">Syntax</span></span>

    str dimensionReferenceStr(str dimensionReference)

### <a name="parameters"></a><span data-ttu-id="20efa-264">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-264">Parameters</span></span>

| <span data-ttu-id="20efa-265">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-265">Parameter</span></span>          | <span data-ttu-id="20efa-266">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-266">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="20efa-267">dimensionReference</span><span class="sxs-lookup"><span data-stu-id="20efa-267">dimensionReference</span></span> | <span data-ttu-id="20efa-268">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-268">The name of the dimension reference.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-269">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-269">Return Value</span></span>

<span data-ttu-id="20efa-270">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-270">The name of the dimension reference.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-271">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-271">Remarks</span></span>

<span data-ttu-id="20efa-272">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-272">This is a compile-time function.</span></span> <span data-ttu-id="20efa-273">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-273">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-274">例</span><span class="sxs-lookup"><span data-stu-id="20efa-274">Example</span></span>

    No example.

## <a name="dutystr"></a><span data-ttu-id="20efa-275">dutyStr</span><span class="sxs-lookup"><span data-stu-id="20efa-275">dutyStr</span></span>
<span data-ttu-id="20efa-276">指定したセキュリティ職務権限の名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-276">Retrieves a string that represents the name of the specified security duty.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-277">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-277">Syntax</span></span>

    str dutyStr(str securityDuty)

### <a name="parameters"></a><span data-ttu-id="20efa-278">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-278">Parameters</span></span>

| <span data-ttu-id="20efa-279">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-279">Parameter</span></span>    | <span data-ttu-id="20efa-280">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-280">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="20efa-281">securityDuty</span><span class="sxs-lookup"><span data-stu-id="20efa-281">securityDuty</span></span> | <span data-ttu-id="20efa-282">セキュリティ職務権限の名前です。</span><span class="sxs-lookup"><span data-stu-id="20efa-282">The name of the security duty.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-283">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-283">Return Value</span></span>

<span data-ttu-id="20efa-284">文字列のセキュリティ職務の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-284">The name of the security duty in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-285">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-285">Remarks</span></span>

<span data-ttu-id="20efa-286">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-286">This is a compile-time function.</span></span> <span data-ttu-id="20efa-287">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-287">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-288">例</span><span class="sxs-lookup"><span data-stu-id="20efa-288">Example</span></span>

    No example.

## <a name="enumcnt"></a><span data-ttu-id="20efa-289">enumCnt</span><span class="sxs-lookup"><span data-stu-id="20efa-289">enumCnt</span></span>
<span data-ttu-id="20efa-290">指定された列挙型の要素数を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-290">Retrieves the number of elements in the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-291">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-291">Syntax</span></span>

    int enumCnt(enum enumtype)

### <a name="parameters"></a><span data-ttu-id="20efa-292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-292">Parameters</span></span>

| <span data-ttu-id="20efa-293">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-293">Parameter</span></span> | <span data-ttu-id="20efa-294">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-294">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="20efa-295">enumtype</span><span class="sxs-lookup"><span data-stu-id="20efa-295">enumtype</span></span>  | <span data-ttu-id="20efa-296">列挙型タイプ。</span><span class="sxs-lookup"><span data-stu-id="20efa-296">The enumeration type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-297">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-297">Return Value</span></span>

<span data-ttu-id="20efa-298">指定された列挙型の要素数。</span><span class="sxs-lookup"><span data-stu-id="20efa-298">The number of elements in the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-299">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-299">Remarks</span></span>

<span data-ttu-id="20efa-300">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-300">This is a compile-time function.</span></span> <span data-ttu-id="20efa-301">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-301">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-302">例</span><span class="sxs-lookup"><span data-stu-id="20efa-302">Example</span></span>

    enumCnt(NoYes); //Returns 2, as the two elements are Yes and No.

## <a name="enumliteralstr"></a><span data-ttu-id="20efa-303">enumLiteralStr</span><span class="sxs-lookup"><span data-stu-id="20efa-303">enumLiteralStr</span></span>
<span data-ttu-id="20efa-304">指定した文字列が指定した列挙型の要素であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="20efa-304">Indicates whether the specified string is an element of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-305">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-305">Syntax</span></span>

    enumLiteralStr(enum enum, string str)

### <a name="parameters"></a><span data-ttu-id="20efa-306">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-306">Parameters</span></span>

| <span data-ttu-id="20efa-307">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-307">Parameter</span></span> | <span data-ttu-id="20efa-308">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-308">Description</span></span>                                                      |
|-----------|------------------------------------------------------------------|
| <span data-ttu-id="20efa-309">列挙型</span><span class="sxs-lookup"><span data-stu-id="20efa-309">enum</span></span>      | <span data-ttu-id="20efa-310">指定された値を取得する列挙型。</span><span class="sxs-lookup"><span data-stu-id="20efa-310">The enumeration type from which to retrieve the specified value.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-311">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-311">Return Value</span></span>

<span data-ttu-id="20efa-312">指定された文字列が見つかった場合の *str* パラメーターの値。それ以外の場合は、コンパイル エラーです。</span><span class="sxs-lookup"><span data-stu-id="20efa-312">The value of the *str* parameter if the specified string was found; otherwise, a compilation error.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-313">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-313">Remarks</span></span>

<span data-ttu-id="20efa-314">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-314">This is a compile-time function.</span></span> <span data-ttu-id="20efa-315">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-315">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-316">例</span><span class="sxs-lookup"><span data-stu-id="20efa-316">Example</span></span>

    static void getEnumValueAsString()
    {
        str i;
        i = enumLiteralStr(ABCEnum, "valueInABCEnum");
        print i;
        pause;
    }

## <a name="enumnum"></a><span data-ttu-id="20efa-317">enumNum</span><span class="sxs-lookup"><span data-stu-id="20efa-317">enumNum</span></span>
<span data-ttu-id="20efa-318">指定された列挙型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-318">Retrieves the ID of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-319">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-319">Syntax</span></span>

    int enumNum(enum enum)

### <a name="parameters"></a><span data-ttu-id="20efa-320">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-320">Parameters</span></span>

| <span data-ttu-id="20efa-321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-321">Parameter</span></span> | <span data-ttu-id="20efa-322">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-322">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="20efa-323">列挙型</span><span class="sxs-lookup"><span data-stu-id="20efa-323">enum</span></span>      | <span data-ttu-id="20efa-324">ID を返す列挙。</span><span class="sxs-lookup"><span data-stu-id="20efa-324">The enumeration for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-325">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-325">Return Value</span></span>

<span data-ttu-id="20efa-326">指定された列挙型の ID。</span><span class="sxs-lookup"><span data-stu-id="20efa-326">The ID of the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-327">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-327">Remarks</span></span>

<span data-ttu-id="20efa-328">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-328">This is a compile-time function.</span></span> <span data-ttu-id="20efa-329">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-329">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-330">例</span><span class="sxs-lookup"><span data-stu-id="20efa-330">Example</span></span>

    static void enumNum(Args _args)
    {
        int i;
        ;
        i = enumNum(ABC);
        print i;
        pause;
    }

## <a name="enumstr"></a><span data-ttu-id="20efa-331">enumStr</span><span class="sxs-lookup"><span data-stu-id="20efa-331">enumStr</span></span>
<span data-ttu-id="20efa-332">文字列として列挙型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-332">Retrieves the name of an enumeration as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-333">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-333">Syntax</span></span>

    str enumStr(enum enum)

### <a name="parameters"></a><span data-ttu-id="20efa-334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-334">Parameters</span></span>

| <span data-ttu-id="20efa-335">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-335">Parameter</span></span> | <span data-ttu-id="20efa-336">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-336">Description</span></span>                  |
|-----------|------------------------------|
| <span data-ttu-id="20efa-337">列挙型</span><span class="sxs-lookup"><span data-stu-id="20efa-337">enum</span></span>      | <span data-ttu-id="20efa-338">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-338">The name of the enumeration.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-339">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-339">Return Value</span></span>

<span data-ttu-id="20efa-340">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-340">The name of the enumeration.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-341">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-341">Remarks</span></span>

<span data-ttu-id="20efa-342">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-342">This is a compile-time function.</span></span> <span data-ttu-id="20efa-343">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-343">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-344">例</span><span class="sxs-lookup"><span data-stu-id="20efa-344">Example</span></span>

    static void enumStrExample(Args _args)
    {
        str s;
        ;
        s = enumStr(ABC);
        print s;
        pause;
    }

## <a name="extendedtypenum"></a><span data-ttu-id="20efa-345">extendedTypeNum</span><span class="sxs-lookup"><span data-stu-id="20efa-345">extendedTypeNum</span></span>
<span data-ttu-id="20efa-346">指定された拡張データ型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-346">Retrieves the ID of the specified extended data type.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-347">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-347">Syntax</span></span>

    int extendedTypeNum(int str)

### <a name="parameters"></a><span data-ttu-id="20efa-348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-348">Parameters</span></span>

| <span data-ttu-id="20efa-349">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-349">Parameter</span></span> | <span data-ttu-id="20efa-350">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-350">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="20efa-351">str</span><span class="sxs-lookup"><span data-stu-id="20efa-351">str</span></span>       | <span data-ttu-id="20efa-352">ID を返す拡張データ型。</span><span class="sxs-lookup"><span data-stu-id="20efa-352">The extended data type for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-353">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-353">Return Value</span></span>

<span data-ttu-id="20efa-354">指定された拡張データ型の ID。</span><span class="sxs-lookup"><span data-stu-id="20efa-354">The ID of the specified extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-355">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-355">Remarks</span></span>

<span data-ttu-id="20efa-356">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-356">This is a compile-time function.</span></span> <span data-ttu-id="20efa-357">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-357">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-358">例</span><span class="sxs-lookup"><span data-stu-id="20efa-358">Example</span></span>

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

## <a name="extendedtypestr"></a><span data-ttu-id="20efa-359">extendedTypeStr</span><span class="sxs-lookup"><span data-stu-id="20efa-359">extendedTypeStr</span></span>
<span data-ttu-id="20efa-360">文字列として拡張データ型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-360">Retrieves the name of an extended data type as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-361">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-361">Syntax</span></span>

    str extendedTypeStr(int str)

### <a name="parameters"></a><span data-ttu-id="20efa-362">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-362">Parameters</span></span>

| <span data-ttu-id="20efa-363">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-363">Parameter</span></span> | <span data-ttu-id="20efa-364">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-364">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="20efa-365">str</span><span class="sxs-lookup"><span data-stu-id="20efa-365">str</span></span>       | <span data-ttu-id="20efa-366">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-366">The name of the extended data type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-367">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-367">Return Value</span></span>

<span data-ttu-id="20efa-368">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-368">The name of the extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-369">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-369">Remarks</span></span>

<span data-ttu-id="20efa-370">リテラル テキストの代わりにこの関数を使用すると、拡張データ型名を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-370">Use this function instead of literal text to return a string that contains the extended data type name.</span></span> <span data-ttu-id="20efa-371">データ タイプが存在しない場合、**extendedTypeStr** 関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="20efa-371">If the data type does not exist, the **extendedTypeStr** function generates a syntax error at compile time.</span></span> <span data-ttu-id="20efa-372">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-372">This is a compile-time function.</span></span> <span data-ttu-id="20efa-373">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-373">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-374">例</span><span class="sxs-lookup"><span data-stu-id="20efa-374">Example</span></span>

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

## <a name="fieldnum"></a><span data-ttu-id="20efa-375">fieldNum</span><span class="sxs-lookup"><span data-stu-id="20efa-375">fieldNum</span></span>
<span data-ttu-id="20efa-376">指定したフィールドの ID 番号を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-376">Returns the ID number of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-377">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-377">Syntax</span></span>

    int fieldNum(str tableName, str fieldName)

### <a name="parameters"></a><span data-ttu-id="20efa-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-378">Parameters</span></span>

| <span data-ttu-id="20efa-379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-379">Parameter</span></span> | <span data-ttu-id="20efa-380">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-380">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="20efa-381">tableName</span><span class="sxs-lookup"><span data-stu-id="20efa-381">tableName</span></span> | <span data-ttu-id="20efa-382">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-382">The name of the table.</span></span> |
| <span data-ttu-id="20efa-383">fieldName</span><span class="sxs-lookup"><span data-stu-id="20efa-383">fieldName</span></span> | <span data-ttu-id="20efa-384">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-384">The name of the field.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-385">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-385">Return Value</span></span>

<span data-ttu-id="20efa-386">指定されたフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="20efa-386">The ID of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-387">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-387">Remarks</span></span>

<span data-ttu-id="20efa-388">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-388">This is a compile-time function.</span></span> <span data-ttu-id="20efa-389">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-389">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-390">例</span><span class="sxs-lookup"><span data-stu-id="20efa-390">Example</span></span>

<span data-ttu-id="20efa-391">次の例では、**CashDisc** フィールドの番号を **CustTable** テーブルに出力します。</span><span class="sxs-lookup"><span data-stu-id="20efa-391">The following example prints the number of the **CashDisc** field in the **CustTable** table.</span></span>

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

## <a name="fieldpname"></a><span data-ttu-id="20efa-392">fieldPName</span><span class="sxs-lookup"><span data-stu-id="20efa-392">fieldPName</span></span>
<span data-ttu-id="20efa-393">指定されたフィールドのラベルを取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-393">Retrieves the label of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-394">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-394">Syntax</span></span>

    str fieldPName(str tableid, str fieldid)

### <a name="parameters"></a><span data-ttu-id="20efa-395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-395">Parameters</span></span>

| <span data-ttu-id="20efa-396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-396">Parameter</span></span> | <span data-ttu-id="20efa-397">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-397">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="20efa-398">tableid</span><span class="sxs-lookup"><span data-stu-id="20efa-398">tableid</span></span>   | <span data-ttu-id="20efa-399">指定されたフィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="20efa-399">The table that contains the specified field.</span></span> |
| <span data-ttu-id="20efa-400">fieldid</span><span class="sxs-lookup"><span data-stu-id="20efa-400">fieldid</span></span>   | <span data-ttu-id="20efa-401">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="20efa-401">The field to convert.</span></span>                        |

### <a name="return-value"></a><span data-ttu-id="20efa-402">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-402">Return Value</span></span>

<span data-ttu-id="20efa-403">フィールドのラベル。</span><span class="sxs-lookup"><span data-stu-id="20efa-403">The label of the field.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-404">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-404">Remarks</span></span>

<span data-ttu-id="20efa-405">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-405">This is a compile-time function.</span></span> <span data-ttu-id="20efa-406">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-406">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-407">例</span><span class="sxs-lookup"><span data-stu-id="20efa-407">Example</span></span>

<span data-ttu-id="20efa-408">次の例では、**CashDisc** フィールドのラベルを出力します。</span><span class="sxs-lookup"><span data-stu-id="20efa-408">The following example prints the label of the **CashDisc** field.</span></span>

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

## <a name="fieldstr"></a><span data-ttu-id="20efa-409">fieldStr</span><span class="sxs-lookup"><span data-stu-id="20efa-409">fieldStr</span></span>
<span data-ttu-id="20efa-410">指定したフィールドのフィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-410">Retrieves the field name of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-411">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-411">Syntax</span></span>

    str fieldStr(str tableid, str fieldid)

### <a name="parameters"></a><span data-ttu-id="20efa-412">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-412">Parameters</span></span>

| <span data-ttu-id="20efa-413">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-413">Parameter</span></span> | <span data-ttu-id="20efa-414">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-414">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="20efa-415">tableid</span><span class="sxs-lookup"><span data-stu-id="20efa-415">tableid</span></span>   | <span data-ttu-id="20efa-416">フィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="20efa-416">The table that contains the field.</span></span> |
| <span data-ttu-id="20efa-417">fieldid</span><span class="sxs-lookup"><span data-stu-id="20efa-417">fieldid</span></span>   | <span data-ttu-id="20efa-418">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="20efa-418">The field to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="20efa-419">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-419">Return Value</span></span>

<span data-ttu-id="20efa-420">指定したフィールドのフィールド名。</span><span class="sxs-lookup"><span data-stu-id="20efa-420">The field name of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-421">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-421">Remarks</span></span>

<span data-ttu-id="20efa-422">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-422">This is a compile-time function.</span></span> <span data-ttu-id="20efa-423">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-423">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-424">例</span><span class="sxs-lookup"><span data-stu-id="20efa-424">Example</span></span>

<span data-ttu-id="20efa-425">次の例では、**CashDisc** フィールドの名前を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="20efa-425">The following example assigns the name of the **CashDisc** field to the *myText* variable.</span></span>

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

## <a name="formcontrolstr"></a><span data-ttu-id="20efa-426">formControlStr</span><span class="sxs-lookup"><span data-stu-id="20efa-426">formControlStr</span></span>
<span data-ttu-id="20efa-427">X++ コンパイラは、コントロールがフォームに存在するかどうかをチェックし、関数呼び出しを有効なコントロール名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="20efa-427">Causes the X++ compiler to check whether the control exists on the form, and to replace the function call with a string of the valid control name.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-428">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-428">Syntax</span></span>

    str formControlStr(formName, controlName)

### <a name="parameters"></a><span data-ttu-id="20efa-429">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-429">Parameters</span></span>

| <span data-ttu-id="20efa-430">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-430">Parameter</span></span>   | <span data-ttu-id="20efa-431">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-431">Description</span></span>                                                          |
|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="20efa-432">formName</span><span class="sxs-lookup"><span data-stu-id="20efa-432">formName</span></span>    | <span data-ttu-id="20efa-433">引用符ではなく、フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-433">The name of the form, not in quotation marks.</span></span>                        |
| <span data-ttu-id="20efa-434">controlName</span><span class="sxs-lookup"><span data-stu-id="20efa-434">controlName</span></span> | <span data-ttu-id="20efa-435">フォーム上のコントロールの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="20efa-435">The name of the control that is on the form, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-436">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-436">Return Value</span></span>

<span data-ttu-id="20efa-437">アプリケーション エクスプローラーで表示されるコントロールの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-437">A string that contains the name of the control as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-438">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-438">Remarks</span></span>

<span data-ttu-id="20efa-439">コントロールがフォームに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20efa-439">A compile error is issued if the compiler determines that the control does not exist on the form.</span></span> <span data-ttu-id="20efa-440">X++ コードが引用符が含まれる文字列を使用してコントロールの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="20efa-440">If your X++ code uses a string that contains quotation marks to supply the control name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="20efa-441">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="20efa-441">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="20efa-442">コンパイラにより実行される **formControlStr** などの X++ 関数は、コンパイル時関数と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="20efa-442">X++ functions such as **formControlStr** that are executed by the compiler are called compile-time functions or compile-time functions.</span></span> <span data-ttu-id="20efa-443">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="20efa-443">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="20efa-444">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="20efa-444">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="20efa-445">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-445">This is a compile-time function.</span></span> <span data-ttu-id="20efa-446">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-446">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-447">例</span><span class="sxs-lookup"><span data-stu-id="20efa-447">Example</span></span>

    No example.

## <a name="formdatafieldstr"></a><span data-ttu-id="20efa-448">formDataFieldStr</span><span class="sxs-lookup"><span data-stu-id="20efa-448">formDataFieldStr</span></span>
<span data-ttu-id="20efa-449">フォームのデータ フィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-449">Returns the name of a data field in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-450">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-450">Syntax</span></span>

    str formDataFieldStr(str formName, str dataSource, str dataField)

### <a name="parameters"></a><span data-ttu-id="20efa-451">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-451">Parameters</span></span>

| <span data-ttu-id="20efa-452">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-452">Parameter</span></span>  | <span data-ttu-id="20efa-453">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-453">Description</span></span>                        |
|------------|------------------------------------|
| <span data-ttu-id="20efa-454">formName</span><span class="sxs-lookup"><span data-stu-id="20efa-454">formName</span></span>   | <span data-ttu-id="20efa-455">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-455">The name of the form.</span></span>              |
| <span data-ttu-id="20efa-456">dataSource</span><span class="sxs-lookup"><span data-stu-id="20efa-456">dataSource</span></span> | <span data-ttu-id="20efa-457">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="20efa-457">The data source of the form.</span></span>       |
| <span data-ttu-id="20efa-458">dataField</span><span class="sxs-lookup"><span data-stu-id="20efa-458">dataField</span></span>  | <span data-ttu-id="20efa-459">データ ソースのデータ フィールド。</span><span class="sxs-lookup"><span data-stu-id="20efa-459">The data field of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-460">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-460">Return Value</span></span>

<span data-ttu-id="20efa-461">フォームのデータ フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-461">The name of a data field in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-462">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-462">Remarks</span></span>

<span data-ttu-id="20efa-463">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-463">This is a compile-time function.</span></span> <span data-ttu-id="20efa-464">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-464">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-465">例</span><span class="sxs-lookup"><span data-stu-id="20efa-465">Example</span></span>

    str a = formDataFieldStr(FMVehicle, FMModelRate, RatePerDay);

## <a name="formdatasourcestr"></a><span data-ttu-id="20efa-466">formDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="20efa-466">formDataSourceStr</span></span>
<span data-ttu-id="20efa-467">フォームのデータ ソースの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-467">Returns the name of a data source in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-468">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-468">Syntax</span></span>

    str formDataSourceStr(str formName, str dataSource)

### <a name="parameters"></a><span data-ttu-id="20efa-469">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-469">Parameters</span></span>

| <span data-ttu-id="20efa-470">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-470">Parameter</span></span>  | <span data-ttu-id="20efa-471">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-471">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="20efa-472">formName</span><span class="sxs-lookup"><span data-stu-id="20efa-472">formName</span></span>   | <span data-ttu-id="20efa-473">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-473">The name of the form.</span></span>        |
| <span data-ttu-id="20efa-474">dataSource</span><span class="sxs-lookup"><span data-stu-id="20efa-474">dataSource</span></span> | <span data-ttu-id="20efa-475">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="20efa-475">The data source of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-476">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-476">Return Value</span></span>

<span data-ttu-id="20efa-477">フォームのデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-477">The name of a data source in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-478">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-478">Remarks</span></span>

<span data-ttu-id="20efa-479">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-479">This is a compile-time function.</span></span> <span data-ttu-id="20efa-480">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-480">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-481">例</span><span class="sxs-lookup"><span data-stu-id="20efa-481">Example</span></span>

    str b = formDataSourceStr(FMVehicle, FMModelRate);

## <a name="formmethodstr"></a><span data-ttu-id="20efa-482">formMethodStr</span><span class="sxs-lookup"><span data-stu-id="20efa-482">formMethodStr</span></span>
<span data-ttu-id="20efa-483">フォームのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-483">Returns the name of a method of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-484">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-484">Syntax</span></span>

    str formMethodStr(str formName, str methodName)

### <a name="parameters"></a><span data-ttu-id="20efa-485">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-485">Parameters</span></span>

| <span data-ttu-id="20efa-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-486">Parameter</span></span>  | <span data-ttu-id="20efa-487">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-487">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="20efa-488">formName</span><span class="sxs-lookup"><span data-stu-id="20efa-488">formName</span></span>   | <span data-ttu-id="20efa-489">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-489">The name of the form.</span></span>   |
| <span data-ttu-id="20efa-490">methodName</span><span class="sxs-lookup"><span data-stu-id="20efa-490">methodName</span></span> | <span data-ttu-id="20efa-491">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="20efa-491">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-492">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-492">Return Value</span></span>

<span data-ttu-id="20efa-493">フォームのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-493">The name of a method in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-494">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-494">Remarks</span></span>

<span data-ttu-id="20efa-495">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-495">This is a compile-time function.</span></span> <span data-ttu-id="20efa-496">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-496">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-497">例</span><span class="sxs-lookup"><span data-stu-id="20efa-497">Example</span></span>

<span data-ttu-id="20efa-498">次の例では、**showDialog** メソッドの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="20efa-498">The following example prints the name of the **showDialog** method.</span></span>

    str c = formMethodStr(Batch,showDialog);

## <a name="formstr"></a><span data-ttu-id="20efa-499">formStr</span><span class="sxs-lookup"><span data-stu-id="20efa-499">formStr</span></span>
<span data-ttu-id="20efa-500">フォームの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-500">Retrieves the name of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-501">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-501">Syntax</span></span>

    str formStr(str form)

### <a name="parameters"></a><span data-ttu-id="20efa-502">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-502">Parameters</span></span>

| <span data-ttu-id="20efa-503">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-503">Parameter</span></span> | <span data-ttu-id="20efa-504">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-504">Description</span></span>         |
|-----------|---------------------|
| <span data-ttu-id="20efa-505">フォーム</span><span class="sxs-lookup"><span data-stu-id="20efa-505">form</span></span>      | <span data-ttu-id="20efa-506">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-506">The name of a form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-507">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-507">Return Value</span></span>

<span data-ttu-id="20efa-508">フォームの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-508">A string that represents the name of the form.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-509">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-509">Remarks</span></span>

<span data-ttu-id="20efa-510">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-510">This is a compile-time function.</span></span> <span data-ttu-id="20efa-511">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-511">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-512">例</span><span class="sxs-lookup"><span data-stu-id="20efa-512">Example</span></span>

<span data-ttu-id="20efa-513">次の例では、InventDim フォームの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="20efa-513">The following example prints the name of the InventDim form.</span></span>

    static void formStrExample(Args _arg)
    {
        ;

        Global::info(formStr(InventDim));
    }
    /****Infolog Display
    Message (11:04:39 am)
    InventDim
    ****/

## <a name="identifierstr"></a><span data-ttu-id="20efa-514">identifierStr</span><span class="sxs-lookup"><span data-stu-id="20efa-514">identifierStr</span></span>
<span data-ttu-id="20efa-515">指定された識別子を文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="20efa-515">Converts the specified identifier to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-516">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-516">Syntax</span></span>

    str identifierStr(str ident)

### <a name="parameters"></a><span data-ttu-id="20efa-517">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-517">Parameters</span></span>

| <span data-ttu-id="20efa-518">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-518">Parameter</span></span> | <span data-ttu-id="20efa-519">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-519">Description</span></span>                |
|-----------|----------------------------|
| <span data-ttu-id="20efa-520">ident</span><span class="sxs-lookup"><span data-stu-id="20efa-520">ident</span></span>     | <span data-ttu-id="20efa-521">変換する ID。</span><span class="sxs-lookup"><span data-stu-id="20efa-521">The identifier to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-522">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-522">Return Value</span></span>

<span data-ttu-id="20efa-523">指定した ID を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-523">A string that represents the specified identifier.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-524">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-524">Remarks</span></span>

<span data-ttu-id="20efa-525">**identifierStr** 関数使用する場合、ベスト プラクティス警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="20efa-525">You will receive a best practice warning if you use the **identifierStr** function.</span></span> <span data-ttu-id="20efa-526">これは、**identifierStr** に対して存在チェックが実行されたために発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-526">This occurs because existence checking is performed for **identifierStr**.</span></span> <span data-ttu-id="20efa-527">使用可能な場合は、より具体的なコンパイル時の関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-527">Try to use a more specific compile-time function if one is available.</span></span> <span data-ttu-id="20efa-528">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-528">This is a compile-time function.</span></span> <span data-ttu-id="20efa-529">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-529">For more information, [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-530">例</span><span class="sxs-lookup"><span data-stu-id="20efa-530">Example</span></span>

<span data-ttu-id="20efa-531">次のコード例では、*myvar* 変数名を *thevar* 変数に割り当てています。</span><span class="sxs-lookup"><span data-stu-id="20efa-531">The following code example assigns the *myvar* variable name to the *thevar* variable.</span></span>

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

## <a name="indexnum"></a><span data-ttu-id="20efa-532">indexNum</span><span class="sxs-lookup"><span data-stu-id="20efa-532">indexNum</span></span>
<span data-ttu-id="20efa-533">指定されたインデックスを数字に変換します。</span><span class="sxs-lookup"><span data-stu-id="20efa-533">Converts the specified index to a number.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-534">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-534">Syntax</span></span>

    int indexNum(str tableid, str indexid)

### <a name="parameters"></a><span data-ttu-id="20efa-535">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-535">Parameters</span></span>

| <span data-ttu-id="20efa-536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-536">Parameter</span></span> | <span data-ttu-id="20efa-537">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-537">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="20efa-538">tableid</span><span class="sxs-lookup"><span data-stu-id="20efa-538">tableid</span></span>   | <span data-ttu-id="20efa-539">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="20efa-539">The table that contains the index.</span></span> |
| <span data-ttu-id="20efa-540">indexid</span><span class="sxs-lookup"><span data-stu-id="20efa-540">indexid</span></span>   | <span data-ttu-id="20efa-541">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="20efa-541">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="20efa-542">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-542">Return Value</span></span>

<span data-ttu-id="20efa-543">指定されたインデックスを表すインデックス番号。</span><span class="sxs-lookup"><span data-stu-id="20efa-543">The index number that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-544">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-544">Remarks</span></span>

<span data-ttu-id="20efa-545">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-545">This is a compile-time function.</span></span> <span data-ttu-id="20efa-546">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-546">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-547">例</span><span class="sxs-lookup"><span data-stu-id="20efa-547">Example</span></span>

<span data-ttu-id="20efa-548">次の例では、当事者インデックスのインデックス値を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-548">The following example returns the index value of the Party index.</span></span>

    static void indexNumExample(Args _arg)
    {
        ;

        Global::info(strfmt("%1 is the index number of Party.", indexNum(CustTable, Party)));
    }
    /****Infolog Display
    Message (11:28:03 am)
    3 is the index number of Party.
    ****/

## <a name="indexstr"></a><span data-ttu-id="20efa-549">indexStr</span><span class="sxs-lookup"><span data-stu-id="20efa-549">indexStr</span></span>
<span data-ttu-id="20efa-550">指定されたインデックスを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="20efa-550">Converts the specified index to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-551">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-551">Syntax</span></span>

    str indexStr(str tableid, str indexid)

### <a name="parameters"></a><span data-ttu-id="20efa-552">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-552">Parameters</span></span>

| <span data-ttu-id="20efa-553">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-553">Parameter</span></span> | <span data-ttu-id="20efa-554">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-554">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="20efa-555">tableid</span><span class="sxs-lookup"><span data-stu-id="20efa-555">tableid</span></span>   | <span data-ttu-id="20efa-556">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="20efa-556">The table that contains the index.</span></span> |
| <span data-ttu-id="20efa-557">indexid</span><span class="sxs-lookup"><span data-stu-id="20efa-557">indexid</span></span>   | <span data-ttu-id="20efa-558">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="20efa-558">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="20efa-559">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-559">Return Value</span></span>

<span data-ttu-id="20efa-560">指定インデックスを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-560">A string that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-561">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-561">Remarks</span></span>

<span data-ttu-id="20efa-562">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-562">This is a compile-time function.</span></span> <span data-ttu-id="20efa-563">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-563">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-564">例</span><span class="sxs-lookup"><span data-stu-id="20efa-564">Example</span></span>

<span data-ttu-id="20efa-565">次の例では、**CashDisc** インデックス値を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="20efa-565">The following example assigns the **CashDisc** index value to the *myText* variable.</span></span>

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

## <a name="licensecodenum"></a><span data-ttu-id="20efa-566">licenseCodeNum</span><span class="sxs-lookup"><span data-stu-id="20efa-566">licenseCodeNum</span></span>
<span data-ttu-id="20efa-567">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-567">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-568">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-568">Syntax</span></span>

    int licenseCodeNum(str codename)

### <a name="parameters"></a><span data-ttu-id="20efa-569">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-569">Parameters</span></span>

| <span data-ttu-id="20efa-570">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-570">Parameter</span></span> | <span data-ttu-id="20efa-571">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-571">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="20efa-572">codename</span><span class="sxs-lookup"><span data-stu-id="20efa-572">codename</span></span>  | <span data-ttu-id="20efa-573">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-573">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-574">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-574">Return Value</span></span>

<span data-ttu-id="20efa-575">指定されたライセンス コードの数。</span><span class="sxs-lookup"><span data-stu-id="20efa-575">The number of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-576">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-576">Remarks</span></span>

<span data-ttu-id="20efa-577">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-577">This is a compile-time function.</span></span> <span data-ttu-id="20efa-578">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-578">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-579">例</span><span class="sxs-lookup"><span data-stu-id="20efa-579">Example</span></span>

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

## <a name="licensecodestr"></a><span data-ttu-id="20efa-580">licenseCodeStr</span><span class="sxs-lookup"><span data-stu-id="20efa-580">licenseCodeStr</span></span>
<span data-ttu-id="20efa-581">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-581">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-582">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-582">Syntax</span></span>

    str licenseCodeStr(str codename)

### <a name="parameters"></a><span data-ttu-id="20efa-583">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-583">Parameters</span></span>

| <span data-ttu-id="20efa-584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-584">Parameter</span></span> | <span data-ttu-id="20efa-585">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-585">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="20efa-586">codename</span><span class="sxs-lookup"><span data-stu-id="20efa-586">codename</span></span>  | <span data-ttu-id="20efa-587">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-587">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-588">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-588">Return Value</span></span>

<span data-ttu-id="20efa-589">指定されたライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-589">The name of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-590">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-590">Remarks</span></span>

<span data-ttu-id="20efa-591">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-591">This is a compile-time function.</span></span> <span data-ttu-id="20efa-592">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-592">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-593">例</span><span class="sxs-lookup"><span data-stu-id="20efa-593">Example</span></span>

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

## <a name="literalstr"></a><span data-ttu-id="20efa-594">literalStr</span><span class="sxs-lookup"><span data-stu-id="20efa-594">literalStr</span></span>
<span data-ttu-id="20efa-595">指定した文字列がリテラル文字列であることを検証します。そうでない場合は、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-595">Validates that the specified string can be a literal string; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-596">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-596">Syntax</span></span>

    str literalStr(int str)

### <a name="parameters"></a><span data-ttu-id="20efa-597">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-597">Parameters</span></span>

| <span data-ttu-id="20efa-598">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-598">Parameter</span></span> | <span data-ttu-id="20efa-599">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-599">Description</span></span>             |
|-----------|-------------------------|
| <span data-ttu-id="20efa-600">codename</span><span class="sxs-lookup"><span data-stu-id="20efa-600">codename</span></span>  | <span data-ttu-id="20efa-601">検証する文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-601">The string to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-602">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-602">Return Value</span></span>

<span data-ttu-id="20efa-603">有効な場合は、リテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-603">The literal string if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-604">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-604">Remarks</span></span>

<span data-ttu-id="20efa-605">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-605">This is a compile-time function.</span></span> <span data-ttu-id="20efa-606">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-606">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-607">例</span><span class="sxs-lookup"><span data-stu-id="20efa-607">Example</span></span>

    {
        str s;
        ;

        s = literalStr("This is a literal str");
        print s;
        pause;
    }

## <a name="maxdate"></a><span data-ttu-id="20efa-608">maxDate</span><span class="sxs-lookup"><span data-stu-id="20efa-608">maxDate</span></span>
<span data-ttu-id="20efa-609">日付型の変数に使用できる最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-609">Retrieves the maximum value allowed for a variable of type date.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-610">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-610">Syntax</span></span>

    date maxDate()

### <a name="return-value"></a><span data-ttu-id="20efa-611">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-611">Return Value</span></span>

<span data-ttu-id="20efa-612">**日付** の変数に使用できる最大値は、**2154-12-31**です。</span><span class="sxs-lookup"><span data-stu-id="20efa-612">The maximum value allowed for a variable of type **date**, which is **2154-12-31**.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-613">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-613">Remarks</span></span>

<span data-ttu-id="20efa-614">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-614">This is a compile-time function.</span></span> <span data-ttu-id="20efa-615">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-615">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-616">例</span><span class="sxs-lookup"><span data-stu-id="20efa-616">Example</span></span>

    static void maxDateExample(Args _arg)
    {
        date maximumDate;
        ;
        maximumDate = maxDate();
        print maximumDate;
        pause;
    }

## <a name="maxint"></a><span data-ttu-id="20efa-617">maxInt</span><span class="sxs-lookup"><span data-stu-id="20efa-617">maxInt</span></span>
<span data-ttu-id="20efa-618">**int** 型に格納可能な最大符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-618">Retrieves the maximum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-619">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-619">Syntax</span></span>

    int maxInt()

### <a name="return-value"></a><span data-ttu-id="20efa-620">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-620">Return Value</span></span>

<span data-ttu-id="20efa-621">整数の許容値の最大値。</span><span class="sxs-lookup"><span data-stu-id="20efa-621">The maximum value allowed value of an integer.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-622">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-622">Remarks</span></span>

<span data-ttu-id="20efa-623">その他の整数値は、戻り値以下になります。</span><span class="sxs-lookup"><span data-stu-id="20efa-623">Any other integer will be less than or equal to the returned value.</span></span> <span data-ttu-id="20efa-624">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-624">This is a compile-time function.</span></span> <span data-ttu-id="20efa-625">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-625">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-626">例</span><span class="sxs-lookup"><span data-stu-id="20efa-626">Example</span></span>

    static void maxIntExample(Args _arg)
    {
        int i;
        ;
        print "The maximum value for type int is " + int2Str(maxInt());
        pause;
    }

## <a name="measurementstr"></a><span data-ttu-id="20efa-627">measurementStr</span><span class="sxs-lookup"><span data-stu-id="20efa-627">measurementStr</span></span>
<span data-ttu-id="20efa-628">測定の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-628">Returns the name of a measurement.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-629">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-629">Syntax</span></span>

    str measurementStr(str measurement)

### <a name="parameters"></a><span data-ttu-id="20efa-630">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-630">Parameters</span></span>

| <span data-ttu-id="20efa-631">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-631">Parameter</span></span>   | <span data-ttu-id="20efa-632">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-632">Description</span></span>                  |
|-------------|------------------------------|
| <span data-ttu-id="20efa-633">測定値</span><span class="sxs-lookup"><span data-stu-id="20efa-633">measurement</span></span> | <span data-ttu-id="20efa-634">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-634">The name of the measurement.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-635">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-635">Return Value</span></span>

<span data-ttu-id="20efa-636">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-636">The name of the measurement.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-637">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-637">Remarks</span></span>

<span data-ttu-id="20efa-638">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-638">This is a compile-time function.</span></span> <span data-ttu-id="20efa-639">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-639">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-640">例</span><span class="sxs-lookup"><span data-stu-id="20efa-640">Example</span></span>

    No example.

## <a name="measurestr"></a><span data-ttu-id="20efa-641">measureStr</span><span class="sxs-lookup"><span data-stu-id="20efa-641">measureStr</span></span>
<span data-ttu-id="20efa-642">メジャーの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-642">Returns the name of a measure.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-643">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-643">Syntax</span></span>

    str measureStr(str measure)

### <a name="parameters"></a><span data-ttu-id="20efa-644">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-644">Parameters</span></span>

| <span data-ttu-id="20efa-645">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-645">Parameter</span></span> | <span data-ttu-id="20efa-646">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-646">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="20efa-647">測定</span><span class="sxs-lookup"><span data-stu-id="20efa-647">measure</span></span>   | <span data-ttu-id="20efa-648">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-648">The name of the measure.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-649">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-649">Return Value</span></span>

<span data-ttu-id="20efa-650">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-650">The name of the measure.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-651">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-651">Remarks</span></span>

<span data-ttu-id="20efa-652">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-652">This is a compile-time function.</span></span> <span data-ttu-id="20efa-653">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-653">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-654">例</span><span class="sxs-lookup"><span data-stu-id="20efa-654">Example</span></span>

    No example.

## <a name="menuitemactionstr"></a><span data-ttu-id="20efa-655">menuItemActionStr</span><span class="sxs-lookup"><span data-stu-id="20efa-655">menuItemActionStr</span></span>
<span data-ttu-id="20efa-656">指定したメニュー項目のアクションがアプリケーション オブジェクト ツリー (Application Explorer) に存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-656">Validates that the specified menu item action exists in the Application Object Tree (Application Explorer); if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-657">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-657">Syntax</span></span>

    str menuItemActionStr(class menuitem)

### <a name="parameters"></a><span data-ttu-id="20efa-658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-658">Parameters</span></span>

| <span data-ttu-id="20efa-659">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-659">Parameter</span></span> | <span data-ttu-id="20efa-660">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-660">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="20efa-661">codename</span><span class="sxs-lookup"><span data-stu-id="20efa-661">codename</span></span>  | <span data-ttu-id="20efa-662">検証するメニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-662">The name of the menu item action to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-663">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-663">Return Value</span></span>

<span data-ttu-id="20efa-664">有効な場合の、メニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-664">The name of the menu item action, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-665">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-665">Remarks</span></span>

<span data-ttu-id="20efa-666">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-666">This is a compile-time function.</span></span> <span data-ttu-id="20efa-667">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-667">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-668">例</span><span class="sxs-lookup"><span data-stu-id="20efa-668">Example</span></span>

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

## <a name="menuitemdisplaystr"></a><span data-ttu-id="20efa-669">menuItemDisplayStr</span><span class="sxs-lookup"><span data-stu-id="20efa-669">menuItemDisplayStr</span></span>
<span data-ttu-id="20efa-670">指定したメニュー項目の表示がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-670">Validates that the specified menu item display exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-671">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-671">Syntax</span></span>

    str menuitemdisplaystr(class menuItem)

### <a name="parameters"></a><span data-ttu-id="20efa-672">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-672">Parameters</span></span>

| <span data-ttu-id="20efa-673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-673">Parameter</span></span> | <span data-ttu-id="20efa-674">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-674">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="20efa-675">codename</span><span class="sxs-lookup"><span data-stu-id="20efa-675">codename</span></span>  | <span data-ttu-id="20efa-676">検証するメニュー項目nの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-676">The name of the menu item display to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-677">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-677">Return Value</span></span>

<span data-ttu-id="20efa-678">有効な場合の、指定されたメニューの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-678">The name of the specified menu item display, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-679">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-679">Remarks</span></span>

<span data-ttu-id="20efa-680">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-680">This is a compile-time function.</span></span> <span data-ttu-id="20efa-681">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-681">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-682">例</span><span class="sxs-lookup"><span data-stu-id="20efa-682">Example</span></span>

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

## <a name="menuitemoutputstr"></a><span data-ttu-id="20efa-683">menuItemOutputStr</span><span class="sxs-lookup"><span data-stu-id="20efa-683">menuItemOutputStr</span></span>
<span data-ttu-id="20efa-684">指定したメニュー項目の出力がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-684">Validates that the specified menu item output exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-685">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-685">Syntax</span></span>

    str menuItemOutputStr(class menuitem)

### <a name="parameters"></a><span data-ttu-id="20efa-686">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-686">Parameters</span></span>

| <span data-ttu-id="20efa-687">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-687">Parameter</span></span> | <span data-ttu-id="20efa-688">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-688">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="20efa-689">codename</span><span class="sxs-lookup"><span data-stu-id="20efa-689">codename</span></span>  | <span data-ttu-id="20efa-690">検証するメニュー項目出力の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-690">The name of the menu item output to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-691">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-691">Return Value</span></span>

<span data-ttu-id="20efa-692">有効な場合、指定されたメニュー項目が出力されます。</span><span class="sxs-lookup"><span data-stu-id="20efa-692">The specified menu item output if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-693">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-693">Remarks</span></span>

<span data-ttu-id="20efa-694">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-694">This is a compile-time function.</span></span> <span data-ttu-id="20efa-695">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-695">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-696">例</span><span class="sxs-lookup"><span data-stu-id="20efa-696">Example</span></span>

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

## <a name="menustr"></a><span data-ttu-id="20efa-697">menuStr</span><span class="sxs-lookup"><span data-stu-id="20efa-697">menuStr</span></span>
<span data-ttu-id="20efa-698">指定したメニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-698">Validates that the specified menu exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-699">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-699">Syntax</span></span>

    str menuStr(class menu)

### <a name="parameters"></a><span data-ttu-id="20efa-700">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-700">Parameters</span></span>

| <span data-ttu-id="20efa-701">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-701">Parameter</span></span> | <span data-ttu-id="20efa-702">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-702">Description</span></span>                       |
|-----------|-----------------------------------|
| <span data-ttu-id="20efa-703">メニュー</span><span class="sxs-lookup"><span data-stu-id="20efa-703">menu</span></span>      | <span data-ttu-id="20efa-704">検証するメニューの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-704">The name of the menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-705">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-705">Return Value</span></span>

<span data-ttu-id="20efa-706">有効な場合の指定されたメニュー項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-706">The name of the specified menu item if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-707">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-707">Remarks</span></span>

<span data-ttu-id="20efa-708">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-708">This is a compile-time function.</span></span> <span data-ttu-id="20efa-709">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-709">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-710">例</span><span class="sxs-lookup"><span data-stu-id="20efa-710">Example</span></span>

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

## <a name="methodstr"></a><span data-ttu-id="20efa-711">methodStr</span><span class="sxs-lookup"><span data-stu-id="20efa-711">methodStr</span></span>
<span data-ttu-id="20efa-712">指定したメソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-712">Validates that the specified method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-713">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-713">Syntax</span></span>

    str methodStr(class class, int method)

### <a name="parameters"></a><span data-ttu-id="20efa-714">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-714">Parameters</span></span>

| <span data-ttu-id="20efa-715">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-715">Parameter</span></span> | <span data-ttu-id="20efa-716">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-716">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="20efa-717">クラス</span><span class="sxs-lookup"><span data-stu-id="20efa-717">class</span></span>     | <span data-ttu-id="20efa-718">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-718">The name of the class.</span></span>              |
| <span data-ttu-id="20efa-719">メソッド</span><span class="sxs-lookup"><span data-stu-id="20efa-719">method</span></span>    | <span data-ttu-id="20efa-720">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-720">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-721">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-721">Return Value</span></span>

<span data-ttu-id="20efa-722">有効な場合の、指定されたメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-722">The name of the specified method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-723">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-723">Remarks</span></span>

<span data-ttu-id="20efa-724">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-724">This is a compile-time function.</span></span> <span data-ttu-id="20efa-725">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-725">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-726">例</span><span class="sxs-lookup"><span data-stu-id="20efa-726">Example</span></span>

    {
        #define.timeout(50)
        str s;
        SysHelpInitTimeOut SysHelpInitTimeOut;
        ;

        s = methodStr(SysHelpInitTimeOut, timeout);
        print s;
        pause;
    }

## <a name="minint"></a><span data-ttu-id="20efa-727">minInt</span><span class="sxs-lookup"><span data-stu-id="20efa-727">minInt</span></span>
<span data-ttu-id="20efa-728">**int** 型に格納可能な最小符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-728">Retrieves the minimum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-729">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-729">Syntax</span></span>

    int minInt()

### <a name="return-value"></a><span data-ttu-id="20efa-730">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-730">Return Value</span></span>

<span data-ttu-id="20efa-731">**int** 型の最小値です。</span><span class="sxs-lookup"><span data-stu-id="20efa-731">The minimum value of an **int** type.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-732">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-732">Remarks</span></span>

<span data-ttu-id="20efa-733">その他の整数値は、戻り値以上になります。</span><span class="sxs-lookup"><span data-stu-id="20efa-733">Any other integer value will be greater than or equal to the returned value.</span></span> <span data-ttu-id="20efa-734">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-734">This is a compile-time function.</span></span> <span data-ttu-id="20efa-735">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-735">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-736">例</span><span class="sxs-lookup"><span data-stu-id="20efa-736">Example</span></span>

    static void minIntExample(Args _arg)
    {
        int i;
        ;
        i = minInt();
        print "minInt() is " + int2Str(i);    
        pause;
    }

## <a name="privilegestr"></a><span data-ttu-id="20efa-737">privilegeStr</span><span class="sxs-lookup"><span data-stu-id="20efa-737">privilegeStr</span></span>
<span data-ttu-id="20efa-738">権限の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-738">Returns the name of the privilege.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-739">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-739">Syntax</span></span>

    str privilegeStr(str privilege)

### <a name="parameters"></a><span data-ttu-id="20efa-740">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-740">Parameters</span></span>

| <span data-ttu-id="20efa-741">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-741">Parameter</span></span> | <span data-ttu-id="20efa-742">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-742">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="20efa-743">権限</span><span class="sxs-lookup"><span data-stu-id="20efa-743">privilege</span></span> | <span data-ttu-id="20efa-744">名前を返す対象の特権。</span><span class="sxs-lookup"><span data-stu-id="20efa-744">The privilege for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-745">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-745">Return Value</span></span>

<span data-ttu-id="20efa-746">権限の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-746">The name of the privilege.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-747">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-747">Remarks</span></span>

<span data-ttu-id="20efa-748">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-748">This is a compile-time function.</span></span> <span data-ttu-id="20efa-749">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-749">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-750">例</span><span class="sxs-lookup"><span data-stu-id="20efa-750">Example</span></span>

    No example.

## <a name="querydatasourcestr"></a><span data-ttu-id="20efa-751">queryDatasourceStr</span><span class="sxs-lookup"><span data-stu-id="20efa-751">queryDatasourceStr</span></span>
<span data-ttu-id="20efa-752">X++ コンパイラは、データ ソースがクエリに存在するかどうかをチェックし、関数呼び出しを有効なデータ ソース名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="20efa-752">Causes the X++ compiler to check whether the data source exists on the query, and to replace the function call with a string of the valid data source name.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-753">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-753">Syntax</span></span>

    str queryDataSourceStr(queryName, dataSourceName)

### <a name="parameters"></a><span data-ttu-id="20efa-754">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-754">Parameters</span></span>

| <span data-ttu-id="20efa-755">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-755">Parameter</span></span>      | <span data-ttu-id="20efa-756">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-756">Description</span></span>                                                               |
|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="20efa-757">queryName</span><span class="sxs-lookup"><span data-stu-id="20efa-757">queryName</span></span>      | <span data-ttu-id="20efa-758">引用符ではなく、クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-758">The name of the query, not in quotation marks.</span></span>                            |
| <span data-ttu-id="20efa-759">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="20efa-759">dataSourceName</span></span> | <span data-ttu-id="20efa-760">クエリ上のデータ ソースの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="20efa-760">The name of the data source that is on the query, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-761">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-761">Return Value</span></span>

<span data-ttu-id="20efa-762">アプリケーション エクスプローラーで表示されるデータ ソースの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-762">A string that contains the name of the data source as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-763">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-763">Remarks</span></span>

<span data-ttu-id="20efa-764">データ ソースがクエリに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20efa-764">A compile error is issued if the compiler determines that the data source does not exist on the query.</span></span> <span data-ttu-id="20efa-765">X++ コードが引用符が含まれる文字列を使用してデータ ソースの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="20efa-765">If your X++ code uses a string that contains quotation marks to supply the data source name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="20efa-766">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="20efa-766">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="20efa-767">コンパイラにより実行される **queryDataSourceStr** などの X++ 関数は、コンパイル時関数とみなされます。</span><span class="sxs-lookup"><span data-stu-id="20efa-767">X++ functions such as **queryDataSourceStr** that are executed by the compiler are referred to as compile-time functions or compile-time functions.</span></span> <span data-ttu-id="20efa-768">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="20efa-768">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="20efa-769">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="20efa-769">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="20efa-770">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-770">This is a compile-time function.</span></span> <span data-ttu-id="20efa-771">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-771">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-772">例</span><span class="sxs-lookup"><span data-stu-id="20efa-772">Example</span></span>

    No example.

## <a name="querymethodstr"></a><span data-ttu-id="20efa-773">queryMethodStr</span><span class="sxs-lookup"><span data-stu-id="20efa-773">queryMethodStr</span></span>
<span data-ttu-id="20efa-774">クエリのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-774">Returns the name of a method of a query.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-775">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-775">Syntax</span></span>

    str queryMethodStr(str queryName, str methodName)

### <a name="parameters"></a><span data-ttu-id="20efa-776">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-776">Parameters</span></span>

| <span data-ttu-id="20efa-777">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-777">Parameter</span></span>  | <span data-ttu-id="20efa-778">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-778">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="20efa-779">queryName</span><span class="sxs-lookup"><span data-stu-id="20efa-779">queryName</span></span>  | <span data-ttu-id="20efa-780">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-780">The name of the query.</span></span>  |
| <span data-ttu-id="20efa-781">methodName</span><span class="sxs-lookup"><span data-stu-id="20efa-781">methodName</span></span> | <span data-ttu-id="20efa-782">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="20efa-782">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-783">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-783">Return Value</span></span>

<span data-ttu-id="20efa-784">クエリのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-784">The name of a method in a query.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-785">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-785">Remarks</span></span>

<span data-ttu-id="20efa-786">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-786">This is a compile-time function.</span></span> <span data-ttu-id="20efa-787">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-787">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-788">例</span><span class="sxs-lookup"><span data-stu-id="20efa-788">Example</span></span>

    No example.

## <a name="querystr"></a><span data-ttu-id="20efa-789">queryStr</span><span class="sxs-lookup"><span data-stu-id="20efa-789">queryStr</span></span>
<span data-ttu-id="20efa-790">既存のクエリを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-790">Retrieves a string that represents an existing query.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-791">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-791">Syntax</span></span>

    str queryStr(str query)

### <a name="parameters"></a><span data-ttu-id="20efa-792">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-792">Parameters</span></span>

| <span data-ttu-id="20efa-793">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-793">Parameter</span></span> | <span data-ttu-id="20efa-794">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-794">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="20efa-795">クエリ</span><span class="sxs-lookup"><span data-stu-id="20efa-795">query</span></span>     | <span data-ttu-id="20efa-796">取得するクエリ。</span><span class="sxs-lookup"><span data-stu-id="20efa-796">The query to retrieve.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-797">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-797">Return Value</span></span>

<span data-ttu-id="20efa-798">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-798">The name of the query.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-799">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-799">Remarks</span></span>

<span data-ttu-id="20efa-800">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-800">This is a compile-time function.</span></span> <span data-ttu-id="20efa-801">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-801">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-802">例</span><span class="sxs-lookup"><span data-stu-id="20efa-802">Example</span></span>

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

## <a name="reportstr"></a><span data-ttu-id="20efa-803">reportStr</span><span class="sxs-lookup"><span data-stu-id="20efa-803">reportStr</span></span>
<span data-ttu-id="20efa-804">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-804">Retrieves a string that represents the name of the specified report.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-805">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-805">Syntax</span></span>

    str reportStr(str report)

### <a name="parameters"></a><span data-ttu-id="20efa-806">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-806">Parameters</span></span>

| <span data-ttu-id="20efa-807">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-807">Parameter</span></span> | <span data-ttu-id="20efa-808">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-808">Description</span></span>                              |
|-----------|------------------------------------------|
| <span data-ttu-id="20efa-809">レポート</span><span class="sxs-lookup"><span data-stu-id="20efa-809">report</span></span>    | <span data-ttu-id="20efa-810">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="20efa-810">The report for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-811">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-811">Return Value</span></span>

<span data-ttu-id="20efa-812">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-812">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-813">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-813">Remarks</span></span>

<span data-ttu-id="20efa-814">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-814">This is a compile-time function.</span></span> <span data-ttu-id="20efa-815">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-815">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-816">例</span><span class="sxs-lookup"><span data-stu-id="20efa-816">Example</span></span>

<span data-ttu-id="20efa-817">次の例では、**AssetAddition** レポートの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="20efa-817">The following example assigns the name of the **AssetAddition** report to the *MyTxt* variable.</span></span>

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

## <a name="resourcestr"></a><span data-ttu-id="20efa-818">resourceStr</span><span class="sxs-lookup"><span data-stu-id="20efa-818">resourceStr</span></span>
<span data-ttu-id="20efa-819">指定したリソースがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-819">Validates that the specified resource exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-820">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-820">Syntax</span></span>

    str resourceStr(str resourcename)

### <a name="parameters"></a><span data-ttu-id="20efa-821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-821">Parameters</span></span>

| <span data-ttu-id="20efa-822">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-822">Parameter</span></span>    | <span data-ttu-id="20efa-823">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-823">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="20efa-824">resourcename</span><span class="sxs-lookup"><span data-stu-id="20efa-824">resourcename</span></span> | <span data-ttu-id="20efa-825">検証するリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-825">The name of the resource to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-826">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-826">Return Value</span></span>

<span data-ttu-id="20efa-827">有効な場合の、指定されたリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-827">The name of the specified resource, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-828">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-828">Remarks</span></span>

<span data-ttu-id="20efa-829">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-829">This is a compile-time function.</span></span> <span data-ttu-id="20efa-830">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-830">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-831">例</span><span class="sxs-lookup"><span data-stu-id="20efa-831">Example</span></span>

    {
        print "Str for resource StyleSheet_Help_Axapta is " 
            + resourceStr(StyleSheet_Help_Axapta);
        pause;
    }

## <a name="rolestr"></a><span data-ttu-id="20efa-832">roleStr</span><span class="sxs-lookup"><span data-stu-id="20efa-832">roleStr</span></span>
<span data-ttu-id="20efa-833">指定したセキュリティ ロールの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-833">Retrieves a string that represents the name of the specified security role.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-834">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-834">Syntax</span></span>

    str roleStr(str securityRole)

### <a name="parameters"></a><span data-ttu-id="20efa-835">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-835">Parameters</span></span>

| <span data-ttu-id="20efa-836">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-836">Parameter</span></span>    | <span data-ttu-id="20efa-837">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-837">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="20efa-838">securityRole</span><span class="sxs-lookup"><span data-stu-id="20efa-838">securityRole</span></span> | <span data-ttu-id="20efa-839">セキュリティ ロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="20efa-839">The name of the security role.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-840">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-840">Return Value</span></span>

<span data-ttu-id="20efa-841">文字列のセキュリティ ロールの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-841">The name of the security role in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-842">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-842">Remarks</span></span>

<span data-ttu-id="20efa-843">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-843">This is a compile-time function.</span></span> <span data-ttu-id="20efa-844">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-844">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-845">例</span><span class="sxs-lookup"><span data-stu-id="20efa-845">Example</span></span>

    No example.

## <a name="ssrsreportstr"></a><span data-ttu-id="20efa-846">ssrsReportStr</span><span class="sxs-lookup"><span data-stu-id="20efa-846">ssrsReportStr</span></span>
<span data-ttu-id="20efa-847">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-847">Retrieves a string that represents the name of the specified report.</span></span> <span data-ttu-id="20efa-848">レポート コントローラー クラスで実行されるレポートを指定する場合は、この関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="20efa-848">Use this function when you want to specify the report that should be run by a report controller class.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-849">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-849">Syntax</span></span>

    str ssrsReportStr(str report, str design)

### <a name="parameters"></a><span data-ttu-id="20efa-850">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-850">Parameters</span></span>

| <span data-ttu-id="20efa-851">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-851">Parameter</span></span> | <span data-ttu-id="20efa-852">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-852">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| <span data-ttu-id="20efa-853">レポート</span><span class="sxs-lookup"><span data-stu-id="20efa-853">report</span></span>    | <span data-ttu-id="20efa-854">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="20efa-854">The report to return the name for.</span></span>                         |
| <span data-ttu-id="20efa-855">design</span><span class="sxs-lookup"><span data-stu-id="20efa-855">design</span></span>    | <span data-ttu-id="20efa-856">レポートに関連付けられているデザインの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-856">The name of the design that is associated with the report.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-857">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-857">Return Value</span></span>

<span data-ttu-id="20efa-858">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-858">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-859">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-859">Remarks</span></span>

<span data-ttu-id="20efa-860">**ssrsReportStr** 関数は、有効なレポートに属しているかどうかを検証するために、渡された 2 つの値を解析します。</span><span class="sxs-lookup"><span data-stu-id="20efa-860">The **ssrsReportStr** function parses the two values that are passed to it, to validate whether they belong to a valid report.</span></span> <span data-ttu-id="20efa-861">コントローラーが、どのレポート デザインの組み合わせを呼び出す必要があるかを判断できるように、メニュー項目が controller() を指しているときは、レポート名を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20efa-861">The report name must be set when a menu item points to a controller(), so that the controller can determine which report-design combination must be invoked.</span></span> <span data-ttu-id="20efa-862">**ssrsReportStr** 関数を使用すると、レポートおよびデザイン名のコンパイル時の検証で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="20efa-862">Use of the **ssrsReportStr** function provides the benefit of compile-time validation for the report and design name.</span></span> <span data-ttu-id="20efa-863">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-863">This is a compile-time function.</span></span> <span data-ttu-id="20efa-864">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-864">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-865">例</span><span class="sxs-lookup"><span data-stu-id="20efa-865">Example</span></span>

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

## <a name="staticdelegatestr"></a><span data-ttu-id="20efa-866">staticDelegateStr</span><span class="sxs-lookup"><span data-stu-id="20efa-866">staticDelegateStr</span></span>
<span data-ttu-id="20efa-867">静的デリゲートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="20efa-867">Returns the name of a static delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-868">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-868">Syntax</span></span>

    str staticDelegateStr(str class, str delegate)

### <a name="parameters"></a><span data-ttu-id="20efa-869">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-869">Parameters</span></span>

| <span data-ttu-id="20efa-870">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-870">Parameter</span></span> | <span data-ttu-id="20efa-871">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-871">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="20efa-872">クラス</span><span class="sxs-lookup"><span data-stu-id="20efa-872">class</span></span>     | <span data-ttu-id="20efa-873">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-873">The name of a class, table, or form.</span></span> |
| <span data-ttu-id="20efa-874">デリゲート</span><span class="sxs-lookup"><span data-stu-id="20efa-874">delegate</span></span>  | <span data-ttu-id="20efa-875">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="20efa-875">The name of the delegate.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="20efa-876">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-876">Return Value</span></span>

<span data-ttu-id="20efa-877">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="20efa-877">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-878">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-878">Remarks</span></span>

<span data-ttu-id="20efa-879">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-879">This is a compile-time function.</span></span> <span data-ttu-id="20efa-880">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-880">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-881">例</span><span class="sxs-lookup"><span data-stu-id="20efa-881">Example</span></span>

    No example.

## <a name="staticmethodstr"></a><span data-ttu-id="20efa-882">staticMethodStr</span><span class="sxs-lookup"><span data-stu-id="20efa-882">staticMethodStr</span></span>
<span data-ttu-id="20efa-883">指定した静的メソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-883">Validates that the specified static method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-884">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-884">Syntax</span></span>

    str staticMethodStr(class class, int method)

### <a name="parameters"></a><span data-ttu-id="20efa-885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-885">Parameters</span></span>

| <span data-ttu-id="20efa-886">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-886">Parameter</span></span> | <span data-ttu-id="20efa-887">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-887">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="20efa-888">クラス</span><span class="sxs-lookup"><span data-stu-id="20efa-888">class</span></span>     | <span data-ttu-id="20efa-889">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-889">The name of the class.</span></span>                     |
| <span data-ttu-id="20efa-890">メソッド</span><span class="sxs-lookup"><span data-stu-id="20efa-890">method</span></span>    | <span data-ttu-id="20efa-891">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-891">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-892">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-892">Return Value</span></span>

<span data-ttu-id="20efa-893">有効な場合の、指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-893">The name of the static method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-894">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-894">Remarks</span></span>

<span data-ttu-id="20efa-895">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-895">This is a compile-time function.</span></span> <span data-ttu-id="20efa-896">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-896">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-897">例</span><span class="sxs-lookup"><span data-stu-id="20efa-897">Example</span></span>

    No example.

## <a name="tablecollectionstr"></a><span data-ttu-id="20efa-898">tableCollectionStr</span><span class="sxs-lookup"><span data-stu-id="20efa-898">tableCollectionStr</span></span>
<span data-ttu-id="20efa-899">指定したテーブル コレクションがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-899">Validates that the specified table collection exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-900">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-900">Syntax</span></span>

    str tableCollectionStr(class tablecollection)

### <a name="parameters"></a><span data-ttu-id="20efa-901">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-901">Parameters</span></span>

| <span data-ttu-id="20efa-902">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-902">Parameter</span></span>       | <span data-ttu-id="20efa-903">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-903">Description</span></span>                                   |
|-----------------|-----------------------------------------------|
| <span data-ttu-id="20efa-904">tablecollection</span><span class="sxs-lookup"><span data-stu-id="20efa-904">tablecollection</span></span> | <span data-ttu-id="20efa-905">検証するテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-905">The name of the table collection to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-906">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-906">Return Value</span></span>

<span data-ttu-id="20efa-907">有効な場合の、指定されたテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-907">The name of the specified table collection, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-908">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-908">Remarks</span></span>

<span data-ttu-id="20efa-909">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-909">This is a compile-time function.</span></span> <span data-ttu-id="20efa-910">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-910">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-911">例</span><span class="sxs-lookup"><span data-stu-id="20efa-911">Example</span></span>

    No example.

## <a name="tablefieldgroupstr"></a><span data-ttu-id="20efa-912">tableFieldGroupStr</span><span class="sxs-lookup"><span data-stu-id="20efa-912">tableFieldGroupStr</span></span>
<span data-ttu-id="20efa-913">文字列としてフィールド グループの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-913">Retrieves the name of a field group as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-914">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-914">Syntax</span></span>

    str tableFieldGroupStr(str tableName, str fieldGroupName)

### <a name="parameters"></a><span data-ttu-id="20efa-915">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-915">Parameters</span></span>

| <span data-ttu-id="20efa-916">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-916">Parameter</span></span>      | <span data-ttu-id="20efa-917">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-917">Description</span></span>                              |
|----------------|------------------------------------------|
| <span data-ttu-id="20efa-918">tableName</span><span class="sxs-lookup"><span data-stu-id="20efa-918">tableName</span></span>      | <span data-ttu-id="20efa-919">フィールド グループを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="20efa-919">The table that contains the field group.</span></span> |
| <span data-ttu-id="20efa-920">fieldGroupName</span><span class="sxs-lookup"><span data-stu-id="20efa-920">fieldGroupName</span></span> | <span data-ttu-id="20efa-921">テーブル内のフィールド グループ。</span><span class="sxs-lookup"><span data-stu-id="20efa-921">The field group in the table.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="20efa-922">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-922">Return Value</span></span>

<span data-ttu-id="20efa-923">文字列としてのフィールド グループの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-923">The name of the field group as a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-924">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-924">Remarks</span></span>

<span data-ttu-id="20efa-925">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-925">This is a compile-time function.</span></span> <span data-ttu-id="20efa-926">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-926">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-927">例</span><span class="sxs-lookup"><span data-stu-id="20efa-927">Example</span></span>

<span data-ttu-id="20efa-928">次の例では、**編集** フィールド グループの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-928">The following example retrieves the name of the **Editing** field group as a string.</span></span>

    static void tableFieldGroupStrExample(Args _arg)
    {
        ;

        Global::info(tableFieldGroupStr(AccountingDistribution, Editing));
    }
    /****Infolog Display
    Message (03:14:54 pm)
    Editing
    ****/

## <a name="tablemethodstr"></a><span data-ttu-id="20efa-929">tableMethodStr</span><span class="sxs-lookup"><span data-stu-id="20efa-929">tableMethodStr</span></span>
<span data-ttu-id="20efa-930">指定したメソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-930">Validates that the specified method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-931">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-931">Syntax</span></span>

    str tableMethodStr(int table, int method)

### <a name="parameters"></a><span data-ttu-id="20efa-932">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-932">Parameters</span></span>

| <span data-ttu-id="20efa-933">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-933">Parameter</span></span> | <span data-ttu-id="20efa-934">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-934">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="20efa-935">テーブル</span><span class="sxs-lookup"><span data-stu-id="20efa-935">table</span></span>     | <span data-ttu-id="20efa-936">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-936">The name of the table.</span></span>              |
| <span data-ttu-id="20efa-937">メソッド</span><span class="sxs-lookup"><span data-stu-id="20efa-937">method</span></span>    | <span data-ttu-id="20efa-938">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-938">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-939">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-939">Return Value</span></span>

<span data-ttu-id="20efa-940">有効な場合の、メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-940">The name of the method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-941">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-941">Remarks</span></span>

<span data-ttu-id="20efa-942">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-942">This is a compile-time function.</span></span> <span data-ttu-id="20efa-943">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-943">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-944">例</span><span class="sxs-lookup"><span data-stu-id="20efa-944">Example</span></span>

    No example.

## <a name="tablenum"></a><span data-ttu-id="20efa-945">tableNum</span><span class="sxs-lookup"><span data-stu-id="20efa-945">tableNum</span></span>
<span data-ttu-id="20efa-946">特定のテーブルのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-946">Retrieves the table ID of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-947">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-947">Syntax</span></span>

    int tableNum(str table)

### <a name="parameters"></a><span data-ttu-id="20efa-948">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-948">Parameters</span></span>

| <span data-ttu-id="20efa-949">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-949">Parameter</span></span> | <span data-ttu-id="20efa-950">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-950">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="20efa-951">テーブル</span><span class="sxs-lookup"><span data-stu-id="20efa-951">table</span></span>     | <span data-ttu-id="20efa-952">テーブル ID を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="20efa-952">The table to retrieve the table ID for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-953">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-953">Return Value</span></span>

<span data-ttu-id="20efa-954">特定のテーブルのテーブル ID</span><span class="sxs-lookup"><span data-stu-id="20efa-954">The table ID of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-955">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-955">Remarks</span></span>

<span data-ttu-id="20efa-956">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-956">This is a compile-time function.</span></span> <span data-ttu-id="20efa-957">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-957">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-958">例</span><span class="sxs-lookup"><span data-stu-id="20efa-958">Example</span></span>

<span data-ttu-id="20efa-959">次の例では、**tableID** 変数を 77 に設定します。これは、**CustTable** テーブルの **ID** です。</span><span class="sxs-lookup"><span data-stu-id="20efa-959">The following example sets the **tableID** variable to 77, which is the **ID** of the **CustTable** table.</span></span>

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

## <a name="tablepname"></a><span data-ttu-id="20efa-960">tablePName</span><span class="sxs-lookup"><span data-stu-id="20efa-960">tablePName</span></span>
<span data-ttu-id="20efa-961">指定されたテーブルの出力可能な名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-961">Retrieves a string that contains the printable name of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-962">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-962">Syntax</span></span>

    str tablePName(str table)

### <a name="parameters"></a><span data-ttu-id="20efa-963">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-963">Parameters</span></span>

| <span data-ttu-id="20efa-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-964">Parameter</span></span> | <span data-ttu-id="20efa-965">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-965">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="20efa-966">テーブル</span><span class="sxs-lookup"><span data-stu-id="20efa-966">table</span></span>     | <span data-ttu-id="20efa-967">印刷可能な名前を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="20efa-967">The table to retrieve the printable name for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-968">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-968">Return Value</span></span>

<span data-ttu-id="20efa-969">指定されたテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-969">The name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-970">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-970">Remarks</span></span>

<span data-ttu-id="20efa-971">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-971">This is a compile-time function.</span></span> <span data-ttu-id="20efa-972">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-972">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-973">例</span><span class="sxs-lookup"><span data-stu-id="20efa-973">Example</span></span>

<span data-ttu-id="20efa-974">次の例では、**CustTable** テーブルのラベルを *MyText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="20efa-974">The following example assigns the label of the **CustTable** table to the *MyText* variable.</span></span>

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

## <a name="tablestaticmethodstr"></a><span data-ttu-id="20efa-975">tableStaticMethodStr</span><span class="sxs-lookup"><span data-stu-id="20efa-975">tableStaticMethodStr</span></span>
<span data-ttu-id="20efa-976">指定した静的メソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-976">Validates that the specified static method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-977">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-977">Syntax</span></span>

    str tableStaticMethodStr(int table, int method)

### <a name="parameters"></a><span data-ttu-id="20efa-978">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-978">Parameters</span></span>

| <span data-ttu-id="20efa-979">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-979">Parameter</span></span> | <span data-ttu-id="20efa-980">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-980">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="20efa-981">テーブル</span><span class="sxs-lookup"><span data-stu-id="20efa-981">table</span></span>     | <span data-ttu-id="20efa-982">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-982">The name of the table.</span></span>                     |
| <span data-ttu-id="20efa-983">メソッド</span><span class="sxs-lookup"><span data-stu-id="20efa-983">method</span></span>    | <span data-ttu-id="20efa-984">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-984">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-985">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-985">Return Value</span></span>

<span data-ttu-id="20efa-986">指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-986">The name of the specified static method.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-987">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-987">Remarks</span></span>

<span data-ttu-id="20efa-988">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-988">This is a compile-time function.</span></span> <span data-ttu-id="20efa-989">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-989">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-990">例</span><span class="sxs-lookup"><span data-stu-id="20efa-990">Example</span></span>

    No example.

## <a name="tablestr"></a><span data-ttu-id="20efa-991">tableStr</span><span class="sxs-lookup"><span data-stu-id="20efa-991">tableStr</span></span>
<span data-ttu-id="20efa-992">指定したテーブルの名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-992">Retrieves a string that contains the name the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-993">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-993">Syntax</span></span>

    str tableStr(str table)

### <a name="parameters"></a><span data-ttu-id="20efa-994">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-994">Parameters</span></span>

| <span data-ttu-id="20efa-995">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-995">Parameter</span></span> | <span data-ttu-id="20efa-996">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-996">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="20efa-997">テーブル</span><span class="sxs-lookup"><span data-stu-id="20efa-997">table</span></span>     | <span data-ttu-id="20efa-998">文字列を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="20efa-998">The table to retrieve a string for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-999">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-999">Return Value</span></span>

<span data-ttu-id="20efa-1000">指定したテーブルの名前を含む文字列値。</span><span class="sxs-lookup"><span data-stu-id="20efa-1000">A string value that contains the name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1001">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1001">Remarks</span></span>

<span data-ttu-id="20efa-1002">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1002">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1003">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1003">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1004">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1004">Example</span></span>

<span data-ttu-id="20efa-1005">次の例では、**CustTable** テーブルの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="20efa-1005">The following example assigns the name of the **CustTable** table to the *MyTxt* variable.</span></span>

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

## <a name="tilestr"></a><span data-ttu-id="20efa-1006">tileStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1006">tileStr</span></span>
<span data-ttu-id="20efa-1007">指定したタイルの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1007">Retrieves a string that represents the name of the specified tile.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1008">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1008">Syntax</span></span>

    str tileStr(str tile)

### <a name="parameters"></a><span data-ttu-id="20efa-1009">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1009">Parameters</span></span>

| <span data-ttu-id="20efa-1010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1010">Parameter</span></span> | <span data-ttu-id="20efa-1011">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1011">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="20efa-1012">tile</span><span class="sxs-lookup"><span data-stu-id="20efa-1012">tile</span></span>      | <span data-ttu-id="20efa-1013">タイルの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1013">The name of the tile.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1014">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1014">Return Value</span></span>

<span data-ttu-id="20efa-1015">文字列のタイルの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1015">The name of the tile in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1016">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1016">Remarks</span></span>

<span data-ttu-id="20efa-1017">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1017">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1018">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1018">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1019">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1019">Example</span></span>

    No example.

## <a name="varstr"></a><span data-ttu-id="20efa-1020">varStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1020">varStr</span></span>
<span data-ttu-id="20efa-1021">指定した変数の名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1021">Retrieves a string that contains the name of the specified variable.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1022">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1022">Syntax</span></span>

    str varStr(str var)

### <a name="parameters"></a><span data-ttu-id="20efa-1023">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1023">Parameters</span></span>

| <span data-ttu-id="20efa-1024">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1024">Parameter</span></span> | <span data-ttu-id="20efa-1025">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1025">Description</span></span>               |
|-----------|---------------------------|
| <span data-ttu-id="20efa-1026">var</span><span class="sxs-lookup"><span data-stu-id="20efa-1026">var</span></span>       | <span data-ttu-id="20efa-1027">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1027">The name of the variable.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1028">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1028">Return Value</span></span>

<span data-ttu-id="20efa-1029">指定した変数の名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-1029">A string that contains the name of the specified variable.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1030">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1030">Remarks</span></span>

<span data-ttu-id="20efa-1031">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1031">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1032">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1032">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1033">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1033">Example</span></span>

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

## <a name="webactionitemstr"></a><span data-ttu-id="20efa-1034">webActionItemStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1034">webActionItemStr</span></span>
<span data-ttu-id="20efa-1035">指定した Web アクション項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1035">Validates that the specified web action item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1036">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1036">Syntax</span></span>

    str webActionItemStr(class webactionitem)

### <a name="parameters"></a><span data-ttu-id="20efa-1037">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1037">Parameters</span></span>

| <span data-ttu-id="20efa-1038">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1038">Parameter</span></span>     | <span data-ttu-id="20efa-1039">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1039">Description</span></span>                                  |
|---------------|----------------------------------------------|
| <span data-ttu-id="20efa-1040">webactionitem</span><span class="sxs-lookup"><span data-stu-id="20efa-1040">webactionitem</span></span> | <span data-ttu-id="20efa-1041">検証する Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1041">The name of the web action item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1042">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1042">Return Value</span></span>

<span data-ttu-id="20efa-1043">有効な場合の、指定された Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1043">The name of the specified web action item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1044">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1044">Remarks</span></span>

<span data-ttu-id="20efa-1045">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1045">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1046">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1046">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1047">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1047">Example</span></span>

    {
        str s;
        ;
        s = webActionItemStr(EPFlushData);
        print "webactionitem str is " + s;
        pause;
    }

## <a name="webdisplaycontentitemstr"></a><span data-ttu-id="20efa-1048">webDisplayContentItemStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1048">webDisplayContentItemStr</span></span>
<span data-ttu-id="20efa-1049">指定したWeb 表示のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1049">Validates that the specified web display content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1050">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1050">Syntax</span></span>

    str webDisplayContentItemStr(class webdisplaycontentitem)

### <a name="parameters"></a><span data-ttu-id="20efa-1051">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1051">Parameters</span></span>

| <span data-ttu-id="20efa-1052">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1052">Parameter</span></span>             | <span data-ttu-id="20efa-1053">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1053">Description</span></span>                                           |
|-----------------------|-------------------------------------------------------|
| <span data-ttu-id="20efa-1054">webdisplaycontentitem</span><span class="sxs-lookup"><span data-stu-id="20efa-1054">webdisplaycontentitem</span></span> | <span data-ttu-id="20efa-1055">検証する Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1055">The name of the web display content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1056">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1056">Return Value</span></span>

<span data-ttu-id="20efa-1057">有効な場合の、指定された Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1057">The name of the specified web display content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1058">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1058">Remarks</span></span>

<span data-ttu-id="20efa-1059">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1059">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1060">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1060">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1061">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1061">Example</span></span>

    {
        str s;
        ;

        s = webDisplayContentItemStr(EPAdmin);
        print "string for webcontent display item EPAdmin is " + s;
        pause;
    }

## <a name="webformstr"></a><span data-ttu-id="20efa-1062">webFormStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1062">webFormStr</span></span>
<span data-ttu-id="20efa-1063">指定した Web フォームがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1063">Validates that the specified web form exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1064">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1064">Syntax</span></span>

    str webFormStr(str name)

### <a name="parameters"></a><span data-ttu-id="20efa-1065">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1065">Parameters</span></span>

| <span data-ttu-id="20efa-1066">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1066">Parameter</span></span> | <span data-ttu-id="20efa-1067">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1067">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="20efa-1068">名前</span><span class="sxs-lookup"><span data-stu-id="20efa-1068">name</span></span>      | <span data-ttu-id="20efa-1069">検証する Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1069">The name of the web form to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1070">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1070">Return Value</span></span>

<span data-ttu-id="20efa-1071">有効な場合の、指定された Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1071">The name of the specified web form, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1072">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1072">Remarks</span></span>

<span data-ttu-id="20efa-1073">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1073">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1074">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1074">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1075">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1075">Example</span></span>

    {
        str s;
        ;
        s = webFormStr(EPAdmin);
        print "String for web form EPAdmin is " + s;
        pause;
    }

## <a name="webletitemstr"></a><span data-ttu-id="20efa-1076">webletItemStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1076">webletItemStr</span></span>
<span data-ttu-id="20efa-1077">指定した Weblet 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1077">Validates that the specified weblet item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1078">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1078">Syntax</span></span>

    str webletItemStr(class webletitem)

### <a name="parameters"></a><span data-ttu-id="20efa-1079">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1079">Parameters</span></span>

| <span data-ttu-id="20efa-1080">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1080">Parameter</span></span>  | <span data-ttu-id="20efa-1081">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1081">Description</span></span>                              |
|------------|------------------------------------------|
| <span data-ttu-id="20efa-1082">webletitem</span><span class="sxs-lookup"><span data-stu-id="20efa-1082">webletitem</span></span> | <span data-ttu-id="20efa-1083">検証する Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1083">The name of the weblet item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1084">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1084">Return Value</span></span>

<span data-ttu-id="20efa-1085">有効な場合の、指定された Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1085">The name of the specified weblet item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1086">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1086">Remarks</span></span>

<span data-ttu-id="20efa-1087">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1087">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1088">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1088">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1089">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1089">Example</span></span>

    {
        str s;
        ;
        s = webletItemStr(WebFormWeblet);
        print "String for WebFormWeblet is " + s;
        pause;
    }

## <a name="webmenustr"></a><span data-ttu-id="20efa-1090">webMenuStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1090">webMenuStr</span></span>
<span data-ttu-id="20efa-1091">指定した Web メニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1091">Validates that the specified web menu exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1092">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1092">Syntax</span></span>

    str webMenuStr(str name)

### <a name="parameters"></a><span data-ttu-id="20efa-1093">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1093">Parameters</span></span>

| <span data-ttu-id="20efa-1094">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1094">Parameter</span></span> | <span data-ttu-id="20efa-1095">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1095">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="20efa-1096">名前</span><span class="sxs-lookup"><span data-stu-id="20efa-1096">name</span></span>      | <span data-ttu-id="20efa-1097">検証する Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1097">The name of the web menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1098">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1098">Return Value</span></span>

<span data-ttu-id="20efa-1099">有効な場合の、指定された Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1099">The name of the specified web menu, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1100">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1100">Remarks</span></span>

<span data-ttu-id="20efa-1101">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1101">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1102">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1102">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1103">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1103">Example</span></span>

    {
        str s;
        ;
        s = webMenuStr(ECPAdmin);
        print "String for web menu ECPAdmin is " + s;
        pause;
    }

## <a name="weboutputcontentitemstr"></a><span data-ttu-id="20efa-1104">webOutputContentItemStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1104">webOutputContentItemStr</span></span>
<span data-ttu-id="20efa-1105">指定したWeb 出力のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1105">Validates that the specified web output content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1106">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1106">Syntax</span></span>

    str webOutputContentItemStr(class weboutputcontentitem)

### <a name="parameters"></a><span data-ttu-id="20efa-1107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1107">Parameters</span></span>

| <span data-ttu-id="20efa-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1108">Parameter</span></span>            | <span data-ttu-id="20efa-1109">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1109">Description</span></span>                                          |
|----------------------|------------------------------------------------------|
| <span data-ttu-id="20efa-1110">weboutputcontentitem</span><span class="sxs-lookup"><span data-stu-id="20efa-1110">weboutputcontentitem</span></span> | <span data-ttu-id="20efa-1111">検証する Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1111">The name of the web output content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1112">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1112">Return Value</span></span>

<span data-ttu-id="20efa-1113">有効な場合の、指定された Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1113">The name of the specified web output content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1114">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1114">Remarks</span></span>

<span data-ttu-id="20efa-1115">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1115">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1116">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1116">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1117">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1117">Example</span></span>

    {
        str s;
        ;
        s = webOutputContentItemStr(EPPriceList);
        print "string for weboutput content item EPPriceList is " + s;
        pause;
    }

## <a name="webpagedefstr"></a><span data-ttu-id="20efa-1118">webpageDefStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1118">webpageDefStr</span></span>
<span data-ttu-id="20efa-1119">指定した Web ページ定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1119">Validates that the specified Web page definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1120">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1120">Syntax</span></span>

    str webpageDefStr(str pagename)

### <a name="parameters"></a><span data-ttu-id="20efa-1121">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1121">Parameters</span></span>

| <span data-ttu-id="20efa-1122">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1122">Parameter</span></span> | <span data-ttu-id="20efa-1123">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1123">Description</span></span>                                      |
|-----------|--------------------------------------------------|
| <span data-ttu-id="20efa-1124">pagename</span><span class="sxs-lookup"><span data-stu-id="20efa-1124">pagename</span></span>  | <span data-ttu-id="20efa-1125">検証する Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1125">The name of the Web page definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1126">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1126">Return Value</span></span>

<span data-ttu-id="20efa-1127">有効な場合の、指定された Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1127">The name of the specified web-page definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1128">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1128">Remarks</span></span>

<span data-ttu-id="20efa-1129">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1129">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1130">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1130">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1131">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1131">Example</span></span>

    No example.

## <a name="webreportstr"></a><span data-ttu-id="20efa-1132">webReportStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1132">webReportStr</span></span>
<span data-ttu-id="20efa-1133">指定した Web レポートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1133">Validates that the specified web report exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1134">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1134">Syntax</span></span>

    str webReportStr(str name)

### <a name="parameters"></a><span data-ttu-id="20efa-1135">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1135">Parameters</span></span>

| <span data-ttu-id="20efa-1136">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1136">Parameter</span></span> | <span data-ttu-id="20efa-1137">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1137">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="20efa-1138">名前</span><span class="sxs-lookup"><span data-stu-id="20efa-1138">name</span></span>      | <span data-ttu-id="20efa-1139">検証する Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1139">The name of the web report to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1140">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1140">Return Value</span></span>

<span data-ttu-id="20efa-1141">有効な場合の、指定された Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1141">The name of the specified web report, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1142">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1142">Remarks</span></span>

<span data-ttu-id="20efa-1143">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1143">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1144">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1144">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1145">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1145">Example</span></span>

    {
        str s;
        ;
        s = webReportStr(EPCSSSalesConfirm);
        print "String for web report EPCSSalesConfirm is " + s;
        pause;
    }

## <a name="websitedefstr"></a><span data-ttu-id="20efa-1146">websiteDefStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1146">websiteDefStr</span></span>
<span data-ttu-id="20efa-1147">指定した Web サイトの定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1147">Validates that the specified web-site definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1148">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1148">Syntax</span></span>

    str websiteDefStr(str resourcename)

### <a name="parameters"></a><span data-ttu-id="20efa-1149">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1149">Parameters</span></span>

| <span data-ttu-id="20efa-1150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1150">Parameter</span></span>    | <span data-ttu-id="20efa-1151">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1151">Description</span></span>                                      |
|--------------|--------------------------------------------------|
| <span data-ttu-id="20efa-1152">resourcename</span><span class="sxs-lookup"><span data-stu-id="20efa-1152">resourcename</span></span> | <span data-ttu-id="20efa-1153">検証する Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1153">The name of the Web site definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1154">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1154">Return Value</span></span>

<span data-ttu-id="20efa-1155">有効な場合の、指定された Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1155">The name of the specified web-site definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1156">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1156">Remarks</span></span>

<span data-ttu-id="20efa-1157">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1157">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1158">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1158">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1159">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1159">Example</span></span>

    {
        str s;
        ;

        s = websiteDefStr(AxSiteDef_1033_xip);
        print "string for web site definition AxSiteDef_1033_xip is " + s;
        pause;
    }

## <a name="websitetempstr"></a><span data-ttu-id="20efa-1160">webSiteTempStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1160">webSiteTempStr</span></span>
<span data-ttu-id="20efa-1161">指定した Web サイトのテンプレートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1161">Validates that the specified web-site template exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1162">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1162">Syntax</span></span>

    str websiteTempStr(str resourcename)

### <a name="parameters"></a><span data-ttu-id="20efa-1163">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1163">Parameters</span></span>

| <span data-ttu-id="20efa-1164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1164">Parameter</span></span>    | <span data-ttu-id="20efa-1165">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1165">Description</span></span>                                    |
|--------------|------------------------------------------------|
| <span data-ttu-id="20efa-1166">resourcename</span><span class="sxs-lookup"><span data-stu-id="20efa-1166">resourcename</span></span> | <span data-ttu-id="20efa-1167">検証する Web サイト テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1167">The name of the Web site template to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1168">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1168">Return Value</span></span>

<span data-ttu-id="20efa-1169">有効な場合の、指定された Web テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1169">The name of the specified web-site template, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1170">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1170">Remarks</span></span>

<span data-ttu-id="20efa-1171">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1171">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1172">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1172">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1173">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1173">Example</span></span>

    No example.

## <a name="webstaticfilestr"></a><span data-ttu-id="20efa-1174">webStaticFileStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1174">webStaticFileStr</span></span>
<span data-ttu-id="20efa-1175">指定した Web 静的ファイルがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1175">Validates that the specified web static file exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1176">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1176">Syntax</span></span>

    str webStaticFileStr(str pagename)

### <a name="parameters"></a><span data-ttu-id="20efa-1177">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1177">Parameters</span></span>

| <span data-ttu-id="20efa-1178">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1178">Parameter</span></span> | <span data-ttu-id="20efa-1179">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1179">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="20efa-1180">pagename</span><span class="sxs-lookup"><span data-stu-id="20efa-1180">pagename</span></span>  | <span data-ttu-id="20efa-1181">検証する Web 静的ファイル テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1181">The name of the web static file to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1182">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1182">Return Value</span></span>

<span data-ttu-id="20efa-1183">有効な場合の、指定された Web 静的ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1183">The name of the specified web static file, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1184">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1184">Remarks</span></span>

<span data-ttu-id="20efa-1185">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1185">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1186">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1186">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1187">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1187">Example</span></span>

    {
        str s;
        ;

        s = webStaticFileStr(AXEP);
        print "string for web static file AXEP is " + s;
        pause;
    }

## <a name="weburlitemstr"></a><span data-ttu-id="20efa-1188">webUrlItemStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1188">webUrlItemStr</span></span>
<span data-ttu-id="20efa-1189">指定した Web URL 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1189">Validates that the specified web URL item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1190">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1190">Syntax</span></span>

    str webUrlItemStr(class weburlitem)

### <a name="parameters"></a><span data-ttu-id="20efa-1191">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1191">Parameters</span></span>

| <span data-ttu-id="20efa-1192">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1192">Parameter</span></span>  | <span data-ttu-id="20efa-1193">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1193">Description</span></span>                               |
|------------|-------------------------------------------|
| <span data-ttu-id="20efa-1194">weburlitem</span><span class="sxs-lookup"><span data-stu-id="20efa-1194">weburlitem</span></span> | <span data-ttu-id="20efa-1195">検証する Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1195">The name of the web URL item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1196">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1196">Return Value</span></span>

<span data-ttu-id="20efa-1197">有効な場合の、指定された Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1197">The name of the specified web URL item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1198">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1198">Remarks</span></span>

<span data-ttu-id="20efa-1199">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1199">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1200">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1200">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1201">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1201">Example</span></span>

    {
        str s;
        ;

        s = webUrlItemStr(EPAdmin);
        print "string for web url item EPAdmin is " + s;
        pause;
    }

## <a name="webwebpartstr"></a><span data-ttu-id="20efa-1202">webWebPartStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1202">webWebPartStr</span></span>
<span data-ttu-id="20efa-1203">指定した Web パーツがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1203">Validates that the specified web part exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1204">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1204">Syntax</span></span>

    str webWebpartStr(str resourcename)

### <a name="parameters"></a><span data-ttu-id="20efa-1205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1205">Parameters</span></span>

| <span data-ttu-id="20efa-1206">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1206">Parameter</span></span>    | <span data-ttu-id="20efa-1207">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1207">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="20efa-1208">resourcename</span><span class="sxs-lookup"><span data-stu-id="20efa-1208">resourcename</span></span> | <span data-ttu-id="20efa-1209">検証する Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1209">The name of the web part to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1210">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1210">Return Value</span></span>

<span data-ttu-id="20efa-1211">有効な場合の、指定された Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1211">The name of the specified web part, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1212">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1212">Remarks</span></span>

<span data-ttu-id="20efa-1213">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1213">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1214">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1214">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1215">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1215">Example</span></span>

    {
        str s;
        ;

        s = webWebpartStr(AxWebParts_cab);
        print "string for web part AxWebParts_cab is " + s;
        pause;
    }

## <a name="workflowapprovalstr"></a><span data-ttu-id="20efa-1216">workflowApprovalStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1216">workflowApprovalStr</span></span>
<span data-ttu-id="20efa-1217">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー承認の名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1217">Retrieves the name of a workflow approval in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1218">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1218">Syntax</span></span>

    str workflowapprovalstr(approval approval)

### <a name="parameters"></a><span data-ttu-id="20efa-1219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1219">Parameters</span></span>

| <span data-ttu-id="20efa-1220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1220">Parameter</span></span> | <span data-ttu-id="20efa-1221">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1221">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="20efa-1222">承認</span><span class="sxs-lookup"><span data-stu-id="20efa-1222">approval</span></span>  | <span data-ttu-id="20efa-1223">ワークフローの承認のアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1223">The Application Explorer name of the workflow approval.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1224">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1224">Return Value</span></span>

<span data-ttu-id="20efa-1225">ワークフローの承認のアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-1225">A string that represents the Application Explorer name of the workflow approval.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1226">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1226">Remarks</span></span>

<span data-ttu-id="20efa-1227">リテラル テキストの代わりにこの関数を使用して、ワークフロー承認名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1227">Use this function instead of literal text to retrieve a string that contains the workflow approval name.</span></span> <span data-ttu-id="20efa-1228">ワークフローの承認が存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1228">If the workflow approval does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="20efa-1229">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1229">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1230">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1230">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1231">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1231">Example</span></span>

<span data-ttu-id="20efa-1232">次のコード例では、変数 *str s* を **MyWorkflowApproval** に設定します。これは、アプリケーション エクスプローラーでのワークフロー承認の名前です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1232">The following code example sets the variable *str s* to **MyWorkflowApproval** which is the name of the workflow approval in the Application Explorer.</span></span>

    static void MyWorkflowApprovalStrExample(Args _args)
    {
        str s;
        ;
        s = workflowapprovalstr(MyWorkflowApproval);
        print s;
        pause;
    }

## <a name="workflowcategorystr"></a><span data-ttu-id="20efa-1233">workflowCategoryStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1233">workflowCategoryStr</span></span>
<span data-ttu-id="20efa-1234">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー カテゴリの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1234">Retrieves the name of a workflow category in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1235">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1235">Syntax</span></span>

    str workflowcategorystr(category category)

### <a name="parameters"></a><span data-ttu-id="20efa-1236">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1236">Parameters</span></span>

| <span data-ttu-id="20efa-1237">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1237">Parameter</span></span> | <span data-ttu-id="20efa-1238">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1238">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="20efa-1239">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="20efa-1239">category</span></span>  | <span data-ttu-id="20efa-1240">ワークフロー カテゴリーのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1240">The Application Explorer name of the workflow category.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1241">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1241">Return Value</span></span>

<span data-ttu-id="20efa-1242">ワークフロー カテゴリのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-1242">A string that represents the Application Explorer name of the workflow category.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1243">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1243">Remarks</span></span>

<span data-ttu-id="20efa-1244">リテラル テキストの代わりにこの関数を使用して、ワークフロー カテゴリ名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1244">Use this function instead of literal text to retrieve a string that contains the workflow category name.</span></span> <span data-ttu-id="20efa-1245">ワークフローのカテゴリーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1245">If the workflow category does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="20efa-1246">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1246">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1247">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1247">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1248">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1248">Example</span></span>

<span data-ttu-id="20efa-1249">次のコード例では、変数 *str s* を **MyWorkflowCategory** に設定します。これは、アプリケーション エクスプローラーでのワークフロー カテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1249">The following code example sets the variable *str s* to **MyWorkflowCategory** which is the name of the workflow category in the Application Explorer.</span></span>

    static void MyWorkflowCategoryStrExample(Args _args)
    {
        str s;
        ;
        s = workflowcategorystr(MyWorkflowCategory);
        print s;
        pause;
    }

## <a name="workflowtaskstr"></a><span data-ttu-id="20efa-1250">workflowTaskStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1250">workflowTaskStr</span></span>
<span data-ttu-id="20efa-1251">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー タスクの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1251">Retrieves the name of a workflow task in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1252">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1252">Syntax</span></span>

    str workflowtaskstr(task task)

### <a name="parameters"></a><span data-ttu-id="20efa-1253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1253">Parameters</span></span>

| <span data-ttu-id="20efa-1254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1254">Parameter</span></span> | <span data-ttu-id="20efa-1255">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1255">Description</span></span>                                         |
|-----------|-----------------------------------------------------|
| <span data-ttu-id="20efa-1256">タスク</span><span class="sxs-lookup"><span data-stu-id="20efa-1256">task</span></span>      | <span data-ttu-id="20efa-1257">ワークフロー タスクのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1257">The Application Explorer name of the workflow task.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1258">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1258">Return Value</span></span>

<span data-ttu-id="20efa-1259">ワークフロー タスクのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="20efa-1259">A string that represents the Application Explorer name of the workflow task.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1260">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1260">Remarks</span></span>

<span data-ttu-id="20efa-1261">リテラル テキストの代わりにこの関数を使用して、ワークフロー タスク名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1261">Use this function instead of literal text to retrieve a string that contains the workflow task name.</span></span> <span data-ttu-id="20efa-1262">ワークフローのタスクーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1262">If the workflow task does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="20efa-1263">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1263">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1264">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1264">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1265">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1265">Example</span></span>

<span data-ttu-id="20efa-1266">次のコード例では、変数 *str s* を **MyWorkflowTask** に設定します。これは、アプリケーション エクスプローラーでのワークフロー タスクの名前です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1266">The following code example sets the variable *str s* to **MyWorkflowTask** which is the name of the workflow task in the Application Explorer.</span></span>

    static void MyWorkflowTaskStrExample(Args _args)
    {
        str s;
        ;
        s = workflowtaskstr(MyWorkflowTask);
        print s;
        pause;
    }

## <a name="workflowtypestr"></a><span data-ttu-id="20efa-1267">workflowTypeStr</span><span class="sxs-lookup"><span data-stu-id="20efa-1267">workflowTypeStr</span></span>
<span data-ttu-id="20efa-1268">指定したワークフロー タイプがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20efa-1268">Validates that the specified workflow type exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="20efa-1269">構文</span><span class="sxs-lookup"><span data-stu-id="20efa-1269">Syntax</span></span>

    str workflowTypeStr(str workflow)

### <a name="parameters"></a><span data-ttu-id="20efa-1270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1270">Parameters</span></span>

| <span data-ttu-id="20efa-1271">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20efa-1271">Parameter</span></span> | <span data-ttu-id="20efa-1272">説明</span><span class="sxs-lookup"><span data-stu-id="20efa-1272">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="20efa-1273">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="20efa-1273">workflow</span></span>  | <span data-ttu-id="20efa-1274">検証するワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1274">The name of the workflow type to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="20efa-1275">戻り値</span><span class="sxs-lookup"><span data-stu-id="20efa-1275">Return Value</span></span>

<span data-ttu-id="20efa-1276">ワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="20efa-1276">The name of the workflow type.</span></span>

### <a name="remarks"></a><span data-ttu-id="20efa-1277">備考</span><span class="sxs-lookup"><span data-stu-id="20efa-1277">Remarks</span></span>

<span data-ttu-id="20efa-1278">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="20efa-1278">This is a compile-time function.</span></span> <span data-ttu-id="20efa-1279">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20efa-1279">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="20efa-1280">例</span><span class="sxs-lookup"><span data-stu-id="20efa-1280">Example</span></span>

    static void workFlowTypeStrExample(Args _args)
    {
        str s;
        ;
        s = workFlowTypeStr(BudgetAccountEntryType);
        print s;
        pause;
    }



