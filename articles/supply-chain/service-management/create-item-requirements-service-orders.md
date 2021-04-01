---
title: サービス注文の在庫品目要求の作成
description: サービス注文に特定の品目を引き当てる必要がある場合、その在庫品目要求を作成できます。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b342b20cc11addc53fc6ea4e1a23d3b449eb9ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257945"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="fda7c-103">サービス注文の在庫品目要求の作成</span><span class="sxs-lookup"><span data-stu-id="fda7c-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fda7c-104">顧客に提供するサービスを追跡および管理するサービス注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="fda7c-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="fda7c-105">サービス注文に特定の品目を引き当てる必要がある場合、その在庫品目要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="fda7c-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="fda7c-106">品目要求を在庫からすぐ消費したり、その品目の製造オーダーを開始できます。</span><span class="sxs-lookup"><span data-stu-id="fda7c-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="fda7c-107">品目トランザクションではなく在庫品目要求を使用することによって、品目が実際に使用される直前の配送を計画したり、発注書を作成したり、品目を売買契約の枠組みに含めたり、在庫品目要求を生産計画に含めたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="fda7c-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="fda7c-108">サービス注文に関する要求はプロジェクトを通じて処理します。</span><span class="sxs-lookup"><span data-stu-id="fda7c-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="fda7c-109">サービス注文に対して在庫品目要求を作成するには、サービス注文をプロジェクトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda7c-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="fda7c-110">サービス注文に対して在庫品目要求を作成した後、選択したプロジェクトの **プロジェクト** フォームに在庫品目要求を表示できます。</span><span class="sxs-lookup"><span data-stu-id="fda7c-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="fda7c-111">サービス注文の在庫品目要求の作成</span><span class="sxs-lookup"><span data-stu-id="fda7c-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="fda7c-112">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fda7c-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="fda7c-113">在庫品目要求を作成するサービス注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="fda7c-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="fda7c-114">**アクション ウィンドウ** の **出荷** タブで、**在庫品目要求** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fda7c-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="fda7c-115">**在庫品目要求** フォームで、必要な品目の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="fda7c-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="fda7c-116">フォームのそれぞれのフィールドについては、[在庫品目要求 (フォーム)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fda7c-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="fda7c-117">サービス契約の在庫品目要求の作成</span><span class="sxs-lookup"><span data-stu-id="fda7c-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="fda7c-118">**サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fda7c-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="fda7c-119">在庫品目要求を作成するサービス契約を開きます。</span><span class="sxs-lookup"><span data-stu-id="fda7c-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="fda7c-120">**明細行** クイックタブで、**追加** をクリックして明細行を新規作成します。</span><span class="sxs-lookup"><span data-stu-id="fda7c-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="fda7c-121">**トランザクション タイプ** フィールドで、**品目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fda7c-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="fda7c-122">**項目の設定** フィールドで、**在庫品目要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fda7c-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="fda7c-123">**品目番号** フィールドで、サービス契約に必要な品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="fda7c-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="fda7c-124">**サイト** フィールドの、**製品分析コード** タブにおける、**明細行の詳細** クイック タブで、品目の在庫サイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="fda7c-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="fda7c-125">契約項目からサービス注文を作成するには、**明細行** クイック タブで **サービス注文の作成** をクリックし、**サービス注文の作成** フォームに、関連情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="fda7c-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="fda7c-126">参照</span><span class="sxs-lookup"><span data-stu-id="fda7c-126">See also</span></span>

<span data-ttu-id="fda7c-127">[サービス注文の自動作成](create-service-orders-automatically.md)。</span><span class="sxs-lookup"><span data-stu-id="fda7c-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]