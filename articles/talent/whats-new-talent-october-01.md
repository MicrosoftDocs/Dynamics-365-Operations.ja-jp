---
title: Dynamics 365 Talent - Core HR (2018 年 10 月 1 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
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
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ba7c84e5b1d15fb7a4894af31bbf6793b402b9e4
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008757"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-1-2018"></a><span data-ttu-id="c487c-103">Dynamics 365 Talent: Core HR (2018 年 10 月 1 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="c487c-103">What's new or changed in Dynamics 365 Talent: Core HR (October 1, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c487c-104">**ビルド 8.1.1035.0**</span><span class="sxs-lookup"><span data-stu-id="c487c-104">**Build 8.1.1035.0**</span></span>

<span data-ttu-id="c487c-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="c487c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="turn-off-electronic-payment-validation"></a><span data-ttu-id="c487c-106">電子支払の検証を無効化する</span><span class="sxs-lookup"><span data-stu-id="c487c-106">Turn off electronic payment validation</span></span>

<span data-ttu-id="c487c-107">**従業員セルフ サービス**ワークスペース (ESS) を通してまたは従業員フォームで直接に口座振込の出金を設定した場合、電子支払情報の検証が行われます。</span><span class="sxs-lookup"><span data-stu-id="c487c-107">Electronic payment information validation occurs if you set up disbursements for direct deposit either through **Employee self-service** workspace (ESS) or directly on the employee form.</span></span> <span data-ttu-id="c487c-108">このオプションを使用すると、金額と残余値の検証による確認が不要な場合に、その検証を柔軟に削除できます。</span><span class="sxs-lookup"><span data-stu-id="c487c-108">This option gives you the flexibility to remove that validation if you do not require the validation checks for amounts and remainder values.</span></span> <span data-ttu-id="c487c-109">この機能は、要件が異なる外部給与システムと統合している場合に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="c487c-109">This feature is helpful if you're integrating with an external payroll system that has different requirements.</span></span>

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a><span data-ttu-id="c487c-110">マネージャー セルフ サービス - チーム業績目標タイルを通じてチーム メンバーの目標の追加</span><span class="sxs-lookup"><span data-stu-id="c487c-110">Manager self-service - Add goals for team members through the Team performance goals tile</span></span>

<span data-ttu-id="c487c-111">今回のリリースまでは、管理者は、各従業員に関連付けられている業績目標を通して、その従業員個人に目標を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c487c-111">Prior to this release, managers can add goals to their employees individually through the performance goals associated to each employee.</span></span> <span data-ttu-id="c487c-112">この更新により、管理者は**チーム業績目標**タイルにアクセスでき、直属の部下のいずれかを選択して新しい目標を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c487c-112">With this update, managers can access the **Team performance goals** tile and create new goals by selecting any of their direct reports.</span></span>

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a><span data-ttu-id="c487c-113">マネージャー セルフ サービス - チーム業績レビュー タイルを通じてチーム メンバーのレビューの追加</span><span class="sxs-lookup"><span data-stu-id="c487c-113">Manager self-service - Add reviews for team members through the Team performance reviews tile</span></span>

<span data-ttu-id="c487c-114">今回のリリースまでは、管理者は、各従業員に関連付けられているレビューを通じて、その従業員個人にレビューを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c487c-114">Prior to this release, managers can add reviews to their employees individually through the reviews associated to each employee.</span></span> <span data-ttu-id="c487c-115">この更新により、管理者は**チーム業績レビュー**タイルにアクセスでき、直属の部下のいずれかを選択して新しいレビューを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c487c-115">With this update, managers can access the **Team performance reviews** tile and create new reviews by selecting any of their direct reports.</span></span>

## <a name="configure-proration-options-by-leave-plan"></a><span data-ttu-id="c487c-116">休暇計画による比例配分オプションのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c487c-116">Configure proration options by leave plan</span></span>

<span data-ttu-id="c487c-117">組織は、従業員の入社日および退社日に基づいて、休暇を別々に付与します。</span><span class="sxs-lookup"><span data-stu-id="c487c-117">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="c487c-118">一部の組織によっては、従業員は開始日に全額配賦され、他の従業員は報奨を比例配分します。</span><span class="sxs-lookup"><span data-stu-id="c487c-118">For some organizations, employees are awarded their full allocation on their start date while others prorate the award.</span></span> <span data-ttu-id="c487c-119">このリリースでは、組織内の入退社者に対する比例配分および見越計上を選択する方法に関する新しいオプションが提供されています。</span><span class="sxs-lookup"><span data-stu-id="c487c-119">New options are provided in this release to choose how to prorate the awards and accruals for joiners and leavers in an organization.</span></span> <span data-ttu-id="c487c-120">オプションには次のものがあります: 比例配分、完全な見越計上、および見越計上なし。</span><span class="sxs-lookup"><span data-stu-id="c487c-120">Options include: Prorated, Full accrual, and No accrual.</span></span>

## <a name="other-changes"></a><span data-ttu-id="c487c-121">その他の変更</span><span class="sxs-lookup"><span data-stu-id="c487c-121">Other changes</span></span>

-   <span data-ttu-id="c487c-122">更新された従業員エンティティ - **個人**タイトルは、Excel アドイン/データ管理を使用して更新できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c487c-122">Employee entity updated - The **Personal** title can now be updated using the Excel add-in/data management.</span></span>

-   <span data-ttu-id="c487c-123">支払情報の従業員セルフ サービスで、**削除**および**無効化**ボタンの削除を許可するセキュリティ変更。</span><span class="sxs-lookup"><span data-stu-id="c487c-123">Security change to allow removal of the **Delete** and **Deactivate** buttons in employee self-service for payment information.</span></span>

## <a name="known-issue"></a><span data-ttu-id="c487c-124">既知の問題</span><span class="sxs-lookup"><span data-stu-id="c487c-124">Known issue</span></span>

-   <span data-ttu-id="c487c-125">**問題:** 作業者に新しい添付ファイルを追加する場合、**新規**および**編集**ボタンは灰色表示です。**回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c487c-125">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="c487c-126">**作業者**ページが読み込まれるとき FactBoxes が閉じている場合、**添付ファイル**ボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="c487c-126">If the FactBoxes are closed when the **Worker** page is loaded, the **Attachments** buttons will be enabled.</span></span> <span data-ttu-id="c487c-127">(この問題は次のプラットフォーム更新プログラムで修正されます。)</span><span class="sxs-lookup"><span data-stu-id="c487c-127">(This issue will be fixed in the next platform update.)</span></span>
