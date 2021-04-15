---
title: サービス注文品目の要件
description: サービス注文に特定の品目を引き当てる必要がある場合、その在庫品目要求を作成できます。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bbd15ca83ab116286a3d681887f076896653c76
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810585"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="fd88c-103">サービス注文品目の要件</span><span class="sxs-lookup"><span data-stu-id="fd88c-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fd88c-104">顧客に提供するサービスを追跡および管理するサービス注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="fd88c-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="fd88c-105">サービス注文に特定の品目を引き当てる必要がある場合、その在庫品目要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="fd88c-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="fd88c-106">品目要求を在庫からすぐ消費したり、その品目の製造オーダーを開始できます。</span><span class="sxs-lookup"><span data-stu-id="fd88c-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="fd88c-107">品目トランザクションではなく在庫品目要求を使用することによって、品目が実際に使用される直前の配送を計画したり、発注書を作成したり、品目を売買契約の枠組みに含めたり、在庫品目要求を生産計画に含めたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="fd88c-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="fd88c-108">サービス注文に関する要求はプロジェクトを通じて処理します。</span><span class="sxs-lookup"><span data-stu-id="fd88c-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="fd88c-109">サービス注文に対して在庫品目要求を作成するには、サービス注文をプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd88c-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="fd88c-110">サービス注文に対して作成された在庫品目要求は、個々のサービス注文の **プロジェクト** から、または **販売注文** フォームを使用して表示できます。</span><span class="sxs-lookup"><span data-stu-id="fd88c-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="fd88c-111">サービス注文からの在庫品目要求の表示</span><span class="sxs-lookup"><span data-stu-id="fd88c-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="fd88c-112">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd88c-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="fd88c-113">**派遣** をクリックし、**在庫品目要求** をクリックして **在庫品目要求** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd88c-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="fd88c-114">**プロジェクト** タブをクリックし、**サービス注文** フィールドで在庫品目要求のサービス注文を確認します。</span><span class="sxs-lookup"><span data-stu-id="fd88c-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="fd88c-115">在庫品目要求を含むサービス注文の削除</span><span class="sxs-lookup"><span data-stu-id="fd88c-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="fd88c-116">サービス注文に対して在庫品目要求が作成されている場合は、サービス注文を削除できません。</span><span class="sxs-lookup"><span data-stu-id="fd88c-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="fd88c-117">サービス注文を削除する前に、在庫品目要求を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd88c-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="fd88c-118">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd88c-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="fd88c-119">**派遣** をクリックし、**在庫品目要求** をクリックして **在庫品目要求** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd88c-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="fd88c-120">このフォームに、サービス注文に対して作成されている在庫品目要求が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="fd88c-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="fd88c-121">削除する品目要求を選択し、**削除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd88c-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="fd88c-122">- または -</span><span class="sxs-lookup"><span data-stu-id="fd88c-122">–or–</span></span>

1.  <span data-ttu-id="fd88c-123">**プロジェクト管理および会計** \> **共通** \> **プロジェクト** \> **すべてのプロジェクト** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd88c-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="fd88c-124">在庫品目要求が作成されているサービス注文を含むプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd88c-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="fd88c-125">**プロジェクト** フォームの右ウィンドウで、**在庫品目要求** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd88c-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="fd88c-126">**在庫品目要求** フォームは、選択したプロジェクトに関連付けられている在庫品目要求を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="fd88c-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="fd88c-127">削除する品目要求を選択し、**削除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd88c-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd88c-128">参照</span><span class="sxs-lookup"><span data-stu-id="fd88c-128">See also</span></span>

<span data-ttu-id="fd88c-129">[在庫品目要求 (フォーム)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="fd88c-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]