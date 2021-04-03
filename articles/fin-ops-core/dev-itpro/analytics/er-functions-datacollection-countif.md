---
title: COUNTIF ER 関数
description: このトピックでは、COUNTIF 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 19ceb8d3023aadeb6307ed5d930587a8f00f63b7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561377"
---
# <a name="countif-er-function"></a><span data-ttu-id="2db7a-103">COUNTIF ER 関数</span><span class="sxs-lookup"><span data-stu-id="2db7a-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2db7a-104">`COUNTIF` 関数は、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された、形式要素の数を表す *整数* 値を返します。これは指定された条件を満たすものです。</span><span class="sxs-lookup"><span data-stu-id="2db7a-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="2db7a-105">条件は、キー範囲とキー値で構成されます。</span><span class="sxs-lookup"><span data-stu-id="2db7a-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db7a-106">構文</span><span class="sxs-lookup"><span data-stu-id="2db7a-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="2db7a-107">引数</span><span class="sxs-lookup"><span data-stu-id="2db7a-107">Arguments</span></span>

<span data-ttu-id="2db7a-108">`condition range`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="2db7a-108">`condition range`: *String*</span></span>

<span data-ttu-id="2db7a-109">電子申告 (ER) 形式コンポーネントの **収集したデータ キー名** プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="2db7a-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="2db7a-110">`condition value`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="2db7a-110">`condition value`: *String*</span></span>

<span data-ttu-id="2db7a-111">ER 形式コンポーネントの **収集したデータ キー値** プロパティでコンフィギュレーションされた式によって返される値。</span><span class="sxs-lookup"><span data-stu-id="2db7a-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="2db7a-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="2db7a-112">Return values</span></span>

<span data-ttu-id="2db7a-113">*整数*</span><span class="sxs-lookup"><span data-stu-id="2db7a-113">*Integer*</span></span>

<span data-ttu-id="2db7a-114">結果数値。</span><span class="sxs-lookup"><span data-stu-id="2db7a-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2db7a-115">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="2db7a-115">Usage notes</span></span>

<span data-ttu-id="2db7a-116">**収集したデータ キー名** および **収集したデータ キー値** プロパティは、ER 形式の **シーケンス** コンポーネントまたは **XML 要素** コンポーネントのいずれかに対してコンフィギュレーションできます。それは **出力の詳細を収集** オプションがオンになっている **共通\\ファイル** コンポーネントの下に存在します。</span><span class="sxs-lookup"><span data-stu-id="2db7a-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="2db7a-117">この関数は、現在の **共通\\ファイル** コンポーネントの **出力の詳細を収集** オプションを無効にすると、**0** (ゼロ) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="2db7a-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="2db7a-118">`condition range` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="2db7a-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="2db7a-119">`condition value` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="2db7a-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="2db7a-120">例</span><span class="sxs-lookup"><span data-stu-id="2db7a-120">Example</span></span>

<span data-ttu-id="2db7a-121">この関数の用途の詳細については、**IT サービス/ソリューション コンポーネントの取得/開発** 業務プロセスの一部である [ER 棚卸および集計のために出力された形式の使用](tasks/er-format-counting-summing-1.md) タスク ガイドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2db7a-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2db7a-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2db7a-122">Additional resources</span></span>

[<span data-ttu-id="2db7a-123">データ収集機能</span><span class="sxs-lookup"><span data-stu-id="2db7a-123">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]