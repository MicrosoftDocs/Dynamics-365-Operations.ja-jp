---
title: TDS 税タイプに対する源泉徴収税精算期間の設定
description: このトピックでは、源泉徴収税 (TDS) 決済期間の決済帰還を設定する方法について説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023375"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="b31b0-103">TDS 税タイプに対する源泉徴収税精算期間の設定</span><span class="sxs-lookup"><span data-stu-id="b31b0-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b31b0-104">このトピックでは、源泉徴収税 (TDS) 決済期間の決済帰還を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="b31b0-105">**税 \> 間接税 \> 源泉徴収税 \> 源泉徴収税決済期間** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="b31b0-106">[![源泉徴収税の決済期間ページ](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="b31b0-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="b31b0-107">**税タイプ** フィールドで、**TDS** を選択して、TDS 税タイプの源泉徴収税決済期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="b31b0-108">**新規** を選択して、明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="b31b0-109">**決済期間** フィールドに、TDS 決済期間の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="b31b0-110">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="b31b0-111">**源泉徴収税オーソリティ** フィールドで、TDS 決済期間を定義する TDS オーソリティを選択します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="b31b0-112">**一般** クイック タブの **期間間隔** フィールドで、TDS 決済期間の期間間隔のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="b31b0-113">**単位数** フィールドで、期間間隔タイプの単位数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="b31b0-114">**期間** クイック タブの **開始日** フィールドで、TDS 決済期間の開始日を選択します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="b31b0-115">**終了日** フィールドで、終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="b31b0-116">既存の期間、期間間隔および期間単位に基づいてその後のTDS決済期間を作成するには、**新しい期間** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="b31b0-117">特定の決済期間に対して実行される定期 TDS 決済の詳細を表示するには、**源泉徴収税の支払** を選択して **源泉徴収税の支払** ページ を開きます。</span><span class="sxs-lookup"><span data-stu-id="b31b0-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b31b0-118">定期的な TDS 決済プロセスを実行するには、**一般会計 \> 定期 \> 源泉徴収税 \> 源泉徴収税の支払** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b31b0-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="b31b0-119">[![源泉徴収税支払のページ](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="b31b0-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="b31b0-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b31b0-120">Close the page.</span></span>
