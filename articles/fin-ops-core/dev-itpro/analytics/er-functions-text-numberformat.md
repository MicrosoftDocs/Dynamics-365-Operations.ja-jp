---
title: NUMBERFORMAT ER 関数
description: このトピックでは、NUMBERFORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 2c3907d1d2c74c852f4f90731e5f4bc23bfbd717
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680269"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="c58e5-103">NUMBERFORMAT ER 関数</span><span class="sxs-lookup"><span data-stu-id="c58e5-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c58e5-104">`NUMBERFORMAT` 関数は、指定された形式およびオプションで指定された [カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で、指定された数を表す *文字列* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="c58e5-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="c58e5-105">サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c58e5-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="c58e5-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="c58e5-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="c58e5-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="c58e5-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="c58e5-108">引数</span><span class="sxs-lookup"><span data-stu-id="c58e5-108">Arguments</span></span>

<span data-ttu-id="c58e5-109">`number`: *整数* または *実数*</span><span class="sxs-lookup"><span data-stu-id="c58e5-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="c58e5-110">書式設定する必要がある数値を指定する数値。</span><span class="sxs-lookup"><span data-stu-id="c58e5-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="c58e5-111">`format` : *文字列*</span><span class="sxs-lookup"><span data-stu-id="c58e5-111">`format` : *String*</span></span>

<span data-ttu-id="c58e5-112">形式を表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="c58e5-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="c58e5-113">`culture`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="c58e5-113">`culture`: *String*</span></span>

<span data-ttu-id="c58e5-114">書式設定に使用するカルチャを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="c58e5-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="c58e5-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="c58e5-115">Return values</span></span>

<span data-ttu-id="c58e5-116">*文字列*</span><span class="sxs-lookup"><span data-stu-id="c58e5-116">*String*</span></span>

<span data-ttu-id="c58e5-117">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="c58e5-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c58e5-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="c58e5-118">Usage notes</span></span>

<span data-ttu-id="c58e5-119">カルチャが呼び出された関数の引数として定義されていない場合は、この関数が実行されるコンテキストによって、数値の書式設定に使用されるカルチャが決まります。</span><span class="sxs-lookup"><span data-stu-id="c58e5-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="c58e5-120">例 1</span><span class="sxs-lookup"><span data-stu-id="c58e5-120">Example 1</span></span>

<span data-ttu-id="c58e5-121">**EN-US** カルチャの場合、`NUMBERFORMAT (0.45, "p")` は **"45.00 %"** を返し、`NUMBERFORMAT (10.45, "#")` は **"10"** を返します。</span><span class="sxs-lookup"><span data-stu-id="c58e5-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c58e5-122">例 2</span><span class="sxs-lookup"><span data-stu-id="c58e5-122">Example 2</span></span>

<span data-ttu-id="c58e5-123">`NUMBERFORMAT (10/3, "F2", "de")` は **3,33** 返すが、一方では、`NUMBERFORMAT (10/3, "F2", "en-us")` は **3.33** を返します。</span><span class="sxs-lookup"><span data-stu-id="c58e5-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c58e5-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c58e5-124">Additional resources</span></span>

[<span data-ttu-id="c58e5-125">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="c58e5-125">Text functions</span></span>](er-functions-category-text.md)
