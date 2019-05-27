---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 16 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 51cfe8a92d1ac611e946934fe8ebbc99053788f1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518483"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a><span data-ttu-id="3b944-103">Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 19 日)</span><span class="sxs-lookup"><span data-stu-id="3b944-103">What's new or changed in Dynamics 365 for Talent Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="3b944-104">**ビルド 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="3b944-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="3b944-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="3b944-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="3b944-106">管理者の休暇時間要求更新の許可</span><span class="sxs-lookup"><span data-stu-id="3b944-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="3b944-107">従業員の休暇時間要求は、ワークフローを通じて承認された後に更新する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="3b944-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="3b944-108">多くの場合、これらの更新は従業員の代理としてマネージャーにより行われます。</span><span class="sxs-lookup"><span data-stu-id="3b944-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="3b944-109">この新しい機能により、休暇時間の更新または休暇時間要求のキャンセルを従業員の代理としてマネージャーが行う機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="3b944-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="3b944-110">この能力は、**人材パラメーター**上で設定される**代わりに作業する**パラメーターにより制御されます。</span><span class="sxs-lookup"><span data-stu-id="3b944-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="3b944-111">HR の休暇時間要求更新の許可</span><span class="sxs-lookup"><span data-stu-id="3b944-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="3b944-112">上記の機能と同様に、従業員の休暇時間要求は、ワークフローを通じてすでに承認された後に更新する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="3b944-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="3b944-113">この機能により、HR ユーザーが休暇時間要求を更新する機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="3b944-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="3b944-114">**人員**ワークスペースおよび**作業者**ページにて、**休暇の表示**という新しいオプションを使用して、機能は有効になります。</span><span class="sxs-lookup"><span data-stu-id="3b944-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="3b944-115">それらのページ上で、マネージャーがアクションを実行するのと同様の方法で、HR ユーザーは要求の表示および休暇トランザクションの更新を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3b944-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="3b944-116">この機能へのアクセスを制御するセキュリティ職務権限は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3b944-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="3b944-117">職務権限: 作業者固有の休暇プロセスの管理。</span><span class="sxs-lookup"><span data-stu-id="3b944-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="3b944-118">権限: すべての作業者の休暇申請の管理。</span><span class="sxs-lookup"><span data-stu-id="3b944-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="3b944-119">その他の変更</span><span class="sxs-lookup"><span data-stu-id="3b944-119">Other changes</span></span>
<span data-ttu-id="3b944-120">このリリースでは次の更新が行われました。</span><span class="sxs-lookup"><span data-stu-id="3b944-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="3b944-121">作業者の採用アクションへの変更により、**ワークフロー完了**状態から移動できなくなることはありません。</span><span class="sxs-lookup"><span data-stu-id="3b944-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="3b944-122">雇用開始日がなくても採用レコードを作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3b944-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="3b944-123">従業員のセルフ サービスに表示されるコースに対する Dynamics 365 Talent の登録日について、タイム ゾーン オフセットを日付に適用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3b944-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="3b944-124">Excel ファイルは、**従業員エンティティ**を使用し、エラーを発生させずに複数回インポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="3b944-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="3b944-125">既知の問題</span><span class="sxs-lookup"><span data-stu-id="3b944-125">Known issue</span></span>

- <span data-ttu-id="3b944-126">**問題**: 作業者に新しい添付ファイルを追加する時、**新規**および**編集**ボタンが灰色表示になります。</span><span class="sxs-lookup"><span data-stu-id="3b944-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="3b944-127">**回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3b944-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="3b944-128">**作業者**ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="3b944-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="3b944-129">(この問題は次のプラットフォーム更新プログラムで修正されます。)</span><span class="sxs-lookup"><span data-stu-id="3b944-129">(This issue will be fixed in the next platform update.)</span></span>
