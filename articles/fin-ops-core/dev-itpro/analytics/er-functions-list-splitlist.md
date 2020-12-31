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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0f527dcf313a6a5e3b6601cac9a0f6495f66833
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680342"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="1eb4b-103">SPLITLIST ER 関数</span><span class="sxs-lookup"><span data-stu-id="1eb4b-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1eb4b-104">`SPLITLIST` 関数は、指定されたリストをサブリスト (またはバッチ) に分割します。各サブリストには指定されたレコード数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="1eb4b-105">その後、結果をバッチで構成された新しい *レコード リスト* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb4b-106">構文</span><span class="sxs-lookup"><span data-stu-id="1eb4b-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="1eb4b-107">引数</span><span class="sxs-lookup"><span data-stu-id="1eb4b-107">Arguments</span></span>

<span data-ttu-id="1eb4b-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="1eb4b-108">`list`: *Record list*</span></span>

<span data-ttu-id="1eb4b-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="1eb4b-110">`number`: *整数*</span><span class="sxs-lookup"><span data-stu-id="1eb4b-110">`number`: *Integer*</span></span>

<span data-ttu-id="1eb4b-111">バッチごとのレコードの最大数</span><span class="sxs-lookup"><span data-stu-id="1eb4b-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="1eb4b-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="1eb4b-112">Return values</span></span>

<span data-ttu-id="1eb4b-113">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="1eb4b-113">*Record list*</span></span>

<span data-ttu-id="1eb4b-114">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1eb4b-115">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="1eb4b-115">Usage notes</span></span>

<span data-ttu-id="1eb4b-116">返されるバッチのリストには、次の要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="1eb4b-117">**値:** *リスト*</span><span class="sxs-lookup"><span data-stu-id="1eb4b-117">**Value:** *List*</span></span>

    <span data-ttu-id="1eb4b-118">現在のバッチに属するレコードのリスト。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="1eb4b-119">**Batchnumber:** *整数*</span><span class="sxs-lookup"><span data-stu-id="1eb4b-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="1eb4b-120">返されたリスト内の現在のバッチ数。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="1eb4b-121">例</span><span class="sxs-lookup"><span data-stu-id="1eb4b-121">Example</span></span>

<span data-ttu-id="1eb4b-122">次の図では、**明細行** データ ソースが、3 つのレコードがあるレコード リストとして作成されます。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="1eb4b-123">このリストは、それぞれ最大 2 つのレコードを含むバッチに分割されます。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="1eb4b-124">次の図は、設計された形式レイアウトを示します。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="1eb4b-125">この形式のレイアウトでは、XML 形式で出力を生成するために作成される **明細行** データ ソースにバインディングされます。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="1eb4b-126">この出力は、各バッチとその中のレコードに対する個々のノードを表示します。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="1eb4b-127">次の図は、設計された形式が実行される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="1eb4b-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="1eb4b-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1eb4b-128">Additional resources</span></span>

[<span data-ttu-id="1eb4b-129">リスト機能</span><span class="sxs-lookup"><span data-stu-id="1eb4b-129">List functions</span></span>](er-functions-category-list.md)
