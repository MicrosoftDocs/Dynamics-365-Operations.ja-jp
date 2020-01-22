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
ms.openlocfilehash: a7fe2cbb5421da3c6dd1d044316b276836c5e5c1
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917307"
---
# <span data-ttu-id="810f3-103"><a name="INDEX">INDEX ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="810f3-103"><a name="INDEX">INDEX ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="810f3-104">`INDEX` 関数は、指定されたリストの指定された数値インデックスを使用して選択された*コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="810f3-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="810f3-105">インデックスが指定されたリスト内のレコードの範囲外である場合は、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="810f3-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="810f3-106">構文</span><span class="sxs-lookup"><span data-stu-id="810f3-106">Syntax</span></span>

```
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="810f3-107">引数</span><span class="sxs-lookup"><span data-stu-id="810f3-107">Arguments</span></span>

<span data-ttu-id="810f3-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="810f3-108">`list`: *Record list*</span></span>

<span data-ttu-id="810f3-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="810f3-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="810f3-110">`index`: *整数*</span><span class="sxs-lookup"><span data-stu-id="810f3-110">`index`: *Integer*</span></span>

<span data-ttu-id="810f3-111">指定したリスト内の目的のレコードの位置を示す数値インデックス。</span><span class="sxs-lookup"><span data-stu-id="810f3-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="810f3-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="810f3-112">Return values</span></span>

<span data-ttu-id="810f3-113">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="810f3-113">*Container (record)*</span></span>

<span data-ttu-id="810f3-114">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="810f3-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="810f3-115">例 1</span><span class="sxs-lookup"><span data-stu-id="810f3-115">Example 1</span></span>

<span data-ttu-id="810f3-116">*計算済フィールド* タイプのデータ ソース **DS** を入力していて、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `DS.Value` は、このレコード リストの 2 番目のレコードのテキスト値 **"B"** を返します。</span><span class="sxs-lookup"><span data-stu-id="810f3-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="810f3-117">式 `INDEX (SPLIT ("A|B|C", "|"), 2).Value` もテキスト値 **"B"** を返します。</span><span class="sxs-lookup"><span data-stu-id="810f3-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="810f3-118">例 2</span><span class="sxs-lookup"><span data-stu-id="810f3-118">Example 2</span></span>

<span data-ttu-id="810f3-119">*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `INDEX (SPLIT ("A|B|C", "|"), 4).Value` は実行時に例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="810f3-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="810f3-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="810f3-120">Additional resources</span></span>

[<span data-ttu-id="810f3-121">リスト機能</span><span class="sxs-lookup"><span data-stu-id="810f3-121">List functions</span></span>](er-functions-category-list.md)
