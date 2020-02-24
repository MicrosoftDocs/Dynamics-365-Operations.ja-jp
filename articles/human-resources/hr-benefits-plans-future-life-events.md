---
title: 将来のライフ イベントのコンフィギュレーション
description: Dynamics 365 Human Resources 将来のライフ サイクルをスケジュールできます。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 655070e52e3d1f43ca6904ce3218582868f193fe
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009689"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="e853d-103">将来のライフ イベントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e853d-103">Configure future life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e853d-104">Dynamics 365 Human Resources 将来のライフ サイクルをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="e853d-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="e853d-105">**給付金管理**ワーク スペースの**設定**で、**将来のライフ イベント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e853d-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="e853d-106">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e853d-106">Select **New**.</span></span>

3. <span data-ttu-id="e853d-107">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e853d-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e853d-108">フィールド</span><span class="sxs-lookup"><span data-stu-id="e853d-108">Field</span></span> | <span data-ttu-id="e853d-109">説明</span><span class="sxs-lookup"><span data-stu-id="e853d-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e853d-110">ライフ イベント日付</span><span class="sxs-lookup"><span data-stu-id="e853d-110">Life event date</span></span> | <span data-ttu-id="e853d-111">システムによって登録期間中に、この日付までのすべてのイベントが処理されます。</span><span class="sxs-lookup"><span data-stu-id="e853d-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="e853d-112">ライフ イベントのログが記録されます</span><span class="sxs-lookup"><span data-stu-id="e853d-112">Life event logged</span></span> | <span data-ttu-id="e853d-113">ライフ イベントが記録される日時。</span><span class="sxs-lookup"><span data-stu-id="e853d-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="e853d-114">ログ タイプ</span><span class="sxs-lookup"><span data-stu-id="e853d-114">Log type</span></span> | <span data-ttu-id="e853d-115">アクションが次のいずれかであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e853d-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="e853d-116">- **更新** – ライフ イベントを追跡している既存のレコードへの変更</span><span class="sxs-lookup"><span data-stu-id="e853d-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="e853d-117">- **挿入** – 新しいライフ イベント レコードを作成</span><span class="sxs-lookup"><span data-stu-id="e853d-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="e853d-118">ライフ イベント タイプ ID</span><span class="sxs-lookup"><span data-stu-id="e853d-118">Life event type ID</span></span> | <span data-ttu-id="e853d-119">ライフ イベント タイプの固有識別子。</span><span class="sxs-lookup"><span data-stu-id="e853d-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="e853d-120">ライフ イベント タイプ</span><span class="sxs-lookup"><span data-stu-id="e853d-120">Life event type</span></span> | <span data-ttu-id="e853d-121">従業員の給付金登録を更新する触媒。</span><span class="sxs-lookup"><span data-stu-id="e853d-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="e853d-122">詳細については、ライフ イベント トリガーのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e853d-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="e853d-123">ステータス</span><span class="sxs-lookup"><span data-stu-id="e853d-123">Status</span></span> | <span data-ttu-id="e853d-124">ライフ イベント処理されているかどうか。</span><span class="sxs-lookup"><span data-stu-id="e853d-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="e853d-125">ライン</span><span class="sxs-lookup"><span data-stu-id="e853d-125">Line</span></span> | <span data-ttu-id="e853d-126">将来のライフ イベントの行番号。</span><span class="sxs-lookup"><span data-stu-id="e853d-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="e853d-127">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e853d-127">Select **Save**.</span></span> 
