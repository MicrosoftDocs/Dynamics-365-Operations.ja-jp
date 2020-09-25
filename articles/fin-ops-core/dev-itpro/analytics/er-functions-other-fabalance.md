---
title: FA_BALANCE ER 機能
description: このトピックでは、FA_BALANCE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 6a969e3a484208388fd82d7a714bee27b7fe64a9
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744170"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="5f7c6-103">FA_BALANCE ER 機能</span><span class="sxs-lookup"><span data-stu-id="5f7c6-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f7c6-104">`FA_BALANCE` 関数は、指定された固定資産品目、価値モデル コード、レポート年度、およびレポート日付の固定資産残高のデータで構成される*コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5f7c6-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f7c6-105">構文</span><span class="sxs-lookup"><span data-stu-id="5f7c6-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="5f7c6-106">引数</span><span class="sxs-lookup"><span data-stu-id="5f7c6-106">Arguments</span></span>

<span data-ttu-id="5f7c6-107">`fixed asset code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="5f7c6-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="5f7c6-108">残高が計算される固定資産品目のコードを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="5f7c6-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="5f7c6-109">`value model code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="5f7c6-109">`value model code`: *String*</span></span>

<span data-ttu-id="5f7c6-110">残高が計算される値モデルのコードを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="5f7c6-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="5f7c6-111">`reporting year`: *列挙型*</span><span class="sxs-lookup"><span data-stu-id="5f7c6-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="5f7c6-112">残高計算の期間を定義する **AssetYear** 申請列挙型の列挙値。</span><span class="sxs-lookup"><span data-stu-id="5f7c6-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="5f7c6-113">`reporting date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="5f7c6-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="5f7c6-114">残高計算の日付を定義する*日付*値。</span><span class="sxs-lookup"><span data-stu-id="5f7c6-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="5f7c6-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="5f7c6-115">Return values</span></span>

<span data-ttu-id="5f7c6-116">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="5f7c6-116">*Container (record)*</span></span>

<span data-ttu-id="5f7c6-117">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="5f7c6-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="5f7c6-118">例</span><span class="sxs-lookup"><span data-stu-id="5f7c6-118">Example</span></span>

<span data-ttu-id="5f7c6-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` は、現在のアプリケーション セッションの日付で**現在**値モデル用に準備された固定資産 **COMP-000001** の残高のデータ コンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="5f7c6-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f7c6-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5f7c6-120">Additional resources</span></span>

[<span data-ttu-id="5f7c6-121">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="5f7c6-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
