---
title: INDEX ER 関数
description: このトピックでは、INDEX 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087754"
---
# <a name="index-er-function"></a><span data-ttu-id="272d3-103">INDEX ER 関数</span><span class="sxs-lookup"><span data-stu-id="272d3-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="272d3-104">`INDEX` 関数は、指定されたリストの指定された数値インデックスを使用して選択された *コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="272d3-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="272d3-105">インデックスが指定されたリスト内のレコードの範囲外である場合は、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="272d3-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="272d3-106">構文</span><span class="sxs-lookup"><span data-stu-id="272d3-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="272d3-107">引数</span><span class="sxs-lookup"><span data-stu-id="272d3-107">Arguments</span></span>

<span data-ttu-id="272d3-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="272d3-108">`list`: *Record list*</span></span>

<span data-ttu-id="272d3-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="272d3-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="272d3-110">`index`: *整数*</span><span class="sxs-lookup"><span data-stu-id="272d3-110">`index`: *Integer*</span></span>

<span data-ttu-id="272d3-111">指定したリスト内の目的のレコードの位置を示す数値インデックス。</span><span class="sxs-lookup"><span data-stu-id="272d3-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="272d3-112">この関数では 1 ベースの番号付けを使用しているため、指定したリストの最初のレコードを返すには値 **1** を指定します。</span><span class="sxs-lookup"><span data-stu-id="272d3-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="272d3-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="272d3-113">Return values</span></span>

<span data-ttu-id="272d3-114">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="272d3-114">*Container (record)*</span></span>

<span data-ttu-id="272d3-115">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="272d3-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="272d3-116">例 1</span><span class="sxs-lookup"><span data-stu-id="272d3-116">Example 1</span></span>

<span data-ttu-id="272d3-117">*計算済フィールド* タイプのデータ ソース **DS** を入力していて、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `DS.Value` は、このレコード リストの 2 番目のレコードのテキスト値 **"B"** を返します。</span><span class="sxs-lookup"><span data-stu-id="272d3-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="272d3-118">式 `INDEX (SPLIT ("A|B|C", "|"), 2).Value` もテキスト値 **"B"** を返します。</span><span class="sxs-lookup"><span data-stu-id="272d3-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="272d3-119">例 2</span><span class="sxs-lookup"><span data-stu-id="272d3-119">Example 2</span></span>

<span data-ttu-id="272d3-120">*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `INDEX (SPLIT ("A|B|C", "|"), 4).Value` は実行時に例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="272d3-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="272d3-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="272d3-121">Additional resources</span></span>

[<span data-ttu-id="272d3-122">リスト機能</span><span class="sxs-lookup"><span data-stu-id="272d3-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
