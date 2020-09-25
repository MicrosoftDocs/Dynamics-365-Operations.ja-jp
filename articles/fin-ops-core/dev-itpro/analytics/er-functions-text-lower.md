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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12577e571c8e87db79395895e2a22e66ee7df32c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745684"
---
# <a name="lower-er-function"></a><span data-ttu-id="93e68-103">LOWER ER 関数</span><span class="sxs-lookup"><span data-stu-id="93e68-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93e68-104">`LOWER` 関数は、小文字に変換した後の*文字列*値として指定されたテキスト返します。</span><span class="sxs-lookup"><span data-stu-id="93e68-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e68-105">構文</span><span class="sxs-lookup"><span data-stu-id="93e68-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="93e68-106">引数</span><span class="sxs-lookup"><span data-stu-id="93e68-106">Arguments</span></span>

<span data-ttu-id="93e68-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="93e68-107">`text`: *String*</span></span>

<span data-ttu-id="93e68-108">*文字列*値は、テキストを指定。</span><span class="sxs-lookup"><span data-stu-id="93e68-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="93e68-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="93e68-109">Return values</span></span>

<span data-ttu-id="93e68-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="93e68-110">*String*</span></span>

<span data-ttu-id="93e68-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="93e68-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="93e68-112">例</span><span class="sxs-lookup"><span data-stu-id="93e68-112">Example</span></span>

<span data-ttu-id="93e68-113">`LOWER ("Sample")` は、**"sample"** を返します。</span><span class="sxs-lookup"><span data-stu-id="93e68-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93e68-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="93e68-114">Additional resources</span></span>

[<span data-ttu-id="93e68-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="93e68-115">Text functions</span></span>](er-functions-category-text.md)
