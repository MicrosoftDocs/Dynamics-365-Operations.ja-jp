---
title: 運賃の手動調整
description: この手順では、運賃を手動で調整する方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a0a5450697a09e5e54e74b35b2576eb6bbd4cdf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838517"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="60c03-103">運賃の手動調整</span><span class="sxs-lookup"><span data-stu-id="60c03-103">Reconcile freight manually</span></span>

<span data-ttu-id="60c03-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="60c03-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="60c03-105">この手順では、運賃を手動で調整する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="60c03-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="60c03-106">この設定は、通常、配送コーディネーターにより実行されます。</span><span class="sxs-lookup"><span data-stu-id="60c03-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="60c03-107">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="60c03-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="60c03-108">積荷を選択して調整します。</span><span class="sxs-lookup"><span data-stu-id="60c03-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="60c03-109">[配送管理] > [計画] > [積荷計画ワークベンチ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="60c03-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="60c03-110">[出荷と入庫を非表示にする] チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="60c03-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="60c03-111">リストで、積荷 ID 00006 を持つ積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="60c03-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="60c03-112">運送業者の請求書を作成する</span><span class="sxs-lookup"><span data-stu-id="60c03-112">Create a carrier invoice</span></span>
<span data-ttu-id="60c03-113">運賃を手動で調整して、配送業者の請求書を自動的に受け取らない場合、運賃の請求に基づいて請求書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="60c03-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="60c03-114">[関連情報] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c03-114">Click Related information.</span></span>
2. <span data-ttu-id="60c03-115">[運賃請求書の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c03-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="60c03-116">[運賃請求書の請求書の生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c03-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="60c03-117">[請求書] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60c03-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="60c03-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c03-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="60c03-119">請求書を調整する</span><span class="sxs-lookup"><span data-stu-id="60c03-119">Reconcile the invoice</span></span>
<span data-ttu-id="60c03-120">配送業者の請求書と運賃請求書を調整する場合、1 行ずつ処理します。</span><span class="sxs-lookup"><span data-stu-id="60c03-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="60c03-121">[運賃請求書と請求書の照合] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c03-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="60c03-122">[請求書の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="60c03-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="60c03-123">[一致しない運賃請求書の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="60c03-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="60c03-124">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="60c03-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="60c03-125">[照合] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c03-125">Click Match.</span></span>
6. <span data-ttu-id="60c03-126">一致した配送料請求書の詳細セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="60c03-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="60c03-127">承認のために請求書を送信します</span><span class="sxs-lookup"><span data-stu-id="60c03-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="60c03-128">承認のために [送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c03-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="60c03-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="60c03-129">Close the page.</span></span>
3. <span data-ttu-id="60c03-130">承認済みチェック ボックスの非表示を消去します。</span><span class="sxs-lookup"><span data-stu-id="60c03-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="60c03-131">仕入先の請求仕訳をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c03-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="60c03-132">クリックして [参照仕訳帳番号] フィールドのリンクに従います。</span><span class="sxs-lookup"><span data-stu-id="60c03-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="60c03-133">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c03-133">Click Lines.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]