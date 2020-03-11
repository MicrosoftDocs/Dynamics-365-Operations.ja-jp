---
title: NOW ER 関数
description: このトピックでは、NOW 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: cb5b2fa1b8c466582b15d60a56260f0f7111ebd9
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042346"
---
# <span data-ttu-id="5724a-103"><a name="NOW">NOW ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="5724a-103"><a name="NOW">NOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5724a-104">`NOW` 関数は、現在のアプリケーション サーバーの日付と時刻を表す *DateTime* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5724a-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="5724a-105">構文</span><span class="sxs-lookup"><span data-stu-id="5724a-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="5724a-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="5724a-106">Return values</span></span>

<span data-ttu-id="5724a-107">*日時*</span><span class="sxs-lookup"><span data-stu-id="5724a-107">*DateTime*</span></span>

<span data-ttu-id="5724a-108">結果日時値。</span><span class="sxs-lookup"><span data-stu-id="5724a-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="5724a-109">例</span><span class="sxs-lookup"><span data-stu-id="5724a-109">Example</span></span>

<span data-ttu-id="5724a-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日時値 2015 年 12 月 24 日を **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="5724a-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5724a-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5724a-111">Additional resources</span></span>

[<span data-ttu-id="5724a-112">日時の関数</span><span class="sxs-lookup"><span data-stu-id="5724a-112">Date and time functions</span></span>](er-functions-category-datetime.md)
