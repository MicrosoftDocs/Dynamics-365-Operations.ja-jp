--- 
title: "運賃の手動調整"
description: "この手順では、運賃を手動で調整する方法を示します。"
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="b8229-103">運賃の手動調整</span><span class="sxs-lookup"><span data-stu-id="b8229-103">Reconcile freight manually</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8229-104">この手順では、運賃を手動で調整する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b8229-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="b8229-105">この設定は、通常、配送コーディネーターにより実行されます。</span><span class="sxs-lookup"><span data-stu-id="b8229-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="b8229-106">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b8229-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="b8229-107">積荷を選択して調整します。</span><span class="sxs-lookup"><span data-stu-id="b8229-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="b8229-108">[配送管理] > [計画] > [積荷計画ワークベンチ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8229-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="b8229-109">[出荷と入庫を非表示にする] チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="b8229-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="b8229-110">リストで、積荷 ID 00006 を持つ積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8229-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="b8229-111">運送業者の請求書を作成する</span><span class="sxs-lookup"><span data-stu-id="b8229-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="b8229-112">運賃を手動で調整して、配送業者の請求書を自動的に受け取らない場合、運賃請求書に基づいて請求書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b8229-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="b8229-113">[関連情報] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8229-113">Click Related information.</span></span>
2. <span data-ttu-id="b8229-114">[運賃請求書の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8229-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="b8229-115">[運賃請求書の請求書の生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8229-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="b8229-116">[請求書] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8229-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="b8229-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8229-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="b8229-118">請求書を調整する</span><span class="sxs-lookup"><span data-stu-id="b8229-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="b8229-119">配送業者の請求書と運賃請求書を調整する場合、1 行ずつ処理します。</span><span class="sxs-lookup"><span data-stu-id="b8229-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="b8229-120">[運賃請求書と請求書の照合] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8229-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="b8229-121">[請求書の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b8229-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="b8229-122">[一致しない運賃請求書の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b8229-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="b8229-123">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b8229-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="b8229-124">[照合] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8229-124">Click Match.</span></span>
6. <span data-ttu-id="b8229-125">一致した配送料請求書の詳細セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b8229-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="b8229-126">承認のために請求書を送信します</span><span class="sxs-lookup"><span data-stu-id="b8229-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="b8229-127">承認のために [送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8229-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="b8229-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b8229-128">Close the page.</span></span>
3. <span data-ttu-id="b8229-129">承認済みチェック ボックスの非表示を消去します。</span><span class="sxs-lookup"><span data-stu-id="b8229-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="b8229-130">仕入先の請求仕訳をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8229-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="b8229-131">クリックして [参照仕訳帳番号] フィールドのリンクに従います。</span><span class="sxs-lookup"><span data-stu-id="b8229-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="b8229-132">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8229-132">Click Lines.</span></span>


