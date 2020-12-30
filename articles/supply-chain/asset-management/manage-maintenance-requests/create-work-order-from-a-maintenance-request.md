---
title: メンテナンス要求からの作業指示書の作成
description: このトピックでは、資産管理のメンテナンス要求から作業指示書を作成する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432024"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="21739-103">メンテナンス要求からの作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="21739-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="21739-104">メンテナンス要求を作成した後、それらを簡単に作業指示書に変換できます。</span><span class="sxs-lookup"><span data-stu-id="21739-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="21739-105">このトピックでは、メンテナンス要求を処理し、複数のメンテナンス要求を同時更新してから、複数のメンテナンス要求の作業指示書を同時に作成する最も簡単な方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="21739-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="21739-106">**有効なメンテナンス要求** または **個人用の機能的な場所のメンテナンス要求** ページで、一度に 1 つのメンテナンス依頼を処理し、1 つのメンテナンス依頼を作業指示書に変換することもできます。</span><span class="sxs-lookup"><span data-stu-id="21739-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="21739-107">すべてのメンテナンス依頼は、1 つの作業指示書にのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="21739-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="21739-108">ただし、メンテナンス依頼の資産が異なる場合でも、1 つの作業指示書に複数のメンテナンス依頼を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="21739-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="21739-109">**資産管理** \> **共通** \> **メンテナンス要求** \> **すべてのメンテナンス要求** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="21739-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="21739-110">メンテナンス依頼から作業指示書を作成する前に、この情報が関連する場合は、少なくとも、メンテナンス依頼のメンテナンス作業タイプ、およびメンテナンス作業タイプ バリアントおよびトレードを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21739-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="21739-111">グリッド ビューでは、メンテナンス要求の情報を簡単に更新できます。</span><span class="sxs-lookup"><span data-stu-id="21739-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="21739-112">作業指示書を作成する準備ができたら、その作業指示書に含めるメンテナンス要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="21739-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="21739-113">作業指示書に変換する複数のメンテナンス依頼を選択する場合、作業指示書を作成する前に、**資産** フィールドおよび **メンテナンス作業タイプ** フィールドの両方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21739-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="21739-114">作業指示書に変換するメンテナンス依頼を 1 つ選択したする場合、作業指示書を作成する前に **資産** フィールドのみを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21739-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="21739-115">ただし、作業指示書を作成するときに、**作業指示書の作成** ダイアログ ボックスで、メンテナンス作業タイプ (およびこの情報が関連する場合、関連するメンテナンス作業タイプ バリアントおよびトレード) を選択できます。</span><span class="sxs-lookup"><span data-stu-id="21739-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="21739-116">**販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="21739-116">Select **Work order**.</span></span>
5. <span data-ttu-id="21739-117">**作業指示書の作成** ダイアログ ボックスで、フィールドを設定してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="21739-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="21739-118">メッセージ バーから、新しい作業指示書が作成されたことを通知してくる場合があります。</span><span class="sxs-lookup"><span data-stu-id="21739-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="21739-119">さらに、メンテナンス要求に基づく作業指示書を作成するときに、メンテナンス要求に関連する資産が保証契約に含まれている場合は、メッセージ バーから保証契約について通知があります。</span><span class="sxs-lookup"><span data-stu-id="21739-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="21739-120">**資産管理** \> **共通** \> **作業指示書** \> **すべての作業指示書** の順に選択し、新しい作業指示書を開きます。</span><span class="sxs-lookup"><span data-stu-id="21739-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![新しい作業指示書を開く](media/05-manage-maintenance-requests.png)

