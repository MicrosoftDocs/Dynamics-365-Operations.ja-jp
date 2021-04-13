---
title: IoT インテリジェンス ホーム ページ
description: このトピックでは、IoT インテリジェンスに関する情報へのリンクについて説明します。
author: robinarh
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1482c38de9d91fe256f2a1b28959ebcb0202295d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814864"
---
# <a name="iot-intelligence-home-page"></a>IoT インテリジェンスのホーム ページ

[!include [banner](../../includes/banner.md)]

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

+ **生産の遅延** – このシナリオでは、実際のサイクル時間と計画されたサイクル時間を比較します。 Supply Chain Management では、生産が予定通りに進んでいないことが通知されるため、介入して業務効率を最大化し、注文の遅延を回避できます。
+ **設備のダウンタイム** – このシナリオでは、測定された稼働時間をユーザー定義パラメータと比較します。 Supply Chain Management は、では、停止しきい値を超えると通知されるため、生産作業指示書の再計画やメンテナンス作業指示書の作成などのアクションを実行できます。
+ **製品品質** – このシナリオでは、湿気や気温などのセンサー測定値をユーザー定義の品質指標と比較します。 Supply Chain Management では、誤差が発生すると通知されるため、介入して品質基準を維持し、無駄を最小限に抑えることができます。

次の図は、Azure IoT Hub、IoT インテリジェンス、Supply Chain Management の相互作用を示しています。

![IoT Hub、IoT インテリジェンス、Supply Chain Management](media/iot_intelligence.png)

## <a name="setup"></a>セットアップ

コードを記述することなく、IoT インテリジェンスを設定およびコンフィギュレーションすることができます。 基本的な手順は次のとおりです。

1. [Azure リソースの設定](iot-azure-setup.md) – Supply Chain Management からアクセスできる IoT ハブ、Redis キャッシュ、Key Vault を作成します。
2. [IoT Hub のメッセージ スキーマ 形式 ](iot-schema-format.md) – メッセージを IoT Hub に送信するようにデバイスをコンフィギュレーションして、JavaScript Object Notation (JSON) メッセージ形式を定義します。
3. 機能管理で、IoT インテリジェンス機能のフラグを有効にします。 
4. [IoT インテリジェンス アドインを Microsoft Dynamics Lifecycle Services (LCS) にインストールする](iot-lcs-setup.md) – LCS にアドインをインストールし、Azure シークレットをコンフィギュレーションします。
5. [指標の設定](iot-metrics-setup.md) – Supply Chain Management の指標を設定します。
6. [シナリオ設定](iot-scenario-setup.md) – Supply Chain Management でシナリオを設定します。

## <a name="tracking-and-maintenance"></a>進捗管理とメンテナンス

+ [Dynamics 365 Supply Chain Management でシナリオを監視](iot-management.md#monitor-scenarios)
+ [シナリオの無効化](iot-scenario-setup.md#disable-a-scenario)
+ [アドインのアンインストール](iot-lcs-setup.md#uninstall-addin)
+ [実行中の IoT インテリジェンス シナリオの変更](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [シミュレーション オプション](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]