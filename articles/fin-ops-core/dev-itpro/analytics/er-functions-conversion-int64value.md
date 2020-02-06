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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916548"
---
# <span data-ttu-id="0f6f2-103"><a name="INT64VALUE">INT64VALUE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="0f6f2-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f6f2-104">`INT64VALUE` 関数は、指定された文字列を表す *Int64* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="0f6f2-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0f6f2-105">構文 1</span><span class="sxs-lookup"><span data-stu-id="0f6f2-105">Syntax 1</span></span>

```
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="0f6f2-106">構文 2</span><span class="sxs-lookup"><span data-stu-id="0f6f2-106">Syntax 2</span></span>

```
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="0f6f2-107">引数</span><span class="sxs-lookup"><span data-stu-id="0f6f2-107">Arguments</span></span>

<span data-ttu-id="0f6f2-108">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="0f6f2-108">`text`: *String*</span></span>

<span data-ttu-id="0f6f2-109">*Int64* 数に変換する必要があるテキスト値。</span><span class="sxs-lookup"><span data-stu-id="0f6f2-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="0f6f2-110">`number`: *実数*または*整数*</span><span class="sxs-lookup"><span data-stu-id="0f6f2-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="0f6f2-111">*Int64* 数に変換する必要がある数値の*実数*または*整数*値。</span><span class="sxs-lookup"><span data-stu-id="0f6f2-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="0f6f2-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="0f6f2-112">Return values</span></span>

<span data-ttu-id="0f6f2-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="0f6f2-113">*Int64*</span></span>

<span data-ttu-id="0f6f2-114">結果数値。</span><span class="sxs-lookup"><span data-stu-id="0f6f2-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0f6f2-115">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="0f6f2-115">Usage notes</span></span>

<span data-ttu-id="0f6f2-116">任意の小数点以下の桁数が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="0f6f2-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="0f6f2-117">例 1</span><span class="sxs-lookup"><span data-stu-id="0f6f2-117">Example 1</span></span>

<span data-ttu-id="0f6f2-118">`INT64VALUE ("22565422744")` は、*Int64* の値 **22565422744** を返します。</span><span class="sxs-lookup"><span data-stu-id="0f6f2-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0f6f2-119">例 2</span><span class="sxs-lookup"><span data-stu-id="0f6f2-119">Example 2</span></span>

<span data-ttu-id="0f6f2-120">`INT64VALUE ( VALUE("22565422744.77"))` は、*Int64* の値 **22565422744** を返します。</span><span class="sxs-lookup"><span data-stu-id="0f6f2-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f6f2-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0f6f2-121">Additional resources</span></span>

[<span data-ttu-id="0f6f2-122">型変換関数</span><span class="sxs-lookup"><span data-stu-id="0f6f2-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)