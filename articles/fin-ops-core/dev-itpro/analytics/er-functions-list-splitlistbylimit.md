---
title: SPLITLISTBYLIMIT ER 関数
description: このトピックでは、SPLITLISTBYLIMIT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: eb492560a453ec59bb82d24dd6717f409bd8b257
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745548"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="3e4ec-103">SPLITLISTBYLIMIT ER 関数</span><span class="sxs-lookup"><span data-stu-id="3e4ec-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e4ec-104">`SPLITLISTBYLIMIT` 関数は、指定されたリストを新しいサブリスト (バッチ) のリストに分割します。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="3e4ec-105">各バッチのレコード数は動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="3e4ec-106">その後、関数は結果をバッチで構成された新しい *レコード リスト* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4ec-107">構文</span><span class="sxs-lookup"><span data-stu-id="3e4ec-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="3e4ec-108">引数</span><span class="sxs-lookup"><span data-stu-id="3e4ec-108">Arguments</span></span>

<span data-ttu-id="3e4ec-109">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="3e4ec-109">`list`: *Record list*</span></span>

<span data-ttu-id="3e4ec-110">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="3e4ec-111">`limit value`: *整数* または *実数*</span><span class="sxs-lookup"><span data-stu-id="3e4ec-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="3e4ec-112">元のリストをバッチに分割するために使用される制限の最大値。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="3e4ec-113">`limit source`: *フィールド*</span><span class="sxs-lookup"><span data-stu-id="3e4ec-113">`limit source`: *Field*</span></span>

<span data-ttu-id="3e4ec-114">指定されたリストの *整数* 型または *実数* 型のフィールドの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="3e4ec-115">このフィールドの値は、合計が増加するステップを定義します。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="3e4ec-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="3e4ec-116">Return values</span></span>

<span data-ttu-id="3e4ec-117">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="3e4ec-117">*Record list*</span></span>

<span data-ttu-id="3e4ec-118">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3e4ec-119">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="3e4ec-119">Usage notes</span></span>

<span data-ttu-id="3e4ec-120">返されるバッチのリストには、次の要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="3e4ec-121">**値**: *リスト*</span><span class="sxs-lookup"><span data-stu-id="3e4ec-121">**Value**: *List*</span></span>

    <span data-ttu-id="3e4ec-122">現在のバッチに属するレコードのリスト。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="3e4ec-123">**Batchnumber**: *整数*</span><span class="sxs-lookup"><span data-stu-id="3e4ec-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="3e4ec-124">返されたリスト内の現在のバッチ数。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="3e4ec-125">制限は、制限のソースが定義済み制限を超えると、元のリストの 1 つの項目に適用されません。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="3e4ec-126">例</span><span class="sxs-lookup"><span data-stu-id="3e4ec-126">Example</span></span>

<span data-ttu-id="3e4ec-127">次の図は、電子申告 (ER) 形式を示しています。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="3e4ec-128">次の図は、形式に対して使用されているデータ ソースを示します。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="3e4ec-129">次の図は、形式が実行される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="3e4ec-130">この場合、出力は、商品のフラット リストです。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="3e4ec-131">次の図では、1 つのバッチに合計重量が 9 を超えない商品を含める必要がある場合、商品アイテムのリストをバッチに表示するために同じフォーマットが調整されています。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="3e4ec-132">次の図は、調整された形式が実行される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="3e4ec-133">制限は、制限のソース (**重量**) の値 (**11**) が定義済みの制限 (**9**) を超えるため、元のリストの最後の項目に適用されません。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="3e4ec-134">レポートの生成中にサブリストを無視するには、必要に応じて、 `WHERE` 関数または対応するフォーマット要素の **有効** 式のいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e4ec-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e4ec-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3e4ec-135">Additional resources</span></span>

[<span data-ttu-id="3e4ec-136">リスト機能</span><span class="sxs-lookup"><span data-stu-id="3e4ec-136">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]