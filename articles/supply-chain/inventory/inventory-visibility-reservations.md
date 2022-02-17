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
ms.openlocfilehash: 5e6752539a6381e1f7271883102391374e04f3aa
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061707"
---
# <a name="inventory-visibility-reservations"></a>在庫視覚化引当

[!include [banner](../includes/banner.md)]


このトピックでは、在庫可視化を使用して、引当を作成したり、引当を消費したり、指定された在庫量の引当を解除するために引当機能を設定する方法について説明します。

引当は、将来使用される在庫の数量をマークします。 引当を作成すると、引当が消費または解除されるまで、他の注文によって引当済商品を引当または消費することを防ぎます。 在庫可視化サービスへの API 呼び出しを使用して、引当が作成、消費、およびキャンセルされます。

オプションで、Microsoft Dynamics 365 Supply Chain Management (および他のサード パーティ システム) を設定して、在庫可視化を使用し、引当された数量を自動的に相殺できます。 相殺数量は、在庫可視化の引当レコードから削除されます。

引当機能を有効にすると、Supply Chain Management は在庫可視化を使用して行われた引当を自動的に相殺できます。

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>引当機能を有効にし設定する

引当機能を有効にするには、次の手順を実行します。

1. Power Apps にサインインして、**在庫視覚化** を開きます。
1. **構成** ページを開きます。
1. **機能管理** タブで、*OnHandReservation* 機能を有効にします。
1. Supply Chain Management にサインインします。
1. **[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ワークスペースに移動し、*引当相殺と在庫視覚化の統合* 機能を有効にします (バージョン10.0.22 以降が必要)。
1. **在庫管理 \> 設定 \> 在庫視覚化統合パラメーター** に移動し、**引当相殺** タブを開き、次の設定を行います。
    - **引当相殺を有効にする** – *はい* に設定し、この機能を有効にします。
    - **引当相殺モディファイア** – 在庫視覚化に対して行われた引当を相殺する在庫トランザクション状態を選択します。 この設定は、相殺をトリガーする注文処理ステージを決定します。 ステージは、注文の在庫トランザクション状態によって追跡されます。 次のいずれかを選択します : 
        - *受注中* – *トランザクション中* の状態では、注文が作成されると相殺要求を送信します。 相殺数量は作成された注文の数量になります。
        - *引当* – *引当注文済トランザクション* 状態では、注文が引当、ピッキング、梱包明細の転記、または請求を行った際に相殺要求を送信します。 要求は前述のプロセスが発生したときの最初のステップに対して、1 度だけトリガーされます。 相殺数量は注文明細行の在庫トランザクション状態が *受注中* から *引当済注文* (またはそれ以降の状態) に変更された数量となります。

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>在庫可視化で引当機能を使用する

引当 API を呼び出すと、システムは指定した商品と数量の引当をマークします。 引当階層を定義し、その引当階層と一致する要求を転記する必要があります。 引当 API を直接呼び出すことによって、引当を作成できます。

### <a name="configure-the-reservation-hierarchy"></a>引当階層を構成する

引当階層は、引当の際に指定する必要がある分析コードの順序を表します。 これは、手持在庫クエリに対してインデックス階層が機能するのと同じように機能します。

引当階層は、インデックス階層とは異なる場合があります。 この独立性により、ユーザーが分析コードを詳細に分割して、より正確な引当の要件を指定できるカテゴリ管理を実装できます。

Power Apps で仮引当階層を構成するには、**構成** ページを開き、**仮引当階層** タブで、分析コードと階層レベルを追加、修正して、引当階層を設定します。

仮引当階層には、コンポーネントとして `SiteId` および `LocationId` が含まれている必要がありますが、これはパーティションの構成を構築するためです。

引当の構成方法の詳細については、[引当構成](inventory-visibility-configuration.md#reservation-configuration)を参照してください。

### <a name="call-the-reservation-api"></a>引当 API を呼び出す

引当は、在庫可視化サービスで、`/api/environment/{environment-ID}/onhand/reserve` のようなサービスの URL に POST リクエストを送信することで行われます。

引当の場合、要求本文には、組織 ID、製品 ID、引当済数量、および分析コードが含まれている必要があります。 要求は、各引当レコードに対して一意の引当 ID を生成します。 引当レコードには、製品 ID と分析コードの一意の組み合わせが含まれています。

引当 API を呼び出す際に、要求本文のブール値 `ifCheckAvailForReserv` パラメーターを指定することで、引当の検証を制御できます。 `True` という値は検証が必要であることを意味するのに対し、`False` という値は検証が必要ないことを意味します。 既定値は [`True`] です。

引当をキャンセルしたり、指定した引当在庫数量を解除したい場合は、数量を負の値に設定し、`ifCheckAvailForReserv` パラメーターを `False` に設定して検証をスキップします。

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

### <a name="set-up-the-reservation-offset-modifier"></a>引当相殺モディファイアを設定する

まだ設定していない場合は、[引当機能を有効にし設定する](#turn-on)にあるように引当モディファイアを設定してください。

### <a name="set-up-reservation-ids"></a>引当 ID を設定する

引当 ID は、在庫可視化で引当レコードを一意にマークします。 Supply Chain Management では、ユーザーは注文明細行に対して引当を行い、対応する引当レコードの相殺をマークします。

Supply Chain Management で引当 IDを設定するには、次の手順に従います。

1. 販売注文を開きます (例 : **すべての販売注文** ページから)。
1. **販売注文明細行** クイック タブで、注文明細行を選択します。
1. **販売注文明細行** クイック タブのツール バーで、**明細行の更新 \> 在庫 \> 在庫視覚化統合** を選択します。
1. 関連する引当 ID を入力します。

在庫状態の変更は、相殺モディファイアーの設定と一致します。
