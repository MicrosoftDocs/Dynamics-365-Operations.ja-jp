---
title: IoT ハブ メッセージのスキーマ形式
description: このトピックでは、IoT インテリジェンスで使用できるメッセージ スキーマをデザインする方法について説明します。
author: robinarh
ms.date: 04/25/2020
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
ms.openlocfilehash: 9ddd97b864e0bb361dc9ec26de4825f0de3352a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841973"
---
# <a name="schema-formats-for-iot-hub-messages"></a><span data-ttu-id="09c3b-103">IoT ハブ メッセージのスキーマ形式</span><span class="sxs-lookup"><span data-stu-id="09c3b-103">Schema formats for IoT Hub messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09c3b-104">このトピックでは、IoT インテリジェンスで使用できるメッセージ スキーマをデザインする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="09c3b-104">This topic explains how you should design a message schema that you can use in IoT Intelligence.</span></span>

## <a name="message-requirements"></a><span data-ttu-id="09c3b-105">メッセージ要件</span><span class="sxs-lookup"><span data-stu-id="09c3b-105">Message requirements</span></span>

<span data-ttu-id="09c3b-106">IoT インテリジェンスのメッセージの監視に適用される次のルールがあります。</span><span class="sxs-lookup"><span data-stu-id="09c3b-106">The following rules apply to the monitoring of messages in IoT Intelligence:</span></span>

+ <span data-ttu-id="09c3b-107">メッセージ スキーマは、JavaScript Object Notation (JSON) 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="09c3b-107">Message schemas must be in JavaScript Object Notation (JSON) format.</span></span>
+ <span data-ttu-id="09c3b-108">この値がミリ秒単位で表される UNIX **タイムスタンプ** プロパティ (ms) は、Microsoft Azure IoT ハブ メッセージに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="09c3b-108">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Microsoft Azure IoT Hub message.</span></span>
+ <span data-ttu-id="09c3b-109">メッセージは、シナリオ設定で定義されたすべてのプロパティが含まれている場合にのみ追跡されます。</span><span class="sxs-lookup"><span data-stu-id="09c3b-109">A message is tracked only if it contains all the properties that are defined in the scenario setup.</span></span> <span data-ttu-id="09c3b-110">たとえば、**ID**、**タイムスタンプ**、**値** のプロパティを定義すると、この次のメッセージが監視されます。</span><span class="sxs-lookup"><span data-stu-id="09c3b-110">For example, if you define **id**, **timestamp**, and **value** properties, the following message is monitored.</span></span>

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    <span data-ttu-id="09c3b-111">このメッセージは、**値** プロパティがないため監視されません。</span><span class="sxs-lookup"><span data-stu-id="09c3b-111">This message isn't monitored, because the **value** property is missing.</span></span>

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ <span data-ttu-id="09c3b-112">IoT インテリジェンスは、シナリオ コンフィギュレーションで定義されていないメッセージのプロパティを無視します。</span><span class="sxs-lookup"><span data-stu-id="09c3b-112">IoT Intelligence ignores properties in the message that aren't defined in the scenario configuration.</span></span> <span data-ttu-id="09c3b-113">たとえば、**ID**、**タイムスタンプ**、**値** のプロパティを定義すると、IoT インテリジェンスは次メッセージをすべて監視します。</span><span class="sxs-lookup"><span data-stu-id="09c3b-113">For example, if you define **id**, **timestamp**, and **value** properties, IoT Intelligence will monitor all the following messages.</span></span>

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

+ <span data-ttu-id="09c3b-114">IoT インテリジェンスは、シナリオ コンフィギュレーション基準に一致しないメッセージを警告なしで無視します。</span><span class="sxs-lookup"><span data-stu-id="09c3b-114">IoT Intelligence silently ignores messages that don't match the scenario configuration criteria.</span></span>
+ <span data-ttu-id="09c3b-115">複数のタイプのメッセージ スキーマを定義して使用できます。</span><span class="sxs-lookup"><span data-stu-id="09c3b-115">You can define and use multiple types of message schemas.</span></span>
+ <span data-ttu-id="09c3b-116">すべてのタイプのメッセージ スキーマを定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="09c3b-116">Not every type of message schema must be defined.</span></span> <span data-ttu-id="09c3b-117">IoT インテリジェンス シナリオに使用されるスキーマのみを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09c3b-117">Only schemas that will be used for the IoT Intelligence scenarios must be defined.</span></span>

## <a name="id-value-pair-schema"></a><span data-ttu-id="09c3b-118">Idと値のペア スキーマ</span><span class="sxs-lookup"><span data-stu-id="09c3b-118">Id-value pair schema</span></span>

<span data-ttu-id="09c3b-119">ID と値のペアは、IoT インテリジェンス メッセージ スキーマの一般的なパターンです。</span><span class="sxs-lookup"><span data-stu-id="09c3b-119">An id-value pair is a common pattern for IoT Intelligence message schemas.</span></span> <span data-ttu-id="09c3b-120">ID と値のペアを使用すると、すべてのシナリオでメッセージ スキーマが同じであることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="09c3b-120">By using an id-value pair, you ensure that your message schema is the same across all the scenarios.</span></span> <span data-ttu-id="09c3b-121">たとえば、これが、**装置のダウンタイム** または **生産遅延** シナリオのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="09c3b-121">For example, here is a message for the **Equipment downtime** or **Production delays** scenario.</span></span>

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

<span data-ttu-id="09c3b-122">これが、**製品品質** シナリオのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="09c3b-122">Here is a message for the **Product quality** scenario.</span></span>

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

<span data-ttu-id="09c3b-123">上記の 2 つのメッセージには **ID** と **値** プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="09c3b-123">Both the preceding messages contain **id** and **value** properties.</span></span> <span data-ttu-id="09c3b-124">**id** 値は、シナリオ設定時に **シグナル データ値** テーブルにマップできます。</span><span class="sxs-lookup"><span data-stu-id="09c3b-124">The **id** values can be mapped in the **Signal Data Values** table during scenario setup.</span></span> <span data-ttu-id="09c3b-125">**装置のダウンタイム** シナリオでは、**IoTInt.Machine1225.PartOut** 値をマップします。</span><span class="sxs-lookup"><span data-stu-id="09c3b-125">For the **Equipment downtime** scenario, you will map the **IoTInt.Machine1225.PartOut** value.</span></span> <span data-ttu-id="09c3b-126">**製品品質** シナリオでは、**IoTInt.Machine1225.Temperature** 値をマップします。</span><span class="sxs-lookup"><span data-stu-id="09c3b-126">For the **Product quality** scenario, you will map the **IoTInt.Machine1225.Temperature** value.</span></span>

<span data-ttu-id="09c3b-127">詳細については、[Azure IoT Hub ドキュメント](https://docs.microsoft.com/azure/iot-hub/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09c3b-127">For more information, see [Azure IoT Hub Documentation](https://docs.microsoft.com/azure/iot-hub/).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]