---
title: 電子レポート形式でサポートされるプリミティブ データ型
description: このトピックでは、電子申告 (ER) の式でサポートされるプリミティブ データ型について説明します。
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d5e6bb5e070ebbcdb7e99b1b70010acd5fca5ac
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224101"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a><span data-ttu-id="161b2-103">電子レポート形式でサポートされるプリミティブ データ型</span><span class="sxs-lookup"><span data-stu-id="161b2-103">Supported primitive data types for Electronic reporting formulas</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="161b2-104">このトピックでは、[電子申告 (ER)](general-electronic-reporting.md)の式でサポートされるプリミティブ データ型について説明します。</span><span class="sxs-lookup"><span data-stu-id="161b2-104">This topic provides information about the primitive data types that are supported in [Electronic reporting (ER)](general-electronic-reporting.md) expressions.</span></span> <span data-ttu-id="161b2-105">プリミティブ データ型の一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="161b2-105">Here is a list of the primitive data types:</span></span>

- [<span data-ttu-id="161b2-106">ブール値</span><span class="sxs-lookup"><span data-stu-id="161b2-106">boolean</span></span>](#boolean)
- [<span data-ttu-id="161b2-107">日付</span><span class="sxs-lookup"><span data-stu-id="161b2-107">date</span></span>](#date)
- [<span data-ttu-id="161b2-108">datetime</span><span class="sxs-lookup"><span data-stu-id="161b2-108">datetime</span></span>](#datetime)
- [<span data-ttu-id="161b2-109">列挙型</span><span class="sxs-lookup"><span data-stu-id="161b2-109">enumeration</span></span>](#enumeration)
- [<span data-ttu-id="161b2-110">guid</span><span class="sxs-lookup"><span data-stu-id="161b2-110">guid</span></span>](#guid)
- [<span data-ttu-id="161b2-111">整数</span><span class="sxs-lookup"><span data-stu-id="161b2-111">integer</span></span>](#integer)
- [<span data-ttu-id="161b2-112">int64</span><span class="sxs-lookup"><span data-stu-id="161b2-112">int64</span></span>](#int64)
- [<span data-ttu-id="161b2-113">実質</span><span class="sxs-lookup"><span data-stu-id="161b2-113">real</span></span>](#real)
- [<span data-ttu-id="161b2-114">文字列</span><span class="sxs-lookup"><span data-stu-id="161b2-114">string</span></span>](#string)

## <a name="boolean"></a><a name="boolean"></a><span data-ttu-id="161b2-115">ブール値</span><span class="sxs-lookup"><span data-stu-id="161b2-115">Boolean</span></span>

<span data-ttu-id="161b2-116">*ブール値* プリミティブ データ型には、*true* または *false* のいずれかとして評価される値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="161b2-116">The *boolean* primitive data type contains a value that is evaluated as either *true* or *false*.</span></span> <span data-ttu-id="161b2-117">*ブール値* 式が予期される場所では、引当済のリテラル キーワード **True** および **False** を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="161b2-117">You can use the reserved literal keywords **True** and **False** wherever a *boolean* expression is expected.</span></span> <span data-ttu-id="161b2-118">既定値は *false* です。</span><span class="sxs-lookup"><span data-stu-id="161b2-118">The default value is *false*.</span></span>

<span data-ttu-id="161b2-119">*ブール値* の内部テーブル現は *整数* です。</span><span class="sxs-lookup"><span data-stu-id="161b2-119">The internal representation of a *boolean* is an *integer*.</span></span> <span data-ttu-id="161b2-120">*整数* 値 0 (ゼロ) は *false* と評価され、他のすべての *整数値* は *true* と評価されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-120">The *integer* value 0 (zero) is evaluated as *false*, and all other *integer* values are evaluated as *true*.</span></span> <span data-ttu-id="161b2-121">[ER 式デザイナー](er-advanced-formula-editor.md) で *ブール値* を返す構成済みの式を [検証](general-electronic-reporting-formula-designer.md#TestFormula) すると、式が *false* を返したときにテスト結果ペインに *0* (ゼロ) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-121">When you [validate](general-electronic-reporting-formula-designer.md#TestFormula) a configured expression that returns a *boolean* in the [ER formula designer](er-advanced-formula-editor.md), the test result pane presents *0* (zero) when an expression returns *false*.</span></span> <span data-ttu-id="161b2-122">それ以外の場合、テスト結果ペインに *1* が表示されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-122">Otherwise, the test result pane presents *1*.</span></span>

<span data-ttu-id="161b2-123">*ブール値* に暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="161b2-123">A *boolean* has no implicit conversions.</span></span> <span data-ttu-id="161b2-124">ただし、[TEXT](er-functions-text-text.md) 関数を使用して *ブール値* を *文字列* に明示的に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="161b2-124">However, you can use the [TEXT](er-functions-text-text.md) function to explicitly converts a *boolean* to a *string*:</span></span>

- <span data-ttu-id="161b2-125">*false* の値は、文字列 **False** に変換されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-125">The *false* value is converted to the text string **False**.</span></span>
- <span data-ttu-id="161b2-126">*true* の値は、文字列 **True** に変換されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-126">The *true* value is converted to the text string **True**.</span></span>

> [!NOTE]
> <span data-ttu-id="161b2-127">この変換は、提供された言語とカルチャの [コンテキスト](er-design-multilingual-reports.md) に依存しません。</span><span class="sxs-lookup"><span data-stu-id="161b2-127">This conversion doesn't depend on the provided language and culture [context](er-design-multilingual-reports.md).</span></span>

<span data-ttu-id="161b2-128">比較 [演算子](er-formula-language.md#Operators) は、*ブール値* データ型で使用できる唯一の演算子です。</span><span class="sxs-lookup"><span data-stu-id="161b2-128">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *boolean* data type.</span></span> <span data-ttu-id="161b2-129">次の演算子を使用して、2 つの *ブール* 値を比較することができます:  \<\> and =。</span><span class="sxs-lookup"><span data-stu-id="161b2-129">The following operators can be used to compare two *boolean* values: \<\> and =.</span></span>

## <a name="date"></a><a name="date"></a><span data-ttu-id="161b2-130">日</span><span class="sxs-lookup"><span data-stu-id="161b2-130">Date</span></span>

<span data-ttu-id="161b2-131">*date* プリミティブ データ型は、年、月、日を含みます。</span><span class="sxs-lookup"><span data-stu-id="161b2-131">The *date* primitive data type contains the day, month, and year.</span></span> <span data-ttu-id="161b2-132">データは、次の関数を使用して開始できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-132">Dates can be initiated by using the following functions:</span></span>

- [<span data-ttu-id="161b2-133">DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="161b2-133">DATEVALUE</span></span>](er-functions-datetime-datevalue.md)
- [<span data-ttu-id="161b2-134">NULLDATE</span><span class="sxs-lookup"><span data-stu-id="161b2-134">NULLDATE</span></span>](er-functions-datetime-nulldate.md)
- [<span data-ttu-id="161b2-135">SESSIONTODAY</span><span class="sxs-lookup"><span data-stu-id="161b2-135">SESSIONTODAY</span></span>](er-functions-datetime-sessiontoday.md)
- [<span data-ttu-id="161b2-136">TODAY</span><span class="sxs-lookup"><span data-stu-id="161b2-136">TODAY</span></span>](er-functions-datetime-today.md)

<span data-ttu-id="161b2-137">*日付* データ型は、1900 年 1 月 1 日～ 2154 年 12 月 31 日の日付を保持できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-137">The *date* data type can hold dates between January 1, 1900, and December 31, 2154.</span></span> <span data-ttu-id="161b2-138">既定値は、**null** で、内部表示は、日付の 1900 年 1 月 1 日です。</span><span class="sxs-lookup"><span data-stu-id="161b2-138">The default value is **null**, and the internal representation is the date January 1, 1900.</span></span>

<span data-ttu-id="161b2-139">*日付* に暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="161b2-139">A *date* has no implicit conversions.</span></span> <span data-ttu-id="161b2-140">ただし、次の明示的な変換関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-140">However, you can use the following explicit conversion functions:</span></span>

- [<span data-ttu-id="161b2-141">DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="161b2-141">DATEFORMAT</span></span>](er-functions-datetime-dateformat.md)
- [<span data-ttu-id="161b2-142">DATETODATETIME</span><span class="sxs-lookup"><span data-stu-id="161b2-142">DATETODATETIME</span></span>](er-functions-datetime-datetodatetime.md)
- [<span data-ttu-id="161b2-143">TEXT</span><span class="sxs-lookup"><span data-stu-id="161b2-143">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="161b2-144">[ADDDAYS](er-functions-datetime-adddays.md) 関数を使用すると、日付から日数を加算および減算できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-144">The [ADDDAYS](er-functions-datetime-adddays.md) function lets you add and subtract days from dates.</span></span> <span data-ttu-id="161b2-145">このようにして、日付を特定の日数を未来と過去に移動できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-145">In this way, you can move the date a specific number of days into the future and the past.</span></span> <span data-ttu-id="161b2-146">[DAYS](er-functions-datetime-days.md) 関数を使用すると、日付を相互に減算し、日数での差を計算できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-146">The [DAYS](er-functions-datetime-days.md) function lets you subtract dates from each other and calculate the difference in days.</span></span> <span data-ttu-id="161b2-147">*日付* の値の変換に関する詳細は、[日時カテゴリーの ER 関数一覧](er-functions-category-datetime.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="161b2-147">For more information about the transformation of *date* values, see [List of ER functions in the Date and time category](er-functions-category-datetime.md).</span></span>

<span data-ttu-id="161b2-148">比較 [演算子](er-formula-language.md#Operators) は、*日付* データ型で使用できる唯一の演算子です。</span><span class="sxs-lookup"><span data-stu-id="161b2-148">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *date* data type.</span></span> <span data-ttu-id="161b2-149">次の演算子を使用して、2 つの *日付* の値を比較することができます: \<\>、\<, \<=, =, \>、および \>=。</span><span class="sxs-lookup"><span data-stu-id="161b2-149">The following operators can be used to compare two *date* values: \<\>, \<, \<=, =, \>, and \>=.</span></span>

## <a name="datetime"></a><a name="datetime"></a><span data-ttu-id="161b2-150">Datetime</span><span class="sxs-lookup"><span data-stu-id="161b2-150">Datetime</span></span>

<span data-ttu-id="161b2-151">*日時* プリミティブ データ型は *日付* 型と、午前 0 時から経過した時刻を表す値を組み合わせたものです。</span><span class="sxs-lookup"><span data-stu-id="161b2-151">The *datetime* primitive data type combines the *date* type and a value that represents the time that has passed since midnight.</span></span> <span data-ttu-id="161b2-152">時間は、時間、分、秒、秒の分数で表されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-152">The time is expressed in hours, minutes, seconds, and fractions of a second.</span></span> <span data-ttu-id="161b2-153">*datetime* の値には、タイム ゾーンに関する情報も含まれています。</span><span class="sxs-lookup"><span data-stu-id="161b2-153">A *datetime* value also holds information about the time zone.</span></span>

<span data-ttu-id="161b2-154">*日時* データ型は、1900 年 1 月 1 日 (ラウンド トリップ [形式](/dotnet/standard/base-types/standard-date-and-time-format-strings) で 1900-01-01T00:00:00.0000000+00:00) から 2154 年 12 月 31 日 (ラウンドトリップ形式で 2154/12/31T11:59:59.9999999+00:00)。</span><span class="sxs-lookup"><span data-stu-id="161b2-154">The *datetime* data type can hold dates between January 1, 1900 (1900-01-01T00:00:00.0000000+00:00 in the round-trip [format](/dotnet/standard/base-types/standard-date-and-time-format-strings)) and December 31, 2154 (2154/12/31T11:59:59.9999999+00:00 in the round-trip format).</span></span> <span data-ttu-id="161b2-155">*日時* の最小時間単位は 1000 万分の 1 秒です。</span><span class="sxs-lookup"><span data-stu-id="161b2-155">The smallest unit of time in a *datetime* is one ten millionth of a second.</span></span>

> [!NOTE]
> <span data-ttu-id="161b2-156">**hh** [指定子](/dotnet/standard/base-types/standard-date-and-time-format-strings) を時間単位で使用すると、12:59:59:9999999 より上の時間値は有効時間と解釈できません。</span><span class="sxs-lookup"><span data-stu-id="161b2-156">When the **hh** [specifier](/dotnet/standard/base-types/standard-date-and-time-format-strings) is used for hours, time values above 12:59:59:9999999 can't be interpreted as valid times.</span></span>
>
> <span data-ttu-id="161b2-157">**HH** 指定子 を時間単位で使用すると、23:59:59:9999999 より上の時間値は有効時間と解釈できません。</span><span class="sxs-lookup"><span data-stu-id="161b2-157">When the **HH** specifier is used for hours, time values above 23:59:59:9999999 can't be interpreted as valid times.</span></span>

<span data-ttu-id="161b2-158">既定値は **null** で、内部表現は 1900 年 1 月 1 日 (ラウンドトリップ形式で 1900-01-01T00:00:00.0000000+ 00:00) の日付です。</span><span class="sxs-lookup"><span data-stu-id="161b2-158">The default value is **null**, and the internal representation is the date January 1, 1900 (1900-01-01T00:00:00.0000000+00:00 in the round-trip format).</span></span>

<span data-ttu-id="161b2-159">Datetimes は、次の関数を使用して開始できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-159">Datetimes can be initiated by using the following functions:</span></span>

- [<span data-ttu-id="161b2-160">DATETIMEVALUE</span><span class="sxs-lookup"><span data-stu-id="161b2-160">DATETIMEVALUE</span></span>](er-functions-datetime-datetimevalue.md)
- [<span data-ttu-id="161b2-161">NULNULLDATETIMELDATE</span><span class="sxs-lookup"><span data-stu-id="161b2-161">NULNULLDATETIMELDATE</span></span>](er-functions-datetime-nulldatetime.md)
- [<span data-ttu-id="161b2-162">SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="161b2-162">SESSIONNOW</span></span>](er-functions-datetime-sessionnow.md)
- [<span data-ttu-id="161b2-163">NOW</span><span class="sxs-lookup"><span data-stu-id="161b2-163">NOW</span></span>](er-functions-datetime-now.md)

<span data-ttu-id="161b2-164">*datetime* に暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="161b2-164">A *datetime* has no implicit conversions.</span></span> <span data-ttu-id="161b2-165">ただし、次の明示的な変換関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-165">However, you can use the following explicit conversion functions:</span></span>

- [<span data-ttu-id="161b2-166">DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="161b2-166">DATETIMEFORMAT</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="161b2-167">TEXT</span><span class="sxs-lookup"><span data-stu-id="161b2-167">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="161b2-168">*datetime* の値の変換に関する詳細は、[日時カテゴリーの ER 関数一覧](er-functions-category-datetime.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="161b2-168">For more information about the transformation of *datetime* values, see [List of ER functions in the Date and time category](er-functions-category-datetime.md).</span></span>

<span data-ttu-id="161b2-169">比較 [演算子](er-formula-language.md#Operators) は、*datetime* データ型で使用できる唯一の演算子です。</span><span class="sxs-lookup"><span data-stu-id="161b2-169">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *datetime* data type.</span></span> <span data-ttu-id="161b2-170">次の演算子を使用して、2 つの *datetime* の値を比較することができます: \<\>、\<, \<=, =, \>、および \>=。</span><span class="sxs-lookup"><span data-stu-id="161b2-170">The following operators can be used to compare two *datetime* values: \<\>, \<, \<=, =, \>, and \>=.</span></span>

## <a name="enumeration"></a><a name="enumeration"></a><span data-ttu-id="161b2-171">列挙型</span><span class="sxs-lookup"><span data-stu-id="161b2-171">Enumeration</span></span>

<span data-ttu-id="161b2-172">*列挙* のプリミティブ データ型は、リテラルのリストです。</span><span class="sxs-lookup"><span data-stu-id="161b2-172">The *enumeration* primitive data type is a list of literals.</span></span> <span data-ttu-id="161b2-173">アプリケーションの [ソース コード](../dev-ref/xpp-data-primitive.md#enum) で定義されている列挙体を使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-173">You can use enumerations that are defined in the application [source code](../dev-ref/xpp-data-primitive.md#enum).</span></span> <span data-ttu-id="161b2-174">ER [データ モデル ](general-electronic-reporting.md#data-model-and-model-mapping-components)コンポーネントとER [形式](general-electronic-reporting.md#FormatComponentOutbound) コンポーネントで独自の列挙を導入することもできます。</span><span class="sxs-lookup"><span data-stu-id="161b2-174">You can also introduce your own enumerations in the ER [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) and ER [format](general-electronic-reporting.md#FormatComponentOutbound) components.</span></span>

<span data-ttu-id="161b2-175">アプリケーション *列挙* は、ER モデル マッピングと ER 形式の式で使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-175">An application *enumeration* can be used in expressions of any ER model mapping and ER format.</span></span>

<span data-ttu-id="161b2-176">次の図は、編集可能なERデータ モデルに **CustVendCorrectiveReasonCode** モデル列挙体を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="161b2-176">The following illustration shows how you can add the **CustVendCorrectiveReasonCode** model enumeration to the editable ER data model.</span></span>

<span data-ttu-id="161b2-177">[![ER データ モデル デザイナーでモデルの列挙を構成する](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)</span><span class="sxs-lookup"><span data-stu-id="161b2-177">[![Configuring a model enumeration in the ER data model designer](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)</span></span>

<span data-ttu-id="161b2-178">モデルの *列挙* は、*モデル* が導入されたデータ モデルの下で作成された ER モデル マッピングおよび ER 形式の式で使用できます 。</span><span class="sxs-lookup"><span data-stu-id="161b2-178">A model *enumeration* can be used in expressions of any ER model mapping and ER format that were created under a data model where the *enumeration* was introduced.</span></span>

<span data-ttu-id="161b2-179">次の図は、**編集可能な ER 形式に Natura 逆請求サブ カテゴリー** の一覧の書式列挙を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="161b2-179">The following illustration shows how you can add the **List of Natura reverse charge subcategories** format enumeration to the editable ER format.</span></span>

<span data-ttu-id="161b2-180">[![ER 形式デザイナーで形式の列挙を構成する](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)</span><span class="sxs-lookup"><span data-stu-id="161b2-180">[![Configuring a format enumeration in the ER format designer](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)</span></span>

<span data-ttu-id="161b2-181">形式の *列挙* は、*列挙* が導入された ER 形式の式でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-181">A format *enumeration* can be used only in expressions of the ER format where the *enumeration* was introduced.</span></span>

<span data-ttu-id="161b2-182">設定済 ER コンポーネントに特定の列挙を定数として、または ER ソリューションを実行しているユーザーが実行時にダイアログ ボックスで定義した値として、適切な種類の ER データ ソースを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="161b2-182">You must use the appropriate type of ER data sources to bring a specific enumeration to a configured ER component as a constant or as a value that the user who is running an ER solution defined in the dialog box at runtime.</span></span>

- <span data-ttu-id="161b2-183">アプリケーションの列挙には、**Dynamics 365 for Operations \ 列挙** と **一般 \ ユーザー入力パラメータ** のデータ ソースを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="161b2-183">Application enumerations can be accessed by using the **Dynamics 365 for Operations \ Enumeration** and **General \ User input parameters** data sources.</span></span> <span data-ttu-id="161b2-184">次の図は **NoYes** アプリケーションの列挙を参照する編集可能な ER 形式 **appenumNoYes** データソースと **uipNoYes** データソースに追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="161b2-184">The following illustration shows how you can add to the editable ER format the **appenumNoYes** and **uipNoYes** data sources that refer to the **NoYes** application enumeration.</span></span>

    <span data-ttu-id="161b2-185">[![ER 形式デザイナーでのアプリケーション列挙データ ソースの追加](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)</span><span class="sxs-lookup"><span data-stu-id="161b2-185">[![Adding application enumeration data sources in the ER format designer](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)</span></span>

- <span data-ttu-id="161b2-186">データ モデルの列挙には、データ **モデル \ 列挙** および **データ モデル \ 列挙のユーザー入力パラメーター** データ ソースを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="161b2-186">Data model enumerations can be accessed by using the **Data model \ Enumeration** and **Data model \ Enumeration user input parameters** data sources.</span></span> <span data-ttu-id="161b2-187">次の図は **CustVendCorrectiveReasonCode** データモデルの列挙を参照する編集可能な ER 形式 **CustVendCorrectiveReasonCode** データソースに追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="161b2-187">The following illustration shows how you can add to the editable ER format the **CustVendCorrectiveReasonCode** data source that refers to the **CustVendCorrectiveReasonCode** data model enumeration.</span></span>

    <span data-ttu-id="161b2-188">[![ER 形式デザイナーでのアプリケーション列挙データ ソースの追加](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)</span><span class="sxs-lookup"><span data-stu-id="161b2-188">[![Adding model enumeration data sources in the ER format designer](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)</span></span>

- <span data-ttu-id="161b2-189">データ モデルの列挙には、データ **モデル \ 列挙** および **データ モデル \ 列挙のユーザー入力パラメーター** データ ソースを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="161b2-189">Format enumerations can be accessed by using the **Format \ Enumeration** and **Format \ Enumeration user input parameters** data sources.</span></span> <span data-ttu-id="161b2-190">次の図は **Natura reverse charge subcategories** 形式の列挙を参照する編集可能な ER 形式 **NaturaReverseCharge** データソースに追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="161b2-190">The following illustration shows how you can add to the editable ER format the **NaturaReverseCharge** data source that refers to the **Natura reverse charge subcategories** format enumeration.</span></span>

    <span data-ttu-id="161b2-191">[![ER 形式デザイナーでのアプリケーション列挙データ ソースの追加](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)</span><span class="sxs-lookup"><span data-stu-id="161b2-191">[![Adding format enumeration data sources in the ER format designer](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)</span></span>

<span data-ttu-id="161b2-192">*ブール値* に暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="161b2-192">An *enumeration* has no implicit conversions.</span></span> <span data-ttu-id="161b2-193">[TEXT](er-functions-text-text.md) 変換関数を使用すると *列挙* をテキスト文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="161b2-193">However, you can use the [TEXT](er-functions-text-text.md) conversion function to convert an *enumeration* to a text string.</span></span> <span data-ttu-id="161b2-194">この変換は言語に依存しません。</span><span class="sxs-lookup"><span data-stu-id="161b2-194">This conversion isn't language dependent.</span></span> <span data-ttu-id="161b2-195">*列挙* 値を適切な言語固有のラベルに関連付ける方法については、[LISTOFFIELDS](er-functions-list-listoffields.md) 関数と [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) 関数の使用例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="161b2-195">To learn how you can associate an *enumeration* value with the appropriate language-specific labels, see the usage examples for the [LISTOFFIELDS](er-functions-list-listoffields.md) and [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) functions.</span></span>

<span data-ttu-id="161b2-196">比較 [演算子](er-formula-language.md#Operators) は、*列挙* データ型で使用できる唯一の演算子です。</span><span class="sxs-lookup"><span data-stu-id="161b2-196">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *enumeration* data type.</span></span> <span data-ttu-id="161b2-197">次の演算子を使用して、2 つの *列挙* 値を比較することができます:  \<\> and =。</span><span class="sxs-lookup"><span data-stu-id="161b2-197">The following operators can be used to compare two *enumeration* values: \<\> and =.</span></span>

## <a name="guid"></a><a name="guid"></a><span data-ttu-id="161b2-198">Guid</span><span class="sxs-lookup"><span data-stu-id="161b2-198">Guid</span></span>

<span data-ttu-id="161b2-199">*guid* プリミティブ データ型は、グローバルに一意の識別子 (GUID) 値を保持します。</span><span class="sxs-lookup"><span data-stu-id="161b2-199">The *guid* primitive data type holds a globally unique identifier (GUID) value.</span></span> <span data-ttu-id="161b2-200">GUID は、固有の識別子が必要な場合に、すべてのコンピューターとネットワークで使用できる値です。</span><span class="sxs-lookup"><span data-stu-id="161b2-200">A GUID is a value that can be used across all computers and networks, wherever a unique identifier is required.</span></span> <span data-ttu-id="161b2-201">数字が重複することはあまりありません。</span><span class="sxs-lookup"><span data-stu-id="161b2-201">It's unlikely that the number will be duplicated.</span></span> <span data-ttu-id="161b2-202">有効な GUID は、次のすべての仕様を満たします。</span><span class="sxs-lookup"><span data-stu-id="161b2-202">A valid GUID meets all the following specifications:</span></span>

- <span data-ttu-id="161b2-203">32 桁の 16 進数が必要です。</span><span class="sxs-lookup"><span data-stu-id="161b2-203">There must be 32 hexadecimal digits.</span></span>
- <span data-ttu-id="161b2-204">さらに、次の場所では埋め込まれるダッシュ文字が 4 つ必要です: 8-4-4-4-12。</span><span class="sxs-lookup"><span data-stu-id="161b2-204">In addition, there must be four dash characters that are embedded at the following locations: 8-4-4-4-12.</span></span>
- <span data-ttu-id="161b2-205">また、文字列の先頭と末尾にオプションの中かっこ \{\} を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="161b2-205">In addition, optional braces \{\} can be added at the beginning and end of the string.</span></span> <span data-ttu-id="161b2-206">たとえば **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** および **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** は有効な GUID 文字列です。</span><span class="sxs-lookup"><span data-stu-id="161b2-206">For example, both **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** and **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** are valid GUID strings.</span></span>
- <span data-ttu-id="161b2-207">したがって、かっこを追加するかどうかに応じて、合計 36 文字または 38 文字にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="161b2-207">Therefore, there must be a total of 36 or 38 characters, depending on whether braces are added.</span></span>
- <span data-ttu-id="161b2-208">16 進数の桁として使用されている文字は、大文字 (A–F)、小文字 (a–f)、または混在することができます。</span><span class="sxs-lookup"><span data-stu-id="161b2-208">The letters that are used as hexadecimal digits can be uppercase (A–F), lowercase (a–f), or mixed.</span></span>

<span data-ttu-id="161b2-209">次の明示的な変換関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-209">The following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="161b2-210">GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="161b2-210">GUIDVALUE</span></span>](er-functions-text-guidvalue.md)
- [<span data-ttu-id="161b2-211">TEXT</span><span class="sxs-lookup"><span data-stu-id="161b2-211">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="161b2-212">比較 [演算子](er-formula-language.md#Operators) は、*guid* データ型で使用できる唯一の演算子です。</span><span class="sxs-lookup"><span data-stu-id="161b2-212">Comparison [operators](er-formula-language.md#Operators) are the only type of operator that can be used with the *guid* data type.</span></span> <span data-ttu-id="161b2-213">次の演算子を使用して、2 つの *guid* 値を比較することができます:  \<\> and =。</span><span class="sxs-lookup"><span data-stu-id="161b2-213">The following operators can be used to compare two *guid* values: \<\> and =.</span></span>

## <a name="integer"></a><a name="integer"></a><span data-ttu-id="161b2-214">整数</span><span class="sxs-lookup"><span data-stu-id="161b2-214">Integer</span></span>

<span data-ttu-id="161b2-215">*整数* プリミティブ データ型は、小数点以下の桁数を持たない数値を表します。</span><span class="sxs-lookup"><span data-stu-id="161b2-215">The *integer* primitive data type represents a number that has no decimal places.</span></span> <span data-ttu-id="161b2-216">整数は、繰り返しのステートメントの制御変数またはレコード リストのインデックスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-216">Integers are used as control variables in repetitive statements or as indexes in record lists.</span></span>

<span data-ttu-id="161b2-217">*整数* リテラルは **12345** のように、ER [式](general-electronic-reporting-formula-designer.md#formula-designer-overview) (フォーミュラ) に直接入力された整数です。</span><span class="sxs-lookup"><span data-stu-id="161b2-217">An *integer* literal is the integer as it's entered directly in an ER [expression](general-electronic-reporting-formula-designer.md#formula-designer-overview) (formula), such as **12345**.</span></span> <span data-ttu-id="161b2-218">*整数* は 32 ビット幅です。</span><span class="sxs-lookup"><span data-stu-id="161b2-218">An *integer* is 32-bits wide.</span></span> <span data-ttu-id="161b2-219">既定値は、**0** で、内部表示は、長い番号です。</span><span class="sxs-lookup"><span data-stu-id="161b2-219">The default value is **0**, and the internal representation is a long number.</span></span> <span data-ttu-id="161b2-220">*整数* は自動的に *実数* に変換されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-220">An *integer* is automatically converted to a *real*.</span></span>

<span data-ttu-id="161b2-221">さらに、次の明示的な変換関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-221">Additionally, the following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="161b2-222">INTVALUE</span><span class="sxs-lookup"><span data-stu-id="161b2-222">INTVALUE</span></span>](er-functions-conversion-intvalue.md)
- [<span data-ttu-id="161b2-223">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="161b2-223">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md)
- [<span data-ttu-id="161b2-224">TEXT</span><span class="sxs-lookup"><span data-stu-id="161b2-224">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="161b2-225">*整数* の範囲は \[ -2,147,483,647: 2,147,483,647\] です。</span><span class="sxs-lookup"><span data-stu-id="161b2-225">The range of an *integer* is \[-2,147,483,647 : 2,147,483,647\].</span></span> <span data-ttu-id="161b2-226">この範囲内のすべての整数はリテラルとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-226">All integers of this range can be used as literals.</span></span>

<span data-ttu-id="161b2-227">すべての比較演算子と算術 [演算子](er-formula-language.md#Operators) は *整数* データ型と共に使用できます 。</span><span class="sxs-lookup"><span data-stu-id="161b2-227">All comparison and mathematical [operators](er-formula-language.md#Operators) can be used with the *integer* data type.</span></span>

## <a name="int64"></a><a name="int64"></a><span data-ttu-id="161b2-228">Int64</span><span class="sxs-lookup"><span data-stu-id="161b2-228">Int64</span></span>

<span data-ttu-id="161b2-229">*int64* プリミティブ データ型は、小数点以下の桁数を持たない数値を表します。</span><span class="sxs-lookup"><span data-stu-id="161b2-229">The *int64* primitive data type represents a number that has no decimal places.</span></span> <span data-ttu-id="161b2-230">*int64* 値は、繰り返しのステートメントの制御変数またはレコード識別子として使用されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-230">*Int64* values are used as control variables in repetitive statements or as record identifiers.</span></span>

<span data-ttu-id="161b2-231">*int64* は 64 ビット幅です。</span><span class="sxs-lookup"><span data-stu-id="161b2-231">An *int64* is 64-bits wide.</span></span> <span data-ttu-id="161b2-232">既定値は、**0** で、内部表示は、長い番号です。</span><span class="sxs-lookup"><span data-stu-id="161b2-232">The default value is **0**, and the internal representation is a long number.</span></span> <span data-ttu-id="161b2-233">*int64* は自動的に *実数* に変換されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-233">An *int64* is automatically converted to a *real*.</span></span>

<span data-ttu-id="161b2-234">さらに、次の明示的な変換関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-234">Additionally, the following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="161b2-235">INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="161b2-235">INT64VALUE</span></span>](er-functions-conversion-int64value.md)
- [<span data-ttu-id="161b2-236">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="161b2-236">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md)
- [<span data-ttu-id="161b2-237">TEXT</span><span class="sxs-lookup"><span data-stu-id="161b2-237">TEXT</span></span>](er-functions-text-text.md)

<span data-ttu-id="161b2-238">*int64* の範囲は \[-9,223,372,036,854,775,807: 9,223,372,036,854,775,807\] です。</span><span class="sxs-lookup"><span data-stu-id="161b2-238">The range of an *int64* is \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\].</span></span>

<span data-ttu-id="161b2-239">すべての比較演算子と算術 [演算子](er-formula-language.md#Operators) は *int64* データ型と共に使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-239">All comparison and mathematical [operators](er-formula-language.md#Operators) can be used with the *int64* data type.</span></span>

## <a name="real"></a><a name="real"></a><span data-ttu-id="161b2-240">実績</span><span class="sxs-lookup"><span data-stu-id="161b2-240">Real</span></span>

<span data-ttu-id="161b2-241">*実数* 変数は、整数に加えて小数値を保持できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-241">The *real* primitive data type can hold decimal values in addition to integers.</span></span> <span data-ttu-id="161b2-242">10 進リテラル は *実数* が予期される場所ではどこでも使用することができます。</span><span class="sxs-lookup"><span data-stu-id="161b2-242">You can use decimal literals anywhere that a *real* is expected.</span></span> <span data-ttu-id="161b2-243">10 進数リテラルは、**2.19** のように、コードで直接入力された 10 進数です。</span><span class="sxs-lookup"><span data-stu-id="161b2-243">A decimal literal is the decimal as it's entered directly in code, such as **2.19**.</span></span>

> [!NOTE]
> <span data-ttu-id="161b2-244">ER 式では、ピリオド (.) が常に小数点として使用されます。</span><span class="sxs-lookup"><span data-stu-id="161b2-244">In ER expressions, a period (.) is always used as the decimal separator.</span></span>

<span data-ttu-id="161b2-245">Reals はすべての式で使用することができ、比較演算子と算術演算子の両方と共に使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-245">Reals can be used in all expressions, and they can be used with both comparison and arithmetic operators.</span></span> <span data-ttu-id="161b2-246">*実数* は、16桁の有効な数値の精度があります。</span><span class="sxs-lookup"><span data-stu-id="161b2-246">A *real* has a precision of 16 significant digits.</span></span> <span data-ttu-id="161b2-247">*real* の既定値は **0.0** で、内部表示はバイナリコード化されたデジタル (BCD) 番号です。</span><span class="sxs-lookup"><span data-stu-id="161b2-247">The default value for a *real* is **0.0**, and the internal representation is a binary-coded digital (BCD) number.</span></span> <span data-ttu-id="161b2-248">BCD エンコードにより、0.1 の倍数の値の正確な表現が可能になります。</span><span class="sxs-lookup"><span data-stu-id="161b2-248">The BCD encoding enables exact representations of values that are multiples of 0.1.</span></span> <span data-ttu-id="161b2-249">*実数* 変数の範囲は、-(10)<sup>127</sup> から (10)<sup>127</sup> です。</span><span class="sxs-lookup"><span data-stu-id="161b2-249">The range of a *real* variable is -(10)<sup>127</sup> through (10)<sup>127</sup>.</span></span> <span data-ttu-id="161b2-250">この範囲内のすべての実数は ER 式でリテラルとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-250">All reals in this range can be used as literals in ER expressions.</span></span>

<span data-ttu-id="161b2-251">*実数* に暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="161b2-251">A *real* has no implicit conversions.</span></span> <span data-ttu-id="161b2-252">ただし、次の関数を使用して *実数* を他のデータ型に明示的に変換し、その他のデータ型を *実数* に変換することもできます。</span><span class="sxs-lookup"><span data-stu-id="161b2-252">However, you can use the following functions to explicitly convert a *real* to other data types and other data types to a *real*:</span></span>

- [<span data-ttu-id="161b2-253">INTVALUE</span><span class="sxs-lookup"><span data-stu-id="161b2-253">INTVALUE</span></span>](er-functions-conversion-intvalue.md)
- [<span data-ttu-id="161b2-254">INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="161b2-254">INT64VALUE</span></span>](er-functions-conversion-int64value.md)
- [<span data-ttu-id="161b2-255">NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="161b2-255">NUMBERFORMAT</span></span>](er-functions-text-numberformat.md)
- [<span data-ttu-id="161b2-256">TEXT</span><span class="sxs-lookup"><span data-stu-id="161b2-256">TEXT</span></span>](er-functions-text-text.md)
- [<span data-ttu-id="161b2-257">VALUE</span><span class="sxs-lookup"><span data-stu-id="161b2-257">VALUE</span></span>](er-functions-conversion-value.md)

<span data-ttu-id="161b2-258">すべての比較演算子と算術 [演算子](er-formula-language.md#Operators) は *実数* データ型と共に使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-258">All comparison and mathematical [operators](er-formula-language.md#Operators) can be used with the *real* data type.</span></span>

## <a name="string"></a><a name="string"></a><span data-ttu-id="161b2-259">文字列</span><span class="sxs-lookup"><span data-stu-id="161b2-259">String</span></span>

<span data-ttu-id="161b2-260">*文字列* プリミティブ データ型は、テキスト、アカウント番号、住所、電話番号として使用される文字のシーケンスを表します。</span><span class="sxs-lookup"><span data-stu-id="161b2-260">The *string* primitive data type represents a sequence of characters that are used as texts, account numbers, addresses, and telephone numbers.</span></span>

<span data-ttu-id="161b2-261">*文字列* リテラルは引用符 ("") で囲まれた文字です。</span><span class="sxs-lookup"><span data-stu-id="161b2-261">*String* literals are characters that are enclosed in quotation marks ("").</span></span> <span data-ttu-id="161b2-262">*文字列* の値が ER 式に必要な場合はいつでも、*文字列* リテラルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="161b2-262">*String* literals can be used wherever *string* values are expected in ER expressions.</span></span> <span data-ttu-id="161b2-263">比較などの論理式では文字列を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="161b2-263">You can use strings in logical expressions, such as comparisons.</span></span> <span data-ttu-id="161b2-264">**\&** 演算子または [CONCATENATE](er-functions-text-concatenate.md) 関数を使用して、*文字列* の値を連結することもできます。</span><span class="sxs-lookup"><span data-stu-id="161b2-264">You can also concatenate *string* values by using the **\&** operator or the [CONCATENATE](er-functions-text-concatenate.md) function.</span></span>

> [!NOTE]
> <span data-ttu-id="161b2-265">2 つの *文字列* 値を連結し、結果の *文字列* を複数の行にまたがたい場合は、値の間に改行区切りを使用します。</span><span class="sxs-lookup"><span data-stu-id="161b2-265">If you concatenate two *string* values, and you want the resulting *string* to span more than one line, use the line break separator between the values.</span></span> <span data-ttu-id="161b2-266">TEXT 出力の場合、この区切り文字は [CHAR](er-functions-text-char.md)(10) または CHAR(13) 式を使用して生成される文字にすることができます。</span><span class="sxs-lookup"><span data-stu-id="161b2-266">For the TEXT output, this separator can be a character that is generated by using the [CHAR](er-functions-text-char.md)(10) or CHAR(13) expression.</span></span> <span data-ttu-id="161b2-267">HTML の場合は、**\<br\>** タグにできます 。</span><span class="sxs-lookup"><span data-stu-id="161b2-267">For HTML, it can be the **\<br\>** tag.</span></span>

<span data-ttu-id="161b2-268">*文字列* の既定値は、文字を含む空白のテキスト文字列で、内部表現は文字のリストです。</span><span class="sxs-lookup"><span data-stu-id="161b2-268">The default value for a *string* is a blank text string that has no characters, and the internal representation is a list of characters.</span></span>

<span data-ttu-id="161b2-269">文字列の自動変換はありません。</span><span class="sxs-lookup"><span data-stu-id="161b2-269">There are no automatic conversions for strings.</span></span> <span data-ttu-id="161b2-270">ただし、次の明示的な変換関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-270">However, the following explicit conversion functions can be used:</span></span>

- [<span data-ttu-id="161b2-271">CHAR</span><span class="sxs-lookup"><span data-stu-id="161b2-271">CHAR</span></span>](er-functions-text-char.md)
- [<span data-ttu-id="161b2-272">FORMAT</span><span class="sxs-lookup"><span data-stu-id="161b2-272">FORMAT</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="161b2-273">LEFT</span><span class="sxs-lookup"><span data-stu-id="161b2-273">LEFT</span></span>](er-functions-text-left.md)
- [<span data-ttu-id="161b2-274">LEN</span><span class="sxs-lookup"><span data-stu-id="161b2-274">LEN</span></span>](er-functions-text-len.md)
- [<span data-ttu-id="161b2-275">MID</span><span class="sxs-lookup"><span data-stu-id="161b2-275">MID</span></span>](er-functions-text-mid.md)
- [<span data-ttu-id="161b2-276">PADLEFT</span><span class="sxs-lookup"><span data-stu-id="161b2-276">PADLEFT</span></span>](er-functions-text-padleft.md)
- [<span data-ttu-id="161b2-277">REPLACE</span><span class="sxs-lookup"><span data-stu-id="161b2-277">REPLACE</span></span>](er-functions-text-replace.md)
- [<span data-ttu-id="161b2-278">RIGHT</span><span class="sxs-lookup"><span data-stu-id="161b2-278">RIGHT</span></span>](er-functions-text-right.md)
- [<span data-ttu-id="161b2-279">TEXT</span><span class="sxs-lookup"><span data-stu-id="161b2-279">TEXT</span></span>](er-functions-text-text.md)
- [<span data-ttu-id="161b2-280">TRANSLATE</span><span class="sxs-lookup"><span data-stu-id="161b2-280">TRANSLATE</span></span>](er-functions-text-translate.md)
- [<span data-ttu-id="161b2-281">TRIM</span><span class="sxs-lookup"><span data-stu-id="161b2-281">TRIM</span></span>](er-functions-text-trim.md)
- [<span data-ttu-id="161b2-282">UPPER</span><span class="sxs-lookup"><span data-stu-id="161b2-282">UPPER</span></span>](er-functions-text-upper.md)

<span data-ttu-id="161b2-283">*文字列* の値の変換については、[テキスト カテゴリーの ER 関数一覧](er-functions-category-text.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="161b2-283">For more about the transformation of *string* values, see [List of ER functions of the text category](er-functions-category-text.md).</span></span>

<span data-ttu-id="161b2-284">*文字列* は、無制限の文字数を保持できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-284">A *string* can hold an indefinite number of characters.</span></span>

<span data-ttu-id="161b2-285">すべての比較 [演算子](er-formula-language.md#Operators) は *文字列* データ型と共に使用できます。</span><span class="sxs-lookup"><span data-stu-id="161b2-285">All comparison [operators](er-formula-language.md#Operators) can be used with the *string* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="161b2-286">追加リソース</span><span class="sxs-lookup"><span data-stu-id="161b2-286">Additional resources</span></span>

- [<span data-ttu-id="161b2-287">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="161b2-287">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="161b2-288">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="161b2-288">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="161b2-289">対応している複合データ型</span><span class="sxs-lookup"><span data-stu-id="161b2-289">Supported composite data types</span></span>](er-formula-supported-data-types-composite.md)
