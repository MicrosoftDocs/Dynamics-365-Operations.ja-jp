---
title: Field Service から Supply Chain Management への在庫振替および在庫調整の同期
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: fce407a66c339f2ece4bbc37b30243a2ed172d0a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251892"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="20d26-103">Field Service から Supply Chain Management への在庫振替および在庫調整の同期</span><span class="sxs-lookup"><span data-stu-id="20d26-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="20d26-104">このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="20d26-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="20d26-105">[![Supply Chain Management および Field Service 間の業務プロセスの同期](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="20d26-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="20d26-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="20d26-106">Templates and tasks</span></span>
<span data-ttu-id="20d26-107">次のテンプレートと基本的なタスクは、在庫調整を同期化し、Field Service から Supply Chain Management に振り替えるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="20d26-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="20d26-108">**データ統合でのテンプレート**</span><span class="sxs-lookup"><span data-stu-id="20d26-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="20d26-109">在庫調整 (Field Service から Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="20d26-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="20d26-110">在庫振替 (Field Service から Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="20d26-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="20d26-111">**データ統合プロジェクトのタスク:**</span><span class="sxs-lookup"><span data-stu-id="20d26-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="20d26-112">在庫調整</span><span class="sxs-lookup"><span data-stu-id="20d26-112">Inventory Adjustments</span></span>
- <span data-ttu-id="20d26-113">在庫振替</span><span class="sxs-lookup"><span data-stu-id="20d26-113">Inventory Transfers</span></span>

## <a name="table-set"></a><span data-ttu-id="20d26-114">テーブル セット</span><span class="sxs-lookup"><span data-stu-id="20d26-114">Table set</span></span>
| <span data-ttu-id="20d26-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="20d26-115">Field Service</span></span>                     | <span data-ttu-id="20d26-116">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="20d26-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="20d26-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="20d26-117">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="20d26-118">Dataverse 在庫調整仕訳帳のヘッダーおよび明細行</span><span class="sxs-lookup"><span data-stu-id="20d26-118">Dataverse Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="20d26-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="20d26-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="20d26-120">Dataverse 在庫移動仕訳帳のヘッダーおよび明細行</span><span class="sxs-lookup"><span data-stu-id="20d26-120">Dataverse inventory transfer journal headers and lines</span></span>   |

## <a name="table-flow"></a><span data-ttu-id="20d26-121">テーブル フロー</span><span class="sxs-lookup"><span data-stu-id="20d26-121">Table flow</span></span>
<span data-ttu-id="20d26-122">**ステータスを転記** が **作成済** から **転記済** に変更された後、Field Service で行われた在庫調整と振替は Supply Chain Management と同期します。</span><span class="sxs-lookup"><span data-stu-id="20d26-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="20d26-123">このような場合は、調整または移動オーダーがロックされ、読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="20d26-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="20d26-124">つまり、調整および転送は Supply Chain Management に転記されますが、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="20d26-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="20d26-125">Supply Chain Management では、調整を自動的に転記し、統合中に生成された在庫仕訳帳を振り替えるようにバッチ ジョブを設定できます。</span><span class="sxs-lookup"><span data-stu-id="20d26-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="20d26-126">バッチ ジョブを有効にする方法の詳細については、以下の前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20d26-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="20d26-127">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="20d26-127">Field Service CRM solution</span></span> 
<span data-ttu-id="20d26-128">**在庫単位** 列は、**製品** テーブルに追加されました。</span><span class="sxs-lookup"><span data-stu-id="20d26-128">The **Inventory unit** column has been added to the **Product** table.</span></span> <span data-ttu-id="20d26-129">販売および在庫単位は Supply Chain Management で常に同じであるとは限らないため、この列は必要です。また倉庫在庫の Supply Chain Management では、在庫単位が必要です。</span><span class="sxs-lookup"><span data-stu-id="20d26-129">This column is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="20d26-130">在庫調整と在庫振替の両方の在庫調整製品に製品を設定すると、在庫製品の値から単位がフェッチされます。</span><span class="sxs-lookup"><span data-stu-id="20d26-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="20d26-131">値が見つかると、在庫調整製品の **単位** 列がロックされます。</span><span class="sxs-lookup"><span data-stu-id="20d26-131">If a value is found, the **Unit** column will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="20d26-132">**在庫調整** テーブルと **在庫振替** テーブルの両方に、**転記ステータス** 列が追加されました。</span><span class="sxs-lookup"><span data-stu-id="20d26-132">The **Post status** column has been added to both the **Inventory adjustment** table and the **Inventory transfer** table.</span></span> <span data-ttu-id="20d26-133">この列は、調整または振替が Supply Chain Management に送信されるときにフィルターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="20d26-133">This column is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="20d26-134">この列の既定値は作成済 (1) ですが、Supply Chain Management には送信されません。</span><span class="sxs-lookup"><span data-stu-id="20d26-134">The default for this column is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="20d26-135">転記済 (2) の値を更新する場合、Supply Chain Management に送信されますが、以降調整または振替を変更したり、新しい明細行を追加することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="20d26-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="20d26-136">**番号順序** 列は、**在庫調整製品** テーブルに追加されました。</span><span class="sxs-lookup"><span data-stu-id="20d26-136">The **Number sequence** column has been added to the **Inventory adjustment product** table.</span></span> <span data-ttu-id="20d26-137">この列は、統合に固有の番号があり、統合が調整を作成および更新できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="20d26-137">This column ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="20d26-138">最初の在庫調整製品を作成すると、**P2C 自動採番** テーブルに新しいレコードが作成され、番号シリーズと使用される接頭語が維持されます。</span><span class="sxs-lookup"><span data-stu-id="20d26-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** table to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="20d26-139">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="20d26-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="20d26-140">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="20d26-140">Supply Chain Management</span></span>
<span data-ttu-id="20d26-141">統合によって生成される統合在庫仕訳帳は、バッチ ジョブを使用して自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="20d26-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="20d26-142">これは、**在庫管理 > 定期処理タスク > Dataverse 統合 > 統合在庫仕訳帳** の転記から有効になります。</span><span class="sxs-lookup"><span data-stu-id="20d26-142">This is enabled from **Inventory management > Periodic tasks > Dataverse integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="20d26-143">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="20d26-143">Template mapping in Data integration</span></span>

<span data-ttu-id="20d26-144">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="20d26-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="20d26-145">在庫調整 (Field Service から Supply Chain Management): 在庫調整</span><span class="sxs-lookup"><span data-stu-id="20d26-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="20d26-146">[![データ統合のテンプレートのマッピング](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="20d26-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="20d26-147">在庫振替 (Field Service から Supply Chain Management): 在庫振替</span><span class="sxs-lookup"><span data-stu-id="20d26-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="20d26-148">[![データ統合のテンプレートのマッピング](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="20d26-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]