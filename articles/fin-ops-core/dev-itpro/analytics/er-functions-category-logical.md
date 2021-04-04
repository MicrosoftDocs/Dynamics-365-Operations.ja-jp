---
title: 論理カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされる論理関数について説明します。
author: NickSelin
manager: kfend
ms.date: 02/11/2021
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
ms.openlocfilehash: 7310c2b269c3f4be03102160aebe0ed164a23a5c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561665"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="0a4c3-103">論理カテゴリ内の ER 関数のリスト</span><span class="sxs-lookup"><span data-stu-id="0a4c3-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a4c3-104">電子レポート (ER) 論理関数を使用して、論理値を操作して単一の式で複数の比較を実行したり、複数の条件をテストしたりできます。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="0a4c3-105">このトピックでは、これらの関数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="0a4c3-106">サポートされている関数のリスト</span><span class="sxs-lookup"><span data-stu-id="0a4c3-106">List of supported functions</span></span>

| <span data-ttu-id="0a4c3-107">職務</span><span class="sxs-lookup"><span data-stu-id="0a4c3-107">Function</span></span> | <span data-ttu-id="0a4c3-108">説明</span><span class="sxs-lookup"><span data-stu-id="0a4c3-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="0a4c3-109">かつ</span><span class="sxs-lookup"><span data-stu-id="0a4c3-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="0a4c3-110">この関数は、指定したすべての条件が true である場合、**TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="0a4c3-111">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="0a4c3-112">ケース</span><span class="sxs-lookup"><span data-stu-id="0a4c3-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="0a4c3-113">この関数は、指定された代替オプションに対して指定された式の値を評価し、指定された式の値に等しい最初のオプションの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="0a4c3-114">それ以外の場合は、オプションの前にはない、呼び出された関数の最後の引数としてデフォルト結果が指定されている場合、オプションのデフォルト結果を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="0a4c3-115">返される値は、サポートされているいずれかのデータ型の値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="0a4c3-116">次の値を含む</span><span class="sxs-lookup"><span data-stu-id="0a4c3-116">Contains</span></span>](er-functions-logical-contains.md)             | <span data-ttu-id="0a4c3-117">この関数は、指定された入力に指定されたテキストが含まれるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-117">This function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="0a4c3-118">指定された入力が指定されたテキストを含む場合、関数は *TRUE* の **ブール値** を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-118">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="0a4c3-119">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-119">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="0a4c3-120">EndsWith</span><span class="sxs-lookup"><span data-stu-id="0a4c3-120">EndsWith</span></span>](er-functions-logical-endswith.md)             | <span data-ttu-id="0a4c3-121">この関数は、指定された入力が指定されたテキストで終了するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-121">This function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="0a4c3-122">指定された入力が指定されたテキストで終了する場合、 関数は *TRUE* の **ブール値** を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-122">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="0a4c3-123">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-123">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="0a4c3-124">次の場合</span><span class="sxs-lookup"><span data-stu-id="0a4c3-124">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="0a4c3-125">この関数は、特定の条件が満たされている場合、最初に指定された値を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-125">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="0a4c3-126">それ以外の場合、2 つ目に指定された値を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-126">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="0a4c3-127">返される値は、サポートされているいずれかのデータ型の値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-127">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="0a4c3-128">ない</span><span class="sxs-lookup"><span data-stu-id="0a4c3-128">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="0a4c3-129">この関数は、指定された条件の取消論理値を *ブール* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-129">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="0a4c3-130">Or</span><span class="sxs-lookup"><span data-stu-id="0a4c3-130">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="0a4c3-131">この関数は、指定したすべての条件が false である場合、**FALSE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-131">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="0a4c3-132">指定した任意の条件が true である場合、関数は **TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-132">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="0a4c3-133">StartsWith</span><span class="sxs-lookup"><span data-stu-id="0a4c3-133">StartsWith</span></span>](er-functions-logical-startswith.md)         | <span data-ttu-id="0a4c3-134">この関数は、指定された入力が指定されたテキストで始まるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-134">This function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="0a4c3-135">指定された入力が指定されたテキストで始まる場合、 関数は *TRUE* の **ブール値** を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-135">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="0a4c3-136">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-136">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="0a4c3-137">ValueIn</span><span class="sxs-lookup"><span data-stu-id="0a4c3-137">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="0a4c3-138">この関数は指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-138">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="0a4c3-139">指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-139">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="0a4c3-140">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-140">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="0a4c3-141">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="0a4c3-141">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="0a4c3-142">この関数は、*Int64* あるいは *整数* タイプの指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-142">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="0a4c3-143">指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-143">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="0a4c3-144">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0a4c3-144">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="0a4c3-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0a4c3-145">Additional resources</span></span>

[<span data-ttu-id="0a4c3-146">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="0a4c3-146">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="0a4c3-147">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="0a4c3-147">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="0a4c3-148">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="0a4c3-148">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]