---
title: SPLITLIST ER 関数
description: このトピックでは、SPLITLIST 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745572"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="7959c-103">SPLITLIST ER 関数</span><span class="sxs-lookup"><span data-stu-id="7959c-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7959c-104">`SPLITLIST` 関数は、指定されたリストをサブリスト (またはバッチ) に分割します。各サブリストには指定されたレコード数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7959c-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="7959c-105">その後、結果をバッチで構成された新しい *レコード リスト* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="7959c-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="7959c-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="7959c-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="7959c-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="7959c-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="7959c-108">引数</span><span class="sxs-lookup"><span data-stu-id="7959c-108">Arguments</span></span>

<span data-ttu-id="7959c-109">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="7959c-109">`list`: *Record list*</span></span>

<span data-ttu-id="7959c-110">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="7959c-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7959c-111">`number`: *整数*</span><span class="sxs-lookup"><span data-stu-id="7959c-111">`number`: *Integer*</span></span>

<span data-ttu-id="7959c-112">バッチごとのレコードの最大数</span><span class="sxs-lookup"><span data-stu-id="7959c-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="7959c-113">`on-demand reading flag`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="7959c-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="7959c-114">サブリストの要素をオンデマンドで生成すべきかどうかを指定する *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="7959c-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="7959c-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="7959c-115">Return values</span></span>

<span data-ttu-id="7959c-116">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="7959c-116">*Record list*</span></span>

<span data-ttu-id="7959c-117">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="7959c-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7959c-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="7959c-118">Usage notes</span></span>

<span data-ttu-id="7959c-119">返されるバッチのリストには、次の要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7959c-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="7959c-120">**値:** *リスト*</span><span class="sxs-lookup"><span data-stu-id="7959c-120">**Value:** *List*</span></span>

    <span data-ttu-id="7959c-121">現在のバッチに属するレコードのリスト。</span><span class="sxs-lookup"><span data-stu-id="7959c-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="7959c-122">**Batchnumber:** *整数*</span><span class="sxs-lookup"><span data-stu-id="7959c-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="7959c-123">返されたリスト内の現在のバッチ数。</span><span class="sxs-lookup"><span data-stu-id="7959c-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="7959c-124">需要の読み取りフラグが **True** に設定されている場合、サブリストは要求時に生成され、メモリ消費の減少が可能になりますが、要素が順番に使用されていないと、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7959c-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="7959c-125">例</span><span class="sxs-lookup"><span data-stu-id="7959c-125">Example</span></span>

<span data-ttu-id="7959c-126">次の図では、**明細行** データ ソースが、3 つのレコードがあるレコード リストとして作成されます。</span><span class="sxs-lookup"><span data-stu-id="7959c-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="7959c-127">このリストは、それぞれ最大 2 つのレコードを含むバッチに分割されます。</span><span class="sxs-lookup"><span data-stu-id="7959c-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="7959c-128">次の図は、設計された形式レイアウトを示します。</span><span class="sxs-lookup"><span data-stu-id="7959c-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="7959c-129">この形式のレイアウトでは、XML 形式で出力を生成するために作成される **明細行** データ ソースにバインディングされます。</span><span class="sxs-lookup"><span data-stu-id="7959c-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="7959c-130">この出力は、各バッチとその中のレコードに対する個々のノードを表示します。</span><span class="sxs-lookup"><span data-stu-id="7959c-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="7959c-131">次の図は、設計された形式が実行される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="7959c-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="7959c-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7959c-132">Additional resources</span></span>

[<span data-ttu-id="7959c-133">リスト機能</span><span class="sxs-lookup"><span data-stu-id="7959c-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
