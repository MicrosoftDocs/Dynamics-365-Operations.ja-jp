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
ms.openlocfilehash: a0585d9ed683052612826272f868e957cccb4f4a
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026204"
---
# <a name="x-compile-time-functions"></a><span data-ttu-id="d5946-103">X++ コンパイル時関数</span><span class="sxs-lookup"><span data-stu-id="d5946-103">X++ compile-time functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5946-104">このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。</span><span class="sxs-lookup"><span data-stu-id="d5946-104">This topic lists the compile-time functions and describes their syntax, parameters, and return values.</span></span>

# <a name="overview"></a><span data-ttu-id="d5946-105">概要</span><span class="sxs-lookup"><span data-stu-id="d5946-105">Overview</span></span>

<span data-ttu-id="d5946-106">コンパイル時関数は、X++ コードのコンパイル時に早期実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5946-106">Compile-time functions are executed early during compilation of X++ code.</span></span> <span data-ttu-id="d5946-107">アプリケーション エクスプローラーに保存されているメタデータの変更に対してコードを復元するためには、可能な限り X++ で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5946-107">They should be used wherever possible in X++ code to make the code resilient to changes to the metadata stored in the Application Explorer.</span></span> <span data-ttu-id="d5946-108">コンパイル時関数は、コンパイラによって入力値が検証されます。</span><span class="sxs-lookup"><span data-stu-id="d5946-108">Compile-time functions have their input value verified by the compiler.</span></span> <span data-ttu-id="d5946-109">入力された値が見つからず、アプリケーション エクスプローラーの既存のオブジェクトが一致しない場合は、コンパイラーはエラーを発行します。</span><span class="sxs-lookup"><span data-stu-id="d5946-109">If the input value is not found to match any existing object in the Application Explorer, the compiler issues an error.</span></span> <span data-ttu-id="d5946-110">コンパイラは実行時に変数に含まれる値を判別できないため、これらの関数への入力はリテラルでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d5946-110">The inputs to these functions must be literals, because the compiler cannot determine the value that a variable contains at run time.</span></span> <span data-ttu-id="d5946-111">コンパイル時関数は、メタデータ アサーション関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-111">A compile-time function is a metadata assertion function.</span></span> <span data-ttu-id="d5946-112">アプリケーション エクスプローラーでエンティティを表す引数を取得し、コンパイル時にその引数を検証します。</span><span class="sxs-lookup"><span data-stu-id="d5946-112">It takes arguments that represents an entity in the Application Explorer and validates the arguments at compile time.</span></span> <span data-ttu-id="d5946-113">実行時に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="d5946-113">It has no effect at run time.</span></span> <span data-ttu-id="d5946-114">属性は **SysAttribute** クラスから継承するクラスです。</span><span class="sxs-lookup"><span data-stu-id="d5946-114">Attributes are classes that inherit from the **SysAttribute** class.</span></span> <span data-ttu-id="d5946-115">フォーム、レポート、クエリ、メニュー のメタデータの検証をサポートするには、コントロールの **AutoDeclaration** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d5946-115">To support the validation of form, report, query, and menu metadata, use the **AutoDeclaration** property on controls.</span></span> <span data-ttu-id="d5946-116">これらの機能のほとんどは、アプリケーション エクスプローラーにある項目に関するメタデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-116">Most of these functions retrieve metadata about items that are in the Application Explorer.</span></span> <span data-ttu-id="d5946-117">いくつかの一般的なコンパイル時機能は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d5946-117">Some common compile time functions are as follows:</span></span>

-   <span data-ttu-id="d5946-118">`classNum` – クラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-118">`classNum` – Retrieves the ID of a class.</span></span>
-   <span data-ttu-id="d5946-119">`classStr` – コンパイル時に、その名前のクラスが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="d5946-119">`classStr` – During compile time, verifies that a class of that name exists.</span></span> <span data-ttu-id="d5946-120">この方法は、実行時にエラーを後で発見するよりも優れています。</span><span class="sxs-lookup"><span data-stu-id="d5946-120">This approach is better than discovering the error later during run time.</span></span>
-   <span data-ttu-id="d5946-121">`evalBuf`– X++ コードの入力文字列を評価し、結果を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-121">`evalBuf`– Evaluates the input string of X++ code, and then returns the results as a string.</span></span>
-   <span data-ttu-id="d5946-122">`literalStr` – は、文字列 `"@SYS12345"` などのラベルの文字列表示が与えられたときにラベル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-122">`literalStr` – retrieves a label ID when given the string representation of a label, such as the string `"@SYS12345"`.</span></span> <span data-ttu-id="d5946-123">たとえば、`myLabel.exists(literalStr("@SYS12345"));`。</span><span class="sxs-lookup"><span data-stu-id="d5946-123">For example, `myLabel.exists(literalStr("@SYS12345"));`.</span></span>

| <span data-ttu-id="d5946-124">**メモ**</span><span class="sxs-lookup"><span data-stu-id="d5946-124">**Note**</span></span>                                                         |
|------------------------------------------------------------------|
| <span data-ttu-id="d5946-125">X++ コンパイル時関数は .NET プログラムから呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="d5946-125">X++ compile time functions cannot be called from a .NET program.</span></span> |

### <a name="functions"></a><span data-ttu-id="d5946-126">関数</span><span class="sxs-lookup"><span data-stu-id="d5946-126">Functions</span></span>

## <a name="attributestr"></a><span data-ttu-id="d5946-127">attributeStr</span><span class="sxs-lookup"><span data-stu-id="d5946-127">attributeStr</span></span>
<span data-ttu-id="d5946-128">指定した属性クラスがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-128">Validates that the specified attribute class exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-129">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-129">Syntax</span></span>

```xpp
str classStr(class class)
```

### <a name="parameters"></a><span data-ttu-id="d5946-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-130">Parameters</span></span>

| <span data-ttu-id="d5946-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-131">Parameter</span></span> | <span data-ttu-id="d5946-132">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-132">Description</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="d5946-133">クラス</span><span class="sxs-lookup"><span data-stu-id="d5946-133">class</span></span>     | <span data-ttu-id="d5946-134">検証する属性の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-134">The name of the attribute to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-135">Return Value</span></span>

<span data-ttu-id="d5946-136">属性の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-136">The name of the attribute.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-137">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-137">Remarks</span></span>

<span data-ttu-id="d5946-138">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-138">This is a compile-time function.</span></span> <span data-ttu-id="d5946-139">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-139">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-140">例</span><span class="sxs-lookup"><span data-stu-id="d5946-140">Example</span></span>
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

## <a name="classnum"></a><span data-ttu-id="d5946-141">classNum</span><span class="sxs-lookup"><span data-stu-id="d5946-141">classNum</span></span>
<span data-ttu-id="d5946-142">指定されたクラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-142">Retrieves the ID of the specified class.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-143">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-143">Syntax</span></span>

```xpp
int classNum(class class)
```

### <a name="parameters"></a><span data-ttu-id="d5946-144">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-144">Parameters</span></span>

| <span data-ttu-id="d5946-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-145">Parameter</span></span> | <span data-ttu-id="d5946-146">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-146">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="d5946-147">クラス</span><span class="sxs-lookup"><span data-stu-id="d5946-147">class</span></span>     | <span data-ttu-id="d5946-148">ID を取得するクラス。</span><span class="sxs-lookup"><span data-stu-id="d5946-148">The class for which to retrieve the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-149">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-149">Return Value</span></span>

<span data-ttu-id="d5946-150">指定されたクラスの ID。</span><span class="sxs-lookup"><span data-stu-id="d5946-150">The ID of the specified class.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-151">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-151">Remarks</span></span>

<span data-ttu-id="d5946-152">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-152">This is a compile-time function.</span></span> <span data-ttu-id="d5946-153">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-153">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-154">例</span><span class="sxs-lookup"><span data-stu-id="d5946-154">Example</span></span>

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

## <a name="classstr"></a><span data-ttu-id="d5946-155">classStr</span><span class="sxs-lookup"><span data-stu-id="d5946-155">classStr</span></span>
<span data-ttu-id="d5946-156">文字列としてクラスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-156">Retrieves the name of a class as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-157">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-157">Syntax</span></span>

```xpp
str classStr(class class)
```

### <a name="parameters"></a><span data-ttu-id="d5946-158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-158">Parameters</span></span>

| <span data-ttu-id="d5946-159">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-159">Parameter</span></span> | <span data-ttu-id="d5946-160">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-160">Description</span></span>                      |
|-----------|----------------------------------|
| <span data-ttu-id="d5946-161">クラス</span><span class="sxs-lookup"><span data-stu-id="d5946-161">class</span></span>     | <span data-ttu-id="d5946-162">返すクラスの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-162">The name of the class to return.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-163">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-163">Return Value</span></span>

<span data-ttu-id="d5946-164">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-164">The name of the class.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-165">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-165">Remarks</span></span>

<span data-ttu-id="d5946-166">リテラル テキストの代わりにこの関数を使用して、クラス名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-166">Use this function instead of literal text to retrieve a string that contains the class name.</span></span> <span data-ttu-id="d5946-167">クラスが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="d5946-167">If the class does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="d5946-168">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-168">This is a compile-time function.</span></span> <span data-ttu-id="d5946-169">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-169">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-170">例</span><span class="sxs-lookup"><span data-stu-id="d5946-170">Example</span></span>

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

## <a name="configurationkeynum"></a><span data-ttu-id="d5946-171">configurationKeyNum</span><span class="sxs-lookup"><span data-stu-id="d5946-171">configurationKeyNum</span></span>
<span data-ttu-id="d5946-172">指定されたコンフィギュレーション キーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-172">Retrieves the ID of the specified configuration key.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-173">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-173">Syntax</span></span>

```xpp
int configurationKeyNum(str keyname)
```

### <a name="parameters"></a><span data-ttu-id="d5946-174">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-174">Parameters</span></span>

| <span data-ttu-id="d5946-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-175">Parameter</span></span> | <span data-ttu-id="d5946-176">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-176">Description</span></span>                                       |
|-----------|---------------------------------------------------|
| <span data-ttu-id="d5946-177">keyname</span><span class="sxs-lookup"><span data-stu-id="d5946-177">keyname</span></span>   | <span data-ttu-id="d5946-178">ID を返すコンフィギュレーション キー。</span><span class="sxs-lookup"><span data-stu-id="d5946-178">The configuration key for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-179">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-179">Return Value</span></span>

<span data-ttu-id="d5946-180">指定されたコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="d5946-180">The ID of the specified configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-181">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-181">Remarks</span></span>

<span data-ttu-id="d5946-182">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-182">This is a compile-time function.</span></span> <span data-ttu-id="d5946-183">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-183">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-184">例</span><span class="sxs-lookup"><span data-stu-id="d5946-184">Example</span></span>

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

## <a name="configurationkeystr"></a><span data-ttu-id="d5946-185">configurationKeyStr</span><span class="sxs-lookup"><span data-stu-id="d5946-185">configurationKeyStr</span></span>
<span data-ttu-id="d5946-186">文字列としてコンフィギュレーション キーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-186">Retrieves the name of a configuration key as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-187">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-187">Syntax</span></span>

```xpp
str configurationKeyStr(str keyname)
```

### <a name="parameters"></a><span data-ttu-id="d5946-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-188">Parameters</span></span>

| <span data-ttu-id="d5946-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-189">Parameter</span></span> | <span data-ttu-id="d5946-190">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-190">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="d5946-191">keyname</span><span class="sxs-lookup"><span data-stu-id="d5946-191">keyname</span></span>   | <span data-ttu-id="d5946-192">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-192">The name of the configuration key.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-193">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-193">Return Value</span></span>

<span data-ttu-id="d5946-194">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-194">The name of the configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-195">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-195">Remarks</span></span>

<span data-ttu-id="d5946-196">リテラル テキストの代わりにこの関数を使用して、構成キー名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-196">Use this function instead of literal text to retrieve a string that contains the configuration key name.</span></span> <span data-ttu-id="d5946-197">キーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="d5946-197">If the key does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="d5946-198">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-198">This is a compile-time function.</span></span> <span data-ttu-id="d5946-199">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-199">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-200">例</span><span class="sxs-lookup"><span data-stu-id="d5946-200">Example</span></span>

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

## <a name="dataentitydatasourcestr"></a><span data-ttu-id="d5946-201">dataEntityDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="d5946-201">dataEntityDataSourceStr</span></span>
<span data-ttu-id="d5946-202">データ エンティティのデータ ソースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-202">Retrieves the name of a data source of a data entity.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-203">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-203">Syntax</span></span>

```xpp
str dataEntityDataSourceStr(str dataEntity, str dataSource)
```

### <a name="parameters"></a><span data-ttu-id="d5946-204">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-204">Parameters</span></span>

| <span data-ttu-id="d5946-205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-205">Parameter</span></span>  | <span data-ttu-id="d5946-206">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-206">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="d5946-207">dataEntity</span><span class="sxs-lookup"><span data-stu-id="d5946-207">dataEntity</span></span> | <span data-ttu-id="d5946-208">データ エンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-208">The name of the data entity.</span></span> |
| <span data-ttu-id="d5946-209">dataSource</span><span class="sxs-lookup"><span data-stu-id="d5946-209">dataSource</span></span> | <span data-ttu-id="d5946-210">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-210">The name of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-211">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-211">Return Value</span></span>

<span data-ttu-id="d5946-212">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-212">The name of the data source.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-213">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-213">Remarks</span></span>

<span data-ttu-id="d5946-214">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-214">This is a compile-time function.</span></span> <span data-ttu-id="d5946-215">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-215">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-216">例</span><span class="sxs-lookup"><span data-stu-id="d5946-216">Example</span></span>

<span data-ttu-id="d5946-217">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-217">No example.</span></span>

## <a name="delegatestr"></a><span data-ttu-id="d5946-218">delegateStr</span><span class="sxs-lookup"><span data-stu-id="d5946-218">delegateStr</span></span>
<span data-ttu-id="d5946-219">委任の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-219">Returns the name of the delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-220">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-220">Syntax</span></span>

```xpp
str delegateStr(str class, str instanceDelegate)
```

### <a name="parameters"></a><span data-ttu-id="d5946-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-221">Parameters</span></span>

| <span data-ttu-id="d5946-222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-222">Parameter</span></span>        | <span data-ttu-id="d5946-223">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-223">Description</span></span>                            |
|------------------|----------------------------------------|
| <span data-ttu-id="d5946-224">クラス</span><span class="sxs-lookup"><span data-stu-id="d5946-224">class</span></span>            | <span data-ttu-id="d5946-225">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-225">The name of the class, table, or form.</span></span> |
| <span data-ttu-id="d5946-226">instanceDelegate</span><span class="sxs-lookup"><span data-stu-id="d5946-226">instanceDelegate</span></span> | <span data-ttu-id="d5946-227">インスタンス デリゲートの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-227">The name of the instance delegate.</span></span>     |

### <a name="return-value"></a><span data-ttu-id="d5946-228">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-228">Return Value</span></span>

<span data-ttu-id="d5946-229">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="d5946-229">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-230">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-230">Remarks</span></span>

<span data-ttu-id="d5946-231">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-231">This is a compile-time function.</span></span> <span data-ttu-id="d5946-232">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-232">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-233">例</span><span class="sxs-lookup"><span data-stu-id="d5946-233">Example</span></span>

<span data-ttu-id="d5946-234">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-234">No example.</span></span>

## <a name="dimensionhierarchylevelstr"></a><span data-ttu-id="d5946-235">dimensionHierarchyLevelStr</span><span class="sxs-lookup"><span data-stu-id="d5946-235">dimensionHierarchyLevelStr</span></span>
<span data-ttu-id="d5946-236">分析コード階層レベルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-236">Returns the name of the dimension hierarchy level.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-237">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-237">Syntax</span></span>

```xpp
str dimensionHierarchyLevelStr(str dimensionHierarchyLevel)
```

### <a name="parameters"></a><span data-ttu-id="d5946-238">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-238">Parameters</span></span>

| <span data-ttu-id="d5946-239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-239">Parameter</span></span>               | <span data-ttu-id="d5946-240">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-240">Description</span></span>                                |
|-------------------------|--------------------------------------------|
| <span data-ttu-id="d5946-241">dimensionHierarchyLevel</span><span class="sxs-lookup"><span data-stu-id="d5946-241">dimensionHierarchyLevel</span></span> | <span data-ttu-id="d5946-242">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-242">The name of the dimension hierarchy level.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-243">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-243">Return Value</span></span>

<span data-ttu-id="d5946-244">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-244">The name of the dimension hierarchy level.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-245">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-245">Remarks</span></span>

<span data-ttu-id="d5946-246">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-246">This is a compile-time function.</span></span> <span data-ttu-id="d5946-247">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-247">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-248">例</span><span class="sxs-lookup"><span data-stu-id="d5946-248">Example</span></span>

<span data-ttu-id="d5946-249">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-249">No example.</span></span>

## <a name="dimensionhierarchystr"></a><span data-ttu-id="d5946-250">dimensionHierarchyStr</span><span class="sxs-lookup"><span data-stu-id="d5946-250">dimensionHierarchyStr</span></span>
<span data-ttu-id="d5946-251">分析コード階層の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-251">Returns the name of the dimension hierarchy.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-252">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-252">Syntax</span></span>

```xpp
str dimensionHierarchyStr(str dimensionHierarchy)
```

### <a name="parameters"></a><span data-ttu-id="d5946-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-253">Parameters</span></span>

| <span data-ttu-id="d5946-254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-254">Parameter</span></span>          | <span data-ttu-id="d5946-255">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-255">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="d5946-256">dimensionHierarchy</span><span class="sxs-lookup"><span data-stu-id="d5946-256">dimensionHierarchy</span></span> | <span data-ttu-id="d5946-257">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-257">The name of the dimension hierarchy.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-258">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-258">Return Value</span></span>

<span data-ttu-id="d5946-259">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-259">The name of the dimension hierarchy.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-260">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-260">Remarks</span></span>

<span data-ttu-id="d5946-261">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-261">This is a compile-time function.</span></span> <span data-ttu-id="d5946-262">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-262">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-263">例</span><span class="sxs-lookup"><span data-stu-id="d5946-263">Example</span></span>

<span data-ttu-id="d5946-264">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-264">No example.</span></span>

## <a name="dimensionreferencestr"></a><span data-ttu-id="d5946-265">dimensionReferenceStr</span><span class="sxs-lookup"><span data-stu-id="d5946-265">dimensionReferenceStr</span></span>
<span data-ttu-id="d5946-266">分析コード参照の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-266">Returns the name of the dimension reference.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-267">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-267">Syntax</span></span>

```xpp
str dimensionReferenceStr(str dimensionReference)
```

### <a name="parameters"></a><span data-ttu-id="d5946-268">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-268">Parameters</span></span>

| <span data-ttu-id="d5946-269">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-269">Parameter</span></span>          | <span data-ttu-id="d5946-270">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-270">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="d5946-271">dimensionReference</span><span class="sxs-lookup"><span data-stu-id="d5946-271">dimensionReference</span></span> | <span data-ttu-id="d5946-272">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-272">The name of the dimension reference.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-273">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-273">Return Value</span></span>

<span data-ttu-id="d5946-274">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-274">The name of the dimension reference.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-275">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-275">Remarks</span></span>

<span data-ttu-id="d5946-276">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-276">This is a compile-time function.</span></span> <span data-ttu-id="d5946-277">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-277">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-278">例</span><span class="sxs-lookup"><span data-stu-id="d5946-278">Example</span></span>

<span data-ttu-id="d5946-279">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-279">No example.</span></span>

## <a name="dutystr"></a><span data-ttu-id="d5946-280">dutyStr</span><span class="sxs-lookup"><span data-stu-id="d5946-280">dutyStr</span></span>
<span data-ttu-id="d5946-281">指定したセキュリティ職務権限の名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-281">Retrieves a string that represents the name of the specified security duty.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-282">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-282">Syntax</span></span>

```xpp
str dutyStr(str securityDuty)
```

### <a name="parameters"></a><span data-ttu-id="d5946-283">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-283">Parameters</span></span>

| <span data-ttu-id="d5946-284">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-284">Parameter</span></span>    | <span data-ttu-id="d5946-285">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-285">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="d5946-286">securityDuty</span><span class="sxs-lookup"><span data-stu-id="d5946-286">securityDuty</span></span> | <span data-ttu-id="d5946-287">セキュリティ職務権限の名前です。</span><span class="sxs-lookup"><span data-stu-id="d5946-287">The name of the security duty.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-288">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-288">Return Value</span></span>

<span data-ttu-id="d5946-289">文字列のセキュリティ職務の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-289">The name of the security duty in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-290">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-290">Remarks</span></span>

<span data-ttu-id="d5946-291">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-291">This is a compile-time function.</span></span> <span data-ttu-id="d5946-292">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-292">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-293">例</span><span class="sxs-lookup"><span data-stu-id="d5946-293">Example</span></span>

<span data-ttu-id="d5946-294">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-294">No example.</span></span>

## <a name="enumcnt"></a><span data-ttu-id="d5946-295">enumCnt</span><span class="sxs-lookup"><span data-stu-id="d5946-295">enumCnt</span></span>
<span data-ttu-id="d5946-296">指定された列挙型の要素数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-296">Retrieves the number of elements in the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-297">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-297">Syntax</span></span>

```xpp
int enumCnt(enum enumtype)
```

### <a name="parameters"></a><span data-ttu-id="d5946-298">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-298">Parameters</span></span>

| <span data-ttu-id="d5946-299">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-299">Parameter</span></span> | <span data-ttu-id="d5946-300">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-300">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="d5946-301">enumtype</span><span class="sxs-lookup"><span data-stu-id="d5946-301">enumtype</span></span>  | <span data-ttu-id="d5946-302">列挙型タイプ。</span><span class="sxs-lookup"><span data-stu-id="d5946-302">The enumeration type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-303">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-303">Return Value</span></span>

<span data-ttu-id="d5946-304">指定された列挙型の要素数。</span><span class="sxs-lookup"><span data-stu-id="d5946-304">The number of elements in the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-305">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-305">Remarks</span></span>

<span data-ttu-id="d5946-306">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-306">This is a compile-time function.</span></span> <span data-ttu-id="d5946-307">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-307">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-308">例</span><span class="sxs-lookup"><span data-stu-id="d5946-308">Example</span></span>

```xpp
enumCnt(NoYes); //Returns 2, as the two elements are Yes and No.
```

## <a name="enumliteralstr"></a><span data-ttu-id="d5946-309">enumLiteralStr</span><span class="sxs-lookup"><span data-stu-id="d5946-309">enumLiteralStr</span></span>
<span data-ttu-id="d5946-310">指定した文字列が指定した列挙型の要素であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d5946-310">Indicates whether the specified string is an element of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-311">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-311">Syntax</span></span>

```xpp
\enumLiteralStr(enum enum, string str)
```

### <a name="parameters"></a><span data-ttu-id="d5946-312">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-312">Parameters</span></span>

| <span data-ttu-id="d5946-313">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-313">Parameter</span></span> | <span data-ttu-id="d5946-314">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-314">Description</span></span>                                                      |
|-----------|------------------------------------------------------------------|
| <span data-ttu-id="d5946-315">列挙型</span><span class="sxs-lookup"><span data-stu-id="d5946-315">enum</span></span>      | <span data-ttu-id="d5946-316">指定された値を取得する列挙型。</span><span class="sxs-lookup"><span data-stu-id="d5946-316">The enumeration type from which to retrieve the specified value.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-317">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-317">Return Value</span></span>

<span data-ttu-id="d5946-318">指定された文字列が見つかった場合の *str* パラメーターの値。それ以外の場合は、コンパイル エラーです。</span><span class="sxs-lookup"><span data-stu-id="d5946-318">The value of the *str* parameter if the specified string was found; otherwise, a compilation error.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-319">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-319">Remarks</span></span>

<span data-ttu-id="d5946-320">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-320">This is a compile-time function.</span></span> <span data-ttu-id="d5946-321">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-321">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-322">例</span><span class="sxs-lookup"><span data-stu-id="d5946-322">Example</span></span>

```xpp
static void getEnumValueAsString()
{
    str i;
    i = enumLiteralStr(ABCEnum, "valueInABCEnum");
    print i;
    pause;
}
```

## <a name="enumnum"></a><span data-ttu-id="d5946-323">enumNum</span><span class="sxs-lookup"><span data-stu-id="d5946-323">enumNum</span></span>
<span data-ttu-id="d5946-324">指定された列挙型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-324">Retrieves the ID of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-325">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-325">Syntax</span></span>
```xpp
int enumNum(enum enum)
```

### <a name="parameters"></a><span data-ttu-id="d5946-326">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-326">Parameters</span></span>

| <span data-ttu-id="d5946-327">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-327">Parameter</span></span> | <span data-ttu-id="d5946-328">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-328">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="d5946-329">列挙型</span><span class="sxs-lookup"><span data-stu-id="d5946-329">enum</span></span>      | <span data-ttu-id="d5946-330">ID を返す列挙。</span><span class="sxs-lookup"><span data-stu-id="d5946-330">The enumeration for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-331">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-331">Return Value</span></span>

<span data-ttu-id="d5946-332">指定された列挙型の ID。</span><span class="sxs-lookup"><span data-stu-id="d5946-332">The ID of the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-333">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-333">Remarks</span></span>

<span data-ttu-id="d5946-334">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-334">This is a compile-time function.</span></span> <span data-ttu-id="d5946-335">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-335">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-336">例</span><span class="sxs-lookup"><span data-stu-id="d5946-336">Example</span></span>

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

## <a name="enumstr"></a><span data-ttu-id="d5946-337">enumStr</span><span class="sxs-lookup"><span data-stu-id="d5946-337">enumStr</span></span>
<span data-ttu-id="d5946-338">文字列として列挙型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-338">Retrieves the name of an enumeration as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-339">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-339">Syntax</span></span>

```xpp
str enumStr(enum enum)
```

### <a name="parameters"></a><span data-ttu-id="d5946-340">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-340">Parameters</span></span>

| <span data-ttu-id="d5946-341">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-341">Parameter</span></span> | <span data-ttu-id="d5946-342">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-342">Description</span></span>                  |
|-----------|------------------------------|
| <span data-ttu-id="d5946-343">列挙型</span><span class="sxs-lookup"><span data-stu-id="d5946-343">enum</span></span>      | <span data-ttu-id="d5946-344">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-344">The name of the enumeration.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-345">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-345">Return Value</span></span>

<span data-ttu-id="d5946-346">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-346">The name of the enumeration.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-347">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-347">Remarks</span></span>

<span data-ttu-id="d5946-348">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-348">This is a compile-time function.</span></span> <span data-ttu-id="d5946-349">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-349">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-350">例</span><span class="sxs-lookup"><span data-stu-id="d5946-350">Example</span></span>

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

## <a name="extendedtypenum"></a><span data-ttu-id="d5946-351">extendedTypeNum</span><span class="sxs-lookup"><span data-stu-id="d5946-351">extendedTypeNum</span></span>
<span data-ttu-id="d5946-352">指定された拡張データ型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-352">Retrieves the ID of the specified extended data type.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-353">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-353">Syntax</span></span>

```xpp
int extendedTypeNum(int str)
```

### <a name="parameters"></a><span data-ttu-id="d5946-354">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-354">Parameters</span></span>

| <span data-ttu-id="d5946-355">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-355">Parameter</span></span> | <span data-ttu-id="d5946-356">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-356">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="d5946-357">str</span><span class="sxs-lookup"><span data-stu-id="d5946-357">str</span></span>       | <span data-ttu-id="d5946-358">ID を返す拡張データ型。</span><span class="sxs-lookup"><span data-stu-id="d5946-358">The extended data type for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-359">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-359">Return Value</span></span>

<span data-ttu-id="d5946-360">指定された拡張データ型の ID。</span><span class="sxs-lookup"><span data-stu-id="d5946-360">The ID of the specified extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-361">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-361">Remarks</span></span>

<span data-ttu-id="d5946-362">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-362">This is a compile-time function.</span></span> <span data-ttu-id="d5946-363">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-363">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-364">例</span><span class="sxs-lookup"><span data-stu-id="d5946-364">Example</span></span>

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

## <a name="extendedtypestr"></a><span data-ttu-id="d5946-365">extendedTypeStr</span><span class="sxs-lookup"><span data-stu-id="d5946-365">extendedTypeStr</span></span>
<span data-ttu-id="d5946-366">文字列として拡張データ型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-366">Retrieves the name of an extended data type as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-367">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-367">Syntax</span></span>

```xpp
str extendedTypeStr(int str)
```

### <a name="parameters"></a><span data-ttu-id="d5946-368">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-368">Parameters</span></span>

| <span data-ttu-id="d5946-369">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-369">Parameter</span></span> | <span data-ttu-id="d5946-370">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-370">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="d5946-371">str</span><span class="sxs-lookup"><span data-stu-id="d5946-371">str</span></span>       | <span data-ttu-id="d5946-372">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-372">The name of the extended data type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-373">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-373">Return Value</span></span>

<span data-ttu-id="d5946-374">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-374">The name of the extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-375">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-375">Remarks</span></span>

<span data-ttu-id="d5946-376">リテラル テキストの代わりにこの関数を使用すると、拡張データ型名を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-376">Use this function instead of literal text to return a string that contains the extended data type name.</span></span> <span data-ttu-id="d5946-377">データ タイプが存在しない場合、**extendedTypeStr** 関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="d5946-377">If the data type does not exist, the **extendedTypeStr** function generates a syntax error at compile time.</span></span> <span data-ttu-id="d5946-378">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-378">This is a compile-time function.</span></span> <span data-ttu-id="d5946-379">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-379">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-380">例</span><span class="sxs-lookup"><span data-stu-id="d5946-380">Example</span></span>

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

## <a name="fieldnum"></a><span data-ttu-id="d5946-381">fieldNum</span><span class="sxs-lookup"><span data-stu-id="d5946-381">fieldNum</span></span>
<span data-ttu-id="d5946-382">指定したフィールドの ID 番号を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-382">Returns the ID number of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-383">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-383">Syntax</span></span>

```xpp
int fieldNum(str tableName, str fieldName)
```

### <a name="parameters"></a><span data-ttu-id="d5946-384">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-384">Parameters</span></span>

| <span data-ttu-id="d5946-385">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-385">Parameter</span></span> | <span data-ttu-id="d5946-386">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-386">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="d5946-387">tableName</span><span class="sxs-lookup"><span data-stu-id="d5946-387">tableName</span></span> | <span data-ttu-id="d5946-388">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-388">The name of the table.</span></span> |
| <span data-ttu-id="d5946-389">fieldName</span><span class="sxs-lookup"><span data-stu-id="d5946-389">fieldName</span></span> | <span data-ttu-id="d5946-390">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-390">The name of the field.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-391">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-391">Return Value</span></span>

<span data-ttu-id="d5946-392">指定されたフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="d5946-392">The ID of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-393">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-393">Remarks</span></span>

<span data-ttu-id="d5946-394">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-394">This is a compile-time function.</span></span> <span data-ttu-id="d5946-395">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-395">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-396">例</span><span class="sxs-lookup"><span data-stu-id="d5946-396">Example</span></span>

<span data-ttu-id="d5946-397">次の例では、**CashDisc** フィールドの番号を **CustTable** テーブルに出力します。</span><span class="sxs-lookup"><span data-stu-id="d5946-397">The following example prints the number of the **CashDisc** field in the **CustTable** table.</span></span>

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

## <a name="fieldpname"></a><span data-ttu-id="d5946-398">fieldPName</span><span class="sxs-lookup"><span data-stu-id="d5946-398">fieldPName</span></span>
<span data-ttu-id="d5946-399">指定されたフィールドのラベルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-399">Retrieves the label of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-400">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-400">Syntax</span></span>

```xpp
str fieldPName(str tableid, str fieldid)
```

### <a name="parameters"></a><span data-ttu-id="d5946-401">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-401">Parameters</span></span>

| <span data-ttu-id="d5946-402">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-402">Parameter</span></span> | <span data-ttu-id="d5946-403">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-403">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="d5946-404">tableid</span><span class="sxs-lookup"><span data-stu-id="d5946-404">tableid</span></span>   | <span data-ttu-id="d5946-405">指定されたフィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="d5946-405">The table that contains the specified field.</span></span> |
| <span data-ttu-id="d5946-406">fieldid</span><span class="sxs-lookup"><span data-stu-id="d5946-406">fieldid</span></span>   | <span data-ttu-id="d5946-407">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="d5946-407">The field to convert.</span></span>                        |

### <a name="return-value"></a><span data-ttu-id="d5946-408">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-408">Return Value</span></span>

<span data-ttu-id="d5946-409">フィールドのラベル。</span><span class="sxs-lookup"><span data-stu-id="d5946-409">The label of the field.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-410">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-410">Remarks</span></span>

<span data-ttu-id="d5946-411">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-411">This is a compile-time function.</span></span> <span data-ttu-id="d5946-412">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-412">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-413">例</span><span class="sxs-lookup"><span data-stu-id="d5946-413">Example</span></span>

<span data-ttu-id="d5946-414">次の例では、**CashDisc** フィールドのラベルを出力します。</span><span class="sxs-lookup"><span data-stu-id="d5946-414">The following example prints the label of the **CashDisc** field.</span></span>

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

## <a name="fieldstr"></a><span data-ttu-id="d5946-415">fieldStr</span><span class="sxs-lookup"><span data-stu-id="d5946-415">fieldStr</span></span>
<span data-ttu-id="d5946-416">指定したフィールドのフィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-416">Retrieves the field name of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-417">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-417">Syntax</span></span>

```xpp
str fieldStr(str tableid, str fieldid)
```

### <a name="parameters"></a><span data-ttu-id="d5946-418">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-418">Parameters</span></span>

| <span data-ttu-id="d5946-419">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-419">Parameter</span></span> | <span data-ttu-id="d5946-420">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-420">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="d5946-421">tableid</span><span class="sxs-lookup"><span data-stu-id="d5946-421">tableid</span></span>   | <span data-ttu-id="d5946-422">フィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="d5946-422">The table that contains the field.</span></span> |
| <span data-ttu-id="d5946-423">fieldid</span><span class="sxs-lookup"><span data-stu-id="d5946-423">fieldid</span></span>   | <span data-ttu-id="d5946-424">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="d5946-424">The field to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="d5946-425">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-425">Return Value</span></span>

<span data-ttu-id="d5946-426">指定したフィールドのフィールド名。</span><span class="sxs-lookup"><span data-stu-id="d5946-426">The field name of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-427">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-427">Remarks</span></span>

<span data-ttu-id="d5946-428">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-428">This is a compile-time function.</span></span> <span data-ttu-id="d5946-429">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-429">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-430">例</span><span class="sxs-lookup"><span data-stu-id="d5946-430">Example</span></span>

<span data-ttu-id="d5946-431">次の例では、**CashDisc** フィールドの名前を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d5946-431">The following example assigns the name of the **CashDisc** field to the *myText* variable.</span></span>

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

## <a name="formcontrolstr"></a><span data-ttu-id="d5946-432">formControlStr</span><span class="sxs-lookup"><span data-stu-id="d5946-432">formControlStr</span></span>
<span data-ttu-id="d5946-433">X++ コンパイラは、コントロールがフォームに存在するかどうかをチェックし、関数呼び出しを有効なコントロール名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d5946-433">Causes the X++ compiler to check whether the control exists on the form, and to replace the function call with a string of the valid control name.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-434">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-434">Syntax</span></span>

```xpp
str formControlStr(formName, controlName)
```

### <a name="parameters"></a><span data-ttu-id="d5946-435">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-435">Parameters</span></span>

| <span data-ttu-id="d5946-436">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-436">Parameter</span></span>   | <span data-ttu-id="d5946-437">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-437">Description</span></span>                                                          |
|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="d5946-438">formName</span><span class="sxs-lookup"><span data-stu-id="d5946-438">formName</span></span>    | <span data-ttu-id="d5946-439">引用符ではなく、フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-439">The name of the form, not in quotation marks.</span></span>                        |
| <span data-ttu-id="d5946-440">controlName</span><span class="sxs-lookup"><span data-stu-id="d5946-440">controlName</span></span> | <span data-ttu-id="d5946-441">フォーム上のコントロールの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="d5946-441">The name of the control that is on the form, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-442">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-442">Return Value</span></span>

<span data-ttu-id="d5946-443">アプリケーション エクスプローラーで表示されるコントロールの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-443">A string that contains the name of the control as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-444">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-444">Remarks</span></span>

<span data-ttu-id="d5946-445">コントロールがフォームに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5946-445">A compile error is issued if the compiler determines that the control does not exist on the form.</span></span> <span data-ttu-id="d5946-446">X++ コードが引用符が含まれる文字列を使用してコントロールの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="d5946-446">If your X++ code uses a string that contains quotation marks to supply the control name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="d5946-447">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="d5946-447">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="d5946-448">コンパイラにより実行される **formControlStr** などの X++ 関数は、コンパイル時関数と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d5946-448">X++ functions such as **formControlStr** that are executed by the compiler are called compile-time functions or compile-time functions.</span></span> <span data-ttu-id="d5946-449">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="d5946-449">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="d5946-450">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="d5946-450">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="d5946-451">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-451">This is a compile-time function.</span></span> <span data-ttu-id="d5946-452">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-452">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-453">例</span><span class="sxs-lookup"><span data-stu-id="d5946-453">Example</span></span>

<span data-ttu-id="d5946-454">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-454">No example.</span></span>

## <a name="formdatafieldstr"></a><span data-ttu-id="d5946-455">formDataFieldStr</span><span class="sxs-lookup"><span data-stu-id="d5946-455">formDataFieldStr</span></span>
<span data-ttu-id="d5946-456">フォームのデータ フィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-456">Returns the name of a data field in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-457">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-457">Syntax</span></span>

```xpp
str formDataFieldStr(str formName, str dataSource, str dataField)
```

### <a name="parameters"></a><span data-ttu-id="d5946-458">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-458">Parameters</span></span>

| <span data-ttu-id="d5946-459">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-459">Parameter</span></span>  | <span data-ttu-id="d5946-460">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-460">Description</span></span>                        |
|------------|------------------------------------|
| <span data-ttu-id="d5946-461">formName</span><span class="sxs-lookup"><span data-stu-id="d5946-461">formName</span></span>   | <span data-ttu-id="d5946-462">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-462">The name of the form.</span></span>              |
| <span data-ttu-id="d5946-463">dataSource</span><span class="sxs-lookup"><span data-stu-id="d5946-463">dataSource</span></span> | <span data-ttu-id="d5946-464">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="d5946-464">The data source of the form.</span></span>       |
| <span data-ttu-id="d5946-465">dataField</span><span class="sxs-lookup"><span data-stu-id="d5946-465">dataField</span></span>  | <span data-ttu-id="d5946-466">データ ソースのデータ フィールド。</span><span class="sxs-lookup"><span data-stu-id="d5946-466">The data field of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-467">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-467">Return Value</span></span>

<span data-ttu-id="d5946-468">フォームのデータ フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-468">The name of a data field in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-469">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-469">Remarks</span></span>

<span data-ttu-id="d5946-470">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-470">This is a compile-time function.</span></span> <span data-ttu-id="d5946-471">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-471">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-472">例</span><span class="sxs-lookup"><span data-stu-id="d5946-472">Example</span></span>

```xpp
str a = formDataFieldStr(FMVehicle, FMModelRate, RatePerDay);
```

## <a name="formdatasourcestr"></a><span data-ttu-id="d5946-473">formDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="d5946-473">formDataSourceStr</span></span>
<span data-ttu-id="d5946-474">フォームのデータ ソースの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-474">Returns the name of a data source in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-475">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-475">Syntax</span></span>

```xpp
str formDataSourceStr(str formName, str dataSource)
```

### <a name="parameters"></a><span data-ttu-id="d5946-476">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-476">Parameters</span></span>

| <span data-ttu-id="d5946-477">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-477">Parameter</span></span>  | <span data-ttu-id="d5946-478">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-478">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="d5946-479">formName</span><span class="sxs-lookup"><span data-stu-id="d5946-479">formName</span></span>   | <span data-ttu-id="d5946-480">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-480">The name of the form.</span></span>        |
| <span data-ttu-id="d5946-481">dataSource</span><span class="sxs-lookup"><span data-stu-id="d5946-481">dataSource</span></span> | <span data-ttu-id="d5946-482">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="d5946-482">The data source of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-483">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-483">Return Value</span></span>

<span data-ttu-id="d5946-484">フォームのデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-484">The name of a data source in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-485">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-485">Remarks</span></span>

<span data-ttu-id="d5946-486">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-486">This is a compile-time function.</span></span> <span data-ttu-id="d5946-487">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-487">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-488">例</span><span class="sxs-lookup"><span data-stu-id="d5946-488">Example</span></span>

```xpp
str b = formDataSourceStr(FMVehicle, FMModelRate);
```

## <a name="formmethodstr"></a><span data-ttu-id="d5946-489">formMethodStr</span><span class="sxs-lookup"><span data-stu-id="d5946-489">formMethodStr</span></span>
<span data-ttu-id="d5946-490">フォームのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-490">Returns the name of a method of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-491">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-491">Syntax</span></span>

```xpp
str formMethodStr(str formName, str methodName)
```

### <a name="parameters"></a><span data-ttu-id="d5946-492">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-492">Parameters</span></span>

| <span data-ttu-id="d5946-493">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-493">Parameter</span></span>  | <span data-ttu-id="d5946-494">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-494">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="d5946-495">formName</span><span class="sxs-lookup"><span data-stu-id="d5946-495">formName</span></span>   | <span data-ttu-id="d5946-496">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-496">The name of the form.</span></span>   |
| <span data-ttu-id="d5946-497">methodName</span><span class="sxs-lookup"><span data-stu-id="d5946-497">methodName</span></span> | <span data-ttu-id="d5946-498">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="d5946-498">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-499">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-499">Return Value</span></span>

<span data-ttu-id="d5946-500">フォームのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-500">The name of a method in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-501">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-501">Remarks</span></span>

<span data-ttu-id="d5946-502">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-502">This is a compile-time function.</span></span> <span data-ttu-id="d5946-503">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-503">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-504">例</span><span class="sxs-lookup"><span data-stu-id="d5946-504">Example</span></span>

<span data-ttu-id="d5946-505">次の例では、**showDialog** メソッドの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="d5946-505">The following example prints the name of the **showDialog** method.</span></span>

```xpp
str c = formMethodStr(Batch,showDialog);
```

## <a name="formstr"></a><span data-ttu-id="d5946-506">formStr</span><span class="sxs-lookup"><span data-stu-id="d5946-506">formStr</span></span>
<span data-ttu-id="d5946-507">フォームの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-507">Retrieves the name of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-508">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-508">Syntax</span></span>

```xpp
str formStr(str form)
```

### <a name="parameters"></a><span data-ttu-id="d5946-509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-509">Parameters</span></span>

| <span data-ttu-id="d5946-510">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-510">Parameter</span></span> | <span data-ttu-id="d5946-511">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-511">Description</span></span>         |
|-----------|---------------------|
| <span data-ttu-id="d5946-512">フォーム</span><span class="sxs-lookup"><span data-stu-id="d5946-512">form</span></span>      | <span data-ttu-id="d5946-513">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-513">The name of a form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-514">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-514">Return Value</span></span>

<span data-ttu-id="d5946-515">フォームの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-515">A string that represents the name of the form.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-516">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-516">Remarks</span></span>

<span data-ttu-id="d5946-517">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-517">This is a compile-time function.</span></span> <span data-ttu-id="d5946-518">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-518">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-519">例</span><span class="sxs-lookup"><span data-stu-id="d5946-519">Example</span></span>

<span data-ttu-id="d5946-520">次の例では、InventDim フォームの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="d5946-520">The following example prints the name of the InventDim form.</span></span>

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

## <a name="identifierstr"></a><span data-ttu-id="d5946-521">identifierStr</span><span class="sxs-lookup"><span data-stu-id="d5946-521">identifierStr</span></span>
<span data-ttu-id="d5946-522">指定された識別子を文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="d5946-522">Converts the specified identifier to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-523">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-523">Syntax</span></span>

```xpp
str identifierStr(str ident)
```

### <a name="parameters"></a><span data-ttu-id="d5946-524">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-524">Parameters</span></span>

| <span data-ttu-id="d5946-525">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-525">Parameter</span></span> | <span data-ttu-id="d5946-526">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-526">Description</span></span>                |
|-----------|----------------------------|
| <span data-ttu-id="d5946-527">ident</span><span class="sxs-lookup"><span data-stu-id="d5946-527">ident</span></span>     | <span data-ttu-id="d5946-528">変換する ID。</span><span class="sxs-lookup"><span data-stu-id="d5946-528">The identifier to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-529">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-529">Return Value</span></span>

<span data-ttu-id="d5946-530">指定した ID を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-530">A string that represents the specified identifier.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-531">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-531">Remarks</span></span>

<span data-ttu-id="d5946-532">**identifierStr** 関数使用する場合、ベスト プラクティス警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5946-532">You will receive a best practice warning if you use the **identifierStr** function.</span></span> <span data-ttu-id="d5946-533">これは、**identifierStr** に対して存在チェックが実行されたために発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-533">This occurs because existence checking is performed for **identifierStr**.</span></span> <span data-ttu-id="d5946-534">使用可能な場合は、より具体的なコンパイル時の関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-534">Try to use a more specific compile-time function if one is available.</span></span> <span data-ttu-id="d5946-535">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-535">This is a compile-time function.</span></span> <span data-ttu-id="d5946-536">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-536">For more information, [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-537">例</span><span class="sxs-lookup"><span data-stu-id="d5946-537">Example</span></span>

<span data-ttu-id="d5946-538">次のコード例では、*myvar* 変数名を *thevar* 変数に割り当てています。</span><span class="sxs-lookup"><span data-stu-id="d5946-538">The following code example assigns the *myvar* variable name to the *thevar* variable.</span></span>

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

## <a name="indexnum"></a><span data-ttu-id="d5946-539">indexNum</span><span class="sxs-lookup"><span data-stu-id="d5946-539">indexNum</span></span>
<span data-ttu-id="d5946-540">指定されたインデックスを数字に変換します。</span><span class="sxs-lookup"><span data-stu-id="d5946-540">Converts the specified index to a number.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-541">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-541">Syntax</span></span>

```xpp
int indexNum(str tableid, str indexid)
```

### <a name="parameters"></a><span data-ttu-id="d5946-542">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-542">Parameters</span></span>

| <span data-ttu-id="d5946-543">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-543">Parameter</span></span> | <span data-ttu-id="d5946-544">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-544">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="d5946-545">tableid</span><span class="sxs-lookup"><span data-stu-id="d5946-545">tableid</span></span>   | <span data-ttu-id="d5946-546">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="d5946-546">The table that contains the index.</span></span> |
| <span data-ttu-id="d5946-547">indexid</span><span class="sxs-lookup"><span data-stu-id="d5946-547">indexid</span></span>   | <span data-ttu-id="d5946-548">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="d5946-548">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="d5946-549">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-549">Return Value</span></span>

<span data-ttu-id="d5946-550">指定されたインデックスを表すインデックス番号。</span><span class="sxs-lookup"><span data-stu-id="d5946-550">The index number that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-551">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-551">Remarks</span></span>

<span data-ttu-id="d5946-552">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-552">This is a compile-time function.</span></span> <span data-ttu-id="d5946-553">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-553">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-554">例</span><span class="sxs-lookup"><span data-stu-id="d5946-554">Example</span></span>

<span data-ttu-id="d5946-555">次の例では、当事者インデックスのインデックス値を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-555">The following example returns the index value of the Party index.</span></span>

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

## <a name="indexstr"></a><span data-ttu-id="d5946-556">indexStr</span><span class="sxs-lookup"><span data-stu-id="d5946-556">indexStr</span></span>
<span data-ttu-id="d5946-557">指定されたインデックスを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="d5946-557">Converts the specified index to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-558">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-558">Syntax</span></span>

```xpp
str indexStr(str tableid, str indexid)
```

### <a name="parameters"></a><span data-ttu-id="d5946-559">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-559">Parameters</span></span>

| <span data-ttu-id="d5946-560">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-560">Parameter</span></span> | <span data-ttu-id="d5946-561">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-561">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="d5946-562">tableid</span><span class="sxs-lookup"><span data-stu-id="d5946-562">tableid</span></span>   | <span data-ttu-id="d5946-563">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="d5946-563">The table that contains the index.</span></span> |
| <span data-ttu-id="d5946-564">indexid</span><span class="sxs-lookup"><span data-stu-id="d5946-564">indexid</span></span>   | <span data-ttu-id="d5946-565">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="d5946-565">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="d5946-566">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-566">Return Value</span></span>

<span data-ttu-id="d5946-567">指定インデックスを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-567">A string that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-568">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-568">Remarks</span></span>

<span data-ttu-id="d5946-569">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-569">This is a compile-time function.</span></span> <span data-ttu-id="d5946-570">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-570">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-571">例</span><span class="sxs-lookup"><span data-stu-id="d5946-571">Example</span></span>

<span data-ttu-id="d5946-572">次の例では、**CashDisc** インデックス値を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d5946-572">The following example assigns the **CashDisc** index value to the *myText* variable.</span></span>

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

## <a name="licensecodenum"></a><span data-ttu-id="d5946-573">licenseCodeNum</span><span class="sxs-lookup"><span data-stu-id="d5946-573">licenseCodeNum</span></span>
<span data-ttu-id="d5946-574">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-574">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-575">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-575">Syntax</span></span>

```xpp
int licenseCodeNum(str codename)
```

### <a name="parameters"></a><span data-ttu-id="d5946-576">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-576">Parameters</span></span>

| <span data-ttu-id="d5946-577">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-577">Parameter</span></span> | <span data-ttu-id="d5946-578">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-578">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="d5946-579">codename</span><span class="sxs-lookup"><span data-stu-id="d5946-579">codename</span></span>  | <span data-ttu-id="d5946-580">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-580">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-581">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-581">Return Value</span></span>

<span data-ttu-id="d5946-582">指定されたライセンス コードの数。</span><span class="sxs-lookup"><span data-stu-id="d5946-582">The number of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-583">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-583">Remarks</span></span>

<span data-ttu-id="d5946-584">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-584">This is a compile-time function.</span></span> <span data-ttu-id="d5946-585">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-585">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-586">例</span><span class="sxs-lookup"><span data-stu-id="d5946-586">Example</span></span>

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

## <a name="licensecodestr"></a><span data-ttu-id="d5946-587">licenseCodeStr</span><span class="sxs-lookup"><span data-stu-id="d5946-587">licenseCodeStr</span></span>
<span data-ttu-id="d5946-588">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-588">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-589">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-589">Syntax</span></span>

```xpp
str licenseCodeStr(str codename)
```

### <a name="parameters"></a><span data-ttu-id="d5946-590">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-590">Parameters</span></span>

| <span data-ttu-id="d5946-591">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-591">Parameter</span></span> | <span data-ttu-id="d5946-592">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-592">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="d5946-593">codename</span><span class="sxs-lookup"><span data-stu-id="d5946-593">codename</span></span>  | <span data-ttu-id="d5946-594">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-594">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-595">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-595">Return Value</span></span>

<span data-ttu-id="d5946-596">指定されたライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-596">The name of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-597">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-597">Remarks</span></span>

<span data-ttu-id="d5946-598">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-598">This is a compile-time function.</span></span> <span data-ttu-id="d5946-599">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-599">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-600">例</span><span class="sxs-lookup"><span data-stu-id="d5946-600">Example</span></span>

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

## <a name="literalstr"></a><span data-ttu-id="d5946-601">literalStr</span><span class="sxs-lookup"><span data-stu-id="d5946-601">literalStr</span></span>
<span data-ttu-id="d5946-602">指定した文字列がリテラル文字列であることを検証します。そうでない場合は、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-602">Validates that the specified string can be a literal string; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-603">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-603">Syntax</span></span>

```xpp
str literalStr(int str)
```

### <a name="parameters"></a><span data-ttu-id="d5946-604">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-604">Parameters</span></span>

| <span data-ttu-id="d5946-605">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-605">Parameter</span></span> | <span data-ttu-id="d5946-606">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-606">Description</span></span>             |
|-----------|-------------------------|
| <span data-ttu-id="d5946-607">codename</span><span class="sxs-lookup"><span data-stu-id="d5946-607">codename</span></span>  | <span data-ttu-id="d5946-608">検証する文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-608">The string to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-609">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-609">Return Value</span></span>

<span data-ttu-id="d5946-610">有効な場合は、リテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-610">The literal string if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-611">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-611">Remarks</span></span>

<span data-ttu-id="d5946-612">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-612">This is a compile-time function.</span></span> <span data-ttu-id="d5946-613">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-613">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-614">例</span><span class="sxs-lookup"><span data-stu-id="d5946-614">Example</span></span>

```xpp
{
    str s;
    ;

    s = literalStr("This is a literal str");
    print s;
    pause;
}
```

## <a name="maxdate"></a><span data-ttu-id="d5946-615">maxDate</span><span class="sxs-lookup"><span data-stu-id="d5946-615">maxDate</span></span>
<span data-ttu-id="d5946-616">日付型の変数に使用できる最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-616">Retrieves the maximum value allowed for a variable of type date.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-617">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-617">Syntax</span></span>

```xpp
date maxDate()
```

### <a name="return-value"></a><span data-ttu-id="d5946-618">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-618">Return Value</span></span>

<span data-ttu-id="d5946-619">**日付** の変数に使用できる最大値は、**2154-12-31**です。</span><span class="sxs-lookup"><span data-stu-id="d5946-619">The maximum value allowed for a variable of type **date**, which is **2154-12-31**.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-620">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-620">Remarks</span></span>

<span data-ttu-id="d5946-621">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-621">This is a compile-time function.</span></span> <span data-ttu-id="d5946-622">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-622">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-623">例</span><span class="sxs-lookup"><span data-stu-id="d5946-623">Example</span></span>

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

## <a name="maxint"></a><span data-ttu-id="d5946-624">maxInt</span><span class="sxs-lookup"><span data-stu-id="d5946-624">maxInt</span></span>
<span data-ttu-id="d5946-625">**int** 型に格納可能な最大符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-625">Retrieves the maximum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-626">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-626">Syntax</span></span>

```xpp
int maxInt()
```

### <a name="return-value"></a><span data-ttu-id="d5946-627">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-627">Return Value</span></span>

<span data-ttu-id="d5946-628">整数の許容値の最大値。</span><span class="sxs-lookup"><span data-stu-id="d5946-628">The maximum value allowed value of an integer.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-629">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-629">Remarks</span></span>

<span data-ttu-id="d5946-630">その他の整数値は、戻り値以下になります。</span><span class="sxs-lookup"><span data-stu-id="d5946-630">Any other integer will be less than or equal to the returned value.</span></span> <span data-ttu-id="d5946-631">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-631">This is a compile-time function.</span></span> <span data-ttu-id="d5946-632">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-632">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-633">例</span><span class="sxs-lookup"><span data-stu-id="d5946-633">Example</span></span>

```xpp
static void maxIntExample(Args _arg)
{
    int i;
    ;
    print "The maximum value for type int is " + int2Str(maxInt());
    pause;
}
```

## <a name="measurementstr"></a><span data-ttu-id="d5946-634">measurementStr</span><span class="sxs-lookup"><span data-stu-id="d5946-634">measurementStr</span></span>
<span data-ttu-id="d5946-635">測定の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-635">Returns the name of a measurement.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-636">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-636">Syntax</span></span>

```xpp
str measurementStr(str measurement)
```

### <a name="parameters"></a><span data-ttu-id="d5946-637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-637">Parameters</span></span>

| <span data-ttu-id="d5946-638">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-638">Parameter</span></span>   | <span data-ttu-id="d5946-639">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-639">Description</span></span>                  |
|-------------|------------------------------|
| <span data-ttu-id="d5946-640">測定値</span><span class="sxs-lookup"><span data-stu-id="d5946-640">measurement</span></span> | <span data-ttu-id="d5946-641">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-641">The name of the measurement.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-642">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-642">Return Value</span></span>

<span data-ttu-id="d5946-643">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-643">The name of the measurement.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-644">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-644">Remarks</span></span>

<span data-ttu-id="d5946-645">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-645">This is a compile-time function.</span></span> <span data-ttu-id="d5946-646">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-646">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-647">例</span><span class="sxs-lookup"><span data-stu-id="d5946-647">Example</span></span>

<span data-ttu-id="d5946-648">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-648">No example.</span></span>

## <a name="measurestr"></a><span data-ttu-id="d5946-649">measureStr</span><span class="sxs-lookup"><span data-stu-id="d5946-649">measureStr</span></span>
<span data-ttu-id="d5946-650">メジャーの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-650">Returns the name of a measure.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-651">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-651">Syntax</span></span>

```xpp
str measureStr(str measure)
```

### <a name="parameters"></a><span data-ttu-id="d5946-652">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-652">Parameters</span></span>

| <span data-ttu-id="d5946-653">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-653">Parameter</span></span> | <span data-ttu-id="d5946-654">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-654">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="d5946-655">測定</span><span class="sxs-lookup"><span data-stu-id="d5946-655">measure</span></span>   | <span data-ttu-id="d5946-656">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-656">The name of the measure.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-657">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-657">Return Value</span></span>

<span data-ttu-id="d5946-658">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-658">The name of the measure.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-659">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-659">Remarks</span></span>

<span data-ttu-id="d5946-660">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-660">This is a compile-time function.</span></span> <span data-ttu-id="d5946-661">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-661">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-662">例</span><span class="sxs-lookup"><span data-stu-id="d5946-662">Example</span></span>

<span data-ttu-id="d5946-663">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-663">No example.</span></span>

## <a name="menuitemactionstr"></a><span data-ttu-id="d5946-664">menuItemActionStr</span><span class="sxs-lookup"><span data-stu-id="d5946-664">menuItemActionStr</span></span>
<span data-ttu-id="d5946-665">指定したメニュー項目のアクションがアプリケーション オブジェクト ツリー (Application Explorer) に存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-665">Validates that the specified menu item action exists in the Application Object Tree (Application Explorer); if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-666">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-666">Syntax</span></span>

```xpp
str menuItemActionStr(class menuitem)
```

### <a name="parameters"></a><span data-ttu-id="d5946-667">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-667">Parameters</span></span>

| <span data-ttu-id="d5946-668">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-668">Parameter</span></span> | <span data-ttu-id="d5946-669">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-669">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="d5946-670">codename</span><span class="sxs-lookup"><span data-stu-id="d5946-670">codename</span></span>  | <span data-ttu-id="d5946-671">検証するメニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-671">The name of the menu item action to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-672">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-672">Return Value</span></span>

<span data-ttu-id="d5946-673">有効な場合の、メニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-673">The name of the menu item action, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-674">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-674">Remarks</span></span>

<span data-ttu-id="d5946-675">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-675">This is a compile-time function.</span></span> <span data-ttu-id="d5946-676">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-676">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-677">例</span><span class="sxs-lookup"><span data-stu-id="d5946-677">Example</span></span>

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

## <a name="menuitemdisplaystr"></a><span data-ttu-id="d5946-678">menuItemDisplayStr</span><span class="sxs-lookup"><span data-stu-id="d5946-678">menuItemDisplayStr</span></span>
<span data-ttu-id="d5946-679">指定したメニュー項目の表示がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-679">Validates that the specified menu item display exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-680">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-680">Syntax</span></span>

```xpp
str menuitemdisplaystr(class menuItem)
```

### <a name="parameters"></a><span data-ttu-id="d5946-681">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-681">Parameters</span></span>

| <span data-ttu-id="d5946-682">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-682">Parameter</span></span> | <span data-ttu-id="d5946-683">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-683">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="d5946-684">codename</span><span class="sxs-lookup"><span data-stu-id="d5946-684">codename</span></span>  | <span data-ttu-id="d5946-685">検証するメニュー項目nの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-685">The name of the menu item display to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-686">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-686">Return Value</span></span>

<span data-ttu-id="d5946-687">有効な場合の、指定されたメニューの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-687">The name of the specified menu item display, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-688">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-688">Remarks</span></span>

<span data-ttu-id="d5946-689">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-689">This is a compile-time function.</span></span> <span data-ttu-id="d5946-690">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-690">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-691">例</span><span class="sxs-lookup"><span data-stu-id="d5946-691">Example</span></span>

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

## <a name="menuitemoutputstr"></a><span data-ttu-id="d5946-692">menuItemOutputStr</span><span class="sxs-lookup"><span data-stu-id="d5946-692">menuItemOutputStr</span></span>
<span data-ttu-id="d5946-693">指定したメニュー項目の出力がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-693">Validates that the specified menu item output exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-694">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-694">Syntax</span></span>

```xpp
str menuItemOutputStr(class menuitem)
```

### <a name="parameters"></a><span data-ttu-id="d5946-695">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-695">Parameters</span></span>

| <span data-ttu-id="d5946-696">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-696">Parameter</span></span> | <span data-ttu-id="d5946-697">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-697">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="d5946-698">codename</span><span class="sxs-lookup"><span data-stu-id="d5946-698">codename</span></span>  | <span data-ttu-id="d5946-699">検証するメニュー項目出力の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-699">The name of the menu item output to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-700">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-700">Return Value</span></span>

<span data-ttu-id="d5946-701">有効な場合、指定されたメニュー項目が出力されます。</span><span class="sxs-lookup"><span data-stu-id="d5946-701">The specified menu item output if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-702">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-702">Remarks</span></span>

<span data-ttu-id="d5946-703">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-703">This is a compile-time function.</span></span> <span data-ttu-id="d5946-704">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-704">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-705">例</span><span class="sxs-lookup"><span data-stu-id="d5946-705">Example</span></span>

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

## <a name="menustr"></a><span data-ttu-id="d5946-706">menuStr</span><span class="sxs-lookup"><span data-stu-id="d5946-706">menuStr</span></span>
<span data-ttu-id="d5946-707">指定したメニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-707">Validates that the specified menu exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-708">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-708">Syntax</span></span>

```xpp
str menuStr(class menu)
```

### <a name="parameters"></a><span data-ttu-id="d5946-709">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-709">Parameters</span></span>

| <span data-ttu-id="d5946-710">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-710">Parameter</span></span> | <span data-ttu-id="d5946-711">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-711">Description</span></span>                       |
|-----------|-----------------------------------|
| <span data-ttu-id="d5946-712">メニュー</span><span class="sxs-lookup"><span data-stu-id="d5946-712">menu</span></span>      | <span data-ttu-id="d5946-713">検証するメニューの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-713">The name of the menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-714">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-714">Return Value</span></span>

<span data-ttu-id="d5946-715">有効な場合の指定されたメニュー項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-715">The name of the specified menu item if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-716">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-716">Remarks</span></span>

<span data-ttu-id="d5946-717">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-717">This is a compile-time function.</span></span> <span data-ttu-id="d5946-718">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-718">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-719">例</span><span class="sxs-lookup"><span data-stu-id="d5946-719">Example</span></span>

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

## <a name="methodstr"></a><span data-ttu-id="d5946-720">methodStr</span><span class="sxs-lookup"><span data-stu-id="d5946-720">methodStr</span></span>
<span data-ttu-id="d5946-721">指定したメソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-721">Validates that the specified method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-722">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-722">Syntax</span></span>

```xpp
str methodStr(class class, int method)
```

### <a name="parameters"></a><span data-ttu-id="d5946-723">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-723">Parameters</span></span>

| <span data-ttu-id="d5946-724">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-724">Parameter</span></span> | <span data-ttu-id="d5946-725">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-725">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="d5946-726">クラス</span><span class="sxs-lookup"><span data-stu-id="d5946-726">class</span></span>     | <span data-ttu-id="d5946-727">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-727">The name of the class.</span></span>              |
| <span data-ttu-id="d5946-728">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5946-728">method</span></span>    | <span data-ttu-id="d5946-729">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-729">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-730">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-730">Return Value</span></span>

<span data-ttu-id="d5946-731">有効な場合の、指定されたメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-731">The name of the specified method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-732">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-732">Remarks</span></span>

<span data-ttu-id="d5946-733">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-733">This is a compile-time function.</span></span> <span data-ttu-id="d5946-734">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-734">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-735">例</span><span class="sxs-lookup"><span data-stu-id="d5946-735">Example</span></span>

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

## <a name="minint"></a><span data-ttu-id="d5946-736">minInt</span><span class="sxs-lookup"><span data-stu-id="d5946-736">minInt</span></span>
<span data-ttu-id="d5946-737">**int** 型に格納可能な最小符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-737">Retrieves the minimum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-738">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-738">Syntax</span></span>

```xpp
int minInt()
```

### <a name="return-value"></a><span data-ttu-id="d5946-739">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-739">Return Value</span></span>

<span data-ttu-id="d5946-740">**int** 型の最小値です。</span><span class="sxs-lookup"><span data-stu-id="d5946-740">The minimum value of an **int** type.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-741">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-741">Remarks</span></span>

<span data-ttu-id="d5946-742">その他の整数値は、戻り値以上になります。</span><span class="sxs-lookup"><span data-stu-id="d5946-742">Any other integer value will be greater than or equal to the returned value.</span></span> <span data-ttu-id="d5946-743">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-743">This is a compile-time function.</span></span> <span data-ttu-id="d5946-744">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-744">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-745">例</span><span class="sxs-lookup"><span data-stu-id="d5946-745">Example</span></span>

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

## <a name="privilegestr"></a><span data-ttu-id="d5946-746">privilegeStr</span><span class="sxs-lookup"><span data-stu-id="d5946-746">privilegeStr</span></span>
<span data-ttu-id="d5946-747">権限の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-747">Returns the name of the privilege.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-748">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-748">Syntax</span></span>

```xpp
str privilegeStr(str privilege)
```

### <a name="parameters"></a><span data-ttu-id="d5946-749">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-749">Parameters</span></span>

| <span data-ttu-id="d5946-750">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-750">Parameter</span></span> | <span data-ttu-id="d5946-751">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-751">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="d5946-752">権限</span><span class="sxs-lookup"><span data-stu-id="d5946-752">privilege</span></span> | <span data-ttu-id="d5946-753">名前を返す対象の特権。</span><span class="sxs-lookup"><span data-stu-id="d5946-753">The privilege for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-754">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-754">Return Value</span></span>

<span data-ttu-id="d5946-755">権限の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-755">The name of the privilege.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-756">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-756">Remarks</span></span>

<span data-ttu-id="d5946-757">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-757">This is a compile-time function.</span></span> <span data-ttu-id="d5946-758">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-758">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-759">例</span><span class="sxs-lookup"><span data-stu-id="d5946-759">Example</span></span>

<span data-ttu-id="d5946-760">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-760">No example.</span></span>

## <a name="querydatasourcestr"></a><span data-ttu-id="d5946-761">queryDatasourceStr</span><span class="sxs-lookup"><span data-stu-id="d5946-761">queryDatasourceStr</span></span>
<span data-ttu-id="d5946-762">X++ コンパイラは、データ ソースがクエリに存在するかどうかをチェックし、関数呼び出しを有効なデータ ソース名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d5946-762">Causes the X++ compiler to check whether the data source exists on the query, and to replace the function call with a string of the valid data source name.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-763">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-763">Syntax</span></span>

```xpp
str queryDataSourceStr(queryName, dataSourceName)
```

### <a name="parameters"></a><span data-ttu-id="d5946-764">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-764">Parameters</span></span>

| <span data-ttu-id="d5946-765">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-765">Parameter</span></span>      | <span data-ttu-id="d5946-766">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-766">Description</span></span>                                                               |
|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="d5946-767">queryName</span><span class="sxs-lookup"><span data-stu-id="d5946-767">queryName</span></span>      | <span data-ttu-id="d5946-768">引用符ではなく、クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-768">The name of the query, not in quotation marks.</span></span>                            |
| <span data-ttu-id="d5946-769">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="d5946-769">dataSourceName</span></span> | <span data-ttu-id="d5946-770">クエリ上のデータ ソースの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="d5946-770">The name of the data source that is on the query, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-771">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-771">Return Value</span></span>

<span data-ttu-id="d5946-772">アプリケーション エクスプローラーで表示されるデータ ソースの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-772">A string that contains the name of the data source as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-773">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-773">Remarks</span></span>

<span data-ttu-id="d5946-774">データ ソースがクエリに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5946-774">A compile error is issued if the compiler determines that the data source does not exist on the query.</span></span> <span data-ttu-id="d5946-775">X++ コードが引用符が含まれる文字列を使用してデータ ソースの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="d5946-775">If your X++ code uses a string that contains quotation marks to supply the data source name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="d5946-776">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="d5946-776">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="d5946-777">コンパイラにより実行される **queryDataSourceStr** などの X++ 関数は、コンパイル時関数とみなされます。</span><span class="sxs-lookup"><span data-stu-id="d5946-777">X++ functions such as **queryDataSourceStr** that are executed by the compiler are referred to as compile-time functions or compile-time functions.</span></span> <span data-ttu-id="d5946-778">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="d5946-778">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="d5946-779">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="d5946-779">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="d5946-780">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-780">This is a compile-time function.</span></span> <span data-ttu-id="d5946-781">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-781">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-782">例</span><span class="sxs-lookup"><span data-stu-id="d5946-782">Example</span></span>

<span data-ttu-id="d5946-783">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-783">No example.</span></span>

## <a name="querymethodstr"></a><span data-ttu-id="d5946-784">queryMethodStr</span><span class="sxs-lookup"><span data-stu-id="d5946-784">queryMethodStr</span></span>
<span data-ttu-id="d5946-785">クエリのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-785">Returns the name of a method of a query.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-786">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-786">Syntax</span></span>

```xpp
str queryMethodStr(str queryName, str methodName)
```

### <a name="parameters"></a><span data-ttu-id="d5946-787">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-787">Parameters</span></span>

| <span data-ttu-id="d5946-788">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-788">Parameter</span></span>  | <span data-ttu-id="d5946-789">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-789">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="d5946-790">queryName</span><span class="sxs-lookup"><span data-stu-id="d5946-790">queryName</span></span>  | <span data-ttu-id="d5946-791">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-791">The name of the query.</span></span>  |
| <span data-ttu-id="d5946-792">methodName</span><span class="sxs-lookup"><span data-stu-id="d5946-792">methodName</span></span> | <span data-ttu-id="d5946-793">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="d5946-793">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-794">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-794">Return Value</span></span>

<span data-ttu-id="d5946-795">クエリのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-795">The name of a method in a query.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-796">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-796">Remarks</span></span>

<span data-ttu-id="d5946-797">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-797">This is a compile-time function.</span></span> <span data-ttu-id="d5946-798">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-798">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-799">例</span><span class="sxs-lookup"><span data-stu-id="d5946-799">Example</span></span>

<span data-ttu-id="d5946-800">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-800">No example.</span></span>

## <a name="querystr"></a><span data-ttu-id="d5946-801">queryStr</span><span class="sxs-lookup"><span data-stu-id="d5946-801">queryStr</span></span>
<span data-ttu-id="d5946-802">既存のクエリを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-802">Retrieves a string that represents an existing query.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-803">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-803">Syntax</span></span>

```xpp
str queryStr(str query)
```

### <a name="parameters"></a><span data-ttu-id="d5946-804">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-804">Parameters</span></span>

| <span data-ttu-id="d5946-805">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-805">Parameter</span></span> | <span data-ttu-id="d5946-806">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-806">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="d5946-807">クエリ</span><span class="sxs-lookup"><span data-stu-id="d5946-807">query</span></span>     | <span data-ttu-id="d5946-808">取得するクエリ。</span><span class="sxs-lookup"><span data-stu-id="d5946-808">The query to retrieve.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-809">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-809">Return Value</span></span>

<span data-ttu-id="d5946-810">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-810">The name of the query.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-811">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-811">Remarks</span></span>

<span data-ttu-id="d5946-812">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-812">This is a compile-time function.</span></span> <span data-ttu-id="d5946-813">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-813">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-814">例</span><span class="sxs-lookup"><span data-stu-id="d5946-814">Example</span></span>

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

## <a name="reportstr"></a><span data-ttu-id="d5946-815">reportStr</span><span class="sxs-lookup"><span data-stu-id="d5946-815">reportStr</span></span>
<span data-ttu-id="d5946-816">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-816">Retrieves a string that represents the name of the specified report.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-817">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-817">Syntax</span></span>

```xpp
str reportStr(str report)
```

### <a name="parameters"></a><span data-ttu-id="d5946-818">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-818">Parameters</span></span>

| <span data-ttu-id="d5946-819">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-819">Parameter</span></span> | <span data-ttu-id="d5946-820">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-820">Description</span></span>                              |
|-----------|------------------------------------------|
| <span data-ttu-id="d5946-821">レポート</span><span class="sxs-lookup"><span data-stu-id="d5946-821">report</span></span>    | <span data-ttu-id="d5946-822">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="d5946-822">The report for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-823">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-823">Return Value</span></span>

<span data-ttu-id="d5946-824">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-824">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-825">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-825">Remarks</span></span>

<span data-ttu-id="d5946-826">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-826">This is a compile-time function.</span></span> <span data-ttu-id="d5946-827">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-827">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-828">例</span><span class="sxs-lookup"><span data-stu-id="d5946-828">Example</span></span>

<span data-ttu-id="d5946-829">次の例では、**AssetAddition** レポートの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d5946-829">The following example assigns the name of the **AssetAddition** report to the *MyTxt* variable.</span></span>

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

## <a name="resourcestr"></a><span data-ttu-id="d5946-830">resourceStr</span><span class="sxs-lookup"><span data-stu-id="d5946-830">resourceStr</span></span>
<span data-ttu-id="d5946-831">指定したリソースがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-831">Validates that the specified resource exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-832">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-832">Syntax</span></span>

```xpp
str resourceStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="d5946-833">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-833">Parameters</span></span>

| <span data-ttu-id="d5946-834">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-834">Parameter</span></span>    | <span data-ttu-id="d5946-835">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-835">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="d5946-836">resourcename</span><span class="sxs-lookup"><span data-stu-id="d5946-836">resourcename</span></span> | <span data-ttu-id="d5946-837">検証するリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-837">The name of the resource to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-838">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-838">Return Value</span></span>

<span data-ttu-id="d5946-839">有効な場合の、指定されたリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-839">The name of the specified resource, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-840">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-840">Remarks</span></span>

<span data-ttu-id="d5946-841">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-841">This is a compile-time function.</span></span> <span data-ttu-id="d5946-842">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-842">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-843">例</span><span class="sxs-lookup"><span data-stu-id="d5946-843">Example</span></span>

```xpp
{
    print "Str for resource StyleSheet_Help_Axapta is " 
        + resourceStr(StyleSheet_Help_Axapta);
    pause;
}
```

## <a name="rolestr"></a><span data-ttu-id="d5946-844">roleStr</span><span class="sxs-lookup"><span data-stu-id="d5946-844">roleStr</span></span>
<span data-ttu-id="d5946-845">指定したセキュリティ ロールの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-845">Retrieves a string that represents the name of the specified security role.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-846">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-846">Syntax</span></span>

```xpp
str roleStr(str securityRole)
```

### <a name="parameters"></a><span data-ttu-id="d5946-847">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-847">Parameters</span></span>

| <span data-ttu-id="d5946-848">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-848">Parameter</span></span>    | <span data-ttu-id="d5946-849">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-849">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="d5946-850">securityRole</span><span class="sxs-lookup"><span data-stu-id="d5946-850">securityRole</span></span> | <span data-ttu-id="d5946-851">セキュリティ ロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="d5946-851">The name of the security role.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-852">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-852">Return Value</span></span>

<span data-ttu-id="d5946-853">文字列のセキュリティ ロールの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-853">The name of the security role in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-854">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-854">Remarks</span></span>

<span data-ttu-id="d5946-855">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-855">This is a compile-time function.</span></span> <span data-ttu-id="d5946-856">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-856">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-857">例</span><span class="sxs-lookup"><span data-stu-id="d5946-857">Example</span></span>

<span data-ttu-id="d5946-858">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-858">No example.</span></span>

## <a name="ssrsreportstr"></a><span data-ttu-id="d5946-859">ssrsReportStr</span><span class="sxs-lookup"><span data-stu-id="d5946-859">ssrsReportStr</span></span>
<span data-ttu-id="d5946-860">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-860">Retrieves a string that represents the name of the specified report.</span></span> <span data-ttu-id="d5946-861">レポート コントローラー クラスで実行されるレポートを指定する場合は、この関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="d5946-861">Use this function when you want to specify the report that should be run by a report controller class.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-862">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-862">Syntax</span></span>

```xpp
str ssrsReportStr(str report, str design)
```

### <a name="parameters"></a><span data-ttu-id="d5946-863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-863">Parameters</span></span>

| <span data-ttu-id="d5946-864">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-864">Parameter</span></span> | <span data-ttu-id="d5946-865">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-865">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| <span data-ttu-id="d5946-866">レポート</span><span class="sxs-lookup"><span data-stu-id="d5946-866">report</span></span>    | <span data-ttu-id="d5946-867">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="d5946-867">The report to return the name for.</span></span>                         |
| <span data-ttu-id="d5946-868">design</span><span class="sxs-lookup"><span data-stu-id="d5946-868">design</span></span>    | <span data-ttu-id="d5946-869">レポートに関連付けられているデザインの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-869">The name of the design that is associated with the report.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-870">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-870">Return Value</span></span>

<span data-ttu-id="d5946-871">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-871">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-872">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-872">Remarks</span></span>

<span data-ttu-id="d5946-873">**ssrsReportStr** 関数は、有効なレポートに属しているかどうかを検証するために、渡された 2 つの値を解析します。</span><span class="sxs-lookup"><span data-stu-id="d5946-873">The **ssrsReportStr** function parses the two values that are passed to it, to validate whether they belong to a valid report.</span></span> <span data-ttu-id="d5946-874">コントローラーが、どのレポート デザインの組み合わせを呼び出す必要があるかを判断できるように、メニュー項目が controller() を指しているときは、レポート名を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5946-874">The report name must be set when a menu item points to a controller(), so that the controller can determine which report-design combination must be invoked.</span></span> <span data-ttu-id="d5946-875">**ssrsReportStr** 関数を使用すると、レポートおよびデザイン名のコンパイル時の検証で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d5946-875">Use of the **ssrsReportStr** function provides the benefit of compile-time validation for the report and design name.</span></span> <span data-ttu-id="d5946-876">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-876">This is a compile-time function.</span></span> <span data-ttu-id="d5946-877">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-877">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-878">例</span><span class="sxs-lookup"><span data-stu-id="d5946-878">Example</span></span>

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

## <a name="staticdelegatestr"></a><span data-ttu-id="d5946-879">staticDelegateStr</span><span class="sxs-lookup"><span data-stu-id="d5946-879">staticDelegateStr</span></span>
<span data-ttu-id="d5946-880">静的デリゲートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="d5946-880">Returns the name of a static delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-881">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-881">Syntax</span></span>

```xpp
str staticDelegateStr(str class, str delegate)
```

### <a name="parameters"></a><span data-ttu-id="d5946-882">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-882">Parameters</span></span>

| <span data-ttu-id="d5946-883">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-883">Parameter</span></span> | <span data-ttu-id="d5946-884">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-884">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="d5946-885">クラス</span><span class="sxs-lookup"><span data-stu-id="d5946-885">class</span></span>     | <span data-ttu-id="d5946-886">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-886">The name of a class, table, or form.</span></span> |
| <span data-ttu-id="d5946-887">デリゲート</span><span class="sxs-lookup"><span data-stu-id="d5946-887">delegate</span></span>  | <span data-ttu-id="d5946-888">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="d5946-888">The name of the delegate.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="d5946-889">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-889">Return Value</span></span>

<span data-ttu-id="d5946-890">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="d5946-890">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-891">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-891">Remarks</span></span>

<span data-ttu-id="d5946-892">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-892">This is a compile-time function.</span></span> <span data-ttu-id="d5946-893">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-893">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-894">例</span><span class="sxs-lookup"><span data-stu-id="d5946-894">Example</span></span>

<span data-ttu-id="d5946-895">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-895">No example.</span></span>

## <a name="staticmethodstr"></a><span data-ttu-id="d5946-896">staticMethodStr</span><span class="sxs-lookup"><span data-stu-id="d5946-896">staticMethodStr</span></span>
<span data-ttu-id="d5946-897">指定した静的メソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-897">Validates that the specified static method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-898">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-898">Syntax</span></span>

```xpp
str staticMethodStr(class class, int method)
```

### <a name="parameters"></a><span data-ttu-id="d5946-899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-899">Parameters</span></span>

| <span data-ttu-id="d5946-900">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-900">Parameter</span></span> | <span data-ttu-id="d5946-901">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-901">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="d5946-902">クラス</span><span class="sxs-lookup"><span data-stu-id="d5946-902">class</span></span>     | <span data-ttu-id="d5946-903">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-903">The name of the class.</span></span>                     |
| <span data-ttu-id="d5946-904">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5946-904">method</span></span>    | <span data-ttu-id="d5946-905">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-905">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-906">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-906">Return Value</span></span>

<span data-ttu-id="d5946-907">有効な場合の、指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-907">The name of the static method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-908">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-908">Remarks</span></span>

<span data-ttu-id="d5946-909">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-909">This is a compile-time function.</span></span> <span data-ttu-id="d5946-910">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-910">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-911">例</span><span class="sxs-lookup"><span data-stu-id="d5946-911">Example</span></span>

<span data-ttu-id="d5946-912">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-912">No example.</span></span>

## <a name="tablecollectionstr"></a><span data-ttu-id="d5946-913">tableCollectionStr</span><span class="sxs-lookup"><span data-stu-id="d5946-913">tableCollectionStr</span></span>
<span data-ttu-id="d5946-914">指定したテーブル コレクションがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-914">Validates that the specified table collection exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-915">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-915">Syntax</span></span>

```xpp
str tableCollectionStr(class tablecollection)
```

### <a name="parameters"></a><span data-ttu-id="d5946-916">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-916">Parameters</span></span>

| <span data-ttu-id="d5946-917">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-917">Parameter</span></span>       | <span data-ttu-id="d5946-918">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-918">Description</span></span>                                   |
|-----------------|-----------------------------------------------|
| <span data-ttu-id="d5946-919">tablecollection</span><span class="sxs-lookup"><span data-stu-id="d5946-919">tablecollection</span></span> | <span data-ttu-id="d5946-920">検証するテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-920">The name of the table collection to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-921">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-921">Return Value</span></span>

<span data-ttu-id="d5946-922">有効な場合の、指定されたテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-922">The name of the specified table collection, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-923">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-923">Remarks</span></span>

<span data-ttu-id="d5946-924">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-924">This is a compile-time function.</span></span> <span data-ttu-id="d5946-925">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-925">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-926">例</span><span class="sxs-lookup"><span data-stu-id="d5946-926">Example</span></span>

<span data-ttu-id="d5946-927">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-927">No example.</span></span>

## <a name="tablefieldgroupstr"></a><span data-ttu-id="d5946-928">tableFieldGroupStr</span><span class="sxs-lookup"><span data-stu-id="d5946-928">tableFieldGroupStr</span></span>
<span data-ttu-id="d5946-929">文字列としてフィールド グループの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-929">Retrieves the name of a field group as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-930">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-930">Syntax</span></span>

```xpp
str tableFieldGroupStr(str tableName, str fieldGroupName)
```

### <a name="parameters"></a><span data-ttu-id="d5946-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-931">Parameters</span></span>

| <span data-ttu-id="d5946-932">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-932">Parameter</span></span>      | <span data-ttu-id="d5946-933">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-933">Description</span></span>                              |
|----------------|------------------------------------------|
| <span data-ttu-id="d5946-934">tableName</span><span class="sxs-lookup"><span data-stu-id="d5946-934">tableName</span></span>      | <span data-ttu-id="d5946-935">フィールド グループを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="d5946-935">The table that contains the field group.</span></span> |
| <span data-ttu-id="d5946-936">fieldGroupName</span><span class="sxs-lookup"><span data-stu-id="d5946-936">fieldGroupName</span></span> | <span data-ttu-id="d5946-937">テーブル内のフィールド グループ。</span><span class="sxs-lookup"><span data-stu-id="d5946-937">The field group in the table.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="d5946-938">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-938">Return Value</span></span>

<span data-ttu-id="d5946-939">文字列としてのフィールド グループの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-939">The name of the field group as a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-940">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-940">Remarks</span></span>

<span data-ttu-id="d5946-941">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-941">This is a compile-time function.</span></span> <span data-ttu-id="d5946-942">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-942">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-943">例</span><span class="sxs-lookup"><span data-stu-id="d5946-943">Example</span></span>

<span data-ttu-id="d5946-944">次の例では、**編集** フィールド グループの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-944">The following example retrieves the name of the **Editing** field group as a string.</span></span>

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

## <a name="tablemethodstr"></a><span data-ttu-id="d5946-945">tableMethodStr</span><span class="sxs-lookup"><span data-stu-id="d5946-945">tableMethodStr</span></span>
<span data-ttu-id="d5946-946">指定したメソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-946">Validates that the specified method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-947">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-947">Syntax</span></span>

```xpp
str tableMethodStr(int table, int method)
```

### <a name="parameters"></a><span data-ttu-id="d5946-948">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-948">Parameters</span></span>

| <span data-ttu-id="d5946-949">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-949">Parameter</span></span> | <span data-ttu-id="d5946-950">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-950">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="d5946-951">テーブル</span><span class="sxs-lookup"><span data-stu-id="d5946-951">table</span></span>     | <span data-ttu-id="d5946-952">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-952">The name of the table.</span></span>              |
| <span data-ttu-id="d5946-953">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5946-953">method</span></span>    | <span data-ttu-id="d5946-954">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-954">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-955">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-955">Return Value</span></span>

<span data-ttu-id="d5946-956">有効な場合の、メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-956">The name of the method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-957">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-957">Remarks</span></span>

<span data-ttu-id="d5946-958">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-958">This is a compile-time function.</span></span> <span data-ttu-id="d5946-959">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-959">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-960">例</span><span class="sxs-lookup"><span data-stu-id="d5946-960">Example</span></span>

<span data-ttu-id="d5946-961">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-961">No example.</span></span>

## <a name="tablenum"></a><span data-ttu-id="d5946-962">tableNum</span><span class="sxs-lookup"><span data-stu-id="d5946-962">tableNum</span></span>
<span data-ttu-id="d5946-963">特定のテーブルのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-963">Retrieves the table ID of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-964">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-964">Syntax</span></span>

```xpp
int tableNum(str table)
```

### <a name="parameters"></a><span data-ttu-id="d5946-965">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-965">Parameters</span></span>

| <span data-ttu-id="d5946-966">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-966">Parameter</span></span> | <span data-ttu-id="d5946-967">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-967">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="d5946-968">テーブル</span><span class="sxs-lookup"><span data-stu-id="d5946-968">table</span></span>     | <span data-ttu-id="d5946-969">テーブル ID を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="d5946-969">The table to retrieve the table ID for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-970">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-970">Return Value</span></span>

<span data-ttu-id="d5946-971">特定のテーブルのテーブル ID</span><span class="sxs-lookup"><span data-stu-id="d5946-971">The table ID of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-972">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-972">Remarks</span></span>

<span data-ttu-id="d5946-973">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-973">This is a compile-time function.</span></span> <span data-ttu-id="d5946-974">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-974">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-975">例</span><span class="sxs-lookup"><span data-stu-id="d5946-975">Example</span></span>

<span data-ttu-id="d5946-976">次の例では、**tableID** 変数を 77 に設定します。これは、**CustTable** テーブルの **ID** です。</span><span class="sxs-lookup"><span data-stu-id="d5946-976">The following example sets the **tableID** variable to 77, which is the **ID** of the **CustTable** table.</span></span>

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

## <a name="tablepname"></a><span data-ttu-id="d5946-977">tablePName</span><span class="sxs-lookup"><span data-stu-id="d5946-977">tablePName</span></span>
<span data-ttu-id="d5946-978">指定されたテーブルの出力可能な名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-978">Retrieves a string that contains the printable name of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-979">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-979">Syntax</span></span>

```xpp
str tablePName(str table)
```

### <a name="parameters"></a><span data-ttu-id="d5946-980">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-980">Parameters</span></span>

| <span data-ttu-id="d5946-981">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-981">Parameter</span></span> | <span data-ttu-id="d5946-982">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-982">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="d5946-983">テーブル</span><span class="sxs-lookup"><span data-stu-id="d5946-983">table</span></span>     | <span data-ttu-id="d5946-984">印刷可能な名前を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="d5946-984">The table to retrieve the printable name for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-985">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-985">Return Value</span></span>

<span data-ttu-id="d5946-986">指定されたテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-986">The name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-987">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-987">Remarks</span></span>

<span data-ttu-id="d5946-988">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-988">This is a compile-time function.</span></span> <span data-ttu-id="d5946-989">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-989">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-990">例</span><span class="sxs-lookup"><span data-stu-id="d5946-990">Example</span></span>

<span data-ttu-id="d5946-991">次の例では、**CustTable** テーブルのラベルを *MyText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d5946-991">The following example assigns the label of the **CustTable** table to the *MyText* variable.</span></span>

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

## <a name="tablestaticmethodstr"></a><span data-ttu-id="d5946-992">tableStaticMethodStr</span><span class="sxs-lookup"><span data-stu-id="d5946-992">tableStaticMethodStr</span></span>
<span data-ttu-id="d5946-993">指定した静的メソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-993">Validates that the specified static method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-994">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-994">Syntax</span></span>

```xpp
str tableStaticMethodStr(int table, int method)
```

### <a name="parameters"></a><span data-ttu-id="d5946-995">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-995">Parameters</span></span>

| <span data-ttu-id="d5946-996">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-996">Parameter</span></span> | <span data-ttu-id="d5946-997">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-997">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="d5946-998">テーブル</span><span class="sxs-lookup"><span data-stu-id="d5946-998">table</span></span>     | <span data-ttu-id="d5946-999">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-999">The name of the table.</span></span>                     |
| <span data-ttu-id="d5946-1000">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5946-1000">method</span></span>    | <span data-ttu-id="d5946-1001">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1001">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1002">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1002">Return Value</span></span>

<span data-ttu-id="d5946-1003">指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1003">The name of the specified static method.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1004">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1004">Remarks</span></span>

<span data-ttu-id="d5946-1005">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1005">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1006">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1006">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1007">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1007">Example</span></span>

<span data-ttu-id="d5946-1008">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-1008">No example.</span></span>

## <a name="tablestr"></a><span data-ttu-id="d5946-1009">tableStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1009">tableStr</span></span>
<span data-ttu-id="d5946-1010">指定したテーブルの名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1010">Retrieves a string that contains the name the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1011">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1011">Syntax</span></span>

```xpp
str tableStr(str table)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1012">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1012">Parameters</span></span>

| <span data-ttu-id="d5946-1013">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1013">Parameter</span></span> | <span data-ttu-id="d5946-1014">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1014">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="d5946-1015">テーブル</span><span class="sxs-lookup"><span data-stu-id="d5946-1015">table</span></span>     | <span data-ttu-id="d5946-1016">文字列を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="d5946-1016">The table to retrieve a string for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1017">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1017">Return Value</span></span>

<span data-ttu-id="d5946-1018">指定したテーブルの名前を含む文字列値。</span><span class="sxs-lookup"><span data-stu-id="d5946-1018">A string value that contains the name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1019">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1019">Remarks</span></span>

<span data-ttu-id="d5946-1020">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1020">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1021">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1021">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1022">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1022">Example</span></span>

<span data-ttu-id="d5946-1023">次の例では、**CustTable** テーブルの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d5946-1023">The following example assigns the name of the **CustTable** table to the *MyTxt* variable.</span></span>

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

## <a name="tilestr"></a><span data-ttu-id="d5946-1024">tileStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1024">tileStr</span></span>
<span data-ttu-id="d5946-1025">指定したタイルの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1025">Retrieves a string that represents the name of the specified tile.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1026">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1026">Syntax</span></span>

```xpp
str tileStr(str tile)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1027">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1027">Parameters</span></span>

| <span data-ttu-id="d5946-1028">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1028">Parameter</span></span> | <span data-ttu-id="d5946-1029">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1029">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="d5946-1030">tile</span><span class="sxs-lookup"><span data-stu-id="d5946-1030">tile</span></span>      | <span data-ttu-id="d5946-1031">タイルの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1031">The name of the tile.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1032">Return Value</span></span>

<span data-ttu-id="d5946-1033">文字列のタイルの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1033">The name of the tile in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1034">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1034">Remarks</span></span>

<span data-ttu-id="d5946-1035">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1035">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1036">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1036">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1037">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1037">Example</span></span>

<span data-ttu-id="d5946-1038">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-1038">No example.</span></span>

## <a name="varstr"></a><span data-ttu-id="d5946-1039">varStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1039">varStr</span></span>
<span data-ttu-id="d5946-1040">指定した変数の名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1040">Retrieves a string that contains the name of the specified variable.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1041">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1041">Syntax</span></span>

```xpp
str varStr(str var)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1042">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1042">Parameters</span></span>

| <span data-ttu-id="d5946-1043">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1043">Parameter</span></span> | <span data-ttu-id="d5946-1044">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1044">Description</span></span>               |
|-----------|---------------------------|
| <span data-ttu-id="d5946-1045">var</span><span class="sxs-lookup"><span data-stu-id="d5946-1045">var</span></span>       | <span data-ttu-id="d5946-1046">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1046">The name of the variable.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1047">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1047">Return Value</span></span>

<span data-ttu-id="d5946-1048">指定した変数の名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-1048">A string that contains the name of the specified variable.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1049">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1049">Remarks</span></span>

<span data-ttu-id="d5946-1050">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1050">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1051">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1051">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1052">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1052">Example</span></span>

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

## <a name="webactionitemstr"></a><span data-ttu-id="d5946-1053">webActionItemStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1053">webActionItemStr</span></span>
<span data-ttu-id="d5946-1054">指定した Web アクション項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1054">Validates that the specified web action item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1055">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1055">Syntax</span></span>

```xpp
str webActionItemStr(class webactionitem)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1056">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1056">Parameters</span></span>

| <span data-ttu-id="d5946-1057">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1057">Parameter</span></span>     | <span data-ttu-id="d5946-1058">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1058">Description</span></span>                                  |
|---------------|----------------------------------------------|
| <span data-ttu-id="d5946-1059">webactionitem</span><span class="sxs-lookup"><span data-stu-id="d5946-1059">webactionitem</span></span> | <span data-ttu-id="d5946-1060">検証する Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1060">The name of the web action item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1061">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1061">Return Value</span></span>

<span data-ttu-id="d5946-1062">有効な場合の、指定された Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1062">The name of the specified web action item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1063">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1063">Remarks</span></span>

<span data-ttu-id="d5946-1064">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1064">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1065">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1065">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1066">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1066">Example</span></span>

```xpp
{
    str s;
    ;
    s = webActionItemStr(EPFlushData);
    print "webactionitem str is " + s;
    pause;
}
```

## <a name="webdisplaycontentitemstr"></a><span data-ttu-id="d5946-1067">webDisplayContentItemStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1067">webDisplayContentItemStr</span></span>
<span data-ttu-id="d5946-1068">指定したWeb 表示のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1068">Validates that the specified web display content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1069">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1069">Syntax</span></span>

    str webDisplayContentItemStr(class webdisplaycontentitem)

### <a name="parameters"></a><span data-ttu-id="d5946-1070">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1070">Parameters</span></span>

| <span data-ttu-id="d5946-1071">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1071">Parameter</span></span>             | <span data-ttu-id="d5946-1072">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1072">Description</span></span>                                           |
|-----------------------|-------------------------------------------------------|
| <span data-ttu-id="d5946-1073">webdisplaycontentitem</span><span class="sxs-lookup"><span data-stu-id="d5946-1073">webdisplaycontentitem</span></span> | <span data-ttu-id="d5946-1074">検証する Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1074">The name of the web display content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1075">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1075">Return Value</span></span>

<span data-ttu-id="d5946-1076">有効な場合の、指定された Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1076">The name of the specified web display content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1077">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1077">Remarks</span></span>

<span data-ttu-id="d5946-1078">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1078">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1079">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1079">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1080">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1080">Example</span></span>

```xpp
{
    str s;
    ;

    s = webDisplayContentItemStr(EPAdmin);
    print "string for webcontent display item EPAdmin is " + s;
    pause;
}
```

## <a name="webformstr"></a><span data-ttu-id="d5946-1081">webFormStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1081">webFormStr</span></span>
<span data-ttu-id="d5946-1082">指定した Web フォームがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1082">Validates that the specified web form exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1083">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1083">Syntax</span></span>

```xpp
str webFormStr(str name)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1084">Parameters</span></span>

| <span data-ttu-id="d5946-1085">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1085">Parameter</span></span> | <span data-ttu-id="d5946-1086">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1086">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="d5946-1087">名前</span><span class="sxs-lookup"><span data-stu-id="d5946-1087">name</span></span>      | <span data-ttu-id="d5946-1088">検証する Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1088">The name of the web form to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1089">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1089">Return Value</span></span>

<span data-ttu-id="d5946-1090">有効な場合の、指定された Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1090">The name of the specified web form, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1091">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1091">Remarks</span></span>

<span data-ttu-id="d5946-1092">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1092">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1093">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1093">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1094">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1094">Example</span></span>

```xpp
{
    str s;
    ;
    s = webFormStr(EPAdmin);
    print "String for web form EPAdmin is " + s;
    pause;
}
```

## <a name="webletitemstr"></a><span data-ttu-id="d5946-1095">webletItemStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1095">webletItemStr</span></span>
<span data-ttu-id="d5946-1096">指定した Weblet 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1096">Validates that the specified weblet item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1097">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1097">Syntax</span></span>

```xpp
str webletItemStr(class webletitem)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1098">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1098">Parameters</span></span>

| <span data-ttu-id="d5946-1099">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1099">Parameter</span></span>  | <span data-ttu-id="d5946-1100">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1100">Description</span></span>                              |
|------------|------------------------------------------|
| <span data-ttu-id="d5946-1101">webletitem</span><span class="sxs-lookup"><span data-stu-id="d5946-1101">webletitem</span></span> | <span data-ttu-id="d5946-1102">検証する Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1102">The name of the weblet item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1103">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1103">Return Value</span></span>

<span data-ttu-id="d5946-1104">有効な場合の、指定された Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1104">The name of the specified weblet item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1105">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1105">Remarks</span></span>

<span data-ttu-id="d5946-1106">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1106">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1107">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1107">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1108">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1108">Example</span></span>

```xpp
{
    str s;
    ;
    s = webletItemStr(WebFormWeblet);
    print "String for WebFormWeblet is " + s;
    pause;
}
```

## <a name="webmenustr"></a><span data-ttu-id="d5946-1109">webMenuStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1109">webMenuStr</span></span>
<span data-ttu-id="d5946-1110">指定した Web メニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1110">Validates that the specified web menu exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1111">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1111">Syntax</span></span>

```xpp
str webMenuStr(str name)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1112">Parameters</span></span>

| <span data-ttu-id="d5946-1113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1113">Parameter</span></span> | <span data-ttu-id="d5946-1114">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1114">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="d5946-1115">名前</span><span class="sxs-lookup"><span data-stu-id="d5946-1115">name</span></span>      | <span data-ttu-id="d5946-1116">検証する Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1116">The name of the web menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1117">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1117">Return Value</span></span>

<span data-ttu-id="d5946-1118">有効な場合の、指定された Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1118">The name of the specified web menu, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1119">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1119">Remarks</span></span>

<span data-ttu-id="d5946-1120">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1120">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1121">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1121">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1122">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1122">Example</span></span>

```xpp
{
    str s;
    ;
    s = webMenuStr(ECPAdmin);
    print "String for web menu ECPAdmin is " + s;
    pause;
}
```

## <a name="weboutputcontentitemstr"></a><span data-ttu-id="d5946-1123">webOutputContentItemStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1123">webOutputContentItemStr</span></span>
<span data-ttu-id="d5946-1124">指定したWeb 出力のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1124">Validates that the specified web output content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1125">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1125">Syntax</span></span>

```xpp
str webOutputContentItemStr(class weboutputcontentitem)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1126">Parameters</span></span>

| <span data-ttu-id="d5946-1127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1127">Parameter</span></span>            | <span data-ttu-id="d5946-1128">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1128">Description</span></span>                                          |
|----------------------|------------------------------------------------------|
| <span data-ttu-id="d5946-1129">weboutputcontentitem</span><span class="sxs-lookup"><span data-stu-id="d5946-1129">weboutputcontentitem</span></span> | <span data-ttu-id="d5946-1130">検証する Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1130">The name of the web output content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1131">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1131">Return Value</span></span>

<span data-ttu-id="d5946-1132">有効な場合の、指定された Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1132">The name of the specified web output content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1133">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1133">Remarks</span></span>

<span data-ttu-id="d5946-1134">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1134">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1135">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1135">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1136">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1136">Example</span></span>

```xpp
{
    str s;
    ;
    s = webOutputContentItemStr(EPPriceList);
    print "string for weboutput content item EPPriceList is " + s;
    pause;
}
```

## <a name="webpagedefstr"></a><span data-ttu-id="d5946-1137">webpageDefStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1137">webpageDefStr</span></span>
<span data-ttu-id="d5946-1138">指定した Web ページ定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1138">Validates that the specified Web page definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1139">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1139">Syntax</span></span>

```xpp
str webpageDefStr(str pagename)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1140">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1140">Parameters</span></span>

| <span data-ttu-id="d5946-1141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1141">Parameter</span></span> | <span data-ttu-id="d5946-1142">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1142">Description</span></span>                                      |
|-----------|--------------------------------------------------|
| <span data-ttu-id="d5946-1143">pagename</span><span class="sxs-lookup"><span data-stu-id="d5946-1143">pagename</span></span>  | <span data-ttu-id="d5946-1144">検証する Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1144">The name of the Web page definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1145">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1145">Return Value</span></span>

<span data-ttu-id="d5946-1146">有効な場合の、指定された Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1146">The name of the specified web-page definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1147">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1147">Remarks</span></span>

<span data-ttu-id="d5946-1148">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1148">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1149">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1149">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1150">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1150">Example</span></span>

<span data-ttu-id="d5946-1151">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-1151">No example.</span></span>

## <a name="webreportstr"></a><span data-ttu-id="d5946-1152">webReportStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1152">webReportStr</span></span>
<span data-ttu-id="d5946-1153">指定した Web レポートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1153">Validates that the specified web report exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1154">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1154">Syntax</span></span>

```xpp
str webReportStr(str name)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1155">Parameters</span></span>

| <span data-ttu-id="d5946-1156">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1156">Parameter</span></span> | <span data-ttu-id="d5946-1157">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1157">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="d5946-1158">名前</span><span class="sxs-lookup"><span data-stu-id="d5946-1158">name</span></span>      | <span data-ttu-id="d5946-1159">検証する Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1159">The name of the web report to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1160">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1160">Return Value</span></span>

<span data-ttu-id="d5946-1161">有効な場合の、指定された Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1161">The name of the specified web report, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1162">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1162">Remarks</span></span>

<span data-ttu-id="d5946-1163">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1163">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1164">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1164">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1165">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1165">Example</span></span>

```xpp
{
    str s;
    ;
    s = webReportStr(EPCSSSalesConfirm);
    print "String for web report EPCSSalesConfirm is " + s;
    pause;
}
```

## <a name="websitedefstr"></a><span data-ttu-id="d5946-1166">websiteDefStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1166">websiteDefStr</span></span>
<span data-ttu-id="d5946-1167">指定した Web サイトの定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1167">Validates that the specified web-site definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1168">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1168">Syntax</span></span>

```xpp
str websiteDefStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1169">Parameters</span></span>

| <span data-ttu-id="d5946-1170">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1170">Parameter</span></span>    | <span data-ttu-id="d5946-1171">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1171">Description</span></span>                                      |
|--------------|--------------------------------------------------|
| <span data-ttu-id="d5946-1172">resourcename</span><span class="sxs-lookup"><span data-stu-id="d5946-1172">resourcename</span></span> | <span data-ttu-id="d5946-1173">検証する Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1173">The name of the Web site definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1174">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1174">Return Value</span></span>

<span data-ttu-id="d5946-1175">有効な場合の、指定された Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1175">The name of the specified web-site definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1176">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1176">Remarks</span></span>

<span data-ttu-id="d5946-1177">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1177">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1178">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1178">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1179">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1179">Example</span></span>

```xpp
{
    str s;
    ;

    s = websiteDefStr(AxSiteDef_1033_xip);
    print "string for web site definition AxSiteDef_1033_xip is " + s;
    pause;
}
```

## <a name="websitetempstr"></a><span data-ttu-id="d5946-1180">webSiteTempStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1180">webSiteTempStr</span></span>
<span data-ttu-id="d5946-1181">指定した Web サイトのテンプレートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1181">Validates that the specified web-site template exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1182">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1182">Syntax</span></span>

```xpp
str websiteTempStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1183">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1183">Parameters</span></span>

| <span data-ttu-id="d5946-1184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1184">Parameter</span></span>    | <span data-ttu-id="d5946-1185">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1185">Description</span></span>                                    |
|--------------|------------------------------------------------|
| <span data-ttu-id="d5946-1186">resourcename</span><span class="sxs-lookup"><span data-stu-id="d5946-1186">resourcename</span></span> | <span data-ttu-id="d5946-1187">検証する Web サイト テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1187">The name of the Web site template to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1188">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1188">Return Value</span></span>

<span data-ttu-id="d5946-1189">有効な場合の、指定された Web テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1189">The name of the specified web-site template, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1190">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1190">Remarks</span></span>

<span data-ttu-id="d5946-1191">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1191">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1192">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1192">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1193">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1193">Example</span></span>

<span data-ttu-id="d5946-1194">例なし。</span><span class="sxs-lookup"><span data-stu-id="d5946-1194">No example.</span></span>

## <a name="webstaticfilestr"></a><span data-ttu-id="d5946-1195">webStaticFileStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1195">webStaticFileStr</span></span>
<span data-ttu-id="d5946-1196">指定した Web 静的ファイルがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1196">Validates that the specified web static file exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1197">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1197">Syntax</span></span>

```xpp
str webStaticFileStr(str pagename)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1198">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1198">Parameters</span></span>

| <span data-ttu-id="d5946-1199">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1199">Parameter</span></span> | <span data-ttu-id="d5946-1200">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1200">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="d5946-1201">pagename</span><span class="sxs-lookup"><span data-stu-id="d5946-1201">pagename</span></span>  | <span data-ttu-id="d5946-1202">検証する Web 静的ファイル テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1202">The name of the web static file to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1203">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1203">Return Value</span></span>

<span data-ttu-id="d5946-1204">有効な場合の、指定された Web 静的ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1204">The name of the specified web static file, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1205">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1205">Remarks</span></span>

<span data-ttu-id="d5946-1206">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1206">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1207">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1207">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1208">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1208">Example</span></span>

```xpp
{
    str s;
    ;

    s = webStaticFileStr(AXEP);
    print "string for web static file AXEP is " + s;
    pause;
}
```

## <a name="weburlitemstr"></a><span data-ttu-id="d5946-1209">webUrlItemStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1209">webUrlItemStr</span></span>
<span data-ttu-id="d5946-1210">指定した Web URL 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1210">Validates that the specified web URL item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1211">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1211">Syntax</span></span>

```xpp
str webUrlItemStr(class weburlitem)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1212">Parameters</span></span>

| <span data-ttu-id="d5946-1213">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1213">Parameter</span></span>  | <span data-ttu-id="d5946-1214">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1214">Description</span></span>                               |
|------------|-------------------------------------------|
| <span data-ttu-id="d5946-1215">weburlitem</span><span class="sxs-lookup"><span data-stu-id="d5946-1215">weburlitem</span></span> | <span data-ttu-id="d5946-1216">検証する Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1216">The name of the web URL item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1217">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1217">Return Value</span></span>

<span data-ttu-id="d5946-1218">有効な場合の、指定された Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1218">The name of the specified web URL item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1219">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1219">Remarks</span></span>

<span data-ttu-id="d5946-1220">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1220">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1221">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1221">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1222">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1222">Example</span></span>

```xpp
{
    str s;
    ;

    s = webUrlItemStr(EPAdmin);
    print "string for web url item EPAdmin is " + s;
    pause;
}
```

## <a name="webwebpartstr"></a><span data-ttu-id="d5946-1223">webWebPartStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1223">webWebPartStr</span></span>
<span data-ttu-id="d5946-1224">指定した Web パーツがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1224">Validates that the specified web part exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1225">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1225">Syntax</span></span>

```xpp
str webWebpartStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1226">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1226">Parameters</span></span>

| <span data-ttu-id="d5946-1227">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1227">Parameter</span></span>    | <span data-ttu-id="d5946-1228">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1228">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="d5946-1229">resourcename</span><span class="sxs-lookup"><span data-stu-id="d5946-1229">resourcename</span></span> | <span data-ttu-id="d5946-1230">検証する Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1230">The name of the web part to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1231">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1231">Return Value</span></span>

<span data-ttu-id="d5946-1232">有効な場合の、指定された Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1232">The name of the specified web part, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1233">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1233">Remarks</span></span>

<span data-ttu-id="d5946-1234">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1234">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1235">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1235">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1236">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1236">Example</span></span>

```xpp
{
    str s;
    ;

    s = webWebpartStr(AxWebParts_cab);
    print "string for web part AxWebParts_cab is " + s;
    pause;
}
```

## <a name="workflowapprovalstr"></a><span data-ttu-id="d5946-1237">workflowApprovalStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1237">workflowApprovalStr</span></span>
<span data-ttu-id="d5946-1238">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー承認の名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1238">Retrieves the name of a workflow approval in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1239">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1239">Syntax</span></span>

```xpp
str workflowapprovalstr(approval approval)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1240">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1240">Parameters</span></span>

| <span data-ttu-id="d5946-1241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1241">Parameter</span></span> | <span data-ttu-id="d5946-1242">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1242">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="d5946-1243">承認</span><span class="sxs-lookup"><span data-stu-id="d5946-1243">approval</span></span>  | <span data-ttu-id="d5946-1244">ワークフローの承認のアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1244">The Application Explorer name of the workflow approval.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1245">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1245">Return Value</span></span>

<span data-ttu-id="d5946-1246">ワークフローの承認のアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-1246">A string that represents the Application Explorer name of the workflow approval.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1247">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1247">Remarks</span></span>

<span data-ttu-id="d5946-1248">リテラル テキストの代わりにこの関数を使用して、ワークフロー承認名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1248">Use this function instead of literal text to retrieve a string that contains the workflow approval name.</span></span> <span data-ttu-id="d5946-1249">ワークフローの承認が存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1249">If the workflow approval does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="d5946-1250">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1250">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1251">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1251">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1252">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1252">Example</span></span>

<span data-ttu-id="d5946-1253">次のコード例では、変数 *str s* を **MyWorkflowApproval** に設定します。これは、アプリケーション エクスプローラーでのワークフロー承認の名前です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1253">The following code example sets the variable *str s* to **MyWorkflowApproval** which is the name of the workflow approval in the Application Explorer.</span></span>

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

## <a name="workflowcategorystr"></a><span data-ttu-id="d5946-1254">workflowCategoryStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1254">workflowCategoryStr</span></span>
<span data-ttu-id="d5946-1255">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー カテゴリの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1255">Retrieves the name of a workflow category in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1256">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1256">Syntax</span></span>

```xpp
str workflowcategorystr(category category)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1257">Parameters</span></span>

| <span data-ttu-id="d5946-1258">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1258">Parameter</span></span> | <span data-ttu-id="d5946-1259">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1259">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="d5946-1260">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="d5946-1260">category</span></span>  | <span data-ttu-id="d5946-1261">ワークフロー カテゴリーのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1261">The Application Explorer name of the workflow category.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1262">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1262">Return Value</span></span>

<span data-ttu-id="d5946-1263">ワークフロー カテゴリのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-1263">A string that represents the Application Explorer name of the workflow category.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1264">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1264">Remarks</span></span>

<span data-ttu-id="d5946-1265">リテラル テキストの代わりにこの関数を使用して、ワークフロー カテゴリ名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1265">Use this function instead of literal text to retrieve a string that contains the workflow category name.</span></span> <span data-ttu-id="d5946-1266">ワークフローのカテゴリーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1266">If the workflow category does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="d5946-1267">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1267">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1268">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1268">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1269">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1269">Example</span></span>

<span data-ttu-id="d5946-1270">次のコード例では、変数 *str s* を **MyWorkflowCategory** に設定します。これは、アプリケーション エクスプローラーでのワークフロー カテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1270">The following code example sets the variable *str s* to **MyWorkflowCategory** which is the name of the workflow category in the Application Explorer.</span></span>

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

## <a name="workflowtaskstr"></a><span data-ttu-id="d5946-1271">workflowTaskStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1271">workflowTaskStr</span></span>
<span data-ttu-id="d5946-1272">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー タスクの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1272">Retrieves the name of a workflow task in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1273">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1273">Syntax</span></span>

```xpp
str workflowtaskstr(task task)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1274">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1274">Parameters</span></span>

| <span data-ttu-id="d5946-1275">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1275">Parameter</span></span> | <span data-ttu-id="d5946-1276">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1276">Description</span></span>                                         |
|-----------|-----------------------------------------------------|
| <span data-ttu-id="d5946-1277">タスク</span><span class="sxs-lookup"><span data-stu-id="d5946-1277">task</span></span>      | <span data-ttu-id="d5946-1278">ワークフロー タスクのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1278">The Application Explorer name of the workflow task.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1279">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1279">Return Value</span></span>

<span data-ttu-id="d5946-1280">ワークフロー タスクのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5946-1280">A string that represents the Application Explorer name of the workflow task.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1281">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1281">Remarks</span></span>

<span data-ttu-id="d5946-1282">リテラル テキストの代わりにこの関数を使用して、ワークフロー タスク名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1282">Use this function instead of literal text to retrieve a string that contains the workflow task name.</span></span> <span data-ttu-id="d5946-1283">ワークフローのタスクーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1283">If the workflow task does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="d5946-1284">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1284">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1285">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1285">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1286">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1286">Example</span></span>

<span data-ttu-id="d5946-1287">次のコード例では、変数 *str s* を **MyWorkflowTask** に設定します。これは、アプリケーション エクスプローラーでのワークフロー タスクの名前です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1287">The following code example sets the variable *str s* to **MyWorkflowTask** which is the name of the workflow task in the Application Explorer.</span></span>

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

## <a name="workflowtypestr"></a><span data-ttu-id="d5946-1288">workflowTypeStr</span><span class="sxs-lookup"><span data-stu-id="d5946-1288">workflowTypeStr</span></span>
<span data-ttu-id="d5946-1289">指定したワークフロー タイプがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d5946-1289">Validates that the specified workflow type exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="d5946-1290">構文</span><span class="sxs-lookup"><span data-stu-id="d5946-1290">Syntax</span></span>

```xpp
str workflowTypeStr(str workflow)
```

### <a name="parameters"></a><span data-ttu-id="d5946-1291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1291">Parameters</span></span>

| <span data-ttu-id="d5946-1292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5946-1292">Parameter</span></span> | <span data-ttu-id="d5946-1293">説明</span><span class="sxs-lookup"><span data-stu-id="d5946-1293">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="d5946-1294">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="d5946-1294">workflow</span></span>  | <span data-ttu-id="d5946-1295">検証するワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1295">The name of the workflow type to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="d5946-1296">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5946-1296">Return Value</span></span>

<span data-ttu-id="d5946-1297">ワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="d5946-1297">The name of the workflow type.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5946-1298">備考</span><span class="sxs-lookup"><span data-stu-id="d5946-1298">Remarks</span></span>

<span data-ttu-id="d5946-1299">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="d5946-1299">This is a compile-time function.</span></span> <span data-ttu-id="d5946-1300">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5946-1300">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="d5946-1301">例</span><span class="sxs-lookup"><span data-stu-id="d5946-1301">Example</span></span>

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


