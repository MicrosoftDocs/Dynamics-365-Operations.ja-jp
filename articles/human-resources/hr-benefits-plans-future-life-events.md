---
title: 将来のライフ イベントのコンフィギュレーション
description: Dynamics 365 Human Resources 将来のライフ サイクルをスケジュールできます。
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d390bf2e9b25c50e913967ea51fcfadd4a1120b8
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464353"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="84aab-103">将来のライフ イベントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="84aab-103">Configure future life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="84aab-104">Dynamics 365 Human Resources 将来のライフ サイクルをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="84aab-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="84aab-105">**給付金管理** ワーク スペースの **設定** で、**将来のライフ イベント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84aab-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="84aab-106">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84aab-106">Select **New**.</span></span>

3. <span data-ttu-id="84aab-107">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="84aab-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="84aab-108">フィールド</span><span class="sxs-lookup"><span data-stu-id="84aab-108">Field</span></span> | <span data-ttu-id="84aab-109">説明</span><span class="sxs-lookup"><span data-stu-id="84aab-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="84aab-110">ライフ イベント日付</span><span class="sxs-lookup"><span data-stu-id="84aab-110">Life event date</span></span> | <span data-ttu-id="84aab-111">システムによって登録期間中に、この日付までのすべてのイベントが処理されます。</span><span class="sxs-lookup"><span data-stu-id="84aab-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="84aab-112">ライフ イベントのログが記録されます</span><span class="sxs-lookup"><span data-stu-id="84aab-112">Life event logged</span></span> | <span data-ttu-id="84aab-113">ライフ イベントが記録される日時。</span><span class="sxs-lookup"><span data-stu-id="84aab-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="84aab-114">ログ タイプ</span><span class="sxs-lookup"><span data-stu-id="84aab-114">Log type</span></span> | <span data-ttu-id="84aab-115">アクションが次のいずれかであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="84aab-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="84aab-116">- **更新** – ライフ イベントを追跡している既存のレコードへの変更</span><span class="sxs-lookup"><span data-stu-id="84aab-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="84aab-117">- **挿入** – 新しいライフ イベント レコードを作成</span><span class="sxs-lookup"><span data-stu-id="84aab-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="84aab-118">ライフ イベント タイプ ID</span><span class="sxs-lookup"><span data-stu-id="84aab-118">Life event type ID</span></span> | <span data-ttu-id="84aab-119">ライフ イベント タイプの固有識別子。</span><span class="sxs-lookup"><span data-stu-id="84aab-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="84aab-120">ライフ イベント タイプ</span><span class="sxs-lookup"><span data-stu-id="84aab-120">Life event type</span></span> | <span data-ttu-id="84aab-121">従業員の給付金登録を更新する触媒。</span><span class="sxs-lookup"><span data-stu-id="84aab-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="84aab-122">詳細については、ライフ イベント トリガーのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="84aab-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="84aab-123">ステータス</span><span class="sxs-lookup"><span data-stu-id="84aab-123">Status</span></span> | <span data-ttu-id="84aab-124">ライフ イベント処理されているかどうか。</span><span class="sxs-lookup"><span data-stu-id="84aab-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="84aab-125">ライン</span><span class="sxs-lookup"><span data-stu-id="84aab-125">Line</span></span> | <span data-ttu-id="84aab-126">将来のライフ イベントの行番号。</span><span class="sxs-lookup"><span data-stu-id="84aab-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="84aab-127">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84aab-127">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]