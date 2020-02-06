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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32eb07689598a3b6c852f272b480106670b88cd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916985"
---
# <span data-ttu-id="9c9b4-103"><a name="FA_SUM">FA_SUM ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="9c9b4-103"><a name="FA_SUM">FA_SUM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c9b4-104">`FA_SUM` 関数は、指定された固定資産品目、価値モデル コード、およびの固定資産額のデータで構成される*コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="9c9b4-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c9b4-105">構文</span><span class="sxs-lookup"><span data-stu-id="9c9b4-105">Syntax</span></span>

```
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="9c9b4-106">引数</span><span class="sxs-lookup"><span data-stu-id="9c9b4-106">Arguments</span></span>

<span data-ttu-id="9c9b4-107">`fixed asset code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="9c9b4-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="9c9b4-108">残高が計算される固定資産品目のコードを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="9c9b4-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="9c9b4-109">`value model code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="9c9b4-109">`value model code`: *String*</span></span>

<span data-ttu-id="9c9b4-110">残高が計算される値モデルのコードを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="9c9b4-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="9c9b4-111">`start date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="9c9b4-111">`start date`: *Date*</span></span>

<span data-ttu-id="9c9b4-112">固定資産額が計算された期間の開始日を表す*日付*値。</span><span class="sxs-lookup"><span data-stu-id="9c9b4-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="9c9b4-113">`end date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="9c9b4-113">`end date`: *Date*</span></span>

<span data-ttu-id="9c9b4-114">固定資産額が計算された期間の終了日を表す*日付*値。</span><span class="sxs-lookup"><span data-stu-id="9c9b4-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c9b4-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="9c9b4-115">Return values</span></span>

<span data-ttu-id="9c9b4-116">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="9c9b4-116">*Container (record)*</span></span>

<span data-ttu-id="9c9b4-117">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="9c9b4-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="9c9b4-118">例</span><span class="sxs-lookup"><span data-stu-id="9c9b4-118">Example</span></span>

<span data-ttu-id="9c9b4-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` は、**現在**値モデルと **Date1** から **Date2** の期間のために準備された固定資産 **COMP-000001** の日付コンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="9c9b4-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c9b4-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9c9b4-120">Additional resources</span></span>

[<span data-ttu-id="9c9b4-121">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="9c9b4-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)