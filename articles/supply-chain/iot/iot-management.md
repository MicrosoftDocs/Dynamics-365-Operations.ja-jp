---
title: IoT インテリジェンスの監視と管理
description: このトピックでは、IoT インテリジェンスを監視・管理する方法について説明します。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 15021281b9ec33cd0552bca16e3054d0d3cdd589
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432214"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="a54fc-103">IoT インテリジェンスの監視と管理</span><span class="sxs-lookup"><span data-stu-id="a54fc-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a54fc-104">このトピックでは、IoT インテリジェンスを監視・管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a54fc-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="a54fc-105">Microsoft Dynamics 365 Supply Chain Management のシナリオを監視する</span><span class="sxs-lookup"><span data-stu-id="a54fc-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="a54fc-106">IoT インテリジェンスが行う処理は、複数の場所から監視できます:</span><span class="sxs-lookup"><span data-stu-id="a54fc-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="a54fc-107">**モジュール \> 生産管理 \> 照会とレポート \> IoT インテリジェンス \> 通知** – 未解決の通知の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="a54fc-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="a54fc-108">**モジュール \> 生産管理 \> 照会とレポート \> IoT インテリジェンス \> 確認済みの通知** – 対応済み、または無視した通知の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="a54fc-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="a54fc-109">**モジュール \> 生産管理 \> 照会とレポート \> IoTインテリジェンス \>メトリック キー** – **リソース ステータス** の時系列グラフのメトリック キーを表示し ます。</span><span class="sxs-lookup"><span data-stu-id="a54fc-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="a54fc-110">**モジュール \> 生産管理 \> 製造の実行 \> リソース ステータス** – **構成** ダイアログ ボックスを使用して特定のメトリックを追跡します。</span><span class="sxs-lookup"><span data-stu-id="a54fc-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="a54fc-111">シナリオで例外が検出された場合は、例外の詳細が通知されます。</span><span class="sxs-lookup"><span data-stu-id="a54fc-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="a54fc-112">**ワークスペース \> 生産現場管理 \> 通知** – 未解決の通知の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="a54fc-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="a54fc-113">実行中の IoT インテリジェンス シナリオの変更</span><span class="sxs-lookup"><span data-stu-id="a54fc-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="a54fc-114">シナリオが実行されている場合は、以下の変更を行うことができます:</span><span class="sxs-lookup"><span data-stu-id="a54fc-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="a54fc-115">新たなセンサー スキーマの定義を追加する。</span><span class="sxs-lookup"><span data-stu-id="a54fc-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="a54fc-116">新たなシグナル データ値を選択する。</span><span class="sxs-lookup"><span data-stu-id="a54fc-116">Select new signal data values.</span></span>
+ <span data-ttu-id="a54fc-117">既存のシグナル データ値の選択をキャンセルする。</span><span class="sxs-lookup"><span data-stu-id="a54fc-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="a54fc-118">新たなシグナル データ値を追加・マッピングする。</span><span class="sxs-lookup"><span data-stu-id="a54fc-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="a54fc-119">しきい値を更新する。</span><span class="sxs-lookup"><span data-stu-id="a54fc-119">Update threshold values.</span></span>

<span data-ttu-id="a54fc-120">シナリオが実行されている場合は、以下の変更はできません:</span><span class="sxs-lookup"><span data-stu-id="a54fc-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="a54fc-121">有効なシナリオが現在消費しているスキーマ定義の削除・変更。</span><span class="sxs-lookup"><span data-stu-id="a54fc-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="a54fc-122">有効なシナリオの選択したスキーマのパスを変更する。</span><span class="sxs-lookup"><span data-stu-id="a54fc-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="a54fc-123">シミュレーション オプション</span><span class="sxs-lookup"><span data-stu-id="a54fc-123">Simulation options</span></span>

<span data-ttu-id="a54fc-124">工場のマシンの信号をシミュレートすることができます。</span><span class="sxs-lookup"><span data-stu-id="a54fc-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="a54fc-125">詳細については、以下のトピックを参照してください:</span><span class="sxs-lookup"><span data-stu-id="a54fc-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="a54fc-126">IoT DevKit AZ3166 を Azure IoT ハブに接続する</span><span class="sxs-lookup"><span data-stu-id="a54fc-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="a54fc-127">Raspberry Pi online シミュレーターを Azure IoT ハブ (node.js) に接続する</span><span class="sxs-lookup"><span data-stu-id="a54fc-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="a54fc-128">デバイス シミュレーション ソリューション アクセラレータの概要</span><span class="sxs-lookup"><span data-stu-id="a54fc-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
