---
title: 資産カウンターの手動更新
description: このトピックでは、資産管理での資産カウンターの手動更新について説明します。
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4618ff2d6880f478683fbed0ed716af5ab8d4d9c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842252"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="04a73-103">資産カウンターの手動更新</span><span class="sxs-lookup"><span data-stu-id="04a73-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="04a73-104">カウンターは、資産が処理された時間数や生産された量に関する登録など、資産の登録を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="04a73-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="04a73-105">カウンターに対して選択されたカウンター タイプは、カウンター値を継承するように設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="04a73-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="04a73-106">つまり、**カウンター** ページの **一般** クイック タブで **資産のカウンター値の継承** オプションが **はい** に設定されている場合 (**資産管理** > **設定** > **資産のタイプ** > **カウンター**)。</span><span class="sxs-lookup"><span data-stu-id="04a73-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="04a73-107">この場合、そのタイプの新しいカウンター明細行を作成すると、同じカウンター タイプを使用するすべての子アセットが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="04a73-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="04a73-108">**全資産** ページで、資産の測定値に基づき、資産に対する時間または数量のカウンター登録を作成します。</span><span class="sxs-lookup"><span data-stu-id="04a73-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="04a73-109">**資産管理** >  **共通** >  **資産** > **全資産** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="04a73-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="04a73-110">資産を選択してから、アクション ペインの、**資産** タブの、**予防的** グループで、**カウンター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="04a73-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="04a73-111">**資産カウンター** ページに、選択した資産に対して行われた以前のカウンター登録のすべてのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="04a73-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="04a73-112">**新規** を選択して、登録を作成します。</span><span class="sxs-lookup"><span data-stu-id="04a73-112">Select **New** to create a registration.</span></span> <span data-ttu-id="04a73-113">資産 ID は **資産** フィールドに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="04a73-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="04a73-114">**カウンター** フィールドで、関連するカウンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="04a73-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="04a73-115">資産で選択された資産タイプに関連するカウンターのみを選択できます。</span><span class="sxs-lookup"><span data-stu-id="04a73-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="04a73-116">関連する単位が **単位** フィールドに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="04a73-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="04a73-117">**登録済** フィールドで、カウンター登録の日時を選択します。</span><span class="sxs-lookup"><span data-stu-id="04a73-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="04a73-118">**値** フィールドに、最後のカウンター登録以降の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04a73-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="04a73-119">または、**集計値** フィールドに、合計カウント数を入力します。</span><span class="sxs-lookup"><span data-stu-id="04a73-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="04a73-120">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="04a73-120">Note the following points:</span></span>

- <span data-ttu-id="04a73-121">資産に新しいカウンターを物理的にインストールする場合、**資産カウンター** ページで、資産の変更を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04a73-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="04a73-122">次に、同じタイムスタンプを持つ 2 つの登録明細行を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04a73-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="04a73-123">最初の行は、置換しているカウンター用である必要があります。</span><span class="sxs-lookup"><span data-stu-id="04a73-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="04a73-124">新しいカウンターに関連付けられている行で、**カウンター リセット** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="04a73-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="04a73-125">**合計** フィールドで、合計カウント数は、カウンター タイプに登録されているすべての値のカウンターの合計になります。</span><span class="sxs-lookup"><span data-stu-id="04a73-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="04a73-126">「以降」または「到達」の間隔タイプを持つメンテナンス計画を使用している資産で **カウンター リセット** チェック ボックスがオンになっている場合、別のカウンター明細行を作成し、新しいカウンターでやり直すため、カウンターは新しいカウンター明細行でもまだ有効です。</span><span class="sxs-lookup"><span data-stu-id="04a73-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="04a73-127">次の図は、**資産カウンター** ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="04a73-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![図 1](media/11-work-orders.png)

<span data-ttu-id="04a73-129">**資産カウンター** ページ (**資産管理** > **照会** > **資産** > **資産カウンター**) では、必要に応じて、複数の資産に対して同時にカウンター登録を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="04a73-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="04a73-130">手動のカウンター登録に対する差異を定義する範囲を設定できます。</span><span class="sxs-lookup"><span data-stu-id="04a73-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="04a73-131">登録が定義された範囲に含まれていない場合に表示されるメッセージのタイプを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="04a73-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="04a73-132">カウンターの設定方法の詳細については、[カウンター](../setup-for-objects/counters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04a73-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]