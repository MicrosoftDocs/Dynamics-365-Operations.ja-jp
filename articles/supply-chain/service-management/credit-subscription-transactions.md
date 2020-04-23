---
title: 定期売買トランザクションの貸方記入
description: このトピックでは、定期売買手数料トランザクションの貸方への記入方法について説明します。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a136489b663a066b853344844ad28a14670c8d66
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202517"
---
# <a name="credit-subscription-transactions"></a><span data-ttu-id="98092-103">定期売買トランザクションの貸方記入</span><span class="sxs-lookup"><span data-stu-id="98092-103">Credit subscription transactions</span></span> 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a><span data-ttu-id="98092-104">定期売買トランザクションの貸方記入</span><span class="sxs-lookup"><span data-stu-id="98092-104">Credit subscription transactions</span></span>

1.  <span data-ttu-id="98092-105">**サービス管理** \> **共通** \> **サービスの定期売買** \> **すべてのサービス定期売買**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="98092-105">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span>

2.  <span data-ttu-id="98092-106">貸方票を作成する定期売買トランザクションに関連付けられている定期売買を選択します。</span><span class="sxs-lookup"><span data-stu-id="98092-106">Select the subscription attached to the subscription transaction for which you want to create a credit note.</span></span>

3.  <span data-ttu-id="98092-107">**分析**タブを選択し、アクション ウィンドウで**手数料トランザクション**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98092-107">Select the **Analyze** tab, and then click the **Fee transactions** button on the Action Pane.</span></span>

4.  <span data-ttu-id="98092-108">**手数料トランザクション**フォームから、訂正票を作成するトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="98092-108">From the **Fee transactions** form, select the transaction for which you want to create a credit note.</span></span>

5.  <span data-ttu-id="98092-109">**機能** \> **貸方票の選択**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="98092-109">Click **Functions** \> **Select for credit note**.</span></span>

6.  <span data-ttu-id="98092-110">**貸方票の選択**フォームで、貸方転記するトランザクションを選択し、**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98092-110">From the **Select for credit note** form, select the transaction that you want to credit and then click **OK**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="98092-111">貸方票を作成する場合は、必ず<STRONG>貸方票</STRONG>を選択してください。</span><span class="sxs-lookup"><span data-stu-id="98092-111">When you create the credit note, make sure that you select <STRONG>Credit notes</STRONG>.</span></span> <span data-ttu-id="98092-112">これは、<STRONG>請求書の作成</STRONG>ダイアログ ボックスの<STRONG>請求方法</STRONG>リストにあります。</span><span class="sxs-lookup"><span data-stu-id="98092-112">This is found in the <STRONG>Invoicing method</STRONG> list in the <STRONG>Create invoice</STRONG> dialog box.</span></span></P>

<span data-ttu-id="98092-113">**サービス管理パラメーター**フォームの**見越計上を貸方にリバース仕訳**フィールドが**手動**に設定されている場合は、トランザクションの貸方票提案を作成する前に、各未収収益トランザクションを個別に取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="98092-113">If the **Reverse accruals on crediting** field in the **Service management parameters** form is set to **Manual**, you have to reverse each accrued revenue transaction individually before you create a credit note proposal for the transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="98092-114">参照</span><span class="sxs-lookup"><span data-stu-id="98092-114">See also</span></span>

[<span data-ttu-id="98092-115">定期売買トランザクションの請求</span><span class="sxs-lookup"><span data-stu-id="98092-115">Invoice subscription transactions</span></span>](invoice-subscription-transactions.md)


 
