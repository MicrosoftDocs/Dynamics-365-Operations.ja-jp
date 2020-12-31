---
title: NULLDATETIME ER 関数
description: このトピックでは、NULLDATETIME 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65e9ef92dc30e46c297d93e262bad8878df47a0c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682296"
---
# <a name="nulldatetime-er-function"></a><span data-ttu-id="6deb7-103">NULLDATETIME ER 関数</span><span class="sxs-lookup"><span data-stu-id="6deb7-103">NULLDATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6deb7-104">`NULLDATETIME` 関数は、**null** の日時値 (1900 年 1 月 1 日) を表す *DateTime* 値を協定世界時 (グリニッジ標準時 \[GMT\]) で返します。</span><span class="sxs-lookup"><span data-stu-id="6deb7-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="6deb7-105">構文</span><span class="sxs-lookup"><span data-stu-id="6deb7-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="6deb7-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="6deb7-106">Return values</span></span>

<span data-ttu-id="6deb7-107">*日時*</span><span class="sxs-lookup"><span data-stu-id="6deb7-107">*DateTime*</span></span>

<span data-ttu-id="6deb7-108">結果日時値。</span><span class="sxs-lookup"><span data-stu-id="6deb7-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="6deb7-109">例</span><span class="sxs-lookup"><span data-stu-id="6deb7-109">Example</span></span>

<span data-ttu-id="6deb7-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` は、**言語と国/地域の基本設定** セクションにタイムゾーン値 **(GMT) 協定世界時** を持つアプリケーション ユーザーによって開始されたプロセス中に呼び出されると、文字列値 **1900-01-01T00:00:00.0000000+00:00** を返します。</span><span class="sxs-lookup"><span data-stu-id="6deb7-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6deb7-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6deb7-111">Additional resources</span></span>

[<span data-ttu-id="6deb7-112">日時の関数</span><span class="sxs-lookup"><span data-stu-id="6deb7-112">Date and time functions</span></span>](er-functions-category-datetime.md)
