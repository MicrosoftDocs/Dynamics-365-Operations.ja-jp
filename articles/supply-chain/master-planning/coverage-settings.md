---
title: 補充設定
description: このトピックでは、在庫品目要求の計算にマスター スケジューリングが使用する補充設定について説明します。
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538897"
---
# <a name="coverage-settings"></a><span data-ttu-id="ef954-103">補充設定</span><span class="sxs-lookup"><span data-stu-id="ef954-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef954-104">マスタ スケジューリングでは補充設定を使用して在庫品目要求を計算します。</span><span class="sxs-lookup"><span data-stu-id="ef954-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="ef954-105">補充設定は次のように複数の方法で指定できます。</span><span class="sxs-lookup"><span data-stu-id="ef954-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="ef954-106">補充グループの補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="ef954-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="ef954-107">リンク先のすべての製品の設定を含む補充グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="ef954-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="ef954-108">補充グループを作成するには、**マスター プラン &gt; 設定 &gt; 補充 &gt; 補充グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef954-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="ef954-109">補充グループは製品にリンクできます。</span><span class="sxs-lookup"><span data-stu-id="ef954-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="ef954-110">サイト、倉庫、製品分析コードに固有のリンクの場合、**品目の補充**ページで**補充グループ**のフィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ef954-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="ef954-111">一般のリンクの場合は、製品分析コードに関係なく**製品の詳細**ページの**計画**クイック タブの**補充グループ** フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ef954-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="ef954-112">既定では、補充グループを製品にリンクしない場合は、マスター プランでは**マスター プランのパラメーター**で指定された一般補充グループが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ef954-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="ef954-113">製品の補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="ef954-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="ef954-114">特定の製品の補充設定を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ef954-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="ef954-115">**製品管理情報 &gt; 製品 &gt; リリースされた製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef954-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="ef954-116">製品を選択し、アクション ペイン、**計画**タブ、**補充**グループで、**品目補充**を選択し、**品目補充**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="ef954-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="ef954-117">製品が補充グループにすでにリンクされている場合、**上書き**フィールドで設定した補充グループの設定は無視できます。</span><span class="sxs-lookup"><span data-stu-id="ef954-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="ef954-118">**品目の補充**ページの補充設定は、**補充グループ** ページの設定より優先されます。</span><span class="sxs-lookup"><span data-stu-id="ef954-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="ef954-119">ウィザードで製品の補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="ef954-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="ef954-120">ウィザードでは、主要な品目補充パラメータを設定する手順を順を追って説明します。</span><span class="sxs-lookup"><span data-stu-id="ef954-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="ef954-121">**品目の補充**ページのアクション ペインで**ウィザード**を選択して**品目補充ウィザード**を開きます。</span><span class="sxs-lookup"><span data-stu-id="ef954-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="ef954-122">分析コード グループの補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="ef954-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="ef954-123">**製品管理情報 &gt; 製品 &gt; リリースされた製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef954-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="ef954-124">**管理**セクションの、**一般**クイック タブにおける、**リリース済製品の詳細**ページで、**保管分析コード グループ** フィールドのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef954-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="ef954-125">**保管分析コード グループ** ページで**分析コード別補充計画**チェック ボックスを選択して、保管分析コード グループの分析コードについて補充設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="ef954-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="ef954-126">コンフィギュレーション、色、サイズ、スタイルなどすべての製品分析コードで、**分析コード別補充計画**フィールドを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef954-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef954-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ef954-127">Additional resources</span></span>

[<span data-ttu-id="ef954-128">マスター プラン</span><span class="sxs-lookup"><span data-stu-id="ef954-128">Master plans</span></span>](master-plans.md)
