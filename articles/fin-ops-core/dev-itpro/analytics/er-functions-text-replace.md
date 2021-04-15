---
title: REPLACE ER 関数
description: このトピックでは、REPLACE 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 21cdd8532730925b7d5c6f5b3bb565dcd365dd6d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746203"
---
# <a name="replace-er-function"></a><span data-ttu-id="1e2b2-103">REPLACE ER 関数</span><span class="sxs-lookup"><span data-stu-id="1e2b2-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e2b2-104">`REPLACE` 関数は、そのすべてまたはその一部が別の文字列に置換した後、*文字列* 値として指定されたテキストの文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2b2-105">構文</span><span class="sxs-lookup"><span data-stu-id="1e2b2-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="1e2b2-106">引数</span><span class="sxs-lookup"><span data-stu-id="1e2b2-106">Arguments</span></span>

<span data-ttu-id="1e2b2-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="1e2b2-107">`text`: *String*</span></span>

<span data-ttu-id="1e2b2-108">*文字列* 型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="1e2b2-109">`pattern`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="1e2b2-109">`pattern`: *String*</span></span>

<span data-ttu-id="1e2b2-110">`regular expression flag` 引数が **FALSE** の場合、この引数には置換する必要のあるテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="1e2b2-111">`regular expression flag` 引数が **TRUE** の場合、この引数には検索パターンと置換後のテキストの両方を定義する正規表現が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="1e2b2-112">`replacement`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="1e2b2-112">`replacement`: *String*</span></span>

<span data-ttu-id="1e2b2-113">`regular expression flag` 引数が **FALSE** の場合、この引数には置換として使用するテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="1e2b2-114">`regular expression flag` 引数が **TRUE** の場合、この引数は使用されません。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="1e2b2-115">`regular expression flag`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="1e2b2-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="1e2b2-116">正規表現を使用して置換を行うかどうかを示す *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e2b2-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="1e2b2-117">Return values</span></span>

<span data-ttu-id="1e2b2-118">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e2b2-118">*String*</span></span>

<span data-ttu-id="1e2b2-119">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1e2b2-120">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="1e2b2-120">Usage notes</span></span>

<span data-ttu-id="1e2b2-121">`regular expression flag` 引数が **TRUE** の場合、この関数は `pattern` 引数で指定された正規表現を適用することで変更された後、指定された文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="1e2b2-122">正規表現は、置換する必要のある文字を検索するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="1e2b2-123">`regular expression flag` 引数が **FALSE** の場合、この関数は、`pattern` 引数で定義された文字セットが `replacement` 引数の文字に置換された後、指定された文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="1e2b2-124">例 1</span><span class="sxs-lookup"><span data-stu-id="1e2b2-124">Example 1</span></span>

<span data-ttu-id="1e2b2-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` は、すべての数値以外の記号を削除する正規表現を適用し、**"19234564971"** を返します。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="1e2b2-126">例 2</span><span class="sxs-lookup"><span data-stu-id="1e2b2-126">Example 2</span></span>

<span data-ttu-id="1e2b2-127">`REPLACE ("abcdef", "cd", "GH", false)` は、パターン **"cd"** を文字列 **"GH"** に置き換え、**"abGHef"** 返します。</span><span class="sxs-lookup"><span data-stu-id="1e2b2-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e2b2-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1e2b2-128">Additional resources</span></span>

[<span data-ttu-id="1e2b2-129">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="1e2b2-129">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]