---
title: 法人の作成
description: このトピックでは、Microsoft Dynamics 365 Commerce で法人を作成する方法について説明していますが、チャネルを作成する前に作成してコンフィギュレーションする必要があります。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 28cbcc42505f1dc90c420adc812735841541c8e0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002407"
---
# <a name="create-legal-entities"></a><span data-ttu-id="2b835-103">法人の作成</span><span class="sxs-lookup"><span data-stu-id="2b835-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2b835-104">このトピックでは、Microsoft Dynamics 365 Commerce で法人を作成する方法について説明していますが、チャネルを作成する前に作成してコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b835-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="2b835-105">概要</span><span class="sxs-lookup"><span data-stu-id="2b835-105">Overview</span></span>

<span data-ttu-id="2b835-106">法人とは、登記または法的手続きを済ませた法律上の構造を持つ組織です。</span><span class="sxs-lookup"><span data-stu-id="2b835-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="2b835-107">法人には、法的契約の締結が認められており、業績を報告する収支報告書の作成が義務付けられています。</span><span class="sxs-lookup"><span data-stu-id="2b835-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="2b835-108">会社とは、法人の 1 つのタイプです。</span><span class="sxs-lookup"><span data-stu-id="2b835-108">A company is a type of legal entity.</span></span> <span data-ttu-id="2b835-109">現在、会社はユーザーが作成できる唯一の法人であり、個々の法人は会社 ID と関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="2b835-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="2b835-110">この関連付けは、プログラム内の一部の機能エリアで法人 ID (データモデルでは *DataAreaId*) が使用されているために設けられています。</span><span class="sxs-lookup"><span data-stu-id="2b835-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="2b835-111">これらの機能エリアでは、データのセキュリティ区分として法人が使用されています。</span><span class="sxs-lookup"><span data-stu-id="2b835-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="2b835-112">ユーザーは、現在ログオン中の会社のデータにのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2b835-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="2b835-113">チャネルを作成するときは、チャネルが属している法人を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b835-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="2b835-114">新しい法人の作成</span><span class="sxs-lookup"><span data-stu-id="2b835-114">Create a new legal entity</span></span>

<span data-ttu-id="2b835-115">Dynamics 365 Commerce に新しい法人を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2b835-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2b835-116">ナビゲーション ウィンドウで、**モジュール \> 本社の設定 \> 法人** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2b835-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="2b835-117">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b835-117">On the action pane, select **New**.</span></span> <span data-ttu-id="2b835-118">**新しい法人**ウィンドウが右側に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b835-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="2b835-119">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="2b835-120">**会社**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="2b835-121">**国/地域**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2b835-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="2b835-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b835-122">Select **OK**.</span></span> 

   ![法人の作成](media/legal-entities.png)

1. <span data-ttu-id="2b835-124">**一般**セクションで、法人に関する次の一般情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b835-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="2b835-125">検索名が必要な場合、検索名を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="2b835-126">検索名は、この法人を検索するために使用できる代替名です。</span><span class="sxs-lookup"><span data-stu-id="2b835-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="2b835-127">この法人が連結会社として使用されているかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="2b835-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="2b835-128">この法人が削除会社として使用されているかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="2b835-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="2b835-129">エンティティの**既定の言語**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b835-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="2b835-130">エンティティの**タイム ゾーン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b835-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="2b835-131">**住所**セクションで、**編集**を選択して、番地、郵便番号、市区町村名などの住所情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="2b835-132">**連絡先情報**セクションで、電子メール アドレス、URL と電話番号など通信方法に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="2b835-133">**法定レポート**セクションで、法定レポートに使用される登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="2b835-134">**登録番号**セクションで、法人に必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="2b835-135">**銀行口座情報**セクションで、法人の銀行口座と処理番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="2b835-136">**対外貿易およびロジスティクス**セクションで、法人の出荷情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="2b835-137">**番号順序**セクションで、法人に関連付けられている番号順序を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2b835-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="2b835-138">開始時は空になります。</span><span class="sxs-lookup"><span data-stu-id="2b835-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="2b835-139">**ダッシュボードの画像**セクションで、法人に関連するロゴまたはダッシュボードの画像を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="2b835-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="2b835-140">**税登録**セクションで、税務当局に報告するために使用される登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="2b835-141">**税金 1099** セクションで、法人の 1099 情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="2b835-142">**税情報**セクションで、法人の税情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b835-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="2b835-143">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b835-143">Select **Save**.</span></span>

<span data-ttu-id="2b835-144">次の図は、法人の例の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="2b835-144">The following image shows details of an example legal entity.</span></span>

![法人の一般セクション](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="2b835-146">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2b835-146">Additional resources</span></span>

[<span data-ttu-id="2b835-147">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="2b835-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2b835-148">組織階層の計画</span><span class="sxs-lookup"><span data-stu-id="2b835-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2b835-149">組織階層</span><span class="sxs-lookup"><span data-stu-id="2b835-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="2b835-150">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="2b835-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="2b835-151">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="2b835-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)
