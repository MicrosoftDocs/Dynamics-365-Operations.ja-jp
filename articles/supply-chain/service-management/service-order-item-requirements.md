---
title: サービス注文品目の要件
description: サービス注文に特定の品目を引き当てる必要がある場合、その在庫品目要求を作成できます。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8866d8a4d6ad879f2c43b470af98457cb7c75721
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985743"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="3274a-103">サービス注文品目の要件</span><span class="sxs-lookup"><span data-stu-id="3274a-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3274a-104">顧客に提供するサービスを追跡および管理するサービス注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="3274a-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="3274a-105">サービス注文に特定の品目を引き当てる必要がある場合、その在庫品目要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="3274a-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="3274a-106">品目要求を在庫からすぐ消費したり、その品目の製造オーダーを開始できます。</span><span class="sxs-lookup"><span data-stu-id="3274a-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="3274a-107">品目トランザクションではなく在庫品目要求を使用することによって、品目が実際に使用される直前の配送を計画したり、発注書を作成したり、品目を売買契約の枠組みに含めたり、在庫品目要求を生産計画に含めたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="3274a-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="3274a-108">サービス注文に関する要求はプロジェクトを通じて処理します。</span><span class="sxs-lookup"><span data-stu-id="3274a-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="3274a-109">サービス注文に対して在庫品目要求を作成するには、サービス注文をプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="3274a-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="3274a-110">サービス注文に対して作成された在庫品目要求は、個々のサービス注文の**プロジェクト**から、または**販売注文**フォームを使用して表示できます。</span><span class="sxs-lookup"><span data-stu-id="3274a-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="3274a-111">サービス注文からの在庫品目要求の表示</span><span class="sxs-lookup"><span data-stu-id="3274a-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="3274a-112">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3274a-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="3274a-113">**派遣**をクリックし、**在庫品目要求**をクリックして**在庫品目要求**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="3274a-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="3274a-114">**プロジェクト**タブをクリックし、**サービス注文**フィールドで在庫品目要求のサービス注文を確認します。</span><span class="sxs-lookup"><span data-stu-id="3274a-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="3274a-115">在庫品目要求を含むサービス注文の削除</span><span class="sxs-lookup"><span data-stu-id="3274a-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="3274a-116">サービス注文に対して在庫品目要求が作成されている場合は、サービス注文を削除できません。</span><span class="sxs-lookup"><span data-stu-id="3274a-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="3274a-117">サービス注文を削除する前に、在庫品目要求を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3274a-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="3274a-118">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3274a-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="3274a-119">**派遣**をクリックし、**在庫品目要求**をクリックして**在庫品目要求**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="3274a-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="3274a-120">このフォームに、サービス注文に対して作成されている在庫品目要求が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="3274a-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="3274a-121">削除する品目要求を選択し、**削除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3274a-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="3274a-122">- または -</span><span class="sxs-lookup"><span data-stu-id="3274a-122">–or–</span></span>

1.  <span data-ttu-id="3274a-123">**プロジェクト管理および会計** \> **共通** \> **プロジェクト** \> **すべてのプロジェクト**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3274a-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="3274a-124">在庫品目要求が作成されているサービス注文を含むプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="3274a-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="3274a-125">**プロジェクト**フォームの右ウィンドウで、**在庫品目要求**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3274a-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="3274a-126">**在庫品目要求**フォームは、選択したプロジェクトに関連付けられている在庫品目要求を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="3274a-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="3274a-127">削除する品目要求を選択し、**削除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3274a-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="3274a-128">参照</span><span class="sxs-lookup"><span data-stu-id="3274a-128">See also</span></span>

<span data-ttu-id="3274a-129">[在庫品目要求 (フォーム)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="3274a-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

