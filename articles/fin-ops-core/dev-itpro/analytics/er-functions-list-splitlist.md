---
title: SPLITLIST ER 関数
description: このトピックでは、SPLITLIST 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b324d42a53b35074ba62ccf3df7b77cb4db70450
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917215"
---
# <span data-ttu-id="523ce-103"><a name="SPLITLIST">SPLITLIST ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="523ce-103"><a name="SPLITLIST">SPLITLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="523ce-104">`SPLITLIST` 関数は、指定されたリストをサブリスト (またはバッチ) に分割します。各サブリストには指定されたレコード数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="523ce-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="523ce-105">その後、結果をバッチで構成された新しい*レコード リスト*値として返します。</span><span class="sxs-lookup"><span data-stu-id="523ce-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="523ce-106">構文</span><span class="sxs-lookup"><span data-stu-id="523ce-106">Syntax</span></span>

```
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="523ce-107">引数</span><span class="sxs-lookup"><span data-stu-id="523ce-107">Arguments</span></span>

<span data-ttu-id="523ce-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="523ce-108">`list`: *Record list*</span></span>

<span data-ttu-id="523ce-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="523ce-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="523ce-110">`number`: *整数*</span><span class="sxs-lookup"><span data-stu-id="523ce-110">`number`: *Integer*</span></span>

<span data-ttu-id="523ce-111">バッチごとのレコードの最大数</span><span class="sxs-lookup"><span data-stu-id="523ce-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="523ce-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="523ce-112">Return values</span></span>

<span data-ttu-id="523ce-113">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="523ce-113">*Record list*</span></span>

<span data-ttu-id="523ce-114">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="523ce-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="523ce-115">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="523ce-115">Usage notes</span></span>

<span data-ttu-id="523ce-116">返されるバッチのリストには、次の要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="523ce-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="523ce-117">**値:** *リスト*</span><span class="sxs-lookup"><span data-stu-id="523ce-117">**Value:** *List*</span></span>

    <span data-ttu-id="523ce-118">現在のバッチに属するレコードのリスト。</span><span class="sxs-lookup"><span data-stu-id="523ce-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="523ce-119">**Batchnumber:** *整数*</span><span class="sxs-lookup"><span data-stu-id="523ce-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="523ce-120">返されたリスト内の現在のバッチ数。</span><span class="sxs-lookup"><span data-stu-id="523ce-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="523ce-121">例</span><span class="sxs-lookup"><span data-stu-id="523ce-121">Example</span></span>

<span data-ttu-id="523ce-122">次の図では、**明細行**データ ソースが、3 つのレコードがあるレコード リストとして作成されます。</span><span class="sxs-lookup"><span data-stu-id="523ce-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="523ce-123">このリストは、それぞれ最大 2 つのレコードを含むバッチに分割されます。</span><span class="sxs-lookup"><span data-stu-id="523ce-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="523ce-124">次の図は、設計された形式レイアウトを示します。</span><span class="sxs-lookup"><span data-stu-id="523ce-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="523ce-125">この形式のレイアウトでは、XML 形式で出力を生成するために作成される **明細行** データ ソースにバインディングされます。</span><span class="sxs-lookup"><span data-stu-id="523ce-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="523ce-126">この出力は、各バッチとその中のレコードに対する個々のノードを表示します。</span><span class="sxs-lookup"><span data-stu-id="523ce-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="523ce-127">次の図は、設計された形式が実行される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="523ce-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="523ce-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="523ce-128">Additional resources</span></span>

[<span data-ttu-id="523ce-129">リスト機能</span><span class="sxs-lookup"><span data-stu-id="523ce-129">List functions</span></span>](er-functions-category-list.md)
