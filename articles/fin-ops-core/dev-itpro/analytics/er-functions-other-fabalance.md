---
title: FA_BALANCE ER 機能
description: このトピックでは、FA_BALANCE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 37c440a5c626016ebdb75703a2be63c9a1a2b560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567595"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="8721b-103">FA_BALANCE ER 機能</span><span class="sxs-lookup"><span data-stu-id="8721b-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8721b-104">`FA_BALANCE` 関数は、指定された固定資産品目、価値モデル コード、レポート年度、およびレポート日付の固定資産残高のデータで構成される *コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="8721b-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="8721b-105">構文</span><span class="sxs-lookup"><span data-stu-id="8721b-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="8721b-106">引数</span><span class="sxs-lookup"><span data-stu-id="8721b-106">Arguments</span></span>

<span data-ttu-id="8721b-107">`fixed asset code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="8721b-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="8721b-108">残高が計算される固定資産品目のコードを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="8721b-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="8721b-109">`value model code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="8721b-109">`value model code`: *String*</span></span>

<span data-ttu-id="8721b-110">残高が計算される値モデルのコードを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="8721b-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="8721b-111">`reporting year`: *列挙型*</span><span class="sxs-lookup"><span data-stu-id="8721b-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="8721b-112">残高計算の期間を定義する **AssetYear** 申請列挙型の列挙値。</span><span class="sxs-lookup"><span data-stu-id="8721b-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="8721b-113">`reporting date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="8721b-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="8721b-114">残高計算の日付を定義する *日付* 値。</span><span class="sxs-lookup"><span data-stu-id="8721b-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="8721b-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="8721b-115">Return values</span></span>

<span data-ttu-id="8721b-116">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="8721b-116">*Container (record)*</span></span>

<span data-ttu-id="8721b-117">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="8721b-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="8721b-118">例</span><span class="sxs-lookup"><span data-stu-id="8721b-118">Example</span></span>

<span data-ttu-id="8721b-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` は、現在のアプリケーション セッションの日付で **現在** 値モデル用に準備された固定資産 **COMP-000001** の残高のデータ コンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="8721b-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8721b-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8721b-120">Additional resources</span></span>

[<span data-ttu-id="8721b-121">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="8721b-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]