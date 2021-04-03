---
title: 資産メーカーとモデル
description: このトピックでは、資産管理で資産メーカーと関連モデルを設定する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cec4f644af4a087464635d9a7ca825eb354747eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259965"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="c6d47-103">資産メーカーとモデル</span><span class="sxs-lookup"><span data-stu-id="c6d47-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c6d47-104">このトピックでは、資産管理で資産メーカーと関連モデルを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="c6d47-105">モデルは、資産タイプに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="c6d47-106">製品 - モデルの関係を設定</span><span class="sxs-lookup"><span data-stu-id="c6d47-106">Set up product-model relations</span></span>

1. <span data-ttu-id="c6d47-107">**資産管理** \> **設定** \> **資産** \> **メーカーとモデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="c6d47-108">**新規** を選択して、新しい製品を作成します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="c6d47-109">**メーカー** フィールドに、資産メーカーの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="c6d47-110">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="c6d47-111">**モデル** クイック タブで、**追加** を選択して、資産メーカーに関連する資産モデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="c6d47-112">**モデル** フィールドに、資産モデルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="c6d47-113">**説明** フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="c6d47-114">**資産タイプ** フィールドで、メーカー モデルが関連する資産タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6d47-115">**資産タイプ** ルックアップで、資産タイプ、メーカー、およびモデルの関係を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="c6d47-116">詳細については、[資産タイプ](../setup-for-objects/object-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6d47-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="c6d47-117">**詳細** クイック タブ、**モデル** フィールドには、選択した資産メーカーで設定されている資産モデルの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="c6d47-118">**資産** フィールドには、選択したメーカーを使用している資産の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="c6d47-119">**資産** フィールドには、メーカー モデルを使用しているオブジェクトの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="c6d47-120">資産タイプは、資産メーカー モデルの関係を持たないことも、1 つの資産メーカー モデルに関連付けることも、複数の資産メーカー モデルに関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="c6d47-121">資産タイプが 1 つのメーカー モデルに関連している場合、**メーカー モデル** ルックアップで設定された組み合わせのみが、資産タイプ、メーカー、およびモデルの組み合わせを設定できる資産管理ページで選択できます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="c6d47-122">これらのページには、**全資産**、**資産サービス レベル**、**ジョブ タイプの既定値**、および **メンテナンス予算明細行** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="c6d47-123">一部の資産タイプがメーカー モデルに関連していない場合、それらの資産タイプ、および資産タイプとは関係のないメーカー モデルのみがページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="c6d47-124">オブジェクトのメーカーとモデルを選択</span><span class="sxs-lookup"><span data-stu-id="c6d47-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="c6d47-125">**資産管理** \> **共通** \> **資産** \> **全資産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="c6d47-126">**資産** 列で、資産のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="c6d47-127">**詳細** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6d47-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="c6d47-128">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-128">Select **Edit**.</span></span>
4. <span data-ttu-id="c6d47-129">**一般** クイック タブで、**メーカー** および **モデル** フィールドの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6d47-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]