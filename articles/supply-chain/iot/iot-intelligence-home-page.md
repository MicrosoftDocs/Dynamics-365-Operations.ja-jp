---
title: IoT インテリジェンス ホーム ページ
description: このトピックでは、IoT インテリジェンスに関する情報へのリンクについて説明します。
author: robinarh
manager: tfehr
ms.date: 12/09/2020
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
ms.openlocfilehash: dbb4e2d87b4e8b7a71073e66ffc1861701ce8c3f
ms.sourcegitcommit: bb75a2373b520a8e2b6a9a276d40697bf90ced75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2020
ms.locfileid: "4717265"
---
# <a name="iot-intelligence-home-page"></a><span data-ttu-id="4aa87-103">IoT インテリジェンスのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="4aa87-103">IoT Intelligence home page</span></span>

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="4aa87-104">この機能は、現在次の国/地域でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="4aa87-104">This feature is currently only available in the following countries/regions:</span></span>
>
> - <span data-ttu-id="4aa87-105">US (米国)</span><span class="sxs-lookup"><span data-stu-id="4aa87-105">US (United States of America)</span></span>
> - <span data-ttu-id="4aa87-106">EU (欧州連合)</span><span class="sxs-lookup"><span data-stu-id="4aa87-106">EU (European Union)</span></span>
> - <span data-ttu-id="4aa87-107">AU (オーストラリア)</span><span class="sxs-lookup"><span data-stu-id="4aa87-107">AU (Australia)</span></span>
> - <span data-ttu-id="4aa87-108">CA (カナダ)</span><span class="sxs-lookup"><span data-stu-id="4aa87-108">CA (Canada)</span></span>
> - <span data-ttu-id="4aa87-109">UK (英国)</span><span class="sxs-lookup"><span data-stu-id="4aa87-109">UK (United Kingdom)</span></span>

<span data-ttu-id="4aa87-110">IoT インテリジェンス、Microsoft Dynamics 365 Supply Chain Management のアドインです。</span><span class="sxs-lookup"><span data-stu-id="4aa87-110">IoT Intelligence is an add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4aa87-111">また、モノのインターネット (Internet of Things: IoT) の信号を Supply Chain Management のデータと統合し、実用的な分析情報を生み出します。</span><span class="sxs-lookup"><span data-stu-id="4aa87-111">It integrates Internet of Things (IoT) signals with data in Supply Chain Management to produce actionable insights.</span></span>

<span data-ttu-id="4aa87-112">IoT インテリジェンスにより、次のシナリオがサポートされます:</span><span class="sxs-lookup"><span data-stu-id="4aa87-112">IoT Intelligence supports the following scenarios:</span></span>

+ <span data-ttu-id="4aa87-113">**生産の遅延** – このシナリオでは、実際のサイクル時間と計画されたサイクル時間を比較します。</span><span class="sxs-lookup"><span data-stu-id="4aa87-113">**Production delays** – This scenario compares actual cycle time to planned cycle time.</span></span> <span data-ttu-id="4aa87-114">Supply Chain Management では、生産が予定通りに進んでいないことが通知されるため、介入して業務効率を最大化し、注文の遅延を回避できます。</span><span class="sxs-lookup"><span data-stu-id="4aa87-114">Supply Chain Management notifies you when production isn't on schedule, so that you can intervene to maximize operating efficiency and avoid order delays.</span></span>
+ <span data-ttu-id="4aa87-115">**設備のダウンタイム** – このシナリオでは、測定された稼働時間をユーザー定義パラメータと比較します。</span><span class="sxs-lookup"><span data-stu-id="4aa87-115">**Equipment downtime** – This scenario compares measured uptime to user-defined parameters.</span></span> <span data-ttu-id="4aa87-116">Supply Chain Management は、では、停止しきい値を超えると通知されるため、生産作業指示書の再計画やメンテナンス作業指示書の作成などのアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="4aa87-116">Supply Chain Management notifies you when an outage threshold is exceeded, so that you can take actions such as rescheduling a production work order or creating a maintenance work order.</span></span>
+ <span data-ttu-id="4aa87-117">**製品品質** – このシナリオでは、湿気や気温などのセンサー測定値をユーザー定義の品質指標と比較します。</span><span class="sxs-lookup"><span data-stu-id="4aa87-117">**Product quality** – This scenario compares sensor readings, such as moisture and temperature, to user-defined quality metrics.</span></span> <span data-ttu-id="4aa87-118">Supply Chain Management では、誤差が発生すると通知されるため、介入して品質基準を維持し、無駄を最小限に抑えることができます。</span><span class="sxs-lookup"><span data-stu-id="4aa87-118">Supply Chain Management notifies you when a deviation occurs, so that you can intervene to maintain quality standards and minimize waste.</span></span>

<span data-ttu-id="4aa87-119">次の図は、Azure IoT Hub、IoT インテリジェンス、Supply Chain Management の相互作用を示しています。</span><span class="sxs-lookup"><span data-stu-id="4aa87-119">The following illustration shows the interaction of Azure IoT Hub, IoT Intelligence, and Supply Chain Management.</span></span>

![IoT Hub、IoT インテリジェンス、Supply Chain Management](media/iot_intelligence.png)

## <a name="setup"></a><span data-ttu-id="4aa87-121">セットアップ</span><span class="sxs-lookup"><span data-stu-id="4aa87-121">Setup</span></span>

<span data-ttu-id="4aa87-122">コードを記述することなく、IoT インテリジェンスを設定およびコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="4aa87-122">You can set up and configure IoT Intelligence without writing any code.</span></span> <span data-ttu-id="4aa87-123">基本的な手順は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4aa87-123">Here are the basic steps.</span></span>

1. <span data-ttu-id="4aa87-124">[Azure リソースの設定](iot-azure-setup.md) – Supply Chain Management からアクセスできる IoT ハブ、Redis キャッシュ、Key Vault を作成します。</span><span class="sxs-lookup"><span data-stu-id="4aa87-124">[Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.</span></span>
2. <span data-ttu-id="4aa87-125">[IoT Hub のメッセージ スキーマ 形式 ](iot-schema-format.md) – メッセージを IoT Hub に送信するようにデバイスをコンフィギュレーションして、JavaScript Object Notation (JSON) メッセージ形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="4aa87-125">[Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.</span></span>
3. <span data-ttu-id="4aa87-126">機能管理で、IoT インテリジェンス機能のフラグを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4aa87-126">In Feature Management, enable the IoT Intelligence feature flag.</span></span> 
4. <span data-ttu-id="4aa87-127">[IoT インテリジェンス アドインを Microsoft Dynamics Lifecycle Services (LCS) にインストールする](iot-lcs-setup.md) – LCS にアドインをインストールし、Azure シークレットをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="4aa87-127">[Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.</span></span>
5. <span data-ttu-id="4aa87-128">[指標の設定](iot-metrics-setup.md) – Supply Chain Management の指標を設定します。</span><span class="sxs-lookup"><span data-stu-id="4aa87-128">[Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.</span></span>
6. <span data-ttu-id="4aa87-129">[シナリオ設定](iot-scenario-setup.md) – Supply Chain Management でシナリオを設定します。</span><span class="sxs-lookup"><span data-stu-id="4aa87-129">[Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.</span></span>

## <a name="tracking-and-maintenance"></a><span data-ttu-id="4aa87-130">進捗管理とメンテナンス</span><span class="sxs-lookup"><span data-stu-id="4aa87-130">Tracking and maintenance</span></span>

+ [<span data-ttu-id="4aa87-131">Dynamics 365 Supply Chain Management でシナリオを監視</span><span class="sxs-lookup"><span data-stu-id="4aa87-131">Monitor scenarios in Dynamics 365 Supply Chain Management</span></span>](iot-management.md#monitor-scenarios)
+ [<span data-ttu-id="4aa87-132">シナリオの無効化</span><span class="sxs-lookup"><span data-stu-id="4aa87-132">Disable a scenario</span></span>](iot-scenario-setup.md#disable-a-scenario)
+ [<span data-ttu-id="4aa87-133">アドインのアンインストール</span><span class="sxs-lookup"><span data-stu-id="4aa87-133">Uninstall the add-in</span></span>](iot-lcs-setup.md#uninstall-addin)
+ [<span data-ttu-id="4aa87-134">実行中の IoT インテリジェンス シナリオの変更</span><span class="sxs-lookup"><span data-stu-id="4aa87-134">Modify a running IoT Intelligence scenario</span></span>](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [<span data-ttu-id="4aa87-135">シミュレーション オプション</span><span class="sxs-lookup"><span data-stu-id="4aa87-135">Simulation options</span></span>](iot-management.md#simulation-options)
