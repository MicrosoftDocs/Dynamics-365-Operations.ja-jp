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
ms.openlocfilehash: 1a21140e5636ebd96eca4be90308c915e77510e1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743906"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="ac30f-103">CONCATENATE ER 機能</span><span class="sxs-lookup"><span data-stu-id="ac30f-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac30f-104">`CONCATENATE` 関数は、一つの文字列に結合された後、*文字列*値として指定されたすべてのテキスト文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ac30f-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac30f-105">構文</span><span class="sxs-lookup"><span data-stu-id="ac30f-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="ac30f-106">引数</span><span class="sxs-lookup"><span data-stu-id="ac30f-106">Arguments</span></span>

<span data-ttu-id="ac30f-107">`text 1`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="ac30f-107">`text 1`: *String*</span></span>

<span data-ttu-id="ac30f-108">*文字列*データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="ac30f-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="ac30f-109">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="ac30f-109">This argument is required.</span></span>

<span data-ttu-id="ac30f-110">`text N`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="ac30f-110">`text N`: *String*</span></span>

<span data-ttu-id="ac30f-111">*文字列*データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="ac30f-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="ac30f-112">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="ac30f-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="ac30f-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="ac30f-113">Return values</span></span>

<span data-ttu-id="ac30f-114">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ac30f-114">*String*</span></span>

<span data-ttu-id="ac30f-115">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="ac30f-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ac30f-116">例</span><span class="sxs-lookup"><span data-stu-id="ac30f-116">Example</span></span>

<span data-ttu-id="ac30f-117">`CONCATENATE ("abc", "def")`" は、**abcdef" を返します**。</span><span class="sxs-lookup"><span data-stu-id="ac30f-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ac30f-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="ac30f-118">Usage notes</span></span>

<span data-ttu-id="ac30f-119">式 `"abc" & "def"` も、**"abcdef"** を返します。</span><span class="sxs-lookup"><span data-stu-id="ac30f-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac30f-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ac30f-120">Additional resources</span></span>

[<span data-ttu-id="ac30f-121">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="ac30f-121">Text functions</span></span>](er-functions-category-text.md)
