---
title: 最大能力負荷の計算
description: このトピックでは、資産管理で最大能力負荷を計算する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c6d15861492a46ddb1222db2210f8c751ed38cb3
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886796"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="4da15-103">最大能力負荷の計算</span><span class="sxs-lookup"><span data-stu-id="4da15-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4da15-104">資産管理では、以下で最大能力負荷を計算できます</span><span class="sxs-lookup"><span data-stu-id="4da15-104">In Asset Management, you can calculate capacity load on</span></span>

- <span data-ttu-id="4da15-105">メンテナンス スケジュール明細行</span><span class="sxs-lookup"><span data-stu-id="4da15-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="4da15-106">まだスケジュールされていない作業指示書</span><span class="sxs-lookup"><span data-stu-id="4da15-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="4da15-107">スケジュール済作業指示書</span><span class="sxs-lookup"><span data-stu-id="4da15-107">scheduled work orders</span></span>

<span data-ttu-id="4da15-108">これは、特定の期間における予想される最大能力負荷の概要を取得する場合に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="4da15-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="4da15-109">最大能力負荷の計算は、すべての資産または選択した資産に対して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4da15-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="4da15-110">また、メンテナンス ダウンタイム活動や作業指示書プールで計算を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="4da15-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="4da15-111">**資産管理** > **照会** > **最大能力負荷**の順に、または**資産管理** > **共通** > **作業指示書プール** > **すべての作業指示書プール** / **有効な作業指示書プール** > リスト内で作業指示書プールの選択 > **最大負荷能力**ボタンの順に、または**資産管理** > **共通** > **メンテナンス ダウンタイム活動** > **すべてのメンテナンス ダウンタイム活動** / **有効なメンテナンス ダウンタイム活動** > リスト内でメンテナンス活動を選択 > **最大能力負荷**ボタンの順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4da15-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="4da15-112">**最大能力負荷の計算**ダイアログで、**開始日/時刻**および**終了日/時刻**フィールドの計算に対する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="4da15-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="4da15-113">計算にメンテナンス スケジュール行を含める場合は、**メンテナンス スケジュールを含める**トグル ボタンで "はい" を選択します。</span><span class="sxs-lookup"><span data-stu-id="4da15-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="4da15-114">計算に作業指示書ジョブを含める場合は、**作業指示書を含める**トグル ボタンで "はい" を選択します。</span><span class="sxs-lookup"><span data-stu-id="4da15-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="4da15-115">**レベル** フィールドを使用すると、機能的な場所に関する最大能力負荷行の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4da15-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> <span data-ttu-id="4da15-116">たとえば、フィールドに数値 "1" を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべてのメンテナンス スケジュール明細行および作業指示書が最上位レベルに表示されます。したがって明細行の時間は、下位レベルにある機能的な場所から追加される場合があります。</span><span class="sxs-lookup"><span data-stu-id="4da15-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="4da15-117">**レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルですべてメンテナンス スケジュール行および作業指示書を示す、詳細な結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4da15-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="4da15-118">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="4da15-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="4da15-119">**グループ化**アクション ウィンドウ グループで、関連するボタンをクリックすると、計算の必要な詳細レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4da15-119">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="4da15-120">選択したアクション ウィンドウ グループ ボタンが青色で強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="4da15-120">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="4da15-121">ボタンをクリックして、有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="4da15-121">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="4da15-122">次の図は、インターフェイスの例を示します。</span><span class="sxs-lookup"><span data-stu-id="4da15-122">The figure below shows an example of the interface.</span></span>

![図 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="4da15-124">スケジュール済み作業指示書に関する能力計画にのみ焦点を合わせる場合は、[スケジュール済み作業指示書の最大能力負荷の計算](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4da15-124">If you want to focus only on capacity planning regarding scheduled work orders, refer to [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

