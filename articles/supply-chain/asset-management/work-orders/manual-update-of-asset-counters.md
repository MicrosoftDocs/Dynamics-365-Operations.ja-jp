---
title: 資産カウンターの手動更新
description: このトピックでは、資産管理での資産カウンターの手動更新について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875758"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="b6a5b-103">資産カウンターの手動更新</span><span class="sxs-lookup"><span data-stu-id="b6a5b-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="b6a5b-104">カウンターは、工程の時間数や生産される数量などに関する資産の登録を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="b6a5b-105">カウンターに対して選択されたカウンター タイプがカウンターの値を継承するよう設定されている場合 (**資産管理** > **設定** > **資産タイプ** > **カウンター** > **一般**クイック タブ > **資産カウンターの値を継承する**トグルボタンが「オン」に設定されている)、そのタイプの新しいカウンター明細行を作成する時、同じカウンター タイプを使用するすべての子資産が自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="b6a5b-106">**全資産**で、資産の測定に基づき、資産に対する時間または数量のカウンターの登録を作成します。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="b6a5b-107">**資産管理**  >  **共通**  >  **資産**  >  **全資産**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="b6a5b-108">リストから資産を選択し、**カウンター**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="b6a5b-109">**資産カウンター** フォームで、選択した資産について以前の登録カウンターすべてのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="b6a5b-110">**新規** をクリックして、新しい登録を作成します。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="b6a5b-111">資産 ID が自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="b6a5b-112">**カウンター** フィールドで、関連するカウンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="b6a5b-113">資産で選択された資産タイプに関連するカウンターのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="b6a5b-114">関連する単位が**単位**フィールドに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="b6a5b-115">カウンター登録の日時を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="b6a5b-116">**値**フィールドに前回のカウンター登録からの数値を挿入するか、**集計値**フィールドに合計カウント数を挿入します。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="b6a5b-117">資産に新しいカウンターを物理的にインストールする場合、**資産カウンター**の資産に変更を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="b6a5b-118">次に、同一のタイムスタンプを持つ 2 つの登録明細行を作成し、新しいカウンターに関する明細行で、**カウンター リセット** チェック ボックスをオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="b6a5b-119">2 つの登録明細行を作成する場合、最初の明細行は置換するカウンターに対するものである必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="b6a5b-120">**合計**フィールドにおいて、合計カウント数は、カウンター タイプに登録されているすべての値のカウンター合計になります。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="b6a5b-121">「以降」または「到達」の間隔タイプを持つメンテナンス計画を使用している資産で**カウンター リセット** チェック ボックスがオンになっている場合、別のカウンター明細行を作成し、新しいカウンターでやり直すため、カウンターは新しいカウンター明細行でもまだ有効です。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![図 1](media/11-work-orders.png)


<span data-ttu-id="b6a5b-123">複数の資産のカウンター登録を行う必要がある場合、**資産管理** > **照会** > **資産** > **資産カウンター**で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="b6a5b-124">手動のカウンター登録の誤差を定義する範囲を設定したり、登録が定義された範囲外にある場合に表示されるメッセージ タイプを設定したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="b6a5b-125">カウンターの設定については、[カウンター](../setup-for-objects/counters.md) のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6a5b-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
