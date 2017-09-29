---
title: "請求書の合計価格の照合における差異を解決"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="c44e9-102">請求書の合計価格の照合における差異を解決</span><span class="sxs-lookup"><span data-stu-id="c44e9-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="c44e9-103">請求書照合の検証の一つのタイプは、請求合計の照合です。</span><span class="sxs-lookup"><span data-stu-id="c44e9-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="c44e9-104">システムが請求合計の照合をするよう指定するには、[**買掛金勘定パラメータ**] ページの [**請求書の検証**] タブで [**請求合計の照合**] オプションを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="c44e9-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="c44e9-105">合計請求書の照合により、合計請求書金額が、許容差を超えて予測金額から逸脱していないことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c44e9-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="c44e9-106">6 つの合計が [**請求合計照合の詳細**] ページで比較されます。</span><span class="sxs-lookup"><span data-stu-id="c44e9-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="c44e9-107">合計のいずれかが、対応する発注書の合計予想金額から逸脱すると、照合不一致にフラグが立ちます。</span><span class="sxs-lookup"><span data-stu-id="c44e9-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="c44e9-108">合計の照合不一致のある請求書を確認するには、[**仕入先請求書の入力**] ワークスペースで [**保留中の請求書**] のタイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c44e9-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="c44e9-109">その後、アクション ペインの [**確認**] タブで [**照合の詳細**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c44e9-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="c44e9-110">照合不一致が検出された場合に、警告アイコンが請求金額の横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c44e9-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="c44e9-111">請求合計照合の詳細を表示して合計に関する詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="c44e9-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="c44e9-112">不一致を識別した後で、請求書の情報が間違っていると思う場合には、仕入先に連絡する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="c44e9-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="c44e9-113">その結果の仕入先との合意に応じて、次のいずれかのアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="c44e9-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="c44e9-114">価格差異を受け入れ、照合不一致のある請求書を転記する。</span><span class="sxs-lookup"><span data-stu-id="c44e9-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="c44e9-115">照合不一致がある場合、転記する前に承認を要求するようにシステムが設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="c44e9-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="c44e9-116">この場合、照合不一致を承認し、必要に応じて承認コメントを入力できます。</span><span class="sxs-lookup"><span data-stu-id="c44e9-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="c44e9-117">その後、請求書を転記する選択ができます。</span><span class="sxs-lookup"><span data-stu-id="c44e9-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="c44e9-118">請求書金額を想定される金額に改訂し、請求書を転記する。</span><span class="sxs-lookup"><span data-stu-id="c44e9-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="c44e9-119">仕入先にフル クレジットと訂正した新しい請求書を要求する。</span><span class="sxs-lookup"><span data-stu-id="c44e9-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="c44e9-120">詳細については、「[例外の調査または解決](tasks/research-resolve-exceptions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c44e9-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



