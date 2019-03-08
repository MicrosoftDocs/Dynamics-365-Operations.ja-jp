---
title: 部分的に引当済の移動オーダーのバッチ リリース
description: このトピックでは、モバイル デバイスから、部分的に引当済の移動オーダーのバッチ リリースを設定し、適用する方法について説明します。
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 578b9875deec077a077b54a9227815e2c4fd3b2d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "343722"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="a503e-103">部分的に引当済の移動オーダーのバッチ リリース</span><span class="sxs-lookup"><span data-stu-id="a503e-103">Batch release of partially reserved transfer orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a503e-104">部分的に引当済の移動オーダーのバッチ リリースの機能で、バッチ ジョブを使用して、移動オーダーを倉庫に部分的にリリースできます。</span><span class="sxs-lookup"><span data-stu-id="a503e-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="a503e-105">一部の数量をリリースするオプションがあるため、注文をリリースする前に倉庫で全体の注文数量が入手可能になるのを待つ必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a503e-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="a503e-106">倉庫へのオーダーのリリースは、高度な倉庫管理プロセスです。</span><span class="sxs-lookup"><span data-stu-id="a503e-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="a503e-107">このプロセスには、倉庫作業者がモバイル デバイスを使用して実行できる、ピッキング、梱包、出荷などの活動が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a503e-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="a503e-108">該当する場所</span><span class="sxs-lookup"><span data-stu-id="a503e-108">Where it applies</span></span>

<span data-ttu-id="a503e-109">この機能のため、移動オーダーはバッチ ジョブを使用して倉庫にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="a503e-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="a503e-110">この機能は倉庫に十分な在庫がない場合に便利ですが、それでも 1 つの倉庫から別の倉庫へ品目を移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a503e-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="a503e-111">設定方法</span><span class="sxs-lookup"><span data-stu-id="a503e-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="a503e-112">移動オーダーおよび販売注文のフルフィルメント基準を指定します。</span><span class="sxs-lookup"><span data-stu-id="a503e-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="a503e-113">注文をバッチで倉庫に部分的にリリースする前に、フルフィルメント基準を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="a503e-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="a503e-114">このフルフィルメント基準は、フルフィルメント ポリシーによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="a503e-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="a503e-115">販売注文および移動オーダーのフルフィルメント ポリシーは、会社レベルで指定します。</span><span class="sxs-lookup"><span data-stu-id="a503e-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="a503e-116">フルフィルメント ポリシーの設定に応じて、バッチでの注文のリリースが承認または却下されます。</span><span class="sxs-lookup"><span data-stu-id="a503e-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="a503e-117">その後、その結果に応じて注文が処理されます。</span><span class="sxs-lookup"><span data-stu-id="a503e-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="a503e-118">移動オーダーおよび販売注文のフルフィルメント ポリシーを作成するには、**倉庫管理** \> **設定** \> **倉庫にリリース** \> **フルフィルメント ポリシー** を順にクリックしてから、名前と説明を入力してフルフィルメント ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="a503e-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="a503e-119">フルフィルメント率、値の型、またフルフィルメント ポリシーに違反した場合に表示するメッセージを指定するには、**倉庫管理** \> **設定** \> **倉庫にリリース** \> **フルフィルメント ポリシー** を順にクリックしてから、**フルフィルメント率**、**値の型**、および **フルフィルメント違反メッセージ** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="a503e-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="a503e-120">移動オーダーおよび販売注文のフルフィルメント ポリシーを設定します。</span><span class="sxs-lookup"><span data-stu-id="a503e-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="a503e-121">移動オーダーのフルフィルメント ポリシーを設定するには、**在庫管理** \> **設定** \> **在庫および倉庫管理パラメーター** \> **移動オーダー** \> **倉庫管理** を順にクリックしてから、移動オーダー フルフィルメント ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="a503e-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="a503e-122">販売注文のフルフィルメント ポリシーを設定するには、**売掛金勘定** \> **設定** \> **売掛金勘定パラメーター** \> **倉庫管理** を順にクリックしてから、販売注文フルフィルメント ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="a503e-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="a503e-123">バッチでのリリースを許可し、バッチでリリースする数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="a503e-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="a503e-124">バッチ ジョブを使用して、バッチで倉庫に注文をリリースします。</span><span class="sxs-lookup"><span data-stu-id="a503e-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="a503e-125">バッチ ジョブで実行する必要のある注文を区別するパラメーターは、バッチ ジョブ自体に設定します。</span><span class="sxs-lookup"><span data-stu-id="a503e-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="a503e-126">**数量** パラメーターは、全体の数量または現物引当済の数量をバッチでリリースする必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a503e-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="a503e-127">**部分的にリリースされた注文のリリースを許可** パラメーターは、以前に部分的にリリースされていた場合に、バッチでの注文を承認するか却下するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a503e-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="a503e-128">移動オーダーの **数量** および **部分的にリリースされた注文のリリースを許可** パラメーターを設定するには、**倉庫管理** \> **倉庫にリリース** \> **移動オーダーの自動リリース** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a503e-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="a503e-129">販売注文の **数量** および **部分的にリリースされた注文のリリースを許可** パラメーターを設定するには、**倉庫管理** \> **倉庫にリリース** \> **販売注文の自動リリース** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a503e-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>
