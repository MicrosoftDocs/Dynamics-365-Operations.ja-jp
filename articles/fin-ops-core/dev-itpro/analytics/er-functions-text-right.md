---
title: RIGHT ER 関数
description: このトピックでは、RIGHT 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746126"
---
# <a name="right-er-function"></a><span data-ttu-id="a0342-103">RIGHT ER 関数</span><span class="sxs-lookup"><span data-stu-id="a0342-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0342-104">この `RIGHT` 関数は、指定された文字列の末尾から指定された数の文字を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="a0342-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0342-105">構文</span><span class="sxs-lookup"><span data-stu-id="a0342-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="a0342-106">引数</span><span class="sxs-lookup"><span data-stu-id="a0342-106">Arguments</span></span>

<span data-ttu-id="a0342-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="a0342-107">`text`: *String*</span></span>

<span data-ttu-id="a0342-108">オリジナルのテキストを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="a0342-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="a0342-109">`number`: *整数*</span><span class="sxs-lookup"><span data-stu-id="a0342-109">`number`: *Integer*</span></span>

<span data-ttu-id="a0342-110">元のテキストの末尾から戻される必要がある文字数。</span><span class="sxs-lookup"><span data-stu-id="a0342-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="a0342-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="a0342-111">Return values</span></span>

<span data-ttu-id="a0342-112">*文字列*</span><span class="sxs-lookup"><span data-stu-id="a0342-112">*String*</span></span>

<span data-ttu-id="a0342-113">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="a0342-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a0342-114">例</span><span class="sxs-lookup"><span data-stu-id="a0342-114">Example</span></span>

<span data-ttu-id="a0342-115">`RIGHT ("Sample", 3)` は、**"ple"** を返します。</span><span class="sxs-lookup"><span data-stu-id="a0342-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0342-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a0342-116">Additional resources</span></span>

[<span data-ttu-id="a0342-117">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="a0342-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]