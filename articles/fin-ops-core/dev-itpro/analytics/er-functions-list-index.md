---
title: INDEX ER 関数
description: このトピックでは、INDEX 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745181"
---
# <a name="index-er-function"></a><span data-ttu-id="afa1d-103">INDEX ER 関数</span><span class="sxs-lookup"><span data-stu-id="afa1d-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afa1d-104">`INDEX` 関数は、指定されたリストの指定された数値インデックスを使用して選択された*コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="afa1d-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="afa1d-105">インデックスが指定されたリスト内のレコードの範囲外である場合は、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="afa1d-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa1d-106">構文</span><span class="sxs-lookup"><span data-stu-id="afa1d-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="afa1d-107">引数</span><span class="sxs-lookup"><span data-stu-id="afa1d-107">Arguments</span></span>

<span data-ttu-id="afa1d-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="afa1d-108">`list`: *Record list*</span></span>

<span data-ttu-id="afa1d-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="afa1d-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="afa1d-110">`index`: *整数*</span><span class="sxs-lookup"><span data-stu-id="afa1d-110">`index`: *Integer*</span></span>

<span data-ttu-id="afa1d-111">指定したリスト内の目的のレコードの位置を示す数値インデックス。</span><span class="sxs-lookup"><span data-stu-id="afa1d-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="afa1d-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="afa1d-112">Return values</span></span>

<span data-ttu-id="afa1d-113">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="afa1d-113">*Container (record)*</span></span>

<span data-ttu-id="afa1d-114">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="afa1d-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="afa1d-115">例 1</span><span class="sxs-lookup"><span data-stu-id="afa1d-115">Example 1</span></span>

<span data-ttu-id="afa1d-116">*計算済フィールド* タイプのデータ ソース **DS** を入力していて、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `DS.Value` は、このレコード リストの 2 番目のレコードのテキスト値 **"B"** を返します。</span><span class="sxs-lookup"><span data-stu-id="afa1d-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="afa1d-117">式 `INDEX (SPLIT ("A|B|C", "|"), 2).Value` もテキスト値 **"B"** を返します。</span><span class="sxs-lookup"><span data-stu-id="afa1d-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="afa1d-118">例 2</span><span class="sxs-lookup"><span data-stu-id="afa1d-118">Example 2</span></span>

<span data-ttu-id="afa1d-119">*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `INDEX (SPLIT ("A|B|C", "|"), 4).Value` は実行時に例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="afa1d-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="afa1d-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="afa1d-120">Additional resources</span></span>

[<span data-ttu-id="afa1d-121">リスト機能</span><span class="sxs-lookup"><span data-stu-id="afa1d-121">List functions</span></span>](er-functions-category-list.md)
