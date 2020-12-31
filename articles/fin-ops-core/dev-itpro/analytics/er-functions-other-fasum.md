---
title: FA_SUM ER 関数
description: このトピックでは、FA_SUM 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: 1c46f945a9caae2836886d051da820658e8be9af
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687699"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="47ee2-103">FA_SUM ER 関数</span><span class="sxs-lookup"><span data-stu-id="47ee2-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47ee2-104">`FA_SUM` 関数は、指定された固定資産品目、価値モデル コード、およびの固定資産額のデータで構成される *コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="47ee2-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ee2-105">構文</span><span class="sxs-lookup"><span data-stu-id="47ee2-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="47ee2-106">引数</span><span class="sxs-lookup"><span data-stu-id="47ee2-106">Arguments</span></span>

<span data-ttu-id="47ee2-107">`fixed asset code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="47ee2-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="47ee2-108">残高が計算される固定資産品目のコードを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="47ee2-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="47ee2-109">`value model code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="47ee2-109">`value model code`: *String*</span></span>

<span data-ttu-id="47ee2-110">残高が計算される値モデルのコードを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="47ee2-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="47ee2-111">`start date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="47ee2-111">`start date`: *Date*</span></span>

<span data-ttu-id="47ee2-112">固定資産額が計算された期間の開始日を表す *日付* 値。</span><span class="sxs-lookup"><span data-stu-id="47ee2-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="47ee2-113">`end date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="47ee2-113">`end date`: *Date*</span></span>

<span data-ttu-id="47ee2-114">固定資産額が計算された期間の終了日を表す *日付* 値。</span><span class="sxs-lookup"><span data-stu-id="47ee2-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="47ee2-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="47ee2-115">Return values</span></span>

<span data-ttu-id="47ee2-116">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="47ee2-116">*Container (record)*</span></span>

<span data-ttu-id="47ee2-117">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="47ee2-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="47ee2-118">例</span><span class="sxs-lookup"><span data-stu-id="47ee2-118">Example</span></span>

<span data-ttu-id="47ee2-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` は、**現在** 値モデルと **Date1** から **Date2** の期間のために準備された固定資産 **COMP-000001** の日付コンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="47ee2-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47ee2-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="47ee2-120">Additional resources</span></span>

[<span data-ttu-id="47ee2-121">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="47ee2-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
