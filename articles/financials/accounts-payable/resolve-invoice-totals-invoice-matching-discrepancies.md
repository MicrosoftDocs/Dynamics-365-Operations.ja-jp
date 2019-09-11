---
title: 請求合計の照合における差異の解決の概要
description: 合計請求書の照合により、合計請求書金額が、許容差を超えて予測金額から逸脱していないことを確認できます。
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a20368385ec43547ee3d29770bd83cdec47e4a
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864945"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a><span data-ttu-id="ba09f-103">請求合計の照合における差異の解決の概要</span><span class="sxs-lookup"><span data-stu-id="ba09f-103">Resolve discrepancies during invoice totals matching overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba09f-104">請求書照合の検証の一つのタイプは、請求合計の照合です。</span><span class="sxs-lookup"><span data-stu-id="ba09f-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="ba09f-105">システムが請求合計の照合をするよう指定するには、**買掛金勘定パラメータ** ページの **請求書の検証** タブで **請求合計の照合** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ba09f-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="ba09f-106">合計請求書の照合により、合計請求書金額が、許容差を超えて予測金額から逸脱していないことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="ba09f-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="ba09f-107">6 つの合計が **請求合計照合の詳細** ページで比較されます。</span><span class="sxs-lookup"><span data-stu-id="ba09f-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="ba09f-108">合計のいずれかが、対応する発注書の合計予想金額から逸脱すると、照合不一致にフラグが立ちます。</span><span class="sxs-lookup"><span data-stu-id="ba09f-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="ba09f-109">合計の照合不一致のある請求書を確認するには、**仕入先請求書の入力** ワークスペースで **保留中の請求書** のタイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ba09f-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="ba09f-110">その後、アクション ペインの **確認** タブで **照合の詳細** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ba09f-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="ba09f-111">照合不一致が検出された場合に、警告アイコンが請求金額の横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="ba09f-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="ba09f-112">請求合計照合の詳細を表示して合計に関する詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ba09f-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="ba09f-113">不一致を識別した後で、請求書の情報が間違っていると思う場合には、仕入先に連絡する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="ba09f-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="ba09f-114">その結果の仕入先との合意に応じて、次のいずれかのアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ba09f-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="ba09f-115">価格差異を受け入れ、照合不一致のある請求書を転記する。</span><span class="sxs-lookup"><span data-stu-id="ba09f-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="ba09f-116">照合不一致がある場合、転記する前に承認を要求するようにシステムが設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="ba09f-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="ba09f-117">この場合、照合不一致を承認し、必要に応じて承認コメントを入力できます。</span><span class="sxs-lookup"><span data-stu-id="ba09f-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="ba09f-118">その後、請求書を転記する選択ができます。</span><span class="sxs-lookup"><span data-stu-id="ba09f-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="ba09f-119">請求書金額を想定される金額に改訂し、請求書を転記する。</span><span class="sxs-lookup"><span data-stu-id="ba09f-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="ba09f-120">仕入先にフル クレジットと訂正した新しい請求書を要求する。</span><span class="sxs-lookup"><span data-stu-id="ba09f-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="ba09f-121">詳細については、「[例外の調査または解決](tasks/research-resolve-exceptions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba09f-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>


