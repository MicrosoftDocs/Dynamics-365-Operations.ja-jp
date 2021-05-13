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
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920534"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="0d6bb-103">販売価格の選択基準の作成</span><span class="sxs-lookup"><span data-stu-id="0d6bb-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d6bb-104">この手順では、属性ベースの販売価格モデルに対して販売価格の選択基準を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="0d6bb-105">この手順では、少なくとも 1 つの販売価格モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="0d6bb-106">この例では、デモ データの会社 USMF でスピーカー ソリューションの販売価格モデルに対して価格モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="0d6bb-107">通常、製品マネージャーがこの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="0d6bb-108">既存の販売価格モデルへの新しい条件の追加</span><span class="sxs-lookup"><span data-stu-id="0d6bb-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="0d6bb-109">**製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="0d6bb-110">一覧で、モデル名のリンクを選択せずに、スピーカー ソリューション製品モデルの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="0d6bb-111">アクション ウィンドウで、**モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="0d6bb-112">**価格モデル基準** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="0d6bb-113">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-113">Select **New**.</span></span>
1. <span data-ttu-id="0d6bb-114">**名前** フィールドに 「顧客グループ 10」 と入力します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="0d6bb-115">価格モデル基準の名前を使用すると、基礎の選択基準を特定する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="0d6bb-116">**価格モデル** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="0d6bb-117">**注文タイプ** フィールドで *販売注文* を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="0d6bb-118">注文タイプで、選択クエリで使用できるデータベース フィールドが決まります。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="0d6bb-119">**発効日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="0d6bb-120">**有効期限** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="0d6bb-121">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="0d6bb-122">選択基準のクエリの作成</span><span class="sxs-lookup"><span data-stu-id="0d6bb-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="0d6bb-123">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-123">Select **Edit**.</span></span>
2. <span data-ttu-id="0d6bb-124">**テーブル** フィールドで、*顧客* を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="0d6bb-125">**フィールド** フィールドで、*顧客グループ* を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="0d6bb-126">この例では、選択基準に特定の顧客グループを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="0d6bb-127">**基準** フィールドで、*顧客グループ 10* を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="0d6bb-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d6bb-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]