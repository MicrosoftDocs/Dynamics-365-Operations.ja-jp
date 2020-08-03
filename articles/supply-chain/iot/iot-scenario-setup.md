---
title: IoT インテリジェンスのシナリオ設定
description: このトピックでは、IoT インテリジェンスの Supply Chain Management のシナリオを構成する方法について説明します。
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597171"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="f46ad-103">IoT インテリジェンスのシナリオ設定</span><span class="sxs-lookup"><span data-stu-id="f46ad-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f46ad-104">このトピックでは、IoT インテリジェンスの Supply Chain Management のシナリオを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="f46ad-105">シナリオを設定する前に、[LCS を設定する](iot-lcs-setup.md)必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="f46ad-106">このトピックでは、マシンが停止した際に Supply Chain Management で通知を生成する、**装置のダウンタイム**のシナリオを構成します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="f46ad-107">Supply Chain Management における **装置のダウンタイム**シナリオの構成</span><span class="sxs-lookup"><span data-stu-id="f46ad-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="f46ad-108">**装置のダウンタイム** シナリオでは、パーツ アウト信号をマシンの警告しきい値にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="f46ad-109">シナリオでマシンが選択されていて、Supply Chain Management で動作するように設定されている場合にのみ、監視がされます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="f46ad-110">マシンが最後に受信したパーツ アウト信号からの時間が、警告のしきい値よりも大きい場合、**マシンの停止** 通知がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="f46ad-111">マシンがまだ動作している場合は、次の**パーツ アウト**信号を受け取ったときに、**マシンの起動**通知がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="f46ad-112">マシンが 30 分間停止した場合は、新たな **マシンの停止** 通知がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="f46ad-113">**装置のダウンタイム**のシナリオには、次のような依存関係があります:</span><span class="sxs-lookup"><span data-stu-id="f46ad-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="f46ad-114">警告をトリガーするには、マッピングされたマシンで製造オーダーを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="f46ad-115">マッピングされたマシンのパーツ アウト信号を表す信号は、一意のプロパティ名で IoT ハブに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="f46ad-116">IoT ハブ メッセージに Unix ミリタイム スタンプ プロパティが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="f46ad-117">このシナリオを構成するには、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="f46ad-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="f46ad-118">Supply Chain Management にログインします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="f46ad-119">IoT インテリジェンス機能のフラグを有効化します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="f46ad-120">詳細については [機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f46ad-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="f46ad-121">メトリックを構成します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-121">Configure the metrics.</span></span> <span data-ttu-id="f46ad-122">構成方法の詳細については、[メトリックの構成方法](iot-metrics-setup.md#configure-metrics)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f46ad-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="f46ad-123">**生産管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="f46ad-124">**設定 \> IoT インテリジェンス \> シナリオ管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="f46ad-125">**装置のダウンタイム**タイルで **構成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="f46ad-126">構成ウィザードで、**装置のセンサーのスキーマを定義する** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="f46ad-127">ここでは、IoT メッセージの JSON 形式に合わせて Supply Chain Management のスキーマを設定することです。</span><span class="sxs-lookup"><span data-stu-id="f46ad-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="f46ad-128">複数のメッセージ スキーマを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="f46ad-129">詳細については、[IoT ハブが使用するメッセージス キーマの形式](iot-schema-format.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f46ad-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="f46ad-130">この例では、メッセージ ペイロードに次の形式のメッセージがまとめて含まれています:</span><span class="sxs-lookup"><span data-stu-id="f46ad-130">In this example, the message payload contains a batch of messages with this format:</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="f46ad-131">テーブルに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="f46ad-132">**スキーマ名称**に **ID** を設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="f46ad-133">**スキーマのパス** に **/payload[\*]/id** を設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="f46ad-134">**メッセージ ID** に**説明**を設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="f46ad-135">テーブルに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="f46ad-136">**スキーマ名称**に **タイムスタンプ** を設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="f46ad-137">**スキーマのパス** に **/payload[\*]/timestamp** を設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="f46ad-138">**メッセージのタイムスタンプ** に**説明**を設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="f46ad-139">テーブルに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="f46ad-140">**スキーマ名称**に **値** を設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="f46ad-141">**スキーマのパス** に **/payload[\*]/value** を設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="f46ad-142">**メッセージの値** に**説明**を設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="f46ad-143">メッセージ内のすべてのプロパティを定義する必要はありません。必要なものだけを定義してください。</span><span class="sxs-lookup"><span data-stu-id="f46ad-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="f46ad-144">この例では、**ルート タイムスタンプ**の行を作成していません。</span><span class="sxs-lookup"><span data-stu-id="f46ad-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="f46ad-145">**ルート タイムスタンプ**のパスは **/timestamp** です。</span><span class="sxs-lookup"><span data-stu-id="f46ad-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="f46ad-146">**次へ** をクリックして、 **装置センサーのスキーマ マッピング** ページに移動し ます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="f46ad-147">**装置リソース ID** の行で、**スキーマ名称** を **ID** に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="f46ad-148">有効な値が、ドロップダウン テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="f46ad-149">**UTC 時間**の行で、**スキーマ名称**を **Timestamp** に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="f46ad-150">有効な値が、ドロップダウン テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="f46ad-151">**パーツ生成信号** の行で、**スキーマ名称** を **値** に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="f46ad-152">有効な値が、ドロップダウン テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="f46ad-153">**装置リソース ID の構成** ページで **次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="f46ad-154">このステップでは、IoT ハブ メッセージの値を Supply Chain Management のリソースにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="f46ad-155">**信号データ値の値** テーブルで、新たな行を追加し、**値**に **IoTInt.Machine1225.PartOut** を入力します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="f46ad-156">**IoTInt.Machine1225.PartOut** の値は、IoT ハブ メッセージの JSON **id**プロパティから取得されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="f46ad-157">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-157">Click **Save**.</span></span>
    3. <span data-ttu-id="f46ad-158">**業務レコードのマッピング**テーブルで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="f46ad-159">**業務レコード タイプ**の既定値は自動入力されるため、変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f46ad-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="f46ad-160">**業務レコード**列で、この信号の値を送信する Supple Chain Management マシンのリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="f46ad-161">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-161">Click **Save**.</span></span>
    6. <span data-ttu-id="f46ad-162">**Machine1226**に新たな業務レコード マッピングを追加し、これらの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="f46ad-163">Supply Chain Management では、複数の信号データの値を 1 つのレコードにマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="f46ad-164">処理するマシンを選択するには、**選択済** 列を使用します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="f46ad-165">すべての信号の値を定義する必要はなく、すべてのマシンを選択する必要もありません。</span><span class="sxs-lookup"><span data-stu-id="f46ad-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="f46ad-166">**次へ**をクリックし て、**パーツ生成信号の構成**ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="f46ad-167">**信号データ値** テーブルで、行を追加し、**値**を **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="f46ad-168">**True** の値は、IoT ハブ メッセージの JSON **値**プロパティから取得されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="f46ad-169">シナリオに必要な数だけ値を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="f46ad-170">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-170">Click **Save**.</span></span>
20. <span data-ttu-id="f46ad-171">**次へ** をクリックして、 **装置ダウンタイムのしきい値** ページに移動し ます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="f46ad-172">一覧に表示されているマシンは、既に信号の値にマッピングされているマシンです。</span><span class="sxs-lookup"><span data-stu-id="f46ad-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="f46ad-173">この手順では、マシンが停止しているかどうかを判断するしきい値を定義します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="f46ad-174">たとえば、しきい値を 10 に設定した場合、10分間マシンからメッセージが出ていない場合は Supply Chain Management が通知が生成します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="f46ad-175">**次へ** をクリックして **シナリオの有効化** ページに進みます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="f46ad-176">スライダーを切替えてシナリオを有効化します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="f46ad-177">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-177">Click **Finish**.</span></span>

<span data-ttu-id="f46ad-178">シナリオの設定が完了しました。</span><span class="sxs-lookup"><span data-stu-id="f46ad-178">The scenario setup is complete.</span></span> <span data-ttu-id="f46ad-179">IoT インテリジェンスでは、IoT ハブ メッセージの処理が自動的に開始されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="f46ad-180">Supply Chain Management における **製品の品質**シナリオの構成</span><span class="sxs-lookup"><span data-stu-id="f46ad-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="f46ad-181">**製品の品質**シナリオでは、品目の属性が指定された範囲外の場合に通知を生成します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="f46ad-182">たとえば、センサーで各品目の重量を IoT ハブに送信することができます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="f46ad-183">Supply Chain Management では、品目が重すぎる、または軽すぎる場合に通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="f46ad-184">このシナリオには、次のような依存関係があります:</span><span class="sxs-lookup"><span data-stu-id="f46ad-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="f46ad-185">警告を発生させるには、マッピングされたマシンで製造オーダーを実行し、マッピングされたバッチ属性を持つ製品を生産する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="f46ad-186">マッピングされたマシンのバッチ属を表す信号は、一意のプロパティ名で IoT ハブに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="f46ad-187">IoT ハブ メッセージに Unix ミリ秒のタイムスタンプ プロパティが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="f46ad-188">Supply Chain Management における **生産遅延**シナリオの構成</span><span class="sxs-lookup"><span data-stu-id="f46ad-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="f46ad-189">**生産遅延**シナリオでは、生産の処理能力がしきい値を下回った場合に通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="f46ad-190">このシナリオでは、生産されたアイテムごとに **パーツアウト** 信号が IoT ハブに送信されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="f46ad-191">Supply Chain Managementでは、注文の遅延は、製造オーダーの実行がスケジュールされている期間、生成される品目の数、ジョブの実行期間、受信した**パーツアウトt**信号の数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="f46ad-192">ジョブに対する **パーツアウト** 信号の数が想定されるしきい値を下回った場合に、遅延通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f46ad-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="f46ad-193">このシナリオには、次のような依存関係があります:</span><span class="sxs-lookup"><span data-stu-id="f46ad-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="f46ad-194">警告をトリガーするには、マッピングされたマシンで製造オーダーが実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="f46ad-195">マッピングされたマシンのパーツ アウト信号を表す信号は、一意のプロパティ名で IoT ハブに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="f46ad-196">IoT ハブ メッセージに Unix ミリ秒のタイムスタンプ プロパティが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46ad-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="f46ad-197">シナリオを無効にする方法</span><span class="sxs-lookup"><span data-stu-id="f46ad-197">How to disable a scenario</span></span>

<span data-ttu-id="f46ad-198">次の手順に従い、シナリオを無効化します:</span><span class="sxs-lookup"><span data-stu-id="f46ad-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="f46ad-199">Supply Chain Management で、**生産管理 \> 設定 \> IoT インテリジェンス \> シナリオ管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="f46ad-200">シナリオの **構成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f46ad-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="f46ad-201">**次へ** をクリックし て、最後のウィザード タブを表示します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="f46ad-202">スライダーを切替えてシナリオを無効化します。</span><span class="sxs-lookup"><span data-stu-id="f46ad-202">Toggle the slider to disable the scenario.</span></span>
