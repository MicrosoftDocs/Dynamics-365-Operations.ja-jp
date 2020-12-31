---
title: PADLEFT ER 関数
description: このトピックでは、PADLEFT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 268941d8bc0bd4dc6de6d2597c05a11c1f530f15
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680149"
---
# <a name="padleft-er-function"></a><span data-ttu-id="00f90-103">PADLEFT ER 関数</span><span class="sxs-lookup"><span data-stu-id="00f90-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00f90-104">`PADLEFT` 関数は、指定の文字列から始まる指定の文字でパディングされた指定の長さの *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="00f90-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="00f90-105">構文</span><span class="sxs-lookup"><span data-stu-id="00f90-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="00f90-106">引数</span><span class="sxs-lookup"><span data-stu-id="00f90-106">Arguments</span></span>

<span data-ttu-id="00f90-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="00f90-107">`text`: *String*</span></span>

<span data-ttu-id="00f90-108">オリジナルのテキストを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="00f90-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="00f90-109">`length`: *整数*</span><span class="sxs-lookup"><span data-stu-id="00f90-109">`length`: *Integer*</span></span>

<span data-ttu-id="00f90-110">パディングされた文字列の最終文字数を表す *整数* 値。</span><span class="sxs-lookup"><span data-stu-id="00f90-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="00f90-111">`padding chars`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="00f90-111">`padding chars`: *String*</span></span>

<span data-ttu-id="00f90-112">パディングに使用する文字。</span><span class="sxs-lookup"><span data-stu-id="00f90-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="00f90-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="00f90-113">Return values</span></span>

<span data-ttu-id="00f90-114">*文字列*</span><span class="sxs-lookup"><span data-stu-id="00f90-114">*String*</span></span>

<span data-ttu-id="00f90-115">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="00f90-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="00f90-116">例</span><span class="sxs-lookup"><span data-stu-id="00f90-116">Example</span></span>

<span data-ttu-id="00f90-117">`PADLEFT ("1234", 10, "`&nbsp;`")` は、テキスト文字列の **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"** を返します。</span><span class="sxs-lookup"><span data-stu-id="00f90-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00f90-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="00f90-118">Additional resources</span></span>

[<span data-ttu-id="00f90-119">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="00f90-119">Text functions</span></span>](er-functions-category-text.md)
