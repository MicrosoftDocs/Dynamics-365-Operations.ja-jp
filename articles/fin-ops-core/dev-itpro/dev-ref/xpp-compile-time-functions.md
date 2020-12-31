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
ms.custom: 29581
ms.assetid: fa6613a4-7d0b-40d3-be29-9d14c22c7d5b
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d10ee2709f9bb94e63b4b4f3ff95804327d2af60
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408749"
---
# <a name="x-compile-time-functions"></a><span data-ttu-id="f8e95-103">X++ コンパイル時関数</span><span class="sxs-lookup"><span data-stu-id="f8e95-103">X++ compile-time functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8e95-104">このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-104">This topic lists the compile-time functions and describes their syntax, parameters, and return values.</span></span>

## <a name="overview"></a><span data-ttu-id="f8e95-105">概要</span><span class="sxs-lookup"><span data-stu-id="f8e95-105">Overview</span></span>

<span data-ttu-id="f8e95-106">コンパイル時関数は、X++ コードのコンパイル時に早期実行されます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-106">Compile-time functions are executed early during compilation of X++ code.</span></span> <span data-ttu-id="f8e95-107">アプリケーション エクスプローラーに保存されているメタデータの変更に対してコードを復元するためには、可能な限り X++ で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8e95-107">They should be used wherever possible in X++ code to make the code resilient to changes to the metadata stored in the Application Explorer.</span></span> <span data-ttu-id="f8e95-108">コンパイル時関数は、コンパイラによって入力値が検証されます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-108">Compile-time functions have their input value verified by the compiler.</span></span> <span data-ttu-id="f8e95-109">入力された値が見つからず、アプリケーション エクスプローラーの既存のオブジェクトが一致しない場合は、コンパイラーはエラーを発行します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-109">If the input value is not found to match any existing object in the Application Explorer, the compiler issues an error.</span></span> <span data-ttu-id="f8e95-110">コンパイラは実行時に変数に含まれる値を判別できないため、これらの関数への入力はリテラルでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f8e95-110">The inputs to these functions must be literals, because the compiler cannot determine the value that a variable contains at run time.</span></span> <span data-ttu-id="f8e95-111">コンパイル時関数は、メタデータ アサーション関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-111">A compile-time function is a metadata assertion function.</span></span> <span data-ttu-id="f8e95-112">アプリケーション エクスプローラーでエンティティを表す引数を取得し、コンパイル時にその引数を検証します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-112">It takes arguments that represents an entity in the Application Explorer and validates the arguments at compile time.</span></span> <span data-ttu-id="f8e95-113">実行時に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="f8e95-113">It has no effect at run time.</span></span> <span data-ttu-id="f8e95-114">属性は **SysAttribute** クラスから継承するクラスです。</span><span class="sxs-lookup"><span data-stu-id="f8e95-114">Attributes are classes that inherit from the **SysAttribute** class.</span></span> <span data-ttu-id="f8e95-115">フォーム、レポート、クエリ、メニュー のメタデータの検証をサポートするには、コントロールの **AutoDeclaration** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-115">To support the validation of form, report, query, and menu metadata, use the **AutoDeclaration** property on controls.</span></span> <span data-ttu-id="f8e95-116">これらの機能のほとんどは、アプリケーション エクスプローラーにある項目に関するメタデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-116">Most of these functions retrieve metadata about items that are in the Application Explorer.</span></span> <span data-ttu-id="f8e95-117">いくつかの一般的なコンパイル時機能は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f8e95-117">Some common compile time functions are as follows:</span></span>

-   <span data-ttu-id="f8e95-118">`classNum` – クラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-118">`classNum` – Retrieves the ID of a class.</span></span>
-   <span data-ttu-id="f8e95-119">`classStr` – コンパイル時に、その名前のクラスが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-119">`classStr` – During compile time, verifies that a class of that name exists.</span></span> <span data-ttu-id="f8e95-120">この方法は、実行時にエラーを後で発見するよりも優れています。</span><span class="sxs-lookup"><span data-stu-id="f8e95-120">This approach is better than discovering the error later during run time.</span></span>
-   <span data-ttu-id="f8e95-121">`evalBuf`– X++ コードの入力文字列を評価し、結果を文字列として返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-121">`evalBuf`– Evaluates the input string of X++ code, and then returns the results as a string.</span></span>
-   <span data-ttu-id="f8e95-122">`literalStr` – は、文字列 `"@SYS12345"` などのラベルの文字列表示が与えられたときにラベル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-122">`literalStr` – retrieves a label ID when given the string representation of a label, such as the string `"@SYS12345"`.</span></span> <span data-ttu-id="f8e95-123">たとえば、`myLabel.exists(literalStr("@SYS12345"));`。</span><span class="sxs-lookup"><span data-stu-id="f8e95-123">For example, `myLabel.exists(literalStr("@SYS12345"));`.</span></span>

> [!NOTE]
> <span data-ttu-id="f8e95-124">X++ コンパイル時関数は .NET プログラムから呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="f8e95-124">X++ compile time functions cannot be called from a .NET program.</span></span>

### <a name="functions"></a><span data-ttu-id="f8e95-125">関数</span><span class="sxs-lookup"><span data-stu-id="f8e95-125">Functions</span></span>

## <a name="attributestr"></a><span data-ttu-id="f8e95-126">attributeStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-126">attributeStr</span></span>
<span data-ttu-id="f8e95-127">指定した属性クラスがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-127">Validates that the specified attribute class exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-128">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-128">Syntax</span></span>

```xpp
str classStr(class class)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-129">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-129">Parameters</span></span>

| <span data-ttu-id="f8e95-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-130">Parameter</span></span> | <span data-ttu-id="f8e95-131">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-131">Description</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="f8e95-132">クラス</span><span class="sxs-lookup"><span data-stu-id="f8e95-132">class</span></span>     | <span data-ttu-id="f8e95-133">検証する属性の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-133">The name of the attribute to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-134">Return Value</span></span>

<span data-ttu-id="f8e95-135">属性の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-135">The name of the attribute.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-136">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-136">Remarks</span></span>

<span data-ttu-id="f8e95-137">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-137">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-138">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-138">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-139">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-139">Example</span></span>
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

## <a name="classnum"></a><span data-ttu-id="f8e95-140">classNum</span><span class="sxs-lookup"><span data-stu-id="f8e95-140">classNum</span></span>
<span data-ttu-id="f8e95-141">指定されたクラスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-141">Retrieves the ID of the specified class.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-142">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-142">Syntax</span></span>

```xpp
int classNum(class class)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-143">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-143">Parameters</span></span>

| <span data-ttu-id="f8e95-144">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-144">Parameter</span></span> | <span data-ttu-id="f8e95-145">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-145">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="f8e95-146">クラス</span><span class="sxs-lookup"><span data-stu-id="f8e95-146">class</span></span>     | <span data-ttu-id="f8e95-147">ID を取得するクラス。</span><span class="sxs-lookup"><span data-stu-id="f8e95-147">The class for which to retrieve the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-148">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-148">Return Value</span></span>

<span data-ttu-id="f8e95-149">指定されたクラスの ID。</span><span class="sxs-lookup"><span data-stu-id="f8e95-149">The ID of the specified class.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-150">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-150">Remarks</span></span>

<span data-ttu-id="f8e95-151">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-151">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-152">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-152">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-153">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-153">Example</span></span>

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

## <a name="classstr"></a><span data-ttu-id="f8e95-154">classStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-154">classStr</span></span>
<span data-ttu-id="f8e95-155">文字列としてクラスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-155">Retrieves the name of a class as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-156">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-156">Syntax</span></span>

```xpp
str classStr(class class)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-157">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-157">Parameters</span></span>

| <span data-ttu-id="f8e95-158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-158">Parameter</span></span> | <span data-ttu-id="f8e95-159">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-159">Description</span></span>                      |
|-----------|----------------------------------|
| <span data-ttu-id="f8e95-160">クラス</span><span class="sxs-lookup"><span data-stu-id="f8e95-160">class</span></span>     | <span data-ttu-id="f8e95-161">返すクラスの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-161">The name of the class to return.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-162">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-162">Return Value</span></span>

<span data-ttu-id="f8e95-163">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-163">The name of the class.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-164">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-164">Remarks</span></span>

<span data-ttu-id="f8e95-165">リテラル テキストの代わりにこの関数を使用して、クラス名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-165">Use this function instead of literal text to retrieve a string that contains the class name.</span></span> <span data-ttu-id="f8e95-166">クラスが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-166">If the class does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="f8e95-167">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-167">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-168">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-168">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-169">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-169">Example</span></span>

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

## <a name="configurationkeynum"></a><span data-ttu-id="f8e95-170">configurationKeyNum</span><span class="sxs-lookup"><span data-stu-id="f8e95-170">configurationKeyNum</span></span>
<span data-ttu-id="f8e95-171">指定されたコンフィギュレーション キーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-171">Retrieves the ID of the specified configuration key.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-172">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-172">Syntax</span></span>

```xpp
int configurationKeyNum(str keyname)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-173">Parameters</span></span>

| <span data-ttu-id="f8e95-174">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-174">Parameter</span></span> | <span data-ttu-id="f8e95-175">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-175">Description</span></span>                                       |
|-----------|---------------------------------------------------|
| <span data-ttu-id="f8e95-176">keyname</span><span class="sxs-lookup"><span data-stu-id="f8e95-176">keyname</span></span>   | <span data-ttu-id="f8e95-177">ID を返すコンフィギュレーション キー。</span><span class="sxs-lookup"><span data-stu-id="f8e95-177">The configuration key for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-178">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-178">Return Value</span></span>

<span data-ttu-id="f8e95-179">指定されたコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="f8e95-179">The ID of the specified configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-180">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-180">Remarks</span></span>

<span data-ttu-id="f8e95-181">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-181">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-182">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-182">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-183">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-183">Example</span></span>

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

## <a name="configurationkeystr"></a><span data-ttu-id="f8e95-184">configurationKeyStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-184">configurationKeyStr</span></span>
<span data-ttu-id="f8e95-185">文字列としてコンフィギュレーション キーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-185">Retrieves the name of a configuration key as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-186">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-186">Syntax</span></span>

```xpp
str configurationKeyStr(str keyname)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-187">Parameters</span></span>

| <span data-ttu-id="f8e95-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-188">Parameter</span></span> | <span data-ttu-id="f8e95-189">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-189">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="f8e95-190">keyname</span><span class="sxs-lookup"><span data-stu-id="f8e95-190">keyname</span></span>   | <span data-ttu-id="f8e95-191">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-191">The name of the configuration key.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-192">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-192">Return Value</span></span>

<span data-ttu-id="f8e95-193">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-193">The name of the configuration key.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-194">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-194">Remarks</span></span>

<span data-ttu-id="f8e95-195">リテラル テキストの代わりにこの関数を使用して、構成キー名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-195">Use this function instead of literal text to retrieve a string that contains the configuration key name.</span></span> <span data-ttu-id="f8e95-196">キーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-196">If the key does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="f8e95-197">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-197">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-198">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-198">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-199">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-199">Example</span></span>

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

## <a name="dataentitydatasourcestr"></a><span data-ttu-id="f8e95-200">dataEntityDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-200">dataEntityDataSourceStr</span></span>
<span data-ttu-id="f8e95-201">データ エンティティのデータ ソースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-201">Retrieves the name of a data source of a data entity.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-202">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-202">Syntax</span></span>

```xpp
str dataEntityDataSourceStr(str dataEntity, str dataSource)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-203">Parameters</span></span>

| <span data-ttu-id="f8e95-204">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-204">Parameter</span></span>  | <span data-ttu-id="f8e95-205">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-205">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="f8e95-206">dataEntity</span><span class="sxs-lookup"><span data-stu-id="f8e95-206">dataEntity</span></span> | <span data-ttu-id="f8e95-207">データ エンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-207">The name of the data entity.</span></span> |
| <span data-ttu-id="f8e95-208">dataSource</span><span class="sxs-lookup"><span data-stu-id="f8e95-208">dataSource</span></span> | <span data-ttu-id="f8e95-209">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-209">The name of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-210">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-210">Return Value</span></span>

<span data-ttu-id="f8e95-211">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-211">The name of the data source.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-212">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-212">Remarks</span></span>

<span data-ttu-id="f8e95-213">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-213">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-214">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-214">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-215">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-215">Example</span></span>

<span data-ttu-id="f8e95-216">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-216">No example.</span></span>

## <a name="delegatestr"></a><span data-ttu-id="f8e95-217">delegateStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-217">delegateStr</span></span>
<span data-ttu-id="f8e95-218">委任の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-218">Returns the name of the delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-219">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-219">Syntax</span></span>

```xpp
str delegateStr(str class, str instanceDelegate)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-220">Parameters</span></span>

| <span data-ttu-id="f8e95-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-221">Parameter</span></span>        | <span data-ttu-id="f8e95-222">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-222">Description</span></span>                            |
|------------------|----------------------------------------|
| <span data-ttu-id="f8e95-223">クラス</span><span class="sxs-lookup"><span data-stu-id="f8e95-223">class</span></span>            | <span data-ttu-id="f8e95-224">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-224">The name of the class, table, or form.</span></span> |
| <span data-ttu-id="f8e95-225">instanceDelegate</span><span class="sxs-lookup"><span data-stu-id="f8e95-225">instanceDelegate</span></span> | <span data-ttu-id="f8e95-226">インスタンス デリゲートの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-226">The name of the instance delegate.</span></span>     |

### <a name="return-value"></a><span data-ttu-id="f8e95-227">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-227">Return Value</span></span>

<span data-ttu-id="f8e95-228">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-228">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-229">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-229">Remarks</span></span>

<span data-ttu-id="f8e95-230">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-230">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-231">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-231">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-232">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-232">Example</span></span>

<span data-ttu-id="f8e95-233">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-233">No example.</span></span>

## <a name="dimensionhierarchylevelstr"></a><span data-ttu-id="f8e95-234">dimensionHierarchyLevelStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-234">dimensionHierarchyLevelStr</span></span>
<span data-ttu-id="f8e95-235">分析コード階層レベルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-235">Returns the name of the dimension hierarchy level.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-236">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-236">Syntax</span></span>

```xpp
str dimensionHierarchyLevelStr(str dimensionHierarchyLevel)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-237">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-237">Parameters</span></span>

| <span data-ttu-id="f8e95-238">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-238">Parameter</span></span>               | <span data-ttu-id="f8e95-239">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-239">Description</span></span>                                |
|-------------------------|--------------------------------------------|
| <span data-ttu-id="f8e95-240">dimensionHierarchyLevel</span><span class="sxs-lookup"><span data-stu-id="f8e95-240">dimensionHierarchyLevel</span></span> | <span data-ttu-id="f8e95-241">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-241">The name of the dimension hierarchy level.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-242">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-242">Return Value</span></span>

<span data-ttu-id="f8e95-243">分析コード階層レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-243">The name of the dimension hierarchy level.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-244">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-244">Remarks</span></span>

<span data-ttu-id="f8e95-245">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-245">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-246">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-246">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-247">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-247">Example</span></span>

<span data-ttu-id="f8e95-248">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-248">No example.</span></span>

## <a name="dimensionhierarchystr"></a><span data-ttu-id="f8e95-249">dimensionHierarchyStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-249">dimensionHierarchyStr</span></span>
<span data-ttu-id="f8e95-250">分析コード階層の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-250">Returns the name of the dimension hierarchy.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-251">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-251">Syntax</span></span>

```xpp
str dimensionHierarchyStr(str dimensionHierarchy)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-252">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-252">Parameters</span></span>

| <span data-ttu-id="f8e95-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-253">Parameter</span></span>          | <span data-ttu-id="f8e95-254">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-254">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="f8e95-255">dimensionHierarchy</span><span class="sxs-lookup"><span data-stu-id="f8e95-255">dimensionHierarchy</span></span> | <span data-ttu-id="f8e95-256">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-256">The name of the dimension hierarchy.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-257">Return Value</span></span>

<span data-ttu-id="f8e95-258">分析コード階層の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-258">The name of the dimension hierarchy.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-259">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-259">Remarks</span></span>

<span data-ttu-id="f8e95-260">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-260">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-261">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-261">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-262">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-262">Example</span></span>

<span data-ttu-id="f8e95-263">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-263">No example.</span></span>

## <a name="dimensionreferencestr"></a><span data-ttu-id="f8e95-264">dimensionReferenceStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-264">dimensionReferenceStr</span></span>
<span data-ttu-id="f8e95-265">分析コード参照の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-265">Returns the name of the dimension reference.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-266">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-266">Syntax</span></span>

```xpp
str dimensionReferenceStr(str dimensionReference)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-267">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-267">Parameters</span></span>

| <span data-ttu-id="f8e95-268">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-268">Parameter</span></span>          | <span data-ttu-id="f8e95-269">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-269">Description</span></span>                          |
|--------------------|--------------------------------------|
| <span data-ttu-id="f8e95-270">dimensionReference</span><span class="sxs-lookup"><span data-stu-id="f8e95-270">dimensionReference</span></span> | <span data-ttu-id="f8e95-271">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-271">The name of the dimension reference.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-272">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-272">Return Value</span></span>

<span data-ttu-id="f8e95-273">分析コード参照の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-273">The name of the dimension reference.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-274">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-274">Remarks</span></span>

<span data-ttu-id="f8e95-275">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-275">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-276">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-276">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-277">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-277">Example</span></span>

<span data-ttu-id="f8e95-278">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-278">No example.</span></span>

## <a name="dutystr"></a><span data-ttu-id="f8e95-279">dutyStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-279">dutyStr</span></span>
<span data-ttu-id="f8e95-280">指定したセキュリティ職務権限の名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-280">Retrieves a string that represents the name of the specified security duty.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-281">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-281">Syntax</span></span>

```xpp
str dutyStr(str securityDuty)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-282">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-282">Parameters</span></span>

| <span data-ttu-id="f8e95-283">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-283">Parameter</span></span>    | <span data-ttu-id="f8e95-284">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-284">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="f8e95-285">securityDuty</span><span class="sxs-lookup"><span data-stu-id="f8e95-285">securityDuty</span></span> | <span data-ttu-id="f8e95-286">セキュリティ職務権限の名前です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-286">The name of the security duty.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-287">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-287">Return Value</span></span>

<span data-ttu-id="f8e95-288">文字列のセキュリティ職務の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-288">The name of the security duty in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-289">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-289">Remarks</span></span>

<span data-ttu-id="f8e95-290">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-290">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-291">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-291">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-292">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-292">Example</span></span>

<span data-ttu-id="f8e95-293">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-293">No example.</span></span>

## <a name="enumcnt"></a><span data-ttu-id="f8e95-294">enumCnt</span><span class="sxs-lookup"><span data-stu-id="f8e95-294">enumCnt</span></span>
<span data-ttu-id="f8e95-295">指定された列挙型の要素数を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-295">Retrieves the number of elements in the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-296">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-296">Syntax</span></span>

```xpp
int enumCnt(enum enumtype)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-297">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-297">Parameters</span></span>

| <span data-ttu-id="f8e95-298">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-298">Parameter</span></span> | <span data-ttu-id="f8e95-299">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-299">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="f8e95-300">enumtype</span><span class="sxs-lookup"><span data-stu-id="f8e95-300">enumtype</span></span>  | <span data-ttu-id="f8e95-301">列挙型タイプ。</span><span class="sxs-lookup"><span data-stu-id="f8e95-301">The enumeration type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-302">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-302">Return Value</span></span>

<span data-ttu-id="f8e95-303">指定された列挙型の要素数。</span><span class="sxs-lookup"><span data-stu-id="f8e95-303">The number of elements in the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-304">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-304">Remarks</span></span>

<span data-ttu-id="f8e95-305">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-305">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-306">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-306">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-307">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-307">Example</span></span>

```xpp
enumCnt(NoYes); //Returns 2, as the two elements are Yes and No.
```

## <a name="enumliteralstr"></a><span data-ttu-id="f8e95-308">enumLiteralStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-308">enumLiteralStr</span></span>
<span data-ttu-id="f8e95-309">指定した文字列が指定した列挙型の要素であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-309">Indicates whether the specified string is an element of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-310">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-310">Syntax</span></span>

```xpp
\enumLiteralStr(enum enum, string str)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-311">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-311">Parameters</span></span>

| <span data-ttu-id="f8e95-312">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-312">Parameter</span></span> | <span data-ttu-id="f8e95-313">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-313">Description</span></span>                                                      |
|-----------|------------------------------------------------------------------|
| <span data-ttu-id="f8e95-314">列挙型</span><span class="sxs-lookup"><span data-stu-id="f8e95-314">enum</span></span>      | <span data-ttu-id="f8e95-315">指定された値を取得する列挙型。</span><span class="sxs-lookup"><span data-stu-id="f8e95-315">The enumeration type from which to retrieve the specified value.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-316">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-316">Return Value</span></span>

<span data-ttu-id="f8e95-317">指定された文字列が見つかった場合の *str* パラメーターの値。それ以外の場合は、コンパイル エラーです。</span><span class="sxs-lookup"><span data-stu-id="f8e95-317">The value of the *str* parameter if the specified string was found; otherwise, a compilation error.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-318">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-318">Remarks</span></span>

<span data-ttu-id="f8e95-319">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-319">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-320">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-320">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-321">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-321">Example</span></span>

```xpp
static void getEnumValueAsString()
{
    str i;
    i = enumLiteralStr(ABCEnum, "valueInABCEnum");
    print i;
    pause;
}
```

## <a name="enumnum"></a><span data-ttu-id="f8e95-322">enumNum</span><span class="sxs-lookup"><span data-stu-id="f8e95-322">enumNum</span></span>
<span data-ttu-id="f8e95-323">指定された列挙型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-323">Retrieves the ID of the specified enumeration type.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-324">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-324">Syntax</span></span>
```xpp
int enumNum(enum enum)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-325">Parameters</span></span>

| <span data-ttu-id="f8e95-326">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-326">Parameter</span></span> | <span data-ttu-id="f8e95-327">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-327">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="f8e95-328">列挙型</span><span class="sxs-lookup"><span data-stu-id="f8e95-328">enum</span></span>      | <span data-ttu-id="f8e95-329">ID を返す列挙。</span><span class="sxs-lookup"><span data-stu-id="f8e95-329">The enumeration for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-330">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-330">Return Value</span></span>

<span data-ttu-id="f8e95-331">指定された列挙型の ID。</span><span class="sxs-lookup"><span data-stu-id="f8e95-331">The ID of the specified enumeration type.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-332">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-332">Remarks</span></span>

<span data-ttu-id="f8e95-333">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-333">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-334">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-334">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-335">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-335">Example</span></span>

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

## <a name="enumstr"></a><span data-ttu-id="f8e95-336">enumStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-336">enumStr</span></span>
<span data-ttu-id="f8e95-337">文字列として列挙型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-337">Retrieves the name of an enumeration as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-338">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-338">Syntax</span></span>

```xpp
str enumStr(enum enum)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-339">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-339">Parameters</span></span>

| <span data-ttu-id="f8e95-340">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-340">Parameter</span></span> | <span data-ttu-id="f8e95-341">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-341">Description</span></span>                  |
|-----------|------------------------------|
| <span data-ttu-id="f8e95-342">列挙型</span><span class="sxs-lookup"><span data-stu-id="f8e95-342">enum</span></span>      | <span data-ttu-id="f8e95-343">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-343">The name of the enumeration.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-344">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-344">Return Value</span></span>

<span data-ttu-id="f8e95-345">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-345">The name of the enumeration.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-346">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-346">Remarks</span></span>

<span data-ttu-id="f8e95-347">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-347">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-348">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-348">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-349">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-349">Example</span></span>

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

## <a name="extendedtypenum"></a><span data-ttu-id="f8e95-350">extendedTypeNum</span><span class="sxs-lookup"><span data-stu-id="f8e95-350">extendedTypeNum</span></span>
<span data-ttu-id="f8e95-351">指定された拡張データ型の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-351">Retrieves the ID of the specified extended data type.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-352">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-352">Syntax</span></span>

```xpp
int extendedTypeNum(int str)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-353">Parameters</span></span>

| <span data-ttu-id="f8e95-354">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-354">Parameter</span></span> | <span data-ttu-id="f8e95-355">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-355">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="f8e95-356">str</span><span class="sxs-lookup"><span data-stu-id="f8e95-356">str</span></span>       | <span data-ttu-id="f8e95-357">ID を返す拡張データ型。</span><span class="sxs-lookup"><span data-stu-id="f8e95-357">The extended data type for which to return the ID.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-358">Return Value</span></span>

<span data-ttu-id="f8e95-359">指定された拡張データ型の ID。</span><span class="sxs-lookup"><span data-stu-id="f8e95-359">The ID of the specified extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-360">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-360">Remarks</span></span>

<span data-ttu-id="f8e95-361">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-361">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-362">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-362">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-363">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-363">Example</span></span>

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

## <a name="extendedtypestr"></a><span data-ttu-id="f8e95-364">extendedTypeStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-364">extendedTypeStr</span></span>
<span data-ttu-id="f8e95-365">文字列として拡張データ型の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-365">Retrieves the name of an extended data type as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-366">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-366">Syntax</span></span>

```xpp
str extendedTypeStr(int str)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-367">Parameters</span></span>

| <span data-ttu-id="f8e95-368">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-368">Parameter</span></span> | <span data-ttu-id="f8e95-369">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-369">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="f8e95-370">str</span><span class="sxs-lookup"><span data-stu-id="f8e95-370">str</span></span>       | <span data-ttu-id="f8e95-371">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-371">The name of the extended data type.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-372">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-372">Return Value</span></span>

<span data-ttu-id="f8e95-373">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-373">The name of the extended data type.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-374">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-374">Remarks</span></span>

<span data-ttu-id="f8e95-375">リテラル テキストの代わりにこの関数を使用すると、拡張データ型名を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-375">Use this function instead of literal text to return a string that contains the extended data type name.</span></span> <span data-ttu-id="f8e95-376">データ タイプが存在しない場合、**extendedTypeStr** 関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-376">If the data type does not exist, the **extendedTypeStr** function generates a syntax error at compile time.</span></span> <span data-ttu-id="f8e95-377">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-377">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-378">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-378">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-379">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-379">Example</span></span>

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

## <a name="fieldnum"></a><span data-ttu-id="f8e95-380">fieldNum</span><span class="sxs-lookup"><span data-stu-id="f8e95-380">fieldNum</span></span>
<span data-ttu-id="f8e95-381">指定したフィールドの ID 番号を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-381">Returns the ID number of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-382">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-382">Syntax</span></span>

```xpp
int fieldNum(str tableName, str fieldName)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-383">Parameters</span></span>

| <span data-ttu-id="f8e95-384">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-384">Parameter</span></span> | <span data-ttu-id="f8e95-385">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-385">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="f8e95-386">tableName</span><span class="sxs-lookup"><span data-stu-id="f8e95-386">tableName</span></span> | <span data-ttu-id="f8e95-387">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-387">The name of the table.</span></span> |
| <span data-ttu-id="f8e95-388">fieldName</span><span class="sxs-lookup"><span data-stu-id="f8e95-388">fieldName</span></span> | <span data-ttu-id="f8e95-389">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-389">The name of the field.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-390">Return Value</span></span>

<span data-ttu-id="f8e95-391">指定されたフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="f8e95-391">The ID of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-392">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-392">Remarks</span></span>

<span data-ttu-id="f8e95-393">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-393">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-394">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-394">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-395">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-395">Example</span></span>

<span data-ttu-id="f8e95-396">次の例では、**CashDisc** フィールドの番号を **CustTable** テーブルに出力します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-396">The following example prints the number of the **CashDisc** field in the **CustTable** table.</span></span>

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

## <a name="fieldpname"></a><span data-ttu-id="f8e95-397">fieldPName</span><span class="sxs-lookup"><span data-stu-id="f8e95-397">fieldPName</span></span>
<span data-ttu-id="f8e95-398">指定されたフィールドのラベルを取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-398">Retrieves the label of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-399">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-399">Syntax</span></span>

```xpp
str fieldPName(str tableid, str fieldid)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-400">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-400">Parameters</span></span>

| <span data-ttu-id="f8e95-401">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-401">Parameter</span></span> | <span data-ttu-id="f8e95-402">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-402">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="f8e95-403">tableid</span><span class="sxs-lookup"><span data-stu-id="f8e95-403">tableid</span></span>   | <span data-ttu-id="f8e95-404">指定されたフィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="f8e95-404">The table that contains the specified field.</span></span> |
| <span data-ttu-id="f8e95-405">fieldid</span><span class="sxs-lookup"><span data-stu-id="f8e95-405">fieldid</span></span>   | <span data-ttu-id="f8e95-406">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="f8e95-406">The field to convert.</span></span>                        |

### <a name="return-value"></a><span data-ttu-id="f8e95-407">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-407">Return Value</span></span>

<span data-ttu-id="f8e95-408">フィールドのラベル。</span><span class="sxs-lookup"><span data-stu-id="f8e95-408">The label of the field.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-409">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-409">Remarks</span></span>

<span data-ttu-id="f8e95-410">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-410">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-411">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-411">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-412">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-412">Example</span></span>

<span data-ttu-id="f8e95-413">次の例では、**CashDisc** フィールドのラベルを出力します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-413">The following example prints the label of the **CashDisc** field.</span></span>

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

## <a name="fieldstr"></a><span data-ttu-id="f8e95-414">fieldStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-414">fieldStr</span></span>
<span data-ttu-id="f8e95-415">指定したフィールドのフィールド名を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-415">Retrieves the field name of the specified field.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-416">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-416">Syntax</span></span>

```xpp
str fieldStr(str tableid, str fieldid)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-417">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-417">Parameters</span></span>

| <span data-ttu-id="f8e95-418">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-418">Parameter</span></span> | <span data-ttu-id="f8e95-419">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-419">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="f8e95-420">tableid</span><span class="sxs-lookup"><span data-stu-id="f8e95-420">tableid</span></span>   | <span data-ttu-id="f8e95-421">フィールドを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="f8e95-421">The table that contains the field.</span></span> |
| <span data-ttu-id="f8e95-422">fieldid</span><span class="sxs-lookup"><span data-stu-id="f8e95-422">fieldid</span></span>   | <span data-ttu-id="f8e95-423">変換するフィールド。</span><span class="sxs-lookup"><span data-stu-id="f8e95-423">The field to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="f8e95-424">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-424">Return Value</span></span>

<span data-ttu-id="f8e95-425">指定したフィールドのフィールド名。</span><span class="sxs-lookup"><span data-stu-id="f8e95-425">The field name of the specified field.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-426">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-426">Remarks</span></span>

<span data-ttu-id="f8e95-427">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-427">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-428">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-428">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-429">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-429">Example</span></span>

<span data-ttu-id="f8e95-430">次の例では、**CashDisc** フィールドの名前を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-430">The following example assigns the name of the **CashDisc** field to the *myText* variable.</span></span>

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

## <a name="formcontrolstr"></a><span data-ttu-id="f8e95-431">formControlStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-431">formControlStr</span></span>
<span data-ttu-id="f8e95-432">X++ コンパイラは、コントロールがフォームに存在するかどうかをチェックし、関数呼び出しを有効なコントロール名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-432">Causes the X++ compiler to check whether the control exists on the form, and to replace the function call with a string of the valid control name.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-433">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-433">Syntax</span></span>

```xpp
str formControlStr(formName, controlName)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-434">Parameters</span></span>

| <span data-ttu-id="f8e95-435">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-435">Parameter</span></span>   | <span data-ttu-id="f8e95-436">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-436">Description</span></span>                                                          |
|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="f8e95-437">formName</span><span class="sxs-lookup"><span data-stu-id="f8e95-437">formName</span></span>    | <span data-ttu-id="f8e95-438">引用符ではなく、フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-438">The name of the form, not in quotation marks.</span></span>                        |
| <span data-ttu-id="f8e95-439">controlName</span><span class="sxs-lookup"><span data-stu-id="f8e95-439">controlName</span></span> | <span data-ttu-id="f8e95-440">フォーム上のコントロールの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="f8e95-440">The name of the control that is on the form, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-441">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-441">Return Value</span></span>

<span data-ttu-id="f8e95-442">アプリケーション エクスプローラーで表示されるコントロールの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-442">A string that contains the name of the control as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-443">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-443">Remarks</span></span>

<span data-ttu-id="f8e95-444">コントロールがフォームに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-444">A compile error is issued if the compiler determines that the control does not exist on the form.</span></span> <span data-ttu-id="f8e95-445">X++ コードが引用符が含まれる文字列を使用してコントロールの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="f8e95-445">If your X++ code uses a string that contains quotation marks to supply the control name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="f8e95-446">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-446">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="f8e95-447">コンパイラにより実行される **formControlStr** などの X++ 関数は、コンパイル時関数と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-447">X++ functions such as **formControlStr** that are executed by the compiler are called compile-time functions or compile-time functions.</span></span> <span data-ttu-id="f8e95-448">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="f8e95-448">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="f8e95-449">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="f8e95-449">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="f8e95-450">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-450">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-451">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-451">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-452">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-452">Example</span></span>

<span data-ttu-id="f8e95-453">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-453">No example.</span></span>

## <a name="formdatafieldstr"></a><span data-ttu-id="f8e95-454">formDataFieldStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-454">formDataFieldStr</span></span>
<span data-ttu-id="f8e95-455">フォームのデータ フィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-455">Returns the name of a data field in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-456">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-456">Syntax</span></span>

```xpp
str formDataFieldStr(str formName, str dataSource, str dataField)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-457">Parameters</span></span>

| <span data-ttu-id="f8e95-458">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-458">Parameter</span></span>  | <span data-ttu-id="f8e95-459">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-459">Description</span></span>                        |
|------------|------------------------------------|
| <span data-ttu-id="f8e95-460">formName</span><span class="sxs-lookup"><span data-stu-id="f8e95-460">formName</span></span>   | <span data-ttu-id="f8e95-461">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-461">The name of the form.</span></span>              |
| <span data-ttu-id="f8e95-462">dataSource</span><span class="sxs-lookup"><span data-stu-id="f8e95-462">dataSource</span></span> | <span data-ttu-id="f8e95-463">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="f8e95-463">The data source of the form.</span></span>       |
| <span data-ttu-id="f8e95-464">dataField</span><span class="sxs-lookup"><span data-stu-id="f8e95-464">dataField</span></span>  | <span data-ttu-id="f8e95-465">データ ソースのデータ フィールド。</span><span class="sxs-lookup"><span data-stu-id="f8e95-465">The data field of the data source.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-466">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-466">Return Value</span></span>

<span data-ttu-id="f8e95-467">フォームのデータ フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-467">The name of a data field in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-468">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-468">Remarks</span></span>

<span data-ttu-id="f8e95-469">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-469">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-470">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-470">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-471">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-471">Example</span></span>

```xpp
str a = formDataFieldStr(FMVehicle, FMModelRate, RatePerDay);
```

## <a name="formdatasourcestr"></a><span data-ttu-id="f8e95-472">formDataSourceStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-472">formDataSourceStr</span></span>
<span data-ttu-id="f8e95-473">フォームのデータ ソースの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-473">Returns the name of a data source in a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-474">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-474">Syntax</span></span>

```xpp
str formDataSourceStr(str formName, str dataSource)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-475">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-475">Parameters</span></span>

| <span data-ttu-id="f8e95-476">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-476">Parameter</span></span>  | <span data-ttu-id="f8e95-477">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-477">Description</span></span>                  |
|------------|------------------------------|
| <span data-ttu-id="f8e95-478">formName</span><span class="sxs-lookup"><span data-stu-id="f8e95-478">formName</span></span>   | <span data-ttu-id="f8e95-479">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-479">The name of the form.</span></span>        |
| <span data-ttu-id="f8e95-480">dataSource</span><span class="sxs-lookup"><span data-stu-id="f8e95-480">dataSource</span></span> | <span data-ttu-id="f8e95-481">フォームのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="f8e95-481">The data source of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-482">Return Value</span></span>

<span data-ttu-id="f8e95-483">フォームのデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-483">The name of a data source in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-484">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-484">Remarks</span></span>

<span data-ttu-id="f8e95-485">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-485">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-486">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-486">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-487">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-487">Example</span></span>

```xpp
str b = formDataSourceStr(FMVehicle, FMModelRate);
```

## <a name="formmethodstr"></a><span data-ttu-id="f8e95-488">formMethodStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-488">formMethodStr</span></span>
<span data-ttu-id="f8e95-489">フォームのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-489">Returns the name of a method of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-490">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-490">Syntax</span></span>

```xpp
str formMethodStr(str formName, str methodName)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-491">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-491">Parameters</span></span>

| <span data-ttu-id="f8e95-492">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-492">Parameter</span></span>  | <span data-ttu-id="f8e95-493">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-493">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="f8e95-494">formName</span><span class="sxs-lookup"><span data-stu-id="f8e95-494">formName</span></span>   | <span data-ttu-id="f8e95-495">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-495">The name of the form.</span></span>   |
| <span data-ttu-id="f8e95-496">methodName</span><span class="sxs-lookup"><span data-stu-id="f8e95-496">methodName</span></span> | <span data-ttu-id="f8e95-497">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="f8e95-497">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-498">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-498">Return Value</span></span>

<span data-ttu-id="f8e95-499">フォームのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-499">The name of a method in a form.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-500">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-500">Remarks</span></span>

<span data-ttu-id="f8e95-501">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-501">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-502">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-502">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-503">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-503">Example</span></span>

<span data-ttu-id="f8e95-504">次の例では、**showDialog** メソッドの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-504">The following example prints the name of the **showDialog** method.</span></span>

```xpp
str c = formMethodStr(Batch,showDialog);
```

## <a name="formstr"></a><span data-ttu-id="f8e95-505">formStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-505">formStr</span></span>
<span data-ttu-id="f8e95-506">フォームの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-506">Retrieves the name of a form.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-507">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-507">Syntax</span></span>

```xpp
str formStr(str form)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-508">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-508">Parameters</span></span>

| <span data-ttu-id="f8e95-509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-509">Parameter</span></span> | <span data-ttu-id="f8e95-510">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-510">Description</span></span>         |
|-----------|---------------------|
| <span data-ttu-id="f8e95-511">フォーム</span><span class="sxs-lookup"><span data-stu-id="f8e95-511">form</span></span>      | <span data-ttu-id="f8e95-512">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-512">The name of a form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-513">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-513">Return Value</span></span>

<span data-ttu-id="f8e95-514">フォームの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-514">A string that represents the name of the form.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-515">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-515">Remarks</span></span>

<span data-ttu-id="f8e95-516">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-516">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-517">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-517">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-518">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-518">Example</span></span>

<span data-ttu-id="f8e95-519">次の例では、InventDim フォームの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-519">The following example prints the name of the InventDim form.</span></span>

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

## <a name="identifierstr"></a><span data-ttu-id="f8e95-520">identifierStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-520">identifierStr</span></span>
<span data-ttu-id="f8e95-521">指定された識別子を文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-521">Converts the specified identifier to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-522">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-522">Syntax</span></span>

```xpp
str identifierStr(str ident)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-523">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-523">Parameters</span></span>

| <span data-ttu-id="f8e95-524">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-524">Parameter</span></span> | <span data-ttu-id="f8e95-525">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-525">Description</span></span>                |
|-----------|----------------------------|
| <span data-ttu-id="f8e95-526">ident</span><span class="sxs-lookup"><span data-stu-id="f8e95-526">ident</span></span>     | <span data-ttu-id="f8e95-527">変換する ID。</span><span class="sxs-lookup"><span data-stu-id="f8e95-527">The identifier to convert.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-528">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-528">Return Value</span></span>

<span data-ttu-id="f8e95-529">指定した ID を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-529">A string that represents the specified identifier.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-530">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-530">Remarks</span></span>

<span data-ttu-id="f8e95-531">**identifierStr** 関数使用する場合、ベスト プラクティス警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-531">You will receive a best practice warning if you use the **identifierStr** function.</span></span> <span data-ttu-id="f8e95-532">これは、**identifierStr** に対して存在チェックが実行されたために発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-532">This occurs because existence checking is performed for **identifierStr**.</span></span> <span data-ttu-id="f8e95-533">使用可能な場合は、より具体的なコンパイル時の関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-533">Try to use a more specific compile-time function if one is available.</span></span> <span data-ttu-id="f8e95-534">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-534">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-535">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-535">For more information, [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-536">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-536">Example</span></span>

<span data-ttu-id="f8e95-537">次のコード例では、*myvar* 変数名を *thevar* 変数に割り当てています。</span><span class="sxs-lookup"><span data-stu-id="f8e95-537">The following code example assigns the *myvar* variable name to the *thevar* variable.</span></span>

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

## <a name="indexnum"></a><span data-ttu-id="f8e95-538">indexNum</span><span class="sxs-lookup"><span data-stu-id="f8e95-538">indexNum</span></span>
<span data-ttu-id="f8e95-539">指定されたインデックスを数字に変換します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-539">Converts the specified index to a number.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-540">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-540">Syntax</span></span>

```xpp
int indexNum(str tableid, str indexid)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-541">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-541">Parameters</span></span>

| <span data-ttu-id="f8e95-542">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-542">Parameter</span></span> | <span data-ttu-id="f8e95-543">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-543">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="f8e95-544">tableid</span><span class="sxs-lookup"><span data-stu-id="f8e95-544">tableid</span></span>   | <span data-ttu-id="f8e95-545">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="f8e95-545">The table that contains the index.</span></span> |
| <span data-ttu-id="f8e95-546">indexid</span><span class="sxs-lookup"><span data-stu-id="f8e95-546">indexid</span></span>   | <span data-ttu-id="f8e95-547">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="f8e95-547">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="f8e95-548">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-548">Return Value</span></span>

<span data-ttu-id="f8e95-549">指定されたインデックスを表すインデックス番号。</span><span class="sxs-lookup"><span data-stu-id="f8e95-549">The index number that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-550">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-550">Remarks</span></span>

<span data-ttu-id="f8e95-551">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-551">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-552">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-552">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-553">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-553">Example</span></span>

<span data-ttu-id="f8e95-554">次の例では、当事者インデックスのインデックス値を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-554">The following example returns the index value of the Party index.</span></span>

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

## <a name="indexstr"></a><span data-ttu-id="f8e95-555">indexStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-555">indexStr</span></span>
<span data-ttu-id="f8e95-556">指定されたインデックスを文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-556">Converts the specified index to a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-557">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-557">Syntax</span></span>

```xpp
str indexStr(str tableid, str indexid)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-558">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-558">Parameters</span></span>

| <span data-ttu-id="f8e95-559">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-559">Parameter</span></span> | <span data-ttu-id="f8e95-560">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-560">Description</span></span>                        |
|-----------|------------------------------------|
| <span data-ttu-id="f8e95-561">tableid</span><span class="sxs-lookup"><span data-stu-id="f8e95-561">tableid</span></span>   | <span data-ttu-id="f8e95-562">フィールド インデックスを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="f8e95-562">The table that contains the index.</span></span> |
| <span data-ttu-id="f8e95-563">indexid</span><span class="sxs-lookup"><span data-stu-id="f8e95-563">indexid</span></span>   | <span data-ttu-id="f8e95-564">変換するインデックス。</span><span class="sxs-lookup"><span data-stu-id="f8e95-564">The index to convert.</span></span>              |

### <a name="return-value"></a><span data-ttu-id="f8e95-565">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-565">Return Value</span></span>

<span data-ttu-id="f8e95-566">指定インデックスを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-566">A string that represents the specified index.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-567">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-567">Remarks</span></span>

<span data-ttu-id="f8e95-568">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-568">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-569">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-569">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-570">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-570">Example</span></span>

<span data-ttu-id="f8e95-571">次の例では、**CashDisc** インデックス値を *myText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-571">The following example assigns the **CashDisc** index value to the *myText* variable.</span></span>

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

## <a name="licensecodenum"></a><span data-ttu-id="f8e95-572">licenseCodeNum</span><span class="sxs-lookup"><span data-stu-id="f8e95-572">licenseCodeNum</span></span>
<span data-ttu-id="f8e95-573">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-573">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-574">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-574">Syntax</span></span>

```xpp
int licenseCodeNum(str codename)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-575">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-575">Parameters</span></span>

| <span data-ttu-id="f8e95-576">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-576">Parameter</span></span> | <span data-ttu-id="f8e95-577">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-577">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="f8e95-578">codename</span><span class="sxs-lookup"><span data-stu-id="f8e95-578">codename</span></span>  | <span data-ttu-id="f8e95-579">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-579">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-580">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-580">Return Value</span></span>

<span data-ttu-id="f8e95-581">指定されたライセンス コードの数。</span><span class="sxs-lookup"><span data-stu-id="f8e95-581">The number of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-582">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-582">Remarks</span></span>

<span data-ttu-id="f8e95-583">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-583">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-584">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-584">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-585">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-585">Example</span></span>

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

## <a name="licensecodestr"></a><span data-ttu-id="f8e95-586">licenseCodeStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-586">licenseCodeStr</span></span>
<span data-ttu-id="f8e95-587">指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-587">Validates that the specified license code exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-588">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-588">Syntax</span></span>

```xpp
str licenseCodeStr(str codename)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-589">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-589">Parameters</span></span>

| <span data-ttu-id="f8e95-590">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-590">Parameter</span></span> | <span data-ttu-id="f8e95-591">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-591">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="f8e95-592">codename</span><span class="sxs-lookup"><span data-stu-id="f8e95-592">codename</span></span>  | <span data-ttu-id="f8e95-593">検証するライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-593">The name of the license code to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-594">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-594">Return Value</span></span>

<span data-ttu-id="f8e95-595">指定されたライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-595">The name of the specified license code.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-596">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-596">Remarks</span></span>

<span data-ttu-id="f8e95-597">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-597">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-598">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-598">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-599">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-599">Example</span></span>

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

## <a name="literalstr"></a><span data-ttu-id="f8e95-600">literalStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-600">literalStr</span></span>
<span data-ttu-id="f8e95-601">指定した文字列がリテラル文字列であることを検証します。そうでない場合は、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-601">Validates that the specified string can be a literal string; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-602">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-602">Syntax</span></span>

```xpp
str literalStr(int str)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-603">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-603">Parameters</span></span>

| <span data-ttu-id="f8e95-604">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-604">Parameter</span></span> | <span data-ttu-id="f8e95-605">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-605">Description</span></span>             |
|-----------|-------------------------|
| <span data-ttu-id="f8e95-606">codename</span><span class="sxs-lookup"><span data-stu-id="f8e95-606">codename</span></span>  | <span data-ttu-id="f8e95-607">検証する文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-607">The string to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-608">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-608">Return Value</span></span>

<span data-ttu-id="f8e95-609">有効な場合は、リテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-609">The literal string if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-610">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-610">Remarks</span></span>

<span data-ttu-id="f8e95-611">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-611">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-612">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-612">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-613">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-613">Example</span></span>

```xpp
{
    str s;
    ;

    s = literalStr("This is a literal str");
    print s;
    pause;
}
```

## <a name="maxdate"></a><span data-ttu-id="f8e95-614">maxDate</span><span class="sxs-lookup"><span data-stu-id="f8e95-614">maxDate</span></span>
<span data-ttu-id="f8e95-615">日付型の変数に使用できる最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-615">Retrieves the maximum value allowed for a variable of type date.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-616">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-616">Syntax</span></span>

```xpp
date maxDate()
```

### <a name="return-value"></a><span data-ttu-id="f8e95-617">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-617">Return Value</span></span>

<span data-ttu-id="f8e95-618">**日付** の変数に使用できる最大値は、**2154-12-31** です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-618">The maximum value allowed for a variable of type **date**, which is **2154-12-31**.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-619">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-619">Remarks</span></span>

<span data-ttu-id="f8e95-620">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-620">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-621">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-621">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-622">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-622">Example</span></span>

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

## <a name="maxint"></a><span data-ttu-id="f8e95-623">maxInt</span><span class="sxs-lookup"><span data-stu-id="f8e95-623">maxInt</span></span>
<span data-ttu-id="f8e95-624">**int** 型に格納可能な最大符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-624">Retrieves the maximum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-625">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-625">Syntax</span></span>

```xpp
int maxInt()
```

### <a name="return-value"></a><span data-ttu-id="f8e95-626">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-626">Return Value</span></span>

<span data-ttu-id="f8e95-627">整数の許容値の最大値。</span><span class="sxs-lookup"><span data-stu-id="f8e95-627">The maximum value allowed value of an integer.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-628">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-628">Remarks</span></span>

<span data-ttu-id="f8e95-629">その他の整数値は、戻り値以下になります。</span><span class="sxs-lookup"><span data-stu-id="f8e95-629">Any other integer will be less than or equal to the returned value.</span></span> <span data-ttu-id="f8e95-630">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-630">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-631">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-631">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-632">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-632">Example</span></span>

```xpp
static void maxIntExample(Args _arg)
{
    int i;
    ;
    print "The maximum value for type int is " + int2Str(maxInt());
    pause;
}
```

## <a name="measurementstr"></a><span data-ttu-id="f8e95-633">measurementStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-633">measurementStr</span></span>
<span data-ttu-id="f8e95-634">測定の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-634">Returns the name of a measurement.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-635">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-635">Syntax</span></span>

```xpp
str measurementStr(str measurement)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-636">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-636">Parameters</span></span>

| <span data-ttu-id="f8e95-637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-637">Parameter</span></span>   | <span data-ttu-id="f8e95-638">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-638">Description</span></span>                  |
|-------------|------------------------------|
| <span data-ttu-id="f8e95-639">測定値</span><span class="sxs-lookup"><span data-stu-id="f8e95-639">measurement</span></span> | <span data-ttu-id="f8e95-640">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-640">The name of the measurement.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-641">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-641">Return Value</span></span>

<span data-ttu-id="f8e95-642">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-642">The name of the measurement.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-643">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-643">Remarks</span></span>

<span data-ttu-id="f8e95-644">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-644">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-645">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-645">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-646">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-646">Example</span></span>

<span data-ttu-id="f8e95-647">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-647">No example.</span></span>

## <a name="measurestr"></a><span data-ttu-id="f8e95-648">measureStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-648">measureStr</span></span>
<span data-ttu-id="f8e95-649">メジャーの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-649">Returns the name of a measure.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-650">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-650">Syntax</span></span>

```xpp
str measureStr(str measure)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-651">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-651">Parameters</span></span>

| <span data-ttu-id="f8e95-652">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-652">Parameter</span></span> | <span data-ttu-id="f8e95-653">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-653">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="f8e95-654">測定</span><span class="sxs-lookup"><span data-stu-id="f8e95-654">measure</span></span>   | <span data-ttu-id="f8e95-655">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-655">The name of the measure.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-656">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-656">Return Value</span></span>

<span data-ttu-id="f8e95-657">測定の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-657">The name of the measure.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-658">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-658">Remarks</span></span>

<span data-ttu-id="f8e95-659">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-659">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-660">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-660">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-661">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-661">Example</span></span>

<span data-ttu-id="f8e95-662">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-662">No example.</span></span>

## <a name="menuitemactionstr"></a><span data-ttu-id="f8e95-663">menuItemActionStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-663">menuItemActionStr</span></span>
<span data-ttu-id="f8e95-664">指定したメニュー項目のアクションがアプリケーション オブジェクト ツリー (Application Explorer) に存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-664">Validates that the specified menu item action exists in the Application Object Tree (Application Explorer); if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-665">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-665">Syntax</span></span>

```xpp
str menuItemActionStr(class menuitem)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-666">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-666">Parameters</span></span>

| <span data-ttu-id="f8e95-667">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-667">Parameter</span></span> | <span data-ttu-id="f8e95-668">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-668">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="f8e95-669">codename</span><span class="sxs-lookup"><span data-stu-id="f8e95-669">codename</span></span>  | <span data-ttu-id="f8e95-670">検証するメニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-670">The name of the menu item action to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-671">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-671">Return Value</span></span>

<span data-ttu-id="f8e95-672">有効な場合の、メニュー項目アクションの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-672">The name of the menu item action, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-673">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-673">Remarks</span></span>

<span data-ttu-id="f8e95-674">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-674">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-675">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-675">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-676">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-676">Example</span></span>

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

## <a name="menuitemdisplaystr"></a><span data-ttu-id="f8e95-677">menuItemDisplayStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-677">menuItemDisplayStr</span></span>
<span data-ttu-id="f8e95-678">指定したメニュー項目の表示がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-678">Validates that the specified menu item display exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-679">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-679">Syntax</span></span>

```xpp
str menuitemdisplaystr(class menuItem)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-680">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-680">Parameters</span></span>

| <span data-ttu-id="f8e95-681">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-681">Parameter</span></span> | <span data-ttu-id="f8e95-682">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-682">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="f8e95-683">codename</span><span class="sxs-lookup"><span data-stu-id="f8e95-683">codename</span></span>  | <span data-ttu-id="f8e95-684">検証するメニュー項目nの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-684">The name of the menu item display to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-685">Return Value</span></span>

<span data-ttu-id="f8e95-686">有効な場合の、指定されたメニューの表示の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-686">The name of the specified menu item display, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-687">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-687">Remarks</span></span>

<span data-ttu-id="f8e95-688">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-688">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-689">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-689">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-690">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-690">Example</span></span>

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

## <a name="menuitemoutputstr"></a><span data-ttu-id="f8e95-691">menuItemOutputStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-691">menuItemOutputStr</span></span>
<span data-ttu-id="f8e95-692">指定したメニュー項目の出力がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-692">Validates that the specified menu item output exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-693">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-693">Syntax</span></span>

```xpp
str menuItemOutputStr(class menuitem)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-694">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-694">Parameters</span></span>

| <span data-ttu-id="f8e95-695">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-695">Parameter</span></span> | <span data-ttu-id="f8e95-696">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-696">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="f8e95-697">codename</span><span class="sxs-lookup"><span data-stu-id="f8e95-697">codename</span></span>  | <span data-ttu-id="f8e95-698">検証するメニュー項目出力の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-698">The name of the menu item output to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-699">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-699">Return Value</span></span>

<span data-ttu-id="f8e95-700">有効な場合、指定されたメニュー項目が出力されます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-700">The specified menu item output if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-701">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-701">Remarks</span></span>

<span data-ttu-id="f8e95-702">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-702">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-703">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-703">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-704">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-704">Example</span></span>

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

## <a name="menustr"></a><span data-ttu-id="f8e95-705">menuStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-705">menuStr</span></span>
<span data-ttu-id="f8e95-706">指定したメニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-706">Validates that the specified menu exists in the Application Explorer; if not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-707">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-707">Syntax</span></span>

```xpp
str menuStr(class menu)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-708">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-708">Parameters</span></span>

| <span data-ttu-id="f8e95-709">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-709">Parameter</span></span> | <span data-ttu-id="f8e95-710">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-710">Description</span></span>                       |
|-----------|-----------------------------------|
| <span data-ttu-id="f8e95-711">メニュー</span><span class="sxs-lookup"><span data-stu-id="f8e95-711">menu</span></span>      | <span data-ttu-id="f8e95-712">検証するメニューの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-712">The name of the menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-713">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-713">Return Value</span></span>

<span data-ttu-id="f8e95-714">有効な場合の指定されたメニュー項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-714">The name of the specified menu item if valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-715">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-715">Remarks</span></span>

<span data-ttu-id="f8e95-716">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-716">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-717">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-717">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-718">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-718">Example</span></span>

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

## <a name="methodstr"></a><span data-ttu-id="f8e95-719">methodStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-719">methodStr</span></span>
<span data-ttu-id="f8e95-720">指定したメソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-720">Validates that the specified method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-721">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-721">Syntax</span></span>

```xpp
str methodStr(class class, int method)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-722">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-722">Parameters</span></span>

| <span data-ttu-id="f8e95-723">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-723">Parameter</span></span> | <span data-ttu-id="f8e95-724">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-724">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="f8e95-725">クラス</span><span class="sxs-lookup"><span data-stu-id="f8e95-725">class</span></span>     | <span data-ttu-id="f8e95-726">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-726">The name of the class.</span></span>              |
| <span data-ttu-id="f8e95-727">メソッド</span><span class="sxs-lookup"><span data-stu-id="f8e95-727">method</span></span>    | <span data-ttu-id="f8e95-728">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-728">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-729">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-729">Return Value</span></span>

<span data-ttu-id="f8e95-730">有効な場合の、指定されたメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-730">The name of the specified method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-731">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-731">Remarks</span></span>

<span data-ttu-id="f8e95-732">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-732">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-733">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-733">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-734">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-734">Example</span></span>

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

## <a name="minint"></a><span data-ttu-id="f8e95-735">minInt</span><span class="sxs-lookup"><span data-stu-id="f8e95-735">minInt</span></span>
<span data-ttu-id="f8e95-736">**int** 型に格納可能な最小符号付き値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-736">Retrieves the minimum signed value that can be stored in an **int** type.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-737">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-737">Syntax</span></span>

```xpp
int minInt()
```

### <a name="return-value"></a><span data-ttu-id="f8e95-738">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-738">Return Value</span></span>

<span data-ttu-id="f8e95-739">**int** 型の最小値です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-739">The minimum value of an **int** type.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-740">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-740">Remarks</span></span>

<span data-ttu-id="f8e95-741">その他の整数値は、戻り値以上になります。</span><span class="sxs-lookup"><span data-stu-id="f8e95-741">Any other integer value will be greater than or equal to the returned value.</span></span> <span data-ttu-id="f8e95-742">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-742">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-743">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-743">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-744">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-744">Example</span></span>

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

## <a name="privilegestr"></a><span data-ttu-id="f8e95-745">privilegeStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-745">privilegeStr</span></span>
<span data-ttu-id="f8e95-746">権限の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-746">Returns the name of the privilege.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-747">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-747">Syntax</span></span>

```xpp
str privilegeStr(str privilege)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-748">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-748">Parameters</span></span>

| <span data-ttu-id="f8e95-749">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-749">Parameter</span></span> | <span data-ttu-id="f8e95-750">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-750">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="f8e95-751">権限</span><span class="sxs-lookup"><span data-stu-id="f8e95-751">privilege</span></span> | <span data-ttu-id="f8e95-752">名前を返す対象の特権。</span><span class="sxs-lookup"><span data-stu-id="f8e95-752">The privilege for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-753">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-753">Return Value</span></span>

<span data-ttu-id="f8e95-754">権限の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-754">The name of the privilege.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-755">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-755">Remarks</span></span>

<span data-ttu-id="f8e95-756">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-756">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-757">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-757">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-758">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-758">Example</span></span>

<span data-ttu-id="f8e95-759">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-759">No example.</span></span>

## <a name="querydatasourcestr"></a><span data-ttu-id="f8e95-760">queryDatasourceStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-760">queryDatasourceStr</span></span>
<span data-ttu-id="f8e95-761">X++ コンパイラは、データ ソースがクエリに存在するかどうかをチェックし、関数呼び出しを有効なデータ ソース名の文字列で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-761">Causes the X++ compiler to check whether the data source exists on the query, and to replace the function call with a string of the valid data source name.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-762">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-762">Syntax</span></span>

```xpp
str queryDataSourceStr(queryName, dataSourceName)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-763">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-763">Parameters</span></span>

| <span data-ttu-id="f8e95-764">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-764">Parameter</span></span>      | <span data-ttu-id="f8e95-765">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-765">Description</span></span>                                                               |
|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="f8e95-766">queryName</span><span class="sxs-lookup"><span data-stu-id="f8e95-766">queryName</span></span>      | <span data-ttu-id="f8e95-767">引用符ではなく、クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-767">The name of the query, not in quotation marks.</span></span>                            |
| <span data-ttu-id="f8e95-768">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="f8e95-768">dataSourceName</span></span> | <span data-ttu-id="f8e95-769">クエリ上のデータ ソースの名前で、引用符ではありません。</span><span class="sxs-lookup"><span data-stu-id="f8e95-769">The name of the data source that is on the query, not in quotation marks.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-770">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-770">Return Value</span></span>

<span data-ttu-id="f8e95-771">アプリケーション エクスプローラーで表示されるデータ ソースの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-771">A string that contains the name of the data source as it appears in the Application Explorer.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-772">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-772">Remarks</span></span>

<span data-ttu-id="f8e95-773">データ ソースがクエリに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-773">A compile error is issued if the compiler determines that the data source does not exist on the query.</span></span> <span data-ttu-id="f8e95-774">X++ コードが引用符が含まれる文字列を使用してデータ ソースの名前を入力する場合、実行時までエラーを検出できません。</span><span class="sxs-lookup"><span data-stu-id="f8e95-774">If your X++ code uses a string that contains quotation marks to supply the data source name, the error cannot be discovered until run time.</span></span> <span data-ttu-id="f8e95-775">この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-775">Use of this function enables the compiler to discover the error earlier at compile time.</span></span> <span data-ttu-id="f8e95-776">コンパイラにより実行される **queryDataSourceStr** などの X++ 関数は、コンパイル時関数とみなされます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-776">X++ functions such as **queryDataSourceStr** that are executed by the compiler are referred to as compile-time functions or compile-time functions.</span></span> <span data-ttu-id="f8e95-777">入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。</span><span class="sxs-lookup"><span data-stu-id="f8e95-777">That is why the input parameters are not standard strings in quotation marks.</span></span> <span data-ttu-id="f8e95-778">コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。</span><span class="sxs-lookup"><span data-stu-id="f8e95-778">Compile-time functions are not represented in the p-code or other executable that is output by the compiler.</span></span> <span data-ttu-id="f8e95-779">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-779">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-780">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-780">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-781">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-781">Example</span></span>

<span data-ttu-id="f8e95-782">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-782">No example.</span></span>

## <a name="querymethodstr"></a><span data-ttu-id="f8e95-783">queryMethodStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-783">queryMethodStr</span></span>
<span data-ttu-id="f8e95-784">クエリのメソッドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-784">Returns the name of a method of a query.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-785">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-785">Syntax</span></span>

```xpp
str queryMethodStr(str queryName, str methodName)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-786">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-786">Parameters</span></span>

| <span data-ttu-id="f8e95-787">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-787">Parameter</span></span>  | <span data-ttu-id="f8e95-788">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-788">Description</span></span>             |
|------------|-------------------------|
| <span data-ttu-id="f8e95-789">queryName</span><span class="sxs-lookup"><span data-stu-id="f8e95-789">queryName</span></span>  | <span data-ttu-id="f8e95-790">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-790">The name of the query.</span></span>  |
| <span data-ttu-id="f8e95-791">methodName</span><span class="sxs-lookup"><span data-stu-id="f8e95-791">methodName</span></span> | <span data-ttu-id="f8e95-792">フォームのメソッド。</span><span class="sxs-lookup"><span data-stu-id="f8e95-792">The method of the form.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-793">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-793">Return Value</span></span>

<span data-ttu-id="f8e95-794">クエリのメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-794">The name of a method in a query.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-795">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-795">Remarks</span></span>

<span data-ttu-id="f8e95-796">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-796">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-797">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-797">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-798">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-798">Example</span></span>

<span data-ttu-id="f8e95-799">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-799">No example.</span></span>

## <a name="querystr"></a><span data-ttu-id="f8e95-800">queryStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-800">queryStr</span></span>
<span data-ttu-id="f8e95-801">既存のクエリを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-801">Retrieves a string that represents an existing query.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-802">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-802">Syntax</span></span>

```xpp
str queryStr(str query)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-803">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-803">Parameters</span></span>

| <span data-ttu-id="f8e95-804">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-804">Parameter</span></span> | <span data-ttu-id="f8e95-805">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-805">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="f8e95-806">クエリ</span><span class="sxs-lookup"><span data-stu-id="f8e95-806">query</span></span>     | <span data-ttu-id="f8e95-807">取得するクエリ。</span><span class="sxs-lookup"><span data-stu-id="f8e95-807">The query to retrieve.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-808">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-808">Return Value</span></span>

<span data-ttu-id="f8e95-809">クエリの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-809">The name of the query.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-810">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-810">Remarks</span></span>

<span data-ttu-id="f8e95-811">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-811">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-812">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-812">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-813">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-813">Example</span></span>

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

## <a name="reportstr"></a><span data-ttu-id="f8e95-814">reportStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-814">reportStr</span></span>
<span data-ttu-id="f8e95-815">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-815">Retrieves a string that represents the name of the specified report.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-816">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-816">Syntax</span></span>

```xpp
str reportStr(str report)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-817">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-817">Parameters</span></span>

| <span data-ttu-id="f8e95-818">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-818">Parameter</span></span> | <span data-ttu-id="f8e95-819">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-819">Description</span></span>                              |
|-----------|------------------------------------------|
| <span data-ttu-id="f8e95-820">レポート</span><span class="sxs-lookup"><span data-stu-id="f8e95-820">report</span></span>    | <span data-ttu-id="f8e95-821">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="f8e95-821">The report for which to return the name.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-822">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-822">Return Value</span></span>

<span data-ttu-id="f8e95-823">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-823">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-824">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-824">Remarks</span></span>

<span data-ttu-id="f8e95-825">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-825">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-826">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-826">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-827">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-827">Example</span></span>

<span data-ttu-id="f8e95-828">次の例では、**AssetAddition** レポートの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-828">The following example assigns the name of the **AssetAddition** report to the *MyTxt* variable.</span></span>

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

## <a name="resourcestr"></a><span data-ttu-id="f8e95-829">resourceStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-829">resourceStr</span></span>
<span data-ttu-id="f8e95-830">指定したリソースがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-830">Validates that the specified resource exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-831">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-831">Syntax</span></span>

```xpp
str resourceStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-832">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-832">Parameters</span></span>

| <span data-ttu-id="f8e95-833">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-833">Parameter</span></span>    | <span data-ttu-id="f8e95-834">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-834">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="f8e95-835">resourcename</span><span class="sxs-lookup"><span data-stu-id="f8e95-835">resourcename</span></span> | <span data-ttu-id="f8e95-836">検証するリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-836">The name of the resource to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-837">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-837">Return Value</span></span>

<span data-ttu-id="f8e95-838">有効な場合の、指定されたリソースの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-838">The name of the specified resource, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-839">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-839">Remarks</span></span>

<span data-ttu-id="f8e95-840">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-840">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-841">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-841">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-842">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-842">Example</span></span>

```xpp
{
    print "Str for resource StyleSheet_Help_Axapta is " 
        + resourceStr(StyleSheet_Help_Axapta);
    pause;
}
```

## <a name="rolestr"></a><span data-ttu-id="f8e95-843">roleStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-843">roleStr</span></span>
<span data-ttu-id="f8e95-844">指定したセキュリティ ロールの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-844">Retrieves a string that represents the name of the specified security role.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-845">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-845">Syntax</span></span>

```xpp
str roleStr(str securityRole)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-846">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-846">Parameters</span></span>

| <span data-ttu-id="f8e95-847">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-847">Parameter</span></span>    | <span data-ttu-id="f8e95-848">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-848">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="f8e95-849">securityRole</span><span class="sxs-lookup"><span data-stu-id="f8e95-849">securityRole</span></span> | <span data-ttu-id="f8e95-850">セキュリティ ロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-850">The name of the security role.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-851">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-851">Return Value</span></span>

<span data-ttu-id="f8e95-852">文字列のセキュリティ ロールの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-852">The name of the security role in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-853">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-853">Remarks</span></span>

<span data-ttu-id="f8e95-854">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-854">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-855">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-855">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-856">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-856">Example</span></span>

<span data-ttu-id="f8e95-857">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-857">No example.</span></span>

## <a name="ssrsreportstr"></a><span data-ttu-id="f8e95-858">ssrsReportStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-858">ssrsReportStr</span></span>
<span data-ttu-id="f8e95-859">指定したレポートの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-859">Retrieves a string that represents the name of the specified report.</span></span> <span data-ttu-id="f8e95-860">レポート コントローラー クラスで実行されるレポートを指定する場合は、この関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-860">Use this function when you want to specify the report that should be run by a report controller class.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-861">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-861">Syntax</span></span>

```xpp
str ssrsReportStr(str report, str design)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-862">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-862">Parameters</span></span>

| <span data-ttu-id="f8e95-863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-863">Parameter</span></span> | <span data-ttu-id="f8e95-864">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-864">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| <span data-ttu-id="f8e95-865">レポート</span><span class="sxs-lookup"><span data-stu-id="f8e95-865">report</span></span>    | <span data-ttu-id="f8e95-866">名前を返す対象のレポート。</span><span class="sxs-lookup"><span data-stu-id="f8e95-866">The report to return the name for.</span></span>                         |
| <span data-ttu-id="f8e95-867">design</span><span class="sxs-lookup"><span data-stu-id="f8e95-867">design</span></span>    | <span data-ttu-id="f8e95-868">レポートに関連付けられているデザインの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-868">The name of the design that is associated with the report.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-869">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-869">Return Value</span></span>

<span data-ttu-id="f8e95-870">レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-870">The name of the report.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-871">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-871">Remarks</span></span>

<span data-ttu-id="f8e95-872">**ssrsReportStr** 関数は、有効なレポートに属しているかどうかを検証するために、渡された 2 つの値を解析します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-872">The **ssrsReportStr** function parses the two values that are passed to it, to validate whether they belong to a valid report.</span></span> <span data-ttu-id="f8e95-873">コントローラーが、どのレポート デザインの組み合わせを呼び出す必要があるかを判断できるように、メニュー項目が controller() を指しているときは、レポート名を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8e95-873">The report name must be set when a menu item points to a controller(), so that the controller can determine which report-design combination must be invoked.</span></span> <span data-ttu-id="f8e95-874">**ssrsReportStr** 関数を使用すると、レポートおよびデザイン名のコンパイル時の検証で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-874">Use of the **ssrsReportStr** function provides the benefit of compile-time validation for the report and design name.</span></span> <span data-ttu-id="f8e95-875">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-875">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-876">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-876">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-877">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-877">Example</span></span>

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

## <a name="staticdelegatestr"></a><span data-ttu-id="f8e95-878">staticDelegateStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-878">staticDelegateStr</span></span>
<span data-ttu-id="f8e95-879">静的デリゲートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-879">Returns the name of a static delegate.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-880">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-880">Syntax</span></span>

```xpp
str staticDelegateStr(str class, str delegate)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-881">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-881">Parameters</span></span>

| <span data-ttu-id="f8e95-882">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-882">Parameter</span></span> | <span data-ttu-id="f8e95-883">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-883">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="f8e95-884">クラス</span><span class="sxs-lookup"><span data-stu-id="f8e95-884">class</span></span>     | <span data-ttu-id="f8e95-885">クラス、テーブル、またはフォームの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-885">The name of a class, table, or form.</span></span> |
| <span data-ttu-id="f8e95-886">デリゲート</span><span class="sxs-lookup"><span data-stu-id="f8e95-886">delegate</span></span>  | <span data-ttu-id="f8e95-887">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-887">The name of the delegate.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="f8e95-888">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-888">Return Value</span></span>

<span data-ttu-id="f8e95-889">委任の名前です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-889">The name of the delegate.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-890">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-890">Remarks</span></span>

<span data-ttu-id="f8e95-891">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-891">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-892">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-892">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-893">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-893">Example</span></span>

<span data-ttu-id="f8e95-894">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-894">No example.</span></span>

## <a name="staticmethodstr"></a><span data-ttu-id="f8e95-895">staticMethodStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-895">staticMethodStr</span></span>
<span data-ttu-id="f8e95-896">指定した静的メソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-896">Validates that the specified static method exists in the specified class; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-897">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-897">Syntax</span></span>

```xpp
str staticMethodStr(class class, int method)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-898">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-898">Parameters</span></span>

| <span data-ttu-id="f8e95-899">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-899">Parameter</span></span> | <span data-ttu-id="f8e95-900">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-900">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="f8e95-901">クラス</span><span class="sxs-lookup"><span data-stu-id="f8e95-901">class</span></span>     | <span data-ttu-id="f8e95-902">クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-902">The name of the class.</span></span>                     |
| <span data-ttu-id="f8e95-903">メソッド</span><span class="sxs-lookup"><span data-stu-id="f8e95-903">method</span></span>    | <span data-ttu-id="f8e95-904">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-904">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-905">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-905">Return Value</span></span>

<span data-ttu-id="f8e95-906">有効な場合の、指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-906">The name of the static method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-907">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-907">Remarks</span></span>

<span data-ttu-id="f8e95-908">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-908">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-909">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-909">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-910">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-910">Example</span></span>

<span data-ttu-id="f8e95-911">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-911">No example.</span></span>

## <a name="tablecollectionstr"></a><span data-ttu-id="f8e95-912">tableCollectionStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-912">tableCollectionStr</span></span>
<span data-ttu-id="f8e95-913">指定したテーブル コレクションがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-913">Validates that the specified table collection exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-914">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-914">Syntax</span></span>

```xpp
str tableCollectionStr(class tablecollection)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-915">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-915">Parameters</span></span>

| <span data-ttu-id="f8e95-916">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-916">Parameter</span></span>       | <span data-ttu-id="f8e95-917">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-917">Description</span></span>                                   |
|-----------------|-----------------------------------------------|
| <span data-ttu-id="f8e95-918">tablecollection</span><span class="sxs-lookup"><span data-stu-id="f8e95-918">tablecollection</span></span> | <span data-ttu-id="f8e95-919">検証するテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-919">The name of the table collection to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-920">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-920">Return Value</span></span>

<span data-ttu-id="f8e95-921">有効な場合の、指定されたテーブル コレクションの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-921">The name of the specified table collection, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-922">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-922">Remarks</span></span>

<span data-ttu-id="f8e95-923">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-923">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-924">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-924">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-925">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-925">Example</span></span>

<span data-ttu-id="f8e95-926">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-926">No example.</span></span>

## <a name="tablefieldgroupstr"></a><span data-ttu-id="f8e95-927">tableFieldGroupStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-927">tableFieldGroupStr</span></span>
<span data-ttu-id="f8e95-928">文字列としてフィールド グループの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-928">Retrieves the name of a field group as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-929">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-929">Syntax</span></span>

```xpp
str tableFieldGroupStr(str tableName, str fieldGroupName)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-930">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-930">Parameters</span></span>

| <span data-ttu-id="f8e95-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-931">Parameter</span></span>      | <span data-ttu-id="f8e95-932">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-932">Description</span></span>                              |
|----------------|------------------------------------------|
| <span data-ttu-id="f8e95-933">tableName</span><span class="sxs-lookup"><span data-stu-id="f8e95-933">tableName</span></span>      | <span data-ttu-id="f8e95-934">フィールド グループを含むテーブル。</span><span class="sxs-lookup"><span data-stu-id="f8e95-934">The table that contains the field group.</span></span> |
| <span data-ttu-id="f8e95-935">fieldGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e95-935">fieldGroupName</span></span> | <span data-ttu-id="f8e95-936">テーブル内のフィールド グループ。</span><span class="sxs-lookup"><span data-stu-id="f8e95-936">The field group in the table.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="f8e95-937">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-937">Return Value</span></span>

<span data-ttu-id="f8e95-938">文字列としてのフィールド グループの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-938">The name of the field group as a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-939">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-939">Remarks</span></span>

<span data-ttu-id="f8e95-940">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-940">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-941">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-941">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-942">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-942">Example</span></span>

<span data-ttu-id="f8e95-943">次の例では、**編集** フィールド グループの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-943">The following example retrieves the name of the **Editing** field group as a string.</span></span>

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

## <a name="tablemethodstr"></a><span data-ttu-id="f8e95-944">tableMethodStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-944">tableMethodStr</span></span>
<span data-ttu-id="f8e95-945">指定したメソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-945">Validates that the specified method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-946">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-946">Syntax</span></span>

```xpp
str tableMethodStr(int table, int method)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-947">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-947">Parameters</span></span>

| <span data-ttu-id="f8e95-948">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-948">Parameter</span></span> | <span data-ttu-id="f8e95-949">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-949">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="f8e95-950">テーブル</span><span class="sxs-lookup"><span data-stu-id="f8e95-950">table</span></span>     | <span data-ttu-id="f8e95-951">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-951">The name of the table.</span></span>              |
| <span data-ttu-id="f8e95-952">メソッド</span><span class="sxs-lookup"><span data-stu-id="f8e95-952">method</span></span>    | <span data-ttu-id="f8e95-953">検証するメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-953">The name of the method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-954">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-954">Return Value</span></span>

<span data-ttu-id="f8e95-955">有効な場合の、メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-955">The name of the method, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-956">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-956">Remarks</span></span>

<span data-ttu-id="f8e95-957">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-957">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-958">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-958">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-959">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-959">Example</span></span>

<span data-ttu-id="f8e95-960">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-960">No example.</span></span>

## <a name="tablenum"></a><span data-ttu-id="f8e95-961">tableNum</span><span class="sxs-lookup"><span data-stu-id="f8e95-961">tableNum</span></span>
<span data-ttu-id="f8e95-962">特定のテーブルのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-962">Retrieves the table ID of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-963">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-963">Syntax</span></span>

```xpp
int tableNum(str table)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-964">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-964">Parameters</span></span>

| <span data-ttu-id="f8e95-965">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-965">Parameter</span></span> | <span data-ttu-id="f8e95-966">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-966">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="f8e95-967">テーブル</span><span class="sxs-lookup"><span data-stu-id="f8e95-967">table</span></span>     | <span data-ttu-id="f8e95-968">テーブル ID を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="f8e95-968">The table to retrieve the table ID for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-969">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-969">Return Value</span></span>

<span data-ttu-id="f8e95-970">特定のテーブルのテーブル ID</span><span class="sxs-lookup"><span data-stu-id="f8e95-970">The table ID of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-971">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-971">Remarks</span></span>

<span data-ttu-id="f8e95-972">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-972">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-973">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-973">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-974">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-974">Example</span></span>

<span data-ttu-id="f8e95-975">次の例では、**tableID** 変数を 77 に設定します。これは、**CustTable** テーブルの **ID** です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-975">The following example sets the **tableID** variable to 77, which is the **ID** of the **CustTable** table.</span></span>

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

## <a name="tablepname"></a><span data-ttu-id="f8e95-976">tablePName</span><span class="sxs-lookup"><span data-stu-id="f8e95-976">tablePName</span></span>
<span data-ttu-id="f8e95-977">指定されたテーブルの出力可能な名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-977">Retrieves a string that contains the printable name of the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-978">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-978">Syntax</span></span>

```xpp
str tablePName(str table)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-979">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-979">Parameters</span></span>

| <span data-ttu-id="f8e95-980">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-980">Parameter</span></span> | <span data-ttu-id="f8e95-981">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-981">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="f8e95-982">テーブル</span><span class="sxs-lookup"><span data-stu-id="f8e95-982">table</span></span>     | <span data-ttu-id="f8e95-983">印刷可能な名前を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="f8e95-983">The table to retrieve the printable name for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-984">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-984">Return Value</span></span>

<span data-ttu-id="f8e95-985">指定されたテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-985">The name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-986">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-986">Remarks</span></span>

<span data-ttu-id="f8e95-987">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-987">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-988">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-988">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-989">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-989">Example</span></span>

<span data-ttu-id="f8e95-990">次の例では、**CustTable** テーブルのラベルを *MyText* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-990">The following example assigns the label of the **CustTable** table to the *MyText* variable.</span></span>

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

## <a name="tablestaticmethodstr"></a><span data-ttu-id="f8e95-991">tableStaticMethodStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-991">tableStaticMethodStr</span></span>
<span data-ttu-id="f8e95-992">指定した静的メソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-992">Validates that the specified static method exists in the specified table; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-993">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-993">Syntax</span></span>

```xpp
str tableStaticMethodStr(int table, int method)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-994">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-994">Parameters</span></span>

| <span data-ttu-id="f8e95-995">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-995">Parameter</span></span> | <span data-ttu-id="f8e95-996">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-996">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="f8e95-997">テーブル</span><span class="sxs-lookup"><span data-stu-id="f8e95-997">table</span></span>     | <span data-ttu-id="f8e95-998">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-998">The name of the table.</span></span>                     |
| <span data-ttu-id="f8e95-999">メソッド</span><span class="sxs-lookup"><span data-stu-id="f8e95-999">method</span></span>    | <span data-ttu-id="f8e95-1000">検証する静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1000">The name of the static method to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1001">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1001">Return Value</span></span>

<span data-ttu-id="f8e95-1002">指定された静的メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1002">The name of the specified static method.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1003">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1003">Remarks</span></span>

<span data-ttu-id="f8e95-1004">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1004">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1005">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1005">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1006">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1006">Example</span></span>

<span data-ttu-id="f8e95-1007">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1007">No example.</span></span>

## <a name="tablestr"></a><span data-ttu-id="f8e95-1008">tableStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1008">tableStr</span></span>
<span data-ttu-id="f8e95-1009">指定したテーブルの名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1009">Retrieves a string that contains the name the specified table.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1010">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1010">Syntax</span></span>

```xpp
str tableStr(str table)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1011">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1011">Parameters</span></span>

| <span data-ttu-id="f8e95-1012">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1012">Parameter</span></span> | <span data-ttu-id="f8e95-1013">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1013">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="f8e95-1014">テーブル</span><span class="sxs-lookup"><span data-stu-id="f8e95-1014">table</span></span>     | <span data-ttu-id="f8e95-1015">文字列を取得するテーブル。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1015">The table to retrieve a string for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1016">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1016">Return Value</span></span>

<span data-ttu-id="f8e95-1017">指定したテーブルの名前を含む文字列値。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1017">A string value that contains the name of the specified table.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1018">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1018">Remarks</span></span>

<span data-ttu-id="f8e95-1019">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1019">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1020">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1020">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1021">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1021">Example</span></span>

<span data-ttu-id="f8e95-1022">次の例では、**CustTable** テーブルの名前を *MyTxt* 変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1022">The following example assigns the name of the **CustTable** table to the *MyTxt* variable.</span></span>

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

## <a name="tilestr"></a><span data-ttu-id="f8e95-1023">tileStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1023">tileStr</span></span>
<span data-ttu-id="f8e95-1024">指定したタイルの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1024">Retrieves a string that represents the name of the specified tile.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1025">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1025">Syntax</span></span>

```xpp
str tileStr(str tile)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1026">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1026">Parameters</span></span>

| <span data-ttu-id="f8e95-1027">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1027">Parameter</span></span> | <span data-ttu-id="f8e95-1028">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1028">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="f8e95-1029">tile</span><span class="sxs-lookup"><span data-stu-id="f8e95-1029">tile</span></span>      | <span data-ttu-id="f8e95-1030">タイルの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1030">The name of the tile.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1031">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1031">Return Value</span></span>

<span data-ttu-id="f8e95-1032">文字列のタイルの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1032">The name of the tile in a string.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1033">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1033">Remarks</span></span>

<span data-ttu-id="f8e95-1034">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1034">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1035">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1035">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1036">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1036">Example</span></span>

<span data-ttu-id="f8e95-1037">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1037">No example.</span></span>

## <a name="varstr"></a><span data-ttu-id="f8e95-1038">varStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1038">varStr</span></span>
<span data-ttu-id="f8e95-1039">指定した変数の名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1039">Retrieves a string that contains the name of the specified variable.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1040">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1040">Syntax</span></span>

```xpp
str varStr(str var)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1041">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1041">Parameters</span></span>

| <span data-ttu-id="f8e95-1042">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1042">Parameter</span></span> | <span data-ttu-id="f8e95-1043">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1043">Description</span></span>               |
|-----------|---------------------------|
| <span data-ttu-id="f8e95-1044">var</span><span class="sxs-lookup"><span data-stu-id="f8e95-1044">var</span></span>       | <span data-ttu-id="f8e95-1045">変数の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1045">The name of the variable.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1046">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1046">Return Value</span></span>

<span data-ttu-id="f8e95-1047">指定した変数の名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1047">A string that contains the name of the specified variable.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1048">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1048">Remarks</span></span>

<span data-ttu-id="f8e95-1049">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1049">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1050">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1050">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1051">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1051">Example</span></span>

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

## <a name="webactionitemstr"></a><span data-ttu-id="f8e95-1052">webActionItemStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1052">webActionItemStr</span></span>
<span data-ttu-id="f8e95-1053">指定した Web アクション項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1053">Validates that the specified web action item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1054">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1054">Syntax</span></span>

```xpp
str webActionItemStr(class webactionitem)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1055">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1055">Parameters</span></span>

| <span data-ttu-id="f8e95-1056">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1056">Parameter</span></span>     | <span data-ttu-id="f8e95-1057">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1057">Description</span></span>                                  |
|---------------|----------------------------------------------|
| <span data-ttu-id="f8e95-1058">webactionitem</span><span class="sxs-lookup"><span data-stu-id="f8e95-1058">webactionitem</span></span> | <span data-ttu-id="f8e95-1059">検証する Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1059">The name of the web action item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1060">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1060">Return Value</span></span>

<span data-ttu-id="f8e95-1061">有効な場合の、指定された Web アクション項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1061">The name of the specified web action item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1062">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1062">Remarks</span></span>

<span data-ttu-id="f8e95-1063">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1063">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1064">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1064">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1065">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1065">Example</span></span>

```xpp
{
    str s;
    ;
    s = webActionItemStr(EPFlushData);
    print "webactionitem str is " + s;
    pause;
}
```

## <a name="webdisplaycontentitemstr"></a><span data-ttu-id="f8e95-1066">webDisplayContentItemStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1066">webDisplayContentItemStr</span></span>
<span data-ttu-id="f8e95-1067">指定したWeb 表示のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1067">Validates that the specified web display content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1068">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1068">Syntax</span></span>

```xpp
str webDisplayContentItemStr(class webdisplaycontentitem)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1069">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1069">Parameters</span></span>

| <span data-ttu-id="f8e95-1070">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1070">Parameter</span></span>             | <span data-ttu-id="f8e95-1071">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1071">Description</span></span>                                           |
|-----------------------|-------------------------------------------------------|
| <span data-ttu-id="f8e95-1072">webdisplaycontentitem</span><span class="sxs-lookup"><span data-stu-id="f8e95-1072">webdisplaycontentitem</span></span> | <span data-ttu-id="f8e95-1073">検証する Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1073">The name of the web display content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1074">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1074">Return Value</span></span>

<span data-ttu-id="f8e95-1075">有効な場合の、指定された Web 表示コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1075">The name of the specified web display content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1076">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1076">Remarks</span></span>

<span data-ttu-id="f8e95-1077">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1077">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1078">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1078">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1079">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1079">Example</span></span>

```xpp
{
    str s;
    ;

    s = webDisplayContentItemStr(EPAdmin);
    print "string for webcontent display item EPAdmin is " + s;
    pause;
}
```

## <a name="webformstr"></a><span data-ttu-id="f8e95-1080">webFormStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1080">webFormStr</span></span>
<span data-ttu-id="f8e95-1081">指定した Web フォームがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1081">Validates that the specified web form exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1082">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1082">Syntax</span></span>

```xpp
str webFormStr(str name)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1083">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1083">Parameters</span></span>

| <span data-ttu-id="f8e95-1084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1084">Parameter</span></span> | <span data-ttu-id="f8e95-1085">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1085">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="f8e95-1086">名前</span><span class="sxs-lookup"><span data-stu-id="f8e95-1086">name</span></span>      | <span data-ttu-id="f8e95-1087">検証する Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1087">The name of the web form to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1088">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1088">Return Value</span></span>

<span data-ttu-id="f8e95-1089">有効な場合の、指定された Web フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1089">The name of the specified web form, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1090">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1090">Remarks</span></span>

<span data-ttu-id="f8e95-1091">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1091">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1092">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1092">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1093">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1093">Example</span></span>

```xpp
{
    str s;
    ;
    s = webFormStr(EPAdmin);
    print "String for web form EPAdmin is " + s;
    pause;
}
```

## <a name="webletitemstr"></a><span data-ttu-id="f8e95-1094">webletItemStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1094">webletItemStr</span></span>
<span data-ttu-id="f8e95-1095">指定した Weblet 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1095">Validates that the specified weblet item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1096">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1096">Syntax</span></span>

```xpp
str webletItemStr(class webletitem)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1097">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1097">Parameters</span></span>

| <span data-ttu-id="f8e95-1098">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1098">Parameter</span></span>  | <span data-ttu-id="f8e95-1099">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1099">Description</span></span>                              |
|------------|------------------------------------------|
| <span data-ttu-id="f8e95-1100">webletitem</span><span class="sxs-lookup"><span data-stu-id="f8e95-1100">webletitem</span></span> | <span data-ttu-id="f8e95-1101">検証する Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1101">The name of the weblet item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1102">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1102">Return Value</span></span>

<span data-ttu-id="f8e95-1103">有効な場合の、指定された Weblet 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1103">The name of the specified weblet item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1104">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1104">Remarks</span></span>

<span data-ttu-id="f8e95-1105">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1105">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1106">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1106">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1107">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1107">Example</span></span>

```xpp
{
    str s;
    ;
    s = webletItemStr(WebFormWeblet);
    print "String for WebFormWeblet is " + s;
    pause;
}
```

## <a name="webmenustr"></a><span data-ttu-id="f8e95-1108">webMenuStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1108">webMenuStr</span></span>
<span data-ttu-id="f8e95-1109">指定した Web メニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1109">Validates that the specified web menu exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1110">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1110">Syntax</span></span>

```xpp
str webMenuStr(str name)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1111">Parameters</span></span>

| <span data-ttu-id="f8e95-1112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1112">Parameter</span></span> | <span data-ttu-id="f8e95-1113">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1113">Description</span></span>                           |
|-----------|---------------------------------------|
| <span data-ttu-id="f8e95-1114">名前</span><span class="sxs-lookup"><span data-stu-id="f8e95-1114">name</span></span>      | <span data-ttu-id="f8e95-1115">検証する Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1115">The name of the web menu to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1116">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1116">Return Value</span></span>

<span data-ttu-id="f8e95-1117">有効な場合の、指定された Web メニューの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1117">The name of the specified web menu, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1118">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1118">Remarks</span></span>

<span data-ttu-id="f8e95-1119">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1119">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1120">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1120">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1121">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1121">Example</span></span>

```xpp
{
    str s;
    ;
    s = webMenuStr(ECPAdmin);
    print "String for web menu ECPAdmin is " + s;
    pause;
}
```

## <a name="weboutputcontentitemstr"></a><span data-ttu-id="f8e95-1122">webOutputContentItemStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1122">webOutputContentItemStr</span></span>
<span data-ttu-id="f8e95-1123">指定したWeb 出力のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1123">Validates that the specified web output content item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1124">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1124">Syntax</span></span>

```xpp
str webOutputContentItemStr(class weboutputcontentitem)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1125">Parameters</span></span>

| <span data-ttu-id="f8e95-1126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1126">Parameter</span></span>            | <span data-ttu-id="f8e95-1127">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1127">Description</span></span>                                          |
|----------------------|------------------------------------------------------|
| <span data-ttu-id="f8e95-1128">weboutputcontentitem</span><span class="sxs-lookup"><span data-stu-id="f8e95-1128">weboutputcontentitem</span></span> | <span data-ttu-id="f8e95-1129">検証する Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1129">The name of the web output content item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1130">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1130">Return Value</span></span>

<span data-ttu-id="f8e95-1131">有効な場合の、指定された Web 出力コンテンツ項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1131">The name of the specified web output content item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1132">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1132">Remarks</span></span>

<span data-ttu-id="f8e95-1133">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1133">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1134">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1134">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1135">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1135">Example</span></span>

```xpp
{
    str s;
    ;
    s = webOutputContentItemStr(EPPriceList);
    print "string for weboutput content item EPPriceList is " + s;
    pause;
}
```

## <a name="webpagedefstr"></a><span data-ttu-id="f8e95-1136">webpageDefStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1136">webpageDefStr</span></span>
<span data-ttu-id="f8e95-1137">指定した Web ページ定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1137">Validates that the specified Web page definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1138">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1138">Syntax</span></span>

```xpp
str webpageDefStr(str pagename)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1139">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1139">Parameters</span></span>

| <span data-ttu-id="f8e95-1140">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1140">Parameter</span></span> | <span data-ttu-id="f8e95-1141">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1141">Description</span></span>                                      |
|-----------|--------------------------------------------------|
| <span data-ttu-id="f8e95-1142">pagename</span><span class="sxs-lookup"><span data-stu-id="f8e95-1142">pagename</span></span>  | <span data-ttu-id="f8e95-1143">検証する Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1143">The name of the Web page definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1144">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1144">Return Value</span></span>

<span data-ttu-id="f8e95-1145">有効な場合の、指定された Web ページ定義の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1145">The name of the specified web-page definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1146">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1146">Remarks</span></span>

<span data-ttu-id="f8e95-1147">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1147">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1148">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1148">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1149">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1149">Example</span></span>

<span data-ttu-id="f8e95-1150">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1150">No example.</span></span>

## <a name="webreportstr"></a><span data-ttu-id="f8e95-1151">webReportStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1151">webReportStr</span></span>
<span data-ttu-id="f8e95-1152">指定した Web レポートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1152">Validates that the specified web report exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1153">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1153">Syntax</span></span>

```xpp
str webReportStr(str name)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1154">Parameters</span></span>

| <span data-ttu-id="f8e95-1155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1155">Parameter</span></span> | <span data-ttu-id="f8e95-1156">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1156">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="f8e95-1157">名前</span><span class="sxs-lookup"><span data-stu-id="f8e95-1157">name</span></span>      | <span data-ttu-id="f8e95-1158">検証する Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1158">The name of the web report to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1159">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1159">Return Value</span></span>

<span data-ttu-id="f8e95-1160">有効な場合の、指定された Web レポートの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1160">The name of the specified web report, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1161">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1161">Remarks</span></span>

<span data-ttu-id="f8e95-1162">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1162">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1163">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1163">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1164">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1164">Example</span></span>

```xpp
{
    str s;
    ;
    s = webReportStr(EPCSSSalesConfirm);
    print "String for web report EPCSSalesConfirm is " + s;
    pause;
}
```

## <a name="websitedefstr"></a><span data-ttu-id="f8e95-1165">websiteDefStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1165">websiteDefStr</span></span>
<span data-ttu-id="f8e95-1166">指定した Web サイトの定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1166">Validates that the specified web-site definition exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1167">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1167">Syntax</span></span>

```xpp
str websiteDefStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1168">Parameters</span></span>

| <span data-ttu-id="f8e95-1169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1169">Parameter</span></span>    | <span data-ttu-id="f8e95-1170">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1170">Description</span></span>                                      |
|--------------|--------------------------------------------------|
| <span data-ttu-id="f8e95-1171">resourcename</span><span class="sxs-lookup"><span data-stu-id="f8e95-1171">resourcename</span></span> | <span data-ttu-id="f8e95-1172">検証する Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1172">The name of the Web site definition to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1173">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1173">Return Value</span></span>

<span data-ttu-id="f8e95-1174">有効な場合の、指定された Web サイト定義の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1174">The name of the specified web-site definition, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1175">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1175">Remarks</span></span>

<span data-ttu-id="f8e95-1176">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1176">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1177">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1177">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1178">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1178">Example</span></span>

```xpp
{
    str s;
    ;

    s = websiteDefStr(AxSiteDef_1033_xip);
    print "string for web site definition AxSiteDef_1033_xip is " + s;
    pause;
}
```

## <a name="websitetempstr"></a><span data-ttu-id="f8e95-1179">webSiteTempStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1179">webSiteTempStr</span></span>
<span data-ttu-id="f8e95-1180">指定した Web サイトのテンプレートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1180">Validates that the specified web-site template exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1181">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1181">Syntax</span></span>

```xpp
str websiteTempStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1182">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1182">Parameters</span></span>

| <span data-ttu-id="f8e95-1183">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1183">Parameter</span></span>    | <span data-ttu-id="f8e95-1184">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1184">Description</span></span>                                    |
|--------------|------------------------------------------------|
| <span data-ttu-id="f8e95-1185">resourcename</span><span class="sxs-lookup"><span data-stu-id="f8e95-1185">resourcename</span></span> | <span data-ttu-id="f8e95-1186">検証する Web サイト テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1186">The name of the Web site template to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1187">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1187">Return Value</span></span>

<span data-ttu-id="f8e95-1188">有効な場合の、指定された Web テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1188">The name of the specified web-site template, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1189">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1189">Remarks</span></span>

<span data-ttu-id="f8e95-1190">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1190">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1191">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1191">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1192">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1192">Example</span></span>

<span data-ttu-id="f8e95-1193">例なし。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1193">No example.</span></span>

## <a name="webstaticfilestr"></a><span data-ttu-id="f8e95-1194">webStaticFileStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1194">webStaticFileStr</span></span>
<span data-ttu-id="f8e95-1195">指定した Web 静的ファイルがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1195">Validates that the specified web static file exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1196">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1196">Syntax</span></span>

```xpp
str webStaticFileStr(str pagename)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1197">Parameters</span></span>

| <span data-ttu-id="f8e95-1198">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1198">Parameter</span></span> | <span data-ttu-id="f8e95-1199">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1199">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="f8e95-1200">pagename</span><span class="sxs-lookup"><span data-stu-id="f8e95-1200">pagename</span></span>  | <span data-ttu-id="f8e95-1201">検証する Web 静的ファイル テンプレートの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1201">The name of the web static file to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1202">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1202">Return Value</span></span>

<span data-ttu-id="f8e95-1203">有効な場合の、指定された Web 静的ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1203">The name of the specified web static file, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1204">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1204">Remarks</span></span>

<span data-ttu-id="f8e95-1205">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1205">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1206">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1206">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1207">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1207">Example</span></span>

```xpp
{
    str s;
    ;

    s = webStaticFileStr(AXEP);
    print "string for web static file AXEP is " + s;
    pause;
}
```

## <a name="weburlitemstr"></a><span data-ttu-id="f8e95-1208">webUrlItemStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1208">webUrlItemStr</span></span>
<span data-ttu-id="f8e95-1209">指定した Web URL 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1209">Validates that the specified web URL item exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1210">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1210">Syntax</span></span>

```xpp
str webUrlItemStr(class weburlitem)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1211">Parameters</span></span>

| <span data-ttu-id="f8e95-1212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1212">Parameter</span></span>  | <span data-ttu-id="f8e95-1213">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1213">Description</span></span>                               |
|------------|-------------------------------------------|
| <span data-ttu-id="f8e95-1214">weburlitem</span><span class="sxs-lookup"><span data-stu-id="f8e95-1214">weburlitem</span></span> | <span data-ttu-id="f8e95-1215">検証する Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1215">The name of the web URL item to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1216">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1216">Return Value</span></span>

<span data-ttu-id="f8e95-1217">有効な場合の、指定された Web URL 項目の名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1217">The name of the specified web URL item, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1218">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1218">Remarks</span></span>

<span data-ttu-id="f8e95-1219">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1219">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1220">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1220">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1221">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1221">Example</span></span>

```xpp
{
    str s;
    ;

    s = webUrlItemStr(EPAdmin);
    print "string for web url item EPAdmin is " + s;
    pause;
}
```

## <a name="webwebpartstr"></a><span data-ttu-id="f8e95-1222">webWebPartStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1222">webWebPartStr</span></span>
<span data-ttu-id="f8e95-1223">指定した Web パーツがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1223">Validates that the specified web part exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1224">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1224">Syntax</span></span>

```xpp
str webWebpartStr(str resourcename)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1225">Parameters</span></span>

| <span data-ttu-id="f8e95-1226">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1226">Parameter</span></span>    | <span data-ttu-id="f8e95-1227">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1227">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="f8e95-1228">resourcename</span><span class="sxs-lookup"><span data-stu-id="f8e95-1228">resourcename</span></span> | <span data-ttu-id="f8e95-1229">検証する Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1229">The name of the web part to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1230">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1230">Return Value</span></span>

<span data-ttu-id="f8e95-1231">有効な場合の、指定された Web パーツの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1231">The name of the specified web part, if it is valid.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1232">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1232">Remarks</span></span>

<span data-ttu-id="f8e95-1233">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1233">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1234">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1234">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1235">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1235">Example</span></span>

```xpp
{
    str s;
    ;

    s = webWebpartStr(AxWebParts_cab);
    print "string for web part AxWebParts_cab is " + s;
    pause;
}
```

## <a name="workflowapprovalstr"></a><span data-ttu-id="f8e95-1236">workflowApprovalStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1236">workflowApprovalStr</span></span>
<span data-ttu-id="f8e95-1237">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー承認の名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1237">Retrieves the name of a workflow approval in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1238">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1238">Syntax</span></span>

```xpp
str workflowapprovalstr(approval approval)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1239">Parameters</span></span>

| <span data-ttu-id="f8e95-1240">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1240">Parameter</span></span> | <span data-ttu-id="f8e95-1241">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1241">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="f8e95-1242">承認</span><span class="sxs-lookup"><span data-stu-id="f8e95-1242">approval</span></span>  | <span data-ttu-id="f8e95-1243">ワークフローの承認のアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1243">The Application Explorer name of the workflow approval.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1244">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1244">Return Value</span></span>

<span data-ttu-id="f8e95-1245">ワークフローの承認のアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1245">A string that represents the Application Explorer name of the workflow approval.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1246">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1246">Remarks</span></span>

<span data-ttu-id="f8e95-1247">リテラル テキストの代わりにこの関数を使用して、ワークフロー承認名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1247">Use this function instead of literal text to retrieve a string that contains the workflow approval name.</span></span> <span data-ttu-id="f8e95-1248">ワークフローの承認が存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1248">If the workflow approval does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="f8e95-1249">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1249">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1250">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1250">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1251">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1251">Example</span></span>

<span data-ttu-id="f8e95-1252">次のコード例では、変数 *str s* を **MyWorkflowApproval** に設定します。これは、アプリケーション エクスプローラーでのワークフロー承認の名前です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1252">The following code example sets the variable *str s* to **MyWorkflowApproval** which is the name of the workflow approval in the Application Explorer.</span></span>

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

## <a name="workflowcategorystr"></a><span data-ttu-id="f8e95-1253">workflowCategoryStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1253">workflowCategoryStr</span></span>
<span data-ttu-id="f8e95-1254">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー カテゴリの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1254">Retrieves the name of a workflow category in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1255">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1255">Syntax</span></span>

```xpp
str workflowcategorystr(category category)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1256">Parameters</span></span>

| <span data-ttu-id="f8e95-1257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1257">Parameter</span></span> | <span data-ttu-id="f8e95-1258">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1258">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="f8e95-1259">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="f8e95-1259">category</span></span>  | <span data-ttu-id="f8e95-1260">ワークフロー カテゴリーのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1260">The Application Explorer name of the workflow category.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1261">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1261">Return Value</span></span>

<span data-ttu-id="f8e95-1262">ワークフロー カテゴリのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1262">A string that represents the Application Explorer name of the workflow category.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1263">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1263">Remarks</span></span>

<span data-ttu-id="f8e95-1264">リテラル テキストの代わりにこの関数を使用して、ワークフロー カテゴリ名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1264">Use this function instead of literal text to retrieve a string that contains the workflow category name.</span></span> <span data-ttu-id="f8e95-1265">ワークフローのカテゴリーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1265">If the workflow category does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="f8e95-1266">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1266">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1267">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1267">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1268">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1268">Example</span></span>

<span data-ttu-id="f8e95-1269">次のコード例では、変数 *str s* を **MyWorkflowCategory** に設定します。これは、アプリケーション エクスプローラーでのワークフロー カテゴリの名前です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1269">The following code example sets the variable *str s* to **MyWorkflowCategory** which is the name of the workflow category in the Application Explorer.</span></span>

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

## <a name="workflowtaskstr"></a><span data-ttu-id="f8e95-1270">workflowTaskStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1270">workflowTaskStr</span></span>
<span data-ttu-id="f8e95-1271">アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー タスクの名前を文字列として取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1271">Retrieves the name of a workflow task in the Application Object Tree (Application Explorer) as a string.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1272">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1272">Syntax</span></span>

```xpp
str workflowtaskstr(task task)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1273">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1273">Parameters</span></span>

| <span data-ttu-id="f8e95-1274">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1274">Parameter</span></span> | <span data-ttu-id="f8e95-1275">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1275">Description</span></span>                                         |
|-----------|-----------------------------------------------------|
| <span data-ttu-id="f8e95-1276">タスク</span><span class="sxs-lookup"><span data-stu-id="f8e95-1276">task</span></span>      | <span data-ttu-id="f8e95-1277">ワークフロー タスクのアプリケーション エクスプローラーの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1277">The Application Explorer name of the workflow task.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1278">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1278">Return Value</span></span>

<span data-ttu-id="f8e95-1279">ワークフロー タスクのアプリケーション エクスプローラーの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1279">A string that represents the Application Explorer name of the workflow task.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1280">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1280">Remarks</span></span>

<span data-ttu-id="f8e95-1281">リテラル テキストの代わりにこの関数を使用して、ワークフロー タスク名を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1281">Use this function instead of literal text to retrieve a string that contains the workflow task name.</span></span> <span data-ttu-id="f8e95-1282">ワークフローのタスクーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1282">If the workflow task does not exist, the function generates a syntax error at compile time.</span></span> <span data-ttu-id="f8e95-1283">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1283">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1284">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1284">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1285">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1285">Example</span></span>

<span data-ttu-id="f8e95-1286">次のコード例では、変数 *str s* を **MyWorkflowTask** に設定します。これは、アプリケーション エクスプローラーでのワークフロー タスクの名前です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1286">The following code example sets the variable *str s* to **MyWorkflowTask** which is the name of the workflow task in the Application Explorer.</span></span>

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

## <a name="workflowtypestr"></a><span data-ttu-id="f8e95-1287">workflowTypeStr</span><span class="sxs-lookup"><span data-stu-id="f8e95-1287">workflowTypeStr</span></span>
<span data-ttu-id="f8e95-1288">指定したワークフロー タイプがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1288">Validates that the specified workflow type exists in the Application Explorer; if it does not, a compiler error occurs.</span></span>

### <a name="syntax"></a><span data-ttu-id="f8e95-1289">構文</span><span class="sxs-lookup"><span data-stu-id="f8e95-1289">Syntax</span></span>

```xpp
str workflowTypeStr(str workflow)
```

### <a name="parameters"></a><span data-ttu-id="f8e95-1290">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1290">Parameters</span></span>

| <span data-ttu-id="f8e95-1291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f8e95-1291">Parameter</span></span> | <span data-ttu-id="f8e95-1292">説明</span><span class="sxs-lookup"><span data-stu-id="f8e95-1292">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="f8e95-1293">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f8e95-1293">workflow</span></span>  | <span data-ttu-id="f8e95-1294">検証するワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1294">The name of the workflow type to validate.</span></span> |

### <a name="return-value"></a><span data-ttu-id="f8e95-1295">戻り値</span><span class="sxs-lookup"><span data-stu-id="f8e95-1295">Return Value</span></span>

<span data-ttu-id="f8e95-1296">ワークフロー タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1296">The name of the workflow type.</span></span>

### <a name="remarks"></a><span data-ttu-id="f8e95-1297">備考</span><span class="sxs-lookup"><span data-stu-id="f8e95-1297">Remarks</span></span>

<span data-ttu-id="f8e95-1298">これは、コンパイル時関数です。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1298">This is a compile-time function.</span></span> <span data-ttu-id="f8e95-1299">詳細については、「[概要](#overview)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8e95-1299">For more information, see [Overview](#overview).</span></span>

### <a name="example"></a><span data-ttu-id="f8e95-1300">例</span><span class="sxs-lookup"><span data-stu-id="f8e95-1300">Example</span></span>

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


