---
title: SESSIONTODAY ER 関数
description: このトピックでは、SESSIONTODAY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042272"
---
# <span data-ttu-id="3ec04-103"><a name="SESSIONTODAY">SESSIONTODAY ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="3ec04-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ec04-104">`SESSIONTODAY` 関数は、現在のアプリケーション セッションの日付を表す*日付*値を返します。</span><span class="sxs-lookup"><span data-stu-id="3ec04-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec04-105">構文</span><span class="sxs-lookup"><span data-stu-id="3ec04-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="3ec04-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="3ec04-106">Return values</span></span>

<span data-ttu-id="3ec04-107">*日付*</span><span class="sxs-lookup"><span data-stu-id="3ec04-107">*Date*</span></span>

<span data-ttu-id="3ec04-108">結果日付値。</span><span class="sxs-lookup"><span data-stu-id="3ec04-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="3ec04-109">例</span><span class="sxs-lookup"><span data-stu-id="3ec04-109">Example</span></span>

<span data-ttu-id="3ec04-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="3ec04-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ec04-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3ec04-111">Additional resources</span></span>

[<span data-ttu-id="3ec04-112">日時の関数</span><span class="sxs-lookup"><span data-stu-id="3ec04-112">Date and time functions</span></span>](er-functions-category-datetime.md)
