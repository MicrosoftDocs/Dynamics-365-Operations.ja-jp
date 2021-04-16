---
title: COUNT ER 関数
description: このトピックでは、COUNT 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746630"
---
# <a name="count-er-function"></a><span data-ttu-id="f5332-103">COUNT ER 関数</span><span class="sxs-lookup"><span data-stu-id="f5332-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5332-104">`COUNT` 関数は、リストが空でない場合に、指定されたリストのレコード数を表す *整数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="f5332-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="f5332-105">リストが空の場合は、この関数は **0** (ゼロ) を返します。</span><span class="sxs-lookup"><span data-stu-id="f5332-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5332-106">構文</span><span class="sxs-lookup"><span data-stu-id="f5332-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="f5332-107">引数</span><span class="sxs-lookup"><span data-stu-id="f5332-107">Arguments</span></span>

<span data-ttu-id="f5332-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="f5332-108">`list`: *Record list*</span></span>

<span data-ttu-id="f5332-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="f5332-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f5332-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="f5332-110">Return values</span></span>

<span data-ttu-id="f5332-111">*整数*</span><span class="sxs-lookup"><span data-stu-id="f5332-111">*Integer*</span></span>

<span data-ttu-id="f5332-112">結果数値。</span><span class="sxs-lookup"><span data-stu-id="f5332-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="f5332-113">例</span><span class="sxs-lookup"><span data-stu-id="f5332-113">Example</span></span>

<span data-ttu-id="f5332-114">この例で使用される `SPLIT` 関数は 2 つのレコードで構成されるリストを作成するため、`COUNT (SPLIT("abcd" , 3))` は、**2** を返します。</span><span class="sxs-lookup"><span data-stu-id="f5332-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5332-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f5332-115">Additional resources</span></span>

[<span data-ttu-id="f5332-116">リスト機能</span><span class="sxs-lookup"><span data-stu-id="f5332-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]