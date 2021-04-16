---
title: データ収集カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされるデータ収集関数について説明します。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 31b5e7b08a3de77d461fff5e42164975e53dfe1e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748066"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="d41ce-103">データ収集カテゴリ内の ER 関数のリスト</span><span class="sxs-lookup"><span data-stu-id="d41ce-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d41ce-104">電子申告 (ER) データ収集関数は、**テキスト** または **Xml** 形式で生成された出力のデータに基づいて、実行中の ER 形式で棚卸および集計を行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d41ce-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="d41ce-105">この方法は、実行される ER 形式のパフォーマンスを向上させたり、生成されたドキュメントに実行中の合計値を入力したり、その他の目的でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="d41ce-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="d41ce-106">このトピックでは、これらの関数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="d41ce-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="d41ce-107">サポートされている関数のリスト</span><span class="sxs-lookup"><span data-stu-id="d41ce-107">List of supported functions</span></span>

| <span data-ttu-id="d41ce-108">職務</span><span class="sxs-lookup"><span data-stu-id="d41ce-108">Function</span></span> | <span data-ttu-id="d41ce-109">説明</span><span class="sxs-lookup"><span data-stu-id="d41ce-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="d41ce-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="d41ce-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="d41ce-111">この関数は、形式要素の **収集されたデータ キー値** プロパティによって返され、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された値のリストを含む *レコード リスト* 値を返します。これは指定された条件を満たすものです。</span><span class="sxs-lookup"><span data-stu-id="d41ce-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="d41ce-112">各条件は、キー範囲とキー値で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d41ce-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="d41ce-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="d41ce-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="d41ce-114">この関数は、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された、形式要素の数を表す *整数* 値を返します。これは指定された条件を満たすものです。</span><span class="sxs-lookup"><span data-stu-id="d41ce-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="d41ce-115">条件は、キー範囲とキー値で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d41ce-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="d41ce-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="d41ce-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="d41ce-117">この関数は、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された、形式要素の数を表す *整数* 値を返します。これは指定された条件を満たすものです。</span><span class="sxs-lookup"><span data-stu-id="d41ce-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="d41ce-118">各条件は、キー範囲とキー値で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d41ce-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="d41ce-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="d41ce-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="d41ce-120">この関数は、現在の ER 形式要素の名前を表す *文字列* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="d41ce-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="d41ce-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="d41ce-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="d41ce-122">この関数は、形式要素のバインディングにより返された、およびフォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された値の合計を表す *実数* 値を返します。これは指定された条件を満たすものです。</span><span class="sxs-lookup"><span data-stu-id="d41ce-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="d41ce-123">条件は、キー範囲とキー値で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d41ce-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="d41ce-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="d41ce-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="d41ce-125">この関数は、形式要素のバインディングにより返された、およびフォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された値の合計を表す *実数* 値を返します。これは指定された条件を満たすものです。</span><span class="sxs-lookup"><span data-stu-id="d41ce-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="d41ce-126">各条件は、キー範囲とキー値で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d41ce-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d41ce-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d41ce-127">Additional resources</span></span>

[<span data-ttu-id="d41ce-128">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="d41ce-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="d41ce-129">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="d41ce-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="d41ce-130">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="d41ce-130">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]