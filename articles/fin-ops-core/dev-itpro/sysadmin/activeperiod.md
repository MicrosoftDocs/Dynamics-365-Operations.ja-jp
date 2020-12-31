---
title: 有効なバッチ期間
description: このトピックでは、有効なバッチ期間のセットアップおよび作業に関する情報を説明します。
author: hasaid
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 21
ms.openlocfilehash: c75e026cf39b83bc3f93b533f2c884728ea9cb5c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688189"
---
# <a name="active-batch-periods"></a><span data-ttu-id="d8215-103">有効なバッチ期間</span><span class="sxs-lookup"><span data-stu-id="d8215-103">Active batch periods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8215-104">プラットフォーム更新 21 のリリースでは、バッチ ジョブがいつ実行されるかの制御の追加レベルが使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d8215-104">With the release of Platform update 21, an additional level of control over when batch jobs execute is now available.</span></span> <span data-ttu-id="d8215-105">以前は、一定の時間数または特定の日付までの 1 時間ごとにバッチ ジョブが実行されるようにスケジュールすることのみ可能でした。</span><span class="sxs-lookup"><span data-stu-id="d8215-105">Previously, it was only possible to schedule a batch job to execute every hour for a specified number of hours or until a given date.</span></span> <span data-ttu-id="d8215-106">管理者は、次のシナリオなど、追加のアクティブ期間の情報を指定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d8215-106">Administrators can now provide information for an additional active period, such as in the following scenarios:</span></span>
- <span data-ttu-id="d8215-107">バッチ グループ内のジョブが実行を開始できる期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8215-107">Specifying time ranges during which jobs within a batch group can start execution.</span></span> 
- <span data-ttu-id="d8215-108">営業時間外にのみバッチ ジョブを実行する場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="d8215-108">Selecting to run batch jobs outside of office hours only.</span></span> 
- <span data-ttu-id="d8215-109">アクティブ期間内で任意の回数の繰り返しを設定します。</span><span class="sxs-lookup"><span data-stu-id="d8215-109">Setting the recurrence for anytime within the active period.</span></span> <span data-ttu-id="d8215-110">たとえば、管理者は、午後 6 時から午前 8 時の間のみ、毎時間バッチ ジョブを実行することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d8215-110">For example, you administrator might select to run the batch jobs every hour, but only between the hours of 6:00 PM and 8:00 AM.</span></span>

> [!NOTE] 
> <span data-ttu-id="d8215-111">この機能は、Platform update 21 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="d8215-111">This feature is available as of Platform update 21.</span></span>

## <a name="set-up-active-periods-for-batch-jobs"></a><span data-ttu-id="d8215-112">バッチ ジョブの有効期間の設定</span><span class="sxs-lookup"><span data-stu-id="d8215-112">Set up active periods for batch jobs</span></span> 

1.  <span data-ttu-id="d8215-113">**システム管理** > **設定** > **バッチ ジョブの有効期間** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8215-113">Go to **System administration** > **Setup** > **Active periods for batch jobs**.</span></span>
2.  <span data-ttu-id="d8215-114">バッチ ジョブの名前を入力し、バッチ ジョブが有効な開始日と終了日を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8215-114">Enter the name of the batch job, and specify start and end dates that the batch job is active.</span></span> 
4.  <span data-ttu-id="d8215-115">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8215-115">Click **Save**.</span></span>

![有効期間フォーム](./media/active-periods.png)

## <a name="assign-active-periods-to-batch-jobs"></a><span data-ttu-id="d8215-117">バッチ ジョブの有効期間の割り当て</span><span class="sxs-lookup"><span data-stu-id="d8215-117">Assign active periods to batch jobs</span></span>

1.  <span data-ttu-id="d8215-118">**システム管理** > **照会** > **バッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8215-118">Go to **System administration** > **Inquiries** > **Batch jobs**.</span></span>
2.  <span data-ttu-id="d8215-119">期間を割り当てるバッチ ジョブを選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8215-119">Select the batch job that you want to assign a period to, and click **Edit**.</span></span>
3.  <span data-ttu-id="d8215-120">**有効期間** フィールドで、割り当てる有効期間を選択し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d8215-120">In the **Active period** field, select the active period that you want to assign, and then click **Save**.</span></span>

![有効期間の割り当て](./media/assign-active-period.png)
 
