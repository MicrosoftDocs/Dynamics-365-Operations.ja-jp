---
title: ORDERBY ER 関数
description: このトピックでは、ORDERBY 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 0a6b5cddc325625dc5b3d677ffcc1da1f8b829cd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041955"
---
# <span data-ttu-id="1c1aa-103"><a name="ORDERBY">ORDERBY ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="1c1aa-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c1aa-104">`ORDERBY` 関数は、指定されたリストを、指定された引数に基づいて並べ替えられた後に*レコード リスト*値として返します。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="1c1aa-105">これらの引数は、式として定義することができます。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1aa-106">構文</span><span class="sxs-lookup"><span data-stu-id="1c1aa-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="1c1aa-107">引数</span><span class="sxs-lookup"><span data-stu-id="1c1aa-107">Arguments</span></span>

<span data-ttu-id="1c1aa-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="1c1aa-108">`list`: *Record list*</span></span>

<span data-ttu-id="1c1aa-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="1c1aa-110">`expression 1`: *フィールド*</span><span class="sxs-lookup"><span data-stu-id="1c1aa-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="1c1aa-111">呼び出された関数の `list` 引数によって参照されるデータ ソースのフィールドの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="1c1aa-112">参照フィールドは、プリミティブ データ型のフィールドである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="1c1aa-113">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-113">This argument is required.</span></span>

<span data-ttu-id="1c1aa-114">`expression N`: *フィールド*</span><span class="sxs-lookup"><span data-stu-id="1c1aa-114">`expression N`: *Field*</span></span>

<span data-ttu-id="1c1aa-115">呼び出された関数の `list` 引数によって参照されるデータ ソースのフィールドの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="1c1aa-116">参照フィールドは、プリミティブ データ型のフィールドである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="1c1aa-117">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1c1aa-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="1c1aa-118">Return values</span></span>

<span data-ttu-id="1c1aa-119">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="1c1aa-119">*Record list*</span></span>

<span data-ttu-id="1c1aa-120">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="1c1aa-121">例 1</span><span class="sxs-lookup"><span data-stu-id="1c1aa-121">Example 1</span></span>

<span data-ttu-id="1c1aa-122">*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("C|B|A", "|")` が含まれている場合、式 `FIRST( ORDERBY( DS, DS. Value)).Value` はテキスト値 **"A"** を返します。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1c1aa-123">例 2</span><span class="sxs-lookup"><span data-stu-id="1c1aa-123">Example 2</span></span>

<span data-ttu-id="1c1aa-124">**仕入先**を VendTable テーブルを参照する電子申告 (ER) データ ソースとして構成している場合、式 `ORDERBY (Vendors, Vendors.'name()')` は昇順の名前で並べ替えられた仕入先のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="1c1aa-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c1aa-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1c1aa-125">Additional resources</span></span>

[<span data-ttu-id="1c1aa-126">リスト機能</span><span class="sxs-lookup"><span data-stu-id="1c1aa-126">List functions</span></span>](er-functions-category-list.md)
