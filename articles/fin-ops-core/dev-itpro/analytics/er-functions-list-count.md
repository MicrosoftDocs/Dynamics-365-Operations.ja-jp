---
title: COUNT ER 関数
description: このトピックでは、COUNT 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: c48483a6677aaeb36eac57a57cec71bf54c7991d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745348"
---
# <a name="count-er-function"></a><span data-ttu-id="2e110-103">COUNT ER 関数</span><span class="sxs-lookup"><span data-stu-id="2e110-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e110-104">`COUNT` 関数は、リストが空でない場合に、指定されたリストのレコード数を表す*整数*値を返します。</span><span class="sxs-lookup"><span data-stu-id="2e110-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="2e110-105">リストが空の場合は、この関数は **0** (ゼロ) を返します。</span><span class="sxs-lookup"><span data-stu-id="2e110-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e110-106">構文</span><span class="sxs-lookup"><span data-stu-id="2e110-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="2e110-107">引数</span><span class="sxs-lookup"><span data-stu-id="2e110-107">Arguments</span></span>

<span data-ttu-id="2e110-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="2e110-108">`list`: *Record list*</span></span>

<span data-ttu-id="2e110-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="2e110-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2e110-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="2e110-110">Return values</span></span>

<span data-ttu-id="2e110-111">*整数*</span><span class="sxs-lookup"><span data-stu-id="2e110-111">*Integer*</span></span>

<span data-ttu-id="2e110-112">結果数値。</span><span class="sxs-lookup"><span data-stu-id="2e110-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="2e110-113">例</span><span class="sxs-lookup"><span data-stu-id="2e110-113">Example</span></span>

<span data-ttu-id="2e110-114">この例で使用される `SPLIT` 関数は 2 つのレコードで構成されるリストを作成するため、`COUNT (SPLIT("abcd" , 3))` は、**2** を返します。</span><span class="sxs-lookup"><span data-stu-id="2e110-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e110-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2e110-115">Additional resources</span></span>

[<span data-ttu-id="2e110-116">リスト機能</span><span class="sxs-lookup"><span data-stu-id="2e110-116">List functions</span></span>](er-functions-category-list.md)
