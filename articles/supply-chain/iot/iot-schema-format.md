---
title: IoT ハブ メッセージのスキーマ形式
description: このトピックでは、IoT インテリジェンスで使用できるメッセージ スキーマをデザインする方法について説明します。
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
ms.openlocfilehash: 720ffe718fd95d6f7f9ba046ecb3b15ed739ac02
ms.sourcegitcommit: 8adc65e26d78e229271eb427659a87ee5f371319
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2020
ms.locfileid: "3814047"
---
# <a name="schema-formats-for-iot-hub-messages"></a>IoT ハブ メッセージのスキーマ形式

[!include [banner](../../includes/banner.md)]

このトピックでは、IoT インテリジェンスで使用できるメッセージ スキーマをデザインする方法について説明します。

## <a name="message-requirements"></a>メッセージ要件

IoT インテリジェンスのメッセージの監視に適用される次のルールがあります。

+ メッセージ スキーマは、JavaScript Object Notation (JSON) 形式である必要があります。
+ この値がミリ秒単位で表される UNIX **タイムスタンプ** プロパティ (ms) は、Microsoft Azure IoT ハブ メッセージに含まれている必要があります。
+ メッセージは、シナリオ設定で定義されたすべてのプロパティが含まれている場合にのみ追跡されます。 たとえば、**ID**、**タイムスタンプ**、**値**のプロパティを定義すると、この次のメッセージが監視されます。

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    このメッセージは、**値**プロパティがないため監視されません。

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT インテリジェンスは、シナリオ コンフィギュレーションで定義されていないメッセージのプロパティを無視します。 たとえば、**ID**、**タイムスタンプ**、**値**のプロパティを定義すると、IoT インテリジェンスは次メッセージをすべて監視します。

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT インテリジェンスは、シナリオ コンフィギュレーション基準に一致しないメッセージを警告なしで無視します。
+ 複数のタイプのメッセージ スキーマを定義して使用できます。
+ すべてのタイプのメッセージ スキーマを定義する必要はありません。 IoT インテリジェンス シナリオに使用されるスキーマのみを定義する必要があります。

## <a name="id-value-pair-schema"></a>Idと値のペア スキーマ

ID と値のペアは、IoT インテリジェンス メッセージ スキーマの一般的なパターンです。 ID と値のペアを使用すると、すべてのシナリオでメッセージ スキーマが同じであることを確認できます。 たとえば、これが、**装置のダウンタイム**または**生産遅延**シナリオのメッセージです。

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

これが、**製品品質**シナリオのメッセージです。

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

上記の 2 つのメッセージには **ID** と**値**プロパティが含まれます。 **id** 値は、シナリオ設定時に **シグナル データ値** テーブルにマップできます。 **装置のダウンタイム** シナリオでは、**IoTInt.Machine1225.PartOut** 値をマップします。 **製品品質**シナリオでは、**IoTInt.Machine1225.Temperature** 値をマップします。

詳細については、[Azure IoT Hub ドキュメント](https://docs.microsoft.com/azure/iot-hub/) を参照してください。
