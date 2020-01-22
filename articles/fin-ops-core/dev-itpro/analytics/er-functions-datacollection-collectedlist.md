---
title: COLLECTEDLIST ER 関数
description: このトピックでは、COLLECTEDLIST 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 4650cfce76b1c2a66df820fa7660c9c421411343
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916502"
---
# <span data-ttu-id="0d653-103"><a name="COLLECTEDLIST">COLLECTEDLIST ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="0d653-103"><a name="COLLECTEDLIST">COLLECTEDLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d653-104">`COLLECTEDLIST` 関数は、形式要素の**収集されたデータ キー値**プロパティによって返され、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された値のリストを含む*レコード リスト*値を返します。これは指定された条件を満たすものです。</span><span class="sxs-lookup"><span data-stu-id="0d653-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="0d653-105">各条件は、キー範囲とキー値で構成されます。</span><span class="sxs-lookup"><span data-stu-id="0d653-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d653-106">構文</span><span class="sxs-lookup"><span data-stu-id="0d653-106">Syntax</span></span>

```
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="0d653-107">引数</span><span class="sxs-lookup"><span data-stu-id="0d653-107">Arguments</span></span>

<span data-ttu-id="0d653-108">`condition 1 range`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="0d653-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="0d653-109">電子申告 (ER) 形式コンポーネントの**収集したデータ キー名**プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="0d653-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="0d653-110">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="0d653-110">This argument is mandatory.</span></span>

<span data-ttu-id="0d653-111">`condition 1 value`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="0d653-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="0d653-112">ER 形式コンポーネントの**収集したデータ キー値**プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="0d653-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="0d653-113">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="0d653-113">This argument is mandatory.</span></span>

<span data-ttu-id="0d653-114">`condition N range`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="0d653-114">`condition N range`: *String*</span></span>

<span data-ttu-id="0d653-115">ER 形式コンポーネントの**収集したデータ キー名**プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="0d653-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="0d653-116">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="0d653-116">These additional arguments are optional.</span></span>

<span data-ttu-id="0d653-117">`condition N value`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="0d653-117">`condition N value`: *String*</span></span>

<span data-ttu-id="0d653-118">ER 形式コンポーネントの**収集したデータ キー値**プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="0d653-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="0d653-119">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="0d653-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d653-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d653-120">Return values</span></span>

<span data-ttu-id="0d653-121">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="0d653-121">*Record list*</span></span>

<span data-ttu-id="0d653-122">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="0d653-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0d653-123">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="0d653-123">Usage notes</span></span>

<span data-ttu-id="0d653-124">**収集したデータ キー名**および**収集したデータ キー値**プロパティは、ER 形式の**シーケンス** コンポーネントまたは **XML 要素** コンポーネントのいずれかに対してコンフィギュレーションできます。それは**出力の詳細を収集**オプションがオンになっている**共通\\ファイル** コンポーネントの下に存在します。</span><span class="sxs-lookup"><span data-stu-id="0d653-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="0d653-125">この関数は、現在の**共通\\ファイル** コンポーネントの **出力の詳細を収集**オプションを無効にすると、空のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="0d653-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="0d653-126">`condition range` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="0d653-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="0d653-127">`condition value` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="0d653-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="0d653-128">例</span><span class="sxs-lookup"><span data-stu-id="0d653-128">Example</span></span>

<span data-ttu-id="0d653-129">この関数の用途の詳細については、**IT サービス/ソリューション コンポーネントの取得/開発**業務プロセスの一部である [ER 棚卸および集計のために出力された形式の使用](tasks/er-format-counting-summing-1.md) タスク ガイドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d653-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d653-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0d653-130">Additional resources</span></span>

[<span data-ttu-id="0d653-131">データ収集機能</span><span class="sxs-lookup"><span data-stu-id="0d653-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
