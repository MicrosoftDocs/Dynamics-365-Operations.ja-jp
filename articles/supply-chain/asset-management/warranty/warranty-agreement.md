---
title: 保証契約
description: このトピックでは、資産管理の保証契約について説明します。
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021507"
---
# <a name="warranty-agreements"></a><span data-ttu-id="1f949-103">保証契約</span><span class="sxs-lookup"><span data-stu-id="1f949-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="1f949-104">資産管理では、資産または資産タイプに関連付けることができる保証条件を設定できます。</span><span class="sxs-lookup"><span data-stu-id="1f949-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="1f949-105">保証条件は特定の期間に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="1f949-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="1f949-106">保証は、完全補償または部分補償を行うように設定したり、時間、経費、および品目に関連する条件を設定したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="1f949-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="1f949-107">最初のステップでは、設備に関する仕入先保証契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="1f949-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="1f949-108">次に、資産または資産のタイプに保証契約を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="1f949-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="1f949-109">仕入先保証契約は、情報提供の目的でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="1f949-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="1f949-110">資産に対して仕入先保証が設定されている場合は、資産の保証期間を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1f949-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="1f949-111">保証契約の作成</span><span class="sxs-lookup"><span data-stu-id="1f949-111">Create a warranty agreement</span></span>

<span data-ttu-id="1f949-112">保証契約には、作業時間、経費、および品目の保証について、複数の契約明細行を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1f949-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="1f949-113">**資産管理** \> **設定** \> **資産** \> **保証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f949-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="1f949-114">**新規** を選択して製品を作成します。</span><span class="sxs-lookup"><span data-stu-id="1f949-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="1f949-115">**保証** フィールドに、保証 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f949-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="1f949-116">**名前** フィールドに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f949-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="1f949-117">**詳細** クイック タブの **資産** フィールドには、保証契約を使用する有効な資産の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f949-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="1f949-118">**保証明細** クイック タブで、次の手順に従って保証契約に含める明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1f949-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="1f949-119">**明細行の追加** を選択して、新しい条件を保証に追加します。</span><span class="sxs-lookup"><span data-stu-id="1f949-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="1f949-120">**明細行** フィールドに、連続する明細行番号が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="1f949-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="1f949-121">**期間** フィールドで、保証期間のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="1f949-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="1f949-122">**間隔** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f949-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="1f949-123">このフィールドでは、保証が有効な期間数を定義します。</span><span class="sxs-lookup"><span data-stu-id="1f949-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="1f949-124">**割合** フィールドに、保証明細行の補償割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f949-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="1f949-125">この割合は、会社の補償範囲を示します。</span><span class="sxs-lookup"><span data-stu-id="1f949-125">The percentage indicates how much is covered by your company.</span></span>

![保証ページ](media/01-warranty.png)
