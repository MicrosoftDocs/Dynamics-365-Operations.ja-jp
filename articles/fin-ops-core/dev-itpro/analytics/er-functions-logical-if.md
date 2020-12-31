---
title: IF ER 関数
description: このトピックでは、IF 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687005"
---
# <a name="if-er-function"></a><span data-ttu-id="f24a2-103">IF ER 関数</span><span class="sxs-lookup"><span data-stu-id="f24a2-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f24a2-104">`IF` 関数は、指定された条件が満たされている場合、最初に指定された値を返します。</span><span class="sxs-lookup"><span data-stu-id="f24a2-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="f24a2-105">それ以外の場合、2 つ目に指定された値を返します。</span><span class="sxs-lookup"><span data-stu-id="f24a2-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="f24a2-106">返される値は、サポートされているいずれかのデータ型の値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f24a2-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="f24a2-107">構文</span><span class="sxs-lookup"><span data-stu-id="f24a2-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="f24a2-108">引数</span><span class="sxs-lookup"><span data-stu-id="f24a2-108">Arguments</span></span>

<span data-ttu-id="f24a2-109">`condition`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="f24a2-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="f24a2-110">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="f24a2-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="f24a2-111">`first value`: *サポートされているいずれかのデータ型*</span><span class="sxs-lookup"><span data-stu-id="f24a2-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="f24a2-112">条件が満たされた場合に返される結果。</span><span class="sxs-lookup"><span data-stu-id="f24a2-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="f24a2-113">`second value`: *サポートされているいずれかのデータ型*</span><span class="sxs-lookup"><span data-stu-id="f24a2-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="f24a2-114">条件が満たされていない場合に返される結果。</span><span class="sxs-lookup"><span data-stu-id="f24a2-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="f24a2-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="f24a2-115">Return values</span></span>

<span data-ttu-id="f24a2-116">*サポートされているいずれかのデータ型*</span><span class="sxs-lookup"><span data-stu-id="f24a2-116">*Any of the supported data types*</span></span>

<span data-ttu-id="f24a2-117">サポートされているいずれかのデータ型の結果値。</span><span class="sxs-lookup"><span data-stu-id="f24a2-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f24a2-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="f24a2-118">Usage notes</span></span>

<span data-ttu-id="f24a2-119">`first value` および `second value` 引数 は、同じデータ型を使用して指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f24a2-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="f24a2-120">構成された値のデータ型が一致しない場合は、デザイン時に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="f24a2-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="f24a2-121">最初の結果値と 2 番目の結果値が *コンテナー (レコード)* または *レコード リスト* データ型の値である場合、結果には両方の値に存在するフィールドのみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f24a2-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="f24a2-122">例</span><span class="sxs-lookup"><span data-stu-id="f24a2-122">Example</span></span>

<span data-ttu-id="f24a2-123">`IF (1=2, "condition is met", "condition is not met")` は、文字列 **"条件を満たしていない"** を返します。</span><span class="sxs-lookup"><span data-stu-id="f24a2-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f24a2-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f24a2-124">Additional resources</span></span>

[<span data-ttu-id="f24a2-125">論理機能</span><span class="sxs-lookup"><span data-stu-id="f24a2-125">Logical functions</span></span>](er-functions-category-logical.md)
