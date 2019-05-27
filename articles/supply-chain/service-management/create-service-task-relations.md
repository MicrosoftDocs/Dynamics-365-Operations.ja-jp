---
title: サービス作業関係の作成
description: サービス契約またはサービス注文で実行するサービス作業を記述するには、サービス作業をその契約または注文に関連付けることができます。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aa0e5200ff2a6822e631c72124335e2dc556c14
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552118"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="41755-103">サービス作業関係の作成</span><span class="sxs-lookup"><span data-stu-id="41755-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41755-104">サービス契約またはサービス注文で実行するサービス作業を記述するには、サービス作業をその契約または注文に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="41755-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="41755-105">この情報は、サービス技術者および顧客が利用できます。</span><span class="sxs-lookup"><span data-stu-id="41755-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="41755-106">サービス合意との関係の作成</span><span class="sxs-lookup"><span data-stu-id="41755-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="41755-107">**サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="41755-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="41755-108">既存のサービス合意を選択するか、新しいサービス合意を作成します。</span><span class="sxs-lookup"><span data-stu-id="41755-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="41755-109">アクション ウィンドウで、**サービス作業**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="41755-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="41755-110">**サービス作業**フォームで Ctrl + N キーを押して新しい行を作成し、**サービス作業**リストからサービス作業を選択して、サービス作業をサービス契約に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="41755-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="41755-111">**説明**タブで、自由書式のフィールドに内部または外部の任意のメモ説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="41755-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="41755-112">フォームを閉じてレコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="41755-112">Close the form to save the record.</span></span>

<span data-ttu-id="41755-113">この手順を繰り返して、必要なすべてのサービス作業をサービス合意に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="41755-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="41755-114">これらのサービス作業は、関連付けられた任意の合意明細行に対して指定できます。</span><span class="sxs-lookup"><span data-stu-id="41755-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="41755-115">サービス合意に対して作成したサービス作業関係は、そのサービス合意に関連付けられているすべてのサービス注文から使用できます。</span><span class="sxs-lookup"><span data-stu-id="41755-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="41755-116">サービス注文との関係の作成</span><span class="sxs-lookup"><span data-stu-id="41755-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="41755-117">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="41755-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="41755-118">既存のサービス注文を選択するか、新しいサービス注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="41755-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="41755-119">アクション ウィンドウで、**サービス作業**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="41755-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="41755-120">**サービス作業**フォームから、Ctrl + N キーを押して新しい行を作成し、**サービス作業**リストからサービス作業を選択して、サービス作業をサービス注文に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="41755-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="41755-121">**説明**タブで、自由書式のフィールドに内部または外部の任意のメモ説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="41755-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="41755-122">フォームを閉じてレコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="41755-122">Close the form to save the record.</span></span>

<span data-ttu-id="41755-123">この手順を繰り返して、必要なすべてのサービス作業をサービス注文に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="41755-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="41755-124">関係を作成したサービス作業は、サービス注文明細行の作成時に選択できます。</span><span class="sxs-lookup"><span data-stu-id="41755-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="41755-125">サービス注文に対して作成されたサービス作業関係は、そのサービス注文でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="41755-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="41755-126">参照</span><span class="sxs-lookup"><span data-stu-id="41755-126">See also</span></span>

[<span data-ttu-id="41755-127">サービス作業</span><span class="sxs-lookup"><span data-stu-id="41755-127">Service tasks</span></span>](service-tasks.md)


  


