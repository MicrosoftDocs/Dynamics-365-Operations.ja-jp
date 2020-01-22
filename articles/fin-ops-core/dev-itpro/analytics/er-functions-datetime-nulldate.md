---
title: NULLDATE ER 関数
description: このトピックでは、NULLDATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 7761342c6759c11591e06fc7c32f0ddd8bef407a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916318"
---
# <span data-ttu-id="3e773-103"><a name="NULLDATE">NULLDATE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="3e773-103"><a name="NULLDATE">NULLDATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e773-104">`NULLDATE` 関数は、**null** の日付 (1900 年 1 月 1 日) を表す*日付*値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e773-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e773-105">構文</span><span class="sxs-lookup"><span data-stu-id="3e773-105">Syntax</span></span>

```
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="3e773-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="3e773-106">Return values</span></span>

<span data-ttu-id="3e773-107">*日付*</span><span class="sxs-lookup"><span data-stu-id="3e773-107">*Date*</span></span>

<span data-ttu-id="3e773-108">結果日付値。</span><span class="sxs-lookup"><span data-stu-id="3e773-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="3e773-109">例 1</span><span class="sxs-lookup"><span data-stu-id="3e773-109">Example 1</span></span>

<span data-ttu-id="3e773-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` は、指定されたカスタム形式に基づいて、**null** の日付 1900 年 1 月 1 日を **"1900-01-01"** として返します。</span><span class="sxs-lookup"><span data-stu-id="3e773-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="3e773-111">例 2</span><span class="sxs-lookup"><span data-stu-id="3e773-111">Example 2</span></span>

<span data-ttu-id="3e773-112">式 `IF( Invoice.DocumentDate = NULLDATE(), true, false)` は、**DocumentDate** フィールドの値が **null** の日付と同じである場合に **True** を返します。</span><span class="sxs-lookup"><span data-stu-id="3e773-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="3e773-113">この例では、**請求書**は、**Finance/Table records** タイプの電子申告 (ER) データ ソースで、CustInvoiceJour テーブルを参照します。</span><span class="sxs-lookup"><span data-stu-id="3e773-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e773-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3e773-114">Additional resources</span></span>

[<span data-ttu-id="3e773-115">日時の関数</span><span class="sxs-lookup"><span data-stu-id="3e773-115">Date and time functions</span></span>](er-functions-category-datetime.md)
