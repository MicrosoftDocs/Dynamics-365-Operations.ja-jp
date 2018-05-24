---
title: "定期売買手数料の日数の引き下げ"
description: "既存の定期売買手数料の日数の下方修正は、定期売買手数料期間にもはや含まれない期間を除外した、新しいトランザクションを作成して行えます。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c70e393c125eecef85e8711d1635250f5ff408d9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---


# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="c2799-103">定期売買手数料の日数の引き下げ</span><span class="sxs-lookup"><span data-stu-id="c2799-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c2799-104">既存の定期売買手数料の日数の下方修正は、定期売買手数料期間にもはや含まれない期間を除外した、新しいトランザクションを作成して行えます。</span><span class="sxs-lookup"><span data-stu-id="c2799-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="c2799-105">定期売買手数料の日数の下方修正</span><span class="sxs-lookup"><span data-stu-id="c2799-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="c2799-106">**サービス管理** \> **共通** \> **サービスの定期売買** \> **すべてのサービス定期売買**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2799-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="c2799-107">サービスの定期売買を選択し、アクション ウィンドウで、**定期売買手数料**をクリックします</span><span class="sxs-lookup"><span data-stu-id="c2799-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="c2799-108">**定期売買タイプ**フィールドで、**下方修正日数**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2799-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="c2799-109">**開始日**フィールドおよび**終了日**フィールドを使用して、定期売買手数料期間から除外する定期売買手数料の日付範囲を定義し、 **OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2799-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="c2799-110">作成したトランザクションを表示するには、**定期売買**フォームで、**手数料トランザクション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2799-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="c2799-111">例</span><span class="sxs-lookup"><span data-stu-id="c2799-111">Example</span></span>

<span data-ttu-id="c2799-112">1 月 1 日から 1 月 31 日までの定期売買トランザクションの期間を 10 日間だけ下方修正する場合は、1 月 1 日から 1 月 10 日までを下方修正期間とする新しいトランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="c2799-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="c2799-113">(下方修正期間は、1 月 5 日から 1 月 15 日までなど、別の 10 日を指定することもできます)。</span><span class="sxs-lookup"><span data-stu-id="c2799-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="c2799-114">また、下方修正期間の**開始日**が 1 月 21 日 (31 - 10) である場合は、**終了日**を 1 月 31 日以降の任意の日付に設定できます。この場合も、手数料トランザクション期間が 10 日間下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="c2799-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2799-115">参照</span><span class="sxs-lookup"><span data-stu-id="c2799-115">See also</span></span>

[<span data-ttu-id="c2799-116">下方修正日数の例</span><span class="sxs-lookup"><span data-stu-id="c2799-116">Reduction days example</span></span>](reduction-days-example.md)

  



