---
title: "サービス対象グループ"
description: "対象グループは、レポートや統計用の対象に関するデータの並べ替えやフィルタ処理を行う場合に便利です。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2ab3ed8a8f36f980473b17b5dfed8cb3d0054253
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="a9a88-103">サービス対象グループ</span><span class="sxs-lookup"><span data-stu-id="a9a88-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9a88-104">対象グループは、レポートや統計用の対象に関するデータの並べ替えやフィルタ処理を行う場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="a9a88-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="a9a88-105">たとえば、地理的な場所またはタイプ別に対象をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="a9a88-106">地理的な場所別のグループ化</span><span class="sxs-lookup"><span data-stu-id="a9a88-106">Group by geographical location</span></span>

<span data-ttu-id="a9a88-107">このグループ化の方法を使用すると、会社がサービスを提供しているさまざまな対象の場所を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="a9a88-108">地理的な場所別に対象をグループ化すると、たとえば、特定の国/地域で既にサービスを提供している対象を識別する必要がある場合などにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="a9a88-109">例</span><span class="sxs-lookup"><span data-stu-id="a9a88-109">Example</span></span>

<span data-ttu-id="a9a88-110">ベルギーの顧客からサービス センターに電話があり、対象 ABC のサービス合意を作成するように依頼されました。</span><span class="sxs-lookup"><span data-stu-id="a9a88-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="a9a88-111">ベルギーでサービスを提供しているすべての対象には、ベルギーという地理的な場所の対象グループを関連付けてあります。</span><span class="sxs-lookup"><span data-stu-id="a9a88-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="a9a88-112">フィルタとしてこのグループを使用して、プログラムに既に ABC のレコードがあるか、または新しい対象を設定する必要があるかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="a9a88-113">タイプ別のグループ化</span><span class="sxs-lookup"><span data-stu-id="a9a88-113">Group by type</span></span>

<span data-ttu-id="a9a88-114">このグループ化の方法を使用すると、会社でサービスを実行している対象のタイプを表示できます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="a9a88-115">タイプ別に対象をグループ化すると、たとえば、既にプログラムに存在する同様の対象に基づいて新しい対象を作成する場合などにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="a9a88-116">例</span><span class="sxs-lookup"><span data-stu-id="a9a88-116">Example</span></span>

<span data-ttu-id="a9a88-117">顧客から電話があり、空調機械 HIJ のサービス合意を設定するように依頼されました。</span><span class="sxs-lookup"><span data-stu-id="a9a88-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="a9a88-118">既にこの機械のレコードがありません。</span><span class="sxs-lookup"><span data-stu-id="a9a88-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="a9a88-119">ただし、空調装置という名前のオブジェクト グループを設定して、このグループは空調機械のすべてのオブジェクトに関連付されました。</span><span class="sxs-lookup"><span data-stu-id="a9a88-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="a9a88-120">したがって、他の空調機械すべてをすばやく検索し、これらのオブジェクトのテンプレート情報を使用してHIJ のサービス契約項目を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="a9a88-121">この方法で対象グループを使用して、簡単に新しい対象を設定し、実行するサービス作業を決定できます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="a9a88-122">サービス対象グループの作成</span><span class="sxs-lookup"><span data-stu-id="a9a88-122">Create service object groups</span></span>

<span data-ttu-id="a9a88-123">サービス対象を割り当てることができるグループを作成します。</span><span class="sxs-lookup"><span data-stu-id="a9a88-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="a9a88-124">サービス対象とは、サービスを実行する他の製品および在庫品目です。</span><span class="sxs-lookup"><span data-stu-id="a9a88-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="a9a88-125">サービス対象のグループ化することによって、同様のそして関連するサービス対象のレポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="a9a88-126">たとえば、サービス対象グループは 2 種類のサービス対象から構成される場合があります: 1 番目のサービス対象はキット、2 番目のサービス対象はキットをインストールするサービスです。</span><span class="sxs-lookup"><span data-stu-id="a9a88-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="a9a88-127">サービス対象グループを作成するには、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="a9a88-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="a9a88-128">**サービス管理 > 設定 > サービス対象 > サービス対象グループ**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9a88-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="a9a88-129">**新規**をクリックして、新しいサービス対象グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="a9a88-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="a9a88-130">サービス対象グループに一意の名前、および必要に応じて説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a9a88-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="a9a88-131">**サービス対象**フォームを使用すると、グループにサービス対象を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="a9a88-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="a9a88-132">参照</span><span class="sxs-lookup"><span data-stu-id="a9a88-132">See also</span></span>

[<span data-ttu-id="a9a88-133">サービス対象の作成</span><span class="sxs-lookup"><span data-stu-id="a9a88-133">Create service objects</span></span>](create-service-objects.md)



