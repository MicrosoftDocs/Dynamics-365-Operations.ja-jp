---
title: 既存のフォーミュラ バージョンから連産品をコピー
description: この手順では、既存のフォーミュラ バージョンから、リリース済製品の別のフォーミュラ バージョンに連産品をコピーする方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cbcf2abc37441f9ff23e2b180c261831dfb79369
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829285"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="6c135-103">既存のフォーミュラ バージョンから連産品をコピー</span><span class="sxs-lookup"><span data-stu-id="6c135-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c135-104">この手順では、既存のフォーミュラ バージョンから、リリース済製品の別のフォーミュラ バージョンに連産品をコピーする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6c135-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="6c135-105">連産品と関連付けられている少なくとも 1 つのフォーミュラ バージョンがあることが前提条件です。</span><span class="sxs-lookup"><span data-stu-id="6c135-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="6c135-106">この手順の作成に使用するデモ データの会社は USP2 です。</span><span class="sxs-lookup"><span data-stu-id="6c135-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="6c135-107">リリース済製品の検索</span><span class="sxs-lookup"><span data-stu-id="6c135-107">Find a released product</span></span>
1. <span data-ttu-id="6c135-108">[リリースされた製品] に進みます。</span><span class="sxs-lookup"><span data-stu-id="6c135-108">Go to Released products.</span></span>
2. <span data-ttu-id="6c135-109">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c135-109">Click Show filters.</span></span>
    * <span data-ttu-id="6c135-110">フィルターのダイアログ ボックスで [生産] タイプのフィールドを追加しようとしています。</span><span class="sxs-lookup"><span data-stu-id="6c135-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="6c135-111">[生産] タイプのフィールドを追加するために [フィルター フィールドの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c135-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="6c135-112">次の手順で、[適用] を選択する前に手動で [生産タイプ] フィールドに式を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c135-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="6c135-113">これは、リリース済製品一覧のフィルターを設定します。</span><span class="sxs-lookup"><span data-stu-id="6c135-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="6c135-114">手動で [生産タイプ] フィールドに式を入力します。</span><span class="sxs-lookup"><span data-stu-id="6c135-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="6c135-115">[適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c135-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="6c135-116">リリース済製品の選択</span><span class="sxs-lookup"><span data-stu-id="6c135-116">Select a released product</span></span>
1. <span data-ttu-id="6c135-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6c135-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="6c135-118">[フォーミュラ バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c135-118">Click Formula versions.</span></span>
    * <span data-ttu-id="6c135-119">[技術アクション ペイン] で、[フォーミュラ バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c135-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="6c135-120">連産物のコピー</span><span class="sxs-lookup"><span data-stu-id="6c135-120">Copy co-products</span></span>
1. <span data-ttu-id="6c135-121">[アクション ペイン] で、[フォーミュラ バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c135-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="6c135-122">[連産品 (複数)] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c135-122">Click Co-products.</span></span>
3. <span data-ttu-id="6c135-123">[コピー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c135-123">Click Copy.</span></span>
4. <span data-ttu-id="6c135-124">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6c135-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="6c135-125">[フォーミュラ バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6c135-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="6c135-126">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c135-126">Click OK.</span></span>
7. <span data-ttu-id="6c135-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6c135-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]