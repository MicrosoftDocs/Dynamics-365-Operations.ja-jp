---
title: FILTER ER 関数
description: このトピックでは、FILTER 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: aa8c0b4601db625d442dd545151968f38bd58cf1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746606"
---
# <a name="filter-er-function"></a><span data-ttu-id="1c1fc-103">FILTER ER 関数</span><span class="sxs-lookup"><span data-stu-id="1c1fc-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c1fc-104">`FILTER` 関数は、クエリが変更された後、指定されたリストを *レコード リスト* 値として返し、指定された条件でフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1fc-105">構文</span><span class="sxs-lookup"><span data-stu-id="1c1fc-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="1c1fc-106">引数</span><span class="sxs-lookup"><span data-stu-id="1c1fc-106">Arguments</span></span>

<span data-ttu-id="1c1fc-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="1c1fc-107">`list`: *Record list*</span></span>

<span data-ttu-id="1c1fc-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="1c1fc-109">`condition`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="1c1fc-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="1c1fc-110">指定されたリストのレコードをフィルター処理するために使用される有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="1c1fc-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="1c1fc-111">Return values</span></span>

<span data-ttu-id="1c1fc-112">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="1c1fc-112">*Record list*</span></span>

<span data-ttu-id="1c1fc-113">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1c1fc-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="1c1fc-114">Usage notes</span></span>

<span data-ttu-id="1c1fc-115">この関数は [WHERE](er-functions-list-where.md) 関数とは異なります。指定された条件がデータベース レベルで *テーブル レコード* タイプの任意の電子申告 (ER) データ ソースに適用されるためです。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="1c1fc-116">テーブルおよび関係を使用して、リストと条件を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="1c1fc-117">この関数に対して構成されている引数 (`list` および `condition`) のいずれかまたは両方がこの要求を SQL の直接呼び出しに変換できない場合、デザイン時に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="1c1fc-118">この例外は、`list` または `condition` のいずれもデータベースのクエリに使用できないことをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="1c1fc-119">例 1</span><span class="sxs-lookup"><span data-stu-id="1c1fc-119">Example 1</span></span>

<span data-ttu-id="1c1fc-120">**仕入先** が VendTable テーブルを参照する ER データ ソースとして構成されている場合、式 `FILTER (Vendors, Vendors.VendGroup = "40")` は仕入先グループ 40 に属している仕入先のみのリストを返します。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="1c1fc-121">例 2</span><span class="sxs-lookup"><span data-stu-id="1c1fc-121">Example 2</span></span>

<span data-ttu-id="1c1fc-122">**仕入先** が VendTable テーブルを参照する ER データ ソースとして構成され、**parmVendorBankGroup** が *文字列* データ型の値を返す ER データ ソースとして構成されている場合、式 `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` が特定の銀行グループに属する仕入先のみの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="1c1fc-123">例 3</span><span class="sxs-lookup"><span data-stu-id="1c1fc-123">Example 3</span></span>

<span data-ttu-id="1c1fc-124">`SPLIT ("A,B,C", ",")` 式を含む *計算済フィールド* タイプの **DS** データ ソースを入力します。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="1c1fc-125">次に、別の式 `FILTER( DS, DS.Value = "B")` を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c1fc-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="1c1fc-126">この式を ER フォーミュラ デザイナーに保存しようとすると、次の例外がスローされます。「検証エラー : FILTER 関数のリスト式はクエリ可能ではありません。」</span><span class="sxs-lookup"><span data-stu-id="1c1fc-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c1fc-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1c1fc-127">Additional resources</span></span>

[<span data-ttu-id="1c1fc-128">リスト機能</span><span class="sxs-lookup"><span data-stu-id="1c1fc-128">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]