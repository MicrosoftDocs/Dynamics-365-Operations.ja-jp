---
title: IoT ハブ メッセージのスキーマ形式
description: このトピックでは、IoT インテリジェンスで使用するメッセージ スキーマをデザインする方法について説明します。
author: robinarh
manager: AnnBe
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
ms.openlocfilehash: 5de0671366490c046d4fd32ae8ec77bc744a5402
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386424"
---
# <a name="message-schema-formats-for-iot-hub"></a>IoT ハブのメッセージ スキーマ形式

[!include [banner](../../includes/banner.md)]

このトピックでは、IoT インテリジェンスで使用するメッセージ スキーマをデザインする方法について説明します。

## <a name="message-requirements"></a>メッセージ要件

IoT インテリジェンスのメッセージの監視に適用されるいくつかのルールがあります。

+ メッセージ スキーマは JSON 形式でなければなりません。

+ IoT ハブ メッセージに Unix ミリタイム スタンプ プロパティが存在する必要があります。

+ メッセージは、シナリオ設定で定義されたすべてのプロパティが含まれている場合にのみ追跡されます。 たとえば、**id**、**タイムスタンプ**、**値** のプロパティを定義すると、このメッセージが監視されます:

    ```json
        {
            "id": "IoTInt.Machine1225.PartOut",
            "timestamp": 1576016821614,
            "value": True
        }
    ```

    このメッセージは、**値** プロパティがないため監視されません。

    ```json
        {
            "id": "IoTInt.Machine1225.PartOut",
            "timestamp": 1576016821614,
        }
    ```

+ IoT インテリジェンスは、シナリオ コンフィギュレーションで定義されていないメッセージのプロパティを無視します。 たとえば、**id**、**タイムスタンプ**、**値** のプロパティを定義すると、IoT インテリジェンスはこれらのメッセージをすべて監視します。

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

idと値のペアの使用は、IoT インテリジェンス メッセージ スキーマの一般的なパターンです。 Idと値のペアを使用すると、すべてのシナリオでメッセージ スキーマが同じになります。 たとえば、**設備のダウンタイム** または **生産の遅延** シナリオのメッセージは次のようになります:

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

**製品品質** シナリオのメッセージは、次のようになります:
```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

どちらにも **id** と **値** プロパティが含まれます。 **id** 値は、シナリオ設定時に **シグナル データ値** テーブルにマップできます。 **設備のダウンタイム** シナリオでは、**IoTInt.Machine1225.PartOut** 値をマップします。 **製品品質** シナリオでは、**IoTInt.Machine1225.Temperature** 値をマップします。

詳細については、[Azure IoT Hub ドキュメント](https://docs.microsoft.com/azure/iot-hub/) を参照してください。
