---
title: ENDSWITH ER 関数
description: このトピックでは、ENDSWITH 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 1155bb5446f0370d9a5c4b035a767aaeb1d46ee1
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048897"
---
# <a name="endswith-er-function"></a><span data-ttu-id="eb09a-103">ENDSWITH ER 関数</span><span class="sxs-lookup"><span data-stu-id="eb09a-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb09a-104">`ENDSWITH` 関数は、指定された入力が指定されたテキストで終了するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="eb09a-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="eb09a-105">指定された入力が指定されたテキストで終了する場合、 関数は *TRUE* の **ブール値** を返します。</span><span class="sxs-lookup"><span data-stu-id="eb09a-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="eb09a-106">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="eb09a-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb09a-107">構文</span><span class="sxs-lookup"><span data-stu-id="eb09a-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="eb09a-108">引数</span><span class="sxs-lookup"><span data-stu-id="eb09a-108">Arguments</span></span>

<span data-ttu-id="eb09a-109">`input`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="eb09a-109">`input`: *String*</span></span>

<span data-ttu-id="eb09a-110">*文字列* 型または文字列定数のデータ ソースの項目の有効なパスで、2 番目の引数で終わる可能性がある値です。</span><span class="sxs-lookup"><span data-stu-id="eb09a-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="eb09a-111">`start text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="eb09a-111">`start text`: *String*</span></span>

<span data-ttu-id="eb09a-112">*文字列* データ型または文字列定数のデータ ソースの項目の有効なパスで、1 番目の引数で終わる可能性がある値です。</span><span class="sxs-lookup"><span data-stu-id="eb09a-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb09a-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="eb09a-113">Return values</span></span>

<span data-ttu-id="eb09a-114">*ブール値*</span><span class="sxs-lookup"><span data-stu-id="eb09a-114">*Boolean*</span></span>

<span data-ttu-id="eb09a-115">結果 *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="eb09a-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="eb09a-116">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="eb09a-116">Usage notes</span></span>

<span data-ttu-id="eb09a-117">この機能は、[Microsoft Dataverse](/power-platform/admin/data-integrator) にアクセスするための適切なマッピングが [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) で構成されている場合にのみ、[FILTER](er-functions-list-filter.md) 関数の条件式を指定をするのに使用できます。</span><span class="sxs-lookup"><span data-stu-id="eb09a-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="eb09a-118">それ以外の場合は、設計時に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="eb09a-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="eb09a-119">受信するメッセージは、効率を向上させるために、`FILTER` 関数の代わりに [WHERE](er-functions-list-where.md) 関数を使用することを推奨しています。</span><span class="sxs-lookup"><span data-stu-id="eb09a-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="eb09a-120">例 1</span><span class="sxs-lookup"><span data-stu-id="eb09a-120">Example 1</span></span>

<span data-ttu-id="eb09a-121">`ENDSWITH ("abc", "d")` 式は **FALSE** を返し、`ENDSWITH ("abc", "C")` 式は **TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="eb09a-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="eb09a-122">例 2</span><span class="sxs-lookup"><span data-stu-id="eb09a-122">Example 2</span></span>

<span data-ttu-id="eb09a-123">**モデル** データ ソースの **アドレス** フィールドの値が文字列 **USA** で始まる場合、`ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` 式は **TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="eb09a-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="eb09a-124">それ以外の場合、**FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="eb09a-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb09a-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="eb09a-125">Additional resources</span></span>

[<span data-ttu-id="eb09a-126">論理関数</span><span class="sxs-lookup"><span data-stu-id="eb09a-126">Logical functions</span></span>](er-functions-category-logical.md)
