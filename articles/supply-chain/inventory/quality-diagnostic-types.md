---
title: 不適合の診断タイプ
description: このトピックでは、不適合で使用できる診断タイプの使用方法および作成方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022279"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="93345-103">不適合の診断タイプ</span><span class="sxs-lookup"><span data-stu-id="93345-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93345-104">このトピックでは、不適合で使用できる診断タイプの使用方法および作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="93345-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="93345-105">診断アクションの分類を定義するには、**診断タイプ** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="93345-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="93345-106">その後、不適合に対する修正を作成するときに、診断を選択します。</span><span class="sxs-lookup"><span data-stu-id="93345-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="93345-107">訂正は、承認された不適合に対して行う必要のある診断アクションのタイプ、担当者などを指定します。</span><span class="sxs-lookup"><span data-stu-id="93345-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="93345-108">また、要求された完了日、予定完了日を指定します。</span><span class="sxs-lookup"><span data-stu-id="93345-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="93345-109">診断タイプの例</span><span class="sxs-lookup"><span data-stu-id="93345-109">Examples of diagnostic types</span></span>

<span data-ttu-id="93345-110">製造会社で勤務しており、複数の品目が品質テストに合格しなかったとします。</span><span class="sxs-lookup"><span data-stu-id="93345-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="93345-111">これらの品目は検査領域に移動し、不適合製品としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="93345-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="93345-112">不適合レコードが Microsoft Dynamics 365 Supply Chain Management で作成され、問題解決を通じて詳細を追跡します。</span><span class="sxs-lookup"><span data-stu-id="93345-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="93345-113">この例では、品目のパッケージ化する機械のベアリングが劣化し過熱しているため、品質上の問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="93345-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="93345-114">この問題の修正には、機械の部品の交換が必要です。</span><span class="sxs-lookup"><span data-stu-id="93345-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="93345-115">診断タイプを構成する場合、複数のレコードを作成できます。各レコードは、機械に発生する可能性のあるさまざまな種類の問題を表します。</span><span class="sxs-lookup"><span data-stu-id="93345-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="93345-116">または、機械の修理を表す 1 つの包括的な診断タイプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="93345-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="93345-117">診断タイプを作成する</span><span class="sxs-lookup"><span data-stu-id="93345-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="93345-118">**在庫管理 \> 設定 \> 品質管理 \> 診断タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="93345-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="93345-119">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="93345-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="93345-120">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="93345-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="93345-121">**診断** – 診断タイプの固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="93345-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="93345-122">**説明** – 診断タイプの詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="93345-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="93345-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="93345-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93345-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="93345-124">Additional resources</span></span>

- [<span data-ttu-id="93345-125">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="93345-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="93345-126">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="93345-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="93345-127">不適合の承認を担当する作業者</span><span class="sxs-lookup"><span data-stu-id="93345-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="93345-128">不適合の検査ゾーン</span><span class="sxs-lookup"><span data-stu-id="93345-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="93345-129">不適合の問題タイプ</span><span class="sxs-lookup"><span data-stu-id="93345-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="93345-130">不適合の品質諸費用</span><span class="sxs-lookup"><span data-stu-id="93345-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="93345-131">不適合の工程</span><span class="sxs-lookup"><span data-stu-id="93345-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="93345-132">倉庫プロセスに対する品質管理</span><span class="sxs-lookup"><span data-stu-id="93345-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
