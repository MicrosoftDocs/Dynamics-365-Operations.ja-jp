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
ms.openlocfilehash: f10d7b6c9b45f6cedc16972fb157e43b7e0c40b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113301"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="ac1f1-103">将来のライフ イベントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ac1f1-103">Configure future life events</span></span>

<span data-ttu-id="ac1f1-104">Dynamics 365 Human Resources 将来のライフ サイクルをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="ac1f1-105">**給付金管理** ワーク スペースの **設定** で、**将来のライフ イベント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="ac1f1-106">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-106">Select **New**.</span></span>

3. <span data-ttu-id="ac1f1-107">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ac1f1-108">フィールド</span><span class="sxs-lookup"><span data-stu-id="ac1f1-108">Field</span></span> | <span data-ttu-id="ac1f1-109">説明</span><span class="sxs-lookup"><span data-stu-id="ac1f1-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ac1f1-110">ライフ イベント日付</span><span class="sxs-lookup"><span data-stu-id="ac1f1-110">Life event date</span></span> | <span data-ttu-id="ac1f1-111">システムによって登録期間中に、この日付までのすべてのイベントが処理されます。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="ac1f1-112">ライフ イベントのログが記録されます</span><span class="sxs-lookup"><span data-stu-id="ac1f1-112">Life event logged</span></span> | <span data-ttu-id="ac1f1-113">ライフ イベントが記録される日時。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="ac1f1-114">ログ タイプ</span><span class="sxs-lookup"><span data-stu-id="ac1f1-114">Log type</span></span> | <span data-ttu-id="ac1f1-115">アクションが次のいずれかであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="ac1f1-116">- **更新** – ライフ イベントを追跡している既存のレコードへの変更</span><span class="sxs-lookup"><span data-stu-id="ac1f1-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="ac1f1-117">- **挿入** – 新しいライフ イベント レコードを作成</span><span class="sxs-lookup"><span data-stu-id="ac1f1-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="ac1f1-118">ライフ イベント タイプ ID</span><span class="sxs-lookup"><span data-stu-id="ac1f1-118">Life event type ID</span></span> | <span data-ttu-id="ac1f1-119">ライフ イベント タイプの固有識別子。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="ac1f1-120">ライフ イベント タイプ</span><span class="sxs-lookup"><span data-stu-id="ac1f1-120">Life event type</span></span> | <span data-ttu-id="ac1f1-121">従業員の給付金登録を更新する触媒。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="ac1f1-122">詳細については、ライフ イベント トリガーのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="ac1f1-123">ステータス</span><span class="sxs-lookup"><span data-stu-id="ac1f1-123">Status</span></span> | <span data-ttu-id="ac1f1-124">ライフ イベント処理されているかどうか。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="ac1f1-125">ライン</span><span class="sxs-lookup"><span data-stu-id="ac1f1-125">Line</span></span> | <span data-ttu-id="ac1f1-126">将来のライフ イベントの行番号。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="ac1f1-127">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac1f1-127">Select **Save**.</span></span> 
