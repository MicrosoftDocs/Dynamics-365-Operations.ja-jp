---
title: IoT インテリジェンス ホーム ページ
description: このトピックでは、IoT インテリジェンスに関する情報へのリンクについて説明します。
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
ms.openlocfilehash: 0fe45c1145b084acd0fcf9a79b9dd376f1cdcd1e
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597446"
---
# <a name="iot-intelligence-home-page"></a><span data-ttu-id="3a9e3-103">IoT インテリジェンス ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="3a9e3-103">IoT Intelligence home page</span></span>

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="3a9e3-104">**使用可能性:** この機能は、中国の 21Vianet が運営する Finance and Operations アプリでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-104">**Availability:** This feature isn't available for Finance and Operations apps that are operated by 21Vianet in China.</span></span>

<span data-ttu-id="3a9e3-105">IoT インテリジェンス、Microsoft Dynamics 365 Supply Chain Management のアドインです。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-105">IoT Intelligence is an add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3a9e3-106">また、モノのインターネット (Internet of Things: IoT) の信号を Supply Chain Management のデータと統合し、実用的な分析情報を生み出します。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-106">It integrates Internet of Things (IoT) signals with data in Supply Chain Management to produce actionable insights.</span></span>

<span data-ttu-id="3a9e3-107">IoT インテリジェンスにより、次のシナリオがサポートされます:</span><span class="sxs-lookup"><span data-stu-id="3a9e3-107">IoT Intelligence supports the following scenarios:</span></span>

+ <span data-ttu-id="3a9e3-108">**生産の遅延** – このシナリオでは、実際のサイクル時間と計画されたサイクル時間を比較します。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-108">**Production delays** – This scenario compares actual cycle time to planned cycle time.</span></span> <span data-ttu-id="3a9e3-109">Supply Chain Management では、生産が予定通りに進んでいないことが通知されるため、介入して業務効率を最大化し、注文の遅延を回避できます。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-109">Supply Chain Management notifies you when production isn't on schedule, so that you can intervene to maximize operating efficiency and avoid order delays.</span></span>
+ <span data-ttu-id="3a9e3-110">**設備のダウンタイム** – このシナリオでは、測定された稼働時間をユーザー定義パラメータと比較します。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-110">**Equipment downtime** – This scenario compares measured uptime to user-defined parameters.</span></span> <span data-ttu-id="3a9e3-111">Supply Chain Management は、では、停止しきい値を超えると通知されるため、生産作業指示書の再計画やメンテナンス作業指示書の作成などのアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-111">Supply Chain Management notifies you when an outage threshold is exceeded, so that you can take actions such as rescheduling a production work order or creating a maintenance work order.</span></span>
+ <span data-ttu-id="3a9e3-112">**製品品質** – このシナリオでは、湿気や気温などのセンサー測定値をユーザー定義の品質指標と比較します。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-112">**Product quality** – This scenario compares sensor readings, such as moisture and temperature, to user-defined quality metrics.</span></span> <span data-ttu-id="3a9e3-113">Supply Chain Management では、誤差が発生すると通知されるため、介入して品質基準を維持し、無駄を最小限に抑えることができます。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-113">Supply Chain Management notifies you when a deviation occurs, so that you can intervene to maintain quality standards and minimize waste.</span></span>

<span data-ttu-id="3a9e3-114">次の図は、Azure IoT Hub、IoT インテリジェンス、Supply Chain Management の相互作用を示しています。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-114">The following illustration shows the interaction of Azure IoT Hub, IoT Intelligence, and Supply Chain Management.</span></span>

![IoT Hub、IoT インテリジェンス、Supply Chain Management](media/iot_intelligence.png)

## <a name="setup"></a><span data-ttu-id="3a9e3-116">セットアップ</span><span class="sxs-lookup"><span data-stu-id="3a9e3-116">Setup</span></span>

<span data-ttu-id="3a9e3-117">コードを記述することなく、IoT インテリジェンスを設定およびコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-117">You can set up and configure IoT Intelligence without writing any code.</span></span> <span data-ttu-id="3a9e3-118">基本的な手順は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-118">Here are the basic steps.</span></span>

1. <span data-ttu-id="3a9e3-119">[Azure リソースの設定](iot-azure-setup.md) – Supply Chain Management からアクセスできる IoT ハブ、Redis キャッシュ、Key Vault を作成します。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-119">[Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.</span></span>
2. <span data-ttu-id="3a9e3-120">[IoT Hub のメッセージ スキーマ 形式 ](iot-schema-format.md) – メッセージを IoT Hub に送信するようにデバイスをコンフィギュレーションして、JavaScript Object Notation (JSON) メッセージ形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-120">[Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.</span></span>
3. <span data-ttu-id="3a9e3-121">機能管理で、IoT インテリジェンス機能のフラグを有効にします。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-121">In Feature Management, enable the IoT Intelligence feature flag.</span></span> 
4. <span data-ttu-id="3a9e3-122">[IoT インテリジェンス アドインを Microsoft Dynamics Lifecycle Services (LCS) にインストールする](iot-lcs-setup.md) – LCS にアドインをインストールし、Azure シークレットをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-122">[Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.</span></span>
5. <span data-ttu-id="3a9e3-123">[指標の設定](iot-metrics-setup.md) – Supply Chain Management の指標を設定します。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-123">[Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.</span></span>
6. <span data-ttu-id="3a9e3-124">[シナリオ設定](iot-scenario-setup.md) – Supply Chain Management でシナリオを設定します。</span><span class="sxs-lookup"><span data-stu-id="3a9e3-124">[Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.</span></span>

## <a name="tracking-and-maintenance"></a><span data-ttu-id="3a9e3-125">進捗管理とメンテナンス</span><span class="sxs-lookup"><span data-stu-id="3a9e3-125">Tracking and maintenance</span></span>

+ [<span data-ttu-id="3a9e3-126">Dynamics 365 Supply Chain Management でシナリオを監視</span><span class="sxs-lookup"><span data-stu-id="3a9e3-126">Monitor scenarios in Dynamics 365 Supply Chain Management</span></span>](iot-management.md#monitor-scenarios)
+ [<span data-ttu-id="3a9e3-127">シナリオの無効化</span><span class="sxs-lookup"><span data-stu-id="3a9e3-127">Disable a scenario</span></span>](iot-scenario-setup.md#how-to-disable-a-scenario)
+ [<span data-ttu-id="3a9e3-128">アドインのアンインストール</span><span class="sxs-lookup"><span data-stu-id="3a9e3-128">Uninstall the add-in</span></span>](iot-lcs-setup.md#uninstall-addin)
+ [<span data-ttu-id="3a9e3-129">実行中の IoT インテリジェンス シナリオの変更</span><span class="sxs-lookup"><span data-stu-id="3a9e3-129">Modify a running IoT Intelligence scenario</span></span>](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [<span data-ttu-id="3a9e3-130">シミュレーション オプション</span><span class="sxs-lookup"><span data-stu-id="3a9e3-130">Simulation options</span></span>](iot-management.md#simulation-options)
