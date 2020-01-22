---
title: VALUE ER 関数
description: このトピックでは、VALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917629"
---
# <span data-ttu-id="e509e-103"><a name="VALUE">VALUE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="e509e-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e509e-104">`VALUE` 関数は、指定された文字列から変換された*実数*値を返します。</span><span class="sxs-lookup"><span data-stu-id="e509e-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e509e-105">構文</span><span class="sxs-lookup"><span data-stu-id="e509e-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="e509e-106">引数</span><span class="sxs-lookup"><span data-stu-id="e509e-106">Arguments</span></span>

<span data-ttu-id="e509e-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="e509e-107">`text`: *String*</span></span>

<span data-ttu-id="e509e-108">数値に変換する必要がある文字列値。</span><span class="sxs-lookup"><span data-stu-id="e509e-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="e509e-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="e509e-109">Return values</span></span>

<span data-ttu-id="e509e-110">*実績*</span><span class="sxs-lookup"><span data-stu-id="e509e-110">*Real*</span></span>

<span data-ttu-id="e509e-111">結果数値。</span><span class="sxs-lookup"><span data-stu-id="e509e-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e509e-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="e509e-112">Usage notes</span></span>

<span data-ttu-id="e509e-113">コンマとドット (.) が小数点の区切り記号とみなされ、先頭のハイフン (-) は負の記号として使用されます。</span><span class="sxs-lookup"><span data-stu-id="e509e-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="e509e-114">他の数値以外の文字が指定された文字列に含まれている場合、実行時に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="e509e-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="e509e-115">例 1</span><span class="sxs-lookup"><span data-stu-id="e509e-115">Example 1</span></span>

<span data-ttu-id="e509e-116">`VALUE ("1 234,56")` で例外がスローされました。</span><span class="sxs-lookup"><span data-stu-id="e509e-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="e509e-117">例 2</span><span class="sxs-lookup"><span data-stu-id="e509e-117">Example 2</span></span>

<span data-ttu-id="e509e-118">`VALUE ("1234,56")` は、**1234.56** を返します。</span><span class="sxs-lookup"><span data-stu-id="e509e-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e509e-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e509e-119">Additional resources</span></span>

[<span data-ttu-id="e509e-120">型変換関数</span><span class="sxs-lookup"><span data-stu-id="e509e-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
