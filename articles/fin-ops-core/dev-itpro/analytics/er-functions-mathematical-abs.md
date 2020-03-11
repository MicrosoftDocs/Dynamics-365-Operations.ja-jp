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
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041656"
---
# <span data-ttu-id="b5c44-103"><a name="ABS">ABS ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="b5c44-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5c44-104">`ABS` 関数は、指定された数の絶対値 (係数) を*実数*値として返します。</span><span class="sxs-lookup"><span data-stu-id="b5c44-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="b5c44-105">つまり、符号のない数値を返します。</span><span class="sxs-lookup"><span data-stu-id="b5c44-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c44-106">構文</span><span class="sxs-lookup"><span data-stu-id="b5c44-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="b5c44-107">引数</span><span class="sxs-lookup"><span data-stu-id="b5c44-107">Arguments</span></span>

<span data-ttu-id="b5c44-108">`number`: *実数*</span><span class="sxs-lookup"><span data-stu-id="b5c44-108">`number`: *Real*</span></span>

<span data-ttu-id="b5c44-109">係数を求める数値。</span><span class="sxs-lookup"><span data-stu-id="b5c44-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="b5c44-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="b5c44-110">Return values</span></span>

<span data-ttu-id="b5c44-111">*実績*</span><span class="sxs-lookup"><span data-stu-id="b5c44-111">*Real*</span></span>

<span data-ttu-id="b5c44-112">結果数値。</span><span class="sxs-lookup"><span data-stu-id="b5c44-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="b5c44-113">例</span><span class="sxs-lookup"><span data-stu-id="b5c44-113">Example</span></span>

<span data-ttu-id="b5c44-114">`ABS (-1)` は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="b5c44-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5c44-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b5c44-115">Additional resources</span></span>

[<span data-ttu-id="b5c44-116">算術関数</span><span class="sxs-lookup"><span data-stu-id="b5c44-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
