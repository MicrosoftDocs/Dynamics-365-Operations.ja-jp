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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a27fd30236a61576ab9063010ea6bc38d9cf7a1e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686789"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="25dea-103">CONVERTCURRENCY ER 関数</span><span class="sxs-lookup"><span data-stu-id="25dea-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25dea-104">`CONVERTCURRENCY` 関数は、特定の日付で指定された会社の設定を使用して、指定された換算元の通貨から指定された換算先の通貨に指定された金額を変換した結果を表す、*実数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="25dea-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="25dea-105">構文</span><span class="sxs-lookup"><span data-stu-id="25dea-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="25dea-106">引数</span><span class="sxs-lookup"><span data-stu-id="25dea-106">Arguments</span></span>

<span data-ttu-id="25dea-107">`amount`: *整数* または *実数*</span><span class="sxs-lookup"><span data-stu-id="25dea-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="25dea-108">変換が必要な金額を表す数値。</span><span class="sxs-lookup"><span data-stu-id="25dea-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="25dea-109">`source currency`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="25dea-109">`source currency`: *String*</span></span>

<span data-ttu-id="25dea-110">換算元の通貨のコード</span><span class="sxs-lookup"><span data-stu-id="25dea-110">The code of the source currency.</span></span>

<span data-ttu-id="25dea-111">`target currency`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="25dea-111">`target currency`: *String*</span></span>

<span data-ttu-id="25dea-112">換算先の通貨のコード</span><span class="sxs-lookup"><span data-stu-id="25dea-112">The code of the target currency.</span></span>

<span data-ttu-id="25dea-113">`date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="25dea-113">`date`: *Date*</span></span>

<span data-ttu-id="25dea-114">変換の為替レートを決定するために使用される日付を表す *日付* 値。</span><span class="sxs-lookup"><span data-stu-id="25dea-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="25dea-115">`company`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="25dea-115">`company`: *String*</span></span>

<span data-ttu-id="25dea-116">変換に使用される設定を提供する会社のコードを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="25dea-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="25dea-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="25dea-117">Return values</span></span>

<span data-ttu-id="25dea-118">*実績*</span><span class="sxs-lookup"><span data-stu-id="25dea-118">*Real*</span></span>

<span data-ttu-id="25dea-119">結果数値。</span><span class="sxs-lookup"><span data-stu-id="25dea-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="25dea-120">例</span><span class="sxs-lookup"><span data-stu-id="25dea-120">Example</span></span>

<span data-ttu-id="25dea-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` は、**DEMF** 会社の設定に基づいて現在のセッションの日付の 1 ユーロに相当する額を米ドルで返します。</span><span class="sxs-lookup"><span data-stu-id="25dea-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25dea-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="25dea-122">Additional resources</span></span>

[<span data-ttu-id="25dea-123">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="25dea-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
