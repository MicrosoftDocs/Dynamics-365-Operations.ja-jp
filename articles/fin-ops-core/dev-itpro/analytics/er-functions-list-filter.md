---
title: FILTER ER 関数
description: このトピックでは、FILTER 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: adeefd08531f59e478efbb45ab294b3bc8216f4c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042161"
---
# <span data-ttu-id="0795e-103"><a name="FILTER">FILTER ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="0795e-103"><a name="FILTER">FILTER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0795e-104">`FILTER` 関数は、クエリが変更された後、指定されたリストを*レコード リスト*値として返し、指定された条件でフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="0795e-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="0795e-105">構文</span><span class="sxs-lookup"><span data-stu-id="0795e-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="0795e-106">引数</span><span class="sxs-lookup"><span data-stu-id="0795e-106">Arguments</span></span>

<span data-ttu-id="0795e-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="0795e-107">`list`: *Record list*</span></span>

<span data-ttu-id="0795e-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="0795e-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0795e-109">`condition`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="0795e-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="0795e-110">指定されたリストのレコードをフィルター処理するために使用される有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="0795e-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="0795e-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="0795e-111">Return values</span></span>

<span data-ttu-id="0795e-112">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="0795e-112">*Record list*</span></span>

<span data-ttu-id="0795e-113">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="0795e-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0795e-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="0795e-114">Usage notes</span></span>

<span data-ttu-id="0795e-115">この関数は [WHERE](er-functions-list-where.md) 関数とは異なります。指定された条件がデータベース レベルで *テーブル レコード* タイプの任意の電子申告 (ER) データ ソースに適用されるためです。</span><span class="sxs-lookup"><span data-stu-id="0795e-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="0795e-116">テーブルおよび関係を使用して、リストと条件を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="0795e-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="0795e-117">この関数に対して構成されている引数 (`list` および `condition`) のいずれかまたは両方がこの要求を SQL の直接呼び出しに変換できない場合、デザイン時に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="0795e-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="0795e-118">この例外は、`list` または `condition` のいずれもデータベースのクエリに使用できないことをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="0795e-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="0795e-119">例 1</span><span class="sxs-lookup"><span data-stu-id="0795e-119">Example 1</span></span>

<span data-ttu-id="0795e-120">**仕入先**が VendTable テーブルを参照する ER データ ソースとして構成されている場合、式 `FILTER (Vendors, Vendors.VendGroup = "40")` は仕入先グループ 40 に属している仕入先のみのリストを返します。</span><span class="sxs-lookup"><span data-stu-id="0795e-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="0795e-121">例 2</span><span class="sxs-lookup"><span data-stu-id="0795e-121">Example 2</span></span>

<span data-ttu-id="0795e-122">**仕入先**が VendTable テーブルを参照する ER データ ソースとして構成され、**parmVendorBankGroup** が*文字列*データ型の値を返す ER データ ソースとして構成されている場合、式 `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` が特定の銀行グループに属する仕入先のみの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="0795e-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="0795e-123">例 3</span><span class="sxs-lookup"><span data-stu-id="0795e-123">Example 3</span></span>

<span data-ttu-id="0795e-124">`SPLIT ("A,B,C", ",")` 式を含む*計算済フィールド* タイプの **DS** データ ソースを入力します。</span><span class="sxs-lookup"><span data-stu-id="0795e-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="0795e-125">次に、別の式 `FILTER( DS, DS.Value = "B")` を入力します。</span><span class="sxs-lookup"><span data-stu-id="0795e-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="0795e-126">この式を ER フォーミュラ デザイナーに保存しようとすると、次の例外がスローされます。「検証エラー : FILTER 関数のリスト式はクエリ可能ではありません。」</span><span class="sxs-lookup"><span data-stu-id="0795e-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0795e-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0795e-127">Additional resources</span></span>

[<span data-ttu-id="0795e-128">リスト機能</span><span class="sxs-lookup"><span data-stu-id="0795e-128">List functions</span></span>](er-functions-category-list.md)
