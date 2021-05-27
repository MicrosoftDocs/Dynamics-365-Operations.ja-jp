---
title: CONTAINS ER 関数
description: このトピックでは、CONTAINS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: a31d89f036a6e821bea2b6733c0c646145d2a47c
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048873"
---
# <a name="contains-er-function"></a><span data-ttu-id="14ac6-103">CONTAINS ER 関数</span><span class="sxs-lookup"><span data-stu-id="14ac6-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14ac6-104">`CONTAINS` 関数は、指定された入力に指定されたテキストが含まれるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="14ac6-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="14ac6-105">指定された入力が指定されたテキストを含む場合、関数は *TRUE* の **ブール値** を返します。</span><span class="sxs-lookup"><span data-stu-id="14ac6-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="14ac6-106">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="14ac6-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ac6-107">構文</span><span class="sxs-lookup"><span data-stu-id="14ac6-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="14ac6-108">引数</span><span class="sxs-lookup"><span data-stu-id="14ac6-108">Arguments</span></span>

<span data-ttu-id="14ac6-109">`input`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="14ac6-109">`input`: *String*</span></span>

<span data-ttu-id="14ac6-110">*文字列* 型または文字列定数のデータ ソースの項目の有効なパスで、2 番目の引数を含む可能性がある値です。</span><span class="sxs-lookup"><span data-stu-id="14ac6-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="14ac6-111">`search text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="14ac6-111">`search text`: *String*</span></span>

<span data-ttu-id="14ac6-112">*文字列* データ型または文字列定数のデータ ソースの項目の有効なパスで、1 番目の引数を含む可能性がある値です。</span><span class="sxs-lookup"><span data-stu-id="14ac6-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="14ac6-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="14ac6-113">Return values</span></span>

<span data-ttu-id="14ac6-114">*ブール値*</span><span class="sxs-lookup"><span data-stu-id="14ac6-114">*Boolean*</span></span>

<span data-ttu-id="14ac6-115">結果 *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="14ac6-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="14ac6-116">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="14ac6-116">Usage notes</span></span>

<span data-ttu-id="14ac6-117">この機能は、[Microsoft Dataverse](/power-platform/admin/data-integrator) にアクセスするための適切なマッピングが [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) で構成されている場合にのみ、[FILTER](er-functions-list-filter.md) 関数の条件式を指定をするのに使用できます。</span><span class="sxs-lookup"><span data-stu-id="14ac6-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="14ac6-118">それ以外の場合は、設計時に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="14ac6-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="14ac6-119">受信するメッセージは、効率を向上させるために、`FILTER` 関数の代わりに [WHERE](er-functions-list-where.md) 関数を使用することを推奨しています。</span><span class="sxs-lookup"><span data-stu-id="14ac6-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="14ac6-120">例 1</span><span class="sxs-lookup"><span data-stu-id="14ac6-120">Example 1</span></span>

<span data-ttu-id="14ac6-121">`CONTAINS ("abc", "d")` 式は **FALSE** を返し、`CONTAINS ("abc", "C")` 式は **TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="14ac6-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="14ac6-122">例 2</span><span class="sxs-lookup"><span data-stu-id="14ac6-122">Example 2</span></span>

<span data-ttu-id="14ac6-123">**モデル** データ ソースの **アドレス** フィールドの値が文字列 **DEU** を含む場合、`CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` 式は **TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="14ac6-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="14ac6-124">それ以外の場合、**FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="14ac6-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14ac6-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="14ac6-125">Additional resources</span></span>

[<span data-ttu-id="14ac6-126">論理関数</span><span class="sxs-lookup"><span data-stu-id="14ac6-126">Logical functions</span></span>](er-functions-category-logical.md)
