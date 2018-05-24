---
title: "サービス注文のキャンセル"
description: "サービス注文自体からサービス注文またはサービス注文明細行をキャンセルしたり、定期処理ジョブを実行して複数のサービス注文をキャンセルしたりできます。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.openlocfilehash: 8e5ad119c28bba18b75bb5ed7854e94a4e734d55
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="07612-103">サービス注文のキャンセル</span><span class="sxs-lookup"><span data-stu-id="07612-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="07612-104">サービス注文自体からサービス注文またはサービス注文明細行をキャンセルしたり、定期処理ジョブを実行して複数のサービス注文をキャンセルしたりできます。</span><span class="sxs-lookup"><span data-stu-id="07612-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="07612-105">サービス注文のステージでキャンセルが許可されない場合、サービス注文に在庫品目要求がある場合、またはサービス注文が既に転記されている場合は、サービス注文をキャンセルできません。</span><span class="sxs-lookup"><span data-stu-id="07612-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="07612-106">"サービス注文" フォームでのサービス注文のキャンセル</span><span class="sxs-lookup"><span data-stu-id="07612-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="07612-107">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="07612-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="07612-108">サービス注文を選択し、アクション ウィンドウで、**注文のキャンセル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07612-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="07612-109">サービス注文明細行のキャンセル</span><span class="sxs-lookup"><span data-stu-id="07612-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="07612-110">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="07612-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="07612-111">キャンセルする明細行が含まれているサービス注文をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="07612-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="07612-112">キャンセルするサービス注文明細行を選択し、**注文明細行のキャンセル**をクリックして明細行のステータスを**キャンセル済**に変更します。</span><span class="sxs-lookup"><span data-stu-id="07612-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="07612-113">サービス注文明細行のキャンセルを取り消し、ステータスを<STRONG>作成済</STRONG>に戻すには、<STRONG>キャンセルの無効化</STRONG>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07612-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="07612-114">複数のサービス注文のキャンセル</span><span class="sxs-lookup"><span data-stu-id="07612-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="07612-115">**サービス管理** \> **定期処理** \> **サービス注文** \> **サービス注文のキャンセル**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="07612-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="07612-116">**選択** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="07612-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="07612-117">**照会** フォームの、**基準**列で、キャンセルするサービス注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="07612-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="07612-118">**OK**をクリックして**照会**フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="07612-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="07612-119">キャンセルされたサービス注文を一覧表示する情報ログを生成するには、**情報ログの表示**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="07612-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="07612-120">サービス注文の**キャンセル済**ステータスを元に戻すには、**キャンセルの無効化**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="07612-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="07612-121">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07612-121">Click **OK**.</span></span>

<span data-ttu-id="07612-122">選択したサービス注文がキャンセルされるか、その**キャンセル済**進捗状況ステータスが**処理中**に戻ります。</span><span class="sxs-lookup"><span data-stu-id="07612-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="07612-123"><STRONG>キャンセルの無効化</STRONG>チェック ボックスをオンにすると、進捗状況ステータスが<STRONG>キャンセル済</STRONG> のサービス注文が取り消されて、進捗状況ステータスが<STRONG>処理中</STRONG>のサービス注文のキャンセルは実行されません。</span><span class="sxs-lookup"><span data-stu-id="07612-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  



