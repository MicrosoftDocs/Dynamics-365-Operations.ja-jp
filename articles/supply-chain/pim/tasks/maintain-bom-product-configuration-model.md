---
title: 製品コンフィギュレーション モデルの BOM の管理
description: この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457aa5720919d8455a3099b200980bb36f60577f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567725"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="314f1-103">製品コンフィギュレーション モデルの BOM の管理</span><span class="sxs-lookup"><span data-stu-id="314f1-103">Maintain BOM for a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="314f1-104">この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="314f1-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="314f1-105">この手順を作成するのに、デモ会社 USMF の [ハイエンド スピーカー] モデルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="314f1-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="314f1-106">BOM 明細行の追加</span><span class="sxs-lookup"><span data-stu-id="314f1-106">Add a BOM line</span></span>
1. <span data-ttu-id="314f1-107">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="314f1-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="314f1-108">[製品コンフィギュレーション モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="314f1-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="314f1-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="314f1-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="314f1-110">この手順で [ハイエンド スピーカー] を選択します。</span><span class="sxs-lookup"><span data-stu-id="314f1-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="314f1-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="314f1-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="314f1-112">[BOM 明細行] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="314f1-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="314f1-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="314f1-113">Click Add.</span></span>
7. <span data-ttu-id="314f1-114">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="314f1-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="314f1-115">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="314f1-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="314f1-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="314f1-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="314f1-117">BOM 明細行の詳細の追加</span><span class="sxs-lookup"><span data-stu-id="314f1-117">Add BOM line details</span></span>
1. <span data-ttu-id="314f1-118">[BOM 明細行の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="314f1-118">Click BOM line details.</span></span>
2. <span data-ttu-id="314f1-119">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="314f1-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="314f1-120">たとえば、品目 M0055 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="314f1-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="314f1-121">各 BOM 明細行プロパティに、固定値をとるか、属性にマップさせるかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="314f1-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="314f1-122">[設定] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="314f1-122">Select the Set check box.</span></span>
4. <span data-ttu-id="314f1-123">[計算] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="314f1-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="314f1-124">[計算] プロパティで [はい] を設定すると、原価計算に BOM 明細行 が含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="314f1-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="314f1-125">[設定] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="314f1-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="314f1-126">[設定] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="314f1-126">Select the Set check box.</span></span>
7. <span data-ttu-id="314f1-127">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="314f1-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="314f1-128">数量フィールドは、BOM に含まれる品目の数量を決定します。</span><span class="sxs-lookup"><span data-stu-id="314f1-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="314f1-129">これは、属性のマッピングの明確な候補になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="314f1-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="314f1-130">[分析コード] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="314f1-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="314f1-131">製品分析コードのいずれかが有効であるかどうかを確認します。したがって、値または属性が割り当て済である必要があります。</span><span class="sxs-lookup"><span data-stu-id="314f1-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="314f1-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="314f1-132">Click OK.</span></span>

