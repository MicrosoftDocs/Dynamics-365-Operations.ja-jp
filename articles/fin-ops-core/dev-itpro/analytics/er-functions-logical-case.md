---
title: CASE ER 関数
description: このトピックでは、CASE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3bba9cd190db61fda3636cc3c8093030f886b9bd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041771"
---
# <span data-ttu-id="7fc87-103"><a name="CASE">CASE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="7fc87-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fc87-104">`CASE` 関数は、指定された代替オプションに対して指定された式の値を評価し、指定された式の値に等しい最初のオプションの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="7fc87-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="7fc87-105">それ以外の場合は、オプションの前にはない呼び出された関数の最後の引数としてデフォルト結果が指定されている場合、オプションのデフォルト結果を返します。</span><span class="sxs-lookup"><span data-stu-id="7fc87-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="7fc87-106">返される値は、サポートされているいずれかのデータ型の値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7fc87-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc87-107">構文</span><span class="sxs-lookup"><span data-stu-id="7fc87-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="7fc87-108">引数</span><span class="sxs-lookup"><span data-stu-id="7fc87-108">Arguments</span></span>

<span data-ttu-id="7fc87-109">`expression`: *プリミティブ データ型* (ブール値、数値、またはテキスト)</span><span class="sxs-lookup"><span data-stu-id="7fc87-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="7fc87-110">プリミティブ データ型の値を返す有効な式。</span><span class="sxs-lookup"><span data-stu-id="7fc87-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="7fc87-111">`option 1`: *プリミティブ データ型* (ブール値、数値、またはテキスト)</span><span class="sxs-lookup"><span data-stu-id="7fc87-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="7fc87-112">呼び出された関数の `expression` 引数と同じプリミティブ データ型の値を返す有効な式。</span><span class="sxs-lookup"><span data-stu-id="7fc87-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="7fc87-113">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="7fc87-113">This argument is required.</span></span>

<span data-ttu-id="7fc87-114">`result 1`: *サポートされているいずれかのデータ型*</span><span class="sxs-lookup"><span data-stu-id="7fc87-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="7fc87-115">前のオプションに対応する返された結果。</span><span class="sxs-lookup"><span data-stu-id="7fc87-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="7fc87-116">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="7fc87-116">This argument is required.</span></span>

<span data-ttu-id="7fc87-117">`option N`: *プリミティブ データ型* (ブール値、数値、またはテキスト)</span><span class="sxs-lookup"><span data-stu-id="7fc87-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="7fc87-118">呼び出された関数の `expression` 引数と同じプリミティブ データ型の値を返す有効な式。</span><span class="sxs-lookup"><span data-stu-id="7fc87-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="7fc87-119">この引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="7fc87-119">This argument is optional.</span></span>

<span data-ttu-id="7fc87-120">`result N`: *サポートされているいずれかのデータ型*</span><span class="sxs-lookup"><span data-stu-id="7fc87-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="7fc87-121">前のオプションに対応する返された結果。</span><span class="sxs-lookup"><span data-stu-id="7fc87-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="7fc87-122">この引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="7fc87-122">This argument is optional.</span></span>

<span data-ttu-id="7fc87-123">`default result`: *サポートされているいずれかのデータ型*</span><span class="sxs-lookup"><span data-stu-id="7fc87-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="7fc87-124">一致がない場合に返される結果。</span><span class="sxs-lookup"><span data-stu-id="7fc87-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="7fc87-125">この引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="7fc87-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="7fc87-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="7fc87-126">Return values</span></span>

<span data-ttu-id="7fc87-127">*サポートされているいずれかのデータ型*</span><span class="sxs-lookup"><span data-stu-id="7fc87-127">*Any of the supported data types*</span></span>

<span data-ttu-id="7fc87-128">サポートされているいずれかのデータ型の結果値。</span><span class="sxs-lookup"><span data-stu-id="7fc87-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7fc87-129">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="7fc87-129">Usage notes</span></span>

<span data-ttu-id="7fc87-130">実行時に、一致するものがなく、オプションの既定の結果が定義されていない場合は、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="7fc87-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="7fc87-131">すべての結果は、同じデータ型を使用して指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fc87-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="7fc87-132">構成された結果のデータ型が一致しない場合は、デザイン時に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="7fc87-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="7fc87-133">最初の結果値と *N* 番目の結果値が*コンテナー (レコード)* または*レコード リスト* データ型の値である場合、結果には両方の値に存在するフィールドのみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7fc87-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="7fc87-134">例</span><span class="sxs-lookup"><span data-stu-id="7fc87-134">Example</span></span>

<span data-ttu-id="7fc87-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` は、現在のアプリケーション セッションの日付が 10 月から 12 月の場合に文字列 **"WINTER"** を返します。</span><span class="sxs-lookup"><span data-stu-id="7fc87-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="7fc87-136">それ以外の場合は、空白文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="7fc87-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fc87-137">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7fc87-137">Additional resources</span></span>

[<span data-ttu-id="7fc87-138">論理機能</span><span class="sxs-lookup"><span data-stu-id="7fc87-138">Logical functions</span></span>](er-functions-category-logical.md)
