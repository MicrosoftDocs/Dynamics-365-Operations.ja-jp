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
ms.openlocfilehash: 77854d645ba5b65a2819437af510fcd67be6d99d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040943"
---
# <span data-ttu-id="51387-103"><a name="UPPER">UPPER ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="51387-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51387-104">`UPPER` 関数は、大文字に変換した後の*文字列*値として指定されたテキスト返します。</span><span class="sxs-lookup"><span data-stu-id="51387-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="51387-105">構文</span><span class="sxs-lookup"><span data-stu-id="51387-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="51387-106">引数</span><span class="sxs-lookup"><span data-stu-id="51387-106">Arguments</span></span>

<span data-ttu-id="51387-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="51387-107">`text`: *String*</span></span>

<span data-ttu-id="51387-108">*文字列*型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="51387-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="51387-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="51387-109">Return values</span></span>

<span data-ttu-id="51387-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="51387-110">*String*</span></span>

<span data-ttu-id="51387-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="51387-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="51387-112">例</span><span class="sxs-lookup"><span data-stu-id="51387-112">Example</span></span>

<span data-ttu-id="51387-113">`UPPER ("Sample")` は、**"SAMPLE"** を返します。</span><span class="sxs-lookup"><span data-stu-id="51387-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51387-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="51387-114">Additional resources</span></span>

[<span data-ttu-id="51387-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="51387-115">Text functions</span></span>](er-functions-category-text.md)
