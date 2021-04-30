---
title: DATEVALUE ER 関数
description: このトピックでは、DATEVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: cfaf183c61d3663442cbc244239b872b9e1957bb
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891236"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="6aadd-103">DATEVALUE ER 関数</span><span class="sxs-lookup"><span data-stu-id="6aadd-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6aadd-104">`DATEVALUE` 関数は、指定された形式およびオプションで指定された [カルチャ](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) の、特定のテキスト値から日付値に変換される *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="6aadd-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="6aadd-105">サポートされている形式の詳細については、[標準](/dotnet/standard/base-types/standard-date-and-time-format-strings) と [カスタム](/dotnet/standard/base-types/custom-date-and-time-format-strings) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6aadd-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="6aadd-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="6aadd-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="6aadd-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="6aadd-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="6aadd-108">引数</span><span class="sxs-lookup"><span data-stu-id="6aadd-108">Arguments</span></span>

<span data-ttu-id="6aadd-109">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="6aadd-109">`text`: *String*</span></span>

<span data-ttu-id="6aadd-110">書式設定する値を表すテキスト。</span><span class="sxs-lookup"><span data-stu-id="6aadd-110">Text that represents the value to format.</span></span>

<span data-ttu-id="6aadd-111">`format`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="6aadd-111">`format`: *String*</span></span>

<span data-ttu-id="6aadd-112">指定されたテキストの形式。</span><span class="sxs-lookup"><span data-stu-id="6aadd-112">The format of the given text.</span></span>

<span data-ttu-id="6aadd-113">`culture`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="6aadd-113">`culture`: *String*</span></span>

<span data-ttu-id="6aadd-114">指定されたテキストの書式設定に使用されるカルチャ。</span><span class="sxs-lookup"><span data-stu-id="6aadd-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="6aadd-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="6aadd-115">Return values</span></span>

<span data-ttu-id="6aadd-116">*日付*</span><span class="sxs-lookup"><span data-stu-id="6aadd-116">*Date*</span></span>

<span data-ttu-id="6aadd-117">結果日付値。</span><span class="sxs-lookup"><span data-stu-id="6aadd-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6aadd-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="6aadd-118">Usage notes</span></span>

<span data-ttu-id="6aadd-119">呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="6aadd-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="6aadd-120">たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATEVALUE` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="6aadd-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="6aadd-121">既定の `culture` の値は **EN-US** です。</span><span class="sxs-lookup"><span data-stu-id="6aadd-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="6aadd-122">例 1</span><span class="sxs-lookup"><span data-stu-id="6aadd-122">Example 1</span></span>

<span data-ttu-id="6aadd-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")`は、指定されたカスタム形式と既定のアプリケーションの **EN-US** カルチャに基づいて、日付値 **2016 年 12 月 21 日** を返します。</span><span class="sxs-lookup"><span data-stu-id="6aadd-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="6aadd-124">例 2</span><span class="sxs-lookup"><span data-stu-id="6aadd-124">Example 2</span></span>

<span data-ttu-id="6aadd-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` は、指定されたカスタム形式とカルチャに基づいて、日付値 **2016 年 1 月 21 日** を返します。</span><span class="sxs-lookup"><span data-stu-id="6aadd-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="6aadd-126">ただし、`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` は、指定した文字列が、指定したカルチャに対する有効な日付として認識されていないことをユーザーに通知するための例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="6aadd-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6aadd-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6aadd-127">Additional resources</span></span>

[<span data-ttu-id="6aadd-128">日時の関数</span><span class="sxs-lookup"><span data-stu-id="6aadd-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]