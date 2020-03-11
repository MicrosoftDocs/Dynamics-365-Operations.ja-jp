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
ms.openlocfilehash: 6784384bac31d8c7cdc9c6f71b7dbab79c15a934
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041104"
---
# <span data-ttu-id="fd0a1-103"><a name="LOWER">LOWER ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="fd0a1-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd0a1-104">`LOWER` 関数は、小文字に変換した後の*文字列*値として指定されたテキスト返します。</span><span class="sxs-lookup"><span data-stu-id="fd0a1-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0a1-105">構文</span><span class="sxs-lookup"><span data-stu-id="fd0a1-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="fd0a1-106">引数</span><span class="sxs-lookup"><span data-stu-id="fd0a1-106">Arguments</span></span>

<span data-ttu-id="fd0a1-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="fd0a1-107">`text`: *String*</span></span>

<span data-ttu-id="fd0a1-108">*文字列*値は、テキストを指定。</span><span class="sxs-lookup"><span data-stu-id="fd0a1-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="fd0a1-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="fd0a1-109">Return values</span></span>

<span data-ttu-id="fd0a1-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="fd0a1-110">*String*</span></span>

<span data-ttu-id="fd0a1-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="fd0a1-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fd0a1-112">例</span><span class="sxs-lookup"><span data-stu-id="fd0a1-112">Example</span></span>

<span data-ttu-id="fd0a1-113">`LOWER ("Sample")` は、**"sample"** を返します。</span><span class="sxs-lookup"><span data-stu-id="fd0a1-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd0a1-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fd0a1-114">Additional resources</span></span>

[<span data-ttu-id="fd0a1-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="fd0a1-115">Text functions</span></span>](er-functions-category-text.md)
