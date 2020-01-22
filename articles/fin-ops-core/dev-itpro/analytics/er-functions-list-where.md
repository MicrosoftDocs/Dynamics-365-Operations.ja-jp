---
title: WHERE ER 関数
description: このトピックでは、WHERE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 50d90697f522f3c4d7b62190928008b6d923ffc6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916088"
---
# <span data-ttu-id="9bbb8-103"><a name="WHERE">WHERE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="9bbb8-103"><a name="WHERE">WHERE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bbb8-104">`WHERE` 関数は、指定されたリストを、指定された条件に基づいてフィルタリングされた後に*レコード リスト*値として返します。</span><span class="sxs-lookup"><span data-stu-id="9bbb8-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bbb8-105">構文</span><span class="sxs-lookup"><span data-stu-id="9bbb8-105">Syntax</span></span>

```
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="9bbb8-106">引数</span><span class="sxs-lookup"><span data-stu-id="9bbb8-106">Arguments</span></span>

<span data-ttu-id="9bbb8-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="9bbb8-107">`list`: *Record list*</span></span>

<span data-ttu-id="9bbb8-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="9bbb8-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9bbb8-109">`condition`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="9bbb8-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="9bbb8-110">指定されたリストのレコードをフィルター処理するために使用される有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="9bbb8-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="9bbb8-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="9bbb8-111">Return values</span></span>

<span data-ttu-id="9bbb8-112">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="9bbb8-112">*Record list*</span></span>

<span data-ttu-id="9bbb8-113">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="9bbb8-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9bbb8-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="9bbb8-114">Usage notes</span></span>

<span data-ttu-id="9bbb8-115">この関数は [FILTER](er-functions-list-filter.md) 関数とは異なります。指定された条件がメモリに存在する*レコード リスト* タイプの任意の電子申告 (ER) データ ソースに適用されるためです。</span><span class="sxs-lookup"><span data-stu-id="9bbb8-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="9bbb8-116">この関数に対して構成されている引数 (`list` および `condition`) がこの要求を SQL の直接呼び出しに変換できる場合、デザイン時に警告メッセージがスローされます。</span><span class="sxs-lookup"><span data-stu-id="9bbb8-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="9bbb8-117">このメッセージは、`WHERE` 関数の代わりに [FILTER](er-functions-list-filter.md) 関数が使用された場合にパフォーマンスが向上する可能性があることをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="9bbb8-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="9bbb8-118">例 1</span><span class="sxs-lookup"><span data-stu-id="9bbb8-118">Example 1</span></span>

<span data-ttu-id="9bbb8-119">**仕入先**が VendTable テーブルを参照する ER データ ソースとして構成されている場合、式 `WHERE (Vendors, Vendors.VendGroup = "40")` は仕入先グループ 40 に属している仕入先のみのリストを返します。</span><span class="sxs-lookup"><span data-stu-id="9bbb8-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="9bbb8-120">例 2</span><span class="sxs-lookup"><span data-stu-id="9bbb8-120">Example 2</span></span>

<span data-ttu-id="9bbb8-121">*計算済フィールド* タイプのデータ ソース **DS** を入力していて、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `WHERE( DS, DS.Value = "B")` は、**値**フィールドにテキスト **"B"** を含む 1 つのレコードのみのリストを返します。</span><span class="sxs-lookup"><span data-stu-id="9bbb8-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bbb8-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9bbb8-122">Additional resources</span></span>

[<span data-ttu-id="9bbb8-123">リスト機能</span><span class="sxs-lookup"><span data-stu-id="9bbb8-123">List functions</span></span>](er-functions-category-list.md)
