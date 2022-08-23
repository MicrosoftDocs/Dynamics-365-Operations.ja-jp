---
title: IoT ハブ メッセージのスキーマ形式
description: この記事では、IoT インテリジェンスで使用できるメッセージ スキーマをデザインする方法について説明します。
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6d133d520ce0a1dccb2575e352f63e6ceb2bd3f
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228635"
---
# <a name="schema-formats-for-iot-hub-messages"></a>IoT ハブ メッセージのスキーマ形式

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

この記事では、IoT インテリジェンスで使用できるメッセージ スキーマをデザインする方法について説明します。

## <a name="message-requirements"></a>メッセージ要件

IoT インテリジェンスのメッセージの監視に適用される次のルールがあります。

+ メッセージ スキーマは、JavaScript Object Notation (JSON) 形式である必要があります。
+ この値がミリ秒単位で表される UNIX **タイムスタンプ** プロパティ (ms) は、Microsoft Azure IoT ハブ メッセージに含まれている必要があります。
+ メッセージは、シナリオ設定で定義されたすべてのプロパティが含まれている場合にのみ追跡されます。 たとえば、**ID**、**タイムスタンプ**、**値** のプロパティを定義すると、この次のメッセージが監視されます。

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

+ IoT インテリジェンスは、シナリオ コンフィギュレーションで定義されていないメッセージのプロパティを無視します。 たとえば、**ID**、**タイムスタンプ**、**値** のプロパティを定義すると、IoT インテリジェンスは次メッセージをすべて監視します。

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

ID と値のペアは、IoT インテリジェンス メッセージ スキーマの一般的なパターンです。 ID と値のペアを使用すると、すべてのシナリオでメッセージ スキーマが同じであることを確認できます。 たとえば、これが、**装置のダウンタイム** または **生産遅延** シナリオのメッセージです。

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

これが、**製品品質** シナリオのメッセージです。

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

上記の 2 つのメッセージには **ID** と **値** プロパティが含まれます。 **id** 値は、シナリオ設定時に **シグナル データ値** テーブルにマップできます。 **装置のダウンタイム** シナリオでは、**IoTInt.Machine1225.PartOut** 値をマップします。 **製品品質** シナリオでは、**IoTInt.Machine1225.Temperature** 値をマップします。

詳細については、[Azure IoT Hub ドキュメント](/azure/iot-hub/) を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]