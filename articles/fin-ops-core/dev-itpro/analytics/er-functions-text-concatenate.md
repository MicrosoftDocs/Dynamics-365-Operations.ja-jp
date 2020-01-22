---
title: CONCATENATE ER 機能
description: このトピックでは、CONCATENATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915766"
---
# <span data-ttu-id="4df87-103"><a name="CONCATENATE">CONCATENATE ER 機能</a></span><span class="sxs-lookup"><span data-stu-id="4df87-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4df87-104">`CONCATENATE` 関数は、一つの文字列に結合された後、*文字列*値として指定されたすべてのテキスト文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4df87-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df87-105">構文</span><span class="sxs-lookup"><span data-stu-id="4df87-105">Syntax</span></span>

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="4df87-106">引数</span><span class="sxs-lookup"><span data-stu-id="4df87-106">Arguments</span></span>

<span data-ttu-id="4df87-107">`text 1`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="4df87-107">`text 1`: *String*</span></span>

<span data-ttu-id="4df87-108">*文字列*データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="4df87-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="4df87-109">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="4df87-109">This argument is required.</span></span>

<span data-ttu-id="4df87-110">`text N`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="4df87-110">`text N`: *String*</span></span>

<span data-ttu-id="4df87-111">*文字列*データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="4df87-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="4df87-112">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="4df87-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4df87-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="4df87-113">Return values</span></span>

<span data-ttu-id="4df87-114">*文字列*</span><span class="sxs-lookup"><span data-stu-id="4df87-114">*String*</span></span>

<span data-ttu-id="4df87-115">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="4df87-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4df87-116">例</span><span class="sxs-lookup"><span data-stu-id="4df87-116">Example</span></span>

<span data-ttu-id="4df87-117">`CONCATENATE ("abc", "def")`" は、**abcdef" を返します**。</span><span class="sxs-lookup"><span data-stu-id="4df87-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4df87-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="4df87-118">Usage notes</span></span>

<span data-ttu-id="4df87-119">式 `"abc" & "def"` も、**"abcdef"** を返します。</span><span class="sxs-lookup"><span data-stu-id="4df87-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4df87-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4df87-120">Additional resources</span></span>

[<span data-ttu-id="4df87-121">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="4df87-121">Text functions</span></span>](er-functions-category-text.md)
