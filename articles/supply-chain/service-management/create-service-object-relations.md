---
title: サービス対象関係の作成
description: このトピックでは、サービス契約またはサービス注文のサービス対象の関係を作成する方法について説明します。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab5de850ef40c26e447b96d8f42ccf83fb490818
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202770"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="46307-103">サービス対象関係の作成</span><span class="sxs-lookup"><span data-stu-id="46307-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="46307-104">このトピックでは、サービス契約またはサービス注文のサービス対象の関係を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="46307-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="46307-105">サービス対象の関係を作成すると、サービス対象がサービス契約またはサービス注文に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="46307-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="46307-106">顧客がサービス対象である品目に対するサービスを要求すると、サービス対象の関係の一覧からサービス対象を選択できます。</span><span class="sxs-lookup"><span data-stu-id="46307-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="46307-107">サービス契約に対するサービス対象の関係の作成</span><span class="sxs-lookup"><span data-stu-id="46307-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="46307-108">次の手順で、サービス契約に対してサービス対象の関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="46307-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="46307-109">**サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="46307-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="46307-110">**サービス契約**一覧で、既存のサービス契約を選択するか、**新規**をクリックして新しいサービス契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="46307-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="46307-111">**関係**グループの**サービス契約**タブの、**アクション ウィンドウ**における、**サービス契約**フォームで、**サービス対象**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="46307-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="46307-112">**サービス対象**フォームで、**新規**をクリックし、このサービス契約に対するサービス対象を選択します。</span><span class="sxs-lookup"><span data-stu-id="46307-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="46307-113">テンプレートの部品表 (BOM) をサービス契約に割り当てるには、**機能**をクリックし、**テンプレート BOM の添付**を選択します。</span><span class="sxs-lookup"><span data-stu-id="46307-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="46307-114">**テンプレート BOM の選択**フォームの**テンプレート**フィールドで、テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="46307-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="46307-115">サービス注文に対するサービス対象の関係の作成</span><span class="sxs-lookup"><span data-stu-id="46307-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="46307-116">次の手順で、サービス注文に対してサービス対象の関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="46307-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="46307-117">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="46307-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="46307-118">**サービス注文**一覧で既存のサービス注文を選択するか、新しいサービス注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="46307-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="46307-119">**関係**グループの**サービス注文**タブの、**アクション ウィンドウ**における、**サービス注文**フォームで、**サービス対象**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="46307-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="46307-120">**サービス対象** フォームで、**新規**をクリックし、このサービス注文に対するサービス対象を選択します。</span><span class="sxs-lookup"><span data-stu-id="46307-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="46307-121">テンプレート BOM をサービス契約に割り当てるには、**機能**をクリックし、**テンプレート BOM の添付**を選択します。</span><span class="sxs-lookup"><span data-stu-id="46307-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="46307-122">**テンプレート BOM の選択**フォームの**テンプレート**フィールドで、テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="46307-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="46307-123">参照</span><span class="sxs-lookup"><span data-stu-id="46307-123">See also</span></span>

[<span data-ttu-id="46307-124">サービス対象の概要</span><span class="sxs-lookup"><span data-stu-id="46307-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="46307-125">サービス対象の関係</span><span class="sxs-lookup"><span data-stu-id="46307-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="46307-126">テンプレート BOM</span><span class="sxs-lookup"><span data-stu-id="46307-126">Template BOMs</span></span>](template-boms.md)

  


