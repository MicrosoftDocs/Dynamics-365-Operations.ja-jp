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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042691"
---
# <span data-ttu-id="09d8b-103"><a name="INT64VALUE">INT64VALUE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="09d8b-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09d8b-104">`INT64VALUE` 関数は、指定された文字列を表す *Int64* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="09d8b-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="09d8b-105">構文 1</span><span class="sxs-lookup"><span data-stu-id="09d8b-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="09d8b-106">構文 2</span><span class="sxs-lookup"><span data-stu-id="09d8b-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="09d8b-107">引数</span><span class="sxs-lookup"><span data-stu-id="09d8b-107">Arguments</span></span>

<span data-ttu-id="09d8b-108">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="09d8b-108">`text`: *String*</span></span>

<span data-ttu-id="09d8b-109">*Int64* 数に変換する必要があるテキスト値。</span><span class="sxs-lookup"><span data-stu-id="09d8b-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="09d8b-110">`number`: *実数*または*整数*</span><span class="sxs-lookup"><span data-stu-id="09d8b-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="09d8b-111">*Int64* 数に変換する必要がある数値の*実数*または*整数*値。</span><span class="sxs-lookup"><span data-stu-id="09d8b-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="09d8b-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="09d8b-112">Return values</span></span>

<span data-ttu-id="09d8b-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="09d8b-113">*Int64*</span></span>

<span data-ttu-id="09d8b-114">結果数値。</span><span class="sxs-lookup"><span data-stu-id="09d8b-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="09d8b-115">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="09d8b-115">Usage notes</span></span>

<span data-ttu-id="09d8b-116">任意の小数点以下の桁数が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="09d8b-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="09d8b-117">例 1</span><span class="sxs-lookup"><span data-stu-id="09d8b-117">Example 1</span></span>

<span data-ttu-id="09d8b-118">`INT64VALUE ("22565422744")` は、*Int64* の値 **22565422744** を返します。</span><span class="sxs-lookup"><span data-stu-id="09d8b-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="09d8b-119">例 2</span><span class="sxs-lookup"><span data-stu-id="09d8b-119">Example 2</span></span>

<span data-ttu-id="09d8b-120">`INT64VALUE ( VALUE("22565422744.77"))` は、*Int64* の値 **22565422744** を返します。</span><span class="sxs-lookup"><span data-stu-id="09d8b-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09d8b-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="09d8b-121">Additional resources</span></span>

[<span data-ttu-id="09d8b-122">型変換関数</span><span class="sxs-lookup"><span data-stu-id="09d8b-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
