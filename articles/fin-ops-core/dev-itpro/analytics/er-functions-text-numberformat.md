---
title: NUMBERFORMAT ER 関数
description: このトピックでは、NUMBERFORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890386"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="375d9-103">NUMBERFORMAT ER 関数</span><span class="sxs-lookup"><span data-stu-id="375d9-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="375d9-104">`NUMBERFORMAT` 関数は、指定された形式およびオプションで指定された [カルチャ](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で、指定された数を表す *文字列* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="375d9-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="375d9-105">サポートされている形式の詳細については、[標準](/dotnet/standard/base-types/standard-numeric-format-strings) と [カスタム](/dotnet/standard/base-types/custom-numeric-format-strings) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="375d9-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-numeric-format-strings) and [custom](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="375d9-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="375d9-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="375d9-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="375d9-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="375d9-108">引数</span><span class="sxs-lookup"><span data-stu-id="375d9-108">Arguments</span></span>

<span data-ttu-id="375d9-109">`number`: *整数* または *実数*</span><span class="sxs-lookup"><span data-stu-id="375d9-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="375d9-110">書式設定する必要がある数値を指定する数値。</span><span class="sxs-lookup"><span data-stu-id="375d9-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="375d9-111">`format` : *文字列*</span><span class="sxs-lookup"><span data-stu-id="375d9-111">`format` : *String*</span></span>

<span data-ttu-id="375d9-112">形式を表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="375d9-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="375d9-113">`culture`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="375d9-113">`culture`: *String*</span></span>

<span data-ttu-id="375d9-114">書式設定に使用するカルチャを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="375d9-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="375d9-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="375d9-115">Return values</span></span>

<span data-ttu-id="375d9-116">*文字列*</span><span class="sxs-lookup"><span data-stu-id="375d9-116">*String*</span></span>

<span data-ttu-id="375d9-117">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="375d9-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="375d9-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="375d9-118">Usage notes</span></span>

<span data-ttu-id="375d9-119">カルチャが呼び出された関数の引数として定義されていない場合は、この関数が実行されるコンテキストによって、数値の書式設定に使用されるカルチャが決まります。</span><span class="sxs-lookup"><span data-stu-id="375d9-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="375d9-120">例 1</span><span class="sxs-lookup"><span data-stu-id="375d9-120">Example 1</span></span>

<span data-ttu-id="375d9-121">**EN-US** カルチャの場合、`NUMBERFORMAT (0.45, "p")` は **"45.00 %"** を返し、`NUMBERFORMAT (10.45, "#")` は **"10"** を返します。</span><span class="sxs-lookup"><span data-stu-id="375d9-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="375d9-122">例 2</span><span class="sxs-lookup"><span data-stu-id="375d9-122">Example 2</span></span>

<span data-ttu-id="375d9-123">`NUMBERFORMAT (10/3, "F2", "de")` は **3,33** 返すが、一方では、`NUMBERFORMAT (10/3, "F2", "en-us")` は **3.33** を返します。</span><span class="sxs-lookup"><span data-stu-id="375d9-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="375d9-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="375d9-124">Additional resources</span></span>

[<span data-ttu-id="375d9-125">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="375d9-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]