---
title: Dynamics 365 Talent - Core HR の新機能および変更された機能 (2018 年 8 月)
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: db7c91ea6599bde7d4c589a021d2d3b262e57ec9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010455"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-august-2018"></a><span data-ttu-id="3b567-103">Dynamics 365 Talent: Core HR の新機能または変更された機能 (2018 年 8 月)</span><span class="sxs-lookup"><span data-stu-id="3b567-103">What's new or changed in Dynamics 365 Talent: Core HR (August 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b567-104">**ビルド 8.1.104**</span><span class="sxs-lookup"><span data-stu-id="3b567-104">**Build 8.1.104**</span></span>

<span data-ttu-id="3b567-105">このトピックでは、Dynamics 365 Talent: Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="3b567-105">This topic describes features that are either new or changed in Dynamics 365 Talent: Core HR.</span></span>

## <a name="view-expiring-records-in-manager-self-service"></a><span data-ttu-id="3b567-106">マネージャー セルフ サービスで期限が切れるレコードの表示</span><span class="sxs-lookup"><span data-stu-id="3b567-106">View expiring records in Manager self service</span></span>

<span data-ttu-id="3b567-107">マネージャー セルフ サービスで期限が切れるレコードを表示できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3b567-107">You can now view expiring records in Manager self-service.</span></span> <span data-ttu-id="3b567-108">新しいオプションでは、管理者が表示用に使用する情報を構成できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3b567-108">New options are allow you to configure what information will be available for managers to view.</span></span> <span data-ttu-id="3b567-109">コピーされるフィールドは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3b567-109">These include:</span></span>

-   <span data-ttu-id="3b567-110">証明書</span><span class="sxs-lookup"><span data-stu-id="3b567-110">Certificates</span></span>

-   <span data-ttu-id="3b567-111">ID 番号</span><span class="sxs-lookup"><span data-stu-id="3b567-111">Identification numbers</span></span>

-   <span data-ttu-id="3b567-112">猶予期間</span><span class="sxs-lookup"><span data-stu-id="3b567-112">Probation periods</span></span>

-   <span data-ttu-id="3b567-113">審査</span><span class="sxs-lookup"><span data-stu-id="3b567-113">Screenings</span></span>

-   <span data-ttu-id="3b567-114">テスト</span><span class="sxs-lookup"><span data-stu-id="3b567-114">Tests</span></span>

<span data-ttu-id="3b567-115">この機能は、期限切れになるレコードを検索する日数の範囲も指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3b567-115">This feature also gives you the ability to specify the range of days in which to look for expiring records.</span></span>

## <a name="configurable-transfer-actions"></a><span data-ttu-id="3b567-116">構成可能な移動アクション</span><span class="sxs-lookup"><span data-stu-id="3b567-116">Configurable transfer actions</span></span>

<span data-ttu-id="3b567-117">転送要求の入力中に利用可能なオプションをロール別に構成できます。</span><span class="sxs-lookup"><span data-stu-id="3b567-117">You can configure by role the options that will be available during the entry of a transfer request.</span></span> <span data-ttu-id="3b567-118">この機能は、組織内のロール間でさらに柔軟性を提供します。</span><span class="sxs-lookup"><span data-stu-id="3b567-118">This feature provides additional flexibility across the roles in an organization.</span></span>

<span data-ttu-id="3b567-119">たとえば、従業員の転送を要求するマネージャには、報酬金額を提案または入力する、または転送要求に関連付けられるタスク リストを選択するためのアクセス権がない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3b567-119">For example, managers requesting employee transfers may not have access to suggest or enter compensation amounts or select the task lists that will be associated with the transfer request.</span></span> <span data-ttu-id="3b567-120">この場合、マネージャは転送要求を作成または送信できますが、報酬またはタスク リストの割り当てを入力することはできません。</span><span class="sxs-lookup"><span data-stu-id="3b567-120">In this case, managers can create and submit transfer requests but are not allowed to enter compensation or task list assignments.</span></span> <span data-ttu-id="3b567-121">この同じ構成で、HR は新しい報酬値を割り当てると共に、転送完了の結果として完了するための任意の追加のチェックリストを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="3b567-121">In this same configuration, HR will be able to assign the new compensation values as well as assign any additional checklists to be completed as a result of the transfer completing.</span></span>

<span data-ttu-id="3b567-122">既定では、新しい構成オプションはこの更新の前に処理能力を変更しないよう設定されています。</span><span class="sxs-lookup"><span data-stu-id="3b567-122">By default, the new configuration options are set to not change the capabilities prior to this update.</span></span>

## <a name="leave-and-absence"></a><span data-ttu-id="3b567-123">休暇</span><span class="sxs-lookup"><span data-stu-id="3b567-123">Leave and absence</span></span>

<span data-ttu-id="3b567-124">追加の日付フィールドが休暇で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3b567-124">There are now additional Date fields available in Leave and Absence.</span></span>

<span data-ttu-id="3b567-125">この機能により、特定の従業員の日付を使用する計画レベルで見越計上期間の基準を設定できます。</span><span class="sxs-lookup"><span data-stu-id="3b567-125">With this feature you can set the accrual period basis at the plan level to use specific employee dates.</span></span> <span data-ttu-id="3b567-126">これにより、休暇の見越計上処理中に使用される計画の開始日以外の日付を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b567-126">This allows for dates other than the plan start date to be used during the leave accrual process.</span></span> <span data-ttu-id="3b567-127">従業員の特定の日付のオプションには、次の値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3b567-127">Options for employee specific dates include the following values:</span></span>

-   <span data-ttu-id="3b567-128">カスタム (この更新前に使用可能)</span><span class="sxs-lookup"><span data-stu-id="3b567-128">Custom (available prior to this update)</span></span>

-   <span data-ttu-id="3b567-129">記念日</span><span class="sxs-lookup"><span data-stu-id="3b567-129">Anniversary date</span></span>

-   <span data-ttu-id="3b567-130">元の採用日付</span><span class="sxs-lookup"><span data-stu-id="3b567-130">Original hire date</span></span>

-   <span data-ttu-id="3b567-131">勤続日数</span><span class="sxs-lookup"><span data-stu-id="3b567-131">Seniority date</span></span>

-   <span data-ttu-id="3b567-132">作業者の調整済開始日</span><span class="sxs-lookup"><span data-stu-id="3b567-132">Worker’s adjusted start date</span></span>

-   <span data-ttu-id="3b567-133">作業者の開始日</span><span class="sxs-lookup"><span data-stu-id="3b567-133">Worker’s start date</span></span>

<span data-ttu-id="3b567-134">従業員の特定の日付のいずれかを使用するように構成する場合は、登録プロセスでは指定された日付を使用して見越計上期間を計算します。</span><span class="sxs-lookup"><span data-stu-id="3b567-134">When configured to use one of the employee specific dates, the enrollment process will use the specified date to calculate the accrual periods.</span></span> <span data-ttu-id="3b567-135">見越計上期間の基準は、見越計上処理中に何が使用されるかを理解するための従業員の計画登録にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="3b567-135">The accrual period basis is also displayed on the employee’s plan enrollment to help you understand what’s being used during the accrual process.</span></span>

## <a name="microsoft-word-integration"></a><span data-ttu-id="3b567-136">Microsoft Word 統合</span><span class="sxs-lookup"><span data-stu-id="3b567-136">Microsoft Word integration</span></span>

<span data-ttu-id="3b567-137">ドキュメント テンプレートは Core HR 全体で有効になります。</span><span class="sxs-lookup"><span data-stu-id="3b567-137">Document templates have been enabled throughout Core HR.</span></span> <span data-ttu-id="3b567-138">この機能により、作成した Word テンプレートに基づく文字およびレポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="3b567-138">This feature allows you to create letters and reports based on Word templates that you create.</span></span>

<span data-ttu-id="3b567-139">この機能に関する追加情報は、[Office 統合のチュートリアル](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json) で参照できます。</span><span class="sxs-lookup"><span data-stu-id="3b567-139">Additional information about this feature is available in the [Office integration tutorial](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span></span>


## <a name="other-fixes"></a><span data-ttu-id="3b567-140">その他の修正</span><span class="sxs-lookup"><span data-stu-id="3b567-140">Other fixes</span></span>

<span data-ttu-id="3b567-141">今回のリリースには、複数のバグ修正、新しいエンティティの追加、既存のエンティティの修正、およびローカライズされたラベルの変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3b567-141">This release also includes a number of bug fixes, the addition of new entities, fixes to existing entities, and localized label changes.</span></span>
