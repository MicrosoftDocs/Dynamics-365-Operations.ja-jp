---
title: テキスト カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされるテキスト関数について説明します。
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: bd4dd7e9a3e1aa448adea5abd0c21b8133f34e3b
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201092"
---
# <a name="list-of-er-functions-of-the-text-category"></a><span data-ttu-id="5b019-103">テキスト カテゴリ内の ER 関数のリスト</span><span class="sxs-lookup"><span data-stu-id="5b019-103">List of ER functions of the text category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b019-104">電子申告 (ER) テキスト関数を使用して、*文字列*データ タイプのデータ ソースで操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5b019-104">Electronic reporting (ER) text functions can be used to perform operations on data sources of the *String* data type.</span></span> <span data-ttu-id="5b019-105">このトピックでは、これらの関数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="5b019-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="5b019-106">サポートされている関数のリスト</span><span class="sxs-lookup"><span data-stu-id="5b019-106">List of supported functions</span></span>

| <span data-ttu-id="5b019-107">職務</span><span class="sxs-lookup"><span data-stu-id="5b019-107">Function</span></span> | <span data-ttu-id="5b019-108">説明</span><span class="sxs-lookup"><span data-stu-id="5b019-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="5b019-109">Char</span><span class="sxs-lookup"><span data-stu-id="5b019-109">Char</span></span>](er-functions-text-char.md) | <span data-ttu-id="5b019-110">この関数は、指定された Unicode 番号で参照される単一の文字を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-110">This function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="5b019-111">連結</span><span class="sxs-lookup"><span data-stu-id="5b019-111">Concatenate</span></span>](er-functions-text-concatenate.md) | <span data-ttu-id="5b019-112">この関数は、1 つの文字列に結合された後、*文字列*値として指定されたすべてのテキスト文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-112">This function returns  all the specified text strings as a *String* value after they have been joined into one string.</span></span> |
| [<span data-ttu-id="5b019-113">形式</span><span class="sxs-lookup"><span data-stu-id="5b019-113">Format</span></span>](er-functions-text-format.md) | <span data-ttu-id="5b019-114">この関数は、*N* 番目の引数で **%N** の出現を置き換えることで書式設定した後に、*文字列*値として指定された文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-114">This function returns the specified string a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span> |
| [<span data-ttu-id="5b019-115">GetEnumValueByName</span><span class="sxs-lookup"><span data-stu-id="5b019-115">GetEnumValueByName</span></span>](er-functions-text-getenumvaluebyname.md) | <span data-ttu-id="5b019-116">この関数は、*文字列*値として指定された列挙名を使用して、指定された列挙データソースの特定の*列挙*値を検索します。</span><span class="sxs-lookup"><span data-stu-id="5b019-116">This function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="5b019-117">*列挙*値が見つかった場合、関数によって返されます。</span><span class="sxs-lookup"><span data-stu-id="5b019-117">If the *Enum* value is found, the function returns it.</span></span> |
| [<span data-ttu-id="5b019-118">GuidValue</span><span class="sxs-lookup"><span data-stu-id="5b019-118">GuidValue</span></span>](er-functions-text-guidvalue.md) | <span data-ttu-id="5b019-119">この関数は、指定された*文字列*型の入力を *GUID* 型のデータ品目に変換します。</span><span class="sxs-lookup"><span data-stu-id="5b019-119">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="5b019-120">JsonValue</span><span class="sxs-lookup"><span data-stu-id="5b019-120">JsonValue</span></span>](er-functions-text-jsonvalue.md) | <span data-ttu-id="5b019-121">この関数は指定した ID に基づくスカラー値を抽出し、指定したパスでアクセスする JavaScript Object Notation (JSON) 形式で、データを解析します。</span><span class="sxs-lookup"><span data-stu-id="5b019-121">This function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that is based on the specified ID.</span></span> <span data-ttu-id="5b019-122">次に、抽出したスカラー値を*文字列*値として返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-122">It then returns the extracted scalar value as a *String* value.</span></span> |
| [<span data-ttu-id="5b019-123">左</span><span class="sxs-lookup"><span data-stu-id="5b019-123">Left</span></span>](er-functions-text-left.md) | <span data-ttu-id="5b019-124">この関数は、指定された文字列の冒頭から指定された数の文字を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-124">This function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span> |
| [<span data-ttu-id="5b019-125">Len</span><span class="sxs-lookup"><span data-stu-id="5b019-125">Len</span></span>](er-functions-text-len.md) | <span data-ttu-id="5b019-126">この関数は、指定された文字列の文字数を表す*整数*値を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-126">This function returns an *Integer* value that presents the number of characters in the specified string.</span></span> |
| [<span data-ttu-id="5b019-127">Lower</span><span class="sxs-lookup"><span data-stu-id="5b019-127">Lower</span></span>](er-functions-text-lower.md) | <span data-ttu-id="5b019-128">この関数は、小文字に変換した後の*文字列*値として指定されたテキスト返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-128">This function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span> |
| [<span data-ttu-id="5b019-129">Mid</span><span class="sxs-lookup"><span data-stu-id="5b019-129">Mid</span></span>](er-functions-text-mid.md) | <span data-ttu-id="5b019-130">この関数は、指定された位置から始まる指定された文字列から、指定された数の文字を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-130">This function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span> |
| [<span data-ttu-id="5b019-131">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="5b019-131">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="5b019-132">この関数は、指定された形式およびオプションで指定されたカルチャで指定された数を表す、*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-132">This function returns a *String* value that presents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="5b019-133">NumeralsToText</span><span class="sxs-lookup"><span data-stu-id="5b019-133">NumeralsToText</span></span>](er-functions-text-numeralstotext.md) | <span data-ttu-id="5b019-134">この関数は、指定された言語で綴らた (つまり、テキスト文字列に変換された) 後、*文字列*値として指定された数を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-134">This function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span> |
| [<span data-ttu-id="5b019-135">PadLeft</span><span class="sxs-lookup"><span data-stu-id="5b019-135">PadLeft</span></span>](er-functions-text-padleft.md) | <span data-ttu-id="5b019-136">この関数は、指定された長さの*文字列*値を返します。指定された文字列の先頭には、指定された文字のインスタンスが 1 つ以上パディングされます。</span><span class="sxs-lookup"><span data-stu-id="5b019-136">This function returns a *String* value of the specified length, where the start of the specified string is padded with one or more instances of the specified characters.</span></span> |
| [<span data-ttu-id="5b019-137">QrCode</span><span class="sxs-lookup"><span data-stu-id="5b019-137">QrCode</span></span>](er-functions-text-qrcode.md) | <span data-ttu-id="5b019-138">この関数は、バイナリ形式の指定された文字列に対して、クイック応答コード (QR コード) イメージを表示する*コンテナー*値を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-138">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="5b019-139">置換</span><span class="sxs-lookup"><span data-stu-id="5b019-139">Replace</span></span>](er-functions-text-replace.md) | <span data-ttu-id="5b019-140">この関数は、すべてまたはその一部が別の文字列に置換した後、*文字列*値として指定されたテキストの文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-140">This function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span> |
| [<span data-ttu-id="5b019-141">右</span><span class="sxs-lookup"><span data-stu-id="5b019-141">Right</span></span>](er-functions-text-right.md) | <span data-ttu-id="5b019-142">この関数は、指定された文字列の末尾から指定された数の文字を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-142">This function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span> |
| [<span data-ttu-id="5b019-143">テキスト</span><span class="sxs-lookup"><span data-stu-id="5b019-143">Text</span></span>](er-functions-text-text.md) | <span data-ttu-id="5b019-144">この関数は、現在のアプリケーション インスタンス のサーバー ロケール設定に従って書式設定されるテキスト文字列に変換した後に、*文字列*値として指定された数を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-144">This function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |
| [<span data-ttu-id="5b019-145">翻訳</span><span class="sxs-lookup"><span data-stu-id="5b019-145">Translate</span></span>](er-functions-text-translate.md) | <span data-ttu-id="5b019-146">この関数は、指定したテキストを別の提供された文字セットに置換した結果を含む *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-146">This function returns a *String* value that contains the result of the replacement the specified text in characters for another provided set of characters.</span></span> |
| [<span data-ttu-id="5b019-147">Trim</span><span class="sxs-lookup"><span data-stu-id="5b019-147">Trim</span></span>](er-functions-text-trim.md) | <span data-ttu-id="5b019-148">この関数は、先頭と末尾のスペースを切り捨ててから*文字列*値として指定されたテキスト文字列を返し、その後単語間の複数のスペースが削除されます。</span><span class="sxs-lookup"><span data-stu-id="5b019-148">This function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span> |
| [<span data-ttu-id="5b019-149">Upper</span><span class="sxs-lookup"><span data-stu-id="5b019-149">Upper</span></span>](er-functions-text-upper.md) | <span data-ttu-id="5b019-150">この関数は、大文字に変換した後の*文字列*値として指定されたテキスト返します。</span><span class="sxs-lookup"><span data-stu-id="5b019-150">This function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="5b019-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5b019-151">Additional resources</span></span>

[<span data-ttu-id="5b019-152">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="5b019-152">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="5b019-153">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="5b019-153">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="5b019-154">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="5b019-154">Electronic reporting formula language</span></span>](er-formula-language.md)
