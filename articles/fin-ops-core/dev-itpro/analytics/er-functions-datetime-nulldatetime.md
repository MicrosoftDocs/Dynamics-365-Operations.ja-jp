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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4165f6e064d12200907ac76b6779d35bc578daba
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917491"
---
# <span data-ttu-id="794f0-103"><a name="NULLDATETIME">NULLDATETIME ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="794f0-103"><a name="NULLDATETIME">NULLDATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="794f0-104">`NULLDATETIME` 関数は、**null** の日時値 (1900 年 1 月 1 日) を表す *DateTime* 値を協定世界時 (グリニッジ標準時 \[GMT\]) で返します。</span><span class="sxs-lookup"><span data-stu-id="794f0-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="794f0-105">構文</span><span class="sxs-lookup"><span data-stu-id="794f0-105">Syntax</span></span>

```
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="794f0-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="794f0-106">Return values</span></span>

<span data-ttu-id="794f0-107">*日時*</span><span class="sxs-lookup"><span data-stu-id="794f0-107">*DateTime*</span></span>

<span data-ttu-id="794f0-108">結果日時値。</span><span class="sxs-lookup"><span data-stu-id="794f0-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="794f0-109">例</span><span class="sxs-lookup"><span data-stu-id="794f0-109">Example</span></span>

<span data-ttu-id="794f0-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` は、**言語と国/地域の基本設定**セクションにタイムゾーン値 **(GMT) 協定世界時** を持つアプリケーション ユーザーによって開始されたプロセス中に呼び出されると、文字列値 **1900-01-01T00:00:00.0000000+00:00** を返します。</span><span class="sxs-lookup"><span data-stu-id="794f0-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="794f0-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="794f0-111">Additional resources</span></span>

[<span data-ttu-id="794f0-112">日時の関数</span><span class="sxs-lookup"><span data-stu-id="794f0-112">Date and time functions</span></span>](er-functions-category-datetime.md)
