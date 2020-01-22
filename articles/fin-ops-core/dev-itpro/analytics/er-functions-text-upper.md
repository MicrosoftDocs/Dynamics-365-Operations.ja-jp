---
title: UPPER ER 関数
description: このトピックでは、UPPER 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: ed862ab823cfc3539c420d3066c9397e1e6d870e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916686"
---
# <span data-ttu-id="5e76d-103"><a name="UPPER">UPPER ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="5e76d-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e76d-104">`UPPER` 関数は、大文字に変換した後の*文字列*値として指定されたテキスト返します。</span><span class="sxs-lookup"><span data-stu-id="5e76d-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e76d-105">構文</span><span class="sxs-lookup"><span data-stu-id="5e76d-105">Syntax</span></span>

```
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="5e76d-106">引数</span><span class="sxs-lookup"><span data-stu-id="5e76d-106">Arguments</span></span>

<span data-ttu-id="5e76d-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="5e76d-107">`text`: *String*</span></span>

<span data-ttu-id="5e76d-108">*文字列*型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="5e76d-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5e76d-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e76d-109">Return values</span></span>

<span data-ttu-id="5e76d-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="5e76d-110">*String*</span></span>

<span data-ttu-id="5e76d-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="5e76d-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5e76d-112">例</span><span class="sxs-lookup"><span data-stu-id="5e76d-112">Example</span></span>

<span data-ttu-id="5e76d-113">`UPPER ("Sample")` は、**"SAMPLE"** を返します。</span><span class="sxs-lookup"><span data-stu-id="5e76d-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e76d-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5e76d-114">Additional resources</span></span>

[<span data-ttu-id="5e76d-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="5e76d-115">Text functions</span></span>](er-functions-category-text.md)
