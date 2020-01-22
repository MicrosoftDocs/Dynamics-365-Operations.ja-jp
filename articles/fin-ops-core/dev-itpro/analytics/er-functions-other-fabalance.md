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
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916019"
---
# <span data-ttu-id="9958e-103"><a name="FA_BALANCE">FA_BALANCE ER 機能</a></span><span class="sxs-lookup"><span data-stu-id="9958e-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9958e-104">`FA_BALANCE` 関数は、指定された固定資産品目、価値モデル コード、レポート年度、およびレポート日付の固定資産残高のデータで構成される*コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="9958e-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="9958e-105">構文</span><span class="sxs-lookup"><span data-stu-id="9958e-105">Syntax</span></span>

```
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="9958e-106">引数</span><span class="sxs-lookup"><span data-stu-id="9958e-106">Arguments</span></span>

<span data-ttu-id="9958e-107">`fixed asset code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="9958e-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="9958e-108">残高が計算される固定資産品目のコードを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="9958e-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="9958e-109">`value model code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="9958e-109">`value model code`: *String*</span></span>

<span data-ttu-id="9958e-110">残高が計算される値モデルのコードを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="9958e-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="9958e-111">`reporting year`: *列挙型*</span><span class="sxs-lookup"><span data-stu-id="9958e-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="9958e-112">残高計算の期間を定義する **AssetYear** 申請列挙型の列挙値。</span><span class="sxs-lookup"><span data-stu-id="9958e-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="9958e-113">`reporting date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="9958e-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="9958e-114">残高計算の日付を定義する*日付*値。</span><span class="sxs-lookup"><span data-stu-id="9958e-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="9958e-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="9958e-115">Return values</span></span>

<span data-ttu-id="9958e-116">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="9958e-116">*Container (record)*</span></span>

<span data-ttu-id="9958e-117">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="9958e-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="9958e-118">例</span><span class="sxs-lookup"><span data-stu-id="9958e-118">Example</span></span>

<span data-ttu-id="9958e-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` は、現在のアプリケーション セッションの日付で**現在**値モデル用に準備された固定資産 **COMP-000001** の残高のデータ コンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="9958e-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9958e-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9958e-120">Additional resources</span></span>

[<span data-ttu-id="9958e-121">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="9958e-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
