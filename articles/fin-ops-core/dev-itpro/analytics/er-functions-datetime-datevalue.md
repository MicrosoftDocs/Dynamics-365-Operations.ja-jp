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
ms.openlocfilehash: d760c3f874bfebad11b9497b136cb67df4e9ea61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746942"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="b80dd-103">DATEVALUE ER 関数</span><span class="sxs-lookup"><span data-stu-id="b80dd-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b80dd-104">`DATEVALUE` 関数は、指定された形式およびオプションで指定された [カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) の、特定のテキスト値から日付値に変換される *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="b80dd-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="b80dd-105">サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b80dd-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b80dd-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="b80dd-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="b80dd-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="b80dd-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="b80dd-108">引数</span><span class="sxs-lookup"><span data-stu-id="b80dd-108">Arguments</span></span>

<span data-ttu-id="b80dd-109">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="b80dd-109">`text`: *String*</span></span>

<span data-ttu-id="b80dd-110">書式設定する値を表すテキスト。</span><span class="sxs-lookup"><span data-stu-id="b80dd-110">Text that represents the value to format.</span></span>

<span data-ttu-id="b80dd-111">`format`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="b80dd-111">`format`: *String*</span></span>

<span data-ttu-id="b80dd-112">指定されたテキストの形式。</span><span class="sxs-lookup"><span data-stu-id="b80dd-112">The format of the given text.</span></span>

<span data-ttu-id="b80dd-113">`culture`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="b80dd-113">`culture`: *String*</span></span>

<span data-ttu-id="b80dd-114">指定されたテキストの書式設定に使用されるカルチャ。</span><span class="sxs-lookup"><span data-stu-id="b80dd-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b80dd-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="b80dd-115">Return values</span></span>

<span data-ttu-id="b80dd-116">*日付*</span><span class="sxs-lookup"><span data-stu-id="b80dd-116">*Date*</span></span>

<span data-ttu-id="b80dd-117">結果日付値。</span><span class="sxs-lookup"><span data-stu-id="b80dd-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b80dd-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="b80dd-118">Usage notes</span></span>

<span data-ttu-id="b80dd-119">呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="b80dd-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="b80dd-120">たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATEVALUE` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="b80dd-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="b80dd-121">既定の `culture` の値は **EN-US** です。</span><span class="sxs-lookup"><span data-stu-id="b80dd-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="b80dd-122">例 1</span><span class="sxs-lookup"><span data-stu-id="b80dd-122">Example 1</span></span>

<span data-ttu-id="b80dd-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")`は、指定されたカスタム形式と既定のアプリケーションの **EN-US** カルチャに基づいて、日付値 **2016 年 12 月 21 日** を返します。</span><span class="sxs-lookup"><span data-stu-id="b80dd-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="b80dd-124">例 2</span><span class="sxs-lookup"><span data-stu-id="b80dd-124">Example 2</span></span>

<span data-ttu-id="b80dd-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` は、指定されたカスタム形式とカルチャに基づいて、日付値 **2016 年 1 月 21 日** を返します。</span><span class="sxs-lookup"><span data-stu-id="b80dd-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="b80dd-126">ただし、`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` は、指定した文字列が、指定したカルチャに対する有効な日付として認識されていないことをユーザーに通知するための例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="b80dd-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b80dd-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b80dd-127">Additional resources</span></span>

[<span data-ttu-id="b80dd-128">日時の関数</span><span class="sxs-lookup"><span data-stu-id="b80dd-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]