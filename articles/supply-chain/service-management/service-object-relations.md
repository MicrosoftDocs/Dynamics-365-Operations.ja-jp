---
title: "サービス対象の関係"
description: "サービス対象とサービス合意またはサービス注文の間に、サービス対象の関係を作成できます。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: 0e54a0dc9b643077d45fe76e073772e81f99ea44
ms.contentlocale: ja-jp
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-relations"></a><span data-ttu-id="02386-103">サービス対象の関係</span><span class="sxs-lookup"><span data-stu-id="02386-103">Service object relations</span></span> 

[!include[banner](../includes/banner.md)]



<span data-ttu-id="02386-104">サービス対象とサービス合意またはサービス注文の間に、サービス対象の関係を作成できます。</span><span class="sxs-lookup"><span data-stu-id="02386-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="02386-105">関係を作成すると、サービス対象がサービス合意またはサービス注文に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="02386-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="02386-106">リレーションが作成された後、サービス合意またはサービス注文の任意の明細行にサービス対象を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="02386-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="02386-107">テンプレート BOM</span><span class="sxs-lookup"><span data-stu-id="02386-107">Template BOMs</span></span>

<span data-ttu-id="02386-108">サービス対象の関係にはテンプレート BOM を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="02386-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="02386-109">テンプレート BOM は、サービスの実行対象に対する部品表です。</span><span class="sxs-lookup"><span data-stu-id="02386-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="02386-110">サービス訪問時にサービス対象の部品を交換する場合は、[サービス対象] フォームを使用して、この変更をサービス BOM に登録できます。</span><span class="sxs-lookup"><span data-stu-id="02386-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="02386-111">例</span><span class="sxs-lookup"><span data-stu-id="02386-111">Example</span></span>

<span data-ttu-id="02386-112">顧客サイトで 2 台のエレベーターを点検するサービス合意を作成します。</span><span class="sxs-lookup"><span data-stu-id="02386-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="02386-113">このサービス合意の ID は SAL-001 です。</span><span class="sxs-lookup"><span data-stu-id="02386-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="02386-114">このエレベーターは、[サービス対象] フォームで EL-S/1000 および EL-L/1000 という対象として設定されています。</span><span class="sxs-lookup"><span data-stu-id="02386-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="02386-115">このサービス対象 (EL-S/1000 および EL-L/1000) をサービス合意に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="02386-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="02386-116">サービス対象の部品を交換した場合に、その対象の BOM に変更を登録する必要があります。そこで、次の表のように、サービス BOM をサービス対象の関係に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="02386-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="02386-117">サービス対象</span><span class="sxs-lookup"><span data-stu-id="02386-117">Service object</span></span> | <span data-ttu-id="02386-118">リレーション - サービス契約</span><span class="sxs-lookup"><span data-stu-id="02386-118">Relation – Service agreement</span></span> | <span data-ttu-id="02386-119">サービス BOM</span><span class="sxs-lookup"><span data-stu-id="02386-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="02386-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="02386-120">EL-S/1000</span></span>      | <span data-ttu-id="02386-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="02386-121">ID SAL-001</span></span>                   | <span data-ttu-id="02386-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="02386-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="02386-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="02386-123">EL-L/1000</span></span>      | <span data-ttu-id="02386-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="02386-124">ID SAL-001</span></span>                   | <span data-ttu-id="02386-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="02386-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="02386-126">この合意にはサービス対象の関係が存在するため、上記の対象に対して次の表のようにサービス合意項目を作成できます。</span><span class="sxs-lookup"><span data-stu-id="02386-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="02386-127">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="02386-127">Transaction type</span></span> | <span data-ttu-id="02386-128">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="02386-128">Category</span></span>           | <span data-ttu-id="02386-129">サービス対象</span><span class="sxs-lookup"><span data-stu-id="02386-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="02386-130">時間</span><span class="sxs-lookup"><span data-stu-id="02386-130">Hour</span></span>             | <span data-ttu-id="02386-131">検査</span><span class="sxs-lookup"><span data-stu-id="02386-131">Inspection</span></span>         | <span data-ttu-id="02386-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="02386-132">EL-S/1000</span></span>      |
| <span data-ttu-id="02386-133">時間</span><span class="sxs-lookup"><span data-stu-id="02386-133">Hour</span></span>             | <span data-ttu-id="02386-134">ギアボックスのクリーニング</span><span class="sxs-lookup"><span data-stu-id="02386-134">Gear box cleaning</span></span>  | <span data-ttu-id="02386-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="02386-135">EL-S/1000</span></span>      |
| <span data-ttu-id="02386-136">品目</span><span class="sxs-lookup"><span data-stu-id="02386-136">Item</span></span>             | <span data-ttu-id="02386-137">クリーニング用具</span><span class="sxs-lookup"><span data-stu-id="02386-137">Cleaning materials</span></span> | <span data-ttu-id="02386-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="02386-138">EL-S/1000</span></span>      |
| <span data-ttu-id="02386-139">時間</span><span class="sxs-lookup"><span data-stu-id="02386-139">Hour</span></span>             | <span data-ttu-id="02386-140">検査</span><span class="sxs-lookup"><span data-stu-id="02386-140">Inspection</span></span>         | <span data-ttu-id="02386-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="02386-141">EL-L/1000</span></span>      |
| <span data-ttu-id="02386-142">時間</span><span class="sxs-lookup"><span data-stu-id="02386-142">Hour</span></span>             | <span data-ttu-id="02386-143">ギアボックスのクリーニング</span><span class="sxs-lookup"><span data-stu-id="02386-143">Gearbox cleaning</span></span>   | <span data-ttu-id="02386-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="02386-144">EL-L/1000</span></span>      |
| <span data-ttu-id="02386-145">品目</span><span class="sxs-lookup"><span data-stu-id="02386-145">Item</span></span>             | <span data-ttu-id="02386-146">クリーニング用具</span><span class="sxs-lookup"><span data-stu-id="02386-146">Cleaning materials</span></span> | <span data-ttu-id="02386-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="02386-147">EL-L/1000</span></span>      |

<span data-ttu-id="02386-148">サービス訪問時にエレベーター EL-S/1000 のギアボックスを交換する必要が生じました。</span><span class="sxs-lookup"><span data-stu-id="02386-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="02386-149">この対象の部品を交換するには、現在のサービス合意に対して設定したサービス対象の関係を使用して、BOM デザイナにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="02386-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="02386-150">サービス対象の関係を使用した BOM デザイナへのアクセス</span><span class="sxs-lookup"><span data-stu-id="02386-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="02386-151">サービス契約</span><span class="sxs-lookup"><span data-stu-id="02386-151">Service agreements</span></span>
2. <span data-ttu-id="02386-152">サービス契約をダブルクリックするか、[サービス契約] をクリックしてサービス契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="02386-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="02386-153">[設定] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="02386-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="02386-154">テンプレート BOM をサービス合意に関連付けるには、[サービス対象] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02386-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="02386-155">[サービス対象] フォームでは、テンプレート BOM を変更する [デザイナー] フォームを開いて [デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="02386-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="02386-156">自動的に作成されるサービス注文</span><span class="sxs-lookup"><span data-stu-id="02386-156">Automatically created service orders</span></span>

<span data-ttu-id="02386-157">サービス合意に対してサービス注文を自動的に作成すると、合意におけるサービス対象の関係が、サービス注文にも作成されます。</span><span class="sxs-lookup"><span data-stu-id="02386-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


