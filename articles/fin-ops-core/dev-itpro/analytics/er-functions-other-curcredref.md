---
title: CURCREDREF ER 関数
description: このトピックでは、CURCREDREF 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d5f126d71abdc9e3e488b4e8476850dc7763fe5a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567619"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="9acf8-103">CURCREDREF ER 関数</span><span class="sxs-lookup"><span data-stu-id="9acf8-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9acf8-104">この `CURCREDREF` 関数は、指定された請求書番号の桁数に基づいて、債権者参照を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="9acf8-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9acf8-105">構文</span><span class="sxs-lookup"><span data-stu-id="9acf8-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="9acf8-106">引数</span><span class="sxs-lookup"><span data-stu-id="9acf8-106">Arguments</span></span>

<span data-ttu-id="9acf8-107">`invoice number digits`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="9acf8-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="9acf8-108">請求書番号の桁数を表すテキスト値。</span><span class="sxs-lookup"><span data-stu-id="9acf8-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="9acf8-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="9acf8-109">Return values</span></span>

<span data-ttu-id="9acf8-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9acf8-110">*String*</span></span>

<span data-ttu-id="9acf8-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="9acf8-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9acf8-112">例</span><span class="sxs-lookup"><span data-stu-id="9acf8-112">Example</span></span>

<span data-ttu-id="9acf8-113">`CURCredRef ("VEND-200002")` は、**"2200002"** を返します。</span><span class="sxs-lookup"><span data-stu-id="9acf8-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9acf8-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9acf8-114">Additional resources</span></span>

[<span data-ttu-id="9acf8-115">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="9acf8-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]