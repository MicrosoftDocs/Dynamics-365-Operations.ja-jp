---
title: CONVERTCURRENCY ER 関数
description: このトピックでは、CONVERTCURRENCY 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: bf972c6c2cc798811a9fb3bd3a355ac6ffca5a60
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915950"
---
# <span data-ttu-id="a5f4d-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="a5f4d-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5f4d-104">`CONVERTCURRENCY` 関数は、特定の日付で指定された会社の設定を使用して、指定された換算元の通貨から指定された換算先の通貨に指定された金額を変換した結果を表す、*実数*値を返します。</span><span class="sxs-lookup"><span data-stu-id="a5f4d-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f4d-105">構文</span><span class="sxs-lookup"><span data-stu-id="a5f4d-105">Syntax</span></span>

```
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="a5f4d-106">引数</span><span class="sxs-lookup"><span data-stu-id="a5f4d-106">Arguments</span></span>

<span data-ttu-id="a5f4d-107">`amount`: *整数*または*実数*</span><span class="sxs-lookup"><span data-stu-id="a5f4d-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="a5f4d-108">変換が必要な金額を表す数値。</span><span class="sxs-lookup"><span data-stu-id="a5f4d-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="a5f4d-109">`source currency`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="a5f4d-109">`source currency`: *String*</span></span>

<span data-ttu-id="a5f4d-110">換算元の通貨のコード</span><span class="sxs-lookup"><span data-stu-id="a5f4d-110">The code of the source currency.</span></span>

<span data-ttu-id="a5f4d-111">`target currency`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="a5f4d-111">`target currency`: *String*</span></span>

<span data-ttu-id="a5f4d-112">換算先の通貨のコード</span><span class="sxs-lookup"><span data-stu-id="a5f4d-112">The code of the target currency.</span></span>

<span data-ttu-id="a5f4d-113">`date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="a5f4d-113">`date`: *Date*</span></span>

<span data-ttu-id="a5f4d-114">変換の為替レートを決定するために使用される日付を表す*日付*値。</span><span class="sxs-lookup"><span data-stu-id="a5f4d-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="a5f4d-115">`company`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="a5f4d-115">`company`: *String*</span></span>

<span data-ttu-id="a5f4d-116">変換に使用される設定を提供する会社のコードを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="a5f4d-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="a5f4d-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="a5f4d-117">Return values</span></span>

<span data-ttu-id="a5f4d-118">*実績*</span><span class="sxs-lookup"><span data-stu-id="a5f4d-118">*Real*</span></span>

<span data-ttu-id="a5f4d-119">結果数値。</span><span class="sxs-lookup"><span data-stu-id="a5f4d-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="a5f4d-120">例</span><span class="sxs-lookup"><span data-stu-id="a5f4d-120">Example</span></span>

<span data-ttu-id="a5f4d-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` は、**DEMF** 会社の設定に基づいて現在のセッションの日付の 1 ユーロに相当する額を米ドルで返します。</span><span class="sxs-lookup"><span data-stu-id="a5f4d-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5f4d-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a5f4d-122">Additional resources</span></span>

[<span data-ttu-id="a5f4d-123">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="a5f4d-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)