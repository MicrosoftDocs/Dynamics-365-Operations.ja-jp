---
title: "POS の現金貨幣単位をコンフィギュレーションします。"
description: "紙幣および硬貨の現金貨幣単位は、POS 内で店舗のレジ担当者、店員およびマネージャーにより使用されるバック オフィスで定義できます。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45e70765c43b93e9d8abab5fbb9de1d67a739a74
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="configure-cash-denominations-for-pos"></a><span data-ttu-id="5e6db-103">POS の現金貨幣単位をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="5e6db-103">Configure cash denominations for POS</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="5e6db-104">紙幣および硬貨の現金貨幣単位は、POS 内で店舗のレジ担当者、店員およびマネージャーにより使用されるバック オフィスで定義できます。</span><span class="sxs-lookup"><span data-stu-id="5e6db-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="5e6db-105">これらの貨幣単位は、営業終了時の支払/入金申告、または売上の簡単な支払/入金の現金計算をする助けとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="5e6db-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="5e6db-106">貨幣単位の定義</span><span class="sxs-lookup"><span data-stu-id="5e6db-106">Define denominations</span></span>
<span data-ttu-id="5e6db-107">貨幣単位は店舗ごとに **設定** > **店舗プロパティからの現金申告オプション** ページで設定されます。</span><span class="sxs-lookup"><span data-stu-id="5e6db-107">The denominations are set up per store on the **Set up** > **Cash declaration option from the store property** page.</span></span> 

![現金貨幣単位](./media/image1-denomination.png)

<span data-ttu-id="5e6db-109">貨幣単位を定義する方法:</span><span class="sxs-lookup"><span data-stu-id="5e6db-109">To define a denomination:</span></span>
1. <span data-ttu-id="5e6db-110">[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e6db-110">Click **New**.</span></span>
1. <span data-ttu-id="5e6db-111">種類 (硬貨または紙幣) を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e6db-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="5e6db-112">金額 (値) を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e6db-112">Specify the amount (value).</span></span>

![現金貨幣単位](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="5e6db-114">機能プロファイルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5e6db-114">Configure the functionality profile</span></span>
<span data-ttu-id="5e6db-115">POS での現金による支払の際、ユーザーは、顧客によって支払われた金額をすばやく入力するため紙幣の通貨単位を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5e6db-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="5e6db-116">機能プロファイルで、POSで貨幣単位を表示するための 2 つのオプションをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="5e6db-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

<span data-ttu-id="5e6db-117">**合計金額以上**: 既定では、POS は未払い金額より多い紙幣の通貨単位のみを表示し、ワンタッチの支払/入金をできるようにします。</span><span class="sxs-lookup"><span data-stu-id="5e6db-117">**Greater or equal to amount due**: By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="5e6db-118">たとえば、請求額が $7.50 の場合、POS は次の通貨単位を表示します: $10、$20、$50、および $100。</span><span class="sxs-lookup"><span data-stu-id="5e6db-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="5e6db-119">これらの金額のいずれかにタッチすると、自動的にその金額に対する売上の支払/入金をします。</span><span class="sxs-lookup"><span data-stu-id="5e6db-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="5e6db-120">$1 および $5 紙幣、これらの金額は、請求額よりも少ないため表示されません。</span><span class="sxs-lookup"><span data-stu-id="5e6db-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>

<span data-ttu-id="5e6db-121">**すべての貨幣単位**: 請求額に関係なく、POS で常にすべての紙幣の貨幣単位を表示するため、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e6db-121">**All denominations**: Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="5e6db-122">つまり、ユーザーは請求額に達する紙幣の組み合わせを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5e6db-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="5e6db-123">たとえば、請求額が $25.00 の場合は、ユーザーは $20 よび $5 を選択して販売を完了できます。</span><span class="sxs-lookup"><span data-stu-id="5e6db-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>

