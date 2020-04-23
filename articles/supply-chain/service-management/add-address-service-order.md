---
title: 住所をサービス注文に追加する
description: このトピックでは、サービス注文に顧客の住所を追加する方法について説明します。
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5b1c0e300edc45ae3f4be9eae8afa56e06cccd6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203092"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="e6187-103">住所をサービス注文に追加する</span><span class="sxs-lookup"><span data-stu-id="e6187-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e6187-104">このトピックでは、サービス注文に顧客の住所を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6187-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="e6187-105">サービス注文を作成する際、住所情報は、そのサービス注文が関連付けられているプロジェクトから転送されます。</span><span class="sxs-lookup"><span data-stu-id="e6187-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="e6187-106">ただし、顧客、仕入先、サイト、倉庫、サービス注文およびプロジェクトの Microsoft Dynamics AX に既に入力した住所から別の場所を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="e6187-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="e6187-107">また、新しい住所を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="e6187-107">You can also create a new address.</span></span> <span data-ttu-id="e6187-108">既定では、新しい住所はプロジェクトに転送されます。</span><span class="sxs-lookup"><span data-stu-id="e6187-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="e6187-109">ただし、新しい住所がサービスのこのインスタンスにのみ関連するよう指定できます。</span><span class="sxs-lookup"><span data-stu-id="e6187-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="e6187-110">その場合、新しい住所はプロジェクトに転送されません。</span><span class="sxs-lookup"><span data-stu-id="e6187-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="e6187-111">サービス注文に対する顧客の住所の作成</span><span class="sxs-lookup"><span data-stu-id="e6187-111">Create a customer address for a service order</span></span>

<span data-ttu-id="e6187-112">サービス注文に住所を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e6187-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="e6187-113">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6187-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="e6187-114">住所を作成するサービス注文を開きます。</span><span class="sxs-lookup"><span data-stu-id="e6187-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="e6187-115">**アクション ペイン**で**編集**をクリックして、**ヘッダー ビュー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6187-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="e6187-116">**アドレス**クイック タブで、**住所の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6187-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="e6187-117">**新しい住所**フォームに、住所の一意の名前を入力し、残りのフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="e6187-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="e6187-118">既存の住所と同じ名前を入力した場合、残りのフィールドに入力した情報が、既存の住所の情報に上書きされます。</span><span class="sxs-lookup"><span data-stu-id="e6187-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="e6187-119">自分のサービス注文に新しい住所をコピーするには **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6187-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="e6187-120">サービス注文に対する代替住所の指定</span><span class="sxs-lookup"><span data-stu-id="e6187-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="e6187-121">サービス注文に別の住所を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e6187-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="e6187-122">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6187-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="e6187-123">別の住所を入力するサービス注文を開きます。</span><span class="sxs-lookup"><span data-stu-id="e6187-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="e6187-124">**アクション ペイン**で**編集**をクリックして、**ヘッダー ビュー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6187-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="e6187-125">**アドレス**クイック タブで、**その他の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6187-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="e6187-126">**レコード タイプ**フィールドの**アドレスの選択**フォームで、**サービス注文**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6187-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="e6187-127">住所を選択して **OK** をクリックし、自分のサービス注文にコピーします。</span><span class="sxs-lookup"><span data-stu-id="e6187-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


