---
title: TEXT ER 関数
description: このトピックでは、TEXT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560064"
---
# <a name="text-er-function"></a><span data-ttu-id="6ef51-103">TEXT ER 関数</span><span class="sxs-lookup"><span data-stu-id="6ef51-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ef51-104">`TEXT` 関数は、現在のアプリケーション インスタンス のサーバー ロケール設定に従って、書式設定されるテキスト文字列に変換した後に、*文字列* 値として指定された数を返します。</span><span class="sxs-lookup"><span data-stu-id="6ef51-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef51-105">構文</span><span class="sxs-lookup"><span data-stu-id="6ef51-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="6ef51-106">引数</span><span class="sxs-lookup"><span data-stu-id="6ef51-106">Arguments</span></span>

<span data-ttu-id="6ef51-107">`number`: *整数* または *実数*</span><span class="sxs-lookup"><span data-stu-id="6ef51-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="6ef51-108">テキスト文字列に変換する必要がある番号。</span><span class="sxs-lookup"><span data-stu-id="6ef51-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ef51-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="6ef51-109">Return values</span></span>

<span data-ttu-id="6ef51-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="6ef51-110">*String*</span></span>

<span data-ttu-id="6ef51-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="6ef51-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6ef51-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="6ef51-112">Usage notes</span></span>

<span data-ttu-id="6ef51-113">*実数* 型の値では、文字列変換が小数点第 2 位に制限されます。</span><span class="sxs-lookup"><span data-stu-id="6ef51-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="6ef51-114">例</span><span class="sxs-lookup"><span data-stu-id="6ef51-114">Example</span></span>

<span data-ttu-id="6ef51-115">Microsoft Dynamics 365 Finance インスタンスのサーバー ロケールが **EN-US** で定義されている場合、`TEXT (NOW ())` は現在の財務セッション日付、2015 年 12 月 17 日、をテキスト文字列 **"12/17/2015 07:59:23 AM"** として返します。</span><span class="sxs-lookup"><span data-stu-id="6ef51-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="6ef51-116">`TEXT (1/3)` は、**"0.33"** を返します。</span><span class="sxs-lookup"><span data-stu-id="6ef51-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ef51-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6ef51-117">Additional resources</span></span>

[<span data-ttu-id="6ef51-118">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="6ef51-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]