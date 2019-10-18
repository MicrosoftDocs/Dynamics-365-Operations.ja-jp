---
title: 入庫および出庫資産
description: このトピックでは、資産管理で入庫および出庫資産を登録する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847554"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="e7b81-103">入庫および出庫資産</span><span class="sxs-lookup"><span data-stu-id="e7b81-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e7b81-104">会社が他の場所または顧客から受け取った資産の修復作業またはメンテナンス作業をする場合、資産管理は、会社に向かう途中の入庫資産と返される出庫資産の両方を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="e7b81-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="e7b81-105">入庫および出庫のライフサイクル状態を使用して、入庫および出庫される資産を管理する場合は、これらのアクションをサポートするライフスタイル モデルを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7b81-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="e7b81-106">詳細については、[メンテナンス要求の設定](../setup-for-maintenance-requests/requests.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7b81-106">For more information, see [Setup for maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="e7b81-107">資産管理の設定によって、入庫資産と出庫資産を操作できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="e7b81-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="e7b81-108">資産を入庫として登録する</span><span class="sxs-lookup"><span data-stu-id="e7b81-108">Register assets as inbound</span></span>

1. <span data-ttu-id="e7b81-109">**資産管理**\>**共通**\>**メンテナンス要求**\>**有効なメンテナンス要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="e7b81-110">メンテナンス要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="e7b81-111">**メンテナンス要求の状態の更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="e7b81-112">**入庫** (または入庫資産用に作成した別のライフサイクル状態) を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![図 1](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="e7b81-114">入庫資産を入庫済として登録する</span><span class="sxs-lookup"><span data-stu-id="e7b81-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="e7b81-115">**資産管理**\>**共通**\>**入庫/出庫資産**\>**入庫資産**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="e7b81-116">資産またはメンテナンス要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="e7b81-117">**資産の受入**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="e7b81-118">**受入済**フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="e7b81-119">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-119">Then select **OK**.</span></span> <span data-ttu-id="e7b81-120">レコードは、**入庫資産**リスト ページから削除されます。</span><span class="sxs-lookup"><span data-stu-id="e7b81-120">The record is removed from the **Inbound assets** list page.</span></span>

![図 2](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="e7b81-122">資産を出庫として登録する</span><span class="sxs-lookup"><span data-stu-id="e7b81-122">Register assets as outbound</span></span>

<span data-ttu-id="e7b81-123">メンテナンス作業または修理作業が完了したら、資産を返却済として登録できます。</span><span class="sxs-lookup"><span data-stu-id="e7b81-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="e7b81-124">**資産管理**\>**共通**\>**メンテナンス要求**\>**有効なメンテナンス要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="e7b81-125">メンテナンス要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="e7b81-126">**メンテナンス要求の状態の更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="e7b81-127">**出庫** (または出庫資産用に作成した別のライフサイクル状態) を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="e7b81-128">出庫資産を配送済として登録する</span><span class="sxs-lookup"><span data-stu-id="e7b81-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="e7b81-129">**資産管理**\>**共通**\>**入庫/出庫資産**\>**出庫資産**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="e7b81-130">資産またはメンテナンス要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="e7b81-131">**資産を配送**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="e7b81-132">**配送済**フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="e7b81-133">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7b81-133">Then select **OK**.</span></span> <span data-ttu-id="e7b81-134">レコードは、**出庫資産**リスト ページから削除されます。</span><span class="sxs-lookup"><span data-stu-id="e7b81-134">The record is removed from the **Outbound assets** list page.</span></span>