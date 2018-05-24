---
title: "補充設定"
description: "マスタ スケジューリングでは補充設定を使用して在庫品目要求を計算します。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 858328ec60e0ffa5ca46a98b365fb0fc599ae1f0
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="coverage-settings"></a><span data-ttu-id="a6818-103">補充設定</span><span class="sxs-lookup"><span data-stu-id="a6818-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6818-104">マスタ スケジューリングでは補充設定を使用して在庫品目要求を計算します。</span><span class="sxs-lookup"><span data-stu-id="a6818-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="a6818-105">補充設定は次のように複数の方法で指定できます。</span><span class="sxs-lookup"><span data-stu-id="a6818-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="a6818-106">補充グループの補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6818-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="a6818-107">リンク先のすべての製品の設定を含む補充グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6818-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="a6818-108">補充グループを作成するには、**マスター プラン &gt; 設定 &gt; 補充 &gt; 補充グループ**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6818-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="a6818-109">補充グループは製品にリンクできます。</span><span class="sxs-lookup"><span data-stu-id="a6818-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="a6818-110">サイト、倉庫、製品分析コードに固有のリンクの場合、**品目の補充**ページで**補充グループ**のフィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6818-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="a6818-111">製品分析コードに関係なく、一般のリンクの場合は、**製品の詳細**ページの**計画**クイック タブの**補充グループ**を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6818-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="a6818-112">補充グループを製品にリンクしない場合は、マスター プランでは**マスター プランのパラメーター**ページで指定された**一般補充グループ**が既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6818-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="a6818-113">製品の補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6818-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="a6818-114">特定の製品の補充設定を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6818-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="a6818-115">**製品情報管理 &gt; 製品 &gt; リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6818-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="a6818-116">製品を選択し、**アクション ペイン**、**計画**タブ、**補充グループ**、**品目補充**の順にクリックして**品目補充**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a6818-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="a6818-117">製品が補充グループにすでにリンクされている場合、**上書き**フィールドで設定した補充グループの設定は無視できます。</span><span class="sxs-lookup"><span data-stu-id="a6818-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="a6818-118">**品目の補充**ページの補充設定は、**補充グループ** ページの設定より優先されます。</span><span class="sxs-lookup"><span data-stu-id="a6818-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="a6818-119">ウィザードで製品の補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6818-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="a6818-120">ウィザードは、基本的な品目補充パラメーターを着実に設定するお手伝いをするガイドです。</span><span class="sxs-lookup"><span data-stu-id="a6818-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="a6818-121">**品目の補充**ページで、**ウィザード**をクリックして**品目補充ウィザード**を開きます。</span><span class="sxs-lookup"><span data-stu-id="a6818-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="a6818-122">分析コード グループの補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6818-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="a6818-123">**製品情報管理 &gt; 共通 &gt; リリースされた製品** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6818-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="a6818-124">**管理**グループの、**一般**タブにおける、**リリース済製品の詳細**ページで、**保管分析コード グループ**リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6818-124">On the **Released product detail** page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="a6818-125">**保管分析コード グループ** ページで**分析コード別補充計画**フィールドを選択して、保管分析コード グループの分析コードについて補充設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="a6818-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="a6818-126">コンフィギュレーション、色、サイズ、スタイルなどすべての製品分析コードで、**分析コード別補充計画**フィールドを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6818-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="additional-resources"></a><span data-ttu-id="a6818-127">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="a6818-127">Additional resources</span></span>
--------

[<span data-ttu-id="a6818-128">マスター プラン</span><span class="sxs-lookup"><span data-stu-id="a6818-128">Master plans</span></span>](master-plans.md)




