---
title: 不適合工程の諸費用
description: このトピックでは、不適合の工程で使用できる品質諸費用を作成する方法について説明します。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956727"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="c8a1d-103">不適合工程の諸費用</span><span class="sxs-lookup"><span data-stu-id="c8a1d-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8a1d-104">このトピックでは、不適合の工程で使用できる品質諸費用を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="c8a1d-105">**品質諸費用** ページを使用して、不適合の行程で追加できる諸費用の種類を定義します。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="c8a1d-106">諸費用を使用すると、不適合製品に対して顧客に支払う必要がある手数料や諸費用、または受け取った不適合製品に対して仕入先が支払う必要がある手数料や諸費用に関する詳細を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="c8a1d-107">また諸費用を使用して、外部の仕入先または工程を実行するサービスに対して必要な原価を追跡することもできます。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="c8a1d-108">品質諸費用の例</span><span class="sxs-lookup"><span data-stu-id="c8a1d-108">Examples of quality charges</span></span>

<span data-ttu-id="c8a1d-109">製造会社に勤務しているとします。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-109">You work for a manufacturing company.</span></span> <span data-ttu-id="c8a1d-110">会社は複数の仕入先と契約を結んでいます。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="c8a1d-111">これらの契約では、品目の期限内出荷、損害、および製品品質に関する基準が示されます。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="c8a1d-112">同様に、複数の顧客が、返品、損害、および製品品質に関して会社と合意しています。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="c8a1d-113">手数料構造は状況ごとに定義され、契約で指定されます。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="c8a1d-114">品質諸費用を構成して、*損害*、*遅延出荷*、*品質* などさまざまな種類の費用を概要できます。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="c8a1d-115">その後、不適合を作成するときに、1 つ以上の行程を追加します。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="c8a1d-116">各行程に対して、**諸費用** を選択して手数料の詳細を定義します。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="c8a1d-117">品質諸費用を作成する</span><span class="sxs-lookup"><span data-stu-id="c8a1d-117">Create a quality charge</span></span>

1. <span data-ttu-id="c8a1d-118">**在庫管理 \> 設定 \> 品質管理 \> 品質諸費用** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="c8a1d-119">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="c8a1d-120">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="c8a1d-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c8a1d-121">**諸費用コード** – 品質諸費用の固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="c8a1d-122">**説明** – 品質諸費用の詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="c8a1d-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="c8a1d-124">不適合の行程に品質諸費用を追加する</span><span class="sxs-lookup"><span data-stu-id="c8a1d-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="c8a1d-125">不適合に行程を追加し、諸費用を適用する方法の詳細については、[不適合の工程](quality-operations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8a1d-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8a1d-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c8a1d-126">Additional resources</span></span>

- [<span data-ttu-id="c8a1d-127">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="c8a1d-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="c8a1d-128">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="c8a1d-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="c8a1d-129">不適合の承認を担当する作業者</span><span class="sxs-lookup"><span data-stu-id="c8a1d-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="c8a1d-130">不適合の検査ゾーン</span><span class="sxs-lookup"><span data-stu-id="c8a1d-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="c8a1d-131">不適合の診断タイプ</span><span class="sxs-lookup"><span data-stu-id="c8a1d-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="c8a1d-132">不適合の品質諸費用</span><span class="sxs-lookup"><span data-stu-id="c8a1d-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="c8a1d-133">不適合の工程</span><span class="sxs-lookup"><span data-stu-id="c8a1d-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="c8a1d-134">倉庫プロセスに対する品質管理</span><span class="sxs-lookup"><span data-stu-id="c8a1d-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
