---
title: "生産需要に基づく委託販売在庫の所有権の変更"
description: "この手順は、生産中における在庫需要があるときに委託製品在庫所有者を仕入先から自らの法人に変更する方法を示します。"
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 5925f5423d596adc4326dfff4734de2afd80b5a8
ms.contentlocale: ja-jp
ms.lasthandoff: 09/12/2017

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="ae37b-103">生産需要に基づく委託販売在庫の所有権の変更</span><span class="sxs-lookup"><span data-stu-id="ae37b-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae37b-104">この手順は、生産中における在庫需要があるときに委託製品在庫所有者を仕入先から自らの法人に変更する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ae37b-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="ae37b-105">所有権を変更するには、在庫所有権変更仕訳を作成、転記します。</span><span class="sxs-lookup"><span data-stu-id="ae37b-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="ae37b-106">所有権変更は、既存の生産需要に基づき、この記録で示されるように手作業で作成します。</span><span class="sxs-lookup"><span data-stu-id="ae37b-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="ae37b-107">通常、現場の監督者がこの作業を実施します。</span><span class="sxs-lookup"><span data-stu-id="ae37b-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="ae37b-108">デモ データ会社 USMF でこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="ae37b-109">自分のデータを使用する場合は、次の条件があることを確認します: 在庫所有権変更に設定された在庫仕訳、物理的に記録された仕入先所有の手持在庫品目、原材料の複数の製造オーダーライン</span><span class="sxs-lookup"><span data-stu-id="ae37b-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="ae37b-110">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="ae37b-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="ae37b-111">在庫所有権仕訳を作成する</span><span class="sxs-lookup"><span data-stu-id="ae37b-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="ae37b-112">[在庫管理] > [仕訳入力] > [品目] > [在庫所有権変更] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ae37b-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="ae37b-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae37b-113">Click New.</span></span>
    * <span data-ttu-id="ae37b-114">在庫所有権変更仕訳は、委託製品在庫の所有者を仕入先から現事業者に変更するために用いられます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="ae37b-115">この所有権を変更するには、仕入先所有の手持在庫を解除して現事業者で当該在庫を受領します。</span><span class="sxs-lookup"><span data-stu-id="ae37b-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="ae37b-116">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ae37b-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="ae37b-117">所有権変更の仕訳種類がある在庫仕訳名のみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="ae37b-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae37b-118">Click OK.</span></span>
5. <span data-ttu-id="ae37b-119">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae37b-119">Click Functions.</span></span>
6. <span data-ttu-id="ae37b-120">[製造オーダーから仕訳帳明細行を作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae37b-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="ae37b-121">原材料消費の需要を有する製品を問い合わせることで所有権変更処理を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="ae37b-122">フィールドを含む在庫払出では、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae37b-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="ae37b-123">このオプションによって、在庫トランザクションの状態別にフィルターすることができます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="ae37b-124">たとえば、物理的状況を選択、保存している在庫の仕訳を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="ae37b-125">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ae37b-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="ae37b-126">このセクションでは、追加のフィルターを適用することができます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="ae37b-127">たとえば、特定の原材料の日付を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="ae37b-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae37b-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="ae37b-129">在庫所有権変更仕訳を転記する</span><span class="sxs-lookup"><span data-stu-id="ae37b-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="ae37b-130">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae37b-130">Click Post.</span></span>
    * <span data-ttu-id="ae37b-131">仕訳を記帳する際、仕入先所有の在庫は「所有権変更」の参照で解除されます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="ae37b-132">その後在庫は、購入注文製品受領書で更新された在庫トランザクションを使用して手持ちの在庫として受領されます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="ae37b-133">記帳済み仕訳に関連するトランザクションのみが作成されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ae37b-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="ae37b-134">在庫トランザクションの予定は作成されません。</span><span class="sxs-lookup"><span data-stu-id="ae37b-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="ae37b-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae37b-135">Click OK.</span></span>
3. <span data-ttu-id="ae37b-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ae37b-136">Close the page.</span></span>

