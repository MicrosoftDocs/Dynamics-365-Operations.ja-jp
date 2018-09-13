--- 
title: "法人の作成"
description: "法人は、法的権利の登録によって識別される組織です。"
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMLegalEntity, OMNewLegalEntity
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: abd59b96a2e5dceb2492c2db2c617485b332fbd3
ms.openlocfilehash: 2b1869afa9ebbfc81ca321c57cc8e01739103d16
ms.contentlocale: ja-jp
ms.lasthandoff: 09/13/2018

---
# <a name="create-a-legal-entity"></a><span data-ttu-id="525da-103">法人の作成</span><span class="sxs-lookup"><span data-stu-id="525da-103">Create a legal entity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="525da-104">法人は、法的権利の登録によって識別される組織です。</span><span class="sxs-lookup"><span data-stu-id="525da-104">A legal entity is an organization that is identified through registration with a legal authority.</span></span> <span data-ttu-id="525da-105">法人には、契約の締結が認められており、業績を報告する収支報告書の作成が義務付けられています。</span><span class="sxs-lookup"><span data-stu-id="525da-105">Legal entities can enter into contracts and are required to prepare statements that report on their performance.</span></span> <span data-ttu-id="525da-106">次の手順では、法人の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="525da-106">The following procedure explains how to create a legal entity.</span></span> <span data-ttu-id="525da-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="525da-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="525da-108">[組織管理] > [組織] > [法人] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="525da-108">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="525da-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="525da-109">Click New.</span></span>
3. <span data-ttu-id="525da-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="525da-111">[会社] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-111">In the Company field, type a value.</span></span>
5. <span data-ttu-id="525da-112">[国/地域] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="525da-112">In the Country/region field, enter or select a value.</span></span>
6. <span data-ttu-id="525da-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="525da-113">Click OK.</span></span>
    * <span data-ttu-id="525da-114">[一般] セクションで、法人に関する次の一般情報を指定します。検索名が必要な場合、検索名を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-114">In the General section, provide the following general information about the legal entity: Enter a search name, if a search name is required.</span></span> <span data-ttu-id="525da-115">検索名は、この法人を検索するために使用できる代替名です。</span><span class="sxs-lookup"><span data-stu-id="525da-115">A search name is an alternate name that can be used to search for this legal entity.</span></span> <span data-ttu-id="525da-116">この法人が連結会社として使用されているかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="525da-116">Select whether this legal entity is being used as a consolidation company.</span></span> <span data-ttu-id="525da-117">この法人が削除会社として使用されているかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="525da-117">Select whether this legal entity is being used as an elimination company.</span></span>  
7. <span data-ttu-id="525da-118">[住所] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-118">Expand the Addresses section.</span></span>
    * <span data-ttu-id="525da-119">[住所] セクションで、番地、郵便番号、市区町村名などの住所情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-119">In the Addresses section, enter address information, such as the street name and number, postal code, and city.</span></span>  
8. <span data-ttu-id="525da-120">[連絡先情報] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-120">Expand the Contact information section.</span></span>
    * <span data-ttu-id="525da-121">[連絡先情報] セクションで、電子メール アドレス、URL と電話番号など通信方法に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-121">In the Contact information section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>  
9. <span data-ttu-id="525da-122">[法定レポート] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-122">Expand the Statutory reporting section.</span></span>
    * <span data-ttu-id="525da-123">[法定レポート] セクションで、法定レポートに使用される登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-123">In the Statutory reporting section, enter the registration numbers that are used for statutory reporting.</span></span>  
10. <span data-ttu-id="525da-124">[登録番号] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-124">Expand the Registration numbers section.</span></span>
    * <span data-ttu-id="525da-125">[登録番号] セクションで、法人に必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-125">In the Registration numbers section, enter any information required by the legal entity.</span></span>  
11. <span data-ttu-id="525da-126">[銀行口座情報] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-126">Expand the Bank account information section.</span></span>
    * <span data-ttu-id="525da-127">[銀行口座情報] セクションで、法人の銀行口座と処理番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-127">In the Bank account information section, enter bank accounts and routing numbers for the legal entity.</span></span>  
12. <span data-ttu-id="525da-128">[対外貿易およびロジスティクス] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-128">Expand the Foreign trade and logistics section.</span></span>
    * <span data-ttu-id="525da-129">[対外貿易およびロジスティクス] セクションで、法人の出荷情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-129">In the Foreign trade and logistics section, enter shipping information for the legal entity.</span></span>  
13. <span data-ttu-id="525da-130">[番号順序] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-130">Expand the Number sequences section.</span></span>
    * <span data-ttu-id="525da-131">[番号順序] セクションで、法人に関連付けられている番号順序を表示できます。</span><span class="sxs-lookup"><span data-stu-id="525da-131">In the Number sequences section, you can view the number sequences that are associated with the legal entity.</span></span>  
14. <span data-ttu-id="525da-132">[画像] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-132">Expand the Images section.</span></span>
    * <span data-ttu-id="525da-133">[画像] セクションで、法人に関連するロゴまたはダッシュボードの画像を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="525da-133">In the Images section, view or change the logo and/or dashboard image that are associated with the legal entity.</span></span>  
15. <span data-ttu-id="525da-134">[税登録] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-134">Expand the Tax registration section.</span></span>
    * <span data-ttu-id="525da-135">[税登録] セクションで、税務当局に報告するために使用される登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-135">In the Tax registration section, enter the registration numbers that are used to report to tax authorities.</span></span>  
16. <span data-ttu-id="525da-136">[税金 1099] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="525da-136">Expand the Tax 1099 section.</span></span>
    * <span data-ttu-id="525da-137">[税金 1099] セクションで、法人の 1099 情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="525da-137">In the Tax 1099 section, enter 1099 information for the legal entity.</span></span>  
17. <span data-ttu-id="525da-138">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="525da-138">Click Save.</span></span>


