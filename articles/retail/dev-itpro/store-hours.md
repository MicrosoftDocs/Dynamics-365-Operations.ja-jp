---
title: 店舗の営業時間の作成と更新
description: このトピックでは、Retail Headquarters で営業時間を作成および更新する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 1b55b91246b22951f4e1d148f59444423e1d8a3d
ms.sourcegitcommit: e54607a2c80bec4db05045825914f50947f6e31e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1917515"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="45332-103">店舗の営業時間の作成と更新</span><span class="sxs-lookup"><span data-stu-id="45332-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="45332-104">概要</span><span class="sxs-lookup"><span data-stu-id="45332-104">Overview</span></span>

<span data-ttu-id="45332-105">小売業者は 1 つの場所から、複数の地域にまたがるさまざまな店舗の営業時間を作成、維持、および管理することができます。</span><span class="sxs-lookup"><span data-stu-id="45332-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="45332-106">店舗の営業時間は、販売時点管理 (POS) ターミナルに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="45332-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="45332-107">これにより、レジ担当者は、店舗の営業時間を顧客と共有し、他の店舗の在庫に関心を持つ買い物客をよりよくサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="45332-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="45332-108">顧客が後で店舗に戻りたい場合に備えて、店舗の営業時間をレシートに印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="45332-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="45332-109">異なるチャネル間で、複数の店舗の営業時間をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="45332-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="45332-110">これらチャネルには、従来型の店舗、コール センター、モバイル デバイス、および電子商取引サイトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="45332-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="45332-111">顧客が別の店舗の集荷注文を持っている場合、レジ担当者はその店舗で集荷できる日付を選択できます。</span><span class="sxs-lookup"><span data-stu-id="45332-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="45332-112">店舗ルックアップでは、日付と店舗の営業時間を参照できます。</span><span class="sxs-lookup"><span data-stu-id="45332-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="45332-113">レジ担当者は日付と場所を選択でき、店舗の営業時間を含む集荷受入を印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="45332-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="45332-114">この機能は、Microsoft Dynamics 365 for Retail バージョン 8.1.2 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="45332-114">This functionality is available in Microsoft Dynamics 365 for Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="45332-115">店舗の営業時間のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="45332-115">Configure store hours</span></span>

<span data-ttu-id="45332-116">店舗の営業時間をコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="45332-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="45332-117">**小売** \> **チャネル設定** \> **店舗の営業時間**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="45332-117">Go to **Retail** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="45332-118">**新規**を選択して、新しい店舗営業時間のテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="45332-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="45332-119">既存のテンプレートを使用するには、左ウィンドウでテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="45332-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="45332-120">**範囲の追加**ダイアログ ボックスで、日付範囲、店舗の営業時間、および必要な休日を定義します。</span><span class="sxs-lookup"><span data-stu-id="45332-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="45332-121">店舗の営業時間が変更されない場合は、**終了日**フィールドで**終了しない**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45332-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="45332-122">店舗の営業時間が特定の月、週、または日に限定される場合は、**開始日**フィールドと**終了日**フィールドに適切な日付を設定します。</span><span class="sxs-lookup"><span data-stu-id="45332-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="45332-123">開始日と終了日が重複する複数のテンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="45332-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="45332-124">したがって、たとえば、異なるタイム ゾーンの店舗の営業時間を定義できます。</span><span class="sxs-lookup"><span data-stu-id="45332-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="45332-125">![範囲の追加ダイアログ ボックス](../dev-itpro/media/Storehours1.png "範囲の追加ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="45332-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="45332-126">営業時間テンプレートを使用される店舗に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="45332-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="45332-127">**組織ノードの選択**ダイアログ ボックスで、テンプレートが関連付けられている店舗、地域、および組織を選択します。</span><span class="sxs-lookup"><span data-stu-id="45332-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="45332-128">各店舗に関連付けることができる店舗の営業時間のテンプレートは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="45332-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="45332-129">矢印ボタンを使用して、店舗、地域、または組織を選択します。</span><span class="sxs-lookup"><span data-stu-id="45332-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="45332-130">カレンダーは店舗または店舗グループで使用でき、POS で参照できるように表示されます。</span><span class="sxs-lookup"><span data-stu-id="45332-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="45332-131">![組織ノード ダイアログ ボックスの選択](../dev-itpro/media/Storehours2.png "組織ノード ダイアログ ボックスの選択")</span><span class="sxs-lookup"><span data-stu-id="45332-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="45332-132">**配送スケジュール** ページで **1070** および **1090** のジョブを実行して、POS で店舗の営業時間を使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="45332-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="45332-133">印刷されたレシートに店舗の営業時間を追加する</span><span class="sxs-lookup"><span data-stu-id="45332-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="45332-134">印刷された POS のレシートに店舗の営業時間を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="45332-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="45332-135">入庫デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="45332-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="45332-136">右下隅の**フッター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45332-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="45332-137">**店舗の営業時間**要素を左ウィンドウからレシート テンプレートの下部のフッターにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="45332-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="45332-138">必要に応じて、**店舗の営業時間**要素の既定のラベルを編集できます。</span><span class="sxs-lookup"><span data-stu-id="45332-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="45332-139">レシートを保存し、入庫デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="45332-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="45332-140">**配送スケジュール** ページで、**1070** および **1090** のジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="45332-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="45332-141">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="45332-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="45332-142">販売を完了し、レシートの印刷を選択します。</span><span class="sxs-lookup"><span data-stu-id="45332-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="45332-143">POS レシートには、店舗の営業時間が含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="45332-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="45332-144">テンプレートに休日が含まれている場合は、レシートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="45332-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="45332-145">![レシート例](../dev-itpro/media/Storehours3.png "レシート例")</span><span class="sxs-lookup"><span data-stu-id="45332-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
