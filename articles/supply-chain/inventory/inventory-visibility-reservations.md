---
title: 在庫視覚化引当
description: このトピックでは、在庫可視化を使用して、引当を作成したり、引当を消費したり、指定された在庫量の引当を解除するために引当機能を設定する方法について説明します。
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6c87018cbfbe22fbbc441a1a23aee0ac44af9ddc
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345152"
---
# <a name="inventory-visibility-reservations"></a>在庫視覚化引当

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

このトピックでは、在庫可視化を使用して、引当を作成したり、引当を消費したり、指定された在庫量の引当を解除するために引当機能を設定する方法について説明します。

引当は、将来使用される在庫の数量をマークします。 引当を作成すると、引当が消費または解除されるまで、他の注文によって引当済商品を引当または消費することを防ぎます。 在庫可視化サービスへの API 呼び出しを使用して、引当が作成、消費、およびキャンセルされます。

オプションで、Microsoft Dynamics 365 Supply Chain Management (および他のサード パーティ システム) を設定して、在庫可視化を使用し、引当された数量を自動的に相殺できます。 相殺数量は、在庫可視化の引当レコードから削除されます。

引当機能を有効にすると、Supply Chain Management は在庫可視化を使用して行われた引当を自動的に相殺できます。

> [!NOTE]
> 相殺機能を使用するには、Supply Chain Management version のバージョン 10.0.22 以降が必要です。 在庫可視化引当を使用する場合は、Supply Chain Management をバージョン 10.0.22、またはそれ以降にアップグレードしてからご利用になることをお勧めします。

## <a name="turn-on-the-reservation-feature"></a>引当機能を有効にする

引当機能を有効にするには、次の手順を実行します。

1. Power Apps で **在庫可視化** を開きます。
1. **構成** ページを開きます。
1. **機能管理** タブで、*OnHandReservation* 機能を有効にします。
1. Supply Chain Management にサインインします。
1. **在庫管理 \> 設定 \> 在庫可視化統合パラメーター** の順に移動します。
1. **引当相殺** で、**引当相殺を有効にする** オプションを *はい* に設定します。

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>在庫可視化で引当機能を使用する

引当 API を呼び出すと、システムは指定した商品と数量の引当をマークします。 引当階層を定義し、その引当階層と一致する要求を転記する必要があります。 引当 API を直接呼び出すことによって、引当を作成できます。

### <a name="configure-the-reservation-hierarchy"></a>引当階層を構成する

引当階層は、引当の際に指定する必要がある分析コードの順序を表します。 これは、手持在庫クエリに対してインデックス階層が機能するのと同じように機能します。

引当階層は、インデックス階層とは異なる場合があります。 この独立性により、ユーザーが分析コードを詳細に分割して、より正確な引当の要件を指定できるカテゴリ管理を実装できます。

Power Apps で仮引当階層を構成するには、**コンフィギュレーション** ページを開き、**仮引当マッピング** タブで、分析コードと階層レベルを追加、修正して、引当階層を設定します。

### <a name="call-the-reservation-api"></a>引当 API を呼び出す

引当は、在庫可視化サービスで、`/api/environment/{environment-ID}/onhand/reserve` のようなサービスの URL に POST リクエストを送信することで行われます。

引当の場合、要求本文には、組織 ID、製品 ID、引当済数量、および分析コードが含まれている必要があります。 要求は、各引当レコードに対して一意の引当 ID を生成します。 引当レコードには、製品 ID と分析コードの一意の組み合わせが含まれています。

参照用の要求本文の例を次に示します。

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Supply Chain Management で 引当を相殺する

指定された引当相殺モディファイアを含む在庫トランザクション状態は、次のすべての条件が満たされた場合に、トランザクションの更新により、対応する引当レコードが相殺されます。

- 在庫トランザクションでの引当 ID は、在庫可視化サービスで引当レコードの引当 ID と一致します。
- 在庫トランザクションの分析コードは、在庫可視化サービスの引当レコードの分析コードと一致します。
- 在庫トランザクション状態の変更は、在庫トランザクション状態が注文プロセスが完了またはスキップされたという事実を反映している場合に、引当に対する相殺をトリガーします。

相殺数量は、在庫トランザクションで指定された在庫数量に従います。 在庫可視化サービスに引当済数量が残ってない場合、相殺は有効になりません。

> [!NOTE]
> 相殺機能はバージョン 10.0.22 以降より使用できます

### <a name="set-up-the-reserve-offset-modifier"></a>引当相殺モディファイアを設定する

引当相殺モディファイアは、相殺をトリガーする注文処理ステージを決定します。 ステージは、注文の在庫トランザクション状態によって追跡されます。 引当相殺モディファイアを設定するには、次の手順を実行します。

1. **在庫管理 \> 設定 \> 在庫可視化統合パラメーター \> 引当相殺** に移動します。
1. **引当相殺モディファイア** フィールドに、次のいずれかの値を設定する必要があります。

    - *受注中* – *トランザクション中* の状態では、注文が作成されると相殺要求を送信します。
    - *引当* – *引当注文済トランザクション* 状態では、注文が引当、ピッキング、梱包明細の転記、または請求を行った際に相殺要求を送信します。 要求は前述のプロセスが発生したときの最初のステップに対して、1 度だけトリガーされます。

### <a name="set-up-reservation-ids"></a>引当 ID を設定する

引当 ID は、在庫可視化で引当レコードを一意にマークします。 Supply Chain Management では、ユーザーは注文明細行に対して引当を行い、対応する引当レコードの相殺をマークします。

Supply Chain Management で引当 IDを設定するには、次の手順に従います。

1. 販売注文を開きます (例 : **すべての販売注文** ページから)。
1. **販売注文明細行** クイック タブで、注文明細行を選択します。
1. **販売注文明細行** クイック タブのツール バーで、**明細行の更新 \> 在庫 \> 在庫視覚化統合** を選択します。
1. 関連する引当 ID を入力します。

在庫状態の変更は、相殺モディファイアーの設定と一致します。
