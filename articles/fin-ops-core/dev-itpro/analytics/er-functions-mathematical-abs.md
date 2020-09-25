---
title: ABS ER 関数
description: このトピックでは、ABS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: b53535d1a000b72577be5c6284cc4676c43d591b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744602"
---
# <a name="abs-er-function"></a><span data-ttu-id="25dce-103">ABS ER 関数</span><span class="sxs-lookup"><span data-stu-id="25dce-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25dce-104">`ABS` 関数は、指定された数の絶対値 (係数) を*実数*値として返します。</span><span class="sxs-lookup"><span data-stu-id="25dce-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="25dce-105">つまり、符号のない数値を返します。</span><span class="sxs-lookup"><span data-stu-id="25dce-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="25dce-106">構文</span><span class="sxs-lookup"><span data-stu-id="25dce-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="25dce-107">引数</span><span class="sxs-lookup"><span data-stu-id="25dce-107">Arguments</span></span>

<span data-ttu-id="25dce-108">`number`: *実数*</span><span class="sxs-lookup"><span data-stu-id="25dce-108">`number`: *Real*</span></span>

<span data-ttu-id="25dce-109">係数を求める数値。</span><span class="sxs-lookup"><span data-stu-id="25dce-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="25dce-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="25dce-110">Return values</span></span>

<span data-ttu-id="25dce-111">*実績*</span><span class="sxs-lookup"><span data-stu-id="25dce-111">*Real*</span></span>

<span data-ttu-id="25dce-112">結果数値。</span><span class="sxs-lookup"><span data-stu-id="25dce-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="25dce-113">例</span><span class="sxs-lookup"><span data-stu-id="25dce-113">Example</span></span>

<span data-ttu-id="25dce-114">`ABS (-1)` は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="25dce-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25dce-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="25dce-115">Additional resources</span></span>

[<span data-ttu-id="25dce-116">算術関数</span><span class="sxs-lookup"><span data-stu-id="25dce-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
