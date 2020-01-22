---
title: SESSIONNOW ER 関数
description: このトピックでは、SESSIONNOW 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916272"
---
# <span data-ttu-id="6dda4-103"><a name="">SESSIONNOW ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="6dda4-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dda4-104">`SESSIONNOW` 関数は、現在のアプリケーション セッションの日付と時刻を表す *DateTime* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="6dda4-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dda4-105">構文</span><span class="sxs-lookup"><span data-stu-id="6dda4-105">Syntax</span></span>

```
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="6dda4-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="6dda4-106">Return values</span></span>

<span data-ttu-id="6dda4-107">*日時*</span><span class="sxs-lookup"><span data-stu-id="6dda4-107">*DateTime*</span></span>

<span data-ttu-id="6dda4-108">結果日時値。</span><span class="sxs-lookup"><span data-stu-id="6dda4-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="6dda4-109">例</span><span class="sxs-lookup"><span data-stu-id="6dda4-109">Example</span></span>

<span data-ttu-id="6dda4-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日時値 2015 年 12 月 24 日を **"24.12.2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="6dda4-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dda4-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6dda4-111">Additional resources</span></span>

[<span data-ttu-id="6dda4-112">日時の関数</span><span class="sxs-lookup"><span data-stu-id="6dda4-112">Date and time functions</span></span>](er-functions-category-datetime.md)
