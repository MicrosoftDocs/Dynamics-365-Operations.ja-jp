---
title: 不適合の問題タイプ
description: このトピックでは、不適合の問題タイプを作成および使用する方法について説明します。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956734"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="5cee2-103">不適合の問題タイプ</span><span class="sxs-lookup"><span data-stu-id="5cee2-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cee2-104">このトピックでは、不適合の問題タイプを作成および使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="5cee2-105">**問題タイプ** ページを使用して、さまざまな不適合タイプで発生する可能性のある品質上の問題の分類を定義します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="5cee2-106">作成する問題タイプごとに、問題タイプを使用できる不適合のタイプを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cee2-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="5cee2-107">次の不適合タイプを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5cee2-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="5cee2-108">**内部** – このタイプの不適合は、手持在庫に関連しています (たとえば、品質指示や検査指示)。</span><span class="sxs-lookup"><span data-stu-id="5cee2-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="5cee2-109">**顧客** – このタイプの不適合は、販売注文に関連しています。</span><span class="sxs-lookup"><span data-stu-id="5cee2-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="5cee2-110">**仕入先** – このタイプの不適合は、発注書に関連しています。</span><span class="sxs-lookup"><span data-stu-id="5cee2-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="5cee2-111">**サービス要求** – このタイプの不適合は、サービス注文に関連しています。</span><span class="sxs-lookup"><span data-stu-id="5cee2-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="5cee2-112">**生産** – このタイプの不適合は、バッチ オーダーまたは製造オーダーに関連しています。</span><span class="sxs-lookup"><span data-stu-id="5cee2-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="5cee2-113">**連産品の生産** – このタイプの不適合は、連産品のバッチ オーダーに関連しています。</span><span class="sxs-lookup"><span data-stu-id="5cee2-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="5cee2-114">新しい問題タイプを作成する場合は、アクション ウィンドウで **不適合タイプ** を選択して、その問題タイプに対して承認されている 1 つ以上の不適合タイプの一覧を作成します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="5cee2-115">たとえば、欠陥コードに関する問題タイプは、すべての不適合タイプに適用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5cee2-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="5cee2-116">ただし、顧客の苦情に関連する問題タイプは、**顧客** および **サービス要求** の不適合タイプにのみ適用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5cee2-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="5cee2-117">問題タイプの例</span><span class="sxs-lookup"><span data-stu-id="5cee2-117">Examples of problem types</span></span>

<span data-ttu-id="5cee2-118">さまざまな不適合タイプで使用できる問題タイプのシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="5cee2-119">**顧客:** 顧客が苦情を申し立て、顧客が返品を行った、または品質仕様が満たされていなかった。</span><span class="sxs-lookup"><span data-stu-id="5cee2-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="5cee2-120">**仕入先:** 製品が破損していた、品質仕様が満たされていなかった、または間違った製品を受け取った。</span><span class="sxs-lookup"><span data-stu-id="5cee2-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="5cee2-121">**サービス要求:** 品質仕様が満たされていなかった、顧客が苦情を申し立てた、または機械のメンテナンスが必要である。</span><span class="sxs-lookup"><span data-stu-id="5cee2-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="5cee2-122">**生産:** 品質仕様を満たしていない、機械のメンテナンスが必要、または製品が破損していた。</span><span class="sxs-lookup"><span data-stu-id="5cee2-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="5cee2-123">**連産品の生産:** 品質仕様を満たしていない、機械のメンテナンスが必要、または製品が破損していた。</span><span class="sxs-lookup"><span data-stu-id="5cee2-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="5cee2-124">問題タイプの作成および不適合タイプへの割り当て</span><span class="sxs-lookup"><span data-stu-id="5cee2-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="5cee2-125">**在庫管理 \> 設定 \> 品質管理 \> 問題タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="5cee2-126">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5cee2-127">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="5cee2-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5cee2-128">**問題タイプ** – 問題タイプの固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="5cee2-129">**説明** – 問題タイプの詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="5cee2-130">新しい行がまだ選択されている間に、アクション ウィンドウで **不適合** タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="5cee2-131">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5cee2-132">次に、新しい行に対して、**不適合タイプ** フィールドを、問題タイプに対して許可する不適合タイプに設定します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="5cee2-133">問題タイプに対して許可する追加の不適合タイプごとに、前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="5cee2-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="5cee2-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5cee2-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5cee2-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5cee2-135">Additional resources</span></span>

- [<span data-ttu-id="5cee2-136">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="5cee2-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="5cee2-137">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="5cee2-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="5cee2-138">不適合の承認を担当する作業者</span><span class="sxs-lookup"><span data-stu-id="5cee2-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="5cee2-139">不適合の検査ゾーン</span><span class="sxs-lookup"><span data-stu-id="5cee2-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="5cee2-140">不適合の診断タイプ</span><span class="sxs-lookup"><span data-stu-id="5cee2-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="5cee2-141">不適合の品質諸費用</span><span class="sxs-lookup"><span data-stu-id="5cee2-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="5cee2-142">不適合の工程</span><span class="sxs-lookup"><span data-stu-id="5cee2-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="5cee2-143">倉庫プロセスに対する品質管理</span><span class="sxs-lookup"><span data-stu-id="5cee2-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
