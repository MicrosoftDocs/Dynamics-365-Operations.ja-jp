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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87e8d5498c82d7c9ca6ee0a855f139dde77d75ab
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683822"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="b716c-103">SESSIONTODAY ER 関数</span><span class="sxs-lookup"><span data-stu-id="b716c-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b716c-104">`SESSIONTODAY` 関数は、現在のアプリケーション セッションの日付を表す *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="b716c-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="b716c-105">構文</span><span class="sxs-lookup"><span data-stu-id="b716c-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="b716c-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="b716c-106">Return values</span></span>

<span data-ttu-id="b716c-107">*日付*</span><span class="sxs-lookup"><span data-stu-id="b716c-107">*Date*</span></span>

<span data-ttu-id="b716c-108">結果日付値。</span><span class="sxs-lookup"><span data-stu-id="b716c-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="b716c-109">例</span><span class="sxs-lookup"><span data-stu-id="b716c-109">Example</span></span>

<span data-ttu-id="b716c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="b716c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b716c-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b716c-111">Additional resources</span></span>

[<span data-ttu-id="b716c-112">日時の関数</span><span class="sxs-lookup"><span data-stu-id="b716c-112">Date and time functions</span></span>](er-functions-category-datetime.md)
