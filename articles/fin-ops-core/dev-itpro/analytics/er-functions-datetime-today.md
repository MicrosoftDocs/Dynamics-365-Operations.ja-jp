---
title: TODAY ER 関数
description: このトピックでは、TODAY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746750"
---
# <a name="today-er-function"></a><span data-ttu-id="9e137-103">TODAY ER 関数</span><span class="sxs-lookup"><span data-stu-id="9e137-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e137-104">`TODAY` 関数は、現在のアプリケーション サーバーの日付を表す *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="9e137-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e137-105">構文</span><span class="sxs-lookup"><span data-stu-id="9e137-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="9e137-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="9e137-106">Return values</span></span>

<span data-ttu-id="9e137-107">*日付*</span><span class="sxs-lookup"><span data-stu-id="9e137-107">*Date*</span></span>

<span data-ttu-id="9e137-108">結果日付値。</span><span class="sxs-lookup"><span data-stu-id="9e137-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="9e137-109">例</span><span class="sxs-lookup"><span data-stu-id="9e137-109">Example</span></span>

<span data-ttu-id="9e137-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="9e137-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e137-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9e137-111">Additional resources</span></span>

[<span data-ttu-id="9e137-112">日時の関数</span><span class="sxs-lookup"><span data-stu-id="9e137-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]