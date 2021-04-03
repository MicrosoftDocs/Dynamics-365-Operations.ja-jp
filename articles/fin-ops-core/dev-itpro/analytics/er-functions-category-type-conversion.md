---
title: 型変換カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされる型変換関数について説明します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 5613496d3131ccd39b198cac214eb791a6d07355
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561521"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="15fe0-103">型変換カテゴリ内の ER 関数のリスト</span><span class="sxs-lookup"><span data-stu-id="15fe0-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15fe0-104">電子レポート (ER) 型変換関数を使用して、タイプ間で値を変換できます。</span><span class="sxs-lookup"><span data-stu-id="15fe0-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="15fe0-105">このトピックでは、これらの関数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="15fe0-106">型変換関数</span><span class="sxs-lookup"><span data-stu-id="15fe0-106">Type conversion functions</span></span>

| <span data-ttu-id="15fe0-107">職務</span><span class="sxs-lookup"><span data-stu-id="15fe0-107">Function</span></span> | <span data-ttu-id="15fe0-108">説明</span><span class="sxs-lookup"><span data-stu-id="15fe0-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="15fe0-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="15fe0-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="15fe0-110">この関数は、指定された文字列を表す *Int64* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="15fe0-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="15fe0-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="15fe0-112">この関数は、指定された文字列を表す *Int* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="15fe0-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="15fe0-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="15fe0-114">この関数は、指定された *文字列* 値から変換された *実数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="15fe0-115">変換時に、指定された 10 進と桁区切り記号が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="15fe0-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="15fe0-116">金額</span><span class="sxs-lookup"><span data-stu-id="15fe0-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="15fe0-117">この関数は、指定された *文字列* 値から変換された *実数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="15fe0-118">コンテナー カテゴリ内の型変換関数</span><span class="sxs-lookup"><span data-stu-id="15fe0-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="15fe0-119">次の表では、[コンテナー](er-functions-category-container.md) カテゴリにおける型変換関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="15fe0-120">関数</span><span class="sxs-lookup"><span data-stu-id="15fe0-120">Function</span></span> | <span data-ttu-id="15fe0-121">説明</span><span class="sxs-lookup"><span data-stu-id="15fe0-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="15fe0-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="15fe0-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="15fe0-123">この関数は、指定された *文字列* 型の入力を *コンテナー* 型のデータ項目に変換します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="15fe0-124">日付と時刻のカテゴリ内の型変換関数のリスト</span><span class="sxs-lookup"><span data-stu-id="15fe0-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="15fe0-125">次の表では、[日付と時刻のカテゴリ](er-functions-category-datetime.md) における型変換関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="15fe0-126">職務</span><span class="sxs-lookup"><span data-stu-id="15fe0-126">Function</span></span> | <span data-ttu-id="15fe0-127">説明</span><span class="sxs-lookup"><span data-stu-id="15fe0-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="15fe0-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="15fe0-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="15fe0-129">この関数は、指定された形式およびオプションで指定されたカルチャの特定の *文字列* 値から、日付/時刻値に変換される *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="15fe0-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="15fe0-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="15fe0-131">この関数は、特定の *日付* 値から協定世界時 (グリニッジ標準時 \[GMT\]) の日付/時刻値に変換された *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="15fe0-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="15fe0-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="15fe0-133">この関数は、指定された形式およびオプションで指定されたカルチャの特定の *文字列* 値から、日付値に変換される *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="15fe0-134">リスト カテゴリ内の型変換関数</span><span class="sxs-lookup"><span data-stu-id="15fe0-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="15fe0-135">次の表では、[リスト カテゴリ](er-functions-category-list.md) における型変換関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="15fe0-136">職務</span><span class="sxs-lookup"><span data-stu-id="15fe0-136">Function</span></span> | <span data-ttu-id="15fe0-137">説明</span><span class="sxs-lookup"><span data-stu-id="15fe0-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="15fe0-138">リスト</span><span class="sxs-lookup"><span data-stu-id="15fe0-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="15fe0-139">この関数は、*コンテナー (レコード)* タイプの指定された引数から作成された新しいリストとして *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="15fe0-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="15fe0-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="15fe0-141">この関数は、*列挙* または *コンテナー (レコード)* タイプの特定の引数の構造に基づいて作成された *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="15fe0-142">分割</span><span class="sxs-lookup"><span data-stu-id="15fe0-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="15fe0-143">この関数は、指定された *文字列* 値をサブ文字列に分割し、新しい *レコード リスト* 値として結果を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="15fe0-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="15fe0-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="15fe0-145">この関数は、指定された *レコード リスト* 値から指定したフィールドの連結された値で構成される *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="15fe0-146">値は、指定した区切り記号で区切ることができます。</span><span class="sxs-lookup"><span data-stu-id="15fe0-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="15fe0-147">テキスト カテゴリ内の型変換関数</span><span class="sxs-lookup"><span data-stu-id="15fe0-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="15fe0-148">次の表では、[テキスト カテゴリ](er-functions-category-text.md) における型変換関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="15fe0-149">職務</span><span class="sxs-lookup"><span data-stu-id="15fe0-149">Function</span></span> | <span data-ttu-id="15fe0-150">説明</span><span class="sxs-lookup"><span data-stu-id="15fe0-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="15fe0-151">Char</span><span class="sxs-lookup"><span data-stu-id="15fe0-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="15fe0-152">この関数は、指定された Unicode 番号で参照される単一文字を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="15fe0-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="15fe0-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="15fe0-154">この関数は、指定された *文字列* 型の入力を *GUID* 型のデータ品目に変換します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="15fe0-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="15fe0-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="15fe0-156">この関数は、指定された形式およびオプションで指定されたカルチャで指定された数を表す、*文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="15fe0-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="15fe0-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="15fe0-158">この関数は、バイナリ形式の指定された文字列に対して、クイック応答コード (QR コード) イメージを表示する *コンテナー* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="15fe0-159">テキスト</span><span class="sxs-lookup"><span data-stu-id="15fe0-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="15fe0-160">この関数は、現在のアプリケーション インスタンスのサーバー ロケール設定に従って書式設定されるテキスト文字列に変換した後に、指定された数を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="15fe0-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="15fe0-161">追加リソース</span><span class="sxs-lookup"><span data-stu-id="15fe0-161">Additional resources</span></span>

[<span data-ttu-id="15fe0-162">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="15fe0-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="15fe0-163">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="15fe0-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="15fe0-164">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="15fe0-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]