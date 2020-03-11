---
title: RIGHT ER 関数
description: このトピックでは、RIGHT 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040874"
---
# <span data-ttu-id="042a9-103"><a name="RIGHT">RIGHT ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="042a9-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="042a9-104">この `RIGHT` 関数は、指定された文字列の末尾から指定された数の文字を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="042a9-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="042a9-105">構文</span><span class="sxs-lookup"><span data-stu-id="042a9-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="042a9-106">引数</span><span class="sxs-lookup"><span data-stu-id="042a9-106">Arguments</span></span>

<span data-ttu-id="042a9-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="042a9-107">`text`: *String*</span></span>

<span data-ttu-id="042a9-108">オリジナルのテキストを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="042a9-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="042a9-109">`number`: *整数*</span><span class="sxs-lookup"><span data-stu-id="042a9-109">`number`: *Integer*</span></span>

<span data-ttu-id="042a9-110">元のテキストの末尾から戻される必要がある文字数。</span><span class="sxs-lookup"><span data-stu-id="042a9-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="042a9-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="042a9-111">Return values</span></span>

<span data-ttu-id="042a9-112">*文字列*</span><span class="sxs-lookup"><span data-stu-id="042a9-112">*String*</span></span>

<span data-ttu-id="042a9-113">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="042a9-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="042a9-114">例</span><span class="sxs-lookup"><span data-stu-id="042a9-114">Example</span></span>

<span data-ttu-id="042a9-115">`RIGHT ("Sample", 3)` は、**"ple"** を返します。</span><span class="sxs-lookup"><span data-stu-id="042a9-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="042a9-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="042a9-116">Additional resources</span></span>

[<span data-ttu-id="042a9-117">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="042a9-117">Text functions</span></span>](er-functions-category-text.md)
