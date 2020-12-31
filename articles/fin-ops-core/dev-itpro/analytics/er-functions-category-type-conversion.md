---
title: 型変換カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされる型変換関数について説明します。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d160c02403bf067ed523fbd634e65c622b522b97
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686078"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="7365b-103">型変換カテゴリ内の ER 関数のリスト</span><span class="sxs-lookup"><span data-stu-id="7365b-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7365b-104">電子レポート (ER) 型変換関数を使用して、タイプ間で値を変換できます。</span><span class="sxs-lookup"><span data-stu-id="7365b-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="7365b-105">このトピックでは、これらの関数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="7365b-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="7365b-106">型変換関数</span><span class="sxs-lookup"><span data-stu-id="7365b-106">Type conversion functions</span></span>

| <span data-ttu-id="7365b-107">職務</span><span class="sxs-lookup"><span data-stu-id="7365b-107">Function</span></span> | <span data-ttu-id="7365b-108">説明</span><span class="sxs-lookup"><span data-stu-id="7365b-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7365b-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="7365b-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="7365b-110">この関数は、指定された文字列を表す *Int64* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="7365b-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="7365b-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="7365b-112">この関数は、指定された文字列を表す *Int* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="7365b-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="7365b-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="7365b-114">この関数は、指定された *文字列* 値から変換された *実数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="7365b-115">変換時に、指定された 10 進と桁区切り記号が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="7365b-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="7365b-116">金額</span><span class="sxs-lookup"><span data-stu-id="7365b-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="7365b-117">この関数は、指定された *文字列* 値から変換された *実数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="7365b-118">日付と時刻のカテゴリ内の型変換関数のリスト</span><span class="sxs-lookup"><span data-stu-id="7365b-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="7365b-119">次の表では、[日付と時刻のカテゴリ](er-functions-category-datetime.md) における型変換関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="7365b-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="7365b-120">職務</span><span class="sxs-lookup"><span data-stu-id="7365b-120">Function</span></span> | <span data-ttu-id="7365b-121">説明</span><span class="sxs-lookup"><span data-stu-id="7365b-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7365b-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="7365b-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="7365b-123">この関数は、指定された形式およびオプションで指定されたカルチャの特定の *文字列* 値から、日付/時刻値に変換される *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="7365b-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="7365b-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="7365b-125">この関数は、特定の *日付* 値から協定世界時 (グリニッジ標準時 \[GMT\]) の日付/時刻値に変換された *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="7365b-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="7365b-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="7365b-127">この関数は、指定された形式およびオプションで指定されたカルチャの特定の *文字列* 値から、日付値に変換される *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="7365b-128">リスト カテゴリ内の型変換関数</span><span class="sxs-lookup"><span data-stu-id="7365b-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="7365b-129">次の表では、[リスト カテゴリ](er-functions-category-list.md) における型変換関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="7365b-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="7365b-130">職務</span><span class="sxs-lookup"><span data-stu-id="7365b-130">Function</span></span> | <span data-ttu-id="7365b-131">説明</span><span class="sxs-lookup"><span data-stu-id="7365b-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7365b-132">リスト</span><span class="sxs-lookup"><span data-stu-id="7365b-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="7365b-133">この関数は、*コンテナー (レコード)* タイプの指定された引数から作成された新しいリストとして *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="7365b-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="7365b-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="7365b-135">この関数は、*列挙* または *コンテナー (レコード)* タイプの特定の引数の構造に基づいて作成された *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="7365b-136">分割</span><span class="sxs-lookup"><span data-stu-id="7365b-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="7365b-137">この関数は、指定された *文字列* 値をサブ文字列に分割し、新しい *レコード リスト* 値として結果を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="7365b-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="7365b-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="7365b-139">この関数は、指定された *レコード リスト* 値から指定したフィールドの連結された値で構成される *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="7365b-140">値は、指定した区切り記号で区切ることができます。</span><span class="sxs-lookup"><span data-stu-id="7365b-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="7365b-141">テキスト カテゴリ内の型変換関数</span><span class="sxs-lookup"><span data-stu-id="7365b-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="7365b-142">次の表では、[テキスト カテゴリ](er-functions-category-text.md) における型変換関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="7365b-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="7365b-143">職務</span><span class="sxs-lookup"><span data-stu-id="7365b-143">Function</span></span> | <span data-ttu-id="7365b-144">説明</span><span class="sxs-lookup"><span data-stu-id="7365b-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7365b-145">Char</span><span class="sxs-lookup"><span data-stu-id="7365b-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="7365b-146">この関数は、指定された Unicode 番号で参照される単一文字を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="7365b-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="7365b-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="7365b-148">この関数は、指定された *文字列* 型の入力を *GUID* 型のデータ品目に変換します。</span><span class="sxs-lookup"><span data-stu-id="7365b-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="7365b-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="7365b-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="7365b-150">この関数は、指定された形式およびオプションで指定されたカルチャで指定された数を表す、*文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="7365b-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="7365b-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="7365b-152">この関数は、バイナリ形式の指定された文字列に対して、クイック応答コード (QR コード) イメージを表示する *コンテナー* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="7365b-153">テキスト</span><span class="sxs-lookup"><span data-stu-id="7365b-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="7365b-154">この関数は、現在のアプリケーション インスタンスのサーバー ロケール設定に従って書式設定されるテキスト文字列に変換した後に、指定された数を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7365b-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7365b-155">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7365b-155">Additional resources</span></span>

[<span data-ttu-id="7365b-156">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="7365b-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7365b-157">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="7365b-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="7365b-158">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="7365b-158">Electronic reporting formula language</span></span>](er-formula-language.md)
