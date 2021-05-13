---
title: 不適合の検査ゾーン
description: このトピックでは、不適合の検査ゾーンを作成および使用する方法について説明します。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956733"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="786a0-103">不適合の検査ゾーン</span><span class="sxs-lookup"><span data-stu-id="786a0-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="786a0-104">このトピックでは、不適合の検査ゾーンを作成および使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="786a0-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="786a0-105">**検査ゾーン** ページを使用して、不適合に割り当てることができるゾーンを定義します。</span><span class="sxs-lookup"><span data-stu-id="786a0-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="786a0-106">不適合を作成する場合、**不適合** ページの **全般** タブで、**検査ゾーン** フィールドおよび **検査タイプ** フィールドを設定できます。</span><span class="sxs-lookup"><span data-stu-id="786a0-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="786a0-107">**検査ゾーン** フィールドは通常、品目が保管されているエリアまたは場所を示します。</span><span class="sxs-lookup"><span data-stu-id="786a0-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="786a0-108">**検査タイプ** フィールドは、品目を *使用制限* または *使用不可* として定義します。</span><span class="sxs-lookup"><span data-stu-id="786a0-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="786a0-109">不適合または不適合の修正レポートを印刷すると、品目が配置されている検査ゾーンを表示できます。</span><span class="sxs-lookup"><span data-stu-id="786a0-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="786a0-110">不適合の不適合タグを印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="786a0-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="786a0-111">このレポートには、割り当てられた検査ゾーンと使用法に関する情報が表示され、欠陥材料をどのように扱うべきかに関するガイダンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="786a0-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="786a0-112">検査ゾーンは在庫場所または運営リソースに対応する場合があります。</span><span class="sxs-lookup"><span data-stu-id="786a0-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="786a0-113">検査ゾーンの例</span><span class="sxs-lookup"><span data-stu-id="786a0-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="786a0-114">例 1</span><span class="sxs-lookup"><span data-stu-id="786a0-114">Example 1</span></span>

<span data-ttu-id="786a0-115">テレビ、スピーカー、メディア プレーヤーを製造および販売している電子製品製造会社で働いているとします。</span><span class="sxs-lookup"><span data-stu-id="786a0-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="786a0-116">この場合、各タイプの製品を表す検査ゾーンを構成できます。</span><span class="sxs-lookup"><span data-stu-id="786a0-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="786a0-117">例 2</span><span class="sxs-lookup"><span data-stu-id="786a0-117">Example 2</span></span>

<span data-ttu-id="786a0-118">3 つの容器と 2 つのラックは、不適合品目を保管するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="786a0-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="786a0-119">この場合は、5 つの検査ゾーン (各容器と各ラックごとに 1 つずつ) を構成できます。</span><span class="sxs-lookup"><span data-stu-id="786a0-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="786a0-120">検査ゾーンの作成</span><span class="sxs-lookup"><span data-stu-id="786a0-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="786a0-121">**在庫管理 \> 設定 \> 品質管理 \> 検査ゾーン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="786a0-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="786a0-122">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="786a0-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="786a0-123">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="786a0-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="786a0-124">**検査ゾーン** – 検査ゾーンの固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="786a0-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="786a0-125">**説明** – 検査ゾーンの詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="786a0-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="786a0-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="786a0-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="786a0-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="786a0-127">Additional resources</span></span>

- [<span data-ttu-id="786a0-128">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="786a0-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="786a0-129">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="786a0-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="786a0-130">不適合の承認を担当する作業者</span><span class="sxs-lookup"><span data-stu-id="786a0-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="786a0-131">不適合の問題タイプ</span><span class="sxs-lookup"><span data-stu-id="786a0-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="786a0-132">不適合の診断タイプ</span><span class="sxs-lookup"><span data-stu-id="786a0-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="786a0-133">不適合の品質諸費用</span><span class="sxs-lookup"><span data-stu-id="786a0-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="786a0-134">不適合の工程</span><span class="sxs-lookup"><span data-stu-id="786a0-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="786a0-135">倉庫プロセスに対する品質管理</span><span class="sxs-lookup"><span data-stu-id="786a0-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
