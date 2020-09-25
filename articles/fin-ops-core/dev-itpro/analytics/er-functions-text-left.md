---
title: LEFT ER 関数
description: このトピックでは、LEFT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 112852ab955fdf8de9f78cc93486cc1d5f048517
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743786"
---
# <a name="left-er-function"></a><span data-ttu-id="e6a1e-103">LEFT ER 関数</span><span class="sxs-lookup"><span data-stu-id="e6a1e-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6a1e-104">`LEFT` 関数は、指定された文字列の冒頭から指定された数の文字を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="e6a1e-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a1e-105">構文</span><span class="sxs-lookup"><span data-stu-id="e6a1e-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="e6a1e-106">引数</span><span class="sxs-lookup"><span data-stu-id="e6a1e-106">Arguments</span></span>

<span data-ttu-id="e6a1e-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="e6a1e-107">`text`: *String*</span></span>

<span data-ttu-id="e6a1e-108">オリジナルのテキストを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="e6a1e-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="e6a1e-109">`number`: *整数*</span><span class="sxs-lookup"><span data-stu-id="e6a1e-109">`number`: *Integer*</span></span>

<span data-ttu-id="e6a1e-110">元のテキストの冒頭から戻される必要がある文字数。</span><span class="sxs-lookup"><span data-stu-id="e6a1e-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="e6a1e-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="e6a1e-111">Return values</span></span>

<span data-ttu-id="e6a1e-112">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e6a1e-112">*String*</span></span>

<span data-ttu-id="e6a1e-113">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="e6a1e-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e6a1e-114">例</span><span class="sxs-lookup"><span data-stu-id="e6a1e-114">Example</span></span>

<span data-ttu-id="e6a1e-115">`LEFT ("Sample", 3)` は、**"Sam"** を返します。</span><span class="sxs-lookup"><span data-stu-id="e6a1e-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6a1e-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e6a1e-116">Additional resources</span></span>

[<span data-ttu-id="e6a1e-117">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="e6a1e-117">Text functions</span></span>](er-functions-category-text.md)
