---
title: 合理化された従業員の入力とナビゲーション
description: Dynamics 365 for Talent の作業者データの入力が拡張され、過去、有効、または未来のすべての従業員に対して簡単な入力ができるようになりました。 簡易/連結ナビゲーション モデルが更新され、関連情報をすばやく検索し、必要な更新の表示と実行を行うことができるようになりました。
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
ms.openlocfilehash: be0253ffc4396f36050ef02c51a20d378e44473d
ms.sourcegitcommit: 4176c333ce3f88c5c68e95bd47e5791d32365dd2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1918209"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="a74d8-104">合理化された従業員の入力とナビゲーション</span><span class="sxs-lookup"><span data-stu-id="a74d8-104">Streamlined employee entry and navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a74d8-105">Dynamics 365 for Talent により、従業員および雇用データを効率的に入力できます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-105">Dynamics 365 for Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="a74d8-106">過去、有効、および未来の従業員および契約社員の作業履歴情報をすばやく更新できます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="a74d8-107">また、簡易ナビゲーション エクスペリエンスを有効にして、関連情報をすばやく検索し、必要な変更を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="a74d8-108">この機能は、サンドボックス環境で使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="a74d8-108">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="a74d8-109">この機能を有効にするには、**システム管理 > リンク > 設定 > システム パラメーター > プレビュー機能**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a74d8-109">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="a74d8-110">**拡張された作業者フォームおよびナビゲーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a74d8-110">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="a74d8-111">これにより、これらの変更がすべてのユーザーに対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="a74d8-111">This will enable these changes for all users.</span></span> <span data-ttu-id="a74d8-112">このオプションはいつでもオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-112">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="a74d8-113">オプションの表示</span><span class="sxs-lookup"><span data-stu-id="a74d8-113">View options</span></span>

<span data-ttu-id="a74d8-114">作業者フォームの**オプションの表示**を使用し、1 つの一覧から従業員と契約社員の組み合わせを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-114">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="a74d8-115">これらのオプションにより、法人間、または現在サインインしている法人の従業員を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-115">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="a74d8-116">また、有効、保留中、および退職した作業者を表示したり、作業者のタイプ (従業員または契約社員) に基づいて結果を制限したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-116">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="a74d8-117">高度なセキュリティが有効にされている場合、アクセスできる法人の従業員と契約社員のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-117">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="a74d8-118">リスト ビューの列は、選択に基づいて変更されます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-118">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="a74d8-119">たとえば、退職した従業員を表示する場合、退職日および理由コードがリストに追加の列として表示されます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-119">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="a74d8-120">[![オプションの表示](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="a74d8-120">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="a74d8-121">ナビゲーションおよびバナー</span><span class="sxs-lookup"><span data-stu-id="a74d8-121">Navigation and banner</span></span>

<span data-ttu-id="a74d8-122">バナーには、各作業者の重要な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-122">A banner displays key information for each worker.</span></span> <span data-ttu-id="a74d8-123">有効な作業者のバナーには、次のフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-123">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="a74d8-124">**肩書き**</span><span class="sxs-lookup"><span data-stu-id="a74d8-124">**Title**</span></span>
- <span data-ttu-id="a74d8-125">**部門**</span><span class="sxs-lookup"><span data-stu-id="a74d8-125">**Department**</span></span>
- <span data-ttu-id="a74d8-126">**職位タイプ**</span><span class="sxs-lookup"><span data-stu-id="a74d8-126">**Position type**</span></span>
- <span data-ttu-id="a74d8-127">**作業者タイプ**</span><span class="sxs-lookup"><span data-stu-id="a74d8-127">**Worker type**</span></span>
- <span data-ttu-id="a74d8-128">**マネージャー**</span><span class="sxs-lookup"><span data-stu-id="a74d8-128">**Manager**</span></span>
- <span data-ttu-id="a74d8-129">**法人エンティティ**</span><span class="sxs-lookup"><span data-stu-id="a74d8-129">**Legal entity**</span></span>

<span data-ttu-id="a74d8-130">退職した作業者のバナーには、次のフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-130">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="a74d8-131">**退職日**</span><span class="sxs-lookup"><span data-stu-id="a74d8-131">**Exited date**</span></span>
- <span data-ttu-id="a74d8-132">**理由**</span><span class="sxs-lookup"><span data-stu-id="a74d8-132">**Reason**</span></span>

<span data-ttu-id="a74d8-133">保留中の作業者のバナーには、次のフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-133">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="a74d8-134">**肩書き**</span><span class="sxs-lookup"><span data-stu-id="a74d8-134">**Title**</span></span>
- <span data-ttu-id="a74d8-135">**部門**</span><span class="sxs-lookup"><span data-stu-id="a74d8-135">**Department**</span></span>
- <span data-ttu-id="a74d8-136">**職位タイプ**</span><span class="sxs-lookup"><span data-stu-id="a74d8-136">**Position type**</span></span>
- <span data-ttu-id="a74d8-137">**マネージャー**</span><span class="sxs-lookup"><span data-stu-id="a74d8-137">**Manager**</span></span>
- <span data-ttu-id="a74d8-138">**開始日**</span><span class="sxs-lookup"><span data-stu-id="a74d8-138">**Starting date**</span></span>
- <span data-ttu-id="a74d8-139">**法人エンティティ**</span><span class="sxs-lookup"><span data-stu-id="a74d8-139">**Legal entity**</span></span>

<span data-ttu-id="a74d8-140">作業者ページのアクション ペインは、基本オプションを含めるように再編成されています。</span><span class="sxs-lookup"><span data-stu-id="a74d8-140">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="a74d8-141">情報は次のカテゴリに組織されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a74d8-141">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="a74d8-142">作業</span><span class="sxs-lookup"><span data-stu-id="a74d8-142">Work</span></span>
- <span data-ttu-id="a74d8-143">名前</span><span class="sxs-lookup"><span data-stu-id="a74d8-143">Person</span></span>
- <span data-ttu-id="a74d8-144">離脱</span><span class="sxs-lookup"><span data-stu-id="a74d8-144">Leave</span></span>
- <span data-ttu-id="a74d8-145">報酬</span><span class="sxs-lookup"><span data-stu-id="a74d8-145">Compensation</span></span>
- <span data-ttu-id="a74d8-146">福利厚生</span><span class="sxs-lookup"><span data-stu-id="a74d8-146">Benefits</span></span>
- <span data-ttu-id="a74d8-147">コンプライアンス</span><span class="sxs-lookup"><span data-stu-id="a74d8-147">Compliance</span></span>

<span data-ttu-id="a74d8-148">さらに、作業者のメイン ページにある新しい**リンク** タブにより、ユーザーに作業者に関連する情報すべてにアクセスできる中心的な場所が与えられます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-148">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="a74d8-149">これらの変更により、使用している場所とは異なる場所に情報が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="a74d8-149">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="a74d8-150">たとえば、以前、作業者フォームに表示されていた給与情報が**報酬 > 給与**の下のアクション ペインに表示され、**個人情報**タブの**詳細情報**ボタンにより、頻繁にアクセスされないフィールドを非表示にできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a74d8-150">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="a74d8-151">[![バナー](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="a74d8-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="a74d8-152">作業履歴</span><span class="sxs-lookup"><span data-stu-id="a74d8-152">Work history</span></span>

<span data-ttu-id="a74d8-153">**作業履歴**タブに、すべての法人間での作業履歴が表示され、退職、有効、および保留中の従業員および契約社員に対して使用可能です。</span><span class="sxs-lookup"><span data-stu-id="a74d8-153">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="a74d8-154">アクセスできる法人について、すべての作業履歴を一度に表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a74d8-154">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="a74d8-155">さらに、データ コンテキストを変更することなく、各作業履歴入力の情報を編集することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a74d8-155">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="a74d8-156">ページ上のすべての情報を直接更新することができます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-156">You can update all information directly on the page.</span></span> 

<span data-ttu-id="a74d8-157">[![作業履歴](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="a74d8-157">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="a74d8-158">職位履歴</span><span class="sxs-lookup"><span data-stu-id="a74d8-158">Position history</span></span>

<span data-ttu-id="a74d8-159">作業者のメイン ページの**職位**タブに、過去、現在、および未来のすべての割り当てを含む、組織内のすべての職位が完全表示されます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-159">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="a74d8-160">アクション ペインで作業者の職位履歴に直接移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="a74d8-160">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="a74d8-161">[![職位](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="a74d8-161">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

