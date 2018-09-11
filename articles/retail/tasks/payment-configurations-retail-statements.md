--- 
title: "小売明細書の支払コンフィギュレーション"
description: "この手順では、小売店舗支払方法のコンフィギュレーションが、小売明細書の作成と転記にどのように影響を及ぼすかを示します。"
author: jashanno
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 6261d9c3d6bf6591be296115d4f25a124a17b9dd
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="edc63-103">小売明細書の支払コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="edc63-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="edc63-104">この手順では、小売店舗支払方法のコンフィギュレーションが、小売明細書の作成と転記にどのように影響を及ぼすかを示します。</span><span class="sxs-lookup"><span data-stu-id="edc63-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="edc63-105">このレコードでは、MXMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="edc63-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="edc63-106">[小売とコマース] > [チャンネル] > [小売店舗] > [すべての小売店舗] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="edc63-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="edc63-107">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="edc63-108">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="edc63-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="edc63-109">アクション ペインで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="edc63-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="edc63-110">[支払方法] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="edc63-110">Click Payment methods.</span></span>
6. <span data-ttu-id="edc63-111">[転記] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="edc63-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="edc63-112">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="edc63-112">Click Edit.</span></span>
    * <span data-ttu-id="edc63-113">この支払方法に対して受領した勘定科目、または銀行口座への金額を転記するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="edc63-114">転記される必要がある支払方法の受領済金額の勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="edc63-115">受け取ったトランザクション金額の合計と、この支払方法でカウントされた金額の差額を転記する勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="edc63-116">別の差額勘定に差額が転記される必要がある場合、管理するために、このフィールドに金額を転記できます。</span><span class="sxs-lookup"><span data-stu-id="edc63-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="edc63-117">大きな差額を追跡するために、これを使用できます。</span><span class="sxs-lookup"><span data-stu-id="edc63-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="edc63-118">[最大差額量] で定義された値を超えた場合に、受け取ったトランザクション金額の合計とカウントされた金額の差額を転記する勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="edc63-119">個別勘定への銀行入金額を転記するには、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-119">Select "Yes" to post bank drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="edc63-120">このフィールドで、銀行入金額を、勘定科目、または銀行口座へ転記するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="edc63-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="edc63-121">銀行入金額を転記する口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="edc63-122">銀行入金額を銀行口座に転記するときの、銀行トランザクション タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="edc63-123">個別勘定への金庫保管額を転記するには、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-123">Select "Yes" to post safe drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="edc63-124">金庫保管額を、勘定科目、または銀行口座へ転記するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="edc63-125">金庫保管額を転記する口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="edc63-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="edc63-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="edc63-126">Click Save.</span></span>


