---
title: 計画最適化の自動確定
description: このトピックでは、計画の最適化による自動確定の使用方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 61e9e6aa660bc0828645c6bf1f2655539804831a
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594529"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="865b8-103">計画最適化の自動確定</span><span class="sxs-lookup"><span data-stu-id="865b8-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="865b8-104">自動確定を使用して、マスター プラン プロセスの一部として計画オーダーを確定 (つまり、リリース) できます。</span><span class="sxs-lookup"><span data-stu-id="865b8-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="865b8-105">計画オーダーが確定されると、実際の発注書、移動オーダー、または製造オーダーに変換されます。</span><span class="sxs-lookup"><span data-stu-id="865b8-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="865b8-106">計画の最適化を使用すると、注文日 (つまり、開始日) が確定のタイム フェンス内にある場合、マスター プランの実行時に計画オーダーが確定されます。</span><span class="sxs-lookup"><span data-stu-id="865b8-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="865b8-107">計画発注書の自動確定は、品目が仕入先に関連付けられている場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="865b8-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="865b8-108">自動確定を有効にする</span><span class="sxs-lookup"><span data-stu-id="865b8-108">Turn on autofirming</span></span>

<span data-ttu-id="865b8-109">自動確定を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="865b8-109">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="865b8-110">**機能管理** ワークスペースの **新規** タブで、一覧から **計画の最適化の自動確定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="865b8-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="865b8-111">この機能が **新しい** タブに表示されない場合は、**無効** タブおよび **すべての** タブを確認します。</span><span class="sxs-lookup"><span data-stu-id="865b8-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="865b8-112">**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="865b8-112">Select **Enable now**.</span></span> <span data-ttu-id="865b8-113">または、**スケジュール** を選択し、機能を有効にする時間を選択します。</span><span class="sxs-lookup"><span data-stu-id="865b8-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="865b8-114">確定タイム フェンスを設定する</span><span class="sxs-lookup"><span data-stu-id="865b8-114">Set up the firming time fence</span></span>

<span data-ttu-id="865b8-115">確定タイム フェンスは、マスター プランの実行日から未来に向かって計算されます。</span><span class="sxs-lookup"><span data-stu-id="865b8-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="865b8-116">入力する日数によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="865b8-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="865b8-117">次の方法で、確定タイム フェンスを制御できます。</span><span class="sxs-lookup"><span data-stu-id="865b8-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="865b8-118">補充グループの既定の確定タイム フェンスを定義するには、**マスター プラン** \> **設定** \> **補充** \> **補充グループ** の順に移動し、補充グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="865b8-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="865b8-119">次に、**その他** クイック タブの **自動確定タイム フェンス (日)** フィールドに、日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="865b8-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="865b8-120">特定の品目の補充グループに対して定義される確定タイム フェンスを上書きするには、**製品情報管理** \> **リリース済製品** に移動し、アクション ウィンドウから **計画** を選択し、続いて **品目補充** を選択します。</span><span class="sxs-lookup"><span data-stu-id="865b8-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="865b8-121">次に **一般** タブで、**タイム フェンスの上書き** を選択し、**自動確定タイム フェンス (日)** に日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="865b8-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="865b8-122">特定のマスター プランの補充グループおよび品目補充に対して定義される確定タイム フェンスを上書きするには、**マスター プラン** \> **設定** \> **マスター プラン** の順に移動し、マスター プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="865b8-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="865b8-123">次に、**タイム フェンス (日数)** クイック タブで、**確定** を **はい** に設定して、日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="865b8-123">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="865b8-124">計画の最適化を使用するマスター プランの実行に対して自動確定が有効になっている場合、自動確定処理は自動確定の設定に応じて実行されます。</span><span class="sxs-lookup"><span data-stu-id="865b8-124">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="865b8-125">自動確定が有効になっていない場合、または **正味必要量** ページから計画を開始している場合は、自動確定プロセスはスキップされます。</span><span class="sxs-lookup"><span data-stu-id="865b8-125">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="865b8-126">計画の最適化と組み込み Supply Chain Management 計画エンジンの対比</span><span class="sxs-lookup"><span data-stu-id="865b8-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="865b8-127">Microsoft Dynamics 365 Supply Chain Management に組み込まれる計画の最適化および計画エンジンの両方は、計画オーダーを自動確定できます。</span><span class="sxs-lookup"><span data-stu-id="865b8-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="865b8-128">ただし、重要な違いがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="865b8-128">However, there are some important differences.</span></span> <span data-ttu-id="865b8-129">たとえば、計画の最適化は注文日 (つまり、開始日) を使用して確定する計画オーダーを決定しますが、組み込み Supply Chain Management 計画エンジンは、要求期日 (つまり、終了日) を使用します。</span><span class="sxs-lookup"><span data-stu-id="865b8-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="865b8-130">次に差異の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="865b8-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="865b8-131">**計画の最適化**</span><span class="sxs-lookup"><span data-stu-id="865b8-131">**Planning Optimization**</span></span>

- <span data-ttu-id="865b8-132">自動確定は注文日 (開始日) に基づきます。</span><span class="sxs-lookup"><span data-stu-id="865b8-132">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="865b8-133">注文日 (開始日) によって確定がトリガーされるため、確定タイム フェンスの一部としてリード タイムを考慮する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="865b8-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="865b8-134">現在の週に開始する必要があるすべての注文を確定する場合、確定タイム フェンスを 1 週間にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="865b8-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="865b8-135">**組み込み Supply Chain Management 計画エンジン**</span><span class="sxs-lookup"><span data-stu-id="865b8-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="865b8-136">自動確定は要求期日 (終了日) に基づきます。</span><span class="sxs-lookup"><span data-stu-id="865b8-136">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="865b8-137">注文が期限内に確定されるようにするには、確定タイム フェンスはリード タイムよりも長くする必要があります。</span><span class="sxs-lookup"><span data-stu-id="865b8-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="865b8-138">現在の週に開始する必要があるすべての注文を確定する場合、確定タイム フェンスはリードタイム + 1 週間にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="865b8-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
