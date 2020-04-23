---
title: 品目予測の計算
description: このトピックでは、資産管理で品目予測を計算する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20f969b68e4e9a9936f377000191ba9db202447f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216462"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="f5bde-103">品目予測の計算</span><span class="sxs-lookup"><span data-stu-id="f5bde-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f5bde-104">前のセクションで説明されている最大能力負荷計算を行うことができるのと同様に、以下で品目予測を計算することもできます。</span><span class="sxs-lookup"><span data-stu-id="f5bde-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="f5bde-105">メンテナンス スケジュール明細行</span><span class="sxs-lookup"><span data-stu-id="f5bde-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="f5bde-106">まだスケジュールされていない作業指示書</span><span class="sxs-lookup"><span data-stu-id="f5bde-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="f5bde-107">スケジュール済作業指示書</span><span class="sxs-lookup"><span data-stu-id="f5bde-107">scheduled work orders</span></span>

<span data-ttu-id="f5bde-108">これは、特定の期間において、予想される品目消費 (予備部品および作業指示書を完了するのに必要なその他の品目) の概要を取得する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f5bde-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="f5bde-109">品目予測の計算は、すべての資産または選択した資産に対して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f5bde-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="f5bde-110">また、メンテナンス ダウンタイム活動 (**すべてのメンテナンス ダウンタイム活動**または**有効なメンテナンス ダウンタイム活動**) で、または作業指示書プール (**すべての作業指示書プール**または**有効な作業指示書プール**) で計算を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="f5bde-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="f5bde-111">**資産管理** > **照会** > **品目予測**の順に、または**資産管理** > **共通** > **作業指示書プール** > **すべての作業指示書プール** / **有効な作業指示書プール** > リスト内で作業指示書プールの選択 > **品目予測**ボタンの順に、または**資産管理** > **共通** > **メンテナンス ダウンタイム活動** > **すべてのメンテナンス ダウンタイム活動** / **有効なメンテナンス ダウンタイム活動** > リスト内でメンテナンス ダウンタイム活動を選択 > **品目予測**ボタンの順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5bde-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="f5bde-112">**品目予測の計算**ダイアログで、**開始日/時刻**および**終了日/時刻**フィールドの計算に対する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5bde-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="f5bde-113">予測計算にメンテナンス スケジュール明細行を含める場合は、**メンテナンス スケジュールを含める**トグル ボタンで "はい" を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5bde-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="f5bde-114">予測計算に作業指示書ジョブを含める場合は、**作業指示書を含める**トグル ボタンで "はい" を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5bde-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="f5bde-115">**レベル** フィールドを使用すると、機能的な場所に関する品目予測行の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f5bde-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="f5bde-116">たとえば、フィールドに数値 "1" を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべてのメンテナンス スケジュール明細行および作業指示書が最上位レベルに表示されます。したがって明細行の時間は、下位レベルにある機能的な場所から追加される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f5bde-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="f5bde-117">**レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルですべてメンテナンス スケジュール行および作業指示書を示す、詳細な結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f5bde-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="f5bde-118">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="f5bde-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="f5bde-119">**グループ化**グループで、関連するボタンをクリックすると、計算の必要な詳細レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f5bde-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="f5bde-120">下のスクリーンショットでは、選択した**グループ化**ボタンが青色で強調表示されています。</span><span class="sxs-lookup"><span data-stu-id="f5bde-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="f5bde-121">ボタンをクリックして、有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="f5bde-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="f5bde-122">品目に製品、保管、または追跡用分析コードを表示する場合は、**分析コードの表示**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5bde-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="f5bde-123">該当するチェック ボックスを選択して、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5bde-123">Select the relevant check boxes, and click **OK**.</span></span>

![図 1](media/02-capacity-planning.png)
