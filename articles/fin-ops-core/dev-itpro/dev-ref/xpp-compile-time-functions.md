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
ms.openlocfilehash: 72bec5a120a4b05d5f1fff5c3e736e44c0652fe6
ms.sourcegitcommit: 7c750711e9fe1d3726c6ee650669529684933001
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386120"
---
# <a name="x-compile-time-functions"></a><span data-ttu-id="2274c-103">X++ コンパイル時関数</span><span class="sxs-lookup"><span data-stu-id="2274c-103">X++ compile-time functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2274c-104">このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。</span><span class="sxs-lookup"><span data-stu-id="2274c-104">This topic lists the compile-time functions and describes their syntax, parameters, and return values.</span></span>

## <a name="overview"></a><span data-ttu-id="2274c-105">概要</span><span class="sxs-lookup"><span data-stu-id="2274c-105">Overview</span></span>

<span data-ttu-id="2274c-106">コンパイル時関数は、X++ コードのコンパイル時に早期実行されます。</span><span class="sxs-lookup"><span data-stu-id="2274c-106">Compile-time functions are executed early during compilation of X++ code.</span></span> <span data-ttu-id="2274c-107">アプリケーション エクスプローラーに保存されているメタデータの変更に対してコードを復元するためには、可能な限り X++ で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2274c-107">They should be used wherever possible in X++ code to make the code resilient to changes to the metadata stored in the Application Explorer.</span></span> <span data-ttu-id="2274c-108">コンパイル時関数は、コンパイラによって入力値が検証されます。</span><span class="sxs-lookup"><span data-stu-id="2274c-108">Compile-time functions have their input value verified by the compiler.</span></span> <span data-ttu-id="2274c-109">入力された値が見つからず、アプリケーション エクスプローラーの既存のオブジェクトが一致しない場合は、コンパイラーはエラーを発行します。</span><span class="sxs-lookup"><span data-stu-id="2274c-109">If the input value is not found to match any existing object in the Application Explorer, the compiler issues an error.</span></span> <span data-ttu-id="2274c-110">コンパイラは実行時に変数に含まれる値を判別できないため、これらの関数への入力はリテラルでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2274c-110">The inputs to these functions must be literals, because the compiler cannot determine the value that a variable contains at run time.</span></span> <span data-ttu-id="2274c-111">コンパイル時関数は、メタデータ アサーション関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-111">A compile-time function is a metadata assertion function.</span></span> <span data-ttu-id="2274c-112">アプリケーション エクスプローラーでエンティティを表す引数を取得し、コンパイル時にその引数を検証します。</span><span class="sxs-lookup"><span data-stu-id="2274c-112">It takes arguments that represents an entity in the Application Explorer and validates the arguments at compile time.</span></span> <span data-ttu-id="2274c-113">実行時に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="2274c-113">It has no effect at run time.</span></span> <span data-ttu-id="2274c-114">属性は **SysAttribute** クラスから継承するクラスです。</span><span class="sxs-lookup"><span data-stu-id="2274c-114">Attributes are classes that inherit from the **SysAttribute** class.</span></span> <span data-ttu-id="2274c-115">フォーム、レポート、クエリ、メニュー のメタデータの検証をサポートするには、コントロールの **AutoDeclaration** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="2274c-115">To support the validation of form, report, query, and menu metadata, use the **AutoDeclaration** property on controls.</span></span> <span data-ttu-id="2274c-116">これらの機能のほとんどは、アプリケーション エクスプローラーにある項目に関するメタデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-116">Most of these functions retrieve metadata about items that are in the Application Explorer.</span></span> <span data-ttu-id="2274c-117">いくつかの一般的なコンパイル時機能は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2274c-117">Some common compile time functions are as follows:</span></span>

-   <span data-ttu-id="2274c-118">`classNum` – クラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-118">`classNum` – Retrieves the ID of a class.</span></span>
-   <span data-ttu-id="2274c-119">`classStr` – コンパイル時に、その名前のクラスが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2274c-119">`classStr` – During compile time, verifies that a class of that name exists.</span></span> <span data-ttu-id="2274c-120">この方法は、実行時にエラーを後で発見するよりも優れています。</span><span class="sxs-lookup"><span data-stu-id="2274c-120">This approach is better than discovering the error later during run time.</span></span>
-   <span data-ttu-id="2274c-121">`evalBuf`– X++ コードの入力文字列を評価し、結果を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-121">`evalBuf`– Evaluates the input string of X++ code, and then returns the results as a string.</span></span>
-   <span data-ttu-id="2274c-122">`literalStr` – は、文字列 `"@SYS12345"` などのラベルの文字列表示が与えられたときにラベル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-122">`literalStr` – retrieves a label ID when given the string representation of a label, such as the string `"@SYS12345"`.</span></span> <span data-ttu-id="2274c-123">たとえば、`myLabel.exists(literalStr("@SYS12345"));`。</span><span class="sxs-lookup"><span data-stu-id="2274c-123">For example, `myLabel.exists(literalStr("@SYS12345"));`.</span></span>

> [!NOTE]
> <span data-ttu-id="2274c-124">X++ コンパイル時関数は .NET プログラムから呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="2274c-124">X++ compile time functions cannot be called from a .NET program.</span></span>

### <a name="functions"></a><span data-ttu-id="2274c-125">関数</span><span class="sxs-lookup"><span data-stu-id="2274c-125">Functions</span></span>

## <a name="attributestr"></a><span data-ttu-id="2274c-126">attributeStr</span><span class="sxs-lookup"><span data-stu-id="2274c-126">attributeStr</span></span>
<span data-ttu-id="2274c-127">指定した属性クラスがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-127">Validates that the specified attribute class exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-128">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-128">Syntax</span></span>

```xpp
str classStr(class class)
```

### <a name="parameters"></a><span data-ttu-id="2274c-129">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-129">Parameters</span></span>

| <span data-ttu-id="2274c-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-130">Parameter</span></span> | <span data-ttu-id="2274c-131">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-131">Description</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="2274c-132">クラス</span><span class="sxs-lookup"><span data-stu-id="2274c-132">class</span></span>     | <span data-ttu-id="2274c-133">検証する属性の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-133">The name of the attribute to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-134">Return Value</span></span>

<span data-ttu-id="2274c-135">属性の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-135">The name of the attribute.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-136">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-136">Remarks</span></span>

<span data-ttu-id="2274c-137">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-137">This is a compile-time function.</span></span> <span data-ttu-id="2274c-138">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-138">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-139">例</span><span class="sxs-lookup"><span data-stu-id="2274c-139">Example</span></span>
```xpp
static void attributeStrExample(Args _args)
{
    str s;
    ;
    s = attributeStr(AifDocumentOperationAttribute);
    print s;
    pause;
}
``` 

## <a name="classnum"></a><span data-ttu-id="2274c-140">classNum</span><span class="sxs-lookup"><span data-stu-id="2274c-140">classNum</span></span>
<span data-ttu-id="2274c-141">指定されたクラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-141">Retrieves the ID of the specified class.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-142">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-142">Syntax</span></span>

```xpp
int classNum(class class)
```

### <a name="parameters"></a><span data-ttu-id="2274c-143">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-143">Parameters</span></span>

| <span data-ttu-id="2274c-144">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-144">Parameter</span></span> | <span data-ttu-id="2274c-145">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-145">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="2274c-146">クラス</span><span class="sxs-lookup"><span data-stu-id="2274c-146">class</span></span>     | <span data-ttu-id="2274c-147">ID を取得するクラス。</span><span class="sxs-lookup"><span data-stu-id="2274c-147">The class for which to retrieve the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-148">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-148">Return Value</span></span>

<span data-ttu-id="2274c-149">指定されたクラスの ID。</span><span class="sxs-lookup"><span data-stu-id="2274c-149">The ID of the specified class.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-150">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-150">Remarks</span></span>

<span data-ttu-id="2274c-151">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-151">This is a compile-time function.</span></span> <span data-ttu-id="2274c-152">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-152">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-153">例</span><span class="sxs-lookup"><span data-stu-id="2274c-153">Example</span></span>

```xpp
static void classNumExample(Args _args)
{
    int i;
    ;
    i = classNum(Global);
    print i;
    pause;
}
```

## <a name="classstr"></a><span data-ttu-id="2274c-154">classStr</span><span class="sxs-lookup"><span data-stu-id="2274c-154">classStr</span></span>
<span data-ttu-id="2274c-155">文字列としてクラスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-155">Retrieves the name of a class as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-156">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-156">Syntax</span></span>

```xpp
str classStr(class class)
```

### <a name="parameters"></a><span data-ttu-id="2274c-157">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-157">Parameters</span></span>

| <span data-ttu-id="2274c-158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-158">Parameter</span></span> | <span data-ttu-id="2274c-159">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-159">Description</span></span>                      |
|-----------|----------------------------------|
| <span data-ttu-id="2274c-160">クラス</span><span class="sxs-lookup"><span data-stu-id="2274c-160">class</span></span>     | <span data-ttu-id="2274c-161">返すクラスの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-161">The name of the class to return.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-162">Return Value</span></span>

<span data-ttu-id="2274c-163">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-163">The name of the class.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-164">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-164">Remarks</span></span>

<span data-ttu-id="2274c-165">リテラル テキストの代わりにこの関数を使用して、クラス名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-165">Use this function instead of literal text to retrieve a string that contains the class name.</span></span> <span data-ttu-id="2274c-166">クラスが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="2274c-166">If the class does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="2274c-167">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-167">This is a compile-time function.</span></span> <span data-ttu-id="2274c-168">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-168">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-169">例</span><span class="sxs-lookup"><span data-stu-id="2274c-169">Example</span></span>

```xpp
static void clStrExample(Args _args)
{
    str s;
    ;
    s = classStr(Global);
    print s;
    pause;
}
```

## <a name="configurationkeynum"></a><span data-ttu-id="2274c-170">configurationKeyNum</span><span class="sxs-lookup"><span data-stu-id="2274c-170">configurationKeyNum</span></span>
<span data-ttu-id="2274c-171">指定されたコンフィギュレーション キーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-171">Retrieves the ID of the specified configuration key.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-172">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-172">Syntax</span></span>

```xpp
int configurationKeyNum(str keyname)
```

### <a name="parameters"></a><span data-ttu-id="2274c-173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-173">Parameters</span></span>

| <span data-ttu-id="2274c-174">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-174">Parameter</span></span> | <span data-ttu-id="2274c-175">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-175">Description</span></span>                                       |
|-----------|---------------------------------------------------|
| <span data-ttu-id="2274c-176">keyname</span><span class="sxs-lookup"><span data-stu-id="2274c-176">keyname</span></span>   | <span data-ttu-id="2274c-177">ID を返すコンフィギュレーション キー。</span><span class="sxs-lookup"><span data-stu-id="2274c-177">The configuration key for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-178">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-178">Return Value</span></span>

<span data-ttu-id="2274c-179">指定されたコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="2274c-179">The ID of the specified configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-180">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-180">Remarks</span></span>

<span data-ttu-id="2274c-181">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-181">This is a compile-time function.</span></span> <span data-ttu-id="2274c-182">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-182">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-183">例</span><span class="sxs-lookup"><span data-stu-id="2274c-183">Example</span></span>

```xpp
static void configurationKeyNum(Args _args)
{
    int i;
    ;
    i = configurationKeyNum(AIF);
    print i;
    pause;
}
```

## <a name="configurationkeystr"></a><span data-ttu-id="2274c-184">configurationKeyStr</span><span class="sxs-lookup"><span data-stu-id="2274c-184">configurationKeyStr</span></span>
<span data-ttu-id="2274c-185">文字列としてコンフィギュレーション キーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-185">Retrieves the name of a configuration key as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-186">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-186">Syntax</span></span>

```xpp
str configurationKeyStr(str keyname)
```

### <a name="parameters"></a><span data-ttu-id="2274c-187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-187">Parameters</span></span>

| <span data-ttu-id="2274c-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-188">Parameter</span></span> | <span data-ttu-id="2274c-189">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-189">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="2274c-190">keyname</span><span class="sxs-lookup"><span data-stu-id="2274c-190">keyname</span></span>   | <span data-ttu-id="2274c-191">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-191">The name of the configuration key.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-192">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-192">Return Value</span></span>

<span data-ttu-id="2274c-193">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-193">The name of the configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-194">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-194">Remarks</span></span>

<span data-ttu-id="2274c-195">リテラル テキストの代わりにこの関数を使用して、構成キー名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-195">Use this function instead of literal text to retrieve a string that contains the configuration key name.</span></span> <span data-ttu-id="2274c-196">キーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="2274c-196">If the key does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="2274c-197">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-197">This is a compile-time function.</span></span> <span data-ttu-id="2274c-198">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-198">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-199">例</span><span class="sxs-lookup"><span data-stu-id="2274c-199">Example</span></span>

```xpp
static void configurationKeyStrExample(Args _args)
{
    str s;
    ;
    s = configurationKeyStr(AIF);
    print s;
    pause;
}
```

## <a name="dataentitydatasourcestr"></a><span data-ttu-id="2274c-200">dataEntityDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="2274c-200">dataEntityDataSourceStr</span></span>
<span data-ttu-id="2274c-201">データ エンティティのデータ ソースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-201">Retrieves the name of a data source of a data entity.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-202">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-202">Syntax</span></span>

```xpp
str dataEntityDataSourceStr(str dataEntity, str dataSource)
```

### <a name="parameters"></a><span data-ttu-id="2274c-203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-203">Parameters</span></span>

| <span data-ttu-id="2274c-204">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-204">Parameter</span></span>  | <span data-ttu-id="2274c-205">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-205">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="2274c-206">dataEntity</span><span class="sxs-lookup"><span data-stu-id="2274c-206">dataEntity</span></span> | <span data-ttu-id="2274c-207">データ エンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-207">The name of the data entity.</span></span> |
| <span data-ttu-id="2274c-208">dataSource</span><span class="sxs-lookup"><span data-stu-id="2274c-208">dataSource</span></span> | <span data-ttu-id="2274c-209">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-209">The name of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-210">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-210">Return Value</span></span>

<span data-ttu-id="2274c-211">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-211">The name of the data source.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-212">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-212">Remarks</span></span>

<span data-ttu-id="2274c-213">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-213">This is a compile-time function.</span></span> <span data-ttu-id="2274c-214">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-214">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-215">例</span><span class="sxs-lookup"><span data-stu-id="2274c-215">Example</span></span>

<span data-ttu-id="2274c-216">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-216">No example.</span></span>

## <a name="delegatestr"></a><span data-ttu-id="2274c-217">delegateStr</span><span class="sxs-lookup"><span data-stu-id="2274c-217">delegateStr</span></span>
<span data-ttu-id="2274c-218">委任の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-218">Returns the name of the delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-219">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-219">Syntax</span></span>

```xpp
str delegateStr(str class, str instanceDelegate)
```

### <a name="parameters"></a><span data-ttu-id="2274c-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-220">Parameters</span></span>

| <span data-ttu-id="2274c-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-221">Parameter</span></span>        | <span data-ttu-id="2274c-222">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-222">Description</span></span>                            |
|------------------|----------------------------------------|
| <span data-ttu-id="2274c-223">クラス</span><span class="sxs-lookup"><span data-stu-id="2274c-223">class</span></span>            | <span data-ttu-id="2274c-224">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-224">The name of the class, table, or form.</span></span> |
| <span data-ttu-id="2274c-225">instanceDelegate</span><span class="sxs-lookup"><span data-stu-id="2274c-225">instanceDelegate</span></span> | <span data-ttu-id="2274c-226">インスタンス デリゲートの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-226">The name of the instance delegate.</span></span>     |

### <a name="return-value"></a><span data-ttu-id="2274c-227">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-227">Return Value</span></span>

<span data-ttu-id="2274c-228">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="2274c-228">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-229">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-229">Remarks</span></span>

<span data-ttu-id="2274c-230">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-230">This is a compile-time function.</span></span> <span data-ttu-id="2274c-231">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-231">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-232">例</span><span class="sxs-lookup"><span data-stu-id="2274c-232">Example</span></span>

<span data-ttu-id="2274c-233">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-233">No example.</span></span>

## <a name="dimensionhierarchylevelstr"></a><span data-ttu-id="2274c-234">dimensionHierarchyLevelStr</span><span class="sxs-lookup"><span data-stu-id="2274c-234">dimensionHierarchyLevelStr</span></span>
<span data-ttu-id="2274c-235">分析コード階層レベルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-235">Returns the name of the dimension hierarchy level.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-236">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-236">Syntax</span></span>

```xpp
str dimensionHierarchyLevelStr(str dimensionHierarchyLevel)
```

### <a name="parameters"></a><span data-ttu-id="2274c-237">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-237">Parameters</span></span>

| <span data-ttu-id="2274c-238">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-238">Parameter</span></span>               | <span data-ttu-id="2274c-239">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-239">Description</span></span>                                |
|-------------------------|--------------------------------------------|
| <span data-ttu-id="2274c-240">dimensionHierarchyLevel</span><span class="sxs-lookup"><span data-stu-id="2274c-240">dimensionHierarchyLevel</span></span> | <span data-ttu-id="2274c-241">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-241">The name of the dimension hierarchy level.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-242">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-242">Return Value</span></span>

<span data-ttu-id="2274c-243">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-243">The name of the dimension hierarchy level.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-244">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-244">Remarks</span></span>

<span data-ttu-id="2274c-245">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-245">This is a compile-time function.</span></span> <span data-ttu-id="2274c-246">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-246">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-247">例</span><span class="sxs-lookup"><span data-stu-id="2274c-247">Example</span></span>

<span data-ttu-id="2274c-248">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-248">No example.</span></span>

## <a name="dimensionhierarchystr"></a><span data-ttu-id="2274c-249">dimensionHierarchyStr</span><span class="sxs-lookup"><span data-stu-id="2274c-249">dimensionHierarchyStr</span></span>
<span data-ttu-id="2274c-250">分析コード階層の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-250">Returns the name of the dimension hierarchy.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-251">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-251">Syntax</span></span>

```xpp
str dimensionHierarchyStr(str dimensionHierarchy)
```

### <a name="parameters"></a><span data-ttu-id="2274c-252">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-252">Parameters</span></span>

| <span data-ttu-id="2274c-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-253">Parameter</span></span>          | <span data-ttu-id="2274c-254">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-254">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="2274c-255">dimensionHierarchy</span><span class="sxs-lookup"><span data-stu-id="2274c-255">dimensionHierarchy</span></span> | <span data-ttu-id="2274c-256">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-256">The name of the dimension hierarchy.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-257">Return Value</span></span>

<span data-ttu-id="2274c-258">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-258">The name of the dimension hierarchy.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-259">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-259">Remarks</span></span>

<span data-ttu-id="2274c-260">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-260">This is a compile-time function.</span></span> <span data-ttu-id="2274c-261">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-261">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-262">例</span><span class="sxs-lookup"><span data-stu-id="2274c-262">Example</span></span>

<span data-ttu-id="2274c-263">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-263">No example.</span></span>

## <a name="dimensionreferencestr"></a><span data-ttu-id="2274c-264">dimensionReferenceStr</span><span class="sxs-lookup"><span data-stu-id="2274c-264">dimensionReferenceStr</span></span>
<span data-ttu-id="2274c-265">分析コード参照の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-265">Returns the name of the dimension reference.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-266">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-266">Syntax</span></span>

```xpp
str dimensionReferenceStr(str dimensionReference)
```

### <a name="parameters"></a><span data-ttu-id="2274c-267">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-267">Parameters</span></span>

| <span data-ttu-id="2274c-268">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-268">Parameter</span></span>          | <span data-ttu-id="2274c-269">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-269">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="2274c-270">dimensionReference</span><span class="sxs-lookup"><span data-stu-id="2274c-270">dimensionReference</span></span> | <span data-ttu-id="2274c-271">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-271">The name of the dimension reference.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-272">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-272">Return Value</span></span>

<span data-ttu-id="2274c-273">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-273">The name of the dimension reference.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-274">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-274">Remarks</span></span>

<span data-ttu-id="2274c-275">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-275">This is a compile-time function.</span></span> <span data-ttu-id="2274c-276">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-276">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-277">例</span><span class="sxs-lookup"><span data-stu-id="2274c-277">Example</span></span>

<span data-ttu-id="2274c-278">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-278">No example.</span></span>

## <a name="dutystr"></a><span data-ttu-id="2274c-279">dutyStr</span><span class="sxs-lookup"><span data-stu-id="2274c-279">dutyStr</span></span>
<span data-ttu-id="2274c-280">指定したセキュリティ職務権限の名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-280">Retrieves a string that represents the name of the specified security duty.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-281">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-281">Syntax</span></span>

```xpp
str dutyStr(str securityDuty)
```

### <a name="parameters"></a><span data-ttu-id="2274c-282">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-282">Parameters</span></span>

| <span data-ttu-id="2274c-283">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-283">Parameter</span></span>    | <span data-ttu-id="2274c-284">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-284">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="2274c-285">securityDuty</span><span class="sxs-lookup"><span data-stu-id="2274c-285">securityDuty</span></span> | <span data-ttu-id="2274c-286">セキュリティ職務権限の名前です。</span><span class="sxs-lookup"><span data-stu-id="2274c-286">The name of the security duty.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-287">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-287">Return Value</span></span>

<span data-ttu-id="2274c-288">文字列のセキュリティ職務の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-288">The name of the security duty in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-289">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-289">Remarks</span></span>

<span data-ttu-id="2274c-290">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-290">This is a compile-time function.</span></span> <span data-ttu-id="2274c-291">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-291">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-292">例</span><span class="sxs-lookup"><span data-stu-id="2274c-292">Example</span></span>

<span data-ttu-id="2274c-293">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-293">No example.</span></span>

## <a name="enumcnt"></a><span data-ttu-id="2274c-294">enumCnt</span><span class="sxs-lookup"><span data-stu-id="2274c-294">enumCnt</span></span>
<span data-ttu-id="2274c-295">指定された列挙型の要素数を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-295">Retrieves the number of elements in the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-296">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-296">Syntax</span></span>

```xpp
int enumCnt(enum enumtype)
```

### <a name="parameters"></a><span data-ttu-id="2274c-297">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-297">Parameters</span></span>

| <span data-ttu-id="2274c-298">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-298">Parameter</span></span> | <span data-ttu-id="2274c-299">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-299">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="2274c-300">enumtype</span><span class="sxs-lookup"><span data-stu-id="2274c-300">enumtype</span></span>  | <span data-ttu-id="2274c-301">列挙型タイプ。</span><span class="sxs-lookup"><span data-stu-id="2274c-301">The enumeration type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-302">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-302">Return Value</span></span>

<span data-ttu-id="2274c-303">指定された列挙型の要素数。</span><span class="sxs-lookup"><span data-stu-id="2274c-303">The number of elements in the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-304">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-304">Remarks</span></span>

<span data-ttu-id="2274c-305">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-305">This is a compile-time function.</span></span> <span data-ttu-id="2274c-306">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-306">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-307">例</span><span class="sxs-lookup"><span data-stu-id="2274c-307">Example</span></span>

```xpp
enumCnt(NoYes); //Returns 2, as the two elements are Yes and No.
```

## <a name="enumliteralstr"></a><span data-ttu-id="2274c-308">enumLiteralStr</span><span class="sxs-lookup"><span data-stu-id="2274c-308">enumLiteralStr</span></span>
<span data-ttu-id="2274c-309">指定した文字列が指定した列挙型の要素であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2274c-309">Indicates whether the specified string is an element of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-310">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-310">Syntax</span></span>

```xpp
\enumLiteralStr(enum enum, string str)
```

### <a name="parameters"></a><span data-ttu-id="2274c-311">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-311">Parameters</span></span>

| <span data-ttu-id="2274c-312">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-312">Parameter</span></span> | <span data-ttu-id="2274c-313">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-313">Description</span></span>                                                      |
|-----------|------------------------------------------------------------------|
| <span data-ttu-id="2274c-314">列挙型</span><span class="sxs-lookup"><span data-stu-id="2274c-314">enum</span></span>      | <span data-ttu-id="2274c-315">指定された値を取得する列挙型。</span><span class="sxs-lookup"><span data-stu-id="2274c-315">The enumeration type from which to retrieve the specified value.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-316">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-316">Return Value</span></span>

<span data-ttu-id="2274c-317">指定された文字列が見つかった場合の *str* パラメーターの値。それ以外の場合は、コンパイル エラーです。</span><span class="sxs-lookup"><span data-stu-id="2274c-317">The value of the *str* parameter if the specified string was found; otherwise, a compilation error.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-318">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-318">Remarks</span></span>

<span data-ttu-id="2274c-319">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-319">This is a compile-time function.</span></span> <span data-ttu-id="2274c-320">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-320">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-321">例</span><span class="sxs-lookup"><span data-stu-id="2274c-321">Example</span></span>

```xpp
static void getEnumValueAsString()
{
    str i;
    i = enumLiteralStr(ABCEnum, "valueInABCEnum");
    print i;
    pause;
}
```

## <a name="enumnum"></a><span data-ttu-id="2274c-322">enumNum</span><span class="sxs-lookup"><span data-stu-id="2274c-322">enumNum</span></span>
<span data-ttu-id="2274c-323">指定された列挙型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-323">Retrieves the ID of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-324">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-324">Syntax</span></span>
```xpp
int enumNum(enum enum)
```

### <a name="parameters"></a><span data-ttu-id="2274c-325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-325">Parameters</span></span>

| <span data-ttu-id="2274c-326">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-326">Parameter</span></span> | <span data-ttu-id="2274c-327">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-327">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="2274c-328">列挙型</span><span class="sxs-lookup"><span data-stu-id="2274c-328">enum</span></span>      | <span data-ttu-id="2274c-329">ID を返す列挙。</span><span class="sxs-lookup"><span data-stu-id="2274c-329">The enumeration for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-330">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-330">Return Value</span></span>

<span data-ttu-id="2274c-331">指定された列挙型の ID。</span><span class="sxs-lookup"><span data-stu-id="2274c-331">The ID of the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-332">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-332">Remarks</span></span>

<span data-ttu-id="2274c-333">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-333">This is a compile-time function.</span></span> <span data-ttu-id="2274c-334">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-334">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-335">例</span><span class="sxs-lookup"><span data-stu-id="2274c-335">Example</span></span>

```xpp
static void enumNum(Args _args)
{
    int i;
    ;
    i = enumNum(ABC);
    print i;
    pause;
}
```

## <a name="enumstr"></a><span data-ttu-id="2274c-336">enumStr</span><span class="sxs-lookup"><span data-stu-id="2274c-336">enumStr</span></span>
<span data-ttu-id="2274c-337">文字列として列挙型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-337">Retrieves the name of an enumeration as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-338">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-338">Syntax</span></span>

```xpp
str enumStr(enum enum)
```

### <a name="parameters"></a><span data-ttu-id="2274c-339">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-339">Parameters</span></span>

| <span data-ttu-id="2274c-340">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-340">Parameter</span></span> | <span data-ttu-id="2274c-341">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-341">Description</span></span>                  |
|-----------|------------------------------|
| <span data-ttu-id="2274c-342">列挙型</span><span class="sxs-lookup"><span data-stu-id="2274c-342">enum</span></span>      | <span data-ttu-id="2274c-343">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-343">The name of the enumeration.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-344">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-344">Return Value</span></span>

<span data-ttu-id="2274c-345">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-345">The name of the enumeration.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-346">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-346">Remarks</span></span>

<span data-ttu-id="2274c-347">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-347">This is a compile-time function.</span></span> <span data-ttu-id="2274c-348">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-348">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-349">例</span><span class="sxs-lookup"><span data-stu-id="2274c-349">Example</span></span>

```xpp
static void enumStrExample(Args _args)
{
    str s;
    ;
    s = enumStr(ABC);
    print s;
    pause;
}
```

## <a name="extendedtypenum"></a><span data-ttu-id="2274c-350">extendedTypeNum</span><span class="sxs-lookup"><span data-stu-id="2274c-350">extendedTypeNum</span></span>
<span data-ttu-id="2274c-351">指定された拡張データ型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-351">Retrieves the ID of the specified extended data type.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-352">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-352">Syntax</span></span>

```xpp
int extendedTypeNum(int str)
```

### <a name="parameters"></a><span data-ttu-id="2274c-353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-353">Parameters</span></span>

| <span data-ttu-id="2274c-354">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-354">Parameter</span></span> | <span data-ttu-id="2274c-355">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-355">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="2274c-356">str</span><span class="sxs-lookup"><span data-stu-id="2274c-356">str</span></span>       | <span data-ttu-id="2274c-357">ID を返す拡張データ型。</span><span class="sxs-lookup"><span data-stu-id="2274c-357">The extended data type for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-358">Return Value</span></span>

<span data-ttu-id="2274c-359">指定された拡張データ型の ID。</span><span class="sxs-lookup"><span data-stu-id="2274c-359">The ID of the specified extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-360">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-360">Remarks</span></span>

<span data-ttu-id="2274c-361">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-361">This is a compile-time function.</span></span> <span data-ttu-id="2274c-362">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-362">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-363">例</span><span class="sxs-lookup"><span data-stu-id="2274c-363">Example</span></span>

```xpp
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
```

## <a name="extendedtypestr"></a><span data-ttu-id="2274c-364">extendedTypeStr</span><span class="sxs-lookup"><span data-stu-id="2274c-364">extendedTypeStr</span></span>
<span data-ttu-id="2274c-365">文字列として拡張データ型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-365">Retrieves the name of an extended data type as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-366">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-366">Syntax</span></span>

```xpp
str extendedTypeStr(int str)
```

### <a name="parameters"></a><span data-ttu-id="2274c-367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-367">Parameters</span></span>

| <span data-ttu-id="2274c-368">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-368">Parameter</span></span> | <span data-ttu-id="2274c-369">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-369">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="2274c-370">str</span><span class="sxs-lookup"><span data-stu-id="2274c-370">str</span></span>       | <span data-ttu-id="2274c-371">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-371">The name of the extended data type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-372">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-372">Return Value</span></span>

<span data-ttu-id="2274c-373">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-373">The name of the extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-374">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-374">Remarks</span></span>

<span data-ttu-id="2274c-375">リテラル テキストの代わりにこの関数を使用すると、拡張データ型名を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-375">Use this function instead of literal text to return a string that contains the extended data type name.</span></span> <span data-ttu-id="2274c-376">データ タイプが存在しない場合、**extendedTypeStr** 関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="2274c-376">If the data type does not exist, the **extendedTypeStr** function generates a syntax error at compile time.</span></span> <span data-ttu-id="2274c-377">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-377">This is a compile-time function.</span></span> <span data-ttu-id="2274c-378">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-378">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-379">例</span><span class="sxs-lookup"><span data-stu-id="2274c-379">Example</span></span>

```xpp
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
```

## <a name="fieldnum"></a><span data-ttu-id="2274c-380">fieldNum</span><span class="sxs-lookup"><span data-stu-id="2274c-380">fieldNum</span></span>
<span data-ttu-id="2274c-381">指定したフィールドの ID 番号を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-381">Returns the ID number of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-382">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-382">Syntax</span></span>

```xpp
int fieldNum(str tableName, str fieldName)
```

### <a name="parameters"></a><span data-ttu-id="2274c-383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-383">Parameters</span></span>

| <span data-ttu-id="2274c-384">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-384">Parameter</span></span> | <span data-ttu-id="2274c-385">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-385">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="2274c-386">tableName</span><span class="sxs-lookup"><span data-stu-id="2274c-386">tableName</span></span> | <span data-ttu-id="2274c-387">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-387">The name of the table.</span></span> |
| <span data-ttu-id="2274c-388">fieldName</span><span class="sxs-lookup"><span data-stu-id="2274c-388">fieldName</span></span> | <span data-ttu-id="2274c-389">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-389">The name of the field.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-390">Return Value</span></span>

<span data-ttu-id="2274c-391">指定されたフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="2274c-391">The ID of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-392">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-392">Remarks</span></span>

<span data-ttu-id="2274c-393">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-393">This is a compile-time function.</span></span> <span data-ttu-id="2274c-394">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-394">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-395">例</span><span class="sxs-lookup"><span data-stu-id="2274c-395">Example</span></span>

<span data-ttu-id="2274c-396">次の例では、**CashDisc** フィールドの番号を **CustTable** テーブルに出力します。</span><span class="sxs-lookup"><span data-stu-id="2274c-396">The following example prints the number of the **CashDisc** field in the **CustTable** table.</span></span>

```xpp
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
```

## <a name="fieldpname"></a><span data-ttu-id="2274c-397">fieldPName</span><span class="sxs-lookup"><span data-stu-id="2274c-397">fieldPName</span></span>
<span data-ttu-id="2274c-398">指定されたフィールドのラベルを取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-398">Retrieves the label of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-399">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-399">Syntax</span></span>

```xpp
str fieldPName(str tableid, str fieldid)
```

### <a name="parameters"></a><span data-ttu-id="2274c-400">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-400">Parameters</span></span>

| <span data-ttu-id="2274c-401">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-401">Parameter</span></span> | <span data-ttu-id="2274c-402">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-402">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="2274c-403">tableid</span><span class="sxs-lookup"><span data-stu-id="2274c-403">tableid</span></span>   | <span data-ttu-id="2274c-404">指定されたフィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="2274c-404">The table that contains the specified field.</span></span> |
| <span data-ttu-id="2274c-405">fieldid</span><span class="sxs-lookup"><span data-stu-id="2274c-405">fieldid</span></span>   | <span data-ttu-id="2274c-406">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="2274c-406">The field to convert.</span></span>                        |

### <a name="return-value"></a><span data-ttu-id="2274c-407">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-407">Return Value</span></span>

<span data-ttu-id="2274c-408">フィールドのラベル。</span><span class="sxs-lookup"><span data-stu-id="2274c-408">The label of the field.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-409">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-409">Remarks</span></span>

<span data-ttu-id="2274c-410">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-410">This is a compile-time function.</span></span> <span data-ttu-id="2274c-411">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-411">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-412">例</span><span class="sxs-lookup"><span data-stu-id="2274c-412">Example</span></span>

<span data-ttu-id="2274c-413">次の例では、**CashDisc** フィールドのラベルを出力します。</span><span class="sxs-lookup"><span data-stu-id="2274c-413">The following example prints the label of the **CashDisc** field.</span></span>

```xpp
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
```

## <a name="fieldstr"></a><span data-ttu-id="2274c-414">fieldStr</span><span class="sxs-lookup"><span data-stu-id="2274c-414">fieldStr</span></span>
<span data-ttu-id="2274c-415">指定したフィールドのフィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-415">Retrieves the field name of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-416">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-416">Syntax</span></span>

```xpp
str fieldStr(str tableid, str fieldid)
```

### <a name="parameters"></a><span data-ttu-id="2274c-417">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-417">Parameters</span></span>

| <span data-ttu-id="2274c-418">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-418">Parameter</span></span> | <span data-ttu-id="2274c-419">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-419">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="2274c-420">tableid</span><span class="sxs-lookup"><span data-stu-id="2274c-420">tableid</span></span>   | <span data-ttu-id="2274c-421">フィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="2274c-421">The table that contains the field.</span></span> |
| <span data-ttu-id="2274c-422">fieldid</span><span class="sxs-lookup"><span data-stu-id="2274c-422">fieldid</span></span>   | <span data-ttu-id="2274c-423">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="2274c-423">The field to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="2274c-424">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-424">Return Value</span></span>

<span data-ttu-id="2274c-425">指定したフィールドのフィールド名。</span><span class="sxs-lookup"><span data-stu-id="2274c-425">The field name of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-426">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-426">Remarks</span></span>

<span data-ttu-id="2274c-427">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-427">This is a compile-time function.</span></span> <span data-ttu-id="2274c-428">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-428">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-429">例</span><span class="sxs-lookup"><span data-stu-id="2274c-429">Example</span></span>

<span data-ttu-id="2274c-430">次の例では、**CashDisc** フィールドの名前を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2274c-430">The following example assigns the name of the **CashDisc** field to the *myText* variable.</span></span>

```xpp
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
```

## <a name="formcontrolstr"></a><span data-ttu-id="2274c-431">formControlStr</span><span class="sxs-lookup"><span data-stu-id="2274c-431">formControlStr</span></span>
<span data-ttu-id="2274c-432">X++ コンパイラは、コントロールがフォームに存在するかどうかをチェックし、関数呼び出しを有効なコントロール名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2274c-432">Causes the X++ compiler to check whether the control exists on the form, and to replace the function call with a string of the valid control name.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-433">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-433">Syntax</span></span>

```xpp
str formControlStr(formName, controlName)
```

### <a name="parameters"></a><span data-ttu-id="2274c-434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-434">Parameters</span></span>

| <span data-ttu-id="2274c-435">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-435">Parameter</span></span>   | <span data-ttu-id="2274c-436">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-436">Description</span></span>                                                          |
|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="2274c-437">formName</span><span class="sxs-lookup"><span data-stu-id="2274c-437">formName</span></span>    | <span data-ttu-id="2274c-438">引用符ではなく、フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-438">The name of the form, not in quotation marks.</span></span>                        |
| <span data-ttu-id="2274c-439">controlName</span><span class="sxs-lookup"><span data-stu-id="2274c-439">controlName</span></span> | <span data-ttu-id="2274c-440">フォーム上のコントロールの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="2274c-440">The name of the control that is on the form, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-441">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-441">Return Value</span></span>

<span data-ttu-id="2274c-442">アプリケーション エクスプローラーで表示されるコントロールの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-442">A string that contains the name of the control as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-443">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-443">Remarks</span></span>

<span data-ttu-id="2274c-444">コントロールがフォームに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2274c-444">A compile error is issued if the compiler determines that the control does not exist on the form.</span></span> <span data-ttu-id="2274c-445">X++ コードが引用符が含まれる文字列を使用してコントロールの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="2274c-445">If your X++ code uses a string that contains quotation marks to supply the control name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="2274c-446">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="2274c-446">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="2274c-447">コンパイラにより実行される **formControlStr** などの X++ 関数は、コンパイル時関数と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="2274c-447">X++ functions such as **formControlStr** that are executed by the compiler are called compile-time functions or compile-time functions.</span></span> <span data-ttu-id="2274c-448">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="2274c-448">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="2274c-449">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="2274c-449">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="2274c-450">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-450">This is a compile-time function.</span></span> <span data-ttu-id="2274c-451">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-451">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-452">例</span><span class="sxs-lookup"><span data-stu-id="2274c-452">Example</span></span>

<span data-ttu-id="2274c-453">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-453">No example.</span></span>

## <a name="formdatafieldstr"></a><span data-ttu-id="2274c-454">formDataFieldStr</span><span class="sxs-lookup"><span data-stu-id="2274c-454">formDataFieldStr</span></span>
<span data-ttu-id="2274c-455">フォームのデータ フィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-455">Returns the name of a data field in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-456">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-456">Syntax</span></span>

```xpp
str formDataFieldStr(str formName, str dataSource, str dataField)
```

### <a name="parameters"></a><span data-ttu-id="2274c-457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-457">Parameters</span></span>

| <span data-ttu-id="2274c-458">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-458">Parameter</span></span>  | <span data-ttu-id="2274c-459">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-459">Description</span></span>                        |
|------------|------------------------------------|
| <span data-ttu-id="2274c-460">formName</span><span class="sxs-lookup"><span data-stu-id="2274c-460">formName</span></span>   | <span data-ttu-id="2274c-461">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-461">The name of the form.</span></span>              |
| <span data-ttu-id="2274c-462">dataSource</span><span class="sxs-lookup"><span data-stu-id="2274c-462">dataSource</span></span> | <span data-ttu-id="2274c-463">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="2274c-463">The data source of the form.</span></span>       |
| <span data-ttu-id="2274c-464">dataField</span><span class="sxs-lookup"><span data-stu-id="2274c-464">dataField</span></span>  | <span data-ttu-id="2274c-465">データ ソースのデータ フィールド。</span><span class="sxs-lookup"><span data-stu-id="2274c-465">The data field of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-466">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-466">Return Value</span></span>

<span data-ttu-id="2274c-467">フォームのデータ フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-467">The name of a data field in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-468">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-468">Remarks</span></span>

<span data-ttu-id="2274c-469">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-469">This is a compile-time function.</span></span> <span data-ttu-id="2274c-470">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-470">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-471">例</span><span class="sxs-lookup"><span data-stu-id="2274c-471">Example</span></span>

```xpp
str a = formDataFieldStr(FMVehicle, FMModelRate, RatePerDay);
```

## <a name="formdatasourcestr"></a><span data-ttu-id="2274c-472">formDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="2274c-472">formDataSourceStr</span></span>
<span data-ttu-id="2274c-473">フォームのデータ ソースの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-473">Returns the name of a data source in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-474">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-474">Syntax</span></span>

```xpp
str formDataSourceStr(str formName, str dataSource)
```

### <a name="parameters"></a><span data-ttu-id="2274c-475">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-475">Parameters</span></span>

| <span data-ttu-id="2274c-476">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-476">Parameter</span></span>  | <span data-ttu-id="2274c-477">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-477">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="2274c-478">formName</span><span class="sxs-lookup"><span data-stu-id="2274c-478">formName</span></span>   | <span data-ttu-id="2274c-479">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-479">The name of the form.</span></span>        |
| <span data-ttu-id="2274c-480">dataSource</span><span class="sxs-lookup"><span data-stu-id="2274c-480">dataSource</span></span> | <span data-ttu-id="2274c-481">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="2274c-481">The data source of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-482">Return Value</span></span>

<span data-ttu-id="2274c-483">フォームのデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-483">The name of a data source in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-484">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-484">Remarks</span></span>

<span data-ttu-id="2274c-485">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-485">This is a compile-time function.</span></span> <span data-ttu-id="2274c-486">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-486">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-487">例</span><span class="sxs-lookup"><span data-stu-id="2274c-487">Example</span></span>

```xpp
str b = formDataSourceStr(FMVehicle, FMModelRate);
```

## <a name="formmethodstr"></a><span data-ttu-id="2274c-488">formMethodStr</span><span class="sxs-lookup"><span data-stu-id="2274c-488">formMethodStr</span></span>
<span data-ttu-id="2274c-489">フォームのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-489">Returns the name of a method of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-490">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-490">Syntax</span></span>

```xpp
str formMethodStr(str formName, str methodName)
```

### <a name="parameters"></a><span data-ttu-id="2274c-491">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-491">Parameters</span></span>

| <span data-ttu-id="2274c-492">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-492">Parameter</span></span>  | <span data-ttu-id="2274c-493">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-493">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="2274c-494">formName</span><span class="sxs-lookup"><span data-stu-id="2274c-494">formName</span></span>   | <span data-ttu-id="2274c-495">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-495">The name of the form.</span></span>   |
| <span data-ttu-id="2274c-496">methodName</span><span class="sxs-lookup"><span data-stu-id="2274c-496">methodName</span></span> | <span data-ttu-id="2274c-497">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="2274c-497">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-498">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-498">Return Value</span></span>

<span data-ttu-id="2274c-499">フォームのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-499">The name of a method in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-500">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-500">Remarks</span></span>

<span data-ttu-id="2274c-501">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-501">This is a compile-time function.</span></span> <span data-ttu-id="2274c-502">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-502">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-503">例</span><span class="sxs-lookup"><span data-stu-id="2274c-503">Example</span></span>

<span data-ttu-id="2274c-504">次の例では、**showDialog** メソッドの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="2274c-504">The following example prints the name of the **showDialog** method.</span></span>

```xpp
str c = formMethodStr(Batch,showDialog);
```

## <a name="formstr"></a><span data-ttu-id="2274c-505">formStr</span><span class="sxs-lookup"><span data-stu-id="2274c-505">formStr</span></span>
<span data-ttu-id="2274c-506">フォームの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-506">Retrieves the name of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-507">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-507">Syntax</span></span>

```xpp
str formStr(str form)
```

### <a name="parameters"></a><span data-ttu-id="2274c-508">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-508">Parameters</span></span>

| <span data-ttu-id="2274c-509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-509">Parameter</span></span> | <span data-ttu-id="2274c-510">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-510">Description</span></span>         |
|-----------|---------------------|
| <span data-ttu-id="2274c-511">フォーム</span><span class="sxs-lookup"><span data-stu-id="2274c-511">form</span></span>      | <span data-ttu-id="2274c-512">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-512">The name of a form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-513">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-513">Return Value</span></span>

<span data-ttu-id="2274c-514">フォームの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-514">A string that represents the name of the form.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-515">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-515">Remarks</span></span>

<span data-ttu-id="2274c-516">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-516">This is a compile-time function.</span></span> <span data-ttu-id="2274c-517">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-517">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-518">例</span><span class="sxs-lookup"><span data-stu-id="2274c-518">Example</span></span>

<span data-ttu-id="2274c-519">次の例では、InventDim フォームの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="2274c-519">The following example prints the name of the InventDim form.</span></span>

```xpp
static void formStrExample(Args _arg)
{
    ;

    Global::info(formStr(InventDim));
}
/****Infolog Display
Message (11:04:39 am)
InventDim
****/
```

## <a name="identifierstr"></a><span data-ttu-id="2274c-520">identifierStr</span><span class="sxs-lookup"><span data-stu-id="2274c-520">identifierStr</span></span>
<span data-ttu-id="2274c-521">指定された識別子を文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="2274c-521">Converts the specified identifier to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-522">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-522">Syntax</span></span>

```xpp
str identifierStr(str ident)
```

### <a name="parameters"></a><span data-ttu-id="2274c-523">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-523">Parameters</span></span>

| <span data-ttu-id="2274c-524">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-524">Parameter</span></span> | <span data-ttu-id="2274c-525">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-525">Description</span></span>                |
|-----------|----------------------------|
| <span data-ttu-id="2274c-526">ident</span><span class="sxs-lookup"><span data-stu-id="2274c-526">ident</span></span>     | <span data-ttu-id="2274c-527">変換する ID。</span><span class="sxs-lookup"><span data-stu-id="2274c-527">The identifier to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-528">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-528">Return Value</span></span>

<span data-ttu-id="2274c-529">指定した ID を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-529">A string that represents the specified identifier.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-530">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-530">Remarks</span></span>

<span data-ttu-id="2274c-531">**identifierStr** 関数使用する場合、ベスト プラクティス警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2274c-531">You will receive a best practice warning if you use the **identifierStr** function.</span></span> <span data-ttu-id="2274c-532">これは、**identifierStr** に対して存在チェックが実行されたために発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-532">This occurs because existence checking is performed for **identifierStr**.</span></span> <span data-ttu-id="2274c-533">使用可能な場合は、より具体的なコンパイル時の関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-533">Try to use a more specific compile-time function if one is available.</span></span> <span data-ttu-id="2274c-534">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-534">This is a compile-time function.</span></span> <span data-ttu-id="2274c-535">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-535">For more information, [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-536">例</span><span class="sxs-lookup"><span data-stu-id="2274c-536">Example</span></span>

<span data-ttu-id="2274c-537">次のコード例では、*myvar* 変数名を *thevar* 変数に割り当てています。</span><span class="sxs-lookup"><span data-stu-id="2274c-537">The following code example assigns the *myvar* variable name to the *thevar* variable.</span></span>

```xpp
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
```

## <a name="indexnum"></a><span data-ttu-id="2274c-538">indexNum</span><span class="sxs-lookup"><span data-stu-id="2274c-538">indexNum</span></span>
<span data-ttu-id="2274c-539">指定されたインデックスを数字に変換します。</span><span class="sxs-lookup"><span data-stu-id="2274c-539">Converts the specified index to a number.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-540">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-540">Syntax</span></span>

```xpp
int indexNum(str tableid, str indexid)
```

### <a name="parameters"></a><span data-ttu-id="2274c-541">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-541">Parameters</span></span>

| <span data-ttu-id="2274c-542">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-542">Parameter</span></span> | <span data-ttu-id="2274c-543">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-543">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="2274c-544">tableid</span><span class="sxs-lookup"><span data-stu-id="2274c-544">tableid</span></span>   | <span data-ttu-id="2274c-545">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="2274c-545">The table that contains the index.</span></span> |
| <span data-ttu-id="2274c-546">indexid</span><span class="sxs-lookup"><span data-stu-id="2274c-546">indexid</span></span>   | <span data-ttu-id="2274c-547">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="2274c-547">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="2274c-548">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-548">Return Value</span></span>

<span data-ttu-id="2274c-549">指定されたインデックスを表すインデックス番号。</span><span class="sxs-lookup"><span data-stu-id="2274c-549">The index number that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-550">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-550">Remarks</span></span>

<span data-ttu-id="2274c-551">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-551">This is a compile-time function.</span></span> <span data-ttu-id="2274c-552">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-552">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-553">例</span><span class="sxs-lookup"><span data-stu-id="2274c-553">Example</span></span>

<span data-ttu-id="2274c-554">次の例では、当事者インデックスのインデックス値を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-554">The following example returns the index value of the Party index.</span></span>

```xpp
static void indexNumExample(Args _arg)
{
    ;

    Global::info(strfmt("%1 is the index number of Party.", indexNum(CustTable, Party)));
}
/****Infolog Display
Message (11:28:03 am)
3 is the index number of Party.
****/
```

## <a name="indexstr"></a><span data-ttu-id="2274c-555">indexStr</span><span class="sxs-lookup"><span data-stu-id="2274c-555">indexStr</span></span>
<span data-ttu-id="2274c-556">指定されたインデックスを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="2274c-556">Converts the specified index to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-557">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-557">Syntax</span></span>

```xpp
str indexStr(str tableid, str indexid)
```

### <a name="parameters"></a><span data-ttu-id="2274c-558">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-558">Parameters</span></span>

| <span data-ttu-id="2274c-559">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-559">Parameter</span></span> | <span data-ttu-id="2274c-560">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-560">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="2274c-561">tableid</span><span class="sxs-lookup"><span data-stu-id="2274c-561">tableid</span></span>   | <span data-ttu-id="2274c-562">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="2274c-562">The table that contains the index.</span></span> |
| <span data-ttu-id="2274c-563">indexid</span><span class="sxs-lookup"><span data-stu-id="2274c-563">indexid</span></span>   | <span data-ttu-id="2274c-564">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="2274c-564">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="2274c-565">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-565">Return Value</span></span>

<span data-ttu-id="2274c-566">指定インデックスを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-566">A string that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-567">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-567">Remarks</span></span>

<span data-ttu-id="2274c-568">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-568">This is a compile-time function.</span></span> <span data-ttu-id="2274c-569">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-569">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-570">例</span><span class="sxs-lookup"><span data-stu-id="2274c-570">Example</span></span>

<span data-ttu-id="2274c-571">次の例では、**CashDisc** インデックス値を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2274c-571">The following example assigns the **CashDisc** index value to the *myText* variable.</span></span>

```xpp
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
```

## <a name="licensecodenum"></a><span data-ttu-id="2274c-572">licenseCodeNum</span><span class="sxs-lookup"><span data-stu-id="2274c-572">licenseCodeNum</span></span>
<span data-ttu-id="2274c-573">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-573">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-574">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-574">Syntax</span></span>

```xpp
int licenseCodeNum(str codename)
```

### <a name="parameters"></a><span data-ttu-id="2274c-575">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-575">Parameters</span></span>

| <span data-ttu-id="2274c-576">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-576">Parameter</span></span> | <span data-ttu-id="2274c-577">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-577">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="2274c-578">codename</span><span class="sxs-lookup"><span data-stu-id="2274c-578">codename</span></span>  | <span data-ttu-id="2274c-579">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-579">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-580">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-580">Return Value</span></span>

<span data-ttu-id="2274c-581">指定されたライセンス コードの数。</span><span class="sxs-lookup"><span data-stu-id="2274c-581">The number of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-582">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-582">Remarks</span></span>

<span data-ttu-id="2274c-583">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-583">This is a compile-time function.</span></span> <span data-ttu-id="2274c-584">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-584">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-585">例</span><span class="sxs-lookup"><span data-stu-id="2274c-585">Example</span></span>

```xpp
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
```

## <a name="licensecodestr"></a><span data-ttu-id="2274c-586">licenseCodeStr</span><span class="sxs-lookup"><span data-stu-id="2274c-586">licenseCodeStr</span></span>
<span data-ttu-id="2274c-587">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-587">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-588">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-588">Syntax</span></span>

```xpp
str licenseCodeStr(str codename)
```

### <a name="parameters"></a><span data-ttu-id="2274c-589">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-589">Parameters</span></span>

| <span data-ttu-id="2274c-590">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-590">Parameter</span></span> | <span data-ttu-id="2274c-591">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-591">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="2274c-592">codename</span><span class="sxs-lookup"><span data-stu-id="2274c-592">codename</span></span>  | <span data-ttu-id="2274c-593">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-593">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-594">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-594">Return Value</span></span>

<span data-ttu-id="2274c-595">指定されたライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-595">The name of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-596">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-596">Remarks</span></span>

<span data-ttu-id="2274c-597">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-597">This is a compile-time function.</span></span> <span data-ttu-id="2274c-598">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-598">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-599">例</span><span class="sxs-lookup"><span data-stu-id="2274c-599">Example</span></span>

```xpp
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
```

## <a name="literalstr"></a><span data-ttu-id="2274c-600">literalStr</span><span class="sxs-lookup"><span data-stu-id="2274c-600">literalStr</span></span>
<span data-ttu-id="2274c-601">指定した文字列がリテラル文字列であることを検証します。そうでない場合は、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-601">Validates that the specified string can be a literal string; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-602">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-602">Syntax</span></span>

```xpp
str literalStr(int str)
```

### <a name="parameters"></a><span data-ttu-id="2274c-603">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-603">Parameters</span></span>

| <span data-ttu-id="2274c-604">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-604">Parameter</span></span> | <span data-ttu-id="2274c-605">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-605">Description</span></span>             |
|-----------|-------------------------|
| <span data-ttu-id="2274c-606">codename</span><span class="sxs-lookup"><span data-stu-id="2274c-606">codename</span></span>  | <span data-ttu-id="2274c-607">検証する文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-607">The string to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-608">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-608">Return Value</span></span>

<span data-ttu-id="2274c-609">有効な場合は、リテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-609">The literal string if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-610">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-610">Remarks</span></span>

<span data-ttu-id="2274c-611">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-611">This is a compile-time function.</span></span> <span data-ttu-id="2274c-612">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-612">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-613">例</span><span class="sxs-lookup"><span data-stu-id="2274c-613">Example</span></span>

```xpp
{
    str s;
    ;

    s = literalStr("This is a literal str");
    print s;
    pause;
}
```

## <a name="maxdate"></a><span data-ttu-id="2274c-614">maxDate</span><span class="sxs-lookup"><span data-stu-id="2274c-614">maxDate</span></span>
<span data-ttu-id="2274c-615">日付型の変数に使用できる最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-615">Retrieves the maximum value allowed for a variable of type date.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-616">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-616">Syntax</span></span>

```xpp
date maxDate()
```

### <a name="return-value"></a><span data-ttu-id="2274c-617">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-617">Return Value</span></span>

<span data-ttu-id="2274c-618">**日付** の変数に使用できる最大値は、**2154-12-31**です。</span><span class="sxs-lookup"><span data-stu-id="2274c-618">The maximum value allowed for a variable of type **date**, which is **2154-12-31**.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-619">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-619">Remarks</span></span>

<span data-ttu-id="2274c-620">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-620">This is a compile-time function.</span></span> <span data-ttu-id="2274c-621">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-621">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-622">例</span><span class="sxs-lookup"><span data-stu-id="2274c-622">Example</span></span>

```xpp
static void maxDateExample(Args _arg)
{
    date maximumDate;
    ;
    maximumDate = maxDate();
    print maximumDate;
    pause;
}
```

## <a name="maxint"></a><span data-ttu-id="2274c-623">maxInt</span><span class="sxs-lookup"><span data-stu-id="2274c-623">maxInt</span></span>
<span data-ttu-id="2274c-624">**int** 型に格納可能な最大符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-624">Retrieves the maximum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-625">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-625">Syntax</span></span>

```xpp
int maxInt()
```

### <a name="return-value"></a><span data-ttu-id="2274c-626">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-626">Return Value</span></span>

<span data-ttu-id="2274c-627">整数の許容値の最大値。</span><span class="sxs-lookup"><span data-stu-id="2274c-627">The maximum value allowed value of an integer.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-628">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-628">Remarks</span></span>

<span data-ttu-id="2274c-629">その他の整数値は、戻り値以下になります。</span><span class="sxs-lookup"><span data-stu-id="2274c-629">Any other integer will be less than or equal to the returned value.</span></span> <span data-ttu-id="2274c-630">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-630">This is a compile-time function.</span></span> <span data-ttu-id="2274c-631">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-631">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-632">例</span><span class="sxs-lookup"><span data-stu-id="2274c-632">Example</span></span>

```xpp
static void maxIntExample(Args _arg)
{
    int i;
    ;
    print "The maximum value for type int is " + int2Str(maxInt());
    pause;
}
```

## <a name="measurementstr"></a><span data-ttu-id="2274c-633">measurementStr</span><span class="sxs-lookup"><span data-stu-id="2274c-633">measurementStr</span></span>
<span data-ttu-id="2274c-634">測定の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-634">Returns the name of a measurement.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-635">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-635">Syntax</span></span>

```xpp
str measurementStr(str measurement)
```

### <a name="parameters"></a><span data-ttu-id="2274c-636">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-636">Parameters</span></span>

| <span data-ttu-id="2274c-637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-637">Parameter</span></span>   | <span data-ttu-id="2274c-638">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-638">Description</span></span>                  |
|-------------|------------------------------|
| <span data-ttu-id="2274c-639">測定値</span><span class="sxs-lookup"><span data-stu-id="2274c-639">measurement</span></span> | <span data-ttu-id="2274c-640">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-640">The name of the measurement.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-641">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-641">Return Value</span></span>

<span data-ttu-id="2274c-642">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-642">The name of the measurement.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-643">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-643">Remarks</span></span>

<span data-ttu-id="2274c-644">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-644">This is a compile-time function.</span></span> <span data-ttu-id="2274c-645">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-645">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-646">例</span><span class="sxs-lookup"><span data-stu-id="2274c-646">Example</span></span>

<span data-ttu-id="2274c-647">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-647">No example.</span></span>

## <a name="measurestr"></a><span data-ttu-id="2274c-648">measureStr</span><span class="sxs-lookup"><span data-stu-id="2274c-648">measureStr</span></span>
<span data-ttu-id="2274c-649">メジャーの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-649">Returns the name of a measure.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-650">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-650">Syntax</span></span>

```xpp
str measureStr(str measure)
```

### <a name="parameters"></a><span data-ttu-id="2274c-651">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-651">Parameters</span></span>

| <span data-ttu-id="2274c-652">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-652">Parameter</span></span> | <span data-ttu-id="2274c-653">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-653">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="2274c-654">測定</span><span class="sxs-lookup"><span data-stu-id="2274c-654">measure</span></span>   | <span data-ttu-id="2274c-655">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-655">The name of the measure.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-656">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-656">Return Value</span></span>

<span data-ttu-id="2274c-657">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-657">The name of the measure.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-658">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-658">Remarks</span></span>

<span data-ttu-id="2274c-659">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-659">This is a compile-time function.</span></span> <span data-ttu-id="2274c-660">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-660">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-661">例</span><span class="sxs-lookup"><span data-stu-id="2274c-661">Example</span></span>

<span data-ttu-id="2274c-662">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-662">No example.</span></span>

## <a name="menuitemactionstr"></a><span data-ttu-id="2274c-663">menuItemActionStr</span><span class="sxs-lookup"><span data-stu-id="2274c-663">menuItemActionStr</span></span>
<span data-ttu-id="2274c-664">指定したメニュー項目のアクションがアプリケーション オブジェクト ツリー (Application Explorer) に存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-664">Validates that the specified menu item action exists in the Application Object Tree (Application Explorer); if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-665">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-665">Syntax</span></span>

```xpp
str menuItemActionStr(class menuitem)
```

### <a name="parameters"></a><span data-ttu-id="2274c-666">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-666">Parameters</span></span>

| <span data-ttu-id="2274c-667">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-667">Parameter</span></span> | <span data-ttu-id="2274c-668">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-668">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="2274c-669">codename</span><span class="sxs-lookup"><span data-stu-id="2274c-669">codename</span></span>  | <span data-ttu-id="2274c-670">検証するメニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-670">The name of the menu item action to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-671">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-671">Return Value</span></span>

<span data-ttu-id="2274c-672">有効な場合の、メニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-672">The name of the menu item action, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-673">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-673">Remarks</span></span>

<span data-ttu-id="2274c-674">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-674">This is a compile-time function.</span></span> <span data-ttu-id="2274c-675">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-675">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-676">例</span><span class="sxs-lookup"><span data-stu-id="2274c-676">Example</span></span>

```xpp
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
```

## <a name="menuitemdisplaystr"></a><span data-ttu-id="2274c-677">menuItemDisplayStr</span><span class="sxs-lookup"><span data-stu-id="2274c-677">menuItemDisplayStr</span></span>
<span data-ttu-id="2274c-678">指定したメニュー項目の表示がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-678">Validates that the specified menu item display exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-679">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-679">Syntax</span></span>

```xpp
str menuitemdisplaystr(class menuItem)
```

### <a name="parameters"></a><span data-ttu-id="2274c-680">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-680">Parameters</span></span>

| <span data-ttu-id="2274c-681">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-681">Parameter</span></span> | <span data-ttu-id="2274c-682">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-682">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="2274c-683">codename</span><span class="sxs-lookup"><span data-stu-id="2274c-683">codename</span></span>  | <span data-ttu-id="2274c-684">検証するメニュー項目nの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-684">The name of the menu item display to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-685">Return Value</span></span>

<span data-ttu-id="2274c-686">有効な場合の、指定されたメニューの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-686">The name of the specified menu item display, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-687">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-687">Remarks</span></span>

<span data-ttu-id="2274c-688">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-688">This is a compile-time function.</span></span> <span data-ttu-id="2274c-689">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-689">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-690">例</span><span class="sxs-lookup"><span data-stu-id="2274c-690">Example</span></span>

```xpp
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
```

## <a name="menuitemoutputstr"></a><span data-ttu-id="2274c-691">menuItemOutputStr</span><span class="sxs-lookup"><span data-stu-id="2274c-691">menuItemOutputStr</span></span>
<span data-ttu-id="2274c-692">指定したメニュー項目の出力がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-692">Validates that the specified menu item output exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-693">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-693">Syntax</span></span>

```xpp
str menuItemOutputStr(class menuitem)
```

### <a name="parameters"></a><span data-ttu-id="2274c-694">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-694">Parameters</span></span>

| <span data-ttu-id="2274c-695">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-695">Parameter</span></span> | <span data-ttu-id="2274c-696">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-696">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="2274c-697">codename</span><span class="sxs-lookup"><span data-stu-id="2274c-697">codename</span></span>  | <span data-ttu-id="2274c-698">検証するメニュー項目出力の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-698">The name of the menu item output to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-699">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-699">Return Value</span></span>

<span data-ttu-id="2274c-700">有効な場合、指定されたメニュー項目が出力されます。</span><span class="sxs-lookup"><span data-stu-id="2274c-700">The specified menu item output if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-701">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-701">Remarks</span></span>

<span data-ttu-id="2274c-702">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-702">This is a compile-time function.</span></span> <span data-ttu-id="2274c-703">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-703">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-704">例</span><span class="sxs-lookup"><span data-stu-id="2274c-704">Example</span></span>

```xpp
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
```

## <a name="menustr"></a><span data-ttu-id="2274c-705">menuStr</span><span class="sxs-lookup"><span data-stu-id="2274c-705">menuStr</span></span>
<span data-ttu-id="2274c-706">指定したメニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-706">Validates that the specified menu exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-707">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-707">Syntax</span></span>

```xpp
str menuStr(class menu)
```

### <a name="parameters"></a><span data-ttu-id="2274c-708">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-708">Parameters</span></span>

| <span data-ttu-id="2274c-709">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-709">Parameter</span></span> | <span data-ttu-id="2274c-710">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-710">Description</span></span>                       |
|-----------|-----------------------------------|
| <span data-ttu-id="2274c-711">メニュー</span><span class="sxs-lookup"><span data-stu-id="2274c-711">menu</span></span>      | <span data-ttu-id="2274c-712">検証するメニューの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-712">The name of the menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-713">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-713">Return Value</span></span>

<span data-ttu-id="2274c-714">有効な場合の指定されたメニュー項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-714">The name of the specified menu item if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-715">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-715">Remarks</span></span>

<span data-ttu-id="2274c-716">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-716">This is a compile-time function.</span></span> <span data-ttu-id="2274c-717">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-717">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-718">例</span><span class="sxs-lookup"><span data-stu-id="2274c-718">Example</span></span>

```xpp
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
```

## <a name="methodstr"></a><span data-ttu-id="2274c-719">methodStr</span><span class="sxs-lookup"><span data-stu-id="2274c-719">methodStr</span></span>
<span data-ttu-id="2274c-720">指定したメソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-720">Validates that the specified method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-721">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-721">Syntax</span></span>

```xpp
str methodStr(class class, int method)
```

### <a name="parameters"></a><span data-ttu-id="2274c-722">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-722">Parameters</span></span>

| <span data-ttu-id="2274c-723">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-723">Parameter</span></span> | <span data-ttu-id="2274c-724">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-724">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="2274c-725">クラス</span><span class="sxs-lookup"><span data-stu-id="2274c-725">class</span></span>     | <span data-ttu-id="2274c-726">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-726">The name of the class.</span></span>              |
| <span data-ttu-id="2274c-727">メソッド</span><span class="sxs-lookup"><span data-stu-id="2274c-727">method</span></span>    | <span data-ttu-id="2274c-728">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-728">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-729">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-729">Return Value</span></span>

<span data-ttu-id="2274c-730">有効な場合の、指定されたメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-730">The name of the specified method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-731">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-731">Remarks</span></span>

<span data-ttu-id="2274c-732">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-732">This is a compile-time function.</span></span> <span data-ttu-id="2274c-733">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-733">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-734">例</span><span class="sxs-lookup"><span data-stu-id="2274c-734">Example</span></span>

```xpp
{
    #define.timeout(50)
    str s;
    SysHelpInitTimeOut SysHelpInitTimeOut;
    ;

    s = methodStr(SysHelpInitTimeOut, timeout);
    print s;
    pause;
}
```

## <a name="minint"></a><span data-ttu-id="2274c-735">minInt</span><span class="sxs-lookup"><span data-stu-id="2274c-735">minInt</span></span>
<span data-ttu-id="2274c-736">**int** 型に格納可能な最小符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-736">Retrieves the minimum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-737">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-737">Syntax</span></span>

```xpp
int minInt()
```

### <a name="return-value"></a><span data-ttu-id="2274c-738">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-738">Return Value</span></span>

<span data-ttu-id="2274c-739">**int** 型の最小値です。</span><span class="sxs-lookup"><span data-stu-id="2274c-739">The minimum value of an **int** type.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-740">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-740">Remarks</span></span>

<span data-ttu-id="2274c-741">その他の整数値は、戻り値以上になります。</span><span class="sxs-lookup"><span data-stu-id="2274c-741">Any other integer value will be greater than or equal to the returned value.</span></span> <span data-ttu-id="2274c-742">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-742">This is a compile-time function.</span></span> <span data-ttu-id="2274c-743">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-743">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-744">例</span><span class="sxs-lookup"><span data-stu-id="2274c-744">Example</span></span>

```xpp
static void minIntExample(Args _arg)
{
    int i;
    ;
    i = minInt();
    print "minInt() is " + int2Str(i);    
    pause;
}
```

## <a name="privilegestr"></a><span data-ttu-id="2274c-745">privilegeStr</span><span class="sxs-lookup"><span data-stu-id="2274c-745">privilegeStr</span></span>
<span data-ttu-id="2274c-746">権限の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-746">Returns the name of the privilege.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-747">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-747">Syntax</span></span>

```xpp
str privilegeStr(str privilege)
```

### <a name="parameters"></a><span data-ttu-id="2274c-748">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-748">Parameters</span></span>

| <span data-ttu-id="2274c-749">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-749">Parameter</span></span> | <span data-ttu-id="2274c-750">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-750">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="2274c-751">権限</span><span class="sxs-lookup"><span data-stu-id="2274c-751">privilege</span></span> | <span data-ttu-id="2274c-752">名前を返す対象の特権。</span><span class="sxs-lookup"><span data-stu-id="2274c-752">The privilege for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-753">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-753">Return Value</span></span>

<span data-ttu-id="2274c-754">権限の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-754">The name of the privilege.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-755">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-755">Remarks</span></span>

<span data-ttu-id="2274c-756">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-756">This is a compile-time function.</span></span> <span data-ttu-id="2274c-757">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-757">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-758">例</span><span class="sxs-lookup"><span data-stu-id="2274c-758">Example</span></span>

<span data-ttu-id="2274c-759">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-759">No example.</span></span>

## <a name="querydatasourcestr"></a><span data-ttu-id="2274c-760">queryDatasourceStr</span><span class="sxs-lookup"><span data-stu-id="2274c-760">queryDatasourceStr</span></span>
<span data-ttu-id="2274c-761">X++ コンパイラは、データ ソースがクエリに存在するかどうかをチェックし、関数呼び出しを有効なデータ ソース名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2274c-761">Causes the X++ compiler to check whether the data source exists on the query, and to replace the function call with a string of the valid data source name.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-762">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-762">Syntax</span></span>

```xpp
str queryDataSourceStr(queryName, dataSourceName)
```

### <a name="parameters"></a><span data-ttu-id="2274c-763">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-763">Parameters</span></span>

| <span data-ttu-id="2274c-764">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-764">Parameter</span></span>      | <span data-ttu-id="2274c-765">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-765">Description</span></span>                                                               |
|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="2274c-766">queryName</span><span class="sxs-lookup"><span data-stu-id="2274c-766">queryName</span></span>      | <span data-ttu-id="2274c-767">引用符ではなく、クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-767">The name of the query, not in quotation marks.</span></span>                            |
| <span data-ttu-id="2274c-768">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="2274c-768">dataSourceName</span></span> | <span data-ttu-id="2274c-769">クエリ上のデータ ソースの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="2274c-769">The name of the data source that is on the query, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-770">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-770">Return Value</span></span>

<span data-ttu-id="2274c-771">アプリケーション エクスプローラーで表示されるデータ ソースの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-771">A string that contains the name of the data source as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-772">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-772">Remarks</span></span>

<span data-ttu-id="2274c-773">データ ソースがクエリに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2274c-773">A compile error is issued if the compiler determines that the data source does not exist on the query.</span></span> <span data-ttu-id="2274c-774">X++ コードが引用符が含まれる文字列を使用してデータ ソースの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="2274c-774">If your X++ code uses a string that contains quotation marks to supply the data source name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="2274c-775">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="2274c-775">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="2274c-776">コンパイラにより実行される **queryDataSourceStr** などの X++ 関数は、コンパイル時関数とみなされます。</span><span class="sxs-lookup"><span data-stu-id="2274c-776">X++ functions such as **queryDataSourceStr** that are executed by the compiler are referred to as compile-time functions or compile-time functions.</span></span> <span data-ttu-id="2274c-777">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="2274c-777">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="2274c-778">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="2274c-778">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="2274c-779">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-779">This is a compile-time function.</span></span> <span data-ttu-id="2274c-780">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-780">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-781">例</span><span class="sxs-lookup"><span data-stu-id="2274c-781">Example</span></span>

<span data-ttu-id="2274c-782">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-782">No example.</span></span>

## <a name="querymethodstr"></a><span data-ttu-id="2274c-783">queryMethodStr</span><span class="sxs-lookup"><span data-stu-id="2274c-783">queryMethodStr</span></span>
<span data-ttu-id="2274c-784">クエリのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-784">Returns the name of a method of a query.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-785">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-785">Syntax</span></span>

```xpp
str queryMethodStr(str queryName, str methodName)
```

### <a name="parameters"></a><span data-ttu-id="2274c-786">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-786">Parameters</span></span>

| <span data-ttu-id="2274c-787">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-787">Parameter</span></span>  | <span data-ttu-id="2274c-788">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-788">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="2274c-789">queryName</span><span class="sxs-lookup"><span data-stu-id="2274c-789">queryName</span></span>  | <span data-ttu-id="2274c-790">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-790">The name of the query.</span></span>  |
| <span data-ttu-id="2274c-791">methodName</span><span class="sxs-lookup"><span data-stu-id="2274c-791">methodName</span></span> | <span data-ttu-id="2274c-792">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="2274c-792">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-793">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-793">Return Value</span></span>

<span data-ttu-id="2274c-794">クエリのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-794">The name of a method in a query.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-795">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-795">Remarks</span></span>

<span data-ttu-id="2274c-796">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-796">This is a compile-time function.</span></span> <span data-ttu-id="2274c-797">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-797">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-798">例</span><span class="sxs-lookup"><span data-stu-id="2274c-798">Example</span></span>

<span data-ttu-id="2274c-799">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-799">No example.</span></span>

## <a name="querystr"></a><span data-ttu-id="2274c-800">queryStr</span><span class="sxs-lookup"><span data-stu-id="2274c-800">queryStr</span></span>
<span data-ttu-id="2274c-801">既存のクエリを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-801">Retrieves a string that represents an existing query.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-802">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-802">Syntax</span></span>

```xpp
str queryStr(str query)
```

### <a name="parameters"></a><span data-ttu-id="2274c-803">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-803">Parameters</span></span>

| <span data-ttu-id="2274c-804">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-804">Parameter</span></span> | <span data-ttu-id="2274c-805">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-805">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="2274c-806">クエリ</span><span class="sxs-lookup"><span data-stu-id="2274c-806">query</span></span>     | <span data-ttu-id="2274c-807">取得するクエリ。</span><span class="sxs-lookup"><span data-stu-id="2274c-807">The query to retrieve.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-808">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-808">Return Value</span></span>

<span data-ttu-id="2274c-809">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-809">The name of the query.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-810">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-810">Remarks</span></span>

<span data-ttu-id="2274c-811">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-811">This is a compile-time function.</span></span> <span data-ttu-id="2274c-812">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-812">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-813">例</span><span class="sxs-lookup"><span data-stu-id="2274c-813">Example</span></span>

```xpp
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
```

## <a name="reportstr"></a><span data-ttu-id="2274c-814">reportStr</span><span class="sxs-lookup"><span data-stu-id="2274c-814">reportStr</span></span>
<span data-ttu-id="2274c-815">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-815">Retrieves a string that represents the name of the specified report.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-816">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-816">Syntax</span></span>

```xpp
str reportStr(str report)
```

### <a name="parameters"></a><span data-ttu-id="2274c-817">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-817">Parameters</span></span>

| <span data-ttu-id="2274c-818">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-818">Parameter</span></span> | <span data-ttu-id="2274c-819">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-819">Description</span></span>                              |
|-----------|------------------------------------------|
| <span data-ttu-id="2274c-820">レポート</span><span class="sxs-lookup"><span data-stu-id="2274c-820">report</span></span>    | <span data-ttu-id="2274c-821">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="2274c-821">The report for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-822">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-822">Return Value</span></span>

<span data-ttu-id="2274c-823">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-823">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-824">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-824">Remarks</span></span>

<span data-ttu-id="2274c-825">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-825">This is a compile-time function.</span></span> <span data-ttu-id="2274c-826">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-826">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-827">例</span><span class="sxs-lookup"><span data-stu-id="2274c-827">Example</span></span>

<span data-ttu-id="2274c-828">次の例では、**AssetAddition** レポートの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2274c-828">The following example assigns the name of the **AssetAddition** report to the *MyTxt* variable.</span></span>

```xpp
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
```

## <a name="resourcestr"></a><span data-ttu-id="2274c-829">resourceStr</span><span class="sxs-lookup"><span data-stu-id="2274c-829">resourceStr</span></span>
<span data-ttu-id="2274c-830">指定したリソースがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-830">Validates that the specified resource exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-831">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-831">Syntax</span></span>

```xpp
str resourceStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="2274c-832">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-832">Parameters</span></span>

| <span data-ttu-id="2274c-833">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-833">Parameter</span></span>    | <span data-ttu-id="2274c-834">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-834">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="2274c-835">resourcename</span><span class="sxs-lookup"><span data-stu-id="2274c-835">resourcename</span></span> | <span data-ttu-id="2274c-836">検証するリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-836">The name of the resource to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-837">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-837">Return Value</span></span>

<span data-ttu-id="2274c-838">有効な場合の、指定されたリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-838">The name of the specified resource, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-839">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-839">Remarks</span></span>

<span data-ttu-id="2274c-840">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-840">This is a compile-time function.</span></span> <span data-ttu-id="2274c-841">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-841">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-842">例</span><span class="sxs-lookup"><span data-stu-id="2274c-842">Example</span></span>

```xpp
{
    print "Str for resource StyleSheet_Help_Axapta is " 
        + resourceStr(StyleSheet_Help_Axapta);
    pause;
}
```

## <a name="rolestr"></a><span data-ttu-id="2274c-843">roleStr</span><span class="sxs-lookup"><span data-stu-id="2274c-843">roleStr</span></span>
<span data-ttu-id="2274c-844">指定したセキュリティ ロールの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-844">Retrieves a string that represents the name of the specified security role.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-845">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-845">Syntax</span></span>

```xpp
str roleStr(str securityRole)
```

### <a name="parameters"></a><span data-ttu-id="2274c-846">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-846">Parameters</span></span>

| <span data-ttu-id="2274c-847">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-847">Parameter</span></span>    | <span data-ttu-id="2274c-848">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-848">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="2274c-849">securityRole</span><span class="sxs-lookup"><span data-stu-id="2274c-849">securityRole</span></span> | <span data-ttu-id="2274c-850">セキュリティ ロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="2274c-850">The name of the security role.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-851">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-851">Return Value</span></span>

<span data-ttu-id="2274c-852">文字列のセキュリティ ロールの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-852">The name of the security role in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-853">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-853">Remarks</span></span>

<span data-ttu-id="2274c-854">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-854">This is a compile-time function.</span></span> <span data-ttu-id="2274c-855">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-855">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-856">例</span><span class="sxs-lookup"><span data-stu-id="2274c-856">Example</span></span>

<span data-ttu-id="2274c-857">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-857">No example.</span></span>

## <a name="ssrsreportstr"></a><span data-ttu-id="2274c-858">ssrsReportStr</span><span class="sxs-lookup"><span data-stu-id="2274c-858">ssrsReportStr</span></span>
<span data-ttu-id="2274c-859">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-859">Retrieves a string that represents the name of the specified report.</span></span> <span data-ttu-id="2274c-860">レポート コントローラー クラスで実行されるレポートを指定する場合は、この関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="2274c-860">Use this function when you want to specify the report that should be run by a report controller class.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-861">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-861">Syntax</span></span>

```xpp
str ssrsReportStr(str report, str design)
```

### <a name="parameters"></a><span data-ttu-id="2274c-862">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-862">Parameters</span></span>

| <span data-ttu-id="2274c-863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-863">Parameter</span></span> | <span data-ttu-id="2274c-864">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-864">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| <span data-ttu-id="2274c-865">レポート</span><span class="sxs-lookup"><span data-stu-id="2274c-865">report</span></span>    | <span data-ttu-id="2274c-866">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="2274c-866">The report to return the name for.</span></span>                         |
| <span data-ttu-id="2274c-867">design</span><span class="sxs-lookup"><span data-stu-id="2274c-867">design</span></span>    | <span data-ttu-id="2274c-868">レポートに関連付けられているデザインの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-868">The name of the design that is associated with the report.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-869">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-869">Return Value</span></span>

<span data-ttu-id="2274c-870">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-870">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-871">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-871">Remarks</span></span>

<span data-ttu-id="2274c-872">**ssrsReportStr** 関数は、有効なレポートに属しているかどうかを検証するために、渡された 2 つの値を解析します。</span><span class="sxs-lookup"><span data-stu-id="2274c-872">The **ssrsReportStr** function parses the two values that are passed to it, to validate whether they belong to a valid report.</span></span> <span data-ttu-id="2274c-873">コントローラーが、どのレポート デザインの組み合わせを呼び出す必要があるかを判断できるように、メニュー項目が controller() を指しているときは、レポート名を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2274c-873">The report name must be set when a menu item points to a controller(), so that the controller can determine which report-design combination must be invoked.</span></span> <span data-ttu-id="2274c-874">**ssrsReportStr** 関数を使用すると、レポートおよびデザイン名のコンパイル時の検証で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2274c-874">Use of the **ssrsReportStr** function provides the benefit of compile-time validation for the report and design name.</span></span> <span data-ttu-id="2274c-875">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-875">This is a compile-time function.</span></span> <span data-ttu-id="2274c-876">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-876">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-877">例</span><span class="sxs-lookup"><span data-stu-id="2274c-877">Example</span></span>

```xpp
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
```

## <a name="staticdelegatestr"></a><span data-ttu-id="2274c-878">staticDelegateStr</span><span class="sxs-lookup"><span data-stu-id="2274c-878">staticDelegateStr</span></span>
<span data-ttu-id="2274c-879">静的デリゲートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="2274c-879">Returns the name of a static delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-880">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-880">Syntax</span></span>

```xpp
str staticDelegateStr(str class, str delegate)
```

### <a name="parameters"></a><span data-ttu-id="2274c-881">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-881">Parameters</span></span>

| <span data-ttu-id="2274c-882">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-882">Parameter</span></span> | <span data-ttu-id="2274c-883">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-883">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="2274c-884">クラス</span><span class="sxs-lookup"><span data-stu-id="2274c-884">class</span></span>     | <span data-ttu-id="2274c-885">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-885">The name of a class, table, or form.</span></span> |
| <span data-ttu-id="2274c-886">デリゲート</span><span class="sxs-lookup"><span data-stu-id="2274c-886">delegate</span></span>  | <span data-ttu-id="2274c-887">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="2274c-887">The name of the delegate.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="2274c-888">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-888">Return Value</span></span>

<span data-ttu-id="2274c-889">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="2274c-889">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-890">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-890">Remarks</span></span>

<span data-ttu-id="2274c-891">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-891">This is a compile-time function.</span></span> <span data-ttu-id="2274c-892">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-892">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-893">例</span><span class="sxs-lookup"><span data-stu-id="2274c-893">Example</span></span>

<span data-ttu-id="2274c-894">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-894">No example.</span></span>

## <a name="staticmethodstr"></a><span data-ttu-id="2274c-895">staticMethodStr</span><span class="sxs-lookup"><span data-stu-id="2274c-895">staticMethodStr</span></span>
<span data-ttu-id="2274c-896">指定した静的メソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-896">Validates that the specified static method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-897">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-897">Syntax</span></span>

```xpp
str staticMethodStr(class class, int method)
```

### <a name="parameters"></a><span data-ttu-id="2274c-898">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-898">Parameters</span></span>

| <span data-ttu-id="2274c-899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-899">Parameter</span></span> | <span data-ttu-id="2274c-900">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-900">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="2274c-901">クラス</span><span class="sxs-lookup"><span data-stu-id="2274c-901">class</span></span>     | <span data-ttu-id="2274c-902">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-902">The name of the class.</span></span>                     |
| <span data-ttu-id="2274c-903">メソッド</span><span class="sxs-lookup"><span data-stu-id="2274c-903">method</span></span>    | <span data-ttu-id="2274c-904">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-904">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-905">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-905">Return Value</span></span>

<span data-ttu-id="2274c-906">有効な場合の、指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-906">The name of the static method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-907">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-907">Remarks</span></span>

<span data-ttu-id="2274c-908">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-908">This is a compile-time function.</span></span> <span data-ttu-id="2274c-909">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-909">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-910">例</span><span class="sxs-lookup"><span data-stu-id="2274c-910">Example</span></span>

<span data-ttu-id="2274c-911">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-911">No example.</span></span>

## <a name="tablecollectionstr"></a><span data-ttu-id="2274c-912">tableCollectionStr</span><span class="sxs-lookup"><span data-stu-id="2274c-912">tableCollectionStr</span></span>
<span data-ttu-id="2274c-913">指定したテーブル コレクションがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-913">Validates that the specified table collection exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-914">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-914">Syntax</span></span>

```xpp
str tableCollectionStr(class tablecollection)
```

### <a name="parameters"></a><span data-ttu-id="2274c-915">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-915">Parameters</span></span>

| <span data-ttu-id="2274c-916">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-916">Parameter</span></span>       | <span data-ttu-id="2274c-917">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-917">Description</span></span>                                   |
|-----------------|-----------------------------------------------|
| <span data-ttu-id="2274c-918">tablecollection</span><span class="sxs-lookup"><span data-stu-id="2274c-918">tablecollection</span></span> | <span data-ttu-id="2274c-919">検証するテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-919">The name of the table collection to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-920">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-920">Return Value</span></span>

<span data-ttu-id="2274c-921">有効な場合の、指定されたテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-921">The name of the specified table collection, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-922">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-922">Remarks</span></span>

<span data-ttu-id="2274c-923">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-923">This is a compile-time function.</span></span> <span data-ttu-id="2274c-924">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-924">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-925">例</span><span class="sxs-lookup"><span data-stu-id="2274c-925">Example</span></span>

<span data-ttu-id="2274c-926">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-926">No example.</span></span>

## <a name="tablefieldgroupstr"></a><span data-ttu-id="2274c-927">tableFieldGroupStr</span><span class="sxs-lookup"><span data-stu-id="2274c-927">tableFieldGroupStr</span></span>
<span data-ttu-id="2274c-928">文字列としてフィールド グループの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-928">Retrieves the name of a field group as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-929">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-929">Syntax</span></span>

```xpp
str tableFieldGroupStr(str tableName, str fieldGroupName)
```

### <a name="parameters"></a><span data-ttu-id="2274c-930">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-930">Parameters</span></span>

| <span data-ttu-id="2274c-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-931">Parameter</span></span>      | <span data-ttu-id="2274c-932">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-932">Description</span></span>                              |
|----------------|------------------------------------------|
| <span data-ttu-id="2274c-933">tableName</span><span class="sxs-lookup"><span data-stu-id="2274c-933">tableName</span></span>      | <span data-ttu-id="2274c-934">フィールド グループを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="2274c-934">The table that contains the field group.</span></span> |
| <span data-ttu-id="2274c-935">fieldGroupName</span><span class="sxs-lookup"><span data-stu-id="2274c-935">fieldGroupName</span></span> | <span data-ttu-id="2274c-936">テーブル内のフィールド グループ。</span><span class="sxs-lookup"><span data-stu-id="2274c-936">The field group in the table.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="2274c-937">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-937">Return Value</span></span>

<span data-ttu-id="2274c-938">文字列としてのフィールド グループの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-938">The name of the field group as a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-939">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-939">Remarks</span></span>

<span data-ttu-id="2274c-940">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-940">This is a compile-time function.</span></span> <span data-ttu-id="2274c-941">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-941">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-942">例</span><span class="sxs-lookup"><span data-stu-id="2274c-942">Example</span></span>

<span data-ttu-id="2274c-943">次の例では、**編集** フィールド グループの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-943">The following example retrieves the name of the **Editing** field group as a string.</span></span>

```xpp
static void tableFieldGroupStrExample(Args _arg)
{
    ;

    Global::info(tableFieldGroupStr(AccountingDistribution, Editing));
}
/****Infolog Display
Message (03:14:54 pm)
Editing
****/
```

## <a name="tablemethodstr"></a><span data-ttu-id="2274c-944">tableMethodStr</span><span class="sxs-lookup"><span data-stu-id="2274c-944">tableMethodStr</span></span>
<span data-ttu-id="2274c-945">指定したメソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-945">Validates that the specified method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-946">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-946">Syntax</span></span>

```xpp
str tableMethodStr(int table, int method)
```

### <a name="parameters"></a><span data-ttu-id="2274c-947">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-947">Parameters</span></span>

| <span data-ttu-id="2274c-948">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-948">Parameter</span></span> | <span data-ttu-id="2274c-949">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-949">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="2274c-950">テーブル</span><span class="sxs-lookup"><span data-stu-id="2274c-950">table</span></span>     | <span data-ttu-id="2274c-951">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-951">The name of the table.</span></span>              |
| <span data-ttu-id="2274c-952">メソッド</span><span class="sxs-lookup"><span data-stu-id="2274c-952">method</span></span>    | <span data-ttu-id="2274c-953">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-953">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-954">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-954">Return Value</span></span>

<span data-ttu-id="2274c-955">有効な場合の、メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-955">The name of the method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-956">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-956">Remarks</span></span>

<span data-ttu-id="2274c-957">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-957">This is a compile-time function.</span></span> <span data-ttu-id="2274c-958">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-958">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-959">例</span><span class="sxs-lookup"><span data-stu-id="2274c-959">Example</span></span>

<span data-ttu-id="2274c-960">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-960">No example.</span></span>

## <a name="tablenum"></a><span data-ttu-id="2274c-961">tableNum</span><span class="sxs-lookup"><span data-stu-id="2274c-961">tableNum</span></span>
<span data-ttu-id="2274c-962">特定のテーブルのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-962">Retrieves the table ID of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-963">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-963">Syntax</span></span>

```xpp
int tableNum(str table)
```

### <a name="parameters"></a><span data-ttu-id="2274c-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-964">Parameters</span></span>

| <span data-ttu-id="2274c-965">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-965">Parameter</span></span> | <span data-ttu-id="2274c-966">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-966">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="2274c-967">テーブル</span><span class="sxs-lookup"><span data-stu-id="2274c-967">table</span></span>     | <span data-ttu-id="2274c-968">テーブル ID を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="2274c-968">The table to retrieve the table ID for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-969">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-969">Return Value</span></span>

<span data-ttu-id="2274c-970">特定のテーブルのテーブル ID</span><span class="sxs-lookup"><span data-stu-id="2274c-970">The table ID of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-971">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-971">Remarks</span></span>

<span data-ttu-id="2274c-972">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-972">This is a compile-time function.</span></span> <span data-ttu-id="2274c-973">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-973">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-974">例</span><span class="sxs-lookup"><span data-stu-id="2274c-974">Example</span></span>

<span data-ttu-id="2274c-975">次の例では、**tableID** 変数を 77 に設定します。これは、**CustTable** テーブルの **ID** です。</span><span class="sxs-lookup"><span data-stu-id="2274c-975">The following example sets the **tableID** variable to 77, which is the **ID** of the **CustTable** table.</span></span>

```xpp
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
```

## <a name="tablepname"></a><span data-ttu-id="2274c-976">tablePName</span><span class="sxs-lookup"><span data-stu-id="2274c-976">tablePName</span></span>
<span data-ttu-id="2274c-977">指定されたテーブルの出力可能な名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-977">Retrieves a string that contains the printable name of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-978">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-978">Syntax</span></span>

```xpp
str tablePName(str table)
```

### <a name="parameters"></a><span data-ttu-id="2274c-979">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-979">Parameters</span></span>

| <span data-ttu-id="2274c-980">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-980">Parameter</span></span> | <span data-ttu-id="2274c-981">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-981">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="2274c-982">テーブル</span><span class="sxs-lookup"><span data-stu-id="2274c-982">table</span></span>     | <span data-ttu-id="2274c-983">印刷可能な名前を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="2274c-983">The table to retrieve the printable name for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-984">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-984">Return Value</span></span>

<span data-ttu-id="2274c-985">指定されたテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-985">The name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-986">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-986">Remarks</span></span>

<span data-ttu-id="2274c-987">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-987">This is a compile-time function.</span></span> <span data-ttu-id="2274c-988">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-988">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-989">例</span><span class="sxs-lookup"><span data-stu-id="2274c-989">Example</span></span>

<span data-ttu-id="2274c-990">次の例では、**CustTable** テーブルのラベルを *MyText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2274c-990">The following example assigns the label of the **CustTable** table to the *MyText* variable.</span></span>

```xpp
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
```

## <a name="tablestaticmethodstr"></a><span data-ttu-id="2274c-991">tableStaticMethodStr</span><span class="sxs-lookup"><span data-stu-id="2274c-991">tableStaticMethodStr</span></span>
<span data-ttu-id="2274c-992">指定した静的メソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-992">Validates that the specified static method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-993">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-993">Syntax</span></span>

```xpp
str tableStaticMethodStr(int table, int method)
```

### <a name="parameters"></a><span data-ttu-id="2274c-994">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-994">Parameters</span></span>

| <span data-ttu-id="2274c-995">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-995">Parameter</span></span> | <span data-ttu-id="2274c-996">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-996">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="2274c-997">テーブル</span><span class="sxs-lookup"><span data-stu-id="2274c-997">table</span></span>     | <span data-ttu-id="2274c-998">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-998">The name of the table.</span></span>                     |
| <span data-ttu-id="2274c-999">メソッド</span><span class="sxs-lookup"><span data-stu-id="2274c-999">method</span></span>    | <span data-ttu-id="2274c-1000">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1000">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1001">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1001">Return Value</span></span>

<span data-ttu-id="2274c-1002">指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1002">The name of the specified static method.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1003">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1003">Remarks</span></span>

<span data-ttu-id="2274c-1004">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1004">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1005">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1005">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1006">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1006">Example</span></span>

<span data-ttu-id="2274c-1007">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-1007">No example.</span></span>

## <a name="tablestr"></a><span data-ttu-id="2274c-1008">tableStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1008">tableStr</span></span>
<span data-ttu-id="2274c-1009">指定したテーブルの名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1009">Retrieves a string that contains the name the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1010">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1010">Syntax</span></span>

```xpp
str tableStr(str table)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1011">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1011">Parameters</span></span>

| <span data-ttu-id="2274c-1012">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1012">Parameter</span></span> | <span data-ttu-id="2274c-1013">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1013">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="2274c-1014">テーブル</span><span class="sxs-lookup"><span data-stu-id="2274c-1014">table</span></span>     | <span data-ttu-id="2274c-1015">文字列を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="2274c-1015">The table to retrieve a string for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1016">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1016">Return Value</span></span>

<span data-ttu-id="2274c-1017">指定したテーブルの名前を含む文字列値。</span><span class="sxs-lookup"><span data-stu-id="2274c-1017">A string value that contains the name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1018">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1018">Remarks</span></span>

<span data-ttu-id="2274c-1019">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1019">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1020">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1020">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1021">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1021">Example</span></span>

<span data-ttu-id="2274c-1022">次の例では、**CustTable** テーブルの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2274c-1022">The following example assigns the name of the **CustTable** table to the *MyTxt* variable.</span></span>

```xpp
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
```

## <a name="tilestr"></a><span data-ttu-id="2274c-1023">tileStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1023">tileStr</span></span>
<span data-ttu-id="2274c-1024">指定したタイルの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1024">Retrieves a string that represents the name of the specified tile.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1025">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1025">Syntax</span></span>

```xpp
str tileStr(str tile)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1026">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1026">Parameters</span></span>

| <span data-ttu-id="2274c-1027">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1027">Parameter</span></span> | <span data-ttu-id="2274c-1028">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1028">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="2274c-1029">tile</span><span class="sxs-lookup"><span data-stu-id="2274c-1029">tile</span></span>      | <span data-ttu-id="2274c-1030">タイルの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1030">The name of the tile.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1031">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1031">Return Value</span></span>

<span data-ttu-id="2274c-1032">文字列のタイルの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1032">The name of the tile in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1033">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1033">Remarks</span></span>

<span data-ttu-id="2274c-1034">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1034">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1035">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1035">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1036">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1036">Example</span></span>

<span data-ttu-id="2274c-1037">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-1037">No example.</span></span>

## <a name="varstr"></a><span data-ttu-id="2274c-1038">varStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1038">varStr</span></span>
<span data-ttu-id="2274c-1039">指定した変数の名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1039">Retrieves a string that contains the name of the specified variable.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1040">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1040">Syntax</span></span>

```xpp
str varStr(str var)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1041">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1041">Parameters</span></span>

| <span data-ttu-id="2274c-1042">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1042">Parameter</span></span> | <span data-ttu-id="2274c-1043">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1043">Description</span></span>               |
|-----------|---------------------------|
| <span data-ttu-id="2274c-1044">var</span><span class="sxs-lookup"><span data-stu-id="2274c-1044">var</span></span>       | <span data-ttu-id="2274c-1045">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1045">The name of the variable.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1046">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1046">Return Value</span></span>

<span data-ttu-id="2274c-1047">指定した変数の名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-1047">A string that contains the name of the specified variable.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1048">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1048">Remarks</span></span>

<span data-ttu-id="2274c-1049">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1049">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1050">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1050">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1051">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1051">Example</span></span>

```xpp
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
```

## <a name="webactionitemstr"></a><span data-ttu-id="2274c-1052">webActionItemStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1052">webActionItemStr</span></span>
<span data-ttu-id="2274c-1053">指定した Web アクション項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1053">Validates that the specified web action item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1054">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1054">Syntax</span></span>

```xpp
str webActionItemStr(class webactionitem)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1055">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1055">Parameters</span></span>

| <span data-ttu-id="2274c-1056">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1056">Parameter</span></span>     | <span data-ttu-id="2274c-1057">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1057">Description</span></span>                                  |
|---------------|----------------------------------------------|
| <span data-ttu-id="2274c-1058">webactionitem</span><span class="sxs-lookup"><span data-stu-id="2274c-1058">webactionitem</span></span> | <span data-ttu-id="2274c-1059">検証する Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1059">The name of the web action item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1060">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1060">Return Value</span></span>

<span data-ttu-id="2274c-1061">有効な場合の、指定された Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1061">The name of the specified web action item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1062">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1062">Remarks</span></span>

<span data-ttu-id="2274c-1063">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1063">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1064">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1064">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1065">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1065">Example</span></span>

```xpp
{
    str s;
    ;
    s = webActionItemStr(EPFlushData);
    print "webactionitem str is " + s;
    pause;
}
```

## <a name="webdisplaycontentitemstr"></a><span data-ttu-id="2274c-1066">webDisplayContentItemStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1066">webDisplayContentItemStr</span></span>
<span data-ttu-id="2274c-1067">指定したWeb 表示のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1067">Validates that the specified web display content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1068">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1068">Syntax</span></span>

```xpp
str webDisplayContentItemStr(class webdisplaycontentitem)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1069">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1069">Parameters</span></span>

| <span data-ttu-id="2274c-1070">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1070">Parameter</span></span>             | <span data-ttu-id="2274c-1071">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1071">Description</span></span>                                           |
|-----------------------|-------------------------------------------------------|
| <span data-ttu-id="2274c-1072">webdisplaycontentitem</span><span class="sxs-lookup"><span data-stu-id="2274c-1072">webdisplaycontentitem</span></span> | <span data-ttu-id="2274c-1073">検証する Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1073">The name of the web display content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1074">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1074">Return Value</span></span>

<span data-ttu-id="2274c-1075">有効な場合の、指定された Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1075">The name of the specified web display content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1076">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1076">Remarks</span></span>

<span data-ttu-id="2274c-1077">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1077">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1078">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1078">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1079">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1079">Example</span></span>

```xpp
{
    str s;
    ;

    s = webDisplayContentItemStr(EPAdmin);
    print "string for webcontent display item EPAdmin is " + s;
    pause;
}
```

## <a name="webformstr"></a><span data-ttu-id="2274c-1080">webFormStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1080">webFormStr</span></span>
<span data-ttu-id="2274c-1081">指定した Web フォームがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1081">Validates that the specified web form exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1082">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1082">Syntax</span></span>

```xpp
str webFormStr(str name)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1083">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1083">Parameters</span></span>

| <span data-ttu-id="2274c-1084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1084">Parameter</span></span> | <span data-ttu-id="2274c-1085">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1085">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="2274c-1086">名前</span><span class="sxs-lookup"><span data-stu-id="2274c-1086">name</span></span>      | <span data-ttu-id="2274c-1087">検証する Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1087">The name of the web form to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1088">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1088">Return Value</span></span>

<span data-ttu-id="2274c-1089">有効な場合の、指定された Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1089">The name of the specified web form, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1090">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1090">Remarks</span></span>

<span data-ttu-id="2274c-1091">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1091">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1092">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1092">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1093">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1093">Example</span></span>

```xpp
{
    str s;
    ;
    s = webFormStr(EPAdmin);
    print "String for web form EPAdmin is " + s;
    pause;
}
```

## <a name="webletitemstr"></a><span data-ttu-id="2274c-1094">webletItemStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1094">webletItemStr</span></span>
<span data-ttu-id="2274c-1095">指定した Weblet 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1095">Validates that the specified weblet item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1096">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1096">Syntax</span></span>

```xpp
str webletItemStr(class webletitem)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1097">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1097">Parameters</span></span>

| <span data-ttu-id="2274c-1098">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1098">Parameter</span></span>  | <span data-ttu-id="2274c-1099">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1099">Description</span></span>                              |
|------------|------------------------------------------|
| <span data-ttu-id="2274c-1100">webletitem</span><span class="sxs-lookup"><span data-stu-id="2274c-1100">webletitem</span></span> | <span data-ttu-id="2274c-1101">検証する Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1101">The name of the weblet item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1102">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1102">Return Value</span></span>

<span data-ttu-id="2274c-1103">有効な場合の、指定された Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1103">The name of the specified weblet item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1104">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1104">Remarks</span></span>

<span data-ttu-id="2274c-1105">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1105">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1106">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1106">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1107">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1107">Example</span></span>

```xpp
{
    str s;
    ;
    s = webletItemStr(WebFormWeblet);
    print "String for WebFormWeblet is " + s;
    pause;
}
```

## <a name="webmenustr"></a><span data-ttu-id="2274c-1108">webMenuStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1108">webMenuStr</span></span>
<span data-ttu-id="2274c-1109">指定した Web メニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1109">Validates that the specified web menu exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1110">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1110">Syntax</span></span>

```xpp
str webMenuStr(str name)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1111">Parameters</span></span>

| <span data-ttu-id="2274c-1112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1112">Parameter</span></span> | <span data-ttu-id="2274c-1113">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1113">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="2274c-1114">名前</span><span class="sxs-lookup"><span data-stu-id="2274c-1114">name</span></span>      | <span data-ttu-id="2274c-1115">検証する Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1115">The name of the web menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1116">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1116">Return Value</span></span>

<span data-ttu-id="2274c-1117">有効な場合の、指定された Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1117">The name of the specified web menu, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1118">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1118">Remarks</span></span>

<span data-ttu-id="2274c-1119">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1119">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1120">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1120">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1121">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1121">Example</span></span>

```xpp
{
    str s;
    ;
    s = webMenuStr(ECPAdmin);
    print "String for web menu ECPAdmin is " + s;
    pause;
}
```

## <a name="weboutputcontentitemstr"></a><span data-ttu-id="2274c-1122">webOutputContentItemStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1122">webOutputContentItemStr</span></span>
<span data-ttu-id="2274c-1123">指定したWeb 出力のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1123">Validates that the specified web output content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1124">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1124">Syntax</span></span>

```xpp
str webOutputContentItemStr(class weboutputcontentitem)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1125">Parameters</span></span>

| <span data-ttu-id="2274c-1126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1126">Parameter</span></span>            | <span data-ttu-id="2274c-1127">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1127">Description</span></span>                                          |
|----------------------|------------------------------------------------------|
| <span data-ttu-id="2274c-1128">weboutputcontentitem</span><span class="sxs-lookup"><span data-stu-id="2274c-1128">weboutputcontentitem</span></span> | <span data-ttu-id="2274c-1129">検証する Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1129">The name of the web output content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1130">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1130">Return Value</span></span>

<span data-ttu-id="2274c-1131">有効な場合の、指定された Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1131">The name of the specified web output content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1132">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1132">Remarks</span></span>

<span data-ttu-id="2274c-1133">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1133">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1134">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1134">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1135">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1135">Example</span></span>

```xpp
{
    str s;
    ;
    s = webOutputContentItemStr(EPPriceList);
    print "string for weboutput content item EPPriceList is " + s;
    pause;
}
```

## <a name="webpagedefstr"></a><span data-ttu-id="2274c-1136">webpageDefStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1136">webpageDefStr</span></span>
<span data-ttu-id="2274c-1137">指定した Web ページ定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1137">Validates that the specified Web page definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1138">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1138">Syntax</span></span>

```xpp
str webpageDefStr(str pagename)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1139">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1139">Parameters</span></span>

| <span data-ttu-id="2274c-1140">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1140">Parameter</span></span> | <span data-ttu-id="2274c-1141">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1141">Description</span></span>                                      |
|-----------|--------------------------------------------------|
| <span data-ttu-id="2274c-1142">pagename</span><span class="sxs-lookup"><span data-stu-id="2274c-1142">pagename</span></span>  | <span data-ttu-id="2274c-1143">検証する Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1143">The name of the Web page definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1144">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1144">Return Value</span></span>

<span data-ttu-id="2274c-1145">有効な場合の、指定された Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1145">The name of the specified web-page definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1146">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1146">Remarks</span></span>

<span data-ttu-id="2274c-1147">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1147">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1148">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1148">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1149">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1149">Example</span></span>

<span data-ttu-id="2274c-1150">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-1150">No example.</span></span>

## <a name="webreportstr"></a><span data-ttu-id="2274c-1151">webReportStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1151">webReportStr</span></span>
<span data-ttu-id="2274c-1152">指定した Web レポートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1152">Validates that the specified web report exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1153">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1153">Syntax</span></span>

```xpp
str webReportStr(str name)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1154">Parameters</span></span>

| <span data-ttu-id="2274c-1155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1155">Parameter</span></span> | <span data-ttu-id="2274c-1156">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1156">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="2274c-1157">名前</span><span class="sxs-lookup"><span data-stu-id="2274c-1157">name</span></span>      | <span data-ttu-id="2274c-1158">検証する Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1158">The name of the web report to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1159">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1159">Return Value</span></span>

<span data-ttu-id="2274c-1160">有効な場合の、指定された Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1160">The name of the specified web report, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1161">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1161">Remarks</span></span>

<span data-ttu-id="2274c-1162">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1162">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1163">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1163">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1164">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1164">Example</span></span>

```xpp
{
    str s;
    ;
    s = webReportStr(EPCSSSalesConfirm);
    print "String for web report EPCSSalesConfirm is " + s;
    pause;
}
```

## <a name="websitedefstr"></a><span data-ttu-id="2274c-1165">websiteDefStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1165">websiteDefStr</span></span>
<span data-ttu-id="2274c-1166">指定した Web サイトの定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1166">Validates that the specified web-site definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1167">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1167">Syntax</span></span>

```xpp
str websiteDefStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1168">Parameters</span></span>

| <span data-ttu-id="2274c-1169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1169">Parameter</span></span>    | <span data-ttu-id="2274c-1170">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1170">Description</span></span>                                      |
|--------------|--------------------------------------------------|
| <span data-ttu-id="2274c-1171">resourcename</span><span class="sxs-lookup"><span data-stu-id="2274c-1171">resourcename</span></span> | <span data-ttu-id="2274c-1172">検証する Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1172">The name of the Web site definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1173">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1173">Return Value</span></span>

<span data-ttu-id="2274c-1174">有効な場合の、指定された Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1174">The name of the specified web-site definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1175">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1175">Remarks</span></span>

<span data-ttu-id="2274c-1176">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1176">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1177">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1177">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1178">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1178">Example</span></span>

```xpp
{
    str s;
    ;

    s = websiteDefStr(AxSiteDef_1033_xip);
    print "string for web site definition AxSiteDef_1033_xip is " + s;
    pause;
}
```

## <a name="websitetempstr"></a><span data-ttu-id="2274c-1179">webSiteTempStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1179">webSiteTempStr</span></span>
<span data-ttu-id="2274c-1180">指定した Web サイトのテンプレートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1180">Validates that the specified web-site template exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1181">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1181">Syntax</span></span>

```xpp
str websiteTempStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1182">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1182">Parameters</span></span>

| <span data-ttu-id="2274c-1183">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1183">Parameter</span></span>    | <span data-ttu-id="2274c-1184">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1184">Description</span></span>                                    |
|--------------|------------------------------------------------|
| <span data-ttu-id="2274c-1185">resourcename</span><span class="sxs-lookup"><span data-stu-id="2274c-1185">resourcename</span></span> | <span data-ttu-id="2274c-1186">検証する Web サイト テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1186">The name of the Web site template to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1187">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1187">Return Value</span></span>

<span data-ttu-id="2274c-1188">有効な場合の、指定された Web テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1188">The name of the specified web-site template, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1189">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1189">Remarks</span></span>

<span data-ttu-id="2274c-1190">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1190">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1191">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1191">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1192">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1192">Example</span></span>

<span data-ttu-id="2274c-1193">例なし。</span><span class="sxs-lookup"><span data-stu-id="2274c-1193">No example.</span></span>

## <a name="webstaticfilestr"></a><span data-ttu-id="2274c-1194">webStaticFileStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1194">webStaticFileStr</span></span>
<span data-ttu-id="2274c-1195">指定した Web 静的ファイルがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1195">Validates that the specified web static file exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1196">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1196">Syntax</span></span>

```xpp
str webStaticFileStr(str pagename)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1197">Parameters</span></span>

| <span data-ttu-id="2274c-1198">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1198">Parameter</span></span> | <span data-ttu-id="2274c-1199">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1199">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="2274c-1200">pagename</span><span class="sxs-lookup"><span data-stu-id="2274c-1200">pagename</span></span>  | <span data-ttu-id="2274c-1201">検証する Web 静的ファイル テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1201">The name of the web static file to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1202">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1202">Return Value</span></span>

<span data-ttu-id="2274c-1203">有効な場合の、指定された Web 静的ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1203">The name of the specified web static file, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1204">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1204">Remarks</span></span>

<span data-ttu-id="2274c-1205">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1205">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1206">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1206">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1207">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1207">Example</span></span>

```xpp
{
    str s;
    ;

    s = webStaticFileStr(AXEP);
    print "string for web static file AXEP is " + s;
    pause;
}
```

## <a name="weburlitemstr"></a><span data-ttu-id="2274c-1208">webUrlItemStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1208">webUrlItemStr</span></span>
<span data-ttu-id="2274c-1209">指定した Web URL 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1209">Validates that the specified web URL item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1210">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1210">Syntax</span></span>

```xpp
str webUrlItemStr(class weburlitem)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1211">Parameters</span></span>

| <span data-ttu-id="2274c-1212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1212">Parameter</span></span>  | <span data-ttu-id="2274c-1213">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1213">Description</span></span>                               |
|------------|-------------------------------------------|
| <span data-ttu-id="2274c-1214">weburlitem</span><span class="sxs-lookup"><span data-stu-id="2274c-1214">weburlitem</span></span> | <span data-ttu-id="2274c-1215">検証する Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1215">The name of the web URL item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1216">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1216">Return Value</span></span>

<span data-ttu-id="2274c-1217">有効な場合の、指定された Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1217">The name of the specified web URL item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1218">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1218">Remarks</span></span>

<span data-ttu-id="2274c-1219">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1219">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1220">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1220">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1221">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1221">Example</span></span>

```xpp
{
    str s;
    ;

    s = webUrlItemStr(EPAdmin);
    print "string for web url item EPAdmin is " + s;
    pause;
}
```

## <a name="webwebpartstr"></a><span data-ttu-id="2274c-1222">webWebPartStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1222">webWebPartStr</span></span>
<span data-ttu-id="2274c-1223">指定した Web パーツがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1223">Validates that the specified web part exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1224">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1224">Syntax</span></span>

```xpp
str webWebpartStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1225">Parameters</span></span>

| <span data-ttu-id="2274c-1226">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1226">Parameter</span></span>    | <span data-ttu-id="2274c-1227">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1227">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="2274c-1228">resourcename</span><span class="sxs-lookup"><span data-stu-id="2274c-1228">resourcename</span></span> | <span data-ttu-id="2274c-1229">検証する Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1229">The name of the web part to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1230">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1230">Return Value</span></span>

<span data-ttu-id="2274c-1231">有効な場合の、指定された Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1231">The name of the specified web part, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1232">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1232">Remarks</span></span>

<span data-ttu-id="2274c-1233">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1233">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1234">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1234">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1235">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1235">Example</span></span>

```xpp
{
    str s;
    ;

    s = webWebpartStr(AxWebParts_cab);
    print "string for web part AxWebParts_cab is " + s;
    pause;
}
```

## <a name="workflowapprovalstr"></a><span data-ttu-id="2274c-1236">workflowApprovalStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1236">workflowApprovalStr</span></span>
<span data-ttu-id="2274c-1237">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー承認の名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1237">Retrieves the name of a workflow approval in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1238">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1238">Syntax</span></span>

```xpp
str workflowapprovalstr(approval approval)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1239">Parameters</span></span>

| <span data-ttu-id="2274c-1240">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1240">Parameter</span></span> | <span data-ttu-id="2274c-1241">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1241">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="2274c-1242">承認</span><span class="sxs-lookup"><span data-stu-id="2274c-1242">approval</span></span>  | <span data-ttu-id="2274c-1243">ワークフローの承認のアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1243">The Application Explorer name of the workflow approval.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1244">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1244">Return Value</span></span>

<span data-ttu-id="2274c-1245">ワークフローの承認のアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-1245">A string that represents the Application Explorer name of the workflow approval.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1246">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1246">Remarks</span></span>

<span data-ttu-id="2274c-1247">リテラル テキストの代わりにこの関数を使用して、ワークフロー承認名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1247">Use this function instead of literal text to retrieve a string that contains the workflow approval name.</span></span> <span data-ttu-id="2274c-1248">ワークフローの承認が存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1248">If the workflow approval does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="2274c-1249">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1249">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1250">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1250">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1251">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1251">Example</span></span>

<span data-ttu-id="2274c-1252">次のコード例では、変数 *str s* を **MyWorkflowApproval** に設定します。これは、アプリケーション エクスプローラーでのワークフロー承認の名前です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1252">The following code example sets the variable *str s* to **MyWorkflowApproval** which is the name of the workflow approval in the Application Explorer.</span></span>

```xpp
static void MyWorkflowApprovalStrExample(Args _args)
{
    str s;
    ;
    s = workflowapprovalstr(MyWorkflowApproval);
    print s;
    pause;
}
```

## <a name="workflowcategorystr"></a><span data-ttu-id="2274c-1253">workflowCategoryStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1253">workflowCategoryStr</span></span>
<span data-ttu-id="2274c-1254">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー カテゴリの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1254">Retrieves the name of a workflow category in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1255">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1255">Syntax</span></span>

```xpp
str workflowcategorystr(category category)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1256">Parameters</span></span>

| <span data-ttu-id="2274c-1257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1257">Parameter</span></span> | <span data-ttu-id="2274c-1258">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1258">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="2274c-1259">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="2274c-1259">category</span></span>  | <span data-ttu-id="2274c-1260">ワークフロー カテゴリーのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1260">The Application Explorer name of the workflow category.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1261">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1261">Return Value</span></span>

<span data-ttu-id="2274c-1262">ワークフロー カテゴリのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-1262">A string that represents the Application Explorer name of the workflow category.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1263">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1263">Remarks</span></span>

<span data-ttu-id="2274c-1264">リテラル テキストの代わりにこの関数を使用して、ワークフロー カテゴリ名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1264">Use this function instead of literal text to retrieve a string that contains the workflow category name.</span></span> <span data-ttu-id="2274c-1265">ワークフローのカテゴリーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1265">If the workflow category does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="2274c-1266">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1266">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1267">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1267">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1268">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1268">Example</span></span>

<span data-ttu-id="2274c-1269">次のコード例では、変数 *str s* を **MyWorkflowCategory** に設定します。これは、アプリケーション エクスプローラーでのワークフロー カテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1269">The following code example sets the variable *str s* to **MyWorkflowCategory** which is the name of the workflow category in the Application Explorer.</span></span>

```xpp
static void MyWorkflowCategoryStrExample(Args _args)
{
    str s;
    ;
    s = workflowcategorystr(MyWorkflowCategory);
    print s;
    pause;
}
```

## <a name="workflowtaskstr"></a><span data-ttu-id="2274c-1270">workflowTaskStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1270">workflowTaskStr</span></span>
<span data-ttu-id="2274c-1271">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー タスクの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1271">Retrieves the name of a workflow task in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1272">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1272">Syntax</span></span>

```xpp
str workflowtaskstr(task task)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1273">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1273">Parameters</span></span>

| <span data-ttu-id="2274c-1274">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1274">Parameter</span></span> | <span data-ttu-id="2274c-1275">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1275">Description</span></span>                                         |
|-----------|-----------------------------------------------------|
| <span data-ttu-id="2274c-1276">タスク</span><span class="sxs-lookup"><span data-stu-id="2274c-1276">task</span></span>      | <span data-ttu-id="2274c-1277">ワークフロー タスクのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1277">The Application Explorer name of the workflow task.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1278">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1278">Return Value</span></span>

<span data-ttu-id="2274c-1279">ワークフロー タスクのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="2274c-1279">A string that represents the Application Explorer name of the workflow task.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1280">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1280">Remarks</span></span>

<span data-ttu-id="2274c-1281">リテラル テキストの代わりにこの関数を使用して、ワークフロー タスク名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1281">Use this function instead of literal text to retrieve a string that contains the workflow task name.</span></span> <span data-ttu-id="2274c-1282">ワークフローのタスクーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1282">If the workflow task does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="2274c-1283">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1283">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1284">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1284">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1285">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1285">Example</span></span>

<span data-ttu-id="2274c-1286">次のコード例では、変数 *str s* を **MyWorkflowTask** に設定します。これは、アプリケーション エクスプローラーでのワークフロー タスクの名前です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1286">The following code example sets the variable *str s* to **MyWorkflowTask** which is the name of the workflow task in the Application Explorer.</span></span>

```xpp
static void MyWorkflowTaskStrExample(Args _args)
{
    str s;
    ;
    s = workflowtaskstr(MyWorkflowTask);
    print s;
    pause;
}
```

## <a name="workflowtypestr"></a><span data-ttu-id="2274c-1287">workflowTypeStr</span><span class="sxs-lookup"><span data-stu-id="2274c-1287">workflowTypeStr</span></span>
<span data-ttu-id="2274c-1288">指定したワークフロー タイプがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2274c-1288">Validates that the specified workflow type exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="2274c-1289">構文</span><span class="sxs-lookup"><span data-stu-id="2274c-1289">Syntax</span></span>

```xpp
str workflowTypeStr(str workflow)
```

### <a name="parameters"></a><span data-ttu-id="2274c-1290">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1290">Parameters</span></span>

| <span data-ttu-id="2274c-1291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2274c-1291">Parameter</span></span> | <span data-ttu-id="2274c-1292">説明</span><span class="sxs-lookup"><span data-stu-id="2274c-1292">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="2274c-1293">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="2274c-1293">workflow</span></span>  | <span data-ttu-id="2274c-1294">検証するワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1294">The name of the workflow type to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="2274c-1295">戻り値</span><span class="sxs-lookup"><span data-stu-id="2274c-1295">Return Value</span></span>

<span data-ttu-id="2274c-1296">ワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="2274c-1296">The name of the workflow type.</span></span>

### <a name="remarks"></a><span data-ttu-id="2274c-1297">備考</span><span class="sxs-lookup"><span data-stu-id="2274c-1297">Remarks</span></span>

<span data-ttu-id="2274c-1298">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="2274c-1298">This is a compile-time function.</span></span> <span data-ttu-id="2274c-1299">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2274c-1299">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="2274c-1300">例</span><span class="sxs-lookup"><span data-stu-id="2274c-1300">Example</span></span>

```xpp
static void workFlowTypeStrExample(Args _args)
{
    str s;
    ;
    s = workFlowTypeStr(BudgetAccountEntryType);
    print s;
    pause;
}
```


