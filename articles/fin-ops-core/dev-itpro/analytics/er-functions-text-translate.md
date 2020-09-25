---
title: TRANSLATE ER 関数
description: このトピックでは、TRANSLATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 51b9a2e25a9f1dfc08e9e0f7fc3ad84b359a6d1b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744242"
---
# <a name="translate-er-function"></a><span data-ttu-id="14456-103">TRANSLATE ER 関数</span><span class="sxs-lookup"><span data-stu-id="14456-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14456-104">`TRANSLATE` 関数は、指定されたテキストを別の提供されたセットの文字に置換した結果を含む *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="14456-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="14456-105">構文</span><span class="sxs-lookup"><span data-stu-id="14456-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="14456-106">引数</span><span class="sxs-lookup"><span data-stu-id="14456-106">Arguments</span></span>

<span data-ttu-id="14456-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="14456-107">`text`: *String*</span></span>

<span data-ttu-id="14456-108">*文字列*型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="14456-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="14456-109">`pattern`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="14456-109">`pattern`: *String*</span></span>

<span data-ttu-id="14456-110">置換が必要なテキスト。</span><span class="sxs-lookup"><span data-stu-id="14456-110">The text that must be replaced.</span></span>

<span data-ttu-id="14456-111">`replacement`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="14456-111">`replacement`: *String*</span></span>

<span data-ttu-id="14456-112">置換として使用するテキスト。</span><span class="sxs-lookup"><span data-stu-id="14456-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="14456-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="14456-113">Return values</span></span>

<span data-ttu-id="14456-114">*文字列*</span><span class="sxs-lookup"><span data-stu-id="14456-114">*String*</span></span>

<span data-ttu-id="14456-115">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="14456-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="14456-116">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="14456-116">Usage notes</span></span>

<span data-ttu-id="14456-117">`TRANSLATE` 関数は一度に 1 文字ずつ置き換えます。</span><span class="sxs-lookup"><span data-stu-id="14456-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="14456-118">この関数は、`text` 引数の最初の文字を `pattern` 引数の最初の文字に、次に 2 番目の文字に置き換え、完了するまで同じフローに従います。</span><span class="sxs-lookup"><span data-stu-id="14456-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="14456-119">引数 `text` と `pattern` の文字が一致すると、`pattern` 引数の文字と同じ位置にある `replacement` 引数の文字に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="14456-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="14456-120">文字が `pattern` 引数に複数回出現する場合は、この文字の最初の出現に対応する `replacement` 引数マッピングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="14456-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="14456-121">例 1</span><span class="sxs-lookup"><span data-stu-id="14456-121">Example 1</span></span>

<span data-ttu-id="14456-122">`TRANSLATE ("abcdef", "cd", "GH")` は、次の理由により、指定された **"abcdef"** テキストの **"c"** 文字を `replacement` テキストの **"G"** 文字に置き換えます:</span><span class="sxs-lookup"><span data-stu-id="14456-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="14456-123">**"c"** 文字は、最初の位置の `pattern` テキストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="14456-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="14456-124">`replacement` テキストの最初の位置には **"G"** 文字が含まれます。</span><span class="sxs-lookup"><span data-stu-id="14456-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="14456-125">例 2</span><span class="sxs-lookup"><span data-stu-id="14456-125">Example 2</span></span>

<span data-ttu-id="14456-126">`TRANSLATE ("abcdef", "ccd", "GH")` は、**"abGdef"** を返します。</span><span class="sxs-lookup"><span data-stu-id="14456-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="14456-127">例 3</span><span class="sxs-lookup"><span data-stu-id="14456-127">Example 3</span></span>

<span data-ttu-id="14456-128">`TRANSLATE ("abccba", "abc", "123")` は、**"123321"** を返します。</span><span class="sxs-lookup"><span data-stu-id="14456-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14456-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="14456-129">Additional resources</span></span>

[<span data-ttu-id="14456-130">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="14456-130">Text functions</span></span>](er-functions-category-text.md)
