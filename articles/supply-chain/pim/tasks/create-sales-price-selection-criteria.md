---
title: 販売価格の選択基準の作成
description: この手順では、属性ベースの販売価格モデルに対して販売価格の選択基準を作成する方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a616dcfdd755efc9bf0473e9239acb9127f11f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818160"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="a02e1-103">販売価格の選択基準の作成</span><span class="sxs-lookup"><span data-stu-id="a02e1-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a02e1-104">この手順では、属性ベースの販売価格モデルに対して販売価格の選択基準を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="a02e1-105">この手順では、少なくとも 1 つの販売価格モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="a02e1-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="a02e1-106">この例では、デモ データの会社 USMF でスピーカー ソリューションの販売価格モデルに対して価格モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="a02e1-107">通常、製品マネージャーがこの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="a02e1-108">既存の販売価格モデルへの新しい条件の追加</span><span class="sxs-lookup"><span data-stu-id="a02e1-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="a02e1-109">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a02e1-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a02e1-110">[製品コンフィギュレーション モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a02e1-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="a02e1-111">リストにて、モデル名のリンクをクリックせずに、スピーカー ソリューション製品モデルの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="a02e1-112">[アクション] ウィンドウで、[モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a02e1-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="a02e1-113">[価格モデル基準] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a02e1-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="a02e1-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a02e1-114">Click New.</span></span>
7. <span data-ttu-id="a02e1-115">[名前] フィールドに 「顧客グループ 10」 と入力します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="a02e1-116">価格モデル基準の名前を使用すると、基礎の選択基準を特定する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a02e1-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="a02e1-117">[価格モデル] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="a02e1-118">[注文タイプ] フィールドで [販売注文] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="a02e1-119">注文タイプで、選択クエリで使用できるデータベース フィールドが決まります。</span><span class="sxs-lookup"><span data-stu-id="a02e1-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="a02e1-120">[発効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="a02e1-121">[有効期限] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="a02e1-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a02e1-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="a02e1-123">選択基準のクエリの作成</span><span class="sxs-lookup"><span data-stu-id="a02e1-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="a02e1-124">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a02e1-124">Click Edit.</span></span>
2. <span data-ttu-id="a02e1-125">[テーブル] フィールドで、[顧客] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="a02e1-126">[フィールド] フィールドで、[顧客グループ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="a02e1-127">この例では、選択基準に特定の顧客グループを使用します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="a02e1-128">[基準] フィールドで、[顧客グループ 10] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a02e1-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="a02e1-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a02e1-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]