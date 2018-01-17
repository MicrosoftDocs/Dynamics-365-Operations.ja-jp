---
title: "委託販売の設定"
description: "このトピックでは、入庫委託販売在庫工程をコンフィギュレーションする方法を説明します。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 3e86aa8a718a36d61cfb3bd0c93007b209636113
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-consignment"></a><span data-ttu-id="18749-103">委託販売の設定</span><span class="sxs-lookup"><span data-stu-id="18749-103">Set up consignment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="18749-104">このトピックでは、入庫委託販売在庫工程をコンフィギュレーションする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="18749-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="18749-105">委託販売在庫は、仕入先によって所有されているが、サイトで保管されている在庫です。</span><span class="sxs-lookup"><span data-stu-id="18749-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="18749-106">在庫を消費するか、または使用する準備ができたら、在庫の所有権を引き継ぎます。</span><span class="sxs-lookup"><span data-stu-id="18749-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="18749-107">このトピックでは、委託販売プロセスを有効にするのに必要な設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="18749-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="18749-108">委託販売プロセスに関する詳細については、「[委託販売](consignment.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18749-108">For more information about consignment processes, see [Consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="18749-109">在庫所有者</span><span class="sxs-lookup"><span data-stu-id="18749-109">Inventory owners</span></span>
<span data-ttu-id="18749-110">現物入庫の委託販売の在庫を記録するには、仕入先の所有者を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18749-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="18749-111">これは、[**在庫所有者**] のページで行われます。</span><span class="sxs-lookup"><span data-stu-id="18749-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="18749-112">[**仕入先口座**] を選択すると、[**名前**] と [**所有者**] のフィールドの規定値が生成されます。</span><span class="sxs-lookup"><span data-stu-id="18749-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="18749-113">[**所有者**] フィールドの値が仕入先に表示されるので、仕入先口座名が外部ユーザーに認識されにくい場合は変更することができます。</span><span class="sxs-lookup"><span data-stu-id="18749-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="18749-114">[**所有者**] フィールドを編集できますが、**在庫所有者**記録を保存する時点までです。</span><span class="sxs-lookup"><span data-stu-id="18749-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="18749-115">[**名前**] フィールドには、仕入先口座が関連付けられている当事者名を入力できますが、変更できません。</span><span class="sxs-lookup"><span data-stu-id="18749-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="18749-116">[![在庫所有者](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="18749-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="18749-117">追跡用分析コード グループ</span><span class="sxs-lookup"><span data-stu-id="18749-117">Tracking dimension group</span></span>
<span data-ttu-id="18749-118">委託販売プロセスで使用される品目は、**所有者**分析コードが**有効**に設定されている**追跡用分析コード グループ**に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="18749-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="18749-119">所有者分析コードは、常に [**現物在庫**] と [**資産在庫**] オプションが選択されます。</span><span class="sxs-lookup"><span data-stu-id="18749-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="18749-120">[**分析コード別補充計画**] は選択されません。</span><span class="sxs-lookup"><span data-stu-id="18749-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="18749-121">[![追跡用分析コード グループ](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="18749-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="18749-122">在庫所有権変更仕訳</span><span class="sxs-lookup"><span data-stu-id="18749-122">Inventory ownership change journal</span></span>
<span data-ttu-id="18749-123">**在庫所有権変更**仕訳張は、委託販売在庫の所有権の仕入先から消費している法人への移転の記録に使用されます。</span><span class="sxs-lookup"><span data-stu-id="18749-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="18749-124">在庫仕訳帳のように、在庫仕訳帳の名前で識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18749-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="18749-125">これらの名前は、[**在庫仕訳帳の名前**] ページで作成され、[**仕訳帳タイプ**] は、[**所有権変更**] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18749-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="18749-126">[![在庫所有権変更仕訳](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="18749-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="18749-127">委託販売プロセスでの仕入先コラボレーション</span><span class="sxs-lookup"><span data-stu-id="18749-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="18749-128">仕入先コラボレーション インターフェイスを使用している仕入れ先は、サイトで在庫の消費を監視するために、これを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="18749-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="18749-129">仕入先コラボレーションを使用する仕入先の設定については、「[仕入先コラボレーション ユーザーのセキュリティのコンフィギュレーション](../procurement/configure-security-vendor-portal-users.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18749-129">For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](../procurement/configure-security-vendor-portal-users.md).</span></span>

