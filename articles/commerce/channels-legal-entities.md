---
title: 法人を作成します
description: このトピックでは、Microsoft Dynamics 365 Commerce で法人を作成する方法について説明していますが、チャネルを作成する前に作成してコンフィギュレーションする必要があります。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800618"
---
# <a name="create-legal-entities"></a><span data-ttu-id="d0481-103">法人を作成します</span><span class="sxs-lookup"><span data-stu-id="d0481-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d0481-104">このトピックでは、Microsoft Dynamics 365 Commerce で法人を作成する方法について説明していますが、チャネルを作成する前に作成してコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0481-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="d0481-105">法人とは、登記または法的手続きを済ませた法律上の構造を持つ組織です。</span><span class="sxs-lookup"><span data-stu-id="d0481-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="d0481-106">法人には、法的契約の締結が認められており、業績を報告する収支報告書の作成が義務付けられています。</span><span class="sxs-lookup"><span data-stu-id="d0481-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="d0481-107">会社とは、法人の 1 つのタイプです。</span><span class="sxs-lookup"><span data-stu-id="d0481-107">A company is a type of legal entity.</span></span> <span data-ttu-id="d0481-108">現在、会社はユーザーが作成できる唯一の法人であり、個々の法人は会社 ID と関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="d0481-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="d0481-109">この関連付けは、プログラム内の一部の機能エリアで法人 ID (データモデルでは *DataAreaId*) が使用されているために設けられています。</span><span class="sxs-lookup"><span data-stu-id="d0481-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="d0481-110">これらの機能エリアでは、データのセキュリティ区分として法人が使用されています。</span><span class="sxs-lookup"><span data-stu-id="d0481-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="d0481-111">ユーザーは、現在ログオン中の会社のデータにのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d0481-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="d0481-112">チャネルを作成するときは、チャネルが属している法人を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0481-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="d0481-113">新しい法人の作成</span><span class="sxs-lookup"><span data-stu-id="d0481-113">Create a new legal entity</span></span>

<span data-ttu-id="d0481-114">Dynamics 365 Commerce に新しい法人を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d0481-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d0481-115">ナビゲーション ウィンドウで、**モジュール \> 本社の設定 \> 法人** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0481-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="d0481-116">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0481-116">On the action pane, select **New**.</span></span> <span data-ttu-id="d0481-117">**新しい法人** ウィンドウが右側に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d0481-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="d0481-118">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="d0481-119">**会社** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="d0481-120">**国/地域** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d0481-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="d0481-121">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0481-121">Select **OK**.</span></span> 

   ![法人の作成](media/legal-entities.png)

1. <span data-ttu-id="d0481-123">**一般** セクションで、法人に関する次の一般情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d0481-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="d0481-124">検索名が必要な場合、検索名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="d0481-125">検索名は、この法人を検索するために使用できる代替名です。</span><span class="sxs-lookup"><span data-stu-id="d0481-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="d0481-126">この法人が連結会社として使用されているかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0481-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="d0481-127">この法人が削除会社として使用されているかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0481-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="d0481-128">エンティティの **既定の言語** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0481-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="d0481-129">エンティティの **タイム ゾーン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0481-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="d0481-130">**住所** セクションで、**編集** を選択して、番地、郵便番号、市区町村名などの住所情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="d0481-131">**連絡先情報** セクションで、電子メール アドレス、URL と電話番号など通信方法に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="d0481-132">**法定レポート** セクションで、法定レポートに使用される登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="d0481-133">**登録番号** セクションで、法人に必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="d0481-134">**銀行口座情報** セクションで、法人の銀行口座と処理番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="d0481-135">**対外貿易およびロジスティクス** セクションで、法人の出荷情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="d0481-136">**番号順序** セクションで、法人に関連付けられている番号順序を表示できます。</span><span class="sxs-lookup"><span data-stu-id="d0481-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="d0481-137">開始時は空になります。</span><span class="sxs-lookup"><span data-stu-id="d0481-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="d0481-138">**ダッシュボードの画像** セクションで、法人に関連するロゴまたはダッシュボードの画像を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="d0481-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="d0481-139">**税登録** セクションで、税務当局に報告するために使用される登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="d0481-140">**税金 1099** セクションで、法人の 1099 情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="d0481-141">**税情報** セクションで、法人の税情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0481-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="d0481-142">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0481-142">Select **Save**.</span></span>

<span data-ttu-id="d0481-143">次の図は、法人の例の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="d0481-143">The following image shows details of an example legal entity.</span></span>

![法人の一般セクション](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="d0481-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d0481-145">Additional resources</span></span>

[<span data-ttu-id="d0481-146">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="d0481-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d0481-147">組織階層の計画</span><span class="sxs-lookup"><span data-stu-id="d0481-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d0481-148">組織階層</span><span class="sxs-lookup"><span data-stu-id="d0481-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="d0481-149">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="d0481-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d0481-150">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="d0481-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
