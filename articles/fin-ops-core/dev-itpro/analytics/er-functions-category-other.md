---
title: ビジネス ドメイン固有のカテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされるビジネス ドメイン固有の関数について説明します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 8f7612e83d9f30281e2b1a783275365459e67a40
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686126"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a><span data-ttu-id="5e42a-103">ビジネス ドメイン固有のカテゴリ内の ER 関数のリスト</span><span class="sxs-lookup"><span data-stu-id="5e42a-103">List of ER functions in the business domain–specific category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e42a-104">電子報告 (ER) ドメイン固有の関数を使用すると、Microsoft Dynamics 365 Finance の実装固有の計算およびデータ アクセス要求を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5e42a-104">Electronic reporting (ER) domain-specific functions can be used to perform calculations and data access requests that are specific to the implementation of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="5e42a-105">このトピックでは、これらの関数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="5e42a-106">サポートされている関数のリスト</span><span class="sxs-lookup"><span data-stu-id="5e42a-106">List of supported functions</span></span>

| <span data-ttu-id="5e42a-107">職務</span><span class="sxs-lookup"><span data-stu-id="5e42a-107">Function</span></span>| <span data-ttu-id="5e42a-108">説明</span><span class="sxs-lookup"><span data-stu-id="5e42a-108">Description</span></span> |
|---------|-------------|
| [<span data-ttu-id="5e42a-109">CH_Bank_Mod_10</span><span class="sxs-lookup"><span data-stu-id="5e42a-109">CH_Bank_Mod_10</span></span>](er-functions-other-chbankmode10.md) | <span data-ttu-id="5e42a-110">この関数は、指定された請求書番号の桁数に基づいて、MOD10 式として債権者参照を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-110">This function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="5e42a-111">CN_GBT_AdditionalDimensionID</span><span class="sxs-lookup"><span data-stu-id="5e42a-111">CN_GBT_AdditionalDimensionID</span></span>](er-functions-other-cngbtadditionaldimensionid.md) | <span data-ttu-id="5e42a-112">この関数は、指定された文字列から取得された単一の財務分析コード ID を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-112">This function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="5e42a-113">指定された文字列は、ID のコンマ区切りのリストとしてすべての分析コードを示します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-113">The specified string presents all dimensions as a comma-separated list of IDs.</span></span> |
| [<span data-ttu-id="5e42a-114">ConvertCurrency</span><span class="sxs-lookup"><span data-stu-id="5e42a-114">ConvertCurrency</span></span>](er-functions-other-convertcurrency.md) | <span data-ttu-id="5e42a-115">この関数は、特定の日付で指定された会社の設定を使用して、指定された換算元の通貨から指定された換算先の通貨に指定された金額を変換した結果を表す、*実数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-115">This function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span> |
| [<span data-ttu-id="5e42a-116">CurCredRef</span><span class="sxs-lookup"><span data-stu-id="5e42a-116">CurCredRef</span></span>](er-functions-other-curcredref.md) | <span data-ttu-id="5e42a-117">この関数は、指定された請求書番号の桁数に基づいて、債権者参照を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-117">This function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="5e42a-118">FA_Balance</span><span class="sxs-lookup"><span data-stu-id="5e42a-118">FA_Balance</span></span>](er-functions-other-fabalance.md) | <span data-ttu-id="5e42a-119">この関数は、指定された固定資産品目、価値モデル コード、レポート年度、およびレポート日付の固定資産残高のデータで構成される *コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-119">This function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span> |
| [<span data-ttu-id="5e42a-120">FA_Sum</span><span class="sxs-lookup"><span data-stu-id="5e42a-120">FA_Sum</span></span>](er-functions-other-fasum.md) | <span data-ttu-id="5e42a-121">この関数は、指定された固定資産品目、価値モデル コード、およびの固定資産額のデータで構成される *コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-121">This function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span> |
| [<span data-ttu-id="5e42a-122">GetCurrentCompany</span><span class="sxs-lookup"><span data-stu-id="5e42a-122">GetCurrentCompany</span></span>](er-functions-other-getcurrentcompany.md) | <span data-ttu-id="5e42a-123">この関数は、現在ユーザーがサイン インしている法人 (会社) コードのテキスト表現する *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-123">This function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span> |
| [<span data-ttu-id="5e42a-124">ISOCredRef</span><span class="sxs-lookup"><span data-stu-id="5e42a-124">ISOCredRef</span></span>](er-functions-other-isocredref.md) | <span data-ttu-id="5e42a-125">この関数は、指定された請求書番号の数字とアルファベット記号に基づいて、国際標準化機構 (ISO) 送金受取人参照情報を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-125">This function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span> |
| [<span data-ttu-id="5e42a-126">IsValidCharacterISO7064</span><span class="sxs-lookup"><span data-stu-id="5e42a-126">IsValidCharacterISO7064</span></span>](er-functions-other-isvalidchariso7064.md) | <span data-ttu-id="5e42a-127">この関数は、指定された文字列が有効な国際銀行番号 (IBAN) を表す場合、**TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-127">This function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="5e42a-128">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5e42a-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="5e42a-129">Mod_97</span><span class="sxs-lookup"><span data-stu-id="5e42a-129">Mod_97</span></span>](er-functions-other-mod97.md) | <span data-ttu-id="5e42a-130">この関数は、指定された請求書番号の桁数に基づいて、MOD97 式として債権者参照を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-130">This function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="5e42a-131">NumSeqValue</span><span class="sxs-lookup"><span data-stu-id="5e42a-131">NumSeqValue</span></span>](er-functions-other-numseqvalue.md) | <span data-ttu-id="5e42a-132">この関数は、指定された番号順序、範囲、およびスコープ ID に基づいて、番号順序の新しい生成値を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-132">This function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="5e42a-133">スコープ ID は、ER 形式が実行されるコンテキストによって提供される会社コードと同じです。</span><span class="sxs-lookup"><span data-stu-id="5e42a-133">The scope ID equals the company code that is supplied by the context that the ER format is run under.</span></span> |
| [<span data-ttu-id="5e42a-134">RoundAmount</span><span class="sxs-lookup"><span data-stu-id="5e42a-134">RoundAmount</span></span>](er-functions-other-roundamount.md) | <span data-ttu-id="5e42a-135">この関数は、指定された丸めルールに従って、指定された数値を指定された小数点以下の桁数となるように丸めた結果を表す *実数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-135">This function returns a *Real* value that represents the result of rounding the specified amount to the specified number of decimal places according to the specified rounding rule.</span></span> |
| [<span data-ttu-id="5e42a-136">TableName2ID</span><span class="sxs-lookup"><span data-stu-id="5e42a-136">TableName2ID</span></span>](er-functions-other-tablename2id.md) | <span data-ttu-id="5e42a-137">この関数は、*整数* 値として指定されたテーブル名に対応するテーブル ID の数値表現を返します。</span><span class="sxs-lookup"><span data-stu-id="5e42a-137">This function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="5e42a-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5e42a-138">Additional resources</span></span>

[<span data-ttu-id="5e42a-139">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="5e42a-139">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="5e42a-140">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="5e42a-140">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="5e42a-141">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="5e42a-141">Electronic reporting formula language</span></span>](er-formula-language.md)
