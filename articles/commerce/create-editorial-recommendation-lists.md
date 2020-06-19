---
title: 収集された推奨事項の手動作成
description: このトピックでは、小売業者が Microsoft Dynamics 365 Commerce の顧客のために、製品リストを手動で作成および管理する方法を説明します。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b866704b419fb07dcf1ddd386af2f7d6cfa02e2
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404119"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="90ffb-103">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="90ffb-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="90ffb-104">このトピックでは、小売業者が Microsoft Dynamics 365 Commerce の顧客のために、製品の推奨リストを手動で作成および管理する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="90ffb-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="90ffb-105">キュレーション リストとは、ユーザーによって作成され、精選された、個々のコンテンツの集合のことです。</span><span class="sxs-lookup"><span data-stu-id="90ffb-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="90ffb-106">新しいリストの作成</span><span class="sxs-lookup"><span data-stu-id="90ffb-106">Create a new list</span></span>

<span data-ttu-id="90ffb-107">精選された製品推奨事項リストを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="90ffb-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="90ffb-108">**小売りとコマース &gt; 製品推奨事項 &gt; 推奨リスト**に移動します。</span><span class="sxs-lookup"><span data-stu-id="90ffb-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="90ffb-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90ffb-109">Select **New**.</span></span>
1. <span data-ttu-id="90ffb-110">**リスト ID** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="90ffb-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="90ffb-111">**リスト名**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="90ffb-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="90ffb-112">**リスト名**は、**製品収集**モジュールの精選されたリスト セクションに表示されるリストのタイトルです。</span><span class="sxs-lookup"><span data-stu-id="90ffb-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="90ffb-113">リストに製品を追加するには、**製品の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90ffb-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="90ffb-114">リスト上で製品の表示順を変えるには、**表示順**列に値を入力します。</span><span class="sxs-lookup"><span data-stu-id="90ffb-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="90ffb-115">2 つの製品が同じ表示順の値を持つ場合、それら 2 つの最終的な並び順は、バック オフィスとは異なることがあります。</span><span class="sxs-lookup"><span data-stu-id="90ffb-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="90ffb-116">**保存**を選択してリストを保存します。</span><span class="sxs-lookup"><span data-stu-id="90ffb-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="90ffb-117">リストの例</span><span class="sxs-lookup"><span data-stu-id="90ffb-117">Example List</span></span>

![バック オフィスのキュレーション リストの例](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="90ffb-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="90ffb-119">Additional resources</span></span>

[<span data-ttu-id="90ffb-120">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="90ffb-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="90ffb-121">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="90ffb-121">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="90ffb-122">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="90ffb-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="90ffb-123">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="90ffb-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="90ffb-124">カスタマイズされた製品推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="90ffb-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="90ffb-125">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="90ffb-125">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="90ffb-126">トランザクション画面への推奨設定の追加</span><span class="sxs-lookup"><span data-stu-id="90ffb-126">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="90ffb-127">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="90ffb-127">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="90ffb-128">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="90ffb-128">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="90ffb-129">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="90ffb-129">Product recommendations FAQ</span></span>](faq-recommendations.md)
