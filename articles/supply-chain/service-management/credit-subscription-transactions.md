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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4238c625930767990d28a206b10a4d71841f2ad8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247505"
---
# <a name="credit-subscription-transactions"></a><span data-ttu-id="b3aea-103">定期売買トランザクションの貸方記入</span><span class="sxs-lookup"><span data-stu-id="b3aea-103">Credit subscription transactions</span></span> 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a><span data-ttu-id="b3aea-104">定期売買トランザクションの貸方記入</span><span class="sxs-lookup"><span data-stu-id="b3aea-104">Credit subscription transactions</span></span>

1.  <span data-ttu-id="b3aea-105">**サービス管理** \> **共通** \> **サービスの定期売買** \> **すべてのサービス定期売買** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3aea-105">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span>

2.  <span data-ttu-id="b3aea-106">貸方票を作成する定期売買トランザクションに関連付けられている定期売買を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3aea-106">Select the subscription attached to the subscription transaction for which you want to create a credit note.</span></span>

3.  <span data-ttu-id="b3aea-107">**分析** タブを選択し、アクション ウィンドウで **手数料トランザクション** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3aea-107">Select the **Analyze** tab, and then click the **Fee transactions** button on the Action Pane.</span></span>

4.  <span data-ttu-id="b3aea-108">**手数料トランザクション** フォームから、訂正票を作成するトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3aea-108">From the **Fee transactions** form, select the transaction for which you want to create a credit note.</span></span>

5.  <span data-ttu-id="b3aea-109">**機能** \> **貸方票の選択** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3aea-109">Click **Functions** \> **Select for credit note**.</span></span>

6.  <span data-ttu-id="b3aea-110">**貸方票の選択** フォームで、貸方転記するトランザクションを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3aea-110">From the **Select for credit note** form, select the transaction that you want to credit and then click **OK**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b3aea-111">貸方票を作成する場合は、必ず<STRONG>貸方票</STRONG>を選択してください。</span><span class="sxs-lookup"><span data-stu-id="b3aea-111">When you create the credit note, make sure that you select <STRONG>Credit notes</STRONG>.</span></span> <span data-ttu-id="b3aea-112">これは、<STRONG>請求書の作成</STRONG>ダイアログ ボックスの<STRONG>請求方法</STRONG>リストにあります。</span><span class="sxs-lookup"><span data-stu-id="b3aea-112">This is found in the <STRONG>Invoicing method</STRONG> list in the <STRONG>Create invoice</STRONG> dialog box.</span></span></P>

<span data-ttu-id="b3aea-113">**サービス管理パラメーター** フォームの **見越計上を貸方にリバース仕訳** フィールドが **手動** に設定されている場合は、トランザクションの貸方票提案を作成する前に、各未収収益トランザクションを個別に取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3aea-113">If the **Reverse accruals on crediting** field in the **Service management parameters** form is set to **Manual**, you have to reverse each accrued revenue transaction individually before you create a credit note proposal for the transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3aea-114">参照</span><span class="sxs-lookup"><span data-stu-id="b3aea-114">See also</span></span>

[<span data-ttu-id="b3aea-115">定期売買トランザクションの請求</span><span class="sxs-lookup"><span data-stu-id="b3aea-115">Invoice subscription transactions</span></span>](invoice-subscription-transactions.md)


 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]