---
title: COUNTIFS ER 関数
description: このトピックでは、COUNTIFS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 667002aa01537f846c616d38bba436da18f6e05f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755279"
---
# <a name="countifs-er-function"></a><span data-ttu-id="30415-103">COUNTIFS ER 関数</span><span class="sxs-lookup"><span data-stu-id="30415-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30415-104">`COUNTIFS` 関数は、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された、形式要素の数を表す *整数* 値を返します。これは指定された条件を満たすものです。</span><span class="sxs-lookup"><span data-stu-id="30415-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="30415-105">各条件は、キー範囲とキー値で構成されます。</span><span class="sxs-lookup"><span data-stu-id="30415-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="30415-106">構文</span><span class="sxs-lookup"><span data-stu-id="30415-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="30415-107">引数</span><span class="sxs-lookup"><span data-stu-id="30415-107">Arguments</span></span>

<span data-ttu-id="30415-108">`condition 1 range`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="30415-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="30415-109">電子申告 (ER) 形式コンポーネントの **収集したデータ キー名** プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="30415-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="30415-110">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="30415-110">This argument is mandatory.</span></span>

<span data-ttu-id="30415-111">`condition 1 value`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="30415-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="30415-112">ER 形式コンポーネントの **収集したデータ キー値** プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="30415-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="30415-113">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="30415-113">This argument is mandatory.</span></span>

<span data-ttu-id="30415-114">`condition N range`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="30415-114">`condition N range`: *String*</span></span>

<span data-ttu-id="30415-115">ER 形式コンポーネントの **収集したデータ キー名** プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="30415-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="30415-116">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="30415-116">These additional arguments are optional.</span></span>

<span data-ttu-id="30415-117">`condition N value`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="30415-117">`condition N value`: *String*</span></span>

<span data-ttu-id="30415-118">ER 形式コンポーネントの **収集したデータ キー値** プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="30415-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="30415-119">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="30415-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="30415-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="30415-120">Return values</span></span>

<span data-ttu-id="30415-121">*整数*</span><span class="sxs-lookup"><span data-stu-id="30415-121">*Integer*</span></span>

<span data-ttu-id="30415-122">結果数値。</span><span class="sxs-lookup"><span data-stu-id="30415-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="30415-123">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="30415-123">Usage notes</span></span>

<span data-ttu-id="30415-124">**収集したデータ キー名** および **収集したデータ キー値** プロパティは、ER 形式の **シーケンス** コンポーネントまたは **XML 要素** コンポーネントのいずれかに対してコンフィギュレーションできます。それは **出力の詳細を収集** オプションがオンになっている **共通\\ファイル** コンポーネントの下に存在します。</span><span class="sxs-lookup"><span data-stu-id="30415-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="30415-125">この関数は、現在の **共通\\ファイル** コンポーネントの **出力の詳細を収集** オプションを無効にすると、**0** (ゼロ) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="30415-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="30415-126">`condition range` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="30415-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="30415-127">`condition value` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="30415-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="30415-128">例</span><span class="sxs-lookup"><span data-stu-id="30415-128">Example</span></span>

<span data-ttu-id="30415-129">この関数の用途の詳細については、**IT サービス/ソリューション コンポーネントの取得/開発** 業務プロセスの一部である [ER 棚卸および集計のために出力された形式の使用](tasks/er-format-counting-summing-1.md) タスク ガイドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="30415-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30415-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="30415-130">Additional resources</span></span>

[<span data-ttu-id="30415-131">データ収集機能</span><span class="sxs-lookup"><span data-stu-id="30415-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]