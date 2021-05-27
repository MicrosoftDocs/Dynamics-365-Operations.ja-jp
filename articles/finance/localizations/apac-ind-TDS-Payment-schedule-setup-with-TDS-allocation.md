---
title: TDS 配賦の支払スケジュールの設定
description: このトピックでは、源泉徴収 (TDS) の配賦を考慮した支払いスケジュールを設定する方法について説明します。
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023396"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="8a717-103">TDS 配賦の支払スケジュールの設定</span><span class="sxs-lookup"><span data-stu-id="8a717-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a717-104">このトピックでは、源泉徴収 (TDS) の配賦を考慮した支払いスケジュールを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8a717-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="8a717-105">**買掛金勘定 \> 支払の設定 \> 支払スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a717-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="8a717-106">[![支払スケジュール ページ](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="8a717-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="8a717-107">アクション ペインで、**新規** を選択して、支払いスケジュールを作成し、必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a717-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="8a717-108">**配賦** フィールドで、支払スケジュールの支払の配賦に使用する手段を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a717-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="8a717-109">小計</span><span class="sxs-lookup"><span data-stu-id="8a717-109">Total</span></span>
    - <span data-ttu-id="8a717-110">固定金額</span><span class="sxs-lookup"><span data-stu-id="8a717-110">Fixed amount</span></span>
    - <span data-ttu-id="8a717-111">固定数量</span><span class="sxs-lookup"><span data-stu-id="8a717-111">Fixed quantity</span></span>
    - <span data-ttu-id="8a717-112">指定</span><span class="sxs-lookup"><span data-stu-id="8a717-112">Specified</span></span>

    <span data-ttu-id="8a717-113">**源泉徴収税の配賦** フィールドには、支払スケジュールの TDS の配賦方法が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a717-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="8a717-114">**配賦** フィールドで **合計** を選択すると、**源泉徴収税の配賦** フィールドが自動的に **合計** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8a717-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="8a717-115">**配賦** フィールドで **固定金額**、**固定数量**、または **指定済** を選択した場合、**源泉徴収税の配賦** フィールドが自動的に **比例して** 設定されます。</span><span class="sxs-lookup"><span data-stu-id="8a717-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a717-116">**源泉徴収税の配賦** フィールドが **合計** に設定されている場合は、TDS 金額を含む総額に基づいて支払の配分が計算されます。</span><span class="sxs-lookup"><span data-stu-id="8a717-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="8a717-117">**源泉徴収税の配賦** フィールドが **比例** に設定されている場合は、分割払いは、TDS金額を差し引いた後の正味の請求書金額に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="8a717-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="8a717-118">その他の必要な詳細をフォームに入力し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a717-118">Enter the other required details, and then close the page.</span></span>
