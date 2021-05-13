---
title: 製品コンフィギュレーション モデルの BOM の管理
description: この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921320"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="49f49-103">製品コンフィギュレーション モデルの BOM の管理</span><span class="sxs-lookup"><span data-stu-id="49f49-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49f49-104">この手順を実行するには、既存の製品コンフィギュレーション モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="49f49-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="49f49-105">この手順を作成するのに、デモ会社 USMF の [ハイエンド スピーカー] モデルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="49f49-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="49f49-106">BOM 明細行の追加</span><span class="sxs-lookup"><span data-stu-id="49f49-106">Add a BOM line</span></span>

1. <span data-ttu-id="49f49-107">**製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="49f49-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="49f49-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="49f49-109">この手順で [ハイエンド スピーカー] を選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="49f49-110">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="49f49-111">**BOM 明細行** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="49f49-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="49f49-112">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-112">Select **Add**.</span></span>
1. <span data-ttu-id="49f49-113">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49f49-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="49f49-114">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49f49-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="49f49-115">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="49f49-116">BOM 明細行の詳細の追加</span><span class="sxs-lookup"><span data-stu-id="49f49-116">Add BOM line details</span></span>

1. <span data-ttu-id="49f49-117">**BOM 明細行の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="49f49-118">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="49f49-119">たとえば、品目 M0055 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="49f49-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="49f49-120">各 BOM 明細行プロパティに、固定値をとるか、属性にマップさせるかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="49f49-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="49f49-121">**設定** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="49f49-122">**計算** フィールドで、*はい* を選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="49f49-123">**計算** プロパティを *はい* にを設定すると、原価計算に BOM 明細行 が含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="49f49-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="49f49-124">**設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="49f49-125">**設定** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="49f49-126">**数量** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49f49-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="49f49-127">数量フィールドは、BOM に含まれる品目の数量を決定します。</span><span class="sxs-lookup"><span data-stu-id="49f49-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="49f49-128">これは、属性のマッピングの明確な候補になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="49f49-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="49f49-129">**分析コード** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="49f49-130">製品分析コードのいずれかが有効であるかどうかを確認します。したがって、値または属性が割り当て済である必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f49-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="49f49-131">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49f49-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]