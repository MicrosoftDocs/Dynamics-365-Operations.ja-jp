---
title: 論理カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされる論理関数について説明します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916640"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="85e81-103">論理カテゴリ内の ER 関数のリスト</span><span class="sxs-lookup"><span data-stu-id="85e81-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85e81-104">電子レポート (ER) 論理関数を使用して、論理値を操作して単一の式で複数の比較を実行したり、複数の条件をテストしたりできます。</span><span class="sxs-lookup"><span data-stu-id="85e81-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="85e81-105">このトピックでは、これらの関数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="85e81-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="85e81-106">サポートされている関数のリスト</span><span class="sxs-lookup"><span data-stu-id="85e81-106">List of supported functions</span></span>

| <span data-ttu-id="85e81-107">職務</span><span class="sxs-lookup"><span data-stu-id="85e81-107">Function</span></span> | <span data-ttu-id="85e81-108">説明</span><span class="sxs-lookup"><span data-stu-id="85e81-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="85e81-109">かつ</span><span class="sxs-lookup"><span data-stu-id="85e81-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="85e81-110">この関数は、指定したすべての条件が true である場合、**TRUE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="85e81-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="85e81-111">それ以外の場合は、**FALSE** の*ブール*値が返されます。</span><span class="sxs-lookup"><span data-stu-id="85e81-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="85e81-112">ケース</span><span class="sxs-lookup"><span data-stu-id="85e81-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="85e81-113">この関数は、指定された代替オプションに対して指定された式の値を評価し、指定された式の値に等しい最初のオプションの結果を返します。</span><span class="sxs-lookup"><span data-stu-id="85e81-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="85e81-114">それ以外の場合は、オプションの前にはない、呼び出された関数の最後の引数としてデフォルト結果が指定されている場合、オプションのデフォルト結果を返します。</span><span class="sxs-lookup"><span data-stu-id="85e81-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="85e81-115">返される値は、サポートされているいずれかのデータ型の値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="85e81-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="85e81-116">次の場合</span><span class="sxs-lookup"><span data-stu-id="85e81-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="85e81-117">この関数は、特定の条件が満たされている場合、最初に指定された値を返します。</span><span class="sxs-lookup"><span data-stu-id="85e81-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="85e81-118">それ以外の場合、2 つ目に指定された値を返します。</span><span class="sxs-lookup"><span data-stu-id="85e81-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="85e81-119">返される値は、サポートされているいずれかのデータ型の値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="85e81-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="85e81-120">ない</span><span class="sxs-lookup"><span data-stu-id="85e81-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="85e81-121">この関数は、指定された条件の取消論理値を*ブール*値として返します。</span><span class="sxs-lookup"><span data-stu-id="85e81-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="85e81-122">Or</span><span class="sxs-lookup"><span data-stu-id="85e81-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="85e81-123">この関数は、指定したすべての条件が false である場合、**FALSE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="85e81-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="85e81-124">指定した任意の条件が true である場合、関数は **TRUE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="85e81-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="85e81-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="85e81-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="85e81-126">この関数は指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="85e81-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="85e81-127">指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="85e81-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="85e81-128">それ以外の場合は、**FALSE** の*ブール*値が返されます。</span><span class="sxs-lookup"><span data-stu-id="85e81-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="85e81-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="85e81-129">Additional resources</span></span>

[<span data-ttu-id="85e81-130">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="85e81-130">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="85e81-131">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="85e81-131">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="85e81-132">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="85e81-132">Electronic reporting formula language</span></span>](er-formula-language.md)
