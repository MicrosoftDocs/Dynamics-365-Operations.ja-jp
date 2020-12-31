---
title: IoT インテリジェンスの指標の設定
description: このトピックでは、IoT インテリジェンスの指標を設定する方法について説明します。
author: robinarh
manager: tfehr
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d854923876e013cc53542d809f61901e997dc09f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409461"
---
# <a name="set-up-metrics-for-iot-intelligence"></a><span data-ttu-id="790b7-103">IoT インテリジェンスの指標の設定</span><span class="sxs-lookup"><span data-stu-id="790b7-103">Set up metrics for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a><span data-ttu-id="790b7-104">指標のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="790b7-104">Configure metrics</span></span>

<span data-ttu-id="790b7-105">Microsoft Dynamics 365 Supply Chain Management でメッセージのタイム シリーズ チャートを表示する場合は、次の手順に従って指標を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="790b7-105">If you want to view the time series charts of your messages in Microsoft Dynamics 365 Supply Chain Management, you must set up the metrics by following these steps.</span></span>

1. <span data-ttu-id="790b7-106">Redis キャッシュの接続文字列をコピーします:</span><span class="sxs-lookup"><span data-stu-id="790b7-106">Copy the connection string for the Redis cache:</span></span>

    1. <span data-ttu-id="790b7-107">Azure portal で、Redis キャッシュに移動します。</span><span class="sxs-lookup"><span data-stu-id="790b7-107">In the Azure portal, go to the Redis cache.</span></span>
    2. <span data-ttu-id="790b7-108">**設定** \> **アクセス キー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="790b7-108">Go to **Settings** \> **Access keys**.</span></span>
    3. <span data-ttu-id="790b7-109">**ライマリ接続文字列** フィールドの値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="790b7-109">Copy the value in the **Primary connection string** field.</span></span>

2. <span data-ttu-id="790b7-110">Supply Chain Management では、**生産管理 \> 設定 \> IoT インテリジェンス \> シナリオ パラメータ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="790b7-110">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario parameters**.</span></span>
3. <span data-ttu-id="790b7-111">**シナリオ パラメータ** ページの **タイム シリーズ** タブの **Redis メトリック ストア接続文字列** フィールドに、前の手順でコピーした接続文字列を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="790b7-111">On the **Scenario parameters** page, on the **Time series** tab, in the **Redis metric store connection string** field, paste the connection string that you copied earlier.</span></span> <span data-ttu-id="790b7-112">この手順により、Azure IoT Hub からの指標を Supply Chain Management で視覚化できます。</span><span class="sxs-lookup"><span data-stu-id="790b7-112">This step enables the metrics from Azure IoT Hub to be visualized in Supply Chain Management.</span></span> <span data-ttu-id="790b7-113">フィールドに値を貼り付けると、**\*\*\*\*\*\*** と表示されます。</span><span class="sxs-lookup"><span data-stu-id="790b7-113">When you paste the value into the field, it's shown as **\*\*\*\*\*\***.</span></span>

    > [!NOTE]
    > <span data-ttu-id="790b7-114">Redis キャッシュ接続文字列を更新する場合はいつでも、このフィールドも更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="790b7-114">Whenever you update the Redis cache connection string, you must also update this field.</span></span>

4. <span data-ttu-id="790b7-115">**生産管理 \> 照会とレポート \> IoT インテリジェンス \> 指標キー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="790b7-115">Go to **Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys**.</span></span>
5. <span data-ttu-id="790b7-116">**指標キー** ページで、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-116">On the **Metric keys** page, select **Update**.</span></span>
6. <span data-ttu-id="790b7-117">**指標キーの更新** ダイアログ ボックスで、フィールドで **バックグラウンドで実行** が選択されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="790b7-117">In the **Update metric keys** dialog box, notice that **Run in the background** is selected in the field.</span></span> <span data-ttu-id="790b7-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-118">Select **OK**.</span></span>

<span data-ttu-id="790b7-119">Redis キャッシュ内のすべての指標キーが取得され、**指標キー** 一覧に追加されます。</span><span class="sxs-lookup"><span data-stu-id="790b7-119">All the metric keys in the Redis cache are retrieved and added to the **Metric keys** list.</span></span> <span data-ttu-id="790b7-120">指標値は、[シナリオを有効にする](iot-scenario-setup.md) まで表示されません。</span><span class="sxs-lookup"><span data-stu-id="790b7-120">Metric values won't appear until you [enable the scenarios](iot-scenario-setup.md).</span></span>

## <a name="configure-the-resource-status-time-series"></a><span data-ttu-id="790b7-121">リソース ステータス タイム シリーズのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="790b7-121">Configure the Resource Status time series</span></span>

<span data-ttu-id="790b7-122">**リソース ステータス** タイム シリーズをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="790b7-122">To configure the **Resource Status** time series, follow these steps.</span></span>

1. <span data-ttu-id="790b7-123">Supply Chain Management で、**生産管理 \> 製造実行 \> リソース ステータス** に移動します。</span><span class="sxs-lookup"><span data-stu-id="790b7-123">In Supply Chain Management, go to **Production control \> Manufacturing execution \> Resource Status**.</span></span>
2. <span data-ttu-id="790b7-124">**リソース ステータス** ページで、**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-124">On the **Resource status** page, select **Configure**.</span></span>
2. <span data-ttu-id="790b7-125">**コンフィギュレーション** ダイアログ ボックスの **リソース** 一覧で、監視する項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-125">In the **Configure** dialog box, in the **Resource** list, select an item to monitor.</span></span>
3. <span data-ttu-id="790b7-126">**タイム シリーズ 1** の **編集** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-126">Select the **Edit** button for **Time series 1**.</span></span>
4. <span data-ttu-id="790b7-127">**タイム シリーズの選択** ダイアログ ボックスで、グリッドの指標を選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-127">In the **Select time series** dialog box, select a metric in the grid.</span></span> <span data-ttu-id="790b7-128">(**指標キーの更新** リンクを使用して、このダイアログ ボックスから指標キーを更新します。)</span><span class="sxs-lookup"><span data-stu-id="790b7-128">(You can also use the **Update metric keys** link to update the metric keys from this dialog box.)</span></span>
5. <span data-ttu-id="790b7-129">**OK** を選択し て、**コンフィギュレーション** ダイアログ ボックスに戻ります。</span><span class="sxs-lookup"><span data-stu-id="790b7-129">Select **OK** to return to the **Configure** dialog box.</span></span>
6. <span data-ttu-id="790b7-130">表示名を入力します。</span><span class="sxs-lookup"><span data-stu-id="790b7-130">Enter a display name.</span></span>
7. <span data-ttu-id="790b7-131">**データの表示元** フィールドで、タイム フレームを選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-131">In the **Show data from** field, select a time frame.</span></span>
8. <span data-ttu-id="790b7-132">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-132">Select **OK**.</span></span>

<span data-ttu-id="790b7-133">グラフが表示されます。</span><span class="sxs-lookup"><span data-stu-id="790b7-133">The chart is shown.</span></span>

## <a name="delete-a-metric-key"></a><span data-ttu-id="790b7-134">指標キーの削除</span><span class="sxs-lookup"><span data-stu-id="790b7-134">Delete a metric key</span></span>

1. <span data-ttu-id="790b7-135">Supply Chain Management で、**生産管理 \> 照会とレポート \> IoT インテリジェンス \> 指標キー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="790b7-135">In Supply Chain Management, go to **Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys**.</span></span>
2. <span data-ttu-id="790b7-136">**指標キー** ページで、削除する指標キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-136">On the **Metric keys** page, select the metric key to delete.</span></span>
3. <span data-ttu-id="790b7-137">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="790b7-137">Select **Delete**.</span></span>
