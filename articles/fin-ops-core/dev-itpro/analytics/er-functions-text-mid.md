---
title: MID ER 関数
description: このトピックでは、MID 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 9a9ff3f1055f6757d6d4073dbb816773d8bfc8ba
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746270"
---
# <a name="mid-er-function"></a><span data-ttu-id="f0329-103">MID ER 関数</span><span class="sxs-lookup"><span data-stu-id="f0329-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0329-104">`MID` 関数は、指定された位置から始まる指定された文字列から、指定された数の文字を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="f0329-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0329-105">構文</span><span class="sxs-lookup"><span data-stu-id="f0329-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="f0329-106">引数</span><span class="sxs-lookup"><span data-stu-id="f0329-106">Arguments</span></span>

<span data-ttu-id="f0329-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="f0329-107">`text`: *String*</span></span>

<span data-ttu-id="f0329-108">文字を返すテキストを指定する *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="f0329-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="f0329-109">`starting position`: *整数*</span><span class="sxs-lookup"><span data-stu-id="f0329-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="f0329-110">指定されたテキストから返す必要がある最初の文字の位置を指定する *整数* 値。</span><span class="sxs-lookup"><span data-stu-id="f0329-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="f0329-111">`number of characters`: *整数*</span><span class="sxs-lookup"><span data-stu-id="f0329-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="f0329-112">指定された開始位置から始め、返す必要がある文字の数を指定する *整数* 値。</span><span class="sxs-lookup"><span data-stu-id="f0329-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="f0329-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="f0329-113">Return values</span></span>

<span data-ttu-id="f0329-114">*文字列*</span><span class="sxs-lookup"><span data-stu-id="f0329-114">*String*</span></span>

<span data-ttu-id="f0329-115">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="f0329-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f0329-116">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="f0329-116">Usage notes</span></span>

<span data-ttu-id="f0329-117">`starting position` 引数の値が 0 (ゼロ) よりも小さい場合は、指定された文字列の最初の位置から返される文字がカウントされます。</span><span class="sxs-lookup"><span data-stu-id="f0329-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="f0329-118">`starting position` 引数の値が指定した文字列の長さを超える場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="f0329-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="f0329-119">例</span><span class="sxs-lookup"><span data-stu-id="f0329-119">Example</span></span>

<span data-ttu-id="f0329-120">`MID ("Sample", 2, 3)` は、**"amp"** を返します。</span><span class="sxs-lookup"><span data-stu-id="f0329-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0329-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f0329-121">Additional resources</span></span>

[<span data-ttu-id="f0329-122">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="f0329-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]