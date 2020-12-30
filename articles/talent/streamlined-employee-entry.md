---
title: 合理化された従業員の入力とナビゲーション
description: Dynamics 365 Talent の作業者データの入力が拡張され、過去、有効、または未来のすべての従業員に対して簡単な入力ができるようになりました。 簡易/連結ナビゲーション モデルが更新され、関連情報をすばやく検索し、必要な更新の表示と実行を行うことができるようになりました。
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: b73b420c2eb75077814fbfeb6cd17404c7efc11e
ms.sourcegitcommit: 436731d8b3889bebfe6f17922b0a31b1994f6796
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/26/2020
ms.locfileid: "4461818"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="913b8-104">合理化された従業員の入力とナビゲーション</span><span class="sxs-lookup"><span data-stu-id="913b8-104">Streamlined employee entry and navigation</span></span>

<span data-ttu-id="913b8-105">Dynamics 365 Talent により、従業員および雇用データを効率的に入力できます。</span><span class="sxs-lookup"><span data-stu-id="913b8-105">Dynamics 365 Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="913b8-106">過去、有効、および未来の従業員および契約社員の作業履歴情報をすばやく更新できます。</span><span class="sxs-lookup"><span data-stu-id="913b8-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="913b8-107">また、簡易ナビゲーション エクスペリエンスを有効にして、関連情報をすばやく検索し、必要な変更を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="913b8-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="913b8-108">この機能は、すべての環境で使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="913b8-108">This functionality is now available in all environments.</span></span> <span data-ttu-id="913b8-109">この機能を有効にするには、**システム管理 > 機能管理 > 新規 > 合理化された従業員エントリ > 有効にする** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="913b8-109">To turn this feature on, navigate to **System administration > Feature Management > New > Streamlined employee entry > Enable**.</span></span> <span data-ttu-id="913b8-110">これにより、これらの変更がすべてのユーザーに対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="913b8-110">This will enable these changes for all users.</span></span> <span data-ttu-id="913b8-111">このオプションはいつでもオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="913b8-111">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="913b8-112">オプションの表示</span><span class="sxs-lookup"><span data-stu-id="913b8-112">View options</span></span>

<span data-ttu-id="913b8-113">作業者フォームの **オプションの表示** を使用し、1 つの一覧から従業員と契約社員の組み合わせを選択できます。</span><span class="sxs-lookup"><span data-stu-id="913b8-113">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="913b8-114">これらのオプションにより、法人間、または現在サインインしている法人の従業員を表示できます。</span><span class="sxs-lookup"><span data-stu-id="913b8-114">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="913b8-115">また、有効、保留中、および退職した作業者を表示したり、作業者のタイプ (従業員または契約社員) に基づいて結果を制限したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="913b8-115">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="913b8-116">高度なセキュリティが有効にされている場合、アクセスできる法人の従業員と契約社員のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="913b8-116">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="913b8-117">リスト ビューの列は、選択に基づいて変更されます。</span><span class="sxs-lookup"><span data-stu-id="913b8-117">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="913b8-118">たとえば、退職した従業員を表示する場合、退職日および理由コードがリストに追加の列として表示されます。</span><span class="sxs-lookup"><span data-stu-id="913b8-118">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="913b8-119">[![オプションの表示](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="913b8-119">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="913b8-120">ナビゲーションおよびバナー</span><span class="sxs-lookup"><span data-stu-id="913b8-120">Navigation and banner</span></span>

<span data-ttu-id="913b8-121">バナーには、各作業者の重要な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="913b8-121">A banner displays key information for each worker.</span></span> <span data-ttu-id="913b8-122">有効な作業者のバナーには、次のフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="913b8-122">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="913b8-123">**肩書き**</span><span class="sxs-lookup"><span data-stu-id="913b8-123">**Title**</span></span>
- <span data-ttu-id="913b8-124">**部門**</span><span class="sxs-lookup"><span data-stu-id="913b8-124">**Department**</span></span>
- <span data-ttu-id="913b8-125">**職位タイプ**</span><span class="sxs-lookup"><span data-stu-id="913b8-125">**Position type**</span></span>
- <span data-ttu-id="913b8-126">**作業者タイプ**</span><span class="sxs-lookup"><span data-stu-id="913b8-126">**Worker type**</span></span>
- <span data-ttu-id="913b8-127">**マネージャー**</span><span class="sxs-lookup"><span data-stu-id="913b8-127">**Manager**</span></span>
- <span data-ttu-id="913b8-128">**法人エンティティ**</span><span class="sxs-lookup"><span data-stu-id="913b8-128">**Legal entity**</span></span>

<span data-ttu-id="913b8-129">退職した作業者のバナーには、次のフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="913b8-129">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="913b8-130">**退職日**</span><span class="sxs-lookup"><span data-stu-id="913b8-130">**Exited date**</span></span>
- <span data-ttu-id="913b8-131">**理由**</span><span class="sxs-lookup"><span data-stu-id="913b8-131">**Reason**</span></span>

<span data-ttu-id="913b8-132">保留中の作業者のバナーには、次のフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="913b8-132">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="913b8-133">**肩書き**</span><span class="sxs-lookup"><span data-stu-id="913b8-133">**Title**</span></span>
- <span data-ttu-id="913b8-134">**部門**</span><span class="sxs-lookup"><span data-stu-id="913b8-134">**Department**</span></span>
- <span data-ttu-id="913b8-135">**職位タイプ**</span><span class="sxs-lookup"><span data-stu-id="913b8-135">**Position type**</span></span>
- <span data-ttu-id="913b8-136">**マネージャー**</span><span class="sxs-lookup"><span data-stu-id="913b8-136">**Manager**</span></span>
- <span data-ttu-id="913b8-137">**開始日**</span><span class="sxs-lookup"><span data-stu-id="913b8-137">**Starting date**</span></span>
- <span data-ttu-id="913b8-138">**法人エンティティ**</span><span class="sxs-lookup"><span data-stu-id="913b8-138">**Legal entity**</span></span>

<span data-ttu-id="913b8-139">作業者ページのアクション ペインは、基本オプションを含めるように再編成されています。</span><span class="sxs-lookup"><span data-stu-id="913b8-139">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="913b8-140">情報は次のカテゴリに組織されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="913b8-140">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="913b8-141">作業</span><span class="sxs-lookup"><span data-stu-id="913b8-141">Work</span></span>
- <span data-ttu-id="913b8-142">名前</span><span class="sxs-lookup"><span data-stu-id="913b8-142">Person</span></span>
- <span data-ttu-id="913b8-143">休暇</span><span class="sxs-lookup"><span data-stu-id="913b8-143">Leave</span></span>
- <span data-ttu-id="913b8-144">報酬</span><span class="sxs-lookup"><span data-stu-id="913b8-144">Compensation</span></span>
- <span data-ttu-id="913b8-145">給付金</span><span class="sxs-lookup"><span data-stu-id="913b8-145">Benefits</span></span>
- <span data-ttu-id="913b8-146">コンプライアンス</span><span class="sxs-lookup"><span data-stu-id="913b8-146">Compliance</span></span>

<span data-ttu-id="913b8-147">さらに、作業者のメイン ページにある新しい **リンク** タブにより、ユーザーに作業者に関連する情報すべてにアクセスできる中心的な場所が与えられます。</span><span class="sxs-lookup"><span data-stu-id="913b8-147">In addition, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="913b8-148">これらの変更により、使用している場所とは異なる場所に情報が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="913b8-148">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="913b8-149">たとえば、以前、作業者フォームに表示されていた給与情報が **報酬 > 給与** の下のアクション ペインに表示され、**個人情報** タブの **詳細情報** ボタンにより、頻繁にアクセスされないフィールドを非表示にできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="913b8-149">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="913b8-150">[![バナー](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="913b8-150">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="913b8-151">作業履歴</span><span class="sxs-lookup"><span data-stu-id="913b8-151">Work history</span></span>

<span data-ttu-id="913b8-152">**作業履歴** タブに、すべての法人間での作業履歴が表示され、退職、有効、および保留中の従業員および契約社員に対して使用可能です。</span><span class="sxs-lookup"><span data-stu-id="913b8-152">The **Work history** tab shows work history across all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="913b8-153">アクセスできる法人について、すべての作業履歴を一度に表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="913b8-153">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="913b8-154">さらに、データ コンテキストを変更することなく、各作業履歴入力の情報を編集することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="913b8-154">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="913b8-155">ページ上のすべての情報を直接更新することができます。</span><span class="sxs-lookup"><span data-stu-id="913b8-155">You can update all information directly on the page.</span></span> 

<span data-ttu-id="913b8-156">[![作業履歴](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="913b8-156">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="913b8-157">職位履歴</span><span class="sxs-lookup"><span data-stu-id="913b8-157">Position history</span></span>

<span data-ttu-id="913b8-158">作業者のメイン ページの **職位** タブに、過去、現在、および未来のすべての割り当てを含む、組織内のすべての職位が完全表示されます。</span><span class="sxs-lookup"><span data-stu-id="913b8-158">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="913b8-159">アクション ペインで作業者の職位履歴に直接移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="913b8-159">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="913b8-160">[![職位](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="913b8-160">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

