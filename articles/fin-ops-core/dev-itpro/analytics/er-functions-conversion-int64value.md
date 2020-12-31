---
title: INT64VALUE ER 関数
description: このトピックでは、INT64VALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb750116312df82448f5a0048e380f9e5274f8e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686054"
---
# <a name="int64value-er-function"></a><span data-ttu-id="22f47-103">INT64VALUE ER 関数</span><span class="sxs-lookup"><span data-stu-id="22f47-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22f47-104">`INT64VALUE` 関数は、指定された文字列を表す *Int64* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="22f47-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="22f47-105">構文 1</span><span class="sxs-lookup"><span data-stu-id="22f47-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="22f47-106">構文 2</span><span class="sxs-lookup"><span data-stu-id="22f47-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="22f47-107">引数</span><span class="sxs-lookup"><span data-stu-id="22f47-107">Arguments</span></span>

<span data-ttu-id="22f47-108">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="22f47-108">`text`: *String*</span></span>

<span data-ttu-id="22f47-109">*Int64* 数に変換する必要があるテキスト値。</span><span class="sxs-lookup"><span data-stu-id="22f47-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="22f47-110">`number`: *実数* または *整数*</span><span class="sxs-lookup"><span data-stu-id="22f47-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="22f47-111">*Int64* 数に変換する必要がある数値の *実数* または *整数* 値。</span><span class="sxs-lookup"><span data-stu-id="22f47-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="22f47-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="22f47-112">Return values</span></span>

<span data-ttu-id="22f47-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="22f47-113">*Int64*</span></span>

<span data-ttu-id="22f47-114">結果数値。</span><span class="sxs-lookup"><span data-stu-id="22f47-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="22f47-115">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="22f47-115">Usage notes</span></span>

<span data-ttu-id="22f47-116">任意の小数点以下の桁数が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="22f47-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="22f47-117">例 1</span><span class="sxs-lookup"><span data-stu-id="22f47-117">Example 1</span></span>

<span data-ttu-id="22f47-118">`INT64VALUE ("22565422744")` は、*Int64* の値 **22565422744** を返します。</span><span class="sxs-lookup"><span data-stu-id="22f47-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="22f47-119">例 2</span><span class="sxs-lookup"><span data-stu-id="22f47-119">Example 2</span></span>

<span data-ttu-id="22f47-120">`INT64VALUE ( VALUE("22565422744.77"))` は、*Int64* の値 **22565422744** を返します。</span><span class="sxs-lookup"><span data-stu-id="22f47-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22f47-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="22f47-121">Additional resources</span></span>

[<span data-ttu-id="22f47-122">型変換関数</span><span class="sxs-lookup"><span data-stu-id="22f47-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
