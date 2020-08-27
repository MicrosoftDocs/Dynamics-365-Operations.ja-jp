---
title: IoT ハブ メッセージのスキーマ形式
description: このトピックでは、IoT インテリジェンスで使用するメッセージ スキーマをデザインする方法について説明します。
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
ms.openlocfilehash: 6f56d6042133f016cb4a994cc169a41fd834a139
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597130"
---
# <a name="message-schema-formats-for-iot-hub"></a><span data-ttu-id="c15a4-103">IoT ハブのメッセージ スキーマ形式</span><span class="sxs-lookup"><span data-stu-id="c15a4-103">Message schema formats for IoT Hub</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c15a4-104">このトピックでは、IoT インテリジェンスで使用するメッセージ スキーマをデザインする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c15a4-104">This topic describes how you should design your message schema for use in IoT Intelligence.</span></span>

## <a name="message-requirements"></a><span data-ttu-id="c15a4-105">メッセージ要件</span><span class="sxs-lookup"><span data-stu-id="c15a4-105">Message requirements</span></span>

<span data-ttu-id="c15a4-106">IoT インテリジェンスのメッセージの監視に適用されるいくつかのルールがあります。</span><span class="sxs-lookup"><span data-stu-id="c15a4-106">There are a few rules that apply to monitoring messages in IoT Intelligence.</span></span>

+ <span data-ttu-id="c15a4-107">メッセージ スキーマは JSON 形式でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c15a4-107">Message schemas must be in JSON format.</span></span>

+ <span data-ttu-id="c15a4-108">IoT ハブ メッセージに Unix ミリタイム スタンプ プロパティが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c15a4-108">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

+ <span data-ttu-id="c15a4-109">メッセージは、シナリオ設定で定義されたすべてのプロパティが含まれている場合にのみ追跡されます。</span><span class="sxs-lookup"><span data-stu-id="c15a4-109">A message is tracked only if it contains all the properties defined in the scenario setup.</span></span> <span data-ttu-id="c15a4-110">たとえば、**id**、**タイムスタンプ**、**値** のプロパティを定義すると、このメッセージが監視されます:</span><span class="sxs-lookup"><span data-stu-id="c15a4-110">For example, if you define **id**, **timestamp**, and **value** properties then this message is monitored:</span></span>

    ```json
        {
            "id": "IoTInt.Machine1225.PartOut",
            "timestamp": 1576016821614,
            "value": True
        }
    ```

    <span data-ttu-id="c15a4-111">このメッセージは、**値** プロパティがないため監視されません。</span><span class="sxs-lookup"><span data-stu-id="c15a4-111">This message isn't monitored, because the **value** property is missing:</span></span>

    ```json
        {
            "id": "IoTInt.Machine1225.PartOut",
            "timestamp": 1576016821614,
        }
    ```

+ <span data-ttu-id="c15a4-112">IoT インテリジェンスは、シナリオ コンフィギュレーションで定義されていないメッセージのプロパティを無視します。</span><span class="sxs-lookup"><span data-stu-id="c15a4-112">IoT Intelligence ignores properties in the message that aren't defined in the scenario configuration.</span></span> <span data-ttu-id="c15a4-113">たとえば、**id**、**タイムスタンプ**、**値** のプロパティを定義すると、IoT インテリジェンスはこれらのメッセージをすべて監視します。</span><span class="sxs-lookup"><span data-stu-id="c15a4-113">For example, if you define **id**, **timestamp**, and **value** properties, then IoT Intelligence will monitor all of these messages:</span></span>

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

+ <span data-ttu-id="c15a4-114">IoT インテリジェンスは、シナリオ コンフィギュレーション基準に一致しないメッセージを警告なしで無視します。</span><span class="sxs-lookup"><span data-stu-id="c15a4-114">IoT Intelligence silently ignores messages that don't match the scenario configuration criteria.</span></span>

+ <span data-ttu-id="c15a4-115">複数のタイプのメッセージ スキーマを定義して使用できます。</span><span class="sxs-lookup"><span data-stu-id="c15a4-115">You can define and use multiple types of message schemas.</span></span>

+ <span data-ttu-id="c15a4-116">すべてのタイプのメッセージ スキーマを定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c15a4-116">Every type of message schema does not need to be defined.</span></span> <span data-ttu-id="c15a4-117">IoT インテリジェンス シナリオに使用されるスキーマのみを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c15a4-117">Only schemas that will be used for the IoT Intelligence scenarios need to be defined.</span></span>

## <a name="id-value-pair-schema"></a><span data-ttu-id="c15a4-118">Idと値のペア スキーマ</span><span class="sxs-lookup"><span data-stu-id="c15a4-118">Id-value pair schema</span></span>

<span data-ttu-id="c15a4-119">idと値のペアの使用は、IoT インテリジェンス メッセージ スキーマの一般的なパターンです。</span><span class="sxs-lookup"><span data-stu-id="c15a4-119">Using an id-value pair is a common pattern for IoT Intelligence message schemas.</span></span> <span data-ttu-id="c15a4-120">Idと値のペアを使用すると、すべてのシナリオでメッセージ スキーマが同じになります。</span><span class="sxs-lookup"><span data-stu-id="c15a4-120">By using an id-value pair, your message schema is the same across all the scenarios.</span></span> <span data-ttu-id="c15a4-121">たとえば、**設備のダウンタイム** または **生産の遅延** シナリオのメッセージは次のようになります:</span><span class="sxs-lookup"><span data-stu-id="c15a4-121">For example, a message for the **Equipment downtime** or **Production delays** scenario might look like this:</span></span>

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

<span data-ttu-id="c15a4-122">**製品品質** シナリオのメッセージは、次のようになります:</span><span class="sxs-lookup"><span data-stu-id="c15a4-122">A message for the **Product quality** scenario might look like this:</span></span>
```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

<span data-ttu-id="c15a4-123">どちらにも **id** と **値** プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c15a4-123">Both contain **id** and **value** properties.</span></span> <span data-ttu-id="c15a4-124">**id** 値は、シナリオ設定時に **シグナル データ値** テーブルにマップできます。</span><span class="sxs-lookup"><span data-stu-id="c15a4-124">The **id** values can be mapped in the **Signal Data Values** table during scenario setup.</span></span> <span data-ttu-id="c15a4-125">**設備のダウンタイム** シナリオでは、**IoTInt.Machine1225.PartOut** 値をマップします。</span><span class="sxs-lookup"><span data-stu-id="c15a4-125">For the **Equipment downtime** scenario, you would map the **IoTInt.Machine1225.PartOut** value.</span></span> <span data-ttu-id="c15a4-126">**製品品質** シナリオでは、**IoTInt.Machine1225.Temperature** 値をマップします。</span><span class="sxs-lookup"><span data-stu-id="c15a4-126">For the **Product quality** scenario, you would map the **IoTInt.Machine1225.Temperature** value.</span></span>

<span data-ttu-id="c15a4-127">詳細については、[Azure IoT Hub ドキュメント](https://docs.microsoft.com/azure/iot-hub/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c15a4-127">For more information, see [Azure IoT Hub Documentation](https://docs.microsoft.com/azure/iot-hub/).</span></span>
