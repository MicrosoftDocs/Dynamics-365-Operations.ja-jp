---
title: Sensor Data Intelligence のパラメーター
description: この記事では、Sensor Data Intelligence パラメータ ページで使用できる構成の設定に関する情報を提供します。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5240537e3a6526ceb35253b9e68f46b1753c6a37
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689376"
---
# <a name="sensor-data-intelligence-parameters"></a>Sensor Data Intelligence のパラメーター

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

**Sensor Data Intelligence パラメータ** ページには、機能の構成に使用できるいくつかの設定が表示されます。 これらの設定には、Azure 接続パラメータと、調整測定に応答してユーザーに送信される警告メッセージの有効期間のパラメータが含まれます。

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Azure IoT ソリューションの接続の詳細を読み、変更する

通常は、Azure IoT ソリューションを設定し、そのソリューションを **Azure リソースの配置と接続** ページから Microsoft Dynamics 365 Supply Chain Management に接続します。このページでは、両方の手順について説明します。 (詳細については、[Azure に IoT ソリューションを配置する](sdi-deploy-iot-solution-on-azure.md) を参照してください。) Supply Chain Management では、次の手順に従って接続の詳細をいつでも表示および編集できます。

1. **システム管理 \> 設定 \> Sensor Data Intelligence \> Sensor Data Intelligence パラメーター** の順に移動します。
1. **時系列** タブの **Redis メトリック店舗の接続文字列** フィールドに、接続する Azure IoT ソリューションの **Primary 接続文字列 (StackExchange.Redis)** 値を入力します。 この値の検索方法の詳細については、[Azureへの IoT ソリューションの配置](sdi-deploy-iot-solution-on-azure.md) を参照してください。
1. **統合** タブの **Azure AD アプリケーション クライアント ID** フィールドに、接続する Azure IoT ソリューションの **クライアントID** 値を入力します。 この値の検索方法の詳細については、[Azureへの IoT ソリューションの配置](sdi-deploy-iot-solution-on-azure.md) を参照してください。

## <a name="set-the-lifetime-of-alert-messages"></a>警告メッセージの有効期間の設定

そのユーザーの注意が必要な状況がそのユーザーによって検出されると、そのユーザーに通知が送信されます。 これらの通知がシステムに表示されるのを防ぐには、数日後に期限切れとして設定する必要があります。

1. **システム管理 \> 設定 \> Sensor Data Intelligence \> Sensor Data Intelligence パラメーター** の順に移動します。
1. **通知** タブ の **通知日数** フィールド に、通知を保持する日数を入力します。 指定した時間が経過した後に通知が削除されます。
