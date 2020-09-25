---
title: FIRST ER 関数
description: このトピックでは、FIRST 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 3ed0e0aaf29e2a67a4842d71121f1adc24f524f7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745228"
---
# <a name="first-er-function"></a><span data-ttu-id="7bb76-103">FIRST ER 関数</span><span class="sxs-lookup"><span data-stu-id="7bb76-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bb76-104">`FIRST` 関数は、リストが空でない場合に、指定されたリストの最初のレコードを*コンテナー (レコード)* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="7bb76-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="7bb76-105">リストが空の場合、この関数は例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="7bb76-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb76-106">構文</span><span class="sxs-lookup"><span data-stu-id="7bb76-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="7bb76-107">引数</span><span class="sxs-lookup"><span data-stu-id="7bb76-107">Arguments</span></span>

<span data-ttu-id="7bb76-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="7bb76-108">`list`: *Record list*</span></span>

<span data-ttu-id="7bb76-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="7bb76-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7bb76-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="7bb76-110">Return values</span></span>

<span data-ttu-id="7bb76-111">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="7bb76-111">*Container (record)*</span></span>

<span data-ttu-id="7bb76-112">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="7bb76-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="7bb76-113">例 1</span><span class="sxs-lookup"><span data-stu-id="7bb76-113">Example 1</span></span>

<span data-ttu-id="7bb76-114">式 `FIRST(SPLIT("ABC",1)).Value` はテキスト値 **"A"** を返します。</span><span class="sxs-lookup"><span data-stu-id="7bb76-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7bb76-115">例 2</span><span class="sxs-lookup"><span data-stu-id="7bb76-115">Example 2</span></span>

<span data-ttu-id="7bb76-116">式 `FIRST(SPLIT("",1)).Value` は、実行時に例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="7bb76-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7bb76-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7bb76-117">Additional resources</span></span>

[<span data-ttu-id="7bb76-118">リスト機能</span><span class="sxs-lookup"><span data-stu-id="7bb76-118">List functions</span></span>](er-functions-category-list.md)
