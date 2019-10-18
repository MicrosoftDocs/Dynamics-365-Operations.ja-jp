---
title: 属性タイプの管理
description: このトピックでは、資産管理で属性タイプを作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783398"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="51ad5-103">属性タイプの管理</span><span class="sxs-lookup"><span data-stu-id="51ad5-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="51ad5-104">このトピックでは、資産管理で属性タイプを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="51ad5-105">属性は、さまざまな要素のプロパティを記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="51ad5-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="51ad5-106">次の要素の属性を設定できます。</span><span class="sxs-lookup"><span data-stu-id="51ad5-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="51ad5-107">機能的な場所のタイプ</span><span class="sxs-lookup"><span data-stu-id="51ad5-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="51ad5-108">機能的な場所</span><span class="sxs-lookup"><span data-stu-id="51ad5-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="51ad5-109">資産タイプ</span><span class="sxs-lookup"><span data-stu-id="51ad5-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="51ad5-110">資産</span><span class="sxs-lookup"><span data-stu-id="51ad5-110">Assets</span></span>

<span data-ttu-id="51ad5-111">設定できる属性は、要素によって異なります。</span><span class="sxs-lookup"><span data-stu-id="51ad5-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="51ad5-112">たとえば、機能的な場所の場合、場所の構成と物理サイズの属性を設定できます。</span><span class="sxs-lookup"><span data-stu-id="51ad5-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="51ad5-113">資産タイプまたは資産の場合、さまざまな条件下でエンジンのボリューム、パワー消費量、および最大積載能力の属性を設定できます。</span><span class="sxs-lookup"><span data-stu-id="51ad5-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="51ad5-114">属性タイプの作成</span><span class="sxs-lookup"><span data-stu-id="51ad5-114">Create attribute types</span></span>

<span data-ttu-id="51ad5-115">独自の属性タイプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="51ad5-115">You can create your own attribute types.</span></span> <span data-ttu-id="51ad5-116">また、Microsoft Dynamics 365 for Finance and Operations から**属性タイプ** ページに製品分析コードを転送できます。</span><span class="sxs-lookup"><span data-stu-id="51ad5-116">Additionally, you can transfer product dimensions from Microsoft Dynamics 365 for Finance and Operations to the **Attribute types** page.</span></span>

1. <span data-ttu-id="51ad5-117">**資産管理** \> **設定** \> **属性タイプ**選択します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="51ad5-118">属性タイプを初めて設定する場合は、**製品分析コードの作成**を選択し、標準の Finance and Operations 製品分析コードを自動的に転送します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard Finance and Operations product dimensions.</span></span>
3. <span data-ttu-id="51ad5-119">**新規作成**を選択して、新しい属性タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="51ad5-120">**属性タイプ** フィールドに、属性タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="51ad5-121">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="51ad5-122">**単位**フィールドで、必要に応じて関連する属性単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="51ad5-123">**データ型**フィールドで、単位のデータ型を選択します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="51ad5-124">データ型として**文字列**を選択した場合は、次の手順に従って属性タイプの値を作成します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="51ad5-125">属性タイプを選択し、**値**を選択します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="51ad5-126">**属性値**フィールドで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="51ad5-127">**属性タイプ** フィールドで、属性タイプ (分析コード) を選択します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="51ad5-128">**値**フィールドで、関連する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="51ad5-129">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="51ad5-130">レコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-130">Save the record.</span></span>
    7. <span data-ttu-id="51ad5-131">**属性タイプ** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="51ad5-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="51ad5-132">レコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="51ad5-132">Save the record.</span></span>

    <span data-ttu-id="51ad5-133">**機能的な場所のタイプ** フィールドには、属性タイプを使用する機能的な場所の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="51ad5-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="51ad5-134">**資産タイプ** フィールドには、使用する資産タイプの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="51ad5-134">The **Asset types** field shows the number of asset types that are using it.</span></span>