---
title: REVERSE ER 関数
description: このトピックでは、REVERSE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917238"
---
# <span data-ttu-id="11f06-103"><a name="REVERSE">REVERSE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="11f06-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11f06-104">`REVERSE` 関数は、指定されたリストを、逆の並べ替え順で*レコード リスト*値として返します。</span><span class="sxs-lookup"><span data-stu-id="11f06-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f06-105">構文</span><span class="sxs-lookup"><span data-stu-id="11f06-105">Syntax</span></span>

```
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="11f06-106">引数</span><span class="sxs-lookup"><span data-stu-id="11f06-106">Arguments</span></span>

<span data-ttu-id="11f06-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="11f06-107">`list`: *Record list*</span></span>

<span data-ttu-id="11f06-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="11f06-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="11f06-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="11f06-109">Return values</span></span>

<span data-ttu-id="11f06-110">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="11f06-110">*Record list*</span></span>

<span data-ttu-id="11f06-111">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="11f06-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="11f06-112">例 1</span><span class="sxs-lookup"><span data-stu-id="11f06-112">Example 1</span></span>

<span data-ttu-id="11f06-113">*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("C|B|A", "|")` が含まれている場合、式 `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` はテキスト値 **"C"** を返します。</span><span class="sxs-lookup"><span data-stu-id="11f06-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="11f06-114">例 2</span><span class="sxs-lookup"><span data-stu-id="11f06-114">Example 2</span></span>

<span data-ttu-id="11f06-115">**仕入先**を VendTable テーブルを参照する電子申告 (ER) データ ソースとして構成している場合、式 `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` は降順の名前で並べ替えられた仕入先のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="11f06-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11f06-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="11f06-116">Additional resources</span></span>

[<span data-ttu-id="11f06-117">リスト機能</span><span class="sxs-lookup"><span data-stu-id="11f06-117">List functions</span></span>](er-functions-category-list.md)
