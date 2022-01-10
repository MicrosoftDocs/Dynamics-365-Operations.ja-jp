---
title: 在庫の視覚化のコンフィギュレーション
description: このトピックでは、在庫の視覚化を構成する方法について説明します。
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: fcbace2bd28a843fca8aa2f4f998c08f238c29d6
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920301"
---
# <a name="configure-inventory-visibility"></a>在庫の視覚化のコンフィギュレーション

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

このトピックでは、Power Apps で、在庫視覚化アプリを使用して在庫視覚化を構成する方法を説明します。

## <a name="introduction"></a><a name="introduction"></a>概要

在庫の視覚化の使用を開始する前に、このトピックの説明に従って、次の構成を完了する必要があります。

- [データ ソースの構成](#data-source-configuration)
- [パーティションの構成](#partition-configuration)
- [製品インデックス階層の構成](#index-configuration)
- [引当の構成 (オプション)](#reservation-configuration)
- [既定の構成サンプル](#default-configuration-sample)

## <a name="prerequisites"></a>必要条件

開始する前に、[在庫視覚化のインストールと設定](inventory-visibility-setup.md)で示されているように、在庫視覚化アドインのインストールと設定を行います。

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Power Apps の機能管理で在庫視覚化機能を有効にする

在庫視覚化アドインは、Power Apps のインストールにいくつかの新機能を追加します。 既定では、これらの機能は無効になっています。 これらを使用するには、Power Apps の **構成** ページを開き、**機能管理** タブで以下の機能を有効にします。

- *OnHandReservation*
- *OnHandMostSpecificBackgroundService*

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>サービス エンドポイントを検索する

在庫視覚化サービスの正しいエンドポイントが分からない場合、Power Apps の **構成** ページを開き、右上隅の **サービス エンドポイントの表示** を選択します。 ページに正しいサービス エンドポイントが表示されます。

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>在庫視覚化アプリの構成ページ

Power Apps で、[在庫視覚化アプリ](inventory-visibility-power-platform.md) の **構成** ぺージで手持構成および仮引当構成の設定をサポートします。 アドインをインストールすると、既定の構成に Microsoft Dynamics 365 Supply Chain Management (`fno` データ ソース) からの値が含まれます。 既定の設定を確認できます。 また、業務要件や外部システムの在庫転記要件に基づき、複数のシステム間で在庫変更を転記、整理、およびクエリする方法を標準化するように構成を変更することができます。 このトピックの残りのセクションでは、**構成** ページの各部分の使い方について説明します。

構成の完了後、必ずアプリ内の **構成の更新** を選択してください。

## <a name="data-source-configuration"></a>データ ソースの構成

各データ ソースは、データの取得元のシステムを表しています。 データソース名の例としては、`fno` ("Dynamics 365 Finance and Operations アプリ" の略) および `pos` ("販売時点管理" の略) が含まれます。 既定では、Supply Chain Management が在庫視覚化の既定のデータ ソース (`fno`) として設定されます。

> [!NOTE]
> `fno` データ ソースは Supply Chain Management 用に予約されています。 在庫の可視性アドインが Supply Chain Management 環境と統合されている場合は、データソースの `fno` に関連する設定を削除しないことをお勧めします。

データ ソースを追加するには、次の手順に従います。

1. Power Apps 環境にサインインし、**在庫視覚化** を開きます。
1. **構成** ページを開きます。
1. **データ ソース** タブで **新しいデータ ソース** を選択してデータ ソースを追加します。

> [!NOTE]
> データ ソースを追加する場合、在庫視覚化サービスの構成を更新する前に、データ ソースの名前、物理的測定、および分析コードのマッピングを検証してください。 **構成の更新** を選択した後は、これらの設定を変更することはできません。

データ ソースの構成には、次の部分が含まれています。

- 分析コード (分析コード マッピング)
- 物理的測定
- 計算メジャー

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>分析コード (分析コード マッピング)

分析コードを構成する目的は、分析コードの組み合わせに基づいて、イベントやクエリを投稿する複数のシステム統合を標準化することです。 在庫視覚化は、データ ソースの分析コードからマッピングできるベース分析コードの一覧を提供します。 33 個の分析コードをマッピングに使用することができます。

- 既定では、データ ソースの 1 つとして Supply Chain Management を使用している場合、Supply Chain Management の標準分析コードに 13 の分析コードがマップされます。 他の 12 の分析コード (`inventDimension1` から `inventDimension12`) が Supply Chain Management のカスタム分析コードにマッピングされます。 残りの 8 つの分析コードは、外部データ ソースにマップできる拡張分析コードです。
- データ ソースの 1 つとして Supply Chain Management を使用しない場合、分析コードを自由にマップすることができます。 使用可能な分析コードの完全な一覧を次の表に示します。

> [!NOTE]
> 分析コードが既定の分析コードの一覧に含まれておらず、外部データ ソースを使用している場合は、`ExtendedDimension1` から `ExtendedDimension8` を使用してマッピングを行うことをお勧めします。

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
| 拡張機能 | `ExtendedDimension1` から `ExtendedDimension8` |
| System | `Empty` |

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

分析コード マッピングを追加するには、次の手順に従います。

1. Power Apps 環境にサインインし、**在庫視覚化** を開きます。
1. **構成** ページを開きます。
1. **データ ソース** タブの **分析コード マッピング** セクションで **追加** を選択して、分析コード マッピングを追加します。
    ![分析コード マッピングの追加](media/inventory-visibility-dimension-mapping.png "分析コード マッピングの追加")

1. **分析コード名** フィールドで、ソース分析コードを指定します。
1. **終了分析コード** フィールドで、マップする在庫視覚化の分析コードを選択します。
1. **保存** を選択します。

たとえば、データ ソースに製品のカラー分析コードが含まれる場合、`exterchannel` データ ソースで `ProductColor` カスタム分析コードを追加して、`ColorId` ベース分析コードにマップすることができます。 `ColorId` ベース分析コードにマップされます。

### <a name="physical-measures"></a>物理的測定

データ ソースが在庫の変更を在庫視覚化に転記する場合、*物理的測定* を使用してその変更を転記します。 物理的測定は数量を変更し、在庫状態を反映します。 必要に応じて、独自の物理的測定を定義することができます。 クエリは、物理的測定に基づくことがあります。

在庫の視覚化は、Supply Chain Management (`fno` データ ソース) にリンクされている既定の物理的測定の一覧を提供します。 これら既定の物理的測定は、Supply Chain Management (**在庫管理 \> 照会およびレポート \> 手持在庫リスト**) の **手持在庫リスト** ページにある在庫トランザクションの状態から取得されます。 次の表に、物理的測定の例を示します。

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

データ ソースが Supply Chain Management である場合、既定の物理的測定を再作成する必要はありません。 ただし、外部データ ソースの場合は、次の手順に従って新しい物理的測定を作成することができます。

1. Power Apps 環境にサインインし、**在庫視覚化** を開きます。
1. **構成** ページを開きます。
1. **データ ソース** タブの **物理的測定** セクションで **追加** を選択し、ソース測定の名前を指定して、変更を保存します。

### <a name="calculated-measures"></a>計算メジャー

在庫視覚化を使用して、在庫の物理的測定と *カスタム計算測定* の両方を照会できます。 計算メジャーは、物理的測定の組み合わせで構成されるカスタマイズされた計算式を提供します。 この機能により、追加または削除される一連の物理的測定を定義して、カスタマイズされた測定を作成できるようになります。

構成により、合計集計された出来高数量を取得するために加算または減算する一連のモディファイアーを定義できます。

カスタム計算測定を設定するには、次の手順に従います。

1. Power Apps 環境にサインインし、**在庫視覚化** を開きます。
1. **構成** ページを開きます。
1. **計算測定** タブで **新しい計測** を選択し、計算された測定を追加します。 その後、次の表の説明に従ってフィールドを設定します。

    | フィールド | 先頭値 |
    |---|---|
    | 新しい計算測定の名前 | 計算測定の名前を入力します。 |
    | データ ソース | 照会しているシステムはデータ ソースです。 |
    | モディファイアーのデータ ソース | モディファイアーのデータ ソースを入力します。 |
    | モディファイアー | モディファイアーの名前を入力します。 |
    | モディファイアー タイプ | モディファイアー タイプ (*加算* または *減算*) を選択します。 |

例えば、次のようなクエリ結果があるとします。

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

カスタム測定での計算設定に基づく `MyCustomAvailableforReservation` の出力は、100+50–10+80–20+90+30–60–40=220 となります。

## <a name="partition-configuration"></a><a name="partition-configuration"></a>パーティションの構成

現在、パーティション構成は、データの分散方法を示す 2 つの基本分析コード (`SiteId` と `LocationId`) で構成されています。 同じパーティションで運用することで、より高いパフォーマンスを低コストで実現できます。 次の表は、在庫の視覚化アドインが提供する規定のパーティション構成です。

| ベース分析コード | 階層 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

ソリューションには、このパーティション構成が規定で含まれています。 したがって、 *自分で定義する必要はありません*。

> [!IMPORTANT]
> 既定のパーティション構成をカスタマイズしないでください。 それを削除したり変更したりすると、予期せぬエラーが発生する可能性があります。

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>製品インデックス階層の構成

多くの場合、手持在庫クエリは、最高「合計」レベルのみだけではありません。 代わりに、在庫分析コードに基づいて集計される結果も表示することができます。

在庫の視覚化を使用すると、_インデックス_ を設定できるので、柔軟性を高めることができます。 これらのインデックスは、分析コードまたは分析コードの組み合わせに基づいています。 インデックスは、次の表で定義されているように、*セット番号*、*分析コード*、および *階層* で構成されています。

| 氏名 | 説明 |
|---|---|
| セット番号 | 同じセット (インデックス) に属する分析コードはグループ化され、同じセット番号が割り当てされます。 |
| 分析コード | クエリ結果が集計されるベース分析コード。 |
| 階層 | 階層は、クエリ可能なサポートされる分析コードの組み合わせを定義するために使用されます。 たとえば、`(ColorId, SizeId, StyleId)` という階層順序を持つ分析コード セットを設定します。 この場合、システムは 4 つの分析コードの組み合わせに対するクエリをサポートします。 最初の組み合わせは空、2 番目が `(ColorId)`、3 番目が `(ColorId, SizeId)`、4 番目が `(ColorId, SizeId, StyleId)` です。 その他の組み合わせはサポートされていません。 詳細については、次の例を参照してください。 |

製品階層インデックスを設定するには、以下の手順に従ってください。

1. Power Apps 環境にサインインし、**在庫視覚化** を開きます。
1. **構成** ページを開きます。
1. **製品階層インデックス** タブの **分析コード マッピング** セクションで **追加** を選択して、分析コード マッピングを追加します。
1. 既定では、インデックスの一覧が用意されています。 既存のインデックスを変更するには、関連するインデックスのセクションで **編集** または **追加** を選択します。 新しいインデックス セットを作成するには、**新しいインデックス セット** を選択します。 すべてのインデックス セットの各行の **分析コード** フィールドで、ベース分析コードの一覧から選択します。 次のフィールドの値は自動的に生成されます。

    - **セット番号** – 同じグループ (インデックス) に属する分析コードはグループ化され、同じセット番号が割り当てされます。
    - **階層** – 階層は、分析コード グループ (インデックス) でクエリ可能できるようサポートされる分析コードの組み合わせを定義するために使用されます。 たとえば、*スタイル*、*色*、および *サイズ* の階層の順序が設定されている分析コード グループを設定する場合、システムは 3 つのクエリ グループの結果をサポートします。 1 つ目のグループはスタイルのみです。 2 つ目のグループはスタイルおよび色の組み合わせです。 3 つ目のグループはスタイル、色、およびサイズの組み合わせです。 その他の組み合わせはサポートされていません。

### <a name="example"></a>例

このセクションでは、階層の仕組みを示す例を提供します。

次の表に、このサンプルで使用可能な在庫の一覧を示します。

| 項目 | ColorId | SizeId | StyleId | 件数 |
|---|---|---|---|---|
| T シャツ | 黒 | 小 | ワイド | 1 |
| T シャツ | 黒 | 小 | 通常 | 2 |
| T シャツ | 黒 | 大 | ワイド | 3 |
| T シャツ | 黒 | 大 | 通常 | 4 |
| T シャツ | 赤 | 小 | ワイド | 5 |
| T シャツ | 赤 | 小 | 通常 | 6 |
| T シャツ | 赤 | 大 | 通常 | 7 |

インデックス階層の設定方法を次の表に示します。

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
> 
> すべての分析コードの組み合わせによって集計された在庫のみをクエリする必要がある場合は、基本分析コード `Empty` を含む単一のインデックスを設定できます。

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>引当の構成 (オプション)

仮引当機能を使用する場合は、引当の構成が必要です。 構成は 2 つの基本的な部分で構成されています。

- 仮引当マッピング
- 仮引当階層

### <a name="soft-reservation-mapping"></a>仮引当マッピング

引当を行う際に、手持在庫が現在引当可能であるかどうかについて知りたい場合があります。 検証は、物理的測定の組み合わせの計算式を表す計算メジャーにリンクされます。

物理的測定から計算メジャーへのマッピングを設定することにより、在庫視覚化サービスを有効にし、物理的測定に基づいて、引当可能在庫数を自動的に検証することができます。

このマッピングを設定する前に、(このトピックで前述されているように) Power Apps の **構成** ページの **データ ソース** タブと **計算メジャー** タブで、物理的測定、計算メジャー、およびそれらのデータ ソースを定義する必要があります。

仮引当マッピングを定義するには、次の手順に従います。

1. 仮引当測定として機能する物理的測定を定義します (`SoftReservOrdered` など)。
1. **構成** ページの **計算メジャー** タブで、物理的計測にマップする AFR 計算式を含む、*引当に使用可能な* (AFR) 計算メジャーを定義します。 たとえば、`AvailableToReserve` (引当に使用可能) を設定し、以前に定義された `SoftReservOrdered` 物理的測定にマップすることができます。 このようにして、引当に使用可能になる `SoftReservOrdered` 在庫状態の数量を検索できます。 次の表は、AFR 計算式を示しています。

    | 計算タイプ | データ ソース | 物理的測定 |
    |---|---|---|
    | 加算 | `fno` | `AvailPhysical` |
    | 加算 | `pos` | `Inbound` |
    | 減算 | `pos` | `Outbound` |
    | 減算 | `iv` | `SoftReservOrdered` |

    引当測定の基になる物理的測定が含まれるように、計算メジャーを設定することをお勧めします。 このようにして、計算メジャー数量は、引当測定数量の影響を受けます。 したがって、この例では、`iv` データー ソースの `AvailableToReserve` 計算メジャーには、コンポーネント として `iv` からの `SoftReservOrdered` 物理測定を含む必要があります。

1. **構成** ページを開きます。
1. **仮引当マッピング** タブで、物理的測定から計算メジャーへのマッピングを設定します。 前の例の場合、次の設定を使用して、以前に定義された `SoftReservOrdered` 物理測定に `AvailableToReserve` をマップすることができます。

    | 物理的測定データ ソース | 物理的測定 | 引当データ ソースで使用可能 | 引当計算メジャーで使用可能 |
    |---|---|---|---|
    | `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > **仮引当マッピング** タブで編集できない場合、**機能管理** タブの *OnHandReservation* 機能を有効にしなければならない場合があります。

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

> [!NOTE]
> 引当 API を呼び出す際に、要求本文のブール値 `ifCheckAvailForReserv` パラメーターを指定することで、引当の検証を制御できます。 `True` という値は検証が必要であることを意味するのに対し、`False` という値は検証が必要ないことを意味します。 既定値は [`True`] です。

### <a name="soft-reservation-hierarchy"></a>仮引当階層

引当階層は、引当の際に指定する必要がある分析コードの順序を表します。 これは、手持在庫クエリに対して製品インデックス階層が機能するのと同じように機能します。

引当階層は製品インデックス階層には依存しません。 この独立性により、ユーザーが分析コードを詳細に分割して、より正確な引当の要件を指定できるカテゴリ管理を実装できます。 仮引当階層には、コンポーネントとして `SiteId` および `LocationId` が含まれている必要がありますが、これはパーティションの構成を構築するためです。 引当を行う場合は、製品のパーティションを指定する必要があります。

仮引当階層の例を次に示します。

| ベース分析コード | 階層 |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

この例では、次の分析コード順序で引当を実行できます。 引当を行う場合は、製品のパーティションを指定する必要があります。 したがって、使用できる基本的な階層は `(SiteId, LocationId)` となります。

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

有効な分析コード順序は、分析コードごとに引当階層に厳密に従う必要があります。 たとえば、階層順序 `(SiteId, LocationId, SizeId)` は `ColorId` が欠落しているため無効です。

## <a name="complete-and-update-the-configuration"></a>構成の完了と更新

構成が完了した後、すべての変更を在庫視覚化にコミットする必要があります。 変更をコミットするには、Power Apps の **構成** ページの右上隅にある **構成の更新** を選択します。

**構成の更新** を初めて選択するとき、システムは資格情報を要求します。

- **クライアント ID** – 在庫視覚化のために作成した Azure アプリケーション ID。
- **テナント ID** – Azure テナント ID。
- **クライアント シークレット** – 在庫視覚化のために作成した Azure アプリケーション シークレット。

サインインした後、在庫視覚化サービスで構成が更新されます。

> [!NOTE]
> 在庫視覚化サービスの構成を更新する前に、データ ソースの名前、物理的測定、および分析コードのマッピングを検証してください。 **構成の更新** を選択した後は、これらの設定を変更することはできません。

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>既定の構成サンプル

初期化の段階では、在庫視覚化が既定の構成を設定しますが、その詳細はこちらをごらんください。 必要に応じてこの構成を変更できます。

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
