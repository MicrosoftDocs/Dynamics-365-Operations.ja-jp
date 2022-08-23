---
title: IoT インテリジェンスのホーム ページ
description: この記事では、IoT インテリジェンスに関する情報へのリンクについて説明します。
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d8b2be25abaeff7404d7f4ef3cd825a50147fef
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228360"
---
# <a name="iot-intelligence-home-page"></a>IoT インテリジェンスのホーム ページ

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

> [!IMPORTANT]
> この機能は、現在次の国/地域でのみ使用できます。
>
> - US (米国)
> - EU (欧州連合)
> - AU (オーストラリア)
> - CA (カナダ)
> - UK (英国)

IoT インテリジェンス、Microsoft Dynamics 365 Supply Chain Management のアドインです。 また、モノのインターネット (Internet of Things: IoT) の信号を Supply Chain Management のデータと統合し、実用的な分析情報を生み出します。

IoT インテリジェンスにより、次のシナリオがサポートされます:

- **生産の遅延** – このシナリオでは、実際のサイクル時間と計画されたサイクル時間を比較します。 Supply Chain Management では、生産が予定通りに進んでいないことが通知されるため、介入して業務効率を最大化し、注文の遅延を回避できます。
- **設備のダウンタイム** – このシナリオでは、測定された稼働時間をユーザー定義パラメータと比較します。 Supply Chain Management は、では、停止しきい値を超えると通知されるため、生産作業指示書の再計画やメンテナンス作業指示書の作成などのアクションを実行できます。
- **製品品質** – このシナリオでは、湿気や気温などのセンサー測定値をユーザー定義の品質指標と比較します。 Supply Chain Management では、誤差が発生すると通知されるため、介入して品質基準を維持し、無駄を最小限に抑えることができます。

次の図は、Azure IoT Hub、IoT インテリジェンス、Supply Chain Management の相互作用を示しています。

![IoT Hub、IoT インテリジェンス、Supply Chain Management。](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>進捗管理とメンテナンス

- [Dynamics 365 Supply Chain Management でシナリオを監視](iot-management.md#monitor-scenarios)
- [シナリオの無効化](iot-scenario-setup.md#disable-a-scenario)
- [実行中の IoT インテリジェンス シナリオの変更](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [シミュレーション オプション](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]