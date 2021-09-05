---
title: 在庫の視覚化の構成
description: このトピックでは、在庫の視覚化を構成する方法について説明します。
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
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345036"
---
# <a name="inventory-visibility-configuration"></a>在庫の視覚化の構成

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

このトピックでは、在庫の視覚化を構成する方法について説明します。

## <a name="introduction"></a><a name="introduction"></a>概要

在庫の視覚化の使用を開始する前に、このトピックの説明に従って、次の構成を完了する必要があります。

- [データ ソースの構成](#data-source-configuration)
- [パーティションの構成](#partition-configuration)
- [製品インデックス階層の構成](#index-configuration)
- [引当の構成 (オプション)](#reservation-configuration)
- [既定の構成サンプル](#default-configuration-sample)

> [!NOTE]
> 在庫の視覚化の構成は、[Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration) で表示および編集できます。 構成が完了したら、アプリ内の **構成の更新** を選択します。

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>データ ソースの構成

データ ソースは、データの取得元のシステムを表します。 例には、`fno` (「Dynamics 365 Finance and Operations」アプリの略) や `pos` (「販売時点管理」の略) が含まれます。

データ ソースの構成には、次の部分が含まれています。

- 分析コード (分析コード マッピング)
- 物理的測定
- 計算メジャー

> [!NOTE]
> `fno` データ ソースは Dynamics 365 Supply Chain Management に対して引当されています。

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>分析コード (分析コード マッピング)

分析コードを構成する目的は、分析コードの組み合わせに基づいて、イベントやクエリを投稿する複数のシステム統合を標準化することです。

在庫の視覚化では、次の一般ベース分析コードがサポートされます。

| 分析コード タイプ | ベース分析コード |
|---|---|
| 品目 | `ColorId` |
| 品目 | `SizeId` |
| 品目 | `StyleId` |
| 品目 | `ConfigId` |
| 追跡 | `BatchId` |
| 追跡 | `SerialId` |
| 保管場所 | `LocationId` |
| 保管場所 | `SiteId` |
| 在庫状態 | `StatusId` |
| 倉庫固有 | `WMSLocationId` |
| 倉庫固有 | `WMSPalletId` |
| 倉庫固有 | `LicensePlateId` |
| その他 | `VersionId` |
| 在庫 (カスタム) | `InventDimension1` から `InventDimension12` |
| 内線 | `ExtendedDimension1` から `ExtendedDimension8` |

> [!NOTE]
> 前の表で表示されていた分析コード タイプは、参照専用です。 在庫の視覚化で定義する必要はありません。
>
> 在庫 (カスタム) 分析コードは、Supply Chain Management に対して引当されている場合があります。 その場合、代わりに拡張分析コードを使用できます。

外部システムは、RESTful API を介して在庫の視覚化にアクセスできます。 統合の場合、在庫の視覚化では _外部データ ソース_ と、_外部分析コード_ から _ベース分析コード_ へのマッピングを構成できます。 分析コードのマッピング テーブルの例を次に示します。

| 外部分析コード | ベース分析コード |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

分析コード マッピングを構成することで、外部分析コードを直接在庫の視覚化に送信できます。 次に、在庫の視覚化は外部分析コードをベース分析コードに自動的に変換します。

### <a name="physical-measures"></a>物理的測定

物理的測定は数量を変更し、在庫状態を反映します。 必要に応じて、独自の物理的測定を定義することができます。

在庫の視覚化は、Supply Chain Management (`fno` データ ソース) にリンクされている既定の物理的測定の一覧を提供します。 次の表に、物理的測定の例を示します。

| 物理的測定の名前 | 説明 |
|---|---|
| `NotSpecified` | 指定なし |
| `Arrived` | 着荷済 |
| `AvailOrdered` | 注文可能 |
| `AvailPhysical` | 引当可能現物数 |
| `Deducted` | 払出済 |
| `OnOrder` | OnOrder |
| `Ordered` | 発行済 |
| `PhysicalInvent` | 現物在庫 |
| `Picked` | 受取済 |
| `PostedQty` | 転記された数量 |
| `QuotationIssue` | 見積書発行 |
| `QuotationReceipt` | 見積受入 |
| `Received` | 受領済み |
| `Registered` | 登録済 |
| `ReservOrdered` | 発注引当済 |
| `ReservPhysical` | 引当済現物数 |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>計算メジャー

計算メジャーは、物理的測定の組み合わせで構成されるカスタマイズされた計算式を提供します。 この機能により、追加または削除される一連の物理的測定を定義して、カスタマイズされた測定を作成できるようになります。

たとえば、次のようなクエリ結果があります。

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

次に、次の表に示すように、`MyCustomAvailableforReservation` という名前の計算メジャーを構成します。 この計算メジャーは、消費システムによって消費されます。

| 消費システム | 計算メジャー | データ ソース | 物理的測定 | 計算タイプ |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

この計算式を使用すると、新しいクエリ結果にカスタマイズされた測定が含まれます。

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

カスタム測定での計算設定に基づく `MyCustomAvailableforReservation` の出力は、100+50+80+90+30–10–20–60–40=220 となります。

## <a name="partition-configuration"></a><a name="partition-configuration"></a>パーティションの構成

パーティションの構成は、ベース分析コードの組み合わせで構成されます。 データ配分パターンを定義します。 同じパーティション内のデータ操作は高パフォーマンスをサポートし、あまりコストもかかりません。 したがって、適切なパーティションのパターンは大きな利益をもたらします。

在庫の視覚化は、次の既定のパーティションの構成を提供します。

| ベース分析コード | 階層 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> 既定のパーティションの構成は参照専用です。 在庫の視覚化で定義する必要はありません。 現在、パーティションの構成のアップグレードはサポートされていません。

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>製品インデックス階層の構成

多くの場合、手持在庫クエリは、最高「合計」レベルのみだけではありません。 代わりに、在庫分析コードに基づいて集計される結果も表示することができます。

在庫の視覚化を使用すると、_インデックス_ を設定できるので、柔軟性を高めることができます。 これらのインデックスは、分析コードまたは分析コードの組み合わせに基づいています。 インデックスは、次の表で定義されているように、*セット番号*、*分析コード*、および *階層* で構成されています。

| 氏名 | 説明 |
|---|---|
| セット番号 | 同じセット (インデックス) に属する分析コードはグループ化され、同じセット番号が割り当てされます。 |
| 分析コード | クエリ結果が集計されるベース分析コード。 |
| 階層 | 階層は、クエリ可能なサポートされる分析コードの組み合わせを定義するために使用されます。 たとえば、`(ColorId, SizeId, StyleId)` という階層順序を持つ分析コード セットを設定します。 この場合、システムは 4 つの分析コードの組み合わせに対するクエリをサポートします。 最初の組み合わせは空、2 番目が `(ColorId)`、3 番目が `(ColorId, SizeId)`、4 番目が `(ColorId, SizeId, StyleId)` です。 その他の組み合わせはサポートされていません。 詳細については、次の例を参照してください。 |

### <a name="example"></a>例

このセクションでは、階層の仕組みを示す例を提供します。

在庫に次の項目があります。

| 項目 | ColorId | SizeId | StyleId | 件数 |
|---|---|---|---|---|
| T シャツ | 黒 | 小 | ワイド | 1 |
| T シャツ | 黒 | 小 | 通常 | 2 |
| T シャツ | 黒 | 大 | ワイド | 3 |
| T シャツ | 黒 | 大 | 通常 | 4 |
| T シャツ | 赤 | 小 | ワイド | 5 |
| T シャツ | 赤 | 小 | 通常 | 6 |
| T シャツ | 赤 | 大 | 通常 | 7 |

インデックスを次に示します。

| 設定番号 | 分析コード | 階層 |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

インデックスを使用すると、次の方法で手持在庫をクエリできます。

- `()` – すべてグループ化されます

    - T シャツ、28

- `(ColorId)` – `ColorId` 別にグループ化されます

    - T シャツ、黒、10
    - T シャツ、赤、18

- `(ColorId, SizeId)` – `ColorId` と `SizeId` の組み合わせ別にグループ化されます

    - T シャツ、黒、S、3
    - T シャツ、黒、L、7
    - T シャツ、赤、S、11
    - T シャツ、赤、L、7

- `(ColorId, SizeId, StyleId)` – `ColorId`、`SizeId` および `StyleId` の組み合わせ別にグループ化されます

    - T シャツ、黒、S、ワイド、1
    - T シャツ、黒、S、レギュラー、2
    - T シャツ、黒、L、ワイド、3
    - T シャツ、黒、L、レギュラー、4
    - T シャツ、赤、S、ワイド、5
    - T シャツ、赤、S、レギュラー、6
    - T シャツ、赤、L、レギュラー、7

> [!NOTE]
> パーティション構成で定義されたベース分析コードは、インデックス構成で定義しないでください。

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>引当の構成 (オプション)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

仮引当機能を使用する場合は、引当の構成が必要です。 構成は 2 つの基本的な部分で構成されています。

- 仮引当マッピング
- 仮引当階層

### <a name="soft-reservation-mapping"></a>仮引当マッピング

引当を行う際に、手持在庫が現在引当可能であるかどうかについて知りたい場合があります。 検証は、物理的測定の組み合わせの計算式を表す計算メジャーにリンクされます。

たとえば、引当測定は、`iv` (在庫の視覚化) データ ソース の `SoftReservOrdered` の物理的な測定に基づいています。 この場合、次に示すように、`iv` データ ソースの `AvailableToReserve` の計算メジャーを設定できます。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `AvailPhysical` |
| 加算 | `pos` | `Inbound` |
| 減算 | `pos` | `Outbound` |
| 減算 | `iv` | `SoftReservOrdered` |

その後、仮引当マッピングを設定して、`SoftReservOrdered` 引当測定から `AvailableToReserve` 計算メジャーへのマッピングを提供します。

| 物理的測定データ ソース | 物理的測定 | 引当データ ソースで使用可能 | 引当計算メジャーで使用可能 |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

これで、`SoftReservOrdered` で引当を行うと、在庫の視覚化によって自動的に `AvailableToReserve` とその関連計算式が検出され、引当の検証が行われます。

たとえば、在庫の視覚化に次の手持在庫があるとします。

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

この場合、次の計算が適用されます。

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
=70+50–20–90  
=10

したがって、`iv.SoftReservOrdered` で引当を行う場合、数量が `AvailableToReserve` (10) 以下であれば引当を実行できます。

### <a name="soft-reservation-hierarchy"></a>仮引当階層

引当階層は、引当の際に指定する必要がある分析コードの順序を表します。 これは、手持在庫クエリに対して製品インデックス階層が機能するのと同じように機能します。

引当階層は製品インデックス階層には依存しません。 この独立性により、ユーザーが分析コードを詳細に分割して、より正確な引当の要件を指定できるカテゴリ管理を実装できます。

仮引当階層の例を次に示します。

| ベース分析コード | 階層 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

この例では、次の分析コード順序で引当を実行できます。

- `()` – 分析コードは指定されていません。
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

有効な分析コード順序は、分析コードごとに引当階層に厳密に従う必要があります。 たとえば、階層順序 `(SiteId, LocationId, SizeId)` は `ColorId` が欠落しているため無効です。

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>既定の構成サンプル

初期化段階では、在庫の視覚化によって既定の構成が設定されます。 必要に応じて構成を変更できます。

### <a name="data-source-configuration"></a>データ ソースの構成

#### <a name="configuration-of-the-iv-data-source"></a>iv データ ソースの構成

このセクションでは、`iv` データ ソースの構成方法について説明します。

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>iv データ ソース用に構成された物理的測定

次の物理的測定は、`iv` データ ソース用に構成されています。

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>OrderedTotal 計算メジャー

次の表に示すように、`OrderedTotal` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 測定 |
|---|---|---|
| 加算 | `fno` | `Ordered` |
| 加算 | `fno` | `Arrived` |
| 加算 | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>OnHand 計算メジャー

次の表に示すように、`OnHand` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `PhysicalInvent` |
| 加算 | `iom` | `OnHand` |
| 加算 | `erp` | `Unrestricted` |
| 加算 | `erp` | `QualityInspection` |
| 加算 | `pos` | `PosInbound` |
| 減算 | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>ReservedTotal 計算メジャー

次の表に示すように、`ReservedTotal` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `ReservPhysical` |
| 加算 | `fno` | `ReservOrdered` |
| 加算 | `iv` | `SoftReservPhysical` |
| 加算 | `iv` | `SoftReservOrdered` |
| 加算 | `iv` | `ReservPhysical` |
| 加算 | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>SoftReserved 計算メジャー

次の表に示すように、`SoftReserved` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `iv` | `SoftReservPhysical` |
| 加算 | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>HardReserved 計算メジャー

次の表に示すように、`HardReserved` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `ReservPhysical` |
| 加算 | `fno` | `ReservOrdered` |
| 加算 | `iv` | `ReservPhysical` |
| 加算 | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>OpenOrder 計算メジャー

次の表に示すように、`OpenOrder` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `OnOrder` |
| 加算 | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>OnHandAvailable 計算メジャー

次の表に示すように、`OnHandAvailable` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `PhysicalInvent` |
| 加算 | `iom` | `OnHand` |
| 加算 | `erp` | `Unrestricted` |
| 加算 | `erp` | `QualityInspection` |
| 加算 | `pos` | `PosInbound` |
| 減算 | `fno` | `ReservPhysical` |
| 減算 | `iv` | `SoftReservPhysical` |
| 減算 | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>AvailableToReserve 計算メジャー

次の表に示すように、`AvailableToReserve` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `PhysicalInvent` |
| 加算 | `iom` | `OnHand` |
| 加算 | `erp` | `Unrestricted` |
| 加算 | `erp` | `QualityInspection` |
| 加算 | `pos` | `PosInbound` |
| 加算 | `fno` | `Ordered` |
| 加算 | `fno` | `Arrived` |
| 加算 | `iv` | `Ordered` |
| 減算 | `fno` | `ReservPhysical` |
| 減算 | `fno` | `ReservOrdered` |
| 減算 | `iv` | `SoftReservPhysical` |
| 減算 | `iv` | `SoftReservOrdered` |
| 減算 | `iv` | `ReservPhysical` |
| 減算 | `iv` | `ReservOrdered` |
| 減算 | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>InventorySupply 計算メジャー

次の表に示すように、`InventorySupply` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `Ordered` |
| 加算 | `fno` | `Arrived` |
| 加算 | `iv` | `Ordered` |
| 加算 | `fno` | `PhysicalInvent` |
| 加算 | `iom` | `OnHand` |
| 加算 | `erp` | `Unrestricted` |
| 加算 | `erp` | `QualityInspection` |
| 加算 | `pos` | `PosInbound` |
| 減算 | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>InventoryDemand 計算メジャー

次の表に示すように、`InventoryDemand` 計算メジャーは `iv` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `OnOrder` |
| 加算 | `iom` | `OnOrder` |
| 加算 | `iv` | `SoftReservPhysical` |
| 加算 | `iv` | `SoftReservOrdered` |
| 加算 | `fno` | `ReservPhysical` |
| 加算 | `fno` | `ReservOrdered` |
| 加算 | `iv` | `ReservPhysical` |
| 加算 | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>fno データ ソースの構成

このセクションでは、`fno` データ ソースの構成方法について説明します。

##### <a name="dimension-mappings-for-the-fno-data-source"></a>fno データ ソースの分析コード マッピング

次の表に示す分析コード マッピングは、`fno` データ ソース用に構成されています。

| 外部分析コード | ベース分析コード |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>fno データ ソース用に構成された物理的測定

次の物理的測定は、`fno` データ ソース用に構成されています。

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>pos データ ソースの構成

このセクションでは、データ ソース `pos` の構成方法について説明します。

##### <a name="physical-measures-for-the-pos-data-source"></a>pos データ ソース用の物理的測定

次の物理的測定は、`pos` データ ソース用に構成されています。

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity 計算メジャー

次の表に示すように、`AvailQuantity` 計算メジャーは `pos` データ ソース用に構成されています。

| 計算タイプ | データ ソース | 物理的測定 |
|---|---|---|
| 加算 | `fno` | `AvailPhysical` |
| 加算 | `pos` | `PosInbound` |
| 減算 | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>iom データ ソースの構成

次の物理的測定は、`iom` (Intelligent Order Management) データ ソース用に構成されています。

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>erp データ ソースの構成

次の物理的測定は、`erp` (エンタープライズ リソース プランニング) データ ソース用に構成されています。

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>パーティションの構成

次の表に、既定のパーティションの構成を示します。

| ベース分析コード | 階層 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>インデックスの構成

次の表に、既定のインデックスの構成を示します。

| 設定番号 | 分析コード | 階層 |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>引当の構成

このセクションでは、既定引当の構成について説明します。

#### <a name="reservation-mapping"></a>引当マッピング

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

次の表に、既定の引当マッピングを示します。

| 物理的測定データ ソース | 物理的測定 | 引当データ ソースで使用可能 | 引当計算メジャーで使用可能 |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>引当階層

次の表に、既定の引当階層を示します。

| ベース分析コード | 階層 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
