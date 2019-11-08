---
title: Dynamics 365 Talent - Core HR (2018 年 11 月 15 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a571568850a675f3472f2b62df33c0c35d905af0
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551383"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a><span data-ttu-id="fa686-103">Dynamics 365 Talent - Core HR (2018 年 11 月 15 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="fa686-103">What's new or changed in Dynamics 365 Talent - Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa686-104">**ビルド 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="fa686-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="fa686-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="fa686-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="fa686-106">その他の変更または修正</span><span class="sxs-lookup"><span data-stu-id="fa686-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="fa686-107">従業員の現在の職位を将来の空いている職位に変更することができない</span><span class="sxs-lookup"><span data-stu-id="fa686-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="fa686-108">職位が将来でのみ利用可能な場合、職位の転送を有効にするための変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="fa686-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="fa686-109">新しい従業員を作成するときに職位が表示されない</span><span class="sxs-lookup"><span data-stu-id="fa686-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="fa686-110">Talent で新しい従業員を採用するときに割り当て可能なすべての空いている職位を表示するための変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="fa686-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="fa686-111">これには、過去の職位または、職位が将来の日付になっているかどうかが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fa686-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="fa686-112">職位が雇用開始日に基づいて正しく表示されます。</span><span class="sxs-lookup"><span data-stu-id="fa686-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="fa686-113">退職日はユーザーの設定に基づいて表示される</span><span class="sxs-lookup"><span data-stu-id="fa686-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="fa686-114">退職日を表示しているときに、従業員の優先タイム ゾーンのタイム ゾーン オフセットを考慮に入れるための変更が過去の従業員のリストに行われました。</span><span class="sxs-lookup"><span data-stu-id="fa686-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="fa686-115">自分に割り当てられた作業項目のリンクが正しい情報を表示しない</span><span class="sxs-lookup"><span data-stu-id="fa686-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="fa686-116">この変更により、個々の作業項目のリストの詳細へのナビゲーションは、選択した項目の正しい情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="fa686-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="fa686-117">この問題は、高度なセキュリティ オプションでのみ発生しました。</span><span class="sxs-lookup"><span data-stu-id="fa686-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="fa686-118">既知の問題</span><span class="sxs-lookup"><span data-stu-id="fa686-118">Known issue</span></span>

- <span data-ttu-id="fa686-119">**問題**: 作業者に新しい添付ファイルを追加する時、**新規**および**編集**ボタンが灰色表示になります。</span><span class="sxs-lookup"><span data-stu-id="fa686-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="fa686-120">**回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa686-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="fa686-121">**作業者**ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="fa686-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="fa686-122">(この問題は次のプラットフォーム更新プログラムで修正されます。)</span><span class="sxs-lookup"><span data-stu-id="fa686-122">(This issue will be fixed in the next platform update.)</span></span>
