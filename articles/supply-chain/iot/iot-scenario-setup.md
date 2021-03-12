---
title: IoT インテリジェンスのシナリオ設定
description: このトピックでは、IoT インテリジェンスのシナリオを Microsoft Dynamics 365 Supply Chain Management でコンフィギュレーションする方法について説明します。
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 91deb080121d50794e6ff6fe79f9ca876b76deb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005255"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="2595f-103">IoT インテリジェンスのシナリオ設定</span><span class="sxs-lookup"><span data-stu-id="2595f-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2595f-104">このトピックでは、IoT インテリジェンスのシナリオを Microsoft Dynamics 365 Supply Chain Management でコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2595f-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2595f-105">シナリオを設定する前に、[Microsoft Dynamics Lifecycle Services (LCS) の設定](iot-lcs-setup.md) おこなう必要があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="2595f-106">このトピックでは、マシンが停止した際に Supply Chain Management で通知を生成するように、**装置のダウンタイム** のシナリオを構成します。</span><span class="sxs-lookup"><span data-stu-id="2595f-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="2595f-107">このトピックでは、品目の属性が指定された範囲外である場合に通知が生成されるように、**製品品質** シナリオをコンフィギュレーションする方法、および生産スループットがしきい値を下回った場合に通知を生成するように **生産遅延** シナリオをコンフィギュレーションする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="2595f-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="2595f-108">Supply Chain Management における 装置のダウンタイムシナリオの構成</span><span class="sxs-lookup"><span data-stu-id="2595f-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="2595f-109">**装置のダウンタイム** シナリオでは、**PartOut** 信号をマシンの警告しきい値にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="2595f-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="2595f-110">シナリオに対してマシンが選択されていて、Supply Chain Management で **動作** するように設定されている場合にのみ、監視がされます。</span><span class="sxs-lookup"><span data-stu-id="2595f-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="2595f-111">マシンから最後に受信した **PartOut** 信号からの時間が、警告のしきい値よりも大きい場合、**マシンの停止** 通知がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="2595f-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="2595f-112">マシンがまだ動作している場合は、次の **パーツ アウト** 信号を受け取ったときに、**マシンの起動** 通知がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="2595f-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="2595f-113">マシンが 30 分間停止した場合は、新たな **マシンの停止** 通知がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="2595f-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="2595f-114">**装置のダウンタイム** シナリオには、次のような依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="2595f-115">警告をトリガーするには、マッピングされたマシンで製造オーダーが実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="2595f-116">マッピングされたマシンの **PartOut** 信号を表す信号は、一意のプロパティ名で IoT ハブに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="2595f-117">この値がミリ秒単位で表される UNIX **タイムスタンプ** プロパティ (ms) は、Azure IoT ハブ メッセージに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="2595f-118">このシナリオを構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2595f-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="2595f-119">Supply Chain Management にサインインします。</span><span class="sxs-lookup"><span data-stu-id="2595f-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="2595f-120">IoT インテリジェンス機能のフラグを有効化します。</span><span class="sxs-lookup"><span data-stu-id="2595f-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="2595f-121">詳細については [機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2595f-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="2595f-122">メトリックを構成します。</span><span class="sxs-lookup"><span data-stu-id="2595f-122">Configure the metrics.</span></span> <span data-ttu-id="2595f-123">構成方法の詳細については、[メトリックの構成方法](iot-metrics-setup.md#configure-metrics)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2595f-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="2595f-124">**生産管理 \> 設定 \> IoT インテリジェンス \> シナリオ管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2595f-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="2595f-125">**装置のダウンタイムタイル** タイルで、**コンフィギュレーション** を選択して、コンフィギュレーション ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="2595f-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="2595f-126">ウィザードの最初のページは、**装置のセンサーのスキーマ定義** ページです。</span><span class="sxs-lookup"><span data-stu-id="2595f-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="2595f-127">このページでは、Supply Chain Management のスキーマを設定して、IoT Hub メッセージの JavaScript Object Notation (JSON) 形式と一致させることを目標としています。</span><span class="sxs-lookup"><span data-stu-id="2595f-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="2595f-128">複数のメッセージ スキーマを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="2595f-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="2595f-129">詳細については、[IoT Hub メッセージのスキーマの形式](iot-schema-format.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2595f-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="2595f-130">この例では、メッセージ ペイロードに次の形式のメッセージがまとめて含まれています。</span><span class="sxs-lookup"><span data-stu-id="2595f-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

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

7. <span data-ttu-id="2595f-131">テーブルに明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="2595f-132">**スキーマ名** フィールドを **ID** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="2595f-133">**スキーマのパス** フィールドを **/payload\[\*\]/id** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="2595f-134">**説明** フィールドを **メッセージ ID** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="2595f-135">テーブルに別の明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="2595f-136">**スキーマ名** フィールドを **タイムスタンプ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="2595f-137">**スキーマのパス** フィールドを **/payload\[\*\]/id** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="2595f-138">**説明** フィールドを **メッセージ タイムスタンプ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="2595f-139">テーブルに別の明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="2595f-140">**スキーマ名** フィールドを **ID** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="2595f-141">**スキーマのパス** フィールドを **/payload\[\*\]/id** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="2595f-142">**説明** フィールドを **メッセージ値** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2595f-143">メッセージ内のすべてのプロパティを定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2595f-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="2595f-144">必要なプロパティのみを定義します。</span><span class="sxs-lookup"><span data-stu-id="2595f-144">Define only the properties that you require.</span></span> <span data-ttu-id="2595f-145">前の手順では、**ルートタイムスタンプ** の行は作成しませんでした。</span><span class="sxs-lookup"><span data-stu-id="2595f-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="2595f-146">**ルート タイムスタンプ** のパスは **/timestamp** です。</span><span class="sxs-lookup"><span data-stu-id="2595f-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="2595f-147">**次へ** をクリックして、**装置センサーのスキーマ マッピング** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="2595f-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="2595f-148">**装置リソース ID** の行の、**スキーマ名** フィールドで **ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="2595f-149">**UTC 時間** の行で、**スキーマ名** フィールドの **タイムスタンプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="2595f-150">**パーツ生成信号** の行で、**スキーマ名** フィールドで **値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="2595f-151">**次へ** をクリックして、**装置リソース ID の構成** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="2595f-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="2595f-152">これらの手順に従って、IoT Hub メッセージの値を Supply Chain Management のリソースにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="2595f-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="2595f-153">**シグナル データ値** テーブルで、新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="2595f-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="2595f-154">**値** フィールドで、**IoTInt.Machine1225.PartOut** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2595f-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="2595f-155">この値は、IoT Hub メッセージの JSON **ID** 値プロパティから取得されます。</span><span class="sxs-lookup"><span data-stu-id="2595f-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="2595f-156">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-156">Select **Save**.</span></span>
    3. <span data-ttu-id="2595f-157">**業務レコードのマッピング** テーブルで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="2595f-158">**業務レコード タイプ** フィールドの既定値は自動入力されるため、変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2595f-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="2595f-159">**業務レコード** フィールドで、この信号の値を送信する Supply Chain Management マシンのリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="2595f-160">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-160">Select **Save**.</span></span>
    6. <span data-ttu-id="2595f-161">これらの手順を繰り返して、**Machine1226** に新たな業務レコード マッピングを追加します。</span><span class="sxs-lookup"><span data-stu-id="2595f-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="2595f-162">Supply Chain Management では、複数の信号データの値を 1 つのレコードにマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="2595f-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="2595f-163">処理するマシンを選択するには、**選択済** 列を使用します。</span><span class="sxs-lookup"><span data-stu-id="2595f-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="2595f-164">すべての信号の値を定義する必要はなく、すべてのマシンを選択する必要もありません。</span><span class="sxs-lookup"><span data-stu-id="2595f-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="2595f-165">**次へ** を選択して、**パーツ生成信号の構成** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="2595f-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="2595f-166">**信号データ値** テーブルで、行を追加し、**値** フィールドを **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2595f-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="2595f-167">この値は、IoT Hub メッセージの JSON **値** プロパティから取得されます。</span><span class="sxs-lookup"><span data-stu-id="2595f-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="2595f-168">シナリオに必要な数だけ値を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="2595f-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="2595f-169">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-169">Select **Save**.</span></span>
20. <span data-ttu-id="2595f-170">**次へ** を選択して、**装置ダウンタイムのしきい値** ページに移動し ます。</span><span class="sxs-lookup"><span data-stu-id="2595f-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="2595f-171">一覧に表示されているマシンは、既に信号の値にマッピングされているマシンです。</span><span class="sxs-lookup"><span data-stu-id="2595f-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="2595f-172">このページでは、マシンが停止しているかどうかを判断するしきい値を定義します。</span><span class="sxs-lookup"><span data-stu-id="2595f-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="2595f-173">たとえば、しきい値を **10** に設定した場合、**PartOut** 信号を 10 分間マシンから受信しない場合は Supply Chain Management が通知が生成します。</span><span class="sxs-lookup"><span data-stu-id="2595f-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="2595f-174">**次へ** を選択して **シナリオの有効化** ページに進みます。</span><span class="sxs-lookup"><span data-stu-id="2595f-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="2595f-175">オプションを設定してシナリオを有効化します。</span><span class="sxs-lookup"><span data-stu-id="2595f-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="2595f-176">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-176">Select **Finish**.</span></span>

<span data-ttu-id="2595f-177">シナリオの設定が完了しました。</span><span class="sxs-lookup"><span data-stu-id="2595f-177">The scenario setup is now completed.</span></span> <span data-ttu-id="2595f-178">IoT Hub インテリジェンスでは、IoT Hub メッセージの処理が自動的に開始されます。</span><span class="sxs-lookup"><span data-stu-id="2595f-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="2595f-179">Supply Chain Management における 製品の品質シナリオの構成</span><span class="sxs-lookup"><span data-stu-id="2595f-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="2595f-180">**製品の品質** シナリオでは、品目の属性が指定された範囲外の場合に通知を生成します。</span><span class="sxs-lookup"><span data-stu-id="2595f-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="2595f-181">たとえば、センサーで各品目の重量を IoT Hub に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="2595f-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="2595f-182">Supply Chain Management では、品目が重すぎる、または軽すぎる場合に通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="2595f-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="2595f-183">**製品品質** シナリオには、次のような依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="2595f-184">マッピングされたマシンで製造オーダーを実行し、マッピングされたバッチ属性を持つ製品を生産したときのみ警告をトリガーすることができます。</span><span class="sxs-lookup"><span data-stu-id="2595f-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="2595f-185">バッチ属性を表す信号が IoT ハブに送信され、一意のプロパティ名が含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="2595f-186">この値がミリ秒単位で表される UNIX **タイムスタンプ** プロパティが、IoT Hib メッセージに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="2595f-187">Supply Chain Management における 生産遅延シナリオの構成</span><span class="sxs-lookup"><span data-stu-id="2595f-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="2595f-188">**生産遅延** シナリオでは、生産の処理能力がしきい値を下回った場合に通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="2595f-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="2595f-189">このシナリオでは、生産された品目ごとに **PartOut** 信号が IoT Hub に送信されます。</span><span class="sxs-lookup"><span data-stu-id="2595f-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="2595f-190">Supply Chain Management では、注文の遅延は、製造オーダーの実行がスケジュールされている量、生産されるべき品目の数、ジョブが実行された時間数、および入庫した **PartOut** 信号数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="2595f-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="2595f-191">ジョブに対する **PartOut** 信号の数が想定されるしきい値を下回った場合に、遅延通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="2595f-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="2595f-192">**生産遅延** シナリオには、次のような依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="2595f-193">警告をトリガーするには、マッピングされたマシンで製造オーダーが実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="2595f-194">マッピングされたマシンの **PartOut** 信号を表す信号は、一意のプロパティ名でAzure IoT ハブに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="2595f-195">この値がミリ秒単位で表される UNIX **タイムスタンプ** プロパティが、IoT Hib メッセージに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2595f-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="2595f-196">シナリオの無効化</span><span class="sxs-lookup"><span data-stu-id="2595f-196">Disable a scenario</span></span>

<span data-ttu-id="2595f-197">次の手順に従い、シナリオを無効化します。</span><span class="sxs-lookup"><span data-stu-id="2595f-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="2595f-198">Supply Chain Management では、**生産管理 \> 設定 \> IoT インテリジェンス \> シナリオ管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2595f-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="2595f-199">シナリオのタイルで、**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2595f-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="2595f-200">**次へ** を選択して最後のウィザード ページに進みます。</span><span class="sxs-lookup"><span data-stu-id="2595f-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="2595f-201">オプションを設定してシナリオを無効化します。</span><span class="sxs-lookup"><span data-stu-id="2595f-201">Set the option to disable the scenario.</span></span>
