---
title: TRANSLATE ER 関数
description: このトピックでは、TRANSLATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040920"
---
# <span data-ttu-id="030fe-103"><a name="TRANSLATE">TRANSLATE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="030fe-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="030fe-104">`TRANSLATE` 関数は、そのすべてまたはその一部が別の文字列に置換した後、*文字列*値として指定されたテキストの文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="030fe-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="030fe-105">構文</span><span class="sxs-lookup"><span data-stu-id="030fe-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="030fe-106">引数</span><span class="sxs-lookup"><span data-stu-id="030fe-106">Arguments</span></span>

<span data-ttu-id="030fe-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="030fe-107">`text`: *String*</span></span>

<span data-ttu-id="030fe-108">*文字列*型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="030fe-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="030fe-109">`pattern`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="030fe-109">`pattern`: *String*</span></span>

<span data-ttu-id="030fe-110">置換が必要なテキスト。</span><span class="sxs-lookup"><span data-stu-id="030fe-110">The text that must be replaced.</span></span>

<span data-ttu-id="030fe-111">`replacement`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="030fe-111">`replacement`: *String*</span></span>

<span data-ttu-id="030fe-112">置換として使用するテキスト。</span><span class="sxs-lookup"><span data-stu-id="030fe-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="030fe-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="030fe-113">Return values</span></span>

<span data-ttu-id="030fe-114">*文字列*</span><span class="sxs-lookup"><span data-stu-id="030fe-114">*String*</span></span>

<span data-ttu-id="030fe-115">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="030fe-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="030fe-116">例</span><span class="sxs-lookup"><span data-stu-id="030fe-116">Example</span></span>

<span data-ttu-id="030fe-117">`TRANSLATE ("abcdef", "cd", "GH")` は、パターン **"cd"** を文字列 **"GH"** に置き換え、**"abGHef"** 返します。</span><span class="sxs-lookup"><span data-stu-id="030fe-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="030fe-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="030fe-118">Additional resources</span></span>

[<span data-ttu-id="030fe-119">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="030fe-119">Text functions</span></span>](er-functions-category-text.md)
