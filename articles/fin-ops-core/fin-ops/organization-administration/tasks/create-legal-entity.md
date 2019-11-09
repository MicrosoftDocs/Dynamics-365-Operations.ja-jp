---
title: 法人の作成
description: 法人は、法的権利の登録によって識別される組織です。
author: sericks007
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntity, OMNewLegalEntity
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f63591d2bdb88de8c9bc7a544ac4f3adbab90a7c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178743"
---
# <a name="create-a-legal-entity"></a><span data-ttu-id="c259a-103">法人の作成</span><span class="sxs-lookup"><span data-stu-id="c259a-103">Create a legal entity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c259a-104">法人は、法的権利の登録によって識別される組織です。</span><span class="sxs-lookup"><span data-stu-id="c259a-104">A legal entity is an organization that is identified through registration with a legal authority.</span></span> <span data-ttu-id="c259a-105">法人には、契約の締結が認められており、業績を報告する収支報告書の作成が義務付けられています。</span><span class="sxs-lookup"><span data-stu-id="c259a-105">Legal entities can enter into contracts and are required to prepare statements that report on their performance.</span></span> <span data-ttu-id="c259a-106">次の手順では、法人の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c259a-106">The following procedure explains how to create a legal entity.</span></span> <span data-ttu-id="c259a-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c259a-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c259a-108">**ナビゲーション ウィンドウ > モジュール > 組織管理 > 組織 > 法人**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c259a-108">Go to **Navigation pane > Modules > Organization administration > Organizations > Legal entities**.</span></span>
2. <span data-ttu-id="c259a-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c259a-109">Click **New**.</span></span>
3. <span data-ttu-id="c259a-110">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="c259a-111">**会社**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-111">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="c259a-112">**国/地域**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c259a-112">In the **Country/region** field, enter or select a value.</span></span>
6. <span data-ttu-id="c259a-113">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c259a-113">Click **OK**.</span></span> <span data-ttu-id="c259a-114">**一般**セクションで、法人に関する次の一般情報を指定します。検索名が必要な場合、検索名を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-114">In the **General** section, provide the following general information about the legal entity: Enter a search name, if a search name is required.</span></span> <span data-ttu-id="c259a-115">検索名は、この法人を検索するために使用できる代替名です。</span><span class="sxs-lookup"><span data-stu-id="c259a-115">A search name is an alternate name that can be used to search for this legal entity.</span></span> <span data-ttu-id="c259a-116">この法人が連結会社として使用されているかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="c259a-116">Select whether this legal entity is being used as a consolidation company.</span></span> <span data-ttu-id="c259a-117">この法人が削除会社として使用されているかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="c259a-117">Select whether this legal entity is being used as an elimination company.</span></span> 
7. <span data-ttu-id="c259a-118">**住所**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-118">Expand the **Addresses** section.</span></span> <span data-ttu-id="c259a-119">**住所**セクションで、**編集**をクリックして、番地、郵便番号、市区町村名などの住所情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-119">In the **Addresses** section, click **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
8. <span data-ttu-id="c259a-120">**連絡先情報**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-120">Expand the **Contact information** section.</span></span> <span data-ttu-id="c259a-121">**連絡先情報**セクションで、電子メール アドレス、URL と電話番号など通信方法に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-121">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span> 
9. <span data-ttu-id="c259a-122">**法定レポート**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-122">Expand the **Statutory reporting** section.</span></span> <span data-ttu-id="c259a-123">**法定レポート**セクションで、法定レポートに使用される登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-123">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
10. <span data-ttu-id="c259a-124">**登録番号**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-124">Expand the **Registration numbers** section.</span></span> <span data-ttu-id="c259a-125">**登録番号**セクションで、法人に必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-125">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>  
11. <span data-ttu-id="c259a-126">**銀行口座情報**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-126">Expand the **Bank account information** section.</span></span> <span data-ttu-id="c259a-127">**銀行口座情報**セクションで、法人の銀行口座と処理番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-127">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
12. <span data-ttu-id="c259a-128">**対外貿易およびロジスティクス**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-128">Expand the **Foreign trade and logistics** section.</span></span> <span data-ttu-id="c259a-129">**対外貿易およびロジスティクス**セクションで、法人の出荷情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-129">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>  
13. <span data-ttu-id="c259a-130">**番号順序**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-130">Expand the **Number sequences** section.</span></span> <span data-ttu-id="c259a-131">**番号順序**セクションで、法人に関連付けられている番号順序を表示できます。</span><span class="sxs-lookup"><span data-stu-id="c259a-131">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span>  
14. <span data-ttu-id="c259a-132">**画像**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-132">Expand the **Images** section.</span></span> <span data-ttu-id="c259a-133">**画像**セクションで、法人に関連するロゴまたはダッシュボードの画像を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="c259a-133">In the **Images** section, view or change the logo and/or dashboard image that are associated with the legal entity.</span></span>  
15. <span data-ttu-id="c259a-134">**税登録**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-134">Expand the **Tax registration** section.</span></span> <span data-ttu-id="c259a-135">**税登録**セクションで、税務当局に報告するために使用される登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-135">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
16. <span data-ttu-id="c259a-136">**税金 1099** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c259a-136">Expand the **Tax 1099** section.</span></span> <span data-ttu-id="c259a-137">**税金 1099** セクションで、法人の 1099 情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c259a-137">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>  
17. <span data-ttu-id="c259a-138">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c259a-138">Click **Save**.</span></span>