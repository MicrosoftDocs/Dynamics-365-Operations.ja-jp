---
title: サービス注文の自動作成
description: 1 つのサービス契約または複数のサービス契約に対して、サービス注文を作成できます。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee68190b117b974ff4131f5d2237d138cac1fda3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552279"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="ace4c-103">サービス注文の自動作成</span><span class="sxs-lookup"><span data-stu-id="ace4c-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ace4c-104">1 つのサービス契約または複数のサービス契約に対して、サービス注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ace4c-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="ace4c-105">作成したサービス注文は、**サービス注文**フォームで表示できます。</span><span class="sxs-lookup"><span data-stu-id="ace4c-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="ace4c-106">サービス注文は、サービス契約の有効期間に対してのみ作成されます。</span><span class="sxs-lookup"><span data-stu-id="ace4c-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="ace4c-107">**サービス注文の作成**フォームで指定する範囲がサービス契約の開始日の前または終了日の後である場合、サービス注文は、その範囲のうちサービス契約日の期間内にある期間に対してのみ作成されます。</span><span class="sxs-lookup"><span data-stu-id="ace4c-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="ace4c-108">サービス注文を手動で作成する場合、またはサービス合意項目から自動的に作成する場合、その項目に対して終了日が指定されていない場合を除き、サービス注文は、その項目の開始日と終了日で定義された時間間隔内に該当する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ace4c-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="ace4c-109">サービス契約に対するサービス注文の自動作成</span><span class="sxs-lookup"><span data-stu-id="ace4c-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="ace4c-110">**サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="ace4c-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="ace4c-111">サービス合意を選択します。</span><span class="sxs-lookup"><span data-stu-id="ace4c-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="ace4c-112">**出荷**タブをクリックし、**計画されたサービス注文**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ace4c-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="ace4c-113">**開始日**および**終了日**フィールドに日付を指定して、サービス期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="ace4c-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="ace4c-114">**情報ログの表示**チェック ボックスをオンにして、作成されたサービス注文の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="ace4c-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="ace4c-115">**トランザクション タイプを含む**フィールド グループで、トランザクション タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ace4c-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="ace4c-116">トランザクション タイプは、サービス契約で作成された項目を表し、選択した各トランザクション タイプは、サービス契約項目で指定されたサービス期間に応じて複数のサービス注文を生成します。</span><span class="sxs-lookup"><span data-stu-id="ace4c-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="ace4c-117">連続する一連のサービス注文に不足しているサービス注文を作成するには、**継続**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="ace4c-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="ace4c-118">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ace4c-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="ace4c-119">複数のサービス契約に対するサービス注文の自動作成</span><span class="sxs-lookup"><span data-stu-id="ace4c-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="ace4c-120">**サービス管理** \> **定期処理** \> **サービス注文** \> **サービス注文の作成**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="ace4c-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="ace4c-121">**選択**をクリックして、サービス注文の作成に使用する基準を追加または削除するための選択を行います。</span><span class="sxs-lookup"><span data-stu-id="ace4c-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="ace4c-122">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ace4c-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ace4c-123">参照</span><span class="sxs-lookup"><span data-stu-id="ace4c-123">See also</span></span>

[<span data-ttu-id="ace4c-124">サービス注文</span><span class="sxs-lookup"><span data-stu-id="ace4c-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="ace4c-125">サービス注文の自動作成</span><span class="sxs-lookup"><span data-stu-id="ace4c-125">Automatically creating service orders</span></span>](auto-create-service-orders.md)

  


