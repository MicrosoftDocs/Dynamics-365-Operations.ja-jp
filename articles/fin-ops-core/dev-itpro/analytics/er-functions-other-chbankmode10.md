---
title: CH_BANK_MOD_10 ER 関数
description: このトピックでは、CH_BANK_MOD_10 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: c18a7f96096fbc6bbc7b6d15135c11bd70960d26
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744473"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="d492e-103">CH_BANK_MOD_10 ER 関数</span><span class="sxs-lookup"><span data-stu-id="d492e-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d492e-104">`CH_BANK_MOD_10` 関数は、指定された請求書番号の桁数に基づいて、MOD10 式として債権者参照を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="d492e-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d492e-105">構文</span><span class="sxs-lookup"><span data-stu-id="d492e-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="d492e-106">引数</span><span class="sxs-lookup"><span data-stu-id="d492e-106">Arguments</span></span>

<span data-ttu-id="d492e-107">`invoice number digits`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="d492e-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="d492e-108">請求書番号の桁数を表すテキスト値。</span><span class="sxs-lookup"><span data-stu-id="d492e-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="d492e-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="d492e-109">Return values</span></span>

<span data-ttu-id="d492e-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="d492e-110">*String*</span></span>

<span data-ttu-id="d492e-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="d492e-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d492e-112">例</span><span class="sxs-lookup"><span data-stu-id="d492e-112">Example</span></span>

<span data-ttu-id="d492e-113">`CH_BANK_MOD_10 ("VEND-200002")` は、**3** を返します。</span><span class="sxs-lookup"><span data-stu-id="d492e-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d492e-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d492e-114">Additional resources</span></span>

[<span data-ttu-id="d492e-115">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="d492e-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
