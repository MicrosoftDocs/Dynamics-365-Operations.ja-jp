---
title: LOWER ER 関数
description: このトピックでは、LOWER 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad971bd78fa1da17be916efcc6857aa32575f7ac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680317"
---
# <a name="lower-er-function"></a><span data-ttu-id="f06b0-103">LOWER ER 関数</span><span class="sxs-lookup"><span data-stu-id="f06b0-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f06b0-104">`LOWER` 関数は、小文字に変換した後の *文字列* 値として指定されたテキスト返します。</span><span class="sxs-lookup"><span data-stu-id="f06b0-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="f06b0-105">構文</span><span class="sxs-lookup"><span data-stu-id="f06b0-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="f06b0-106">引数</span><span class="sxs-lookup"><span data-stu-id="f06b0-106">Arguments</span></span>

<span data-ttu-id="f06b0-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="f06b0-107">`text`: *String*</span></span>

<span data-ttu-id="f06b0-108">*文字列* 値は、テキストを指定。</span><span class="sxs-lookup"><span data-stu-id="f06b0-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="f06b0-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="f06b0-109">Return values</span></span>

<span data-ttu-id="f06b0-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="f06b0-110">*String*</span></span>

<span data-ttu-id="f06b0-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="f06b0-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f06b0-112">例</span><span class="sxs-lookup"><span data-stu-id="f06b0-112">Example</span></span>

<span data-ttu-id="f06b0-113">`LOWER ("Sample")` は、**"sample"** を返します。</span><span class="sxs-lookup"><span data-stu-id="f06b0-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f06b0-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f06b0-114">Additional resources</span></span>

[<span data-ttu-id="f06b0-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="f06b0-115">Text functions</span></span>](er-functions-category-text.md)
